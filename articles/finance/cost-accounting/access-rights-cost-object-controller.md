---
title: Käyttöoikeudet kustannusobjektin vastuuhenkilölle
description: Tässä ohjeaiheessa on tietoja kustannusobjektin vastuuhenkilöiden käyttöoikeuksista.
author: AndersGirke
ms.date: 06/24/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CAMCostControlWorkspace, CAMParameters
audience: Application User
ms.reviewer: roschlom
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: roschlom
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: a3639c05b24de31cfa09d2d9d0cf427122f51eae
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/01/2021
ms.locfileid: "5810195"
---
# <a name="access-rights-for-cost-object-controllers"></a><span data-ttu-id="dbd0a-103">Käyttöoikeudet kustannusobjektin vastuuhenkilölle</span><span class="sxs-lookup"><span data-stu-id="dbd0a-103">Access rights for cost object controllers</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="dbd0a-104">Esimiehet voivat tarkastella **kustannusseurannan** työtilassa keskitetysti kustannusobjektiensa suoriutumista.</span><span class="sxs-lookup"><span data-stu-id="dbd0a-104">The **Cost control** workspace is a central point where managers can view the performance of their cost objects.</span></span> <span data-ttu-id="dbd0a-105">Esimiehet voivat käyttää tässä tilassa kustannuslaskentatietoja, vaikka he eivät ole kustannuslaskijoita.</span><span class="sxs-lookup"><span data-stu-id="dbd0a-105">This workspace lets managers consume Cost accounting data even though they aren't cost accountants.</span></span> <span data-ttu-id="dbd0a-106">Tietoturvasyistä esimiesten pitäisi saada tarkastella vain niitä kustannuslaskentatietoja, jotka liittyvät heidän vastuullaan olevien kustannusobjekteihin.</span><span class="sxs-lookup"><span data-stu-id="dbd0a-106">For security reasons, managers should be allowed to see only the Cost accounting data that is related to the specific cost objects that they are responsible for.</span></span>

<span data-ttu-id="dbd0a-107">Kustannuslaskennassa on neljä yksilöivää roolia.</span><span class="sxs-lookup"><span data-stu-id="dbd0a-107">There are four unique roles in Cost accounting.</span></span>

| <span data-ttu-id="dbd0a-108">Roolin nimi</span><span class="sxs-lookup"><span data-stu-id="dbd0a-108">Role name</span></span>               | <span data-ttu-id="dbd0a-109">Käyttöoikeus</span><span class="sxs-lookup"><span data-stu-id="dbd0a-109">License</span></span>      |
|-------------------------|--------------|
| <span data-ttu-id="dbd0a-110">Kustannuslaskennan hallinta</span><span class="sxs-lookup"><span data-stu-id="dbd0a-110">Cost accounting manager</span></span> | <span data-ttu-id="dbd0a-111">Tehtävä</span><span class="sxs-lookup"><span data-stu-id="dbd0a-111">Activity</span></span>     |
| <span data-ttu-id="dbd0a-112">Kustannuslaskija</span><span class="sxs-lookup"><span data-stu-id="dbd0a-112">Cost accountant</span></span>         | <span data-ttu-id="dbd0a-113">Operations</span><span class="sxs-lookup"><span data-stu-id="dbd0a-113">Operations</span></span>   |
| <span data-ttu-id="dbd0a-114">Kustannuslaskijan apulainen</span><span class="sxs-lookup"><span data-stu-id="dbd0a-114">Cost accountant clerk</span></span>   | <span data-ttu-id="dbd0a-115">Operations</span><span class="sxs-lookup"><span data-stu-id="dbd0a-115">Operations</span></span>   |
| <span data-ttu-id="dbd0a-116">Kustannusobjektin vastuuhenkilö</span><span class="sxs-lookup"><span data-stu-id="dbd0a-116">Cost object controller</span></span>  | <span data-ttu-id="dbd0a-117">Tiimin jäsenet</span><span class="sxs-lookup"><span data-stu-id="dbd0a-117">Team members</span></span> |

