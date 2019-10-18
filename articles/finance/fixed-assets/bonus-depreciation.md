---
title: Bonuspoisto
description: Tämä artikkeli sisältää bonuspoiston toimintojen yleiskatsauksen.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetBonus
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 3621
ms.assetid: 835ec594-744e-461c-a676-1b9abc094173
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 687ba57042ad65d3a1ff4ad92f0da774c6751eac
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/27/2019
ms.locfileid: "2187380"
---
# <a name="bonus-depreciation"></a><span data-ttu-id="2e646-103">Bonuspoisto</span><span class="sxs-lookup"><span data-stu-id="2e646-103">Bonus depreciation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2e646-104">Tämä artikkeli sisältää bonuspoiston toimintojen yleiskatsauksen.</span><span class="sxs-lookup"><span data-stu-id="2e646-104">This article provides an overview of the bonus depreciation functionality.</span></span>

<span data-ttu-id="2e646-105">Bonuspoisto mahdollistaa ylimääräiset poistosummat sinä vuonna, jolloin käyttöomaisuus otetaan käyttöön ja siitä tehdään poisto ensimmäistä kertaa.</span><span class="sxs-lookup"><span data-stu-id="2e646-105">For bonus depreciation, you can take extra or bonus depreciation amounts during the first year that the asset is put in service and depreciated.</span></span> <span data-ttu-id="2e646-106">Bonuspoisto on suoritettava ennen muiden poistojen laskemista.</span><span class="sxs-lookup"><span data-stu-id="2e646-106">Bonus depreciation must be taken before any other depreciation calculations.</span></span> <span data-ttu-id="2e646-107">Näin kannattaa käyttää bonuspoistoa kirjoissa, joissa Kirjaa kirjanpitoon -toiminto on poistettu käytöstä.</span><span class="sxs-lookup"><span data-stu-id="2e646-107">Therefore, it's best to use bonus depreciation with books where the Post to general ledger functionality is disabled.</span></span> <span data-ttu-id="2e646-108">Voit käyttää **Poista kirjanpitoon kirjaamattomat tapahtumat** ja poistaa aiempia tapahtumia kirjoista, joita ei kirjata kirjanpitoon.</span><span class="sxs-lookup"><span data-stu-id="2e646-108">You can use the **Delete transactions not posted to general ledger** option to delete historical transactions for books that don't post to the general ledger.</span></span> <span data-ttu-id="2e646-109">Bonuspoisto voidaan sisällyttää myöhemmin käyttöomaisuuserän elinkaareen poistamalla aiemmin kirjattuja poistotapahtumia.</span><span class="sxs-lookup"><span data-stu-id="2e646-109">You can then accommodate bonus depreciation later in the asset life cycle by deleting depreciation transactions that were previously posted.</span></span> 

<span data-ttu-id="2e646-110">Bonuspoisto voidaan laskea ehdotusprosessia käyttäen tai luomalla manuaalisia bonuspoistotapahtumia.</span><span class="sxs-lookup"><span data-stu-id="2e646-110">You can calculate bonus depreciation by using the proposal process, or you can create manual bonus depreciation transactions.</span></span> <span data-ttu-id="2e646-111">Bonuspoistotapahtumia ei voi luoda, jos kyseisessä käyttöomaisuuskirjassa on jo poistotapahtumia tai poistojen oikaisutapahtumia.</span><span class="sxs-lookup"><span data-stu-id="2e646-111">You can't create bonus depreciation transactions if depreciation transactions or depreciation adjustment transactions exist for that asset book.</span></span>

<span data-ttu-id="2e646-112">Kun lasket bonuspoiston ehdotusprosessin avulla, kaikki olemassa olevat bonustapahtumat sisältyvät perustan laskentaan.</span><span class="sxs-lookup"><span data-stu-id="2e646-112">When you use the proposal process to calculate bonus depreciation, all existing bonus transactions are included in the calculation of the basis.</span></span> <span data-ttu-id="2e646-113">Laskenta sisältää myös aiemmat käyttöomaisuudelle manuaalisesti kirjatut bonuspoistot.</span><span class="sxs-lookup"><span data-stu-id="2e646-113">The calculation also includes any previous bonus depreciations that you manually entered for the asset.</span></span> 

<span data-ttu-id="2e646-114">Jos käyttöomaisuuserälle tehdään useita bonuspoistoja, myös prioriteetti otetaan huomioon.</span><span class="sxs-lookup"><span data-stu-id="2e646-114">If more than one bonus depreciation will be taken for an asset, the priority is considered.</span></span> <span data-ttu-id="2e646-115">Jokainen bonus vähentää seuraavan bonuksen perustaa.</span><span class="sxs-lookup"><span data-stu-id="2e646-115">Each bonus reduces the asset basis for the next bonus.</span></span> <span data-ttu-id="2e646-116">Bonuspoiston laskennassa käytetyssä käyttöomaisuuden perustassa ei oteta huomioon jäännösarvoa eikä bonuspoistoon sovelleta poistomenetelmää.</span><span class="sxs-lookup"><span data-stu-id="2e646-116">Salvage value isn't considered in the asset basis for bonus depreciation calculations, and the depreciation convention doesn't apply for bonus depreciation.</span></span> 

