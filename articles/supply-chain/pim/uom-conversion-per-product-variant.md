---
title: Mittayksiköiden tuotevarianttikohtaiset muunnokset
description: Tässä ohjeaiheessa käsitellään tuotevarianteille määritettäviä mittayksiköiden muunnoksia.
author: johanhoffmann
manager: AnnBe
ms.date: 01/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: UnitOfMeasureConversion
ROBOTS: noindex, nofollow
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-04-01
ms.dyn365.ops.version: 10
ms.openlocfilehash: c8181f0bda9b781a6c2b0feb0aba1beb51bfea65
ms.sourcegitcommit: af36eb17b36092a3101bbfc96486b25036676558
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/06/2020
ms.locfileid: "2935096"
---
# <a name="unit-of-measure-conversion-per-product-variant"></a><span data-ttu-id="b0f87-103">Mittayksiköiden tuotevarianttikohtaiset muunnokset</span><span class="sxs-lookup"><span data-stu-id="b0f87-103">Unit of measure conversion per product variant</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b0f87-104">Tässä ohjeaiheessa käsitellään tuotevarianteille määritettäviä mittayksiköiden muunnoksia.</span><span class="sxs-lookup"><span data-stu-id="b0f87-104">This topic explains how unit of measure conversions can be set up on product variants.</span></span> <span data-ttu-id="b0f87-105">Siinä on myös määritysesimerkki.</span><span class="sxs-lookup"><span data-stu-id="b0f87-105">It includes an example of the setup.</span></span>

<span data-ttu-id="b0f87-106">Tämän ominaisuuden ansiosta yritykset voivat määrittää yksikkömuunnokset saman tuotteen varianttien välillä.</span><span class="sxs-lookup"><span data-stu-id="b0f87-106">This feature makes it possible for companies to define different unit conversion between the variants of the same product.</span></span> <span data-ttu-id="b0f87-107">Tässä ohjeaiheessa käytetään seuraavaa esimerkkiä.</span><span class="sxs-lookup"><span data-stu-id="b0f87-107">The following example is used in this topic.</span></span> <span data-ttu-id="b0f87-108">Yritys myy t-paitoja, joiden koot ovat S, M, L ja XL.</span><span class="sxs-lookup"><span data-stu-id="b0f87-108">A company sells T-shirts in sizes Small, Medium, Large, and Extra-Large.</span></span> <span data-ttu-id="b0f87-109">T-paita määritetään tuotteena ja eri koot määritetään tuotteen variantteina.</span><span class="sxs-lookup"><span data-stu-id="b0f87-109">The T-shirt is defined as a product, and the different sizes are defined as variants of the product.</span></span> <span data-ttu-id="b0f87-110">T-paidat pakataan laatikoihin. Laatikossa voi olla viisi t-paitaa, joskin XL-koossa tilaa on kuitenkin vain neljälle t-paidalle.</span><span class="sxs-lookup"><span data-stu-id="b0f87-110">The T-shirts are packed in boxes and there can be five T-shirts in a box, except for the Extra-Large size where there is only space for four T-shirts.</span></span> <span data-ttu-id="b0f87-111">Yritys haluaa seurata t-paitojen eri variantteja **Kappaletta**-yksikkönä, vaikka niitä myydään **Laatikot**-yksikkönä.</span><span class="sxs-lookup"><span data-stu-id="b0f87-111">The company wants to track the different variants of the T-shirts in the unit **Pieces** but is selling the T-shirts in the unit **Boxes**.</span></span> <span data-ttu-id="b0f87-112">Varastoyksikön ja myyntiyksikön välinen muunto on 1 laatikko = 5 kappaletta. XL-variantin muunto on kuitenkin 1 laatikko = 4 kappaletta.</span><span class="sxs-lookup"><span data-stu-id="b0f87-112">The conversion between the inventory unit and the sales unit is 1 Box = 5 Pieces, except for the variant Extra-Large, where the conversion is 1 Box = 4 Pieces.</span></span>

