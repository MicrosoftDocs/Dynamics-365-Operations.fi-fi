---
title: Luo uusi projekti
description: Tämä ohjeaihe sisältää uuden projektin luomista käsitteleviä tietoja.
author: Yowelle
manager: AnnBe
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c8c52b8c1c86ea2f6e03cf439ba5930f1006ab4f
ms.sourcegitcommit: 241ada0945c72d769eaa70ae35aedbb6a3233fdf
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/02/2020
ms.locfileid: "3760533"
---
# <a name="create-a-new-project"></a><span data-ttu-id="0424d-103">Luo uusi projekti</span><span class="sxs-lookup"><span data-stu-id="0424d-103">Create a new project</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0424d-104">Luo uusi projekti seuraavalla tavalla.</span><span class="sxs-lookup"><span data-stu-id="0424d-104">Complete the following steps to create a new project.</span></span>

1. <span data-ttu-id="0424d-105">Valitse **Projektin hallinta** -sivulla **Uusi projekti** ja anna seuraavat arvot:</span><span class="sxs-lookup"><span data-stu-id="0424d-105">On the **Project management** page, select **New project**, and enter the following values:</span></span>

    - <span data-ttu-id="0424d-106">**Projektityyppi:** Aika ja materiaali</span><span class="sxs-lookup"><span data-stu-id="0424d-106">**Project type:** Time and material</span></span>
    - <span data-ttu-id="0424d-107">**Projektin nimi:** XYZ-päivitysvaihe 2</span><span class="sxs-lookup"><span data-stu-id="0424d-107">**Project name:** XYZ Upgrade Phase 2</span></span>
    - <span data-ttu-id="0424d-108">**Projektiryhmä**: TM\_WIP</span><span class="sxs-lookup"><span data-stu-id="0424d-108">**Project group:** TM\_WIP</span></span>
    - <span data-ttu-id="0424d-109">**Projektisopimuksen tunnus:** 00000002</span><span class="sxs-lookup"><span data-stu-id="0424d-109">**Project contract ID:** 00000002</span></span>

2. <span data-ttu-id="0424d-110">Valitse **Luo projekti**.</span><span class="sxs-lookup"><span data-stu-id="0424d-110">Select **Create project**.</span></span>

## <a name="assign-a-resource-to-a-project"></a><span data-ttu-id="0424d-111">Resurssin määrittäminen projektiin</span><span class="sxs-lookup"><span data-stu-id="0424d-111">Assign a resource to a project</span></span>

1. <span data-ttu-id="0424d-112">Valitse **Työntekijät**-sivun **Työntekijät**-luettelosta sen työntekijän tietue, jonka osaamisalueet määritit aiemmassa vaiheessa, ja avaa tietue.</span><span class="sxs-lookup"><span data-stu-id="0424d-112">On the **Workers** page, in the **Workers** list, select the record for the worker that you previously set up competencies for, and open the worker record.</span></span>
2. <span data-ttu-id="0424d-113">Valitse toimintoruudussa **Projekti**-välilehden **Asetukset**-ryhmästä **Määritä projektit**.</span><span class="sxs-lookup"><span data-stu-id="0424d-113">On the Action Pane, on the **Project** tab, in the **Setup** group, select **Assign projects**.</span></span>
3. <span data-ttu-id="0424d-114">Suodata **Resurssin oikeellisuustarkistuksen projektimääritykset** -sivun **Projektit**-välilehden **Lisää projekti valittuihin projekteihin** -kentässä **XYZ-päivitysvaihe 2** -projektiin.</span><span class="sxs-lookup"><span data-stu-id="0424d-114">On the **Resource validation project assignments** page, on the **Projects** tab, in the **Add the project to selected projects** field, filter on the **XYZ Upgrade Phase 2** project.</span></span>
4. <span data-ttu-id="0424d-115">Valitse **Jäljellä olevat projektit** -ruudusta haluamasi projekti ja lisää se **Valitut projektit** -ruutuun napsauttamalla nuolta.</span><span class="sxs-lookup"><span data-stu-id="0424d-115">In the **Remaining projects** pane, select a project, and then select the arrow button to add it to the **Selected projects** pane.</span></span>

