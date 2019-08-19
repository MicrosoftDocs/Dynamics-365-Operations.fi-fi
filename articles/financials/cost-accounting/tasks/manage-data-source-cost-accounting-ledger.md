---
title: Kustannuslaskennan kirjanpidon tietolähteen hallinta
description: Tämän menettelyn avulla hallitaan kirjanpidon tietolähdettä kustannuslaskennan kirjanpidossa.
author: ShylaThompson
manager: AnnBe
ms.date: 06/27/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3d9d688113c1e1cc13b3651ce416cbf3037ad35a
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/01/2019
ms.locfileid: "1841174"
---
# <a name="manage-a-data-source-for-the-cost-accounting-ledger"></a><span data-ttu-id="00891-103">Kustannuslaskennan kirjanpidon tietolähteen hallinta</span><span class="sxs-lookup"><span data-stu-id="00891-103">Manage a data source for the cost accounting ledger</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="00891-104">Tämän menettelyn avulla hallitaan kirjanpidon tietolähdettä kustannuslaskennan kirjanpidossa.</span><span class="sxs-lookup"><span data-stu-id="00891-104">Use this procedure to manage the general ledger data source for a cost accounting ledger.</span></span> <span data-ttu-id="00891-105">Ennen tämän tehtävän suorittamista tulee toistaa Kustannuslaskennan kirjanpidon luominen- ja Kustannusseurantayksiköiden määrittäminen -tehtäväoppaat.</span><span class="sxs-lookup"><span data-stu-id="00891-105">Before you complete this task, make sure that you play the "Create a cost accounting ledger" and "Define cost control units" task guides.</span></span> <span data-ttu-id="00891-106">Tämä tallenne käyttää esittelytietojen USP2-yritystä.</span><span class="sxs-lookup"><span data-stu-id="00891-106">This recording uses the USP2 demo data company.</span></span>

1. <span data-ttu-id="00891-107">Valitse Kustannuslaskenta > Kirjanpidon asetukset > Kustannuslaskennan kirjanpidot.</span><span class="sxs-lookup"><span data-stu-id="00891-107">Go to Cost accounting > Ledger setup > Cost accounting ledgers.</span></span>
2. <span data-ttu-id="00891-108">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="00891-108">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="00891-109">Valitse Toteutuneet versiot.</span><span class="sxs-lookup"><span data-stu-id="00891-109">Click Actual versions.</span></span>
4. <span data-ttu-id="00891-110">Valitse toimintoruudussa Hallitse.</span><span class="sxs-lookup"><span data-stu-id="00891-110">On the Action Pane, click Manage.</span></span>
5. <span data-ttu-id="00891-111">Valitse Kirjanpito.</span><span class="sxs-lookup"><span data-stu-id="00891-111">Click General ledger.</span></span>
6. <span data-ttu-id="00891-112">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="00891-112">Click New.</span></span>
7. <span data-ttu-id="00891-113">Kirjoita arvo Nimi-kenttään.</span><span class="sxs-lookup"><span data-stu-id="00891-113">In the Name field, type a value.</span></span>
8. <span data-ttu-id="00891-114">Anna tai valitse arvo Tietopalvelu-kenttään.</span><span class="sxs-lookup"><span data-stu-id="00891-114">In the Data provider field, enter or select a value.</span></span>
    * <span data-ttu-id="00891-115">Valitse tässä esimerkissä Dynamics 365 for Finance and Operations -Kirjanpitomerkinnät.</span><span class="sxs-lookup"><span data-stu-id="00891-115">For this example, select Dynamics 365 for Finance and Operations - General ledger entries.</span></span>  
9. <span data-ttu-id="00891-116">Syötä tai valitse arvo Kustannustason dimensio -kenttään.</span><span class="sxs-lookup"><span data-stu-id="00891-116">In the Cost element dimension field, enter or select a value.</span></span>
    * <span data-ttu-id="00891-117">Valitse tässä esimerkissä Kustannustasot.</span><span class="sxs-lookup"><span data-stu-id="00891-117">For this example, select Cost elements.</span></span>  
10. <span data-ttu-id="00891-118">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="00891-118">Click Save.</span></span>
11. <span data-ttu-id="00891-119">Valitse Määritä tietopalvelu.</span><span class="sxs-lookup"><span data-stu-id="00891-119">Click Configure data provider.</span></span>
12. <span data-ttu-id="00891-120">Anna tai valitse arvo Yritys-kenttään.</span><span class="sxs-lookup"><span data-stu-id="00891-120">In the Legal entity field, enter or select a value.</span></span>
    * <span data-ttu-id="00891-121">Valitse tässä esimerkissä USP2.</span><span class="sxs-lookup"><span data-stu-id="00891-121">For this example, select USP2.</span></span>  
13. <span data-ttu-id="00891-122">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="00891-122">Click New.</span></span>
14. <span data-ttu-id="00891-123">Valitse Kirjanpitotaso-kentässä Nykyinen.</span><span class="sxs-lookup"><span data-stu-id="00891-123">In the Posting layer field, select Current.</span></span>
15. <span data-ttu-id="00891-124">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="00891-124">Click OK.</span></span>

