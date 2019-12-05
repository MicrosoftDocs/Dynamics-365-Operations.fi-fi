---
title: Lisää sijainnin ja osapuolen suhteen tyypit
description: Tässä ohjeaiheessa kerrotaan, miten voit lisätä uuden sijainnin ja osapuolen suhteen tyypin.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 13991
ms.assetid: 2a0a4789-8619-4974-bef9-0923cc848420
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2018-05-02
ms.dyn365.ops.version: AX 8.0.0
ms.openlocfilehash: e38d0bd75ad865b7885182f798beb43551576beb
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/06/2019
ms.locfileid: "2770893"
---
# <a name="add-location-and-party-relationship-types"></a><span data-ttu-id="250c8-103">Lisää sijainnin ja osapuolen suhteen tyypit</span><span class="sxs-lookup"><span data-stu-id="250c8-103">Add location and party relationship types</span></span> 

[!include [banner](../includes/banner.md)]

## <a name="add-location-roles"></a><span data-ttu-id="250c8-104">Lisää toimipaikkaroolit</span><span class="sxs-lookup"><span data-stu-id="250c8-104">Add location roles</span></span>

<span data-ttu-id="250c8-105">On kaksi tapaa lisätä uusia sijaintirooleja osoitteelle ja yhteystiedoille:</span><span class="sxs-lookup"><span data-stu-id="250c8-105">There are two ways to add a new location roles for address and contact information:</span></span>

-  <span data-ttu-id="250c8-106">Lisää ne **Osoitteen ja yhteystietojen tarkoitus** -sivulla.</span><span class="sxs-lookup"><span data-stu-id="250c8-106">Add it through the **Address and contact information purpose** page.</span></span> <span data-ttu-id="250c8-107">Uusi rooli tallennetaan **LogisticsLocationRole**-tauluun tyyppinä 0, mikä ilmaisee, että rooli ei ole järjestelmärooli, joka on määritetty **LogisticsLocationRoleType**-luettelossa ja sen laajennuksissa.</span><span class="sxs-lookup"><span data-stu-id="250c8-107">The new role will be saved to the **LogisticsLocationRole** table with type = 0, which indicates that the role is not a system role defined in the **LogisticsLocationRoleType** enum and its extensions.</span></span> <span data-ttu-id="250c8-108">Käyttäjä voi käyttää tätä roolia luodessaan osoitteen tai yhteyshenkilön tiedot.</span><span class="sxs-lookup"><span data-stu-id="250c8-108">A user will be able to use this role when creating address or contact information.</span></span>

    ![Osoitteen ja yhteystietojen tarkoitus](media/Address-Contact.PNG)

-  <span data-ttu-id="250c8-110">Lisää se **LogisticsLocationRoleType**-valintalistan laajennukseen, minkä jälkeen se täyttää taulut tietokannan synkronoinnin prosessin kautta.</span><span class="sxs-lookup"><span data-stu-id="250c8-110">Add it to the **LogisticsLocationRoleType** enum extension, and let it populate through the database sync process.</span></span>

    1.  <span data-ttu-id="250c8-111">Luo laajennus **LogisticsLocationRoleType**-valintalistalle ja lisää uusi rooli laajennukseen.</span><span class="sxs-lookup"><span data-stu-id="250c8-111">Create an extension to the **LogisticsLocationRoleType** enum and add the new role in the extension.</span></span> 
  
        ![LogisticsLocationRoleType-valintalistan laajennus](media/Logistics.PNG)

    2. <span data-ttu-id="250c8-113">Luo uuden roolin uusi resurssitiedosto ja määritä sitten arvot sen ominaisuuksille.</span><span class="sxs-lookup"><span data-stu-id="250c8-113">Create a new resource file for the new role, and then assign a value for its properties.</span></span>
     
     ![Uusi resurssitiedosto](media/Resource.PNG)
        
    3.  <span data-ttu-id="250c8-115">Luo tietojen täyttöluokka ja anna käsittelijämetodi uuden roolin täyttämiseen.</span><span class="sxs-lookup"><span data-stu-id="250c8-115">Create a data population class and provide a handler method to populate the new role.</span></span> 

        ![Tietojen täyttö](media/Dirdata.PNG)

    4.  <span data-ttu-id="250c8-117">Voit testata uuden sijaintiroolin täyttöä luomalla runnable-luokan ja kutsumalla DirDataPopulation:::insertLogisticsLocationRoles()-menetelmää Main()-menetelmässä.</span><span class="sxs-lookup"><span data-stu-id="250c8-117">To test populating the new location role, you can create a runnable class, and call DirDataPopulation::insertLogisticsLocationRoles() in Main().</span></span> <span data-ttu-id="250c8-118">Kun tämä prosessi on valmis, sinun pitäisi nähdä, että uusi rooli täytetään **LogisticsLocationRole**-tauluun määritteellä type \> 0.</span><span class="sxs-lookup"><span data-stu-id="250c8-118">After this process is complete, you should see the new role populated in the **LogisticsLocationRole** table with type \> 0.</span></span> <span data-ttu-id="250c8-119">Uusi rooli tulee näkyviin **Osoitteen ja yhteystietojen tarkoitus** -sivulle.</span><span class="sxs-lookup"><span data-stu-id="250c8-119">The new role will display on the **Address and contact information purpose** page.</span></span>

        ![Lisää uusi sijainti](media/InsertNewLocation.PNG)

