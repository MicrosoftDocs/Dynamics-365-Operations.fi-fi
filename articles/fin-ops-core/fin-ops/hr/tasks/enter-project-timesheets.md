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
ms.search.scope: Operations, Talent
ms.search.region: Global
ms.search.industry: Service industries
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d2fd5c1e6c38c2e4380a8c8b061b08bce2dd43c8
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/27/2019
ms.locfileid: "2190439"
---
# <a name="enter-project-timesheets"></a><span data-ttu-id="a9594-103">Syötä projektin työaikaraportit</span><span class="sxs-lookup"><span data-stu-id="a9594-103">Enter project timesheets</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="a9594-104">Voit luoda tässä menettelyssä aikaraportin käyttämällä tyhjää aikaraporttilomaketta.</span><span class="sxs-lookup"><span data-stu-id="a9594-104">This procedure lets you create a timesheet by using an empty timesheet form.</span></span> <span data-ttu-id="a9594-105">Uusi aikaraportti voi perustua aiemman aikaraportin tietoihin tai **Omat suosikit** -sivun projekti- ja tehtävämäärityksiin.</span><span class="sxs-lookup"><span data-stu-id="a9594-105">The new timesheet can be based on information from a previous timesheet, or from project and activity assignments in the **My favorites** page.</span></span> <span data-ttu-id="a9594-106">Oletusarvoisesti **Kaikki työaikaraportit** -luettelosivu näyttää kaikki kuluvan kauden aikaraportit.</span><span class="sxs-lookup"><span data-stu-id="a9594-106">By default, the **All timesheets** list page displays all your timesheets for the current period.</span></span> <span data-ttu-id="a9594-107">Voit käyttää **Omat aikaraportit** -sivun **Näytä**-kentän avattavaa luetteloa suodattamaan aikaraporttiluetteloa ajanjakson tai raportin mukaan. Voit myös tarkastella sen avulla muiden työntekijöiden puolesta luotuja aikaraportteja.</span><span class="sxs-lookup"><span data-stu-id="a9594-107">You can use the drop-down list for the **Show** field in the **My timesheets** page to filter the timesheet list by time period or project, or to view timesheets that were created on behalf of other workers.</span></span> <span data-ttu-id="a9594-108">Tämän menettelyn luomisessa käytettiin USSI-yrityksen demotietoja.</span><span class="sxs-lookup"><span data-stu-id="a9594-108">The demo data company used to create this procedure is USSI.</span></span> 

1. <span data-ttu-id="a9594-109">Siirry **siirtymisruudussa** kohtaan **Moduulit > Projektinhallinta ja kirjanpito > Aikaraportit > Omat aikaraportit**.</span><span class="sxs-lookup"><span data-stu-id="a9594-109">In the **Navigation pane**, go to **Modules > Project management and accounting > Timesheets > My timesheets**.</span></span>
2. <span data-ttu-id="a9594-110">Anna uusi aikaraportti valitsemalla **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="a9594-110">To enter a new timesheet, click **New**.</span></span>
    - <span data-ttu-id="a9594-111">Avattavassa Resurssi-luettelo näyttää oletusarvoisesti nykyiselle käyttäjälle määritetyn työntekijän.</span><span class="sxs-lookup"><span data-stu-id="a9594-111">The Resource drop-down list shows the worker assigned to the current user, by default.</span></span>  
    - <span data-ttu-id="a9594-112">Jos käyttäjä on määritetty edustajaksi, tässä on luettelo nimistä, jotta käyttäjä voi täyttää aikaraportin heidän puolestaan.</span><span class="sxs-lookup"><span data-stu-id="a9594-112">If the user is designated as a delegate, this will list the names so that a user can enter a timesheet on their behalf.</span></span>  
