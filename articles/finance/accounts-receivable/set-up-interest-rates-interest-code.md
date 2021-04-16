---
title: Korkoryhmän korkoprosenttien määrittäminen
description: Korkokoodit sisältävät asetukset, joilla määritetään, milloin korkoa veloitetaan ja miten se lasketaan erääntyneillä tileillä.
author: ShivamPandey-msft
ms.date: 02/17/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: Interest
audience: Application User
ms.reviewer: roschlom
ms.custom: 59402
ms.assetid: 3b945333-1eaf-4658-ab5a-1a7791a7eb40
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 62868c30d3ff60e51d99c71b743ab0bbb3c87451
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/01/2021
ms.locfileid: "5835193"
---
# <a name="set-up-interest-rates-for-an-interest-code"></a><span data-ttu-id="5bfd5-103">Korkoryhmän korkoprosenttien määrittäminen</span><span class="sxs-lookup"><span data-stu-id="5bfd5-103">Set up interest rates for an interest code</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5bfd5-104">Korkokoodit sisältävät asetukset, joilla määritetään, milloin korkoa veloitetaan ja miten se lasketaan erääntyneillä tileillä.</span><span class="sxs-lookup"><span data-stu-id="5bfd5-104">Interest codes contain settings that determine when interest is charged and how it is calculated on overdue accounts.</span></span>

<span data-ttu-id="5bfd5-105">Voit määrittää yksittäisen korkokoodin ja käyttää sitä useassa asiakaskirjausprofiilissa, laskutuskoodeissa tai tietyillä laskuriviellä.</span><span class="sxs-lookup"><span data-stu-id="5bfd5-105">You can set up a single interest code and apply it to multiple customer posting profiles, billing codes, or to specific invoice lines.</span></span> <span data-ttu-id="5bfd5-106">Kun korkokoodin tietoja muutetaan, kaikki koodia käyttävät toiminnot käyttävät automaattisesti muutoksia uusissa tapahtumissa.</span><span class="sxs-lookup"><span data-stu-id="5bfd5-106">When the interest code details are changed, all features that use the code will automatically implement the changes on new transactions.</span></span> <span data-ttu-id="5bfd5-107">Kullekin korkokoodille voi määrittää kahdentyyppisiä tuloja:</span><span class="sxs-lookup"><span data-stu-id="5bfd5-107">For each interest code, you can set up two types of rates:</span></span>
-   <span data-ttu-id="5bfd5-108">Tulot korkoansioista – Nämä ovat tuloja, jotka on ansaittu veloittamalla korkoa laskuista tai korkolaskuista.</span><span class="sxs-lookup"><span data-stu-id="5bfd5-108">Rates for interest earnings − These represent revenue that is earned by charging interest on invoices or interest notes.</span></span>
-   <span data-ttu-id="5bfd5-109">TUlost kokorkomaksuista – Nämä ovat kustannuksia, jotka maksetaan korkolaskujen koroista.</span><span class="sxs-lookup"><span data-stu-id="5bfd5-109">Rates for interest payments − These represent a cost that is paid for interest on credit notes.</span></span>

<span data-ttu-id="5bfd5-110">Molemmat korkotyypit voivat olla olemassa samanaikaisesti ja samassa korkokoodissa.</span><span class="sxs-lookup"><span data-stu-id="5bfd5-110">Both of these rate types can exist at the same time and in the same interest code.</span></span> <span data-ttu-id="5bfd5-111">Korot voivat perustua kolmeen laskentatyyppin:</span><span class="sxs-lookup"><span data-stu-id="5bfd5-111">Interest rates can be based on three calculation types:</span></span>
-   <span data-ttu-id="5bfd5-112">Korko prosenttiosuuden mukaan.</span><span class="sxs-lookup"><span data-stu-id="5bfd5-112">Interest by percentage.</span></span>
-   <span data-ttu-id="5bfd5-113">Korko summan mukaan.</span><span class="sxs-lookup"><span data-stu-id="5bfd5-113">Interest by amount.</span></span>
-   <span data-ttu-id="5bfd5-114">Korko alueen mukaan, joka tuottaa yhden prosenttiosuuden tai summan.</span><span class="sxs-lookup"><span data-stu-id="5bfd5-114">Interest by range, which results in a single percentage or amount.</span></span>

