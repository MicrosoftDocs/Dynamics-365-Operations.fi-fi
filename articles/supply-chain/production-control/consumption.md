---
title: Laske materiaalin kulutus
description: "Tässä artikkelissa on tietoja eri asetuksista, jotka liittyvät materiaalikulutuksen laskemiseen."
author: johanhoffmann
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: BOMDesignerEditBOM, BOMTable, ProdBOM
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 53401
ms.assetid: 9cff88e4-0425-4707-9178-3c2cb10df7c2
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 8defe5735726e877f37d8595a6aaa7c3d14d226b
ms.contentlocale: fi-fi
ms.lasthandoff: 09/29/2017

---

# <a name="calculate-material-consumption"></a><span data-ttu-id="8ceb4-103">Laske materiaalin kulutus</span><span class="sxs-lookup"><span data-stu-id="8ceb4-103">Calculate material consumption</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="8ceb4-104">Tässä artikkelissa on tietoja eri asetuksista, jotka liittyvät materiaalikulutuksen laskemiseen.</span><span class="sxs-lookup"><span data-stu-id="8ceb4-104">This article provides information about various options that are related to the calculation of material consumption.</span></span> 

<span data-ttu-id="8ceb4-105">Käytettävissä ovat seuraavat materiaalikulutuksen laskemiseen liittyvät vaihtoehdot, jotka ovat saatavilla **Tuoterakenne**-sivun **Rivin tiedot** -pikavälilehden **Asetukset**- ja **Vaihekulutus**-välilehdillä.</span><span class="sxs-lookup"><span data-stu-id="8ceb4-105">The following options that are related to the calculation of material consumption are available on the **Setup** and **Step consumption** tabs on the **Line details** FastTab of the **Bill of materials** page.</span></span>

## <a name="variable-and-constant-consumption"></a><span data-ttu-id="8ceb4-106">Muuttuva ja kiinteä kulutus</span><span class="sxs-lookup"><span data-stu-id="8ceb4-106">Variable and constant consumption</span></span>
<span data-ttu-id="8ceb4-107">**Kulutus on** -kentässä voit valita, onko kulutus laskettava vakiomääränä vai vaihtelevana määränä.</span><span class="sxs-lookup"><span data-stu-id="8ceb4-107">In the **Consumption is** field, you can select whether consumption should be calculated as a constant quantity or a variable quantity.</span></span> <span data-ttu-id="8ceb4-108">Valitse **Vakio**, jos tuotannolle tarvitaan kiinteä määrä tai volyymi tuotetusta määrästä riippumatta.</span><span class="sxs-lookup"><span data-stu-id="8ceb4-108">Select **Constant** if a fixed quantity or volume is required for the production, regardless of the quantity that is produced.</span></span> <span data-ttu-id="8ceb4-109">Valitse **Muuttuva**, joka on oletusarvo, jos tarvittava valmiiden tuotteiden määrä on suhteellinen tuotettavien tavaroiden valmiiseen määrään nähden.</span><span class="sxs-lookup"><span data-stu-id="8ceb4-109">Select **Variable**, which is the default setting, if the required amount of material in the finished goods is proportional to the number of finished goods that are produced.</span></span>

## <a name="calculating-consumption-from-a-formula"></a><span data-ttu-id="8ceb4-110">Kulutuksen laskeminen kaavalla</span><span class="sxs-lookup"><span data-stu-id="8ceb4-110">Calculating consumption from a formula</span></span>
<span data-ttu-id="8ceb4-111">Voit määrittää **Kaava**-kenttään useita kaavoja materiaalikulutuksen laskentaan.</span><span class="sxs-lookup"><span data-stu-id="8ceb4-111">In the **Formula** field, you can set up various formulas for calculating material consumption.</span></span> <span data-ttu-id="8ceb4-112">Jos käytät oletusarvoa, joka on **Vakio**, kulutusta ei lasketa kaavalla.</span><span class="sxs-lookup"><span data-stu-id="8ceb4-112">If you use the default value, **Standard**, the consumption isn't calculated from a formula.</span></span> <span data-ttu-id="8ceb4-113">Seuraavia kaavoja voi käyttää **Korkeus**-, **Leveys**-, **Syvyys**-, **Tiheys**- ja **Vakio**-kenttien kanssa:</span><span class="sxs-lookup"><span data-stu-id="8ceb4-113">The following formulas work together with the **Height**, **Width**, **Depth**, **Density**, and **Constant** fields:</span></span>

