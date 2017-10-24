---
title: "Jäljellä olevan käyttöajan tasapoisto"
description: "Tässä artikkelissa on yleiskuvaus jäljellä olevaan käyttöaikaan perustuvasta tasapoistomenetelmästä."
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
ms.custom: 13851
ms.assetid: 0fa2f71a-596c-414c-a6e6-8f7405a0bf81
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 4ad82f3177e4abb7b9cb575b910aabc69901f475
ms.contentlocale: fi-fi
ms.lasthandoff: 09/29/2017

---

# <a name="straight-line-life-remaining-depreciation"></a><span data-ttu-id="06e30-103">Jäljellä olevan käyttöajan tasapoisto</span><span class="sxs-lookup"><span data-stu-id="06e30-103">Straight line life remaining depreciation</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="06e30-104">Tässä artikkelissa on yleiskuvaus jäljellä olevaan käyttöaikaan perustuvasta tasapoistomenetelmästä.</span><span class="sxs-lookup"><span data-stu-id="06e30-104">This article gives an overview of the Straight line life remaining method of depreciation.</span></span>

<span data-ttu-id="06e30-105">Jos määrität käyttöomaisuudelle poistoprofiilin ja valitset **Tasapoisto - jäljellä oleva käyttöaika** -asetuksen **Poistoprofiilit**-sivun **Menetelmä** -kenttään, niiden käyttöomaisuuserien poisto, joille on määritetty tämä poistoprofiili, perustuu käyttöomaisuuden jäljelläoleviin käyttövuosiin.</span><span class="sxs-lookup"><span data-stu-id="06e30-105">When you set up a fixed asset depreciation profile and select **Straight line life remaining** in the **Method** field on the **Depreciation profiles** page, the depreciation of fixed assets that are assigned to the depreciation profile is based on the remaining service life of the asset.</span></span> <span data-ttu-id="06e30-106">Tavallisesti poiston määrä on tällöin sama kullakin poistojaksolla.</span><span class="sxs-lookup"><span data-stu-id="06e30-106">The depreciation amount is generally the same in each depreciation period.</span></span> <span data-ttu-id="06e30-107">Jos haluat määrittää jäljellä olevaan käyttöaikaan perustuvan tasapoiston, valitse **Poistoprofiilit**-sivulla myös **Poistovuosi**- ja **Kausiväli**-kenttien asetukset.</span><span class="sxs-lookup"><span data-stu-id="06e30-107">To set up straight line life remaining depreciation, you also must select options in the **Depreciation year** field and the **Period frequency** field on the **Depreciation profiles** page.</span></span> <span data-ttu-id="06e30-108">**Kausiväli**-kentän käytettävissä olevat vaihtoehdot vaihtelevat **Poistovuosi**-kentässä valitun arvon mukaan.</span><span class="sxs-lookup"><span data-stu-id="06e30-108">The options that are available in the **Period frequency** field vary, depending on the value that is selected in the **Depreciation year** field.</span></span>

## <a name="select-a-depreciation-year"></a><span data-ttu-id="06e30-109">Poistovuoden valitseminen</span><span class="sxs-lookup"><span data-stu-id="06e30-109">Select a depreciation year</span></span>
<span data-ttu-id="06e30-110">Voit valita **Poistoprofiilit**-sivulla **Poistovuosi**-kenttään joko **Kalenteri** tai **Tilikausi**.</span><span class="sxs-lookup"><span data-stu-id="06e30-110">You can select either **Calendar** or **Fiscal** in the **Depreciation year** field on the **Depreciation profiles** page.</span></span> <span data-ttu-id="06e30-111">Oletusarvo on **Kalenteri**.</span><span class="sxs-lookup"><span data-stu-id="06e30-111">The default value is **Calendar**.</span></span> <span data-ttu-id="06e30-112">Valinta määrittää, mitä valintoja **Kausiväli**-kentässä on käytettävissä.</span><span class="sxs-lookup"><span data-stu-id="06e30-112">Your selection determines the options that are available in the **Period frequency** field.</span></span> <span data-ttu-id="06e30-113">Tämä kenttäsi määrittää poiston jaksotuksen kirjauspäivät ja -määrät kalenterivuoden aikana.</span><span class="sxs-lookup"><span data-stu-id="06e30-113">This field defines the depreciation accrual posting dates and amounts throughout the calendar year.</span></span>

### <a name="calendar"></a><span data-ttu-id="06e30-114">Kalenteri</span><span class="sxs-lookup"><span data-stu-id="06e30-114">Calendar</span></span>

