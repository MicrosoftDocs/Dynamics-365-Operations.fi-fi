---
title: "Projektin kululuokkien synkronointi Finance and Operationsin ja Project Service Automationin välillä"
description: "Tässä ohjeaiheessa käsitellään malleja ja taustalla olevia tehtäviä, joilla projektin kululuokat synkronoidaan Microsoft Dynamics 365 for Finance and Operationsin ja Microsoft Dynamics 365 for Project Service Automationin välillä."
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
ms.dyn365.ops.version: AX 8.0.0
ms.translationtype: HT
ms.sourcegitcommit: d9747ba144d56c9410846769e5465372c89ea111
ms.openlocfilehash: c4d09fde2cf4335553243c136590f9f3135db97a
ms.contentlocale: fi-fi
ms.lasthandoff: 08/08/2018

---

# <a name="synchronize-project-expense-categories-between-finance-and-operations-and-project-service-automation"></a><span data-ttu-id="316d5-103">Projektin kululuokkien synkronointi Finance and Operationsin ja Project Service Automationin välillä</span><span class="sxs-lookup"><span data-stu-id="316d5-103">Synchronize project expense categories between Finance and Operations and Project Service Automation</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="316d5-104">Tässä ohjeaiheessa käsitellään malleja ja taustalla olevia tehtäviä, joilla projektin kululuokat synkronoidaan Microsoft Dynamics 365 for Finance and Operationsin ja Microsoft Dynamics 365 for Project Service Automationin välillä.</span><span class="sxs-lookup"><span data-stu-id="316d5-104">This topic describes the templates and underlying tasks that are used to synchronize project expense categories between Microsoft Dynamics 365 for Finance and Operations and Microsoft Dynamics 365 for Project Service Automation.</span></span>

> [!NOTE]
> - <span data-ttu-id="316d5-105">Projektitehtävän integrointi, kulutapahtumaluokat, tuntiarviot, kuluarviot ja toiminnon lukitseminen ovat käytössä Microsoft Dynamics 365 for Finance and Operationsin versiossa 8.0.</span><span class="sxs-lookup"><span data-stu-id="316d5-105">Project task integration, expense transaction categories, hour estimates, expense estimates, and functionality locking are available in Microsoft Dynamics 365 for Finance and Operations version 8.0.</span></span>
> - <span data-ttu-id="316d5-106">Todellisten tietojen integrointi on käytettävissä Microsoft Dynamics 365 for Finance and Operationsin versiossa 8.01 tai myöhempi.</span><span class="sxs-lookup"><span data-stu-id="316d5-106">Actuals integration is available in Microsoft Dynamics 365 for Finance and Operations version 8.0.1 or later.</span></span>
> - <span data-ttu-id="316d5-107">Jos käytössä on Microsoft Dynamics 365 for Finance and Operations, Enterprise edition 7.3.0 ja KB 4132657 ja KB 4132660 on asennettu, voit integroida projektitehtäviä, kulutapahtumaluokkia, tuntiarvioita, kuluarvioita ja todellisia tietoja sekä määrittää toimintojen lukituksen.</span><span class="sxs-lookup"><span data-stu-id="316d5-107">If you're using Microsoft Dynamics 365 for Finance and Operations, Enterprise edition 7.3.0, after you install KB 4132657 and KB 4132660, you will be able to use the templates to integrate project tasks, expense transaction categories, hour estimates, expense estimates, and actuals, and to configure functionality locking.</span></span> <span data-ttu-id="316d5-108">Jos kirjanpidollinen jako on palautettava alkuperäisasetuksiin, myös KB 4131710 kannattaa asentaa.</span><span class="sxs-lookup"><span data-stu-id="316d5-108">If you must reset the accounting distributions, we recommend that you also install KB 4131710.</span></span>

## <a name="data-flow-for-project-service-automation-and-finance-and-operations"></a><span data-ttu-id="316d5-109">Project Service Automationin ja Finance and Operationsin tiedonkulku</span><span class="sxs-lookup"><span data-stu-id="316d5-109">Data flow for Project Service Automation and Finance and Operations</span></span>

