---
title: Synkronoi tuoteluokitukset Dynamics 365 Retailissa
description: Tässä ohjeaiheessa kerrotaan, miten tuoteluokitukset synkronoidaan Microsoft Dynamics 365 Retail -sovelluksessa.
author: gvrmohanreddy
manager: annbe
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: gmohanv
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: db5a4e1f78797d20ded2274cc99bef422fd50acc
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/01/2019
ms.locfileid: "2698162"
---
# <a name="sync-product-ratings-in-dynamics-365-retail"></a><span data-ttu-id="2c965-103">Synkronoi tuoteluokitukset Dynamics 365 Retailissa</span><span class="sxs-lookup"><span data-stu-id="2c965-103">Sync product ratings in Dynamics 365 Retail</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="2c965-104">Tässä ohjeaiheessa kerrotaan, miten tuoteluokitukset synkronoidaan Microsoft Dynamics 365 Retail -sovelluksessa.</span><span class="sxs-lookup"><span data-stu-id="2c965-104">This topic describes how to sync product ratings in Microsoft Dynamics 365 Retail.</span></span>

## <a name="overview"></a><span data-ttu-id="2c965-105">Yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="2c965-105">Overview</span></span>

<span data-ttu-id="2c965-106">Jotta monikanavien, kuten myyntipisteen ja puhelinkeskusten, tuoteluokituksia voidaan käyttää, luokitusten ja arvostelujen palvelun tuotteiden luokitukset on tuotava Retail-sovelluksen kanavatietokantaan.</span><span class="sxs-lookup"><span data-stu-id="2c965-106">To consume product ratings in omnichannels, such as at the point of sale (POS) and in call centers, product ratings from the ratings and reviews service must be imported into the Retail channel database.</span></span> <span data-ttu-id="2c965-107">Kun tuoteluokitukset ovat käytettävissä monikanavissa, ne auttavat asiakkaita epäsuorasti myyjien kanssa tehtävässä vuorovaikutuksessa.</span><span class="sxs-lookup"><span data-stu-id="2c965-107">When product ratings are made available in omnichannels, they can help customers indirectly during their interactions with sales associates.</span></span>

<span data-ttu-id="2c965-108">Tässä ohjeaiheessa esitellään seuraavat tehtävät:</span><span class="sxs-lookup"><span data-stu-id="2c965-108">This topic describes following tasks:</span></span>

1. <span data-ttu-id="2c965-109">Määritä Retail-erätyö ja tuo tuoteluokitukset.</span><span class="sxs-lookup"><span data-stu-id="2c965-109">Configure a Retail batch job to import product ratings.</span></span>
1. <span data-ttu-id="2c965-110">Tarkista, että tuoteluokituksen synkronoinnin erätyö onnistui.</span><span class="sxs-lookup"><span data-stu-id="2c965-110">Verify that the batch job for product rating synchronization was successful.</span></span>
1. <span data-ttu-id="2c965-111">Määritä tuoteluokitukset käytettäviksi myyntipisteessä.</span><span class="sxs-lookup"><span data-stu-id="2c965-111">Make product ratings available at the POS.</span></span>

## <a name="configure-a-retail-batch-job-to-import-product-ratings"></a><span data-ttu-id="2c965-112">Retail-erätyön määrittäminen tuoteluokitusten tuontia varten</span><span class="sxs-lookup"><span data-stu-id="2c965-112">Configure a Retail batch job to import product ratings</span></span>

> [!IMPORTANT]
> <span data-ttu-id="2c965-113">Varmista ennen aloittamista, että asennettuna on Retail-versio 10.0.6 tai uudempi versio.</span><span class="sxs-lookup"><span data-stu-id="2c965-113">Before you start, make sure that version 10.0.6 or later of Retail is installed.</span></span>

### <a name="initialize-the-retail-scheduler"></a><span data-ttu-id="2c965-114">Retail-ajastuksen alustaminen</span><span class="sxs-lookup"><span data-stu-id="2c965-114">Initialize the retail scheduler</span></span>

<span data-ttu-id="2c965-115">Alusta Retail-ajastus noudattamalla seuraavia vaiheita:</span><span class="sxs-lookup"><span data-stu-id="2c965-115">To initialize the retail scheduler, follow these steps.</span></span>

