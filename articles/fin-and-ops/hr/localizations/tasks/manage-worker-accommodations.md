--- 
title: "Hallitse työntekijän apuvälineitä"
description: "Tässä menettelyssä esitellään työympäristön apuvälinetyyppien määrittäminen. Tyyppejä ovat esimerkiksi ergonominen tuoli ja jaksoittaiset tauot."
author: ShielaSogge
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Operations
ms.search.region: Global
ms.author: shielas
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 10d34d0b2eca95034d1f67931ff72a035be9a6b8
ms.contentlocale: fi-fi
ms.lasthandoff: 09/29/2017

---
# <a name="manage-worker-accommodations"></a><span data-ttu-id="87540-103">Hallitse työntekijän apuvälineitä</span><span class="sxs-lookup"><span data-stu-id="87540-103">Manage worker accommodations</span></span>

[!include[task guide banner](../../../includes/task-guide-banner.md)]

<span data-ttu-id="87540-104">Tässä menettelyssä esitellään työympäristön apuvälinetyyppien määrittäminen. Tyyppejä ovat esimerkiksi ergonominen tuoli ja jaksoittaiset tauot.</span><span class="sxs-lookup"><span data-stu-id="87540-104">This procedure walks through the steps for setting up work environment accommodation types, such as ergonomic chairs or periodic breaks.</span></span> <span data-ttu-id="87540-105">Menettelyssä kerrotaan myös, miten apuvälinetyypit liitetään työntekijään sekä miten apuvälinetyypit hyväksytään ja hylätään.</span><span class="sxs-lookup"><span data-stu-id="87540-105">It also shows how to assign these accommodation types to a worker, and either approve or deny the accommodation type.</span></span> <span data-ttu-id="87540-106">Tämän menettelyn luomisessa käytetty esittely-yritys on USMF.</span><span class="sxs-lookup"><span data-stu-id="87540-106">The demo data company used to create this procedure is USMF.</span></span>


## <a name="setup-accommodations"></a><span data-ttu-id="87540-107">Apuvälineiden määrittäminen</span><span class="sxs-lookup"><span data-stu-id="87540-107">Setup accommodations</span></span>
1. <span data-ttu-id="87540-108">Siirry kohtaan Henkilöstöhallinto > Asetukset > Apuvälinetyypit.</span><span class="sxs-lookup"><span data-stu-id="87540-108">Go to Human resources > Setup > Accommodation types.</span></span>
2. <span data-ttu-id="87540-109">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="87540-109">Click New.</span></span>
3. <span data-ttu-id="87540-110">Syötä Apuvälinetyyppi-kenttään apuvälineen nimi.</span><span class="sxs-lookup"><span data-stu-id="87540-110">In the Accommodation type field, enter a name for the accommodation.</span></span> <span data-ttu-id="87540-111">Esimerkki: Näppäimistö.</span><span class="sxs-lookup"><span data-stu-id="87540-111">Example: Keyboard.</span></span>
4. <span data-ttu-id="87540-112">Syötä Kuvaus-kenttään apuvälineen kuvaus.</span><span class="sxs-lookup"><span data-stu-id="87540-112">In the Description field, enter a description for the accommodation.</span></span> <span data-ttu-id="87540-113">Esimerkki: Ergonominen näppäimistö.</span><span class="sxs-lookup"><span data-stu-id="87540-113">Example: Ergonomic Keyboard.</span></span>
5. <span data-ttu-id="87540-114">Syötä Huomautus-kenttään apuvälinettä kuvaavat tiedot.</span><span class="sxs-lookup"><span data-stu-id="87540-114">In the Note field, enter any information that helps to clarify the accommodation.</span></span>
6. <span data-ttu-id="87540-115">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="87540-115">Click Save.</span></span>
7. <span data-ttu-id="87540-116">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="87540-116">Close the page.</span></span>