<span data-ttu-id="5bfd5-115">Kun korkokoodia käytetään koron laskennassa, luodaan erillinen korkolasku kutakin korkotasoa varten, joka on voimassa sinä aikana, jonka maksu on ylittänyt tapahtuman eräpäivän.</span><span class="sxs-lookup"><span data-stu-id="5bfd5-115">When an interest code is used to calculate interest, a separate interest note is created for each interest rate that is in effect during the time that the payment has exceeded the transaction due date.</span></span> <span data-ttu-id="5bfd5-116">Voit määrittää **Korkoryhmä**-sivun **Ansiot**-välilehdessä korkotasot koroille, jotka ansaitaan veloittamalla korkoa.</span><span class="sxs-lookup"><span data-stu-id="5bfd5-116">You use the **Earnings** tab on the **Interest code** page to set up interest rates for interest that you earn by charging interest.</span></span> <span data-ttu-id="5bfd5-117">Määritä korkotasot itse maksamillesi koroille **Maksut**-välilehdessä.</span><span class="sxs-lookup"><span data-stu-id="5bfd5-117">Use the **Payments** tab to set up interest rates for interest that you pay.</span></span>

## <a name="interest-rates-based-on-a-percentage"></a><span data-ttu-id="5bfd5-118">Prosenttiosuuksiin perustuvat korkotasot</span><span class="sxs-lookup"><span data-stu-id="5bfd5-118">Interest rates based on a percentage</span></span>
<span data-ttu-id="5bfd5-119">Voit määrittää korkotasot, jotka laskevat määritetyn prosenttiosuuden.</span><span class="sxs-lookup"><span data-stu-id="5bfd5-119">You can set up interest rates that calculate a specified percentage.</span></span>

- <span data-ttu-id="5bfd5-120">Korkosumman koskee kaikkia valuuttoja.</span><span class="sxs-lookup"><span data-stu-id="5bfd5-120">Interest amount applies to all currencies.</span></span>
- <span data-ttu-id="5bfd5-121">Korkosumman rajojen antaminen on valinnaista.</span><span class="sxs-lookup"><span data-stu-id="5bfd5-121">Optional interest amount limits can be entered.</span></span>
- <span data-ttu-id="5bfd5-122">**Prosentti** valitaan **Korkokoodien määrittäminen** -sivun **Käytä korkolaskennan perusteena** -kentässä.</span><span class="sxs-lookup"><span data-stu-id="5bfd5-122">**Percentage** is selected in the **Calculate interest based on** field on the **Set up Interest codes** page.</span></span>

<span data-ttu-id="5bfd5-123">Jos esimerkiksi haluat määrittää korkokoodin, joka määrää 5 prosentin koron jokaista kahta kuukautta kohti, jonka laskun maksaminen ylittää tapahtuman eräpäivän, anna arvo 2 **Koronlaskentaväli**-kenttään ja valitse **Kuukausi**.</span><span class="sxs-lookup"><span data-stu-id="5bfd5-123">For example, to set up an interest code that assesses 5 percent interest for every two months that the invoice payment exceeds the transaction due date, you would enter 2 in the **Calculate interest every** field and select **Month**.</span></span>

> [!NOTE] 
> <span data-ttu-id="5bfd5-124">Uusi korkolaskun laskennassa käytettävä algoritmi lisätään käyttämällä ominaisuuksien hallintaa.</span><span class="sxs-lookup"><span data-stu-id="5bfd5-124">The new algorithm for interest note calculation is added using Feature management.</span></span> <span data-ttu-id="5bfd5-125">Jos haluat käyttää tätä algoritmia, ota käyttöön ominaisuus **(GBL) Salli päiväkohtaisen koron laskenta jakamalla vuositaisen prosentin luvulla 365**.</span><span class="sxs-lookup"><span data-stu-id="5bfd5-125">To use this algorithm, enable the **(GBL) Allow to calculate interest per day as yearly percent divided by 365** feature.</span></span> <span data-ttu-id="5bfd5-126">Lisätietoja uuden ominaisuuden käyttöönotosta on kohdassa [ominaisuuksien hallinnan yleiskuvaus](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).</span><span class="sxs-lookup"><span data-stu-id="5bfd5-126">For information about how to enable the feature, see [Feature management overview](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).</span></span>
> 
> <span data-ttu-id="5bfd5-127">Korkolaskun summan laskentakaava on:</span><span class="sxs-lookup"><span data-stu-id="5bfd5-127">The formula for the calculation for the interest note amount is:</span></span> 
>  
> <span data-ttu-id="5bfd5-128">Korkolaskun summa = Velkasumma \* Vuosittainen korkoprosentti / 365 \* myöhässä olevien päivien määrä</span><span class="sxs-lookup"><span data-stu-id="5bfd5-128">Interest note amount = Amount owed \* Yearly interest % / 365 \* Number of days late</span></span>
>  
> <span data-ttu-id="5bfd5-129">Ominaisuus on saatavilla versiossa 10.0.18 ja sitä uudemmissa versioissa.</span><span class="sxs-lookup"><span data-stu-id="5bfd5-129">This feature is available in version 10.0.18 or later.</span></span>    
 
