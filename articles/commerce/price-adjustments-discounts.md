---
title: Hinnanoikaisut ja alennukset
description: Tässä artikkelissa on tietoja Dynamics 365 Commercein hinnanoikaisuista ja alennuksista.
author: scott-tucker
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailParameters, RetailPeriodicDiscount
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 15891
ms.assetid: bab5adf3-ddf0-4c22-a2eb-b4d25b88de99
ms.search.region: global
ms.search.industry: Retail
ms.author: scotttuc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: dfaacfa7681258e3b2273083017c0c398d566651
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/01/2020
ms.locfileid: "3022438"
---
# <a name="price-adjustments-and-discounts"></a><span data-ttu-id="9df7a-103">Hinnanoikaisut ja alennukset</span><span class="sxs-lookup"><span data-stu-id="9df7a-103">Price adjustments and discounts</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="9df7a-104">Tässä artikkelissa on tietoja Dynamics 365 Commercein hinnanoikaisuista ja alennuksista.</span><span class="sxs-lookup"><span data-stu-id="9df7a-104">This article provides information about price adjustments and discounts in Dynamics 365 Commerce.</span></span>

<span data-ttu-id="9df7a-105">Voit tehdä Commercessa tuotteiden hinnanoikaisuja ja myös määrittää alennuksia, joita käytetään nimikkeeseen tai tapahtumaan myyntipisteessä, puhelinkeskuksen myyntitilauksessa tai verkkotilauksessa.</span><span class="sxs-lookup"><span data-stu-id="9df7a-105">In Commerce, you can make price adjustments to products, and can also set up discounts that are applied to a line item or a transaction at the point of sale (POS), in a call center sales order, or in an online order.</span></span> <span data-ttu-id="9df7a-106">Sekä hinnanoikaisut että alennukset voidaan linkittää hintaryhmiin.</span><span class="sxs-lookup"><span data-stu-id="9df7a-106">Both price adjustments and discounts can be linked to price groups.</span></span> <span data-ttu-id="9df7a-107">Hinnanoikaisuille ja alennuksille voidaan määrittää yksi aloitus- ja päättymispäivämäärä tai toistuva jakso, alennuskoodi ja joitakin muita määritteitä.</span><span class="sxs-lookup"><span data-stu-id="9df7a-107">For both price adjustments and discounts, you can specify a single start date and end date or a reoccurring period, a discount code, and a few additional attributes.</span></span> 

<span data-ttu-id="9df7a-108">Hinnanoikaisuja ja alennuksia voidaan käyttää tuotteissa, varianteissa tai kategorioissa.</span><span class="sxs-lookup"><span data-stu-id="9df7a-108">Price adjustments and discounts can be applied to products, variants, or categories.</span></span> <span data-ttu-id="9df7a-109">Jos tuotteelle on useita alennuksia, asiakas voi saada minkä tahansa alennuksen tai alennusten yhdistelmän alennuksen määritysten mukaisesti.</span><span class="sxs-lookup"><span data-stu-id="9df7a-109">If more than one discount applies to a product, a customer might receive either one of the discounts or a combined discount, depending on the configuration of the discount.</span></span> <span data-ttu-id="9df7a-110">Commerce käyttää automaattisesti alennusta tai alennusten yhdistelmää, joka takaa asiakkaalle parhaan hinnan.</span><span class="sxs-lookup"><span data-stu-id="9df7a-110">Commerce automatically applies the discount or combination of discounts that gives the best price to the customer.</span></span> <span data-ttu-id="9df7a-111">Kun määrität hinnanoikaisua tai alennusta, muista vahvistaa, että hintaryhmät on liitetty oikeisiin kanaviin, luetteloihin, liitoksiin tai kanta-asiakasohjelmiin, joissa haluat käyttää alennusta.</span><span class="sxs-lookup"><span data-stu-id="9df7a-111">When you set up a price adjustment or a discount, be sure to confirm that price groups are assigned to the correct channels, catalogs, affiliations, or loyalty programs that you want the discount to apply to.</span></span> <span data-ttu-id="9df7a-112">Lisäksi jos haluat luoda alennustunnuksen automaattisesti, määritä numerosarjat **Commercen parametrit** -sivulla, ennen kuin määrität uuden hinnanoikaisun tai alennuksen.</span><span class="sxs-lookup"><span data-stu-id="9df7a-112">Additionally, if you want to automatically generate the discount ID, set up number sequences on the **Commerce parameters** page before you define a new price adjustment or discount.</span></span>

> [!NOTE]
> <span data-ttu-id="9df7a-113">Voit poistaa hinnanoikaisun tai alennuksen.</span><span class="sxs-lookup"><span data-stu-id="9df7a-113">You can delete a price adjustment or a discount.</span></span> <span data-ttu-id="9df7a-114">Tällöin tilastotiedot kuitenkin häviävät.</span><span class="sxs-lookup"><span data-stu-id="9df7a-114">However, statistical information will be lost.</span></span>

## <a name="types-of-discounts"></a><span data-ttu-id="9df7a-115">Alennusten tyypit</span><span class="sxs-lookup"><span data-stu-id="9df7a-115">Types of discounts</span></span>

<span data-ttu-id="9df7a-116">Alennuksia on neljää tyyppiä:</span><span class="sxs-lookup"><span data-stu-id="9df7a-116">There are four types of discounts:</span></span>

- <span data-ttu-id="9df7a-117">**Yksinkertainen alennus** – Yksi prosenttiosuus tai määrä.</span><span class="sxs-lookup"><span data-stu-id="9df7a-117">**Simple discount** – A single percentage or amount.</span></span>
- <span data-ttu-id="9df7a-118">**Määräalennus** – alennus, jota käytetään, kun tuotteita ostetaan vähintään kaksi.</span><span class="sxs-lookup"><span data-stu-id="9df7a-118">**Quantity discount** – A discount that is applied when two or more products are purchased.</span></span>
- <span data-ttu-id="9df7a-119">**Yhdistelmäalennus** – alennus, jota käytetään, kun ostetaan tietty tuoteyhdistelmä.</span><span class="sxs-lookup"><span data-stu-id="9df7a-119">**Mix and match discount** – A discount that is applied when a specific combination of products is purchased.</span></span>
- <span data-ttu-id="9df7a-120">**Raja-arvon alennus** – alennus, jota käytetään, kun tapahtuman kokonaissumma ylittää tietyn summan.</span><span class="sxs-lookup"><span data-stu-id="9df7a-120">**Threshold discount** – A discount that is applied when the transaction total is more than a specified amount.</span></span>

<span data-ttu-id="9df7a-121">Sekä hinnanoikaisut että alennukset voidaan yhdistää hintaryhmiin.</span><span class="sxs-lookup"><span data-stu-id="9df7a-121">Both price adjustments and discounts can be associated with price groups.</span></span> <span data-ttu-id="9df7a-122">Hintaryhmät voidaan tämän jälkeen liittää kanaviin, luetteloihin, liitoksiin ja kanta-asiakasohjelmiin.</span><span class="sxs-lookup"><span data-stu-id="9df7a-122">Price groups can then be associated with channels, catalogs, affiliations, and loyalty programs.</span></span>