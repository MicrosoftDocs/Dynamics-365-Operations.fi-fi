---
title: "Korkoryhmän korkoprosenttien määrittäminen"
description: "Korkokoodit sisältävät asetukset, joilla määritetään, milloin korkoa veloitetaan ja miten se lasketaan erääntyneillä tileillä."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 01/12/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 59402
ms.assetid: 3b945333-1eaf-4658-ab5a-1a7791a7eb40
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 63bf043124797b328116fd7951913eaeda6ff97b
ms.openlocfilehash: c79b85f95ccb4164e33d6b559b23f740c555907f
ms.contentlocale: fi-fi
ms.lasthandoff: 01/12/2018

---

# <a name="set-up-interest-rates-for-an-interest-code"></a><span data-ttu-id="21f11-103">Korkoryhmän korkoprosenttien määrittäminen</span><span class="sxs-lookup"><span data-stu-id="21f11-103">Set up interest rates for an interest code</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="21f11-104">Korkokoodit sisältävät asetukset, joilla määritetään, milloin korkoa veloitetaan ja miten se lasketaan erääntyneillä tileillä.</span><span class="sxs-lookup"><span data-stu-id="21f11-104">Interest codes contain settings that determine when interest is charged and how it is calculated on overdue accounts.</span></span>

<span data-ttu-id="21f11-105">Voit määrittää yksittäisen korkokoodin ja käyttää sitä useassa asiakaskirjausprofiilissa, laskutuskoodeissa tai tietyillä laskuriviellä.</span><span class="sxs-lookup"><span data-stu-id="21f11-105">You can set up a single interest code and apply it to multiple customer posting profiles, billing codes, or to specific invoice lines.</span></span> <span data-ttu-id="21f11-106">Kun korkokoodin tietoja muutetaan, kaikki koodia käyttävät toiminnot käyttävät automaattisesti muutoksia uusissa tapahtumissa.</span><span class="sxs-lookup"><span data-stu-id="21f11-106">When the interest code details are changed, all features that use the code will automatically implement the changes on new transactions.</span></span> <span data-ttu-id="21f11-107">Kullekin korkokoodille voi määrittää kahdentyyppisiä tuloja:</span><span class="sxs-lookup"><span data-stu-id="21f11-107">For each interest code, you can set up two types of rates:</span></span>
-   <span data-ttu-id="21f11-108">Tulot korkoansioista – Nämä ovat tuloja, jotka on ansaittu veloittamalla korkoa laskuista tai korkolaskuista.</span><span class="sxs-lookup"><span data-stu-id="21f11-108">Rates for interest earnings − These represent revenue that is earned by charging interest on invoices or interest notes.</span></span>
-   <span data-ttu-id="21f11-109">TUlost kokorkomaksuista – Nämä ovat kustannuksia, jotka maksetaan korkolaskujen koroista.</span><span class="sxs-lookup"><span data-stu-id="21f11-109">Rates for interest payments − These represent a cost that is paid for interest on credit notes.</span></span>

<span data-ttu-id="21f11-110">Molemmat korkotyypit voivat olla olemassa samanaikaisesti ja samassa korkokoodissa.</span><span class="sxs-lookup"><span data-stu-id="21f11-110">Both of these rate types can exist at the same time and in the same interest code.</span></span> <span data-ttu-id="21f11-111">Korot voivat perustua kolmeen laskentatyyppin:</span><span class="sxs-lookup"><span data-stu-id="21f11-111">Interest rates can be based on three calculation types:</span></span>
-   <span data-ttu-id="21f11-112">Korko prosenttiosuuden mukaan.</span><span class="sxs-lookup"><span data-stu-id="21f11-112">Interest by percentage.</span></span>
-   <span data-ttu-id="21f11-113">Korko summan mukaan.</span><span class="sxs-lookup"><span data-stu-id="21f11-113">Interest by amount.</span></span>
-   <span data-ttu-id="21f11-114">Korko alueen mukaan, joka tuottaa yhden prosenttiosuuden tai summan.</span><span class="sxs-lookup"><span data-stu-id="21f11-114">Interest by range, which results in a single percentage or amount.</span></span>

