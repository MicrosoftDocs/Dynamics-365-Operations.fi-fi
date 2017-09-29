--- 
title: "Ota käyttöön rekisterikilven etiketin tulostus"
description: "Näin sarjatoimitusyksikkökoodin (SSCC) etiketti voidaan tulostaa automaattisesti varastosta viimeksi kerätyn nimikkeen jälkeen myynnin keräystyöprosessissa."
author: perlynne
manager: AnnBe
ms.date: 11/03/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 6d186bf7e4aee8cfa97adbd90b9090085e842f9b
ms.contentlocale: fi-fi
ms.lasthandoff: 08/29/2017

---
# <a name="enable-license-plate-label-printing"></a><span data-ttu-id="2ea2c-103">Ota käyttöön rekisterikilven etiketin tulostus</span><span class="sxs-lookup"><span data-stu-id="2ea2c-103">Enable license plate label printing</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="2ea2c-104">Näin sarjatoimitusyksikkökoodin (SSCC) etiketti voidaan tulostaa automaattisesti varastosta viimeksi kerätyn nimikkeen jälkeen myynnin keräystyöprosessissa.</span><span class="sxs-lookup"><span data-stu-id="2ea2c-104">This procedure enables the automatic printing of a Serial shipping container code (SSCC) label after the last item is picked from inventory in a sales picking work process.</span></span> <span data-ttu-id="2ea2c-105">Voit suorittaa tämän menettelyn esittely-yrityksessä USMF.</span><span class="sxs-lookup"><span data-stu-id="2ea2c-105">You can run this procedure in demo data company USMF.</span></span> <span data-ttu-id="2ea2c-106">Jos suoritit menettelyn omien tietojen avulla, rekisterikilville on määritettävä numerosarja.</span><span class="sxs-lookup"><span data-stu-id="2ea2c-106">If you’re run it using your own data, you need to have a number sequence set up for license plates.</span></span> <span data-ttu-id="2ea2c-107">Määritä etikettitulostin, ennen kuin aloitat tämän tehtävän.</span><span class="sxs-lookup"><span data-stu-id="2ea2c-107">You need to set up a label printer before you begin this task.</span></span> <span data-ttu-id="2ea2c-108">Valitse Organisaation hallinta > Asetukset > Verkkotulostimet.</span><span class="sxs-lookup"><span data-stu-id="2ea2c-108">Go to Organization administration > Setup > Network printers.</span></span> <span data-ttu-id="2ea2c-109">Valitse toimintoruudussa Asetukset ja valitse sitten Lataa asiakirjan reititysagentin asennusohjelma -painike.</span><span class="sxs-lookup"><span data-stu-id="2ea2c-109">On the Action pane, click Options, and then click the Download document routing agent installer button.</span></span> <span data-ttu-id="2ea2c-110">Suorita asennusohjelma ja varmista, että toimiva verkkotulostin on määritetty aktiiviseksi, ennen kuin jatkat.</span><span class="sxs-lookup"><span data-stu-id="2ea2c-110">Run the installer and make sure that you have a working network printer set to Active before you continue with the procedure.</span></span>


## <a name="set-up-the-gs1-company-prefix"></a><span data-ttu-id="2ea2c-111">Yrityksen GS1-etuliitteen määrittäminen</span><span class="sxs-lookup"><span data-stu-id="2ea2c-111">Set up the GS1 company prefix</span></span>
1. <span data-ttu-id="2ea2c-112">Valitse Varastonhallinta > Asetukset > Varastonhallinnan parametrit.</span><span class="sxs-lookup"><span data-stu-id="2ea2c-112">Go to Warehouse management > Setup > Warehouse management parameters.</span></span>
2. <span data-ttu-id="2ea2c-113">Syötä yrityksen GS1-etuliite -kenttään GS1-yritysnumeron 7 numeroa.</span><span class="sxs-lookup"><span data-stu-id="2ea2c-113">In the GS1 company prefix field, enter the 7 numbers for your GS1 company number.</span></span>
3. <span data-ttu-id="2ea2c-114">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="2ea2c-114">Click Save.</span></span>
4. <span data-ttu-id="2ea2c-115">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="2ea2c-115">Close the page.</span></span>

