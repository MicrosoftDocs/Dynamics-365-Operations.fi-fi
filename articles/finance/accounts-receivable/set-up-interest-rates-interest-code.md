---
title: Korkoryhmän korkoprosenttien määrittäminen
description: Korkokoodit sisältävät asetukset, joilla määritetään, milloin korkoa veloitetaan ja miten se lasketaan erääntyneillä tileillä.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 01/12/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: Interest
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 59402
ms.assetid: 3b945333-1eaf-4658-ab5a-1a7791a7eb40
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a3ca43503ecbe8e814958576e46ced10bfe9ad49
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/13/2020
ms.locfileid: "4442668"
---
# <a name="set-up-interest-rates-for-an-interest-code"></a><span data-ttu-id="93dde-103">Korkoryhmän korkoprosenttien määrittäminen</span><span class="sxs-lookup"><span data-stu-id="93dde-103">Set up interest rates for an interest code</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="93dde-104">Korkokoodit sisältävät asetukset, joilla määritetään, milloin korkoa veloitetaan ja miten se lasketaan erääntyneillä tileillä.</span><span class="sxs-lookup"><span data-stu-id="93dde-104">Interest codes contain settings that determine when interest is charged and how it is calculated on overdue accounts.</span></span>

<span data-ttu-id="93dde-105">Voit määrittää yksittäisen korkokoodin ja käyttää sitä useassa asiakaskirjausprofiilissa, laskutuskoodeissa tai tietyillä laskuriviellä.</span><span class="sxs-lookup"><span data-stu-id="93dde-105">You can set up a single interest code and apply it to multiple customer posting profiles, billing codes, or to specific invoice lines.</span></span> <span data-ttu-id="93dde-106">Kun korkokoodin tietoja muutetaan, kaikki koodia käyttävät toiminnot käyttävät automaattisesti muutoksia uusissa tapahtumissa.</span><span class="sxs-lookup"><span data-stu-id="93dde-106">When the interest code details are changed, all features that use the code will automatically implement the changes on new transactions.</span></span> <span data-ttu-id="93dde-107">Kullekin korkokoodille voi määrittää kahdentyyppisiä tuloja:</span><span class="sxs-lookup"><span data-stu-id="93dde-107">For each interest code, you can set up two types of rates:</span></span>
-   <span data-ttu-id="93dde-108">Tulot korkoansioista – Nämä ovat tuloja, jotka on ansaittu veloittamalla korkoa laskuista tai korkolaskuista.</span><span class="sxs-lookup"><span data-stu-id="93dde-108">Rates for interest earnings − These represent revenue that is earned by charging interest on invoices or interest notes.</span></span>
-   <span data-ttu-id="93dde-109">TUlost kokorkomaksuista – Nämä ovat kustannuksia, jotka maksetaan korkolaskujen koroista.</span><span class="sxs-lookup"><span data-stu-id="93dde-109">Rates for interest payments − These represent a cost that is paid for interest on credit notes.</span></span>

<span data-ttu-id="93dde-110">Molemmat korkotyypit voivat olla olemassa samanaikaisesti ja samassa korkokoodissa.</span><span class="sxs-lookup"><span data-stu-id="93dde-110">Both of these rate types can exist at the same time and in the same interest code.</span></span> <span data-ttu-id="93dde-111">Korot voivat perustua kolmeen laskentatyyppin:</span><span class="sxs-lookup"><span data-stu-id="93dde-111">Interest rates can be based on three calculation types:</span></span>
-   <span data-ttu-id="93dde-112">Korko prosenttiosuuden mukaan.</span><span class="sxs-lookup"><span data-stu-id="93dde-112">Interest by percentage.</span></span>
-   <span data-ttu-id="93dde-113">Korko summan mukaan.</span><span class="sxs-lookup"><span data-stu-id="93dde-113">Interest by amount.</span></span>
-   <span data-ttu-id="93dde-114">Korko alueen mukaan, joka tuottaa yhden prosenttiosuuden tai summan.</span><span class="sxs-lookup"><span data-stu-id="93dde-114">Interest by range, which results in a single percentage or amount.</span></span>

