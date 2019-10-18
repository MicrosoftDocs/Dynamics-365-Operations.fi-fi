---
title: Projektiin laskutus
description: Tämä artikkeli sisältää aika- ja materiaaliprojektien sekä kiinteähintaisten projektien projektilaskutuksen yleiskatsauksen. Artikkelissa on tietoja myös laskuehdotuksista (alustavista laskuista), laskutuksen hallinnasta, ennakkolaskutuksesta, toimittajan laskutuksesta ja hyvityslaskuista.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjInvoiceCashFlow, ProjInvoiceControl, ProjInvoiceListPage, ProjInvoiceProposalDetail, ProjInvoiceProposalListPage
audience: Application User, IT Pro
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 23111
ms.assetid: 1812d6f2-8b34-4258-8f5f-dcf12281547f
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e3d91f6b1ccc3254e2c04d24c5f9bf2014c64e50
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/27/2019
ms.locfileid: "2177608"
---
# <a name="project-invoicing"></a><span data-ttu-id="a7a50-104">Projektiin laskutus</span><span class="sxs-lookup"><span data-stu-id="a7a50-104">Project invoicing</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a7a50-105">Tämä artikkeli sisältää aika- ja materiaaliprojektien sekä kiinteähintaisten projektien projektilaskutuksen yleiskatsauksen.</span><span class="sxs-lookup"><span data-stu-id="a7a50-105">This article provides an overview of project invoicing for Time and material projects and Fixed-price projects.</span></span> <span data-ttu-id="a7a50-106">Artikkelissa on tietoja myös laskuehdotuksista (alustavista laskuista), laskutuksen hallinnasta, ennakkolaskutuksesta, toimittajan laskutuksesta ja hyvityslaskuista.</span><span class="sxs-lookup"><span data-stu-id="a7a50-106">It includes information about invoice proposals (preliminary invoices), invoice control, on-account invoicing, vendor invoicing, and credit notes.</span></span>

<span data-ttu-id="a7a50-107">Projektityyppi määrittää, mitä laskutusmenettelyä käytetään.</span><span class="sxs-lookup"><span data-stu-id="a7a50-107">The project type determines which invoicing procedure should be applied.</span></span> <span data-ttu-id="a7a50-108">Vain kahta ulkoista projektityyppiä, aika- ja materiaaliprojektit sekä kiinteähintaiset projektit, voidaan laskuttaa.</span><span class="sxs-lookup"><span data-stu-id="a7a50-108">Only the two external project types, Time and material and Fixed-price, can be invoiced.</span></span> <span data-ttu-id="a7a50-109">Aika- ja materiaaliprojektit sekä kiinteähintaiset projektit liittyvät aina projektisopimukseen.</span><span class="sxs-lookup"><span data-stu-id="a7a50-109">Time and material projects and Fixed-price projects are always attached to a project contract.</span></span>

-   <span data-ttu-id="a7a50-110">**Kiinteähintaiset projektit** – Myyntilaskun summa perustuu laskun laskutusaikatauluun.</span><span class="sxs-lookup"><span data-stu-id="a7a50-110">**Fixed-price projects** – The customer invoice amount is based on invoice billing schedules.</span></span> <span data-ttu-id="a7a50-111">Laskutus tapahtuu ennakkolaskuasetusten, joita kutsutaan myös laskutusaikatauluksi.</span><span class="sxs-lookup"><span data-stu-id="a7a50-111">Invoicing is done through an on-account setup, which is also referred to as a billing schedule.</span></span> <span data-ttu-id="a7a50-112">Kiinteähintaiset projektit voidaan laskuttaa projekti- tai projektisopimuskohtaisesti.</span><span class="sxs-lookup"><span data-stu-id="a7a50-112">Fixed-price projects can be invoiced per project or per project contract.</span></span>
-   <span data-ttu-id="a7a50-113">**Aika- ja materiaaliprojektit** – Myyntilaskun summa perustuu projekteille annettuihin tapahtumariveihin.</span><span class="sxs-lookup"><span data-stu-id="a7a50-113">**Time and material projects** – The customer invoice amount is based on transaction lines that are entered on projects.</span></span> <span data-ttu-id="a7a50-114">Tapahtumat voidaan laskuttaa projekti- tai projektisopimuskohtaisesti.</span><span class="sxs-lookup"><span data-stu-id="a7a50-114">Transactions can be invoiced per project or per project contract.</span></span>

