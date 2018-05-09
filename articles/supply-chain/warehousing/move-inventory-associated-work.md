---
title: "Työhön liitetyn varaston siirtäminen varastonhallinnassa"
description: "Tässä ohjeaiheessa kerrotaan kappaleen keräilyvahvistuksen määrittämisestä ja käyttämisestä mobiililaitteessa."
author: Mirzaab
manager: AnnBe
ms.date: 05/26/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: WHSWorker
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, Operations
ms.custom: 269384
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 2889f04017bdd20be05174146ba88a24cbefacbb
ms.contentlocale: fi-fi
ms.lasthandoff: 05/08/2018

---

# <a name="movement-of-inventory-with-associated-work-in-warehouse-management"></a><span data-ttu-id="9babf-103">Työhön liitetyn varaston siirtäminen varastonhallinnassa</span><span class="sxs-lookup"><span data-stu-id="9babf-103">Movement of inventory with associated work in Warehouse management</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9babf-104">Voit päättää varaston siirron avulla, mitä varastotyöntekijät saavat siirtää varattuun varastoon.</span><span class="sxs-lookup"><span data-stu-id="9babf-104">Using movement of inventory, you can decide which warehouse workers are allowed to move reserved inventory.</span></span> <span data-ttu-id="9babf-105">Tämä parantaa joustavuutta säännellyissä varastoissa, joissa voit olla antamatta työtekijällä mahdollisuuden valita uuden keräilysijainnin aiemmin luodulle keräilytyölle.</span><span class="sxs-lookup"><span data-stu-id="9babf-105">This provides a flexibility in regulated warehouses where you can decide to not allow a worker to choose a new pick location for pick work that is already created.</span></span> <span data-ttu-id="9babf-106">Sen avulla varastopäälliköt voivat myös hallita, mitä ominaisuuksia kokemattomat työntekijät saavat.</span><span class="sxs-lookup"><span data-stu-id="9babf-106">It also allows a warehouse manager to control which capabilities some less experienced workers should have.</span></span>

<span data-ttu-id="9babf-107">Varastotyöntekijöiden päivittäisten toimenpiteiden hallintaan liittyvästä monipuolisuudesta on hyöytä esimerkiksi seuraavanlaisissa skenaarioissa:</span><span class="sxs-lookup"><span data-stu-id="9babf-107">The flexibility to manage the daily operations of warehouse workers can be useful in scenarios such as these:</span></span>

## <a name="scenario-1"></a><span data-ttu-id="9babf-108">Skenaario 1</span><span class="sxs-lookup"><span data-stu-id="9babf-108">Scenario 1</span></span>
<span data-ttu-id="9babf-109">Yrityksellä on suhteellisen pieni vastaanottoalue ja se on täynnä poispanoa odottavia kuormalavoja ja laatikoita.</span><span class="sxs-lookup"><span data-stu-id="9babf-109">A company has a relatively small receiving area, and it’s congested with pallets and boxes awaiting put away.</span></span> <span data-ttu-id="9babf-110">Suurta lähetystä odotetaan kuluvana päivänä, joten vastaanottotyöntekijä päättää tyhjentää vastaanottoalueen siirtämällä osan kuormalavoista toissijaiselle saapuvien väliaikaiselle varastoalueelle.</span><span class="sxs-lookup"><span data-stu-id="9babf-110">A large shipment is expected on the current day, so the receiving clerk decides to clear up the receiving area by moving some of the pallets to a secondary inbound staging area.</span></span>

## <a name="scenario-2"></a><span data-ttu-id="9babf-111">Skenaario 2</span><span class="sxs-lookup"><span data-stu-id="9babf-111">Scenario 2</span></span>
<span data-ttu-id="9babf-112">Kokenut varastotyöntekijä huomaa mahdollisuuden konsolidoida nimikkeet varastossa yhteen sijaintiin sen sijaan, että ne jaettaisiin kolmeen läheiseen sijaintiin niin, että kussakin on vähän nimikkeitä.</span><span class="sxs-lookup"><span data-stu-id="9babf-112">An experienced warehouse worker notices an opportunity in a warehouse to consolidate items in one location instead of having them divided across 3 nearby locations with little quantity on each.</span></span> <span data-ttu-id="9babf-113">Työntekijä haluaa konsolidoida määrän siirtämällä nimikkeet kustakin näistä sijainneista samaan sijaintiin ja samaan rekisterikilpeen.</span><span class="sxs-lookup"><span data-stu-id="9babf-113">The worker wants to consolidate the quantity by moving items from each of these locations into the same location and onto the same license plate.</span></span>

