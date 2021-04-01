---
title: "\"Tuotteet, joissa samankaltainen kuvaus\" -suositusten ottaminen käyttöön"
description: Tässä ohjeaiheessa kuvataan, kuinka voit ottaa käyttöön "Tuotteet, joissa samankaltainen kuvaus" -tuotesuositukset Microsoft Dynamics 365 Commercessa.
author: bsokolov
manager: AnnBe
ms.date: 01/13/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail, eCommerce
ms.author: bebeale
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.16
ms.openlocfilehash: b6b397b1f21e3dfcdb4a2b7fe67ddb541d090a97
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5234386"
---
# <a name="enable-shop-similar-description-recommendations"></a><span data-ttu-id="750e5-103">Vastaavien tuotteiden kuvaukseen perustuvien suositusten ottaminen käyttöön</span><span class="sxs-lookup"><span data-stu-id="750e5-103">Enable "shop similar description" recommendations</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="750e5-104">Tässä ohjeaiheessa kuvataan, kuinka voit ottaa käyttöön "Tuotteet, joissa samankaltainen kuvaus" -tuotesuositukset Microsoft Dynamics 365 Commercessa.</span><span class="sxs-lookup"><span data-stu-id="750e5-104">This topic describes how to enable "shop similar description" product recommendations in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="750e5-105">Dynamics 365 Commercen "Tuotteet, joissa samankaltainen kuvaus" -suositusominaisuus, joka käyttää tekoälyä ja koneoppimista (AI-ML) antaakseen suosituksia tuotteista, joiden kuvaukset ovat samankaltaisia, kuin mitä asiakas etsii.</span><span class="sxs-lookup"><span data-stu-id="750e5-105">The "shop similar description" recommendations feature in Dynamics 365 Commerce uses artificial intelligence and machine learning (AI-ML) to deliver recommendations for products that have descriptions that are similar to what the customer is looking for.</span></span> <span data-ttu-id="750e5-106">Tekemällä "Tuotteet, joissa samankaltainen kuvaus" -suosituksia kaikille Commercen kanaville vähittäiskauppiaat voivat auttaa asiakkaita löytämään haluamansa helposti.</span><span class="sxs-lookup"><span data-stu-id="750e5-106">By making "shop similar description" recommendations available for all retail channels in Commerce, retailers can help customers easily find what they want.</span></span>

<span data-ttu-id="750e5-107">"Tuotteet, joissa samankaltainen kuvaus" -suositusten toiminnallisuus käyttää alkuperäisen tuotteen nimeä ja kuvausta etsimään ja suosittelemaan samanlaisia tuotteita jälleenmyyjän tuoteluettelosta.</span><span class="sxs-lookup"><span data-stu-id="750e5-107">The functionality for "shop similar description" recommendations uses the product name and description of seed products to find and recommend similar products in a retailer's product catalog.</span></span>

<span data-ttu-id="750e5-108">"Tuotteet, joissa samankaltainen kuvaus" -suositukset ovat saatavilla sekä myyntipisteissä (POS) ja sähköisen kaupankäynnin kokemuksissa.</span><span class="sxs-lookup"><span data-stu-id="750e5-108">"Shop similar description" recommendations are available in both the point of sale (POS) and e-commerce experiences.</span></span>

## <a name="example-scenarios"></a><span data-ttu-id="750e5-109">Esimerkkiskenaariot</span><span class="sxs-lookup"><span data-stu-id="750e5-109">Example scenarios</span></span>

<span data-ttu-id="750e5-110">Seuraavissa esimerkkiskenaarioissa kuvataan, millaisia suosituksia "Tuotteet, joissa samankaltainen kuvaus" -toiminnoilla voi olla:</span><span class="sxs-lookup"><span data-stu-id="750e5-110">The following example scenarios show the types of recommendations that the "shop similar description" functionality can provide:</span></span>

- <span data-ttu-id="750e5-111">Asiakas katselee retrotyylisiä paksusankaisia silmälaseja ja saa joukon suosituksia muista samantapaisista laseista, joissa on sama tyyli, vähittäismyyjän toimialan mukaisesti.</span><span class="sxs-lookup"><span data-stu-id="750e5-111">A customer views a pair of retro-style horn-rimmed glasses and receives a set of recommendations for other glasses that have a similar design, in the context of the retailer's industry.</span></span>
- <span data-ttu-id="750e5-112">Asiakas käyttää "Tuotteet, joissa samankaltainen kuvaus" -suosituksia löytääksen samankaltaisia kahvimakuja kuin mitä hän vähittäismyyjältä aiemmin osti.</span><span class="sxs-lookup"><span data-stu-id="750e5-112">A customer uses "shop similar description" recommendations to discover coffee flavors that are similar to a flavor that they previously purchased from the retailer.</span></span>

## <a name="set-up-shop-similar-description-recommendations"></a><span data-ttu-id="750e5-113">"Tuotteet, joissa samankaltainen kuvaus" -suositusten määrittäminen</span><span class="sxs-lookup"><span data-stu-id="750e5-113">Set up "shop similar description" recommendations</span></span>

