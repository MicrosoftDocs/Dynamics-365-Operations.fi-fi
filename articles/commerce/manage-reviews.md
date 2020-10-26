---
title: Hallitse luokituksia ja arvosteluja
description: Tässä ohjeaiheessa käsitellään luokitusten ja arvostelujen hallintaa Microsoft Dynamics 365 Commerce -sivustonmuodostimessa.
author: gvrmohanreddy
manager: annbe
ms.date: 10/09/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Operations, Retail, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: gmohanv
ms.search.validFrom: 2019-10-01
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 3fc88bc5a5868dce7c0539bf3f0ddc5b751e7b75
ms.sourcegitcommit: 83ec80382bfeb693d5c5949b6f65296bd50eed12
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/09/2020
ms.locfileid: "3974003"
---
# <a name="manage-ratings-and-reviews"></a><span data-ttu-id="86dc8-103">Hallitse luokituksia ja arvosteluja</span><span class="sxs-lookup"><span data-stu-id="86dc8-103">Manage ratings and reviews</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="86dc8-104">Tässä ohjeaiheessa käsitellään luokitusten ja arvostelujen hallintaa Microsoft Dynamics 365 Commerce -sivustonmuodostimessa.</span><span class="sxs-lookup"><span data-stu-id="86dc8-104">This topic explains how to manage ratings and reviews in Microsoft Dynamics 365 Commerce site builder.</span></span>

## <a name="overview"></a><span data-ttu-id="86dc8-105">Yleiskuvaus</span><span class="sxs-lookup"><span data-stu-id="86dc8-105">Overview</span></span>

<span data-ttu-id="86dc8-106">Dynamics 365 Commerce käyttää Microsoft Azure Cognitive Service -palvelua arvostelun tekstin automaattisessa valvonnassa havaitsemalla sopimattomat sanat.</span><span class="sxs-lookup"><span data-stu-id="86dc8-106">Dynamics 365 Commerce uses Microsoft Azure Cognitive Service to automatically moderate review text by redacting profane words.</span></span> <span data-ttu-id="86dc8-107">Valvojat voivat toteuttaa myös seuraavat manuaaliset tehtävät Dynamics 365 Commerce -sivustonmuodostimessa.</span><span class="sxs-lookup"><span data-stu-id="86dc8-107">In addition, moderators can use Dynamics 365 Commerce site builder to implement the following manual tasks:</span></span>

- <span data-ttu-id="86dc8-108">Arvostelujen valvominen vastaamalla niihin tai poistamalla ne.</span><span class="sxs-lookup"><span data-stu-id="86dc8-108">Moderate reviews by responding to them or removing them.</span></span>
- <span data-ttu-id="86dc8-109">Asiakkaan arvostelujen poistaminen asiakkaan pyynnöstä.</span><span class="sxs-lookup"><span data-stu-id="86dc8-109">Delete a customer's reviews at the customer's request.</span></span>
- <span data-ttu-id="86dc8-110">Joukkotuonnin luokitusten ja arvostelujen tiedot kaikille tuotteille Microsoft Power BI -mallissa niin, että luokitusten ja arvostelujen trendit voidaan analysoida.</span><span class="sxs-lookup"><span data-stu-id="86dc8-110">Bulk-import ratings and reviews data for all products into a Microsoft Power BI template, so that trends for ratings and reviews can be analyzed.</span></span>

## <a name="read-a-review"></a><span data-ttu-id="86dc8-111">Arvostelun lukeminen</span><span class="sxs-lookup"><span data-stu-id="86dc8-111">Read a review</span></span> 

<span data-ttu-id="86dc8-112">Commerce-sivustonmuodostimessa voi lukea arvostelun seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="86dc8-112">To read to a review in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="86dc8-113">Siirry kohtaan **Aloitus \> Arvostelut \> Valvonta**.</span><span class="sxs-lookup"><span data-stu-id="86dc8-113">Go to **Home \> Reviews \> Moderation**.</span></span>
1. <span data-ttu-id="86dc8-114">Suodata tuotteen arvostelut tuotteen tunnuksen, tuotteen nimen tai arvostelun tekstin mukaan sivun oikeassa yläkulmassa olevan hakukentän avulla.</span><span class="sxs-lookup"><span data-stu-id="86dc8-114">Use the search field in the upper right of the page to filter the reviews that are shown by product ID, product name, or review text.</span></span>