<span data-ttu-id="316d5-110">Project Service Automationin ja Finance and Operationsin välinen integrointiratkaisu synkronoi Project Service Automationin ja Finance and Operationsin esiintymien tiedot tietojen integrointiominaisuudella.</span><span class="sxs-lookup"><span data-stu-id="316d5-110">The Project Service Automation and Finance and Operations integration solution uses the Data integration feature to synchronize data across instances of Project Service Automation and Finance and Operations.</span></span> <span data-ttu-id="316d5-111">Tietojen integrointiominaisuudessa käytettävissä olevat integrointimallit mahdollistavat projektin kulutapahtumaluokkia koskevan tiedonkulun Project Service Automationin ja Finance and Operationsin välillä.</span><span class="sxs-lookup"><span data-stu-id="316d5-111">The integration templates that are available with the Data integration feature enable the flow of data about project expense transaction categories between Finance and Operations and Project Service Automation.</span></span>

<span data-ttu-id="316d5-112">Jos projektin kululuokkia hallitaan Finance and Operationsista, integrointi tapahtuu ensin Finance and Operationsista Project Service Automationiin.</span><span class="sxs-lookup"><span data-stu-id="316d5-112">If the project expense categories are mastered in Finance and Operations, the integration flow is first from Finance and Operations to Project Service Automation.</span></span> <span data-ttu-id="316d5-113">Projektin kustannusluokkien integraatiotunnukset päivitetään sitten synkronoinnin avulla Project Service Automationista Finance and Operationsiin.</span><span class="sxs-lookup"><span data-stu-id="316d5-113">The integration IDs of the project expense categories are then updated through synchronization from Project Service Automation to Finance and Operations.</span></span>

<span data-ttu-id="316d5-114">Jos projektin kululuokkia hallitaan Project Service Automationista, integrointi tapahtuu ensin Project Service Automationista Finance and Operationsiin.</span><span class="sxs-lookup"><span data-stu-id="316d5-114">If the project expense categories are mastered in Project Service Automation, the integration flow is first from Project Service Automation to Finance and Operations.</span></span> <span data-ttu-id="316d5-115">Projektiluokkien on oltava määritettynä Finance and Operationsissa ennen synkronointia Project Service Automationista.</span><span class="sxs-lookup"><span data-stu-id="316d5-115">The project categories must already be configured in Finance and Operations before the synchronization from Project Service Automation.</span></span> <span data-ttu-id="316d5-116">Voit tämän jälkeen tehdä synkronoinnin Finance and Operationsista takaisin Project Service Automationiin ja sitten uudelleen Project Service Automationista Finance and Operationsiin.</span><span class="sxs-lookup"><span data-stu-id="316d5-116">Then synchronize from Finance and Operations back to Project Service Automation, and then from Project Service Automation to Finance and Operations again.</span></span> <span data-ttu-id="316d5-117">Tällöin voit varmistua, että kategoriat on linkitetty eikä kaksoiskappaleita luoda.</span><span class="sxs-lookup"><span data-stu-id="316d5-117">In this way, you help guarantee that the categories are linked, and that no duplicates are created.</span></span>

