---
title: Tuotesuositusten yleiskatsaus
description: Tässä aiheessa on yleisiä tietoja tuotesuosituksista. Tuotesuositusten avulla asiakkaat löytävät helposti ja nopeasti tuotteita, joita he haluavat. He löytävät jopa tuotteita, joita he eivät alun perin aikoneet ostaa.
author: Moonma
manager: AnnBe
ms.date: 10/1/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: moonma
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: eb369e6d1356ba13a2310d523b671ac57b9642bf
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/06/2019
ms.locfileid: "2770043"
---
# <a name="product-recommendations-overview"></a><span data-ttu-id="c90a0-104">Tuotesuositusten yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="c90a0-104">Product recommendations overview</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="c90a0-105">Microsoft Dynamics 365 Commerce -sovelluksen avulla voidaan näyttää tuotesuosituksia sähköisen kaupankäynnin sivustossa ja myyntipistelaitteessa.</span><span class="sxs-lookup"><span data-stu-id="c90a0-105">Microsoft Dynamics 365 Commerce can be used to show product recommendations on the e-Commerce website and point of sale (POS) device.</span></span> <span data-ttu-id="c90a0-106">Tuotesuositukset ovat nimikkeitä, joista asiakas voi olla kiinnostunut.</span><span class="sxs-lookup"><span data-stu-id="c90a0-106">Product recommendations are items that a customer might be interested in.</span></span> <span data-ttu-id="c90a0-107">Suositukset perustuvat muiden asiakkaiden ostotrendeihin verkko- ja kivijalkamyymälöissä.</span><span class="sxs-lookup"><span data-stu-id="c90a0-107">The recommendations are based on the purchase trends of other customers in online and brick-and-mortar stores.</span></span>

<span data-ttu-id="c90a0-108">Tuotesuositusten avulla asiakkaat löytävät helposti ja nopeasti tuotteita, joita he haluavat. Samalla he saavat kokemuksen hyvin toimivasta sovelluksesta.</span><span class="sxs-lookup"><span data-stu-id="c90a0-108">Product recommendations let customers easily and quickly find products that they want while they have an experience that serves them well.</span></span> <span data-ttu-id="c90a0-109">Ristiinmyyntiä ja lisämyyntiä voidaan käyttää myös autettaessa asiakkaita löytämään tuotteita, joita he eivät alun perin aikoneet ostaa.</span><span class="sxs-lookup"><span data-stu-id="c90a0-109">Cross-selling and upselling can even be used to help customers find additional products than they didn't originally intend to buy.</span></span> <span data-ttu-id="c90a0-110">Suositusten käyttäminen tuotteiden etsimisessä voi luoda lisää muuntomahdollisuuksia, auttaa myyntituoton lisäämisessä ja jopa parantaa asiakastyytyväisyyttä ja asiakkaiden säilyttämistä.</span><span class="sxs-lookup"><span data-stu-id="c90a0-110">When recommendations are used to help with product discovery, they can create more conversion opportunities, help increase sales revenue, and even help enhance customer satisfaction and retention.</span></span>

<span data-ttu-id="c90a0-111">Commercessa tuotesuositukset perustuvat Microsoftin koneoppimisen teknologian perusteella laatimiin suosituksiin.</span><span class="sxs-lookup"><span data-stu-id="c90a0-111">In Commerce, product recommendations are powered by Microsoft Recommendations machine learning technologies on a large scale.</span></span>


## <a name="scenarios"></a><span data-ttu-id="c90a0-112">Skenaariot</span><span class="sxs-lookup"><span data-stu-id="c90a0-112">Scenarios</span></span>

<span data-ttu-id="c90a0-113">Tuotesuositukset ovat käytettävissä seuraavissa skenaarioissa:</span><span class="sxs-lookup"><span data-stu-id="c90a0-113">Product recommendations are available for the following scenarios:</span></span>

