---
title: LISTDISTINCT ER -toiminto
description: Tässä ohjeaiheessa on tietoja siitä, miten sähköisen raportoinnin (ER) LISTDISTINCT-funktiota käytetään.
author: NickSelin
manager: kfend
ms.date: 7/30/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2020-08-01
ms.dyn365.ops.version: AX 10.0.14
ms.openlocfilehash: 2333cfc21a16a5905acadd590982020fdf878330
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/05/2020
ms.locfileid: "4682264"
---
# <a name="listdistinct-er-function"></a><span data-ttu-id="50c41-103">LISTDISTINCT ER -toiminto</span><span class="sxs-lookup"><span data-stu-id="50c41-103">LISTDISTINCT ER Function</span></span>

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

<span data-ttu-id="50c41-104">`LISTDISTINCT`-funktio laskee määritetyn lausekkeen valitun luettelon jokaisen tietueen valitsimena.</span><span class="sxs-lookup"><span data-stu-id="50c41-104">The `LISTDISTINCT` function calculates the specified expression as a selector for every record of the specified list.</span></span> <span data-ttu-id="50c41-105">Se palauttaa uuden *tietueluettelon* arvon, joka sisältää yhden tietueen kutakin yksilöllistä valitsinarvoa kohden.</span><span class="sxs-lookup"><span data-stu-id="50c41-105">It returns a new *Record list* value that contains a single record for each unique selector value.</span></span>

## <a name="syntax"></a><span data-ttu-id="50c41-106">Syntaksi</span><span class="sxs-lookup"><span data-stu-id="50c41-106">Syntax</span></span>

```
LISTDISTINCT (list, selector)
```

## <a name="arguments"></a><span data-ttu-id="50c41-107">Argumentit</span><span class="sxs-lookup"><span data-stu-id="50c41-107">Arguments</span></span>

<span data-ttu-id="50c41-108">`list`: *Tietueluettelo*</span><span class="sxs-lookup"><span data-stu-id="50c41-108">`list`: *Record list*</span></span>

<span data-ttu-id="50c41-109">*Tietueluettelo*-tietotyypin tietolähteen kelvollinen polku.</span><span class="sxs-lookup"><span data-stu-id="50c41-109">The valid path of a data source of the *Record list* data type.</span></span>

<span data-ttu-id="50c41-110">`selector`: *Primitiiviset tietotyypit*</span><span class="sxs-lookup"><span data-stu-id="50c41-110">`selector`: *Primitive data type*</span></span>

<span data-ttu-id="50c41-111">Kelvollinen lauseke, jonka avulla lasketaan valitun luettelon jokaisen tietueen valitsinarvo.</span><span class="sxs-lookup"><span data-stu-id="50c41-111">A valid expression that is used to calculate a selector value for every record in the specified list.</span></span>

<span data-ttu-id="50c41-112">Tämä parametri tukee seuraavia tietotyyppejä:</span><span class="sxs-lookup"><span data-stu-id="50c41-112">The following data types are supported for this parameter:</span></span>

- <span data-ttu-id="50c41-113">Boolen arvo</span><span class="sxs-lookup"><span data-stu-id="50c41-113">Boolean</span></span>
- <span data-ttu-id="50c41-114">Päivämäärä</span><span class="sxs-lookup"><span data-stu-id="50c41-114">Date</span></span>
- <span data-ttu-id="50c41-115">Päivämäärä ja aika</span><span class="sxs-lookup"><span data-stu-id="50c41-115">DateTime</span></span>
- <span data-ttu-id="50c41-116">Guid</span><span class="sxs-lookup"><span data-stu-id="50c41-116">GUID</span></span>
- <span data-ttu-id="50c41-117">Kokonaisluku</span><span class="sxs-lookup"><span data-stu-id="50c41-117">Integer</span></span>
- <span data-ttu-id="50c41-118">Int64</span><span class="sxs-lookup"><span data-stu-id="50c41-118">Int64</span></span>
- <span data-ttu-id="50c41-119">Reaaliluku</span><span class="sxs-lookup"><span data-stu-id="50c41-119">Real</span></span>
- <span data-ttu-id="50c41-120">Merkkijono</span><span class="sxs-lookup"><span data-stu-id="50c41-120">String</span></span>