<span data-ttu-id="dbd0a-118">Tässä ohjeaiheessa kerrotaan, miten **kustannusobjektin vastuuhenkilön** määritetään esimiehelle.</span><span class="sxs-lookup"><span data-stu-id="dbd0a-118">This topic explains how to assign the **Cost object controller** role to a manager.</span></span>

<span data-ttu-id="dbd0a-119">Kun **kustannusobjektin vastuuhenkilön** rooli on määritetty esimiehelle, tämä voi suorittaa seuraavat tehtävät:</span><span class="sxs-lookup"><span data-stu-id="dbd0a-119">When the **Cost object controller** role is assigned to a manager, the manager can perform the following tasks:</span></span>

- <span data-ttu-id="dbd0a-120">**kustannusseurannan** työtilan käyttö (asiakasohjelmassa)</span><span class="sxs-lookup"><span data-stu-id="dbd0a-120">Access the **Cost control** workspace (in the client).</span></span>

    - <span data-ttu-id="dbd0a-121">porautumista tukevien sivujen poraus- ja tarkasteluoikeudet</span><span class="sxs-lookup"><span data-stu-id="dbd0a-121">Drill through and have view access to the pages that support the drill-through experience.</span></span>

- <span data-ttu-id="dbd0a-122">**kustannusseurannan** työtilan käyttö (mobiilisovelluksessa)</span><span class="sxs-lookup"><span data-stu-id="dbd0a-122">Access the **Cost control** workspace (in the mobile application).</span></span>

> [!NOTE]
> <span data-ttu-id="dbd0a-123">**kustannusobjektin vastuuhenkilön** roolilla ei voi hallita sitä, mitä kustannusobjekteja käyttäjä voi käyttää ja minkä tietoja hän voi tarkastella.</span><span class="sxs-lookup"><span data-stu-id="dbd0a-123">The **Cost object controller** role doesn't control which cost objects the user can access and view data for.</span></span> <span data-ttu-id="dbd0a-124">Rivitason suojaus perustuu dimensio- ja käyttöoikeusluettelohierarkioihin.</span><span class="sxs-lookup"><span data-stu-id="dbd0a-124">Row-level security is provided via dimension hierarchies and the Access list hierarchy.</span></span>

## <a name="grant-access-rights"></a><span data-ttu-id="dbd0a-125">Käyttöoikeuksien myöntäminen</span><span class="sxs-lookup"><span data-stu-id="dbd0a-125">Grant access rights</span></span>
<span data-ttu-id="dbd0a-126">Seuraavassa on esimerkki dimensiohierarkiasta.</span><span class="sxs-lookup"><span data-stu-id="dbd0a-126">The following example shows what a dimension hierarchy can look like.</span></span>

<span data-ttu-id="dbd0a-127">**Dimension hierarkiatiedot**</span><span class="sxs-lookup"><span data-stu-id="dbd0a-127">**Dimension hierarchy details**</span></span>

| <span data-ttu-id="dbd0a-128">Dimensiohierarkian nimi</span><span class="sxs-lookup"><span data-stu-id="dbd0a-128">Dimension hierarchy name</span></span> | <span data-ttu-id="dbd0a-129">Dimensio</span><span class="sxs-lookup"><span data-stu-id="dbd0a-129">Dimension</span></span>    | <span data-ttu-id="dbd0a-130">Dimensiohierarkiatyypin nimi</span><span class="sxs-lookup"><span data-stu-id="dbd0a-130">Dimension hierarchy type name</span></span>      | <span data-ttu-id="dbd0a-131">Käyttöoikeusluettelohierarkia</span><span class="sxs-lookup"><span data-stu-id="dbd0a-131">Access list hierarchy</span></span> |
|--------------------------|--------------|------------------------------------|-----------------------|
| <span data-ttu-id="dbd0a-132">Organisaatio</span><span class="sxs-lookup"><span data-stu-id="dbd0a-132">Organization</span></span>             | <span data-ttu-id="dbd0a-133">Kustannuspaikat</span><span class="sxs-lookup"><span data-stu-id="dbd0a-133">Cost centers</span></span> | <span data-ttu-id="dbd0a-134">Dimension luokitteluhierarkia</span><span class="sxs-lookup"><span data-stu-id="dbd0a-134">Dimension classification hierarchy</span></span> | <span data-ttu-id="dbd0a-135">**Kyllä**</span><span class="sxs-lookup"><span data-stu-id="dbd0a-135">**Yes**</span></span>               |

