---
title: ER Muodon päivittäminen ottamalla käyttöön sitä koskeva uusi perusversio
description: Seuraavissa vaiheissa kerrotaan, miten järjestelmänvalvojan tai sähköisen raportoinnin kehittäjän roolin omaava käyttäjä voi ylläpitää muotokonfiguraatiota sähköiselle raportoinnille (ER).
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERVendorPart, ERSolutionTable, ERSolutionCreateDropDialog, EROperationDesigner, ERComponentTypeDropDialog
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0b4ad9fb7a3d768acb0af73dcbe3d87b323de727
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/12/2020
ms.locfileid: "3042801"
---
# <a name="er-upgrade-your-format-by-adopting-a-new-base-version-of-that-format"></a><span data-ttu-id="7a832-103">ER Muodon päivittäminen ottamalla käyttöön sitä koskeva uusi perusversio</span><span class="sxs-lookup"><span data-stu-id="7a832-103">ER Upgrade your format by adopting a new, base version of that format</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="7a832-104">Seuraavissa vaiheissa kerrotaan, miten järjestelmänvalvojan tai sähköisen raportoinnin kehittäjän roolin omaava käyttäjä voi ylläpitää muotokonfiguraatiota sähköiselle raportoinnille (ER).</span><span class="sxs-lookup"><span data-stu-id="7a832-104">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can maintain an Electronic reporting (ER) format configuration.</span></span> <span data-ttu-id="7a832-105">Seuraavassa menettelyssä kerrotaan, miten luodaan muodosta mukautettu versio konfiguroinnin lähteen (CP) tarjoaman muodon perusteella.</span><span class="sxs-lookup"><span data-stu-id="7a832-105">This procedure explains how a custom version of a format can be created based on the format received from a configuration provider (CP).</span></span> <span data-ttu-id="7a832-106">Siinä käsitellään myös muodon uuden perusversion käyttöönotto.</span><span class="sxs-lookup"><span data-stu-id="7a832-106">It also explains how to adopt a new, base version of that format.</span></span>

<span data-ttu-id="7a832-107">Näitä vaiheita varten on suoritettava ensin seuraavien menettelyiden vaiheet: "Konfiguraation lähteen luominen ja sen merkitseminen aktiiviseksi" ja "Käytä luotua muotoa sähköisten maksuasiakirjojen luomiseen".</span><span class="sxs-lookup"><span data-stu-id="7a832-107">To complete these steps, you must first complete the steps in the “Create a configuration provider and mark it as active” and “Use created format to generate electronic documents for payments” procedures.</span></span> <span data-ttu-id="7a832-108">Nämä vaiheet voidaan suorittaa GBSI-yrityksessä.</span><span class="sxs-lookup"><span data-stu-id="7a832-108">These steps can be performed in the GBSI company.</span></span>

