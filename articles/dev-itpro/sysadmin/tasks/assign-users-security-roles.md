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
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: maertenm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4c0afd0f5754e59307a82af9c9700b36c31edcc4
ms.sourcegitcommit: 16bfa0fd08feec1647829630401ce62ce2ffa1a4
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/02/2019
ms.locfileid: "1851356"
---
# <a name="assign-users-to-security-roles"></a><span data-ttu-id="4cf4d-103">Käyttäjien liittäminen käyttöoikeusrooleihin</span><span class="sxs-lookup"><span data-stu-id="4cf4d-103">Assign users to security roles</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="4cf4d-104">Microsoft Dynamics 365 for Finance and Operations, Enterprise Editionin käyttämistä varten käyttäjille on määritettävä käyttöoikeusrooleja.</span><span class="sxs-lookup"><span data-stu-id="4cf4d-104">To access Microsoft Dynamics 365 for Finance and Operations, Enterprise edition, users must be assigned to security roles.</span></span> <span data-ttu-id="4cf4d-105">Tässä menettelyssä kerrotaan, kuinka järjestelmänvalvojat voivat määrittää rooleja käyttäjille automaattisesti liiketoimintatietojen perusteella.</span><span class="sxs-lookup"><span data-stu-id="4cf4d-105">This procedure explains how system administrators can assign users to roles automatically, based on business data.</span></span> <span data-ttu-id="4cf4d-106">Tämän menettelyn luomisessa käytetty esittely-yritys on USMF.</span><span class="sxs-lookup"><span data-stu-id="4cf4d-106">The demo data company used to create this procedure is USMF.</span></span>


## <a name="automatically-assign-users-to-roles"></a><span data-ttu-id="4cf4d-107">Liitä käyttäjät rooleihin automaattisesti</span><span class="sxs-lookup"><span data-stu-id="4cf4d-107">Automatically assign users to roles</span></span>
1. <span data-ttu-id="4cf4d-108">Valitse **Siirtymisruutu > Moduulit > Järjestelmänhallinta > Suojaus > Määritä käyttäjät rooleihin**.</span><span class="sxs-lookup"><span data-stu-id="4cf4d-108">Go to **Navigation pane > Modules > System administration > Security > Assign users to roles**.</span></span>
2. <span data-ttu-id="4cf4d-109">Valitse puusta Taloushallintopäällikkö.</span><span class="sxs-lookup"><span data-stu-id="4cf4d-109">In the tree, select 'Accounting supervisor'.</span></span> <span data-ttu-id="4cf4d-110">Valitse rooli, jolle haluat konfiguroida säännön.</span><span class="sxs-lookup"><span data-stu-id="4cf4d-110">Select the role that you want to configure the rule for.</span></span> <span data-ttu-id="4cf4d-111">Valitse tässä esimerkissä Taloushallintopäällikkö.</span><span class="sxs-lookup"><span data-stu-id="4cf4d-111">In this example, select Accounting supervisor.</span></span> 
3. <span data-ttu-id="4cf4d-112">Avaa avattava luettelo valitsemalla **Lisää sääntö**.</span><span class="sxs-lookup"><span data-stu-id="4cf4d-112">Click **Add rule** to open the drop dialog.</span></span>
4. <span data-ttu-id="4cf4d-113">Etsi haluamasi tietue **Valitse kysely** -luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="4cf4d-113">In the **Select a query**list, find and select the desired record.</span></span> <span data-ttu-id="4cf4d-114">Valitse tämä tässä säännössä käytettävä kysely.</span><span class="sxs-lookup"><span data-stu-id="4cf4d-114">Select the query to use for this rule.</span></span>  
5. <span data-ttu-id="4cf4d-115">Napsauta **Jäsenyyssäännön nimi** -luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="4cf4d-115">In the **Membership rule name** list, click the link in the selected row.</span></span>
6. <span data-ttu-id="4cf4d-116">Valitse **Muokkaa kyselyä**.</span><span class="sxs-lookup"><span data-stu-id="4cf4d-116">Click **Edit query**.</span></span> <span data-ttu-id="4cf4d-117">Muokkaa kyselyä tarvittaessa.</span><span class="sxs-lookup"><span data-stu-id="4cf4d-117">Edit the query, as needed.</span></span>  
7. <span data-ttu-id="4cf4d-118">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="4cf4d-118">Click **OK**.</span></span>

