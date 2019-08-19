---
title: Resurssien tuoterakenteet
description: Tässä ohjeaiheessa kuvataan resurssin tuoterakenteita resurssien hallinnassa.
author: josaw1
manager: AnnBe
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 761364c8c58258baf2268f917cb174ac300c4528
ms.sourcegitcommit: 747bcd25ce7c6c20ce9eaa0027e730f74d4fd6aa
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 07/23/2019
ms.locfileid: "1783248"
---
# <a name="asset-boms"></a><span data-ttu-id="668a2-103">Resurssien tuoterakenteet</span><span class="sxs-lookup"><span data-stu-id="668a2-103">Asset BOMs</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="668a2-104">Tässä ohjeaiheessa kuvataan resurssin tuoterakenteita resurssien hallinnassa.</span><span class="sxs-lookup"><span data-stu-id="668a2-104">This topic describes asset bills of materials (BOMs) in Asset Management.</span></span> <span data-ttu-id="668a2-105">**Resurssin tuoterakenne** -sivulla näkyy luettelo kaikista nimikkeistä (varaosista ja muista nimikkeistä), joita resurssin koko käyttöiän aikana käytetään.</span><span class="sxs-lookup"><span data-stu-id="668a2-105">The **Asset BOM** page shows a list of all items (spare parts and other items) that are used on an asset during its whole lifetime.</span></span> <span data-ttu-id="668a2-106">Kun luot uuden resurssin, sinun kannattaa harkita resurssin tuoterakenteen määrittämistä osana asetusmenettelyä.</span><span class="sxs-lookup"><span data-stu-id="668a2-106">When you create a new asset, you should consider setting up an asset BOM as a part of the setup procedure.</span></span> <span data-ttu-id="668a2-107">Tällä tavoin voit seurata resurssin nimikehistoriaa luontipäivästä lähtien.</span><span class="sxs-lookup"><span data-stu-id="668a2-107">In this way, you can track item history for the asset from the creation date.</span></span>

<span data-ttu-id="668a2-108">Kun kunnossapitotyö on suoritettu ja nimikekulutus on rekisteröity työtilaukseen, voit seurata varaosien ja muiden resurssin käyttämien nimikkeiden kulutusta.</span><span class="sxs-lookup"><span data-stu-id="668a2-108">After you've completed a maintenance job, and item consumption has been registered on a work order, you can track consumption of spare parts and other items that are used on the asset.</span></span> <span data-ttu-id="668a2-109">Tämän toiminnon avulla voit säilyttää täydellisen nimikekulutustietueen kaikille resursseille.</span><span class="sxs-lookup"><span data-stu-id="668a2-109">This functionality lets you keep a complete item consumption record for all your assets.</span></span> <span data-ttu-id="668a2-110">Voit käyttää tietuetta esimerkiksi valvomaan, onko tietty varaosa usein korvattu, tai seurata varaosia tai muita nimikkeitä, joita käytetään tällä hetkellä käyttö resurssissa.</span><span class="sxs-lookup"><span data-stu-id="668a2-110">For example, you can use the record to monitor whether a specific spare part is often replaced, or to keep track of the spare parts or other items that are currently used on an asset.</span></span>

> [!NOTE]
> <span data-ttu-id="668a2-111">Työtilauksessa nimikkeen kulutus voi sisältää sekä varaosia että muita nimikkeitä, kuten voiteluaineita, pultteja ja tiivisteitä.</span><span class="sxs-lookup"><span data-stu-id="668a2-111">On a work order, item consumption might include both spare parts and other, additional items, such as lubricants, bolts, and gaskets.</span></span>