<span data-ttu-id="21f11-115">Kun korkokoodia käytetään koron laskennassa, luodaan erillinen korkolasku kutakin korkotasoa varten, joka on voimassa sinä aikana, jonka maksu on ylittänyt tapahtuman eräpäivän.</span><span class="sxs-lookup"><span data-stu-id="21f11-115">When an interest code is used to calculate interest, a separate interest note is created for each interest rate that is in effect during the time that the payment has exceeded the transaction due date.</span></span> <span data-ttu-id="21f11-116">Voit määrittää **Korkoryhmä**-sivun **Ansiot**-välilehdessä korkotasot koroille, jotka ansaitaan veloittamalla korkoa.</span><span class="sxs-lookup"><span data-stu-id="21f11-116">You use the **Earnings** tab on the **Interest code** page to set up interest rates for interest that you earn by charging interest.</span></span> <span data-ttu-id="21f11-117">Määritä korkotasot itse maksamillesi koroille **Maksut**-välilehdessä.</span><span class="sxs-lookup"><span data-stu-id="21f11-117">Use the **Payments** tab to set up interest rates for interest that you pay.</span></span>

## <a name="interest-rates-based-on-a-percentage"></a><span data-ttu-id="21f11-118">Prosenttiosuuksiin perustuvat korkotasot</span><span class="sxs-lookup"><span data-stu-id="21f11-118">Interest rates based on a percentage</span></span>
<span data-ttu-id="21f11-119">Voit määrittää korkotasot, jotka laskevat määritetyn prosenttiosuuden.</span><span class="sxs-lookup"><span data-stu-id="21f11-119">You can set up interest rates that calculate a specified percentage.</span></span>

-   <span data-ttu-id="21f11-120">Korkosumman koskee kaikkia valuuttoja.</span><span class="sxs-lookup"><span data-stu-id="21f11-120">Interest amount applies to all currencies.</span></span>
-   <span data-ttu-id="21f11-121">Korkosumman rajojen antaminen on valinnaista.</span><span class="sxs-lookup"><span data-stu-id="21f11-121">Optional interest amount limits can be entered.</span></span>
-   <span data-ttu-id="21f11-122">**Prosentti** valitaan **Korkokoodien määrittäminen** -sivun **Käytä korkolaskennan perusteena** -kentässä.</span><span class="sxs-lookup"><span data-stu-id="21f11-122">**Percentage** is selected** **in the **Calculate interest based on** field on the **Set up Interest codes** page.</span></span>

<span data-ttu-id="21f11-123">Jos esimerkiksi haluat määrittää korkokoodin, joka määrää 5 prosentin koron jokaista kahta kuukautta kohti, jonka laskun maksaminen ylittää tapahtuman eräpäivän, anna arvo 2 **Koronlaskentaväli**-kenttään ja valitse **Kuukausi**.</span><span class="sxs-lookup"><span data-stu-id="21f11-123">For example, to set up an interest code that assesses 5 percent interest for every two months that the invoice payment exceeds the transaction due date, you would enter 2 in the **Calculate interest every** field and select **Month**.</span></span>

## <a name="interest-rates-based-on-amounts"></a><span data-ttu-id="21f11-124">Summin perustuvat korkotasot</span><span class="sxs-lookup"><span data-stu-id="21f11-124">Interest rates based on amounts</span></span>
<span data-ttu-id="21f11-125">Voit määrittää korkotasot, jotka laskevat määritetyn summan valuuttaa kohden.</span><span class="sxs-lookup"><span data-stu-id="21f11-125">You can set up interest rates that calculate a specified amount per currency.</span></span>
-   <span data-ttu-id="21f11-126">Korkosumma on määritettävä jokaiselle korkokoodin valuutalle.</span><span class="sxs-lookup"><span data-stu-id="21f11-126">An interest amount is specified for each currency in the interest code.</span></span>
-   <span data-ttu-id="21f11-127">Korkosumman rajojen antaminen on valinnaista.</span><span class="sxs-lookup"><span data-stu-id="21f11-127">Optional interest amount limits can be entered.</span></span>
-   <span data-ttu-id="21f11-128">**Summa** valitaan **Korkokoodien määrittäminen** -sivun **Käytä korkolaskennan perusteena** -kentässä.</span><span class="sxs-lookup"><span data-stu-id="21f11-128">**Amount **is selected in the **Calculate interest based on** field on the **Set up Interest codes** page.</span></span>

<span data-ttu-id="21f11-129">Jos esimerkiksi haluat määrittää korkokoodin, joka määrää 25,00 valuuttayksikön koron jokaista 20 päivää kohti, jonka laskun maksaminen ylittää tapahtuman eräpäivän, anna arvo 20 **Koronlaskentaväli**-kentässä ja valitse **Päivä**.</span><span class="sxs-lookup"><span data-stu-id="21f11-129">For example, to set up an interest code that assesses interest of 25.00 for every 20 days that the invoice payment exceeds the transaction due date, you would enter 20 in the **Calculate interest every** field and select **Day**.</span></span>