<span data-ttu-id="0424d-116">Tarvittaessa voit myös määrittää resurssille luokkia.</span><span class="sxs-lookup"><span data-stu-id="0424d-116">You can also assign categories for a resource as you require.</span></span> <span data-ttu-id="0424d-117">Luokkatyyppi on joko **Kustannus** tai **Tuotto**.</span><span class="sxs-lookup"><span data-stu-id="0424d-117">The category type is either **Cost** or **Revenue**.</span></span> <span data-ttu-id="0424d-118">Luokkatyyppi määräytyy organisaation mukaan.</span><span class="sxs-lookup"><span data-stu-id="0424d-118">The category type is determined by your organization.</span></span> <span data-ttu-id="0424d-119">Jos resurssille ei ole määritetty luokkia, Finance etsii oletusluokan kustannusten ja tuoton tuntihinnoista.</span><span class="sxs-lookup"><span data-stu-id="0424d-119">If no categories are assigned for a resource, Finance looks up the default category on hour prices for cost and revenue.</span></span>

## <a name="set-up-project-resource-and-role-characteristics"></a><span data-ttu-id="0424d-120">Projektin resurssin ja rooliominaisuuksien määrittäminen</span><span class="sxs-lookup"><span data-stu-id="0424d-120">Set up project resource and role characteristics</span></span>

<span data-ttu-id="0424d-121">Projektipäällikkö voi projektin resursointitoiminnolla luoda projektissa tarvittavia rooleja.</span><span class="sxs-lookup"><span data-stu-id="0424d-121">A project manager can use the project resourcing functionality to create the roles that are required for the project.</span></span> <span data-ttu-id="0424d-122">Rooleja voidaan käyttää, kun vahvistetut resurssit eivät ole vielä tiedossa resurssien varaamisen aikana.</span><span class="sxs-lookup"><span data-stu-id="0424d-122">Roles can be used if confirmed resources are still unknown when resources are being reserved.</span></span> <span data-ttu-id="0424d-123">Rooleja voidaan väliaikaisesti varata suunnitelluiksi resursseiksi, jotta voit jatkaa projektin suunnitteluvaiheita.</span><span class="sxs-lookup"><span data-stu-id="0424d-123">Roles can be temporarily reserved as planned resources, so that you can continue the project planning stages.</span></span>

<span data-ttu-id="0424d-124">[![Esimerkki roolista](./media/projectresourcing05.jpg)](./media/projectresourcing05.jpg)</span><span class="sxs-lookup"><span data-stu-id="0424d-124">[![Example of a role](./media/projectresourcing05.jpg)](./media/projectresourcing05.jpg)</span></span> 

<span data-ttu-id="0424d-125">**Skenaario:** Contoso palkattiin suorittamaan aika- ja materiaaliprojekti, jolla on hyväksytty projektin perustamisasiakirja.</span><span class="sxs-lookup"><span data-stu-id="0424d-125">**Scenario:** Contoso was hired to complete a Time and material project that has an approved project charter.</span></span> <span data-ttu-id="0424d-126">Nuorempi projektipäällikkö on yhä laatimassa projektin laajuutta.</span><span class="sxs-lookup"><span data-stu-id="0424d-126">The junior project manager is still completing the scope of the project.</span></span> <span data-ttu-id="0424d-127">Resurssipäällikkö on parhaillaan määrittämässä resursseja, jotka varataan uuteen projektiin.</span><span class="sxs-lookup"><span data-stu-id="0424d-127">The resource manager is currently identifying specific resources that will be reserved to work on the new project.</span></span> <span data-ttu-id="0424d-128">Koska projekti on erityisen tärkeä, projektin sponsori on toivonut yhden rooleista olevan vastaava projektipäällikkö.</span><span class="sxs-lookup"><span data-stu-id="0424d-128">Because of the critical nature of the project, the project sponsor requested Senior project manager as one of the roles.</span></span> <span data-ttu-id="0424d-129">Resurssipäällikön on hankittava uusi resurssi, ja hän määrittää roolin järjestelmään siltä varalta, että nuorempi projektipäällikkö tarvitsee resurssitiedot projektin suunnittelua varten.</span><span class="sxs-lookup"><span data-stu-id="0424d-129">The resource manager must acquire the new resource and define the role in the system in case the junior project manager requires the resource information during project planning.</span></span>