<span data-ttu-id="750e5-114">Tuotesuosituksia tuetaan vain Commerce-asiakkaille, jotka ovat siirtäneet tallennustilansa Azure Data Lake Storage Gen2:een.</span><span class="sxs-lookup"><span data-stu-id="750e5-114">Product recommendations are supported only for Commerce users who have migrated their storage to Azure Data Lake Storage Gen2.</span></span>

### <a name="prerequisites"></a><span data-ttu-id="750e5-115">Edellytykset</span><span class="sxs-lookup"><span data-stu-id="750e5-115">Prerequisites</span></span>

<span data-ttu-id="750e5-116">Ennen kuin asiakkaille voidaan näyttää "Tuotteet, joissa samankaltainen kuvaus" -suositukset, sinun on täytettävä seuraavat edellytykset:</span><span class="sxs-lookup"><span data-stu-id="750e5-116">Before "shop similar description" recommendations can be shown to customers, you must complete the following prerequisites:</span></span>

- <span data-ttu-id="750e5-117">[Ota tuotesuositukset käyttöön](enable-product-recommendations.md) Commerce Headquarters -sovelluksessa.</span><span class="sxs-lookup"><span data-stu-id="750e5-117">[Enable product recommendations](enable-product-recommendations.md) in Commerce headquarters.</span></span>
- <span data-ttu-id="750e5-118">Varmista, että mediasisältöpalvelin tukee HTTPS-puheluja.</span><span class="sxs-lookup"><span data-stu-id="750e5-118">Confirm that the media server supports HTTPS calls.</span></span>

### <a name="turn-on-the-shop-similar-description-recommendations-feature"></a><span data-ttu-id="750e5-119">Ota "Tuotteet, joissa samankaltainen kuvaus" -suositusten ominaisuus käyttöön</span><span class="sxs-lookup"><span data-stu-id="750e5-119">Turn on the "shop similar description" recommendations feature</span></span>

<span data-ttu-id="750e5-120">Jos haluat ottaa käyttöön "Tuotteet, joissa samankaltainen kuvaus" -suositukset-toiminnon Commerce headquarters -sovelluksessa, toimi seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="750e5-120">To turn on the "shop similar description" recommendations feature in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="750e5-121">Etsi ja valitse **Tuotteet, joissa samankaltainen kuvaus** **Toimintohallinta**-työtilan käytettävissä olevien ominaisuuksien luettelosta.</span><span class="sxs-lookup"><span data-stu-id="750e5-121">In the **Feature management** workspace, in the list of available features, search for and select **Shop similar description**.</span></span>
1. <span data-ttu-id="750e5-122">Valitse oikeanpuoleisesta ruudusta **Ota käyttöön**.</span><span class="sxs-lookup"><span data-stu-id="750e5-122">In the right pane, select **Enable**.</span></span>

> [!NOTE]
> <span data-ttu-id="750e5-123">Kun otat ominaisuuden käyttöön, järjestelmä alkaa luoda tuotesuositusluetteloita.</span><span class="sxs-lookup"><span data-stu-id="750e5-123">When you turn on the feature, the system starts to generate product recommendation lists.</span></span> <span data-ttu-id="750e5-124">Saattaa kulua vuorokausi, ennen kuin nämä luettelot ovat käytettävissä ja näkyvissä verkossa ja myyntipisteissä.</span><span class="sxs-lookup"><span data-stu-id="750e5-124">It might take up to a day for those lists to become available and visible online and on POS terminals.</span></span>
>
> <span data-ttu-id="750e5-125">Jos poistat toiminnon käytöstä, se ei vaikuta muuntyyppisiin tuotesuosituksiin.</span><span class="sxs-lookup"><span data-stu-id="750e5-125">If you turn off the feature, other types of product recommendations aren't affected.</span></span> <span data-ttu-id="750e5-126">Lisätietoja tuotesuosituksista on kohdassa [Tuotesuositusten yleiskatsaus](product-recommendations.md).</span><span class="sxs-lookup"><span data-stu-id="750e5-126">For more information about product recommendations, see [Product recommendations overview](product-recommendations.md).</span></span>

## <a name="add-a-shop-similar-description-button-to-product-details-pages"></a><span data-ttu-id="750e5-127">Tuotteet, joissa samankaltainen kuvaus -painikkeen lisääminen tuotetietosivuille</span><span class="sxs-lookup"><span data-stu-id="750e5-127">Add a Shop similar description button to product details pages</span></span>

<span data-ttu-id="750e5-128">Kun olet ottanut käyttöön "Tuotteet, joissa samankaltainen kuvaus" -suositukset-toiminnon Commerce headquarters -sovelluksessa, voit lisätä **Tuotteet, joissa samankaltainen kuvaus** -painikkeen ostoruutuun millä tahansa tuotetietosivulla (PDP).</span><span class="sxs-lookup"><span data-stu-id="750e5-128">After you turn on the "shop similar description" recommendations feature in Commerce headquarters, you can add a **Shop similar description** button to the buy box on any product details page (PDP).</span></span> <span data-ttu-id="750e5-129">Asiakas, joka valitsee tämän painikkeen, viedään erilliselle **Tuotteet, joissa samankaltainen kuvaus** -sivulle, joka näyttää samankaltaiset tuotteet.</span><span class="sxs-lookup"><span data-stu-id="750e5-129">A customer who selects this button is taken to a dedicated **Shop similar description** page that shows visually similar products.</span></span> <span data-ttu-id="750e5-130">Näin asiakas voi suodattaa tuotteita käyttämällä valitsimia.</span><span class="sxs-lookup"><span data-stu-id="750e5-130">The customer can then use selectors to further filter the products.</span></span>

