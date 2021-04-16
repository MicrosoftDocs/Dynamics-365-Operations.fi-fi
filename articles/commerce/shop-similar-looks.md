---
title: "\"Osta samankaltaisia tyylejä\" -suositusten käyttöönotto"
description: Tässä ohjeaiheessa kuvataan, kuinka voit ottaa käyttöön "Osta samankaltaisia tyylejä" -tuotesuositukset Microsoft Dynamics 365 Commercessa.
author: bebeale
ms.date: 08/06/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail, eCommerce
ms.author: bebeale
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 06b5721c423330b8840bb546bdb144c3189c25bb
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2021
ms.locfileid: "5795378"
---
# <a name="enable-shop-similar-looks-recommendations"></a><span data-ttu-id="d5092-103">Vastaavien tuotteiden ostosuositusten ottaminen käyttöön</span><span class="sxs-lookup"><span data-stu-id="d5092-103">Enable "shop similar looks" recommendations</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="d5092-104">Tässä ohjeaiheessa kuvataan, kuinka voit ottaa käyttöön "Osta samankaltaisia tyylejä" -tuotesuositukset Microsoft Dynamics 365 Commercessa.</span><span class="sxs-lookup"><span data-stu-id="d5092-104">This topic describes how to enable "shop similar looks" product recommendations in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="d5092-105">Dynamics 365 Commercen "Osta samankaltaisia tyylejä" -suositusominaisuus, joka käyttää tekoälyä ja koneoppimista (AI-ML) antaakseen suosituksia visuaalisesti vastaavista tuotteista asiakkaille.</span><span class="sxs-lookup"><span data-stu-id="d5092-105">The "shop similar looks" recommendations feature in Dynamics 365 Commerce uses the power of artificial intelligence and machine learning (AI-ML) to deliver recommendations for visually similar products to customers.</span></span> <span data-ttu-id="d5092-106">Tekemällä "Osta samankaltaisia tyylejä" -suosituksia kaikille Commercen kanaville vähittäiskauppiaat voivat lisätä asiakastyytyväisyyttä auttamalla asiakkaita löytämään haluamansa helposti.</span><span class="sxs-lookup"><span data-stu-id="d5092-106">By making "shop similar looks" recommendations available for all retail channels in Commerce, retailers can increase customer satisfaction by helping customers easily find what they want.</span></span>

<span data-ttu-id="d5092-107">"Osta samankaltaisia tyylejä" -suositusten toiminnallisuus käyttää siementuotevalikoimien tuotekuvia etsimään ja suosittelemaan visuaalisesti samanlaisia tuotteita jälleenmyyjän tuoteluettelosta.</span><span class="sxs-lookup"><span data-stu-id="d5092-107">The functionality for "shop similar looks" recommendations uses product images of seed product variants to find and recommend visually similar products in a retailer's product catalog.</span></span> 

<span data-ttu-id="d5092-108">"Osta samankaltaisia tyylejä" -suositukset ovat saatavilla sekä myyntipisteissä (POS) ja sähköisen kaupankäynnin kokemuksissa.</span><span class="sxs-lookup"><span data-stu-id="d5092-108">"Shop similar looks" recommendations are available in both the point of sale (POS) and e-Commerce experiences.</span></span>

### <a name="example-scenarios"></a><span data-ttu-id="d5092-109">Esimerkkiskenaariot</span><span class="sxs-lookup"><span data-stu-id="d5092-109">Example scenarios</span></span>

- <span data-ttu-id="d5092-110">Asiakas tarkastelee mustaa raidallista puseroa ja saa suosituksen samanlaisesta punaisesta puserosta.</span><span class="sxs-lookup"><span data-stu-id="d5092-110">A customer views a black striped sweater and receives a recommendation for a similar sweater in red.</span></span> <span data-ttu-id="d5092-111">Asiakas valitsee suositellun tuotteen alun perin tarkasteltujen tuotteiden asemesta ja saa sen jälkeen suosituksia samankaltaisista tuotteista punaisina.</span><span class="sxs-lookup"><span data-stu-id="d5092-111">The customer selects the recommended product instead of the originally viewed product and then receives recommendations for similar products in red.</span></span> 
- <span data-ttu-id="d5092-112">Asiakas käyttää "Osta samankaltaisia tyylejä" -suosituksia löytääkseen korvakorut pariksi sormukselle, jonka asiakas on kiinnostunut ostamaan.</span><span class="sxs-lookup"><span data-stu-id="d5092-112">A customer uses "shop similar looks" recommendations to discover matching earrings for a ring that the customer is interested in buying.</span></span>

