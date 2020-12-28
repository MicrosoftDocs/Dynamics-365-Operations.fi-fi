---
title: Määritä työntekijän vamma- ja sairaustiedot
description: Tapaturmien ja sairauksien asetukset -tehtävän opastus kannattaa suorittaa ensin, sillä joitakin asetustietoja käytetään tässä tehtävässä.
author: andreabichsel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: HRMInjuryIncident, HcmWorkerLookUp, HcmPersonnelManagementWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 367834e7e02d2061732f46d8e697044e7c49b884
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/13/2020
ms.locfileid: "4418293"
---
# <a name="maintain-employee-injury-and-illness-information"></a><span data-ttu-id="432ad-103">Määritä työntekijän vamma- ja sairaustiedot</span><span class="sxs-lookup"><span data-stu-id="432ad-103">Maintain employee injury and illness information</span></span>



<span data-ttu-id="432ad-104">Tapaturmien ja sairauksien asetukset -tehtävän opastus kannattaa suorittaa ensin, sillä joitakin asetustietoja käytetään tässä tehtävässä.</span><span class="sxs-lookup"><span data-stu-id="432ad-104">It is recommended to complete the 'Setup injury and illness' task guide first, as some of the setup information is used here.</span></span> 



<span data-ttu-id="432ad-105">Tämän tehtävän tallenteessa käsitellään tapaturma- tai sairaustapauksen perusvaiheet.</span><span class="sxs-lookup"><span data-stu-id="432ad-105">This task recording covers the basic steps to creating an injury or illness case.</span></span> <span data-ttu-id="432ad-106">Tapaturman tai sairauden tietojen seurannan lisäksi myös tapauksen tilaa seurataan.</span><span class="sxs-lookup"><span data-stu-id="432ad-106">Besides tracking the details of the injury or illness, there is a case status that is tracked as well.</span></span>  <span data-ttu-id="432ad-107">Tapauksen oletusarvo on Avoin-tila.</span><span class="sxs-lookup"><span data-stu-id="432ad-107">The case defaults with an 'open' status.</span></span>  <span data-ttu-id="432ad-108">Tiloja voi hallita sivun yläosan Tapauksen tila -valikkovaihtoehdolla.</span><span class="sxs-lookup"><span data-stu-id="432ad-108">The statuses can be managed from the 'Case status' menu item at the top of the page.</span></span>

1. <span data-ttu-id="432ad-109">Valitse Henkilöstöhallinto > Työntekijät > Tapaturma ja sairaus > Tapaturma- tai sairastapaukset.</span><span class="sxs-lookup"><span data-stu-id="432ad-109">Go to Human resources > Workers > Injury and illness > Injury or illness incidents.</span></span>
2. <span data-ttu-id="432ad-110">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="432ad-110">Click New.</span></span>
3. <span data-ttu-id="432ad-111">Kirjoita Tapauksen kuvaus -kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="432ad-111">In the Case description field, type a value.</span></span>
    * <span data-ttu-id="432ad-112">Esimerkki: rannevamma</span><span class="sxs-lookup"><span data-stu-id="432ad-112">Example:  Wrist injury</span></span>  
4. <span data-ttu-id="432ad-113">Anna tai valitse Työntekijä-kentässä arvo.</span><span class="sxs-lookup"><span data-stu-id="432ad-113">In the Worker field, enter or select a value.</span></span>
    * <span data-ttu-id="432ad-114">Esimerkki: Ahmed Barnett</span><span class="sxs-lookup"><span data-stu-id="432ad-114">Example: Ahmed Barnett</span></span>  
5. <span data-ttu-id="432ad-115">Anna Tapauksen päivämäärä ja aika -kentässä päivämäärä ja aika.</span><span class="sxs-lookup"><span data-stu-id="432ad-115">In the Date and time of incident field, enter a date and time.</span></span>
    * <span data-ttu-id="432ad-116">Esimerkki: 20.1.2016 klo 10.00</span><span class="sxs-lookup"><span data-stu-id="432ad-116">Example:  1/20/2016 10:00 AM</span></span>  