<span data-ttu-id="668a2-112">Resurssin tuoterakenne voidaan päivittää automaattisesti resurssien hallinnan asetusten perusteella.</span><span class="sxs-lookup"><span data-stu-id="668a2-112">An asset BOM can be automatically updated based on the setup in Asset Management.</span></span> <span data-ttu-id="668a2-113">Jos työtilauksen elinkaaren tila on luotu käsittelemään suoritettuja tai valmiita työtilauksia ja jos **Päivitä resurssin tuoterakenne** -vaihtoehto kyseiselle työtilauksen elinkaaritilalle on **Kyllä** **Työtilauksen elinkaaren tilat** -sivulla, kaikki työtilauksessa käytettävät nimikkeet päivitetään automaattisesti **Resurssin tuoterakenne** -sivulla, kun työtilaus päivitetään kyseiseen elinkaaren tilaan.</span><span class="sxs-lookup"><span data-stu-id="668a2-113">If a work order lifecycle state has been created to handle finished or completed work orders, and if the **Update asset BOM** option for that work order lifecycle state is set to **Yes** on the **Work order lifecycle states** page, all items that are used on the work order will be automatically updated on the **Asset BOM** page when the work order is updated to that lifecycle state.</span></span> 


<span data-ttu-id="668a2-114">Voit myös päivittää resurssin tuoterakenteen manuaalisesti luomalla uusia nimikerivejä **Resurssin tuoterakenne** -sivulla.</span><span class="sxs-lookup"><span data-stu-id="668a2-114">You can also manually update an asset BOM by creating new item lines on the **Asset BOM** page.</span></span>

<span data-ttu-id="668a2-115">**Resurssin tuoterakenne** -sivulla voit seurata resurssien varaosahistoriaa sen jälkeen, kun nimikekulutus on rekisteröity työtilaukseen.</span><span class="sxs-lookup"><span data-stu-id="668a2-115">On the **Asset BOM** page, you can track spare parts history for assets after item consumption is registered on a work order.</span></span> <span data-ttu-id="668a2-116">Jotta voit käyttää tätä toimintoa, sinun on valittava nimikeryhmät, joita käytetään varaosien rekisteröintiin **Varaosien nimikeryhmät** -sivulla.</span><span class="sxs-lookup"><span data-stu-id="668a2-116">To use this functionality, you must select the item groups that should be used for spare parts registration on the **Spare parts item groups** page.</span></span>

<span data-ttu-id="668a2-117">Jotta voit käyttää resurssin tuoterakenteen toiminnallisuutta, sinun on ensin määritettävä tarvittavat varaosien nimikeryhmät.</span><span class="sxs-lookup"><span data-stu-id="668a2-117">To use asset BOM functionality, you must first set up the required spare parts items groups.</span></span> <span data-ttu-id="668a2-118">Jos sitten haluat, että resurssin tuoterakenne päivitetään automaattisesti, kun työtilaus on valmis, voit määrittää työtilauksen elinkaaritilan käsittelemään kyseistä päivitystä.</span><span class="sxs-lookup"><span data-stu-id="668a2-118">Then, if you want the asset BOM to be automatically updated when a work order is completed, you can set up a work order lifecycle state to handle that update.</span></span> 


## <a name="set-up-spare-parts-item-groups"></a><span data-ttu-id="668a2-119">Määritä varaosien nimikeryhmät</span><span class="sxs-lookup"><span data-stu-id="668a2-119">Set up spare parts item groups</span></span>

<span data-ttu-id="668a2-120">Varaosien historian asetukset perustuvat nimikeryhmiin, jotka on luotu **Varastonhallinta** -moduulissa.</span><span class="sxs-lookup"><span data-stu-id="668a2-120">The setup of spare parts history is based on item groups that are created in the **Inventory and warehouse management** module.</span></span> <span data-ttu-id="668a2-121">Resurssien hallinnassa määritetään nimikeryhmät, jotta voit seurata valittujen nimikeryhmien nimikkeiden varaosahistoriaa.</span><span class="sxs-lookup"><span data-stu-id="668a2-121">In Asset Management, you set up item groups so that you can track spare parts history for the items in the selected item groups.</span></span>

1. <span data-ttu-id="668a2-122">Valitse **resurssien hallinta** \> **Asetukset** \> **resurssi** \> **Varaosien nimikeryhmät**.</span><span class="sxs-lookup"><span data-stu-id="668a2-122">Select **Asset management** \> **Setup** \> **Asset** \> **Spare parts item groups**.</span></span>
2. <span data-ttu-id="668a2-123">Määritä nimikeryhmä valitsemalla **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="668a2-123">Select **New** to set up an item group.</span></span>
3. <span data-ttu-id="668a2-124">Valitse **Nimikeryhmä**-kentässä ryhmä.</span><span class="sxs-lookup"><span data-stu-id="668a2-124">In the **Item group** field, select the group.</span></span> <span data-ttu-id="668a2-125">Ryhmän nimi tulee automaattisesti **Nimi**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="668a2-125">The name of the group is automatically entered in the **Name** field.</span></span>

