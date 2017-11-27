---
title: "Jäännöspoisto 125 prosenttia"
description: "Tässä artikkelissa on yleiskuvaus 125 prosentin jäännösarvon poistomenetelmästä."
author: saraschi2
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: AssetDepreciationProfile
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 13871
ms.assetid: 3abc263e-59d6-4f1a-986d-1be388948bd3
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 8ec88d799c44e035b6490861383557f8c3beda41
ms.contentlocale: fi-fi
ms.lasthandoff: 11/03/2017

---

# <a name="125-percent-reducing-balance-depreciation"></a><span data-ttu-id="ecc6e-103">Jäännöspoisto 125 prosenttia</span><span class="sxs-lookup"><span data-stu-id="ecc6e-103">125 percent reducing balance depreciation</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="ecc6e-104">Tässä artikkelissa on yleiskuvaus 125 prosentin jäännösarvon poistomenetelmästä.</span><span class="sxs-lookup"><span data-stu-id="ecc6e-104">This article gives an overview of the 125 percent reducing balance method of depreciation.</span></span>

<span data-ttu-id="ecc6e-105">Kun käyttöomaisuuden poistoprofiili määritetään ja **Poistoprofiilit**-sivun **Menetelmä** -kentästä valitaan **Jäännösarvo 125 %**, tähän poistoprofiiliin liitetyn käyttöomaisuuden poistoprosentti on sama kullakin poistojaksolla.</span><span class="sxs-lookup"><span data-stu-id="ecc6e-105">When you set up a fixed asset depreciation profile and select **125% reducing balance** in the **Method** field on the **Depreciation profiles** page, fixed assets that are assigned to the depreciation profile are depreciated by the same percentage in each depreciation period.</span></span> <span data-ttu-id="ecc6e-106">Tämä prosentti lasketaan omaisuuserän käyttöajan mukaan.</span><span class="sxs-lookup"><span data-stu-id="ecc6e-106">This percentage is calculated based on the service life of the asset.</span></span> <span data-ttu-id="ecc6e-107">Jos omaisuuserän käyttöaika on esimerkiksi viisi vuotta, poistoprosentti on 25 (125 % ÷ 5).</span><span class="sxs-lookup"><span data-stu-id="ecc6e-107">For example, if an asset has a service life of five years, the percentage is calculated as 25 percent (125% ÷ 5).</span></span>

<span data-ttu-id="ecc6e-108">Jos haluat määrittää jäännösarvoksi 125 %, valitse **Poistoprofiilit**-sivulla myös **Poistovuosi**- ja **Kausiväli**-kentän asetukset.</span><span class="sxs-lookup"><span data-stu-id="ecc6e-108">To set up 125% reducing balance depreciation, you must also select options in the **Depreciation year** field and the **Period frequency** field on the **Depreciation profiles** page.</span></span> <span data-ttu-id="ecc6e-109">**Kausiväli**-kentän käytettävissä olevat vaihtoehdot vaihtelevat **Poistovuosi**-kentässä valitun arvon mukaan.</span><span class="sxs-lookup"><span data-stu-id="ecc6e-109">The options that are available in the **Period frequency** field vary, depending on the value that is selected in the **Depreciation year** field.</span></span>

## <a name="select-a-depreciation-year"></a><span data-ttu-id="ecc6e-110">Poistovuoden valitseminen</span><span class="sxs-lookup"><span data-stu-id="ecc6e-110">Select a depreciation year</span></span>
<span data-ttu-id="ecc6e-111">Voit valita **Poistoprofiilit**-sivulla **Poistovuosi**-kenttään joko **Kalenteri** tai **Tilikausi**.</span><span class="sxs-lookup"><span data-stu-id="ecc6e-111">You can select either **Calendar** or **Fiscal** in the **Depreciation year** field on the **Depreciation profiles** page.</span></span> <span data-ttu-id="ecc6e-112">Oletusarvo on **Kalenteri**.</span><span class="sxs-lookup"><span data-stu-id="ecc6e-112">The default value is **Calendar**.</span></span> 

<span data-ttu-id="ecc6e-113">Valinta määrittää, mitä valintoja **Kausiväli**-kentässä on käytettävissä.</span><span class="sxs-lookup"><span data-stu-id="ecc6e-113">Your selection determines the options that are available in the **Period frequency** field.</span></span> <span data-ttu-id="ecc6e-114">Tämä kenttäsi määrittää poiston jaksotuksen kirjauspäivät ja -määrät kalenterivuoden aikana.</span><span class="sxs-lookup"><span data-stu-id="ecc6e-114">This field defines the depreciation accrual posting dates and amounts throughout the calendar year.</span></span>

