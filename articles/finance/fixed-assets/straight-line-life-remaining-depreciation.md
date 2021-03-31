---
title: Jäljellä olevan käyttöajan tasapoisto
description: Tässä artikkelissa on yleiskuvaus jäljellä olevaan käyttöaikaan perustuvasta tasapoistomenetelmästä.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetDepreciationProfile
audience: Application User
ms.reviewer: roschlom
ms.custom: 13851
ms.assetid: 0fa2f71a-596c-414c-a6e6-8f7405a0bf81
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 823b2569670adfbf04038abca656e34f0199fce1
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5210092"
---
# <a name="straight-line-life-remaining-depreciation"></a><span data-ttu-id="5ed86-103">Jäljellä olevan käyttöajan tasapoisto</span><span class="sxs-lookup"><span data-stu-id="5ed86-103">Straight line life remaining depreciation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5ed86-104">Tässä artikkelissa on yleiskuvaus jäljellä olevaan käyttöaikaan perustuvasta tasapoistomenetelmästä.</span><span class="sxs-lookup"><span data-stu-id="5ed86-104">This article gives an overview of the Straight line life remaining method of depreciation.</span></span>

<span data-ttu-id="5ed86-105">Jos määrität käyttöomaisuudelle poistoprofiilin ja valitset **Tasapoisto - jäljellä oleva käyttöaika** -asetuksen **Poistoprofiilit**-sivun **Menetelmä** -kenttään, niiden käyttöomaisuuserien poisto, joille on määritetty tämä poistoprofiili, perustuu käyttöomaisuuden jäljelläoleviin käyttövuosiin.</span><span class="sxs-lookup"><span data-stu-id="5ed86-105">When you set up a fixed asset depreciation profile and select **Straight line life remaining** in the **Method** field on the **Depreciation profiles** page, the depreciation of fixed assets that are assigned to the depreciation profile is based on the remaining service life of the asset.</span></span> <span data-ttu-id="5ed86-106">Tavallisesti poiston määrä on tällöin sama kullakin poistojaksolla.</span><span class="sxs-lookup"><span data-stu-id="5ed86-106">The depreciation amount is generally the same in each depreciation period.</span></span> <span data-ttu-id="5ed86-107">Jos haluat määrittää jäljellä olevaan käyttöaikaan perustuvan tasapoiston, valitse **Poistoprofiilit**-sivulla myös **Poistovuosi**- ja **Kausiväli**-kenttien asetukset.</span><span class="sxs-lookup"><span data-stu-id="5ed86-107">To set up straight line life remaining depreciation, you also must select options in the **Depreciation year** field and the **Period frequency** field on the **Depreciation profiles** page.</span></span> <span data-ttu-id="5ed86-108">**Kausiväli**-kentän käytettävissä olevat vaihtoehdot vaihtelevat **Poistovuosi**-kentässä valitun arvon mukaan.</span><span class="sxs-lookup"><span data-stu-id="5ed86-108">The options that are available in the **Period frequency** field vary, depending on the value that is selected in the **Depreciation year** field.</span></span>

## <a name="select-a-depreciation-year"></a><span data-ttu-id="5ed86-109">Poistovuoden valitseminen</span><span class="sxs-lookup"><span data-stu-id="5ed86-109">Select a depreciation year</span></span>
<span data-ttu-id="5ed86-110">Voit valita **Poistoprofiilit**-sivulla **Poistovuosi**-kenttään joko **Kalenteri** tai **Tilikausi**.</span><span class="sxs-lookup"><span data-stu-id="5ed86-110">You can select either **Calendar** or **Fiscal** in the **Depreciation year** field on the **Depreciation profiles** page.</span></span> <span data-ttu-id="5ed86-111">Oletusarvo on **Kalenteri**.</span><span class="sxs-lookup"><span data-stu-id="5ed86-111">The default value is **Calendar**.</span></span> <span data-ttu-id="5ed86-112">Valinta määrittää, mitä valintoja **Kausiväli**-kentässä on käytettävissä.</span><span class="sxs-lookup"><span data-stu-id="5ed86-112">Your selection determines the options that are available in the **Period frequency** field.</span></span> <span data-ttu-id="5ed86-113">Tämä kenttäsi määrittää poiston jaksotuksen kirjauspäivät ja -määrät kalenterivuoden aikana.</span><span class="sxs-lookup"><span data-stu-id="5ed86-113">This field defines the depreciation accrual posting dates and amounts throughout the calendar year.</span></span>

### <a name="calendar"></a><span data-ttu-id="5ed86-114">Kalenteri</span><span class="sxs-lookup"><span data-stu-id="5ed86-114">Calendar</span></span>

