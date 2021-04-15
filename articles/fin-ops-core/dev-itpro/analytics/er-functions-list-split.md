---
title: SPLIT ER-funktio
description: Tässä ohjeaiheessa on tietoja siitä, miten sähköisen raportoinnin (ER) SPLIT-funktiota käytetään.
author: NickSelin
ms.date: 12/12/2019
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
ms.openlocfilehash: 5c99ee5e8129ed45253893dc83acdef99b4ce2c9
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2021
ms.locfileid: "5745590"
---
# <a name="split-er-function"></a><span data-ttu-id="18357-103">SPLIT ER-funktio</span><span class="sxs-lookup"><span data-stu-id="18357-103">SPLIT ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="18357-104">`SPLIT`-funktio jakaa määritetyn syötemerkkijonon arvon alimerkkijonoiksi ja palauttaa tuloksen uudeksi *Tietueluettelon* arvoksi.</span><span class="sxs-lookup"><span data-stu-id="18357-104">The `SPLIT` function splits the specified input string into substrings and returns the result as a new *Record list* value.</span></span>

## <a name="syntax-1"></a><span data-ttu-id="18357-105">Syntaksi 1</span><span class="sxs-lookup"><span data-stu-id="18357-105">Syntax 1</span></span>

```vb
SPLIT (input, length)
```

<span data-ttu-id="18357-106">Tätä syntaksia käytetään jakamaan määritetty syötemerkkijono alimerkkijonoiksi, joilla on tietty pituus.</span><span class="sxs-lookup"><span data-stu-id="18357-106">This syntax is used to split the specified input string into substrings, each of which has the specified length.</span></span>

## <a name="syntax-2"></a><span data-ttu-id="18357-107">Syntaksi 2</span><span class="sxs-lookup"><span data-stu-id="18357-107">Syntax 2</span></span>

```vb
SPLIT (input, delimiter)
```

<span data-ttu-id="18357-108">Tätä syntaksia käytetään jakamaan määritetty syötemerkkijono alimerkkijonoiksi määritetyn erottimen perusteella.</span><span class="sxs-lookup"><span data-stu-id="18357-108">This syntax is used to split the specified input string into substrings, based on the specified delimiter.</span></span>

## <a name="arguments"></a><span data-ttu-id="18357-109">Argumentit</span><span class="sxs-lookup"><span data-stu-id="18357-109">Arguments</span></span>

<span data-ttu-id="18357-110">`input`: *Merkkijono*</span><span class="sxs-lookup"><span data-stu-id="18357-110">`input`: *String*</span></span>

<span data-ttu-id="18357-111">Jaettava teksti.</span><span class="sxs-lookup"><span data-stu-id="18357-111">The text to split.</span></span>

<span data-ttu-id="18357-112">`length`: *Kokonaisluku*</span><span class="sxs-lookup"><span data-stu-id="18357-112">`length`: *Integer*</span></span>

<span data-ttu-id="18357-113">Yksittäisen alimerkkijonon enimmäispituus.</span><span class="sxs-lookup"><span data-stu-id="18357-113">The maximum length of a single substring.</span></span>

<span data-ttu-id="18357-114">`delimiter`: *Merkkijono*</span><span class="sxs-lookup"><span data-stu-id="18357-114">`delimiter`: *String*</span></span>

<span data-ttu-id="18357-115">Erotin, jota käytetään erottelemaan alimerkkijonoja.</span><span class="sxs-lookup"><span data-stu-id="18357-115">A delimiter that is used to separate substrings.</span></span>

## <a name="return-values"></a><span data-ttu-id="18357-116">Palautusarvot</span><span class="sxs-lookup"><span data-stu-id="18357-116">Return values</span></span>

<span data-ttu-id="18357-117">*Tietueluettelo*</span><span class="sxs-lookup"><span data-stu-id="18357-117">*Record list*</span></span>

<span data-ttu-id="18357-118">Tuloksena oleva tietueluettelo.</span><span class="sxs-lookup"><span data-stu-id="18357-118">The resulting list of records.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="18357-119">Käyttöhuomautukset</span><span class="sxs-lookup"><span data-stu-id="18357-119">Usage notes</span></span>