## <a name="scenario-3"></a><span data-ttu-id="9babf-114">Skenaario 3</span><span class="sxs-lookup"><span data-stu-id="9babf-114">Scenario 3</span></span>
<span data-ttu-id="9babf-115">Kuormalava odottaa lähetystä väliaikaisessa sijainnissa, kuten STAGE01, jonka lähellä on BAYDOOR01.</span><span class="sxs-lookup"><span data-stu-id="9babf-115">A pallet is awaiting shipment in a staging location, such as STAGE01, which is near BAYDOOR01.</span></span> <span data-ttu-id="9babf-116">Suunnitelmien muutoksen vuoksi kuorma-auto on kuitenkin ajoitettu saapumaan sijaintiin BAYDOOR04.</span><span class="sxs-lookup"><span data-stu-id="9babf-116">However, due to a change of plans the truck is scheduled to arrive at BAYDOOR04.</span></span> <span data-ttu-id="9babf-117">Kuljetustyöntekijä tietää tämän ja hänen on varmistettava, että kuorma-auton ei tarvitse odottaa lastaamista sijainnista STAGE01.</span><span class="sxs-lookup"><span data-stu-id="9babf-117">The shipping clerk is aware of this and needs to ensure that the truck does not have to wait to be loaded from STAGE01.</span></span> <span data-ttu-id="9babf-118">Kuljetustyöntekijä päättää siirtää kyseisen lähetyksen nimikkeet sijainnista STAGE01 sijaintiin STAGE04, mikä on lähempänä uutta kohdetta.</span><span class="sxs-lookup"><span data-stu-id="9babf-118">The shipping clerk decides to move the items in that shipment from STAGE01 to STAGE04, which is closer to the new destination.</span></span>

### <a name="current-limitations"></a><span data-ttu-id="9babf-119">Nykyiset rajoitukset</span><span class="sxs-lookup"><span data-stu-id="9babf-119">Current limitations</span></span>

<span data-ttu-id="9babf-120">Siirrettävät työrajoituksia ovat vain myyntitilaus, siirtotilauksen varasto-otto, siirtotilauksen vastaanotto, ostotilaus ja täydennystyö.</span><span class="sxs-lookup"><span data-stu-id="9babf-120">The work reservations that you can move are limited to Sales order, Transfer order issue, Transfer order receipt, Purchase order, and Replenishment work.</span></span>

<span data-ttu-id="9babf-121">Nimikkeiden siirtoa on rajoitettu, jotta työrivejä ei jaeta.</span><span class="sxs-lookup"><span data-stu-id="9babf-121">Moving items is restricted to prevent splitting of work lines.</span></span> <span data-ttu-id="9babf-122">Jos sinulla on nimikkeen A 100 kappaleen työrivi sijainnista Loc1, et voi siirtää tämän vuoksi vain 30:ntä nimikkeen A kappaletta tästä sijainnista toiseen sijaintiin.</span><span class="sxs-lookup"><span data-stu-id="9babf-122">This means that if you have a work line for 100 pcs of item A from location Loc1, you won’t be able to move only 30 pcs of item A from there to another location.</span></span> <span data-ttu-id="9babf-123">Tämä aiheuttaisi aiemmin luodun työrivin jakamisen 30:een ja 70:een, koska sijainnit eivät ole nyt samat.</span><span class="sxs-lookup"><span data-stu-id="9babf-123">This would lead to a split of the existing work line to 30 and 70, because the locations are now different.</span></span>

<span data-ttu-id="9babf-124">Väliaikaisvarastoskenaariossa, joissa rekisterikilpi, johon siirrät tavaroita tai josta siirrät tavaroita, on määritetty työtilauksen kohderekisterikilveksi, vain koko rekisterikilven siirto on sallittu, jotta kohderekisterikilpi ei jakaudu.</span><span class="sxs-lookup"><span data-stu-id="9babf-124">For staging scenarios, where the license plate you move the goods from or the license plate you move the goods to, are set as a Target LP for a work order, only movement of the entire LP is allowed, so as not to break up the Target LP.</span></span>
<span data-ttu-id="9babf-125">Tällä hetkellä tuetaan vain ad hoc -siirtoja.</span><span class="sxs-lookup"><span data-stu-id="9babf-125">Only the ad hoc movement is currently supported.</span></span> <span data-ttu-id="9babf-126">Tämän vuoksi et voi siirtää varattua varastoa eteenpäin mallin mobiililaitteen valikkovaihtoehdoilla.</span><span class="sxs-lookup"><span data-stu-id="9babf-126">That means that you will not be able to move reserved inventory through the movement by template mobile device menu items.</span></span>

### <a name="set-up-permission-to-move-reserved-inventory-for-individual-workers"></a><span data-ttu-id="9babf-127">Varatun varaston siirto-oikeuksien määrittäminen yksittäisille työntekijöille</span><span class="sxs-lookup"><span data-stu-id="9babf-127">Set up permission to move reserved inventory for individual workers</span></span>

<span data-ttu-id="9babf-128">Valitse työntekijän, jolle annetaan oikeus siirtää varattua varastoa, **Salli työhön liitetyn varaston siirto** -valintaruutu kohdassa **Varastonhallinta** > **Asetukset** > **Työntekijä**.</span><span class="sxs-lookup"><span data-stu-id="9babf-128">For the worker who should be allowed to move reserved inventory, select the **Allow movement of inventory with work associated** check box under **Warehouse management** > **Setup** > **Worker**.</span></span>  

### <a name="backported"></a><span data-ttu-id="9babf-129">Takaisinsovitus</span><span class="sxs-lookup"><span data-stu-id="9babf-129">Backported</span></span>

<span data-ttu-id="9babf-130">Tämä toiminto on takaisinsovitettu Microsoft Dynamics AX 2012 R3:een ja on käytettävissä CU12:n osana.</span><span class="sxs-lookup"><span data-stu-id="9babf-130">This feature has also been back-ported to Microsoft Dynamics AX 2012 R3 and will be available as part of CU12.</span></span>
<span data-ttu-id="9babf-131">Se voidaan myös ladata erikseen KB-numeron 3192548 kautta.</span><span class="sxs-lookup"><span data-stu-id="9babf-131">It can also be downloaded individually through KB number 3192548.</span></span> 