<span data-ttu-id="5ed86-115">Jos valitset **Kalenteri** \**_Poistovuosi_*_ -kentässä, oletetaan vuosi 1.1.–31.12., vaikka olisit määrittänyt kirjanpidon vuosikalenterin eri tavalla. _\* Kalneteri\*\*-asetus päivittää poistokannan 1. tammikuuta joka vuosi.</span><span class="sxs-lookup"><span data-stu-id="5ed86-115">If you select **Calendar** in the **_Depreciation year_*_ field, a year of January 1 through December 31 is assumed, even if you've defined the fiscal calendar differently. The _\* Calendar*\* option updates the depreciation base on January 1 of each year.</span></span> <span data-ttu-id="5ed86-116">Yleensä poistokanta on nettokirjanpitoarvo vähennettynä jäännösarvolla.</span><span class="sxs-lookup"><span data-stu-id="5ed86-116">Typically, the depreciation base is the net book value minus the salvage value.</span></span> <span data-ttu-id="5ed86-117">Alla olevissa esimerkeissä poistokanta on laskentasarakkeen ensimmäisen lausekkeen osoittaja.</span><span class="sxs-lookup"><span data-stu-id="5ed86-117">In the example later in this topic, the depreciation base is the numerator in the first expression in the calculations column.</span></span> <span data-ttu-id="5ed86-118">Jos poistovuodeksi valitaan **Kalenteri**, **Kausiväli**-kentässä ovat käytettävissä seuraavat vaihtoehdot:</span><span class="sxs-lookup"><span data-stu-id="5ed86-118">If you select **Calendar** as the depreciation year, the following options are available in the **Period frequency** field:</span></span>

-   <span data-ttu-id="5ed86-119">**Vuosittain** kirjaa summan 31. joulukuuta.</span><span class="sxs-lookup"><span data-stu-id="5ed86-119">**Yearly** posts an amount on December 31.</span></span>
-   <span data-ttu-id="5ed86-120">**Kuukausittain** kirjaa kuukausikohtaisen poiston kunkin kuun lopussa.</span><span class="sxs-lookup"><span data-stu-id="5ed86-120">**Monthly** posts a monthly amount at the end of each calendar month.</span></span>
-   <span data-ttu-id="5ed86-121">**Neljännesvuosittain** kirjaa neljännesvuoden poiston kalenterivuoden kunkin neljänneksen lopussa (31.3, 30.6. 30.9. ja 31.12.)</span><span class="sxs-lookup"><span data-stu-id="5ed86-121">**Quarterly** posts a quarterly amount at the end of each calendar quarter (March 31, June 30, September 30, and December 31).</span></span>
-   <span data-ttu-id="5ed86-122">**Puolivuosittain** kirjaa puolen vuoden summan kunkin kalenterivuosipuolikkaan lopussa (30.6. ja 31.12.)</span><span class="sxs-lookup"><span data-stu-id="5ed86-122">**Half-Yearly** posts a half-yearly amount at the end of each calendar half year (June 30 and December 31).</span></span>
-   <span data-ttu-id="5ed86-123">**Päivittäin** kirjaa päivittäisen poistomenetelmän poistosumman käyttämällä yhtä tapahtumaa päivää kohden.</span><span class="sxs-lookup"><span data-stu-id="5ed86-123">**Daily** posts the depreciation amount for the daily depreciation method by using one transaction for each day.</span></span>

<span data-ttu-id="5ed86-124">Jos valitset esimerkiksi **Vuosittain**, vuoden poisto kirjataan vain kerran eli kunkin vuoden joulukuun 31. päivä.</span><span class="sxs-lookup"><span data-stu-id="5ed86-124">For example, if you select **Yearly**, the yearly depreciation is posted only one time, on December 31 of each year.</span></span> <span data-ttu-id="5ed86-125">Jos valitset **Kuukausittain**, kuukauden poisto kirjataan joka kuukausi käyttämällä kahdestoistaosaa koko vuoden poistosummasta.</span><span class="sxs-lookup"><span data-stu-id="5ed86-125">If you select **Monthly**, the monthly depreciation is posted each month, as one-twelfth of the yearly depreciation amount.</span></span>

### <a name="fiscal"></a><span data-ttu-id="5ed86-126">Veroasiakirja</span><span class="sxs-lookup"><span data-stu-id="5ed86-126">Fiscal</span></span>