## <a name="return-values"></a><span data-ttu-id="50c41-121">Palautusarvot</span><span class="sxs-lookup"><span data-stu-id="50c41-121">Return values</span></span>

<span data-ttu-id="50c41-122">*Tietueluettelo*</span><span class="sxs-lookup"><span data-stu-id="50c41-122">*Record list*</span></span>

<span data-ttu-id="50c41-123">Tuloksena oleva tietueluettelo.</span><span class="sxs-lookup"><span data-stu-id="50c41-123">The resulting list of records.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="50c41-124">Käyttöhuomautukset</span><span class="sxs-lookup"><span data-stu-id="50c41-124">Usage notes</span></span>

<span data-ttu-id="50c41-125">Luotavan luettelon rakenne vastaa määritetyn luettelon rakennetta.</span><span class="sxs-lookup"><span data-stu-id="50c41-125">The structure of the list that is created matches the structure of the specified list.</span></span>

<span data-ttu-id="50c41-126">Sama valitsimen arvo voidaan laskea useille tietueille määritetyssä luettelossa.</span><span class="sxs-lookup"><span data-stu-id="50c41-126">The same selector value might be calculated for multiple records in the specified list.</span></span> <span data-ttu-id="50c41-127">Tässä tapauksessa luodun luettelon vastaavan tietueen kenttäarvot vastaavat määritetyn luettelon ensimmäisen tietueen arvoja, joille valitsinarvo lasketaan.</span><span class="sxs-lookup"><span data-stu-id="50c41-127">In this case, field values of the corresponding record in the created list equal the values of the first record from the specified list that the selector value is calculated for.</span></span>

<span data-ttu-id="50c41-128">Tämän toiminnon suorittaminen tapahtuu muistissa olevan *tietueluettelo*-tyypin [sähköisen raportoinnin (ER)](general-electronic-reporting.md) tietolähteen avulla.</span><span class="sxs-lookup"><span data-stu-id="50c41-128">The execution of this function is done on any [Electronic reporting (ER)](general-electronic-reporting.md) data source of the *Record list* type that is present in memory.</span></span>

<span data-ttu-id="50c41-129">**GROUPBY**-tietolähdettä voidaan käyttää myös sellaisten luettelotietojen luomiseen, joille on määritetty erilliset arvot sisältävä valitsin.</span><span class="sxs-lookup"><span data-stu-id="50c41-129">The **GROUPBY** data source can also be used to generate the list of records that the selector that has distinct values is calculated for.</span></span> <span data-ttu-id="50c41-130">Suorituskyvyn ja muistin kulutuksen näkökulmasta on kuitenkin parempi käyttää `LISTDISTINCT`-funktiota kuin **GROUPBY**-tietolähdettä, koska toiminnon suorittaminen tapahtuu muistissa.</span><span class="sxs-lookup"><span data-stu-id="50c41-130">However, from a performance and memory consumption perspective, it's better to use the `LISTDISTINCT` function than the **GROUPBY** data source, because the execution of the function is done in memory.</span></span>

## <a name="example"></a><span data-ttu-id="50c41-131">Esimerkki</span><span class="sxs-lookup"><span data-stu-id="50c41-131">Example</span></span>

<span data-ttu-id="50c41-132">Seuraavassa esimerkissä näkyy, miten voit saada luettelon yksilöivistä asiakastilinumeroista, joille on myönnetty vähintään yksi myyntilasku tai projektilasku tiettynä kautena.</span><span class="sxs-lookup"><span data-stu-id="50c41-132">The following example shows how you can get the list of unique customer account numbers that at least one sales invoice or project invoice has been issued to during a specific period.</span></span>

