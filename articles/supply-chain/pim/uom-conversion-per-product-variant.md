---
title: Mittayksiköiden tuotevarianttikohtaiset muunnokset
description: Tässä ohjeaiheessa käsitellään tuotevarianttien mittayksiköiden muunnosten määrittämistä. Siinä on myös määritysesimerkki.
author: johanhoffmann
ms.date: 05/11/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: UnitOfMeasureConversion
ROBOTS: noindex, nofollow
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-04-01
ms.dyn365.ops.version: 10
ms.openlocfilehash: ed28928b0f07833d5906a68f780e3bb5bbe0bfe9
ms.sourcegitcommit: fa99a36c3d30d0c0577fd3f63ed6bf2f71599e40
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/20/2021
ms.locfileid: "5921214"
---
# <a name="unit-of-measure-conversion-per-product-variant"></a><span data-ttu-id="820bd-104">Mittayksiköiden tuotevarianttikohtaiset muunnokset</span><span class="sxs-lookup"><span data-stu-id="820bd-104">Unit of measure conversion per product variant</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="820bd-105">Tässä ohjeaiheessa käsitellään eri tuotevarianttien mittayksiköiden muunnosten määrittämistä.</span><span class="sxs-lookup"><span data-stu-id="820bd-105">This topic explains how to set up unit of measure conversions for various product variants.</span></span>

<span data-ttu-id="820bd-106">Tuotevarianttien avulla yksittäisestä tuotteesta voi luoda variaatioita sen sijaan, että luotaisiin useita ylläpidettäviä yksittäisiä tuotteita.</span><span class="sxs-lookup"><span data-stu-id="820bd-106">Instead of creating multiple individual products that must be maintained, you can use product variants to create variations of a single product.</span></span> <span data-ttu-id="820bd-107">Tuotevariantti voi olla esimeriksi tietyn kokoinen ja värinen T-paita.</span><span class="sxs-lookup"><span data-stu-id="820bd-107">For example, a product variant might be a T-shirt of a given size and color.</span></span>

<span data-ttu-id="820bd-108">Aiemmin yksikkömuunnokset voitiin määrittää vain päätuotteissa.</span><span class="sxs-lookup"><span data-stu-id="820bd-108">Previously, unit conversions could be set up only on the product master.</span></span> <span data-ttu-id="820bd-109">Tämän vuoksi kaikilla tuotevarianteilla oli samat yksikön muunnossäännöt.</span><span class="sxs-lookup"><span data-stu-id="820bd-109">Therefore, all product variants had the same unit conversion rules.</span></span> <span data-ttu-id="820bd-110">Jos *Tuotevarianttien mittamuunnosten yksikkö* -toiminto on kuitenkin otettu käyttöön ja jos T-paitoja myydään laatikoittain ja laatikkoon pakattavien T-paitojen määrä määräytyy T-paitojen koon mukaan, yksikkömuunnokset voidaan nyt määrittää T-paitojen eri kokojen ja pakkauksessa käytettyjen laatikoitten mukaan,</span><span class="sxs-lookup"><span data-stu-id="820bd-110">However, when the *Unit of measure conversions for product variants* feature is turned on, if your T-shirts are sold in boxes, and the number of T-shirts that can be packed in a box depends on the size of the T-shirts, you can now set up unit conversions between the different shirt sizes and the boxes that are used for packaging.</span></span>

## <a name="turn-on-the-feature-in-your-system"></a><span data-ttu-id="820bd-111">Toiminnon ottaminen käyttöön järjestelmässä</span><span class="sxs-lookup"><span data-stu-id="820bd-111">Turn on the feature in your system</span></span>

<span data-ttu-id="820bd-112">Jos toiminto ei vielä näy järjestelmässä valitse [Toimintojen hallinta](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) ja ota *Tuotevarianttien mittamuunnosten yksikkö* -toiminto käyttöön.</span><span class="sxs-lookup"><span data-stu-id="820bd-112">If you don't already see this feature in your system, go to [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md), and turn on the *Unit of measure conversions for product variants* feature.</span></span>

