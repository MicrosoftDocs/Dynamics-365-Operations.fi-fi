---
title: "Määritä työtiloja ja suodata niitä"
description: "Tämä artikkeli sisältää työtilojen määrittämisen ja suodattamisen yleiskuvauksen."
author: jasongre
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 17491
ms.assetid: 541e6012-4680-4684-8494-e9b5ca4684ee
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 08c38aada355583c5a6872f75b57db95d9b81786
ms.openlocfilehash: 754cd81a4550318de7003d847fafb2bcc7414b32
ms.contentlocale: fi-fi
ms.lasthandoff: 07/18/2017

---

# <a name="configure-and-filter-workspaces"></a><span data-ttu-id="f2200-103">Määritä työtiloja ja suodata niitä</span><span class="sxs-lookup"><span data-stu-id="f2200-103">Configure and filter workspaces</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="f2200-104">Tämä artikkeli sisältää työtilojen määrittämisen ja suodattamisen yleiskuvauksen.</span><span class="sxs-lookup"><span data-stu-id="f2200-104">This article provides an overview about how to configure and filter workspaces.</span></span>

<a name="configuring-a-workspace"></a><span data-ttu-id="f2200-105">Työtilan määrittäminen</span><span class="sxs-lookup"><span data-stu-id="f2200-105">Configuring a workspace</span></span>
-----------------------

<span data-ttu-id="f2200-106">Voit muuttaa joidenkin työtilojen ulkoasua ja toimintaa päivittämällä koko työtilaa koskevat asetukset.</span><span class="sxs-lookup"><span data-stu-id="f2200-106">You can change the appearance and behavior of some workspaces by updating settings that apply to the whole workspace.</span></span> <span data-ttu-id="f2200-107">Kun työtilaa voi määrittää, toimintoruudussa on painike, jonka avulla määrityksiä voi muuttaa.</span><span class="sxs-lookup"><span data-stu-id="f2200-107">When a workspace can be configured, the Action Pane includes a button that instructs you to click it to make configuration changes.</span></span> <span data-ttu-id="f2200-108">Esimerkiksi seuraavassa kuvassa painikkeen nimeksi on annettu **Määritä oma työtila**.</span><span class="sxs-lookup"><span data-stu-id="f2200-108">For example, in the following illustration, the button is named **Configure my workspace**.</span></span> 

<span data-ttu-id="f2200-109">[![configure-and-filter-workspaces](./media/configure-and-filter-workspaces.png)](./media/configure-and-filter-workspaces.png)</span><span class="sxs-lookup"><span data-stu-id="f2200-109">[![configure-and-filter-workspaces](./media/configure-and-filter-workspaces.png)](./media/configure-and-filter-workspaces.png)</span></span>   

<span data-ttu-id="f2200-110">Kun napsautat painiketta, voit muokata avautuvassa valintaikkunassa työtilan ennalta määritettyjä asetuksia.</span><span class="sxs-lookup"><span data-stu-id="f2200-110">When you click the button, a dialog appears, where you can modify the predefined settings for the workspace.</span></span> <span data-ttu-id="f2200-111">Valintaikkunassa olevat erikoisasetukset vaihtelevat työtilan mukaan. Ne riippuvat työtilan erityisistä ohjausobjekteista ja liiketoimintatiedoista.</span><span class="sxs-lookup"><span data-stu-id="f2200-111">The specific settings that you see in this dialog vary by workspace, and depend on the specific controls and business data that are available in the workspace.</span></span> 

<span data-ttu-id="f2200-112">[![configure-my-workspace](./media/configure-my-workspace.png)](./media/configure-my-workspace.png)</span><span class="sxs-lookup"><span data-stu-id="f2200-112">[![configure-my-workspace](./media/configure-my-workspace.png)](./media/configure-my-workspace.png)</span></span>

