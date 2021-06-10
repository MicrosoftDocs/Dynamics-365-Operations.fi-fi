---
title: Osaamisalueiden määritykset
description: Voit seurata työntekijän osaamisalueita Dynamics 365 Human Resourcesissa. Voit myös määrittää tietyn työn edellyttämät osaamisalueet.
author: andreabichsel
manager: tfehr
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: HcmSkill, HcmSkillGapProfile, HcmSkillMapping, HcmSkillType, HcmEmployeeDevelopmentWorkspace
audience: Application User
ms.search.scope: Human Resources
ms.custom: 3361
ms.assetid: c2ce94c0-933d-4edb-822c-7f0e7b49e4ee
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Human Resources
ms.openlocfilehash: 816822d1f3d365b4c5571c13e9f596e1c5d5e59c
ms.sourcegitcommit: 48528233e0f02dbd47e96e030254ef65f2bb899e
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/20/2021
ms.locfileid: "6076556"
---
# <a name="configure-skills"></a><span data-ttu-id="23b68-104">Osaamisalueiden määritykset</span><span class="sxs-lookup"><span data-stu-id="23b68-104">Configure skills</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="23b68-105">Voit seurata työntekijän osaamisalueita Dynamics 365 Human Resourcesissa.</span><span class="sxs-lookup"><span data-stu-id="23b68-105">You can track your worker's skills in Dynamics 365 Human Resources.</span></span> <span data-ttu-id="23b68-106">Voit myös määrittää tietyn työn edellyttämät osaamisalueet.</span><span class="sxs-lookup"><span data-stu-id="23b68-106">You can also specify the skills that are required for a specific job.</span></span>

<span data-ttu-id="23b68-107">Seurattavia osaamisalueita ovat esimerkiksi:</span><span class="sxs-lookup"><span data-stu-id="23b68-107">Examples of skills you can track include:</span></span>

- <span data-ttu-id="23b68-108">Esimiestaito – kyky valvoa muiden työskentelyä.</span><span class="sxs-lookup"><span data-stu-id="23b68-108">Supervisory – Ability to supervise the work of others.</span></span>
- <span data-ttu-id="23b68-109">Johtajuus – kyky johtaa työntekijöitä ja liiketoimintayksiköitä.</span><span class="sxs-lookup"><span data-stu-id="23b68-109">Leadership – Ability to lead employees and business domains.</span></span>
- <span data-ttu-id="23b68-110">Suunnittelu – kaukonäköisyys - kyky nähdä eteenpäin, luoda visiolausekkeita ja saattaa ne loppuun.</span><span class="sxs-lookup"><span data-stu-id="23b68-110">Planning – Ability to look ahead, to form vision statements, and to see them through.</span></span>
- <span data-ttu-id="23b68-111">HTML-kyky kirjoittaa HTML-koodia.</span><span class="sxs-lookup"><span data-stu-id="23b68-111">HTML – Ability to write HTML code.</span></span>

<span data-ttu-id="23b68-112">Jos et ole vielä määrittänyt osaamisaluetyyppejä ja arviointimalleja, sinun on lisättävä joitakin tietoja ennen osaamisalueiden luomista.</span><span class="sxs-lookup"><span data-stu-id="23b68-112">If you haven't already set up skill types and rating models, you'll need to add some before creating skills.</span></span>

<span data-ttu-id="23b68-113">Seuraavat henkilöt voivat määrittää työntekijälle osaamisalueita:</span><span class="sxs-lookup"><span data-stu-id="23b68-113">The following people can enter skills for a worker:</span></span>

- <span data-ttu-id="23b68-114">Työntekijät voivat määrittää itseään varten osaamisalueita työntekijän itsepalvelussa.</span><span class="sxs-lookup"><span data-stu-id="23b68-114">Workers can enter skills for themselves in Employee self-service.</span></span> <span data-ttu-id="23b68-115">Nämä osaamisalueet edellyttävät esimiehen hyväksyntää.</span><span class="sxs-lookup"><span data-stu-id="23b68-115">These skills require manager approval.</span></span>
- <span data-ttu-id="23b68-116">Esimiehet voivat määrittää työntekijöille osaamisalueita.</span><span class="sxs-lookup"><span data-stu-id="23b68-116">Managers can enter skills for their workers.</span></span> <span data-ttu-id="23b68-117">Voit luoda työnkulun, joka hyväksyy nämä osaamisalueet automaattisesti.</span><span class="sxs-lookup"><span data-stu-id="23b68-117">You can create a workflow that auto-approves these skills.</span></span>

## <a name="create-a-skill-type"></a><span data-ttu-id="23b68-118">Luo osaamisaluetyyppi</span><span class="sxs-lookup"><span data-stu-id="23b68-118">Create a skill type</span></span>