## <a name="set-up-a-product-for-unit-conversion-per-variant"></a><span data-ttu-id="820bd-113">Tuotteen varianttikohtaisen yksikkömuunnoksen määrittäminen</span><span class="sxs-lookup"><span data-stu-id="820bd-113">Set up a product for unit conversion per variant</span></span>

<span data-ttu-id="820bd-114">Tuotevariantteja voidaan luoda vain tuotteille, jotka ovat päätuotteita.</span><span class="sxs-lookup"><span data-stu-id="820bd-114">Product variants can be created only for products that are product masters.</span></span> <span data-ttu-id="820bd-115">Lisätietoja on kohdassa [Päätuotteen luominen](tasks/create-product-master.md).</span><span class="sxs-lookup"><span data-stu-id="820bd-115">For more information, see [Create a product master](tasks/create-product-master.md).</span></span> <span data-ttu-id="820bd-116">*Tuotevarianttien mittamuunnosten yksikkö* -toimintoa ei voi käyttää tuotteissa, joihin on määritetty todellisen painon prosesseja.</span><span class="sxs-lookup"><span data-stu-id="820bd-116">The *Unit of measure conversions for product variants* feature isn't available for products that are set up for catch-weight processes.</span></span>

<span data-ttu-id="820bd-117">Päätuote määritetään tukemaan varianttikohtaista yksikkömuunnosta seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="820bd-117">To configure a product master to support unit conversion per variant, follow these steps.</span></span>

1. <span data-ttu-id="820bd-118">Valitse **Tuotetietojen hallinta \> Tuotteet \> Päätuotteet**.</span><span class="sxs-lookup"><span data-stu-id="820bd-118">Go to **Product information management \> Products \> Product masters**.</span></span>
1. <span data-ttu-id="820bd-119">Päätuotteen voi luoda tai avata tuotteen **Tuotteen tiedot** -sivulla.</span><span class="sxs-lookup"><span data-stu-id="820bd-119">Create or open a product master to go to its **Product details** page.</span></span>
1. <span data-ttu-id="820bd-120">Määritä **Ota käyttöön mittayksiköiden muunnokset** -asetukseksi *Kyllä*.</span><span class="sxs-lookup"><span data-stu-id="820bd-120">Set the **Enable unit of measure conversions** option to *Yes*.</span></span>
1. <span data-ttu-id="820bd-121">Valitse toimintoruudun **Tuote**-välilehden **Asetukset**-ryhmässä **Yksikkömuunnokset**.</span><span class="sxs-lookup"><span data-stu-id="820bd-121">On the Action Pane, on the **Product** tab, in the **Set up** group, select **Unit conversions**.</span></span>
1. <span data-ttu-id="820bd-122">**Yksikkömuunnokset** -sivu avautuu.</span><span class="sxs-lookup"><span data-stu-id="820bd-122">The **Unit conversions** page opens.</span></span> <span data-ttu-id="820bd-123">Valitse yksi seuraavista välilehdistä:</span><span class="sxs-lookup"><span data-stu-id="820bd-123">Select one of the following tabs:</span></span>

    - <span data-ttu-id="820bd-124">**Luokansisäiset muunnokset** – valitse tämä välilehti, kun haluat muuntaa samaan yksikköluokkaan kuuluvia yksiköitä.</span><span class="sxs-lookup"><span data-stu-id="820bd-124">**Intra-class conversions** – Select this tab to convert between units that belong to the same unit class.</span></span>
    - <span data-ttu-id="820bd-125">**Luokkienväliset muunnokset** – valitse tämä välilehti, kun haluat muuntaa eri yksikköluokkiin kuuluvia yksiköitä.</span><span class="sxs-lookup"><span data-stu-id="820bd-125">**Inter-class conversions** – Select this tab to convert between units that belong to different unit classes.</span></span>