> [!NOTE]
> <span data-ttu-id="316d5-118">Yleensä projektin kululuokkia hallitaan Finance and Operationsissa.</span><span class="sxs-lookup"><span data-stu-id="316d5-118">Typically, the project expense categories are mastered in Finance and Operations.</span></span> <span data-ttu-id="316d5-119">Jos niitä ei kuitenkaan hallita Finance and Operationssa tai kululuokat on jo luotu Project Service Automationissa, synkronoi ensin käyttämällä Project expense transactionin (Fin ja Ops PSA) -kategoriatemplaattia.</span><span class="sxs-lookup"><span data-stu-id="316d5-119">However, if they aren't mastered in Finance and Operations, or if expense categories have already been created in Project Service Automation, you must first synchronize by using the Project expense transaction categories (PSA to Fin and Ops) template.</span></span> <span data-ttu-id="316d5-120">Synkronoi käyttämällä Project expense transactionin kategoriatemplaattia (Fin ja Ops PSA).</span><span class="sxs-lookup"><span data-stu-id="316d5-120">Then synchronize by using the Project expense transaction categories (Fin and Ops to PSA) template.</span></span> <span data-ttu-id="316d5-121">Suorita synkronointi vielä kerran Project Service Automationista Finance and Operationsiin.</span><span class="sxs-lookup"><span data-stu-id="316d5-121">You should then run the synchronization from Project Service Automation to Finance and Operations one more time.</span></span>
>
> <span data-ttu-id="316d5-122">Jos synkronoit ensin Project Service Automationista, Finance and Operationsin täytyy täyttää seuraavat vaatimukset ennen kuin synkronointi suoritetaan:</span><span class="sxs-lookup"><span data-stu-id="316d5-122">If you synchronize first from Project Service Automation, the following requirements must be met in Finance and Operations before the synchronization is run:</span></span>
>
> - <span data-ttu-id="316d5-123">Jaetun kategorian, joka vastaa projektikategoriaa, joka on Project Service Automationissa täytyy olla olemassa ja sen pitää olla käytössä sekä kohdissa **Projekti** että **Kulu**.</span><span class="sxs-lookup"><span data-stu-id="316d5-123">The shared category that matches the project category that is set up in Project Service Automation must exist, and it must be enabled for both **Project** and **Expense**.</span></span>
> - <span data-ttu-id="316d5-124">Seuraavien projektiluokkien täytyy olla olemassa kullakin Finance and Operations -yrityksellä, joka on integroitava:</span><span class="sxs-lookup"><span data-stu-id="316d5-124">For each Finance and Operations legal entity that must be integrated with, the following project categories must exist:</span></span>
>
>     - <span data-ttu-id="316d5-125">**Projektikategoria** on olemassa.</span><span class="sxs-lookup"><span data-stu-id="316d5-125">**Project category** exists.</span></span> 
>     - <span data-ttu-id="316d5-126">**Käytä kuluissa** on käytössä.</span><span class="sxs-lookup"><span data-stu-id="316d5-126">**Use in Expense** is enabled.</span></span>
>     - <span data-ttu-id="316d5-127">**Aktiivinen kirjauskansiossa** on käytössä.</span><span class="sxs-lookup"><span data-stu-id="316d5-127">**Active in journal** is enabled.</span></span>
>     - <span data-ttu-id="316d5-128">**Transaktiotyyppi** on **Kulu**.</span><span class="sxs-lookup"><span data-stu-id="316d5-128">**Transaction type** is set to **Expense**.</span></span>

<span data-ttu-id="316d5-129">Seuraava kuva ilmaisee, miten tiedot synkronoidaan Project Service Automationin ja Finance and Operationsin välillä.</span><span class="sxs-lookup"><span data-stu-id="316d5-129">The following illustration shows how the data is synchronized between Project Service Automation and Finance and Operations.</span></span>

<span data-ttu-id="316d5-130">[![Project Service Automationin ja Finance and Operationsin välisen integroinnin tiedonkulku](./media/ProjectExpenseCategoriesFlow.png)](./media/ProjectExpenseCategoriesFlow.png)</span><span class="sxs-lookup"><span data-stu-id="316d5-130">[![Data flow for Project Service Automation integration with Finance and Operations](./media/ProjectExpenseCategoriesFlow.png)](./media/ProjectExpenseCategoriesFlow.png)</span></span>

## <a name="project-expense-category-synchronization-from-finance-and-operations-to-project-service-automation"></a><span data-ttu-id="316d5-131">Projektin kululuokkien synkronointi Finance and Operationsista ja Project Service Automationiin</span><span class="sxs-lookup"><span data-stu-id="316d5-131">Project expense category synchronization from Finance and Operations to Project Service Automation</span></span>

