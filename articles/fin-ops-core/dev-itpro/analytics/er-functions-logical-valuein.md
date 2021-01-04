---
title: VALUEIN ER -funktio
description: Tässä ohjeaiheessa on tietoja siitä, miten sähköisen raportoinnin (ER) VALUEIN-funktiota käytetään.
author: NickSelin
manager: kfend
ms.date: 08/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
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
ms.openlocfilehash: 0a133067ab74c711084cc1d7f456cbe49acdf79d
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/05/2020
ms.locfileid: "4686927"
---
# <a name="valuein-er-function"></a><span data-ttu-id="77c1c-103">VALUEIN ER -funktio</span><span class="sxs-lookup"><span data-stu-id="77c1c-103">VALUEIN ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="77c1c-104">`VALUEIN`-funktio määrittää, vastaako määritetty syöte määritetyn luettelokohteen tiettyä arvoa.</span><span class="sxs-lookup"><span data-stu-id="77c1c-104">The `VALUEIN` function determines whether the specified input matches any value of a specified item in the specified list.</span></span> <span data-ttu-id="77c1c-105">Se palauttaa *totuusarvon* arvon **TOSI**, jos määritetty syöte vastaa määritetyn lausekkeen suorittamisen tulosta vähintään yhdelle määritetyn luettelon tietueelle.</span><span class="sxs-lookup"><span data-stu-id="77c1c-105">It returns a *Boolean* value of **TRUE** if the specified input matches the result of running the specified expression for at least one record of the specified list.</span></span> <span data-ttu-id="77c1c-106">Muussa tapauksessa se palauttaa *totuusarvon* **EPÄTOSI**.</span><span class="sxs-lookup"><span data-stu-id="77c1c-106">Otherwise, it returns a *Boolean* value of **FALSE**.</span></span>

## <a name="syntax"></a><span data-ttu-id="77c1c-107">Syntaksi</span><span class="sxs-lookup"><span data-stu-id="77c1c-107">Syntax</span></span>

```vb
VALUEIN (input, list, list item expression)
```

## <a name="arguments"></a><span data-ttu-id="77c1c-108">Argumentit</span><span class="sxs-lookup"><span data-stu-id="77c1c-108">Arguments</span></span>

<span data-ttu-id="77c1c-109">`input`: *Kenttä*</span><span class="sxs-lookup"><span data-stu-id="77c1c-109">`input`: *Field*</span></span>

<span data-ttu-id="77c1c-110">*Tietueluettelo*-tyypin tietolähteen kelvollinen polku.</span><span class="sxs-lookup"><span data-stu-id="77c1c-110">The valid path of an item of a data source of the *Record list* type.</span></span> <span data-ttu-id="77c1c-111">Tämän nimikkeen arvon vastaavuus määritetään.</span><span class="sxs-lookup"><span data-stu-id="77c1c-111">The value of this item will be matched.</span></span>

<span data-ttu-id="77c1c-112">`list`: *Tietueluettelo*</span><span class="sxs-lookup"><span data-stu-id="77c1c-112">`list`: *Record list*</span></span>

<span data-ttu-id="77c1c-113">*Tietueluettelo*-tietotyypin tietolähteen kelvollinen polku.</span><span class="sxs-lookup"><span data-stu-id="77c1c-113">The valid path of a data source of the *Record list* data type.</span></span>

<span data-ttu-id="77c1c-114">`list item expression`: *Totuusarvo*</span><span class="sxs-lookup"><span data-stu-id="77c1c-114">`list item expression`: *Boolean*</span></span>

<span data-ttu-id="77c1c-115">Kelvollinen ehdollinen lauseke, joka joko osoittaa tai sisältää määritetyn luettelon yhden kentän, jota olisi käytettävä vastaavuuteen.</span><span class="sxs-lookup"><span data-stu-id="77c1c-115">A valid conditional expression that either points to or contains a single field of the specified list that should be used for the matching.</span></span>

## <a name="return-values"></a><span data-ttu-id="77c1c-116">Palautusarvot</span><span class="sxs-lookup"><span data-stu-id="77c1c-116">Return values</span></span>

<span data-ttu-id="77c1c-117">*Boolen arvo*</span><span class="sxs-lookup"><span data-stu-id="77c1c-117">*Boolean*</span></span>

<span data-ttu-id="77c1c-118">Tuloksena oleva *Totuusarvo*-arvo.</span><span class="sxs-lookup"><span data-stu-id="77c1c-118">The resulting *Boolean* value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="77c1c-119">Käyttöhuomautukset</span><span class="sxs-lookup"><span data-stu-id="77c1c-119">Usage notes</span></span>

