---
title: Projektin kululuokkien synkronointi Project Service Automationista
description: "Tässä ohjeaiheessa käsitellään malleja ja taustalla olevia tehtäviä, joilla projektin kululuokat synkronoidaan Dynamics 365 for Finance and Operationsin ja Microsoft Dynamics 365 for Project Service Automationin välillä."
author: KimANelson
manager: AnnBe
ms.date: 04/02/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 8.0.0
ms.translationtype: HT
ms.sourcegitcommit: bd8feff598cf80ca675c7d2b5dda636799b19e29
ms.openlocfilehash: dcdb9b6ec296073d511c069cdceb1c61080b6d97
ms.contentlocale: fi-fi
ms.lasthandoff: 05/29/2018

---

# <a name="synchronize-project-expense-categories-between-finance-and-operations-and-project-service-automation"></a><span data-ttu-id="280e8-103">Projektin kululuokkien synkronointi Finance and Operationsin ja Project Service Automationin välillä</span><span class="sxs-lookup"><span data-stu-id="280e8-103">Synchronize project expense categories between Finance and Operations and Project Service Automation</span></span>

<span data-ttu-id="280e8-104">Tässä ohjeaiheessa käsitellään malleja ja taustalla olevia tehtäviä, joilla projektin kululuokat synkronoidaan Dynamics 365 for Finance and Operationsin ja Microsoft Dynamics 365 for Project Service Automationin välillä.</span><span class="sxs-lookup"><span data-stu-id="280e8-104">This topic describes the templates and underlying tasks that are used to synchronize project expense categories between Microsoft Dynamics 365 for Finance and Operations and Dynamics 365 for Project Service Automation.</span></span>

> [!NOTE]
> <span data-ttu-id="280e8-105">Projektitehtävien integrointi, kulutapahtumaluokat, tuntiarviot, kuluarviot ja toiminnon lukitseminen ovat käytössä Dynamics 365 for Finance and Operationsin versiossa 8.0.</span><span class="sxs-lookup"><span data-stu-id="280e8-105">Project tasks integration, expense transaction categories, hour estimates, expense estimates, and functionality locking is available in Dynamics 365 for Finance and Operations version 8.0.</span></span>

## <a name="data-flow-for-project-service-automation-and-finance-and-operations"></a><span data-ttu-id="280e8-106">Project Service Automationin ja Finance and Operationsin tiedonkulku</span><span class="sxs-lookup"><span data-stu-id="280e8-106">Data flow for Project Service Automation and Finance and Operations</span></span>

<span data-ttu-id="280e8-107">Project Service Automationin ja Finance and Operationsin välinen integrointiratkaisu synkronoi Project Service Automationin ja Finance and Operationsin esiintymien tiedot tietojen integrointiominaisuudella.</span><span class="sxs-lookup"><span data-stu-id="280e8-107">The Project Service Automation and Finance and Operations integration solution uses the Data integration feature to synchronize data across instances of Project Service Automation and Finance and Operations.</span></span> <span data-ttu-id="280e8-108">Tietojen integrointiominaisuudessa käytettävissä olevat integrointimallit mahdollistavat projektin kulutapahtumaluokkia koskevan tiedonkulun Project Service Automationin ja Finance and Operationsin välillä.</span><span class="sxs-lookup"><span data-stu-id="280e8-108">The integration templates that are available with the Data integration feature enables the flow of data about project expense transaction categories between Finance and Operations and Project Service Automation.</span></span>

<span data-ttu-id="280e8-109">Jos projektin kululuokkia hallitaan Finance and Operationsissa, integrointi tapahtuu ensin Finance and Operationsista Project Service Automationiin. Sen jälkeen projektin kululuokkien integrointitunnukset päivitetään synkronoimalla Project Service Automationista Finance and Operationsiin.</span><span class="sxs-lookup"><span data-stu-id="280e8-109">If the project expense categories are mastered in Finance and Operations, the integration flow is first from Finance and Operations to Project Service Automation, and then updating the project expense categories integration IDs by synchronizing from Project Service Automation to Finance and Operations.</span></span>

