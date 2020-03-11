---
title: FILTER ER-toiminto
description: Tässä ohjeaiheessa on tietoja siitä, miten sähköisen raportoinnin (ER) FILTER-funktiota käytetään.
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
ms.openlocfilehash: adeefd08531f59e478efbb45ab294b3bc8216f4c
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/12/2020
ms.locfileid: "3042133"
---
# <span data-ttu-id="71710-103"><a name="FILTER">FILTER ER-toiminto</a></span><span class="sxs-lookup"><span data-stu-id="71710-103"><a name="FILTER">FILTER ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="71710-104">`FILTER` funktio palauttaa määritetyn luettelon *tietueluettelon* arvoksi sen jälkeen, kun kyselyä on muutettu niin, että se suodattaa määritetyn ehdon.</span><span class="sxs-lookup"><span data-stu-id="71710-104">The `FILTER` function returns the specified list as a *Record list* value after the query has been changed so that it filters for the specified condition.</span></span>

## <a name="syntax"></a><span data-ttu-id="71710-105">Syntaksi</span><span class="sxs-lookup"><span data-stu-id="71710-105">Syntax</span></span>

```vb
FILTER (list, condition)
```

## <a name="arguments"></a><span data-ttu-id="71710-106">Argumentit</span><span class="sxs-lookup"><span data-stu-id="71710-106">Arguments</span></span>

<span data-ttu-id="71710-107">`list`: *Tietueluettelo*</span><span class="sxs-lookup"><span data-stu-id="71710-107">`list`: *Record list*</span></span>

<span data-ttu-id="71710-108">*Tietueluettelo*-tietotyypin tietolähteen kelvollinen polku.</span><span class="sxs-lookup"><span data-stu-id="71710-108">The valid path of a data source of the *Record list* data type.</span></span>

<span data-ttu-id="71710-109">`condition`: *Totuusarvo*</span><span class="sxs-lookup"><span data-stu-id="71710-109">`condition`: *Boolean*</span></span>

<span data-ttu-id="71710-110">Kelvollinen ehtolauseke, jota käytetään määritetyn luettelon tietueiden suodattamiseen.</span><span class="sxs-lookup"><span data-stu-id="71710-110">A valid conditional expression that is used to filter records of the specified list.</span></span>

## <a name="return-values"></a><span data-ttu-id="71710-111">Palautusarvot</span><span class="sxs-lookup"><span data-stu-id="71710-111">Return values</span></span>

<span data-ttu-id="71710-112">*Tietueluettelo*</span><span class="sxs-lookup"><span data-stu-id="71710-112">*Record list*</span></span>

<span data-ttu-id="71710-113">Tuloksena oleva tietueluettelo.</span><span class="sxs-lookup"><span data-stu-id="71710-113">The resulting list of records.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="71710-114">Käyttöhuomautukset</span><span class="sxs-lookup"><span data-stu-id="71710-114">Usage notes</span></span>

<span data-ttu-id="71710-115">Funktio eroaa [WHERE](er-functions-list-where.md)-funktiosta, koska määritettyä ehtoa käytetään tietokannan tasolla kaikkiin *Taulukkotietue*-tyypin elektronisen raportoinnin (ER) tietolähteisiin.</span><span class="sxs-lookup"><span data-stu-id="71710-115">This function differs from the [WHERE](er-functions-list-where.md) function, because the specified condition is applied to any Electronic reporting (ER) data source of the *Table records* type at the database level.</span></span> <span data-ttu-id="71710-116">Luettelo ja ehto voidaan määrittää tauluja ja suhteita käyttämällä.</span><span class="sxs-lookup"><span data-stu-id="71710-116">The list and condition can be defined by using tables and relations.</span></span>

