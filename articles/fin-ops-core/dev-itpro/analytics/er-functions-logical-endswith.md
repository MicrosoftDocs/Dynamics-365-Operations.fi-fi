---
title: ER:n ENDSWITH-funktio
description: Tässä ohjeaiheessa on tietoja siitä, miten sähköisen raportoinnin (ER) ENDSWITH-funktiota käytetään.
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
ms.openlocfilehash: bdd2f364e2d0b80d3df20592ec827dcabf99a06c
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2021
ms.locfileid: "5745398"
---
# <a name="endswith-er-function"></a><span data-ttu-id="72507-103">ER:n ENDSWITH-funktio</span><span class="sxs-lookup"><span data-stu-id="72507-103">ENDSWITH ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="72507-104">`ENDSWITH`-funktio määrittää, loppuuko määritetty syöte määritettyyn tekstiin.</span><span class="sxs-lookup"><span data-stu-id="72507-104">The `ENDSWITH` function determines whether the specified input ends with the specified text.</span></span> <span data-ttu-id="72507-105">Se palauttaa *totuus*-arvon **TOSI**, jos määritetty syöte loppuu määritetyllä tekstillä.</span><span class="sxs-lookup"><span data-stu-id="72507-105">It returns a *Boolean* value of **TRUE** if the specified input ends with the specified text.</span></span> <span data-ttu-id="72507-106">Muussa tapauksessa se palauttaa *totuusarvon* **EPÄTOSI**.</span><span class="sxs-lookup"><span data-stu-id="72507-106">Otherwise, it returns a *Boolean* value of **FALSE**.</span></span>

## <a name="syntax"></a><span data-ttu-id="72507-107">Syntaksi</span><span class="sxs-lookup"><span data-stu-id="72507-107">Syntax</span></span>

```vb
ENDSWITH (input, end text)
```

## <a name="arguments"></a><span data-ttu-id="72507-108">Argumentit</span><span class="sxs-lookup"><span data-stu-id="72507-108">Arguments</span></span>

<span data-ttu-id="72507-109">`input`: *Merkkijono*</span><span class="sxs-lookup"><span data-stu-id="72507-109">`input`: *String*</span></span>

<span data-ttu-id="72507-110">*Merkkijono*-tyypin tai merkkijonovakion tietolähteen kohteen kelvollinen polku, jonka arvo voi päättyä toiseen argumenttiin.</span><span class="sxs-lookup"><span data-stu-id="72507-110">The valid path of an item of a data source of the *String* type or a string constant, the value of which might end with the second argument.</span></span>

<span data-ttu-id="72507-111">`start text`: *Merkkijono*</span><span class="sxs-lookup"><span data-stu-id="72507-111">`start text`: *String*</span></span>

<span data-ttu-id="72507-112">*Merkkijono*-tietotyypin tai merkkijonovakion tietolähteen kelvollinen polku, jonka arvo voi olla ensimmäisen argumentin lopussa.</span><span class="sxs-lookup"><span data-stu-id="72507-112">The valid path of a data source of the *String* data type or a string constant, the value of which might be at the end of the first argument.</span></span>

## <a name="return-values"></a><span data-ttu-id="72507-113">Palautusarvot</span><span class="sxs-lookup"><span data-stu-id="72507-113">Return values</span></span>

<span data-ttu-id="72507-114">*Boolen arvo*</span><span class="sxs-lookup"><span data-stu-id="72507-114">*Boolean*</span></span>

<span data-ttu-id="72507-115">Tuloksena oleva *Totuusarvo*-arvo.</span><span class="sxs-lookup"><span data-stu-id="72507-115">The resulting *Boolean* value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="72507-116">Käyttöhuomautukset</span><span class="sxs-lookup"><span data-stu-id="72507-116">Usage notes</span></span>

<span data-ttu-id="72507-117">Tätä toimintoa voidaan käyttää [FILTER](er-functions-list-filter.md)-toiminnon ehtolausekkeen määrittämiseen vain, kun asianmukainen määritys on konfiguroitu [Regulatory Configuration Servicesissä](../../../finance/localizations/rcs-globalization-feature.md), jotta voidaan käyttää [Microsoft Dataversea](../data-entities/data-integration-cds.md).</span><span class="sxs-lookup"><span data-stu-id="72507-117">This function can be used to specify a condition expression of the [FILTER](er-functions-list-filter.md) function only when the relevant mapping is configured in [Regulatory Configuration Services](../../../finance/localizations/rcs-globalization-feature.md) to access [Microsoft Dataverse](../data-entities/data-integration-cds.md).</span></span> <span data-ttu-id="72507-118">Muussa tapauksessa tuotetaan poikkeus suunnittelun aikana.</span><span class="sxs-lookup"><span data-stu-id="72507-118">Otherwise, an exception is thrown at design time.</span></span> <span data-ttu-id="72507-119">Vastaanotettu sanoma suosittelee [WHERE](er-functions-list-where.md)-funktion käyttöä `FILTER`-funktion asemesta suorituskyvyn parantamiseksi.</span><span class="sxs-lookup"><span data-stu-id="72507-119">The message that you receive recommends that you use the [WHERE](er-functions-list-where.md) function instead of the `FILTER` function.</span></span>

## <a name="example-1"></a><span data-ttu-id="72507-120">Esimerkki 1</span><span class="sxs-lookup"><span data-stu-id="72507-120">Example 1</span></span>

<span data-ttu-id="72507-121">Lauseke `ENDSWITH ("abc", "d")` palauttaa arvon **EPÄTOSI** ja lauseke `ENDSWITH ("abc", "C")` palauttaa arvon **TOSI**.</span><span class="sxs-lookup"><span data-stu-id="72507-121">The expression `ENDSWITH ("abc", "d")` returns **FALSE**, whereas the expression `ENDSWITH ("abc", "C")` returns **TRUE**.</span></span>

## <a name="example-2"></a><span data-ttu-id="72507-122">Esimerkki 2</span><span class="sxs-lookup"><span data-stu-id="72507-122">Example 2</span></span>

<span data-ttu-id="72507-123">Lauseke `ENDSWITH (model.InvoiceBase.Customer.PostalAddress.Address, "USA")` palauttaa arvon **TOSI**, jos **malli**-tietolähteen **Address**-kentän arvo päättyy merkkijonolla **USA**.</span><span class="sxs-lookup"><span data-stu-id="72507-123">The expression `ENDSWITH (model.InvoiceBase.Customer.PostalAddress.Address, "USA")` returns **TRUE** if the value of the **Address** field of the **model** data source ends with the string **USA**.</span></span> <span data-ttu-id="72507-124">Muussa tapauksessa se palauttaa **EPÄTOSI**-arvon.</span><span class="sxs-lookup"><span data-stu-id="72507-124">Otherwise, it returns **FALSE**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="72507-125">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="72507-125">Additional resources</span></span>

[<span data-ttu-id="72507-126">Loogiset toiminnot</span><span class="sxs-lookup"><span data-stu-id="72507-126">Logical functions</span></span>](er-functions-category-logical.md)
