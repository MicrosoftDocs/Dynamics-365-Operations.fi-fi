--- 
title: "Käyttäjien liittäminen käyttöoikeusrooleihin"
description: "Microsoft Dynamics 365 for Finance and Operationsin käyttö edellyttää, että käyttäjille on määritetty käyttöoikeusroolit."
author: maertenm
manager: AnnBe
ms.date: 06/07/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: sericks
ms.search.scope: Operations
ms.search.region: Global
ms.author: maertenm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a0739304723d19b910388893d08e8c36a1f49d13
ms.openlocfilehash: da96ec8357ea209fd958e32ab438b13e668735df
ms.contentlocale: fi-fi
ms.lasthandoff: 03/26/2018

---
# <a name="assign-users-to-security-roles"></a><span data-ttu-id="7b698-103">Käyttäjien liittäminen suojausrooleihin</span><span class="sxs-lookup"><span data-stu-id="7b698-103">Assign users to security roles</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="7b698-104">Microsoft Dynamics 365 for Finance and Operationsin käyttö edellyttää, että käyttäjille on määritetty käyttöoikeusroolit.</span><span class="sxs-lookup"><span data-stu-id="7b698-104">To access Microsoft Dynamics 365 for Finance and Operations, users must be assigned to security roles.</span></span> <span data-ttu-id="7b698-105">Tässä menettelyssä kerrotaan, kuinka järjestelmänvalvojat voivat määrittää rooleja käyttäjille automaattisesti liiketoimintatietojen perusteella.</span><span class="sxs-lookup"><span data-stu-id="7b698-105">This procedure explains how system administrators can assign users to roles automatically, based on business data.</span></span> <span data-ttu-id="7b698-106">Tämän menettelyn luomisessa käytetty esittely-yritys on USMF.</span><span class="sxs-lookup"><span data-stu-id="7b698-106">The demo data company used to create this procedure is USMF.</span></span>


## <a name="automatically-assign-users-to-roles"></a><span data-ttu-id="7b698-107">Liitä käyttäjät rooleihin automaattisesti</span><span class="sxs-lookup"><span data-stu-id="7b698-107">Automatically assign users to roles</span></span>
1. <span data-ttu-id="7b698-108">Valitse Järjestelmänhallinta > Suojaus > Määritä käyttäjät rooleihin.</span><span class="sxs-lookup"><span data-stu-id="7b698-108">Go to System administration > Security > Assign users to roles.</span></span>
2. <span data-ttu-id="7b698-109">Valitse puusta Taloushallintopäällikkö.</span><span class="sxs-lookup"><span data-stu-id="7b698-109">In the tree, select 'Accounting supervisor'.</span></span>
    * <span data-ttu-id="7b698-110">Valitse rooli, jolle haluat konfiguroida säännön.</span><span class="sxs-lookup"><span data-stu-id="7b698-110">Select the role that you want to configure the rule for.</span></span> <span data-ttu-id="7b698-111">Valitse tässä esimerkissä Taloushallintopäällikkö.</span><span class="sxs-lookup"><span data-stu-id="7b698-111">In this example, select Accounting supervisor.</span></span>  
3. <span data-ttu-id="7b698-112">Avaa valintaikkuna napsauttamalla Lisää sääntö -painiketta.</span><span class="sxs-lookup"><span data-stu-id="7b698-112">Click Add rule to open the drop dialog.</span></span>
4. <span data-ttu-id="7b698-113">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="7b698-113">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="7b698-114">Valitse tämä tässä säännössä käytettävä kysely.</span><span class="sxs-lookup"><span data-stu-id="7b698-114">Select the query to use for this rule.</span></span>  
5. <span data-ttu-id="7b698-115">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="7b698-115">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="7b698-116">Valitse Muokkaa kyselyä.</span><span class="sxs-lookup"><span data-stu-id="7b698-116">Click Edit query.</span></span>
    * <span data-ttu-id="7b698-117">Muokkaa kyselyä tarvittaessa.</span><span class="sxs-lookup"><span data-stu-id="7b698-117">Edit the query, as needed.</span></span>  
