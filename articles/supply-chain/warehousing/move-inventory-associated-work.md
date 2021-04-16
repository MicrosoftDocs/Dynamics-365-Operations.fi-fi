---
title: Työhön liitetyn varaston siirtäminen varastonhallinnassa
description: Voit päättää varaston siirron avulla, mitä varastotyöntekijät saavat siirtää varattuun varastoon.
author: Mirzaab
ms.date: 05/26/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSWorker
audience: Application User
ms.reviewer: kamaybac
ms.custom: 269384
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d6477a91b3c65e8be5ab527eaff12c92ae7918b7
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/01/2021
ms.locfileid: "5808747"
---
# <a name="movement-of-inventory-with-associated-work-in-warehouse-management"></a><span data-ttu-id="59356-103">Työhön liitetyn varaston siirtäminen varastonhallinnassa</span><span class="sxs-lookup"><span data-stu-id="59356-103">Movement of inventory with associated work in Warehouse management</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="59356-104">Voit päättää varaston siirron avulla, mitä varastotyöntekijät saavat siirtää varattuun varastoon.</span><span class="sxs-lookup"><span data-stu-id="59356-104">Using movement of inventory, you can decide which warehouse workers are allowed to move reserved inventory.</span></span> <span data-ttu-id="59356-105">Tämä parantaa joustavuutta säännellyissä varastoissa, joissa voit olla antamatta työtekijällä mahdollisuuden valita uuden keräilysijainnin aiemmin luodulle keräilytyölle.</span><span class="sxs-lookup"><span data-stu-id="59356-105">This provides a flexibility in regulated warehouses where you can decide to not allow a worker to choose a new pick location for pick work that is already created.</span></span> <span data-ttu-id="59356-106">Sen avulla varastopäälliköt voivat myös hallita, mitä ominaisuuksia kokemattomat työntekijät saavat.</span><span class="sxs-lookup"><span data-stu-id="59356-106">It also allows a warehouse manager to control which capabilities some less experienced workers should have.</span></span>

<span data-ttu-id="59356-107">Varastotyöntekijöiden päivittäisten toimenpiteiden hallintaan liittyvästä monipuolisuudesta on hyöytä esimerkiksi seuraavanlaisissa skenaarioissa:</span><span class="sxs-lookup"><span data-stu-id="59356-107">The flexibility to manage the daily operations of warehouse workers can be useful in scenarios such as these:</span></span>

## <a name="scenario-1"></a><span data-ttu-id="59356-108">Skenaario 1</span><span class="sxs-lookup"><span data-stu-id="59356-108">Scenario 1</span></span>

<span data-ttu-id="59356-109">Yrityksellä on suhteellisen pieni vastaanottoalue ja se on täynnä poispanoa odottavia kuormalavoja ja laatikoita.</span><span class="sxs-lookup"><span data-stu-id="59356-109">A company has a relatively small receiving area, and it’s congested with pallets and boxes awaiting put away.</span></span> <span data-ttu-id="59356-110">Suurta lähetystä odotetaan kuluvana päivänä, joten vastaanottotyöntekijä päättää tyhjentää vastaanottoalueen siirtämällä osan kuormalavoista toissijaiselle saapuvien väliaikaiselle varastoalueelle.</span><span class="sxs-lookup"><span data-stu-id="59356-110">A large shipment is expected on the current day, so the receiving clerk decides to clear up the receiving area by moving some of the pallets to a secondary inbound staging area.</span></span>

## <a name="scenario-2"></a><span data-ttu-id="59356-111">Skenaario 2</span><span class="sxs-lookup"><span data-stu-id="59356-111">Scenario 2</span></span>

<span data-ttu-id="59356-112">Kokenut varastotyöntekijä huomaa mahdollisuuden konsolidoida nimikkeet varastossa yhteen sijaintiin sen sijaan, että ne jaettaisiin kolmeen läheiseen sijaintiin niin, että kussakin on vähän nimikkeitä.</span><span class="sxs-lookup"><span data-stu-id="59356-112">An experienced warehouse worker notices an opportunity in a warehouse to consolidate items in one location instead of having them divided across three nearby locations with little quantity on each.</span></span> <span data-ttu-id="59356-113">Työntekijä haluaa konsolidoida määrän siirtämällä nimikkeet kustakin näistä sijainneista samaan sijaintiin ja samaan rekisterikilpeen.</span><span class="sxs-lookup"><span data-stu-id="59356-113">The worker wants to consolidate the quantity by moving items from each of these locations into the same location and onto the same license plate.</span></span>

## <a name="scenario-3"></a><span data-ttu-id="59356-114">Skenaario 3</span><span class="sxs-lookup"><span data-stu-id="59356-114">Scenario 3</span></span>