<span data-ttu-id="77c1c-120">Yleensä `VALUEIN`-funktio muunnetaan **OR**-ehtojoukoksi.</span><span class="sxs-lookup"><span data-stu-id="77c1c-120">In general, the `VALUEIN` function is translated to a set of **OR** conditions.</span></span> <span data-ttu-id="77c1c-121">Jos **TAI**-ehtojen luettelo on suuri ja SQL-lausekkeen enimmäispituus voi ylittyä, harkitse [`VALUEINLARGE`](er-functions-logical-valueinlarge.md)-funktion käyttöä.</span><span class="sxs-lookup"><span data-stu-id="77c1c-121">If the list of **OR** conditions is large and the maximum total length of an SQL statement might be exceeded, consider using the [`VALUEINLARGE`](er-functions-logical-valueinlarge.md) function.</span></span>

```vb
(input = list.item1.value) OR (input = list.item2.value) OR …
```

<span data-ttu-id="77c1c-122">Joissakin tapauksissa se voidaan kääntää tietokannan SQL-lauseessa `EXISTS JOIN`-operaattoria käyttämällä.</span><span class="sxs-lookup"><span data-stu-id="77c1c-122">In some cases, it can be translated to a database SQL statement by using the `EXISTS JOIN` operator.</span></span>

## <a name="example-1"></a><span data-ttu-id="77c1c-123">Esimerkki 1</span><span class="sxs-lookup"><span data-stu-id="77c1c-123">Example 1</span></span>

<span data-ttu-id="77c1c-124">Mallikartoituksessa määrität *Laskettu kenttä*-tyypin **Luettelo**-tietolähteen.</span><span class="sxs-lookup"><span data-stu-id="77c1c-124">In your model mapping, you define the **List** data source of the *Calculated field* type.</span></span> <span data-ttu-id="77c1c-125">Tässä tietolähteessä on lauseke `SPLIT ("a,b,c", ",")`.</span><span class="sxs-lookup"><span data-stu-id="77c1c-125">This data source contains the expression `SPLIT ("a,b,c", ",")`.</span></span>

<span data-ttu-id="77c1c-126">Jos tietolähde on kutsuttaessa määritetty `VALUEIN ("B", List, List.Value)`-lausekkeeksi, funktio palauttaa arvon **TOSI**.</span><span class="sxs-lookup"><span data-stu-id="77c1c-126">When a data source is called, if it has been configured as the `VALUEIN ("B", List, List.Value)` expression, it returns **TRUE**.</span></span> <span data-ttu-id="77c1c-127">Tässä tapauksessa `VALUEIN`-funktio muunnetaan seuraavaksi ehtojoukoksi: `(("B" = "a") or ("B" = "b") or ("B" = "c"))`, jossa `("B" = "b")` on yhtä kuin **TOSI**.</span><span class="sxs-lookup"><span data-stu-id="77c1c-127">In this case, the `VALUEIN` function is translated to the following set of conditions: `(("B" = "a") or ("B" = "b") or ("B" = "c"))`, where `("B" = "b")` equals **TRUE**.</span></span>

<span data-ttu-id="77c1c-128">Jos tietolähde on kutsuttaessa määritetty `VALUEIN ("B", List, LEFT(List.Value, 0))`-lausekkeeksi, funktio palauttaa arvon **EPÄTOSI**.</span><span class="sxs-lookup"><span data-stu-id="77c1c-128">When a data source is called, if it has been configured as the `VALUEIN ("B", List, LEFT(List.Value, 0))` expression, it returns **FALSE**.</span></span> <span data-ttu-id="77c1c-129">Tässä tapauksessa `VALUEIN`-funktio muunnetaan seuraavaksi ehdoksi: `("B" = "")` ei ole yhtä kuin **TOSI**.</span><span class="sxs-lookup"><span data-stu-id="77c1c-129">In this case, the `VALUEIN` function is translated to the following condition: `("B" = "")`, which doesn't equal **TRUE**.</span></span>

