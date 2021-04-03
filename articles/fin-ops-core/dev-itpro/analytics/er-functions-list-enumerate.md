---
title: ENUMERATE ER-funktio
description: Tässä ohjeaiheessa on tietoja siitä, miten sähköisen raportoinnin (ER) ENUMERATE-funktiota käytetään.
author: NickSelin
manager: kfend
ms.date: 12/12/2019
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
ms.openlocfilehash: 0827fe33a548970c7673ac2ab830bb22d367c8cc
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/09/2021
ms.locfileid: "5567865"
---
# <a name="enumerate-er-function"></a><span data-ttu-id="5d5ee-103">ENUMERATE ER-funktio</span><span class="sxs-lookup"><span data-stu-id="5d5ee-103">ENUMERATE ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5d5ee-104">`ENUMERATE`-funktio palauttaa uuden *Tietueluettelon* arvon, joka koostuu määritetyn luettelon valintalistan tietueista.</span><span class="sxs-lookup"><span data-stu-id="5d5ee-104">The `ENUMERATE` function returns a new *Record list* value that consists of enumerated records of the specified list.</span></span>

## <a name="syntax"></a><span data-ttu-id="5d5ee-105">Syntaksi</span><span class="sxs-lookup"><span data-stu-id="5d5ee-105">Syntax</span></span>

```vb
ENUMERATE (list)
```

## <a name="arguments"></a><span data-ttu-id="5d5ee-106">Argumentit</span><span class="sxs-lookup"><span data-stu-id="5d5ee-106">Arguments</span></span>

<span data-ttu-id="5d5ee-107">`list`: *Tietueluettelo*</span><span class="sxs-lookup"><span data-stu-id="5d5ee-107">`list`: *Record list*</span></span>

<span data-ttu-id="5d5ee-108">*Tietueluettelo*-tietotyypin tietolähteen kelvollinen polku.</span><span class="sxs-lookup"><span data-stu-id="5d5ee-108">The valid path of a data source of the *Record list* data type.</span></span>

## <a name="return-values"></a><span data-ttu-id="5d5ee-109">Palautusarvot</span><span class="sxs-lookup"><span data-stu-id="5d5ee-109">Return values</span></span>

<span data-ttu-id="5d5ee-110">*Tietueluettelo*</span><span class="sxs-lookup"><span data-stu-id="5d5ee-110">*Record list*</span></span>

<span data-ttu-id="5d5ee-111">Tuloksena oleva tietueluettelo.</span><span class="sxs-lookup"><span data-stu-id="5d5ee-111">The resulting list of records.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="5d5ee-112">Käyttöhuomautukset</span><span class="sxs-lookup"><span data-stu-id="5d5ee-112">Usage notes</span></span>

<span data-ttu-id="5d5ee-113">Palautettujen luetteloidut tietueet -luettelo paljastaa seuraavat lisäelementit:</span><span class="sxs-lookup"><span data-stu-id="5d5ee-113">The list of enumerated records that is returned exposes the following additional elements:</span></span>

- <span data-ttu-id="5d5ee-114">Kenttien tietue (**Arvo**-komponentti)</span><span class="sxs-lookup"><span data-stu-id="5d5ee-114">The record of fields (**Value** component)</span></span>
- <span data-ttu-id="5d5ee-115">Nykyisen tietueen indeksi (**numero**-komponentti)</span><span class="sxs-lookup"><span data-stu-id="5d5ee-115">The current record index (**Number** component)</span></span>

## <a name="example"></a><span data-ttu-id="5d5ee-116">Esimerkki</span><span class="sxs-lookup"><span data-stu-id="5d5ee-116">Example</span></span>

<span data-ttu-id="5d5ee-117">Seuraavassa kuvassa **Numeroitu**-tietolähde luodaan toimittajan tietueiden numeroituna luettelona **Toimittajat**-tietolähteestä, joka viittaa VendTable-tauluun.</span><span class="sxs-lookup"><span data-stu-id="5d5ee-117">In the following illustration, an **Enumerated** data source is created as an enumerated list of vendor records from the **Vendors** data source that refers to the VendTable table.</span></span>

<a href="./media/picture-enumerate-datasource.jpg"><img src="./media/picture-enumerate-datasource.jpg" alt="Enumerated data source" class="alignnone wp-image-290711 size-full" width="387" height="136" /></a>

<span data-ttu-id="5d5ee-118">Seuraavassa kuvassa on sähköisen raportoinnin (ER) muodon.</span><span class="sxs-lookup"><span data-stu-id="5d5ee-118">The following illustration shows the Electronic reporting (ER) format.</span></span> <span data-ttu-id="5d5ee-119">Tässä muodossa tiedon sidonnat luodaan muodostamaan tulos XML-muodossa.</span><span class="sxs-lookup"><span data-stu-id="5d5ee-119">In this format, data bindings are created to generate output in XML format.</span></span> <span data-ttu-id="5d5ee-120">Tämä tulos esittää yksittäiset toimittajat luetteloituina solmuina.</span><span class="sxs-lookup"><span data-stu-id="5d5ee-120">This output presents individual vendors as enumerated nodes.</span></span>

<a href="./media/picture-enumerate-format.jpg"><img src="./media/picture-enumerate-format.jpg" alt="Format that has data bindings" class="alignnone wp-image-290721 size-full" width="414" height="138" /></a>

<span data-ttu-id="5d5ee-121">Seuraavassa kuvassa on tulos, kun suunniteltu muoto suoritetaan.</span><span class="sxs-lookup"><span data-stu-id="5d5ee-121">The following illustration shows the result when the designed format is run.</span></span>

<a href="./media/picture-enumerate-result.jpg"><img src="./media/picture-enumerate-result.jpg" alt="Result of running the format" class="alignnone wp-image-290731 size-full" width="567" height="176" /></a>

## <a name="additional-resources"></a><span data-ttu-id="5d5ee-122">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="5d5ee-122">Additional resources</span></span>

[<span data-ttu-id="5d5ee-123">Luettelotoiminnot</span><span class="sxs-lookup"><span data-stu-id="5d5ee-123">List functions</span></span>](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]