--- 
title: "Luo myyntipisteen käyttöoikeusryhmät"
description: "Tässä menettelyssä kerrotaan, miten myyntipisteen käyttöoikeusryhmä luodaan."
author: scott-tucker
manager: AnnBe
ms.date: 03/02/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations, Retail
ms.search.region: Global
ms.search.industry: Retail
ms.author: scotttuc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 985cce1f1848408517ce71b36575162960c3d84e
ms.contentlocale: fi-fi
ms.lasthandoff: 05/08/2018

---
# <a name="create-pos-permission-groups"></a><span data-ttu-id="13227-103">Luo myyntipisteen käyttöoikeusryhmät</span><span class="sxs-lookup"><span data-stu-id="13227-103">Create POS permission groups</span></span>

[!include [task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="13227-104">Tässä menettelyssä kerrotaan, miten myyntipisteen käyttöoikeusryhmä luodaan.</span><span class="sxs-lookup"><span data-stu-id="13227-104">This procedure will show how to create a POS permission group.</span></span> <span data-ttu-id="13227-105">Tämän tehtävän luomisessa käytetty USRT-yrityksen demotietoja.</span><span class="sxs-lookup"><span data-stu-id="13227-105">The demo data company used to create this task is USRT.</span></span> <span data-ttu-id="13227-106">Tämä tehtävä on tarkoitettu vähittäismyynnin toiminnoista vastaavan johtajan roolille.</span><span class="sxs-lookup"><span data-stu-id="13227-106">This task is intended for the Retail operations manager role.</span></span>

1. <span data-ttu-id="13227-107">Siirry Käyttöoikeusryhmät-kohtaan.</span><span class="sxs-lookup"><span data-stu-id="13227-107">Go to Permission groups.</span></span>
2. <span data-ttu-id="13227-108">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="13227-108">Click New.</span></span>
3. <span data-ttu-id="13227-109">Syötä Myyntipisteen käyttöoikeusryhmän tunnus -kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="13227-109">In the POS permission group ID field, type a value.</span></span>
4. <span data-ttu-id="13227-110">Kirjoita arvo Kuvaus-kenttään.</span><span class="sxs-lookup"><span data-stu-id="13227-110">In the Description field, type a value.</span></span>
5. <span data-ttu-id="13227-111">Valitse Näytä aikamerkinnät -kentässä Kyllä.</span><span class="sxs-lookup"><span data-stu-id="13227-111">Select Yes in the View time clock entries field.</span></span>
    * <span data-ttu-id="13227-112">Voit ottaa käyttöön myyntipisteen käyttöoikeusryhmän käyttöoikeuksia tai poistaa niitä käytöstä.</span><span class="sxs-lookup"><span data-stu-id="13227-112">You can now enable or disable various permissions for your POS Permission group.</span></span> <span data-ttu-id="13227-113">Joillekin käyttöoikeuksille voi määrittää arvon, jonka avulla arvioidaan, voiko myyntipisteen käyttäjä suorittaa toiminnon.</span><span class="sxs-lookup"><span data-stu-id="13227-113">For some permission you can set a value that will be used to evaluate if the POS user can perform the action.</span></span>  <span data-ttu-id="13227-114">Tässä tehtävän ohjauksessa otetaan käyttöön joitakin käyttöoikeuksia, jotka voidaan antaa kassalle.</span><span class="sxs-lookup"><span data-stu-id="13227-114">This task guide enables a few permission that might be given to a cashier.</span></span>  
6. <span data-ttu-id="13227-115">Valitse Salli tilauksen luominen -kentässä Kyllä.</span><span class="sxs-lookup"><span data-stu-id="13227-115">Select Yes in the Allow create order field.</span></span>
7. <span data-ttu-id="13227-116">Valitse Salli tilauksen muokkaaminen -kentässä Kyllä.</span><span class="sxs-lookup"><span data-stu-id="13227-116">Select Yes in the Allow edit order field.</span></span>
8. <span data-ttu-id="13227-117">Valitse Salli tilauksen noutaminen -kentässä Kyllä.</span><span class="sxs-lookup"><span data-stu-id="13227-117">Select Yes in the Allow retrieve order field.</span></span>
9. <span data-ttu-id="13227-118">Valitse Salli salasanan vaihtaminen -kentässä Kyllä.</span><span class="sxs-lookup"><span data-stu-id="13227-118">Select Yes in the Allow password change field.</span></span>
10. <span data-ttu-id="13227-119">Valitse Salli piilottava sulkeminen -kentässä Kyllä.</span><span class="sxs-lookup"><span data-stu-id="13227-119">Select Yes in the Allow blind close field.</span></span>
11. <span data-ttu-id="13227-120">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="13227-120">Click Save.</span></span>
    * <span data-ttu-id="13227-121">Kun muutokset on tallennettu, suorita henkilökunnan jakeluaikataulu ja siirrä muutokset vähittäismyyntikanaville.</span><span class="sxs-lookup"><span data-stu-id="13227-121">After your changes are saved you need to run the Staff distribution schedule to push the changes to retail channels.</span></span>  
12. <span data-ttu-id="13227-122">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="13227-122">Close the page.</span></span>
13. <span data-ttu-id="13227-123">Siirry Työt-kohtaan.</span><span class="sxs-lookup"><span data-stu-id="13227-123">Go to Jobs.</span></span>
    * <span data-ttu-id="13227-124">Seuraavaksi liitetään myyntipisteen käyttöoikeusryhmä työhön.</span><span class="sxs-lookup"><span data-stu-id="13227-124">Next we will assign the POS permission group to a Job.</span></span>  
14. <span data-ttu-id="13227-125">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="13227-125">In the list, find and select the desired record.</span></span>
15. <span data-ttu-id="13227-126">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="13227-126">In the list, click the link in the selected row.</span></span>
16. <span data-ttu-id="13227-127">Valitse Muokkaa.</span><span class="sxs-lookup"><span data-stu-id="13227-127">Click Edit.</span></span>
17. <span data-ttu-id="13227-128">Laajenna Työn luokittelu -osa.</span><span class="sxs-lookup"><span data-stu-id="13227-128">Expand the Job classification section.</span></span>
18. <span data-ttu-id="13227-129">Syötä tai valitse arvo Myyntipisteen käyttöoikeusryhmä -kentässä.</span><span class="sxs-lookup"><span data-stu-id="13227-129">In the POS permission group field, enter or select a value.</span></span>
    * <span data-ttu-id="13227-130">Kaikki tämän työn toimissa olevat työntekijät käyttävät näitä myyntipisteen käyttöoikeusryhmän asetuksia, ellei työntekijöiden myyntipisteen käyttöoikeuksia ole ohitettu toimen tasolla.</span><span class="sxs-lookup"><span data-stu-id="13227-130">All Workers in Positions for this Job will use this POS permission group’s settings unless the workers POS permissions have been overridden at their Position level.</span></span>  
19. <span data-ttu-id="13227-131">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="13227-131">Click Save.</span></span>
    * <span data-ttu-id="13227-132">Kun muutokset on tallennettu, suorita henkilökunnan jakeluaikataulu ja siirrä muutokset vähittäismyyntikanaville.</span><span class="sxs-lookup"><span data-stu-id="13227-132">After your changes are saved you need to run the Staff distribution schedule to push the changes to retail channels.</span></span>  