<span data-ttu-id="23b68-119">Osaamisaluetyypit ovat luokkia, joihin yksittäiset osaamisalueet, kuten Hallinto tai Myynti, kuuluvat.</span><span class="sxs-lookup"><span data-stu-id="23b68-119">Skill types are categories that individual skills fall under, such as Administration or Sales.</span></span>

1. <span data-ttu-id="23b68-120">Valitse **Työntekijän kehitys** -työtilassa **Linkit**.</span><span class="sxs-lookup"><span data-stu-id="23b68-120">In the **Employee development** workspace, select **Links**.</span></span>

2. <span data-ttu-id="23b68-121">Valitse **Tasoasetukset**-kohdasta **Osaamisaluetyypit**.</span><span class="sxs-lookup"><span data-stu-id="23b68-121">Under **Competency setup**, select **Skill types**.</span></span>

3. <span data-ttu-id="23b68-122">Valitse **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="23b68-122">Select **New**.</span></span>

4. <span data-ttu-id="23b68-123">Täytä seuraavat kentät:</span><span class="sxs-lookup"><span data-stu-id="23b68-123">Complete the following fields:</span></span>

   - <span data-ttu-id="23b68-124">**Osaamisaluetyyppi**: anna osaamisaluetyypin nimi.</span><span class="sxs-lookup"><span data-stu-id="23b68-124">**Skill type**: Enter a name for the skill type.</span></span>
   - <span data-ttu-id="23b68-125">**Kuvaus**: anna osaamisaluetyypin kuvaus.</span><span class="sxs-lookup"><span data-stu-id="23b68-125">**Description**: Enter a description for the skill type.</span></span>

5. <span data-ttu-id="23b68-126">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="23b68-126">Select **Save**.</span></span>

## <a name="create-a-rating-model"></a><span data-ttu-id="23b68-127">Luo arvostelujärjestelmä</span><span class="sxs-lookup"><span data-stu-id="23b68-127">Create a rating model</span></span>

<span data-ttu-id="23b68-128">Arviointimallien avulla voit arvioida henkilön osaamisalueen todellisen tason, tason joka hänen tulee saavuttaa tai tason, joka tarvitaan työssä.</span><span class="sxs-lookup"><span data-stu-id="23b68-128">Rating models help evaluate a person's actual level of skill, the level they should work to achieve, or the level of skill required for a job.</span></span> <span data-ttu-id="23b68-129">Kullekin arviointimallin tasolle määritetään kerroin.</span><span class="sxs-lookup"><span data-stu-id="23b68-129">Each level in a rating model is assigned a factor.</span></span>

1. <span data-ttu-id="23b68-130">Valitse **Työntekijän kehitys** -työtilassa **Linkit**.</span><span class="sxs-lookup"><span data-stu-id="23b68-130">In the **Employee development** workspace, select **Links**.</span></span>

2. <span data-ttu-id="23b68-131">Valitse **Osaamisasetukset**-kohdasta **Arviointimallit**.</span><span class="sxs-lookup"><span data-stu-id="23b68-131">Under **Competency setup**, select **Rating models**.</span></span>

3. <span data-ttu-id="23b68-132">Valitse **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="23b68-132">Select **New**.</span></span>

4. <span data-ttu-id="23b68-133">Täytä seuraavat kentät:</span><span class="sxs-lookup"><span data-stu-id="23b68-133">Complete the following fields:</span></span>

   - <span data-ttu-id="23b68-134">**Luokitus**: Kirjoita arviointimallille nimi, esimerkiksi **Osaamisalueet**.</span><span class="sxs-lookup"><span data-stu-id="23b68-134">**Rating**: Enter a name for the rating model, such as **Skills**.</span></span>
   - <span data-ttu-id="23b68-135">**Kuvaus**: Kirjoita arviointimallille kuvaus, esimerkiksi **Osaamisalueluokitukset**.</span><span class="sxs-lookup"><span data-stu-id="23b68-135">**Description**: Enter a description for the rating model, such as **Skill ratings**.</span></span>

