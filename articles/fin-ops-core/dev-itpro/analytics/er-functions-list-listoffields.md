---
title: LISTOFFIELDS ER-funktio
description: Tässä ohjeaiheessa on tietoja siitä, miten sähköisen raportoinnin (ER) LISTOFFIELDS-funktiota käytetään.
author: NickSelin
manager: kfend
ms.date: 12/12/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 494dc347fadf44121c7eae0acf8c30768c58f035
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/09/2021
ms.locfileid: "5567661"
---
# <a name="listoffields-er-function"></a><span data-ttu-id="19f27-103">LISTOFFIELDS ER-funktio</span><span class="sxs-lookup"><span data-stu-id="19f27-103">LISTOFFIELDS ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="19f27-104">`LISTOFFIELDS`-funktio palauttaa *Tietueluettelon* arvon, joka luodaan *luettelointi*- tai *säilö (tietue)* -tyypin määritetyn argumentin rakenteen perusteella.</span><span class="sxs-lookup"><span data-stu-id="19f27-104">The `LISTOFFIELDS` function returns a *Record list* value that is created based on the structure of the specified argument of the *Enumeration* or *Container (record)* type.</span></span>

## <a name="syntax-1"></a><span data-ttu-id="19f27-105">Syntaksi 1</span><span class="sxs-lookup"><span data-stu-id="19f27-105">Syntax 1</span></span>

```vb
LISTOFFIELDS (path)
```

## <a name="syntax-2"></a><span data-ttu-id="19f27-106">Syntaksi 2</span><span class="sxs-lookup"><span data-stu-id="19f27-106">Syntax 2</span></span>

```vb
LISTOFFIELDS (path, language)
```

## <a name="arguments"></a><span data-ttu-id="19f27-107">Argumentit</span><span class="sxs-lookup"><span data-stu-id="19f27-107">Arguments</span></span>

<span data-ttu-id="19f27-108">`path`: Tietolähdeviite</span><span class="sxs-lookup"><span data-stu-id="19f27-108">`path`: Data source reference</span></span>

<span data-ttu-id="19f27-109">Tieto lähteen kelvollinen viitepolku, joka on jokin seuraavista tietotyypeistä:</span><span class="sxs-lookup"><span data-stu-id="19f27-109">The valid reference path of a data source of one of the following data types:</span></span>

- <span data-ttu-id="19f27-110">Mallin luettelointi</span><span class="sxs-lookup"><span data-stu-id="19f27-110">Model enumeration</span></span>
- <span data-ttu-id="19f27-111">Muodon luettelointi</span><span class="sxs-lookup"><span data-stu-id="19f27-111">Format enumeration</span></span>
- <span data-ttu-id="19f27-112">Sovellusten luettelointi</span><span class="sxs-lookup"><span data-stu-id="19f27-112">Application enumeration</span></span>
- <span data-ttu-id="19f27-113">Kontti (tietue)</span><span class="sxs-lookup"><span data-stu-id="19f27-113">Container (record)</span></span>

<span data-ttu-id="19f27-114">`language`: *Merkkijono*</span><span class="sxs-lookup"><span data-stu-id="19f27-114">`language`: *String*</span></span>

<span data-ttu-id="19f27-115">Kielikoodia edustava teksti.</span><span class="sxs-lookup"><span data-stu-id="19f27-115">Text that represents a language code.</span></span>

## <a name="return-values"></a><span data-ttu-id="19f27-116">Palautusarvot</span><span class="sxs-lookup"><span data-stu-id="19f27-116">Return values</span></span>

<span data-ttu-id="19f27-117">*Tietueluettelo*</span><span class="sxs-lookup"><span data-stu-id="19f27-117">*Record list*</span></span>

<span data-ttu-id="19f27-118">Tuloksena oleva tietueluettelo.</span><span class="sxs-lookup"><span data-stu-id="19f27-118">The resulting list of records.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="19f27-119">Käyttöhuomautukset</span><span class="sxs-lookup"><span data-stu-id="19f27-119">Usage notes</span></span>

