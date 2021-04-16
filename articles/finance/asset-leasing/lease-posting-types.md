---
title: Vuokrauksen kirjaustyypit
description: Tässä ohjeaiheessa kuvataan kirjaustyypit, joita käytetään resurssien vuokratapahtumissa.
author: moaamer
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: ddc229f3ab8e048390f27503e2c6c26bd1a6f24f
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/01/2021
ms.locfileid: "5841138"
---
# <a name="lease-posting-types"></a><span data-ttu-id="a39b5-103">Vuokrauksen kirjaustyypit</span><span class="sxs-lookup"><span data-stu-id="a39b5-103">Lease posting types</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a39b5-104">Tässä ohjeaiheessa kuvataan kirjaustyypit, joita käytetään resurssien vuokratapahtumissa.</span><span class="sxs-lookup"><span data-stu-id="a39b5-104">This topic describes the posting types that are used for asset leasing transactions.</span></span>

## <a name="lease-asset"></a><span data-ttu-id="a39b5-105">Vuokraresurssi</span><span class="sxs-lookup"><span data-stu-id="a39b5-105">Lease asset</span></span>

<span data-ttu-id="a39b5-106">Tili liittyy käyttöoikeusomaisuuserään.</span><span class="sxs-lookup"><span data-stu-id="a39b5-106">The account is associated with the right-of-use (ROU) asset.</span></span> <span data-ttu-id="a39b5-107">Tätä tiliä veloitetaan, kun vuokra kirjataan alun perin uusien vuokrauksen tilinpäätösstandardien ASC 842:n (Accounting Standards Codification Topic 842) ja IFRS 16:n (International Financial Reporting Standard 16) mukaan.</span><span class="sxs-lookup"><span data-stu-id="a39b5-107">This account is debited when a lease is initially recognized under the new lease accounting standards, Accounting Standards Codification Topic 842 (ASC 842) and International Financial Reporting Standard 16 (IFRS 16).</span></span> <span data-ttu-id="a39b5-108">Jos kyseessä on muokattu vuokra, tätä tiliä voidaan veloittaa tai hyvittää sen mukaan, lisääkö muokkaus vuokravelkaa vai vähentääkö se sitä.</span><span class="sxs-lookup"><span data-stu-id="a39b5-108">For a modified lease, this account might be either debited or credited, depending on whether the modification increases or decreases the lease liability.</span></span>

<span data-ttu-id="a39b5-109">**Esimerkki kirjauskansiovienneistä:** Alkuperäinen kirjaus</span><span class="sxs-lookup"><span data-stu-id="a39b5-109">**Example journal entries:** Initial recognition</span></span><br>
<span data-ttu-id="a39b5-110">**Veloitus:** Vuokrasopimuksen resurssi XXX</span><span class="sxs-lookup"><span data-stu-id="a39b5-110">**Debit:** Lease asset XXX</span></span><br>
<span data-ttu-id="a39b5-111">**Hyvitys:** Vuokrasopimusvelka XXX</span><span class="sxs-lookup"><span data-stu-id="a39b5-111">**Credit:** Lease liability XXX</span></span>

## <a name="lease-liability"></a><span data-ttu-id="a39b5-112">Vuokrasopimusvelka</span><span class="sxs-lookup"><span data-stu-id="a39b5-112">Lease liability</span></span>

<span data-ttu-id="a39b5-113">Tili liittyy vuokrasopimusvelkaan, joka toteutuu kun maksut diskontataan uusien IFRS 16- ja ASC 842 -standardien mukaan.</span><span class="sxs-lookup"><span data-stu-id="a39b5-113">The account is associated with the lease liability that occurs when payments are discounted under the new IFRS 16 and ASC 842 standards.</span></span> <span data-ttu-id="a39b5-114">Tätä tiliä hyvitetään, kun vuokra kirjataan alun perin uusien standardien mukaan.</span><span class="sxs-lookup"><span data-stu-id="a39b5-114">This account is credited when a lease is initially recognized under the new standards.</span></span> <span data-ttu-id="a39b5-115">Vuokrat veloitetaan ja korkokertymät hyvitetään.</span><span class="sxs-lookup"><span data-stu-id="a39b5-115">It's debited for lease payments and credited for interest accruals.</span></span>

