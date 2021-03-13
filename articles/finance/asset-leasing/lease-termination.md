---
title: Vuokrasopimuksen irtisanomisen ehdotus
description: Tässä ohjeaiheessa kerrotaan, miten ehdotetaan vuokran päättämistä.
author: moaamer
manager: Ann Beebe
ms.date: 1/14/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetLease
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2021-1-28
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 144559b14878a44afd8a77648bb5ce1d3ba17832
ms.sourcegitcommit: f8bac7ca2803913fd236adbc3806259a17a110f4
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/06/2021
ms.locfileid: "5131282"
---
# <a name="propose-a-lease-for-termination"></a><span data-ttu-id="521c1-103">Vuokran ehdottaminen irtisanomista varten</span><span class="sxs-lookup"><span data-stu-id="521c1-103">Propose a lease for termination</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="521c1-104">Jos vuokra päätetään etuajassa, käyttöomaisuuden vuokraus voi kirjata irtisanomisen kirjauskansiomerkinnän, joka poistaa vuokravelkaa, käyttöoikeutta (ROU) sekä kertyneitä poistoja, sekä kirjata voiton tai tappion.</span><span class="sxs-lookup"><span data-stu-id="521c1-104">If a lease is terminated early, Asset leasing can record a termination journal entry to write off the lease liability, right-of-use (ROU) asset, and accumulated depreciation, and book a gain or loss.</span></span> <span data-ttu-id="521c1-105">Varhaisen irtisanomisen prosessi päättää vuokra-ajan ja siihen liittyvät vuokrakirjat.</span><span class="sxs-lookup"><span data-stu-id="521c1-105">The early termination process terminates a lease and its associated lease books.</span></span> <span data-ttu-id="521c1-106">Se ei päätä yksittäisiä vuokrakirjoja.</span><span class="sxs-lookup"><span data-stu-id="521c1-106">It doesn't terminate individual lease books.</span></span> <span data-ttu-id="521c1-107">Tässä aiheessa kuvataan toimintoja, jotka mahdollistaa vuokrasopimuksen ehdottamisen irtisanomista varten ja vuokran päättymisen kirjauskansion merkinnän käsittelemisen.</span><span class="sxs-lookup"><span data-stu-id="521c1-107">This topic describes the functionality that lets you propose a lease for termination and process the lease termination journal entry.</span></span>

<span data-ttu-id="521c1-108">Jos vuokra ei ole luokiteltu lykättynä vuokrakäsittelyn vuokrasopimuksina eikä sitä ole liitetty käyttöomaisuuserään, käyttöomaisuuden vuokraus tuottaa seuraava lopetuksen kirjauskansiomerkintä.</span><span class="sxs-lookup"><span data-stu-id="521c1-108">If a lease isn't classified as a deferred rent treatment lease and isn't associated with a fixed asset, Asset leasing produces the following termination journal entry.</span></span>

| <span data-ttu-id="521c1-109">Tapahtuma</span><span class="sxs-lookup"><span data-stu-id="521c1-109">Transaction</span></span>                           | <span data-ttu-id="521c1-110">Debet (Dr.)</span><span class="sxs-lookup"><span data-stu-id="521c1-110">Debit (Dr.)</span></span> | <span data-ttu-id="521c1-111">Kredit (Cr.)</span><span class="sxs-lookup"><span data-stu-id="521c1-111">Credit (Cr.)</span></span> |
|---------------------------------------|-------------|--------------|
| <span data-ttu-id="521c1-112">Dr. Vuokrasopimusvelka</span><span class="sxs-lookup"><span data-stu-id="521c1-112">Dr. Lease liability</span></span>                   | <span data-ttu-id="521c1-113">X</span><span class="sxs-lookup"><span data-stu-id="521c1-113">X</span></span>           |              |
| <span data-ttu-id="521c1-114">Dr. kertynyt poisto</span><span class="sxs-lookup"><span data-stu-id="521c1-114">Dr. Accumulated depreciation</span></span>          | <span data-ttu-id="521c1-115">X</span><span class="sxs-lookup"><span data-stu-id="521c1-115">X</span></span>           |              |
| <span data-ttu-id="521c1-116">Dr. Vuokranmuokkauksen voitto/tappio</span><span class="sxs-lookup"><span data-stu-id="521c1-116">Dr. Gain (loss) on lease modification</span></span> | <span data-ttu-id="521c1-117">X</span><span class="sxs-lookup"><span data-stu-id="521c1-117">X</span></span>           |              |
| <span data-ttu-id="521c1-118">Cr. Vuokraresurssi</span><span class="sxs-lookup"><span data-stu-id="521c1-118">Cr. Lease asset</span></span>                       |             | <span data-ttu-id="521c1-119">X</span><span class="sxs-lookup"><span data-stu-id="521c1-119">X</span></span>            |
| <span data-ttu-id="521c1-120">Cr. Vuokranmuokkauksen voitto/tappio</span><span class="sxs-lookup"><span data-stu-id="521c1-120">Cr. Gain (loss) on lease modification</span></span> |             | <span data-ttu-id="521c1-121">X</span><span class="sxs-lookup"><span data-stu-id="521c1-121">X</span></span>            |

