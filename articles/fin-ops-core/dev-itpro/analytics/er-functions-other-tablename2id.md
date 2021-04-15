---
title: TABLENAME2ID ER -funktio
description: Tässä ohjeaiheessa on tietoja siitä, miten sähköisen raportoinnin (ER) TABLENAME2ID-funktiota käytetään.
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
ms.openlocfilehash: 0f94d00d9d40830d895e906ffbaa2a236f1efc43
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2021
ms.locfileid: "5746552"
---
# <a name="tablename2id-er-function"></a><span data-ttu-id="9d8c0-103">TABLENAME2ID ER -funktio</span><span class="sxs-lookup"><span data-stu-id="9d8c0-103">TABLENAME2ID ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9d8c0-104">`TABLENAME2ID`-funktio palauttaa määritetyn taulukon nimen numeerisen esityksen taulukon tunnukselle *kokonaisluku*-arvona.</span><span class="sxs-lookup"><span data-stu-id="9d8c0-104">The `TABLENAME2ID` function returns a numeric representation of the table ID for the specified table name as an *Integer* value.</span></span>

## <a name="syntax"></a><span data-ttu-id="9d8c0-105">Syntaksi</span><span class="sxs-lookup"><span data-stu-id="9d8c0-105">Syntax</span></span>

```vb
TABLENAME2ID (text)
```

## <a name="arguments"></a><span data-ttu-id="9d8c0-106">Argumentit</span><span class="sxs-lookup"><span data-stu-id="9d8c0-106">Arguments</span></span>

<span data-ttu-id="9d8c0-107">`text`: *Merkkijono*</span><span class="sxs-lookup"><span data-stu-id="9d8c0-107">`text`: *String*</span></span>

<span data-ttu-id="9d8c0-108">Tekstiarvo, joka edustaa kelvollista taulukon nimeä.</span><span class="sxs-lookup"><span data-stu-id="9d8c0-108">A text value that represents a valid table name.</span></span>

## <a name="return-values"></a><span data-ttu-id="9d8c0-109">Palautusarvot</span><span class="sxs-lookup"><span data-stu-id="9d8c0-109">Return values</span></span>

<span data-ttu-id="9d8c0-110">*Kokonaisluku*</span><span class="sxs-lookup"><span data-stu-id="9d8c0-110">*Integer*</span></span>

<span data-ttu-id="9d8c0-111">Tuloksena oleva numeroarvo.</span><span class="sxs-lookup"><span data-stu-id="9d8c0-111">The resulting numeric value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="9d8c0-112">Käyttöhuomautukset</span><span class="sxs-lookup"><span data-stu-id="9d8c0-112">Usage notes</span></span>

<span data-ttu-id="9d8c0-113">Tämän funktion suorittaminen voi aiheuttaa erilaisia tuloksia eri Microsoft Dynamics 365 Finance -esiintymissä, vaikka käytössä olisi sama yrityksen nimi.</span><span class="sxs-lookup"><span data-stu-id="9d8c0-113">Execution of this function can have different results in different instances of Microsoft Dynamics 365 Finance, even if the same company name is used.</span></span>

## <a name="example"></a><span data-ttu-id="9d8c0-114">Esimerkki</span><span class="sxs-lookup"><span data-stu-id="9d8c0-114">Example</span></span>

<span data-ttu-id="9d8c0-115">`TABLENAME2ID ("Intrastat")` palauttaa **1510**.</span><span class="sxs-lookup"><span data-stu-id="9d8c0-115">`TABLENAME2ID ("Intrastat")` returns **1510**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="9d8c0-116">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="9d8c0-116">Additional resources</span></span>

[<span data-ttu-id="9d8c0-117">Muut (liiketoiminnan toimialuekohtaiset) toiminnot</span><span class="sxs-lookup"><span data-stu-id="9d8c0-117">Other (business domain–specific) functions</span></span>](er-functions-category-other.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]