--- 
title: Vanhentuneiden tuotevarianttien etsiminen
description: "Tässä menettelyssä kerrotaan, miten vanhentuneita julkaistuja tuotteita tai tuotevariantteja etsitään ja miten tuotteen elinkaaren tila liitetään vanhentuneisiin tuotteisiin."
author: cvocph
manager: AnnBe
ms.date: 12/05/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: conradv
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 402f387ac58d550037fbae2011b176c09f45185a
ms.contentlocale: fi-fi
ms.lasthandoff: 04/13/2018

---
# <a name="find-obsolete-product-variants"></a><span data-ttu-id="c1913-103">Vanhentuneiden tuotevarianttien etsiminen</span><span class="sxs-lookup"><span data-stu-id="c1913-103">Find obsolete product variants</span></span> 

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="c1913-104">Tässä menettelyssä kerrotaan, miten vanhentuneita julkaistuja tuotteita tai tuotevariantteja etsitään ja miten tuotteen elinkaaren tila liitetään vanhentuneisiin tuotteisiin.</span><span class="sxs-lookup"><span data-stu-id="c1913-104">This procedure shows how to find obsolete released products or product variants and how to associate a product lifecycle state to the obsolete products.</span></span> <span data-ttu-id="c1913-105">Edellytys: Sinun on määritettävä vähintään yksi tuotteen elinkaaren tila, joka ei ole aktiivinen suunnittelua varten, ennen kuin voit toistaa tämän tehtäväoppaan.</span><span class="sxs-lookup"><span data-stu-id="c1913-105">Prerequisite: You need to define at least one product lifecycle state that is inactive for planning before you can play this task guide.</span></span>


## <a name="run-a-simulation"></a><span data-ttu-id="c1913-106">Simuloinnin suorittaminen</span><span class="sxs-lookup"><span data-stu-id="c1913-106">Run a simulation</span></span>
1. <span data-ttu-id="c1913-107">Valitse Tuotetietojen hallinta > Kausittaiset tehtävät > Muuta vanhentuneiden tuotteiden elinkaaren tilaa.</span><span class="sxs-lookup"><span data-stu-id="c1913-107">Go to Product information management > Periodic tasks > Change lifecycle state for obsolete products.</span></span>
2. <span data-ttu-id="c1913-108">Syötä tai valitse arvo Uusi tuotteen elinkaaren tila -kenttään.</span><span class="sxs-lookup"><span data-stu-id="c1913-108">In the New product lifecycle state field, enter or select a value.</span></span>
3. <span data-ttu-id="c1913-109">Valitse Kyllä Suorita simulaatio päivittämättä tuotetietoja -kenttään.</span><span class="sxs-lookup"><span data-stu-id="c1913-109">Select Yes in the Run simulation without updating product data field.</span></span>
4. <span data-ttu-id="c1913-110">Syötä Jätä pois tätä päivien määrää uudemmat tuotteet -kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="c1913-110">In the Exclude products created within this number of days field, enter a number.</span></span>
5. <span data-ttu-id="c1913-111">Syötä Jätä pois tuotteet, joita on käytetty tapahtumissa (päivien määrän kuluessa) -kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="c1913-111">In the Exclude products used in transactions (in number of days) field, enter a number.</span></span>
6. <span data-ttu-id="c1913-112">Laajenna Tietueet-kohta ja sisällytä osaan.</span><span class="sxs-lookup"><span data-stu-id="c1913-112">Expand the Records to include section.</span></span>
7. <span data-ttu-id="c1913-113">Valitse Suodatin.</span><span class="sxs-lookup"><span data-stu-id="c1913-113">Click Filter.</span></span>
8. <span data-ttu-id="c1913-114">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="c1913-114">In the list, mark the selected row.</span></span>
9. <span data-ttu-id="c1913-115">Kirjoita arvo Ehdot-kenttään.</span><span class="sxs-lookup"><span data-stu-id="c1913-115">In the Criteria field, type a value.</span></span>
10. <span data-ttu-id="c1913-116">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="c1913-116">Click OK.</span></span>
11. <span data-ttu-id="c1913-117">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="c1913-117">Click OK.</span></span>

> [!NOTE]
> <span data-ttu-id="c1913-118">Simulointi kannattaa suorittaa eräajona, jos haku tehdään suuresta tuotemäärästä.</span><span class="sxs-lookup"><span data-stu-id="c1913-118">It is recommended to run the simulation in batch if you expect to search a large number of products.</span></span> <span data-ttu-id="c1913-119">Varmista myös, että simulointia ei suoriteta yrityksen aktiivisena työaikana.</span><span class="sxs-lookup"><span data-stu-id="c1913-119">Also, make sure that the simulation is not run during the most active working time of the company.</span></span>  