<span data-ttu-id="93dde-115">Kun korkokoodia käytetään koron laskennassa, luodaan erillinen korkolasku kutakin korkotasoa varten, joka on voimassa sinä aikana, jonka maksu on ylittänyt tapahtuman eräpäivän.</span><span class="sxs-lookup"><span data-stu-id="93dde-115">When an interest code is used to calculate interest, a separate interest note is created for each interest rate that is in effect during the time that the payment has exceeded the transaction due date.</span></span> <span data-ttu-id="93dde-116">Voit määrittää **Korkoryhmä**-sivun **Ansiot**-välilehdessä korkotasot koroille, jotka ansaitaan veloittamalla korkoa.</span><span class="sxs-lookup"><span data-stu-id="93dde-116">You use the **Earnings** tab on the **Interest code** page to set up interest rates for interest that you earn by charging interest.</span></span> <span data-ttu-id="93dde-117">Määritä korkotasot itse maksamillesi koroille **Maksut**-välilehdessä.</span><span class="sxs-lookup"><span data-stu-id="93dde-117">Use the **Payments** tab to set up interest rates for interest that you pay.</span></span>

## <a name="interest-rates-based-on-a-percentage"></a><span data-ttu-id="93dde-118">Prosenttiosuuksiin perustuvat korkotasot</span><span class="sxs-lookup"><span data-stu-id="93dde-118">Interest rates based on a percentage</span></span>
<span data-ttu-id="93dde-119">Voit määrittää korkotasot, jotka laskevat määritetyn prosenttiosuuden.</span><span class="sxs-lookup"><span data-stu-id="93dde-119">You can set up interest rates that calculate a specified percentage.</span></span>

- <span data-ttu-id="93dde-120">Korkosumman koskee kaikkia valuuttoja.</span><span class="sxs-lookup"><span data-stu-id="93dde-120">Interest amount applies to all currencies.</span></span>
- <span data-ttu-id="93dde-121">Korkosumman rajojen antaminen on valinnaista.</span><span class="sxs-lookup"><span data-stu-id="93dde-121">Optional interest amount limits can be entered.</span></span>
- <span data-ttu-id="93dde-122"><strong>Prosentti</strong> valitaan\*\* <strong>Korkokoodien määrittäminen</strong> -sivun <strong>\*\*Käytä korkolaskennan perusteena</strong> -kentässä.</span><span class="sxs-lookup"><span data-stu-id="93dde-122"><strong>Percentage</strong> is selected\*\* <strong>in the \*\*Calculate interest based on</strong> field on the <strong>Set up Interest codes</strong> page.</span></span>

<span data-ttu-id="93dde-123">Jos esimerkiksi haluat määrittää korkokoodin, joka määrää 5 prosentin koron jokaista kahta kuukautta kohti, jonka laskun maksaminen ylittää tapahtuman eräpäivän, anna arvo 2 **Koronlaskentaväli**-kenttään ja valitse **Kuukausi**.</span><span class="sxs-lookup"><span data-stu-id="93dde-123">For example, to set up an interest code that assesses 5 percent interest for every two months that the invoice payment exceeds the transaction due date, you would enter 2 in the **Calculate interest every** field and select **Month**.</span></span>

