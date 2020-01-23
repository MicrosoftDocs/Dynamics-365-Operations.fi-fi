---
title: TABLENAME2ID ER -funktio
description: Tässä ohjeaiheessa on tietoja siitä, miten sähköisen raportoinnin (ER) TABLENAME2ID-funktiota käytetään.
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
ms.openlocfilehash: 77d889f75f38b3c07855a96bf65f1456ac2f42e2
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/20/2019
ms.locfileid: "2915806"
---
# <span data-ttu-id="5e6ed-103"><a name="TABLENAME2ID">TABLENAME2ID ER -funktio</a></span><span class="sxs-lookup"><span data-stu-id="5e6ed-103"><a name="TABLENAME2ID">TABLENAME2ID ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5e6ed-104">`TABLENAME2ID`-funktio palauttaa määritetyn taulukon nimen numeerisen esityksen taulukon tunnukselle *kokonaisluku*-arvona.</span><span class="sxs-lookup"><span data-stu-id="5e6ed-104">The `TABLENAME2ID` function returns a numeric representation of the table ID for the specified table name as an *Integer* value.</span></span>

## <a name="syntax"></a><span data-ttu-id="5e6ed-105">Syntaksi</span><span class="sxs-lookup"><span data-stu-id="5e6ed-105">Syntax</span></span>

```
TABLENAME2ID (text)
```

## <a name="arguments"></a><span data-ttu-id="5e6ed-106">Argumentit</span><span class="sxs-lookup"><span data-stu-id="5e6ed-106">Arguments</span></span>

<span data-ttu-id="5e6ed-107">`text`: *Merkkijono*</span><span class="sxs-lookup"><span data-stu-id="5e6ed-107">`text`: *String*</span></span>

<span data-ttu-id="5e6ed-108">Tekstiarvo, joka edustaa kelvollista taulukon nimeä.</span><span class="sxs-lookup"><span data-stu-id="5e6ed-108">A text value that represents a valid table name.</span></span>

## <a name="return-values"></a><span data-ttu-id="5e6ed-109">Palautusarvot</span><span class="sxs-lookup"><span data-stu-id="5e6ed-109">Return values</span></span>

<span data-ttu-id="5e6ed-110">*Kokonaisluku*</span><span class="sxs-lookup"><span data-stu-id="5e6ed-110">*Integer*</span></span>

<span data-ttu-id="5e6ed-111">Tuloksena oleva numeroarvo.</span><span class="sxs-lookup"><span data-stu-id="5e6ed-111">The resulting numeric value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="5e6ed-112">Käyttöhuomautukset</span><span class="sxs-lookup"><span data-stu-id="5e6ed-112">Usage notes</span></span>

<span data-ttu-id="5e6ed-113">Tämän funktion suorittaminen voi aiheuttaa erilaisia tuloksia eri Microsoft Dynamics 365 Finance -esiintymissä, vaikka käytössä olisi sama yrityksen nimi.</span><span class="sxs-lookup"><span data-stu-id="5e6ed-113">Execution of this function can have different results in different instances of Microsoft Dynamics 365 Finance, even if the same company name is used.</span></span>

## <a name="example"></a><span data-ttu-id="5e6ed-114">Esimerkki</span><span class="sxs-lookup"><span data-stu-id="5e6ed-114">Example</span></span>

<span data-ttu-id="5e6ed-115">`TABLENAME2ID ("Intrastat")` palauttaa **1510**.</span><span class="sxs-lookup"><span data-stu-id="5e6ed-115">`TABLENAME2ID ("Intrastat")` returns **1510**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="5e6ed-116">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="5e6ed-116">Additional resources</span></span>

[<span data-ttu-id="5e6ed-117">Muut (liiketoiminnan toimialuekohtaiset) toiminnot</span><span class="sxs-lookup"><span data-stu-id="5e6ed-117">Other (business domain–specific) functions</span></span>](er-functions-category-other.md)
