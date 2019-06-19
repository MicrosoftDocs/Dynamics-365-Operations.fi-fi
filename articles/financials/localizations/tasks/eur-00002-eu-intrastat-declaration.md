---
title: EUR-00002 EU Intrastat -ilmoituksen luominen
description: Tässä menettelyssä käydään läpi vaiheet, joissa viedään Intrastat-ilmoituksen sähköisessä tiedostomuodossa ja esikatsellaan ilmoitustiedot Excel-muodossa.
author: Anasyash
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionRepositoryTable, ERSolutionImport, IntrastatParameters, IntrastatCommodityLookup, IntrastatCompressParameters, Intrastat, SysQueryForm
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Austria, Belgium, Czech Republic, Denmark, Estonia, Finland, France, Germany, Hungary, Ireland, Italy, Latvia, Lithuania, Netherlands, Poland, Spain, Sweden, United Kingdom
ms.author: anasyash
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1236f27a3a5c208ffec41374a6593d1f0e7c4433
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/15/2019
ms.locfileid: "1566787"
---
# <a name="eur-00002-generate-an-eu-intrastat-declaration"></a><span data-ttu-id="cac43-103">EUR-00002 EU Intrastat -ilmoituksen luominen</span><span class="sxs-lookup"><span data-stu-id="cac43-103">EUR-00002 Generate an EU Intrastat declaration</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="cac43-104">Tässä menettelyssä käydään läpi vaiheet, joissa viedään Intrastat-ilmoituksen sähköisessä tiedostomuodossa ja esikatsellaan ilmoitustiedot Excel-muodossa.</span><span class="sxs-lookup"><span data-stu-id="cac43-104">This procedure walks you through the steps required to export the Intrastat declaration in the electronic file format and preview the declaration data in an Excel format.</span></span> 

<span data-ttu-id="cac43-105">Ennen kuin suoritat tämän menettelyn, tapahtumat on siirrettävä Intrastatiin.</span><span class="sxs-lookup"><span data-stu-id="cac43-105">Before you can complete this procedure, you must transfer transactions to the Intrastat.</span></span> 

<span data-ttu-id="cac43-106">Tämä menettelyn luomisessa käytettiin DEMF-yrityksen demotietoja.</span><span class="sxs-lookup"><span data-stu-id="cac43-106">This procedure was created using the demo data company DEMF.</span></span>


## <a name="import-configurations-with-settings"></a><span data-ttu-id="cac43-107">Asetuksia sisältävien konfiguraatioiden tuonti</span><span class="sxs-lookup"><span data-stu-id="cac43-107">Import configurations with settings</span></span>
1. <span data-ttu-id="cac43-108">Valitse Työtilat > Sähköinen raportointi</span><span class="sxs-lookup"><span data-stu-id="cac43-108">Go to Workspaces > Electronic reporting</span></span>
2. <span data-ttu-id="cac43-109">Valitse Aseta aktiiviseksi.</span><span class="sxs-lookup"><span data-stu-id="cac43-109">Click Set active.</span></span>
3. <span data-ttu-id="cac43-110">Valitse Säilöt.</span><span class="sxs-lookup"><span data-stu-id="cac43-110">Click Repositories.</span></span>
4. <span data-ttu-id="cac43-111">Valitse Avaa.</span><span class="sxs-lookup"><span data-stu-id="cac43-111">Click Open.</span></span>
5. <span data-ttu-id="cac43-112">Avaa Konfiguraation nimi -sarakkeen suodatin.</span><span class="sxs-lookup"><span data-stu-id="cac43-112">Open Configuration name column filter.</span></span>
6. <span data-ttu-id="cac43-113">Käytä suodatinta Konfiguraation nimi -kentässä niin, että arvo on "Intrastat (DE)" ja suodatinoperaattori Alkaa.</span><span class="sxs-lookup"><span data-stu-id="cac43-113">Apply a filter on the "Configuration name" field, with a value of "Intrastat (DE)", using the "begins with" filter operator.</span></span>
    * <span data-ttu-id="cac43-114">Valitse yrityksesi toimintamaata vastaava konfiguraation nimi.</span><span class="sxs-lookup"><span data-stu-id="cac43-114">You should select the configuration name applicable for the country of your legal entity.</span></span> <span data-ttu-id="cac43-115">Näissä toimintaohjeissa käytetään esimerkkinä saksalaista yritystä (DEMF); tämän vuoksi tulee valita "Intrastat (DE)".</span><span class="sxs-lookup"><span data-stu-id="cac43-115">This procedure uses the German legal entity (DEMF) as an example, therefore "Intrastat (DE)" should be chosen.</span></span>  
    * <span data-ttu-id="cac43-116">Valitse Tuo ja valitse sitten Kyllä.</span><span class="sxs-lookup"><span data-stu-id="cac43-116">Click Import and then click Yes.</span></span>  
