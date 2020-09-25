---
title: LISTJOIN ER-funktio
description: Tässä ohjeaiheessa on tietoja siitä, miten sähköisen raportoinnin (ER) LISTJOIN-funktiota käytetään.
author: NickSelin
manager: kfend
ms.date: 04/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 58771
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 035bf720a892e987ff9fc073ab8ed6f6cc6ea18e
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/01/2020
ms.locfileid: "3745102"
---
# <a name="listjoin-er-function"></a><span data-ttu-id="a7b23-103">LISTJOIN ER-funktio</span><span class="sxs-lookup"><span data-stu-id="a7b23-103">LISTJOIN ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a7b23-104">`LISTJOIN`-funktio palauttaa *Tietueluettelon* arvon, joka edustaa uutta liitettyä tietueluetteloa, joka luodaan määritetyistä argumenteista.</span><span class="sxs-lookup"><span data-stu-id="a7b23-104">The `LISTJOIN` function returns a *Record list* value that represents a new joined list of records that is created from the specified arguments.</span></span>

## <a name="syntax"></a><span data-ttu-id="a7b23-105">Syntaksi</span><span class="sxs-lookup"><span data-stu-id="a7b23-105">Syntax</span></span>

```vb
LIST (list 1 [, list 2, …, list N])
```

## <a name="arguments"></a><span data-ttu-id="a7b23-106">Argumentit</span><span class="sxs-lookup"><span data-stu-id="a7b23-106">Arguments</span></span>

<span data-ttu-id="a7b23-107">`list 1`: *Tietueluettelo*</span><span class="sxs-lookup"><span data-stu-id="a7b23-107">`list 1`: *Record list*</span></span>

<span data-ttu-id="a7b23-108">Viittaus *Tietueluettelon* tietotyypin tietolähteeseen.</span><span class="sxs-lookup"><span data-stu-id="a7b23-108">A reference to a data source of the *Record list* data type.</span></span> <span data-ttu-id="a7b23-109">Tämä argumentti on pakollinen.</span><span class="sxs-lookup"><span data-stu-id="a7b23-109">This argument is mandatory.</span></span>

<span data-ttu-id="a7b23-110">`list N`: *Tietueluettelo*</span><span class="sxs-lookup"><span data-stu-id="a7b23-110">`list N`: *Record list*</span></span>

<span data-ttu-id="a7b23-111">Viittaus *Tietueluettelon* tietotyypin tietolähteeseen.</span><span class="sxs-lookup"><span data-stu-id="a7b23-111">A reference to a data source of the *Record list* data type.</span></span> <span data-ttu-id="a7b23-112">Nämä lisäargumentit ovat valinnaisia.</span><span class="sxs-lookup"><span data-stu-id="a7b23-112">These additional arguments are optional.</span></span>

## <a name="return-values"></a><span data-ttu-id="a7b23-113">Palautusarvot</span><span class="sxs-lookup"><span data-stu-id="a7b23-113">Return values</span></span>

<span data-ttu-id="a7b23-114">*Tietueluettelo*</span><span class="sxs-lookup"><span data-stu-id="a7b23-114">*Record list*</span></span>

<span data-ttu-id="a7b23-115">Tuloksena oleva tietueluettelo.</span><span class="sxs-lookup"><span data-stu-id="a7b23-115">The resulting list of records.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="a7b23-116">Käyttöhuomautukset</span><span class="sxs-lookup"><span data-stu-id="a7b23-116">Usage notes</span></span>

<span data-ttu-id="a7b23-117">Luodun luettelon rakenne sisältää vain kentät, jotka ovat läsnä jokaisessa argumentissa mainitun tietueluettelon rakenteessa.</span><span class="sxs-lookup"><span data-stu-id="a7b23-117">The structure of the list that is created contains only the fields that are present in the structure of every record list that is referenced in the arguments.</span></span>

## <a name="example"></a><span data-ttu-id="a7b23-118">Esimerkki</span><span class="sxs-lookup"><span data-stu-id="a7b23-118">Example</span></span>

