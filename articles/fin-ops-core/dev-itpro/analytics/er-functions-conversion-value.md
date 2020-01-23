---
title: VALUE ER -funktio
description: Tässä ohjeaiheessa on tietoja siitä, miten sähköisen raportoinnin (ER) VALUE-funktiota käytetään.
author: NickSelin
manager: kfend
ms.date: 12/05/2019
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
ms.openlocfilehash: 160dd81baa43702b2deea1e3eea20080fca122ca
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/20/2019
ms.locfileid: "2917623"
---
# <span data-ttu-id="62020-103"><a name="VALUE">VALUE ER -funktio</a></span><span class="sxs-lookup"><span data-stu-id="62020-103"><a name="VALUE">VALUE ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="62020-104">`VALUE`-funktio palauttaa *todellisen* arvon, joka muunnetaan määritetystä merkkijonosta.</span><span class="sxs-lookup"><span data-stu-id="62020-104">The `VALUE` function returns a *Real* value that is converted from the specified string.</span></span>

## <a name="syntax"></a><span data-ttu-id="62020-105">Syntaksi</span><span class="sxs-lookup"><span data-stu-id="62020-105">Syntax</span></span>

```
VALUE (text)
```

## <a name="arguments"></a><span data-ttu-id="62020-106">Argumentit</span><span class="sxs-lookup"><span data-stu-id="62020-106">Arguments</span></span>

<span data-ttu-id="62020-107">`text`: *Merkkijono*</span><span class="sxs-lookup"><span data-stu-id="62020-107">`text`: *String*</span></span>

<span data-ttu-id="62020-108">Merkkijonon arvo, jota ei pidä muuntaa numeroarvoon.</span><span class="sxs-lookup"><span data-stu-id="62020-108">A string value that must be converted to a numeric value.</span></span>

## <a name="return-values"></a><span data-ttu-id="62020-109">Palautusarvot</span><span class="sxs-lookup"><span data-stu-id="62020-109">Return values</span></span>

<span data-ttu-id="62020-110">*Reaaliluku*</span><span class="sxs-lookup"><span data-stu-id="62020-110">*Real*</span></span>

<span data-ttu-id="62020-111">Tuloksena oleva numeroarvo.</span><span class="sxs-lookup"><span data-stu-id="62020-111">The resulting numeric value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="62020-112">Käyttöhuomautukset</span><span class="sxs-lookup"><span data-stu-id="62020-112">Usage notes</span></span>

<span data-ttu-id="62020-113">Pilkkuja ja pisteitä (.) pidetään desimaalierottimina. Alussa olevaa tavuviivaa (-) pidetään miinusmerkkinä.</span><span class="sxs-lookup"><span data-stu-id="62020-113">Commas and dot characters (.) are considered decimal separators, and a leading hyphen (-) is used as a negative sign.</span></span> <span data-ttu-id="62020-114">Poikkeus annetaan suorituksen aikana, jos määritetyssä merkkijonossa on muita kuin numeerisia merkkejä.</span><span class="sxs-lookup"><span data-stu-id="62020-114">An exception is thrown at runtime if the specified string contains other non-numeric characters.</span></span>

## <a name="example-1"></a><span data-ttu-id="62020-115">Esimerkki 1</span><span class="sxs-lookup"><span data-stu-id="62020-115">Example 1</span></span>

<span data-ttu-id="62020-116">`VALUE ("1 234,56")` antaa poikkeuksen.</span><span class="sxs-lookup"><span data-stu-id="62020-116">`VALUE ("1 234,56")` throws an exception.</span></span>

## <a name="example-2"></a><span data-ttu-id="62020-117">Esimerkki 2</span><span class="sxs-lookup"><span data-stu-id="62020-117">Example 2</span></span>

<span data-ttu-id="62020-118">`VALUE ("1234,56")` palauttaa **1234.56**.</span><span class="sxs-lookup"><span data-stu-id="62020-118">`VALUE ("1234,56")` returns **1234.56**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="62020-119">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="62020-119">Additional resources</span></span>

[<span data-ttu-id="62020-120">Tyypin muuntamisen toiminnot</span><span class="sxs-lookup"><span data-stu-id="62020-120">Type conversion functions</span></span>](er-functions-category-type-conversion.md)
