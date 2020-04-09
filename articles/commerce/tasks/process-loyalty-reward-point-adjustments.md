---
title: Kanta-asiakkuuspalkkiopisteiden oikaisujen käsittely
description: Tässä menettelyssä käsitellään, miten kanta-asiakaskortin tietoa voi etsiä ja miten kanta-asiakkaan palkkiopisteitä säädetään.
author: scott-tucker
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailLoyaltyCards, RetailLoyaltyCardRewardPointTrans, RetailLoyaltyCardRewardPointAdjustment, RetailAffiliationLookup
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: scotttuc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: bdbd9fa60fe4d000359e4695a9fb034fae3ca1b0
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/18/2020
ms.locfileid: "3140723"
---
# <a name="process-loyalty-reward-point-adjustments"></a><span data-ttu-id="f9b26-103">Kanta-asiakkuuspalkkiopisteiden oikaisujen käsittely</span><span class="sxs-lookup"><span data-stu-id="f9b26-103">Process loyalty reward point adjustments</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f9b26-104">Tässä menettelyssä käsitellään, miten kanta-asiakaskortin tietoa voi etsiä ja miten kanta-asiakkaan palkkiopisteitä säädetään.</span><span class="sxs-lookup"><span data-stu-id="f9b26-104">This procedure demonstrates how to look up loyalty card information and adjust loyalty reward points.</span></span> <span data-ttu-id="f9b26-105">Tämän tehtävän luomisessa käytetty USRT-yrityksen demotietoja.</span><span class="sxs-lookup"><span data-stu-id="f9b26-105">The demo data company used to create this task is USRT.</span></span> <span data-ttu-id="f9b26-106">Tämä tehtävä on tarkoitettu Commercen toiminnoista vastaavan johtajan roolille tai asiakaspalvelupäällikön roolille.</span><span class="sxs-lookup"><span data-stu-id="f9b26-106">This task is intended for the Commerce operations manager role or a Customer service manager role.</span></span>

1. <span data-ttu-id="f9b26-107">Valitse Kanta-asiakaskortit</span><span class="sxs-lookup"><span data-stu-id="f9b26-107">Go to Loyalty cards.</span></span>
2. <span data-ttu-id="f9b26-108">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="f9b26-108">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="f9b26-109">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="f9b26-109">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="f9b26-110">Valitse Korttitapahtumat.</span><span class="sxs-lookup"><span data-stu-id="f9b26-110">Click Card transactions.</span></span>
    * <span data-ttu-id="f9b26-111">Voit tarkastella tällä sivulla valitun kanta-asiakaskortin kaikkia kanta-asiakastapahtumia.</span><span class="sxs-lookup"><span data-stu-id="f9b26-111">On this page you can view all loyalty transactions for the selected loyalty card.</span></span>  
5. <span data-ttu-id="f9b26-112">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="f9b26-112">Close the page.</span></span>
6. <span data-ttu-id="f9b26-113">Valitse Korttioikaisut.</span><span class="sxs-lookup"><span data-stu-id="f9b26-113">Click Card adjustments.</span></span>
7. <span data-ttu-id="f9b26-114">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="f9b26-114">Click New.</span></span>
8. <span data-ttu-id="f9b26-115">Anna tai valitse arvo Palkkiopiste-kentässä.</span><span class="sxs-lookup"><span data-stu-id="f9b26-115">In the Reward point field, enter or select a value.</span></span>
9. <span data-ttu-id="f9b26-116">Lisää Summa tai määrä -kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="f9b26-116">In the Amount or quantity field, enter a number.</span></span>
    * <span data-ttu-id="f9b26-117">Voit lisätä pisteitä kanta-asiakaskorttiin tai poistaa niitä käyttämällä positiivisia tai negatiivisia summia.</span><span class="sxs-lookup"><span data-stu-id="f9b26-117">You can add or remove points from the loyalty card by using positive or negative amounts.</span></span>  
10. <span data-ttu-id="f9b26-118">Anna tai valitse arvo Kanta-asiakasohjelma -kentässä.</span><span class="sxs-lookup"><span data-stu-id="f9b26-118">In the Loyalty program field, enter or select a value.</span></span>
11. <span data-ttu-id="f9b26-119">Kirjoita Kommentti-kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="f9b26-119">In the Comment field, type a value.</span></span>
12. <span data-ttu-id="f9b26-120">Valitse Kirjaa oikaisu.</span><span class="sxs-lookup"><span data-stu-id="f9b26-120">Click Post adjustment.</span></span>
13. <span data-ttu-id="f9b26-121">Valitse Kyllä.</span><span class="sxs-lookup"><span data-stu-id="f9b26-121">Click Yes.</span></span>
14. <span data-ttu-id="f9b26-122">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="f9b26-122">Close the page.</span></span>
    * <span data-ttu-id="f9b26-123">Sivu yleensä päivitetään tässä vaiheessa, jotta voit katsoa palkkiopisteiden oikaisun tuloksen Palkkiopisteyhteenveto-välilehdessä. Mutta jos käytät tätä tehtäväopastuksena, älä tee päivitystä nyt, sillä se pysäyttää tehtäväopastuksen.</span><span class="sxs-lookup"><span data-stu-id="f9b26-123">Normally at this point you'd refresh the page to see the result of the reward points adjustment in the Reward point summary tab. But if you are running this as a task guide, don't refresh now because if you do, the task guide will stop.</span></span>  
15. <span data-ttu-id="f9b26-124">Valitse Korttitapahtumat.</span><span class="sxs-lookup"><span data-stu-id="f9b26-124">Click Card transactions.</span></span>
16. <span data-ttu-id="f9b26-125">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="f9b26-125">Close the page.</span></span>