7. <span data-ttu-id="cac43-117">Avaa Konfiguraation nimi -sarakkeen suodatin.</span><span class="sxs-lookup"><span data-stu-id="cac43-117">Open Configuration name column filter.</span></span>
8. <span data-ttu-id="cac43-118">Käytä suodatinta Konfiguraation nimi -kentässä niin, että arvo on "Intrastat-raportti" ja suodatinoperaattori Alkaa.</span><span class="sxs-lookup"><span data-stu-id="cac43-118">Apply a filter on the "Configuration name" field, with a value of "intrastat report", using the "begins with" filter operator.</span></span>
    * <span data-ttu-id="cac43-119">Valitse Tuo ja valitse sitten Kyllä.</span><span class="sxs-lookup"><span data-stu-id="cac43-119">Click Import and then click Yes.</span></span>  

## <a name="set-up-foreign-trade-parameters"></a><span data-ttu-id="cac43-120">Määritä ulkomaankaupan parametrit</span><span class="sxs-lookup"><span data-stu-id="cac43-120">Set up Foreign trade parameters</span></span>
1. <span data-ttu-id="cac43-121">Valitse Vero > Asetukset > Ulkomaankauppa > Ulkomaankaupan parametrit</span><span class="sxs-lookup"><span data-stu-id="cac43-121">Go to Tax > Setup > Foreign trade > Foreign trade parameters</span></span>
2. <span data-ttu-id="cac43-122">Laajenna Sähköinen raportointi -osa.</span><span class="sxs-lookup"><span data-stu-id="cac43-122">Expand the Electronic reporting section.</span></span>
3. <span data-ttu-id="cac43-123">Anna tai valitse Tiedostomuodon yhdistäminen -kentässä arvoksi Intrastat (DE).</span><span class="sxs-lookup"><span data-stu-id="cac43-123">In the File format mapping field, enter or select a value Intrastat (DE)</span></span>
4. <span data-ttu-id="cac43-124">Anna tai valitse Raporttimuodon yhdistäminen -kentässä arvoksi Intrastat-raportti.</span><span class="sxs-lookup"><span data-stu-id="cac43-124">In the Report format mapping field, enter or select a value Intrastat report</span></span>
5. <span data-ttu-id="cac43-125">Laajenna Pyöristyssäännöt-osa.</span><span class="sxs-lookup"><span data-stu-id="cac43-125">Expand the Rounding rules section.</span></span>
    * <span data-ttu-id="cac43-126">Pyöristyssäännöt tulee määrittää maasi/alueesi Intrastat-raportoinnin käytäntöjen mukaisiksi.</span><span class="sxs-lookup"><span data-stu-id="cac43-126">You should set up rounding rules that are applicable in your country/region for Intrastat reporting.</span></span>  