<span data-ttu-id="a7a50-115">Aika- ja materiaaliprojektit ja kiinteähintaiset projektit voidaan liittää laskutusprojekteihin kolmella tavalla:</span><span class="sxs-lookup"><span data-stu-id="a7a50-115">There are three ways to attach Time and material projects and Fixed-price projects to the invoice projects:</span></span>

-   <span data-ttu-id="a7a50-116">**Ennakkolaskutus** – Aika- ja materiaaliprojektit ja kiinteähintaiset projektit voidaan laskuttaa ennakkoon.</span><span class="sxs-lookup"><span data-stu-id="a7a50-116">**On-account invoicing** – Time and material projects and Fixed-price projects can be invoiced on account.</span></span> <span data-ttu-id="a7a50-117">Kummallekin projektityypille on määritettävä omat ennakkolaskutusasetukset.</span><span class="sxs-lookup"><span data-stu-id="a7a50-117">Two types of on-account setup are required, one for each project type.</span></span>
-   <span data-ttu-id="a7a50-118">**Laskutus kausittain** – Kausitoimintojen avulla voidaan laskuttaa eri projektien tapahtumia.</span><span class="sxs-lookup"><span data-stu-id="a7a50-118">**Invoicing in the periodic section** – Through the periodic functions, transactions can be invoiced across projects.</span></span> <span data-ttu-id="a7a50-119">Kausitoimintojen avulla voi laatia laskutettavien tapahtumien yleiskatsauksen.</span><span class="sxs-lookup"><span data-stu-id="a7a50-119">The periodic functions provide an overview of transactions that must be invoiced.</span></span>
-   <span data-ttu-id="a7a50-120">**Hyvityslaskujen käyttö laskutuksessa**– hyvityslasku voidaan luoda sekä aika- ja materiaaliprojekteille että kiinteähintaisille projekteille.</span><span class="sxs-lookup"><span data-stu-id="a7a50-120">**By using credit notes in invoicing** – A credit note can be created for both Time and material projects and Fixed-price projects.</span></span>

## <a name="invoice-proposals"></a><span data-ttu-id="a7a50-121">Laskuehdotukset</span><span class="sxs-lookup"><span data-stu-id="a7a50-121">Invoice proposals</span></span>
<span data-ttu-id="a7a50-122">Ennen kuin luot projektin myyntilaskun, voit luoda alustavan laskun tai laskuehdotuksen.</span><span class="sxs-lookup"><span data-stu-id="a7a50-122">Before you create a customer invoice for a project, you can create a preliminary invoice, or invoice proposal.</span></span> <span data-ttu-id="a7a50-123">Voit valita laskuehdotuksessa projektilaskuun sisällytettävät projektitapahtumat.</span><span class="sxs-lookup"><span data-stu-id="a7a50-123">In an invoice proposal, you can select project transactions to include in a project invoice.</span></span> <span data-ttu-id="a7a50-124">Voit sitten tarkistaa laskun tiedot ennen projektilaskun kirjaamista ja lähettämistä asiakkaalle tai toiselle rahoituslähteelle.</span><span class="sxs-lookup"><span data-stu-id="a7a50-124">You can then review the invoice details before you post the project invoice and send it to the customer or other funding source.</span></span>

### <a name="creating-invoice-proposals"></a><span data-ttu-id="a7a50-125">Laskuehdotusten luominen</span><span class="sxs-lookup"><span data-stu-id="a7a50-125">Creating invoice proposals</span></span>

