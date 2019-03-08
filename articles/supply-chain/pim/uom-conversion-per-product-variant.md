---
title: Mittayksiköiden tuotevarianttikohtaiset muunnokset
description: Tässä ohjeaiheessa käsitellään tuotevarianteille määritettäviä mittayksiköiden muunnoksia.
author: johanhoffmann
manager: AnnBe
ms.date: 12/18/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
ROBOTS: noindex, nofollow
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-04-01
ms.dyn365.ops.version: 10
ms.openlocfilehash: 9d5d6fd65717cd886f1c6576aabf2bc59ca4fcaf
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/29/2019
ms.locfileid: "345924"
---
# <a name="unit-of-measure-conversion-per-product-variant"></a><span data-ttu-id="80136-103">Mittayksiköiden tuotevarianttikohtaiset muunnokset</span><span class="sxs-lookup"><span data-stu-id="80136-103">Unit of measure conversion per product variant</span></span>

[!include [banner](../includes/banner.md)]

[!include [pivate-preview](../includes/pivate-preview-banner.md)]

<span data-ttu-id="80136-104">Tässä ohjeaiheessa käsitellään tuotevarianteille määritettäviä mittayksiköiden muunnoksia.</span><span class="sxs-lookup"><span data-stu-id="80136-104">This topic explains how unit of measure conversions can be set up on product variants.</span></span> <span data-ttu-id="80136-105">Siinä on myös määritysesimerkki.</span><span class="sxs-lookup"><span data-stu-id="80136-105">It includes an example of the setup.</span></span>

<span data-ttu-id="80136-106">Tämän ominaisuuden ansiosta yritykset voivat määrittää yksikkömuunnokset saman tuotteen varianttien välillä.</span><span class="sxs-lookup"><span data-stu-id="80136-106">This feature makes it possible for companies to define different unit conversion between the variants of the same product.</span></span> <span data-ttu-id="80136-107">Tässä ohjeaiheessa käytetään seuraavaa esimerkkiä.</span><span class="sxs-lookup"><span data-stu-id="80136-107">The following example is used in this topic.</span></span> <span data-ttu-id="80136-108">Yritys myy t-paitoja, joiden koot ovat S, M, L ja XL.</span><span class="sxs-lookup"><span data-stu-id="80136-108">A company sells T-shirts in sizes Small, Medium, Large, and Extra-Large.</span></span> <span data-ttu-id="80136-109">T-paita määritetään tuotteena ja eri koot määritetään tuotteen variantteina.</span><span class="sxs-lookup"><span data-stu-id="80136-109">The T-shirt is defined as a product, and the different sizes are defined as variants of the product.</span></span> <span data-ttu-id="80136-110">T-paidat pakataan laatikoihin. Laatikossa voi olla viisi t-paitaa, joskin XL-koossa tilaa on kuitenkin vain neljälle t-paidalle.</span><span class="sxs-lookup"><span data-stu-id="80136-110">The T-shirts are packed in boxes and there can be five T-shirts in a box, except for the Extra-Large size where there is only space for four T-shirts.</span></span> <span data-ttu-id="80136-111">Yritys haluaa seurata t-paitojen eri variantteja **Kappaletta**-yksikkönä, vaikka niitä myydään **Laatikot**-yksikkönä.</span><span class="sxs-lookup"><span data-stu-id="80136-111">The company wants to track the different variants of the T-shirts in the unit **Pieces** but is selling the T-shirts in the unit **Boxes**.</span></span> <span data-ttu-id="80136-112">Varastoyksikön ja myyntiyksikön välinen muunto on 1 laatikko = 5 kappaletta. XL-variantin muunto on kuitenkin 1 laatikko = 4 kappaletta.</span><span class="sxs-lookup"><span data-stu-id="80136-112">The conversion between the inventory unit and the sales unit is 1 Box = 5 Pieces, except for the variant Extra-Large, where the conversion is 1 Box = 4 Pieces.</span></span>

## <a name="setup"></a><span data-ttu-id="80136-113">Luo perustiedot</span><span class="sxs-lookup"><span data-stu-id="80136-113">Setup</span></span>

