---
title: Kustannuslaskentataso
description: Tässä aiheessa kuvataan tuoterakennetaso, jonka nimi on kustannuslaskennassa käytettävä taso. Tämä tuoterakennetaso ei sisällä tuotanto- ja erätilauksia laskelmista.
author: AndersGirke
ms.date: 04/23/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2020-04-23
ms.dyn365.ops.version: Release 10.0.12
ms.openlocfilehash: f7cde239107528a6bc2aeb0e424d024d4f3fb2a6
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/01/2021
ms.locfileid: "5839484"
---
# <a name="cost-calculation-level"></a><span data-ttu-id="42071-104">Kustannuslaskentataso</span><span class="sxs-lookup"><span data-stu-id="42071-104">Cost calculation level</span></span>

<span data-ttu-id="42071-105">Tuoterakennetaso, jonka nimi on **Kustannuslaskentataso**, jättää tuotantotilaukset ja erätilaukset pois laskelmista.</span><span class="sxs-lookup"><span data-stu-id="42071-105">The bill of materials (BOM) level that is named **Cost calculation level** excludes production orders and batch orders from its calculations.</span></span> <span data-ttu-id="42071-106">Järjestelmä käyttää tätä tasoa, kun se suorittaa kustannuslaskelmia kustannuslaskelmaversioissa.</span><span class="sxs-lookup"><span data-stu-id="42071-106">The system uses this level when it runs cost calculations in costing versions.</span></span> <span data-ttu-id="42071-107">Järjestelmä käyttää sen sijaan **Kustannuslaskentataso**-tuoterakennetasoa prosesseissa, kuten uudelleenlaskennassa ja varaston sulkemisessa.</span><span class="sxs-lookup"><span data-stu-id="42071-107">In processes such as recalculation and inventory close, the system uses the **Costing level** BOM level instead.</span></span>

<span data-ttu-id="42071-108">Seuraavassa yksinkertaisessa skenaariossa näkyvät **kustannuslaskentatason** tuoterakennetason ja **Kustannustason** tuoterakennetason erot.</span><span class="sxs-lookup"><span data-stu-id="42071-108">The following simple scenario shows the differences between the **Cost calculation level** BOM level and the **Costing level** BOM level.</span></span>

<span data-ttu-id="42071-109">Sinulla on kolme tuotetta: A, B ja C. Tuote C on tuotteen B komponentti, ja tuote B on tuotteen A komponentti.</span><span class="sxs-lookup"><span data-stu-id="42071-109">You have three products: A, B, and C. Product C is the component of product B, and product B is the component of product A.</span></span>

- <span data-ttu-id="42071-110">**Kustannustaso** määrittää seuraavat tuoterakennetasot:</span><span class="sxs-lookup"><span data-stu-id="42071-110">**Costing level** assigns the following BOM levels:</span></span>

    - <span data-ttu-id="42071-111">**Tuote A:** 0</span><span class="sxs-lookup"><span data-stu-id="42071-111">**Product A:** 0</span></span>
    - <span data-ttu-id="42071-112">**Tuote B:** 1</span><span class="sxs-lookup"><span data-stu-id="42071-112">**Product B:** 1</span></span>
    - <span data-ttu-id="42071-113">**Tuote C:** 2</span><span class="sxs-lookup"><span data-stu-id="42071-113">**Product C:** 2</span></span>

- <span data-ttu-id="42071-114">**Kustannuslaskentataso** määrittää seuraavat tuoterakennetasot:</span><span class="sxs-lookup"><span data-stu-id="42071-114">**Cost calculation level** assigns the following BOM levels:</span></span>

    - <span data-ttu-id="42071-115">**Tuote A:** 0</span><span class="sxs-lookup"><span data-stu-id="42071-115">**Product A:** 0</span></span>
    - <span data-ttu-id="42071-116">**Tuote B:** 1</span><span class="sxs-lookup"><span data-stu-id="42071-116">**Product B:** 1</span></span>
    - <span data-ttu-id="42071-117">**Tuote C:** 2</span><span class="sxs-lookup"><span data-stu-id="42071-117">**Product C:** 2</span></span>

<span data-ttu-id="42071-118">Tuotteen C tuotantotilaus luodaan ja tuote A lisätään tuotantotilauksen tuoterakenteeseen.</span><span class="sxs-lookup"><span data-stu-id="42071-118">A production order for product C is then created, and product A is added to the production order BOM.</span></span> <span data-ttu-id="42071-119">Kun tilaus on arvioitu, tuoterakennetasot päivitetään seuraavalla tavalla:</span><span class="sxs-lookup"><span data-stu-id="42071-119">After the order is estimated, BOM levels are updated in the following way:</span></span>

- <span data-ttu-id="42071-120">**Kustannustaso** määrittää seuraavat tuoterakennetasot:</span><span class="sxs-lookup"><span data-stu-id="42071-120">**Costing level** assigns the following BOM levels:</span></span>

    - <span data-ttu-id="42071-121">**Tuote B:** 1</span><span class="sxs-lookup"><span data-stu-id="42071-121">**Product B:** 1</span></span>
    - <span data-ttu-id="42071-122">**Tuote C:** 2</span><span class="sxs-lookup"><span data-stu-id="42071-122">**Product C:** 2</span></span>
    - <span data-ttu-id="42071-123">**Tuote A:** 3</span><span class="sxs-lookup"><span data-stu-id="42071-123">**Product A:** 3</span></span>

- <span data-ttu-id="42071-124">**Kustannuslaskentataso** määrittää seuraavat tuoterakennetasot:</span><span class="sxs-lookup"><span data-stu-id="42071-124">**Cost calculation level** assigns the following BOM levels:</span></span>

    - <span data-ttu-id="42071-125">**Tuote A:** 0</span><span class="sxs-lookup"><span data-stu-id="42071-125">**Product A:** 0</span></span>
    - <span data-ttu-id="42071-126">**Tuote B:** 1</span><span class="sxs-lookup"><span data-stu-id="42071-126">**Product B:** 1</span></span>
    - <span data-ttu-id="42071-127">**Tuote C:** 2</span><span class="sxs-lookup"><span data-stu-id="42071-127">**Product C:** 2</span></span>

<span data-ttu-id="42071-128">Tämä toiminto varmistaa, että tuotantotilauksen tuoterakenteiden muutokset eivät vaikuta seuraaviin kustannuslaskelmiin.</span><span class="sxs-lookup"><span data-stu-id="42071-128">This behavior ensures that changes to production order BOMs don't affect subsequent cost calculations.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]