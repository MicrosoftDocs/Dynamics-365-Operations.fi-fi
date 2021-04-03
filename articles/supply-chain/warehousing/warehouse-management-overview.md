---
title: Varastonhallinnan yhteenveto
description: Varastonhallinnan avulla voit valvoa ja automatisoida varastoprosesseja.
author: ShylaThompson
manager: tfehr
ms.date: 04/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSParameters, WHSWorkPool
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d7d48ecd834c226fb40bede7519a476bd4c5f0ad
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5248568"
---
# <a name="warehouse-management-overview"></a><span data-ttu-id="b4cf4-103">Varastonhallinnan yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="b4cf4-103">Warehouse management overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b4cf4-104">Varastonhallintamoduulin avulla voit hallita tuotanto-, jakelu- ja vähittäismyyntiyritysten varastoprosesseja.</span><span class="sxs-lookup"><span data-stu-id="b4cf4-104">The Warehouse management module lets you manage warehouse processes in manufacturing, distribution, and retail companies.</span></span> <span data-ttu-id="b4cf4-105">Moduulissa on useita ominaisuuksia varastolaitoksen optimaaliseksi tueksi milloin tahansa.</span><span class="sxs-lookup"><span data-stu-id="b4cf4-105">This module has a wide range of features to support the warehouse facility at an optimal level, at any time.</span></span> <span data-ttu-id="b4cf4-106">Varastonhallinta on täysin integroitu muihin liiketoimintaprosesseihin, kuten kuljetukseen, tuotantoon, laadunvalvontaan, hankintaan, siirtoon, myyntiin ja palautuksiin.</span><span class="sxs-lookup"><span data-stu-id="b4cf4-106">Warehouse management is fully integrated with other business processes such as transportation, manufacturing, quality control, purchase, transfer, sales, and returns.</span></span>

## <a name="get-started"></a><span data-ttu-id="b4cf4-107">Aloittaminen</span><span class="sxs-lookup"><span data-stu-id="b4cf4-107">Get started</span></span>
<span data-ttu-id="b4cf4-108">Varastonhallinnan käyttämiseksi sinun on määritettävä yleiset varastoparametrit tukemaan yrityksesi liiketoimintaprosesseja.</span><span class="sxs-lookup"><span data-stu-id="b4cf4-108">To start working with Warehouse management, you need to complete the setup of the general warehouse parameters to support the business processes of your company.</span></span>

- <span data-ttu-id="b4cf4-109">Siirry **Varastonhallinnan parametrit** -sivulle kohdassa **Varastonhallinta** > **Asetukset** määrittämään yleiset varastoparametrit.</span><span class="sxs-lookup"><span data-stu-id="b4cf4-109">Go to the **Warehouse management parameters** page under **Warehouse management** > **Setup** to set up general warehouse parameters.</span></span>

<span data-ttu-id="b4cf4-110">Määritä lähtevän ja saapuvan varastointiprosessien komponentit liiketoiminnan tarpeiden mukaisesti.</span><span class="sxs-lookup"><span data-stu-id="b4cf4-110">You must configure components for inbound and outbound warehouse process workflows according to business requirements.</span></span> <span data-ttu-id="b4cf4-111">Tärkeimmät määritettävät komponentit ovat aaltomallit, työmallit, työpoolit ja sijaintidirektiivit.</span><span class="sxs-lookup"><span data-stu-id="b4cf4-111">The most important components that you must configure are wave templates, work templates, work pools, and location directives.</span></span>

- [<span data-ttu-id="b4cf4-112">Varaston konfiguroinnin yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="b4cf4-112">Warehouse configuration overview</span></span>](warehouse-configuration.md)
- [<span data-ttu-id="b4cf4-113">Varastotyön valvonta työmallien ja sijaintidirektiivien avulla</span><span class="sxs-lookup"><span data-stu-id="b4cf4-113">Control warehouse work by using work templates and location directives</span></span>](control-warehouse-location-directives.md)
- [<span data-ttu-id="b4cf4-114">Varastotyön mobiililaitteiden määrittäminen</span><span class="sxs-lookup"><span data-stu-id="b4cf4-114">Set up mobile devices for warehouse work</span></span>](configure-mobile-devices-warehouse.md)
- [<span data-ttu-id="b4cf4-115">Määritä sijaintidirektiivi ostotilauksen poispanolle</span><span class="sxs-lookup"><span data-stu-id="b4cf4-115">Set up a location directive for purchase order put-away</span></span>](../transportation/tasks/set-up-location-directive-purchase-order-put-away.md)
- [<span data-ttu-id="b4cf4-116">Määritä työmalli ostotilauksia varten</span><span class="sxs-lookup"><span data-stu-id="b4cf4-116">Set up a work template for purchase orders</span></span>](./tasks/set-up-work-template-purchase-orders.md)