1. <span data-ttu-id="820bd-126">Lisää uusi yksikkömuunto valitsemalla **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="820bd-126">Select **New** to add a new unit conversion.</span></span>
1. <span data-ttu-id="820bd-127">Määritä **Luo muunnos kohteelle** -kentän arvoksi jokin seuraavista:</span><span class="sxs-lookup"><span data-stu-id="820bd-127">Set the **Create conversion for** field to one of the following values:</span></span>

    - <span data-ttu-id="820bd-128">**Tuote** – Jos valitset tämän arvon, voit määrittää päätuotteen yksikkömuunnoksen.</span><span class="sxs-lookup"><span data-stu-id="820bd-128">**Product** – If you select this value, you can set up a unit conversion for the product master.</span></span> <span data-ttu-id="820bd-129">Tätä yksikkömuunnosta käytetään kaikkien niiden tuotevarianttien varalla olevan muunnoksena, jos mitään yksikkömuunnosta ei ole määritetty.</span><span class="sxs-lookup"><span data-stu-id="820bd-129">That unit conversion will be used as a fallback for all product variants that no unit conversion is defined for.</span></span>
    - <span data-ttu-id="820bd-130">**Tuotevariantti** – Jos valitset tämän arvon, voit määrittää tietyn tuotevariantin yksikkömuunnoksen.</span><span class="sxs-lookup"><span data-stu-id="820bd-130">**Product variant** – If you select this value, you can set up a unit conversion for a specific product variant.</span></span> <span data-ttu-id="820bd-131">Valitse variantti **Tuotevariantti**-kentän avulla.</span><span class="sxs-lookup"><span data-stu-id="820bd-131">Use the **Product variant** field to select the variant.</span></span>

    <span data-ttu-id="820bd-132">![Uuden yksikkömuunnoksen lisääminen](media/uom-new-conversion.png "Uuden yksikkömuunnoksen lisääminen")</span><span class="sxs-lookup"><span data-stu-id="820bd-132">![Adding a new unit conversion](media/uom-new-conversion.png "Adding a new unit conversion")</span></span>

1. <span data-ttu-id="820bd-133">Käytä muita käytettävissä olevia kenttiä yksikkömuunnoksen määrittämiseen.</span><span class="sxs-lookup"><span data-stu-id="820bd-133">Use the other fields that are provided to set up your unit conversion.</span></span>
1. <span data-ttu-id="820bd-134">Tallenna uusi yksikkömuunnos valitsemalla **OK**.</span><span class="sxs-lookup"><span data-stu-id="820bd-134">Select **OK** to save the new unit conversion.</span></span>

> [!TIP]
> <span data-ttu-id="820bd-135">Voit avata tuotteen tai tuotevariantin **Yksikkömuunnokset**-sivun seuraavilta sivuilta:</span><span class="sxs-lookup"><span data-stu-id="820bd-135">You can open the **Unit conversions** page for a product or a product variant from any of the following pages:</span></span>
> 
> - <span data-ttu-id="820bd-136">Tuotteen tiedot</span><span class="sxs-lookup"><span data-stu-id="820bd-136">Product details</span></span>
> - <span data-ttu-id="820bd-137">Vapautettujen tuotteiden tiedot</span><span class="sxs-lookup"><span data-stu-id="820bd-137">Released products details</span></span>
> - <span data-ttu-id="820bd-138">Vapautetut tuotevariantit</span><span class="sxs-lookup"><span data-stu-id="820bd-138">Released product variants</span></span>

## <a name="example-scenario"></a><span data-ttu-id="820bd-139">Esimerkkiskenaario</span><span class="sxs-lookup"><span data-stu-id="820bd-139">Example scenario</span></span>

<span data-ttu-id="820bd-140">Tässä skenaariossa yritys myy t-paitoja, joiden koot ovat S, M, L ja XL.</span><span class="sxs-lookup"><span data-stu-id="820bd-140">In this scenario, a company sells T-shirts in sizes small, medium, large, and extra-large.</span></span> <span data-ttu-id="820bd-141">T-paita määritetään tuotteena ja eri koot määritetään kyseisen tuotteen variantteina.</span><span class="sxs-lookup"><span data-stu-id="820bd-141">The T-shirt is defined as a product, and the different sizes are defined as variants of that product.</span></span> <span data-ttu-id="820bd-142">T-paidat pakataan laatikkoihin.</span><span class="sxs-lookup"><span data-stu-id="820bd-142">The shirts are packed in boxes.</span></span> <span data-ttu-id="820bd-143">Kussakin laatikossa voi olla viisi S-, M- ja L-kokoista T-paitaa.</span><span class="sxs-lookup"><span data-stu-id="820bd-143">For sizes small, medium, and large, there can be five shirts in each box.</span></span> <span data-ttu-id="820bd-144">XL-kokoisia T-paitoja voi laatikossa olla vain neljä.</span><span class="sxs-lookup"><span data-stu-id="820bd-144">However, for size extra-large, there is space for only four shirts in each box.</span></span>

