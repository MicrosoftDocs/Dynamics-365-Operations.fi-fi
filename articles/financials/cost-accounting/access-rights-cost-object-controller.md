---
title: "Kustannusobjektin vastuuhenkilöiden käyttöoikeuksien määrittäminen"
description: "Tässä ohjeaiheessa on tietoja kustannusobjektin vastuuhenkilöiden käyttöoikeuksista."
author: AndersGirke
manager: AnnBe
ms.date: 06/24/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CAMCostControlWorkspace, CAMParameters
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations, Core
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: YuyuScheller
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 2ba38ddc5c717df29462e4316dc5045d0eef8c1a
ms.contentlocale: fi-fi
ms.lasthandoff: 11/03/2017

---

# <a name="access-rights-of-a-cost-object-controller"></a><span data-ttu-id="e6ca1-103">Kustannusobjektin vastuuhenkilön käyttöoikeudet</span><span class="sxs-lookup"><span data-stu-id="e6ca1-103">Access rights of a cost object controller</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="e6ca1-104">Esimiehet voivat tarkastella **kustannusseurannan** työtilassa keskitetysti kustannusobjektiensa suoriutumista.</span><span class="sxs-lookup"><span data-stu-id="e6ca1-104">The **Cost control** workspace is a central point where managers can view the performance of their cost objects.</span></span> <span data-ttu-id="e6ca1-105">Esimiehet voivat käyttää tässä tilassa kustannuslaskentatietoja, vaikka he eivät ole kustannuslaskijoita.</span><span class="sxs-lookup"><span data-stu-id="e6ca1-105">This workspace lets managers consume Cost accounting data even though they aren't cost accountants.</span></span> <span data-ttu-id="e6ca1-106">Tietoturvasyistä esimiesten pitäisi saada tarkastella vain niitä kustannuslaskentatietoja, jotka liittyvät heidän vastuullaan olevien kustannusobjekteihin.</span><span class="sxs-lookup"><span data-stu-id="e6ca1-106">For security reasons, managers should be allowed to see only the Cost accounting data that is related to the specific cost objects that they are responsible for.</span></span>

<span data-ttu-id="e6ca1-107">Kustannuslaskennassa on neljä yksilöivää roolia.</span><span class="sxs-lookup"><span data-stu-id="e6ca1-107">There are four unique roles in Cost accounting.</span></span>

| <span data-ttu-id="e6ca1-108">Roolin nimi</span><span class="sxs-lookup"><span data-stu-id="e6ca1-108">Role name</span></span>               | <span data-ttu-id="e6ca1-109">Käyttöoikeus</span><span class="sxs-lookup"><span data-stu-id="e6ca1-109">License</span></span>      |
|-------------------------|--------------|
| <span data-ttu-id="e6ca1-110">Kustannuslaskennan hallinta</span><span class="sxs-lookup"><span data-stu-id="e6ca1-110">Cost accounting manager</span></span> | <span data-ttu-id="e6ca1-111">Tehtävä</span><span class="sxs-lookup"><span data-stu-id="e6ca1-111">Activity</span></span>     |
| <span data-ttu-id="e6ca1-112">Kustannuslaskija</span><span class="sxs-lookup"><span data-stu-id="e6ca1-112">Cost accountant</span></span>         | <span data-ttu-id="e6ca1-113">Operations</span><span class="sxs-lookup"><span data-stu-id="e6ca1-113">Operations</span></span>   |
| <span data-ttu-id="e6ca1-114">Kustannuslaskijan apulainen</span><span class="sxs-lookup"><span data-stu-id="e6ca1-114">Cost accountant clerk</span></span>   | <span data-ttu-id="e6ca1-115">Operations</span><span class="sxs-lookup"><span data-stu-id="e6ca1-115">Operations</span></span>   |
| <span data-ttu-id="e6ca1-116">Kustannusobjektin vastuuhenkilö</span><span class="sxs-lookup"><span data-stu-id="e6ca1-116">Cost object controller</span></span>  | <span data-ttu-id="e6ca1-117">Tiimin jäsenet</span><span class="sxs-lookup"><span data-stu-id="e6ca1-117">Team members</span></span> |

