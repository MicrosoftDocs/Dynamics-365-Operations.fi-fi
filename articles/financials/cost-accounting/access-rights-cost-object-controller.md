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
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: a0739304723d19b910388893d08e8c36a1f49d13
ms.openlocfilehash: 6403aabb6b029807b42ab1ccb11756dcb0dda5dc
ms.contentlocale: fi-fi
ms.lasthandoff: 03/26/2018

---

# <a name="access-rights-of-a-cost-object-controller"></a><span data-ttu-id="e3d19-103">Kustannusobjektin vastuuhenkilön käyttöoikeudet</span><span class="sxs-lookup"><span data-stu-id="e3d19-103">Access rights of a cost object controller</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="e3d19-104">Esimiehet voivat tarkastella **kustannusseurannan** työtilassa keskitetysti kustannusobjektiensa suoriutumista.</span><span class="sxs-lookup"><span data-stu-id="e3d19-104">The **Cost control** workspace is a central point where managers can view the performance of their cost objects.</span></span> <span data-ttu-id="e3d19-105">Esimiehet voivat käyttää tässä tilassa kustannuslaskentatietoja, vaikka he eivät ole kustannuslaskijoita.</span><span class="sxs-lookup"><span data-stu-id="e3d19-105">This workspace lets managers consume Cost accounting data even though they aren't cost accountants.</span></span> <span data-ttu-id="e3d19-106">Tietoturvasyistä esimiesten pitäisi saada tarkastella vain niitä kustannuslaskentatietoja, jotka liittyvät heidän vastuullaan olevien kustannusobjekteihin.</span><span class="sxs-lookup"><span data-stu-id="e3d19-106">For security reasons, managers should be allowed to see only the Cost accounting data that is related to the specific cost objects that they are responsible for.</span></span>

<span data-ttu-id="e3d19-107">Kustannuslaskennassa on neljä yksilöivää roolia.</span><span class="sxs-lookup"><span data-stu-id="e3d19-107">There are four unique roles in Cost accounting.</span></span>

| <span data-ttu-id="e3d19-108">Roolin nimi</span><span class="sxs-lookup"><span data-stu-id="e3d19-108">Role name</span></span>               | <span data-ttu-id="e3d19-109">Käyttöoikeus</span><span class="sxs-lookup"><span data-stu-id="e3d19-109">License</span></span>      |
|-------------------------|--------------|
| <span data-ttu-id="e3d19-110">Kustannuslaskennan hallinta</span><span class="sxs-lookup"><span data-stu-id="e3d19-110">Cost accounting manager</span></span> | <span data-ttu-id="e3d19-111">Tehtävä</span><span class="sxs-lookup"><span data-stu-id="e3d19-111">Activity</span></span>     |
| <span data-ttu-id="e3d19-112">Kustannuslaskija</span><span class="sxs-lookup"><span data-stu-id="e3d19-112">Cost accountant</span></span>         | <span data-ttu-id="e3d19-113">Operations</span><span class="sxs-lookup"><span data-stu-id="e3d19-113">Operations</span></span>   |
| <span data-ttu-id="e3d19-114">Kustannuslaskijan apulainen</span><span class="sxs-lookup"><span data-stu-id="e3d19-114">Cost accountant clerk</span></span>   | <span data-ttu-id="e3d19-115">Operations</span><span class="sxs-lookup"><span data-stu-id="e3d19-115">Operations</span></span>   |
| <span data-ttu-id="e3d19-116">Kustannusobjektin vastuuhenkilö</span><span class="sxs-lookup"><span data-stu-id="e3d19-116">Cost object controller</span></span>  | <span data-ttu-id="e3d19-117">Tiimin jäsenet</span><span class="sxs-lookup"><span data-stu-id="e3d19-117">Team members</span></span> |