### <a name="template-and-task"></a><span data-ttu-id="316d5-132">Malli ja tehtävä</span><span class="sxs-lookup"><span data-stu-id="316d5-132">Template and task</span></span>

<span data-ttu-id="316d5-133">Saat mallin käyttöösi valitsemalla Microsoft PowerAppsin hallintakeskuksessa **Projektit**. Valitse sitten julkiset mallit valitsemalla oikeassa yläkulmassa **Uusi projekti**.</span><span class="sxs-lookup"><span data-stu-id="316d5-133">To access the template, in the Microsoft PowerApps admin center, select **Projects**, and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="316d5-134">Seuraavaa mallia ja sen taustalla olevaa tehtävää käytetään synkronoimaan projektin kululuokat Finance and Operationsista Project Service Automationiin:</span><span class="sxs-lookup"><span data-stu-id="316d5-134">The following template and underlying task are used to synchronize project expense categories from Finance and Operations to Project Service Automation:</span></span>

- <span data-ttu-id="316d5-135">**Mallin nimi tietojen integroinnissa:** projektin kulutapahtumaluokat (Fin and Opsista PSA:han)</span><span class="sxs-lookup"><span data-stu-id="316d5-135">**Name of the template in Data integration:** Project expense transaction categories (Fin and Ops to PSA)</span></span>
- <span data-ttu-id="316d5-136">**Projektin tehtävän nimi:** luokkien synkronointi PSA:han</span><span class="sxs-lookup"><span data-stu-id="316d5-136">**Name of the task in the project:** Sync categories to PSA</span></span>

### <a name="entity-set"></a><span data-ttu-id="316d5-137">Yksikköjoukko</span><span class="sxs-lookup"><span data-stu-id="316d5-137">Entity set</span></span>

| <span data-ttu-id="316d5-138">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="316d5-138">Finance and Operations</span></span>            | <span data-ttu-id="316d5-139">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="316d5-139">Project Service Automation</span></span> |
|-----------------------------------|----------------------------|
| <span data-ttu-id="316d5-140">Luokkien integrointiyksikkö</span><span class="sxs-lookup"><span data-stu-id="316d5-140">Integration entity for categories</span></span> | <span data-ttu-id="316d5-141">Tapahtumaluokat</span><span class="sxs-lookup"><span data-stu-id="316d5-141">Transaction categories</span></span>     |

### <a name="entity-flow"></a><span data-ttu-id="316d5-142">Yksikön työnkulku</span><span class="sxs-lookup"><span data-stu-id="316d5-142">Entity flow</span></span>

<span data-ttu-id="316d5-143">Projektin kululuokkia tietoja hallitaan Finance and Operationsissa ja ne synkronoidaan Project Service Automationiin tapahtumaluokkina.</span><span class="sxs-lookup"><span data-stu-id="316d5-143">Project expense categories are managed in Finance and Operations, and they are synchronized to Project Service Automation as transaction categories.</span></span>

### <a name="power-query"></a><span data-ttu-id="316d5-144">Power Query</span><span class="sxs-lookup"><span data-stu-id="316d5-144">Power Query</span></span>

<span data-ttu-id="316d5-145">Tapahtumaluokan laskutustyyppi on määritettävä Microsoft Power Query for Excelillä, kun synkronointi tehdään Project Service Automationiin.</span><span class="sxs-lookup"><span data-stu-id="316d5-145">When you're synchronizing to Project Service Automation, you must use Microsoft Power Query for Excel to set the billing type on the transaction category.</span></span> <span data-ttu-id="316d5-146">Projektin kulutapahtumaluokkien malli (Fin and Opsista PSA:han) tarjoaa oletussarakkeen ja yhdistämismäärityksen.</span><span class="sxs-lookup"><span data-stu-id="316d5-146">The Project expense transaction categories (Fin and Ops to PSA) template provides a default column and mapping.</span></span> <span data-ttu-id="316d5-147">Jos luot oman mallin, ehtosarake on lisättävä Power Queryssä.</span><span class="sxs-lookup"><span data-stu-id="316d5-147">If you create your own template, you must add a conditional column in Power Query.</span></span> <span data-ttu-id="316d5-148">Noudata näitä ohjeita.</span><span class="sxs-lookup"><span data-stu-id="316d5-148">Follow these steps.</span></span>