<span data-ttu-id="a7a50-126">Voit luoda laskuehdotuksia manuaalisesti valitsemalla määritetyn projektin tapahtumien luettelosta.</span><span class="sxs-lookup"><span data-stu-id="a7a50-126">You can create invoice proposals by manually selecting from a list of transactions for a specified project.</span></span> <span data-ttu-id="a7a50-127">Voit määrittää laskutuksen säännöt, jotka määrittävät milloin laskuehdotus luodaan automaattisesti.</span><span class="sxs-lookup"><span data-stu-id="a7a50-127">You can also set up billing rules that specify when to automatically create an invoice proposal.</span></span> <span data-ttu-id="a7a50-128">Voit esimerkiksi luoda laskutussäännön laskuehdotuksen luomiseksi, kun projektin työstä on suoritettu 25 %, 50 %, 75 % ja 100 %.</span><span class="sxs-lookup"><span data-stu-id="a7a50-128">For example, you can create a billing rule to create an invoice proposal when work on a project is 25 percent, 50 percent, 75 percent, and 100 percent completed.</span></span> 

<span data-ttu-id="a7a50-129">Voit luoda laskuehdotukset seuraaville tapahtumille:</span><span class="sxs-lookup"><span data-stu-id="a7a50-129">You can create invoice proposals for the following transactions:</span></span>

-   <span data-ttu-id="a7a50-130">Tunnit, kulut ja muut projektitapahtumat</span><span class="sxs-lookup"><span data-stu-id="a7a50-130">Hours, expenses, and other project transactions</span></span>
-   <span data-ttu-id="a7a50-131">Summat, jotka asiakkaat ovat pidättäneet ennen projektilaskuja</span><span class="sxs-lookup"><span data-stu-id="a7a50-131">Amounts that are withheld by customers on previous project invoices</span></span>
-   <span data-ttu-id="a7a50-132">Hyvityslaskut</span><span class="sxs-lookup"><span data-stu-id="a7a50-132">Credit notes</span></span>
-   <span data-ttu-id="a7a50-133">Summat, jotka asiakas on maksanut ennen projektin alkamista</span><span class="sxs-lookup"><span data-stu-id="a7a50-133">Amounts that a customer paid to you before a project is started</span></span>

<span data-ttu-id="a7a50-134">Voit luoda laskuehdotuksen maksutapahtumat.</span><span class="sxs-lookup"><span data-stu-id="a7a50-134">You can create fee transactions in an invoice proposal.</span></span> <span data-ttu-id="a7a50-135">Voit myös muokata myyntihintaa tunti-, nimike- ja maksutapahtumissa.</span><span class="sxs-lookup"><span data-stu-id="a7a50-135">You can also modify the sales price on hour, expense, item, and fee transactions.</span></span> <span data-ttu-id="a7a50-136">Jos kirjaat laskuehdotuksen, päivitetyt hinnat ja tapahtumat lisätään projektiraportteihin ja tapahtumien historiatietoihin.</span><span class="sxs-lookup"><span data-stu-id="a7a50-136">When you post an invoice proposal, the updated prices and transactions are added to project reports and the transaction history.</span></span> 

<span data-ttu-id="a7a50-137">Voit halutessasi luoda useita asiakaslaskuja projektille luomalla kullekin laskulle laskuehdotuksen.</span><span class="sxs-lookup"><span data-stu-id="a7a50-137">To create multiple customer invoices for a project, you must create an invoice proposal for each invoice.</span></span> <span data-ttu-id="a7a50-138">Voit esimerkiksi luoda laskuja tapahtumatyypin perusteella.</span><span class="sxs-lookup"><span data-stu-id="a7a50-138">For example, you can create invoices based on transaction type.</span></span> <span data-ttu-id="a7a50-139">Voit määrittää tunnit yhteen myyntilaskuun ja nimikkeet toiseen laskuun luomalla tuntitapahtumille ja maksutapahtumille laskuehdotukset.</span><span class="sxs-lookup"><span data-stu-id="a7a50-139">To specify hours on one customer invoice and items on another, you must create separate invoice proposals for hour transactions and fee transactions.</span></span> 

