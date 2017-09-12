---
title: "Jäännöspoiston vähentäminen"
description: "Tässä artikkelissa on yleiskuvaus poiston jäännösarvopoistomenetelmästä."
author: twheeloc
manager: AnnBe
ms.date: 04/25/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: AssetDepreciationProfile
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 3281
ms.assetid: 1b86763d-d47c-4a6a-a9a6-d97a736750da
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 20d28e22e4e89d0d864a0cbeaadeb568e73e223e
ms.openlocfilehash: 9416af0efdf9b33b1de559d302a1ff4c5f530dce
ms.contentlocale: fi-fi
ms.lasthandoff: 06/29/2017


---

# <a name="reduce-balance-depreciation"></a><span data-ttu-id="b9eb3-103">Jäännöspoiston vähentäminen</span><span class="sxs-lookup"><span data-stu-id="b9eb3-103">Reduce balance depreciation</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="b9eb3-104">Tässä artikkelissa on yleiskuvaus poiston jäännösarvopoistomenetelmästä.</span><span class="sxs-lookup"><span data-stu-id="b9eb3-104">This article gives an overview of the Reducing balance method of depreciation.</span></span>

<span data-ttu-id="b9eb3-105">Kun käyttöomaisuuden poistoprofiili määritetään ja Poistoprofiilit-sivun Menetelmä-kentästä valitaan Jäännösarvo, tähän poistoprofiiliin liitettyjen käyttöomaisuuserien poistoprosentti on sama kullakin poistojaksolla.</span><span class="sxs-lookup"><span data-stu-id="b9eb3-105">When you set up a fixed asset depreciation profile and select Reducing balance in the Method field in the Depreciation profiles page, the assets that have this depreciation profile assigned to them are depreciated by the same percentage in each depreciation period.</span></span>

<span data-ttu-id="b9eb3-106">Voit määrittää jäännösarvopoiston tekemällä valinnat myös Poistoprofiilit-lomakkeen Yleinen-pikavälilehden kenttissä.</span><span class="sxs-lookup"><span data-stu-id="b9eb3-106">To set up reducing balance depreciation, you must also make selections in fields on the General FastTab of the Depreciation profiles page.</span></span> <span data-ttu-id="b9eb3-107">Valitse ensin vuosi Poistovuosi-kentässä.</span><span class="sxs-lookup"><span data-stu-id="b9eb3-107">First, select a year in the Depreciation year field.</span></span> <span data-ttu-id="b9eb3-108">Tekemäsi valinnan mukaan Kausiväli-kentässä näkyy erilaisia vaihtoehtoja, kuten seuraavissa osissa kerrotaan.</span><span class="sxs-lookup"><span data-stu-id="b9eb3-108">Depending on the selection, different options appear in the Period frequency field, as explained in the following sections.</span></span> 

<span data-ttu-id="b9eb3-109">Määritä arvo myös poistoprofiilin Prosentti-kenttään.</span><span class="sxs-lookup"><span data-stu-id="b9eb3-109">You must also enter a value in the Percentage field for the depreciation profile.</span></span> <span data-ttu-id="b9eb3-110">Jos valitset Täyspoisto-vaihtoehdon, jäljellä oleva poistokantana käytetään viimeisen poistokauden summaa, joka voi olla suuri.</span><span class="sxs-lookup"><span data-stu-id="b9eb3-110">If you select the Full depreciation option, the remaining depreciation basis is taken in the last depreciation period and could be a large amount.</span></span> <span data-ttu-id="b9eb3-111">Joissakin maissa tai joillakin alueilla ei käytetä siirtymistä tasapoistomenetelmään.</span><span class="sxs-lookup"><span data-stu-id="b9eb3-111">Some countries/regions do not use a switchover to a straight line method.</span></span> <span data-ttu-id="b9eb3-112">Vaihdos tapahtuu, kun vaihtoehtoisen poistomenetelmän summa on suurempi tai yhtä suuri kuin ensisijaisen poistoprofiilin summa ja poistosummaksi valitaan vaihtoehtoisen menetelmän summa.</span><span class="sxs-lookup"><span data-stu-id="b9eb3-112">Switchover occurs when the alternative depreciation method amount is greater than or equal to the primary depreciation profile amount, and the depreciation amount taken is the alternative method amount.</span></span> 

