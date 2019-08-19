---
title: Huoltohallinta
description: Huoltohallinta-toimintoa käytetään tekemään huoltosopimuksia ja huollon ylläpitosopimuksia, käsittelemään huoltotilauksia ja asiakaskyselyitä, sekä hallinnoimaan ja analysoimaan huoltotoimituksia asiakkaille.
author: ShylaThompson
manager: AnnBe
ms.date: 05/24/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAServiceOrderTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b2fc5361b1b30db29789ff67b56a15eb66a919f5
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/01/2019
ms.locfileid: "1843286"
---
# <a name="service-management"></a><span data-ttu-id="a7d00-103">Huoltohallinta</span><span class="sxs-lookup"><span data-stu-id="a7d00-103">Service management</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="a7d00-104">**Huoltohallinta**-toimintoa käytetään tekemään huoltosopimuksia ja huollon ylläpitosopimuksia, käsittelemään huoltotilauksia ja asiakaskyselyitä, sekä hallinnoimaan ja analysoimaan huoltotoimituksia asiakkaille.</span><span class="sxs-lookup"><span data-stu-id="a7d00-104">Use **Service management** to establish service agreements and service subscriptions, handle service orders and customer inquiries, and to manage and analyze the delivery of services to customers.</span></span> <span data-ttu-id="a7d00-105">Voit käyttää palvelusopimuksia määrittämään tavallisessa palveluluettelossa käytettäviä resursseja.</span><span class="sxs-lookup"><span data-stu-id="a7d00-105">You can use service agreements to define the resources that are used in a typical service visit.</span></span> <span data-ttu-id="a7d00-106">Huoltosopimusten avulla voit tarkastella, miten nämä resurssit laskutetaan asiakkaalta.</span><span class="sxs-lookup"><span data-stu-id="a7d00-106">You can also use service agreements to view how those resources are invoiced to the customer.</span></span> <span data-ttu-id="a7d00-107">Huoltosopimus voidaan myös sisällyttää palvelutasosopimukseen, jossa määritetään normaali vasteaika ja tarjotaan työkalut todellisen ajan kirjaamiseen.</span><span class="sxs-lookup"><span data-stu-id="a7d00-107">A service agreement can also include a service level agreement that specifies standard response times, and offers tools to record the actual time.</span></span>

<span data-ttu-id="a7d00-108">Voit luoda huoltotilauksia hallitsemaan tietoja ajoitetuista ja ajoittamattomista käynneistä, jotka huoltoteknikko tekee asiakkaan toimipaikassa.</span><span class="sxs-lookup"><span data-stu-id="a7d00-108">You can create service orders to manage information about scheduled and unscheduled visits by a service technician to a customer site.</span></span> <span data-ttu-id="a7d00-109">Huoltotilauksiin kuuluu tietoja, kuten:</span><span class="sxs-lookup"><span data-stu-id="a7d00-109">Service orders include information such as:</span></span>

1.  <span data-ttu-id="a7d00-110">Työtunnit, jotka huoltoteknikko suorittaa</span><span class="sxs-lookup"><span data-stu-id="a7d00-110">The hours of work that the service technician will perform</span></span>

2.  <span data-ttu-id="a7d00-111">Palvelun tai korjauksen tyyppi</span><span class="sxs-lookup"><span data-stu-id="a7d00-111">The type of service or repair</span></span>

3.  <span data-ttu-id="a7d00-112">Korjattava nimike, mukaan lukien tiedot oireista ja diagnoosi</span><span class="sxs-lookup"><span data-stu-id="a7d00-112">The item to repair, including details about the symptoms and diagnosis</span></span>

4.  <span data-ttu-id="a7d00-113">Kaikki kulut ja maksut, jotka liittyvät palveluun tai huoltoon</span><span class="sxs-lookup"><span data-stu-id="a7d00-113">Any expenses and fees related to the service or repair</span></span>

<span data-ttu-id="a7d00-114">Voit vastaanottaa, käsitellä ja resursoida palvelupyyntöjä.</span><span class="sxs-lookup"><span data-stu-id="a7d00-114">You can receive, process, and dispatch service requests.</span></span> <span data-ttu-id="a7d00-115">Kun olet luonut huoltotilauksen, voit valvoa edistymistä huoltovaiheiden avulla sekä määrittää sääntöjä, jotka ohjaavat kussakin vaiheessa käytössä olevia toimintoja.</span><span class="sxs-lookup"><span data-stu-id="a7d00-115">After you have created a service order, you can use service stages to monitor progress and specify rules that control what actions are enabled in each stage.</span></span> <span data-ttu-id="a7d00-116">Kun huoltotilaus on valmis, voit hyväksyä tilauksen vahvistaaksesi, että se on valmis ja kirjata sitten tilauksen laskutusprosessin käynnistämiseksi.</span><span class="sxs-lookup"><span data-stu-id="a7d00-116">When a service order is complete, you can sign off on the order to confirm that it is complete, and then post the order to start the invoice process.</span></span>