6. <span data-ttu-id="cac43-127">Syötä Pyöristyssääntö-kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="cac43-127">In the Rounding rule field, enter a number.</span></span>
    * <span data-ttu-id="cac43-128">Anna pyöristystarkkuus, esimerkiksi 0,01.</span><span class="sxs-lookup"><span data-stu-id="cac43-128">Enter rounding precision, for example, enter '0.01'.</span></span>  
7. <span data-ttu-id="cac43-129">Syötä Summan desimaalien määrä -kenttään haluamasi luku.</span><span class="sxs-lookup"><span data-stu-id="cac43-129">In the Number of decimals for amount field, enter a number.</span></span>
    * <span data-ttu-id="cac43-130">Kirjoita esimerkiksi 2.</span><span class="sxs-lookup"><span data-stu-id="cac43-130">For example, enter '2'.</span></span>  
8. <span data-ttu-id="cac43-131">Valitse vaihtoehto Pyöristys, alle 1 kg -kentässä.</span><span class="sxs-lookup"><span data-stu-id="cac43-131">In the Rounding below 1 kg field, select an option.</span></span>
    * <span data-ttu-id="cac43-132">Valitse esimerkiksi "Pyöristys, enintään 1 kg".</span><span class="sxs-lookup"><span data-stu-id="cac43-132">For example, select 'Rounding up to 1 kg'.</span></span>  
9. <span data-ttu-id="cac43-133">Syötä Pyöristyssääntö-kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="cac43-133">In the Rounding rule field, enter a number.</span></span>
    * <span data-ttu-id="cac43-134">Kirjoita esimerkiksi 1 kokonaisluvun pyöristyksen painotukseksi.</span><span class="sxs-lookup"><span data-stu-id="cac43-134">For example, enter '1' for rounding weight to the integer.</span></span>  
10. <span data-ttu-id="cac43-135">Laajenna Vähimmäisraja-osa.</span><span class="sxs-lookup"><span data-stu-id="cac43-135">Expand the Minimum limit section.</span></span>
11. <span data-ttu-id="cac43-136">Syötä numero Paino-kenttään.</span><span class="sxs-lookup"><span data-stu-id="cac43-136">In the Weight field, enter a number.</span></span>
    * <span data-ttu-id="cac43-137">Määritä vähimmäispainoksi esimerkiksi "10".</span><span class="sxs-lookup"><span data-stu-id="cac43-137">For example, enter '10' as the minimum weight.</span></span>  
12. <span data-ttu-id="cac43-138">Lisää Summa-kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="cac43-138">In the Amount field, enter a number.</span></span>
    * <span data-ttu-id="cac43-139">Määritä vähimmäismääräksi esimerkiksi "200".</span><span class="sxs-lookup"><span data-stu-id="cac43-139">For example, enter '200' as the minimum amount.</span></span>  
13. <span data-ttu-id="cac43-140">Syötä tai valitse arvo Kauppatavara-kentässä.</span><span class="sxs-lookup"><span data-stu-id="cac43-140">In the Commodity field, enter or select a value.</span></span>

## <a name="set-up-compression-of-intrastat"></a><span data-ttu-id="cac43-141">Määritä Intrastatin tiivistysasetukset</span><span class="sxs-lookup"><span data-stu-id="cac43-141">Set up Compression of Intrastat</span></span>
1. <span data-ttu-id="cac43-142">Valitse Vero > Asetukset > Ulkomaankauppa > Intrastatin tiivistys.</span><span class="sxs-lookup"><span data-stu-id="cac43-142">Go to Tax > Setup > Foreign trade > Compression of Intrastat.</span></span>
2. <span data-ttu-id="cac43-143">Valitse Poista.</span><span class="sxs-lookup"><span data-stu-id="cac43-143">Click Remove.</span></span>
3. <span data-ttu-id="cac43-144">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="cac43-144">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="cac43-145">Valitse esimerkiksi Kauppatavara Käytettävissä-osasta.</span><span class="sxs-lookup"><span data-stu-id="cac43-145">For example, select Commodity in the Available section.</span></span>  
4. <span data-ttu-id="cac43-146">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="cac43-146">Click Add.</span></span>

