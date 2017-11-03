---
title: Tuotedimensiot
description: "Tuotedimensioita on neljä: Väri, Konfigurointi, Koko ja Tyyli. Tuotedimensiot yhdistetään dimensioryhmiksi ja dimensioryhmät liitetään päätuotteisiin. Tuotedimensioiden yhdistelmät määrittävät sen, kuinka tuotevariantit määritetään."
author: cvocph
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: EcoResProductDimension, EcoResProductDimensionGroup, EcoResProductMasterDimension, RetailEcoResColor, RetailEcoResSize, RetailEcoResStyle
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: Core, Operations, Retail
ms.custom: 19171
ms.assetid: 81fa3709-4ab8-4fbf-9806-359892a05985
ms.search.region: Global
ms.search.industry: Retail
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 68f4bfcf62b5e7c65cbe361b510c2769b0e9bebb
ms.contentlocale: fi-fi
ms.lasthandoff: 11/03/2017

---

# <a name="product-dimensions"></a><span data-ttu-id="9bc37-105">Tuotedimensiot</span><span class="sxs-lookup"><span data-stu-id="9bc37-105">Product dimensions</span></span>

[!include[banner](../includes/banner.md)]

[!include[Retail name](../includes/retail-name.md)]


<span data-ttu-id="9bc37-106">Tuotedimensioita on neljä: Väri, Konfigurointi, Koko ja Tyyli.</span><span class="sxs-lookup"><span data-stu-id="9bc37-106">There are four product dimensions -  Color, Configuration, Size and Style.</span></span> <span data-ttu-id="9bc37-107">Tuotedimensiot yhdistetään dimensioryhmiksi ja dimensioryhmät liitetään päätuotteisiin.</span><span class="sxs-lookup"><span data-stu-id="9bc37-107">You combine product dimensions in dimension groups and assign dimension groups to product masters.</span></span> <span data-ttu-id="9bc37-108">Tuotedimensioiden yhdistelmät määrittävät sen, kuinka tuotevariantit määritetään.</span><span class="sxs-lookup"><span data-stu-id="9bc37-108">The combinations of product dimensions determine how product variants are defined.</span></span>

<span data-ttu-id="9bc37-109">Tuotedimensiot ovat ominaisuuksia, joilla voidaan määrittää tuotemallin muuttuja.</span><span class="sxs-lookup"><span data-stu-id="9bc37-109">Product dimensions are characteristics that serve to identify a product variant.</span></span> <span data-ttu-id="9bc37-110">Voit käyttää tuotevarianttien määrittämiseen tuotedimensioiden yhdistelmiä.</span><span class="sxs-lookup"><span data-stu-id="9bc37-110">You can use combinations of product dimensions to define product variants.</span></span> <span data-ttu-id="9bc37-111">Sinun on määritettävä päätuotteelle vähintään yksi tuotedimensio, jotta voit luoda tuotevariantin.</span><span class="sxs-lookup"><span data-stu-id="9bc37-111">You must define at least one product dimension for a product master in order to create a product variant.</span></span>
<span data-ttu-id="9bc37-112">Tuotevariantit</span><span class="sxs-lookup"><span data-stu-id="9bc37-112">Product variants</span></span>
----------------

<span data-ttu-id="9bc37-113">Tuotemallin muuttujien kutsutaan myös nimikkeinä.</span><span class="sxs-lookup"><span data-stu-id="9bc37-113">Product variants are also referred to as items.</span></span> <span data-ttu-id="9bc37-114">Nimike on aineellinen tuote eikä tarkoita samaa kuin palvelu.</span><span class="sxs-lookup"><span data-stu-id="9bc37-114">An item is a tangible product, which is not the same as a service.</span></span> <span data-ttu-id="9bc37-115">Päätuotteen voi kuitenkin määrittää myös palvelutyypin kanssa.</span><span class="sxs-lookup"><span data-stu-id="9bc37-115">It is also possible to define a product master with the Service type.</span></span> <span data-ttu-id="9bc37-116">Käyttämällä Palvelu-tyyppiä voit määrittää tuotevariantit, jotka sisältävät palveluita.</span><span class="sxs-lookup"><span data-stu-id="9bc37-116">By using the Service type, you can specify product variants that include services.</span></span> <span data-ttu-id="9bc37-117">Voit esimerkiksi määrittää konsultointityölle päätuotteen ja tuotevariantit kokeneempien ja nuorempien konsulttien suorittamalle työlle.</span><span class="sxs-lookup"><span data-stu-id="9bc37-117">For example, you can specify a product master for Consultancy work and product variants for work that is performed by senior consultants and junior consultants.</span></span>

