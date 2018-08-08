---
title: "175 prosentin jäännöspoisto"
description: "Tässä ohjeaiheessa on yleiskuvaus 175 prosentin jäännösarvon poistomenetelmästä."
author: saraschi2
manager: AnnBe
ms.date: 10/30/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: AssetDepreciationProfile
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 13911
ms.assetid: cc5d001f-bcfe-4602-9ec1-9e265e9fd188
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: d9747ba144d56c9410846769e5465372c89ea111
ms.openlocfilehash: 2a63293dbf24c27733f8013947aeab5792fa0db9
ms.contentlocale: fi-fi
ms.lasthandoff: 08/07/2018

---

# <a name="175-percent-reducing-balance-depreciation"></a><span data-ttu-id="cc1b0-103">175 prosentin jäännöspoisto</span><span class="sxs-lookup"><span data-stu-id="cc1b0-103">175 percent reducing balance depreciation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="cc1b0-104">Tässä ohjeaiheessa on yleiskuvaus 175 prosentin jäännösarvon poistomenetelmästä.</span><span class="sxs-lookup"><span data-stu-id="cc1b0-104">This topic gives an overview of the 175 percent reducing balance method of depreciation.</span></span>

<span data-ttu-id="cc1b0-105">Kun käyttöomaisuuden poistoprofiili määritetään ja **Poistoprofiilit**-sivun **Menetelmä** -kentästä valitaan **Jäännösarvo 175 %**, tähän poistoprofiiliin liitetyn käyttöomaisuuden poistoprosentti on sama kullakin poistojaksolla.</span><span class="sxs-lookup"><span data-stu-id="cc1b0-105">When you set up a fixed asset depreciation profile and select **175% reducing balance** in the **Method** field on the **Depreciation profiles** page, fixed assets that are assigned the depreciation profile are depreciated by the same percentage in each depreciation period.</span></span> 

<span data-ttu-id="cc1b0-106">Jos haluat määrittää jäännösarvoksi 175 %, valitse **Poistoprofiilit**-sivulla myös **Poistovuosi**- ja **Kausiväli**-kentän asetukset.</span><span class="sxs-lookup"><span data-stu-id="cc1b0-106">To set up 175% reducing balance depreciation, you must also select options in the **Depreciation year** field and the **Period frequency** field on the **Depreciation profiles** page.</span></span> <span data-ttu-id="cc1b0-107">**Kausiväli**-kentän käytettävissä olevat vaihtoehdot vaihtelevat **Poistovuosi**-kentässä valitun arvon mukaan.</span><span class="sxs-lookup"><span data-stu-id="cc1b0-107">The options that are available in the **Period frequency** field vary, depending on the value that is selected in the **Depreciation year** field.</span></span>

## <a name="select-a-depreciation-year"></a><span data-ttu-id="cc1b0-108">Poistovuoden valitseminen</span><span class="sxs-lookup"><span data-stu-id="cc1b0-108">Select a depreciation year</span></span>
<span data-ttu-id="cc1b0-109">Voit valita **Poistoprofiilit**-sivulla **Poistovuosi**-kenttään joko **Kalenteri** tai **Tilikausi**.</span><span class="sxs-lookup"><span data-stu-id="cc1b0-109">You can select either **Calendar** or **Fiscal** in the **Depreciation year** field on the **Depreciation profiles** page.</span></span> <span data-ttu-id="cc1b0-110">Oletusarvo on **Kalenteri**.</span><span class="sxs-lookup"><span data-stu-id="cc1b0-110">The default value is **Calendar**.</span></span> 

<span data-ttu-id="cc1b0-111">Valinta määrittää, mitä valintoja **Kausiväli**-kentässä on käytettävissä.</span><span class="sxs-lookup"><span data-stu-id="cc1b0-111">Your selection determines the options that are available in the **Period frequency** field.</span></span> <span data-ttu-id="cc1b0-112">Tämä kenttäsi määrittää poiston jaksotuksen kirjauspäivät ja -määrät kalenterivuoden aikana.</span><span class="sxs-lookup"><span data-stu-id="cc1b0-112">This field defines the depreciation accrual posting dates and amounts throughout the calendar year.</span></span>

### <a name="calendar"></a><span data-ttu-id="cc1b0-113">Kalenteri</span><span class="sxs-lookup"><span data-stu-id="cc1b0-113">Calendar</span></span>

<span data-ttu-id="cc1b0-114">Voit säilyttää **Poistovuosi** -kentässä oletusarvon **Kalenteri**.</span><span class="sxs-lookup"><span data-stu-id="cc1b0-114">You can keep the default value in the **Depreciation year** field, **Calendar**.</span></span> 

