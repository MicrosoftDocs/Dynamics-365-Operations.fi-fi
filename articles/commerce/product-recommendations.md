---
title: Tuotesuositusten yleiskatsaus
description: Tässä aiheessa on yleisiä tietoja tuotesuosituksista. Tuotesuositusten avulla asiakkaat löytävät helposti ja nopeasti tuotteita, joita he haluavat. He löytävät jopa tuotteita, joita he eivät alun perin aikoneet ostaa.
author: Moonma
manager: AnnBe
ms.date: 05/26/2020
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
ms.search.industry: Retail
ms.author: moonma
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: eb64cd05ac8580c3ddcd719d62544f1edbdbef0b
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5231029"
---
# <a name="product-recommendations-overview"></a><span data-ttu-id="fc9f3-104">Tuotesuositusten yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="fc9f3-104">Product recommendations overview</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="fc9f3-105">Microsoft Dynamics 365 Commerce -sovelluksen avulla voidaan näyttää tuotesuosituksia sähköisen kaupankäynnin sivustossa ja myyntipistelaitteessa.</span><span class="sxs-lookup"><span data-stu-id="fc9f3-105">Microsoft Dynamics 365 Commerce can be used to show product recommendations on the e-Commerce website and point of sale (POS) device.</span></span> <span data-ttu-id="fc9f3-106">Tuotesuositukset ovat nimikkeitä, joista asiakas voi olla kiinnostunut.</span><span class="sxs-lookup"><span data-stu-id="fc9f3-106">Product recommendations are items that a customer might be interested in.</span></span> <span data-ttu-id="fc9f3-107">Suositukset perustuvat muiden asiakkaiden ostotrendeihin verkko- ja kivijalkamyymälöissä.</span><span class="sxs-lookup"><span data-stu-id="fc9f3-107">The recommendations are based on the purchase trends of other customers in online and brick-and-mortar stores.</span></span>

<span data-ttu-id="fc9f3-108">Tuotesuositusten avulla asiakkaat löytävät helposti ja nopeasti tuotteita, joita he haluavat. Samalla he saavat kokemuksen hyvin toimivasta sovelluksesta.</span><span class="sxs-lookup"><span data-stu-id="fc9f3-108">Product recommendations allow customers to easily and quickly find products that they want while they have an experience that serves them well.</span></span> <span data-ttu-id="fc9f3-109">Ristiinmyyntiä ja lisämyyntiä voidaan käyttää myös autettaessa asiakkaita löytämään tuotteita, joita he eivät alun perin aikoneet ostaa.</span><span class="sxs-lookup"><span data-stu-id="fc9f3-109">Cross-selling and upselling can even be used to assist customers find additional products that they didn't originally intend to buy.</span></span> <span data-ttu-id="fc9f3-110">Suositusten käyttäminen tuotteiden etsimisessä voi luoda lisää muuntomahdollisuuksia, auttaa myyntituoton lisäämisessä ja jopa parantaa asiakastyytyväisyyttä ja asiakkaiden säilyttämistä.</span><span class="sxs-lookup"><span data-stu-id="fc9f3-110">When recommendations are used to enhance product discovery, they create more conversion opportunities, help increase sales revenue, and even amplify customer satisfaction and retention.</span></span>

<span data-ttu-id="fc9f3-111">Sähköisessä kaupankäynnissä tuotesuositukset perustuvat Microsoftin koneoppimisen teknologian perusteella laatimiin suosituksiin.</span><span class="sxs-lookup"><span data-stu-id="fc9f3-111">In e-Commerce, product recommendations are powered by Microsoft Recommendations machine learning technologies on a large scale.</span></span>

## <a name="recommendation-service"></a><span data-ttu-id="fc9f3-112">Suosituspalvelu</span><span class="sxs-lookup"><span data-stu-id="fc9f3-112">Recommendation service</span></span>

<span data-ttu-id="fc9f3-113">Tuotesuositukset-palvelu hyödyntää tekoäly-ja kone opiskelu tekniikoita (AI-ML) seuraavalla tavalla:</span><span class="sxs-lookup"><span data-stu-id="fc9f3-113">The product recommendations service utilizes artificial intelligence and machine learning (AI-ML) technologies in the following way:</span></span>