<span data-ttu-id="a7a50-140">Jos projektilla on enemmän kuin yksi rahoituslähde, voit luoda kullekin rahoituslähteelle erillisen laskuehdotuksen.</span><span class="sxs-lookup"><span data-stu-id="a7a50-140">If a project has more than one funding source, you can create a separate invoice proposal for each funding source.</span></span> <span data-ttu-id="a7a50-141">Voit määrittää **Rahoitussäännön kohdistukset** -sivulla tapahtumasumman prosenttiosuuden, joka kohdistetaan kullekin rahoituslähteelle, ja lähteen, johon pyöristyserot kirjataan.</span><span class="sxs-lookup"><span data-stu-id="a7a50-141">On the **Funding rule allocations** page, you can define the percentage of the transaction amount to allocate to each funding source, and the source to post rounding differences.</span></span>

### <a name="creating-customer-invoices-from-invoice-proposals"></a><span data-ttu-id="a7a50-142">Myyntilaskujen luominen laskuehdotuksista</span><span class="sxs-lookup"><span data-stu-id="a7a50-142">Creating customer invoices from invoice proposals</span></span>

<span data-ttu-id="a7a50-143">Kun olet luonut ja kirjannut laskuehdotuksen, laskuehdotukseen sisältyville tapahtumille luodaan automaattisesti myyntilasku.</span><span class="sxs-lookup"><span data-stu-id="a7a50-143">After you create and post an invoice proposal, a customer invoice is automatically created for the transactions that are included in the invoice proposal.</span></span> 

<span data-ttu-id="a7a50-144">Voit lisätä tapahtumia laskuehdotukseen tai poistaa niitä laskuehdotuksesta ennen laskuehdotuksen kirjaamista.</span><span class="sxs-lookup"><span data-stu-id="a7a50-144">Before you post an invoice proposal, you can add transactions to it or delete transactions from it.</span></span> <span data-ttu-id="a7a50-145">Voit esimerkiksi poistaa kulutapahtumat, jotka kirjattiin projektiin mutta joita ei voi laskuttaa asiakkaalta.</span><span class="sxs-lookup"><span data-stu-id="a7a50-145">For example, you can remove expense transactions that were posted to a project, but that are not chargeable to the customer.</span></span> 

<span data-ttu-id="a7a50-146">Jos organisaatio edellyttää laskuehdotuksien tarkistamista ennen niiden kirjaamista, laskuehdotus saattaa edellyttää hyväksymistä projektin laskuehdotuksen tarkistuksen työnkulun kautta, ennen kuin se kirjataan.</span><span class="sxs-lookup"><span data-stu-id="a7a50-146">If your organization requires that invoice proposals be reviewed before they are posted, the invoice proposal might need to be approved through the "Review project invoice proposals" workflow before it is posted.</span></span>

## <a name="on-account-invoicing"></a><span data-ttu-id="a7a50-147">Ennakkolaskutus</span><span class="sxs-lookup"><span data-stu-id="a7a50-147">On-account invoicing</span></span>
<span data-ttu-id="a7a50-148">Summa, jonka kirjaat projektin ennakkolaskulle, perustuu ajoitukseen, valmistumisprosenttiin ja muihin laskutusehtoihin, jotka on määritetty liittyvässä projektisopimuksessa.</span><span class="sxs-lookup"><span data-stu-id="a7a50-148">The amount that you enter for a project in an on-account invoice is based on the timing, percentage of completion, and other billing conditions that are specified in the related project contract.</span></span> <span data-ttu-id="a7a50-149">Summaa ei lasketa projektiin kirjattujen tuntien, nimikkeiden, kulujen tai maksujen perusteella.</span><span class="sxs-lookup"><span data-stu-id="a7a50-149">The amount is not calculated based on the hours, items, expenses, or fees that are posted to the project.</span></span> 

