---
title: Rekisterikilven etiketin tulostuksen ottaminen käyttöön
description: Tässä aiheessa näytetään, miten sarjatoimitusyksikkökoodin (SSCC) etiketti voidaan tulostaa automaattisesti varastosta viimeksi kerätyn nimikkeen jälkeen myynnin keräystyöprosessissa.
author: perlynne
manager: tfehr
ms.date: 07/19/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysCorpNetPrinterList, WHSParameters, NumberSequenceTableListPage, NumberSequenceDetails, WHSDocumentRoutingLayout, WHSDocumentRouting, WHSRFMenuItem, WHSRFMenu, WHSWorkTemplateTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 43dc913e84fa53179855d7ab8dbbf4d179e2cc63
ms.sourcegitcommit: 8a2127c5af6cdbda30ccc1f9bef9bd4ab61e9e50
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/18/2020
ms.locfileid: "3383041"
---
# <a name="enable-license-plate-label-printing"></a><span data-ttu-id="da14e-103">Rekisterikilven etiketin tulostuksen ottaminen käyttöön</span><span class="sxs-lookup"><span data-stu-id="da14e-103">Enable license plate label printing</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="da14e-104">Tässä aiheessa näytetään, miten sarjatoimitusyksikkökoodin (SSCC) etiketti voidaan tulostaa automaattisesti varastosta viimeksi kerätyn nimikkeen jälkeen myynnin keräystyöprosessissa.</span><span class="sxs-lookup"><span data-stu-id="da14e-104">This topic shows how to enable the automatic printing of a Serial shipping container code (SSCC) label after the last item is picked from inventory in a sales picking work process.</span></span> <span data-ttu-id="da14e-105">Voit suorittaa tämän menettelyn esittely-yrityksessä USMF.</span><span class="sxs-lookup"><span data-stu-id="da14e-105">You can run this procedure in demo data company USMF.</span></span> <span data-ttu-id="da14e-106">Jos suoritit menettelyn omien tietojen avulla, rekisterikilville on määritettävä numerosarja.</span><span class="sxs-lookup"><span data-stu-id="da14e-106">If you're run it using your own data, you need to have a number sequence set up for license plates.</span></span> <span data-ttu-id="da14e-107">Määritä etikettitulostin, ennen kuin aloitat tämän tehtävän.</span><span class="sxs-lookup"><span data-stu-id="da14e-107">You need to set up a label printer before you begin this task.</span></span> <span data-ttu-id="da14e-108">Valitse Organisaation hallinta > Asetukset > Verkkotulostimet.</span><span class="sxs-lookup"><span data-stu-id="da14e-108">Go to Organization administration > Setup > Network printers.</span></span> <span data-ttu-id="da14e-109">Valitse toimintoruudussa Asetukset ja valitse sitten Lataa asiakirjan reititysagentin asennusohjelma -painike.</span><span class="sxs-lookup"><span data-stu-id="da14e-109">On the Action Pane, click Options, and then click the Download document routing agent installer button.</span></span> <span data-ttu-id="da14e-110">Suorita asennusohjelma ja varmista, että toimiva verkkotulostin on määritetty aktiiviseksi, ennen kuin jatkat.</span><span class="sxs-lookup"><span data-stu-id="da14e-110">Run the installer and make sure that you have a working network printer set to Active before you continue with the procedure.</span></span>


## <a name="set-up-the-gs1-company-prefix"></a><span data-ttu-id="da14e-111">Yrityksen GS1-etuliitteen määrittäminen</span><span class="sxs-lookup"><span data-stu-id="da14e-111">Set up the GS1 company prefix</span></span>
1. <span data-ttu-id="da14e-112">Siirry kohtaan **Siirtymisruutu > Moduulit > Varastonhallinta > Asetukset > Varastonhallinnan parametrit**.</span><span class="sxs-lookup"><span data-stu-id="da14e-112">Go to **Navigation pane > Modules > Warehouse management > Setup > Warehouse management parameters**.</span></span>
2. <span data-ttu-id="da14e-113">Syötä **yrityksen GS1-etuliite** -kenttään GS1-yritysnumeron 7 numeroa.</span><span class="sxs-lookup"><span data-stu-id="da14e-113">In the **GS1 company prefix** field, enter the 7 numbers for your GS1 company number.</span></span>
3. <span data-ttu-id="da14e-114">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="da14e-114">Select **Save**.</span></span>
4. <span data-ttu-id="da14e-115">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="da14e-115">Close the page.</span></span>