<span data-ttu-id="b9eb3-113">Koska käyttöomaisuus ei prosenttilaskennan avulla tule koskaan kokonaan poistetuksi, Täyspoisto-vaihtoehto on valittava, jos käyttöomaisuuserä halutaan poistaa kokonaan.</span><span class="sxs-lookup"><span data-stu-id="b9eb3-113">Because an asset will never be fully depreciated based on a percentage calculation, you must select the Full depreciation option to fully depreciate an asset.</span></span>

## <a name="select-a-depreciation-year"></a><span data-ttu-id="b9eb3-114">Poistovuoden valitseminen</span><span class="sxs-lookup"><span data-stu-id="b9eb3-114">Select a depreciation year</span></span>
<span data-ttu-id="b9eb3-115">Voit valita Poistoprofiilit-sivulla Poistovuosi-kenttään joko Kalenteri tai Tilikausi.</span><span class="sxs-lookup"><span data-stu-id="b9eb3-115">You can select either Calendar or Fiscal in the Depreciation year field in the Depreciation profiles page.</span></span> <span data-ttu-id="b9eb3-116">Valinta määrittää, mitä valintoja Kausiväli-kentässä on käytettävissä.</span><span class="sxs-lookup"><span data-stu-id="b9eb3-116">The selection defines the options that are available in the Period frequency field.</span></span> <span data-ttu-id="b9eb3-117">Oletusarvo on Kalenteri.</span><span class="sxs-lookup"><span data-stu-id="b9eb3-117">The default option is Calendar.</span></span>

### <a name="calendar"></a><span data-ttu-id="b9eb3-118">Kalenteri</span><span class="sxs-lookup"><span data-stu-id="b9eb3-118">Calendar</span></span>

<span data-ttu-id="b9eb3-119">Kalenteri-vaihtoehto päivittää poistokannan, joka on tavallisesti nettokirjanpitoarvo vähennettynä jäännösarvolla, kunkin vuoden tammikuun 1. päivänä.</span><span class="sxs-lookup"><span data-stu-id="b9eb3-119">The Calendar option updates the depreciation base, which is typically the net book value minus the scrap value, on January 1 of each year.</span></span> <span data-ttu-id="b9eb3-120">Myöhemmin tässä ohjeaiheessa olevassa jäännöspoistoesimerkeissä poistokanta on laskelmien sarakkeen ensimmäisen lausekkeen osoittaja.</span><span class="sxs-lookup"><span data-stu-id="b9eb3-120">In the reducing balance depreciation example later in this topic, the depreciation base is the numerator in the first expression in the calculations column.</span></span> 

<span data-ttu-id="b9eb3-121">Jos valitset Kalenteri-vaihtoehdon, Kausiväli-kentässä ovat käytettävissä seuraavat vaihtoehdot, jotka määrittävät poiston jaksotuksen kirjauspäivät ja -määrät kalenterivuoden aikana:</span><span class="sxs-lookup"><span data-stu-id="b9eb3-121">If you select Calendar, the following options are available in the Period frequency field, which defines the depreciation accrual posting dates and amounts throughout the calendar year:</span></span>

-   <span data-ttu-id="b9eb3-122">Vuosittain tekee kirjauksen 31. joulukuuta</span><span class="sxs-lookup"><span data-stu-id="b9eb3-122">Yearly posts on December 31.</span></span>
-   <span data-ttu-id="b9eb3-123">Kuukausittain kirjaa kuukausikohtaisen poiston kunkin kuun lopussa</span><span class="sxs-lookup"><span data-stu-id="b9eb3-123">Monthly posts a monthly amount at the end of each calendar month.</span></span>
-   <span data-ttu-id="b9eb3-124">Neljännesvuosittain kirjaa neljännesvuoden poiston kalenterivuoden kunkin neljänneksen lopussa (31.3, 30.6. 30.9. ja 31.12.)</span><span class="sxs-lookup"><span data-stu-id="b9eb3-124">Quarterly posts a quarterly amount at the end of each calendar quarter (March 31, June 30, September 30, and December 31).</span></span>
-   <span data-ttu-id="b9eb3-125">Puolivuosittain kirjaa puolen vuoden summan kunkin kalenterivuosipuolikkaan lopussa (30.6. ja 31.12.)</span><span class="sxs-lookup"><span data-stu-id="b9eb3-125">Half-Yearly posts a half-yearly amount at the end of each calendar half-year (June 30 and December 31).</span></span>
-   <span data-ttu-id="b9eb3-126">Päivittäin kirjaa päivittäisen poistomenetelmän poistosumman yhdellä tapahtumalla päivää kohden.</span><span class="sxs-lookup"><span data-stu-id="b9eb3-126">Daily posts the depreciation amount for the daily depreciation method using one transaction for each day.</span></span>

