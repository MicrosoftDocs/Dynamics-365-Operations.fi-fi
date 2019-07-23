---
title: Käyttäjien liittäminen käyttöoikeusrooleihin
description: Microsoft Dynamics 365 for Finance and Operations, Enterprise Editionin käyttämistä varten käyttäjille on määritettävä käyttöoikeusrooleja.
author: maertenm
manager: AnnBe
ms.date: 06/21/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysSecRolesEditUsers, SysSecAssignmentQueryLookup, SysQueryForm, SysSecRoleExcludeUsers
audience: Application User
ms.reviewer: margoc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: maertenm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ab9f2f5ea07ae1d616c48dffa8810b966f7dbb2f
ms.sourcegitcommit: 33e98f89294086334fe9c0a350abb6a52ef9dacb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/28/2019
ms.locfileid: "1711128"
---
# <a name="assign-users-to-security-roles"></a><span data-ttu-id="43efe-103">Käyttäjien liittäminen käyttöoikeusrooleihin</span><span class="sxs-lookup"><span data-stu-id="43efe-103">Assign users to security roles</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="43efe-104">Microsoft Dynamics 365 for Finance and Operations, Enterprise Editionin käyttämistä varten käyttäjille on määritettävä käyttöoikeusrooleja.</span><span class="sxs-lookup"><span data-stu-id="43efe-104">To access Microsoft Dynamics 365 for Finance and Operations, Enterprise edition, users must be assigned to security roles.</span></span> <span data-ttu-id="43efe-105">Tässä menettelyssä kerrotaan, kuinka järjestelmänvalvojat voivat määrittää rooleja käyttäjille automaattisesti liiketoimintatietojen perusteella.</span><span class="sxs-lookup"><span data-stu-id="43efe-105">This procedure explains how system administrators can assign users to roles automatically, based on business data.</span></span> <span data-ttu-id="43efe-106">Tämän menettelyn luomisessa käytetty esittely-yritys on USMF.</span><span class="sxs-lookup"><span data-stu-id="43efe-106">The demo data company used to create this procedure is USMF.</span></span>


## <a name="automatically-assign-users-to-roles"></a><span data-ttu-id="43efe-107">Liitä käyttäjät rooleihin automaattisesti</span><span class="sxs-lookup"><span data-stu-id="43efe-107">Automatically assign users to roles</span></span>
1. <span data-ttu-id="43efe-108">Valitse **Siirtymisruutu > Moduulit > Järjestelmänhallinta > Suojaus > Määritä käyttäjät rooleihin**.</span><span class="sxs-lookup"><span data-stu-id="43efe-108">Go to **Navigation pane > Modules > System administration > Security > Assign users to roles**.</span></span>
2. <span data-ttu-id="43efe-109">Valitse puusta Taloushallintopäällikkö.</span><span class="sxs-lookup"><span data-stu-id="43efe-109">In the tree, select 'Accounting supervisor'.</span></span> <span data-ttu-id="43efe-110">Valitse rooli, jolle haluat konfiguroida säännön.</span><span class="sxs-lookup"><span data-stu-id="43efe-110">Select the role that you want to configure the rule for.</span></span> <span data-ttu-id="43efe-111">Valitse tässä esimerkissä Taloushallintopäällikkö.</span><span class="sxs-lookup"><span data-stu-id="43efe-111">In this example, select Accounting supervisor.</span></span> 
3. <span data-ttu-id="43efe-112">Avaa avattava luettelo valitsemalla **Lisää sääntö**.</span><span class="sxs-lookup"><span data-stu-id="43efe-112">Click **Add rule** to open the drop dialog.</span></span>
4. <span data-ttu-id="43efe-113">Etsi haluamasi tietue **Valitse kysely** -luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="43efe-113">In the **Select a query**list, find and select the desired record.</span></span> <span data-ttu-id="43efe-114">Valitse tämä tässä säännössä käytettävä kysely.</span><span class="sxs-lookup"><span data-stu-id="43efe-114">Select the query to use for this rule.</span></span>  
5. <span data-ttu-id="43efe-115">Napsauta **Jäsenyyssäännön nimi** -luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="43efe-115">In the **Membership rule name** list, click the link in the selected row.</span></span>
6. <span data-ttu-id="43efe-116">Valitse **Muokkaa kyselyä**.</span><span class="sxs-lookup"><span data-stu-id="43efe-116">Click **Edit query**.</span></span> <span data-ttu-id="43efe-117">Muokkaa kyselyä tarvittaessa.</span><span class="sxs-lookup"><span data-stu-id="43efe-117">Edit the query, as needed.</span></span>  
7. <span data-ttu-id="43efe-118">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="43efe-118">Click **OK**.</span></span>