<span data-ttu-id="18357-120">Palautettavan luettelon tietuerakenne koostuu *Merkkijono*-tyypin **Arvo**-kentästä.</span><span class="sxs-lookup"><span data-stu-id="18357-120">The record structure of the list that is returned consists of the **Value** field of the *String* type.</span></span> <span data-ttu-id="18357-121">Jokainen palautettavan luettelon tietue sisältää tämän kentän luotuja alimerkkijonoja.</span><span class="sxs-lookup"><span data-stu-id="18357-121">Every record of the list that is returned contains generated substrings in this field.</span></span>

<span data-ttu-id="18357-122">Jos `delimiter`-argumentti on tyhjä, palautettu uusi luettelo koostuu yhdestä tietueesta, jolla on *merkkijono*-tyypin **Arvo**-kenttä.</span><span class="sxs-lookup"><span data-stu-id="18357-122">If the `delimiter` argument is empty, the new list that is returned consists of one record that has the **Value** field of the *String* type.</span></span> <span data-ttu-id="18357-123">Tässä kentässä on syöteteksti.</span><span class="sxs-lookup"><span data-stu-id="18357-123">This field contains the input text.</span></span>

<span data-ttu-id="18357-124">Jos `input`-argumentti on tyhjä, palautettava uusi luettelo on tyhjä.</span><span class="sxs-lookup"><span data-stu-id="18357-124">If the `input` argument is empty, a new empty list is returned.</span></span> <span data-ttu-id="18357-125">Jos `input`- tai `delimiter`-argumentti on määrittämättä (tyhjäarvo), sovellus antaa poikkeuksen.</span><span class="sxs-lookup"><span data-stu-id="18357-125">If either the `input` or `delimiter` argument is unspecified (null), an application exception is thrown.</span></span>

## <a name="example-1"></a><span data-ttu-id="18357-126">Esimerkki 1</span><span class="sxs-lookup"><span data-stu-id="18357-126">Example 1</span></span>

<span data-ttu-id="18357-127">`SPLIT ("abcd", 3)` palauttaa uuden luettelon, joka sisältää kaksi tietuetta, joilla on *Merkkijono*-tyypin **Arvo**-kenttä.</span><span class="sxs-lookup"><span data-stu-id="18357-127">`SPLIT ("abcd", 3)` returns a new list that consists of two records that have the **Value** field of the *String* type.</span></span> <span data-ttu-id="18357-128">Ensimmäisen tietueen **Arvo**-kenttä sisältää tekstin **abc** ja toisen tietueen **Arvo**-kenttä tekstin **d**.</span><span class="sxs-lookup"><span data-stu-id="18357-128">The **Value** field in the first record contains the text **"abc"**, and the **Value** field in the second record contains the text **"d"**.</span></span>

## <a name="example-2"></a><span data-ttu-id="18357-129">Esimerkki 2</span><span class="sxs-lookup"><span data-stu-id="18357-129">Example 2</span></span>

<span data-ttu-id="18357-130">`SPLIT ("XAb aBy", "aB")` palauttaa uuden luettelon, joka sisältää kolme tietuetta, joilla on *Merkkijono*-tyypin **Arvo**-kenttä.</span><span class="sxs-lookup"><span data-stu-id="18357-130">`SPLIT ("XAb aBy", "aB")` returns a new list that consists of three records that have the **Value** field of the *String* type.</span></span> <span data-ttu-id="18357-131">Ensimmäisen tietueen **Arvo**-kentässä on teksti **X**, toisen tietueen **Arvo**-kentässä teksti **&nbsp;** ja kolmannen tietueen **Arvo**-kentässä teksti **y**.</span><span class="sxs-lookup"><span data-stu-id="18357-131">The **Value** field in the first record contains the text **"X"**, the **Value** field in the second record contains the text **"&nbsp;"**, and the **Value** field in the third record contains the text **"y"**.</span></span> 

## <a name="additional-resources"></a><span data-ttu-id="18357-132">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="18357-132">Additional resources</span></span>

[<span data-ttu-id="18357-133">Luettelotoiminnot</span><span class="sxs-lookup"><span data-stu-id="18357-133">List functions</span></span>](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]