1. <span data-ttu-id="2c965-116">Siirry kohtaan **Retail \> Headquarters-asetus \> Retail-ajastus \> Alusta Retail-ajastus**.</span><span class="sxs-lookup"><span data-stu-id="2c965-116">Go to **Retail \> Headquarters setup \> Retail scheduler \> Initialize retail scheduler**.</span></span> <span data-ttu-id="2c965-117">Vaihtoehtoisesti voit tehdä haun käyttämällä Alusta Retail-ajoitus -lausetta.</span><span class="sxs-lookup"><span data-stu-id="2c965-117">Alternatively, search for "Initialize retail scheduler."</span></span>
1. <span data-ttu-id="2c965-118">Varmista **Alusta Retail-ajastus** -valintaikkunassa, että **Poista olemassa oleva määritys** -vaihtoehdon arvoksi on määritetty **Ei**. Valitse sitten **OK**.</span><span class="sxs-lookup"><span data-stu-id="2c965-118">In the **Initialize retail scheduler** dialog box, make sure that the **Delete existing configuration** option is set to **No**, and then select **OK**.</span></span>

### <a name="verify-the-retailproductrating-subjob"></a><span data-ttu-id="2c965-119">RetailProductRating-alityön tarkistaminen</span><span class="sxs-lookup"><span data-stu-id="2c965-119">Verify the RetailProductRating subjob</span></span>

<span data-ttu-id="2c965-120">Seuraavalla tavalla voit tarkistaa, että **RetailProductRating**-alityö on olemassa.</span><span class="sxs-lookup"><span data-stu-id="2c965-120">To verify that the **RetailProductRating** subjob exists, follow these steps.</span></span>

1. <span data-ttu-id="2c965-121">Siirry kohtaan **Retail \> Headquarters-asetus \> Retail-ajastus \> Ajastuksen alityöt**.</span><span class="sxs-lookup"><span data-stu-id="2c965-121">Go to **Retail \> Headquarters setup \> Retail scheduler \> Scheduler subjobs**.</span></span> <span data-ttu-id="2c965-122">Vaihtoehtoisesti voit tehdä haun käyttämällä Ajastuksen alityöt -lausetta.</span><span class="sxs-lookup"><span data-stu-id="2c965-122">Alternatively, search for "Scheduler subjobs."</span></span>
1. <span data-ttu-id="2c965-123">Etsi alityöluettelosta **RetailProductRating**-alityö tai hae sitä.</span><span class="sxs-lookup"><span data-stu-id="2c965-123">In the subjob list, find or search for the **RetailProductRating** subjob.</span></span>

<span data-ttu-id="2c965-124">Seuraavassa kuvassa on esimerkki Retail-sovelluksen alityön tiedoista.</span><span class="sxs-lookup"><span data-stu-id="2c965-124">The following illustration shows an example of the subjob details in Retail.</span></span>

![RetailProductRating-alityön tiedot](media/rnr-hq-ratings-sub-job.png)

> [!NOTE]
> <span data-ttu-id="2c965-126">Jos et löydä **RetailProductRating**-alityötä, **Synkronoi tuoteluokitukset** -työ on jo ehkä suoritettu ja **1040 CDX**-työ on jo ehkä suoritettu ennen Retail-ajastuksen alustusta.</span><span class="sxs-lookup"><span data-stu-id="2c965-126">If you don't find the **RetailProductRating** subjob, you might already have run the **Sync product ratings** job and the **1040 CDX** job before you initialized the retail scheduler.</span></span> <span data-ttu-id="2c965-127">Tässä tapauksessa suorita **Tietojen täydellinen synkronointi** -työ seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="2c965-127">In this case, follow these steps to run the **Full data sync** job.</span></span>
>
> 1. <span data-ttu-id="2c965-128">Siirry kohtaan **Retail \> Headquarters-asetus \> Retail-ajastus \> Kanavatietokanta**.</span><span class="sxs-lookup"><span data-stu-id="2c965-128">Go to **Retail \> Headquarters setup \> Retail scheduler \> Channel database**.</span></span> <span data-ttu-id="2c965-129">Vaihtoehtoisesti voit tehdä haun käyttämällä kanavatietokanta-sanaa.</span><span class="sxs-lookup"><span data-stu-id="2c965-129">Alternatively, search for "Channel database."</span></span>
> 1. <span data-ttu-id="2c965-130">Valitse synkronoitava kanavatietokanta.</span><span class="sxs-lookup"><span data-stu-id="2c965-130">Select the channel database to sync.</span></span>
> 1. <span data-ttu-id="2c965-131">Valitse toimintoruudusta **Tietojen täydellinen synkronointi**.</span><span class="sxs-lookup"><span data-stu-id="2c965-131">On the Action Pane, select **Full data sync**.</span></span>
> 1. <span data-ttu-id="2c965-132">Valitse avattavasta **Valitse jakeluaikataulu** -luettelosta **1040 - tuotteet** ja valitse sitten **OK**.</span><span class="sxs-lookup"><span data-stu-id="2c965-132">In the **Select a distribution schedule** drop-down dialog box, select **1040 - products**, and then select **OK**.</span></span>
> 1. <span data-ttu-id="2c965-133">Toista edellisen proseduurin vaiheet ja varmista, että **RetailProductRating**-alityö on luotu.</span><span class="sxs-lookup"><span data-stu-id="2c965-133">Repeat the steps of the previous procedure to verify that the **RetailProductRating** subjob has been created.</span></span>