1. <span data-ttu-id="316d5-149">Avaa projektikustannusluokkatehtävän kartoitus napsauttamalla nuolta projektin kulukirjausmallissa (Fin ja Ops to PSA).</span><span class="sxs-lookup"><span data-stu-id="316d5-149">Click the arrow to open the mapping of the project expense categories task in the Project expense transaction categories (Fin and Ops to PSA) template.</span></span>
2. <span data-ttu-id="316d5-150">Napsauta **Kyselyn ja suodatuksen lisäasetukset** avataksesi Power Queryn.</span><span class="sxs-lookup"><span data-stu-id="316d5-150">Click the **Advance Query and Filtering** link to open Power Query.</span></span>
2. <span data-ttu-id="316d5-151">Valitse **Lisää ehtosarake**.</span><span class="sxs-lookup"><span data-stu-id="316d5-151">Select **Add Conditional Column**.</span></span>
3. <span data-ttu-id="316d5-152">Anna sarakkeelle uusi nimi, kuten **Laskutustyyppi**.</span><span class="sxs-lookup"><span data-stu-id="316d5-152">Enter a name for the new column, such as **BillingType**.</span></span>
4. <span data-ttu-id="316d5-153">Anna seuraava ehto: **jos CATEGORYID ei sama kuin tyhjäarvo sitten 19235001, muuten tyhjäarvo**.</span><span class="sxs-lookup"><span data-stu-id="316d5-153">Enter the following condition: **if CATEGORYID not equal to null then 19235001, Otherwise null**.</span></span>
5. <span data-ttu-id="316d5-154">Valitse sarakkeessa **OK**.</span><span class="sxs-lookup"><span data-stu-id="316d5-154">Click **OK** on the column.</span></span>
6. <span data-ttu-id="316d5-155">Varmista, että yhdistät tämän uuden sarakkeen yhdistämismäärityssivulla.</span><span class="sxs-lookup"><span data-stu-id="316d5-155">Be sure to map this new column on the mapping page.</span></span>

<span data-ttu-id="316d5-156">Seuraavassa kuvassa on esimerkki mallitehtävän yhdistämisestä tietojen integroinnin yhteydessä.</span><span class="sxs-lookup"><span data-stu-id="316d5-156">The following illustration shows an example of the template task mapping in Data integration.</span></span> <span data-ttu-id="316d5-157">Yhdistämismääritys näyttää Finance and Operationsista Project Service Automationiin synkronoitavan kentän tiedot.</span><span class="sxs-lookup"><span data-stu-id="316d5-157">The mapping shows the field information that will be synchronized from Finance and Operations to Project Service Automation.</span></span>