-   <span data-ttu-id="8ceb4-114">Korkeus \* Vakio</span><span class="sxs-lookup"><span data-stu-id="8ceb4-114">Height \* Constant</span></span>
-   <span data-ttu-id="8ceb4-115">Korkeus \* Leveys \* Vakio</span><span class="sxs-lookup"><span data-stu-id="8ceb4-115">Height \* Width \* Constant</span></span>
-   <span data-ttu-id="8ceb4-116">Korkeus \* Leveys \* Syvyys \* Vakio</span><span class="sxs-lookup"><span data-stu-id="8ceb4-116">Height \* Width \* Depth \* Constant</span></span>
-   <span data-ttu-id="8ceb4-117">(Korkeus \* Leveys \* Syvyys / Tiheys) \* Vakio</span><span class="sxs-lookup"><span data-stu-id="8ceb4-117">(Height \* Width \* Depth / Density) \* Constant</span></span>

## <a name="rounding-up-and-multiples"></a><span data-ttu-id="8ceb4-118">Pyöristäminen ja kerrannaiset</span><span class="sxs-lookup"><span data-stu-id="8ceb4-118">Rounding up and multiples</span></span>
<span data-ttu-id="8ceb4-119">**Pyöristys**- ja **Kerrannaiset**-kenttien avulla voit pyöristää materiaalikulutuksen arvon.</span><span class="sxs-lookup"><span data-stu-id="8ceb4-119">Together, the **Rounding up** and **Multiples** fields let you round up the material consumption value.</span></span> <span data-ttu-id="8ceb4-120">Voit esimerkiksi pyöristää sen materiaalin käsittely-yksikön arvon mukaan, jossa raaka-aineet poimitaan tuotantoon.</span><span class="sxs-lookup"><span data-stu-id="8ceb4-120">For example, you can round up the value according to the handling unit in which the raw material is picked for production.</span></span> <span data-ttu-id="8ceb4-121">**Pyöristys**-kentässä voit käyttää seuraavia asetuksia: **Määrä**, **Mittaus**, ja **Kulutus**.</span><span class="sxs-lookup"><span data-stu-id="8ceb4-121">The following options are available in the **Rounding up** field: **Quantity**, **Measurement**, and **Consumption**.</span></span>

### <a name="quantity"></a><span data-ttu-id="8ceb4-122">Määrä</span><span class="sxs-lookup"><span data-stu-id="8ceb4-122">Quantity</span></span>

<span data-ttu-id="8ceb4-123">Jos valitset pyöristysmekanismiksi **Määrän**, määrän on oltava määritetyn määrän kerrannainen.</span><span class="sxs-lookup"><span data-stu-id="8ceb4-123">If you select **Quantity** as the rounding-up mechanism, the quantity must be a multiple of the specified quantity.</span></span> <span data-ttu-id="8ceb4-124">Jos esimerkiksi tarvitaan kokonaislukuja, valitse **Kerrannaiset**-kenttään **1**.</span><span class="sxs-lookup"><span data-stu-id="8ceb4-124">For example, if whole numbers are required, select **1** in the **Multiples** field.</span></span> <span data-ttu-id="8ceb4-125">Luvut pyöristetään sitten määrään, joka on 1:llä jaollinen.</span><span class="sxs-lookup"><span data-stu-id="8ceb4-125">Numbers are then rounded up to a quantity that is divisible by 1.</span></span>

### <a name="measurement"></a><span data-ttu-id="8ceb4-126">Mittaus</span><span class="sxs-lookup"><span data-stu-id="8ceb4-126">Measurement</span></span>

