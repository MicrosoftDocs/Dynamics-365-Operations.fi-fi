---
title: Projektiarvioiden synkronointi suoraan Project Service Automationista Finance and Operationsin projektitoimintoihin
description: Tässä ohjeaiheessa käsitellään malleja ja tehtäviä, joilla projektin tunti- ja kuluarviot synkronoidaan suoraan Microsoft Dynamics 365 Project Service Automationista Dynamics 365 Financeen.
author: KimANelson
manager: AnnBe
ms.date: 07/20/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.3.0
ms.openlocfilehash: ebf0fce60ad006e798aa4f404fbffcf10a0b31f9
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/06/2019
ms.locfileid: "2770286"
---
# <a name="synchronize-project-estimates-directly-from-project-service-automation-to-finance-and-operations"></a><span data-ttu-id="1ad6f-103">Projektiarvioiden synkronointi suoraan Project Service Automationista Finance and Operationsin projektitoimintoihin</span><span class="sxs-lookup"><span data-stu-id="1ad6f-103">Synchronize project estimates directly from Project Service Automation to Finance and Operations</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="1ad6f-104">Tässä ohjeaiheessa käsitellään malleja ja tehtäviä, joilla projektin tunti- ja kuluarviot synkronoidaan suoraan Dynamics 365 Project Service Automationista Dynamics 365 Financeiin.</span><span class="sxs-lookup"><span data-stu-id="1ad6f-104">This topic describes the templates and underlying tasks that are used to synchronize project hour estimates and project expense estimates directly from Dynamics 365 Project Service Automation to Dynamics 365 Finance.</span></span>

> [!NOTE]
> - <span data-ttu-id="1ad6f-105">Projektitehtävän integrointi, kulutapahtumaluokat, tuntiarviot, kuluarviot ja toiminnon lukitseminen ovat käytössä versiossa 8.0.</span><span class="sxs-lookup"><span data-stu-id="1ad6f-105">Project task integration, expense transaction categories, hour estimates, expense estimates, and functionality locking is available in version 8.0.</span></span>
> - <span data-ttu-id="1ad6f-106">Todellisten tietojen integrointi on käytettävissä versiossa 8.0.1 tai sitä uudemmassa.</span><span class="sxs-lookup"><span data-stu-id="1ad6f-106">Actuals integration is available in version 8.0.1 or later.</span></span>

## <a name="data-flow-for-project-service-automation-to-finance"></a><span data-ttu-id="1ad6f-107">Tiedonkulku Project Service Automationista Financeen</span><span class="sxs-lookup"><span data-stu-id="1ad6f-107">Data flow for Project Service Automation to Finance</span></span>

<span data-ttu-id="1ad6f-108">Project Service Automationin ja Financen välinen integrointiratkaisu synkronoi Project Service Automation- ja Finance-esiintymien tiedot tietojen integrointiominaisuudella.</span><span class="sxs-lookup"><span data-stu-id="1ad6f-108">The Project Service Automation to Finance integration solution uses the Data integration feature to synchronize data across instances of Project Service Automation and Finance.</span></span> <span data-ttu-id="1ad6f-109">Tietojen integrointiominaisuudessa käytettävissä olevat integrointimallit mahdollistavat projektin tunti- ja kuluarviointeja koskevan tiedonkulun Project Service Automationista ja Financeen.</span><span class="sxs-lookup"><span data-stu-id="1ad6f-109">The integration templates that are available with the Data integration feature enable the flow of data about project hour estimates and project expense estimates from Project Service Automation to Finance.</span></span>

<span data-ttu-id="1ad6f-110">Seuraava kuva ilmaisee, miten tiedot synkronoidaan Project Service Automationin ja Financen välillä.</span><span class="sxs-lookup"><span data-stu-id="1ad6f-110">The following illustration shows how the data is synchronized between Project Service Automation and Finance.</span></span>

<span data-ttu-id="1ad6f-111">[![Project Service Automationin ja Financen välisen integroinnin tiedonkulku](./media/ProjectEstimatesFlow.png)](./media/ProjectEstimatesFlow.png)</span><span class="sxs-lookup"><span data-stu-id="1ad6f-111">[![Data flow for Project Service Automation integration with Finance](./media/ProjectEstimatesFlow.png)](./media/ProjectEstimatesFlow.png)</span></span>