## <a name="interest-rates-based-on-amounts"></a><span data-ttu-id="5bfd5-130">Summin perustuvat korkotasot</span><span class="sxs-lookup"><span data-stu-id="5bfd5-130">Interest rates based on amounts</span></span>
<span data-ttu-id="5bfd5-131">Voit määrittää korkotasot, jotka laskevat määritetyn summan valuuttaa kohden.</span><span class="sxs-lookup"><span data-stu-id="5bfd5-131">You can set up interest rates that calculate a specified amount per currency.</span></span>
- <span data-ttu-id="5bfd5-132">Korkosumma on määritettävä jokaiselle korkokoodin valuutalle.</span><span class="sxs-lookup"><span data-stu-id="5bfd5-132">An interest amount is specified for each currency in the interest code.</span></span>
- <span data-ttu-id="5bfd5-133">Korkosumman rajojen antaminen on valinnaista.</span><span class="sxs-lookup"><span data-stu-id="5bfd5-133">Optional interest amount limits can be entered.</span></span>
- <span data-ttu-id="5bfd5-134">**Summa** valitaan **Korkokoodien määrittäminen** -sivun **Käytä korkolaskennan perusteena** -kentässä.</span><span class="sxs-lookup"><span data-stu-id="5bfd5-134">**Amount** is selected in the **Calculate interest based on** field on the **Set up Interest codes** page.</span></span>

<span data-ttu-id="5bfd5-135">Jos esimerkiksi haluat määrittää korkokoodin, joka määrää 25,00 valuuttayksikön koron jokaista 20 päivää kohti, jonka laskun maksaminen ylittää tapahtuman eräpäivän, anna arvo 20 **Koronlaskentaväli**-kentässä ja valitse **Päivä**.</span><span class="sxs-lookup"><span data-stu-id="5bfd5-135">For example, to set up an interest code that assesses interest of 25.00 for every 20 days that the invoice payment exceeds the transaction due date, you would enter 20 in the **Calculate interest every** field and select **Day**.</span></span>

## <a name="interest-rates-based-on-ranges"></a><span data-ttu-id="5bfd5-136">Alueisiin perustuvat korkotasot</span><span class="sxs-lookup"><span data-stu-id="5bfd5-136">Interest rates based on ranges</span></span>
<span data-ttu-id="5bfd5-137">Voit määrittää korkotasot, jotka vaihtelevat myöhässä olevan summan, summan myöhässä olevien päivien määrän tai summan myöhässä olevien kuukausien määrän mukaan.</span><span class="sxs-lookup"><span data-stu-id="5bfd5-137">You can set up interest rates that vary depending on the overdue amount, the number of days that the amount is late, or the number of months that the amount is late.</span></span>
-   <span data-ttu-id="5bfd5-138">Voit määrittää kunkin valuutan korkoasetukset **Ansiot valuutan mukaan** -välilehdessä.</span><span class="sxs-lookup"><span data-stu-id="5bfd5-138">You can use the **Earnings by Currency** tab to define specific interest settings for each currency.</span></span> <span data-ttu-id="5bfd5-139">Myös alue määritetään tässä välilehdessä.</span><span class="sxs-lookup"><span data-stu-id="5bfd5-139">This is also where you will define the range.</span></span>
-   <span data-ttu-id="5bfd5-140">Lisää **Alueet**-painikkeella rivit, jotka ilmaisevat määritettäviä alueita.</span><span class="sxs-lookup"><span data-stu-id="5bfd5-140">Use the **Ranges** button to add lines that represent the ranges that you want to set up.</span></span> <span data-ttu-id="5bfd5-141">**Mistä**-arvo ilmaisee alueen alkamiskohdan ja **Korkoarvo**-luku ilmaisee joko prosentin tai summan sen mukaan, mitä **Korkokoodien määrittäminen** -sivun **Käytä korkolaskennan perusteena** -kentässä on valittu.</span><span class="sxs-lookup"><span data-stu-id="5bfd5-141">The **From** value represents the beginning of the range and the **Interest value** number represents either a percentage or an amount, depending on the selection in the **Calculate interest based on** field on the **Set up Interest codes** page.</span></span>