<span data-ttu-id="a39b5-116">**Esimerkki kirjauskansiovienneistä:** Alkuperäinen kirjaus</span><span class="sxs-lookup"><span data-stu-id="a39b5-116">**Example journal entries:** Initial recognition</span></span><br>
<span data-ttu-id="a39b5-117">**Veloitus:** Vuokrasopimuksen resurssi XXX</span><span class="sxs-lookup"><span data-stu-id="a39b5-117">**Debit:** Lease asset XXX</span></span><br>
<span data-ttu-id="a39b5-118">**Hyvitys:** Vuokrasopimusvelka XXX</span><span class="sxs-lookup"><span data-stu-id="a39b5-118">**Credit:** Lease liability XXX</span></span>

<span data-ttu-id="a39b5-119">**Esimerkki kirjauskansiovienneistä:** Korkokertymä</span><span class="sxs-lookup"><span data-stu-id="a39b5-119">**Example journal entries:** Interest accrual</span></span><br>
<span data-ttu-id="a39b5-120">**Veloitus:** Korkokustannus XXX</span><span class="sxs-lookup"><span data-stu-id="a39b5-120">**Debit:** Interest expense XXX</span></span><br>
<span data-ttu-id="a39b5-121">**Hyvitys:** Vuokrasopimusvelka XXX</span><span class="sxs-lookup"><span data-stu-id="a39b5-121">**Credit:** Lease liability XXX</span></span>

<span data-ttu-id="a39b5-122">**Esimerkki kirjauskansiovienneistä:** Vuokra</span><span class="sxs-lookup"><span data-stu-id="a39b5-122">**Example journal entries:** Lease payment</span></span><br>
<span data-ttu-id="a39b5-123">**Veloitus:** Vuokrasopimusvelka XXX</span><span class="sxs-lookup"><span data-stu-id="a39b5-123">**Debit:** Lease liability XXX</span></span><br>
<span data-ttu-id="a39b5-124">**Hyvitys:** Toimittajan maksettava / maksu XXX</span><span class="sxs-lookup"><span data-stu-id="a39b5-124">**Credit:** Vendor payable/lease payment XXX</span></span>

## <a name="short-term-lease-liability"></a><span data-ttu-id="a39b5-125">Lyhytaikainen vuokravelka</span><span class="sxs-lookup"><span data-stu-id="a39b5-125">Short-term lease liability</span></span>

<span data-ttu-id="a39b5-126">Tili liittyy lyhytaikaiseen vuokrasopimusvelkaan, kun lyhytaikaisen vuokrasopimusvelan uudelleenluokittelun kirjauskansiovienti kirjataan.</span><span class="sxs-lookup"><span data-stu-id="a39b5-126">The account is associated with the short-term lease liability when the short-term lease liability reclass journal entry is posted.</span></span> <span data-ttu-id="a39b5-127">Tälle tilille hyvitetään lyhytaikainen velka kuoletusaikataulusta kuukauden viimeisenä päivänä.</span><span class="sxs-lookup"><span data-stu-id="a39b5-127">This account is credited for the short-term liability from the amortization schedule on the last day of the month.</span></span> <span data-ttu-id="a39b5-128">Sama summa veloitetaan kuitenkin seuraavan kuukauden ensimmäisenä päivänä.</span><span class="sxs-lookup"><span data-stu-id="a39b5-128">However, the same amount is debited on the first day of the next month.</span></span>

