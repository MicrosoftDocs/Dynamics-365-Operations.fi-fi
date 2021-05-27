---
title: LISTJOIN ER-funktio
description: Tässä ohjeaiheessa on tietoja siitä, miten sähköisen raportoinnin (ER) LISTJOIN-funktiota käytetään.
author: NickSelin
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
ms.openlocfilehash: 9b300cef0a508f7cc37397480738091158efdead
ms.sourcegitcommit: cabd991fda2bfcabb55db84c225b24a7bb061631
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/12/2021
ms.locfileid: "6027912"
---
# <a name="listjoin-er-function"></a><span data-ttu-id="b7e51-103">LISTJOIN ER-funktio</span><span class="sxs-lookup"><span data-stu-id="b7e51-103">LISTJOIN ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b7e51-104">`LISTJOIN`-funktio palauttaa *Tietueluettelon* arvon, joka edustaa uutta liitettyä tietueluetteloa, joka luodaan määritetyistä argumenteista.</span><span class="sxs-lookup"><span data-stu-id="b7e51-104">The `LISTJOIN` function returns a *Record list* value that represents a new joined list of records that is created from the specified arguments.</span></span>

## <a name="syntax"></a><span data-ttu-id="b7e51-105">Syntaksi</span><span class="sxs-lookup"><span data-stu-id="b7e51-105">Syntax</span></span>

```vb
LISTJOIN (list 1 [, list 2, …, list N])
```

## <a name="arguments"></a><span data-ttu-id="b7e51-106">Argumentit</span><span class="sxs-lookup"><span data-stu-id="b7e51-106">Arguments</span></span>

<span data-ttu-id="b7e51-107">`list 1`: *Tietueluettelo*</span><span class="sxs-lookup"><span data-stu-id="b7e51-107">`list 1`: *Record list*</span></span>

<span data-ttu-id="b7e51-108">Viittaus *Tietueluettelon* tietotyypin tietolähteeseen.</span><span class="sxs-lookup"><span data-stu-id="b7e51-108">A reference to a data source of the *Record list* data type.</span></span> <span data-ttu-id="b7e51-109">Tämä argumentti on pakollinen.</span><span class="sxs-lookup"><span data-stu-id="b7e51-109">This argument is mandatory.</span></span>

<span data-ttu-id="b7e51-110">`list N`: *Tietueluettelo*</span><span class="sxs-lookup"><span data-stu-id="b7e51-110">`list N`: *Record list*</span></span>

<span data-ttu-id="b7e51-111">Viittaus *Tietueluettelon* tietotyypin tietolähteeseen.</span><span class="sxs-lookup"><span data-stu-id="b7e51-111">A reference to a data source of the *Record list* data type.</span></span> <span data-ttu-id="b7e51-112">Nämä lisäargumentit ovat valinnaisia.</span><span class="sxs-lookup"><span data-stu-id="b7e51-112">These additional arguments are optional.</span></span>

## <a name="return-values"></a><span data-ttu-id="b7e51-113">Palautusarvot</span><span class="sxs-lookup"><span data-stu-id="b7e51-113">Return values</span></span>

<span data-ttu-id="b7e51-114">*Tietueluettelo*</span><span class="sxs-lookup"><span data-stu-id="b7e51-114">*Record list*</span></span>

<span data-ttu-id="b7e51-115">Tuloksena oleva tietueluettelo.</span><span class="sxs-lookup"><span data-stu-id="b7e51-115">The resulting list of records.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="b7e51-116">Käyttöhuomautukset</span><span class="sxs-lookup"><span data-stu-id="b7e51-116">Usage notes</span></span>

<span data-ttu-id="b7e51-117">Luodun luettelon rakenne sisältää vain kentät, jotka ovat läsnä jokaisessa argumentissa mainitun tietueluettelon rakenteessa.</span><span class="sxs-lookup"><span data-stu-id="b7e51-117">The structure of the list that is created contains only the fields that are present in the structure of every record list that is referenced in the arguments.</span></span>

## <a name="example"></a><span data-ttu-id="b7e51-118">Esimerkki</span><span class="sxs-lookup"><span data-stu-id="b7e51-118">Example</span></span>

