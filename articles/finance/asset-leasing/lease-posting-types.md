---
title: Vuokrauksen kirjaustyypit
description: Tässä ohjeaiheessa kuvataan kirjaustyypit, joita käytetään resurssien vuokratapahtumissa.
author: moaamer
manager: Ann Beebe
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: b79b02f7e241783d19a315ccff5bb6874a238c38
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/15/2021
ms.locfileid: "4995415"
---
# <a name="lease-posting-types"></a><span data-ttu-id="372f9-103">Vuokrauksen kirjaustyypit</span><span class="sxs-lookup"><span data-stu-id="372f9-103">Lease posting types</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="372f9-104">Tässä ohjeaiheessa kuvataan kirjaustyypit, joita käytetään resurssien vuokratapahtumissa.</span><span class="sxs-lookup"><span data-stu-id="372f9-104">This topic describes the posting types that are used for asset leasing transactions.</span></span>

## <a name="lease-asset"></a><span data-ttu-id="372f9-105">Vuokraresurssi</span><span class="sxs-lookup"><span data-stu-id="372f9-105">Lease asset</span></span>

<span data-ttu-id="372f9-106">Tili liittyy käyttöoikeusomaisuuserään.</span><span class="sxs-lookup"><span data-stu-id="372f9-106">The account is associated with the right-of-use (ROU) asset.</span></span> <span data-ttu-id="372f9-107">Tätä tiliä veloitetaan, kun vuokra kirjataan alun perin uusien vuokrauksen tilinpäätösstandardien ASC 842:n (Accounting Standards Codification Topic 842) ja IFRS 16:n (International Financial Reporting Standard 16) mukaan.</span><span class="sxs-lookup"><span data-stu-id="372f9-107">This account is debited when a lease is initially recognized under the new lease accounting standards, Accounting Standards Codification Topic 842 (ASC 842) and International Financial Reporting Standard 16 (IFRS 16).</span></span> <span data-ttu-id="372f9-108">Jos kyseessä on muokattu vuokra, tätä tiliä voidaan veloittaa tai hyvittää sen mukaan, lisääkö muokkaus vuokravelkaa vai vähentääkö se sitä.</span><span class="sxs-lookup"><span data-stu-id="372f9-108">For a modified lease, this account might be either debited or credited, depending on whether the modification increases or decreases the lease liability.</span></span>

<span data-ttu-id="372f9-109">**Esimerkki kirjauskansiovienneistä:** Alkuperäinen kirjaus</span><span class="sxs-lookup"><span data-stu-id="372f9-109">**Example journal entries:** Initial recognition</span></span><br>
<span data-ttu-id="372f9-110">**Veloitus:** Vuokrasopimuksen resurssi XXX</span><span class="sxs-lookup"><span data-stu-id="372f9-110">**Debit:** Lease asset XXX</span></span><br>
<span data-ttu-id="372f9-111">**Hyvitys:** Vuokrasopimusvelka XXX</span><span class="sxs-lookup"><span data-stu-id="372f9-111">**Credit:** Lease liability XXX</span></span>

## <a name="lease-liability"></a><span data-ttu-id="372f9-112">Vuokrasopimusvelka</span><span class="sxs-lookup"><span data-stu-id="372f9-112">Lease liability</span></span>

<span data-ttu-id="372f9-113">Tili liittyy vuokrasopimusvelkaan, joka toteutuu kun maksut diskontataan uusien IFRS 16- ja ASC 842 -standardien mukaan.</span><span class="sxs-lookup"><span data-stu-id="372f9-113">The account is associated with the lease liability that occurs when payments are discounted under the new IFRS 16 and ASC 842 standards.</span></span> <span data-ttu-id="372f9-114">Tätä tiliä hyvitetään, kun vuokra kirjataan alun perin uusien standardien mukaan.</span><span class="sxs-lookup"><span data-stu-id="372f9-114">This account is credited when a lease is initially recognized under the new standards.</span></span> <span data-ttu-id="372f9-115">Vuokrat veloitetaan ja korkokertymät hyvitetään.</span><span class="sxs-lookup"><span data-stu-id="372f9-115">It's debited for lease payments and credited for interest accruals.</span></span>

