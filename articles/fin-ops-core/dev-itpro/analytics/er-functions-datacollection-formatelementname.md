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
ms.openlocfilehash: 5f299a4bb697afce152a61ec35fcefab7157f356
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/12/2020
ms.locfileid: "3042524"
---
# <span data-ttu-id="fb422-103"><a name="FORMATELEMENTNAME">FORMATELEMENTNAME ER -funktio</a></span><span class="sxs-lookup"><span data-stu-id="fb422-103"><a name="FORMATELEMENTNAME">FORMATELEMENTNAME ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="fb422-104">`FORMATELEMENTNAME`-funktio palauttaa *Merkkijonoarvon*, joka edustaa nykyisen sähköisen raportoinnin (ER) muodon elementin nimeä.</span><span class="sxs-lookup"><span data-stu-id="fb422-104">The `FORMATELEMENTNAME` function returns a *String* value that represents the name of the current Electronic reporting (ER) format's element.</span></span>

## <a name="syntax"></a><span data-ttu-id="fb422-105">Syntaksi</span><span class="sxs-lookup"><span data-stu-id="fb422-105">Syntax</span></span>

```vb
FORMATELEMENTNAME ()
```

## <a name="return-values"></a><span data-ttu-id="fb422-106">Palautusarvot</span><span class="sxs-lookup"><span data-stu-id="fb422-106">Return values</span></span>

<span data-ttu-id="fb422-107">*merkkijono*</span><span class="sxs-lookup"><span data-stu-id="fb422-107">*String*</span></span>

<span data-ttu-id="fb422-108">Tulokseksi saatava tekstiarvo.</span><span class="sxs-lookup"><span data-stu-id="fb422-108">The resulting text value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="fb422-109">Käyttöhuomautukset</span><span class="sxs-lookup"><span data-stu-id="fb422-109">Usage notes</span></span>

<span data-ttu-id="fb422-110">Tätä funktiota voidaan kutsua ER-lausekkeissa, jotka määritettiin **Kerättyjen tietojen avaimen nimi** ja **Kerättyjen tietojen avainten arvo** -ominaisuuksiksi ER-muotokomponentin **Teksti**-ryhmästä, joka sijaitsee **Yleinen\\Tiedosto**-komponentissa, jossa **Kerää tuotostiedot** -asetus on käytössä.</span><span class="sxs-lookup"><span data-stu-id="fb422-110">This function can be called in ER expressions that were configured for the **Collected data key name** and **Collected data key value** properties of an ER format component from the **Text** group that resides under the **Common\\File** component where the **Collect output details** option is turned on.</span></span>

## <a name="example"></a><span data-ttu-id="fb422-111">Esimerkki</span><span class="sxs-lookup"><span data-stu-id="fb422-111">Example</span></span>

<span data-ttu-id="fb422-112">Lisätietoja tämän toiminnon käytöstä on tehtäväoppaassa [ER Käytä tulostusmuotoa laskennassa ja summauksessa](tasks/er-format-counting-summing-1.md), joka on osa **IT-palvelujen ja -ratkaisujen komponenttien hankkiminen ja kehittäminen** -liiketoimintaprosessia.</span><span class="sxs-lookup"><span data-stu-id="fb422-112">For more information about how to use this function, see the [ER Use data of format output for counting and summing](tasks/er-format-counting-summing-1.md) task guide, which is part of the **Acquire/Develop IT service/solution components** business process.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="fb422-113">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="fb422-113">Additional resources</span></span>

[<span data-ttu-id="fb422-114">Tietojen keruutoiminnot</span><span class="sxs-lookup"><span data-stu-id="fb422-114">Data collection functions</span></span>](er-functions-category-data-collection.md)
