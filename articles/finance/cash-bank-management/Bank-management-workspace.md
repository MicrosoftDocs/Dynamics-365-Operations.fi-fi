---
title: Maksuliikenteen työtila
description: Tässä ohjeaiheessa on tietoja maksuliikenteen työtilasta. Työtilassa on näkyvillä yrityksen pankkitileihin liittyviä tietoja. Siinä on myös yhteenvetonäkymä ja analytiikkasivu. Yhteenvetonäkymässä on yhteenvetoruudut, pankkitilitiedot, saldokaavio ja liittyvät tiedot. Analytiikkasivu näyttää Microsoft Power BI:n ominaisuuksien avulla pankkitilin saldoihin liittyviä visuaalisia tietoja.
author: saraschi2
manager: AnnBe
ms.date: 01/12/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BankTreasurerWorkspace
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: 4b7d2da346880278f684a796f2d649e7da52b647
ms.sourcegitcommit: 7592c2dec0428d56843ab395d2a52c89f77f99b5
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/22/2020
ms.locfileid: "4097183"
---
# <a name="bank-management-workspace"></a><span data-ttu-id="697b9-106">Maksuliikenteen työtila</span><span class="sxs-lookup"><span data-stu-id="697b9-106">Bank management workspace</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="697b9-107">**Maksuliikenne** -työtilassa on yrityksen pankkitileihin liittyviä tietoja.</span><span class="sxs-lookup"><span data-stu-id="697b9-107">The **Bank management** workspace shows information that is related to company bank accounts.</span></span> <span data-ttu-id="697b9-108">Työtilassa on **Yhteenveto** -näkymä ja **Analytiikka** -sivu.</span><span class="sxs-lookup"><span data-stu-id="697b9-108">This workspace includes a **Summary** view and an **Analytics** page.</span></span> <span data-ttu-id="697b9-109">**Yhteenveto** -näkymässä on yhteenvetoruudut, pankkitilitiedot, saldokaavio ja liittyvät tiedot.</span><span class="sxs-lookup"><span data-stu-id="697b9-109">The **Summary** view shows summary tiles, bank account information, a balance chart, and related information.</span></span> <span data-ttu-id="697b9-110">**Analytiikka** -sivu näyttää Microsoft Power BI:n ominaisuuksien avulla pankkitilin saldoihin liittyviä visuaalisia tietoja.</span><span class="sxs-lookup"><span data-stu-id="697b9-110">The **Analytics** page uses the capabilities of Microsoft Power BI to show visuals that are related to bank account balances.</span></span>

## <a name="summary-view"></a><span data-ttu-id="697b9-111">Yhteenvetonäkymä</span><span class="sxs-lookup"><span data-stu-id="697b9-111">Summary view</span></span>

### <a name="summary"></a><span data-ttu-id="697b9-112">Yhteenveto</span><span class="sxs-lookup"><span data-stu-id="697b9-112">Summary</span></span>

<span data-ttu-id="697b9-113">**Yhteenveto** -osan ruuduissa on pankkitilien yleiskatsaus, Siitä voi myös siirtyä nopeasti eniten käytetyille sivuille.</span><span class="sxs-lookup"><span data-stu-id="697b9-113">The tiles in the **Summary** section give an overview of your bank accounts and provide quick access to the pages that you most often have to use.</span></span> <span data-ttu-id="697b9-114">Pankkitilin täsmäytystiedot koskevat Pankkitilin täsmäytyksen lisätoiminnot -toimintoa.</span><span class="sxs-lookup"><span data-stu-id="697b9-114">The bank reconciliation information is specific to the Advanced bank reconciliation functionality.</span></span> <span data-ttu-id="697b9-115">Tiedot koskevat vain niitä pankkitilejä, joiden **Pankkitilin täsmäytyksen lisätoiminnot** -asetukseksi on valittu **Kyllä** **Pankkitili** -sivulla.</span><span class="sxs-lookup"><span data-stu-id="697b9-115">Information is included only for those bank accounts that have the **Advanced bank reconciliation** option set to **Yes** on the **Bank account** page.</span></span> <span data-ttu-id="697b9-116">Voit tuoda **Yhteenveto** -osiossa kaikkien yritysten pankkitilien pankkitiedostoja.</span><span class="sxs-lookup"><span data-stu-id="697b9-116">From the **Summary** section, you can import electronic bank files for bank accounts across all legal entities.</span></span>