<span data-ttu-id="820bd-145">Yritys haluaa seurata eri variantteja *Kappaletta*-yksikkönä, vaikka niitä myydään *Laatikot*-yksikkönä.</span><span class="sxs-lookup"><span data-stu-id="820bd-145">The company wants to track the different variants in the *Pieces* unit, but it's selling them in the *Boxes* unit.</span></span> <span data-ttu-id="820bd-146">S-, M- ja L-kokojen varastoyksikön ja myyntiyksikön muunnos on 1 laatikko = 5 kappaletta.</span><span class="sxs-lookup"><span data-stu-id="820bd-146">For sizes small, medium, and large, the conversion between the inventory unit and the sales unit is 1 Box = 5 Pieces.</span></span> <span data-ttu-id="820bd-147">XL-kokoisten muunnos on 1 laatikko = 4 kappaletta.</span><span class="sxs-lookup"><span data-stu-id="820bd-147">For size extra-large, the conversion is 1 Box = 4 Pieces.</span></span>

1. <span data-ttu-id="820bd-148">Avaa **Yksikkömuunnokset**-sivu **T-paita**-tuotteen **Vapautetun tuotteen tiedot** -sivulla.</span><span class="sxs-lookup"><span data-stu-id="820bd-148">From the **Released product details** page for the **T-Shirt** product, open the **Unit conversions** page.</span></span>
1. <span data-ttu-id="820bd-149">Määritä **Yksikkömuunnokset**-sivulla seuraava vapautetun **XL**-tuotevariantin yksikkömuunnos.</span><span class="sxs-lookup"><span data-stu-id="820bd-149">On the **Unit conversions** page, set up the following unit conversion for the **X-Large** released product variant.</span></span>

    | <span data-ttu-id="820bd-150">Kenttä</span><span class="sxs-lookup"><span data-stu-id="820bd-150">Field</span></span>                 | <span data-ttu-id="820bd-151">Asetus</span><span class="sxs-lookup"><span data-stu-id="820bd-151">Setting</span></span>                 |
    |-----------------------|-------------------------|
    | <span data-ttu-id="820bd-152">Luo muunnos kohteelle</span><span class="sxs-lookup"><span data-stu-id="820bd-152">Create conversion for</span></span> | <span data-ttu-id="820bd-153">Tuotevariantti</span><span class="sxs-lookup"><span data-stu-id="820bd-153">Product variant</span></span>         |
    | <span data-ttu-id="820bd-154">Tuotevariantti</span><span class="sxs-lookup"><span data-stu-id="820bd-154">Product variant</span></span>       | <span data-ttu-id="820bd-155">T-paita : : XL : :</span><span class="sxs-lookup"><span data-stu-id="820bd-155">T-Shirt : : X-Large : :</span></span> |
    | <span data-ttu-id="820bd-156">Yksiköstä</span><span class="sxs-lookup"><span data-stu-id="820bd-156">From unit</span></span>             | <span data-ttu-id="820bd-157">Laatikot</span><span class="sxs-lookup"><span data-stu-id="820bd-157">Boxes</span></span>                   |
    | <span data-ttu-id="820bd-158">Kerroin</span><span class="sxs-lookup"><span data-stu-id="820bd-158">Factor</span></span>                | <span data-ttu-id="820bd-159">4</span><span class="sxs-lookup"><span data-stu-id="820bd-159">4</span></span>                       |
    | <span data-ttu-id="820bd-160">Yksikköön</span><span class="sxs-lookup"><span data-stu-id="820bd-160">To Unit</span></span>               | <span data-ttu-id="820bd-161">Kappaletta</span><span class="sxs-lookup"><span data-stu-id="820bd-161">Pieces</span></span>                  |

