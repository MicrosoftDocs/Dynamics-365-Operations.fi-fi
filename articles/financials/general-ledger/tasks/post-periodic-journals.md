--- 
title: Kirjaa kausittaiset kirjauskansiot
description: "Kausikirjauskansioita kutsutaan joskus toistuviksi kirjauskansioiksi, koska summa, teksti ja muut tiedot toistetaan aina kausikirjauskansion haun yhteydessä."
author: aprilolson
manager: AnnBe
ms.date: 8/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: LedgerJournalTable, LedgerJournalTransPeriodic, LedgerJournalTransDaily
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 32d71167fdad65cb1dec37671999a497759ca484
ms.openlocfilehash: c84e9297b2a672600e71fcb614d80d9729a000d6
ms.contentlocale: fi-fi
ms.lasthandoff: 09/11/2018

---
# <a name="post-periodic-journals"></a><span data-ttu-id="681e2-103">Kirjaa kausittaiset kirjauskansiot</span><span class="sxs-lookup"><span data-stu-id="681e2-103">Post periodic journals</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="681e2-104">Kausikirjauskansioita kutsutaan joskus toistuviksi kirjauskansioiksi, koska summa, teksti ja muut tiedot toistetaan aina kausikirjauskansion haun yhteydessä.</span><span class="sxs-lookup"><span data-stu-id="681e2-104">Periodic journals are sometimes called recurring journals because the amount, text, and other information are repeated each time that the periodic journal is retrieved.</span></span> <span data-ttu-id="681e2-105">Kausikirjauskansion luomisen yhteydessä määritetään toistumisen kausiväli, kuten päivät tai kuukaudet.</span><span class="sxs-lookup"><span data-stu-id="681e2-105">When you create the periodic journal, you specify the period interval for the recurrence, such as days or months.</span></span> <span data-ttu-id="681e2-106">Tässä tehtävän ohjauksessa luodaan kausikirjauskansio, jonka toiston kausiväli on kuukausi.</span><span class="sxs-lookup"><span data-stu-id="681e2-106">This task guide will create a periodic journal with a monthly recurrence.</span></span>



1. <span data-ttu-id="681e2-107">Siirry kohtaan Kirjanpito > Kausittaiset tehtävät > Kausikirjauskansiot.</span><span class="sxs-lookup"><span data-stu-id="681e2-107">Go to General ledger > Periodic tasks > Periodic journals.</span></span>
2. <span data-ttu-id="681e2-108">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="681e2-108">Click New.</span></span>
3. <span data-ttu-id="681e2-109">Syötä tai valitse arvo Nimi-kenttään.</span><span class="sxs-lookup"><span data-stu-id="681e2-109">In the Name field, enter or select a value.</span></span>
4. <span data-ttu-id="681e2-110">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="681e2-110">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="681e2-111">Kirjoita arvo Kuvaus-kenttään.</span><span class="sxs-lookup"><span data-stu-id="681e2-111">In the Description field, type a value.</span></span>
    * <span data-ttu-id="681e2-112">Kuvaus on myöhemmin haettavan kausikirjauskansion nimi, joten varmista, että annat sopivan nimen.</span><span class="sxs-lookup"><span data-stu-id="681e2-112">The description will be the name of the Periodic journal when retrieved later so make sure to give it a relevant name.</span></span>  
6. <span data-ttu-id="681e2-113">Valitse Rivit.</span><span class="sxs-lookup"><span data-stu-id="681e2-113">Click Lines.</span></span>
    * <span data-ttu-id="681e2-114">Kausikirjauskansio sisältää yleensä useita kirjauskansion rivejä.</span><span class="sxs-lookup"><span data-stu-id="681e2-114">A periodic journal will typically include several journal lines.</span></span> <span data-ttu-id="681e2-115">tässä tehtävän ohjauksessa lisätään kuitenkin vain yksi rivi.</span><span class="sxs-lookup"><span data-stu-id="681e2-115">this task guide will however only add one line.</span></span>  
