---
title: FILTER ER-toiminto
description: Tässä ohjeaiheessa on tietoja siitä, miten sähköisen raportoinnin (ER) FILTER-funktiota käytetään.
author: NickSelin
manager: kfend
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
ms.openlocfilehash: 0e90db1836a93dab42be5dc91e9ea478163a1437
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/09/2021
ms.locfileid: "5559696"
---
# <a name="filter-er-function"></a><span data-ttu-id="c7fcc-103">FILTER ER-toiminto</span><span class="sxs-lookup"><span data-stu-id="c7fcc-103">FILTER ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c7fcc-104">`FILTER` funktio palauttaa määritetyn luettelon *tietueluettelon* arvoksi sen jälkeen, kun kyselyä on muutettu niin, että se suodattaa määritetyn ehdon.</span><span class="sxs-lookup"><span data-stu-id="c7fcc-104">The `FILTER` function returns the specified list as a *Record list* value after the query has been changed so that it filters for the specified condition.</span></span>

## <a name="syntax"></a><span data-ttu-id="c7fcc-105">Syntaksi</span><span class="sxs-lookup"><span data-stu-id="c7fcc-105">Syntax</span></span>

```vb
FILTER (list, condition)
```

## <a name="arguments"></a><span data-ttu-id="c7fcc-106">Argumentit</span><span class="sxs-lookup"><span data-stu-id="c7fcc-106">Arguments</span></span>

<span data-ttu-id="c7fcc-107">`list`: *Tietueluettelo*</span><span class="sxs-lookup"><span data-stu-id="c7fcc-107">`list`: *Record list*</span></span>

<span data-ttu-id="c7fcc-108">*Tietueluettelo*-tietotyypin tietolähteen kelvollinen polku.</span><span class="sxs-lookup"><span data-stu-id="c7fcc-108">The valid path of a data source of the *Record list* data type.</span></span>

<span data-ttu-id="c7fcc-109">`condition`: *Totuusarvo*</span><span class="sxs-lookup"><span data-stu-id="c7fcc-109">`condition`: *Boolean*</span></span>

<span data-ttu-id="c7fcc-110">Kelvollinen ehtolauseke, jota käytetään määritetyn luettelon tietueiden suodattamiseen.</span><span class="sxs-lookup"><span data-stu-id="c7fcc-110">A valid conditional expression that is used to filter records of the specified list.</span></span>

## <a name="return-values"></a><span data-ttu-id="c7fcc-111">Palautusarvot</span><span class="sxs-lookup"><span data-stu-id="c7fcc-111">Return values</span></span>

<span data-ttu-id="c7fcc-112">*Tietueluettelo*</span><span class="sxs-lookup"><span data-stu-id="c7fcc-112">*Record list*</span></span>

<span data-ttu-id="c7fcc-113">Tuloksena oleva tietueluettelo.</span><span class="sxs-lookup"><span data-stu-id="c7fcc-113">The resulting list of records.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="c7fcc-114">Käyttöhuomautukset</span><span class="sxs-lookup"><span data-stu-id="c7fcc-114">Usage notes</span></span>

<span data-ttu-id="c7fcc-115">Funktio eroaa [WHERE](er-functions-list-where.md)-funktiosta, koska määritettyä ehtoa käytetään tietokannan tasolla kaikkiin *Taulukkotietue*-tyypin elektronisen raportoinnin (ER) tietolähteisiin.</span><span class="sxs-lookup"><span data-stu-id="c7fcc-115">This function differs from the [WHERE](er-functions-list-where.md) function, because the specified condition is applied to any Electronic reporting (ER) data source of the *Table records* type at the database level.</span></span> <span data-ttu-id="c7fcc-116">Luettelo ja ehto voidaan määrittää tauluja ja suhteita käyttämällä.</span><span class="sxs-lookup"><span data-stu-id="c7fcc-116">The list and condition can be defined by using tables and relations.</span></span>

