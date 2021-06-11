---
title: Syötä osaamisalueet
description: Työt ja esimiehet voivat syöttää osaamisalueita Dynamics 365 Human Resourcesiin.
author: andreabichsel
manager: tfehr
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: HcmSkill, HcmSkillGapProfile, HcmSkillMapping, HcmSkillType, HcmEmployeeDevelopmentWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 3361
ms.assetid: c2ce94c0-933d-4edb-822c-7f0e7b49e4ee
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Human Resources
ms.openlocfilehash: b24d37292a2e9749fb2fde06b9f03fcd13db0bbe
ms.sourcegitcommit: 48528233e0f02dbd47e96e030254ef65f2bb899e
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/20/2021
ms.locfileid: "6076590"
---
# <a name="enter-skills"></a><span data-ttu-id="f05ad-103">Syötä osaamisalueet</span><span class="sxs-lookup"><span data-stu-id="f05ad-103">Enter skills</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="f05ad-104">Määritä tavoite- tai todelliset osaamisalueet työntekijöille, hakijoille tai yhteyshenkilöille Dynamics 365 Human Resourcesissa.</span><span class="sxs-lookup"><span data-stu-id="f05ad-104">You can enter target skills or actual skills for workers, applicants, or contacts in Dynamics 365 Human Resources.</span></span> <span data-ttu-id="f05ad-105">Tavoitetaito on taito, jonka henkilö aikoo saavuttavansa.</span><span class="sxs-lookup"><span data-stu-id="f05ad-105">A target skill is a skill that a person plans to achieve.</span></span> <span data-ttu-id="f05ad-106">Todellisella osaamisalueella tarkoitetaan osaamista, jonka henkilöllä tällä hetkellä on.</span><span class="sxs-lookup"><span data-stu-id="f05ad-106">An actual skill is a skill that a person currently has.</span></span>

## <a name="create-a-workflow-to-auto-approve-skills"></a><span data-ttu-id="f05ad-107">Osaamisalueiden automaattisen hyväksymisen työnkulun luominen</span><span class="sxs-lookup"><span data-stu-id="f05ad-107">Create a workflow to auto-approve skills</span></span>

<span data-ttu-id="f05ad-108">Jos haluat määrittää osaamisalueita ilman hyväksyntää, sinun on luotava työnkulku osaamisalueiden automaattista hyväksymistä varten.</span><span class="sxs-lookup"><span data-stu-id="f05ad-108">To enter skills without requiring approval, you must create a workflow to auto-approve skills.</span></span>

> [!NOTE]
> <span data-ttu-id="f05ad-109">Työntekijöiden syötetyt osaamisalueet edellyttävät aina esimiehen hyväksyntää.</span><span class="sxs-lookup"><span data-stu-id="f05ad-109">Skills entered by workers always require manager approval.</span></span> <span data-ttu-id="f05ad-110">Tämä työnkulku hyväksyy vain esimiesten työntekijöiden puolesta syötetyt osaamisalueet automaattisesti.</span><span class="sxs-lookup"><span data-stu-id="f05ad-110">This workflow only auto-approves skills entered by managers on behalf of their workers.</span></span>

1. <span data-ttu-id="f05ad-111">Valitse **Henkilöstön hallinta** -työtilassa **Linkit**.</span><span class="sxs-lookup"><span data-stu-id="f05ad-111">In the **Personnel management** workspace, select **Links**.</span></span>

2. <span data-ttu-id="f05ad-112">Valitse **Määritys**-kohdasta **Henkilöstöhallinnon työnkulut**.</span><span class="sxs-lookup"><span data-stu-id="f05ad-112">Under **Setup**, select **Human resources workflows**.</span></span>

3. <span data-ttu-id="f05ad-113">Valitse **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="f05ad-113">Select **New**.</span></span>

