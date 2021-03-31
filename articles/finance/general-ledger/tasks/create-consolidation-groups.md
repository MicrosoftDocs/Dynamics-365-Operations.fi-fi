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
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a02d6cf5516e63378f4aa356627c069404546e07
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5216512"
---
# <a name="create-consolidation-groups-and-additional-consolidation-accounts"></a><span data-ttu-id="17232-103">Luo konsolidaatioryhmät ja lisäkonsolidaatiotilit</span><span class="sxs-lookup"><span data-stu-id="17232-103">Create consolidation groups and additional consolidation accounts</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="17232-104">Tässä menettelyssä käsitellään konsolidointitiliryhmän luontia ja tilien lisäämistä ryhmään.</span><span class="sxs-lookup"><span data-stu-id="17232-104">This procedure shows how to create a consolidation account group and then add accounts to the group.</span></span> <span data-ttu-id="17232-105">Menettely käyttää USMF-demotietoyritystä.</span><span class="sxs-lookup"><span data-stu-id="17232-105">This procedure uses the demo data company USMF.</span></span>


## <a name="create-a-consolidation-account-group"></a><span data-ttu-id="17232-106">Konsolidointitiliryhmän luominen</span><span class="sxs-lookup"><span data-stu-id="17232-106">Create a consolidation account group</span></span>
1. <span data-ttu-id="17232-107">Valitse Kirjanpito > Tilikartta > Tilit > Konsolidointitiliryhmät.</span><span class="sxs-lookup"><span data-stu-id="17232-107">Go to General ledger > Chart of accounts > Accounts > Consolidation account groups.</span></span>
2. <span data-ttu-id="17232-108">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="17232-108">Click New.</span></span>
3. <span data-ttu-id="17232-109">Anna Konsolidointitiliryhmä-kentässä konsolidointitiliryhmän yksilöllinen tunnus.</span><span class="sxs-lookup"><span data-stu-id="17232-109">In the Consolidation account group field, enter a unique identifier for the consolidation account group.</span></span>
4. <span data-ttu-id="17232-110">Kirjoita arvo Nimi-kenttään.</span><span class="sxs-lookup"><span data-stu-id="17232-110">In the Name field, type a value.</span></span>

## <a name="add-accounts-to-consolidation-account-group"></a><span data-ttu-id="17232-111">Lisää tilejä konsolidointitiliryhmään</span><span class="sxs-lookup"><span data-stu-id="17232-111">Add accounts to consolidation account group</span></span>
1. <span data-ttu-id="17232-112">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="17232-112">Close the page.</span></span>
2. <span data-ttu-id="17232-113">Valitse Kirjanpito > Tilikartta > Tilit > Lisäkonsolidointitilit.</span><span class="sxs-lookup"><span data-stu-id="17232-113">Go to General ledger > Chart of accounts > Accounts > Additional consolidation accounts.</span></span>
3. <span data-ttu-id="17232-114">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="17232-114">Click New.</span></span>
4. <span data-ttu-id="17232-115">Avaa haku napsauttamalla Päätili-kentässä avattavan valikon painiketta.</span><span class="sxs-lookup"><span data-stu-id="17232-115">In the Main account field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="17232-116">Valitse luettelosta yhdistettävä päätili.</span><span class="sxs-lookup"><span data-stu-id="17232-116">In the list, click the main account that you want to map.</span></span>
6. <span data-ttu-id="17232-117">Avaa haku napsauttamalla Konsolidointitiliryhmä-kentässä avattavan valikon painiketta.</span><span class="sxs-lookup"><span data-stu-id="17232-117">In the Consolidation account group field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="17232-118">Valitse luettelossa konsolidointitiliryhmä.</span><span class="sxs-lookup"><span data-stu-id="17232-118">In the list, click the consolidation account group.</span></span>
8. <span data-ttu-id="17232-119">Kirjoita Konsolidointitili-kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="17232-119">In the Consolidation account field, type a value.</span></span>
9. <span data-ttu-id="17232-120">Kirjoita Konsolidointitilin nimi -kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="17232-120">In the Consolidation account name field, type a value.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]