## <a name="add-party-relationship-types"></a><span data-ttu-id="250c8-121">Lisää uusia osapuolten suhteen tyyppejä</span><span class="sxs-lookup"><span data-stu-id="250c8-121">Add party relationship types</span></span> 

<span data-ttu-id="250c8-122">Voit lisätä uusia suhteen tyyppejä kahdella tavalla:</span><span class="sxs-lookup"><span data-stu-id="250c8-122">There are two ways to add a new relationship type:</span></span>

-   <span data-ttu-id="250c8-123">Lisää se **Suhdetyypit**-sivulla.</span><span class="sxs-lookup"><span data-stu-id="250c8-123">Add it through the **Relationship types** page.</span></span> <span data-ttu-id="250c8-124">Uusi suhde tallennetaan **DirRelationshipTypeTable**-tauluun määritteelllä systemtype = 0.</span><span class="sxs-lookup"><span data-stu-id="250c8-124">The new relationship will be saved to **DirRelationshipTypeTable** with systemtype = 0.</span></span>

    ![Suhdetyypit](media/Relationship.PNG)

-  <span data-ttu-id="250c8-126">Lisää se **DirSystemRelationshipType**-valintalistan laajennukseen, minkä jälkeen se täyttää taulut tietokannan synkronoinnin prosessin kautta.</span><span class="sxs-lookup"><span data-stu-id="250c8-126">Add it to the extension of the **DirSystemRelationshipType** enum, and let it populate through database sync process.</span></span>

    1.  <span data-ttu-id="250c8-127">Luo laajennus **DirSystemRelationshipType**-valintalistalle ja lisää uusi suhdetyyppi.</span><span class="sxs-lookup"><span data-stu-id="250c8-127">Create an extension to the **DirSystemRelationshipType** enum and add the new relationship type.</span></span>

    2. <span data-ttu-id="250c8-128">Luo alustustoiminto tälle uudelle tyypille.</span><span class="sxs-lookup"><span data-stu-id="250c8-128">Create an initializer for this new type.</span></span> <span data-ttu-id="250c8-129">Löydät useita esimerkkejä ydinkoodissa, esimerkiksim kohdassa **DirRelationshipTypeChildInitialize**.</span><span class="sxs-lookup"><span data-stu-id="250c8-129">You can find several examples in the core code, one of them is  **DirRelationshipTypeChildInitialize**.</span></span> <span data-ttu-id="250c8-130">Tämä on alustajatoimintoluokka osapuolen suhteen tyypille Child (alataso).</span><span class="sxs-lookup"><span data-stu-id="250c8-130">This is an initializer class for party relationship type “Child”.</span></span> <span data-ttu-id="250c8-131">Voit aloittaa oman alustimen kirjoittamisen kopioimalla ja liittämällä tämän koodin ja päivittämällä korostetut alueet.</span><span class="sxs-lookup"><span data-stu-id="250c8-131">You can start with your initializer by copying and pasting this code and then update the highlighted areas.</span></span>
    
    ![DirRelationshipChild-alustaja](media/DirRelationship.PNG)

    3.  <span data-ttu-id="250c8-133">Voit testata uuden suhdetyypin täyttöä luomalla runnable-luokan ja kutsumalla DirDataPopulation::insertDirRelationshipTypes()-menetelmää Main()-menetelmässä.</span><span class="sxs-lookup"><span data-stu-id="250c8-133">To test populating the new relationship type, you can create a runnable class, and call DirDataPopulation::insertDirRelationshipTypes() in Main().</span></span> <span data-ttu-id="250c8-134">Näkyviin tulee uusi suhteen laji **DirRelationshipTypeTable**-taulussa ja uusi suhdetyyppi on käytettävissä **Suhdetyypit**-sivulla.</span><span class="sxs-lookup"><span data-stu-id="250c8-134">You should see the new relationship type in the **DirRelationshipTypeTable**, and the new relationship type will be available on the **Relationship types** page.</span></span>

        ![Runnable-luokka](media/Runnable.PNG)