<span data-ttu-id="b9eb3-127">Jos valitset esimerkiksi Vuosittain, vuoden poisto kirjataan vain kerran eli kunkin vuoden joulukuun 31. päivä.</span><span class="sxs-lookup"><span data-stu-id="b9eb3-127">For example, if you select Yearly, the yearly depreciation is posted only one time, on December 31 of each year.</span></span> <span data-ttu-id="b9eb3-128">Jos valitset Kuukausittain, kuukauden poisto kirjataan joka kuukausi käyttämällä 1/12 koko vuoden poistosummasta.</span><span class="sxs-lookup"><span data-stu-id="b9eb3-128">If you select Monthly, the monthly depreciation is posted each month as 1/12 of the yearly depreciation amount.</span></span>

### <a name="fiscal"></a><span data-ttu-id="b9eb3-129">Tilivuosi</span><span class="sxs-lookup"><span data-stu-id="b9eb3-129">Fiscal</span></span>

<span data-ttu-id="b9eb3-130">Jos valitset Poistovuosi-kentästä Tilivuosi-vaihtoehdon, käytetään tasapoistomenetelmää.</span><span class="sxs-lookup"><span data-stu-id="b9eb3-130">If you select Fiscal in the Depreciation year field, the straight line depreciation method is used.</span></span> <span data-ttu-id="b9eb3-131">Se lasketaan Kirjanpito-sivulla valitulle tilikalenterille Kirjanpidon kalenterit -sivulla määritetyn tilivuoden perustella.</span><span class="sxs-lookup"><span data-stu-id="b9eb3-131">It is calculated based on the fiscal year, which is set up in the Fiscal calendars page for the fiscal calendar that is selected in the Ledger page.</span></span> <span data-ttu-id="b9eb3-132">Esimerkiksi tilikauden 1.7–30.6. poistojen laskeminen alkaa 1.7.</span><span class="sxs-lookup"><span data-stu-id="b9eb3-132">For example, for fiscal year July 1 through June 30, the depreciation calculation starts on July 1.</span></span> <span data-ttu-id="b9eb3-133">Tilivuosi voi olla pidempi tai lyhyempi kuin 12 kuukautta.</span><span class="sxs-lookup"><span data-stu-id="b9eb3-133">The fiscal year can be longer or shorter than 12 months.</span></span> <span data-ttu-id="b9eb3-134">Poisto oikaistaan jokaisella tilikaudella.</span><span class="sxs-lookup"><span data-stu-id="b9eb3-134">The depreciation is adjusted for each fiscal period.</span></span> <span data-ttu-id="b9eb3-135">Seuraavan tilivuoden pituus perustuu Kirjanpidon kalenterit -sivulla uuden tilivuoden luomisen yhteydessä määritettyihin tilikausiin.</span><span class="sxs-lookup"><span data-stu-id="b9eb3-135">The length of the next fiscal year is based on the fiscal periods that you set up when you create a new fiscal year in the Fiscal calendars page.</span></span>


<span data-ttu-id="b9eb3-136">Jos valitset tilivuoden, seuraavat vaihtoehdot ovat käytettävissä Kausiväli-kentässä:</span><span class="sxs-lookup"><span data-stu-id="b9eb3-136">If you select Fiscal, the following options are available in the Period frequency field:</span></span>

-   <span data-ttu-id="b9eb3-137">Kirjaa vuosittain tilivuodelle lasketun poiston kokonaismäärän yhtenä summana tilivuoden viimeisenä päivänä.</span><span class="sxs-lookup"><span data-stu-id="b9eb3-137">Yearly posts the total amount of the depreciation calculated for the fiscal year as one amount on the last day of the fiscal year.</span></span>
-   <span data-ttu-id="b9eb3-138">Tilikausi kirjaa tilikaudelle lasketun poiston kokonaismäärän, joka jaksotetaan tilikausille, jotka on määritetty Kirjanpito-sivulla valitun kirjanpidon kalenterissa tai käyttöomaisuuden kirjalle valitussa kirjanpidon kalenterissa.</span><span class="sxs-lookup"><span data-stu-id="b9eb3-138">Fiscal period posts the total amount of the depreciation calculated for the fiscal year, which is accrued into the fiscal periods that are defined for the fiscal calendar that is selected in the Ledger page, or for the fiscal calendar that is selected for the book for a fixed asset.</span></span>