## <a name="interest-rates-based-on-amounts"></a><span data-ttu-id="93dde-124">Summin perustuvat korkotasot</span><span class="sxs-lookup"><span data-stu-id="93dde-124">Interest rates based on amounts</span></span>
<span data-ttu-id="93dde-125">Voit määrittää korkotasot, jotka laskevat määritetyn summan valuuttaa kohden.</span><span class="sxs-lookup"><span data-stu-id="93dde-125">You can set up interest rates that calculate a specified amount per currency.</span></span>
- <span data-ttu-id="93dde-126">Korkosumma on määritettävä jokaiselle korkokoodin valuutalle.</span><span class="sxs-lookup"><span data-stu-id="93dde-126">An interest amount is specified for each currency in the interest code.</span></span>
- <span data-ttu-id="93dde-127">Korkosumman rajojen antaminen on valinnaista.</span><span class="sxs-lookup"><span data-stu-id="93dde-127">Optional interest amount limits can be entered.</span></span>
- <span data-ttu-id="93dde-128">**Summa** valitaan **Korkokoodien määrittäminen** -sivun **Käytä korkolaskennan perusteena** -kentässä.</span><span class="sxs-lookup"><span data-stu-id="93dde-128">**Amount** is selected in the **Calculate interest based on** field on the **Set up Interest codes** page.</span></span>

<span data-ttu-id="93dde-129">Jos esimerkiksi haluat määrittää korkokoodin, joka määrää 25,00 valuuttayksikön koron jokaista 20 päivää kohti, jonka laskun maksaminen ylittää tapahtuman eräpäivän, anna arvo 20 **Koronlaskentaväli**-kentässä ja valitse **Päivä**.</span><span class="sxs-lookup"><span data-stu-id="93dde-129">For example, to set up an interest code that assesses interest of 25.00 for every 20 days that the invoice payment exceeds the transaction due date, you would enter 20 in the **Calculate interest every** field and select **Day**.</span></span>

## <a name="interest-rates-based-on-ranges"></a><span data-ttu-id="93dde-130">Alueisiin perustuvat korkotasot</span><span class="sxs-lookup"><span data-stu-id="93dde-130">Interest rates based on ranges</span></span>
<span data-ttu-id="93dde-131">Voit määrittää korkotasot, jotka vaihtelevat myöhässä olevan summan, summan myöhässä olevien päivien määrän tai summan myöhässä olevien kuukausien määrän mukaan.</span><span class="sxs-lookup"><span data-stu-id="93dde-131">You can set up interest rates that vary depending on the overdue amount, the number of days that the amount is late, or the number of months that the amount is late.</span></span>
-   <span data-ttu-id="93dde-132">Voit määrittää kunkin valuutan korkoasetukset **Ansiot valuutan mukaan** -välilehdessä.</span><span class="sxs-lookup"><span data-stu-id="93dde-132">You can use the **Earnings by Currency** tab to define specific interest settings for each currency.</span></span> <span data-ttu-id="93dde-133">Myös alue määritetään tässä välilehdessä.</span><span class="sxs-lookup"><span data-stu-id="93dde-133">This is also where you will define the range.</span></span>
-   <span data-ttu-id="93dde-134">Lisää **Alueet**-painikkeella rivit, jotka ilmaisevat määritettäviä alueita.</span><span class="sxs-lookup"><span data-stu-id="93dde-134">Use the **Ranges** button to add lines that represent the ranges that you want to set up.</span></span> <span data-ttu-id="93dde-135">**Mistä**-arvo ilmaisee alueen alkamiskohdan ja **Korkoarvo**-luku ilmaisee joko prosentin tai summan sen mukaan, mitä **Korkokoodien määrittäminen** -sivun **Käytä korkolaskennan perusteena** -kentässä on valittu.</span><span class="sxs-lookup"><span data-stu-id="93dde-135">The **From** value represents the beginning of the range and the **Interest value** number represents either a percentage or an amount, depending on the selection in the **Calculate interest based on** field on the **Set up Interest codes** page.</span></span>