## <a name="setup-the-sscc-license-plate-number-sequence"></a><span data-ttu-id="2ea2c-116">SSCC-rekisterinumeron järjestyksen määrittäminen</span><span class="sxs-lookup"><span data-stu-id="2ea2c-116">Setup the SSCC license plate number sequence</span></span>
1. <span data-ttu-id="2ea2c-117">Siirry kohtaan Organisaation hallinta > Numerosarjat > Numerosarjat.</span><span class="sxs-lookup"><span data-stu-id="2ea2c-117">Go to Organization administration > Number sequences > Number sequences.</span></span>
2. <span data-ttu-id="2ea2c-118">Valitse Alue-kentässä vaihtoehto.</span><span class="sxs-lookup"><span data-stu-id="2ea2c-118">In the Area field, select an option.</span></span>
3. <span data-ttu-id="2ea2c-119">Valitse Viite-kentässä vaihtoehto.</span><span class="sxs-lookup"><span data-stu-id="2ea2c-119">In the Reference field, select an option.</span></span>
4. <span data-ttu-id="2ea2c-120">Kirjoita arvo Yritys-kenttään.</span><span class="sxs-lookup"><span data-stu-id="2ea2c-120">In the Company field, type a value.</span></span>
5. <span data-ttu-id="2ea2c-121">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="2ea2c-121">In the list, mark the selected row.</span></span>
6. <span data-ttu-id="2ea2c-122">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="2ea2c-122">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="2ea2c-123">Laajenna Segmentit-osa.</span><span class="sxs-lookup"><span data-stu-id="2ea2c-123">Expand the Segments section.</span></span>
8. <span data-ttu-id="2ea2c-124">Valitse Muokkaa.</span><span class="sxs-lookup"><span data-stu-id="2ea2c-124">Click Edit.</span></span>
9. <span data-ttu-id="2ea2c-125">Valitse Segmentit-taulukon ensimmäinen rivi.</span><span class="sxs-lookup"><span data-stu-id="2ea2c-125">In the Segments table, select the first row</span></span>
10. <span data-ttu-id="2ea2c-126">Valitse Poista.</span><span class="sxs-lookup"><span data-stu-id="2ea2c-126">Click Remove.</span></span>
11. <span data-ttu-id="2ea2c-127">Valitse Poista.</span><span class="sxs-lookup"><span data-stu-id="2ea2c-127">Click Remove.</span></span>
12. <span data-ttu-id="2ea2c-128">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="2ea2c-128">Click Save.</span></span>
13. <span data-ttu-id="2ea2c-129">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="2ea2c-129">Close the page.</span></span>

## <a name="create-the-document-route-layout"></a><span data-ttu-id="2ea2c-130">Asiakirjan reittiasettelun luominen</span><span class="sxs-lookup"><span data-stu-id="2ea2c-130">Create the document route layout</span></span>
1. <span data-ttu-id="2ea2c-131">Valitse Varastonhallinta >> Asetukset > Asiakirjan reititys > Asiakirjan reititysasettelut.</span><span class="sxs-lookup"><span data-stu-id="2ea2c-131">Go to Warehouse management > Setup > Document routing > Document routing layouts.</span></span>
    * <span data-ttu-id="2ea2c-132">Ota SSCC-asettelu käyttöön.</span><span class="sxs-lookup"><span data-stu-id="2ea2c-132">Enable the SSCC layout.</span></span>  
2. <span data-ttu-id="2ea2c-133">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="2ea2c-133">Click New.</span></span>
3. <span data-ttu-id="2ea2c-134">Kirjoita Asettelun tunnus -kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="2ea2c-134">In the Layout ID field, type a value.</span></span>
4. <span data-ttu-id="2ea2c-135">Kirjoita arvo Kuvaus-kenttään.</span><span class="sxs-lookup"><span data-stu-id="2ea2c-135">In the Description field, type a value.</span></span>
5. <span data-ttu-id="2ea2c-136">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="2ea2c-136">In the list, find and select the desired record.</span></span>
6. <span data-ttu-id="2ea2c-137">Valitse Lisää tekstin loppuun.</span><span class="sxs-lookup"><span data-stu-id="2ea2c-137">Click Insert at end of text.</span></span>
7. <span data-ttu-id="2ea2c-138">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="2ea2c-138">Click Save.</span></span>
8. <span data-ttu-id="2ea2c-139">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="2ea2c-139">Close the page.</span></span>