<span data-ttu-id="e3d19-118">Tässä ohjeaiheessa kerrotaan, miten **kustannusobjektin vastuuhenkilön** määritetään esimiehelle.</span><span class="sxs-lookup"><span data-stu-id="e3d19-118">This topic explains how to assign the **Cost object controller** role to a manager.</span></span>

<span data-ttu-id="e3d19-119">Kun **kustannusobjektin vastuuhenkilön** rooli on määritetty esimiehelle, tämä voi suorittaa seuraavat tehtävät:</span><span class="sxs-lookup"><span data-stu-id="e3d19-119">When the **Cost object controller** role is assigned to a manager, the manager can perform the following tasks:</span></span>

- <span data-ttu-id="e3d19-120">**kustannusseurannan** työtilan käyttö (asiakasohjelmassa)</span><span class="sxs-lookup"><span data-stu-id="e3d19-120">Access the **Cost control** workspace (in the client).</span></span>

    - <span data-ttu-id="e3d19-121">porautumista tukevien sivujen poraus- ja tarkasteluoikeudet</span><span class="sxs-lookup"><span data-stu-id="e3d19-121">Drill through and have view access to the pages that support the drill-through experience.</span></span>

- <span data-ttu-id="e3d19-122">**kustannusseurannan** työtilan käyttö (mobiilisovelluksessa)</span><span class="sxs-lookup"><span data-stu-id="e3d19-122">Access the **Cost control** workspace (in the mobile application).</span></span>

> [!NOTE]
> <span data-ttu-id="e3d19-123">**kustannusobjektin vastuuhenkilön** roolilla ei voi hallita sitä, mitä kustannusobjekteja käyttäjä voi käyttää ja minkä tietoja hän voi tarkastella.</span><span class="sxs-lookup"><span data-stu-id="e3d19-123">The **Cost object controller** role doesn't control which cost objects the user can access and view data for.</span></span> <span data-ttu-id="e3d19-124">Rivitason suojaus perustuu dimensio- ja käyttöoikeusluettelohierarkioihin.</span><span class="sxs-lookup"><span data-stu-id="e3d19-124">Row-level security is provided via dimension hierarchies and the Access list hierarchy.</span></span>

## <a name="grant-access-rights"></a><span data-ttu-id="e3d19-125">Käyttöoikeuksien myöntäminen</span><span class="sxs-lookup"><span data-stu-id="e3d19-125">Grant access rights</span></span>
<span data-ttu-id="e3d19-126">Seuraavassa on esimerkki dimensiohierarkiasta.</span><span class="sxs-lookup"><span data-stu-id="e3d19-126">The following example shows what a dimension hierarchy can look like.</span></span>

<span data-ttu-id="e3d19-127">**Dimension hierarkiatiedot**</span><span class="sxs-lookup"><span data-stu-id="e3d19-127">**Dimension hierarchy details**</span></span>

| <span data-ttu-id="e3d19-128">Dimensiohierarkian nimi</span><span class="sxs-lookup"><span data-stu-id="e3d19-128">Dimension hierarchy name</span></span> | <span data-ttu-id="e3d19-129">Dimensio</span><span class="sxs-lookup"><span data-stu-id="e3d19-129">Dimension</span></span>    | <span data-ttu-id="e3d19-130">Dimensiohierarkiatyypin nimi</span><span class="sxs-lookup"><span data-stu-id="e3d19-130">Dimension hierarchy type name</span></span>      | <span data-ttu-id="e3d19-131">Käyttöoikeusluettelohierarkia</span><span class="sxs-lookup"><span data-stu-id="e3d19-131">Access list hierarchy</span></span> |
|--------------------------|--------------|------------------------------------|-----------------------|
| <span data-ttu-id="e3d19-132">Organisaatio</span><span class="sxs-lookup"><span data-stu-id="e3d19-132">Organization</span></span>             | <span data-ttu-id="e3d19-133">Kustannuspaikat</span><span class="sxs-lookup"><span data-stu-id="e3d19-133">Cost centers</span></span> | <span data-ttu-id="e3d19-134">Dimension luokitteluhierarkia</span><span class="sxs-lookup"><span data-stu-id="e3d19-134">Dimension classification hierarchy</span></span> | <span data-ttu-id="e3d19-135">**Kyllä**</span><span class="sxs-lookup"><span data-stu-id="e3d19-135">**Yes**</span></span>               |

