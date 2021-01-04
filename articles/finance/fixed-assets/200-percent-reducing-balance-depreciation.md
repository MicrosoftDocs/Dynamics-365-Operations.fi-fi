---
title: Jäännöspoisto 200 prosenttia
description: Tässä artikkelissa on yleiskuvaus 200 prosentin jäännösarvon poistomenetelmästä.
author: saraschi2
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetDepreciationProfile
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 13951
ms.assetid: 69b4e010-7683-4dc2-8a06-6d572f37e903
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0474a8cecccaf1e23874458c27e0bea991140b6c
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/13/2020
ms.locfileid: "4442815"
---
# <a name="200-percent-reducing-balance-depreciation"></a><span data-ttu-id="a3739-103">Jäännöspoisto 200 prosenttia</span><span class="sxs-lookup"><span data-stu-id="a3739-103">200 percent reducing balance depreciation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a3739-104">Tässä artikkelissa on yleiskuvaus 200 prosentin jäännösarvon poistomenetelmästä.</span><span class="sxs-lookup"><span data-stu-id="a3739-104">This article gives an overview of the 200 percent reducing balance method of depreciation.</span></span>

<span data-ttu-id="a3739-105">Kun käyttöomaisuuden poistoprofiili määritetään ja **Poistoprofiilit**-sivun **Menetelmä** -kentästä valitaan **Jäännösarvo 200 %**, tähän poistoprofiiliin liitetyn käyttöomaisuuden poistoprosentti on sama kullakin poistojaksolla.</span><span class="sxs-lookup"><span data-stu-id="a3739-105">When you set up a fixed asset depreciation profile and select **200% reducing balance** in the **Method** field on the **Depreciation profiles** page, fixed assets that are assigned the depreciation profile are depreciated by the same percentage in each depreciation period.</span></span> <span data-ttu-id="a3739-106">Prosentti lasketaan omaisuuserän käyttöajan mukaan.</span><span class="sxs-lookup"><span data-stu-id="a3739-106">The percentage is calculated based on the service life of the asset.</span></span> <span data-ttu-id="a3739-107">Jos omaisuuserän käyttöaika on esimerkiksi viisi vuotta, poistoprosentti on 40 (200 % ÷ 5).</span><span class="sxs-lookup"><span data-stu-id="a3739-107">For example, if an asset has a service life of five years, the percentage is calculated as 40 percent (200% ÷ 5).</span></span> 

<span data-ttu-id="a3739-108">Tästä menetelmästä käytetään myös nimeä DDB-menetelmä.</span><span class="sxs-lookup"><span data-stu-id="a3739-108">This method is also known as double declining balance.</span></span>

<span data-ttu-id="a3739-109">Jos haluat määrittää jäännösarvoksi 200 %, valitse **Poistoprofiilit**-sivulla myös **Poistovuosi**- ja **Kausiväli**-kentän asetukset.</span><span class="sxs-lookup"><span data-stu-id="a3739-109">To set up 200% reducing balance depreciation, you must also select options in the **Depreciation year** field and the **Period frequency** field on the **Depreciation profiles** page.</span></span> <span data-ttu-id="a3739-110">**Kausiväli**-kentässä valittavissa olevat vaihtoehdot vaihtelevat **Poistovuosi**-kentässä valitun arvon mukaan.</span><span class="sxs-lookup"><span data-stu-id="a3739-110">The options that are available in the **Period frequency** field vary, depending on the value that you select in the **Depreciation year** field.</span></span>

## <a name="select-a-depreciation-year"></a><span data-ttu-id="a3739-111">Poistovuoden valitseminen</span><span class="sxs-lookup"><span data-stu-id="a3739-111">Select a depreciation year</span></span>
<span data-ttu-id="a3739-112">Voit valita **Poistoprofiilit**-sivulla **Poistovuosi**-kenttään joko **Kalenteri** tai **Tilikausi**.</span><span class="sxs-lookup"><span data-stu-id="a3739-112">You can select either **Calendar** or **Fiscal** in the **Depreciation year** field on the **Depreciation profiles** page.</span></span> <span data-ttu-id="a3739-113">Oletusarvo on **Kalenteri**.</span><span class="sxs-lookup"><span data-stu-id="a3739-113">The default value is **Calendar**.</span></span> 

<span data-ttu-id="a3739-114">Valinta määrittää, mitä valintoja **Kausiväli**-kentässä on käytettävissä.</span><span class="sxs-lookup"><span data-stu-id="a3739-114">Your selection determines the options that are available in the **Period frequency** field.</span></span> <span data-ttu-id="a3739-115">Tämä kenttäsi määrittää poiston jaksotuksen kirjauspäivät ja -määrät kalenterivuoden aikana.</span><span class="sxs-lookup"><span data-stu-id="a3739-115">This field defines the depreciation accrual posting dates and amounts throughout the calendar year.</span></span>

