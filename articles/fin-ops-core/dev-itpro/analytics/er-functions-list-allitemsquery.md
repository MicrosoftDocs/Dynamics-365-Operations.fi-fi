---
title: ALLITEMSQUERY ER-funktio
description: Tässä ohjeaiheessa on tietoja siitä, miten sähköisen raportoinnin (ER) ALLITEMSQUERY-funktiota käytetään.
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
ms.openlocfilehash: 7995b497a2bd95d4aec9ae6d5f1c3cb790823ea0
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2021
ms.locfileid: "5746696"
---
# <a name="allitemsquery-er-function"></a><span data-ttu-id="8ebf4-103">ALLITEMSQUERY ER-funktio</span><span class="sxs-lookup"><span data-stu-id="8ebf4-103">ALLITEMSQUERY ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8ebf4-104">`ALLITEMSQUERY`-funktio suoritetaan liitettynä SQL-kyselynä.</span><span class="sxs-lookup"><span data-stu-id="8ebf4-104">The `ALLITEMSQUERY` function runs as a joined SQL query.</span></span> <span data-ttu-id="8ebf4-105">Se palauttaa uuden litistetyn *Tietueluettelo*-arvon, joka sisältää luettelon kaikista kohteista, jotka vastaavat määritettyä polkua.</span><span class="sxs-lookup"><span data-stu-id="8ebf4-105">It returns a new flattened *Record list* value that consists of a list of records that represent all items that match the specified path.</span></span>

## <a name="syntax"></a><span data-ttu-id="8ebf4-106">Syntaksi</span><span class="sxs-lookup"><span data-stu-id="8ebf4-106">Syntax</span></span>

```vb
ALLITEMSQUERY (path)
```

## <a name="arguments"></a><span data-ttu-id="8ebf4-107">Argumentit</span><span class="sxs-lookup"><span data-stu-id="8ebf4-107">Arguments</span></span>

<span data-ttu-id="8ebf4-108">`path`: *Tietueluettelo*</span><span class="sxs-lookup"><span data-stu-id="8ebf4-108">`path`: *Record list*</span></span>

<span data-ttu-id="8ebf4-109">*Tietueluettelo*-tietotyypin tietolähteen kelvollinen polku.</span><span class="sxs-lookup"><span data-stu-id="8ebf4-109">The valid path of a data source of the *Record list* data type.</span></span> <span data-ttu-id="8ebf4-110">Sen on sisällettävä vähintään yksi suhde.</span><span class="sxs-lookup"><span data-stu-id="8ebf4-110">It must contain at least one relation.</span></span>

## <a name="return-values"></a><span data-ttu-id="8ebf4-111">Palautusarvot</span><span class="sxs-lookup"><span data-stu-id="8ebf4-111">Return values</span></span>

<span data-ttu-id="8ebf4-112">*Tietueluettelo*</span><span class="sxs-lookup"><span data-stu-id="8ebf4-112">*Record list*</span></span>

<span data-ttu-id="8ebf4-113">Tuloksena oleva tietueluettelo.</span><span class="sxs-lookup"><span data-stu-id="8ebf4-113">The resulting list of records.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="8ebf4-114">Käyttöhuomautukset</span><span class="sxs-lookup"><span data-stu-id="8ebf4-114">Usage notes</span></span>

<span data-ttu-id="8ebf4-115">Määritetty polku on määritettävä sallituksi tietolähteen poluksi *Tietueluettelo*-tietotyypin tietolähteen elementtiin.</span><span class="sxs-lookup"><span data-stu-id="8ebf4-115">The specified path must be defined as a valid data source path of a data source element of the *Record list* data type.</span></span> <span data-ttu-id="8ebf4-116">Sen on myös sisällettävä vähintään yksi suhde.</span><span class="sxs-lookup"><span data-stu-id="8ebf4-116">It must also contain at least one relation.</span></span> <span data-ttu-id="8ebf4-117">Tietoelementit, kuten polun *merkkijono* ja *päivämäärä*, käynnistävät virheen sähköisen raportoinnin (ER) lausekkeenmuodostimessa suunnitteluaikana.</span><span class="sxs-lookup"><span data-stu-id="8ebf4-117">Data elements such as the path *String* and *Date* should raise an error in the Electronic reporting (ER) expression builder at design time.</span></span>

