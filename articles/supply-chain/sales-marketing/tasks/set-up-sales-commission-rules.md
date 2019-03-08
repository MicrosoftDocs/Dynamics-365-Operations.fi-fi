---
title: Määritä myyntiprovision säännöt
description: Tässä menettelyssä käsitellään, miten myyntiprovision laskenta ja seuranta määritetään ja otetaan käyttöön.
author: omulvad
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CommissionCustomerGroup, CommissionItemGroup, CommissionSalesGroup, CommissionSalesMember, DirPartyLookup, CommissionCalc, InventPosting, CustTable, EcoResProductDetailsExtended
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0ed7ec4ca74e4b6863ab2feff7f20de319789038
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/29/2019
ms.locfileid: "334217"
---
# <a name="set-up-sales-commission-rules"></a><span data-ttu-id="a2e85-103">Määritä myyntiprovision säännöt</span><span class="sxs-lookup"><span data-stu-id="a2e85-103">Set up sales commission rules</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="a2e85-104">Tässä menettelyssä käsitellään, miten myyntiprovision laskenta ja seuranta määritetään ja otetaan käyttöön.</span><span class="sxs-lookup"><span data-stu-id="a2e85-104">This procedure shows you how to set up and enable sales commission calculation and tracking.</span></span> <span data-ttu-id="a2e85-105">Menettely osoittaa, miten asiakas- ja nimikeprovisioryhmät luodaan ja miten valittu asiakas ja tuote linkitetään vastaaviin ryhmiin.</span><span class="sxs-lookup"><span data-stu-id="a2e85-105">The procedure shows how to create both customer and item commission groups, and then how to link a selected customer and product to the respective groups.</span></span> <span data-ttu-id="a2e85-106">Kyseisiä ryhmiä käytetään sitten provision laskenta-asetuksissa luomaan asiakas-, nimike- ja myyntiedustajayhdistelmä, joka on täsmäytettävä myyntitilaukseen, jotta myyjät saisivat provision.</span><span class="sxs-lookup"><span data-stu-id="a2e85-106">Those groups are then used in the commission calculation setup to create a customer, item, and sales representatives combination that must be matched by the sales order to entitle the sales people to a commission.</span></span> <span data-ttu-id="a2e85-107">Asiakas- ja nimikeprovisioryhmien on vapaaehtoista, sillä provisio voidaan laskea yksittäisen asiakkaan ja/tai nimikkeen perusteella.</span><span class="sxs-lookup"><span data-stu-id="a2e85-107">Creating customer and item commission groups are optional, as the calculation of commission can also be done for an individual customer and/or item.</span></span> <span data-ttu-id="a2e85-108">Voit suorittaa tämän menettelyn esittely-yrityksen USMF kanssa tai käyttää omia tietojasi.</span><span class="sxs-lookup"><span data-stu-id="a2e85-108">You can run this procedure in demo data company USMF or on your own data.</span></span>