7. <span data-ttu-id="7b698-118">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="7b698-118">Click OK.</span></span>

## <a name="exclude-users-from-automatic-role-assignment"></a><span data-ttu-id="7b698-119">Sulje käyttäjät pois automaattisesta roolin määrityksestä</span><span class="sxs-lookup"><span data-stu-id="7b698-119">Exclude users from automatic role assignment</span></span>
1. <span data-ttu-id="7b698-120">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="7b698-120">Close the page.</span></span>
2. <span data-ttu-id="7b698-121">Valitse Järjestelmänhallinta > Suojaus > Määritä käyttäjät rooleihin.</span><span class="sxs-lookup"><span data-stu-id="7b698-121">Go to System administration > Security > Assign users to roles.</span></span>
3. <span data-ttu-id="7b698-122">Valitse puusta Taloushallintopäällikkö.</span><span class="sxs-lookup"><span data-stu-id="7b698-122">In the tree, select 'Accounting supervisor'.</span></span>
    * <span data-ttu-id="7b698-123">Valitse rooli.</span><span class="sxs-lookup"><span data-stu-id="7b698-123">Select a role.</span></span> <span data-ttu-id="7b698-124">Valitse tässä esimerkissä Taloushallintopäällikkö.</span><span class="sxs-lookup"><span data-stu-id="7b698-124">For this example, select Accounting supervisor.</span></span>  
4. <span data-ttu-id="7b698-125">Napsauta Määritä tai sulje pois käyttäjiä manuaalisesti -kohtaa.</span><span class="sxs-lookup"><span data-stu-id="7b698-125">Click Manually assign / exclude users.</span></span>
5. <span data-ttu-id="7b698-126">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="7b698-126">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="7b698-127">Valitse käyttäjä.</span><span class="sxs-lookup"><span data-stu-id="7b698-127">Select a user.</span></span>  
6. <span data-ttu-id="7b698-128">Napsauta Sulje pois roolista -kohtaa.</span><span class="sxs-lookup"><span data-stu-id="7b698-128">Click Exclude from role.</span></span>
    * <span data-ttu-id="7b698-129">Napsauta Sulje pois roolista -painiketta sulkeaksesi valitut käyttäjät pois roolista.</span><span class="sxs-lookup"><span data-stu-id="7b698-129">Click Exclude from role to exclude the selected users from the role.</span></span> <span data-ttu-id="7b698-130">Ohitukset voit poistaa valitsemalla käyttäjät, joiden ohituksen haluat poistaa ja napsauttamalla Palauta tila -painiketta.</span><span class="sxs-lookup"><span data-stu-id="7b698-130">To remove exclusions, select the users that you want to remove exclusions for, and then click Reset status.</span></span> <span data-ttu-id="7b698-131">Kun poistat ohituksen palauttamalla käyttäjän tilan, käyttäjän rooli määritetään uudelleen automaattisesti.</span><span class="sxs-lookup"><span data-stu-id="7b698-131">When you remove an exclusion by resetting the user’s status, the user’s role is again assigned automatically.</span></span> <span data-ttu-id="7b698-132">Käyttäjää ei kuitenkaan määritetä välittömästi rooliin tai suljeta siitä pois kun palautat tilan.</span><span class="sxs-lookup"><span data-stu-id="7b698-132">However, the user is not immediately assigned to the role or excluded from the role when you reset the status.</span></span> <span data-ttu-id="7b698-133">Sen sijaan käyttäjä määritetään rooliin tai poistetaan siitä seuraavalla kerralla, kun automaattisen roolinmäärityksen säännöt ajetaan.</span><span class="sxs-lookup"><span data-stu-id="7b698-133">Instead, the user is either assigned to the role or removed from the role the next time that the rules for automatic role assignment are run.</span></span>  


