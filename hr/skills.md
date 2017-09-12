---
title: "Työvoiman osaamisalueiden kohdistaminen liiketoimintatarpeisiin"
description: "Voit seurata työntekijöillä, hakijoilla tai yhteyshenkilöillä olevia osaamisalueita tai mitä osaamisalueita heillä pitäisi olla voidakseen suoriutua rooleistaan tehokkaasti. Voit myös määrittää tietyn työn edellyttämät osaamisalueet."
author: kherr75
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
ms.search.form: HcmSkill, HcmSkillGapProfile, HcmSkillMapping, HcmSkillType
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 3361
ms.assetid: c2ce94c0-933d-4edb-822c-7f0e7b49e4ee
ms.search.region: Global
ms.author: kherr
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Talent July 2017 update
ms.translationtype: Human Translation
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 2b76064049daccdcdff04c9f2fdde9a8b9c9e8e0
ms.contentlocale: fi-fi
ms.lasthandoff: 08/29/2017

---

# <a name="align-workforce-skills-with-business-needs"></a><span data-ttu-id="37feb-104">Työvoiman osaamisalueiden kohdistaminen liiketoimintatarpeisiin</span><span class="sxs-lookup"><span data-stu-id="37feb-104">Align workforce skills with business needs</span></span>

[!include[banner](includes/banner.md)]


<span data-ttu-id="37feb-105">Voit seurata työntekijöillä, hakijoilla tai yhteyshenkilöillä olevia osaamisalueita tai mitä osaamisalueita heillä pitäisi olla voidakseen suoriutua rooleistaan tehokkaasti.</span><span class="sxs-lookup"><span data-stu-id="37feb-105">You can track the skills that workers, applicants, or contact persons have, or should have, to fulfill their roles effectively.</span></span> <span data-ttu-id="37feb-106">Voit myös määrittää tietyn työn edellyttämät osaamisalueet.</span><span class="sxs-lookup"><span data-stu-id="37feb-106">You can also specify the skills that are required for a specific job.</span></span>

<span data-ttu-id="37feb-107">Seurattavia osaamisalueita ovat esimerkiksi seuraavat:</span><span class="sxs-lookup"><span data-stu-id="37feb-107">Examples of skills you can track include the following:</span></span>
-   <span data-ttu-id="37feb-108">Esimiestaito – kyky valvoa muiden työskentelyä.</span><span class="sxs-lookup"><span data-stu-id="37feb-108">Supervisory – Ability to supervise the work of others.</span></span>
-   <span data-ttu-id="37feb-109">Johtajuus – kyky johtaa työntekijöitä ja liiketoimintayksiköitä.</span><span class="sxs-lookup"><span data-stu-id="37feb-109">Leadership – Ability to lead employees and business domains.</span></span>
-   <span data-ttu-id="37feb-110">Suunnittelu – kaukonäköisyys - kyky nähdä eteenpäin, luoda visioita ja saattaa ne loppuun.</span><span class="sxs-lookup"><span data-stu-id="37feb-110">Planning – Ability to look ahead, to form visions, and to see them through.</span></span>
-   <span data-ttu-id="37feb-111">HTML-kyky kirjoittaa HTML-koodia.</span><span class="sxs-lookup"><span data-stu-id="37feb-111">HTML – Ability to write HTML code.</span></span>

<span data-ttu-id="37feb-112">Ennen kuin voit määrittää osaamisalueen henkilölle tai työlle, luoda osaamisaluekartoitushaun tai luoda osaamisprofiilin, osaamisalueiden tiedot on lisättävä **Osaamisalueet**-sivulle.</span><span class="sxs-lookup"><span data-stu-id="37feb-112">Before you can assign a skill to a person or a job, create a skill-mapping search, or create a skill profile, you must enter information about the skills on the **Skills** page.</span></span> <span data-ttu-id="37feb-113">Voit valita jokaiselle osaamisalueelle osaamisaluetyypin ja arviointimallin.</span><span class="sxs-lookup"><span data-stu-id="37feb-113">For each skill, you can select a skill type and a rating model.</span></span>

