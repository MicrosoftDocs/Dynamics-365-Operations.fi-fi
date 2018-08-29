---
title: Projektiarvioiden synkronointi suoraan Project Service Automationista Finance and Operationsin projektitoimintoihin
description: "Tässä ohjeaiheessa käsitellään malleja ja tehtäviä, joilla projektin tunti- ja kuluarviot synkronoidaan suoraan Microsoft Dynamics 365 for Project Service Automationista Microsoft Dynamics 365 for Finance and Operationsiin."
author: KimANelson
manager: AnnBe
ms.date: 07/20/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.3.0
ms.translationtype: HT
ms.sourcegitcommit: d9747ba144d56c9410846769e5465372c89ea111
ms.openlocfilehash: 21338b889e0377dbfd5adfd461ea81b39a75baf8
ms.contentlocale: fi-fi
ms.lasthandoff: 08/08/2018

---
# <a name="synchronize-project-estimates-directly-from-project-service-automation-to-finance-and-operations"></a><span data-ttu-id="dc8ee-103">Projektiarvioiden synkronointi suoraan Project Service Automationista Finance and Operationsin projektitoimintoihin</span><span class="sxs-lookup"><span data-stu-id="dc8ee-103">Synchronize project estimates directly from Project Service Automation to Finance and Operations</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="dc8ee-104">Tässä ohjeaiheessa käsitellään malleja ja tehtäviä, joilla projektin tunti- ja kuluarviot synkronoidaan suoraan Microsoft Dynamics 365 for Project Service Automationista Dynamics 365 for Finance and Operationsiin.</span><span class="sxs-lookup"><span data-stu-id="dc8ee-104">This topic describes the templates and underlying tasks that are used to synchronize project hour estimates and project expense estimates directly from Microsoft Dynamics 365 for Project Service Automation to Dynamics 365 for Finance and Operations.</span></span>

> [!NOTE]
> - <span data-ttu-id="dc8ee-105">Projektitehtävän integrointi, kulutapahtumaluokat, tuntiarviot, kuluarviot ja toiminnon lukitseminen on käytössä Microsoft Dynamics 365 for Finance and Operationsin versiossa 8.0.</span><span class="sxs-lookup"><span data-stu-id="dc8ee-105">Project task integration, expense transaction categories, hour estimates, expense estimates, and functionality locking is available in Microsoft Dynamics 365 for Finance and Operations version 8.0.</span></span>
> - <span data-ttu-id="dc8ee-106">Todellisten tietojen integrointi on käytettävissä Microsoft Dynamics 365 for Finance and Operationsin versiossa 8.01 tai myöhempi.</span><span class="sxs-lookup"><span data-stu-id="dc8ee-106">Actuals integration is available in Microsoft Dynamics 365 for Finance and Operations version 8.0.1 or later.</span></span>
> - <span data-ttu-id="dc8ee-107">Jos käytössä on Microsoft Dynamics 365 for Finance and Operations, Enterprise edition 7.3.0 ja KB 4132657 ja KB 4132660 on asennettu, voit integroida projektitehtäviä, kulutapahtumaluokkia, tuntiarvioita, kuluarvioita ja todellisia tietoja sekä määrittää toimintojen lukituksen.</span><span class="sxs-lookup"><span data-stu-id="dc8ee-107">If you're using Microsoft Dynamics 365 for Finance and Operations, Enterprise edition 7.3.0, after you install KB 4132657 and KB 4132660, you will be able to use the templates to integrate project tasks, expense transaction categories, hour estimates, expense estimates, and actuals, and to configure functionality locking.</span></span> <span data-ttu-id="dc8ee-108">Jos kirjanpidollinen jako on palautettava alkuperäisasetuksiin, myös KB 4131710 kannattaa asentaa.</span><span class="sxs-lookup"><span data-stu-id="dc8ee-108">If you must reset the accounting distributions, we recommend that you also install KB 4131710.</span></span>

## <a name="data-flow-for-project-service-automation-to-finance-and-operations"></a><span data-ttu-id="dc8ee-109">Tiedonkulku Project Service Automationista Finance and Operationsiin</span><span class="sxs-lookup"><span data-stu-id="dc8ee-109">Data flow for Project Service Automation to Finance and Operations</span></span>

