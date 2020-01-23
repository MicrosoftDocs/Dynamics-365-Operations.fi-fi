---
title: FA_BALANCE ER-funktio
description: Tässä ohjeaiheessa on tietoja siitä, miten sähköisen raportoinnin (ER) FA_BALANCE-funktiota käytetään.
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
ms.openlocfilehash: 0907cb8cb4bc1e90b9fb59eccedb699a894b5cc9
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/20/2019
ms.locfileid: "2916013"
---
# <span data-ttu-id="65eec-103"><a name="FA_BALANCE">FA_BALANCE ER-funktio</a></span><span class="sxs-lookup"><span data-stu-id="65eec-103"><a name="FA_BALANCE">FA_BALANCE ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="65eec-104">`FA_BALANCE`-funktio palauttaa *Säilö (tietue)*-arvon, joka koostuu määritetyn käyttöomaisuuserän, arvomallin koodin, raportointivuoden ja raportointipäivämäärän käyttöomaisuussaldon tiedoista.</span><span class="sxs-lookup"><span data-stu-id="65eec-104">The `FA_BALANCE` function returns a *Container (record)* value that consists of data for the fixed asset balance for the specified fixed asset item, value model code, reporting year, and reporting date.</span></span>

## <a name="syntax"></a><span data-ttu-id="65eec-105">Syntaksi</span><span class="sxs-lookup"><span data-stu-id="65eec-105">Syntax</span></span>

```
FA_BALANCE (fixed asset code, value model code, reporting year, reporting date)
```

## <a name="arguments"></a><span data-ttu-id="65eec-106">Argumentit</span><span class="sxs-lookup"><span data-stu-id="65eec-106">Arguments</span></span>

<span data-ttu-id="65eec-107">`fixed asset code`: *Merkkijono*</span><span class="sxs-lookup"><span data-stu-id="65eec-107">`fixed asset code`: *String*</span></span>

<span data-ttu-id="65eec-108">*Merkkijono*-arvo, joka edustaa sen käyttöomaisuuserän koodia, jolle saldo on laskettu.</span><span class="sxs-lookup"><span data-stu-id="65eec-108">A *String* value that represents the code of a fixed asset item that the balance is calculated for.</span></span>

<span data-ttu-id="65eec-109">`value model code`: *Merkkijono*</span><span class="sxs-lookup"><span data-stu-id="65eec-109">`value model code`: *String*</span></span>

<span data-ttu-id="65eec-110">*Merkkijono*-arvo, joka edustaa sen arvomallin koodia, jolle saldo on laskettu.</span><span class="sxs-lookup"><span data-stu-id="65eec-110">A *String* value that represents the code of a value model that the balance is calculated for.</span></span>

<span data-ttu-id="65eec-111">`reporting year`: *Luettelointiarvo*</span><span class="sxs-lookup"><span data-stu-id="65eec-111">`reporting year`: *Enumeration value*</span></span>

<span data-ttu-id="65eec-112">**AssetYear**-sovelluksen luetteloinnin luettelointiarvo, joka määrittää saldon laskennan kauden.</span><span class="sxs-lookup"><span data-stu-id="65eec-112">An enumeration value of the **AssetYear** application enumeration that defines a period for the balance calculation.</span></span>

<span data-ttu-id="65eec-113">`reporting date`: *Päivämäärä*</span><span class="sxs-lookup"><span data-stu-id="65eec-113">`reporting date`: *Date*</span></span>

<span data-ttu-id="65eec-114">*Päivämäärä*-arvo, joka määrittää saldon laskennan päivämäärän.</span><span class="sxs-lookup"><span data-stu-id="65eec-114">A *Date* value that defines a date for the balance calculation.</span></span>

## <a name="return-values"></a><span data-ttu-id="65eec-115">Palautusarvot</span><span class="sxs-lookup"><span data-stu-id="65eec-115">Return values</span></span>

<span data-ttu-id="65eec-116">*Kontti (tietue)*</span><span class="sxs-lookup"><span data-stu-id="65eec-116">*Container (record)*</span></span>

<span data-ttu-id="65eec-117">Tuloksena oleva tietueen arvo.</span><span class="sxs-lookup"><span data-stu-id="65eec-117">The resulting record value.</span></span>

## <a name="example"></a><span data-ttu-id="65eec-118">Esimerkki</span><span class="sxs-lookup"><span data-stu-id="65eec-118">Example</span></span>

<span data-ttu-id="65eec-119">`FA_ BALANCE ("COMP-000001", "Current", AxEnumAssetYear.ThisYear, SESSIONTODAY ())` palauttaa käyttöomaisuuden **COMP-000001**-saldojen valmistellun tietosäilön, jonka arvomalli on **Current** kyseisenä sovellusistunnon päivämääränä.</span><span class="sxs-lookup"><span data-stu-id="65eec-119">`FA_ BALANCE ("COMP-000001", "Current", AxEnumAssetYear.ThisYear, SESSIONTODAY ())` returns the data container of balances for fixed asset **COMP-000001** that has been prepared for the **Current** value model on the current application session date.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="65eec-120">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="65eec-120">Additional resources</span></span>

[<span data-ttu-id="65eec-121">Muut (liiketoiminnan toimialuekohtaiset) toiminnot</span><span class="sxs-lookup"><span data-stu-id="65eec-121">Other (business domain–specific) functions</span></span>](er-functions-category-other.md)