## <a name="interest-rates-based-on-ranges"></a><span data-ttu-id="21f11-130">Alueisiin perustuvat korkotasot</span><span class="sxs-lookup"><span data-stu-id="21f11-130">Interest rates based on ranges</span></span>
<span data-ttu-id="21f11-131">Voit määrittää korkotasot, jotka vaihtelevat myöhässä olevan summan, summan myöhässä olevien päivien määrän tai summan myöhässä olevien kuukausien määrän mukaan.</span><span class="sxs-lookup"><span data-stu-id="21f11-131">You can set up interest rates that vary depending on the overdue amount, the number of days that the amount is late, or the number of months that the amount is late.</span></span>
-   <span data-ttu-id="21f11-132">Voit määrittää kunkin valuutan korkoasetukset **Ansiot valuutan mukaan** -välilehdessä.</span><span class="sxs-lookup"><span data-stu-id="21f11-132">You can use the **Earnings by Currency** tab to define specific interest settings for each currency.</span></span> <span data-ttu-id="21f11-133">Myös alue määritetään tässä välilehdessä.</span><span class="sxs-lookup"><span data-stu-id="21f11-133">This is also where you will define the range.</span></span>
-   <span data-ttu-id="21f11-134">Lisää **Alueet**-painikkeella rivit, jotka ilmaisevat määritettäviä alueita.</span><span class="sxs-lookup"><span data-stu-id="21f11-134">Use the **Ranges** button to add lines that represent the ranges that you want to set up.</span></span> <span data-ttu-id="21f11-135">**Mistä**-arvo ilmaisee alueen alkamiskohdan ja **Korkoarvo**-luku ilmaisee joko prosentin tai summan sen mukaan, mitä **Korkokoodien määrittäminen** -sivun **Käytä korkolaskennan perusteena** -kentässä on valittu.</span><span class="sxs-lookup"><span data-stu-id="21f11-135">The **From** value represents the beginning of the range and the **Interest value** number represents either a percentage or an amount, depending on the selection in the **Calculate interest based on** field on the **Set up Interest codes** page.</span></span>

## <a name="example-1-interest-by-range--amount"></a><span data-ttu-id="21f11-136">Esimerkki 1: Korko alueen mukaan = summa</span><span class="sxs-lookup"><span data-stu-id="21f11-136">Example 1: Interest by range = Amount</span></span>
<span data-ttu-id="21f11-137">Määrität korkokoodin, joka arvioi koron kerran jokaista kolmea kuukautta kohden, jonka laskun maksu on myöhässä tapahtuman eräpäivästä.</span><span class="sxs-lookup"><span data-stu-id="21f11-137">You set up an interest code that assesses interest one time for every three months that the invoice payment exceeds the transaction due date.</span></span> <span data-ttu-id="21f11-138">Haluat laskennan perustuvan prosentuaaliseen korkoarvoon askeleittaisten summavälien mukaan.</span><span class="sxs-lookup"><span data-stu-id="21f11-138">You want to base the calculation on a percentage interest value, according to stepped amount intervals.</span></span> <span data-ttu-id="21f11-139">Koron arvo on 1 prosentti laskun summasta summaan 1 000,00 saakka, 2 prosenttia summasta välillä 1 001,00–5 000,00 ja 3 prosenttia yli 5 000,00:n summista.</span><span class="sxs-lookup"><span data-stu-id="21f11-139">The interest value will be 1 percent for invoice amounts up to 1,000.00, 2 percent for amounts from 1,001.00 to 5,000.00, and 3 percent for amounts larger than 5,000.00.</span></span> <span data-ttu-id="21f11-140">Määrität korkokoodin kenttien arvot seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="21f11-140">You set up the interest code field values as follows.</span></span>