<span data-ttu-id="8ceb4-127">Tavallisesti voit valita **Mittauksen** pyöristysmekanismiksi, kun raaka-aineet saapuvat tietyissä mitoissa.</span><span class="sxs-lookup"><span data-stu-id="8ceb4-127">Typically, you select **Measurement** as the rounding-up mechanism when the raw material comes in specific dimensions.</span></span> <span data-ttu-id="8ceb4-128">Lopputuotteeseen vaaditaan esimerkiksi 2 metrin metalliputkea, ja metalliputki varastoidaan 4,5 metrin mittaisena.</span><span class="sxs-lookup"><span data-stu-id="8ceb4-128">For example, a piece of 2-meter metal tube is required for a finished good, and the metal tube is stored in 4.5-meter lengths.</span></span> <span data-ttu-id="8ceb4-129">Tässä tapauksessa **Mittausta** voi käyttää pyöristysmekanismina laskemaan, kuinka monta metalliputkea tarvitaan tietyn määrän lopputuotteita valmistamiseen.</span><span class="sxs-lookup"><span data-stu-id="8ceb4-129">In this case, the **Measurement** rounding-up mechanism can be used to calculate how many metal tubes are required to produce a specific number of pieces of the finished good.</span></span> <span data-ttu-id="8ceb4-130">Tässä esimerkissä **Kaavan** -kentän arvo on **Korkeus \* Vakio**.</span><span class="sxs-lookup"><span data-stu-id="8ceb4-130">For this example, the **Formula** field is set to **Height \* Constant**.</span></span> <span data-ttu-id="8ceb4-131">**Korkeus** -kentän arvo on **2** ilmaisemaan putken pituuden, joka vaaditaan valmiissa tuotteessa.</span><span class="sxs-lookup"><span data-stu-id="8ceb4-131">The **Height** field is set to **2** to indicate the length of the tube that is required for the finished good.</span></span> <span data-ttu-id="8ceb4-132">**Kerrannainen**-kentän arvoksi tulee **4,5** osoittamaan, että putkea voi keräillä 4,5 metrin mittaisena.</span><span class="sxs-lookup"><span data-stu-id="8ceb4-132">The **Multiple** field is set to **4.5** to indicate that the tube is picked in lengths of 4.5 meters.</span></span> <span data-ttu-id="8ceb4-133">Laskenta näyttää tältä:</span><span class="sxs-lookup"><span data-stu-id="8ceb4-133">Here is the calculation:</span></span>

1.  <span data-ttu-id="8ceb4-134">Kerrannaisten summa, joka tarvitaan 10:een lopputuotteeseen: 10 ÷ 2 = 5 osaa</span><span class="sxs-lookup"><span data-stu-id="8ceb4-134">Number of multiples that are required for 10 pieces of the finished good: 10 ÷ 2 = 5 pieces</span></span>
2.  <span data-ttu-id="8ceb4-135">Kokonaiskulutus: 4,5 x 5 = 22,5 metriä metalliputkea</span><span class="sxs-lookup"><span data-stu-id="8ceb4-135">Total consumption:  4.5 × 5 = 22.5 meters of metal tube</span></span>

<span data-ttu-id="8ceb4-136">Oletamme, 0,5 metriä putkea menee hävikkiin jokaista viittä kulutettua putken osaa kohden.</span><span class="sxs-lookup"><span data-stu-id="8ceb4-136">It's assumed that 0.5 meter of tube is scrapped for every five pieces of tube that are consumed.</span></span>

### <a name="consumption"></a><span data-ttu-id="8ceb4-137">Kulutus</span><span class="sxs-lookup"><span data-stu-id="8ceb4-137">Consumption</span></span>

<span data-ttu-id="8ceb4-138">Tavallisesti valitset **Kulutuksen** pyöristysmekanismiksi, kun raaka-aine on keräiltävä kokonaisina määrinä tietystä tuotteen materiaalin käsittely-yksiköstä.</span><span class="sxs-lookup"><span data-stu-id="8ceb4-138">Typically, you select **Consumption** as the rounding-up mechanism when raw material must be picked in whole quantities of a specific handling unit of the product.</span></span> <span data-ttu-id="8ceb4-139">Esimerkiksi 2 litraa maalia käytetään yhden lopputuotekappaleen tuottamiseen, ja maali on keräiltävä 25 litran purkeissa.</span><span class="sxs-lookup"><span data-stu-id="8ceb4-139">For example, 2 quarts of paint are used to produce one piece of a finished good, and the paint is picked in 25-quart cans.</span></span> <span data-ttu-id="8ceb4-140">Tässä tapauksessa **Kulutus**-pyöristysmekanismia voi käyttää pyöristämään kulutus kokonaisiin 25 litran maalipurkkeihin.</span><span class="sxs-lookup"><span data-stu-id="8ceb4-140">In this case, the **Consumption** rounding-up mechanism can be used to round up consumption to whole numbers of 25-quart cans.</span></span> <span data-ttu-id="8ceb4-141">Tässä ovat laskutoimitukset maalin määrälle, joka tarvitaan 180 lopputuotekappaleen tuottamiseen:</span><span class="sxs-lookup"><span data-stu-id="8ceb4-141">Here is the calculation for the amount of paint that is required if 180 pieces of the finished good must be produced:</span></span>

