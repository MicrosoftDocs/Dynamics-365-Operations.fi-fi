---
title: Luo myyntipisteen taloushallinnon dimensiot kassakoneille ja määritä dimensioarvot kassakoneille
description: Tässä menettelyssä kerrotaan, miten myyntipisteen kassojen taloushallinnon dimensiot luodaan ja kassojen taloushallinnon arvot määritetään.
author: jashanno
manager: AnnBe
ms.date: 11/14/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4042fb9da0fe38de50ad7e0c8e64b98925ea1188
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5265956"
---
# <a name="create-financial-dimensions-for-pos-registers-and-configure-dimension-values-on-registers"></a><span data-ttu-id="b9a5a-103">Luo myyntipisteen taloushallinnon dimensiot kassakoneille ja määritä dimensioarvot kassakoneille</span><span class="sxs-lookup"><span data-stu-id="b9a5a-103">Create financial dimensions for POS registers and configure dimension values on registers</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b9a5a-104">Tässä menettelyssä kerrotaan, miten myyntipisteen kassojen taloushallinnon dimensiot luodaan ja kassojen taloushallinnon arvot määritetään.</span><span class="sxs-lookup"><span data-stu-id="b9a5a-104">This procedure walks through creating financial dimensions for point of sale (POS) registers, and demonstrates how to configure financial dimension values on registers.</span></span> <span data-ttu-id="b9a5a-105">Tämä menettely ei sisällä muita liittyviä vaiheita, kuten dimensiojoukkojen ja tilirakenteiden luomista.</span><span class="sxs-lookup"><span data-stu-id="b9a5a-105">This procedure doesn't include other related steps, such as creating dimension sets and account structures.</span></span> <span data-ttu-id="b9a5a-106">Nämä tehtävät löytyvät muista aiheista.</span><span class="sxs-lookup"><span data-stu-id="b9a5a-106">Those tasks can be found in other topics.</span></span> <span data-ttu-id="b9a5a-107">Tässä tallenteessa käytetään esittely-yritystä USRT.</span><span class="sxs-lookup"><span data-stu-id="b9a5a-107">This recording uses USRT demo company.</span></span>

1. <span data-ttu-id="b9a5a-108">Valitse Kirjanpito > Tilikartta > Dimensiot > Taloushallinnon dimensiot.</span><span class="sxs-lookup"><span data-stu-id="b9a5a-108">Go to General ledger > Chart of accounts > Dimensions > Financial dimensions.</span></span>
2. <span data-ttu-id="b9a5a-109">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="b9a5a-109">Click New.</span></span>
3. <span data-ttu-id="b9a5a-110">Valitse vaihtoehto Käytä arvoja kohteesta -kentässä.</span><span class="sxs-lookup"><span data-stu-id="b9a5a-110">In the Use values from field, select an option.</span></span>
4. <span data-ttu-id="b9a5a-111">Kirjoita arvo Dimension nimi -kenttään.</span><span class="sxs-lookup"><span data-stu-id="b9a5a-111">In the Dimension name field, type a value.</span></span>
5. <span data-ttu-id="b9a5a-112">Valitse Aktivoi.</span><span class="sxs-lookup"><span data-stu-id="b9a5a-112">Click Activate.</span></span>
6. <span data-ttu-id="b9a5a-113">Valitse Sulje.</span><span class="sxs-lookup"><span data-stu-id="b9a5a-113">Click Close.</span></span>
7. <span data-ttu-id="b9a5a-114">Valitse Aktivoi.</span><span class="sxs-lookup"><span data-stu-id="b9a5a-114">Click Activate.</span></span>
8. <span data-ttu-id="b9a5a-115">Valitse Dimensioarvot.</span><span class="sxs-lookup"><span data-stu-id="b9a5a-115">Click Dimension values.</span></span>
9. <span data-ttu-id="b9a5a-116">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="b9a5a-116">Close the page.</span></span>
10. <span data-ttu-id="b9a5a-117">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="b9a5a-117">Click Save.</span></span>
11. <span data-ttu-id="b9a5a-118">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="b9a5a-118">Close the page.</span></span>
12. <span data-ttu-id="b9a5a-119">Siirry kohtaan Retail ja Commerce > Kanavan asetukset > Myyntipisteen asetukset > Kassakoneet.</span><span class="sxs-lookup"><span data-stu-id="b9a5a-119">Go to Retail and Commerce > Channel setup > POS setup > Registers.</span></span>
13. <span data-ttu-id="b9a5a-120">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="b9a5a-120">In the list, find and select the desired record.</span></span>
14. <span data-ttu-id="b9a5a-121">Ota käyttöön Taloushallinnon dimensiot -osan laajennus.</span><span class="sxs-lookup"><span data-stu-id="b9a5a-121">Toggle the expansion of the Financial dimensions section.</span></span>
15. <span data-ttu-id="b9a5a-122">Valitse Muokkaa.</span><span class="sxs-lookup"><span data-stu-id="b9a5a-122">Click Edit.</span></span>
16. <span data-ttu-id="b9a5a-123">Avaa haku valitsemalla Pääte-kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="b9a5a-123">In the Terminal field, click the drop-down button to open the lookup.</span></span>
17. <span data-ttu-id="b9a5a-124">Etsi ja valitse luettelosta päivitettävän kassakoneen dimension arvo.</span><span class="sxs-lookup"><span data-stu-id="b9a5a-124">In the list, find and select the dimension value for the register being updated.</span></span>
18. <span data-ttu-id="b9a5a-125">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="b9a5a-125">Click Save.</span></span>



[!INCLUDE[footer-include](../../includes/footer-banner.md)]