<span data-ttu-id="a7a50-150">Sinun on luotava ennakkomaksutapahtuma kiinteähintaiselle projektille tai aika ja materiaali -projektille ennen kyseisen ennakkomaksutapahtuman lisäämistä projektilaskuun.</span><span class="sxs-lookup"><span data-stu-id="a7a50-150">You must create an on-account transaction for a Time and material project or a Fixed-price project before you can add that on-account transaction to a project invoice.</span></span> <span data-ttu-id="a7a50-151">Kirjoita ennakkolaskutustapahtumaan asiakkaalta laskutettava summa.</span><span class="sxs-lookup"><span data-stu-id="a7a50-151">On the on-account transaction, enter the amount to invoice a customer.</span></span> <span data-ttu-id="a7a50-152">Jos haluat luoda projektilaskun, luo alustava lasku (laskuehdotus).</span><span class="sxs-lookup"><span data-stu-id="a7a50-152">To create a project invoice for the amount, create a preliminary invoice (invoice proposal).</span></span> <span data-ttu-id="a7a50-153">Valitse ennakkotapahtuma laskuehdotuksessa.</span><span class="sxs-lookup"><span data-stu-id="a7a50-153">In the invoice proposal, select the on-account transaction.</span></span> <span data-ttu-id="a7a50-154">Voit tarkastaa ennakkolaskun tiedot laskuehdotuksesta, ennen kuin luot projektilaskun siitä.</span><span class="sxs-lookup"><span data-stu-id="a7a50-154">You can review the on-account information in the invoice proposal before you create a project invoice for it.</span></span>

### <a name="fixed-price-projects"></a><span data-ttu-id="a7a50-155">Kiinteähintaiset projektit</span><span class="sxs-lookup"><span data-stu-id="a7a50-155">Fixed-price projects</span></span>

<span data-ttu-id="a7a50-156">Kiinteähintaisissa projekteissa ennakkolaskutapahtumat perustuvat sovittuun välitavoitteeseen, toimitusyksikköön tai projektin sopimuksessa määritettyyn edistymiseen perustuvaan laskutusjärjestelyyn.</span><span class="sxs-lookup"><span data-stu-id="a7a50-156">For Fixed-price projects, on-account transactions are based on an agreed-upon milestone, unit of delivery, or progress billing arrangement that is specified in a project contract.</span></span> <span data-ttu-id="a7a50-157">Ohjelma luo rivin jokaiselle maksulle, joka tullaan vastaanottamaan projektiasiakkaalta.</span><span class="sxs-lookup"><span data-stu-id="a7a50-157">One line is created for each payment that must be received from the project customer.</span></span> <span data-ttu-id="a7a50-158">Vähennyksiä ei edellytetä.</span><span class="sxs-lookup"><span data-stu-id="a7a50-158">No deductions are required.</span></span>

### <a name="time-and-material-projects"></a><span data-ttu-id="a7a50-159">Aika- ja materiaaliprojektit</span><span class="sxs-lookup"><span data-stu-id="a7a50-159">Time and material projects</span></span>

<span data-ttu-id="a7a50-160">Aika-ja materiaaliprojekteissa voit laskuttaa asiakasta tai toista rahoituslähdettä ennakkomaksun määrän käyttämällä ennakkolaskulaskuehdotusta.</span><span class="sxs-lookup"><span data-stu-id="a7a50-160">For Time and material projects, you can bill a customer or other funding source for a prepayment amount by using an on-account invoice proposal.</span></span> <span data-ttu-id="a7a50-161">Kirjoita ennakkolaskutapahtumat yhdellä rivillä</span><span class="sxs-lookup"><span data-stu-id="a7a50-161">Enter on-account transactions as one line.</span></span> <span data-ttu-id="a7a50-162">Voit halutessasi lisätä lisärivejä vähennyksinä vastakirjataksesi kaikki ennakkomaksut, jotka asiakas on tehnyt.</span><span class="sxs-lookup"><span data-stu-id="a7a50-162">You can optionally enter additional lines as deductions to offset any prepayments that the customer has already made.</span></span> <span data-ttu-id="a7a50-163">Voit luoda vähennysrivit lisäämällä niiden eteen miinusmerkin.</span><span class="sxs-lookup"><span data-stu-id="a7a50-163">To create deduction lines, precede the amount with a minus sign.</span></span>

