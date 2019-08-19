---
title: Ota käyttöön rekisterikilven etiketin tulostus
description: Näin sarjatoimitusyksikkökoodin (SSCC) etiketti voidaan tulostaa automaattisesti varastosta viimeksi kerätyn nimikkeen jälkeen myynnin keräystyöprosessissa.
author: perlynne
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysCorpNetPrinterList, WHSParameters, NumberSequenceTableListPage, NumberSequenceDetails, WHSDocumentRoutingLayout, WHSDocumentRouting, WHSRFMenuItem, WHSRFMenu, WHSWorkTemplateTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ed74806e5e037570f3ed7f59725eed494c829d34
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/01/2019
ms.locfileid: "1847262"
---
# <a name="enable-license-plate-label-printing"></a><span data-ttu-id="d7ade-103">Ota käyttöön rekisterikilven etiketin tulostus</span><span class="sxs-lookup"><span data-stu-id="d7ade-103">Enable license plate label printing</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="d7ade-104">Näin sarjatoimitusyksikkökoodin (SSCC) etiketti voidaan tulostaa automaattisesti varastosta viimeksi kerätyn nimikkeen jälkeen myynnin keräystyöprosessissa.</span><span class="sxs-lookup"><span data-stu-id="d7ade-104">This procedure enables the automatic printing of a Serial shipping container code (SSCC) label after the last item is picked from inventory in a sales picking work process.</span></span> <span data-ttu-id="d7ade-105">Voit suorittaa tämän menettelyn esittely-yrityksessä USMF.</span><span class="sxs-lookup"><span data-stu-id="d7ade-105">You can run this procedure in demo data company USMF.</span></span> <span data-ttu-id="d7ade-106">Jos suoritit menettelyn omien tietojen avulla, rekisterikilville on määritettävä numerosarja.</span><span class="sxs-lookup"><span data-stu-id="d7ade-106">If you’re run it using your own data, you need to have a number sequence set up for license plates.</span></span> <span data-ttu-id="d7ade-107">Määritä etikettitulostin, ennen kuin aloitat tämän tehtävän.</span><span class="sxs-lookup"><span data-stu-id="d7ade-107">You need to set up a label printer before you begin this task.</span></span> <span data-ttu-id="d7ade-108">Valitse Organisaation hallinta > Asetukset > Verkkotulostimet.</span><span class="sxs-lookup"><span data-stu-id="d7ade-108">Go to Organization administration > Setup > Network printers.</span></span> <span data-ttu-id="d7ade-109">Valitse toimintoruudussa Asetukset ja valitse sitten Lataa asiakirjan reititysagentin asennusohjelma -painike.</span><span class="sxs-lookup"><span data-stu-id="d7ade-109">On the Action pane, click Options, and then click the Download document routing agent installer button.</span></span> <span data-ttu-id="d7ade-110">Suorita asennusohjelma ja varmista, että toimiva verkkotulostin on määritetty aktiiviseksi, ennen kuin jatkat.</span><span class="sxs-lookup"><span data-stu-id="d7ade-110">Run the installer and make sure that you have a working network printer set to Active before you continue with the procedure.</span></span>


## <a name="set-up-the-gs1-company-prefix"></a><span data-ttu-id="d7ade-111">Yrityksen GS1-etuliitteen määrittäminen</span><span class="sxs-lookup"><span data-stu-id="d7ade-111">Set up the GS1 company prefix</span></span>
1. <span data-ttu-id="d7ade-112">Valitse Varastonhallinta > Asetukset > Varastonhallinnan parametrit.</span><span class="sxs-lookup"><span data-stu-id="d7ade-112">Go to Warehouse management > Setup > Warehouse management parameters.</span></span>
2. <span data-ttu-id="d7ade-113">Syötä yrityksen GS1-etuliite -kenttään GS1-yritysnumeron 7 numeroa.</span><span class="sxs-lookup"><span data-stu-id="d7ade-113">In the GS1 company prefix field, enter the 7 numbers for your GS1 company number.</span></span>
3. <span data-ttu-id="d7ade-114">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="d7ade-114">Click Save.</span></span>
4. <span data-ttu-id="d7ade-115">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="d7ade-115">Close the page.</span></span>