## <a name="project-hour-estimates"></a><span data-ttu-id="1ad6f-112">Projektien tuntiarvioita</span><span class="sxs-lookup"><span data-stu-id="1ad6f-112">Project hour estimates</span></span>

### <a name="template-and-tasks"></a><span data-ttu-id="1ad6f-113">Malli ja tehtävät</span><span class="sxs-lookup"><span data-stu-id="1ad6f-113">Template and tasks</span></span>

<span data-ttu-id="1ad6f-114">Saat käytettävissä olevat mallit käyttöösi valitsemalla Microsoft Power Appsin hallintakeskuksessa **Projektit**. Valitse sitten julkiset mallit valitsemalla oikeassa yläkulmassa **Uusi projekti**.</span><span class="sxs-lookup"><span data-stu-id="1ad6f-114">To access the available templates, in the Microsoft Power Apps admin center, select **Projects**, and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="1ad6f-115">Seuraavaa mallia ja sen taustalla olevia tehtäviä käytetään synkronoimaan projektin tuntiarviot Project Service Automationista Financeen:</span><span class="sxs-lookup"><span data-stu-id="1ad6f-115">The following template and underlying tasks are used to synchronize project hour estimates from Project Service Automation to Finance:</span></span>

- <span data-ttu-id="1ad6f-116">**Mallin nimi tietojen integroinnissa:** Projektin tuntiarviot (PSA:sta Fin and Opsiin)</span><span class="sxs-lookup"><span data-stu-id="1ad6f-116">**Name of the template in Data integration:** Project hour estimates (PSA to Fin and Ops)</span></span>
- <span data-ttu-id="1ad6f-117">**Projektin tehtävien nimi:**</span><span class="sxs-lookup"><span data-stu-id="1ad6f-117">**Name of the tasks in the project:**</span></span>

    - <span data-ttu-id="1ad6f-118">Tapahtumasuhteet</span><span class="sxs-lookup"><span data-stu-id="1ad6f-118">Transaction relationships</span></span>
    - <span data-ttu-id="1ad6f-119">Kuluarviot</span><span class="sxs-lookup"><span data-stu-id="1ad6f-119">Expense estimates</span></span>

### <a name="entity-set"></a><span data-ttu-id="1ad6f-120">Yksikköjoukko</span><span class="sxs-lookup"><span data-stu-id="1ad6f-120">Entity set</span></span>

| <span data-ttu-id="1ad6f-121">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="1ad6f-121">Project Service Automation</span></span> | <span data-ttu-id="1ad6f-122">Myyntitiedot</span><span class="sxs-lookup"><span data-stu-id="1ad6f-122">Finance</span></span>                                       |
|----------------------------|-----------------------------------------------|
| <span data-ttu-id="1ad6f-123">Projektitehtävät</span><span class="sxs-lookup"><span data-stu-id="1ad6f-123">Project tasks</span></span>              | <span data-ttu-id="1ad6f-124">Projektin tuntiarvioiden integrointiyksikkö</span><span class="sxs-lookup"><span data-stu-id="1ad6f-124">Integration entity for project hour estimates</span></span> |

### <a name="entity-flow"></a><span data-ttu-id="1ad6f-125">Yksikön työnkulku</span><span class="sxs-lookup"><span data-stu-id="1ad6f-125">Entity flow</span></span>

<span data-ttu-id="1ad6f-126">Projektin tuntiarvioita hallitaan Project Service Automationissa ja ne synkronoidaan Financen projektin tuntiennusteisiin.</span><span class="sxs-lookup"><span data-stu-id="1ad6f-126">Project hour estimates are managed in Project Service Automation, and they are synchronized to Finance as project hour forecasts.</span></span>

### <a name="prerequisites"></a><span data-ttu-id="1ad6f-127">Edellytykset</span><span class="sxs-lookup"><span data-stu-id="1ad6f-127">Prerequisites</span></span>

<span data-ttu-id="1ad6f-128">Projektin, projektitehtävien ja projektin kuluarvion tapahtumaluokat on synkronoitava, ennen kuin projektin tuntiarviot voidaan synkronoida.</span><span class="sxs-lookup"><span data-stu-id="1ad6f-128">Before synchronization of project hour estimates can occur, you must synchronize projects, project tasks, and project expense transaction categories.</span></span>

### <a name="power-query"></a><span data-ttu-id="1ad6f-129">Power Query</span><span class="sxs-lookup"><span data-stu-id="1ad6f-129">Power Query</span></span>

