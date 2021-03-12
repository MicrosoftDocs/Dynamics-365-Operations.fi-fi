---
title: Kustannuslaskentataso
description: Tässä aiheessa kuvataan tuoterakennetaso, jonka nimi on kustannuslaskennassa käytettävä taso. Tämä tuoterakennetaso ei sisällä tuotanto- ja erätilauksia laskelmista.
author: AndersGirke
manager: tfehr
ms.date: 04/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2020-04-23
ms.dyn365.ops.version: Release 10.0.12
ms.openlocfilehash: 42088d8c005cf3fc04e768f1b8e8c8ca0b8c6993
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/15/2021
ms.locfileid: "4967723"
---
# <a name="cost-calculation-level"></a><span data-ttu-id="f067a-104">Kustannuslaskentataso</span><span class="sxs-lookup"><span data-stu-id="f067a-104">Cost calculation level</span></span>

<span data-ttu-id="f067a-105">Tuoterakennetaso, jonka nimi on **Kustannuslaskentataso**, jättää tuotantotilaukset ja erätilaukset pois laskelmista.</span><span class="sxs-lookup"><span data-stu-id="f067a-105">The bill of materials (BOM) level that is named **Cost calculation level** excludes production orders and batch orders from its calculations.</span></span> <span data-ttu-id="f067a-106">Järjestelmä käyttää tätä tasoa, kun se suorittaa kustannuslaskelmia kustannuslaskelmaversioissa.</span><span class="sxs-lookup"><span data-stu-id="f067a-106">The system uses this level when it runs cost calculations in costing versions.</span></span> <span data-ttu-id="f067a-107">Järjestelmä käyttää sen sijaan **Kustannuslaskentataso**-tuoterakennetasoa prosesseissa, kuten uudelleenlaskennassa ja varaston sulkemisessa.</span><span class="sxs-lookup"><span data-stu-id="f067a-107">In processes such as recalculation and inventory close, the system uses the **Costing level** BOM level instead.</span></span>

<span data-ttu-id="f067a-108">Seuraavassa yksinkertaisessa skenaariossa näkyvät **kustannuslaskentatason** tuoterakennetason ja **Kustannustason** tuoterakennetason erot.</span><span class="sxs-lookup"><span data-stu-id="f067a-108">The following simple scenario shows the differences between the **Cost calculation level** BOM level and the **Costing level** BOM level.</span></span>

<span data-ttu-id="f067a-109">Sinulla on kolme tuotetta: A, B ja C. Tuote C on tuotteen B komponentti, ja tuote B on tuotteen A komponentti.</span><span class="sxs-lookup"><span data-stu-id="f067a-109">You have three products: A, B, and C. Product C is the component of product B, and product B is the component of product A.</span></span>

- <span data-ttu-id="f067a-110">**Kustannustaso** määrittää seuraavat tuoterakennetasot:</span><span class="sxs-lookup"><span data-stu-id="f067a-110">**Costing level** assigns the following BOM levels:</span></span>

    - <span data-ttu-id="f067a-111">**Tuote A:** 0</span><span class="sxs-lookup"><span data-stu-id="f067a-111">**Product A:** 0</span></span>
    - <span data-ttu-id="f067a-112">**Tuote B:** 1</span><span class="sxs-lookup"><span data-stu-id="f067a-112">**Product B:** 1</span></span>
    - <span data-ttu-id="f067a-113">**Tuote C:** 2</span><span class="sxs-lookup"><span data-stu-id="f067a-113">**Product C:** 2</span></span>

- <span data-ttu-id="f067a-114">**Kustannuslaskentataso** määrittää seuraavat tuoterakennetasot:</span><span class="sxs-lookup"><span data-stu-id="f067a-114">**Cost calculation level** assigns the following BOM levels:</span></span>

    - <span data-ttu-id="f067a-115">**Tuote A:** 0</span><span class="sxs-lookup"><span data-stu-id="f067a-115">**Product A:** 0</span></span>
    - <span data-ttu-id="f067a-116">**Tuote B:** 1</span><span class="sxs-lookup"><span data-stu-id="f067a-116">**Product B:** 1</span></span>
    - <span data-ttu-id="f067a-117">**Tuote C:** 2</span><span class="sxs-lookup"><span data-stu-id="f067a-117">**Product C:** 2</span></span>

<span data-ttu-id="f067a-118">Tuotteen C tuotantotilaus luodaan ja tuote A lisätään tuotantotilauksen tuoterakenteeseen.</span><span class="sxs-lookup"><span data-stu-id="f067a-118">A production order for product C is then created, and product A is added to the production order BOM.</span></span> <span data-ttu-id="f067a-119">Kun tilaus on arvioitu, tuoterakennetasot päivitetään seuraavalla tavalla:</span><span class="sxs-lookup"><span data-stu-id="f067a-119">After the order is estimated, BOM levels are updated in the following way:</span></span>

- <span data-ttu-id="f067a-120">**Kustannustaso** määrittää seuraavat tuoterakennetasot:</span><span class="sxs-lookup"><span data-stu-id="f067a-120">**Costing level** assigns the following BOM levels:</span></span>

    - <span data-ttu-id="f067a-121">**Tuote B:** 1</span><span class="sxs-lookup"><span data-stu-id="f067a-121">**Product B:** 1</span></span>
    - <span data-ttu-id="f067a-122">**Tuote C:** 2</span><span class="sxs-lookup"><span data-stu-id="f067a-122">**Product C:** 2</span></span>
    - <span data-ttu-id="f067a-123">**Tuote A:** 3</span><span class="sxs-lookup"><span data-stu-id="f067a-123">**Product A:** 3</span></span>

- <span data-ttu-id="f067a-124">**Kustannuslaskentataso** määrittää seuraavat tuoterakennetasot:</span><span class="sxs-lookup"><span data-stu-id="f067a-124">**Cost calculation level** assigns the following BOM levels:</span></span>

    - <span data-ttu-id="f067a-125">**Tuote A:** 0</span><span class="sxs-lookup"><span data-stu-id="f067a-125">**Product A:** 0</span></span>
    - <span data-ttu-id="f067a-126">**Tuote B:** 1</span><span class="sxs-lookup"><span data-stu-id="f067a-126">**Product B:** 1</span></span>
    - <span data-ttu-id="f067a-127">**Tuote C:** 2</span><span class="sxs-lookup"><span data-stu-id="f067a-127">**Product C:** 2</span></span>

<span data-ttu-id="f067a-128">Tämä toiminto varmistaa, että tuotantotilauksen tuoterakenteiden muutokset eivät vaikuta seuraaviin kustannuslaskelmiin.</span><span class="sxs-lookup"><span data-stu-id="f067a-128">This behavior ensures that changes to production order BOMs don't affect subsequent cost calculations.</span></span>
