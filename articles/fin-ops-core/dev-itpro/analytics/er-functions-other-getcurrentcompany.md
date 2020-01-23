---
title: GETCURRENTCOMPANY ER-funktio
description: Tässä ohjeaiheessa on tietoja siitä, miten sähköisen raportoinnin (ER) GETCURRENTCOMPANY-funktiota käytetään.
author: NickSelin
manager: kfend
ms.date: 12/17/2019
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
ms.openlocfilehash: a0b4c93a4705cd0e382b9b6c7af1d199beeceabe
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/20/2019
ms.locfileid: "2915990"
---
# <span data-ttu-id="66f14-103"><a name="GETCURRENTCOMPANY">GETCURRENTCOMPANY ER-funktio</a></span><span class="sxs-lookup"><span data-stu-id="66f14-103"><a name="GETCURRENTCOMPANY">GETCURRENTCOMPANY ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="66f14-104">`GETCURRENTCOMPANY`-funktio palauttaa *Merkkijono*-arvon siltä yritykseltä, johon käyttäjä on tällä hetkellä kirjautunut.</span><span class="sxs-lookup"><span data-stu-id="66f14-104">The `GETCURRENTCOMPANY` function returns a *String* value that represents the code for the legal entity (company) that a user is currently signed in to.</span></span>

## <a name="syntax"></a><span data-ttu-id="66f14-105">Syntaksi</span><span class="sxs-lookup"><span data-stu-id="66f14-105">Syntax</span></span>

```
GETCURRENTCOMPANY ()
```

## <a name="return-values"></a><span data-ttu-id="66f14-106">Palautusarvot</span><span class="sxs-lookup"><span data-stu-id="66f14-106">Return values</span></span>

<span data-ttu-id="66f14-107">*merkkijono*</span><span class="sxs-lookup"><span data-stu-id="66f14-107">*String*</span></span>

<span data-ttu-id="66f14-108">Tulokseksi saatava tekstiarvo.</span><span class="sxs-lookup"><span data-stu-id="66f14-108">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="66f14-109">Esimerkki</span><span class="sxs-lookup"><span data-stu-id="66f14-109">Example</span></span>

<span data-ttu-id="66f14-110">`GETCURRENTCOMPANY ()` palauttaa arvon **USMF** käyttäjälle, joka on kirjautunut yritykseen **Contoso Entertainment System USA**.</span><span class="sxs-lookup"><span data-stu-id="66f14-110">`GETCURRENTCOMPANY ()` returns **USMF** for a user who is signed in to the **Contoso Entertainment System USA** company.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="66f14-111">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="66f14-111">Additional resources</span></span>

[<span data-ttu-id="66f14-112">Muut (liiketoiminnan toimialuekohtaiset) toiminnot</span><span class="sxs-lookup"><span data-stu-id="66f14-112">Other (business domain–specific) functions</span></span>](er-functions-category-other.md)
