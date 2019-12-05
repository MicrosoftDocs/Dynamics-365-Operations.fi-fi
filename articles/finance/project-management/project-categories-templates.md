---
title: Projektin kululuokkien synkronointi Finance and Operationsin ja Project Service Automationin välillä
description: Tässä ohjeaiheessa käsitellään malleja ja taustalla olevia tehtäviä, joilla projektin kululuokat synkronoidaan Microsoft Dynamics 365 Financen ja Dynamics 365 Project Service Automationin välillä.
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
ms.dyn365.ops.version: AX 8.0.0
ms.openlocfilehash: 7b0b3721c3b0755218c834d2bf77ec976be3bdcc
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/06/2019
ms.locfileid: "2770309"
---
# <a name="synchronize-project-expense-categories-between-finance-and-operations-and-project-service-automation"></a><span data-ttu-id="bf216-103">Projektin kululuokkien synkronointi Finance and Operationsin ja Project Service Automationin välillä</span><span class="sxs-lookup"><span data-stu-id="bf216-103">Synchronize project expense categories between Finance and Operations and Project Service Automation</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="bf216-104">Tässä ohjeaiheessa käsitellään malleja ja taustalla olevia tehtäviä, joilla projektin kululuokat synkronoidaan Dynamics 365 Financein ja Dynamics 365 Project Service Automationin välillä.</span><span class="sxs-lookup"><span data-stu-id="bf216-104">This topic describes the templates and underlying tasks that are used to synchronize project expense categories between Dynamics 365 Finance and Dynamics 365 Project Service Automation.</span></span>

> [!NOTE]
> - <span data-ttu-id="bf216-105">Projektitehtävän integrointi, kulutapahtumaluokat, tuntiarviot, kuluarviot ja toiminnon lukitseminen ovat käytettävissä versiossa 8.0.</span><span class="sxs-lookup"><span data-stu-id="bf216-105">Project task integration, expense transaction categories, hour estimates, expense estimates, and functionality locking are available in version 8.0.</span></span>
> - <span data-ttu-id="bf216-106">Todellisten tietojen integrointi on käytettävissä versiossa 8.0.1 tai sitä uudemmassa.</span><span class="sxs-lookup"><span data-stu-id="bf216-106">Actuals integration is available in version 8.0.1 or later.</span></span>
> - <span data-ttu-id="bf216-107">Jos käytät Enterprise edition -versiota 7.3.0 sen jälkeen, kun KB 4132657 ja KB 4132660 on asennettu, voit käyttää malleja integroidaksesi projektitehtäviä, kulutapahtumaluokkia, tuntiarvioita, kuluarvioita ja todellisia tietoja sekä määrittääksesi toimintojen lukituksen.</span><span class="sxs-lookup"><span data-stu-id="bf216-107">If you're using Enterprise edition 7.3.0, after you install KB 4132657 and KB 4132660, you will be able to use the templates to integrate project tasks, expense transaction categories, hour estimates, expense estimates, and actuals, and to configure functionality locking.</span></span> <span data-ttu-id="bf216-108">Jos kirjanpidollinen jako on palautettava alkuperäisasetuksiin, myös KB 4131710 kannattaa asentaa.</span><span class="sxs-lookup"><span data-stu-id="bf216-108">If you must reset the accounting distributions, we recommend that you also install KB 4131710.</span></span>

## <a name="data-flow-for-project-service-automation-and-finance"></a><span data-ttu-id="bf216-109">Tiedonkulku Project Service Automation ja Financen välillä</span><span class="sxs-lookup"><span data-stu-id="bf216-109">Data flow for Project Service Automation and Finance</span></span>

<span data-ttu-id="bf216-110">Project Service Automationin ja Financen välinen integrointiratkaisu synkronoi Project Service Automation- ja Finance-esiintymien tiedot tietojen integrointiominaisuudella.</span><span class="sxs-lookup"><span data-stu-id="bf216-110">The Project Service Automation and Finance integration solution uses the Data integration feature to synchronize data across instances of Project Service Automation and Finance.</span></span> <span data-ttu-id="bf216-111">Tietojen integrointiominaisuudessa käytettävissä olevat integrointimallit mahdollistavat projektin kulutapahtumaluokkia koskevan tiedonkulun Project Service Automationin ja Financen välillä.</span><span class="sxs-lookup"><span data-stu-id="bf216-111">The integration templates that are available with the Data integration feature enable the flow of data about project expense transaction categories between Finance and Project Service Automation.</span></span>