<span data-ttu-id="1ad6f-130">Projektin tuntiarvioiden mallissa on käytettävä Microsoft Power Query for Exceliä seuraavien toimintojen päivittämiseen:</span><span class="sxs-lookup"><span data-stu-id="1ad6f-130">In the project hour estimates template, you must use Microsoft Power Query for Excel to complete these tasks:</span></span>

- <span data-ttu-id="1ad6f-131">Määritettävää oletusennustemallin tunnusta käytetään, kun integrointi luo uusi tuntiennusteita.</span><span class="sxs-lookup"><span data-stu-id="1ad6f-131">Set the default forecast model ID that will be used when the integration creates new hour forecasts.</span></span>
- <span data-ttu-id="1ad6f-132">Sellaisten tehtävän resurssikohteisten tietueiden suodattaminen pois, jotka aiheuttavat tuntiennusteisiin tapahtuvan integroinnin epäonnistumisen.</span><span class="sxs-lookup"><span data-stu-id="1ad6f-132">Filter out any resource-specific records in the task that will fail the integration into hour forecasts.</span></span>
- <span data-ttu-id="1ad6f-133">Tyhjien tapahtumaluokkarivien suodattaminen pois.</span><span class="sxs-lookup"><span data-stu-id="1ad6f-133">Filter out any empty transaction category rows.</span></span> <span data-ttu-id="1ad6f-134">Jos suodatusta ei tehdä valmiiksi, tuloksena voi olla virheellisiä tuntiennusteita</span><span class="sxs-lookup"><span data-stu-id="1ad6f-134">Failure to complete this task might result in incorrect hour forecasts.</span></span>

#### <a name="set-the-default-forecast-model-id"></a><span data-ttu-id="1ad6f-135">Aseta ennustemallin oletusarvon tunnus.</span><span class="sxs-lookup"><span data-stu-id="1ad6f-135">Set the default forecast model ID</span></span>

<span data-ttu-id="1ad6f-136">Voit päivittää malliin oletusennustemallin tunnuksen avaamalla määrityksen napsauttamalla **Yhdistä**-nuolta.</span><span class="sxs-lookup"><span data-stu-id="1ad6f-136">To update the default forecast model ID in the template, click the **Map** arrow to open the mapping.</span></span> <span data-ttu-id="1ad6f-137">Valitse sitten **Kyselyn ja suodatuksen lisäasetukset** -linkki.</span><span class="sxs-lookup"><span data-stu-id="1ad6f-137">Then select the **Advanced Query and Filtering** link.</span></span>

- <span data-ttu-id="1ad6f-138">Jos käytät projektin tuntiarvioita (PSA:sta Fin and Opsiin) -oletusmallia, valitse **Lisätty ehto** **Käytetyt vaiheet** -listassa.</span><span class="sxs-lookup"><span data-stu-id="1ad6f-138">If you're using the default Project hour estimates (PSA to Fin and Ops) template, select the **Inserted Condition** in the list of **Applied Steps**.</span></span> <span data-ttu-id="1ad6f-139">Vaihda **Toiminto**-merkinnän **O\_forecast** tilalle sen ennustemallin tunnuksen nimi, jota käytetään integraatiossa.</span><span class="sxs-lookup"><span data-stu-id="1ad6f-139">In the **Function** entry, replace **O\_forecast** with the name of the forecast model ID that should be used with the integration.</span></span> <span data-ttu-id="1ad6f-140">Oletusmallin ennustemalli tunnus on saatu esittelytiedoista.</span><span class="sxs-lookup"><span data-stu-id="1ad6f-140">The default template has a forecast model ID from the demo data.</span></span>
- <span data-ttu-id="1ad6f-141">Jos luot uuden mallin, sinun on lisättävä tämä sarake.</span><span class="sxs-lookup"><span data-stu-id="1ad6f-141">If you're creating a new template, you must add this column.</span></span> <span data-ttu-id="1ad6f-142">Valitse Power Queryssä **Lisää ehtosarake** ja anna uudelle sarakkeelle nimi, kuten **Mallin tunnus**.</span><span class="sxs-lookup"><span data-stu-id="1ad6f-142">In Power Query, select **Add Conditional Column**, and enter a name for the new column, such as **ModelID**.</span></span> <span data-ttu-id="1ad6f-143">Anna sarakkeelle ehto, jonka mukaan jos projektitehtävä ei ole tyhjäarvo, niin \<anna ennustemallin tunnus\>; muutoin tyhjäarvo.</span><span class="sxs-lookup"><span data-stu-id="1ad6f-143">Enter the condition for the column, where, if Project task is not null, then \<enter the forecast model ID\>; else null.</span></span>