## <a name="view-and-update-asset-boms"></a><span data-ttu-id="668a2-126">Tarkastele ja päivitä resurssien tuoterakenteita</span><span class="sxs-lookup"><span data-stu-id="668a2-126">View and update asset BOMs</span></span>

<span data-ttu-id="668a2-127">Kun olet kirjannut nimikekulutuksen työtilaukseen, voit tarkastella rekisteröityjen nimikkeiden kulutusta **resurssin tuoterakenne** -sivulla.</span><span class="sxs-lookup"><span data-stu-id="668a2-127">After you post item consumption on a work order, you can view the registered item consumption on the **Asset BOM** page.</span></span>

1. <span data-ttu-id="668a2-128">Valitse **Resurssien hallinta** \> **Yhteiset** \> **Resurssit** \> **Aktiiviset resurssit**.</span><span class="sxs-lookup"><span data-stu-id="668a2-128">Select **Asset management** \> **Common** \> **Assets** \> **Active assets**.</span></span> <span data-ttu-id="668a2-129">Valitse resurssiluettelosta resurssi ja valitse sitten **Resurssin tuoterakenne**.</span><span class="sxs-lookup"><span data-stu-id="668a2-129">Select the asset in the list, and then select **Asset BOM**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="668a2-130">Voit tarkastella kaikkien resurssien kaikkien nimikkeiden kulutuksen rekisteröintejä valitsemalla **Resurssien hallinta** \> **Kyselyt** \> **Resurssit** \> **Resurssin tuoterakenne**.</span><span class="sxs-lookup"><span data-stu-id="668a2-130">To view all item consumption registrations on all assets, select **Asset management** \> **Inquiries** \> **Assets** \> **Asset BOM**.</span></span>

2. <span data-ttu-id="668a2-131">Valitse **Päivitä resurssin tuoterakenne**.</span><span class="sxs-lookup"><span data-stu-id="668a2-131">Select **Update asset BOM**.</span></span> <span data-ttu-id="668a2-132">Voit lisätä päivitykseen resursseja, resurssityyppejä ja resursseja valitsemalla **Valitse**.</span><span class="sxs-lookup"><span data-stu-id="668a2-132">You can add assets, asset types, and resources to the update as you require by selecting **Select**.</span></span> <span data-ttu-id="668a2-133">Aloita päivitys valitsemalla **OK**.</span><span class="sxs-lookup"><span data-stu-id="668a2-133">Select **OK** to start the update.</span></span> <span data-ttu-id="668a2-134">Voit myös määrittää Päivitä-funktion erätyöksi.</span><span class="sxs-lookup"><span data-stu-id="668a2-134">You can also set up the Update function as a batch job.</span></span>
3. <span data-ttu-id="668a2-135">Jos haluat nähdä lisätietoja, jotka liittyvät nimikkeisiin, voit lisätä varastodimensioita.</span><span class="sxs-lookup"><span data-stu-id="668a2-135">If you want to see more information that is related to the items, you can add inventory dimensions.</span></span> <span data-ttu-id="668a2-136">Valitse **Varasto** \> **Dimensionäyttö** ja valitse sitten niiden dimensioiden valintaruudut, jotka haluat nähdä.</span><span class="sxs-lookup"><span data-stu-id="668a2-136">Select **Inventory** \> **Dimensions display**, and then select the check boxes for the dimensions that you want to see.</span></span> <span data-ttu-id="668a2-137">Jos haluat säilyttää tämän määrityksen kaikille **Resurssin tuoterakenne** -sivun resursseille, määritä **Tallenna asetukset** -asetukseksi **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="668a2-137">To keep this setup for all assets on the **Asset BOM** page, set the **Save setup** option to **Yes**.</span></span>
4. <span data-ttu-id="668a2-138">Saat yleiskatsauksen siitä, missä resurssien hallinnassa valitulla rivillä olevaa nimikettä käytetään suhteessa resursseihin, työtyypin oletuksiin, varaosiin ja työtilauksiin, valitse **Nimike, missä käytetty**.</span><span class="sxs-lookup"><span data-stu-id="668a2-138">To get an overview of where in Asset Management the item on the selected line is used, in relation to assets, job type defaults, spare parts, and work orders, select **Item where used**.</span></span> 
5. <span data-ttu-id="668a2-139">Jos haluat nähdä vain aktiiviset nimikerivit, valitse **Näytä** \> **Nykyinen**.</span><span class="sxs-lookup"><span data-stu-id="668a2-139">If you want to see only active item lines, select **View** \> **Current**.</span></span> <span data-ttu-id="668a2-140">Jos haluat nähdä kaikki nimikerivit, mukaan lukien rivit, joiden vanhentumispäivämäärä on aikaisempi kuin nykyinen päivämäärä, valitse **Näytä** \> **Kaikki**.</span><span class="sxs-lookup"><span data-stu-id="668a2-140">To see all item lines, including lines where the expiration date is earlier than the current date, select **View** \> **All**.</span></span>

