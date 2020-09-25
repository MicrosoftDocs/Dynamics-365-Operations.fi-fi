---
title: NULLDATE ER-funktio
description: Tässä ohjeaiheessa on tietoja siitä, miten sähköisen raportoinnin (ER) NULLDATE-funktiota käytetään.
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
ms.openlocfilehash: edf43cc19636f51387504a7d9da73d757d96e558
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/01/2020
ms.locfileid: "3744284"
---
# <a name="nulldate-er-function"></a><span data-ttu-id="a8125-103">NULLDATE ER-funktio</span><span class="sxs-lookup"><span data-stu-id="a8125-103">NULLDATE ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a8125-104">`NULLDATE`-funktio palauttaa *päivämäärän* arvon, joka vastaa **Null**-arvoa (1. tammikuuta 1900).</span><span class="sxs-lookup"><span data-stu-id="a8125-104">The `NULLDATE` function returns a *Date* value that represents the **null** date (January 1, 1900).</span></span>

## <a name="syntax"></a><span data-ttu-id="a8125-105">Syntaksi</span><span class="sxs-lookup"><span data-stu-id="a8125-105">Syntax</span></span>

```vb
NULLDATE () as 
```

## <a name="return-values"></a><span data-ttu-id="a8125-106">Palautusarvot</span><span class="sxs-lookup"><span data-stu-id="a8125-106">Return values</span></span>

<span data-ttu-id="a8125-107">*Päivämäärä*</span><span class="sxs-lookup"><span data-stu-id="a8125-107">*Date*</span></span>

<span data-ttu-id="a8125-108">Tulokseksi saatava päivämääräarvo.</span><span class="sxs-lookup"><span data-stu-id="a8125-108">The resulting date value.</span></span>

## <a name="example-1"></a><span data-ttu-id="a8125-109">Esimerkki 1</span><span class="sxs-lookup"><span data-stu-id="a8125-109">Example 1</span></span>

<span data-ttu-id="a8125-110">`DATEFORMAT (NULLDATE(), "yyyy-MM-dd")` palauttaa **null**-arvon, 1. tammikuuta 1900, muodossa **"1900-01-01"** määritetyn mukautetun muodon perusteella.</span><span class="sxs-lookup"><span data-stu-id="a8125-110">`DATEFORMAT (NULLDATE(), "yyyy-MM-dd")` returns the **null** date, January 1, 1900, as **"1900-01-01"**, based on the specified custom format.</span></span>

## <a name="example-2"></a><span data-ttu-id="a8125-111">Esimerkki 2</span><span class="sxs-lookup"><span data-stu-id="a8125-111">Example 2</span></span>

<span data-ttu-id="a8125-112">Lauseke `IF( Invoice.DocumentDate = NULLDATE(), true, false)` palauttaa arvon **Tosi**, kun **DocumentDate**-kentän arvo on **Null**-päivämäärä.</span><span class="sxs-lookup"><span data-stu-id="a8125-112">The expression `IF( Invoice.DocumentDate = NULLDATE(), true, false)` returns **True** when the value of the **DocumentDate** field equals the **null** date.</span></span> <span data-ttu-id="a8125-113">Tässä esimerkissä **Lasku** on **Finance/taulutietueet**-tyypin sähköisen raportoinnin ER-tietolähde, joka viittaa CustInvoiceJour-tauluun.</span><span class="sxs-lookup"><span data-stu-id="a8125-113">In this example, **Invoice** is an Electronic reporting (ER) data source of the **Finance/Table records** type, and it refers to the CustInvoiceJour table.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="a8125-114">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="a8125-114">Additional resources</span></span>

[<span data-ttu-id="a8125-115">Päivämäärä- ja aikatoiminnot</span><span class="sxs-lookup"><span data-stu-id="a8125-115">Date and time functions</span></span>](er-functions-category-datetime.md)
