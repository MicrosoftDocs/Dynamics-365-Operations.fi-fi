---
title: Täytä myyntisopimuksia
description: Tässä menettelyssä käsitellään, miten myyntisopimus toteutetaan liittämällä siihen myyntitilauksia.
author: omulvad
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SalesAgreementListPage, SalesAgreement, SalesAgreementGenerateReleaseOrder, SalesTableListPage, SalesTable, AgreementLine, SalesCreateOrder,  SalesEditLines, SalesAgreementHistory
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 31c86ae556789ecf04dc303ddd9510458c1f6d01
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5260380"
---
# <a name="fulfill-sales-agreements"></a><span data-ttu-id="1f6f5-103">Täytä myyntisopimuksia</span><span class="sxs-lookup"><span data-stu-id="1f6f5-103">Fulfill sales agreements</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="1f6f5-104">Tässä menettelyssä käsitellään, miten myyntisopimus toteutetaan liittämällä siihen myyntitilauksia.</span><span class="sxs-lookup"><span data-stu-id="1f6f5-104">This procedure shows you how to fulfill a sales agreement by associating sales orders with it.</span></span> <span data-ttu-id="1f6f5-105">Voit suorittaa tämän menettelyn esittely-yrityksen USMF kanssa tai käyttää omia tietojasi.</span><span class="sxs-lookup"><span data-stu-id="1f6f5-105">You can run this procedure in demo data company USMF or on your own data.</span></span> <span data-ttu-id="1f6f5-106">Varmista ennen tämän opastuksen aloittamista, että sinulla on voimassaoleva myyntisopimus, jonka tyyppi on Tuotteen arvon vahvistus.</span><span class="sxs-lookup"><span data-stu-id="1f6f5-106">Before starting this guide, make sure you have an effective sales agreement of type "Product value commitment".</span></span> <span data-ttu-id="1f6f5-107">Vaihtoehtoisesti voit suorittaa Luo myyntisopimuksia -tehtäväopastuksen.</span><span class="sxs-lookup"><span data-stu-id="1f6f5-107">Alternatively, you can run the task guide called "Create sales agreements".</span></span>  




## <a name="release-a-sales-order-from-the-agreement"></a><span data-ttu-id="1f6f5-108">Vapauta myyntitilaus sopimuksista</span><span class="sxs-lookup"><span data-stu-id="1f6f5-108">Release a sales order from the agreement</span></span>
1. <span data-ttu-id="1f6f5-109">Valitse Myynti ja markkinointi > Myyntisopimukset > Myyntisopimukset.</span><span class="sxs-lookup"><span data-stu-id="1f6f5-109">Go to Sales and marketing > Sales agreements > Sales agreements.</span></span>
2. <span data-ttu-id="1f6f5-110">Avaa luettelossa sopimus, jonka mukaisesti haluat vapauttaa tilauksen.</span><span class="sxs-lookup"><span data-stu-id="1f6f5-110">In the list, open the agreement against which you want to release the order.</span></span>
3. <span data-ttu-id="1f6f5-111">Valitse toimintoruudussa Myyntisopimus.</span><span class="sxs-lookup"><span data-stu-id="1f6f5-111">On the Action Pane, click Sales agreement.</span></span>
4. <span data-ttu-id="1f6f5-112">Valitse Vapauta tilaus.</span><span class="sxs-lookup"><span data-stu-id="1f6f5-112">Click Release order.</span></span>
    * <span data-ttu-id="1f6f5-113">Luo vapautustilaus -sivun yläosassa oleva teksti ilmaisee, että myyntitilausrivin edellyttävät tiedot vaihtelevat sen mukaan, onko sopimus määrä- vai arvoperusteinen.</span><span class="sxs-lookup"><span data-stu-id="1f6f5-113">As the text on top of the  Create release order page points out, the details required for the sales order lines will differ depending on whether the agreement is quantity- or value-based.</span></span>  
    * <span data-ttu-id="1f6f5-114">Tämän opastuksen sopimuksen tyyppi on Tuotteen arvon vahvistus.</span><span class="sxs-lookup"><span data-stu-id="1f6f5-114">The agreement in this guide is of type "Product value commitment".</span></span> <span data-ttu-id="1f6f5-115">Tämän vuoksi tämän sivun Rivit-osa on tyhjä.</span><span class="sxs-lookup"><span data-stu-id="1f6f5-115">This is why the Lines section of this page is blank.</span></span> <span data-ttu-id="1f6f5-116">Jos sitoutuminen perustuisi määrään, rivitiedot kopioitaisiin sopimuksesta.</span><span class="sxs-lookup"><span data-stu-id="1f6f5-116">If the commitment was based on quantity, the line information would be copied from the agreement.</span></span>  
