---
title: FORMATELEMENTNAME ER -funktio
description: Tässä ohjeaiheessa on tietoja siitä, miten sähköisen raportoinnin (ER) FORMATELEMENTNAME-funktiota käytetään.
author: NickSelin
manager: kfend
ms.date: 12/05/2019
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
ms.openlocfilehash: e8be55d9a90e841d64288b0c618c0012912ddbab
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/01/2020
ms.locfileid: "3745630"
---
# <a name="formatelementname-er-function"></a><span data-ttu-id="ecd1f-103">FORMATELEMENTNAME ER -funktio</span><span class="sxs-lookup"><span data-stu-id="ecd1f-103">FORMATELEMENTNAME ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ecd1f-104">`FORMATELEMENTNAME`-funktio palauttaa *Merkkijonoarvon*, joka edustaa nykyisen sähköisen raportoinnin (ER) muodon elementin nimeä.</span><span class="sxs-lookup"><span data-stu-id="ecd1f-104">The `FORMATELEMENTNAME` function returns a *String* value that represents the name of the current Electronic reporting (ER) format's element.</span></span>

## <a name="syntax"></a><span data-ttu-id="ecd1f-105">Syntaksi</span><span class="sxs-lookup"><span data-stu-id="ecd1f-105">Syntax</span></span>

```vb
FORMATELEMENTNAME ()
```

## <a name="return-values"></a><span data-ttu-id="ecd1f-106">Palautusarvot</span><span class="sxs-lookup"><span data-stu-id="ecd1f-106">Return values</span></span>

<span data-ttu-id="ecd1f-107">*merkkijono*</span><span class="sxs-lookup"><span data-stu-id="ecd1f-107">*String*</span></span>

<span data-ttu-id="ecd1f-108">Tulokseksi saatava tekstiarvo.</span><span class="sxs-lookup"><span data-stu-id="ecd1f-108">The resulting text value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="ecd1f-109">Käyttöhuomautukset</span><span class="sxs-lookup"><span data-stu-id="ecd1f-109">Usage notes</span></span>

<span data-ttu-id="ecd1f-110">Tätä funktiota voidaan kutsua ER-lausekkeissa, jotka määritettiin **Kerättyjen tietojen avaimen nimi** ja **Kerättyjen tietojen avainten arvo** -ominaisuuksiksi ER-muotokomponentin **Teksti**-ryhmästä, joka sijaitsee **Yleinen\\Tiedosto**-komponentissa, jossa **Kerää tuotostiedot** -asetus on käytössä.</span><span class="sxs-lookup"><span data-stu-id="ecd1f-110">This function can be called in ER expressions that were configured for the **Collected data key name** and **Collected data key value** properties of an ER format component from the **Text** group that resides under the **Common\\File** component where the **Collect output details** option is turned on.</span></span>

## <a name="example"></a><span data-ttu-id="ecd1f-111">Esimerkki</span><span class="sxs-lookup"><span data-stu-id="ecd1f-111">Example</span></span>

<span data-ttu-id="ecd1f-112">Lisätietoja tämän toiminnon käytöstä on tehtäväoppaassa [ER Käytä tulostusmuotoa laskennassa ja summauksessa](tasks/er-format-counting-summing-1.md), joka on osa **IT-palvelujen ja -ratkaisujen komponenttien hankkiminen ja kehittäminen** -liiketoimintaprosessia.</span><span class="sxs-lookup"><span data-stu-id="ecd1f-112">For more information about how to use this function, see the [ER Use data of format output for counting and summing](tasks/er-format-counting-summing-1.md) task guide, which is part of the **Acquire/Develop IT service/solution components** business process.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="ecd1f-113">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="ecd1f-113">Additional resources</span></span>

[<span data-ttu-id="ecd1f-114">Tietojen keruutoiminnot</span><span class="sxs-lookup"><span data-stu-id="ecd1f-114">Data collection functions</span></span>](er-functions-category-data-collection.md)