## <a name="exclude-users-from-automatic-role-assignment"></a><span data-ttu-id="43efe-119">Sulje käyttäjät pois automaattisesta roolin määrityksestä</span><span class="sxs-lookup"><span data-stu-id="43efe-119">Exclude users from automatic role assignment</span></span>
1. <span data-ttu-id="43efe-120">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="43efe-120">Close the page.</span></span>
2. <span data-ttu-id="43efe-121">Valitse **Siirtymisruutu > Moduulit > Järjestelmänhallinta > Suojaus > Määritä käyttäjät rooleihin**.</span><span class="sxs-lookup"><span data-stu-id="43efe-121">Go to **Navigation pane > Modules > System administration > Security > Assign users to roles**.</span></span>
3. <span data-ttu-id="43efe-122">Valitse puusta Taloushallintopäällikkö.</span><span class="sxs-lookup"><span data-stu-id="43efe-122">In the tree, select 'Accounting supervisor'.</span></span> <span data-ttu-id="43efe-123">Valitse rooli.</span><span class="sxs-lookup"><span data-stu-id="43efe-123">Select a role.</span></span> <span data-ttu-id="43efe-124">Valitse tässä esimerkissä Taloushallintopäällikkö.</span><span class="sxs-lookup"><span data-stu-id="43efe-124">For this example, select Accounting supervisor.</span></span>  
4. <span data-ttu-id="43efe-125">Valitse **Roolille määritetyt käyttäjät** -valikossa **Määritä tai sulje pois käyttäjiä manuaalisesti**.</span><span class="sxs-lookup"><span data-stu-id="43efe-125">In the **Users assigned to role** menu, select **Manually assign / exclude users**.</span></span>
5. <span data-ttu-id="43efe-126">Merkitse valittu rivi **Määritä käyttäjiä rooliin tai sulje käyttäjiä pois roolista** -luettelossa.</span><span class="sxs-lookup"><span data-stu-id="43efe-126">In the **Assign users to or exclude users from role** list, mark the selected row.</span></span> <span data-ttu-id="43efe-127">Valitse käyttäjä.</span><span class="sxs-lookup"><span data-stu-id="43efe-127">Select a user.</span></span>  
6. <span data-ttu-id="43efe-128">Valitse **toimintoruudussa** **Sulje pois roolista**.</span><span class="sxs-lookup"><span data-stu-id="43efe-128">On the **Action pane**, select **Exclude from role**.</span></span>
    
    <span data-ttu-id="43efe-129">Sulje valitut käyttäjät pois roolista valitsemalla **Sulje pois roolista**.</span><span class="sxs-lookup"><span data-stu-id="43efe-129">Click **Exclude from role** to exclude the selected users from the role.</span></span> <span data-ttu-id="43efe-130">Ohitukset voit poistaa valitsemalla käyttäjät, joiden ohituksen haluat poistaa, ja valitsemalla sitten **Palauta tila**.</span><span class="sxs-lookup"><span data-stu-id="43efe-130">To remove exclusions, select the users that you want to remove exclusions for, and then click **Reset status**.</span></span> <span data-ttu-id="43efe-131">Kun poistat ohituksen palauttamalla käyttäjän tilan, käyttäjän rooli määritetään uudelleen automaattisesti.</span><span class="sxs-lookup"><span data-stu-id="43efe-131">When you remove an exclusion by resetting the user’s status, the user’s role is again assigned automatically.</span></span> <span data-ttu-id="43efe-132">Käyttäjää ei kuitenkaan määritetä välittömästi rooliin tai suljeta siitä pois kun palautat tilan.</span><span class="sxs-lookup"><span data-stu-id="43efe-132">However, the user is not immediately assigned to the role or excluded from the role when you reset the status.</span></span> <span data-ttu-id="43efe-133">Sen sijaan käyttäjä määritetään rooliin tai poistetaan siitä seuraavalla kerralla, kun automaattisen roolinmäärityksen säännöt ajetaan.</span><span class="sxs-lookup"><span data-stu-id="43efe-133">Instead, the user is either assigned to the role or removed from the role the next time that the rules for automatic role assignment are run.</span></span>  