<span data-ttu-id="a39b5-129">**Esimerkki kirjauskansiovienneistä:** Lyhytaikaisen vuokrasopimusvelan uudelleenluokittelu</span><span class="sxs-lookup"><span data-stu-id="a39b5-129">**Example journal entries:** Short-term lease liability reclass</span></span><br>
<span data-ttu-id="a39b5-130">**Veloitus:** Vuokrasopimusvelka XXX</span><span class="sxs-lookup"><span data-stu-id="a39b5-130">**Debit:** Lease liability XXX</span></span><br>
<span data-ttu-id="a39b5-131">**Hyvitys:** Lyhytaikainen vuokrasopimusvelka XXX</span><span class="sxs-lookup"><span data-stu-id="a39b5-131">**Credit:** Short-term lease liability XXX</span></span><br>
<span data-ttu-id="a39b5-132">**Veloitus:** Lyhytaikainen vuokrasopimusvelka XXX</span><span class="sxs-lookup"><span data-stu-id="a39b5-132">**Debit:** Short-term lease liability XXX</span></span><br>
<span data-ttu-id="a39b5-133">**Hyvitys:** Vuokrasopimusvelka XXX</span><span class="sxs-lookup"><span data-stu-id="a39b5-133">**Credit:** Lease liability XXX</span></span>

## <a name="depreciation-expense"></a><span data-ttu-id="a39b5-134">Poistokulu</span><span class="sxs-lookup"><span data-stu-id="a39b5-134">Depreciation expense</span></span>

<span data-ttu-id="a39b5-135">Tili liittyy kuluun, joka liittyy käyttöoikeusomaisuuserän poistoon IFRS 16-, ASC 842- ja rahoitusleasingsopimusstandardeihin IAS 17:n ja ASC 840:n mukaan.</span><span class="sxs-lookup"><span data-stu-id="a39b5-135">The account is associated with the expense that is related to the depreciation of the ROU asset under IFRS 16, ASC 842, and finance leases under IAS 17 and ASC 840.</span></span> <span data-ttu-id="a39b5-136">Tätä tiliä veloitetaan, kun käyttöoikeusomaisuuserä poistetaan kuukausittain.</span><span class="sxs-lookup"><span data-stu-id="a39b5-136">This account is debited when an ROU asset is depreciated each month.</span></span>

<span data-ttu-id="a39b5-137">**Esimerkki kirjauskansiovienneistä:** Poistokertymä</span><span class="sxs-lookup"><span data-stu-id="a39b5-137">**Example journal entries:** Depreciation accrual</span></span><br>
<span data-ttu-id="a39b5-138">**Veloitus:** Poistokulu XXX</span><span class="sxs-lookup"><span data-stu-id="a39b5-138">**Debit:** Depreciation expense XXX</span></span><br>
<span data-ttu-id="a39b5-139">**Hyvitys:** Kumulatiivinen poisto XXX</span><span class="sxs-lookup"><span data-stu-id="a39b5-139">**Credit:** Accumulated Depreciation XXX</span></span>

## <a name="gainloss-on-lease-modification"></a><span data-ttu-id="a39b5-140">Vuokranmuokkauksen voitto/tappio</span><span class="sxs-lookup"><span data-stu-id="a39b5-140">Gain/loss on lease modification</span></span>

<span data-ttu-id="a39b5-141">Tili on liitetty voittoihin tai tappioihin, jotka vuokrasopimuksen muokkauksista saadaan.</span><span class="sxs-lookup"><span data-stu-id="a39b5-141">The account is associated with any gains or losses that arise from lease modifications.</span></span> <span data-ttu-id="a39b5-142">Voitto saatetaan saada vuokrasopimuksen muokkauksen aikana, jos muokkaus vähentää vuokrasopimusvelkaa summalla, joka ylittää käyttöoikeusomaisuuserän kirjanpitoarvon.</span><span class="sxs-lookup"><span data-stu-id="a39b5-142">A gain might arise during a lease modification if the modification decreases the lease liability by an amount that exceeds the carrying value of the ROU asset.</span></span>

