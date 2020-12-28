---
title: Uuden tuotteen luominen Commerce-ohjelmassa
description: Tässä ohjeaiheessa käsitellään uuden tuotteen luontia Microsoft Dynamics 365 Commercessa.
author: samjarawan
manager: annbe
ms.date: 01/27/2020
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
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: eb2dd36c6149f2aa40305cd57eac060b232b09e5
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/13/2020
ms.locfileid: "4411929"
---
# <a name="create-a-new-product-in-commerce"></a><span data-ttu-id="b3677-103">Uuden tuotteen luominen Commerce-ohjelmassa</span><span class="sxs-lookup"><span data-stu-id="b3677-103">Create a new product in Commerce</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="b3677-104">Tässä ohjeaiheessa käsitellään uuden tuotteen luontia Microsoft Dynamics 365 Commercessa.</span><span class="sxs-lookup"><span data-stu-id="b3677-104">This topic describes how to create a new product in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="b3677-105">Yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="b3677-105">Overview</span></span>

<span data-ttu-id="b3677-106">Tuote määritetään ensisijaisesti tuotenumeron, nimen ja kuvauksen perusteella.</span><span class="sxs-lookup"><span data-stu-id="b3677-106">A product is primarily defined by a product number, name, and description.</span></span> <span data-ttu-id="b3677-107">Tuotteen tai palvelun kuvaamiseen tarvitaan myös muita tietoja:</span><span class="sxs-lookup"><span data-stu-id="b3677-107">However, other data is also required in order to describe a product or service:</span></span>

## <a name="create-a-new-product"></a><span data-ttu-id="b3677-108">Luo uusi tuote</span><span class="sxs-lookup"><span data-stu-id="b3677-108">Create a new product</span></span>

1. <span data-ttu-id="b3677-109">Siirry selausruudussa kohtaan **Moduulit \> Vähittäismyynti ja kauppa \> Tuotteet ja luokat \> Tuotteet luokittain**.</span><span class="sxs-lookup"><span data-stu-id="b3677-109">In the navigation pane, go to **Modules \> Retail and commerce \> Products and categories \> Products by category**.</span></span>
1. <span data-ttu-id="b3677-110">Valitse toimintoruudussa **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="b3677-110">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="b3677-111">Valitse avattavassa **Tuotetyyppi**-valikossa joko **Nimike** tai **Palvelu**.</span><span class="sxs-lookup"><span data-stu-id="b3677-111">In the **Product type** drop-down list, select either **Item** or **Service**.</span></span>
1. <span data-ttu-id="b3677-112">Valitse avattavasta **Tuotteen alatyyppi** -luettelosta joko **Tuote** (jos tuotteella ei ole variantteja) tai **Päätuote** (jos tuotteella on variantteja).</span><span class="sxs-lookup"><span data-stu-id="b3677-112">In the **Product subtype** drop-down list, select either **Product** (if the product will have no variants) or **Product master** (if the product will have variants).</span></span>
1. <span data-ttu-id="b3677-113">Syötä **Tuotenumero**-ruutuun tuotenumero, jos sellaista ei ole täytetty valmiiksi.</span><span class="sxs-lookup"><span data-stu-id="b3677-113">In the **Product number** box, enter a product number if one is not already prepopulated.</span></span>
1. <span data-ttu-id="b3677-114">Syötä **Tuotenimi** -ruutuun tuotteen nimi.</span><span class="sxs-lookup"><span data-stu-id="b3677-114">In the **Product name** box, enter a product name.</span></span>
1. <span data-ttu-id="b3677-115">Syötä **Hakunimi**-ruutuun hakunimi.</span><span class="sxs-lookup"><span data-stu-id="b3677-115">In the **Search name** box, enter a search name.</span></span>
1. <span data-ttu-id="b3677-116">Valitse avattavassa **Vähittäismyyntiluokka**-luettelosta asianmukainen luokka.</span><span class="sxs-lookup"><span data-stu-id="b3677-116">In the **Retail category** drop-down list, select an appropriate category.</span></span>
1. <span data-ttu-id="b3677-117">Jos tuote on pakkaus, valitse parametrin **Tuotepaketti** arvoksi **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="b3677-117">If the product is a kit, select **Yes** for **Product kit**.</span></span>
1. <span data-ttu-id="b3677-118">Jos tuotteen alatyyppi on päätuote, määritä **Tuotedimensioryhmä** sisältämään tuetut variantit.</span><span class="sxs-lookup"><span data-stu-id="b3677-118">If the product subtype is product master, set the **Product dimension group** to include the supported variants.</span></span> <span data-ttu-id="b3677-119">Vaihtoehtoja ovat **Väri**, **Koko**, **Tyyli** ja **Määritys**.</span><span class="sxs-lookup"><span data-stu-id="b3677-119">Options include **Color**, **Size**, **Style**, and **Configuration**.</span></span> <span data-ttu-id="b3677-120">Tarvittaessa sinun on luotava lisää tuotedimensioryhmiä.</span><span class="sxs-lookup"><span data-stu-id="b3677-120">You may need to create additional product dimension groups if needed.</span></span>
1. <span data-ttu-id="b3677-121">Valitse avattavassa **Määritysteknologia**-luettelosta asianmukainen vaihtoehto.</span><span class="sxs-lookup"><span data-stu-id="b3677-121">In the **Configuration technology** drop-down list, select an appropriate option.</span></span>
1. <span data-ttu-id="b3677-122">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="b3677-122">Select **OK**.</span></span>