### <a name="set-up-a-product-for-unit-conversion-per-variant"></a><span data-ttu-id="b0f87-113">Tuotteen varianttikohtaisen yksikkömuunnoksen määrittäminen</span><span class="sxs-lookup"><span data-stu-id="b0f87-113">Set up a product for unit conversion per variant</span></span>

<span data-ttu-id="b0f87-114">Tuotevariantit voidaan luoda vain **Tuotteen alatyyppi**: **Päätuote** -tuotteille.</span><span class="sxs-lookup"><span data-stu-id="b0f87-114">Product variants can only be created for products of **Product subtype**: **Product master**.</span></span> <span data-ttu-id="b0f87-115">Lisätietoja on kohdassa [Päätuotteen luominen](tasks/create-product-master.md).</span><span class="sxs-lookup"><span data-stu-id="b0f87-115">For more information, see [Create a product master](tasks/create-product-master.md).</span></span>

<span data-ttu-id="b0f87-116">Tätä ominaisuutta ei ole otettu käyttöön tuotteille, jotka on määritetty todellisen painon prosesseille.</span><span class="sxs-lookup"><span data-stu-id="b0f87-116">The feature is not enabled for products that are set up for Catch Weight processes.</span></span> 

<span data-ttu-id="b0f87-117">Kun luodaan päätuote, jolla on julkaistuja tuotevariantteja, varianttikohtaiset yksikkömuunnokset voidaan määrittää.</span><span class="sxs-lookup"><span data-stu-id="b0f87-117">When the product master with released products variants is created, unit conversions per variants can be set up.</span></span> <span data-ttu-id="b0f87-118">Yksikön muunnossivun avaava valikkovaihtoehto on tuotteen tai tuotevariantin yhteydessä seuraavilla sivuilla.</span><span class="sxs-lookup"><span data-stu-id="b0f87-118">You can find the menu item for opening the unit conversion page in context of a product or a product variant on the following pages.</span></span>

-   <span data-ttu-id="b0f87-119">**Tuotteen tiedot** -sivut</span><span class="sxs-lookup"><span data-stu-id="b0f87-119">**Product details** page</span></span>
-   <span data-ttu-id="b0f87-120">**Julkaistujen tuotteiden tiedot** -sivu</span><span class="sxs-lookup"><span data-stu-id="b0f87-120">**Released products details** page</span></span>
-   <span data-ttu-id="b0f87-121">**Vapautetut tuotevariantit** -sivu</span><span class="sxs-lookup"><span data-stu-id="b0f87-121">**Released product variants** page</span></span>

<span data-ttu-id="b0f87-122">Kun avaat **Yksikkömuunnos**-sivun päätuotteen tai vapautetun tuotevariantin yhteydessä, voit valita, haluatko määrittää tuotteelle tai tuotevariantille yksikkömuunnoksen.</span><span class="sxs-lookup"><span data-stu-id="b0f87-122">When you open the **Unit conversion** page in context of a product master or released product variant, you can select if you want to set up the unit conversion for the product or for a product variant.</span></span> <span data-ttu-id="b0f87-123">Tee se valitsemalla joko **Tuotevariantti** tai **Tuote** **Luo muunnos kohteelle** -kentässä.</span><span class="sxs-lookup"><span data-stu-id="b0f87-123">You do that by selecting either **Product variant** or **Product** in the **Create conversion for** field.</span></span>

### <a name="product-variant"></a><span data-ttu-id="b0f87-124">Tuotevariantti</span><span class="sxs-lookup"><span data-stu-id="b0f87-124">Product variant</span></span>

<span data-ttu-id="b0f87-125">Jos valitset **Tuotevariantti**, voit sitten valita, minkä variantin yksikkömuunnoksen haluat määrittää **Tuotevariantti**-kentässä.</span><span class="sxs-lookup"><span data-stu-id="b0f87-125">If you select **Product variant,** then you can select for which variant you want to set up the unit conversion in the **Product variant** field.</span></span>

### <a name="product"></a><span data-ttu-id="b0f87-126">Tuote</span><span class="sxs-lookup"><span data-stu-id="b0f87-126">Product</span></span>