<span data-ttu-id="521c1-122">Jos vuokrakirja on luokiteltu lykätyksi vuokrakirjaksi, merkintä kirjaa lykätyn vuokran saldon ennen voitto- tai tappiotilille päättämistä, kuten tässä näkyy.</span><span class="sxs-lookup"><span data-stu-id="521c1-122">If the lease book is classified as a deferred rent book, the entry writes off the balance of the deferred rent before the termination to the gain or loss account, as shown here.</span></span>

| <span data-ttu-id="521c1-123">Tapahtuma</span><span class="sxs-lookup"><span data-stu-id="521c1-123">Transaction</span></span>                           | <span data-ttu-id="521c1-124">Debet (Dr.)</span><span class="sxs-lookup"><span data-stu-id="521c1-124">Debit (Dr.)</span></span> | <span data-ttu-id="521c1-125">Kredit (Cr.)</span><span class="sxs-lookup"><span data-stu-id="521c1-125">Credit (Cr.)</span></span> | 
|---------------------------------------|-------------|--------------|
| <span data-ttu-id="521c1-126">Dr. Toteutumaton vuokra</span><span class="sxs-lookup"><span data-stu-id="521c1-126">Dr. Deferred rent</span></span>                     | <span data-ttu-id="521c1-127">X</span><span class="sxs-lookup"><span data-stu-id="521c1-127">X</span></span>           |              |
| <span data-ttu-id="521c1-128">Cr. Vuokranmuokkauksen voitto/tappio</span><span class="sxs-lookup"><span data-stu-id="521c1-128">Cr. Gain (loss) on lease modification</span></span> |             | <span data-ttu-id="521c1-129">X</span><span class="sxs-lookup"><span data-stu-id="521c1-129">X</span></span>            |
| <span data-ttu-id="521c1-130">Cr. Toteutumaton vuokra</span><span class="sxs-lookup"><span data-stu-id="521c1-130">Cr. Deferred rent</span></span>                     |             | <span data-ttu-id="521c1-131">X</span><span class="sxs-lookup"><span data-stu-id="521c1-131">X</span></span>            |
| <span data-ttu-id="521c1-132">Dr. Vuokranmuokkauksen voitto/tappio</span><span class="sxs-lookup"><span data-stu-id="521c1-132">Dr. Gain (loss) on lease modification</span></span> | <span data-ttu-id="521c1-133">X</span><span class="sxs-lookup"><span data-stu-id="521c1-133">X</span></span>           |              |

<span data-ttu-id="521c1-134">Jos vuokrakirja on liitetty käyttöomaisuuserään, ROU-resurssi otetaan huomioon käyttöomaisuudessa.</span><span class="sxs-lookup"><span data-stu-id="521c1-134">If the lease book is connected to a fixed asset, the ROU asset is accounted for in Fixed assets.</span></span> <span data-ttu-id="521c1-135">Tämä kirjanpito sisältää varhaisten päättymisten kirjanpidon.</span><span class="sxs-lookup"><span data-stu-id="521c1-135">This accounting includes the accounting for early terminations.</span></span> <span data-ttu-id="521c1-136">Käyttöomaisuuden vuokraus tuottaa seuraavan kirjauskansiomerkinnän, jossa vuokravelka voidaan poistaa.</span><span class="sxs-lookup"><span data-stu-id="521c1-136">Asset leasing produces the following journal entry to write off the lease liability.</span></span>

| <span data-ttu-id="521c1-137">Tapahtuma</span><span class="sxs-lookup"><span data-stu-id="521c1-137">Transaction</span></span>                           | <span data-ttu-id="521c1-138">Debet (Dr.)</span><span class="sxs-lookup"><span data-stu-id="521c1-138">Debit (Dr.)</span></span> | <span data-ttu-id="521c1-139">Kredit (Cr.)</span><span class="sxs-lookup"><span data-stu-id="521c1-139">Credit (Cr.)</span></span> |
|---------------------------------------|-------------|--------------|
| <span data-ttu-id="521c1-140">Dr. Vuokrasopimusvelka</span><span class="sxs-lookup"><span data-stu-id="521c1-140">Dr. Lease liability</span></span>                   | <span data-ttu-id="521c1-141">X</span><span class="sxs-lookup"><span data-stu-id="521c1-141">X</span></span>           |              |
| <span data-ttu-id="521c1-142">Cr. Vuokranmuokkauksen voitto/tappio</span><span class="sxs-lookup"><span data-stu-id="521c1-142">Cr. Gain (loss) on lease modification</span></span> |             | <span data-ttu-id="521c1-143">X</span><span class="sxs-lookup"><span data-stu-id="521c1-143">X</span></span>            |

