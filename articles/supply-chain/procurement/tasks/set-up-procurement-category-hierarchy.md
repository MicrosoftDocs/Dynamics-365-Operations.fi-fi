---
title: Määritä hankintaluokkahierarkia
description: Tässä menettelyssä selvitetään, miten voit luoda uusia solmuja hankintaluokkahierarkiaan ja miten hankintaprosessissa käytettävä hankintaluokka määritetään.
author: mkirknel
manager: AnnBe
ms.date: 06/21/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d7010a1c612b9b3884c675f578657d951da06c38
ms.sourcegitcommit: 25fe679b73663fda6b5b3c32646026d0993a9f00
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/12/2019
ms.locfileid: "1995279"
---
# <a name="set-up-a-procurement-category-hierarchy"></a><span data-ttu-id="7dceb-103">Määritä hankintaluokkahierarkia</span><span class="sxs-lookup"><span data-stu-id="7dceb-103">Set up a procurement category hierarchy</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="7dceb-104">Tässä menettelyssä selvitetään, miten voit luoda uusia solmuja hankintaluokkahierarkiaan ja miten hankintaprosessissa käytettävä hankintaluokka määritetään.</span><span class="sxs-lookup"><span data-stu-id="7dceb-104">This procedure shows you how to create new nodes in a procurement category hierarchy and how to configure a procurement category to be used in a procurement process.</span></span> <span data-ttu-id="7dceb-105">Yleensä ostopäällikkö tekee nämä tehtävät.</span><span class="sxs-lookup"><span data-stu-id="7dceb-105">These tasks would typically be carried out by a Purchasing manager.</span></span> <span data-ttu-id="7dceb-106">Ennen menettelyn aloittamista on oltava Hankita-tyyppinen luokkahierarkia.</span><span class="sxs-lookup"><span data-stu-id="7dceb-106">Before you can start this procedure, there must be a category hierarchy of type Procurement.</span></span> <span data-ttu-id="7dceb-107">Jos käytössä on demotietoyritys, voit suorittaa tämän menettelyn USMF-yrityksessä.</span><span class="sxs-lookup"><span data-stu-id="7dceb-107">If you're using a demo data company, you can run this procedure in the USMF company.</span></span>


