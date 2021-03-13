---
title: Luo uusi kanban-sääntö kopioimalla olemassa oleva sääntö
description: Tässä menettelyssä käsitellään aiemmin luodun kanban-säännön kaksoiskappaleen luomista.
author: ChristianRytt
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanRules, KanbanRuleDuplicate, InventItemIdLookupSimple
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7a1fda7e00c64f18e8078805a98cba8cdb1c4309
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/15/2021
ms.locfileid: "5010994"
---
# <a name="create-a-new-kanban-rule-by-duplicating-an-existing-kanban-rule"></a><span data-ttu-id="342e0-103">Luo uusi kanban-sääntö kopioimalla olemassa oleva sääntö</span><span class="sxs-lookup"><span data-stu-id="342e0-103">Create a new kanban rule by duplicating an existing kanban rule</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="342e0-104">Tässä menettelyssä käsitellään aiemmin luodun kanban-säännön kaksoiskappaleen luomista.</span><span class="sxs-lookup"><span data-stu-id="342e0-104">This procedure focuses on creating a duplicate of an existing kanban rule.</span></span> <span data-ttu-id="342e0-105">Tämä on kätevää, jos haluat luoda aiemmin luotuihin kanban-sääntöihin perustuvia uusia kanban-sääntöjä.</span><span class="sxs-lookup"><span data-stu-id="342e0-105">This is useful if you want to create new kanban rules based on existing kanban rules.</span></span> <span data-ttu-id="342e0-106">Tämän menettelyn luomisessa käytetty esittely-yritys on USMF.</span><span class="sxs-lookup"><span data-stu-id="342e0-106">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="342e0-107">Menettely on tarkoitettu prosessiteknikolle tai arvovirtaa hallitsevalle työntekijälle muutetun tuotantovirran tai uuden täydennyssäännön tuotannon valmisteluun.</span><span class="sxs-lookup"><span data-stu-id="342e0-107">This procedure is intended for the process engineer or the value stream manager as they prepare production for a changed production flow or a new replenishment rule.</span></span>


## <a name="select-a-kanban-rule"></a><span data-ttu-id="342e0-108">Valitse kanban-sääntö</span><span class="sxs-lookup"><span data-stu-id="342e0-108">Select a kanban rule</span></span>
1. <span data-ttu-id="342e0-109">Valitse Kanban-säännöt.</span><span class="sxs-lookup"><span data-stu-id="342e0-109">Go to Kanban rules.</span></span>
2. <span data-ttu-id="342e0-110">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="342e0-110">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="342e0-111">Valitse tuotteelle M0006 kanban-sääntö 000017.</span><span class="sxs-lookup"><span data-stu-id="342e0-111">Select kanban rule 000017 for Product M0006.</span></span>  

## <a name="duplicate-a-kanban-rule"></a><span data-ttu-id="342e0-112">Kanban-säännön kaksoiskappale</span><span class="sxs-lookup"><span data-stu-id="342e0-112">Duplicate a kanban rule</span></span>
1. <span data-ttu-id="342e0-113">Valitse Kanban-säännön kaksoiskappale.</span><span class="sxs-lookup"><span data-stu-id="342e0-113">Click Duplicate kanban rule.</span></span>
    * <span data-ttu-id="342e0-114">Kun kanban-säännöstä tehdään kaksoiskappale, tyyppi-, päivämäärä-, tehtävä -ja tuotevalintaa voi muuttaa.</span><span class="sxs-lookup"><span data-stu-id="342e0-114">When duplicating a kanban rule, it is possible to change type, dates, activities, and the product selection.</span></span> <span data-ttu-id="342e0-115">Tämän menettely vaihdetaan menettelyn seuraavassa vaiheessa.</span><span class="sxs-lookup"><span data-stu-id="342e0-115">Change the product for this procedure in the next step.</span></span>  
2. <span data-ttu-id="342e0-116">Anna tai valitse Tuote-kentässä arvo.</span><span class="sxs-lookup"><span data-stu-id="342e0-116">In the Product field, enter or select a value.</span></span>
    * <span data-ttu-id="342e0-117">Valitse M0007.</span><span class="sxs-lookup"><span data-stu-id="342e0-117">Select M0007.</span></span>  
3. <span data-ttu-id="342e0-118">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="342e0-118">Click OK.</span></span>
    * <span data-ttu-id="342e0-119">Huomaa, että kanban-säännön 000017 kaksoiskappale luodaan.</span><span class="sxs-lookup"><span data-stu-id="342e0-119">Note that a duplicate of kanban rule 000017 is created.</span></span>    

