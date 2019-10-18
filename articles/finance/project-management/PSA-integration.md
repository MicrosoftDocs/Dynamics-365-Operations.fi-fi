---
title: Project Service Automationin yleiskatsaus
description: Tässä ohjeaiheessa on tietoja Dynamics 365 Project Service Automationin ja Dynamics 365 Financen integrointiratkaisusta.
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
ms.openlocfilehash: 31d72591041f8d8cc327aa7c6578c15731ba13c5
ms.sourcegitcommit: 2460d0da812c45fce67a061386db52e0ae46b0f3
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/30/2019
ms.locfileid: "2250550"
---
# <a name="project-service-automation-overview"></a><span data-ttu-id="7b910-103">Project Service Automationin yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="7b910-103">Project Service Automation overview</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="7b910-104">Project Service Automationin ja Financen välinen integrointiratkaisu synkronoi tietojen integrointitoiminnolla tietoja Dynamics 365 Financen ja Dynamics 365 Project Service Automationin esiintymien välillä Common Data Servicen kautta.</span><span class="sxs-lookup"><span data-stu-id="7b910-104">The Project Service Automation to Finance integration solution uses the Data integration feature to synchronize data across instances of Dynamics 365 Finance and Dynamics 365 Project Service Automation via Common Data Service.</span></span> <span data-ttu-id="7b910-105">Tietojen integrointiominaisuuteen sisältyvät integrointimallit mahdollistavat projekteja, projektisopimuksia, projektisopimuksen rivejä, projektisopimuksen rivien välitavoitteita, projektitehtäviä, kulutapahtumaluokkia, tuntiarvioita ja kuluarvioita koskevien tietojen siirtymisen Project Service Automationista Financeen.</span><span class="sxs-lookup"><span data-stu-id="7b910-105">The integration templates that are available with the Data integration feature enable the flow of projects, project contracts, project contract lines, project contract line milestones, project tasks, expense transaction categories, hour estimates, and expense estimates from Project Service Automation to Finance.</span></span>

> [!NOTE]
> - <span data-ttu-id="7b910-106">Jos käytät versiota 7.3.0, sinun on asennettava KB 4074835.</span><span class="sxs-lookup"><span data-stu-id="7b910-106">If you're using version 7.3.0, you must install KB 4074835.</span></span> <span data-ttu-id="7b910-107">Sen avulla voi integroida kiinteähintaisia projekteja.</span><span class="sxs-lookup"><span data-stu-id="7b910-107">You will then be able to integrate fixed price projects.</span></span>
> - <span data-ttu-id="7b910-108">Jos käytät versiota 7.3.0 ja tuot maksutapahtumia Project Service Automationista, sinun on asennettava KB 4345320, jotta maksut sisällytetään projektin laskuun.</span><span class="sxs-lookup"><span data-stu-id="7b910-108">If you're using version 7.3.0, and you are bringing fee transactions over from Project Service Automation, you must install KB 4345320 in order to include those fees in the project invoice.</span></span>
> - <span data-ttu-id="7b910-109">Jos käytä versiota 8.0, voit käyttää projektitehtävien integrointia, kulutapahtumaluokkia, tuntiarvioita, kuluarvioita ja toiminnon lukitsemista.</span><span class="sxs-lookup"><span data-stu-id="7b910-109">If you're using version 8.0, you will be able to use project task integration, expense transaction categories, hour estimates, expense estimates, and functionality locking.</span></span>
> - <span data-ttu-id="7b910-110">Jos käytät versiota 8.0.1 tai uudempaa, voit synkronoida todelliset tiedot.</span><span class="sxs-lookup"><span data-stu-id="7b910-110">If you're using version 8.0.1 or later, you will be able to synchronize actuals.</span></span>

