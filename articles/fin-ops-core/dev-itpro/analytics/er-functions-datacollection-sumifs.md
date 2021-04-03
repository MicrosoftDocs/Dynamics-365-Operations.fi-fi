---
title: SUMIFS ER-funktio
description: Tässä ohjeaiheessa on tietoja siitä, miten sähköisen raportoinnin (ER) SUMIFS-funktiota käytetään.
author: NickSelin
manager: kfend
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
ms.openlocfilehash: ff5ad3371a6e18ca1a3ee855e3b35f51f7513ef0
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/09/2021
ms.locfileid: "5564756"
---
# <a name="sumifs-er-function"></a><span data-ttu-id="6ff35-103">SUMIFS ER-funktio</span><span class="sxs-lookup"><span data-stu-id="6ff35-103">SUMIFS ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6ff35-104">`SUMIFS`-funktio palauttaa *Todellisen* arvon, joka on niiden arvojen summa, jotka palautettiin muotoiluelementtien sitomisella ja, jotka kerättiin, kun muotoelementtejä käytettiin lähtevän asiakirjan luomiseen muotoajon aikana ja joka täyttää määritetyt ehdot.</span><span class="sxs-lookup"><span data-stu-id="6ff35-104">The `SUMIFS` function returns a *Real* value that represents the sum of values that were returned by bindings of format elements and collected when the format elements were used to generate an outbound document during the format run, and that satisfies the specified conditions.</span></span> <span data-ttu-id="6ff35-105">Jokainen ehto muodostuu avainalueesta ja avainarvosta.</span><span class="sxs-lookup"><span data-stu-id="6ff35-105">Each condition consists of a key range and a key value.</span></span>

## <a name="syntax"></a><span data-ttu-id="6ff35-106">Syntaksi</span><span class="sxs-lookup"><span data-stu-id="6ff35-106">Syntax</span></span>

```vb
SUMIFS (key name for summing, condition 1 range, condition 1 value[, condition 2 range, condition 2 value, …, condition N range, condition N value])
```

## <a name="arguments"></a><span data-ttu-id="6ff35-107">Argumentit</span><span class="sxs-lookup"><span data-stu-id="6ff35-107">Arguments</span></span>

<span data-ttu-id="6ff35-108">`key name for summing`: *Merkkijono*</span><span class="sxs-lookup"><span data-stu-id="6ff35-108">`key name for summing`: *String*</span></span>

<span data-ttu-id="6ff35-109">Arvo, joka palautetaan lausekkeella, joka on määritetty sähköisen raportoinnin (ER) muoto-osan **kerätyn tietoavaimen nimi** -ominaisarvoon, jolle sidonnan arvoa on käytettävä summaustarkoituksiin.</span><span class="sxs-lookup"><span data-stu-id="6ff35-109">A value that is returned by the expression that has been configured in the **Collected data key name** property of the Electronic reporting (ER) format component for which the value of the binding must be used for summing purposes.</span></span>

<span data-ttu-id="6ff35-110">**Kerättyjen tietoavainten nimi** -ominaisuus voidaan määrittää joko **Numeeriselle** komponentille tai ER-muodon **Merkkijono**-komponentille, joka sijaitsee **yhteinen\\tiedosto**-komponentissa, jossa **Kerää tuotostiedot** -asetus on käytössä.</span><span class="sxs-lookup"><span data-stu-id="6ff35-110">The **Collected data key name** property can be configured for either a **Numeric** component or a **String** component of an ER format that resides under the **Common\\File** component where the **Collect output details** option is turned on.</span></span>

<span data-ttu-id="6ff35-111">`condition 1 range`: *Merkkijono*</span><span class="sxs-lookup"><span data-stu-id="6ff35-111">`condition 1 range`: *String*</span></span>