<span data-ttu-id="372f9-116">**Esimerkki kirjauskansiovienneistä:** Alkuperäinen kirjaus</span><span class="sxs-lookup"><span data-stu-id="372f9-116">**Example journal entries:** Initial recognition</span></span><br>
<span data-ttu-id="372f9-117">**Veloitus:** Vuokrasopimuksen resurssi XXX</span><span class="sxs-lookup"><span data-stu-id="372f9-117">**Debit:** Lease asset XXX</span></span><br>
<span data-ttu-id="372f9-118">**Hyvitys:** Vuokrasopimusvelka XXX</span><span class="sxs-lookup"><span data-stu-id="372f9-118">**Credit:** Lease liability XXX</span></span>

<span data-ttu-id="372f9-119">**Esimerkki kirjauskansiovienneistä:** Korkokertymä</span><span class="sxs-lookup"><span data-stu-id="372f9-119">**Example journal entries:** Interest accrual</span></span><br>
<span data-ttu-id="372f9-120">**Veloitus:** Korkokustannus XXX</span><span class="sxs-lookup"><span data-stu-id="372f9-120">**Debit:** Interest expense XXX</span></span><br>
<span data-ttu-id="372f9-121">**Hyvitys:** Vuokrasopimusvelka XXX</span><span class="sxs-lookup"><span data-stu-id="372f9-121">**Credit:** Lease liability XXX</span></span>

<span data-ttu-id="372f9-122">**Esimerkki kirjauskansiovienneistä:** Vuokra</span><span class="sxs-lookup"><span data-stu-id="372f9-122">**Example journal entries:** Lease payment</span></span><br>
<span data-ttu-id="372f9-123">**Veloitus:** Vuokrasopimusvelka XXX</span><span class="sxs-lookup"><span data-stu-id="372f9-123">**Debit:** Lease liability XXX</span></span><br>
<span data-ttu-id="372f9-124">**Hyvitys:** Toimittajan maksettava / maksu XXX</span><span class="sxs-lookup"><span data-stu-id="372f9-124">**Credit:** Vendor payable/lease payment XXX</span></span>

## <a name="short-term-lease-liability"></a><span data-ttu-id="372f9-125">Lyhytaikainen vuokravelka</span><span class="sxs-lookup"><span data-stu-id="372f9-125">Short-term lease liability</span></span>

<span data-ttu-id="372f9-126">Tili liittyy lyhytaikaiseen vuokrasopimusvelkaan, kun lyhytaikaisen vuokrasopimusvelan uudelleenluokittelun kirjauskansiovienti kirjataan.</span><span class="sxs-lookup"><span data-stu-id="372f9-126">The account is associated with the short-term lease liability when the short-term lease liability reclass journal entry is posted.</span></span> <span data-ttu-id="372f9-127">Tälle tilille hyvitetään lyhytaikainen velka kuoletusaikataulusta kuukauden viimeisenä päivänä.</span><span class="sxs-lookup"><span data-stu-id="372f9-127">This account is credited for the short-term liability from the amortization schedule on the last day of the month.</span></span> <span data-ttu-id="372f9-128">Sama summa veloitetaan kuitenkin seuraavan kuukauden ensimmäisenä päivänä.</span><span class="sxs-lookup"><span data-stu-id="372f9-128">However, the same amount is debited on the first day of the next month.</span></span>

<span data-ttu-id="372f9-129">**Esimerkki kirjauskansiovienneistä:** Lyhytaikaisen vuokrasopimusvelan uudelleenluokittelu</span><span class="sxs-lookup"><span data-stu-id="372f9-129">**Example journal entries:** Short-term lease liability reclass</span></span><br>
<span data-ttu-id="372f9-130">**Veloitus:** Vuokrasopimusvelka XXX</span><span class="sxs-lookup"><span data-stu-id="372f9-130">**Debit:** Lease liability XXX</span></span><br>
<span data-ttu-id="372f9-131">**Hyvitys:** Lyhytaikainen vuokrasopimusvelka XXX</span><span class="sxs-lookup"><span data-stu-id="372f9-131">**Credit:** Short-term lease liability XXX</span></span><br>
<span data-ttu-id="372f9-132">**Veloitus:** Lyhytaikainen vuokrasopimusvelka XXX</span><span class="sxs-lookup"><span data-stu-id="372f9-132">**Debit:** Short-term lease liability XXX</span></span><br>
<span data-ttu-id="372f9-133">**Hyvitys:** Vuokrasopimusvelka XXX</span><span class="sxs-lookup"><span data-stu-id="372f9-133">**Credit:** Lease liability XXX</span></span>

