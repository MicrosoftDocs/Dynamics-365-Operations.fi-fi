---
title: Kustannustasodimension jäsenten yhdistäminen yhteiseen dimension jäsenten joukkoon
description: Yhdistämällä eri kustannustason dimension jäsenet joukoksi kustannustason dimensiojäsenet yhdistät tiedot yleiseen muotoon analyysitarkoituksiin.
author: AndersGirke
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CAMDimension, CAMDimensionMember
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 223234
ms.assetid: 4c66a231-aed2-48b5-9727-b3eb4fe6e6aa
ms.search.region: global
ms.author: shylaw
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: deb9b5aab9cd69270c78d4e1ea0e2a6cac6ac370
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/01/2019
ms.locfileid: "1841510"
---
# <a name="map-cost-element-dimension-members-to-a-common-set-of-dimension-members"></a><span data-ttu-id="e3f07-103">Kustannustasodimension jäsenten yhdistäminen yhteiseen dimension jäsenten joukkoon</span><span class="sxs-lookup"><span data-stu-id="e3f07-103">Map cost element dimension members to a common set of dimension members</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e3f07-104">Yhdistämällä eri kustannustason dimension jäsenet joukoksi kustannustason dimensiojäsenet yhdistät tiedot yleiseen muotoon analyysitarkoituksiin.</span><span class="sxs-lookup"><span data-stu-id="e3f07-104">By mapping different cost element dimension members to a common set of cost element dimension members, you merge data into a common format for analysis purposes.</span></span>

<span data-ttu-id="e3f07-105">Maailmanlaajuisilla yrityksillä, jotka noudattavat lakisääteisiä vaatimuksia, voi olla useita tilikarttoja käytössä.</span><span class="sxs-lookup"><span data-stu-id="e3f07-105">If you're a global company and comply with statutory accounting requirements, you might use multiple charts of accounts.</span></span> <span data-ttu-id="e3f07-106">Kun kustannustason dimension jäsenet tuodaan eri tilikartoista, lopputuloksena voi olla sekalainen tilijoukko.</span><span class="sxs-lookup"><span data-stu-id="e3f07-106">When you import cost element dimension members from different charts of accounts, you can end up with a mix of accounts.</span></span> <span data-ttu-id="e3f07-107">Tilit saattavat todellisuudessa olla samantyyppisiä, ja niiden kustannukset halutaan kohdistaa ja analysoida yhteisen muodon mukaisesti.</span><span class="sxs-lookup"><span data-stu-id="e3f07-107">However, these accounts might actually have the same nature, and you might want to analyze and allocate costs for them by using a common format.</span></span>

## <a name="map-cost-element-dimension-members-to-a-common-format"></a><span data-ttu-id="e3f07-108">Kustannustason dimension jäsenten yhdistäminen yhteisen muodon mukaan</span><span class="sxs-lookup"><span data-stu-id="e3f07-108">Map cost element dimension members to a common format</span></span>
<span data-ttu-id="e3f07-109">Seuraavassa esimerkissä esitetään, kuinka kustannusten vastuuhenkilö voi luoda uuden kustannustason dimension kustannuslaskentaan, joka yhdistää kustannustason dimension jäsenet Yhdysvaltojen tilikartan rakenteesta ja Ranskan tilikartan rakenteesta kustannustason dimension jäsenten yhteiseksi joukoksi.</span><span class="sxs-lookup"><span data-stu-id="e3f07-109">The following example shows how you, as a cost controller, can create a new cost element dimension in Cost accounting that maps cost element dimension members from the US chart of accounts structure and the French chart of accounts structure to a common set of cost element dimension members.</span></span> <span data-ttu-id="e3f07-110">Kustannustason dimension jäsenten yhteistä joukkoa voidaan käyttää analysoitaessa kustannusten tietoja kahdesta yrityksestä kustannuslaskennan kirjanpidossa.</span><span class="sxs-lookup"><span data-stu-id="e3f07-110">You can then use the common set of cost element dimension members to analyze cost data from the two legal entities in a cost accounting ledger.</span></span>