<span data-ttu-id="8ebf4-118">Kun tätä toimintoa käytetään *tietueluettelon* tietolähteisiin, jotka viittaavat sovellusobjektiin, jota voidaan kutsua suoraan SQL:n (esimerkiksi taulukon, entiteetin tai kyselyn) avulla, se suoritetaan liitetyssä SQL-kyselynä.</span><span class="sxs-lookup"><span data-stu-id="8ebf4-118">When this function is applied to data sources of the *Record list* data type that refer to an application object that can be directly called by using SQL (for example, an table, entity, or query), it runs as a joined SQL query.</span></span> <span data-ttu-id="8ebf4-119">Muussa tapauksessa se toimii muistissa [ALLITEMS](er-functions-list-allitems.md)-funktiolla.</span><span class="sxs-lookup"><span data-stu-id="8ebf4-119">Otherwise, it runs in memory as the [ALLITEMS](er-functions-list-allitems.md) function.</span></span>

## <a name="example"></a><span data-ttu-id="8ebf4-120">Esimerkki</span><span class="sxs-lookup"><span data-stu-id="8ebf4-120">Example</span></span>

<span data-ttu-id="8ebf4-121">Määritä seuraavat tietolähteet omassa mallimäärityksessäsi:</span><span class="sxs-lookup"><span data-stu-id="8ebf4-121">You define the following data sources in your model mapping:</span></span>

- <span data-ttu-id="8ebf4-122">**CustInv**-tietolähde, joka on *Taulukkotietueet*-tyypiä, joka viittaa CustInvoiceTable-tauluun</span><span class="sxs-lookup"><span data-stu-id="8ebf4-122">A **CustInv** data source of the *Table records* type that refers to the CustInvoiceTable table</span></span>
- <span data-ttu-id="8ebf4-123">*Lasketun kenttätyypin* **FilteredInv**-tietolähde, joka sisältää lausekkeen `FILTER (CustInv, CustInv.InvoiceAccount = "US-001")`</span><span class="sxs-lookup"><span data-stu-id="8ebf4-123">A **FilteredInv** data source of the *Calculated field* type that contains the expression `FILTER (CustInv, CustInv.InvoiceAccount = "US-001")`</span></span>
- <span data-ttu-id="8ebf4-124">*Lasketun kenttätyypin* **JourLines**, joka sisältää lausekkeen `ALLITEMSQUERY ( FilteredInv.'<Relations'.CustInvoiceJour.'<Relations'.CustInvoiceTrans)`</span><span class="sxs-lookup"><span data-stu-id="8ebf4-124">A **JourLines** of the *Calculated field* type that contains the expression `ALLITEMSQUERY ( FilteredInv.'<Relations'.CustInvoiceJour.'<Relations'.CustInvoiceTrans)`</span></span>

<span data-ttu-id="8ebf4-125">Kun suoritat mallimäärityksen kutsumaan **JourLines**-tietolähdettä, seuraava SQL-lauseke suoritetaan:</span><span class="sxs-lookup"><span data-stu-id="8ebf4-125">When you run the model mapping to call the **JourLines** data source, the following SQL statement is run:</span></span>

```sql
SELECT ... FROM CUSTINVOICETABLE T1 CROSS JOIN CUSTINVOICEJOUR T2 CROSS JOIN
CUSTINVOICETRANS T3 WHERE...
```

## <a name="additional-resources"></a><span data-ttu-id="8ebf4-126">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="8ebf4-126">Additional resources</span></span>

[<span data-ttu-id="8ebf4-127">Luettelotoiminnot</span><span class="sxs-lookup"><span data-stu-id="8ebf4-127">List functions</span></span>](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]