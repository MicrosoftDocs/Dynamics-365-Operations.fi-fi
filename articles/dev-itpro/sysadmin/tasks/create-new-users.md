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
ms.reviewer: margoc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: maertenm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 12cf223d262c4e0f2a195e95c83a00fc1a3f07e5
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/29/2019
ms.locfileid: "361955"
---
# <a name="create-new-users"></a><span data-ttu-id="4a63a-103">Uusien käyttäjien luominen</span><span class="sxs-lookup"><span data-stu-id="4a63a-103">Create new users</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="4a63a-104">Käyttäjät ovat organisaation sisäisiä käyttäjiä tai ulkoisia asiakkaita ja toimittajia, jotka tarvitsevat järjestelmän käyttöoikeuden töidensä tekemiseen.</span><span class="sxs-lookup"><span data-stu-id="4a63a-104">Users are internal employees of your organization, or external customers and vendors, who require access to the system to perform their jobs.</span></span> <span data-ttu-id="4a63a-105">Järjestelmänvalvojat voivat lisätä käyttäjiä järjestelmään suorittamalla tämän menettelyn.</span><span class="sxs-lookup"><span data-stu-id="4a63a-105">System administrators can complete this procedure to add users to the system.</span></span> <span data-ttu-id="4a63a-106">Tämän menettelyn luomisessa käytetty esittely-yritys on USMF.</span><span class="sxs-lookup"><span data-stu-id="4a63a-106">The demo data company used to create this procedure is USMF.</span></span> 


## <a name="add-a-new-user"></a><span data-ttu-id="4a63a-107">Lisää uusi käyttäjä</span><span class="sxs-lookup"><span data-stu-id="4a63a-107">Add a new user</span></span>
1. <span data-ttu-id="4a63a-108">Valitse Järjestelmänhallinta > Käyttäjät > Käyttäjät.</span><span class="sxs-lookup"><span data-stu-id="4a63a-108">Go to System administration > Users > Users.</span></span>
2. <span data-ttu-id="4a63a-109">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="4a63a-109">Click New.</span></span>
3. <span data-ttu-id="4a63a-110">Kirjoita Käyttäjätunnus-kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="4a63a-110">In the User ID field, type a value.</span></span>
    * <span data-ttu-id="4a63a-111">Anna käyttäjän yksilöllinen tunniste.</span><span class="sxs-lookup"><span data-stu-id="4a63a-111">Enter a unique identifier for the user.</span></span> <span data-ttu-id="4a63a-112">Käyttäjätunnus on pakollinen.</span><span class="sxs-lookup"><span data-stu-id="4a63a-112">A user ID is required.</span></span>  
4. <span data-ttu-id="4a63a-113">Kirjoita Käyttäjän nimi -kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="4a63a-113">In the User name field, type a value.</span></span>
    * <span data-ttu-id="4a63a-114">Anna käyttäjän nimi.</span><span class="sxs-lookup"><span data-stu-id="4a63a-114">Enter the user's name.</span></span>  
5. <span data-ttu-id="4a63a-115">Kirjoita Toimialue-kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="4a63a-115">In the Domain field, type a value.</span></span>
    * <span data-ttu-id="4a63a-116">Anna käyttäjän toimialue.</span><span class="sxs-lookup"><span data-stu-id="4a63a-116">Enter the user's domain.</span></span>  
6. <span data-ttu-id="4a63a-117">Kirjoita Alias-kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="4a63a-117">In the Alias field, type a value.</span></span>
    * <span data-ttu-id="4a63a-118">Anna käyttäjän alias.</span><span class="sxs-lookup"><span data-stu-id="4a63a-118">Enter the user's alias.</span></span>  
7. <span data-ttu-id="4a63a-119">Avaa haku napsauttamalla Yritys-kentässä avattavan valikon painiketta.</span><span class="sxs-lookup"><span data-stu-id="4a63a-119">In the Company field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="4a63a-120">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="4a63a-120">In the list, find and select the desired record.</span></span>
9. <span data-ttu-id="4a63a-121">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="4a63a-121">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="4a63a-122">Valitse käyttäjän yritys</span><span class="sxs-lookup"><span data-stu-id="4a63a-122">Select the user's company</span></span>  
10. <span data-ttu-id="4a63a-123">Valitse Määritä rooleja.</span><span class="sxs-lookup"><span data-stu-id="4a63a-123">Click Assign roles.</span></span>
11. <span data-ttu-id="4a63a-124">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="4a63a-124">In the list, find and select the desired record.</span></span>
12. <span data-ttu-id="4a63a-125">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="4a63a-125">Click OK.</span></span>
13. <span data-ttu-id="4a63a-126">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="4a63a-126">Click Save.</span></span>

## <a name="import-users"></a><span data-ttu-id="4a63a-127">Tuo käyttäjiä</span><span class="sxs-lookup"><span data-stu-id="4a63a-127">Import users</span></span>
1. <span data-ttu-id="4a63a-128">Valitse Tuo käyttäjiä.</span><span class="sxs-lookup"><span data-stu-id="4a63a-128">Click Import users.</span></span>
2. <span data-ttu-id="4a63a-129">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="4a63a-129">In the list, mark the selected row.</span></span>
3. <span data-ttu-id="4a63a-130">Valitse Tuo käyttäjiä.</span><span class="sxs-lookup"><span data-stu-id="4a63a-130">Click Import users.</span></span>
4. <span data-ttu-id="4a63a-131">Valitse Sulje.</span><span class="sxs-lookup"><span data-stu-id="4a63a-131">Click Close.</span></span>

