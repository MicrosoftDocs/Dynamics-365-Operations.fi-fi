---
title: Luo organisaatiohierarkia
description: Luo organisaatiohierarkia seuraavien ohjeiden mukaan.
author: sericks007
manager: AnnBe
ms.date: 07/01/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: OMHierarchyManager, OMHierarchyPurposeAssociation, OMHierarchySelection, HierarchyDesigner
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 673403680525eff57c5886bb4f430a33efd76250
ms.sourcegitcommit: f5e31c34640add6d40308ac1365cc0ee60e60e24
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/08/2020
ms.locfileid: "4694786"
---
# <a name="create-an-organization-hierarchy"></a><span data-ttu-id="04931-103">Luo organisaatiohierarkia</span><span class="sxs-lookup"><span data-stu-id="04931-103">Create an organization hierarchy</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="04931-104">Luo organisaatiohierarkia seuraavien ohjeiden mukaan.</span><span class="sxs-lookup"><span data-stu-id="04931-104">Use the following procedure to create an organizational hierarchy.</span></span> <span data-ttu-id="04931-105">Voit käyttää organisaatiohierarkioita liiketoiminnan tarkastelemiseen ja raportointiin eri näkökulmista.</span><span class="sxs-lookup"><span data-stu-id="04931-105">You can use organizational hierarchies to view and report on your business from various perspectives.</span></span> <span data-ttu-id="04931-106">Voit esimerkiksi määrittää yhden hierarkian veroraportteja tai oikeudellista tai lakisääteistä raportointia varten.</span><span class="sxs-lookup"><span data-stu-id="04931-106">For example, you can set up one hierarchy for tax, legal, or statutory reporting.</span></span> <span data-ttu-id="04931-107">Voit määrittää toisen hierarkian raportoimaan sellaiset taloustiedot, joiden raportointia lainsäädäntö ei edellytä mutta joita käytetään sisäisessä raportoinnissa.</span><span class="sxs-lookup"><span data-stu-id="04931-107">You can then set up another hierarchy to report financial information that is not legally required, but that is used for internal reporting.</span></span> 

<span data-ttu-id="04931-108">Ennen organisaatiohierarkian luomista sinun on luotava organisaatiot.</span><span class="sxs-lookup"><span data-stu-id="04931-108">Before you create an organizational hierarchy, you must create organizations.</span></span> <span data-ttu-id="04931-109">Lisätietoja on tehtävissä "Yrityksen luominen" tai "Toimintayksikön luominen".</span><span class="sxs-lookup"><span data-stu-id="04931-109">For more information, see the "Create a legal entity" or "Create an operating unit" tasks.</span></span> <span data-ttu-id="04931-110">Voit myös luoda osastoja ja tiimejä.</span><span class="sxs-lookup"><span data-stu-id="04931-110">You can also create departments and teams.</span></span> 

<span data-ttu-id="04931-111">Tämän menettelyn luomisessa käytetty esittely-yritys on USMF.</span><span class="sxs-lookup"><span data-stu-id="04931-111">The demo data company used to create this procedure is USMF.</span></span>

## <a name="create-a-hierarchy"></a><span data-ttu-id="04931-112">Luo hierarkia</span><span class="sxs-lookup"><span data-stu-id="04931-112">Create a hierarchy</span></span>
1. <span data-ttu-id="04931-113">Valitse **Siirtymisruutu > Moduuli > Organisaation hallinto > Organisaatiot >Organisaatiohierarkiat**.</span><span class="sxs-lookup"><span data-stu-id="04931-113">Go to **Navigation pane > Modules > Organization administration > Organizations > Organization hierarchies**.</span></span>
2. <span data-ttu-id="04931-114">Napsauta **Toimintoruudussa** **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="04931-114">On the **Action pane**, click **New**.</span></span>
3. <span data-ttu-id="04931-115">Kirjoita arvo **Nimi**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="04931-115">In the **Name** field, type a value.</span></span>
4. <span data-ttu-id="04931-116">Valitse **Tarkoitus** -osassa **Määritä tarkoitus**.</span><span class="sxs-lookup"><span data-stu-id="04931-116">In the **Purpose** section, click **Assign purpose**.</span></span>
5. <span data-ttu-id="04931-117">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="04931-117">In the list, find and select the desired record.</span></span> <span data-ttu-id="04931-118">Valitse tarkoitus määritettäväksi organisaatiohierarkiaan.</span><span class="sxs-lookup"><span data-stu-id="04931-118">Select a purpose to assign to your organization hierarchy.</span></span>  
6. <span data-ttu-id="04931-119">Valitse **Määritetyt hierarkiat** -kohdasta **Lisää.**</span><span class="sxs-lookup"><span data-stu-id="04931-119">In the **Assigned hierarchies** sectiom, click **Add**.</span></span>
7. <span data-ttu-id="04931-120">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="04931-120">In the list, mark the selected row.</span></span> <span data-ttu-id="04931-121">Etsi juuri luomasi hierarkia.</span><span class="sxs-lookup"><span data-stu-id="04931-121">Find the hierarchy you just created.</span></span>  
8. <span data-ttu-id="04931-122">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="04931-122">Click **OK**.</span></span>

## <a name="add-organizations-to-the-hierarchy"></a><span data-ttu-id="04931-123">Organisaatioiden lisääminen hierarkiaan</span><span class="sxs-lookup"><span data-stu-id="04931-123">Add organizations to the hierarchy</span></span>
1. <span data-ttu-id="04931-124">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="04931-124">In the list, find and select the desired record.</span></span> <span data-ttu-id="04931-125">Valitse hierarkia.</span><span class="sxs-lookup"><span data-stu-id="04931-125">Select your hierarchy.</span></span>  
2. <span data-ttu-id="04931-126">Valitse **Määritetyt hierarkiat** -osassa **Näytä hierarkia**.</span><span class="sxs-lookup"><span data-stu-id="04931-126">In the **Assigned hierarchies** section, click **View hierarchy**.</span></span>
    - <span data-ttu-id="04931-127">Lisää organisaatioita tarvittaessa.</span><span class="sxs-lookup"><span data-stu-id="04931-127">Add organizations, as necessary.</span></span>  
    - <span data-ttu-id="04931-128">Lisää organisaatio napsauttamalla **Muokkaa** ja sitten **Lisää**.</span><span class="sxs-lookup"><span data-stu-id="04931-128">To add an organization, click **Edit** and then **Insert** to add the organization.</span></span> <span data-ttu-id="04931-129">Kun olet tehnyt haluamasi muutokset, voit tallentaa luonnoksena (**Tallenna**) ja/tai julkaista muutokset (**Julkaise**).</span><span class="sxs-lookup"><span data-stu-id="04931-129">When you are done making changes you can **Save** a draft and/or **Publish** the changes.</span></span>  