7. <span data-ttu-id="681e2-116">Syötä Päivämäärään-kenttään päivämäärä.</span><span class="sxs-lookup"><span data-stu-id="681e2-116">In the Date field, enter a date.</span></span>
    * <span data-ttu-id="681e2-117">Päivämäärä-kenttä sisältää seuraavan kirjauskansioon siirron kirjauspäivämäärän.</span><span class="sxs-lookup"><span data-stu-id="681e2-117">The Date field contains the posting date for the next transfer to the daily journal.</span></span> <span data-ttu-id="681e2-118">Jos kirjauskansio haetaan joka kuukausi, kannattaa käyttää kirjauskuukauden päivämäärää. Yleensä se on kauden ensimmäinen tai viimeinen päivä.</span><span class="sxs-lookup"><span data-stu-id="681e2-118">For journals that will be retrieved each month it is recommended to use the date in the month when it will be posted, typically the first or last date in the period.</span></span> <span data-ttu-id="681e2-119">Päivämäärä-kentän voi jättää tyhjäksi, jolloin päivämäärä annetaan kirjauskansion haun yhteydessä Tyhjä päivämäärä -kentän avulla.</span><span class="sxs-lookup"><span data-stu-id="681e2-119">It is possible to leave the Date field blank and to give a date when the journal is retrieved, using the Empty date field.</span></span>    <span data-ttu-id="681e2-120">Kentän arvoksi päivitetään automaattisesti seuraava toistuva päivämäärä, kun tapahtumat haetaan.</span><span class="sxs-lookup"><span data-stu-id="681e2-120">The field is automatically updated to the next recurring date when transactions are retrieved.</span></span>  
8. <span data-ttu-id="681e2-121">Määritä Tili-kenttään haluamasi arvot.</span><span class="sxs-lookup"><span data-stu-id="681e2-121">In the Account field, specify the desired values.</span></span>
9. <span data-ttu-id="681e2-122">Kirjoita arvo Kuvaus-kenttään.</span><span class="sxs-lookup"><span data-stu-id="681e2-122">In the Description field, type a value.</span></span>
10. <span data-ttu-id="681e2-123">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="681e2-123">Close the page.</span></span>
11. <span data-ttu-id="681e2-124">Syötä Debet-kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="681e2-124">In the Debit field, enter a number.</span></span>
12. <span data-ttu-id="681e2-125">Määritä Vastatili-kenttään haluamasi arvot.</span><span class="sxs-lookup"><span data-stu-id="681e2-125">In the Offset account field, specify the desired values.</span></span>
13. <span data-ttu-id="681e2-126">Valitse Yksikkö-kentässä Kuukaudet.</span><span class="sxs-lookup"><span data-stu-id="681e2-126">In the Unit field, select 'Months'.</span></span>
14. <span data-ttu-id="681e2-127">Syötä Yksiköiden määrä -kenttään 1.</span><span class="sxs-lookup"><span data-stu-id="681e2-127">In the Number of units field, enter '1'.</span></span>
15. <span data-ttu-id="681e2-128">Syötä päivämäärä Viimeinen päivämäärä -kenttään.</span><span class="sxs-lookup"><span data-stu-id="681e2-128">In the Last date field, enter a date.</span></span>
    * <span data-ttu-id="681e2-129">Edellisen kauden viimeisen päivämäärän syöttäminen estää toistuvan kirjauskansion luomisen vahingossa väärälle aloituskaudelle.</span><span class="sxs-lookup"><span data-stu-id="681e2-129">Entering last date in the preceding period will prevent that the recurring journal by mistake is created in the wrong starting period.</span></span> <span data-ttu-id="681e2-130">Viimeinen päivämäärä päivitetään myöhemmin aina, kun kausikirjauskansio haetaan.</span><span class="sxs-lookup"><span data-stu-id="681e2-130">Last date will later on be updated each time the periodic journal is retrieved.</span></span>  