## <a name="enable-shop-similar-looks-recommendations-in-commerce-headquarters"></a><span data-ttu-id="d5092-113">Ota "Osta samankaltaisia tyylejä" -suositukset käyttöön Commerce Headquarters -sovelluksessa</span><span class="sxs-lookup"><span data-stu-id="d5092-113">Enable "shop similar looks" recommendations in Commerce headquarters</span></span>

<span data-ttu-id="d5092-114">Tuotesuosituksia tuetaan vain Commerce-asiakkaille, jotka ovat siirtäneet tallennustilansa Azure Data Lake Gen2:een.</span><span class="sxs-lookup"><span data-stu-id="d5092-114">Product recommendations are supported only for Commerce users who have migrated their storage to Azure Data Lake Gen2.</span></span>

### <a name="prerequisites"></a><span data-ttu-id="d5092-115">Edellytykset</span><span class="sxs-lookup"><span data-stu-id="d5092-115">Prerequisites</span></span>

<span data-ttu-id="d5092-116">Ennen kuin jälleenmyyjät voivat alkaa näyttää "Osta samankaltaisia tyylejä" -suosituksia asiakkaille, seuraavia vaiheita on kaksi:</span><span class="sxs-lookup"><span data-stu-id="d5092-116">Before retailers can begin to show "shop similar looks" recommendations to customers, there are two prerequisite steps:</span></span>

- <span data-ttu-id="d5092-117">[Ota tuotesuositukset käyttöön](enable-product-recommendations.md) Commerce Headquarters -sovelluksessa.</span><span class="sxs-lookup"><span data-stu-id="d5092-117">[Enable product recommendations](enable-product-recommendations.md) in Commerce headquarters.</span></span>
- <span data-ttu-id="d5092-118">Varmista, että mediasisältöpalvelin tukee HTTPS-puheluja.</span><span class="sxs-lookup"><span data-stu-id="d5092-118">Confirm that the media server supports HTTPS calls.</span></span>

<span data-ttu-id="d5092-119">Jotta suositukset-moduuli voi käyttää tuotekuvia, jälleenmyyjien on luotava tuotteen URL-osoitteet.</span><span class="sxs-lookup"><span data-stu-id="d5092-119">For the recommendations engine to access the product images, retailers must generate the product URLs.</span></span> <span data-ttu-id="d5092-120">Luo tuotteen URL-osoitteet Commerce headquartersissa seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="d5092-120">To generate product URLs in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="d5092-121">Siirry kohtaan **Tuotekuvat**.</span><span class="sxs-lookup"><span data-stu-id="d5092-121">Go to **Product images**.</span></span>
1. <span data-ttu-id="d5092-122">Valitse Toimintoruudussa **Määritä mediasisältömalli**.</span><span class="sxs-lookup"><span data-stu-id="d5092-122">On the Action Pane, select **Define media template**.</span></span>
1. <span data-ttu-id="d5092-123">Valitse **Määritä mediasisältömallin** ominaisuudet-ruudun **Median URL-osoitteet** -kohdasta **Luo URL-osoitteita**.</span><span class="sxs-lookup"><span data-stu-id="d5092-123">In the **Define media template** properties pane, under **Media URLs**, select **Generate URLs**.</span></span>

> [!NOTE]
> <span data-ttu-id="d5092-124">Kun otat käyttöön "Osta samankaltaisia tyylejä" -suositukset-toiminnon, tuotesuositusluetteloiden luontiprosessi alkaa.</span><span class="sxs-lookup"><span data-stu-id="d5092-124">When you enable the "shop similar looks" recommendations feature, the process of generating product recommendation lists begins.</span></span> <span data-ttu-id="d5092-125">Enintään yksi päivä saattaa olla tarpeen, ennen kuin nämä luettelot ovat käytettävissä ja näkyvissä verkossa ja myyntipisteissä.</span><span class="sxs-lookup"><span data-stu-id="d5092-125">Up to a day might be required before those lists are available and visible online and on POS terminals.</span></span>

<span data-ttu-id="d5092-126">Jos haluat ottaa käyttöön "Osta samankaltaisia tyylejä" -suositukset-toiminnon Commerce Headquarters -sovelluksessa, toimi seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="d5092-126">To enable the "shop similar looks" recommendations feature in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="d5092-127">Mene **Toimintojen hallintaan**.</span><span class="sxs-lookup"><span data-stu-id="d5092-127">Go to **Feature management**.</span></span>
1. <span data-ttu-id="d5092-128">Etsi ja valitse käytettävissä olevien toimintojen luettelosta **Osta samankaltaisia tyylejä**.</span><span class="sxs-lookup"><span data-stu-id="d5092-128">In the list of available features, search for and select **Shop similar looks**.</span></span>
1. <span data-ttu-id="d5092-129">Ota palvelu käyttöön valitsemalla oikeanpuoleisesta ruudusta **Ota käyttöön**.</span><span class="sxs-lookup"><span data-stu-id="d5092-129">In the right pane, select **Enable** to turn on the service.</span></span>