<span data-ttu-id="316d5-158">[![Mallin yhdistäminen](./media/ProjectExpenseCategoriesToPSAMapping.jpg)](./media/ProjectExpenseCategoriesToPSAMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="316d5-158">[![Template mapping](./media/ProjectExpenseCategoriesToPSAMapping.jpg)](./media/ProjectExpenseCategoriesToPSAMapping.jpg)</span></span>

## <a name="project-expense-category-synchronization-from-project-service-automation-to-finance-and-operations"></a><span data-ttu-id="316d5-159">Projektin kululuokkien synkronointi Project Service Automationista Finance and Operationsiin</span><span class="sxs-lookup"><span data-stu-id="316d5-159">Project expense category synchronization from Project Service Automation to Finance and Operations</span></span>

### <a name="template-and-task"></a><span data-ttu-id="316d5-160">Malli ja tehtävä</span><span class="sxs-lookup"><span data-stu-id="316d5-160">Template and task</span></span>

<span data-ttu-id="316d5-161">Seuraavaa mallia ja sen taustalla olevaa tehtävää käytetään synkronoimaan projektin kululuokat Project Service Automationista Finance and Operationsiin:</span><span class="sxs-lookup"><span data-stu-id="316d5-161">The following template and underlying task are used to synchronize project expense categories from Project Service Automation to Finance and Operations:</span></span>

- <span data-ttu-id="316d5-162">**Mallin nimi tietojen integroinnissa:** projektin kulutapahtumaluokat (PSA to Fin and Ops:iin)</span><span class="sxs-lookup"><span data-stu-id="316d5-162">**Name of the template in Data integration:** Project expense transaction categories (PSA to Fin and Ops)</span></span>
- <span data-ttu-id="316d5-163">**Projektin tehtävän nimi:** luokkien synkronointi Fin Ops:iin</span><span class="sxs-lookup"><span data-stu-id="316d5-163">**Name of the task in the project:** Sync categories to Fin Ops</span></span>

### <a name="entity-set"></a><span data-ttu-id="316d5-164">Yksikköjoukko</span><span class="sxs-lookup"><span data-stu-id="316d5-164">Entity set</span></span>

| <span data-ttu-id="316d5-165">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="316d5-165">Project Service Automation</span></span> | <span data-ttu-id="316d5-166">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="316d5-166">Finance and Operations</span></span>            |
|----------------------------|-----------------------------------|
| <span data-ttu-id="316d5-167">Tapahtumaluokat</span><span class="sxs-lookup"><span data-stu-id="316d5-167">Transaction categories</span></span>     | <span data-ttu-id="316d5-168">Luokkien integrointiyksikkö</span><span class="sxs-lookup"><span data-stu-id="316d5-168">Integration entity for categories</span></span> |

### <a name="entity-flow"></a><span data-ttu-id="316d5-169">Yksikön työnkulku</span><span class="sxs-lookup"><span data-stu-id="316d5-169">Entity flow</span></span>

<span data-ttu-id="316d5-170">Projektin kululuokkia tietoja hallitaan Finance and Operationsissa ja ne synkronoidaan Project Service Automationiin tapahtumaluokkina.</span><span class="sxs-lookup"><span data-stu-id="316d5-170">Project expense categories are managed in Finance and Operations, and they are synchronized to Project Service Automation as transaction categories.</span></span> <span data-ttu-id="316d5-171">Synkronointi takaisin Finance and Operationsiin päivittää projektiluokan Finance and Operationsissa Project Service Automationin integrointitunnuksella.</span><span class="sxs-lookup"><span data-stu-id="316d5-171">The synchronization back to Finance and Operations updates the project category in Finance and Operations with the integration ID from Project Service Automation.</span></span>

### <a name="template-mapping-in-data-integration"></a><span data-ttu-id="316d5-172">Mallin yhdistäminen tietojen integroinnin yhteydessä</span><span class="sxs-lookup"><span data-stu-id="316d5-172">Template mapping in Data integration</span></span>

<span data-ttu-id="316d5-173">Seuraavassa kuvassa on esimerkki mallitehtävän yhdistämisestä tietojen integroinnin yhteydessä.</span><span class="sxs-lookup"><span data-stu-id="316d5-173">The following illustration shows an example of the template task mapping in Data integration.</span></span>

> [!NOTE]
> <span data-ttu-id="316d5-174">Yhdistämismääritys näyttää Project Service Automationista Finance and Operationsiin synkronoitavan kentän tiedot.</span><span class="sxs-lookup"><span data-stu-id="316d5-174">The mapping shows the field information that will be synchronized from Project Service Automation to Finance and Operations.</span></span>

<span data-ttu-id="316d5-175">[![Mallin yhdistäminen](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="316d5-175">[![Template mapping](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)</span></span>