<span data-ttu-id="a7d00-117">Käytä raportointityökaluja huoltotilausten marginaalien ja ylläpitosopimustapahtumien valvontaan sekä työmääräinten ja työn vastaanottokuittausten tulostamiseen.</span><span class="sxs-lookup"><span data-stu-id="a7d00-117">Use the reporting tools to monitor service order margins and subscription transactions, and print work descriptions and work receipts.</span></span>

## <a name="business-processes"></a><span data-ttu-id="a7d00-118">Liiketoimintaprosessit</span><span class="sxs-lookup"><span data-stu-id="a7d00-118">Business processes</span></span>

<span data-ttu-id="a7d00-119">Seuraavassa kaaviossa on kuvattu **huoltohallinnan** korkean tason liiketoimintaprosessit, ja se näyttää, missä huoltoprosessit integroituvat muiden Microsoft Dynamics 365 for Finance and Operations -moduulien kanssa.</span><span class="sxs-lookup"><span data-stu-id="a7d00-119">The following diagram illustrates the high level business processes for **Service management**, and shows where service processes integrate with other modules in Microsoft Dynamics 365 for Finance and Operations.</span></span>

<span data-ttu-id="a7d00-120">[![Huoltohallinta-moduulin liiketoimintaprosessikaavio](./media/sm_home_page.gif)](./media/sm_home_page.gif)</span><span class="sxs-lookup"><span data-stu-id="a7d00-120">[![Service management business process diagram](./media/sm_home_page.gif)](./media/sm_home_page.gif)</span></span>

## <a name="service-management-at-a-glance"></a><span data-ttu-id="a7d00-121">Palveluhallinnan esittely</span><span class="sxs-lookup"><span data-stu-id="a7d00-121">Service management at a glance</span></span>

|<span data-ttu-id="a7d00-122">Tärkeät tehtävät</span><span class="sxs-lookup"><span data-stu-id="a7d00-122">Important tasks</span></span>           | <span data-ttu-id="a7d00-123">Ensisijaiset sivut</span><span class="sxs-lookup"><span data-stu-id="a7d00-123">Primary pages</span></span>                         |<span data-ttu-id="a7d00-124">Suositut raportit</span><span class="sxs-lookup"><span data-stu-id="a7d00-124">Popular reports</span></span>              |
|--------------------------|---------------------------------------|-----------------------------|
|<span data-ttu-id="a7d00-125">Huoltosopimusten täyttäminen</span><span class="sxs-lookup"><span data-stu-id="a7d00-125">Fulfill service agreements</span></span>|<span data-ttu-id="a7d00-126">Huoltosopimukset</span><span class="sxs-lookup"><span data-stu-id="a7d00-126">Service agreements</span></span>                     |<span data-ttu-id="a7d00-127">Huoltotilauksen marginaali</span><span class="sxs-lookup"><span data-stu-id="a7d00-127">Service order margin</span></span>         |
|<span data-ttu-id="a7d00-128">Käsittele asiakkaan kyselyt</span><span class="sxs-lookup"><span data-stu-id="a7d00-128">Handle customer inquiries</span></span> |<span data-ttu-id="a7d00-129">Huoltotilaukset</span><span class="sxs-lookup"><span data-stu-id="a7d00-129">Service orders</span></span>                         |<span data-ttu-id="a7d00-130">Työmääräin</span><span class="sxs-lookup"><span data-stu-id="a7d00-130">Work description</span></span>             |
|                          |<span data-ttu-id="a7d00-131">Resursointitaulu</span><span class="sxs-lookup"><span data-stu-id="a7d00-131">Dispatch board</span></span>                         |<span data-ttu-id="a7d00-132">Tapahtuma - ylläpitosopimus</span><span class="sxs-lookup"><span data-stu-id="a7d00-132">Transaction - subscription</span></span>   |
|                          |                                       |<span data-ttu-id="a7d00-133">Ylläpitosopimusmaksutapahtumat</span><span class="sxs-lookup"><span data-stu-id="a7d00-133">Subscription fee transactions</span></span>|


## <a name="integration-of-service-management"></a><span data-ttu-id="a7d00-134">Palvelun hallinnan integrointi</span><span class="sxs-lookup"><span data-stu-id="a7d00-134">Integration of Service management</span></span>

<span data-ttu-id="a7d00-135">Palvelunhallinta voidaan integroida seuraavien moduulien kanssa sovelluksessa:</span><span class="sxs-lookup"><span data-stu-id="a7d00-135">Service management can be integrated with the following modules:</span></span>

  - [<span data-ttu-id="a7d00-136">Myynti ja markkinointi</span><span class="sxs-lookup"><span data-stu-id="a7d00-136">Sales and marketing</span></span>](../sales-marketing/overview-sales-marketing.md)
  - [<span data-ttu-id="a7d00-137">Henkilöstö</span><span class="sxs-lookup"><span data-stu-id="a7d00-137">Human resources</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/talent/index)

  

