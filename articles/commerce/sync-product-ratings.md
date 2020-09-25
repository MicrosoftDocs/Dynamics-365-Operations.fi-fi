---
title: Synkronoi tuoteluokitukset Dynamics 365 Commerceissa
description: Tässä ohjeaiheessa kerrotaan, miten tuoteluokitukset synkronoidaan Microsoft Dynamics 365 Commerce -sovelluksessa.
author: gvrmohanreddy
manager: annbe
ms.date: 02/06/2020
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
ms.openlocfilehash: dec87b548f3a218e1f833b752305f373e893b14c
ms.sourcegitcommit: 58d7133ae9909fa205730e3cf4c7fd5a1d5d0b75
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/10/2020
ms.locfileid: "3793584"
---
# <a name="sync-product-ratings-in-dynamics-365-commerce"></a><span data-ttu-id="4500c-103">Synkronoi tuoteluokitukset Dynamics 365 Commerceissa</span><span class="sxs-lookup"><span data-stu-id="4500c-103">Sync product ratings in Dynamics 365 Commerce</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="4500c-104">Tässä ohjeaiheessa kerrotaan, miten tuoteluokitukset synkronoidaan Microsoft Dynamics 365 Commerce -sovelluksessa.</span><span class="sxs-lookup"><span data-stu-id="4500c-104">This topic describes how to sync product ratings in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="4500c-105">Yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="4500c-105">Overview</span></span>

<span data-ttu-id="4500c-106">Jotta monikanavien, kuten myyntipisteen ja puhelinkeskusten, tuoteluokituksia voidaan käyttää, luokitusten ja arvostelujen palvelun tuotteiden luokitukset on tuotava Commerce-sovelluksen kanavatietokantaan.</span><span class="sxs-lookup"><span data-stu-id="4500c-106">To consume product ratings in omnichannels, such as at the point of sale (POS) and in call centers, product ratings from the ratings and reviews service must be imported into the Commerce channel database.</span></span> <span data-ttu-id="4500c-107">Kun tuoteluokitukset ovat käytettävissä monikanavissa, ne auttavat asiakkaita epäsuorasti myyjien kanssa tehtävässä vuorovaikutuksessa.</span><span class="sxs-lookup"><span data-stu-id="4500c-107">When product ratings are made available in omnichannels, they can help customers indirectly during their interactions with sales associates.</span></span>

<span data-ttu-id="4500c-108">Tässä ohjeaiheessa esitellään seuraavat tehtävät:</span><span class="sxs-lookup"><span data-stu-id="4500c-108">This topic describes following tasks:</span></span>

1. <span data-ttu-id="4500c-109">**Tuoteluokitusten synkronointityön** määrittäminen erätyönä tuoteluokitusten synkronoimiseksi **Luokitus- ja arvostelupalvelussa**.</span><span class="sxs-lookup"><span data-stu-id="4500c-109">Configure **Product ratings sync job** as a batch job to synchronize product ratings from the **Ratings and Reviews service**.</span></span>
1. <span data-ttu-id="4500c-110">Tarkista, että tuoteluokituksen synkronoinnin erätyö onnistui.</span><span class="sxs-lookup"><span data-stu-id="4500c-110">Verify that the batch job for product rating synchronization was successful.</span></span>
1. <span data-ttu-id="4500c-111">Määritä tuoteluokitukset käytettäviksi myyntipisteessä.</span><span class="sxs-lookup"><span data-stu-id="4500c-111">Make product ratings available at the POS.</span></span>

## <a name="configure-a-batch-job-to-synchronize-product-ratings"></a><span data-ttu-id="4500c-112">Määritä erätyö ja synkronoi tuoteluokitukset</span><span class="sxs-lookup"><span data-stu-id="4500c-112">Configure a batch job to synchronize product ratings</span></span>

> [!IMPORTANT]
> <span data-ttu-id="4500c-113">Varmista ennen aloittamista, että asennettuna on Dynamics 365 Commerce -versio 10.0.6 tai uudempi versio.</span><span class="sxs-lookup"><span data-stu-id="4500c-113">Before you start, make sure that version 10.0.6 or later of Dynamics 365 Commerce is installed.</span></span>

### <a name="initialize-the-commerce-scheduler"></a><span data-ttu-id="4500c-114">Commerce-ajastuksen alustaminen</span><span class="sxs-lookup"><span data-stu-id="4500c-114">Initialize the commerce scheduler</span></span>

<span data-ttu-id="4500c-115">Alusta Commerce-ajastus noudattamalla seuraavia vaiheita:</span><span class="sxs-lookup"><span data-stu-id="4500c-115">To initialize the commerce scheduler, follow these steps.</span></span>