<span data-ttu-id="b3677-123">Seuraavassa kuvassa näkyy esimerkkituotteen lisääminen.</span><span class="sxs-lookup"><span data-stu-id="b3677-123">The following image shows an example product being added.</span></span>

![Tuotteen luominen](media/create-new-product.png)

<span data-ttu-id="b3677-125">Kun tuote on lisätty, sille voidaan määrittää lisää tietoja. Näitä ovat esimerkiksi **Tuotekuvaus**, **Varianttiryhmät**, **Dimensioryhmät**, **Tuotemääritteet** ja **Liittyvät tuotteet**.</span><span class="sxs-lookup"><span data-stu-id="b3677-125">Once a product is added, additional data can be set for it, such as **Product description**, **Variant groups**, **Dimension groups**, **Product attributes**, and **Related products**.</span></span>

<span data-ttu-id="b3677-126">Seuraavassa kuvassa esitetään tuotteen lisätiedot.</span><span class="sxs-lookup"><span data-stu-id="b3677-126">The following image shows a product's additional details.</span></span>

![Tuotteen tiedot](media/create-new-product-2.png)

### <a name="create-product-variants"></a><span data-ttu-id="b3677-128">Luo tuotevariantit</span><span class="sxs-lookup"><span data-stu-id="b3677-128">Create product variants</span></span>

<span data-ttu-id="b3677-129">Jos tuotteen alatyyppi on **Päätuote**, on luotava tiettyjä variantteja.</span><span class="sxs-lookup"><span data-stu-id="b3677-129">If the product subtype is **Product master**, specific variants will need to be created.</span></span> 

<span data-ttu-id="b3677-130">Luo tuotevariantteja noudattamalla seuraavia vaiheita.</span><span class="sxs-lookup"><span data-stu-id="b3677-130">To create product variants, follow these steps.</span></span>

1. <span data-ttu-id="b3677-131">Valitse toimintoruudussa **Tuotevariantit**.</span><span class="sxs-lookup"><span data-stu-id="b3677-131">On the action pane, select **Product variants**.</span></span>
1. <span data-ttu-id="b3677-132">Jos toimintoruudussa on valittu varianttiryhmiä, valitse \**varianttiehdotukset*.</span><span class="sxs-lookup"><span data-stu-id="b3677-132">If variant groups have been selected on the action pane, select \**Variant suggestions*.</span></span>
1. <span data-ttu-id="b3677-133">Valitse variantit, joita haluaisit tukea tuotteen osalta.</span><span class="sxs-lookup"><span data-stu-id="b3677-133">Select the variants you would like to support for the product.</span></span>
1. <span data-ttu-id="b3677-134">Valitse **Luo**.</span><span class="sxs-lookup"><span data-stu-id="b3677-134">Select **Create**.</span></span>

## <a name="release-a-product"></a><span data-ttu-id="b3677-135">Tuotteen vapautus</span><span class="sxs-lookup"><span data-stu-id="b3677-135">Release a product</span></span>

<span data-ttu-id="b3677-136">Tuote on ensin vapautettava yritykselle, jotta se voidaan myydä.</span><span class="sxs-lookup"><span data-stu-id="b3677-136">To sell a product it must first be released to a legal entity.</span></span>

1. <span data-ttu-id="b3677-137">Valitse tuotesivulla **Vapauta tuotteita**.</span><span class="sxs-lookup"><span data-stu-id="b3677-137">From the product page, select **Release products**.</span></span>

    ![Tuotteen vapautus](media/create-new-product-3.png)