1. <span data-ttu-id="50c41-133">Kirjoita sen tyypin **SalesInvoice**-tietolähde `Record list`-tyyppistä, joka viittaa **CustInvoiceJour**-sovellustauluun ja suodattaa tiettyjen kausien myyntilaskut.</span><span class="sxs-lookup"><span data-stu-id="50c41-133">Enter the **SalesInvoice** data source of the `Record list` type that refers to the **CustInvoiceJour** application table and filters sales invoices for specific periods.</span></span>

    <span data-ttu-id="50c41-134">Tämän tietolähteen `InvoiceAccount`-kenttä palauttaa laskutetun asiakkaan tilinumeron.</span><span class="sxs-lookup"><span data-stu-id="50c41-134">The `InvoiceAccount` field of this data source returns the account number of an invoiced customer.</span></span>

2. <span data-ttu-id="50c41-135">Kirjoita sen tyypin **ProjectInvoice**-tietolähde `Record list`-tyyppistä, joka viittaa **ProjInvoiceJour**-sovellustauluun ja suodattaa tiettyjen kausien projektilaskut.</span><span class="sxs-lookup"><span data-stu-id="50c41-135">Enter the **ProjectInvoice** data source of the `Record list` type that refers to the **ProjInvoiceJour** application table and filters project invoices for specific periods.</span></span>

    <span data-ttu-id="50c41-136">Tämän tietolähteen `InvoiceAccount`-kenttä palauttaa laskutetun asiakkaan tilinumeron.</span><span class="sxs-lookup"><span data-stu-id="50c41-136">The `InvoiceAccount` field of this data source returns the account number of an invoiced customer.</span></span>

3. <span data-ttu-id="50c41-137">Määritä `Calculated field`-tyypin **AllInvoices**-tietolähde, joka sisältää lausekkeen `LISTJOIN(SalesInvoice, ProjectInvoice)`.</span><span class="sxs-lookup"><span data-stu-id="50c41-137">Configure the **AllInvoices** data source of the `Calculated field` type that contains the expression `LISTJOIN(SalesInvoice, ProjectInvoice)`.</span></span>

    <span data-ttu-id="50c41-138">Tämä tietolähde palauttaa liitettyjen myyntilaskujen ja projektilaskujen luettelon.</span><span class="sxs-lookup"><span data-stu-id="50c41-138">This data source returns the joined list of sales invoices and project invoices.</span></span>

4. <span data-ttu-id="50c41-139">Määritä `Record list`-tyypin **InvoicedCustomer**-tietolähde, joka sisältää lausekkeen `LISTDISTINCT(AllInvoices, AllInvoices.InvoiceAccount)`.</span><span class="sxs-lookup"><span data-stu-id="50c41-139">Configure the **InvoicedCustomer** data source of the `Record list` type that contains the expression `LISTDISTINCT(AllInvoices, AllInvoices.InvoiceAccount)`.</span></span>

    <span data-ttu-id="50c41-140">Tämä tietolähde palauttaa uuden luettelon, joka sisältää yhden tietueen jokaiselle määritetyn kauden aikana laskutetulle asiakkaalle.</span><span class="sxs-lookup"><span data-stu-id="50c41-140">This data source returns a new list that contains a single record for every unique customer that has been invoiced during the defined period.</span></span> <span data-ttu-id="50c41-141">Tämän luettelon `InvoiceAccount`-kenttä sisältää asiakkaan tilinumeron.</span><span class="sxs-lookup"><span data-stu-id="50c41-141">The `InvoiceAccount` field of this list contains a customer account number.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="50c41-142">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="50c41-142">Additional resources</span></span>

[<span data-ttu-id="50c41-143">Luettelotoiminnot</span><span class="sxs-lookup"><span data-stu-id="50c41-143">List functions</span></span>](er-functions-category-list.md)
