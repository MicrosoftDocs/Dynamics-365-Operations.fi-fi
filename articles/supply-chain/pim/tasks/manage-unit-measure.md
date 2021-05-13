---
title: Mittayksiköiden hallinta
description: Tässä aiheessa kerrotaan, miten mittayksikkö määritetään, miten yksikkö ja sen kuvaukset käännetään ja miten liittyvien yksiköiden muunnossäännöt määritetään.
author: sorenva
ms.date: 04/09/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: EcoResProductMaintainWorkspace, EcoResProductOpenCasesFormPart, UnitOfMeasure, UnitOfMeasureReportingTranslation, UnitOfMeasureTranslation, UnitOfMeasureConversion, UnitOfMeasureConversionEditOrCreate, UnitOfMeasureLookup, UnitOfMeasureCalculator, UnitOfMeasureWizard, UnitOfMeasureLookupTest
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: sorenand
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d36839cd8e3398225d3421bf0f268068599ca49f
ms.sourcegitcommit: fa99a36c3d30d0c0577fd3f63ed6bf2f71599e40
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/20/2021
ms.locfileid: "5921338"
---
# <a name="manage-units-of-measure"></a><span data-ttu-id="0e117-103">Mittayksiköiden hallinta</span><span class="sxs-lookup"><span data-stu-id="0e117-103">Manage units of measure</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="0e117-104">Tässä aiheessa kerrotaan, miten mittayksikkö määritetään, miten yksikkö ja sen kuvaukset käännetään ja miten liittyvien yksiköiden muunnossäännöt määritetään.</span><span class="sxs-lookup"><span data-stu-id="0e117-104">This topic describes how to define a unit of measure, provide translations for the unit and its description, and define conversion rules for related units.</span></span>

## <a name="open-the-units-page"></a><span data-ttu-id="0e117-105">Avaa Yksiköt-sivu</span><span class="sxs-lookup"><span data-stu-id="0e117-105">Open the Units page</span></span>

<span data-ttu-id="0e117-106">Jos haluat luoda ja käyttää järjestelmässä käytettävissä olevia mittayksiköitä, siirry kohtaan **Organisaation hallinto \> Asetukset \> Yksiköt \> Yksiköt**.</span><span class="sxs-lookup"><span data-stu-id="0e117-106">To create and work with the units of measure that are available in your system, go to **Organization administration \> Setup \> Units \> Units**.</span></span>

<span data-ttu-id="0e117-107">Tämän ohjeaiheen muut osat kuvaavat, mitä voit tehdä **Yksiköt**-sivulla.</span><span class="sxs-lookup"><span data-stu-id="0e117-107">The remaining sections of this topic describe what you can do on the **Units** page.</span></span>

## <a name="create-standard-units-and-conversions"></a><span data-ttu-id="0e117-108">Vakioyksiköiden ja muunnosten luominen</span><span class="sxs-lookup"><span data-stu-id="0e117-108">Create standard units and conversions</span></span>

<span data-ttu-id="0e117-109">Jos järjestelmä ei sisällä vielä eniten käytettyjä mittayksiköitä metrijärjestelmässä ja/tai USCS-järjestelmässä, ohjatun yksikkömäärityksen avulla voit aloittaa perusyksikkömääritykset ja -muunnokset nopeasti.</span><span class="sxs-lookup"><span data-stu-id="0e117-109">If your system doesn't already include the most commonly used units of measure for the metric system and/or the US customary system (USCS), the unit setup wizard can help you quickly get started with basic unit definitions and conversions.</span></span> <span data-ttu-id="0e117-110">Voit suorittaa ohjatun toiminnon loppuun valitsemalla toimintoruudusta **Ohjattu yksikköjen luonti** noudattamalla sitten näyttöön tulevia ohjeita.</span><span class="sxs-lookup"><span data-stu-id="0e117-110">To complete the wizard, select **Unit creation wizard** on the Action Pane, and then follow the on-screen instructions.</span></span>

## <a name="create-or-edit-a-unit-of-measure"></a><span data-ttu-id="0e117-111">Mittayksikön luominen tai muokkaaminen</span><span class="sxs-lookup"><span data-stu-id="0e117-111">Create or edit a unit of measure</span></span>