1. <span data-ttu-id="b3677-139">Valitse vapautettava tuote ja sitten **Seuraava**.</span><span class="sxs-lookup"><span data-stu-id="b3677-139">Select the product to release, and then select **Next**.</span></span>

    ![Vapautettavan tuotteen valitseminen](media/create-new-product-4.png)

1. <span data-ttu-id="b3677-141">Valitse vapautettavien tuotevarianttien joukko ja valitse sitten **Seuraava**.</span><span class="sxs-lookup"><span data-stu-id="b3677-141">Select the set of product variants to release, and then select **Next**.</span></span>

    ![Vapautettavien varianttien valitseminen](media/create-new-product-5.png)

1. <span data-ttu-id="b3677-143">Valitse yritys ja sitten **Seuraava**.</span><span class="sxs-lookup"><span data-stu-id="b3677-143">Select the legal entity, and then select **Next**.</span></span>

    ![Valitse yritys/oikeushenkilö](media/create-new-product-6.png)

1. <span data-ttu-id="b3677-145">Valitse **Valmis**.</span><span class="sxs-lookup"><span data-stu-id="b3677-145">Select **Finish**.</span></span>

    ![Tuotteen vapautuksen viimeistely](media/create-new-product-7.png)

## <a name="configure-a-released-product"></a><span data-ttu-id="b3677-147">Määritä vapautettu tuote</span><span class="sxs-lookup"><span data-stu-id="b3677-147">Configure a released product</span></span>

<span data-ttu-id="b3677-148">Kun tuote on vapautettu, se edellyttää lisämääritystä, johon kuuluu hinnan lisääminen tuotteelle.</span><span class="sxs-lookup"><span data-stu-id="b3677-148">Once a product is released, it will then require further configuration that includes adding a price to the product.</span></span>

1. <span data-ttu-id="b3677-149">Siirry siirtymisruudussa kohtaan **Moduulit \> Vähittäiskauppa ja kauppa \> Tuotteet ja luokat \> Vapautetut tuotteet luokan mukaan**.</span><span class="sxs-lookup"><span data-stu-id="b3677-149">In the navigation pane, go to **Modules \> Retail and commerce \> Products and categories \> Released products by category**.</span></span>
1. <span data-ttu-id="b3677-150">Valitse vapautetulle tuotteelle tuoteluokkasolmu ja valitse sitten tuote tuoteluettelosta.</span><span class="sxs-lookup"><span data-stu-id="b3677-150">Select the product category node for the product that was released, and then select the product from the product list.</span></span>
1. <span data-ttu-id="b3677-151">Valitse toimintoruudussa **Muokkaa**.</span><span class="sxs-lookup"><span data-stu-id="b3677-151">On the action pane, select **Edit**.</span></span>
1. <span data-ttu-id="b3677-152">Määritä **Hankinta**-osassa tarvittavat ominaisuudet, kuten **Yksikkö**, **Hinta** ja **Määrä**.</span><span class="sxs-lookup"><span data-stu-id="b3677-152">In the **Purchase** section, configure any required properties including **Unit**, **Price**,  and **Quantity**.</span></span>
1. <span data-ttu-id="b3677-153">Valitse toimintoruudussa **Vahvista** sen varmistamiseksi, ettei puuttuvien kenttien osalta anneta virheilmoituksia.</span><span class="sxs-lookup"><span data-stu-id="b3677-153">On the action pane, select **Validate** to ensure that no errors are reported for missing fields.</span></span>
1. <span data-ttu-id="b3677-154">Valitse toimintoruudussa **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="b3677-154">On the action pane, select **Save**.</span></span>

<span data-ttu-id="b3677-155">Seuraavassa kuvassa on esimerkki vapautetun tuotteen asetusten määrityksistä.</span><span class="sxs-lookup"><span data-stu-id="b3677-155">The following image shows an example configuration for a released product.</span></span>

![Vapautetun tuotteen määritys](media/create-new-product-8.png)

## <a name="additional-resources"></a><span data-ttu-id="b3677-157">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="b3677-157">Additional resources</span></span>

[<span data-ttu-id="b3677-158">Yritysten luominen</span><span class="sxs-lookup"><span data-stu-id="b3677-158">Create legal entities</span></span>](channels-legal-entities.md)

[<span data-ttu-id="b3677-159">Luo varianttiryhmä</span><span class="sxs-lookup"><span data-stu-id="b3677-159">Create a variant group</span></span>](create-variant-group.md) 
