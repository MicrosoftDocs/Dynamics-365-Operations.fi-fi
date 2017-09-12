--- 
title: "Määritä myyntiprovision säännöt"
description: "Tässä menettelyssä käsitellään, miten myyntiprovision laskenta ja seuranta määritetään ja otetaan käyttöön."
author: omulvad
manager: AnnBe
ms.date: 11/10/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: 0ab5b3b5447e56eb8ed012a67454400cb2357af4
ms.contentlocale: fi-fi
ms.lasthandoff: 07/27/2017

---
# <a name="set-up-sales-commission-rules"></a><span data-ttu-id="610a4-103">Määritä myyntiprovision säännöt</span><span class="sxs-lookup"><span data-stu-id="610a4-103">Set up sales commission rules</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="610a4-104">Tässä menettelyssä käsitellään, miten myyntiprovision laskenta ja seuranta määritetään ja otetaan käyttöön.</span><span class="sxs-lookup"><span data-stu-id="610a4-104">This procedure shows you how to set up and enable sales commission calculation and tracking.</span></span> <span data-ttu-id="610a4-105">Menettely osoittaa, miten asiakas- ja nimikeprovisioryhmät luodaan ja miten valittu asiakas ja tuote linkitetään vastaaviin ryhmiin.</span><span class="sxs-lookup"><span data-stu-id="610a4-105">The procedure shows how to create both customer and item commission groups, and then how to link a selected customer and product to the respective groups.</span></span> <span data-ttu-id="610a4-106">Kyseisiä ryhmiä käytetään sitten provision laskenta-asetuksissa luomaan asiakas-, nimike- ja myyntiedustajayhdistelmä, joka on täsmäytettävä myyntitilaukseen, jotta myyjät saisivat provision.</span><span class="sxs-lookup"><span data-stu-id="610a4-106">Those groups are then used in the commission calculation setup to create a customer, item, and sales representatives combination that must be matched by the sales order to entitle the sales people to a commission.</span></span> <span data-ttu-id="610a4-107">Asiakas- ja nimikeprovisioryhmien on vapaaehtoista, sillä provisio voidaan laskea yksittäisen asiakkaan ja/tai nimikkeen perusteella.</span><span class="sxs-lookup"><span data-stu-id="610a4-107">Creating customer and item commission groups are optional, as the calculation of commission can also be done for an individual customer and/or item.</span></span> <span data-ttu-id="610a4-108">Voit suorittaa tämän menettelyn esittely-yrityksen USMF kanssa tai käyttää omia tietojasi.</span><span class="sxs-lookup"><span data-stu-id="610a4-108">You can run this procedure in demo data company USMF or on your own data.</span></span>


## <a name="set-up-commission-groups-and-commission-rates"></a><span data-ttu-id="610a4-109">Määritä provisioryhmät ja provisioprosentit</span><span class="sxs-lookup"><span data-stu-id="610a4-109">Set up commission groups and commission rates</span></span>
1. <span data-ttu-id="610a4-110">Valitse Myynti ja markkinointi > Provisiot > Provision asiakasryhmät.</span><span class="sxs-lookup"><span data-stu-id="610a4-110">Go to Sales and marketing > Commissions > Customer groups for commission.</span></span>
2. <span data-ttu-id="610a4-111">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="610a4-111">Click New.</span></span>
3. <span data-ttu-id="610a4-112">Kirjoita Ryhmä-kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="610a4-112">In the Group field, type a value.</span></span>
4. <span data-ttu-id="610a4-113">Kirjoita arvo Nimi-kenttään.</span><span class="sxs-lookup"><span data-stu-id="610a4-113">In the Name field, type a value.</span></span>
5. <span data-ttu-id="610a4-114">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="610a4-114">Click Save.</span></span>
6. <span data-ttu-id="610a4-115">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="610a4-115">Close the page.</span></span>
7. <span data-ttu-id="610a4-116">Valitse Myynti ja markkinointi > Provisiot > Nimikeryhmät.</span><span class="sxs-lookup"><span data-stu-id="610a4-116">Go to Sales and marketing > Commissions > Item groups.</span></span>
8. <span data-ttu-id="610a4-117">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="610a4-117">Click New.</span></span>
9. <span data-ttu-id="610a4-118">Kirjoita Ryhmä-kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="610a4-118">In the Group field, type a value.</span></span>
10. <span data-ttu-id="610a4-119">Kirjoita arvo Nimi-kenttään.</span><span class="sxs-lookup"><span data-stu-id="610a4-119">In the Name field, type a value.</span></span>
11. <span data-ttu-id="610a4-120">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="610a4-120">Close the page.</span></span>
12. <span data-ttu-id="610a4-121">Valitse Myynti ja markkinointi > Provisiot > Myyntiryhmät.</span><span class="sxs-lookup"><span data-stu-id="610a4-121">Go to Sales and marketing > Commissions > Sales groups.</span></span>
    * <span data-ttu-id="610a4-122">Provisiomyyntiryhmä määrittää, ketkä työntekijät, joilla on myyntiedustajan rooli, voivat saada provision, kun kyseiseen myyntiryhmään liitetty asiakas ostaa tiettyjä nimikkeitä.</span><span class="sxs-lookup"><span data-stu-id="610a4-122">A Commission sales group specifies the employees in sales representative roles who are eligible to receive a commission when a customer associated with the relevant sales group buys certain items.</span></span>  
    * <span data-ttu-id="610a4-123">USMF-demotietoyrityksessä myyntiryhmä Sales reps US.</span><span class="sxs-lookup"><span data-stu-id="610a4-123">In the USMF demo data company, there is a sales group called "Sales reps US."</span></span>  
