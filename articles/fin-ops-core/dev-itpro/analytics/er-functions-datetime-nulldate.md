---
title: NULLDATE ER-funktio
description: Tässä ohjeaiheessa on tietoja siitä, miten sähköisen raportoinnin (ER) NULLDATE-funktiota käytetään.
author: NickSelin
ms.date: 12/04/2019
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
ms.openlocfilehash: 6ac8da3f18c7793512685d52dd64a9bd55bfb8fc
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2021
ms.locfileid: "5746840"
---
# <a name="nulldate-er-function"></a><span data-ttu-id="a5760-103">NULLDATE ER-funktio</span><span class="sxs-lookup"><span data-stu-id="a5760-103">NULLDATE ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a5760-104">`NULLDATE`-funktio palauttaa *päivämäärän* arvon, joka vastaa **Null**-arvoa (1. tammikuuta 1900).</span><span class="sxs-lookup"><span data-stu-id="a5760-104">The `NULLDATE` function returns a *Date* value that represents the **null** date (January 1, 1900).</span></span>

## <a name="syntax"></a><span data-ttu-id="a5760-105">Syntaksi</span><span class="sxs-lookup"><span data-stu-id="a5760-105">Syntax</span></span>

```vb
NULLDATE () as 
```

## <a name="return-values"></a><span data-ttu-id="a5760-106">Palautusarvot</span><span class="sxs-lookup"><span data-stu-id="a5760-106">Return values</span></span>

<span data-ttu-id="a5760-107">*Päivämäärä*</span><span class="sxs-lookup"><span data-stu-id="a5760-107">*Date*</span></span>

<span data-ttu-id="a5760-108">Tulokseksi saatava päivämääräarvo.</span><span class="sxs-lookup"><span data-stu-id="a5760-108">The resulting date value.</span></span>

## <a name="example-1"></a><span data-ttu-id="a5760-109">Esimerkki 1</span><span class="sxs-lookup"><span data-stu-id="a5760-109">Example 1</span></span>

<span data-ttu-id="a5760-110">`DATEFORMAT (NULLDATE(), "yyyy-MM-dd")` palauttaa **null**-arvon, 1. tammikuuta 1900, muodossa **"1900-01-01"** määritetyn mukautetun muodon perusteella.</span><span class="sxs-lookup"><span data-stu-id="a5760-110">`DATEFORMAT (NULLDATE(), "yyyy-MM-dd")` returns the **null** date, January 1, 1900, as **"1900-01-01"**, based on the specified custom format.</span></span>

## <a name="example-2"></a><span data-ttu-id="a5760-111">Esimerkki 2</span><span class="sxs-lookup"><span data-stu-id="a5760-111">Example 2</span></span>

<span data-ttu-id="a5760-112">Lauseke `IF( Invoice.DocumentDate = NULLDATE(), true, false)` palauttaa arvon **Tosi**, kun **DocumentDate**-kentän arvo on **Null**-päivämäärä.</span><span class="sxs-lookup"><span data-stu-id="a5760-112">The expression `IF( Invoice.DocumentDate = NULLDATE(), true, false)` returns **True** when the value of the **DocumentDate** field equals the **null** date.</span></span> <span data-ttu-id="a5760-113">Tässä esimerkissä **Lasku** on **Finance/taulutietueet**-tyypin sähköisen raportoinnin ER-tietolähde, joka viittaa CustInvoiceJour-tauluun.</span><span class="sxs-lookup"><span data-stu-id="a5760-113">In this example, **Invoice** is an Electronic reporting (ER) data source of the **Finance/Table records** type, and it refers to the CustInvoiceJour table.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="a5760-114">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="a5760-114">Additional resources</span></span>

[<span data-ttu-id="a5760-115">Päivämäärä- ja aikatoiminnot</span><span class="sxs-lookup"><span data-stu-id="a5760-115">Date and time functions</span></span>](er-functions-category-datetime.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]