### <a name="bank-accounts"></a><span data-ttu-id="697b9-117">Pankkitilit</span><span class="sxs-lookup"><span data-stu-id="697b9-117">Bank accounts</span></span>

<span data-ttu-id="697b9-118">Kutakin yrityksen pankkitiliä vastaa **Pankkitilit** -osion kortti.</span><span class="sxs-lookup"><span data-stu-id="697b9-118">Each bank account in the legal entity is represented by a card in the **Bank accounts** section.</span></span> <span data-ttu-id="697b9-119">Näkyvissä on nykyinen saldo. Lisäksi kyseisen yhteenvedon saldosumman tapahtumiin voi porautua.</span><span class="sxs-lookup"><span data-stu-id="697b9-119">The current balance is shown, and you can drill down to the transactions that make up that summary balance amount.</span></span> <span data-ttu-id="697b9-120">Myös **Välitilitapahtumat** -summassa voi porautua kyseisen yhteenvetosumman tapahtumiin.</span><span class="sxs-lookup"><span data-stu-id="697b9-120">The **Bridged transactions** amount also lets you drill down to the transactions that make up that summary amount.</span></span> <span data-ttu-id="697b9-121">Välitilitapahtumat ovat odottavia tapahtumia, jotka on kirjattu välitiliöintitoiminnolla mutta joita ei ole vielä selvitetty.</span><span class="sxs-lookup"><span data-stu-id="697b9-121">Bridged transactions are any pending transactions that have been posted by using bridging functionality, but that haven't yet been cleared.</span></span> <span data-ttu-id="697b9-122">**Odottava saldo** -summa on nykyinen saldo, josta on vähennetty välitiliöidyt eli odottavat tapahtumat.</span><span class="sxs-lookup"><span data-stu-id="697b9-122">The **Pending balance** amount is the current balance minus the bridged, or pending, transactions.</span></span>

<span data-ttu-id="697b9-123">Kortista näkee myös, milloin pankkitili täsmäytettiin viimeksi.</span><span class="sxs-lookup"><span data-stu-id="697b9-123">The card also shows when the bank account was last reconciled.</span></span> <span data-ttu-id="697b9-124">Nämä tiedot näkyvät vain, jos pankkitilissä on otettu käyttöön Pankkitilin täsmäytyksen lisätoiminnot.</span><span class="sxs-lookup"><span data-stu-id="697b9-124">This information is shown only if Advanced bank reconciliation is enabled for the bank account.</span></span>

### <a name="balance"></a><span data-ttu-id="697b9-125">Tase</span><span class="sxs-lookup"><span data-stu-id="697b9-125">Balance</span></span>

<span data-ttu-id="697b9-126">**Saldo** -kaaviossa on näkyvissä joko **Pankkitilit** -osiossa valitun tilin historialliset saldotiedot tai yrityksen kaikkien pankkitilien historiallisten saldotietojen yhteenveto.</span><span class="sxs-lookup"><span data-stu-id="697b9-126">The **Balance** chart shows either historic balance information for the bank account that is selected in the **Bank accounts** section or a summary of historic balance information for all bank accounts in the legal entity.</span></span> <span data-ttu-id="697b9-127">Nämä tiedot ovat saatavilla eripituisille jaksoille: kuluva viikko, kuluva kuukausi, kuluva vuosi, viimeiset viisi vuotta ja kaikki kaudet (pankkitilin koko historia).</span><span class="sxs-lookup"><span data-stu-id="697b9-127">This information is available for various periods: the current week, the current month, the current year, the last five years, and all periods (the full history of the bank account).</span></span> 