## <a name="example-of-reducing-balance-depreciation"></a><span data-ttu-id="b9eb3-139">Esimerkki jäännöspoistosta</span><span class="sxs-lookup"><span data-stu-id="b9eb3-139">Example of reducing balance depreciation</span></span>

<span data-ttu-id="b9eb3-140">Oletetaan, että käyttöomaisuuserän hankintahinta on 11 000, romutusarvo on 1 000 ja poistoprosentti on 30.</span><span class="sxs-lookup"><span data-stu-id="b9eb3-140">Suppose that the fixed asset acquisition price is 11,000, the scrap value is 1,000, and the depreciation percentage factor is 30.</span></span> 

<span data-ttu-id="b9eb3-141">Jäännösarvopoisto-menetelmää käytettäessä lasketaan 30 prosenttia edellisen poistokauden lopun poistokannasta (nettokirjanpitoarvo vähennettynä romutusarvolla).</span><span class="sxs-lookup"><span data-stu-id="b9eb3-141">Using the Reducing balance method, 30 percent of the depreciation base (net book value minus scrap value) is calculated at the end of the previous depreciation period.</span></span> <span data-ttu-id="b9eb3-142">Seuraavassa taulukossa on esitetty ensimmäisten kolmen vuoden poistot.</span><span class="sxs-lookup"><span data-stu-id="b9eb3-142">Depreciation for the first three years is shown in the following table.</span></span>

| <span data-ttu-id="b9eb3-143">Kausi</span><span class="sxs-lookup"><span data-stu-id="b9eb3-143">Period</span></span> | <span data-ttu-id="b9eb3-144">Vuotuisen poistomäärän laskeminen:</span><span class="sxs-lookup"><span data-stu-id="b9eb3-144">Calculation of yearly depreciation amount</span></span> | <span data-ttu-id="b9eb3-145">Nettokirjanpitoarvo vuoden lopussa:</span><span class="sxs-lookup"><span data-stu-id="b9eb3-145">Net book value at the end of the year</span></span> |
|--------|-------------------------------------------|---------------------------------------|
| <span data-ttu-id="b9eb3-146">Vuosi 1</span><span class="sxs-lookup"><span data-stu-id="b9eb3-146">Year 1</span></span> | <span data-ttu-id="b9eb3-147">(11 000 - 1 000) \* 30 % = 3 000</span><span class="sxs-lookup"><span data-stu-id="b9eb3-147">(11,000 - 1,000) \* 30% = 3,000</span></span>           | <span data-ttu-id="b9eb3-148">(11 000 - 1 000) - 3 000 = 7 000</span><span class="sxs-lookup"><span data-stu-id="b9eb3-148">(11,000 - 1,000) - 3,000 = 7,000</span></span>      |
| <span data-ttu-id="b9eb3-149">Vuosi 2</span><span class="sxs-lookup"><span data-stu-id="b9eb3-149">Year 2</span></span> | <span data-ttu-id="b9eb3-150">(7 000 - 1 000) \* 30 % = 1 800</span><span class="sxs-lookup"><span data-stu-id="b9eb3-150">(7,000 - 1,000) \* 30% = 1,800</span></span>            | <span data-ttu-id="b9eb3-151">(7 000 -1 800) = 5 200</span><span class="sxs-lookup"><span data-stu-id="b9eb3-151">(7,000 -1,800) = 5,200</span></span>                |
| <span data-ttu-id="b9eb3-152">Vuosi 3</span><span class="sxs-lookup"><span data-stu-id="b9eb3-152">Year 3</span></span> | <span data-ttu-id="b9eb3-153">(5 200 - 1 000) \* 30 % = 1 260</span><span class="sxs-lookup"><span data-stu-id="b9eb3-153">(5,200 - 1,000) \* 30% = 1,260</span></span>            | <span data-ttu-id="b9eb3-154">(5 200 - 1 260) = 3 940</span><span class="sxs-lookup"><span data-stu-id="b9eb3-154">(5,200 - 1,260) = 3,940</span></span>               |

 
-