| <span data-ttu-id="21f11-141">**Kentän nimi**</span><span class="sxs-lookup"><span data-stu-id="21f11-141">**Field name**</span></span>                  | <span data-ttu-id="21f11-142">**Kentän arvo**</span><span class="sxs-lookup"><span data-stu-id="21f11-142">**Field value**</span></span> |
|---------------------------------|-----------------|
| <span data-ttu-id="21f11-143">**Korkoryhmä**</span><span class="sxs-lookup"><span data-stu-id="21f11-143">**Interest code**</span></span>               | <span data-ttu-id="21f11-144">3M%ByAmt</span><span class="sxs-lookup"><span data-stu-id="21f11-144">3M%ByAmt</span></span>        |
| <span data-ttu-id="21f11-145">**Koronlaskentaväli**</span><span class="sxs-lookup"><span data-stu-id="21f11-145">**Calculate interest every**</span></span>    | <span data-ttu-id="21f11-146">3/kuukausi</span><span class="sxs-lookup"><span data-stu-id="21f11-146">3/Month</span></span>         |
| <span data-ttu-id="21f11-147">**Korko alueen mukaan**</span><span class="sxs-lookup"><span data-stu-id="21f11-147">**Interest by range**</span></span>           | <span data-ttu-id="21f11-148">Summa</span><span class="sxs-lookup"><span data-stu-id="21f11-148">Amount</span></span>          |
| <span data-ttu-id="21f11-149">**Käytä korkolaskennan perusteena**</span><span class="sxs-lookup"><span data-stu-id="21f11-149">**Calculate interest based on**</span></span> | <span data-ttu-id="21f11-150">Prosentti</span><span class="sxs-lookup"><span data-stu-id="21f11-150">Percentage</span></span>      |

<span data-ttu-id="21f11-151">Määrität alueen tiedot seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="21f11-151">You set up the range information as follows.</span></span>

| <span data-ttu-id="21f11-152">**Arvosta**</span><span class="sxs-lookup"><span data-stu-id="21f11-152">**From value**</span></span> | <span data-ttu-id="21f11-153">**Korkoarvo**</span><span class="sxs-lookup"><span data-stu-id="21f11-153">**Interest value**</span></span> |
|----------------|--------------------|
| <span data-ttu-id="21f11-154">0</span><span class="sxs-lookup"><span data-stu-id="21f11-154">0</span></span>              | <span data-ttu-id="21f11-155">1</span><span class="sxs-lookup"><span data-stu-id="21f11-155">1</span></span>                  |
| <span data-ttu-id="21f11-156">1,001</span><span class="sxs-lookup"><span data-stu-id="21f11-156">1,001</span></span>          | <span data-ttu-id="21f11-157">2</span><span class="sxs-lookup"><span data-stu-id="21f11-157">2</span></span>                  |
| <span data-ttu-id="21f11-158">5,001</span><span class="sxs-lookup"><span data-stu-id="21f11-158">5,001</span></span>          | <span data-ttu-id="21f11-159">3</span><span class="sxs-lookup"><span data-stu-id="21f11-159">3</span></span>                  |

 
## <a name="example-2-interest-by-range--days"></a><span data-ttu-id="21f11-160">Esimerkki 2: Korko alueen mukaan = päivät</span><span class="sxs-lookup"><span data-stu-id="21f11-160">Example 2: Interest by range = Days</span></span>
--------------------------------------------------

<span data-ttu-id="21f11-161">Määrität korkokoodin, joka arvioi koron kerran jokaista 15 päivää kohden, jonka laskun maksu on myöhässä tapahtuman eräpäivästä.</span><span class="sxs-lookup"><span data-stu-id="21f11-161">You set up an interest code that assesses interest one time for every 15 days that the invoice payment exceeds the transaction due date.</span></span> <span data-ttu-id="21f11-162">Haluat laskennan perustuvan summan korkoarvoon askeleittaisten päivävälien mukaan.</span><span class="sxs-lookup"><span data-stu-id="21f11-162">You want to base the calculation on an amount interest value, according to stepped day intervals.</span></span> <span data-ttu-id="21f11-163">Koron arvo on 10,00 kutakin 15 päivää kohden 60 ensimmäisen päivän ajan, 15,00 kutakin 15 päivää kohden päivien 61–90 ajan ja 20,00 kutakin 15 päivää kohden päivän 91 ja sen jälkeisten päivien ajan.</span><span class="sxs-lookup"><span data-stu-id="21f11-163">The interest value will be 10.00 per 15 days during the first 60 days, 15.00 per 15 days during days 61 to 90, and 20.00 per 15 days from day 91 and after.</span></span> <span data-ttu-id="21f11-164">Määrität korkokoodin kenttien arvot seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="21f11-164">You set up the interest code field values as follows.</span></span>