<span data-ttu-id="d5092-130">Seuraavassa kuvassa näkyy **Osta samankaltaisia tyylejä** -ominaisuus, joka sijaitsee Commerce Headquarters -sovelluksen **toimintojen hallinta** -sivulla.</span><span class="sxs-lookup"><span data-stu-id="d5092-130">The following illustration shows the **Shop similar looks** feature on the **Feature management** page in Commerce headquarters.</span></span>

![Commerce headquartersin toimintojen hallinta -sivun Osta samankaltaisia tyylejä -ominaisuus](./media/enableshopsimilarlooks.png)

<span data-ttu-id="d5092-132">Kun edeltävät tehtävät on suoritettu, POS-päätteisiin päivittyy automaattisesti asiayhteyteen liittyvä **Osta samankaltaisia tuotteita** - paneeli.</span><span class="sxs-lookup"><span data-stu-id="d5092-132">After the preceding tasks been completed, POS terminals are automatically enhanced with a contextual **Shop similar products** panel.</span></span> <span data-ttu-id="d5092-133">Kun valitset **Näytä lisää**, POS-päätteen käyttäjät voidaan viedä erityiseen "Osta samankaltaisia tyylejä" -sivulle, jota voidaan suodattaa edelleen.</span><span class="sxs-lookup"><span data-stu-id="d5092-133">By selecting **See more**, POS terminal users can be taken to a dedicated "shop similar looks" page that can be filtered further.</span></span>

> [!NOTE]
> <span data-ttu-id="d5092-134">Muihin tuotesuosituksiin ei vaikuta, jos poistat "Osta samankaltaisia tyylejä" -suositukset käytöstä.</span><span class="sxs-lookup"><span data-stu-id="d5092-134">If you turn off the "shop similar looks" recommendations feature, no other types of product recommendations are affected.</span></span> <span data-ttu-id="d5092-135">Lisätietoja tuotesuosituksista on kohdassa [Tuotesuositusten yleiskatsaus](product-recommendations.md).</span><span class="sxs-lookup"><span data-stu-id="d5092-135">For more information about product recommendations, see [Product recommendations overview](product-recommendations.md).</span></span>

## <a name="add-a-shop-similar-looks-button-to-product-details-pages-by-using-commerce-site-builder"></a><span data-ttu-id="d5092-136">Osta samankaltaisia tyylejä -painikkeen lisääminen tuotetieto sivuille Commerce site builderin avulla</span><span class="sxs-lookup"><span data-stu-id="d5092-136">Add a Shop similar looks button to product details pages by using Commerce site builder</span></span>

<span data-ttu-id="d5092-137">Kun olet ottanut käyttöön "osta samankaltaisia lookkeja" -suositukset-toiminnon Commerce Headquarters -sovelluksessa, Commerce site Builderin vaihtoehdon avulla jälleenmyyjät voivat lisätä **Osta samankaltaisia tyylejä** -painikkeen osto-ruutuun millä tahansa tuotetietosivulla (PDP).</span><span class="sxs-lookup"><span data-stu-id="d5092-137">After you enable the "shop similar looks" recommendations feature in Commerce headquarters, an option in Commerce site builder lets retailers to add a **Shop similar looks** button to the buy box on any product details page (PDP).</span></span> <span data-ttu-id="d5092-138">Asiakas, joka valitsee tämän painikkeen, viedään omistautuneelle "Osta samankaltaisia tyylejä" -sivulle, joka palauttaa visuaalisesti samankaltaiset tuotteet.</span><span class="sxs-lookup"><span data-stu-id="d5092-138">A customer who selects this button is taken to a dedicated "shop similar looks" page that returns visually similar products.</span></span> <span data-ttu-id="d5092-139">Tällöin asiakas voi suodattaa tuotteita käyttämällä valitsimia.</span><span class="sxs-lookup"><span data-stu-id="d5092-139">There, the customer can use selectors to further filter the products.</span></span>

