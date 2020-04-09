---
title: Valmiiksi ilmoittaminen rekisterikilpiohjaamattomaan sijaintiin (Sovellus, Toukokuu 2016)
description: Tässä tehtäväoppaassa näytetään esimerkki valmiiksi ilmoittamisesta sijaintiin, jota ei ohjata rekisterikilvellä.
author: ChristianRytt
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WrkCtrResourceGroup, ProdTableListPage, ProdTableCreate, InventItemIdLookupPurchase, ProdParmCostEstimation, ProdParmStartUp, ProdParmReportFinished, WHSWorkTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2e96267a80160a63258b97f2e6ac49fad753a93a
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/18/2020
ms.locfileid: "3148908"
---
# <a name="report-as-finished-to-a-non-license-plate-controlled-location--application-may-2016"></a><span data-ttu-id="90c0f-103">Valmiiksi ilmoittaminen rekisterikilpiohjaamattomaan sijaintiin (Sovellus, Toukokuu 2016)</span><span class="sxs-lookup"><span data-stu-id="90c0f-103">Report as finished to a non-license plate controlled location  (Application, May 2016)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="90c0f-104">Tässä tehtäväoppaassa näytetään esimerkki valmiiksi ilmoittamisesta sijaintiin, jota ei ohjata rekisterikilvellä.</span><span class="sxs-lookup"><span data-stu-id="90c0f-104">This task guide shows an example of reporting as finished to a location that isn't license plate–controlled.</span></span> <span data-ttu-id="90c0f-105">Tehtävä edellyttää käytettävää työkäytäntöä.</span><span class="sxs-lookup"><span data-stu-id="90c0f-105">An applicable work policy is the prerequisite for this task.</span></span> <span data-ttu-id="90c0f-106">Työkäytännön määrittäminen on esitelty edellisessä tehtäväoppaassa.</span><span class="sxs-lookup"><span data-stu-id="90c0f-106">A previous task guide showed the setup of the work policy.</span></span> <span data-ttu-id="90c0f-107">Tämä tehtäväopas vaatii Dynamics AX -sovelluksen version 7.0.1 tai sitä uudemman.</span><span class="sxs-lookup"><span data-stu-id="90c0f-107">This task guide requires Dynamics AX application 7.0.1 or later.</span></span>




## <a name="set-up-an-output-location"></a><span data-ttu-id="90c0f-108">Määritä tulostussijainti</span><span class="sxs-lookup"><span data-stu-id="90c0f-108">Set up an output location</span></span>
1. <span data-ttu-id="90c0f-109">Valitse Organisaation hallinto > Resurssit > Resurssiryhmät.</span><span class="sxs-lookup"><span data-stu-id="90c0f-109">Go to Organization administration > Resources > Resource groups.</span></span>
2. <span data-ttu-id="90c0f-110">Valitse luettelosta resurssiryhmä 5102.</span><span class="sxs-lookup"><span data-stu-id="90c0f-110">In the list, select resource group '5102'.</span></span>
3. <span data-ttu-id="90c0f-111">Valitse Muokkaa.</span><span class="sxs-lookup"><span data-stu-id="90c0f-111">Click Edit.</span></span>
4. <span data-ttu-id="90c0f-112">Kirjoita Tulostusvarasto-kenttään arvo 51.</span><span class="sxs-lookup"><span data-stu-id="90c0f-112">In the Output warehouse field, enter '51'.</span></span>
5. <span data-ttu-id="90c0f-113">Kirjoita Tulostussijainti-kenttään arvo 001.</span><span class="sxs-lookup"><span data-stu-id="90c0f-113">In the Output location field, enter '001'.</span></span>
    * <span data-ttu-id="90c0f-114">Sijainti 001 ei ole rekisterikilven mukaan ohjattu sijainti.</span><span class="sxs-lookup"><span data-stu-id="90c0f-114">Location 001 isn't a license plate–controlled location.</span></span> <span data-ttu-id="90c0f-115">Voit määrittää rekisterikilven mukaan ohjaamattoman sijainnin ainoastaan, jos sijainnille on olemassa soveltuva työkäytäntö.</span><span class="sxs-lookup"><span data-stu-id="90c0f-115">You can set up a non–license plate output location only if an applicable work policy exists for the location.</span></span>  