<span data-ttu-id="dbd0a-136">Voit lisätä kuhunkin solmuun käyttäjätunnuksia hierarkian suunnittelutoiminnon **Käyttäjät**-pikavälilehdessä.</span><span class="sxs-lookup"><span data-stu-id="dbd0a-136">You can use the **Users** FastTab in the hierarchy designer to insert one or more user IDs on each node.</span></span>

|                                   | <span data-ttu-id="dbd0a-137">Käyttäjät</span><span class="sxs-lookup"><span data-stu-id="dbd0a-137">Users</span></span>            | <span data-ttu-id="dbd0a-138">Dimension jäsenalueet</span><span class="sxs-lookup"><span data-stu-id="dbd0a-138">Dimension member ranges</span></span>   |                         |
|-----------------------------------|------------------|---------------------------|-------------------------|
| <span data-ttu-id="dbd0a-139">**Solmukohdat**</span><span class="sxs-lookup"><span data-stu-id="dbd0a-139">**Nodes**</span></span>                         | <span data-ttu-id="dbd0a-140">**Käyttäjätunnus**</span><span class="sxs-lookup"><span data-stu-id="dbd0a-140">**User ID**</span></span>      | <span data-ttu-id="dbd0a-141">**Lähtödimension jäsen**</span><span class="sxs-lookup"><span data-stu-id="dbd0a-141">**From dimension member**</span></span> | <span data-ttu-id="dbd0a-142">**Kohdedimension jäsen**</span><span class="sxs-lookup"><span data-stu-id="dbd0a-142">**To dimension member**</span></span> |
| <span data-ttu-id="dbd0a-143">Organisaatio</span><span class="sxs-lookup"><span data-stu-id="dbd0a-143">Organization</span></span>                      | <span data-ttu-id="dbd0a-144">Benjamin, Claire</span><span class="sxs-lookup"><span data-stu-id="dbd0a-144">Benjamin, Claire</span></span> |                           |                         |
| <span data-ttu-id="dbd0a-145">&nbsp;&nbsp;Hallinto</span><span class="sxs-lookup"><span data-stu-id="dbd0a-145">&nbsp;&nbsp;Admin</span></span>                 | <span data-ttu-id="dbd0a-146">Huhtikuu</span><span class="sxs-lookup"><span data-stu-id="dbd0a-146">April</span></span>            |                           |                         |
| <span data-ttu-id="dbd0a-147">&nbsp;&nbsp;&nbsp;&nbsp;Myyntitiedot</span><span class="sxs-lookup"><span data-stu-id="dbd0a-147">&nbsp;&nbsp;&nbsp;&nbsp;Finance</span></span>   | <span data-ttu-id="dbd0a-148">Alicia</span><span class="sxs-lookup"><span data-stu-id="dbd0a-148">Alicia</span></span>           | <span data-ttu-id="dbd0a-149">CC002</span><span class="sxs-lookup"><span data-stu-id="dbd0a-149">CC002</span></span>                     | <span data-ttu-id="dbd0a-150">CC003</span><span class="sxs-lookup"><span data-stu-id="dbd0a-150">CC003</span></span>                   |
|                                   |                  | <span data-ttu-id="dbd0a-151">CC007</span><span class="sxs-lookup"><span data-stu-id="dbd0a-151">CC007</span></span>                     | <span data-ttu-id="dbd0a-152">CC007</span><span class="sxs-lookup"><span data-stu-id="dbd0a-152">CC007</span></span>                   |
| <span data-ttu-id="dbd0a-153">&nbsp;&nbsp;&nbsp;&nbsp;Henkilöstöhallinto</span><span class="sxs-lookup"><span data-stu-id="dbd0a-153">&nbsp;&nbsp;&nbsp;&nbsp;HR</span></span>        | <span data-ttu-id="dbd0a-154">Arnie</span><span class="sxs-lookup"><span data-stu-id="dbd0a-154">Arnie</span></span>            | <span data-ttu-id="dbd0a-155">CC001</span><span class="sxs-lookup"><span data-stu-id="dbd0a-155">CC001</span></span>                     | <span data-ttu-id="dbd0a-156">CC001</span><span class="sxs-lookup"><span data-stu-id="dbd0a-156">CC001</span></span>                   |
| <span data-ttu-id="dbd0a-157">&nbsp;&nbsp;Tuotanto</span><span class="sxs-lookup"><span data-stu-id="dbd0a-157">&nbsp;&nbsp;Production</span></span>            | <span data-ttu-id="dbd0a-158">David</span><span class="sxs-lookup"><span data-stu-id="dbd0a-158">David</span></span>            |                           |                         |
| <span data-ttu-id="dbd0a-159">&nbsp;&nbsp;&nbsp;&nbsp;Pakkaus</span><span class="sxs-lookup"><span data-stu-id="dbd0a-159">&nbsp;&nbsp;&nbsp;&nbsp;Packaging</span></span> | <span data-ttu-id="dbd0a-160">Ellen</span><span class="sxs-lookup"><span data-stu-id="dbd0a-160">Ellen</span></span>            | <span data-ttu-id="dbd0a-161">CC005</span><span class="sxs-lookup"><span data-stu-id="dbd0a-161">CC005</span></span>                     | <span data-ttu-id="dbd0a-162">CC005</span><span class="sxs-lookup"><span data-stu-id="dbd0a-162">CC005</span></span>                   |
| <span data-ttu-id="dbd0a-163">&nbsp;&nbsp;&nbsp;&nbsp;Kokoonpano</span><span class="sxs-lookup"><span data-stu-id="dbd0a-163">&nbsp;&nbsp;&nbsp;&nbsp;Assembly</span></span>  | <span data-ttu-id="dbd0a-164">Chris</span><span class="sxs-lookup"><span data-stu-id="dbd0a-164">Chris</span></span>            | <span data-ttu-id="dbd0a-165">CC006</span><span class="sxs-lookup"><span data-stu-id="dbd0a-165">CC006</span></span>                     | <span data-ttu-id="dbd0a-166">CC006</span><span class="sxs-lookup"><span data-stu-id="dbd0a-166">CC006</span></span>                   |