## <a name="setup-the-sscc-license-plate-number-sequence"></a><span data-ttu-id="d7ade-116">SSCC-rekisterinumeron järjestyksen määrittäminen</span><span class="sxs-lookup"><span data-stu-id="d7ade-116">Setup the SSCC license plate number sequence</span></span>
1. <span data-ttu-id="d7ade-117">Siirry kohtaan Organisaation hallinta > Numerosarjat > Numerosarjat.</span><span class="sxs-lookup"><span data-stu-id="d7ade-117">Go to Organization administration > Number sequences > Number sequences.</span></span>
2. <span data-ttu-id="d7ade-118">Valitse Alue-kentässä vaihtoehto.</span><span class="sxs-lookup"><span data-stu-id="d7ade-118">In the Area field, select an option.</span></span>
3. <span data-ttu-id="d7ade-119">Valitse Viite-kentässä vaihtoehto.</span><span class="sxs-lookup"><span data-stu-id="d7ade-119">In the Reference field, select an option.</span></span>
4. <span data-ttu-id="d7ade-120">Kirjoita arvo Yritys-kenttään.</span><span class="sxs-lookup"><span data-stu-id="d7ade-120">In the Company field, type a value.</span></span>
5. <span data-ttu-id="d7ade-121">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="d7ade-121">In the list, mark the selected row.</span></span>
6. <span data-ttu-id="d7ade-122">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="d7ade-122">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="d7ade-123">Laajenna Segmentit-osa.</span><span class="sxs-lookup"><span data-stu-id="d7ade-123">Expand the Segments section.</span></span>
8. <span data-ttu-id="d7ade-124">Valitse Muokkaa.</span><span class="sxs-lookup"><span data-stu-id="d7ade-124">Click Edit.</span></span>
9. <span data-ttu-id="d7ade-125">Valitse Segmentit-taulukon ensimmäinen rivi.</span><span class="sxs-lookup"><span data-stu-id="d7ade-125">In the Segments table, select the first row</span></span>
10. <span data-ttu-id="d7ade-126">Valitse Poista.</span><span class="sxs-lookup"><span data-stu-id="d7ade-126">Click Remove.</span></span>
11. <span data-ttu-id="d7ade-127">Valitse Poista.</span><span class="sxs-lookup"><span data-stu-id="d7ade-127">Click Remove.</span></span>
12. <span data-ttu-id="d7ade-128">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="d7ade-128">Click Save.</span></span>
13. <span data-ttu-id="d7ade-129">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="d7ade-129">Close the page.</span></span>

## <a name="create-the-document-route-layout"></a><span data-ttu-id="d7ade-130">Asiakirjan reittiasettelun luominen</span><span class="sxs-lookup"><span data-stu-id="d7ade-130">Create the document route layout</span></span>
1. <span data-ttu-id="d7ade-131">Valitse Varastonhallinta >> Asetukset > Asiakirjan reititys > Asiakirjan reititysasettelut.</span><span class="sxs-lookup"><span data-stu-id="d7ade-131">Go to Warehouse management > Setup > Document routing > Document routing layouts.</span></span>
    * <span data-ttu-id="d7ade-132">Ota SSCC-asettelu käyttöön.</span><span class="sxs-lookup"><span data-stu-id="d7ade-132">Enable the SSCC layout.</span></span>  
2. <span data-ttu-id="d7ade-133">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="d7ade-133">Click New.</span></span>
3. <span data-ttu-id="d7ade-134">Kirjoita Asettelun tunnus -kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="d7ade-134">In the Layout ID field, type a value.</span></span>
4. <span data-ttu-id="d7ade-135">Kirjoita arvo Kuvaus-kenttään.</span><span class="sxs-lookup"><span data-stu-id="d7ade-135">In the Description field, type a value.</span></span>
5. <span data-ttu-id="d7ade-136">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="d7ade-136">In the list, find and select the desired record.</span></span>
6. <span data-ttu-id="d7ade-137">Valitse Lisää tekstin loppuun.</span><span class="sxs-lookup"><span data-stu-id="d7ade-137">Click Insert at end of text.</span></span>
7. <span data-ttu-id="d7ade-138">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="d7ade-138">Click Save.</span></span>
8. <span data-ttu-id="d7ade-139">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="d7ade-139">Close the page.</span></span>