## <a name="depreciation-expense"></a><span data-ttu-id="372f9-134">Poistokulu</span><span class="sxs-lookup"><span data-stu-id="372f9-134">Depreciation expense</span></span>

<span data-ttu-id="372f9-135">Tili liittyy kuluun, joka liittyy käyttöoikeusomaisuuserän poistoon IFRS 16-, ASC 842- ja rahoitusleasingsopimusstandardeihin IAS 17:n ja ASC 840:n mukaan.</span><span class="sxs-lookup"><span data-stu-id="372f9-135">The account is associated with the expense that is related to the depreciation of the ROU asset under IFRS 16, ASC 842, and finance leases under IAS 17 and ASC 840.</span></span> <span data-ttu-id="372f9-136">Tätä tiliä veloitetaan, kun käyttöoikeusomaisuuserä poistetaan kuukausittain.</span><span class="sxs-lookup"><span data-stu-id="372f9-136">This account is debited when an ROU asset is depreciated each month.</span></span>

<span data-ttu-id="372f9-137">**Esimerkki kirjauskansiovienneistä:** Poistokertymä</span><span class="sxs-lookup"><span data-stu-id="372f9-137">**Example journal entries:** Depreciation accrual</span></span><br>
<span data-ttu-id="372f9-138">**Veloitus:** Poistokulu XXX</span><span class="sxs-lookup"><span data-stu-id="372f9-138">**Debit:** Depreciation expense XXX</span></span><br>
<span data-ttu-id="372f9-139">**Hyvitys:** Kumulatiivinen poisto XXX</span><span class="sxs-lookup"><span data-stu-id="372f9-139">**Credit:** Accumulated Depreciation XXX</span></span>

## <a name="gainloss-on-lease-modification"></a><span data-ttu-id="372f9-140">Vuokranmuokkauksen voitto/tappio</span><span class="sxs-lookup"><span data-stu-id="372f9-140">Gain/loss on lease modification</span></span>

<span data-ttu-id="372f9-141">Tili on liitetty voittoihin tai tappioihin, jotka vuokrasopimuksen muokkauksista saadaan.</span><span class="sxs-lookup"><span data-stu-id="372f9-141">The account is associated with any gains or losses that arise from lease modifications.</span></span> <span data-ttu-id="372f9-142">Voitto saatetaan saada vuokrasopimuksen muokkauksen aikana, jos muokkaus vähentää vuokrasopimusvelkaa summalla, joka ylittää käyttöoikeusomaisuuserän kirjanpitoarvon.</span><span class="sxs-lookup"><span data-stu-id="372f9-142">A gain might arise during a lease modification if the modification decreases the lease liability by an amount that exceeds the carrying value of the ROU asset.</span></span>

<span data-ttu-id="372f9-143">Vuokrasopimuksen nykyinen kirjanpitoarvo on esimerkiksi 150 000 $ ja käyttöoikeusomaisuuserän 100 000 $.</span><span class="sxs-lookup"><span data-stu-id="372f9-143">For example, a lease has a current carrying value of the lease liability of $150,000 and a carrying value of the ROU asset of $100,000.</span></span> <span data-ttu-id="372f9-144">Vuokrasopimusta muokataan, ja muokkaus tuottaa tulevalle vähimmäisvuokralle (PVFMLP) uuden arvon 40 000 $.</span><span class="sxs-lookup"><span data-stu-id="372f9-144">The lease is modified, and this modification produces a new present value of the future minimum lease payments (PVFMLP) of $40,000.</span></span> <span data-ttu-id="372f9-145">Tämän vuoksi vuokrasopimusvelkaa veloitetaan 110 000 $:n verran (150 000–40 000 $).</span><span class="sxs-lookup"><span data-stu-id="372f9-145">Therefore, the lease liability will be debited by $110,000 ($150,000 – $40,000).</span></span> <span data-ttu-id="372f9-146">Koska käyttöoikeusomaisuuserän arvo on vain 100 000 $, 110 000 $:n arvoisen vähennyksen vuoksi erän arvo on alle 0 (nolla).</span><span class="sxs-lookup"><span data-stu-id="372f9-146">Because the ROU asset is only $100,000, the decrease of $110,000 will decrease the asset past 0 (zero).</span></span> <span data-ttu-id="372f9-147">Kirjanpidon ohjeissa sanotaan, että jäljellä oleva arvo tulee kirjata voittotilille.</span><span class="sxs-lookup"><span data-stu-id="372f9-147">Therefore, the accounting guidance states that the remainder should be booked to a gain account.</span></span> <span data-ttu-id="372f9-148">Tässä tapauksessa lopullinen kirjauskansiovienti on vuokrasopimusvelan veloitus (110 000 $), vuokrasopimuksen resurssin hyvitys (100 000 $) ja voittotilin hyvitys (10 000 $).</span><span class="sxs-lookup"><span data-stu-id="372f9-148">In this case, the final journal entry will be a debit to the lease liability for $110,000, a credit to the lease asset for $100,000, and a credit to the gain account for $10,000.</span></span>

