---
title: Käyttäjien liittäminen käyttöoikeusrooleihin
description: Finance and Operations -sovellusten käyttö edellyttää, että käyttäjille on määritetty käyttöoikeusroolit.
author: ChrisGarty
manager: AnnBe
ms.date: 11/14/2019
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
ms.openlocfilehash: e4f4ef4535de9e371829c2d86d4fdc1400510c7b
ms.sourcegitcommit: 6aa74f66f1abd3a7977050a5339b0b17e62ff053
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/15/2019
ms.locfileid: "2807993"
---
# <a name="assign-users-to-security-roles"></a><span data-ttu-id="4f8d3-103">Käyttäjien liittäminen käyttöoikeusrooleihin</span><span class="sxs-lookup"><span data-stu-id="4f8d3-103">Assign users to security roles</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="4f8d3-104">Muiden kuin yhteisten toimintojen käyttöä varten käyttäjät on määritettävä käyttöoikeusrooleihin.</span><span class="sxs-lookup"><span data-stu-id="4f8d3-104">To use anything other than common capabilities, users must be assigned to security roles.</span></span> <span data-ttu-id="4f8d3-105">Tässä menettelyssä kerrotaan, kuinka järjestelmänvalvojat voivat automaattisesti määrittää rooleja käyttäjille liiketoimintatietojen perusteella.</span><span class="sxs-lookup"><span data-stu-id="4f8d3-105">This procedure explains how system administrators can automatically assign users to roles, based on business data.</span></span> 

## <a name="automatically-assign-users-to-roles"></a><span data-ttu-id="4f8d3-106">Liitä käyttäjät rooleihin automaattisesti</span><span class="sxs-lookup"><span data-stu-id="4f8d3-106">Automatically assign users to roles</span></span>
1. <span data-ttu-id="4f8d3-107">Valitse **Siirtymisruutu > Moduulit > Järjestelmänhallinta > Suojaus > Määritä käyttäjät rooleihin**.</span><span class="sxs-lookup"><span data-stu-id="4f8d3-107">Go to **Navigation pane > Modules > System administration > Security > Assign users to roles**.</span></span>
2. <span data-ttu-id="4f8d3-108">Valitse puusta Taloushallintopäällikkö.</span><span class="sxs-lookup"><span data-stu-id="4f8d3-108">In the tree, select 'Accounting supervisor'.</span></span> <span data-ttu-id="4f8d3-109">Valitse rooli, jolle haluat konfiguroida säännön.</span><span class="sxs-lookup"><span data-stu-id="4f8d3-109">Select the role that you want to configure the rule for.</span></span> <span data-ttu-id="4f8d3-110">Valitse tässä esimerkissä Taloushallintopäällikkö.</span><span class="sxs-lookup"><span data-stu-id="4f8d3-110">In this example, select Accounting supervisor.</span></span> 
3. <span data-ttu-id="4f8d3-111">Avaa avattava luettelo valitsemalla **Lisää sääntö**.</span><span class="sxs-lookup"><span data-stu-id="4f8d3-111">Click **Add rule** to open the drop dialog.</span></span>
4. <span data-ttu-id="4f8d3-112">Etsi haluamasi tietue **Valitse kysely** -luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="4f8d3-112">In the **Select a query**list, find and select the desired record.</span></span> <span data-ttu-id="4f8d3-113">Valitse tämä tässä säännössä käytettävä kysely.</span><span class="sxs-lookup"><span data-stu-id="4f8d3-113">Select the query to use for this rule.</span></span>  
5. <span data-ttu-id="4f8d3-114">Napsauta **Jäsenyyssäännön nimi** -luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="4f8d3-114">In the **Membership rule name** list, click the link in the selected row.</span></span>
6. <span data-ttu-id="4f8d3-115">Valitse **Muokkaa kyselyä**.</span><span class="sxs-lookup"><span data-stu-id="4f8d3-115">Click **Edit query**.</span></span> <span data-ttu-id="4f8d3-116">Muokkaa kyselyä tarvittaessa.</span><span class="sxs-lookup"><span data-stu-id="4f8d3-116">Edit the query, as needed.</span></span>  
7. <span data-ttu-id="4f8d3-117">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="4f8d3-117">Click **OK**.</span></span>
8. <span data-ttu-id="4f8d3-118">Valitse **Suorita automaattinen roolin määritys**.</span><span class="sxs-lookup"><span data-stu-id="4f8d3-118">Click **Run automatic role assignment**.</span></span>
9. <span data-ttu-id="4f8d3-119">Valitse **Siirtymisruutu > Moduulit > Järjestelmän hallinta > Käyttäjät > Käyttäjät** (mielellään erillisessä selaimen välilehdessä).</span><span class="sxs-lookup"><span data-stu-id="4f8d3-119">Go to **Navigation pane > Modules > System administration > Users > Users** (ideally in a separate browser tab).</span></span>
10. <span data-ttu-id="4f8d3-120">Vahvista, että roolien määrityskysely oli oikein, tarkistamalla eri käyttäjille määritetyt roolit.</span><span class="sxs-lookup"><span data-stu-id="4f8d3-120">Review the roles assigned to various users to confirm that the role assignment query was correct.</span></span> <span data-ttu-id="4f8d3-121">Säädä ja suorita tarvittaessa uudelleen.</span><span class="sxs-lookup"><span data-stu-id="4f8d3-121">Adjust and re-run if needed.</span></span>

