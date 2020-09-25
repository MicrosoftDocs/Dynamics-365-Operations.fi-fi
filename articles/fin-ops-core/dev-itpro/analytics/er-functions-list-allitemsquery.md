---
title: ALLITEMSQUERY ER-funktio
description: Tässä ohjeaiheessa on tietoja siitä, miten sähköisen raportoinnin (ER) ALLITEMSQUERY-funktiota käytetään.
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
ms.openlocfilehash: 37546fccf804a4522638147d39206997e8c0c24c
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/01/2020
ms.locfileid: "3745366"
---
# <a name="allitemsquery-er-function"></a><span data-ttu-id="16d66-103">ALLITEMSQUERY ER-funktio</span><span class="sxs-lookup"><span data-stu-id="16d66-103">ALLITEMSQUERY ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="16d66-104">`ALLITEMSQUERY`-funktio suoritetaan liitettynä SQL-kyselynä.</span><span class="sxs-lookup"><span data-stu-id="16d66-104">The `ALLITEMSQUERY` function runs as a joined SQL query.</span></span> <span data-ttu-id="16d66-105">Se palauttaa uuden litistetyn *Tietueluettelo*-arvon, joka sisältää luettelon kaikista kohteista, jotka vastaavat määritettyä polkua.</span><span class="sxs-lookup"><span data-stu-id="16d66-105">It returns a new flattened *Record list* value that consists of a list of records that represent all items that match the specified path.</span></span>

## <a name="syntax"></a><span data-ttu-id="16d66-106">Syntaksi</span><span class="sxs-lookup"><span data-stu-id="16d66-106">Syntax</span></span>

```vb
ALLITEMSQUERY (path)
```

## <a name="arguments"></a><span data-ttu-id="16d66-107">Argumentit</span><span class="sxs-lookup"><span data-stu-id="16d66-107">Arguments</span></span>

<span data-ttu-id="16d66-108">`path`: *Tietueluettelo*</span><span class="sxs-lookup"><span data-stu-id="16d66-108">`path`: *Record list*</span></span>

<span data-ttu-id="16d66-109">*Tietueluettelo*-tietotyypin tietolähteen kelvollinen polku.</span><span class="sxs-lookup"><span data-stu-id="16d66-109">The valid path of a data source of the *Record list* data type.</span></span> <span data-ttu-id="16d66-110">Sen on sisällettävä vähintään yksi suhde.</span><span class="sxs-lookup"><span data-stu-id="16d66-110">It must contain at least one relation.</span></span>

## <a name="return-values"></a><span data-ttu-id="16d66-111">Palautusarvot</span><span class="sxs-lookup"><span data-stu-id="16d66-111">Return values</span></span>

<span data-ttu-id="16d66-112">*Tietueluettelo*</span><span class="sxs-lookup"><span data-stu-id="16d66-112">*Record list*</span></span>

<span data-ttu-id="16d66-113">Tuloksena oleva tietueluettelo.</span><span class="sxs-lookup"><span data-stu-id="16d66-113">The resulting list of records.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="16d66-114">Käyttöhuomautukset</span><span class="sxs-lookup"><span data-stu-id="16d66-114">Usage notes</span></span>

<span data-ttu-id="16d66-115">Määritetty polku on määritettävä sallituksi tietolähteen poluksi *Tietueluettelo*-tietotyypin tietolähteen elementtiin.</span><span class="sxs-lookup"><span data-stu-id="16d66-115">The specified path must be defined as a valid data source path of a data source element of the *Record list* data type.</span></span> <span data-ttu-id="16d66-116">Sen on myös sisällettävä vähintään yksi suhde.</span><span class="sxs-lookup"><span data-stu-id="16d66-116">It must also contain at least one relation.</span></span> <span data-ttu-id="16d66-117">Tietoelementit, kuten polun *merkkijono* ja *päivämäärä*, käynnistävät virheen sähköisen raportoinnin (ER) lausekkeenmuodostimessa suunnitteluaikana.</span><span class="sxs-lookup"><span data-stu-id="16d66-117">Data elements such as the path *String* and *Date* should raise an error in the Electronic reporting (ER) expression builder at design time.</span></span>

