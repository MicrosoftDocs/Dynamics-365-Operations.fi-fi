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
ms.openlocfilehash: c90772ca1e93500ac45cc52ba92d4169c4d29bad
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/12/2020
ms.locfileid: "3042616"
---
# <span data-ttu-id="71908-103"><a name="VALUE">VALUE ER -funktio</a></span><span class="sxs-lookup"><span data-stu-id="71908-103"><a name="VALUE">VALUE ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="71908-104">`VALUE`-funktio palauttaa *todellisen* arvon, joka muunnetaan määritetystä merkkijonosta.</span><span class="sxs-lookup"><span data-stu-id="71908-104">The `VALUE` function returns a *Real* value that is converted from the specified string.</span></span>

## <a name="syntax"></a><span data-ttu-id="71908-105">Syntaksi</span><span class="sxs-lookup"><span data-stu-id="71908-105">Syntax</span></span>

```vb
VALUE (text)
```

## <a name="arguments"></a><span data-ttu-id="71908-106">Argumentit</span><span class="sxs-lookup"><span data-stu-id="71908-106">Arguments</span></span>

<span data-ttu-id="71908-107">`text`: *Merkkijono*</span><span class="sxs-lookup"><span data-stu-id="71908-107">`text`: *String*</span></span>

<span data-ttu-id="71908-108">Merkkijonon arvo, jota ei pidä muuntaa numeroarvoon.</span><span class="sxs-lookup"><span data-stu-id="71908-108">A string value that must be converted to a numeric value.</span></span>

## <a name="return-values"></a><span data-ttu-id="71908-109">Palautusarvot</span><span class="sxs-lookup"><span data-stu-id="71908-109">Return values</span></span>

<span data-ttu-id="71908-110">*Reaaliluku*</span><span class="sxs-lookup"><span data-stu-id="71908-110">*Real*</span></span>

<span data-ttu-id="71908-111">Tuloksena oleva numeroarvo.</span><span class="sxs-lookup"><span data-stu-id="71908-111">The resulting numeric value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="71908-112">Käyttöhuomautukset</span><span class="sxs-lookup"><span data-stu-id="71908-112">Usage notes</span></span>

<span data-ttu-id="71908-113">Pilkkuja ja pisteitä (.) pidetään desimaalierottimina. Alussa olevaa tavuviivaa (-) pidetään miinusmerkkinä.</span><span class="sxs-lookup"><span data-stu-id="71908-113">Commas and dot characters (.) are considered decimal separators, and a leading hyphen (-) is used as a negative sign.</span></span> <span data-ttu-id="71908-114">Poikkeus annetaan suorituksen aikana, jos määritetyssä merkkijonossa on muita kuin numeerisia merkkejä.</span><span class="sxs-lookup"><span data-stu-id="71908-114">An exception is thrown at runtime if the specified string contains other non-numeric characters.</span></span>

## <a name="example-1"></a><span data-ttu-id="71908-115">Esimerkki 1</span><span class="sxs-lookup"><span data-stu-id="71908-115">Example 1</span></span>

<span data-ttu-id="71908-116">`VALUE ("1 234,56")` antaa poikkeuksen.</span><span class="sxs-lookup"><span data-stu-id="71908-116">`VALUE ("1 234,56")` throws an exception.</span></span>

## <a name="example-2"></a><span data-ttu-id="71908-117">Esimerkki 2</span><span class="sxs-lookup"><span data-stu-id="71908-117">Example 2</span></span>

<span data-ttu-id="71908-118">`VALUE ("1234,56")` palauttaa **1234.56**.</span><span class="sxs-lookup"><span data-stu-id="71908-118">`VALUE ("1234,56")` returns **1234.56**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="71908-119">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="71908-119">Additional resources</span></span>

[<span data-ttu-id="71908-120">Tyypin muuntamisen toiminnot</span><span class="sxs-lookup"><span data-stu-id="71908-120">Type conversion functions</span></span>](er-functions-category-type-conversion.md)
