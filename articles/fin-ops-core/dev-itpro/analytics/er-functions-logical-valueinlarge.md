---
title: VALUEINLARGE ER -funktio
description: Tässä ohjeaiheessa käsitellään sähköisen raportoinnin (ER) VALUEINLARGE-funktion käyttämistä.
author: NickSelin
manager: kfend
ms.date: 08/17/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2020-08-01
ms.dyn365.ops.version: AX 10.0.14
ms.openlocfilehash: 4630ec20e7cbca97c5e43093e6a888a5e09f41a3
ms.sourcegitcommit: 38ad6f791c3d5688a5dc201a234ba89f155f7f03
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/19/2020
ms.locfileid: "3705140"
---
# <a name="valueinlarge-er-function"></a><span data-ttu-id="0e630-103">VALUEINLARGE ER -funktio</span><span class="sxs-lookup"><span data-stu-id="0e630-103">VALUEINLARGE ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0e630-104">`VALUEINLARGE`-funktio määrittää, vastaako määritetty *Int64*- tai *Kokonaisluku*-tyyppi määritetyn luettelokohteen tiettyä arvoa.</span><span class="sxs-lookup"><span data-stu-id="0e630-104">The `VALUEINLARGE` function determines whether the specified input of the *Int64* or *Integer* type matches any value of a specified item in the specified list.</span></span> <span data-ttu-id="0e630-105">Funktio *totuusarvon* arvon **TOSI**, jos määritetty syöte vastaa määritetyn lausekkeen suorittamisen tulosta vähintään yhdelle määritetyn luettelon tietueelle.</span><span class="sxs-lookup"><span data-stu-id="0e630-105">The function returns a *Boolean* value of **TRUE** if the specified input matches the result of running the specified expression for at least one record of the specified list.</span></span> <span data-ttu-id="0e630-106">Muussa tapauksessa se palauttaa *totuusarvon* **EPÄTOSI**.</span><span class="sxs-lookup"><span data-stu-id="0e630-106">Otherwise, it returns a *Boolean* value of **FALSE**.</span></span> <span data-ttu-id="0e630-107">Lisätietoja erosta `VALUEIN`-funktioon on jäljempänä tässä ohjeaiheessa kohdassa [Käyttötiedote](#usage_note).</span><span class="sxs-lookup"><span data-stu-id="0e630-107">To understand the difference with the `VALUEIN` function, see the [Usage note](#usage_note) section later in this topic.</span></span>

## <a name="syntax"></a><span data-ttu-id="0e630-108">Syntaksi</span><span class="sxs-lookup"><span data-stu-id="0e630-108">Syntax</span></span>

```vb
VALUEINLARGE (input, list, list item expression)
```

## <a name="arguments"></a><span data-ttu-id="0e630-109">Argumentit</span><span class="sxs-lookup"><span data-stu-id="0e630-109">Arguments</span></span>

<span data-ttu-id="0e630-110">`input`: *Kenttä*</span><span class="sxs-lookup"><span data-stu-id="0e630-110">`input`: *Field*</span></span>

<span data-ttu-id="0e630-111">*Tietueluettelo*-tyypin tietolähdenimikkeen kelvollinen polku.</span><span class="sxs-lookup"><span data-stu-id="0e630-111">The valid path of a data source item of the *Record list* type.</span></span> <span data-ttu-id="0e630-112">Tämän nimikkeen arvon vastaavuus määritetään.</span><span class="sxs-lookup"><span data-stu-id="0e630-112">The value of this item will be matched.</span></span>

<span data-ttu-id="0e630-113">`list`: *Tietueluettelo*</span><span class="sxs-lookup"><span data-stu-id="0e630-113">`list`: *Record list*</span></span>

<span data-ttu-id="0e630-114">*Tietueluettelo*-tietotyypin tietolähteen kelvollinen polku.</span><span class="sxs-lookup"><span data-stu-id="0e630-114">The valid path of a data source of the *Record list* data type.</span></span>

<span data-ttu-id="0e630-115">`list item expression`: *Lauseke*</span><span class="sxs-lookup"><span data-stu-id="0e630-115">`list item expression`: *Expression*</span></span>

<span data-ttu-id="0e630-116">Kelvollinen ehdollinen lauseke, joka joko osoittaa tai sisältää määritetyn luettelon yhden kentän, jota olisi käytettävä vastaavuuteen.</span><span class="sxs-lookup"><span data-stu-id="0e630-116">A valid conditional expression that either points to or contains a single field of the specified list that should be used for the matching.</span></span>

## <a name="return-values"></a><span data-ttu-id="0e630-117">Palautusarvot</span><span class="sxs-lookup"><span data-stu-id="0e630-117">Return values</span></span>

<span data-ttu-id="0e630-118">*Boolen arvo*</span><span class="sxs-lookup"><span data-stu-id="0e630-118">*Boolean*</span></span>

<span data-ttu-id="0e630-119">Tuloksena oleva *Totuusarvo*-arvo.</span><span class="sxs-lookup"><span data-stu-id="0e630-119">The resulting *Boolean* value.</span></span>

## <a name=""></a><span data-ttu-id="0e630-120"><a name="usage_note">Käyttöhuomautukset</a></span><span class="sxs-lookup"><span data-stu-id="0e630-120"><a name="usage_note">Usage notes</a></span></span>