<span data-ttu-id="0e117-112">Voit luoda mittayksikön tai muokata sitä noudattamalla seuraavia vaiheita.</span><span class="sxs-lookup"><span data-stu-id="0e117-112">To create or edit a unit of measure, follow these steps.</span></span>

1. <span data-ttu-id="0e117-113">Noudata seuraavia ohjeita:</span><span class="sxs-lookup"><span data-stu-id="0e117-113">Follow one of these steps:</span></span>

    - <span data-ttu-id="0e117-114">Jos haluat muokata aiemmin luotua yksikköä, valitse se luetteloruudusta.</span><span class="sxs-lookup"><span data-stu-id="0e117-114">To edit an existing unit, select it in the list pane.</span></span>
    - <span data-ttu-id="0e117-115">Valitse toimintoruudussa **Uusi** luodaksesi uuden yksikön.</span><span class="sxs-lookup"><span data-stu-id="0e117-115">To create a new unit, select **New** on the Action Pane.</span></span>

1. <span data-ttu-id="0e117-116">Määritä tietueen ylätunnisteessa seuraavat kentät:</span><span class="sxs-lookup"><span data-stu-id="0e117-116">On the header of the record, set the following fields:</span></span>

    - <span data-ttu-id="0e117-117">**Yksikkö** – Kirjoita tunnus tai symboli, jota käytetään yksikön viittaamiseen järjestelmän kielellä.</span><span class="sxs-lookup"><span data-stu-id="0e117-117">**Unit** – Enter the ID or symbol to use to refer to the unit in the system language.</span></span> <span data-ttu-id="0e117-118">Tämä tunnus tai symboli on yleensä yksikköä varten oleva yleinen lyhenne, esimerkiksi *kpl* (kappale) tai *cm* (senttimetri).</span><span class="sxs-lookup"><span data-stu-id="0e117-118">This ID or symbol is usually a common abbreviation for the unit, such as *ea* for each or *cm* for centimeter.</span></span>
    - <span data-ttu-id="0e117-119">**Kuvaus** – Syötä yksikölle kuvaava nimi järjestelmän kielellä.</span><span class="sxs-lookup"><span data-stu-id="0e117-119">**Description** – Enter a descriptive name for the unit in the system language.</span></span> <span data-ttu-id="0e117-120">Tämä nimi on yleensä yksikön koko nimi, esimerkiksi *Kappale* tai *Senttimetri*.</span><span class="sxs-lookup"><span data-stu-id="0e117-120">This name is usually the full name of the unit, such as *Each* or *Centimeter*.</span></span>

