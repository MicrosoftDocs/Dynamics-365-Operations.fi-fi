---
title: Jäännöspoisto 150 prosenttia
description: Tässä artikkelissa on yleiskuvaus 150 prosentin jäännösarvon poistomenetelmästä.
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
ms.custom: 13891
ms.assetid: 36d1112d-921c-4fff-abe0-0ff2429848d3
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a132a8d6e5eaf0dad54133fc9d0c12dcf5866c7c
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/13/2020
ms.locfileid: "4442745"
---
# <a name="150-percent-reducing-balance-depreciation"></a><span data-ttu-id="f0749-103">Jäännöspoisto 150 prosenttia</span><span class="sxs-lookup"><span data-stu-id="f0749-103">150 percent reducing balance depreciation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f0749-104">Tässä artikkelissa on yleiskuvaus 150 prosentin jäännösarvon poistomenetelmästä.</span><span class="sxs-lookup"><span data-stu-id="f0749-104">This article gives an overview of the 150 percent reducing balance method of depreciation.</span></span>

<span data-ttu-id="f0749-105">Kun käyttöomaisuuden poistoprofiili määritetään ja **Poistoprofiilit**-sivun **Jäännösarvo 150 %** -kentästä valitaan **Menetelmä**, tähän poistoprofiiliin liitetyn käyttöomaisuuden poistoprosentti on sama kullakin poistojaksolla.</span><span class="sxs-lookup"><span data-stu-id="f0749-105">When you set up a fixed asset depreciation profile and select **150% reducing balance** in the **Method** field on the **Depreciation profiles** page, fixed assets that are assigned the depreciation profile are depreciated by the same percentage in each depreciation period.</span></span> <span data-ttu-id="f0749-106">Tämä prosentti lasketaan omaisuuserän käyttöajan mukaan.</span><span class="sxs-lookup"><span data-stu-id="f0749-106">This percentage is calculated based on the service life of the asset.</span></span> <span data-ttu-id="f0749-107">Jos omaisuuserän käyttöaika on esimerkiksi viisi vuotta, poistoprosentti on 30 (150 % ÷ 5).</span><span class="sxs-lookup"><span data-stu-id="f0749-107">For example, if an asset has a service life of five years, the percentage is calculated as 30 percent (150% ÷ 5).</span></span> 

<span data-ttu-id="f0749-108">Kun haluat määrittää jäännösarvoksi 150 %, valitse myös **Poistoprofiilit**-sivun **Poistovuosi**- ja **Kausiväli**-kenttä.</span><span class="sxs-lookup"><span data-stu-id="f0749-108">To set up 150% reducing balance depreciation, you must also select options in the **Depreciation year** field and the **Period frequency** field on the **Depreciation profiles** page.</span></span> <span data-ttu-id="f0749-109">**Kausiväli**-kentän käytettävissä olevat vaihtoehdot vaihtelevat **Poistovuosi**-kentässä valitun arvon mukaan.</span><span class="sxs-lookup"><span data-stu-id="f0749-109">The options that are available in the **Period frequency** field vary, depending on the value that is selected in the **Depreciation year** field.</span></span>

## <a name="selection-of-depreciation-year"></a><span data-ttu-id="f0749-110">Poistovuoden valitseminen</span><span class="sxs-lookup"><span data-stu-id="f0749-110">Selection of depreciation year</span></span>
<span data-ttu-id="f0749-111">Voit valita **Poistoprofiilit**-sivulla **Poistovuosi**-kenttään joko **Kalenteri** tai **Tilikausi**.</span><span class="sxs-lookup"><span data-stu-id="f0749-111">You can select either **Calendar** or **Fiscal** in the **Depreciation year** field on the **Depreciation profiles** page.</span></span> 

<span data-ttu-id="f0749-112">Oletusarvo on **Kalenteri**.</span><span class="sxs-lookup"><span data-stu-id="f0749-112">The default value is **Calendar**.</span></span> <span data-ttu-id="f0749-113">Valinta määrittää, mitä valintoja **Kausiväli**-kentässä on käytettävissä.</span><span class="sxs-lookup"><span data-stu-id="f0749-113">Your selection determines the options that are available in the **Period frequency** field.</span></span> <span data-ttu-id="f0749-114">Tämä kenttäsi määrittää poiston jaksotuksen kirjauspäivät ja -määrät kalenterivuoden aikana.</span><span class="sxs-lookup"><span data-stu-id="f0749-114">This field defines the depreciation accrual posting dates and amounts throughout the calendar year.</span></span>

