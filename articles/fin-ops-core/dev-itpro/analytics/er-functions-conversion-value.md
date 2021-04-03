---
title: VALUE ER -funktio
description: Tässä ohjeaiheessa on tietoja siitä, miten sähköisen raportoinnin (ER) VALUE-funktiota käytetään.
author: NickSelin
manager: kfend
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
ms.openlocfilehash: 7cdaa302e757b54858e36c3716167593383d7071
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/09/2021
ms.locfileid: "5561443"
---
# <a name="value-er-function"></a><span data-ttu-id="c0c6b-103">VALUE ER -funktio</span><span class="sxs-lookup"><span data-stu-id="c0c6b-103">VALUE ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c0c6b-104">`VALUE`-funktio palauttaa *todellisen* arvon, joka muunnetaan määritetystä merkkijonosta.</span><span class="sxs-lookup"><span data-stu-id="c0c6b-104">The `VALUE` function returns a *Real* value that is converted from the specified string.</span></span>

## <a name="syntax"></a><span data-ttu-id="c0c6b-105">Syntaksi</span><span class="sxs-lookup"><span data-stu-id="c0c6b-105">Syntax</span></span>

```vb
VALUE (text)
```

## <a name="arguments"></a><span data-ttu-id="c0c6b-106">Argumentit</span><span class="sxs-lookup"><span data-stu-id="c0c6b-106">Arguments</span></span>

<span data-ttu-id="c0c6b-107">`text`: *Merkkijono*</span><span class="sxs-lookup"><span data-stu-id="c0c6b-107">`text`: *String*</span></span>

<span data-ttu-id="c0c6b-108">Merkkijonon arvo, jota ei pidä muuntaa numeroarvoon.</span><span class="sxs-lookup"><span data-stu-id="c0c6b-108">A string value that must be converted to a numeric value.</span></span>

## <a name="return-values"></a><span data-ttu-id="c0c6b-109">Palautusarvot</span><span class="sxs-lookup"><span data-stu-id="c0c6b-109">Return values</span></span>

<span data-ttu-id="c0c6b-110">*Reaaliluku*</span><span class="sxs-lookup"><span data-stu-id="c0c6b-110">*Real*</span></span>

<span data-ttu-id="c0c6b-111">Tuloksena oleva numeroarvo.</span><span class="sxs-lookup"><span data-stu-id="c0c6b-111">The resulting numeric value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="c0c6b-112">Käyttöhuomautukset</span><span class="sxs-lookup"><span data-stu-id="c0c6b-112">Usage notes</span></span>

<span data-ttu-id="c0c6b-113">Pilkkuja ja pisteitä (.) pidetään desimaalierottimina. Alussa olevaa tavuviivaa (-) pidetään miinusmerkkinä.</span><span class="sxs-lookup"><span data-stu-id="c0c6b-113">Commas and dot characters (.) are considered decimal separators, and a leading hyphen (-) is used as a negative sign.</span></span> <span data-ttu-id="c0c6b-114">Poikkeus annetaan suorituksen aikana, jos määritetyssä merkkijonossa on muita kuin numeerisia merkkejä.</span><span class="sxs-lookup"><span data-stu-id="c0c6b-114">An exception is thrown at runtime if the specified string contains other non-numeric characters.</span></span>

## <a name="example-1"></a><span data-ttu-id="c0c6b-115">Esimerkki 1</span><span class="sxs-lookup"><span data-stu-id="c0c6b-115">Example 1</span></span>

<span data-ttu-id="c0c6b-116">`VALUE ("1 234,56")` antaa poikkeuksen.</span><span class="sxs-lookup"><span data-stu-id="c0c6b-116">`VALUE ("1 234,56")` throws an exception.</span></span>

## <a name="example-2"></a><span data-ttu-id="c0c6b-117">Esimerkki 2</span><span class="sxs-lookup"><span data-stu-id="c0c6b-117">Example 2</span></span>

<span data-ttu-id="c0c6b-118">`VALUE ("1234,56")` palauttaa **1234.56**.</span><span class="sxs-lookup"><span data-stu-id="c0c6b-118">`VALUE ("1234,56")` returns **1234.56**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="c0c6b-119">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="c0c6b-119">Additional resources</span></span>

[<span data-ttu-id="c0c6b-120">Tyypin muuntamisen toiminnot</span><span class="sxs-lookup"><span data-stu-id="c0c6b-120">Type conversion functions</span></span>](er-functions-category-type-conversion.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]