<span data-ttu-id="372f9-149">**Esimerkki kirjauskansiovienneistä:** Vuokrasopimuksen muokkaus</span><span class="sxs-lookup"><span data-stu-id="372f9-149">**Example journal entries:** Lease modification</span></span><br>
<span data-ttu-id="372f9-150">**Veloitus:** Vuokrasopimusvelka XXX</span><span class="sxs-lookup"><span data-stu-id="372f9-150">**Debit:** Lease liability XXX</span></span><br>
<span data-ttu-id="372f9-151">**Hyvitys:** Vuokrasopimuksen resurssi XXX</span><span class="sxs-lookup"><span data-stu-id="372f9-151">**Credit:** Lease Asset XXX</span></span><br>
<span data-ttu-id="372f9-152">**Hyvitys:** Voitto XXX</span><span class="sxs-lookup"><span data-stu-id="372f9-152">**Credit:** Gain XXX</span></span>

## <a name="accumulated-depreciation"></a><span data-ttu-id="372f9-153">Kertynyt poisto</span><span class="sxs-lookup"><span data-stu-id="372f9-153">Accumulated depreciation</span></span>

<span data-ttu-id="372f9-154">Tili on liitetty käyttöoikeusomaisuuserän vastatilille.</span><span class="sxs-lookup"><span data-stu-id="372f9-154">The account is associated with the contra-asset account of the ROU asset.</span></span> <span data-ttu-id="372f9-155">Tätä tiliä hyvitetään poistokulun kirjaamisen yhteydessä.</span><span class="sxs-lookup"><span data-stu-id="372f9-155">This account is credited when a depreciation expense is posted.</span></span>

<span data-ttu-id="372f9-156">**Esimerkki kirjauskansiovienneistä:** Poistokertymä</span><span class="sxs-lookup"><span data-stu-id="372f9-156">**Example journal entries:** Depreciation accrual</span></span><br>
<span data-ttu-id="372f9-157">**Veloitus:** Poistokulu XXX</span><span class="sxs-lookup"><span data-stu-id="372f9-157">**Debit:** Depreciation expense XXX</span></span><br>
<span data-ttu-id="372f9-158">**Hyvitys:** Kumulatiivinen poisto XXX</span><span class="sxs-lookup"><span data-stu-id="372f9-158">**Credit:** Accumulated depreciation XXX</span></span>

## <a name="retained-earnings"></a><span data-ttu-id="372f9-159">Jakamaton voitto</span><span class="sxs-lookup"><span data-stu-id="372f9-159">Retained earnings</span></span>

<span data-ttu-id="372f9-160">Kertyneisiin tuottoihin liittyvä tili.</span><span class="sxs-lookup"><span data-stu-id="372f9-160">The account is associated with retained earnings.</span></span> <span data-ttu-id="372f9-161">Tätä tiliä veloitetaan tai hyvitetään siirtymäoikaisun kirjauskansioviennissä käyttämällä kokonaan takautuvaa menetelmää tai päivittävää kumulatiivista vaihtoehto A -menetelmää.</span><span class="sxs-lookup"><span data-stu-id="372f9-161">This account might be either debited or credited in a transition adjustment journal entry by using the full retrospective method or the cumulative catch-up option A method.</span></span> <span data-ttu-id="372f9-162">Alkuperäisen käyttöoikeusomaisuuserän ja vuokrasopimusvelan välinen ero kirjataan kertyneisiin tuottoihin.</span><span class="sxs-lookup"><span data-stu-id="372f9-162">The difference between the initial ROU asset and lease liability is booked to retained earnings.</span></span> <span data-ttu-id="372f9-163">Harvoissa tapauksissa myös vuokrasopimuksen muokkaus vaikuttaa kertyneisiin tuottoihin, jos vuokrasopimuksen luokittelu muutetaan rahoitusleasingsopimuksesta käyttöleasingsopimukseksi ja käyttöoikeusomaisuuserä korotetaan tai alennetaan niin, että se vastaa vuokrasopimusvelkaa.</span><span class="sxs-lookup"><span data-stu-id="372f9-163">In rare cases, the retained earnings might also be affected during lease modification, if the classification of a lease is changed from finance to operating to write the ROU asset up or down so that it equals the lease liability.</span></span>