### <a name="calendar"></a><span data-ttu-id="ecc6e-115">Kalenteri</span><span class="sxs-lookup"><span data-stu-id="ecc6e-115">Calendar</span></span>

<span data-ttu-id="ecc6e-116">Voit säilyttää **Poistovuosi** -kentässä oletusarvon **Kalenteri**.</span><span class="sxs-lookup"><span data-stu-id="ecc6e-116">You can keep the default value in the **Depreciation year** field, **Calendar**.</span></span> 

<span data-ttu-id="ecc6e-117">**Kalenteri**-vaihtoehto päivittää joka vuosi poistokannan 1. tammikuuta.</span><span class="sxs-lookup"><span data-stu-id="ecc6e-117">The **Calendar** option updates the depreciation base on January 1 of each year.</span></span> <span data-ttu-id="ecc6e-118">Yleensä poistokanta on nettokirjanpitoarvo vähennettynä jäännösarvolla.</span><span class="sxs-lookup"><span data-stu-id="ecc6e-118">Typically, the depreciation base is the net book value minus the scrap value.</span></span> <span data-ttu-id="ecc6e-119">Alla olevissa esimerkeissä poistokanta on laskentasarakkeen ensimmäisen lausekkeen osoittaja.</span><span class="sxs-lookup"><span data-stu-id="ecc6e-119">In the examples later in this topic, the depreciation base is the numerator in the first expression in the calculations column.</span></span> 

<span data-ttu-id="ecc6e-120">Jos poistovuodeksi valitaan **Kalenteri**, **Kausiväli**-kentässä ovat käytettävissä seuraavat vaihtoehdot:</span><span class="sxs-lookup"><span data-stu-id="ecc6e-120">If you select **Calendar** as the depreciation year, the following options are available in the **Period frequency** field:</span></span>

-   <span data-ttu-id="ecc6e-121">**Vuosittain** kirjaa summan 31. joulukuuta.</span><span class="sxs-lookup"><span data-stu-id="ecc6e-121">**Yearly** posts an amount on December 31.</span></span>
-   <span data-ttu-id="ecc6e-122">**Kuukausittain** kirjaa kuukausikohtaisen poiston kunkin kuun lopussa.</span><span class="sxs-lookup"><span data-stu-id="ecc6e-122">**Monthly** posts a monthly amount at the end of each calendar month.</span></span>
-   <span data-ttu-id="ecc6e-123">**Neljännesvuosittain** kirjaa neljännesvuoden poiston kalenterivuoden kunkin neljänneksen lopussa (31.3, 30.6. 30.9. ja 31.12.)</span><span class="sxs-lookup"><span data-stu-id="ecc6e-123">**Quarterly** posts a quarterly amount at the end of each calendar quarter (March 31, June 30, September 30, and December 31).</span></span>
-   <span data-ttu-id="ecc6e-124">**Puolivuosittain** kirjaa puolen vuoden summan kalenteripuolivuosittain (30.6. ja 31.12.).</span><span class="sxs-lookup"><span data-stu-id="ecc6e-124">**Half-Yearly** posts a half-yearly amount at the calendar half year (June 30 and December 31).</span></span>
-   <span data-ttu-id="ecc6e-125">**Päivittäin** kirjaa päivittäisen poistomenetelmän poistosumman käyttämällä yhtä tapahtumaa päivää kohden.</span><span class="sxs-lookup"><span data-stu-id="ecc6e-125">**Daily** posts the depreciation amount for the daily depreciation method by using one transaction for each day.</span></span>

### <a name="fiscal"></a><span data-ttu-id="ecc6e-126">Veroasiakirja</span><span class="sxs-lookup"><span data-stu-id="ecc6e-126">Fiscal</span></span>

<span data-ttu-id="ecc6e-127">Jos valitset **Poistovuosi**-kentässä **Tilivuosi**-vaihtoehdon, 125 prosentin poisto lasketaan kirjalle määritetyn kirjanpidon vuosikalenterin tilivuoden perusteella tai **Kirjanpito**-sivulla valitun kirjanpidon vuosikalenterin perusteella.</span><span class="sxs-lookup"><span data-stu-id="ecc6e-127">If you select **Fiscal** in the **Depreciation year** field, 125% reducing depreciation is calculated based on the fiscal year for the fiscal calendar that is specified for the book, or for the fiscal calendar that is selected on the **Ledger** page.</span></span> <span data-ttu-id="ecc6e-128">Kirjanpidon vuosikalenterit määritetään **Kirjanpidon kalenterit** -sivulla.</span><span class="sxs-lookup"><span data-stu-id="ecc6e-128">Fiscal calendars are set up on the **Fiscal calendars** page.</span></span> 

