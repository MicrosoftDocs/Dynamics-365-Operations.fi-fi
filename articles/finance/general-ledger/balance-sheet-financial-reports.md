---
title: Taseen talousraportit
description: Tässä artikkelissa kuvataan taseiden oletusraportteja. Siinä myös kuvataan rakenneosat, jotka liittyvät näihin raportteihin.
author: jcart1106
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: FinanicalReports
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 12274
ms.assetid: 52f78229-f531-4d16-b337-e2628994acb6
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d9dcac902118c643b9a9d783c12f02fa5c90827b
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/27/2019
ms.locfileid: "2177502"
---
# <a name="balance-sheet-financial-reports"></a><span data-ttu-id="a49f1-104">Taseen talousraportit</span><span class="sxs-lookup"><span data-stu-id="a49f1-104">Balance sheet financial reports</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a49f1-105">Tässä artikkelissa kuvataan taseiden oletusraportteja.</span><span class="sxs-lookup"><span data-stu-id="a49f1-105">This article describes the default reports for balance sheets.</span></span> <span data-ttu-id="a49f1-106">Siinä myös kuvataan rakenneosat, jotka liittyvät näihin raportteihin.</span><span class="sxs-lookup"><span data-stu-id="a49f1-106">It also describes the building blocks that are associated with these reports.</span></span> 

<a name="default-balance-sheet-reports"></a><span data-ttu-id="a49f1-107">Oletustaseraportit</span><span class="sxs-lookup"><span data-stu-id="a49f1-107">Default balance sheet reports</span></span>
-----------------------------

<span data-ttu-id="a49f1-108">Oletustaseraportteja on kaksi.</span><span class="sxs-lookup"><span data-stu-id="a49f1-108">There are two default balance sheet reports.</span></span> <span data-ttu-id="a49f1-109">Osat on pinottu yhteen raporttiin.</span><span class="sxs-lookup"><span data-stu-id="a49f1-109">On one report, the sections are stacked.</span></span> <span data-ttu-id="a49f1-110">Osat ovat rinnakkain raportissa.</span><span class="sxs-lookup"><span data-stu-id="a49f1-110">On the other report, the sections are side by side.</span></span>

| <span data-ttu-id="a49f1-111">Oletusraportti</span><span class="sxs-lookup"><span data-stu-id="a49f1-111">Default report</span></span>                       | <span data-ttu-id="a49f1-112">Toiminnot</span><span class="sxs-lookup"><span data-stu-id="a49f1-112">What it does</span></span>                                                                                                                           |
|--------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a49f1-113">Tase – oletus</span><span class="sxs-lookup"><span data-stu-id="a49f1-113">Balance Sheet – Default</span></span>              | <span data-ttu-id="a49f1-114">Määrittää organisaation vuoden rahoitusaseman näkymän.</span><span class="sxs-lookup"><span data-stu-id="a49f1-114">Provides a view of the organization's financial position for the year.</span></span>                                                                 |
| <span data-ttu-id="a49f1-115">Tase rinnakkain – oletus</span><span class="sxs-lookup"><span data-stu-id="a49f1-115">Side by Side Balance Sheet – Default</span></span> | <span data-ttu-id="a49f1-116">Määrittää organisaation vuoden rahoitusaseman näkymän.</span><span class="sxs-lookup"><span data-stu-id="a49f1-116">Provides a view of the organization's financial position for the year.</span></span> <span data-ttu-id="a49f1-117">Käyttöomaisuus, velat ja osakkeenomistajien oma pääoma ovat rinnakkain.</span><span class="sxs-lookup"><span data-stu-id="a49f1-117">Assets and liability and shareholder’s equity are side by side.</span></span> |

## <a name="building-blocks"></a><span data-ttu-id="a49f1-118">Rakenneosat</span><span class="sxs-lookup"><span data-stu-id="a49f1-118">Building blocks</span></span>
<span data-ttu-id="a49f1-119">Taseen talousraporteissa käytetään seuraavia rakenneosia.</span><span class="sxs-lookup"><span data-stu-id="a49f1-119">The balance sheet financial reports use the following building blocks.</span></span>

| <span data-ttu-id="a49f1-120">Oletusraportti</span><span class="sxs-lookup"><span data-stu-id="a49f1-120">Default report</span></span>                       | <span data-ttu-id="a49f1-121">Rivimääritys</span><span class="sxs-lookup"><span data-stu-id="a49f1-121">Row definition</span></span>                       | <span data-ttu-id="a49f1-122">Sarakemääritys</span><span class="sxs-lookup"><span data-stu-id="a49f1-122">Column definition</span></span>             |
|--------------------------------------|--------------------------------------|-------------------------------|
| <span data-ttu-id="a49f1-123">Tase - oletusarvo</span><span class="sxs-lookup"><span data-stu-id="a49f1-123">Balance Sheet - Default</span></span>              | <span data-ttu-id="a49f1-124">Tase - oletusarvo</span><span class="sxs-lookup"><span data-stu-id="a49f1-124">Balance Sheet - Default</span></span>              | <span data-ttu-id="a49f1-125">Vuoden alusta ja varianssi - oletusarvo</span><span class="sxs-lookup"><span data-stu-id="a49f1-125">YTD and Variance - Default</span></span>    |
| <span data-ttu-id="a49f1-126">Tase rinnakkain – oletus</span><span class="sxs-lookup"><span data-stu-id="a49f1-126">Side by Side Balance Sheet – Default</span></span> | <span data-ttu-id="a49f1-127">Tase rinnakkain – oletus</span><span class="sxs-lookup"><span data-stu-id="a49f1-127">Side by Side Balance Sheet – Default</span></span> | <span data-ttu-id="a49f1-128">Vuoden alusta -sarake - oletusarvo</span><span class="sxs-lookup"><span data-stu-id="a49f1-128">Year to Date Column - Default</span></span> |

