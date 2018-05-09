--- 
title: Luo dimensioihin perustuvat konfiguraatiot
description: "Seuraavassa kuvataan konfiguraation määrittäminen dimensioperustaiselle tuotteelle."
author: YuyuScheller
manager: AnnBe
ms.date: 06/21/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: bis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 55f69d75b7b00eb640eb3fff5eda28a420fa84ad
ms.contentlocale: fi-fi
ms.lasthandoff: 05/08/2018

---
# <a name="create-dimension-based-configurations"></a><span data-ttu-id="7be7c-103">Luo dimensioihin perustuvat konfiguraatiot</span><span class="sxs-lookup"><span data-stu-id="7be7c-103">Create dimension-based configurations</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="7be7c-104">Seuraavassa kuvataan konfiguraation määrittäminen dimensioperustaiselle tuotteelle.</span><span class="sxs-lookup"><span data-stu-id="7be7c-104">This procedure shows how to define a configuration for a dimension-based product.</span></span> <span data-ttu-id="7be7c-105">Tämä on viimeinen kahdeksasta menettelystä, joissa selitetään, miten dimensioihin perustuvia konfiguraatioyhdistelmiä luodaan.</span><span class="sxs-lookup"><span data-stu-id="7be7c-105">This is the last procedure in the series that explains how to build combinations for dimension-based configuration.</span></span> <span data-ttu-id="7be7c-106">Tämän menettelyn suorittaminen on riippuvainen seitsemässä edellisessä osassa luoduista tiedoista.</span><span class="sxs-lookup"><span data-stu-id="7be7c-106">The execution of this procedure is dependent on the data created in the previous seven recordings.</span></span> <span data-ttu-id="7be7c-107">Tämän menettelyn luomisessa käytetty esittely-yritys on USMF.</span><span class="sxs-lookup"><span data-stu-id="7be7c-107">The demo data company used to create this procedure is USMF.</span></span>


## <a name="find-the-dimension-based-product-master"></a><span data-ttu-id="7be7c-108">Paikanna dimensioihin perustuva päätuote</span><span class="sxs-lookup"><span data-stu-id="7be7c-108">Find the dimension-based product master</span></span>
1. <span data-ttu-id="7be7c-109">Valitse Vapautetun tuotteen ylläpito.</span><span class="sxs-lookup"><span data-stu-id="7be7c-109">Click Released product maintenance.</span></span>
2. <span data-ttu-id="7be7c-110">Valitse Vapautetut tuotteet.</span><span class="sxs-lookup"><span data-stu-id="7be7c-110">Click Released products.</span></span>
3. <span data-ttu-id="7be7c-111">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="7be7c-111">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="7be7c-112">Valitse tämän kahdeksanosaisen tallennesarjan ensimmäisessä osassa luomasi dimensioperustainen päätuote.</span><span class="sxs-lookup"><span data-stu-id="7be7c-112">Select the dimension-based product master that you created in the first recording in this sequence of 8 recordings.</span></span>  

## <a name="create-configurations"></a><span data-ttu-id="7be7c-113">Luo konfiguroinnit</span><span class="sxs-lookup"><span data-stu-id="7be7c-113">Create configurations</span></span>
1. <span data-ttu-id="7be7c-114">Valitse teknisen suunnittelun toimintoruudussa Ylläpidä konfigurointeja.</span><span class="sxs-lookup"><span data-stu-id="7be7c-114">On the Engineering Action Pane, click Maintain configurations.</span></span>
2. <span data-ttu-id="7be7c-115">Napsauta Konfiguroi.</span><span class="sxs-lookup"><span data-stu-id="7be7c-115">Click Configure.</span></span>
3. <span data-ttu-id="7be7c-116">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="7be7c-116">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="7be7c-117">Syötä tai valitse arvo Nimiketunnus-kentässä.</span><span class="sxs-lookup"><span data-stu-id="7be7c-117">In the Item number field, enter or select a value.</span></span>
    * <span data-ttu-id="7be7c-118">Valitse nimikkeet ensimmäisestä konfiguraatioryhmästä.</span><span class="sxs-lookup"><span data-stu-id="7be7c-118">Select any of the items in the first configuration group.</span></span>  
5. <span data-ttu-id="7be7c-119">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="7be7c-119">In the list, find and select the desired record.</span></span>
6. <span data-ttu-id="7be7c-120">Syötä tai valitse arvo Nimiketunnus-kentässä.</span><span class="sxs-lookup"><span data-stu-id="7be7c-120">In the Item number field, enter or select a value.</span></span>
    * <span data-ttu-id="7be7c-121">Valitse nimike toisesta konfiguraatioryhmästä.</span><span class="sxs-lookup"><span data-stu-id="7be7c-121">Select any item from the second configuration group.</span></span>  
7. <span data-ttu-id="7be7c-122">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="7be7c-122">Click OK.</span></span>
8. <span data-ttu-id="7be7c-123">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="7be7c-123">In the list, mark the selected row.</span></span>
9. <span data-ttu-id="7be7c-124">Syötä arvo Konfiguraatio-kenttään.</span><span class="sxs-lookup"><span data-stu-id="7be7c-124">In the Configuration field, type a value.</span></span>
    * <span data-ttu-id="7be7c-125">Määritä konfiguroinnin nimi, jonka avulla se on helppo tunnistaa.</span><span class="sxs-lookup"><span data-stu-id="7be7c-125">Enter a configuration name that will make it easy to identify the configuration.</span></span>  
10. <span data-ttu-id="7be7c-126">Kirjoita arvo Kuvaus-kenttään.</span><span class="sxs-lookup"><span data-stu-id="7be7c-126">In the Description field, type a value.</span></span>
    * <span data-ttu-id="7be7c-127">Kirjoita konfiguraatiolle sen sisällön selittävä kuvaus.</span><span class="sxs-lookup"><span data-stu-id="7be7c-127">Enter a description of the configuration to explain what it contains.</span></span>  
11. <span data-ttu-id="7be7c-128">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="7be7c-128">Click OK.</span></span>


