---
title: Poistomenetelmät ja -käytännöt
description: Tämä artikkeli sisältää yleiskuvauksen Microsoft Dynamics 365 Financen tukemista poistokäytännöistä ja poistomenetelmistä.
author: ShylaThompson
ms.date: 04/25/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetDepreciationProfile, AssetGroupBookSetup, AssetGroupDepBookSetup
audience: Application User
ms.reviewer: roschlom
ms.custom: 3441
ms.assetid: 1d8267b1-86a8-44bf-8814-f56b5d45a0ae
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 76b20c895519edb7316c2b9a6b223a109a307e77
ms.sourcegitcommit: ff09736563d3cd2bc74c7664edd1767b218401cb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/04/2021
ms.locfileid: "6189394"
---
# <a name="depreciation-methods-and-conventions"></a><span data-ttu-id="59b91-103">Poistomenetelmät ja -käytännöt</span><span class="sxs-lookup"><span data-stu-id="59b91-103">Depreciation methods and conventions</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="59b91-104">Tämä artikkeli sisältää yleiskuvauksen tuetuista poistokäytännöistä ja poistomenetelmistä.</span><span class="sxs-lookup"><span data-stu-id="59b91-104">This article provides an overview of the supported depreciation conventions and depreciation methods.</span></span>

<span data-ttu-id="59b91-105">Voit valita useita poistomenetelmiä.</span><span class="sxs-lookup"><span data-stu-id="59b91-105">You can select various depreciation methods and conventions.</span></span> <span data-ttu-id="59b91-106">Menetelmien tarkoituksena on kohdistaa käyttöomaisuuserän poistokelpoinen arvo tilikausille.</span><span class="sxs-lookup"><span data-stu-id="59b91-106">The purpose of the methods is to allocate the depreciable value of the fixed asset into fiscal periods.</span></span> <span data-ttu-id="59b91-107">Käyttöomaisuuserän poistokelpoinen arvo on hankintahinta vähennettynä mahdollisella jäännösarvolla.</span><span class="sxs-lookup"><span data-stu-id="59b91-107">The depreciable value of the fixed asset is the acquisition price, reduced by a scrap value, if any.</span></span> 

<span data-ttu-id="59b91-108">Jos käytät poistomenetelmiä ja muutat käyttöomaisuuserän viimeisen poiston suorituspäivää, jolloin jotkin poistot jäävät väliin, viimeisen vuoden poisto voi olla odotettua suurempi tai pienempi.</span><span class="sxs-lookup"><span data-stu-id="59b91-108">If you are using depreciation conventions and you modify the last depreciation run date for an asset, which then causes some depreciations to be skipped, the depreciation for the last year might be more than or less than is expected.</span></span> <span data-ttu-id="59b91-109">Poistoa muutetaan niiden poistokausien määrällä, joihin viimeisen poistokerran päivämäärän muuttaminen vaikuttaa</span><span class="sxs-lookup"><span data-stu-id="59b91-109">The depreciation is adjusted by the number of depreciation periods affected by the modification of the last depreciation run date.</span></span>

<span data-ttu-id="59b91-110">Jos esimerkiksi käytät puolivuosittaista poistomenetelmää kolmen vuoden ajan, poistot tehdään yleensä 3,5 vuoden aikana.</span><span class="sxs-lookup"><span data-stu-id="59b91-110">For example, if you are using the Half year depreciation convention over three years, depreciation ordinarily occurs over 3 1/2 years.</span></span> <span data-ttu-id="59b91-111">Jos muutat viimeisen poiston suorituspäivää tämän 3 1/2 vuoden kuluessa, viimeinen poistovuosi siirtää niiden kausien määrää, joihin muutos vaikuttaa.</span><span class="sxs-lookup"><span data-stu-id="59b91-111">If you change the last depreciation run date during the 3 1/2 years, the last year of depreciation moves out the number of periods affected.</span></span> <span data-ttu-id="59b91-112">Jos siirrät päivämäärää kolmella kuukaudella, viimeisessä vuodessa on yhdeksän kuukautta poistettavaa, kun tavallisesti siinä olisi kuusi kuukautta poistettavaa.</span><span class="sxs-lookup"><span data-stu-id="59b91-112">If you move the date by three months, the last year will have nine months’ worth of depreciation, when ordinarily there would be six months’ worth of depreciation.</span></span>

<span data-ttu-id="59b91-113">Voit valita jonkin seuraavista poistomenetelmistä.</span><span class="sxs-lookup"><span data-stu-id="59b91-113">You can select from the following depreciation conventions.</span></span>


-   <span data-ttu-id="59b91-114">Puolivuosi</span><span class="sxs-lookup"><span data-stu-id="59b91-114">Half year</span></span>
-   <span data-ttu-id="59b91-115">Täysi kuukausi</span><span class="sxs-lookup"><span data-stu-id="59b91-115">Full month</span></span>
-   <span data-ttu-id="59b91-116">Vuosineljänneksen puoliväli</span><span class="sxs-lookup"><span data-stu-id="59b91-116">Mid quarter</span></span>
-   <span data-ttu-id="59b91-117">Kuukauden puoliväli (kuukauden 1. päivä)</span><span class="sxs-lookup"><span data-stu-id="59b91-117">Mid month (1st of month)</span></span>
-   <span data-ttu-id="59b91-118">Kuukauden puoliväli (kuukauden 15. päivä)</span><span class="sxs-lookup"><span data-stu-id="59b91-118">Mid month (15th of month)</span></span>
-   <span data-ttu-id="59b91-119">Puolivuosi (vuoden alku)</span><span class="sxs-lookup"><span data-stu-id="59b91-119">Half year (start of year)</span></span>
-   <span data-ttu-id="59b91-120">Puolivuosi (seuraava vuosi)</span><span class="sxs-lookup"><span data-stu-id="59b91-120">Half year (next year)</span></span>