## <a name="filtering-a-workspace"></a><span data-ttu-id="f2200-113">Työtilan suodattaminen</span><span class="sxs-lookup"><span data-stu-id="f2200-113">Filtering a workspace</span></span>
<span data-ttu-id="f2200-114">Useiden työtilojen sisältöä voi suodattaa.</span><span class="sxs-lookup"><span data-stu-id="f2200-114">Many workspaces let you filter the content that appears in them.</span></span> <span data-ttu-id="f2200-115">Käytettävissä olevien ohjausobjektien avulla voi suodattaa kaiken sisällön tai vain tietyn osan sisällön työtilassa.</span><span class="sxs-lookup"><span data-stu-id="f2200-115">The controls that are available might let you filter all the content in the workspace or only the content in a specific section of the workspace.</span></span> <span data-ttu-id="f2200-116">Työtilojen suodattimet voivat olla valintoja, yhdistelmäruutuja, vapaatekstikenttiä tai muita ohjausobjekteja.</span><span class="sxs-lookup"><span data-stu-id="f2200-116">The filters on workspaces can be lookups, combo boxes, free-form text fields, or other types of controls.</span></span> <span data-ttu-id="f2200-117">Jokaisella suodattimella on kuitenkin samat vaikutukset seuraavissa osissa esitetyllä tavalla.</span><span class="sxs-lookup"><span data-stu-id="f2200-117">However, every type of filter has the same effects, as described in the following sections.</span></span>

### <a name="workspace-wide-filters"></a><span data-ttu-id="f2200-118">Työtilakohtaiset suodattimet</span><span class="sxs-lookup"><span data-stu-id="f2200-118">Workspace-wide filters</span></span>

<span data-ttu-id="f2200-119">Voit suodattaa koko työtilan työtilakohtaisen suodattimen avulla.</span><span class="sxs-lookup"><span data-stu-id="f2200-119">You can filter the whole workspace by using a workspace-wide filter.</span></span> <span data-ttu-id="f2200-120">Työtilakohtainen suodatin löytyy työtilan vasemmasta yläkulmasta.</span><span class="sxs-lookup"><span data-stu-id="f2200-120">A workspace-wide filter appears in the upper-left corner of the workspace.</span></span> <span data-ttu-id="f2200-121">Kun avattavasta luettelosta valitaan arvo, työtilan sisältö suodatetaan valinnan mukaan.</span><span class="sxs-lookup"><span data-stu-id="f2200-121">When you select a specific value in the drop-down list, the contents of the workspace are filtered based on that selection.</span></span> 

<span data-ttu-id="f2200-122">[![workspace-filter](./media/workspace-filter.png)](./media/workspace-filter.png)</span><span class="sxs-lookup"><span data-stu-id="f2200-122">[![workspace-filter](./media/workspace-filter.png)](./media/workspace-filter.png)</span></span> 

<span data-ttu-id="f2200-123">Kun avaat suodattimen, esiin tulee useita vaihtoehtoja.</span><span class="sxs-lookup"><span data-stu-id="f2200-123">When you click to open the filter, you're presented with several options.</span></span> 

<span data-ttu-id="f2200-124">[![workspace-filter-expanded](./media/workspace-filter-expanded.png)](./media/workspace-filter-expanded.png)</span><span class="sxs-lookup"><span data-stu-id="f2200-124">[![workspace-filter-expanded](./media/workspace-filter-expanded.png)](./media/workspace-filter-expanded.png)</span></span> 

<span data-ttu-id="f2200-125">Valitse asetus, jonka perusteella työtila suodatetaan.</span><span class="sxs-lookup"><span data-stu-id="f2200-125">Select an option to filter the workspace based on that option.</span></span>

### <a name="workspace-section-filters"></a><span data-ttu-id="f2200-126">Työtilan osan suodattimet</span><span class="sxs-lookup"><span data-stu-id="f2200-126">Workspace section filters</span></span>

<span data-ttu-id="f2200-127">Jos työtilan yksittäisillä osilla on suodattimia, voit suodattaa kunkin osan erikseen.</span><span class="sxs-lookup"><span data-stu-id="f2200-127">If individual sections of the workspace have filters, you can filter each section separately.</span></span> <span data-ttu-id="f2200-128">Seuraavassa kuvassa suodatin (kenttä, jossa lukee Suodatin) on esimerkki vapaatekstikentän suodattimesta.</span><span class="sxs-lookup"><span data-stu-id="f2200-128">In the following illustration, the filter (the field that contains the text "Filter") is an example of a free-form text field filter.</span></span> 

<span data-ttu-id="f2200-129">[![workspace-section-filters](./media/workspace-section-filters.png)](./media/workspace-section-filters.png)</span><span class="sxs-lookup"><span data-stu-id="f2200-129">[![workspace-section-filters](./media/workspace-section-filters.png)](./media/workspace-section-filters.png)</span></span> 

<span data-ttu-id="f2200-130">Suodata osan sisältö valitsemalla tai antamalla arvo samalla tavalla kuin työtilakohtaisessa suodattimessa.</span><span class="sxs-lookup"><span data-stu-id="f2200-130">As with a workspace-wide filter, select or enter a value in the field to filter the contents of the section.</span></span>




