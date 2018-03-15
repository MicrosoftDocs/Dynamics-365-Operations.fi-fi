---
title: Huoltokohteen suhteet
description: "Voit luoda suhteen huoltokohteen ja huoltosopimuksen tai huoltotilauksen välille."
author: YuyuScheller
manager: AnnBe
ms.date: 02/21/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SMAServiceObjectRelation
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: YuyuScheller
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 221b9dae7e83e7f4a535ac60f2a2011533d7861c
ms.openlocfilehash: 0e54a0dc9b643077d45fe76e073772e81f99ea44
ms.contentlocale: fi-fi
ms.lasthandoff: 02/21/2018

---

# <a name="service-object-relations"></a><span data-ttu-id="86768-103">Huoltokohteen suhteet</span><span class="sxs-lookup"><span data-stu-id="86768-103">Service object relations</span></span> 

[!include[banner](../includes/banner.md)]



<span data-ttu-id="86768-104">Voit luoda suhteen huoltokohteen ja huoltosopimuksen tai huoltotilauksen välille.</span><span class="sxs-lookup"><span data-stu-id="86768-104">You can create service object relations between a service object and a service agreement or service order.</span></span> <span data-ttu-id="86768-105">Kun luot suhteen, liität huoltokohteen huoltosopimukseen tai huoltotilaukseen.</span><span class="sxs-lookup"><span data-stu-id="86768-105">When you create a relation, you attach the service object to the service agreement or service order.</span></span>

<span data-ttu-id="86768-106">Kun suhde on luotu, voit liittää huoltokohteen huoltosopimuksen tai huoltotilauksen riveille.</span><span class="sxs-lookup"><span data-stu-id="86768-106">After the relation is created, you can attach the service object to any lines on the service agreement or service order.</span></span>

## <a name="template-boms"></a><span data-ttu-id="86768-107">Mallituoterakenteet</span><span class="sxs-lookup"><span data-stu-id="86768-107">Template BOMs</span></span>

<span data-ttu-id="86768-108">Voit määrittää kohdesuhteelle myös mallituoterakenteen.</span><span class="sxs-lookup"><span data-stu-id="86768-108">You can also specify a template BOM for the object relation.</span></span> <span data-ttu-id="86768-109">Mallituoterakenne on sen kohteen tuoterakenne, jolle huolto suoritetaan.</span><span class="sxs-lookup"><span data-stu-id="86768-109">The template BOM is a bill of materials for the object on which you perform service.</span></span> <span data-ttu-id="86768-110">Jos vaihdat huoltokohteen komponenttiosan huoltokäynnin aikana, voit rekisteröidä tämän muutoksen huollon tuoterakenteeseen Huoltokohteet-lomakkeessa.</span><span class="sxs-lookup"><span data-stu-id="86768-110">If you replace a component part of the service object during a service visit, you can register this change in the service BOM by using the Service objects form.</span></span>

## <a name="example"></a><span data-ttu-id="86768-111">Esimerkki</span><span class="sxs-lookup"><span data-stu-id="86768-111">Example</span></span>

<span data-ttu-id="86768-112">Luot huoltosopimuksen kahden hissin huoltamisesta asiakkaan toimipisteessä.</span><span class="sxs-lookup"><span data-stu-id="86768-112">You create a service agreement for servicing two elevators at a customer site.</span></span>
<span data-ttu-id="86768-113">Huoltosopimuksen on tunnus SAL-001.</span><span class="sxs-lookup"><span data-stu-id="86768-113">The service agreement has the identifier ID SAL-001.</span></span>

<span data-ttu-id="86768-114">Hissit on määritetty Huoltokohteeksi-lomakkeessa kohteiksi EL-S/1000 ja EL-L/1000.</span><span class="sxs-lookup"><span data-stu-id="86768-114">The elevators are set up in the Service objects form as objects, EL-S/1000 and EL-L/1000.</span></span>

<span data-ttu-id="86768-115">Liität huoltokohteet EL-S/1000 ja EL-L/1000 huoltosopimukseen.</span><span class="sxs-lookup"><span data-stu-id="86768-115">You attach the service objects, EL-S/1000 and EL-L/1000, to the service agreement.</span></span>