<span data-ttu-id="80136-114">Voit määrittää parametrit, jolla käytetään ominaisuutta tuotteissa, joissa **Kaikki prosessit** on otettu käyttöön, tai vain tuotteessa, joissa **Varastoprosessit** on otettu käyttöön. Määritys tehdään **Tuotetietojen hallintaparametrit** -sivun **Ota käyttöön mittayksiköiden muunnokset** -asetuksella.</span><span class="sxs-lookup"><span data-stu-id="80136-114">You can configure the parameters for using the feature for products enabled for **All processes** or only for product enabled for the **Warehouse processes** by using the **Enable unit of measure conversations** option on the **Product information parameters** page.</span></span>

### <a name="set-up-a-product-for-unit-conversion-per-variant"></a><span data-ttu-id="80136-115">Tuotteen varianttikohtaisen yksikkömuunnoksen määrittäminen</span><span class="sxs-lookup"><span data-stu-id="80136-115">Set up a product for unit conversion per variant</span></span>

<span data-ttu-id="80136-116">Tuotevariantit voidaan luoda vain **Tuotteen alatyyppi**: **Päätuote** -tuotteille.</span><span class="sxs-lookup"><span data-stu-id="80136-116">Product variants can only be created for products of **Product subtype**: **Product master**.</span></span> <span data-ttu-id="80136-117">Lisätietoja on kohdassa [Päätuotteen luominen](tasks/create-product-master.md).</span><span class="sxs-lookup"><span data-stu-id="80136-117">For more information, see [Create a product master](tasks/create-product-master.md).</span></span>

<span data-ttu-id="80136-118">Tätä ominaisuutta ei ole otettu käyttöön tuotteille, jotka on määritetty todellisen painon prosesseille.</span><span class="sxs-lookup"><span data-stu-id="80136-118">The feature is not enabled for products that are set up for Catch Weight processes.</span></span> 

<span data-ttu-id="80136-119">Ota mittayksiköiden muunnos käyttöön päätuotteen luonnin aikana valitsemalla **Ota käyttöön mittayksiköiden muunnokset** -asetus **Tuotteen tiedot** -sivulla.</span><span class="sxs-lookup"><span data-stu-id="80136-119">During the creation of a product master enable unit of measure conversion by using the **Enable unit of measure conversions** option on the **Product details** page.</span></span>

<span data-ttu-id="80136-120">Kun luodaan päätuote, jolla on julkaistuja tuotevariantteja, varianttikohtaiset yksikkömuunnokset voidaan määrittää.</span><span class="sxs-lookup"><span data-stu-id="80136-120">When the product master with released products variants is created, unit conversions per variants can be set up.</span></span> <span data-ttu-id="80136-121">Yksikön muunnossivun avaava valikkovaihtoehto on tuotteen tai tuotevariantin yhteydessä seuraavilla sivuilla.</span><span class="sxs-lookup"><span data-stu-id="80136-121">You can find the menu item for opening the unit conversion page in context of a product or a product variant on the following pages.</span></span>

-   <span data-ttu-id="80136-122">**Tuotteen tiedot** -sivut</span><span class="sxs-lookup"><span data-stu-id="80136-122">**Product details** page</span></span>
-   <span data-ttu-id="80136-123">**Julkaistujen tuotteiden tiedot** -sivu</span><span class="sxs-lookup"><span data-stu-id="80136-123">**Released products details** page</span></span>
-   <span data-ttu-id="80136-124">**Vapautetut tuotevariantit** -sivu</span><span class="sxs-lookup"><span data-stu-id="80136-124">**Released product variants** page</span></span>

<span data-ttu-id="80136-125">Kun avaat **Yksikkömuunnos**-sivun päätuotteen tai vapautetun tuotevariantin yhteydessä, voit valita, haluatko määrittää tuotteelle tai tuotevariantille yksikkömuunnoksen.</span><span class="sxs-lookup"><span data-stu-id="80136-125">When you open the **Unit conversion** page in context of a product master or released product variant, you can select if you want to set up the unit conversion for the product or for a product variant.</span></span> <span data-ttu-id="80136-126">Tee se valitsemalla joko **Tuotevariantti** tai **Tuote** **Luo muunnos kohteelle** -kentässä.</span><span class="sxs-lookup"><span data-stu-id="80136-126">You do that by selecting either **Product variant** or **Product** in the **Create conversion for** field.</span></span>