<span data-ttu-id="b0f87-127">Jos valitset **Tuote**, voit määrittää päätuotteen yksikkömuunnoksen.</span><span class="sxs-lookup"><span data-stu-id="b0f87-127">If you select **Product**, then you can set up a unit conversion for the product master.</span></span> <span data-ttu-id="b0f87-128">Tätä yksikkömuunnosta käytetään kaikissa tuotevarianteissa, joissa yksikkömuunnosta ei ole määritetty.</span><span class="sxs-lookup"><span data-stu-id="b0f87-128">This unit conversion will apply for all product variants with no defined unit conversion.</span></span>

### <a name="example"></a><span data-ttu-id="b0f87-129">Esimerkki</span><span class="sxs-lookup"><span data-stu-id="b0f87-129">Example</span></span>

<span data-ttu-id="b0f87-130">Päätuotteella, **T-paita**, on neljä vapautettua tuotevarianttia: S, M, L ja XL.</span><span class="sxs-lookup"><span data-stu-id="b0f87-130">A product master, **T-Shirt**, has four released products variants Small, Medium, Large, and X-Large.</span></span> <span data-ttu-id="b0f87-131">T-paidat pakataan laatikoihin. Laatikossa voi olla viisi t-paitaa, joskin XL-koossa tilaa on kuitenkin vain neljälle t-paidalle.</span><span class="sxs-lookup"><span data-stu-id="b0f87-131">The T-shirts are packed in boxes and there can be five T-shirts in a box, except for the Extra-large size where there is only space for four T-shirts.</span></span>

<span data-ttu-id="b0f87-132">Avaa ensin **Yksikkömuunnos**-sivu **t-paidan** Vapautetun tuotteen tiedot -sivulla.</span><span class="sxs-lookup"><span data-stu-id="b0f87-132">First, open the **Unit conversion** page from the Release product details page for **T-shirt.**</span></span>

<span data-ttu-id="b0f87-133">Määritä **Yksikkömuunnos**-sivulla vapautetun XL-tuotevariantin yksikkömuunnos.</span><span class="sxs-lookup"><span data-stu-id="b0f87-133">On the **Unit conversion** page, set up the unit conversion for the release product variant X-Large.</span></span>

| <span data-ttu-id="b0f87-134">**Kenttä**</span><span class="sxs-lookup"><span data-stu-id="b0f87-134">**Field**</span></span>             | <span data-ttu-id="b0f87-135">**Asetus**</span><span class="sxs-lookup"><span data-stu-id="b0f87-135">**Setting**</span></span>             |
|-----------------------|-------------------------|
| <span data-ttu-id="b0f87-136">Luo muunnos kohteelle</span><span class="sxs-lookup"><span data-stu-id="b0f87-136">Create conversion for</span></span> | <span data-ttu-id="b0f87-137">Tuotevariantti</span><span class="sxs-lookup"><span data-stu-id="b0f87-137">Product variant</span></span>         |
| <span data-ttu-id="b0f87-138">Tuotevariantti</span><span class="sxs-lookup"><span data-stu-id="b0f87-138">Product variant</span></span>       | <span data-ttu-id="b0f87-139">T-paita : : XL : :</span><span class="sxs-lookup"><span data-stu-id="b0f87-139">T-Shirt : : X-Large : :</span></span> |
| <span data-ttu-id="b0f87-140">Yksiköstä</span><span class="sxs-lookup"><span data-stu-id="b0f87-140">From unit</span></span>             | <span data-ttu-id="b0f87-141">Laatikot</span><span class="sxs-lookup"><span data-stu-id="b0f87-141">Boxes</span></span>                   |
| <span data-ttu-id="b0f87-142">Kerroin</span><span class="sxs-lookup"><span data-stu-id="b0f87-142">Factor</span></span>                | <span data-ttu-id="b0f87-143">4</span><span class="sxs-lookup"><span data-stu-id="b0f87-143">4</span></span>                       |
| <span data-ttu-id="b0f87-144">Yksikköön</span><span class="sxs-lookup"><span data-stu-id="b0f87-144">To Unit</span></span>               | <span data-ttu-id="b0f87-145">Kappaletta</span><span class="sxs-lookup"><span data-stu-id="b0f87-145">Pieces</span></span>                  |

