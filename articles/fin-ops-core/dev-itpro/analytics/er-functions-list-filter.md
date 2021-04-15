---
title: FILTER ER-toiminto
description: Tässä ohjeaiheessa on tietoja siitä, miten sähköisen raportoinnin (ER) FILTER-funktiota käytetään.
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
ms.openlocfilehash: aa8c0b4601db625d442dd545151968f38bd58cf1
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2021
ms.locfileid: "5746600"
---
# <a name="filter-er-function"></a><span data-ttu-id="9d0f2-103">FILTER ER-toiminto</span><span class="sxs-lookup"><span data-stu-id="9d0f2-103">FILTER ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9d0f2-104">`FILTER` funktio palauttaa määritetyn luettelon *tietueluettelon* arvoksi sen jälkeen, kun kyselyä on muutettu niin, että se suodattaa määritetyn ehdon.</span><span class="sxs-lookup"><span data-stu-id="9d0f2-104">The `FILTER` function returns the specified list as a *Record list* value after the query has been changed so that it filters for the specified condition.</span></span>

## <a name="syntax"></a><span data-ttu-id="9d0f2-105">Syntaksi</span><span class="sxs-lookup"><span data-stu-id="9d0f2-105">Syntax</span></span>

```vb
FILTER (list, condition)
```

## <a name="arguments"></a><span data-ttu-id="9d0f2-106">Argumentit</span><span class="sxs-lookup"><span data-stu-id="9d0f2-106">Arguments</span></span>

<span data-ttu-id="9d0f2-107">`list`: *Tietueluettelo*</span><span class="sxs-lookup"><span data-stu-id="9d0f2-107">`list`: *Record list*</span></span>

<span data-ttu-id="9d0f2-108">*Tietueluettelo*-tietotyypin tietolähteen kelvollinen polku.</span><span class="sxs-lookup"><span data-stu-id="9d0f2-108">The valid path of a data source of the *Record list* data type.</span></span>

<span data-ttu-id="9d0f2-109">`condition`: *Totuusarvo*</span><span class="sxs-lookup"><span data-stu-id="9d0f2-109">`condition`: *Boolean*</span></span>

<span data-ttu-id="9d0f2-110">Kelvollinen ehtolauseke, jota käytetään määritetyn luettelon tietueiden suodattamiseen.</span><span class="sxs-lookup"><span data-stu-id="9d0f2-110">A valid conditional expression that is used to filter records of the specified list.</span></span>

## <a name="return-values"></a><span data-ttu-id="9d0f2-111">Palautusarvot</span><span class="sxs-lookup"><span data-stu-id="9d0f2-111">Return values</span></span>

<span data-ttu-id="9d0f2-112">*Tietueluettelo*</span><span class="sxs-lookup"><span data-stu-id="9d0f2-112">*Record list*</span></span>

<span data-ttu-id="9d0f2-113">Tuloksena oleva tietueluettelo.</span><span class="sxs-lookup"><span data-stu-id="9d0f2-113">The resulting list of records.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="9d0f2-114">Käyttöhuomautukset</span><span class="sxs-lookup"><span data-stu-id="9d0f2-114">Usage notes</span></span>

<span data-ttu-id="9d0f2-115">Funktio eroaa [WHERE](er-functions-list-where.md)-funktiosta, koska määritettyä ehtoa käytetään tietokannan tasolla kaikkiin *Taulukkotietue*-tyypin elektronisen raportoinnin (ER) tietolähteisiin.</span><span class="sxs-lookup"><span data-stu-id="9d0f2-115">This function differs from the [WHERE](er-functions-list-where.md) function, because the specified condition is applied to any Electronic reporting (ER) data source of the *Table records* type at the database level.</span></span> <span data-ttu-id="9d0f2-116">Luettelo ja ehto voidaan määrittää tauluja ja suhteita käyttämällä.</span><span class="sxs-lookup"><span data-stu-id="9d0f2-116">The list and condition can be defined by using tables and relations.</span></span>

