---
title: Syötä projektin työaikaraportit
description: Voit luoda tässä menettelyssä aikaraportin käyttämällä tyhjää aikaraporttilomaketta.
author: andreabichsel
manager: AnnBe
ms.date: 08/08/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Operations, Human Resources
ms.search.region: Global
ms.search.industry: Service industries
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 10dbb43cec47a758d11362947f27932a4911911a
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/13/2020
ms.locfileid: "4418350"
---
# <a name="enter-project-timesheets"></a><span data-ttu-id="bb610-103">Syötä projektin työaikaraportit</span><span class="sxs-lookup"><span data-stu-id="bb610-103">Enter project timesheets</span></span>



<span data-ttu-id="bb610-104">Voit luoda tässä menettelyssä aikaraportin käyttämällä tyhjää aikaraporttilomaketta.</span><span class="sxs-lookup"><span data-stu-id="bb610-104">This procedure lets you create a timesheet by using an empty timesheet form.</span></span> <span data-ttu-id="bb610-105">Uusi aikaraportti voi perustua aiemman aikaraportin tietoihin tai **Omat suosikit** -sivun projekti- ja tehtävämäärityksiin.</span><span class="sxs-lookup"><span data-stu-id="bb610-105">The new timesheet can be based on information from a previous timesheet, or from project and activity assignments in the **My favorites** page.</span></span> <span data-ttu-id="bb610-106">Oletusarvoisesti **Kaikki työaikaraportit** -luettelosivu näyttää kaikki kuluvan kauden aikaraportit.</span><span class="sxs-lookup"><span data-stu-id="bb610-106">By default, the **All timesheets** list page displays all your timesheets for the current period.</span></span> <span data-ttu-id="bb610-107">Voit käyttää **Omat aikaraportit** -sivun **Näytä**-kentän avattavaa luetteloa suodattamaan aikaraporttiluetteloa ajanjakson tai raportin mukaan. Voit myös tarkastella sen avulla muiden työntekijöiden puolesta luotuja aikaraportteja.</span><span class="sxs-lookup"><span data-stu-id="bb610-107">You can use the drop-down list for the **Show** field in the **My timesheets** page to filter the timesheet list by time period or project, or to view timesheets that were created on behalf of other workers.</span></span> <span data-ttu-id="bb610-108">Tämän menettelyn luomisessa käytettiin USSI-yrityksen demotietoja.</span><span class="sxs-lookup"><span data-stu-id="bb610-108">The demo data company used to create this procedure is USSI.</span></span> 

1. <span data-ttu-id="bb610-109">Siirry **siirtymisruudussa** kohtaan **Moduulit > Projektinhallinta ja kirjanpito > Aikaraportit > Omat aikaraportit**.</span><span class="sxs-lookup"><span data-stu-id="bb610-109">In the **Navigation pane**, go to **Modules > Project management and accounting > Timesheets > My timesheets**.</span></span>
2. <span data-ttu-id="bb610-110">Anna uusi aikaraportti valitsemalla **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="bb610-110">To enter a new timesheet, click **New**.</span></span>
    - <span data-ttu-id="bb610-111">Avattavassa Resurssi-luettelo näyttää oletusarvoisesti nykyiselle käyttäjälle määritetyn työntekijän.</span><span class="sxs-lookup"><span data-stu-id="bb610-111">The Resource drop-down list shows the worker assigned to the current user, by default.</span></span>  
    - <span data-ttu-id="bb610-112">Jos käyttäjä on määritetty edustajaksi, tässä on luettelo nimistä, jotta käyttäjä voi täyttää aikaraportin heidän puolestaan.</span><span class="sxs-lookup"><span data-stu-id="bb610-112">If the user is designated as a delegate, this will list the names so that a user can enter a timesheet on their behalf.</span></span>  
