--- 
title: "Määritä ennakonpidätys"
description: "Ennakonpidätys on toimittajilta perittävä vero, josta ei synny arvonlisäverotapahtumia."
author: ShylaThompson
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: d9747ba144d56c9410846769e5465372c89ea111
ms.openlocfilehash: 362df7c97adae2526cb61b07e3022dc3b63fc59e
ms.contentlocale: fi-fi
ms.lasthandoff: 08/07/2018

---
# <a name="set-up-withholding-tax"></a><span data-ttu-id="a954e-103">Määritä ennakonpidätys</span><span class="sxs-lookup"><span data-stu-id="a954e-103">Set up withholding tax</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="a954e-104">Ennakonpidätys on toimittajilta perittävä vero, josta ei synny arvonlisäverotapahtumia.</span><span class="sxs-lookup"><span data-stu-id="a954e-104">Withholding tax is a tax on vendors that does not create sales tax transactions.</span></span> <span data-ttu-id="a954e-105">Toimittajien maksuista laskettava ennakonpidätys on velkaa.</span><span class="sxs-lookup"><span data-stu-id="a954e-105">Withholding tax that is calculated on vendor payments is a liability.</span></span> <span data-ttu-id="a954e-106">Sen vuoksi ennakonpidätyksen voi kirjata vain tase- tai velkatileille.</span><span class="sxs-lookup"><span data-stu-id="a954e-106">Therefore, only balance sheet accounts or liability accounts are valid accounts for posting withholding tax.</span></span> <span data-ttu-id="a954e-107">Tässä tehtävän ohjauksessa kerrotaan, miten ennakonpidätys määritetään.</span><span class="sxs-lookup"><span data-stu-id="a954e-107">This task guide demonstrates how to set up withholding tax.</span></span>

1. <span data-ttu-id="a954e-108">Siirry kohtaan Vero > Välilliset verot > Ennakonpidätys > Ennakonpidätyskoodit.</span><span class="sxs-lookup"><span data-stu-id="a954e-108">Go to Tax > Indirect taxes > Withholding tax > Withholding tax codes.</span></span>
2. <span data-ttu-id="a954e-109">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="a954e-109">Click New.</span></span>
3. <span data-ttu-id="a954e-110">Kirjoita Ennakonpidätyskoodi-kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="a954e-110">In the Withholding tax code field, type a value.</span></span>
4. <span data-ttu-id="a954e-111">Syötä Ennakonpidätyksen nimi -kenttään ennakonpidätyskoodin nimi.</span><span class="sxs-lookup"><span data-stu-id="a954e-111">In the Withholding tax name field, enter the name of the withholding tax code.</span></span>
5. <span data-ttu-id="a954e-112">Valitse Päätili-kentässä päätili ennakonpidätysvelan kirjaamista varten.</span><span class="sxs-lookup"><span data-stu-id="a954e-112">In the Main account field, select the main account for posting the withholding tax liability.</span></span>
6. <span data-ttu-id="a954e-113">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="a954e-113">Click Save.</span></span>
7. <span data-ttu-id="a954e-114">Valitse Arvot.</span><span class="sxs-lookup"><span data-stu-id="a954e-114">Click Values.</span></span>
8. <span data-ttu-id="a954e-115">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="a954e-115">In the list, mark the selected row.</span></span>
9. <span data-ttu-id="a954e-116">Syötä Arvo-kenttään ennakonpidätyksen laskemisessa käytettävä prosenttiluku.</span><span class="sxs-lookup"><span data-stu-id="a954e-116">In the Value field, enter a percentage used for the calculation of the withholding tax.</span></span>
10. <span data-ttu-id="a954e-117">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="a954e-117">Click Save.</span></span>
11. <span data-ttu-id="a954e-118">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="a954e-118">Close the page.</span></span>
12. <span data-ttu-id="a954e-119">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="a954e-119">Click Save.</span></span>
13. <span data-ttu-id="a954e-120">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="a954e-120">Close the page.</span></span>
14. <span data-ttu-id="a954e-121">Siirry kohtaan Vero > Välilliset verot > Ennakonpidätys > Ennakonpidätysryhmät.</span><span class="sxs-lookup"><span data-stu-id="a954e-121">Go to Tax > Indirect taxes > Withholding tax > Withholding tax groups.</span></span>
15. <span data-ttu-id="a954e-122">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="a954e-122">Click New.</span></span>
16. <span data-ttu-id="a954e-123">Syötä Ennakonpidätysryhmä-kenttään ennakonpidätysryhmän tunnus.</span><span class="sxs-lookup"><span data-stu-id="a954e-123">In the Withholding tax group field, enter the identifier of the withholding tax group.</span></span>
17. <span data-ttu-id="a954e-124">Syötä Kuvaus-kenttään ennakonpidätysryhmän nimi.</span><span class="sxs-lookup"><span data-stu-id="a954e-124">In the Description field, enter the name of the withholding tax group.</span></span>
18. <span data-ttu-id="a954e-125">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="a954e-125">In the list, mark the selected row.</span></span>
19. <span data-ttu-id="a954e-126">Valitse Ennakonpidätyskoodi-kentässä ennakonpidätyskoodi.</span><span class="sxs-lookup"><span data-stu-id="a954e-126">In the Withholding tax code field, select the withholding tax code.</span></span>
20. <span data-ttu-id="a954e-127">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="a954e-127">In the list, click the link in the selected row.</span></span>
21. <span data-ttu-id="a954e-128">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="a954e-128">Click Save.</span></span>


