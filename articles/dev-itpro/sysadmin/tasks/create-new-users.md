---
title: Uusien käyttäjien luominen
description: Käyttäjät ovat organisaation sisäisiä käyttäjiä tai ulkoisia asiakkaita ja toimittajia, jotka tarvitsevat järjestelmän käyttöoikeuden töidensä tekemiseen.
author: maertenm
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysUserManagement, SysDataAreaSelectLookup, SysSecUserAddRoles, SysUserMSODSUserImport
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: maertenm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 89e492ef5030dd28020094152259b615010aa676
ms.sourcegitcommit: 16bfa0fd08feec1647829630401ce62ce2ffa1a4
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/02/2019
ms.locfileid: "1851308"
---
# <a name="create-new-users"></a><span data-ttu-id="ad294-103">Uusien käyttäjien luominen</span><span class="sxs-lookup"><span data-stu-id="ad294-103">Create new users</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="ad294-104">Käyttäjät ovat organisaation sisäisiä käyttäjiä tai ulkoisia asiakkaita ja toimittajia, jotka tarvitsevat järjestelmän käyttöoikeuden töidensä tekemiseen.</span><span class="sxs-lookup"><span data-stu-id="ad294-104">Users are internal employees of your organization, or external customers and vendors, who require access to the system to perform their jobs.</span></span> <span data-ttu-id="ad294-105">Järjestelmänvalvojat voivat lisätä käyttäjiä järjestelmään suorittamalla tämän menettelyn.</span><span class="sxs-lookup"><span data-stu-id="ad294-105">System administrators can complete this procedure to add users to the system.</span></span> <span data-ttu-id="ad294-106">Tämän menettelyn luomisessa käytetty esittely-yritys on USMF.</span><span class="sxs-lookup"><span data-stu-id="ad294-106">The demo data company used to create this procedure is USMF.</span></span> 


## <a name="add-a-new-user"></a><span data-ttu-id="ad294-107">Lisää uusi käyttäjä</span><span class="sxs-lookup"><span data-stu-id="ad294-107">Add a new user</span></span>
1. <span data-ttu-id="ad294-108">Valitse Järjestelmänhallinta > Käyttäjät > Käyttäjät.</span><span class="sxs-lookup"><span data-stu-id="ad294-108">Go to System administration > Users > Users.</span></span>
2. <span data-ttu-id="ad294-109">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="ad294-109">Click New.</span></span>
3. <span data-ttu-id="ad294-110">Kirjoita Käyttäjätunnus-kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="ad294-110">In the User ID field, type a value.</span></span>
    * <span data-ttu-id="ad294-111">Anna käyttäjän yksilöllinen tunniste.</span><span class="sxs-lookup"><span data-stu-id="ad294-111">Enter a unique identifier for the user.</span></span> <span data-ttu-id="ad294-112">Käyttäjätunnus on pakollinen.</span><span class="sxs-lookup"><span data-stu-id="ad294-112">A user ID is required.</span></span>  
4. <span data-ttu-id="ad294-113">Kirjoita Käyttäjän nimi -kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="ad294-113">In the User name field, type a value.</span></span>
    * <span data-ttu-id="ad294-114">Anna käyttäjän nimi.</span><span class="sxs-lookup"><span data-stu-id="ad294-114">Enter the user's name.</span></span>  
5. <span data-ttu-id="ad294-115">Kirjoita Toimialue-kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="ad294-115">In the Domain field, type a value.</span></span>
    * <span data-ttu-id="ad294-116">Anna käyttäjän toimialue.</span><span class="sxs-lookup"><span data-stu-id="ad294-116">Enter the user's domain.</span></span>  
6. <span data-ttu-id="ad294-117">Kirjoita Alias-kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="ad294-117">In the Alias field, type a value.</span></span>
    * <span data-ttu-id="ad294-118">Anna käyttäjän alias.</span><span class="sxs-lookup"><span data-stu-id="ad294-118">Enter the user's alias.</span></span>  
7. <span data-ttu-id="ad294-119">Avaa haku napsauttamalla Yritys-kentässä avattavan valikon painiketta.</span><span class="sxs-lookup"><span data-stu-id="ad294-119">In the Company field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="ad294-120">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="ad294-120">In the list, find and select the desired record.</span></span>
9. <span data-ttu-id="ad294-121">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="ad294-121">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="ad294-122">Valitse käyttäjän yritys</span><span class="sxs-lookup"><span data-stu-id="ad294-122">Select the user's company</span></span>  
10. <span data-ttu-id="ad294-123">Valitse Määritä rooleja.</span><span class="sxs-lookup"><span data-stu-id="ad294-123">Click Assign roles.</span></span>
11. <span data-ttu-id="ad294-124">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="ad294-124">In the list, find and select the desired record.</span></span>
12. <span data-ttu-id="ad294-125">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="ad294-125">Click OK.</span></span>
13. <span data-ttu-id="ad294-126">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="ad294-126">Click Save.</span></span>

## <a name="import-users"></a><span data-ttu-id="ad294-127">Tuo käyttäjiä</span><span class="sxs-lookup"><span data-stu-id="ad294-127">Import users</span></span>
1. <span data-ttu-id="ad294-128">Valitse Tuo käyttäjiä.</span><span class="sxs-lookup"><span data-stu-id="ad294-128">Click Import users.</span></span>
2. <span data-ttu-id="ad294-129">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="ad294-129">In the list, mark the selected row.</span></span>
3. <span data-ttu-id="ad294-130">Valitse Tuo käyttäjiä.</span><span class="sxs-lookup"><span data-stu-id="ad294-130">Click Import users.</span></span>
4. <span data-ttu-id="ad294-131">Valitse Sulje.</span><span class="sxs-lookup"><span data-stu-id="ad294-131">Click Close.</span></span>

