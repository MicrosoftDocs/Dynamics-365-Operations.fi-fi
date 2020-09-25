---
title: ALLITEMS ER-funktio
description: Tässä ohjeaiheessa on tietoja siitä, miten sähköisen raportoinnin (ER) ALLITEMS-funktiota käytetään.
author: NickSelin
manager: kfend
ms.date: 12/04/2019
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
ms.openlocfilehash: 47113d52e15d3d61f00b3c54229e286eb0f1a8d7
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/01/2020
ms.locfileid: "3745390"
---
# <a name="allitems-er-function"></a><span data-ttu-id="a6087-103">ALLITEMS ER-funktio</span><span class="sxs-lookup"><span data-stu-id="a6087-103">ALLITEMS ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a6087-104">`ALLITEMS`-funktio suoritetaan muistissa olevan valinnan mukaan ja se palauttaa uuden litistetty *Tietueluettelo*-arvon tietueluettelona, joka edustaa kaikkia määritettyä polkua vastaavia kohteita.</span><span class="sxs-lookup"><span data-stu-id="a6087-104">The `ALLITEMS` function runs as an in-memory selection and returns a new flattened *Record list* value as a list of records that represents all items that match the specified path.</span></span>

## <a name="syntax"></a><span data-ttu-id="a6087-105">Syntaksi</span><span class="sxs-lookup"><span data-stu-id="a6087-105">Syntax</span></span>

```vb
ALLITEMS (path)
```

## <a name="arguments"></a><span data-ttu-id="a6087-106">Argumentit</span><span class="sxs-lookup"><span data-stu-id="a6087-106">Arguments</span></span>

<span data-ttu-id="a6087-107">`path`: *Tietueluettelo*</span><span class="sxs-lookup"><span data-stu-id="a6087-107">`path`: *Record list*</span></span>

<span data-ttu-id="a6087-108">*Tietueluettelo*-tietotyypin tietolähteen kelvollinen polku.</span><span class="sxs-lookup"><span data-stu-id="a6087-108">The valid path of a data source of the *Record list* data type.</span></span>

## <a name="return-values"></a><span data-ttu-id="a6087-109">Palautusarvot</span><span class="sxs-lookup"><span data-stu-id="a6087-109">Return values</span></span>

<span data-ttu-id="a6087-110">*Tietueluettelo*</span><span class="sxs-lookup"><span data-stu-id="a6087-110">*Record list*</span></span>

<span data-ttu-id="a6087-111">Tuloksena oleva tietueluettelo.</span><span class="sxs-lookup"><span data-stu-id="a6087-111">The resulting list of records.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="a6087-112">Käyttöhuomautukset</span><span class="sxs-lookup"><span data-stu-id="a6087-112">Usage notes</span></span>

<span data-ttu-id="a6087-113">Polku on määritettävä sallituksi tietolähteen poluksi *Tietueluettelo*-tietotyypin tietolähteen elementtiin.</span><span class="sxs-lookup"><span data-stu-id="a6087-113">The path must be defined as a valid data source path of a data source element of the *Record list* data type.</span></span> <span data-ttu-id="a6087-114">Tietoelementit, kuten polun merkkijono ja päivämäärä, käynnistävät virheen sähköisen raportoinnin (ER) lausekkeenmuodostimessa suunnitteluaikana.</span><span class="sxs-lookup"><span data-stu-id="a6087-114">Data elements such as the path string and date should raise an error in the Electronic reporting (ER) expression builder at design time.</span></span>

<span data-ttu-id="a6087-115">Tätä funktiota ei suositella käytettäväksi tapahtumatietolähteissä, jotka saattavat sisältää suuren määrän tietoja.</span><span class="sxs-lookup"><span data-stu-id="a6087-115">We don't recommend that you use this function for transactional data sources that might contain a large volume of data.</span></span> <span data-ttu-id="a6087-116">Harkitse sen sijaan [ALLTEMSQUERY](er-functions-list-allitemsquery.md) -funktion käyttämistä.</span><span class="sxs-lookup"><span data-stu-id="a6087-116">Instead, consider using the [ALLTEMSQUERY](er-functions-list-allitemsquery.md) function.</span></span>

## <a name="example-1"></a><span data-ttu-id="a6087-117">Esimerkki 1</span><span class="sxs-lookup"><span data-stu-id="a6087-117">Example 1</span></span>

<span data-ttu-id="a6087-118">Jos syötät `SPLIT("abcdef" , 2)` tietolähteeksi **DS**, lauseke `COUNT( ALLITEMS (DS))` palauttaa arvon **3**.</span><span class="sxs-lookup"><span data-stu-id="a6087-118">If you enter `SPLIT("abcdef" , 2)` as data source **DS**, the expression `COUNT( ALLITEMS (DS))` returns **3**.</span></span>

## <a name="example-2"></a><span data-ttu-id="a6087-119">Esimerkki 2</span><span class="sxs-lookup"><span data-stu-id="a6087-119">Example 2</span></span>

<span data-ttu-id="a6087-120">Jos syötät **Vend** *Tietueluettelon* tietotyypin tietolähteeksi, joka viittaa VendTable-sovellus tauluun, lauseke `ALLITEMS (Vend.'<Relations'.ContactPerson)` palauttaa litistetyn tietueluettelon, jossa on **ContactPerson**-taulukon rakenne ja joka sisältää kaikki yhteyshenkilöt, joita voi käyttää **ContactPerson.ContactForParty == VendTable.Party**-relaatio, ja joka on käytettävissä kaikille toimittajille viitatun toimittajan taulukosta.</span><span class="sxs-lookup"><span data-stu-id="a6087-120">If you enter **Vend** as the data source of the *Record list* data type that refers to the VendTable application table, the expression `ALLITEMS (Vend.'<Relations'.ContactPerson)` returns a flattened list of records that has the **ContactPerson** table structure and contains all contact persons that can be accessed by using the **ContactPerson.ContactForParty == VendTable.Party** relation, and that is available for all vendors from the referenced vendor table.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="a6087-121">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="a6087-121">Additional resources</span></span>

[<span data-ttu-id="a6087-122">Luettelotoiminnot</span><span class="sxs-lookup"><span data-stu-id="a6087-122">List functions</span></span>](er-functions-category-list.md)
