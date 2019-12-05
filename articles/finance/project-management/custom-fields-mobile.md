---
title: Ota Microsoft Dynamics 365 Project Timesheet -mobiilisovelluksen mukautetut kentät käyttöön iOS:ssa ja Androidissa
description: Tässä ohjeaiheessa on yleisiä tapoja käyttää laajennuksia mukautettujen kenttien käyttöönottoon.
author: KimANelson
manager: AnnBe
ms.date: 05/29/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: knelson
ms.dyn365.ops.version: 10.0.3
ms.search.validFrom: 2019-05-29
ms.openlocfilehash: c0c578ca44919671b67daeea51a9ec7687f755c9
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/06/2019
ms.locfileid: "2773642"
---
# <a name="implement-custom-fields-for-the-microsoft-dynamics-365-project-timesheet-mobile-app-on-ios-and-android"></a><span data-ttu-id="f4b7f-103">Ota Microsoft Dynamics 365 Project Timesheet -mobiilisovelluksen mukautetut kentät käyttöön iOS:ssa ja Androidissa</span><span class="sxs-lookup"><span data-stu-id="f4b7f-103">Implement custom fields for the Microsoft Dynamics 365 Project Timesheet mobile app on iOS and Android</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f4b7f-104">Tässä ohjeaiheessa on yleisiä tapoja käyttää laajennuksia mukautettujen kenttien käyttöönottoon.</span><span class="sxs-lookup"><span data-stu-id="f4b7f-104">This topic provides common patterns for using extensions to implement custom fields.</span></span> <span data-ttu-id="f4b7f-105">Ohje käsittelee seuraavia aiheita:</span><span class="sxs-lookup"><span data-stu-id="f4b7f-105">The following topics are covered:</span></span>

- <span data-ttu-id="f4b7f-106">Eri tietotyypit, joita mukautettu kenttäkehys tukee</span><span class="sxs-lookup"><span data-stu-id="f4b7f-106">The various data types that the custom field framework supports</span></span>
- <span data-ttu-id="f4b7f-107">Miten näytetään luku- tai muokattavat kentät työaikaraportin merkinnöissä ja tallennetaan käyttäjän antamat arvot takaisin tietokantaan</span><span class="sxs-lookup"><span data-stu-id="f4b7f-107">How to show read-only or editable fields on timesheet entries, and save user-provided values back to the database</span></span>
- <span data-ttu-id="f4b7f-108">Vain luku -kenttien näyttäminen työaikaraportin otsikossa</span><span class="sxs-lookup"><span data-stu-id="f4b7f-108">How to show read-only fields on the timesheet header</span></span>
- <span data-ttu-id="f4b7f-109">Muun mukautetun liiketoimintalogiikan integroiminen oletusarvojen syöttämiseen kenttiin ja lisätarkistuksen tekemiseksi</span><span class="sxs-lookup"><span data-stu-id="f4b7f-109">How to integrate other custom business logic to enter default values in fields and do additional validation</span></span>

## <a name="audience"></a><span data-ttu-id="f4b7f-110">Yleisö</span><span class="sxs-lookup"><span data-stu-id="f4b7f-110">Audience</span></span>

<span data-ttu-id="f4b7f-111">Tämä ohjeaihe on tarkoitettu kehittäjille, jotka ovat integroimassa mukautettuja kenttiä Microsoft Dynamics 365 Project Timesheet -mobiilisovelluksen piiriin, joka on saatavilla Apple iOS:lle ja Google Androidille.</span><span class="sxs-lookup"><span data-stu-id="f4b7f-111">This topic is intended for developers who are integrating their custom fields into the Microsoft Dynamics 365 Project Timesheet mobile application that is available for Apple iOS and Google Android.</span></span> <span data-ttu-id="f4b7f-112">Oletuksena on, että lukijat tuntevat X++-kehitystyön ja projektin työaikaraportin toiminnot.</span><span class="sxs-lookup"><span data-stu-id="f4b7f-112">The assumption is that readers are familiar with X++ development and project timesheet functionality.</span></span>

## <a name="data-contract--tstimesheetcustomfield-x-class"></a><span data-ttu-id="f4b7f-113">Tietosopimus – TSTimesheetCustomField X++-luokka</span><span class="sxs-lookup"><span data-stu-id="f4b7f-113">Data contract – TSTimesheetCustomField X++ class</span></span>

<span data-ttu-id="f4b7f-114">**TSTimesheetCustomField** -luokka on X++-tietosopimusluokka, joka vastaa työaikaraportin toiminnon mukautettua kenttää koskevia tietoja.</span><span class="sxs-lookup"><span data-stu-id="f4b7f-114">The **TSTimesheetCustomField** class is the X++ data contract class that represents information about a custom field for timesheet functionality.</span></span> <span data-ttu-id="f4b7f-115">Mukautettujen kenttäobjektien luettelot välitetään sekä TSTimesheetDetails-tietosopimuksessa että TSTimesheetEntry-tietosopimuksessa, jolloin mobiilisovelluksen mukautetut kentät näkyvät.</span><span class="sxs-lookup"><span data-stu-id="f4b7f-115">Lists of the custom field objects are passed on both the TSTimesheetDetails data contract and the TSTimesheetEntry data contract to show custom fields in the mobile app.</span></span>

- <span data-ttu-id="f4b7f-116">**TSTimesheetDetails** - Työaikaraportin otsikkosopimus.</span><span class="sxs-lookup"><span data-stu-id="f4b7f-116">**TSTimesheetDetails** - The timesheet header contract.</span></span>
- <span data-ttu-id="f4b7f-117">**TSTimesheetEntry** - Työaikaraportin tapahtumasopimus.</span><span class="sxs-lookup"><span data-stu-id="f4b7f-117">**TSTimesheetEntry** - The timesheet transaction contract.</span></span> <span data-ttu-id="f4b7f-118">Näiden objektien ryhmät, joilla on samat projektitiedot ja **timesheetLineRecId**-arvo, muodostavat rivin.</span><span class="sxs-lookup"><span data-stu-id="f4b7f-118">Groups of these objects that have the same project information and **timesheetLineRecId** value constitute a line.</span></span>

### <a name="fieldbasetype-types"></a><span data-ttu-id="f4b7f-119">fieldBaseType (Tyypit)</span><span class="sxs-lookup"><span data-stu-id="f4b7f-119">fieldBaseType (Types)</span></span>

<span data-ttu-id="f4b7f-120">**FieldBaseType**-objektin **TsTimesheetCustom**-ominaisuus määrittää sovelluksessa näkyvän kentän tyypin.</span><span class="sxs-lookup"><span data-stu-id="f4b7f-120">The **FieldBaseType** property on the **TsTimesheetCustom** object determines the type of the field that appears in the app.</span></span> <span data-ttu-id="f4b7f-121">Seuraavia **tyyppi**arvoja tuetaan.</span><span class="sxs-lookup"><span data-stu-id="f4b7f-121">The following **Types** values that are supported.</span></span>