1. <span data-ttu-id="4500c-116">Siirry kohtaan **Retail ja Commerce \> Headquarters-asetukset \> Commerce-ajastus \> Alusta Commerce-ajastus**.</span><span class="sxs-lookup"><span data-stu-id="4500c-116">Go to **Retail and Commerce \> Headquarters setup \> Commerce scheduler \> Initialize commerce scheduler**.</span></span> <span data-ttu-id="4500c-117">Vaihtoehtoisesti voit tehdä haun käyttämällä Alusta Commerce-ajoitus -lausetta.</span><span class="sxs-lookup"><span data-stu-id="4500c-117">Alternatively, search for "Initialize commerce scheduler."</span></span>
1. <span data-ttu-id="4500c-118">Varmista **Alusta Commerce-ajastus** -valintaikkunassa, että **Poista olemassa oleva määritys** -vaihtoehdon arvoksi on määritetty **Ei**. Valitse sitten **OK**.</span><span class="sxs-lookup"><span data-stu-id="4500c-118">In the **Initialize commerce scheduler** dialog box, make sure that the **Delete existing configuration** option is set to **No**, and then select **OK**.</span></span>

### <a name="verify-the-retailproductrating-subjob"></a><span data-ttu-id="4500c-119">RetailProductRating-alityön tarkistaminen</span><span class="sxs-lookup"><span data-stu-id="4500c-119">Verify the RetailProductRating subjob</span></span>

<span data-ttu-id="4500c-120">Seuraavalla tavalla voit tarkistaa, että **RetailProductRating**-alityö on olemassa.</span><span class="sxs-lookup"><span data-stu-id="4500c-120">To verify that the **RetailProductRating** subjob exists, follow these steps.</span></span>

1. <span data-ttu-id="4500c-121">Siirry kohtaan **Retail ja Commerce \> Headquarters-asetukset \> Commerce-ajastus \> Aikataulun alatyöt**.</span><span class="sxs-lookup"><span data-stu-id="4500c-121">Go to **Retail and Commerce \> Headquarters setup \> Commerce scheduler \> Scheduler subjobs**.</span></span> <span data-ttu-id="4500c-122">Vaihtoehtoisesti voit tehdä haun käyttämällä Ajastuksen alityöt -lausetta.</span><span class="sxs-lookup"><span data-stu-id="4500c-122">Alternatively, search for "Scheduler subjobs."</span></span>
1. <span data-ttu-id="4500c-123">Etsi alityöluettelosta **RetailProductRating**-alityö tai hae sitä.</span><span class="sxs-lookup"><span data-stu-id="4500c-123">In the subjob list, find or search for the **RetailProductRating** subjob.</span></span>

<span data-ttu-id="4500c-124">Seuraavassa kuvassa on esimerkki Commerce-sovelluksen alityön tiedoista.</span><span class="sxs-lookup"><span data-stu-id="4500c-124">The following illustration shows an example of the subjob details in Commerce.</span></span>

![RetailProductRating-alityön tiedot](media/rnr-hq-ratings-sub-job.png)

> [!NOTE]
> <span data-ttu-id="4500c-126">Jos et löydä **RetailProductRating**-alityötä, **Synkronoi tuoteluokitukset** -työ on jo ehkä suoritettu ja **1040 CDX**-työ on jo ehkä suoritettu ennen Commerce-ajastuksen alustusta.</span><span class="sxs-lookup"><span data-stu-id="4500c-126">If you don't find the **RetailProductRating** subjob, you might already have run the **Sync product ratings** job and the **1040 CDX** job before you initialized the Commerce scheduler.</span></span> <span data-ttu-id="4500c-127">Tässä tapauksessa suorita **Tietojen täydellinen synkronointi** -työ seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="4500c-127">In this case, follow these steps to run the **Full data sync** job.</span></span>