5. <span data-ttu-id="1f6f5-117">Valitse Luo.</span><span class="sxs-lookup"><span data-stu-id="1f6f5-117">Click Create.</span></span>
    * <span data-ttu-id="1f6f5-118">Sanoma ilmoittaa, että myyntitilaus on luotu.</span><span class="sxs-lookup"><span data-stu-id="1f6f5-118">The message informs you that a sales order has been created.</span></span> <span data-ttu-id="1f6f5-119">Koska tilauksessa ei ole rivejä, sinun on viimeisteltävä vapautusprosessi lisäämällä tilausrivin tiedot.</span><span class="sxs-lookup"><span data-stu-id="1f6f5-119">Since the order does not contain any lines, you must add order line details to complete the release process.</span></span>   
6. <span data-ttu-id="1f6f5-120">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="1f6f5-120">Close the page.</span></span>
7. <span data-ttu-id="1f6f5-121">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="1f6f5-121">Close the page.</span></span>
8. <span data-ttu-id="1f6f5-122">Siirry kohtaan Myynti ja markkinointi > Myyntitilaukset > Kaikki myyntitilaukset.</span><span class="sxs-lookup"><span data-stu-id="1f6f5-122">Go to Sales and marketing > Sales orders > All sales orders.</span></span>
9. <span data-ttu-id="1f6f5-123">Etsi ja avaa luettelossa tilaus, joka luotiin edellisessä tehtävässä vapautetun tilauksen vuoksi.</span><span class="sxs-lookup"><span data-stu-id="1f6f5-123">In the list, find and open the order that was created as the result of the order release in the previous task.</span></span>
10. <span data-ttu-id="1f6f5-124">Valitse Lisää rivi.</span><span class="sxs-lookup"><span data-stu-id="1f6f5-124">Click Add line.</span></span>
11. <span data-ttu-id="1f6f5-125">Avaa haku valitsemalla Nimiketunnus-kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="1f6f5-125">In the Item number field, click the drop-down button to open the lookup.</span></span>
12. <span data-ttu-id="1f6f5-126">Kirjoita tai valitse Nimiketunnus-kentässä nimike, joka määritettiin liitetyssä myyntisopimuksessa.</span><span class="sxs-lookup"><span data-stu-id="1f6f5-126">In the Item number field, type or select the item that is specified on the associated sales agreement.</span></span>
13. <span data-ttu-id="1f6f5-127">Kirjoita numero Määrä-kenttään.</span><span class="sxs-lookup"><span data-stu-id="1f6f5-127">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="1f6f5-128">Varmista, että annat määrän, jonka mukainen nettosumma alittaa liittyvän myyntisopimuksen arvon.</span><span class="sxs-lookup"><span data-stu-id="1f6f5-128">Make sure that you enter a quantity that brings the Net amount under the value of the associated sales agreement.</span></span>  
    * <span data-ttu-id="1f6f5-129">Huomaa, että koska myyntitilaus on linkitetty sopimukseen, neuvoteltua alennusprosenttia käytetään tilausrivillä.</span><span class="sxs-lookup"><span data-stu-id="1f6f5-129">Notice that because the sales order is linked to the agreement, the negotiated discount percent is applied to the order line.</span></span>  
14. <span data-ttu-id="1f6f5-130">Valitse Päivitä rivi.</span><span class="sxs-lookup"><span data-stu-id="1f6f5-130">Click Update line.</span></span>
15. <span data-ttu-id="1f6f5-131">Valitse Liitetty.</span><span class="sxs-lookup"><span data-stu-id="1f6f5-131">Click Attached.</span></span>
    * <span data-ttu-id="1f6f5-132">Liitetty sopimus -sivulla on sen sopimuksen tunnus ja ehdot, josta rivi on vapautettu.</span><span class="sxs-lookup"><span data-stu-id="1f6f5-132">The Attached agreement page shows the ID and terms of the agreement from which the line is released.</span></span>  
16. <span data-ttu-id="1f6f5-133">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="1f6f5-133">Close the page.</span></span>
17. <span data-ttu-id="1f6f5-134">Valitse toimintoruudussa Yleiset.</span><span class="sxs-lookup"><span data-stu-id="1f6f5-134">On the Action Pane, click General.</span></span>
18. <span data-ttu-id="1f6f5-135">Valitse Liittyvä myyntisopimus.</span><span class="sxs-lookup"><span data-stu-id="1f6f5-135">Click Attached sales agreement.</span></span>
19. <span data-ttu-id="1f6f5-136">Laajenna Rivin erittely -osa.</span><span class="sxs-lookup"><span data-stu-id="1f6f5-136">Expand the Line details section.</span></span>
20. <span data-ttu-id="1f6f5-137">Valitse Täytäntöönpano-välilehti.</span><span class="sxs-lookup"><span data-stu-id="1f6f5-137">Click the Fulfillment tab.</span></span>
    * <span data-ttu-id="1f6f5-138">Täytäntöönpano-välilehdessä on kaikkien tähän sitoutumiseen liitettyjen myyntitilausrivien yhteenveto ja niiden täytäntöönpanotila sekä vielä vapauttamaton summa tai määrä.</span><span class="sxs-lookup"><span data-stu-id="1f6f5-138">The Fulfillment tab shows a summary of all the sales order lines that are associated with this commitment, and their fulfillment state, as well as the amount or quantity that has not yet been released.</span></span>   