### <a name="import-product-ratings"></a><span data-ttu-id="2c965-134">Tuoteluokitusten tuominen</span><span class="sxs-lookup"><span data-stu-id="2c965-134">Import product ratings</span></span>

<span data-ttu-id="2c965-135">Voit tuoda tuoteluokitukset Retail-sovelluksiin luokitusten ja arvostelujen palvelusta seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="2c965-135">To import product ratings into Retail from the ratings and reviews service, follow these steps.</span></span>

1. <span data-ttu-id="2c965-136">Siirry kohtaan **Retail \> Headquarters-asetus \> Retail-ajastus \> Synkronoi tuoteluokitukset -työ**.</span><span class="sxs-lookup"><span data-stu-id="2c965-136">Go to **Retail \> Headquarters setup \> Retail scheduler \> Sync product ratings job**.</span></span> <span data-ttu-id="2c965-137">Vaihtoehtoisesti voit tehdä haun käyttämällä Synkronoi tuoteluokitukset -työ -lausetta.</span><span class="sxs-lookup"><span data-stu-id="2c965-137">Alternatively, search for "Sync product ratings job."</span></span>
1. <span data-ttu-id="2c965-138">Valitse **Nouda tuoteluokitukset** -valintaikkunan **Suorita taustalla** -pikavälilehdessä **Toistuminen**.</span><span class="sxs-lookup"><span data-stu-id="2c965-138">In the **Pull product ratings** dialog box, on the **Run in the background** FastTab, select **Recurrence**.</span></span>
1. <span data-ttu-id="2c965-139">Määritä **Määritä toistuminen** -valintaikkunassa toistumisen malli.</span><span class="sxs-lookup"><span data-stu-id="2c965-139">In the **Define recurrence** dialog box, set up a recurrence pattern.</span></span> <span data-ttu-id="2c965-140">(Ehdotettu arvo on kaksi tuntia.) Älä ajoita toistumista, joka on pienempi kuin yksi tunti.</span><span class="sxs-lookup"><span data-stu-id="2c965-140">(The suggested value is two hours.) Don't schedule a recurrence that is less than one hour.</span></span>
1. <span data-ttu-id="2c965-141">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="2c965-141">Select **OK**.</span></span>
1. <span data-ttu-id="2c965-142">Määritä **Eräkäsittely**-vaihtoehdon arvoksi **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="2c965-142">Set the **Batch process** option to **Yes**.</span></span> <span data-ttu-id="2c965-143">Tämän asetuksen avulla voidaan varmistaa, että lokeja voi valvoa ja että erätyön suorituksen tilan voi tarkistaa.</span><span class="sxs-lookup"><span data-stu-id="2c965-143">This setting helps guarantee that you will be able to audit the logs and verify the status of batch job runs.</span></span>
1. <span data-ttu-id="2c965-144">Ajoita erätyö valitsemalla **OK**.</span><span class="sxs-lookup"><span data-stu-id="2c965-144">Select **OK** to schedule the batch job.</span></span>

<span data-ttu-id="2c965-145">Seuraavassa kuvassa on esimerkki Retail-sovelluksen erätyön määrityksestä.</span><span class="sxs-lookup"><span data-stu-id="2c965-145">The following illustration shows an example of batch job configuration in Retail.</span></span>

![Synkronoi tuoteluokitukset -erätyön määritys](media/rnr-hq-batchjob-recurrence.png)

## <a name="verify-that-the-batch-job-for-product-rating-synchronization-was-successful"></a><span data-ttu-id="2c965-147">Varmista, että tuoteluokituksen synkronoinnin erätyö onnistui</span><span class="sxs-lookup"><span data-stu-id="2c965-147">Verify that the batch job for product rating synchronization was successful</span></span>