- <span data-ttu-id="fc9f3-114">Tiedot muodossa, jota suosituspalvelu vaatii, saadaan Commercen toiminnallisesta tietokannasta. Tiedot lähetetään Azure Data Lake Storageen tai entiteettimyymälään.</span><span class="sxs-lookup"><span data-stu-id="fc9f3-114">Data in the format that the Recommendation service requires is extracted from the Commerce operational database and sent to Azure Data Lake Storage or Entity store.</span></span>
- <span data-ttu-id="fc9f3-115">Suosituspalvelu käyttää tallennettuja tietoja suositusmallien opettamisessa **Ihmiset pitävät myös**-, **Ostetaan usein yhdessä**-, **Uudet**-, **Myydyimmät**- ja **Suositut**-luetteloissa.</span><span class="sxs-lookup"><span data-stu-id="fc9f3-115">The recommendations service uses the stored data to train recommendation models for the **People also like**, **Frequently bought together**, **New**, **Best selling**, and **Trending** lists.</span></span>

## <a name="scenarios"></a><span data-ttu-id="fc9f3-116">Skenaariot</span><span class="sxs-lookup"><span data-stu-id="fc9f3-116">Scenarios</span></span>

<span data-ttu-id="fc9f3-117">Tuotesuositukset ovat käytettävissä seuraavissa skenaarioissa:</span><span class="sxs-lookup"><span data-stu-id="fc9f3-117">Product recommendations are available for the following scenarios:</span></span>

- <span data-ttu-id="fc9f3-118">**Millä tahansa sähköisen kaupankäynnin selaus- tai saapumissivulla:** Jos asiakkaat tai myyjät käyvät myymälän sivulla, suositusohjelma ehdottaa tuotteita **Uudet**-, **Myydyimmät**- ja **Suositut**-luetteloissa.</span><span class="sxs-lookup"><span data-stu-id="fc9f3-118">**On any store page for browsing or landing page in e-Commerce:** If customers or store associates visit a store page, the recommendation engine can suggest products in the **New**, **Best Selling**, and **Trending** lists.</span></span>
- <span data-ttu-id="fc9f3-119">**Tuotetietosivu:** Jos asiakkaat tai myyjät käyvät **tuotetietosivulla**, suositusohjelma ehdottaa lisänimikkeitä, joita saatetaan haluta ostaa.</span><span class="sxs-lookup"><span data-stu-id="fc9f3-119">**On the Product details page:** If customers or store associates visit a **Product details** page, the recommendation engine suggests additional items that are also likely to be purchased.</span></span> <span data-ttu-id="fc9f3-120">Nämä nimikkeet näkyvät myös **Ihmiset pitävät myös** -luettelossa.</span><span class="sxs-lookup"><span data-stu-id="fc9f3-120">These items appear in the **People also like** list.</span></span>
- <span data-ttu-id="fc9f3-121">**Tapahtuma-sivu tai Kassasivu** Suositusohjelma ehdottaa nimikkeitä korin kaikkien nimikkeiden luettelon perusteella.</span><span class="sxs-lookup"><span data-stu-id="fc9f3-121">**On the Transaction page or the checkout page:** The recommendation engine suggests items, based on the whole list of items in the basket.</span></span> <span data-ttu-id="fc9f3-122">Nämä nimikkeet näkyvät **Ostetaan usein yhdessä** -luettelossa.</span><span class="sxs-lookup"><span data-stu-id="fc9f3-122">These items appear in the **Frequently bought together** list.</span></span>
- <span data-ttu-id="fc9f3-123">**Henkilökohtaiset suositukset:** Jälleenmyyjät voivat tarjota kirjautuneille asiakkaille henkilökohtaisen **Poimintoja sinulle** -luettelon lisäksi uusia toimintoja, jotka mahdollistavat nykyisten luetteloskenaarioiden mukauttamisen asiakkaaseen perustuen.</span><span class="sxs-lookup"><span data-stu-id="fc9f3-123">**Personalized recommendations:** Merchandizers can provide signed-in customers a personalized **picks for you** list, in addition to new functionality that allows for existing list scenarios to be personalized based on that customer.</span></span> <span data-ttu-id="fc9f3-124">Saat lisätietoja kohdasta [Ota kohdennetut suositukset käyttöön](personalized-recommendations.md).</span><span class="sxs-lookup"><span data-stu-id="fc9f3-124">To learn more, see [Enable personalized recommendations.](personalized-recommendations.md).</span></span>

### <a name="types-of-product-recommendations"></a><span data-ttu-id="fc9f3-125">Tuotesuositusten tyypit</span><span class="sxs-lookup"><span data-stu-id="fc9f3-125">Types of product recommendations</span></span>