<span data-ttu-id="521c1-144">Lisätietoja oikeasta tavasta poistaa ROU-käyttöomaisuuserä on kohdassa [käyttöomaisuuserän poistaminen hävikkinä](../fixed-assets/dispose-of-a-fixed-asset-as-scrap.md).</span><span class="sxs-lookup"><span data-stu-id="521c1-144">For information about the correct way to dispose of an ROU asset, see [Dispose of a fixed asset as scrap](../fixed-assets/dispose-of-a-fixed-asset-as-scrap.md).</span></span>

## <a name="propose-a-lease-for-termination"></a><span data-ttu-id="521c1-145">Vuokran ehdottaminen irtisanomista varten</span><span class="sxs-lookup"><span data-stu-id="521c1-145">Propose a lease for termination</span></span>

1. <span data-ttu-id="521c1-146">Siirry vuokraan, joka on lopetettava, ja valitse sitten toimintoruudusta **Irtisanomisehdotus**.</span><span class="sxs-lookup"><span data-stu-id="521c1-146">Go to the lease that must be terminated, and then, on the Action Pane, select **Termination proposal**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="521c1-147">**Irtisanomisehdotus**-painike ei ole käytettävissä, jos kirjaamattomia kirjauskansiomerkintöjä on mille tahansa kirjalle.</span><span class="sxs-lookup"><span data-stu-id="521c1-147">The **Termination proposal** button is unavailable if there are any unposted journal entries against any book.</span></span> <span data-ttu-id="521c1-148">Ennen kuin voit päättää vuokran, sinun on kirjattava tai poistettava kaikki vuokralle luodut kirjauskansiomerkinnät.</span><span class="sxs-lookup"><span data-stu-id="521c1-148">Before you can terminate the lease, you must post or delete any journal entries that have been created against the lease.</span></span>

2. <span data-ttu-id="521c1-149">Määritä näyttöön tulevassa valintaikkunassa irtisanomisen kirjauskansiomerkinnän **Voimaantulopäivä** ja **Kirjauspäivämäärä**.</span><span class="sxs-lookup"><span data-stu-id="521c1-149">In the dialog box that appears, set the **Effective date** and **Posting date** fields for the termination journal entry.</span></span>
3. <span data-ttu-id="521c1-150">Valitse **Irtisanomisehdotus** ehdottaaksesi vuokraa päättämistä varten.</span><span class="sxs-lookup"><span data-stu-id="521c1-150">Select **Termination proposal** to propose the lease for termination.</span></span>
4. <span data-ttu-id="521c1-151">Valitse **Kirjaa vuokran päättyminen**, jos haluat kirjata vuokran päättymisen kirjauskansiomerkinnän automaattisesti.</span><span class="sxs-lookup"><span data-stu-id="521c1-151">Select **Post lease termination** to automatically post the lease termination journal entry.</span></span>
5. <span data-ttu-id="521c1-152">Valitse **Vuokran päättymiset** -sivulla sen vuokrasopimuksen vuokratunnus, jota olet ehdottanut päätettäväksi nähdäksesi päättymisrivit.</span><span class="sxs-lookup"><span data-stu-id="521c1-152">On the **Lease terminations** page, select the lease ID of the lease that you proposed for termination to view the termination lines.</span></span> <span data-ttu-id="521c1-153">Irtisanomisriveillä näkyvät ROU-käyttöomaisuuden, vuokravelan, kertyneen poiston, lykättyn vuokran (jos sovellettavissa) ja voiton tai tappion arvo, joka on tunnistettava vuokran päättymisen yhteydessä.</span><span class="sxs-lookup"><span data-stu-id="521c1-153">The termination lines show the carrying values of the ROU asset, lease liability, accumulated depreciation, deferred rent (if applicable), and gain or loss that must be recognized on the termination of the lease.</span></span>

