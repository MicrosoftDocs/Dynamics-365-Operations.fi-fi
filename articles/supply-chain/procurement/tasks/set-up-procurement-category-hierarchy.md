---
title: Määritä hankintaluokkahierarkia
description: Tässä menettelyssä selvitetään, miten voit luoda uusia solmuja hankintaluokkahierarkiaan ja miten hankintaprosessissa käytettävä hankintaluokka määritetään.
author: mkirknel
manager: tfehr
ms.date: 06/21/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: eaab2093eb2531b63f27717d828f7064a8f9ed1d
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/02/2020
ms.locfileid: "3207505"
---
# <a name="set-up-a-procurement-category-hierarchy"></a><span data-ttu-id="c1952-103">Määritä hankintaluokkahierarkia</span><span class="sxs-lookup"><span data-stu-id="c1952-103">Set up a procurement category hierarchy</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="c1952-104">Tässä menettelyssä selvitetään, miten voit luoda uusia solmuja hankintaluokkahierarkiaan ja miten hankintaprosessissa käytettävä hankintaluokka määritetään.</span><span class="sxs-lookup"><span data-stu-id="c1952-104">This procedure shows you how to create new nodes in a procurement category hierarchy and how to configure a procurement category to be used in a procurement process.</span></span> <span data-ttu-id="c1952-105">Yleensä ostopäällikkö tekee nämä tehtävät.</span><span class="sxs-lookup"><span data-stu-id="c1952-105">These tasks would typically be carried out by a Purchasing manager.</span></span> <span data-ttu-id="c1952-106">Ennen menettelyn aloittamista on oltava Hankita-tyyppinen luokkahierarkia.</span><span class="sxs-lookup"><span data-stu-id="c1952-106">Before you can start this procedure, there must be a category hierarchy of type Procurement.</span></span> <span data-ttu-id="c1952-107">Jos käytössä on demotietoyritys, voit suorittaa tämän menettelyn USMF-yrityksessä.</span><span class="sxs-lookup"><span data-stu-id="c1952-107">If you're using a demo data company, you can run this procedure in the USMF company.</span></span>


## <a name="add-a-new-procurement-category"></a><span data-ttu-id="c1952-108">Lisää uusi hankintaluokka</span><span class="sxs-lookup"><span data-stu-id="c1952-108">Add a new procurement category</span></span>
1. <span data-ttu-id="c1952-109">Siirry kohtaan **Siirtymisruutu > Moduulit > Hankinta > Tavaralähetys > Hankintaluokat**.</span><span class="sxs-lookup"><span data-stu-id="c1952-109">Go to **Navigation pane > Modules > Procurement and sourcing > Consignment > Procurement categories**.</span></span>
2. <span data-ttu-id="c1952-110">Valitse toimintoruudusta **Muokkaa luokkahierarkiaa**.</span><span class="sxs-lookup"><span data-stu-id="c1952-110">On the action pane, select **Edit category hierarchy**.</span></span> <span data-ttu-id="c1952-111">Nykyisen hankintaluokkahierarkia näkyy sivun vasemmalla puolella.</span><span class="sxs-lookup"><span data-stu-id="c1952-111">The current procurement category hierarchy is displayed in the left side of the page.</span></span> <span data-ttu-id="c1952-112">Olet muokkaamassa hierarkiaa.</span><span class="sxs-lookup"><span data-stu-id="c1952-112">You  are about to modify the hierarchy.</span></span>  
3. <span data-ttu-id="c1952-113">Valitse toimintoruudusta **Uusi luokkasolmu**.</span><span class="sxs-lookup"><span data-stu-id="c1952-113">On the action pane, select **New category node**.</span></span> <span data-ttu-id="c1952-114">Järjestelmä valitsee oletusarvoisesti ylimmän solmun.</span><span class="sxs-lookup"><span data-stu-id="c1952-114">The system selects the top node by default.</span></span> <span data-ttu-id="c1952-115">Jos käytät menettelyä tehtävän ohjauksena, voit napsauttaa Poista lukitus -painiketta ja valita toisen pääsolmun, johon voit lisätä uuden solmun.</span><span class="sxs-lookup"><span data-stu-id="c1952-115">If you are running this procedure as a task guide, you can click the Unlock button and select another parent node to insert your new node into.</span></span> <span data-ttu-id="c1952-116">Kun tämä on tehty, lukitse tehtäväopas uudelleen ja napsauta Uusi luokka -solmua.</span><span class="sxs-lookup"><span data-stu-id="c1952-116">Once that is done, lock the task guide again and then click New category node.</span></span>  
4. <span data-ttu-id="c1952-117">Kirjoita arvo **Nimi**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="c1952-117">In the **Name** field, type a value.</span></span>
5. <span data-ttu-id="c1952-118">Kirjoita **Kuvaus**-kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="c1952-118">In the **Description** field, type a value.</span></span>
6. <span data-ttu-id="c1952-119">Kirjoita **Kutsumanimi**-kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="c1952-119">In the **Friendly name** field, type a value.</span></span> <span data-ttu-id="c1952-120">Kutsumanimi on valinnainen.</span><span class="sxs-lookup"><span data-stu-id="c1952-120">The friendly name is optional.</span></span> <span data-ttu-id="c1952-121">Se näkyy luokkahauissa yhdessä luokan nimen kanssa.</span><span class="sxs-lookup"><span data-stu-id="c1952-121">It will be displayed in category lookups together with the category name.</span></span>  
7. <span data-ttu-id="c1952-122">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="c1952-122">Select **Save**.</span></span>

## <a name="add-products-to-your-new-procurement-category"></a><span data-ttu-id="c1952-123">Lisää tuotteita uuteen hankintaluokkaan</span><span class="sxs-lookup"><span data-stu-id="c1952-123">Add products to your new procurement category</span></span>
1. <span data-ttu-id="c1952-124">Siirry kohtaan **Hankinta > Tavaralähetys > Hankintaluokat**.</span><span class="sxs-lookup"><span data-stu-id="c1952-124">Go to **Procurement and sourcing > Consignment > Procurement categories**.</span></span> <span data-ttu-id="c1952-125">Valitse juuri lisäämäsi solmu.</span><span class="sxs-lookup"><span data-stu-id="c1952-125">Select the node you just added.</span></span> <span data-ttu-id="c1952-126">Jos käytät menettelyä tehtävän ohjauksena, sinun on ehkä poistettava lukitus, ennen kuin voit valita solmun.</span><span class="sxs-lookup"><span data-stu-id="c1952-126">If you're running this procedure as a task guide you might need to unlock the task guide to select the node.</span></span>  
2. <span data-ttu-id="c1952-127">Ota **Tuotteet**-osion laajennus käyttöön.</span><span class="sxs-lookup"><span data-stu-id="c1952-127">Toggle the expansion of the **Products** section.</span></span>
3. <span data-ttu-id="c1952-128">Liitä tuotteet hankintaluokkaan valitsemalla **Lisää**.</span><span class="sxs-lookup"><span data-stu-id="c1952-128">Select **Add** to associate products with the procurement category.</span></span>
4. <span data-ttu-id="c1952-129">Valitse hankintaluokkaan lisättävät tuotteet.</span><span class="sxs-lookup"><span data-stu-id="c1952-129">Select the products you want to add to the procurement category.</span></span>
5. <span data-ttu-id="c1952-130">Lisää tuotteet **Valitut**-taulukkoon nuolen avulla.</span><span class="sxs-lookup"><span data-stu-id="c1952-130">Select the arrow to add the products to the **Selected** table.</span></span>
6. <span data-ttu-id="c1952-131">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="c1952-131">Select **OK**.</span></span>
