---
title: COUNTIFS ER-funktio
description: Tässä ohjeaiheessa on tietoja siitä, miten sähköisen raportoinnin (ER) COUNTIFS-funktiota käytetään.
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
ms.openlocfilehash: 9627c7835c8f3f1b6aedc1f691470dc29a11d6b5
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/12/2020
ms.locfileid: "3042547"
---
# <span data-ttu-id="eecac-103"><a name="COUNTIFS">COUNTIFS ER-funktio</a></span><span class="sxs-lookup"><span data-stu-id="eecac-103"><a name="COUNTIFS">COUNTIFS ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="eecac-104">`COUNTIFS`-funktio palauttaa *Kokonaislukuarvon*, joka vastaa niiden muotoelementtien määrää, jotka kerättiin, kun muotoelementtejä käytettiin lähtevän asiakirjan luomiseen muotoajon aikana ja joka täyttää määritetyt ehdot.</span><span class="sxs-lookup"><span data-stu-id="eecac-104">The `COUNTIFS` function returns an *Integer* value that represents the number of format elements that was collected when the format elements were used to generate an outbound document during the format run, and that satisfies the specified conditions.</span></span> <span data-ttu-id="eecac-105">Jokainen ehto muodostuu avainalueesta ja avainarvosta.</span><span class="sxs-lookup"><span data-stu-id="eecac-105">Each condition consists of a key range and a key value.</span></span>

## <a name="syntax"></a><span data-ttu-id="eecac-106">Syntaksi</span><span class="sxs-lookup"><span data-stu-id="eecac-106">Syntax</span></span>

```vb
COUNTIFS (condition 1 range, condition 1 value[, condition 2 range, condition 2 value, …, condition N range, condition N value])
```

## <a name="arguments"></a><span data-ttu-id="eecac-107">Argumentit</span><span class="sxs-lookup"><span data-stu-id="eecac-107">Arguments</span></span>

<span data-ttu-id="eecac-108">`condition 1 range`: *Merkkijono*</span><span class="sxs-lookup"><span data-stu-id="eecac-108">`condition 1 range`: *String*</span></span>

<span data-ttu-id="eecac-109">Arvo, joka palautetaan lausekkeella, joka on määritetty sähköisen raportoinnin (ER) muotokomponentin **kerätyn tietoavaimen nimi** -ominaisarvoon.</span><span class="sxs-lookup"><span data-stu-id="eecac-109">A value that is returned by the expression that has been configured in the **Collected data key name** property of an Electronic reporting (ER) format component.</span></span> <span data-ttu-id="eecac-110">Tämä argumentti on pakollinen.</span><span class="sxs-lookup"><span data-stu-id="eecac-110">This argument is mandatory.</span></span>

<span data-ttu-id="eecac-111">`condition 1 value`: *Merkkijono*</span><span class="sxs-lookup"><span data-stu-id="eecac-111">`condition 1 value`: *String*</span></span>

<span data-ttu-id="eecac-112">Arvo, joka palautetaan lausekkeella, joka on määritetty ER-muotokomponentin **Kerätyn tietoavaimen arvo** -ominaisarvoon.</span><span class="sxs-lookup"><span data-stu-id="eecac-112">A value that is returned by the expression that has been configured in the **Collected data key value** property of an ER format component.</span></span> <span data-ttu-id="eecac-113">Tämä argumentti on pakollinen.</span><span class="sxs-lookup"><span data-stu-id="eecac-113">This argument is mandatory.</span></span>

<span data-ttu-id="eecac-114">`condition N range`: *Merkkijono*</span><span class="sxs-lookup"><span data-stu-id="eecac-114">`condition N range`: *String*</span></span>

<span data-ttu-id="eecac-115">Arvo, joka palautetaan lausekkeella, joka on määritetty ER-muotokomponentin **Kerätyn tietoavaimen nimi** -ominaisarvoon.</span><span class="sxs-lookup"><span data-stu-id="eecac-115">A value that is returned by the expression that has been configured in the **Collected data key name** property of an ER format component.</span></span> <span data-ttu-id="eecac-116">Nämä lisäargumentit ovat valinnaisia.</span><span class="sxs-lookup"><span data-stu-id="eecac-116">These additional arguments are optional.</span></span>