## <a name="example-1-interest-by-range--amount"></a><span data-ttu-id="93dde-136">Esimerkki 1: Korko alueen mukaan = summa</span><span class="sxs-lookup"><span data-stu-id="93dde-136">Example 1: Interest by range = Amount</span></span>
<span data-ttu-id="93dde-137">Määrität korkokoodin, joka arvioi koron kerran jokaista kolmea kuukautta kohden, jonka laskun maksu on myöhässä tapahtuman eräpäivästä.</span><span class="sxs-lookup"><span data-stu-id="93dde-137">You set up an interest code that assesses interest one time for every three months that the invoice payment exceeds the transaction due date.</span></span> <span data-ttu-id="93dde-138">Haluat laskennan perustuvan prosentuaaliseen korkoarvoon askeleittaisten summavälien mukaan.</span><span class="sxs-lookup"><span data-stu-id="93dde-138">You want to base the calculation on a percentage interest value, according to stepped amount intervals.</span></span> <span data-ttu-id="93dde-139">Koron arvo on 1 prosentti laskun summasta summaan 1 000,00 saakka, 2 prosenttia summasta välillä 1 001,00–5 000,00 ja 3 prosenttia yli 5 000,00:n summista.</span><span class="sxs-lookup"><span data-stu-id="93dde-139">The interest value will be 1 percent for invoice amounts up to 1,000.00, 2 percent for amounts from 1,001.00 to 5,000.00, and 3 percent for amounts larger than 5,000.00.</span></span> <span data-ttu-id="93dde-140">Määrität korkokoodin kenttien arvot seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="93dde-140">You set up the interest code field values as follows.</span></span>

| <span data-ttu-id="93dde-141">**Kentän nimi**</span><span class="sxs-lookup"><span data-stu-id="93dde-141">**Field name**</span></span>                  | <span data-ttu-id="93dde-142">**Kentän arvo**</span><span class="sxs-lookup"><span data-stu-id="93dde-142">**Field value**</span></span> |
|---------------------------------|-----------------|
| <span data-ttu-id="93dde-143">**Korkoryhmä**</span><span class="sxs-lookup"><span data-stu-id="93dde-143">**Interest code**</span></span>               | <span data-ttu-id="93dde-144">3M%ByAmt</span><span class="sxs-lookup"><span data-stu-id="93dde-144">3M%ByAmt</span></span>        |
| <span data-ttu-id="93dde-145">**Koronlaskentaväli**</span><span class="sxs-lookup"><span data-stu-id="93dde-145">**Calculate interest every**</span></span>    | <span data-ttu-id="93dde-146">3/kuukausi</span><span class="sxs-lookup"><span data-stu-id="93dde-146">3/Month</span></span>         |
| <span data-ttu-id="93dde-147">**Korko alueen mukaan**</span><span class="sxs-lookup"><span data-stu-id="93dde-147">**Interest by range**</span></span>           | <span data-ttu-id="93dde-148">Summa</span><span class="sxs-lookup"><span data-stu-id="93dde-148">Amount</span></span>          |
| <span data-ttu-id="93dde-149">**Käytä korkolaskennan perusteena**</span><span class="sxs-lookup"><span data-stu-id="93dde-149">**Calculate interest based on**</span></span> | <span data-ttu-id="93dde-150">Prosentti</span><span class="sxs-lookup"><span data-stu-id="93dde-150">Percentage</span></span>      |

<span data-ttu-id="93dde-151">Määrität alueen tiedot seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="93dde-151">You set up the range information as follows.</span></span>

