---
title: Maksuliikenteen työtila
description: Tässä ohjeaiheessa on tietoja maksuliikenteen työtilasta. Työtilassa on näkyvillä yrityksen pankkitileihin liittyviä tietoja. Siinä on myös yhteenvetonäkymä ja analytiikkasivu. Yhteenvetonäkymässä on yhteenvetoruudut, pankkitilitiedot, saldokaavio ja liittyvät tiedot. Analytiikkasivu näyttää Microsoft Power BI:n ominaisuuksien avulla pankkitilin saldoihin liittyviä visuaalisia tietoja.
author: saraschi2
ms.date: 01/12/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BankTreasurerWorkspace
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: 262b871a7c35d01283386af6454bb2852197e3b9
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/01/2021
ms.locfileid: "5818821"
---
# <a name="bank-management-workspace"></a><span data-ttu-id="f83d7-106">Maksuliikenteen työtila</span><span class="sxs-lookup"><span data-stu-id="f83d7-106">Bank management workspace</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f83d7-107">**Maksuliikenne**-työtilassa on yrityksen pankkitileihin liittyviä tietoja.</span><span class="sxs-lookup"><span data-stu-id="f83d7-107">The **Bank management** workspace shows information that is related to company bank accounts.</span></span> <span data-ttu-id="f83d7-108">Työtilassa on **Yhteenveto**-näkymä ja **Analytiikka**-sivu.</span><span class="sxs-lookup"><span data-stu-id="f83d7-108">This workspace includes a **Summary** view and an **Analytics** page.</span></span> <span data-ttu-id="f83d7-109">**Yhteenveto**-näkymässä on yhteenvetoruudut, pankkitilitiedot, saldokaavio ja liittyvät tiedot.</span><span class="sxs-lookup"><span data-stu-id="f83d7-109">The **Summary** view shows summary tiles, bank account information, a balance chart, and related information.</span></span> <span data-ttu-id="f83d7-110">**Analytiikka**-sivu näyttää Microsoft Power BI:n ominaisuuksien avulla pankkitilin saldoihin liittyviä visuaalisia tietoja.</span><span class="sxs-lookup"><span data-stu-id="f83d7-110">The **Analytics** page uses the capabilities of Microsoft Power BI to show visuals that are related to bank account balances.</span></span>

## <a name="summary-view"></a><span data-ttu-id="f83d7-111">Yhteenvetonäkymä</span><span class="sxs-lookup"><span data-stu-id="f83d7-111">Summary view</span></span>

### <a name="summary"></a><span data-ttu-id="f83d7-112">Yhteenveto</span><span class="sxs-lookup"><span data-stu-id="f83d7-112">Summary</span></span>

<span data-ttu-id="f83d7-113">**Yhteenveto**-osan ruuduissa on pankkitilien yleiskatsaus, Siitä voi myös siirtyä nopeasti eniten käytetyille sivuille.</span><span class="sxs-lookup"><span data-stu-id="f83d7-113">The tiles in the **Summary** section give an overview of your bank accounts and provide quick access to the pages that you most often have to use.</span></span> <span data-ttu-id="f83d7-114">Pankkitilin täsmäytystiedot koskevat Pankkitilin täsmäytyksen lisätoiminnot -toimintoa.</span><span class="sxs-lookup"><span data-stu-id="f83d7-114">The bank reconciliation information is specific to the Advanced bank reconciliation functionality.</span></span> <span data-ttu-id="f83d7-115">Tiedot koskevat vain niitä pankkitilejä, joiden **Pankkitilin täsmäytyksen lisätoiminnot** -asetukseksi on valittu **Kyllä** **Pankkitili**-sivulla.</span><span class="sxs-lookup"><span data-stu-id="f83d7-115">Information is included only for those bank accounts that have the **Advanced bank reconciliation** option set to **Yes** on the **Bank account** page.</span></span> <span data-ttu-id="f83d7-116">Voit tuoda **Yhteenveto**-osiossa kaikkien yritysten pankkitilien pankkitiedostoja.</span><span class="sxs-lookup"><span data-stu-id="f83d7-116">From the **Summary** section, you can import electronic bank files for bank accounts across all legal entities.</span></span>

