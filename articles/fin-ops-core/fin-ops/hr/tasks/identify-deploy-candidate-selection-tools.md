---
title: Ehdokkaiden valintatyökalujen määrittäminen ja käyttöönotto
description: Hyväksyttyjen ehdokkaiden joukon löytäminen avointen toimien täyttämistä varten voi olla vaikeaa erityisesti silloin, kun paikka vaatii eritystä osaamisaluejoukkoa.
author: andreabichsel
manager: AnnBe
ms.date: 11/20/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: HcmSkillMapping, HcmJobLookup, HcmSkillMappingLine, HcmPersonCertificate, CCHTMLPrintPreview
audience: Application User
ms.reviewer: anbichse
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f4e7ed6feaa1b5b27fcfc0ec99a2d75415fe7d6a
ms.sourcegitcommit: f5e31c34640add6d40308ac1365cc0ee60e60e24
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/08/2020
ms.locfileid: "4693061"
---
# <a name="identify-and-deploy-candidate-selection-tools"></a><span data-ttu-id="1c2f1-103">Ehdokkaiden valintatyökalujen määrittäminen ja käyttöönotto</span><span class="sxs-lookup"><span data-stu-id="1c2f1-103">Identify and deploy candidate selection tools</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="1c2f1-104">Hyväksyttyjen ehdokkaiden joukon löytäminen avointen toimien täyttämistä varten voi olla vaikeaa erityisesti silloin, kun paikka vaatii eritystä osaamisaluejoukkoa.</span><span class="sxs-lookup"><span data-stu-id="1c2f1-104">Finding a qualified pool of candidates to fill vacancies can be difficult, especially when a position requires a unique set of skills.</span></span>  <span data-ttu-id="1c2f1-105">Organisaatiossasi voi jo olla töissä tarvittuja osaamisalueita omaavia ehdokkaita.</span><span class="sxs-lookup"><span data-stu-id="1c2f1-105">However, candidates with the skills you need might already be employed in your organization.</span></span> <span data-ttu-id="1c2f1-106">Voit hakea nykyisten työntekijöiden tai uusien hakijoiden joukosta henkilöitä, jotka omaavat tietyt osaamisalueet.</span><span class="sxs-lookup"><span data-stu-id="1c2f1-106">You can search for a specific skill set among existing employees, or new applicants.</span></span> <span data-ttu-id="1c2f1-107">Näin rekrytoija voi nopeasti kerätä hakijoiden tiedot ja tarkistaa, kuka on hakenut avointa toimea nyt tai aiemmin, tai etsiä mahdollisia ehdokkaita aiemmin luoduista ehdokasryhmästä.</span><span class="sxs-lookup"><span data-stu-id="1c2f1-107">This allows a recruiter to quickly gather and screen applicants who have applied for open position now or in the past, or to find potential candidates from their existing pool of employees.</span></span> <span data-ttu-id="1c2f1-108">Tämän tehtävän tallennuksen avulla opit, miten osaamisaluekartoituksen toiminto auttaa etsimään oikean henkilön avoimeen toimeen.</span><span class="sxs-lookup"><span data-stu-id="1c2f1-108">Use this task recording to learn how the skill mapping functionality can help you find the right person for an open position.</span></span> <span data-ttu-id="1c2f1-109">Tämän menettelyn luomisessa käytetty esittely-yritys on USMF.</span><span class="sxs-lookup"><span data-stu-id="1c2f1-109">The demo data company used to create this procedure is USMF.</span></span>

1. <span data-ttu-id="1c2f1-110">Siirry kohtaan Henkilöstöhallinto > Osaamistiedot > Osaamisanalyysi > Osaamisaluekartoituksen profiilit.</span><span class="sxs-lookup"><span data-stu-id="1c2f1-110">Go to Human resources > Competencies > Skill analysis > Skill mapping profiles.</span></span>
2. <span data-ttu-id="1c2f1-111">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="1c2f1-111">Click New.</span></span>
3. <span data-ttu-id="1c2f1-112">Syötä Osaamisaluekartoitus-kenttään osaamisaluekartoituksen nimi.</span><span class="sxs-lookup"><span data-stu-id="1c2f1-112">In the Skill mapping field, enter a name for your skill mapping.</span></span>  <span data-ttu-id="1c2f1-113">Esimerkki: Kirjanpitäjä.</span><span class="sxs-lookup"><span data-stu-id="1c2f1-113">Example: Accountant.</span></span>
4. <span data-ttu-id="1c2f1-114">Syötä Kuvaus-kenttään osaamisaluekartoituksen kuvaus.</span><span class="sxs-lookup"><span data-stu-id="1c2f1-114">In the Description field, enter a description of the skill mapping..</span></span>
5. <span data-ttu-id="1c2f1-115">Syötä Päivämäärään-kenttään päivämäärä.</span><span class="sxs-lookup"><span data-stu-id="1c2f1-115">In the Date field, enter a date.</span></span>
6. <span data-ttu-id="1c2f1-116">Valitse Nouda profiili.</span><span class="sxs-lookup"><span data-stu-id="1c2f1-116">Click Retrieve profile.</span></span>
    * <span data-ttu-id="1c2f1-117">Nouda profiili -kohdan avulla voit tuoda valitun henkilön, työn tai kurssin todistus-, osaamisalue- ja koulutustiedot haun perusteeksi.</span><span class="sxs-lookup"><span data-stu-id="1c2f1-117">Use Retrieve profile to pull in the Certificate, Skill, and Education data from a selected Person, Job or Course as the basis for your search.</span></span>   <span data-ttu-id="1c2f1-118">Tämän jälkeen voit lisätä tai poistaa ehtoja, määrittää, ovatko ehdot valinnaisia ja määrittää ehtojen tärkeyden.</span><span class="sxs-lookup"><span data-stu-id="1c2f1-118">You can then add or remove criteria, state if the criteria is optional and rank the importance of the criteria.</span></span>  
