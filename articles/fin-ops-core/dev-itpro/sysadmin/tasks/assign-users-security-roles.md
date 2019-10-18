---
title: Käyttäjien liittäminen käyttöoikeusrooleihin
description: Finance and Operations -sovellusten käyttö edellyttää, että käyttäjille on määritetty käyttöoikeusroolit.
author: ChrisGarty
manager: AnnBe
ms.date: 09/16/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysSecRolesEditUsers, SysSecAssignmentQueryLookup, SysQueryForm, SysSecRoleExcludeUsers
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a4daecc1acd589cd1656402244e5325382a407e7
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/27/2019
ms.locfileid: "2180964"
---
# <a name="assign-users-to-security-roles"></a><span data-ttu-id="5a880-103">Käyttäjien liittäminen käyttöoikeusrooleihin</span><span class="sxs-lookup"><span data-stu-id="5a880-103">Assign users to security roles</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="5a880-104">Muiden kuin yhteisten toimintojen käyttöä varten käyttäjät on määritettävä käyttöoikeusrooleihin.</span><span class="sxs-lookup"><span data-stu-id="5a880-104">To use anything other than common capabilities, users must be assigned to security roles.</span></span> <span data-ttu-id="5a880-105">Tässä menettelyssä kerrotaan, kuinka järjestelmänvalvojat voivat automaattisesti määrittää rooleja käyttäjille liiketoimintatietojen perusteella.</span><span class="sxs-lookup"><span data-stu-id="5a880-105">This procedure explains how system administrators can automatically assign users to roles, based on business data.</span></span> 

## <a name="automatically-assign-users-to-roles"></a><span data-ttu-id="5a880-106">Liitä käyttäjät rooleihin automaattisesti</span><span class="sxs-lookup"><span data-stu-id="5a880-106">Automatically assign users to roles</span></span>
1. <span data-ttu-id="5a880-107">Valitse **Siirtymisruutu > Moduulit > Järjestelmänhallinta > Suojaus > Määritä käyttäjät rooleihin**.</span><span class="sxs-lookup"><span data-stu-id="5a880-107">Go to **Navigation pane > Modules > System administration > Security > Assign users to roles**.</span></span>
2. <span data-ttu-id="5a880-108">Valitse puusta Taloushallintopäällikkö.</span><span class="sxs-lookup"><span data-stu-id="5a880-108">In the tree, select 'Accounting supervisor'.</span></span> <span data-ttu-id="5a880-109">Valitse rooli, jolle haluat konfiguroida säännön.</span><span class="sxs-lookup"><span data-stu-id="5a880-109">Select the role that you want to configure the rule for.</span></span> <span data-ttu-id="5a880-110">Valitse tässä esimerkissä Taloushallintopäällikkö.</span><span class="sxs-lookup"><span data-stu-id="5a880-110">In this example, select Accounting supervisor.</span></span> 
3. <span data-ttu-id="5a880-111">Avaa avattava luettelo valitsemalla **Lisää sääntö**.</span><span class="sxs-lookup"><span data-stu-id="5a880-111">Click **Add rule** to open the drop dialog.</span></span>
4. <span data-ttu-id="5a880-112">Etsi haluamasi tietue **Valitse kysely** -luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="5a880-112">In the **Select a query**list, find and select the desired record.</span></span> <span data-ttu-id="5a880-113">Valitse tämä tässä säännössä käytettävä kysely.</span><span class="sxs-lookup"><span data-stu-id="5a880-113">Select the query to use for this rule.</span></span>  
5. <span data-ttu-id="5a880-114">Napsauta **Jäsenyyssäännön nimi** -luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="5a880-114">In the **Membership rule name** list, click the link in the selected row.</span></span>
6. <span data-ttu-id="5a880-115">Valitse **Muokkaa kyselyä**.</span><span class="sxs-lookup"><span data-stu-id="5a880-115">Click **Edit query**.</span></span> <span data-ttu-id="5a880-116">Muokkaa kyselyä tarvittaessa.</span><span class="sxs-lookup"><span data-stu-id="5a880-116">Edit the query, as needed.</span></span>  
7. <span data-ttu-id="5a880-117">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="5a880-117">Click **OK**.</span></span>

