---
title: CONVERTCURRENCY ER-funktio
description: Tässä ohjeaiheessa on tietoja siitä, miten sähköisen raportoinnin (ER) CONVERTCURRENCY-funktiota käytetään.
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
ms.openlocfilehash: 0f0d5bace9b62cf6f0d7576744a6cc271666bf73
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/09/2021
ms.locfileid: "5567637"
---
# <a name="convertcurrency-er-function"></a><span data-ttu-id="dae66-103">CONVERTCURRENCY ER-funktio</span><span class="sxs-lookup"><span data-stu-id="dae66-103">CONVERTCURRENCY ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="dae66-104">`CONVERTCURRENCY`-funktio palauttaa *todellisen* arvon, joka edustaa tulosta muuntamalla määritetty rahasumma määritetystä lähdevaluutasta määritettyyn kohdevaluuttaan käyttämällä määritetyn yrityksen asetuksia tiettynä päivänä.</span><span class="sxs-lookup"><span data-stu-id="dae66-104">The `CONVERTCURRENCY` function returns a *Real* value that represents the result of converting the specified monetary amount from the specified source currency to the specified target currency by using the settings of the specified company on the specified date.</span></span>

## <a name="syntax"></a><span data-ttu-id="dae66-105">Syntaksi</span><span class="sxs-lookup"><span data-stu-id="dae66-105">Syntax</span></span>

```vb
CONVERTCURRENCY (amount, source currency, target currency, date, company)
```

## <a name="arguments"></a><span data-ttu-id="dae66-106">Argumentit</span><span class="sxs-lookup"><span data-stu-id="dae66-106">Arguments</span></span>

<span data-ttu-id="dae66-107">`amount`: *Kokonaisluku* tai *Todellinen*</span><span class="sxs-lookup"><span data-stu-id="dae66-107">`amount`: *Integer* or *Real*</span></span>

<span data-ttu-id="dae66-108">Numeerinen arvo, joka edustaa muunnettavaa rahasummaa.</span><span class="sxs-lookup"><span data-stu-id="dae66-108">A numeric value that represents the monetary amount that must be converted.</span></span>

<span data-ttu-id="dae66-109">`source currency`: *Merkkijono*</span><span class="sxs-lookup"><span data-stu-id="dae66-109">`source currency`: *String*</span></span>

<span data-ttu-id="dae66-110">Lähdevaluutan koodi.</span><span class="sxs-lookup"><span data-stu-id="dae66-110">The code of the source currency.</span></span>

<span data-ttu-id="dae66-111">`target currency`: *Merkkijono*</span><span class="sxs-lookup"><span data-stu-id="dae66-111">`target currency`: *String*</span></span>

<span data-ttu-id="dae66-112">Kohdevaluutan koodi.</span><span class="sxs-lookup"><span data-stu-id="dae66-112">The code of the target currency.</span></span>

<span data-ttu-id="dae66-113">`date`: *Päivämäärä*</span><span class="sxs-lookup"><span data-stu-id="dae66-113">`date`: *Date*</span></span>

<span data-ttu-id="dae66-114">*Päivämäärä*-arvo, joka vastaa muunnoksen vaihtokurssin määrittämiseen käytettävää päivämäärää.</span><span class="sxs-lookup"><span data-stu-id="dae66-114">A *Date* value that represents the date that is used to determine the exchange rate for the conversion.</span></span>

<span data-ttu-id="dae66-115">`company`: *Merkkijono*</span><span class="sxs-lookup"><span data-stu-id="dae66-115">`company`: *String*</span></span>

<span data-ttu-id="dae66-116">*Merkkijono*-arvo, joka kuvaa konversiolle käytettäviä asetuksia käsittelevän yrityksen koodia.</span><span class="sxs-lookup"><span data-stu-id="dae66-116">A *String* value that represents the code of a company that supplies the settings that are used for the conversion.</span></span>

## <a name="return-values"></a><span data-ttu-id="dae66-117">Palautusarvot</span><span class="sxs-lookup"><span data-stu-id="dae66-117">Return values</span></span>

<span data-ttu-id="dae66-118">*Reaaliluku*</span><span class="sxs-lookup"><span data-stu-id="dae66-118">*Real*</span></span>

<span data-ttu-id="dae66-119">Tuloksena oleva numeroarvo.</span><span class="sxs-lookup"><span data-stu-id="dae66-119">The resulting numeric value.</span></span>

## <a name="example"></a><span data-ttu-id="dae66-120">Esimerkki</span><span class="sxs-lookup"><span data-stu-id="dae66-120">Example</span></span>

<span data-ttu-id="dae66-121">`CONVERTCURRENCY (1, "EUR", "USD", TODAY(), "DEMF")` palauttaa yhden euron suuruisen määrän Yhdysvaltojen dollareita nykyisen istunnon päivämääränä **DEMF**-yrityksen asetusten perusteella.</span><span class="sxs-lookup"><span data-stu-id="dae66-121">`CONVERTCURRENCY (1, "EUR", "USD", TODAY(), "DEMF")` returns the equivalent of one euro in US dollars on the current session date, based on settings for the **DEMF** company.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="dae66-122">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="dae66-122">Additional resources</span></span>

[<span data-ttu-id="dae66-123">Muut (liiketoiminnan toimialuekohtaiset) toiminnot</span><span class="sxs-lookup"><span data-stu-id="dae66-123">Other (business domain–specific) functions</span></span>](er-functions-category-other.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]