<span data-ttu-id="6ff35-112">Arvo, joka palautetaan lausekkeella, joka on määritetty ER-muotokomponentin **Kerätyn tietoavaimen nimi** -ominaisarvoon.</span><span class="sxs-lookup"><span data-stu-id="6ff35-112">A value that is returned by the expression that has been configured in the **Collected data key name** property of an ER format component.</span></span> <span data-ttu-id="6ff35-113">Tämä argumentti on pakollinen.</span><span class="sxs-lookup"><span data-stu-id="6ff35-113">This argument is mandatory.</span></span>

<span data-ttu-id="6ff35-114">**Kerättyjen tietoavainten nimi** -ominaisuus voidaan määrittää joko **sarja**-komponentille tai ER-muodon **XML-elementti**-komponentille, joka sijaitsee **yhteinen\\tiedosto**-komponentissa, jossa **Kerää tuotostiedot** -asetus on käytössä.</span><span class="sxs-lookup"><span data-stu-id="6ff35-114">The **Collected data key name** property can be configured for either a **Sequence** component or an **XML Element** component of an ER format that resides under the **Common\\File** component where the **Collect output details** option is turned on.</span></span>

<span data-ttu-id="6ff35-115">`condition 1 value`: *Merkkijono*</span><span class="sxs-lookup"><span data-stu-id="6ff35-115">`condition 1 value`: *String*</span></span>

<span data-ttu-id="6ff35-116">Arvo, joka palautetaan lausekkeella, joka on määritetty ER-muotokomponentin **Kerätyn tietoavaimen arvo** -ominaisarvoon.</span><span class="sxs-lookup"><span data-stu-id="6ff35-116">A value that is returned by the expression that has been configured in the **Collected data key value** property of an ER format component.</span></span> <span data-ttu-id="6ff35-117">Tämä argumentti on pakollinen.</span><span class="sxs-lookup"><span data-stu-id="6ff35-117">This argument is mandatory.</span></span>

<span data-ttu-id="6ff35-118">**Kerättyjen tietoavainten nimi** -ominaisuus voidaan määrittää joko **sarja**-komponentille tai ER-muodon **XML-elementti**-komponentille, joka sijaitsee **yhteinen\\tiedosto**-komponentissa, jossa **Kerää tuotostiedot** -asetus on käytössä.</span><span class="sxs-lookup"><span data-stu-id="6ff35-118">The **Collected data key value** property can be configured for either a **Sequence** component or an **XML Element** component of an ER format that resides under the **Common\\File** component where the **Collect output details** option is turned on.</span></span>

<span data-ttu-id="6ff35-119">`condition N range`: *Merkkijono*</span><span class="sxs-lookup"><span data-stu-id="6ff35-119">`condition N range`: *String*</span></span>

<span data-ttu-id="6ff35-120">Arvo, joka palautetaan lausekkeella, joka on määritetty ER-muotokomponentin **Kerätyn tietoavaimen nimi** -ominaisarvoon.</span><span class="sxs-lookup"><span data-stu-id="6ff35-120">A value that is returned by the expression that has been configured in the **Collected data key name** property of an ER format component.</span></span> <span data-ttu-id="6ff35-121">Nämä lisäargumentit ovat valinnaisia.</span><span class="sxs-lookup"><span data-stu-id="6ff35-121">These additional arguments are optional.</span></span>

<span data-ttu-id="6ff35-122">**Kerättyjen tietoavainten nimi** -ominaisuus voidaan määrittää joko **sarja**-komponentille tai ER-muodon **XML-elementti**-komponentille, joka sijaitsee **yhteinen\\tiedosto**-komponentissa, jossa **Kerää tuotostiedot** -asetus on käytössä.</span><span class="sxs-lookup"><span data-stu-id="6ff35-122">The **Collected data key name** property can be configured for either a **Sequence** component or an **XML Element** component of an ER format that resides under the **Common\\File** component where the **Collect output details** option is turned on.</span></span>

<span data-ttu-id="6ff35-123">`condition N value`: *Merkkijono*</span><span class="sxs-lookup"><span data-stu-id="6ff35-123">`condition N value`: *String*</span></span>