<span data-ttu-id="e6ca1-118">Tässä ohjeaiheessa kerrotaan, miten **kustannusobjektin vastuuhenkilön** määritetään esimiehelle.</span><span class="sxs-lookup"><span data-stu-id="e6ca1-118">This topic explains how to assign the **Cost object controller** role to a manager.</span></span>

<span data-ttu-id="e6ca1-119">Kun **kustannusobjektin vastuuhenkilön** rooli on määritetty esimiehelle, tämä voi suorittaa seuraavat tehtävät:</span><span class="sxs-lookup"><span data-stu-id="e6ca1-119">When the **Cost object controller** role is assigned to a manager, the manager can perform the following tasks:</span></span>

- <span data-ttu-id="e6ca1-120">**kustannusseurannan** työtilan käyttö (asiakasohjelmassa)</span><span class="sxs-lookup"><span data-stu-id="e6ca1-120">Access the **Cost control** workspace (in the client).</span></span>

    - <span data-ttu-id="e6ca1-121">porautumista tukevien sivujen poraus- ja tarkasteluoikeudet</span><span class="sxs-lookup"><span data-stu-id="e6ca1-121">Drill through and have view access to the pages that support the drill-through experience.</span></span>

- <span data-ttu-id="e6ca1-122">**kustannusseurannan** työtilan käyttö (mobiilisovelluksessa)</span><span class="sxs-lookup"><span data-stu-id="e6ca1-122">Access the **Cost control** workspace (in the mobile application).</span></span>

> [!NOTE]
> <span data-ttu-id="e6ca1-123">**kustannusobjektin vastuuhenkilön** roolilla ei voi hallita sitä, mitä kustannusobjekteja käyttäjä voi käyttää ja minkä tietoja hän voi tarkastella.</span><span class="sxs-lookup"><span data-stu-id="e6ca1-123">The **Cost object controller** role doesn't control which cost objects the user can access and view data for.</span></span> <span data-ttu-id="e6ca1-124">Rivitason suojaus perustuu dimensio- ja käyttöoikeusluettelohierarkioihin.</span><span class="sxs-lookup"><span data-stu-id="e6ca1-124">Row-level security is provided via dimension hierarchies and the Access list hierarchy.</span></span>

## <a name="grant-access-rights"></a><span data-ttu-id="e6ca1-125">Käyttöoikeuksien myöntäminen</span><span class="sxs-lookup"><span data-stu-id="e6ca1-125">Grant access rights</span></span>
<span data-ttu-id="e6ca1-126">Seuraavassa on esimerkki dimensiohierarkiasta.</span><span class="sxs-lookup"><span data-stu-id="e6ca1-126">The following example shows what a dimension hierarchy can look like.</span></span>

<span data-ttu-id="e6ca1-127">**Dimension hierarkiatiedot**</span><span class="sxs-lookup"><span data-stu-id="e6ca1-127">**Dimension hierarchy details**</span></span>

| <span data-ttu-id="e6ca1-128">Dimensiohierarkian nimi</span><span class="sxs-lookup"><span data-stu-id="e6ca1-128">Dimension hierarchy name</span></span> | <span data-ttu-id="e6ca1-129">Dimensio</span><span class="sxs-lookup"><span data-stu-id="e6ca1-129">Dimension</span></span>    | <span data-ttu-id="e6ca1-130">Dimensiohierarkiatyypin nimi</span><span class="sxs-lookup"><span data-stu-id="e6ca1-130">Dimension hierarchy type name</span></span>      | <span data-ttu-id="e6ca1-131">Käyttöoikeusluettelohierarkia</span><span class="sxs-lookup"><span data-stu-id="e6ca1-131">Access list hierarchy</span></span> |
|--------------------------|--------------|------------------------------------|-----------------------|
| <span data-ttu-id="e6ca1-132">Organisaatio</span><span class="sxs-lookup"><span data-stu-id="e6ca1-132">Organization</span></span>             | <span data-ttu-id="e6ca1-133">Kustannuspaikat</span><span class="sxs-lookup"><span data-stu-id="e6ca1-133">Cost centers</span></span> | <span data-ttu-id="e6ca1-134">Dimension luokitteluhierarkia</span><span class="sxs-lookup"><span data-stu-id="e6ca1-134">Dimension classification hierarchy</span></span> | <span data-ttu-id="e6ca1-135">**Kyllä**</span><span class="sxs-lookup"><span data-stu-id="e6ca1-135">**Yes**</span></span>               |