<span data-ttu-id="521c1-154">Vuokra on nyt valmis päätettäväksi.</span><span class="sxs-lookup"><span data-stu-id="521c1-154">The lease is now ready for termination.</span></span> <span data-ttu-id="521c1-155">Vuokrakirjan **Irtisanomistila**-kentän arvoksi tulee **Valmis päätettäväksi**.</span><span class="sxs-lookup"><span data-stu-id="521c1-155">The value of the **Termination status** field for the lease book is changed to **Ready for termination**.</span></span> <span data-ttu-id="521c1-156">Tässä vaiheessa kirjauskansioon ei voi enää kirjata kirjauksia vuokraan tai muuttaa tai heikentää sitä.</span><span class="sxs-lookup"><span data-stu-id="521c1-156">At this point, you can no longer post journal entries against the lease, or adjust or impair it.</span></span> 

## <a name="process-leases-that-are-ready-for-termination"></a><span data-ttu-id="521c1-157">Käsittele vuokrat, jotka ovat valmiita päätettäväksi</span><span class="sxs-lookup"><span data-stu-id="521c1-157">Process leases that are ready for termination</span></span>

<span data-ttu-id="521c1-158">Toimi seuraavasti, kun haluat käsitellä vuokrat, jotka ovat valmiita irtisanomisen jälkeisiin työvaiheisiin ja kirjata irtisanomisen kirjauskansiomerkinnän.</span><span class="sxs-lookup"><span data-stu-id="521c1-158">To process leases that are ready for termination and post the termination journal entry, follow these steps.</span></span>

1. <span data-ttu-id="521c1-159">Valitse **Vuokran irtisanomiset**-sivulla käsiteltävä vuokrasopimus ja valitse sitten **Irtisano**.</span><span class="sxs-lookup"><span data-stu-id="521c1-159">On the **Lease terminations** page, select the lease to process, and then select **Terminate**.</span></span>
2. <span data-ttu-id="521c1-160">Valitse avautuvassa valintaikkunassa **OK**.</span><span class="sxs-lookup"><span data-stu-id="521c1-160">In the dialog box that appears, select **OK**.</span></span>

<span data-ttu-id="521c1-161">Järjestelmä kirjaa irtisanomisen kirjauskansiomerkinnän.</span><span class="sxs-lookup"><span data-stu-id="521c1-161">The system posts the termination journal entry.</span></span> <span data-ttu-id="521c1-162">Vuokrakirjan **Vuokran tila** -kentän arvoksi määritetään **Lopetettu** ja **Irtisanomisehdotuksen tila** -kentän arvoksi tulee **Valmis**.</span><span class="sxs-lookup"><span data-stu-id="521c1-162">The **Lease status** field for the lease book is set to **Terminated**, and the **Termination proposal status** field is set to **Completed**.</span></span>

## <a name="reverse-a-lease-termination"></a><span data-ttu-id="521c1-163">Vuokran päättymisen peruutus</span><span class="sxs-lookup"><span data-stu-id="521c1-163">Reverse a lease termination</span></span>

<span data-ttu-id="521c1-164">Peruuta vuokran päättymisen kirjauskansion kirjaus ja avaa vuokra, joka on päättynyt, seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="521c1-164">To reverse a lease termination journal entry and open a terminated lease, follow this step.</span></span>

- <span data-ttu-id="521c1-165">Valitse **Vuokran irtisanomiset**-sivulla palautettava vuokrasopimus ja valitse sitten **Peruuta irtisanominen**.</span><span class="sxs-lookup"><span data-stu-id="521c1-165">On the **Lease terminations** page, select the terminated lease to reverse, and then select **Reverse termination**.</span></span>

<span data-ttu-id="521c1-166">Järjestelmä peruttaa irtisanomisen kirjauskansiomerkinnän.</span><span class="sxs-lookup"><span data-stu-id="521c1-166">The system reverses the termination journal entry.</span></span> <span data-ttu-id="521c1-167">Vuokrakirjan **Vuokran tila** -kentän arvoksi määritetään **Avoin**.</span><span class="sxs-lookup"><span data-stu-id="521c1-167">The **Lease status** field for the lease book is set to **Open**.</span></span> <span data-ttu-id="521c1-168">Vuokra ei enää näy **Vuokrasopimuksen päättymiset** -sivulla, ja sitä voidaan ehdottaa uudelleen irtisanomista varten.</span><span class="sxs-lookup"><span data-stu-id="521c1-168">The lease no longer appears on the **Lease terminations** page and can be proposed again for termination.</span></span>

## <a name="example-of-a-lease-termination"></a><span data-ttu-id="521c1-169">Esimerkki vuokran päättämisestä</span><span class="sxs-lookup"><span data-stu-id="521c1-169">Example of a lease termination</span></span>