13. <span data-ttu-id="610a4-124">Valitse toimintoruudussa Yleiset.</span><span class="sxs-lookup"><span data-stu-id="610a4-124">On the Action Pane, click General.</span></span>
14. <span data-ttu-id="610a4-125">Valitse Myyjä.</span><span class="sxs-lookup"><span data-stu-id="610a4-125">Click Sales rep..</span></span>
    * <span data-ttu-id="610a4-126">Myyntiedustaja-</span><span class="sxs-lookup"><span data-stu-id="610a4-126">The Sales rep.</span></span> <span data-ttu-id="610a4-127">sivulla on luettelo yrityksen tiettyyn provisioryhmään liitetyistä myyjistä.</span><span class="sxs-lookup"><span data-stu-id="610a4-127">page displays a list of the company's sales people who are associated with a specific commission group.</span></span> <span data-ttu-id="610a4-128">Voit määrittää samaan ryhmään useita myyntiedustajia ja määrittää prosentteina kunkin osuuden kokonaisprovisiosta.</span><span class="sxs-lookup"><span data-stu-id="610a4-128">You can assign multiple sales representatives to the same group and define their respective share of the total commission fee as a percentage value.</span></span> <span data-ttu-id="610a4-129">Kaikkien työntekijöiden osuus kokonaisprovisiosta ei voi olla yli 100.</span><span class="sxs-lookup"><span data-stu-id="610a4-129">The total commission share across all employees must not exceed 100.</span></span>  
15. <span data-ttu-id="610a4-130">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="610a4-130">In the list, mark the selected row.</span></span>
16. <span data-ttu-id="610a4-131">Valitse Muokkaa.</span><span class="sxs-lookup"><span data-stu-id="610a4-131">Click Edit.</span></span>
17. <span data-ttu-id="610a4-132">Määritä provisio-osuudeksi 50.</span><span class="sxs-lookup"><span data-stu-id="610a4-132">Set Commission share to '50'.</span></span>
18. <span data-ttu-id="610a4-133">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="610a4-133">Click New.</span></span>
19. <span data-ttu-id="610a4-134">Avaa haku valitsemalla Nimi-kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="610a4-134">In the Name field, click the drop-down button to open the lookup.</span></span>
20. <span data-ttu-id="610a4-135">Käytä pikasuodatinta tietueiden etsimiseen.</span><span class="sxs-lookup"><span data-stu-id="610a4-135">Use the Quick Filter to find records.</span></span> <span data-ttu-id="610a4-136">Voit esimerkiksi suodattaa Nimi-kenttää arvolla Sudan Burk.</span><span class="sxs-lookup"><span data-stu-id="610a4-136">For example, filter on the Name field with a value of 'Susan Burk'.</span></span>
21. <span data-ttu-id="610a4-137">Klikkaa Valitse.</span><span class="sxs-lookup"><span data-stu-id="610a4-137">Click Select.</span></span>
22. <span data-ttu-id="610a4-138">Määritä provisio-osuudeksi 50.</span><span class="sxs-lookup"><span data-stu-id="610a4-138">Set Commission share to '50'.</span></span>
23. <span data-ttu-id="610a4-139">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="610a4-139">Click Save.</span></span>
24. <span data-ttu-id="610a4-140">Valitse Myynti ja markkinointi > Provisiot > Provisiolaskelma.</span><span class="sxs-lookup"><span data-stu-id="610a4-140">Go to Sales and marketing > Commissions > Commission calculation.</span></span>
    * <span data-ttu-id="610a4-141">Voit määrittää Provisiolaskelma-sivulla provisioprosentin, jonka työntekijä saa myyntitapahtumasta, kun se sisältää ennaltamääritetyn asiakas- ja tuoteyhdistelmän.</span><span class="sxs-lookup"><span data-stu-id="610a4-141">In the Commission calculation page you define the commission rate that the employee is to receive for a sales transaction when it contains the pre-set combination of customer and product.</span></span> <span data-ttu-id="610a4-142">Provisioprosenttiasetusten osana on määritettävä provision laskentaperusta sekä alennusten sisällyttäminen tai poissulkeminen.</span><span class="sxs-lookup"><span data-stu-id="610a4-142">As part of the commission rate setup, you must specify the commission calculation basis and whether it should include or exclude discounts.</span></span> <span data-ttu-id="610a4-143">Voit myös antaa voimassaoloajan, jolloin provisioprosentti on aktiivinen.</span><span class="sxs-lookup"><span data-stu-id="610a4-143">You can also enter a validity period for when the commission rate is active.</span></span>  
