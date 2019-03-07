---
title: Nimikkeiden kattavuussääntöjen määrittäminen
description: Tämän menettelyn luomisessa käytetty esittely-yritys on USMF.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqGroup, DefaultDashboard, EcoResProductDetailsExtended, EcoResProductCreate, InventItemOrderSetup, ReqItemTable
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 02aa3b2b7924cdf6317225bfce23f182aa390b8c
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/29/2019
ms.locfileid: "320624"
---
# <a name="define-coverage-rules-for-items"></a><span data-ttu-id="886eb-103">Nimikkeiden kattavuussääntöjen määrittäminen</span><span class="sxs-lookup"><span data-stu-id="886eb-103">Define coverage rules for items</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="886eb-104">Tämän menettelyn luomisessa käytetty esittely-yritys on USMF.</span><span class="sxs-lookup"><span data-stu-id="886eb-104">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="886eb-105">Tässä menettelyssä näytetään, miten tietyn nimikkeen kattavuussäännöt luodaan ja kattavuusasetukset korvataan.</span><span class="sxs-lookup"><span data-stu-id="886eb-105">This procedure shows how to create coverage rules and override coverage settings for a specific item.</span></span> <span data-ttu-id="886eb-106">Siinä näytetään myös, miten oletusvarastoasetukset määritetään.</span><span class="sxs-lookup"><span data-stu-id="886eb-106">It also shows how to specify default inventory settings.</span></span>


## <a name="create-a-coverage-group"></a><span data-ttu-id="886eb-107">Kattavuusryhmän luominen</span><span class="sxs-lookup"><span data-stu-id="886eb-107">Create a coverage group</span></span>
1. <span data-ttu-id="886eb-108">Siirry Kattavuusryhmät-kohtaan.</span><span class="sxs-lookup"><span data-stu-id="886eb-108">Go to Coverage groups.</span></span>
2. <span data-ttu-id="886eb-109">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="886eb-109">Click New.</span></span>
3. <span data-ttu-id="886eb-110">Kirjoita Kattavuusryhmä-kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="886eb-110">In the Coverage group field, type a value.</span></span>
4. <span data-ttu-id="886eb-111">Kirjoita arvo Nimi-kenttään.</span><span class="sxs-lookup"><span data-stu-id="886eb-111">In the Name field, type a value.</span></span>
5. <span data-ttu-id="886eb-112">Kirjoita Kalenteri-kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="886eb-112">In the Calendar field, type a value.</span></span>
    * <span data-ttu-id="886eb-113">Valitse kalenteri, jota pääsuunnittelu käyttää tämän ryhmän nimikkeiden täydennysehdotusten luomisessa.</span><span class="sxs-lookup"><span data-stu-id="886eb-113">Choose the calendar that master planning uses to create replenishment suggestions for items in this group.</span></span>  
6. <span data-ttu-id="886eb-114">Valitse Kattavuuskoodi-kentässä vaihtoehto.</span><span class="sxs-lookup"><span data-stu-id="886eb-114">In the Coverage code field, select an option.</span></span>
    * <span data-ttu-id="886eb-115">Valitse tämän menettelyn Tarve.</span><span class="sxs-lookup"><span data-stu-id="886eb-115">Select Requirement for this procedure.</span></span>  
7. <span data-ttu-id="886eb-116">Syötä Kattavuuden aikaraja (päivää) -kenttään 90.</span><span class="sxs-lookup"><span data-stu-id="886eb-116">In the Coverage time fence (days) field, enter '90'.</span></span>
    * <span data-ttu-id="886eb-117">Pääsuunnittelu luo tämän ryhmän nimikkeille täydennysehdotukset enintään 90 päivän ajalle tulevaisuuteen.</span><span class="sxs-lookup"><span data-stu-id="886eb-117">For items in this group, master planning will create replenishment suggestions for up to 90 days in the future.</span></span>  
