---
title: VALUE ER -funktio
description: Tässä ohjeaiheessa on tietoja siitä, miten sähköisen raportoinnin (ER) VALUE-funktiota käytetään.
author: NickSelin
ms.date: 12/05/2019
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
ms.openlocfilehash: 2252823d98b63d36d9bb195696abef34ac9c98b6
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2021
ms.locfileid: "5752577"
---
# <a name="value-er-function"></a><span data-ttu-id="79a2e-103">VALUE ER -funktio</span><span class="sxs-lookup"><span data-stu-id="79a2e-103">VALUE ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="79a2e-104">`VALUE`-funktio palauttaa *todellisen* arvon, joka muunnetaan määritetystä merkkijonosta.</span><span class="sxs-lookup"><span data-stu-id="79a2e-104">The `VALUE` function returns a *Real* value that is converted from the specified string.</span></span>

## <a name="syntax"></a><span data-ttu-id="79a2e-105">Syntaksi</span><span class="sxs-lookup"><span data-stu-id="79a2e-105">Syntax</span></span>

```vb
VALUE (text)
```

## <a name="arguments"></a><span data-ttu-id="79a2e-106">Argumentit</span><span class="sxs-lookup"><span data-stu-id="79a2e-106">Arguments</span></span>

<span data-ttu-id="79a2e-107">`text`: *Merkkijono*</span><span class="sxs-lookup"><span data-stu-id="79a2e-107">`text`: *String*</span></span>

<span data-ttu-id="79a2e-108">Merkkijonon arvo, jota ei pidä muuntaa numeroarvoon.</span><span class="sxs-lookup"><span data-stu-id="79a2e-108">A string value that must be converted to a numeric value.</span></span>

## <a name="return-values"></a><span data-ttu-id="79a2e-109">Palautusarvot</span><span class="sxs-lookup"><span data-stu-id="79a2e-109">Return values</span></span>

<span data-ttu-id="79a2e-110">*Reaaliluku*</span><span class="sxs-lookup"><span data-stu-id="79a2e-110">*Real*</span></span>

<span data-ttu-id="79a2e-111">Tuloksena oleva numeroarvo.</span><span class="sxs-lookup"><span data-stu-id="79a2e-111">The resulting numeric value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="79a2e-112">Käyttöhuomautukset</span><span class="sxs-lookup"><span data-stu-id="79a2e-112">Usage notes</span></span>

<span data-ttu-id="79a2e-113">Pilkkuja ja pisteitä (.) pidetään desimaalierottimina. Alussa olevaa tavuviivaa (-) pidetään miinusmerkkinä.</span><span class="sxs-lookup"><span data-stu-id="79a2e-113">Commas and dot characters (.) are considered decimal separators, and a leading hyphen (-) is used as a negative sign.</span></span> <span data-ttu-id="79a2e-114">Poikkeus annetaan suorituksen aikana, jos määritetyssä merkkijonossa on muita kuin numeerisia merkkejä.</span><span class="sxs-lookup"><span data-stu-id="79a2e-114">An exception is thrown at runtime if the specified string contains other non-numeric characters.</span></span>

## <a name="example-1"></a><span data-ttu-id="79a2e-115">Esimerkki 1</span><span class="sxs-lookup"><span data-stu-id="79a2e-115">Example 1</span></span>

<span data-ttu-id="79a2e-116">`VALUE ("1 234,56")` antaa poikkeuksen.</span><span class="sxs-lookup"><span data-stu-id="79a2e-116">`VALUE ("1 234,56")` throws an exception.</span></span>

## <a name="example-2"></a><span data-ttu-id="79a2e-117">Esimerkki 2</span><span class="sxs-lookup"><span data-stu-id="79a2e-117">Example 2</span></span>

<span data-ttu-id="79a2e-118">`VALUE ("1234,56")` palauttaa **1234.56**.</span><span class="sxs-lookup"><span data-stu-id="79a2e-118">`VALUE ("1234,56")` returns **1234.56**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="79a2e-119">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="79a2e-119">Additional resources</span></span>

[<span data-ttu-id="79a2e-120">Tyypin muuntamisen toiminnot</span><span class="sxs-lookup"><span data-stu-id="79a2e-120">Type conversion functions</span></span>](er-functions-category-type-conversion.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]