| <span data-ttu-id="e3f07-111">Lähde: US Tilikartta</span><span class="sxs-lookup"><span data-stu-id="e3f07-111">Source: US chart of accounts</span></span>                                          | <span data-ttu-id="e3f07-112">Lähde: Ranska tilikartta</span><span class="sxs-lookup"><span data-stu-id="e3f07-112">Source: French chart of accounts</span></span>                                          | <span data-ttu-id="e3f07-113">Uusi kustannustason dimension jäsenten joukko</span><span class="sxs-lookup"><span data-stu-id="e3f07-113">New common set of cost element dimension members</span></span>                        |
|-----------------------------------------------------------------------|---------------------------------------------------------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="e3f07-114">Yhdysvaltojen tilikartasta tuodut kustannustason dimensiojäsenet</span><span class="sxs-lookup"><span data-stu-id="e3f07-114">Imported cost element dimension members from the US chart of accounts</span></span> | <span data-ttu-id="e3f07-115">Ranskan tilikartasta tuodut kustannustason dimensiojäsenet</span><span class="sxs-lookup"><span data-stu-id="e3f07-115">Imported cost element dimension members from the French chart of accounts</span></span> | <span data-ttu-id="e3f07-116">Yhdysvallan ja Ranskan yhdistetty kustannustason dimension jäsenten joukko</span><span class="sxs-lookup"><span data-stu-id="e3f07-116">Mapping of US and French cost element dimension members to a common set</span></span> |
| <span data-ttu-id="e3f07-117">5001: Myynti</span><span class="sxs-lookup"><span data-stu-id="e3f07-117">5001: Sales</span></span>                                                           | <span data-ttu-id="e3f07-118">5001: Myynti ja mainonta</span><span class="sxs-lookup"><span data-stu-id="e3f07-118">5001: Sales and advertising</span></span>                                               | <span data-ttu-id="e3f07-119">5000: Myynti ja mainonta</span><span class="sxs-lookup"><span data-stu-id="e3f07-119">5000: Sales and advertising</span></span>                                             |
| <span data-ttu-id="e3f07-120">5030: Mainonta</span><span class="sxs-lookup"><span data-stu-id="e3f07-120">5030: Advertising</span></span>                                                     | <span data-ttu-id="e3f07-121">6390: Varasto-ostot\*</span><span class="sxs-lookup"><span data-stu-id="e3f07-121">6390: Stock purchase\*</span></span>                                                    | <span data-ttu-id="e3f07-122">7000: puhtaanapitokulut</span><span class="sxs-lookup"><span data-stu-id="e3f07-122">7000: Cleaning expenses</span></span>                                                 |
| <span data-ttu-id="e3f07-123">7001: puhtaanapitokulut</span><span class="sxs-lookup"><span data-stu-id="e3f07-123">7001: Cleaning expenses</span></span>                                               | <span data-ttu-id="e3f07-124">7001: Matkakulut</span><span class="sxs-lookup"><span data-stu-id="e3f07-124">7001: Travel expense</span></span>                                                      | <span data-ttu-id="e3f07-125">7001: Matkakulut</span><span class="sxs-lookup"><span data-stu-id="e3f07-125">7001: Travel expenses</span></span>                                                   |

<span data-ttu-id="e3f07-126">\* Varaston ostotilauksen kustannus Ranskan kustannustason dimension jäsenellä ei ole määritetty.</span><span class="sxs-lookup"><span data-stu-id="e3f07-126">\*The Stock purchase French cost element dimension member isn't mapped.</span></span>

## <a name="currency-conversion"></a><span data-ttu-id="e3f07-127">Valuuttamuunnos</span><span class="sxs-lookup"><span data-stu-id="e3f07-127">Currency conversion</span></span>
<span data-ttu-id="e3f07-128">Eri tilikartat,, joita käytetään, voivat määrittää eri valuuttoja.</span><span class="sxs-lookup"><span data-stu-id="e3f07-128">The various charts of accounts that you use might be set up to use different currencies.</span></span> <span data-ttu-id="e3f07-129">Tässä tapauksessa muista määrittää valuuttamuunnoksen, jolloin kustannustiedot käsitellään oikeassa valuutassa,määritetyn kustannuslaskennan kirjanpidon mukaan jossa käytetään kustannustason dimensiojäsenet.</span><span class="sxs-lookup"><span data-stu-id="e3f07-129">In this case, be sure to specify a currency conversion, so that cost data is processed by using the correct currency, as defined in the cost accounting ledger where the cost element dimension members are used.</span></span> <span data-ttu-id="e3f07-130">Edellisessä esimerkissä, jos käytettyinä Yhdysvaltain dollarin (USD) kustannuslaskennan kirjanpitoon, sinun on luotava valuutan muuntaminen USD-euro (EUR) tapahtumien käsittelyyn yhdistetyille kustannustason dimensiojäsenet.</span><span class="sxs-lookup"><span data-stu-id="e3f07-130">In the preceding example, if US dollars (USD) are used in the cost accounting ledger, you must create a currency conversion from USD to euros (EUR) to process transactions for the mapped cost element dimension members.</span></span>

## <a name="update-mappings-at-any-time"></a><span data-ttu-id="e3f07-131">Päivitä yhdistämiset koska tahansa</span><span class="sxs-lookup"><span data-stu-id="e3f07-131">Update mappings at any time</span></span>
<span data-ttu-id="e3f07-132">Voit päivittää yhdistetyt kustannustason dimension määritykset milloin tahansa.</span><span class="sxs-lookup"><span data-stu-id="e3f07-132">You can update the mapping definitions for a cost element dimension at any time.</span></span> <span data-ttu-id="e3f07-133">Määritykset eivät ole päivämääräpohjaisia, koska muutokset vaikuttavat seuraavan kerran, kun käsittelet kustannustapahtumat tai suorittaa kustannuslaskelman.</span><span class="sxs-lookup"><span data-stu-id="e3f07-133">Because mappings aren't date-effective, changes are applied the next time that you process cost transactions or run cost calculations.</span></span>



