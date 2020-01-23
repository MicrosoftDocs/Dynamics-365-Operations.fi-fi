---
title: FA_SUM ER -funktio
description: Tässä ohjeaiheessa on tietoja siitä, miten sähköisen raportoinnin (ER) FA_SUM-funktiota käytetään.
author: NickSelin
manager: kfend
ms.date: 12/17/2019
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
ms.openlocfilehash: 32eb07689598a3b6c852f272b480106670b88cd0
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/20/2019
ms.locfileid: "2916979"
---
# <span data-ttu-id="29416-103"><a name="FA_SUM">FA_SUM ER -funktio</a></span><span class="sxs-lookup"><span data-stu-id="29416-103"><a name="FA_SUM">FA_SUM ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="29416-104">`FA_SUM`-funktio palauttaa *Säilö (tietue)*-arvon, joka koostuu tietyn käyttöomaisuushyödykkeen kiinteän omaisuuden määrien tiedoista, arvomallikoodista ja päivämääräajanjaksosta.</span><span class="sxs-lookup"><span data-stu-id="29416-104">The `FA_SUM` function returns a *Container (record)* value that consists of data for the fixed asset amounts for the specified fixed asset item, value model code, and period of dates.</span></span>

## <a name="syntax"></a><span data-ttu-id="29416-105">Syntaksi</span><span class="sxs-lookup"><span data-stu-id="29416-105">Syntax</span></span>

```
FA_SUM (fixed asset code, value model code, start date, end date)
```

## <a name="arguments"></a><span data-ttu-id="29416-106">Argumentit</span><span class="sxs-lookup"><span data-stu-id="29416-106">Arguments</span></span>

<span data-ttu-id="29416-107">`fixed asset code`: *Merkkijono*</span><span class="sxs-lookup"><span data-stu-id="29416-107">`fixed asset code`: *String*</span></span>

<span data-ttu-id="29416-108">*Merkkijono*-arvo, joka edustaa sen käyttöomaisuuserän koodia, jolle saldo on laskettu.</span><span class="sxs-lookup"><span data-stu-id="29416-108">A *String* value that represents the code of a fixed asset item that the balance is calculated for.</span></span>

<span data-ttu-id="29416-109">`value model code`: *Merkkijono*</span><span class="sxs-lookup"><span data-stu-id="29416-109">`value model code`: *String*</span></span>

<span data-ttu-id="29416-110">*Merkkijono*-arvo, joka edustaa sen arvomallin koodia, jolle saldo on laskettu.</span><span class="sxs-lookup"><span data-stu-id="29416-110">A *String* value that represents the code of a value model that the balance is calculated for.</span></span>

<span data-ttu-id="29416-111">`start date`: *Päivämäärä*</span><span class="sxs-lookup"><span data-stu-id="29416-111">`start date`: *Date*</span></span>

<span data-ttu-id="29416-112">*Päivämäärä*, joka ilmaisee alkamispäivämäärän kauden, jolle käyttöomaisuuserien summat lasketaan.</span><span class="sxs-lookup"><span data-stu-id="29416-112">A *Date* value that represents the start date of a period that the fixed asset amounts are calculated for.</span></span>

<span data-ttu-id="29416-113">`end date`: *Päivämäärä*</span><span class="sxs-lookup"><span data-stu-id="29416-113">`end date`: *Date*</span></span>

<span data-ttu-id="29416-114">*Päivämäärä*, joka ilmaisee loppumispäivämäärän kauden, jolle käyttöomaisuuserien summat lasketaan.</span><span class="sxs-lookup"><span data-stu-id="29416-114">A *Date* value that represents the end date of a period that the fixed asset amounts are calculated for.</span></span>

## <a name="return-values"></a><span data-ttu-id="29416-115">Palautusarvot</span><span class="sxs-lookup"><span data-stu-id="29416-115">Return values</span></span>

<span data-ttu-id="29416-116">*Kontti (tietue)*</span><span class="sxs-lookup"><span data-stu-id="29416-116">*Container (record)*</span></span>

<span data-ttu-id="29416-117">Tuloksena oleva tietueen arvo.</span><span class="sxs-lookup"><span data-stu-id="29416-117">The resulting record value.</span></span>

## <a name="example"></a><span data-ttu-id="29416-118">Esimerkki</span><span class="sxs-lookup"><span data-stu-id="29416-118">Example</span></span>

<span data-ttu-id="29416-119">`FA_SUM ("COMP-000001", "Current", Date1, Date2)` palauttaa käyttöomaisuuden **COMP-000001**-tieto säilön, joka on laadittu **nykyiselle** arvomallille ja ajanjaksolta **päivämäärä1** **päivämäärä2**.</span><span class="sxs-lookup"><span data-stu-id="29416-119">`FA_SUM ("COMP-000001", "Current", Date1, Date2)` returns the data container for fixed asset **COMP-000001** that has been prepared for the **Current** value model and for a period from **Date1** to **Date2**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="29416-120">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="29416-120">Additional resources</span></span>

[<span data-ttu-id="29416-121">Muut (liiketoiminnan toimialuekohtaiset) toiminnot</span><span class="sxs-lookup"><span data-stu-id="29416-121">Other (business domain–specific) functions</span></span>](er-functions-category-other.md)