8. <span data-ttu-id="886eb-118">Syötä Negatiiviset päivät -kenttään 1.</span><span class="sxs-lookup"><span data-stu-id="886eb-118">In the Negative days field, enter '1'.</span></span>
9. <span data-ttu-id="886eb-119">Syötä Positiiviset päivät -kenttään 1.</span><span class="sxs-lookup"><span data-stu-id="886eb-119">In the Positive days field, enter '1'.</span></span>
10. <span data-ttu-id="886eb-120">Laajenna tai tiivistä Muu-osa.</span><span class="sxs-lookup"><span data-stu-id="886eb-120">Expand or collapse the Other section.</span></span>
11. <span data-ttu-id="886eb-121">Syötä Tarvepäivään lisätty vastaanottomarginaali -kenttään 1.</span><span class="sxs-lookup"><span data-stu-id="886eb-121">In the Receipt margin added to requirement date field, enter '1'.</span></span>
    * <span data-ttu-id="886eb-122">Jos esimerkiksi vastaanottomarginaaliksi määritetään yksi päivä ja ostotilausrivi on ajoitettu vastaanotettavaksi 15.5., pääsuunnittelu laskee muutetuksi vastaanottopäiväksi 16.5.</span><span class="sxs-lookup"><span data-stu-id="886eb-122">For example, if the receipt margin is set to 1 day, and a purchase order line is scheduled for receipt on May 15, master planning calculates the adjusted receipt date as May 16.</span></span>  
12. <span data-ttu-id="886eb-123">Syötä Tarvepäivästä vähennetty toimitusmarginaali -kenttään 1.</span><span class="sxs-lookup"><span data-stu-id="886eb-123">In the Issue margin deducted from requirement date field, enter '1'.</span></span>
    * <span data-ttu-id="886eb-124">Jos esimerkiksi varmuusmarginaaliksi määritetään yksi päivä ja myyntitilausrivi on ajoitettu toimitettavaksi 15.5., pääajoitus laskee muutetuksi toimituspäiväksi 14.5.</span><span class="sxs-lookup"><span data-stu-id="886eb-124">For example, if the safety margin is set to 1 day, and a sales order line is scheduled for delivery on May 15, master scheduling calculates the adjusted delivery date as May 14.</span></span>  
13. <span data-ttu-id="886eb-125">Syötä Nimikkeen läpimenoaikaan lisätty uudelleenjärjestyksen marginaali -kenttään 1.</span><span class="sxs-lookup"><span data-stu-id="886eb-125">In the Reorder margin added to item lead time field, enter '1'.</span></span>
14. <span data-ttu-id="886eb-126">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="886eb-126">Click Save.</span></span>

## <a name="create-a-new-product"></a><span data-ttu-id="886eb-127">Luo uusi tuote</span><span class="sxs-lookup"><span data-stu-id="886eb-127">Create a new product</span></span>
1. <span data-ttu-id="886eb-128">Siirry Vapautetut tuotteet -kohtaan.</span><span class="sxs-lookup"><span data-stu-id="886eb-128">Go to Released products.</span></span>
2. <span data-ttu-id="886eb-129">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="886eb-129">Click New.</span></span>
3. <span data-ttu-id="886eb-130">Kirjoita arvo Tuotenumero-kenttään.</span><span class="sxs-lookup"><span data-stu-id="886eb-130">In the Product number field, type a value.</span></span>
4. <span data-ttu-id="886eb-131">Kirjoita arvo Tuotteen nimi -kenttään.</span><span class="sxs-lookup"><span data-stu-id="886eb-131">In the Product name field, type a value.</span></span>
5. <span data-ttu-id="886eb-132">Avaa haku valitsemalla Nimikemalliryhmä-kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="886eb-132">In the Item model group field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="886eb-133">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="886eb-133">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="886eb-134">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="886eb-134">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="886eb-135">Avaa haku valitsemalla Nimikeryhmä-kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="886eb-135">In the Item group field, click the drop-down button to open the lookup.</span></span>
9. <span data-ttu-id="886eb-136">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="886eb-136">In the list, find and select the desired record.</span></span>
10. <span data-ttu-id="886eb-137">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="886eb-137">In the list, click the link in the selected row.</span></span>
11. <span data-ttu-id="886eb-138">Avaa haku valitsemalla Varastodimensioryhmä-kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="886eb-138">In the Storage dimension group field, click the drop-down button to open the lookup.</span></span>
12. <span data-ttu-id="886eb-139">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="886eb-139">In the list, find and select the desired record.</span></span>
13. <span data-ttu-id="886eb-140">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="886eb-140">In the list, click the link in the selected row.</span></span>
14. <span data-ttu-id="886eb-141">Avaa haku valitsemalla Seurantadimensioryhmä-kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="886eb-141">In the Tracking dimension group field, click the drop-down button to open the lookup.</span></span>
15. <span data-ttu-id="886eb-142">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="886eb-142">In the list, find and select the desired record.</span></span>
16. <span data-ttu-id="886eb-143">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="886eb-143">In the list, click the link in the selected row.</span></span>
17. <span data-ttu-id="886eb-144">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="886eb-144">Click OK.</span></span>

