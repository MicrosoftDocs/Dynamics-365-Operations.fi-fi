---
title: Määritä resurssin ominaisuudet
description: Resurssin ominaisuudet kertovat, mitä operatiiviset resurssit voivat tehdä.
author: sorenva
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WrkCtrCapability
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: sorenand
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 6bd3f2b1efc1e6a883ad2a25d127e74a8925de8f
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/18/2020
ms.locfileid: "3146787"
---
# <a name="define-resource-capabilities"></a><span data-ttu-id="b177d-103">Määritä resurssin ominaisuudet</span><span class="sxs-lookup"><span data-stu-id="b177d-103">Define resource capabilities</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="b177d-104">Resurssin ominaisuudet kertovat, mitä operatiiviset resurssit voivat tehdä.</span><span class="sxs-lookup"><span data-stu-id="b177d-104">Resource capabilities describe what operations resources can do.</span></span> <span data-ttu-id="b177d-105">Ajoituksen aikana kunkin työn ja työvaiheen vaatimukset kohdistetaan käytettävissä olevien resurssien ominaisuuksiin.</span><span class="sxs-lookup"><span data-stu-id="b177d-105">During scheduling, the requirements of each job and operation are matched against the capabilities of the available resources.</span></span> <span data-ttu-id="b177d-106">Tämä tehtävän ohjaus auttaa resurssin ominaisuuden luomisessa ja ominaisuuden liittämisessä resurssiin.</span><span class="sxs-lookup"><span data-stu-id="b177d-106">This task guide will help you create a resource capability and assign it to a resource.</span></span> <span data-ttu-id="b177d-107">Tämän tehtävän luomisessa käytetty esittely-yritys on USMF.</span><span class="sxs-lookup"><span data-stu-id="b177d-107">The demo data company used to create this task is USMF.</span></span>


## <a name="create-a-resource-capability"></a><span data-ttu-id="b177d-108">Resurssin ominaisuuden luominen</span><span class="sxs-lookup"><span data-stu-id="b177d-108">Create a resource capability</span></span>
1. <span data-ttu-id="b177d-109">Siirry Resurssin ominaisuudet -kohtaan.</span><span class="sxs-lookup"><span data-stu-id="b177d-109">Go to Resource capabilities.</span></span>
2. <span data-ttu-id="b177d-110">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="b177d-110">Click New.</span></span>
3. <span data-ttu-id="b177d-111">Kirjoita resurssin ominaisuuden tunnus Ominaisuus-kenttään.</span><span class="sxs-lookup"><span data-stu-id="b177d-111">In the Capability field, type the ID of the resource capability.</span></span>
    * <span data-ttu-id="b177d-112">Ominaisuuden tunnuksen avulla voit määrittää annetun työvaiheen ne resurssit, joilla on oltava tämä ominaisuus työvaiheen suorittamista varten.</span><span class="sxs-lookup"><span data-stu-id="b177d-112">For a given operation, you use the capability ID to specify that resources must have this capability to perform the operation.</span></span>  
4. <span data-ttu-id="b177d-113">Syötä ominaisuuden kuvaus Kuvaus-kenttään.</span><span class="sxs-lookup"><span data-stu-id="b177d-113">In the Description field, enter a description of the capability.</span></span>

## <a name="assign-capability-to-a-resource"></a><span data-ttu-id="b177d-114">Ominaisuuden määrittäminen resurssille</span><span class="sxs-lookup"><span data-stu-id="b177d-114">Assign capability to a resource</span></span>
1. <span data-ttu-id="b177d-115">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="b177d-115">Click Add.</span></span>
2. <span data-ttu-id="b177d-116">Kirjoita resurssin tunnus Resurssi-kenttään.</span><span class="sxs-lookup"><span data-stu-id="b177d-116">In the Resource field, type the ID of the resource.</span></span>
    * <span data-ttu-id="b177d-117">Resurssin ominaisuus voidaan määrittää yhteen tai useaan resurssiin.</span><span class="sxs-lookup"><span data-stu-id="b177d-117">A resource capability can be assigned to one or more resources.</span></span>  
3. <span data-ttu-id="b177d-118">Syötä päivämäärä Päättyminen-kenttään.</span><span class="sxs-lookup"><span data-stu-id="b177d-118">In the Expiration field, enter a date.</span></span>
    * <span data-ttu-id="b177d-119">Tämän kentän avulla voit määrittää resurssin, jolla on ominaisuus vain rajoitetun ajan.</span><span class="sxs-lookup"><span data-stu-id="b177d-119">You can use this field to specify that a resource has the capability for only a limited time.</span></span>  
4. <span data-ttu-id="b177d-120">Syötä numero Prioriteetti-kenttään.</span><span class="sxs-lookup"><span data-stu-id="b177d-120">In the Priority field, enter a number.</span></span>
    * <span data-ttu-id="b177d-121">Töiden ja työvaiheiden ajoittamisen yhteydessä voit määrittää, valitaanko resurssit prioriteetin mukaan.</span><span class="sxs-lookup"><span data-stu-id="b177d-121">When you schedule jobs and operations, you can specify whether to select resources by priority.</span></span> <span data-ttu-id="b177d-122">Jos tämä on valittu ja usea resurssi voi suorittaa työn tai työvaiheen vaadittuun päivämäärään mennessä, valitaan resurssi, jolla on liittyvän pakollisen ominaisuuden alhaisin prioriteetti.</span><span class="sxs-lookup"><span data-stu-id="b177d-122">If you choose to do this, and more than one resource can perform the job or operation by the requested date, the resource that has the lowest priority with respect to the required capability is selected.</span></span>  
5. <span data-ttu-id="b177d-123">Syötä numero Taso-kenttään.</span><span class="sxs-lookup"><span data-stu-id="b177d-123">In the Level field, enter a number.</span></span>
    * <span data-ttu-id="b177d-124">Kun määrität, että työ tai työvaihe vaatii tietyn ominaisuuden, voit määrittää myös vaadittavan vähimmäistason.</span><span class="sxs-lookup"><span data-stu-id="b177d-124">When you specify that a job or operation requires a particular capability, you can also specify the minimum level that is required.</span></span> <span data-ttu-id="b177d-125">Ominaisuuden tason avulla voit erotella resurssit, jotka voivat suorittaa saman työn, mutta jotka käyttävät erilaista nopeutta, voimaa jne.</span><span class="sxs-lookup"><span data-stu-id="b177d-125">Use the capability level to differentiate resources that can perform the same job, but at different speeds, strengths, sizes, and so on.</span></span>  