<span data-ttu-id="fc9f3-126">Seuraavassa taulussa on automaattisten tuotesuositusten eri tyypit, jotka ovat vähittäismyyjien käytettävissä Dynamics 365 Commerce -ratkaisun käyttöönottoa varten [tuotteen keräilymoduulissa](product-collection-module-overview.md).</span><span class="sxs-lookup"><span data-stu-id="fc9f3-126">The following table describes various types of automated product recommendations available for retailers to implement in their Dynamics 365 Commerce solution via the [product collection module](product-collection-module-overview.md).</span></span> <span data-ttu-id="fc9f3-127">Vähittäismyyjät voivat myös näyttää mukautettuja tuloksia kirjautuneesta käyttäjästä, jos sivuston tekijä valitsee kyseisen vaihtoehdon.</span><span class="sxs-lookup"><span data-stu-id="fc9f3-127">Retailers can also show personalized results for a signed-in user if the site author chooses that option.</span></span>

| <span data-ttu-id="fc9f3-128">Tuotekokoelmamoduuli</span><span class="sxs-lookup"><span data-stu-id="fc9f3-128">Product collection module</span></span>  | <span data-ttu-id="fc9f3-129">Laji</span><span class="sxs-lookup"><span data-stu-id="fc9f3-129">Type</span></span> | <span data-ttu-id="fc9f3-130">kuvaus</span><span class="sxs-lookup"><span data-stu-id="fc9f3-130">Description</span></span> |
|----------------------------|------|-------------|
| <span data-ttu-id="fc9f3-131">Uusi</span><span class="sxs-lookup"><span data-stu-id="fc9f3-131">New</span></span>                        | <span data-ttu-id="fc9f3-132">Algoritmi</span><span class="sxs-lookup"><span data-stu-id="fc9f3-132">Algorithmic</span></span> | <span data-ttu-id="fc9f3-133">Tämä moduuli näyttää luettelon uusimmista tuotteista, jotka on lajiteltu kanaviin ja luetteloihin viime aikoina.</span><span class="sxs-lookup"><span data-stu-id="fc9f3-133">This module shows a list of the newest products that have been recently assorted to channels and catalogs.</span></span> |
| <span data-ttu-id="fc9f3-134">Myydyin</span><span class="sxs-lookup"><span data-stu-id="fc9f3-134">Best selling</span></span>               | <span data-ttu-id="fc9f3-135">Algoritmi</span><span class="sxs-lookup"><span data-stu-id="fc9f3-135">Algorithmic</span></span> | <span data-ttu-id="fc9f3-136">Tämä moduuli näyttää luettelon tuotteista, jotka on järjestetty suurimman myyntimäärän mukaan.</span><span class="sxs-lookup"><span data-stu-id="fc9f3-136">This module shows a list of products that are ranked by the highest number of sales.</span></span> |
| <span data-ttu-id="fc9f3-137">Suosittu</span><span class="sxs-lookup"><span data-stu-id="fc9f3-137">Trending</span></span>                   | <span data-ttu-id="fc9f3-138">Algoritmi</span><span class="sxs-lookup"><span data-stu-id="fc9f3-138">Algorithmic</span></span> | <span data-ttu-id="fc9f3-139">Tämä moduuli näyttää luettelon annetun ajanjakson parhaiten menestyvistä tuotteista parhaan myynnin mukaan lajiteltuina.</span><span class="sxs-lookup"><span data-stu-id="fc9f3-139">This module shows a list of the highest-performing products for a given period, ranked by highest number of sales.</span></span>  |
| <span data-ttu-id="fc9f3-140">Ostetaan usein yhdessä</span><span class="sxs-lookup"><span data-stu-id="fc9f3-140">Frequently bought together</span></span> | <span data-ttu-id="fc9f3-141">AI-ML</span><span class="sxs-lookup"><span data-stu-id="fc9f3-141">AI-ML</span></span> | <span data-ttu-id="fc9f3-142">Tämä moduuli suosittelee luetteloa tuotteista, jotka ostetaan yleisesti yhdessä kuluttajien nykyisen ostoskorin sisällön kanssa.</span><span class="sxs-lookup"><span data-stu-id="fc9f3-142">This module recommends a list of products that are commonly purchased together with the contents of the consumers current cart.</span></span> |
| <span data-ttu-id="fc9f3-143">Ihmiset pitävät myös seuraavista</span><span class="sxs-lookup"><span data-stu-id="fc9f3-143">People also like</span></span>           | <span data-ttu-id="fc9f3-144">AI-ML</span><span class="sxs-lookup"><span data-stu-id="fc9f3-144">AI-ML</span></span> | <span data-ttu-id="fc9f3-145">Tämä moduuli suosittelee tietyn alkutuotteen tuotteita kuluttajien ostotottumusten perusteella.</span><span class="sxs-lookup"><span data-stu-id="fc9f3-145">This module recommends products for a given seed product based on consumer purchase patterns.</span></span> |
| <span data-ttu-id="fc9f3-146">Valinnat sinulle</span><span class="sxs-lookup"><span data-stu-id="fc9f3-146">Picks for you</span></span>              | <span data-ttu-id="fc9f3-147">AI-ML</span><span class="sxs-lookup"><span data-stu-id="fc9f3-147">AI-ML</span></span> | <span data-ttu-id="fc9f3-148">Tämä moduuli suosittelee räätälöityjen tuotteiden luetteloa, joka perustuu kirjautuneen käyttäjän ostomalleihin.</span><span class="sxs-lookup"><span data-stu-id="fc9f3-148">This module recommends a personalized list of products based on purchase patterns of the signed-in user.</span></span> <span data-ttu-id="fc9f3-149">Vieraskäyttäjän luettelo on kutistettu.</span><span class="sxs-lookup"><span data-stu-id="fc9f3-149">For a guest user, this list will be collapsed.</span></span> |

