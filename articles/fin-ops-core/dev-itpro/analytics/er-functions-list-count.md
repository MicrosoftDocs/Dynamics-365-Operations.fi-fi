---
title: COUNT ER-funktio
description: Tässä ohjeaiheessa on tietoja siitä, miten sähköisen raportoinnin (ER) COUNT-funktiota käytetään.
author: NickSelin
ms.date: 12/12/2019
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
ms.openlocfilehash: a0b780051684ef52d06a9baf78d9b513d9ac1f0e
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2021
ms.locfileid: "5746624"
---
# <a name="count-er-function"></a><span data-ttu-id="84fbc-103">COUNT ER-funktio</span><span class="sxs-lookup"><span data-stu-id="84fbc-103">COUNT ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="84fbc-104">`COUNT`-funktio palauttaa *kokonaisluku*-arvon, joka vastaa määritetyn luettelon tietueiden määrää, jos luettelo ei ole tyhjä.</span><span class="sxs-lookup"><span data-stu-id="84fbc-104">The `COUNT` function returns an *Integer* value that represents the number of records in the specified list, if the list isn't empty.</span></span> <span data-ttu-id="84fbc-105">Jos luettelo on tyhjä, funktio palauttaa arvon **0** (nolla).</span><span class="sxs-lookup"><span data-stu-id="84fbc-105">If the list is empty, this function returns **0** (zero).</span></span>

## <a name="syntax"></a><span data-ttu-id="84fbc-106">Syntaksi</span><span class="sxs-lookup"><span data-stu-id="84fbc-106">Syntax</span></span>

```vb
COUNT (list)
```

## <a name="arguments"></a><span data-ttu-id="84fbc-107">Argumentit</span><span class="sxs-lookup"><span data-stu-id="84fbc-107">Arguments</span></span>

<span data-ttu-id="84fbc-108">`list`: *Tietueluettelo*</span><span class="sxs-lookup"><span data-stu-id="84fbc-108">`list`: *Record list*</span></span>

<span data-ttu-id="84fbc-109">*Tietueluettelo*-tietotyypin tietolähteen kelvollinen polku.</span><span class="sxs-lookup"><span data-stu-id="84fbc-109">The valid path of a data source of the *Record list* data type.</span></span>

## <a name="return-values"></a><span data-ttu-id="84fbc-110">Palautusarvot</span><span class="sxs-lookup"><span data-stu-id="84fbc-110">Return values</span></span>

<span data-ttu-id="84fbc-111">*Kokonaisluku*</span><span class="sxs-lookup"><span data-stu-id="84fbc-111">*Integer*</span></span>

<span data-ttu-id="84fbc-112">Tuloksena oleva numeroarvo.</span><span class="sxs-lookup"><span data-stu-id="84fbc-112">The resulting numeric value.</span></span>

## <a name="example"></a><span data-ttu-id="84fbc-113">Esimerkki</span><span class="sxs-lookup"><span data-stu-id="84fbc-113">Example</span></span>

<span data-ttu-id="84fbc-114">`COUNT (SPLIT("abcd" , 3))` palauttaa arvon **2**, koska tässä esimerkissä käytetty `SPLIT`-funktio luo luettelon, joka koostuu kahdesta tietueesta.</span><span class="sxs-lookup"><span data-stu-id="84fbc-114">`COUNT (SPLIT("abcd" , 3))` returns **2**, because the `SPLIT` function that is used in this example creates a list that consists of two records.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="84fbc-115">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="84fbc-115">Additional resources</span></span>

[<span data-ttu-id="84fbc-116">Luettelotoiminnot</span><span class="sxs-lookup"><span data-stu-id="84fbc-116">List functions</span></span>](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]