<span data-ttu-id="280e8-110">Jos projektin kululuokkia hallitaan Project Service Automationista, integrointi tapahtuu ensin Project Service Automationista Finance and Operationsiin.</span><span class="sxs-lookup"><span data-stu-id="280e8-110">If the project expense categories are mastered in Project Service Automation, the integration flow is first from Project Service Automation to Finance and Operations.</span></span> <span data-ttu-id="280e8-111">Projektiluokkien on oltava määritettynä Finance and Operationsissa ennen synkronointia Project Service Automationista.</span><span class="sxs-lookup"><span data-stu-id="280e8-111">The project categories must already be configured in Finance and Operations prior to the synchronization from Project Service Automation.</span></span> <span data-ttu-id="280e8-112">Voit tämän jälkeen tehdä synkronoinnin Finance and Operationsista takaisin Project Service Automationiin ja sitten uudelleen Project Service Automationista Finance and Operationsiin.</span><span class="sxs-lookup"><span data-stu-id="280e8-112">Then synchronize from Finance and Operations back to Project Service Automation and then from Project Service Automation to Finance and Operations again.</span></span> <span data-ttu-id="280e8-113">Näin varmistetaan, että luokat linkitetään ja ettei kaksoiskappaleita luoda.</span><span class="sxs-lookup"><span data-stu-id="280e8-113">This ensures the categories are linked and duplicates are not created.</span></span>

> [!NOTE]
> <span data-ttu-id="280e8-114">Yleensä projektin kululuokkia hallitaan Finance and Operationsissa.</span><span class="sxs-lookup"><span data-stu-id="280e8-114">Typically, the project expense categories will be mastered in Finance and Operations.</span></span> <span data-ttu-id="280e8-115">Mikäli näin ei tehdä tai jos olet jo luonut kululuokat Project Service Automationin, sinun on synkronoitava ensin käyttämällä projektin kulutapahtumaluokkia (PSA:sta Fin and Opsiin) ja sitten käyttämällä projektin kulutapahtumaluokkia (Fin and Opsista PSA:han).</span><span class="sxs-lookup"><span data-stu-id="280e8-115">If that is not your situation, or you already have expense categories created in Project Service Automation, you must first sync using the Project expense transaction categories (PSA to Fin and Ops) and then sync using Project expense transaction categories (Fin and Ops to PSA).</span></span> <span data-ttu-id="280e8-116">Tämän jälkeen on tehtävä vielä kerran synkronointi PSA:sta Fin and Opsiin.</span><span class="sxs-lookup"><span data-stu-id="280e8-116">You should then run the sync from PSA to Fin and Ops one more time.</span></span>

> <span data-ttu-id="280e8-117">Jos synkronointi tehdään ensin Project Service Automationista, projektiluokkien on oltava jo määritettyinä Finance and Operationsissa. Lisäksi Project Service Automationin tapahtumaluokkien kanssa synkronoitavien projektiluokkien määrityksen on oltava **Käytössä kirjauskansioissa**.</span><span class="sxs-lookup"><span data-stu-id="280e8-117">If synchronizing first from Project Service Automation, the project categories must already be set up in Finance and Operations and any project categories that need to be synched with the Project Service Automation transaction categories must be set up to be **Active in journals**.</span></span>

<span data-ttu-id="280e8-118">Seuraava kuva ilmaisee, miten tiedot synkronoidaan Project Service Automationin ja Finance and Operationsin välillä.</span><span class="sxs-lookup"><span data-stu-id="280e8-118">The following illustration shows how the data is synchronized between Project Service Automation and Finance and Operations.</span></span>

<span data-ttu-id="280e8-119">[![Project Service Automationin ja Finance and Operationsin välisen integroinnin tiedonkulku](./media/ProjectExpenseCategoriesFlow.png)](./media/ProjectExpenseCategoriesFlow.png)</span><span class="sxs-lookup"><span data-stu-id="280e8-119">[![Data flow for Project Service Automation integration with Finance and Operations](./media/ProjectExpenseCategoriesFlow.png)](./media/ProjectExpenseCategoriesFlow.png)</span></span>


## <a name="templates-and-tasks"></a><span data-ttu-id="280e8-120">Mallit ja tehtävät</span><span class="sxs-lookup"><span data-stu-id="280e8-120">Templates and tasks</span></span>

<span data-ttu-id="280e8-121">Saat käytettävissä olevat mallit käyttöösi valitsemalla Microsoft PowerAppsin hallintakeskuksessa **Projektit**. Valitse sitten julkiset mallit valitsemalla oikeassa yläkulmassa **Uusi projekti**.</span><span class="sxs-lookup"><span data-stu-id="280e8-121">To access available templates, in the Microsoft PowerApps Admin Center, select **Projects**, and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="280e8-122">Seuraavaa mallia ja sen taustalla olevaa tehtävää käytetään synkronoimaan projektin kululuokat Finance and Operationsista Project Service Automationiin:</span><span class="sxs-lookup"><span data-stu-id="280e8-122">The following template and underlying task is used to synchronize project expense categories from Finance and Operations to Project Service Automation:</span></span>

