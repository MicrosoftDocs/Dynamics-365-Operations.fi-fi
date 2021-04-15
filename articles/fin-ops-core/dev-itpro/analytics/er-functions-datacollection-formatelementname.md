---
title: FORMATELEMENTNAME ER -funktio
description: Tässä ohjeaiheessa on tietoja siitä, miten sähköisen raportoinnin (ER) FORMATELEMENTNAME-funktiota käytetään.
author: NickSelin
ms.date: 12/05/2019
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
ms.openlocfilehash: f716fe779903b4e9142b7959d868256f2d84c624
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2021
ms.locfileid: "5755225"
---
# <a name="formatelementname-er-function"></a><span data-ttu-id="cd4e1-103">FORMATELEMENTNAME ER -funktio</span><span class="sxs-lookup"><span data-stu-id="cd4e1-103">FORMATELEMENTNAME ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="cd4e1-104">`FORMATELEMENTNAME`-funktio palauttaa *Merkkijonoarvon*, joka edustaa nykyisen sähköisen raportoinnin (ER) muodon elementin nimeä.</span><span class="sxs-lookup"><span data-stu-id="cd4e1-104">The `FORMATELEMENTNAME` function returns a *String* value that represents the name of the current Electronic reporting (ER) format's element.</span></span>

## <a name="syntax"></a><span data-ttu-id="cd4e1-105">Syntaksi</span><span class="sxs-lookup"><span data-stu-id="cd4e1-105">Syntax</span></span>

```vb
FORMATELEMENTNAME ()
```

## <a name="return-values"></a><span data-ttu-id="cd4e1-106">Palautusarvot</span><span class="sxs-lookup"><span data-stu-id="cd4e1-106">Return values</span></span>

<span data-ttu-id="cd4e1-107">*merkkijono*</span><span class="sxs-lookup"><span data-stu-id="cd4e1-107">*String*</span></span>

<span data-ttu-id="cd4e1-108">Tulokseksi saatava tekstiarvo.</span><span class="sxs-lookup"><span data-stu-id="cd4e1-108">The resulting text value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="cd4e1-109">Käyttöhuomautukset</span><span class="sxs-lookup"><span data-stu-id="cd4e1-109">Usage notes</span></span>

<span data-ttu-id="cd4e1-110">Tätä funktiota voidaan kutsua ER-lausekkeissa, jotka määritettiin **Kerättyjen tietojen avaimen nimi** ja **Kerättyjen tietojen avainten arvo** -ominaisuuksiksi ER-muotokomponentin **Teksti**-ryhmästä, joka sijaitsee **Yleinen\\Tiedosto**-komponentissa, jossa **Kerää tuotostiedot** -asetus on käytössä.</span><span class="sxs-lookup"><span data-stu-id="cd4e1-110">This function can be called in ER expressions that were configured for the **Collected data key name** and **Collected data key value** properties of an ER format component from the **Text** group that resides under the **Common\\File** component where the **Collect output details** option is turned on.</span></span>

## <a name="example"></a><span data-ttu-id="cd4e1-111">Esimerkki</span><span class="sxs-lookup"><span data-stu-id="cd4e1-111">Example</span></span>

<span data-ttu-id="cd4e1-112">Lisätietoja tämän toiminnon käytöstä on tehtäväoppaassa [ER Käytä tulostusmuotoa laskennassa ja summauksessa](tasks/er-format-counting-summing-1.md), joka on osa **IT-palvelujen ja -ratkaisujen komponenttien hankkiminen ja kehittäminen** -liiketoimintaprosessia.</span><span class="sxs-lookup"><span data-stu-id="cd4e1-112">For more information about how to use this function, see the [ER Use data of format output for counting and summing](tasks/er-format-counting-summing-1.md) task guide, which is part of the **Acquire/Develop IT service/solution components** business process.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="cd4e1-113">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="cd4e1-113">Additional resources</span></span>

[<span data-ttu-id="cd4e1-114">Tietojen keruutoiminnot</span><span class="sxs-lookup"><span data-stu-id="cd4e1-114">Data collection functions</span></span>](er-functions-category-data-collection.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]