<span data-ttu-id="521c1-170">Tässä esimerkissä vuokrasopimus liittyy ei-erikoistuneeseen resurssiin, ja se ei siirrä resurssin omistajuutta tai myönnä vuokralle ottajalle resurssin osto-oikeutta.</span><span class="sxs-lookup"><span data-stu-id="521c1-170">For this example, the lease is associated with a non-specialized asset, and it doesn't transfer ownership of the asset or grant the lessee the option to purchase the asset.</span></span>

### <a name="setup"></a><span data-ttu-id="521c1-171">Luo perustiedot</span><span class="sxs-lookup"><span data-stu-id="521c1-171">Setup</span></span>

<span data-ttu-id="521c1-172">Seuraavissa taulukoissa ovat arvot, jotka on määritetty **Yleistiedot**- ja **Maksuaikataulun rivit** -välilehdille vuokrasopimuksessa, jota käytetään tässä esimerkeissä.</span><span class="sxs-lookup"><span data-stu-id="521c1-172">The following tables show the values that are set on the **General** and **Payment schedule lines** tabs for the lease that is used in this example.</span></span>

<span data-ttu-id="521c1-173">**Yleinen-välilehti**</span><span class="sxs-lookup"><span data-stu-id="521c1-173">**General tab**</span></span>

| <span data-ttu-id="521c1-174">Kenttä</span><span class="sxs-lookup"><span data-stu-id="521c1-174">Field</span></span>                      | <span data-ttu-id="521c1-175">Arvo</span><span class="sxs-lookup"><span data-stu-id="521c1-175">Value</span></span>            |
|----------------------------|------------------|
| <span data-ttu-id="521c1-176">Resurssin käypä arvo</span><span class="sxs-lookup"><span data-stu-id="521c1-176">Fair value of the asset</span></span>    | <span data-ttu-id="521c1-177">600,000</span><span class="sxs-lookup"><span data-stu-id="521c1-177">600,000</span></span>          |
| <span data-ttu-id="521c1-178">Valuutta</span><span class="sxs-lookup"><span data-stu-id="521c1-178">Currency</span></span>                   | <span data-ttu-id="521c1-179">USD</span><span class="sxs-lookup"><span data-stu-id="521c1-179">USD</span></span>              |
| <span data-ttu-id="521c1-180">Alkuvaiheen välittömät menot</span><span class="sxs-lookup"><span data-stu-id="521c1-180">Initial direct costs</span></span>       | <span data-ttu-id="521c1-181">1 000</span><span class="sxs-lookup"><span data-stu-id="521c1-181">1,000</span></span>            |
| <span data-ttu-id="521c1-182">Inkrementaalinen lainakorko</span><span class="sxs-lookup"><span data-stu-id="521c1-182">Incremental borrowing rate</span></span> | <span data-ttu-id="521c1-183">7 %</span><span class="sxs-lookup"><span data-stu-id="521c1-183">7%</span></span>               |
| <span data-ttu-id="521c1-184">Yhdistämisväli</span><span class="sxs-lookup"><span data-stu-id="521c1-184">Compounding interval</span></span>       | <span data-ttu-id="521c1-185">Vuosittain</span><span class="sxs-lookup"><span data-stu-id="521c1-185">Annually</span></span>         |
| <span data-ttu-id="521c1-186">Käyttöomaisuuden käyttöikä (kuukautta)</span><span class="sxs-lookup"><span data-stu-id="521c1-186">Asset useful life (months)</span></span> | <span data-ttu-id="521c1-187">600</span><span class="sxs-lookup"><span data-stu-id="521c1-187">600</span></span>              |
| <span data-ttu-id="521c1-188">Annuiteetin tyyppi</span><span class="sxs-lookup"><span data-stu-id="521c1-188">Annuity type</span></span>               | <span data-ttu-id="521c1-189">Tavallinen annuiteetti</span><span class="sxs-lookup"><span data-stu-id="521c1-189">Ordinary annuity</span></span> |
| <span data-ttu-id="521c1-190">Aloituspäivämäärä</span><span class="sxs-lookup"><span data-stu-id="521c1-190">Commencement date</span></span>          | <span data-ttu-id="521c1-191">1.1.2019</span><span class="sxs-lookup"><span data-stu-id="521c1-191">1/1/2019</span></span>         |

<span data-ttu-id="521c1-192">**Maksusuunnitelmarivit-välilehti**</span><span class="sxs-lookup"><span data-stu-id="521c1-192">**Payment schedule lines tab**</span></span>