<span data-ttu-id="dc8ee-110">Project Service Automationin ja Finance and Operationsin välinen integrointiratkaisu synkronoi Project Service Automationin ja Finance and Operationsin esiintymien tiedot tietojen integrointiominaisuudella.</span><span class="sxs-lookup"><span data-stu-id="dc8ee-110">The Project Service Automation to Finance and Operations integration solution uses the Data integration feature to synchronize data across instances of Project Service Automation and Finance and Operations.</span></span> <span data-ttu-id="dc8ee-111">Tietojen integrointiominaisuudessa käytettävissä olevat integrointimallit mahdollistavat projektin tunti- ja kuluarviointeja koskevan tiedonkulun Project Service Automationista ja Finance and Operationsiin.</span><span class="sxs-lookup"><span data-stu-id="dc8ee-111">The integration templates that are available with the Data integration feature enable the flow of data about project hour estimates and project expense estimates from Project Service Automation to Finance and Operations.</span></span>

<span data-ttu-id="dc8ee-112">Seuraava kuva ilmaisee, miten tiedot synkronoidaan Project Service Automationin ja Finance and Operationsin välillä.</span><span class="sxs-lookup"><span data-stu-id="dc8ee-112">The following illustration shows how the data is synchronized between Project Service Automation and Finance and Operations.</span></span>

<span data-ttu-id="dc8ee-113">[![Project Service Automationin ja Finance and Operationsin välisen integroinnin tiedonkulku](./media/ProjectEstimatesFlow.png)](./media/ProjectEstimatesFlow.png)</span><span class="sxs-lookup"><span data-stu-id="dc8ee-113">[![Data flow for Project Service Automation integration with Finance and Operations](./media/ProjectEstimatesFlow.png)](./media/ProjectEstimatesFlow.png)</span></span>

## <a name="project-hour-estimates"></a><span data-ttu-id="dc8ee-114">Projektien tuntiarvioita</span><span class="sxs-lookup"><span data-stu-id="dc8ee-114">Project hour estimates</span></span>

### <a name="template-and-tasks"></a><span data-ttu-id="dc8ee-115">Malli ja tehtävät</span><span class="sxs-lookup"><span data-stu-id="dc8ee-115">Template and tasks</span></span>

<span data-ttu-id="dc8ee-116">Saat käytettävissä olevat mallit käyttöösi valitsemalla Microsoft PowerAppsin hallintakeskuksessa **Projektit**. Valitse sitten julkaiset mallit valitsemalla oikeassa yläkulmassa **Uusi projekti**.</span><span class="sxs-lookup"><span data-stu-id="dc8ee-116">To access the available templates, in the Microsoft PowerApps admin center, select **Projects**, and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="dc8ee-117">Seuraavaa mallia ja sen taustalla olevia tehtäviä käytetään synkronoimaan projektin tuntiarviot Project Service Automationista Finance and Operationsiin:</span><span class="sxs-lookup"><span data-stu-id="dc8ee-117">The following template and underlying tasks are used to synchronize project hour estimates from Project Service Automation to Finance and Operations:</span></span>

- <span data-ttu-id="dc8ee-118">**Mallin nimi tietojen integroinnissa:** Projektin tuntiarviot (PSA:sta Fin and Opsiin)</span><span class="sxs-lookup"><span data-stu-id="dc8ee-118">**Name of the template in Data integration:** Project hour estimates (PSA to Fin and Ops)</span></span>
- <span data-ttu-id="dc8ee-119">**Projektin tehtävien nimi:**</span><span class="sxs-lookup"><span data-stu-id="dc8ee-119">**Name of the tasks in the project:**</span></span>

    - <span data-ttu-id="dc8ee-120">Tapahtumasuhteet</span><span class="sxs-lookup"><span data-stu-id="dc8ee-120">Transaction relationships</span></span>
    - <span data-ttu-id="dc8ee-121">Kuluarviot</span><span class="sxs-lookup"><span data-stu-id="dc8ee-121">Expense estimates</span></span>

### <a name="entity-set"></a><span data-ttu-id="dc8ee-122">Yksikköjoukko</span><span class="sxs-lookup"><span data-stu-id="dc8ee-122">Entity set</span></span>

| <span data-ttu-id="dc8ee-123">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="dc8ee-123">Project Service Automation</span></span> | <span data-ttu-id="dc8ee-124">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="dc8ee-124">Finance and Operations</span></span>                        |
|----------------------------|-----------------------------------------------|
| <span data-ttu-id="dc8ee-125">Projektitehtävät</span><span class="sxs-lookup"><span data-stu-id="dc8ee-125">Project tasks</span></span>              | <span data-ttu-id="dc8ee-126">Projektin tuntiarvioiden integrointiyksikkö</span><span class="sxs-lookup"><span data-stu-id="dc8ee-126">Integration entity for project hour estimates</span></span> |

### <a name="entity-flow"></a><span data-ttu-id="dc8ee-127">Yksikön työnkulku</span><span class="sxs-lookup"><span data-stu-id="dc8ee-127">Entity flow</span></span>

