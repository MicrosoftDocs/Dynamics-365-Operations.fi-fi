---
title: Tekstimuotoisten laskujen kirjanpidolliset jaot ja kirjauskansioviennit
description: Kirjanpidollisia jakoja käytetään määritettäessä summan käsittely, kuten esimerkiksi se, miten tuottoa, veroa tai maksua käsitellään vapaatekstilaskussa. Jokaisella määrällä, joka on huomioitava vapaatekstilaskun kirjauksen yhteydessä, on yksi tai useampi kirjanpidollinen jako.
author: ShivamPandey-msft
ms.date: 08/22/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CustFreeInvoice
audience: Application User
ms.reviewer: roschlom
ms.custom: 3141
ms.assetid: fecd17a2-d7b4-4a20-ac81-eb71abbfa9d1
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9c3609ed396b543bb708ea36f308eee60976e66f
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/01/2021
ms.locfileid: "5837174"
---
# <a name="accounting-distributions-and-subledger-entries-for-free-text-invoices"></a><span data-ttu-id="adfec-104">Tekstimuotoisten laskujen kirjanpidolliset jaot ja alareskontran viennit</span><span class="sxs-lookup"><span data-stu-id="adfec-104">Accounting distributions and subledger entries for free text invoices</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="adfec-105">Kirjanpidollisia jakoja käytetään määritettäessä summan käsittely, kuten esimerkiksi se, miten tuottoa, veroa tai maksua käsitellään vapaatekstilaskussa.</span><span class="sxs-lookup"><span data-stu-id="adfec-105">Accounting distributions are used to define how an amount will be accounted for, such as how the revenue, tax, or charges will be accounted for on a free text invoice.</span></span> <span data-ttu-id="adfec-106">Jokaisella määrällä, joka on huomioitava vapaatekstilaskun kirjauksen yhteydessä, on yksi tai useampi kirjanpidollinen jako.</span><span class="sxs-lookup"><span data-stu-id="adfec-106">Every amount that must be accounted for when the free text invoice is journalized will have one or more accounting distributions.</span></span>

<a name="accounting-distributions"></a><span data-ttu-id="adfec-107">Kirjanpidolliset jaot</span><span class="sxs-lookup"><span data-stu-id="adfec-107">Accounting distributions</span></span>
------------------------

<span data-ttu-id="adfec-108">Seuraavilla Vapaatekstilasku-sivun painikkeilla voit tarkastella ja mahdollisesti muokata kirjanpidollisia jakoja kullekin vapaatekstilaskun summalle.</span><span class="sxs-lookup"><span data-stu-id="adfec-108">You can use the following buttons in the Free text invoice page to view, and possibly change, the accounting distributions for each amount on the free text invoice.</span></span>

-   <span data-ttu-id="adfec-109">**Jaa summat** – Tarkastele ja muuta yksittäisen rivin ja sen alarivien, kuten verojen tai kulujen, kirjanpidollisia jakoja.</span><span class="sxs-lookup"><span data-stu-id="adfec-109">**Distribute amounts**—View and change the accounting distributions for an individual line and any child lines, such as taxes or charges.</span></span> <span data-ttu-id="adfec-110">Voit tarkastella ja muuttaa alarivin kirjanpidollisia jakoja myös suoraan Arvonlisäverotapahtumat- tai Kulutapahtumat-sivulla.</span><span class="sxs-lookup"><span data-stu-id="adfec-110">You can also view and change the accounting distributions for the child line directly from the Sales tax transactions page or the Charges transactions page.</span></span>
    -   <span data-ttu-id="adfec-111">Muuta vapaatekstilaskun otsikon summia, kuten kuluja tai valuutan pyöristyssummia.</span><span class="sxs-lookup"><span data-stu-id="adfec-111">Change free text invoice header amounts, such as charges or currency rounding amounts.</span></span>
    -   <span data-ttu-id="adfec-112">Muuta vapaatekstilaskun rivisummia.</span><span class="sxs-lookup"><span data-stu-id="adfec-112">Change free text invoice line amounts.</span></span>
-   <span data-ttu-id="adfec-113">**Näytä jakaumat** – Näytä asiakirjan kaikkien rivien kirjanpidolliset jaot.</span><span class="sxs-lookup"><span data-stu-id="adfec-113">**View distributions**—View the accounting distributions for all lines on the document.</span></span> <span data-ttu-id="adfec-114">Et voi muuttaa kirjanpidollisia jakoja tästä näkymästä.</span><span class="sxs-lookup"><span data-stu-id="adfec-114">You can't change the accounting distributions from this view.</span></span>
    -   <span data-ttu-id="adfec-115">Näytä otsikon ja rivien summat.</span><span class="sxs-lookup"><span data-stu-id="adfec-115">View header and line amounts.</span></span>