## <a name="rating-models"></a><span data-ttu-id="37feb-114">Arviointimallit</span><span class="sxs-lookup"><span data-stu-id="37feb-114">Rating models</span></span>
<span data-ttu-id="37feb-115">Arviointimallien avulla voit arvioida henkilön osaamisalueen todellisen tason, tason joka hänen tulee saavuttaa tai tason, joka tarvitaan työssä.</span><span class="sxs-lookup"><span data-stu-id="37feb-115">Rating models help evaluate a person's actual level of skill, the level they should work to achieve, or the level of skill that is required for a job.</span></span> <span data-ttu-id="37feb-116">Voit kirjoittaa arviointimallille enintään 10 tasoa.</span><span class="sxs-lookup"><span data-stu-id="37feb-116">You can enter up to 10 levels for a rating model.</span></span>  <span data-ttu-id="37feb-117">Kullekin arviointimallin tasolle määritetään kerroin.</span><span class="sxs-lookup"><span data-stu-id="37feb-117">Each level in a rating model is assigned a factor.</span></span>  <span data-ttu-id="37feb-118">Kertoimen arvoa käytetään eri luokitusmalleja käyttävien osaamisalueiden normalisointiin.</span><span class="sxs-lookup"><span data-stu-id="37feb-118">The factor value will be used to normalize the scores of skills that use different rating models.</span></span>  <span data-ttu-id="37feb-119">Kertoimen on oltava numero väliltä 0-9, ja kullakin tasolla on oltava yksilöllinen kerroin.</span><span class="sxs-lookup"><span data-stu-id="37feb-119">The factor must be a number between 0-9 and each level must have a unique factor.</span></span>  <span data-ttu-id="37feb-120">Tasoja, joilla on korkeammat kertoimen arvot, painotetaan enemmän arviointimallissa.</span><span class="sxs-lookup"><span data-stu-id="37feb-120">Levels with higher factor values carry more weight in a rating model.</span></span>

## <a name="specify-job-skills"></a><span data-ttu-id="37feb-121">Määritä työn osaamisalueet</span><span class="sxs-lookup"><span data-stu-id="37feb-121">Specify job skills</span></span>
<span data-ttu-id="37feb-122">Kun syötät tietoja työstä, voit määrittää osaamisalueita joita henkilöllä tulisi olla, ennen kuin hän voi toimia kyseisessä työssä.</span><span class="sxs-lookup"><span data-stu-id="37feb-122">When you enter information about a job, you can specify the skills that a person should have to perform the work required for the job.</span></span>  <span data-ttu-id="37feb-123">Voi lisäksi määrittää kullekin osaamisalueelle toivotun tason sekä osaamisalueen tärkeystason.</span><span class="sxs-lookup"><span data-stu-id="37feb-123">In addition you can specify the desired level for each skill as well the level of importance of the skill.</span></span> <span data-ttu-id="37feb-124">Eri töissä voidaan edellyttää saman osaamisalueen eri tärkeystasoja.</span><span class="sxs-lookup"><span data-stu-id="37feb-124">Different jobs can require different levels of importance for the same skill.</span></span>

## <a name="enter-skills-for-workers-applicants-or-contacts"></a><span data-ttu-id="37feb-125">Kirjoita työntekijöiden, hakijoiden tai yhteyshenkilöiden osaamisalueet.</span><span class="sxs-lookup"><span data-stu-id="37feb-125">Enter skills for workers, applicants, or contacts</span></span>
<span data-ttu-id="37feb-126">Määritä tavoite- tai todelliset osaamisalueet työntekijöille, hakijoille tai yhteyshenkilöille.</span><span class="sxs-lookup"><span data-stu-id="37feb-126">You can enter target skills or actual skills for workers, applicants, or contacts.</span></span> <span data-ttu-id="37feb-127">Tavoitetaito on taito, jonka henkilö aikoo saavuttavansa.</span><span class="sxs-lookup"><span data-stu-id="37feb-127">A target skill is a skill that a person plans to achieve.</span></span> <span data-ttu-id="37feb-128">Todellisella osaamisalueella tarkoitetaan osaamista, jonka henkilöllä tällä hetkellä on.</span><span class="sxs-lookup"><span data-stu-id="37feb-128">An actual skill is a skill that a person currently has.</span></span>

## <a name="skill-mapping-and-skill-mapping-profiles"></a><span data-ttu-id="37feb-129"> Osaamisaluekartoitukset ja kartoitusprofiilit</span><span class="sxs-lookup"><span data-stu-id="37feb-129">Skill mapping and Skill mapping profiles</span></span>
<span data-ttu-id="37feb-130">Voit luoda osaamisaluekartoitushaun ja etsiä työntekijän, hakijan tai yhteyshenkilön, jolla on tietyntyyppiseen tehtävään tarvittava pätevyys.</span><span class="sxs-lookup"><span data-stu-id="37feb-130">You can create a skill-mapping search to find a worker, applicant, or contact person who is qualified to perform a specific type of task.</span></span> <span data-ttu-id="37feb-131">Osaamisaluekartoitushaku etsii osaamisalueita, koulutusta, todistuksia, luottamustehtäviä ja projektikokemusta ja palauttaa annettuja ehtoja vastaavat tulokset.</span><span class="sxs-lookup"><span data-stu-id="37feb-131">Skill-mapping searches look across skills, education, certificates, positions of trust and project experience and return a results that match the criteria entered.</span></span>  <span data-ttu-id="37feb-132">Voi esimerkiksi olla hyödyllistä tietää organisaation työntekijöiden koulutustaso.</span><span class="sxs-lookup"><span data-stu-id="37feb-132">For example, it might be useful to know which workers in your organization earned their CPA.</span></span>