<span data-ttu-id="0424d-130">Seuraavissa vaiheissa on esitetty, miten resurssipäällikkö voi määrittää vastaavan projektipäällikön roolin ja liittää siihen resurssin ominaisuudet.</span><span class="sxs-lookup"><span data-stu-id="0424d-130">The following steps show how the resource manager can set up the Senior project manager role and associate resource characteristics with it.</span></span> <span data-ttu-id="0424d-131">Myöhemmin roolin avulla voidaan hakea käytettävissä olevia resursseja, jotka vastaavat tarvittavia resurssin osaamisalueita.</span><span class="sxs-lookup"><span data-stu-id="0424d-131">Later, the role can be used to search for available resources that match the required resource competencies.</span></span>

1. <span data-ttu-id="0424d-132">Valitse **Määritä roolit** -sivulla **Uusi** ja anna seuraavat arvot:</span><span class="sxs-lookup"><span data-stu-id="0424d-132">On the **Setup roles** page, select **New**, and enter the following values:</span></span>

    - <span data-ttu-id="0424d-133">**Roolin tunnus:** Vastaava projektipäällikkö</span><span class="sxs-lookup"><span data-stu-id="0424d-133">**Role ID:** Senior Project Manager</span></span>
    - <span data-ttu-id="0424d-134">**Kuvaus:** Vastaava projektipäällikkö</span><span class="sxs-lookup"><span data-stu-id="0424d-134">**Description:** Senior Project Manager</span></span>

2. <span data-ttu-id="0424d-135">Valitse **Luo**.</span><span class="sxs-lookup"><span data-stu-id="0424d-135">Select **Create**.</span></span>
3. <span data-ttu-id="0424d-136">Valitse **Vastaava projektipäällikkö** -rooli ja sitten **Määritä ominaisuudet**.</span><span class="sxs-lookup"><span data-stu-id="0424d-136">Select the **Senior Project Manager** role, and then select **Configure characteristics**.</span></span>
4. <span data-ttu-id="0424d-137">Valitse **Ominaisuuden tyyppi** -kentästä **Osaamisalue**.</span><span class="sxs-lookup"><span data-stu-id="0424d-137">In the **Characteristics type** field, select **Skill**.</span></span>
5. <span data-ttu-id="0424d-138">Syötä **Käytettävissä olevat ominaisuudet** -kenttään haettava osaamisalue.</span><span class="sxs-lookup"><span data-stu-id="0424d-138">In the **Available characteristics** field, enter the skill to search for.</span></span>
6. <span data-ttu-id="0424d-139">Valitse **Ominaisuustyyppi**-kentästä **Todistus**.</span><span class="sxs-lookup"><span data-stu-id="0424d-139">In the **Characteristic type** field, select **Certificate**.</span></span>
7. <span data-ttu-id="0424d-140">Syötä **Käytettävissä olevat ominaisuudet** -kenttään haettava todistustyyppi.</span><span class="sxs-lookup"><span data-stu-id="0424d-140">In the **Available characteristics** field, enter the certificate type to search for.</span></span>

## <a name="assign-a-project-resource-to-a-project"></a><span data-ttu-id="0424d-141">Projektiresurssin määrittäminen projektiin</span><span class="sxs-lookup"><span data-stu-id="0424d-141">Assign a project resource to a project</span></span>