### <a name="product-variant"></a><span data-ttu-id="80136-127">Tuotevariantti</span><span class="sxs-lookup"><span data-stu-id="80136-127">Product variant</span></span>

<span data-ttu-id="80136-128">Jos valitset **Tuotevariantti**, voit sitten valita, minkä variantin yksikkömuunnoksen haluat määrittää **Tuotevariantti**-kentässä.</span><span class="sxs-lookup"><span data-stu-id="80136-128">If you select **Product variant,** then you can select for which variant you want to set up the unit conversion in the **Product variant** field.</span></span>

### <a name="product"></a><span data-ttu-id="80136-129">Tuote</span><span class="sxs-lookup"><span data-stu-id="80136-129">Product</span></span>

<span data-ttu-id="80136-130">Jos valitset **Tuote**, voit määrittää päätuotteen yksikkömuunnoksen.</span><span class="sxs-lookup"><span data-stu-id="80136-130">If you select **Product**, then you can set up a unit conversion for the product master.</span></span> <span data-ttu-id="80136-131">Tätä yksikkömuunnosta käytetään kaikissa tuotevarianteissa, joissa yksikkömuunnosta ei ole määritetty.</span><span class="sxs-lookup"><span data-stu-id="80136-131">This unit conversion will apply for all product variants with no defined unit conversion.</span></span>

### <a name="example"></a><span data-ttu-id="80136-132">Esimerkki</span><span class="sxs-lookup"><span data-stu-id="80136-132">Example</span></span>

<span data-ttu-id="80136-133">Päätuotteella, **T-paita**, on neljä vapautettua tuotevarianttia: S, M, L ja XL.</span><span class="sxs-lookup"><span data-stu-id="80136-133">A product master, **T-Shirt**, has four released products variants Small, Medium, Large, and X-Large.</span></span> <span data-ttu-id="80136-134">T-paidat pakataan laatikoihin. Laatikossa voi olla viisi t-paitaa, joskin XL-koossa tilaa on kuitenkin vain neljälle t-paidalle.</span><span class="sxs-lookup"><span data-stu-id="80136-134">The T-shirts are packed in boxes and there can be five T-shirts in a box, except for the Extra-large size where there is only space for four T-shirts.</span></span>

<span data-ttu-id="80136-135">Avaa ensin **Yksikkömuunnos**-sivu **t-paidan** Vapautetun tuotteen tiedot -sivulla.</span><span class="sxs-lookup"><span data-stu-id="80136-135">First, open the **Unit conversion** page from the Release product details page for **T-shirt.**</span></span>

<span data-ttu-id="80136-136">Määritä **Yksikkömuunnos**-sivulla vapautetun XL-tuotevariantin yksikkömuunnos.</span><span class="sxs-lookup"><span data-stu-id="80136-136">On the **Unit conversion** page, set up the unit conversion for the release product variant X-Large.</span></span>

| <span data-ttu-id="80136-137">**Kenttä**</span><span class="sxs-lookup"><span data-stu-id="80136-137">**Field**</span></span>             | <span data-ttu-id="80136-138">**Asetus**</span><span class="sxs-lookup"><span data-stu-id="80136-138">**Setting**</span></span>             |
|-----------------------|-------------------------|
| <span data-ttu-id="80136-139">Luo muunnos kohteelle</span><span class="sxs-lookup"><span data-stu-id="80136-139">Create conversion for</span></span> | <span data-ttu-id="80136-140">Tuotevariantti</span><span class="sxs-lookup"><span data-stu-id="80136-140">Product variant</span></span>         |
| <span data-ttu-id="80136-141">Tuotevariantti</span><span class="sxs-lookup"><span data-stu-id="80136-141">Product variant</span></span>       | <span data-ttu-id="80136-142">T-paita : : XL : :</span><span class="sxs-lookup"><span data-stu-id="80136-142">T-Shirt : : X-Large : :</span></span> |
| <span data-ttu-id="80136-143">Yksiköstä</span><span class="sxs-lookup"><span data-stu-id="80136-143">From unit</span></span>             | <span data-ttu-id="80136-144">Laatikot</span><span class="sxs-lookup"><span data-stu-id="80136-144">Boxes</span></span>                   |
| <span data-ttu-id="80136-145">Kerroin</span><span class="sxs-lookup"><span data-stu-id="80136-145">Factor</span></span>                | <span data-ttu-id="80136-146">4</span><span class="sxs-lookup"><span data-stu-id="80136-146">4</span></span>                       |
| <span data-ttu-id="80136-147">Yksikköön</span><span class="sxs-lookup"><span data-stu-id="80136-147">To Unit</span></span>               | <span data-ttu-id="80136-148">Kappaletta</span><span class="sxs-lookup"><span data-stu-id="80136-148">Pieces</span></span>                  |