<span data-ttu-id="372f9-164">**Esimerkki kirjauskansiovienneistä:** Siirtymän oikaisu (kokonaan takautuva menetelmä tai päivittävä kumulatiivinen vaihtoehto A -menetelmä)</span><span class="sxs-lookup"><span data-stu-id="372f9-164">**Example journal entries:** Transition adjustment (full retrospective or cumulative catch-up option A method)</span></span><br>
<span data-ttu-id="372f9-165">**Veloitus:** Vuokrasopimusvelka XXX</span><span class="sxs-lookup"><span data-stu-id="372f9-165">**Debit:** Lease liability XXX</span></span><br>
<span data-ttu-id="372f9-166">**Hyvitys:** Vuokrasopimuksen resurssi XXX</span><span class="sxs-lookup"><span data-stu-id="372f9-166">**Credit:** Lease asset XXX</span></span><br>
<span data-ttu-id="372f9-167">**Hyvitys:** Kertynyt tuotto XXX</span><span class="sxs-lookup"><span data-stu-id="372f9-167">**Credit:** Retained earnings XXX</span></span>

## <a name="variable-payment"></a><span data-ttu-id="372f9-168">Muuttuva maksu</span><span class="sxs-lookup"><span data-stu-id="372f9-168">Variable payment</span></span>

<span data-ttu-id="372f9-169">Tämä tili liittyy muuttuviin vuoksiin, jotka indeksin uudelleenarviointi luo ASC 842-, ASC 840- ja IAS 17 -vuokrasopimusten avulla.</span><span class="sxs-lookup"><span data-stu-id="372f9-169">The account is associated with variable lease payments that are produced by an index revaluation under ASC 842, ASC 840, and IAS 17 leases.</span></span> <span data-ttu-id="372f9-170">Vuokra-aikataulussa muuttuvat maksut sisältyvät **Muuttuva maksu** -sarakkeeseen.</span><span class="sxs-lookup"><span data-stu-id="372f9-170">In the lease payment schedule, variable payments are included in the **Variable payment** column.</span></span> <span data-ttu-id="372f9-171">Tätä tiliä veloitetaan, kun lasku luodaan muuttuvan maksun sisältävälle maksuaikatauluriville.</span><span class="sxs-lookup"><span data-stu-id="372f9-171">This account is debited when an invoice is created against a payment schedule line that contains a variable payment.</span></span>

<span data-ttu-id="372f9-172">**Esimerkki kirjauskansiovienneistä:** Vuokra</span><span class="sxs-lookup"><span data-stu-id="372f9-172">**Example journal entries:** Lease payment</span></span><br>
<span data-ttu-id="372f9-173">**Veloitus:** Vuokrasopimusvelka XXX</span><span class="sxs-lookup"><span data-stu-id="372f9-173">**Debit:** Lease liability XXX</span></span><br>
<span data-ttu-id="372f9-174">**Veloitus:** Muuttuva maksu XXX</span><span class="sxs-lookup"><span data-stu-id="372f9-174">**Debit:** Variable payment XXX</span></span><br>
<span data-ttu-id="372f9-175">**Hyvitys:** Toimittajan maksettava / maksu XXX</span><span class="sxs-lookup"><span data-stu-id="372f9-175">**Credit:** Vendor payable/lease payment XXX</span></span>

## <a name="deferred-rent-asset-liability"></a><span data-ttu-id="372f9-176">Toteutumaton vuokrauksen resurssi (velka)</span><span class="sxs-lookup"><span data-stu-id="372f9-176">Deferred rent asset (liability)</span></span>