### <a name="calendar"></a><span data-ttu-id="f0749-115">Kalenteri</span><span class="sxs-lookup"><span data-stu-id="f0749-115">Calendar</span></span>

<span data-ttu-id="f0749-116">Voit säilyttää **Poistovuosi** -kentässä oletusarvon **Kalenteri**.</span><span class="sxs-lookup"><span data-stu-id="f0749-116">You can keep the default value in the **Depreciation year** field, **Calendar**.</span></span> 

<span data-ttu-id="f0749-117">**Kalenteri**-vaihtoehto päivittää joka vuosi poistokannan 1. tammikuuta.</span><span class="sxs-lookup"><span data-stu-id="f0749-117">The **Calendar** option updates the depreciation base on January 1 of each year.</span></span> <span data-ttu-id="f0749-118">Yleensä poistokanta on nettokirjanpitoarvo vähennettynä jäännösarvolla.</span><span class="sxs-lookup"><span data-stu-id="f0749-118">Typically, the depreciation base is the net book value minus the scrap value.</span></span> <span data-ttu-id="f0749-119">Alla olevissa esimerkeissä poistokanta on laskentasarakkeen ensimmäisen lausekkeen osoittaja.</span><span class="sxs-lookup"><span data-stu-id="f0749-119">In the examples later in this topic, the depreciation base is the numerator in the first expression in the calculations column.</span></span> 

<span data-ttu-id="f0749-120">Jos poistovuodeksi valitaan **Kalenteri**, **Kausiväli**-kentässä ovat käytettävissä seuraavat vaihtoehdot:</span><span class="sxs-lookup"><span data-stu-id="f0749-120">If you select **Calendar** as the depreciation year, the following options are available in the **Period frequency** field:</span></span>

-   <span data-ttu-id="f0749-121">**Vuosittain** kirjaa summan 31. joulukuuta.</span><span class="sxs-lookup"><span data-stu-id="f0749-121">**Yearly** posts an amount on December 31.</span></span>
-   <span data-ttu-id="f0749-122">**Kuukausittain** kirjaa kuukausikohtaisen poiston kunkin kuun lopussa.</span><span class="sxs-lookup"><span data-stu-id="f0749-122">**Monthly** posts a monthly amount at the end of each calendar month.</span></span>
-   <span data-ttu-id="f0749-123">**Neljännesvuosittain** kirjaa neljännesvuoden poiston kalenterivuoden kunkin neljänneksen lopussa (31.3, 30.6. 30.9. ja 31.12.)</span><span class="sxs-lookup"><span data-stu-id="f0749-123">**Quarterly** posts a quarterly amount at the end of each calendar quarter (March 31, June 30, September 30, and December 31).</span></span>
-   <span data-ttu-id="f0749-124">**Puolivuosittain** kirjaa puolen vuoden summan kalenteripuolivuosittain (30.6. ja 31.12.).</span><span class="sxs-lookup"><span data-stu-id="f0749-124">**Half-Yearly** posts a half-yearly amount at the calendar half year (June 30 and December 31).</span></span>
-   <span data-ttu-id="f0749-125">**Päivittäin** kirjaa päivittäisen poistomenetelmän poistosumman käyttämällä yhtä tapahtumaa päivää kohden.</span><span class="sxs-lookup"><span data-stu-id="f0749-125">**Daily** posts the depreciation amount for the daily depreciation method by using one transaction for each day.</span></span>

### <a name="fiscal"></a><span data-ttu-id="f0749-126">Veroasiakirja</span><span class="sxs-lookup"><span data-stu-id="f0749-126">Fiscal</span></span>

<span data-ttu-id="f0749-127">Jos valitset **Poistovuosi**-kentässä **Tilivuosi**-vaihtoehdon, 150 prosentin jäännösarvo lasketaan kirjalle määritetyn kirjanpidon vuosikalenterin tilivuoden perusteella tai **Kirjanpito**-sivulla valitun kirjanpidon vuosikalenterin perusteella.</span><span class="sxs-lookup"><span data-stu-id="f0749-127">If you select **Fiscal** in the **Depreciation year** field, 150% reducing balance depreciation is calculated based on the fiscal year for the fiscal calendar that is specified for the book, or for the fiscal calendar that is selected on the **Ledger** page.</span></span> <span data-ttu-id="f0749-128">Kirjanpidon vuosikalenterit määritetään **Kirjanpidon kalenterit** -sivulla.</span><span class="sxs-lookup"><span data-stu-id="f0749-128">Fiscal calendars are set up on the **Fiscal calendars** page.</span></span> 

