---
title: Vähittäismyynnin laskelmat
description: Tässä ohjeaiheessa kerrotaan, miten laskelmat luodaan ja kirjataan.
author: ashishmsft
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailParameters
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 85183
ms.assetid: df9c62a2-6f13-4a08-bdca-07d041172c1b
ms.search.region: Global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: Retail July 2017 update
ms.openlocfilehash: 9e88a8b22b73aca5c2cee6984ecad3c62e597102
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/29/2019
ms.locfileid: "347695"
---
# <a name="retail-statements"></a><span data-ttu-id="4059f-103">Vähittäismyyntilaskelmat</span><span class="sxs-lookup"><span data-stu-id="4059f-103">Retail statements</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="4059f-104">Microsoft Dynamics 365 for Retailissa laskelman kirjausprosessia käytetään seuraamaan pilvimyyntipisteen tai Modern POS:n (MPOS) tapahtumia.</span><span class="sxs-lookup"><span data-stu-id="4059f-104">In Microsoft Dynamics 365 for Retail, the statement posting process is used to account for the transactions that occur in Cloud point of sale (POS) or Modern POS (MPOS).</span></span> <span data-ttu-id="4059f-105">Laskelman kirjausprosessi hakee myyntipistetapahtumajoukon Headquarters (HQ) -asiakasohjelmaan jakeluaikataulun avulla.</span><span class="sxs-lookup"><span data-stu-id="4059f-105">The statement posting process uses the distribution schedule to pull a set of POS transactions into the headquarters (HQ) client.</span></span> <span data-ttu-id="4059f-106">**Vähittäismyynnin parametrit**- ja **Myymälät**-sivuilla määritetyillä parametreilla valitaan yksittäisiin laskelmiin haettavat tapahtumat.</span><span class="sxs-lookup"><span data-stu-id="4059f-106">The parameters that are defined on the **Retail parameters** and **Stores** pages are used to select the transactions that are pulled into individual statements.</span></span>

<span data-ttu-id="4059f-107">Seuraavassa kuvassa on laskelman kirjausprosessi.</span><span class="sxs-lookup"><span data-stu-id="4059f-107">The following illustration shows the statement posting process.</span></span> <span data-ttu-id="4059f-108">Tässä prosessissa myyntipisteeseen tallennetut tapahtumat lähetetään asiakkaalle Retail-ajastuksen avulla.</span><span class="sxs-lookup"><span data-stu-id="4059f-108">In this process, transactions that are recorded in the POS are transmitted to the client by using the Retail scheduler.</span></span> <span data-ttu-id="4059f-109">Kun asiakas on vastaanottanut tapahtumat, voit luoda, laskea ja kirjata myymälän tapahtumaotteen.</span><span class="sxs-lookup"><span data-stu-id="4059f-109">After the client receives the transactions, you can create, calculate, and post the transaction statement for the store.</span></span>

<span data-ttu-id="4059f-110">[![Laskelman kirjausprosessi](./media/retail-statements.png)](./media/retail-statements.png)</span><span class="sxs-lookup"><span data-stu-id="4059f-110">[![Statement posting process](./media/retail-statements.png)](./media/retail-statements.png)</span></span>

## <a name="creating-and-posting-statements"></a><span data-ttu-id="4059f-111">Laskelmien luominen ja kirjaaminen</span><span class="sxs-lookup"><span data-stu-id="4059f-111">Creating and posting statements</span></span>

<span data-ttu-id="4059f-112">Voit luoda laskelman manuaalisesti tai eräprosesseissa, jotka määritetään suoritettavaksi säännöllisesti koko päivän ajalta.</span><span class="sxs-lookup"><span data-stu-id="4059f-112">You can create a statement manually or by using batch processes that you set up to run periodically throughout the day.</span></span> <span data-ttu-id="4059f-113">Molemmissa tapauksissa käytetään seuraavia ohjeita, joilla voit luoda ja kirjata laskelmat.</span><span class="sxs-lookup"><span data-stu-id="4059f-113">In both cases, the following steps are used to create and post statements.</span></span>

### <a name="create-the-statement"></a><span data-ttu-id="4059f-114">Luo laskelma</span><span class="sxs-lookup"><span data-stu-id="4059f-114">Create the statement</span></span>

