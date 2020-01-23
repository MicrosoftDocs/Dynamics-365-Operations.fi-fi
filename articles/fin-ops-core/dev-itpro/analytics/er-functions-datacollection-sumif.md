---
title: SUMIF ER-funktio
description: Tässä ohjeaiheessa on tietoja siitä, miten sähköisen raportoinnin (ER) SUMIF-funktiota käytetään.
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
ms.openlocfilehash: 579b14c713bc5f9831c5e012d16bb3b6f97b1035
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/20/2019
ms.locfileid: "2916427"
---
# <span data-ttu-id="47f8d-103"><a name="SUMIF">SUMIF ER-funktio</a></span><span class="sxs-lookup"><span data-stu-id="47f8d-103"><a name="SUMIF">SUMIF ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="47f8d-104">`SUMIF`-funktio palauttaa *Todellisen* arvon, joka on niiden arvojen summa, jotka palautettiin muotoiluelementtien sitomisella ja, jotka kerättiin, kun muotoelementtejä käytettiin lähtevän asiakirjan luomiseen muotoajon aikana ja joka täyttää määritetyn ehdon.</span><span class="sxs-lookup"><span data-stu-id="47f8d-104">The `SUMIF` function returns a *Real* value that represents the sum of values that were returned by bindings of format elements and collected when the format elements were used to generate an outbound document during the format run, and that satisfies the specified condition.</span></span> <span data-ttu-id="47f8d-105">Ehto muodostuu avainalueesta ja avainarvosta.</span><span class="sxs-lookup"><span data-stu-id="47f8d-105">The condition consists of a key range and a key value.</span></span>

## <a name="syntax"></a><span data-ttu-id="47f8d-106">Syntaksi</span><span class="sxs-lookup"><span data-stu-id="47f8d-106">Syntax</span></span>

```
SUMIF (key name for summing, condition range, condition value)
```

## <a name="arguments"></a><span data-ttu-id="47f8d-107">Argumentit</span><span class="sxs-lookup"><span data-stu-id="47f8d-107">Arguments</span></span>

<span data-ttu-id="47f8d-108">`key name for summing`: *Merkkijono*</span><span class="sxs-lookup"><span data-stu-id="47f8d-108">`key name for summing`: *String*</span></span>

<span data-ttu-id="47f8d-109">Arvo, joka palautetaan lausekkeella, joka on määritetty sähköisen raportoinnin (ER) muoto-osan **kerätyn tietoavaimen nimi** -ominaisarvoon, jolle sidonnan arvoa on käytettävä summaustarkoituksiin.</span><span class="sxs-lookup"><span data-stu-id="47f8d-109">A value that is returned by the expression that has been configured in the **Collected data key name** property of the Electronic reporting (ER) format component for which the value of the binding must be used for summing purposes.</span></span>

<span data-ttu-id="47f8d-110">**Kerättyjen tietoavainten nimi** -ominaisuus voidaan määrittää joko **sarja**-komponentille tai ER-muodon **XML-elementti**-komponentille, joka sijaitsee **yhteinen\\tiedosto**-komponentissa, jossa **Kerää tuotostiedot** -asetus on käytössä.</span><span class="sxs-lookup"><span data-stu-id="47f8d-110">The **Collected data key value** property can be configured for either a **Sequence** component or an **XML Element** component of an ER format that resides under the **Common\\File** component where the **Collect output details** option is turned on.</span></span>

## <a name="return-values"></a><span data-ttu-id="47f8d-111">Palautusarvot</span><span class="sxs-lookup"><span data-stu-id="47f8d-111">Return values</span></span>

<span data-ttu-id="47f8d-112">*Reaaliluku*</span><span class="sxs-lookup"><span data-stu-id="47f8d-112">*Real*</span></span>

<span data-ttu-id="47f8d-113">Tuloksena oleva numeroarvo.</span><span class="sxs-lookup"><span data-stu-id="47f8d-113">The resulting numeric value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="47f8d-114">Käyttöhuomautukset</span><span class="sxs-lookup"><span data-stu-id="47f8d-114">Usage notes</span></span>

<span data-ttu-id="47f8d-115">Tämä funktio palauttaa **0** (nolla)-arvon, kun **Kerää tuotos tiedot** -vaihtoehto on poistettu käytöstä nykyisessä **Yleinen\\Tiedosto**-komponentissa.</span><span class="sxs-lookup"><span data-stu-id="47f8d-115">This function returns a **0** (zero) value when the **Collect output details** option of the current **Common\\File** component is turned off.</span></span>

<span data-ttu-id="47f8d-116">`condition range`-argumentessa yleismerkkiä **"\*"** voidaan käyttää kuvaamaan mitä tahansa useita merkkejä.</span><span class="sxs-lookup"><span data-stu-id="47f8d-116">In the `condition range` argument, the wildcard character **"\*"** can be used to represent any multiple characters.</span></span>

<span data-ttu-id="47f8d-117">`condition value`-argumentessa yleismerkkiä **"\*"** voidaan käyttää kuvaamaan mitä tahansa useita merkkejä.</span><span class="sxs-lookup"><span data-stu-id="47f8d-117">In the `condition value` argument, the wildcard character **"\*"** can be used to represent any multiple characters.</span></span>

## <a name="example"></a><span data-ttu-id="47f8d-118">Esimerkki</span><span class="sxs-lookup"><span data-stu-id="47f8d-118">Example</span></span>

<span data-ttu-id="47f8d-119">Lisätietoja tämän toiminnon käytöstä on tehtäväoppaassa [ER Käytä tulostusmuotoa laskennassa ja summauksessa](tasks/er-format-counting-summing-1.md), joka on osa **IT-palvelujen ja -ratkaisujen komponenttien hankkiminen ja kehittäminen** -liiketoimintaprosessia.</span><span class="sxs-lookup"><span data-stu-id="47f8d-119">For more information about how to use this function, see the [ER Use data of format output for counting and summing](tasks/er-format-counting-summing-1.md) task guide, which is part of the **Acquire/Develop IT service/solution components** business process.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="47f8d-120">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="47f8d-120">Additional resources</span></span>

[<span data-ttu-id="47f8d-121">Tietojen keruutoiminnot</span><span class="sxs-lookup"><span data-stu-id="47f8d-121">Data collection functions</span></span>](er-functions-category-data-collection.md)
