---
title: Ostotilausten vianmääritys
description: Tässä ohjeaiheessa käsitellään sellaisten ongelmien korjaamista, joita ostotilausten käytössä voi esiintyä.
author: SmithaNataraj
manager: tfehr
ms.date: 09/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchTable, PurchTablePart
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: smnatara
ms.search.validFrom: 2020-9-16
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: 5959b098082ac1a0c8ea768795fa63b13950a9c7
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5242514"
---
# <a name="troubleshoot-purchase-orders"></a><span data-ttu-id="c9140-103">Ostotilausten vianmääritys</span><span class="sxs-lookup"><span data-stu-id="c9140-103">Troubleshoot purchase orders</span></span>

<span data-ttu-id="c9140-104">Tässä ohjeaiheessa käsitellään sellaisten ongelmien korjaamista, joita ostotilausten käytössä voi esiintyä.</span><span class="sxs-lookup"><span data-stu-id="c9140-104">This topic describes how to fix issues that you might encounter while you work with purchase orders.</span></span>

## <a name="an-action-can-be-completed-only-after-the-line-number-is-fully-distributed"></a><span data-ttu-id="c9140-105">Toimi voidaan suorittaa vasta, kun rivinumero on täysin jaeltu.</span><span class="sxs-lookup"><span data-stu-id="c9140-105">An action can be completed only after the line number is fully distributed.</span></span>

<span data-ttu-id="c9140-106">Tämä ongelma voi esiintyä, kun ostotilausten jaoissa on epäjohdonmukaisuuksia.</span><span class="sxs-lookup"><span data-stu-id="c9140-106">This issue can occur because of inconsistency in purchase order distributions.</span></span>