<span data-ttu-id="2c965-148">Seuraavalla tavalla voit varmistaa, että **Synkronoi tuoteluokitukset** -erätyö onnistui.</span><span class="sxs-lookup"><span data-stu-id="2c965-148">To verify that the **Sync product ratings** batch job was successful, follow these steps.</span></span>

1. <span data-ttu-id="2c965-149">Siirry kohtaan **Retail \> Järjestelmänvalvoja \> Kyselyt \> Erätyöt** tai jos käytössä on Retail-sovelluksen varastointiyksikkö, siirry kohtaan **Retail \> Kyselyt ja raportit \> Erätyöt**.</span><span class="sxs-lookup"><span data-stu-id="2c965-149">Go to **Retail \> System administrator \> Inquiries \> Batch jobs** or, if you're using a Retail-only stock keeping unit (SKU), **Retail \> Inquiries and reports \> Batch jobs** instead.</span></span> <span data-ttu-id="2c965-150">Vaihtoehtoisesti voit tehdä haun erätyöt-sanalla.</span><span class="sxs-lookup"><span data-stu-id="2c965-150">Alternatively, search for "Batch jobs."</span></span>
1. <span data-ttu-id="2c965-151">Jos haluat tarkastella erätyön tietoja, hae erätyöluettelon **Työn kuvaus** -sarakkeessa kuvausta, jossa on maininta Nouda tuoteluokitukset.</span><span class="sxs-lookup"><span data-stu-id="2c965-151">To view the details of the batch job, in the batch job list, in the **Job description** column, search for a description that contains "Pull product ratings."</span></span>
1. <span data-ttu-id="2c965-152">Valitse työn tunnus, jos haluat tarkastella erätyön tietoja, kuten ajoituksen aloituspäivää ja aikaa ja toistuvaa tekstiä.</span><span class="sxs-lookup"><span data-stu-id="2c965-152">Select the job ID to view the batch job details, such as the scheduled start date/time and the recurrence text.</span></span>

<span data-ttu-id="2c965-153">Seuraavassa kuvassa on esimerkki erätyön tiedoista Retail-sovelluksessa, kun erätyö on ajoitettu suoritettavaksi kahden tunnin välein.</span><span class="sxs-lookup"><span data-stu-id="2c965-153">The following illustration shows an example of the batch job details in Retail when the batch job is scheduled to run at two-hour intervals.</span></span>

![Synkronoi tuoteluokitus -erätyön tiedot](media/rnr-hq-batchjob-status-checking.png)

## <a name="make-product-ratings-available-at-the-pos"></a><span data-ttu-id="2c965-155">Määritä tuoteluokitukset käytettäviksi myyntipisteessä</span><span class="sxs-lookup"><span data-stu-id="2c965-155">Make product ratings available at the POS</span></span>

<span data-ttu-id="2c965-156">Dynamics 365 Commercen luokitusten ja arvosteluiden ratkaisu on monikanavaratkaisu.</span><span class="sxs-lookup"><span data-stu-id="2c965-156">The ratings and reviews solution in Dynamics 365 Commerce is an omnichannel solution.</span></span> <span data-ttu-id="2c965-157">Tuotteiden luokitukset eivät kuitenkaan näy myyntipisteessä oletusarvoisesti.</span><span class="sxs-lookup"><span data-stu-id="2c965-157">However, products ratings aren't shown at the POS by default.</span></span> <span data-ttu-id="2c965-158">Jos haluat auttaa myymälöissä käyviä asiakkaita näkemään luokitukset ja arvostelut silloin, kun myyjät palvelevat heitä, ota tuoteluokitukset käyttöön myyntipisteessä.</span><span class="sxs-lookup"><span data-stu-id="2c965-158">To help customers in stores see ratings and reviews when they are being helped by sales associates, you must turn on product ratings at the POS.</span></span>

<span data-ttu-id="2c965-159">Voit ottaa tuoteluokitukset käyttöön myyntipisteessä seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="2c965-159">To turn on product ratings at the POS, follow these steps.</span></span>