-  <span data-ttu-id="280e8-123">**Mallin nimi tietojen integroinnissa:** projektin kulutapahtumaluokat (Fin and Opsista PSA:han)</span><span class="sxs-lookup"><span data-stu-id="280e8-123">**Name of the template in Data integration:** Project expense transaction categories (Fin and Ops to PSA)</span></span>
-  <span data-ttu-id="280e8-124">**Projektin tehtävän nimi:** luokkien synkronointi PSA:han</span><span class="sxs-lookup"><span data-stu-id="280e8-124">**Name of the task in the project:** Sync categories to PSA</span></span>

## <a name="entity-set"></a><span data-ttu-id="280e8-125">Yksikköjoukko</span><span class="sxs-lookup"><span data-stu-id="280e8-125">Entity set</span></span>

| <span data-ttu-id="280e8-126">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="280e8-126">Finance and Operations</span></span>               | <span data-ttu-id="280e8-127">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="280e8-127">Project Service Automation</span></span>    |
|--------------------------------------|-------------------------------|
| <span data-ttu-id="280e8-128">Luokkien integrointiyksikkö</span><span class="sxs-lookup"><span data-stu-id="280e8-128">Integration entity for categories</span></span>    | <span data-ttu-id="280e8-129">Tapahtumaluokat</span><span class="sxs-lookup"><span data-stu-id="280e8-129">Transaction categories</span></span>        |

## <a name="entity-flow"></a><span data-ttu-id="280e8-130">Yksikön työnkulku</span><span class="sxs-lookup"><span data-stu-id="280e8-130">Entity flow</span></span>

<span data-ttu-id="280e8-131">Projektin kululuokkia tietoja hallitaan Finance and Operationsissa ja ne synkronoidaan Project Service Automationiin tapahtumaluokkina.</span><span class="sxs-lookup"><span data-stu-id="280e8-131">Project expense categories are managed in Finance and Operations, and they are synchronized to Project Service Automation as transaction categories.</span></span>

## <a name="power-query"></a><span data-ttu-id="280e8-132">Power Query</span><span class="sxs-lookup"><span data-stu-id="280e8-132">Power Query</span></span>

<span data-ttu-id="280e8-133">Tapahtumaluokan laskutustyyppi on määritettävä Microsoft Power Queryllä, kun synkronointi tehdään Project Service Automationiin.</span><span class="sxs-lookup"><span data-stu-id="280e8-133">You must use Microsoft Power Query to set the billing type on the transaction category when synchronizing to Project Service Automation.</span></span> <span data-ttu-id="280e8-134">Projektin kulutapahtumaluokkien mallissa (Fin and Opsista PSA:han) on valmiina oletussarake ja yhdistämismääritys.</span><span class="sxs-lookup"><span data-stu-id="280e8-134">The Project expense transaction categories (Fin and Ops to PSA) template has a default column and mapping already provided.</span></span> <span data-ttu-id="280e8-135">Jos luot oman mallin, ehtosarake on lisättävä Power Queryssä.</span><span class="sxs-lookup"><span data-stu-id="280e8-135">If you create your own template, you must add a conditional column in Power Query.</span></span>
- <span data-ttu-id="280e8-136">Avaa kyselyn ja suodatuksen lisäasetuslomake, kun yhdistät projektin kululuokkatehtävää.</span><span class="sxs-lookup"><span data-stu-id="280e8-136">Open the Advance Query and Filtering form from within the mapping of project expense categories task.</span></span>
- <span data-ttu-id="280e8-137">Valitse **Lisää ehtosarake**.</span><span class="sxs-lookup"><span data-stu-id="280e8-137">Select **Add Conditional Column**.</span></span>
- <span data-ttu-id="280e8-138">Anna sarakkeelle uusi nimi, kuten Laskutustyyppi.</span><span class="sxs-lookup"><span data-stu-id="280e8-138">Give the new column a name, such as BillingType.</span></span>
- <span data-ttu-id="280e8-139">Anna seuraava ehto: jos **CATEGORYID ei sama kuin tyhjäarvo sitten 19235001, muuten tyhjäarvo**.</span><span class="sxs-lookup"><span data-stu-id="280e8-139">Enter the following condition: if **CATEGORYID not equal to null then 19235001, Otherwise null**.</span></span>
- <span data-ttu-id="280e8-140">Valitse sarakkeessa **OK**.</span><span class="sxs-lookup"><span data-stu-id="280e8-140">Click **OK** on the column.</span></span>
- <span data-ttu-id="280e8-141">Varmista, että yhdistät tämän uuden sarakkeen yhdistämismäärityssivulle.</span><span class="sxs-lookup"><span data-stu-id="280e8-141">Be sure to map this new column in the mapping page.</span></span>

