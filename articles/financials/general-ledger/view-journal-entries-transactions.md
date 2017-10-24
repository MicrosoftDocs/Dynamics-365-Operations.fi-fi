---
title: "Näytä tapahtumat ja kirjauskansiomerkinnät"
description: "Tässä artikkelissa esitellään kirjauskansiovientien ja -tapahtumien eri tarkastelutavat."
author: aprilolson
manager: AnnBe
ms.date: 08/01/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: LedgerTransVoucher
audience: Application User
ms.reviewer: robinr
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 13031
ms.assetid: 281c7ea6-4dfd-4d1f-994f-c361ee299dbe
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: fda51a8382cb7d8a9aa7392224486189c442550f
ms.contentlocale: fi-fi
ms.lasthandoff: 09/29/2017

---

# <a name="view-journal-entries-and-transactions"></a><span data-ttu-id="69179-103">Näytä tapahtumat ja kirjauskansiomerkinnät</span><span class="sxs-lookup"><span data-stu-id="69179-103">View journal entries and transactions</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="69179-104">Tässä artikkelissa esitellään kirjauskansiovientien ja -tapahtumien eri tarkastelutavat.</span><span class="sxs-lookup"><span data-stu-id="69179-104">This article explains the various ways that you can view journal entries and transactions.</span></span> 

<span data-ttu-id="69179-105">Käyttäjillä, jotka haluavat tarkastella kirjauskansioita ja tapahtumia, on monta eri tapaa tarkastella tietoja.</span><span class="sxs-lookup"><span data-stu-id="69179-105">Users who want to view journals and transactions have several ways to access the data.</span></span> <span data-ttu-id="69179-106">He voivat hyödyntää kyselysivuja, joissa on perehtymismahdollisuus tai he voivat käyttää kirjanpidon eri raporttivaihtoehtoja.</span><span class="sxs-lookup"><span data-stu-id="69179-106">They can take advantage of inquiry pages that provide drill-down ability, or they can use various report options in the general ledger.</span></span>

## <a name="voucher-transactions"></a><span data-ttu-id="69179-107">Tositetapahtumat</span><span class="sxs-lookup"><span data-stu-id="69179-107">Voucher transactions</span></span>
<span data-ttu-id="69179-108">**Tositetapahtumat** on kysely-sivu, jossa voit valita eri tauluista ja kentistä kriteerit etsimäsi saldon tai tapahtuman valitsemiseksi.</span><span class="sxs-lookup"><span data-stu-id="69179-108">**Voucher transactions** is an inquiry page where you can select from various tables and fields to specify criteria for the balance or transaction that you're searching for.</span></span> <span data-ttu-id="69179-109">Esimerkiksi voit tarkastella kaikkia tietyn päivän tai tilin tapahtumia, tai kaikkia tapahtumia **Käyttöjärjestelmä**-tyypissä, jotka ovat tietyssä kirjanpitotasossa.</span><span class="sxs-lookup"><span data-stu-id="69179-109">For example, you can view all transactions for a specific date or account, or all transactions of the **Operating** type that are in a specific posting layer.</span></span> <span data-ttu-id="69179-110">Oletusarvon mukaan sivulla näkyy kirjauskansionumero, tosite, päivämäärä ja päätili, mutta voit lisätä muita tauluja, kenttiä ja kriteerejä tarkentaakesi hakua.</span><span class="sxs-lookup"><span data-stu-id="69179-110">By default, the page shows the journal number, voucher, date, and main account, but you can add additional tables, fields, and criteria to narrow down your search.</span></span>

## <a name="audit-trail"></a><span data-ttu-id="69179-111">Kirjausketju</span><span class="sxs-lookup"><span data-stu-id="69179-111">Audit trail</span></span>
<span data-ttu-id="69179-112">**Kirjausketju** on kysely-sivu, jossa näkyvät tapahtumatyypit, kuvaukset, kenen luomia tapahtumat ovet ja milloin ne on luotu.</span><span class="sxs-lookup"><span data-stu-id="69179-112">**Audit trail** is an inquiry page that shows the types of transactions, descriptions, who the transactions were created by, and when they were created.</span></span> <span data-ttu-id="69179-113">**Kirjausketju** -kyselyn sivulla voit tarkastella tositetapahtumia.</span><span class="sxs-lookup"><span data-stu-id="69179-113">From the **Audit trail** inquiry page, you can view the voucher transactions.</span></span>

## <a name="financial-reports"></a><span data-ttu-id="69179-114">Talousraportit</span><span class="sxs-lookup"><span data-stu-id="69179-114">Financial reports</span></span>
<span data-ttu-id="69179-115">Voit myös selata ja analysoida kirjanpitotapahtumia suorittamalla tilinpäätökset.</span><span class="sxs-lookup"><span data-stu-id="69179-115">You can also explore and analyze general ledger transactions by running financial reports.</span></span> <span data-ttu-id="69179-116">Koska tilinpäätöksien rakenne voi perustua tileihin, dimensioihin, tililuokkiin tai näiden kolmen yhdistelmään, voit tarkastella tapahtumia siirtymällä eri tavoin.</span><span class="sxs-lookup"><span data-stu-id="69179-116">Because the design of financial reports can be based on accounts, dimensions, account categories, or a combination of the three, you can view the transactions by drilling down in various ways.</span></span> <span data-ttu-id="69179-117">Jos tarvitset lisätietoja kirjanpitoa varten, voit sisällyttää myös useita tapahtuman ominaisuuksia raportin suunnittelun yhteydessä.</span><span class="sxs-lookup"><span data-stu-id="69179-117">If you require more information for general ledger transactions, you can also include multiple transaction properties as part of the report design.</span></span> <span data-ttu-id="69179-118">Lisäksi voit halutessasi tarkastella tapahtumia, jotka muodostavat yleisen kirjanpitosaldon, voit tutkia tilitapahtumia, aivan samoin kuin voit **pääkirjan** luettelosivulta.</span><span class="sxs-lookup"><span data-stu-id="69179-118">Additionally, if you want to see the transactions that make up a general ledger balance, you can drill down to account transactions, just as you can from the **Trial balance** list page.</span></span>