6. <span data-ttu-id="432ad-117">Anna tai valitse Tapaturma- tai sairaustyyppi -kentässä arvo.</span><span class="sxs-lookup"><span data-stu-id="432ad-117">In the Injury or illness type field, enter or select a value.</span></span>
    * <span data-ttu-id="432ad-118">Esimerkki: Murtuma</span><span class="sxs-lookup"><span data-stu-id="432ad-118">Example:  Fracture</span></span>  
7. <span data-ttu-id="432ad-119">Anna tai valitse Kehon osa -kentässä arvo.</span><span class="sxs-lookup"><span data-stu-id="432ad-119">In the Body part field, enter or select a value.</span></span>
    * <span data-ttu-id="432ad-120">Esimerkki: Ranne</span><span class="sxs-lookup"><span data-stu-id="432ad-120">Example:  Wrist</span></span>  
8. <span data-ttu-id="432ad-121">Anna tai valitse Seuraustyyppi-kentässä arvo.</span><span class="sxs-lookup"><span data-stu-id="432ad-121">In the Outcome type field, enter or select a value.</span></span>
    * <span data-ttu-id="432ad-122">Esimerkki: Terapia</span><span class="sxs-lookup"><span data-stu-id="432ad-122">Example:  Therapy</span></span>  
9. <span data-ttu-id="432ad-123">Anna Raportoitu päivämäärä ja aika -kentässä päivämäärä ja aika.</span><span class="sxs-lookup"><span data-stu-id="432ad-123">In the Date and time reported field, enter a date and time.</span></span>
    * <span data-ttu-id="432ad-124">Raportoidun päivämäärän ja ajan on oltava myöhäisempi kuin tapauksen päivämäärä ja aika.</span><span class="sxs-lookup"><span data-stu-id="432ad-124">The date and time reported must be later than the date and time of incident.</span></span>  
10. <span data-ttu-id="432ad-125">Anna tai valitse Ilmoittaja-kentässä arvo.</span><span class="sxs-lookup"><span data-stu-id="432ad-125">In the Person who reported case field, enter or select a value.</span></span>
    * <span data-ttu-id="432ad-126">Tämä voi olla työntekijä tai joku muu tapahtuman todistaja.</span><span class="sxs-lookup"><span data-stu-id="432ad-126">This could be the employee or another witness to the incident.</span></span>  <span data-ttu-id="432ad-127">Esimerkki: Ahmed Barnett</span><span class="sxs-lookup"><span data-stu-id="432ad-127">Example: Ahmed Barnett</span></span>  
11. <span data-ttu-id="432ad-128">Laajenna Tapaus-osa.</span><span class="sxs-lookup"><span data-stu-id="432ad-128">Expand the Incident section.</span></span>
12. <span data-ttu-id="432ad-129">Kirjoita Tapahtumapaikka -kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="432ad-129">In the Where incident occurred field, type a value.</span></span>
    * <span data-ttu-id="432ad-130">Esimerkki: varasto</span><span class="sxs-lookup"><span data-stu-id="432ad-130">Example:  Warehouse</span></span>  
13. <span data-ttu-id="432ad-131">Valitse Työpaikalla-kentässä Kyllä.</span><span class="sxs-lookup"><span data-stu-id="432ad-131">Select Yes in the On work premises field.</span></span>
    * <span data-ttu-id="432ad-132">Jos tapaus sattui työpaikalla, valitse kyllä.</span><span class="sxs-lookup"><span data-stu-id="432ad-132">If the incident occurred on work premises, select yes.</span></span>  
14. <span data-ttu-id="432ad-133">Anna Työn aloituspäivä ja -aika -kentässä päivämäärä ja aika.</span><span class="sxs-lookup"><span data-stu-id="432ad-133">In the Date and time began work field, enter a date and time.</span></span>
    * <span data-ttu-id="432ad-134">Anna päivämäärä ja aika, jolloin kyseinen henkilö aloitti työnteon ennen tapaushetkeä.</span><span class="sxs-lookup"><span data-stu-id="432ad-134">Enter the date and time that affected individual started working, prior to the incident occurring.</span></span>  
