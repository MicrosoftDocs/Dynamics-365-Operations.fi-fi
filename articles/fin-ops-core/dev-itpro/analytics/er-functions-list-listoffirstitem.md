---
title: LISTOFFIRSTITEM ER-funktio
description: Tässä ohjeaiheessa on tietoja siitä, miten sähköisen raportoinnin (ER) LISTOFFIRSTITEM-funktiota käytetään.
author: NickSelin
manager: kfend
ms.date: 12/12/2019
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
ms.openlocfilehash: 8cd48732280c9af0b89129a32b42285207f97fb7
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/12/2020
ms.locfileid: "3041972"
---
# <span data-ttu-id="e2e12-103"><a name="LISTOFFIRSTITEM">LISTOFFIRSTITEM ER-funktio</a></span><span class="sxs-lookup"><span data-stu-id="e2e12-103"><a name="LISTOFFIRSTITEM">LISTOFFIRSTITEM ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e2e12-104">`LISTOFFIRSTITEM`-funktio palauttaa uuden *Tietueluettelon* arvon, joka koostuu vain määritetyn luettelon ensimmäisestä tietueesta.</span><span class="sxs-lookup"><span data-stu-id="e2e12-104">The `LISTOFFIRSTITEM` function returns a *Record list* value that consists of only the first record of the specified list.</span></span>

## <a name="syntax"></a><span data-ttu-id="e2e12-105">Syntaksi</span><span class="sxs-lookup"><span data-stu-id="e2e12-105">Syntax</span></span>

```vb
LISTOFFIRSTITEM (list)
```

## <a name="arguments"></a><span data-ttu-id="e2e12-106">Argumentit</span><span class="sxs-lookup"><span data-stu-id="e2e12-106">Arguments</span></span>

<span data-ttu-id="e2e12-107">`list`: *Tietueluettelo*</span><span class="sxs-lookup"><span data-stu-id="e2e12-107">`list`: *Record list*</span></span>

<span data-ttu-id="e2e12-108">*Tietueluettelo*-tietotyypin tietolähteen kelvollinen polku.</span><span class="sxs-lookup"><span data-stu-id="e2e12-108">The valid path of a data source of the *Record list* data type.</span></span>

## <a name="return-values"></a><span data-ttu-id="e2e12-109">Palautusarvot</span><span class="sxs-lookup"><span data-stu-id="e2e12-109">Return values</span></span>

<span data-ttu-id="e2e12-110">*Tietueluettelo*</span><span class="sxs-lookup"><span data-stu-id="e2e12-110">*Record list*</span></span>

<span data-ttu-id="e2e12-111">Tuloksena oleva tietueluettelo.</span><span class="sxs-lookup"><span data-stu-id="e2e12-111">The resulting list of records.</span></span>

## <a name="example"></a><span data-ttu-id="e2e12-112">Esimerkki</span><span class="sxs-lookup"><span data-stu-id="e2e12-112">Example</span></span>

<span data-ttu-id="e2e12-113">Lauseke `FIRST( LISTOFFIRSTITEM ( SPLIT ("ABC",1))).Value` palauttaa tekstiarvon **"A"**.</span><span class="sxs-lookup"><span data-stu-id="e2e12-113">The expression `FIRST( LISTOFFIRSTITEM ( SPLIT ("ABC",1))).Value` returns the text value **"A"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="e2e12-114">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="e2e12-114">Additional resources</span></span>

[<span data-ttu-id="e2e12-115">Luettelotoiminnot</span><span class="sxs-lookup"><span data-stu-id="e2e12-115">List functions</span></span>](er-functions-category-list.md)
