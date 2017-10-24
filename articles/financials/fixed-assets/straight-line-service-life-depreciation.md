---
title: "Käyttöikään perustuva tasapoisto"
description: "Tässä artikkelissa on yleiskuvaus käyttöikään perustuvasta tasapoistomenetelmästä."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: AssetDepreciationProfile
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 3341
ms.assetid: ae5ceaeb-aeb7-45cd-b835-23cf9c5cf95a
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 2b8c078841ca2e4bd994bbfbbe2abb130a4cf6fa
ms.contentlocale: fi-fi
ms.lasthandoff: 09/29/2017

---

# <a name="straight-line-service-life-depreciation"></a><span data-ttu-id="55c6d-103">Käyttöikään perustuva tasapoisto</span><span class="sxs-lookup"><span data-stu-id="55c6d-103">Straight line service life depreciation</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="55c6d-104">Tässä artikkelissa on yleiskuvaus käyttöikään perustuvasta tasapoistomenetelmästä.</span><span class="sxs-lookup"><span data-stu-id="55c6d-104">This article gives an overview of the Straight line service life method of depreciation.</span></span>

<span data-ttu-id="55c6d-105">Jos määrität käyttöomaisuudelle poistoprofiilin ja valitset Tasapoisto - käyttöaika -asetuksen Poistoprofiilit-sivun Menetelmä-kentästä, niiden käyttöomaisuuserien poisto, joille on määritetty tämä poistoprofiili, perustuu käyttöomaisuuden jäljellä olevaan käyttöikään.</span><span class="sxs-lookup"><span data-stu-id="55c6d-105">When you set up a fixed asset depreciation profile and select Straight line service life in the Method field in the Depreciation profiles page, the assets that have this depreciation profile assigned to them are depreciated based on the total service life of the asset.</span></span> <span data-ttu-id="55c6d-106">Tavallisesti poiston määrä on tällöin sama kullakin poistojaksolla.</span><span class="sxs-lookup"><span data-stu-id="55c6d-106">This generally is the same depreciation amount in each depreciation period.</span></span> 

<span data-ttu-id="55c6d-107">Ero tasapoiston jäljellä olevan käyttöajan ja tasapoiston käyttöajan mukaan lasketun poiston määrässä on silloin, kun käyttöomaisuuteen kirjataan arvon muutos.</span><span class="sxs-lookup"><span data-stu-id="55c6d-107">The difference in the depreciation amount that is calculated between straight line service life remaining and straight line service life is when there is an adjustment posted to the asset.</span></span> 

<span data-ttu-id="55c6d-108">Jos haluat määrittää käyttöaikaan perustuvan tasapoiston, valitse Poistoprofiilit-sivulla myös Poistovuosi- ja Kausiväli-kenttien asetukset.</span><span class="sxs-lookup"><span data-stu-id="55c6d-108">To set up straight line service life depreciation, you must also select options in the Depreciation year and Period frequency fields in the Depreciation profiles page.</span></span>

## <a name="select-a-depreciation-year"></a><span data-ttu-id="55c6d-109">Poistovuoden valitseminen</span><span class="sxs-lookup"><span data-stu-id="55c6d-109">Select a depreciation year</span></span>
<span data-ttu-id="55c6d-110">Voit valita Poistoprofiilit-sivulla Poistovuosi-kenttään joko Kalenteri tai Tilikausi.</span><span class="sxs-lookup"><span data-stu-id="55c6d-110">You can select either Calendar or Fiscal in the Depreciation year field in the Depreciation profiles page.</span></span> <span data-ttu-id="55c6d-111">Valinta määrittää, mitä valintoja Kausiväli-kentässä on käytettävissä.</span><span class="sxs-lookup"><span data-stu-id="55c6d-111">The selection defines the options that are available in the Period frequency field.</span></span> <span data-ttu-id="55c6d-112">Oletusarvo on Kalenteri.</span><span class="sxs-lookup"><span data-stu-id="55c6d-112">The default option is Calendar.</span></span>

### <a name="calendar"></a><span data-ttu-id="55c6d-113">Kalenteri</span><span class="sxs-lookup"><span data-stu-id="55c6d-113">Calendar</span></span>