<span data-ttu-id="4059f-115">Tämä vaihe kuvaa myymälän, johon laskelma luodaan manuaalisesti.</span><span class="sxs-lookup"><span data-stu-id="4059f-115">This step identifies the store that the statement is manually created for.</span></span> <span data-ttu-id="4059f-116">Jos määrität eräkäsittelyn, voit automaattisesti luoda raportteja myymälöille määrittämäsi aikataulun mukaan.</span><span class="sxs-lookup"><span data-stu-id="4059f-116">If you configure a batch process, you can automatically create statements for all stores, based on a schedule that you define.</span></span>

### <a name="calculate-the-statement"></a><span data-ttu-id="4059f-117">Laske laskelma</span><span class="sxs-lookup"><span data-stu-id="4059f-117">Calculate the statement</span></span>

<span data-ttu-id="4059f-118">Tässä vaiheessa valitaan tapahtumarivit jokaiselle myymälälle **Vähittäismyynnin parametrit**- ja **Myymälät**-sivuilla määritettyjen ehtojen perusteella.</span><span class="sxs-lookup"><span data-stu-id="4059f-118">In this step, the transaction lines are selected based on criteria that are defined for each store on the **Retail parameters** and **Stores** pages.</span></span> <span data-ttu-id="4059f-119">Voit määrittää näillä sivuilla ehdot ja tapahtumien laskentatavan.</span><span class="sxs-lookup"><span data-stu-id="4059f-119">On these pages, you define the criteria and specify how the transactions are calculated.</span></span> <span data-ttu-id="4059f-120">Tarkastele luetteloa laskelmaan sisältyvistä tapahtumista ennen laskelman laatimista käyttämällä **Tapahtumat**-sivulla.</span><span class="sxs-lookup"><span data-stu-id="4059f-120">To view a list of the transactions that are included in the statement before you calculate the statement, use the **Transactions** page.</span></span>

<span data-ttu-id="4059f-121">Laskelman laskennassa käytetään kassanlaskennan summaa laskettuna summana.</span><span class="sxs-lookup"><span data-stu-id="4059f-121">Statement calculation uses tender declarations from the registers as the counted amount.</span></span> <span data-ttu-id="4059f-122">Lasketun summan voi myös syöttää manuaalisesti.</span><span class="sxs-lookup"><span data-stu-id="4059f-122">Alternatively, you can enter the counted amount manually.</span></span> <span data-ttu-id="4059f-123">Laskelma näyttää kaikkien maksutapojen tapahtumien myyntimäärän ja todellisen lasketun määrän välisen eron.</span><span class="sxs-lookup"><span data-stu-id="4059f-123">The statement shows the difference between the sales amount for the transactions and the actual counted amount in all payment methods.</span></span> <span data-ttu-id="4059f-124">Laskelma kirjataan vain, jos tämä ero on pienempi kuin suurin mahdollinen myymälälle määritetty kirjausero.</span><span class="sxs-lookup"><span data-stu-id="4059f-124">The statement is posted only if this difference is less than the maximum posting difference that is defined for the store.</span></span>

> [!NOTE]
> <span data-ttu-id="4059f-125">Laskelman laskentaprosessi käyttää yleistä numerosarjaa.</span><span class="sxs-lookup"><span data-stu-id="4059f-125">The statement calculation process uses the global number sequence.</span></span>

<span data-ttu-id="4059f-126">Kun lasket laskelman, laskenta sisältää seuraavat tehtävät:</span><span class="sxs-lookup"><span data-stu-id="4059f-126">When you calculate a statement, the calculation includes the following tasks:</span></span>