<span data-ttu-id="a7b23-119">Syötät `Container`-tyypin **Tietue 1**:n tietolähteen.</span><span class="sxs-lookup"><span data-stu-id="a7b23-119">You enter data source **Record 1** of the `Container` type.</span></span> <span data-ttu-id="a7b23-120">Tämä tietolähde sisältää seuraavat `Calculated field` -tyypin sisäkkäiset kentät:</span><span class="sxs-lookup"><span data-stu-id="a7b23-120">This data source contains the following nested fields of the `Calculated field` type:</span></span>

- <span data-ttu-id="a7b23-121">**Koodi**: Tässä kentässä on lauseke, joka palauttaa `String`-tyypin arvon.</span><span class="sxs-lookup"><span data-stu-id="a7b23-121">**Code**: This field contains an expression that returns a value of the `String` type.</span></span>
- <span data-ttu-id="a7b23-122">**Summa**: Tässä kentässä on lauseke, joka palauttaa `Real`-tyypin arvon.</span><span class="sxs-lookup"><span data-stu-id="a7b23-122">**Amount**: This field contains an expression that returns a value of the `Real` type.</span></span>

<span data-ttu-id="a7b23-123">Syötä sitten `Container`-tyypin **Tietue 2**:n tietolähde.</span><span class="sxs-lookup"><span data-stu-id="a7b23-123">You then enter data source **Record 2** of the `Container` type.</span></span> <span data-ttu-id="a7b23-124">Tämä tietolähde sisältää seuraavat `Calculated field` -tyypin sisäkkäiset kentät:</span><span class="sxs-lookup"><span data-stu-id="a7b23-124">This data source contains the following nested fields of the `Calculated field` type:</span></span>

- <span data-ttu-id="a7b23-125">**Summa**: Tässä kentässä on lauseke, joka palauttaa `Real`-tyypin arvon.</span><span class="sxs-lookup"><span data-stu-id="a7b23-125">**Amount**: This field contains an expression that returns a value of the `Real` type.</span></span>
- <span data-ttu-id="a7b23-126">**IsValid**: Tässä kentässä on lauseke, joka palauttaa `Boolean`-tyypin arvon.</span><span class="sxs-lookup"><span data-stu-id="a7b23-126">**IsValid**: This field contains an expression that returns a value of the `Boolean` type.</span></span>

![ER-mallimäärityksen suunnittelun sivu](./media/er-functions-list-listjoin-image1.gif)

<span data-ttu-id="a7b23-128">Tässä tapauksessa lauseke `LISTJOIN(LIST('Record 1'), LIST('Record 2'))` palauttaa uuden luettelon, joka sisältää kaksi tietuetta.</span><span class="sxs-lookup"><span data-stu-id="a7b23-128">In this case, the expression `LISTJOIN(LIST('Record 1'), LIST('Record 2'))` returns a new list that contains two records.</span></span>

![Sähköisen raportoinnin mallivastaavuusmäärityksen suunnittelun sivu ja kaksi tietuetta](./media/er-functions-list-listjoin-image2.gif)

<span data-ttu-id="a7b23-130">Tämän luettelon rakenne koostuu `Real`-tyypistä, joka on yksittäisessä **Summa**-kentässä, koska tämä kenttä on ainoa kenttä, joka esitetään kutsutun funktion jokaisessa argumentissa.</span><span class="sxs-lookup"><span data-stu-id="a7b23-130">The structure of this list consists of a single **Amount** field of the `Real` type, because this field is the only field that is presented in every argument of the called function.</span></span>

![Sähköisen raportoinnin malliyhdistämismäärityksen suunnittelun sivun summakenttä](./media/er-functions-list-listjoin-image3.gif)

## <a name="additional-resources"></a><span data-ttu-id="a7b23-132">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="a7b23-132">Additional resources</span></span>

[<span data-ttu-id="a7b23-133">Luettelotoiminnot</span><span class="sxs-lookup"><span data-stu-id="a7b23-133">List functions</span></span>](er-functions-category-list.md)

[<span data-ttu-id="a7b23-134">Suoritettavan ER-muodon tietolähteiden vianmääritys tiedonkulun ja muunnoksen analysointia varten</span><span class="sxs-lookup"><span data-stu-id="a7b23-134">Debug data sources of an executed ER format to analyze data flow and transformation</span></span>](er-debug-data-sources.md)