<span data-ttu-id="d5092-140">Noudata seuraavia ohjeita **Osta samankaltaisia tyylejä** -painikkeen lisäämiseksi tuotetietosivuille (PDP) Commerce site builderin avulla.</span><span class="sxs-lookup"><span data-stu-id="d5092-140">To add a **Shop similar looks** button to a PDP by using Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="d5092-141">Avaa aiemmin luotu sivustonluontisivu, joka sisältää ostolaatikkomoduulin.</span><span class="sxs-lookup"><span data-stu-id="d5092-141">Open an existing site builder page that contains a buy box module.</span></span>
1. <span data-ttu-id="d5092-142">Valitse vasemmasta siirtymisruudusta ostolaatikkomoduuli.</span><span class="sxs-lookup"><span data-stu-id="d5092-142">In the left navigation pane, select the buy box module.</span></span>
1. <span data-ttu-id="d5092-143">Valitse oikeanpuoleisesta siirtymisruudusta **Ota käyttöön Osta samankaltaisia tyylejä -linkki** -valintaruutu.</span><span class="sxs-lookup"><span data-stu-id="d5092-143">In the right navigation pane, select the **Enable Shop Similar Looks Link** check box.</span></span>
1. <span data-ttu-id="d5092-144">Valitse **Tallenna**, valitse **Viimeistele muokkaus** tarkistaaksesi sivun, ja julkaise se valitsemalla **Julkaise**.</span><span class="sxs-lookup"><span data-stu-id="d5092-144">Select **Save**, select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span> <span data-ttu-id="d5092-145">Kun sivu on julkaistu, PDP:n mukana tulee **Osta samankaltaisia tyylejä** -painike.</span><span class="sxs-lookup"><span data-stu-id="d5092-145">After the page is published, the PDP will include a **Shop similar looks** button.</span></span>

<span data-ttu-id="d5092-146">Seuraavassa kuvassa on **Ota käyttöön Osta samankaltaisia tyylejä -linkki** -valintaruutu ja **Osta samankaltaisia lookkeja** -painike esimerkiksi PDP:n sivustomuodostimessa.</span><span class="sxs-lookup"><span data-stu-id="d5092-146">The following illustration shows the **Enable Shop Similar Looks Link** check box and **Shop similar looks** button on an example PDP in site builder.</span></span>

![Ota käyttöön Osta samankaltaisia tyylejä -linkki -valintaruutu ja Osta samanlaisia lookkeja -painike PDP:n sivustomuodostimessa](./media/SSLecomtooling.png)

## <a name="additional-resources"></a><span data-ttu-id="d5092-148">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="d5092-148">Additional resources</span></span>

[<span data-ttu-id="d5092-149">Tuotesuositusten yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="d5092-149">Product recommendations overview</span></span>](product-recommendations.md)

[<span data-ttu-id="d5092-150">Azure Data Lake Storagen käyttöönotto Dynamics 365 Commerce -ympäristössä</span><span class="sxs-lookup"><span data-stu-id="d5092-150">Enable Azure Data Lake Storage in a Dynamics 365 Commerce environment</span></span>](enable-adls-environment.md)

[<span data-ttu-id="d5092-151">Tuotesuositusten ottaminen käyttöön</span><span class="sxs-lookup"><span data-stu-id="d5092-151">Enable product recommendations</span></span>](enable-product-recommendations.md)

[<span data-ttu-id="d5092-152">Kohdennetuista tuotesuosituksista kieltäytyminen</span><span class="sxs-lookup"><span data-stu-id="d5092-152">Opt out of personalized recommendations</span></span>](personalization-gdpr.md)

[<span data-ttu-id="d5092-153">Tuotesuositusten lisääminen myyntipisteessä</span><span class="sxs-lookup"><span data-stu-id="d5092-153">Add product recommendations on POS</span></span>](product.md)

[<span data-ttu-id="d5092-154">Suositusten lisääminen tapahtumanäyttöön</span><span class="sxs-lookup"><span data-stu-id="d5092-154">Add recommendations to the transaction screen</span></span>](add-recommendations-control-pos-screen.md)

[<span data-ttu-id="d5092-155">AI-ML-suositusten tulosten muokkaaminen</span><span class="sxs-lookup"><span data-stu-id="d5092-155">Adjust AI-ML recommendations results</span></span>](modify-product-recommendation-results.md)

[<span data-ttu-id="d5092-156">Kuratoitujen suositusten manuaalinen luominen</span><span class="sxs-lookup"><span data-stu-id="d5092-156">Manually create curated recommendations</span></span>](create-editorial-recommendation-lists.md)

[<span data-ttu-id="d5092-157">Suositusten luominen esittelytietojen avulla</span><span class="sxs-lookup"><span data-stu-id="d5092-157">Create recommendations with demo data</span></span>](product-recommendations-demo-data.md)

[<span data-ttu-id="d5092-158">Tuotesuositukset – usein kysytyt kysymykset</span><span class="sxs-lookup"><span data-stu-id="d5092-158">Product recommendations FAQ</span></span>](faq-recommendations.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