## <a name="warehouse-management-processes"></a><span data-ttu-id="b4cf4-117">Varastonhallinnan prosessit</span><span class="sxs-lookup"><span data-stu-id="b4cf4-117">Warehouse management processes</span></span>
- <span data-ttu-id="b4cf4-118">Integroitu tuki myyntitilausten, palautusten, siirtotilausten, tuotantotilausten ja kanbanien lähdeasiakirjoille</span><span class="sxs-lookup"><span data-stu-id="b4cf4-118">Integrated support for source documents for sales orders, returns, transfer orders, production orders, and kanban</span></span>  
- <span data-ttu-id="b4cf4-119">Joustava, kyselyihin perustuva saapuvan ja lähtevän materiaalin työnkulun tuki</span><span class="sxs-lookup"><span data-stu-id="b4cf4-119">Flexible, inbound and outbound material workflow support based on queries</span></span>
- <span data-ttu-id="b4cf4-120">Täysi integraatio Valmistus- ja Kuljetusratkaisujen tarjontaan</span><span class="sxs-lookup"><span data-stu-id="b4cf4-120">Full integration with the Manufacturing and Transportation offerings</span></span>
- <span data-ttu-id="b4cf4-121">Täysi hallinta sijaintien varastointirajoituksiin ja sijaintien tilavuustietoihin</span><span class="sxs-lookup"><span data-stu-id="b4cf4-121">Full control of location stocking limits and location volumetrics</span></span>
- <span data-ttu-id="b4cf4-122">Varastotilan mukaan hallittavat varaston ominaisuudet</span><span class="sxs-lookup"><span data-stu-id="b4cf4-122">Inventory properties controlled by inventory status</span></span>
- <span data-ttu-id="b4cf4-123">Täysi erä- ja sarjanimikkeiden tuki</span><span class="sxs-lookup"><span data-stu-id="b4cf4-123">Full batch and serial item support</span></span>
- <span data-ttu-id="b4cf4-124">Useita nimikkeen vastaanotto-ominaisuuksia</span><span class="sxs-lookup"><span data-stu-id="b4cf4-124">Various item receiving capabilities</span></span>
- <span data-ttu-id="b4cf4-125">Useita keräilystrategioita</span><span class="sxs-lookup"><span data-stu-id="b4cf4-125">Multiple picking strategies</span></span>
- <span data-ttu-id="b4cf4-126">Valmis tuki uuden sukupolven viivakoodinlukijoille</span><span class="sxs-lookup"><span data-stu-id="b4cf4-126">Out-of-the-box support for the next generation of barcode scanners</span></span>
- <span data-ttu-id="b4cf4-127">Kuormalava/konttityypit varastointiprosesseille</span><span class="sxs-lookup"><span data-stu-id="b4cf4-127">Pallet/container types for warehouse processes</span></span>
- <span data-ttu-id="b4cf4-128">Laajennetut laskentaominaisuudet</span><span class="sxs-lookup"><span data-stu-id="b4cf4-128">Advanced counting capabilities</span></span>
- <span data-ttu-id="b4cf4-129">Etikettien tulostus ja reititys Zebra ZPL -tuella</span><span class="sxs-lookup"><span data-stu-id="b4cf4-129">Label printing and label routing with Zebra ZPL support</span></span>
- <span data-ttu-id="b4cf4-130">Business Intelligence -integrointi Power BI:hin</span><span class="sxs-lookup"><span data-stu-id="b4cf4-130">Business intelligence integration into Power BI</span></span>
- <span data-ttu-id="b4cf4-131">Manuaalinen ja automaattinen varaston siirtäminen</span><span class="sxs-lookup"><span data-stu-id="b4cf4-131">Manual and automatic movement of inventory</span></span>
- <span data-ttu-id="b4cf4-132">Täysin integroitu laadunvalvonta (QMS)</span><span class="sxs-lookup"><span data-stu-id="b4cf4-132">Fully-integrated quality control (QMS)</span></span>
- <span data-ttu-id="b4cf4-133">Työntekijöiden materiaalikäsittelyn täysi seurattavuus</span><span class="sxs-lookup"><span data-stu-id="b4cf4-133">Full traceability of workers' material handling</span></span>
- <span data-ttu-id="b4cf4-134">Lähtevän aallon käsittely</span><span class="sxs-lookup"><span data-stu-id="b4cf4-134">Outbound wave processing</span></span>
- <span data-ttu-id="b4cf4-135">Manuaalisen pakkauksen ja automaattisen konttiinpakkauksen tuki</span><span class="sxs-lookup"><span data-stu-id="b4cf4-135">Manual packing and automatic containerization support</span></span>
- <span data-ttu-id="b4cf4-136">Klusterin keräily</span><span class="sxs-lookup"><span data-stu-id="b4cf4-136">Cluster picking</span></span>
- <span data-ttu-id="b4cf4-137">Yksinkertainen cross docking</span><span class="sxs-lookup"><span data-stu-id="b4cf4-137">Simple cross docking</span></span>

## <a name="additional-resources"></a><span data-ttu-id="b4cf4-138">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="b4cf4-138">Additional resources</span></span>
### <a name="whats-new-and-in-development"></a><span data-ttu-id="b4cf4-139">Uudet ja kehitteillä olevat toiminnot</span><span class="sxs-lookup"><span data-stu-id="b4cf4-139">What's new and in development</span></span>
<span data-ttu-id="b4cf4-140">[Microsoft Dynamics 365 Tiekartta](https://roadmap.dynamics.com/) -sivustossa on lisätietoja julkaistuista ja kehitteillä olevista uusista toiminnoista.</span><span class="sxs-lookup"><span data-stu-id="b4cf4-140">Go to the [Microsoft Dynamics 365 Roadmap](https://roadmap.dynamics.com/) to see what new features have been released and what new features are in development.</span></span>

### <a name="blogs"></a><span data-ttu-id="b4cf4-141">Blogit</span><span class="sxs-lookup"><span data-stu-id="b4cf4-141">Blogs</span></span>
<span data-ttu-id="b4cf4-142">[Microsoft Dynamics 365 -blogissa](https://community.dynamics.com/b/msftdynamicsblog) on varastonhallintaa ja muita ratkaisuja koskevia mielipiteitä, uutisia ja muita tietoja.</span><span class="sxs-lookup"><span data-stu-id="b4cf4-142">You can find opinions, news, and other information about Warehouse management and other solutions on the [Microsoft Dynamics 365 blog](https://community.dynamics.com/b/msftdynamicsblog).</span></span>


 



[!INCLUDE[footer-include](../../includes/footer-banner.md)]