## <a name="example-1-interest-by-range--amount"></a><span data-ttu-id="5bfd5-142">Esimerkki 1: Korko alueen mukaan = summa</span><span class="sxs-lookup"><span data-stu-id="5bfd5-142">Example 1: Interest by range = Amount</span></span>
<span data-ttu-id="5bfd5-143">Määrität korkokoodin, joka arvioi koron kerran jokaista kolmea kuukautta kohden, jonka laskun maksu on myöhässä tapahtuman eräpäivästä.</span><span class="sxs-lookup"><span data-stu-id="5bfd5-143">You set up an interest code that assesses interest one time for every three months that the invoice payment exceeds the transaction due date.</span></span> <span data-ttu-id="5bfd5-144">Haluat laskennan perustuvan prosentuaaliseen korkoarvoon askeleittaisten summavälien mukaan.</span><span class="sxs-lookup"><span data-stu-id="5bfd5-144">You want to base the calculation on a percentage interest value, according to stepped amount intervals.</span></span> <span data-ttu-id="5bfd5-145">Koron arvo on 1 prosentti laskun summasta summaan 1 000,00 saakka, 2 prosenttia summasta välillä 1 001,00–5 000,00 ja 3 prosenttia yli 5 000,00:n summista.</span><span class="sxs-lookup"><span data-stu-id="5bfd5-145">The interest value will be 1 percent for invoice amounts up to 1,000.00, 2 percent for amounts from 1,001.00 to 5,000.00, and 3 percent for amounts larger than 5,000.00.</span></span> <span data-ttu-id="5bfd5-146">Määrität korkokoodin kenttien arvot seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="5bfd5-146">You set up the interest code field values as follows.</span></span>

| <span data-ttu-id="5bfd5-147">**Kentän nimi**</span><span class="sxs-lookup"><span data-stu-id="5bfd5-147">**Field name**</span></span>                  | <span data-ttu-id="5bfd5-148">**Kentän arvo**</span><span class="sxs-lookup"><span data-stu-id="5bfd5-148">**Field value**</span></span> |
|---------------------------------|-----------------|
| <span data-ttu-id="5bfd5-149">**Korkoryhmä**</span><span class="sxs-lookup"><span data-stu-id="5bfd5-149">**Interest code**</span></span>               | <span data-ttu-id="5bfd5-150">3M%ByAmt</span><span class="sxs-lookup"><span data-stu-id="5bfd5-150">3M%ByAmt</span></span>        |
| <span data-ttu-id="5bfd5-151">**Koronlaskentaväli**</span><span class="sxs-lookup"><span data-stu-id="5bfd5-151">**Calculate interest every**</span></span>    | <span data-ttu-id="5bfd5-152">3/kuukausi</span><span class="sxs-lookup"><span data-stu-id="5bfd5-152">3/Month</span></span>         |
| <span data-ttu-id="5bfd5-153">**Korko alueen mukaan**</span><span class="sxs-lookup"><span data-stu-id="5bfd5-153">**Interest by range**</span></span>           | <span data-ttu-id="5bfd5-154">Summa</span><span class="sxs-lookup"><span data-stu-id="5bfd5-154">Amount</span></span>          |
| <span data-ttu-id="5bfd5-155">**Käytä korkolaskennan perusteena**</span><span class="sxs-lookup"><span data-stu-id="5bfd5-155">**Calculate interest based on**</span></span> | <span data-ttu-id="5bfd5-156">Prosentti</span><span class="sxs-lookup"><span data-stu-id="5bfd5-156">Percentage</span></span>      |