| <span data-ttu-id="f4b7f-122">Tyypin arvo</span><span class="sxs-lookup"><span data-stu-id="f4b7f-122">Types value</span></span> | <span data-ttu-id="f4b7f-123">Laji</span><span class="sxs-lookup"><span data-stu-id="f4b7f-123">Type</span></span>              | <span data-ttu-id="f4b7f-124">Muistiinpanot</span><span class="sxs-lookup"><span data-stu-id="f4b7f-124">Notes</span></span> |
|-------------|-------------------|-------|
| <span data-ttu-id="f4b7f-125">0</span><span class="sxs-lookup"><span data-stu-id="f4b7f-125">0</span></span>           | <span data-ttu-id="f4b7f-126">Merkkijono (ja Enum)</span><span class="sxs-lookup"><span data-stu-id="f4b7f-126">String (and Enum)</span></span> | <span data-ttu-id="f4b7f-127">Kenttä näkyy tekstikenttänä.</span><span class="sxs-lookup"><span data-stu-id="f4b7f-127">The field appears as a text field.</span></span> |
| <span data-ttu-id="f4b7f-128">1</span><span class="sxs-lookup"><span data-stu-id="f4b7f-128">1</span></span>           | <span data-ttu-id="f4b7f-129">Kokonaisluku</span><span class="sxs-lookup"><span data-stu-id="f4b7f-129">Integer</span></span>           | <span data-ttu-id="f4b7f-130">Arvo näkyy lukuna ilman desimaalipaikkoja.</span><span class="sxs-lookup"><span data-stu-id="f4b7f-130">The value is shown as a number without decimal places.</span></span> |
| <span data-ttu-id="f4b7f-131">2</span><span class="sxs-lookup"><span data-stu-id="f4b7f-131">2</span></span>           | <span data-ttu-id="f4b7f-132">Reaaliluku</span><span class="sxs-lookup"><span data-stu-id="f4b7f-132">Real</span></span>              | <span data-ttu-id="f4b7f-133">Arvo näkyy lukuna, jolla on desimaalipaikkoja.</span><span class="sxs-lookup"><span data-stu-id="f4b7f-133">The value is shown as a number that has decimal places.</span></span><p><span data-ttu-id="f4b7f-134">Jos haluat, että todellinen arvo näkyy sovelluksessa valuuttana, käytä **fieldExtenededType**-ominaisuutta.</span><span class="sxs-lookup"><span data-stu-id="f4b7f-134">To show the real value as a currency in the app, use the **fieldExtenededType** property.</span></span> <span data-ttu-id="f4b7f-135">**numberOfDecimals**-ominaisuuden avulla voit määrittää näytettävien desimaalien määrän.</span><span class="sxs-lookup"><span data-stu-id="f4b7f-135">You can use the **numberOfDecimals** property to set the number of decimal places that are shown.</span></span></p> |
| <span data-ttu-id="f4b7f-136">3</span><span class="sxs-lookup"><span data-stu-id="f4b7f-136">3</span></span>           | <span data-ttu-id="f4b7f-137">Päivämäärä</span><span class="sxs-lookup"><span data-stu-id="f4b7f-137">Date</span></span>              | <span data-ttu-id="f4b7f-138">Päivämäärämuodot määräytyvät käyttäjän **päivämäärä, kellonajan ja numeromuodon** asetuksella , joka on määritetty kohdassa **Kieli- ja maa-/alue** -asetukset kohdassa **Käyttäjäasetukset**.</span><span class="sxs-lookup"><span data-stu-id="f4b7f-138">Date formats are determined by the user's **Date, times, and number format** setting that is specified under **Language and country/region preference** in **User options**.</span></span> |
| <span data-ttu-id="f4b7f-139">4</span><span class="sxs-lookup"><span data-stu-id="f4b7f-139">4</span></span>           | <span data-ttu-id="f4b7f-140">Boolen arvo</span><span class="sxs-lookup"><span data-stu-id="f4b7f-140">Boolean</span></span>           | |
| <span data-ttu-id="f4b7f-141">15</span><span class="sxs-lookup"><span data-stu-id="f4b7f-141">15</span></span>          | <span data-ttu-id="f4b7f-142">GUID</span><span class="sxs-lookup"><span data-stu-id="f4b7f-142">GUID</span></span>              | |
| <span data-ttu-id="f4b7f-143">16</span><span class="sxs-lookup"><span data-stu-id="f4b7f-143">16</span></span>          | <span data-ttu-id="f4b7f-144">Int64</span><span class="sxs-lookup"><span data-stu-id="f4b7f-144">Int64</span></span>             | |

- <span data-ttu-id="f4b7f-145">Jos **TSTimesheetCustomField**-objektissa ei ole **stringOptions**-ominaisuutta, käyttäjälle annetaan vapaamuotoinen tekstikenttä.</span><span class="sxs-lookup"><span data-stu-id="f4b7f-145">If the **stringOptions** property isn't provided on the **TSTimesheetCustomField** object, a free-text field is provided to the user.</span></span>

    <span data-ttu-id="f4b7f-146">**Stringlength**-ominaisuudella voidaan määrittää suurin sallittu merkkijonon pituus, jonka käyttäjät voivat kirjoittaa.</span><span class="sxs-lookup"><span data-stu-id="f4b7f-146">The **stringLength** property can be used to set the maximum string length that users can enter.</span></span>

- <span data-ttu-id="f4b7f-147">Jos **TSTimesheetCustomField**-objektissa on **stringOptions**-ominaisuus, nämä luetteloelementit ovat ainoat arvot, joita käyttäjät voivat valita valintapainikkeiden avulla.</span><span class="sxs-lookup"><span data-stu-id="f4b7f-147">If the **stringOptions** property is provided on the **TSTimesheetCustomField** object, those list elements are the only values that users can select by using option buttons (radio buttons).</span></span>

    <span data-ttu-id="f4b7f-148">Tässä tapauksessa merkkijonokenttä voi toimia Enum-arvona käyttäjämerkintää varten.</span><span class="sxs-lookup"><span data-stu-id="f4b7f-148">In this case, the string field can act as an enum value for the purpose of user entry.</span></span> <span data-ttu-id="f4b7f-149">Jos haluat tallentaa arvon tietokantaan luetteloluetteloksi, määritä merkkijonon arvo manuaalisesti takaisin Enum-arvoksi ennen tallennusta tietokantaan käyttämällä komentoketjua (Katso "Käytä komentoketjua TSTimesheetEntryService-luokassa, kun haluat tallentaa tuntilomake merkinnän sovelluksesta takaisin tietokantaan"-osassa, joka on jäljempänä tässä esimerkissä).</span><span class="sxs-lookup"><span data-stu-id="f4b7f-149">To save the value to the database as an enum, manually map the string value back to the enum value before you save to the database by using chain of command (see the “Use chain of command on the TSTimesheetEntryService class to save a timesheet entry from the app back to the database” section later in this topic for an example).</span></span>

### <a name="fieldextendedtype-tscustomfieldextendedtype"></a><span data-ttu-id="f4b7f-150">fieldExtendedType (TSCustomFieldExtendedType)</span><span class="sxs-lookup"><span data-stu-id="f4b7f-150">fieldExtendedType (TSCustomFieldExtendedType)</span></span>

<span data-ttu-id="f4b7f-151">Tämän ominaisuuden avulla voit muotoilla todellisia arvoja valuutoiksi.</span><span class="sxs-lookup"><span data-stu-id="f4b7f-151">You can use this property to format real values as currency.</span></span> <span data-ttu-id="f4b7f-152">Tämä menetelmä on käytettävissä vain, kun **fieldBaseType**-arvo on **reaaliluku**.</span><span class="sxs-lookup"><span data-stu-id="f4b7f-152">This approach is applicable only when the **fieldBaseType** value is **Real**.</span></span>

- <span data-ttu-id="f4b7f-153">**TSCustomFieldExtendedType:None** – Muotoilua ei käytetä.</span><span class="sxs-lookup"><span data-stu-id="f4b7f-153">**TSCustomFieldExtendedType:None** – No formatting is applied.</span></span>
- <span data-ttu-id="f4b7f-154">**TSCustomFieldExtendedType::Valuutta** – Muotoile arvo valuuttana.</span><span class="sxs-lookup"><span data-stu-id="f4b7f-154">**TSCustomFieldExtendedType::Currency** – Format the value as currency.</span></span>

    <span data-ttu-id="f4b7f-155">Kun valuuttamuotoilu on käytössä, voit käyttää **stringValue**-kenttää ja siirtääksesi valuuttakoodin, joka näytetään sovelluksessa.</span><span class="sxs-lookup"><span data-stu-id="f4b7f-155">When currency formatting is active, the **stringValue** field can be used pass the currency code that should be shown in the app.</span></span> <span data-ttu-id="f4b7f-156">Arvo on vain luku -arvo.</span><span class="sxs-lookup"><span data-stu-id="f4b7f-156">The value is a read-only value.</span></span>

    <span data-ttu-id="f4b7f-157">**realValue**-kenttä sisältää rahamäärän, joka on tallennettava tietokantaan.</span><span class="sxs-lookup"><span data-stu-id="f4b7f-157">The **realValue** field contains the money amount that should be saved to the database.</span></span>

### <a name="fieldsection-tscustomfieldsection"></a><span data-ttu-id="f4b7f-158">fieldSection (TSCustomFieldSection)</span><span class="sxs-lookup"><span data-stu-id="f4b7f-158">fieldSection (TSCustomFieldSection)</span></span>

<span data-ttu-id="f4b7f-159">Tämän ominaisuuden avulla voit määrittää, missä sovelluksessa mukautetun kentän pitäisi näkyä.</span><span class="sxs-lookup"><span data-stu-id="f4b7f-159">You can use this property specify where the custom field should appear in the app.</span></span>