## <a name="generate-intrastat-declaration"></a><span data-ttu-id="cac43-147">Intrastat-ilmoituksen luominen</span><span class="sxs-lookup"><span data-stu-id="cac43-147">Generate Intrastat declaration</span></span>
1. <span data-ttu-id="cac43-148">Valitse Vero > Ilmoitukset > Ulkomaankauppa > Intrastat</span><span class="sxs-lookup"><span data-stu-id="cac43-148">Go to Tax > Declarations > Foreign trade > Intrastat</span></span>
2. <span data-ttu-id="cac43-149">Valitse Vahvista.</span><span class="sxs-lookup"><span data-stu-id="cac43-149">Click Validate.</span></span>
    * <span data-ttu-id="cac43-150">Oikeellisuustarkistus suoritetaan Ulkomaankaupan parametrit -sivun Tarkista asetukset -kentän mukaisesti.</span><span class="sxs-lookup"><span data-stu-id="cac43-150">The validation is done according to the Check setup field on the Foreign trade parameters page.</span></span>  
3. <span data-ttu-id="cac43-151">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="cac43-151">Click OK.</span></span>
4. <span data-ttu-id="cac43-152">Valitse Päivitä.</span><span class="sxs-lookup"><span data-stu-id="cac43-152">Click Update.</span></span>
5. <span data-ttu-id="cac43-153">Valitse Vähimmäisraja.</span><span class="sxs-lookup"><span data-stu-id="cac43-153">Click Minimum limit.</span></span>
6. <span data-ttu-id="cac43-154">Syötä päivämäärä Aloituspäivä-kenttään.</span><span class="sxs-lookup"><span data-stu-id="cac43-154">In the Start date field, enter a date.</span></span>
    * <span data-ttu-id="cac43-155">Syötä kenttään esimerkiksi 1. tammikuuta 2015.</span><span class="sxs-lookup"><span data-stu-id="cac43-155">For example, enter January 1, 2015.</span></span>  
7. <span data-ttu-id="cac43-156">Valitse Tiivistä-kentässä Kyllä.</span><span class="sxs-lookup"><span data-stu-id="cac43-156">Select Yes in the Compress field.</span></span>
8. <span data-ttu-id="cac43-157">Syötä päivämäärä Päättymispäivä-kenttään.</span><span class="sxs-lookup"><span data-stu-id="cac43-157">In the End date field, enter a date.</span></span>
    * <span data-ttu-id="cac43-158">Syötä kenttään esimerkiksi 31. tammikuuta 2015.</span><span class="sxs-lookup"><span data-stu-id="cac43-158">For example, enter January 31, 2015.</span></span>  
9. <span data-ttu-id="cac43-159">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="cac43-159">Click OK.</span></span>
10. <span data-ttu-id="cac43-160">Valitse Päivitä.</span><span class="sxs-lookup"><span data-stu-id="cac43-160">Click Update.</span></span>
11. <span data-ttu-id="cac43-161">Valitse Tiivistä.</span><span class="sxs-lookup"><span data-stu-id="cac43-161">Click Compress.</span></span>
    * <span data-ttu-id="cac43-162">Tämä pakkaus tapahtuu sen mukaan, miten Intrastatin pakkausasetukset on määritetty.</span><span class="sxs-lookup"><span data-stu-id="cac43-162">This compression happens according to how you set the Compression of intrastate settings.</span></span>  
12. <span data-ttu-id="cac43-163">Syötä päivämäärä Aloituspäivä-kenttään.</span><span class="sxs-lookup"><span data-stu-id="cac43-163">In the Start date field, enter a date.</span></span>
    * <span data-ttu-id="cac43-164">Syötä kenttään esimerkiksi 1. tammikuuta 2015.</span><span class="sxs-lookup"><span data-stu-id="cac43-164">For example, enter January 1, 2015.</span></span>  
