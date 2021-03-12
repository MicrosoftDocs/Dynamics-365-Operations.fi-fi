---
title: Varastotapahtumien tuotesuodattimien määrittäminen
description: Tässä aiheessa käsitellään tuotesuodattimien ja suodatinkoodien määrittämistä luokittelemaan varastonimikkeitä varastossa. Suodattimilla voidaan myös määrittää asiakkaat, jotka voivat tilata tietyn nimikkeen, ja määrittää nimikkeet, joita voidaan ostaa tietyltä toimittajalta.
author: Mirzaab
manager: tfehr
ms.date: 01/04/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSFilters,WHSFilterGroupTable,EcoResProductDetailsExtended,WHSFilterGenerallyAvail
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2021-01-04
ms.dyn365.ops.version: Release 10.0.16
ms.openlocfilehash: 922ff818e069f41c139cc00db9161dc6e113888b
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/15/2021
ms.locfileid: "4973732"
---
# <a name="configure-product-filters-for-warehouse-transactions"></a><span data-ttu-id="06c79-104">Varastotapahtumien tuotesuodattimien määrittäminen</span><span class="sxs-lookup"><span data-stu-id="06c79-104">Configure product filters for warehouse transactions</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="06c79-105">Tässä aiheessa käsitellään tuotesuodattimien ja suodatinkoodien määrittämistä luokittelemaan varastonimikkeitä varastossa.</span><span class="sxs-lookup"><span data-stu-id="06c79-105">This topic describes how to configure product filters and filter codes to categorize inventory items in a warehouse.</span></span> <span data-ttu-id="06c79-106">Suodattimilla voidaan myös määrittää asiakkaat, jotka voivat tilata tietyn nimikkeen, ja määrittää nimikkeet, joita voidaan ostaa tietyltä toimittajalta.</span><span class="sxs-lookup"><span data-stu-id="06c79-106">You can also use filters to specify which customers can order a particular item and which items can be purchased from a particular vendor.</span></span>

<span data-ttu-id="06c79-107">Lisäksi voidaan määrittää ja käyttää tuotesuodattimia varastonimikkeiden automaattiseen järjestämiseen ja suodatettujen nimikkeiden yhdistämiseen suodatusryhmiksi.</span><span class="sxs-lookup"><span data-stu-id="06c79-107">Additionally, you can set up and use product filters to automatically organize inventory items in a warehouse and combine filtered items into filter groups.</span></span> <span data-ttu-id="06c79-108">Suodattimien avulla nimikkeitä voidaan sijoittaa luokkiin käsittely-, osto- ja myyntiprosesseja varten.</span><span class="sxs-lookup"><span data-stu-id="06c79-108">Filters can be used to put items into categories for handling, purchasing, and selling processes.</span></span> <span data-ttu-id="06c79-109">Nimikkeitä halutaan ehkä ryhmitellä tai erottaa toisistaan silloin, kun niiden käsittelytapa perustuu painoon tai käsittelyrajoituksiin.</span><span class="sxs-lookup"><span data-stu-id="06c79-109">You might want to group items together or separate them from each other when the way that they are handled is based on weight or handling restrictions.</span></span> <span data-ttu-id="06c79-110">Lisäksi voidaan määrittää asiakkaat tai toimittajat, joille nimike voidaan myydä tai joilta se voidaan ostaa.</span><span class="sxs-lookup"><span data-stu-id="06c79-110">You can also specify which customers or vendors an item can be purchased from or sold to.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="06c79-111">Edellytykset</span><span class="sxs-lookup"><span data-stu-id="06c79-111">Prerequisites</span></span>

<span data-ttu-id="06c79-112">Seuraavassa taulukossa esitellään edellytykset, joiden on täytyttävä ennen aloittamista.</span><span class="sxs-lookup"><span data-stu-id="06c79-112">The following table shows the prerequisites that must be in place before you start.</span></span>