<span data-ttu-id="71710-117">Jos jompikumpi tai molemmat tälle toiminnolle määritetyt argumentit (`list` ja `condition`) eivät salli tämän pyynnön kääntyä suoraan SQL-puheluun, suunnitteluaikaan tulee poikkeus.</span><span class="sxs-lookup"><span data-stu-id="71710-117">If one or both arguments that are configured for this function (`list` and `condition`) don't allow this request to be translated to the direct SQL call, an exception is thrown at design time.</span></span> <span data-ttu-id="71710-118">Tämä poikkeus ilmoittaa käyttäjälle, että joko `list` tai `condition` ei voi käyttää tietokannan kyselyä.</span><span class="sxs-lookup"><span data-stu-id="71710-118">This exception informs the user that either `list` or `condition` can't be used to query the database.</span></span>

## <a name="example-1"></a><span data-ttu-id="71710-119">Esimerkki 1</span><span class="sxs-lookup"><span data-stu-id="71710-119">Example 1</span></span>

<span data-ttu-id="71710-120">Jos **Toimittaja** on määritetty VendTable-tauluun viittaavaksi ER-tietolähteeksi, lauseke `FILTER (Vendors, Vendors.VendGroup = "40")` palauttaa luettelon toimittajista, jotka kuuluvat vain toimittajaryhmään 40.</span><span class="sxs-lookup"><span data-stu-id="71710-120">If **Vendor** is configured as an ER data source that refers to the VendTable table, the expression `FILTER (Vendors, Vendors.VendGroup = "40")` returns a list of only vendors that belong to vendor group 40.</span></span>

## <a name="example-2"></a><span data-ttu-id="71710-121">Esimerkki 2</span><span class="sxs-lookup"><span data-stu-id="71710-121">Example 2</span></span>

<span data-ttu-id="71710-122">Jos **Toimittaja** määritetään VendTable-tauluun viittaavaksi ER-tietolähteeksi ja ER-tietolähteeksi määritetty **parmVendorBankGroup** palauttaa *String*-tietotyypin arvon, `FILTER ( Vendor.'<Relations'.VendBankAccount, Vendor.'<Relations'.VendBankAccount.BankGroupID = parmVendorBankGroup)` palauttaa luettelon vain niistä toimittajatileistä, jotka kuuluvat tiettyyn pankkiryhmään.</span><span class="sxs-lookup"><span data-stu-id="71710-122">If **Vendor** is configured as an ER data source that refers to the VendTable table, and if **parmVendorBankGroup** is configured as an ER data source that returns a value of the *String* data type, the expression `FILTER ( Vendor.'<Relations'.VendBankAccount, Vendor.'<Relations'.VendBankAccount.BankGroupID = parmVendorBankGroup)` returns a list of only vendor accounts that belong to a specific bank group.</span></span>

## <a name="example-3"></a><span data-ttu-id="71710-123">Esimerkki 3</span><span class="sxs-lookup"><span data-stu-id="71710-123">Example 3</span></span>

<span data-ttu-id="71710-124">Syötät *Lasketun kenttä*-tyypin **DS**-tietolähteen, ja se sisältää lausekkeen `SPLIT ("A,B,C", ",")`.</span><span class="sxs-lookup"><span data-stu-id="71710-124">You enter data source **DS** of the *Calculated field* type, and it contains the expression `SPLIT ("A,B,C", ",")`.</span></span> <span data-ttu-id="71710-125">Kirjoita sitten toinen lauseke `FILTER( DS, DS.Value = "B")`.</span><span class="sxs-lookup"><span data-stu-id="71710-125">You then enter another expression, `FILTER( DS, DS.Value = "B")`.</span></span> <span data-ttu-id="71710-126">Kun yrität tallentaa lausekkeen ER-kaavan suunnittelutoimintoon, seuraava poikkeus hylätään: "Vahvistusvirhe: suodatusfunktion luettelolauseke ei ole kyseltävä."</span><span class="sxs-lookup"><span data-stu-id="71710-126">When you try to save this expression in the ER formula designer, the following exception is thrown: "Validation error: The list expression of FILTER function is not queryable."</span></span>

## <a name="additional-resources"></a><span data-ttu-id="71710-127">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="71710-127">Additional resources</span></span>

[<span data-ttu-id="71710-128">Luettelotoiminnot</span><span class="sxs-lookup"><span data-stu-id="71710-128">List functions</span></span>](er-functions-category-list.md)