<span data-ttu-id="06e30-115">Valitessasi ***Poistovuosi***-kentän arvoksi **Kalenterivuosi**, järjestelmä olettaa kauden olevan 1. tammikuuta – 31. joulukuuta, vaikka kirjanpidon vuosikalenteri olisikin määritetty toisin.</span><span class="sxs-lookup"><span data-stu-id="06e30-115">If you select **Calendar** in the ***Depreciation year*** field, a year of January 1 through December 31 is assumed, even if you've defined the fiscal calendar differently.</span></span> <span data-ttu-id="06e30-116">**Kalenteri**-vaihtoehto päivittää joka vuosi poistokannan 1. tammikuuta.</span><span class="sxs-lookup"><span data-stu-id="06e30-116">The **Calendar** option updates the depreciation base on January 1 of each year.</span></span> <span data-ttu-id="06e30-117">Yleensä poistokanta on nettokirjanpitoarvo vähennettynä jäännösarvolla.</span><span class="sxs-lookup"><span data-stu-id="06e30-117">Typically, the depreciation base is the net book value minus the salvage value.</span></span> <span data-ttu-id="06e30-118">Alla olevissa esimerkeissä poistokanta on laskentasarakkeen ensimmäisen lausekkeen osoittaja.</span><span class="sxs-lookup"><span data-stu-id="06e30-118">In the example later in this topic, the depreciation base is the numerator in the first expression in the calculations column.</span></span> <span data-ttu-id="06e30-119">Jos poistovuodeksi valitaan **Kalenteri**, **Kausiväli**-kentässä ovat käytettävissä seuraavat vaihtoehdot:</span><span class="sxs-lookup"><span data-stu-id="06e30-119">If you select **Calendar** as the depreciation year, the following options are available in the **Period frequency** field:</span></span>

-   <span data-ttu-id="06e30-120">**Vuosittain** kirjaa summan 31. joulukuuta.</span><span class="sxs-lookup"><span data-stu-id="06e30-120">**Yearly** posts an amount on December 31.</span></span>
-   <span data-ttu-id="06e30-121">**Kuukausittain** kirjaa kuukausikohtaisen poiston kunkin kuun lopussa.</span><span class="sxs-lookup"><span data-stu-id="06e30-121">**Monthly** posts a monthly amount at the end of each calendar month.</span></span>
-   <span data-ttu-id="06e30-122">**Neljännesvuosittain** kirjaa neljännesvuoden poiston kalenterivuoden kunkin neljänneksen lopussa (31.3, 30.6. 30.9. ja 31.12.)</span><span class="sxs-lookup"><span data-stu-id="06e30-122">**Quarterly** posts a quarterly amount at the end of each calendar quarter (March 31, June 30, September 30, and December 31).</span></span>
-   <span data-ttu-id="06e30-123">**Puolivuosittain** kirjaa puolen vuoden summan kunkin kalenterivuosipuolikkaan lopussa (30.6. ja 31.12.)</span><span class="sxs-lookup"><span data-stu-id="06e30-123">**Half-Yearly** posts a half-yearly amount at the end of each calendar half year (June 30 and December 31).</span></span>
-   <span data-ttu-id="06e30-124">**Päivittäin** kirjaa päivittäisen poistomenetelmän poistosumman käyttämällä yhtä tapahtumaa päivää kohden.</span><span class="sxs-lookup"><span data-stu-id="06e30-124">**Daily** posts the depreciation amount for the daily depreciation method by using one transaction for each day.</span></span>

<span data-ttu-id="06e30-125">Jos valitset esimerkiksi **Vuosittain**, vuoden poisto kirjataan vain kerran eli kunkin vuoden joulukuun 31. päivä.</span><span class="sxs-lookup"><span data-stu-id="06e30-125">For example, if you select **Yearly**, the yearly depreciation is posted only one time, on December 31 of each year.</span></span> <span data-ttu-id="06e30-126">Jos valitset **Kuukausittain**, kuukauden poisto kirjataan joka kuukausi käyttämällä kahdestoistaosaa koko vuoden poistosummasta.</span><span class="sxs-lookup"><span data-stu-id="06e30-126">If you select **Monthly**, the monthly depreciation is posted each month, as one-twelfth of the yearly depreciation amount.</span></span>

### <a name="fiscal"></a><span data-ttu-id="06e30-127">Veroasiakirja</span><span class="sxs-lookup"><span data-stu-id="06e30-127">Fiscal</span></span>