<span data-ttu-id="e6ca1-136">Voit lisätä kuhunkin solmuun käyttäjätunnuksia hierarkian suunnittelutoiminnon **Käyttäjät**-pikavälilehdessä.</span><span class="sxs-lookup"><span data-stu-id="e6ca1-136">You can use the **Users** FastTab in the hierarchy designer to insert one or more user IDs on each node.</span></span>

|                                   | <span data-ttu-id="e6ca1-137">Käyttäjät</span><span class="sxs-lookup"><span data-stu-id="e6ca1-137">Users</span></span>            | <span data-ttu-id="e6ca1-138">Dimension jäsenalueet</span><span class="sxs-lookup"><span data-stu-id="e6ca1-138">Dimension member ranges</span></span>   |                         |
|-----------------------------------|------------------|---------------------------|-------------------------|
| <span data-ttu-id="e6ca1-139">**Solmukohdat**</span><span class="sxs-lookup"><span data-stu-id="e6ca1-139">**Nodes**</span></span>                         | <span data-ttu-id="e6ca1-140">**Käyttäjätunnus**</span><span class="sxs-lookup"><span data-stu-id="e6ca1-140">**User ID**</span></span>      | <span data-ttu-id="e6ca1-141">**Lähtödimension jäsen**</span><span class="sxs-lookup"><span data-stu-id="e6ca1-141">**From dimension member**</span></span> | <span data-ttu-id="e6ca1-142">**Kohdedimension jäsen**</span><span class="sxs-lookup"><span data-stu-id="e6ca1-142">**To dimension member**</span></span> |
| <span data-ttu-id="e6ca1-143">Organisaatio</span><span class="sxs-lookup"><span data-stu-id="e6ca1-143">Organization</span></span>                      | <span data-ttu-id="e6ca1-144">Benjamin, Claire</span><span class="sxs-lookup"><span data-stu-id="e6ca1-144">Benjamin, Claire</span></span> |                           |                         |
| <span data-ttu-id="e6ca1-145">&nbsp;&nbsp;Hallinto</span><span class="sxs-lookup"><span data-stu-id="e6ca1-145">&nbsp;&nbsp;Admin</span></span>                 | <span data-ttu-id="e6ca1-146">Huhtikuu</span><span class="sxs-lookup"><span data-stu-id="e6ca1-146">April</span></span>            |                           |                         |
| <span data-ttu-id="e6ca1-147">&nbsp;&nbsp;&nbsp;&nbsp;Myyntitiedot</span><span class="sxs-lookup"><span data-stu-id="e6ca1-147">&nbsp;&nbsp;&nbsp;&nbsp;Finance</span></span>   | <span data-ttu-id="e6ca1-148">Alicia</span><span class="sxs-lookup"><span data-stu-id="e6ca1-148">Alicia</span></span>           | <span data-ttu-id="e6ca1-149">CC002</span><span class="sxs-lookup"><span data-stu-id="e6ca1-149">CC002</span></span>                     | <span data-ttu-id="e6ca1-150">CC003</span><span class="sxs-lookup"><span data-stu-id="e6ca1-150">CC003</span></span>                   |
|                                   |                  | <span data-ttu-id="e6ca1-151">CC007</span><span class="sxs-lookup"><span data-stu-id="e6ca1-151">CC007</span></span>                     | <span data-ttu-id="e6ca1-152">CC007</span><span class="sxs-lookup"><span data-stu-id="e6ca1-152">CC007</span></span>                   |
| <span data-ttu-id="e6ca1-153">&nbsp;&nbsp;&nbsp;&nbsp;Henkilöstöhallinto</span><span class="sxs-lookup"><span data-stu-id="e6ca1-153">&nbsp;&nbsp;&nbsp;&nbsp;HR</span></span>        | <span data-ttu-id="e6ca1-154">Arnie</span><span class="sxs-lookup"><span data-stu-id="e6ca1-154">Arnie</span></span>            | <span data-ttu-id="e6ca1-155">CC001</span><span class="sxs-lookup"><span data-stu-id="e6ca1-155">CC001</span></span>                     | <span data-ttu-id="e6ca1-156">CC001</span><span class="sxs-lookup"><span data-stu-id="e6ca1-156">CC001</span></span>                   |
| <span data-ttu-id="e6ca1-157">&nbsp;&nbsp;Tuotanto</span><span class="sxs-lookup"><span data-stu-id="e6ca1-157">&nbsp;&nbsp;Production</span></span>            | <span data-ttu-id="e6ca1-158">David</span><span class="sxs-lookup"><span data-stu-id="e6ca1-158">David</span></span>            |                           |                         |
| <span data-ttu-id="e6ca1-159">&nbsp;&nbsp;&nbsp;&nbsp;Pakkaus</span><span class="sxs-lookup"><span data-stu-id="e6ca1-159">&nbsp;&nbsp;&nbsp;&nbsp;Packaging</span></span> | <span data-ttu-id="e6ca1-160">Ellen</span><span class="sxs-lookup"><span data-stu-id="e6ca1-160">Ellen</span></span>            | <span data-ttu-id="e6ca1-161">CC005</span><span class="sxs-lookup"><span data-stu-id="e6ca1-161">CC005</span></span>                     | <span data-ttu-id="e6ca1-162">CC005</span><span class="sxs-lookup"><span data-stu-id="e6ca1-162">CC005</span></span>                   |
| <span data-ttu-id="e6ca1-163">&nbsp;&nbsp;&nbsp;&nbsp;Kokoonpano</span><span class="sxs-lookup"><span data-stu-id="e6ca1-163">&nbsp;&nbsp;&nbsp;&nbsp;Assembly</span></span>  | <span data-ttu-id="e6ca1-164">Chris</span><span class="sxs-lookup"><span data-stu-id="e6ca1-164">Chris</span></span>            | <span data-ttu-id="e6ca1-165">CC006</span><span class="sxs-lookup"><span data-stu-id="e6ca1-165">CC006</span></span>                     | <span data-ttu-id="e6ca1-166">CC006</span><span class="sxs-lookup"><span data-stu-id="e6ca1-166">CC006</span></span>                   |

