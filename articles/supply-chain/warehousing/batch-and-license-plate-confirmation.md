---
title: Erän ja rekisterikilven tiedot
description: Tässä ohjeaiheessa kerrotaan erän ja rekisterikilven vahvistuksen määrittämisestä ja käyttämisestä mobiililaitteessa.
author: Mirzaab
ms.date: 11/11/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSRFAutoConfirm
audience: Application User
ms.reviewer: kamaybac
ms.custom: 269384
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c588e6ed11d275b75133e2824f3d385048050426
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/01/2021
ms.locfileid: "5837534"
---
# <a name="batch-and-license-plate-confirmation"></a><span data-ttu-id="7e733-103">Erän ja rekisterikilven tiedot</span><span class="sxs-lookup"><span data-stu-id="7e733-103">Batch and license plate confirmation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7e733-104">Erän vahvistuksen avulla mobiililaitteessa voidaan vahvistaa, että kerättävä erä on oikea.</span><span class="sxs-lookup"><span data-stu-id="7e733-104">Batch confirmation allows you to confirm that the correct batch is being picked from the mobile device.</span></span> <span data-ttu-id="7e733-105">Kun vain *erä-yllä\[sijainti\]* -nimikkeiden erän keräilytyö tehdään ensimmäisen kerran, erä-yllä ilmaisee, että erä on hakuhierarkiassa sijaintia korkeammalla, sinun on vahvistettava, että kerättävä erä vastaa työrivillä olevaa erää.</span><span class="sxs-lookup"><span data-stu-id="7e733-105">On the initial pick of work for *Batch-above\[location\]* items only, where batch-above indicates that batch is placed higher than location in the search hierarchy, you must verify that the batch that is picked matches the batch on the work line.</span></span>

<span data-ttu-id="7e733-106">Rekisterikilven vahvistuksen avulla mobiililaitteessa voidaan vahvistaa, että kerättävä rekisterikilpi on oikea.</span><span class="sxs-lookup"><span data-stu-id="7e733-106">License plate confirmation allows you to confirm that the correct license plate is being picked from the mobile device.</span></span> <span data-ttu-id="7e733-107">Kun työ kerätään väliaikaisesta sijainnista, sinun on varmistettava, että kerättävä rekisterikilpi vastaa työhön liitettyä rekisterikilpeä.</span><span class="sxs-lookup"><span data-stu-id="7e733-107">When picking work from a stage location, you must verify that the license plate that is picked matches the license plate that is associated with the work.</span></span> <span data-ttu-id="7e733-108">Jos työ aloitetaan rekisterikilven skannauksella, tämä vahvistusvaihe ohitetaan.</span><span class="sxs-lookup"><span data-stu-id="7e733-108">If the work is started by scanning a license plate, this confirmation step will be skipped.</span></span>

## <a name="where-it-applies"></a><span data-ttu-id="7e733-109">Käyttö</span><span class="sxs-lookup"><span data-stu-id="7e733-109">Where it applies</span></span>

<span data-ttu-id="7e733-110">Vahvistusta käytetään seuraavissa skenaarioissa:</span><span class="sxs-lookup"><span data-stu-id="7e733-110">Confirmation applies in the following scenarios:</span></span>

- <span data-ttu-id="7e733-111">Erän vahvistusta käytetään yläpuolella olevan nimike-erän ensimmäisissä keräilytöissä.</span><span class="sxs-lookup"><span data-stu-id="7e733-111">Batch confirmation applies to the initial picks of work for batch above-items.</span></span>
- <span data-ttu-id="7e733-112">Rekisterikilven vahvistusta käytetään väliaikaisista sijainneista tehtävissä keräilyissä.</span><span class="sxs-lookup"><span data-stu-id="7e733-112">License plate confirmation applies to picks from stage locations.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="7e733-113">Täydennystä ei tueta rekisterikilven vahvistuksessa.</span><span class="sxs-lookup"><span data-stu-id="7e733-113">Replenishment is not supported for license plate confirmation.</span></span> <span data-ttu-id="7e733-114">Täydennystyötä suoritettaessa ei luoda rekisterikilven vahvistusvaihetta.</span><span class="sxs-lookup"><span data-stu-id="7e733-114">When executing replenishment work, no license plate confirmation step is created.</span></span>

## <a name="set-up-batch-and-license-plate-confirmation"></a><span data-ttu-id="7e733-115">Erän ja rekisterikilven tietojen määrittäminen</span><span class="sxs-lookup"><span data-stu-id="7e733-115">Set up batch and license plate confirmation</span></span>

<span data-ttu-id="7e733-116">Voit määrittää erän ja rekisterikilven tiedot mobiililaitteen valikkovaihtoehdoilla.</span><span class="sxs-lookup"><span data-stu-id="7e733-116">You can configure batch and license plate confirmation from the mobile device menu items.</span></span>

1. <span data-ttu-id="7e733-117">Anna työn vahvistusasetukset mobiililaitteen valikkovaihtoehdoissa.</span><span class="sxs-lookup"><span data-stu-id="7e733-117">From the mobile device menu items, enter the work confirmation setup.</span></span>  
1. <span data-ttu-id="7e733-118">Valitse jo erän tai rekisterikilven vahvistusvaihtoehto.</span><span class="sxs-lookup"><span data-stu-id="7e733-118">Select the option for either batch or license plate confirmation.</span></span> <span data-ttu-id="7e733-119">Kumpikin vaihtoehto on valittavissa keräilytyötyypeissä, joissa automaattista vahvistusta ei ole otettu käyttöön.</span><span class="sxs-lookup"><span data-stu-id="7e733-119">Both options are available for work type picks that do not have automatic confirmation enabled.</span></span>  


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