<span data-ttu-id="77c1c-130">Kyseisen ehdon tekstin suurin merkkimäärä on 32 768 merkkiä.</span><span class="sxs-lookup"><span data-stu-id="77c1c-130">The upper limit for the number of characters in the text of such a condition is 32,768 characters.</span></span> <span data-ttu-id="77c1c-131">Älä tämän vuoksi luo tietolähteitä, jotka voivat ylittää suorituksen aikana tämän rajan.</span><span class="sxs-lookup"><span data-stu-id="77c1c-131">Therefore, you should not create data sources that might exceed this limit at runtime.</span></span> <span data-ttu-id="77c1c-132">Jos raja ylitetään, sovellus pysähtyy ja annetaan poikkeus.</span><span class="sxs-lookup"><span data-stu-id="77c1c-132">If the limit is exceeded, the application stops running, and an exception is thrown.</span></span> <span data-ttu-id="77c1c-133">Tämä tilanne voi esiintyä esimerkiksi silloin, jos tietolähteeksi on määritetty `WHERE (List1, VALUEIN (List1.ID, List2, List2.ID)` ja **List1**- ja **List2**-luetteloissa on suuria määriä tietueita.</span><span class="sxs-lookup"><span data-stu-id="77c1c-133">For example, this situation can occur if the data source is configured as `WHERE (List1, VALUEIN (List1.ID, List2, List2.ID)`, and the **List1** and **List2** lists contain a large volume of records.</span></span>

<span data-ttu-id="77c1c-134">Joissakin tapauksissa `VALUEIN`-funktio muunnetaan tietokantalausekkeeksi `EXISTS JOIN` -operaattorin avulla.</span><span class="sxs-lookup"><span data-stu-id="77c1c-134">In some cases, the `VALUEIN` function is translated to a database statement by using the `EXISTS JOIN` operator.</span></span> <span data-ttu-id="77c1c-135">Näin tapahtuu, kun käytetään [`FILTER`](er-functions-list-filter.md)-funktiota ja seuraavat ehdot täyttyvät:</span><span class="sxs-lookup"><span data-stu-id="77c1c-135">This behavior occurs when the [`FILTER`](er-functions-list-filter.md) function is used and the following conditions are met:</span></span>

- <span data-ttu-id="77c1c-136">**KYSY KYSELYÄ** -asetus on poistettu käytöstä siinä `VALUEIN`-funktion tietolähteessä, joka viittaa tietueluetteloon.</span><span class="sxs-lookup"><span data-stu-id="77c1c-136">The **ASK FOR QUERY** option is turned off for the data source of the `VALUEIN` function that refers to the list of records.</span></span> <span data-ttu-id="77c1c-137">Tässä tietolähteessä ei käytetä suorituksen aikana mitään lisäehtoja.</span><span class="sxs-lookup"><span data-stu-id="77c1c-137">No additional conditions will be applied to this data source at runtime.</span></span>
- <span data-ttu-id="77c1c-138">Tietueluetteloon viittaavaan `VALUEIN`-funktion tietolähteeseen ei ole määritetty upotettuja lausekkeita.</span><span class="sxs-lookup"><span data-stu-id="77c1c-138">No nested expressions are configured for the data source of the `VALUEIN` function that refers to the list of records.</span></span>
- <span data-ttu-id="77c1c-139">`VALUEIN`-funktion luettelokohde viittaa määritetyn tietolähteen kenttään eikä tämän tietolähteen lausekkeeseen tai menetelmään.</span><span class="sxs-lookup"><span data-stu-id="77c1c-139">A list item of the `VALUEIN` function refers to a field of the specified data source, not to an expression or method of that data source.</span></span>

<span data-ttu-id="77c1c-140">Harkitse tämän vaihtoehdon käyttöä [`WHERE`](er-functions-list-where.md)-funktion sijaan, joka on kuvattu aiemmin tässä esimerkissä.</span><span class="sxs-lookup"><span data-stu-id="77c1c-140">Consider using this option instead of the [`WHERE`](er-functions-list-where.md) function that is described earlier in this example.</span></span>

## <a name="example-2"></a><span data-ttu-id="77c1c-141">Esimerkki 2</span><span class="sxs-lookup"><span data-stu-id="77c1c-141">Example 2</span></span>

<span data-ttu-id="77c1c-142">Määritä seuraavat tietolähteet omassa mallimäärityksessäsi:</span><span class="sxs-lookup"><span data-stu-id="77c1c-142">You define the following data sources in your model mapping:</span></span>

