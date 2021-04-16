---
title: JSONVALUE ER -funktio
description: Tässä ohjeaiheessa on tietoja siitä, miten sähköisen raportoinnin (ER) JSONVALUE-funktiota käytetään.
author: NickSelin
ms.date: 12/11/2019
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
ms.openlocfilehash: e8336e43a236e3f3b875fb3cb81bc139507673c2
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2021
ms.locfileid: "5746360"
---
# <a name="jsonvalue-er-function"></a><span data-ttu-id="4af2c-103">JSONVALUE ER -funktio</span><span class="sxs-lookup"><span data-stu-id="4af2c-103">JSONVALUE ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4af2c-104">`JSONVALUE`-funktio jäsentää tiedot JavaScript Object Notation (JSON) -muodossa, jota käytettään tietyssä polussa, ja se purkaa skalaariarvon, jolla on tietty tunnus.</span><span class="sxs-lookup"><span data-stu-id="4af2c-104">The `JSONVALUE` function parses data in JavaScript Object Notation (JSON) format that is accessed at the specified path, and it extracts a scalar value that has the specified ID.</span></span> <span data-ttu-id="4af2c-105">Sen jälkeen se palauttaa puretut skalaariarvot *merkkijono*-arvona.</span><span class="sxs-lookup"><span data-stu-id="4af2c-105">It then returns the extracted scalar value as a *String* value.</span></span>

## <a name="syntax"></a><span data-ttu-id="4af2c-106">Syntaksi</span><span class="sxs-lookup"><span data-stu-id="4af2c-106">Syntax</span></span>

```vb
JSONVALUE (input, path)
```

## <a name="arguments"></a><span data-ttu-id="4af2c-107">Argumentit</span><span class="sxs-lookup"><span data-stu-id="4af2c-107">Arguments</span></span>

<span data-ttu-id="4af2c-108">`input`: *Merkkijono*</span><span class="sxs-lookup"><span data-stu-id="4af2c-108">`input`: *String*</span></span>

<span data-ttu-id="4af2c-109">JSON-tietoja sisältävän *Merkkijono*-tyypin tietolähteen kelvollinen polku.</span><span class="sxs-lookup"><span data-stu-id="4af2c-109">The valid path of a data source of the *String* type that contains JSON data.</span></span>

<span data-ttu-id="4af2c-110">`path`: *Merkkijono*</span><span class="sxs-lookup"><span data-stu-id="4af2c-110">`path`: *String*</span></span>

<span data-ttu-id="4af2c-111">JSON-tietojen skaalariarvon tunniste.</span><span class="sxs-lookup"><span data-stu-id="4af2c-111">The identifier of a scalar value of JSON data.</span></span>

## <a name="return-values"></a><span data-ttu-id="4af2c-112">Palautusarvot</span><span class="sxs-lookup"><span data-stu-id="4af2c-112">Return values</span></span>

<span data-ttu-id="4af2c-113">*merkkijono*</span><span class="sxs-lookup"><span data-stu-id="4af2c-113">*String*</span></span>

<span data-ttu-id="4af2c-114">Tulokseksi saatava tekstiarvo.</span><span class="sxs-lookup"><span data-stu-id="4af2c-114">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="4af2c-115">Esimerkki</span><span class="sxs-lookup"><span data-stu-id="4af2c-115">Example</span></span>

<span data-ttu-id="4af2c-116">**$JsonField**-tietolähde sisältää seuraavat tiedot JSON-muodossa: **{BuildNumber":"7.3.1234.1", "KeyThumbprint":"7366E"}**.</span><span class="sxs-lookup"><span data-stu-id="4af2c-116">The **JsonField** data source contains the following data in JSON format: **{"BuildNumber":"7.3.1234.1", "KeyThumbprint":"7366E"}**.</span></span> <span data-ttu-id="4af2c-117">Tässä tapauksessa `JSONVALUE (JsonField, "BuildNumber")`-lauseke palauttaa *merkkijonon* tietotyypin seuraavan arvon: **"7.3.1234.1"**.</span><span class="sxs-lookup"><span data-stu-id="4af2c-117">In this case, the expression `JSONVALUE (JsonField, "BuildNumber")` returns the following value of the *String* data type: **"7.3.1234.1"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="4af2c-118">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="4af2c-118">Additional resources</span></span>

[<span data-ttu-id="4af2c-119">Tekstitoiminnot</span><span class="sxs-lookup"><span data-stu-id="4af2c-119">Text functions</span></span>](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]