## <a name="invoice-control"></a><span data-ttu-id="a7a50-164">Laskutuksen hallinta</span><span class="sxs-lookup"><span data-stu-id="a7a50-164">Invoice control</span></span>
<span data-ttu-id="a7a50-165">Voit seurata laskun hallinnalla sekä laskutettuja että laskuttamattomia tapahtumia ja analysoida kyseisiä tapahtumia vertaamalla niitä tarjouksiin. Saat tällä tavoin kattavan näkemyksen projekteista tarjousvaiheesta valmistumiseen.</span><span class="sxs-lookup"><span data-stu-id="a7a50-165">You can use invoice control to track both invoiced and non-invoiced transactions, and to analyze those transactions against quotations for an end-to-end view of your projects from the quotation stage to completion.</span></span> <span data-ttu-id="a7a50-166">Näet, mitkä tapahtumat on veloitettu tietylle projektille ja mitkä rivit on laskutettu.</span><span class="sxs-lookup"><span data-stu-id="a7a50-166">You can see which transactions have been charged to a specific project and which lines have been invoiced.</span></span> <span data-ttu-id="a7a50-167">Voit tarkastella myös yksittäisiä tapahtumia, joten voit oikaista niitä kirjaamisen jälkeen.</span><span class="sxs-lookup"><span data-stu-id="a7a50-167">You can also view individual transactions, so that you can adjust them after they are posted.</span></span>

## <a name="invoicing-fixed-price-projects"></a><span data-ttu-id="a7a50-168">Kiinteähintaisten projektien laskuttaminen</span><span class="sxs-lookup"><span data-stu-id="a7a50-168">Invoicing Fixed-price projects</span></span>
<span data-ttu-id="a7a50-169">Kiinteähintaisen projektin laskuttaminen edellyttää laskutusaikataulun määrittämistä ja laskutusmenettelyn suorittamista.</span><span class="sxs-lookup"><span data-stu-id="a7a50-169">To invoice a Fixed-price project, you must define a billing schedule and complete the invoicing procedure.</span></span>

### <a name="billing-schedule"></a><span data-ttu-id="a7a50-170">Laskutusaikataulu</span><span class="sxs-lookup"><span data-stu-id="a7a50-170">Billing schedule</span></span>

<span data-ttu-id="a7a50-171">Voit laskuttaa kiinteähintaiset projektit laskutusaikataulun mukaisesti.</span><span class="sxs-lookup"><span data-stu-id="a7a50-171">You can invoice Fixed-price projects on a billing schedule.</span></span> <span data-ttu-id="a7a50-172">Laskutusaikataulu määritetään projektin välitavoitteiden mukaan, joita voi olla yksi tai useita.</span><span class="sxs-lookup"><span data-stu-id="a7a50-172">The billing schedule is defined in terms of one or more milestones for the project.</span></span> <span data-ttu-id="a7a50-173">Jokaiselle välitavoitteelle määritetään tietty päivämäärä, myyntivaluutta, myyntihinta ja tehtävä.</span><span class="sxs-lookup"><span data-stu-id="a7a50-173">For each milestone, you can define a specific date, sales currency, sales price, and activity.</span></span> 

<span data-ttu-id="a7a50-174">Voit esimerkiksi määrittää seuraavan laskutusaikataulun:</span><span class="sxs-lookup"><span data-stu-id="a7a50-174">For example, you can set up the following billing schedule:</span></span>