## <a name="distributing-amounts"></a><span data-ttu-id="adfec-116">Summien jakaminen</span><span class="sxs-lookup"><span data-stu-id="adfec-116">Distributing amounts</span></span>
<span data-ttu-id="adfec-117">Kun annat vapaatekstilaskun, jokainen määrä jaetaan seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="adfec-117">When you enter a free text invoice, each amount will be distributed as follows.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="adfec-118">Kirjoita rahasumma</span><span class="sxs-lookup"><span data-stu-id="adfec-118">Type of monetary amount</span></span></th>
<th><span data-ttu-id="adfec-119">Mistä päätili näytetään</span><span class="sxs-lookup"><span data-stu-id="adfec-119">Where the main account is displayed from</span></span></th>
<th><span data-ttu-id="adfec-120">Tärkeysjärjestys, joka määrittää, mikä oletusarvoinen taloushallinnon dimensio tulee näkyviin.</span><span class="sxs-lookup"><span data-stu-id="adfec-120">Order of priority that determines which default financial dimension is displayed</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="adfec-121">Vapaatekstilaskun rivi</span><span class="sxs-lookup"><span data-stu-id="adfec-121">Free text invoice line</span></span></td>
<td><span data-ttu-id="adfec-122">Vapaatekstilaskurivin kirjanpitotili.</span><span class="sxs-lookup"><span data-stu-id="adfec-122">The ledger account on the free text invoice line.</span></span></td>
<td><ol>
<li><span data-ttu-id="adfec-123">Jos päätili on kohdistustili, käytä oletusarvoa kohdistustilin määrityksestä.</span><span class="sxs-lookup"><span data-stu-id="adfec-123">If the main account is an allocation account, use the default value from the allocation account definition.</span></span></li>
<li><span data-ttu-id="adfec-124">Jos päätili ei ole kohdistustili, käytä vapaatekstilaskun rivillä taloushallinnon dimension oletusmallia.</span><span class="sxs-lookup"><span data-stu-id="adfec-124">If the main account is not an allocation account, use the financial dimension default template on the free text invoice line.</span></span></li>
<li><span data-ttu-id="adfec-125">Käytä taloushallinnon dimension oletusarvoja vapaatekstilaskun rivillä.</span><span class="sxs-lookup"><span data-stu-id="adfec-125">Use the default financial dimension values on the free text invoice line.</span></span></li>
<li><span data-ttu-id="adfec-126">Käytä Tilikartta-sivun kirjanpitotilin taloushallinnon dimension oletusarvoja.</span><span class="sxs-lookup"><span data-stu-id="adfec-126">Use the default financial dimension values from the ledger account in the Chart of accounts page.</span></span></li>
</ol></td>
</tr>
<tr class="even">
<td><span data-ttu-id="adfec-127">Käyttöomaisuustunnuksen ja arvomallin yhdistelmän vapaatekstilaskun rivi</span><span class="sxs-lookup"><span data-stu-id="adfec-127">Free text invoice line for a fixed asset number and value model combination</span></span>
<div class="alert">
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="adfec-128"><strong>Huomautus </strong></span><span class="sxs-lookup"><span data-stu-id="adfec-128"><strong>Note</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="adfec-129">Vapaatekstilaskun rivin päätili on käyttöomaisuuden poistotili.</span><span class="sxs-lookup"><span data-stu-id="adfec-129">The main account on the free text invoice line will be the fixed asset disposal account.</span></span></td>
</tr>
</tbody>
</table>
</div></td>
<td><span data-ttu-id="adfec-130">Vapaatekstilaskurivin kirjanpitotili.</span><span class="sxs-lookup"><span data-stu-id="adfec-130">The ledger account on the free text invoice line.</span></span></td>
<td><ol>
<li><span data-ttu-id="adfec-131">Käytä taloushallinnon dimension oletusarvoja vapaatekstilaskun rivillä.</span><span class="sxs-lookup"><span data-stu-id="adfec-131">Use the default financial dimension values on the free text invoice line.</span></span></li>
<li><span data-ttu-id="adfec-132">Käytä Tilikartta-sivun kirjanpitotilin taloushallinnon dimension oletusarvoja.</span><span class="sxs-lookup"><span data-stu-id="adfec-132">Use the default financial dimension values from the ledger account in the Chart of accounts page.</span></span></li>
</ol></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="adfec-133">Vapaatekstilaskun alennussumman</span><span class="sxs-lookup"><span data-stu-id="adfec-133">Free text invoice discount amount</span></span></td>
<td><span data-ttu-id="adfec-134">Asiakkaan alennusten päätili -kenttä Käteisalennukset-sivulla.</span><span class="sxs-lookup"><span data-stu-id="adfec-134">The Main account for customer discounts field in the Cash discounts page.</span></span></td>
<td><ol>
<li><span data-ttu-id="adfec-135">Jos päätili on kohdistustili, käytä oletusarvoa kohdistustilin määrityksestä.</span><span class="sxs-lookup"><span data-stu-id="adfec-135">If the main account is an allocation account, use the default value from the allocation account definition.</span></span></li>
<li><span data-ttu-id="adfec-136">Jos päätili ei ole kohdistustili, käytä vapaatekstilaskun rivillä taloushallinnon dimension oletusmallia.</span><span class="sxs-lookup"><span data-stu-id="adfec-136">If the main account is not an allocation account, use the financial dimension default template on the free text invoice line.</span></span></li>
<li><span data-ttu-id="adfec-137">Käytä taloushallinnon dimension oletusarvoja vapaatekstilaskun rivillä.</span><span class="sxs-lookup"><span data-stu-id="adfec-137">Use the default financial dimension values on the free text invoice line.</span></span></li>
<li><span data-ttu-id="adfec-138">Käytä Tilikartta-sivun kirjanpitotilin taloushallinnon dimension oletusarvoja.</span><span class="sxs-lookup"><span data-stu-id="adfec-138">Use the default financial dimension values from the ledger account in the Chart of accounts page.</span></span></li>
</ol></td>
</tr>
<tr class="even">
<td><span data-ttu-id="adfec-139">Vapaatekstilaskun arvonlisäveron summa</span><span class="sxs-lookup"><span data-stu-id="adfec-139">Free text invoice sales tax amount</span></span></td>
<td><span data-ttu-id="adfec-140">Maksettava arvonlisävero -kenttä Kirjanpidon kirjausryhmät -sivulla.</span><span class="sxs-lookup"><span data-stu-id="adfec-140">The Sales tax payable field in the Ledger posting groups page.</span></span></td>
<td><ol>
<li><span data-ttu-id="adfec-141">Käytä taloushallinnon dimensioita, jotka on määritetty vapaatekstilaskun rivisummassa tai maksurivin summan jaossa.</span><span class="sxs-lookup"><span data-stu-id="adfec-141">Use the financial dimensions that are defined on the free text invoice line amount or the distributions for the charge line amount.</span></span></li>
<li><span data-ttu-id="adfec-142">Käytä taloushallinnon dimension oletusarvoja vapaatekstilaskun rivillä.</span><span class="sxs-lookup"><span data-stu-id="adfec-142">Use the default financial dimension values on the free text invoice line.</span></span></li>
<li><span data-ttu-id="adfec-143">Käytä Tilikartta-sivun kirjanpitotilin taloushallinnon dimension oletusarvoja.</span><span class="sxs-lookup"><span data-stu-id="adfec-143">Use the default financial dimension values from the ledger account in the Chart of accounts page.</span></span></li>
</ol></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="adfec-144">Vapaatekstilaskun maksurivin summa</span><span class="sxs-lookup"><span data-stu-id="adfec-144">Free text invoice charge line amount</span></span></td>
<td><span data-ttu-id="adfec-145">Kredit-tili-kenttä Kulujen koodi -sivulla.</span><span class="sxs-lookup"><span data-stu-id="adfec-145">The Credit account field in the Charges code page.</span></span></td>
<td><ol>
<li><span data-ttu-id="adfec-146">Jos päätili on kohdistustili, käytä oletusarvoa kohdistustilin määrityksestä.</span><span class="sxs-lookup"><span data-stu-id="adfec-146">If the main account is an allocation account, use the default value from the allocation account definition.</span></span></li>
<li><span data-ttu-id="adfec-147">Jos päätili ei ole kohdistustili, käytä vapaatekstilaskun rivillä taloushallinnon dimension oletusmallia.</span><span class="sxs-lookup"><span data-stu-id="adfec-147">If the main account is not an allocation account, use the financial dimension default template on the free text invoice line.</span></span></li>
<li><span data-ttu-id="adfec-148">Käytä taloushallinnon dimension oletusarvoja vapaatekstilaskun rivillä.</span><span class="sxs-lookup"><span data-stu-id="adfec-148">Use the default financial dimension values on the free text invoice line.</span></span></li>
<li><span data-ttu-id="adfec-149">Käytä Tilikartta-sivun kirjanpitotilin taloushallinnon dimension oletusarvoja.</span><span class="sxs-lookup"><span data-stu-id="adfec-149">Use the default financial dimension values from the ledger account in the Chart of accounts page.</span></span></li>
</ol></td>
</tr>
</tbody>
</table>