<span data-ttu-id="dc8ee-128">Projektin tuntiarvioita hallitaan Project Service Automationissa ja ne synkronoidaan Finance and Operationsiin projektin tuntiennusteisiin.</span><span class="sxs-lookup"><span data-stu-id="dc8ee-128">Project hour estimates are managed in Project Service Automation, and they are synchronized to Finance and Operations as project hour forecasts.</span></span>

### <a name="prerequisites"></a><span data-ttu-id="dc8ee-129">Edellytykset</span><span class="sxs-lookup"><span data-stu-id="dc8ee-129">Prerequisites</span></span>

<span data-ttu-id="dc8ee-130">Projektin, projektitehtävien ja projektin kuluarvion tapahtumaluokat on synkronoitava, ennen kuin projektin tuntiarviot voidaan synkronoida.</span><span class="sxs-lookup"><span data-stu-id="dc8ee-130">Before synchronization of project hour estimates can occur, you must synchronize projects, project tasks, and project expense transaction categories.</span></span>

### <a name="power-query"></a><span data-ttu-id="dc8ee-131">Power Query</span><span class="sxs-lookup"><span data-stu-id="dc8ee-131">Power Query</span></span>

<span data-ttu-id="dc8ee-132">Projektin tuntiarvioiden mallissa on käytettävä Microsoft Power Query for Exceliä seuraavien toimintojen päivittämiseen:</span><span class="sxs-lookup"><span data-stu-id="dc8ee-132">In the project hour estimates template, you must use Microsoft Power Query for Excel to complete these tasks:</span></span>

- <span data-ttu-id="dc8ee-133">Määritettävää oletusennustemallin tunnusta käytetään, kun integrointi luo uusi tuntiennusteita.</span><span class="sxs-lookup"><span data-stu-id="dc8ee-133">Set the default forecast model ID that will be used when the integration creates new hour forecasts.</span></span>
- <span data-ttu-id="dc8ee-134">Sellaisten tehtävän resurssikohteisten tietueiden suodattaminen pois, jotka aiheuttavat tuntiennusteisiin tapahtuvan integroinnin epäonnistumisen.</span><span class="sxs-lookup"><span data-stu-id="dc8ee-134">Filter out any resource-specific records in the task that will fail the integration into hour forecasts.</span></span>
- <span data-ttu-id="dc8ee-135">Tyhjien tapahtumaluokkarivien suodattaminen pois.</span><span class="sxs-lookup"><span data-stu-id="dc8ee-135">Filter out any empty transaction category rows.</span></span> <span data-ttu-id="dc8ee-136">Jos suodatusta ei tehdä valmiiksi, tuloksena voi olla virheellisiä tuntiennusteita</span><span class="sxs-lookup"><span data-stu-id="dc8ee-136">Failure to complete this task might result in incorrect hour forecasts.</span></span>

#### <a name="set-the-default-forecast-model-id"></a><span data-ttu-id="dc8ee-137">Aseta ennustemallin oletusarvon tunnus.</span><span class="sxs-lookup"><span data-stu-id="dc8ee-137">Set the default forecast model ID</span></span>

<span data-ttu-id="dc8ee-138">Voit päivittää malliin oletusennustemallin tunnuksen avaamalla määrityksen napsauttamalla **Yhdistä**-nuolta.</span><span class="sxs-lookup"><span data-stu-id="dc8ee-138">To update the default forecast model ID in the template, click the **Map** arrow to open the mapping.</span></span> <span data-ttu-id="dc8ee-139">Valitse sitten **Kyselyn ja suodatuksen lisäasetukset** -linkki.</span><span class="sxs-lookup"><span data-stu-id="dc8ee-139">Then select the **Advanced Query and Filtering** link.</span></span>

