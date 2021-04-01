---
title: Tuloslaskelman talousraportti
description: Tässä artikkelissa kuvataan tuloilmoituksen oletusraporttia. Siinä myös kuvataan rakenneosat, jotka liittyvät tähän raporttiin.
author: jcart1106
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: FinancialReports
audience: Application User
ms.reviewer: roschlom
ms.custom: 12294
ms.assetid: 30820be0-d943-4f8b-8c25-6414ec393b3d
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: fab0e9d5e550b1848c3483b3172836e258353ebb
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5249068"
---
# <a name="income-statement-financial-report"></a><span data-ttu-id="f424c-104">Tuloslaskelman talousraportti</span><span class="sxs-lookup"><span data-stu-id="f424c-104">Income statement financial report</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f424c-105">Tässä artikkelissa kuvataan tuloilmoituksen oletusraporttia.</span><span class="sxs-lookup"><span data-stu-id="f424c-105">This article describes the default report for income statements.</span></span> <span data-ttu-id="f424c-106">Siinä myös kuvataan rakenneosat, jotka liittyvät tähän raporttiin.</span><span class="sxs-lookup"><span data-stu-id="f424c-106">It also describes the building blocks that are associated with this report.</span></span> 

<a name="default-income-statement-report"></a><span data-ttu-id="f424c-107">Tuloslaskelman oletusraportti</span><span class="sxs-lookup"><span data-stu-id="f424c-107">Default income statement report</span></span>
-------------------------------

| <span data-ttu-id="f424c-108">Oletusraportti</span><span class="sxs-lookup"><span data-stu-id="f424c-108">Default report</span></span>             | <span data-ttu-id="f424c-109">Toiminnot</span><span class="sxs-lookup"><span data-stu-id="f424c-109">What it does</span></span>                                                                                              |
|----------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f424c-110">Tuloslaskelma – oletus</span><span class="sxs-lookup"><span data-stu-id="f424c-110">Income Statement – Default</span></span> | <span data-ttu-id="f424c-111">Sisältää organisaation tuottavuusnäkymän sekä kuluvalle kaudelle että vuoden alusta tähän asti.</span><span class="sxs-lookup"><span data-stu-id="f424c-111">Provides a view of the organization’s profitability for the current period and also for the year to date.</span></span> |

## <a name="building-blocks"></a><span data-ttu-id="f424c-112">Rakenneosat</span><span class="sxs-lookup"><span data-stu-id="f424c-112">Building blocks</span></span>
<span data-ttu-id="f424c-113">Tuloslaskelman talousraportissa käytetään seuraavia rakenneosia.</span><span class="sxs-lookup"><span data-stu-id="f424c-113">The income statement financial report uses the following building blocks.</span></span>

| <span data-ttu-id="f424c-114">Oletusraportti</span><span class="sxs-lookup"><span data-stu-id="f424c-114">Default report</span></span>             | <span data-ttu-id="f424c-115">Rivimääritys</span><span class="sxs-lookup"><span data-stu-id="f424c-115">Row definition</span></span>                     | <span data-ttu-id="f424c-116">Sarakemääritys</span><span class="sxs-lookup"><span data-stu-id="f424c-116">Column definition</span></span>          |
|----------------------------|------------------------------------|----------------------------|
| <span data-ttu-id="f424c-117">Tuloslaskelma - oletus</span><span class="sxs-lookup"><span data-stu-id="f424c-117">Income Statement - Default</span></span> | <span data-ttu-id="f424c-118">Yhteenvetotuloslaskelma - oletus</span><span class="sxs-lookup"><span data-stu-id="f424c-118">Summary Income Statement - Default</span></span> | <span data-ttu-id="f424c-119">Kausittainen ja vuoden alusta - oletusarvo</span><span class="sxs-lookup"><span data-stu-id="f424c-119">Periodic and YTD - Default</span></span> |

### <a name="row-definition"></a><span data-ttu-id="f424c-120">Rivimääritys</span><span class="sxs-lookup"><span data-stu-id="f424c-120">Row definition</span></span>

<span data-ttu-id="f424c-121">Rivimääritys, yhteenvetotuloslaskelma – oletusarvo, sisältää osan perinteisen tuloslaskelman jokaiselle osalle.</span><span class="sxs-lookup"><span data-stu-id="f424c-121">The row definition, Summary Income Statement – Default, contains a section for each part of a traditional income statement.</span></span> <span data-ttu-id="f424c-122">Päätilin luokan dimensiota käytetään tämän rivimäärityksen muodostamisessa.</span><span class="sxs-lookup"><span data-stu-id="f424c-122">The Main Account Category dimension is used to build this row definition.</span></span> <span data-ttu-id="f424c-123">Tämän vuoksi kuka tahansa voi luoda raportin ilman muutosten tekemistä.</span><span class="sxs-lookup"><span data-stu-id="f424c-123">Therefore, anyone can generate the report without having to make any modifications.</span></span>

### <a name="column-definition"></a><span data-ttu-id="f424c-124">Sarakemääritys</span><span class="sxs-lookup"><span data-stu-id="f424c-124">Column Definition</span></span>

<span data-ttu-id="f424c-125">Sarakemääritykset sisältävät erityppisiä sarakkeita, joissa on useita yksityiskohtaisia tasoja ja taloushallinnon tietoja.</span><span class="sxs-lookup"><span data-stu-id="f424c-125">The column definitions contain different types of columns to provide different levels of detail and financial data.</span></span>

-   <span data-ttu-id="f424c-126">**Kausittainen ja vuoden alusta – oletussaraketyypit:**</span><span class="sxs-lookup"><span data-stu-id="f424c-126">**Periodic and YTD – Default column types:**</span></span>
    -   <span data-ttu-id="f424c-127">**DESC** – rivimäärityksen kuvaus</span><span class="sxs-lookup"><span data-stu-id="f424c-127">**DESC** – The description from the row definition</span></span>
    -   <span data-ttu-id="f424c-128">**FD** – nykyisen kauden taloushallinnon tiedot</span><span class="sxs-lookup"><span data-stu-id="f424c-128">**FD** – Financial data for the current period</span></span>
    -   <span data-ttu-id="f424c-129">**FD** – taloushallinnon tiedot vuoden alusta</span><span class="sxs-lookup"><span data-stu-id="f424c-129">**FD** – Financial data for the year to date</span></span>



<a name="additional-resources"></a><span data-ttu-id="f424c-130">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="f424c-130">Additional resources</span></span>
--------

[<span data-ttu-id="f424c-131">Taloushallinnon raportoinnin yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="f424c-131">Financial reporting overview</span></span>](financial-reporting-getting-started.md)

[<span data-ttu-id="f424c-132">Raporttien tarkasteleminen</span><span class="sxs-lookup"><span data-stu-id="f424c-132">View financial reports</span></span>](view-financial-reports.md)

[<span data-ttu-id="f424c-133">Dynamicsin talousraportointi -blogi</span><span class="sxs-lookup"><span data-stu-id="f424c-133">Dynamics Financial Reporting Blog</span></span>](https://community.dynamics.com/365/financeandoperations/b/dynamics-365-finance-blog)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]