## <a name="set-up-commission-groups-and-commission-rates"></a><span data-ttu-id="a2e85-109">Määritä provisioryhmät ja provisioprosentit</span><span class="sxs-lookup"><span data-stu-id="a2e85-109">Set up commission groups and commission rates</span></span>
1. <span data-ttu-id="a2e85-110">Valitse Myynti ja markkinointi > Provisiot > Provision asiakasryhmät.</span><span class="sxs-lookup"><span data-stu-id="a2e85-110">Go to Sales and marketing > Commissions > Customer groups for commission.</span></span>
2. <span data-ttu-id="a2e85-111">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="a2e85-111">Click New.</span></span>
3. <span data-ttu-id="a2e85-112">Kirjoita Ryhmä-kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="a2e85-112">In the Group field, type a value.</span></span>
4. <span data-ttu-id="a2e85-113">Kirjoita arvo Nimi-kenttään.</span><span class="sxs-lookup"><span data-stu-id="a2e85-113">In the Name field, type a value.</span></span>
5. <span data-ttu-id="a2e85-114">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="a2e85-114">Click Save.</span></span>
6. <span data-ttu-id="a2e85-115">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="a2e85-115">Close the page.</span></span>
7. <span data-ttu-id="a2e85-116">Valitse Myynti ja markkinointi > Provisiot > Nimikeryhmät.</span><span class="sxs-lookup"><span data-stu-id="a2e85-116">Go to Sales and marketing > Commissions > Item groups.</span></span>
8. <span data-ttu-id="a2e85-117">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="a2e85-117">Click New.</span></span>
9. <span data-ttu-id="a2e85-118">Kirjoita Ryhmä-kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="a2e85-118">In the Group field, type a value.</span></span>
10. <span data-ttu-id="a2e85-119">Kirjoita arvo Nimi-kenttään.</span><span class="sxs-lookup"><span data-stu-id="a2e85-119">In the Name field, type a value.</span></span>
11. <span data-ttu-id="a2e85-120">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="a2e85-120">Close the page.</span></span>
12. <span data-ttu-id="a2e85-121">Valitse Myynti ja markkinointi > Provisiot > Myyntiryhmät.</span><span class="sxs-lookup"><span data-stu-id="a2e85-121">Go to Sales and marketing > Commissions > Sales groups.</span></span>
    * <span data-ttu-id="a2e85-122">Provisiomyyntiryhmä määrittää, ketkä työntekijät, joilla on myyntiedustajan rooli, voivat saada provision, kun kyseiseen myyntiryhmään liitetty asiakas ostaa tiettyjä nimikkeitä.</span><span class="sxs-lookup"><span data-stu-id="a2e85-122">A Commission sales group specifies the employees in sales representative roles who are eligible to receive a commission when a customer associated with the relevant sales group buys certain items.</span></span>  
    * <span data-ttu-id="a2e85-123">USMF-demotietoyrityksessä myyntiryhmä Sales reps US.</span><span class="sxs-lookup"><span data-stu-id="a2e85-123">In the USMF demo data company, there is a sales group called "Sales reps US."</span></span>  
13. <span data-ttu-id="a2e85-124">Valitse toimintoruudussa Yleiset.</span><span class="sxs-lookup"><span data-stu-id="a2e85-124">On the Action Pane, click General.</span></span>
14. <span data-ttu-id="a2e85-125">Valitse Myyjä.</span><span class="sxs-lookup"><span data-stu-id="a2e85-125">Click Sales rep..</span></span>
    * <span data-ttu-id="a2e85-126">Myyjä-sivulla näkyy luettelo yrityksen myyntihenkilöistä, jotka liittyvät määrättyyn provisioryhmään.</span><span class="sxs-lookup"><span data-stu-id="a2e85-126">The Sales rep. page displays a list of the company's sales people who are associated with a specific commission group.</span></span> <span data-ttu-id="a2e85-127">Voit määrittää samaan ryhmään useita myyntiedustajia ja määrittää prosentteina kunkin osuuden kokonaisprovisiosta.</span><span class="sxs-lookup"><span data-stu-id="a2e85-127">You can assign multiple sales representatives to the same group and define their respective share of the total commission fee as a percentage value.</span></span> <span data-ttu-id="a2e85-128">Kaikkien työntekijöiden osuus kokonaisprovisiosta ei voi olla yli 100.</span><span class="sxs-lookup"><span data-stu-id="a2e85-128">The total commission share across all employees must not exceed 100.</span></span>  
