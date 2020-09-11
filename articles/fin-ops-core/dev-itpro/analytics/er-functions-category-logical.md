---
title: Luettelo ER-funktioista loogisessa luokassa
description: Tässä ohjeaiheessa on tietoja sähköisen raportoinnin (ER) tukemista loogisista funktioista.
author: NickSelin
manager: kfend
ms.date: 08/19/2020
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
ms.openlocfilehash: e622778c60646e5cc84cd6e23a5d4954a0fe0bb3
ms.sourcegitcommit: 38ad6f791c3d5688a5dc201a234ba89f155f7f03
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/19/2020
ms.locfileid: "3705092"
---
# <a name="list-of-er-functions-in-the-logical-category"></a><span data-ttu-id="ffb30-103">Luettelo ER-funktioista loogisessa luokassa</span><span class="sxs-lookup"><span data-stu-id="ffb30-103">List of ER functions in the logical category</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ffb30-104">Sähköisten raportointitoimintojen loogisia funktioita voidaan käyttää loogisten arvojen tekemiseen, jotta voit suorittaa useamman kuin yhden vertailun yksittäisessä lausekkeessa tai testata useita ehtoja.</span><span class="sxs-lookup"><span data-stu-id="ffb30-104">Electronic reporting (ER) logical functions can be used to work with logical values to perform more than one comparison in a single expression or test multiple conditions.</span></span> <span data-ttu-id="ffb30-105">Tässä aiheessa on yhteenveto näistä funktioista.</span><span class="sxs-lookup"><span data-stu-id="ffb30-105">This topic provides a summary of these functions.</span></span>

## <a name="list-of-supported-functions"></a><span data-ttu-id="ffb30-106">Luettelo tuetuista toiminnoista</span><span class="sxs-lookup"><span data-stu-id="ffb30-106">List of supported functions</span></span>

