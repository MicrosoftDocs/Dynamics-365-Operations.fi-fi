---
title: Käyttäjien tuominen joukkotoimintona
description: Näiden ohjeiden avulla järjestelmänvalvoja voi tuoda suuren määrän käyttäjiä Azure Active Directorysta.
author: maertenm
manager: AnnBe
ms.date: 07/07/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: sericks
ms.search.scope: Operations
ms.search.region: Global
ms.author: maertenm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 339cc1d3bcdc1dc93b796c385d2165f45f8f7ecf
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/29/2019
ms.locfileid: "338725"
---
# <a name="import-users-in-bulk"></a><span data-ttu-id="b1689-103">Käyttäjien joukkotuonti</span><span class="sxs-lookup"><span data-stu-id="b1689-103">Import users in bulk</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="b1689-104">Näiden ohjeiden avulla järjestelmänvalvoja voi tuoda suuren määrän käyttäjiä Azure Active Directorysta.</span><span class="sxs-lookup"><span data-stu-id="b1689-104">This procedure can be used by system administrators to import a large number of users from Azure Active Directory.</span></span>


## <a name="run-as-a-batch-job"></a><span data-ttu-id="b1689-105">Suorita työ komentojonotyönä</span><span class="sxs-lookup"><span data-stu-id="b1689-105">Run as a batch job</span></span>
1. <span data-ttu-id="b1689-106">Valitse Järjestelmänhallinta > Käyttäjät > Käyttäjät.</span><span class="sxs-lookup"><span data-stu-id="b1689-106">Go to System administration > Users > Users.</span></span>
2. <span data-ttu-id="b1689-107">Valitse Erän tuonti.</span><span class="sxs-lookup"><span data-stu-id="b1689-107">Click Batch import.</span></span>
3. <span data-ttu-id="b1689-108">Laajenna Suorita taustalla -osa.</span><span class="sxs-lookup"><span data-stu-id="b1689-108">Expand the Run in the background section.</span></span>
4. <span data-ttu-id="b1689-109">Valitse Eräkäsittely-kentässä Kyllä.</span><span class="sxs-lookup"><span data-stu-id="b1689-109">Select Yes in the Batch processing field.</span></span>
5. <span data-ttu-id="b1689-110">Kirjoita arvo Tehtävän kuvaus -kenttään.</span><span class="sxs-lookup"><span data-stu-id="b1689-110">In the Task description field, type a value.</span></span>
6. <span data-ttu-id="b1689-111">Anna tai valitse arvo Eräryhmä-kentässä.</span><span class="sxs-lookup"><span data-stu-id="b1689-111">In the Batch group field, enter or select a value.</span></span>
    * <span data-ttu-id="b1689-112">Tämä on valinnainen vaihe.</span><span class="sxs-lookup"><span data-stu-id="b1689-112">This is an optional step.</span></span>  
7. <span data-ttu-id="b1689-113">Valitse Yksityinen-kentässä Kyllä.</span><span class="sxs-lookup"><span data-stu-id="b1689-113">Select Yes in the Private field.</span></span>
    * <span data-ttu-id="b1689-114">Tämä on valinnainen vaihe.</span><span class="sxs-lookup"><span data-stu-id="b1689-114">This is an optional step.</span></span>  
8. <span data-ttu-id="b1689-115">Valitse Kriittinen työ -kentässä Kyllä.</span><span class="sxs-lookup"><span data-stu-id="b1689-115">Select Yes in the Critical Job field.</span></span>
    * <span data-ttu-id="b1689-116">Tämä on valinnainen vaihe.</span><span class="sxs-lookup"><span data-stu-id="b1689-116">This is an optional step.</span></span>  
9. <span data-ttu-id="b1689-117">Valitse vaihtoehto Luokan valvonta -kentässä.</span><span class="sxs-lookup"><span data-stu-id="b1689-117">In the Monitoring category field, select an option.</span></span>
10. <span data-ttu-id="b1689-118">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="b1689-118">Click OK.</span></span>

## <a name="run-in-a-sandbox-environment"></a><span data-ttu-id="b1689-119">Eristysympäristön suorittaminen</span><span class="sxs-lookup"><span data-stu-id="b1689-119">Run in a sandbox environment</span></span>
1. <span data-ttu-id="b1689-120">Valitse Erän tuonti.</span><span class="sxs-lookup"><span data-stu-id="b1689-120">Click Batch import.</span></span>
2. <span data-ttu-id="b1689-121">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="b1689-121">Click OK.</span></span>