| <span data-ttu-id="521c1-193">Kenttä</span><span class="sxs-lookup"><span data-stu-id="521c1-193">Field</span></span>             | <span data-ttu-id="521c1-194">Arvo</span><span class="sxs-lookup"><span data-stu-id="521c1-194">Value</span></span>      |
|-------------------|------------|
| <span data-ttu-id="521c1-195">Aloituspäivä</span><span class="sxs-lookup"><span data-stu-id="521c1-195">Start date</span></span>        | <span data-ttu-id="521c1-196">1.1.2019</span><span class="sxs-lookup"><span data-stu-id="521c1-196">1/1/2019</span></span>   |
| <span data-ttu-id="521c1-197">Kausiväli</span><span class="sxs-lookup"><span data-stu-id="521c1-197">Period interval</span></span>   | <span data-ttu-id="521c1-198">Kuukausittain</span><span class="sxs-lookup"><span data-stu-id="521c1-198">Monthly</span></span>    |
| <span data-ttu-id="521c1-199">Kaudet</span><span class="sxs-lookup"><span data-stu-id="521c1-199">Periods</span></span>           | <span data-ttu-id="521c1-200">120</span><span class="sxs-lookup"><span data-stu-id="521c1-200">120</span></span>        |
| <span data-ttu-id="521c1-201">Päättymispäivämäärä</span><span class="sxs-lookup"><span data-stu-id="521c1-201">End date</span></span>          | <span data-ttu-id="521c1-202">31.12.2028</span><span class="sxs-lookup"><span data-stu-id="521c1-202">12/31/2028</span></span> |
| <span data-ttu-id="521c1-203">Maksun toistuvuus</span><span class="sxs-lookup"><span data-stu-id="521c1-203">Payment frequency</span></span> | <span data-ttu-id="521c1-204">Vuosittain</span><span class="sxs-lookup"><span data-stu-id="521c1-204">Annually</span></span>   |
| <span data-ttu-id="521c1-205">Maksun summa</span><span class="sxs-lookup"><span data-stu-id="521c1-205">Payment amount</span></span>    | <span data-ttu-id="521c1-206">10,000</span><span class="sxs-lookup"><span data-stu-id="521c1-206">10,000</span></span>     |

### <a name="steps-for-terminating-the-lease"></a><span data-ttu-id="521c1-207">Vuokran päättämisen vaiheet</span><span class="sxs-lookup"><span data-stu-id="521c1-207">Steps for terminating the lease</span></span>

1. <span data-ttu-id="521c1-208">Kun olet luonut vuokrasopimuksen aiemmin tässä ohjeaiheessa kuvatulla tavalla, siirry vuokrauskirjaan ja vahvista maksuaikataulu.</span><span class="sxs-lookup"><span data-stu-id="521c1-208">After you create the lease as described earlier in this topic, go to the lease book, and confirm the payment schedule.</span></span> <span data-ttu-id="521c1-209">Kirjaa sitten alkuperäinen tuloutuksen kirjauskansiovienti.</span><span class="sxs-lookup"><span data-stu-id="521c1-209">Then post the initial recognition journal entry.</span></span> <span data-ttu-id="521c1-210">Alkuperäinen käyttöoikeusomaisuuserä on 71 235,81 $ ja vuokrasopimusvelan on oltava 70 235,81 $.</span><span class="sxs-lookup"><span data-stu-id="521c1-210">The initial ROU asset is $71,235.81, and lease liability should be $70,235.81.</span></span> <span data-ttu-id="521c1-211">Tässä esimerkissä vuokrasopimus luokiteltiin käyttöleasingsopimukseksi Accounting Standards Codification Topic 842:n (ASC 842) mukaan.</span><span class="sxs-lookup"><span data-stu-id="521c1-211">For this example, the lease was classified as an operating lease under Accounting Standards Codification Topic 842 (ASC 842).</span></span>
2. <span data-ttu-id="521c1-212">Suorita kirjauskansion eräprosessi kolme kertaa, jotta voit simuloida kolmen vuoden kulumista vuokrille, korkokuluille ja poistokuluille.</span><span class="sxs-lookup"><span data-stu-id="521c1-212">Run the batch journal process three times to simulate the passage of three years for the lease payments, interest expenses, and depreciation expenses.</span></span>
3. <span data-ttu-id="521c1-213">Kun kaikki kolme erätyötä on suoritettu, siirry takaisin vuokrauskirjaan ja avaa velka- ja resurssitapahtumien taulukot tarkastellaksesi resurssin ja vuokrasopimusvelan nykyistä kirjanpitoarvoa.</span><span class="sxs-lookup"><span data-stu-id="521c1-213">After you've finished running all three batch jobs, go back to the lease book, and open the Liability and Asset transactions tables to view the current carrying value of the ROU asset and lease liability.</span></span> <span data-ttu-id="521c1-214">Kolmen vuoden kuluttua velan arvon on oltava noin -53 893,00 dollaria ja resurssin arvon noin 54 593,00 dollaria.</span><span class="sxs-lookup"><span data-stu-id="521c1-214">After three years, the value of the liability should be approximately $-53,893.00, and the value of the asset should be approximately $54,593.00.</span></span>

    <span data-ttu-id="521c1-215">Kun nämä kolme vuotta ovat kuluneet, liike ja vuokraaja ovat sopineet, että vuokra päättyy.</span><span class="sxs-lookup"><span data-stu-id="521c1-215">After the three years have passed, the business and lessor mutually agree to terminate the lease.</span></span> <span data-ttu-id="521c1-216">Sinun on näin ollen päätettävä vuokra.</span><span class="sxs-lookup"><span data-stu-id="521c1-216">Therefore, you must now terminate the lease.</span></span>