<span data-ttu-id="eecac-117">`condition N value`: *Merkkijono*</span><span class="sxs-lookup"><span data-stu-id="eecac-117">`condition N value`: *String*</span></span>

<span data-ttu-id="eecac-118">Arvo, joka palautetaan lausekkeella, joka on määritetty ER-muotokomponentin **Kerätyn tietoavaimen arvo** -ominaisarvoon.</span><span class="sxs-lookup"><span data-stu-id="eecac-118">A value that is returned by the expression that has been configured in the **Collected data key value** property of an ER format component.</span></span> <span data-ttu-id="eecac-119">Nämä lisäargumentit ovat valinnaisia.</span><span class="sxs-lookup"><span data-stu-id="eecac-119">These additional arguments are optional.</span></span>

## <a name="return-values"></a><span data-ttu-id="eecac-120">Palautusarvot</span><span class="sxs-lookup"><span data-stu-id="eecac-120">Return values</span></span>

<span data-ttu-id="eecac-121">*Kokonaisluku*</span><span class="sxs-lookup"><span data-stu-id="eecac-121">*Integer*</span></span>

<span data-ttu-id="eecac-122">Tuloksena oleva numeroarvo.</span><span class="sxs-lookup"><span data-stu-id="eecac-122">The resulting numeric value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="eecac-123">Käyttöhuomautukset</span><span class="sxs-lookup"><span data-stu-id="eecac-123">Usage notes</span></span>

<span data-ttu-id="eecac-124">**Kerättyjen tietoavainten nimen** ja **Kerättyjen tietoavainten arvon** ominaisuudet voidaan määrittää joko **sarja**-komponentille tai ER-muodon **XML-elementti**-komponentille, joka sijaitsee **yhteisessä\\tiedosto**-komponentissa, jossa **Kerää tuotostiedot** -asetus on käytössä.</span><span class="sxs-lookup"><span data-stu-id="eecac-124">The **Collected data key name** and **Collected data key value** properties can be configured for either the **Sequence** component or the **XML Element** component of an ER format that resides under the **Common\\File** component where the **Collect output details** option is turned on.</span></span>

<span data-ttu-id="eecac-125">Tämä funktio palauttaa **0** (nolla)-arvon, kun **Kerää tuotos tiedot** -vaihtoehto on poistettu käytöstä nykyisessä **Yleinen\\Tiedosto**-komponentissa.</span><span class="sxs-lookup"><span data-stu-id="eecac-125">This function returns a **0** (zero) value when the **Collect output details** option of the current **Common\\File** component is turned off.</span></span>

<span data-ttu-id="eecac-126">`condition range`-argumenteissa yleismerkkiä **"\*"** voidaan käyttää kuvaamaan mitä tahansa useita merkkejä.</span><span class="sxs-lookup"><span data-stu-id="eecac-126">In `condition range` arguments, the wildcard character **"\*"** can be used to represent any multiple characters.</span></span>

<span data-ttu-id="eecac-127">`condition value`-argumenteissa yleismerkkiä **"\*"** voidaan käyttää kuvaamaan mitä tahansa useita merkkejä.</span><span class="sxs-lookup"><span data-stu-id="eecac-127">In `condition value` arguments, the wildcard character **"\*"** can be used to represent any multiple characters.</span></span>

## <a name="example"></a><span data-ttu-id="eecac-128">Esimerkki</span><span class="sxs-lookup"><span data-stu-id="eecac-128">Example</span></span>

<span data-ttu-id="eecac-129">Lisätietoja tämän toiminnon käytöstä on tehtäväoppaassa [ER Käytä tulostusmuotoa laskennassa ja summauksessa](tasks/er-format-counting-summing-1.md), joka on osa **IT-palvelujen ja -ratkaisujen komponenttien hankkiminen ja kehittäminen** -liiketoimintaprosessia.</span><span class="sxs-lookup"><span data-stu-id="eecac-129">For more information about how to use this function, see the [ER Use data of format output for counting and summing](tasks/er-format-counting-summing-1.md) task guide, which is part of the **Acquire/Develop IT service/solution components** business process.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="eecac-130">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="eecac-130">Additional resources</span></span>

[<span data-ttu-id="eecac-131">Tietojen keruutoiminnot</span><span class="sxs-lookup"><span data-stu-id="eecac-131">Data collection functions</span></span>](er-functions-category-data-collection.md)