> [!NOTE]
> <span data-ttu-id="dbd0a-167">Kustannuslaskijat on määritettävä hierarkian ylimmälle tasolle, jotta he näkevät kaikki kustannuslaskennan merkinnät.</span><span class="sxs-lookup"><span data-stu-id="dbd0a-167">Cost accountants should be assigned to the top level of the hierarchy, so that they can see all entries in Cost accounting.</span></span>

<span data-ttu-id="dbd0a-168">Ennen käyttöoikeushierarkian ja sen suojausasetusten käyttöönottoa **Ota käyttöön katseluoikeus kustannusobjektin dimension jäsenille** -asetukseksi on valittava **Kyllä** **Kustannuslaskentaparametrit**-sivun **Yleiset**-välilehdessä (**Kustannuslaskenta** > **Asetukset** > **Parametrit**).</span><span class="sxs-lookup"><span data-stu-id="dbd0a-168">Before the Access list hierarchy and its security settings can be applied, the **Enable view access for cost object dimension members** option must be set to **Yes** on the **General** tab of the **Cost accounting parameters** page (**Cost accounting** > **Setup** > **Parameters**).</span></span>

<span data-ttu-id="dbd0a-169">Käyttöoikeusluettelohierarkian asetuksilla hallitaan seuraavilla alueilla näkyviä tietoja:</span><span class="sxs-lookup"><span data-stu-id="dbd0a-169">The settings for the Access list hierarchy are used to control the data that is shown in following areas:</span></span>