21. <span data-ttu-id="1f6f5-139">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="1f6f5-139">Close the page.</span></span>
22. <span data-ttu-id="1f6f5-140">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="1f6f5-140">Close the page.</span></span>
23. <span data-ttu-id="1f6f5-141">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="1f6f5-141">Close the page.</span></span>

## <a name="apply-sales-agreement-in-the-order-process"></a><span data-ttu-id="1f6f5-142">Käytä myyntisopimuksia tilausprosessissa</span><span class="sxs-lookup"><span data-stu-id="1f6f5-142">Apply sales agreement in the order process</span></span>
1. <span data-ttu-id="1f6f5-143">Siirry kohtaan Myynti ja markkinointi > Myyntitilaukset > Kaikki myyntitilaukset.</span><span class="sxs-lookup"><span data-stu-id="1f6f5-143">Go to Sales and marketing > Sales orders > All sales orders.</span></span>
2. <span data-ttu-id="1f6f5-144">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="1f6f5-144">Click New.</span></span>
3. <span data-ttu-id="1f6f5-145">Avaa haku valitsemalla Asiakastili-kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="1f6f5-145">In the Customer account field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="1f6f5-146">Etsi ja valitse luettelossa asiakas, joka on määritetty myyntisopimuksessa.</span><span class="sxs-lookup"><span data-stu-id="1f6f5-146">In the list, find and select the customer specified on the sales agreement.</span></span>
5. <span data-ttu-id="1f6f5-147">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="1f6f5-147">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="1f6f5-148">Laajenna Yleinen-osa.</span><span class="sxs-lookup"><span data-stu-id="1f6f5-148">Expand the General section.</span></span>
7. <span data-ttu-id="1f6f5-149">Avaa haku napsauttamalla Myyntisopimuksen tunnus -kentässä avattavan valikon painiketta.</span><span class="sxs-lookup"><span data-stu-id="1f6f5-149">In the Sales agreement ID field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="1f6f5-150">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="1f6f5-150">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="1f6f5-151">Valitse Kyllä.</span><span class="sxs-lookup"><span data-stu-id="1f6f5-151">Click Yes.</span></span>
10. <span data-ttu-id="1f6f5-152">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="1f6f5-152">Click OK.</span></span>
11. <span data-ttu-id="1f6f5-153">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="1f6f5-153">In the list, mark the selected row.</span></span>
12. <span data-ttu-id="1f6f5-154">Avaa haku valitsemalla Nimiketunnus-kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="1f6f5-154">In the Item number field, click the drop-down button to open the lookup.</span></span>
13. <span data-ttu-id="1f6f5-155">Kirjoita tai valitse Nimiketunnus-kentässä nimike, joka määritettiin liitetyssä myyntisopimuksessa.</span><span class="sxs-lookup"><span data-stu-id="1f6f5-155">In the Item number field, type or select the item that is specified on the associated sales agreement.</span></span>
14. <span data-ttu-id="1f6f5-156">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="1f6f5-156">In the list, click the link in the selected row.</span></span>
15. <span data-ttu-id="1f6f5-157">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="1f6f5-157">Click Save.</span></span>
16. <span data-ttu-id="1f6f5-158">Valitse toimintoruudussa Kerää ja pakkaa.</span><span class="sxs-lookup"><span data-stu-id="1f6f5-158">On the Action Pane, click Pick and pack.</span></span>
17. <span data-ttu-id="1f6f5-159">Valitse Kirjaa pakkausluettelo.</span><span class="sxs-lookup"><span data-stu-id="1f6f5-159">Click Post packing slip.</span></span>
18. <span data-ttu-id="1f6f5-160">Laajenna Parametrit-osa.</span><span class="sxs-lookup"><span data-stu-id="1f6f5-160">Expand the Parameters section.</span></span>
19. <span data-ttu-id="1f6f5-161">Valitse Kirjaus-kentässä Kyllä.</span><span class="sxs-lookup"><span data-stu-id="1f6f5-161">Select Yes in the Posting field.</span></span>
20. <span data-ttu-id="1f6f5-162">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="1f6f5-162">Click OK.</span></span>
21. <span data-ttu-id="1f6f5-163">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="1f6f5-163">Click OK.</span></span>
22. <span data-ttu-id="1f6f5-164">Valitse toimintoruudussa Yleiset.</span><span class="sxs-lookup"><span data-stu-id="1f6f5-164">On the Action Pane, click General.</span></span>
23. <span data-ttu-id="1f6f5-165">Valitse Liittyvä myyntisopimus.</span><span class="sxs-lookup"><span data-stu-id="1f6f5-165">Click Attached sales agreement.</span></span>
24. <span data-ttu-id="1f6f5-166">Valitse Täytäntöönpano-välilehti.</span><span class="sxs-lookup"><span data-stu-id="1f6f5-166">Click the Fulfillment tab.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]