<span data-ttu-id="372f9-177">Tili liitetään toteutumattomaan vuokrauksen resurssiin tai velkaan, jonka toteutumattoman vuokran käsittelyn vuokrasopimus luo.</span><span class="sxs-lookup"><span data-stu-id="372f9-177">The account is associated with the deferred rent asset or liability that is produced by a deferred rent treatment lease.</span></span> <span data-ttu-id="372f9-178">Tätä tiliä veloitetaan, kun lasku kirjataan toteutumattoman vuokran käsittelyn vuokrasopimuksen mukaan, jos vuokrasumma on enemmän kuin kauden suora vuokrakulu.</span><span class="sxs-lookup"><span data-stu-id="372f9-178">This account is debited when an invoice is posted against a deferred rent treatment lease, if the lease payment amount is more than the period's straight-line rent expense.</span></span> <span data-ttu-id="372f9-179">Se hyvitetään, jos vuokra on vähemmän kuin kauden suora vuokrakulu.</span><span class="sxs-lookup"><span data-stu-id="372f9-179">It's credited if the lease payment is less than the period's straight-line rent expense.</span></span>

<span data-ttu-id="372f9-180">**Esimerkki kirjauskansiovienneistä:** Vuokra (toteutumattoman vuokran käsittelyn vuokrasopimus)</span><span class="sxs-lookup"><span data-stu-id="372f9-180">**Example journal entries:** Lease payment (deferred rent treatment lease)</span></span><br>
<span data-ttu-id="372f9-181">**Veloitus:** Vuokran kulu XXX</span><span class="sxs-lookup"><span data-stu-id="372f9-181">**Debit:** Lease expense XXX</span></span><br>
<span data-ttu-id="372f9-182">**Hyvitys:** Toteutumattoman vuokran velka XXX</span><span class="sxs-lookup"><span data-stu-id="372f9-182">**Credit:** Deferred rent liability XXX</span></span><br>
<span data-ttu-id="372f9-183">**Hyvitys:** Toimittajan maksettava / maksu XXX</span><span class="sxs-lookup"><span data-stu-id="372f9-183">**Credit:** Vendor payable/lease payment XXX</span></span>

## <a name="lease-expense"></a><span data-ttu-id="372f9-184">Vuokran kulu</span><span class="sxs-lookup"><span data-stu-id="372f9-184">Lease expense</span></span>

<span data-ttu-id="372f9-185">Tili liittyy vuokran kuluun, jos vuokra luokitellaan toteutumattoman vuokran käsittelyn vuokrasopimukseksi.</span><span class="sxs-lookup"><span data-stu-id="372f9-185">The account is associated with the lease expense if the lease is classified as a deferred rent treatment lease.</span></span> <span data-ttu-id="372f9-186">Tätä tiliä veloitetaan, kun lasku kirjataan toteutumattoman vuokran käsittelyn vuokrasopimuksen mukaan.</span><span class="sxs-lookup"><span data-stu-id="372f9-186">This account is debited when an invoice is posted against a deferred rent treatment lease.</span></span>

<span data-ttu-id="372f9-187">**Esimerkki kirjauskansiovienneistä:** Vuokra (toteutumattoman vuokran käsittelyn vuokrasopimus)</span><span class="sxs-lookup"><span data-stu-id="372f9-187">**Example journal entries:** Lease payment (deferred rent treatment lease)</span></span><br>
<span data-ttu-id="372f9-188">**Veloitus:** Vuokran kulu XXX</span><span class="sxs-lookup"><span data-stu-id="372f9-188">**Debit:** Lease expense XXX</span></span><br>
<span data-ttu-id="372f9-189">**Hyvitys:** Toteutumattoman vuokran velka XXX</span><span class="sxs-lookup"><span data-stu-id="372f9-189">**Credit:** Deferred rent liability XXX</span></span><br>
<span data-ttu-id="372f9-190">**Hyvitys:** Toimittajan maksettava / maksu XXX</span><span class="sxs-lookup"><span data-stu-id="372f9-190">**Credit:** Vendor payable/lease payment XXX</span></span>

## <a name="impairment-expense"></a><span data-ttu-id="372f9-191">Arvonalennuksen kulu</span><span class="sxs-lookup"><span data-stu-id="372f9-191">Impairment expense</span></span>

<span data-ttu-id="372f9-192">Tilille kirjataan, kun vuokran arvoa alennetaan.</span><span class="sxs-lookup"><span data-stu-id="372f9-192">The account is posted against when a lease is impaired.</span></span> <span data-ttu-id="372f9-193">Tätä tiliä veloitetaan, kun taas käyttöoikeusomaisuuserän tiliä hyvitetään suoraan.</span><span class="sxs-lookup"><span data-stu-id="372f9-193">This account is debited, whereas the ROU asset account is directly credited.</span></span>