| <span data-ttu-id="06c79-113">Edellytys</span><span class="sxs-lookup"><span data-stu-id="06c79-113">Prerequisite</span></span> | <span data-ttu-id="06c79-114">Ohjeet</span><span class="sxs-lookup"><span data-stu-id="06c79-114">Instructions</span></span> |
|---|---|
| <span data-ttu-id="06c79-115">Varastokäsittely on otettava käyttöön tuotteen varastodimensioryhmässä, ennen kuin tuotteiden määrittäminen **Vapautetun tuotteen tiedot** -sivulla voidaan aloittaa.</span><span class="sxs-lookup"><span data-stu-id="06c79-115">Before you start to configure products on the **Released product details** page, you must turn on warehouse processing for the product's storage dimension group.</span></span> | <span data-ttu-id="06c79-116">Valitse **Tuotetietojen hallinta \> Asetukset \> Dimensio- ja varianttiryhmät \> Varastodimensioryhmät**. Valitse tai luo sitten varastodimensioryhmä, jossa **Käytä varastonhallintaprosesseja** -asetukseksi on määritetty *Kyllä*.</span><span class="sxs-lookup"><span data-stu-id="06c79-116">Go to **Product information management \> Setup \> Dimension and variant groups \> Storage dimension groups**, and select or create a storage dimension group where the **Use warehouse management processes** option is set to *Yes*.</span></span> |
| <span data-ttu-id="06c79-117">Jos käytössä on asiakkaan suodattamia ja/tai toimittajan suodattimia, ne on otettava käyttöön varastonhallinnan parametreissa.</span><span class="sxs-lookup"><span data-stu-id="06c79-117">If you will use customer filters and/or vendor filters, you must enable their use in Warehouse management parameters.</span></span> | <span data-ttu-id="06c79-118">Siirry kohtaan **Varastonhallinta \> Asetukset \> Varastonhallinnan parametrit**.</span><span class="sxs-lookup"><span data-stu-id="06c79-118">Go to **Warehouse management \> Setup \> Warehouse management parameters**.</span></span> <span data-ttu-id="06c79-119">Määritä **Tuotesuodattimet**-välilehdessä **Ota asiakkaan suodattimet käyttöön**- ja/tai **Ota toimittajan suodattimet käyttöön** -asetukseksi *Kyllä*.</span><span class="sxs-lookup"><span data-stu-id="06c79-119">On the **Product filters** tab, set the **Enable customer filters** and/or **Enable vendor filters** option  to *Yes*.</span></span> |

## <a name="set-up-product-filters"></a><span data-ttu-id="06c79-120">Tuotesuodattimien määrittäminen</span><span class="sxs-lookup"><span data-stu-id="06c79-120">Set up product filters</span></span>

<span data-ttu-id="06c79-121">Tuotesuodattimessa voi olla enintään 10 **Suodattimen otsikko** -ominaisuutta, jotka ovat luetteloinnin (valintalistan) arvoja.</span><span class="sxs-lookup"><span data-stu-id="06c79-121">Product filters provide up to 10 **Filter title** characteristics, which are enumeration (enum) values.</span></span> <span data-ttu-id="06c79-122">Valintalistan arvot ovat valittavissa, kun tuotesuodatin luodaan.</span><span class="sxs-lookup"><span data-stu-id="06c79-122">These enum values are available for selection when you create a product filter.</span></span> <span data-ttu-id="06c79-123">Valintalistan arvot *Koodi 1*–*Koodi 10* ovat järjestelmän määrittämiä arvoja, ja ne ilmaisevat nimikkeen erikoisominaisuuden tai määritteen.</span><span class="sxs-lookup"><span data-stu-id="06c79-123">The enum values *Code 1* through *Code 10* are system-defined and represent a specific characteristic or attribute of an item.</span></span> <span data-ttu-id="06c79-124">*Koodi 1* voi esimerkiksi ilmaista nimikkeet, jotka on luokiteltu vaaralliseksi aineeksi.</span><span class="sxs-lookup"><span data-stu-id="06c79-124">For example, *Code 1* might represent items that have a hazardous material classification.</span></span> <span data-ttu-id="06c79-125">*Koodi 2* voisi taas ilmaista nimikkeitä, joita vain toimittajat voivat ostaa.</span><span class="sxs-lookup"><span data-stu-id="06c79-125">*Code 2* might represent items that only vendors can purchase.</span></span> <span data-ttu-id="06c79-126">Tuotesuodattimet määrittävät sitten tietyn **suodatinkoodin** arvon, joka liitetään **suodattimen otsikon** arvoon.</span><span class="sxs-lookup"><span data-stu-id="06c79-126">Product filters then define the specific **Filter code** value that is associated with a **Filter title** value.</span></span>

1. <span data-ttu-id="06c79-127">Valitse **Varastonhallinta \> Asetukset \> Tuotesuodattimet \> Tuotesuodattimet**.</span><span class="sxs-lookup"><span data-stu-id="06c79-127">Go to **Warehouse management \> Setup \> Product filters \> Product filters**.</span></span>
1. <span data-ttu-id="06c79-128">Lisää tuotesuodatin ruudukkoon valitsemalla toimintoruudussa **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="06c79-128">On the Action Pane, select **New** to add a product filter to the grid.</span></span>
1. <span data-ttu-id="06c79-129">Valitse **Suodattimen otsikko** -kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="06c79-129">In the **Filter title** field, select a value.</span></span>
1. <span data-ttu-id="06c79-130">Anna **Suodatinkoodi**-kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="06c79-130">In the **Filter code** field, enter a value.</span></span>

    <span data-ttu-id="06c79-131">![Tuotesuodattimen määrittäminen](media/Product_Filters10.png "Tuotesuodattimen määrittäminen")</span><span class="sxs-lookup"><span data-stu-id="06c79-131">![Setting up a product filter](media/Product_Filters10.png "Setting up a product filter")</span></span>