<span data-ttu-id="59356-115">Kuormalava odottaa lähetystä väliaikaisessa sijainnissa, kuten STAGE01, jonka lähellä on BAYDOOR01.</span><span class="sxs-lookup"><span data-stu-id="59356-115">A pallet is awaiting shipment in a staging location, such as STAGE01, which is near BAYDOOR01.</span></span> <span data-ttu-id="59356-116">Suunnitelmien muutoksen vuoksi kuorma-auto on kuitenkin ajoitettu saapumaan sijaintiin BAYDOOR04.</span><span class="sxs-lookup"><span data-stu-id="59356-116">However, due to a change of plans the truck is scheduled to arrive at BAYDOOR04.</span></span> <span data-ttu-id="59356-117">Kuljetustyöntekijä tietää tämän ja hänen on varmistettava, että kuorma-auton ei tarvitse odottaa lastaamista sijainnista STAGE01.</span><span class="sxs-lookup"><span data-stu-id="59356-117">The shipping clerk is aware of this and needs to ensure that the truck does not have to wait to be loaded from STAGE01.</span></span> <span data-ttu-id="59356-118">Kuljetustyöntekijä päättää siirtää kyseisen lähetyksen nimikkeet sijainnista STAGE01 sijaintiin STAGE04, mikä on lähempänä uutta kohdetta.</span><span class="sxs-lookup"><span data-stu-id="59356-118">The shipping clerk decides to move the items in that shipment from STAGE01 to STAGE04, which is closer to the new destination.</span></span>

### <a name="current-limitations"></a><span data-ttu-id="59356-119">Nykyiset rajoitukset</span><span class="sxs-lookup"><span data-stu-id="59356-119">Current limitations</span></span>

<span data-ttu-id="59356-120">Siirrettävät työrajoituksia ovat vain myyntitilaus, siirtotilauksen varasto-otto, siirtotilauksen vastaanotto, ostotilaus ja täydennystyö.</span><span class="sxs-lookup"><span data-stu-id="59356-120">The work reservations that you can move are limited to Sales order, Transfer order issue, Transfer order receipt, Purchase order, and Replenishment work.</span></span>

<span data-ttu-id="59356-121">Nimikkeiden siirtoa on rajoitettu, jotta työrivejä ei jaeta.</span><span class="sxs-lookup"><span data-stu-id="59356-121">Moving items is restricted to prevent splitting of work lines.</span></span> <span data-ttu-id="59356-122">Jos sinulla on nimikkeen A 100 kappaleen työrivi sijainnista Loc1, et voi siirtää tämän vuoksi vain 30:ntä nimikkeen A kappaletta tästä sijainnista toiseen sijaintiin.</span><span class="sxs-lookup"><span data-stu-id="59356-122">This means that if you have a work line for 100 pcs of item A from location Loc1, you won’t be able to move only 30 pcs of item A from there to another location.</span></span> <span data-ttu-id="59356-123">Tämä aiheuttaisi aiemmin luodun työrivin jakamisen 30:een ja 70:een, koska sijainnit eivät ole nyt samat.</span><span class="sxs-lookup"><span data-stu-id="59356-123">This would lead to a split of the existing work line to 30 and 70, because the locations are now different.</span></span>

<span data-ttu-id="59356-124">Väliaikaisvarastoskenaariossa, joissa rekisterikilpi, johon siirrät tavaroita tai josta siirrät tavaroita, on määritetty työtilauksen kohderekisterikilveksi, vain koko rekisterikilven siirto on sallittu, jotta kohderekisterikilpi ei jakaudu.</span><span class="sxs-lookup"><span data-stu-id="59356-124">For staging scenarios, where the license plate you move the goods from or the license plate you move the goods to, are set as a Target LP for a work order, only movement of the entire LP is allowed, so as not to break up the Target LP.</span></span>

<span data-ttu-id="59356-125">Tällä hetkellä tuetaan vain ad hoc -siirtoja.</span><span class="sxs-lookup"><span data-stu-id="59356-125">Only the ad hoc movement is currently supported.</span></span> <span data-ttu-id="59356-126">Tämän vuoksi et voi siirtää varattua varastoa eteenpäin mallin mobiililaitteen valikkovaihtoehdoilla.</span><span class="sxs-lookup"><span data-stu-id="59356-126">That means that you will not be able to move reserved inventory through the movement by template mobile device menu items.</span></span>

### <a name="set-up-permission-to-move-reserved-inventory-for-individual-workers"></a><span data-ttu-id="59356-127">Varatun varaston siirto-oikeuksien määrittäminen yksittäisille työntekijöille</span><span class="sxs-lookup"><span data-stu-id="59356-127">Set up permission to move reserved inventory for individual workers</span></span>

<span data-ttu-id="59356-128">Valitse työntekijän, jolle annetaan oikeus siirtää varattua varastoa, **Salli työhön liitetyn varaston siirto** -valintaruutu kohdassa **Varastonhallinta \> Asetukset \> Työntekijä**.</span><span class="sxs-lookup"><span data-stu-id="59356-128">For the worker who is allowed to move reserved inventory, select the **Allow movement of inventory with work associated** check box under **Warehouse management \> Setup \> Worker**.</span></span>  

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
