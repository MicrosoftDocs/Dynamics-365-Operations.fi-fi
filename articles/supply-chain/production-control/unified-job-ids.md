---
title: Työtunnusten yhdistetty numerosarja
description: Tämä ominaisuus tarjoaa yhden yhdistetyn numerosarjan, joka luo työn tunnukset tuotannon hallinnassa, valmistuksen suorittamisen sekä aika- ja läsnäolomoduulissa.
author: johanhoffmann
ms.date: 03/25/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2021-03-05
ms.dyn365.ops.version: 10.0.16
ms.openlocfilehash: 00212803c46d898a39eafbc5c62016eb829535e2
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/01/2021
ms.locfileid: "5824939"
---
# <a name="unified-number-sequence-for-job-ids"></a><span data-ttu-id="77b7f-103">Työtunnusten yhdistetty numerosarja</span><span class="sxs-lookup"><span data-stu-id="77b7f-103">Unified number sequence for job IDs</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="77b7f-104">Tämä ominaisuus tarjoaa yhden yhdistetyn numerosarjan, joka luo työn tunnukset tuotannon hallinnassa, valmistuksen suorittamisen sekä aika- ja läsnäolomoduulissa.</span><span class="sxs-lookup"><span data-stu-id="77b7f-104">This feature provides a single, unified number sequence that generates job IDs for the Production control, Manufacturing execution, and Time and attendance modules.</span></span> <span data-ttu-id="77b7f-105">Aiemmin voit valita kullekin moduulille eri numerosarjan, mikä saattaa aiheuttaa ristiriidan työtunnuksissa, jos vähintään kaksi näistä sarjoista käyttää samaa muotoa.</span><span class="sxs-lookup"><span data-stu-id="77b7f-105">Previously, you were able to choose a different number sequence for each of these modules, which could result in conflicting job IDs if two or more of these sequences used an identical format.</span></span> <span data-ttu-id="77b7f-106">Tällainen ristiriita voi aiheuttaa tietojen vaurioitumista.</span><span class="sxs-lookup"><span data-stu-id="77b7f-106">Such a conflict can cause data corruption.</span></span>

## <a name="turn-on-this-feature-for-your-system"></a><span data-ttu-id="77b7f-107">Tämän ominaisuuden ottaminen käyttöön järjestelmällesi</span><span class="sxs-lookup"><span data-stu-id="77b7f-107">Turn on this feature for your system</span></span>

<span data-ttu-id="77b7f-108">Jos järjestelmäsi ei vielä sisällä tässä aiheessa kuvattua ominaisuutta, avaa [Ominaisuuksien hallinta](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) ja ota *Työtunnusten yhdistetty numerosarja* -ominaisuus käyttöön.</span><span class="sxs-lookup"><span data-stu-id="77b7f-108">If your system doesn't already include the feature described in this topic, go to [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) and turn on the *Unified number sequence for job IDs* feature.</span></span>

## <a name="set-up-the-unified-number-sequence-for-job-ids"></a><span data-ttu-id="77b7f-109">Määritä työtunnusten yhdistetty numerosarja</span><span class="sxs-lookup"><span data-stu-id="77b7f-109">Set up the unified number sequence for job IDs</span></span>

<span data-ttu-id="77b7f-110">Kun tämä ominaisuus on käytössä, tuotannonohjauksen, valmistuksen suorittamisen ja aika- ja läsnäolomoduulien parametrisivuilla olevat **Työtunnus**- numerosarjan asetukset vanhentuvat ja uusi **Yhdistetty työtunnus** -kenttä lisätään.</span><span class="sxs-lookup"><span data-stu-id="77b7f-110">After enabling this feature, the existing **Job identification** number-sequence settings located on the parameters pages for the Production control, Manufacturing execution, and Time and attendance modules will be deprecated and a new **Unified job ID** field will be added.</span></span> <span data-ttu-id="77b7f-111">Kaikki kolme moduulia jakavat **Yhdistetty työtunnus** -arvon, mikä varmistaa, että kaikissa moduuleissa viitataan samaan numerosarjaan.</span><span class="sxs-lookup"><span data-stu-id="77b7f-111">The **Unified job ID** value is shared by all three modules, thus ensuring that all modules reference the same number sequence.</span></span> <span data-ttu-id="77b7f-112">Tämän vuoksi työtunnukset ovat yksilöllisiä kaikissa kolmessa moduulissa, eikä ristiriitoja tule koskaan.</span><span class="sxs-lookup"><span data-stu-id="77b7f-112">Job IDs will therefore be unique across all three modules and a conflict will never occur.</span></span>

<span data-ttu-id="77b7f-113">Määritä työtunnusten yhdistetty numerosarja seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="77b7f-113">To set up the unified number sequence for job IDs:</span></span>

1. <span data-ttu-id="77b7f-114">Ota toiminto käyttöön edellisessä osassa kuvatulla tavalla.</span><span class="sxs-lookup"><span data-stu-id="77b7f-114">Turn on the feature as described in the previous section.</span></span>
1. <span data-ttu-id="77b7f-115">Määritä yhdistettyjä työtunnuksia varten käytettävä numerosarja tai luo uusi numerosarja.</span><span class="sxs-lookup"><span data-stu-id="77b7f-115">Either identify the number sequence you want to use for your unified job IDs, or create a new one.</span></span> <span data-ttu-id="77b7f-116">Lisätietoja on kohdassa [Numerosarjojen yleiskatsaus](../../fin-ops-core/fin-ops/organization-administration/number-sequence-overview.md).</span><span class="sxs-lookup"><span data-stu-id="77b7f-116">For more information, see [Number sequences overview](../../fin-ops-core/fin-ops/organization-administration/number-sequence-overview.md).</span></span>
1. <span data-ttu-id="77b7f-117">Siirry **Tuotannonhallinnan parametrit**-, **Tuotannon suoritusparametrit**- tai **Aika ja läsnäolo -parametrit** -sivulle.</span><span class="sxs-lookup"><span data-stu-id="77b7f-117">Go to the **Production control parameters**, **Manufacturing execution parameters**, or **Time and attendance parameters** page.</span></span> <span data-ttu-id="77b7f-118">Valinnalla ei ole merkitystä, sillä kun teet tämän asetuksen jollain sivulla, kaikki muut sivut päivittyvät automaattisesti.</span><span class="sxs-lookup"><span data-stu-id="77b7f-118">It doesn't matter which one you choose because when you make this setting on any of those pages, all of the other pages will update automatically.</span></span>
1. <span data-ttu-id="77b7f-119">Avaa valittujen parametrien sivun **Numerosarjat**-välilehti.</span><span class="sxs-lookup"><span data-stu-id="77b7f-119">Open the **Number sequences** tab on your selected parameters page.</span></span>
1. <span data-ttu-id="77b7f-120">Määritä aiemmin määritetty **Numerosarjakoodi** ruudukon **Yhdistetty työtunnus** -riville.</span><span class="sxs-lookup"><span data-stu-id="77b7f-120">Assign the **Number sequence code** that you identified previously to the **Unified job IDs** row of the grid.</span></span>
