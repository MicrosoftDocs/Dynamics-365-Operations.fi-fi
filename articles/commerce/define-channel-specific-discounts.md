---
title: Kanavakohtaisten alennusten määrittäminen
description: Vähittäismyyjät määrittävät usein erilaisia alennuksia eri kanaville. Tässä aiheessa tarkastellaan käsitteitä, joita tarvitaan tietyn kanavan alennuksen luomisessa.
author: scott-tucker
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailAffiliationPriceGroup, RetailCatalogPriceGroup, RetailChannelPriceGroup, RetailDiscountPriceGroup, RetailDiscountPricingWorkspace, RetailPeriodicDiscount, RetailStoreItemPriceList, RetailStoreTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 16401
ms.assetid: d807fd51-86aa-47a0-8e00-6c5ddd21ff6b
ms.search.region: global
ms.search.industry: Retail
ms.author: scotttuc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 539a6f2df46450c5e0fd18ba69501432d6f3fbdd
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/13/2020
ms.locfileid: "4411981"
---
# <a name="define-channel-specific-discounts"></a><span data-ttu-id="67740-104">Kanavakohtaisten alennusten määrittäminen</span><span class="sxs-lookup"><span data-stu-id="67740-104">Define channel-specific discounts</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="67740-105">Tässä aiheessa tarkastellaan käsitteitä, joita tarvitaan tietyn kanavan alennuksen luomisessa.</span><span class="sxs-lookup"><span data-stu-id="67740-105">This topic reviews the concepts you need to know to create a discount for a specific channel.</span></span>

## <a name="channel-specific-discounts"></a><span data-ttu-id="67740-106">Kanavakohtaiset alennukset</span><span class="sxs-lookup"><span data-stu-id="67740-106">Channel-specific discounts</span></span>

<span data-ttu-id="67740-107">Vähittäismyyjät tarjoavat usein erilaisia alennuksia eri kanaville.</span><span class="sxs-lookup"><span data-stu-id="67740-107">Retailers often offer different discounts in different channels.</span></span> <span data-ttu-id="67740-108">Syynä voi olla paikallisten markkinaolosuhteiden huomioon ottaminen tai kilpailu muiden vähittäismyyjien kanssa.</span><span class="sxs-lookup"><span data-stu-id="67740-108">This may be done to address local market conditions or to deal with competing retailers.</span></span>

<span data-ttu-id="67740-109">Commerce määrittää kanavakohtaiset alennukset hintaryhmien avulla.</span><span class="sxs-lookup"><span data-stu-id="67740-109">Commerce uses price groups to define channel-specific discounts.</span></span> <span data-ttu-id="67740-110">Hintaryhmät voivat määrittää yhteen seuraavista yksiköistä tai useisiin yksikköihin: kanavat. luettelot, liitokset ja kanta-asiakasohjelmat.</span><span class="sxs-lookup"><span data-stu-id="67740-110">Price groups can be assigned to one or more of the following entities: channels, catalogs, affiliations, and loyalty programs.</span></span> <span data-ttu-id="67740-111">Tässä artikkelissa käsitellään kanavia, mutta samat käsitteet koskevat myös luettelo-, liitos- ja kanta-asiakasalennuksia.</span><span class="sxs-lookup"><span data-stu-id="67740-111">This article discusses channels, but the same concepts apply to catalog discounts, affiliations discounts, and loyalty discounts.</span></span>

## <a name="price-groups"></a><span data-ttu-id="67740-112">Hintaryhmät</span><span class="sxs-lookup"><span data-stu-id="67740-112">Price groups</span></span>

<span data-ttu-id="67740-113">[![Hintaryhmät](./media/price-groups-1024x608.png)](./media/price-groups.png)</span><span class="sxs-lookup"><span data-stu-id="67740-113">[![Price groups](./media/price-groups-1024x608.png)](./media/price-groups.png)</span></span>

<span data-ttu-id="67740-114">Edellä olevassa kaaviossa on kuva tapahtumassa mahdollisesti olevien yksikköjen suhteesta (kanava, luettelo, liitos, asiakas, kanta-asiakaskortti) ja erilaisista määritettävistä alennustyypeistä.</span><span class="sxs-lookup"><span data-stu-id="67740-114">The diagram above illustrates the relationship between entities that may be on a transaction (channel, catalog, affiliation, customer, loyalty card) and the various discount types that can be configured.</span></span> <span data-ttu-id="67740-115">Kaikki tapahtumat tapahtuvat kanavassa, joten kanava on varmasti mukana tapahtumassa.</span><span class="sxs-lookup"><span data-stu-id="67740-115">All transactions occur in a channel, so the channel is guaranteed to be present on a transaction.</span></span> <span data-ttu-id="67740-116">Muut yksiköt ovat valinnaisia.</span><span class="sxs-lookup"><span data-stu-id="67740-116">The remaining entities are optional.</span></span> <span data-ttu-id="67740-117">Jokaisella päätietosivulla on linkki liittyvään hintaryhmäsivuun, jossa voit tarkastella hintaryhmiä ja lisätä niitä tarvittaessa.</span><span class="sxs-lookup"><span data-stu-id="67740-117">On each master data pages there is a link to a related price groups page where you can view and add price groups as needed.</span></span> <span data-ttu-id="67740-118">Hintaryhmän avulla neljä eri tyyppistä yksikköä liitetään alennuksiin, hinnanoikaisuihin ja kauppasopimuksiin.</span><span class="sxs-lookup"><span data-stu-id="67740-118">A price group is used to relate four different types of entities to discounts, price adjustments, and trade agreements.</span></span> <span data-ttu-id="67740-119">On suositeltavaa, että suunnittelet hintaryhmille nimeämisstrategian, jotta ne pysyvät järjestyksessä.</span><span class="sxs-lookup"><span data-stu-id="67740-119">We recommend that you plan a strategy for how you will name your price groups to keep them organized.</span></span> <span data-ttu-id="67740-120">Tyypit voi erottaa toisistaan käyttämällä etu- tai jälkiliitteenä kirjainta tai numeroa.</span><span class="sxs-lookup"><span data-stu-id="67740-120">One option would be to use a letter or number prefix or suffix to distinguish between the different types.</span></span> <span data-ttu-id="67740-121">Esimerkiksi 1-xxxxx voi viitata kanavan hintaryhmään ja 2-xxxxx luettelon hintaryhmään.</span><span class="sxs-lookup"><span data-stu-id="67740-121">For example, 1-xxxxx for channel price groups and 2-xxxxx for catalog price groups.</span></span> <span data-ttu-id="67740-122">Kullakin kaupankäynnin myyntiyksiköllä, joihin voidaan liittää alennuksia, on neljä kyselysivua.</span><span class="sxs-lookup"><span data-stu-id="67740-122">There are four inquiry pages that focus on each of the commerce entities that can have discounts associated to them.</span></span>

