---
title: Luo myyntipisteen käyttöoikeusryhmät
description: Tässä menettelyssä kerrotaan, miten myyntipisteen käyttöoikeusryhmä luodaan.
author: scott-tucker
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailPosPermissionGroup, HcmJob
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: scotttuc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1b30c9a1d7fe4598695423ba700ebc88a794a49c
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/15/2019
ms.locfileid: "1566361"
---
# <a name="create-pos-permission-groups"></a><span data-ttu-id="8bc9c-103">Luo myyntipisteen käyttöoikeusryhmät</span><span class="sxs-lookup"><span data-stu-id="8bc9c-103">Create POS permission groups</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="8bc9c-104">Tässä menettelyssä kerrotaan, miten myyntipisteen käyttöoikeusryhmä luodaan.</span><span class="sxs-lookup"><span data-stu-id="8bc9c-104">This procedure will show how to create a POS permission group.</span></span> <span data-ttu-id="8bc9c-105">Tämän tehtävän luomisessa käytetty USRT-yrityksen demotietoja.</span><span class="sxs-lookup"><span data-stu-id="8bc9c-105">The demo data company used to create this task is USRT.</span></span> <span data-ttu-id="8bc9c-106">Tämä tehtävä on tarkoitettu vähittäismyynnin toiminnoista vastaavan johtajan roolille.</span><span class="sxs-lookup"><span data-stu-id="8bc9c-106">This task is intended for the Retail operations manager role.</span></span>

1. <span data-ttu-id="8bc9c-107">Siirry Käyttöoikeusryhmät-kohtaan.</span><span class="sxs-lookup"><span data-stu-id="8bc9c-107">Go to Permission groups.</span></span>
2. <span data-ttu-id="8bc9c-108">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="8bc9c-108">Click New.</span></span>
3. <span data-ttu-id="8bc9c-109">Syötä Myyntipisteen käyttöoikeusryhmän tunnus -kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="8bc9c-109">In the POS permission group ID field, type a value.</span></span>
4. <span data-ttu-id="8bc9c-110">Kirjoita arvo Kuvaus-kenttään.</span><span class="sxs-lookup"><span data-stu-id="8bc9c-110">In the Description field, type a value.</span></span>
5. <span data-ttu-id="8bc9c-111">Valitse Näytä aikamerkinnät -kentässä Kyllä.</span><span class="sxs-lookup"><span data-stu-id="8bc9c-111">Select Yes in the View time clock entries field.</span></span>
    * <span data-ttu-id="8bc9c-112">Voit ottaa käyttöön myyntipisteen käyttöoikeusryhmän käyttöoikeuksia tai poistaa niitä käytöstä.</span><span class="sxs-lookup"><span data-stu-id="8bc9c-112">You can now enable or disable various permissions for your POS Permission group.</span></span> <span data-ttu-id="8bc9c-113">Joillekin käyttöoikeuksille voi määrittää arvon, jonka avulla arvioidaan, voiko myyntipisteen käyttäjä suorittaa toiminnon.</span><span class="sxs-lookup"><span data-stu-id="8bc9c-113">For some permission you can set a value that will be used to evaluate if the POS user can perform the action.</span></span>  <span data-ttu-id="8bc9c-114">Tässä tehtävän ohjauksessa otetaan käyttöön joitakin käyttöoikeuksia, jotka voidaan antaa kassalle.</span><span class="sxs-lookup"><span data-stu-id="8bc9c-114">This task guide enables a few permission that might be given to a cashier.</span></span>  
6. <span data-ttu-id="8bc9c-115">Valitse Salli tilauksen luominen -kentässä Kyllä.</span><span class="sxs-lookup"><span data-stu-id="8bc9c-115">Select Yes in the Allow create order field.</span></span>
7. <span data-ttu-id="8bc9c-116">Valitse Salli tilauksen muokkaaminen -kentässä Kyllä.</span><span class="sxs-lookup"><span data-stu-id="8bc9c-116">Select Yes in the Allow edit order field.</span></span>
8. <span data-ttu-id="8bc9c-117">Valitse Salli tilauksen noutaminen -kentässä Kyllä.</span><span class="sxs-lookup"><span data-stu-id="8bc9c-117">Select Yes in the Allow retrieve order field.</span></span>
9. <span data-ttu-id="8bc9c-118">Valitse Salli salasanan vaihtaminen -kentässä Kyllä.</span><span class="sxs-lookup"><span data-stu-id="8bc9c-118">Select Yes in the Allow password change field.</span></span>
10. <span data-ttu-id="8bc9c-119">Valitse Salli piilottava sulkeminen -kentässä Kyllä.</span><span class="sxs-lookup"><span data-stu-id="8bc9c-119">Select Yes in the Allow blind close field.</span></span>
11. <span data-ttu-id="8bc9c-120">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="8bc9c-120">Click Save.</span></span>
    * <span data-ttu-id="8bc9c-121">Kun muutokset on tallennettu, suorita henkilökunnan jakeluaikataulu ja siirrä muutokset vähittäismyyntikanaville.</span><span class="sxs-lookup"><span data-stu-id="8bc9c-121">After your changes are saved you need to run the Staff distribution schedule to push the changes to retail channels.</span></span>  
12. <span data-ttu-id="8bc9c-122">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="8bc9c-122">Close the page.</span></span>
13. <span data-ttu-id="8bc9c-123">Siirry Työt-kohtaan.</span><span class="sxs-lookup"><span data-stu-id="8bc9c-123">Go to Jobs.</span></span>
    * <span data-ttu-id="8bc9c-124">Seuraavaksi liitetään myyntipisteen käyttöoikeusryhmä työhön.</span><span class="sxs-lookup"><span data-stu-id="8bc9c-124">Next we will assign the POS permission group to a Job.</span></span>  
14. <span data-ttu-id="8bc9c-125">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="8bc9c-125">In the list, find and select the desired record.</span></span>
15. <span data-ttu-id="8bc9c-126">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="8bc9c-126">In the list, click the link in the selected row.</span></span>
16. <span data-ttu-id="8bc9c-127">Valitse Muokkaa.</span><span class="sxs-lookup"><span data-stu-id="8bc9c-127">Click Edit.</span></span>
17. <span data-ttu-id="8bc9c-128">Laajenna Työn luokittelu -osa.</span><span class="sxs-lookup"><span data-stu-id="8bc9c-128">Expand the Job classification section.</span></span>
18. <span data-ttu-id="8bc9c-129">Syötä tai valitse arvo Myyntipisteen käyttöoikeusryhmä -kentässä.</span><span class="sxs-lookup"><span data-stu-id="8bc9c-129">In the POS permission group field, enter or select a value.</span></span>
    * <span data-ttu-id="8bc9c-130">Kaikki tämän työn toimissa olevat työntekijät käyttävät näitä myyntipisteen käyttöoikeusryhmän asetuksia, ellei työntekijöiden myyntipisteen käyttöoikeuksia ole ohitettu toimen tasolla.</span><span class="sxs-lookup"><span data-stu-id="8bc9c-130">All Workers in Positions for this Job will use this POS permission group’s settings unless the workers POS permissions have been overridden at their Position level.</span></span>  
19. <span data-ttu-id="8bc9c-131">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="8bc9c-131">Click Save.</span></span>
    * <span data-ttu-id="8bc9c-132">Kun muutokset on tallennettu, suorita henkilökunnan jakeluaikataulu ja siirrä muutokset vähittäismyyntikanaville.</span><span class="sxs-lookup"><span data-stu-id="8bc9c-132">After your changes are saved you need to run the Staff distribution schedule to push the changes to retail channels.</span></span>  

