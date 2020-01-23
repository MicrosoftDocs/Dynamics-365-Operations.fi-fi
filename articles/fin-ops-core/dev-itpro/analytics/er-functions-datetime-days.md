---
title: DAYS ER -funktio
description: Tässä ohjeaiheessa on tietoja siitä, miten sähköisen raportoinnin (ER) DAYS-funktiota käytetään.
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
ms.openlocfilehash: 4f8c12a22f7654285d5598064473bf86689ed207
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/20/2019
ms.locfileid: "2916289"
---
# <span data-ttu-id="e7301-103"><a name="DAYS">DAYS ER -funktio</a></span><span class="sxs-lookup"><span data-stu-id="e7301-103"><a name="DAYS">DAYS ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e7301-104">`DAYS`-funktio palauttaa ensimmäisen määritetyn päivämäärän ja toisen määritetyn päivämäärän välisten päivien määrää kuvaavan arvon *kokonaislukuna*.</span><span class="sxs-lookup"><span data-stu-id="e7301-104">The `DAYS` function returns an *Integer* value that represents the number of days between one specified date and a second specified date.</span></span>

## <a name="syntax"></a><span data-ttu-id="e7301-105">Syntaksi</span><span class="sxs-lookup"><span data-stu-id="e7301-105">Syntax</span></span>

```
DAYS (date 1, date 2) as Integer
```

## <a name="arguments"></a><span data-ttu-id="e7301-106">Argumentit</span><span class="sxs-lookup"><span data-stu-id="e7301-106">Arguments</span></span>

<span data-ttu-id="e7301-107">`date 1`: *Päivämäärä*</span><span class="sxs-lookup"><span data-stu-id="e7301-107">`date 1`: *Date*</span></span>

<span data-ttu-id="e7301-108">Päivämääräarvo, joka ilmaisee päivien määrän laskennassa käytettävää aloituspäivämäärää.</span><span class="sxs-lookup"><span data-stu-id="e7301-108">A date value that represents the start date for the calculation of the number of days.</span></span>

<span data-ttu-id="e7301-109">`date 2`: *Päivämäärä*</span><span class="sxs-lookup"><span data-stu-id="e7301-109">`date 2`: *Date*</span></span>

<span data-ttu-id="e7301-110">Päivämääräarvo, joka ilmaisee päivien määrän laskennassa käytettävää lopetuspäivämäärää.</span><span class="sxs-lookup"><span data-stu-id="e7301-110">A date value that represents the end date for the calculation of the number of days.</span></span>

## <a name="return-values"></a><span data-ttu-id="e7301-111">Palautusarvot</span><span class="sxs-lookup"><span data-stu-id="e7301-111">Return values</span></span>

<span data-ttu-id="e7301-112">*Kokonaisluku*</span><span class="sxs-lookup"><span data-stu-id="e7301-112">*Integer*</span></span>

<span data-ttu-id="e7301-113">Tuloksena oleva numeroarvo.</span><span class="sxs-lookup"><span data-stu-id="e7301-113">The resulting numeric value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="e7301-114">Käyttöhuomautukset</span><span class="sxs-lookup"><span data-stu-id="e7301-114">Usage notes</span></span>

<span data-ttu-id="e7301-115">`DAYS`-funktio palauttaa positiivisen arvon, kun ensimmäinen päivämäärä on myöhemmin kuin toinen päivämäärä, se palauttaa arvon **0** (nolla), kun ensimmäinen päivämäärä on sama kuin toinen päivämäärä ja palauttaa negatiivisen arvon, kun ensimmäinen päivämäärä on aikaisempi kuin toinen päivämäärä.</span><span class="sxs-lookup"><span data-stu-id="e7301-115">The `DAYS` function returns a positive value when the first date is later than the second date, it returns **0** (zero) when the first date equals the second date, and it returns a negative value when the first date is earlier than the second date.</span></span>

## <a name="example"></a><span data-ttu-id="e7301-116">Esimerkki</span><span class="sxs-lookup"><span data-stu-id="e7301-116">Example</span></span>

<span data-ttu-id="e7301-117">`DAYS (TODAY (), DATEVALUE( DATETIMEFORMAT( ADDDAYS ( NOW(), 1), "yyyyMMdd"), "yyyyMMdd"))` returns **-1**.</span><span class="sxs-lookup"><span data-stu-id="e7301-117">`DAYS (TODAY (), DATEVALUE( DATETIMEFORMAT( ADDDAYS ( NOW(), 1), "yyyyMMdd"), "yyyyMMdd"))` returns **-1**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="e7301-118">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="e7301-118">Additional resources</span></span>

[<span data-ttu-id="e7301-119">Päivämäärä- ja aikatoiminnot</span><span class="sxs-lookup"><span data-stu-id="e7301-119">Date and time functions</span></span>](er-functions-category-datetime.md)