- <span data-ttu-id="67740-123">**Kanavan hintaryhmät** – Tällä sivulla on luettelo kanavista ja alennuksista, jotka on liitetty yhteen kullekin hintaryhmälle.</span><span class="sxs-lookup"><span data-stu-id="67740-123">**Channel channel price groups** – This page shows a list of channels and discounts linked together for each price group.</span></span>
- <span data-ttu-id="67740-124">**Luettelon hintaryhmät** – tällä sivulla on luettelo luetteloista ja alennuksista, jotka on liitetty yhteen kullekin hintaryhmälle.</span><span class="sxs-lookup"><span data-stu-id="67740-124">**Catalog price groups** – This page shows a list of catalogs and discounts linked together for each price group.</span></span>
- <span data-ttu-id="67740-125">**Kanta-asiakasohjelman hintaryhmät** – tällä sivulla on luettelo kanta-asiakasohjelmista ja alennuksista, jotka on liitetty yhteen kullekin hintaryhmälle.</span><span class="sxs-lookup"><span data-stu-id="67740-125">**Loyalty price groups** – This page shows a list of loyalty programs and discounts linked together for each price group.</span></span>
- <span data-ttu-id="67740-126">**Liitoksen hintaryhmät** – tällä sivulla on luettelo liitoksista ja alennuksista, jotka on liitetty yhteen kullekin hintaryhmälle.</span><span class="sxs-lookup"><span data-stu-id="67740-126">**Affiliation price groups** – This page shows a list of affiliations and discounts linked together for each price group.</span></span>

## <a name="example-channel-discount-set-up"></a><span data-ttu-id="67740-127">Kanavan alennusasetusten esimerkki</span><span class="sxs-lookup"><span data-stu-id="67740-127">Example channel discount set up</span></span>

<span data-ttu-id="67740-128">Seuraavassa esimerkissä käsitellään tehtäviä, jotka liittyvät kanava-alennuksen määrittämiseen.</span><span class="sxs-lookup"><span data-stu-id="67740-128">The following example illustrates the tasks involved in setting up a channel discount.</span></span>

1. <span data-ttu-id="67740-129">Tässä esimerkissä on **Houston**-niminen kanava ja luot uuden alennuksen, jonka nimi on **Takaisin kouluun**.</span><span class="sxs-lookup"><span data-stu-id="67740-129">For this example, you have a channel called **Houston**, and you're going to create a new discount called **Back-to-School**.</span></span>
2. <span data-ttu-id="67740-130">Koska hinnoittelu- ja alennusstrategia mahdollistaa kanava-alennukset, kanavaa luotaessa luodaan aina myös kanavakohtainen hintaryhmä.</span><span class="sxs-lookup"><span data-stu-id="67740-130">Because the pricing and discount strategy includes the possibility of channel discounts, you always create a channel-specific price group when you create a channel.</span></span>
3. <span data-ttu-id="67740-131">Sinulla hintaryhmä **Houston-PG**, joka on määritetty **Houston**-kanavaan.</span><span class="sxs-lookup"><span data-stu-id="67740-131">You have the price group **Houston-PG** and it is assigned to the **Houston** channel.</span></span>
4. <span data-ttu-id="67740-132">Kun olet luonut uuden **Takaisin kouluun** -alennukset, valitse **Hintaryhmät** **Alennus**-sivun yläosassa.</span><span class="sxs-lookup"><span data-stu-id="67740-132">After you create the new **Back-to-School** discount, you need to click **Price groups** on the top of the **Discount** page.</span></span> <span data-ttu-id="67740-133">**Alennushintaryhmät**-sivu avautuu.</span><span class="sxs-lookup"><span data-stu-id="67740-133">The **Discount price groups** page will open.</span></span> <span data-ttu-id="67740-134">Valitse seuraavaksi ensin **Uusi** ja sitten **Houston-PG**-hintaryhmä.</span><span class="sxs-lookup"><span data-stu-id="67740-134">Next, click **New** and select the **Houston-PG** price group.</span></span>
5. <span data-ttu-id="67740-135">Voit nyt ottaa alennuksen käyttöön ja siirtää sen kanavaan.</span><span class="sxs-lookup"><span data-stu-id="67740-135">Now you can enable the discount and push it to the channel.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="67740-136">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="67740-136">Additional resources</span></span>

[<span data-ttu-id="67740-137">Hinnanoikaisut ja alennukset</span><span class="sxs-lookup"><span data-stu-id="67740-137">Price adjustments and discounts</span></span>](price-adjustments-discounts.md)
