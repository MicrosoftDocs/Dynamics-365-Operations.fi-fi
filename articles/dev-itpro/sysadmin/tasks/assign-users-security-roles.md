---
title: Käyttäjien liittäminen käyttöoikeusrooleihin
description: Microsoft Dynamics 365 for Finance and Operations, Enterprise Editionin käyttämistä varten käyttäjille on määritettävä käyttöoikeusrooleja.
author: maertenm
manager: AnnBe
ms.date: 08/29/2018
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
ms.openlocfilehash: 55cb085bb5170aa4894a2240a12f6ca451b922fb
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/15/2019
ms.locfileid: "1556706"
---
# <a name="assign-users-to-security-roles"></a><span data-ttu-id="37659-103">Käyttäjien liittäminen käyttöoikeusrooleihin</span><span class="sxs-lookup"><span data-stu-id="37659-103">Assign users to security roles</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="37659-104">Microsoft Dynamics 365 for Finance and Operations, Enterprise Editionin käyttämistä varten käyttäjille on määritettävä käyttöoikeusrooleja.</span><span class="sxs-lookup"><span data-stu-id="37659-104">To access Microsoft Dynamics 365 for Finance and Operations, Enterprise edition, users must be assigned to security roles.</span></span> <span data-ttu-id="37659-105">Tässä menettelyssä kerrotaan, kuinka järjestelmänvalvojat voivat määrittää rooleja käyttäjille automaattisesti liiketoimintatietojen perusteella.</span><span class="sxs-lookup"><span data-stu-id="37659-105">This procedure explains how system administrators can assign users to roles automatically, based on business data.</span></span> <span data-ttu-id="37659-106">Tämän menettelyn luomisessa käytetty esittely-yritys on USMF.</span><span class="sxs-lookup"><span data-stu-id="37659-106">The demo data company used to create this procedure is USMF.</span></span>


## <a name="automatically-assign-users-to-roles"></a><span data-ttu-id="37659-107">Liitä käyttäjät rooleihin automaattisesti</span><span class="sxs-lookup"><span data-stu-id="37659-107">Automatically assign users to roles</span></span>
1. <span data-ttu-id="37659-108">Valitse Järjestelmänhallinta > Suojaus > Määritä käyttäjät rooleihin.</span><span class="sxs-lookup"><span data-stu-id="37659-108">Go to System administration > Security > Assign users to roles.</span></span>
2. <span data-ttu-id="37659-109">Valitse puusta Taloushallintopäällikkö.</span><span class="sxs-lookup"><span data-stu-id="37659-109">In the tree, select 'Accounting supervisor'.</span></span>
    * <span data-ttu-id="37659-110">Valitse rooli, jolle haluat konfiguroida säännön.</span><span class="sxs-lookup"><span data-stu-id="37659-110">Select the role that you want to configure the rule for.</span></span> <span data-ttu-id="37659-111">Valitse tässä esimerkissä Taloushallintopäällikkö.</span><span class="sxs-lookup"><span data-stu-id="37659-111">In this example, select Accounting supervisor.</span></span>  
3. <span data-ttu-id="37659-112">Avaa valintaikkuna napsauttamalla Lisää sääntö -painiketta.</span><span class="sxs-lookup"><span data-stu-id="37659-112">Click Add rule to open the drop dialog.</span></span>
4. <span data-ttu-id="37659-113">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="37659-113">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="37659-114">Valitse tämä tässä säännössä käytettävä kysely.</span><span class="sxs-lookup"><span data-stu-id="37659-114">Select the query to use for this rule.</span></span>  
5. <span data-ttu-id="37659-115">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="37659-115">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="37659-116">Valitse Muokkaa kyselyä.</span><span class="sxs-lookup"><span data-stu-id="37659-116">Click Edit query.</span></span>
    * <span data-ttu-id="37659-117">Muokkaa kyselyä tarvittaessa.</span><span class="sxs-lookup"><span data-stu-id="37659-117">Edit the query, as needed.</span></span>  
7. <span data-ttu-id="37659-118">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="37659-118">Click OK.</span></span>

## <a name="exclude-users-from-automatic-role-assignment"></a><span data-ttu-id="37659-119">Sulje käyttäjät pois automaattisesta roolin määrityksestä</span><span class="sxs-lookup"><span data-stu-id="37659-119">Exclude users from automatic role assignment</span></span>
1. <span data-ttu-id="37659-120">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="37659-120">Close the page.</span></span>
2. <span data-ttu-id="37659-121">Valitse Järjestelmänhallinta > Suojaus > Määritä käyttäjät rooleihin.</span><span class="sxs-lookup"><span data-stu-id="37659-121">Go to System administration > Security > Assign users to roles.</span></span>
3. <span data-ttu-id="37659-122">Valitse puusta Taloushallintopäällikkö.</span><span class="sxs-lookup"><span data-stu-id="37659-122">In the tree, select 'Accounting supervisor'.</span></span>
    * <span data-ttu-id="37659-123">Valitse rooli.</span><span class="sxs-lookup"><span data-stu-id="37659-123">Select a role.</span></span> <span data-ttu-id="37659-124">Valitse tässä esimerkissä Taloushallintopäällikkö.</span><span class="sxs-lookup"><span data-stu-id="37659-124">For this example, select Accounting supervisor.</span></span>  
4. <span data-ttu-id="37659-125">Napsauta Määritä tai sulje pois käyttäjiä manuaalisesti -kohtaa.</span><span class="sxs-lookup"><span data-stu-id="37659-125">Click Manually assign / exclude users.</span></span>
5. <span data-ttu-id="37659-126">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="37659-126">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="37659-127">Valitse käyttäjä.</span><span class="sxs-lookup"><span data-stu-id="37659-127">Select a user.</span></span>  
6. <span data-ttu-id="37659-128">Napsauta Sulje pois roolista -kohtaa.</span><span class="sxs-lookup"><span data-stu-id="37659-128">Click Exclude from role.</span></span>
    * <span data-ttu-id="37659-129">Napsauta Sulje pois roolista -painiketta sulkeaksesi valitut käyttäjät pois roolista.</span><span class="sxs-lookup"><span data-stu-id="37659-129">Click Exclude from role to exclude the selected users from the role.</span></span> <span data-ttu-id="37659-130">Ohitukset voit poistaa valitsemalla käyttäjät, joiden ohituksen haluat poistaa ja napsauttamalla Palauta tila -painiketta.</span><span class="sxs-lookup"><span data-stu-id="37659-130">To remove exclusions, select the users that you want to remove exclusions for, and then click Reset status.</span></span> <span data-ttu-id="37659-131">Kun poistat ohituksen palauttamalla käyttäjän tilan, käyttäjän rooli määritetään uudelleen automaattisesti.</span><span class="sxs-lookup"><span data-stu-id="37659-131">When you remove an exclusion by resetting the user’s status, the user’s role is again assigned automatically.</span></span> <span data-ttu-id="37659-132">Käyttäjää ei kuitenkaan määritetä välittömästi rooliin tai suljeta siitä pois kun palautat tilan.</span><span class="sxs-lookup"><span data-stu-id="37659-132">However, the user is not immediately assigned to the role or excluded from the role when you reset the status.</span></span> <span data-ttu-id="37659-133">Sen sijaan käyttäjä määritetään rooliin tai poistetaan siitä seuraavalla kerralla, kun automaattisen roolinmäärityksen säännöt ajetaan.</span><span class="sxs-lookup"><span data-stu-id="37659-133">Instead, the user is either assigned to the role or removed from the role the next time that the rules for automatic role assignment are run.</span></span>  