#### <a name="filter-out-resource-specific-records"></a><span data-ttu-id="1ad6f-144">Resurssikohtaisten tietueiden suodattaminen</span><span class="sxs-lookup"><span data-stu-id="1ad6f-144">Filter out resource-specific records</span></span>

<span data-ttu-id="1ad6f-145">Projektin tuntiarviot (PSA:sta Fin and Opsiin) -mallissa on oletussuodatin, joka poistaa kaikki resurssikohtaiset tietueet.</span><span class="sxs-lookup"><span data-stu-id="1ad6f-145">The Project hour estimates (PSA to Fin and Ops) template has a default filter that removes any resource-specific records.</span></span> <span data-ttu-id="1ad6f-146">Jos luot oman mallin, tämä suodatin on lisättävä.</span><span class="sxs-lookup"><span data-stu-id="1ad6f-146">If you create your own template, you must add this filter.</span></span> <span data-ttu-id="1ad6f-147">Valitse **Advanced Query and Filtering** -linkki suodattaaksesi **msdyn\_islinetask** -sarakkesta niin, että vain **Epätosi** -asiakirjat ovat mukana.</span><span class="sxs-lookup"><span data-stu-id="1ad6f-147">Select the **Advanced Query and Filtering** link to filter on the **msdyn\_islinetask** column so that only **False** records are included.</span></span>

#### <a name="filter-out-empty-transaction-category-rows"></a><span data-ttu-id="1ad6f-148">Tyhjien tapahtumaluokkarivien suodattaminen</span><span class="sxs-lookup"><span data-stu-id="1ad6f-148">Filter out empty transaction category rows</span></span>

<span data-ttu-id="1ad6f-149">Kaikki tyhjiä tapahtumaluokkia sisältävät rivit poistava suodatin on lisättävä.</span><span class="sxs-lookup"><span data-stu-id="1ad6f-149">You must add a filter to remove any rows that have empty transaction categories.</span></span> <span data-ttu-id="1ad6f-150">Tämä tehtävä vaaditaan riippumatta siitä, käytätkö oletusmallia vai luotko oman mallin.</span><span class="sxs-lookup"><span data-stu-id="1ad6f-150">This task is required, regardless of whether you're using the default template or creating your own template.</span></span> <span data-ttu-id="1ad6f-151">Tämä suodatin poistaa kaikki Project Service Automationin yhteenvetorivit, joiden vuoksi Financen tuntiennusteet voisivat olla virheellisiä.</span><span class="sxs-lookup"><span data-stu-id="1ad6f-151">This filter removes any summary rows from Project Service Automation that might cause the hour forecasts in Finance to be incorrect.</span></span> <span data-ttu-id="1ad6f-152">Valitse **Advanced Query and Filtering** -linkki poissuodattaaksesi tyhjäarvoiset tietueet **msdyn\_transactioncategory\_value** -sarakkeessa.</span><span class="sxs-lookup"><span data-stu-id="1ad6f-152">Select **Advanced Query and Filtering** link to filter out null records in the **msdyn\_transactioncategory\_value** column.</span></span>

### <a name="template-mapping-in-data-integration"></a><span data-ttu-id="1ad6f-153">Mallin yhdistäminen tietojen integroinnin yhteydessä</span><span class="sxs-lookup"><span data-stu-id="1ad6f-153">Template mapping in Data integration</span></span>

<span data-ttu-id="1ad6f-154">Seuraavassa kuvassa on esimerkki mallitehtävän yhdistämisestä tietojen integroinnin yhteydessä.</span><span class="sxs-lookup"><span data-stu-id="1ad6f-154">The following illustration shows an example of the template task mapping in Data integration.</span></span> <span data-ttu-id="1ad6f-155">Yhdistämismääritys näyttää Project Service Automationista Financeen synkronoitavien kenttien tiedot.</span><span class="sxs-lookup"><span data-stu-id="1ad6f-155">The mapping shows the field information that will be synchronized from Project Service Automation to Finance.</span></span>