## <a name="setup-default-order-settings"></a><span data-ttu-id="886eb-145">Tilauksen oletusasetusten määrittäminen</span><span class="sxs-lookup"><span data-stu-id="886eb-145">Setup default order settings</span></span>
1. <span data-ttu-id="886eb-146">Valitse toimintoruudussa Suunnitelma.</span><span class="sxs-lookup"><span data-stu-id="886eb-146">On the Action Pane, click Plan.</span></span>
2. <span data-ttu-id="886eb-147">Valitse Tilauksen oletusasetukset.</span><span class="sxs-lookup"><span data-stu-id="886eb-147">Click Default order settings.</span></span>
3. <span data-ttu-id="886eb-148">Kirjoita Ostotoimipaikka-kenttään toimipaikka, jota käytetään oletusarvona ostotilausten luomisen yhteydessä.</span><span class="sxs-lookup"><span data-stu-id="886eb-148">In the Purchase site field, type the site used as default when purchase orders are created.</span></span>
4. <span data-ttu-id="886eb-149">Kirjoita Varastotoimipaikka-kenttään toimipaikka, joka on nimikkeen varasto.</span><span class="sxs-lookup"><span data-stu-id="886eb-149">In the Inventory site field, type the site where the item is stored.</span></span>
5. <span data-ttu-id="886eb-150">Laajenna tai tiivistä Varasto-osa.</span><span class="sxs-lookup"><span data-stu-id="886eb-150">Expand or collapse the Inventory section.</span></span>
6. <span data-ttu-id="886eb-151">Määritä Useita-kohdan arvoksi 10.</span><span class="sxs-lookup"><span data-stu-id="886eb-151">Set Multiple to '10'.</span></span>
7. <span data-ttu-id="886eb-152">Määritä</span><span class="sxs-lookup"><span data-stu-id="886eb-152">Set Min.</span></span> <span data-ttu-id="886eb-153">Väh.tilausmäärä-kohdan arvoksi 10.</span><span class="sxs-lookup"><span data-stu-id="886eb-153">order quantity to '10'.</span></span>
8. <span data-ttu-id="886eb-154">Määritä</span><span class="sxs-lookup"><span data-stu-id="886eb-154">Set Max.</span></span> <span data-ttu-id="886eb-155">Enimm.tilausmäärä-kohdan arvoksi 100.</span><span class="sxs-lookup"><span data-stu-id="886eb-155">order quantity to '100'.</span></span>
9. <span data-ttu-id="886eb-156">Määritä Vakiotilausmäärä-kohdan arvoksi 10.</span><span class="sxs-lookup"><span data-stu-id="886eb-156">Set Standard order quantity to '10'.</span></span>
10. <span data-ttu-id="886eb-157">Syötä Oston läpimenoaika -kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="886eb-157">In the Purchase lead time field, enter a number.</span></span>
11. <span data-ttu-id="886eb-158">Valitse Työpäivät-valintaruutu tai poista sen valinta.</span><span class="sxs-lookup"><span data-stu-id="886eb-158">Select or clear the Working days check box.</span></span>
12. <span data-ttu-id="886eb-159">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="886eb-159">Click Save.</span></span>
13. <span data-ttu-id="886eb-160">Valitse Oletustilaustyyppi-kenttään Ostotilaus.</span><span class="sxs-lookup"><span data-stu-id="886eb-160">In the Default order type field select 'Purchase order'.</span></span>
14. <span data-ttu-id="886eb-161">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="886eb-161">Click Save.</span></span>
15. <span data-ttu-id="886eb-162">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="886eb-162">Close the page.</span></span>
    * <span data-ttu-id="886eb-163">Sulje Tilauksen oletusasetukset -sivu.</span><span class="sxs-lookup"><span data-stu-id="886eb-163">Close the Default order settings page.</span></span>  