## <a name="setup-the-sscc-license-plate-number-sequence"></a><span data-ttu-id="da14e-116">SSCC-rekisterinumeron järjestyksen määrittäminen</span><span class="sxs-lookup"><span data-stu-id="da14e-116">Setup the SSCC license plate number sequence</span></span>
1. <span data-ttu-id="da14e-117">Siirry kohtaan **Siirtymisruutu > Moduulit > Organisaation hallinta > Numerosarjat > Numerosarjat**.</span><span class="sxs-lookup"><span data-stu-id="da14e-117">Go to **Navigation pane > Modules > Organization administration > Number sequences > Number sequences**.</span></span>
2. <span data-ttu-id="da14e-118">Valitse **Alue**-kentässä vaihtoehto.</span><span class="sxs-lookup"><span data-stu-id="da14e-118">In the **Area** field, select an option.</span></span>
3. <span data-ttu-id="da14e-119">Valitse **Viite**-kentässä vaihtoehto.</span><span class="sxs-lookup"><span data-stu-id="da14e-119">In the **Reference** field, select an option.</span></span>
4. <span data-ttu-id="da14e-120">Kirjoita arvo **Yritys**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="da14e-120">In the **Company** field, type a value.</span></span>
5. <span data-ttu-id="da14e-121">Laajenna **Segmentit**-osa.</span><span class="sxs-lookup"><span data-stu-id="da14e-121">Expand the **Segments** section.</span></span>
6. <span data-ttu-id="da14e-122">Valitse **Muokkaa**.</span><span class="sxs-lookup"><span data-stu-id="da14e-122">Select **Edit**.</span></span>
7. <span data-ttu-id="da14e-123">Valitse **Segmentit**-taulukon ensimmäinen rivi.</span><span class="sxs-lookup"><span data-stu-id="da14e-123">In the **Segments** table, select the first row</span></span>
8. <span data-ttu-id="da14e-124">Valitse **Poista**.</span><span class="sxs-lookup"><span data-stu-id="da14e-124">Select **Remove**.</span></span>
9. <span data-ttu-id="da14e-125">Valitse **Poista**.</span><span class="sxs-lookup"><span data-stu-id="da14e-125">Select **Remove**.</span></span>
10. <span data-ttu-id="da14e-126">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="da14e-126">Select **Save**.</span></span>
11. <span data-ttu-id="da14e-127">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="da14e-127">Close the page.</span></span>

## <a name="create-the-document-route-layout"></a><span data-ttu-id="da14e-128">Asiakirjan reittiasettelun luominen</span><span class="sxs-lookup"><span data-stu-id="da14e-128">Create the document route layout</span></span>
1. <span data-ttu-id="da14e-129">Valitse **Siirtymisruutu > Moduulit > Varastonhallinta >> Asetukset > Asiakirjan reititys > Asiakirjan reititysasettelut**.</span><span class="sxs-lookup"><span data-stu-id="da14e-129">Go to **Navigation pane > Modules > Warehouse management > Setup > Document routing > Document routing layouts**.</span></span> <span data-ttu-id="da14e-130">Ota SSCC-asettelu käyttöön.</span><span class="sxs-lookup"><span data-stu-id="da14e-130">Enable the SSCC layout.</span></span>  
2. <span data-ttu-id="da14e-131">Valitse **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="da14e-131">Select **New**.</span></span>
3. <span data-ttu-id="da14e-132">Kirjoita **Asettelun tunnus** -kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="da14e-132">In the **Layout ID** field, type a value.</span></span>
4. <span data-ttu-id="da14e-133">Kirjoita **Kuvaus**-kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="da14e-133">In the **Description** field, type a value.</span></span>
5. <span data-ttu-id="da14e-134">Valitse **Lisää tekstin loppuun**.</span><span class="sxs-lookup"><span data-stu-id="da14e-134">Select **Insert at end of text**.</span></span>
6. <span data-ttu-id="da14e-135">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="da14e-135">Select **Save**.</span></span>
7. <span data-ttu-id="da14e-136">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="da14e-136">Close the page.</span></span>

