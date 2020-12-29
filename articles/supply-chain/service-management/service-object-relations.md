---
title: Huoltokohteen suhteet
description: Voit luoda suhteen huoltokohteen ja huoltosopimuksen tai huoltotilauksen välille.
author: ShylaThompson
manager: tfehr
ms.date: 02/21/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAServiceObjectRelation
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e2b1b76dffc2751d51c2a25d831fab512b747c15
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/13/2020
ms.locfileid: "4426762"
---
# <a name="service-object-relations"></a><span data-ttu-id="eb7a0-103">Huoltokohteen suhteet</span><span class="sxs-lookup"><span data-stu-id="eb7a0-103">Service object relations</span></span> 

[!include [banner](../includes/banner.md)]

<span data-ttu-id="eb7a0-104">Voit luoda suhteen huoltokohteen ja huoltosopimuksen tai huoltotilauksen välille.</span><span class="sxs-lookup"><span data-stu-id="eb7a0-104">You can create service object relations between a service object and a service agreement or service order.</span></span> <span data-ttu-id="eb7a0-105">Kun luot suhteen, liität huoltokohteen huoltosopimukseen tai huoltotilaukseen.</span><span class="sxs-lookup"><span data-stu-id="eb7a0-105">When you create a relation, you attach the service object to the service agreement or service order.</span></span>

<span data-ttu-id="eb7a0-106">Kun suhde on luotu, voit liittää huoltokohteen huoltosopimuksen tai huoltotilauksen riveille.</span><span class="sxs-lookup"><span data-stu-id="eb7a0-106">After the relation is created, you can attach the service object to any lines on the service agreement or service order.</span></span>

## <a name="template-boms"></a><span data-ttu-id="eb7a0-107">Mallituoterakenteet</span><span class="sxs-lookup"><span data-stu-id="eb7a0-107">Template BOMs</span></span>

<span data-ttu-id="eb7a0-108">Voit määrittää kohdesuhteelle myös mallituoterakenteen.</span><span class="sxs-lookup"><span data-stu-id="eb7a0-108">You can also specify a template BOM for the object relation.</span></span> <span data-ttu-id="eb7a0-109">Mallituoterakenne on sen kohteen tuoterakenne, jolle huolto suoritetaan.</span><span class="sxs-lookup"><span data-stu-id="eb7a0-109">The template BOM is a bill of materials for the object on which you perform service.</span></span> <span data-ttu-id="eb7a0-110">Jos vaihdat huoltokohteen komponenttiosan huoltokäynnin aikana, voit rekisteröidä tämän muutoksen huollon tuoterakenteeseen Huoltokohteet-lomakkeessa.</span><span class="sxs-lookup"><span data-stu-id="eb7a0-110">If you replace a component part of the service object during a service visit, you can register this change in the service BOM by using the Service objects form.</span></span>

## <a name="example"></a><span data-ttu-id="eb7a0-111">Esimerkki</span><span class="sxs-lookup"><span data-stu-id="eb7a0-111">Example</span></span>

<span data-ttu-id="eb7a0-112">Luot huoltosopimuksen kahden hissin huoltamisesta asiakkaan toimipisteessä.</span><span class="sxs-lookup"><span data-stu-id="eb7a0-112">You create a service agreement for servicing two elevators at a customer site.</span></span>
<span data-ttu-id="eb7a0-113">Huoltosopimuksen on tunnus SAL-001.</span><span class="sxs-lookup"><span data-stu-id="eb7a0-113">The service agreement has the identifier ID SAL-001.</span></span>

<span data-ttu-id="eb7a0-114">Hissit on määritetty Huoltokohteeksi-lomakkeessa kohteiksi EL-S/1000 ja EL-L/1000.</span><span class="sxs-lookup"><span data-stu-id="eb7a0-114">The elevators are set up in the Service objects form as objects, EL-S/1000 and EL-L/1000.</span></span>

<span data-ttu-id="eb7a0-115">Liität huoltokohteet EL-S/1000 ja EL-L/1000 huoltosopimukseen.</span><span class="sxs-lookup"><span data-stu-id="eb7a0-115">You attach the service objects, EL-S/1000 and EL-L/1000, to the service agreement.</span></span>

<span data-ttu-id="eb7a0-116">Haluat rekisteröidä muutokset huoltokohteen tuoterakenteeseen, kun vaihdat kohteen komponenttiosia, joten liität huollon tuoterakenteen huoltokohteen suhteeseen seuraavassa taulukossa kuvatulla tavalla.</span><span class="sxs-lookup"><span data-stu-id="eb7a0-116">You want to register changes in the BOM for the service object as you replace component parts of the object, so you attach a service BOM to the service object relation, as described in the following table.</span></span>