### <a name="bank-accounts"></a><span data-ttu-id="f83d7-117">Pankkitilit</span><span class="sxs-lookup"><span data-stu-id="f83d7-117">Bank accounts</span></span>

<span data-ttu-id="f83d7-118">Kutakin yrityksen pankkitiliä vastaa **Pankkitilit**-osion kortti.</span><span class="sxs-lookup"><span data-stu-id="f83d7-118">Each bank account in the legal entity is represented by a card in the **Bank accounts** section.</span></span> <span data-ttu-id="f83d7-119">Näkyvissä on nykyinen saldo. Lisäksi kyseisen yhteenvedon saldosumman tapahtumiin voi porautua.</span><span class="sxs-lookup"><span data-stu-id="f83d7-119">The current balance is shown, and you can drill down to the transactions that make up that summary balance amount.</span></span> <span data-ttu-id="f83d7-120">Myös **Välitilitapahtumat**-summassa voi porautua kyseisen yhteenvetosumman tapahtumiin.</span><span class="sxs-lookup"><span data-stu-id="f83d7-120">The **Bridged transactions** amount also lets you drill down to the transactions that make up that summary amount.</span></span> <span data-ttu-id="f83d7-121">Välitilitapahtumat ovat odottavia tapahtumia, jotka on kirjattu välitiliöintitoiminnolla mutta joita ei ole vielä selvitetty.</span><span class="sxs-lookup"><span data-stu-id="f83d7-121">Bridged transactions are any pending transactions that have been posted by using bridging functionality, but that haven't yet been cleared.</span></span> <span data-ttu-id="f83d7-122">**Odottava saldo** -summa on nykyinen saldo, josta on vähennetty välitiliöidyt eli odottavat tapahtumat.</span><span class="sxs-lookup"><span data-stu-id="f83d7-122">The **Pending balance** amount is the current balance minus the bridged, or pending, transactions.</span></span>

<span data-ttu-id="f83d7-123">Kortista näkee myös, milloin pankkitili täsmäytettiin viimeksi.</span><span class="sxs-lookup"><span data-stu-id="f83d7-123">The card also shows when the bank account was last reconciled.</span></span> <span data-ttu-id="f83d7-124">Nämä tiedot näkyvät vain, jos pankkitilissä on otettu käyttöön Pankkitilin täsmäytyksen lisätoiminnot.</span><span class="sxs-lookup"><span data-stu-id="f83d7-124">This information is shown only if Advanced bank reconciliation is enabled for the bank account.</span></span>

### <a name="balance"></a><span data-ttu-id="f83d7-125">Tase</span><span class="sxs-lookup"><span data-stu-id="f83d7-125">Balance</span></span>

<span data-ttu-id="f83d7-126">**Saldo**-kaaviossa on näkyvissä joko **Pankkitilit**-osiossa valitun tilin historialliset saldotiedot tai yrityksen kaikkien pankkitilien historiallisten saldotietojen yhteenveto.</span><span class="sxs-lookup"><span data-stu-id="f83d7-126">The **Balance** chart shows either historic balance information for the bank account that is selected in the **Bank accounts** section or a summary of historic balance information for all bank accounts in the legal entity.</span></span> <span data-ttu-id="f83d7-127">Nämä tiedot ovat saatavilla eripituisille jaksoille: kuluva viikko, kuluva kuukausi, kuluva vuosi, viimeiset viisi vuotta ja kaikki kaudet (pankkitilin koko historia).</span><span class="sxs-lookup"><span data-stu-id="f83d7-127">This information is available for various periods: the current week, the current month, the current year, the last five years, and all periods (the full history of the bank account).</span></span> 

<span data-ttu-id="f83d7-128">Jos tarkastelet yksittäisen pankkitilin **Saldo**-kaaviota, historialliset saldot näytetään pankkitilin valuuttana.</span><span class="sxs-lookup"><span data-stu-id="f83d7-128">If you're viewing the **Balance** chart for a single bank account, the historic balances are shown in the bank account currency.</span></span> <span data-ttu-id="f83d7-129">Jos tarkastelet yrityksen kaikkien pankkitilin kaaviota, historialliset saldot näytetään kirjapitovaluuttana.</span><span class="sxs-lookup"><span data-stu-id="f83d7-129">If you're viewing the chart for all bank accounts in the legal entity, the historic balances are shown in the accounting currency.</span></span>