<span data-ttu-id="5ed86-127">Jos valitset **Poistovuosi**-kentästä **Tilivuosi**-vaihtoehdon, käytetään käyttöaikaan perustuvaa tasapoistomenetelmää.</span><span class="sxs-lookup"><span data-stu-id="5ed86-127">If you select **Fiscal** in the **Depreciation year** field, straight line life remaining depreciation is used.</span></span> <span data-ttu-id="5ed86-128">Poisto lasketaan jäljellä olevien tilikausien mukaan.</span><span class="sxs-lookup"><span data-stu-id="5ed86-128">Depreciation is calculated based on the fiscal years remaining.</span></span> <span data-ttu-id="5ed86-129">Esimerkiksi tilikauden 1.7.2015 – 30.6.2016 poistojen laskeminen alkaa 1.7.</span><span class="sxs-lookup"><span data-stu-id="5ed86-129">For example, for the fiscal year July 1, 2015, through June 30, 2016, the depreciation calculation starts on July 1.</span></span> <span data-ttu-id="5ed86-130">Tilivuosi voi olla pidempi tai lyhyempi kuin 12 kuukautta.</span><span class="sxs-lookup"><span data-stu-id="5ed86-130">The fiscal year can be longer or shorter than 12 months.</span></span> <span data-ttu-id="5ed86-131">Poisto oikaistaan jokaisella tilikaudella.</span><span class="sxs-lookup"><span data-stu-id="5ed86-131">The depreciation is adjusted for each fiscal period.</span></span> <span data-ttu-id="5ed86-132">**Kirjanpidon kalenterit** -sivun kausien asetuksissa määritetään seuraavan tilikauden pituus.</span><span class="sxs-lookup"><span data-stu-id="5ed86-132">The length of the next fiscal year is determined by the fiscal periods that are set up on the **Fiscal calendars** page.</span></span> <span data-ttu-id="5ed86-133">Jos valitset poistovuodeksi **Tilivuosi**, seuraavat vaihtoehdot ovat valittavissa **Kausiväli**-kentässä:</span><span class="sxs-lookup"><span data-stu-id="5ed86-133">If you select **Fiscal** as the depreciation year, the following options are available in the **Period frequency** field:</span></span>

-   <span data-ttu-id="5ed86-134">**Vuosittain** kirjaa tilivuodelle lasketun poiston kokonaismäärän yhtenä summana tilivuoden viimeisenä päivänä.</span><span class="sxs-lookup"><span data-stu-id="5ed86-134">**Yearly** posts the total amount of the depreciation that is calculated for the fiscal year as one amount, on the last day of the fiscal year.</span></span>
-   <span data-ttu-id="5ed86-135">**Tilikausi** laskee tilikaudelle lasketun poiston kokonaismäärän.</span><span class="sxs-lookup"><span data-stu-id="5ed86-135">**Fiscal period** calculates the total amount of the depreciation for the fiscal year.</span></span> <span data-ttu-id="5ed86-136">Tämä määrä jaetaan kirjauskausille, jotka on määritetty kirjan **Kirjanpidon kalenterit** -sivulla valitussa kirjanpitokalenterissa.</span><span class="sxs-lookup"><span data-stu-id="5ed86-136">This amount is then accrued into the fiscal periods that are defined on the **Fiscal calendars** page for the fiscal calendar that is specified for the book.</span></span>

## <a name="example-of-straight-line-depreciation-of-an-unchanged-fixed-asset"></a><span data-ttu-id="5ed86-137">Esimerkki muuttamattoman käyttöomaisuuden tasapoistosta</span><span class="sxs-lookup"><span data-stu-id="5ed86-137">Example of straight line depreciation of an unchanged fixed asset</span></span>
<span data-ttu-id="5ed86-138">Käyttöomaisuudella on seuraavat ominaisuudet:</span><span class="sxs-lookup"><span data-stu-id="5ed86-138">A fixed asset has the following characteristics.</span></span>

|                     |        |
|---------------------|--------|
| <span data-ttu-id="5ed86-139">Hankintakustannukset</span><span class="sxs-lookup"><span data-stu-id="5ed86-139">Acquisition cost</span></span>    | <span data-ttu-id="5ed86-140">11 000</span><span class="sxs-lookup"><span data-stu-id="5ed86-140">11,000</span></span> |
| <span data-ttu-id="5ed86-141">Jäännösarvo</span><span class="sxs-lookup"><span data-stu-id="5ed86-141">Salvage value</span></span>       | <span data-ttu-id="5ed86-142">1 000</span><span class="sxs-lookup"><span data-stu-id="5ed86-142">1,000</span></span>  |
| <span data-ttu-id="5ed86-143">Poistokanta</span><span class="sxs-lookup"><span data-stu-id="5ed86-143">Depreciation base</span></span>   | <span data-ttu-id="5ed86-144">10 000</span><span class="sxs-lookup"><span data-stu-id="5ed86-144">10,000</span></span> |
| <span data-ttu-id="5ed86-145">Käyttöikä vuosina</span><span class="sxs-lookup"><span data-stu-id="5ed86-145">Service life years</span></span>  | <span data-ttu-id="5ed86-146">5</span><span class="sxs-lookup"><span data-stu-id="5ed86-146">5</span></span>      |
| <span data-ttu-id="5ed86-147">Vuotuinen poisto</span><span class="sxs-lookup"><span data-stu-id="5ed86-147">Yearly depreciation</span></span> | <span data-ttu-id="5ed86-148">2 000</span><span class="sxs-lookup"><span data-stu-id="5ed86-148">2,000</span></span>  |

