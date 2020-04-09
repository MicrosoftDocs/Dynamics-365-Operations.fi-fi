---
title: Luo tarjouspyyntöjen pisteytystapa
description: Tässä menettelyssä näytetään, miten pisteytysmenetelmä luodaan.
author: mkirknel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchRFQScoringMethod
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e0e1fe2a27998c01012e40d80eacf13aa11f5689
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/18/2020
ms.locfileid: "3147339"
---
# <a name="create-a-scoring-method-for-rfqs"></a><span data-ttu-id="0be91-103">Luo tarjouspyyntöjen pisteytystapa</span><span class="sxs-lookup"><span data-stu-id="0be91-103">Create a scoring method for RFQs</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="0be91-104">Tässä menettelyssä näytetään, miten pisteytysmenetelmä luodaan.</span><span class="sxs-lookup"><span data-stu-id="0be91-104">This procedure shows you how to create a scoring method.</span></span> <span data-ttu-id="0be91-105">Pisteytysmenetelmä on joukko ehtoja, jonka avulla voit verrata tarjouksia, jotka lähetetään vastauksena tarjouspyyntöön.</span><span class="sxs-lookup"><span data-stu-id="0be91-105">A scoring method is a set of criteria that can be used to compare bids that are sent in reply to a request for quotation (RFQ).</span></span> <span data-ttu-id="0be91-106">Voit esimerkiksi haluta arvioida toimittajan aiemman suoritustason perusteella tai arvioida, onko yritys ympäristöystävällinen tai hyvä yhteistyökumppani, tai voit vertailla tarjouksia hinnan perusteella.</span><span class="sxs-lookup"><span data-stu-id="0be91-106">For example, you might want to rate a vendor on past performance, or rate whether the company is environmentally friendly or a good collaborator, or you might want to compare bids based on price.</span></span> <span data-ttu-id="0be91-107">Pisteytysmenetelmän voi liittää pyyntötyyppiin oletusmenetelmäksi määrätyn tyyppisille tarjouspyynnöille.</span><span class="sxs-lookup"><span data-stu-id="0be91-107">The scoring method can be associated with a solicitation type as the default scoring method for RFQs of that type.</span></span> <span data-ttu-id="0be91-108">Yleensä ostopäällikkö tekee nämä tehtävät.</span><span class="sxs-lookup"><span data-stu-id="0be91-108">These tasks would typically be carried out by a purchasing manager.</span></span> <span data-ttu-id="0be91-109">Voit käyttää tätä menettelyä USMF-demoyrityksen tiedoilla tai omilla tiedoillasi.</span><span class="sxs-lookup"><span data-stu-id="0be91-109">You can use this procedure in demo data company USMF or on your own data.</span></span>

1. <span data-ttu-id="0be91-110">Siirry kohtaan Hankinta > Asetukset > Tarjouspyyntö > Pisteytysmenetelmä.</span><span class="sxs-lookup"><span data-stu-id="0be91-110">Go to Procurement and sourcing > Setup > Request for quotation > Scoring method.</span></span>
2. <span data-ttu-id="0be91-111">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="0be91-111">Click New.</span></span>
3. <span data-ttu-id="0be91-112">Kirjoita arvo Nimi-kenttään.</span><span class="sxs-lookup"><span data-stu-id="0be91-112">In the Name field, type a value.</span></span>
4. <span data-ttu-id="0be91-113">Kirjoita arvo Kuvaus-kenttään.</span><span class="sxs-lookup"><span data-stu-id="0be91-113">In the Description field, type a value.</span></span>
5. <span data-ttu-id="0be91-114">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="0be91-114">Click Save.</span></span>
6. <span data-ttu-id="0be91-115">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="0be91-115">Click New.</span></span>
7. <span data-ttu-id="0be91-116">Kirjoita arvo Nimi-kenttään.</span><span class="sxs-lookup"><span data-stu-id="0be91-116">In the Name field, type a value.</span></span>
8. <span data-ttu-id="0be91-117">Kirjoita arvo Kuvaus-kenttään.</span><span class="sxs-lookup"><span data-stu-id="0be91-117">In the Description field, type a value.</span></span>
    * <span data-ttu-id="0be91-118">Kuvaus sekä pisteytysmenetelmän nimi näytetään, kun tarjouspyynnölle valitaan menetelmä.</span><span class="sxs-lookup"><span data-stu-id="0be91-118">This description is shown along with the scoring method name when a scoring method is selected for an RFQ.</span></span>  
9. <span data-ttu-id="0be91-119">Syötä Alue alkaa -kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="0be91-119">In the Range from field, enter a number.</span></span>
    * <span data-ttu-id="0be91-120">Väli rajoittaa, mitä hankinnan ammattilainen voi kirjata pistearvoksi.</span><span class="sxs-lookup"><span data-stu-id="0be91-120">The range limits what the procurement professional can enter as a score.</span></span> <span data-ttu-id="0be91-121">Kun tarjouspyynnöllä on useita pisteytysehtoja, annetut pistearvot lisätään toisiinsa ja summa on käytettävissä tarjousten vertailussa.</span><span class="sxs-lookup"><span data-stu-id="0be91-121">When there are multiple scoring criteria on an RFQ, the scores that have been entered are added to each other and the sum is made available to allow the bids to be compared.</span></span>  
10. <span data-ttu-id="0be91-122">Syötä Alue loppuu -kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="0be91-122">In the Range to field, enter a number.</span></span>
11. <span data-ttu-id="0be91-123">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="0be91-123">Click New.</span></span>
12. <span data-ttu-id="0be91-124">Kirjoita arvo Nimi-kenttään.</span><span class="sxs-lookup"><span data-stu-id="0be91-124">In the Name field, type a value.</span></span>
13. <span data-ttu-id="0be91-125">Kirjoita arvo Kuvaus-kenttään.</span><span class="sxs-lookup"><span data-stu-id="0be91-125">In the Description field, type a value.</span></span>
14. <span data-ttu-id="0be91-126">Syötä Alue alkaa -kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="0be91-126">In the Range from field, enter a number.</span></span>
15. <span data-ttu-id="0be91-127">Syötä Alue loppuu -kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="0be91-127">In the Range to field, enter a number.</span></span>