<span data-ttu-id="bf216-112">Jos projektin kululuokkia hallitaan Financesta, integrointi tapahtuu ensin Financesta Project Service Automationiin.</span><span class="sxs-lookup"><span data-stu-id="bf216-112">If the project expense categories are mastered in Finance, the integration flow is first from Finance to Project Service Automation.</span></span> <span data-ttu-id="bf216-113">Projektin kustannusluokkien integraatiotunnukset päivitetään sitten synkronoinnin avulla Project Service Automationista Financeen.</span><span class="sxs-lookup"><span data-stu-id="bf216-113">The integration IDs of the project expense categories are then updated through synchronization from Project Service Automation to Finance.</span></span>

<span data-ttu-id="bf216-114">Jos projektin kululuokkia hallitaan Project Service Automationista, integrointi tapahtuu ensin Project Service Automationista Financeen.</span><span class="sxs-lookup"><span data-stu-id="bf216-114">If the project expense categories are mastered in Project Service Automation, the integration flow is first from Project Service Automation to Finance.</span></span> <span data-ttu-id="bf216-115">Projektiluokkien on oltava määritettynä Financessa ennen synkronointia Project Service Automationista.</span><span class="sxs-lookup"><span data-stu-id="bf216-115">The project categories must already be configured in Finance before the synchronization from Project Service Automation.</span></span> <span data-ttu-id="bf216-116">Synkronoi tiedot sitten Financesta takaisin Project Service Automationiin ja sitten uudelleen Project Service Automationista Financeen.</span><span class="sxs-lookup"><span data-stu-id="bf216-116">Then synchronize from Finance back to Project Service Automation, and then from Project Service Automation to Finance again.</span></span> <span data-ttu-id="bf216-117">Tällöin voit varmistua, että kategoriat on linkitetty eikä kaksoiskappaleita luoda.</span><span class="sxs-lookup"><span data-stu-id="bf216-117">In this way, you help guarantee that the categories are linked, and that no duplicates are created.</span></span>

> [!NOTE]
> <span data-ttu-id="bf216-118">Tavallisesti projektin kululuokkia hallitaan Financessa.</span><span class="sxs-lookup"><span data-stu-id="bf216-118">Typically, the project expense categories are mastered in Finance.</span></span> <span data-ttu-id="bf216-119">Jos näin ei kuitenkaan ole tai kululuokat on jo luotu Project Service Automationissa, synkronoi ensin käyttämällä projektin kulutapahtumaluokkien mallia (PSA:sta Fin and Opsiin).</span><span class="sxs-lookup"><span data-stu-id="bf216-119">However, if they aren't, or if expense categories have already been created in Project Service Automation, you must first synchronize by using the Project expense transaction categories (PSA to Fin and Ops) template.</span></span> <span data-ttu-id="bf216-120">Synkronoi käyttämällä Project expense transactionin kategoriatemplaattia (Fin ja Ops PSA).</span><span class="sxs-lookup"><span data-stu-id="bf216-120">Then synchronize by using the Project expense transaction categories (Fin and Ops to PSA) template.</span></span> <span data-ttu-id="bf216-121">Sinun tulisi suorittaa synkronointi Project Service Automationista Financeen vielä kerran.</span><span class="sxs-lookup"><span data-stu-id="bf216-121">You should then run the synchronization from Project Service Automation to Finance one more time.</span></span>
>
> <span data-ttu-id="bf216-122">Jos synkronoit ensin Project Service Automationista, Financen täytyy täyttää seuraavat vaatimukset ennen kuin synkronointi suoritetaan:</span><span class="sxs-lookup"><span data-stu-id="bf216-122">If you synchronize first from Project Service Automation, the following requirements must be met in Finance before the synchronization is run:</span></span>
>
> - <span data-ttu-id="bf216-123">Jaetun kategorian, joka vastaa projektikategoriaa, joka on Project Service Automationissa täytyy olla olemassa ja sen pitää olla käytössä sekä kohdissa **Projekti** että **Kulu**.</span><span class="sxs-lookup"><span data-stu-id="bf216-123">The shared category that matches the project category that is set up in Project Service Automation must exist, and it must be enabled for both **Project** and **Expense**.</span></span>
> - <span data-ttu-id="bf216-124">Jokaisella integroitavalla Finance-yrityksellä täytyy olla seuraavat projektiluokat:</span><span class="sxs-lookup"><span data-stu-id="bf216-124">For each Finance legal entity that must be integrated with, the following project categories must exist:</span></span>
>
>     - <span data-ttu-id="bf216-125">**Projektikategoria** on olemassa.</span><span class="sxs-lookup"><span data-stu-id="bf216-125">**Project category** exists.</span></span> 
>     - <span data-ttu-id="bf216-126">**Käytä kuluissa** on käytössä.</span><span class="sxs-lookup"><span data-stu-id="bf216-126">**Use in Expense** is enabled.</span></span>
>     - <span data-ttu-id="bf216-127">**Aktiivinen kirjauskansiossa** on käytössä.</span><span class="sxs-lookup"><span data-stu-id="bf216-127">**Active in journal** is enabled.</span></span>
>     - <span data-ttu-id="bf216-128">**Transaktiotyyppi** on **Kulu**.</span><span class="sxs-lookup"><span data-stu-id="bf216-128">**Transaction type** is set to **Expense**.</span></span>