## <a name="distributing-taxes"></a><span data-ttu-id="adfec-150">Verojen jakaminen</span><span class="sxs-lookup"><span data-stu-id="adfec-150">Distributing taxes</span></span>
<span data-ttu-id="adfec-151">verojen kirjanpidollisia jakoja ei voi luoda ennen verojen laskentaa.</span><span class="sxs-lookup"><span data-stu-id="adfec-151">Accounting distributions for taxes cannot be created until taxes are calculated.</span></span> <span data-ttu-id="adfec-152">Jotta voit laskea arvonlisäverot, sinun on suoritettava jokin seuraavista Vapaatekstilasku-lomakkeen tehtävistä:</span><span class="sxs-lookup"><span data-stu-id="adfec-152">To calculate sales taxes, you must complete one of the following tasks in the Free text invoice form:</span></span>
-   <span data-ttu-id="adfec-153">Näytä arvonlisävero.</span><span class="sxs-lookup"><span data-stu-id="adfec-153">View the sales tax.</span></span>
-   <span data-ttu-id="adfec-154">Näytä laskun summa.</span><span class="sxs-lookup"><span data-stu-id="adfec-154">View the invoice total.</span></span>
-   <span data-ttu-id="adfec-155">Näytä kassavirta.</span><span class="sxs-lookup"><span data-stu-id="adfec-155">View the cash flow.</span></span>
-   <span data-ttu-id="adfec-156">Näytä koko vapaatekstilaskun kirjanpidolliset jaot.</span><span class="sxs-lookup"><span data-stu-id="adfec-156">View accounting distributions for the whole free text invoice.</span></span>
-   <span data-ttu-id="adfec-157">Näytä alareskontran kirjauskansio.</span><span class="sxs-lookup"><span data-stu-id="adfec-157">View the subledger journal.</span></span>