<span data-ttu-id="5bfd5-157">Määrität alueen tiedot seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="5bfd5-157">You set up the range information as follows.</span></span>

| <span data-ttu-id="5bfd5-158">**Arvosta**</span><span class="sxs-lookup"><span data-stu-id="5bfd5-158">**From value**</span></span> | <span data-ttu-id="5bfd5-159">**Korkoarvo**</span><span class="sxs-lookup"><span data-stu-id="5bfd5-159">**Interest value**</span></span> |
|----------------|--------------------|
| <span data-ttu-id="5bfd5-160">0</span><span class="sxs-lookup"><span data-stu-id="5bfd5-160">0</span></span>              | <span data-ttu-id="5bfd5-161">1</span><span class="sxs-lookup"><span data-stu-id="5bfd5-161">1</span></span>                  |
| <span data-ttu-id="5bfd5-162">1,001</span><span class="sxs-lookup"><span data-stu-id="5bfd5-162">1,001</span></span>          | <span data-ttu-id="5bfd5-163">2</span><span class="sxs-lookup"><span data-stu-id="5bfd5-163">2</span></span>                  |
| <span data-ttu-id="5bfd5-164">5,001</span><span class="sxs-lookup"><span data-stu-id="5bfd5-164">5,001</span></span>          | <span data-ttu-id="5bfd5-165">3</span><span class="sxs-lookup"><span data-stu-id="5bfd5-165">3</span></span>                  |


## <a name="example-2-interest-by-range--days"></a><span data-ttu-id="5bfd5-166">Esimerkki 2: Korko alueen mukaan = päivät</span><span class="sxs-lookup"><span data-stu-id="5bfd5-166">Example 2: Interest by range = Days</span></span>
--------------------------------------------------

<span data-ttu-id="5bfd5-167">Määrität korkokoodin, joka arvioi koron kerran jokaista 15 päivää kohden, jonka laskun maksu on myöhässä tapahtuman eräpäivästä.</span><span class="sxs-lookup"><span data-stu-id="5bfd5-167">You set up an interest code that assesses interest one time for every 15 days that the invoice payment exceeds the transaction due date.</span></span> <span data-ttu-id="5bfd5-168">Haluat laskennan perustuvan summan korkoarvoon askeleittaisten päivävälien mukaan.</span><span class="sxs-lookup"><span data-stu-id="5bfd5-168">You want to base the calculation on an amount interest value, according to stepped day intervals.</span></span> <span data-ttu-id="5bfd5-169">Koron arvo on 10,00 kutakin 15 päivää kohden 60 ensimmäisen päivän ajan, 15,00 kutakin 15 päivää kohden päivien 61–90 ajan ja 20,00 kutakin 15 päivää kohden päivän 91 ja sen jälkeisten päivien ajan.</span><span class="sxs-lookup"><span data-stu-id="5bfd5-169">The interest value will be 10.00 per 15 days during the first 60 days, 15.00 per 15 days during days 61 to 90, and 20.00 per 15 days from day 91 and after.</span></span> <span data-ttu-id="5bfd5-170">Määrität korkokoodin kenttien arvot seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="5bfd5-170">You set up the interest code field values as follows.</span></span>

| <span data-ttu-id="5bfd5-171">**Kentän nimi**</span><span class="sxs-lookup"><span data-stu-id="5bfd5-171">**Field name**</span></span>                  | <span data-ttu-id="5bfd5-172">**Kentän arvo**</span><span class="sxs-lookup"><span data-stu-id="5bfd5-172">**Field value**</span></span> |
|---------------------------------|-----------------|
| <span data-ttu-id="5bfd5-173">**Korkoryhmä**</span><span class="sxs-lookup"><span data-stu-id="5bfd5-173">**Interest code**</span></span>               | <span data-ttu-id="5bfd5-174">15DAmtXDay</span><span class="sxs-lookup"><span data-stu-id="5bfd5-174">15DAmtXDay</span></span>      |
| <span data-ttu-id="5bfd5-175">**Koronlaskentaväli**</span><span class="sxs-lookup"><span data-stu-id="5bfd5-175">**Calculate interest every**</span></span>    | <span data-ttu-id="5bfd5-176">15/päivä</span><span class="sxs-lookup"><span data-stu-id="5bfd5-176">15/Day</span></span>          |
| <span data-ttu-id="5bfd5-177">**Korko alueen mukaan**</span><span class="sxs-lookup"><span data-stu-id="5bfd5-177">**Interest by range**</span></span>           | <span data-ttu-id="5bfd5-178">Päivää</span><span class="sxs-lookup"><span data-stu-id="5bfd5-178">Days</span></span>            |
| <span data-ttu-id="5bfd5-179">**Käytä korkolaskennan perusteena**</span><span class="sxs-lookup"><span data-stu-id="5bfd5-179">**Calculate interest based on**</span></span> | <span data-ttu-id="5bfd5-180">Summa</span><span class="sxs-lookup"><span data-stu-id="5bfd5-180">Amount</span></span>          |