- <span data-ttu-id="f4b7f-160">**TSCustomFieldSection::Otsikko** – Kenttä näkyy sovelluksen **Katso lisätietoja** -osassa.</span><span class="sxs-lookup"><span data-stu-id="f4b7f-160">**TSCustomFieldSection::Header** – The field will appear in the **View more details** section in the app.</span></span> <span data-ttu-id="f4b7f-161">Nämä kentät ovat aina vain luku -muotoisia.</span><span class="sxs-lookup"><span data-stu-id="f4b7f-161">These fields are always read-only.</span></span>
- <span data-ttu-id="f4b7f-162">**TSCustomFieldSection::Tivi** – Kenttä tulee näkyviin, kun kaikki valmiiksi määritetyt rivikentät ovat aikaraporttikentissä.</span><span class="sxs-lookup"><span data-stu-id="f4b7f-162">**TSCustomFieldSection::Line** – The field will appear after all the out-of-box line fields on timesheet entries.</span></span> <span data-ttu-id="f4b7f-163">Nämä kentät voivat olla joko muokattavia tai vain luku -muotoisia.</span><span class="sxs-lookup"><span data-stu-id="f4b7f-163">These fields can be either editable or read-only.</span></span>

### <a name="fieldname-fieldnameshort"></a><span data-ttu-id="f4b7f-164">fieldName (FieldNameShort)</span><span class="sxs-lookup"><span data-stu-id="f4b7f-164">fieldName (FieldNameShort)</span></span>

<span data-ttu-id="f4b7f-165">Tämä ominaisuus määrittää kentän, kun sovelluksen luomat arvot tallennetaan takaisin tietokantaan.</span><span class="sxs-lookup"><span data-stu-id="f4b7f-165">This property identifies the field when values that the app provides are saved back to the database.</span></span>

### <a name="tablename-tablenameshort"></a><span data-ttu-id="f4b7f-166">tableName (TableNameShort)</span><span class="sxs-lookup"><span data-stu-id="f4b7f-166">tableName (TableNameShort)</span></span>

<span data-ttu-id="f4b7f-167">Tämä ominaisuus määrittää kentän, kun sovelluksen luomat arvot tallennetaan takaisin tietokantaan.</span><span class="sxs-lookup"><span data-stu-id="f4b7f-167">This property identifies the field when values that the app provides are saved back to the database.</span></span>

### <a name="iseditable-noyes"></a><span data-ttu-id="f4b7f-168">isEditable (NoYes)</span><span class="sxs-lookup"><span data-stu-id="f4b7f-168">isEditable (NoYes)</span></span>

<span data-ttu-id="f4b7f-169">Määrittämällä tämän ominaisuuden arvoksi **Kyllä** voit määrittää, että käyttäjät voivat muokata tuntilomakkeen merkintäosan kenttää.</span><span class="sxs-lookup"><span data-stu-id="f4b7f-169">Set this property to **Yes** to specify that the field in the timesheet entry section should be editable by users.</span></span> <span data-ttu-id="f4b7f-170">Määritä ominaisuuden arvoksi **Ei**, jos haluat tehdä kentästä vain luku -muotoisen.</span><span class="sxs-lookup"><span data-stu-id="f4b7f-170">Set the property to **No** to make the field read-only.</span></span>

### <a name="ismandatory-noyes"></a><span data-ttu-id="f4b7f-171">isMandatory (NoYes)</span><span class="sxs-lookup"><span data-stu-id="f4b7f-171">isMandatory (NoYes)</span></span>

<span data-ttu-id="f4b7f-172">Määrittämällä tämän ominaisuuden arvoksi **Kyllä** voit määrittää, että tuntilomakkeen merkintäosan kentän tulisi olla pakollinen.</span><span class="sxs-lookup"><span data-stu-id="f4b7f-172">Set this property to **Yes** to specify that the field in the timesheet entry section should be mandatory.</span></span>

### <a name="label-str"></a><span data-ttu-id="f4b7f-173">label (str)</span><span class="sxs-lookup"><span data-stu-id="f4b7f-173">label (str)</span></span>

<span data-ttu-id="f4b7f-174">Tämä ominaisuus määrittää otsikon, joka näkyy sovelluksen kentän vieressä.</span><span class="sxs-lookup"><span data-stu-id="f4b7f-174">This property specifies the label that is shown next the field in the app.</span></span>

### <a name="stringoptions-list-of-strings"></a><span data-ttu-id="f4b7f-175">stringOptions (merkkijonojen luettelo)</span><span class="sxs-lookup"><span data-stu-id="f4b7f-175">stringOptions (List of Strings)</span></span>

<span data-ttu-id="f4b7f-176">Tämä ominaisuus on käytettävissä vain, kun **fieldbasetype** -arvo on **Merkkijono**.</span><span class="sxs-lookup"><span data-stu-id="f4b7f-176">This property is applicable only when **fieldBaseType** is set to **String**.</span></span> <span data-ttu-id="f4b7f-177">Jos **stringOptions** on määritetty, valintapainikkeiden kautta valittavissa olevat merkkijonoarvot (Radiopainikkeet) määritetään luettelon merkkijonojen avulla.</span><span class="sxs-lookup"><span data-stu-id="f4b7f-177">If **stringOptions** is set, the string values that are available for selection via option buttons (radio buttons) are specified by the strings in the list.</span></span> <span data-ttu-id="f4b7f-178">Jos merkkijonoja ei anneta, merkkijonokentän vapaatekstin syöttö on sallittu (esimerkin löydät kohdassa "komentoketjun käyttäminen Tstimessheedistryservice-luokassa, jolloin tuntilomakekohta tallennetaan sovelluksesta tietokantaan uudelleen" -osassa myöhemmin tässä aiheessa).</span><span class="sxs-lookup"><span data-stu-id="f4b7f-178">If no strings are provided, free-text entry in the string field is allowed (see the “Use chain of command on the TSTimesheetEntryService class to save a timesheet entry from the app back to the database” section later in this topic for an example).</span></span>

### <a name="stringlength-int"></a><span data-ttu-id="f4b7f-179">stringLength (int)</span><span class="sxs-lookup"><span data-stu-id="f4b7f-179">stringLength (int)</span></span>

<span data-ttu-id="f4b7f-180">Tämä ominaisuus määrittää merkkijonokentän enimmäispituuden.</span><span class="sxs-lookup"><span data-stu-id="f4b7f-180">This property specifies the maximum length for a string field.</span></span> <span data-ttu-id="f4b7f-181">Se on käytettävissä vain, kun **fieldBaseType**-arvo on **Merkkijono**.</span><span class="sxs-lookup"><span data-stu-id="f4b7f-181">It's applicable only when **fieldBaseType** is set to **String**.</span></span>

### <a name="numberofdecimals-int"></a><span data-ttu-id="f4b7f-182">numberOfDecimals (int)</span><span class="sxs-lookup"><span data-stu-id="f4b7f-182">numberOfDecimals (int)</span></span>

<span data-ttu-id="f4b7f-183">Tämä ominaisuus määrittää todellisen kentän desimaalipaikkojen määrän.</span><span class="sxs-lookup"><span data-stu-id="f4b7f-183">This property specifies the number of decimal places that are shown for a real field.</span></span> <span data-ttu-id="f4b7f-184">Se on käytettävissä vain, kun **fieldBaseType**-arvo on **Reaaliarvo**.</span><span class="sxs-lookup"><span data-stu-id="f4b7f-184">It's applicable only when **fieldBaseType** is set to **Real**.</span></span>

### <a name="ordersequence-int"></a><span data-ttu-id="f4b7f-185">orderSequence (int)</span><span class="sxs-lookup"><span data-stu-id="f4b7f-185">orderSequence (int)</span></span>

<span data-ttu-id="f4b7f-186">Tämä ominaisuus määrittää, missä järjestyksessä mukautetut kentät näkyvät sovelluksessa, kun määritettynä on useita mukautettuja kenttiä.</span><span class="sxs-lookup"><span data-stu-id="f4b7f-186">This property controls the order in which the custom fields are shown in the app when more than one custom field is specified.</span></span> <span data-ttu-id="f4b7f-187">Alanumeroita käyttävät kentät näytetään ensin.</span><span class="sxs-lookup"><span data-stu-id="f4b7f-187">Fields that have lower numbers are shown first.</span></span>

### <a name="booleanvalue-boolean"></a><span data-ttu-id="f4b7f-188">booleanValue (boolean)</span><span class="sxs-lookup"><span data-stu-id="f4b7f-188">booleanValue (boolean)</span></span>