-   <span data-ttu-id="a7a50-175">20 prosenttia, kun projektisopimus allekirjoitetaan</span><span class="sxs-lookup"><span data-stu-id="a7a50-175">20 percent when the project contract is signed</span></span>
-   <span data-ttu-id="a7a50-176">30 prosenttia ensimmäisen toimituksen yhteydessä</span><span class="sxs-lookup"><span data-stu-id="a7a50-176">30 percent on first delivery</span></span>
-   <span data-ttu-id="a7a50-177">15 prosentti toisen toimituksen yhteydessä</span><span class="sxs-lookup"><span data-stu-id="a7a50-177">15 percent on second delivery</span></span>
-   <span data-ttu-id="a7a50-178">35 prosenttia viimeisen toimituksen yhteydessä</span><span class="sxs-lookup"><span data-stu-id="a7a50-178">35 percent on final delivery</span></span>

### <a name="invoicing-procedure"></a><span data-ttu-id="a7a50-179">Laskutusmenettely</span><span class="sxs-lookup"><span data-stu-id="a7a50-179">Invoicing procedure</span></span>

<span data-ttu-id="a7a50-180">Kun välitavoitemaksut ovat valmiita laskutettaviksi, käytetään ennakkosummien laskutustapaa.</span><span class="sxs-lookup"><span data-stu-id="a7a50-180">When the milestone payments are ready to be invoiced, you use the procedure for invoicing on-account amounts.</span></span>

## <a name="vendor-invoicing"></a><span data-ttu-id="a7a50-181">Toimittajan laskutus</span><span class="sxs-lookup"><span data-stu-id="a7a50-181">Vendor invoicing</span></span>
<span data-ttu-id="a7a50-182">Kun tilaat nimikkeen toimittajalta ja määrität nimikkeen projektiin, kyseisen nimikkeen ostotilausriville valittu riviominaisuus määrittää, laskutetaanko ostettu nimike asiakkaalle.</span><span class="sxs-lookup"><span data-stu-id="a7a50-182">When you order an item from a vendor and assign the item to a project, the line property that you select for the purchase order line for that item determines whether the purchased item is invoiced to a customer.</span></span> <span data-ttu-id="a7a50-183">Jos määrität oletusriviominaisuudet, ne näytetään nimikkeelle ostotilausrivillä (Rivin erittely &gt; Projekti &gt; Rivin ominaisuus).</span><span class="sxs-lookup"><span data-stu-id="a7a50-183">If you set up default line properties, they are displayed for the item on the purchase order line (Line details &gt; Project &gt; Line property).</span></span> <span data-ttu-id="a7a50-184">Riviominaisuutta voi muokata kahdella tavalla:</span><span class="sxs-lookup"><span data-stu-id="a7a50-184">There are two ways to modify the line property:</span></span>

-   <span data-ttu-id="a7a50-185">Projektin asiakasta laskutetaan nimikkeestä: määritä nimikkeen riviominaisuus veloitettavalle arvolle ostotilauksessa ja laskuta sitten asiakasta oikealla projektilaskutustavalla.</span><span class="sxs-lookup"><span data-stu-id="a7a50-185">Invoice the project's customer for the item: Set the line property for the item to a chargeable value on the purchase order, and then invoice the customer by using the correct project invoicing method.</span></span>
-   <span data-ttu-id="a7a50-186">Projektin asiakasta ei laskuteta nimikkeestä: Älä valitse nimikkeen ostotilausrivin **Veloitettava**-riviominaisuutta.</span><span class="sxs-lookup"><span data-stu-id="a7a50-186">Don’t invoice the project's customer for the item: Don’t select the **Chargeable** line property on the purchase order line for the item.</span></span> <span data-ttu-id="a7a50-187">Voit sitten laskuttaa ostotilauksen eikä muita toimintoja tarvita.</span><span class="sxs-lookup"><span data-stu-id="a7a50-187">You can then invoice the purchase order, and no further action is required.</span></span>

## <a name="credit-notes"></a><span data-ttu-id="a7a50-188">Hyvityslaskut</span><span class="sxs-lookup"><span data-stu-id="a7a50-188">Credit notes</span></span>
<span data-ttu-id="a7a50-189">Kun myyntilaskun summana on negatiivinen arvo, lasku luokitellaan hyvityslaskuksi.</span><span class="sxs-lookup"><span data-stu-id="a7a50-189">When an amount on a customer invoice has a negative value, the invoice is classified as a credit note.</span></span> <span data-ttu-id="a7a50-190">Kun asiakirja tulostetaan, sen otsikkona on Hyvityslasku.</span><span class="sxs-lookup"><span data-stu-id="a7a50-190">When the document is printed, it has the title "Credit note."</span></span> 