## <a name="product-dimensions"></a><span data-ttu-id="9bc37-118">Tuotedimensiot</span><span class="sxs-lookup"><span data-stu-id="9bc37-118">Product dimensions</span></span>
<span data-ttu-id="9bc37-119">Tuotedimensioita on neljä: Konfigurointi, Väri, Koko ja Tyyli.</span><span class="sxs-lookup"><span data-stu-id="9bc37-119">The following product dimensions are available: Configuration, Color, Size, and Style.</span></span> <span data-ttu-id="9bc37-120">Tuotevariantit voidaan luoda tuotedimensioarvojen perusteella.</span><span class="sxs-lookup"><span data-stu-id="9bc37-120">A product variant can be generated based on the product dimension values.</span></span>

<span data-ttu-id="9bc37-121">Tuotedimensioiden arvot, kuten Koko, Väri ja Tyyli, voidaan luoda **Koko**-, **Väri**- ja **Tyyli**-sivuilla, jotka voi avata valitsemalla **Tuotetietojen hallinta** &gt; **Asetukset** &gt; **Dimensio ja varianttiryhmät** &gt; **Koot/Värit/Tyylit**.</span><span class="sxs-lookup"><span data-stu-id="9bc37-121">Product dimensions values such as Size, Color and Style can be created on the **Size**, **Color** and **Style** pages, which can be accessed from the following locations: **Product information management** &gt; **Setup** &gt; **Dimension and variant Groups** &gt; **Sizes/Colors/Styles**.</span></span> <span data-ttu-id="9bc37-122">Konfiguraatiodimension tuotedimension arvot luodaan yleensä käyttämällä joko tuotekonfiguraatiota tai dimensioihin perustuvaa konfiguraatiota.</span><span class="sxs-lookup"><span data-stu-id="9bc37-122">Product dimension values for the Configuration dimension are typically created using either the Product configurator or the Dimension-based configurator.</span></span> <span data-ttu-id="9bc37-123">Tuotedimensioita voi luoda ja ylläpitää myös **Tuotedimensiot**-sivulla, jonka voi avata seuraavista sijainneista:</span><span class="sxs-lookup"><span data-stu-id="9bc37-123">Product dimensions can also be created and maintained on the **Product dimensions** page, which can be accessed from the following locations:</span></span>
-   <span data-ttu-id="9bc37-124">Valitse **Tuotetietojen hallinta** &gt; **Tuotteet** &gt; **Päätuotteet**.</span><span class="sxs-lookup"><span data-stu-id="9bc37-124">Click **Product information management** &gt; **Products** &gt; **Product masters**.</span></span> <span data-ttu-id="9bc37-125">Valitse **toimintoruudussa** **Tuotedimensiot**.</span><span class="sxs-lookup"><span data-stu-id="9bc37-125">On the **Action Pane**, click **Product dimensions**.</span></span>
-   <span data-ttu-id="9bc37-126">Valitse **Tuotetietojen hallinta** &gt; **Tuotteet** &gt; **Kaikki tuotteet ja päätuotteet**.</span><span class="sxs-lookup"><span data-stu-id="9bc37-126">Click **Product information management** &gt; **Products** &gt; **All products and product masters**.</span></span> <span data-ttu-id="9bc37-127">Valitse päätuote.</span><span class="sxs-lookup"><span data-stu-id="9bc37-127">Select a product master.</span></span> <span data-ttu-id="9bc37-128">Valitse **toimintoruudussa** **Tuotedimensiot**.</span><span class="sxs-lookup"><span data-stu-id="9bc37-128">On the **Action Pane**, click **Product dimensions**.</span></span>
-   <span data-ttu-id="9bc37-129">Valitse **Tuotetietojen hallinta** &gt; **Vapautetut tuotteet**.</span><span class="sxs-lookup"><span data-stu-id="9bc37-129">Click **Product information management** &gt; **Released products**.</span></span> <span data-ttu-id="9bc37-130">Valitse päätuote.</span><span class="sxs-lookup"><span data-stu-id="9bc37-130">Select a product master.</span></span> <span data-ttu-id="9bc37-131">Valitse **toimintoruudusta** **Tuote**.</span><span class="sxs-lookup"><span data-stu-id="9bc37-131">On the **Action Pane**, click **Product**.</span></span> <span data-ttu-id="9bc37-132">Valitse **Päätuote**-ryhmästä **Tuotedimensiot**.</span><span class="sxs-lookup"><span data-stu-id="9bc37-132">In the **Product master** group, click **Product dimensions**.</span></span>

<span data-ttu-id="9bc37-133">Tälle nimikkeelle luotavien varianttien lukumäärää rajoittaa mahdollisten tuotedimensioiden yhdistelmien määrä.</span><span class="sxs-lookup"><span data-stu-id="9bc37-133">The number of variants that you can create for an item is limited by the number of possible product dimension combinations.</span></span>
| <span data-ttu-id="9bc37-134">**Vihje**</span><span class="sxs-lookup"><span data-stu-id="9bc37-134">**Tip**</span></span>                                                                                                                                              |
|------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9bc37-135">Jos käytät tuotetta esimerkiksi tilausrivillä, voit valita tuotedimensiot määrittämään tuotevariantit, joita haluat käsitellä.</span><span class="sxs-lookup"><span data-stu-id="9bc37-135">When you use a product on, for example, an order line, you select the product dimensions to identify the product variant that you want to work with.</span></span> |