<span data-ttu-id="7b910-111">Project Service Automationin integrointiparametrit on määritettävä ennen Project Service Automationin ja Financen integrointia.</span><span class="sxs-lookup"><span data-stu-id="7b910-111">Before you can integrate Project Service Automation Finance, you must configure the Project Service Automation integration parameters.</span></span> <span data-ttu-id="7b910-112">Lisätietoja on kohdassa [Project Service Automationin integrointiparametrit](PSA-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="7b910-112">For more information, see [Project Service Automation integration parameters](PSA-parameters.md).</span></span>

<span data-ttu-id="7b910-113">Integrointiratkaisu mahdollistaa suoran synkronoinnin seuraavissa skenaarioissa:</span><span class="sxs-lookup"><span data-stu-id="7b910-113">This integration solution enables direct synchronization in the following scenarios:</span></span>

- <span data-ttu-id="7b910-114">Projektisopimusten ylläpito Project Service Automationissa ja niiden synkronointi suoraan Project Service Automationista Financeen.</span><span class="sxs-lookup"><span data-stu-id="7b910-114">Maintain project contracts in Project Service Automation, and synchronize them directly from Project Service Automation to Finance.</span></span>
- <span data-ttu-id="7b910-115">Projektien luonti Project Service Automationissa ja niiden synkronointi suoraan Project Service Automationista Financeen.</span><span class="sxs-lookup"><span data-stu-id="7b910-115">Create projects in Project Service Automation, and synchronize them directly from Project Service Automation to Finance.</span></span>
- <span data-ttu-id="7b910-116">Projektisopimusten rivien ylläpito Project Service Automationissa ja niiden synkronointi suoraan Project Service Automationista Financeen.</span><span class="sxs-lookup"><span data-stu-id="7b910-116">Maintain project contract lines in Project Service Automation, and synchronize them directly from Project Service Automation to Finance.</span></span>
- <span data-ttu-id="7b910-117">Projektisopimusten rivien välitavoitteiden ylläpito Project Service Automationissa ja niiden synkronointi suoraan Project Service Automationista Financeen.</span><span class="sxs-lookup"><span data-stu-id="7b910-117">Maintain project contract line milestones in Project Service Automation, and synchronize them directly from Project Service Automation to Finance.</span></span>
- <span data-ttu-id="7b910-118">Projektitehtävien ylläpito Project Service Automationissa ja niiden synkronointi suoraan Project Service Automationista Financeen.</span><span class="sxs-lookup"><span data-stu-id="7b910-118">Maintain project tasks in Project Service Automation, and synchronize them directly from Project Service Automation to Finance.</span></span>
- <span data-ttu-id="7b910-119">Kulutapahtumaluokkien ylläpito Financessa ja niiden synkronointi suoraan Financesta Project Service Automationiin.</span><span class="sxs-lookup"><span data-stu-id="7b910-119">Maintain expense transaction categories in Finance, and synchronize them directly from Finance to Project Service Automation.</span></span>
- <span data-ttu-id="7b910-120">Projektin tuntiarvioiden luonti Project Service Automationissa ja niiden synkronointi suoraan Project Service Automationista Financeen.</span><span class="sxs-lookup"><span data-stu-id="7b910-120">Create project hour estimates in Project Service Automation, and synchronize them directly from Project Service Automation to Finance.</span></span>
- <span data-ttu-id="7b910-121">Projektin kuluarvioiden luonti Project Service Automationissa ja niiden synkronointi suoraan Project Service Automationista Financeen.</span><span class="sxs-lookup"><span data-stu-id="7b910-121">Create project expense estimates in Project Service Automation, and synchronize them directly from Project Service Automation to Finance.</span></span>
- <span data-ttu-id="7b910-122">Luo projektin aika, kulut ja todelliset maksut Project Service Automationissa ja luo projektitapahtumat Project Service Automationin integraatiokirjauskansiossa siten, että ne voidaan kirjataan Financeen.</span><span class="sxs-lookup"><span data-stu-id="7b910-122">Create project time, expense, and fee actuals in Project Service Automation, and create project transactions in the Project Service Automation integration journal so that they can be posted in Finance.</span></span>

## <a name="data-synchronization"></a><span data-ttu-id="7b910-123">Tietojen synkronointi</span><span class="sxs-lookup"><span data-stu-id="7b910-123">Data synchronization</span></span>

<span data-ttu-id="7b910-124">Seuraava kuva ilmaisee, miten tiedot synkronoidaan osana Project Service Automationin ja Financen välistä integrointia.</span><span class="sxs-lookup"><span data-stu-id="7b910-124">The following illustration shows how data is synchronized as part of the integration between Project Service Automation and Finance.</span></span>

> [!NOTE]
> <span data-ttu-id="7b910-125">Tällä hetkellä yhtään mallia ei ole käytettävissä.</span><span class="sxs-lookup"><span data-stu-id="7b910-125">Not all templates are currently available.</span></span> <span data-ttu-id="7b910-126">Mallit julkaistaan, kun ne valmistuvat.</span><span class="sxs-lookup"><span data-stu-id="7b910-126">Templates will be released as they are completed.</span></span>

<span data-ttu-id="7b910-127">[![Project Service Automationin ja Financen integrointi](./media/PSA-integration.png)](./media/PSA-integration.png)</span><span class="sxs-lookup"><span data-stu-id="7b910-127">[![Project Service Automation integration with Finance](./media/PSA-integration.png)](./media/PSA-integration.png)</span></span>

## <a name="system-requirements-for-finance"></a><span data-ttu-id="7b910-128">Financen järjestelmävaatimukset</span><span class="sxs-lookup"><span data-stu-id="7b910-128">System requirements for Finance</span></span>

<span data-ttu-id="7b910-129">Project Service Automationin ja Financen välisen integrointiratkaisua varten on asennettava Enterprise edition 7.3, jossa on ympäristöpäivitys 12 tai uudempi.</span><span class="sxs-lookup"><span data-stu-id="7b910-129">To use the Project Service Automation to Finance integration solution, you must install Enterprise edition 7.3 with Platform update 12 or later.</span></span>

## <a name="system-requirements-for-project-service-automation"></a><span data-ttu-id="7b910-130">Project Service Automationin järjestelmävaatimukset</span><span class="sxs-lookup"><span data-stu-id="7b910-130">System requirements for Project Service Automation</span></span>

<span data-ttu-id="7b910-131">Project Service Automationin ja Financen välisen integrointiratkaisun käyttöä varten on asennettava seuraavat osat:</span><span class="sxs-lookup"><span data-stu-id="7b910-131">To use the Project Service Automation to Finance integration solution, you must install the following components:</span></span>

- <span data-ttu-id="7b910-132">Dynamics 365 Project Service Automation versio 9.0.0.0 tai uudempi</span><span class="sxs-lookup"><span data-stu-id="7b910-132">Dynamics 365 Project Service Automation version 9.0.0.0 or later</span></span>
- <span data-ttu-id="7b910-133">Dynamics 365 Salesin Prospektista käteiseksi -ratkaisu, versio 1.14.0.0 (v14) tai uudempi</span><span class="sxs-lookup"><span data-stu-id="7b910-133">Prospect to cash solution for Dynamics 365 Sales, version 1.14.0.0 (v14) or later</span></span>
- <span data-ttu-id="7b910-134">Project Service Automationista Financeen -ratkaisu Dynamics 365 Project Service Automation -versiolle 1.0.0.0 tai uudemmalle</span><span class="sxs-lookup"><span data-stu-id="7b910-134">Project Service Automation to Finance solution for Dynamics 365 Project Service Automation version 1.0.0.0 or later</span></span>

## <a name="install-the-project-service-automation-to-finance-integration-solution-in-your-project-service-automation-instance"></a><span data-ttu-id="7b910-135">Asenna Project Service Automationin ja Financen välinen integrointiratkaisu Project Service Automationin esiintymään</span><span class="sxs-lookup"><span data-stu-id="7b910-135">Install the Project Service Automation to Finance integration solution in your Project Service Automation instance</span></span>

<span data-ttu-id="7b910-136">Lataa Project Service Automationin ja Financen välinen integrointiratkaisu [Microsoft Download Center](https://www.microsoft.com/download/details.aspx?id=57016) -sivulta ja noudata ratkaisun mukana olevia ohjeita.</span><span class="sxs-lookup"><span data-stu-id="7b910-136">Download the Project Service Automation to Finance integration solution from [Microsoft Download Center](https://www.microsoft.com/download/details.aspx?id=57016), and follow the instructions that are included with the solution.</span></span>