<span data-ttu-id="c7fcc-117">Jos jompikumpi tai molemmat tälle toiminnolle määritetyt argumentit (`list` ja `condition`) eivät salli tämän pyynnön kääntyä suoraan SQL-puheluun, suunnitteluaikaan tulee poikkeus.</span><span class="sxs-lookup"><span data-stu-id="c7fcc-117">If one or both arguments that are configured for this function (`list` and `condition`) don't allow this request to be translated to the direct SQL call, an exception is thrown at design time.</span></span> <span data-ttu-id="c7fcc-118">Tämä poikkeus ilmoittaa käyttäjälle, että joko `list` tai `condition` ei voi käyttää tietokannan kyselyä.</span><span class="sxs-lookup"><span data-stu-id="c7fcc-118">This exception informs the user that either `list` or `condition` can't be used to query the database.</span></span>

## <a name="example-1"></a><span data-ttu-id="c7fcc-119">Esimerkki 1</span><span class="sxs-lookup"><span data-stu-id="c7fcc-119">Example 1</span></span>

<span data-ttu-id="c7fcc-120">Jos **Toimittaja** on määritetty VendTable-tauluun viittaavaksi ER-tietolähteeksi, lauseke `FILTER (Vendors, Vendors.VendGroup = "40")` palauttaa luettelon toimittajista, jotka kuuluvat vain toimittajaryhmään 40.</span><span class="sxs-lookup"><span data-stu-id="c7fcc-120">If **Vendor** is configured as an ER data source that refers to the VendTable table, the expression `FILTER (Vendors, Vendors.VendGroup = "40")` returns a list of only vendors that belong to vendor group 40.</span></span>

## <a name="example-2"></a><span data-ttu-id="c7fcc-121">Esimerkki 2</span><span class="sxs-lookup"><span data-stu-id="c7fcc-121">Example 2</span></span>

<span data-ttu-id="c7fcc-122">Jos **Toimittaja** määritetään VendTable-tauluun viittaavaksi ER-tietolähteeksi ja ER-tietolähteeksi määritetty **parmVendorBankGroup** palauttaa *String*-tietotyypin arvon, `FILTER ( Vendor.'<Relations'.VendBankAccount, Vendor.'<Relations'.VendBankAccount.BankGroupID = parmVendorBankGroup)` palauttaa luettelon vain niistä toimittajatileistä, jotka kuuluvat tiettyyn pankkiryhmään.</span><span class="sxs-lookup"><span data-stu-id="c7fcc-122">If **Vendor** is configured as an ER data source that refers to the VendTable table, and if **parmVendorBankGroup** is configured as an ER data source that returns a value of the *String* data type, the expression `FILTER ( Vendor.'<Relations'.VendBankAccount, Vendor.'<Relations'.VendBankAccount.BankGroupID = parmVendorBankGroup)` returns a list of only vendor accounts that belong to a specific bank group.</span></span>

## <a name="example-3"></a><span data-ttu-id="c7fcc-123">Esimerkki 3</span><span class="sxs-lookup"><span data-stu-id="c7fcc-123">Example 3</span></span>

<span data-ttu-id="c7fcc-124">Syötät *Lasketun kenttä*-tyypin **DS**-tietolähteen, ja se sisältää lausekkeen `SPLIT ("A,B,C", ",")`.</span><span class="sxs-lookup"><span data-stu-id="c7fcc-124">You enter data source **DS** of the *Calculated field* type, and it contains the expression `SPLIT ("A,B,C", ",")`.</span></span> <span data-ttu-id="c7fcc-125">Kirjoita sitten toinen lauseke `FILTER( DS, DS.Value = "B")`.</span><span class="sxs-lookup"><span data-stu-id="c7fcc-125">You then enter another expression, `FILTER( DS, DS.Value = "B")`.</span></span> <span data-ttu-id="c7fcc-126">Kun yrität tallentaa lausekkeen ER-kaavan suunnittelutoimintoon, seuraava poikkeus hylätään: "Vahvistusvirhe: suodatusfunktion luettelolauseke ei ole kyseltävä."</span><span class="sxs-lookup"><span data-stu-id="c7fcc-126">When you try to save this expression in the ER formula designer, the following exception is thrown: "Validation error: The list expression of FILTER function is not queryable."</span></span>

## <a name="additional-resources"></a><span data-ttu-id="c7fcc-127">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="c7fcc-127">Additional resources</span></span>

[<span data-ttu-id="c7fcc-128">Luettelotoiminnot</span><span class="sxs-lookup"><span data-stu-id="c7fcc-128">List functions</span></span>](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]