## <a name="example"></a><span data-ttu-id="9bc37-136">Esimerkki</span><span class="sxs-lookup"><span data-stu-id="9bc37-136">Example</span></span>
<span data-ttu-id="9bc37-137">Yritys myy farmarihousuja.</span><span class="sxs-lookup"><span data-stu-id="9bc37-137">A company sells denim jeans.</span></span> <span data-ttu-id="9bc37-138">Farkut-nimikkeessä on käytössä Väri- ja Koko-tuotedimensiot.</span><span class="sxs-lookup"><span data-stu-id="9bc37-138">The item, Jeans, uses the Color and Size product dimensions.</span></span> <span data-ttu-id="9bc37-139">Myytäviä farmarihousuja on kolmea eri väriä ja kuutta eri kokoa.</span><span class="sxs-lookup"><span data-stu-id="9bc37-139">The jeans are sold in three different colors and six different sizes.</span></span> <span data-ttu-id="9bc37-140">Värit: Sininen, musta, ruskea Koot: XS S, M, L, XL, XXL Kaikkia kokoja ei ole saatavana kolmena värinä.</span><span class="sxs-lookup"><span data-stu-id="9bc37-140">Colors: Blue, Black, Brown Sizes: XS, S, M, L, XL, XXL Not all sizes are available in all the three colors.</span></span> <span data-ttu-id="9bc37-141">Jos kaikki yhdistelmät olivat käytettävissä, ne loisivat 18 eri farmarihousutyyppiä.</span><span class="sxs-lookup"><span data-stu-id="9bc37-141">If all combinations were available, it would create 18 different types of jeans.</span></span> <span data-ttu-id="9bc37-142">Tässä esimerkissä tuotetaan vain seuraavat yhdeksän tuotevarianttia.</span><span class="sxs-lookup"><span data-stu-id="9bc37-142">In this example, only the following nine product variant combinations are produced.</span></span>

| <span data-ttu-id="9bc37-143">Väri</span><span class="sxs-lookup"><span data-stu-id="9bc37-143">Color</span></span> | <span data-ttu-id="9bc37-144">Koko</span><span class="sxs-lookup"><span data-stu-id="9bc37-144">Size</span></span> |
|-------|------|
| <span data-ttu-id="9bc37-145">Sininen</span><span class="sxs-lookup"><span data-stu-id="9bc37-145">Blue</span></span>  | <span data-ttu-id="9bc37-146">XS</span><span class="sxs-lookup"><span data-stu-id="9bc37-146">XS</span></span>   |
| <span data-ttu-id="9bc37-147">Sininen</span><span class="sxs-lookup"><span data-stu-id="9bc37-147">Blue</span></span>  | <span data-ttu-id="9bc37-148">L</span><span class="sxs-lookup"><span data-stu-id="9bc37-148">S</span></span>    |
| <span data-ttu-id="9bc37-149">Sininen</span><span class="sxs-lookup"><span data-stu-id="9bc37-149">Blue</span></span>  | <span data-ttu-id="9bc37-150">M</span><span class="sxs-lookup"><span data-stu-id="9bc37-150">M</span></span>    |
| <span data-ttu-id="9bc37-151">Musta</span><span class="sxs-lookup"><span data-stu-id="9bc37-151">Black</span></span> | <span data-ttu-id="9bc37-152">M</span><span class="sxs-lookup"><span data-stu-id="9bc37-152">M</span></span>    |
| <span data-ttu-id="9bc37-153">Musta</span><span class="sxs-lookup"><span data-stu-id="9bc37-153">Black</span></span> | <span data-ttu-id="9bc37-154">L</span><span class="sxs-lookup"><span data-stu-id="9bc37-154">L</span></span>    |
| <span data-ttu-id="9bc37-155">Musta</span><span class="sxs-lookup"><span data-stu-id="9bc37-155">Black</span></span> | <span data-ttu-id="9bc37-156">XL</span><span class="sxs-lookup"><span data-stu-id="9bc37-156">XL</span></span>   |
| <span data-ttu-id="9bc37-157">Ruskea</span><span class="sxs-lookup"><span data-stu-id="9bc37-157">Brown</span></span> | <span data-ttu-id="9bc37-158">L</span><span class="sxs-lookup"><span data-stu-id="9bc37-158">L</span></span>    |
| <span data-ttu-id="9bc37-159">Ruskea</span><span class="sxs-lookup"><span data-stu-id="9bc37-159">Brown</span></span> | <span data-ttu-id="9bc37-160">XL</span><span class="sxs-lookup"><span data-stu-id="9bc37-160">XL</span></span>   |
| <span data-ttu-id="9bc37-161">Ruskea</span><span class="sxs-lookup"><span data-stu-id="9bc37-161">Brown</span></span> | <span data-ttu-id="9bc37-162">XXL</span><span class="sxs-lookup"><span data-stu-id="9bc37-162">XXL</span></span>  |