25. <span data-ttu-id="610a4-144">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="610a4-144">Click New.</span></span>
26. <span data-ttu-id="610a4-145">Valitse Nimikekoodi-kentässä Ryhmä.</span><span class="sxs-lookup"><span data-stu-id="610a4-145">In the Item code field, select 'Group'.</span></span>
27. <span data-ttu-id="610a4-146">Avaa haku napsauttamalla Nimikesuhde-kentässä avattavan valikon painiketta.</span><span class="sxs-lookup"><span data-stu-id="610a4-146">In the Item relation field, click the drop-down button to open the lookup.</span></span>
28. <span data-ttu-id="610a4-147">Etsi ja valitse luettelosta aiemmin luomasi ryhmä.</span><span class="sxs-lookup"><span data-stu-id="610a4-147">In the list, find and select the group that you created earlier.</span></span>
29. <span data-ttu-id="610a4-148">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="610a4-148">In the list, click the link in the selected row.</span></span>
30. <span data-ttu-id="610a4-149">Valitse Asiakaskoodi-kentässä Ryhmä.</span><span class="sxs-lookup"><span data-stu-id="610a4-149">In the Customer code field, select 'Group'.</span></span>
31. <span data-ttu-id="610a4-150">Avaa haku napsauttamalla Asiakassuhde-kentässä avattavan valikon painiketta.</span><span class="sxs-lookup"><span data-stu-id="610a4-150">In the Customer relation field, click the drop-down button to open the lookup.</span></span>
32. <span data-ttu-id="610a4-151">Valitse luettelosta aiemmin määrittämäsi ryhmä.</span><span class="sxs-lookup"><span data-stu-id="610a4-151">In the list, select the group that you set up earlier.</span></span>
33. <span data-ttu-id="610a4-152">Avaa haku napsauttamalla Myyjän</span><span class="sxs-lookup"><span data-stu-id="610a4-152">In the Sales rep.</span></span> <span data-ttu-id="610a4-153">suhde -kentässä avattavan valikon painiketta.</span><span class="sxs-lookup"><span data-stu-id="610a4-153">relation field, click the drop-down button to open the lookup.</span></span>
34. <span data-ttu-id="610a4-154">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="610a4-154">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="610a4-155">Säilytä Ennen rivialennusta -vaihtoehto.</span><span class="sxs-lookup"><span data-stu-id="610a4-155">Keep the "Before line discount" option.</span></span>  
    * <span data-ttu-id="610a4-156">Säilytä Tuotto-vaihtoehto provision arvon laskennan perusteena.</span><span class="sxs-lookup"><span data-stu-id="610a4-156">Keep the "Revenue" option as the basis for commission value calculation.</span></span>    
35. <span data-ttu-id="610a4-157">Lisää Provisioprosentti-kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="610a4-157">In the Commission percentage field, enter a number.</span></span>
36. <span data-ttu-id="610a4-158">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="610a4-158">Click Save.</span></span>

## <a name="setting-up-commission-posting"></a><span data-ttu-id="610a4-159">Provision kirjauksen määrittäminen</span><span class="sxs-lookup"><span data-stu-id="610a4-159">Setting up commission posting</span></span>
1. <span data-ttu-id="610a4-160">Valitse Myynti ja markkinointi > Provisiot > Provision kirjaus.</span><span class="sxs-lookup"><span data-stu-id="610a4-160">Go to Sales and marketing > Commissions > Commission posting.</span></span>
    * <span data-ttu-id="610a4-161">Provisiot maksetaan työntekijöille, joten ne on määritettävä varmistamaan, että taloudellinen kirjaus tehdään oikein asianmukaisille tileille kirjanpidossa.</span><span class="sxs-lookup"><span data-stu-id="610a4-161">Commission fees are payable to the employees and must therefore be set up to ensure correct financial posting to the appropriate accounts in the General ledger.</span></span> <span data-ttu-id="610a4-162">Se tehdään Provision kirjaus -sivulle.</span><span class="sxs-lookup"><span data-stu-id="610a4-162">This is done in the Commission posting page.</span></span> <span data-ttu-id="610a4-163">Tarkista nykyisessä yrityksessä käytettävissä oleva asetus.</span><span class="sxs-lookup"><span data-stu-id="610a4-163">Review the setup that is available for the current company.</span></span> <span data-ttu-id="610a4-164">Yleensä provisiosummat kirjataan erityiskulutilille ja vastakirjataan erityisostoreskontraan.</span><span class="sxs-lookup"><span data-stu-id="610a4-164">Typically, the commission amounts are posted to a dedicated expense account and are offset to a dedicated payable account.</span></span> <span data-ttu-id="610a4-165">Jos et ole määrittänyt provision kirjaussääntöjä, järjestelmä ei suorita provisioon oikeuttavien myyntitilausten laskutusta.</span><span class="sxs-lookup"><span data-stu-id="610a4-165">If you don't have the commission posting rules set up, the system will fail to complete invoicing of a sales order which has eligible commissions.</span></span>  