<span data-ttu-id="55c6d-114">Jos valitset Poistovuosi-kentän arvoksi Kalenterivuosi, järjestelmä olettaa kauden olevan 1. tammikuuta–31. joulukuuta, vaikka kirjanpidon vuosikalenteri olisikin määritetty toisin.</span><span class="sxs-lookup"><span data-stu-id="55c6d-114">If you select Calendar, a year of January 1 to December 31 is assumed, even if you have defined the fiscal calendar differently.</span></span> 

<span data-ttu-id="55c6d-115">Kalenteri-vaihtoehto päivittää poistokannan, joka on tavallisesti nettokirjanpitoarvo vähennettynä jäännösarvolla, kunkin vuoden tammikuun 1. päivänä.</span><span class="sxs-lookup"><span data-stu-id="55c6d-115">The Calendar option updates the depreciation base, which is typically the net book value minus the salvage value, on January 1 of each year.</span></span> <span data-ttu-id="55c6d-116">Alla olevissa esimerkeissä poistokanta on laskentasarakkeen ensimmäisen lausekkeen osoittaja.</span><span class="sxs-lookup"><span data-stu-id="55c6d-116">In the examples later in this topic, the depreciation base is the numerator in the first expression in the calculations column.</span></span> 

<span data-ttu-id="55c6d-117">Jos valitset Kalenteri-vaihtoehdon, Kausiväli-kentässä ovat käytettävissä seuraavat vaihtoehdot, jotka määrittävät poiston jaksotuksen kirjauspäivät ja -määrät kalenterivuoden aikana:</span><span class="sxs-lookup"><span data-stu-id="55c6d-117">If you select Calendar, the following options are available in the Period frequency field, which defines the depreciation accrual posting dates and amounts throughout the calendar year:</span></span>
-   <span data-ttu-id="55c6d-118">Vuosittain – summa kirjataan 31. joulukuuta.</span><span class="sxs-lookup"><span data-stu-id="55c6d-118">Yearly posts an amount on December 31.</span></span>
-   <span data-ttu-id="55c6d-119">Kuukausittain kirjaa kuukausikohtaisen poiston kunkin kuun lopussa</span><span class="sxs-lookup"><span data-stu-id="55c6d-119">Monthly posts a monthly amount at the end of each calendar month.</span></span>
-   <span data-ttu-id="55c6d-120">Neljännesvuosittain kirjaa neljännesvuoden poiston kalenterivuoden kunkin neljänneksen lopussa (31.3, 30.6. 30.9. ja 31.12.)</span><span class="sxs-lookup"><span data-stu-id="55c6d-120">Quarterly posts a quarterly amount at the end of each calendar quarter (March 31, June 30, September 30, and December 31).</span></span>
-   <span data-ttu-id="55c6d-121">Puolivuosittain – puolen vuoden summa kirjataan kunkin kalenterivuosipuolikkaan lopussa (30.6. ja 31.12.)</span><span class="sxs-lookup"><span data-stu-id="55c6d-121">Half-Yearly posts a half-yearly amount at the end of each calendar half year (June 30 and December 31).</span></span>
-   <span data-ttu-id="55c6d-122">Päivittäin kirjaa päivittäisen poistomenetelmän poistosumman yhdellä tapahtumalla päivää kohden.</span><span class="sxs-lookup"><span data-stu-id="55c6d-122">Daily posts the depreciation amount for the daily depreciation method using one transaction for each day.</span></span>

<span data-ttu-id="55c6d-123">Jos valitset esimerkiksi Vuosittain, vuoden poisto kirjataan vain kerran eli kunkin vuoden joulukuun 31. päivä.</span><span class="sxs-lookup"><span data-stu-id="55c6d-123">For example, if you select Yearly, the yearly depreciation is posted only one time, on December 31 of each year.</span></span> <span data-ttu-id="55c6d-124">Jos valitset Kuukausittain, kuukauden poisto kirjataan joka kuukausi käyttämällä 1/12 koko vuoden poistosummasta.</span><span class="sxs-lookup"><span data-stu-id="55c6d-124">If you select Monthly, the monthly depreciation is posted each month as 1/12 of the yearly depreciation amount.</span></span>