<span data-ttu-id="f4b7f-189">**Boolean**-tyypin kentissä tämä ominaisuus siirtää kentän totuusarvon palvelimen ja sovelluksen välille.</span><span class="sxs-lookup"><span data-stu-id="f4b7f-189">For fields of the **Boolean** type, this property passes the Boolean value of the field between the server and the app.</span></span>

### <a name="guidvalue-guid"></a><span data-ttu-id="f4b7f-190">guidValue (guid)</span><span class="sxs-lookup"><span data-stu-id="f4b7f-190">guidValue (guid)</span></span>

<span data-ttu-id="f4b7f-191">**GUID**-tyypin kentissä tämä ominaisuus siirtää kentän yksilöivän tunnisteen palvelimen ja sovelluksen välille.</span><span class="sxs-lookup"><span data-stu-id="f4b7f-191">For fields of the **GUID** type, this property passes the globally unique identifier (GUID) value of the field between the server and the app.</span></span>

### <a name="int64value-int64"></a><span data-ttu-id="f4b7f-192">int64Value (Int64)</span><span class="sxs-lookup"><span data-stu-id="f4b7f-192">int64Value (int64)</span></span>

<span data-ttu-id="f4b7f-193">**Int64**-tyypin kentissä tämä ominaisuus siirtää kentän Int64-arvon palvelimen ja sovelluksen välille.</span><span class="sxs-lookup"><span data-stu-id="f4b7f-193">For fields of the **Int64** type, this property passes the int64 value of the field between the server and the app.</span></span>

### <a name="intvalue-int"></a><span data-ttu-id="f4b7f-194">intValue (int)</span><span class="sxs-lookup"><span data-stu-id="f4b7f-194">intValue (int)</span></span>

<span data-ttu-id="f4b7f-195">**Int**-tyypin kentissä tämä ominaisuus siirtää kentän Int-arvon palvelimen ja sovelluksen välille.</span><span class="sxs-lookup"><span data-stu-id="f4b7f-195">For fields of the **Int** type, this property passes the int value of the field between the server and the app.</span></span>

### <a name="realvalue-real"></a><span data-ttu-id="f4b7f-196">realValue (real)</span><span class="sxs-lookup"><span data-stu-id="f4b7f-196">realValue (real)</span></span>

<span data-ttu-id="f4b7f-197">**Reaaliarvo**-tyypin kentissä tämä ominaisuus siirtää kentän reaaliarvon palvelimen ja sovelluksen välille .</span><span class="sxs-lookup"><span data-stu-id="f4b7f-197">For fields of the **Real** type, this property passes the real value of the field between the server and the app .</span></span>

### <a name="stringvalue-str"></a><span data-ttu-id="f4b7f-198">stringValue (str)</span><span class="sxs-lookup"><span data-stu-id="f4b7f-198">stringValue (str)</span></span>

<span data-ttu-id="f4b7f-199">**Merkkijono**-tyypin kentissä tämä ominaisuus siirtää kentän merkkijonoarvon palvelimen ja sovelluksen välille.</span><span class="sxs-lookup"><span data-stu-id="f4b7f-199">For fields of the **String** type, this property passes the string value of the field between the server and the app.</span></span> <span data-ttu-id="f4b7f-200">Sitä käytetään myös sellaisissa kentissä, joiden **reaaliarvo** on muotoiltu valuutaksi.</span><span class="sxs-lookup"><span data-stu-id="f4b7f-200">It's also used for fields of the **Real** type that are formatted as currency.</span></span> <span data-ttu-id="f4b7f-201">Näiden kenttien osalta ominaisuutta käytetään valuuttakoodin välittämiseen sovellukseen.</span><span class="sxs-lookup"><span data-stu-id="f4b7f-201">For those fields, the property is used to pass the currency code to the app.</span></span>

### <a name="datevalue-date"></a><span data-ttu-id="f4b7f-202">dateValue (date)</span><span class="sxs-lookup"><span data-stu-id="f4b7f-202">dateValue (date)</span></span>

<span data-ttu-id="f4b7f-203">**Päivämäärä**-tyypin kentissä tämä ominaisuus siirtää kentän päivämäärän palvelimen ja sovelluksen välille.</span><span class="sxs-lookup"><span data-stu-id="f4b7f-203">For fields of the **Date** type, this property passes the date value of the field between the server and the app.</span></span>

## <a name="show-and-save-a-custom-field-in-the-timesheet-entry-section"></a><span data-ttu-id="f4b7f-204">Mukautetun kentän näyttäminen ja tallentaminen tuntilomakemerkinnän osassa</span><span class="sxs-lookup"><span data-stu-id="f4b7f-204">Show and save a custom field in the timesheet entry section</span></span>

<span data-ttu-id="f4b7f-205">Alla on näyttökuva aikaraportin merkinnän luomisesta mobiilisovelluksesta.</span><span class="sxs-lookup"><span data-stu-id="f4b7f-205">Below is a screenshot from the mobile app of a timesheet entry creation.</span></span> <span data-ttu-id="f4b7f-206">Se näyttää valmiiksi määritetyt kentät ja mukautetun kentän aikamerkintäosassa nimeltä "Testimerkkijono" ja enum-arvo "Toinen vaihtoehto" on jo asetettu.</span><span class="sxs-lookup"><span data-stu-id="f4b7f-206">It shows the out-of-box fields and a custom field in the "Time entry" section called "Test string" with an enum value of "Second option" already set.</span></span>

![Testimerkkijonon mukautettu kenttä sovelluksessa](media/timesheet-entry.jpg)



<span data-ttu-id="f4b7f-208">Alla on kuvakaappaus käyttäjän mobiilisovelluksesta, jossa valitaan jokin käytettävissä olevista enum-asetuksista Testimerkkijono-kohtaan.</span><span class="sxs-lookup"><span data-stu-id="f4b7f-208">Below is a screenshot from the mobile app of the user selecting one of the enum options available for the "Test string" custom field.</span></span>  <span data-ttu-id="f4b7f-209">Kaksi vaihtoehtoa ovat "ensimmäinen vaihtoehto" ja "toinen vaihtoehto", jotka näkyvät valintapainikkeina.</span><span class="sxs-lookup"><span data-stu-id="f4b7f-209">The two options are "First option" and "Second option" shown as radio buttons.</span></span> <span data-ttu-id="f4b7f-210">Toinen vaihtoehto on valittuna.</span><span class="sxs-lookup"><span data-stu-id="f4b7f-210">The second option is currently selected.</span></span>

![Testimerkkijonon mukautetun kentän valintapainikkeita (valintanappeja)](media/enum-option.jpg)



### <a name="extend-the-tstimesheetline-table-so-that-it-has-a-custom-field"></a><span data-ttu-id="f4b7f-212">Laajenna TSTimesheetLine-taulukkoa niin, että siinä on mukautettu kenttä</span><span class="sxs-lookup"><span data-stu-id="f4b7f-212">Extend the TSTimesheetLine table so that it has a custom field</span></span>

<span data-ttu-id="f4b7f-213">Tyypillisissä skenaarioissa on todennäköistä, että tuntilomakemerkinnän mukautetun kentän tiedot tallennetaan TSTimesheetLine-tauluun.</span><span class="sxs-lookup"><span data-stu-id="f4b7f-213">In typical scenarios, it's likely that the data for a custom field in the timesheet entry section will be saved to the TSTimesheetLine table.</span></span> <span data-ttu-id="f4b7f-214">Muita tauluja voidaan kuitenkin käyttää, jos tiedot voidaan noutaa annetun TSTimesheetTrans-tietueen perusteella tai jos niillä ei ole tiettyä tietuetaustaa (Jos esimerkiksi kenttä on määritetty vain luku -tilaan projektin parametreissä).</span><span class="sxs-lookup"><span data-stu-id="f4b7f-214">However, other tables can be used if the data can be retrieved based on a TSTimesheetTrans record that is provided, or if it doesn't have specific record context (for example, if the field is set as read-only in the project parameters).</span></span>

<span data-ttu-id="f4b7f-215">Huomaa, että mukautettujen kenttien ei tarvitse sisältää tietokantatietuetta.</span><span class="sxs-lookup"><span data-stu-id="f4b7f-215">Note that custom fields don't have to have any backing database records.</span></span> <span data-ttu-id="f4b7f-216">Ne voidaan luoda dynaamisesti X++-logiikan perusteella.</span><span class="sxs-lookup"><span data-stu-id="f4b7f-216">They can be dynamically generated based on X++ logic.</span></span> <span data-ttu-id="f4b7f-217">Tämä lähestymistapa voi olla hyödyllinen vain luku -tilassa olevissa skenaarioissa (lisätietoja on kohdassa "komentoketjun käyttäminen TSTimesheetDetails-luokassa, buildCustomFieldListForHeader-menetelmä, joka täyttää tuntilomakkeen tiedot" -osassa, jossa on esimerkki dynaamisesti tuotetuista mukautetuista kenttäarvoista.)</span><span class="sxs-lookup"><span data-stu-id="f4b7f-217">This approach can be useful in read-only scenarios (see the “Use chain of command on the TSTimesheetDetails class, buildCustomFieldListForHeader method to fill in timesheet details” section for an example of dynamically generated custom field values.)</span></span>

