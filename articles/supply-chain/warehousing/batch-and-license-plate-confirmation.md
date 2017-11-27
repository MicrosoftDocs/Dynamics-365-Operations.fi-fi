---
title: "Erän ja rekisterikilven tiedot"
description: "Tässä ohjeaiheessa kerrotaan erän ja rekisterikilven vahvistuksen määrittämisestä ja käyttämisestä mobiililaitteessa."
author: Mirzaab
manager: AnnBe
ms.date: 05/26/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, Operations
ms.custom: 269384
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 0444caa0f1cc176153c322b8619db65bd377ddd0
ms.contentlocale: fi-fi
ms.lasthandoff: 11/03/2017

---

# <a name="batch-and-license-plate-confirmation"></a><span data-ttu-id="b4b1b-103">Erän ja rekisterikilven tiedot</span><span class="sxs-lookup"><span data-stu-id="b4b1b-103">Batch and license plate confirmation</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="b4b1b-104">Erän vahvistuksen avulla mobiililaitteessa voidaan vahvistaa, että kerättävä erä on oikea.</span><span class="sxs-lookup"><span data-stu-id="b4b1b-104">Batch confirmation allows you to confirm that the correct batch is being picked from the mobile device.</span></span> <span data-ttu-id="b4b1b-105">Kun vain yläpuolella olevien nimikkeiden erän keräilytyö tehdään ensimmäisen kerran, yläpuolella oleva erä ilmaiseen eräalueet, jotka ovat hakuhierarkiassa sijaintia korkeammalla, sinun on vahvistettava, että kerättävä erä vastaa työrivillä olevaa erää.</span><span class="sxs-lookup"><span data-stu-id="b4b1b-105">On the initial pick of work for batch above-items only, where batch above indicates that batch ranges higher than location in the search hierarchy, you must verify that the batch that is picked matches the batch on the work line.</span></span> 

<span data-ttu-id="b4b1b-106">Rekisterikilven vahvistuksen avulla mobiililaitteessa voidaan vahvistaa, että kerättävä rekisterikilpi on oikea.</span><span class="sxs-lookup"><span data-stu-id="b4b1b-106">License plate confirmation allows you to confirm that the correct license plate is being picked from the mobile device.</span></span> <span data-ttu-id="b4b1b-107">Kun työ kerätään väliaikaisesta sijainnista, sinun on varmistettava, että kerättävä rekisterikilpi vastaa työhön liitettyä rekisterikilpeä.</span><span class="sxs-lookup"><span data-stu-id="b4b1b-107">When picking work from a stage location, you must verify that the license plate that is picked matches the license plate that is associated with the work.</span></span> <span data-ttu-id="b4b1b-108">Jos työ aloitetaan rekisterikilven skannauksella, tämä vahvistusvaihe ohitetaan.</span><span class="sxs-lookup"><span data-stu-id="b4b1b-108">If the work is started by scanning a license plate, this confirmation step will be skipped.</span></span>

## <a name="where-it-applies"></a><span data-ttu-id="b4b1b-109">Käyttö</span><span class="sxs-lookup"><span data-stu-id="b4b1b-109">Where it applies</span></span>
<span data-ttu-id="b4b1b-110">Vahvistusta käytetään seuraavissa skenaarioissa:</span><span class="sxs-lookup"><span data-stu-id="b4b1b-110">Confirmation applies in the following scenarios:</span></span>

- <span data-ttu-id="b4b1b-111">Erän vahvistusta käytetään yläpuolella olevan nimike-erän ensimmäisissä keräilytöissä.</span><span class="sxs-lookup"><span data-stu-id="b4b1b-111">Batch confirmation applies to the initial picks of work for batch above-items.</span></span>
- <span data-ttu-id="b4b1b-112">Rekisterikilven vahvistusta käytetään väliaikaisista sijainneista tehtävissä keräilyissä.</span><span class="sxs-lookup"><span data-stu-id="b4b1b-112">License plate confirmation applies to picks from stage locations.</span></span>

## <a name="set-up-batch-and-license-plate-confirmation"></a><span data-ttu-id="b4b1b-113">Erän ja rekisterikilven tietojen määrittäminen</span><span class="sxs-lookup"><span data-stu-id="b4b1b-113">Set up batch and license plate confirmation</span></span>
<span data-ttu-id="b4b1b-114">Voit määrittää erän ja rekisterikilven tiedot mobiililaitteen valikkovaihtoehdoilla.</span><span class="sxs-lookup"><span data-stu-id="b4b1b-114">You can configure batch and license plate confirmation from the mobile device menu items.</span></span>  
1.  <span data-ttu-id="b4b1b-115">Anna työn vahvistusasetukset mobiililaitteen valikkovaihtoehdoissa.</span><span class="sxs-lookup"><span data-stu-id="b4b1b-115">From the mobile device menu items, enter the work confirmation setup.</span></span>  
2.  <span data-ttu-id="b4b1b-116">Valitse jo erän tai rekisterikilven vahvistusvaihtoehto.</span><span class="sxs-lookup"><span data-stu-id="b4b1b-116">Select the option for either batch or license plate confirmation.</span></span> <span data-ttu-id="b4b1b-117">Kumpikin vaihtoehto on valittavissa keräilytyötyypeissä, joissa automaattista vahvistusta ei ole otettu käyttöön.</span><span class="sxs-lookup"><span data-stu-id="b4b1b-117">Both options are available for work type picks that do not have automatic confirmation enabled.</span></span>  