<span data-ttu-id="b0f87-146">Vapautetuilla S-, M- ja L-tuotevarianteilla on sama yksikkömuunnos laatikon ja kappaleen välillä, joten voit määrittää näiden tuotevarianttien yksikkömuunnoksen päätuotteessa.</span><span class="sxs-lookup"><span data-stu-id="b0f87-146">The Released product variants Small, Medium, and Large have the same unit conversion between the unit Box and Pieces, which means that you can define the unit conversion for these product variants on the product master.</span></span>

| <span data-ttu-id="b0f87-147">**Kenttä**</span><span class="sxs-lookup"><span data-stu-id="b0f87-147">**Field**</span></span>             | <span data-ttu-id="b0f87-148">**Asetus**</span><span class="sxs-lookup"><span data-stu-id="b0f87-148">**Setting**</span></span> |
|-----------------------|-------------|
| <span data-ttu-id="b0f87-149">Luo muunnos kohteelle</span><span class="sxs-lookup"><span data-stu-id="b0f87-149">Create conversion for</span></span> | <span data-ttu-id="b0f87-150">Tuote</span><span class="sxs-lookup"><span data-stu-id="b0f87-150">Product</span></span>     |
| <span data-ttu-id="b0f87-151">Tuote</span><span class="sxs-lookup"><span data-stu-id="b0f87-151">Product</span></span>               | <span data-ttu-id="b0f87-152">T-paita</span><span class="sxs-lookup"><span data-stu-id="b0f87-152">T-Shirt</span></span>     |
| <span data-ttu-id="b0f87-153">Yksiköstä</span><span class="sxs-lookup"><span data-stu-id="b0f87-153">From unit</span></span>             | <span data-ttu-id="b0f87-154">Laatikot</span><span class="sxs-lookup"><span data-stu-id="b0f87-154">Boxes</span></span>       |
| <span data-ttu-id="b0f87-155">Kerroin</span><span class="sxs-lookup"><span data-stu-id="b0f87-155">Factor</span></span>                | <span data-ttu-id="b0f87-156">5</span><span class="sxs-lookup"><span data-stu-id="b0f87-156">5</span></span>           |
| <span data-ttu-id="b0f87-157">Yksikköön</span><span class="sxs-lookup"><span data-stu-id="b0f87-157">To Unit</span></span>               | <span data-ttu-id="b0f87-158">Kappaletta</span><span class="sxs-lookup"><span data-stu-id="b0f87-158">Pieces</span></span>      |

### <a name="using-excel-to-update-the-unit-conversions"></a><span data-ttu-id="b0f87-159">Yksikkömuunnosten päivittäminen Excelin avulla</span><span class="sxs-lookup"><span data-stu-id="b0f87-159">Using Excel to update the unit conversions</span></span>

<span data-ttu-id="b0f87-160">Jos tuotteella on useita tuotevariantteja, joilla on erilaiset yksikkömuunnokset, yksikkömuunnokset kannattaa viedä **Yksikkömuunnos**-sivulta Excel-laskentataulukkoon, päivittää sitten muunnokset ja julkaista ne lopuksi takaisin Supply Chain Mangementiin.</span><span class="sxs-lookup"><span data-stu-id="b0f87-160">If a product has many product variants with different unit conversions, it's a good idea to export the unit conversions from the **Unit conversion** page to an Excel spreadsheet, update the conversions, and then publish them back to Supply Chain Mangement.</span></span>

<span data-ttu-id="b0f87-161">Exceliin viennin ja muokkausten takaisin Supply Chain Mangementiin julkaisemisen asetus otetaan käyttöön **Yksikkömuunnos**-sivun toimintoruudun **Avaa Microsoft Officessa** -valikkovaihtoehdossa.</span><span class="sxs-lookup"><span data-stu-id="b0f87-161">The option to export to Excel and publish the edits back to Supply Chain Mangement is enabled from the **Open in Microsoft office** menu item on the Action Pane on the **Unit conversion** page.</span></span>
