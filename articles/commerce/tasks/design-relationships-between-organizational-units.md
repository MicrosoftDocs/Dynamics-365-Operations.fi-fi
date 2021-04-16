---
title: Organisaatioyksiköiden välisten suhteiden suunnittelu
description: Menettely opastaa organisaatioyksiköiden välisten suhteiden suunnittelemisessa.
author: mugunthanm
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: OMHierarchyManager, OMHierarchyPurposeAssociation, OMHierarchySelection, HierarchyDesigner, OMNodeSelection,  HierarchyPublishAndCloseForm
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.search.industry: Retail
ms.author: mumani
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 660db4a846eda7fb4b62ba6664acef3e8f718d53
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2021
ms.locfileid: "5796775"
---
# <a name="design-the-relationships-between-organizational-units"></a><span data-ttu-id="fcaa5-103">Organisaatioyksiköiden välisten suhteiden suunnittelu</span><span class="sxs-lookup"><span data-stu-id="fcaa5-103">Design the relationships between organizational units</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="fcaa5-104">Menettely opastaa organisaatioyksiköiden välisten suhteiden suunnittelemisessa.</span><span class="sxs-lookup"><span data-stu-id="fcaa5-104">This procedure walks through how to design the relationship between organizational units.</span></span> <span data-ttu-id="fcaa5-105">Luo uuden organisaation tarkoitus, ennen kuin määrität suhteen. Voit myös käyttää aiemmin luotua organisaation tarkoitusta.</span><span class="sxs-lookup"><span data-stu-id="fcaa5-105">You must create a new organization purpose before defining the relationship, or you can use the existing organization purpose.</span></span> <span data-ttu-id="fcaa5-106">Tämä menettely tehdään valmiiksi käyttämällä esittely-yritystä USRT.</span><span class="sxs-lookup"><span data-stu-id="fcaa5-106">The demo data company used to complete this procedure is USRT.</span></span> <span data-ttu-id="fcaa5-107">Tämä tehtävä on tarkoitettu järjestelmänvalvojan roolille.</span><span class="sxs-lookup"><span data-stu-id="fcaa5-107">This task is intended for the administrator role.</span></span>

1. <span data-ttu-id="fcaa5-108">Valitse Organisaation hallinto > Organisaatiot > Organisaatiohierarkiat.</span><span class="sxs-lookup"><span data-stu-id="fcaa5-108">Go to Organization administration > Organizations > Organization hierarchies.</span></span>
2. <span data-ttu-id="fcaa5-109">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="fcaa5-109">Click New.</span></span>
3. <span data-ttu-id="fcaa5-110">Kirjoita arvo Nimi-kenttään.</span><span class="sxs-lookup"><span data-stu-id="fcaa5-110">In the Name field, type a value.</span></span>
4. <span data-ttu-id="fcaa5-111">Valitse Määritä tarkoitus.</span><span class="sxs-lookup"><span data-stu-id="fcaa5-111">Click Assign purpose.</span></span>
5. <span data-ttu-id="fcaa5-112">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="fcaa5-112">In the list, find and select the desired record.</span></span>
6. <span data-ttu-id="fcaa5-113">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="fcaa5-113">Click Add.</span></span>
7. <span data-ttu-id="fcaa5-114">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="fcaa5-114">In the list, find and select the desired record.</span></span>
8. <span data-ttu-id="fcaa5-115">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="fcaa5-115">Click OK.</span></span>
    * <span data-ttu-id="fcaa5-116">Voit valita organisaation vaatiman määrän organisaation tarkoituksia.</span><span class="sxs-lookup"><span data-stu-id="fcaa5-116">You can select as many organization purposes as required for your organization.</span></span>  
9. <span data-ttu-id="fcaa5-117">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="fcaa5-117">In the list, find and select the desired record.</span></span>
10. <span data-ttu-id="fcaa5-118">Valitse Aseta oletukseksi.</span><span class="sxs-lookup"><span data-stu-id="fcaa5-118">Click Set as default.</span></span>
11. <span data-ttu-id="fcaa5-119">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="fcaa5-119">Close the page.</span></span>
12. <span data-ttu-id="fcaa5-120">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="fcaa5-120">Click Save.</span></span>
13. <span data-ttu-id="fcaa5-121">Valitse Näytä.</span><span class="sxs-lookup"><span data-stu-id="fcaa5-121">Click View.</span></span>
14. <span data-ttu-id="fcaa5-122">Valitse Muokkaa.</span><span class="sxs-lookup"><span data-stu-id="fcaa5-122">Click Edit.</span></span>
15. <span data-ttu-id="fcaa5-123">Valitse Lisää.</span><span class="sxs-lookup"><span data-stu-id="fcaa5-123">Click Insert.</span></span>
16. <span data-ttu-id="fcaa5-124">Valitse Liiketoimintayksikkö.</span><span class="sxs-lookup"><span data-stu-id="fcaa5-124">Click Business unit.</span></span>
17. <span data-ttu-id="fcaa5-125">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="fcaa5-125">In the list, find and select the desired record.</span></span>
18. <span data-ttu-id="fcaa5-126">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="fcaa5-126">In the list, click the link in the selected row.</span></span>
19. <span data-ttu-id="fcaa5-127">Valitse Lisää.</span><span class="sxs-lookup"><span data-stu-id="fcaa5-127">Click Insert.</span></span>
20. <span data-ttu-id="fcaa5-128">Valitse Commerce-kanava.</span><span class="sxs-lookup"><span data-stu-id="fcaa5-128">Click Commerce channel.</span></span>
21. <span data-ttu-id="fcaa5-129">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="fcaa5-129">In the list, find and select the desired record.</span></span>
22. <span data-ttu-id="fcaa5-130">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="fcaa5-130">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="fcaa5-131">Voit lisätä tarvittavan määrän organisaatioyksiköitä.</span><span class="sxs-lookup"><span data-stu-id="fcaa5-131">You can add as many organization units as is required.</span></span>  
23. <span data-ttu-id="fcaa5-132">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="fcaa5-132">Click Save.</span></span>
24. <span data-ttu-id="fcaa5-133">Valitse Sulje.</span><span class="sxs-lookup"><span data-stu-id="fcaa5-133">Click Close.</span></span>
25. <span data-ttu-id="fcaa5-134">Valitse Julkaise, jolloin valintaikkuna avautuu.</span><span class="sxs-lookup"><span data-stu-id="fcaa5-134">Click Publish to open the drop dialog.</span></span>
26. <span data-ttu-id="fcaa5-135">Syötä päivämäärä ja kellonaika Voimaantulopäivä-kenttään.</span><span class="sxs-lookup"><span data-stu-id="fcaa5-135">In the Effective date field, enter a date and time.</span></span>
27. <span data-ttu-id="fcaa5-136">Syötä päivämäärä ja kellonaika Voimaantulopäivä-kenttään.</span><span class="sxs-lookup"><span data-stu-id="fcaa5-136">In the Effective date field, enter a date and time.</span></span>
28. <span data-ttu-id="fcaa5-137">Kirjoita arvo Kuvaa muutokset -kenttään.</span><span class="sxs-lookup"><span data-stu-id="fcaa5-137">In the Describe changes field, type a value.</span></span>
29. <span data-ttu-id="fcaa5-138">Valitse Julkaise.</span><span class="sxs-lookup"><span data-stu-id="fcaa5-138">Click Publish.</span></span>
30. <span data-ttu-id="fcaa5-139">Valitse Sulje.</span><span class="sxs-lookup"><span data-stu-id="fcaa5-139">Click Close.</span></span>



[!INCLUDE[footer-include](../../includes/footer-banner.md)]