<span data-ttu-id="f0749-129">Esimerkiksi tilikauden 1.7 – 30.6. poistojen laskeminen alkaa 1.7.</span><span class="sxs-lookup"><span data-stu-id="f0749-129">For example, for the fiscal year July 1 through June 30, the depreciation calculation starts on July 1.</span></span> <span data-ttu-id="f0749-130">Tilivuosi voi olla pidempi tai lyhyempi kuin 12 kuukautta.</span><span class="sxs-lookup"><span data-stu-id="f0749-130">The fiscal year can be longer or shorter than 12 months.</span></span> <span data-ttu-id="f0749-131">Poisto oikaistaan jokaisella kaudella.</span><span class="sxs-lookup"><span data-stu-id="f0749-131">The depreciation is adjusted for each period.</span></span> <span data-ttu-id="f0749-132">**Kirjanpidon kalenterit** -sivun kausien asetuksissa määritetään seuraavan tilikauden pituus.</span><span class="sxs-lookup"><span data-stu-id="f0749-132">The length of the next fiscal year is determined by the setup of periods on the **Fiscal calendars** page.</span></span> 

<span data-ttu-id="f0749-133">Jos valitset poistovuodeksi **Tilivuosi**, seuraavat vaihtoehdot ovat valittavissa **Kausiväli**-kentässä:</span><span class="sxs-lookup"><span data-stu-id="f0749-133">If you select **Fiscal** as the depreciation year, the following options are available in the **Period frequency** field:</span></span>

-   <span data-ttu-id="f0749-134">**Vuosittain** kirjaa tilivuodelle lasketun poiston kokonaismäärän tilivuoden viimeisenä päivänä.</span><span class="sxs-lookup"><span data-stu-id="f0749-134">**Yearly** posts the total amount of the depreciation that is calculated for the fiscal year on the last day of the fiscal year.</span></span>
-   <span data-ttu-id="f0749-135">**Tilikausi** kirjaa tilivuodelle lasketun poiston kokonaismäärän.</span><span class="sxs-lookup"><span data-stu-id="f0749-135">**Fiscal period** posts the total amount of the depreciation that is calculated for the fiscal year.</span></span> <span data-ttu-id="f0749-136">Summa on jaksotettu tilikausille, jotka määritetään **Kirjanpidon kalenterit** -sivulla.</span><span class="sxs-lookup"><span data-stu-id="f0749-136">This amount is accrued into the fiscal periods that are defined on the **Fiscal calendars** page.</span></span>

## <a name="example-of-150-reducing-balance-depreciation"></a><span data-ttu-id="f0749-137">Esimerkki 150 %:n jäännöspoistosta</span><span class="sxs-lookup"><span data-stu-id="f0749-137">Example of 150% reducing balance depreciation</span></span>

|                                |        |
|--------------------------------|--------|
| <span data-ttu-id="f0749-138">Hankintakustannukset</span><span class="sxs-lookup"><span data-stu-id="f0749-138">Acquisition cost</span></span>               | <span data-ttu-id="f0749-139">11 000</span><span class="sxs-lookup"><span data-stu-id="f0749-139">11,000</span></span> |
| <span data-ttu-id="f0749-140">Jäännösarvo</span><span class="sxs-lookup"><span data-stu-id="f0749-140">Salvage value</span></span>                  | <span data-ttu-id="f0749-141">1 000</span><span class="sxs-lookup"><span data-stu-id="f0749-141">1,000</span></span>  |
| <span data-ttu-id="f0749-142">Poistokanta</span><span class="sxs-lookup"><span data-stu-id="f0749-142">Depreciation base</span></span>              | <span data-ttu-id="f0749-143">10 000</span><span class="sxs-lookup"><span data-stu-id="f0749-143">10,000</span></span> |
| <span data-ttu-id="f0749-144">Käyttöikä vuosina</span><span class="sxs-lookup"><span data-stu-id="f0749-144">Service life years</span></span>             | <span data-ttu-id="f0749-145">5</span><span class="sxs-lookup"><span data-stu-id="f0749-145">5</span></span>      |
| <span data-ttu-id="f0749-146">Vuosittainen poistoprosentti:</span><span class="sxs-lookup"><span data-stu-id="f0749-146">Yearly depreciation percentage</span></span> | <span data-ttu-id="f0749-147">30 %</span><span class="sxs-lookup"><span data-stu-id="f0749-147">30%</span></span>    |