2. <span data-ttu-id="610a4-166">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="610a4-166">Close the page.</span></span>

## <a name="assign-a-commission-group-to-a-customer-and-a-product"></a><span data-ttu-id="610a4-167">Määritä provisioryhmä asiakkaaseen ja tuotteeseen</span><span class="sxs-lookup"><span data-stu-id="610a4-167">Assign a commission group to a customer and a product</span></span>
1. <span data-ttu-id="610a4-168">Valitse Myynti ja markkinointi > Asiakkaat > Kaikki asiakkaat.</span><span class="sxs-lookup"><span data-stu-id="610a4-168">Go to Sales and marketing > Customers > All customers.</span></span>
2. <span data-ttu-id="610a4-169">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="610a4-169">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="610a4-170">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="610a4-170">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="610a4-171">Valitse Muokkaa.</span><span class="sxs-lookup"><span data-stu-id="610a4-171">Click Edit.</span></span>
5. <span data-ttu-id="610a4-172">Laajenna Oletusmyyntitilaukset-osa.</span><span class="sxs-lookup"><span data-stu-id="610a4-172">Expand the Sales order defaults section.</span></span>
6. <span data-ttu-id="610a4-173">Avaa haku napsauttamalla Provisioryhmä-kentässä avattavan valikon painiketta.</span><span class="sxs-lookup"><span data-stu-id="610a4-173">In the Commission group field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="610a4-174">Valitse luettelosta aiemmin luomasi ryhmä.</span><span class="sxs-lookup"><span data-stu-id="610a4-174">In the list, select the group that you created earlier.</span></span>
8. <span data-ttu-id="610a4-175">Avaa haku napsauttamalla Myyntiryhmä-kentässä avattavan valikon painiketta.</span><span class="sxs-lookup"><span data-stu-id="610a4-175">In the Sales group field, click the drop-down button to open the lookup.</span></span>
9. <span data-ttu-id="610a4-176">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="610a4-176">In the list, find and select the desired record.</span></span>
10. <span data-ttu-id="610a4-177">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="610a4-177">Click Save.</span></span>
11. <span data-ttu-id="610a4-178">Mene Tuotetietojen hallinta > Tuotteet > Vapautetut tuotteet.</span><span class="sxs-lookup"><span data-stu-id="610a4-178">Go to Product information management > Products > Released products.</span></span>
12. <span data-ttu-id="610a4-179">Käytä pikasuodatinta tietueiden etsimiseen.</span><span class="sxs-lookup"><span data-stu-id="610a4-179">Use the Quick Filter to find records.</span></span> <span data-ttu-id="610a4-180">Voit esimerkiksi suodattaa Nimiketunnus-kenttää arvolla T0020.</span><span class="sxs-lookup"><span data-stu-id="610a4-180">For example, filter on the Item number field with a value of 'T0020 '.</span></span>
13. <span data-ttu-id="610a4-181">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="610a4-181">In the list, click the link in the selected row.</span></span>
14. <span data-ttu-id="610a4-182">Valitse Muokkaa.</span><span class="sxs-lookup"><span data-stu-id="610a4-182">Click Edit.</span></span>
15. <span data-ttu-id="610a4-183">Laajenna Myynti-osa.</span><span class="sxs-lookup"><span data-stu-id="610a4-183">Expand the Sell section.</span></span>
16. <span data-ttu-id="610a4-184">Avaa haku napsauttamalla Provisioryhmä-kentässä avattavan valikon painiketta.</span><span class="sxs-lookup"><span data-stu-id="610a4-184">In the Commission group field, click the drop-down button to open the lookup.</span></span>
17. <span data-ttu-id="610a4-185">Etsi ja valitse luettelosta aiemmin luomasi provisioryhmä.</span><span class="sxs-lookup"><span data-stu-id="610a4-185">In the list, select the commission group that you created earlier.</span></span>