<span data-ttu-id="f4b7f-218">Alla on kuvakaappaus Visual Studion sovellusobjektipuusta.</span><span class="sxs-lookup"><span data-stu-id="f4b7f-218">Below is a screenshot from Visual Studio of the Application Object Tree.</span></span> <span data-ttu-id="f4b7f-219">Siinä näkyy TSTimesheetLine-taulun laajennus ja TestLineString-kenttä on lisätty mukautetuksi kentäksi.</span><span class="sxs-lookup"><span data-stu-id="f4b7f-219">It shows an extension of the TSTimesheetLine table with the TestLineString field added as a custom field.</span></span>

![Merkkijono](media/b6756b4a3fc5298093327a088a7710fd.png)

### <a name="use-chain-of-command-on-the-buildcustomfieldlist-method-of-the-tstimesheetsettings-class-to-show-a-field-in-the-timesheet-entry-section"></a><span data-ttu-id="f4b7f-221">Käytä komentoketjua TSTimesheetSettings-luokan buildCustomFieldList-menetelmässä, kun haluat näyttää kentän tuntilomakemerkinnän osassa.</span><span class="sxs-lookup"><span data-stu-id="f4b7f-221">Use chain of command on the buildCustomFieldList method of the TSTimesheetSettings class to show a field in the timesheet entry section</span></span>

<span data-ttu-id="f4b7f-222">Tämä koodi ohjaa sovelluksen kentän näyttöasetuksia.</span><span class="sxs-lookup"><span data-stu-id="f4b7f-222">This code controls the display settings for the field in the app.</span></span> <span data-ttu-id="f4b7f-223">Se määrittää esimerkiksi kentän tyypin, otsikon, sen, onko kenttä pakollinen, ja missä osassa kenttä näkyy.</span><span class="sxs-lookup"><span data-stu-id="f4b7f-223">For example, it controls the type of field, the label, whether the field is mandatory, and what section the field appears in.</span></span>

<span data-ttu-id="f4b7f-224">Seuraavassa esimerkissä näkyy aikamerkintöjen merkkijonokenttä.</span><span class="sxs-lookup"><span data-stu-id="f4b7f-224">The following example shows a string field on time entries.</span></span> <span data-ttu-id="f4b7f-225">Tässä kentässä on kaksi vaihtoehtoa **Ensimmäinen vaihtoehto** ja **Toinen vaihtoehto**, jotka ovat käytettävissä valintapainikkeiden kautta (valintanapit).</span><span class="sxs-lookup"><span data-stu-id="f4b7f-225">This field has two options, **First option** and **Second option**, that are available via option buttons (radio buttons).</span></span> <span data-ttu-id="f4b7f-226">Sovelluksen kenttä liitetään **TestLineString**-kenttään, joka lisätään TSTimesheetLine-tauluun.</span><span class="sxs-lookup"><span data-stu-id="f4b7f-226">The field in the app is associated with the **TestLineString** field that is added to the TSTimesheetLine table.</span></span>

<span data-ttu-id="f4b7f-227">Huomaa **TSTimesheetCustomField::newFromMetatdata()**-menetelmän käyttäminen mukautettujen kenttien ominaisuuksien alustamisen yksinkertaistamiseksi: **fieldBaseType**, **tableName**, **fieldname**, **label**, **isEditable**, **isMandatory**, **stringLength** ja **numberOfDecimals**.</span><span class="sxs-lookup"><span data-stu-id="f4b7f-227">Note the use of the **TSTimesheetCustomField::newFromMetatdata()** method to simplify the initialization of the custom field properties: **fieldBaseType**, **tableName**, **fieldname**, **label**, **isEditable**, **isMandatory**, **stringLength**, and **numberOfDecimals**.</span></span> <span data-ttu-id="f4b7f-228">Voit myös määrittää nämä parametrit manuaalisesti kuten haluat.</span><span class="sxs-lookup"><span data-stu-id="f4b7f-228">You can also set these parameters manually, as you prefer.</span></span>

```
...
[ExtensionOf(classStr(TsTimesheetSettings))]
final class TSTimesheetSettings_Extension
{
    protected List buildCustomFieldList()
    {
        List customFieldList = next buildCustomFieldList();
        TSTimesheetCustomField tsTimesheetCustomField;
        tsTimesheetCustomField =
        TSTimesheetCustomField::newFromMetadata(tableNum(TsTimesheetLine),
        fieldNum(TSTimesheetLine, TestLineString));
        tsTimesheetCustomField.parmFieldSection(TSCustomFieldSection::Line);
        tsTimesheetCustomField.parmOrderSequence(1);
        List stringOptions = new List(Types::String);
        stringOptions.addEnd('First option');
        stringOptions.addEnd('Second option');
        tsTimesheetCustomField.parmStringOptions(stringOptions);
        customFieldList.addEnd(tsTimesheetCustomField);
        return customFieldList;
    }
}
...
```

### <a name="use-chain-of-command-on-the-buildcustomfieldlistforentry-method-of-the-tstimesheetentry-class-to-enter-values-in-a-timesheet-entry"></a><span data-ttu-id="f4b7f-229">Käytä komentoketjua TSTimesheetEntry-luokan buildCustomFieldListForEntry-menetelmässä, kun haluat syöttää arvoja tuntilomakkeeseen</span><span class="sxs-lookup"><span data-stu-id="f4b7f-229">Use chain of command on the buildCustomFieldListForEntry method of the TSTimesheetEntry class to enter values in a timesheet entry</span></span>

<span data-ttu-id="f4b7f-230">**buildCustomFieldListForEntry**-menetelmällä syötetään arvoja mobiilisovellukseen tallennettujen työaikaraporttien riveille.</span><span class="sxs-lookup"><span data-stu-id="f4b7f-230">The **buildCustomFieldListForEntry** method is used to enter values on the saved timesheet lines in the mobile app.</span></span> <span data-ttu-id="f4b7f-231">Se ottaa TSTimesheetTrans-tietueen parametriksi.</span><span class="sxs-lookup"><span data-stu-id="f4b7f-231">It takes a TSTimesheetTrans record as a parameter.</span></span> <span data-ttu-id="f4b7f-232">Tietueen kenttiä voidaan käyttää sovelluksen mukautetun kentän arvon täyttämiseen.</span><span class="sxs-lookup"><span data-stu-id="f4b7f-232">Fields from that record can be used to fill in the custom field value in the app.</span></span>

```
...
[ExtensionOf(classStr(TsTimesheetEntry))]
final class TsTimesheetEntry_Extension
{
    protected List buildCustomFieldListForEntry(TSTimesheetTrans _tsTimesheetTrans)
    {
        List customFieldList = next buildCustomFieldListForEntry(_tsTimesheetTrans);
        TSTimesheetLine tsTimesheetLine = _tsTimesheetTrans.timesheetLine();
        TSTimesheetCustomField tsTimesheetCustomField;
        tsTimesheetCustomField =
        TSTimesheetCustomField::newFromMetadata(tableNum(TsTimesheetLine),
        fieldNum(TSTimesheetLine, TestLineString));
        tsTimesheetCustomField.parmFieldSection(TSCustomFieldSection::Line);
        tsTimesheetCustomField.parmOrderSequence(1);
        tsTimesheetCustomField.parmStringValue(tsTimesheetLine.TestLineString);
        List stringOptions = new List(Types::String);
        stringOptions.addEnd('First option');
        stringOptions.addEnd('second option;);
        tsTimesheetCustomField.parmStringOptions(stringOptions);
        customFieldList.addEnd(tsTimesheetCustomField);
        return customFieldList;
    }
}
...
```

### <a name="use-chain-of-command-on-the-tstimesheetentryservice-class-to-save-a-timesheet-entry-from-the-app-back-to-the-database"></a><span data-ttu-id="f4b7f-233">Käyttämällä TSTimesheetEntryService-luokan komentoketjua voit tallentaa tuntilomakemerkinnän sovelluksesta takaisin tietokantaan.</span><span class="sxs-lookup"><span data-stu-id="f4b7f-233">Use chain of command on the TSTimesheetEntryService class to save a timesheet entry from the app back to the database</span></span>