<span data-ttu-id="bf216-129">Seuraava kuva ilmaisee, miten tiedot synkronoidaan Project Service Automationin ja Financen välillä.</span><span class="sxs-lookup"><span data-stu-id="bf216-129">The following illustration shows how the data is synchronized between Project Service Automation and Finance.</span></span>

<span data-ttu-id="bf216-130">[![Project Service Automationin ja Financen välisen integroinnin tiedonkulku](./media/ProjectExpenseCategoriesFlow.png)](./media/ProjectExpenseCategoriesFlow.png)</span><span class="sxs-lookup"><span data-stu-id="bf216-130">[![Data flow for Project Service Automation integration with Finance](./media/ProjectExpenseCategoriesFlow.png)](./media/ProjectExpenseCategoriesFlow.png)</span></span>

## <a name="project-expense-category-synchronization-from-finance-to-project-service-automation"></a><span data-ttu-id="bf216-131">Projektin kululuokkien synkronointi Financesta Project Service Automationiin</span><span class="sxs-lookup"><span data-stu-id="bf216-131">Project expense category synchronization from Finance to Project Service Automation</span></span>

### <a name="template-and-task"></a><span data-ttu-id="bf216-132">Malli ja tehtävä</span><span class="sxs-lookup"><span data-stu-id="bf216-132">Template and task</span></span>

<span data-ttu-id="bf216-133">Saat mallin käyttöösi valitsemalla Microsoft Power Appsin hallintakeskuksessa **Projektit**. Valitse sitten julkiset mallit valitsemalla oikeassa yläkulmassa **Uusi projekti**.</span><span class="sxs-lookup"><span data-stu-id="bf216-133">To access the template, in the Microsoft Power Apps admin center, select **Projects**, and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="bf216-134">Seuraavaa mallia ja sen taustalla olevaa tehtävää käytetään synkronoimaan projektin kululuokat Financesta Project Service Automationiin:</span><span class="sxs-lookup"><span data-stu-id="bf216-134">The following template and underlying task are used to synchronize project expense categories from Finance to Project Service Automation:</span></span>

- <span data-ttu-id="bf216-135">**Mallin nimi tietojen integroinnissa:** projektin kulutapahtumaluokat (Fin and Opsista PSA:han)</span><span class="sxs-lookup"><span data-stu-id="bf216-135">**Name of the template in Data integration:** Project expense transaction categories (Fin and Ops to PSA)</span></span>
- <span data-ttu-id="bf216-136">**Projektin tehtävän nimi:** luokkien synkronointi PSA:han</span><span class="sxs-lookup"><span data-stu-id="bf216-136">**Name of the task in the project:** Sync categories to PSA</span></span>

### <a name="entity-set"></a><span data-ttu-id="bf216-137">Yksikköjoukko</span><span class="sxs-lookup"><span data-stu-id="bf216-137">Entity set</span></span>

| <span data-ttu-id="bf216-138">Myyntitiedot</span><span class="sxs-lookup"><span data-stu-id="bf216-138">Finance</span></span>                           | <span data-ttu-id="bf216-139">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="bf216-139">Project Service Automation</span></span> |
|-----------------------------------|----------------------------|
| <span data-ttu-id="bf216-140">Luokkien integrointiyksikkö</span><span class="sxs-lookup"><span data-stu-id="bf216-140">Integration entity for categories</span></span> | <span data-ttu-id="bf216-141">Tapahtumaluokat</span><span class="sxs-lookup"><span data-stu-id="bf216-141">Transaction categories</span></span>     |

### <a name="entity-flow"></a><span data-ttu-id="bf216-142">Yksikön työnkulku</span><span class="sxs-lookup"><span data-stu-id="bf216-142">Entity flow</span></span>