1. <span data-ttu-id="0e117-121">Valitse **Yleiset**-pikavälilehdellä seuraavat lisäkentät:</span><span class="sxs-lookup"><span data-stu-id="0e117-121">On the **General** FastTab, set the following fields:</span></span><!-- KFM: confirm this:    - **Fixed unit assignment** and **Fixed unit** – These fields have an effect only if you're using the Microsoft Retail Essentials product. If the current unit can be mapped to one of the fixed units that are used by Retail Essentials, set the **Fixed unit assignment** option to *Yes*. Then select the fixed unit in the **Fixed unit** field. -->

    - <span data-ttu-id="0e117-122">**Yksikköluokka** – Valitse ominaisuus, jonka mittayksikkö mittaa (esimerkiksi pituus, alue, massa tai määrä).</span><span class="sxs-lookup"><span data-stu-id="0e117-122">**Unit class** – Select the property that the unit measures (such as length, area, mass, or quantity).</span></span>
    - <span data-ttu-id="0e117-123">**Yksikköjärjestelmä** – Valitse mittausjärjestelmä, johon yksikkö kuuluu (*Metrijärjestelmän yksiköt* tai *Yhdysvaltojen yksikköjärjestelmän yksiköt*).</span><span class="sxs-lookup"><span data-stu-id="0e117-123">**System of units** – Select the measurement system that the unit belongs to (*Metric units* or *United States customary units*).</span></span>
    - <span data-ttu-id="0e117-124">**Perusyksikkö** – Määritä tämän asetuksen arvoksi *Kyllä*, jos haluat käyttää nykyistä yksikköä yksikköluokan perusyksikkönä.</span><span class="sxs-lookup"><span data-stu-id="0e117-124">**Base unit** – Set this option to *Yes* to use the current unit as the base unit for its unit class.</span></span> <span data-ttu-id="0e117-125">Tällöin sinun on määritettävä vain perusyksikön ja kunkin yksikköluokan lisäyksikön välinen muuntokerroin.</span><span class="sxs-lookup"><span data-stu-id="0e117-125">In this case, you only have to specify the conversion factor between the base unit and each additional unit in the unit class.</span></span> <span data-ttu-id="0e117-126">Järjestelmä voi tämän jälkeen muuntaa kaikkien yksikön luokan yksiköiden välillä.</span><span class="sxs-lookup"><span data-stu-id="0e117-126">The system can then convert between all units in that unit class.</span></span> <span data-ttu-id="0e117-127">Siksi on helpompi määrittää muunnokset.</span><span class="sxs-lookup"><span data-stu-id="0e117-127">Therefore, it's easier to set up conversions.</span></span>

        <span data-ttu-id="0e117-128">Jos esimerkiksi gallona on *Tilavuus*-yksikköluokan perusyksikkö, muuntokertoimet on määritettävä vain neljännesgallonasta gallonaan ja pintista gallonaan.</span><span class="sxs-lookup"><span data-stu-id="0e117-128">For example, if gallon is the base unit for the *Volume* unit class, you only have to set up conversion factors from quart to gallon and from pint to gallon.</span></span> <span data-ttu-id="0e117-129">Tämän jälkeen järjestelmä voi myös muuntaa sen neljännesgallonasta pintiin.</span><span class="sxs-lookup"><span data-stu-id="0e117-129">The system can then also convert from quart to pint.</span></span>

        <span data-ttu-id="0e117-130">Yhtä yksikköluokkaa kohden voi olla vain yksi perusyksikkö.</span><span class="sxs-lookup"><span data-stu-id="0e117-130">You can have only one base unit per unit class.</span></span>

    - <span data-ttu-id="0e117-131">**Järjestelmäyksikkö** – Määritä tämän asetuksen arvoksi *Kyllä*, jos haluat käyttää nykyistä yksikköä kaikkien yksikköluokan määrittämättömien mittojen oletettuna yksikkönä.</span><span class="sxs-lookup"><span data-stu-id="0e117-131">**System unit** – Set this option to *Yes* to use the current unit as the assumed unit for all unspecified measurements in its unit class.</span></span> <span data-ttu-id="0e117-132">Esimerkiksi jos määrän syöttöön käytettävä kenttä ei salli yksikön määrittämistä (tai jos käyttäjä ei valitse yksikköä), järjestelmä käyttää yksikköä, joka on määritetty *Määrä*-yksikköluokan järjestelmäyksiköksi.</span><span class="sxs-lookup"><span data-stu-id="0e117-132">For example, if a field that is used to enter a quantity doesn't allow a unit to be specified (of if the user doesn't select a unit), the system uses the unit that is set as the system unit for the *Quantity* unit class.</span></span> <span data-ttu-id="0e117-133">Yhtä yksikköluokkaa kohden voi olla vain yksi järjestelmäyksikkö.</span><span class="sxs-lookup"><span data-stu-id="0e117-133">You can have only one system unit per unit class.</span></span>
    - <span data-ttu-id="0e117-134">**Desimaalitarkkuus** – Määritä desimaalien määrä, joksi nykyiselle yksikölle määritetyt tai siihen muunnetut arvot pyöristetään.</span><span class="sxs-lookup"><span data-stu-id="0e117-134">**Decimal precision** – Specify the number of decimal places that values that are specified for the current unit or converted to it should be rounded to.</span></span>

1. <span data-ttu-id="0e117-135">Valitse toimintoruudussa **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="0e117-135">On the Action Pane, select **Save**.</span></span>

## <a name="define-unit-translations"></a><span data-ttu-id="0e117-136">Yksikkökäännösten määrittäminen</span><span class="sxs-lookup"><span data-stu-id="0e117-136">Define unit translations</span></span>