<span data-ttu-id="86dc8-115">Lisäsuodattimien avulla voit rajoittaa arvosteluita kauden, arvioinnin, kanavan tai vaikutuksen tila (poistettu, vastattu tai raportoitu).</span><span class="sxs-lookup"><span data-stu-id="86dc8-115">Additional filters let you limit the reviews by period, rating, channel, or concern status (taken down, responded, or reported).</span></span>

![Valvonnan aloitussivu](media/rnr-moderation-home.png) 

## <a name="respond-to-a-review"></a><span data-ttu-id="86dc8-117">Arvosteluun vastaaminen</span><span class="sxs-lookup"><span data-stu-id="86dc8-117">Respond to a review</span></span> 

<span data-ttu-id="86dc8-118">Joskus tuotteen ostaneet asiakkaat ilmaisevat tyytyväisyyttä tai tyytymättömyyttä tai he eivät tiedä, miten tuotetta käytetään.</span><span class="sxs-lookup"><span data-stu-id="86dc8-118">Sometimes, customers who purchased a product express their satisfaction or dissatisfaction, or they don't understand how to use the product.</span></span> <span data-ttu-id="86dc8-119">Valvoja voi vastata arvosteluun.</span><span class="sxs-lookup"><span data-stu-id="86dc8-119">As a moderator, you can post a response to a review.</span></span> <span data-ttu-id="86dc8-120">Tämä vastaus näkyy yhdessä arvostelun kanssa sivustossa.</span><span class="sxs-lookup"><span data-stu-id="86dc8-120">This response appears together with the review on the site.</span></span> 

<span data-ttu-id="86dc8-121">Commerce-sivustonmuodostimessa voi vastata arvostelun seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="86dc8-121">To respond to a review in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="86dc8-122">Siirry kohtaan **Aloitus \> Arvostelut \> Valvonta**.</span><span class="sxs-lookup"><span data-stu-id="86dc8-122">Go to **Home \> Reviews \> Moderation**.</span></span>
1. <span data-ttu-id="86dc8-123">Etsi ja valitse arvostelu, johon haluat vastata.</span><span class="sxs-lookup"><span data-stu-id="86dc8-123">Find and select the review that requires a response.</span></span>
1. <span data-ttu-id="86dc8-124">Valitse oikeanpuoleisessa ominaisuusruudussa **Lisää vastaus**.</span><span class="sxs-lookup"><span data-stu-id="86dc8-124">In the properties pane on the right, select **Add a response**.</span></span>
1. <span data-ttu-id="86dc8-125">Kirjoita vastauksen teksti ja nimi, jonka haluat näkyvän vastaajan kohdalla.</span><span class="sxs-lookup"><span data-stu-id="86dc8-125">Enter the response text and the name that should be shown for the responder.</span></span> <span data-ttu-id="86dc8-126">Vastaajan oletusnimi on **valvoja**.</span><span class="sxs-lookup"><span data-stu-id="86dc8-126">The default responder name is **Moderator**.</span></span>
1. <span data-ttu-id="86dc8-127">Kun olet valmis, valitse **Kirjaa vastaus**.</span><span class="sxs-lookup"><span data-stu-id="86dc8-127">When you've finished, select **Post response**.</span></span>

![Arvosteluun vastaaminen](media/rnr-moderation-response.png) 

## <a name="take-down-a-review"></a><span data-ttu-id="86dc8-129">Arvostelun poistaminen</span><span class="sxs-lookup"><span data-stu-id="86dc8-129">Take down a review</span></span> 

<span data-ttu-id="86dc8-130">Joskus valvojien kannattaa poistaa asiakkaiden arvosteluita liiketoiminnallisista syistä.</span><span class="sxs-lookup"><span data-stu-id="86dc8-130">Sometimes, there is a business justification for moderators to take down customer reviews.</span></span> 

<span data-ttu-id="86dc8-131">Commerce-sivustonmuodostimessa voi poistaa arvostelun seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="86dc8-131">To take down a review in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="86dc8-132">Siirry kohtaan **Aloitus \> Arvostelut \> Valvonta**.</span><span class="sxs-lookup"><span data-stu-id="86dc8-132">Go to **Home \> Reviews \> Moderation**.</span></span>
1. <span data-ttu-id="86dc8-133">Etsi ja valitse arvostelu, jonka haluat poistaa.</span><span class="sxs-lookup"><span data-stu-id="86dc8-133">Find and select the review that must be taken down.</span></span>
1. <span data-ttu-id="86dc8-134">Valitse oikeassa ominaisuusruudussa poiston syy **Poista arvostelu** -kohdassa ja valitse sitten **Poista**.</span><span class="sxs-lookup"><span data-stu-id="86dc8-134">In the properties pane on the right, select a takedown reason under **Takedown Review**, and then select **Take down**.</span></span>
    
