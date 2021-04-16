---
title: Määritä hankintaluokkahierarkia
description: Tässä menettelyssä selvitetään, miten voit luoda uusia solmuja hankintaluokkahierarkiaan ja miten hankintaprosessissa käytettävä hankintaluokka määritetään.
author: kamaybac
ms.date: 06/21/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: dabourq
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 206dd5dc8f332268fe7665d84b005b5a7bfd1f9a
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/01/2021
ms.locfileid: "5837702"
---
# <a name="set-up-a-procurement-category-hierarchy"></a><span data-ttu-id="ae899-103">Määritä hankintaluokkahierarkia</span><span class="sxs-lookup"><span data-stu-id="ae899-103">Set up a procurement category hierarchy</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="ae899-104">Tässä menettelyssä selvitetään, miten voit luoda uusia solmuja hankintaluokkahierarkiaan ja miten hankintaprosessissa käytettävä hankintaluokka määritetään.</span><span class="sxs-lookup"><span data-stu-id="ae899-104">This procedure shows you how to create new nodes in a procurement category hierarchy and how to configure a procurement category to be used in a procurement process.</span></span> <span data-ttu-id="ae899-105">Yleensä ostopäällikkö tekee nämä tehtävät.</span><span class="sxs-lookup"><span data-stu-id="ae899-105">These tasks would typically be carried out by a Purchasing manager.</span></span> <span data-ttu-id="ae899-106">Ennen menettelyn aloittamista on oltava Hankita-tyyppinen luokkahierarkia.</span><span class="sxs-lookup"><span data-stu-id="ae899-106">Before you can start this procedure, there must be a category hierarchy of type Procurement.</span></span> <span data-ttu-id="ae899-107">Jos käytössä on demotietoyritys, voit suorittaa tämän menettelyn USMF-yrityksessä.</span><span class="sxs-lookup"><span data-stu-id="ae899-107">If you're using a demo data company, you can run this procedure in the USMF company.</span></span>


## <a name="add-a-new-procurement-category"></a><span data-ttu-id="ae899-108">Lisää uusi hankintaluokka</span><span class="sxs-lookup"><span data-stu-id="ae899-108">Add a new procurement category</span></span>
1. <span data-ttu-id="ae899-109">Siirry kohtaan **Siirtymisruutu > Moduulit > Hankinta > Tavaralähetys > Hankintaluokat**.</span><span class="sxs-lookup"><span data-stu-id="ae899-109">Go to **Navigation pane > Modules > Procurement and sourcing > Consignment > Procurement categories**.</span></span>
2. <span data-ttu-id="ae899-110">Valitse toimintoruudussa **Muokkaa luokkahierarkiaa**.</span><span class="sxs-lookup"><span data-stu-id="ae899-110">On the Action Pane, select **Edit category hierarchy**.</span></span> <span data-ttu-id="ae899-111">Nykyisen hankintaluokkahierarkia näkyy sivun vasemmalla puolella.</span><span class="sxs-lookup"><span data-stu-id="ae899-111">The current procurement category hierarchy is displayed in the left side of the page.</span></span> <span data-ttu-id="ae899-112">Olet muokkaamassa hierarkiaa.</span><span class="sxs-lookup"><span data-stu-id="ae899-112">You  are about to modify the hierarchy.</span></span>  
3. <span data-ttu-id="ae899-113">Valitse toimintoruudussa **Uusi luokkasolmu**.</span><span class="sxs-lookup"><span data-stu-id="ae899-113">On the Action Pane, select **New category node**.</span></span> <span data-ttu-id="ae899-114">Järjestelmä valitsee oletusarvoisesti ylimmän solmun.</span><span class="sxs-lookup"><span data-stu-id="ae899-114">The system selects the top node by default.</span></span> <span data-ttu-id="ae899-115">Jos käytät menettelyä tehtävän ohjauksena, voit napsauttaa Poista lukitus -painiketta ja valita toisen pääsolmun, johon voit lisätä uuden solmun.</span><span class="sxs-lookup"><span data-stu-id="ae899-115">If you are running this procedure as a task guide, you can click the Unlock button and select another parent node to insert your new node into.</span></span> <span data-ttu-id="ae899-116">Kun tämä on tehty, lukitse tehtäväopas uudelleen ja napsauta Uusi luokka -solmua.</span><span class="sxs-lookup"><span data-stu-id="ae899-116">Once that is done, lock the task guide again and then click New category node.</span></span>  
4. <span data-ttu-id="ae899-117">Kirjoita arvo **Nimi**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="ae899-117">In the **Name** field, type a value.</span></span>
5. <span data-ttu-id="ae899-118">Kirjoita **Kuvaus**-kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="ae899-118">In the **Description** field, type a value.</span></span>
6. <span data-ttu-id="ae899-119">Kirjoita **Kutsumanimi**-kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="ae899-119">In the **Friendly name** field, type a value.</span></span> <span data-ttu-id="ae899-120">Kutsumanimi on valinnainen.</span><span class="sxs-lookup"><span data-stu-id="ae899-120">The friendly name is optional.</span></span> <span data-ttu-id="ae899-121">Se näkyy luokkahauissa yhdessä luokan nimen kanssa.</span><span class="sxs-lookup"><span data-stu-id="ae899-121">It will be displayed in category lookups together with the category name.</span></span>  
7. <span data-ttu-id="ae899-122">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="ae899-122">Select **Save**.</span></span>

## <a name="add-products-to-your-new-procurement-category"></a><span data-ttu-id="ae899-123">Lisää tuotteita uuteen hankintaluokkaan</span><span class="sxs-lookup"><span data-stu-id="ae899-123">Add products to your new procurement category</span></span>
1. <span data-ttu-id="ae899-124">Siirry kohtaan **Hankinta > Tavaralähetys > Hankintaluokat**.</span><span class="sxs-lookup"><span data-stu-id="ae899-124">Go to **Procurement and sourcing > Consignment > Procurement categories**.</span></span> <span data-ttu-id="ae899-125">Valitse juuri lisäämäsi solmu.</span><span class="sxs-lookup"><span data-stu-id="ae899-125">Select the node you just added.</span></span> <span data-ttu-id="ae899-126">Jos käytät menettelyä tehtävän ohjauksena, sinun on ehkä poistettava lukitus, ennen kuin voit valita solmun.</span><span class="sxs-lookup"><span data-stu-id="ae899-126">If you're running this procedure as a task guide you might need to unlock the task guide to select the node.</span></span>  
2. <span data-ttu-id="ae899-127">Ota **Tuotteet**-osion laajennus käyttöön.</span><span class="sxs-lookup"><span data-stu-id="ae899-127">Toggle the expansion of the **Products** section.</span></span>
3. <span data-ttu-id="ae899-128">Liitä tuotteet hankintaluokkaan valitsemalla **Lisää**.</span><span class="sxs-lookup"><span data-stu-id="ae899-128">Select **Add** to associate products with the procurement category.</span></span>
4. <span data-ttu-id="ae899-129">Valitse hankintaluokkaan lisättävät tuotteet.</span><span class="sxs-lookup"><span data-stu-id="ae899-129">Select the products you want to add to the procurement category.</span></span>
5. <span data-ttu-id="ae899-130">Lisää tuotteet **Valitut**-taulukkoon nuolen avulla.</span><span class="sxs-lookup"><span data-stu-id="ae899-130">Select the arrow to add the products to the **Selected** table.</span></span>
6. <span data-ttu-id="ae899-131">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="ae899-131">Select **OK**.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]