| <span data-ttu-id="eb7a0-117">Huoltokohde</span><span class="sxs-lookup"><span data-stu-id="eb7a0-117">Service object</span></span> | <span data-ttu-id="eb7a0-118">Suhde – huoltosopimus</span><span class="sxs-lookup"><span data-stu-id="eb7a0-118">Relation – Service agreement</span></span> | <span data-ttu-id="eb7a0-119">Huollon tuoterakenne</span><span class="sxs-lookup"><span data-stu-id="eb7a0-119">Service BOM</span></span>   |
|----------------|------------------------------|---------------|
| <span data-ttu-id="eb7a0-120">EL-S/1000</span><span class="sxs-lookup"><span data-stu-id="eb7a0-120">EL-S/1000</span></span>      | <span data-ttu-id="eb7a0-121">ID SAL-001</span><span class="sxs-lookup"><span data-stu-id="eb7a0-121">ID SAL-001</span></span>                   | <span data-ttu-id="eb7a0-122">BOM-EL-S/1000</span><span class="sxs-lookup"><span data-stu-id="eb7a0-122">BOM-EL-S/1000</span></span> |
| <span data-ttu-id="eb7a0-123">EL-L/1000</span><span class="sxs-lookup"><span data-stu-id="eb7a0-123">EL-L/1000</span></span>      | <span data-ttu-id="eb7a0-124">ID SAL-001</span><span class="sxs-lookup"><span data-stu-id="eb7a0-124">ID SAL-001</span></span>                   | <span data-ttu-id="eb7a0-125">BOM-EL-L/1000</span><span class="sxs-lookup"><span data-stu-id="eb7a0-125">BOM-EL-L/1000</span></span> |

<span data-ttu-id="eb7a0-126">Koska sopimus sisältää huoltokohteen suhteita, voi nyt luoda näiden kohteiden huoltosopimusrivit seuraavassa taulukossa osoitetulla tavalla.</span><span class="sxs-lookup"><span data-stu-id="eb7a0-126">Because there are service object relations for the agreement, you can now create service agreement lines with these objects, as shown in the following table.</span></span>

| <span data-ttu-id="eb7a0-127">Tapahtumalaji</span><span class="sxs-lookup"><span data-stu-id="eb7a0-127">Transaction type</span></span> | <span data-ttu-id="eb7a0-128">Luokka</span><span class="sxs-lookup"><span data-stu-id="eb7a0-128">Category</span></span>           | <span data-ttu-id="eb7a0-129">Huoltokohde</span><span class="sxs-lookup"><span data-stu-id="eb7a0-129">Service object</span></span> |
|------------------|--------------------|----------------|
| <span data-ttu-id="eb7a0-130">Tunti</span><span class="sxs-lookup"><span data-stu-id="eb7a0-130">Hour</span></span>             | <span data-ttu-id="eb7a0-131">Tarkastus</span><span class="sxs-lookup"><span data-stu-id="eb7a0-131">Inspection</span></span>         | <span data-ttu-id="eb7a0-132">EL-S/1000</span><span class="sxs-lookup"><span data-stu-id="eb7a0-132">EL-S/1000</span></span>      |
| <span data-ttu-id="eb7a0-133">Tunti</span><span class="sxs-lookup"><span data-stu-id="eb7a0-133">Hour</span></span>             | <span data-ttu-id="eb7a0-134">Vaihdelaatikon puhdistus</span><span class="sxs-lookup"><span data-stu-id="eb7a0-134">Gear box cleaning</span></span>  | <span data-ttu-id="eb7a0-135">EL-S/1000</span><span class="sxs-lookup"><span data-stu-id="eb7a0-135">EL-S/1000</span></span>      |
| <span data-ttu-id="eb7a0-136">Nimike</span><span class="sxs-lookup"><span data-stu-id="eb7a0-136">Item</span></span>             | <span data-ttu-id="eb7a0-137">Puhdistusmateriaalit</span><span class="sxs-lookup"><span data-stu-id="eb7a0-137">Cleaning materials</span></span> | <span data-ttu-id="eb7a0-138">EL-S/1000</span><span class="sxs-lookup"><span data-stu-id="eb7a0-138">EL-S/1000</span></span>      |
| <span data-ttu-id="eb7a0-139">Tunti</span><span class="sxs-lookup"><span data-stu-id="eb7a0-139">Hour</span></span>             | <span data-ttu-id="eb7a0-140">Tarkastus</span><span class="sxs-lookup"><span data-stu-id="eb7a0-140">Inspection</span></span>         | <span data-ttu-id="eb7a0-141">EL-L/1000</span><span class="sxs-lookup"><span data-stu-id="eb7a0-141">EL-L/1000</span></span>      |
| <span data-ttu-id="eb7a0-142">Tunti</span><span class="sxs-lookup"><span data-stu-id="eb7a0-142">Hour</span></span>             | <span data-ttu-id="eb7a0-143">Vaihdelaatikon puhdistus</span><span class="sxs-lookup"><span data-stu-id="eb7a0-143">Gearbox cleaning</span></span>   | <span data-ttu-id="eb7a0-144">EL-L/1000</span><span class="sxs-lookup"><span data-stu-id="eb7a0-144">EL-L/1000</span></span>      |
| <span data-ttu-id="eb7a0-145">Nimike</span><span class="sxs-lookup"><span data-stu-id="eb7a0-145">Item</span></span>             | <span data-ttu-id="eb7a0-146">Puhdistusmateriaalit</span><span class="sxs-lookup"><span data-stu-id="eb7a0-146">Cleaning materials</span></span> | <span data-ttu-id="eb7a0-147">EL-L/1000</span><span class="sxs-lookup"><span data-stu-id="eb7a0-147">EL-L/1000</span></span>      |