<span data-ttu-id="f4b7f-234">Jos haluat tallentaa mukautetun kentän takaisin tietokantaan tyypillisessä käytössä, sinun on laajennettava useita menetelmiä:</span><span class="sxs-lookup"><span data-stu-id="f4b7f-234">To save a custom field back to the database in typical usage, you must extend multiple methods:</span></span>

- <span data-ttu-id="f4b7f-235">**timesheetLineNeedsUpdating**-menetelmän avulla määritetään, onko käyttäjä muuttanut rivitietuetta sovelluksessa ja pitääkö se tallentaa tietokantaan.</span><span class="sxs-lookup"><span data-stu-id="f4b7f-235">The **timesheetLineNeedsUpdating** method is used to determine whether the line record has been changed by the user in the app and must be saved to the database.</span></span> <span data-ttu-id="f4b7f-236">Jos suorituskyky ei ole ongelma, tätä menetelmää voidaan yksinkertaistaa niin, että se palauttaa aina arvon **Tosi**.</span><span class="sxs-lookup"><span data-stu-id="f4b7f-236">If performance isn't a concern, this method can be simplified so that it always returns **true**.</span></span>
- <span data-ttu-id="f4b7f-237">**populateTimesheetLineFromEntryDuringCreate**- ja **populateTimesheetLineFromEntryDuringUpdate** -menetelmiä voidaan jatkaa siten, että ne syöttävät arvot TSTimesheetLine-tietokantatietueeseen TSTimesheetEntry-tietueesta annetusta tietosopimustietueesta.</span><span class="sxs-lookup"><span data-stu-id="f4b7f-237">The **populateTimesheetLineFromEntryDuringCreate** and **populateTimesheetLineFromEntryDuringUpdate** methods can be extended so that they enter values in the TSTimesheetLine database record from the TSTimesheetEntry data contract record that is provided.</span></span> <span data-ttu-id="f4b7f-238">Seuraavassa esimerkissä ilmoitetaan, miten tietokantakentän ja syöttökentän välinen vastaavuus tehdään manuaalisesti X++-koodin avulla.</span><span class="sxs-lookup"><span data-stu-id="f4b7f-238">In the example that follows, notice how the mapping between the database field and the entry field is manually done via X++ code.</span></span>
- <span data-ttu-id="f4b7f-239">**populateTimesheetWeekFromEntry**-menetelmää voidaan myös jatkaa, jos **TSTimesheetEntry**-objektiin yhdistettävän mukautetun kentän on kirjoitettava takaisin TSTimesheetLineweek-tietokantatauluun.</span><span class="sxs-lookup"><span data-stu-id="f4b7f-239">The **populateTimesheetWeekFromEntry** method can also be extended if the custom field that is mapped to the **TSTimesheetEntry** object must write back to the TSTimesheetLineweek database table.</span></span>

> [!NOTE]
> <span data-ttu-id="f4b7f-240">Seuraavassa esimerkissä tallennetaan **firstOption**- tai **secondOption**-arvo, jonka käyttäjä valitsee tietokantaan raakamerkkijonoarvona.</span><span class="sxs-lookup"><span data-stu-id="f4b7f-240">The following example saves the **firstOption** or **secondOption** value that the user selects to the database as a raw string value.</span></span> <span data-ttu-id="f4b7f-241">Jos tietokantakenttä on **Enum**-tyypin kenttä, arvot voidaan määrittää manuaalisesti Enum-arvoksi ja tallentaa sitten tietokantataulun Enum-kenttään.</span><span class="sxs-lookup"><span data-stu-id="f4b7f-241">If the database field is a field of the **Enum** type, those values can be manually mapped to an enum value and then saved to an enum field on the database table.</span></span>

```
...
[ExtensionOf(classStr(TSTimesheetEntryService))]
final class TSTimesheetEntryService_Extension
{
    protected boolean timesheetLineNeedsUpdating(TSTimesheetLine _tsTimesheetLine,
    TsTimesheetEntry _tsTimesheetEntry)
    {
        boolean ret = next timesheetLineNeedsUpdating(_tsTimesheetLine,
        _tsTimesheetEntry);
        if (!ret)
        {
            */ Loop through custom fields to see if value needs updating*/
            ListEnumerator enumerator =  _tsTimesheetEntry.parmCustomFields().getEnumerator();
            while (enumerator.moveNext())
            {
                TSTimesheetCustomField customField = enumerator.current();
                if (customField.parmFieldName() == fieldId2Name(tableNum(TsTimesheetLine),
                fieldNum(TSTimesheetLine, TestLineString)))
                {
                    */ If Custom field value for TestLineString field has changed, We need to update the timesheet line.*/
                    if (_tsTimesheetLine.TestLineString != customField.parmStringValue())
                    {
                        ret = true;
                    }
                }
            }
        }
        return ret;
    }
    protected void populateTimesheetLineFromEntryDuringCreate(TSTimesheetLine
    _tsTimesheetLine, TSTimesheetEntry _tsTimesheetEntry)
    {
        next populateTimesheetLineFromEntryDuringCreate(_tsTimesheetLine,
        _tsTimesheetEntry);
        this.populateTimesheetLineFromCustomFields(_tsTimesheetLine,
        _tsTimesheetEntry);
        }
        protected void populateTimesheetLineFromEntryDuringUpdate(TSTimesheetLine
        \_tsTimesheetLine, TSTimesheetEntry _tsTimesheetEntry)
        {
            next populateTimesheetLineFromEntryDuringUpdate(_tsTimesheetLine,
            _tsTimesheetEntry);
            this.populateTimesheetLineFromCustomFields(_tsTimesheetLine,
            _tsTimesheetEntry);
        }
        private void populateTimesheetLineFromCustomFields(TSTimesheetLine
        _tsTimesheetLine, TSTimesheetEntry _tsTimesheetEntry)
        {
            ListEnumerator enumerator =
            _tsTimesheetEntry.parmCustomFields().getEnumerator();
            while (enumerator.moveNext())
            {
                TSTimesheetCustomField customField = enumerator.current();
                if (customField.parmFieldName() == fieldId2Name(tableNum(TsTimesheetLine),
                fieldNum(TSTimesheetLine, TestLineString)))
                {
                    _tsTimesheetLine.TestLineString = customField.parmStringValue();
                }
            }
        }
    }
...
```

## <a name="show-a-custom-field-in-the-timesheet-header-section"></a><span data-ttu-id="f4b7f-242">Mukautetun kentän näyttäminen tuntilomakkeen otsikossa</span><span class="sxs-lookup"><span data-stu-id="f4b7f-242">Show a custom field in the timesheet header section</span></span>

<span data-ttu-id="f4b7f-243">Alla on näyttökuva aikaraportin käyttäjän mobiilisovelluksesta, jossa näkyy käyttäjän tuntilomakenäkymä.</span><span class="sxs-lookup"><span data-stu-id="f4b7f-243">Below is a screenshot from the mobile app of a user viewing a timesheet.</span></span> <span data-ttu-id="f4b7f-244">Lisätietoja-painike on valittu oikeasta yläkulmasta, jolloin näkyviin tulee Näytä lisätiedot -vaihtoehto.</span><span class="sxs-lookup"><span data-stu-id="f4b7f-244">The "More information" button has been selected in the upper-right corner to show the "View more details" option.</span></span>  

![Näytä lisätietoja -komento](media/show-more.png)

<span data-ttu-id="f4b7f-246">Alla on näyttökuva aikaraportin käyttäjän mobiilisovelluksesta, jossa näkyy tuntilomakkeen Lisää-osa.</span><span class="sxs-lookup"><span data-stu-id="f4b7f-246">Below is a screenshot from the mobile app showing the “More” section of a timesheet.</span></span> <span data-ttu-id="f4b7f-247">Tuntilomakkeen otsikko-osaan on lisätty mukautettu kenttä, jonka nimi on Tämän tuntilomakkeen käyttöaste (laskettu mukautettu kenttä).</span><span class="sxs-lookup"><span data-stu-id="f4b7f-247">A custom field called “Utilization rate of this timesheet (computed custom field)” has been added to the timesheet header section.</span></span> <span data-ttu-id="f4b7f-248">Vain luku -arvo 0,667 on määritetty mukautettuun kenttään.</span><span class="sxs-lookup"><span data-stu-id="f4b7f-248">A read-only value of "0.667" is set on the custom field.</span></span>