<span data-ttu-id="16d66-118">Kun tätä toimintoa käytetään *tietueluettelon* tietolähteisiin, jotka viittaavat sovellusobjektiin, jota voidaan kutsua suoraan SQL:n (esimerkiksi taulukon, entiteetin tai kyselyn) avulla, se suoritetaan liitetyssä SQL-kyselynä.</span><span class="sxs-lookup"><span data-stu-id="16d66-118">When this function is applied to data sources of the *Record list* data type that refer to an application object that can be directly called by using SQL (for example, an table, entity, or query), it runs as a joined SQL query.</span></span> <span data-ttu-id="16d66-119">Muussa tapauksessa se toimii muistissa [ALLITEMS](er-functions-list-allitems.md)-funktiolla.</span><span class="sxs-lookup"><span data-stu-id="16d66-119">Otherwise, it runs in memory as the [ALLITEMS](er-functions-list-allitems.md) function.</span></span>

## <a name="example"></a><span data-ttu-id="16d66-120">Esimerkki</span><span class="sxs-lookup"><span data-stu-id="16d66-120">Example</span></span>

<span data-ttu-id="16d66-121">Määritä seuraavat tietolähteet omassa mallimäärityksessäsi:</span><span class="sxs-lookup"><span data-stu-id="16d66-121">You define the following data sources in your model mapping:</span></span>

- <span data-ttu-id="16d66-122">**CustInv**-tietolähde, joka on *Taulukkotietueet*-tyypiä, joka viittaa CustInvoiceTable-tauluun</span><span class="sxs-lookup"><span data-stu-id="16d66-122">A **CustInv** data source of the *Table records* type that refers to the CustInvoiceTable table</span></span>
- <span data-ttu-id="16d66-123">*Lasketun kenttätyypin* **FilteredInv**-tietolähde, joka sisältää lausekkeen `FILTER (CustInv, CustInv.InvoiceAccount = "US-001")`</span><span class="sxs-lookup"><span data-stu-id="16d66-123">A **FilteredInv** data source of the *Calculated field* type that contains the expression `FILTER (CustInv, CustInv.InvoiceAccount = "US-001")`</span></span>
- <span data-ttu-id="16d66-124">*Lasketun kenttätyypin* **JourLines**, joka sisältää lausekkeen `ALLITEMSQUERY ( FilteredInv.'<Relations'.CustInvoiceJour.'<Relations'.CustInvoiceTrans)`</span><span class="sxs-lookup"><span data-stu-id="16d66-124">A **JourLines** of the *Calculated field* type that contains the expression `ALLITEMSQUERY ( FilteredInv.'<Relations'.CustInvoiceJour.'<Relations'.CustInvoiceTrans)`</span></span>

<span data-ttu-id="16d66-125">Kun suoritat mallimäärityksen kutsumaan **JourLines**-tietolähdettä, seuraava SQL-lauseke suoritetaan:</span><span class="sxs-lookup"><span data-stu-id="16d66-125">When you run the model mapping to call the **JourLines** data source, the following SQL statement is run:</span></span>

```sql
SELECT ... FROM CUSTINVOICETABLE T1 CROSS JOIN CUSTINVOICEJOUR T2 CROSS JOIN
CUSTINVOICETRANS T3 WHERE...
```

## <a name="additional-resources"></a><span data-ttu-id="16d66-126">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="16d66-126">Additional resources</span></span>

[<span data-ttu-id="16d66-127">Luettelotoiminnot</span><span class="sxs-lookup"><span data-stu-id="16d66-127">List functions</span></span>](er-functions-category-list.md)