<span data-ttu-id="0e117-137">Kun haluat määrittää tunnuksen tai symbolin käännökset ja mittayksikön kuvauksen, noudata seuraavia ohjeita.</span><span class="sxs-lookup"><span data-stu-id="0e117-137">To define translations for the ID or symbol and the description for a unit of measure, follow these steps.</span></span>

1. <span data-ttu-id="0e117-138">Luo tai valitse yksikkö, jolle käännökset luodaan.</span><span class="sxs-lookup"><span data-stu-id="0e117-138">Create or select the unit to create translations for.</span></span>
1. <span data-ttu-id="0e117-139">Valitse toimintoruudussa **Yksikön tekstit**.</span><span class="sxs-lookup"><span data-stu-id="0e117-139">On the Action Pane, select **Unit texts**.</span></span>

    <span data-ttu-id="0e117-140">**Yksikkötekstit**-sivu avautuu.</span><span class="sxs-lookup"><span data-stu-id="0e117-140">The **Unit texts** page appears.</span></span> <span data-ttu-id="0e117-141">Tällä sivulla voit määrittää valitun yksikön tunnuksen tai symbolin käännökset.</span><span class="sxs-lookup"><span data-stu-id="0e117-141">You use this page to define translations for the ID or symbol for the selected unit.</span></span> <span data-ttu-id="0e117-142">Käännöksiä voidaan tämän jälkeen käyttää ulkoisille tiedostoille asiakas- tai toimittajakohtaisissa kielissä.</span><span class="sxs-lookup"><span data-stu-id="0e117-142">Those translations can then be used on external documents in customer-specific or vendor-specific languages.</span></span>

1. <span data-ttu-id="0e117-143">Valitse toimintoruudussa **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="0e117-143">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="0e117-144">Valitse **Kieli**-kentässä kieli, jolle yksikön tunnus tai symboli käännetään.</span><span class="sxs-lookup"><span data-stu-id="0e117-144">In the **Language** field, select the language to translate the unit ID or symbol to.</span></span>
1. <span data-ttu-id="0e117-145">Kirjoita **Teksti**-kenttään yksikön tunnuksen tai symbolin käännös valitulla kielellä.</span><span class="sxs-lookup"><span data-stu-id="0e117-145">In the **Text** field, enter the translation of the unit ID or symbol in the selected language.</span></span>
1. <span data-ttu-id="0e117-146">Valitse toimintoruudussa **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="0e117-146">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="0e117-147">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="0e117-147">Close the page.</span></span>
1. <span data-ttu-id="0e117-148">Valitse **toimintoruudussa** **Käännetyt yksiköiden kuvaukset**.</span><span class="sxs-lookup"><span data-stu-id="0e117-148">On the **Action Pane**, select **Translated unit descriptions**.</span></span>

    <span data-ttu-id="0e117-149">**Käännetyt yksiköiden kuvaukset** -sivu tulee näkyviin.</span><span class="sxs-lookup"><span data-stu-id="0e117-149">The **Translated unit descriptions** page appears.</span></span> <span data-ttu-id="0e117-150">Tämän sivun avulla voit määrittää valitun yksikön kielikohtaiset kuvaukset.</span><span class="sxs-lookup"><span data-stu-id="0e117-150">You use this page to define language-specific descriptions for the selected unit.</span></span>

1. <span data-ttu-id="0e117-151">Valitse toimintoruudussa **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="0e117-151">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="0e117-152">Valitse **Kieli**-kentässä kieli, jolle yksikön kuvaus käännetään.</span><span class="sxs-lookup"><span data-stu-id="0e117-152">In the **Language** field, select the language to translate the unit description to.</span></span>
1. <span data-ttu-id="0e117-153">Kirjoita **Kuvaus**-kenttään yksikön kuvauksen käännös valitulla kielellä.</span><span class="sxs-lookup"><span data-stu-id="0e117-153">In the **Description** field, enter the translation of the unit description in the selected language.</span></span>
1. <span data-ttu-id="0e117-154">Valitse toimintoruudussa **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="0e117-154">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="0e117-155">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="0e117-155">Close the page.</span></span>

## <a name="define-unit-conversion-rules"></a><span data-ttu-id="0e117-156">Yksikön muunnössääntöjen määrittäminen</span><span class="sxs-lookup"><span data-stu-id="0e117-156">Define unit conversion rules</span></span>

