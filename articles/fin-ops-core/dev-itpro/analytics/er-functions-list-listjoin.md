---
title: LISTJOIN ER-funktio
description: Tässä ohjeaiheessa on tietoja siitä, miten sähköisen raportoinnin (ER) LISTJOIN-funktiota käytetään.
author: NickSelin
manager: kfend
ms.date: 04/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 58771
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6713823d8d089a677c39bc2a8b5cfe1d1b23b459
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/09/2021
ms.locfileid: "5563773"
---
# <a name="listjoin-er-function"></a><span data-ttu-id="035f0-103">LISTJOIN ER-funktio</span><span class="sxs-lookup"><span data-stu-id="035f0-103">LISTJOIN ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="035f0-104">`LISTJOIN`-funktio palauttaa *Tietueluettelon* arvon, joka edustaa uutta liitettyä tietueluetteloa, joka luodaan määritetyistä argumenteista.</span><span class="sxs-lookup"><span data-stu-id="035f0-104">The `LISTJOIN` function returns a *Record list* value that represents a new joined list of records that is created from the specified arguments.</span></span>

## <a name="syntax"></a><span data-ttu-id="035f0-105">Syntaksi</span><span class="sxs-lookup"><span data-stu-id="035f0-105">Syntax</span></span>

```vb
LIST (list 1 [, list 2, …, list N])
```

## <a name="arguments"></a><span data-ttu-id="035f0-106">Argumentit</span><span class="sxs-lookup"><span data-stu-id="035f0-106">Arguments</span></span>

<span data-ttu-id="035f0-107">`list 1`: *Tietueluettelo*</span><span class="sxs-lookup"><span data-stu-id="035f0-107">`list 1`: *Record list*</span></span>

<span data-ttu-id="035f0-108">Viittaus *Tietueluettelon* tietotyypin tietolähteeseen.</span><span class="sxs-lookup"><span data-stu-id="035f0-108">A reference to a data source of the *Record list* data type.</span></span> <span data-ttu-id="035f0-109">Tämä argumentti on pakollinen.</span><span class="sxs-lookup"><span data-stu-id="035f0-109">This argument is mandatory.</span></span>

<span data-ttu-id="035f0-110">`list N`: *Tietueluettelo*</span><span class="sxs-lookup"><span data-stu-id="035f0-110">`list N`: *Record list*</span></span>

<span data-ttu-id="035f0-111">Viittaus *Tietueluettelon* tietotyypin tietolähteeseen.</span><span class="sxs-lookup"><span data-stu-id="035f0-111">A reference to a data source of the *Record list* data type.</span></span> <span data-ttu-id="035f0-112">Nämä lisäargumentit ovat valinnaisia.</span><span class="sxs-lookup"><span data-stu-id="035f0-112">These additional arguments are optional.</span></span>

## <a name="return-values"></a><span data-ttu-id="035f0-113">Palautusarvot</span><span class="sxs-lookup"><span data-stu-id="035f0-113">Return values</span></span>

<span data-ttu-id="035f0-114">*Tietueluettelo*</span><span class="sxs-lookup"><span data-stu-id="035f0-114">*Record list*</span></span>

<span data-ttu-id="035f0-115">Tuloksena oleva tietueluettelo.</span><span class="sxs-lookup"><span data-stu-id="035f0-115">The resulting list of records.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="035f0-116">Käyttöhuomautukset</span><span class="sxs-lookup"><span data-stu-id="035f0-116">Usage notes</span></span>

<span data-ttu-id="035f0-117">Luodun luettelon rakenne sisältää vain kentät, jotka ovat läsnä jokaisessa argumentissa mainitun tietueluettelon rakenteessa.</span><span class="sxs-lookup"><span data-stu-id="035f0-117">The structure of the list that is created contains only the fields that are present in the structure of every record list that is referenced in the arguments.</span></span>

## <a name="example"></a><span data-ttu-id="035f0-118">Esimerkki</span><span class="sxs-lookup"><span data-stu-id="035f0-118">Example</span></span>