- <span data-ttu-id="4059f-127">Merkitään sellaiset tapahtumat, joita ei sisällytetty edellisen raportin laskelmaan valitulla päivämääräalueella.</span><span class="sxs-lookup"><span data-stu-id="4059f-127">For the selected date range, mark transactions that weren't included in a previous statement calculation.</span></span>
- <span data-ttu-id="4059f-128">Laske valittujen tapahtumien maksuvälinesummien kokonaissummat.</span><span class="sxs-lookup"><span data-stu-id="4059f-128">Calculate the total amounts that were tendered in the selected transactions.</span></span> <span data-ttu-id="4059f-129">Tulokset näkyvät laskelmariveillä laskelmamenetelmästä mukaan:</span><span class="sxs-lookup"><span data-stu-id="4059f-129">The results are shown on the statement lines, depending on the statement method:</span></span>

    - <span data-ttu-id="4059f-130">Jos raporttitapa on **Yhteensä**, rivi luodaan jokaiselle maksutavalle valituissa tapahtumissa.</span><span class="sxs-lookup"><span data-stu-id="4059f-130">If the statement method is **Total**, a line is created for each payment method in the selected transactions.</span></span>
    - <span data-ttu-id="4059f-131">Jos valittu raporttitapa on **Henkilökunta**, rivi luodaan jokaiselle maksutavalle tapahtumissa, jotka suoritti valittu työntekijä.</span><span class="sxs-lookup"><span data-stu-id="4059f-131">If the statement method is **Staff**, a line is created for each payment method in transactions that were performed by the selected staff member.</span></span>
    - <span data-ttu-id="4059f-132">Jos valittu raporttitapa on **Kassapääte**, rivi luodaan jokaiselle maksutavalle tapahtumissa, jotka suoritettiin valitussa kassakoneessa.</span><span class="sxs-lookup"><span data-stu-id="4059f-132">If the statement method is **POS terminal**, a line is created for each payment method in transactions that were performed on the selected register.</span></span>
    - <span data-ttu-id="4059f-133">Jos valittu raporttitapa on **Vuoro**, rivi luodaan jokaiselle maksutavalle tapahtumissa, jotka suoritettiin vuoron aikana.</span><span class="sxs-lookup"><span data-stu-id="4059f-133">If the statement method is **Shift**, a line is created for each payment method in transactions that were performed during a shift.</span></span>

<span data-ttu-id="4059f-134">Jos **Jakoperusteena laskelmatapa** -valintaruutu valitaan **Myymälät**-sivulla, erillinen laskelma luodaan **Laskelmatapa**-kentässä valitun arvon perusteella.</span><span class="sxs-lookup"><span data-stu-id="4059f-134">If the **Split by Statement method** check box is selected on the **Stores** page, a separate statement is created based on the value that is selected in the **Statement method** field.</span></span>

<span data-ttu-id="4059f-135">Jos myymälän työajat on laajennettu yli keskiyön, voit määrittää laskelman kirjauksen siten, se perustuu työpäivän päättymiseen kalenteripäivän päättymisen sijaan.</span><span class="sxs-lookup"><span data-stu-id="4059f-135">If your store's operating hours extend past midnight, you can configure statement posting so that it's based on the end of the business day instead of the end of the calendar day.</span></span>

<span data-ttu-id="4059f-136">Anna **Myymälät**-sivun **Laskelma/sulkeminen**-pikavälilehden **Työpäivän päätös**-kenttään aika, jolloin viimeinen tapahtuma on kirjattava, jotta se sisältyy työpäivän tapahtumiin.</span><span class="sxs-lookup"><span data-stu-id="4059f-136">On the **Stores** page, on the **Statement/closing** FastTab, in the **End of business day** field, enter the time that the last transaction must be recorded to be included in the business day's statement.</span></span> <span data-ttu-id="4059f-137">Valitse **Kirjaa työpäivänä** -valintaruutu, jotta tapahtumat kirjataan saman työpäivän aikana.</span><span class="sxs-lookup"><span data-stu-id="4059f-137">Select the **Post as business day** check box to post the transactions within the same business day.</span></span> <span data-ttu-id="4059f-138">Kun laskelma kirjataan, saman työpäivän aikana tallennetut tapahtumat voidaan sisällyttää samaan myyntitilaukseen, vaikka osa tapahtumista tapahtuu ennen puoltayötä ja osa puolenyön jälkeen.</span><span class="sxs-lookup"><span data-stu-id="4059f-138">When the statement is posted, transactions that are recorded within the same business day can be included on the same sales order, even if some transactions occur before midnight and other transactions occur after midnight.</span></span>

#### <a name="example-post-a-statement-for-a-business-day-that-extends-over-two-calendar-days"></a><span data-ttu-id="4059f-139">Esimerkki: Kirjaa ilmoitus työpäivälle, joka ulottuu yli kahdelle kalenteripäivällle</span><span class="sxs-lookup"><span data-stu-id="4059f-139">Example: Post a statement for a business day that extends over two calendar days</span></span>

