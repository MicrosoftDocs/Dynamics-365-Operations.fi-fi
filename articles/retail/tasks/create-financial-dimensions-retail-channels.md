--- 
title: "Luo vähittäismyyntikanaville taloushallinnon dimensiot ja määritä dimensioarvot myymälöille"
description: "Tässä menetelmässä kerrotaan, miten vähittäismyyntikanavan taloushallinnon dimensio ja dimension arvot luodaan ja vähittäismyymälöiden taloushallinnon dimensioiden arvot määritetään."
author: jashanno
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations, Retail
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: d0ee9e2edcda436d3dec6f9002a2d3d30de85503
ms.contentlocale: fi-fi
ms.lasthandoff: 04/13/2018

---
# <a name="create-financial-dimensions-for-retail-channels-and-configure-dimension-values-on-stores"></a><span data-ttu-id="1bf1d-103">Luo vähittäismyyntikanaville taloushallinnon dimensiot ja määritä dimensioarvot myymälöille</span><span class="sxs-lookup"><span data-stu-id="1bf1d-103">Create financial dimensions for Retail channels and configure dimension values on stores</span></span>

[!INCLUDE [task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="1bf1d-104">Tässä menetelmässä kerrotaan, miten vähittäismyyntikanavan taloushallinnon dimensio ja dimension arvot luodaan ja vähittäismyymälöiden taloushallinnon dimensioiden arvot määritetään.</span><span class="sxs-lookup"><span data-stu-id="1bf1d-104">This procedure walks through creating a retail channel financial dimension with dimension values and steps to configure financial dimension values on retail stores.</span></span> <span data-ttu-id="1bf1d-105">Aihe ei sisällä muita liittyviä vaiheita, kuten dimensiojoukkojen ja tilirakenteiden luomista.</span><span class="sxs-lookup"><span data-stu-id="1bf1d-105">The topic does not include other related steps, such as creating dimension sets and account structures.</span></span> <span data-ttu-id="1bf1d-106">Menettely käyttää esittelytietojen USRT-yritystä.</span><span class="sxs-lookup"><span data-stu-id="1bf1d-106">This procedure uses the USRT company in demo data.</span></span>

1. <span data-ttu-id="1bf1d-107">Valitse Kirjanpito > Tilikartta > Dimensiot > Taloushallinnon dimensiot.</span><span class="sxs-lookup"><span data-stu-id="1bf1d-107">Go to General ledger > Chart of accounts > Dimensions > Financial dimensions.</span></span>
2. <span data-ttu-id="1bf1d-108">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="1bf1d-108">Click New.</span></span>
3. <span data-ttu-id="1bf1d-109">Valitse Käytä arvoja -kenttään Vähittäismyyntikanavat.</span><span class="sxs-lookup"><span data-stu-id="1bf1d-109">In the Use values from field, select 'Retail channels'.</span></span>
4. <span data-ttu-id="1bf1d-110">Kirjoita arvo Dimension nimi -kenttään.</span><span class="sxs-lookup"><span data-stu-id="1bf1d-110">In the Dimension name field, type a value.</span></span>
5. <span data-ttu-id="1bf1d-111">Valitse Aktivoi.</span><span class="sxs-lookup"><span data-stu-id="1bf1d-111">Click Activate.</span></span>
6. <span data-ttu-id="1bf1d-112">Valitse Sulje.</span><span class="sxs-lookup"><span data-stu-id="1bf1d-112">Click Close.</span></span>
7. <span data-ttu-id="1bf1d-113">Valitse Aktivoi.</span><span class="sxs-lookup"><span data-stu-id="1bf1d-113">Click Activate.</span></span>
8. <span data-ttu-id="1bf1d-114">Valitse Dimensioarvot.</span><span class="sxs-lookup"><span data-stu-id="1bf1d-114">Click Dimension values.</span></span>
9. <span data-ttu-id="1bf1d-115">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="1bf1d-115">Close the page.</span></span>
10. <span data-ttu-id="1bf1d-116">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="1bf1d-116">Click Save.</span></span>
11. <span data-ttu-id="1bf1d-117">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="1bf1d-117">Close the page.</span></span>
12. <span data-ttu-id="1bf1d-118">Siirry kohtaan Vähittäismyynti ja kauppa > Kanavat > Vähittäismyymälät > Kaikki vähittäismyymälät.</span><span class="sxs-lookup"><span data-stu-id="1bf1d-118">Go to Retail and commerce > Channels > Retail stores > All retail stores.</span></span>
13. <span data-ttu-id="1bf1d-119">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="1bf1d-119">In the list, click the link in the selected row.</span></span>
14. <span data-ttu-id="1bf1d-120">Ota käyttöön Taloushallinnon dimensiot -osan laajennus.</span><span class="sxs-lookup"><span data-stu-id="1bf1d-120">Toggle the expansion of the Financial dimensions section.</span></span>
15. <span data-ttu-id="1bf1d-121">Valitse Muokkaa.</span><span class="sxs-lookup"><span data-stu-id="1bf1d-121">Click Edit.</span></span>
16. <span data-ttu-id="1bf1d-122">Avaa haku valitsemalla Retailchannel-kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="1bf1d-122">In the Retailchannel field, click the drop-down button to open the lookup.</span></span>
17. <span data-ttu-id="1bf1d-123">Etsi ja valitse luettelosta päivitettävän myymälän dimension arvo.</span><span class="sxs-lookup"><span data-stu-id="1bf1d-123">In the list, find and select the dimension value for the store being updated.</span></span>
18. <span data-ttu-id="1bf1d-124">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="1bf1d-124">In the list, click the link in the selected row.</span></span>
19. <span data-ttu-id="1bf1d-125">Avaa haku valitsemalla CostCenter-kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="1bf1d-125">In the CostCenter field, click the drop-down button to open the lookup.</span></span>
20. <span data-ttu-id="1bf1d-126">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="1bf1d-126">In the list, find and select the desired record.</span></span>
21. <span data-ttu-id="1bf1d-127">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="1bf1d-127">In the list, click the link in the selected row.</span></span>
22. <span data-ttu-id="1bf1d-128">Avaa haku valitsemalla Osasto-kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="1bf1d-128">In the Department field, click the drop-down button to open the lookup.</span></span>
23. <span data-ttu-id="1bf1d-129">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="1bf1d-129">In the list, find and select the desired record.</span></span>
24. <span data-ttu-id="1bf1d-130">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="1bf1d-130">In the list, click the link in the selected row.</span></span>
25. <span data-ttu-id="1bf1d-131">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="1bf1d-131">Click Save.</span></span>