## <a name="subledger-journals-for-free-text-invoices"></a><span data-ttu-id="adfec-158"> Vapaatekstilaskujen alareskontran kirjauskansiot</span><span class="sxs-lookup"><span data-stu-id="adfec-158">Subledger journals for free text invoices</span></span>
<span data-ttu-id="adfec-159">Ennen kuin kirjaat vapaatekstilaskun, voit tarkastella laskun koko kirjanpitokirjausta, joka sisältää hyvitykset ja veloitukset, jotta voit varmistaa, että lasku kirjataan oikeille tileille.</span><span class="sxs-lookup"><span data-stu-id="adfec-159">Before you post a free text invoice, you can view the full accounting entry of the invoice, which includes debits and credits, to verify that the invoice is being posted to the correct accounts.</span></span> <span data-ttu-id="adfec-160">Tämä kirjanpitomerkinnän koko näkymä tunnetaan nimellä alareskontran kirjauskansio.</span><span class="sxs-lookup"><span data-stu-id="adfec-160">This view of the full accounting entry is called a subledger journal.</span></span> <span data-ttu-id="adfec-161">Jos alareskontran kirjauskansiovienti on virheellinen esikatselussa, et voi muuttaa sitä ennen kuin kirjaat vapaatekstilaskun.</span><span class="sxs-lookup"><span data-stu-id="adfec-161">If the subledger journal entry is incorrect when you preview it before you journalize the free text invoice, you can't change the subledger journal entry.</span></span> <span data-ttu-id="adfec-162">Sen sijaan sinun on muutettava kirjanpidollisia jakoja tai kirjausprofiilia.</span><span class="sxs-lookup"><span data-stu-id="adfec-162">Instead, you must change the accounting distributions or the posting profile.</span></span> <span data-ttu-id="adfec-163">Kirjanpidollisia jakoja käytetään määrittämään yksi kirjanpitomerkinnän puolista, debet tai kredit.</span><span class="sxs-lookup"><span data-stu-id="adfec-163">The accounting distributions are used to define one side of the accounting entry, the debit or the credit.</span></span> <span data-ttu-id="adfec-164">Alareskontran kirjauskansion kirjanpitoviennin vastakirjaus luodaan kirjausprofiileista, kuten asiakastilistä tai verosta.</span><span class="sxs-lookup"><span data-stu-id="adfec-164">The offsetting subledger journal account entry is created from the posting profiles, such as from the customer account or the tax.</span></span>





[!INCLUDE[footer-include](../../includes/footer-banner.md)]