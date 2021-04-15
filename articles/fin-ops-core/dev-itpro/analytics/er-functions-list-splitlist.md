---
title: SPLITLIST ER-funktio
description: Tässä ohjeaiheessa on tietoja siitä, miten sähköisen raportoinnin (ER) SPLITLIST-funktiota käytetään.
author: NickSelin
ms.date: 03/15/2021
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
ms.openlocfilehash: 99e199e238b3132622a8b305895637b430e8f6d2
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2021
ms.locfileid: "5745566"
---
# <a name="splitlist-er-function"></a><span data-ttu-id="344d9-103">SPLITLIST ER-funktio</span><span class="sxs-lookup"><span data-stu-id="344d9-103">SPLITLIST ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="344d9-104">`SPLITLIST`-funktio jakaa määritetyn luettelon aliluetteloiksi (tai eriksi), joissa on tietty määrä tietueita.</span><span class="sxs-lookup"><span data-stu-id="344d9-104">The `SPLITLIST` function splits the specified list into sublists (or batches), each of which contains the specified number of records.</span></span> <span data-ttu-id="344d9-105">Sitten se palauttaa tuloksen uutena *Tietueluettelon* arvona, joka koostuu eristä.</span><span class="sxs-lookup"><span data-stu-id="344d9-105">It then returns the result as a new *Record list* value that consists of the batches.</span></span>

## <a name="syntax-1"></a><span data-ttu-id="344d9-106">Syntaksi 1</span><span class="sxs-lookup"><span data-stu-id="344d9-106">Syntax 1</span></span>

```vb
SPLITLIST (list, number)
```

## <a name="syntax-2"></a><span data-ttu-id="344d9-107">Syntaksi 2</span><span class="sxs-lookup"><span data-stu-id="344d9-107">Syntax 2</span></span>

```vb
SPLITLIST (list, number, on-demand reading flag)
```

## <a name="arguments"></a><span data-ttu-id="344d9-108">Argumentit</span><span class="sxs-lookup"><span data-stu-id="344d9-108">Arguments</span></span>

<span data-ttu-id="344d9-109">`list`: *Tietueluettelo*</span><span class="sxs-lookup"><span data-stu-id="344d9-109">`list`: *Record list*</span></span>

<span data-ttu-id="344d9-110">*Tietueluettelo*-tietotyypin tietolähteen kelvollinen polku.</span><span class="sxs-lookup"><span data-stu-id="344d9-110">The valid path of a data source of the *Record list* data type.</span></span>

<span data-ttu-id="344d9-111">`number`: *Kokonaisluku*</span><span class="sxs-lookup"><span data-stu-id="344d9-111">`number`: *Integer*</span></span>

<span data-ttu-id="344d9-112">Tietueiden enimmäismäärä erää kohti.</span><span class="sxs-lookup"><span data-stu-id="344d9-112">The maximum number of records per batch.</span></span>

<span data-ttu-id="344d9-113">`on-demand reading flag`: *Totuusarvo*</span><span class="sxs-lookup"><span data-stu-id="344d9-113">`on-demand reading flag`: *Boolean*</span></span>

<span data-ttu-id="344d9-114">*Totuusarvo* joka määrittää, luodaanko aliluetteloiden elementtejä tarpeen mukaan.</span><span class="sxs-lookup"><span data-stu-id="344d9-114">A *Boolean* value that specifies whether elements of sublists should be generated on demand.</span></span>

## <a name="return-values"></a><span data-ttu-id="344d9-115">Palautusarvot</span><span class="sxs-lookup"><span data-stu-id="344d9-115">Return values</span></span>

<span data-ttu-id="344d9-116">*Tietueluettelo*</span><span class="sxs-lookup"><span data-stu-id="344d9-116">*Record list*</span></span>

<span data-ttu-id="344d9-117">Tuloksena oleva tietueluettelo.</span><span class="sxs-lookup"><span data-stu-id="344d9-117">The resulting list of records.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="344d9-118">Käyttöhuomautukset</span><span class="sxs-lookup"><span data-stu-id="344d9-118">Usage notes</span></span>