15. <span data-ttu-id="a2e85-129">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="a2e85-129">In the list, mark the selected row.</span></span>
16. <span data-ttu-id="a2e85-130">Valitse Muokkaa.</span><span class="sxs-lookup"><span data-stu-id="a2e85-130">Click Edit.</span></span>
17. <span data-ttu-id="a2e85-131">Määritä provisio-osuudeksi 50.</span><span class="sxs-lookup"><span data-stu-id="a2e85-131">Set Commission share to '50'.</span></span>
18. <span data-ttu-id="a2e85-132">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="a2e85-132">Click New.</span></span>
19. <span data-ttu-id="a2e85-133">Avaa haku valitsemalla Nimi-kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="a2e85-133">In the Name field, click the drop-down button to open the lookup.</span></span>
20. <span data-ttu-id="a2e85-134">Käytä pikasuodatinta tietueiden etsimiseen.</span><span class="sxs-lookup"><span data-stu-id="a2e85-134">Use the Quick Filter to find records.</span></span> <span data-ttu-id="a2e85-135">Voit esimerkiksi suodattaa Nimi-kenttää arvolla Sudan Burk.</span><span class="sxs-lookup"><span data-stu-id="a2e85-135">For example, filter on the Name field with a value of 'Susan Burk'.</span></span>
21. <span data-ttu-id="a2e85-136">Klikkaa Valitse.</span><span class="sxs-lookup"><span data-stu-id="a2e85-136">Click Select.</span></span>
22. <span data-ttu-id="a2e85-137">Määritä provisio-osuudeksi 50.</span><span class="sxs-lookup"><span data-stu-id="a2e85-137">Set Commission share to '50'.</span></span>
23. <span data-ttu-id="a2e85-138">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="a2e85-138">Click Save.</span></span>
24. <span data-ttu-id="a2e85-139">Valitse Myynti ja markkinointi > Provisiot > Provisiolaskelma.</span><span class="sxs-lookup"><span data-stu-id="a2e85-139">Go to Sales and marketing > Commissions > Commission calculation.</span></span>
    * <span data-ttu-id="a2e85-140">Voit määrittää Provisiolaskelma-sivulla provisioprosentin, jonka työntekijä saa myyntitapahtumasta, kun se sisältää ennaltamääritetyn asiakas- ja tuoteyhdistelmän.</span><span class="sxs-lookup"><span data-stu-id="a2e85-140">In the Commission calculation page you define the commission rate that the employee is to receive for a sales transaction when it contains the pre-set combination of customer and product.</span></span> <span data-ttu-id="a2e85-141">Provisioprosenttiasetusten osana on määritettävä provision laskentaperusta sekä alennusten sisällyttäminen tai poissulkeminen.</span><span class="sxs-lookup"><span data-stu-id="a2e85-141">As part of the commission rate setup, you must specify the commission calculation basis and whether it should include or exclude discounts.</span></span> <span data-ttu-id="a2e85-142">Voit myös antaa voimassaoloajan, jolloin provisioprosentti on aktiivinen.</span><span class="sxs-lookup"><span data-stu-id="a2e85-142">You can also enter a validity period for when the commission rate is active.</span></span>  