<span data-ttu-id="59b91-121">Voit valita seuraavista poistomenetelmistä.</span><span class="sxs-lookup"><span data-stu-id="59b91-121">You can select from the following depreciation methods.</span></span>
-   <span data-ttu-id="59b91-122">Tasapoisto - käyttöaika</span><span class="sxs-lookup"><span data-stu-id="59b91-122">Straight line service life</span></span>
-   <span data-ttu-id="59b91-123">Jäännösarvopoisto</span><span class="sxs-lookup"><span data-stu-id="59b91-123">Reducing balance</span></span>
-   <span data-ttu-id="59b91-124">Manuaalinen</span><span class="sxs-lookup"><span data-stu-id="59b91-124">Manual</span></span>
-   <span data-ttu-id="59b91-125">Kerroin</span><span class="sxs-lookup"><span data-stu-id="59b91-125">Factor</span></span>
-   <span data-ttu-id="59b91-126">Kulutus</span><span class="sxs-lookup"><span data-stu-id="59b91-126">Consumption</span></span>
-   <span data-ttu-id="59b91-127">Tasapoisto - jäljellä oleva käyttöaika</span><span class="sxs-lookup"><span data-stu-id="59b91-127">Straight line life remaining</span></span>
-   <span data-ttu-id="59b91-128">Jäännös 200 %</span><span class="sxs-lookup"><span data-stu-id="59b91-128">200% reducing balance</span></span>
-   <span data-ttu-id="59b91-129">Jäännös 175 %</span><span class="sxs-lookup"><span data-stu-id="59b91-129">175% reducing balance</span></span>
-   <span data-ttu-id="59b91-130">Jäännös 150 %</span><span class="sxs-lookup"><span data-stu-id="59b91-130">150% reducing balance</span></span>
-   <span data-ttu-id="59b91-131">Jäännös 125 %</span><span class="sxs-lookup"><span data-stu-id="59b91-131">125% reducing balance</span></span>





## <a name="additional-resources"></a><span data-ttu-id="59b91-132">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="59b91-132">Additional resources</span></span>

[<span data-ttu-id="59b91-133">Käyttöomaisuuden poisto</span><span class="sxs-lookup"><span data-stu-id="59b91-133">Fixed asset depreciation</span></span>](fixed-asset-depreciation.md)

[<span data-ttu-id="59b91-134">Käyttöikään perustuva tasapoisto</span><span class="sxs-lookup"><span data-stu-id="59b91-134">Straight line service life depreciation</span></span>](Straight-line-service-life-depreciation.md)

[<span data-ttu-id="59b91-135">Jäännöspoisto</span><span class="sxs-lookup"><span data-stu-id="59b91-135">Reduce balance depreciation</span></span>](reduce-balance-depreciation.md)

[<span data-ttu-id="59b91-136">Manuaalinen poisto</span><span class="sxs-lookup"><span data-stu-id="59b91-136">Manual depreciation</span></span>](manual-depreciation.md)

[<span data-ttu-id="59b91-137">Kerroinpoisto</span><span class="sxs-lookup"><span data-stu-id="59b91-137">Factor depreciation</span></span>](factor-depreciation.md)

[<span data-ttu-id="59b91-138">Kulutuspoisto</span><span class="sxs-lookup"><span data-stu-id="59b91-138">Consumption depreciation</span></span>](consumption-depreciation.md)

[<span data-ttu-id="59b91-139">Jäljellä olevan käyttöajan tasapoisto</span><span class="sxs-lookup"><span data-stu-id="59b91-139">Straight line life remaining depreciation</span></span>](straight-line-life-remaining-depreciation.md)

[<span data-ttu-id="59b91-140">Jäännöspoisto 125 prosenttia</span><span class="sxs-lookup"><span data-stu-id="59b91-140">125 percent reducing balance depreciation</span></span>](125-percent-reducing-balance-depreciation.md)

[<span data-ttu-id="59b91-141">Jäännöspoisto 150 prosenttia</span><span class="sxs-lookup"><span data-stu-id="59b91-141">150 percent reducing balance depreciation</span></span>](150-percent-reducing-balance-depreciation.md)

[<span data-ttu-id="59b91-142">Jäännöspoisto 175 prosenttia</span><span class="sxs-lookup"><span data-stu-id="59b91-142">175 percent reducing balance depreciation</span></span>](175-percent-reducing-balance-depreciation.md)

[<span data-ttu-id="59b91-143">Jäännöspoisto 200 prosenttia</span><span class="sxs-lookup"><span data-stu-id="59b91-143">200 percent reducing balance depreciation</span></span>](200-percent-reducing-balance-depreciation.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]