---
title: Kustannuslaskennan kirjanpidon tietolähteen hallinta
description: Tämän menettelyn avulla hallitaan kirjanpidon tietolähdettä kustannuslaskennan kirjanpidossa.
author: ShylaThompson
ms.date: 06/27/2017
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: CAMAXGeneralLedgerEntryProviderConfiguration
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: da4d351f4bce6494a107a55895866e4d3d43953f
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/01/2021
ms.locfileid: "5841066"
---
# <a name="manage-a-data-source-for-the-cost-accounting-ledger"></a><span data-ttu-id="56be3-103">Kustannuslaskennan kirjanpidon tietolähteen hallinta</span><span class="sxs-lookup"><span data-stu-id="56be3-103">Manage a data source for the cost accounting ledger</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="56be3-104">Tämän menettelyn avulla hallitaan kirjanpidon tietolähdettä kustannuslaskennan kirjanpidossa.</span><span class="sxs-lookup"><span data-stu-id="56be3-104">Use this procedure to manage the general ledger data source for a cost accounting ledger.</span></span> <span data-ttu-id="56be3-105">Ennen tämän tehtävän suorittamista tulee toistaa Kustannuslaskennan kirjanpidon luominen- ja Kustannusseurantayksiköiden määrittäminen -tehtäväoppaat.</span><span class="sxs-lookup"><span data-stu-id="56be3-105">Before you complete this task, make sure that you play the "Create a cost accounting ledger" and "Define cost control units" task guides.</span></span> <span data-ttu-id="56be3-106">Tämä tallenne käyttää esittelytietojen USP2-yritystä.</span><span class="sxs-lookup"><span data-stu-id="56be3-106">This recording uses the USP2 demo data company.</span></span>

1. <span data-ttu-id="56be3-107">Valitse Kustannuslaskenta > Kirjanpidon asetukset > Kustannuslaskennan kirjanpidot.</span><span class="sxs-lookup"><span data-stu-id="56be3-107">Go to Cost accounting > Ledger setup > Cost accounting ledgers.</span></span>
2. <span data-ttu-id="56be3-108">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="56be3-108">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="56be3-109">Valitse Toteutuneet versiot.</span><span class="sxs-lookup"><span data-stu-id="56be3-109">Click Actual versions.</span></span>
4. <span data-ttu-id="56be3-110">Valitse toimintoruudussa Hallitse.</span><span class="sxs-lookup"><span data-stu-id="56be3-110">On the Action Pane, click Manage.</span></span>
5. <span data-ttu-id="56be3-111">Valitse Kirjanpito.</span><span class="sxs-lookup"><span data-stu-id="56be3-111">Click General ledger.</span></span>
6. <span data-ttu-id="56be3-112">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="56be3-112">Click New.</span></span>
7. <span data-ttu-id="56be3-113">Kirjoita arvo Nimi-kenttään.</span><span class="sxs-lookup"><span data-stu-id="56be3-113">In the Name field, type a value.</span></span>
8. <span data-ttu-id="56be3-114">Anna tai valitse arvo Tietopalvelu-kenttään.</span><span class="sxs-lookup"><span data-stu-id="56be3-114">In the Data provider field, enter or select a value.</span></span>
    * <span data-ttu-id="56be3-115">Valitse tässä esimerkissä Dynamics 365 Finance -Kirjanpitomerkinnät.</span><span class="sxs-lookup"><span data-stu-id="56be3-115">For this example, select Dynamics 365 Finance - General ledger entries.</span></span>  
9. <span data-ttu-id="56be3-116">Syötä tai valitse arvo Kustannustason dimensio -kenttään.</span><span class="sxs-lookup"><span data-stu-id="56be3-116">In the Cost element dimension field, enter or select a value.</span></span>
    * <span data-ttu-id="56be3-117">Valitse tässä esimerkissä Kustannustasot.</span><span class="sxs-lookup"><span data-stu-id="56be3-117">For this example, select Cost elements.</span></span>  
10. <span data-ttu-id="56be3-118">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="56be3-118">Click Save.</span></span>
11. <span data-ttu-id="56be3-119">Valitse Määritä tietopalvelu.</span><span class="sxs-lookup"><span data-stu-id="56be3-119">Click Configure data provider.</span></span>
12. <span data-ttu-id="56be3-120">Anna tai valitse arvo Yritys-kenttään.</span><span class="sxs-lookup"><span data-stu-id="56be3-120">In the Legal entity field, enter or select a value.</span></span>
    * <span data-ttu-id="56be3-121">Valitse tässä esimerkissä USP2.</span><span class="sxs-lookup"><span data-stu-id="56be3-121">For this example, select USP2.</span></span>  
13. <span data-ttu-id="56be3-122">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="56be3-122">Click New.</span></span>
14. <span data-ttu-id="56be3-123">Valitse Kirjanpitotaso-kentässä Nykyinen.</span><span class="sxs-lookup"><span data-stu-id="56be3-123">In the Posting layer field, select Current.</span></span>
15. <span data-ttu-id="56be3-124">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="56be3-124">Click OK.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]