![Lisää-osa](media/more-section.jpg)

### <a name="extend-the-tstimesheettable-table-so-that-it-has-a-custom-field"></a><span data-ttu-id="f4b7f-250">Laajenna TSTimesheetTable-taulukkoa niin, että siinä on mukautettu kenttä</span><span class="sxs-lookup"><span data-stu-id="f4b7f-250">Extend the TSTimesheetTable table so that it has a custom field</span></span>

<span data-ttu-id="f4b7f-251">Tyypillisissä skenaarioissa on todennäköistä, että otsikon mukautetun kentän tiedot haetaan TSTimesheetLine-taulusta.</span><span class="sxs-lookup"><span data-stu-id="f4b7f-251">In typical scenarios, it's likely that the data for a custom field in the header section will be pulled from the TSTimesheetHeader table.</span></span> <span data-ttu-id="f4b7f-252">Muita tauluja voidaan kuitenkin käyttää, jos tiedot voidaan noutaa annetun TSTimesheetTable-tietueen perusteella tai jos niillä ei ole tiettyä tietuetaustaa (Jos esimerkiksi kenttä on määritetty vain luku -tilaan projektin parametreissä).</span><span class="sxs-lookup"><span data-stu-id="f4b7f-252">However, other tables can be used if the data can be retrieved based on a TSTimesheetTable record that is provided, or if it doesn't have specific record context (for example, if the field is set as read-only in the project parameters).</span></span>

<span data-ttu-id="f4b7f-253">Huomaa, että mukautettujen kenttien ei tarvitse sisältää tietokantatietuetta.</span><span class="sxs-lookup"><span data-stu-id="f4b7f-253">Note that custom fields don't have to have any backing database records.</span></span> <span data-ttu-id="f4b7f-254">Ne voidaan luoda dynaamisesti X++-logiikan perusteella.</span><span class="sxs-lookup"><span data-stu-id="f4b7f-254">They can be dynamically generated based on X++ logic.</span></span> <span data-ttu-id="f4b7f-255">Seuraava esimerkki osoittaa tämän lähestymistavan.</span><span class="sxs-lookup"><span data-stu-id="f4b7f-255">The example that follows shows this approach.</span></span>

<span data-ttu-id="f4b7f-256">Otsikko-osan kentät ovat aina vain luku -tilassa sovelluksessa.</span><span class="sxs-lookup"><span data-stu-id="f4b7f-256">Fields in the header section are always read-only in the app.</span></span>

### <a name="use-chain-of-command-on-the-buildcustomfieldlist-method-of-the-tstimesheetsettings-class-to-show-a-field-in-the-header-section"></a><span data-ttu-id="f4b7f-257">Käytä komentoketjua TSTimesheetSettings-luokan buildCustomFieldList-menetelmässä, kun haluat näyttää kentän otsikon osassa.</span><span class="sxs-lookup"><span data-stu-id="f4b7f-257">Use chain of command on the buildCustomFieldList method of the TSTimesheetSettings class to show a field in the header section</span></span>

<span data-ttu-id="f4b7f-258">Tämä koodi ohjaa sovelluksen kentän näyttöasetuksia.</span><span class="sxs-lookup"><span data-stu-id="f4b7f-258">This code controls the display settings for the field in the app.</span></span> <span data-ttu-id="f4b7f-259">Se määrittää esimerkiksi kentän tyypin, otsikon, sen, onko kenttä pakollinen, ja missä osassa kenttä näkyy.</span><span class="sxs-lookup"><span data-stu-id="f4b7f-259">For example, it controls the type of field, the label, whether the field is mandatory, and what section the field appears in.</span></span>

<span data-ttu-id="f4b7f-260">Seuraavassa esimerkissä näkyy laskettu arvo sovelluksen otsikko-osassa.</span><span class="sxs-lookup"><span data-stu-id="f4b7f-260">The following example shows a computed value in the header section in the app.</span></span>

```
...
[ExtensionOf(classStr(TsTimesheetSettings))]
final class TSTimesheetSettings_Extension
{
    protected List buildCustomFieldList()
    {
        List customFieldList = next buildCustomFieldList();
        TSTimesheetCustomField tsTimesheetCustomField;

        */ Computed utilization rate*/
        tsTimesheetCustomField = new TSTimesheetCustomField();
        tsTimesheetCustomField.parmFieldBaseType(Types::Real);
        tsTimesheetCustomField.parmLabel("Utilization rate of this timesheet (computed
        custom field)");
        tsTimesheetCustomField.parmFieldSection(TSCustomFieldSection::Header);
        tsTimesheetCustomField.parmOrderSequence(2);
        tsTimesheetCustomField.parmNumberOfDecimals(3);
        customFieldList.addEnd(tsTimesheetCustomField);
        return customFieldList;
    }
}
...
```

### <a name="use-chain-of-command-on-the-buildcustomfieldlistforheader-method-of-the-tstimesheetdetails-class-to-fill-in-timesheet-details"></a><span data-ttu-id="f4b7f-261">Käytä komentoketjua TSTimesheetDetails-luokan buildCustomFieldListForHeader-menetelmässä, kun haluat täyttää arvoja tuntilomakkeen tietoihin</span><span class="sxs-lookup"><span data-stu-id="f4b7f-261">Use chain of command on the buildCustomFieldListForHeader method of the TSTimesheetDetails class to fill in timesheet details</span></span>

<span data-ttu-id="f4b7f-262">**buildCustomFieldListForHeader**-menetelmällä täytetään arvoja mobiilisovellukseen työaikaraporttien otsikkotietoihin.</span><span class="sxs-lookup"><span data-stu-id="f4b7f-262">The **buildCustomFieldListForHeader** method is used to fill in the timesheet header details in the mobile app.</span></span> <span data-ttu-id="f4b7f-263">Se ottaa TSTimesheetTable-tietueen parametriksi.</span><span class="sxs-lookup"><span data-stu-id="f4b7f-263">It takes a TSTimesheetTable record as a parameter.</span></span> <span data-ttu-id="f4b7f-264">Tietueen kenttiä voidaan käyttää sovelluksen mukautetun kentän arvon täyttämiseen.</span><span class="sxs-lookup"><span data-stu-id="f4b7f-264">Fields from that record can be used to fill in the custom field value in the app.</span></span> <span data-ttu-id="f4b7f-265">Seuraava esimerkki ei lue mitään tietokannan arvoja.</span><span class="sxs-lookup"><span data-stu-id="f4b7f-265">The following example doesn't read any values from the database.</span></span> <span data-ttu-id="f4b7f-266">Sen sijaan se luo X++-logiikan avulla lasketun arvon, joka näkyy sovelluksessa.</span><span class="sxs-lookup"><span data-stu-id="f4b7f-266">Instead, it uses X++ logic to generate a computed value that is then shown in the app.</span></span>


```
...
[ExtensionOf(classStr(TSTimesheetDetails))]
final class TSTimesheetDetails_Extension
{
    protected List buildCustomFieldListForHeader(TSTimesheetTable
    _tsTimesheetTable)
    {
        List customFieldList = next buildCustomFieldListForHeader(_tsTimesheetTable);
        TSTimesheetCustomField tsTimesheetCustomField;

        */ Computed utilization rate*/
        tsTimesheetCustomField = new TSTimesheetCustomField();
        tsTimesheetCustomField.parmFieldBaseType(Types::Real);
        tsTimesheetCustomField.parmLabel("Utilization rate of this timesheet (computed
        custom field)");
        tsTimesheetCustomField.parmFieldSection(TSCustomFieldSection::Header);
        tsTimesheetCustomField.parmOrderSequence(2);
        tsTimesheetCustomField.parmNumberOfDecimals(3);
        real utilizationRate = 0;
        if (_tsTimesheetTable.totalHours() != 0)
        {
            utilizationRate = _tsTimesheetTable.totalHoursBillable() /
            _tsTimesheetTable.totalHours();
        }
        tsTimesheetCustomField.parmRealValue(utilizationRate);
        customFieldList.addEnd(tsTimesheetCustomField);
        return customFieldList;
    }
}
...
```

## <a name="other-configurabilityextensibility-opportunities"></a><span data-ttu-id="f4b7f-267">Muut konfiguroitavuus- ja laajennettavuusmahdollisuudet</span><span class="sxs-lookup"><span data-stu-id="f4b7f-267">Other configurability/extensibility opportunities</span></span>