<span data-ttu-id="86768-116">Haluat rekisteröidä muutokset huoltokohteen tuoterakenteeseen, kun vaihdat kohteen komponenttiosia, joten liität huollon tuoterakenteen huoltokohteen suhteeseen seuraavassa taulukossa kuvatulla tavalla.</span><span class="sxs-lookup"><span data-stu-id="86768-116">You want to register changes in the BOM for the service object as you replace component parts of the object, so you attach a service BOM to the service object relation, as described in the following table.</span></span>

| <span data-ttu-id="86768-117">Huoltokohde</span><span class="sxs-lookup"><span data-stu-id="86768-117">Service object</span></span> | <span data-ttu-id="86768-118">Suhde – huoltosopimus</span><span class="sxs-lookup"><span data-stu-id="86768-118">Relation – Service agreement</span></span> | <span data-ttu-id="86768-119">Huollon tuoterakenne</span><span class="sxs-lookup"><span data-stu-id="86768-119">Service BOM</span></span>   |
|----------------|------------------------------|---------------|
| <span data-ttu-id="86768-120">EL-S/1000</span><span class="sxs-lookup"><span data-stu-id="86768-120">EL-S/1000</span></span>      | <span data-ttu-id="86768-121">ID SAL-001</span><span class="sxs-lookup"><span data-stu-id="86768-121">ID SAL-001</span></span>                   | <span data-ttu-id="86768-122">BOM-EL-S/1000</span><span class="sxs-lookup"><span data-stu-id="86768-122">BOM-EL-S/1000</span></span> |
| <span data-ttu-id="86768-123">EL-L/1000</span><span class="sxs-lookup"><span data-stu-id="86768-123">EL-L/1000</span></span>      | <span data-ttu-id="86768-124">ID SAL-001</span><span class="sxs-lookup"><span data-stu-id="86768-124">ID SAL-001</span></span>                   | <span data-ttu-id="86768-125">BOM-EL-L/1000</span><span class="sxs-lookup"><span data-stu-id="86768-125">BOM-EL-L/1000</span></span> |

<span data-ttu-id="86768-126">Koska sopimus sisältää huoltokohteen suhteita, voi nyt luoda näiden kohteiden huoltosopimusrivit seuraavassa taulukossa osoitetulla tavalla.</span><span class="sxs-lookup"><span data-stu-id="86768-126">Because there are service object relations for the agreement, you can now create service agreement lines with these objects, as shown in the following table.</span></span>

| <span data-ttu-id="86768-127">Tapahtumalaji</span><span class="sxs-lookup"><span data-stu-id="86768-127">Transaction type</span></span> | <span data-ttu-id="86768-128">Luokka</span><span class="sxs-lookup"><span data-stu-id="86768-128">Category</span></span>           | <span data-ttu-id="86768-129">Huoltokohde</span><span class="sxs-lookup"><span data-stu-id="86768-129">Service object</span></span> |
|------------------|--------------------|----------------|
| <span data-ttu-id="86768-130">Tunti</span><span class="sxs-lookup"><span data-stu-id="86768-130">Hour</span></span>             | <span data-ttu-id="86768-131">Tarkastus</span><span class="sxs-lookup"><span data-stu-id="86768-131">Inspection</span></span>         | <span data-ttu-id="86768-132">EL-S/1000</span><span class="sxs-lookup"><span data-stu-id="86768-132">EL-S/1000</span></span>      |
| <span data-ttu-id="86768-133">Tunti</span><span class="sxs-lookup"><span data-stu-id="86768-133">Hour</span></span>             | <span data-ttu-id="86768-134">Vaihdelaatikon puhdistus</span><span class="sxs-lookup"><span data-stu-id="86768-134">Gear box cleaning</span></span>  | <span data-ttu-id="86768-135">EL-S/1000</span><span class="sxs-lookup"><span data-stu-id="86768-135">EL-S/1000</span></span>      |
| <span data-ttu-id="86768-136">Nimike</span><span class="sxs-lookup"><span data-stu-id="86768-136">Item</span></span>             | <span data-ttu-id="86768-137">Puhdistusmateriaalit</span><span class="sxs-lookup"><span data-stu-id="86768-137">Cleaning materials</span></span> | <span data-ttu-id="86768-138">EL-S/1000</span><span class="sxs-lookup"><span data-stu-id="86768-138">EL-S/1000</span></span>      |
| <span data-ttu-id="86768-139">Tunti</span><span class="sxs-lookup"><span data-stu-id="86768-139">Hour</span></span>             | <span data-ttu-id="86768-140">Tarkastus</span><span class="sxs-lookup"><span data-stu-id="86768-140">Inspection</span></span>         | <span data-ttu-id="86768-141">EL-L/1000</span><span class="sxs-lookup"><span data-stu-id="86768-141">EL-L/1000</span></span>      |
| <span data-ttu-id="86768-142">Tunti</span><span class="sxs-lookup"><span data-stu-id="86768-142">Hour</span></span>             | <span data-ttu-id="86768-143">Vaihdelaatikon puhdistus</span><span class="sxs-lookup"><span data-stu-id="86768-143">Gearbox cleaning</span></span>   | <span data-ttu-id="86768-144">EL-L/1000</span><span class="sxs-lookup"><span data-stu-id="86768-144">EL-L/1000</span></span>      |
| <span data-ttu-id="86768-145">Nimike</span><span class="sxs-lookup"><span data-stu-id="86768-145">Item</span></span>             | <span data-ttu-id="86768-146">Puhdistusmateriaalit</span><span class="sxs-lookup"><span data-stu-id="86768-146">Cleaning materials</span></span> | <span data-ttu-id="86768-147">EL-L/1000</span><span class="sxs-lookup"><span data-stu-id="86768-147">EL-L/1000</span></span>      |

