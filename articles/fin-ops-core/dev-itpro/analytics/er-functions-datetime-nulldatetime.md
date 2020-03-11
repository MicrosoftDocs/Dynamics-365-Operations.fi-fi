---
title: NULLDATETIME ER-funktio
description: Tässä ohjeaiheessa on tietoja siitä, miten sähköisen raportoinnin (ER) NULLDATETIME-funktiota käytetään.
author: NickSelin
manager: kfend
ms.date: 12/04/2019
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
ms.openlocfilehash: 3cd4c152d4e220a2f6315265ed5e44d148134279
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/12/2020
ms.locfileid: "3042251"
---
# <span data-ttu-id="a145e-103"><a name="NULLDATETIME">NULLDATETIME ER-funktio</a></span><span class="sxs-lookup"><span data-stu-id="a145e-103"><a name="NULLDATETIME">NULLDATETIME ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a145e-104">`NULLDATETIME`-funktio palauttaa *DateTime*-arvon, joka edustaa **Null**-arvoista päivämäärä- ja aika-arvoa (1. tammikuuta 1900) koordinoituun yleisaikaan (Greenwichin keskimääräinen aika \[GMT\]).</span><span class="sxs-lookup"><span data-stu-id="a145e-104">The `NULLDATETIME` function returns a *DateTime* value that represents the **null** date/time value (January 1, 1900) in Coordinated Universal Time (Greenwich Mean Time \[GMT\]).</span></span>

## <a name="syntax"></a><span data-ttu-id="a145e-105">Syntaksi</span><span class="sxs-lookup"><span data-stu-id="a145e-105">Syntax</span></span>

```vb
NULLDATETIME ()
```

## <a name="return-values"></a><span data-ttu-id="a145e-106">Palautusarvot</span><span class="sxs-lookup"><span data-stu-id="a145e-106">Return values</span></span>

<span data-ttu-id="a145e-107">*DateTime*</span><span class="sxs-lookup"><span data-stu-id="a145e-107">*DateTime*</span></span>

<span data-ttu-id="a145e-108">Tulokseksi saatava päivämäärä-/aika-arvo.</span><span class="sxs-lookup"><span data-stu-id="a145e-108">The resulting date/time value.</span></span>

## <a name="example"></a><span data-ttu-id="a145e-109">Esimerkki</span><span class="sxs-lookup"><span data-stu-id="a145e-109">Example</span></span>

<span data-ttu-id="a145e-110">`DATETIMEFORMAT( NULLDATETIME(), "O")` palauttaa merkkijonon arvon **1900-01-01T00:00:00.0000000+00:00**, kun sitä kutsutaan prosessin aikana, jonka on käynnistänyt sovelluskäyttäjä, jolla on aikavyöhyke arvo **(GMT) koordinoituun yleisaikaan** **kieli ja maa/alue-asetukset** -osassa.</span><span class="sxs-lookup"><span data-stu-id="a145e-110">`DATETIMEFORMAT( NULLDATETIME(), "O")` returns the string value **1900-01-01T00:00:00.0000000+00:00** when it's called during a process that was initiated by an application user who has the time zone value **(GMT) Coordinated Universal Time** in the **Language and country/region preferences** section.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="a145e-111">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="a145e-111">Additional resources</span></span>

[<span data-ttu-id="a145e-112">Päivämäärä- ja aikatoiminnot</span><span class="sxs-lookup"><span data-stu-id="a145e-112">Date and time functions</span></span>](er-functions-category-datetime.md)