## <a name="add-an-item-to-a-coverage-group"></a><span data-ttu-id="886eb-164">Nimikkeen lisääminen kattavuusryhmään</span><span class="sxs-lookup"><span data-stu-id="886eb-164">Add an item to a coverage group</span></span>
1. <span data-ttu-id="886eb-165">Laajenna tai tiivistä Suunnitelma-osa.</span><span class="sxs-lookup"><span data-stu-id="886eb-165">Expand or collapse the Plan section.</span></span>
2. <span data-ttu-id="886eb-166">Avaa haku napsauttamalla Kattavuusryhmä-kentässä avattavan valikon painiketta.</span><span class="sxs-lookup"><span data-stu-id="886eb-166">In the Coverage group field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="886eb-167">Etsi luettelosta luomasi kattavuusryhmä.</span><span class="sxs-lookup"><span data-stu-id="886eb-167">In the list, find the Coverage group you have created.</span></span>
4. <span data-ttu-id="886eb-168">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="886eb-168">In the list, click the link in the selected row.</span></span>

## <a name="create-item-coverage-rules"></a><span data-ttu-id="886eb-169">Nimikkeen kattavuussääntöjen luominen</span><span class="sxs-lookup"><span data-stu-id="886eb-169">Create item coverage rules</span></span>
1. <span data-ttu-id="886eb-170">Valitse toimintoruudussa Suunnitelma.</span><span class="sxs-lookup"><span data-stu-id="886eb-170">On the Action Pane, click Plan.</span></span>
2. <span data-ttu-id="886eb-171">Valitse Nimikekattavuus.</span><span class="sxs-lookup"><span data-stu-id="886eb-171">Click Item coverage.</span></span>
3. <span data-ttu-id="886eb-172">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="886eb-172">Click New.</span></span>
4. <span data-ttu-id="886eb-173">Valitse Yleiset-välilehti.</span><span class="sxs-lookup"><span data-stu-id="886eb-173">Click the General tab.</span></span>
5. <span data-ttu-id="886eb-174">Valitse Korvaa kattavuusryhmän asetukset -kohdan otsikossa valintaruutu.</span><span class="sxs-lookup"><span data-stu-id="886eb-174">Check the box on the header of Override coverage group settings.</span></span>
6. <span data-ttu-id="886eb-175">Syötä Kattavuuden aikaraja (päivää) -kenttään 60.</span><span class="sxs-lookup"><span data-stu-id="886eb-175">In the Coverage time fence (days) field, enter '60'.</span></span>
    * <span data-ttu-id="886eb-176">Vaikka Tarve-kattavuusryhmän nimikkeet on suunniteltu 90 päivän ajalle, tämä nimike suunnitellaan 60 päivän ajalle.</span><span class="sxs-lookup"><span data-stu-id="886eb-176">Although items in coverage group Requiremen are planned 90 days ahead, this item will be planned 60 days ahead.</span></span>  
7. <span data-ttu-id="886eb-177">Syötä Negatiiviset päivät -kenttään 2.</span><span class="sxs-lookup"><span data-stu-id="886eb-177">In the Negative days field, enter '2'.</span></span>
8. <span data-ttu-id="886eb-178">Syötä Positiiviset päivät -kenttään 2.</span><span class="sxs-lookup"><span data-stu-id="886eb-178">In the Positive days field, enter '2'.</span></span>
9. <span data-ttu-id="886eb-179">Valitse Läpimenoaika-välilehti.</span><span class="sxs-lookup"><span data-stu-id="886eb-179">Click the Lead time tab.</span></span>
10. <span data-ttu-id="886eb-180">Valitse Osto-kohdan otsikon valintaruutu.</span><span class="sxs-lookup"><span data-stu-id="886eb-180">Check the box on the header of Purchase.</span></span>
11. <span data-ttu-id="886eb-181">Syötä Ostoaika-kenttään 5.</span><span class="sxs-lookup"><span data-stu-id="886eb-181">In the Purchase time field, enter '5'.</span></span>
12. <span data-ttu-id="886eb-182">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="886eb-182">Click Save.</span></span>

