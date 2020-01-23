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
ms.openlocfilehash: a60bc948ff6223b6e3acccd0ba40bf64f238aac2
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/20/2019
ms.locfileid: "2917393"
---
# <span data-ttu-id="2ca5e-103"><a name="EMPTYLIST">EMPTYLIST ER-funktio</a></span><span class="sxs-lookup"><span data-stu-id="2ca5e-103"><a name="EMPTYLIST">EMPTYLIST ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2ca5e-104">`EMPTYLIST` funktio palauttaa tyhjän *Tietueluettelon* arvon käyttämällä määritettyä luetteloa luettelorakenteen lähteenä.</span><span class="sxs-lookup"><span data-stu-id="2ca5e-104">The `EMPTYLIST` function returns an empty *Record list* value by using the specified list as a source for the list structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="2ca5e-105">Syntaksi</span><span class="sxs-lookup"><span data-stu-id="2ca5e-105">Syntax</span></span>

```
EMPTYLIST (list)
```

## <a name="arguments"></a><span data-ttu-id="2ca5e-106">Argumentit</span><span class="sxs-lookup"><span data-stu-id="2ca5e-106">Arguments</span></span>

<span data-ttu-id="2ca5e-107">`list`: *Tietueluettelo*</span><span class="sxs-lookup"><span data-stu-id="2ca5e-107">`list`: *Record list*</span></span>

<span data-ttu-id="2ca5e-108">*Tietueluettelo*-tietotyypin tietolähteen kelvollinen polku.</span><span class="sxs-lookup"><span data-stu-id="2ca5e-108">The valid path of a data source of the *Record list* data type.</span></span>

## <a name="return-values"></a><span data-ttu-id="2ca5e-109">Palautusarvot</span><span class="sxs-lookup"><span data-stu-id="2ca5e-109">Return values</span></span>

<span data-ttu-id="2ca5e-110">*Tietueluettelo*</span><span class="sxs-lookup"><span data-stu-id="2ca5e-110">*Record list*</span></span>

<span data-ttu-id="2ca5e-111">Tuloksena oleva tietueluettelo.</span><span class="sxs-lookup"><span data-stu-id="2ca5e-111">The resulting list of records.</span></span>

## <a name="example"></a><span data-ttu-id="2ca5e-112">Esimerkki</span><span class="sxs-lookup"><span data-stu-id="2ca5e-112">Example</span></span>

<span data-ttu-id="2ca5e-113">`EMPTYLIST (SPLIT ("abc", 1))` palauttaa uuden tyhjän luettelon, jonka rakenne on sama kuin `SPLIT`-toiminnon palauttamalla luettelolla.</span><span class="sxs-lookup"><span data-stu-id="2ca5e-113">`EMPTYLIST (SPLIT ("abc", 1))` returns a new empty list that has the same structure as the list that is returned by the `SPLIT` function that is used.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="2ca5e-114">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="2ca5e-114">Additional resources</span></span>

[<span data-ttu-id="2ca5e-115">Luettelotoiminnot</span><span class="sxs-lookup"><span data-stu-id="2ca5e-115">List functions</span></span>](er-functions-category-list.md)