| <span data-ttu-id="93dde-152">**Arvosta**</span><span class="sxs-lookup"><span data-stu-id="93dde-152">**From value**</span></span> | <span data-ttu-id="93dde-153">**Korkoarvo**</span><span class="sxs-lookup"><span data-stu-id="93dde-153">**Interest value**</span></span> |
|----------------|--------------------|
| <span data-ttu-id="93dde-154">0</span><span class="sxs-lookup"><span data-stu-id="93dde-154">0</span></span>              | <span data-ttu-id="93dde-155">1</span><span class="sxs-lookup"><span data-stu-id="93dde-155">1</span></span>                  |
| <span data-ttu-id="93dde-156">1,001</span><span class="sxs-lookup"><span data-stu-id="93dde-156">1,001</span></span>          | <span data-ttu-id="93dde-157">2</span><span class="sxs-lookup"><span data-stu-id="93dde-157">2</span></span>                  |
| <span data-ttu-id="93dde-158">5,001</span><span class="sxs-lookup"><span data-stu-id="93dde-158">5,001</span></span>          | <span data-ttu-id="93dde-159">3</span><span class="sxs-lookup"><span data-stu-id="93dde-159">3</span></span>                  |


## <a name="example-2-interest-by-range--days"></a><span data-ttu-id="93dde-160">Esimerkki 2: Korko alueen mukaan = päivät</span><span class="sxs-lookup"><span data-stu-id="93dde-160">Example 2: Interest by range = Days</span></span>
--------------------------------------------------

<span data-ttu-id="93dde-161">Määrität korkokoodin, joka arvioi koron kerran jokaista 15 päivää kohden, jonka laskun maksu on myöhässä tapahtuman eräpäivästä.</span><span class="sxs-lookup"><span data-stu-id="93dde-161">You set up an interest code that assesses interest one time for every 15 days that the invoice payment exceeds the transaction due date.</span></span> <span data-ttu-id="93dde-162">Haluat laskennan perustuvan summan korkoarvoon askeleittaisten päivävälien mukaan.</span><span class="sxs-lookup"><span data-stu-id="93dde-162">You want to base the calculation on an amount interest value, according to stepped day intervals.</span></span> <span data-ttu-id="93dde-163">Koron arvo on 10,00 kutakin 15 päivää kohden 60 ensimmäisen päivän ajan, 15,00 kutakin 15 päivää kohden päivien 61–90 ajan ja 20,00 kutakin 15 päivää kohden päivän 91 ja sen jälkeisten päivien ajan.</span><span class="sxs-lookup"><span data-stu-id="93dde-163">The interest value will be 10.00 per 15 days during the first 60 days, 15.00 per 15 days during days 61 to 90, and 20.00 per 15 days from day 91 and after.</span></span> <span data-ttu-id="93dde-164">Määrität korkokoodin kenttien arvot seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="93dde-164">You set up the interest code field values as follows.</span></span>

| <span data-ttu-id="93dde-165">**Kentän nimi**</span><span class="sxs-lookup"><span data-stu-id="93dde-165">**Field name**</span></span>                  | <span data-ttu-id="93dde-166">**Kentän arvo**</span><span class="sxs-lookup"><span data-stu-id="93dde-166">**Field value**</span></span> |
|---------------------------------|-----------------|
| <span data-ttu-id="93dde-167">**Korkoryhmä**</span><span class="sxs-lookup"><span data-stu-id="93dde-167">**Interest code**</span></span>               | <span data-ttu-id="93dde-168">15DAmtXDay</span><span class="sxs-lookup"><span data-stu-id="93dde-168">15DAmtXDay</span></span>      |
| <span data-ttu-id="93dde-169">**Koronlaskentaväli**</span><span class="sxs-lookup"><span data-stu-id="93dde-169">**Calculate interest every**</span></span>    | <span data-ttu-id="93dde-170">15/päivä</span><span class="sxs-lookup"><span data-stu-id="93dde-170">15/Day</span></span>          |
| <span data-ttu-id="93dde-171">**Korko alueen mukaan**</span><span class="sxs-lookup"><span data-stu-id="93dde-171">**Interest by range**</span></span>           | <span data-ttu-id="93dde-172">Päivää</span><span class="sxs-lookup"><span data-stu-id="93dde-172">Days</span></span>            |
| <span data-ttu-id="93dde-173">**Käytä korkolaskennan perusteena**</span><span class="sxs-lookup"><span data-stu-id="93dde-173">**Calculate interest based on**</span></span> | <span data-ttu-id="93dde-174">Summa</span><span class="sxs-lookup"><span data-stu-id="93dde-174">Amount</span></span>          |

