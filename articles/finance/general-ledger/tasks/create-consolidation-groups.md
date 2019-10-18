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
ms.openlocfilehash: daa950877fd30174b46087303ae7275fb7dca337
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/27/2019
ms.locfileid: "2186207"
---
# <a name="create-consolidation-groups-and-additional-consolidation-accounts"></a><span data-ttu-id="2d7d6-103">Luo konsolidaatioryhmät ja lisäkonsolidaatiotilit</span><span class="sxs-lookup"><span data-stu-id="2d7d6-103">Create consolidation groups and additional consolidation accounts</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="2d7d6-104">Tässä menettelyssä käsitellään konsolidointitiliryhmän luontia ja tilien lisäämistä ryhmään.</span><span class="sxs-lookup"><span data-stu-id="2d7d6-104">This procedure shows how to create a consolidation account group and then add accounts to the group.</span></span> <span data-ttu-id="2d7d6-105">Menettely käyttää USMF-demotietoyritystä.</span><span class="sxs-lookup"><span data-stu-id="2d7d6-105">This procedure uses the demo data company USMF.</span></span>


## <a name="create-a-consolidation-account-group"></a><span data-ttu-id="2d7d6-106">Konsolidointitiliryhmän luominen</span><span class="sxs-lookup"><span data-stu-id="2d7d6-106">Create a consolidation account group</span></span>
1. <span data-ttu-id="2d7d6-107">Valitse Kirjanpito > Tilikartta > Tilit > Konsolidointitiliryhmät.</span><span class="sxs-lookup"><span data-stu-id="2d7d6-107">Go to General ledger > Chart of accounts > Accounts > Consolidation account groups.</span></span>
2. <span data-ttu-id="2d7d6-108">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="2d7d6-108">Click New.</span></span>
3. <span data-ttu-id="2d7d6-109">Anna Konsolidointitiliryhmä-kentässä konsolidointitiliryhmän yksilöllinen tunnus.</span><span class="sxs-lookup"><span data-stu-id="2d7d6-109">In the Consolidation account group field, enter a unique identifier for the consolidation account group.</span></span>
4. <span data-ttu-id="2d7d6-110">Kirjoita arvo Nimi-kenttään.</span><span class="sxs-lookup"><span data-stu-id="2d7d6-110">In the Name field, type a value.</span></span>

## <a name="add-accounts-to-consolidation-account-group"></a><span data-ttu-id="2d7d6-111">Lisää tilejä konsolidointitiliryhmään</span><span class="sxs-lookup"><span data-stu-id="2d7d6-111">Add accounts to consolidation account group</span></span>
1. <span data-ttu-id="2d7d6-112">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="2d7d6-112">Close the page.</span></span>
2. <span data-ttu-id="2d7d6-113">Valitse Kirjanpito > Tilikartta > Tilit > Lisäkonsolidointitilit.</span><span class="sxs-lookup"><span data-stu-id="2d7d6-113">Go to General ledger > Chart of accounts > Accounts > Additional consolidation accounts.</span></span>
3. <span data-ttu-id="2d7d6-114">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="2d7d6-114">Click New.</span></span>
4. <span data-ttu-id="2d7d6-115">Avaa haku napsauttamalla Päätili-kentässä avattavan valikon painiketta.</span><span class="sxs-lookup"><span data-stu-id="2d7d6-115">In the Main account field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="2d7d6-116">Valitse luettelosta yhdistettävä päätili.</span><span class="sxs-lookup"><span data-stu-id="2d7d6-116">In the list, click the main account that you want to map.</span></span>
6. <span data-ttu-id="2d7d6-117">Avaa haku napsauttamalla Konsolidointitiliryhmä-kentässä avattavan valikon painiketta.</span><span class="sxs-lookup"><span data-stu-id="2d7d6-117">In the Consolidation account group field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="2d7d6-118">Valitse luettelossa konsolidointitiliryhmä.</span><span class="sxs-lookup"><span data-stu-id="2d7d6-118">In the list, click the consolidation account group.</span></span>
8. <span data-ttu-id="2d7d6-119">Kirjoita Konsolidointitili-kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="2d7d6-119">In the Consolidation account field, type a value.</span></span>
9. <span data-ttu-id="2d7d6-120">Kirjoita Konsolidointitilin nimi -kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="2d7d6-120">In the Consolidation account name field, type a value.</span></span>