<span data-ttu-id="5bfd5-181">Määrität alueen tiedot seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="5bfd5-181">You set up the range information as follows.</span></span>

| <span data-ttu-id="5bfd5-182">**Arvosta**</span><span class="sxs-lookup"><span data-stu-id="5bfd5-182">**From value**</span></span> | <span data-ttu-id="5bfd5-183">**Korkoarvo**</span><span class="sxs-lookup"><span data-stu-id="5bfd5-183">**Interest value**</span></span> |
|----------------|--------------------|
| <span data-ttu-id="5bfd5-184">0</span><span class="sxs-lookup"><span data-stu-id="5bfd5-184">0</span></span>              | <span data-ttu-id="5bfd5-185">10</span><span class="sxs-lookup"><span data-stu-id="5bfd5-185">10</span></span>                 |
| <span data-ttu-id="5bfd5-186">61</span><span class="sxs-lookup"><span data-stu-id="5bfd5-186">61</span></span>             | <span data-ttu-id="5bfd5-187">15</span><span class="sxs-lookup"><span data-stu-id="5bfd5-187">15</span></span>                 |
| <span data-ttu-id="5bfd5-188">91</span><span class="sxs-lookup"><span data-stu-id="5bfd5-188">91</span></span>             | <span data-ttu-id="5bfd5-189">20</span><span class="sxs-lookup"><span data-stu-id="5bfd5-189">20</span></span>                 |


## <a name="example-3-interest-by-range--months"></a><span data-ttu-id="5bfd5-190">Esimerkki 3: Korko alueen mukaan = kuukaudet</span><span class="sxs-lookup"><span data-stu-id="5bfd5-190">Example 3: Interest by range = Months</span></span>
----------------------------------------------------

<span data-ttu-id="5bfd5-191">Määrität korkokoodin, joka arvioi koron kerran jokaista kuukautta kohden, jonka laskun maksu on myöhässä tapahtuman eräpäivästä.</span><span class="sxs-lookup"><span data-stu-id="5bfd5-191">You set up an interest code that assesses interest one time for every month that the invoice payment exceeds the transaction due date.</span></span> <span data-ttu-id="5bfd5-192">Haluat laskennan perustuvan prosentuaaliseen korkoarvoon askeleittaisten kuukausivälien mukaan.</span><span class="sxs-lookup"><span data-stu-id="5bfd5-192">You want to base the calculation on a percentage interest value, according to stepped month intervals.</span></span> <span data-ttu-id="5bfd5-193">Koron arvo on 1,5 prosenttia kuukaudessa eräpäivän jälkeisen kolmen ensimmäisen kuukauden ajan, 2,0 prosenttia kuukaudessa toisen kolmen kuukauden jakson ajan ja 2,5 prosenttia kuukaudessa kuuden ensimmäisen kuukauden jälkeen.</span><span class="sxs-lookup"><span data-stu-id="5bfd5-193">The interest value will be 1.5 percent per month for the first three overdue months, 2.0 percent per month for the second three months, and 2.5 percent per month for each month beyond the first six months.</span></span> <span data-ttu-id="5bfd5-194">Määrität korkokoodin kenttien arvot seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="5bfd5-194">You set up the interest code field values as follows.</span></span>