| <span data-ttu-id="ffb30-107">Toiminto</span><span class="sxs-lookup"><span data-stu-id="ffb30-107">Function</span></span> | <span data-ttu-id="ffb30-108">Kuvaus</span><span class="sxs-lookup"><span data-stu-id="ffb30-108">Description</span></span> |
|----------|-------------|
| [<span data-ttu-id="ffb30-109">Ja</span><span class="sxs-lookup"><span data-stu-id="ffb30-109">And</span></span>](er-functions-logical-and.md)                       | <span data-ttu-id="ffb30-110">Tämä funktio palauttaa *totuusarvon* **TOSI**, jos kaikki määritetyt ehdot toteutuvat.</span><span class="sxs-lookup"><span data-stu-id="ffb30-110">This function returns a *Boolean* value of **TRUE** if all the specified conditions are true.</span></span> <span data-ttu-id="ffb30-111">Muussa tapauksessa se palauttaa *totuusarvon* **EPÄTOSI**.</span><span class="sxs-lookup"><span data-stu-id="ffb30-111">Otherwise, it returns a *Boolean* value of **FALSE**.</span></span> |
| [<span data-ttu-id="ffb30-112">Laatikko</span><span class="sxs-lookup"><span data-stu-id="ffb30-112">Case</span></span>](er-functions-logical-case.md)                     | <span data-ttu-id="ffb30-113">Tämä funktio arvioi määritetyn lausekkeen arvon määritettyjen vaihtoehtoisten asetusten mukaan ja palauttaa ensimmäisen vaihtoehdon tuloksen, joka on yhtä suuri kuin määritetyn lausekkeen arvo.</span><span class="sxs-lookup"><span data-stu-id="ffb30-113">This function evaluates the value of the specified expression against the specified alternative options and returns the result of the first option that equals the value of the specified expression.</span></span> <span data-ttu-id="ffb30-114">Muussa tapauksessa se palauttaa valinnaisen oletustuloksen, jos oletustulos määritetään kutsutussa funktiossa viimeisenä argumenttina, jota ei edellä vaihtoehto.</span><span class="sxs-lookup"><span data-stu-id="ffb30-114">Otherwise, it returns an optional default result, if a default result is specified as the last argument of the called function that isn't preceded by an option.</span></span> <span data-ttu-id="ffb30-115">Palautettava arvo voi olla minkä tahansa tuettujen tietotyyppien arvo.</span><span class="sxs-lookup"><span data-stu-id="ffb30-115">The value that is returned can be a value of any of the supported data types.</span></span> |
| [<span data-ttu-id="ffb30-116">Jos</span><span class="sxs-lookup"><span data-stu-id="ffb30-116">If</span></span>](er-functions-logical-if.md)                         | <span data-ttu-id="ffb30-117">Tämä funktio palauttaa ensimmäisen määritetyn arvon, jos määritetyt ehdot täyttyvät.</span><span class="sxs-lookup"><span data-stu-id="ffb30-117">This function returns the first specified value if the specified condition is met.</span></span> <span data-ttu-id="ffb30-118">Muussa tapauksessa se palauttaa toisen määritetyn arvon.</span><span class="sxs-lookup"><span data-stu-id="ffb30-118">Otherwise, it returns the second specified value.</span></span> <span data-ttu-id="ffb30-119">Palautettava arvo voi olla minkä tahansa tuettujen tietotyyppien arvo.</span><span class="sxs-lookup"><span data-stu-id="ffb30-119">The value that is returned can be a value of any of the supported data types.</span></span> |
| [<span data-ttu-id="ffb30-120">Ei</span><span class="sxs-lookup"><span data-stu-id="ffb30-120">Not</span></span>](er-functions-logical-not.md)                       | <span data-ttu-id="ffb30-121">Tämä funktio palauttaa määritetyn ehdon käänteisen loogisen arvon *totuusarvoksi*.</span><span class="sxs-lookup"><span data-stu-id="ffb30-121">This function returns the reversed logical value of the specified condition as a *Boolean* value.</span></span> |
| [<span data-ttu-id="ffb30-122">Or</span><span class="sxs-lookup"><span data-stu-id="ffb30-122">Or</span></span>](er-functions-logical-or.md)                         | <span data-ttu-id="ffb30-123">Tämä funktio palauttaa *totuusarvon* **EPÄTOSI**, jos mikään määritetty ehto ei toteudu.</span><span class="sxs-lookup"><span data-stu-id="ffb30-123">This function returns a *Boolean* value of **FALSE** if all the specified conditions are false.</span></span> <span data-ttu-id="ffb30-124">Jos joku määritetty ehto toteutuu, tämä funktio palauttaa *totuusarvon* **TOSI**.</span><span class="sxs-lookup"><span data-stu-id="ffb30-124">If any specified condition is true, the function returns a *Boolean* value of **TRUE**.</span></span> |
| [<span data-ttu-id="ffb30-125">ValueIn</span><span class="sxs-lookup"><span data-stu-id="ffb30-125">ValueIn</span></span>](er-functions-logical-valuein.md)               | <span data-ttu-id="ffb30-126">Tämä funktio määrittää, vastaako määritetty syöte määritetyn luettelokohteen tiettyä arvoa.</span><span class="sxs-lookup"><span data-stu-id="ffb30-126">This function determines whether the specified input matches any value of a specified item in the specified list.</span></span> <span data-ttu-id="ffb30-127">Se palauttaa *totuusarvon* arvon **TOSI**, jos määritetty syöte vastaa määritetyn lausekkeen suorittamisen tulosta vähintään yhdelle määritetyn luettelon tietueelle.</span><span class="sxs-lookup"><span data-stu-id="ffb30-127">It returns a *Boolean* value of **TRUE** if the specified input matches the result of running the specified expression for at least one record of the specified list.</span></span> <span data-ttu-id="ffb30-128">Muussa tapauksessa se palauttaa *totuusarvon* **EPÄTOSI**.</span><span class="sxs-lookup"><span data-stu-id="ffb30-128">Otherwise, it returns a *Boolean* value of **FALSE**.</span></span> |
| [<span data-ttu-id="ffb30-129">ValueInLarge</span><span class="sxs-lookup"><span data-stu-id="ffb30-129">ValueInLarge</span></span>](er-functions-logical-valueinlarge.md)     | <span data-ttu-id="ffb30-130">Tämä funktio määrittää, vastaako määritetty *Int64*- tai *Kokonaisluku*-tyyppi määritetyn luettelokohteen tiettyä arvoa.</span><span class="sxs-lookup"><span data-stu-id="ffb30-130">This function determines whether the specified input of the *Int64* or *Integer* type matches any value of a specified item in the specified list.</span></span> <span data-ttu-id="ffb30-131">Se palauttaa *totuusarvon* arvon **TOSI**, jos määritetty syöte vastaa määritetyn lausekkeen suorittamisen tulosta vähintään yhdelle määritetyn luettelon tietueelle.</span><span class="sxs-lookup"><span data-stu-id="ffb30-131">It returns a *Boolean* value of **TRUE** if the specified input matches the result of running the specified expression for at least one record of the specified list.</span></span> <span data-ttu-id="ffb30-132">Muussa tapauksessa se palauttaa *totuusarvon* **EPÄTOSI**.</span><span class="sxs-lookup"><span data-stu-id="ffb30-132">Otherwise, it returns a *Boolean* value of **FALSE**.</span></span> |


## <a name="additional-resources"></a><span data-ttu-id="ffb30-133">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="ffb30-133">Additional resources</span></span>

[<span data-ttu-id="ffb30-134">Sähköisen raportoinnin yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="ffb30-134">Electronic Reporting overview</span></span>](general-electronic-reporting.md)

[<span data-ttu-id="ffb30-135">Sähköisen raportoinnin kaavojen suunnittelutoiminto</span><span class="sxs-lookup"><span data-stu-id="ffb30-135">Formula designer in Electronic reporting</span></span>](general-electronic-reporting-formula-designer.md)

[<span data-ttu-id="ffb30-136">Sähköisen raportoinnin kaavakieli</span><span class="sxs-lookup"><span data-stu-id="ffb30-136">Electronic reporting formula language</span></span>](er-formula-language.md)