7. <span data-ttu-id="1c2f1-119">Valitse Työ.</span><span class="sxs-lookup"><span data-stu-id="1c2f1-119">Click Job.</span></span>
8. <span data-ttu-id="1c2f1-120">Syötä tai valitse arvo Työ-kenttään.</span><span class="sxs-lookup"><span data-stu-id="1c2f1-120">In the Job field, enter or select a value.</span></span>
9. <span data-ttu-id="1c2f1-121">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="1c2f1-121">Click OK.</span></span>
10. <span data-ttu-id="1c2f1-122">Laajenna Alue-pikavälilehti ja lisää tietoja, kuten osasto.</span><span class="sxs-lookup"><span data-stu-id="1c2f1-122">Expand the Range FastTab, and add any additional information, such as department.</span></span>
11. <span data-ttu-id="1c2f1-123">Laajenna Todistukset-pikavälilehti, kun haluat tarkastella tai muokata todistuksia.</span><span class="sxs-lookup"><span data-stu-id="1c2f1-123">Expand the Certificates FastTab to view or edit the certificates.</span></span>
12. <span data-ttu-id="1c2f1-124">Laajenna Osaamisalueet-pikavälilehti, kun haluat tarkastella tai muokata osaamisalueita.</span><span class="sxs-lookup"><span data-stu-id="1c2f1-124">Expand the Skills FastTab to view or edit the skills.</span></span>
13. <span data-ttu-id="1c2f1-125">Laajenna Koulutus-pikavälilehti, kun haluat tarkastella tai muokata koulutusvaatimuksia.</span><span class="sxs-lookup"><span data-stu-id="1c2f1-125">Expand the Education FastTab to view or edit the education criteria.</span></span>
14. <span data-ttu-id="1c2f1-126">Valitse Suorita.</span><span class="sxs-lookup"><span data-stu-id="1c2f1-126">Click Execute.</span></span>
15. <span data-ttu-id="1c2f1-127">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="1c2f1-127">Click OK.</span></span>
16. <span data-ttu-id="1c2f1-128">Valitse Tulos.</span><span class="sxs-lookup"><span data-stu-id="1c2f1-128">Click Result.</span></span>
17. <span data-ttu-id="1c2f1-129">Valitse Tulos.</span><span class="sxs-lookup"><span data-stu-id="1c2f1-129">Click Result.</span></span>
18. <span data-ttu-id="1c2f1-130">Valitse Jatka.</span><span class="sxs-lookup"><span data-stu-id="1c2f1-130">Click Resume.</span></span>
19. <span data-ttu-id="1c2f1-131">Valitse Todistukset.</span><span class="sxs-lookup"><span data-stu-id="1c2f1-131">Click Certificates.</span></span>
    * <span data-ttu-id="1c2f1-132">Voit noutaa lisää kunkin luettelossa olevan henkilön koulutusta, osaamisaluetta ja ammattikokemusta koskevia tietoja.</span><span class="sxs-lookup"><span data-stu-id="1c2f1-132">You can drill further into each person listed and see details regarding their education, skills, and professional experience.</span></span>  
20. <span data-ttu-id="1c2f1-133">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="1c2f1-133">Close the page.</span></span>
21. <span data-ttu-id="1c2f1-134">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="1c2f1-134">Close the page.</span></span>
22. <span data-ttu-id="1c2f1-135">Valitse tulokset uudelleen.</span><span class="sxs-lookup"><span data-stu-id="1c2f1-135">Select result again.</span></span>
23. <span data-ttu-id="1c2f1-136">Valitse Raportti.</span><span class="sxs-lookup"><span data-stu-id="1c2f1-136">Click Report.</span></span>
    * <span data-ttu-id="1c2f1-137">Parhaat vastaavuudet ovat raportin alkuosassa.</span><span class="sxs-lookup"><span data-stu-id="1c2f1-137">The report will list the best matches at the top of the report.</span></span>  <span data-ttu-id="1c2f1-138">Näet, että kyseinen osaamisalueaukkoelementti on luettelossa.</span><span class="sxs-lookup"><span data-stu-id="1c2f1-138">You can see that a gap element is listed.</span></span>  <span data-ttu-id="1c2f1-139">Tämä on osaamisaluekartoituksessa mainitun tason ja henkilölle määritetyn tason välinen ero.</span><span class="sxs-lookup"><span data-stu-id="1c2f1-139">This is the difference between the level that was listed on the skill mapping, and the level of the skill that is assigned to the person.</span></span>  
24. <span data-ttu-id="1c2f1-140">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="1c2f1-140">Close the page.</span></span>
25. <span data-ttu-id="1c2f1-141">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="1c2f1-141">Click Save.</span></span>