3. <span data-ttu-id="a9594-113">Syötä **Päivämäärä**-kenttään päivämäärä.</span><span class="sxs-lookup"><span data-stu-id="a9594-113">In the **Date** field, enter a date.</span></span> <span data-ttu-id="a9594-114">Jos tämä vaihtoehto on valittu, aikaraporttiin luodaan uusia rivejä käyttämällä suosikeiksi määritettyjä aikaraporttiasetuksia.</span><span class="sxs-lookup"><span data-stu-id="a9594-114">If this option is selected, new timesheet lines will be created by using the timesheet settings that were configured as favorites.</span></span>  
4. <span data-ttu-id="a9594-115">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="a9594-115">Click **OK**.</span></span>
5. <span data-ttu-id="a9594-116">Valitse **Uusi rivi**.</span><span class="sxs-lookup"><span data-stu-id="a9594-116">Click **New line**.</span></span>
6. <span data-ttu-id="a9594-117">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="a9594-117">In the list, mark the selected row.</span></span> <span data-ttu-id="a9594-118">**Oikeushenkilö**-kentässä näkyy oletusarvoisesti nykyinen yritys.</span><span class="sxs-lookup"><span data-stu-id="a9594-118">The **Legal Entity** field displays the current Legal entity by default.</span></span>   
7. <span data-ttu-id="a9594-119">Avaa haku napsauttamalla **Projekti**-kentässä avattavan valikon painiketta.</span><span class="sxs-lookup"><span data-stu-id="a9594-119">In the **Project** field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="a9594-120">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="a9594-120">In the list, find and select the desired record.</span></span>
9. <span data-ttu-id="a9594-121">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="a9594-121">In the list, click the link in the selected row.</span></span>
10. <span data-ttu-id="a9594-122">Avaa haku napsauttamalla **Tehtävän numero** -kentässä avattavan valikon painiketta.</span><span class="sxs-lookup"><span data-stu-id="a9594-122">In the **Activity number** field, click the drop-down button to open the lookup.</span></span>
11. <span data-ttu-id="a9594-123">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="a9594-123">In the list, find and select the desired record.</span></span>
12. <span data-ttu-id="a9594-124">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="a9594-124">In the list, click the link in the selected row.</span></span>
13. <span data-ttu-id="a9594-125">Avaa haku napsauttamalla **Luokka**-kentässä avattavan valikon painiketta.</span><span class="sxs-lookup"><span data-stu-id="a9594-125">In the **Category** field, click the drop-down button to open the lookup.</span></span>
14. <span data-ttu-id="a9594-126">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="a9594-126">In the list, find and select the desired record.</span></span>
15. <span data-ttu-id="a9594-127">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="a9594-127">In the list, click the link in the selected row.</span></span>
16. <span data-ttu-id="a9594-128">Anna kunakin päivänä tehtyjen työtuntien määrä.</span><span class="sxs-lookup"><span data-stu-id="a9594-128">Enter the number of hours worked each day.</span></span> <span data-ttu-id="a9594-129">Kirjoita tunnit desimaalimuodossa.</span><span class="sxs-lookup"><span data-stu-id="a9594-129">Enter the hours in decimal format.</span></span> <span data-ttu-id="a9594-130">Jos olet työskennellyt kaksi tuntia viisitoista minuuttia, kirjoita 2,25.</span><span class="sxs-lookup"><span data-stu-id="a9594-130">For example, if you worked for two hours and fifteen minutes, enter 2.25.</span></span>   
17. <span data-ttu-id="a9594-131">**Rivin erittely** sisältää seuraavat vaihtoehdot:</span><span class="sxs-lookup"><span data-stu-id="a9594-131">In **Line details**, the following options are available:</span></span>
    - <span data-ttu-id="a9594-132">Lisää verojen ja taloushallinnon dimensioiden tiedot **Yleiset**- ja **Taloushallinnon dimensiot** -välilehtiin.</span><span class="sxs-lookup"><span data-stu-id="a9594-132">Add information about taxes and financial dimensions in the **General** and the **Financial Dimensions** tab.</span></span>
    - <span data-ttu-id="a9594-133">Lisää kommentit tuntilomakeriville **Kommentti** -välilehteen.</span><span class="sxs-lookup"><span data-stu-id="a9594-133">Add comments about the timesheet line in the **Comment** tab.</span></span>
20. <span data-ttu-id="a9594-134">Avaa pudotusvalikkoikkuna valitsemalla **toimintoruudussa** **Työnkulku**.</span><span class="sxs-lookup"><span data-stu-id="a9594-134">In the **Action pane**, click **Workflow** to open the drop dialog.</span></span>
21. <span data-ttu-id="a9594-135">Valitse **Lähetä**.</span><span class="sxs-lookup"><span data-stu-id="a9594-135">Click **Submit**.</span></span>
22. <span data-ttu-id="a9594-136">Valitse **Lähetä**.</span><span class="sxs-lookup"><span data-stu-id="a9594-136">Click **Submit**.</span></span>

