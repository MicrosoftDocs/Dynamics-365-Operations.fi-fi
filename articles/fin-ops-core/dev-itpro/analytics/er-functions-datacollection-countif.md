---
title: COUNTIF ER-funktio
description: Tässä ohjeaiheessa on tietoja siitä, miten sähköisen raportoinnin (ER) COUNTIF-funktiota käytetään.
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
ms.openlocfilehash: bebb3d3b810e68fa6a0d3f4deb92b750b7c9a9f3
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2021
ms.locfileid: "5755297"
---
# <a name="countif-er-function"></a><span data-ttu-id="82a78-103">COUNTIF ER-funktio</span><span class="sxs-lookup"><span data-stu-id="82a78-103">COUNTIF ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="82a78-104">`COUNTIF`-funktio palauttaa *Kokonaislukuarvon*, joka vastaa niiden muotoelementtien määrää, jotka kerättiin, kun muotoelementtejä käytettiin lähtevän asiakirjan luomiseen muotoajon aikana ja joka täyttää määritetyn ehdon.</span><span class="sxs-lookup"><span data-stu-id="82a78-104">The `COUNTIF` function returns an *Integer* value that represents the number of format elements that was collected when the format elements were used to generate an outbound document during the format run, and that satisfies the specified condition.</span></span> <span data-ttu-id="82a78-105">Ehto muodostuu avainalueesta ja avainarvosta.</span><span class="sxs-lookup"><span data-stu-id="82a78-105">The condition consists of a key range and a key value.</span></span>

## <a name="syntax"></a><span data-ttu-id="82a78-106">Syntaksi</span><span class="sxs-lookup"><span data-stu-id="82a78-106">Syntax</span></span>

```vb
COUNTIF (condition range, condition value)
```

## <a name="arguments"></a><span data-ttu-id="82a78-107">Argumentit</span><span class="sxs-lookup"><span data-stu-id="82a78-107">Arguments</span></span>

<span data-ttu-id="82a78-108">`condition range`: *Merkkijono*</span><span class="sxs-lookup"><span data-stu-id="82a78-108">`condition range`: *String*</span></span>

<span data-ttu-id="82a78-109">Arvo, joka palautetaan lausekkeella, joka on määritetty sähköisen raportoinnin (ER) muotokomponentin **kerätyn tietoavaimen nimi** -ominaisarvoon.</span><span class="sxs-lookup"><span data-stu-id="82a78-109">A value that is returned by the expression that has been configured in the **Collected data key name** property of an Electronic reporting (ER) format component.</span></span>

<span data-ttu-id="82a78-110">`condition value`: *Merkkijono*</span><span class="sxs-lookup"><span data-stu-id="82a78-110">`condition value`: *String*</span></span>

<span data-ttu-id="82a78-111">Arvo, joka palautetaan lausekkeella, joka on määritetty ER-muotokomponentin **Kerätyn tietoavaimen arvo** -ominaisarvoon.</span><span class="sxs-lookup"><span data-stu-id="82a78-111">A value that is returned by the expression that has been configured in the **Collected data key value** property of an ER format component.</span></span>

## <a name="return-values"></a><span data-ttu-id="82a78-112">Palautusarvot</span><span class="sxs-lookup"><span data-stu-id="82a78-112">Return values</span></span>

<span data-ttu-id="82a78-113">*Kokonaisluku*</span><span class="sxs-lookup"><span data-stu-id="82a78-113">*Integer*</span></span>

<span data-ttu-id="82a78-114">Tuloksena oleva numeroarvo.</span><span class="sxs-lookup"><span data-stu-id="82a78-114">The resulting numeric value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="82a78-115">Käyttöhuomautukset</span><span class="sxs-lookup"><span data-stu-id="82a78-115">Usage notes</span></span>

<span data-ttu-id="82a78-116">**Kerättyjen tietoavainten nimen** ja **Kerättyjen tietoavainten arvon** ominaisuudet voidaan määrittää joko **sarja**-komponentille tai ER-muodon **XML-elementti**-komponentille, joka sijaitsee **yhteisessä\\tiedosto**-komponentissa, jossa **Kerää tuotostiedot** -asetus on käytössä.</span><span class="sxs-lookup"><span data-stu-id="82a78-116">The **Collected data key name** and **Collected data key value** properties can be configured for either the **Sequence** component or the **XML Element** component of an ER format that resides under the **Common\\File** component where the **Collect output details** option is turned on.</span></span>

<span data-ttu-id="82a78-117">Tämä funktio palauttaa **0** (nolla)-arvon, kun **Kerää tuotos tiedot** -vaihtoehto on poistettu käytöstä nykyisessä **Yleinen\\Tiedosto**-komponentissa.</span><span class="sxs-lookup"><span data-stu-id="82a78-117">This function returns a **0** (zero) value when the **Collect output details** option of the current **Common\\File** component is turned off.</span></span>

<span data-ttu-id="82a78-118">`condition range`-argumentessa yleismerkkiä **"\*"** voidaan käyttää kuvaamaan mitä tahansa useita merkkejä.</span><span class="sxs-lookup"><span data-stu-id="82a78-118">In the `condition range` argument, the wildcard character **"\*"** can be used to represent any multiple characters.</span></span>

<span data-ttu-id="82a78-119">`condition value`-argumentessa yleismerkkiä **"\*"** voidaan käyttää kuvaamaan mitä tahansa useita merkkejä.</span><span class="sxs-lookup"><span data-stu-id="82a78-119">In the `condition value` argument, the wildcard character **"\*"** can be used to represent any multiple characters.</span></span>

## <a name="example"></a><span data-ttu-id="82a78-120">Esimerkki</span><span class="sxs-lookup"><span data-stu-id="82a78-120">Example</span></span>

<span data-ttu-id="82a78-121">Lisätietoja tämän toiminnon käytöstä on tehtäväoppaassa [ER Käytä tulostusmuotoa laskennassa ja summauksessa](tasks/er-format-counting-summing-1.md), joka on osa **IT-palvelujen ja -ratkaisujen komponenttien hankkiminen ja kehittäminen** -liiketoimintaprosessia.</span><span class="sxs-lookup"><span data-stu-id="82a78-121">For more information about how to use this function, see the [ER Use data of format output for counting and summing](tasks/er-format-counting-summing-1.md) task guide, which is part of the **Acquire/Develop IT service/solution components** business process.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="82a78-122">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="82a78-122">Additional resources</span></span>

[<span data-ttu-id="82a78-123">Tietojen keruutoiminnot</span><span class="sxs-lookup"><span data-stu-id="82a78-123">Data collection functions</span></span>](er-functions-category-data-collection.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]