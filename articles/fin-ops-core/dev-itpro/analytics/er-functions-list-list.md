---
title: LIST ER -funktio
description: Tässä ohjeaiheessa on tietoja siitä, miten sähköisen raportoinnin (ER) LIST-funktiota käytetään.
author: NickSelin
manager: kfend
ms.date: 12/12/2019
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
ms.openlocfilehash: 6848fe535a6a588eaf06f96e93f28db9ef304940
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/20/2019
ms.locfileid: "2917278"
---
# <span data-ttu-id="fe379-103"><a name="LIST">LIST ER -funktio</a></span><span class="sxs-lookup"><span data-stu-id="fe379-103"><a name="LIST">LIST ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="fe379-104">`LIST`-funktio palauttaa *Tietueluettelon* arvon, joka sisältää uuden tietueluettelon, joka luodaan määritetyistä argumenteista.</span><span class="sxs-lookup"><span data-stu-id="fe379-104">The `LIST` function returns a *Record list* value that consists of a new list of records that is created from the specified arguments.</span></span>

## <a name="syntax"></a><span data-ttu-id="fe379-105">Syntaksi</span><span class="sxs-lookup"><span data-stu-id="fe379-105">Syntax</span></span>

```
LIST (record 1 [, record 2, …, record N])
```

## <a name="arguments"></a><span data-ttu-id="fe379-106">Argumentit</span><span class="sxs-lookup"><span data-stu-id="fe379-106">Arguments</span></span>

<span data-ttu-id="fe379-107">`record 1`: *Kontti (tietue)*</span><span class="sxs-lookup"><span data-stu-id="fe379-107">`record 1`: *Container (record)*</span></span>

<span data-ttu-id="fe379-108">Viittaus *Tietueen* tietotyypin tietolähteeseen.</span><span class="sxs-lookup"><span data-stu-id="fe379-108">A reference to a data source of the *Record* data type.</span></span> <span data-ttu-id="fe379-109">Tämä argumentti on pakollinen.</span><span class="sxs-lookup"><span data-stu-id="fe379-109">This argument is required.</span></span>

<span data-ttu-id="fe379-110">`record N`: *Kontti (tietue)*</span><span class="sxs-lookup"><span data-stu-id="fe379-110">`record N`: *Container (record)*</span></span>

<span data-ttu-id="fe379-111">Viittaus *Tietueen* tietotyypin tietolähteeseen.</span><span class="sxs-lookup"><span data-stu-id="fe379-111">A reference to a data source of the *Record* data type.</span></span> <span data-ttu-id="fe379-112">Nämä lisäargumentit ovat valinnaisia.</span><span class="sxs-lookup"><span data-stu-id="fe379-112">These additional arguments are optional.</span></span>

## <a name="return-values"></a><span data-ttu-id="fe379-113">Palautusarvot</span><span class="sxs-lookup"><span data-stu-id="fe379-113">Return values</span></span>

<span data-ttu-id="fe379-114">*Tietueluettelo*</span><span class="sxs-lookup"><span data-stu-id="fe379-114">*Record list*</span></span>

<span data-ttu-id="fe379-115">Tuloksena oleva tietueluettelo.</span><span class="sxs-lookup"><span data-stu-id="fe379-115">The resulting list of records.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="fe379-116">Käyttöhuomautukset</span><span class="sxs-lookup"><span data-stu-id="fe379-116">Usage notes</span></span>

<span data-ttu-id="fe379-117">Luodun luettelon rakenne sisältää vain kentät, jotka on esitetty jokaisessa argumentissa mainitun tietueen rakenteessa.</span><span class="sxs-lookup"><span data-stu-id="fe379-117">The structure of the list that is created contains only the fields that are presented in the structure of every record that is mentioned in the arguments.</span></span>

## <a name="example"></a><span data-ttu-id="fe379-118">Esimerkki</span><span class="sxs-lookup"><span data-stu-id="fe379-118">Example</span></span>

<span data-ttu-id="fe379-119">Syötät *Säilö*-tyypin **Tietueen 1**:n tietolähteen.</span><span class="sxs-lookup"><span data-stu-id="fe379-119">You enter data source **Record 1** of the *Container* type.</span></span> <span data-ttu-id="fe379-120">Tämä tietolähde sisältää seuraavat *Lasketun kentän* tyypin sisäkkäiset kentät:</span><span class="sxs-lookup"><span data-stu-id="fe379-120">This data source contains the following nested fields of the *Calculated field* type:</span></span>

- <span data-ttu-id="fe379-121">**Koodi:** Tässä kentässä on lauseke, joka palauttaa *merkkijono*-tyypin arvon.</span><span class="sxs-lookup"><span data-stu-id="fe379-121">**Code:** This field contains an expression that returns a value of the *String* type.</span></span>
- <span data-ttu-id="fe379-122">**Määrä:** Tässä kentässä on lauseke, joka palauttaa *Todellisen* tyypin arvon.</span><span class="sxs-lookup"><span data-stu-id="fe379-122">**Amount:** This field contains an expression that returns a value of the *Real* type.</span></span>

<span data-ttu-id="fe379-123">Syötät sitten *Säilö*-tyypin **Tietueen 2**:n tietolähteen.</span><span class="sxs-lookup"><span data-stu-id="fe379-123">You then enter data source **Record 2** of the *Container* type.</span></span> <span data-ttu-id="fe379-124">Tämä tietolähde sisältää seuraavat *Lasketun kentän* tyypin sisäkkäiset kentät:</span><span class="sxs-lookup"><span data-stu-id="fe379-124">This data source contains the following nested fields of the *Calculated field* type:</span></span>

- <span data-ttu-id="fe379-125">**Määrä:** Tässä kentässä on lauseke, joka palauttaa *Todellisen* tyypin arvon.</span><span class="sxs-lookup"><span data-stu-id="fe379-125">**Amount:** This field contains an expression that returns a value of the *Real* type.</span></span>
- <span data-ttu-id="fe379-126">**IsValid:** Tässä kentässä on lauseke, joka palauttaa *Totuusarvon* tyypin arvon.</span><span class="sxs-lookup"><span data-stu-id="fe379-126">**IsValid:** This field contains an expression that returns a value of the *Boolean* type.</span></span>

<span data-ttu-id="fe379-127">Tässä tapauksessa lauseke `LIST('Record 1', 'Record 2')` palauttaa uuden luettelon, joka sisältää kaksi tietuetta.</span><span class="sxs-lookup"><span data-stu-id="fe379-127">In this case, the expression `LIST('Record 1', 'Record 2')` returns a new list that contains two records.</span></span> <span data-ttu-id="fe379-128">Tämän luettelon rakenne koostuu *todellisesta* tyypistä, joka on yksittäisessä **summa**-kentässä, koska tämä kenttä on ainoa kenttä, joka esitetään kutsutun funktion jokaisessa argumentissa.</span><span class="sxs-lookup"><span data-stu-id="fe379-128">The structure of this list consists of a single **Amount** field of the *Real* type, because this field is the only field that is presented in every argument of the called function.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="fe379-129">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="fe379-129">Additional resources</span></span>

[<span data-ttu-id="fe379-130">Luettelotoiminnot</span><span class="sxs-lookup"><span data-stu-id="fe379-130">List functions</span></span>](er-functions-category-list.md)