13. <span data-ttu-id="cac43-165">Syötä päivämäärä Päättymispäivä-kenttään.</span><span class="sxs-lookup"><span data-stu-id="cac43-165">In the End date field, enter a date.</span></span>
    * <span data-ttu-id="cac43-166">Syötä kenttään esimerkiksi 31. tammikuuta 2015.</span><span class="sxs-lookup"><span data-stu-id="cac43-166">For example, enter 31st January 2015.</span></span>  
14. <span data-ttu-id="cac43-167">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="cac43-167">Click OK.</span></span>
15. <span data-ttu-id="cac43-168">Valitse Päivitä.</span><span class="sxs-lookup"><span data-stu-id="cac43-168">Click Update.</span></span>
16. <span data-ttu-id="cac43-169">Valitse Muodosta uudestaan järjestysnumerot.</span><span class="sxs-lookup"><span data-stu-id="cac43-169">Click Regenerate sequence numbers.</span></span>
17. <span data-ttu-id="cac43-170">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="cac43-170">Click OK.</span></span>
18. <span data-ttu-id="cac43-171">Valitse Tulostus.</span><span class="sxs-lookup"><span data-stu-id="cac43-171">Click Output.</span></span>
19. <span data-ttu-id="cac43-172">Valitse Raportti.</span><span class="sxs-lookup"><span data-stu-id="cac43-172">Click Report.</span></span>
20. <span data-ttu-id="cac43-173">Kirjoita Aloituspäivämäärä-kenttään raportointikauden ensimmäinen päivä.</span><span class="sxs-lookup"><span data-stu-id="cac43-173">In the From date field, enter the first date of the reporting period.</span></span>
    * <span data-ttu-id="cac43-174">Aseta päivämääräksi esim. 1. tammikuuta 2015.</span><span class="sxs-lookup"><span data-stu-id="cac43-174">For example, set the date to January 1, 2015.</span></span>  
21. <span data-ttu-id="cac43-175">Kirjoita päivämäärä Päivämäärään-kenttään.</span><span class="sxs-lookup"><span data-stu-id="cac43-175">In the To date field, enter a date.</span></span>
    * <span data-ttu-id="cac43-176">Syötä kenttään esimerkiksi 31. tammikuuta 2015.</span><span class="sxs-lookup"><span data-stu-id="cac43-176">For example, enter January 31, 2015.</span></span>  
22. <span data-ttu-id="cac43-177">Valitse Luo tiedosto -kentässä Kyllä.</span><span class="sxs-lookup"><span data-stu-id="cac43-177">Select Yes in the Generate file field.</span></span>
23. <span data-ttu-id="cac43-178">Kirjoita arvo Tiedostonimi-kenttään.</span><span class="sxs-lookup"><span data-stu-id="cac43-178">In the File name field, type a value.</span></span>
24. <span data-ttu-id="cac43-179">Valitse Luo raportti -kentässä Kyllä.</span><span class="sxs-lookup"><span data-stu-id="cac43-179">Select Yes in the Generate report field.</span></span>
25. <span data-ttu-id="cac43-180">Kirjoita arvo Raportin nimi -kenttään.</span><span class="sxs-lookup"><span data-stu-id="cac43-180">In the Report file name field, type a value.</span></span>
26. <span data-ttu-id="cac43-181">Valitse vaihtoehto kentässä Suunta.</span><span class="sxs-lookup"><span data-stu-id="cac43-181">In the Direction field, select an option.</span></span>
    * <span data-ttu-id="cac43-182">Valitse esimerkiksi Lähtevät.</span><span class="sxs-lookup"><span data-stu-id="cac43-182">For example, select 'Dispatches'.</span></span>  
27. <span data-ttu-id="cac43-183">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="cac43-183">Click OK.</span></span>