## <a name="delete-a-customers-reviews-at-the-customers-request"></a><span data-ttu-id="86dc8-135">Asiakkaan arvostelujen poistaminen asiakkaan pyynnöstä</span><span class="sxs-lookup"><span data-stu-id="86dc8-135">Delete a customer's reviews at the customer's request</span></span> 

<span data-ttu-id="86dc8-136">Joskus asiakkaat haluavat, että luokitukset ja arvostelut poistetaan pysyvästi sähköisen kaupankäynnin sivustosta.</span><span class="sxs-lookup"><span data-stu-id="86dc8-136">Sometimes, customers want their ratings and reviews data to be permanently deleted from an e-Commerce website.</span></span> <span data-ttu-id="86dc8-137">Valvoja, joka vastaanottaa poistopyynnön asiakkaalta, voi poistaa asiakkaan tiedot käyttämällä arvostelun poistotoimintoa.</span><span class="sxs-lookup"><span data-stu-id="86dc8-137">A moderator who receives a removal request from a customer can remove the customer's data by using the review deletion feature.</span></span> <span data-ttu-id="86dc8-138">Valvoja tarvitsee asiakkaan sen sähköpostiosoitteen, jota on käytetty sisäänkirjauksessa ja arvostelujen antamisessa, jotta hän voi etsiä ja poistaa asiakkaan tiedot.</span><span class="sxs-lookup"><span data-stu-id="86dc8-138">To find and delete a customer's data, the moderator requires the email address that the customer used to sign in and provide reviews.</span></span> 

<span data-ttu-id="86dc8-139">Commerce-sivustonmuodostimessa voi etsiä asiakkaan tietoja ja poistaa niitä seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="86dc8-139">To find and delete customer data in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="86dc8-140">Siirry kohtaan **Aloitus \> Arvostelut \> Poista**.</span><span class="sxs-lookup"><span data-stu-id="86dc8-140">Go to **Home \> Reviews \> Delete**.</span></span>
1. <span data-ttu-id="86dc8-141">Anna **Hae käyttäjiä sähköpostiosoitteen avulla** -ruutuun asiakkaan sähköpostiosoite ja valitse sitten **Hae**.</span><span class="sxs-lookup"><span data-stu-id="86dc8-141">In the **Search for users by email address** box, enter the customer's email address, and then select **Search**.</span></span>
1. <span data-ttu-id="86dc8-142">Jos asiakkaalla on arvosteluaktiviteetteja (esimerkiksi arvostelun lähetyksiä, äänestyksiä toisen asiakkaan arvosteluista tai kommentteja toisen asiakkaan arvostelusta), näkyvissä on tuloksia.</span><span class="sxs-lookup"><span data-stu-id="86dc8-142">If the customer has any review activity (for example, review submissions, votes about the helpfulness of another customer's reviews, or comments about another customer's review), the results are shown.</span></span> <span data-ttu-id="86dc8-143">Jokaisen nimikkeen kohdalla on **Poista**-painike.</span><span class="sxs-lookup"><span data-stu-id="86dc8-143">For each item, there is a **Delete** button.</span></span>
1. <span data-ttu-id="86dc8-144">Valitse jokaisen poistettavan nimikkeen kohdalla **Poista**.</span><span class="sxs-lookup"><span data-stu-id="86dc8-144">For each item that must be deleted, select **Delete**.</span></span> <span data-ttu-id="86dc8-145">Kun sinulta kysytään vahvistusta, valitse **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="86dc8-145">When you're prompted for confirmation, select **Yes**.</span></span> 
    
![Asiakkaan tietojen poistaminen](media/rnr-moderation-delete-reviews.png) 