<span data-ttu-id="93dde-175">Määrität alueen tiedot seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="93dde-175">You set up the range information as follows.</span></span>

| <span data-ttu-id="93dde-176">**Arvosta**</span><span class="sxs-lookup"><span data-stu-id="93dde-176">**From value**</span></span> | <span data-ttu-id="93dde-177">**Korkoarvo**</span><span class="sxs-lookup"><span data-stu-id="93dde-177">**Interest value**</span></span> |
|----------------|--------------------|
| <span data-ttu-id="93dde-178">0</span><span class="sxs-lookup"><span data-stu-id="93dde-178">0</span></span>              | <span data-ttu-id="93dde-179">10</span><span class="sxs-lookup"><span data-stu-id="93dde-179">10</span></span>                 |
| <span data-ttu-id="93dde-180">61</span><span class="sxs-lookup"><span data-stu-id="93dde-180">61</span></span>             | <span data-ttu-id="93dde-181">15</span><span class="sxs-lookup"><span data-stu-id="93dde-181">15</span></span>                 |
| <span data-ttu-id="93dde-182">91</span><span class="sxs-lookup"><span data-stu-id="93dde-182">91</span></span>             | <span data-ttu-id="93dde-183">20</span><span class="sxs-lookup"><span data-stu-id="93dde-183">20</span></span>                 |


## <a name="example-3-interest-by-range--months"></a><span data-ttu-id="93dde-184">Esimerkki 3: Korko alueen mukaan = kuukaudet</span><span class="sxs-lookup"><span data-stu-id="93dde-184">Example 3: Interest by range = Months</span></span>
----------------------------------------------------

<span data-ttu-id="93dde-185">Määrität korkokoodin, joka arvioi koron kerran jokaista kuukautta kohden, jonka laskun maksu on myöhässä tapahtuman eräpäivästä.</span><span class="sxs-lookup"><span data-stu-id="93dde-185">You set up an interest code that assesses interest one time for every month that the invoice payment exceeds the transaction due date.</span></span> <span data-ttu-id="93dde-186">Haluat laskennan perustuvan prosentuaaliseen korkoarvoon askeleittaisten kuukausivälien mukaan.</span><span class="sxs-lookup"><span data-stu-id="93dde-186">You want to base the calculation on a percentage interest value, according to stepped month intervals.</span></span> <span data-ttu-id="93dde-187">Koron arvo on 1,5 prosenttia kuukaudessa eräpäivän jälkeisen kolmen ensimmäisen kuukauden ajan, 2,0 prosenttia kuukaudessa toisen kolmen kuukauden jakson ajan ja 2,5 prosenttia kuukaudessa kuuden ensimmäisen kuukauden jälkeen.</span><span class="sxs-lookup"><span data-stu-id="93dde-187">The interest value will be 1.5 percent per month for the first three overdue months, 2.0 percent per month for the second three months, and 2.5 percent per month for each month beyond the first six months.</span></span> <span data-ttu-id="93dde-188">Määrität korkokoodin kenttien arvot seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="93dde-188">You set up the interest code field values as follows.</span></span>