<span data-ttu-id="e3d19-136">Voit lisätä kuhunkin solmuun käyttäjätunnuksia hierarkian suunnittelutoiminnon **Käyttäjät**-pikavälilehdessä.</span><span class="sxs-lookup"><span data-stu-id="e3d19-136">You can use the **Users** FastTab in the hierarchy designer to insert one or more user IDs on each node.</span></span>

|                                   | <span data-ttu-id="e3d19-137">Käyttäjät</span><span class="sxs-lookup"><span data-stu-id="e3d19-137">Users</span></span>            | <span data-ttu-id="e3d19-138">Dimension jäsenalueet</span><span class="sxs-lookup"><span data-stu-id="e3d19-138">Dimension member ranges</span></span>   |                         |
|-----------------------------------|------------------|---------------------------|-------------------------|
| <span data-ttu-id="e3d19-139">**Solmukohdat**</span><span class="sxs-lookup"><span data-stu-id="e3d19-139">**Nodes**</span></span>                         | <span data-ttu-id="e3d19-140">**Käyttäjätunnus**</span><span class="sxs-lookup"><span data-stu-id="e3d19-140">**User ID**</span></span>      | <span data-ttu-id="e3d19-141">**Lähtödimension jäsen**</span><span class="sxs-lookup"><span data-stu-id="e3d19-141">**From dimension member**</span></span> | <span data-ttu-id="e3d19-142">**Kohdedimension jäsen**</span><span class="sxs-lookup"><span data-stu-id="e3d19-142">**To dimension member**</span></span> |
| <span data-ttu-id="e3d19-143">Organisaatio</span><span class="sxs-lookup"><span data-stu-id="e3d19-143">Organization</span></span>                      | <span data-ttu-id="e3d19-144">Benjamin, Claire</span><span class="sxs-lookup"><span data-stu-id="e3d19-144">Benjamin, Claire</span></span> |                           |                         |
| <span data-ttu-id="e3d19-145">&nbsp;&nbsp;Hallinto</span><span class="sxs-lookup"><span data-stu-id="e3d19-145">&nbsp;&nbsp;Admin</span></span>                 | <span data-ttu-id="e3d19-146">Huhtikuu</span><span class="sxs-lookup"><span data-stu-id="e3d19-146">April</span></span>            |                           |                         |
| <span data-ttu-id="e3d19-147">&nbsp;&nbsp;&nbsp;&nbsp;Myyntitiedot</span><span class="sxs-lookup"><span data-stu-id="e3d19-147">&nbsp;&nbsp;&nbsp;&nbsp;Finance</span></span>   | <span data-ttu-id="e3d19-148">Alicia</span><span class="sxs-lookup"><span data-stu-id="e3d19-148">Alicia</span></span>           | <span data-ttu-id="e3d19-149">CC002</span><span class="sxs-lookup"><span data-stu-id="e3d19-149">CC002</span></span>                     | <span data-ttu-id="e3d19-150">CC003</span><span class="sxs-lookup"><span data-stu-id="e3d19-150">CC003</span></span>                   |
|                                   |                  | <span data-ttu-id="e3d19-151">CC007</span><span class="sxs-lookup"><span data-stu-id="e3d19-151">CC007</span></span>                     | <span data-ttu-id="e3d19-152">CC007</span><span class="sxs-lookup"><span data-stu-id="e3d19-152">CC007</span></span>                   |
| <span data-ttu-id="e3d19-153">&nbsp;&nbsp;&nbsp;&nbsp;Henkilöstöhallinto</span><span class="sxs-lookup"><span data-stu-id="e3d19-153">&nbsp;&nbsp;&nbsp;&nbsp;HR</span></span>        | <span data-ttu-id="e3d19-154">Arnie</span><span class="sxs-lookup"><span data-stu-id="e3d19-154">Arnie</span></span>            | <span data-ttu-id="e3d19-155">CC001</span><span class="sxs-lookup"><span data-stu-id="e3d19-155">CC001</span></span>                     | <span data-ttu-id="e3d19-156">CC001</span><span class="sxs-lookup"><span data-stu-id="e3d19-156">CC001</span></span>                   |
| <span data-ttu-id="e3d19-157">&nbsp;&nbsp;Tuotanto</span><span class="sxs-lookup"><span data-stu-id="e3d19-157">&nbsp;&nbsp;Production</span></span>            | <span data-ttu-id="e3d19-158">David</span><span class="sxs-lookup"><span data-stu-id="e3d19-158">David</span></span>            |                           |                         |
| <span data-ttu-id="e3d19-159">&nbsp;&nbsp;&nbsp;&nbsp;Pakkaus</span><span class="sxs-lookup"><span data-stu-id="e3d19-159">&nbsp;&nbsp;&nbsp;&nbsp;Packaging</span></span> | <span data-ttu-id="e3d19-160">Ellen</span><span class="sxs-lookup"><span data-stu-id="e3d19-160">Ellen</span></span>            | <span data-ttu-id="e3d19-161">CC005</span><span class="sxs-lookup"><span data-stu-id="e3d19-161">CC005</span></span>                     | <span data-ttu-id="e3d19-162">CC005</span><span class="sxs-lookup"><span data-stu-id="e3d19-162">CC005</span></span>                   |
| <span data-ttu-id="e3d19-163">&nbsp;&nbsp;&nbsp;&nbsp;Kokoonpano</span><span class="sxs-lookup"><span data-stu-id="e3d19-163">&nbsp;&nbsp;&nbsp;&nbsp;Assembly</span></span>  | <span data-ttu-id="e3d19-164">Chris</span><span class="sxs-lookup"><span data-stu-id="e3d19-164">Chris</span></span>            | <span data-ttu-id="e3d19-165">CC006</span><span class="sxs-lookup"><span data-stu-id="e3d19-165">CC006</span></span>                     | <span data-ttu-id="e3d19-166">CC006</span><span class="sxs-lookup"><span data-stu-id="e3d19-166">CC006</span></span>                   |