## <a name="select-format-configuration-for-customization"></a><span data-ttu-id="7a832-109">Mukautettavan muotokonfiguraation valinta</span><span class="sxs-lookup"><span data-stu-id="7a832-109">Select format configuration for customization</span></span>
1. <span data-ttu-id="7a832-110">Siirry kohtaan Organisaation hallinto > Työtilat > Sähköinen raportointi.</span><span class="sxs-lookup"><span data-stu-id="7a832-110">Go to Organization administration > Workspaces > Electronic reporting.</span></span>

    <span data-ttu-id="7a832-111">Tässä esimerkissä malliyritys Litware, Inc. (https://www.litware.com) toimii konfiguraation lähteenä, joka tukee tietyn maan muotokonfiguraatioita sähköisille maksuille.</span><span class="sxs-lookup"><span data-stu-id="7a832-111">In this example, sample company Litware, Inc. (https://www.litware.com) will act as a configuration provider that supports format configurations for electronic payments for a particular country.</span></span>    <span data-ttu-id="7a832-112">Malliyritys Proseware, Inc. (http://www.proseware.com) toimii kuluttajana Litware, Inc.:n toimittamalle muotokonfiguraatiolle.</span><span class="sxs-lookup"><span data-stu-id="7a832-112">Sample company Proseware, Inc. (http://www.proseware.com) will act as a consumer of the format configuration that Litware, Inc. provided.</span></span> <span data-ttu-id="7a832-113">Proseware, Inc. käyttää muotoja tietyillä maan alueilla.</span><span class="sxs-lookup"><span data-stu-id="7a832-113">Proseware, Inc. uses formats in certain regions of that country.</span></span>  
2. <span data-ttu-id="7a832-114">Valitse Raportointikonfiguraatiot.</span><span class="sxs-lookup"><span data-stu-id="7a832-114">Click Reporting configurations.</span></span>
3. <span data-ttu-id="7a832-115">Valitse Näytä suodattimet.</span><span class="sxs-lookup"><span data-stu-id="7a832-115">Click Show filters.</span></span>
4. <span data-ttu-id="7a832-116">Käytä seuraavia suodattimia: Anna suodattimen arvoksi Nimi-kenttään BACS (Iso-Britannia, kuvitteellinen) käyttämällä Alkaa-suodatinoperaattoria.</span><span class="sxs-lookup"><span data-stu-id="7a832-116">Apply the following filters: Enter a filter value of "BACS (UK fictitious)" on the "Name" field using the "begins with" filter operator.</span></span>
  
    <span data-ttu-id="7a832-117">Valitun BACS-muotomäärityksen (Iso-Britannia, kuvitteellinen ja mukautettu) omistaja on toimittaja Litware, Inc.</span><span class="sxs-lookup"><span data-stu-id="7a832-117">The selected format configuration BACS (UK fictitious) is owned by provider Litware, Inc.</span></span>  

5. <span data-ttu-id="7a832-118">Valitse Näytä suodattimet.</span><span class="sxs-lookup"><span data-stu-id="7a832-118">Click Show filters.</span></span>
6. <span data-ttu-id="7a832-119">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="7a832-119">In the list, find and select the desired record.</span></span>

    <span data-ttu-id="7a832-120">Proseware Inc. käyttää mukauttamiseen tämän muodon versiota, jonka tila on Valmis.</span><span class="sxs-lookup"><span data-stu-id="7a832-120">The version of the format with the status of Completed will be used by Proseware, Inc. for customization.</span></span>  

## <a name="create-a-new-configuration-for-your-custom-format-of-electronic-document"></a><span data-ttu-id="7a832-121">Luo uusi konfiguraatio sähköisen asiakirjan mukautetulle muodolle</span><span class="sxs-lookup"><span data-stu-id="7a832-121">Create a new configuration for your custom format of electronic document</span></span>
<span data-ttu-id="7a832-122">Proseware Inc. on vastaanottanut Litware, Inc:ltä palvelutilauksen mukaisesti version 1.1 BACS-muotokonfiguraatiosta (Iso-Britannia, kuvitteellinen), joka sisältää alustavan muodon sähköisten maksuasiakirjojen luomiseen</span><span class="sxs-lookup"><span data-stu-id="7a832-122">Proseware, Inc. received version 1.1 of BACS (UK fictitious) configuration that contains the initial format to generate electronic payment documents from Litware, Inc. in accordance to their service subscription.</span></span> <span data-ttu-id="7a832-123">Proseware Inc. haluaa käyttää konfiguraatiota vakiomuodossaan maassaan, mutta joitain mukautuksia tarvitaan tukemaan aluekohtaisia erityisvaatimuksia.</span><span class="sxs-lookup"><span data-stu-id="7a832-123">Proseware, Inc. wants to start using this as a standard for their country but some customization is required to support specific regional requirements.</span></span> <span data-ttu-id="7a832-124">Proseware Inc. haluaa säilyttää mahdollisuuden päivittää mukautetun muodon heti, kun uusi versio (joka sisältää muutoksia uusien maakohtaisten vaatimusten tukeen) on saatavilla Litware, Inc:ltä. Yritys haluaa myös suorittaa päivityksen mahdollisimman edullisesti.</span><span class="sxs-lookup"><span data-stu-id="7a832-124">Proseware, Inc. also wants to keep the ability to upgrade a custom format as soon as a new version of it (with changes to support new country-specific requirements) comes from Litware, Inc. and they want to perform this upgrade with the lowest cost.</span></span>  

<span data-ttu-id="7a832-125">Tätä varten Proseware, Inc:n on luotava määritys käyttämällä Litware, Inc:n BACS-muotokonfiguraatiota (Iso-Britannia, kuvitteellinen) pohjana.</span><span class="sxs-lookup"><span data-stu-id="7a832-125">To do this, Proseware, Inc. needs to create a configuration using the Litware, Inc. configuration BACS (UK fictitious) as a base.</span></span>  

1. <span data-ttu-id="7a832-126">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="7a832-126">Close the page.</span></span>
2. <span data-ttu-id="7a832-127">Valitse Proseware, Inc. ja tee siitä aktiivinen lähde.</span><span class="sxs-lookup"><span data-stu-id="7a832-127">Select Proseware, Inc. to make it an active provider.</span></span>
3. <span data-ttu-id="7a832-128">Valitse Aseta aktiiviseksi.</span><span class="sxs-lookup"><span data-stu-id="7a832-128">Click Set active.</span></span>
4. <span data-ttu-id="7a832-129">Valitse Raportointikonfiguraatiot.</span><span class="sxs-lookup"><span data-stu-id="7a832-129">Click Reporting configurations.</span></span>
5. <span data-ttu-id="7a832-130">Laajenna puussa solmu Payments (simplified model).</span><span class="sxs-lookup"><span data-stu-id="7a832-130">In the tree, expand 'Payments (simplified model)'.</span></span>
6. <span data-ttu-id="7a832-131">Valitse puussa solmu Payments (simplified model)\BACS (UK fictitious).</span><span class="sxs-lookup"><span data-stu-id="7a832-131">In the tree, select 'Payments (simplified model)\BACS (UK fictitious)'.</span></span>

    <span data-ttu-id="7a832-132">Valitse Litware, Inc:n BACS-muotokonfiguraatio (Iso-Britannia, kuvitteellinen). Proseware, Inc. käyttää versiota 1.1 mukautetun version pohjana.</span><span class="sxs-lookup"><span data-stu-id="7a832-132">Select the BACS (UK fictitious) configuration from Litware, Inc. Proseware, Inc. will use version 1.1 as a base for the custom version.</span></span>  

7. <span data-ttu-id="7a832-133">Avaa valintaikkuna napsauttamalla Luo konfigurointi.</span><span class="sxs-lookup"><span data-stu-id="7a832-133">Click Create configuration to open the drop dialog.</span></span>

    <span data-ttu-id="7a832-134">Näin voit luoda uuden määrityksen mukautetulle maksumuodolle.</span><span class="sxs-lookup"><span data-stu-id="7a832-134">This lets you create a new configuration for a custom payment format.</span></span>  

8. <span data-ttu-id="7a832-135">Anna Uusi-kentän arvoksi "Derive from Name: BACS (UK fictitious), Litware, Inc."</span><span class="sxs-lookup"><span data-stu-id="7a832-135">In the New field, enter 'Derive from Name: BACS (UK fictitious), Litware, Inc.'.</span></span>

    <span data-ttu-id="7a832-136">Valitse Johda-vaihtoehto vahvistaaksesi BACS (Iso-Britannia, kuvitteellinen) -konfiguraation käytön pohjana mukautetulle versiolle.</span><span class="sxs-lookup"><span data-stu-id="7a832-136">Select the Derive option to confirm the usage of BACS (UK fictitious) as the base for creating the custom version.</span></span>  

9. <span data-ttu-id="7a832-137">Syötä Nimi-kenttään BACS (Iso-Britannia, kuvitteellinen ja mukautettu).</span><span class="sxs-lookup"><span data-stu-id="7a832-137">In the Name field, type 'BACS (UK fictitious custom)'.</span></span>
10. <span data-ttu-id="7a832-138">Kirjoita Kuvaus-kenttään BACS - toimittajan maksumuoto (Iso-Britannia, kuvitteellinen ja mukautettu).</span><span class="sxs-lookup"><span data-stu-id="7a832-138">In the Description field, type 'BACS vendor payment (UK fictitious custom)'.</span></span>

    <span data-ttu-id="7a832-139">Aktiivinen konfiguraation lähde (Proseware, Inc.) syötetään tähän automaattisesti.</span><span class="sxs-lookup"><span data-stu-id="7a832-139">The active configuration provider (Proseware, Inc.) is automatically entered here.</span></span> <span data-ttu-id="7a832-140">Tämä lähde voi ylläpitää tätä konfiguraatiota.</span><span class="sxs-lookup"><span data-stu-id="7a832-140">This provider will be able to maintain this configuration.</span></span> <span data-ttu-id="7a832-141">Muut lähteet voivat käyttää tätä konfiguraatiota, mutta eivät ylläpitää sitä.</span><span class="sxs-lookup"><span data-stu-id="7a832-141">Other providers can use this configuration, but will not be able to maintain it.</span></span>  

11. <span data-ttu-id="7a832-142">Valitse Luo konfiguraatio.</span><span class="sxs-lookup"><span data-stu-id="7a832-142">Click Create configuration.</span></span>

## <a name="customize-your-format-for-the-electronic-document"></a><span data-ttu-id="7a832-143">Sähköisen asiakirjan muodon mukauttaminen</span><span class="sxs-lookup"><span data-stu-id="7a832-143">Customize your format for the electronic document</span></span>
1. <span data-ttu-id="7a832-144">Valitse Suunnittelutoiminto.</span><span class="sxs-lookup"><span data-stu-id="7a832-144">Click Designer.</span></span>
2. <span data-ttu-id="7a832-145">Valitse Laajenna tai tiivistä.</span><span class="sxs-lookup"><span data-stu-id="7a832-145">Click Expand/collapse.</span></span>
3. <span data-ttu-id="7a832-146">Valitse Laajenna tai tiivistä.</span><span class="sxs-lookup"><span data-stu-id="7a832-146">Click Expand/collapse.</span></span>
4. <span data-ttu-id="7a832-147">Valitse puussa Xml\Sanoma\Maksut\Nimike\Toimittaja\Pankki.</span><span class="sxs-lookup"><span data-stu-id="7a832-147">In the tree, select 'Xml\Message\Payments\Item\Vendor\Bank'.</span></span>
5. <span data-ttu-id="7a832-148">Avaa valintaikkuna valitsemalla Lisää.</span><span class="sxs-lookup"><span data-stu-id="7a832-148">Click Add to open the drop dialog.</span></span>
6. <span data-ttu-id="7a832-149">Valitse puussa solmu XML\Element.</span><span class="sxs-lookup"><span data-stu-id="7a832-149">In the tree, select 'XML\Element'.</span></span>
7. <span data-ttu-id="7a832-150">Syötä Nimi-kenttään IBAN.</span><span class="sxs-lookup"><span data-stu-id="7a832-150">In the Name field, type 'IBAN'.</span></span>
8. <span data-ttu-id="7a832-151">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="7a832-151">Click OK.</span></span>
9. <span data-ttu-id="7a832-152">Valitse puussa Xml\Sanoma\Maksut\Nimike\Toimittaja\Pankki\IBAN.</span><span class="sxs-lookup"><span data-stu-id="7a832-152">In the tree, select 'Xml\Message\Payments\Item\Vendor\Bank\IBAN'.</span></span>
10. <span data-ttu-id="7a832-153">Avaa valintaikkuna valitsemalla Lisää.</span><span class="sxs-lookup"><span data-stu-id="7a832-153">Click Add to open the drop dialog.</span></span>
11. <span data-ttu-id="7a832-154">Valitse puussa solmu Text\String.</span><span class="sxs-lookup"><span data-stu-id="7a832-154">In the tree, select 'Text\String'.</span></span>
12. <span data-ttu-id="7a832-155">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="7a832-155">Click OK.</span></span>
13. <span data-ttu-id="7a832-156">Valitse puussa Xml\Sanoma\Maksut\Nimike\Toimittaja\Nimi\Merkkijono.</span><span class="sxs-lookup"><span data-stu-id="7a832-156">In the tree, select 'Xml\Message\Payments\Item\Vendor\Name\String'.</span></span>
14. <span data-ttu-id="7a832-157">Anna Enimmäispituus-kentän arvoksi 60.</span><span class="sxs-lookup"><span data-stu-id="7a832-157">In the Maximum length field, enter '60'.</span></span>
15. <span data-ttu-id="7a832-158">Valitse Yhdistämismääritys-välilehti.</span><span class="sxs-lookup"><span data-stu-id="7a832-158">Click the Mapping tab.</span></span>
16. <span data-ttu-id="7a832-159">Laajenna puussa solmu model.</span><span class="sxs-lookup"><span data-stu-id="7a832-159">In the tree, expand 'model'.</span></span>
17. <span data-ttu-id="7a832-160">Laajenna puussa solmu model\Payments.</span><span class="sxs-lookup"><span data-stu-id="7a832-160">In the tree, expand 'model\Payments'.</span></span>
18. <span data-ttu-id="7a832-161">Laajenna puussa solmu model\Payments\Creditor.</span><span class="sxs-lookup"><span data-stu-id="7a832-161">In the tree, expand 'model\Payments\Creditor'.</span></span>
19. <span data-ttu-id="7a832-162">Laajenna puussa solmu model\Payments\Creditor\Account.</span><span class="sxs-lookup"><span data-stu-id="7a832-162">In the tree, expand 'model\Payments\Creditor\Account'.</span></span>
20. <span data-ttu-id="7a832-163">Valitse puussa malli\Maksut\Laskuttaja\Tili\IBAN.</span><span class="sxs-lookup"><span data-stu-id="7a832-163">In the tree, select 'model\Payments\Creditor\Account\IBAN'.</span></span>
21. <span data-ttu-id="7a832-164">Valitse puussa Xml\Sanoma\Maksut\Nimike =  model.Payments\Vendor\Bank\IBAN\String.</span><span class="sxs-lookup"><span data-stu-id="7a832-164">In the tree, select 'Xml\Message\Payments\Item =  model.Payments\Vendor\Bank\IBAN\String'.</span></span>
22. <span data-ttu-id="7a832-165">Valitse Sido.</span><span class="sxs-lookup"><span data-stu-id="7a832-165">Click Bind.</span></span>
23. <span data-ttu-id="7a832-166">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="7a832-166">Click Save.</span></span>

## <a name="validate-the-customized-format"></a><span data-ttu-id="7a832-167">Mukautetun muodon vahvistaminen</span><span class="sxs-lookup"><span data-stu-id="7a832-167">Validate the customized format</span></span>
1. <span data-ttu-id="7a832-168">Valitse Vahvista.</span><span class="sxs-lookup"><span data-stu-id="7a832-168">Click Validate.</span></span>

    <span data-ttu-id="7a832-169">Vahvista mukautetun muodon asettelu ja tietojen yhdistämisen muutokset, että kaikki sidokset ovat kunnossa.</span><span class="sxs-lookup"><span data-stu-id="7a832-169">Validate the customized format layout and data mapping changes to make sure that all bindings are okay.</span></span>  

2. <span data-ttu-id="7a832-170">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="7a832-170">Close the page.</span></span>

## <a name="change-the-status-of-the-current-version-of-the-custom-format-configuration"></a><span data-ttu-id="7a832-171">Mukautetun muotomäärityksen nykyisen version tilan muuttaminen</span><span class="sxs-lookup"><span data-stu-id="7a832-171">Change the status of the current version of the custom format configuration</span></span>
<span data-ttu-id="7a832-172">Muuta suunnitellun muotomäärityksen tila Luonnos-tilasta Valmis-tilaan. Tällöin se on käytettävissä maksuasiakirjojen luomiseen.</span><span class="sxs-lookup"><span data-stu-id="7a832-172">Change the status of the designed format configuration from Draft to Completed to make it available for payment document generation.</span></span>  

1. <span data-ttu-id="7a832-173">Voit muuttaa tilaa valitsemalla Muuta.</span><span class="sxs-lookup"><span data-stu-id="7a832-173">Click Change status.</span></span>

    <span data-ttu-id="7a832-174">Huomaa, että valitun konfiguraation nykyisen version tila on Luonnos.</span><span class="sxs-lookup"><span data-stu-id="7a832-174">Note that the current version of the selected configuration is in Draft status.</span></span>  

2. <span data-ttu-id="7a832-175">Valitse Valmis.</span><span class="sxs-lookup"><span data-stu-id="7a832-175">Click Complete.</span></span>
3. <span data-ttu-id="7a832-176">Kirjoita arvo Kuvaus-kenttään.</span><span class="sxs-lookup"><span data-stu-id="7a832-176">In the Description field, type a value.</span></span>
4. <span data-ttu-id="7a832-177">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="7a832-177">Click OK.</span></span>
5. <span data-ttu-id="7a832-178">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="7a832-178">In the list, find and select the desired record.</span></span>

    <span data-ttu-id="7a832-179">Huomaa, että luotu konfiguraatio tallennetaan valmiina versiona 1.1.1.</span><span class="sxs-lookup"><span data-stu-id="7a832-179">Note that the created configuration is saved as completed version 1.1.1.</span></span> <span data-ttu-id="7a832-180">Tämä tarkoittaa, että kyseessä on mukautetun BACS-muodon (Iso-Britannia, kuvitteellinen ja mukautettu) versio 1, joka perustuu BACS-muodon versioon 1, joka perustuu Maksut-tietomallin versioon 1 (yksinkertaistettu malli).</span><span class="sxs-lookup"><span data-stu-id="7a832-180">This means it is version 1 of the custom BACS (UK fictitious custom) format, which is based on version 1 of the BACS (UK fictitious) format, which is based on version 1 of the Payments (simplified model) data model.</span></span>  

## <a name="test-the-customized-format-to-generate-payment-files"></a><span data-ttu-id="7a832-181">Mukautetun muodon maksutiedostojen luonnin testaaminen</span><span class="sxs-lookup"><span data-stu-id="7a832-181">Test the customized format to generate payment files</span></span>
<span data-ttu-id="7a832-182">Suorita Käytä luotua muotoa sähköisten maksuasiakirjojen luomiseen -menettelyn vaiheet rinnakkaisessa Finance and Operations -istunnossa.</span><span class="sxs-lookup"><span data-stu-id="7a832-182">Complete the steps in the “Use created format to generate electronic documents for payments” procedure in a parallel Finance and Operations session.</span></span> <span data-ttu-id="7a832-183">Valitse BACS-muoto (Iso-Britannia, kuvitteellinen ja mukautettu) sähköisen maksutavan parametreissa.</span><span class="sxs-lookup"><span data-stu-id="7a832-183">Select the BACS (UK fictitious custom) format in electronic payment method parameters.</span></span> <span data-ttu-id="7a832-184">Varmista, että luotu maksutiedosto sisältää on viimeisimmän XML-solmun, joka vastaa IBAN-koodia aluekohtaisten vaatimusten mukaisesti.</span><span class="sxs-lookup"><span data-stu-id="7a832-184">Make sure that the created payment file contains the recently introduced XML node presenting IBAN code in accordance to regional requirements.</span></span>  

## <a name="update-the-existing-country-specific-configuration"></a><span data-ttu-id="7a832-185">Olemassaolevien maakohtaisten konfiguraatioiden päivittäminen</span><span class="sxs-lookup"><span data-stu-id="7a832-185">Update the existing country-specific configuration</span></span>
<span data-ttu-id="7a832-186">Litware, Inc. haluaa päivittää BACS-konfiguraation (Iso-Britannia, kuvitteellinen) ja ottaa käyttöön uudet maavaatimukset sähköisen asiakirjan muodon hallinnassa.</span><span class="sxs-lookup"><span data-stu-id="7a832-186">Litware, Inc. needs to update the BACS (UK fictitious) configuration and adopt new country requirements for managing the format of the electronic document.</span></span> <span data-ttu-id="7a832-187">Tämä sisältyy tulevaan konfiguraation versiopäivitykseen, joka tarjotaan palvelun tilaajille, joihin Proseware, Inc. kuuluu.</span><span class="sxs-lookup"><span data-stu-id="7a832-187">Later, this will be enclosed in a new version of this configuration that will be offered for service subscribers, including Proseware, Inc.</span></span>  

<span data-ttu-id="7a832-188">Todellisissa palveluntoteutusprosesseissa Proseware Inc. voi tuoda jokaisen uuden version BACS-muodosta (Iso-Britannia, kuvitteellinen) Litware, Inc:n LCS-konfiguraatiosäilöstä.</span><span class="sxs-lookup"><span data-stu-id="7a832-188">In real service provision related processes, each new version of BACS (UK fictitious) can be imported by Proseware, Inc. from Litware, Inc. configurations’ LCS repository.</span></span> <span data-ttu-id="7a832-189">Näissä toimintaohjeissa tätä simuloidaan päivittämällä BACS-muoto (Iso-Britannia, kuvitteellinen) palveluntarjoajan puolesta.</span><span class="sxs-lookup"><span data-stu-id="7a832-189">In this procedure we will simulate this by updating BACS (UK fictitious) on behalf of a service provider.</span></span>  

1. <span data-ttu-id="7a832-190">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="7a832-190">Close the page.</span></span>
2. <span data-ttu-id="7a832-191">Valitse lähteeksi Litware, Inc.</span><span class="sxs-lookup"><span data-stu-id="7a832-191">Select Litware, inc. provider.</span></span>
3. <span data-ttu-id="7a832-192">Valitse Aseta aktiiviseksi.</span><span class="sxs-lookup"><span data-stu-id="7a832-192">Click Set active.</span></span>
4. <span data-ttu-id="7a832-193">Valitse Raportointikonfiguraatiot.</span><span class="sxs-lookup"><span data-stu-id="7a832-193">Click Reporting configurations.</span></span>
5. <span data-ttu-id="7a832-194">Laajenna puussa solmu Payments (simplified model).</span><span class="sxs-lookup"><span data-stu-id="7a832-194">In the tree, expand 'Payments (simplified model)'.</span></span>
6. <span data-ttu-id="7a832-195">Valitse puussa solmu Payments (simplified model)\BACS (UK fictitious).</span><span class="sxs-lookup"><span data-stu-id="7a832-195">In the tree, select 'Payments (simplified model)\BACS (UK fictitious)'.</span></span>

    <span data-ttu-id="7a832-196">Litware, Inc:n omistaman luonnosversion lähde-BACS (Iso-Britannia, kuvitteellinen) valitaan tuomaan uusien maakohtaisten vaatimusten tuki.</span><span class="sxs-lookup"><span data-stu-id="7a832-196">The draft version owned by Litware, Inc. provider BACS (UK fictitious) is selected to bring in changes to support new country-specific requirements.</span></span>  

## <a name="localize-the-base-format-of-the-electronic-document"></a><span data-ttu-id="7a832-197">Sähköisen asiakirjan perusmuodon lokalisoiminen</span><span class="sxs-lookup"><span data-stu-id="7a832-197">Localize the base format of the electronic document</span></span>
<span data-ttu-id="7a832-198">Oletetaan, että Litware Inc:n on tuettava seuraavia uusia maakohtaisia vaatimuksia:</span><span class="sxs-lookup"><span data-stu-id="7a832-198">Assume that there are new country-specific requirements to be supported by Litware, Inc.:</span></span>  

- <span data-ttu-id="7a832-199">Arvo laskuttajan SWIFT-koodille jokaisessa maksutapahtumassa.</span><span class="sxs-lookup"><span data-stu-id="7a832-199">A value for the creditor’s bank SWIFT code in each payment transaction.</span></span>
- <span data-ttu-id="7a832-200">100 merkin raja toimittajan nimelle luontitiedostossa.</span><span class="sxs-lookup"><span data-stu-id="7a832-200">A limit of 100 characters for the length of text for the vendor’s name in a generating file.</span></span>  
- <span data-ttu-id="7a832-201">Uudet maakohtaiset vaatimukset</span><span class="sxs-lookup"><span data-stu-id="7a832-201">New country-specific requirements</span></span>  
- <span data-ttu-id="7a832-202">Valitse halutun konfiguraation luonnosversio tuodaksesi vaaditut muutokset.</span><span class="sxs-lookup"><span data-stu-id="7a832-202">Select the draft version of the desired configuration to introduce required changes.</span></span>  


1. <span data-ttu-id="7a832-203">Valitse Suunnittelutoiminto.</span><span class="sxs-lookup"><span data-stu-id="7a832-203">Click Designer.</span></span>
2. <span data-ttu-id="7a832-204">Valitse Laajenna tai tiivistä.</span><span class="sxs-lookup"><span data-stu-id="7a832-204">Click Expand/collapse.</span></span>
3. <span data-ttu-id="7a832-205">Valitse Laajenna tai tiivistä.</span><span class="sxs-lookup"><span data-stu-id="7a832-205">Click Expand/collapse.</span></span>
4. <span data-ttu-id="7a832-206">Valitse puussa Xml\Sanoma\Maksut\Nimike\Toimittaja\Pankki.</span><span class="sxs-lookup"><span data-stu-id="7a832-206">In the tree, select 'Xml\Message\Payments\Item\Vendor\Bank'.</span></span>
5. <span data-ttu-id="7a832-207">Avaa valintaikkuna valitsemalla Lisää.</span><span class="sxs-lookup"><span data-stu-id="7a832-207">Click Add to open the drop dialog.</span></span>
6. <span data-ttu-id="7a832-208">Valitse puussa solmu XML\Element.</span><span class="sxs-lookup"><span data-stu-id="7a832-208">In the tree, select 'XML\Element'.</span></span>
7. <span data-ttu-id="7a832-209">Syötä Nimi-kenttään SWIFT.</span><span class="sxs-lookup"><span data-stu-id="7a832-209">In the Name field, type 'SWIFT'.</span></span>
8. <span data-ttu-id="7a832-210">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="7a832-210">Click OK.</span></span>
9. <span data-ttu-id="7a832-211">Valitse puussa Xml\Sanoma\Maksut\Nimike\Toimittaja\Pankki\SWIFT.</span><span class="sxs-lookup"><span data-stu-id="7a832-211">In the tree, select 'Xml\Message\Payments\Item\Vendor\Bank\SWIFT'.</span></span>
10. <span data-ttu-id="7a832-212">Avaa valintaikkuna valitsemalla Lisää.</span><span class="sxs-lookup"><span data-stu-id="7a832-212">Click Add to open the drop dialog.</span></span>
11. <span data-ttu-id="7a832-213">Valitse puussa solmu Text\String.</span><span class="sxs-lookup"><span data-stu-id="7a832-213">In the tree, select 'Text\String'.</span></span>
12. <span data-ttu-id="7a832-214">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="7a832-214">Click OK.</span></span>
13. <span data-ttu-id="7a832-215">Valitse puussa Xml\Sanoma\Maksut\Nimike\Toimittaja\Nimi\Merkkijono.</span><span class="sxs-lookup"><span data-stu-id="7a832-215">In the tree, select 'Xml\Message\Payments\Item\Vendor\Name\String'.</span></span>
14. <span data-ttu-id="7a832-216">Anna Enimmäispituus-kentän arvoksi 100.</span><span class="sxs-lookup"><span data-stu-id="7a832-216">In the Maximum length field, enter '100'.</span></span>
15. <span data-ttu-id="7a832-217">Valitse Yhdistämismääritys-välilehti.</span><span class="sxs-lookup"><span data-stu-id="7a832-217">Click the Mapping tab.</span></span>
16. <span data-ttu-id="7a832-218">Laajenna puussa solmu model.</span><span class="sxs-lookup"><span data-stu-id="7a832-218">In the tree, expand 'model'.</span></span>
17. <span data-ttu-id="7a832-219">Laajenna puussa solmu model\Payments.</span><span class="sxs-lookup"><span data-stu-id="7a832-219">In the tree, expand 'model\Payments'.</span></span>
18. <span data-ttu-id="7a832-220">Laajenna puussa solmu model\Payments\Creditor.</span><span class="sxs-lookup"><span data-stu-id="7a832-220">In the tree, expand 'model\Payments\Creditor'.</span></span>
19. <span data-ttu-id="7a832-221">Laajenna puussa solmu expand 'model\Payments\Creditor\Agent.</span><span class="sxs-lookup"><span data-stu-id="7a832-221">In the tree, expand 'model\Payments\Creditor\Agent'.</span></span>
20. <span data-ttu-id="7a832-222">Valitse puussa malli\Maksut\Laskuttaja\Edustaja\SWIFT.</span><span class="sxs-lookup"><span data-stu-id="7a832-222">In the tree, select 'model\Payments\Creditor\Agent\SWIFT'.</span></span>
21. <span data-ttu-id="7a832-223">Valitse puussa Xml\Sanoma\Maksut\Nimike =  model.Payments\Vendor\Bank\SWIFT\String.</span><span class="sxs-lookup"><span data-stu-id="7a832-223">In the tree, select 'Xml\Message\Payments\Item =  model.Payments\Vendor\Bank\SWIFT\String'.</span></span>
22. <span data-ttu-id="7a832-224">Valitse Sido.</span><span class="sxs-lookup"><span data-stu-id="7a832-224">Click Bind.</span></span>
23. <span data-ttu-id="7a832-225">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="7a832-225">Click Save.</span></span>

## <a name="validate-the-localized-format"></a><span data-ttu-id="7a832-226">Lokalisoidun muodon tarkistaminen</span><span class="sxs-lookup"><span data-stu-id="7a832-226">Validate the localized format</span></span>
1. <span data-ttu-id="7a832-227">Valitse Vahvista.</span><span class="sxs-lookup"><span data-stu-id="7a832-227">Click Validate.</span></span>
2. <span data-ttu-id="7a832-228">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="7a832-228">Close the page.</span></span>

## <a name="change-the-status-of-the-current-version-of-the-base-format-configuration"></a><span data-ttu-id="7a832-229">Muotokonfiguraation nykyisen perusversion tilan muuttaminen</span><span class="sxs-lookup"><span data-stu-id="7a832-229">Change the status of the current version of the base format configuration</span></span>
<span data-ttu-id="7a832-230">Muutta päivitetyn muotokonfiguraation perusversion tila luonnoksesta valmiiksi, jotta se on käytettävissä maksuasiakirjojen luomiseen ja siitä johdettujen muotokonfiguraatioiden päivityksiin.</span><span class="sxs-lookup"><span data-stu-id="7a832-230">Change the status of the updated base format configuration from Draft to Completed to make it available for generation of payment documents and updates of format configurations derived from it.</span></span>  

1. <span data-ttu-id="7a832-231">Voit muuttaa tilaa valitsemalla Muuta.</span><span class="sxs-lookup"><span data-stu-id="7a832-231">Click Change status.</span></span>

    <span data-ttu-id="7a832-232">Huomaa, että valitun konfiguraation nykyisen version tila on Luonnos.</span><span class="sxs-lookup"><span data-stu-id="7a832-232">Note that the current version of the selected configuration is in Draft status.</span></span>  

2. <span data-ttu-id="7a832-233">Valitse Valmis.</span><span class="sxs-lookup"><span data-stu-id="7a832-233">Click Complete.</span></span>
3. <span data-ttu-id="7a832-234">Kirjoita arvo Kuvaus-kenttään.</span><span class="sxs-lookup"><span data-stu-id="7a832-234">In the Description field, type a value.</span></span>
4. <span data-ttu-id="7a832-235">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="7a832-235">Click OK.</span></span>
5. <span data-ttu-id="7a832-236">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="7a832-236">In the list, find and select the desired record.</span></span>

## <a name="change-the-base-version-for-the-custom-format-configuration"></a><span data-ttu-id="7a832-237">Mukautetun muotokonfiguraation perusversion muuttaminen</span><span class="sxs-lookup"><span data-stu-id="7a832-237">Change the base version for the custom format configuration</span></span>

<span data-ttu-id="7a832-238">Proseware, Inc. saa tiedon, että saatavilla on BACS-konfiguraation (Iso-Britannia, kuvitteellinen) versiopäivitys 1.2, jolla on mahdollista luoda sähköisiä maksuasiakirjoja vasta julkaistujen maakohtaisten vaatimusten mukaisesti.</span><span class="sxs-lookup"><span data-stu-id="7a832-238">Proseware, Inc. is informed that a new version 1.2 of BACS (UK fictitious) configuration is available to generate electronic payment documents in accordance to recently announced country-specific requirements.</span></span> <span data-ttu-id="7a832-239">Proseware, Inc. haluaa käyttää uutta versiota maan standardien noudattamiseen.</span><span class="sxs-lookup"><span data-stu-id="7a832-239">Proseware, Inc. wants to start using it as a standard for the country.</span></span>  

<span data-ttu-id="7a832-240">Tämän vuoksi Proseware, Inc:n on muutettava peruskonfiguraation versiota mukautetulle BACS-konfiguraatiolleen (Iso-Britannia, kuvitteellinen ja mukautettu).</span><span class="sxs-lookup"><span data-stu-id="7a832-240">To do this, Proseware, Inc. needs to change the base configuration version for the custom configuration BACS (UK fictitious custom).</span></span> <span data-ttu-id="7a832-241">Käytä uutta versiota 1.2 edellisen BACS-muodon (Iso-Britannia, kuvitteellinen) 1.1-version sijaan.</span><span class="sxs-lookup"><span data-stu-id="7a832-241">Instead of version 1.1 of BACS (UK fictitious) use new version 1.2.</span></span>  

1. <span data-ttu-id="7a832-242">Siirry kohtaan Organisaation hallinto > Työtilat > Sähköinen raportointi.</span><span class="sxs-lookup"><span data-stu-id="7a832-242">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="7a832-243">Valitse Proseware, Inc -lähde ja merkitse aktiiviseksi.</span><span class="sxs-lookup"><span data-stu-id="7a832-243">Select the Proseware, Inc. provider to mark it as active.</span></span>
3. <span data-ttu-id="7a832-244">Valitse Aseta aktiiviseksi.</span><span class="sxs-lookup"><span data-stu-id="7a832-244">Click Set active.</span></span>
4. <span data-ttu-id="7a832-245">Valitse Raportointikonfiguraatiot.</span><span class="sxs-lookup"><span data-stu-id="7a832-245">Click Reporting configurations.</span></span>
5. <span data-ttu-id="7a832-246">Laajenna puussa solmu Payments (simplified model).</span><span class="sxs-lookup"><span data-stu-id="7a832-246">In the tree, expand 'Payments (simplified model)'.</span></span>
6. <span data-ttu-id="7a832-247">Laajenna puussa solmu Payments (simplified model)\BACS (UK fictitious).</span><span class="sxs-lookup"><span data-stu-id="7a832-247">In the tree, expand 'Payments (simplified model)\BACS (UK fictitious)'.</span></span>
7. <span data-ttu-id="7a832-248">Valitse puussa solmu Payments (simplified model)\BACS (UK fictitious)\BACS (UK fictitious custom).</span><span class="sxs-lookup"><span data-stu-id="7a832-248">In the tree, select 'Payments (simplified model)\BACS (UK fictitious)\BACS (UK fictitious custom)'.</span></span>

    <span data-ttu-id="7a832-249">Valitse BACS-muodon (Iso-Britannia, kuvitteellinen ja mukautettu) konfiguraatio, jonka omistaa Proseware, Inc.</span><span class="sxs-lookup"><span data-stu-id="7a832-249">Select the BACS (UK fictitious custom) configuration, which is owned by Proseware, Inc.</span></span>  

    <span data-ttu-id="7a832-250">Käytä valitun konfiguraation luonnosversiota tuodaksesi vaaditut muutokset.</span><span class="sxs-lookup"><span data-stu-id="7a832-250">Use the draft version of the selected configuration to introduce required changes.</span></span>  

8. <span data-ttu-id="7a832-251">Valitse Pohjusta.</span><span class="sxs-lookup"><span data-stu-id="7a832-251">Click Rebase.</span></span>

    <span data-ttu-id="7a832-252">Valitse peruskonfiguraation uusi versio 1.2 käytettäväksi perusteena konfiguraation päivityksille.</span><span class="sxs-lookup"><span data-stu-id="7a832-252">Select the new version 1.2 of the base configuration to be applied as a new base for updating the configuration.</span></span>  

9. <span data-ttu-id="7a832-253">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="7a832-253">Click OK.</span></span>

    <span data-ttu-id="7a832-254">Huomaa, että osaa muodon muutosten ristiriidoista, jotka havaitaan mukautetun version ja uuden perusversion yhdistämisen yhteydessä, ei voida yhdistää automaattisesti.</span><span class="sxs-lookup"><span data-stu-id="7a832-254">Note that some conflicts have been discovered between merging the custom version and a new base version representing some format changes that can’t be merged automatically.</span></span>  

## <a name="resolve-rebase-conflicts"></a><span data-ttu-id="7a832-255">Pohjustusriitojen ratkaiseminen</span><span class="sxs-lookup"><span data-stu-id="7a832-255">Resolve rebase conflicts</span></span>
1. <span data-ttu-id="7a832-256">Valitse Suunnittelutoiminto.</span><span class="sxs-lookup"><span data-stu-id="7a832-256">Click Designer.</span></span>
    
    <span data-ttu-id="7a832-257">Huomaa, että muutoksia toimittajan nimen pituusrajoitukseen ei voitu selvittää automaattisesti.</span><span class="sxs-lookup"><span data-stu-id="7a832-257">Note that changes to the vendor’s name text length limit couldn’t be resolved automatically.</span></span> <span data-ttu-id="7a832-258">Tämä esitetään sen vuoksi ristiriitojen luettelossa.</span><span class="sxs-lookup"><span data-stu-id="7a832-258">Therefore, this is presented in a conflicts list.</span></span> <span data-ttu-id="7a832-259">Jokaiselle päivitystyypin ristiriidalle on seuraavat ratkaisuvaihtoehdot: - Käytä aiempaa perusarvoa (painike ruudukon yläpuolella) edellisen perusversion arvon mukaisesti (tässä tapauksessa 0).</span><span class="sxs-lookup"><span data-stu-id="7a832-259">For each conflict of type Update, the following options are available:  - Apply a prior base value (button on top of the grid) to bring in the previous base version value (0 in our case).</span></span>  <span data-ttu-id="7a832-260">- Käytä perusarvoa (painike ruudukon yläpuolella) uuden perusversion arvon mukaisesti (tässä tapauksessa 100).</span><span class="sxs-lookup"><span data-stu-id="7a832-260">- Apply a base value (button on top of the grid) to bring in the new base version value (100 in our case).</span></span>  <span data-ttu-id="7a832-261">- Säilytä oma (mukautettu) arvo (tässä tapauksessa 60).</span><span class="sxs-lookup"><span data-stu-id="7a832-261">- Keep your own (custom) value (60 in our case).</span></span>  <span data-ttu-id="7a832-262">Valitse Kohdista perusarvo -painiketta kohdistaaksesi maakohtaisesti sallitut 100 merkkiä toimittajan nimille.</span><span class="sxs-lookup"><span data-stu-id="7a832-262">Click Apply base value to apply a country-specific limit of 100 characters for vendor’s name text length.</span></span>  

    <span data-ttu-id="7a832-263">Huomaa, että Proseware, Inc. ja Litware, Inc. käyttävät mukautettuja ja paikallisia versioita tästä muodosta käyttäen IBAN- ja SWIFT-koodeja liittyvissä komponenteissa, jotka yhdistetään automaattisesti hallitussa muodossa.</span><span class="sxs-lookup"><span data-stu-id="7a832-263">Note that Proseware, Inc. and Litware, Inc. have custom and local versions of this format using IBAN and SWIFT codes with related components that are automatically merged in the managing format.</span></span>  

2. <span data-ttu-id="7a832-264">Valitse Käytä aiempaa perusarvoa.</span><span class="sxs-lookup"><span data-stu-id="7a832-264">Click Apply base value.</span></span>

    <span data-ttu-id="7a832-265">Valitse Kohdista perusarvo -painiketta kohdistaaksesi maakohtaisesti sallitut 100 merkkiä toimittajan nimille.</span><span class="sxs-lookup"><span data-stu-id="7a832-265">Click Apply base value to apply the country-specific limit of 100 characters for vendor names.</span></span>  

3. <span data-ttu-id="7a832-266">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="7a832-266">Click Save.</span></span>

    <span data-ttu-id="7a832-267">Muodon tallentaminen poistaa ratkaistut ristiriidat luettelosta.</span><span class="sxs-lookup"><span data-stu-id="7a832-267">Saving the format will remove resolved conflicts from the conflicts list.</span></span>  

4. <span data-ttu-id="7a832-268">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="7a832-268">Close the page.</span></span>

## <a name="change-the-status-of-the-new-version-of-the-custom-format-configuration"></a><span data-ttu-id="7a832-269">Muotokonfiguraation uuden mukautetun version tilan muuttaminen</span><span class="sxs-lookup"><span data-stu-id="7a832-269">Change the status of the new version of the custom format configuration</span></span>
1. <span data-ttu-id="7a832-270">Voit muuttaa tilaa valitsemalla Muuta.</span><span class="sxs-lookup"><span data-stu-id="7a832-270">Click Change status.</span></span>

    <span data-ttu-id="7a832-271">Muuttaa päivitetyn mukautetun muotokonfiguraation tilan luonnoksesta valmiiksi.</span><span class="sxs-lookup"><span data-stu-id="7a832-271">Change the status of the updated, custom format configuration from Draft to Completed.</span></span> <span data-ttu-id="7a832-272">Muotomääritykset ovat nyt käytettävissä maksuasiakirjoja luotaessa.</span><span class="sxs-lookup"><span data-stu-id="7a832-272">This will make the format configuration available for generating payment documents.</span></span> <span data-ttu-id="7a832-273">Huomaa, että valitun konfiguraation nykyisen version tila on Luonnos.</span><span class="sxs-lookup"><span data-stu-id="7a832-273">Note that the current version of the selected configuration is in Draft status.</span></span>  

2. <span data-ttu-id="7a832-274">Valitse Valmis.</span><span class="sxs-lookup"><span data-stu-id="7a832-274">Click Complete.</span></span>
3. <span data-ttu-id="7a832-275">Kirjoita arvo Kuvaus-kenttään.</span><span class="sxs-lookup"><span data-stu-id="7a832-275">In the Description field, type a value.</span></span>
4. <span data-ttu-id="7a832-276">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="7a832-276">Click OK.</span></span>

    <span data-ttu-id="7a832-277">Huomaa, että luotu konfiguraatio tallennetaan valmiina versiona 1.2.2: BACS-perusmuodon (Iso-Britannia, kuvitteellinen ja mukautettu) versiona 2, joka perustuu BACS-perusmuodon (Iso-Britannia, kuvitteellinen) versioon 2, joka perustuu maksujen tietomallin versioon 1 (yksinkertaistettu malli).</span><span class="sxs-lookup"><span data-stu-id="7a832-277">Note that the created configuration is saved as completed version 1.2.2: version 2 of base BACS (UK fictitious custom) format, which is based on version 2 of base BACS (UK fictitious) format, which is based on version 1 of Payments (simplified model) data model.</span></span>  

## <a name="test-the-customized-format-for-payment-files-generation"></a><span data-ttu-id="7a832-278">Mukautetun muodon maksutiedostojen luonnin testaaminen</span><span class="sxs-lookup"><span data-stu-id="7a832-278">Test the customized format for payment files generation</span></span>
<span data-ttu-id="7a832-279">Suorita Käytä luotua muotoa sähköisten maksuasiakirjojen luomiseen -menettelyn vaiheet rinnakkaisessa Finance and Operations -istunnossa.</span><span class="sxs-lookup"><span data-stu-id="7a832-279">Complete the steps in the “Use created format to generate electronic documents for payments” procedure in parallel Finance and Operations session.</span></span> <span data-ttu-id="7a832-280">Valitse luotu BACS-muoto (Iso-Britannia, kuvitteellinen ja mukautettu) sähköisen maksutavan parametreissa.</span><span class="sxs-lookup"><span data-stu-id="7a832-280">Select the created ‘BACS (UK fictitious custom)’ format in electronic payment method parameters.</span></span> <span data-ttu-id="7a832-281">Varmista, että luotu maksutiedosto sisältää on viimeisimmän Proseware, Inc:n XML-solmun, joka vastaa IBAN-tilikoodia aluekohtaisten vaatimusten mukaisesti.</span><span class="sxs-lookup"><span data-stu-id="7a832-281">Make sure that the created payment file contains recently introduced by Proseware, Inc. XML node presenting IBAN account code in accordance to regional requirements.</span></span> <span data-ttu-id="7a832-282">Tiedoston pitäisi myös sisältää viimeisin Litware, Inc:n XML-solmu, joka edustaa SWIFT-pankkikoodia maakohtaisten vaatimusten mukaisesti.</span><span class="sxs-lookup"><span data-stu-id="7a832-282">The file also should contain the recently introduced by Litware, Inc. XML node presenting SWIFT bank code in accordance to country requirements.</span></span>  