<span data-ttu-id="6ff35-124">Arvo, joka palautetaan lausekkeella, joka on määritetty ER-muotokomponentin **Kerätyn tietoavaimen arvo** -ominaisarvoon.</span><span class="sxs-lookup"><span data-stu-id="6ff35-124">A value that is returned by the expression that has been configured in the **Collected data key value** property of an ER format component.</span></span> <span data-ttu-id="6ff35-125">Nämä lisäargumentit ovat valinnaisia.</span><span class="sxs-lookup"><span data-stu-id="6ff35-125">These additional arguments are optional.</span></span>

<span data-ttu-id="6ff35-126">**Kerättyjen tietoavainten nimi** -ominaisuus voidaan määrittää joko **sarja**-komponentille tai ER-muodon **XML-elementti**-komponentille, joka sijaitsee **yhteinen\\tiedosto**-komponentissa, jossa **Kerää tuotostiedot** -asetus on käytössä.</span><span class="sxs-lookup"><span data-stu-id="6ff35-126">The **Collected data key value** property can be configured for either a **Sequence** component or an **XML Element** component of an ER format that resides under the **Common\\File** component where the **Collect output details** option is turned on.</span></span>

## <a name="return-values"></a><span data-ttu-id="6ff35-127">Palautusarvot</span><span class="sxs-lookup"><span data-stu-id="6ff35-127">Return values</span></span>

<span data-ttu-id="6ff35-128">*Reaaliluku*</span><span class="sxs-lookup"><span data-stu-id="6ff35-128">*Real*</span></span>

<span data-ttu-id="6ff35-129">Tuloksena oleva numeroarvo.</span><span class="sxs-lookup"><span data-stu-id="6ff35-129">The resulting numeric value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="6ff35-130">Käyttöhuomautukset</span><span class="sxs-lookup"><span data-stu-id="6ff35-130">Usage notes</span></span>

<span data-ttu-id="6ff35-131">Tämä funktio palauttaa **0** (nolla)-arvon, kun **Kerää tuotos tiedot** -vaihtoehto on poistettu käytöstä nykyisessä **Yleinen\\Tiedosto**-komponentissa.</span><span class="sxs-lookup"><span data-stu-id="6ff35-131">This function returns a **0** (zero) value when the **Collect output details** option of the current **Common\\File** component is turned off.</span></span>

<span data-ttu-id="6ff35-132">`condition range`-argumenteissa yleismerkkiä **"\*"** voidaan käyttää kuvaamaan mitä tahansa useita merkkejä.</span><span class="sxs-lookup"><span data-stu-id="6ff35-132">In the `condition range` arguments, the wildcard character **"\*"** can be used to represent any multiple characters.</span></span>

<span data-ttu-id="6ff35-133">`condition value`-argumenteissa yleismerkkiä **"\*"** voidaan käyttää kuvaamaan mitä tahansa useita merkkejä.</span><span class="sxs-lookup"><span data-stu-id="6ff35-133">In the `condition value` arguments, the wildcard character **"\*"** can be used to represent any multiple characters.</span></span>

## <a name="example"></a><span data-ttu-id="6ff35-134">Esimerkki</span><span class="sxs-lookup"><span data-stu-id="6ff35-134">Example</span></span>

<span data-ttu-id="6ff35-135">Lisätietoja tämän toiminnon käytöstä on tehtäväoppaassa [ER Käytä tulostusmuotoa laskennassa ja summauksessa](tasks/er-format-counting-summing-1.md), joka on osa **IT-palvelujen ja -ratkaisujen komponenttien hankkiminen ja kehittäminen** -liiketoimintaprosessia.</span><span class="sxs-lookup"><span data-stu-id="6ff35-135">For more information about how to use this function, see the [ER Use data of format output for counting and summing](tasks/er-format-counting-summing-1.md) task guide, which is part of the **Acquire/Develop IT service/solution components** business process.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="6ff35-136">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="6ff35-136">Additional resources</span></span>

[<span data-ttu-id="6ff35-137">Tietojen keruutoiminnot</span><span class="sxs-lookup"><span data-stu-id="6ff35-137">Data collection functions</span></span>](er-functions-category-data-collection.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]