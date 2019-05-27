---
title: Määritä kanta-asiakkaan palkkiopisteet
description: Tässä menettelyssä esitellään kanta-asiakkaan palkkiopisteiden määrittäminen.
author: scott-tucker
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailLoyaltyRewardPoints
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: scotttuc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 85ae26123d41fa74d32b102ddb7f021e9846a676
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/15/2019
ms.locfileid: "1564313"
---
# <a name="define-loyalty-reward-points"></a><span data-ttu-id="c62f9-103">Määritä kanta-asiakkaan palkkiopisteet</span><span class="sxs-lookup"><span data-stu-id="c62f9-103">Define loyalty reward points</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="c62f9-104">Tässä menettelyssä esitellään kanta-asiakkaan palkkiopisteiden määrittäminen.</span><span class="sxs-lookup"><span data-stu-id="c62f9-104">This procedure walks through defining loyalty reward points.</span></span> <span data-ttu-id="c62f9-105">Määritä kanta-asiakkaan palkkiopisteet ennen kanta-asiakkuusohjelman määrittämistä.</span><span class="sxs-lookup"><span data-stu-id="c62f9-105">You should set up loyalty reward points before you set up a loyalty program.</span></span> <span data-ttu-id="c62f9-106">Menettely käyttää esittelytietojen USRT-yritystä.</span><span class="sxs-lookup"><span data-stu-id="c62f9-106">This procedure uses the USRT demo data company.</span></span>

1. <span data-ttu-id="c62f9-107">Siirry kohtaan Vähittäismyynti ja kauppa > Asiakkaat> Kanta-asiakkaat> Kanta-asiakkaan palkkiopisteet.</span><span class="sxs-lookup"><span data-stu-id="c62f9-107">Go to Retail and commerce > Customers > Loyalty > Loyalty reward points.</span></span>
2. <span data-ttu-id="c62f9-108">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="c62f9-108">Click New.</span></span>
3. <span data-ttu-id="c62f9-109">Syötä Palkkiopisteen tunnus -kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="c62f9-109">In the Reward point ID field, type a value.</span></span>
4. <span data-ttu-id="c62f9-110">Kirjoita arvo Kuvaus-kenttään.</span><span class="sxs-lookup"><span data-stu-id="c62f9-110">In the Description field, type a value.</span></span>
5. <span data-ttu-id="c62f9-111">Valitse Palkkiopisteen tyyppi -kentässä vaihtoehto.</span><span class="sxs-lookup"><span data-stu-id="c62f9-111">In the Reward point type field, select an option.</span></span>
    * <span data-ttu-id="c62f9-112">Valitse määrä, jos haluat pyöristää palkkiopisteet seuraavaan kokonaislukuun.</span><span class="sxs-lookup"><span data-stu-id="c62f9-112">Select Quantity if you want the reward points to be rounded to the nearest integer.</span></span> <span data-ttu-id="c62f9-113">Valitse Summa, jos haluat pyöristää palkkiopisteet valuutan pyöristyssääntöjen mukaan.</span><span class="sxs-lookup"><span data-stu-id="c62f9-113">Select Amount if you want the reward points to be rounded according to currency rounding rules.</span></span> <span data-ttu-id="c62f9-114">Jos valitse Määrä, ohita menettelyn seuraava vaihe.</span><span class="sxs-lookup"><span data-stu-id="c62f9-114">If you select Quantity, skip the next step of this procedure..</span></span>  
6. <span data-ttu-id="c62f9-115">Kirjoita arvo Valuutta-kenttään.</span><span class="sxs-lookup"><span data-stu-id="c62f9-115">In the Currency field, type a value.</span></span>
    * <span data-ttu-id="c62f9-116">Jos palkkiopisteiden tyyppi on Summa, myönnetyille pisteille määritetään valittu valuutta.</span><span class="sxs-lookup"><span data-stu-id="c62f9-116">For Amount type reward points, all points issued will have the selected currency.</span></span> <span data-ttu-id="c62f9-117">Jos palkkiopisteiden tyyppi on Määrä, tämä kenttä ei ole käytössä. Voit ohittaa tämän vaiheen.</span><span class="sxs-lookup"><span data-stu-id="c62f9-117">For Quantity type reward points, this field doesn't apply—skip this step.</span></span>  
7. <span data-ttu-id="c62f9-118">Valitse Lunastettavissa-valintaruutu tai poista sen valinta.</span><span class="sxs-lookup"><span data-stu-id="c62f9-118">Check or uncheck the Redeemable checkbox.</span></span>
8. <span data-ttu-id="c62f9-119">Syötä Lunasta sijoitus -kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="c62f9-119">In the Redeem ranking field, enter a number.</span></span>
    * <span data-ttu-id="c62f9-120">Lunasta sijoitus -kohtaa käytetään, kun tuotteiden maksamisessa voidaan käyttää kahta tai useampaa lunastettavaa palkkiopistettä.</span><span class="sxs-lookup"><span data-stu-id="c62f9-120">Redeem ranking is used when two or more redeemable reward points can be used to pay for products.</span></span> <span data-ttu-id="c62f9-121">Jos kahdella palkkiopisteellä on sama lunastusluokittelu, käytetään sitä, jonka pisteiden määrää tulee vähentää.</span><span class="sxs-lookup"><span data-stu-id="c62f9-121">If the two reward points have the same redeem ranking, then the one that needs to lower number of points will be used.</span></span>  
9. <span data-ttu-id="c62f9-122">Syötä Vanhentumisajan arvo -kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="c62f9-122">In the Expiration time value field, enter a number.</span></span>
    * <span data-ttu-id="c62f9-123">Palkkiopisteet vanhenevat määritettyjen päivien, kuukausien tai vuosien kuluttua siitä, kun pisteet on myönnetty.</span><span class="sxs-lookup"><span data-stu-id="c62f9-123">The reward points will expire the specified number of days, months, or years after when the points are issued.</span></span> <span data-ttu-id="c62f9-124">Arvo 0 tarkoittaa, että kanta-asiakkaan palkkiopisteet eivät vanhene koskaan.</span><span class="sxs-lookup"><span data-stu-id="c62f9-124">A value of ‘0’ means the loyalty reward points will never expire.</span></span>  
10. <span data-ttu-id="c62f9-125">Valitse Vanhentumisajan yksikkö -kenttään vaihtoehto.</span><span class="sxs-lookup"><span data-stu-id="c62f9-125">In the Expiration time unit field, select an option.</span></span>
11. <span data-ttu-id="c62f9-126">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="c62f9-126">Click Save.</span></span>

