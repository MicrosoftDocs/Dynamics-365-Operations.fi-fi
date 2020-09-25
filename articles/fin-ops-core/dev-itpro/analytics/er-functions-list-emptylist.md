---
title: EMPTYLIST ER-funktio
description: Tässä ohjeaiheessa on tietoja siitä, miten sähköisen raportoinnin (ER) EMPTYLIST-funktiota käytetään.
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
ms.openlocfilehash: 747b661d0dee4e9c27741e167c89f9ef7eefa470
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/01/2020
ms.locfileid: "3745318"
---
# <a name="emptylist-er-function"></a><span data-ttu-id="d1110-103">EMPTYLIST ER-funktio</span><span class="sxs-lookup"><span data-stu-id="d1110-103">EMPTYLIST ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d1110-104">`EMPTYLIST` funktio palauttaa tyhjän *Tietueluettelon* arvon käyttämällä määritettyä luetteloa luettelorakenteen lähteenä.</span><span class="sxs-lookup"><span data-stu-id="d1110-104">The `EMPTYLIST` function returns an empty *Record list* value by using the specified list as a source for the list structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="d1110-105">Syntaksi</span><span class="sxs-lookup"><span data-stu-id="d1110-105">Syntax</span></span>

```vb
EMPTYLIST (list)
```

## <a name="arguments"></a><span data-ttu-id="d1110-106">Argumentit</span><span class="sxs-lookup"><span data-stu-id="d1110-106">Arguments</span></span>

<span data-ttu-id="d1110-107">`list`: *Tietueluettelo*</span><span class="sxs-lookup"><span data-stu-id="d1110-107">`list`: *Record list*</span></span>

<span data-ttu-id="d1110-108">*Tietueluettelo*-tietotyypin tietolähteen kelvollinen polku.</span><span class="sxs-lookup"><span data-stu-id="d1110-108">The valid path of a data source of the *Record list* data type.</span></span>

## <a name="return-values"></a><span data-ttu-id="d1110-109">Palautusarvot</span><span class="sxs-lookup"><span data-stu-id="d1110-109">Return values</span></span>

<span data-ttu-id="d1110-110">*Tietueluettelo*</span><span class="sxs-lookup"><span data-stu-id="d1110-110">*Record list*</span></span>

<span data-ttu-id="d1110-111">Tuloksena oleva tietueluettelo.</span><span class="sxs-lookup"><span data-stu-id="d1110-111">The resulting list of records.</span></span>

## <a name="example"></a><span data-ttu-id="d1110-112">Esimerkki</span><span class="sxs-lookup"><span data-stu-id="d1110-112">Example</span></span>

<span data-ttu-id="d1110-113">`EMPTYLIST (SPLIT ("abc", 1))` palauttaa uuden tyhjän luettelon, jonka rakenne on sama kuin `SPLIT`-toiminnon palauttamalla luettelolla.</span><span class="sxs-lookup"><span data-stu-id="d1110-113">`EMPTYLIST (SPLIT ("abc", 1))` returns a new empty list that has the same structure as the list that is returned by the `SPLIT` function that is used.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="d1110-114">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="d1110-114">Additional resources</span></span>

[<span data-ttu-id="d1110-115">Luettelotoiminnot</span><span class="sxs-lookup"><span data-stu-id="d1110-115">List functions</span></span>](er-functions-category-list.md)