<span data-ttu-id="0e117-157">Noudata seuraavia ohjeita, kun haluat määrittää mittayksiköiden välisten muunnosten säännöt.</span><span class="sxs-lookup"><span data-stu-id="0e117-157">To define rules for conversions between units of measure, follow these steps.</span></span>

1. <span data-ttu-id="0e117-158">Luo tai valitse yksikkö, jolle muunnosten säännöt määritetään.</span><span class="sxs-lookup"><span data-stu-id="0e117-158">Create or select the unit to define conversion rules for.</span></span>
1. <span data-ttu-id="0e117-159">Valitse toimintoruudussa **Yksikkömuunnokset**.</span><span class="sxs-lookup"><span data-stu-id="0e117-159">On the Action Pane, select **Unit conversions**.</span></span>

    <span data-ttu-id="0e117-160">**Yksikkömuunnokset**-sivu avautuu.</span><span class="sxs-lookup"><span data-stu-id="0e117-160">The **Unit conversions** page appears.</span></span> <span data-ttu-id="0e117-161">Tällä sivulla voit määrittää valitun yksikön muuntamisen säännöt muihin yksiköihin ja muista yksiköistä yksikköluokassa.</span><span class="sxs-lookup"><span data-stu-id="0e117-161">You use this page to define rules for converting the selected unit to and from other units in the unit class.</span></span>

1. <span data-ttu-id="0e117-162">Valitse jokin seuraavista välilehdistä määritettävän muuntotyypin mukaan:</span><span class="sxs-lookup"><span data-stu-id="0e117-162">Select one of the following tabs, depending on the type of conversion that you want to set up:</span></span>

    - <span data-ttu-id="0e117-163">**Vakiomuunnokset** – Määritä kaikkien tuotteiden vakiomuuntosäännöt.</span><span class="sxs-lookup"><span data-stu-id="0e117-163">**Standard conversions** – Set up standard conversion rules for all products.</span></span>
    - <span data-ttu-id="0e117-164">**Luokansisäiset muunnokset** – Määritä tuotekohtaiset muuntosäännöt saman yksikköluokan yksiköille.</span><span class="sxs-lookup"><span data-stu-id="0e117-164">**Intra-class conversions** – Set up product-specific conversion rules for units in the same unit class.</span></span>
    - <span data-ttu-id="0e117-165">**Luokkienväliset muunnokset** – Määritä tuotekohtaiset muuntosäännöt eri yksikköluokkien yksiköille.</span><span class="sxs-lookup"><span data-stu-id="0e117-165">**Inter-class conversions** – Set up product-specific conversion rules for units across unit classes.</span></span>

1. <span data-ttu-id="0e117-166">Noudata seuraavia ohjeita:</span><span class="sxs-lookup"><span data-stu-id="0e117-166">Follow one of these steps:</span></span>

    - <span data-ttu-id="0e117-167">Valitse työkalurivillä **Uusi** luodaksesi uuden muunnoksen.</span><span class="sxs-lookup"><span data-stu-id="0e117-167">To create a new conversion, select **New** on the toolbar.</span></span>
    - <span data-ttu-id="0e117-168">Jos haluat muokata aiemmin luotua muunnosta, valitse muunnos ruudukosta ja valitse sitten työkaluriviltä **Muokkaa**.</span><span class="sxs-lookup"><span data-stu-id="0e117-168">To edit an existing conversion, select the conversion in the grid, and then select **Edit** on the toolbar.</span></span>