### <a name="calendar"></a><span data-ttu-id="a3739-116">Kalenteri</span><span class="sxs-lookup"><span data-stu-id="a3739-116">Calendar</span></span>

<span data-ttu-id="a3739-117">Voit säilyttää **Poistovuosi** -kentässä oletusarvon **Kalenteri**.</span><span class="sxs-lookup"><span data-stu-id="a3739-117">You can keep the default value in the **Depreciation year** field, **Calendar**.</span></span> 

<span data-ttu-id="a3739-118">**Kalenteri**-vaihtoehto päivittää joka vuosi poistokannan 1. tammikuuta.</span><span class="sxs-lookup"><span data-stu-id="a3739-118">The **Calendar** option updates the depreciation base on January 1 of each year.</span></span> <span data-ttu-id="a3739-119">Yleensä poisto on nettokirjanpitoarvo vähennettynä jäännösarvolla.</span><span class="sxs-lookup"><span data-stu-id="a3739-119">Typically, the depreciation is the net book value minus the scrap value.</span></span> <span data-ttu-id="a3739-120">Alla olevissa esimerkeissä poistokanta on laskentasarakkeen ensimmäisen lausekkeen osoittaja.</span><span class="sxs-lookup"><span data-stu-id="a3739-120">In the examples later in this topic, the depreciation base is the numerator in the first expression in the calculations column.</span></span> 

<span data-ttu-id="a3739-121">Jos poistovuodeksi valitaan **Kalenteri**, **Kausiväli**-kentässä ovat käytettävissä seuraavat vaihtoehdot:</span><span class="sxs-lookup"><span data-stu-id="a3739-121">If you select **Calendar** as the depreciation year, the following options are available in the **Period frequency** field:</span></span>

-   <span data-ttu-id="a3739-122">**Vuosittain** kirjaa summan 31. joulukuuta.</span><span class="sxs-lookup"><span data-stu-id="a3739-122">**Yearly** posts an amount on December 31.</span></span>
-   <span data-ttu-id="a3739-123">**Kuukausittain** kirjaa kuukausikohtaisen poiston kunkin kuun lopussa.</span><span class="sxs-lookup"><span data-stu-id="a3739-123">**Monthly** posts a monthly amount at the end of each calendar month.</span></span>
-   <span data-ttu-id="a3739-124">**Neljännesvuosittain** kirjaa neljännesvuoden poiston kalenterivuoden kunkin neljänneksen lopussa (31.3, 30.6. 30.9. ja 31.12.)</span><span class="sxs-lookup"><span data-stu-id="a3739-124">**Quarterly** posts a quarterly amount at the end of each calendar quarter (March 31, June 30, September 30, and December 31).</span></span>
-   <span data-ttu-id="a3739-125">**Puolivuosittain** kirjaa puolen vuoden summan kalenteripuolivuosittain (30.6. ja 31.12.).</span><span class="sxs-lookup"><span data-stu-id="a3739-125">**Half-Yearly** posts a half-yearly amount at the calendar half year (June 30 and December 31).</span></span>
-   <span data-ttu-id="a3739-126">**Päivittäin** kirjaa päivittäisen poistomenetelmän poistosumman käyttämällä yhtä tapahtumaa päivää kohden.</span><span class="sxs-lookup"><span data-stu-id="a3739-126">**Daily** posts the depreciation amount for the daily depreciation method by using one transaction for each day.</span></span>

### <a name="fiscal"></a><span data-ttu-id="a3739-127">Veroasiakirja</span><span class="sxs-lookup"><span data-stu-id="a3739-127">Fiscal</span></span>

<span data-ttu-id="a3739-128">Jos valitset **Poisto** vuosi-kentässä **Tilivuosi**-vaihtoehdon, 200 prosentin jäännösarvo lasketaan kirjalle määritetyn kirjanpidon vuosikalenterin tilivuoden perusteella tai **Kirjanpito**-sivulla valitun kirjanpidon vuosikalenterin perusteella.</span><span class="sxs-lookup"><span data-stu-id="a3739-128">If you select **Fiscal** in the **Depreciation** year field, 200% reducing balance depreciation is calculated based on the fiscal year for the fiscal calendar that is specified for the book, or for the fiscal calendar that is selected on the **Ledger** page.</span></span> <span data-ttu-id="a3739-129">Kirjanpidon vuosikalenterit määritetään **Kirjanpidon kalenterit** -sivulla.</span><span class="sxs-lookup"><span data-stu-id="a3739-129">Fiscal calendars are set up on the **Fiscal calendars** page.</span></span> 