## <a name="assign-accommodations"></a><span data-ttu-id="87540-117">Apuvälineiden liittäminen</span><span class="sxs-lookup"><span data-stu-id="87540-117">Assign accommodations</span></span>
1. <span data-ttu-id="87540-118">Siirry kohtaan Henkilöstöhallinto > Työntekijät > Työntekijät.</span><span class="sxs-lookup"><span data-stu-id="87540-118">Go to Human resources > Workers > Employees.</span></span>
2. <span data-ttu-id="87540-119">Valitse työntekijä luettelosta.</span><span class="sxs-lookup"><span data-stu-id="87540-119">From the list, select an employee.</span></span>
3. <span data-ttu-id="87540-120">Valitse työntekijän nimi, kun haluat tarkastella apuvälinettä pyytäneen työntekijän tietoja.</span><span class="sxs-lookup"><span data-stu-id="87540-120">Click the employee's name to view details about the employee who is requesting the accommodation.</span></span>
4. <span data-ttu-id="87540-121">Laajenna Henkilökohtaiset tiedot -pikavälilehti.</span><span class="sxs-lookup"><span data-stu-id="87540-121">Expand the Personal information FastTab.</span></span>
5. <span data-ttu-id="87540-122">Valitse Apuvälineet.</span><span class="sxs-lookup"><span data-stu-id="87540-122">Click Accommodations.</span></span>
6. <span data-ttu-id="87540-123">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="87540-123">Click New.</span></span>
7. <span data-ttu-id="87540-124">Valitse sopiva apuväline Apuvälinetyyppi-kentässä.</span><span class="sxs-lookup"><span data-stu-id="87540-124">In the Accommodation type field, select the appropriate accommodation.</span></span> <span data-ttu-id="87540-125">Esimerkki: Näppäimistö</span><span class="sxs-lookup"><span data-stu-id="87540-125">Example: Keyboard</span></span>
8. <span data-ttu-id="87540-126">Syötä Työn tila -kenttään työtehtävä, jossa apuvälinettä tarvitaan.</span><span class="sxs-lookup"><span data-stu-id="87540-126">In the Job task field, enter the work task that requires the accommodation.</span></span>
9. <span data-ttu-id="87540-127">Syötä Tila-kenttään sopiva tila.</span><span class="sxs-lookup"><span data-stu-id="87540-127">In the Status field, enter the appropriate status.</span></span> <span data-ttu-id="87540-128">Esimerkki: Kohtuullinen</span><span class="sxs-lookup"><span data-stu-id="87540-128">Example: Reasonable</span></span>
    * <span data-ttu-id="87540-129">Seuraavat tilat ovat käytettävissä.</span><span class="sxs-lookup"><span data-stu-id="87540-129">The following statuses are available.</span></span> <span data-ttu-id="87540-130">Pyydetty ilmaisee, että apuväline on luotu, mutta sitä ei ole vielä tarkistettu.</span><span class="sxs-lookup"><span data-stu-id="87540-130">Requested indicates that the accommodation has been created but not yet reviewed.</span></span> <span data-ttu-id="87540-131">Kohtuullinen ilmaisee, että apuväline on kohtuullinen ja se myönnetään.</span><span class="sxs-lookup"><span data-stu-id="87540-131">Reasonable indicates that the accommodation is reasonable and will be granted.</span></span> <span data-ttu-id="87540-132">Vaikea ilmaisee, että apuväline on liian suuri kuormitus työnantajalle, ja se hylätään.</span><span class="sxs-lookup"><span data-stu-id="87540-132">Undue hardship indicates that the accommodation will place an unreasonable burden on the employer, and has been denied.</span></span> <span data-ttu-id="87540-133">Tässä esimerkissä pyyntö hyväksyttiin heti, koska apuvälinepyyntö oli pieni.</span><span class="sxs-lookup"><span data-stu-id="87540-133">In this example, the request was approved immediately because the accommodation request was minimal.</span></span>  
10. <span data-ttu-id="87540-134">Valitse Hyväksytty-kentässä henkilö, joka hyväksyi apuvälinepyynnön.</span><span class="sxs-lookup"><span data-stu-id="87540-134">In the Accepted field, select the person who accepted the accommodation request.</span></span>
11. <span data-ttu-id="87540-135">Klikkaa Valitse.</span><span class="sxs-lookup"><span data-stu-id="87540-135">Click Select.</span></span>
12. <span data-ttu-id="87540-136">Syötä Hyväksymispäivämäärä-kenttään apuvälinepyynnön hyväksymispäivämäärä ja -aika.</span><span class="sxs-lookup"><span data-stu-id="87540-136">In the Accepted date field, enter the date and time when the accommodation request was accepted.</span></span>
13. <span data-ttu-id="87540-137">Laajenna Huomautus-osa.</span><span class="sxs-lookup"><span data-stu-id="87540-137">Expand the Note section.</span></span>
14. <span data-ttu-id="87540-138">Syötä Talous-kenttään tiedot tai resurssikustannukset, joiden avulla apuvälineen merkitystä voidaan selvittää.</span><span class="sxs-lookup"><span data-stu-id="87540-138">In the Financial field, enter any information or resource costs that helps to clarify the impact of the accommodation.</span></span>
    * <span data-ttu-id="87540-139">Jos apuväline on hylätty, Vastaus-kenttään kirjoitetaan hylkäyksen syy.</span><span class="sxs-lookup"><span data-stu-id="87540-139">If the accommodation has been denied, the Reply field can be used to indicate why a request was denied.</span></span>  
15. <span data-ttu-id="87540-140">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="87540-140">Click Save.</span></span>