1. <span data-ttu-id="2c965-160">Valitse **Vähittäismyynti \> Retail-asetukset \> Parametrit \> Retail-parametrit**.</span><span class="sxs-lookup"><span data-stu-id="2c965-160">Go to **Retail \> Retail setup \> Parameters \> Retail parameters**.</span></span> <span data-ttu-id="2c965-161">Vaihtoehtoisesti voit tehdä haun Retail-parametrit-sanoilla.</span><span class="sxs-lookup"><span data-stu-id="2c965-161">Alternatively, search for "Retail parameters."</span></span>
1. <span data-ttu-id="2c965-162">Valitse **Määrityksen parametrit** -välilehdessä **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="2c965-162">On the **Configuration parameters** tab, select **New**.</span></span>
1. <span data-ttu-id="2c965-163">Anna nimi, kuten **RatingsAndReviews.EnableProductRatingsForRetailStores**, ja määritä arvoksi **Tosi**.</span><span class="sxs-lookup"><span data-stu-id="2c965-163">Enter a name such as **RatingsAndReviews.EnableProductRatingsForRetailStores**, and set the value to **true**.</span></span>
1. <span data-ttu-id="2c965-164">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="2c965-164">Select **Save**.</span></span>
1. <span data-ttu-id="2c965-165">Siirry kohtaan **Vähittäismyynti \> Vähittäismyynnin IT \> Jakeluaikataulu**.</span><span class="sxs-lookup"><span data-stu-id="2c965-165">Go to **Retail \> Retail IT \> Distribution schedule**.</span></span> <span data-ttu-id="2c965-166">Vaihtoehtoisesti voit tehdä haun jakeluaikataulu-sanalla.</span><span class="sxs-lookup"><span data-stu-id="2c965-166">Alternatively, search for "Distribution schedule."</span></span>
1. <span data-ttu-id="2c965-167">Valitse työluettelosta **1110** (**Yleinen määritys**) ja valitse sitten **Suorita nyt**.</span><span class="sxs-lookup"><span data-stu-id="2c965-167">In the job list, select **1110** (**Global configuration**), and then select **Run now**.</span></span>
1. <span data-ttu-id="2c965-168">Kun työ on suoritettu, tarkista, että tuotteiden luokitukset näkyvät nyt myyntipisteessä.</span><span class="sxs-lookup"><span data-stu-id="2c965-168">After the job has successfully run, verify that products ratings are now shown at the POS.</span></span>

<span data-ttu-id="2c965-169">Seuraavassa kuvassa on esimerkki Retail-parametrien määrityksestä, joita käytetään myyntipisteen tuotteiden luokitusten käyttöönotossa.</span><span class="sxs-lookup"><span data-stu-id="2c965-169">The following illustration shows an example of the configuration of the Retail parameters to turn on product ratings at the POS.</span></span>

![Myyntipisteen tuoteluokitusten Retail-parametrien määritys](media/rnr-hq-enable-ratings-in-pos.png)

<span data-ttu-id="2c965-171">Seuraavassa kuvassa on esimerkki myyntipisteen tuoteluokituksista.</span><span class="sxs-lookup"><span data-stu-id="2c965-171">The following illustration shows an example of product ratings at the POS.</span></span>

![Myyntipisteen tuoteluokitukset](media/rnr-pos-catalog-ratings.png)

<span data-ttu-id="2c965-173">Seuraavassa kuvassa on esimerkki puhelinkeskuskanavien tuoteluokituksista.</span><span class="sxs-lookup"><span data-stu-id="2c965-173">The following illustration shows an example of product ratings in call center channels.</span></span>

![Puhelinkeskuskanavan tuoteluokitukset](media/rnr-call-center-ratings.png)

## <a name="additional-resources"></a><span data-ttu-id="2c965-175">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="2c965-175">Additional resources</span></span>

[<span data-ttu-id="2c965-176">Luokitukset ja arvostelut – yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="2c965-176">Ratings and reviews overview</span></span>](ratings-reviews-overview.md)

[<span data-ttu-id="2c965-177">Osallistu käyttääksesi luokituksia ja arvosteluja</span><span class="sxs-lookup"><span data-stu-id="2c965-177">Opt in to use ratings and reviews</span></span>](opt-in-ratings-reviews.md)

[<span data-ttu-id="2c965-178">Hallitse luokituksia ja arvosteluja</span><span class="sxs-lookup"><span data-stu-id="2c965-178">Manage ratings and reviews</span></span>](manage-reviews.md)

[<span data-ttu-id="2c965-179">Määritä luokitukset ja arvostelut</span><span class="sxs-lookup"><span data-stu-id="2c965-179">Configure ratings and reviews</span></span>](configure-ratings-reviews.md)