### <a name="fiscal"></a><span data-ttu-id="55c6d-125">Tilivuosi</span><span class="sxs-lookup"><span data-stu-id="55c6d-125">Fiscal</span></span>

<span data-ttu-id="55c6d-126">Jos valitset Poistovuosi-kentästä Tilivuosi-vaihtoehdon, käytetään käyttöaikaan perustuvaa tasapoistomenetelmää.</span><span class="sxs-lookup"><span data-stu-id="55c6d-126">If you select Fiscal in the Depreciation year field, the straight line service life depreciation is used.</span></span> <span data-ttu-id="55c6d-127">Se lasketaan tilivuodesta, jonka määrittää kirjalle määritetty kirjanpidon vuosikalenteri tai Kirjanpito-sivulla valittu kirjanpidon vuosikalenteri.</span><span class="sxs-lookup"><span data-stu-id="55c6d-127">It is calculated based on the fiscal year, which is defined by the fiscal calendar that is specified for the book, or by the fiscal calendar that is selected in the Ledger page.</span></span> <span data-ttu-id="55c6d-128">Kirjanpidon vuosikalenterit määritetään Kirjanpidon kalenterit -sivulla.</span><span class="sxs-lookup"><span data-stu-id="55c6d-128">Fiscal calendars are set up in the Fiscal calendars page.</span></span>

<span data-ttu-id="55c6d-129">Esimerkiksi tilikauden 1.7–30.6. poistojen laskeminen alkaa 1.7.</span><span class="sxs-lookup"><span data-stu-id="55c6d-129">For example, for fiscal year July 1 through June 30, the depreciation calculation starts on July 1.</span></span> <span data-ttu-id="55c6d-130">Tilivuosi voi olla pidempi tai lyhyempi kuin 12 kuukautta.</span><span class="sxs-lookup"><span data-stu-id="55c6d-130">The fiscal year can be longer or shorter than 12 months.</span></span> <span data-ttu-id="55c6d-131">Poisto oikaistaan automaattisesti jokaisella tilikaudella.</span><span class="sxs-lookup"><span data-stu-id="55c6d-131">The depreciation automatically is adjusted for each fiscal period.</span></span> <span data-ttu-id="55c6d-132">Seuraavan tilikauden pituus perustuu Kirjanpidon kalenterit -lomakkeessa uuden tilikauden luomisen yhteydessä määritettyihin tilikausiin.</span><span class="sxs-lookup"><span data-stu-id="55c6d-132">The length of the next fiscal year is based on the fiscal periods that you set up when you create a new fiscal year in the Fiscal calendars form.</span></span> 

<span data-ttu-id="55c6d-133">Jos valitset tilivuoden, seuraavat vaihtoehdot ovat käytettävissä Kausiväli-kentässä:</span><span class="sxs-lookup"><span data-stu-id="55c6d-133">If you select Fiscal, the following options are available in the Period frequency field:</span></span>
-   <span data-ttu-id="55c6d-134">Vuosittain-vaihtoehto kirjaa tilikaudelle lasketun poiston kokonaismäärän yhtenä summana tilikauden viimeisenä päivänä.</span><span class="sxs-lookup"><span data-stu-id="55c6d-134">Yearly posts the total amount of the depreciation that is calculated for the fiscal year as one amount on the last day of the fiscal year.</span></span>
-   <span data-ttu-id="55c6d-135">Tilikausi laskee tilivuodelle poiston kokonaismäärän. Se jaetaan kausiksi, jotka on määritetty kirjanpidon vuosikalenterille Kirjanpidon kalenterit -lomakkeessa.</span><span class="sxs-lookup"><span data-stu-id="55c6d-135">Fiscal period calculates the total amount of the depreciation for the fiscal year, which is accrued into the periods that are defined in the Fiscal calendars form for the fiscal calendar.</span></span>

## <a name="example-straight-line-depreciation-of-an-unchanged-fixed-asset"></a><span data-ttu-id="55c6d-136">Esimerkki: Muuttumattoman käyttöomaisuuden tasapoisto</span><span class="sxs-lookup"><span data-stu-id="55c6d-136">Example: Straight line depreciation of an unchanged fixed asset</span></span>
<span data-ttu-id="55c6d-137">Oletetaan, että käyttöomaisuudella on seuraavat ominaisuudet.</span><span class="sxs-lookup"><span data-stu-id="55c6d-137">Suppose that a fixed asset has the following characteristics.</span></span>