4. <span data-ttu-id="f05ad-114">Valitse **Luo työnkulku** -ruudusta **Työntekijän osaamisalueet**.</span><span class="sxs-lookup"><span data-stu-id="f05ad-114">In the **Create workflow** pane, select **Worker skills**.</span></span>

   <span data-ttu-id="f05ad-115">[![Työntekijän osaamisaluetyönkulun valinta](media/hr-develop-skills-new-workflow.png)](media/hr-develop-skills-new-workflow.png)</span><span class="sxs-lookup"><span data-stu-id="f05ad-115">[![Select Worker skills workflow](media/hr-develop-skills-new-workflow.png)](media/hr-develop-skills-new-workflow.png)</span></span>

5. <span data-ttu-id="f05ad-116">Valitse **Avataanko tämä tiedosto** -valintaruudusta **Avaa**.</span><span class="sxs-lookup"><span data-stu-id="f05ad-116">In the **Open this file?** dialogue, select **Open**.</span></span> <span data-ttu-id="f05ad-117">Kirjoita tunnistetietosi, kun näet kehotteen.</span><span class="sxs-lookup"><span data-stu-id="f05ad-117">When prompted, enter your credentials.</span></span>

6. <span data-ttu-id="f05ad-118">Valitse työnkulun editorissa **Hyväksy osaamisalueet** -työnkulun elementti ja vedä se pohjaan perustuvaan sovellukseen.</span><span class="sxs-lookup"><span data-stu-id="f05ad-118">In the workflow editor, select the **Approve skills** workflow element and drag it onto the canvas.</span></span>

   <span data-ttu-id="f05ad-119">[![Valitse Osaamisaluetyönkulun elementin hyväksyminen](media/hr-develop-skills-element.png)](media/hr-develop-skills-element.png)</span><span class="sxs-lookup"><span data-stu-id="f05ad-119">[![Select Approve skills workflow element](media/hr-develop-skills-element.png)](media/hr-develop-skills-element.png)</span></span>

7. <span data-ttu-id="f05ad-120">Liitä **Aloitus**-elementti **Hyväksy osaamisalueet 1** -elementtiin ja liitä sitten **Hyväksy osaamisalueet 1** -elementti **Loppu**-elementtiin.</span><span class="sxs-lookup"><span data-stu-id="f05ad-120">Connect the **Start** element to the **Approve skills 1** element, and then connect the **Approve skills 1** element to the **End** element.</span></span> <span data-ttu-id="f05ad-121">Sinun on ehkä siirryttävä alaspäin, jos haluat nähdä **Loppu**-elementin.</span><span class="sxs-lookup"><span data-stu-id="f05ad-121">You might need to scroll down to see the **End** element.</span></span> <span data-ttu-id="f05ad-122">Voit vetää sitä lähemmäksi muita elementtejä.</span><span class="sxs-lookup"><span data-stu-id="f05ad-122">You can drag it closer to the other elements.</span></span>

   <span data-ttu-id="f05ad-123">[![Yhdistä työnkulun elementit](media/hr-develop-skills-connect-elements.png)](media/hr-develop-skills-connect-elements.png)</span><span class="sxs-lookup"><span data-stu-id="f05ad-123">[![Connect workflow elements](media/hr-develop-skills-connect-elements.png)](media/hr-develop-skills-connect-elements.png)</span></span>

8. <span data-ttu-id="f05ad-124">Kaksoisnapsauta **Hyväksy osaamisalueet 1** -työnkulkuelementtiä ja napsauta **vaiheen 1** elementtiä hiiren kakkospainikkeella.</span><span class="sxs-lookup"><span data-stu-id="f05ad-124">Double-click the **Approve skills 1** workflow element, and then right-click the **Step 1** element.</span></span> <span data-ttu-id="f05ad-125">Napsauta **vaiheen 1** elementtiä hiiren kakkospainikkeella ja valitse **Ominaisuudet**.</span><span class="sxs-lookup"><span data-stu-id="f05ad-125">Right-click the **Step 1** element, and then select **Properties**.</span></span>

9. <span data-ttu-id="f05ad-126">Valitse **Ominaisuudet**-ikkunasta **Ehto** vasemmanpuoleisessa siirtymispalkissa.</span><span class="sxs-lookup"><span data-stu-id="f05ad-126">In the **Properties** window, select **Condition** on the left-hand nav bar.</span></span>