<span data-ttu-id="035f0-119">Syötät `Container`-tyypin **Tietue 1**:n tietolähteen.</span><span class="sxs-lookup"><span data-stu-id="035f0-119">You enter data source **Record 1** of the `Container` type.</span></span> <span data-ttu-id="035f0-120">Tämä tietolähde sisältää seuraavat `Calculated field` -tyypin sisäkkäiset kentät:</span><span class="sxs-lookup"><span data-stu-id="035f0-120">This data source contains the following nested fields of the `Calculated field` type:</span></span>

- <span data-ttu-id="035f0-121">**Koodi**: Tässä kentässä on lauseke, joka palauttaa `String`-tyypin arvon.</span><span class="sxs-lookup"><span data-stu-id="035f0-121">**Code**: This field contains an expression that returns a value of the `String` type.</span></span>
- <span data-ttu-id="035f0-122">**Summa**: Tässä kentässä on lauseke, joka palauttaa `Real`-tyypin arvon.</span><span class="sxs-lookup"><span data-stu-id="035f0-122">**Amount**: This field contains an expression that returns a value of the `Real` type.</span></span>

<span data-ttu-id="035f0-123">Syötä sitten `Container`-tyypin **Tietue 2**:n tietolähde.</span><span class="sxs-lookup"><span data-stu-id="035f0-123">You then enter data source **Record 2** of the `Container` type.</span></span> <span data-ttu-id="035f0-124">Tämä tietolähde sisältää seuraavat `Calculated field` -tyypin sisäkkäiset kentät:</span><span class="sxs-lookup"><span data-stu-id="035f0-124">This data source contains the following nested fields of the `Calculated field` type:</span></span>

- <span data-ttu-id="035f0-125">**Summa**: Tässä kentässä on lauseke, joka palauttaa `Real`-tyypin arvon.</span><span class="sxs-lookup"><span data-stu-id="035f0-125">**Amount**: This field contains an expression that returns a value of the `Real` type.</span></span>
- <span data-ttu-id="035f0-126">**IsValid**: Tässä kentässä on lauseke, joka palauttaa `Boolean`-tyypin arvon.</span><span class="sxs-lookup"><span data-stu-id="035f0-126">**IsValid**: This field contains an expression that returns a value of the `Boolean` type.</span></span>

![ER-mallimäärityksen suunnittelun sivu](./media/er-functions-list-listjoin-image1.gif)

<span data-ttu-id="035f0-128">Tässä tapauksessa lauseke `LISTJOIN(LIST('Record 1'), LIST('Record 2'))` palauttaa uuden luettelon, joka sisältää kaksi tietuetta.</span><span class="sxs-lookup"><span data-stu-id="035f0-128">In this case, the expression `LISTJOIN(LIST('Record 1'), LIST('Record 2'))` returns a new list that contains two records.</span></span>

![Sähköisen raportoinnin mallivastaavuusmäärityksen suunnittelun sivu ja kaksi tietuetta](./media/er-functions-list-listjoin-image2.gif)

<span data-ttu-id="035f0-130">Tämän luettelon rakenne koostuu `Real`-tyypistä, joka on yksittäisessä **Summa**-kentässä, koska tämä kenttä on ainoa kenttä, joka esitetään kutsutun funktion jokaisessa argumentissa.</span><span class="sxs-lookup"><span data-stu-id="035f0-130">The structure of this list consists of a single **Amount** field of the `Real` type, because this field is the only field that is presented in every argument of the called function.</span></span>

![Sähköisen raportoinnin malliyhdistämismäärityksen suunnittelun sivun summakenttä](./media/er-functions-list-listjoin-image3.gif)

## <a name="additional-resources"></a><span data-ttu-id="035f0-132">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="035f0-132">Additional resources</span></span>

[<span data-ttu-id="035f0-133">Luettelotoiminnot</span><span class="sxs-lookup"><span data-stu-id="035f0-133">List functions</span></span>](er-functions-category-list.md)

[<span data-ttu-id="035f0-134">Suoritettavan ER-muodon tietolähteiden vianmääritys tiedonkulun ja muunnoksen analysointia varten</span><span class="sxs-lookup"><span data-stu-id="035f0-134">Debug data sources of an executed ER format to analyze data flow and transformation</span></span>](er-debug-data-sources.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]