> [!NOTE]
> <span data-ttu-id="e6ca1-167">Kustannuslaskijat on määritettävä hierarkian ylimmälle tasolle, jotta he näkevät kaikki kustannuslaskennan merkinnät.</span><span class="sxs-lookup"><span data-stu-id="e6ca1-167">Cost accountants should be assigned to the top level of the hierarchy, so that they can see all entries in Cost accounting.</span></span>

<span data-ttu-id="e6ca1-168">Ennen käyttöoikeushierarkian ja sen suojausasetusten käyttöönottoa **Ota käyttöön katseluoikeus kustannusobjektin dimension jäsenille** -asetukseksi on valittava **Kyllä** **Kustannuslaskentaparametrit**-sivun **Yleiset**-välilehdessä (**Kustannuslaskenta** > **Asetukset** > **Parametrit**).</span><span class="sxs-lookup"><span data-stu-id="e6ca1-168">Before the Access list hierarchy and its security settings can be applied, the **Enable view access for cost object dimension members** option must be set to **Yes** on the **General** tab of the **Cost accounting parameters** page (**Cost accounting** > **Setup** > **Parameters**).</span></span>

<span data-ttu-id="e6ca1-169">Käyttöoikeusluettelohierarkian asetuksilla hallitaan seuraavilla alueilla näkyviä tietoja:</span><span class="sxs-lookup"><span data-stu-id="e6ca1-169">The settings for the Access list hierarchy are used to control the data that is shown in following areas:</span></span>