- <span data-ttu-id="dbd0a-170">**Kustannusseurannan** työtila (asiakasohjelmassa):</span><span class="sxs-lookup"><span data-stu-id="dbd0a-170">**Cost control** workspace (in the client):</span></span>

    - <span data-ttu-id="dbd0a-171">Porautumiseen käytettävien sivujen tiedot</span><span class="sxs-lookup"><span data-stu-id="dbd0a-171">Data on the pages that are used for drill-through</span></span>

- <span data-ttu-id="dbd0a-172">**Kustannusseurannan** työtila (mobiilisovelluksessa):</span><span class="sxs-lookup"><span data-stu-id="dbd0a-172">**Cost control** workspace (in the mobile application):</span></span>

    - <span data-ttu-id="dbd0a-173">Korttien saldot</span><span class="sxs-lookup"><span data-stu-id="dbd0a-173">Balances in cards</span></span>

- <span data-ttu-id="dbd0a-174">Microsoft Power BI:</span><span class="sxs-lookup"><span data-stu-id="dbd0a-174">Microsoft Power BI:</span></span>

    - <span data-ttu-id="dbd0a-175">Power BI -visualisoinneissa näytettävät tiedot</span><span class="sxs-lookup"><span data-stu-id="dbd0a-175">Data that is shown in Power BI visualizations</span></span>
    - <span data-ttu-id="dbd0a-176">Tietojen Power BI -visualisoinnit, jotka on upotettu Dynamics 365 Financen asiakasohjelmassa</span><span class="sxs-lookup"><span data-stu-id="dbd0a-176">Data Power BI visualizations that are embedded in the Dynamics 365 Finance client</span></span>

> [!IMPORTANT]
> - <span data-ttu-id="dbd0a-177">Käyttöoikeusluettelon hierarkia ei ole vaikuta Power BI -tietoihin, ennen kuin käyttöoikeusluettelon hierarkia ja Power BI:n rivitason suojaus ovat muodostaneet parin.</span><span class="sxs-lookup"><span data-stu-id="dbd0a-177">Before the Access list hierarchy can affect data in Power BI, the Access list hierarchy and row-level security in Power BI must be paired.</span></span> <span data-ttu-id="dbd0a-178">Lisätietoja on ohjeaiheessa [Kustannuslaskennan sisältöpaketin suojauksen määrittäminen](../../dev-itpro/analytics/setup-security-cost-accounting-content-pack.md).</span><span class="sxs-lookup"><span data-stu-id="dbd0a-178">For more information, see [Set up security for Cost accounting content pack](../../dev-itpro/analytics/setup-security-cost-accounting-content-pack.md).</span></span>
> - <span data-ttu-id="dbd0a-179">Tässä ohjeaiheessa käsitellään edellytykset, joita ilman **kustannusseurannan** työtilaa ei voi käyttää.</span><span class="sxs-lookup"><span data-stu-id="dbd0a-179">This topic shows the prerequisites that must be in place before you can use the **Cost control** workspace.</span></span>

<span data-ttu-id="dbd0a-180">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="dbd0a-180">Additional resources</span></span>

- [<span data-ttu-id="dbd0a-181">Kustannusseurannan työtila</span><span class="sxs-lookup"><span data-stu-id="dbd0a-181">Cost control workspace</span></span>](cost-control-workspace.md)
- [<span data-ttu-id="dbd0a-182">Dimensiohierarkia</span><span class="sxs-lookup"><span data-stu-id="dbd0a-182">Dimension hierarchy</span></span>](dimension-hierarchy.md)
- [<span data-ttu-id="dbd0a-183">Kustannuslaskennan sisältöpaketin määrittäminen</span><span class="sxs-lookup"><span data-stu-id="dbd0a-183">Set up security for Cost accounting content pack</span></span>](../../dev-itpro/analytics/setup-security-cost-accounting-content-pack.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]