> 1. <span data-ttu-id="4500c-128">Siirry kohtaan **Retail ja Commerce \> Headquarters-asetukset \> Commerce-ajastus \> Kanavatietokanta**.</span><span class="sxs-lookup"><span data-stu-id="4500c-128">Go to **Retail and Commerce \> Headquarters setup \> Commerce scheduler \> Channel database**.</span></span> <span data-ttu-id="4500c-129">Vaihtoehtoisesti voit tehdä haun käyttämällä kanavatietokanta-sanaa.</span><span class="sxs-lookup"><span data-stu-id="4500c-129">Alternatively, search for "Channel database."</span></span>
> 1. <span data-ttu-id="4500c-130">Valitse synkronoitava kanavatietokanta.</span><span class="sxs-lookup"><span data-stu-id="4500c-130">Select the channel database to sync.</span></span>
> 1. <span data-ttu-id="4500c-131">Valitse toimintoruudusta **Tietojen täydellinen synkronointi**.</span><span class="sxs-lookup"><span data-stu-id="4500c-131">On the action pane, select **Full data sync**.</span></span>
> 1. <span data-ttu-id="4500c-132">Valitse avattavasta **Valitse jakeluaikataulu** -luettelosta **1040 - tuotteet** ja valitse sitten **OK**.</span><span class="sxs-lookup"><span data-stu-id="4500c-132">In the **Select a distribution schedule** drop-down dialog box, select **1040 - products**, and then select **OK**.</span></span>
> 1. <span data-ttu-id="4500c-133">Toista edellisen proseduurin vaiheet ja varmista, että **RetailProductRating**-alityö on luotu.</span><span class="sxs-lookup"><span data-stu-id="4500c-133">Repeat the steps of the previous procedure to verify that the **RetailProductRating** subjob has been created.</span></span>

### <a name="import-product-ratings"></a><span data-ttu-id="4500c-134">Tuoteluokitusten tuominen</span><span class="sxs-lookup"><span data-stu-id="4500c-134">Import product ratings</span></span>

<span data-ttu-id="4500c-135">Voit tuoda tuoteluokitukset Commerce-sovelluksiin luokitusten ja arvostelujen palvelusta seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="4500c-135">To import product ratings into Commerce from the ratings and reviews service, follow these steps.</span></span>

1. <span data-ttu-id="4500c-136">Siirry kohtaan **Retail ja Commerce \> Headquarters-asetus \> Commerce-ajastus \> Synkronoi tuoteluokitukset -työ**.</span><span class="sxs-lookup"><span data-stu-id="4500c-136">Go to **Retail and Commerce \> Headquarters setup \> Commerce scheduler \> Sync product ratings job**.</span></span> <span data-ttu-id="4500c-137">Vaihtoehtoisesti voit tehdä haun käyttämällä Synkronoi tuoteluokitukset -työ -lausetta.</span><span class="sxs-lookup"><span data-stu-id="4500c-137">Alternatively, search for "Sync product ratings job."</span></span>
1. <span data-ttu-id="4500c-138">Valitse **Nouda tuoteluokitukset** -valintaikkunan **Suorita taustalla** -pikavälilehdessä **Toistuminen**.</span><span class="sxs-lookup"><span data-stu-id="4500c-138">In the **Pull product ratings** dialog box, on the **Run in the background** FastTab, select **Recurrence**.</span></span>
1. <span data-ttu-id="4500c-139">Määritä **Määritä toistuminen** -valintaikkunassa toistumisen malli.</span><span class="sxs-lookup"><span data-stu-id="4500c-139">In the **Define recurrence** dialog box, set up a recurrence pattern.</span></span> <span data-ttu-id="4500c-140">(Ehdotettu arvo on kaksi tuntia.) Älä ajoita toistumista, joka on pienempi kuin yksi tunti.</span><span class="sxs-lookup"><span data-stu-id="4500c-140">(The suggested value is two hours.) Don't schedule a recurrence that is less than one hour.</span></span>
1. <span data-ttu-id="4500c-141">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="4500c-141">Select **OK**.</span></span>
1. <span data-ttu-id="4500c-142">Määritä **Eräkäsittely**-vaihtoehdon arvoksi **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="4500c-142">Set the **Batch process** option to **Yes**.</span></span> <span data-ttu-id="4500c-143">Tämän asetuksen avulla voidaan varmistaa, että lokeja voi valvoa ja että erätyön suorituksen tilan voi tarkistaa.</span><span class="sxs-lookup"><span data-stu-id="4500c-143">This setting helps guarantee that you will be able to audit the logs and verify the status of batch job runs.</span></span>
1. <span data-ttu-id="4500c-144">Ajoita erätyö valitsemalla **OK**.</span><span class="sxs-lookup"><span data-stu-id="4500c-144">Select **OK** to schedule the batch job.</span></span>

<span data-ttu-id="4500c-145">Seuraavassa kuvassa on esimerkki Commerce-sovelluksen erätyön määrityksestä.</span><span class="sxs-lookup"><span data-stu-id="4500c-145">The following illustration shows an example of batch job configuration in Commerce.</span></span>

![Synkronoi tuoteluokitukset -erätyön määritys](media/rnr-hq-batchjob-recurrence.png)