<span data-ttu-id="19f27-120">Luotu luettelo koostuu tietueista, jossa on seuraavat kentät:</span><span class="sxs-lookup"><span data-stu-id="19f27-120">The list that is created consists of records that have the following fields:</span></span>

- <span data-ttu-id="19f27-121">**Nimi** (*Merkkijono* tietotyyppi)</span><span class="sxs-lookup"><span data-stu-id="19f27-121">**Name** (*String* data type)</span></span>
- <span data-ttu-id="19f27-122">**Otsikko** (*Merkkijono* tietotyyppi)</span><span class="sxs-lookup"><span data-stu-id="19f27-122">**Label** (*String* data type)</span></span>
- <span data-ttu-id="19f27-123">**Kuvaus** (*Merkkijono* tietotyyppi)</span><span class="sxs-lookup"><span data-stu-id="19f27-123">**Description** (*String* data type)</span></span>
- <span data-ttu-id="19f27-124">**IsTranslated** (*Totuusarvo* tietotyyppi)</span><span class="sxs-lookup"><span data-stu-id="19f27-124">**IsTranslated** (*Boolean* data type)</span></span>

<span data-ttu-id="19f27-125">Jos `path`-argumentti viittaa *säilön (tietue)* -tyypin tietolähteeseen viitatun säilötietueen jokaiseen kenttään, luotavaan luetteloon lisätään uusi tietue.</span><span class="sxs-lookup"><span data-stu-id="19f27-125">If the `path` argument refers to a data source of the *Container (Record)* type, for every field of the referenced container record, a new record is added to the list that is created.</span></span> <span data-ttu-id="19f27-126">Jokaisen luodun tietueen **Nimi**-kenttä palauttaa viitatun säilötietueen kentän nimen, jolle nykyinen tietue luotiin.</span><span class="sxs-lookup"><span data-stu-id="19f27-126">For every record that is created, the **Name** field returns the name of the field of the referenced container record that the current record was created for.</span></span>

<span data-ttu-id="19f27-127">Jos `path`-argumentti viittaa johonkin *luettelointi*-tyyppiin, jokaiselle viitatun luettelon arvolle lisätään uusi luettelo luotavaan luetteloon.</span><span class="sxs-lookup"><span data-stu-id="19f27-127">If the `path` argument refers to a data source of one of the *Enumeration* types, for every enumeration value of the referenced enumeration, a new record is added to the list that is created.</span></span> <span data-ttu-id="19f27-128">Jokaisen luodun tietueen **Nimi**-kenttä palauttaa viitatun luetteloinnin arvon, jolle nykyinen tietue luotiin, **Kuvaus**-kenttä palauttaa kyseisen luetteloinnin kuvauksen ja **Selite**-kenttä palauttaa kyseisen luetteloinnin otsikon.</span><span class="sxs-lookup"><span data-stu-id="19f27-128">For every record that is created, the **Name** field returns the value of the referenced enumeration that the current record was created for, the **Description** field returns the description of that enumeration, and the **Label** field returns the label of that enumeration.</span></span>

<span data-ttu-id="19f27-129">Suorituksen aikana, kun käytetään syntaksia 1, **Selite**- ja **Kuvaus**-kenttien on palautettava arvot, jotka perustuvat käynnissä olevan sähköisen raportoinnin (ER) muodon kieliasetuksiin:</span><span class="sxs-lookup"><span data-stu-id="19f27-129">At runtime, when syntax 1 is used, the **Label** and **Description** fields must return values that are based on the language settings of the Electronic reporting (ER) format that is running:</span></span>