<span data-ttu-id="a39b5-143">Vuokrasopimuksen nykyinen kirjanpitoarvo on esimerkiksi 150 000 $ ja käyttöoikeusomaisuuserän 100 000 $.</span><span class="sxs-lookup"><span data-stu-id="a39b5-143">For example, a lease has a current carrying value of the lease liability of $150,000 and a carrying value of the ROU asset of $100,000.</span></span> <span data-ttu-id="a39b5-144">Vuokrasopimusta muokataan, ja muokkaus tuottaa tulevalle vähimmäisvuokralle (PVFMLP) uuden arvon 40 000 $.</span><span class="sxs-lookup"><span data-stu-id="a39b5-144">The lease is modified, and this modification produces a new present value of the future minimum lease payments (PVFMLP) of $40,000.</span></span> <span data-ttu-id="a39b5-145">Tämän vuoksi vuokrasopimusvelkaa veloitetaan 110 000 $:n verran (150 000–40 000 $).</span><span class="sxs-lookup"><span data-stu-id="a39b5-145">Therefore, the lease liability will be debited by $110,000 ($150,000 – $40,000).</span></span> <span data-ttu-id="a39b5-146">Koska käyttöoikeusomaisuuserän arvo on vain 100 000 $, 110 000 $:n arvoisen vähennyksen vuoksi erän arvo on alle 0 (nolla).</span><span class="sxs-lookup"><span data-stu-id="a39b5-146">Because the ROU asset is only $100,000, the decrease of $110,000 will decrease the asset past 0 (zero).</span></span> <span data-ttu-id="a39b5-147">Kirjanpidon ohjeissa sanotaan, että jäljellä oleva arvo tulee kirjata voittotilille.</span><span class="sxs-lookup"><span data-stu-id="a39b5-147">Therefore, the accounting guidance states that the remainder should be booked to a gain account.</span></span> <span data-ttu-id="a39b5-148">Tässä tapauksessa lopullinen kirjauskansiovienti on vuokrasopimusvelan veloitus (110 000 $), vuokrasopimuksen resurssin hyvitys (100 000 $) ja voittotilin hyvitys (10 000 $).</span><span class="sxs-lookup"><span data-stu-id="a39b5-148">In this case, the final journal entry will be a debit to the lease liability for $110,000, a credit to the lease asset for $100,000, and a credit to the gain account for $10,000.</span></span>

<span data-ttu-id="a39b5-149">**Esimerkki kirjauskansiovienneistä:** Vuokrasopimuksen muokkaus</span><span class="sxs-lookup"><span data-stu-id="a39b5-149">**Example journal entries:** Lease modification</span></span><br>
<span data-ttu-id="a39b5-150">**Veloitus:** Vuokrasopimusvelka XXX</span><span class="sxs-lookup"><span data-stu-id="a39b5-150">**Debit:** Lease liability XXX</span></span><br>
<span data-ttu-id="a39b5-151">**Hyvitys:** Vuokrasopimuksen resurssi XXX</span><span class="sxs-lookup"><span data-stu-id="a39b5-151">**Credit:** Lease Asset XXX</span></span><br>
<span data-ttu-id="a39b5-152">**Hyvitys:** Voitto XXX</span><span class="sxs-lookup"><span data-stu-id="a39b5-152">**Credit:** Gain XXX</span></span>

## <a name="accumulated-depreciation"></a><span data-ttu-id="a39b5-153">Kertynyt poisto</span><span class="sxs-lookup"><span data-stu-id="a39b5-153">Accumulated depreciation</span></span>

<span data-ttu-id="a39b5-154">Tili on liitetty käyttöoikeusomaisuuserän vastatilille.</span><span class="sxs-lookup"><span data-stu-id="a39b5-154">The account is associated with the contra-asset account of the ROU asset.</span></span> <span data-ttu-id="a39b5-155">Tätä tiliä hyvitetään poistokulun kirjaamisen yhteydessä.</span><span class="sxs-lookup"><span data-stu-id="a39b5-155">This account is credited when a depreciation expense is posted.</span></span>

<span data-ttu-id="a39b5-156">**Esimerkki kirjauskansiovienneistä:** Poistokertymä</span><span class="sxs-lookup"><span data-stu-id="a39b5-156">**Example journal entries:** Depreciation accrual</span></span><br>
<span data-ttu-id="a39b5-157">**Veloitus:** Poistokulu XXX</span><span class="sxs-lookup"><span data-stu-id="a39b5-157">**Debit:** Depreciation expense XXX</span></span><br>
<span data-ttu-id="a39b5-158">**Hyvitys:** Kumulatiivinen poisto XXX</span><span class="sxs-lookup"><span data-stu-id="a39b5-158">**Credit:** Accumulated depreciation XXX</span></span>