1. <span data-ttu-id="0424d-142">Valitse **Kaikki projektit** -sivulla **XYZ-päivitysvaihe 2** -projekti.</span><span class="sxs-lookup"><span data-stu-id="0424d-142">On the **All projects** page, select the **XYZ Upgrade Phase 2** project.</span></span>
2. <span data-ttu-id="0424d-143">Valitse **Projektiryhmä ja ajoitus** -välilehdestä **Lisää**.</span><span class="sxs-lookup"><span data-stu-id="0424d-143">On the **Project team and scheduling** tab, select **Add**.</span></span>
3. <span data-ttu-id="0424d-144">Valitse **Rooli**-kentästä **Ryhmän jäsen**.</span><span class="sxs-lookup"><span data-stu-id="0424d-144">In the **Role** field, select **Team member**.</span></span>
4. <span data-ttu-id="0424d-145">Valitse **Varaa kalenterista**.</span><span class="sxs-lookup"><span data-stu-id="0424d-145">Select **Book from calendar**.</span></span>
5. <span data-ttu-id="0424d-146">Valitse **Resurssin saatavuus** -sivulta **Näyttöasetukset**.</span><span class="sxs-lookup"><span data-stu-id="0424d-146">On the **Resource availability** page, select **View settings**.</span></span>
6. <span data-ttu-id="0424d-147">Syötä **Muuta näyttöasetuksia** -sivulle seuraavat arvot:</span><span class="sxs-lookup"><span data-stu-id="0424d-147">On the **Adjust view settings** page, enter the following values:</span></span>

    - <span data-ttu-id="0424d-148">**Päivämääräalueen muoto:** Päivä</span><span class="sxs-lookup"><span data-stu-id="0424d-148">**Format for date range view:** Day</span></span>
    - <span data-ttu-id="0424d-149">**Näytä saatavuuskuvaukset:** Kyllä</span><span class="sxs-lookup"><span data-stu-id="0424d-149">**Display availability descriptions:** Yes</span></span>
    - <span data-ttu-id="0424d-150">**Näytä jäljellä oleva kapasiteetti:** Kyllä</span><span class="sxs-lookup"><span data-stu-id="0424d-150">**Display remaining capacity:** Yes</span></span>

7. <span data-ttu-id="0424d-151">Valitse resurssiluettelosta haluamasi resurssi.</span><span class="sxs-lookup"><span data-stu-id="0424d-151">In the list of resources, select a resource.</span></span>
8. <span data-ttu-id="0424d-152">Valitse **Kiinteä varaus** ja **Koko kapasiteetti**.</span><span class="sxs-lookup"><span data-stu-id="0424d-152">Select **Hard book** and **Full capacity**.</span></span>

## <a name="assign-a-resource-to-a-default-role"></a><span data-ttu-id="0424d-153">Resurssin määrittäminen oletusrooliin</span><span class="sxs-lookup"><span data-stu-id="0424d-153">Assign a resource to a default role</span></span>

<span data-ttu-id="0424d-154">Voit auttaa projekti- tai resurssipäälliköitä porautumalla alemmas resursseihin, jotka voidaan varata projektiin.</span><span class="sxs-lookup"><span data-stu-id="0424d-154">To help project or resource managers can drill down further on the resources that can be reserved for a project.</span></span> <span data-ttu-id="0424d-155">Voit liittää oletusroolin aiemmin luotuun tai vasta hankittuun resurssiin.</span><span class="sxs-lookup"><span data-stu-id="0424d-155">You can associate a default role with an existing resource or a newly acquired resource.</span></span> <span data-ttu-id="0424d-156">Esimerkiksi kun Daniel palkattiin, hänellä oli yritysanalyytikon rooliin tarvittava kokemus ja osaamisalueet.</span><span class="sxs-lookup"><span data-stu-id="0424d-156">For example, when Daniel was hired, he had the experience and skills to fill the Business analyst role.</span></span> <span data-ttu-id="0424d-157">Resurssipäällikkö määritti tämän roolin Danielin oletusrooliksi.</span><span class="sxs-lookup"><span data-stu-id="0424d-157">The resource manager assigned this role as Daniel's default role.</span></span> <span data-ttu-id="0424d-158">Resurssipäällikkö lisäsi Danielin toisin sanoen niiden yritysanalyytikkojen pooliin, jotka ovat käytettävissä projekteissa.</span><span class="sxs-lookup"><span data-stu-id="0424d-158">Therefore, the resource manager added Daniel to a pool of business analysts who are available to work on projects.</span></span>