1. <span data-ttu-id="820bd-162">Koska **S**-, **M**- ja **L**-tuotevarianteilla on kaikilla sama yksikkömuunnos *Laatikko*- ja *Kappaleet*-yksikköjen välillä, voit määrittää niiden seuraavan yksikkömuunnoksen päätuotteessa.</span><span class="sxs-lookup"><span data-stu-id="820bd-162">Because the **Small**, **Medium**, and **Large** product variants all have the same unit conversion between the *Box* and *Pieces* units, you can define the following unit conversion for them on the product master.</span></span>

    | <span data-ttu-id="820bd-163">Kenttä</span><span class="sxs-lookup"><span data-stu-id="820bd-163">Field</span></span>                 | <span data-ttu-id="820bd-164">Asetus</span><span class="sxs-lookup"><span data-stu-id="820bd-164">Setting</span></span> |
    |-----------------------|---------|
    | <span data-ttu-id="820bd-165">Luo muunnos kohteelle</span><span class="sxs-lookup"><span data-stu-id="820bd-165">Create conversion for</span></span> | <span data-ttu-id="820bd-166">Tuote</span><span class="sxs-lookup"><span data-stu-id="820bd-166">Product</span></span> |
    | <span data-ttu-id="820bd-167">Tuote</span><span class="sxs-lookup"><span data-stu-id="820bd-167">Product</span></span>               | <span data-ttu-id="820bd-168">T-paita</span><span class="sxs-lookup"><span data-stu-id="820bd-168">T-Shirt</span></span> |
    | <span data-ttu-id="820bd-169">Yksiköstä</span><span class="sxs-lookup"><span data-stu-id="820bd-169">From unit</span></span>             | <span data-ttu-id="820bd-170">Laatikot</span><span class="sxs-lookup"><span data-stu-id="820bd-170">Boxes</span></span>   |
    | <span data-ttu-id="820bd-171">Kerroin</span><span class="sxs-lookup"><span data-stu-id="820bd-171">Factor</span></span>                | <span data-ttu-id="820bd-172">5</span><span class="sxs-lookup"><span data-stu-id="820bd-172">5</span></span>       |
    | <span data-ttu-id="820bd-173">Yksikköön</span><span class="sxs-lookup"><span data-stu-id="820bd-173">To Unit</span></span>               | <span data-ttu-id="820bd-174">Kappaletta</span><span class="sxs-lookup"><span data-stu-id="820bd-174">Pieces</span></span>  |

## <a name="using-excel-to-update-the-unit-conversions"></a><span data-ttu-id="820bd-175">Yksikkömuunnosten päivittäminen Excelin avulla</span><span class="sxs-lookup"><span data-stu-id="820bd-175">Using Excel to update the unit conversions</span></span>

<span data-ttu-id="820bd-176">Jos tuotteella on useita tuotevariantteja, joilla on erilaiset yksikkömuunnokset, yksikkömuunnokset kannattaa viedä Microsoft Excel -työkirjaan, päivittää ne siellä ja julkaista ne lopuksi takaisin Dynamics 365 Supply Chain Managementiin.</span><span class="sxs-lookup"><span data-stu-id="820bd-176">If a product has many product variants that have different unit conversions, it's a good idea to export the unit conversions to a Microsoft Excel workbook, update them, and then publish them back to Dynamics 365 Supply Chain Management.</span></span>

<span data-ttu-id="820bd-177">Yksikkömuunnokset viedään Exceliin valitsemalla **Yksikkömuunnokset**-sivun toimintoruudussa **Avaa Microsoft Officessa**.</span><span class="sxs-lookup"><span data-stu-id="820bd-177">To export unit conversions to Excel, on the **Unit conversions** page, on the Action Pane, select **Open in Microsoft Office**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="820bd-178">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="820bd-178">Additional resources</span></span>

[<span data-ttu-id="820bd-179">Mittayksiköiden hallinta</span><span class="sxs-lookup"><span data-stu-id="820bd-179">Manage units of measure</span></span>](tasks/manage-unit-measure.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]