15. <span data-ttu-id="432ad-135">Kirjoita Työntekijän työ tai tehtävä -kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="432ad-135">In the Employee job or task field, type a value.</span></span>
    * <span data-ttu-id="432ad-136">Anna työ tai tehtävä, jota työntekijä oli suorittamassa tapaushetkellä.</span><span class="sxs-lookup"><span data-stu-id="432ad-136">Enter the job or task the worker was performing when the incident occurred.</span></span>  <span data-ttu-id="432ad-137">Esimerkki: laatikoiden kuormaaminen</span><span class="sxs-lookup"><span data-stu-id="432ad-137">Example:  Loading boxes</span></span>  
16. <span data-ttu-id="432ad-138">Kirjoita Tapauksen syy -kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="432ad-138">In the Cause of incident field, type a value.</span></span>
    * <span data-ttu-id="432ad-139">Anna tapauksen syy.</span><span class="sxs-lookup"><span data-stu-id="432ad-139">Enter the cause of the incident.</span></span>  <span data-ttu-id="432ad-140">Esimerkki: liukastuminen kostealla lattialla</span><span class="sxs-lookup"><span data-stu-id="432ad-140">Example:  Slipped on wet floor</span></span>  
17. <span data-ttu-id="432ad-141">Anna tai valitse Vakavuustaso-kentässä arvo.</span><span class="sxs-lookup"><span data-stu-id="432ad-141">In the Severity level field, enter or select a value.</span></span>
18. <span data-ttu-id="432ad-142">Kirjoita Suoritettava toimenpide -kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="432ad-142">In the Action to be taken field, type a value.</span></span>
    * <span data-ttu-id="432ad-143">Esimerkki: valuneen nesteen kuivaaminen välittömästi</span><span class="sxs-lookup"><span data-stu-id="432ad-143">Example:  Clean up spills promptly</span></span>  
19. <span data-ttu-id="432ad-144">Lisää Poissaolon odotettu kesto päivinä -kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="432ad-144">In the Expected days away from work field, enter a number.</span></span>
    * <span data-ttu-id="432ad-145">Ilmoita kuinka monta päivää henkilön oletetaan olevan pois töistä.</span><span class="sxs-lookup"><span data-stu-id="432ad-145">Enter the number of days that the individual is expected to be away from work.</span></span>  <span data-ttu-id="432ad-146">Kun henkilö palaa töihin, päivitä Poissaolopäivät-kenttä todellisilla poissaolopäivillä.</span><span class="sxs-lookup"><span data-stu-id="432ad-146">Once the individual returns to work, update the 'Days away from work' field with the actual number of days away.</span></span>  
20. <span data-ttu-id="432ad-147">Laajenna Tapaturman tai sairauden kustannukset -osa.</span><span class="sxs-lookup"><span data-stu-id="432ad-147">Expand the Injury or illness costs section.</span></span>
21. <span data-ttu-id="432ad-148">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="432ad-148">Click Add.</span></span>
22. <span data-ttu-id="432ad-149">Syötä Päivämäärään-kenttään päivämäärä.</span><span class="sxs-lookup"><span data-stu-id="432ad-149">In the Date field, enter a date.</span></span>
23. <span data-ttu-id="432ad-150">Anna tai valitse Kustannustyyppi-kentässä arvo.</span><span class="sxs-lookup"><span data-stu-id="432ad-150">In the Cost type field, enter or select a value.</span></span>
    * <span data-ttu-id="432ad-151">Esimerkki: Terapia Voit antaa myös summan ja liittää kustannukseen tukidokumentaation, kuten laskut tai lääkärin kommentit.</span><span class="sxs-lookup"><span data-stu-id="432ad-151">Example:  Therapy    You can also enter in an amount, and attach any supporting documentation such as invoices or doctor's notes to the cost.</span></span>  
24. <span data-ttu-id="432ad-152">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="432ad-152">Click Add.</span></span>
25. <span data-ttu-id="432ad-153">Syötä Päivämäärään-kenttään päivämäärä.</span><span class="sxs-lookup"><span data-stu-id="432ad-153">In the Date field, enter a date.</span></span>
26. <span data-ttu-id="432ad-154">Anna tai valitse Kustannustyyppi-kentässä arvo.</span><span class="sxs-lookup"><span data-stu-id="432ad-154">In the Cost type field, enter or select a value.</span></span>
    * <span data-ttu-id="432ad-155">Esimerkki: lääkäri</span><span class="sxs-lookup"><span data-stu-id="432ad-155">Example: Doctor</span></span>  