<span data-ttu-id="c9140-107">Voit poistaa tämän ongelman eston ja palauttaa ostotilauksen *Luonnos* siirtymällä kohtaan **Ostot ja hankinnat \> Säännölliset tehtävät \> Tyhjennys \> Ostotilauksen jaon palautus**.</span><span class="sxs-lookup"><span data-stu-id="c9140-107">To unblock this issue and reset the purchase order to a *Draft* state, go to **Procurement and sourcing \> Periodic tasks \> Clean up \> Purchase order distribution reset**.</span></span> <span data-ttu-id="c9140-108">Lisä tietoja on seuraavassa blogikirjoituksessa: [Ostotilausten jakovirheiden korjaaminen Dynamics 365 Supply Chain Managementissa](https://cloudblogs.microsoft.com/dynamics365/it/2020/08/12/resolve-po-distribution-errors-in-dynamics-365-supply-chain-management/).</span><span class="sxs-lookup"><span data-stu-id="c9140-108">For more information, see the following blog post: [Resolve PO distribution errors in Dynamics 365 Supply Chain Management](https://cloudblogs.microsoft.com/dynamics365/it/2020/08/12/resolve-po-distribution-errors-in-dynamics-365-supply-chain-management/).</span></span>

## <a name="when-purchase-orders-are-imported-through-data-management-purchase-order-line-numbers-dont-follow-the-increment-that-defined-in-system-parameters"></a><span data-ttu-id="c9140-109">Kun ostotilaukset tuodaan tiedonhallinnan kautta, ostotilausten rivi numerot eivät noudata järjestelmän parametreissa määritettyä korotusta.</span><span class="sxs-lookup"><span data-stu-id="c9140-109">When purchase orders are imported through data management, purchase order line numbers don't follow the increment that defined in system parameters.</span></span>

### <a name="issue-description"></a><span data-ttu-id="c9140-110">Ongelman kuvaus</span><span class="sxs-lookup"><span data-stu-id="c9140-110">Issue description</span></span>

<span data-ttu-id="c9140-111">Oletusarvoisesti automaattisesti luodut *Ostotilausrivit V2* -tietoyksikön kautta tuotujen tilausrivien rivinumerot eivät käytä järjestelmän parametreissa määritettyä rivinumeron korotusta.</span><span class="sxs-lookup"><span data-stu-id="c9140-111">By default, automatically generated line numbers for purchase order lines that are imported through the *Purchase order lines V2* data entity don't use the system line number increment that is specified in system parameters.</span></span> <span data-ttu-id="c9140-112">Jos luot ostotilauksen manuaalisesti ja lisäät rivejä käyttöliittymän kautta, rivinumerot kasvavat oikein.</span><span class="sxs-lookup"><span data-stu-id="c9140-112">If you manually create a purchase order and add lines through the user interface (UI), the line numbers are incremented correctly.</span></span> <span data-ttu-id="c9140-113">Jos kuitenkin käytät tiedonhallinnan kehystä (DMF), niitä ei koroteta oikein.</span><span class="sxs-lookup"><span data-stu-id="c9140-113">However, if you use the Data management framework (DMF), they aren't incremented correctly.</span></span>

<span data-ttu-id="c9140-114">Tämä ongelma ilmenee, koska tuotaessa rivejä DMF-kehyksen kautta järjestelmä käyttää DMF:n menetelmää niiden määrittämiseen, jos tuodussa yksikössä ei ole määritetty rivinumeroita valmiiksi.</span><span class="sxs-lookup"><span data-stu-id="c9140-114">This issue occurs because, when you import lines via DMF, if line numbers aren't already assigned in the imported entity, the system uses DMF's method for assigning them.</span></span> <span data-ttu-id="c9140-115">Tässä menetelmässä rivinumeroita kasvatetaan aina yhdellä.</span><span class="sxs-lookup"><span data-stu-id="c9140-115">That method always increments line numbers by one.</span></span>

### <a name="issue-workaround"></a><span data-ttu-id="c9140-116">Ongelman kiertotapa</span><span class="sxs-lookup"><span data-stu-id="c9140-116">Issue workaround</span></span>

<span data-ttu-id="c9140-117">Varmista, että halutut rivinumerot on jo määritetty tietoyksikön numerokentissä, kun tuot ostotilauksen rivit.</span><span class="sxs-lookup"><span data-stu-id="c9140-117">Make sure that the desired line numbers are already given in the data entity line number fields when you import the purchase order lines.</span></span> <span data-ttu-id="c9140-118">Tällöin DMF ei korvaa rivinumeroita.</span><span class="sxs-lookup"><span data-stu-id="c9140-118">In this case, DMF won't overwrite the line numbers.</span></span>

## <a name="a-default-tax-group-and-a-default-cash-discount-arent-filled-in-from-the-invoice-account"></a><span data-ttu-id="c9140-119">Oletusveroryhmää ja oletuskäteisalennusta ei täytetä laskutustililtä.</span><span class="sxs-lookup"><span data-stu-id="c9140-119">A default tax group and a default cash discount aren't filled in from the invoice account.</span></span>

<span data-ttu-id="c9140-120">Jos käytät laskutustiliä, joka eroaa asiakkaan tilistä, oletusveroryhmää ja oletuskäteisalennusta ei täytetä laskutustililtä, kun ostotilaus luodaan.</span><span class="sxs-lookup"><span data-stu-id="c9140-120">If you're using an invoice account that differs from the customer account, a default tax group and a default cash discount aren't filled in from the invoice account when a purchase order is created.</span></span>

<span data-ttu-id="c9140-121">Tämä on suunniteltu ominaisuus.</span><span class="sxs-lookup"><span data-stu-id="c9140-121">This behavior is by design.</span></span> <span data-ttu-id="c9140-122">Veroryhmän oletusarvot, käteisalennukset ja muut hintatiedot perustuvat asiakastiliin eivätkä laskutustiliin.</span><span class="sxs-lookup"><span data-stu-id="c9140-122">The default values for the tax group, cash discounts, and other price information are based on the customer account, not the invoice account.</span></span>

## <a name="i-receive-an-object-reference-not-set-error-during-purchase-order-confirmation-or-an-exception-has-been-thrown-by-the-target-of-an-invocation-exception-occurs-during-vendor-invoice-posting"></a><span data-ttu-id="c9140-123">Saan "Kohdeviitettä ei määritetty" -virheen ostotilauksen vahvistuksen aikana tai "Kutsun kohde on aiheuttanut poikkeuksen" -poikkeus esiintyy toimittajan laskun julkaisemisen yhteydessä.</span><span class="sxs-lookup"><span data-stu-id="c9140-123">I receive an "Object reference not set" error during purchase order confirmation, or an "Exception has been thrown by the target of an invocation" exception occurs during vendor invoice posting.</span></span>

<span data-ttu-id="c9140-124">Tämä ongelma voi esiintyä, kun ostotilausten jaoissa on epäjohdonmukaisuuksia.</span><span class="sxs-lookup"><span data-stu-id="c9140-124">This issue can occur because of inconsistency in purchase order distributions.</span></span>

<span data-ttu-id="c9140-125">Voit poistaa tämän ongelman eston ja palauttaa ostotilauksen *Luonnos* siirtymällä kohtaan **Ostot ja hankinnat \> Säännölliset tehtävät \> Tyhjennys \> Ostotilauksen jaon palautus**.</span><span class="sxs-lookup"><span data-stu-id="c9140-125">To unblock this issue and reset the purchase order to a *Draft* state, go to **Procurement and sourcing \> Periodic tasks \> Clean up \> Purchase order distribution reset**.</span></span> <span data-ttu-id="c9140-126">Lisä tietoja on seuraavassa blogikirjoituksessa: [Ostotilausten jakovirheiden korjaaminen Dynamics 365 Supply Chain Managementissa](https://cloudblogs.microsoft.com/dynamics365/it/2020/08/12/resolve-po-distribution-errors-in-dynamics-365-supply-chain-management/).</span><span class="sxs-lookup"><span data-stu-id="c9140-126">For more information, see the following blog post: [Resolve PO distribution errors in Dynamics 365 Supply Chain Management](https://cloudblogs.microsoft.com/dynamics365/it/2020/08/12/resolve-po-distribution-errors-in-dynamics-365-supply-chain-management/).</span></span>

## <a name="one-or-more-accounting-distributions-are-either-over-distributed-or-under-distributed"></a><span data-ttu-id="c9140-127">Vähintään yksi kirjanpidollinen jako on joko yli- tai alijaettu.</span><span class="sxs-lookup"><span data-stu-id="c9140-127">One or more accounting distributions are either over-distributed or under-distributed.</span></span>

### <a name="issue-description"></a><span data-ttu-id="c9140-128">Ongelman kuvaus</span><span class="sxs-lookup"><span data-stu-id="c9140-128">Issue description</span></span>

<span data-ttu-id="c9140-129">Näyttöön tulee seuraava virhe: "Vähintään yksi kirjanpidollinen jako on joko yli- tai alijaettu."</span><span class="sxs-lookup"><span data-stu-id="c9140-129">You receive the following error: "One or more accounting distributions is either over-distributed or under-distributed."</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="c9140-130">Ongelman ratkaisu</span><span class="sxs-lookup"><span data-stu-id="c9140-130">Issue resolution</span></span>

<span data-ttu-id="c9140-131">Tämä ongelma voi esiintyä, kun ostotilausten jaoissa on epäjohdonmukaisuuksia.</span><span class="sxs-lookup"><span data-stu-id="c9140-131">This issue can occur because of inconsistency in purchase order distributions.</span></span>

<span data-ttu-id="c9140-132">Voit poistaa tämän ongelman eston ja palauttaa ostotilauksen *Luonnos* siirtymällä kohtaan **Ostot ja hankinnat \> Säännölliset tehtävät \> Tyhjennys \> Ostotilauksen jaon palautus**.</span><span class="sxs-lookup"><span data-stu-id="c9140-132">To unblock this issue and reset the purchase order to a *Draft* state, go to **Procurement and sourcing \> Periodic tasks \> Clean up \> Purchase order distribution reset**.</span></span> <span data-ttu-id="c9140-133">Lisä tietoja on seuraavassa blogikirjoituksessa: [Ostotilausten jakovirheiden korjaaminen Dynamics 365 Supply Chain Managementissa](https://cloudblogs.microsoft.com/dynamics365/it/2020/08/12/resolve-po-distribution-errors-in-dynamics-365-supply-chain-management/).</span><span class="sxs-lookup"><span data-stu-id="c9140-133">For more information, see the following blog post: [Resolve PO distribution errors in Dynamics 365 Supply Chain Management](https://cloudblogs.microsoft.com/dynamics365/it/2020/08/12/resolve-po-distribution-errors-in-dynamics-365-supply-chain-management/).</span></span>

## <a name="can-i-show-only-purchase-orders-that-i-created"></a><span data-ttu-id="c9140-134">Voinko näyttää vain itse luomiani ostotilauksia?</span><span class="sxs-lookup"><span data-stu-id="c9140-134">Can I show only purchase orders that I created?</span></span>

<span data-ttu-id="c9140-135">Tämä toiminto ei ole tällä hetkellä käytettävissä.</span><span class="sxs-lookup"><span data-stu-id="c9140-135">This functionality isn't currently available.</span></span>

## <a name="can-i-reserve-inventory-and-create-transactions-against-registered-inventory-on-a-purchase-order"></a><span data-ttu-id="c9140-136">Voinko varata varastoa ja luoda tapahtumia rekisteröidyn varaston perusteella ostotilauksessa?</span><span class="sxs-lookup"><span data-stu-id="c9140-136">Can I reserve inventory and create transactions against registered inventory on a purchase order?</span></span>

### <a name="issue-description"></a><span data-ttu-id="c9140-137">Ongelman kuvaus</span><span class="sxs-lookup"><span data-stu-id="c9140-137">Issue description</span></span>

<span data-ttu-id="c9140-138">Vaikka nimikkeitä olisi ostotilauksessa *Rekisteröity*-tilassa, voit kuitenkin varata varastoa.</span><span class="sxs-lookup"><span data-stu-id="c9140-138">Even when items are in a *Registered* state on a purchase order, you can still reserve the inventory.</span></span> <span data-ttu-id="c9140-139">Toisin sanoen voit luoda tapahtumia rekisteröidyn varaston perusteella.</span><span class="sxs-lookup"><span data-stu-id="c9140-139">In other words, you can create transactions against the registered inventory.</span></span>

### <a name="reproduce-the-issue"></a><span data-ttu-id="c9140-140">Ongelman toistaminen</span><span class="sxs-lookup"><span data-stu-id="c9140-140">Reproduce the issue</span></span>

<span data-ttu-id="c9140-141">Seuraavassa esitetään yksi tapa ongelman toistamiseen.</span><span class="sxs-lookup"><span data-stu-id="c9140-141">The following procedure shows one way to reproduce the issue.</span></span>

1. <span data-ttu-id="c9140-142">Luo ostotilaus.</span><span class="sxs-lookup"><span data-stu-id="c9140-142">Create a purchase order.</span></span>
2. <span data-ttu-id="c9140-143">Ostotilausrivin rekisteröinti.</span><span class="sxs-lookup"><span data-stu-id="c9140-143">Register the purchase order line.</span></span>
3. <span data-ttu-id="c9140-144">Huomaa, että voit luoda varauksia tai tapahtumia rekisteröidyn varaston perusteella.</span><span class="sxs-lookup"><span data-stu-id="c9140-144">Notice that you can generate reservations or transactions against the registered inventory.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="c9140-145">Ongelman ratkaisu</span><span class="sxs-lookup"><span data-stu-id="c9140-145">Issue resolution</span></span>

<span data-ttu-id="c9140-146">Tämä on suunniteltu ominaisuus.</span><span class="sxs-lookup"><span data-stu-id="c9140-146">This behavior is by design.</span></span> <span data-ttu-id="c9140-147">Oletetaan, että rekisteröidyt nimikkeet ovat fyysisesti saapuneet varastoon ja että ne ovat näin ollen varattavissa.</span><span class="sxs-lookup"><span data-stu-id="c9140-147">The expectation is that the registered items have physically arrived in the warehouse or inventory, and that they are therefore available for reservation.</span></span>

## <a name="purchase-orders-dont-reflect-the-language-settings-of-the-legal-entity"></a><span data-ttu-id="c9140-148">Ostotilaukset eivät vastaa yrityksen kieliasetuksia.</span><span class="sxs-lookup"><span data-stu-id="c9140-148">Purchase orders don't reflect the language settings of the legal entity.</span></span>

### <a name="issue-description"></a><span data-ttu-id="c9140-149">Ongelman kuvaus</span><span class="sxs-lookup"><span data-stu-id="c9140-149">Issue description</span></span>

<span data-ttu-id="c9140-150">Osto tilauksen tuotenimi näkyy järjestelmän kielellä sen kielen sijaan, joka on määritetty sille yrityksellä, jossa ostotilaus on luotu.</span><span class="sxs-lookup"><span data-stu-id="c9140-150">The product name on a purchase order is shown in the system language instead of the language that is set for the legal entity where the purchase order was created.</span></span>

### <a name="reproduce-the-issue"></a><span data-ttu-id="c9140-151">Ongelman toistaminen</span><span class="sxs-lookup"><span data-stu-id="c9140-151">Reproduce the issue</span></span>

<span data-ttu-id="c9140-152">Seuraavassa esitetään yksi tapa ongelman toistamiseen.</span><span class="sxs-lookup"><span data-stu-id="c9140-152">The following procedure shows one way to reproduce the issue.</span></span>

1. <span data-ttu-id="c9140-153">Määritä järjestelmän kieleksi *EN-US* (Yhdysvaltojen englanti).</span><span class="sxs-lookup"><span data-stu-id="c9140-153">Set the system language to *EN-US* (US English).</span></span>
1. <span data-ttu-id="c9140-154">Varmista, että käytettävissä tuote, jossa kielet *EN-US* ja *DE* (saksa) ovat käytössä tuotenimen käännöksiä varten.</span><span class="sxs-lookup"><span data-stu-id="c9140-154">Make sure that there is a product where the *EN-US* and *DE* (German) languages are maintained for translations of the product name.</span></span>
1. <span data-ttu-id="c9140-155">Muuta yrityksen kieleksi *DE*.</span><span class="sxs-lookup"><span data-stu-id="c9140-155">Change the language of a legal entity to *DE*.</span></span>
1. <span data-ttu-id="c9140-156">Luo siinä yrityksessä, jossa kieleksi on määritetty *DE*, tuotteen sisältävä ostotilaus.</span><span class="sxs-lookup"><span data-stu-id="c9140-156">In the legal entity where *DE* is set as the language, create a purchase order that includes the product.</span></span>
1. <span data-ttu-id="c9140-157">Huomaa, että tuotteen nimi näkyy edelleen kielellä Yhdysvaltojen englanti (järjestelmän kieli).</span><span class="sxs-lookup"><span data-stu-id="c9140-157">Notice that the product name is still shown in US English (the system language).</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="c9140-158">Ongelman ratkaisu</span><span class="sxs-lookup"><span data-stu-id="c9140-158">Issue resolution</span></span>

<span data-ttu-id="c9140-159">Tämä on suunniteltu ominaisuus.</span><span class="sxs-lookup"><span data-stu-id="c9140-159">This behavior is by design.</span></span> <span data-ttu-id="c9140-160">Ostotilauksissa tuote näkyy aina järjestelmän kielellä.</span><span class="sxs-lookup"><span data-stu-id="c9140-160">On purchase orders, the product is always shown in the system language.</span></span> <span data-ttu-id="c9140-161">Ostotilauksen kieltä käytetään luotaessa vahvistuskirjauskansiota.</span><span class="sxs-lookup"><span data-stu-id="c9140-161">The purchase order language is used when a confirmation journal is created.</span></span>

## <a name="the-approved-vendor-list-by-product-entity-doesnt-allow-the-effective-date-to-be-changed"></a><span data-ttu-id="c9140-162">Tuoteyksikkökohtainen hyväksyttyjen toimittajien luettelo ei salli voimaantulopäivän muuttamista.</span><span class="sxs-lookup"><span data-stu-id="c9140-162">The Approved vendor list by product entity doesn't allow the effective date to be changed.</span></span>

### <a name="issue-description"></a><span data-ttu-id="c9140-163">Ongelman kuvaus</span><span class="sxs-lookup"><span data-stu-id="c9140-163">Issue description</span></span>

<span data-ttu-id="c9140-164">Tuotteella on hyväksytty toimittaja, jonka voimaantulopäivä on esimerkiksi 11. tammikuuta 2018 (*01/11/2018*) ja vanhentumispäivä on *Ei koskaan*.</span><span class="sxs-lookup"><span data-stu-id="c9140-164">A product has an approved vendor that has, for example, an effective date of January 11, 2018 (*01/11/2018*), and an expiration date of *Never*.</span></span> <span data-ttu-id="c9140-165">Jos yrität muuttaa voimaantulopäivän muotoon 10. tammikuuta 2018 (*01/10/2018*) tai 12. tammikuuta 2018 (*01/12/2018*), näyttöön tulee seuraava virhesanoma:</span><span class="sxs-lookup"><span data-stu-id="c9140-165">If you try to change the effective date to January 10, 2018 (*01/10/2018*), or January 12, 2018 (*01/12/2018*), you receive the following error:</span></span>

> <span data-ttu-id="c9140-166">Tietuetta ei voi luoda hyväksyttyjen toimittajien luetteloon (PdsApproveVendorList).</span><span class="sxs-lookup"><span data-stu-id="c9140-166">Cannot create a record in Approved supplier list (PdsApproveVendorList).</span></span> <span data-ttu-id="c9140-167">Vanhentumispäivän arvon on oltava sama tai suurempi kuin voimaantulopäivän arvo.</span><span class="sxs-lookup"><span data-stu-id="c9140-167">The 'Expiration' value needs to be greater than or equal to the 'Effective' value.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="c9140-168">Ongelman ratkaisu</span><span class="sxs-lookup"><span data-stu-id="c9140-168">Issue resolution</span></span>

<span data-ttu-id="c9140-169">Voit pidentää vain sitä jaksoa, jolle toimittaja on hyväksytty.</span><span class="sxs-lookup"><span data-stu-id="c9140-169">You can only extend the period that the vendor is approved for.</span></span> <span data-ttu-id="c9140-170">Seuraavat säännöt pätevät:</span><span class="sxs-lookup"><span data-stu-id="c9140-170">The following rules apply:</span></span>

- <span data-ttu-id="c9140-171">Jos haluat muuttaa voimaantulopäivää siten, että se nimikkeen toimittajan olemassa olevia tietueita (jaksoja) aiemmin, uuden jakson vanhanemispäivän on oltava ennen kaikkia olemassa olevien tietueiden vanhenemispäivää.</span><span class="sxs-lookup"><span data-stu-id="c9140-171">To change the effective date so that it's earlier than any of the existing records (periods) for the item vendor, the expiration date of the new period must be before all the expiration dates in the existing records.</span></span>
- <span data-ttu-id="c9140-172">Jos haluat muuttaa vanhenemispäivää siten, että se on myöhempi kuin jokin olemassa oleva jakso, voimaantulopäivämäärän ei saa olla ennen olemassa olevan tietueen vanhenemispäivää.</span><span class="sxs-lookup"><span data-stu-id="c9140-172">To change the expiration date so that it's later than any of the existing periods, the effective date must be after the latest expiration date in any existing record.</span></span>
- <span data-ttu-id="c9140-173">Jos haluat pienentää kokonaisaikaa, jolle toimittaja on hyväksytty, sinun on poistettava tai muokattava olemassa olevia tietueia.</span><span class="sxs-lookup"><span data-stu-id="c9140-173">To reduce the overall period that the vendor is approved for, you must delete or modify existing records.</span></span> <span data-ttu-id="c9140-174">Vaihtoehtoisesti voit käyttää **katkaisu**-valitsinta tuonnin aikana.</span><span class="sxs-lookup"><span data-stu-id="c9140-174">Alternatively, you can use the **truncate** switch during import.</span></span> <span data-ttu-id="c9140-175">Tämä valitsin poistaa kaikki olemassa olevat tietueet nimikekohteisten hyväksyttyjen toimittajien taulukosta.</span><span class="sxs-lookup"><span data-stu-id="c9140-175">This switch deletes all existing records in the table for approved vendors by item.</span></span>

<span data-ttu-id="c9140-176">Esimerkiksi ongelmankuvauksessa kuvattu skenaario, jossa tietueen voimaantulopäivä on *01/11/2018* ja vanhenemispäivä *Ei koskaan*, y voit tuoda uuden tiedoston, jonka voimaantulopäivänä on *01/10/2018* vanhenemispäivänä *Ei koskaan*.</span><span class="sxs-lookup"><span data-stu-id="c9140-176">For the example scenario that is described in the issue description, where a record has an effective date of *01/11/2018* and an expiration date of *Never*, you can import a new record that has an effective date of *01/10/2018* and an expiration date of *Never*.</span></span> <span data-ttu-id="c9140-177">Et kuitenkaan voi lyhentää ajanjaksoa niin, että voimaantulopäiväksi päivittyy tiedonhallinnan kautta *01/12/2018*.</span><span class="sxs-lookup"><span data-stu-id="c9140-177">However, you can't reduce the period so that the effective date is updated to *01/12/2018* via data management.</span></span> <span data-ttu-id="c9140-178">Tämä muutos on tehtävä käyttöliittymässä.</span><span class="sxs-lookup"><span data-stu-id="c9140-178">You must make this change through the UI.</span></span>

## <a name="after-i-change-the-delivery-address-on-a-purchase-order-header-the-delivery-name-isnt-synced"></a><span data-ttu-id="c9140-179">Kun muutan ostotilauksen otsikon toimitusosoitetta, toimituksen nimeä ei synkronoida.</span><span class="sxs-lookup"><span data-stu-id="c9140-179">After I change the delivery address on a purchase order header, the delivery name isn't synced.</span></span>

### <a name="issue-description"></a><span data-ttu-id="c9140-180">Ongelman kuvaus</span><span class="sxs-lookup"><span data-stu-id="c9140-180">Issue description</span></span>

<span data-ttu-id="c9140-181">Ostotilauksen otsikossa oleva osoite päivitetään osoitteeksi, joka ei ole toimitusosoite.</span><span class="sxs-lookup"><span data-stu-id="c9140-181">The address on the header of a purchase order is updated to an address that isn't a delivery address.</span></span> <span data-ttu-id="c9140-182">Vaikka osoite päivitetään ostotilauksessa, toimituksen nimeä ei päivitetä päivitetyn osoitteen perusteella.</span><span class="sxs-lookup"><span data-stu-id="c9140-182">Although the address is updated on the purchase order, the delivery name isn't updated based on the updated address.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="c9140-183">Ongelman ratkaisu</span><span class="sxs-lookup"><span data-stu-id="c9140-183">Issue resolution</span></span>

<span data-ttu-id="c9140-184">Tämä on suunniteltu ominaisuus.</span><span class="sxs-lookup"><span data-stu-id="c9140-184">This behavior is by design.</span></span> <span data-ttu-id="c9140-185">Valittu osoite on luokiteltava toimitusosoitteeksi.</span><span class="sxs-lookup"><span data-stu-id="c9140-185">The selected address must be classified as a delivery address.</span></span> <span data-ttu-id="c9140-186">Muussa tapauksessa toimituksen nimeä ei päivitetä valitun osoitteen perusteella.</span><span class="sxs-lookup"><span data-stu-id="c9140-186">Otherwise, the delivery name isn't updated based on the selected address.</span></span>

## <a name="can-i-find-the-user-who-canceled-a-purchase-order"></a><span data-ttu-id="c9140-187">Voinko löytää ostotilauksen peruneen käyttäjän?</span><span class="sxs-lookup"><span data-stu-id="c9140-187">Can I find the user who canceled a purchase order?</span></span>

<span data-ttu-id="c9140-188">Näitä tietoja seurataan vain, jos ostotilaus edellyttää muutoksenhallintaa.</span><span class="sxs-lookup"><span data-stu-id="c9140-188">This information is tracked only if the purchase order is subject to change management.</span></span> <span data-ttu-id="c9140-189">Jos käytät muutoksenhallintaa, voit nähdä muutoksen (peruutuksen) lähettäjän ja hyväksyjän.</span><span class="sxs-lookup"><span data-stu-id="c9140-189">If you use change management, you can see who submitted the change (the cancellation), and who approved it.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]