<span data-ttu-id="b7e51-119">Syötät `Container`-tyypin **Tietue 1**:n tietolähteen.</span><span class="sxs-lookup"><span data-stu-id="b7e51-119">You enter data source **Record 1** of the `Container` type.</span></span> <span data-ttu-id="b7e51-120">Tämä tietolähde sisältää seuraavat `Calculated field` -tyypin sisäkkäiset kentät:</span><span class="sxs-lookup"><span data-stu-id="b7e51-120">This data source contains the following nested fields of the `Calculated field` type:</span></span>

- <span data-ttu-id="b7e51-121">**Koodi**: Tässä kentässä on lauseke, joka palauttaa `String`-tyypin arvon.</span><span class="sxs-lookup"><span data-stu-id="b7e51-121">**Code**: This field contains an expression that returns a value of the `String` type.</span></span>
- <span data-ttu-id="b7e51-122">**Summa**: Tässä kentässä on lauseke, joka palauttaa `Real`-tyypin arvon.</span><span class="sxs-lookup"><span data-stu-id="b7e51-122">**Amount**: This field contains an expression that returns a value of the `Real` type.</span></span>

<span data-ttu-id="b7e51-123">Syötä sitten `Container`-tyypin **Tietue 2**:n tietolähde.</span><span class="sxs-lookup"><span data-stu-id="b7e51-123">You then enter data source **Record 2** of the `Container` type.</span></span> <span data-ttu-id="b7e51-124">Tämä tietolähde sisältää seuraavat `Calculated field` -tyypin sisäkkäiset kentät:</span><span class="sxs-lookup"><span data-stu-id="b7e51-124">This data source contains the following nested fields of the `Calculated field` type:</span></span>

- <span data-ttu-id="b7e51-125">**Summa**: Tässä kentässä on lauseke, joka palauttaa `Real`-tyypin arvon.</span><span class="sxs-lookup"><span data-stu-id="b7e51-125">**Amount**: This field contains an expression that returns a value of the `Real` type.</span></span>
- <span data-ttu-id="b7e51-126">**IsValid**: Tässä kentässä on lauseke, joka palauttaa `Boolean`-tyypin arvon.</span><span class="sxs-lookup"><span data-stu-id="b7e51-126">**IsValid**: This field contains an expression that returns a value of the `Boolean` type.</span></span>

![ER-mallimäärityksen suunnittelun sivu](./media/er-functions-list-listjoin-image1.gif)

<span data-ttu-id="b7e51-128">Tässä tapauksessa lauseke `LISTJOIN(LIST('Record 1'), LIST('Record 2'))` palauttaa uuden luettelon, joka sisältää kaksi tietuetta.</span><span class="sxs-lookup"><span data-stu-id="b7e51-128">In this case, the expression `LISTJOIN(LIST('Record 1'), LIST('Record 2'))` returns a new list that contains two records.</span></span>

![Sähköisen raportoinnin mallivastaavuusmäärityksen suunnittelun sivu ja kaksi tietuetta](./media/er-functions-list-listjoin-image2.gif)

<span data-ttu-id="b7e51-130">Tämän luettelon rakenne koostuu `Real`-tyypistä, joka on yksittäisessä **Summa**-kentässä, koska tämä kenttä on ainoa kenttä, joka esitetään kutsutun funktion jokaisessa argumentissa.</span><span class="sxs-lookup"><span data-stu-id="b7e51-130">The structure of this list consists of a single **Amount** field of the `Real` type, because this field is the only field that is presented in every argument of the called function.</span></span>

![Sähköisen raportoinnin malliyhdistämismäärityksen suunnittelun sivun summakenttä](./media/er-functions-list-listjoin-image3.gif)

## <a name="additional-resources"></a><span data-ttu-id="b7e51-132">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="b7e51-132">Additional resources</span></span>

[<span data-ttu-id="b7e51-133">Luettelotoiminnot</span><span class="sxs-lookup"><span data-stu-id="b7e51-133">List functions</span></span>](er-functions-category-list.md)

[<span data-ttu-id="b7e51-134">Suoritettavan ER-muodon tietolähteiden vianmääritys tiedonkulun ja muunnoksen analysointia varten</span><span class="sxs-lookup"><span data-stu-id="b7e51-134">Debug data sources of an executed ER format to analyze data flow and transformation</span></span>](er-debug-data-sources.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
