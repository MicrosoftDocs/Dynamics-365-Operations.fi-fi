---
title: ER:n STARTSWITH-funktio
description: Tässä ohjeaiheessa on tietoja siitä, miten sähköisen raportoinnin (ER) STARTSWITH-funktiota käytetään.
author: NickSelin
ms.date: 02/11/2021
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 50883bb604d2d1f2947545ce27fa02099e70b0e6
ms.sourcegitcommit: 17cee26b03f7b5afe8a089a0a9b2380e8d377d70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/15/2021
ms.locfileid: "6048839"
---
# <a name="startswith-er-function"></a><span data-ttu-id="52fd7-103">ER:n STARTSWITH-funktio</span><span class="sxs-lookup"><span data-stu-id="52fd7-103">STARTSWITH ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="52fd7-104">`STARTSWITH`-funktio määrittää, alkaako määritetty syöte määritetyllä tekstillä.</span><span class="sxs-lookup"><span data-stu-id="52fd7-104">The `STARTSWITH` function determines whether the specified input starts with the specified text.</span></span> <span data-ttu-id="52fd7-105">Se palauttaa *totuus*-arvon **TOSI**, jos määritetty syöte alkaa määritetyllä tekstillä.</span><span class="sxs-lookup"><span data-stu-id="52fd7-105">It returns a *Boolean* value of **TRUE** if the specified input starts with the specified text.</span></span> <span data-ttu-id="52fd7-106">Muussa tapauksessa se palauttaa *totuusarvon* **EPÄTOSI**.</span><span class="sxs-lookup"><span data-stu-id="52fd7-106">Otherwise, it returns a *Boolean* value of **FALSE**.</span></span>

## <a name="syntax"></a><span data-ttu-id="52fd7-107">Syntaksi</span><span class="sxs-lookup"><span data-stu-id="52fd7-107">Syntax</span></span>

```vb
STARTSWITH (input, start text)
```

## <a name="arguments"></a><span data-ttu-id="52fd7-108">Argumentit</span><span class="sxs-lookup"><span data-stu-id="52fd7-108">Arguments</span></span>

<span data-ttu-id="52fd7-109">`input`: *Merkkijono*</span><span class="sxs-lookup"><span data-stu-id="52fd7-109">`input`: *String*</span></span>

<span data-ttu-id="52fd7-110">*Merkkijono*-tyypin tai merkkijonovakion tietolähteen kohteen kelvollinen polku, jonka arvo voi alkaa toisella argumentilla.</span><span class="sxs-lookup"><span data-stu-id="52fd7-110">The valid path of an item of a data source of the *String* type or a string constant, the value of which might start with the second argument.</span></span>

<span data-ttu-id="52fd7-111">`start text`: *Merkkijono*</span><span class="sxs-lookup"><span data-stu-id="52fd7-111">`start text`: *String*</span></span>

<span data-ttu-id="52fd7-112">*Merkkijono*-tietotyypin tai merkkijonovakion tietolähteen kelvollinen polku, jonka arvo voi olla ensimmäisen argumentin alussa.</span><span class="sxs-lookup"><span data-stu-id="52fd7-112">The valid path of a data source of the *String* data type or a string constant, the value of which might be at the beginning of the first argument.</span></span>

## <a name="return-values"></a><span data-ttu-id="52fd7-113">Palautusarvot</span><span class="sxs-lookup"><span data-stu-id="52fd7-113">Return values</span></span>

<span data-ttu-id="52fd7-114">*Boolen arvo*</span><span class="sxs-lookup"><span data-stu-id="52fd7-114">*Boolean*</span></span>

<span data-ttu-id="52fd7-115">Tuloksena oleva *Totuusarvo*-arvo.</span><span class="sxs-lookup"><span data-stu-id="52fd7-115">The resulting *Boolean* value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="52fd7-116">Käyttöhuomautukset</span><span class="sxs-lookup"><span data-stu-id="52fd7-116">Usage notes</span></span>

<span data-ttu-id="52fd7-117">Tätä toimintoa voidaan käyttää [FILTER](er-functions-list-filter.md)-toiminnon ehtolausekkeen määrittämiseen vain, kun asianmukainen määritys on konfiguroitu [Regulatory Configuration Servicesissä](../../../finance/localizations/rcs-globalization-feature.md), jotta voidaan käyttää [Microsoft Dataversea](/power-platform/admin/data-integrator).</span><span class="sxs-lookup"><span data-stu-id="52fd7-117">This function can be used to specify a condition expression of the [FILTER](er-functions-list-filter.md) function only when the relevant mapping is configured in [Regulatory Configuration Services](../../../finance/localizations/rcs-globalization-feature.md) to access [Microsoft Dataverse](/power-platform/admin/data-integrator).</span></span> <span data-ttu-id="52fd7-118">Muussa tapauksessa tuotetaan poikkeus suunnittelun aikana.</span><span class="sxs-lookup"><span data-stu-id="52fd7-118">Otherwise, an exception is thrown at design time.</span></span> <span data-ttu-id="52fd7-119">Vastaanotettu sanoma suosittelee [WHERE](er-functions-list-where.md)-funktion käyttöä `FILTER`-funktion asemesta suorituskyvyn parantamiseksi.</span><span class="sxs-lookup"><span data-stu-id="52fd7-119">The message that you receive recommends that you use the [WHERE](er-functions-list-where.md) function instead of the `FILTER` function.</span></span>

## <a name="example-1"></a><span data-ttu-id="52fd7-120">Esimerkki 1</span><span class="sxs-lookup"><span data-stu-id="52fd7-120">Example 1</span></span>

<span data-ttu-id="52fd7-121">Lauseke `STARTSWITH ("abc", "d")` palauttaa arvon **EPÄTOSI** ja lauseke `STARTSWITH ("abc", "A")` palauttaa arvon **TOSI**.</span><span class="sxs-lookup"><span data-stu-id="52fd7-121">The expression `STARTSWITH ("abc", "d")` returns **FALSE**, whereas the expression `STARTSWITH ("abc", "A")` returns **TRUE**.</span></span>

## <a name="example-2"></a><span data-ttu-id="52fd7-122">Esimerkki 2</span><span class="sxs-lookup"><span data-stu-id="52fd7-122">Example 2</span></span>

<span data-ttu-id="52fd7-123">Lauseke `STARTSWITH (model.InvoiceBase.Customer.PostalAddress.Address, "123 Coffee Street")` palauttaa arvon **TOSI**, jos **malli**-tietolähteen **Address**-kentän arvo alkaa merkkijonolla **123 Coffee Street**.</span><span class="sxs-lookup"><span data-stu-id="52fd7-123">The expression `STARTSWITH (model.InvoiceBase.Customer.PostalAddress.Address, "123 Coffee Street")` returns **TRUE** if the value of the **Address** field of the **model** data source starts with the string **123 Coffee Street**.</span></span> <span data-ttu-id="52fd7-124">Muussa tapauksessa se palauttaa **EPÄTOSI**-arvon.</span><span class="sxs-lookup"><span data-stu-id="52fd7-124">Otherwise, it returns **FALSE**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="52fd7-125">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="52fd7-125">Additional resources</span></span>

[<span data-ttu-id="52fd7-126">Loogiset toiminnot</span><span class="sxs-lookup"><span data-stu-id="52fd7-126">Logical functions</span></span>](er-functions-category-logical.md)
