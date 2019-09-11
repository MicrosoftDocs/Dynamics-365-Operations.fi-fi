---
title: Project Service Automation – yleiskatsaus
description: Tässä ohjeaiheessa on tietoja Project Service Automation to Finance and Operationsin integraatioratkaisuista. Tämä integraatioratkaisu synkronoi tietojen integrointitoiminnolla tietoja Microsoft Dynamics 365 for Finance and Operationsin ja Microsoft Dynamics 365 for Project Service Automationin esiintymien välillä Common Data Servicen kautta.
author: KimANelson
manager: AnnBe
ms.date: 07/25/2019
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
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 85dde35033122ad234ec8efd1bddf64b950578ef
ms.sourcegitcommit: e286572ce94a9442a5b3076c3ff5b429be0ed512
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/06/2019
ms.locfileid: "1865625"
---
# <a name="project-service-automation-overview"></a><span data-ttu-id="f3dee-104">Project Service Automation – yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="f3dee-104">Project Service Automation overview</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="f3dee-105">Project Service Automationin ja Finance and Operationsin välinen integrointiratkaisu synkronoi tietojen integrointitoiminnolla tietoja Microsoft Dynamics 365 for Finance and Operationsin ja Microsoft Dynamics 365 for Project Service Automationin esiintymien välillä Common Data Servicen kautta.</span><span class="sxs-lookup"><span data-stu-id="f3dee-105">The Project Service Automation to Finance and Operations integration solution uses the Data integration feature to synchronize data across instances of Microsoft Dynamics 365 for Finance and Operations and Microsoft Dynamics 365 for Project Service Automation via Common Data Service.</span></span> <span data-ttu-id="f3dee-106">Tietojen integrointiominaisuuteen sisältyvät integrointimallit mahdollistavat projekteja, projektisopimuksia, projektisopimuksen rivejä, projektisopimuksen rivien välitavoitteita, projektitehtäviä, kulutapahtumaluokkia, tuntiarvioita ja kuluarvioita koskevien tietojen siirtymisen Project Service Automationista Finance and Operationsiin.</span><span class="sxs-lookup"><span data-stu-id="f3dee-106">The integration templates that are available with the Data integration feature enable the flow of projects, project contracts, project contract lines, project contract line milestones, project tasks, expense transaction categories, hour estimates, and expense estimates from Project Service Automation to Finance and Operations.</span></span>

> [!NOTE]
> - <span data-ttu-id="f3dee-107">Jos käytössä on Microsoft Dynamics 365 for Finance and Operations, Enterprise edition 7.3.0 ja KB 4132657 ja KB 4132660 on asennettu, voit integroida projektitehtäviä, kulutapahtumaluokkia, tuntiarvioita, kuluarvioita ja todellisia tietoja sekä määrittää toimintojen lukituksen.</span><span class="sxs-lookup"><span data-stu-id="f3dee-107">If you're using Microsoft Dynamics 365 for Finance and Operations, Enterprise edition 7.3.0, after you install KB 4132657 and KB 4132660, you will be able to use the templates to integrate project tasks, expense transaction categories, hour estimates, expense estimates, and actuals, and to configure functionality locking.</span></span> <span data-ttu-id="f3dee-108">Jos kirjanpidollinen jako on palautettava alkuperäisasetuksiin, myös KB 4131710 kannattaa asentaa.</span><span class="sxs-lookup"><span data-stu-id="f3dee-108">If you must reset the accounting distributions, we recommend that you also install KB 4131710.</span></span>
> - <span data-ttu-id="f3dee-109">Jos käytät Finance and Operations 7.3.0 -versiota, sinun on asennettava KB 4074835.</span><span class="sxs-lookup"><span data-stu-id="f3dee-109">If you're using Finance and Operations 7.3.0, you must install KB 4074835.</span></span> <span data-ttu-id="f3dee-110">Sen avulla voi integroida kiinteähintaisia projekteja.</span><span class="sxs-lookup"><span data-stu-id="f3dee-110">You will then be able to integrate fixed price projects.</span></span>
> - <span data-ttu-id="f3dee-111">Jos käytät Finance and Operations 7.3.0:aa ja tuot maksutapahtumia Project Service Automationista, sinun on asennettava KB 4345320, jotta maksut sisällytetään projektin laskuun.</span><span class="sxs-lookup"><span data-stu-id="f3dee-111">If you're using Finance and Operations 7.3.0, and you are bringing fee transactions over from Project Service Automation, you must install KB 4345320 in order to include those fees in the project invoice.</span></span>
> - <span data-ttu-id="f3dee-112">Jos käytössä on Microsoft Dynamics 365 for Finance and Operationsin versio 8.0, voit käyttää projektitehtävien integrointia, kulutapahtumaluokkia, tuntiarvioita, kuluarvioita ja toiminnon lukitsemista.</span><span class="sxs-lookup"><span data-stu-id="f3dee-112">If you're using Microsoft Dynamics 365 for Finance and Operations version 8.0, you will be able to use project task integration, expense transaction categories, hour estimates, expense estimates, and functionality locking.</span></span>
> - <span data-ttu-id="f3dee-113">Jos käytössä on Microsoft Dynamics 365 for Finance and Operationsin versio 8.0.1 tai uudempi, voit synkronoida todelliset tiedot.</span><span class="sxs-lookup"><span data-stu-id="f3dee-113">If you're using Microsoft Dynamics 365 for Finance and Operations version 8.0.1, or later, you will be able to synchronize actuals.</span></span>

