---
title: Hallitse luokituksia ja arvosteluja
description: Tässä ohjeaiheessa kerrotaan, miten luokituksia ja arvosteluita hallitaan Microsoft Dynamics 365 Commercen luokitusten ja arvostelujen valvontatyökalun avulla.
author: gvrmohanreddy
manager: annbe
ms.date: 01/30/2020
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
ms.openlocfilehash: a7fa2ae3124a0a68b3890987c5dce2730e5c2183
ms.sourcegitcommit: 1e6c8163da5818196769eb278afb3a2335d0cbe3
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/05/2020
ms.locfileid: "3027239"
---
# <a name="manage-ratings-and-reviews"></a><span data-ttu-id="96d7d-103">Hallitse luokituksia ja arvosteluja</span><span class="sxs-lookup"><span data-stu-id="96d7d-103">Manage ratings and reviews</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="96d7d-104">Tässä ohjeaiheessa kerrotaan, miten luokituksia ja arvosteluita hallitaan Microsoft Dynamics 365 Commercen luokitusten ja arvostelujen valvontatyökalun avulla.</span><span class="sxs-lookup"><span data-stu-id="96d7d-104">This topic explains how to manage ratings and reviews by using the Microsoft Dynamics 365 Commerce ratings and reviews moderation tool.</span></span>

## <a name="overview"></a><span data-ttu-id="96d7d-105">Yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="96d7d-105">Overview</span></span>

<span data-ttu-id="96d7d-106">Dynamics 365 Commerce käyttää Microsoft Azure Cognitive Service -palvelua arvostelun tekstin automaattisessa valvonnassa havaitsemalla sopimattomat sanat.</span><span class="sxs-lookup"><span data-stu-id="96d7d-106">Dynamics 365 Commerce uses Microsoft Azure Cognitive Service to automatically moderate review text by redacting profane words.</span></span> <span data-ttu-id="96d7d-107">Lisäksi valvojat voivat käyttää luokitusten ja arvostelujen valvontatyökalua seuraavissa manuaalisissa tehtävissä:</span><span class="sxs-lookup"><span data-stu-id="96d7d-107">In addition, moderators can use the ratings and reviews moderation tool for the following manual tasks:</span></span>

- <span data-ttu-id="96d7d-108">Arvostelujen valvominen vastaamalla niihin tai poistamalla ne.</span><span class="sxs-lookup"><span data-stu-id="96d7d-108">Moderate reviews by responding to them or removing them.</span></span>
- <span data-ttu-id="96d7d-109">Asiakkaan arvostelujen poistaminen asiakkaan pyynnöstä.</span><span class="sxs-lookup"><span data-stu-id="96d7d-109">Delete a customer's reviews at the customer's request.</span></span>
- <span data-ttu-id="96d7d-110">Joukkotuonnin luokitusten ja arvostelujen tiedot kaikille tuotteille Microsoft Power BI -mallissa niin, että luokitusten ja arvostelujen trendit voidaan analysoida.</span><span class="sxs-lookup"><span data-stu-id="96d7d-110">Bulk-import ratings and reviews data for all products into a Microsoft Power BI template, so that trends for ratings and reviews can be analyzed.</span></span>

## <a name="access-ratings-and-reviews-moderation-features"></a><span data-ttu-id="96d7d-111">Käyttöoikeuksien luokitusten ja arviointien valvontatoiminnot</span><span class="sxs-lookup"><span data-stu-id="96d7d-111">Access ratings and reviews moderation features</span></span>

<span data-ttu-id="96d7d-112">Voit käyttää verkkokauppasivuston hallintatyökalun luokituksia ja arviointien valvontatoimintoja noudattamalla seuraavia ohjeita.</span><span class="sxs-lookup"><span data-stu-id="96d7d-112">To access ratings and reviews moderation features in the e-Commerce site management tool, follow these steps.</span></span>