<span data-ttu-id="bf216-143">Projektin kululuokkia tietoja hallitaan Financessa ja ne synkronoidaan Project Service Automationiin tapahtumaluokkina.</span><span class="sxs-lookup"><span data-stu-id="bf216-143">Project expense categories are managed in Finance, and they are synchronized to Project Service Automation as transaction categories.</span></span>

### <a name="power-query"></a><span data-ttu-id="bf216-144">Power Query</span><span class="sxs-lookup"><span data-stu-id="bf216-144">Power Query</span></span>

<span data-ttu-id="bf216-145">Tapahtumaluokan laskutustyyppi on määritettävä Microsoft Power Query for Excelillä, kun synkronointi tehdään Project Service Automationiin.</span><span class="sxs-lookup"><span data-stu-id="bf216-145">When you're synchronizing to Project Service Automation, you must use Microsoft Power Query for Excel to set the billing type on the transaction category.</span></span> <span data-ttu-id="bf216-146">Projektin kulutapahtumaluokkien malli (Fin and Opsista PSA:han) tarjoaa oletussarakkeen ja yhdistämismäärityksen.</span><span class="sxs-lookup"><span data-stu-id="bf216-146">The Project expense transaction categories (Fin and Ops to PSA) template provides a default column and mapping.</span></span> <span data-ttu-id="bf216-147">Jos luot oman mallin, ehtosarake on lisättävä Power Queryssä.</span><span class="sxs-lookup"><span data-stu-id="bf216-147">If you create your own template, you must add a conditional column in Power Query.</span></span> <span data-ttu-id="bf216-148">Noudata näitä ohjeita.</span><span class="sxs-lookup"><span data-stu-id="bf216-148">Follow these steps.</span></span>

1. <span data-ttu-id="bf216-149">Avaa projektikustannusluokkatehtävän kartoitus napsauttamalla nuolta projektin kulukirjausmallissa (Fin ja Ops to PSA).</span><span class="sxs-lookup"><span data-stu-id="bf216-149">Click the arrow to open the mapping of the project expense categories task in the Project expense transaction categories (Fin and Ops to PSA) template.</span></span>
2. <span data-ttu-id="bf216-150">Napsauta **Kyselyn ja suodatuksen lisäasetukset** avataksesi Power Queryn.</span><span class="sxs-lookup"><span data-stu-id="bf216-150">Click the **Advance Query and Filtering** link to open Power Query.</span></span>
2. <span data-ttu-id="bf216-151">Valitse **Lisää ehtosarake**.</span><span class="sxs-lookup"><span data-stu-id="bf216-151">Select **Add Conditional Column**.</span></span>
3. <span data-ttu-id="bf216-152">Anna sarakkeelle uusi nimi, kuten **Laskutustyyppi**.</span><span class="sxs-lookup"><span data-stu-id="bf216-152">Enter a name for the new column, such as **BillingType**.</span></span>
4. <span data-ttu-id="bf216-153">Anna seuraava ehto: **jos CATEGORYID ei sama kuin tyhjäarvo sitten 19235001, muuten tyhjäarvo**.</span><span class="sxs-lookup"><span data-stu-id="bf216-153">Enter the following condition: **if CATEGORYID not equal to null then 19235001, Otherwise null**.</span></span>
5. <span data-ttu-id="bf216-154">Valitse sarakkeessa **OK**.</span><span class="sxs-lookup"><span data-stu-id="bf216-154">Click **OK** on the column.</span></span>
6. <span data-ttu-id="bf216-155">Varmista, että yhdistät tämän uuden sarakkeen yhdistämismäärityssivulla.</span><span class="sxs-lookup"><span data-stu-id="bf216-155">Be sure to map this new column on the mapping page.</span></span>

<span data-ttu-id="bf216-156">Seuraavassa kuvassa on esimerkki mallitehtävän yhdistämisestä tietojen integroinnin yhteydessä.</span><span class="sxs-lookup"><span data-stu-id="bf216-156">The following illustration shows an example of the template task mapping in Data integration.</span></span> <span data-ttu-id="bf216-157">Yhdistämismääritys näyttää Financesta Project Service Automationiin synkronoitavien kenttien tiedot.</span><span class="sxs-lookup"><span data-stu-id="bf216-157">The mapping shows the field information that will be synchronized from Finance to Project Service Automation.</span></span>