- <span data-ttu-id="dc8ee-140">Jos käytät projektin tuntiarvioita (PSA:sta Fin and Opsiin) -oletusmallia, valitse **Lisätty ehto** **Käytetyt vaiheet** -listassa.</span><span class="sxs-lookup"><span data-stu-id="dc8ee-140">If you're using the default Project hour estimates (PSA to Fin and Ops) template, select the **Inserted Condition** in the list of **Applied Steps**.</span></span> <span data-ttu-id="dc8ee-141">Vaihda **Toiminto**-merkinnän **O\_forecast** tilalle sen ennustemallin tunnuksen nimi, jota käytetään integraatiossa.</span><span class="sxs-lookup"><span data-stu-id="dc8ee-141">In the **Function** entry, replace **O\_forecast** with the name of the forecast model ID that should be used with the integration.</span></span> <span data-ttu-id="dc8ee-142">Oletusmallin ennustemalli tunnus on saatu esittelytiedoista.</span><span class="sxs-lookup"><span data-stu-id="dc8ee-142">The default template has a forecast model ID from the demo data.</span></span>
- <span data-ttu-id="dc8ee-143">Jos luot uuden mallin, sinun on lisättävä tämä sarake.</span><span class="sxs-lookup"><span data-stu-id="dc8ee-143">If you're creating a new template, you must add this column.</span></span> <span data-ttu-id="dc8ee-144">Valitse Power Queryssä **Lisää ehtosarake** ja anna uudelle sarakkeelle nimi, kuten **Mallin tunnus**.</span><span class="sxs-lookup"><span data-stu-id="dc8ee-144">In Power Query, select **Add Conditional Column**, and enter a name for the new column, such as **ModelID**.</span></span> <span data-ttu-id="dc8ee-145">Anna sarakkeelle ehto, jonka mukaan jos projektitehtävä ei ole tyhjäarvo, niin \<anna ennustemallin tunnus\>; muutoin tyhjäarvo.</span><span class="sxs-lookup"><span data-stu-id="dc8ee-145">Enter the condition for the column, where, if Project task is not null, then \<enter the forecast model ID\>; else null.</span></span>

#### <a name="filter-out-resource-specific-records"></a><span data-ttu-id="dc8ee-146">Resurssikohtaisten tietueiden suodattaminen</span><span class="sxs-lookup"><span data-stu-id="dc8ee-146">Filter out resource-specific records</span></span>

<span data-ttu-id="dc8ee-147">Projektin tuntiarviot (PSA:sta Fin and Opsiin) -mallissa on oletussuodatin, joka poistaa kaikki resurssikohtaiset tietueet.</span><span class="sxs-lookup"><span data-stu-id="dc8ee-147">The Project hour estimates (PSA to Fin and Ops) template has a default filter that removes any resource-specific records.</span></span> <span data-ttu-id="dc8ee-148">Jos luot oman mallin, tämä suodatin on lisättävä.</span><span class="sxs-lookup"><span data-stu-id="dc8ee-148">If you create your own template, you must add this filter.</span></span> <span data-ttu-id="dc8ee-149">Valitse **Advanced Query and Filtering** -linkki suodattaaksesi **msdyn\_islinetask** -sarakkesta niin, että vain **Epätosi** -asiakirjat ovat mukana.</span><span class="sxs-lookup"><span data-stu-id="dc8ee-149">Select the **Advanced Query and Filtering** link to filter on the **msdyn\_islinetask** column so that only **False** records are included.</span></span>

#### <a name="filter-out-empty-transaction-category-rows"></a><span data-ttu-id="dc8ee-150">Tyhjien tapahtumaluokkarivien suodattaminen</span><span class="sxs-lookup"><span data-stu-id="dc8ee-150">Filter out empty transaction category rows</span></span>

<span data-ttu-id="dc8ee-151">Kaikki tyhjiä tapahtumaluokkia sisältävät rivit poistava suodatin on lisättävä.</span><span class="sxs-lookup"><span data-stu-id="dc8ee-151">You must add a filter to remove any rows that have empty transaction categories.</span></span> <span data-ttu-id="dc8ee-152">Tämä tehtävä vaaditaan riippumatta siitä, käytätkö oletusmallia vai luotko oman mallin.</span><span class="sxs-lookup"><span data-stu-id="dc8ee-152">This task is required, regardless of whether you're using the default template or creating your own template.</span></span> <span data-ttu-id="dc8ee-153">Tämä suodatin poistaa kaikki Project Service Automationin yhteenvetorivit, joiden vuoksi Finance and Operationsin tuntiennusteet voisivat olla virheellisiä.</span><span class="sxs-lookup"><span data-stu-id="dc8ee-153">This filter removes any summary rows from Project Service Automation that might cause the hour forecasts in Finance and Operations to be incorrect.</span></span> <span data-ttu-id="dc8ee-154">Valitse **Advanced Query and Filtering** -linkki poissuodattaaksesi tyhjäarvoiset tietueet **msdyn\_transactioncategory\_value** -sarakkeessa.</span><span class="sxs-lookup"><span data-stu-id="dc8ee-154">Select **Advanced Query and Filtering** link to filter out null records in the **msdyn\_transactioncategory\_value** column.</span></span>

### <a name="template-mapping-in-data-integration"></a><span data-ttu-id="dc8ee-155">Mallin yhdistäminen tietojen integroinnin yhteydessä</span><span class="sxs-lookup"><span data-stu-id="dc8ee-155">Template mapping in Data integration</span></span>

