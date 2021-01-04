---
title: Luo konsolidaatioryhmät ja lisäkonsolidaatiotilit
description: Tässä menettelyssä käsitellään konsolidointitiliryhmän luontia ja tilien lisäämistä ryhmään.
author: aprilolson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerConsolidateAccountGroup, MainAccountConsolidateAccount
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 826a65af563207fbfbc7391b176aa0e65b3363f9
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/13/2020
ms.locfileid: "4442844"
---
# <a name="create-consolidation-groups-and-additional-consolidation-accounts"></a><span data-ttu-id="b30ee-103">Luo konsolidaatioryhmät ja lisäkonsolidaatiotilit</span><span class="sxs-lookup"><span data-stu-id="b30ee-103">Create consolidation groups and additional consolidation accounts</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="b30ee-104">Tässä menettelyssä käsitellään konsolidointitiliryhmän luontia ja tilien lisäämistä ryhmään.</span><span class="sxs-lookup"><span data-stu-id="b30ee-104">This procedure shows how to create a consolidation account group and then add accounts to the group.</span></span> <span data-ttu-id="b30ee-105">Menettely käyttää USMF-demotietoyritystä.</span><span class="sxs-lookup"><span data-stu-id="b30ee-105">This procedure uses the demo data company USMF.</span></span>


## <a name="create-a-consolidation-account-group"></a><span data-ttu-id="b30ee-106">Konsolidointitiliryhmän luominen</span><span class="sxs-lookup"><span data-stu-id="b30ee-106">Create a consolidation account group</span></span>
1. <span data-ttu-id="b30ee-107">Valitse Kirjanpito > Tilikartta > Tilit > Konsolidointitiliryhmät.</span><span class="sxs-lookup"><span data-stu-id="b30ee-107">Go to General ledger > Chart of accounts > Accounts > Consolidation account groups.</span></span>
2. <span data-ttu-id="b30ee-108">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="b30ee-108">Click New.</span></span>
3. <span data-ttu-id="b30ee-109">Anna Konsolidointitiliryhmä-kentässä konsolidointitiliryhmän yksilöllinen tunnus.</span><span class="sxs-lookup"><span data-stu-id="b30ee-109">In the Consolidation account group field, enter a unique identifier for the consolidation account group.</span></span>
4. <span data-ttu-id="b30ee-110">Kirjoita arvo Nimi-kenttään.</span><span class="sxs-lookup"><span data-stu-id="b30ee-110">In the Name field, type a value.</span></span>

## <a name="add-accounts-to-consolidation-account-group"></a><span data-ttu-id="b30ee-111">Lisää tilejä konsolidointitiliryhmään</span><span class="sxs-lookup"><span data-stu-id="b30ee-111">Add accounts to consolidation account group</span></span>
1. <span data-ttu-id="b30ee-112">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="b30ee-112">Close the page.</span></span>
2. <span data-ttu-id="b30ee-113">Valitse Kirjanpito > Tilikartta > Tilit > Lisäkonsolidointitilit.</span><span class="sxs-lookup"><span data-stu-id="b30ee-113">Go to General ledger > Chart of accounts > Accounts > Additional consolidation accounts.</span></span>
3. <span data-ttu-id="b30ee-114">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="b30ee-114">Click New.</span></span>
4. <span data-ttu-id="b30ee-115">Avaa haku napsauttamalla Päätili-kentässä avattavan valikon painiketta.</span><span class="sxs-lookup"><span data-stu-id="b30ee-115">In the Main account field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="b30ee-116">Valitse luettelosta yhdistettävä päätili.</span><span class="sxs-lookup"><span data-stu-id="b30ee-116">In the list, click the main account that you want to map.</span></span>
6. <span data-ttu-id="b30ee-117">Avaa haku napsauttamalla Konsolidointitiliryhmä-kentässä avattavan valikon painiketta.</span><span class="sxs-lookup"><span data-stu-id="b30ee-117">In the Consolidation account group field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="b30ee-118">Valitse luettelossa konsolidointitiliryhmä.</span><span class="sxs-lookup"><span data-stu-id="b30ee-118">In the list, click the consolidation account group.</span></span>
8. <span data-ttu-id="b30ee-119">Kirjoita Konsolidointitili-kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="b30ee-119">In the Consolidation account field, type a value.</span></span>
9. <span data-ttu-id="b30ee-120">Kirjoita Konsolidointitilin nimi -kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="b30ee-120">In the Consolidation account name field, type a value.</span></span>