- <span data-ttu-id="e6ca1-170">**Kustannusseurannan** työtila (asiakasohjelmassa):</span><span class="sxs-lookup"><span data-stu-id="e6ca1-170">**Cost control** workspace (in the client):</span></span>

    - <span data-ttu-id="e6ca1-171">Porautumiseen käytettävien sivujen tiedot</span><span class="sxs-lookup"><span data-stu-id="e6ca1-171">Data on the pages that are used for drill-through</span></span>

- <span data-ttu-id="e6ca1-172">**Kustannusseurannan** työtila (mobiilisovelluksessa):</span><span class="sxs-lookup"><span data-stu-id="e6ca1-172">**Cost control** workspace (in the mobile application):</span></span>

    - <span data-ttu-id="e6ca1-173">Korttien saldot</span><span class="sxs-lookup"><span data-stu-id="e6ca1-173">Balances in cards</span></span>

- <span data-ttu-id="e6ca1-174">Microsoft Power BI:</span><span class="sxs-lookup"><span data-stu-id="e6ca1-174">Microsoft Power BI:</span></span>

    - <span data-ttu-id="e6ca1-175">Power BI -visualisoinneissa näytettävät tiedot</span><span class="sxs-lookup"><span data-stu-id="e6ca1-175">Data that is shown in Power BI visualizations</span></span>
    - <span data-ttu-id="e6ca1-176">Microsoft Dynamics 365 for Finance and Operations, Enterprise Editionin asiakasohjelmaan upotetut tietojen Power BI -visualisoinnit</span><span class="sxs-lookup"><span data-stu-id="e6ca1-176">Data Power BI visualizations that are embedded in the Microsoft Dynamics 365 for Finance and Operations, Enterprise edition, client</span></span>

> [!IMPORTANT]
> - <span data-ttu-id="e6ca1-177">Käyttöoikeusluettelohierarkialla ei ole vaikutusta Power BI -tietoihin, ennen kuin käyttöoikeusluettelohierarkia ja Power BI:n rivitason suojaus ovat muodostaneet parin.</span><span class="sxs-lookup"><span data-stu-id="e6ca1-177">Before the Access list hierarchy can affect data in Power BI, the Access list hierarchy and row-level security in Power BI must be paired.</span></span> <span data-ttu-id="e6ca1-178">Lisätietoja on ohjeaiheessa [Kustannuslaskennan sisältöpaketin suojauksen määrittäminen](../../dev-itpro/analytics/setup-security-cost-accounting-content-pack.md).</span><span class="sxs-lookup"><span data-stu-id="e6ca1-178">For more information, see [Set up security for Cost accounting content pack](../../dev-itpro/analytics/setup-security-cost-accounting-content-pack.md).</span></span>
> - <span data-ttu-id="e6ca1-179">Tässä ohjeaiheessa käsitellään edellytykset, joita ilman **kustannusseurannan** työtilaa ei voi käyttää.</span><span class="sxs-lookup"><span data-stu-id="e6ca1-179">This topic shows the prerequisites that must be in place before you can use the **Cost control** workspace.</span></span>

<span data-ttu-id="e6ca1-180">Lisätietoja</span><span class="sxs-lookup"><span data-stu-id="e6ca1-180">See also</span></span>

- [<span data-ttu-id="e6ca1-181">Kustannusseurannan työtila</span><span class="sxs-lookup"><span data-stu-id="e6ca1-181">Cost control workspace</span></span>](cost-control-workspace.md)
- [<span data-ttu-id="e6ca1-182">Dimensiohierarkia</span><span class="sxs-lookup"><span data-stu-id="e6ca1-182">Dimension hierarchy</span></span>](dimension-hierarchy.md)
- [<span data-ttu-id="e6ca1-183">Kustannuslaskennan sisältöpaketin määrittäminen</span><span class="sxs-lookup"><span data-stu-id="e6ca1-183">Set up security for Cost accounting content pack</span></span>](../../dev-itpro/analytics/setup-security-cost-accounting-content-pack.md)