## <a name="set-up-the-document-routing"></a><span data-ttu-id="d7ade-140">Asiakirjan reitityksen määrittäminen</span><span class="sxs-lookup"><span data-stu-id="d7ade-140">Set up the document routing</span></span>
1. <span data-ttu-id="d7ade-141">Valitse Varastonhallinta > Asetukset > Asiakirjan reititys > Asiakirjan reititys.</span><span class="sxs-lookup"><span data-stu-id="d7ade-141">Go to Warehouse management > Setup > Document routing > Document routing.</span></span>
2. <span data-ttu-id="d7ade-142">Valitse Työtilauksen tyyppi -kentässä vaihtoehto.</span><span class="sxs-lookup"><span data-stu-id="d7ade-142">In the Work order type field, select an option.</span></span>
3. <span data-ttu-id="d7ade-143">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="d7ade-143">Click New.</span></span>
4. <span data-ttu-id="d7ade-144">Kirjoita arvo Varasto-kenttään.</span><span class="sxs-lookup"><span data-stu-id="d7ade-144">In the Warehouse field, type a value.</span></span>
5. <span data-ttu-id="d7ade-145">Kirjoita arvo Nimi-kenttään.</span><span class="sxs-lookup"><span data-stu-id="d7ade-145">In the Name field, type a value.</span></span>
6. <span data-ttu-id="d7ade-146">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="d7ade-146">Click New.</span></span>
7. <span data-ttu-id="d7ade-147">Syötä tai valitse arvo Asettelun tunnus -kenttään.</span><span class="sxs-lookup"><span data-stu-id="d7ade-147">In the Layout ID field, enter or select a value.</span></span>
8. <span data-ttu-id="d7ade-148">Valitse Nimi-kentästä tulostin, jota haluat käyttää.</span><span class="sxs-lookup"><span data-stu-id="d7ade-148">In the Name field, enter the printer name that you want to use..</span></span>
9. <span data-ttu-id="d7ade-149">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="d7ade-149">Click Save.</span></span>
10. <span data-ttu-id="d7ade-150">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="d7ade-150">Close the page.</span></span>