<span data-ttu-id="37feb-133">Osaamisaluekartoitusprofiilien avulla voit etsiä nykyisiä työntekijöitä tai hakijoita, joiden pätevyys vastaa suoraan liiketoiminnan tarpeita.</span><span class="sxs-lookup"><span data-stu-id="37feb-133">Skill-mapping profiles allow you to find current employees or candidates with qualifications that directly correspond to business needs.</span></span>  <span data-ttu-id="37feb-134">Voit esimerkiksi luoda osaamisaluekartoitusprofiileja organisaatiossa avoimena olevia toimia varten.</span><span class="sxs-lookup"><span data-stu-id="37feb-134">For example, you could create a skill-mapping profile for an open position in your organization.</span></span> <span data-ttu-id="37feb-135">Luomalla profiilin tietylle työlle ja kopioimalla työn osaamisalueet, koulutuksen ja todistukset profiiliin voit nopeasti hakea työntekijöitä, hakijoita ja yhteyshenkilöitä, jotka vastaavat yhtä tai useampaa profiilissa määritettyä ehtoa, ja tarkastella sellaisten hakijoiden luetteloa, joiden osaamisalueet lähimmin vastaavat työn vaatimuksia.</span><span class="sxs-lookup"><span data-stu-id="37feb-135">By creating a profile for a particular job and copying the skills, education and certificates from that job to the profile, you can quickly search workers, applicants and contact persons who match one or more of the criteria entered on the profile and view a list of the candidates whose skills most closely match the skills required for the job.</span></span>

><span data-ttu-id="37feb-136">**Huomautus** Vain osaamisaluekartoitushakuihin valitut työntekijät, hakijat ja yhteyshenkilöt voidaan näyttää osaamisaluekartoituksen tulosluettelossa tai sisällyttää osaamisalueprofiilin.</span><span class="sxs-lookup"><span data-stu-id="37feb-136">**Note** Only workers, applicants, and contact persons who are selected to be included in skill mapping searches can be displayed in a skill-mapping results list, or included in a skill profile.</span></span> <span data-ttu-id="37feb-137">Jos haluat sisällyttää työntekijän, hakijan tai yhteyshenkilön osaamisaluekartoitushakuihin, määritä **Sisällytä osaamisaluekartoitukseen** -asetukseksi Kyllä seuraavilla sivuilla:</span><span class="sxs-lookup"><span data-stu-id="37feb-137">To include a worker, applicant, or contact person in skill mapping searches, set the **Include in skill mapping** selection to Yes in the following pages:</span></span>

> + <span data-ttu-id="37feb-138">Työntekijä</span><span class="sxs-lookup"><span data-stu-id="37feb-138">Worker</span></span>
> + <span data-ttu-id="37feb-139">Työntekijä</span><span class="sxs-lookup"><span data-stu-id="37feb-139">Employee</span></span>
> + <span data-ttu-id="37feb-140">Hakija</span><span class="sxs-lookup"><span data-stu-id="37feb-140">Applicant</span></span>
> + <span data-ttu-id="37feb-141">Yhteyshenkilöt</span><span class="sxs-lookup"><span data-stu-id="37feb-141">Contacts</span></span>

## <a name="skill-gap-analysis-and-skill-profile-analysis"></a><span data-ttu-id="37feb-142">Osaamiseroanalyysi ja osaamisprofiilianalyysi</span><span class="sxs-lookup"><span data-stu-id="37feb-142">Skill gap analysis and skill profile analysis</span></span>
<span data-ttu-id="37feb-143">Luomalla osaamisprofiilianalyysin voit tarkastella luetteloa työntekijän, hakijan tai yhteyshenkilön osaamisalueista tiettynä päivänä.</span><span class="sxs-lookup"><span data-stu-id="37feb-143">You can create a skill profile analysis to view a list of the competencies of a worker, applicant, or contact person as of a specific date.</span></span> <span data-ttu-id="37feb-144">Voit luoda osaamisalueaukkoanalyysi, jotta voit verrata henkilön taitoja työhön vaadittaviin taitoihin</span><span class="sxs-lookup"><span data-stu-id="37feb-144">You can create a skill gap analysis to compare a person’s skills and the skills that are required for a specific job.</span></span>  



<a name="see-also"></a><span data-ttu-id="37feb-145">Lisätietoja</span><span class="sxs-lookup"><span data-stu-id="37feb-145">See also</span></span>
--------

[<span data-ttu-id="37feb-146">Henkilöstöhallinto</span><span class="sxs-lookup"><span data-stu-id="37feb-146">Human resources</span></span>](index.md)




