---
title: LOWER ER-toiminto
description: Tässä ohjeaiheessa on tietoja siitä, miten sähköisen raportoinnin (ER) LOWER-funktiota käytetään.
author: NickSelin
manager: kfend
ms.date: 12/11/2019
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
ms.openlocfilehash: 6784384bac31d8c7cdc9c6f71b7dbab79c15a934
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/12/2020
ms.locfileid: "3041098"
---
# <span data-ttu-id="7c489-103"><a name="LOWER">LOWER ER-toiminto</a></span><span class="sxs-lookup"><span data-stu-id="7c489-103"><a name="LOWER">LOWER ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7c489-104">`LOWER`-funktio palauttaa määritetyn tekstimerkkijonon *Merkkijono*-arvona sen jälkeen, kun se on muunnettu pieniksi kirjaimiksi.</span><span class="sxs-lookup"><span data-stu-id="7c489-104">The `LOWER` function returns the specified text string as a *String* value after it has been converted to lowercase letters.</span></span>

## <a name="syntax"></a><span data-ttu-id="7c489-105">Syntaksi</span><span class="sxs-lookup"><span data-stu-id="7c489-105">Syntax</span></span>

```vb
LOWER (text)
```

## <a name="arguments"></a><span data-ttu-id="7c489-106">Argumentit</span><span class="sxs-lookup"><span data-stu-id="7c489-106">Arguments</span></span>

<span data-ttu-id="7c489-107">`text`: *Merkkijono*</span><span class="sxs-lookup"><span data-stu-id="7c489-107">`text`: *String*</span></span>

<span data-ttu-id="7c489-108">*Merkkijono*-arvo, joka määrittää tekstin.</span><span class="sxs-lookup"><span data-stu-id="7c489-108">A *String* value that specifies the text.</span></span>

## <a name="return-values"></a><span data-ttu-id="7c489-109">Palautusarvot</span><span class="sxs-lookup"><span data-stu-id="7c489-109">Return values</span></span>

<span data-ttu-id="7c489-110">*merkkijono*</span><span class="sxs-lookup"><span data-stu-id="7c489-110">*String*</span></span>

<span data-ttu-id="7c489-111">Tulokseksi saatava tekstiarvo.</span><span class="sxs-lookup"><span data-stu-id="7c489-111">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="7c489-112">Esimerkki</span><span class="sxs-lookup"><span data-stu-id="7c489-112">Example</span></span>

<span data-ttu-id="7c489-113">`LOWER ("Sample")` palauttaa arvon **Malli**.</span><span class="sxs-lookup"><span data-stu-id="7c489-113">`LOWER ("Sample")` returns **"sample"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="7c489-114">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="7c489-114">Additional resources</span></span>

[<span data-ttu-id="7c489-115">Tekstitoiminnot</span><span class="sxs-lookup"><span data-stu-id="7c489-115">Text functions</span></span>](er-functions-category-text.md)