|                     |        |
|---------------------|--------|
| <span data-ttu-id="55c6d-138">Hankintakustannukset</span><span class="sxs-lookup"><span data-stu-id="55c6d-138">Acquisition cost</span></span>    | <span data-ttu-id="55c6d-139">11 000</span><span class="sxs-lookup"><span data-stu-id="55c6d-139">11,000</span></span> |
| <span data-ttu-id="55c6d-140">Jäännösarvo</span><span class="sxs-lookup"><span data-stu-id="55c6d-140">Salvage value</span></span>       | <span data-ttu-id="55c6d-141">1 000</span><span class="sxs-lookup"><span data-stu-id="55c6d-141">1,000</span></span>  |
| <span data-ttu-id="55c6d-142">Poistokanta</span><span class="sxs-lookup"><span data-stu-id="55c6d-142">Depreciation base</span></span>   | <span data-ttu-id="55c6d-143">10 000</span><span class="sxs-lookup"><span data-stu-id="55c6d-143">10,000</span></span> |
| <span data-ttu-id="55c6d-144">Käyttöikä vuosina</span><span class="sxs-lookup"><span data-stu-id="55c6d-144">Service life years</span></span>  | <span data-ttu-id="55c6d-145">5</span><span class="sxs-lookup"><span data-stu-id="55c6d-145">5</span></span>      |
| <span data-ttu-id="55c6d-146">Vuotuinen poisto</span><span class="sxs-lookup"><span data-stu-id="55c6d-146">Yearly depreciation</span></span> | <span data-ttu-id="55c6d-147">2 000</span><span class="sxs-lookup"><span data-stu-id="55c6d-147">2,000</span></span>  |

<span data-ttu-id="55c6d-148">Poiston määrä kunakin vuonna on sama.</span><span class="sxs-lookup"><span data-stu-id="55c6d-148">You get the same depreciation amount each year.</span></span> <span data-ttu-id="55c6d-149">(hankintahinta - jäännösarvo) / käyttöaika vuosina</span><span class="sxs-lookup"><span data-stu-id="55c6d-149">(Acquisition cost - Salvage value) / Service life years</span></span>

| <span data-ttu-id="55c6d-150">Jakso:</span><span class="sxs-lookup"><span data-stu-id="55c6d-150">Period</span></span> | <span data-ttu-id="55c6d-151">Vuotuisen poistomäärän laskeminen:</span><span class="sxs-lookup"><span data-stu-id="55c6d-151">Calculation of yearly depreciation amount</span></span> | <span data-ttu-id="55c6d-152">Nettokirjanpitoarvo vuoden lopussa:</span><span class="sxs-lookup"><span data-stu-id="55c6d-152">Net book value at the end of the year</span></span> |
|--------|-------------------------------------------|---------------------------------------|
| <span data-ttu-id="55c6d-153">Vuosi 1</span><span class="sxs-lookup"><span data-stu-id="55c6d-153">Year 1</span></span> | <span data-ttu-id="55c6d-154">(11 000 - 1 000) / 5 = 2 000</span><span class="sxs-lookup"><span data-stu-id="55c6d-154">(11,000 - 1,000) / 5 = 2,000</span></span>              | <span data-ttu-id="55c6d-155">9 000</span><span class="sxs-lookup"><span data-stu-id="55c6d-155">9,000</span></span>                                 |
| <span data-ttu-id="55c6d-156">Vuosi 2</span><span class="sxs-lookup"><span data-stu-id="55c6d-156">Year 2</span></span> | <span data-ttu-id="55c6d-157">(11 000 - 1 000) / 5 = 2 000</span><span class="sxs-lookup"><span data-stu-id="55c6d-157">(11,000 - 1,000) / 5 = 2,000</span></span>              | <span data-ttu-id="55c6d-158">7 000</span><span class="sxs-lookup"><span data-stu-id="55c6d-158">7,000</span></span>                                 |
| <span data-ttu-id="55c6d-159">Vuosi 3</span><span class="sxs-lookup"><span data-stu-id="55c6d-159">Year 3</span></span> | <span data-ttu-id="55c6d-160">(11 000 - 1 000) / 5 = 2 000</span><span class="sxs-lookup"><span data-stu-id="55c6d-160">(11,000 - 1,000) / 5 = 2,000</span></span>              | <span data-ttu-id="55c6d-161">5 000</span><span class="sxs-lookup"><span data-stu-id="55c6d-161">5,000</span></span>                                 |
| <span data-ttu-id="55c6d-162">Vuosi 4</span><span class="sxs-lookup"><span data-stu-id="55c6d-162">Year 4</span></span> | <span data-ttu-id="55c6d-163">(11 000 - 1 000) / 5 = 2 000</span><span class="sxs-lookup"><span data-stu-id="55c6d-163">(11,000 - 1,000) / 5 = 2,000</span></span>              | <span data-ttu-id="55c6d-164">3 000</span><span class="sxs-lookup"><span data-stu-id="55c6d-164">3,000</span></span>                                 |
| <span data-ttu-id="55c6d-165">Vuosi 5</span><span class="sxs-lookup"><span data-stu-id="55c6d-165">Year 5</span></span> | <span data-ttu-id="55c6d-166">(11 000 - 1 000) / 5 = 2 000</span><span class="sxs-lookup"><span data-stu-id="55c6d-166">(11,000 - 1,000) / 5 = 2,000</span></span>              | <span data-ttu-id="55c6d-167">1 000</span><span class="sxs-lookup"><span data-stu-id="55c6d-167">1,000</span></span>                                 |

