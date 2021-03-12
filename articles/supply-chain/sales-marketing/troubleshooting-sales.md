---
title: Myyntitilausten vianmääritys
description: Tässä ohjeaiheessa käsitellään sellaisten ongelmien korjaamista, joita myyntitilausten käytössä voi esiintyä.
author: SmithaNataraj
manager: tfehr
ms.date: 09/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SalesTable, SalesTableListPage, SalesTableListPage_SalesCancelOrder
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: smnatara
ms.search.validFrom: 2020-9-16
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: c9a5b7a5e8cac7f8816233dd2d7ff1a7f84ea480
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/15/2021
ms.locfileid: "4974782"
---
# <a name="troubleshoot-sales-orders"></a><span data-ttu-id="ef529-103">Myyntitilausten vianmääritys</span><span class="sxs-lookup"><span data-stu-id="ef529-103">Troubleshoot sales orders</span></span>

<span data-ttu-id="ef529-104">Tässä ohjeaiheessa käsitellään sellaisten ongelmien korjaamista, joita myyntitilausten käytössä voi esiintyä.</span><span class="sxs-lookup"><span data-stu-id="ef529-104">This topic describes how to fix issues that you might encounter while you work with sales orders.</span></span>

## <a name="the-tax-information-isnt-updated-if-i-change-the-location-on-a-sales-order-header"></a><span data-ttu-id="ef529-105">Verotietoja ei päivitetä, jos myyntitilauksen otsikon sijaintia muutetaan.</span><span class="sxs-lookup"><span data-stu-id="ef529-105">The tax information isn't updated if I change the location on a sales order header.</span></span>

### <a name="issue-description"></a><span data-ttu-id="ef529-106">Ongelman kuvaus</span><span class="sxs-lookup"><span data-stu-id="ef529-106">Issue description</span></span>

<span data-ttu-id="ef529-107">Jos toimipaikkaa, varastoa tai toimitusositetta muutetaan joko myyntitilauksen otsikossa tai rivitasolla, tapauksen verotietoja ei päivitetä riveillä automaattisesti.</span><span class="sxs-lookup"><span data-stu-id="ef529-107">If the site, warehouse, or delivery address is changed either on a sales order header or at the line level, the case tax information isn't automatically updated for the lines.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="ef529-108">Ongelman ratkaisu</span><span class="sxs-lookup"><span data-stu-id="ef529-108">Issue resolution</span></span>

<span data-ttu-id="ef529-109">Tämä on suunniteltu ominaisuus.</span><span class="sxs-lookup"><span data-stu-id="ef529-109">This behavior is by design.</span></span> <span data-ttu-id="ef529-110">Ongelma ilmenee, koska toimitusosoitetta, toimipaikkaa ja varastoa ei muuteta automaattisesti myöskään rivitasolla.</span><span class="sxs-lookup"><span data-stu-id="ef529-110">The issue occurs because the delivery address, site, and warehouse aren't automatically changed at the line level either.</span></span> <span data-ttu-id="ef529-111">Ne on päivitettävä manuaalisesti.</span><span class="sxs-lookup"><span data-stu-id="ef529-111">You must update them manually.</span></span>

## <a name="if-there-are-two-trade-agreements-for-the-same-period-or-overlapping-periods-the-same-agreement-line-is-always-selected"></a><span data-ttu-id="ef529-112">Jos samalle jaksolle tai päällekkäisille jakosoille on kaksi kauppasopimusta, valitaan aina sama sopimusrivi.</span><span class="sxs-lookup"><span data-stu-id="ef529-112">If there are two trade agreements for the same period or overlapping periods, the same agreement line is always selected.</span></span>

### <a name="issue-description"></a><span data-ttu-id="ef529-113">Ongelman kuvaus</span><span class="sxs-lookup"><span data-stu-id="ef529-113">Issue description</span></span>

