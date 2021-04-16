---
title: Taloushallinnon dimensioiden luominen vähittäismyyntikanaville ja dimensioarvojen määrittäminen myymälöille
description: Tässä menetelmässä kerrotaan, miten kaupankäyntikanavan taloushallinnon dimensio ja dimension arvot luodaan ja myymälöiden taloushallinnon dimensioiden arvot määritetään.
author: jashanno
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0212d3bd808b2a46fa30e8b2bdaa3c0b52ca0dd6
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2021
ms.locfileid: "5790929"
---
# <a name="create-financial-dimensions-for-retail-channels-and-configure-dimension-values-on-stores"></a><span data-ttu-id="bfe74-103">Taloushallinnon dimensioiden luominen vähittäismyyntikanaville ja dimensioarvojen määrittäminen myymälöille</span><span class="sxs-lookup"><span data-stu-id="bfe74-103">Create financial dimensions for retail channels and configure dimension values on stores</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="bfe74-104">Tässä menetelmässä kerrotaan, miten kaupankäyntikanavan taloushallinnon dimensio ja dimension arvot luodaan ja myymälöiden taloushallinnon dimensioiden arvot määritetään.</span><span class="sxs-lookup"><span data-stu-id="bfe74-104">This procedure walks through creating a commerce channel financial dimension with dimension values and steps to configure financial dimension values on stores.</span></span> <span data-ttu-id="bfe74-105">Aihe ei sisällä muita liittyviä vaiheita, kuten dimensiojoukkojen ja tilirakenteiden luomista.</span><span class="sxs-lookup"><span data-stu-id="bfe74-105">The topic does not include other related steps, such as creating dimension sets and account structures.</span></span> <span data-ttu-id="bfe74-106">Menettely käyttää esittelytietojen USRT-yritystä.</span><span class="sxs-lookup"><span data-stu-id="bfe74-106">This procedure uses the USRT company in demo data.</span></span>

1. <span data-ttu-id="bfe74-107">Valitse Kirjanpito > Tilikartta > Dimensiot > Taloushallinnon dimensiot.</span><span class="sxs-lookup"><span data-stu-id="bfe74-107">Go to General ledger > Chart of accounts > Dimensions > Financial dimensions.</span></span>
2. <span data-ttu-id="bfe74-108">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="bfe74-108">Click New.</span></span>
3. <span data-ttu-id="bfe74-109">Valitse Käytä arvoja -kenttään Kaupankäyntikanavat.</span><span class="sxs-lookup"><span data-stu-id="bfe74-109">In the Use values from field, select 'Commerce channels'.</span></span>
4. <span data-ttu-id="bfe74-110">Kirjoita arvo Dimension nimi -kenttään.</span><span class="sxs-lookup"><span data-stu-id="bfe74-110">In the Dimension name field, type a value.</span></span>
5. <span data-ttu-id="bfe74-111">Valitse Aktivoi.</span><span class="sxs-lookup"><span data-stu-id="bfe74-111">Click Activate.</span></span>
6. <span data-ttu-id="bfe74-112">Valitse Sulje.</span><span class="sxs-lookup"><span data-stu-id="bfe74-112">Click Close.</span></span>
7. <span data-ttu-id="bfe74-113">Valitse Aktivoi.</span><span class="sxs-lookup"><span data-stu-id="bfe74-113">Click Activate.</span></span>
8. <span data-ttu-id="bfe74-114">Valitse Dimensioarvot.</span><span class="sxs-lookup"><span data-stu-id="bfe74-114">Click Dimension values.</span></span>
9. <span data-ttu-id="bfe74-115">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="bfe74-115">Close the page.</span></span>
10. <span data-ttu-id="bfe74-116">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="bfe74-116">Click Save.</span></span>
11. <span data-ttu-id="bfe74-117">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="bfe74-117">Close the page.</span></span>
12. <span data-ttu-id="bfe74-118">Valitse Retail ja Commerce > Kanavat > Myymälät > Kaikki myymälät.</span><span class="sxs-lookup"><span data-stu-id="bfe74-118">Go to Retail and Commerce > Channels > Stores > All stores.</span></span>
13. <span data-ttu-id="bfe74-119">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="bfe74-119">In the list, click the link in the selected row.</span></span>
14. <span data-ttu-id="bfe74-120">Ota käyttöön Taloushallinnon dimensiot -osan laajennus.</span><span class="sxs-lookup"><span data-stu-id="bfe74-120">Toggle the expansion of the Financial dimensions section.</span></span>
15. <span data-ttu-id="bfe74-121">Valitse Muokkaa.</span><span class="sxs-lookup"><span data-stu-id="bfe74-121">Click Edit.</span></span>
16. <span data-ttu-id="bfe74-122">Avaa haku napsauttamalla Kaupankäyntikanava-kentässä avattavan valikon painiketta.</span><span class="sxs-lookup"><span data-stu-id="bfe74-122">In the Commerce channel field, click the drop-down button to open the lookup.</span></span>
17. <span data-ttu-id="bfe74-123">Etsi ja valitse luettelosta päivitettävän myymälän dimension arvo.</span><span class="sxs-lookup"><span data-stu-id="bfe74-123">In the list, find and select the dimension value for the store being updated.</span></span>
18. <span data-ttu-id="bfe74-124">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="bfe74-124">In the list, click the link in the selected row.</span></span>
19. <span data-ttu-id="bfe74-125">Avaa haku valitsemalla CostCenter-kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="bfe74-125">In the CostCenter field, click the drop-down button to open the lookup.</span></span>
20. <span data-ttu-id="bfe74-126">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="bfe74-126">In the list, find and select the desired record.</span></span>
21. <span data-ttu-id="bfe74-127">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="bfe74-127">In the list, click the link in the selected row.</span></span>
22. <span data-ttu-id="bfe74-128">Avaa haku valitsemalla Osasto-kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="bfe74-128">In the Department field, click the drop-down button to open the lookup.</span></span>
23. <span data-ttu-id="bfe74-129">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="bfe74-129">In the list, find and select the desired record.</span></span>
24. <span data-ttu-id="bfe74-130">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="bfe74-130">In the list, click the link in the selected row.</span></span>
25. <span data-ttu-id="bfe74-131">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="bfe74-131">Click Save.</span></span>



[!INCLUDE[footer-include](../../includes/footer-banner.md)]