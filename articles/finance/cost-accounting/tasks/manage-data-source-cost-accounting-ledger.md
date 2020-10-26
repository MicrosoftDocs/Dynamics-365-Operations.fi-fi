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
ms.search.form: CAMAXGeneralLedgerEntryProviderConfiguration
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Operations
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 88f5170610ea9b5634c4bf5da7079cacccdafe04
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/10/2020
ms.locfileid: "3977572"
---
# <a name="manage-a-data-source-for-the-cost-accounting-ledger"></a><span data-ttu-id="45101-103">Kustannuslaskennan kirjanpidon tietolähteen hallinta</span><span class="sxs-lookup"><span data-stu-id="45101-103">Manage a data source for the cost accounting ledger</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="45101-104">Tämän menettelyn avulla hallitaan kirjanpidon tietolähdettä kustannuslaskennan kirjanpidossa.</span><span class="sxs-lookup"><span data-stu-id="45101-104">Use this procedure to manage the general ledger data source for a cost accounting ledger.</span></span> <span data-ttu-id="45101-105">Ennen tämän tehtävän suorittamista tulee toistaa Kustannuslaskennan kirjanpidon luominen- ja Kustannusseurantayksiköiden määrittäminen -tehtäväoppaat.</span><span class="sxs-lookup"><span data-stu-id="45101-105">Before you complete this task, make sure that you play the "Create a cost accounting ledger" and "Define cost control units" task guides.</span></span> <span data-ttu-id="45101-106">Tämä tallenne käyttää esittelytietojen USP2-yritystä.</span><span class="sxs-lookup"><span data-stu-id="45101-106">This recording uses the USP2 demo data company.</span></span>

1. <span data-ttu-id="45101-107">Valitse Kustannuslaskenta > Kirjanpidon asetukset > Kustannuslaskennan kirjanpidot.</span><span class="sxs-lookup"><span data-stu-id="45101-107">Go to Cost accounting > Ledger setup > Cost accounting ledgers.</span></span>
2. <span data-ttu-id="45101-108">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="45101-108">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="45101-109">Valitse Toteutuneet versiot.</span><span class="sxs-lookup"><span data-stu-id="45101-109">Click Actual versions.</span></span>
4. <span data-ttu-id="45101-110">Valitse toimintoruudussa Hallitse.</span><span class="sxs-lookup"><span data-stu-id="45101-110">On the Action Pane, click Manage.</span></span>
5. <span data-ttu-id="45101-111">Valitse Kirjanpito.</span><span class="sxs-lookup"><span data-stu-id="45101-111">Click General ledger.</span></span>
6. <span data-ttu-id="45101-112">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="45101-112">Click New.</span></span>
7. <span data-ttu-id="45101-113">Kirjoita arvo Nimi-kenttään.</span><span class="sxs-lookup"><span data-stu-id="45101-113">In the Name field, type a value.</span></span>
8. <span data-ttu-id="45101-114">Anna tai valitse arvo Tietopalvelu-kenttään.</span><span class="sxs-lookup"><span data-stu-id="45101-114">In the Data provider field, enter or select a value.</span></span>
    * <span data-ttu-id="45101-115">Valitse tässä esimerkissä Dynamics 365 Finance -Kirjanpitomerkinnät.</span><span class="sxs-lookup"><span data-stu-id="45101-115">For this example, select Dynamics 365 Finance - General ledger entries.</span></span>  
9. <span data-ttu-id="45101-116">Syötä tai valitse arvo Kustannustason dimensio -kenttään.</span><span class="sxs-lookup"><span data-stu-id="45101-116">In the Cost element dimension field, enter or select a value.</span></span>
    * <span data-ttu-id="45101-117">Valitse tässä esimerkissä Kustannustasot.</span><span class="sxs-lookup"><span data-stu-id="45101-117">For this example, select Cost elements.</span></span>  
10. <span data-ttu-id="45101-118">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="45101-118">Click Save.</span></span>
11. <span data-ttu-id="45101-119">Valitse Määritä tietopalvelu.</span><span class="sxs-lookup"><span data-stu-id="45101-119">Click Configure data provider.</span></span>
12. <span data-ttu-id="45101-120">Anna tai valitse arvo Yritys-kenttään.</span><span class="sxs-lookup"><span data-stu-id="45101-120">In the Legal entity field, enter or select a value.</span></span>
    * <span data-ttu-id="45101-121">Valitse tässä esimerkissä USP2.</span><span class="sxs-lookup"><span data-stu-id="45101-121">For this example, select USP2.</span></span>  
13. <span data-ttu-id="45101-122">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="45101-122">Click New.</span></span>
14. <span data-ttu-id="45101-123">Valitse Kirjanpitotaso-kentässä Nykyinen.</span><span class="sxs-lookup"><span data-stu-id="45101-123">In the Posting layer field, select Current.</span></span>
15. <span data-ttu-id="45101-124">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="45101-124">Click OK.</span></span>