## <a name="set-up-the-document-routing"></a><span data-ttu-id="2ea2c-140">Asiakirjan reitityksen määrittäminen</span><span class="sxs-lookup"><span data-stu-id="2ea2c-140">Set up the document routing</span></span>
1. <span data-ttu-id="2ea2c-141">Valitse Varastonhallinta > Asetukset > Asiakirjan reititys > Asiakirjan reititys.</span><span class="sxs-lookup"><span data-stu-id="2ea2c-141">Go to Warehouse management > Setup > Document routing > Document routing.</span></span>
2. <span data-ttu-id="2ea2c-142">Valitse Työtilauksen tyyppi -kentässä vaihtoehto.</span><span class="sxs-lookup"><span data-stu-id="2ea2c-142">In the Work order type field, select an option.</span></span>
3. <span data-ttu-id="2ea2c-143">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="2ea2c-143">Click New.</span></span>
4. <span data-ttu-id="2ea2c-144">Kirjoita arvo Varasto-kenttään.</span><span class="sxs-lookup"><span data-stu-id="2ea2c-144">In the Warehouse field, type a value.</span></span>
5. <span data-ttu-id="2ea2c-145">Kirjoita arvo Nimi-kenttään.</span><span class="sxs-lookup"><span data-stu-id="2ea2c-145">In the Name field, type a value.</span></span>
6. <span data-ttu-id="2ea2c-146">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="2ea2c-146">Click New.</span></span>
7. <span data-ttu-id="2ea2c-147">Syötä tai valitse arvo Asettelun tunnus -kenttään.</span><span class="sxs-lookup"><span data-stu-id="2ea2c-147">In the Layout ID field, enter or select a value.</span></span>
8. <span data-ttu-id="2ea2c-148">Valitse Nimi-kentästä tulostin, jota haluat käyttää.</span><span class="sxs-lookup"><span data-stu-id="2ea2c-148">In the Name field, enter the printer name that you want to use..</span></span>
9. <span data-ttu-id="2ea2c-149">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="2ea2c-149">Click Save.</span></span>
10. <span data-ttu-id="2ea2c-150">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="2ea2c-150">Close the page.</span></span>

