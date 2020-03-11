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
ms.openlocfilehash: 951de1d1505508ebb6abeff5b80ecef10573e117
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/12/2020
ms.locfileid: "3041260"
---
# <span data-ttu-id="7b8be-103"><a name="TABLENAME2ID">TABLENAME2ID ER -funktio</a></span><span class="sxs-lookup"><span data-stu-id="7b8be-103"><a name="TABLENAME2ID">TABLENAME2ID ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7b8be-104">`TABLENAME2ID`-funktio palauttaa määritetyn taulukon nimen numeerisen esityksen taulukon tunnukselle *kokonaisluku*-arvona.</span><span class="sxs-lookup"><span data-stu-id="7b8be-104">The `TABLENAME2ID` function returns a numeric representation of the table ID for the specified table name as an *Integer* value.</span></span>

## <a name="syntax"></a><span data-ttu-id="7b8be-105">Syntaksi</span><span class="sxs-lookup"><span data-stu-id="7b8be-105">Syntax</span></span>

```vb
TABLENAME2ID (text)
```

## <a name="arguments"></a><span data-ttu-id="7b8be-106">Argumentit</span><span class="sxs-lookup"><span data-stu-id="7b8be-106">Arguments</span></span>

<span data-ttu-id="7b8be-107">`text`: *Merkkijono*</span><span class="sxs-lookup"><span data-stu-id="7b8be-107">`text`: *String*</span></span>

<span data-ttu-id="7b8be-108">Tekstiarvo, joka edustaa kelvollista taulukon nimeä.</span><span class="sxs-lookup"><span data-stu-id="7b8be-108">A text value that represents a valid table name.</span></span>

## <a name="return-values"></a><span data-ttu-id="7b8be-109">Palautusarvot</span><span class="sxs-lookup"><span data-stu-id="7b8be-109">Return values</span></span>

<span data-ttu-id="7b8be-110">*Kokonaisluku*</span><span class="sxs-lookup"><span data-stu-id="7b8be-110">*Integer*</span></span>

<span data-ttu-id="7b8be-111">Tuloksena oleva numeroarvo.</span><span class="sxs-lookup"><span data-stu-id="7b8be-111">The resulting numeric value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="7b8be-112">Käyttöhuomautukset</span><span class="sxs-lookup"><span data-stu-id="7b8be-112">Usage notes</span></span>

<span data-ttu-id="7b8be-113">Tämän funktion suorittaminen voi aiheuttaa erilaisia tuloksia eri Microsoft Dynamics 365 Finance -esiintymissä, vaikka käytössä olisi sama yrityksen nimi.</span><span class="sxs-lookup"><span data-stu-id="7b8be-113">Execution of this function can have different results in different instances of Microsoft Dynamics 365 Finance, even if the same company name is used.</span></span>

## <a name="example"></a><span data-ttu-id="7b8be-114">Esimerkki</span><span class="sxs-lookup"><span data-stu-id="7b8be-114">Example</span></span>

<span data-ttu-id="7b8be-115">`TABLENAME2ID ("Intrastat")` palauttaa **1510**.</span><span class="sxs-lookup"><span data-stu-id="7b8be-115">`TABLENAME2ID ("Intrastat")` returns **1510**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="7b8be-116">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="7b8be-116">Additional resources</span></span>

[<span data-ttu-id="7b8be-117">Muut (liiketoiminnan toimialuekohtaiset) toiminnot</span><span class="sxs-lookup"><span data-stu-id="7b8be-117">Other (business domain–specific) functions</span></span>](er-functions-category-other.md)
