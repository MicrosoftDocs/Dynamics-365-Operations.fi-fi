---
title: Tuloslaskelman talousraportti
description: "Tässä artikkelissa kuvataan tuloilmoituksen oletusraporttia. Siinä myös kuvataan rakenneosat, jotka liittyvät tähän raporttiin."
author: jcart1106
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 12294
ms.assetid: 30820be0-d943-4f8b-8c25-6414ec393b3d
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 0017d13b7f7594462dfff4ef896f4139607d4bc5
ms.contentlocale: fi-fi
ms.lasthandoff: 08/29/2017

---

# <a name="income-statement-financial-report"></a><span data-ttu-id="236a0-104">Tuloslaskelman talousraportti</span><span class="sxs-lookup"><span data-stu-id="236a0-104">Income statement financial report</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="236a0-105">Tässä artikkelissa kuvataan tuloilmoituksen oletusraporttia.</span><span class="sxs-lookup"><span data-stu-id="236a0-105">This article describes the default report for income statements.</span></span> <span data-ttu-id="236a0-106">Siinä myös kuvataan rakenneosat, jotka liittyvät tähän raporttiin.</span><span class="sxs-lookup"><span data-stu-id="236a0-106">It also describes the building blocks that are associated with this report.</span></span> 

<a name="default-income-statement-report"></a><span data-ttu-id="236a0-107">Tuloslaskelman oletusraportti</span><span class="sxs-lookup"><span data-stu-id="236a0-107">Default income statement report</span></span>
-------------------------------

| <span data-ttu-id="236a0-108">Oletusraportti</span><span class="sxs-lookup"><span data-stu-id="236a0-108">Default report</span></span>             | <span data-ttu-id="236a0-109">Toiminnot</span><span class="sxs-lookup"><span data-stu-id="236a0-109">What it does</span></span>                                                                                              |
|----------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="236a0-110">Tuloslaskelma – oletus</span><span class="sxs-lookup"><span data-stu-id="236a0-110">Income Statement – Default</span></span> | <span data-ttu-id="236a0-111">Sisältää organisaation tuottavuusnäkymän sekä kuluvalle kaudelle että vuoden alusta tähän asti.</span><span class="sxs-lookup"><span data-stu-id="236a0-111">Provides a view of the organization’s profitability for the current period and also for the year to date.</span></span> |

## <a name="building-blocks"></a><span data-ttu-id="236a0-112">Rakenneosat</span><span class="sxs-lookup"><span data-stu-id="236a0-112">Building blocks</span></span>
<span data-ttu-id="236a0-113">Tuloslaskelman talousraportissa käytetään seuraavia rakenneosia.</span><span class="sxs-lookup"><span data-stu-id="236a0-113">The income statement financial report uses the following building blocks.</span></span>

| <span data-ttu-id="236a0-114">Oletusraportti</span><span class="sxs-lookup"><span data-stu-id="236a0-114">Default report</span></span>             | <span data-ttu-id="236a0-115">Rivimääritys</span><span class="sxs-lookup"><span data-stu-id="236a0-115">Row definition</span></span>                     | <span data-ttu-id="236a0-116">Sarakemääritys</span><span class="sxs-lookup"><span data-stu-id="236a0-116">Column definition</span></span>          |
|----------------------------|------------------------------------|----------------------------|
| <span data-ttu-id="236a0-117">Tuloslaskelma - oletus</span><span class="sxs-lookup"><span data-stu-id="236a0-117">Income Statement - Default</span></span> | <span data-ttu-id="236a0-118">Yhteenvetotuloslaskelma - oletus</span><span class="sxs-lookup"><span data-stu-id="236a0-118">Summary Income Statement - Default</span></span> | <span data-ttu-id="236a0-119">Kausittainen ja vuoden alusta - oletusarvo</span><span class="sxs-lookup"><span data-stu-id="236a0-119">Periodic and YTD - Default</span></span> |

### <a name="row-definition"></a><span data-ttu-id="236a0-120">Rivimääritys</span><span class="sxs-lookup"><span data-stu-id="236a0-120">Row definition</span></span>

<span data-ttu-id="236a0-121">Rivimääritys, yhteenvetotuloslaskelma – oletusarvo, sisältää osan perinteisen tuloslaskelman jokaiselle osalle.</span><span class="sxs-lookup"><span data-stu-id="236a0-121">The row definition, Summary Income Statement – Default, contains a section for each part of a traditional income statement.</span></span> <span data-ttu-id="236a0-122">Päätilin luokan dimensiota käytetään tämän rivimäärityksen muodostamisessa.</span><span class="sxs-lookup"><span data-stu-id="236a0-122">The Main Account Category dimension is used to build this row definition.</span></span> <span data-ttu-id="236a0-123">Tämän vuoksi kuka tahansa voi luoda raportin ilman muutosten tekemistä.</span><span class="sxs-lookup"><span data-stu-id="236a0-123">Therefore, anyone can generate the report without having to make any modifications.</span></span>

### <a name="column-definition"></a><span data-ttu-id="236a0-124">Sarakemääritys</span><span class="sxs-lookup"><span data-stu-id="236a0-124">Column Definition</span></span>

<span data-ttu-id="236a0-125">Sarakemääritykset sisältävät erityppisiä sarakkeita, joissa on useita yksityiskohtaisia tasoja ja taloushallinnon tietoja.</span><span class="sxs-lookup"><span data-stu-id="236a0-125">The column definitions contain different types of columns to provide different levels of detail and financial data.</span></span>

-   <span data-ttu-id="236a0-126">**Kausittainen ja vuoden alusta – oletussaraketyypit:**</span><span class="sxs-lookup"><span data-stu-id="236a0-126">**Periodic and YTD – Default column types:**</span></span>
    -   <span data-ttu-id="236a0-127">**DESC** – rivimäärityksen kuvaus</span><span class="sxs-lookup"><span data-stu-id="236a0-127">**DESC** – The description from the row definition</span></span>
    -   <span data-ttu-id="236a0-128">**FD** – nykyisen kauden taloushallinnon tiedot</span><span class="sxs-lookup"><span data-stu-id="236a0-128">**FD** – Financial data for the current period</span></span>
    -   <span data-ttu-id="236a0-129">**FD** – taloushallinnon tiedot vuoden alusta</span><span class="sxs-lookup"><span data-stu-id="236a0-129">**FD** – Financial data for the year to date</span></span>

 

<a name="see-also"></a><span data-ttu-id="236a0-130">Lisätietoja</span><span class="sxs-lookup"><span data-stu-id="236a0-130">See also</span></span>
--------

[<span data-ttu-id="236a0-131">Talousraportointi</span><span class="sxs-lookup"><span data-stu-id="236a0-131">Financial reporting</span></span>](financial-reporting-getting-started.md)

[<span data-ttu-id="236a0-132">Raporttien näyttäminen</span><span class="sxs-lookup"><span data-stu-id="236a0-132">View financial reports</span></span>](view-financial-reports.md)

[<span data-ttu-id="236a0-133">Dynamicsin talousraportointi -blogi</span><span class="sxs-lookup"><span data-stu-id="236a0-133">Dynamics Financial Reporting Blog</span></span>](http://blogs.msdn.com/b/dynamics_financial_reporting/)