- <span data-ttu-id="19f27-130">Jos pyydetyn kielen otsikot ja kuvaukset ovat saatavilla, **Otsikko**- ja **Kuvaus** -kentät palauttavat kyseiseen kieleen perustuvat arvot, ja **IsTranslated**-kenttä palauttaa arvon **Tosi**.</span><span class="sxs-lookup"><span data-stu-id="19f27-130">If the labels and descriptions for the requested language are available, the **Label** and **Description** fields return values that are based on that language, and the **IsTranslated** field returns **True**.</span></span>
- <span data-ttu-id="19f27-131">Jos pyydetyn kielen otsikot ja kuvaukset eivät ole saatavilla, **Otsikko**- ja **Kuvaus** -kentät palauttavat oletuksena olevaan kieleen **EN-US** perustuvat arvot, ja **IsTranslated**-kenttä palauttaa arvon **Epätosi**.</span><span class="sxs-lookup"><span data-stu-id="19f27-131">If the labels and descriptions for the requested language aren't available, the **Label** and **Description** fields return values that are based on the default **EN-US** language, and the **IsTranslated** field returns **False**.</span></span>

<span data-ttu-id="19f27-132">Suorituksen aikana, kun käytetään syntaksia 2, **Selite**- ja **Kuvaus**-kenttien on palautettava arvot, jotka perustuvat kieleen, joka määritetään kutsutun funktion toisena argumenttina:</span><span class="sxs-lookup"><span data-stu-id="19f27-132">At runtime, when syntax 2 is used, the **Label** and **Description** fields must return values that are based on the language that is defined as the second argument of the called function:</span></span>

- <span data-ttu-id="19f27-133">Jos pyydetyn kielen otsikot ja kuvaukset ovat saatavilla, **Otsikko**- ja **Kuvaus** -kentät palauttavat kyseiseen kieleen perustuvat arvot, ja **IsTranslated**-kenttä palauttaa arvon **Tosi**.</span><span class="sxs-lookup"><span data-stu-id="19f27-133">If the labels and descriptions for the requested language are available, the **Label** and **Description** fields return values that are based on that language, and the **IsTranslated** field returns **True**.</span></span>
- <span data-ttu-id="19f27-134">Jos pyydetyn kielen otsikot ja kuvaukset eivät ole saatavilla, **Otsikko**- ja **Kuvaus** -kentät palauttavat kieleen **EN-US** perustuvat arvot, ja **IsTranslated**-kenttä palauttaa arvon **Epätosi**.</span><span class="sxs-lookup"><span data-stu-id="19f27-134">If the labels and descriptions for the requested language aren't available, the **Label** and **Description** fields return values that are based on the **EN-US** language, and the **IsTranslated** field returns **False**.</span></span>

## <a name="example-1"></a><span data-ttu-id="19f27-135">Esimerkki 1</span><span class="sxs-lookup"><span data-stu-id="19f27-135">Example 1</span></span>

<span data-ttu-id="19f27-136">Seuraavassa kuvan on ER-tietomallin luettelointi.</span><span class="sxs-lookup"><span data-stu-id="19f27-136">In the following illustration, an enumeration is introduced in an ER data model.</span></span>

<a href="./media/ger-listoffields-function-model-enumeration.png"><img src="./media/ger-listoffields-function-model-enumeration-e1474545790761.png" alt="Enumeration in a model" class="alignnone wp-image-1203943 size-full" width="514" height="155" /></a>

<span data-ttu-id="19f27-137">Seuraavassa kuvassa on nämä tiedot:</span><span class="sxs-lookup"><span data-stu-id="19f27-137">The following illustration shows these details:</span></span>

- <span data-ttu-id="19f27-138">Mallin luettelointi lisätään raporttiin tietolähteenä.</span><span class="sxs-lookup"><span data-stu-id="19f27-138">The model enumeration is inserted into a report as a data source.</span></span>
- <span data-ttu-id="19f27-139">ER-lauseke käyttää mallin luettelointia `LISTOFFIELDS`-funktion parametrina.</span><span class="sxs-lookup"><span data-stu-id="19f27-139">An ER expression uses the model enumeration as a parameter of the `LISTOFFIELDS` function.</span></span>
- <span data-ttu-id="19f27-140">*Tietueluettelon* tyypin tietolähde lisätään raporttiin luodun ER-lausekkeen avulla.</span><span class="sxs-lookup"><span data-stu-id="19f27-140">A data source of the *Record list* type is inserted into a report by using the ER expression that is created.</span></span>