<span data-ttu-id="344d9-119">Palautettu eräluettelo, joka sisältää seuraavat elementit:</span><span class="sxs-lookup"><span data-stu-id="344d9-119">The list of batches that is returned contains the following elements:</span></span>

 - <span data-ttu-id="344d9-120">**Arvo:** *Luettelo*</span><span class="sxs-lookup"><span data-stu-id="344d9-120">**Value:** *List*</span></span>

    <span data-ttu-id="344d9-121">Nykyiseen erään kuuluvien tietueiden luettelo.</span><span class="sxs-lookup"><span data-stu-id="344d9-121">The list of records that belong to the current batch.</span></span>

- <span data-ttu-id="344d9-122">**BatchNumber:** *Kokonaisluku*</span><span class="sxs-lookup"><span data-stu-id="344d9-122">**BatchNumber:** *Integer*</span></span>

    <span data-ttu-id="344d9-123">Palautetun luettelon nykyisen erän numero.</span><span class="sxs-lookup"><span data-stu-id="344d9-123">The number of the current batch in the returned list.</span></span>

<span data-ttu-id="344d9-124">Kun tarvittaessa lukemisen merkinnän arvoksi määritetään **Tosi**, järjestelmä luo pyydettäessä aliluetteloita, jotka mahdollistavat muistin kulutuksen vähentämisen, mutta jotka voivat aiheuttaa suorituskyvyn heikentymisen, jos elementtejä ei käytetä peräkkäin.</span><span class="sxs-lookup"><span data-stu-id="344d9-124">When the on-demand reading flag is set to **True**, sublists are generated upon request which allows for a reduction in memory consumption but may cause performance degradation if elements aren't used sequentially.</span></span>

## <a name="example"></a><span data-ttu-id="344d9-125">Esimerkki</span><span class="sxs-lookup"><span data-stu-id="344d9-125">Example</span></span>

<span data-ttu-id="344d9-126">Seuraavassa kuvassa **Rivit**-tietolähde luodaan tietueluettelo, jossa on kolme tietuetta.</span><span class="sxs-lookup"><span data-stu-id="344d9-126">In the following illustration, a **Lines** data source is created as a record list that has three records.</span></span> <span data-ttu-id="344d9-127">Tämä luettelo on jaettu eriin, joista kussakin on enintään kaksi tietuetta.</span><span class="sxs-lookup"><span data-stu-id="344d9-127">This list is divided into batches, each of which contains up to two records.</span></span>

<a href="./media/picture-splitlist-datasource.jpg"><img src="./media/picture-splitlist-datasource.jpg" alt="Data source that is divided into batches" class="alignnone wp-image-290681 size-full" width="397" height="136" /></a>

<span data-ttu-id="344d9-128">Seuraavassa kuvassa on suunnitellun muodon asettelu.</span><span class="sxs-lookup"><span data-stu-id="344d9-128">The following illustration shows the designed format layout.</span></span> <span data-ttu-id="344d9-129">Tässä muodon asettelussa sidonnat **Rivit**-tietolähde luodaan muodostamaan tulos XML-muodossa.</span><span class="sxs-lookup"><span data-stu-id="344d9-129">In this format layout, bindings to the **Lines** data source are created to generate output in XML format.</span></span> <span data-ttu-id="344d9-130">Tämä tulos esittää kunkin erän erilliset solmut ja sen tietueet.</span><span class="sxs-lookup"><span data-stu-id="344d9-130">This output presents individual nodes for each batch and the records in it.</span></span>

<a href="./media/picture-splitlist-format.jpg"><img src="./media/picture-splitlist-format.jpg" alt="Format layout that has bindings to a data source" class="alignnone wp-image-290691 size-full" width="374" height="161" /></a>

<span data-ttu-id="344d9-131">Seuraavassa kuvassa on tulos, kun suunniteltu muoto suoritetaan.</span><span class="sxs-lookup"><span data-stu-id="344d9-131">The following illustration shows the result when the designed format is run.</span></span>

<a href="./media/picture-splitlist-result.jpg"><img src="./media/picture-splitlist-result.jpg" alt="Result of running the format" class="alignnone wp-image-290701 size-full" width="358" height="191" /></a>

## <a name="additional-resources"></a><span data-ttu-id="344d9-132">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="344d9-132">Additional resources</span></span>

[<span data-ttu-id="344d9-133">Luettelotoiminnot</span><span class="sxs-lookup"><span data-stu-id="344d9-133">List functions</span></span>](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