10. <span data-ttu-id="f05ad-127">Valitse **Suorita tämä vaihe vain, kun seuraava ehto täyttyy**.</span><span class="sxs-lookup"><span data-stu-id="f05ad-127">Select **Run this step only when the following condition is met**.</span></span>

11. <span data-ttu-id="f05ad-128">Valitse **Lisää ehto**.</span><span class="sxs-lookup"><span data-stu-id="f05ad-128">Select **Add condition**.</span></span> <span data-ttu-id="f05ad-129">Valitse **Missä**-ehdon jälkeen **Työntekijän itsepalvelun osaamisalueet** ja valitse sitten **Työntekijän itsepalvelun osaamisalueet.Henkilö**.</span><span class="sxs-lookup"><span data-stu-id="f05ad-129">After **Where**, select **Employee self service skills**, and then select **Employee self service skills.Person**.</span></span> <span data-ttu-id="f05ad-130">Valitse arvon **on** jälkeen **kenttä** ja valitse sitten **Käyttäjä suhteeseen.Henkilö**.</span><span class="sxs-lookup"><span data-stu-id="f05ad-130">After **is**, select **field**, and then select **User to person relationship.Person**.</span></span>

    <span data-ttu-id="f05ad-131">[![Määritä ehto](media/hr-develop-skills-condition.png)](media/hr-develop-skills-condition.png)</span><span class="sxs-lookup"><span data-stu-id="f05ad-131">[![Specify condition](media/hr-develop-skills-condition.png)](media/hr-develop-skills-condition.png)</span></span>

12. <span data-ttu-id="f05ad-132">Valitse **Määritys** vasemmalla puolella olevasta valikosta.</span><span class="sxs-lookup"><span data-stu-id="f05ad-132">Select **Assignment** on the left-hand nav bar.</span></span>

13. <span data-ttu-id="f05ad-133">Valitse **Hierarkia** **Määrityksen tyyppi** -välilehdestä.</span><span class="sxs-lookup"><span data-stu-id="f05ad-133">On the **Assignment type** tab, select **Hierarchy**.</span></span>

14. <span data-ttu-id="f05ad-134">Valitse **Hierarkian valinta** -välilehden **Hierarkiatyyppi:** -kentässä **Hallintahierarkia**.</span><span class="sxs-lookup"><span data-stu-id="f05ad-134">On the **Hierarchy selection** tab, in the **Hierarchy type:** field, select **Managerial hierarchy**.</span></span>

    <span data-ttu-id="f05ad-135">[![Hallintahierarkian asetukset](media/hr-develop-skills-hierarchy.png)](media/hr-develop-skills-hierarchy.png)</span><span class="sxs-lookup"><span data-stu-id="f05ad-135">[![Specify managerial hierarchy](media/hr-develop-skills-hierarchy.png)](media/hr-develop-skills-hierarchy.png)</span></span>

15. <span data-ttu-id="f05ad-136">Valitse **Sulje**, valitse **Työnkulku** kaavan polusta ja valitse sitten **Tallenna ja sulje**.</span><span class="sxs-lookup"><span data-stu-id="f05ad-136">Select **Close**, select **Workflow** in the canvas breadcrumb, and then select **Save and close**.</span></span>

<span data-ttu-id="f05ad-137">Lisätietoja työnkulkujen luomisesta on kohdassa [Työnkulkujärjestelmän yleiskatsaus](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/overview-workflow-system?toc=/dynamics365/human-resources/toc.json).</span><span class="sxs-lookup"><span data-stu-id="f05ad-137">For more information about creating workflows, see [Workflow system overview](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/overview-workflow-system?toc=/dynamics365/human-resources/toc.json).</span></span>

## <a name="enter-skills-for-a-worker"></a><span data-ttu-id="f05ad-138">Työntekijän osaamisalueille syötetyt tiedot</span><span class="sxs-lookup"><span data-stu-id="f05ad-138">Enter skills for a worker</span></span>

