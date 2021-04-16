---
title: Anna hakijan ja hakemuksen tiedot manuaalisesti
description: Tässä menettelyssä kerrotaan, miten hakijoiden ja hakemusten tietoja ylläpidetään manuaalisesti.
author: andreabichsel
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: HcmApplicant, LogisticsContactInfoGrid, HRMApplication,  DirPartyTable
audience: Application User
ms.reviewer: anbichse
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 08104729f5be15ef7e727102e7be731bdda1a38c
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2021
ms.locfileid: "5751979"
---
# <a name="enter-applicant-and-application-data-manually"></a><span data-ttu-id="ca4dd-103">Anna hakijan ja hakemuksen tiedot manuaalisesti</span><span class="sxs-lookup"><span data-stu-id="ca4dd-103">Enter applicant and application data manually</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="ca4dd-104">Tässä menettelyssä kerrotaan, miten hakijoiden ja hakemusten tietoja ylläpidetään manuaalisesti.</span><span class="sxs-lookup"><span data-stu-id="ca4dd-104">This procedure shows how to manually maintain information about applicants and their application.</span></span>   <span data-ttu-id="ca4dd-105">Voit syöttää ja ylläpitää hakijoiden henkilökohtaisia tietoja, haastattelupäivämääriä ja -aikoja, suosituksia, osaamisalueita ja apuvälinepyyntöjä.</span><span class="sxs-lookup"><span data-stu-id="ca4dd-105">You can enter and maintain personal information, interview dates and times, references, competencies, and accommodation requests for applicants.</span></span> <span data-ttu-id="ca4dd-106">Voit myös päivittää hakijoiden työhakemusten tilaa ja luoda hakijoille kansilehtiä tai sähköpostiviestejä.</span><span class="sxs-lookup"><span data-stu-id="ca4dd-106">You can also update the status of applicants' applications for employment and create letters or email messages to communicate with applicants.</span></span> <span data-ttu-id="ca4dd-107">Kun hakijatietue on luotu, hakijalle luodaan henkilötietue yleiseen osoitekirjaan.</span><span class="sxs-lookup"><span data-stu-id="ca4dd-107">When you create an applicant record, a person record for that applicant is created in the global address book.</span></span>       <span data-ttu-id="ca4dd-108">Tämän menettelyn luomisessa käytetty esittely-yritys on USMF.</span><span class="sxs-lookup"><span data-stu-id="ca4dd-108">The demo data company used to create this procedure is USMF.</span></span>


## <a name="create-a-new-applicant-record"></a><span data-ttu-id="ca4dd-109">Uuden hakijatietueen luominen</span><span class="sxs-lookup"><span data-stu-id="ca4dd-109">Create a new applicant record</span></span>
1. <span data-ttu-id="ca4dd-110">Siirry kohtaan Henkilöstöhallinto > Työhönotto > Hakijat > Hakijat.</span><span class="sxs-lookup"><span data-stu-id="ca4dd-110">Go to Human resources > Recruitment > Applicants > Applicants.</span></span>
2. <span data-ttu-id="ca4dd-111">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="ca4dd-111">Click New.</span></span>
3. <span data-ttu-id="ca4dd-112">Kirjoita arvo Etunimi-kenttään.</span><span class="sxs-lookup"><span data-stu-id="ca4dd-112">In the First name field, type a value.</span></span>
4. <span data-ttu-id="ca4dd-113">Kirjoita arvo Sukunimi-kenttään.</span><span class="sxs-lookup"><span data-stu-id="ca4dd-113">In the Last name field, type a value.</span></span>
    * <span data-ttu-id="ca4dd-114">Voit syöttää hakijalle tarvittaessa lisätietoja.</span><span class="sxs-lookup"><span data-stu-id="ca4dd-114">You can enter additional applicant information if it's available.</span></span> <span data-ttu-id="ca4dd-115">Lisätietoja voivat olla esimerkiksi hakijan korkein tutkinto, nykyinen ammattinimike tai edellinen työnantaja.</span><span class="sxs-lookup"><span data-stu-id="ca4dd-115">For example, information can include the applicant's highest degree, current job title, or previous employer.</span></span>  
5. <span data-ttu-id="ca4dd-116">Ota käyttöön Yhteystiedot-osan laajennus.</span><span class="sxs-lookup"><span data-stu-id="ca4dd-116">Toggle the expansion of the Contact information section.</span></span>
6. <span data-ttu-id="ca4dd-117">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="ca4dd-117">Click Add.</span></span>
7. <span data-ttu-id="ca4dd-118">Syötä Kuvaus-kenttään Viestintä - sähköposti.</span><span class="sxs-lookup"><span data-stu-id="ca4dd-118">In the Description field, type 'Communications email'.</span></span>
8. <span data-ttu-id="ca4dd-119">Valitse vaihtoehto Tyyppi-kentässä.</span><span class="sxs-lookup"><span data-stu-id="ca4dd-119">In the Type field, select an option.</span></span>
9. <span data-ttu-id="ca4dd-120">Kirjoita arvo Yhteyshenkilön puhelinnumero/osoite -kenttään.</span><span class="sxs-lookup"><span data-stu-id="ca4dd-120">In the Contact number/address field, type a value.</span></span>
    * <span data-ttu-id="ca4dd-121">Tätä sähköpostiosoitetta käytetään luotaessa sähköpostiviestintä hakijan kanssa.</span><span class="sxs-lookup"><span data-stu-id="ca4dd-121">This email address will be used to generate email communication with the applicant.</span></span>  