<span data-ttu-id="06e30-128">Jos valitset **Poistovuosi**-kentästä **Tilivuosi**-vaihtoehdon, käytetään käyttöaikaan perustuvaa tasapoistomenetelmää.</span><span class="sxs-lookup"><span data-stu-id="06e30-128">If you select **Fiscal** in the **Depreciation year** field, straight line life remaining depreciation is used.</span></span> <span data-ttu-id="06e30-129">Poisto lasketaan jäljellä olevien tilikausien mukaan.</span><span class="sxs-lookup"><span data-stu-id="06e30-129">Depreciation is calculated based on the fiscal years remaining.</span></span> <span data-ttu-id="06e30-130">Esimerkiksi tilikauden 1.7.2015 – 30.6.2016 poistojen laskeminen alkaa 1.7.</span><span class="sxs-lookup"><span data-stu-id="06e30-130">For example, for the fiscal year July 1, 2015, through June 30, 2016, the depreciation calculation starts on July 1.</span></span> <span data-ttu-id="06e30-131">Tilivuosi voi olla pidempi tai lyhyempi kuin 12 kuukautta.</span><span class="sxs-lookup"><span data-stu-id="06e30-131">The fiscal year can be longer or shorter than 12 months.</span></span> <span data-ttu-id="06e30-132">Poisto oikaistaan jokaisella tilikaudella.</span><span class="sxs-lookup"><span data-stu-id="06e30-132">The depreciation is adjusted for each fiscal period.</span></span> <span data-ttu-id="06e30-133">**Kirjanpidon kalenterit** -sivun kausien asetuksissa määritetään seuraavan tilikauden pituus.</span><span class="sxs-lookup"><span data-stu-id="06e30-133">The length of the next fiscal year is determined by the fiscal periods that are set up on the **Fiscal calendars** page.</span></span> <span data-ttu-id="06e30-134">Jos valitset poistovuodeksi **Tilivuosi**, seuraavat vaihtoehdot ovat valittavissa **Kausiväli**-kentässä:</span><span class="sxs-lookup"><span data-stu-id="06e30-134">If you select **Fiscal** as the depreciation year, the following options are available in the **Period frequency** field:</span></span>

-   <span data-ttu-id="06e30-135">**Vuosittain** kirjaa tilivuodelle lasketun poiston kokonaismäärän yhtenä summana tilivuoden viimeisenä päivänä.</span><span class="sxs-lookup"><span data-stu-id="06e30-135">**Yearly** posts the total amount of the depreciation that is calculated for the fiscal year as one amount, on the last day of the fiscal year.</span></span>
-   <span data-ttu-id="06e30-136">**Tilikausi** laskee tilikaudelle lasketun poiston kokonaismäärän.</span><span class="sxs-lookup"><span data-stu-id="06e30-136">**Fiscal period** calculates the total amount of the depreciation for the fiscal year.</span></span> <span data-ttu-id="06e30-137">Tämä määrä jaetaan kirjauskausille, jotka on määritetty kirjan **Kirjanpidon kalenterit** -sivulla valitussa kirjanpitokalenterissa.</span><span class="sxs-lookup"><span data-stu-id="06e30-137">This amount is then accrued into the fiscal periods that are defined on the **Fiscal calendars** page for the fiscal calendar that is specified for the book.</span></span>

## <a name="example-of-straight-line-depreciation-of-an-unchanged-fixed-asset"></a><span data-ttu-id="06e30-138">Esimerkki muuttamattoman käyttöomaisuuden tasapoistosta</span><span class="sxs-lookup"><span data-stu-id="06e30-138">Example of straight line depreciation of an unchanged fixed asset</span></span>
<span data-ttu-id="06e30-139">Käyttöomaisuudella on seuraavat ominaisuudet:</span><span class="sxs-lookup"><span data-stu-id="06e30-139">A fixed asset has the following characteristics.</span></span>

|                     |        |
|---------------------|--------|
| <span data-ttu-id="06e30-140">Hankintakustannukset</span><span class="sxs-lookup"><span data-stu-id="06e30-140">Acquisition cost</span></span>    | <span data-ttu-id="06e30-141">11 000</span><span class="sxs-lookup"><span data-stu-id="06e30-141">11,000</span></span> |
| <span data-ttu-id="06e30-142">Jäännösarvo</span><span class="sxs-lookup"><span data-stu-id="06e30-142">Salvage value</span></span>       | <span data-ttu-id="06e30-143">1 000</span><span class="sxs-lookup"><span data-stu-id="06e30-143">1,000</span></span>  |
| <span data-ttu-id="06e30-144">Poistokanta</span><span class="sxs-lookup"><span data-stu-id="06e30-144">Depreciation base</span></span>   | <span data-ttu-id="06e30-145">10 000</span><span class="sxs-lookup"><span data-stu-id="06e30-145">10,000</span></span> |
| <span data-ttu-id="06e30-146">Käyttöikä vuosina</span><span class="sxs-lookup"><span data-stu-id="06e30-146">Service life years</span></span>  | <span data-ttu-id="06e30-147">5</span><span class="sxs-lookup"><span data-stu-id="06e30-147">5</span></span>      |
| <span data-ttu-id="06e30-148">Vuotuinen poisto</span><span class="sxs-lookup"><span data-stu-id="06e30-148">Yearly depreciation</span></span> | <span data-ttu-id="06e30-149">2 000</span><span class="sxs-lookup"><span data-stu-id="06e30-149">2,000</span></span>  |