## <a name="set-up-the-document-routing"></a><span data-ttu-id="da14e-137">Asiakirjan reitityksen määrittäminen</span><span class="sxs-lookup"><span data-stu-id="da14e-137">Set up the document routing</span></span>
1. <span data-ttu-id="da14e-138">Valitse **Siirtymisruutu > Moduulit > Varastonhallinta >> Asetukset > Asiakirjan reititys > Asiakirjan reititys**.</span><span class="sxs-lookup"><span data-stu-id="da14e-138">Go to **Navigation pane > Modules > Warehouse management > Setup > Document routing > Document routing**.</span></span>
2. <span data-ttu-id="da14e-139">Valitse **Työtilauksen tyyppi** -kentässä vaihtoehto.</span><span class="sxs-lookup"><span data-stu-id="da14e-139">In the **Work order type** field, select an option.</span></span>
3. <span data-ttu-id="da14e-140">Valitse **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="da14e-140">Select **New**.</span></span>
4. <span data-ttu-id="da14e-141">Kirjoita arvo **Varasto**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="da14e-141">In the **Warehouse** field, type a value.</span></span>
5. <span data-ttu-id="da14e-142">Kirjoita arvo **Nimi**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="da14e-142">In the **Name** field, type a value.</span></span>
6. <span data-ttu-id="da14e-143">Valitse **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="da14e-143">Select **New**.</span></span>
7. <span data-ttu-id="da14e-144">Syötä tai valitse arvo **Asettelun tunnus** -kenttään.</span><span class="sxs-lookup"><span data-stu-id="da14e-144">In the **Layout ID** field, enter or select a value.</span></span>
8. <span data-ttu-id="da14e-145">Valitse **Nimi**-kentästä tulostin, jota haluat käyttää.</span><span class="sxs-lookup"><span data-stu-id="da14e-145">In the **Name** field, enter the printer name that you want to use.</span></span>
9. <span data-ttu-id="da14e-146">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="da14e-146">Select **Save**.</span></span>
10. <span data-ttu-id="da14e-147">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="da14e-147">Close the page.</span></span>

