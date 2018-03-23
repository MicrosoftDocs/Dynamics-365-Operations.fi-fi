--- 
title: "Luo myyntipisteen taloushallinnon dimensiot kassakoneille ja määritä dimensioarvot kassakoneille"
description: "Tässä menettelyssä kerrotaan, miten myyntipisteen kassojen taloushallinnon dimensiot luodaan ja kassojen taloushallinnon arvot määritetään."
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
ms.sourcegitcommit: ea07d8e91c94d9fdad4c2d05533981e254420188
ms.openlocfilehash: d2d34080409de25a3a1966d0898d0ecd98297891
ms.contentlocale: fi-fi
ms.lasthandoff: 02/07/2018

---
# <a name="create-financial-dimensions-for-pos-registers-and-configure-dimension-values-on-registers"></a><span data-ttu-id="0139f-103">Luo myyntipisteen taloushallinnon dimensiot kassakoneille ja määritä dimensioarvot kassakoneille</span><span class="sxs-lookup"><span data-stu-id="0139f-103">Create financial dimensions for POS registers and configure dimension values on registers</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="0139f-104">Tässä menettelyssä kerrotaan, miten myyntipisteen kassojen taloushallinnon dimensiot luodaan ja kassojen taloushallinnon arvot määritetään.</span><span class="sxs-lookup"><span data-stu-id="0139f-104">This procedure walks through creating financial dimensions for point of sale (POS) registers, and demonstrates how to configure financial dimension values on registers.</span></span> <span data-ttu-id="0139f-105">Tämä menettely ei sisällä muita liittyviä vaiheita, kuten dimensiojoukkojen ja tilirakenteiden luomista.</span><span class="sxs-lookup"><span data-stu-id="0139f-105">This procedure doesn’t include other related steps, such as creating dimension sets and account structures.</span></span> <span data-ttu-id="0139f-106">Nämä tehtävät löytyvät muista aiheista.</span><span class="sxs-lookup"><span data-stu-id="0139f-106">Those tasks can be found in other topics.</span></span> <span data-ttu-id="0139f-107">Tässä tallenteessa käytetään esittely-yritystä USRT.</span><span class="sxs-lookup"><span data-stu-id="0139f-107">This recording uses USRT demo company.</span></span>

1. <span data-ttu-id="0139f-108">Valitse Kirjanpito > Tilikartta > Dimensiot > Taloushallinnon dimensiot.</span><span class="sxs-lookup"><span data-stu-id="0139f-108">Go to General ledger > Chart of accounts > Dimensions > Financial dimensions.</span></span>
2. <span data-ttu-id="0139f-109">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="0139f-109">Click New.</span></span>
3. <span data-ttu-id="0139f-110">Valitse vaihtoehto Käytä arvoja kohteesta -kentässä.</span><span class="sxs-lookup"><span data-stu-id="0139f-110">In the Use values from field, select an option.</span></span>
4. <span data-ttu-id="0139f-111">Kirjoita arvo Dimension nimi -kenttään.</span><span class="sxs-lookup"><span data-stu-id="0139f-111">In the Dimension name field, type a value.</span></span>
5. <span data-ttu-id="0139f-112">Valitse Aktivoi.</span><span class="sxs-lookup"><span data-stu-id="0139f-112">Click Activate.</span></span>
6. <span data-ttu-id="0139f-113">Valitse Sulje.</span><span class="sxs-lookup"><span data-stu-id="0139f-113">Click Close.</span></span>
7. <span data-ttu-id="0139f-114">Valitse Aktivoi.</span><span class="sxs-lookup"><span data-stu-id="0139f-114">Click Activate.</span></span>
8. <span data-ttu-id="0139f-115">Valitse Dimensioarvot.</span><span class="sxs-lookup"><span data-stu-id="0139f-115">Click Dimension values.</span></span>
9. <span data-ttu-id="0139f-116">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="0139f-116">Close the page.</span></span>
10. <span data-ttu-id="0139f-117">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="0139f-117">Click Save.</span></span>
11. <span data-ttu-id="0139f-118">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="0139f-118">Close the page.</span></span>
12. <span data-ttu-id="0139f-119">Siirry kohtaan Vähittäismyynti ja kauppa > Kanavan asetukset > Myyntipisteen asetukset > Kassakoneet.</span><span class="sxs-lookup"><span data-stu-id="0139f-119">Go to Retail and commerce > Channel setup > POS setup > Registers.</span></span>
13. <span data-ttu-id="0139f-120">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="0139f-120">In the list, find and select the desired record.</span></span>
14. <span data-ttu-id="0139f-121">Ota käyttöön Taloushallinnon dimensiot -osan laajennus.</span><span class="sxs-lookup"><span data-stu-id="0139f-121">Toggle the expansion of the Financial dimensions section.</span></span>
15. <span data-ttu-id="0139f-122">Valitse Muokkaa.</span><span class="sxs-lookup"><span data-stu-id="0139f-122">Click Edit.</span></span>
16. <span data-ttu-id="0139f-123">Avaa haku valitsemalla Pääte-kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="0139f-123">In the Terminal field, click the drop-down button to open the lookup.</span></span>
17. <span data-ttu-id="0139f-124">Etsi ja valitse luettelosta päivitettävän kassakoneen dimension arvo.</span><span class="sxs-lookup"><span data-stu-id="0139f-124">In the list, find and select the dimension value for the register being updated.</span></span>
18. <span data-ttu-id="0139f-125">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="0139f-125">Click Save.</span></span>