> [!NOTE]
> <span data-ttu-id="668a2-141">Kun olet suorittanut työtilauksen, jos jotkin kyseiseen resurssiin liittyvät nimikkeet tai varaosat ovat vanhentuneet tai ne on korvattu muilla nimikkeillä tai varaosilla, on suositeltavaa päivittää resurssin tuoterakenne vastaavasti.</span><span class="sxs-lookup"><span data-stu-id="668a2-141">When you've completed a work order, if some items or spare parts that are related to the related asset have expired or have been replaced by other items or spare parts, we recommend that you update the asset BOM accordingly.</span></span>

## <a name="create-a-new-item-line-in-an-asset-bom"></a><span data-ttu-id="668a2-142">Uuden nimikerivin luominen resurssin tuoterakenteeseen</span><span class="sxs-lookup"><span data-stu-id="668a2-142">Create a new item line in an asset BOM</span></span>

<span data-ttu-id="668a2-143">Voit luoda nimikerivejä manuaalisesti resursseille.</span><span class="sxs-lookup"><span data-stu-id="668a2-143">You can manually create item lines for assets.</span></span>

1. <span data-ttu-id="668a2-144">Valitse **Resurssin tuoterakenne** -sivulla **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="668a2-144">On the **Asset BOM** page, select **New**.</span></span>
2. <span data-ttu-id="668a2-145">Valitse **Resurssi**-kentässä resurssi, jolle nimikerivi lisätään.</span><span class="sxs-lookup"><span data-stu-id="668a2-145">In the **Asset** field, select the asset to add an item line for.</span></span>
3. <span data-ttu-id="668a2-146">Syötä luku **Rivinumero**-kenttään rivin järjestysnumero.</span><span class="sxs-lookup"><span data-stu-id="668a2-146">In the **Line number** field, enter a sequential line number.</span></span>
4. <span data-ttu-id="668a2-147">Valitse **Voimassa**-kentässä nimikkeen alkamispäivä.</span><span class="sxs-lookup"><span data-stu-id="668a2-147">In the **Effective** field, enter a start date for the item.</span></span>
5. <span data-ttu-id="668a2-148">Jos nimike vanhenee, kirjoita päättymispäivä **Vanheneminen**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="668a2-148">If the item will expire, in the **Expiration** field, enter an end date.</span></span>
6. <span data-ttu-id="668a2-149">Valitse **Nimiketunnus**-kentässä nimike.</span><span class="sxs-lookup"><span data-stu-id="668a2-149">In the **Item number** field, select the item.</span></span> <span data-ttu-id="668a2-150">Nimi tulee automaattisesti **Tuotteen nimi** -kenttään.</span><span class="sxs-lookup"><span data-stu-id="668a2-150">The name is automatically entered in the **Product name** field.</span></span>
7. <span data-ttu-id="668a2-151">Anna käytetty määrä **Määrä**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="668a2-151">In the **Quantity** field, enter the quantity that is used.</span></span> <span data-ttu-id="668a2-152">**Yksikkö**-kenttä päivittyy automaattisesti.</span><span class="sxs-lookup"><span data-stu-id="668a2-152">The **Unit** field is automatically updated.</span></span>