## <a name="additional-resources"></a><span data-ttu-id="fc9f3-150">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="fc9f3-150">Additional resources</span></span>

[<span data-ttu-id="fc9f3-151">Azure Data Lake Storagen käyttöönotto Dynamics 365 Commerce -ympäristössä</span><span class="sxs-lookup"><span data-stu-id="fc9f3-151">Enable Azure Data Lake Storage in a Dynamics 365 Commerce environment</span></span>](enable-adls-environment.md)

[<span data-ttu-id="fc9f3-152">Tuotesuositusten ottaminen käyttöön</span><span class="sxs-lookup"><span data-stu-id="fc9f3-152">Enable product recommendations</span></span>](enable-product-recommendations.md)

[<span data-ttu-id="fc9f3-153">Kohdennettujen suositusten ottaminen käyttöön</span><span class="sxs-lookup"><span data-stu-id="fc9f3-153">Enable personalized recommendations</span></span>](personalized-recommendations.md)

[<span data-ttu-id="fc9f3-154">Kohdennetuista tuotesuosituksista kieltäytyminen</span><span class="sxs-lookup"><span data-stu-id="fc9f3-154">Opt out of personalized recommendations</span></span>](personalization-gdpr.md)

[<span data-ttu-id="fc9f3-155">"Osta samankaltaisia tyylejä" -suositusten käyttöönotto</span><span class="sxs-lookup"><span data-stu-id="fc9f3-155">Enable "shop similar looks" recommendations</span></span>](shop-similar-looks.md)

[<span data-ttu-id="fc9f3-156">Tuotesuositusten lisääminen myyntipisteessä</span><span class="sxs-lookup"><span data-stu-id="fc9f3-156">Add product recommendations on POS</span></span>](product.md)

[<span data-ttu-id="fc9f3-157">Suositusten lisääminen tapahtumanäyttöön</span><span class="sxs-lookup"><span data-stu-id="fc9f3-157">Add recommendations to the transaction screen</span></span>](add-recommendations-control-pos-screen.md)

[<span data-ttu-id="fc9f3-158">AI-ML-suositusten tulosten muokkaaminen</span><span class="sxs-lookup"><span data-stu-id="fc9f3-158">Adjust AI-ML recommendations results</span></span>](modify-product-recommendation-results.md)

[<span data-ttu-id="fc9f3-159">Kuratoitujen suositusten manuaalinen luominen</span><span class="sxs-lookup"><span data-stu-id="fc9f3-159">Manually create curated recommendations</span></span>](create-editorial-recommendation-lists.md)

[<span data-ttu-id="fc9f3-160">Suositusten luominen esittelytietojen avulla</span><span class="sxs-lookup"><span data-stu-id="fc9f3-160">Create recommendations with demo data</span></span>](product-recommendations-demo-data.md)

[<span data-ttu-id="fc9f3-161">Tuotesuositukset – usein kysytyt kysymykset</span><span class="sxs-lookup"><span data-stu-id="fc9f3-161">Product recommendations FAQ</span></span>](faq-recommendations.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]