10. <span data-ttu-id="ca4dd-122">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="ca4dd-122">Click Add.</span></span>
11. <span data-ttu-id="ca4dd-123">Kirjoita arvo Kuvaus-kenttään.</span><span class="sxs-lookup"><span data-stu-id="ca4dd-123">In the Description field, type a value.</span></span>
12. <span data-ttu-id="ca4dd-124">Kirjoita arvo Yhteyshenkilön puhelinnumero/osoite -kenttään.</span><span class="sxs-lookup"><span data-stu-id="ca4dd-124">In the Contact number/address field, type a value.</span></span>
    * <span data-ttu-id="ca4dd-125">Hakijan henkilökohtaiset tiedot.</span><span class="sxs-lookup"><span data-stu-id="ca4dd-125">Applicant personal information.</span></span>  
    * <span data-ttu-id="ca4dd-126">Voit syöttää hakijalle tarvittaessa lisätietoja henkilökohtaisiin tietoihin.</span><span class="sxs-lookup"><span data-stu-id="ca4dd-126">You can enter additional personal information for the applicant, if needed.</span></span> <span data-ttu-id="ca4dd-127">Tiedot voivat olla esimerkiksi syntymäpäivä, etninen alkuperä, sukupuoli tai siviilisääty.</span><span class="sxs-lookup"><span data-stu-id="ca4dd-127">For example, this can include birth date, ethnic origin, gender, or marital status.</span></span>  
13. <span data-ttu-id="ca4dd-128">Valitse toimintoruudussa Osaamisalueet.</span><span class="sxs-lookup"><span data-stu-id="ca4dd-128">On the Action Pane, click Competencies.</span></span>
    * <span data-ttu-id="ca4dd-129">Voit syöttää hakijan osaamisalueprofiilin, joka sisältää osaamisalueet, työkokemus, koulutuksen ja todistukset.</span><span class="sxs-lookup"><span data-stu-id="ca4dd-129">You can enter the applicant's competency profile, including their skills, professional experiences, education, tests, or certificates.</span></span>  
    * <span data-ttu-id="ca4dd-130">Näitä tietoja voidaan käyttää yhdistettäessä hakijan osaamisalueet yrityksen tiedoissa määritettyjen töihin liitettyihin osaamisalueiden kanssa.</span><span class="sxs-lookup"><span data-stu-id="ca4dd-130">This information can be used to map the applicant's skills to the skills associated with the jobs defined in your company's data.</span></span>   

## <a name="create-an-application-for-the-applicant"></a><span data-ttu-id="ca4dd-131">Hakemuksen luominen hakijalle</span><span class="sxs-lookup"><span data-stu-id="ca4dd-131">Create an application for the applicant</span></span>
1. <span data-ttu-id="ca4dd-132">Valitse Hakemukset.</span><span class="sxs-lookup"><span data-stu-id="ca4dd-132">Click Applications.</span></span>
2. <span data-ttu-id="ca4dd-133">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="ca4dd-133">Click New.</span></span>
3. <span data-ttu-id="ca4dd-134">Avaa haku valitsemalla Työhönottoprojekti-kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="ca4dd-134">In the Recruitment project field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="ca4dd-135">Kun valitset työhönottoprojektin, hakija liitetään tiettyyn kyseisen työhönottoprojektin avoimeen työpaikkaan.</span><span class="sxs-lookup"><span data-stu-id="ca4dd-135">By selecting a recruitment project, the applicant will be associated with a specific opening included in that recruitment project.</span></span>  
4. <span data-ttu-id="ca4dd-136">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="ca4dd-136">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="ca4dd-137">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="ca4dd-137">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="ca4dd-138">Oletusarvoisesti työ ja osasto perustuvat valittuun työhönottoprojektiin.</span><span class="sxs-lookup"><span data-stu-id="ca4dd-138">By default, the job and department are based on the selected recruitment project.</span></span>  
6. <span data-ttu-id="ca4dd-139">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="ca4dd-139">Click Save.</span></span>
    * <span data-ttu-id="ca4dd-140">Kun hakemus on tallennettu, voit liittää siihen asiakirjoja. Niitä ovat esimerkiksi hakijan kokemus, palkkiot ja kansilehti.</span><span class="sxs-lookup"><span data-stu-id="ca4dd-140">After saving the application, you can attach documents to it, including the applicant's experience, awards, and cover letter.</span></span>  



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]