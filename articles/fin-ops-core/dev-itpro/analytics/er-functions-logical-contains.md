---
title: ER:n CONTAINS-funktio
description: Tässä ohjeaiheessa on tietoja siitä, miten sähköisen raportoinnin (ER) CONTAINS-funktiota käytetään.
author: NickSelin
ms.date: 02/11/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2021-02-01
ms.dyn365.ops.version: AX 10.0.18
ms.openlocfilehash: c1d2d761a38d0edfb9abd439e0f710b336f54927
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2021
ms.locfileid: "5745422"
---
# <a name="contains-er-function"></a><span data-ttu-id="17f1b-103">ER:n CONTAINS-funktio</span><span class="sxs-lookup"><span data-stu-id="17f1b-103">CONTAINS ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="17f1b-104">`CONTAINS`-funktio määrittää, sisältääkö määritetty syöte määritetyn tekstin.</span><span class="sxs-lookup"><span data-stu-id="17f1b-104">The `CONTAINS` function determines whether the specified input contains the specified text.</span></span> <span data-ttu-id="17f1b-105">Se palauttaa *totuus*-arvon **TOSI**, jos määritetty syöte sisältää määritetyn tekstin.</span><span class="sxs-lookup"><span data-stu-id="17f1b-105">It returns a *Boolean* value of **TRUE** if the specified input contains the specified text.</span></span> <span data-ttu-id="17f1b-106">Muussa tapauksessa se palauttaa *totuusarvon* **EPÄTOSI**.</span><span class="sxs-lookup"><span data-stu-id="17f1b-106">Otherwise, it returns a *Boolean* value of **FALSE**.</span></span>

## <a name="syntax"></a><span data-ttu-id="17f1b-107">Syntaksi</span><span class="sxs-lookup"><span data-stu-id="17f1b-107">Syntax</span></span>

```vb
CONTAINS (input, search text)
```

## <a name="arguments"></a><span data-ttu-id="17f1b-108">Argumentit</span><span class="sxs-lookup"><span data-stu-id="17f1b-108">Arguments</span></span>

<span data-ttu-id="17f1b-109">`input`: *Merkkijono*</span><span class="sxs-lookup"><span data-stu-id="17f1b-109">`input`: *String*</span></span>

<span data-ttu-id="17f1b-110">*Merkkijono*-tyypin tai merkkijonovakion tietolähteen kohteen kelvollinen polku, jonka arvo voi sisältää toisen argumentin.</span><span class="sxs-lookup"><span data-stu-id="17f1b-110">The valid path of an item of a data source of the *String* type or a string constant, the value of which might contain the second argument.</span></span>

<span data-ttu-id="17f1b-111">`search text`: *Merkkijono*</span><span class="sxs-lookup"><span data-stu-id="17f1b-111">`search text`: *String*</span></span>

<span data-ttu-id="17f1b-112">*Merkkijono*-tietotyypin tai merkkijonovakion tietolähteen kelvollinen polku, jonka arvo voi sisältyä ensimmäiseen argumenttiin.</span><span class="sxs-lookup"><span data-stu-id="17f1b-112">The valid path of a data source of the *String* data type or a string constant, the value of which might be contained in the first argument.</span></span>

## <a name="return-values"></a><span data-ttu-id="17f1b-113">Palautusarvot</span><span class="sxs-lookup"><span data-stu-id="17f1b-113">Return values</span></span>

<span data-ttu-id="17f1b-114">*Boolen arvo*</span><span class="sxs-lookup"><span data-stu-id="17f1b-114">*Boolean*</span></span>

<span data-ttu-id="17f1b-115">Tuloksena oleva *Totuusarvo*-arvo.</span><span class="sxs-lookup"><span data-stu-id="17f1b-115">The resulting *Boolean* value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="17f1b-116">Käyttöhuomautukset</span><span class="sxs-lookup"><span data-stu-id="17f1b-116">Usage notes</span></span>

<span data-ttu-id="17f1b-117">Tätä toimintoa voidaan käyttää [FILTER](er-functions-list-filter.md)-toiminnon ehtolausekkeen määrittämiseen vain, kun asianmukainen määritys on konfiguroitu [Regulatory Configuration Servicesissä](../../../finance/localizations/rcs-globalization-feature.md), jotta voidaan käyttää [Microsoft Dataversea](../data-entities/data-integration-cds.md).</span><span class="sxs-lookup"><span data-stu-id="17f1b-117">This function can be used to specify a condition expression of the [FILTER](er-functions-list-filter.md) function only when the relevant mapping is configured in [Regulatory Configuration Services](../../../finance/localizations/rcs-globalization-feature.md) to access [Microsoft Dataverse](../data-entities/data-integration-cds.md).</span></span> <span data-ttu-id="17f1b-118">Muussa tapauksessa tuotetaan poikkeus suunnittelun aikana.</span><span class="sxs-lookup"><span data-stu-id="17f1b-118">Otherwise, an exception is thrown at design time.</span></span> <span data-ttu-id="17f1b-119">Vastaanotettu sanoma suosittelee [WHERE](er-functions-list-where.md)-funktion käyttöä `FILTER`-funktion asemesta suorituskyvyn parantamiseksi.</span><span class="sxs-lookup"><span data-stu-id="17f1b-119">The message that you receive recommends that you use the [WHERE](er-functions-list-where.md) function instead of the `FILTER` function.</span></span>

## <a name="example-1"></a><span data-ttu-id="17f1b-120">Esimerkki 1</span><span class="sxs-lookup"><span data-stu-id="17f1b-120">Example 1</span></span>

<span data-ttu-id="17f1b-121">Lauseke `CONTAINS ("abc", "d")` palauttaa arvon **EPÄTOSI** ja lauseke `CONTAINS ("abc", "C")` palauttaa arvon **TOSI**.</span><span class="sxs-lookup"><span data-stu-id="17f1b-121">The expression `CONTAINS ("abc", "d")` returns **FALSE**, whereas the expression `CONTAINS ("abc", "C")` returns **TRUE**.</span></span>

## <a name="example-2"></a><span data-ttu-id="17f1b-122">Esimerkki 2</span><span class="sxs-lookup"><span data-stu-id="17f1b-122">Example 2</span></span>

<span data-ttu-id="17f1b-123">Lauseke `CONTAINS (model.InvoiceBase.Customer.PostalAddress.Address, "DEU")` palauttaa arvon **TOSI**, jos **malli**-tietolähteen **Address**-kentän arvo sisältäää merkkijonon **DEU**.</span><span class="sxs-lookup"><span data-stu-id="17f1b-123">The expression `CONTAINS (model.InvoiceBase.Customer.PostalAddress.Address, "DEU")` returns **TRUE** if the value of the **Address** field of the **model** data source contains the string **DEU**.</span></span> <span data-ttu-id="17f1b-124">Muussa tapauksessa se palauttaa **EPÄTOSI**-arvon.</span><span class="sxs-lookup"><span data-stu-id="17f1b-124">Otherwise, it returns **FALSE**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="17f1b-125">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="17f1b-125">Additional resources</span></span>

[<span data-ttu-id="17f1b-126">Loogiset toiminnot</span><span class="sxs-lookup"><span data-stu-id="17f1b-126">Logical functions</span></span>](er-functions-category-logical.md)
