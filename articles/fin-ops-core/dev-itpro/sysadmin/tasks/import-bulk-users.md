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
ms.openlocfilehash: cb2c316465f8c6964a562e92ce0a2233b37d38fe
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/27/2019
ms.locfileid: "2180895"
---
# <a name="import-users-in-bulk"></a><span data-ttu-id="9273e-103">Käyttäjien joukkotuonti</span><span class="sxs-lookup"><span data-stu-id="9273e-103">Import users in bulk</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="9273e-104">Näiden ohjeiden avulla järjestelmänvalvoja voi tuoda suuren määrän käyttäjiä Azure Active Directorysta.</span><span class="sxs-lookup"><span data-stu-id="9273e-104">This procedure can be used by system administrators to import a large number of users from Azure Active Directory.</span></span>


## <a name="run-as-a-batch-job"></a><span data-ttu-id="9273e-105">Suorita työ komentojonotyönä</span><span class="sxs-lookup"><span data-stu-id="9273e-105">Run as a batch job</span></span>
1. <span data-ttu-id="9273e-106">Valitse Järjestelmänhallinta > Käyttäjät > Käyttäjät.</span><span class="sxs-lookup"><span data-stu-id="9273e-106">Go to System administration > Users > Users.</span></span>
2. <span data-ttu-id="9273e-107">Valitse Erän tuonti.</span><span class="sxs-lookup"><span data-stu-id="9273e-107">Click Batch import.</span></span>
3. <span data-ttu-id="9273e-108">Laajenna Suorita taustalla -osa.</span><span class="sxs-lookup"><span data-stu-id="9273e-108">Expand the Run in the background section.</span></span>
4. <span data-ttu-id="9273e-109">Valitse Eräkäsittely-kentässä Kyllä.</span><span class="sxs-lookup"><span data-stu-id="9273e-109">Select Yes in the Batch processing field.</span></span>
5. <span data-ttu-id="9273e-110">Kirjoita arvo Tehtävän kuvaus -kenttään.</span><span class="sxs-lookup"><span data-stu-id="9273e-110">In the Task description field, type a value.</span></span>
6. <span data-ttu-id="9273e-111">Anna tai valitse arvo Eräryhmä-kentässä.</span><span class="sxs-lookup"><span data-stu-id="9273e-111">In the Batch group field, enter or select a value.</span></span>
    * <span data-ttu-id="9273e-112">Tämä on valinnainen vaihe.</span><span class="sxs-lookup"><span data-stu-id="9273e-112">This is an optional step.</span></span>  
7. <span data-ttu-id="9273e-113">Valitse Yksityinen-kentässä Kyllä.</span><span class="sxs-lookup"><span data-stu-id="9273e-113">Select Yes in the Private field.</span></span>
    * <span data-ttu-id="9273e-114">Tämä on valinnainen vaihe.</span><span class="sxs-lookup"><span data-stu-id="9273e-114">This is an optional step.</span></span>  
8. <span data-ttu-id="9273e-115">Valitse Kriittinen työ -kentässä Kyllä.</span><span class="sxs-lookup"><span data-stu-id="9273e-115">Select Yes in the Critical Job field.</span></span>
    * <span data-ttu-id="9273e-116">Tämä on valinnainen vaihe.</span><span class="sxs-lookup"><span data-stu-id="9273e-116">This is an optional step.</span></span>  
9. <span data-ttu-id="9273e-117">Valitse vaihtoehto Luokan valvonta -kentässä.</span><span class="sxs-lookup"><span data-stu-id="9273e-117">In the Monitoring category field, select an option.</span></span>
10. <span data-ttu-id="9273e-118">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="9273e-118">Click OK.</span></span>

## <a name="run-in-a-sandbox-environment"></a><span data-ttu-id="9273e-119">Eristysympäristön suorittaminen</span><span class="sxs-lookup"><span data-stu-id="9273e-119">Run in a sandbox environment</span></span>
1. <span data-ttu-id="9273e-120">Valitse Erän tuonti.</span><span class="sxs-lookup"><span data-stu-id="9273e-120">Click Batch import.</span></span>
2. <span data-ttu-id="9273e-121">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="9273e-121">Click OK.</span></span>