<span data-ttu-id="86768-148">Hissin EL-S/1000 vaihdelaatikko on vaihdettava huoltokäynnillä.</span><span class="sxs-lookup"><span data-stu-id="86768-148">On a service visit, you have to replace the gearbox for elevator EL-S/1000.</span></span> <span data-ttu-id="86768-149">Kun haluat vaihtaa kohteen komponenttiosan, siirry graafiseen rakennesuunnitteluun käyttämällä nykyiselle huoltosopimukselle määritettävää huoltokohteen suhdetta.</span><span class="sxs-lookup"><span data-stu-id="86768-149">To replace a component part of the object, you can access the BOM Designer by using the service object relation that you set up for the current service agreement.</span></span>

<span data-ttu-id="86768-150">Graafisen rakennesuunnittelun avaaminen huoltokohteen suhteen avulla</span><span class="sxs-lookup"><span data-stu-id="86768-150">Access the BOM Designer by using a service object relation</span></span>

1. <span data-ttu-id="86768-151">Huoltosopimukset</span><span class="sxs-lookup"><span data-stu-id="86768-151">Service agreements</span></span>
2. <span data-ttu-id="86768-152">Kaksoisnapsauta huoltosopimusta tai luo uusi huoltosopimus valitsemalla Huoltosopimus.</span><span class="sxs-lookup"><span data-stu-id="86768-152">Double-click a service agreement, or click Service agreement to create a service agreement.</span></span>
3. <span data-ttu-id="86768-153">Valitse Asetukset-välilehti.</span><span class="sxs-lookup"><span data-stu-id="86768-153">Click the Setup tab.</span></span>
4. <span data-ttu-id="86768-154">Liitä mallituoterakenne huoltosopimukseen valitsemalla Huoltokohteet.</span><span class="sxs-lookup"><span data-stu-id="86768-154">Click Service objects to attach a template BOM to the service agreement.</span></span>
5. <span data-ttu-id="86768-155">Muokkaa mallituoterakennetta avaamalla suunnittelulomake valitsemalla Suunnittelutoiminto Huoltokohteet-lomakkeessa.</span><span class="sxs-lookup"><span data-stu-id="86768-155">In the Service objects form, click Designer to open the Designer form to modify the template BOM.</span></span>

## <a name="automatically-created-service-orders"></a><span data-ttu-id="86768-156">Automaattisesti luodut huoltotilaukset</span><span class="sxs-lookup"><span data-stu-id="86768-156">Automatically created service orders</span></span>

<span data-ttu-id="86768-157">Jos luot huoltosopimuksen huoltotilaukset automaattisesti, myös sopimuksen huoltokohteiden suhteet luodaan huoltotilauksissa.</span><span class="sxs-lookup"><span data-stu-id="86768-157">If you automatically create service orders for a service agreement, the service object relations in the agreement are also created in the service orders.</span></span>