## <a name="variable-payment"></a><span data-ttu-id="a39b5-159">Muuttuva maksu</span><span class="sxs-lookup"><span data-stu-id="a39b5-159">Variable payment</span></span>

<span data-ttu-id="a39b5-160">Tämä tili liittyy muuttuviin vuoksiin, jotka indeksin uudelleenarviointi luo ASC 842-, ASC 840- ja IAS 17 -vuokrasopimusten avulla.</span><span class="sxs-lookup"><span data-stu-id="a39b5-160">The account is associated with variable lease payments that are produced by an index revaluation under ASC 842, ASC 840, and IAS 17 leases.</span></span> <span data-ttu-id="a39b5-161">Vuokra-aikataulussa muuttuvat maksut sisältyvät **Muuttuva maksu** -sarakkeeseen.</span><span class="sxs-lookup"><span data-stu-id="a39b5-161">In the lease payment schedule, variable payments are included in the **Variable payment** column.</span></span> <span data-ttu-id="a39b5-162">Tätä tiliä veloitetaan, kun lasku luodaan muuttuvan maksun sisältävälle maksuaikatauluriville.</span><span class="sxs-lookup"><span data-stu-id="a39b5-162">This account is debited when an invoice is created against a payment schedule line that contains a variable payment.</span></span>

<span data-ttu-id="a39b5-163">**Esimerkki kirjauskansiovienneistä:** Vuokra</span><span class="sxs-lookup"><span data-stu-id="a39b5-163">**Example journal entries:** Lease payment</span></span><br>
<span data-ttu-id="a39b5-164">**Veloitus:** Vuokrasopimusvelka XXX</span><span class="sxs-lookup"><span data-stu-id="a39b5-164">**Debit:** Lease liability XXX</span></span><br>
<span data-ttu-id="a39b5-165">**Veloitus:** Muuttuva maksu XXX</span><span class="sxs-lookup"><span data-stu-id="a39b5-165">**Debit:** Variable payment XXX</span></span><br>
<span data-ttu-id="a39b5-166">**Hyvitys:** Toimittajan maksettava / maksu XXX</span><span class="sxs-lookup"><span data-stu-id="a39b5-166">**Credit:** Vendor payable/lease payment XXX</span></span>

## <a name="deferred-rent-asset-liability"></a><span data-ttu-id="a39b5-167">Toteutumaton vuokrauksen resurssi (velka)</span><span class="sxs-lookup"><span data-stu-id="a39b5-167">Deferred rent asset (liability)</span></span>

<span data-ttu-id="a39b5-168">Tili liitetään toteutumattomaan vuokrauksen resurssiin tai velkaan, jonka toteutumattoman vuokran käsittelyn vuokrasopimus luo.</span><span class="sxs-lookup"><span data-stu-id="a39b5-168">The account is associated with the deferred rent asset or liability that is produced by a deferred rent treatment lease.</span></span> <span data-ttu-id="a39b5-169">Tätä tiliä veloitetaan, kun lasku kirjataan toteutumattoman vuokran käsittelyn vuokrasopimuksen mukaan, jos vuokrasumma on enemmän kuin kauden suora vuokrakulu.</span><span class="sxs-lookup"><span data-stu-id="a39b5-169">This account is debited when an invoice is posted against a deferred rent treatment lease, if the lease payment amount is more than the period's straight-line rent expense.</span></span> <span data-ttu-id="a39b5-170">Se hyvitetään, jos vuokra on vähemmän kuin kauden suora vuokrakulu.</span><span class="sxs-lookup"><span data-stu-id="a39b5-170">It's credited if the lease payment is less than the period's straight-line rent expense.</span></span>