| <span data-ttu-id="21f11-165">**Kentän nimi**</span><span class="sxs-lookup"><span data-stu-id="21f11-165">**Field name**</span></span>                  | <span data-ttu-id="21f11-166">**Kentän arvo**</span><span class="sxs-lookup"><span data-stu-id="21f11-166">**Field value**</span></span> |
|---------------------------------|-----------------|
| <span data-ttu-id="21f11-167">**Korkoryhmä**</span><span class="sxs-lookup"><span data-stu-id="21f11-167">**Interest code**</span></span>               | <span data-ttu-id="21f11-168">15DAmtXDay</span><span class="sxs-lookup"><span data-stu-id="21f11-168">15DAmtXDay</span></span>      |
| <span data-ttu-id="21f11-169">**Koronlaskentaväli**</span><span class="sxs-lookup"><span data-stu-id="21f11-169">**Calculate interest every**</span></span>    | <span data-ttu-id="21f11-170">15/päivä</span><span class="sxs-lookup"><span data-stu-id="21f11-170">15/Day</span></span>          |
| <span data-ttu-id="21f11-171">**Korko alueen mukaan**</span><span class="sxs-lookup"><span data-stu-id="21f11-171">**Interest by range**</span></span>           | <span data-ttu-id="21f11-172">Päivää</span><span class="sxs-lookup"><span data-stu-id="21f11-172">Days</span></span>            |
| <span data-ttu-id="21f11-173">**Käytä korkolaskennan perusteena**</span><span class="sxs-lookup"><span data-stu-id="21f11-173">**Calculate interest based on**</span></span> | <span data-ttu-id="21f11-174">Summa</span><span class="sxs-lookup"><span data-stu-id="21f11-174">Amount</span></span>          |

<span data-ttu-id="21f11-175">Määrität alueen tiedot seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="21f11-175">You set up the range information as follows.</span></span>

| <span data-ttu-id="21f11-176">**Arvosta**</span><span class="sxs-lookup"><span data-stu-id="21f11-176">**From value**</span></span> | <span data-ttu-id="21f11-177">**Korkoarvo**</span><span class="sxs-lookup"><span data-stu-id="21f11-177">**Interest value**</span></span> |
|----------------|--------------------|
| <span data-ttu-id="21f11-178">0</span><span class="sxs-lookup"><span data-stu-id="21f11-178">0</span></span>              | <span data-ttu-id="21f11-179">10</span><span class="sxs-lookup"><span data-stu-id="21f11-179">10</span></span>                 |
| <span data-ttu-id="21f11-180">61</span><span class="sxs-lookup"><span data-stu-id="21f11-180">61</span></span>             | <span data-ttu-id="21f11-181">15</span><span class="sxs-lookup"><span data-stu-id="21f11-181">15</span></span>                 |
| <span data-ttu-id="21f11-182">91</span><span class="sxs-lookup"><span data-stu-id="21f11-182">91</span></span>             | <span data-ttu-id="21f11-183">20</span><span class="sxs-lookup"><span data-stu-id="21f11-183">20</span></span>                 |

 
## <a name="example-3-interest-by-range--months"></a><span data-ttu-id="21f11-184">Esimerkki 3: Korko alueen mukaan = kuukaudet</span><span class="sxs-lookup"><span data-stu-id="21f11-184">Example 3: Interest by range = Months</span></span>
----------------------------------------------------

<span data-ttu-id="21f11-185">Määrität korkokoodin, joka arvioi koron kerran jokaista kuukautta kohden, jonka laskun maksu on myöhässä tapahtuman eräpäivästä.</span><span class="sxs-lookup"><span data-stu-id="21f11-185">You set up an interest code that assesses interest one time for every month that the invoice payment exceeds the transaction due date.</span></span> <span data-ttu-id="21f11-186">Haluat laskennan perustuvan prosentuaaliseen korkoarvoon askeleittaisten kuukausivälien mukaan.</span><span class="sxs-lookup"><span data-stu-id="21f11-186">You want to base the calculation on a percentage interest value, according to stepped month intervals.</span></span> <span data-ttu-id="21f11-187">Koron arvo on 1,5 prosenttia kuukaudessa eräpäivän jälkeisen kolmen ensimmäisen kuukauden ajan, 2,0 prosenttia kuukaudessa toisen kolmen kuukauden jakson ajan ja 2,5 prosenttia kuukaudessa kuuden ensimmäisen kuukauden jälkeen.</span><span class="sxs-lookup"><span data-stu-id="21f11-187">The interest value will be 1.5 percent per month for the first three overdue months, 2.0 percent per month for the second three months, and 2.5 percent per month for each month beyond the first six months.</span></span> <span data-ttu-id="21f11-188">Määrität korkokoodin kenttien arvot seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="21f11-188">You set up the interest code field values as follows.</span></span>