## <a name="example-straight-line-depreciation-of-a-modified-fixed-asset"></a><span data-ttu-id="55c6d-168"> Esimerkki: Muutetun käyttöomaisuuden tasapoisto</span><span class="sxs-lookup"><span data-stu-id="55c6d-168">Example: Straight line depreciation of a modified fixed asset</span></span>

<span data-ttu-id="55c6d-169">Oletetaan, että samaan käyttöomaisuuserään lisätään vuonna 2 hankintaoikaisu, jonka arvo on 4 000.</span><span class="sxs-lookup"><span data-stu-id="55c6d-169">Suppose that you add an acquisition adjustment of 4,000 in year 2 to the same fixed asset.</span></span> 

<span data-ttu-id="55c6d-170">Hankintaoikaisun käyttöaika on sama kuin käyttöomaisuuserän käyttöaika ja se alkaa hankintahetkellä.</span><span class="sxs-lookup"><span data-stu-id="55c6d-170">The service life of the acquisition adjustment is the same as that of the fixed asset and starts at the time of its acquisition.</span></span> <span data-ttu-id="55c6d-171">Vuoden 5 lopussa on jäljellä nettokirjanpitoarvo, joka vastaa hankintaoikaisun nettokirjanpitoarvoa.</span><span class="sxs-lookup"><span data-stu-id="55c6d-171">A net book value remains at the end of year 5, corresponding to the net book value of the acquisition adjustment.</span></span> <span data-ttu-id="55c6d-172">Kunkin jakson poisto lasketaan seuraavassa taulukossa esitetyllä tavalla.</span><span class="sxs-lookup"><span data-stu-id="55c6d-172">The depreciation by period is calculated as shown in the following table.</span></span>