<span data-ttu-id="f0749-148">150 %:n jäännösarvomenetelmä jakaa arvon 150 % käyttövuosilla.</span><span class="sxs-lookup"><span data-stu-id="f0749-148">The 150% reducing balance method divides 150 percent by the service life years.</span></span> <span data-ttu-id="f0749-149">Kyseinen prosentti kerrotaan käyttöomaisuuserän nettokirjanpitoarvolla, jolloin saadaan tulokseksi vuoden poistosumma.</span><span class="sxs-lookup"><span data-stu-id="f0749-149">That percentage will be multiplied by the net book value of the asset to determine the depreciation amount for the year.</span></span>

| <span data-ttu-id="f0749-150">Kausi</span><span class="sxs-lookup"><span data-stu-id="f0749-150">Period</span></span> | <span data-ttu-id="f0749-151">Vuotuisen poistomäärän laskeminen</span><span class="sxs-lookup"><span data-stu-id="f0749-151">Calculation of the yearly depreciation amount</span></span> | <span data-ttu-id="f0749-152">Kirjanpitoarvo</span><span class="sxs-lookup"><span data-stu-id="f0749-152">Book value</span></span>             | <span data-ttu-id="f0749-153">Nettokirjanpitoarvo vuoden lopussa:</span><span class="sxs-lookup"><span data-stu-id="f0749-153">Net book value at the end of the year</span></span> |
|--------|-----------------------------------------------|------------------------|---------------------------------------|
| <span data-ttu-id="f0749-154">Vuosi 1</span><span class="sxs-lookup"><span data-stu-id="f0749-154">Year 1</span></span> | <span data-ttu-id="f0749-155">(11 000 - 1 000) × 30 % = 3 000</span><span class="sxs-lookup"><span data-stu-id="f0749-155">(11,000 – 1,000) × 30% = 3,000</span></span>                | <span data-ttu-id="f0749-156">11 000 - 3 000 = 8 000</span><span class="sxs-lookup"><span data-stu-id="f0749-156">11,000 – 3,000 = 8,000</span></span> | <span data-ttu-id="f0749-157">11 000 - 1 000 – 3 000 = 7 000</span><span class="sxs-lookup"><span data-stu-id="f0749-157">11,000 – 1,000 – 3,000 = 7,000</span></span>        |
| <span data-ttu-id="f0749-158">Vuosi 2</span><span class="sxs-lookup"><span data-stu-id="f0749-158">Year 2</span></span> | <span data-ttu-id="f0749-159">7 000 × 30 % = 2 100</span><span class="sxs-lookup"><span data-stu-id="f0749-159">7,000 × 30% = 2,100</span></span>                           | <span data-ttu-id="f0749-160">8 000 - 2 100 = 5 900</span><span class="sxs-lookup"><span data-stu-id="f0749-160">8,000 – 2,100 = 5,900</span></span>  | <span data-ttu-id="f0749-161">7 000 - 2 100 = 4 900</span><span class="sxs-lookup"><span data-stu-id="f0749-161">7,000 – 2,100 = 4,900</span></span>                 |
| <span data-ttu-id="f0749-162">Vuosi 3</span><span class="sxs-lookup"><span data-stu-id="f0749-162">Year 3</span></span> | <span data-ttu-id="f0749-163">4 900 × 30 % = 1 470</span><span class="sxs-lookup"><span data-stu-id="f0749-163">4,900 × 30% = 1,470</span></span>                           | <span data-ttu-id="f0749-164">5 900 - 1 470 = 4 430</span><span class="sxs-lookup"><span data-stu-id="f0749-164">5,900 – 1,470 = 4,430</span></span>  | <span data-ttu-id="f0749-165">4 900 - 1 470 = 3 430</span><span class="sxs-lookup"><span data-stu-id="f0749-165">4,900 – 1,470 = 3,430</span></span>                 |

> [!NOTE]
> <span data-ttu-id="f0749-166">Jos 150 %:n jäännösarvon poistomenetelmän avulla laskettu määrä on pienempi kuin tasapoistomenetelmän avulla laskettu määrä, jäljellä olevalle käyttöiälle on yleensä olemassa tasapoistomenetelmä.</span><span class="sxs-lookup"><span data-stu-id="f0749-166">Typically, when the amount that is calculated by using the 150% reducing balance depreciation method becomes less than the amount that would be calculated by using the straight line method, there is a conversion to the straight line method for the remaining life.</span></span>