<span data-ttu-id="372f9-194">**Esimerkki kirjauskansiovienneistä:** Vuokra</span><span class="sxs-lookup"><span data-stu-id="372f9-194">**Example journal entries:** Lease payment</span></span><br>
<span data-ttu-id="372f9-195">**Veloitus:** Arvonalennuksen kulu XXX</span><span class="sxs-lookup"><span data-stu-id="372f9-195">**Debit:** Impairment expense XXX</span></span><br>
<span data-ttu-id="372f9-196">**Hyvitys:** Käyttöoikeusomaisuuserä XXX</span><span class="sxs-lookup"><span data-stu-id="372f9-196">**Credit:** ROU asset XXX</span></span>

## <a name="lease-payment"></a><span data-ttu-id="372f9-197">Vuokra</span><span class="sxs-lookup"><span data-stu-id="372f9-197">Lease payment</span></span>

<span data-ttu-id="372f9-198">Tilille kirjataan, jos **Maksu toimittajalle** -parametri on poistettu käytöstä.</span><span class="sxs-lookup"><span data-stu-id="372f9-198">The account is posted against if the **Pay to Vendor** parameter is turned off.</span></span> <span data-ttu-id="372f9-199">Tiliä hyvitetään toimittajan maksettavan sijaan, jos parametri on poistettu käytöstä.</span><span class="sxs-lookup"><span data-stu-id="372f9-199">This account is credited instead of the vendor payable if the parameter is turned off.</span></span>

<span data-ttu-id="372f9-200">**Esimerkki kirjauskansiovienneistä:** Vuokra</span><span class="sxs-lookup"><span data-stu-id="372f9-200">**Example journal entries:** Lease payment</span></span><br>
<span data-ttu-id="372f9-201">**Veloitus:** Vuokrasopimusvelka XXX</span><span class="sxs-lookup"><span data-stu-id="372f9-201">**Debit:** Lease liability XXX</span></span><br>
<span data-ttu-id="372f9-202">**Hyvitys:** Vuokra XXX</span><span class="sxs-lookup"><span data-stu-id="372f9-202">**Credit:** Lease payment XXX</span></span>

## <a name="expense-type-postings"></a><span data-ttu-id="372f9-203">Kulutyypin kirjaukset</span><span class="sxs-lookup"><span data-stu-id="372f9-203">Expense type postings</span></span>

<span data-ttu-id="372f9-204">Kullekin kulutyypille valittua tiliä veloitetaan, kun luodaan maksu, jonka tyyppi on Kulu.</span><span class="sxs-lookup"><span data-stu-id="372f9-204">The account that is selected for each expense type is debited when a payment for that expense type is generated.</span></span> <span data-ttu-id="372f9-205">Jos tilin kulutyypiksi on määritetty esimerkiksi **Vakuutus**, tiliä veloitetaan aina, kun lasku tai maksukirjauskansiovienti luodaan vakuutuskulun toimeenpanokustannusaikataulusta.</span><span class="sxs-lookup"><span data-stu-id="372f9-205">For example, the account that is specified for the **Insurance** expense type is debited whenever an invoice or payment journal entry is created from the executory cost schedule for insurance expense.</span></span>

<span data-ttu-id="372f9-206">**Esimerkki kirjauskansiovienneistä:** Vakuutusmaksu</span><span class="sxs-lookup"><span data-stu-id="372f9-206">**Example journal entries:** Insurance payment</span></span><br>
<span data-ttu-id="372f9-207">**Veloitus:** Vakuutuskulutyypin tili XXX</span><span class="sxs-lookup"><span data-stu-id="372f9-207">**Debit:** Insurance expense type account XXX</span></span><br>
<span data-ttu-id="372f9-208">**Hyvitys:** Vastatili XXX</span><span class="sxs-lookup"><span data-stu-id="372f9-208">**Credit:** Offset account XXX</span></span>

> [!NOTE]
> <span data-ttu-id="372f9-209">Vastatili valitaan toimeenpanokustannuksen maksuaikataulun rivien vuokratasolla.</span><span class="sxs-lookup"><span data-stu-id="372f9-209">The offset account is selected at the lease level on the lines for the executory cost payment schedule.</span></span> <span data-ttu-id="372f9-210">Tämä vastatili voidaan liittää toimittajaan tai kirjanpitotiliin.</span><span class="sxs-lookup"><span data-stu-id="372f9-210">This offset account can associated with the vendor, or with a ledger account.</span></span>