<span data-ttu-id="750e5-131">Noudata seuraavia ohjeita **Tuotteet, joissa samankaltainen kuvaus** -painikkeen lisäämiseksi tuotetietosivuille (PDP) Commercen sivustonmuodostimen avulla.</span><span class="sxs-lookup"><span data-stu-id="750e5-131">To add a **Shop similar description** button to a PDP by using Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="750e5-132">Avaa aiemmin luotu sivustonluontisivu, joka sisältää ostolaatikkomoduulin.</span><span class="sxs-lookup"><span data-stu-id="750e5-132">Open an existing site builder page that contains a buy box module.</span></span>
1. <span data-ttu-id="750e5-133">Valitse vasemmasta siirtymisruudusta ostolaatikkomoduuli.</span><span class="sxs-lookup"><span data-stu-id="750e5-133">In the left navigation pane, select the buy box module.</span></span>
1. <span data-ttu-id="750e5-134">Valitse oikeanpuoleisesta ruudusta **Ota käyttöön Tuotteet, joissa samankaltainen kuvaus -linkki** -valintaruutu.</span><span class="sxs-lookup"><span data-stu-id="750e5-134">In the right pane, select the **Enable Shop Similar description Link** check box.</span></span>
1. <span data-ttu-id="750e5-135">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="750e5-135">Select **Save**.</span></span>
1. <span data-ttu-id="750e5-136">Valitse **Lopeta muokkaus** tallentaaksesi sivun ja valitse sitten **Julkaise** julkaistaksesi sen.</span><span class="sxs-lookup"><span data-stu-id="750e5-136">Select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span> <span data-ttu-id="750e5-137">Kun sivu on julkaistu, PDP sisältää **Tuotteet, joissa samankaltainen kuvaus** -painikkeen.</span><span class="sxs-lookup"><span data-stu-id="750e5-137">After the page is published, the PDP will include a **Shop similar description** button.</span></span>

<span data-ttu-id="750e5-138">Seuraavassa kuvassa on **ota käyttöön Tuotteet, joissa samankaltainen kuvaus -linkki** -valintaruutu ja **Tuotteet, joissa samankaltainen kuvaus** -painike esimerkkituotetietosivulla sivustomuodostimessa.</span><span class="sxs-lookup"><span data-stu-id="750e5-138">The following illustration shows the **Enable shop similar description Link** check box and the **Shop similar description** button on an example PDP in site builder.</span></span>

![Ota käyttöön Tuotteet, joissa samankaltainen kuvaus -linkki -valintaruutu ja Tuotteet, joissa samankaltainen kuvaus -painike tuotetietosivulla sivustomuodostimessa](./media/ter_site_builder_buybox_button.png)

## <a name="additional-resources"></a><span data-ttu-id="750e5-140">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="750e5-140">Additional resources</span></span>

[<span data-ttu-id="750e5-141">Tuotesuositusten yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="750e5-141">Product recommendations overview</span></span>](product-recommendations.md)

[<span data-ttu-id="750e5-142">Azure Data Lake Storagen käyttöönotto Dynamics 365 Commerce -ympäristössä</span><span class="sxs-lookup"><span data-stu-id="750e5-142">Enable Azure Data Lake Storage in a Dynamics 365 Commerce environment</span></span>](enable-adls-environment.md)

[<span data-ttu-id="750e5-143">Ota tuotesuositukset käyttöön</span><span class="sxs-lookup"><span data-stu-id="750e5-143">Enable product recommendations</span></span>](enable-product-recommendations.md)

[<span data-ttu-id="750e5-144">Vastaavien tuotteiden ostosuositusten ottaminen käyttöön</span><span class="sxs-lookup"><span data-stu-id="750e5-144">Enable "shop similar looks" recommendations</span></span>](shop-similar-looks.md)

[<span data-ttu-id="750e5-145">AI-ML-suositusten tulosten muokkaaminen</span><span class="sxs-lookup"><span data-stu-id="750e5-145">Adjust AI-ML recommendations results</span></span>](modify-product-recommendation-results.md)

[<span data-ttu-id="750e5-146">Kuratoitujen suositusten manuaalinen luominen</span><span class="sxs-lookup"><span data-stu-id="750e5-146">Manually create curated recommendations</span></span>](create-editorial-recommendation-lists.md)

[<span data-ttu-id="750e5-147">Tuotesuositukset – usein kysytyt kysymykset</span><span class="sxs-lookup"><span data-stu-id="750e5-147">Product recommendations FAQ</span></span>](faq-recommendations.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]