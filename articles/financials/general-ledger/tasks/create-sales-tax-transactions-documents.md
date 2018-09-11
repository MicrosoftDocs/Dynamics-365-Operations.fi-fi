--- 
title: "Luo arvonlisäverotapahtumia asiakirjoihin"
description: "Asiakirjojen arvonlisävero lasketaan määrittämällä arvonlisäveroryhmä ja nimikkeen arvonlisäveroryhmä asiakirjariveille."
author: twheeloc
manager: AnnBe
ms.date: 8/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable, TaxTmpWorkTrans
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 32d71167fdad65cb1dec37671999a497759ca484
ms.openlocfilehash: 4e2edf0688224c6fcd0940f94801562440604d27
ms.contentlocale: fi-fi
ms.lasthandoff: 09/11/2018

---
# <a name="create-sales-tax-transactions-on-documents"></a><span data-ttu-id="20daf-103">Luo arvonlisäverotapahtumia asiakirjoihin</span><span class="sxs-lookup"><span data-stu-id="20daf-103">Create sales tax transactions on documents</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="20daf-104">Asiakirjojen arvonlisävero lasketaan määrittämällä arvonlisäveroryhmä ja nimikkeen arvonlisäveroryhmä asiakirjariveille.</span><span class="sxs-lookup"><span data-stu-id="20daf-104">Sales tax on documents is calculated by providing a Sales tax group and an Item sales tax group on document lines.</span></span> <span data-ttu-id="20daf-105">Näiden oletusarvot saadaan päätiedoista, mutta arvoja voi muuttaa manuaalisesti tarvittaessa.</span><span class="sxs-lookup"><span data-stu-id="20daf-105">These default from master data but can be changed manually if necessary.</span></span> <span data-ttu-id="20daf-106">Laskettu arvonlisävero voidaan tarkistaa rivi- ja asiakirjatasolla.</span><span class="sxs-lookup"><span data-stu-id="20daf-106">The calculated sales tax can be checked on a line and document level.</span></span> <span data-ttu-id="20daf-107">Tässä tehtävässä käytetään esittely-yritystä USMF.</span><span class="sxs-lookup"><span data-stu-id="20daf-107">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="20daf-108">Siirry kohtaan Myyntireskontra > Tilaukset > Kaikki myyntitilaukset.</span><span class="sxs-lookup"><span data-stu-id="20daf-108">Go to Accounts receivable > Orders > All sales orders.</span></span>
2. <span data-ttu-id="20daf-109">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="20daf-109">Click New.</span></span>
3. <span data-ttu-id="20daf-110">Avaa haku valitsemalla Asiakastili-kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="20daf-110">In the Customer account field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="20daf-111">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="20daf-111">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="20daf-112">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="20daf-112">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="20daf-113">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="20daf-113">Click OK.</span></span>
7. <span data-ttu-id="20daf-114">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="20daf-114">In the list, mark the selected row.</span></span>
8. <span data-ttu-id="20daf-115">Avaa haku valitsemalla Nimiketunnus-kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="20daf-115">In the Item number field, click the drop-down button to open the lookup.</span></span>
9. <span data-ttu-id="20daf-116">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="20daf-116">In the list, click the link in the selected row.</span></span>
10. <span data-ttu-id="20daf-117">Syötä Yksikköhinta-kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="20daf-117">In the Unit price field, enter a number.</span></span>
11. <span data-ttu-id="20daf-118">Laajenna tai tiivistä Rivitiedot-osa.</span><span class="sxs-lookup"><span data-stu-id="20daf-118">Expand or collapse the Line details section.</span></span>
12. <span data-ttu-id="20daf-119">Valitse Asetukset-välilehti.</span><span class="sxs-lookup"><span data-stu-id="20daf-119">Click the Setup tab.</span></span>
13. <span data-ttu-id="20daf-120">Avaa haku valitsemalla Nimikkeen arvonlisäveroryhmä -kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="20daf-120">In the Item sales tax group field, click the drop-down button to open the lookup.</span></span>
14. <span data-ttu-id="20daf-121">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="20daf-121">In the list, find and select the desired record.</span></span>
15. <span data-ttu-id="20daf-122">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="20daf-122">In the list, click the link in the selected row.</span></span>
16. <span data-ttu-id="20daf-123">Valitse Myyntitiedot.</span><span class="sxs-lookup"><span data-stu-id="20daf-123">Click Financials.</span></span>
17. <span data-ttu-id="20daf-124">Valitse Arvonlisävero.</span><span class="sxs-lookup"><span data-stu-id="20daf-124">Click Sales tax.</span></span>
18. <span data-ttu-id="20daf-125">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="20daf-125">Click OK.</span></span>
19. <span data-ttu-id="20daf-126">Valitse Lisää rivi.</span><span class="sxs-lookup"><span data-stu-id="20daf-126">Click Add line.</span></span>
20. <span data-ttu-id="20daf-127">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="20daf-127">In the list, mark the selected row.</span></span>
21. <span data-ttu-id="20daf-128">Avaa haku valitsemalla Nimiketunnus-kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="20daf-128">In the Item number field, click the drop-down button to open the lookup.</span></span>
22. <span data-ttu-id="20daf-129">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="20daf-129">In the list, find and select the desired record.</span></span>
23. <span data-ttu-id="20daf-130">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="20daf-130">In the list, click the link in the selected row.</span></span>
24. <span data-ttu-id="20daf-131">Syötä Yksikköhinta-kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="20daf-131">In the Unit price field, enter a number.</span></span>
25. <span data-ttu-id="20daf-132">Avaa haku valitsemalla Nimikkeen arvonlisäveroryhmä -kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="20daf-132">In the Item sales tax group field, click the drop-down button to open the lookup.</span></span>
26. <span data-ttu-id="20daf-133">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="20daf-133">In the list, find and select the desired record.</span></span>
27. <span data-ttu-id="20daf-134">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="20daf-134">In the list, click the link in the selected row.</span></span>
28. <span data-ttu-id="20daf-135">Valitse toimintoruudussa Myynti.</span><span class="sxs-lookup"><span data-stu-id="20daf-135">On the Action Pane, click Sell.</span></span>
29. <span data-ttu-id="20daf-136">Valitse Arvonlisävero.</span><span class="sxs-lookup"><span data-stu-id="20daf-136">Click Sales tax.</span></span>
30. <span data-ttu-id="20daf-137">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="20daf-137">Click OK.</span></span>


