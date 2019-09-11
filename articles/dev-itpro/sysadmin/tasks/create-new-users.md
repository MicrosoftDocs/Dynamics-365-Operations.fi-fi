---
title: Uusien käyttäjien luominen
description: Käyttäjät ovat organisaation sisäisiä käyttäjiä tai ulkoisia asiakkaita ja toimittajia, jotka tarvitsevat järjestelmän käyttöoikeuden töidensä tekemiseen.
author: maertenm
manager: AnnBe
ms.date: 07/01/2019
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
ms.openlocfilehash: a542ece226750330262e0c44427e5654fa4f6369
ms.sourcegitcommit: cbcf344b3b552acca56c3e27606eac7f2f124afe
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/22/2019
ms.locfileid: "1916481"
---
# <a name="create-new-users"></a><span data-ttu-id="f5984-103">Uusien käyttäjien luominen</span><span class="sxs-lookup"><span data-stu-id="f5984-103">Create new users</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="f5984-104">Käyttäjät ovat organisaation sisäisiä käyttäjiä tai ulkoisia asiakkaita ja toimittajia, jotka tarvitsevat järjestelmän käyttöoikeuden töidensä tekemiseen.</span><span class="sxs-lookup"><span data-stu-id="f5984-104">Users are internal employees of your organization, or external customers and vendors, who require access to the system to perform their jobs.</span></span> <span data-ttu-id="f5984-105">Järjestelmänvalvojat voivat lisätä käyttäjiä järjestelmään suorittamalla tämän menettelyn.</span><span class="sxs-lookup"><span data-stu-id="f5984-105">System administrators can complete this procedure to add users to the system.</span></span> <span data-ttu-id="f5984-106">Tämän menettelyn luomisessa käytetty esittely-yritys on USMF.</span><span class="sxs-lookup"><span data-stu-id="f5984-106">The demo data company used to create this procedure is USMF.</span></span> 


## <a name="add-a-new-user"></a><span data-ttu-id="f5984-107">Lisää uusi käyttäjä</span><span class="sxs-lookup"><span data-stu-id="f5984-107">Add a new user</span></span>
1. <span data-ttu-id="f5984-108">Valitse **Siirtymisruutu > Moduulit > Järjestelmänhallinta > Käyttäjät > Käyttäjät**.</span><span class="sxs-lookup"><span data-stu-id="f5984-108">Go to **Navigation pane > Modules > System administration > Users > Users**.</span></span>
2. <span data-ttu-id="f5984-109">Napsauta **Toimintoruudussa** **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="f5984-109">On the **Action pane**, click **New**.</span></span>
3. <span data-ttu-id="f5984-110">Kirjoita **Käyttäjätunnus**-kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="f5984-110">In the **User ID** field, type a value.</span></span> <span data-ttu-id="f5984-111">Anna käyttäjän yksilöllinen tunniste.</span><span class="sxs-lookup"><span data-stu-id="f5984-111">Enter a unique identifier for the user.</span></span> <span data-ttu-id="f5984-112">Käyttäjätunnus on pakollinen.</span><span class="sxs-lookup"><span data-stu-id="f5984-112">A user ID is required.</span></span>  
4. <span data-ttu-id="f5984-113">Kirjoita **Käyttäjän nimi** -kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="f5984-113">In the **User name** field, type a value.</span></span> <span data-ttu-id="f5984-114">Anna käyttäjän nimi.</span><span class="sxs-lookup"><span data-stu-id="f5984-114">Enter the user's name.</span></span>  
5. <span data-ttu-id="f5984-115">Kirjoita **Toimialue**-kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="f5984-115">In the **Domain** field, type a value.</span></span> <span data-ttu-id="f5984-116">Anna käyttäjän toimialue.</span><span class="sxs-lookup"><span data-stu-id="f5984-116">Enter the user's domain.</span></span>  
6. <span data-ttu-id="f5984-117">Kirjoita **Alias**-kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="f5984-117">In the **Alias** field, type a value.</span></span> <span data-ttu-id="f5984-118">Anna käyttäjän alias.</span><span class="sxs-lookup"><span data-stu-id="f5984-118">Enter the user's alias.</span></span>  
7. <span data-ttu-id="f5984-119">Avaa haku napsauttamalla **Yritys**-kentässä avattavan valikon painiketta.</span><span class="sxs-lookup"><span data-stu-id="f5984-119">In the **Company** field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="f5984-120">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="f5984-120">In the list, find and select the desired record.</span></span> 
9. <span data-ttu-id="f5984-121">Valitse **Käyttäjän roolit** -osassa **Määritä roolit**.</span><span class="sxs-lookup"><span data-stu-id="f5984-121">In the **User's roles** section, click **Assign roles**.</span></span>
10. <span data-ttu-id="f5984-122">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="f5984-122">In the list, find and select the desired record.</span></span>
11. <span data-ttu-id="f5984-123">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="f5984-123">Click **OK**.</span></span>
12. <span data-ttu-id="f5984-124">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="f5984-124">Click **Save**.</span></span>

## <a name="import-users"></a><span data-ttu-id="f5984-125">Tuo käyttäjiä</span><span class="sxs-lookup"><span data-stu-id="f5984-125">Import users</span></span>
1. <span data-ttu-id="f5984-126">Valitse **toimintoruudussa** **Tuo käyttäjiä**.</span><span class="sxs-lookup"><span data-stu-id="f5984-126">On the **Action pane**, click **Import users**.</span></span>
2. <span data-ttu-id="f5984-127">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="f5984-127">In the list, mark the selected row.</span></span>
3. <span data-ttu-id="f5984-128">Valitse **Tuo käyttäjiä**.</span><span class="sxs-lookup"><span data-stu-id="f5984-128">Click **Import users**.</span></span>
4. <span data-ttu-id="f5984-129">Valitse **Sulje**.</span><span class="sxs-lookup"><span data-stu-id="f5984-129">Click **Close**.</span></span>