<span data-ttu-id="a39b5-171">**Esimerkki kirjauskansiovienneistä:** Vuokra (toteutumattoman vuokran käsittelyn vuokrasopimus)</span><span class="sxs-lookup"><span data-stu-id="a39b5-171">**Example journal entries:** Lease payment (deferred rent treatment lease)</span></span><br>
<span data-ttu-id="a39b5-172">**Veloitus:** Vuokran kulu XXX</span><span class="sxs-lookup"><span data-stu-id="a39b5-172">**Debit:** Lease expense XXX</span></span><br>
<span data-ttu-id="a39b5-173">**Hyvitys:** Toteutumattoman vuokran velka XXX</span><span class="sxs-lookup"><span data-stu-id="a39b5-173">**Credit:** Deferred rent liability XXX</span></span><br>
<span data-ttu-id="a39b5-174">**Hyvitys:** Toimittajan maksettava / maksu XXX</span><span class="sxs-lookup"><span data-stu-id="a39b5-174">**Credit:** Vendor payable/lease payment XXX</span></span>

## <a name="lease-expense"></a><span data-ttu-id="a39b5-175">Vuokran kulu</span><span class="sxs-lookup"><span data-stu-id="a39b5-175">Lease expense</span></span>

<span data-ttu-id="a39b5-176">Tili liittyy vuokran kuluun, jos vuokra luokitellaan toteutumattoman vuokran käsittelyn vuokrasopimukseksi.</span><span class="sxs-lookup"><span data-stu-id="a39b5-176">The account is associated with the lease expense if the lease is classified as a deferred rent treatment lease.</span></span> <span data-ttu-id="a39b5-177">Tätä tiliä veloitetaan, kun lasku kirjataan toteutumattoman vuokran käsittelyn vuokrasopimuksen mukaan.</span><span class="sxs-lookup"><span data-stu-id="a39b5-177">This account is debited when an invoice is posted against a deferred rent treatment lease.</span></span>

<span data-ttu-id="a39b5-178">**Esimerkki kirjauskansiovienneistä:** Vuokra (toteutumattoman vuokran käsittelyn vuokrasopimus)</span><span class="sxs-lookup"><span data-stu-id="a39b5-178">**Example journal entries:** Lease payment (deferred rent treatment lease)</span></span><br>
<span data-ttu-id="a39b5-179">**Veloitus:** Vuokran kulu XXX</span><span class="sxs-lookup"><span data-stu-id="a39b5-179">**Debit:** Lease expense XXX</span></span><br>
<span data-ttu-id="a39b5-180">**Hyvitys:** Toteutumattoman vuokran velka XXX</span><span class="sxs-lookup"><span data-stu-id="a39b5-180">**Credit:** Deferred rent liability XXX</span></span><br>
<span data-ttu-id="a39b5-181">**Hyvitys:** Toimittajan maksettava / maksu XXX</span><span class="sxs-lookup"><span data-stu-id="a39b5-181">**Credit:** Vendor payable/lease payment XXX</span></span>

## <a name="impairment-expense"></a><span data-ttu-id="a39b5-182">Arvonalennuksen kulu</span><span class="sxs-lookup"><span data-stu-id="a39b5-182">Impairment expense</span></span>

<span data-ttu-id="a39b5-183">Tilille kirjataan, kun vuokran arvoa alennetaan.</span><span class="sxs-lookup"><span data-stu-id="a39b5-183">The account is posted against when a lease is impaired.</span></span> <span data-ttu-id="a39b5-184">Tätä tiliä veloitetaan, kun taas käyttöoikeusomaisuuserän tiliä hyvitetään suoraan.</span><span class="sxs-lookup"><span data-stu-id="a39b5-184">This account is debited, whereas the ROU asset account is directly credited.</span></span>

<span data-ttu-id="a39b5-185">**Esimerkki kirjauskansiovienneistä:** Vuokra</span><span class="sxs-lookup"><span data-stu-id="a39b5-185">**Example journal entries:** Lease payment</span></span><br>
<span data-ttu-id="a39b5-186">**Veloitus:** Arvonalennuksen kulu XXX</span><span class="sxs-lookup"><span data-stu-id="a39b5-186">**Debit:** Impairment expense XXX</span></span><br>
<span data-ttu-id="a39b5-187">**Hyvitys:** Käyttöoikeusomaisuuserä XXX</span><span class="sxs-lookup"><span data-stu-id="a39b5-187">**Credit:** ROU asset XXX</span></span>