5. <span data-ttu-id="23b68-136">Valitse **Tasot**-osassa **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="23b68-136">In the **Levels** section, select **New**.</span></span> <span data-ttu-id="23b68-137">Täytä kunkin lisättävän tason kentät:</span><span class="sxs-lookup"><span data-stu-id="23b68-137">For each level you want to add, complete the following fields:</span></span>

   - <span data-ttu-id="23b68-138">**Taso**: Kirjoita tason nimi.</span><span class="sxs-lookup"><span data-stu-id="23b68-138">**Level**: Enter a name for the level.</span></span>
   - <span data-ttu-id="23b68-139">**Kuvaus**: Kirjoita tason kuvaus.</span><span class="sxs-lookup"><span data-stu-id="23b68-139">**Description**: Enter a description for the level.</span></span>
   - <span data-ttu-id="23b68-140">**Kerroin**: Syötä kerroinarvo väliltä 0-9.</span><span class="sxs-lookup"><span data-stu-id="23b68-140">**Factor**: Enter a factor value from 0-9.</span></span> <span data-ttu-id="23b68-141">Kertoimet auttavat normalisoimaan eri luokitusmalleja käyttäviä taitoja.</span><span class="sxs-lookup"><span data-stu-id="23b68-141">Factors help normalize the scores of skills that use different rating models.</span></span> <span data-ttu-id="23b68-142">Jokaisella tasolla on oltava yksilöivä kerroin.</span><span class="sxs-lookup"><span data-stu-id="23b68-142">Each level must have a unique factor.</span></span> <span data-ttu-id="23b68-143">Tasoja, joilla on korkeammat kertoimen arvot, painotetaan enemmän arviointimallissa.</span><span class="sxs-lookup"><span data-stu-id="23b68-143">Levels with higher factor values carry more weight in a rating model.</span></span>

   <span data-ttu-id="23b68-144">Jatka tasojen lisäämistä tarvittaessa.</span><span class="sxs-lookup"><span data-stu-id="23b68-144">Continue adding levels as necessary.</span></span> <span data-ttu-id="23b68-145">Voit syöttää kullekin arviointimallille enintään 10 tasoa.</span><span class="sxs-lookup"><span data-stu-id="23b68-145">You can enter up to 10 levels for each rating model.</span></span>

6. <span data-ttu-id="23b68-146">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="23b68-146">Select **Save**.</span></span>

## <a name="create-a-skill"></a><span data-ttu-id="23b68-147">Luo osaamisalue</span><span class="sxs-lookup"><span data-stu-id="23b68-147">Create a skill</span></span>

<span data-ttu-id="23b68-148">Ennen kuin voit määrittää osaamisalueen, luoda osaamisaluekartoitushaun tai osaamisprofiilin, osaamisalueiden tiedot on lisättävä **Osaamisalueet**-sivulle.</span><span class="sxs-lookup"><span data-stu-id="23b68-148">Before you can assign a skill, or create a skill-mapping search or skill profile, you must enter information about the skills on the **Skills** page.</span></span> <span data-ttu-id="23b68-149">Voit valita jokaiselle osaamisalueelle osaamisaluetyypin ja arviointimallin.</span><span class="sxs-lookup"><span data-stu-id="23b68-149">For each skill, you can select a skill type and a rating model.</span></span>

1. <span data-ttu-id="23b68-150">Valitse **Työntekijän kehitys** -työtilassa **Linkit**.</span><span class="sxs-lookup"><span data-stu-id="23b68-150">In the **Employee development** workspace, select **Links**.</span></span>

2. <span data-ttu-id="23b68-151">Valitse **Tasoasetukset**-kohdasta **Osaamisalueet**.</span><span class="sxs-lookup"><span data-stu-id="23b68-151">Under **Competency setup**, select **Skills**.</span></span>

3. <span data-ttu-id="23b68-152">Valitse **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="23b68-152">Select **New**.</span></span>

4. <span data-ttu-id="23b68-153">Täytä seuraavat kentät:</span><span class="sxs-lookup"><span data-stu-id="23b68-153">Complete the following fields:</span></span>

   - <span data-ttu-id="23b68-154">**Osaamisalue**: anna osaamisalueen nimi.</span><span class="sxs-lookup"><span data-stu-id="23b68-154">**Skill**: Enter a name for the skill.</span></span>
   - <span data-ttu-id="23b68-155">**Kuvaus**: anna osaamisalueen kuvaus.</span><span class="sxs-lookup"><span data-stu-id="23b68-155">**Description**: Enter a description for the skill.</span></span>
   - <span data-ttu-id="23b68-156">**Arvostelu**: Valitse arvostelumalli, jota haluat käyttää tässä osaamisalueessa.</span><span class="sxs-lookup"><span data-stu-id="23b68-156">**Rating**: Select the rating model you want to use for this skill.</span></span>
   - <span data-ttu-id="23b68-157">**Osaamisaluetyyppi**: Valitse osaamisaluetyyppien luettelosta.</span><span class="sxs-lookup"><span data-stu-id="23b68-157">**Skill type**: Select from the list of skill types.</span></span>

5. <span data-ttu-id="23b68-158">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="23b68-158">Select **Save**.</span></span>

## <a name="see-also"></a><span data-ttu-id="23b68-159">Lisätietoja</span><span class="sxs-lookup"><span data-stu-id="23b68-159">See also</span></span>

[<span data-ttu-id="23b68-160">Syötä osaamisalueet</span><span class="sxs-lookup"><span data-stu-id="23b68-160">Enter skills</span></span>](hr-develop-enter-skills.md)<br>
[<span data-ttu-id="23b68-161">Osaamisalueiden kartoitus</span><span class="sxs-lookup"><span data-stu-id="23b68-161">Map skills</span></span>](hr-develop-map-skills.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]