| <span data-ttu-id="93dde-189">**Kentän nimi**</span><span class="sxs-lookup"><span data-stu-id="93dde-189">**Field name**</span></span>                  | <span data-ttu-id="93dde-190">**Kentän arvo**</span><span class="sxs-lookup"><span data-stu-id="93dde-190">**Field value**</span></span> |
|---------------------------------|-----------------|
| <span data-ttu-id="93dde-191">**Korkoryhmä**</span><span class="sxs-lookup"><span data-stu-id="93dde-191">**Interest code**</span></span>               | <span data-ttu-id="93dde-192">1M%ByMth</span><span class="sxs-lookup"><span data-stu-id="93dde-192">1M%ByMth</span></span>        |
| <span data-ttu-id="93dde-193">**Koronlaskentaväli**</span><span class="sxs-lookup"><span data-stu-id="93dde-193">**Calculate interest every**</span></span>    | <span data-ttu-id="93dde-194">1/kuukausi</span><span class="sxs-lookup"><span data-stu-id="93dde-194">1/Month</span></span>         |
| <span data-ttu-id="93dde-195">**Korko alueen mukaan**</span><span class="sxs-lookup"><span data-stu-id="93dde-195">**Interest by range**</span></span>           | <span data-ttu-id="93dde-196">Kuukautta</span><span class="sxs-lookup"><span data-stu-id="93dde-196">Months</span></span>          |
| <span data-ttu-id="93dde-197">**Käytä korkolaskennan perusteena**</span><span class="sxs-lookup"><span data-stu-id="93dde-197">**Calculate interest based on**</span></span> | <span data-ttu-id="93dde-198">Prosentti</span><span class="sxs-lookup"><span data-stu-id="93dde-198">Percentage</span></span>      |

<span data-ttu-id="93dde-199">Määrität alueen tiedot seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="93dde-199">You set up the range information as follows.</span></span>

| <span data-ttu-id="93dde-200">**Arvosta**</span><span class="sxs-lookup"><span data-stu-id="93dde-200">**From value**</span></span> | <span data-ttu-id="93dde-201">**Korkoarvo**</span><span class="sxs-lookup"><span data-stu-id="93dde-201">**Interest value**</span></span> |
|----------------|--------------------|
| <span data-ttu-id="93dde-202">0</span><span class="sxs-lookup"><span data-stu-id="93dde-202">0</span></span>              | <span data-ttu-id="93dde-203">1.5</span><span class="sxs-lookup"><span data-stu-id="93dde-203">1.5</span></span>                |
| <span data-ttu-id="93dde-204">4</span><span class="sxs-lookup"><span data-stu-id="93dde-204">4</span></span>              | <span data-ttu-id="93dde-205">2</span><span class="sxs-lookup"><span data-stu-id="93dde-205">2</span></span>                  |
| <span data-ttu-id="93dde-206">7</span><span class="sxs-lookup"><span data-stu-id="93dde-206">7</span></span>              | <span data-ttu-id="93dde-207">2,5</span><span class="sxs-lookup"><span data-stu-id="93dde-207">2.5</span></span>                |

## <a name="new-versions"></a><span data-ttu-id="93dde-208">Uudet versiot</span><span class="sxs-lookup"><span data-stu-id="93dde-208">New versions</span></span>
<span data-ttu-id="93dde-209">Korkokoodeilla on voimassaolopäivät.</span><span class="sxs-lookup"><span data-stu-id="93dde-209">Interest codes are date effective.</span></span> <span data-ttu-id="93dde-210">Jos haluat muokata korkoprosenttia, voit luoda **uuden version**, jonka voimassaolo alkaa tiettynä päivänä tulevaisuudessa.</span><span class="sxs-lookup"><span data-stu-id="93dde-210">If you want to modify the interest rate, you can create a **new version** that is effective as of a future date.</span></span>

<span data-ttu-id="93dde-211">Voit tarkastella eri versioita valitsemalla **Alkupäivämäärä**-valikkovaihtoehdolla katkaisupäivämäärän.</span><span class="sxs-lookup"><span data-stu-id="93dde-211">To view different versions, you can use the **As of Date** menu choice to select the cutoff date.</span></span> <span data-ttu-id="93dde-212">Jos haluat tarkastella kaikkia sivun korkoprosentteja, valitse **Näytä kaikki tietueet**.</span><span class="sxs-lookup"><span data-stu-id="93dde-212">You can also select the **Display all records** to view all interest codes in the page.</span></span>