<span data-ttu-id="ef529-114">Jos samalle jaksolle tai päällekkäisille jakosoille on määritetty kaksi kauppasopimusta, vaikuttaa siltä, että sama kauppasopimus valitaan aina, kun luot asianomaisia nimikkeitä sisältäviä myyntitilausrivejä.</span><span class="sxs-lookup"><span data-stu-id="ef529-114">If two trade agreements are defined for the same period or overlapping periods, the same trade agreement seems to be selected every time when you create sales order lines that contain those items.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="ef529-115">Ongelman ratkaisu</span><span class="sxs-lookup"><span data-stu-id="ef529-115">Issue resolution</span></span>

<span data-ttu-id="ef529-116">Jos tietylle päivälle on useita kauppasopimuksia, valitaan aina matalimman hinnan kauppasopimus.</span><span class="sxs-lookup"><span data-stu-id="ef529-116">If there is more than one trade agreement for a given date, the trade agreement that has the lowest price is always selected.</span></span> <span data-ttu-id="ef529-117">Lisä tietoja saat lataamalla seuraavan teknisen raportin: [Kauppasopimukset Microsoft Dynamics AX 2012:ssa](https://www.axug.com/HigherLogic/System/DownloadDocumentFile.ashx?DocumentFileKey=3396a3a8-1f48-4d85-8cd6-5fa982f62e90).</span><span class="sxs-lookup"><span data-stu-id="ef529-117">For more information, download the following white paper: [Trade agreements in Microsoft Dynamics AX 2012](https://www.axug.com/HigherLogic/System/DownloadDocumentFile.ashx?DocumentFileKey=3396a3a8-1f48-4d85-8cd6-5fa982f62e90).</span></span>

## <a name="can-i-link-a-purchase-order-to-a-sales-order-to-fulfill-demand"></a><span data-ttu-id="ef529-118">Voinko linkittää ostotilauksen myyntitilaukseen kysynnän täyttämiseksi?</span><span class="sxs-lookup"><span data-stu-id="ef529-118">Can I link a purchase order to a sales order to fulfill demand?</span></span>

<span data-ttu-id="ef529-119">Voit luoda ostotilauksen myyntitilauksesta.</span><span class="sxs-lookup"><span data-stu-id="ef529-119">You can create a purchase order from a sales order.</span></span> <span data-ttu-id="ef529-120">Lisätietoja: [Ostotilauksen luominen myyntitilauksesta](tasks/create-purchase-order-sales-order.md).</span><span class="sxs-lookup"><span data-stu-id="ef529-120">For more information, see [Create a purchase order from a sales order](tasks/create-purchase-order-sales-order.md).</span></span>

## <a name="i-cant-cancel-or-delete-a-return-order-or-a-sales-order"></a><span data-ttu-id="ef529-121">Palautustilausta tai myyntitilausta ei voi peruuttaa eikä poistaa.</span><span class="sxs-lookup"><span data-stu-id="ef529-121">I can't cancel or delete a return order or a sales order.</span></span>

<span data-ttu-id="ef529-122">Voit peruuttaa vain myynti- ja palautustilauksia, jotka ovat tilassa *Luotu*.</span><span class="sxs-lookup"><span data-stu-id="ef529-122">You can cancel only sales orders and return orders that are in a *Created* state.</span></span> <span data-ttu-id="ef529-123">Lisätietoja: [Palautustilauksen peruuttaminen](../service-management/cancel-return-order.md).</span><span class="sxs-lookup"><span data-stu-id="ef529-123">For more information, see [Cancel a return order](../service-management/cancel-return-order.md).</span></span>

## <a name="when-i-try-to-cancel-a-sales-order-i-receive-a-reservations-cannot-be-removed-because-there-is-work-created-which-relies-on-the-reservations-error"></a><span data-ttu-id="ef529-124">Kun yritän peruuttaa myyntitilauksen, näyttöön tulee virhe "Varauksia ei voi poistaa, koska on luotu töitä, jotka ovat riippuvaisia niistä".</span><span class="sxs-lookup"><span data-stu-id="ef529-124">When I try to cancel a sales order, I receive a "Reservations cannot be removed because there is work created which relies on the reservations" error.</span></span>

<span data-ttu-id="ef529-125">Virhekoodi: WAX4661</span><span class="sxs-lookup"><span data-stu-id="ef529-125">Error code: WAX4661</span></span>

<span data-ttu-id="ef529-126">Jos myyntitilaukseen liittyy työtä, et voi peruuttaa myyntitilausta, ennen kuin työ peruutetaan ja palautetaan.</span><span class="sxs-lookup"><span data-stu-id="ef529-126">If work is associated with a sales order, you can't cancel the sales order until the work is canceled and reversed.</span></span> <span data-ttu-id="ef529-127">Tämä vaatimus on pätee, vaikka myyntitilaukseen liittyvä työ olisi suljettu.</span><span class="sxs-lookup"><span data-stu-id="ef529-127">This requirement applies even if the work that is associated with the sales order is closed.</span></span>

<span data-ttu-id="ef529-128">Korjaa tämä ongelma seuraavien ohjeiden mukaisesti.</span><span class="sxs-lookup"><span data-stu-id="ef529-128">To fix this issue, follow these steps.</span></span>

1. <span data-ttu-id="ef529-129">Peruuta työ ja siirrä varasto takaisin haluttuun sijaintiin.</span><span class="sxs-lookup"><span data-stu-id="ef529-129">Cancel the work, and put inventory back into the desired location.</span></span> <span data-ttu-id="ef529-130">Siirry asianomaiseen myyntitilauksen kuormaan ja valitse joko **Vähennä kerättävää määrää** kuormarivillä tai **Palauta työ** toimintoruudussa.</span><span class="sxs-lookup"><span data-stu-id="ef529-130">Go to the relevant load of the sales order, and select either **Reduce picked quantity** on the load line or **Reverse work** on the Action Pane.</span></span>

    <span data-ttu-id="ef529-131">Työn tila on nyt *Peruutettu*, ja uusi varastosiirtotyö luodaan ja käsitellään automaattisesti, jotta varastonimikkeet palautetaan sijaintiin, joka kuvattiin palautuksen yhteydessä.</span><span class="sxs-lookup"><span data-stu-id="ef529-131">The work now has a status of *Canceled*, and new inventory movement work is automatically created and processed to put inventory back into the location that was described at the time of reversal.</span></span>

2. <span data-ttu-id="ef529-132">Poista kuorma.</span><span class="sxs-lookup"><span data-stu-id="ef529-132">Delete the load.</span></span> <span data-ttu-id="ef529-133">Myös lähetys poistetaan.</span><span class="sxs-lookup"><span data-stu-id="ef529-133">The shipment is also deleted.</span></span>
3. <span data-ttu-id="ef529-134">Nyt on pitäisi olla mahdollista siirtyä takaisin myyntitilaukseen ja perua se.</span><span class="sxs-lookup"><span data-stu-id="ef529-134">You should now be able to go to the sales order and cancel it.</span></span>

## <a name="i-cant-cancel-an-intercompany-purchase-order-that-is-linked-to-a-sales-order"></a><span data-ttu-id="ef529-135">En voi peruuttaa konsernin sisäistä ostotilausta, joka on linkitetty myyntitilaukseen.</span><span class="sxs-lookup"><span data-stu-id="ef529-135">I can't cancel an intercompany purchase order that is linked to a sales order.</span></span>

### <a name="issue-description"></a><span data-ttu-id="ef529-136">Ongelman kuvaus</span><span class="sxs-lookup"><span data-stu-id="ef529-136">Issue description</span></span>

<span data-ttu-id="ef529-137">Jos yrität peruuttaa myyntitilaukseen linkitetyn konsernin sisäisen ostotilauksen, näyttöön saattaa tulla seuraava virhesanoma: "Määrää ei voi vähentää, koska jäljelle jäävä päivitysmäärä muuttaa allekirjoitusta".</span><span class="sxs-lookup"><span data-stu-id="ef529-137">If you try to cancel an intercompany purchase order that is linked to a sales order, you might receive the following error message: "Quantity cannot be reduced because the remaining update quantity changes sign."</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="ef529-138">Ongelman ratkaisu</span><span class="sxs-lookup"><span data-stu-id="ef529-138">Issue resolution</span></span>

<span data-ttu-id="ef529-139">Tämä ongelma korjattiin Microsoft Dynamics 365 Supply Chain Managementin versiossa 10.0.13.</span><span class="sxs-lookup"><span data-stu-id="ef529-139">This issue was fixed in Microsoft Dynamics 365 Supply Chain Management version 10.0.13.</span></span> <span data-ttu-id="ef529-140">Tässä versiossa ja uudemmissa versioissa voit nyt peruuttaa konsernin sisäisen ostotilauksen, joka on linkitetty myyntitilaukseen.</span><span class="sxs-lookup"><span data-stu-id="ef529-140">In that version and later versions, you can now cancel an intercompany purchase order that is linked to a sales order.</span></span>

## <a name="can-i-restore-an-invoiced-sales-order-that-was-deleted"></a><span data-ttu-id="ef529-141">Voinko palauttaa poistetun laskutetun myyntitilauksen?</span><span class="sxs-lookup"><span data-stu-id="ef529-141">Can I restore an invoiced sales order that was deleted?</span></span>

### <a name="issue-description"></a><span data-ttu-id="ef529-142">Ongelman kuvaus</span><span class="sxs-lookup"><span data-stu-id="ef529-142">Issue description</span></span>

<span data-ttu-id="ef529-143">Laskutettu myyntitilaus poistettiin vahingossa, ja haluat palauttaa sen tai tarkastella sen tietoja.</span><span class="sxs-lookup"><span data-stu-id="ef529-143">An invoiced sales order was deleted by mistake, and you want to restore it or view its details.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="ef529-144">Ongelman ratkaisu</span><span class="sxs-lookup"><span data-stu-id="ef529-144">Issue resolution</span></span>

<span data-ttu-id="ef529-145">Jos poistettu myyntitilaus on jo laskutettu, siirry kohtaan **Asiakastili \> Tapahtumat \> Alkuperäinen asiakirja \> Näytä tiedot**.</span><span class="sxs-lookup"><span data-stu-id="ef529-145">If the deleted sales order has already been invoiced, go to **Customer account \> Transactions \> Original document \> View details**.</span></span> <span data-ttu-id="ef529-146">Etsi haluamasi lasku ja valitse se, jotta voit tarkastella sen tietoja.</span><span class="sxs-lookup"><span data-stu-id="ef529-146">Find the invoice that you're looking for, and select it to view its details.</span></span> <span data-ttu-id="ef529-147">Näihin tietoihin sisältyvät myyntitilauksen viite.</span><span class="sxs-lookup"><span data-stu-id="ef529-147">These details include the sales order reference.</span></span> <span data-ttu-id="ef529-148">Myös myyntitilauksen tietojen käytön pitäisi olla mahdollista kyseiseltä sivulta.</span><span class="sxs-lookup"><span data-stu-id="ef529-148">You should also be able to access the sales order details from that page.</span></span>

## <a name="the-deadline-of-a-sales-order-header-cant-be-found-in-the-salesorderheaderv2entity-data-entity"></a><span data-ttu-id="ef529-149">Myyntitilauksen otsikon määräaikaa ei löydy tietoentiteetistä SalesOrderHeaderV2Entity.</span><span class="sxs-lookup"><span data-stu-id="ef529-149">The deadline of a sales order header can't be found in the SalesOrderHeaderV2Entity data entity.</span></span>

<span data-ttu-id="ef529-150">Entiteetissä *SalesOrderHeaderV2Entiy* ei ole määräaikakenttää.</span><span class="sxs-lookup"><span data-stu-id="ef529-150">The deadline field doesn't exist on the *SalesOrderHeaderV2Entity* entity.</span></span>

## <a name="i-must-delete-orphaned-sales-order-records"></a><span data-ttu-id="ef529-151">Minun on poistettava orvoksi jääneet myyntitilaustietueet.</span><span class="sxs-lookup"><span data-stu-id="ef529-151">I must delete orphaned sales order records.</span></span>

<span data-ttu-id="ef529-152">Voit tyhjentää orvoksi jääneet myyntitilaustietueet suorittamalla säännöllisen *Myyntitilausten poisto* -tehtävän kummassa tahansa seuraavista paikoista:</span><span class="sxs-lookup"><span data-stu-id="ef529-152">To clean up orphaned sales order records, run the *Sales order deletion* periodic job by going to either of the following places:</span></span>

- <span data-ttu-id="ef529-153">Myynti ja markkinointi \> Säännölliset tehtävät \> Tyhjennä \> Poista myyntitilaukset</span><span class="sxs-lookup"><span data-stu-id="ef529-153">Sales and marketing \> Periodic tasks \> Clean up \> Delete sales orders</span></span>
- <span data-ttu-id="ef529-154">Vähittäismyynti ja kauppa \> Vähittäiskaupan ja kaupan IT \> Tyhjennä \> Poista myyntitilaukset</span><span class="sxs-lookup"><span data-stu-id="ef529-154">Retail and commerce \> Retail and commerce IT \> Clean up \> Delete sales orders</span></span>

## <a name="is-there-a-way-to-calculate-commissions-on-invoices-that-have-already-been-posted"></a><span data-ttu-id="ef529-155">Onko olemassa tapa laskea provisiot jo kirjatuista laskuista?</span><span class="sxs-lookup"><span data-stu-id="ef529-155">Is there a way to calculate commissions on invoices that have already been posted?</span></span>

<span data-ttu-id="ef529-156">Supply Chain Management ei tällä hetkellä tue kirjattujen laskujen provisioiden laskemista.</span><span class="sxs-lookup"><span data-stu-id="ef529-156">Supply Chain Management doesn't currently support the calculation of commissions for posted invoices.</span></span>

## <a name="a-bundle-item-isnt-supported-in-an-intercompany-process"></a><span data-ttu-id="ef529-157">Pakettinimikettä ei tueta konsernin sisäisissä prosesseissa.</span><span class="sxs-lookup"><span data-stu-id="ef529-157">A bundle item isn't supported in an intercompany process.</span></span>

<span data-ttu-id="ef529-158">Pakettinimike ei ole käytettävissä ostotilauksessa, koska jos tarkastelet pakettinimikkeen myyntitilaus rivejä, määrä on *0* (nolla) ja tila on *Peruutettu*.</span><span class="sxs-lookup"><span data-stu-id="ef529-158">The bundle item isn't available for the purchase order because, if you examine the sales order lines for the bundle item, you will notice that the quantity is *0* (zero) and the status is *Canceled*.</span></span> <span data-ttu-id="ef529-159">Tämä on suunniteltu ominaisuus.</span><span class="sxs-lookup"><span data-stu-id="ef529-159">This behavior is by design.</span></span> <span data-ttu-id="ef529-160">myyntitilauksella ostetaan vain pakettinimikkeen osat.</span><span class="sxs-lookup"><span data-stu-id="ef529-160">The sales order buys only the components of the bundle item.</span></span> <span data-ttu-id="ef529-161">Sillä ei osteta itse pakettinimikettä.</span><span class="sxs-lookup"><span data-stu-id="ef529-161">It doesn't buy the bundle item itself.</span></span>

<span data-ttu-id="ef529-162">Jos sinun on ostettava paketti, harkitse, pitääkö se merkitä pakettinimikkeeksi, koska tämä toiminto on suunniteltu tuottokirjausskenaarioita varten.</span><span class="sxs-lookup"><span data-stu-id="ef529-162">If you must buy a bundle, consider whether you have to mark it as bundle item, because this functionality is designed for revenue recognition scenarios.</span></span> <span data-ttu-id="ef529-163">Lisätietoja pakettinimikkeistä: [Paketit](../../finance/accounts-receivable/revenue-recognition-setup.md#bundles).</span><span class="sxs-lookup"><span data-stu-id="ef529-163">For more information about bundle items, see [Bundles](../../finance/accounts-receivable/revenue-recognition-setup.md#bundles).</span></span>
