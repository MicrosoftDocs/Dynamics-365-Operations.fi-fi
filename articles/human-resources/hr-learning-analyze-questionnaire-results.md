---
title: Kyselylomakkeen tulosten analysointi
description: Kyselylomakkeen tilastotietoja voidaan käyttää keskiarvojen, kokonaissummien ja prosenttiosuuksien laskemiseen demografiatietojoukon perusteella.
author: andreabichsel
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: KMQuestionnaireStatistics, KMQuestionnaireStatisticsLine, HcmLearningWorkspace
audience: Application User
ms.search.scope: Human Resources
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 135d74d70023fbe1f52b292c09733e77baa14003
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/18/2021
ms.locfileid: "6052910"
---
# <a name="analyzing-questionnaire-results"></a><span data-ttu-id="b8f9e-103">Kyselylomakkeen tulosten analysointi</span><span class="sxs-lookup"><span data-stu-id="b8f9e-103">Analyzing questionnaire results</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]



<span data-ttu-id="b8f9e-104">Kyselylomakkeen tilastotietoja voidaan käyttää keskiarvojen, kokonaissummien ja prosenttiosuuksien laskemiseen demografiatietojoukon perusteella.</span><span class="sxs-lookup"><span data-stu-id="b8f9e-104">Questionnaire statistics can be used to calculate averages, totals, and percentages based on a set of demographic data.</span></span> <span data-ttu-id="b8f9e-105">Aloita tämä menettely siirtymällä kohtaan Kyselylomake > Näytä ja analysoi tulokset > Kyselylomakkeen tilastotiedot.</span><span class="sxs-lookup"><span data-stu-id="b8f9e-105">To begin this procedure, go to Questionnaire > View and analyze results > Questionnaire statistics.</span></span> <span data-ttu-id="b8f9e-106">Tämän menettelyn luomisessa käytetty esittely-yritys on USMF.</span><span class="sxs-lookup"><span data-stu-id="b8f9e-106">The demo data company used to create this procedure is USMF.</span></span>


## <a name="create-a-questionnaire-statistics-record"></a><span data-ttu-id="b8f9e-107">Kyselylomakkeen tilastotietotietueen luominen</span><span class="sxs-lookup"><span data-stu-id="b8f9e-107">Create a Questionnaire statistics record</span></span>
1. <span data-ttu-id="b8f9e-108">Siirry Kyselylomakkeen tilastotiedot -kohtaan.</span><span class="sxs-lookup"><span data-stu-id="b8f9e-108">Go to Questionnaire statistics.</span></span>
2. <span data-ttu-id="b8f9e-109">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="b8f9e-109">Click New.</span></span>
3. <span data-ttu-id="b8f9e-110">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="b8f9e-110">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="b8f9e-111">Syötä arvo Tilastotiedot-kenttään.</span><span class="sxs-lookup"><span data-stu-id="b8f9e-111">In the Statistics field, type a value.</span></span>
5. <span data-ttu-id="b8f9e-112">Kirjoita Kuvaus-kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="b8f9e-112">In the Description field, type a value.</span></span>
6. <span data-ttu-id="b8f9e-113">Avaa haku valitsemalla Kyselylomake-kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="b8f9e-113">In the Questionnaire field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="b8f9e-114">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="b8f9e-114">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="b8f9e-115">Valitse Yleiset-välilehti.</span><span class="sxs-lookup"><span data-stu-id="b8f9e-115">Click the General tab.</span></span>
    * <span data-ttu-id="b8f9e-116">Määritä, haluatko ottaa mukaan nimettömät tulokset vai työntekijöiden, yhteyshenkilöiden ja hakijoiden tulokset.</span><span class="sxs-lookup"><span data-stu-id="b8f9e-116">Select if you want to include anonymous results or results from workers, contacts, and applicants.</span></span>  
9. <span data-ttu-id="b8f9e-117">Valitse Työntekijä-valintaruutu tai poista valintaruudun valinta.</span><span class="sxs-lookup"><span data-stu-id="b8f9e-117">Select or clear the Worker check box.</span></span>
    * <span data-ttu-id="b8f9e-118">Jos tarkastelet tuloksia virkaiän tai iän perusteella, määritä tulosten ryhmittelyssä käytettävät välit.</span><span class="sxs-lookup"><span data-stu-id="b8f9e-118">If you will be viewing the results by seniority or age, specify the intervals that you would like to use for grouping the results.</span></span>  
    * <span data-ttu-id="b8f9e-119">Kun ikäväliksi syötetään 5, tulokset ryhmitellään viiden vuoden ikävälien perusteella.</span><span class="sxs-lookup"><span data-stu-id="b8f9e-119">Entering a 5 for the age interval will group the results based on five-year age intervals.</span></span>  