<span data-ttu-id="a3739-130">Esimerkiksi tilikauden 1.7 – 30.6. poistojen laskeminen alkaa 1.7.</span><span class="sxs-lookup"><span data-stu-id="a3739-130">For example, for the fiscal year July 1 through June 30, the depreciation calculation starts on July 1.</span></span> <span data-ttu-id="a3739-131">Tilivuosi voi olla pidempi tai lyhyempi kuin 12 kuukautta.</span><span class="sxs-lookup"><span data-stu-id="a3739-131">The fiscal year can be longer or shorter than 12 months.</span></span> <span data-ttu-id="a3739-132">Poisto oikaistaan jokaisella kaudella.</span><span class="sxs-lookup"><span data-stu-id="a3739-132">The depreciation is adjusted for each period.</span></span> <span data-ttu-id="a3739-133">**Kirjanpidon kalenterit** -sivun kausien asetuksissa määritetään seuraavan tilikauden pituus.</span><span class="sxs-lookup"><span data-stu-id="a3739-133">The length of the next fiscal year is determined by the setup of periods on the **Fiscal calendars** page.</span></span> 

<span data-ttu-id="a3739-134">Jos poistovuodeksi valitaan **Tilivuosi**, **Kausiväli**-kentässä ovat valittavana seuraavat vaihtoehdot:</span><span class="sxs-lookup"><span data-stu-id="a3739-134">When **Fiscal** is selected as the depreciation year, the following options are available in the **Period frequency** field:</span></span>

-   <span data-ttu-id="a3739-135">**Vuosittain**-vaihtoehto kirjaa tilikaudelle lasketun poiston kokonaismäärän yhtenä summana tilikauden viimeisenä päivänä.</span><span class="sxs-lookup"><span data-stu-id="a3739-135">**Yearly** posts the total amount of the depreciation that is calculated for the fiscal year as one amount, on the last day of the fiscal year.</span></span>
-   <span data-ttu-id="a3739-136">**Tilikausi** kirjaa tilivuodelle lasketun poiston kokonaismäärän.</span><span class="sxs-lookup"><span data-stu-id="a3739-136">**Fiscal period** posts the total amount of the depreciation that is calculated for the fiscal year.</span></span> <span data-ttu-id="a3739-137">Summa on jaksotettu tilikausille, jotka määritetään **Kirjanpidon kalenterit** -sivulla.</span><span class="sxs-lookup"><span data-stu-id="a3739-137">This amount is accrued into the fiscal periods that are defined on the **Fiscal calendars** page.</span></span>

## <a name="example-of-200-reducing-balance-depreciation"></a><span data-ttu-id="a3739-138">Esimerkki 200 prosentin jäännöspoistosta</span><span class="sxs-lookup"><span data-stu-id="a3739-138">Example of 200% reducing balance depreciation</span></span>

|                                |        |
|--------------------------------|--------|
| <span data-ttu-id="a3739-139">Hankintakustannukset</span><span class="sxs-lookup"><span data-stu-id="a3739-139">Acquisition cost</span></span>               | <span data-ttu-id="a3739-140">11 000</span><span class="sxs-lookup"><span data-stu-id="a3739-140">11,000</span></span> |
| <span data-ttu-id="a3739-141">Jäännösarvo</span><span class="sxs-lookup"><span data-stu-id="a3739-141">Salvage value</span></span>                  | <span data-ttu-id="a3739-142">1 000</span><span class="sxs-lookup"><span data-stu-id="a3739-142">1, 000</span></span> |
| <span data-ttu-id="a3739-143">Poistokanta</span><span class="sxs-lookup"><span data-stu-id="a3739-143">Depreciation base</span></span>              | <span data-ttu-id="a3739-144">10 000</span><span class="sxs-lookup"><span data-stu-id="a3739-144">10,000</span></span> |
| <span data-ttu-id="a3739-145">Käyttöikä vuosina</span><span class="sxs-lookup"><span data-stu-id="a3739-145">Service life years</span></span>             | <span data-ttu-id="a3739-146">5</span><span class="sxs-lookup"><span data-stu-id="a3739-146">5</span></span>      |
| <span data-ttu-id="a3739-147">Vuosittainen poistoprosentti:</span><span class="sxs-lookup"><span data-stu-id="a3739-147">Yearly depreciation percentage</span></span> | <span data-ttu-id="a3739-148">40 %</span><span class="sxs-lookup"><span data-stu-id="a3739-148">40%</span></span>    |