<span data-ttu-id="cc1b0-115">**Kalenteri**-vaihtoehto päivittää joka vuosi poistokannan 1. tammikuuta.</span><span class="sxs-lookup"><span data-stu-id="cc1b0-115">The **Calendar** option updates the depreciation base on January 1 of each year.</span></span> <span data-ttu-id="cc1b0-116">Yleensä poistokanta on nettokirjanpitoarvo vähennettynä jäännösarvolla.</span><span class="sxs-lookup"><span data-stu-id="cc1b0-116">Typically, the depreciation base is the net book value minus the scrap value.</span></span> <span data-ttu-id="cc1b0-117">Alla olevissa esimerkeissä poistokanta on laskentasarakkeen ensimmäisen lausekkeen osoittaja.</span><span class="sxs-lookup"><span data-stu-id="cc1b0-117">In the examples later in this topic, the depreciation base is the numerator in the first expression in the calculations column.</span></span> 

<span data-ttu-id="cc1b0-118">Jos poistovuodeksi valitaan **Kalenteri**, **Kausiväli**-kentässä ovat käytettävissä seuraavat vaihtoehdot:</span><span class="sxs-lookup"><span data-stu-id="cc1b0-118">If you select **Calendar** as the depreciation year, the following options are available in the **Period frequency** field:</span></span>

-   <span data-ttu-id="cc1b0-119">**Vuosittain** kirjaa summan 31. joulukuuta.</span><span class="sxs-lookup"><span data-stu-id="cc1b0-119">**Yearly** posts an amount on December 31.</span></span>
-   <span data-ttu-id="cc1b0-120">**Kuukausittain** kirjaa kuukausikohtaisen poiston kunkin kuun lopussa.</span><span class="sxs-lookup"><span data-stu-id="cc1b0-120">**Monthly** posts a monthly amount at the end of each calendar month.</span></span>
-   <span data-ttu-id="cc1b0-121">**Neljännesvuosittain** kirjaa neljännesvuoden poiston kalenterivuoden kunkin neljänneksen lopussa (31.3, 30.6. 30.9. ja 31.12.)</span><span class="sxs-lookup"><span data-stu-id="cc1b0-121">**Quarterly** posts a quarterly amount at the end of each calendar quarter (March 31, June 30, September 30, and December 31).</span></span>
-   <span data-ttu-id="cc1b0-122">**Puolivuosittain** kirjaa puolen vuoden summan kalenteripuolivuosittain (30.6. ja 31.12.).</span><span class="sxs-lookup"><span data-stu-id="cc1b0-122">**Half-Yearly** posts a half-yearly amount at the calendar half year (June 30 and December 31).</span></span>
-   <span data-ttu-id="cc1b0-123">**Päivittäin** kirjaa päivittäisen poistomenetelmän poistosumman käyttämällä yhtä tapahtumaa päivää kohden.</span><span class="sxs-lookup"><span data-stu-id="cc1b0-123">**Daily** posts the depreciation amount for the daily depreciation method by using one transaction for each day.</span></span>

### <a name="fiscal"></a><span data-ttu-id="cc1b0-124">Veroasiakirja</span><span class="sxs-lookup"><span data-stu-id="cc1b0-124">Fiscal</span></span>

<span data-ttu-id="cc1b0-125">Jos valitset **Poistovuosi**-kentässä **Tilivuosi**-vaihtoehdon, 175 prosentin jäännösarvo lasketaan kirjalle määritetyn kirjanpidon vuosikalenterin tilivuoden perusteella tai **Kirjanpito**-sivulla valitun kirjanpidon vuosikalenterin perusteella.</span><span class="sxs-lookup"><span data-stu-id="cc1b0-125">If you select **Fiscal** in the **Depreciation year** field, 175% reducing balance depreciation is calculated based on the fiscal year for the fiscal calendar that is specified for the book, or for the fiscal calendar that is selected on the **Ledger** page.</span></span> <span data-ttu-id="cc1b0-126">Kirjanpidon vuosikalenterit määritetään **Kirjanpidon kalenterit** -sivulla.</span><span class="sxs-lookup"><span data-stu-id="cc1b0-126">Fiscal calendars are set up on the **Fiscal calendars** page.</span></span> <span data-ttu-id="cc1b0-127">Lisätietoja on kohdassa [Tilikalenterit, tilikaudet ja kaudet](../budgeting/fiscal-calendars-fiscal-years-periods.md).</span><span class="sxs-lookup"><span data-stu-id="cc1b0-127">For more information, see [Fiscal calendars, fiscal years, and periods](../budgeting/fiscal-calendars-fiscal-years-periods.md).</span></span>

