---
title: JSONVALUE ER -funktio
description: Tässä ohjeaiheessa on tietoja siitä, miten sähköisen raportoinnin (ER) JSONVALUE-funktiota käytetään.
author: NickSelin
manager: kfend
ms.date: 12/11/2019
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
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 75f20632074cb4dead98991fd6522ab9b20b9965
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/12/2020
ms.locfileid: "3041213"
---
# <span data-ttu-id="9e510-103"><a name="JSONVALUE">JSONVALUE ER -funktio</a></span><span class="sxs-lookup"><span data-stu-id="9e510-103"><a name="JSONVALUE">JSONVALUE ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9e510-104">`JSONVALUE`-funktio jäsentää tiedot JavaScript Object Notation (JSON) -muodossa, jota käytettään tietyssä polussa, ja se purkaa skalaariarvon, jolla on tietty tunnus.</span><span class="sxs-lookup"><span data-stu-id="9e510-104">The `JSONVALUE` function parses data in JavaScript Object Notation (JSON) format that is accessed at the specified path, and it extracts a scalar value that has the specified ID.</span></span> <span data-ttu-id="9e510-105">Sen jälkeen se palauttaa puretut skalaariarvot *merkkijono*-arvona.</span><span class="sxs-lookup"><span data-stu-id="9e510-105">It then returns the extracted scalar value as a *String* value.</span></span>

## <a name="syntax"></a><span data-ttu-id="9e510-106">Syntaksi</span><span class="sxs-lookup"><span data-stu-id="9e510-106">Syntax</span></span>

```vb
JSONVALUE (input, path)
```

## <a name="arguments"></a><span data-ttu-id="9e510-107">Argumentit</span><span class="sxs-lookup"><span data-stu-id="9e510-107">Arguments</span></span>

<span data-ttu-id="9e510-108">`input`: *Merkkijono*</span><span class="sxs-lookup"><span data-stu-id="9e510-108">`input`: *String*</span></span>

<span data-ttu-id="9e510-109">JSON-tietoja sisältävän *Merkkijono*-tyypin tietolähteen kelvollinen polku.</span><span class="sxs-lookup"><span data-stu-id="9e510-109">The valid path of a data source of the *String* type that contains JSON data.</span></span>

<span data-ttu-id="9e510-110">`path`: *Merkkijono*</span><span class="sxs-lookup"><span data-stu-id="9e510-110">`path`: *String*</span></span>

<span data-ttu-id="9e510-111">JSON-tietojen skaalariarvon tunniste.</span><span class="sxs-lookup"><span data-stu-id="9e510-111">The identifier of a scalar value of JSON data.</span></span>

## <a name="return-values"></a><span data-ttu-id="9e510-112">Palautusarvot</span><span class="sxs-lookup"><span data-stu-id="9e510-112">Return values</span></span>

<span data-ttu-id="9e510-113">*merkkijono*</span><span class="sxs-lookup"><span data-stu-id="9e510-113">*String*</span></span>

<span data-ttu-id="9e510-114">Tulokseksi saatava tekstiarvo.</span><span class="sxs-lookup"><span data-stu-id="9e510-114">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="9e510-115">Esimerkki</span><span class="sxs-lookup"><span data-stu-id="9e510-115">Example</span></span>

<span data-ttu-id="9e510-116">**$JsonField**-tietolähde sisältää seuraavat tiedot JSON-muodossa: **{BuildNumber":"7.3.1234.1", "KeyThumbprint":"7366E"}**.</span><span class="sxs-lookup"><span data-stu-id="9e510-116">The **JsonField** data source contains the following data in JSON format: **{"BuildNumber":"7.3.1234.1", "KeyThumbprint":"7366E"}**.</span></span> <span data-ttu-id="9e510-117">Tässä tapauksessa `JSONVALUE (JsonField, "BuildNumber")`-lauseke palauttaa *merkkijonon* tietotyypin seuraavan arvon: **"7.3.1234.1"**.</span><span class="sxs-lookup"><span data-stu-id="9e510-117">In this case, the expression `JSONVALUE (JsonField, "BuildNumber")` returns the following value of the *String* data type: **"7.3.1234.1"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="9e510-118">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="9e510-118">Additional resources</span></span>

[<span data-ttu-id="9e510-119">Tekstitoiminnot</span><span class="sxs-lookup"><span data-stu-id="9e510-119">Text functions</span></span>](er-functions-category-text.md)
