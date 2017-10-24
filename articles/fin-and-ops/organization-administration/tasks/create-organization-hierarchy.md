--- 
title: Luo organisaatiohierarkia
description: Luo organisaatiohierarkia seuraavien ohjeiden mukaan.
author: sericks007
manager: AnnBe
ms.date: 06/09/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: sericks
ms.search.scope: Operations
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: 2aea56a549131745b2636392561176bf0f87097c
ms.contentlocale: fi-fi
ms.lasthandoff: 09/29/2017

---
# <a name="create-an-organization-hierarchy"></a><span data-ttu-id="b8bfa-103">Luo organisaatiohierarkia</span><span class="sxs-lookup"><span data-stu-id="b8bfa-103">Create an organization hierarchy</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="b8bfa-104">Luo organisaatiohierarkia seuraavien ohjeiden mukaan.</span><span class="sxs-lookup"><span data-stu-id="b8bfa-104">Use the following procedure to create an organizational hierarchy.</span></span> <span data-ttu-id="b8bfa-105">Voit käyttää organisaatiohierarkioita liiketoiminnan tarkastelemiseen ja raportointiin eri näkökulmista.</span><span class="sxs-lookup"><span data-stu-id="b8bfa-105">You can use organizational hierarchies to view and report on your business from various perspectives.</span></span> <span data-ttu-id="b8bfa-106">Voit esimerkiksi määrittää yhden hierarkian veroraportteja tai oikeudellista tai lakisääteistä raportointia varten.</span><span class="sxs-lookup"><span data-stu-id="b8bfa-106">For example, you can set up one hierarchy for tax, legal, or statutory reporting.</span></span> <span data-ttu-id="b8bfa-107">Voit määrittää toisen hierarkian raportoimaan sellaiset taloustiedot, joiden raportointia lainsäädäntö ei edellytä mutta joita käytetään sisäisessä raportoinnissa.</span><span class="sxs-lookup"><span data-stu-id="b8bfa-107">You can then set up another hierarchy to report financial information that is not legally required, but that is used for internal reporting.</span></span> 



<span data-ttu-id="b8bfa-108">Ennen organisaatiohierarkian luomista sinun on luotava organisaatiot.</span><span class="sxs-lookup"><span data-stu-id="b8bfa-108">Before you create an organizational hierarchy, you must create organizations.</span></span> <span data-ttu-id="b8bfa-109">Lisätietoja on tehtävissä "Yrityksen luominen" tai "Toimintayksikön luominen".</span><span class="sxs-lookup"><span data-stu-id="b8bfa-109">For more information, see the “Create a legal entity” or “Create an operating unit” tasks.</span></span> <span data-ttu-id="b8bfa-110">Voit myös luoda osastoja ja tiimejä.</span><span class="sxs-lookup"><span data-stu-id="b8bfa-110">You can also create departments and teams.</span></span> 



<span data-ttu-id="b8bfa-111">Tämän menettelyn luomisessa käytetty esittely-yritys on USMF.</span><span class="sxs-lookup"><span data-stu-id="b8bfa-111">The demo data company used to create this procedure is USMF.</span></span>


## <a name="create-a-hierarchy"></a><span data-ttu-id="b8bfa-112">Luo hierarkia</span><span class="sxs-lookup"><span data-stu-id="b8bfa-112">Create a hierarchy</span></span>
1. <span data-ttu-id="b8bfa-113">Valitse Organisaation hallinto > Organisaatiot > Organisaatiohierarkiat.</span><span class="sxs-lookup"><span data-stu-id="b8bfa-113">Go to Organization administration > Organizations > Organization hierarchies.</span></span>
2. <span data-ttu-id="b8bfa-114">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="b8bfa-114">Click New.</span></span>
3. <span data-ttu-id="b8bfa-115">Kirjoita arvo Nimi-kenttään.</span><span class="sxs-lookup"><span data-stu-id="b8bfa-115">In the Name field, type a value.</span></span>
4. <span data-ttu-id="b8bfa-116">Valitse Määritä tarkoitus.</span><span class="sxs-lookup"><span data-stu-id="b8bfa-116">Click Assign purpose.</span></span>
5. <span data-ttu-id="b8bfa-117">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="b8bfa-117">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="b8bfa-118">Valitse tarkoitus määritettäväksi organisaatiohierarkiaan.</span><span class="sxs-lookup"><span data-stu-id="b8bfa-118">Select a purpose to assign to your organization hierarchy.</span></span>  
6. <span data-ttu-id="b8bfa-119">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="b8bfa-119">Click Add.</span></span>
7. <span data-ttu-id="b8bfa-120">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="b8bfa-120">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="b8bfa-121">Etsi juuri luomasi hierarkia.</span><span class="sxs-lookup"><span data-stu-id="b8bfa-121">Find the hierarchy you just created.</span></span>  
8. <span data-ttu-id="b8bfa-122">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="b8bfa-122">Click OK.</span></span>

## <a name="add-organizations-to-the-hierarchy"></a><span data-ttu-id="b8bfa-123">Organisaatioiden lisääminen hierarkiaan</span><span class="sxs-lookup"><span data-stu-id="b8bfa-123">Add organizations to the hierarchy</span></span>
1. <span data-ttu-id="b8bfa-124">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="b8bfa-124">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="b8bfa-125">Valitse hierarkia.</span><span class="sxs-lookup"><span data-stu-id="b8bfa-125">Select your hierarchy.</span></span>  
2. <span data-ttu-id="b8bfa-126">Valitse Näytä hierarkia.</span><span class="sxs-lookup"><span data-stu-id="b8bfa-126">Click View hierarchy.</span></span>
    * <span data-ttu-id="b8bfa-127">Lisää organisaatioita tarvittaessa.</span><span class="sxs-lookup"><span data-stu-id="b8bfa-127">Add organizations, as necessary.</span></span>  
    * <span data-ttu-id="b8bfa-128">Lisää organisaatio napsauttamalla Muokkaa ja sitten Lisää.</span><span class="sxs-lookup"><span data-stu-id="b8bfa-128">To add an organization, click Edit and then Insert to add the organization.</span></span>     <span data-ttu-id="b8bfa-129">Kun olet tehnyt haluamasi muutokset, voit tallentaa luonnoksena ja/tai julkaista muutokset.</span><span class="sxs-lookup"><span data-stu-id="b8bfa-129">When you are done making changes you can save a draft and/or publish the changes.</span></span>  