<span data-ttu-id="2e646-117">Yhdysvalloissa jotkut omaisuustyypit voidaan katsoa tällä hetkellä Section 179 -omaisuudeksi.</span><span class="sxs-lookup"><span data-stu-id="2e646-117">Currently, in the United States, some property qualifies as Section 179 property.</span></span> <span data-ttu-id="2e646-118">Section 179 -vähennystä käyttämällä omaisuuden koko tai osittainen arvo voidaan saada takaisin tiettyyn rajaan asti.</span><span class="sxs-lookup"><span data-stu-id="2e646-118">By using the Section 179 deduction, you can recover all or part of the cost of some property, up to a limit.</span></span> <span data-ttu-id="2e646-119">Arvon voi saada takaisin vähentämällä se sinä vuonna, jolloin omaisuus otettiin käyttöön.</span><span class="sxs-lookup"><span data-stu-id="2e646-119">You can recover the cost by deducting it in the year when you put the property in service.</span></span>

## <a name="example"></a><span data-ttu-id="2e646-120">Esimerkki</span><span class="sxs-lookup"><span data-stu-id="2e646-120">Example</span></span>
<span data-ttu-id="2e646-121">Oletetaan, että käyttöomaisuuden poistokirjaan liittyvät seuraavat bonuspoistot:</span><span class="sxs-lookup"><span data-stu-id="2e646-121">The following bonus depreciations are associated with an asset book:</span></span>

-   <span data-ttu-id="2e646-122">**Osa 179:** 1 000,00, Prioriteetti 1</span><span class="sxs-lookup"><span data-stu-id="2e646-122">**Section 179:** 1,000.00, Priority 1</span></span>
-   <span data-ttu-id="2e646-123">**Liberty Zone-poisto:** 30 prosenttia, prioriteetti 2</span><span class="sxs-lookup"><span data-stu-id="2e646-123">**Liberty Zone:** 30 percent, Priority 2</span></span>

<span data-ttu-id="2e646-124">Omaisuuden hankintahinta on 5 000.</span><span class="sxs-lookup"><span data-stu-id="2e646-124">The asset acquisition cost is 5,000.00.</span></span> <span data-ttu-id="2e646-125">Kun bonuspoisto lasketaan, ensimmäinen bonuspoistosumma on Osa 179 -poisto 1 000.</span><span class="sxs-lookup"><span data-stu-id="2e646-125">When bonus depreciation is calculated, the first bonus depreciation amount is 1,000.00 for the Section 179 depreciation.</span></span> 

<span data-ttu-id="2e646-126">Seuraava bonuspoistosumma, Liberty Zone -poisto, lasketaan seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="2e646-126">The next bonus depreciation amount, for the Liberty Zone depreciation, is calculated as follows:</span></span> 

<span data-ttu-id="2e646-127">Hankintahinta - 1 000 (Osa 179 -poisto) x 30 % = 1 200</span><span class="sxs-lookup"><span data-stu-id="2e646-127">Acquisition cost – 1,000 (Section 179 depreciation) × 30 percent = 1,200</span></span> 

<span data-ttu-id="2e646-128">Jos bonuspoistosumma on suurempi kuin jäljelle jäävä hankintahinta, bonuspoistosummaksi tulee joko laskettu bonuspoiston tulos tai jäljelle jäävä hankintahinta sen mukaan, kumpi summa on pienempi.</span><span class="sxs-lookup"><span data-stu-id="2e646-128">If the bonus depreciation amount is more than the remaining acquisition cost, the bonus depreciation amount is either the result of the bonus depreciation calculation or the remaining acquisition cost, whichever amount is less.</span></span> 

<span data-ttu-id="2e646-129">Jos jäljelle jäävä hankintahinta on 0 (nolla) tai pienempi, bonuspoistotapahtumia ei luoda.</span><span class="sxs-lookup"><span data-stu-id="2e646-129">If the remaining acquisition cost is 0 (zero) or less, bonus depreciation transactions isn't generated.</span></span> 

<span data-ttu-id="2e646-130">Kun bonuspoisto lasketaan ehdotusprosessia käyttäen, luodaan kaikille poistokirjaan kuuluville soveltuville bonuspoistotietueille bonuspoistotapahtuma.</span><span class="sxs-lookup"><span data-stu-id="2e646-130">When bonus depreciation is calculated by using the proposal process, a bonus depreciation transaction is created for all applicable bonus depreciation records that are associated with the asset book.</span></span> 

<span data-ttu-id="2e646-131">Bonuspoistotietueita voidaan luoda rajaton määrä.</span><span class="sxs-lookup"><span data-stu-id="2e646-131">You can create an unlimited number of bonus depreciation records.</span></span> <span data-ttu-id="2e646-132">Kun tietueet on määritetty käyttöomaisuusryhmän kirjaan, niitä käytetään käyttöomaisuuserän poistokirjassa.</span><span class="sxs-lookup"><span data-stu-id="2e646-132">After you assign those records to the asset group book, they are applied to the asset book.</span></span> 

<span data-ttu-id="2e646-133">Bonuspoisto ilmoitetaan joko prosenttina tai kiinteänä summana.</span><span class="sxs-lookup"><span data-stu-id="2e646-133">Bonus depreciation is entered as either a percentage or a fixed amount.</span></span> <span data-ttu-id="2e646-134">Kun kirjataan poistoehdotuksia, bonuspoistotapahtumat kirjataan kirjaan poistotapahtumista erillisinä tapahtumina.</span><span class="sxs-lookup"><span data-stu-id="2e646-134">When you post depreciation proposals, bonus depreciation transactions are posted to the book as separate transactions from the depreciation transactions.</span></span>