<span data-ttu-id="bf216-158">[![Mallin yhdistäminen](./media/ProjectExpenseCategoriesToPSAMapping.jpg)](./media/ProjectExpenseCategoriesToPSAMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="bf216-158">[![Template mapping](./media/ProjectExpenseCategoriesToPSAMapping.jpg)](./media/ProjectExpenseCategoriesToPSAMapping.jpg)</span></span>

## <a name="project-expense-category-synchronization-from-project-service-automation-to-finance"></a><span data-ttu-id="bf216-159">Projektin kululuokkien synkronointi Project Service Automationista Financeen</span><span class="sxs-lookup"><span data-stu-id="bf216-159">Project expense category synchronization from Project Service Automation to Finance</span></span>

### <a name="template-and-task"></a><span data-ttu-id="bf216-160">Malli ja tehtävä</span><span class="sxs-lookup"><span data-stu-id="bf216-160">Template and task</span></span>

<span data-ttu-id="bf216-161">Seuraavaa mallia ja sen taustalla olevaa tehtävää käytetään synkronoimaan projektin kululuokat Project Service Automationista Financeen:</span><span class="sxs-lookup"><span data-stu-id="bf216-161">The following template and underlying task are used to synchronize project expense categories from Project Service Automation to Finance:</span></span>

- <span data-ttu-id="bf216-162">**Mallin nimi tietojen integroinnissa:** projektin kulutapahtumaluokat (PSA to Fin and Ops:iin)</span><span class="sxs-lookup"><span data-stu-id="bf216-162">**Name of the template in Data integration:** Project expense transaction categories (PSA to Fin and Ops)</span></span>
- <span data-ttu-id="bf216-163">**Projektin tehtävän nimi:** luokkien synkronointi Fin Ops:iin</span><span class="sxs-lookup"><span data-stu-id="bf216-163">**Name of the task in the project:** Sync categories to Fin Ops</span></span>

### <a name="entity-set"></a><span data-ttu-id="bf216-164">Yksikköjoukko</span><span class="sxs-lookup"><span data-stu-id="bf216-164">Entity set</span></span>

| <span data-ttu-id="bf216-165">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="bf216-165">Project Service Automation</span></span> | <span data-ttu-id="bf216-166">Myyntitiedot</span><span class="sxs-lookup"><span data-stu-id="bf216-166">Finance</span></span>                           |
|----------------------------|-----------------------------------|
| <span data-ttu-id="bf216-167">Tapahtumaluokat</span><span class="sxs-lookup"><span data-stu-id="bf216-167">Transaction categories</span></span>     | <span data-ttu-id="bf216-168">Luokkien integrointiyksikkö</span><span class="sxs-lookup"><span data-stu-id="bf216-168">Integration entity for categories</span></span> |

### <a name="entity-flow"></a><span data-ttu-id="bf216-169">Yksikön työnkulku</span><span class="sxs-lookup"><span data-stu-id="bf216-169">Entity flow</span></span>

<span data-ttu-id="bf216-170">Projektin kululuokkia tietoja hallitaan Financessa ja ne synkronoidaan Project Service Automationiin tapahtumaluokkina.</span><span class="sxs-lookup"><span data-stu-id="bf216-170">Project expense categories are managed in Finance, and they are synchronized to Project Service Automation as transaction categories.</span></span> <span data-ttu-id="bf216-171">Synkronointi takaisin Financeen päivittää projektiluokan Financessa Project Service Automationin integrointitunnuksella.</span><span class="sxs-lookup"><span data-stu-id="bf216-171">The synchronization back to Finance updates the project category in Finance with the integration ID from Project Service Automation.</span></span>

### <a name="template-mapping-in-data-integration"></a><span data-ttu-id="bf216-172">Mallin yhdistäminen tietojen integroinnin yhteydessä</span><span class="sxs-lookup"><span data-stu-id="bf216-172">Template mapping in Data integration</span></span>

<span data-ttu-id="bf216-173">Seuraavassa kuvassa on esimerkki mallitehtävän yhdistämisestä tietojen integroinnin yhteydessä.</span><span class="sxs-lookup"><span data-stu-id="bf216-173">The following illustration shows an example of the template task mapping in Data integration.</span></span>

> [!NOTE]
> <span data-ttu-id="bf216-174">Yhdistämismääritys näyttää Project Service Automationista Financeen synkronoitavien kenttien tiedot.</span><span class="sxs-lookup"><span data-stu-id="bf216-174">The mapping shows the field information that will be synchronized from Project Service Automation to Finance.</span></span>

<span data-ttu-id="bf216-175">[![Mallin yhdistäminen](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="bf216-175">[![Template mapping](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)</span></span>