<span data-ttu-id="ecc6e-129">Esimerkiksi tilikauden 1.7 – 30.6. poistojen laskeminen alkaa 1.7.</span><span class="sxs-lookup"><span data-stu-id="ecc6e-129">For example, for the fiscal year July 1 through June 30, the depreciation calculation starts on July 1.</span></span> <span data-ttu-id="ecc6e-130">Tilivuosi voi olla pidempi tai lyhyempi kuin 12 kuukautta.</span><span class="sxs-lookup"><span data-stu-id="ecc6e-130">The fiscal year can be longer or shorter than 12 months.</span></span> <span data-ttu-id="ecc6e-131">Poisto säätyy automaattisesti kutakin tilijaksoa varten ja seuraavan tilivuoden pituus määräytyy **Kirjanpidon kalenterit**-lomakkeessa määritetyistä tilijaksojen asetuksista.</span><span class="sxs-lookup"><span data-stu-id="ecc6e-131">The depreciation is automatically adjusted for each period, and the length of the next fiscal year is determined by the setup of periods on the **Fiscal calendars** page.</span></span> 

<span data-ttu-id="ecc6e-132">Jos valitset poistovuodeksi **Tilivuosi**, seuraavat vaihtoehdot ovat valittavissa **Kausiväli**-kentässä:</span><span class="sxs-lookup"><span data-stu-id="ecc6e-132">If you select **Fiscal** as the depreciation year, the following options are available in the **Period frequency** field:</span></span>

-   <span data-ttu-id="ecc6e-133">**Vuosittain**-vaihtoehto kirjaa tilikaudelle lasketun poiston kokonaismäärän yhtenä summana tilikauden viimeisenä päivänä.</span><span class="sxs-lookup"><span data-stu-id="ecc6e-133">**Yearly** posts the total amount of the depreciation that is calculated for the fiscal year as one amount, on the last day of the fiscal year.</span></span>
-   <span data-ttu-id="ecc6e-134">**Tilikausi** kirjaa tilivuodelle lasketun poiston kokonaismäärän.</span><span class="sxs-lookup"><span data-stu-id="ecc6e-134">**Fiscal period** posts the total amount of the depreciation that is calculated for the fiscal year.</span></span> <span data-ttu-id="ecc6e-135">Summa on jaksotettu tilikausille, jotka määritetään **Kirjanpidon kalenterit** -sivulla.</span><span class="sxs-lookup"><span data-stu-id="ecc6e-135">This amount is accrued into the fiscal periods that are defined on the **Fiscal calendars** page.</span></span>

## <a name="example-of-125-reducing-balance-depreciation"></a><span data-ttu-id="ecc6e-136">Esimerkki 125 prosentin jäännöspoistosta</span><span class="sxs-lookup"><span data-stu-id="ecc6e-136">Example of 125% reducing balance depreciation</span></span>
|                                |        |
|--------------------------------|--------|
| <span data-ttu-id="ecc6e-137">Hankintakustannukset</span><span class="sxs-lookup"><span data-stu-id="ecc6e-137">Acquisition cost</span></span>               | <span data-ttu-id="ecc6e-138">11 000</span><span class="sxs-lookup"><span data-stu-id="ecc6e-138">11,000</span></span> |
| <span data-ttu-id="ecc6e-139">Jäännösarvo</span><span class="sxs-lookup"><span data-stu-id="ecc6e-139">Salvage value</span></span>                  | <span data-ttu-id="ecc6e-140">1 000</span><span class="sxs-lookup"><span data-stu-id="ecc6e-140">1,000</span></span>  |
| <span data-ttu-id="ecc6e-141">Poistokanta</span><span class="sxs-lookup"><span data-stu-id="ecc6e-141">Depreciation base</span></span>              | <span data-ttu-id="ecc6e-142">10 000</span><span class="sxs-lookup"><span data-stu-id="ecc6e-142">10,000</span></span> |
| <span data-ttu-id="ecc6e-143">Käyttöikä vuosina</span><span class="sxs-lookup"><span data-stu-id="ecc6e-143">Service life years</span></span>             | <span data-ttu-id="ecc6e-144">5</span><span class="sxs-lookup"><span data-stu-id="ecc6e-144">5</span></span>      |
| <span data-ttu-id="ecc6e-145">Vuosittainen poistoprosentti:</span><span class="sxs-lookup"><span data-stu-id="ecc6e-145">Yearly depreciation percentage</span></span> | <span data-ttu-id="ecc6e-146">25 %</span><span class="sxs-lookup"><span data-stu-id="ecc6e-146">25%</span></span>    |