<span data-ttu-id="a7a50-191">Kun luot hyvityslaskun aiemmin laskutetun summan hyvittämistä varten, laskutettu summa on ensin valittava hyvittämistä varten.</span><span class="sxs-lookup"><span data-stu-id="a7a50-191">When you create a credit note to credit an amount that was previously invoiced, you must first select the invoiced amount for crediting.</span></span> <span data-ttu-id="a7a50-192">Voit sitten luoda hyvityslaskun samalla tavalla kuin loisit tavallinen myyntilaskun.</span><span class="sxs-lookup"><span data-stu-id="a7a50-192">You then create a credit note by following the same procedure that you would use to create an ordinary customer invoice.</span></span> <span data-ttu-id="a7a50-193">Valitset siis tapahtumat, jotka kirjattiin aiemmin myyntilaskulle, ja luot ja kirjaat sitten hyvityslaskuehdotuksen.</span><span class="sxs-lookup"><span data-stu-id="a7a50-193">In other words, you select the transactions that were previously posted on a customer invoice, and then create and post a credit note proposal.</span></span> 

<span data-ttu-id="a7a50-194">Sama asiakirja voi sisältää tapahtumat, jotka on valittu hyvitettäviksi, hyvitystapahtumia ja tapahtumia, jotka on kirjattu.</span><span class="sxs-lookup"><span data-stu-id="a7a50-194">The same document can include transactions that are selected for crediting, credit transactions, and transactions that have been posted.</span></span> <span data-ttu-id="a7a50-195">Asiakirja luokitellaan joko laskuksi tai hyvityslaskuksi sen mukaan, onko kokonaissumma positiivinen vai negatiivinen luku.</span><span class="sxs-lookup"><span data-stu-id="a7a50-195">The document is classified as either an invoice or a credit note, depending on whether the total amount is positive or negative.</span></span> 

<span data-ttu-id="a7a50-196">Jos haluat hyvittää laskutetun summan, laskutettu summa on ensin valittava hyvittämistä varten, jonka jälkeen luodaan uusi hyvityslasku.</span><span class="sxs-lookup"><span data-stu-id="a7a50-196">To credit an invoiced amount, you first select the invoiced amount to credit and then create a credit note.</span></span> <span data-ttu-id="a7a50-197">Voit luoda hyvityslaskun samalla tavoin kuin loisit myyntilaskun.</span><span class="sxs-lookup"><span data-stu-id="a7a50-197">You create a credit note by following the same procedure that you would use to generate a customer invoice.</span></span> 

<span data-ttu-id="a7a50-198">Voit luoda laskun, jossa on negatiivinen summa ja josta tulee hyvityslaskuksi luokiteltava lasku.</span><span class="sxs-lookup"><span data-stu-id="a7a50-198">You can create an invoice that has a negative amount, which becomes an invoice that is classified as a credit note.</span></span> <span data-ttu-id="a7a50-199">Jos haluat luoda ja tulostaa hyvityslaskun, sinun on valittava tapahtumat, jotka kirjattiin aiemmin myyntilaskulle ja muokattava sitten tapahtumia.</span><span class="sxs-lookup"><span data-stu-id="a7a50-199">To create and print a credit note, you must select the transactions that were previously posted for a customer invoice, and then modify the transactions.</span></span> <span data-ttu-id="a7a50-200">Laskun otsikko on Korjaava lasku, ellei yrityksen ensisijainen osoite ole Saksassa.</span><span class="sxs-lookup"><span data-stu-id="a7a50-200">Unless the primary address of the legal entity is in Germany, the title of the invoice will be "Corrective invoice."</span></span>