## <a name="create-mobile-device-menu"></a><span data-ttu-id="2ea2c-151">Mobiililaitteen valikon luominen</span><span class="sxs-lookup"><span data-stu-id="2ea2c-151">Create mobile device menu</span></span>
1. <span data-ttu-id="2ea2c-152">Valitse Varastonhallinta > Asetukset > Mobiililaite > Mobiililaitteen valikkovaihtoehdot.</span><span class="sxs-lookup"><span data-stu-id="2ea2c-152">Go to Warehouse management > Setup > Mobile device > Mobile device menu items.</span></span>
2. <span data-ttu-id="2ea2c-153">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="2ea2c-153">Click New.</span></span>
3. <span data-ttu-id="2ea2c-154">Kirjoita arvo Valikkovaihtoehdon nimi -kenttään.</span><span class="sxs-lookup"><span data-stu-id="2ea2c-154">In the Menu item name field, type a value.</span></span>
4. <span data-ttu-id="2ea2c-155">Kirjoita Otsikko-kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="2ea2c-155">In the Title field, type a value.</span></span>
5. <span data-ttu-id="2ea2c-156">Valitse Tapa-kentässä vaihtoehto.</span><span class="sxs-lookup"><span data-stu-id="2ea2c-156">In the Mode field, select an option.</span></span>
6. <span data-ttu-id="2ea2c-157">Valitse Käytä nykyistä työtä -kentässä Kyllä.</span><span class="sxs-lookup"><span data-stu-id="2ea2c-157">Select Yes in the Use existing work field.</span></span>
7. <span data-ttu-id="2ea2c-158">Valitse Muodosta rekisterikilpi -kentässä Kyllä.</span><span class="sxs-lookup"><span data-stu-id="2ea2c-158">Select Yes in the Generate license plate field.</span></span>
8. <span data-ttu-id="2ea2c-159">Laajenna Työluokat-osa.</span><span class="sxs-lookup"><span data-stu-id="2ea2c-159">Expand the Work classes section.</span></span>
9. <span data-ttu-id="2ea2c-160">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="2ea2c-160">Click New.</span></span>
10. <span data-ttu-id="2ea2c-161">Kirjoita Työluokan tunnus -kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="2ea2c-161">In the Work class ID field, type a value.</span></span>
11. <span data-ttu-id="2ea2c-162">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="2ea2c-162">Click Save.</span></span>
12. <span data-ttu-id="2ea2c-163">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="2ea2c-163">Close the page.</span></span>
13. <span data-ttu-id="2ea2c-164">Valitse Varastonhallinta > Asetukset > Mobiililaite > Mobiililaitteen valikko.</span><span class="sxs-lookup"><span data-stu-id="2ea2c-164">Go to Warehouse management > Setup > Mobile device > Mobile device menu.</span></span>
14. <span data-ttu-id="2ea2c-165">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="2ea2c-165">In the list, find and select the desired record.</span></span>
15. <span data-ttu-id="2ea2c-166">Valitse puussa solmu In the tree, select the menu item that you created before.</span><span class="sxs-lookup"><span data-stu-id="2ea2c-166">In the tree, select 'In the tree, select the menu item that you created before.'.</span></span>
16. <span data-ttu-id="2ea2c-167">Valitse Muokkaa.</span><span class="sxs-lookup"><span data-stu-id="2ea2c-167">Click Edit.</span></span>
17. <span data-ttu-id="2ea2c-168">Lisää valikkovaihtoehto valikkoon nuolen avulla.</span><span class="sxs-lookup"><span data-stu-id="2ea2c-168">Click on the arrow to add the menu item to the menu.</span></span>
18. <span data-ttu-id="2ea2c-169">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="2ea2c-169">Click Save.</span></span>
19. <span data-ttu-id="2ea2c-170">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="2ea2c-170">Close the page.</span></span>

## <a name="update-a-work-template"></a><span data-ttu-id="2ea2c-171">Työmallin päivittäminen</span><span class="sxs-lookup"><span data-stu-id="2ea2c-171">Update a work template</span></span>
1. <span data-ttu-id="2ea2c-172">Valitse Varastonhallinta > Asetukset > Työ > Työmallit.</span><span class="sxs-lookup"><span data-stu-id="2ea2c-172">Go to Warehouse management > Setup > Work > Work templates.</span></span>
2. <span data-ttu-id="2ea2c-173">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="2ea2c-173">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="2ea2c-174">Valitse Muokkaa.</span><span class="sxs-lookup"><span data-stu-id="2ea2c-174">Click Edit.</span></span>
4. <span data-ttu-id="2ea2c-175">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="2ea2c-175">Click New.</span></span>
5. <span data-ttu-id="2ea2c-176">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="2ea2c-176">In the list, mark the selected row.</span></span>
6. <span data-ttu-id="2ea2c-177">Valitse Työtyyppi-kentässä Tulosta.</span><span class="sxs-lookup"><span data-stu-id="2ea2c-177">In the Work type field, select 'Print'.</span></span>
7. <span data-ttu-id="2ea2c-178">Syötä tai valitse arvo Työluokan tunnus -kenttään.</span><span class="sxs-lookup"><span data-stu-id="2ea2c-178">In the Work class ID field, enter or select a value.</span></span>
8. <span data-ttu-id="2ea2c-179">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="2ea2c-179">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="2ea2c-180">Valitse Siirrä ylöspäin.</span><span class="sxs-lookup"><span data-stu-id="2ea2c-180">Click Move up.</span></span>
10. <span data-ttu-id="2ea2c-181">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="2ea2c-181">Click Save.</span></span>
11. <span data-ttu-id="2ea2c-182">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="2ea2c-182">Close the page.</span></span>


