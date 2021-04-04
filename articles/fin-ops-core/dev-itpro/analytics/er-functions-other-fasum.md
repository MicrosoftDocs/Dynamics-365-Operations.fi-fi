---
title: FA_SUM ER -funktio
description: Tässä ohjeaiheessa on tietoja siitä, miten sähköisen raportoinnin (ER) FA_SUM-funktiota käytetään.
author: NickSelin
manager: kfend
ms.date: 12/17/2019
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
ms.openlocfilehash: c31722537e2a6bae502800953939ca01da4527b9
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/09/2021
ms.locfileid: "5567565"
---
# <a name="fa_sum-er-function"></a><span data-ttu-id="bc436-103">FA_SUM ER -funktio</span><span class="sxs-lookup"><span data-stu-id="bc436-103">FA_SUM ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="bc436-104">`FA_SUM`-funktio palauttaa *Säilö (tietue)*-arvon, joka koostuu tietyn käyttöomaisuushyödykkeen kiinteän omaisuuden määrien tiedoista, arvomallikoodista ja päivämääräajanjaksosta.</span><span class="sxs-lookup"><span data-stu-id="bc436-104">The `FA_SUM` function returns a *Container (record)* value that consists of data for the fixed asset amounts for the specified fixed asset item, value model code, and period of dates.</span></span>

## <a name="syntax"></a><span data-ttu-id="bc436-105">Syntaksi</span><span class="sxs-lookup"><span data-stu-id="bc436-105">Syntax</span></span>

```vb
FA_SUM (fixed asset code, value model code, start date, end date)
```

## <a name="arguments"></a><span data-ttu-id="bc436-106">Argumentit</span><span class="sxs-lookup"><span data-stu-id="bc436-106">Arguments</span></span>

<span data-ttu-id="bc436-107">`fixed asset code`: *Merkkijono*</span><span class="sxs-lookup"><span data-stu-id="bc436-107">`fixed asset code`: *String*</span></span>

<span data-ttu-id="bc436-108">*Merkkijono*-arvo, joka edustaa sen käyttöomaisuuserän koodia, jolle saldo on laskettu.</span><span class="sxs-lookup"><span data-stu-id="bc436-108">A *String* value that represents the code of a fixed asset item that the balance is calculated for.</span></span>

<span data-ttu-id="bc436-109">`value model code`: *Merkkijono*</span><span class="sxs-lookup"><span data-stu-id="bc436-109">`value model code`: *String*</span></span>

<span data-ttu-id="bc436-110">*Merkkijono*-arvo, joka edustaa sen arvomallin koodia, jolle saldo on laskettu.</span><span class="sxs-lookup"><span data-stu-id="bc436-110">A *String* value that represents the code of a value model that the balance is calculated for.</span></span>

<span data-ttu-id="bc436-111">`start date`: *Päivämäärä*</span><span class="sxs-lookup"><span data-stu-id="bc436-111">`start date`: *Date*</span></span>

<span data-ttu-id="bc436-112">*Päivämäärä*, joka ilmaisee alkamispäivämäärän kauden, jolle käyttöomaisuuserien summat lasketaan.</span><span class="sxs-lookup"><span data-stu-id="bc436-112">A *Date* value that represents the start date of a period that the fixed asset amounts are calculated for.</span></span>

<span data-ttu-id="bc436-113">`end date`: *Päivämäärä*</span><span class="sxs-lookup"><span data-stu-id="bc436-113">`end date`: *Date*</span></span>

<span data-ttu-id="bc436-114">*Päivämäärä*, joka ilmaisee loppumispäivämäärän kauden, jolle käyttöomaisuuserien summat lasketaan.</span><span class="sxs-lookup"><span data-stu-id="bc436-114">A *Date* value that represents the end date of a period that the fixed asset amounts are calculated for.</span></span>

## <a name="return-values"></a><span data-ttu-id="bc436-115">Palautusarvot</span><span class="sxs-lookup"><span data-stu-id="bc436-115">Return values</span></span>

<span data-ttu-id="bc436-116">*Kontti (tietue)*</span><span class="sxs-lookup"><span data-stu-id="bc436-116">*Container (record)*</span></span>

<span data-ttu-id="bc436-117">Tuloksena oleva tietueen arvo.</span><span class="sxs-lookup"><span data-stu-id="bc436-117">The resulting record value.</span></span>

## <a name="example"></a><span data-ttu-id="bc436-118">Esimerkki</span><span class="sxs-lookup"><span data-stu-id="bc436-118">Example</span></span>

<span data-ttu-id="bc436-119">`FA_SUM ("COMP-000001", "Current", Date1, Date2)` palauttaa käyttöomaisuuden **COMP-000001**-tieto säilön, joka on laadittu **nykyiselle** arvomallille ja ajanjaksolta **päivämäärä1** **päivämäärä2**.</span><span class="sxs-lookup"><span data-stu-id="bc436-119">`FA_SUM ("COMP-000001", "Current", Date1, Date2)` returns the data container for fixed asset **COMP-000001** that has been prepared for the **Current** value model and for a period from **Date1** to **Date2**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="bc436-120">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="bc436-120">Additional resources</span></span>

[<span data-ttu-id="bc436-121">Muut (liiketoiminnan toimialuekohtaiset) toiminnot</span><span class="sxs-lookup"><span data-stu-id="bc436-121">Other (business domain–specific) functions</span></span>](er-functions-category-other.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]