## <a name="verify-that-the-batch-job-for-product-rating-synchronization-was-successful"></a><span data-ttu-id="4500c-147">Varmista, että tuoteluokituksen synkronoinnin erätyö onnistui</span><span class="sxs-lookup"><span data-stu-id="4500c-147">Verify that the batch job for product rating synchronization was successful</span></span>

<span data-ttu-id="4500c-148">Seuraavalla tavalla voit varmistaa, että **Synkronoi tuoteluokitukset** -erätyö onnistui.</span><span class="sxs-lookup"><span data-stu-id="4500c-148">To verify that the **Sync product ratings** batch job was successful, follow these steps.</span></span>

1. <span data-ttu-id="4500c-149">Siirry kohtaan **Retail ja Commerce \> Järjestelmänvalvoja \> Kyselyt \> Erätyöt** tai jos käytössä on Commerce-sovelluksen varastointiyksikkö, siirry kohtaan **Retail ja Commerce \> Kyselyt ja raportit \> Erätyöt**.</span><span class="sxs-lookup"><span data-stu-id="4500c-149">Go to **Retail and Commerce \> System administrator \> Inquiries \> Batch jobs** or, if you're using a Commerce-only stock keeping unit (SKU), **Retail and Commerce \> Inquiries and reports \> Batch jobs** instead.</span></span> <span data-ttu-id="4500c-150">Vaihtoehtoisesti voit tehdä haun erätyöt-sanalla.</span><span class="sxs-lookup"><span data-stu-id="4500c-150">Alternatively, search for "Batch jobs."</span></span>
1. <span data-ttu-id="4500c-151">Jos haluat tarkastella erätyön tietoja, hae erätyöluettelon **Työn kuvaus** -sarakkeessa kuvausta, jossa on maininta Nouda tuoteluokitukset.</span><span class="sxs-lookup"><span data-stu-id="4500c-151">To view the details of the batch job, in the batch job list, in the **Job description** column, search for a description that contains "Pull product ratings."</span></span>
1. <span data-ttu-id="4500c-152">Valitse työn tunnus, jos haluat tarkastella erätyön tietoja, kuten ajoituksen aloituspäivää ja aikaa ja toistuvaa tekstiä.</span><span class="sxs-lookup"><span data-stu-id="4500c-152">Select the job ID to view the batch job details, such as the scheduled start date/time and the recurrence text.</span></span>

<span data-ttu-id="4500c-153">Seuraavassa kuvassa on esimerkki erätyön tiedoista Commerce-sovelluksessa, kun erätyö on ajoitettu suoritettavaksi kahden tunnin välein.</span><span class="sxs-lookup"><span data-stu-id="4500c-153">The following illustration shows an example of the batch job details in Commerce when the batch job is scheduled to run at two-hour intervals.</span></span>

![Synkronoi tuoteluokitus -erätyön tiedot](media/rnr-hq-batchjob-status-checking.png)

## <a name="make-product-ratings-available-at-the-pos"></a><span data-ttu-id="4500c-155">Määritä tuoteluokitukset käytettäviksi myyntipisteessä</span><span class="sxs-lookup"><span data-stu-id="4500c-155">Make product ratings available at the POS</span></span>

<span data-ttu-id="4500c-156">Dynamics 365 Commercen luokitusten ja arvosteluiden ratkaisu on monikanavaratkaisu.</span><span class="sxs-lookup"><span data-stu-id="4500c-156">The ratings and reviews solution in Dynamics 365 Commerce is an omnichannel solution.</span></span> <span data-ttu-id="4500c-157">Tuotteiden luokitukset eivät kuitenkaan näy myyntipisteessä oletusarvoisesti.</span><span class="sxs-lookup"><span data-stu-id="4500c-157">However, products ratings aren't shown at the POS by default.</span></span> <span data-ttu-id="4500c-158">Jos haluat auttaa myymälöissä käyviä asiakkaita näkemään luokitukset ja arvostelut silloin, kun myyjät palvelevat heitä, ota tuoteluokitukset käyttöön myyntipisteessä.</span><span class="sxs-lookup"><span data-stu-id="4500c-158">To help customers in stores see ratings and reviews when they are being helped by sales associates, you must turn on product ratings at the POS.</span></span>

<span data-ttu-id="4500c-159">Voit ottaa tuoteluokitukset käyttöön myyntipisteessä seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="4500c-159">To turn on product ratings at the POS, follow these steps.</span></span>