<span data-ttu-id="f83d7-130">Kaavion yläreunasta voi tarkistaa, milloin tiedot on viimeksi päivitetty.</span><span class="sxs-lookup"><span data-stu-id="f83d7-130">Information about when the data was last updated appears at the top of the chart.</span></span> <span data-ttu-id="f83d7-131">Voit päivittää tietoja tarpeen mukaan:</span><span class="sxs-lookup"><span data-stu-id="f83d7-131">You can update the data as you require.</span></span>

### <a name="related-information"></a><span data-ttu-id="f83d7-132">Aiheeseen liittyviä tietoja</span><span class="sxs-lookup"><span data-stu-id="f83d7-132">Related information</span></span>

<span data-ttu-id="f83d7-133">Voit viimeistellä pankkisiirrot avaamalla **Liittyvät tiedot** -osiossa **Kirjauskansio**-sivun.</span><span class="sxs-lookup"><span data-stu-id="f83d7-133">From the **Related information** section, you can open the **General journal** page to complete bank transfers.</span></span> <span data-ttu-id="f83d7-134">Voit avata myös **Pankkitapahtumat**- ja **Välitilitapahtumat**-sivut nopeasti.</span><span class="sxs-lookup"><span data-stu-id="f83d7-134">You can also quickly open the **Bank transactions** and **Bridged transactions** pages.</span></span>

## <a name="analytics-view"></a><span data-ttu-id="f83d7-135">Analytiikkanäkymä</span><span class="sxs-lookup"><span data-stu-id="f83d7-135">Analytics view</span></span>

<span data-ttu-id="f83d7-136">**Analytiikka**-sivulla on tärkeitä valitun yrityksen pankkitilien mittareita.</span><span class="sxs-lookup"><span data-stu-id="f83d7-136">The **Analytics** page provides important metrics about the bank accounts in the current company.</span></span> <span data-ttu-id="f83d7-137">Sivulla on seuraavat visualisoinnit:</span><span class="sxs-lookup"><span data-stu-id="f83d7-137">The following visualizations are available on the page:</span></span>

-   <span data-ttu-id="f83d7-138">Pankkitilin kokonaissaldo järjestelmän valuuttana</span><span class="sxs-lookup"><span data-stu-id="f83d7-138">Total bank balance in system currency</span></span>
-   <span data-ttu-id="f83d7-139">Saldo yrityksen mukaan</span><span class="sxs-lookup"><span data-stu-id="f83d7-139">Balance by legal entity</span></span>
-   <span data-ttu-id="f83d7-140">Kuluvan päivän toteutuneen ja ennustetun saldon vertailu pankkitilin valuuttana</span><span class="sxs-lookup"><span data-stu-id="f83d7-140">Today’s actual vs forecasted balance in bank account currency</span></span>
-   <span data-ttu-id="f83d7-141">Saldo pankkitilin mukaan</span><span class="sxs-lookup"><span data-stu-id="f83d7-141">Balance by bank account</span></span>
-   <span data-ttu-id="f83d7-142">Saldo valuutan mukaan</span><span class="sxs-lookup"><span data-stu-id="f83d7-142">Balance by currency</span></span>

<span data-ttu-id="f83d7-143">Voit tarkastella kaikkien yritysten pankkitietojen analytiikkaa **Kassayhteenveto – kaikki yritykset** -työtilassa.</span><span class="sxs-lookup"><span data-stu-id="f83d7-143">You can view bank analytics across all companies from the **Cash overview – all companies** workspace.</span></span> <span data-ttu-id="f83d7-144">Lisätietoja on kohdassa [Kassayhteenvedon Power BI -sisältö](Cash-Overview-Power-BI-content.md).</span><span class="sxs-lookup"><span data-stu-id="f83d7-144">For more information, see [Cash overview Power BI content](Cash-Overview-Power-BI-content.md).</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]