### <a name="row-definition"></a><span data-ttu-id="a49f1-129">Rivimääritys</span><span class="sxs-lookup"><span data-stu-id="a49f1-129">Row definition</span></span>

<span data-ttu-id="a49f1-130">Molempien taseraporttien rivimääritykset sisältävät osia kunkin perinteisen taseen osista.</span><span class="sxs-lookup"><span data-stu-id="a49f1-130">The row definitions for both balance sheet reports contain sections for each part of a traditional balance sheet.</span></span> <span data-ttu-id="a49f1-131">Rinnakkainen raportti sisältää sarakkeen vaihdon, jolloin velat ja omistajan oma pääoma näkyvät käyttöomaisuuden vieressä.</span><span class="sxs-lookup"><span data-stu-id="a49f1-131">The side-by-side report includes a column break, so that liability and the owner’s equity appear next to assets.</span></span> <span data-ttu-id="a49f1-132">Päätilin luokan dimensiota käytetään molempien rivimääritysten muodostamisessa.</span><span class="sxs-lookup"><span data-stu-id="a49f1-132">The Main Account Category dimension is used to build both row definitions.</span></span> <span data-ttu-id="a49f1-133">Tämän vuoksi kuka tahansa voi luoda raportteja ilman muutosten tekemistä.</span><span class="sxs-lookup"><span data-stu-id="a49f1-133">Therefore, anyone can generate the reports without having to make any modifications.</span></span>

### <a name="column-definition"></a><span data-ttu-id="a49f1-134">Sarakemääritys</span><span class="sxs-lookup"><span data-stu-id="a49f1-134">Column definition</span></span>

<span data-ttu-id="a49f1-135">Sarakemääritykset sisältävät erityppisiä sarakkeita, joissa on useita yksityiskohtaisia tasoja ja taloushallinnon tietoja.</span><span class="sxs-lookup"><span data-stu-id="a49f1-135">The column definitions contain different types of columns to provide different levels of detail and financial data.</span></span>

-   <span data-ttu-id="a49f1-136">**Vuoden alusta ja varianssi – oletussaraketyypit:**</span><span class="sxs-lookup"><span data-stu-id="a49f1-136">**YTD and Variance – Default column types:**</span></span>
    -   <span data-ttu-id="a49f1-137">**DESC** – rivimäärityksen kuvaus</span><span class="sxs-lookup"><span data-stu-id="a49f1-137">**DESC** – The description from the row definition</span></span>
    -   <span data-ttu-id="a49f1-138">**FD** – kuluvan vuoden taloushallinnon tiedot vuoden alusta</span><span class="sxs-lookup"><span data-stu-id="a49f1-138">**FD** – Year-to-date financial data for the current year</span></span>
    -   <span data-ttu-id="a49f1-139">**FD** – edellisen vuoden taloushallinnon tiedot vuoden alusta</span><span class="sxs-lookup"><span data-stu-id="a49f1-139">**FD** – Year-to-date financial data for the last year</span></span>
    -   <span data-ttu-id="a49f1-140">**CALC** – varianssi, kun kuluva vuosi vähennetään edellisestä vuodesta</span><span class="sxs-lookup"><span data-stu-id="a49f1-140">**CALC** – The variance from subtracting last year from this year</span></span>

<!-- -->

-   <span data-ttu-id="a49f1-141">**Vuoden alusta -sarake – oletusarvo**</span><span class="sxs-lookup"><span data-stu-id="a49f1-141">**Year to Date Column – Default:**</span></span>
    -   <span data-ttu-id="a49f1-142">**DESC** – rivimäärityksen kuvaus</span><span class="sxs-lookup"><span data-stu-id="a49f1-142">**DESC** – The description from the row definition</span></span>
    -   <span data-ttu-id="a49f1-143">**FD** – kuluvan vuoden taloushallinnon tiedot vuoden alusta</span><span class="sxs-lookup"><span data-stu-id="a49f1-143">**FD** – Year-to-date financial data for the current year</span></span>



<a name="additional-resources"></a><span data-ttu-id="a49f1-144">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="a49f1-144">Additional resources</span></span>
--------

[<span data-ttu-id="a49f1-145">Talousraportointi</span><span class="sxs-lookup"><span data-stu-id="a49f1-145">Financial reporting</span></span>](financial-reporting-getting-started.md)

[<span data-ttu-id="a49f1-146">Raporttien näyttäminen</span><span class="sxs-lookup"><span data-stu-id="a49f1-146">View financial reports</span></span>](view-financial-reports.md)

[<span data-ttu-id="a49f1-147">Dynamicsin talousraportointi -blogi</span><span class="sxs-lookup"><span data-stu-id="a49f1-147">Dynamics Financial Reporting Blog</span></span>](https://blogs.msdn.com/b/dynamics_financial_reporting/)