25. <span data-ttu-id="a2e85-143">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="a2e85-143">Click New.</span></span>
26. <span data-ttu-id="a2e85-144">Valitse Nimikekoodi-kentässä Ryhmä.</span><span class="sxs-lookup"><span data-stu-id="a2e85-144">In the Item code field, select 'Group'.</span></span>
27. <span data-ttu-id="a2e85-145">Avaa haku napsauttamalla Nimikesuhde-kentässä avattavan valikon painiketta.</span><span class="sxs-lookup"><span data-stu-id="a2e85-145">In the Item relation field, click the drop-down button to open the lookup.</span></span>
28. <span data-ttu-id="a2e85-146">Etsi ja valitse luettelosta aiemmin luomasi ryhmä.</span><span class="sxs-lookup"><span data-stu-id="a2e85-146">In the list, find and select the group that you created earlier.</span></span>
29. <span data-ttu-id="a2e85-147">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="a2e85-147">In the list, click the link in the selected row.</span></span>
30. <span data-ttu-id="a2e85-148">Valitse Asiakaskoodi-kentässä Ryhmä.</span><span class="sxs-lookup"><span data-stu-id="a2e85-148">In the Customer code field, select 'Group'.</span></span>
31. <span data-ttu-id="a2e85-149">Avaa haku napsauttamalla Asiakassuhde-kentässä avattavan valikon painiketta.</span><span class="sxs-lookup"><span data-stu-id="a2e85-149">In the Customer relation field, click the drop-down button to open the lookup.</span></span>
32. <span data-ttu-id="a2e85-150">Valitse luettelosta aiemmin määrittämäsi ryhmä.</span><span class="sxs-lookup"><span data-stu-id="a2e85-150">In the list, select the group that you set up earlier.</span></span>
33. <span data-ttu-id="a2e85-151">Avaa haku napsauttamalla Myyjän suhde -kentässä avattavan valikon painiketta.</span><span class="sxs-lookup"><span data-stu-id="a2e85-151">In the Sales rep. relation field, click the drop-down button to open the lookup.</span></span>
34. <span data-ttu-id="a2e85-152">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="a2e85-152">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="a2e85-153">Säilytä Ennen rivialennusta -vaihtoehto.</span><span class="sxs-lookup"><span data-stu-id="a2e85-153">Keep the "Before line discount" option.</span></span>  
    * <span data-ttu-id="a2e85-154">Säilytä Tuotto-vaihtoehto provision arvon laskennan perusteena.</span><span class="sxs-lookup"><span data-stu-id="a2e85-154">Keep the "Revenue" option as the basis for commission value calculation.</span></span>    
35. <span data-ttu-id="a2e85-155">Lisää Provisioprosentti-kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="a2e85-155">In the Commission percentage field, enter a number.</span></span>
36. <span data-ttu-id="a2e85-156">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="a2e85-156">Click Save.</span></span>

## <a name="setting-up-commission-posting"></a><span data-ttu-id="a2e85-157">Provision kirjauksen määrittäminen</span><span class="sxs-lookup"><span data-stu-id="a2e85-157">Setting up commission posting</span></span>
1. <span data-ttu-id="a2e85-158">Valitse Myynti ja markkinointi > Provisiot > Provision kirjaus.</span><span class="sxs-lookup"><span data-stu-id="a2e85-158">Go to Sales and marketing > Commissions > Commission posting.</span></span>
    * <span data-ttu-id="a2e85-159">Provisiot maksetaan työntekijöille, joten ne on määritettävä varmistamaan, että taloudellinen kirjaus tehdään oikein asianmukaisille tileille kirjanpidossa.</span><span class="sxs-lookup"><span data-stu-id="a2e85-159">Commission fees are payable to the employees and must therefore be set up to ensure correct financial posting to the appropriate accounts in the General ledger.</span></span> <span data-ttu-id="a2e85-160">Se tehdään Provision kirjaus -sivulle.</span><span class="sxs-lookup"><span data-stu-id="a2e85-160">This is done in the Commission posting page.</span></span> <span data-ttu-id="a2e85-161">Tarkista nykyisessä yrityksessä käytettävissä oleva asetus.</span><span class="sxs-lookup"><span data-stu-id="a2e85-161">Review the setup that is available for the current company.</span></span> <span data-ttu-id="a2e85-162">Yleensä provisiosummat kirjataan erityiskulutilille ja vastakirjataan erityisostoreskontraan.</span><span class="sxs-lookup"><span data-stu-id="a2e85-162">Typically, the commission amounts are posted to a dedicated expense account and are offset to a dedicated payable account.</span></span> <span data-ttu-id="a2e85-163">Jos et ole määrittänyt provision kirjaussääntöjä, järjestelmä ei suorita provisioon oikeuttavien myyntitilausten laskutusta.</span><span class="sxs-lookup"><span data-stu-id="a2e85-163">If you don't have the commission posting rules set up, the system will fail to complete invoicing of a sales order which has eligible commissions.</span></span>  
2. <span data-ttu-id="a2e85-164">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="a2e85-164">Close the page.</span></span>