<span data-ttu-id="80136-149">Vapautetuilla S-, M- ja L-tuotevarianteilla on sama yksikkömuunnos laatikon ja kappaleen välillä, joten voit määrittää näiden tuotevarianttien yksikkömuunnoksen päätuotteessa.</span><span class="sxs-lookup"><span data-stu-id="80136-149">The Released product variants Small, Medium, and Large have the same unit conversion between the unit Box and Pieces, which means that you can define the unit conversion for these product variants on the product master.</span></span>

| <span data-ttu-id="80136-150">**Kenttä**</span><span class="sxs-lookup"><span data-stu-id="80136-150">**Field**</span></span>             | <span data-ttu-id="80136-151">**Asetus**</span><span class="sxs-lookup"><span data-stu-id="80136-151">**Setting**</span></span> |
|-----------------------|-------------|
| <span data-ttu-id="80136-152">Luo muunnos kohteelle</span><span class="sxs-lookup"><span data-stu-id="80136-152">Create conversion for</span></span> | <span data-ttu-id="80136-153">Tuote</span><span class="sxs-lookup"><span data-stu-id="80136-153">Product</span></span>     |
| <span data-ttu-id="80136-154">Tuote</span><span class="sxs-lookup"><span data-stu-id="80136-154">Product</span></span>               | <span data-ttu-id="80136-155">T-paita</span><span class="sxs-lookup"><span data-stu-id="80136-155">T-Shirt</span></span>     |
| <span data-ttu-id="80136-156">Yksiköstä</span><span class="sxs-lookup"><span data-stu-id="80136-156">From unit</span></span>             | <span data-ttu-id="80136-157">Laatikot</span><span class="sxs-lookup"><span data-stu-id="80136-157">Boxes</span></span>       |
| <span data-ttu-id="80136-158">Kerroin</span><span class="sxs-lookup"><span data-stu-id="80136-158">Factor</span></span>                | <span data-ttu-id="80136-159">5</span><span class="sxs-lookup"><span data-stu-id="80136-159">5</span></span>           |
| <span data-ttu-id="80136-160">Yksikköön</span><span class="sxs-lookup"><span data-stu-id="80136-160">To Unit</span></span>               | <span data-ttu-id="80136-161">Kappaletta</span><span class="sxs-lookup"><span data-stu-id="80136-161">Pieces</span></span>      |

### <a name="using-excel-to-update-the-unit-conversions"></a><span data-ttu-id="80136-162">Yksikkömuunnosten päivittäminen Excelin avulla</span><span class="sxs-lookup"><span data-stu-id="80136-162">Using Excel to update the unit conversions</span></span>

<span data-ttu-id="80136-163">Jos tuotteella on useita tuotevariantteja, joilla on erilaiset yksikkömuunnokset, yksikkömuunnokset kannattaa viedä **Yksikkömuunnos**-sivulta Excel-laskentataulukkoon, päivittää sitten muunnokset ja julkaista ne lopuksi takaisin Finance and Operationsiin.</span><span class="sxs-lookup"><span data-stu-id="80136-163">If a product has many product variants with different unit conversions, it's a good idea to export the unit conversions from the **Unit conversion** page to an Excel spreadsheet, update the conversions, and then publish them back to Finance and Operations.</span></span>

<span data-ttu-id="80136-164">Exceliin viennin ja muokkausten takaisin Finance and Operationsiin julkaisemisen asetus otetaan käyttöön **Yksikkömuunnos**-sivun toimintoruudun **Avaa Microsoft Officessa** -valikkovaihtoehdossa.</span><span class="sxs-lookup"><span data-stu-id="80136-164">The option to export to Excel and publish the edits back to Finance and Operations is enabled from the **Open in Microsoft office** menu item on the Action Pane on the **Unit conversion** page.</span></span>