1. <span data-ttu-id="96d7d-113">Kirjaudu [Microsoft Lifecycle Servicesiin (LCS)](https://lcs.dynamics.com).</span><span class="sxs-lookup"><span data-stu-id="96d7d-113">Sign in to [Microsoft Lifecycle Services (LCS)](https://lcs.dynamics.com).</span></span>
1. <span data-ttu-id="96d7d-114">Avaa projekti, joka sisältää sen ympäristön, jossa haluat alustaa sähköisen kaupankäynnin.</span><span class="sxs-lookup"><span data-stu-id="96d7d-114">Open the project that contains the environment where you want to initialize e-Commerce.</span></span>
1. <span data-ttu-id="96d7d-115">Valitse **Ympäristöt**-osassa ympäristö.</span><span class="sxs-lookup"><span data-stu-id="96d7d-115">In the **Environments** section, select the environment.</span></span>
1. <span data-ttu-id="96d7d-116">Valitse **Ympäristön ominaisuudet** -kohdassa **Vähittäiskaupan hallinta**.</span><span class="sxs-lookup"><span data-stu-id="96d7d-116">Under **Environment features**, select **Retail manage**.</span></span>
1. <span data-ttu-id="96d7d-117">Valitse **Verkkokauppa**-välilehden **Linkit**-kohdassa **Verkkokauppasivuston hallintatyökalu**.</span><span class="sxs-lookup"><span data-stu-id="96d7d-117">On the **e-Commerce** tab under **Links**, select **e-Commerce Site management tool**.</span></span>

## <a name="read-a-review"></a><span data-ttu-id="96d7d-118">Arvostelun lukeminen</span><span class="sxs-lookup"><span data-stu-id="96d7d-118">Read a review</span></span> 

1. <span data-ttu-id="96d7d-119">Siirry kohtaan **Aloitus \> Arvostelut \> Valvonta**.</span><span class="sxs-lookup"><span data-stu-id="96d7d-119">Go to **Home \> Reviews \> Moderation**.</span></span>
1. <span data-ttu-id="96d7d-120">Suodata tuotteen arvostelut tuotteen tunnuksen, tuotteen nimen tai arvostelun tekstin mukaan sivun oikeassa yläkulmassa olevan hakukentän avulla.</span><span class="sxs-lookup"><span data-stu-id="96d7d-120">Use the search field in the upper right of the page to filter the reviews that are shown by product ID, product name, or review text.</span></span>

<span data-ttu-id="96d7d-121">Lisäsuodattimien avulla voit rajoittaa arvosteluita kauden, arvioinnin, kanavan tai vaikutuksen tila (poistettu, vastattu tai raportoitu).</span><span class="sxs-lookup"><span data-stu-id="96d7d-121">Additional filters let you limit the reviews by period, rating, channel, or concern status (taken down, responded, or reported).</span></span>

![Valvonnan aloitussivu](media/rnr-moderation-home.png) 

## <a name="respond-to-a-review"></a><span data-ttu-id="96d7d-123">Arvosteluun vastaaminen</span><span class="sxs-lookup"><span data-stu-id="96d7d-123">Respond to a review</span></span> 

<span data-ttu-id="96d7d-124">Joskus tuotteen ostaneet asiakkaat ilmaisevat tyytyväisyyttä tai tyytymättömyyttä tai he eivät tiedä, miten tuotetta käytetään.</span><span class="sxs-lookup"><span data-stu-id="96d7d-124">Sometimes, customers who purchased a product express their satisfaction or dissatisfaction, or they don't understand how to use the product.</span></span> <span data-ttu-id="96d7d-125">Valvoja voi vastata arvosteluun.</span><span class="sxs-lookup"><span data-stu-id="96d7d-125">As a moderator, you can post a response to a review.</span></span> <span data-ttu-id="96d7d-126">Tämä vastaus näkyy yhdessä arvostelun kanssa sivustossa.</span><span class="sxs-lookup"><span data-stu-id="96d7d-126">This response appears together with the review on the site.</span></span> 

<span data-ttu-id="96d7d-127">Voit vastata arvosteluun seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="96d7d-127">To respond to a review, follow these steps.</span></span>

1. <span data-ttu-id="96d7d-128">Siirry kohtaan **Aloitus \> Arvostelut \> Valvonta**.</span><span class="sxs-lookup"><span data-stu-id="96d7d-128">Go to **Home \> Reviews \> Moderation**.</span></span>
1. <span data-ttu-id="96d7d-129">Etsi ja valitse arvostelu, johon haluat vastata.</span><span class="sxs-lookup"><span data-stu-id="96d7d-129">Find and select the review that requires a response.</span></span>
1. <span data-ttu-id="96d7d-130">Valitse oikeanpuoleisessa ominaisuusruudussa **Lisää vastaus**.</span><span class="sxs-lookup"><span data-stu-id="96d7d-130">In the properties pane on the right, select **Add a response**.</span></span>
1. <span data-ttu-id="96d7d-131">Kirjoita vastauksen teksti ja nimi, jonka haluat näkyvän vastaajan kohdalla.</span><span class="sxs-lookup"><span data-stu-id="96d7d-131">Enter the response text and the name that should be shown for the responder.</span></span> <span data-ttu-id="96d7d-132">Vastaajan oletusnimi on **valvoja**.</span><span class="sxs-lookup"><span data-stu-id="96d7d-132">The default responder name is **Moderator**.</span></span>
1. <span data-ttu-id="96d7d-133">Kun olet valmis, valitse **Kirjaa vastaus**.</span><span class="sxs-lookup"><span data-stu-id="96d7d-133">When you've finished, select **Post response**.</span></span>

![Arvosteluun vastaaminen](media/rnr-moderation-response.png) 

## <a name="take-down-a-review"></a><span data-ttu-id="96d7d-135">Arvostelun poistaminen</span><span class="sxs-lookup"><span data-stu-id="96d7d-135">Take down a review</span></span> 

<span data-ttu-id="96d7d-136">Joskus valvojien kannattaa poistaa asiakkaiden arvosteluita liiketoiminnallisista syistä.</span><span class="sxs-lookup"><span data-stu-id="96d7d-136">Sometimes, there is a business justification for moderators to take down customer reviews.</span></span> 

<span data-ttu-id="96d7d-137">Voit poistaa arvostelun seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="96d7d-137">To take down a review, follow these steps.</span></span>

1. <span data-ttu-id="96d7d-138">Siirry kohtaan **Aloitus \> Arvostelut \> Valvonta**.</span><span class="sxs-lookup"><span data-stu-id="96d7d-138">Go to **Home \> Reviews \> Moderation**.</span></span>
1. <span data-ttu-id="96d7d-139">Etsi ja valitse arvostelu, jonka haluat poistaa.</span><span class="sxs-lookup"><span data-stu-id="96d7d-139">Find and select the review that must be taken down.</span></span>
1. <span data-ttu-id="96d7d-140">Valitse oikeanpuoleisessa ominaisuusruudussa poiston syy ja valitse sitten **Poista**.</span><span class="sxs-lookup"><span data-stu-id="96d7d-140">In the properties pane on the right, select a takedown reason, and then select **Take down**.</span></span>
    
## <a name="delete-a-customers-reviews-at-the-customers-request"></a><span data-ttu-id="96d7d-141">Asiakkaan arvostelujen poistaminen asiakkaan pyynnöstä</span><span class="sxs-lookup"><span data-stu-id="96d7d-141">Delete a customer's reviews at the customer's request</span></span> 

<span data-ttu-id="96d7d-142">Joskus asiakkaat haluavat, että luokitukset ja arvostelut poistetaan pysyvästi sähköisen kaupankäynnin sivustosta.</span><span class="sxs-lookup"><span data-stu-id="96d7d-142">Sometimes, customers want their ratings and reviews data to be permanently deleted from an e-Commerce website.</span></span> <span data-ttu-id="96d7d-143">Valvoja, joka vastaanottaa poistopyynnön asiakkaalta, voi poistaa asiakkaan tiedot käyttämällä arvostelun poistotoimintoa.</span><span class="sxs-lookup"><span data-stu-id="96d7d-143">A moderator who receives a removal request from a customer can remove the customer's data by using the review deletion feature.</span></span> <span data-ttu-id="96d7d-144">Valvoja tarvitsee asiakkaan sen sähköpostiosoitteen, jota on käytetty sisäänkirjauksessa ja arvostelujen antamisessa, jotta hän voi etsiä ja poistaa asiakkaan tiedot.</span><span class="sxs-lookup"><span data-stu-id="96d7d-144">To find and delete a customer's data, the moderator requires the email address that the customer used to sign in and provide reviews.</span></span> 

<span data-ttu-id="96d7d-145">Voit etsiä ja poistaa asiakkaan tietoja seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="96d7d-145">To find and delete customer data, follow these steps.</span></span>

1. <span data-ttu-id="96d7d-146">Siirry kohtaan **Aloitus \> Arvostelut \> Poista**.</span><span class="sxs-lookup"><span data-stu-id="96d7d-146">Go to **Home \> Reviews \> Delete**.</span></span>
1. <span data-ttu-id="96d7d-147">Syötä **Hae käyttäjiä sähköpostiosoitteen avulla** -kenttään asiakkaan sähköpostiosoite ja valitse sitten **Hae**.</span><span class="sxs-lookup"><span data-stu-id="96d7d-147">In the **Search for users by email address** field, enter the customer's email address, and then select **Search**.</span></span>
1. <span data-ttu-id="96d7d-148">Jos asiakkaalla on arvosteluaktiviteetteja (esimerkiksi arvostelun lähetyksiä, äänestyksiä toisen asiakkaan arvosteluista tai kommentteja toisen asiakkaan arvostelusta), näkyvissä on tuloksia.</span><span class="sxs-lookup"><span data-stu-id="96d7d-148">If the customer has any review activity (for example, review submissions, votes about the helpfulness of another customer's reviews, or comments about another customer's review), the results are shown.</span></span> <span data-ttu-id="96d7d-149">Jokaisen nimikkeen kohdalla on **Poista**-painike.</span><span class="sxs-lookup"><span data-stu-id="96d7d-149">For each item, there is a **Delete** button.</span></span>
1. <span data-ttu-id="96d7d-150">Valitse jokaisen poistettavan nimikkeen kohdalla **Poista**.</span><span class="sxs-lookup"><span data-stu-id="96d7d-150">For each item that must be deleted, select **Delete**.</span></span> <span data-ttu-id="96d7d-151">Kun sinulta kysytään vahvistusta, valitse **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="96d7d-151">When you're prompted for confirmation, select **Yes**.</span></span> 
    
![Asiakkaan tietojen poistaminen](media/rnr-moderation-delete-reviews.png) 

> [!NOTE]
> - <span data-ttu-id="96d7d-153">Tietojen poistaminen kokonaan järjestelmästä voi kestää jopa seitsemän päivää.</span><span class="sxs-lookup"><span data-stu-id="96d7d-153">It can take up to seven days for data to be completely removed from the system.</span></span> <span data-ttu-id="96d7d-154">Valvojien tulee ilmoittaa asiakkaille tästä viivästyksestä.</span><span class="sxs-lookup"><span data-stu-id="96d7d-154">Moderators should notify customers about this delay.</span></span>
> - <span data-ttu-id="96d7d-155">Jos asiakkaat ovat muuttaneet nimensä tilin asetuksissa, hakutuloksissa saattaa näkyä useita nimikkeitä.</span><span class="sxs-lookup"><span data-stu-id="96d7d-155">If customers have changed their name in their account settings, multiple items might appear in the search results.</span></span> <span data-ttu-id="96d7d-156">Tässä tapauksessa asiakkaan tietojen poistaminen kokonaan edellyttää, että valvoja valitsee **Poista**-kohdan kaikille nimikkeille.</span><span class="sxs-lookup"><span data-stu-id="96d7d-156">In this case, to completely delete the customer's data, the moderator must select **Delete** for each item.</span></span> 

## <a name="download-ratings-and-reviews-data"></a><span data-ttu-id="96d7d-157">Luokitusten ja arvostelujen tietojen lataaminen</span><span class="sxs-lookup"><span data-stu-id="96d7d-157">Download ratings and reviews data</span></span>

<span data-ttu-id="96d7d-158">Luokitusten ja arvostelujen valvontatyökalun avulla valvojat voivat tuoda luokitusten ja arvostelujen tiedot joukkona ja analysoida trendejä.</span><span class="sxs-lookup"><span data-stu-id="96d7d-158">The ratings and reviews moderation tool lets moderators import ratings and reviews data in bulk, so that they can analyze trends.</span></span> <span data-ttu-id="96d7d-159">Perusmittarit sisältävä Power BI -malli on käytettävissä.</span><span class="sxs-lookup"><span data-stu-id="96d7d-159">A Power BI template that includes basic metrics is available.</span></span> <span data-ttu-id="96d7d-160">Tämän mallin avulla valvojat voivat yhdistää joukkona tuodut tiedot ja tarkastella koontinäyttöä.</span><span class="sxs-lookup"><span data-stu-id="96d7d-160">Moderators can use this template to connect bulk-imported data and view a dashboard.</span></span> <span data-ttu-id="96d7d-161">Heidän ei tarvitse luoda mukautettua koontinäyttöä.</span><span class="sxs-lookup"><span data-stu-id="96d7d-161">They don't have to create a custom dashboard.</span></span> <span data-ttu-id="96d7d-162">Valvojat voivat myös mukauttaa Power BI -mallin vastaamaan erityistarpeita.</span><span class="sxs-lookup"><span data-stu-id="96d7d-162">Moderators can also customize the Power BI template to meet their specific needs.</span></span> 

<span data-ttu-id="96d7d-163">Voit ladata luokitusten ja arvostelujen tiedot seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="96d7d-163">To download ratings and reviews data, follow these steps.</span></span>

1. <span data-ttu-id="96d7d-164">Siirry kohtaan **Aloitus \> Arvostelut \> Raportointi**.</span><span class="sxs-lookup"><span data-stu-id="96d7d-164">Go to **Home \> Reviews \> Reporting**.</span></span>
1. <span data-ttu-id="96d7d-165">Valitse **Lataa arvostelujen tiedot**, jos haluat ladata luokitusten ja arvostelujen tiedot joukkona CSV-muodossa.</span><span class="sxs-lookup"><span data-stu-id="96d7d-165">Select **Download reviews data** to download ratings and reviews data in bulk in comma-separated values (CSV) format.</span></span>

## <a name="view-ratings-and-reviews-trends"></a><span data-ttu-id="96d7d-166">Luokitusten ja arvostelujen trendien tarkasteleminen</span><span class="sxs-lookup"><span data-stu-id="96d7d-166">View ratings and reviews trends</span></span>

<span data-ttu-id="96d7d-167">Valvojat voivat ladata Power BI -mallin niin, että he voivat tarkastella trendejä koontinäytössä.</span><span class="sxs-lookup"><span data-stu-id="96d7d-167">Moderators can download the Power BI template so that they can view trends in a dashboard.</span></span>

<span data-ttu-id="96d7d-168">Voit tarkastella luokitusten ja arvostelujen tietoja seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="96d7d-168">To view ratings and reviews trends, follow these steps.</span></span>

1. <span data-ttu-id="96d7d-169">Siirry kohtaan **Aloitus \> Arvostelut \> Raportointi**.</span><span class="sxs-lookup"><span data-stu-id="96d7d-169">Go to **Home \> Reviews \> Reporting**.</span></span>
1. <span data-ttu-id="96d7d-170">Lataa malli valitsemalla **PowerBI-malli**.</span><span class="sxs-lookup"><span data-stu-id="96d7d-170">Select **PowerBI template** to download the template.</span></span>

    ![Power BI -mallin lataaminen](media/rnr-moderation-reports.png) 

1. <span data-ttu-id="96d7d-172">Avaa ladattu malli käyttämällä Power BI -sovellusta.</span><span class="sxs-lookup"><span data-stu-id="96d7d-172">Open the downloaded template by using the Power BI app.</span></span> <span data-ttu-id="96d7d-173">Sulje näyttöön avautuva **Verkkosisällön käyttöoikeus** -valintaikkuna ja sulje sitten näyttöön tuleva Päivitys-virhesanoma.</span><span class="sxs-lookup"><span data-stu-id="96d7d-173">Close the **Access to web content** dialog box that appears, and then close the "Refresh" error message that appears.</span></span>
1. <span data-ttu-id="96d7d-174">Siirry kohtaan **Aloitus**, valitse **Muokkaa kyselyitä** ja valitse sitten **Tietolähteen asetukset**.</span><span class="sxs-lookup"><span data-stu-id="96d7d-174">Go to **Home**, select **Edit queries**, and then select **Data source settings**.</span></span>
1. <span data-ttu-id="96d7d-175">Valitse **Tietolähteen asetukset** -valintaikkunassa **Muuta lähdettä**.</span><span class="sxs-lookup"><span data-stu-id="96d7d-175">In the **Data source settings** dialog box, select **Change Source**.</span></span>
1. <span data-ttu-id="96d7d-176">Syötä **URL-osoite**-kenttään edellisessä proseduurissa ladattujen arvostelujen tietojen polku (esimerkiksi **c:\\reviews\\ReviewsData.csv**).</span><span class="sxs-lookup"><span data-stu-id="96d7d-176">In the **URL** field, enter the path of the reviews data that you downloaded in the previous procedure (for example, **c:\\reviews\\ReviewsData.csv**).</span></span>

    ![URL-osoite-kenttä CSV-valintaikkunassa](media/rnr-powerbi-datasource-settings.png) 

1. <span data-ttu-id="96d7d-178">Valitse **OK** ja valitse sitten **Käytä muutoksia**.</span><span class="sxs-lookup"><span data-stu-id="96d7d-178">Select **OK**, and then select **Apply changes**.</span></span> <span data-ttu-id="96d7d-179">Muutokset otetaan käyttöön tietolähteessä muutaman minuutin kuluessa.</span><span class="sxs-lookup"><span data-stu-id="96d7d-179">It will take one to two minutes to apply your changes to the data source.</span></span>
1. <span data-ttu-id="96d7d-180">Valitse **Trendien taulukko**, jos haluat tarkastella luokitusten ja arvostelujen trendejä.</span><span class="sxs-lookup"><span data-stu-id="96d7d-180">Select **Trends sheet** to view ratings and reviews trends.</span></span>

    ![Luokitusten ja arvostelujen trendit](media/rnr-powerbi-dashboard-template.png) 
    
## <a name="additional-resources"></a><span data-ttu-id="96d7d-182">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="96d7d-182">Additional resources</span></span>

[<span data-ttu-id="96d7d-183">Luokitukset ja arvostelut – yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="96d7d-183">Ratings and reviews overview</span></span>](ratings-reviews-overview.md)

[<span data-ttu-id="96d7d-184">Osallistu käyttääksesi luokituksia ja arvosteluja</span><span class="sxs-lookup"><span data-stu-id="96d7d-184">Opt in to use ratings and reviews</span></span>](opt-in-ratings-reviews.md)

[<span data-ttu-id="96d7d-185">Määritä luokitukset ja arvostelut</span><span class="sxs-lookup"><span data-stu-id="96d7d-185">Configure ratings and reviews</span></span>](configure-ratings-reviews.md)

[<span data-ttu-id="96d7d-186">Tuoteluokitusten synkronoiminen Dynamics 365 Retailissa</span><span class="sxs-lookup"><span data-stu-id="96d7d-186">Sync product ratings in Dynamics 365 Retail</span></span>](sync-product-ratings.md)