## <a name="assign-a-commission-group-to-a-customer-and-a-product"></a><span data-ttu-id="a2e85-165">Määritä provisioryhmä asiakkaaseen ja tuotteeseen</span><span class="sxs-lookup"><span data-stu-id="a2e85-165">Assign a commission group to a customer and a product</span></span>
1. <span data-ttu-id="a2e85-166">Valitse Myynti ja markkinointi > Asiakkaat > Kaikki asiakkaat.</span><span class="sxs-lookup"><span data-stu-id="a2e85-166">Go to Sales and marketing > Customers > All customers.</span></span>
2. <span data-ttu-id="a2e85-167">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="a2e85-167">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="a2e85-168">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="a2e85-168">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="a2e85-169">Valitse Muokkaa.</span><span class="sxs-lookup"><span data-stu-id="a2e85-169">Click Edit.</span></span>
5. <span data-ttu-id="a2e85-170">Laajenna Oletusmyyntitilaukset-osa.</span><span class="sxs-lookup"><span data-stu-id="a2e85-170">Expand the Sales order defaults section.</span></span>
6. <span data-ttu-id="a2e85-171">Avaa haku napsauttamalla Provisioryhmä-kentässä avattavan valikon painiketta.</span><span class="sxs-lookup"><span data-stu-id="a2e85-171">In the Commission group field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="a2e85-172">Valitse luettelosta aiemmin luomasi ryhmä.</span><span class="sxs-lookup"><span data-stu-id="a2e85-172">In the list, select the group that you created earlier.</span></span>
8. <span data-ttu-id="a2e85-173">Avaa haku napsauttamalla Myyntiryhmä-kentässä avattavan valikon painiketta.</span><span class="sxs-lookup"><span data-stu-id="a2e85-173">In the Sales group field, click the drop-down button to open the lookup.</span></span>
9. <span data-ttu-id="a2e85-174">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="a2e85-174">In the list, find and select the desired record.</span></span>
10. <span data-ttu-id="a2e85-175">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="a2e85-175">Click Save.</span></span>
11. <span data-ttu-id="a2e85-176">Mene Tuotetietojen hallinta > Tuotteet > Vapautetut tuotteet.</span><span class="sxs-lookup"><span data-stu-id="a2e85-176">Go to Product information management > Products > Released products.</span></span>
12. <span data-ttu-id="a2e85-177">Käytä pikasuodatinta tietueiden etsimiseen.</span><span class="sxs-lookup"><span data-stu-id="a2e85-177">Use the Quick Filter to find records.</span></span> <span data-ttu-id="a2e85-178">Voit esimerkiksi suodattaa Nimiketunnus-kenttää arvolla T0020.</span><span class="sxs-lookup"><span data-stu-id="a2e85-178">For example, filter on the Item number field with a value of 'T0020 '.</span></span>
13. <span data-ttu-id="a2e85-179">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="a2e85-179">In the list, click the link in the selected row.</span></span>
14. <span data-ttu-id="a2e85-180">Valitse Muokkaa.</span><span class="sxs-lookup"><span data-stu-id="a2e85-180">Click Edit.</span></span>
15. <span data-ttu-id="a2e85-181">Laajenna Myynti-osa.</span><span class="sxs-lookup"><span data-stu-id="a2e85-181">Expand the Sell section.</span></span>
16. <span data-ttu-id="a2e85-182">Avaa haku napsauttamalla Provisioryhmä-kentässä avattavan valikon painiketta.</span><span class="sxs-lookup"><span data-stu-id="a2e85-182">In the Commission group field, click the drop-down button to open the lookup.</span></span>
17. <span data-ttu-id="a2e85-183">Etsi ja valitse luettelosta aiemmin luomasi provisioryhmä.</span><span class="sxs-lookup"><span data-stu-id="a2e85-183">In the list, select the commission group that you created earlier.</span></span>