- <span data-ttu-id="c90a0-114">**Millä tahansa sähköisen kaupankäynnin selaus- tai saapumissivulla:** Jos asiakkaat tai myyjät käyvät myymälän sivulla, suositusohjelma ehdottaa tuotteita **Uudet**-, **Myydyimmät**- ja **Suositut**-luetteloissa.</span><span class="sxs-lookup"><span data-stu-id="c90a0-114">**On any store page for browsing or landing page in e-Commerce:** If customers or store associates visit a store page, the recommendation engine can suggest products in the **New**, **Best Selling**, and **Trending** lists.</span></span>
- <span data-ttu-id="c90a0-115">**Tuotetietosivu:** Jos asiakkaat tai myyjät käyvät **tuotetietosivulla**, suositusohjelma ehdottaa lisänimikkeitä, joita saatetaan haluta ostaa.</span><span class="sxs-lookup"><span data-stu-id="c90a0-115">**On the Product details page:** If customers or store associates visit a **Product details** page, the recommendation engine suggests additional items that are also likely to be purchased.</span></span> <span data-ttu-id="c90a0-116">Nämä nimikkeet näkyvät myös **Ihmiset pitävät myös** -luettelossa.</span><span class="sxs-lookup"><span data-stu-id="c90a0-116">These items appear in the **People also like** list.</span></span>
- <span data-ttu-id="c90a0-117">**Tapahtuma-sivu tai Kassasivu** Suositusohjelma ehdottaa nimikkeitä korin kaikkien nimikkeiden luettelon perusteella.</span><span class="sxs-lookup"><span data-stu-id="c90a0-117">**On the Transaction page or the checkout page:** The recommendation engine suggests items, based on the whole list of items in the basket.</span></span> <span data-ttu-id="c90a0-118">Nämä nimikkeet näkyvät **Ostetaan usein yhdessä** -luettelossa.</span><span class="sxs-lookup"><span data-stu-id="c90a0-118">These items appear in the **Frequently bought together** list.</span></span>

## <a name="recommendation-service"></a><span data-ttu-id="c90a0-119">Suosituspalvelu</span><span class="sxs-lookup"><span data-stu-id="c90a0-119">Recommendation service</span></span>

<span data-ttu-id="c90a0-120">Tuotesuositukset käyttävät Suositukset-koneoppimisteknologiaa seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="c90a0-120">Product recommendations use the Recommendations machine learning technologies in the following way:</span></span>

- <span data-ttu-id="c90a0-121">Tiedot muodossa, jota suosituspalvelu vaatii, saadaan Commercen toiminnallisesta tietokannasta. Tiedot lähetetään entiteettimyymälään.</span><span class="sxs-lookup"><span data-stu-id="c90a0-121">Data in the format that the Recommendation service requires is extracted from the Commerce operational database and sent to the Entity store.</span></span>
- <span data-ttu-id="c90a0-122">Suosituspalvelu käyttää tietoja suositusmallien opettamisessa **Ihmiset pitävät myös**-, **Ostetaan usein yhdessä**-, **Uudet**-, **Myydyimmät**- ja **Suositut**-luetteloissa.</span><span class="sxs-lookup"><span data-stu-id="c90a0-122">The Recommendation service uses the data to train recommendation models for the **People also like**, **Frequently bought together**, **New**, **Best selling**, and **Trending** lists.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="c90a0-123">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="c90a0-123">Additional resources</span></span>

[<span data-ttu-id="c90a0-124">Ota tuotesuositukset käyttöön</span><span class="sxs-lookup"><span data-stu-id="c90a0-124">Enable product recommendations</span></span>](enable-product-recommendations.md)

[<span data-ttu-id="c90a0-125">Luo kuratoituja tuotesuositusluetteloita</span><span class="sxs-lookup"><span data-stu-id="c90a0-125">Create curated product recommendation lists</span></span>](create-editorial-recommendation-lists.md)

[<span data-ttu-id="c90a0-126">Hallitse AI-ML-pohjaisia tuotesuositustuloksia</span><span class="sxs-lookup"><span data-stu-id="c90a0-126">Manage AI-ML-based product recommendation results</span></span>](modify-product-recommendation-results.md)

[<span data-ttu-id="c90a0-127">Tuotesuositusluetteloiden lisääminen sivuille</span><span class="sxs-lookup"><span data-stu-id="c90a0-127">Add product recommendation lists to pages</span></span>](add-reco-list-to-page.md)