16. <span data-ttu-id="681e2-131">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="681e2-131">Click Save.</span></span>
17. <span data-ttu-id="681e2-132">Siirry oletuskoontinäyttöön.</span><span class="sxs-lookup"><span data-stu-id="681e2-132">Go to Default dashboard.</span></span>
18. <span data-ttu-id="681e2-133">Siirry kohtaan Kirjanpito > Kirjauskansioviennit > Yleiset kirjauskansiot.</span><span class="sxs-lookup"><span data-stu-id="681e2-133">Go to General ledger > Journal entries > General journals.</span></span>
19. <span data-ttu-id="681e2-134">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="681e2-134">Click New.</span></span>
20. <span data-ttu-id="681e2-135">Syötä tai valitse arvo Nimi-kenttään.</span><span class="sxs-lookup"><span data-stu-id="681e2-135">In the Name field, enter or select a value.</span></span>
21. <span data-ttu-id="681e2-136">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="681e2-136">In the list, find and select the desired record.</span></span>
22. <span data-ttu-id="681e2-137">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="681e2-137">In the list, click the link in the selected row.</span></span>
23. <span data-ttu-id="681e2-138">Kirjoita arvo Kuvaus-kenttään.</span><span class="sxs-lookup"><span data-stu-id="681e2-138">In the Description field, type a value.</span></span>
24. <span data-ttu-id="681e2-139">Valitse Rivit.</span><span class="sxs-lookup"><span data-stu-id="681e2-139">Click Lines.</span></span>
25. <span data-ttu-id="681e2-140">Valitse kausikirjauskansio.</span><span class="sxs-lookup"><span data-stu-id="681e2-140">Click Period journal.</span></span>
26. <span data-ttu-id="681e2-141">Valitse Nouda kirjauskansio.</span><span class="sxs-lookup"><span data-stu-id="681e2-141">Click Retrieve journal.</span></span>
27. <span data-ttu-id="681e2-142">Kirjoita päivämäärä Päivämäärään-kenttään.</span><span class="sxs-lookup"><span data-stu-id="681e2-142">In the To date field, enter a date.</span></span>
    * <span data-ttu-id="681e2-143">Loppupäivämäärä toimii kausittaisen tositteen rivien katkaisupäivämääränä.</span><span class="sxs-lookup"><span data-stu-id="681e2-143">The To date serves as the cutoff date for the periodic voucher lines.</span></span> <span data-ttu-id="681e2-144">Toistoasetuksen perusteella viimeinen päivämäärä- ja loppupäivämäärä voidaan sisällyttää usean kerran samalle riville tuloksena olevassa kirjauskansiossa.</span><span class="sxs-lookup"><span data-stu-id="681e2-144">Based on the recurrence setting, the Last date and To date the same line might be included more than once in the resulting journal.</span></span> <span data-ttu-id="681e2-145">Loppupäivämääräksi päivitetään automaattisesti sen istunnon päivämäärä, jonka aikana kausittainen rivi siirrettiin kirjauskansioon.</span><span class="sxs-lookup"><span data-stu-id="681e2-145">To date is automatically updated based on  session date of the last time the periodic line was transferred to a journal.</span></span>  
28. <span data-ttu-id="681e2-146">Syötä tai valitse arvo Kausikirjauskansio-kenttään.</span><span class="sxs-lookup"><span data-stu-id="681e2-146">In the Periodic journal number field, enter or select a value.</span></span>
29. <span data-ttu-id="681e2-147">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="681e2-147">In the list, click the link in the selected row.</span></span>
30. <span data-ttu-id="681e2-148">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="681e2-148">Click OK.</span></span>
    * <span data-ttu-id="681e2-149">Kausikirjauskansio voidaan nyt tarkistaa, hyväksyä tai kirjata tarpeiden ja asetusten perusteella.</span><span class="sxs-lookup"><span data-stu-id="681e2-149">The period journal can now be reviewed, approved or posted depending on requirement and setup.</span></span>  