4. <span data-ttu-id="521c1-217">Siirry vuokraan, joka on lopetettava, ja valitse sitten toimintoruudusta **Irtisanomisehdotus**.</span><span class="sxs-lookup"><span data-stu-id="521c1-217">Go to the lease that must be terminated, and then, on the Action Pane, select **Termination proposal**.</span></span> 
5. <span data-ttu-id="521c1-218">Kirjoita näyttöön tulevaan valintaikkunaan **Voimaantulopäivämäärä**- ja **Kirjauspäivämäärä**-kenttiin **1.1.2021**.</span><span class="sxs-lookup"><span data-stu-id="521c1-218">In the dialog box that appears, in the **Effective date** and **Posting date** field, enter **1/1/2021**.</span></span>
6. <span data-ttu-id="521c1-219">Valitse **Irtisanomisehdotus** ehdottaaksesi vuokraa päättämistä varten.</span><span class="sxs-lookup"><span data-stu-id="521c1-219">Select **Termination proposal** to propose the lease for termination.</span></span>

    <span data-ttu-id="521c1-220">Näkyviin tulee **Vuokrasopimuksen päättymiset** -sivu, joka sisältää irtisanottavan vuokran.</span><span class="sxs-lookup"><span data-stu-id="521c1-220">The **Lease terminations** page appears and shows the lease that will be terminated.</span></span>

7. <span data-ttu-id="521c1-221">Voit tarkastella päättymisrivejä valitsemalla vuokrasopimuksen vuokratunnuksen, jota olet ehdottanut päätettäväksi.</span><span class="sxs-lookup"><span data-stu-id="521c1-221">To view the termination lines, select the lease ID of the lease that you proposed for termination.</span></span> <span data-ttu-id="521c1-222">Irtisanomisriveillä näkyvät vuokran kirjanpitoarvot.</span><span class="sxs-lookup"><span data-stu-id="521c1-222">The termination lines show the carrying values of the lease.</span></span> <span data-ttu-id="521c1-223">Seuraavassa taulukossa on esitetty, mitä näiden arvojen pitäisi olla tässä esimerkissä.</span><span class="sxs-lookup"><span data-stu-id="521c1-223">The following table shows what these values should be for this example.</span></span> 

    | <span data-ttu-id="521c1-224">Kenttä</span><span class="sxs-lookup"><span data-stu-id="521c1-224">Field</span></span>                                                 | <span data-ttu-id="521c1-225">Arvo</span><span class="sxs-lookup"><span data-stu-id="521c1-225">Value</span></span>      |
    |-------------------------------------------------------|------------|
    | <span data-ttu-id="521c1-226">Sopimusvelan kirjanpidon saldo tapahtumavaluuttana</span><span class="sxs-lookup"><span data-stu-id="521c1-226">Carrying balance of liability in transaction currency</span></span> | <span data-ttu-id="521c1-227">53 892,89 $</span><span class="sxs-lookup"><span data-stu-id="521c1-227">$53,892.89</span></span> |
    | <span data-ttu-id="521c1-228">Käyttöoikeusomaisuuserä tapahtumavaluuttana</span><span class="sxs-lookup"><span data-stu-id="521c1-228">Right-of-use asset in transaction currency</span></span>            | <span data-ttu-id="521c1-229">71 235,81 $</span><span class="sxs-lookup"><span data-stu-id="521c1-229">$71,235.81</span></span> |
    | <span data-ttu-id="521c1-230">Kertynyt poisto tapahtumavaluuttana</span><span class="sxs-lookup"><span data-stu-id="521c1-230">Accumulated depreciation in transaction currency</span></span>      | <span data-ttu-id="521c1-231">16 642,92 $</span><span class="sxs-lookup"><span data-stu-id="521c1-231">$16,642.92</span></span> |
    | <span data-ttu-id="521c1-232">Voitto/tappio tapahtumavaluuttana</span><span class="sxs-lookup"><span data-stu-id="521c1-232">Gain (loss) in transaction currency</span></span>                   | <span data-ttu-id="521c1-233">-700,00 $</span><span class="sxs-lookup"><span data-stu-id="521c1-233">$-700.00</span></span>   |