## <a name="ledger-reports"></a><span data-ttu-id="69179-119">Kirjanpitoraportit</span><span class="sxs-lookup"><span data-stu-id="69179-119">Ledger reports</span></span>
<span data-ttu-id="69179-120">Talousraporttien lisäksi voit käyttää seuraavia kirjanpitoraportteja tarkastellaksesi kirjanpidon tapahtumia:</span><span class="sxs-lookup"><span data-stu-id="69179-120">In addition to the financial reports, you can use the following ledger reports to view general ledger transactions:</span></span>

-   <span data-ttu-id="69179-121">**Dimension laskelma** – Tässä raportissa näkyy tapahtumat tilin ja päivän mukaan ja on myös mahdollista näyttää ne ajan ja dimension mukaan.</span><span class="sxs-lookup"><span data-stu-id="69179-121">**Dimension statement** – This report shows transactions by day and account, and there are also options to show transactions by dimension and period.</span></span>
-   <span data-ttu-id="69179-122">**Kirjanpidon tapahtumaluettelo** – Tämä raportti näyttää tapahtumat tapahtumissa, kirjanpidossa ja tilivaluutan raportoinnin.</span><span class="sxs-lookup"><span data-stu-id="69179-122">**Ledger transaction list** – This report shows transactions in transaction, accounting, and reporting currencies for an account.</span></span>
-   <span data-ttu-id="69179-123">**Tulosta kirjauskansio** – Tämä raportti esittää kirjatun kirjauskansion tuloksen.</span><span class="sxs-lookup"><span data-stu-id="69179-123">**Print journal** – This report shows the result of a posted journal.</span></span> <span data-ttu-id="69179-124">Voit suorittaa raportin kirjauskansion eränumeron tai tyypin mukaan, tai lisätä lisäkenttiä.</span><span class="sxs-lookup"><span data-stu-id="69179-124">You can run the report by journal batch number or journal type, or add additional fields.</span></span>
-   <span data-ttu-id="69179-125">**Kirjatut tapahtumat kirjauskansioittain** -Tässä raportissa näkyvät tapahtumat, jotka on kirjattu kirjauskansioon, tositteen mukaan.</span><span class="sxs-lookup"><span data-stu-id="69179-125">**Posted transactions by journal** – This report shows the transactions that have been posted to a journal, grouped by voucher.</span></span>
-   <span data-ttu-id="69179-126">**Tapahtumaluettelo päivämäärittäin** – Tämä raportti näyttää kaikki tapahtumat päivämäärittäin, kirjauskansion numeron, tositteen ja kirjanpitotilin kanssa.</span><span class="sxs-lookup"><span data-stu-id="69179-126">**Transaction list by date** – This report shows all the transactions by date, together with the journal number, voucher, and ledger account.</span></span> <span data-ttu-id="69179-127">Se näyttää lisäksi tapahtumat tapahtuman, kirjanpidon ja raportoinnin valuuttana.</span><span class="sxs-lookup"><span data-stu-id="69179-127">It also shows the transactions in the transaction, accounting, and reporting currencies.</span></span>
-   <span data-ttu-id="69179-128">**Tapahtumalähde** – Tämä tapahtumaraportti näyttää tilin kirjanpidon, tapahtuman ja raportoinnin tilivaluutan.</span><span class="sxs-lookup"><span data-stu-id="69179-128">**Transaction origin** – This transaction report shows the account by journal, and by transaction, accounting, and reporting currency.</span></span> <span data-ttu-id="69179-129">Siinä näkyy myös kirjauskansion jokainen rivi, jota on käytetty osoitteeksi.</span><span class="sxs-lookup"><span data-stu-id="69179-129">It also shows each line of the journal that was used as an offset.</span></span>


##<a name="see-also"></a><span data-ttu-id="69179-130">Lisätietoja</span><span class="sxs-lookup"><span data-stu-id="69179-130">See also</span></span>
- [<span data-ttu-id="69179-131">Kirjanpitotilin saldot</span><span class="sxs-lookup"><span data-stu-id="69179-131">General ledger account balances</span></span>](general-ledger-account-balances.md) 
- [<span data-ttu-id="69179-132">Kirjanpitolähteen hallinta</span><span class="sxs-lookup"><span data-stu-id="69179-132">Accounting source explorer</span></span>](..\accounts-payable\accounting-source-explorer.md)
- [<span data-ttu-id="69179-133">Talousraportointi</span><span class="sxs-lookup"><span data-stu-id="69179-133">Financial reporting</span></span>](financial-reporting-getting-started.md)
- [<span data-ttu-id="69179-134">Kirjauskansiovientien näyttäminen</span><span class="sxs-lookup"><span data-stu-id="69179-134">View journal entries</span></span>](tasks/view-journal-entries-or-transactions.md)