## <a name="add-a-new-procurement-category"></a><span data-ttu-id="7dceb-108">Lisää uusi hankintaluokka</span><span class="sxs-lookup"><span data-stu-id="7dceb-108">Add a new procurement category</span></span>
1. <span data-ttu-id="7dceb-109">Siirry kohtaan **Siirtymisruutu > Moduulit > Hankinta > Tavaralähetys > Hankintaluokat**.</span><span class="sxs-lookup"><span data-stu-id="7dceb-109">Go to **Navigation pane > Modules > Procurement and sourcing > Consignment > Procurement categories**.</span></span>
2. <span data-ttu-id="7dceb-110">Valitse toimintoruudusta **Muokkaa luokkahierarkiaa**.</span><span class="sxs-lookup"><span data-stu-id="7dceb-110">On the action pane, select **Edit category hierarchy**.</span></span> <span data-ttu-id="7dceb-111">Nykyisen hankintaluokkahierarkia näkyy sivun vasemmalla puolella.</span><span class="sxs-lookup"><span data-stu-id="7dceb-111">The current procurement category hierarchy is displayed in the left side of the page.</span></span> <span data-ttu-id="7dceb-112">Olet muokkaamassa hierarkiaa.</span><span class="sxs-lookup"><span data-stu-id="7dceb-112">You  are about to modify the hierarchy.</span></span>  
3. <span data-ttu-id="7dceb-113">Valitse toimintoruudusta **Uusi luokkasolmu**.</span><span class="sxs-lookup"><span data-stu-id="7dceb-113">On the action pane, select **New category node**.</span></span> <span data-ttu-id="7dceb-114">Järjestelmä valitsee oletusarvoisesti ylimmän solmun.</span><span class="sxs-lookup"><span data-stu-id="7dceb-114">The system selects the top node by default.</span></span> <span data-ttu-id="7dceb-115">Jos käytät menettelyä tehtävän ohjauksena, voit napsauttaa Poista lukitus -painiketta ja valita toisen pääsolmun, johon voit lisätä uuden solmun.</span><span class="sxs-lookup"><span data-stu-id="7dceb-115">If you are running this procedure as a task guide, you can click the Unlock button and select another parent node to insert your new node into.</span></span> <span data-ttu-id="7dceb-116">Kun tämä on tehty, lukitse tehtäväopas uudelleen ja napsauta Uusi luokka -solmua.</span><span class="sxs-lookup"><span data-stu-id="7dceb-116">Once that is done, lock the task guide again and then click New category node.</span></span>  
4. <span data-ttu-id="7dceb-117">Kirjoita arvo **Nimi**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="7dceb-117">In the **Name** field, type a value.</span></span>
5. <span data-ttu-id="7dceb-118">Kirjoita **Kuvaus**-kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="7dceb-118">In the **Description** field, type a value.</span></span>
6. <span data-ttu-id="7dceb-119">Kirjoita **Kutsumanimi**-kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="7dceb-119">In the **Friendly name** field, type a value.</span></span> <span data-ttu-id="7dceb-120">Kutsumanimi on valinnainen.</span><span class="sxs-lookup"><span data-stu-id="7dceb-120">The friendly name is optional.</span></span> <span data-ttu-id="7dceb-121">Se näkyy luokkahauissa yhdessä luokan nimen kanssa.</span><span class="sxs-lookup"><span data-stu-id="7dceb-121">It will be displayed in category lookups together with the category name.</span></span>  
7. <span data-ttu-id="7dceb-122">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="7dceb-122">Select **Save**.</span></span>

## <a name="add-products-to-your-new-procurement-category"></a><span data-ttu-id="7dceb-123">Lisää tuotteita uuteen hankintaluokkaan</span><span class="sxs-lookup"><span data-stu-id="7dceb-123">Add products to your new procurement category</span></span>
1. <span data-ttu-id="7dceb-124">Siirry kohtaan **Hankinta > Tavaralähetys > Hankintaluokat**.</span><span class="sxs-lookup"><span data-stu-id="7dceb-124">Go to **Procurement and sourcing > Consignment > Procurement categories**.</span></span> <span data-ttu-id="7dceb-125">Valitse juuri lisäämäsi solmu.</span><span class="sxs-lookup"><span data-stu-id="7dceb-125">Select the node you just added.</span></span> <span data-ttu-id="7dceb-126">Jos käytät menettelyä tehtävän ohjauksena, sinun on ehkä poistettava lukitus, ennen kuin voit valita solmun.</span><span class="sxs-lookup"><span data-stu-id="7dceb-126">If you’re running this procedure as a task guide you might need to unlock the task guide to select the node.</span></span>  
2. <span data-ttu-id="7dceb-127">Ota **Tuotteet**-osion laajennus käyttöön.</span><span class="sxs-lookup"><span data-stu-id="7dceb-127">Toggle the expansion of the **Products** section.</span></span>
3. <span data-ttu-id="7dceb-128">Liitä tuotteet hankintaluokkaan valitsemalla **Lisää**.</span><span class="sxs-lookup"><span data-stu-id="7dceb-128">Select **Add** to associate products with the procurement category.</span></span>
4. <span data-ttu-id="7dceb-129">Valitse hankintaluokkaan lisättävät tuotteet.</span><span class="sxs-lookup"><span data-stu-id="7dceb-129">Select the products you want to add to the procurement category.</span></span>
5. <span data-ttu-id="7dceb-130">Lisää tuotteet **Valitut**-taulukkoon nuolen avulla.</span><span class="sxs-lookup"><span data-stu-id="7dceb-130">Select the arrow to add the products to the **Selected** table.</span></span>
6. <span data-ttu-id="7dceb-131">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="7dceb-131">Select **OK**.</span></span>