> [!NOTE]
> <span data-ttu-id="e3d19-167">Kustannuslaskijat on määritettävä hierarkian ylimmälle tasolle, jotta he näkevät kaikki kustannuslaskennan merkinnät.</span><span class="sxs-lookup"><span data-stu-id="e3d19-167">Cost accountants should be assigned to the top level of the hierarchy, so that they can see all entries in Cost accounting.</span></span>

<span data-ttu-id="e3d19-168">Ennen käyttöoikeushierarkian ja sen suojausasetusten käyttöönottoa **Ota käyttöön katseluoikeus kustannusobjektin dimension jäsenille** -asetukseksi on valittava **Kyllä** **Kustannuslaskentaparametrit**-sivun **Yleiset**-välilehdessä (**Kustannuslaskenta** > **Asetukset** > **Parametrit**).</span><span class="sxs-lookup"><span data-stu-id="e3d19-168">Before the Access list hierarchy and its security settings can be applied, the **Enable view access for cost object dimension members** option must be set to **Yes** on the **General** tab of the **Cost accounting parameters** page (**Cost accounting** > **Setup** > **Parameters**).</span></span>

<span data-ttu-id="e3d19-169">Käyttöoikeusluettelohierarkian asetuksilla hallitaan seuraavilla alueilla näkyviä tietoja:</span><span class="sxs-lookup"><span data-stu-id="e3d19-169">The settings for the Access list hierarchy are used to control the data that is shown in following areas:</span></span>