| <span data-ttu-id="55c6d-173">Jakso:</span><span class="sxs-lookup"><span data-stu-id="55c6d-173">Period</span></span> | <span data-ttu-id="55c6d-174">Vuotuisen poistomäärän laskeminen:</span><span class="sxs-lookup"><span data-stu-id="55c6d-174">Calculation of yearly depreciation amount</span></span> | <span data-ttu-id="55c6d-175">Nettokirjanpitoarvo vuoden lopussa:</span><span class="sxs-lookup"><span data-stu-id="55c6d-175">Net book value at the end of the year</span></span> |
|--------|-------------------------------------------|---------------------------------------|
| <span data-ttu-id="55c6d-176">Vuosi 1</span><span class="sxs-lookup"><span data-stu-id="55c6d-176">Year 1</span></span> | <span data-ttu-id="55c6d-177">10 000 / 5 = 2 000</span><span class="sxs-lookup"><span data-stu-id="55c6d-177">10,000 / 5 = 2,000</span></span>                        | <span data-ttu-id="55c6d-178">11 000 - 2 000 = 9 000</span><span class="sxs-lookup"><span data-stu-id="55c6d-178">11,000 - 2,000 = 9,000</span></span>                |
| <span data-ttu-id="55c6d-179">Vuosi 2</span><span class="sxs-lookup"><span data-stu-id="55c6d-179">Year 2</span></span> | <span data-ttu-id="55c6d-180">4 000 (hankintaoikaisu)</span><span class="sxs-lookup"><span data-stu-id="55c6d-180">4,000 (acquisition adjustment)</span></span>            | <span data-ttu-id="55c6d-181">9 000 + 4 000 =13 000</span><span class="sxs-lookup"><span data-stu-id="55c6d-181">9,000 + 4,000 =13,000</span></span>                 |
| <span data-ttu-id="55c6d-182">Vuosi 2</span><span class="sxs-lookup"><span data-stu-id="55c6d-182">Year 2</span></span> | <span data-ttu-id="55c6d-183">14 000 / 5 = 2 800</span><span class="sxs-lookup"><span data-stu-id="55c6d-183">14,000 / 5 = 2,800</span></span>                        | <span data-ttu-id="55c6d-184">13 000 - 2 800 = 10 200</span><span class="sxs-lookup"><span data-stu-id="55c6d-184">13,000 - 2,800 = 10,200</span></span>               |
| <span data-ttu-id="55c6d-185">Vuosi 3</span><span class="sxs-lookup"><span data-stu-id="55c6d-185">Year 3</span></span> | <span data-ttu-id="55c6d-186">14 000 / 5 = 2 800</span><span class="sxs-lookup"><span data-stu-id="55c6d-186">14,000 / 5 = 2,800</span></span>                        | <span data-ttu-id="55c6d-187">10 200 - 2 800 = 7 400</span><span class="sxs-lookup"><span data-stu-id="55c6d-187">10,200 - 2,800 = 7,400</span></span>                |
| <span data-ttu-id="55c6d-188">Vuosi 4</span><span class="sxs-lookup"><span data-stu-id="55c6d-188">Year 4</span></span> | <span data-ttu-id="55c6d-189">14 000 / 5 = 2 800</span><span class="sxs-lookup"><span data-stu-id="55c6d-189">14,000 / 5 = 2,800</span></span>                        | <span data-ttu-id="55c6d-190">7 400 - 2 800 = 4 600</span><span class="sxs-lookup"><span data-stu-id="55c6d-190">7,400 - 2,800 = 4,600</span></span>                 |
| <span data-ttu-id="55c6d-191">Vuosi 5</span><span class="sxs-lookup"><span data-stu-id="55c6d-191">Year 5</span></span> | <span data-ttu-id="55c6d-192">14 000 / 5 = 2 800</span><span class="sxs-lookup"><span data-stu-id="55c6d-192">14,000 / 5 = 2,800</span></span>                        | <span data-ttu-id="55c6d-193">4 600 - 2 800 = 1 800</span><span class="sxs-lookup"><span data-stu-id="55c6d-193">4,600 - 2,800 = 1,800</span></span>                 |
| <span data-ttu-id="55c6d-194">Vuosi 6</span><span class="sxs-lookup"><span data-stu-id="55c6d-194">Year 6</span></span> | <span data-ttu-id="55c6d-195">Jäljellä oleva arvo 800\*</span><span class="sxs-lookup"><span data-stu-id="55c6d-195">Remaining 800\*</span></span>                           | <span data-ttu-id="55c6d-196">1 800 – 800 = 1 000</span><span class="sxs-lookup"><span data-stu-id="55c6d-196">1,800 – 800 = 1,000</span></span>                   |

<span data-ttu-id="55c6d-197">\*Koska jäännösarvo on pienempi kuin poistosumma, kirjataan vain jäännösarvolla vähennetty jäljellä oleva summa.</span><span class="sxs-lookup"><span data-stu-id="55c6d-197">\*Because the remaining amount is less than the depreciation amount, only the remaining amount minus the salvage value is taken.</span></span>