<span data-ttu-id="4059f-140">Myymälä aukioloaika on 8.00–3.00 ja **Kirjaa työpäivänä** -valintaruutu on valittu myymälän määrityksissä.</span><span class="sxs-lookup"><span data-stu-id="4059f-140">A store is open between 8:00 AM and 3:00 AM, and the **Post as business day** check box is selected in the store's configuration.</span></span> <span data-ttu-id="4059f-141">Myymälä kirjaa tapahtumia 31.5. kello 8.00–24.00.</span><span class="sxs-lookup"><span data-stu-id="4059f-141">On May 31, the store records transactions between 8:00 AM and midnight.</span></span> <span data-ttu-id="4059f-142">Myymälä kirjaa tapahtumia myös 1.6. kello 00.01–3.00.</span><span class="sxs-lookup"><span data-stu-id="4059f-142">The store also records transactions between 12:01 AM and 3:00 AM on June 1.</span></span>

<span data-ttu-id="4059f-143">Kun myymälä kirjaa tapahtumat työpäivän päätteeksi, järjestelmä muodostaa myyntitilauksen, joka sisältää kaikki tapahtumat, jotka on kirjattu työtunteina kello 8.00–3.00, vaikka tapahtumat ovat tapahtuneet toukokuun 31. ja kesäkuun 1. päivänä.</span><span class="sxs-lookup"><span data-stu-id="4059f-143">When the store posts its statement for the close of the business day, the sales order that is generated includes all transactions that were recorded between the business hours of 8:00 AM and 3:00 AM, even though the transactions occurred on two days, May 31 and June 1.</span></span>

<span data-ttu-id="4059f-144">Jos sama myymälä on määritetty, kun **Kirjaa työpäivänä** -valintaruutua ei ole valittu, erillisiä myyntitilauksia luodaan, kun myymälä kirjaa sen laskelman työpäivän päätteeksi.</span><span class="sxs-lookup"><span data-stu-id="4059f-144">If the **Post as business day** check box is cleared for the same store, separate sales orders are generated when the store posts its statement for the close of the business day.</span></span> <span data-ttu-id="4059f-145">Yksi myyntitilaus sisältää tapahtumia, jotka on kirjattu työaikana kello 8.00–24.00 31.5. ja toinen myyntitilaus sisältää tapahtumia, jotka kirjattiin 1.6. kello 00.01–3.00.</span><span class="sxs-lookup"><span data-stu-id="4059f-145">One sales order includes the transactions that were recorded between the business hours of 8:00 AM and midnight on May 31, and the second sales order includes the transactions that were recorded between the business hours of 12:01 AM and 3:00 AM on June 1.</span></span>

> [!NOTE]
> <span data-ttu-id="4059f-146">Laskelman ajanjaksoon sisältyvät vuorot on suljettava, ennen kuin voit luoda laskelmia.</span><span class="sxs-lookup"><span data-stu-id="4059f-146">Before you can create statements, you should close the shifts in the statement period.</span></span>

### <a name="post-the-statement"></a><span data-ttu-id="4059f-147">Kirjaa laskelma</span><span class="sxs-lookup"><span data-stu-id="4059f-147">Post the statement</span></span>

<span data-ttu-id="4059f-148">Kun kirjaat laskelman, myyntitilaukset ja laskut luodaan laskelman vähittäismyyntiin.</span><span class="sxs-lookup"><span data-stu-id="4059f-148">When you post a statement, sales orders and invoices are created for the retail sales in the statement.</span></span>

- <span data-ttu-id="4059f-149">Itsepalvelutukkumyynti yhdistetään yhdeksi myyntitilaukseksi ja laskutetaan oletusasiakkaalta, joka on määritetty myymälälle.</span><span class="sxs-lookup"><span data-stu-id="4059f-149">Cash and carry sales are aggregated onto one sales order, and are invoiced for the default customer who is assigned to the store.</span></span>
- <span data-ttu-id="4059f-150">Vähittäismyynti, johon asiakas on lisätty tapahtumaan Microsoft Dynamics 365 for RetailPOS:ssa luo erillisiä myyntitilauksia ja laskuja, yksi kutakin asiakaskohtaisesti.</span><span class="sxs-lookup"><span data-stu-id="4059f-150">Retail sales for which a customer was added to the transaction in Microsoft Dynamics 365 for Retail POS generate separate sales orders and invoices, one for each unique customer.</span></span>

<span data-ttu-id="4059f-151">Maksukirjauskansioita luodaan automaattisesti lausunnon maksuille, ja varasto päivitetään myyntipistemyymälälle.</span><span class="sxs-lookup"><span data-stu-id="4059f-151">Payment journals are automatically created for the payments in the statement, and the inventory is updated for the POS store.</span></span>