1. <span data-ttu-id="06c79-132">Anna koodi nimi **Kuvaus**-kentässä.</span><span class="sxs-lookup"><span data-stu-id="06c79-132">In the **Description** field, enter a name for the code.</span></span> <span data-ttu-id="06c79-133">Esimerkiksi *Koodi 2* voi viitata toimittajiin.</span><span class="sxs-lookup"><span data-stu-id="06c79-133">For example, *Code 2* might represent vendors.</span></span> <span data-ttu-id="06c79-134">Tämän jälkeen tietylle toimittajalle tai toimittajaryhmällä voidaan luoda tuotesuodatin.</span><span class="sxs-lookup"><span data-stu-id="06c79-134">You can then create a product filter for a specific vendor or group of vendors.</span></span> <span data-ttu-id="06c79-135">Lisätietoja on jäljempänä tämän aiheen kohdassa [Toimittajan suodatinkoodien määrittäminen](#vendor-product-filters).</span><span class="sxs-lookup"><span data-stu-id="06c79-135">For more information, see the [Setup vendor filter codes](#vendor-product-filters) section later in this topic.</span></span>

    <span data-ttu-id="06c79-136">![Tuotesuodattimien joukko](media/Product_Filters.png "Tuotesuodattimien joukko")</span><span class="sxs-lookup"><span data-stu-id="06c79-136">![Set of product filters](media/Product_Filters.png "Set of product filters")</span></span>

## <a name="set-up-product-filter-groups"></a><span data-ttu-id="06c79-137">Tuotesuodatinryhmien määrittäminen</span><span class="sxs-lookup"><span data-stu-id="06c79-137">Set up product filter groups</span></span>

<span data-ttu-id="06c79-138">Suodatinkoodeja voi ryhmitellä suodatinryhmien avulla.</span><span class="sxs-lookup"><span data-stu-id="06c79-138">You can use filter groups to group filter codes.</span></span> <span data-ttu-id="06c79-139">Tämä ominaisuus on kätevä, kun ryhmää käytetään sijaintidirektiivissä tehtävässä kyselyssä, ja haku halutaan kohdistaa ryhmää eikä koodisarjoihin.</span><span class="sxs-lookup"><span data-stu-id="06c79-139">This capability is helpful when a group is used in a query in a location directive, and you want to search for the group instead of a series of codes.</span></span> <span data-ttu-id="06c79-140">Kukin suodatinryhmä liitetään nimikeryhmään.</span><span class="sxs-lookup"><span data-stu-id="06c79-140">Each filter group is associated with an item group.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="06c79-141">Kaikki tuotesuodatinryhmät eivät ole käytettävissä suodatinkoodeille, jotka on suurempia kuin *Koodi 4* (eli koodit *Koodi 5*–*Koodi 10*).</span><span class="sxs-lookup"><span data-stu-id="06c79-141">Not all product filter groups are available for filter codes that are higher than *Code 4* (that is, *Code 5* through *Code 10*).</span></span> <span data-ttu-id="06c79-142">Vaikka esimerkiksi vapautettuihin tuotteisiin voidaan lisätä kaikki tuotteen suodatinkoodit, suodatinkoodien ryhmittelyä ei päivitetä.</span><span class="sxs-lookup"><span data-stu-id="06c79-142">For example, for released products, although all the product filter codes will be added, the grouping of filter codes won't be updated.</span></span> <span data-ttu-id="06c79-143">Tämä toiminto saatetaan päivittää myöhemmissä julkaisuissa.</span><span class="sxs-lookup"><span data-stu-id="06c79-143">This behavior might be updated in later releases.</span></span>

<span data-ttu-id="06c79-144">Suodatinryhmät määritetään seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="06c79-144">To set up filter groups, follow these steps.</span></span>

1. <span data-ttu-id="06c79-145">Valitse **Varastonhallinta \> Asetukset \> Tuotesuodattimet \> Tuotesuodatinryhmät**.</span><span class="sxs-lookup"><span data-stu-id="06c79-145">Go to **Warehouse management \> Setup \> Product filters \> Product filter groups**.</span></span>
1. <span data-ttu-id="06c79-146">Valitse toimintoruudussa **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="06c79-146">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="06c79-147">Anna **Ryhmä 1**- ja **Ryhmä 2** -kentissä nimet, joilla nimikkeitä luokitellaan.</span><span class="sxs-lookup"><span data-stu-id="06c79-147">In the **Group 1** and **Group 2** fields, enter the names that will be used to categorize items.</span></span>
1. <span data-ttu-id="06c79-148">Lisää rivi valitsemalla **Tiedot**-pikavälilehdessä **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="06c79-148">On the **Details** FastTab, select **New** to add a line.</span></span>
1. <span data-ttu-id="06c79-149">Anna suodatinryhmät alkamis- ja päättymispäivät **Alkamispäivämäärä ja -aika**- ja **Päättymispäivämäärä ja -aika** -kentissä.</span><span class="sxs-lookup"><span data-stu-id="06c79-149">In the **Start date/time** and **End date/time** fields, enter start and end dates for the filter group.</span></span>
1. <span data-ttu-id="06c79-150">Valitse **Nimikeryhmä**-kentässä nimikeryhmä, jossa tuotesuodatinta käytetään.</span><span class="sxs-lookup"><span data-stu-id="06c79-150">In the **Item group** field, select the item group that the product filter should apply to.</span></span>
1. <span data-ttu-id="06c79-151">Valitse ryhmässä käytettävät suodatinkoodit tarpeen mukaan kentissä **Koodi 1**–**Koodi 10**.</span><span class="sxs-lookup"><span data-stu-id="06c79-151">In the **Code 1** through **Code 10** fields, select the filter codes to include in the group, as required.</span></span>

    <span data-ttu-id="06c79-152">![Nimikeryhmä](media/ProdFilterGroup.png "Nimikeryhmä")</span><span class="sxs-lookup"><span data-stu-id="06c79-152">![Item group](media/ProdFilterGroup.png "Item group")</span></span>

> [!NOTE]
> <span data-ttu-id="06c79-153">Jos virhesanoma avautuu, kun sivu suljetaan, koodimääritys saattaa puuttua.</span><span class="sxs-lookup"><span data-stu-id="06c79-153">If you receive an error message when you close the page, a code setup might be missing.</span></span> <span data-ttu-id="06c79-154">Nimikeryhmän koodeista voidaan tehdä pakollisia valitsemalla **Nimikeryhmät**-sivulla valintaruudut **Määritä nimikeryhmälle suodatinkoodi 1**, **Määritä nimikeryhmälle suodatinkoodi 2** ja niin edelleen.</span><span class="sxs-lookup"><span data-stu-id="06c79-154">On the **Item groups** page, you can make the codes mandatory for an item group by selecting the **Assign filter code 1 for item group**, **Assign filter code 2 for item group**, and so on, check boxes.</span></span>

## <a name="set-up-filter-codes-on-item-groups"></a><span data-ttu-id="06c79-155">Nimikeryhmien suodatinkoodien määrittäminen</span><span class="sxs-lookup"><span data-stu-id="06c79-155">Set up filter codes on item groups</span></span>

<span data-ttu-id="06c79-156">Nimikeryhmään määritettyjen suodatinkoodien avulla koodeista tulee pakollisia kyseiseen nimikeryhmään liitetyissä tuotteissa.</span><span class="sxs-lookup"><span data-stu-id="06c79-156">By setting up filter codes on an item group, you can make the codes that are required for products that are attached to that item group.</span></span>

<span data-ttu-id="06c79-157">Suodatinkoodit määritetään nimikeryhmissä seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="06c79-157">To set up filter codes on item groups, follow these steps.</span></span>

1. <span data-ttu-id="06c79-158">Valitse **Varastonhallinta \> Asetukset \> Varasto \> Nimikeryhmät**.</span><span class="sxs-lookup"><span data-stu-id="06c79-158">Go to **Inventory management \> Setup \> Inventory \> Item groups**.</span></span>
1. <span data-ttu-id="06c79-159">Luo nimikeryhmä valitse toimintoruudussa **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="06c79-159">On the Action Pane, select **New** to create an item group.</span></span>
1. <span data-ttu-id="06c79-160">Anna **Nimikeryhmä**-kentässä nimi.</span><span class="sxs-lookup"><span data-stu-id="06c79-160">In the **Item group** field, enter a name.</span></span>
1. <span data-ttu-id="06c79-161">Anna kuvaus **nimi**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="06c79-161">In the **Name** field, enter a description.</span></span>
1. <span data-ttu-id="06c79-162">Valitse **Varasto**-pikavälilehden **Pakollinen suodatin** -osassa niiden suodatinkoodien valintaruudut, jotka on määritettävä nimikeryhmään liitetyille tuotteille.</span><span class="sxs-lookup"><span data-stu-id="06c79-162">On the **Warehouse** FastTab, in the **Filter required** section, select the check boxes for the filter codes that must be specified for products that are associated with the item group.</span></span>

    <span data-ttu-id="06c79-163">Päivitä vapautettu tuote avaamalla tuotteen **Vapautetun tuotteen tiedot** -sivu ja valitsemalla sitten toimintoruudussa **Muokkaa**.</span><span class="sxs-lookup"><span data-stu-id="06c79-163">To update a released product, open its **Released product details** page, and then, on the Action Pane, select **Edit**.</span></span> <span data-ttu-id="06c79-164">Koodeihin liitetyt suodattimet ovat tämän jälkeen käytettävissä **Varasto**-pikavälilehdessä.</span><span class="sxs-lookup"><span data-stu-id="06c79-164">The filters that are associated with codes then become available on the **Warehouse** FastTab.</span></span>

    <span data-ttu-id="06c79-165">![Nimikeryhmät](media/ItemGroup10.png "Nimikeryhmät")</span><span class="sxs-lookup"><span data-stu-id="06c79-165">![Item groups](media/ItemGroup10.png "Item groups")</span></span>

1. <span data-ttu-id="06c79-166">Valitse **Nimikeryhmän suodatin** -osassa niiden suodattimien valintaruudut, joiden on vastattava, jotta suodatinryhmä voi olla nimikkeen oletussuodatinryhmä.</span><span class="sxs-lookup"><span data-stu-id="06c79-166">In the **Item group filter** section, select the check boxes for the filters that must match for the filter group to be the default filter group for an item.</span></span>

    <span data-ttu-id="06c79-167">Jos esimerkiksi **Käytä suodatinkoodia 1** ja **Käytä suodatinkoodia 2** -valintaruudut on valittu, nimikkeen suodatinkoodin 1 ja suodatinkoodin 2 on vastattava nimikeryhmän suodatinryhmän määritystä, ennen kuin suodatinryhmä voidaan valita.</span><span class="sxs-lookup"><span data-stu-id="06c79-167">For example, if the **Use filter code 1** and **Use filter code 2** check boxes are selected, both filter code 1 and filter code 2 of the item must match the setup of the filter group for the item group before the filter group can be selected.</span></span> <span data-ttu-id="06c79-168">Uutta nimikettä luotaessa valittu suodatinryhmä on **Vapautetun tuotteen tiedot** -sivun **Varasto**-pikavälilehden **Ryhmä 1**- ja **Ryhmä 2** -kenttien oletussuodatinryhmä.</span><span class="sxs-lookup"><span data-stu-id="06c79-168">When you create a new item, the selected filter group will be the default filter group in the **Group 1** and **Group 2** fields on the **Warehouse** FastTab of the **Released product details** page.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="06c79-169">Tuotteen suodatinkoodit ovat käytössä vain nimikkeissä, joissa käytetään edistynyttä varastonhallintaa.</span><span class="sxs-lookup"><span data-stu-id="06c79-169">Product filter codes are enabled only for items that use advanced warehouse management.</span></span>

## <a name="specify-filter-codes-for-released-products"></a><span data-ttu-id="06c79-170">Vapautettujen tuotteiden suodatinkoodien määrittäminen</span><span class="sxs-lookup"><span data-stu-id="06c79-170">Specify filter codes for released products</span></span>

<span data-ttu-id="06c79-171">Vapautettujen tuotteiden suodatinkoodit määritetään seuraavien ohjeiden avulla.</span><span class="sxs-lookup"><span data-stu-id="06c79-171">Follow these steps to specify filter codes for released products.</span></span> <span data-ttu-id="06c79-172">Suodatinkoodeilla voi ryhmitellä esimerkiksi vaaralliset aineet, joita tietyt toimittajat ostavat.</span><span class="sxs-lookup"><span data-stu-id="06c79-172">For example, you can use filter codes to group hazardous products that specific vendors purchase.</span></span>

1. <span data-ttu-id="06c79-173">Mene **Tuotetietojen hallinta \> Tuotteet \> Vapautetut tuotteet**.</span><span class="sxs-lookup"><span data-stu-id="06c79-173">Go to **Product information management \> Products \> Released products**.</span></span>
1. <span data-ttu-id="06c79-174">Luo tuote valitsemalla toimintoruudussa **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="06c79-174">On the Action Pane, select **New** to create a product.</span></span>
1. <span data-ttu-id="06c79-175">Anna **Uusi vapautettu tuote** -valintaikkunassa tiedot, joita tarvitaan uuden tuotteen perustan luontiin, ja valitse sitten **OK**.</span><span class="sxs-lookup"><span data-stu-id="06c79-175">In the **New released product** dialog box, enter the data that is required to create the base of a new product, and then select **OK**.</span></span>

    <span data-ttu-id="06c79-176">Tuotteen suodatinkoodeja ei ole otettu käyttöön, ellei suodatinkoodeja ole määritetty nimikeryhmään, joka on liitetty tuotteeseen.</span><span class="sxs-lookup"><span data-stu-id="06c79-176">Product filter codes aren't enabled unless the item group that is attached to the product has been configured for filter codes.</span></span>

    <span data-ttu-id="06c79-177">Lisätietoja on kohdassa [Uuden tuotteen luominen](../pim/tasks/create-new-product.md).</span><span class="sxs-lookup"><span data-stu-id="06c79-177">For more information, see [Create a new product](../pim/tasks/create-new-product.md).</span></span>

1. <span data-ttu-id="06c79-178">Määritä tuotteen suodatinkoodit valitsemalla **Varasto**-pikavälilehden **Tuotteen suodatinkoodit**-osassa tarvittaessa kenttien **Koodi 1**–**Koodi 10** suodatinkoodit.</span><span class="sxs-lookup"><span data-stu-id="06c79-178">On the **Warehouse** FastTab, in the **Product filter codes** section, select filter codes for the **Code 1** through **Code 10** fields, as required, to specify filter codes for the product.</span></span>

## <a name="set-up-generally-available-items"></a><span data-ttu-id="06c79-179">Yleisesti saatavana olevien nimikkeiden määrittäminen</span><span class="sxs-lookup"><span data-stu-id="06c79-179">Set up generally available items</span></span>

<span data-ttu-id="06c79-180">Tietyt varastonimikkeet voidaan määrittää käytettäviksi vain asiakkaille, vain toimittajille tai asiakkaille ja toimittajille.</span><span class="sxs-lookup"><span data-stu-id="06c79-180">You can make specific inventory items available only for customers, only for vendors, or for both customers and vendors.</span></span>

> [!NOTE]
> <span data-ttu-id="06c79-181">Asiakkaan ja toimittajan suodattimia ei käytetä nimikkeissä, jotka on määritetty yleisesti saataville.</span><span class="sxs-lookup"><span data-stu-id="06c79-181">Customer and vendor filters don't apply to any item that is set up as generally available.</span></span>

<span data-ttu-id="06c79-182">Yleisesti saatavana olevat nimikkeet määritetään seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="06c79-182">To set up generally available items, follow these steps.</span></span>

1. <span data-ttu-id="06c79-183">Valitse **Varastonhallinta \> Asetukset \> Tuotesuodattimet \> Yleisesti saatavana olevat tuotteet**.</span><span class="sxs-lookup"><span data-stu-id="06c79-183">Go to **Warehouse management \> Setup \> Product filters \> Generally available products**.</span></span>
1. <span data-ttu-id="06c79-184">Luo tietue valitsemalla toimintoruudussa **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="06c79-184">On the Action Pane, select **New** to create a record.</span></span>
1. <span data-ttu-id="06c79-185">Tuo nimikkeet asiakkaiden, toimittajien tai molempien käyttöön valitsemalla **Asiakas tai toimittaja** -kentässä *Asiakas*, *Toimittaja* tai *Kaikki*.</span><span class="sxs-lookup"><span data-stu-id="06c79-185">In the **Customer or vendor** field, select *Customer*, *Vendor*, or *All* to make the items available for customers, vendors, or both.</span></span>
1. <span data-ttu-id="06c79-186">Anna **Alkamispäivämäärä ja -aika** -kentässä päivämäärä ja kellonaika, jolloin nimike on saatavana.</span><span class="sxs-lookup"><span data-stu-id="06c79-186">In the **Start date/time** field, enter the date and time when the item will become available.</span></span>
1. <span data-ttu-id="06c79-187">Valitse **Nimikeryhmä**-kentässä nimikeryhmä.</span><span class="sxs-lookup"><span data-stu-id="06c79-187">In the **Item group** field, select an item group.</span></span>
1. <span data-ttu-id="06c79-188">Rajoita yleisesti saatavana olevia nimikkeitä valitsemalla suodatuskoodit kentissä **Koodi 1**–**Koodi 10**.</span><span class="sxs-lookup"><span data-stu-id="06c79-188">In the **Code 1** through **Code 10** fields, select the filter codes to limit the items that are generally available.</span></span>

    <span data-ttu-id="06c79-189">Kun nimikeryhmä valitaan, kyseinen nimikeryhmä määritetään yleisesti saatavilla.</span><span class="sxs-lookup"><span data-stu-id="06c79-189">When you select an item group, you set that group of items as generally available.</span></span> <span data-ttu-id="06c79-190">Suodatinkoodien valitseminen näissä kentissä rajoittaa saatavana olevia nimikkeitä.</span><span class="sxs-lookup"><span data-stu-id="06c79-190">By selecting filter codes in these fields, you limit the items that are available.</span></span>

## <a name="set-up-customer-product-filters"></a><span data-ttu-id="06c79-191">Asiakkaan tuotesuodattimien määrittäminen</span><span class="sxs-lookup"><span data-stu-id="06c79-191">Set up customer product filters</span></span>

<span data-ttu-id="06c79-192">Tällä valinnaisella menetelmällä voidaan määrittää nimikkeet, joiden on oltava asiakkaiden käytettävissä niiden nimikkeiden ohella, jotka saadaan käytettäviksi **Yleisesti saatavana olevat nimikkeet** -sivun suodatinmääritysten perusteella.</span><span class="sxs-lookup"><span data-stu-id="06c79-192">You can use this optional procedure to specify items that should be available for a customer in addition to the items that are made available via the filter setup on the **Generally available items** page.</span></span> <span data-ttu-id="06c79-193">Yhdelle asiakkaalle voi määrittää useita suodattimia.</span><span class="sxs-lookup"><span data-stu-id="06c79-193">You can set up multiple filters for a single customer.</span></span>

<span data-ttu-id="06c79-194">Asiakkaan suodatinkoodit määritetään seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="06c79-194">To set up customer filter codes, follow these steps.</span></span>

1. <span data-ttu-id="06c79-195">Valitse **Myynti ja markkinointi \> Asiakkaat \> Kaikki asiakkaat**.</span><span class="sxs-lookup"><span data-stu-id="06c79-195">Go to **Sales and marketing \> Customers \> All customers**.</span></span>
1. <span data-ttu-id="06c79-196">Valitse asiakas.</span><span class="sxs-lookup"><span data-stu-id="06c79-196">Select a customer.</span></span>
1. <span data-ttu-id="06c79-197">Valitse toimintoruudun **Asiakas**-välilehden **Asetukset**-ryhmässä **Tuotesuodattimet**.</span><span class="sxs-lookup"><span data-stu-id="06c79-197">On the Action Pane, on the **Customer** tab, in the **Set up** group, select **Product filters**.</span></span>
1. <span data-ttu-id="06c79-198">Valitse **Tuotteen suodatinkoodit** -sivun toimintoruudussa **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="06c79-198">On the **Product filter codes** page, on the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="06c79-199">Anna valitun nimikeryhmän alkamis- ja päättymispäivät **Alkamispäivämäärä ja -aika**- ja **Päättymispäivämäärä ja -aika** -kentissä.</span><span class="sxs-lookup"><span data-stu-id="06c79-199">In the **Start date/time** and **End date/time** fields, enter start and end dates for the selected item group.</span></span>
1. <span data-ttu-id="06c79-200">Valitse **Nimikeryhmä**-kentässä nimikeryhmä.</span><span class="sxs-lookup"><span data-stu-id="06c79-200">In the **Item group** field, select an item group.</span></span>
1. <span data-ttu-id="06c79-201">Valitse kentissä **Koodi 1**–**Koodi 10** suodatinkoodit, joiden perusteella rajoitetaan asiakkaan saatavilla olevia nimikkeitä valitussa nimikeryhmässä.</span><span class="sxs-lookup"><span data-stu-id="06c79-201">In the **Code 1** through **Code 10** fields, select the filter codes to use as criteria to limit the items that are available for customers in the selected item group.</span></span> <span data-ttu-id="06c79-202">Valinta on tehtävä jokaisen nimikeryhmässä määritetyn suodatinkoodin osalta.</span><span class="sxs-lookup"><span data-stu-id="06c79-202">You must make a selection for every filter code that is set up for the item group.</span></span>

## <a name="set-up-vendor-product-filters"></a><a name="vendor-product-filters"></a><span data-ttu-id="06c79-203">Toimittajan tuotesuodattimien määrittäminen</span><span class="sxs-lookup"><span data-stu-id="06c79-203">Set up vendor product filters</span></span>

<span data-ttu-id="06c79-204">Tällä valinnaisella menetelmällä voidaan määrittää nimikkeet, joiden on oltava toimittajien käytettävissä niiden nimikkeiden ohella, jotka saadaan käytettäviksi **Yleisesti saatavana olevat nimikkeet** -sivun suodatinmääritysten perusteella.</span><span class="sxs-lookup"><span data-stu-id="06c79-204">You can use this optional procedure to specify items that should be available for a vendor in addition to the items that are made available via the filter setup on the **Generally available items** page.</span></span> <span data-ttu-id="06c79-205">Yhdelle toimittajalle voidaan määrittää useita suodattimia.</span><span class="sxs-lookup"><span data-stu-id="06c79-205">You can set up multiple filters for a single vendor.</span></span>

<span data-ttu-id="06c79-206">Toimittajan suodatinkoodit määritetään seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="06c79-206">To set up vendor filter codes, follow these steps.</span></span>

1. <span data-ttu-id="06c79-207">Valitse **Hankinta \> Toimittajat \> Kaikki toimittajat**.</span><span class="sxs-lookup"><span data-stu-id="06c79-207">Go to **Procurement and sourcing \> Vendors \> All vendors**.</span></span>
1. <span data-ttu-id="06c79-208">Valitse toimittaja.</span><span class="sxs-lookup"><span data-stu-id="06c79-208">Select a vendor.</span></span>
1. <span data-ttu-id="06c79-209">Valitse toimintoruudun **Toimittaja**-välilehden **Asetukset**-ryhmässä **Tuotesuodattimet**.</span><span class="sxs-lookup"><span data-stu-id="06c79-209">On the Action Pane, on the **Vendor** tab, in the **Set up** group, select **Product filters**.</span></span>
1. <span data-ttu-id="06c79-210">Valitse **Suodatinkoodit** -sivun toimintoruudussa **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="06c79-210">On the **Filter codes** page, on the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="06c79-211">Anna valitun nimikeryhmän alkamis- ja päättymispäivät **Alkamispäivämäärä ja -aika**- ja **Päättymispäivämäärä ja -aika** -kentissä.</span><span class="sxs-lookup"><span data-stu-id="06c79-211">In the **Start date/time** and **End date/time** fields, enter start and end dates for the selected item group.</span></span>
1. <span data-ttu-id="06c79-212">Valitse **Nimikeryhmä**-kentässä nimikeryhmä.</span><span class="sxs-lookup"><span data-stu-id="06c79-212">In the **Item group** field, select an item group.</span></span>
1. <span data-ttu-id="06c79-213">Valitse kentissä **Koodi 1**–**Koodi 10** suodatinkoodit, joiden perusteella rajoitetaan toimittajan saatavilla olevia nimikkeitä valitussa nimikeryhmässä.</span><span class="sxs-lookup"><span data-stu-id="06c79-213">In the **Code 1** through **Code 10** fields, select the filter codes to use as criteria to limit the items that are available for vendors in the selected item group.</span></span> <span data-ttu-id="06c79-214">Valinta on tehtävä jokaisen nimikeryhmässä määritetyn suodatinkoodin osalta.</span><span class="sxs-lookup"><span data-stu-id="06c79-214">You must make a selection for every filter code that is set up for the item group.</span></span>

> [!NOTE]
> <span data-ttu-id="06c79-215">Toimittajan tuotesuodattimien määritykset koskeva sellaisia vapautettuja tuotteita, joissa varastonhallintaprosessit on otettu käyttöön liitetyssä varastodimensioryhmässä.</span><span class="sxs-lookup"><span data-stu-id="06c79-215">The setup of vendor product filters applies to released products where warehouse management processes are enabled for the associated storage dimension group.</span></span> <span data-ttu-id="06c79-216">Suodatinkoodien avulla määritetään ostotilausrivejä luotaessa, antaako järjestelmä käyttäjien ostaa tietyn toimittajan tietyn nimikkeen.</span><span class="sxs-lookup"><span data-stu-id="06c79-216">The filter codes are used to determine whether the system will allow users to purchase a given item from a given vendor when they create purchase order lines.</span></span> <span data-ttu-id="06c79-217">Microsoft Dynamics 365 Supply Chain Managementissa on kaksi tapaa käsitellä toimittajan hyväksyntää.</span><span class="sxs-lookup"><span data-stu-id="06c79-217">Microsoft Dynamics 365 Supply Chain Management has two methods for handling vendor approval.</span></span> <span data-ttu-id="06c79-218">Jos vähintään yhdessä vapautetussa tuotteessa **Hyväksytyn toimittajan tarkistusmenetelmä** -kentän määrityksenä on *Vain varoitus* tai *Ei sallittu*, kumpikin toimittajan hyväksyntämenetelmä voidaan ottaa käyttöön kyseisissä nimikkeissä.</span><span class="sxs-lookup"><span data-stu-id="06c79-218">If one or more released products exist where the **Approved vendor check method** field is set to *Warning only* or *Not allowed*, both vendor approval methods could be enabled for those items.</span></span> <span data-ttu-id="06c79-219">Tämä tilanne voi aiheuttaa ongelmia, kun käyttäjät luovat ostotilausrivejä.</span><span class="sxs-lookup"><span data-stu-id="06c79-219">This situation might cause issues when users create purchase order lines.</span></span>

## <a name="see-also"></a><span data-ttu-id="06c79-220">Lisätietoja</span><span class="sxs-lookup"><span data-stu-id="06c79-220">See also</span></span>

[<span data-ttu-id="06c79-221">Lisätietoja on blogikirjoituksessa WMS-varaston suodatinkoodit</span><span class="sxs-lookup"><span data-stu-id="06c79-221">For more information see the blog post WMS-Warehouse Filter Codes</span></span>](http://blog.dynamics-for-operations.com/2017/09/26/wms-warehouse-filter-codes/)