---
title: CONCATENATE ER-funktio
description: Tässä ohjeaiheessa on tietoja siitä, miten sähköisen raportoinnin (ER) CONCATENATE-funktiota käytetään
author: NickSelin
manager: kfend
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
ms.openlocfilehash: 6e4800ce44d9da07818acec55c50224a9a000fe6
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/09/2021
ms.locfileid: "5569602"
---
# <a name="concatenate-er-function"></a><span data-ttu-id="bd8a9-103">CONCATENATE ER-funktio</span><span class="sxs-lookup"><span data-stu-id="bd8a9-103">CONCATENATE ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="bd8a9-104">`CONCATENATE`-funktio palauttaa kaikki määritetyt tekstimerkkijonot *Merkkijono*-arvona sen jälkeen, kun ne on liitetty yhdeksi merkkijonoksi.</span><span class="sxs-lookup"><span data-stu-id="bd8a9-104">The `CONCATENATE` function returns all the specified text strings as a *String* value after they have been joined into one string.</span></span>

## <a name="syntax"></a><span data-ttu-id="bd8a9-105">Syntaksi</span><span class="sxs-lookup"><span data-stu-id="bd8a9-105">Syntax</span></span>

```vb
CONCATENATE (text 1[, text 2, …, text N])
```

## <a name="arguments"></a><span data-ttu-id="bd8a9-106">Argumentit</span><span class="sxs-lookup"><span data-stu-id="bd8a9-106">Arguments</span></span>

<span data-ttu-id="bd8a9-107">`text 1`: *Merkkijono*</span><span class="sxs-lookup"><span data-stu-id="bd8a9-107">`text 1`: *String*</span></span>

<span data-ttu-id="bd8a9-108">Viittaus *Merkkijonon* tietotyypin tietolähteeseen.</span><span class="sxs-lookup"><span data-stu-id="bd8a9-108">A reference to a data source of the *String* data type.</span></span> <span data-ttu-id="bd8a9-109">Tämä argumentti on pakollinen.</span><span class="sxs-lookup"><span data-stu-id="bd8a9-109">This argument is required.</span></span>

<span data-ttu-id="bd8a9-110">`text N`: *Merkkijono*</span><span class="sxs-lookup"><span data-stu-id="bd8a9-110">`text N`: *String*</span></span>

<span data-ttu-id="bd8a9-111">Viittaus *Merkkijonon* tietotyypin tietolähteeseen.</span><span class="sxs-lookup"><span data-stu-id="bd8a9-111">A reference to a data source of the *String* data type.</span></span> <span data-ttu-id="bd8a9-112">Nämä lisäargumentit ovat valinnaisia.</span><span class="sxs-lookup"><span data-stu-id="bd8a9-112">These additional arguments are optional.</span></span>

## <a name="return-values"></a><span data-ttu-id="bd8a9-113">Palautusarvot</span><span class="sxs-lookup"><span data-stu-id="bd8a9-113">Return values</span></span>

<span data-ttu-id="bd8a9-114">*merkkijono*</span><span class="sxs-lookup"><span data-stu-id="bd8a9-114">*String*</span></span>

<span data-ttu-id="bd8a9-115">Tulokseksi saatava tekstiarvo.</span><span class="sxs-lookup"><span data-stu-id="bd8a9-115">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="bd8a9-116">Esimerkki</span><span class="sxs-lookup"><span data-stu-id="bd8a9-116">Example</span></span>

<span data-ttu-id="bd8a9-117">`CONCATENATE ("abc", "def")`-funktio palauttaa arvon **abcdef**.</span><span class="sxs-lookup"><span data-stu-id="bd8a9-117">`CONCATENATE ("abc", "def")` returns **"abcdef"**.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="bd8a9-118">Käyttöhuomautukset</span><span class="sxs-lookup"><span data-stu-id="bd8a9-118">Usage notes</span></span>

<span data-ttu-id="bd8a9-119">Myös lauseke `"abc" & "def"` palauttaa lausekkeen **abcdef**.</span><span class="sxs-lookup"><span data-stu-id="bd8a9-119">The expression `"abc" & "def"` also returns **"abcdef"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="bd8a9-120">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="bd8a9-120">Additional resources</span></span>

[<span data-ttu-id="bd8a9-121">Tekstitoiminnot</span><span class="sxs-lookup"><span data-stu-id="bd8a9-121">Text functions</span></span>](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]