<span data-ttu-id="5ed86-149">Poiston määrä on sama vuosittain: (hankintahinta-jäännösarvo) / käyttövuodet</span><span class="sxs-lookup"><span data-stu-id="5ed86-149">The depreciation amount is the same every year: (Acquisition cost – Salvage value) ÷ Service life years</span></span>

| <span data-ttu-id="5ed86-150">Kausi</span><span class="sxs-lookup"><span data-stu-id="5ed86-150">Period</span></span> | <span data-ttu-id="5ed86-151">Vuotuisen poistomäärän laskeminen</span><span class="sxs-lookup"><span data-stu-id="5ed86-151">Calculation of the yearly depreciation amount</span></span> | <span data-ttu-id="5ed86-152">Nettokirjanpitoarvo vuoden lopussa:</span><span class="sxs-lookup"><span data-stu-id="5ed86-152">Net book value at the end of the year</span></span> |
|--------|-----------------------------------------------|---------------------------------------|
| <span data-ttu-id="5ed86-153">Vuosi 1</span><span class="sxs-lookup"><span data-stu-id="5ed86-153">Year 1</span></span> | <span data-ttu-id="5ed86-154">(11 000 – 1 000) ÷ 5 = 2 000</span><span class="sxs-lookup"><span data-stu-id="5ed86-154">(11,000 – 1,000) ÷ 5 = 2,000</span></span>                  | <span data-ttu-id="5ed86-155">−9 000</span><span class="sxs-lookup"><span data-stu-id="5ed86-155">9,000</span></span>                                 |
| <span data-ttu-id="5ed86-156">Vuosi 2</span><span class="sxs-lookup"><span data-stu-id="5ed86-156">Year 2</span></span> | <span data-ttu-id="5ed86-157">(9 000 – 1 000) ÷ 4 = 2 000</span><span class="sxs-lookup"><span data-stu-id="5ed86-157">(9,000 – 1,000) ÷ 4 = 2,000</span></span>                   | <span data-ttu-id="5ed86-158">7 000</span><span class="sxs-lookup"><span data-stu-id="5ed86-158">7,000</span></span>                                 |
| <span data-ttu-id="5ed86-159">Vuosi 3</span><span class="sxs-lookup"><span data-stu-id="5ed86-159">Year 3</span></span> | <span data-ttu-id="5ed86-160">(7 000 – 1 000) ÷ 3 = 2 000</span><span class="sxs-lookup"><span data-stu-id="5ed86-160">(7,000 – 1,000) ÷ 3 = 2,000</span></span>                   | <span data-ttu-id="5ed86-161">5 000</span><span class="sxs-lookup"><span data-stu-id="5ed86-161">5,000</span></span>                                 |
| <span data-ttu-id="5ed86-162">Vuosi 4</span><span class="sxs-lookup"><span data-stu-id="5ed86-162">Year 4</span></span> | <span data-ttu-id="5ed86-163">(5 000 – 1 000) ÷ 2 = 2 000</span><span class="sxs-lookup"><span data-stu-id="5ed86-163">(5,000 – 1,000) ÷ 2 = 2,000</span></span>                   | <span data-ttu-id="5ed86-164">3 000</span><span class="sxs-lookup"><span data-stu-id="5ed86-164">3,000</span></span>                                 |
| <span data-ttu-id="5ed86-165">Vuosi 5</span><span class="sxs-lookup"><span data-stu-id="5ed86-165">Year 5</span></span> | <span data-ttu-id="5ed86-166">(3 000 – 1 000) ÷ 1 = 2 000</span><span class="sxs-lookup"><span data-stu-id="5ed86-166">(3,000 – 1,000) ÷ 1 = 2,000</span></span>                   | <span data-ttu-id="5ed86-167">1 000</span><span class="sxs-lookup"><span data-stu-id="5ed86-167">1,000</span></span>                                 |







[!INCLUDE[footer-include](../../includes/footer-banner.md)]