## <a name="create-mobile-device-menu"></a><span data-ttu-id="d7ade-151">Mobiililaitteen valikon luominen</span><span class="sxs-lookup"><span data-stu-id="d7ade-151">Create mobile device menu</span></span>
1. <span data-ttu-id="d7ade-152">Valitse Varastonhallinta > Asetukset > Mobiililaite > Mobiililaitteen valikkovaihtoehdot.</span><span class="sxs-lookup"><span data-stu-id="d7ade-152">Go to Warehouse management > Setup > Mobile device > Mobile device menu items.</span></span>
2. <span data-ttu-id="d7ade-153">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="d7ade-153">Click New.</span></span>
3. <span data-ttu-id="d7ade-154">Kirjoita arvo Valikkovaihtoehdon nimi -kenttään.</span><span class="sxs-lookup"><span data-stu-id="d7ade-154">In the Menu item name field, type a value.</span></span>
4. <span data-ttu-id="d7ade-155">Kirjoita Otsikko-kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="d7ade-155">In the Title field, type a value.</span></span>
5. <span data-ttu-id="d7ade-156">Valitse Tapa-kentässä vaihtoehto.</span><span class="sxs-lookup"><span data-stu-id="d7ade-156">In the Mode field, select an option.</span></span>
6. <span data-ttu-id="d7ade-157">Valitse Käytä nykyistä työtä -kentässä Kyllä.</span><span class="sxs-lookup"><span data-stu-id="d7ade-157">Select Yes in the Use existing work field.</span></span>
7. <span data-ttu-id="d7ade-158">Valitse Muodosta rekisterikilpi -kentässä Kyllä.</span><span class="sxs-lookup"><span data-stu-id="d7ade-158">Select Yes in the Generate license plate field.</span></span>
8. <span data-ttu-id="d7ade-159">Laajenna Työluokat-osa.</span><span class="sxs-lookup"><span data-stu-id="d7ade-159">Expand the Work classes section.</span></span>
9. <span data-ttu-id="d7ade-160">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="d7ade-160">Click New.</span></span>
10. <span data-ttu-id="d7ade-161">Kirjoita Työluokan tunnus -kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="d7ade-161">In the Work class ID field, type a value.</span></span>
11. <span data-ttu-id="d7ade-162">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="d7ade-162">Click Save.</span></span>
12. <span data-ttu-id="d7ade-163">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="d7ade-163">Close the page.</span></span>
13. <span data-ttu-id="d7ade-164">Valitse Varastonhallinta > Asetukset > Mobiililaite > Mobiililaitteen valikko.</span><span class="sxs-lookup"><span data-stu-id="d7ade-164">Go to Warehouse management > Setup > Mobile device > Mobile device menu.</span></span>
14. <span data-ttu-id="d7ade-165">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="d7ade-165">In the list, find and select the desired record.</span></span>
15. <span data-ttu-id="d7ade-166">Valitse puussa solmu In the tree, select the menu item that you created before.</span><span class="sxs-lookup"><span data-stu-id="d7ade-166">In the tree, select 'In the tree, select the menu item that you created before.'.</span></span>
16. <span data-ttu-id="d7ade-167">Valitse Muokkaa.</span><span class="sxs-lookup"><span data-stu-id="d7ade-167">Click Edit.</span></span>
17. <span data-ttu-id="d7ade-168">Lisää valikkovaihtoehto valikkoon nuolen avulla.</span><span class="sxs-lookup"><span data-stu-id="d7ade-168">Click on the arrow to add the menu item to the menu.</span></span>
18. <span data-ttu-id="d7ade-169">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="d7ade-169">Click Save.</span></span>
19. <span data-ttu-id="d7ade-170">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="d7ade-170">Close the page.</span></span>

## <a name="update-a-work-template"></a><span data-ttu-id="d7ade-171">Työmallin päivittäminen</span><span class="sxs-lookup"><span data-stu-id="d7ade-171">Update a work template</span></span>
1. <span data-ttu-id="d7ade-172">Valitse Varastonhallinta > Asetukset > Työ > Työmallit.</span><span class="sxs-lookup"><span data-stu-id="d7ade-172">Go to Warehouse management > Setup > Work > Work templates.</span></span>
2. <span data-ttu-id="d7ade-173">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="d7ade-173">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="d7ade-174">Valitse Muokkaa.</span><span class="sxs-lookup"><span data-stu-id="d7ade-174">Click Edit.</span></span>
4. <span data-ttu-id="d7ade-175">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="d7ade-175">Click New.</span></span>
5. <span data-ttu-id="d7ade-176">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="d7ade-176">In the list, mark the selected row.</span></span>
6. <span data-ttu-id="d7ade-177">Valitse Työtyyppi-kentässä Tulosta.</span><span class="sxs-lookup"><span data-stu-id="d7ade-177">In the Work type field, select 'Print'.</span></span>
7. <span data-ttu-id="d7ade-178">Syötä tai valitse arvo Työluokan tunnus -kenttään.</span><span class="sxs-lookup"><span data-stu-id="d7ade-178">In the Work class ID field, enter or select a value.</span></span>
8. <span data-ttu-id="d7ade-179">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="d7ade-179">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="d7ade-180">Valitse Siirrä ylöspäin.</span><span class="sxs-lookup"><span data-stu-id="d7ade-180">Click Move up.</span></span>
10. <span data-ttu-id="d7ade-181">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="d7ade-181">Click Save.</span></span>
11. <span data-ttu-id="d7ade-182">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="d7ade-182">Close the page.</span></span>