### <a name="adding-additional-validation-for-the-app"></a><span data-ttu-id="f4b7f-268">Lisävahvistuksen lisääminen sovellukselle</span><span class="sxs-lookup"><span data-stu-id="f4b7f-268">Adding additional validation for the app</span></span>

<span data-ttu-id="f4b7f-269">Työaikaraporttien toiminnallisuuden nykyinen logiikka tietokannan tasolla toimii edelleen odotetulla tavalla.</span><span class="sxs-lookup"><span data-stu-id="f4b7f-269">Existing logic for timesheet functionality at the database level will still work as expected.</span></span> <span data-ttu-id="f4b7f-270">Jos haluat keskeyttää Tallenna- tai Lähetä-toimintojen päättymisen ja näyttää tietyn virhesanoman, voit lisätä koodiin **heittovirheen ("sanoma käyttäjälle")** komentolaajennusketjun kautta.</span><span class="sxs-lookup"><span data-stu-id="f4b7f-270">To interrupt the completion of save or submit operations and show a specific error message, you can add **throw error("message to user")** to the code via a chain of command extension.</span></span> <span data-ttu-id="f4b7f-271">Seuraavassa on kolme esimerkkiä hyödyllisistä laajennettavien menetelmien menetelmistä:</span><span class="sxs-lookup"><span data-stu-id="f4b7f-271">Here are three examples of useful extensible methods:</span></span>

- <span data-ttu-id="f4b7f-272">Jos **validateWrite** TSTimesheetLine-taulussa palauttaa arvon **Epätosi** aikaraportin rivin tallennustoiminnon aikana, mobiilisovelluksessa näkyy virhesanoma.</span><span class="sxs-lookup"><span data-stu-id="f4b7f-272">If **validateWrite** on the TSTimesheetLine table returns **false** during a save operation for a timesheet line, an error message is shown in the mobile app.</span></span>
- <span data-ttu-id="f4b7f-273">Jos **validateSubmit** TSTimesheetTable-taulussa palauttaa arvon **Epätosi** aikaraportin sovelluksen esittämisen aikana, käyttäjälle näytetään virhesanoma.</span><span class="sxs-lookup"><span data-stu-id="f4b7f-273">If **validateSubmit** on the TSTimesheetTable table returns **false** during timesheet submission in the app, an error message is shown to the user.</span></span>
- <span data-ttu-id="f4b7f-274">Logiikka, joka täyttää kentät (esimerkiksi **Rivin ominaisuus**) TSTimesheetLine-taulun **insert**-menetelmän aikana, suoritetaan edelleen.</span><span class="sxs-lookup"><span data-stu-id="f4b7f-274">Logic that fills in fields (for example, **Line Property**) during the **insert** method on the TSTimesheetLine table will still run.</span></span>

### <a name="hiding-and-marking-out-of-box-fields-as-read-only-via-configuration"></a><span data-ttu-id="f4b7f-275">Käyttövalmiiden kenttien piilottaminen ja merkitseminen vain luku -muodossa konfiguroinnin kautta</span><span class="sxs-lookup"><span data-stu-id="f4b7f-275">Hiding and marking out-of-box fields as read-only via configuration</span></span>

<span data-ttu-id="f4b7f-276">Projektin parametreistä voit määrittää, että käyttövalmiit kentät ovat vain luku -muotoisia tai piilotettuja mobiilisovelluksessa.</span><span class="sxs-lookup"><span data-stu-id="f4b7f-276">From the project parameters, you can make out-of-box fields read-only or hidden in the mobile app.</span></span> <span data-ttu-id="f4b7f-277">Määritä valinnat **Mobiililaitteen aikaraportti** -osalle **Aikaraportti**-välilehdellä **Projektinhallinta- ja kirjanpidon parametrit** - sivulla.</span><span class="sxs-lookup"><span data-stu-id="f4b7f-277">Set the options in the **Mobile timesheets** section on the **Timesheet** tab of the **Project management and accounting parameters** page.</span></span>

![Projektiparametrit](media/5753b8ecccd1d8bb2b002dd538b3f762.png)

### <a name="changing-the-activities-that-are-available-for-selection-via-extensions"></a><span data-ttu-id="f4b7f-279">Valintaan käytettävissä olevien tehtävien muuttaminen laajennusten kautta</span><span class="sxs-lookup"><span data-stu-id="f4b7f-279">Changing the activities that are available for selection via extensions</span></span>

<span data-ttu-id="f4b7f-280">Projektin valintaan käytettävissä olevat toiminnot täytetään **getActivitiesForProject()**- ja **getActivityQuery()**-menetelmien avulla **TsTimesheetProjectService**-luokassa.</span><span class="sxs-lookup"><span data-stu-id="f4b7f-280">The activities that are available for selection for a project are filled in via the **getActivitiesForProject()** and **getActivityQuery()** methods in the **TsTimesheetProjectService** class.</span></span> <span data-ttu-id="f4b7f-281">Voit käyttää komentoketjua, kun haluat muuttaa tätä toimintatapaa niin, että se vastaa tiettyä projektia varten valittavissa olevien toimintojen liiketoimintaskenaariota.</span><span class="sxs-lookup"><span data-stu-id="f4b7f-281">You can use chain of command to change this behavior to match your business scenario for the activities that are available for selection for a specific project.</span></span>

### <a name="entering-a-default-project-category-on-timesheet-entries"></a><span data-ttu-id="f4b7f-282">Oletusprojektiluokan syöttäminen työaikaraportin merkinnöille</span><span class="sxs-lookup"><span data-stu-id="f4b7f-282">Entering a default project category on timesheet entries</span></span>

<span data-ttu-id="f4b7f-283">Oletusprojektiluokan määritys työaikaraportin merkinnöissä tapahtuu kolmella tasolla.</span><span class="sxs-lookup"><span data-stu-id="f4b7f-283">Entry of a default project category on timesheet entries occurs at three levels.</span></span> <span data-ttu-id="f4b7f-284">Voit käyttää komentoketjua, kun haluat laajentaa käyttäytymistä millä tahansa tai kaikilla näillä tasoilla halutun toiminnan saavuttamiseksi.</span><span class="sxs-lookup"><span data-stu-id="f4b7f-284">You can use chain of command to extend the behavior at any or all of these levels to achieve the desired behavior.</span></span> <span data-ttu-id="f4b7f-285">Seuraavaa hierarkiaa käytetään:</span><span class="sxs-lookup"><span data-stu-id="f4b7f-285">The following hierarchy is used:</span></span>

1. <span data-ttu-id="f4b7f-286">Sovellus yrittää sijoittaa oletusluokan projektiresurssista.</span><span class="sxs-lookup"><span data-stu-id="f4b7f-286">The app tries to put the default category from the project resource.</span></span> <span data-ttu-id="f4b7f-287">Tämä oletus luokka on määritetty **getCurrentUserResource**- ja **getDelegatedResourcesForCurrentUser**-menetelmille **TSTimesheetSettingsService**-luokassa.</span><span class="sxs-lookup"><span data-stu-id="f4b7f-287">This default category is set in the **getCurrentUserResource** and **getDelegatedResourcesForCurrentUser** methods in the **TSTimesheetSettingsService** class.</span></span>
2. <span data-ttu-id="f4b7f-288">Jos oletusluokkaa ei ole projektiresurssitasolla, sovellus yrittää vetää sen projektitehtävästä.</span><span class="sxs-lookup"><span data-stu-id="f4b7f-288">If the default category isn't provided at the project resource level, the app tries to pull it from the project activity.</span></span> <span data-ttu-id="f4b7f-289">Tämä oletusluokka määritetään **getActivitiesForProject**-menetelmällä **TSTimesheetProjectService**-luokassa.</span><span class="sxs-lookup"><span data-stu-id="f4b7f-289">This default category is set in the **getActivitiesForProject** method in the **TSTimesheetProjectService** class.</span></span>
3. <span data-ttu-id="f4b7f-290">Jos oletusluokkaa ei ole projektitehtävätasolla, oletuskategoria otetaan projektin parametreista.</span><span class="sxs-lookup"><span data-stu-id="f4b7f-290">If the default category isn't provided at the project activity level, the default category it taken from the project parameters.</span></span> <span data-ttu-id="f4b7f-291">Tämä oletusluokka määritetään **getProjectDetailsbyRule**-menetelmällä **TSTimesheetProjectService**-luokassa.</span><span class="sxs-lookup"><span data-stu-id="f4b7f-291">This default category is set in the **getProjectDetailsbyRule** method in the **TSTimesheetProjectService** class.</span></span>
