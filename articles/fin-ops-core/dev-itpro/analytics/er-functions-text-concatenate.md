---
title: CONCATENATE ER-funktio
description: Tässä ohjeaiheessa on tietoja siitä, miten sähköisen raportoinnin (ER) CONCATENATE-funktiota käytetään
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
ms.openlocfilehash: 04c7b32e2a9578f8864570a552817ec3ce28fa43
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/12/2020
ms.locfileid: "3041157"
---
# <span data-ttu-id="c9f14-103"><a name="CONCATENATE">CONCATENATE ER-funktio</a></span><span class="sxs-lookup"><span data-stu-id="c9f14-103"><a name="CONCATENATE">CONCATENATE ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c9f14-104">`CONCATENATE`-funktio palauttaa kaikki määritetyt tekstimerkkijonot *Merkkijono*-arvona sen jälkeen, kun ne on liitetty yhdeksi merkkijonoksi.</span><span class="sxs-lookup"><span data-stu-id="c9f14-104">The `CONCATENATE` function returns all the specified text strings as a *String* value after they have been joined into one string.</span></span>

## <a name="syntax"></a><span data-ttu-id="c9f14-105">Syntaksi</span><span class="sxs-lookup"><span data-stu-id="c9f14-105">Syntax</span></span>

```vb
CONCATENATE (text 1[, text 2, …, text N])
```

## <a name="arguments"></a><span data-ttu-id="c9f14-106">Argumentit</span><span class="sxs-lookup"><span data-stu-id="c9f14-106">Arguments</span></span>

<span data-ttu-id="c9f14-107">`text 1`: *Merkkijono*</span><span class="sxs-lookup"><span data-stu-id="c9f14-107">`text 1`: *String*</span></span>

<span data-ttu-id="c9f14-108">Viittaus *Merkkijonon* tietotyypin tietolähteeseen.</span><span class="sxs-lookup"><span data-stu-id="c9f14-108">A reference to a data source of the *String* data type.</span></span> <span data-ttu-id="c9f14-109">Tämä argumentti on pakollinen.</span><span class="sxs-lookup"><span data-stu-id="c9f14-109">This argument is required.</span></span>

<span data-ttu-id="c9f14-110">`text N`: *Merkkijono*</span><span class="sxs-lookup"><span data-stu-id="c9f14-110">`text N`: *String*</span></span>

<span data-ttu-id="c9f14-111">Viittaus *Merkkijonon* tietotyypin tietolähteeseen.</span><span class="sxs-lookup"><span data-stu-id="c9f14-111">A reference to a data source of the *String* data type.</span></span> <span data-ttu-id="c9f14-112">Nämä lisäargumentit ovat valinnaisia.</span><span class="sxs-lookup"><span data-stu-id="c9f14-112">These additional arguments are optional.</span></span>

## <a name="return-values"></a><span data-ttu-id="c9f14-113">Palautusarvot</span><span class="sxs-lookup"><span data-stu-id="c9f14-113">Return values</span></span>

<span data-ttu-id="c9f14-114">*merkkijono*</span><span class="sxs-lookup"><span data-stu-id="c9f14-114">*String*</span></span>

<span data-ttu-id="c9f14-115">Tulokseksi saatava tekstiarvo.</span><span class="sxs-lookup"><span data-stu-id="c9f14-115">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="c9f14-116">Esimerkki</span><span class="sxs-lookup"><span data-stu-id="c9f14-116">Example</span></span>

<span data-ttu-id="c9f14-117">`CONCATENATE ("abc", "def")`-funktio palauttaa arvon **abcdef**.</span><span class="sxs-lookup"><span data-stu-id="c9f14-117">`CONCATENATE ("abc", "def")` returns **"abcdef"**.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="c9f14-118">Käyttöhuomautukset</span><span class="sxs-lookup"><span data-stu-id="c9f14-118">Usage notes</span></span>

<span data-ttu-id="c9f14-119">Myös lauseke `"abc" & "def"` palauttaa lausekkeen **abcdef**.</span><span class="sxs-lookup"><span data-stu-id="c9f14-119">The expression `"abc" & "def"` also returns **"abcdef"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="c9f14-120">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="c9f14-120">Additional resources</span></span>

[<span data-ttu-id="c9f14-121">Tekstitoiminnot</span><span class="sxs-lookup"><span data-stu-id="c9f14-121">Text functions</span></span>](er-functions-category-text.md)