## <a name="exclude-users-from-automatic-role-assignment"></a><span data-ttu-id="5a880-118">Sulje käyttäjät pois automaattisesta roolin määrityksestä</span><span class="sxs-lookup"><span data-stu-id="5a880-118">Exclude users from automatic role assignment</span></span>
1. <span data-ttu-id="5a880-119">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="5a880-119">Close the page.</span></span>
2. <span data-ttu-id="5a880-120">Valitse **Siirtymisruutu > Moduulit > Järjestelmänhallinta > Suojaus > Määritä käyttäjät rooleihin**.</span><span class="sxs-lookup"><span data-stu-id="5a880-120">Go to **Navigation pane > Modules > System administration > Security > Assign users to roles**.</span></span>
3. <span data-ttu-id="5a880-121">Valitse puusta Taloushallintopäällikkö.</span><span class="sxs-lookup"><span data-stu-id="5a880-121">In the tree, select 'Accounting supervisor'.</span></span> <span data-ttu-id="5a880-122">Valitse rooli.</span><span class="sxs-lookup"><span data-stu-id="5a880-122">Select a role.</span></span> <span data-ttu-id="5a880-123">Valitse tässä esimerkissä Taloushallintopäällikkö.</span><span class="sxs-lookup"><span data-stu-id="5a880-123">For this example, select Accounting supervisor.</span></span>  
4. <span data-ttu-id="5a880-124">Valitse **Roolille määritetyt käyttäjät** -valikossa **Määritä tai sulje pois käyttäjiä manuaalisesti**.</span><span class="sxs-lookup"><span data-stu-id="5a880-124">In the **Users assigned to role** menu, select **Manually assign / exclude users**.</span></span>
5. <span data-ttu-id="5a880-125">Merkitse valittu rivi **Määritä käyttäjiä rooliin tai sulje käyttäjiä pois roolista** -luettelossa.</span><span class="sxs-lookup"><span data-stu-id="5a880-125">In the **Assign users to or exclude users from role** list, mark the selected row.</span></span> <span data-ttu-id="5a880-126">Valitse käyttäjä.</span><span class="sxs-lookup"><span data-stu-id="5a880-126">Select a user.</span></span>  
6. <span data-ttu-id="5a880-127">Valitse **toimintoruudussa** **Sulje pois roolista**.</span><span class="sxs-lookup"><span data-stu-id="5a880-127">On the **Action pane**, select **Exclude from role**.</span></span>
    
    <span data-ttu-id="5a880-128">Sulje valitut käyttäjät pois roolista valitsemalla **Sulje pois roolista**.</span><span class="sxs-lookup"><span data-stu-id="5a880-128">Click **Exclude from role** to exclude the selected users from the role.</span></span> <span data-ttu-id="5a880-129">Ohitukset voit poistaa valitsemalla käyttäjät, joiden ohituksen haluat poistaa, ja valitsemalla sitten **Palauta tila**.</span><span class="sxs-lookup"><span data-stu-id="5a880-129">To remove exclusions, select the users that you want to remove exclusions for, and then click **Reset status**.</span></span> <span data-ttu-id="5a880-130">Kun poistat ohituksen palauttamalla käyttäjän tilan, käyttäjän rooli määritetään uudelleen automaattisesti.</span><span class="sxs-lookup"><span data-stu-id="5a880-130">When you remove an exclusion by resetting the user’s status, the user’s role is again assigned automatically.</span></span> <span data-ttu-id="5a880-131">Käyttäjää ei kuitenkaan määritetä välittömästi rooliin tai suljeta siitä pois kun palautat tilan.</span><span class="sxs-lookup"><span data-stu-id="5a880-131">However, the user is not immediately assigned to the role or excluded from the role when you reset the status.</span></span> <span data-ttu-id="5a880-132">Sen sijaan käyttäjä määritetään rooliin tai poistetaan siitä seuraavalla kerralla, kun automaattisen roolinmäärityksen säännöt ajetaan.</span><span class="sxs-lookup"><span data-stu-id="5a880-132">Instead, the user is either assigned to the role or removed from the role the next time that the rules for automatic role assignment are run.</span></span>  