<a href="./media/ger-listoffields-function-in-format-expression.png"><img src="./media/ger-listoffields-function-in-format-expression-e1474546110395.png" alt="Format" class="alignnone wp-image-1204033 size-full" width="549" height="318" /></a>

<span data-ttu-id="19f27-141">Seuraavassa esimerkissä on ER-lomakkeen elementit, jotka on sidottu `LISTOFFIELDS`-funktiolla luotuun *Tietueluettelo*-tyypin tietolähteeseen.</span><span class="sxs-lookup"><span data-stu-id="19f27-141">The following example shows the ER format elements that are bound to the data source of the *Record list* type that was created by using the `LISTOFFIELDS` function.</span></span>

<a href="./media/ger-listoffields-function-format-design.png"><img src="./media/ger-listoffields-function-format-design.png" alt="Format design" class="alignnone size-full wp-image-1204043" width="466" height="221" /></a>

<span data-ttu-id="19f27-142">Seuraavassa kuvassa on tulos, kun suunniteltu muoto suoritetaan.</span><span class="sxs-lookup"><span data-stu-id="19f27-142">The following illustration shows the result when the designed format is run.</span></span>

<a href="./media/ger-listoffields-function-format-output.png"><img src="./media/ger-listoffields-function-format-output.png" alt="Format output" class="alignnone size-full wp-image-1204053" width="585" height="158" /></a>

> [!NOTE] 
> <span data-ttu-id="19f27-143">Selitteiden ja kuvausten käännetty teksti annetaan ER-lomakkeeseen **FILE**- ja **FOLDER**-päälomake-elementeille määritettyjen kieliasetusten perusteella</span><span class="sxs-lookup"><span data-stu-id="19f27-143">Based on the language settings of the parent **FILE** and **FOLDER** format elements, translated text for labels and descriptions is entered in the output of the ER format.</span></span>

## <a name="example-2"></a><span data-ttu-id="19f27-144">Esimerkki 2</span><span class="sxs-lookup"><span data-stu-id="19f27-144">Example 2</span></span>

<span data-ttu-id="19f27-145">Voit esimerkiksi määrittää *Laskettu kenttä*-tietolähdetyypin määrittämään **enumType\_de**- ja **enumType\_deCH**-tietolähteet **enumType**-tietomallin luettelointia varten:</span><span class="sxs-lookup"><span data-stu-id="19f27-145">You use the *Calculated field* data source type to configure **enumType\_de** and **enumType\_deCH** data sources for the **enumType** data model enumeration:</span></span>

- <span data-ttu-id="19f27-146">**enumType\_de** = `LISTOFFIELDS (enumType, "de")`</span><span class="sxs-lookup"><span data-stu-id="19f27-146">**enumType\_de** = `LISTOFFIELDS (enumType, "de")`</span></span>
- <span data-ttu-id="19f27-147">**enumType\_deCH** = `LISTOFFIELDS (enumType, "de-CH")`</span><span class="sxs-lookup"><span data-stu-id="19f27-147">**enumType\_deCH** = `LISTOFFIELDS (enumType, "de-CH")`</span></span>

<span data-ttu-id="19f27-148">Voit hakea tässä tapauksessa otsikon sveitsinsaksan luettelointiarvon, jos tämä käännös on käytettävissä, käyttämällä seuraavaa lauseketta.</span><span class="sxs-lookup"><span data-stu-id="19f27-148">In this case, you can use the following expression to get the label of the enumeration value in Swiss German, if that translation is available.</span></span> <span data-ttu-id="19f27-149">Jos sveitsinsaksan käännös ei ole käytettävissä, otsikko on saksankielinen.</span><span class="sxs-lookup"><span data-stu-id="19f27-149">If the Swiss German translation isn't available, the label is in German.</span></span>

```vb
IF (NOT (enumType_deCH.IsTranslated), enumType_de.Label, enumType_deCH.Label)
```

## <a name="additional-resources"></a><span data-ttu-id="19f27-150">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="19f27-150">Additional resources</span></span>

[<span data-ttu-id="19f27-151">Luettelotoiminnot</span><span class="sxs-lookup"><span data-stu-id="19f27-151">List functions</span></span>](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]