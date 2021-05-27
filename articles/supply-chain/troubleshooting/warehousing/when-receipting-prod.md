---
title: Yhdelle kuitille tulostetaan vain yksi etiketti useille työotsikoille
description: Yhdelle kuitille tulostetaan vain yksi etiketti useille työotsikoille.
author: perlynne
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: WHSLicensePlateLabel
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 8e11dc918eb3c9085018d15b43819522cc8bebe3
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026472"
---
# <a name="only-one-label-is-printed-for-multiple-work-headers-on-a-single-receipt"></a><span data-ttu-id="6f98d-103">Yhdelle kuitille tulostetaan vain yksi etiketti useille työotsikoille</span><span class="sxs-lookup"><span data-stu-id="6f98d-103">Only one label is printed for multiple work headers on a single receipt</span></span>

<span data-ttu-id="6f98d-104">Tietopankin numero: 4614667</span><span class="sxs-lookup"><span data-stu-id="6f98d-104">KB number: 4614667</span></span>

## <a name="symptoms"></a><span data-ttu-id="6f98d-105">Oireet</span><span class="sxs-lookup"><span data-stu-id="6f98d-105">Symptoms</span></span>

<span data-ttu-id="6f98d-106">Samalle kohderekisterikilvelle luodaan useita työotsikkoja, jotka ovat osa yhtä varastosovelluksen vastaanottotapahtumaa.</span><span class="sxs-lookup"><span data-stu-id="6f98d-106">Multiple work headers are created for the same target license plate as part of a single warehouse app receiving event.</span></span> <span data-ttu-id="6f98d-107">Kun tuote vastaanotetaan, tulostetaan kuitenkin vain yksi rekisterikilven etiketti.</span><span class="sxs-lookup"><span data-stu-id="6f98d-107">However, only one license plate label is printed when the product is received.</span></span>

## <a name="resolution"></a><span data-ttu-id="6f98d-108">Ratkaisu</span><span class="sxs-lookup"><span data-stu-id="6f98d-108">Resolution</span></span>

<span data-ttu-id="6f98d-109">Järjestelmä käyttäytyy suunnitellulla tavalla.</span><span class="sxs-lookup"><span data-stu-id="6f98d-109">The system is behaving as designed.</span></span>

<span data-ttu-id="6f98d-110">Nykyisessä suunnittelussa luodaan aina vain yksi rekisterikilven etiketti, riippumatta siitä, kuinka monta työotsikon ja työrivin yhdistelmää on olemassa.</span><span class="sxs-lookup"><span data-stu-id="6f98d-110">In the current design, a single license plate label is always generated, regardless of the number of work header and work line combinations that exist.</span></span> <span data-ttu-id="6f98d-111">Luotu otsikko sisältää vain yhden yhdistelmän tiedot.</span><span class="sxs-lookup"><span data-stu-id="6f98d-111">The generated label includes the information for only one combination.</span></span>

<span data-ttu-id="6f98d-112">Voit ratkaista tämän ongelman varmistamalla, että työotsikon luonti on aina yhdistetty vain yhteen kohderekisterikilpeen.</span><span class="sxs-lookup"><span data-stu-id="6f98d-112">To work around this issue, make sure that work header creation is always mapped to just one target license plate.</span></span>