## <a name="create-mobile-device-menu"></a><span data-ttu-id="da14e-148">Mobiililaitteen valikon luominen</span><span class="sxs-lookup"><span data-stu-id="da14e-148">Create mobile device menu</span></span>
1. <span data-ttu-id="da14e-149">Siirry siirtymisruudussa kohtaan **Moduulit > Varastonhallinta > Asetukset > mobiililaite > Mobiililaitteen valikkovaihtoehdot**.</span><span class="sxs-lookup"><span data-stu-id="da14e-149">Go to **Navigation pane > Modules > Warehouse management > Setup > Mobile device > Mobile device menu items**.</span></span>
2. <span data-ttu-id="da14e-150">Valitse **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="da14e-150">Select **New**.</span></span>
3. <span data-ttu-id="da14e-151">Kirjoita arvo **Valikkovaihtoehdon nimi** -kenttään.</span><span class="sxs-lookup"><span data-stu-id="da14e-151">In the **Menu item name** field, type a value.</span></span>
4. <span data-ttu-id="da14e-152">Kirjoita **Otsikko**-kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="da14e-152">In the **Title** field, type a value.</span></span>
5. <span data-ttu-id="da14e-153">Valitse **Tapa**-kentässä vaihtoehto.</span><span class="sxs-lookup"><span data-stu-id="da14e-153">In the **Mode** field, select an option.</span></span>
6. <span data-ttu-id="da14e-154">Valitse **Käytä nykyistä työtä** -kentässä **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="da14e-154">Select **Yes** in the **Use existing work** field.</span></span>
7. <span data-ttu-id="da14e-155">Valitse **Muodosta rekisterikilpi** -kentässä **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="da14e-155">Select **Yes** in the **Generate license plate** field.</span></span>
8. <span data-ttu-id="da14e-156">Laajenna **Työluokat**-osa.</span><span class="sxs-lookup"><span data-stu-id="da14e-156">Expand the **Work classes** section.</span></span>
9. <span data-ttu-id="da14e-157">Valitse **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="da14e-157">Select **New**.</span></span>
10. <span data-ttu-id="da14e-158">Kirjoita **Työluokan tunnus** -kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="da14e-158">In the **Work class ID** field, type a value.</span></span>
11. <span data-ttu-id="da14e-159">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="da14e-159">Select **Save**.</span></span>
12. <span data-ttu-id="da14e-160">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="da14e-160">Close the page.</span></span>
13. <span data-ttu-id="da14e-161">Siirry siirtymisruudussa kohtaan **Moduulit > Varastonhallinta > Asetukset > mobiililaite > Mobiililaitteen valikko**.</span><span class="sxs-lookup"><span data-stu-id="da14e-161">Go to **navigation pane > Modules > Warehouse management > Setup > Mobile device > Mobile device menu**.</span></span>
14. <span data-ttu-id="da14e-162">Valitse puusta aiemmin luotu valikkovaihtoehto.</span><span class="sxs-lookup"><span data-stu-id="da14e-162">In the tree, select the menu item that you created before.</span></span>
15. <span data-ttu-id="da14e-163">Valitse **Muokkaa**.</span><span class="sxs-lookup"><span data-stu-id="da14e-163">Select **Edit**.</span></span>
16. <span data-ttu-id="da14e-164">Lisää valikkovaihtoehto valikkoon nuolen avulla.</span><span class="sxs-lookup"><span data-stu-id="da14e-164">Select the arrow to add the menu item to the menu.</span></span>
17. <span data-ttu-id="da14e-165">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="da14e-165">Select **Save**.</span></span>
18. <span data-ttu-id="da14e-166">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="da14e-166">Close the page.</span></span>

## <a name="update-a-work-template"></a><span data-ttu-id="da14e-167">Työmallin päivittäminen</span><span class="sxs-lookup"><span data-stu-id="da14e-167">Update a work template</span></span>
1. <span data-ttu-id="da14e-168">Siirry kohtaan **Siirtymisruutu > Moduulit > Varastonhallinta > Asetukset > Työ > Työmallit**.</span><span class="sxs-lookup"><span data-stu-id="da14e-168">Go to **Navigation pane > Modules > Warehouse management > Setup > Work > Work templates**.</span></span>
2. <span data-ttu-id="da14e-169">Valitse **Muokkaa**.</span><span class="sxs-lookup"><span data-stu-id="da14e-169">Select **Edit**.</span></span>
3. <span data-ttu-id="da14e-170">Valitse **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="da14e-170">Select **New**.</span></span>
4. <span data-ttu-id="da14e-171">Valitse **Työtyyppi**-kentässä **Tulosta**.</span><span class="sxs-lookup"><span data-stu-id="da14e-171">In the **Work type** field, select **Print**.</span></span>
5. <span data-ttu-id="da14e-172">Syötä tai valitse arvo **Työluokan tunnus** -kenttään.</span><span class="sxs-lookup"><span data-stu-id="da14e-172">In the **Work class ID** field, enter or select a value.</span></span>
6. <span data-ttu-id="da14e-173">Valitse **Siirrä ylös**.</span><span class="sxs-lookup"><span data-stu-id="da14e-173">Select **Move up**.</span></span>
7. <span data-ttu-id="da14e-174">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="da14e-174">Select **Save**.</span></span>
8. <span data-ttu-id="da14e-175">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="da14e-175">Close the page.</span></span>