<span data-ttu-id="dc8ee-156">Seuraavassa kuvassa on esimerkki mallitehtävän yhdistämisestä tietojen integroinnin yhteydessä.</span><span class="sxs-lookup"><span data-stu-id="dc8ee-156">The following illustration shows an example of the template task mapping in Data integration.</span></span> <span data-ttu-id="dc8ee-157">Yhdistämismääritys näyttää Project Service Automationista Finance and Operationsiin synkronoitavan kentän tiedot.</span><span class="sxs-lookup"><span data-stu-id="dc8ee-157">The mapping shows the field information that will be synchronized from Project Service Automation to Finance and Operations.</span></span>

<span data-ttu-id="dc8ee-158">[![Mallin yhdistäminen](./media/ProjectHourEstimatesMapping.jpg)](./media/ProjectHourEstimatesMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="dc8ee-158">[![Template mapping](./media/ProjectHourEstimatesMapping.jpg)](./media/ProjectHourEstimatesMapping.jpg)</span></span>

## <a name="project-expense-estimates"></a><span data-ttu-id="dc8ee-159">Projektin kustannusarviot</span><span class="sxs-lookup"><span data-stu-id="dc8ee-159">Project expense estimates</span></span>

### <a name="template-and-tasks"></a><span data-ttu-id="dc8ee-160">Malli ja tehtävät</span><span class="sxs-lookup"><span data-stu-id="dc8ee-160">Template and tasks</span></span>

<span data-ttu-id="dc8ee-161">Seuraavaa mallia ja sen taustalla olevia tehtäviä käytetään synkronoimaan projektin kuluarviot Project Service Automationista Finance and Operationsiin:</span><span class="sxs-lookup"><span data-stu-id="dc8ee-161">The following template and underlying tasks are used to synchronize project expense estimates from Project Service Automation to Finance and Operations:</span></span>

- <span data-ttu-id="dc8ee-162">**Mallin nimi tietojen integroinnissa:** Projektin kuluarviot (PSA:sta Fin and Opsiin)</span><span class="sxs-lookup"><span data-stu-id="dc8ee-162">**Name of the template in Data integration:** Project expense estimates (PSA to Fin and Ops)</span></span>
- <span data-ttu-id="dc8ee-163">**Projektin tehtävien nimi:**</span><span class="sxs-lookup"><span data-stu-id="dc8ee-163">**Name of the tasks in the project:**</span></span>

    - <span data-ttu-id="dc8ee-164">Tapahtumasuhteet</span><span class="sxs-lookup"><span data-stu-id="dc8ee-164">Transaction relationships</span></span> 
    - <span data-ttu-id="dc8ee-165">Kuluarviot</span><span class="sxs-lookup"><span data-stu-id="dc8ee-165">Expense estimates</span></span>

### <a name="entity-set"></a><span data-ttu-id="dc8ee-166">Yksikköjoukko</span><span class="sxs-lookup"><span data-stu-id="dc8ee-166">Entity set</span></span>

| <span data-ttu-id="dc8ee-167">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="dc8ee-167">Project Service Automation</span></span> | <span data-ttu-id="dc8ee-168">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="dc8ee-168">Finance and Operations</span></span>                                   |
|----------------------------|----------------------------------------------------------|
| <span data-ttu-id="dc8ee-169">Tapahtumayhteydet</span><span class="sxs-lookup"><span data-stu-id="dc8ee-169">Transaction Connections</span></span>    | <span data-ttu-id="dc8ee-170">Projektin tapahtumasuhteiden integrointiyksikkö</span><span class="sxs-lookup"><span data-stu-id="dc8ee-170">Integration entity for project transaction relationships</span></span> |
| <span data-ttu-id="dc8ee-171">Arviorivit</span><span class="sxs-lookup"><span data-stu-id="dc8ee-171">Estimate Lines</span></span>             | <span data-ttu-id="dc8ee-172">Projektin kuluarvioiden integrointiyksikkö</span><span class="sxs-lookup"><span data-stu-id="dc8ee-172">Integration entity for project expense estimates</span></span>         |

### <a name="entity-flow"></a><span data-ttu-id="dc8ee-173">Yksikön työnkulku</span><span class="sxs-lookup"><span data-stu-id="dc8ee-173">Entity flow</span></span>

<span data-ttu-id="dc8ee-174">Projektin kuluarvioita hallitaan Project Service Automationissa ja ne synkronoidaan Finance and Operationsiin projektin kuluennusteisiin.</span><span class="sxs-lookup"><span data-stu-id="dc8ee-174">Project expense estimates are managed in Project Service Automation, and they are synchronized to Finance and Operations as project expense forecasts.</span></span>

### <a name="prerequisites"></a><span data-ttu-id="dc8ee-175">Edellytykset</span><span class="sxs-lookup"><span data-stu-id="dc8ee-175">Prerequisites</span></span>

<span data-ttu-id="dc8ee-176">Projektin, projektitehtävien ja projektin kuluarvion tapahtumaluokat on synkronoitava, ennen kuin projektin kuluarviot voidaan synkronoida.</span><span class="sxs-lookup"><span data-stu-id="dc8ee-176">Before synchronization of project expense estimates can occur, you must synchronize projects, project tasks, and project expense transaction categories.</span></span>

### <a name="power-query"></a><span data-ttu-id="dc8ee-177">Power Query</span><span class="sxs-lookup"><span data-stu-id="dc8ee-177">Power Query</span></span>

<span data-ttu-id="dc8ee-178">Projektin kuluarviomallissa on käytettävä Power Query for Exceliä seuraavien toimintojen päivittämiseen:</span><span class="sxs-lookup"><span data-stu-id="dc8ee-178">In the project expense estimates template, you must use Power Query to complete the following tasks:</span></span>

- <span data-ttu-id="dc8ee-179">Vain kuluarviorivien tietueet sisällyttävä suodatus.</span><span class="sxs-lookup"><span data-stu-id="dc8ee-179">Filter to include only expense estimate line records.</span></span>
- <span data-ttu-id="dc8ee-180">Määritettävää oletusennustemallin tunnusta käytetään, kun integrointi luo uusi tuntiennusteita.</span><span class="sxs-lookup"><span data-stu-id="dc8ee-180">Set the default forecast model ID that will be used when the integration creates new hour forecasts.</span></span>
- <span data-ttu-id="dc8ee-181">Laskutustyyppien muuntaminen.</span><span class="sxs-lookup"><span data-stu-id="dc8ee-181">Transform the billing types.</span></span>
- <span data-ttu-id="dc8ee-182">Tapahtumatyyppien muuntaminen.</span><span class="sxs-lookup"><span data-stu-id="dc8ee-182">Transform the transaction types.</span></span>

#### <a name="filter-to-include-only-expense-estimate-lines"></a><span data-ttu-id="dc8ee-183">Vain kuluarviorivit sisällyttävä suodatus</span><span class="sxs-lookup"><span data-stu-id="dc8ee-183">Filter to include only expense estimate lines</span></span>

<span data-ttu-id="dc8ee-184">Projektin kuluarviot (PSA:sta Fin and Opsiin) -mallissa oletussuodatin, joka sisällyttää integraatioon vain kulurivit.</span><span class="sxs-lookup"><span data-stu-id="dc8ee-184">The Project expense estimates (PSA to Fin and Ops) template has a default filter that includes only expense lines in the integration.</span></span> <span data-ttu-id="dc8ee-185">Jos luot oman mallin, tämä suodatin on lisättävä.</span><span class="sxs-lookup"><span data-stu-id="dc8ee-185">If you create your own template, you must add this filter.</span></span> <span data-ttu-id="dc8ee-186">Valitse **Tapahtumasuhde**-tehtävä ja napsauta **Yhdistä**-nuolta avataksesi kartoituksen.</span><span class="sxs-lookup"><span data-stu-id="dc8ee-186">Select the **Transaction relationships** task, and then click the **Map** arrow to open the mapping.</span></span> <span data-ttu-id="dc8ee-187">Valitse **Kyselyn ja suodatuksen lisäasetukset** -linkki.</span><span class="sxs-lookup"><span data-stu-id="dc8ee-187">Select the **Advanced Query and Filtering** link.</span></span> <span data-ttu-id="dc8ee-188">Suodata **msdyn\_transactiontype1** -sarake niin, että se sisältää vain **msdyn\_estimateline** -tiedoston.</span><span class="sxs-lookup"><span data-stu-id="dc8ee-188">Filter the **msdyn\_transactiontype1** column so that it includes only **msdyn\_estimateline**.</span></span>

#### <a name="set-the-default-forecast-model-id"></a><span data-ttu-id="dc8ee-189">Aseta ennustemallin oletusarvon tunnus.</span><span class="sxs-lookup"><span data-stu-id="dc8ee-189">Set the default forecast model ID</span></span>

<span data-ttu-id="dc8ee-190">Voit päivittää malliin oletusennustemallin tunnuksen avaamalla **Kuluarvio**-tehtävän ja sitten napsauttaa **Yhdistä**-nuolta avataksesi kartoituksen.</span><span class="sxs-lookup"><span data-stu-id="dc8ee-190">To update the default forecast model ID in the template, select the **Expense estimates** task, and then click the **Map** arrow to open the mapping.</span></span> <span data-ttu-id="dc8ee-191">Valitse **Kyselyn ja suodatuksen lisäasetukset** -linkki.</span><span class="sxs-lookup"><span data-stu-id="dc8ee-191">Select the **Advanced Query and Filtering** link.</span></span>

- <span data-ttu-id="dc8ee-192">Jos käytät projektin kuluarvioiden oletusmallia (PSA:sta Fin and Opsiin), Power Queryssä, valitse ensimmäinen **Lisätty ehto** **Käytetyt vaiheet** -osassa.</span><span class="sxs-lookup"><span data-stu-id="dc8ee-192">If you're using the default Project expense estimates (PSA to Fin and Ops) template, in Power Query, select the first **Inserted Condition** from the **Applied Steps** section.</span></span> <span data-ttu-id="dc8ee-193">Vaihda **Toiminto**-merkinnän **O\_forecast** tilalle sen ennustemallin tunnuksen nimi, jota käytetään integraatiossa.</span><span class="sxs-lookup"><span data-stu-id="dc8ee-193">In the **Function** entry, replace **O\_forecast** with the name of the forecast model ID that should be used with the integration.</span></span> <span data-ttu-id="dc8ee-194">Oletusmallin ennustemalli tunnus on saatu esittelytiedoista.</span><span class="sxs-lookup"><span data-stu-id="dc8ee-194">The default template has a forecast model ID from the demo data.</span></span>
- <span data-ttu-id="dc8ee-195">Jos luot uuden mallin, sinun on lisättävä tämä sarake.</span><span class="sxs-lookup"><span data-stu-id="dc8ee-195">If you're creating a new template, you must add this column.</span></span> <span data-ttu-id="dc8ee-196">Valitse Power Queryssä **Lisää ehtosarake** ja anna uudelle sarakkeelle nimi, kuten **Mallin tunnus**.</span><span class="sxs-lookup"><span data-stu-id="dc8ee-196">In Power Query, select **Add Conditional Column**, and enter a name for the new column, such as **ModelID**.</span></span> <span data-ttu-id="dc8ee-197">Anna sarakkeelle ehto, jonka mukaan jos arviorivin tunnus ei ole tyhjäarvo, niin \<anna ennustemallin tunnus\>; muutoin tyhjäarvo.</span><span class="sxs-lookup"><span data-stu-id="dc8ee-197">Enter the condition for the column, where, if Estimate line ID is not null, then \<enter the forecast model ID\>; else null.</span></span>

#### <a name="transform-the-billing-types"></a><span data-ttu-id="dc8ee-198">Laskutustyyppien muuntaminen</span><span class="sxs-lookup"><span data-stu-id="dc8ee-198">Transform the billing types</span></span>

<span data-ttu-id="dc8ee-199">Projektin kuluarviot (PSA to Fin and Ops) -malliin kuuluva ehtosarake, joka muuntaa Project Service Automationista vastaanotetut laskutustyypit integroinnin aikana.</span><span class="sxs-lookup"><span data-stu-id="dc8ee-199">The Project expense estimates (PSA to Fin and Ops) template includes a conditional column that is used to transform the billing types that are received from Project Service Automation during the integration.</span></span> <span data-ttu-id="dc8ee-200">Jos luot oman mallin, tämä ehtosarake on lisättävä.</span><span class="sxs-lookup"><span data-stu-id="dc8ee-200">If you create your own template, you must add this conditional column.</span></span> <span data-ttu-id="dc8ee-201">Valitse **kyselyn ja suodatuksen** linkki ja valitse sitten **Lisää ehtosarake**.</span><span class="sxs-lookup"><span data-stu-id="dc8ee-201">Select the **Advanced Query and Filtering** link and then select **Add Conditional Column**.</span></span> <span data-ttu-id="dc8ee-202">Anna sarakkeelle uusi nimi, kuten **Laskutustyyppi**.</span><span class="sxs-lookup"><span data-stu-id="dc8ee-202">Enter a name for the new column, such as **BillingType**.</span></span> <span data-ttu-id="dc8ee-203">Anna sitten seuraava ehto:</span><span class="sxs-lookup"><span data-stu-id="dc8ee-203">Then enter the following condition:</span></span>

<span data-ttu-id="dc8ee-204">Jos **msdyn\_billingtype** = 192350000, silloin **NonChargeable**</span><span class="sxs-lookup"><span data-stu-id="dc8ee-204">If **msdyn\_billingtype** = 192350000, then **NonChargeable**</span></span>  
<span data-ttu-id="dc8ee-205">Jos **msdyn\_billingtype** = 192350001, silloin **Chargeable**</span><span class="sxs-lookup"><span data-stu-id="dc8ee-205">else if **msdyn\_billingtype** = 192350001, then **Chargeable**</span></span>  
<span data-ttu-id="dc8ee-206">Jos **msdyn\_billingtype** = 192350002, silloin **Complimentary**</span><span class="sxs-lookup"><span data-stu-id="dc8ee-206">else if **msdyn\_billingtype** = 192350002, then **Complimentary**</span></span>  
<span data-ttu-id="dc8ee-207">muuta **NotAvailable**</span><span class="sxs-lookup"><span data-stu-id="dc8ee-207">else **NotAvailable**</span></span>

#### <a name="transform-the-transaction-types"></a><span data-ttu-id="dc8ee-208">Tapahtumatyyppien muuntaminen</span><span class="sxs-lookup"><span data-stu-id="dc8ee-208">Transform the transaction types</span></span>

<span data-ttu-id="dc8ee-209">Projektin kuluarviot (PSA to Fin and Ops) -malliin kuuluva ehtosarake, joka muuntaa Project Service Automationista vastaanotetut tapahtumatyypit integroinnin aikana.</span><span class="sxs-lookup"><span data-stu-id="dc8ee-209">The Project expense estimates (PSA to Fin and Ops) template includes a conditional column that is used to transform the transaction types that are received from Project Service Automation during the integration.</span></span> <span data-ttu-id="dc8ee-210">Jos luot oman mallin, tämä ehtosarake on lisättävä.</span><span class="sxs-lookup"><span data-stu-id="dc8ee-210">If you create your own template, you must add this conditional column.</span></span> <span data-ttu-id="dc8ee-211">Valitse **kyselyn ja suodatuksen** linkki ja valitse sitten **Lisää ehtosarake**.</span><span class="sxs-lookup"><span data-stu-id="dc8ee-211">Select the **Advanced Query and Filtering** link and then select **Add Conditional Column**.</span></span> <span data-ttu-id="dc8ee-212">Anna sarakkeelle uusi nimi, kuten **Tapahtumatyyppi**.</span><span class="sxs-lookup"><span data-stu-id="dc8ee-212">Enter a name for the new column, such as **TransactionType**.</span></span> <span data-ttu-id="dc8ee-213">Anna sitten seuraava ehto:</span><span class="sxs-lookup"><span data-stu-id="dc8ee-213">Then enter the following condition:</span></span>

<span data-ttu-id="dc8ee-214">Jos **msdyn\_transactiontypecode** = 192350000, silloin **Cost**</span><span class="sxs-lookup"><span data-stu-id="dc8ee-214">If **msdyn\_transactiontypecode** = 192350000, then **Cost**</span></span>  
<span data-ttu-id="dc8ee-215">jos **msdyn\_transactiontypecode** = 192350005, then **Sales**</span><span class="sxs-lookup"><span data-stu-id="dc8ee-215">else if **msdyn\_transactiontypecode** = 192350005, then **Sales**</span></span>  
<span data-ttu-id="dc8ee-216">else **null**</span><span class="sxs-lookup"><span data-stu-id="dc8ee-216">else **null**</span></span>

### <a name="template-mapping-in-data-integration"></a><span data-ttu-id="dc8ee-217">Mallin yhdistäminen tietojen integroinnin yhteydessä</span><span class="sxs-lookup"><span data-stu-id="dc8ee-217">Template mapping in Data integration</span></span>

<span data-ttu-id="dc8ee-218">Seuraavissa kuvissa on esimerkkejä mallitehtävän yhdistämisistä tietojen integroinnin yhteydessä.</span><span class="sxs-lookup"><span data-stu-id="dc8ee-218">The following illustrations show examples of the template task mappings in Data integration.</span></span> <span data-ttu-id="dc8ee-219">Yhdistämismääritys näyttää Project Service Automationista Finance and Operationsiin synkronoitavan kentän tiedot.</span><span class="sxs-lookup"><span data-stu-id="dc8ee-219">The mapping shows the field information that will be synchronized from Project Service Automation to Finance and Operations.</span></span>

<span data-ttu-id="dc8ee-220">[![Mallin yhdistäminen](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="dc8ee-220">[![Template mapping](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)</span></span>

<span data-ttu-id="dc8ee-221">[![Mallin yhdistäminen](./media/ExpenseEstimatesMapping.jpg)](./media/ExpenseEstimatesMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="dc8ee-221">[![Template mapping](./media/ExpenseEstimatesMapping.jpg)](./media/ExpenseEstimatesMapping.jpg)</span></span>