## <a name="lease-payment"></a><span data-ttu-id="a39b5-188">Vuokra</span><span class="sxs-lookup"><span data-stu-id="a39b5-188">Lease payment</span></span>

<span data-ttu-id="a39b5-189">Tilille kirjataan, jos **Maksu toimittajalle** -parametri on poistettu käytöstä.</span><span class="sxs-lookup"><span data-stu-id="a39b5-189">The account is posted against if the **Pay to Vendor** parameter is turned off.</span></span> <span data-ttu-id="a39b5-190">Tiliä hyvitetään toimittajan maksettavan sijaan, jos parametri on poistettu käytöstä.</span><span class="sxs-lookup"><span data-stu-id="a39b5-190">This account is credited instead of the vendor payable if the parameter is turned off.</span></span>

<span data-ttu-id="a39b5-191">**Esimerkki kirjauskansiovienneistä:** Vuokra</span><span class="sxs-lookup"><span data-stu-id="a39b5-191">**Example journal entries:** Lease payment</span></span><br>
<span data-ttu-id="a39b5-192">**Veloitus:** Vuokrasopimusvelka XXX</span><span class="sxs-lookup"><span data-stu-id="a39b5-192">**Debit:** Lease liability XXX</span></span><br>
<span data-ttu-id="a39b5-193">**Hyvitys:** Vuokra XXX</span><span class="sxs-lookup"><span data-stu-id="a39b5-193">**Credit:** Lease payment XXX</span></span>

## <a name="expense-type-postings"></a><span data-ttu-id="a39b5-194">Kulutyypin kirjaukset</span><span class="sxs-lookup"><span data-stu-id="a39b5-194">Expense type postings</span></span>

<span data-ttu-id="a39b5-195">Kullekin kulutyypille valittua tiliä veloitetaan, kun luodaan maksu, jonka tyyppi on Kulu.</span><span class="sxs-lookup"><span data-stu-id="a39b5-195">The account that is selected for each expense type is debited when a payment for that expense type is generated.</span></span> <span data-ttu-id="a39b5-196">Jos tilin kulutyypiksi on määritetty esimerkiksi **Vakuutus**, tiliä veloitetaan aina, kun lasku tai maksukirjauskansiovienti luodaan vakuutuskulun toimeenpanokustannusaikataulusta.</span><span class="sxs-lookup"><span data-stu-id="a39b5-196">For example, the account that is specified for the **Insurance** expense type is debited whenever an invoice or payment journal entry is created from the executory cost schedule for insurance expense.</span></span>

<span data-ttu-id="a39b5-197">**Esimerkki kirjauskansiovienneistä:** Vakuutusmaksu</span><span class="sxs-lookup"><span data-stu-id="a39b5-197">**Example journal entries:** Insurance payment</span></span><br>
<span data-ttu-id="a39b5-198">**Veloitus:** Vakuutuskulutyypin tili XXX</span><span class="sxs-lookup"><span data-stu-id="a39b5-198">**Debit:** Insurance expense type account XXX</span></span><br>
<span data-ttu-id="a39b5-199">**Hyvitys:** Vastatili XXX</span><span class="sxs-lookup"><span data-stu-id="a39b5-199">**Credit:** Offset account XXX</span></span>

> [!NOTE]
> <span data-ttu-id="a39b5-200">Vastatili valitaan toimeenpanokustannuksen maksuaikataulun rivien vuokratasolla.</span><span class="sxs-lookup"><span data-stu-id="a39b5-200">The offset account is selected at the lease level on the lines for the executory cost payment schedule.</span></span> <span data-ttu-id="a39b5-201">Tämä vastatili voidaan liittää toimittajaan tai kirjanpitotiliin.</span><span class="sxs-lookup"><span data-stu-id="a39b5-201">This offset account can associated with the vendor, or with a ledger account.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