1.  <span data-ttu-id="8ceb4-142">Vaadittu maalin määrä ilman hävikkiä: 180 x 2 = 360 litraa</span><span class="sxs-lookup"><span data-stu-id="8ceb4-142">Paint that is required, excluding scrap: 180 × 2 = 360 quarts</span></span>
2.  <span data-ttu-id="8ceb4-143">Maalipurkkien määrä: 360 ÷ 25 = 14,4, joka pyöristetään 15:een</span><span class="sxs-lookup"><span data-stu-id="8ceb4-143">Number of cans: 360 ÷ 25 = 14.4, which is rounded up to 15</span></span>
3.  <span data-ttu-id="8ceb4-144">Vaadittu maalin määrä, hävikki mukaan lukien: 15 x 25 = 375 litraa</span><span class="sxs-lookup"><span data-stu-id="8ceb4-144">Paint that is required, including scrap: 15 × 25 = 375 quarts</span></span>

## <a name="step-consumption"></a><span data-ttu-id="8ceb4-145">Vaihekulutus</span><span class="sxs-lookup"><span data-stu-id="8ceb4-145">Step consumption</span></span>
<span data-ttu-id="8ceb4-146">Vaihekulutusta käytetään määrävälien vakiokulutuksen laskennassa.</span><span class="sxs-lookup"><span data-stu-id="8ceb4-146">Step consumption is used to calculate constant consumption in quantity intervals.</span></span> <span data-ttu-id="8ceb4-147">Jos valitset **Vaihekulutus**-asetuksen **Kaava**-kentän arvoksi **Asetukset**-välilehdessä, voit lisätä tietoja vaiheista **Vaihekulutus**-välilehdellä. Kiinteä kulutettu määrä on mahdollista asettaa väleittäin tuotetun määrän mukaan.</span><span class="sxs-lookup"><span data-stu-id="8ceb4-147">If you select **Step consumption** in the **Formula** field on the **Setup** tab, you can add information about the steps on the **Step consumption** tab. The fixed consumed quantity can be set up in intervals of the produced quantity.</span></span> <span data-ttu-id="8ceb4-148">Vaihdekulutuksen voi esimerkiksi asettaa seuraavan taulukon mukaiseksi.</span><span class="sxs-lookup"><span data-stu-id="8ceb4-148">For example, step consumption is set up as shown in the following table.</span></span>

| <span data-ttu-id="8ceb4-149">Sarjasta</span><span class="sxs-lookup"><span data-stu-id="8ceb4-149">From series</span></span> | <span data-ttu-id="8ceb4-150">Määrä</span><span class="sxs-lookup"><span data-stu-id="8ceb4-150">Quantity</span></span> |
|-------------|----------|
| <span data-ttu-id="8ceb4-151">0,00</span><span class="sxs-lookup"><span data-stu-id="8ceb4-151">0.00</span></span>        | <span data-ttu-id="8ceb4-152">10,0000</span><span class="sxs-lookup"><span data-stu-id="8ceb4-152">10.0000</span></span>  |
| <span data-ttu-id="8ceb4-153">100,00</span><span class="sxs-lookup"><span data-stu-id="8ceb4-153">100.00</span></span>      | <span data-ttu-id="8ceb4-154">20,0000</span><span class="sxs-lookup"><span data-stu-id="8ceb4-154">20.0000</span></span>  |
| <span data-ttu-id="8ceb4-155">200,00</span><span class="sxs-lookup"><span data-stu-id="8ceb4-155">200.00</span></span>      | <span data-ttu-id="8ceb4-156">40,0000</span><span class="sxs-lookup"><span data-stu-id="8ceb4-156">40.0000</span></span>  |

<span data-ttu-id="8ceb4-157">Tuoterakenteen määrä on 1 ja tuotannon määrä 110.</span><span class="sxs-lookup"><span data-stu-id="8ceb4-157">The bill of materials (BOM) quantity is 1, and the production quantity is 110.</span></span> <span data-ttu-id="8ceb4-158">Kulutuksen laskentakaava on Sarjasta (Määrä) = Kulutus.</span><span class="sxs-lookup"><span data-stu-id="8ceb4-158">The formula for the consumption is From series (Quantity) = Consumption.</span></span> <span data-ttu-id="8ceb4-159">Koska tuotannon määrä on 110, se kuuluu "100-sarjaan".</span><span class="sxs-lookup"><span data-stu-id="8ceb4-159">Because the production quantity is 110, it falls into the "From 100 series."</span></span> <span data-ttu-id="8ceb4-160">Määrä on siis 20.</span><span class="sxs-lookup"><span data-stu-id="8ceb4-160">Therefore, the quantity is 20.</span></span>