27. <span data-ttu-id="432ad-156">Laajenna Vamman tai sairauden hoito -osa.</span><span class="sxs-lookup"><span data-stu-id="432ad-156">Expand the Injury or illness treatments section.</span></span>
28. <span data-ttu-id="432ad-157">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="432ad-157">Click Add.</span></span>
29. <span data-ttu-id="432ad-158">Anna Hoitopäivämäärä-kentässä päivämäärä ja aika.</span><span class="sxs-lookup"><span data-stu-id="432ad-158">In the Treatment date field, enter a date and time.</span></span>
30. <span data-ttu-id="432ad-159">Anna tai valitse Hoitotyyppi-kentässä arvo.</span><span class="sxs-lookup"><span data-stu-id="432ad-159">In the Treatment type field, enter or select a value.</span></span>
    * <span data-ttu-id="432ad-160">Esimerkki: lasta</span><span class="sxs-lookup"><span data-stu-id="432ad-160">Example:  Splint</span></span>  
31. <span data-ttu-id="432ad-161">Valitse Sairaalan päivystyspoliklinikka -osassa Kyllä (valinnainen).</span><span class="sxs-lookup"><span data-stu-id="432ad-161">Optionally, set the emergency room hospital visit section to Yes.</span></span>
32. <span data-ttu-id="432ad-162">Kirjoita Hoitokommentit-kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="432ad-162">In the Treatment comments field, type a value.</span></span>
    * <span data-ttu-id="432ad-163">Esimerkki: lasta kahden viikon ajan</span><span class="sxs-lookup"><span data-stu-id="432ad-163">Example:  Splint for 2 weeks</span></span>  
33. <span data-ttu-id="432ad-164">Kirjoita Lääkärin nimi -kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="432ad-164">In the Physician name field, type a value.</span></span>
    * <span data-ttu-id="432ad-165">Esimerkki: tri Anderson</span><span class="sxs-lookup"><span data-stu-id="432ad-165">Example:  Dr. Anderson</span></span>  
34. <span data-ttu-id="432ad-166">Kirjoita Hoitopaikka ja sijainti -kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="432ad-166">In the Treatment facility and location field, type a value.</span></span>
    * <span data-ttu-id="432ad-167">Esimerkki: Elm Streetin päivystävä sairaala</span><span class="sxs-lookup"><span data-stu-id="432ad-167">Example:  Elm St. Emergency</span></span>  
35. <span data-ttu-id="432ad-168">Kirjoita Hoidon lisätiedot -kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="432ad-168">In the Treatment details field, type a value.</span></span>
    * <span data-ttu-id="432ad-169">Esimerkki: röntgenkuva vahvista murtuman, käytettävä lastaa</span><span class="sxs-lookup"><span data-stu-id="432ad-169">Example:  Xray confirms fracture, wear splint</span></span>  
36. <span data-ttu-id="432ad-170">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="432ad-170">Click Save.</span></span>
    * <span data-ttu-id="432ad-171">Tapaustilan voi päivittää milloin tahansa.</span><span class="sxs-lookup"><span data-stu-id="432ad-171">The case status can be updated at any time.</span></span>  <span data-ttu-id="432ad-172">Määritä tapauksen tilaksi keskeneräinen, jos tapaturmaa tai sairautta käsitellään edelleen.</span><span class="sxs-lookup"><span data-stu-id="432ad-172">Set the case to in process, if the processing of the injury or illness is in process.</span></span>  <span data-ttu-id="432ad-173">Kun tapaus on suljettu, siihen voi vain lisätä tapaukseen liittyviä kustannuksia, hoitoja tai ilmoituksia tai poistaa niitä.</span><span class="sxs-lookup"><span data-stu-id="432ad-173">Once you close the incident you can only add or remove costs, treatments or filings related to the incident.</span></span>  <span data-ttu-id="432ad-174">Muiden tietojen muokkaaminen edellyttää tapauksen avaamista uudelleen.</span><span class="sxs-lookup"><span data-stu-id="432ad-174">To modify other information, reopen the case.</span></span>  