3. <span data-ttu-id="bb610-113">Syötä **Päivämäärä**-kenttään päivämäärä.</span><span class="sxs-lookup"><span data-stu-id="bb610-113">In the **Date** field, enter a date.</span></span> <span data-ttu-id="bb610-114">Jos tämä vaihtoehto on valittu, aikaraporttiin luodaan uusia rivejä käyttämällä suosikeiksi määritettyjä aikaraporttiasetuksia.</span><span class="sxs-lookup"><span data-stu-id="bb610-114">If this option is selected, new timesheet lines will be created by using the timesheet settings that were configured as favorites.</span></span>  
4. <span data-ttu-id="bb610-115">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="bb610-115">Click **OK**.</span></span>
5. <span data-ttu-id="bb610-116">Valitse **Uusi rivi**.</span><span class="sxs-lookup"><span data-stu-id="bb610-116">Click **New line**.</span></span>
6. <span data-ttu-id="bb610-117">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="bb610-117">In the list, mark the selected row.</span></span> <span data-ttu-id="bb610-118">**Oikeushenkilö**-kentässä näkyy oletusarvoisesti nykyinen yritys.</span><span class="sxs-lookup"><span data-stu-id="bb610-118">The **Legal Entity** field displays the current Legal entity by default.</span></span>   
7. <span data-ttu-id="bb610-119">Avaa haku napsauttamalla **Projekti**-kentässä avattavan valikon painiketta.</span><span class="sxs-lookup"><span data-stu-id="bb610-119">In the **Project** field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="bb610-120">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="bb610-120">In the list, find and select the desired record.</span></span>
9. <span data-ttu-id="bb610-121">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="bb610-121">In the list, click the link in the selected row.</span></span>
10. <span data-ttu-id="bb610-122">Avaa haku napsauttamalla **Tehtävän numero** -kentässä avattavan valikon painiketta.</span><span class="sxs-lookup"><span data-stu-id="bb610-122">In the **Activity number** field, click the drop-down button to open the lookup.</span></span>
11. <span data-ttu-id="bb610-123">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="bb610-123">In the list, find and select the desired record.</span></span>
12. <span data-ttu-id="bb610-124">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="bb610-124">In the list, click the link in the selected row.</span></span>
13. <span data-ttu-id="bb610-125">Avaa haku napsauttamalla **Luokka**-kentässä avattavan valikon painiketta.</span><span class="sxs-lookup"><span data-stu-id="bb610-125">In the **Category** field, click the drop-down button to open the lookup.</span></span>
14. <span data-ttu-id="bb610-126">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="bb610-126">In the list, find and select the desired record.</span></span>
15. <span data-ttu-id="bb610-127">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="bb610-127">In the list, click the link in the selected row.</span></span>
16. <span data-ttu-id="bb610-128">Anna kunakin päivänä tehtyjen työtuntien määrä.</span><span class="sxs-lookup"><span data-stu-id="bb610-128">Enter the number of hours worked each day.</span></span> <span data-ttu-id="bb610-129">Kirjoita tunnit desimaalimuodossa.</span><span class="sxs-lookup"><span data-stu-id="bb610-129">Enter the hours in decimal format.</span></span> <span data-ttu-id="bb610-130">Jos olet työskennellyt kaksi tuntia viisitoista minuuttia, kirjoita 2,25.</span><span class="sxs-lookup"><span data-stu-id="bb610-130">For example, if you worked for two hours and fifteen minutes, enter 2.25.</span></span>   
17. <span data-ttu-id="bb610-131">**Rivin erittely** sisältää seuraavat vaihtoehdot:</span><span class="sxs-lookup"><span data-stu-id="bb610-131">In **Line details**, the following options are available:</span></span>
    - <span data-ttu-id="bb610-132">Lisää verojen ja taloushallinnon dimensioiden tiedot **Yleiset**- ja **Taloushallinnon dimensiot** -välilehtiin.</span><span class="sxs-lookup"><span data-stu-id="bb610-132">Add information about taxes and financial dimensions in the **General** and the **Financial Dimensions** tab.</span></span>
    - <span data-ttu-id="bb610-133">Lisää kommentit tuntilomakeriville **Kommentti** -välilehteen.</span><span class="sxs-lookup"><span data-stu-id="bb610-133">Add comments about the timesheet line in the **Comment** tab.</span></span>
20. <span data-ttu-id="bb610-134">Avaa pudotusvalikkoikkuna valitsemalla **toimintoruudussa** **Työnkulku**.</span><span class="sxs-lookup"><span data-stu-id="bb610-134">In the **Action pane**, click **Workflow** to open the drop dialog.</span></span>
21. <span data-ttu-id="bb610-135">Valitse **Lähetä**.</span><span class="sxs-lookup"><span data-stu-id="bb610-135">Click **Submit**.</span></span>
22. <span data-ttu-id="bb610-136">Valitse **Lähetä**.</span><span class="sxs-lookup"><span data-stu-id="bb610-136">Click **Submit**.</span></span>

