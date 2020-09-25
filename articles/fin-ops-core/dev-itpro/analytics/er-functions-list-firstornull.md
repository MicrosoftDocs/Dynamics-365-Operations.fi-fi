---
title: FIRSTORNULL ER-funktio
description: Tämä ohjeaihe kertoo, miten sähköisen raportoinnin (ER) FIRSTORNULL-funktiota käytetään
author: NickSelin
manager: kfend
ms.date: 11/29/2019
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
ms.openlocfilehash: e360812c5b0dbfb8df4ab279bf3e0050acebbb25
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/01/2020
ms.locfileid: "3745197"
---
# <a name="firstornull-er-function"></a><span data-ttu-id="01754-103">FIRSTORNULL ER-funktio</span><span class="sxs-lookup"><span data-stu-id="01754-103">FIRSTORNULL ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="01754-104">`FIRSTORNULL` funktio palauttaa ensimmäisen tietueen, joka on määritetty *Säilön (tietueen)* arvona, jos tietue ei ole tyhjä.</span><span class="sxs-lookup"><span data-stu-id="01754-104">The `FIRSTORNULL` function returns the first record of the specified list as a *Container (record)* value, if that record isn't empty.</span></span> <span data-ttu-id="01754-105">Jos tietue on tyhjä, funktio palauttaa Null *Säilö (tietue)*-arvon.</span><span class="sxs-lookup"><span data-stu-id="01754-105">If the record is empty, this function returns a null *Container (record)* value.</span></span>

## <a name="syntax"></a><span data-ttu-id="01754-106">Syntaksi</span><span class="sxs-lookup"><span data-stu-id="01754-106">Syntax</span></span>

```vb
FIRSTORNULL (list)
```

## <a name="arguments"></a><span data-ttu-id="01754-107">Argumentit</span><span class="sxs-lookup"><span data-stu-id="01754-107">Arguments</span></span>

<span data-ttu-id="01754-108">`list`: *Tietueluettelo*</span><span class="sxs-lookup"><span data-stu-id="01754-108">`list`: *Record list*</span></span>

<span data-ttu-id="01754-109">*Tietueluettelo*-tietotyypin tietolähteen kelvollinen polku.</span><span class="sxs-lookup"><span data-stu-id="01754-109">The valid path of a data source of the *Record list* data type.</span></span>

## <a name="return-values"></a><span data-ttu-id="01754-110">Palautusarvot</span><span class="sxs-lookup"><span data-stu-id="01754-110">Return values</span></span>

<span data-ttu-id="01754-111">*Kontti (tietue)*</span><span class="sxs-lookup"><span data-stu-id="01754-111">*Container (record)*</span></span>

<span data-ttu-id="01754-112">Tuloksena oleva tietueen arvo.</span><span class="sxs-lookup"><span data-stu-id="01754-112">The resulting record value.</span></span>

## <a name="example"></a><span data-ttu-id="01754-113">Esimerkki</span><span class="sxs-lookup"><span data-stu-id="01754-113">Example</span></span>

<span data-ttu-id="01754-114">Lauseke `FIRSTORNULL(SPLIT("",1)).Value` palauttaa tyhjän merkkijonon (**""**).</span><span class="sxs-lookup"><span data-stu-id="01754-114">The expression `FIRSTORNULL(SPLIT("",1)).Value` returns an empty string (**""**).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="01754-115">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="01754-115">Additional resources</span></span>

[<span data-ttu-id="01754-116">Luettelotoiminnot</span><span class="sxs-lookup"><span data-stu-id="01754-116">List functions</span></span>](er-functions-category-list.md)