<span data-ttu-id="280e8-142">Seuraavassa kuvassa on esimerkki mallitehtävän yhdistämisestä tietojen integroinnin yhteydessä.</span><span class="sxs-lookup"><span data-stu-id="280e8-142">The following illustration shows an example of the template task mapping in Data integration.</span></span> <span data-ttu-id="280e8-143">Yhdistämismääritys näyttää Finance and Operationsista Project Service Automationiin synkronoitavan kentän tiedot.</span><span class="sxs-lookup"><span data-stu-id="280e8-143">The mapping shows the field information that will be synchronized from Finance and Operations to Project Service Automation.</span></span>

<span data-ttu-id="280e8-144">[![Mallin yhdistäminen](./media/ProjectExpenseCategoriesToPSAMapping.jpg)](./media/ProjectExpenseCategoriesToPSAMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="280e8-144">[![Template mapping](./media/ProjectExpenseCategoriesToPSAMapping.jpg)](./media/ProjectExpenseCategoriesToPSAMapping.jpg)</span></span>

<span data-ttu-id="280e8-145">Seuraavaa mallia ja sen taustalla olevaa tehtävää käytetään synkronoimaan projektin kululuokat Project Service Automationista Finance and Operationsiin:</span><span class="sxs-lookup"><span data-stu-id="280e8-145">The following template and underlying task is used to synchronize project expense categories from Project Service Automation to Finance and Operations:</span></span>

<span data-ttu-id="280e8-146">-**Mallin nimi tietojen integroinnissa:** Projektin kulutapahtumaluokat (PSA:sta Fin and Opsiin) - **Projektin tehtävän nimi:** Luokkien synkronointi Fin Opsiin</span><span class="sxs-lookup"><span data-stu-id="280e8-146">-**Name of the template in Data integration:** Project expense transaction categories (PSA to Fin and Ops) -**Name of the task in the project:** Sync categories to Fin Ops</span></span>

## <a name="entity-set"></a><span data-ttu-id="280e8-147">Yksikköjoukko</span><span class="sxs-lookup"><span data-stu-id="280e8-147">Entity set</span></span>

| <span data-ttu-id="280e8-148">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="280e8-148">Project Service Automation</span></span>      | <span data-ttu-id="280e8-149">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="280e8-149">Finance and Operations</span></span>             |
|---------------------------------|------------------------------------|
| <span data-ttu-id="280e8-150">Tapahtumaluokat</span><span class="sxs-lookup"><span data-stu-id="280e8-150">Transaction categories</span></span>          | <span data-ttu-id="280e8-151">Luokkien integrointiyksikkö</span><span class="sxs-lookup"><span data-stu-id="280e8-151">Integration entity for categories</span></span>  | 

## <a name="entity-flow"></a><span data-ttu-id="280e8-152">Yksikön työnkulku</span><span class="sxs-lookup"><span data-stu-id="280e8-152">Entity flow</span></span>

<span data-ttu-id="280e8-153">Projektin kululuokkia tietoja hallitaan Finance and Operationsissa ja ne synkronoidaan Project Service Automationiin tapahtumaluokkina.</span><span class="sxs-lookup"><span data-stu-id="280e8-153">Project expense categories are managed in Finance and Operations, and they are synchronized to Project Service Automation as transaction categories.</span></span> <span data-ttu-id="280e8-154">Synkronointi takaisin Finance and Operationsiin päivittää Project Service Automationin integrointitunnuksen Finance and Operationsin projektiluokassa.</span><span class="sxs-lookup"><span data-stu-id="280e8-154">The synchronization back to Finance and Operations updates the integration ID from Project Service Automation on the Finance and Operations project category.</span></span>

<span data-ttu-id="280e8-155">Seuraavassa kuvassa on esimerkki mallitehtävän yhdistämisestä tietojen integroinnin yhteydessä.</span><span class="sxs-lookup"><span data-stu-id="280e8-155">The following illustration shows an example of the template task mapping in Data integration.</span></span>

> [!NOTE]
> <span data-ttu-id="280e8-156">Yhdistämismääritys näyttää Project Service Automationista Finance and Operationsiin synkronoitavan kentän tiedot.</span><span class="sxs-lookup"><span data-stu-id="280e8-156">The mapping shows the field information that will be synchronized from Project Service Automation to Finance and Operations.</span></span>

<span data-ttu-id="280e8-157">[![Mallin yhdistäminen](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="280e8-157">[![Template mapping](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)</span></span>