<span data-ttu-id="0e630-121">Kun määritetty syöte ilmaisee *Int64*- tai *Kokonaisluku*-tyyppisen tietolähdenimikkeen, suoraksi SQL-lausekkeeksi käännettävä kutsu, määritetty luettelo muunnetaan väliaikaiseksi SQL-taulukoksi ja vastaavuus suoritetaan tietokannassa suorittamalla yksi `EXISTS JOIN` -kysely.</span><span class="sxs-lookup"><span data-stu-id="0e630-121">When the specified input represents an *Int64* or *Integer* type of a data source item, the call to which is translatable to a direct SQL statement, the specified list is converted to a temporary SQL table and matching is performed in the database by executing a single `EXISTS JOIN` query.</span></span> <span data-ttu-id="0e630-122">Muussa tapauksessa tämä funktio toimii kuten [`VALUEIN`](er-functions-logical-valuein.md)-funktio.</span><span class="sxs-lookup"><span data-stu-id="0e630-122">Otherwise, this function works as the [`VALUEIN`](er-functions-logical-valuein.md) function.</span></span>

<span data-ttu-id="0e630-123">Kun määritetty syöte ilmaisee tietolähdenimikkeen, joka suunniteltiin muuna kuin *Int64*- ja *Kokonaisluku*-tyyppisenä nimikkeenä, suunnitteluvaiheessa tapahtuu virhe, joka ilmoittaa, että `VALUEINLARGE`-funktiota ei voi käytätä määritetyssä ER-lausekkeessa.</span><span class="sxs-lookup"><span data-stu-id="0e630-123">When the specified input represents a data source item that is designed as an item other than *Int64* and *Integer* type, an error occurs at design time informing you that the `VALUEINLARGE` function is not applicable for the configured ER expression.</span></span>

<span data-ttu-id="0e630-124">`VALUEINLARGE`-funktion lauseke suoritetaan ja suoritus koskee vähintään kahta väliaikaista taulukkoa, suorituspalveluvirhe tapahtuu.</span><span class="sxs-lookup"><span data-stu-id="0e630-124">When the `VALUEINLARGE` function expression is executed and more than one temporary table is used in scope of this execution, a runtime error occurs.</span></span>

## <a name="example"></a><span data-ttu-id="0e630-125">Esimerkki</span><span class="sxs-lookup"><span data-stu-id="0e630-125">Example</span></span>

<span data-ttu-id="0e630-126">Määritä seuraavat tietolähteet omassa mallimäärityksessäsi:</span><span class="sxs-lookup"><span data-stu-id="0e630-126">You define the following data sources in your model mapping:</span></span>

- <span data-ttu-id="0e630-127">*Taulukon tietueet* -tyypin **Sisällä**-tietolähde.</span><span class="sxs-lookup"><span data-stu-id="0e630-127">The **In** data source of the *Table records* type.</span></span>
    - <span data-ttu-id="0e630-128">Tämä tietolähde viittaa **Intrastat**-tauluun.</span><span class="sxs-lookup"><span data-stu-id="0e630-128">This data source refers to the **Intrastat** table.</span></span>
    - <span data-ttu-id="0e630-129">**Yritystenvälinen**-asetuksena on **Ei**.</span><span class="sxs-lookup"><span data-stu-id="0e630-129">The **Cross-company** option is set to **No**.</span></span>
- <span data-ttu-id="0e630-130">*Laskettu kenttä* -tyypin **InMemory**-tietolähde.</span><span class="sxs-lookup"><span data-stu-id="0e630-130">The **InMemory** data source of the *Calculated field* type.</span></span>
    - <span data-ttu-id="0e630-131">Tässä tietolähteessä on lauseke `WHERE (In, In.Port <> "")`.</span><span class="sxs-lookup"><span data-stu-id="0e630-131">This data source contains the expression `WHERE (In, In.Port <> "")`.</span></span>
- <span data-ttu-id="0e630-132">*Laskettu kenttä* -tyypin **InFiltered**-tietolähde.</span><span class="sxs-lookup"><span data-stu-id="0e630-132">The **InFiltered** data source of the *Calculated field* type.</span></span>
    - <span data-ttu-id="0e630-133">Tässä tietolähteessä on lauseke `FILTER (In, VALUEINLARGE(In.RecId, InMemory, InMemory.RecId)`.</span><span class="sxs-lookup"><span data-stu-id="0e630-133">This data source contains the expression `FILTER (In, VALUEINLARGE(In.RecId, InMemory, InMemory.RecId)`.</span></span>

<span data-ttu-id="0e630-134">Jos **InFiltered**-tietolähdettä kutsutaan **DEMF**-yrityskontekstissa, sovellustietokantaan luodaan uusi väliaikainen taulu, muistiluetteloon kerätyt tietueen tunnistuskoodit lisätään tähän tauluun ja seuraava SQL-lauseke luodaan palauttamaan **Intrastat**-taulun suodatetut tietueet.</span><span class="sxs-lookup"><span data-stu-id="0e630-134">When the data source **InFiltered** is called under the context of the company **DEMF**, a new temporary table is created in the application database, the collected in memory list of record identification codes are inserted to this table, and the following SQL statement is generated to return filtered records of the **Intrastat** table.</span></span>

```xpp
SELECT … from Intrastat T1
WHERE ((T1.PARTITION=?) AND (T1.DATAAREAID IN (N'DEMF'))) AND
EXISTS (SELECT 'x' FROM tempdb."DBO".? T2 WHERE ((T2.PARTITION=?) AND (T1.RecId=T2.RecId)))
```

## <a name="additional-resources"></a><span data-ttu-id="0e630-135">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="0e630-135">Additional resources</span></span>

[<span data-ttu-id="0e630-136">Loogiset toiminnot</span><span class="sxs-lookup"><span data-stu-id="0e630-136">Logical functions</span></span>](er-functions-category-logical.md)

[<span data-ttu-id="0e630-137">VALUEIN-funktiot</span><span class="sxs-lookup"><span data-stu-id="0e630-137">VALUEIN functions</span></span>](er-functions-logical-valuein.md)