1. <span data-ttu-id="4500c-160">Valitse **Retail ja Commerce \> Pääkonttorin asetukset \> Parametrit \> Commerce-parametrit**.</span><span class="sxs-lookup"><span data-stu-id="4500c-160">Go to **Retail and Commerce \> Commerce setup \> Parameters \> Commerce parameters**.</span></span> <span data-ttu-id="4500c-161">Vaihtoehtoisesti voit tehdä haun Commerce-parametrit-sanoilla.</span><span class="sxs-lookup"><span data-stu-id="4500c-161">Alternatively, search for "Commerce parameters."</span></span>
1. <span data-ttu-id="4500c-162">Valitse **Määrityksen parametrit** -välilehdessä **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="4500c-162">On the **Configuration parameters** tab, select **New**.</span></span>
1. <span data-ttu-id="4500c-163">Anna nimi, kuten **RatingsAndReviews.EnableProductRatingsForRetailStores**, ja määritä arvoksi **Tosi**.</span><span class="sxs-lookup"><span data-stu-id="4500c-163">Enter a name such as **RatingsAndReviews.EnableProductRatingsForRetailStores**, and set the value to **true**.</span></span>
1. <span data-ttu-id="4500c-164">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="4500c-164">Select **Save**.</span></span>
1. <span data-ttu-id="4500c-165">Mene kohtaan **Retail ja Commerce \> Retail ja Commerce IT \> Jakeluaikataulu**.</span><span class="sxs-lookup"><span data-stu-id="4500c-165">Go to **Retail and Commerce \> Retail and Commerce IT \> Distribution schedule**.</span></span> <span data-ttu-id="4500c-166">Vaihtoehtoisesti voit tehdä haun jakeluaikataulu-sanalla.</span><span class="sxs-lookup"><span data-stu-id="4500c-166">Alternatively, search for "Distribution schedule."</span></span>
1. <span data-ttu-id="4500c-167">Valitse työluettelosta **1110** (**Yleinen määritys**) ja valitse sitten **Suorita nyt**.</span><span class="sxs-lookup"><span data-stu-id="4500c-167">In the job list, select **1110** (**Global configuration**), and then select **Run now**.</span></span>
1. <span data-ttu-id="4500c-168">Kun työ on suoritettu, tarkista, että tuotteiden luokitukset näkyvät nyt myyntipisteessä.</span><span class="sxs-lookup"><span data-stu-id="4500c-168">After the job has successfully run, verify that products ratings are now shown at the POS.</span></span>

<span data-ttu-id="4500c-169">Seuraavassa kuvassa on esimerkki Commerce-parametrien määrityksestä, joita käytetään myyntipisteen tuotteiden luokitusten käyttöönotossa.</span><span class="sxs-lookup"><span data-stu-id="4500c-169">The following illustration shows an example of the configuration of the Commerce parameters to turn on product ratings at the POS.</span></span>

![Myyntipisteen tuoteluokitusten Commerce-parametrien määritys](media/rnr-hq-enable-ratings-in-pos.png)

<span data-ttu-id="4500c-171">Seuraavassa kuvassa on esimerkki myyntipisteen tuoteluokituksista.</span><span class="sxs-lookup"><span data-stu-id="4500c-171">The following illustration shows an example of product ratings at the POS.</span></span>

![Myyntipisteen tuoteluokitukset](media/rnr-pos-catalog-ratings.png)

<span data-ttu-id="4500c-173">Seuraavassa kuvassa on esimerkki puhelinkeskuskanavien tuoteluokituksista.</span><span class="sxs-lookup"><span data-stu-id="4500c-173">The following illustration shows an example of product ratings in call center channels.</span></span>

![Puhelinkeskuskanavan tuoteluokitukset](media/rnr-call-center-ratings.png)

## <a name="additional-resources"></a><span data-ttu-id="4500c-175">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="4500c-175">Additional resources</span></span>

[<span data-ttu-id="4500c-176">Luokitukset ja arvostelut – yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="4500c-176">Ratings and reviews overview</span></span>](ratings-reviews-overview.md)

[<span data-ttu-id="4500c-177">Osallistu käyttääksesi luokituksia ja arvosteluja</span><span class="sxs-lookup"><span data-stu-id="4500c-177">Opt in to use ratings and reviews</span></span>](opt-in-ratings-reviews.md)

[<span data-ttu-id="4500c-178">Hallitse luokituksia ja arvosteluja</span><span class="sxs-lookup"><span data-stu-id="4500c-178">Manage ratings and reviews</span></span>](manage-reviews.md)

[<span data-ttu-id="4500c-179">Määritä luokitukset ja arvostelut</span><span class="sxs-lookup"><span data-stu-id="4500c-179">Configure ratings and reviews</span></span>](configure-ratings-reviews.md)