<span data-ttu-id="06e30-150">Poiston määrä on sama vuosittain: (hankintahinta-jäännösarvo) / käyttövuodet</span><span class="sxs-lookup"><span data-stu-id="06e30-150">The depreciation amount is the same every year: (Acquisition cost – Salvage value) ÷ Service life years</span></span>

| <span data-ttu-id="06e30-151">Kausi</span><span class="sxs-lookup"><span data-stu-id="06e30-151">Period</span></span> | <span data-ttu-id="06e30-152">Vuotuisen poistomäärän laskeminen</span><span class="sxs-lookup"><span data-stu-id="06e30-152">Calculation of the yearly depreciation amount</span></span> | <span data-ttu-id="06e30-153">Nettokirjanpitoarvo vuoden lopussa:</span><span class="sxs-lookup"><span data-stu-id="06e30-153">Net book value at the end of the year</span></span> |
|--------|-----------------------------------------------|---------------------------------------|
| <span data-ttu-id="06e30-154">Vuosi 1</span><span class="sxs-lookup"><span data-stu-id="06e30-154">Year 1</span></span> | <span data-ttu-id="06e30-155">(11 000 – 1 000) ÷ 5 = 2 000</span><span class="sxs-lookup"><span data-stu-id="06e30-155">(11,000 – 1,000) ÷ 5 = 2,000</span></span>                  | <span data-ttu-id="06e30-156">−9 000</span><span class="sxs-lookup"><span data-stu-id="06e30-156">9,000</span></span>                                 |
| <span data-ttu-id="06e30-157">Vuosi 2</span><span class="sxs-lookup"><span data-stu-id="06e30-157">Year 2</span></span> | <span data-ttu-id="06e30-158">(9 000 – 1 000) ÷ 4 = 2 000</span><span class="sxs-lookup"><span data-stu-id="06e30-158">(9,000 – 1,000) ÷ 4 = 2,000</span></span>                   | <span data-ttu-id="06e30-159">7 000</span><span class="sxs-lookup"><span data-stu-id="06e30-159">7,000</span></span>                                 |
| <span data-ttu-id="06e30-160">Vuosi 3</span><span class="sxs-lookup"><span data-stu-id="06e30-160">Year 3</span></span> | <span data-ttu-id="06e30-161">(7 000 – 1 000) ÷ 3 = 2 000</span><span class="sxs-lookup"><span data-stu-id="06e30-161">(7,000 – 1,000) ÷ 3 = 2,000</span></span>                   | <span data-ttu-id="06e30-162">5 000</span><span class="sxs-lookup"><span data-stu-id="06e30-162">5,000</span></span>                                 |
| <span data-ttu-id="06e30-163">Vuosi 4</span><span class="sxs-lookup"><span data-stu-id="06e30-163">Year 4</span></span> | <span data-ttu-id="06e30-164">(5 000 – 1 000) ÷ 2 = 2 000</span><span class="sxs-lookup"><span data-stu-id="06e30-164">(5,000 – 1,000) ÷ 2 = 2,000</span></span>                   | <span data-ttu-id="06e30-165">3 000</span><span class="sxs-lookup"><span data-stu-id="06e30-165">3,000</span></span>                                 |
| <span data-ttu-id="06e30-166">Vuosi 5</span><span class="sxs-lookup"><span data-stu-id="06e30-166">Year 5</span></span> | <span data-ttu-id="06e30-167">(3 000 – 1 000) ÷ 1 = 2 000</span><span class="sxs-lookup"><span data-stu-id="06e30-167">(3,000 – 1,000) ÷ 1 = 2,000</span></span>                   | <span data-ttu-id="06e30-168">1 000</span><span class="sxs-lookup"><span data-stu-id="06e30-168">1,000</span></span>                                 |