## <a name="exclude-users-from-automatic-role-assignment"></a><span data-ttu-id="4f8d3-122">Sulje käyttäjät pois automaattisesta roolin määrityksestä</span><span class="sxs-lookup"><span data-stu-id="4f8d3-122">Exclude users from automatic role assignment</span></span>
1. <span data-ttu-id="4f8d3-123">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="4f8d3-123">Close the page.</span></span>
2. <span data-ttu-id="4f8d3-124">Valitse **Siirtymisruutu > Moduulit > Järjestelmänhallinta > Suojaus > Määritä käyttäjät rooleihin**.</span><span class="sxs-lookup"><span data-stu-id="4f8d3-124">Go to **Navigation pane > Modules > System administration > Security > Assign users to roles**.</span></span>
3. <span data-ttu-id="4f8d3-125">Valitse puusta Taloushallintopäällikkö.</span><span class="sxs-lookup"><span data-stu-id="4f8d3-125">In the tree, select 'Accounting supervisor'.</span></span> <span data-ttu-id="4f8d3-126">Valitse rooli.</span><span class="sxs-lookup"><span data-stu-id="4f8d3-126">Select a role.</span></span> <span data-ttu-id="4f8d3-127">Valitse tässä esimerkissä Taloushallintopäällikkö.</span><span class="sxs-lookup"><span data-stu-id="4f8d3-127">For this example, select Accounting supervisor.</span></span>  
4. <span data-ttu-id="4f8d3-128">Valitse **Roolille määritetyt käyttäjät** -valikossa **Määritä tai sulje pois käyttäjiä manuaalisesti**.</span><span class="sxs-lookup"><span data-stu-id="4f8d3-128">In the **Users assigned to role** menu, select **Manually assign / exclude users**.</span></span>
5. <span data-ttu-id="4f8d3-129">Merkitse valittu rivi **Määritä käyttäjiä rooliin tai sulje käyttäjiä pois roolista** -luettelossa.</span><span class="sxs-lookup"><span data-stu-id="4f8d3-129">In the **Assign users to or exclude users from role** list, mark the selected row.</span></span> <span data-ttu-id="4f8d3-130">Valitse käyttäjä.</span><span class="sxs-lookup"><span data-stu-id="4f8d3-130">Select a user.</span></span>  
6. <span data-ttu-id="4f8d3-131">Valitse **toimintoruudussa** **Sulje pois roolista**.</span><span class="sxs-lookup"><span data-stu-id="4f8d3-131">On the **Action pane**, select **Exclude from role**.</span></span>
    
    <span data-ttu-id="4f8d3-132">Sulje valitut käyttäjät pois roolista valitsemalla **Sulje pois roolista**.</span><span class="sxs-lookup"><span data-stu-id="4f8d3-132">Click **Exclude from role** to exclude the selected users from the role.</span></span> <span data-ttu-id="4f8d3-133">Ohitukset voit poistaa valitsemalla käyttäjät, joiden ohituksen haluat poistaa, ja valitsemalla sitten **Palauta tila**.</span><span class="sxs-lookup"><span data-stu-id="4f8d3-133">To remove exclusions, select the users that you want to remove exclusions for, and then click **Reset status**.</span></span> <span data-ttu-id="4f8d3-134">Kun poistat ohituksen palauttamalla käyttäjän tilan, käyttäjän rooli määritetään uudelleen automaattisesti.</span><span class="sxs-lookup"><span data-stu-id="4f8d3-134">When you remove an exclusion by resetting the user’s status, the user’s role is again assigned automatically.</span></span> <span data-ttu-id="4f8d3-135">Käyttäjää ei kuitenkaan määritetä välittömästi rooliin tai suljeta siitä pois kun palautat tilan.</span><span class="sxs-lookup"><span data-stu-id="4f8d3-135">However, the user is not immediately assigned to the role or excluded from the role when you reset the status.</span></span> <span data-ttu-id="4f8d3-136">Sen sijaan käyttäjä määritetään rooliin tai poistetaan siitä seuraavalla kerralla, kun automaattisen roolinmäärityksen säännöt ajetaan.</span><span class="sxs-lookup"><span data-stu-id="4f8d3-136">Instead, the user is either assigned to the role or removed from the role the next time that the rules for automatic role assignment are run.</span></span>  