- <span data-ttu-id="77c1c-143">*Taulukon tietueet* -tyypin **Sisällä**-tietolähde.</span><span class="sxs-lookup"><span data-stu-id="77c1c-143">The **In** data source of the *Table records* type.</span></span> <span data-ttu-id="77c1c-144">Tämä tietolähde viittaa Intrastat-tauluun.</span><span class="sxs-lookup"><span data-stu-id="77c1c-144">This data source refers to the Intrastat table.</span></span>
- <span data-ttu-id="77c1c-145">*Taulukon tietueet* -tyypin **Portti**-tietolähde.</span><span class="sxs-lookup"><span data-stu-id="77c1c-145">The **Port** data source of the *Table records* type.</span></span> <span data-ttu-id="77c1c-146">Tämä tietolähde viittaa IntrastatPort-tauluun.</span><span class="sxs-lookup"><span data-stu-id="77c1c-146">This data source refers to the IntrastatPort table.</span></span>

<span data-ttu-id="77c1c-147">Kun `FILTER (In, VALUEIN(In.Port, Port, Port.PortId)` -lausekkeena määritetty tietolähde kutsutaan, luodaan seuraava SQL-lauseke palauttamaan Intrastat-taulun suodatetut tietueet.</span><span class="sxs-lookup"><span data-stu-id="77c1c-147">When a data source is called that has been configured as the `FILTER (In, VALUEIN(In.Port, Port, Port.PortId)` expression, the following SQL statement is generated to return filtered records of the Intrastat table.</span></span>

```vb
select … from Intrastat
exists join TableId from IntrastatPort
where IntrastatPort.PortId = Intrastat.Port
```

<span data-ttu-id="77c1c-148">**dataAreaId**-kenttien lopullinen SQL-lauseke luodaan käyttämällä `IN`-operaattoria.</span><span class="sxs-lookup"><span data-stu-id="77c1c-148">For **dataAreaId** fields, the final SQL statement is generated by the using `IN` operator.</span></span>

## <a name="example-3"></a><span data-ttu-id="77c1c-149">Esimerkki 3</span><span class="sxs-lookup"><span data-stu-id="77c1c-149">Example 3</span></span>

<span data-ttu-id="77c1c-150">Määritä seuraavat tietolähteet omassa mallimäärityksessäsi:</span><span class="sxs-lookup"><span data-stu-id="77c1c-150">You define the following data sources in your model mapping:</span></span>

- <span data-ttu-id="77c1c-151">*Laskettu kenttä* -tyypin **Le**-tietolähde.</span><span class="sxs-lookup"><span data-stu-id="77c1c-151">The **Le** data source of the *Calculated field* type.</span></span> <span data-ttu-id="77c1c-152">Tässä tietolähteessä on lauseke `SPLIT ("DEMF,GBSI,USMF", ",")`.</span><span class="sxs-lookup"><span data-stu-id="77c1c-152">This data source contains the expression `SPLIT ("DEMF,GBSI,USMF", ",")`.</span></span>
- <span data-ttu-id="77c1c-153">*Taulukon tietueet* -tyypin **Sisällä**-tietolähde.</span><span class="sxs-lookup"><span data-stu-id="77c1c-153">The **In** data source of the *Table records* type.</span></span> <span data-ttu-id="77c1c-154">Tämä tietolähde viittaa Intrastat-tauluun ja **Yritysten väliset** -vaihtoehto on otettu käyttöön.</span><span class="sxs-lookup"><span data-stu-id="77c1c-154">This data source refers to the Intrastat table, and the **Cross-company** option is turned on for it.</span></span>

<span data-ttu-id="77c1c-155">Kun `FILTER (In, VALUEIN (In.dataAreaId, Le, Le.Value)` -lausekkeena määritetty tietolähde kutsutaan, lopullinen SQL-lauseke sisältää seuraavan ehdon.</span><span class="sxs-lookup"><span data-stu-id="77c1c-155">When a data source is called that has been configured as the `FILTER (In, VALUEIN (In.dataAreaId, Le, Le.Value)` expression, the final SQL statement contains the following condition.</span></span>

```vb
Intrastat.dataAreaId IN ('DEMF', 'GBSI', 'USMF')
```

## <a name="additional-resources"></a><span data-ttu-id="77c1c-156">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="77c1c-156">Additional resources</span></span>

[<span data-ttu-id="77c1c-157">Loogiset toiminnot</span><span class="sxs-lookup"><span data-stu-id="77c1c-157">Logical functions</span></span>](er-functions-category-logical.md)

[<span data-ttu-id="77c1c-158">VALUEINLARGE-funktiot</span><span class="sxs-lookup"><span data-stu-id="77c1c-158">VALUEINLARGE functions</span></span>](er-functions-logical-valueinlarge.md)