## <a name="review-the-simulation-results"></a><span data-ttu-id="c1913-120">Simuloinnin tulosten tarkistaminen</span><span class="sxs-lookup"><span data-stu-id="c1913-120">Review the simulation results</span></span>
1. <span data-ttu-id="c1913-121">Valitse Tuotetietojen hallinta > Kyselyt ja raportit > Tuotteen elinkaaren tilan historia.</span><span class="sxs-lookup"><span data-stu-id="c1913-121">Go to Product information management > Inquiries and reports > Product lifecycle state maintenance history.</span></span>
   
> [!NOTE]
> <span data-ttu-id="c1913-122">Tällä sivulla voit tarkastella simulointituloksia ja arvioida, miten useita tuotteita ja tuotevariantteja liitetään uuteen tuotteen elinkaaren tilaan, kun päivitys suoritetaan ilman simulointia.</span><span class="sxs-lookup"><span data-stu-id="c1913-122">On this page, you can review the simulation results and make an assessment of how many products and product variants will be associated with a new product lifecycle state when running the update without simulation.</span></span>  

## <a name="run-the-update-of-the-product-lifecycle-state-for-obsolete-products"></a><span data-ttu-id="c1913-123">Tuotteen elinkaaren tilan päivityksen suorittaminen vanhentuneille tuotteille</span><span class="sxs-lookup"><span data-stu-id="c1913-123">Run the update of the Product lifecycle state for obsolete products</span></span>
1. <span data-ttu-id="c1913-124">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="c1913-124">Close the page.</span></span>
2. <span data-ttu-id="c1913-125">Valitse Tuotetietojen hallinta > Kausittaiset tehtävät > Muuta vanhentuneiden tuotteiden elinkaaren tilaa.</span><span class="sxs-lookup"><span data-stu-id="c1913-125">Go to Product information management > Periodic tasks > Change lifecycle state for obsolete products.</span></span>
3. <span data-ttu-id="c1913-126">Laajenna Tietueet-kohta ja sisällytä osaan.</span><span class="sxs-lookup"><span data-stu-id="c1913-126">Expand the Records to include section.</span></span>

> [!NOTE]
> <span data-ttu-id="c1913-127">Huomaa, että edellinen valinta on tallennettu.</span><span class="sxs-lookup"><span data-stu-id="c1913-127">Note that the last selection has been saved.</span></span>  

4. <span data-ttu-id="c1913-128">Valitse Ei Suorita simulaatio päivittämättä tuotetietoja -kenttään.</span><span class="sxs-lookup"><span data-stu-id="c1913-128">Select No in the Run simulation without updating product data field.</span></span>
5. <span data-ttu-id="c1913-129">Laajenna Suorita taustalla -osa.</span><span class="sxs-lookup"><span data-stu-id="c1913-129">Expand the Run in the background section.</span></span>

> [!NOTE]
> <span data-ttu-id="c1913-130">Tämä työ kannattaa ehkä suorittaa eräajona, jos tuotteita ja tuotevariantteja on paljon.</span><span class="sxs-lookup"><span data-stu-id="c1913-130">Depending on how many products and product variants are affected, consider running this job in batch.</span></span> <span data-ttu-id="c1913-131">Varmista, että et suorita suurta päivitystyötä yrityksen aktiivisimpana työaikana.</span><span class="sxs-lookup"><span data-stu-id="c1913-131">Make sure that you are not running a large update job during the most active working hours in the company.</span></span>  

6. <span data-ttu-id="c1913-132">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="c1913-132">Click OK.</span></span>
7. <span data-ttu-id="c1913-133">Valitse Tuotetietojen hallinta > Kyselyt ja raportit > Tuotteen elinkaaren tilan historia.</span><span class="sxs-lookup"><span data-stu-id="c1913-133">Go to Product information management > Inquiries and reports > Product lifecycle state maintenance history.</span></span>

> [!NOTE]
> <span data-ttu-id="c1913-134">Tarkista muutetut julkaistut tuotteet ja tuotevariantit.</span><span class="sxs-lookup"><span data-stu-id="c1913-134">Review the changed released products and product variants.</span></span>  

8. <span data-ttu-id="c1913-135">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="c1913-135">In the list, find and select the desired record.</span></span>