<span data-ttu-id="ecc6e-147">125 %:n jäännösarvomenetelmä jakaa arvon 125 % käyttövuosilla.</span><span class="sxs-lookup"><span data-stu-id="ecc6e-147">The 125% reducing balance method divides 125 percent by the service life years.</span></span> <span data-ttu-id="ecc6e-148">Kyseinen prosentti kerrotaan käyttöomaisuuserän nettokirjanpitoarvolla, jolloin saadaan tulokseksi vuoden poistosumma.</span><span class="sxs-lookup"><span data-stu-id="ecc6e-148">That percentage will be multiplied by the net book value of the asset to determine the depreciation amount for the year.</span></span>

| <span data-ttu-id="ecc6e-149">Kausi</span><span class="sxs-lookup"><span data-stu-id="ecc6e-149">Period</span></span> | <span data-ttu-id="ecc6e-150">Vuotuisen poistomäärän laskeminen</span><span class="sxs-lookup"><span data-stu-id="ecc6e-150">Calculation of the yearly depreciation amount</span></span> | <span data-ttu-id="ecc6e-151">Kirjanpitoarvo</span><span class="sxs-lookup"><span data-stu-id="ecc6e-151">Book value</span></span>                    | <span data-ttu-id="ecc6e-152">Nettokirjanpitoarvo vuoden lopussa:</span><span class="sxs-lookup"><span data-stu-id="ecc6e-152">Net book value at the end of the year</span></span> |
|--------|-----------------------------------------------|-------------------------------|---------------------------------------|
| <span data-ttu-id="ecc6e-153">Vuosi 1</span><span class="sxs-lookup"><span data-stu-id="ecc6e-153">Year 1</span></span> | <span data-ttu-id="ecc6e-154">(11 000 – 1 000) × 25% = 2 500</span><span class="sxs-lookup"><span data-stu-id="ecc6e-154">(11,000 – 1,000) × 25% = 2,500</span></span>                | <span data-ttu-id="ecc6e-155">(11 000 – 2 500) = 8 500</span><span class="sxs-lookup"><span data-stu-id="ecc6e-155">(11,000 – 2,500) = 8,500</span></span>      | <span data-ttu-id="ecc6e-156">(11 000 – 1 000 – 2 500) = 7 500</span><span class="sxs-lookup"><span data-stu-id="ecc6e-156">(11,000 – 1,000 – 2,500) = 7,500</span></span>      |
| <span data-ttu-id="ecc6e-157">Vuosi 2</span><span class="sxs-lookup"><span data-stu-id="ecc6e-157">Year 2</span></span> | <span data-ttu-id="ecc6e-158">7 500 × 25 % = 1 875</span><span class="sxs-lookup"><span data-stu-id="ecc6e-158">7,500 × 25% = 1,875</span></span>                           | <span data-ttu-id="ecc6e-159">(8 500 – 1 875) = 6 625</span><span class="sxs-lookup"><span data-stu-id="ecc6e-159">(8,500 – 1,875) = 6,625</span></span>       | <span data-ttu-id="ecc6e-160">(7 500 – 1 875) = 5 625</span><span class="sxs-lookup"><span data-stu-id="ecc6e-160">(7,500 – 1,875) = 5,625</span></span>               |
| <span data-ttu-id="ecc6e-161">Vuosi 3</span><span class="sxs-lookup"><span data-stu-id="ecc6e-161">Year 3</span></span> | <span data-ttu-id="ecc6e-162">5 625 × 25 % = 1 406,25</span><span class="sxs-lookup"><span data-stu-id="ecc6e-162">5,625 × 25% = 1,406.25</span></span>                        | <span data-ttu-id="ecc6e-163">(6 625 – 1 406,25) = 5 218,75</span><span class="sxs-lookup"><span data-stu-id="ecc6e-163">(6,625 – 1,406.25) = 5,218.75</span></span> | <span data-ttu-id="ecc6e-164">(5 625 – 1 406,25) = 4 218,75</span><span class="sxs-lookup"><span data-stu-id="ecc6e-164">(5,625 – 1,406.25) = 4,218.75</span></span>         |

> [!NOTE] 
> <span data-ttu-id="ecc6e-165">Jos 125 %:n jäännösarvon poistomenetelmän avulla laskettu määrä on pienempi kuin tasapoistomenetelmän avulla laskettu määrä, jäljellä olevalle käyttöiälle on yleensä olemassa tasapoistomenetelmä.</span><span class="sxs-lookup"><span data-stu-id="ecc6e-165">Typically, when the amount that is calculated by using the 125% reducing balance depreciation method becomes less than the amount that would be calculated by using the straight line method, there is a conversion to the straight line method for the remaining life.</span></span>