> [!NOTE]
> - <span data-ttu-id="86dc8-147">Tietojen poistaminen kokonaan järjestelmästä voi kestää jopa seitsemän päivää.</span><span class="sxs-lookup"><span data-stu-id="86dc8-147">It can take up to seven days for data to be completely removed from the system.</span></span> <span data-ttu-id="86dc8-148">Valvojien tulee ilmoittaa asiakkaille tästä viivästyksestä.</span><span class="sxs-lookup"><span data-stu-id="86dc8-148">Moderators should notify customers about this delay.</span></span>
> - <span data-ttu-id="86dc8-149">Jos asiakkaat ovat muuttaneet nimensä tilin asetuksissa, hakutuloksissa saattaa näkyä useita nimikkeitä.</span><span class="sxs-lookup"><span data-stu-id="86dc8-149">If customers have changed their name in their account settings, multiple items might appear in the search results.</span></span> <span data-ttu-id="86dc8-150">Tässä tapauksessa asiakkaan tietojen poistaminen kokonaan edellyttää, että valvoja valitsee **Poista**-kohdan kaikille nimikkeille.</span><span class="sxs-lookup"><span data-stu-id="86dc8-150">In this case, to completely delete the customer's data, the moderator must select **Delete** for each item.</span></span> 

## <a name="download-ratings-and-reviews-data"></a><span data-ttu-id="86dc8-151">Luokitusten ja arvostelujen tietojen lataaminen</span><span class="sxs-lookup"><span data-stu-id="86dc8-151">Download ratings and reviews data</span></span>

<span data-ttu-id="86dc8-152">Commerce-sivustonmuodostimessa avulla valvojat voivat tuoda luokitusten ja arvostelujen tiedot joukkona ja analysoida trendejä.</span><span class="sxs-lookup"><span data-stu-id="86dc8-152">Commerce site builder lets moderators import ratings and reviews data in bulk, so that they can analyze trends.</span></span> <span data-ttu-id="86dc8-153">Perusmittarit sisältävä Power BI -malli on käytettävissä.</span><span class="sxs-lookup"><span data-stu-id="86dc8-153">A Power BI template that includes basic metrics is available.</span></span> <span data-ttu-id="86dc8-154">Tämän mallin avulla valvojat voivat yhdistää joukkona tuodut tiedot ja tarkastella koontinäyttöä.</span><span class="sxs-lookup"><span data-stu-id="86dc8-154">Moderators can use this template to connect bulk-imported data and view a dashboard.</span></span> <span data-ttu-id="86dc8-155">Heidän ei tarvitse luoda mukautettua koontinäyttöä.</span><span class="sxs-lookup"><span data-stu-id="86dc8-155">They don't have to create a custom dashboard.</span></span> <span data-ttu-id="86dc8-156">Valvojat voivat myös mukauttaa Power BI -mallin vastaamaan erityistarpeita.</span><span class="sxs-lookup"><span data-stu-id="86dc8-156">Moderators can also customize the Power BI template to meet their specific needs.</span></span> 

<span data-ttu-id="86dc8-157">Commerce-sivustonmuodostimessa voi ladata luokituksia ja arvosteluja seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="86dc8-157">To download ratings and reviews data in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="86dc8-158">Siirry kohtaan **Aloitus \> Arvostelut \> Raportointi**.</span><span class="sxs-lookup"><span data-stu-id="86dc8-158">Go to **Home \> Reviews \> Reporting**.</span></span>
1. <span data-ttu-id="86dc8-159">Valitse **Lataa arvostelun tiedot**, jos haluat ladata luokitusten ja arvostelujen tiedot joukkona CSV-muodossa.</span><span class="sxs-lookup"><span data-stu-id="86dc8-159">Select **Download review data** to download ratings and reviews data in bulk in comma-separated values (CSV) format.</span></span>

## <a name="view-ratings-and-reviews-trends"></a><span data-ttu-id="86dc8-160">Luokitusten ja arvostelujen trendien tarkasteleminen</span><span class="sxs-lookup"><span data-stu-id="86dc8-160">View ratings and reviews trends</span></span>

<span data-ttu-id="86dc8-161">Valvojat voivat ladata Power BI -mallin niin, että he voivat tarkastella trendejä koontinäytössä.</span><span class="sxs-lookup"><span data-stu-id="86dc8-161">Moderators can download the Power BI template so that they can view trends in a dashboard.</span></span>