<span data-ttu-id="f3dee-114">Project Service Automationin integrointiparametrit on määritettävä ennen Project Service Automationin ja Finance and Operationsin integrointia.</span><span class="sxs-lookup"><span data-stu-id="f3dee-114">Before you can integrate Project Service Automation with Finance and Operations, you must configure the Project Service Automation integration parameters.</span></span> <span data-ttu-id="f3dee-115">Lisätietoja on kohdassa [Project Service Automationin integrointiparametrit](PSA-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="f3dee-115">For more information, see [Project Service Automation integration parameters](PSA-parameters.md).</span></span>

<span data-ttu-id="f3dee-116">Integrointiratkaisu mahdollistaa suoran synkronoinnin seuraavissa skenaarioissa:</span><span class="sxs-lookup"><span data-stu-id="f3dee-116">This integration solution enables direct synchronization in the following scenarios:</span></span>

- <span data-ttu-id="f3dee-117">Projektisopimusten ylläpito Project Service Automationissa ja niiden synkronointi suoraan Project Service Automationista Finance and Operationsiin.</span><span class="sxs-lookup"><span data-stu-id="f3dee-117">Maintain project contracts in Project Service Automation, and synchronize them directly from Project Service Automation to Finance and Operations.</span></span>
- <span data-ttu-id="f3dee-118">Projektien luonti Project Service Automationissa ja niiden synkronointi suoraan Project Service Automationista Finance and Operationsiin.</span><span class="sxs-lookup"><span data-stu-id="f3dee-118">Create projects in Project Service Automation, and synchronize them directly from Project Service Automation to Finance and Operations.</span></span>
- <span data-ttu-id="f3dee-119">Projektisopimuksen rivien ylläpito Project Service Automationissa ja niiden synkronointi suoraan Project Service Automationista Finance and Operationsiin.</span><span class="sxs-lookup"><span data-stu-id="f3dee-119">Maintain project contract lines in Project Service Automation, and synchronize them directly from Project Service Automation to Finance and Operations.</span></span>
- <span data-ttu-id="f3dee-120">Projektisopimuksen rivien välitavoitteiden ylläpito Project Service Automationissa ja niiden synkronointi suoraan Project Service Automationista Finance and Operationsiin.</span><span class="sxs-lookup"><span data-stu-id="f3dee-120">Maintain project contract line milestones in Project Service Automation, and synchronize them directly from Project Service Automation to Finance and Operations.</span></span>
- <span data-ttu-id="f3dee-121">Projektitehtävien ylläpito Project Service Automationissa ja niiden synkronointi suoraan Project Service Automationista Finance and Operationsiin.</span><span class="sxs-lookup"><span data-stu-id="f3dee-121">Maintain project tasks in Project Service Automation, and synchronize them directly from Project Service Automation to Finance and Operations.</span></span>
- <span data-ttu-id="f3dee-122">Kulutapahtumaluokkien ylläpito Finance and Operationsissa ja niiden synkronointi suoraan Finance and Operationsista Project Service Automationiin.</span><span class="sxs-lookup"><span data-stu-id="f3dee-122">Maintain expense transaction categories in Finance and Operations, and synchronize them directly from Finance and Operations to Project Service Automation.</span></span>
- <span data-ttu-id="f3dee-123">Projektin tuntiarvioiden luonti Project Service Automationissa ja niiden synkronointi suoraan Project Service Automationista Finance and Operationsiin.</span><span class="sxs-lookup"><span data-stu-id="f3dee-123">Create project hour estimates in Project Service Automation, and synchronize them directly from Project Service Automation to Finance and Operations.</span></span>
- <span data-ttu-id="f3dee-124">Projektin kuluarvioiden luonti Project Service Automationissa ja niiden synkronointi suoraan Project Service Automationista Finance and Operationsiin.</span><span class="sxs-lookup"><span data-stu-id="f3dee-124">Create project expense estimates in Project Service Automation, and synchronize them directly from Project Service Automation to Finance and Operations.</span></span>
- <span data-ttu-id="f3dee-125">Luo projektin aika, kulut ja todelliset maksut Project Service Automationissa ja luo projektitapahtumat Project Service Automationin integraatiokirjauskansiossa siten, että ne voidaan kirjataan Finance and Operationsiin.</span><span class="sxs-lookup"><span data-stu-id="f3dee-125">Create project time, expense, and fee actuals in Project Service Automation, and create project transactions in the Project Service Automation integration journal so that they can be posted in Finance and Operations.</span></span>

## <a name="data-synchronization"></a><span data-ttu-id="f3dee-126">Tietojen synkronointi</span><span class="sxs-lookup"><span data-stu-id="f3dee-126">Data synchronization</span></span>

<span data-ttu-id="f3dee-127">Seuraava kuva ilmaisee, miten tiedot synkronoidaan osana Project Service Automationin ja Finance and Operationsin välistä integrointia.</span><span class="sxs-lookup"><span data-stu-id="f3dee-127">The following illustration shows how data is synchronized as part of the integration between Project Service Automation and Finance and Operations.</span></span>

> [!NOTE]
> <span data-ttu-id="f3dee-128">Tällä hetkellä yhtään mallia ei ole käytettävissä.</span><span class="sxs-lookup"><span data-stu-id="f3dee-128">Not all templates are currently available.</span></span> <span data-ttu-id="f3dee-129">Mallit julkaistaan, kun ne valmistuvat.</span><span class="sxs-lookup"><span data-stu-id="f3dee-129">Templates will be released as they are completed.</span></span>

<span data-ttu-id="f3dee-130">[![Project Service Automationin ja Finance and Operationsin integrointi](./media/PSA-integration.png)](./media/PSA-integration.png)</span><span class="sxs-lookup"><span data-stu-id="f3dee-130">[![Project Service Automation integration with Finance and Operations](./media/PSA-integration.png)](./media/PSA-integration.png)</span></span>

## <a name="system-requirements-for-finance-and-operations"></a><span data-ttu-id="f3dee-131">Finance and Operations -sovelluksen järjestelmävaatimukset</span><span class="sxs-lookup"><span data-stu-id="f3dee-131">System requirements for Finance and Operations</span></span>

<span data-ttu-id="f3dee-132">Project Service Automationin ja Finance and Operationsin välisen integrointiratkaisua varten on asennettava Microsoft Dynamics 365 for Finance and Operations, Enterprise edition 7.3, jossa on vähintään ympäristöpäivitys 12.</span><span class="sxs-lookup"><span data-stu-id="f3dee-132">To use the Project Service Automation to Finance and Operations integration solution, you must install Microsoft Dynamics 365 for Finance and Operations, Enterprise edition 7.3 with platform update 12 or later.</span></span>

## <a name="system-requirements-for-project-service-automation"></a><span data-ttu-id="f3dee-133">Project Service Automationin järjestelmävaatimukset</span><span class="sxs-lookup"><span data-stu-id="f3dee-133">System requirements for Project Service Automation</span></span>

<span data-ttu-id="f3dee-134">Project Service Automationin ja Finance and Operationsin välisen integrointiratkaisun käyttöä varten on asennettava seuraavat osat:</span><span class="sxs-lookup"><span data-stu-id="f3dee-134">To use the Project Service Automation to Finance and Operations integration solution, you must install the following components:</span></span>

- <span data-ttu-id="f3dee-135">Microsoft Dynamics 365 for Project Service Automation versio 9.0.0.0 tai uudempi</span><span class="sxs-lookup"><span data-stu-id="f3dee-135">Microsoft Dynamics 365 for Project Service Automation version 9.0.0.0 or later</span></span>
- <span data-ttu-id="f3dee-136">Microsoft Dynamics 365 for Salesin prospektista käteiseksi -ratkaisu, versio 1.14.0.0 (14) tai uudempi</span><span class="sxs-lookup"><span data-stu-id="f3dee-136">Prospect to cash solution for Microsoft Dynamics 365 for Sales, version 1.14.0.0 (v14) or later</span></span>
- <span data-ttu-id="f3dee-137">Microsoft Dynamics 365 for Project Service Automationin version 1.0.0.0 tai uudemman ratkaisu Project Service Automationista Finance and Operationsiin</span><span class="sxs-lookup"><span data-stu-id="f3dee-137">Project Service Automation to Finance and Operations solution for Microsoft Dynamics 365 for Project Service Automation version 1.0.0.0 or later</span></span>

## <a name="install-the-project-service-automation-to-finance-and-operations-integration-solution-in-your-project-service-automation-instance"></a><span data-ttu-id="f3dee-138">Asenna Project Service Automationin ja Finance and Operationsin välinen integrointiratkaisu Project Service Automationin esiintymään.</span><span class="sxs-lookup"><span data-stu-id="f3dee-138">Install the Project Service Automation to Finance and Operations integration solution in your Project Service Automation instance</span></span>

<span data-ttu-id="f3dee-139">Lataa Project Service Automation to Finance and Operationsin integrointiratkaisu [Microsoft Download Center](https://www.microsoft.com/download/details.aspx?id=57016) -sivulta, ja seuraa ratkaisun mukana olevia ohjeita.</span><span class="sxs-lookup"><span data-stu-id="f3dee-139">Download the Project Service Automation to Finance and Operations integration solution from [Microsoft Download Center](https://www.microsoft.com/download/details.aspx?id=57016), and follow the instructions that are included with the solution.</span></span>