<span data-ttu-id="cc1b0-128">Esimerkiksi tilikauden 1.7 – 30.6. poistojen laskeminen alkaa 1.7.</span><span class="sxs-lookup"><span data-stu-id="cc1b0-128">For example, for the fiscal year July 1 through June 30, the depreciation calculation starts on July 1.</span></span> <span data-ttu-id="cc1b0-129">Tilivuosi voi olla pidempi tai lyhyempi kuin 12 kuukautta.</span><span class="sxs-lookup"><span data-stu-id="cc1b0-129">The fiscal year can be longer or shorter than 12 months.</span></span> <span data-ttu-id="cc1b0-130">Poisto säätyy automaattisesti kutakin tilijaksoa varten ja seuraavan tilivuoden pituus määräytyy **Kirjanpidon kalenterit**-lomakkeessa määritetyistä tilijaksojen asetuksista.</span><span class="sxs-lookup"><span data-stu-id="cc1b0-130">The depreciation is automatically adjusted for each period, and the length of the next fiscal year is determined by the setup of periods on the **Fiscal calendars** page.</span></span> 

<span data-ttu-id="cc1b0-131">Jos valitset poistovuodeksi **Tilivuosi**, seuraavat vaihtoehdot ovat valittavissa **Kausiväli**-kentässä:</span><span class="sxs-lookup"><span data-stu-id="cc1b0-131">If you select **Fiscal** as the depreciation year, the following options are available in the **Period frequency** field:</span></span>

-   <span data-ttu-id="cc1b0-132">**Vuosittain** kirjaa tilivuodelle lasketun poiston kokonaismäärän tilivuoden viimeisenä päivänä.</span><span class="sxs-lookup"><span data-stu-id="cc1b0-132">**Yearly** posts the total amount of the depreciation that is calculated for the fiscal year on the last day of the fiscal year.</span></span>
-   <span data-ttu-id="cc1b0-133">**Tilikausi** laskee tilikaudelle lasketun poiston kokonaismäärän.</span><span class="sxs-lookup"><span data-stu-id="cc1b0-133">**Fiscal period** calculates the total amount of the depreciation for the fiscal year.</span></span> <span data-ttu-id="cc1b0-134">Summa on jaksotettu tilikausille, jotka määritetään **Kirjanpidon kalenterit** -sivulla.</span><span class="sxs-lookup"><span data-stu-id="cc1b0-134">This amount is accrued into the fiscal periods that are defined on the **Fiscal calendars** page.</span></span>

## <a name="example-of-175-reducing-balance-depreciation"></a><span data-ttu-id="cc1b0-135">Esimerkki 175 prosentin jäännöspoistosta</span><span class="sxs-lookup"><span data-stu-id="cc1b0-135">Example of 175% reducing balance depreciation</span></span>

|                                |        |
|--------------------------------|--------|
| <span data-ttu-id="cc1b0-136">Hankintakustannukset</span><span class="sxs-lookup"><span data-stu-id="cc1b0-136">Acquisition cost</span></span>               | <span data-ttu-id="cc1b0-137">11 000</span><span class="sxs-lookup"><span data-stu-id="cc1b0-137">11,000</span></span> |
| <span data-ttu-id="cc1b0-138">Jäännösarvo</span><span class="sxs-lookup"><span data-stu-id="cc1b0-138">Salvage value</span></span>                  | <span data-ttu-id="cc1b0-139">1 000</span><span class="sxs-lookup"><span data-stu-id="cc1b0-139">1,000</span></span>  |
| <span data-ttu-id="cc1b0-140">Poistokanta</span><span class="sxs-lookup"><span data-stu-id="cc1b0-140">Depreciation base</span></span>              | <span data-ttu-id="cc1b0-141">10 000</span><span class="sxs-lookup"><span data-stu-id="cc1b0-141">10,000</span></span> |
| <span data-ttu-id="cc1b0-142">Käyttöikä vuosina</span><span class="sxs-lookup"><span data-stu-id="cc1b0-142">Service life years</span></span>             | <span data-ttu-id="cc1b0-143">5</span><span class="sxs-lookup"><span data-stu-id="cc1b0-143">5</span></span>      |
| <span data-ttu-id="cc1b0-144">Vuosittainen poistoprosentti:</span><span class="sxs-lookup"><span data-stu-id="cc1b0-144">Yearly depreciation percentage</span></span> | <span data-ttu-id="cc1b0-145">35 %</span><span class="sxs-lookup"><span data-stu-id="cc1b0-145">35%</span></span>    |