<span data-ttu-id="697b9-128">Jos tarkastelet yksittäisen pankkitilin **Saldo** -kaaviota, historialliset saldot näytetään pankkitilin valuuttana.</span><span class="sxs-lookup"><span data-stu-id="697b9-128">If you're viewing the **Balance** chart for a single bank account, the historic balances are shown in the bank account currency.</span></span> <span data-ttu-id="697b9-129">Jos tarkastelet yrityksen kaikkien pankkitilin kaaviota, historialliset saldot näytetään kirjapitovaluuttana.</span><span class="sxs-lookup"><span data-stu-id="697b9-129">If you're viewing the chart for all bank accounts in the legal entity, the historic balances are shown in the accounting currency.</span></span>

<span data-ttu-id="697b9-130">Kaavion yläreunasta voi tarkistaa, milloin tiedot on viimeksi päivitetty.</span><span class="sxs-lookup"><span data-stu-id="697b9-130">Information about when the data was last updated appears at the top of the chart.</span></span> <span data-ttu-id="697b9-131">Voit päivittää tietoja tarpeen mukaan:</span><span class="sxs-lookup"><span data-stu-id="697b9-131">You can update the data as you require.</span></span>

### <a name="related-information"></a><span data-ttu-id="697b9-132">Aiheeseen liittyviä tietoja</span><span class="sxs-lookup"><span data-stu-id="697b9-132">Related information</span></span>

<span data-ttu-id="697b9-133">Voit viimeistellä pankkisiirrot avaamalla **Liittyvät tiedot** -osiossa **Kirjauskansio** -sivun.</span><span class="sxs-lookup"><span data-stu-id="697b9-133">From the **Related information** section, you can open the **General journal** page to complete bank transfers.</span></span> <span data-ttu-id="697b9-134">Voit avata myös **Pankkitapahtumat** - ja **Välitilitapahtumat** -sivut nopeasti.</span><span class="sxs-lookup"><span data-stu-id="697b9-134">You can also quickly open the **Bank transactions** and **Bridged transactions** pages.</span></span>

## <a name="analytics-view"></a><span data-ttu-id="697b9-135">Analytiikkanäkymä</span><span class="sxs-lookup"><span data-stu-id="697b9-135">Analytics view</span></span>

<span data-ttu-id="697b9-136">**Analytiikka** -sivulla on tärkeitä valitun yrityksen pankkitilien mittareita.</span><span class="sxs-lookup"><span data-stu-id="697b9-136">The **Analytics** page provides important metrics about the bank accounts in the current company.</span></span> <span data-ttu-id="697b9-137">Sivulla on seuraavat visualisoinnit:</span><span class="sxs-lookup"><span data-stu-id="697b9-137">The following visualizations are available on the page:</span></span>

-   <span data-ttu-id="697b9-138">Pankkitilin kokonaissaldo järjestelmän valuuttana</span><span class="sxs-lookup"><span data-stu-id="697b9-138">Total bank balance in system currency</span></span>
-   <span data-ttu-id="697b9-139">Saldo yrityksen mukaan</span><span class="sxs-lookup"><span data-stu-id="697b9-139">Balance by legal entity</span></span>
-   <span data-ttu-id="697b9-140">Kuluvan päivän toteutuneen ja ennustetun saldon vertailu pankkitilin valuuttana</span><span class="sxs-lookup"><span data-stu-id="697b9-140">Today’s actual vs forecasted balance in bank account currency</span></span>
-   <span data-ttu-id="697b9-141">Saldo pankkitilin mukaan</span><span class="sxs-lookup"><span data-stu-id="697b9-141">Balance by bank account</span></span>
-   <span data-ttu-id="697b9-142">Saldo valuutan mukaan</span><span class="sxs-lookup"><span data-stu-id="697b9-142">Balance by currency</span></span>

<span data-ttu-id="697b9-143">Voit tarkastella kaikkien yritysten pankkitietojen analytiikkaa **Kassayhteenveto – kaikki yritykset** -työtilassa.</span><span class="sxs-lookup"><span data-stu-id="697b9-143">You can view bank analytics across all companies from the **Cash overview – all companies** workspace.</span></span> <span data-ttu-id="697b9-144">Lisätietoja on kohdassa [Kassayhteenvedon Power BI -sisältö](Cash-Overview-Power-BI-content.md).</span><span class="sxs-lookup"><span data-stu-id="697b9-144">For more information, see [Cash overview Power BI content](Cash-Overview-Power-BI-content.md).</span></span>
