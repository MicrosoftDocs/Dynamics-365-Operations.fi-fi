--- 
title: Valikoimien hallinta
description: "Tässä menettelyssä kerrotaan, miten uusi tuotevalikoima luodaan ja julkaistaan. Siinä käytetään esittelytietoja yrityksestä USRT."
author: jashanno
manager: AnnBe
ms.date: 10/31/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 1b50b06879fa50db7d7dc652a15e1284d7b74d17
ms.contentlocale: fi-fi
ms.lasthandoff: 08/29/2017

---
# <a name="manage-assortments"></a><span data-ttu-id="af0a6-103">Valikoimien hallinta</span><span class="sxs-lookup"><span data-stu-id="af0a6-103">Manage assortments</span></span> 

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="af0a6-104">Tässä menettelyssä kerrotaan, miten uusi tuotevalikoima luodaan ja julkaistaan. Siinä käytetään esittelytietoja yrityksestä USRT.</span><span class="sxs-lookup"><span data-stu-id="af0a6-104">This procedure demonstrates how to create and publish a new product assortment and uses the demo data company USRT.</span></span> <span data-ttu-id="af0a6-105">Tätä menettelyä varten tarvitaan Dynamics AX -sovellus 7.0.1 tai uudempi ja Dynamics AX -ympäristö 7.1.</span><span class="sxs-lookup"><span data-stu-id="af0a6-105">This procedure requires Dynamics AX application 7.0.1 or later, and Dynamics AX platform 7.1.</span></span>  

1. <span data-ttu-id="af0a6-106">Napsauta kohtaa Luokka- ja tuotehallinta.</span><span class="sxs-lookup"><span data-stu-id="af0a6-106">Click Category and product management.</span></span>

## <a name="create-an-assortment"></a><span data-ttu-id="af0a6-107">Luo valikoima</span><span class="sxs-lookup"><span data-stu-id="af0a6-107">Create an assortment</span></span>
1. <span data-ttu-id="af0a6-108">Avaa Vähittäismyynti-välilehti.</span><span class="sxs-lookup"><span data-stu-id="af0a6-108">Click the Assortments tab.</span></span>
2. <span data-ttu-id="af0a6-109">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="af0a6-109">Click New.</span></span>
3. <span data-ttu-id="af0a6-110">Valitse Valikoima.</span><span class="sxs-lookup"><span data-stu-id="af0a6-110">Click Assortment.</span></span>
    * <span data-ttu-id="af0a6-111">Valikoiman tunnus on pakollinen ja se on oltava yksilöivä.</span><span class="sxs-lookup"><span data-stu-id="af0a6-111">The Assortment ID is required and must be a unique value.</span></span>  
4. <span data-ttu-id="af0a6-112">Kirjoita arvo Valikoiman nimi -kenttään.</span><span class="sxs-lookup"><span data-stu-id="af0a6-112">In the Assortment name field, type a value.</span></span>
5. <span data-ttu-id="af0a6-113">Syötä päivämäärä Voimaantulopäivä-kenttään.</span><span class="sxs-lookup"><span data-stu-id="af0a6-113">In the Effective date field, enter a date.</span></span>
6. <span data-ttu-id="af0a6-114">Kirjoita päivämäärä Vanhentumispäivä-kenttään.</span><span class="sxs-lookup"><span data-stu-id="af0a6-114">In the Expiration date field, enter a date.</span></span>
7. <span data-ttu-id="af0a6-115">Laajenna Vähittäismyynnin Kanavat -osa.</span><span class="sxs-lookup"><span data-stu-id="af0a6-115">Expand the Retail channels section.</span></span>
8. <span data-ttu-id="af0a6-116">Valitse Lisää rivi.</span><span class="sxs-lookup"><span data-stu-id="af0a6-116">Click Add line.</span></span>
9. <span data-ttu-id="af0a6-117">Valitse puussa Contoso Retail\Electronics\Boston.</span><span class="sxs-lookup"><span data-stu-id="af0a6-117">In the tree, select 'Contoso Retail\Electronics\Boston'.</span></span>
10. <span data-ttu-id="af0a6-118">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="af0a6-118">Click Add.</span></span>
11. <span data-ttu-id="af0a6-119">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="af0a6-119">Click OK.</span></span>
12. <span data-ttu-id="af0a6-120">Laajenna Tuotteet-osa.</span><span class="sxs-lookup"><span data-stu-id="af0a6-120">Expand the Products section.</span></span>
13. <span data-ttu-id="af0a6-121">Valitse Lisää rivi.</span><span class="sxs-lookup"><span data-stu-id="af0a6-121">Click Add line.</span></span>
14. <span data-ttu-id="af0a6-122">Anna tai valitse Luokka-kentässä arvo.</span><span class="sxs-lookup"><span data-stu-id="af0a6-122">In the Category field, enter or select a value.</span></span>
15. <span data-ttu-id="af0a6-123">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="af0a6-123">Click Save.</span></span>

## <a name="publish-an-assortment"></a><span data-ttu-id="af0a6-124">Julkaise valikoima</span><span class="sxs-lookup"><span data-stu-id="af0a6-124">Publish an assortment</span></span>
1. <span data-ttu-id="af0a6-125">Valitse Julkaise.</span><span class="sxs-lookup"><span data-stu-id="af0a6-125">Click Publish.</span></span>
2. <span data-ttu-id="af0a6-126">Valitse Kyllä.</span><span class="sxs-lookup"><span data-stu-id="af0a6-126">Click Yes.</span></span>


