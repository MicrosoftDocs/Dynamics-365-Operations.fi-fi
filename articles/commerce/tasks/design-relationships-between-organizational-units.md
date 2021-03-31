---
title: Organisaatioyksiköiden välisten suhteiden suunnittelu
description: Menettely opastaa organisaatioyksiköiden välisten suhteiden suunnittelemisessa.
author: mugunthanm
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: OMHierarchyManager, OMHierarchyPurposeAssociation, OMHierarchySelection, HierarchyDesigner, OMNodeSelection,  HierarchyPublishAndCloseForm
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.search.industry: Retail
ms.author: mumani
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 132b3133bd75cd2b47a96a60e943ff96e686fecf
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5229885"
---
# <a name="design-the-relationships-between-organizational-units"></a><span data-ttu-id="9c3e8-103">Organisaatioyksiköiden välisten suhteiden suunnittelu</span><span class="sxs-lookup"><span data-stu-id="9c3e8-103">Design the relationships between organizational units</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9c3e8-104">Menettely opastaa organisaatioyksiköiden välisten suhteiden suunnittelemisessa.</span><span class="sxs-lookup"><span data-stu-id="9c3e8-104">This procedure walks through how to design the relationship between organizational units.</span></span> <span data-ttu-id="9c3e8-105">Luo uuden organisaation tarkoitus, ennen kuin määrität suhteen. Voit myös käyttää aiemmin luotua organisaation tarkoitusta.</span><span class="sxs-lookup"><span data-stu-id="9c3e8-105">You must create a new organization purpose before defining the relationship, or you can use the existing organization purpose.</span></span> <span data-ttu-id="9c3e8-106">Tämä menettely tehdään valmiiksi käyttämällä esittely-yritystä USRT.</span><span class="sxs-lookup"><span data-stu-id="9c3e8-106">The demo data company used to complete this procedure is USRT.</span></span> <span data-ttu-id="9c3e8-107">Tämä tehtävä on tarkoitettu järjestelmänvalvojan roolille.</span><span class="sxs-lookup"><span data-stu-id="9c3e8-107">This task is intended for the administrator role.</span></span>

1. <span data-ttu-id="9c3e8-108">Valitse Organisaation hallinto > Organisaatiot > Organisaatiohierarkiat.</span><span class="sxs-lookup"><span data-stu-id="9c3e8-108">Go to Organization administration > Organizations > Organization hierarchies.</span></span>
2. <span data-ttu-id="9c3e8-109">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="9c3e8-109">Click New.</span></span>
3. <span data-ttu-id="9c3e8-110">Kirjoita arvo Nimi-kenttään.</span><span class="sxs-lookup"><span data-stu-id="9c3e8-110">In the Name field, type a value.</span></span>
4. <span data-ttu-id="9c3e8-111">Valitse Määritä tarkoitus.</span><span class="sxs-lookup"><span data-stu-id="9c3e8-111">Click Assign purpose.</span></span>
5. <span data-ttu-id="9c3e8-112">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="9c3e8-112">In the list, find and select the desired record.</span></span>
6. <span data-ttu-id="9c3e8-113">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="9c3e8-113">Click Add.</span></span>
7. <span data-ttu-id="9c3e8-114">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="9c3e8-114">In the list, find and select the desired record.</span></span>
8. <span data-ttu-id="9c3e8-115">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="9c3e8-115">Click OK.</span></span>
    * <span data-ttu-id="9c3e8-116">Voit valita organisaation vaatiman määrän organisaation tarkoituksia.</span><span class="sxs-lookup"><span data-stu-id="9c3e8-116">You can select as many organization purposes as required for your organization.</span></span>  
9. <span data-ttu-id="9c3e8-117">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="9c3e8-117">In the list, find and select the desired record.</span></span>
10. <span data-ttu-id="9c3e8-118">Valitse Aseta oletukseksi.</span><span class="sxs-lookup"><span data-stu-id="9c3e8-118">Click Set as default.</span></span>
11. <span data-ttu-id="9c3e8-119">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="9c3e8-119">Close the page.</span></span>
12. <span data-ttu-id="9c3e8-120">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="9c3e8-120">Click Save.</span></span>
13. <span data-ttu-id="9c3e8-121">Valitse Näytä.</span><span class="sxs-lookup"><span data-stu-id="9c3e8-121">Click View.</span></span>
14. <span data-ttu-id="9c3e8-122">Valitse Muokkaa.</span><span class="sxs-lookup"><span data-stu-id="9c3e8-122">Click Edit.</span></span>
15. <span data-ttu-id="9c3e8-123">Valitse Lisää.</span><span class="sxs-lookup"><span data-stu-id="9c3e8-123">Click Insert.</span></span>
16. <span data-ttu-id="9c3e8-124">Valitse Liiketoimintayksikkö.</span><span class="sxs-lookup"><span data-stu-id="9c3e8-124">Click Business unit.</span></span>
17. <span data-ttu-id="9c3e8-125">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="9c3e8-125">In the list, find and select the desired record.</span></span>
18. <span data-ttu-id="9c3e8-126">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="9c3e8-126">In the list, click the link in the selected row.</span></span>
19. <span data-ttu-id="9c3e8-127">Valitse Lisää.</span><span class="sxs-lookup"><span data-stu-id="9c3e8-127">Click Insert.</span></span>
20. <span data-ttu-id="9c3e8-128">Valitse Commerce-kanava.</span><span class="sxs-lookup"><span data-stu-id="9c3e8-128">Click Commerce channel.</span></span>
21. <span data-ttu-id="9c3e8-129">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="9c3e8-129">In the list, find and select the desired record.</span></span>
22. <span data-ttu-id="9c3e8-130">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="9c3e8-130">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="9c3e8-131">Voit lisätä tarvittavan määrän organisaatioyksiköitä.</span><span class="sxs-lookup"><span data-stu-id="9c3e8-131">You can add as many organization units as is required.</span></span>  
23. <span data-ttu-id="9c3e8-132">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="9c3e8-132">Click Save.</span></span>
24. <span data-ttu-id="9c3e8-133">Valitse Sulje.</span><span class="sxs-lookup"><span data-stu-id="9c3e8-133">Click Close.</span></span>
25. <span data-ttu-id="9c3e8-134">Valitse Julkaise, jolloin valintaikkuna avautuu.</span><span class="sxs-lookup"><span data-stu-id="9c3e8-134">Click Publish to open the drop dialog.</span></span>
26. <span data-ttu-id="9c3e8-135">Syötä päivämäärä ja kellonaika Voimaantulopäivä-kenttään.</span><span class="sxs-lookup"><span data-stu-id="9c3e8-135">In the Effective date field, enter a date and time.</span></span>
27. <span data-ttu-id="9c3e8-136">Syötä päivämäärä ja kellonaika Voimaantulopäivä-kenttään.</span><span class="sxs-lookup"><span data-stu-id="9c3e8-136">In the Effective date field, enter a date and time.</span></span>
28. <span data-ttu-id="9c3e8-137">Kirjoita arvo Kuvaa muutokset -kenttään.</span><span class="sxs-lookup"><span data-stu-id="9c3e8-137">In the Describe changes field, type a value.</span></span>
29. <span data-ttu-id="9c3e8-138">Valitse Julkaise.</span><span class="sxs-lookup"><span data-stu-id="9c3e8-138">Click Publish.</span></span>
30. <span data-ttu-id="9c3e8-139">Valitse Sulje.</span><span class="sxs-lookup"><span data-stu-id="9c3e8-139">Click Close.</span></span>



[!INCLUDE[footer-include](../../includes/footer-banner.md)]