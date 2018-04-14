--- 
title: "Bonuspoiston määrittäminen"
description: "Tässä menettelyssä kerrotaan, miten erityinen poistovähennys luodaan ja liitetään käyttöomaisuuskirjaan."
author: saraschi2
manager: AnnBe
ms.date: 10/11/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 3d78be58ee678dbe7a5b5c8798e626125e6a0755
ms.contentlocale: fi-fi
ms.lasthandoff: 04/13/2018

---
# <a name="set-up-bonus-depreciation"></a><span data-ttu-id="1c95d-103">Bonuspoiston määrittäminen</span><span class="sxs-lookup"><span data-stu-id="1c95d-103">Set up bonus depreciation</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="1c95d-104">Tässä menettelyssä kerrotaan, miten erityinen poistovähennys luodaan ja liitetään käyttöomaisuuskirjaan.</span><span class="sxs-lookup"><span data-stu-id="1c95d-104">This procedure shows how to create a special depreciation allowance and associate it with a fixed asset book.</span></span> <span data-ttu-id="1c95d-105">Siinä käytetään kirjanpitäjän roolia ja USMF-yrityksen esittelytietoja.</span><span class="sxs-lookup"><span data-stu-id="1c95d-105">It uses the accountant role and demo data for the USMF legal entity.</span></span>


## <a name="create-a-special-depreciation-allowance"></a><span data-ttu-id="1c95d-106">Erityisen poistovähennyksen luominen</span><span class="sxs-lookup"><span data-stu-id="1c95d-106">Create a special depreciation allowance</span></span>
1. <span data-ttu-id="1c95d-107">Siirry kohtaan Käyttöomaisuus > Asetukset > Erityinen poistovähennys.</span><span class="sxs-lookup"><span data-stu-id="1c95d-107">Go to Fixed assets > Setup > Special depreciation allowance.</span></span>
2. <span data-ttu-id="1c95d-108">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="1c95d-108">Click New.</span></span>
3. <span data-ttu-id="1c95d-109">Kirjoita Erityinen poistovähennys -kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="1c95d-109">In the Special depreciation allowance field, type a value.</span></span>
4. <span data-ttu-id="1c95d-110">Kirjoita arvo Kuvaus-kenttään.</span><span class="sxs-lookup"><span data-stu-id="1c95d-110">In the Description field, type a value.</span></span>
5. <span data-ttu-id="1c95d-111">Syötä Prosentti-kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="1c95d-111">In the Percentage field, enter a number.</span></span>
    * <span data-ttu-id="1c95d-112">Määritä summa, jos prosenttia ei ole ilmoitettu.</span><span class="sxs-lookup"><span data-stu-id="1c95d-112">If a percentage was not indicated, set an amount.</span></span>  

## <a name="associate-a-special-depreciation-allowance-with-a-fixed-asset-group-book"></a><span data-ttu-id="1c95d-113">Erityisen poistovähennyksen liittäminen käyttöomaisuusryhmän kirjaan</span><span class="sxs-lookup"><span data-stu-id="1c95d-113">Associate a special depreciation allowance with a fixed asset group book</span></span>
1. <span data-ttu-id="1c95d-114">Siirry kohtaan Käyttöomaisuus > Asetukset > Käyttöomaisuusryhmät.</span><span class="sxs-lookup"><span data-stu-id="1c95d-114">Go to Fixed assets > Setup > Fixed asset groups.</span></span>
2. <span data-ttu-id="1c95d-115">Valitse luettelosta erityiseen poistovähennykseen liitetty käyttöomaisuusryhmä.</span><span class="sxs-lookup"><span data-stu-id="1c95d-115">In the list, select the fixed asset group associated with the special depreciation allowance.</span></span>
3. <span data-ttu-id="1c95d-116">Valitse Kirjat.</span><span class="sxs-lookup"><span data-stu-id="1c95d-116">Click Books.</span></span>
4. <span data-ttu-id="1c95d-117">Valitse luettelosta erityiseen poistovähennykseen liitetty kirja.</span><span class="sxs-lookup"><span data-stu-id="1c95d-117">In the list, select the book that is associated with the special depreciation allowance.</span></span>
5. <span data-ttu-id="1c95d-118">Valitse Erityinen poistovähennys.</span><span class="sxs-lookup"><span data-stu-id="1c95d-118">Click Special depreciation allowance.</span></span>
6. <span data-ttu-id="1c95d-119">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="1c95d-119">Click New.</span></span>
7. <span data-ttu-id="1c95d-120">Kirjoita tai valitse Erityinen poistovähennys -kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="1c95d-120">In the Special depreciation allowance field, enter or select a value.</span></span>
    * <span data-ttu-id="1c95d-121">Prosentin tai summan oletusarvo saadaan erityisen poistovähennyksen asetuksista.</span><span class="sxs-lookup"><span data-stu-id="1c95d-121">The default for Percentage or Amount comes from the special depreciation allowance setup.</span></span>  
8. <span data-ttu-id="1c95d-122">Syötä numero Prioriteetti-kenttään.</span><span class="sxs-lookup"><span data-stu-id="1c95d-122">In the Priority field, enter a number.</span></span>