<span data-ttu-id="0424d-159">Resurssin varaamisen yhteydessä projektipäälliköt voivat suodattaa roolin resurssit, jotka ovat käytettävissä projektitöihin.</span><span class="sxs-lookup"><span data-stu-id="0424d-159">During resource reservation, project managers can filter the role resources that are available to work on projects.</span></span> <span data-ttu-id="0424d-160">Päälliköt voivat käyttää näitä tietoja yhtenä ehtona analysoidessaan päätöksiä useiden ehtojen perusteella resurssien täyttämisen yhteydessä.</span><span class="sxs-lookup"><span data-stu-id="0424d-160">They can use this information as one criterion when they perform multi-criteria decision analysis during resource fulfillment.</span></span> <span data-ttu-id="0424d-161">He voivat lisätä suodattimeen muitakin resurssin ominaisuuksia ja hakea niiden avulla resursseja, joilla on projektissa tarvittavat osaamisalueet, koulutus ja kokemus.</span><span class="sxs-lookup"><span data-stu-id="0424d-161">They can also add other resource characteristics to the filter to search for resources that have specific skills, education, and experience for a given project.</span></span>

<span data-ttu-id="0424d-162">**Skenaario:** Hyväksytty projekti on alkanut, ja vastaavan projektipäällikön rooli on varattu suunniteltuna resurssina projektin suunnitteluvaiheessa.</span><span class="sxs-lookup"><span data-stu-id="0424d-162">**Scenario:** An approved project has started, and the Senior project manager role was reserved as a planned resource during the project planning stage.</span></span> <span data-ttu-id="0424d-163">Resurssipäällikön on nyt hankittava rooliin sopiva resurssi.</span><span class="sxs-lookup"><span data-stu-id="0424d-163">The resource manager has now acquired a resource to fulfill the Senior project manager role.</span></span>

1. <span data-ttu-id="0424d-164">Valitse **Resurssiluettelo**-sivulta **Daniel Goldschmidt**.</span><span class="sxs-lookup"><span data-stu-id="0424d-164">On the **Resources list** page, select **Daniel Goldschmidt**.</span></span>
2. <span data-ttu-id="0424d-165">Valitse **Resurssin rooli** -sivulla **Uusi** ja anna seuraavat arvot:</span><span class="sxs-lookup"><span data-stu-id="0424d-165">On the **Resource role** page, select **New**, and enter the following values:</span></span>

    - <span data-ttu-id="0424d-166">**Voimassa:** Anna nykyinen päivämäärä.</span><span class="sxs-lookup"><span data-stu-id="0424d-166">**Effective:** Enter the current date.</span></span>
    - <span data-ttu-id="0424d-167">**Päättyminen:** anna arvoksi **Ei koskaan**.</span><span class="sxs-lookup"><span data-stu-id="0424d-167">**Expiration:** Enter **Never**.</span></span>
    - <span data-ttu-id="0424d-168">**Rooli:** anna arvoksi **Vastaava projektipäällikkö**.</span><span class="sxs-lookup"><span data-stu-id="0424d-168">**Role:** Enter **Senior Project Manager**.</span></span>

3. <span data-ttu-id="0424d-169">Valitse **Tallenna** ja sulje sitten sivu.</span><span class="sxs-lookup"><span data-stu-id="0424d-169">Select **Save**, and then close the page.</span></span>
4. <span data-ttu-id="0424d-170">Lisää **Osaamistiedot**-välilehdessä **ProjectMgmt**-osaamisalue ja **PMP**-todistus.</span><span class="sxs-lookup"><span data-stu-id="0424d-170">On the **Competencies** tab, add the **ProjectMgmt** skill and the **PMP** certificate.</span></span>
