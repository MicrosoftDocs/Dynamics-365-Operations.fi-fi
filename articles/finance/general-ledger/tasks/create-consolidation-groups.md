---
title: Luo konsolidaatioryhmät ja lisäkonsolidaatiotilit
description: Tässä menettelyssä käsitellään konsolidointitiliryhmän luontia ja tilien lisäämistä ryhmään.
author: aprilolson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerConsolidateAccountGroup, MainAccountConsolidateAccount
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 6c60b09fd0481c84a9c3a3eb35b66264d92d00eb
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/01/2021
ms.locfileid: "5832775"
---
# <a name="create-consolidation-groups-and-additional-consolidation-accounts"></a><span data-ttu-id="62f17-103">Luo konsolidaatioryhmät ja lisäkonsolidaatiotilit</span><span class="sxs-lookup"><span data-stu-id="62f17-103">Create consolidation groups and additional consolidation accounts</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="62f17-104">Tässä menettelyssä käsitellään konsolidointitiliryhmän luontia ja tilien lisäämistä ryhmään.</span><span class="sxs-lookup"><span data-stu-id="62f17-104">This procedure shows how to create a consolidation account group and then add accounts to the group.</span></span> <span data-ttu-id="62f17-105">Menettely käyttää USMF-demotietoyritystä.</span><span class="sxs-lookup"><span data-stu-id="62f17-105">This procedure uses the demo data company USMF.</span></span>


## <a name="create-a-consolidation-account-group"></a><span data-ttu-id="62f17-106">Konsolidointitiliryhmän luominen</span><span class="sxs-lookup"><span data-stu-id="62f17-106">Create a consolidation account group</span></span>
1. <span data-ttu-id="62f17-107">Valitse Kirjanpito > Tilikartta > Tilit > Konsolidointitiliryhmät.</span><span class="sxs-lookup"><span data-stu-id="62f17-107">Go to General ledger > Chart of accounts > Accounts > Consolidation account groups.</span></span>
2. <span data-ttu-id="62f17-108">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="62f17-108">Click New.</span></span>
3. <span data-ttu-id="62f17-109">Anna Konsolidointitiliryhmä-kentässä konsolidointitiliryhmän yksilöllinen tunnus.</span><span class="sxs-lookup"><span data-stu-id="62f17-109">In the Consolidation account group field, enter a unique identifier for the consolidation account group.</span></span>
4. <span data-ttu-id="62f17-110">Kirjoita arvo Nimi-kenttään.</span><span class="sxs-lookup"><span data-stu-id="62f17-110">In the Name field, type a value.</span></span>

## <a name="add-accounts-to-consolidation-account-group"></a><span data-ttu-id="62f17-111">Lisää tilejä konsolidointitiliryhmään</span><span class="sxs-lookup"><span data-stu-id="62f17-111">Add accounts to consolidation account group</span></span>
1. <span data-ttu-id="62f17-112">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="62f17-112">Close the page.</span></span>
2. <span data-ttu-id="62f17-113">Valitse Kirjanpito > Tilikartta > Tilit > Lisäkonsolidointitilit.</span><span class="sxs-lookup"><span data-stu-id="62f17-113">Go to General ledger > Chart of accounts > Accounts > Additional consolidation accounts.</span></span>
3. <span data-ttu-id="62f17-114">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="62f17-114">Click New.</span></span>
4. <span data-ttu-id="62f17-115">Avaa haku napsauttamalla Päätili-kentässä avattavan valikon painiketta.</span><span class="sxs-lookup"><span data-stu-id="62f17-115">In the Main account field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="62f17-116">Valitse luettelosta yhdistettävä päätili.</span><span class="sxs-lookup"><span data-stu-id="62f17-116">In the list, click the main account that you want to map.</span></span>
6. <span data-ttu-id="62f17-117">Avaa haku napsauttamalla Konsolidointitiliryhmä-kentässä avattavan valikon painiketta.</span><span class="sxs-lookup"><span data-stu-id="62f17-117">In the Consolidation account group field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="62f17-118">Valitse luettelossa konsolidointitiliryhmä.</span><span class="sxs-lookup"><span data-stu-id="62f17-118">In the list, click the consolidation account group.</span></span>
8. <span data-ttu-id="62f17-119">Kirjoita Konsolidointitili-kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="62f17-119">In the Consolidation account field, type a value.</span></span>
9. <span data-ttu-id="62f17-120">Kirjoita Konsolidointitilin nimi -kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="62f17-120">In the Consolidation account name field, type a value.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]