1. <span data-ttu-id="0e117-169">Näyttöön tulevassa avattavassa valintaikkunassa kuvaillaan seuraavat kentät:</span><span class="sxs-lookup"><span data-stu-id="0e117-169">In the drop-down dialog box that appears, set the following fields:</span></span>

    - <span data-ttu-id="0e117-170">**Tuote** – Valitse tietty tuote, jota muunnos koskee.</span><span class="sxs-lookup"><span data-stu-id="0e117-170">**Product** – Select the specific product that the conversion applies to.</span></span> <span data-ttu-id="0e117-171">Tämä kenttä on käytettävissä vain luokansisäisissä ja luokkienvälisissä muunnoksissa.</span><span class="sxs-lookup"><span data-stu-id="0e117-171">This field is available only for intra-class and inter-class conversions.</span></span>
    - <span data-ttu-id="0e117-172">**Kaavan asettelu** – Jätä tämän kentän asetukseksi *Yksinkertainen*, jos haluat määrittää yksinkertaisen muunnoksen, jolla on yksi kerroin.</span><span class="sxs-lookup"><span data-stu-id="0e117-172">**Formula layout** – Leave this field set to *Simple* to specify a simple conversion that has a single factor.</span></span> <span data-ttu-id="0e117-173">Määritä sen arvoksi *Lisäasetukset*, jos haluat määrittää monimutkaisemman yhtälön.</span><span class="sxs-lookup"><span data-stu-id="0e117-173">Set it to *Advanced* to set up a more complex equation.</span></span> <span data-ttu-id="0e117-174">Edistyneiden yhtälöiden muoto vaihtelee yksikköluokan mukaan.</span><span class="sxs-lookup"><span data-stu-id="0e117-174">The format for advanced equations varies, depending on the unit class.</span></span>
    - <span data-ttu-id="0e117-175">**Yksiköstä** – Tässä kentässä näkyy valittu yksikkö.</span><span class="sxs-lookup"><span data-stu-id="0e117-175">**From unit** – This field shows the selected unit.</span></span> <span data-ttu-id="0e117-176">Yleensä arvoa ei pitäisi muuttaa.</span><span class="sxs-lookup"><span data-stu-id="0e117-176">Usually, you should not change the value.</span></span> <span data-ttu-id="0e117-177">(Jos muutat arvoa, avaa valitun yksikön **Yksikkömuunnokset**-sivu, jos haluat tarkastella uutta muunnosta sen tallentamisen jälkeen.)</span><span class="sxs-lookup"><span data-stu-id="0e117-177">(If you do change the value, you must open the **Unit conversions** page for the selected unit to view your new conversion after you save it.)</span></span>
    - <span data-ttu-id="0e117-178">**Yksikköön** – Valitse yksikkö, johon muunnetaan.</span><span class="sxs-lookup"><span data-stu-id="0e117-178">**To unit** – Select the unit to convert to.</span></span>
    - <span data-ttu-id="0e117-179">**Pyöristys** – Valitse, kuinka murtoluvut pyöristetään valitun yksikön **Desimaalitarkkuus**-arvon perusteella (*Lähimpään*, *Ylös* tai *Alas*).</span><span class="sxs-lookup"><span data-stu-id="0e117-179">**Rounding** – Select how fractions should be rounded, based on the **Decimal precision** value of the selected unit (*To nearest*, *Up*, or *Down*).</span></span>
    - <span data-ttu-id="0e117-180">**Muuntokaava** – Määritä avattavan valintaikkunan yläosassa olevien kenttien avulla kaava muuntamiseen näiden kahden yksikön välillä.</span><span class="sxs-lookup"><span data-stu-id="0e117-180">**Conversion formula** – Use the remaining fields at the top of the drop-down dialog box to specify the formula for converting between the two units.</span></span> <span data-ttu-id="0e117-181">Käytettävissä olevat kentät vaihtelevat valitsemasi yksikköluokan ja kaavan asettelun mukaan.</span><span class="sxs-lookup"><span data-stu-id="0e117-181">The available fields vary, depending on the unit class and formula layout that you've selected.</span></span>

1. <span data-ttu-id="0e117-182">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="0e117-182">Select **OK**.</span></span>
1. <span data-ttu-id="0e117-183">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="0e117-183">Close the page.</span></span>

> [!TIP]
> <span data-ttu-id="0e117-184">Voit myös määrittää yksikkömuunnoksia tuotevarianttia kohti.</span><span class="sxs-lookup"><span data-stu-id="0e117-184">You can also set up unit conversions per product variant.</span></span> <span data-ttu-id="0e117-185">Lisätietoa on kohdassa [Mittayksiköiden tuotevarianttikohtaiset muunnokset](../uom-conversion-per-product-variant.md).</span><span class="sxs-lookup"><span data-stu-id="0e117-185">For more information, see [Unit of measure conversion per product variant](../uom-conversion-per-product-variant.md).</span></span>

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