## <a name="create-a-production-order-and-report-it-as-finished"></a><span data-ttu-id="90c0f-116">Luo tuotantotilaus ja ilmoita se valmiiksi</span><span class="sxs-lookup"><span data-stu-id="90c0f-116">Create a production order and report it as finished</span></span>
1. <span data-ttu-id="90c0f-117">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="90c0f-117">Close the page.</span></span>
2. <span data-ttu-id="90c0f-118">Siirry kohtaan Tuotannonhallinta > Tuotantotilaukset > Kaikki tuotantotilaukset.</span><span class="sxs-lookup"><span data-stu-id="90c0f-118">Go to Production control > Production orders > All production orders.</span></span>
3. <span data-ttu-id="90c0f-119">Valitse Uusi tuotantotilaus.</span><span class="sxs-lookup"><span data-stu-id="90c0f-119">Click New production order.</span></span>
4. <span data-ttu-id="90c0f-120">Kirjoita Nimiketunnus-kenttään arvo L0101.</span><span class="sxs-lookup"><span data-stu-id="90c0f-120">In the Item number field, enter 'L0101'.</span></span>
5. <span data-ttu-id="90c0f-121">Valitse Luo.</span><span class="sxs-lookup"><span data-stu-id="90c0f-121">Click Create.</span></span>
6. <span data-ttu-id="90c0f-122">Valitse toimintoruudussa Tuotantotilaus.</span><span class="sxs-lookup"><span data-stu-id="90c0f-122">On the Action Pane, click Production order.</span></span>
7. <span data-ttu-id="90c0f-123">Valitse Arvio.</span><span class="sxs-lookup"><span data-stu-id="90c0f-123">Click Estimate.</span></span>
8. <span data-ttu-id="90c0f-124">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="90c0f-124">Click OK.</span></span>
9. <span data-ttu-id="90c0f-125">Valitse Käynnistys.</span><span class="sxs-lookup"><span data-stu-id="90c0f-125">Click Start.</span></span>
10. <span data-ttu-id="90c0f-126">Valitse Yleiset-välilehti.</span><span class="sxs-lookup"><span data-stu-id="90c0f-126">Click the General tab.</span></span>
11. <span data-ttu-id="90c0f-127">Valitse Automaattinen tuoterakennekulutus -kentässä Ei koskaan.</span><span class="sxs-lookup"><span data-stu-id="90c0f-127">In the Automatic BOM consumption field, select 'Never'.</span></span>
12. <span data-ttu-id="90c0f-128">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="90c0f-128">Click OK.</span></span>
13. <span data-ttu-id="90c0f-129">Valitse Ilmoita valmiiksi.</span><span class="sxs-lookup"><span data-stu-id="90c0f-129">Click Report as finished.</span></span>
14. <span data-ttu-id="90c0f-130">Valitse Yleiset-välilehti.</span><span class="sxs-lookup"><span data-stu-id="90c0f-130">Click the General tab.</span></span>
15. <span data-ttu-id="90c0f-131">Valitse Hyväksy virhe -kentässä Kyllä.</span><span class="sxs-lookup"><span data-stu-id="90c0f-131">Select Yes in the Accept error field.</span></span>
16. <span data-ttu-id="90c0f-132">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="90c0f-132">Click OK.</span></span>
17. <span data-ttu-id="90c0f-133">Valitse toimintoruudussa Varasto.</span><span class="sxs-lookup"><span data-stu-id="90c0f-133">On the Action Pane, click Warehouse.</span></span>
18. <span data-ttu-id="90c0f-134">Valitse Työn tiedot.</span><span class="sxs-lookup"><span data-stu-id="90c0f-134">Click Work details.</span></span>
    * <span data-ttu-id="90c0f-135">Kun tuotantotilaus on raportoitu päättyneeksi, poispanotöitä ei luotu.</span><span class="sxs-lookup"><span data-stu-id="90c0f-135">When the production order was reported as finished, no work was generated for put-away.</span></span> <span data-ttu-id="90c0f-136">Tämä johtuu siitä, että määritettynä on työn käytäntö, joka estää töiden luonnin, kun tuote L0101 ilmoitetaan valmiiksi sijaintiin 001.</span><span class="sxs-lookup"><span data-stu-id="90c0f-136">This occurs because a work policy is defined that prevents work from being generated when product L0101 is reported as finished to location 001.</span></span>  