<span data-ttu-id="eb7a0-148">Hissin EL-S/1000 vaihdelaatikko on vaihdettava huoltokäynnillä.</span><span class="sxs-lookup"><span data-stu-id="eb7a0-148">On a service visit, you have to replace the gearbox for elevator EL-S/1000.</span></span> <span data-ttu-id="eb7a0-149">Kun haluat vaihtaa kohteen komponenttiosan, siirry graafiseen rakennesuunnitteluun käyttämällä nykyiselle huoltosopimukselle määritettävää huoltokohteen suhdetta.</span><span class="sxs-lookup"><span data-stu-id="eb7a0-149">To replace a component part of the object, you can access the BOM Designer by using the service object relation that you set up for the current service agreement.</span></span>

<span data-ttu-id="eb7a0-150">Graafisen rakennesuunnittelun avaaminen huoltokohteen suhteen avulla</span><span class="sxs-lookup"><span data-stu-id="eb7a0-150">Access the BOM Designer by using a service object relation</span></span>

1. <span data-ttu-id="eb7a0-151">Huoltosopimukset</span><span class="sxs-lookup"><span data-stu-id="eb7a0-151">Service agreements</span></span>
2. <span data-ttu-id="eb7a0-152">Kaksoisnapsauta huoltosopimusta tai luo uusi huoltosopimus valitsemalla Huoltosopimus.</span><span class="sxs-lookup"><span data-stu-id="eb7a0-152">Double-click a service agreement, or click Service agreement to create a service agreement.</span></span>
3. <span data-ttu-id="eb7a0-153">Valitse Asetukset-välilehti.</span><span class="sxs-lookup"><span data-stu-id="eb7a0-153">Click the Setup tab.</span></span>
4. <span data-ttu-id="eb7a0-154">Liitä mallituoterakenne huoltosopimukseen valitsemalla Huoltokohteet.</span><span class="sxs-lookup"><span data-stu-id="eb7a0-154">Click Service objects to attach a template BOM to the service agreement.</span></span>
5. <span data-ttu-id="eb7a0-155">Muokkaa mallituoterakennetta avaamalla suunnittelulomake valitsemalla Suunnittelutoiminto Huoltokohteet-lomakkeessa.</span><span class="sxs-lookup"><span data-stu-id="eb7a0-155">In the Service objects form, click Designer to open the Designer form to modify the template BOM.</span></span>

## <a name="automatically-created-service-orders"></a><span data-ttu-id="eb7a0-156">Automaattisesti luodut huoltotilaukset</span><span class="sxs-lookup"><span data-stu-id="eb7a0-156">Automatically created service orders</span></span>

<span data-ttu-id="eb7a0-157">Jos luot huoltosopimuksen huoltotilaukset automaattisesti, myös sopimuksen huoltokohteiden suhteet luodaan huoltotilauksissa.</span><span class="sxs-lookup"><span data-stu-id="eb7a0-157">If you automatically create service orders for a service agreement, the service object relations in the agreement are also created in the service orders.</span></span>