## <a name="exclude-users-from-automatic-role-assignment"></a><span data-ttu-id="4cf4d-119">Sulje käyttäjät pois automaattisesta roolin määrityksestä</span><span class="sxs-lookup"><span data-stu-id="4cf4d-119">Exclude users from automatic role assignment</span></span>
1. <span data-ttu-id="4cf4d-120">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="4cf4d-120">Close the page.</span></span>
2. <span data-ttu-id="4cf4d-121">Valitse **Siirtymisruutu > Moduulit > Järjestelmänhallinta > Suojaus > Määritä käyttäjät rooleihin**.</span><span class="sxs-lookup"><span data-stu-id="4cf4d-121">Go to **Navigation pane > Modules > System administration > Security > Assign users to roles**.</span></span>
3. <span data-ttu-id="4cf4d-122">Valitse puusta Taloushallintopäällikkö.</span><span class="sxs-lookup"><span data-stu-id="4cf4d-122">In the tree, select 'Accounting supervisor'.</span></span> <span data-ttu-id="4cf4d-123">Valitse rooli.</span><span class="sxs-lookup"><span data-stu-id="4cf4d-123">Select a role.</span></span> <span data-ttu-id="4cf4d-124">Valitse tässä esimerkissä Taloushallintopäällikkö.</span><span class="sxs-lookup"><span data-stu-id="4cf4d-124">For this example, select Accounting supervisor.</span></span>  
4. <span data-ttu-id="4cf4d-125">Valitse **Roolille määritetyt käyttäjät** -valikossa **Määritä tai sulje pois käyttäjiä manuaalisesti**.</span><span class="sxs-lookup"><span data-stu-id="4cf4d-125">In the **Users assigned to role** menu, select **Manually assign / exclude users**.</span></span>
5. <span data-ttu-id="4cf4d-126">Merkitse valittu rivi **Määritä käyttäjiä rooliin tai sulje käyttäjiä pois roolista** -luettelossa.</span><span class="sxs-lookup"><span data-stu-id="4cf4d-126">In the **Assign users to or exclude users from role** list, mark the selected row.</span></span> <span data-ttu-id="4cf4d-127">Valitse käyttäjä.</span><span class="sxs-lookup"><span data-stu-id="4cf4d-127">Select a user.</span></span>  
6. <span data-ttu-id="4cf4d-128">Valitse **toimintoruudussa** **Sulje pois roolista**.</span><span class="sxs-lookup"><span data-stu-id="4cf4d-128">On the **Action pane**, select **Exclude from role**.</span></span>
    
    <span data-ttu-id="4cf4d-129">Sulje valitut käyttäjät pois roolista valitsemalla **Sulje pois roolista**.</span><span class="sxs-lookup"><span data-stu-id="4cf4d-129">Click **Exclude from role** to exclude the selected users from the role.</span></span> <span data-ttu-id="4cf4d-130">Ohitukset voit poistaa valitsemalla käyttäjät, joiden ohituksen haluat poistaa, ja valitsemalla sitten **Palauta tila**.</span><span class="sxs-lookup"><span data-stu-id="4cf4d-130">To remove exclusions, select the users that you want to remove exclusions for, and then click **Reset status**.</span></span> <span data-ttu-id="4cf4d-131">Kun poistat ohituksen palauttamalla käyttäjän tilan, käyttäjän rooli määritetään uudelleen automaattisesti.</span><span class="sxs-lookup"><span data-stu-id="4cf4d-131">When you remove an exclusion by resetting the user’s status, the user’s role is again assigned automatically.</span></span> <span data-ttu-id="4cf4d-132">Käyttäjää ei kuitenkaan määritetä välittömästi rooliin tai suljeta siitä pois kun palautat tilan.</span><span class="sxs-lookup"><span data-stu-id="4cf4d-132">However, the user is not immediately assigned to the role or excluded from the role when you reset the status.</span></span> <span data-ttu-id="4cf4d-133">Sen sijaan käyttäjä määritetään rooliin tai poistetaan siitä seuraavalla kerralla, kun automaattisen roolinmäärityksen säännöt ajetaan.</span><span class="sxs-lookup"><span data-stu-id="4cf4d-133">Instead, the user is either assigned to the role or removed from the role the next time that the rules for automatic role assignment are run.</span></span>  