<span data-ttu-id="9d0f2-117">Jos jompikumpi tai molemmat tälle toiminnolle määritetyt argumentit (`list` ja `condition`) eivät salli tämän pyynnön kääntyä suoraan SQL-puheluun, suunnitteluaikaan tulee poikkeus.</span><span class="sxs-lookup"><span data-stu-id="9d0f2-117">If one or both arguments that are configured for this function (`list` and `condition`) don't allow this request to be translated to the direct SQL call, an exception is thrown at design time.</span></span> <span data-ttu-id="9d0f2-118">Tämä poikkeus ilmoittaa käyttäjälle, että joko `list` tai `condition` ei voi käyttää tietokannan kyselyä.</span><span class="sxs-lookup"><span data-stu-id="9d0f2-118">This exception informs the user that either `list` or `condition` can't be used to query the database.</span></span>

## <a name="example-1"></a><span data-ttu-id="9d0f2-119">Esimerkki 1</span><span class="sxs-lookup"><span data-stu-id="9d0f2-119">Example 1</span></span>

<span data-ttu-id="9d0f2-120">Jos **Toimittaja** on määritetty VendTable-tauluun viittaavaksi ER-tietolähteeksi, lauseke `FILTER (Vendors, Vendors.VendGroup = "40")` palauttaa luettelon toimittajista, jotka kuuluvat vain toimittajaryhmään 40.</span><span class="sxs-lookup"><span data-stu-id="9d0f2-120">If **Vendor** is configured as an ER data source that refers to the VendTable table, the expression `FILTER (Vendors, Vendors.VendGroup = "40")` returns a list of only vendors that belong to vendor group 40.</span></span>

## <a name="example-2"></a><span data-ttu-id="9d0f2-121">Esimerkki 2</span><span class="sxs-lookup"><span data-stu-id="9d0f2-121">Example 2</span></span>

<span data-ttu-id="9d0f2-122">Jos **Toimittaja** määritetään VendTable-tauluun viittaavaksi ER-tietolähteeksi ja ER-tietolähteeksi määritetty **parmVendorBankGroup** palauttaa *String*-tietotyypin arvon, `FILTER ( Vendor.'<Relations'.VendBankAccount, Vendor.'<Relations'.VendBankAccount.BankGroupID = parmVendorBankGroup)` palauttaa luettelon vain niistä toimittajatileistä, jotka kuuluvat tiettyyn pankkiryhmään.</span><span class="sxs-lookup"><span data-stu-id="9d0f2-122">If **Vendor** is configured as an ER data source that refers to the VendTable table, and if **parmVendorBankGroup** is configured as an ER data source that returns a value of the *String* data type, the expression `FILTER ( Vendor.'<Relations'.VendBankAccount, Vendor.'<Relations'.VendBankAccount.BankGroupID = parmVendorBankGroup)` returns a list of only vendor accounts that belong to a specific bank group.</span></span>

## <a name="example-3"></a><span data-ttu-id="9d0f2-123">Esimerkki 3</span><span class="sxs-lookup"><span data-stu-id="9d0f2-123">Example 3</span></span>

<span data-ttu-id="9d0f2-124">Syötät *Lasketun kenttä*-tyypin **DS**-tietolähteen, ja se sisältää lausekkeen `SPLIT ("A,B,C", ",")`.</span><span class="sxs-lookup"><span data-stu-id="9d0f2-124">You enter data source **DS** of the *Calculated field* type, and it contains the expression `SPLIT ("A,B,C", ",")`.</span></span> <span data-ttu-id="9d0f2-125">Kirjoita sitten toinen lauseke `FILTER( DS, DS.Value = "B")`.</span><span class="sxs-lookup"><span data-stu-id="9d0f2-125">You then enter another expression, `FILTER( DS, DS.Value = "B")`.</span></span> <span data-ttu-id="9d0f2-126">Kun yrität tallentaa lausekkeen ER-kaavan suunnittelutoimintoon, seuraava poikkeus hylätään: "Vahvistusvirhe: suodatusfunktion luettelolauseke ei ole kyseltävä."</span><span class="sxs-lookup"><span data-stu-id="9d0f2-126">When you try to save this expression in the ER formula designer, the following exception is thrown: "Validation error: The list expression of FILTER function is not queryable."</span></span>

## <a name="additional-resources"></a><span data-ttu-id="9d0f2-127">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="9d0f2-127">Additional resources</span></span>

[<span data-ttu-id="9d0f2-128">Luettelotoiminnot</span><span class="sxs-lookup"><span data-stu-id="9d0f2-128">List functions</span></span>](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]