1. <span data-ttu-id="f05ad-139">Valitse työntekijä.</span><span class="sxs-lookup"><span data-stu-id="f05ad-139">Select a worker.</span></span>

2. <span data-ttu-id="f05ad-140">Valitse **Työntekijä**-sivun toimintopalkissa **Henkilö** ja valitse sitten **Osaamisalueet**.</span><span class="sxs-lookup"><span data-stu-id="f05ad-140">In the action bar of the **Worker** page, select **Person**, and then select **Skills**.</span></span>

3. <span data-ttu-id="f05ad-141">Täytä **Osaamisalueet**-sivulla kunkin osaamisalueen kentät:</span><span class="sxs-lookup"><span data-stu-id="f05ad-141">On the **Skills** page, complete the following fields for each skill:</span></span>

   - <span data-ttu-id="f05ad-142">**Osaamisalue**: Valitse osaamisalue.</span><span class="sxs-lookup"><span data-stu-id="f05ad-142">**Skill**: Select a skill.</span></span>
   - <span data-ttu-id="f05ad-143">**Tasotyyppi**: Valitse **osaamisalue**, joka työntekijällä on jo, tai valitse sen osaamisalueen **kohde**, jolla työntekijä työskentelee.</span><span class="sxs-lookup"><span data-stu-id="f05ad-143">**Level type**: Select **Actual** for a skill the worker already has, or select **Target** for a skill the worker is working toward.</span></span>
   - <span data-ttu-id="f05ad-144">**Taso**: Valitse työntekijän osaamisalueen taso.</span><span class="sxs-lookup"><span data-stu-id="f05ad-144">**Level**: Select a level for the worker's skill.</span></span>
   - <span data-ttu-id="f05ad-145">**Tason päivämäärä**: Valitse päivämäärä kalenterityökalussa.</span><span class="sxs-lookup"><span data-stu-id="f05ad-145">**Level date**: Select a date in the calendar tool.</span></span>
   - <span data-ttu-id="f05ad-146">**Tarkastaja**: Valitse tarvittaessa tarkastaja luettelosta.</span><span class="sxs-lookup"><span data-stu-id="f05ad-146">**Examiner**: If appropriate, select an examiner from the list.</span></span> <span data-ttu-id="f05ad-147">Voit suodattaa hakusi.</span><span class="sxs-lookup"><span data-stu-id="f05ad-147">You can filter your search.</span></span>
   - <span data-ttu-id="f05ad-148">**Kokemusvuodet**: Syötä kokemusvuodet.</span><span class="sxs-lookup"><span data-stu-id="f05ad-148">**Years of experience**: Enter years of experience.</span></span>
   - <span data-ttu-id="f05ad-149">**Vahvistettu**: Jos osaamisalue vahvistetaan, valitse tämä valintaruutu.</span><span class="sxs-lookup"><span data-stu-id="f05ad-149">**Verified**: If the skill is verified, check the box.</span></span>
   - <span data-ttu-id="f05ad-150">**Vahvistanut**: Kirjoita todentajan nimi.</span><span class="sxs-lookup"><span data-stu-id="f05ad-150">**Verified by**: Enter the name of the verifier.</span></span>

4. <span data-ttu-id="f05ad-151">Kun olet syöttänyt osaamisalueet, valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="f05ad-151">When you're done entering skills, select **Save**.</span></span>

## <a name="see-also"></a><span data-ttu-id="f05ad-152">Lisätietoja</span><span class="sxs-lookup"><span data-stu-id="f05ad-152">See also</span></span>

[<span data-ttu-id="f05ad-153">Osaamisalueiden määritykset</span><span class="sxs-lookup"><span data-stu-id="f05ad-153">Configure skills</span></span>](hr-develop-skills.md)<br>
[<span data-ttu-id="f05ad-154">Osaamisalueiden kartoitus</span><span class="sxs-lookup"><span data-stu-id="f05ad-154">Map skills</span></span>](hr-develop-map-skills.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]