<span data-ttu-id="a3739-149">200 %:n jäännösarvomenetelmä jakaa arvon 200 % käyttövuosilla.</span><span class="sxs-lookup"><span data-stu-id="a3739-149">The 200% reducing balance method divides 200 percent by the service life years.</span></span> <span data-ttu-id="a3739-150">Kyseinen prosentti kerrotaan käyttöomaisuuserän nettokirjanpitoarvolla, jolloin saadaan tulokseksi vuoden poistosumma.</span><span class="sxs-lookup"><span data-stu-id="a3739-150">That percentage will be multiplied by the net book value of the asset to determine the depreciation amount for the year.</span></span>

| <span data-ttu-id="a3739-151">Kausi</span><span class="sxs-lookup"><span data-stu-id="a3739-151">Period</span></span> | <span data-ttu-id="a3739-152">Vuotuisen poistomäärän laskeminen</span><span class="sxs-lookup"><span data-stu-id="a3739-152">Calculation of the yearly depreciation amount</span></span> | <span data-ttu-id="a3739-153">Kirjanpitoarvo</span><span class="sxs-lookup"><span data-stu-id="a3739-153">Book value</span></span>             | <span data-ttu-id="a3739-154">Nettokirjanpitoarvo vuoden lopussa:</span><span class="sxs-lookup"><span data-stu-id="a3739-154">Net book value at the end of the year</span></span> |
|--------|-----------------------------------------------|------------------------|---------------------------------------|
| <span data-ttu-id="a3739-155">Vuosi 1</span><span class="sxs-lookup"><span data-stu-id="a3739-155">Year 1</span></span> | <span data-ttu-id="a3739-156">(11 000 – 1 000) × 40 % = 4 000</span><span class="sxs-lookup"><span data-stu-id="a3739-156">(11,000 – 1,000) × 40% = 4,000</span></span>                | <span data-ttu-id="a3739-157">11 000 – 4 000 = 7 000</span><span class="sxs-lookup"><span data-stu-id="a3739-157">11,000 – 4,000 = 7,000</span></span> | <span data-ttu-id="a3739-158">11 000 – 1 000 – 4 000 = 6 000</span><span class="sxs-lookup"><span data-stu-id="a3739-158">11,000 – 1,000 – 4,000 = 6,000</span></span>        |
| <span data-ttu-id="a3739-159">Vuosi 2</span><span class="sxs-lookup"><span data-stu-id="a3739-159">Year 2</span></span> | <span data-ttu-id="a3739-160">6 000 × 40 % = 2 400</span><span class="sxs-lookup"><span data-stu-id="a3739-160">6,000 × 40% = 2,400</span></span>                           | <span data-ttu-id="a3739-161">7 000 – 2 400 = 4 600</span><span class="sxs-lookup"><span data-stu-id="a3739-161">7,000 – 2,400 = 4,600</span></span>  | <span data-ttu-id="a3739-162">6 000 – 2 400 = 3 600</span><span class="sxs-lookup"><span data-stu-id="a3739-162">6,000 – 2,400 = 3,600</span></span>                 |
| <span data-ttu-id="a3739-163">Vuosi 3</span><span class="sxs-lookup"><span data-stu-id="a3739-163">Year 3</span></span> | <span data-ttu-id="a3739-164">3 600 × 40 % = 1 440</span><span class="sxs-lookup"><span data-stu-id="a3739-164">3,600 × 40% = 1,440</span></span>                           | <span data-ttu-id="a3739-165">4 600 – 1 440 = 3 160</span><span class="sxs-lookup"><span data-stu-id="a3739-165">4,600 – 1,440 = 3,160</span></span>  | <span data-ttu-id="a3739-166">3 600 – 1 440 = 2 160</span><span class="sxs-lookup"><span data-stu-id="a3739-166">3,600 – 1,440 = 2,160</span></span>                 |

> [!NOTE] 
> <span data-ttu-id="a3739-167">Jos 200 %:n jäännösarvon poistomenetelmän avulla laskettu määrä on pienempi kuin tasapoistomenetelmän avulla laskettu määrä, jäljellä olevalle käyttöiälle on yleensä olemassa tasapoistomenetelmä.</span><span class="sxs-lookup"><span data-stu-id="a3739-167">Typically, when the amount that is calculated by using the 200% reducing balance depreciation method becomes less than the amount that would be calculated by using the straight line method, there is a conversion to the straight line method for the remaining life.</span></span>