- <span data-ttu-id="e3d19-170">**Kustannusseurannan** työtila (asiakasohjelmassa):</span><span class="sxs-lookup"><span data-stu-id="e3d19-170">**Cost control** workspace (in the client):</span></span>

    - <span data-ttu-id="e3d19-171">Porautumiseen käytettävien sivujen tiedot</span><span class="sxs-lookup"><span data-stu-id="e3d19-171">Data on the pages that are used for drill-through</span></span>

- <span data-ttu-id="e3d19-172">**Kustannusseurannan** työtila (mobiilisovelluksessa):</span><span class="sxs-lookup"><span data-stu-id="e3d19-172">**Cost control** workspace (in the mobile application):</span></span>

    - <span data-ttu-id="e3d19-173">Korttien saldot</span><span class="sxs-lookup"><span data-stu-id="e3d19-173">Balances in cards</span></span>

- <span data-ttu-id="e3d19-174">Microsoft Power BI:</span><span class="sxs-lookup"><span data-stu-id="e3d19-174">Microsoft Power BI:</span></span>

    - <span data-ttu-id="e3d19-175">Power BI -visualisoinneissa näytettävät tiedot</span><span class="sxs-lookup"><span data-stu-id="e3d19-175">Data that is shown in Power BI visualizations</span></span>
    - <span data-ttu-id="e3d19-176">Microsoft Dynamics 365 for Finance and Operations -asiakasohjelmaan upotetut tietojen Power BI -visualisoinnit</span><span class="sxs-lookup"><span data-stu-id="e3d19-176">Data Power BI visualizations that are embedded in the Microsoft Dynamics 365 for Finance and Operations, client</span></span>

> [!IMPORTANT]
> - <span data-ttu-id="e3d19-177">Käyttöoikeusluettelohierarkialla ei ole vaikutusta Power BI -tietoihin, ennen kuin käyttöoikeusluettelohierarkia ja Power BI:n rivitason suojaus ovat muodostaneet parin.</span><span class="sxs-lookup"><span data-stu-id="e3d19-177">Before the Access list hierarchy can affect data in Power BI, the Access list hierarchy and row-level security in Power BI must be paired.</span></span> <span data-ttu-id="e3d19-178">Lisätietoja on ohjeaiheessa [Kustannuslaskennan sisältöpaketin suojauksen määrittäminen](../../dev-itpro/analytics/setup-security-cost-accounting-content-pack.md).</span><span class="sxs-lookup"><span data-stu-id="e3d19-178">For more information, see [Set up security for Cost accounting content pack](../../dev-itpro/analytics/setup-security-cost-accounting-content-pack.md).</span></span>
> - <span data-ttu-id="e3d19-179">Tässä ohjeaiheessa käsitellään edellytykset, joita ilman **kustannusseurannan** työtilaa ei voi käyttää.</span><span class="sxs-lookup"><span data-stu-id="e3d19-179">This topic shows the prerequisites that must be in place before you can use the **Cost control** workspace.</span></span>

<span data-ttu-id="e3d19-180">Lisätietoja</span><span class="sxs-lookup"><span data-stu-id="e3d19-180">See also</span></span>

- [<span data-ttu-id="e3d19-181">Kustannusseurannan työtila</span><span class="sxs-lookup"><span data-stu-id="e3d19-181">Cost control workspace</span></span>](cost-control-workspace.md)
- [<span data-ttu-id="e3d19-182">Dimensiohierarkia</span><span class="sxs-lookup"><span data-stu-id="e3d19-182">Dimension hierarchy</span></span>](dimension-hierarchy.md)
- [<span data-ttu-id="e3d19-183">Kustannuslaskennan sisältöpaketin määrittäminen</span><span class="sxs-lookup"><span data-stu-id="e3d19-183">Set up security for Cost accounting content pack</span></span>](../../dev-itpro/analytics/setup-security-cost-accounting-content-pack.md)