<span data-ttu-id="1ad6f-156">[![Mallin yhdistäminen](./media/ProjectHourEstimatesMapping.jpg)](./media/ProjectHourEstimatesMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="1ad6f-156">[![Template mapping](./media/ProjectHourEstimatesMapping.jpg)](./media/ProjectHourEstimatesMapping.jpg)</span></span>

## <a name="project-expense-estimates"></a><span data-ttu-id="1ad6f-157">Projektin kustannusarviot</span><span class="sxs-lookup"><span data-stu-id="1ad6f-157">Project expense estimates</span></span>

### <a name="template-and-tasks"></a><span data-ttu-id="1ad6f-158">Malli ja tehtävät</span><span class="sxs-lookup"><span data-stu-id="1ad6f-158">Template and tasks</span></span>

<span data-ttu-id="1ad6f-159">Seuraavaa mallia ja sen taustalla olevia tehtäviä käytetään synkronoimaan projektin kuluarviot Project Service Automationista Financeen:</span><span class="sxs-lookup"><span data-stu-id="1ad6f-159">The following template and underlying tasks are used to synchronize project expense estimates from Project Service Automation to Finance:</span></span>

- <span data-ttu-id="1ad6f-160">**Mallin nimi tietojen integroinnissa:** Projektin kuluarviot (PSA:sta Fin and Opsiin)</span><span class="sxs-lookup"><span data-stu-id="1ad6f-160">**Name of the template in Data integration:** Project expense estimates (PSA to Fin and Ops)</span></span>
- <span data-ttu-id="1ad6f-161">**Projektin tehtävien nimi:**</span><span class="sxs-lookup"><span data-stu-id="1ad6f-161">**Name of the tasks in the project:**</span></span>

    - <span data-ttu-id="1ad6f-162">Tapahtumasuhteet</span><span class="sxs-lookup"><span data-stu-id="1ad6f-162">Transaction relationships</span></span> 
    - <span data-ttu-id="1ad6f-163">Kuluarviot</span><span class="sxs-lookup"><span data-stu-id="1ad6f-163">Expense estimates</span></span>

### <a name="entity-set"></a><span data-ttu-id="1ad6f-164">Yksikköjoukko</span><span class="sxs-lookup"><span data-stu-id="1ad6f-164">Entity set</span></span>

| <span data-ttu-id="1ad6f-165">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="1ad6f-165">Project Service Automation</span></span> | <span data-ttu-id="1ad6f-166">Myyntitiedot</span><span class="sxs-lookup"><span data-stu-id="1ad6f-166">Finance</span></span>                                                  |
|----------------------------|----------------------------------------------------------|
| <span data-ttu-id="1ad6f-167">Tapahtumayhteydet</span><span class="sxs-lookup"><span data-stu-id="1ad6f-167">Transaction Connections</span></span>    | <span data-ttu-id="1ad6f-168">Projektin tapahtumasuhteiden integrointiyksikkö</span><span class="sxs-lookup"><span data-stu-id="1ad6f-168">Integration entity for project transaction relationships</span></span> |
| <span data-ttu-id="1ad6f-169">Arviorivit</span><span class="sxs-lookup"><span data-stu-id="1ad6f-169">Estimate Lines</span></span>             | <span data-ttu-id="1ad6f-170">Projektin kuluarvioiden integrointiyksikkö</span><span class="sxs-lookup"><span data-stu-id="1ad6f-170">Integration entity for project expense estimates</span></span>         |

### <a name="entity-flow"></a><span data-ttu-id="1ad6f-171">Yksikön työnkulku</span><span class="sxs-lookup"><span data-stu-id="1ad6f-171">Entity flow</span></span>

<span data-ttu-id="1ad6f-172">Projektin kuluarvioita hallitaan Project Service Automationissa ja ne synkronoidaan Financen projektin kuluennusteisiin.</span><span class="sxs-lookup"><span data-stu-id="1ad6f-172">Project expense estimates are managed in Project Service Automation, and they are synchronized to Finance as project expense forecasts.</span></span>

### <a name="prerequisites"></a><span data-ttu-id="1ad6f-173">Edellytykset</span><span class="sxs-lookup"><span data-stu-id="1ad6f-173">Prerequisites</span></span>

<span data-ttu-id="1ad6f-174">Projektin, projektitehtävien ja projektin kuluarvion tapahtumaluokat on synkronoitava, ennen kuin projektin kuluarviot voidaan synkronoida.</span><span class="sxs-lookup"><span data-stu-id="1ad6f-174">Before synchronization of project expense estimates can occur, you must synchronize projects, project tasks, and project expense transaction categories.</span></span>

### <a name="power-query"></a><span data-ttu-id="1ad6f-175">Power Query</span><span class="sxs-lookup"><span data-stu-id="1ad6f-175">Power Query</span></span>

<span data-ttu-id="1ad6f-176">Projektin kuluarviomallissa on käytettävä Power Query for Exceliä seuraavien toimintojen päivittämiseen:</span><span class="sxs-lookup"><span data-stu-id="1ad6f-176">In the project expense estimates template, you must use Power Query to complete the following tasks:</span></span>

- <span data-ttu-id="1ad6f-177">Vain kuluarviorivien tietueet sisällyttävä suodatus.</span><span class="sxs-lookup"><span data-stu-id="1ad6f-177">Filter to include only expense estimate line records.</span></span>
- <span data-ttu-id="1ad6f-178">Määritettävää oletusennustemallin tunnusta käytetään, kun integrointi luo uusi tuntiennusteita.</span><span class="sxs-lookup"><span data-stu-id="1ad6f-178">Set the default forecast model ID that will be used when the integration creates new hour forecasts.</span></span>
- <span data-ttu-id="1ad6f-179">Laskutustyyppien muuntaminen.</span><span class="sxs-lookup"><span data-stu-id="1ad6f-179">Transform the billing types.</span></span>
- <span data-ttu-id="1ad6f-180">Tapahtumatyyppien muuntaminen.</span><span class="sxs-lookup"><span data-stu-id="1ad6f-180">Transform the transaction types.</span></span>

#### <a name="filter-to-include-only-expense-estimate-lines"></a><span data-ttu-id="1ad6f-181">Vain kuluarviorivit sisällyttävä suodatus</span><span class="sxs-lookup"><span data-stu-id="1ad6f-181">Filter to include only expense estimate lines</span></span>

<span data-ttu-id="1ad6f-182">Projektin kuluarviot (PSA:sta Fin and Opsiin) -mallissa oletussuodatin, joka sisällyttää integraatioon vain kulurivit.</span><span class="sxs-lookup"><span data-stu-id="1ad6f-182">The Project expense estimates (PSA to Fin and Ops) template has a default filter that includes only expense lines in the integration.</span></span> <span data-ttu-id="1ad6f-183">Jos luot oman mallin, tämä suodatin on lisättävä.</span><span class="sxs-lookup"><span data-stu-id="1ad6f-183">If you create your own template, you must add this filter.</span></span> <span data-ttu-id="1ad6f-184">Valitse **Tapahtumasuhde**-tehtävä ja napsauta **Yhdistä**-nuolta avataksesi kartoituksen.</span><span class="sxs-lookup"><span data-stu-id="1ad6f-184">Select the **Transaction relationships** task, and then click the **Map** arrow to open the mapping.</span></span> <span data-ttu-id="1ad6f-185">Valitse **Kyselyn ja suodatuksen lisäasetukset** -linkki.</span><span class="sxs-lookup"><span data-stu-id="1ad6f-185">Select the **Advanced Query and Filtering** link.</span></span> <span data-ttu-id="1ad6f-186">Suodata **msdyn\_transactiontype1** -sarake niin, että se sisältää vain **msdyn\_estimateline** -tiedoston.</span><span class="sxs-lookup"><span data-stu-id="1ad6f-186">Filter the **msdyn\_transactiontype1** column so that it includes only **msdyn\_estimateline**.</span></span>

#### <a name="set-the-default-forecast-model-id"></a><span data-ttu-id="1ad6f-187">Aseta ennustemallin oletusarvon tunnus.</span><span class="sxs-lookup"><span data-stu-id="1ad6f-187">Set the default forecast model ID</span></span>

<span data-ttu-id="1ad6f-188">Voit päivittää malliin oletusennustemallin tunnuksen avaamalla **Kuluarvio**-tehtävän ja sitten napsauttaa **Yhdistä**-nuolta avataksesi kartoituksen.</span><span class="sxs-lookup"><span data-stu-id="1ad6f-188">To update the default forecast model ID in the template, select the **Expense estimates** task, and then click the **Map** arrow to open the mapping.</span></span> <span data-ttu-id="1ad6f-189">Valitse **Kyselyn ja suodatuksen lisäasetukset** -linkki.</span><span class="sxs-lookup"><span data-stu-id="1ad6f-189">Select the **Advanced Query and Filtering** link.</span></span>

- <span data-ttu-id="1ad6f-190">Jos käytät projektin kuluarvioiden oletusmallia (PSA:sta Fin and Opsiin), Power Queryssä, valitse ensimmäinen **Lisätty ehto** **Käytetyt vaiheet** -osassa.</span><span class="sxs-lookup"><span data-stu-id="1ad6f-190">If you're using the default Project expense estimates (PSA to Fin and Ops) template, in Power Query, select the first **Inserted Condition** from the **Applied Steps** section.</span></span> <span data-ttu-id="1ad6f-191">Vaihda **Toiminto**-merkinnän **O\_forecast** tilalle sen ennustemallin tunnuksen nimi, jota käytetään integraatiossa.</span><span class="sxs-lookup"><span data-stu-id="1ad6f-191">In the **Function** entry, replace **O\_forecast** with the name of the forecast model ID that should be used with the integration.</span></span> <span data-ttu-id="1ad6f-192">Oletusmallin ennustemalli tunnus on saatu esittelytiedoista.</span><span class="sxs-lookup"><span data-stu-id="1ad6f-192">The default template has a forecast model ID from the demo data.</span></span>
- <span data-ttu-id="1ad6f-193">Jos luot uuden mallin, sinun on lisättävä tämä sarake.</span><span class="sxs-lookup"><span data-stu-id="1ad6f-193">If you're creating a new template, you must add this column.</span></span> <span data-ttu-id="1ad6f-194">Valitse Power Queryssä **Lisää ehtosarake** ja anna uudelle sarakkeelle nimi, kuten **Mallin tunnus**.</span><span class="sxs-lookup"><span data-stu-id="1ad6f-194">In Power Query, select **Add Conditional Column**, and enter a name for the new column, such as **ModelID**.</span></span> <span data-ttu-id="1ad6f-195">Anna sarakkeelle ehto, jonka mukaan jos arviorivin tunnus ei ole tyhjäarvo, niin \<anna ennustemallin tunnus\>; muutoin tyhjäarvo.</span><span class="sxs-lookup"><span data-stu-id="1ad6f-195">Enter the condition for the column, where, if Estimate line ID is not null, then \<enter the forecast model ID\>; else null.</span></span>

#### <a name="transform-the-billing-types"></a><span data-ttu-id="1ad6f-196">Laskutustyyppien muuntaminen</span><span class="sxs-lookup"><span data-stu-id="1ad6f-196">Transform the billing types</span></span>

<span data-ttu-id="1ad6f-197">Projektin kuluarviot (PSA to Fin and Ops) -malliin kuuluva ehtosarake, joka muuntaa Project Service Automationista vastaanotetut laskutustyypit integroinnin aikana.</span><span class="sxs-lookup"><span data-stu-id="1ad6f-197">The Project expense estimates (PSA to Fin and Ops) template includes a conditional column that is used to transform the billing types that are received from Project Service Automation during the integration.</span></span> <span data-ttu-id="1ad6f-198">Jos luot oman mallin, tämä ehtosarake on lisättävä.</span><span class="sxs-lookup"><span data-stu-id="1ad6f-198">If you create your own template, you must add this conditional column.</span></span> <span data-ttu-id="1ad6f-199">Valitse **kyselyn ja suodatuksen** linkki ja valitse sitten **Lisää ehtosarake**.</span><span class="sxs-lookup"><span data-stu-id="1ad6f-199">Select the **Advanced Query and Filtering** link and then select **Add Conditional Column**.</span></span> <span data-ttu-id="1ad6f-200">Anna sarakkeelle uusi nimi, kuten **Laskutustyyppi**.</span><span class="sxs-lookup"><span data-stu-id="1ad6f-200">Enter a name for the new column, such as **BillingType**.</span></span> <span data-ttu-id="1ad6f-201">Anna sitten seuraava ehto:</span><span class="sxs-lookup"><span data-stu-id="1ad6f-201">Then enter the following condition:</span></span>

<span data-ttu-id="1ad6f-202">Jos **msdyn\_billingtype** = 192350000, silloin **NonChargeable**</span><span class="sxs-lookup"><span data-stu-id="1ad6f-202">If **msdyn\_billingtype** = 192350000, then **NonChargeable**</span></span>  
<span data-ttu-id="1ad6f-203">Jos **msdyn\_billingtype** = 192350001, silloin **Chargeable**</span><span class="sxs-lookup"><span data-stu-id="1ad6f-203">else if **msdyn\_billingtype** = 192350001, then **Chargeable**</span></span>  
<span data-ttu-id="1ad6f-204">Jos **msdyn\_billingtype** = 192350002, silloin **Complimentary**</span><span class="sxs-lookup"><span data-stu-id="1ad6f-204">else if **msdyn\_billingtype** = 192350002, then **Complimentary**</span></span>  
<span data-ttu-id="1ad6f-205">muuta **NotAvailable**</span><span class="sxs-lookup"><span data-stu-id="1ad6f-205">else **NotAvailable**</span></span>

#### <a name="transform-the-transaction-types"></a><span data-ttu-id="1ad6f-206">Tapahtumatyyppien muuntaminen</span><span class="sxs-lookup"><span data-stu-id="1ad6f-206">Transform the transaction types</span></span>

<span data-ttu-id="1ad6f-207">Projektin kuluarviot (PSA to Fin and Ops) -malliin kuuluva ehtosarake, joka muuntaa Project Service Automationista vastaanotetut tapahtumatyypit integroinnin aikana.</span><span class="sxs-lookup"><span data-stu-id="1ad6f-207">The Project expense estimates (PSA to Fin and Ops) template includes a conditional column that is used to transform the transaction types that are received from Project Service Automation during the integration.</span></span> <span data-ttu-id="1ad6f-208">Jos luot oman mallin, tämä ehtosarake on lisättävä.</span><span class="sxs-lookup"><span data-stu-id="1ad6f-208">If you create your own template, you must add this conditional column.</span></span> <span data-ttu-id="1ad6f-209">Valitse **kyselyn ja suodatuksen** linkki ja valitse sitten **Lisää ehtosarake**.</span><span class="sxs-lookup"><span data-stu-id="1ad6f-209">Select the **Advanced Query and Filtering** link and then select **Add Conditional Column**.</span></span> <span data-ttu-id="1ad6f-210">Anna sarakkeelle uusi nimi, kuten **Tapahtumatyyppi**.</span><span class="sxs-lookup"><span data-stu-id="1ad6f-210">Enter a name for the new column, such as **TransactionType**.</span></span> <span data-ttu-id="1ad6f-211">Anna sitten seuraava ehto:</span><span class="sxs-lookup"><span data-stu-id="1ad6f-211">Then enter the following condition:</span></span>

<span data-ttu-id="1ad6f-212">Jos **msdyn\_transactiontypecode** = 192350000, silloin **Cost**</span><span class="sxs-lookup"><span data-stu-id="1ad6f-212">If **msdyn\_transactiontypecode** = 192350000, then **Cost**</span></span>  
<span data-ttu-id="1ad6f-213">jos **msdyn\_transactiontypecode** = 192350005, then **Sales**</span><span class="sxs-lookup"><span data-stu-id="1ad6f-213">else if **msdyn\_transactiontypecode** = 192350005, then **Sales**</span></span>  
<span data-ttu-id="1ad6f-214">else **null**</span><span class="sxs-lookup"><span data-stu-id="1ad6f-214">else **null**</span></span>

### <a name="template-mapping-in-data-integration"></a><span data-ttu-id="1ad6f-215">Mallin yhdistäminen tietojen integroinnin yhteydessä</span><span class="sxs-lookup"><span data-stu-id="1ad6f-215">Template mapping in Data integration</span></span>

<span data-ttu-id="1ad6f-216">Seuraavissa kuvissa on esimerkkejä mallitehtävän yhdistämisistä tietojen integroinnin yhteydessä.</span><span class="sxs-lookup"><span data-stu-id="1ad6f-216">The following illustrations show examples of the template task mappings in Data integration.</span></span> <span data-ttu-id="1ad6f-217">Yhdistämismääritys näyttää Project Service Automationista Financeen synkronoitavien kenttien tiedot.</span><span class="sxs-lookup"><span data-stu-id="1ad6f-217">The mapping shows the field information that will be synchronized from Project Service Automation to Finance.</span></span>

<span data-ttu-id="1ad6f-218">[![Mallin yhdistäminen](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="1ad6f-218">[![Template mapping](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)</span></span>

<span data-ttu-id="1ad6f-219">[![Mallin yhdistäminen](./media/ExpenseEstimatesMapping.jpg)](./media/ExpenseEstimatesMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="1ad6f-219">[![Template mapping](./media/ExpenseEstimatesMapping.jpg)](./media/ExpenseEstimatesMapping.jpg)</span></span>