<span data-ttu-id="86dc8-162">Commerce-sivustonmuodostimessa voi tarkastella luokitus- ja arvostelutrendejä seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="86dc8-162">To view ratings and reviews trends in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="86dc8-163">Siirry kohtaan **Aloitus \> Arvostelut \> Raportointi**.</span><span class="sxs-lookup"><span data-stu-id="86dc8-163">Go to **Home \> Reviews \> Reporting**.</span></span>
1. <span data-ttu-id="86dc8-164">Lataa malli valitsemalla **PowerBI-malli**.</span><span class="sxs-lookup"><span data-stu-id="86dc8-164">Select **PowerBI template** to download the template.</span></span>

    ![Power BI -mallin lataaminen](media/rnr-moderation-reports.png) 

1. <span data-ttu-id="86dc8-166">Avaa ladattu malli käyttämällä Power BI -sovellusta.</span><span class="sxs-lookup"><span data-stu-id="86dc8-166">Open the downloaded template by using the Power BI app.</span></span> <span data-ttu-id="86dc8-167">Sulje näyttöön avautuva **Verkkosisällön käyttöoikeus** -valintaikkuna ja sulje sitten näyttöön tuleva Päivitys-virhesanoma.</span><span class="sxs-lookup"><span data-stu-id="86dc8-167">Close the **Access to web content** dialog box that appears, and then close the "Refresh" error message that appears.</span></span>
1. <span data-ttu-id="86dc8-168">Siirry kohtaan **Aloitus**, valitse **Muokkaa kyselyitä** ja valitse sitten **Tietolähteen asetukset**.</span><span class="sxs-lookup"><span data-stu-id="86dc8-168">Go to **Home**, select **Edit queries**, and then select **Data source settings**.</span></span>
1. <span data-ttu-id="86dc8-169">Valitse **Tietolähteen asetukset** -valintaikkunassa **Muuta lähdettä**.</span><span class="sxs-lookup"><span data-stu-id="86dc8-169">In the **Data source settings** dialog box, select **Change Source**.</span></span>
1. <span data-ttu-id="86dc8-170">Syötä **URL-osoite**-kenttään edellisessä proseduurissa ladattujen arvostelujen tietojen polku (esimerkiksi **c:\\reviews\\ReviewsData.csv**).</span><span class="sxs-lookup"><span data-stu-id="86dc8-170">In the **URL** field, enter the path of the reviews data that you downloaded in the previous procedure (for example, **c:\\reviews\\ReviewsData.csv**).</span></span>

    ![URL-osoite-kenttä CSV-valintaikkunassa](media/rnr-powerbi-datasource-settings.png) 

1. <span data-ttu-id="86dc8-172">Valitse **OK** ja valitse sitten **Käytä muutoksia**.</span><span class="sxs-lookup"><span data-stu-id="86dc8-172">Select **OK**, and then select **Apply changes**.</span></span> <span data-ttu-id="86dc8-173">Muutokset otetaan käyttöön tietolähteessä muutaman minuutin kuluessa.</span><span class="sxs-lookup"><span data-stu-id="86dc8-173">It will take one to two minutes to apply your changes to the data source.</span></span>
1. <span data-ttu-id="86dc8-174">Valitse **Trendien taulukko**, jos haluat tarkastella luokitusten ja arvostelujen trendejä.</span><span class="sxs-lookup"><span data-stu-id="86dc8-174">Select **Trends sheet** to view ratings and reviews trends.</span></span>

    ![Luokitusten ja arvostelujen trendit](media/rnr-powerbi-dashboard-template.png) 
    
## <a name="additional-resources"></a><span data-ttu-id="86dc8-176">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="86dc8-176">Additional resources</span></span>

[<span data-ttu-id="86dc8-177">Luokitukset ja arvostelut – yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="86dc8-177">Ratings and reviews overview</span></span>](ratings-reviews-overview.md)

[<span data-ttu-id="86dc8-178">Osallistu käyttääksesi luokituksia ja arvosteluja</span><span class="sxs-lookup"><span data-stu-id="86dc8-178">Opt in to use ratings and reviews</span></span>](opt-in-ratings-reviews.md)

[<span data-ttu-id="86dc8-179">Määritä luokitukset ja arvostelut</span><span class="sxs-lookup"><span data-stu-id="86dc8-179">Configure ratings and reviews</span></span>](configure-ratings-reviews.md)

[<span data-ttu-id="86dc8-180">Tuoteluokitusten synkronoiminen Dynamics 365 Retailissa</span><span class="sxs-lookup"><span data-stu-id="86dc8-180">Sync product ratings in Dynamics 365 Retail</span></span>](sync-product-ratings.md)