<span data-ttu-id="cc1b0-146">175 %:n jäännösarvon poistomenetelmä jakaa arvon 175 % käyttövuosilla.</span><span class="sxs-lookup"><span data-stu-id="cc1b0-146">The 175% reducing balance depreciation method divides 175 percent by the service life years.</span></span> <span data-ttu-id="cc1b0-147">Kyseinen prosentti kerrotaan käyttöomaisuuserän nettokirjanpitoarvolla, jolloin saadaan tulokseksi vuoden poistosumma.</span><span class="sxs-lookup"><span data-stu-id="cc1b0-147">That percentage will be multiplied by the net book value of the asset to determine the depreciation amount for the year.</span></span>

| <span data-ttu-id="cc1b0-148">Kausi</span><span class="sxs-lookup"><span data-stu-id="cc1b0-148">Period</span></span> | <span data-ttu-id="cc1b0-149">Vuotuisen poistomäärän laskeminen</span><span class="sxs-lookup"><span data-stu-id="cc1b0-149">Calculation of the yearly depreciation amount</span></span> | <span data-ttu-id="cc1b0-150">Kirjanpitoarvo</span><span class="sxs-lookup"><span data-stu-id="cc1b0-150">Book value</span></span>                  | <span data-ttu-id="cc1b0-151">Nettokirjanpitoarvo vuoden lopussa:</span><span class="sxs-lookup"><span data-stu-id="cc1b0-151">Net book value at the end of the year</span></span> |
|--------|-----------------------------------------------|-----------------------------|---------------------------------------|
| <span data-ttu-id="cc1b0-152">Vuosi 1</span><span class="sxs-lookup"><span data-stu-id="cc1b0-152">Year 1</span></span> | <span data-ttu-id="cc1b0-153">(11 000 – 1 000) × 35 % = 3 500</span><span class="sxs-lookup"><span data-stu-id="cc1b0-153">(11,000 – 1,000) × 35% = 3,500</span></span>                | <span data-ttu-id="cc1b0-154">11 000 – 3 500 = 7 500</span><span class="sxs-lookup"><span data-stu-id="cc1b0-154">11,000 – 3,500 = 7,500</span></span>      | <span data-ttu-id="cc1b0-155">11 000 – 1 000 – 3 500 = 6 500</span><span class="sxs-lookup"><span data-stu-id="cc1b0-155">11,000 – 1,000 – 3,500 = 6,500</span></span>        |
| <span data-ttu-id="cc1b0-156">Vuosi 2</span><span class="sxs-lookup"><span data-stu-id="cc1b0-156">Year 2</span></span> | <span data-ttu-id="cc1b0-157">6 500 × 35 % = 2 275</span><span class="sxs-lookup"><span data-stu-id="cc1b0-157">6,500 × 35% = 2,275</span></span>                           | <span data-ttu-id="cc1b0-158">7 500 – 2 275 = 5 225</span><span class="sxs-lookup"><span data-stu-id="cc1b0-158">7,500 – 2,275 = 5,225</span></span>       | <span data-ttu-id="cc1b0-159">6 500 – 2 275 = 4 225</span><span class="sxs-lookup"><span data-stu-id="cc1b0-159">6,500 – 2,275 = 4,225</span></span>                 |
| <span data-ttu-id="cc1b0-160">Vuosi 3</span><span class="sxs-lookup"><span data-stu-id="cc1b0-160">Year 3</span></span> | <span data-ttu-id="cc1b0-161">4 225 × 35 % = 1 478,75</span><span class="sxs-lookup"><span data-stu-id="cc1b0-161">4,225 × 35% = 1,478.75</span></span>                        | <span data-ttu-id="cc1b0-162">5 225 – 1 478,75 = 3 746,25</span><span class="sxs-lookup"><span data-stu-id="cc1b0-162">5,225 – 1,478.75 = 3,746.25</span></span> | <span data-ttu-id="cc1b0-163">4 225 – 1 478,75 = 2 746,25</span><span class="sxs-lookup"><span data-stu-id="cc1b0-163">4,225 – 1,478.75 = 2,746.25</span></span>           |

> [!NOTE] 
> <span data-ttu-id="cc1b0-164">Jos 175 %:n jäännösarvon poistomenetelmän avulla laskettu määrä on pienempi kuin tasapoistomenetelmän avulla laskettu määrä, jäljellä olevalle käyttöiälle on yleensä olemassa tasapoistomenetelmä.</span><span class="sxs-lookup"><span data-stu-id="cc1b0-164">Typically, when the amount that is calculated by using the 175% reducing balance depreciation method becomes less than the amount that would be calculated by using the straight line method, there is a conversion to the straight line method for the remaining life.</span></span>