8. <span data-ttu-id="521c1-234">Voit kirjata päättymisen kirjauskansiomerkinnän valitsemalla **Vuokran irtisanomiset**-sivulla vuokrasopimuksen ja valitsemalla sitten **Irtisano**.</span><span class="sxs-lookup"><span data-stu-id="521c1-234">To post the termination journal entry, select the lease on the **Lease terminations** page, and then select **Terminate**.</span></span>
9. <span data-ttu-id="521c1-235">Valitse avautuvassa valintaikkunassa **OK**.</span><span class="sxs-lookup"><span data-stu-id="521c1-235">In the dialog box that appears, select **OK**.</span></span>
10. <span data-ttu-id="521c1-236">Jos haluat tarkastella luotua ja kirjattua irtisanomiskirjauskansiota, siirry käyttöomaisuuserän vuokrakirjauskansioon vuokrakirjassa.</span><span class="sxs-lookup"><span data-stu-id="521c1-236">To view the termination journal entry that has been created and posted, go to the asset's leasing journal in the lease book.</span></span> <span data-ttu-id="521c1-237">Seuraavassa taulukossa on esitetty, miltä tämän tapahtuman pitäisi olla tässä esimerkissä.</span><span class="sxs-lookup"><span data-stu-id="521c1-237">The following table shows what this entry should look like for this example.</span></span>

    | <span data-ttu-id="521c1-238">Tapahtuma</span><span class="sxs-lookup"><span data-stu-id="521c1-238">Transaction</span></span>                           | <span data-ttu-id="521c1-239">Debet (Dr.)</span><span class="sxs-lookup"><span data-stu-id="521c1-239">Debit (Dr.)</span></span> | <span data-ttu-id="521c1-240">Kredit (Cr.)</span><span class="sxs-lookup"><span data-stu-id="521c1-240">Credit (Cr.)</span></span> |
    |---------------------------------------|-------------|--------------|
    | <span data-ttu-id="521c1-241">Dr. Vuokrasopimusvelka</span><span class="sxs-lookup"><span data-stu-id="521c1-241">Dr. Lease liability</span></span>                   | <span data-ttu-id="521c1-242">53,892.89</span><span class="sxs-lookup"><span data-stu-id="521c1-242">53,892.89</span></span>   |              |
    | <span data-ttu-id="521c1-243">Dr. kertynyt poisto</span><span class="sxs-lookup"><span data-stu-id="521c1-243">Dr. Accumulated depreciation</span></span>          | <span data-ttu-id="521c1-244">16,642.92</span><span class="sxs-lookup"><span data-stu-id="521c1-244">16,642.92</span></span>   |              |
    | <span data-ttu-id="521c1-245">Dr. Vuokranmuokkauksen voitto/tappio</span><span class="sxs-lookup"><span data-stu-id="521c1-245">Dr. Gain (loss) on lease modification</span></span> | <span data-ttu-id="521c1-246">700.00</span><span class="sxs-lookup"><span data-stu-id="521c1-246">700.00</span></span>      |              |
    | <span data-ttu-id="521c1-247">Cr. Vuokraresurssi</span><span class="sxs-lookup"><span data-stu-id="521c1-247">Cr. Lease asset</span></span>                       |             | <span data-ttu-id="521c1-248">71,235.81</span><span class="sxs-lookup"><span data-stu-id="521c1-248">71,235.81</span></span>    |

11. <span data-ttu-id="521c1-249">Avaa velka- ja käyttöomaisuustapahtumataulut, jos haluat tarkastella irtisanomisen nettovaikutusta, jossa ROU-käyttöomaisuus ja vuokravelka ovat 0 (nolla).</span><span class="sxs-lookup"><span data-stu-id="521c1-249">To view the net effect of the termination, where the ROU asset and lease liability will be 0 (zero), open the Liability and Asset transactions tables.</span></span>

<span data-ttu-id="521c1-250">Vuokraustilan olisi nyt oltava **Irtisanottu**.</span><span class="sxs-lookup"><span data-stu-id="521c1-250">The lease status should now be **Terminated**.</span></span> <span data-ttu-id="521c1-251">Tähän vuokraan ei kirjata muita kirjauskansiomerkintöjä, ellei irtisanomista peruta.</span><span class="sxs-lookup"><span data-stu-id="521c1-251">No additional journal entries will be posted against this lease unless the termination is reversed.</span></span>