| <span data-ttu-id="21f11-189">**Kentän nimi**</span><span class="sxs-lookup"><span data-stu-id="21f11-189">**Field name**</span></span>                  | <span data-ttu-id="21f11-190">**Kentän arvo**</span><span class="sxs-lookup"><span data-stu-id="21f11-190">**Field value**</span></span> |
|---------------------------------|-----------------|
| <span data-ttu-id="21f11-191">**Korkoryhmä**</span><span class="sxs-lookup"><span data-stu-id="21f11-191">**Interest code**</span></span>               | <span data-ttu-id="21f11-192">1M%ByMth</span><span class="sxs-lookup"><span data-stu-id="21f11-192">1M%ByMth</span></span>        |
| <span data-ttu-id="21f11-193">**Koronlaskentaväli**</span><span class="sxs-lookup"><span data-stu-id="21f11-193">**Calculate interest every**</span></span>    | <span data-ttu-id="21f11-194">1/kuukausi</span><span class="sxs-lookup"><span data-stu-id="21f11-194">1/Month</span></span>         |
| <span data-ttu-id="21f11-195">**Korko alueen mukaan**</span><span class="sxs-lookup"><span data-stu-id="21f11-195">**Interest by range**</span></span>           | <span data-ttu-id="21f11-196">Kuukautta</span><span class="sxs-lookup"><span data-stu-id="21f11-196">Months</span></span>          |
| <span data-ttu-id="21f11-197">**Käytä korkolaskennan perusteena**</span><span class="sxs-lookup"><span data-stu-id="21f11-197">**Calculate interest based on**</span></span> | <span data-ttu-id="21f11-198">Prosentti</span><span class="sxs-lookup"><span data-stu-id="21f11-198">Percentage</span></span>      |

<span data-ttu-id="21f11-199">Määrität alueen tiedot seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="21f11-199">You set up the range information as follows.</span></span>

| <span data-ttu-id="21f11-200">**Arvosta**</span><span class="sxs-lookup"><span data-stu-id="21f11-200">**From value**</span></span> | <span data-ttu-id="21f11-201">**Korkoarvo**</span><span class="sxs-lookup"><span data-stu-id="21f11-201">**Interest value**</span></span> |
|----------------|--------------------|
| <span data-ttu-id="21f11-202">0</span><span class="sxs-lookup"><span data-stu-id="21f11-202">0</span></span>              | <span data-ttu-id="21f11-203">1.5</span><span class="sxs-lookup"><span data-stu-id="21f11-203">1.5</span></span>                |
| <span data-ttu-id="21f11-204">4</span><span class="sxs-lookup"><span data-stu-id="21f11-204">4</span></span>              | <span data-ttu-id="21f11-205">2</span><span class="sxs-lookup"><span data-stu-id="21f11-205">2</span></span>                  |
| <span data-ttu-id="21f11-206">7</span><span class="sxs-lookup"><span data-stu-id="21f11-206">7</span></span>              | <span data-ttu-id="21f11-207">2,5</span><span class="sxs-lookup"><span data-stu-id="21f11-207">2.5</span></span>                |

## <a name="new-versions"></a><span data-ttu-id="21f11-208">Uudet versiot</span><span class="sxs-lookup"><span data-stu-id="21f11-208">New versions</span></span>
<span data-ttu-id="21f11-209">Korkokoodeilla on voimassaolopäivät.</span><span class="sxs-lookup"><span data-stu-id="21f11-209">Interest codes are date effective.</span></span> <span data-ttu-id="21f11-210">Jos haluat muokata korkoprosenttia, voit luoda **uuden version**, jonka voimassaolo alkaa tiettynä päivänä tulevaisuudessa.</span><span class="sxs-lookup"><span data-stu-id="21f11-210">If you want to modify the interest rate, you can create a **new version** that is effective as of a future date.</span></span>

<span data-ttu-id="21f11-211">Voit tarkastella eri versioita valitsemalla **Alkupäivämäärä**-valikkovaihtoehdolla katkaisupäivämäärän.</span><span class="sxs-lookup"><span data-stu-id="21f11-211">To view different versions, you can use the **As of Date** menu choice to select the cutoff date.</span></span> <span data-ttu-id="21f11-212">Jos haluat tarkastella kaikkia sivun korkoprosentteja, valitse **Näytä kaikki tietueet**.</span><span class="sxs-lookup"><span data-stu-id="21f11-212">You can also select the **Display all records** to view all interest codes in the page.</span></span>