| <span data-ttu-id="5bfd5-195">**Kentän nimi**</span><span class="sxs-lookup"><span data-stu-id="5bfd5-195">**Field name**</span></span>                  | <span data-ttu-id="5bfd5-196">**Kentän arvo**</span><span class="sxs-lookup"><span data-stu-id="5bfd5-196">**Field value**</span></span> |
|---------------------------------|-----------------|
| <span data-ttu-id="5bfd5-197">**Korkoryhmä**</span><span class="sxs-lookup"><span data-stu-id="5bfd5-197">**Interest code**</span></span>               | <span data-ttu-id="5bfd5-198">1M%ByMth</span><span class="sxs-lookup"><span data-stu-id="5bfd5-198">1M%ByMth</span></span>        |
| <span data-ttu-id="5bfd5-199">**Koronlaskentaväli**</span><span class="sxs-lookup"><span data-stu-id="5bfd5-199">**Calculate interest every**</span></span>    | <span data-ttu-id="5bfd5-200">1/kuukausi</span><span class="sxs-lookup"><span data-stu-id="5bfd5-200">1/Month</span></span>         |
| <span data-ttu-id="5bfd5-201">**Korko alueen mukaan**</span><span class="sxs-lookup"><span data-stu-id="5bfd5-201">**Interest by range**</span></span>           | <span data-ttu-id="5bfd5-202">Kuukautta</span><span class="sxs-lookup"><span data-stu-id="5bfd5-202">Months</span></span>          |
| <span data-ttu-id="5bfd5-203">**Käytä korkolaskennan perusteena**</span><span class="sxs-lookup"><span data-stu-id="5bfd5-203">**Calculate interest based on**</span></span> | <span data-ttu-id="5bfd5-204">Prosentti</span><span class="sxs-lookup"><span data-stu-id="5bfd5-204">Percentage</span></span>      |

<span data-ttu-id="5bfd5-205">Määrität alueen tiedot seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="5bfd5-205">You set up the range information as follows.</span></span>

| <span data-ttu-id="5bfd5-206">**Arvosta**</span><span class="sxs-lookup"><span data-stu-id="5bfd5-206">**From value**</span></span> | <span data-ttu-id="5bfd5-207">**Korkoarvo**</span><span class="sxs-lookup"><span data-stu-id="5bfd5-207">**Interest value**</span></span> |
|----------------|--------------------|
| <span data-ttu-id="5bfd5-208">0</span><span class="sxs-lookup"><span data-stu-id="5bfd5-208">0</span></span>              | <span data-ttu-id="5bfd5-209">1.5</span><span class="sxs-lookup"><span data-stu-id="5bfd5-209">1.5</span></span>                |
| <span data-ttu-id="5bfd5-210">4</span><span class="sxs-lookup"><span data-stu-id="5bfd5-210">4</span></span>              | <span data-ttu-id="5bfd5-211">2</span><span class="sxs-lookup"><span data-stu-id="5bfd5-211">2</span></span>                  |
| <span data-ttu-id="5bfd5-212">7</span><span class="sxs-lookup"><span data-stu-id="5bfd5-212">7</span></span>              | <span data-ttu-id="5bfd5-213">2,5</span><span class="sxs-lookup"><span data-stu-id="5bfd5-213">2.5</span></span>                |

## <a name="new-versions"></a><span data-ttu-id="5bfd5-214">Uudet versiot</span><span class="sxs-lookup"><span data-stu-id="5bfd5-214">New versions</span></span>
<span data-ttu-id="5bfd5-215">Korkokoodeilla on voimassaolopäivät.</span><span class="sxs-lookup"><span data-stu-id="5bfd5-215">Interest codes are date effective.</span></span> <span data-ttu-id="5bfd5-216">Jos haluat muokata korkoprosenttia, voit luoda **uuden version**, jonka voimassaolo alkaa tiettynä päivänä tulevaisuudessa.</span><span class="sxs-lookup"><span data-stu-id="5bfd5-216">If you want to modify the interest rate, you can create a **new version** that is effective as of a future date.</span></span>

<span data-ttu-id="5bfd5-217">Voit tarkastella eri versioita valitsemalla **Alkupäivämäärä**-valikkovaihtoehdolla katkaisupäivämäärän.</span><span class="sxs-lookup"><span data-stu-id="5bfd5-217">To view different versions, you can use the **As of Date** menu choice to select the cutoff date.</span></span> <span data-ttu-id="5bfd5-218">Jos haluat tarkastella kaikkia sivun korkoprosentteja, valitse **Näytä kaikki tietueet**.</span><span class="sxs-lookup"><span data-stu-id="5bfd5-218">You can also select the **Display all records** to view all interest codes in the page.</span></span>





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