10. <span data-ttu-id="b8f9e-120">Syötä numero Ikä-kenttään.</span><span class="sxs-lookup"><span data-stu-id="b8f9e-120">In the Age field, enter a number.</span></span>
    * <span data-ttu-id="b8f9e-121">Määritä, haluatko suorittaa laskelman koko kyselylomakkeelle, jokaiselle tulosryhmälle, jokaiselle kysymykselle tai jokaiselle kysymysriville.</span><span class="sxs-lookup"><span data-stu-id="b8f9e-121">Select if you want to run the calculation against the entire questionnaire, for each result group, for each question, or for each question row.</span></span>  
    * <span data-ttu-id="b8f9e-122">Määritä, miten haluat ryhmitellä tulokset.</span><span class="sxs-lookup"><span data-stu-id="b8f9e-122">Select how you would like to group the results.</span></span>  
    * <span data-ttu-id="b8f9e-123">Jos esimerkiksi lasket saatujen pisteiden keskiarvon kysymystä kohti, kysymykset on hyvä nähdä tulosryhmän mukaan ryhmiteltyinä.</span><span class="sxs-lookup"><span data-stu-id="b8f9e-123">For example, if you calculate the average points per question, you may want to see the questions grouped by Result group.</span></span>  
    * <span data-ttu-id="b8f9e-124">Valitse tiedot, joihin laskelma perustuu.</span><span class="sxs-lookup"><span data-stu-id="b8f9e-124">Select the data to base the calculation on.</span></span>  
    * <span data-ttu-id="b8f9e-125">Ajatellaan, että haluat tietää kyselylomakkeen työntekijöiltä saadun keskimääräisen prosentin verrattuna työntekijöiden saamiin keskimääräisiin pisteisiin.</span><span class="sxs-lookup"><span data-stu-id="b8f9e-125">For example, if you want to see the average percent received on the questionnaire across your workers versus the average number of points achieved across your workers.</span></span>  
11. <span data-ttu-id="b8f9e-126">Valitse Alue-välilehti.</span><span class="sxs-lookup"><span data-stu-id="b8f9e-126">Click the Range tab.</span></span>
    * <span data-ttu-id="b8f9e-127">Alueiden avulla voit rajata tulosjoukon sisältämään vain alueen ehtoja vastaavat kohteet.</span><span class="sxs-lookup"><span data-stu-id="b8f9e-127">Use ranges to limit your result set to only those meeting the Range criteria.</span></span>  
12. <span data-ttu-id="b8f9e-128">Valitse Ryhmittely-välilehti.</span><span class="sxs-lookup"><span data-stu-id="b8f9e-128">Click the Grouping by tab.</span></span>
    * <span data-ttu-id="b8f9e-129">Ryhmittelyiden avulla voit määrittää, miten tulokset näytetään.</span><span class="sxs-lookup"><span data-stu-id="b8f9e-129">Use Groupings to determine how the results should be displayed.</span></span>  
    * <span data-ttu-id="b8f9e-130">Voit ryhmitellä tulokset esimerkiksi ensin sukupuolen ja sitten iän perusteella.</span><span class="sxs-lookup"><span data-stu-id="b8f9e-130">For example, group the results first by gender, then by age.</span></span>  
13. <span data-ttu-id="b8f9e-131">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="b8f9e-131">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="b8f9e-132">Siirrä ryhmittelyt Valittu puoli -kohtaan ja aseta ne haluttuun järjestykseen.</span><span class="sxs-lookup"><span data-stu-id="b8f9e-132">Move the groupings into the Selected side and place them in the desired order.</span></span>  

## <a name="execute-the-statistics-calculation"></a><span data-ttu-id="b8f9e-133">Tilastotietojen laskelman suorittaminen</span><span class="sxs-lookup"><span data-stu-id="b8f9e-133">Execute the statistics calculation</span></span>
1. <span data-ttu-id="b8f9e-134">Valitse Suorita.</span><span class="sxs-lookup"><span data-stu-id="b8f9e-134">Click Execute.</span></span>
    * <span data-ttu-id="b8f9e-135">Määritä, mitä laskentatoimintoa tulosten käsittelyssä käytetään.</span><span class="sxs-lookup"><span data-stu-id="b8f9e-135">Select which calculation function you would like to perform on the results.</span></span>  
    * <span data-ttu-id="b8f9e-136">Voit laskea esimerkiksi valittujen ryhmien kyselylomakkeen keskimääräiset prosenttiosuudet tai tulosryhmien pisteiden kokonaistuloksen.</span><span class="sxs-lookup"><span data-stu-id="b8f9e-136">For example, calculate the average percentages across the questionnaire for the selected groupings or total the points across the result groups for the selected groupings.</span></span>  
2. <span data-ttu-id="b8f9e-137">Valitse Poista edelliset haut -valintaruutu tai poista sen valinta.</span><span class="sxs-lookup"><span data-stu-id="b8f9e-137">Select or clear the Delete previous searches check box.</span></span>
3. <span data-ttu-id="b8f9e-138">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="b8f9e-138">Click OK.</span></span>

## <a name="view-the-results-of-the-questionnaire-statistics-run"></a><span data-ttu-id="b8f9e-139">Tarkastele kyselylomakkeen tilastotietojen saatuja tuloksia.</span><span class="sxs-lookup"><span data-stu-id="b8f9e-139">View the results of the questionnaire statistics run.</span></span>
1. <span data-ttu-id="b8f9e-140">Valitse Tulos.</span><span class="sxs-lookup"><span data-stu-id="b8f9e-140">Click Result.</span></span>
2. <span data-ttu-id="b8f9e-141">Valitse Tulos.</span><span class="sxs-lookup"><span data-stu-id="b8f9e-141">Click Result.</span></span>
3. <span data-ttu-id="b8f9e-142">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="b8f9e-142">Close the page.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]