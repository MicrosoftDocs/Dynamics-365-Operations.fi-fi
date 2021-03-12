---
title: Huoltosopimusten laatiminen ja luominen – yleiskatsaus
description: Huoltosopimuksessa voi määrittää tavallisella huoltokäynnillä käytettävät resurssit. Voit myös määrittää, miten nämä resurssit laskutetaan asiakkaalta.
author: ShylaThompson
manager: tfehr
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAAgreementTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3b6c83f5ecd29bbd4202014992277c9ba1ae41ec
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/15/2021
ms.locfileid: "4996522"
---
# <a name="develop-and-establish-service-agreements-overview"></a><span data-ttu-id="fe0f1-103">Huoltosopimusten laatiminen ja luominen – yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="fe0f1-103">Develop and establish service agreements overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="fe0f1-104">Huoltosopimuksessa voi määrittää tavallisella huoltokäynnillä käytettävät resurssit. Voit myös määrittää, miten nämä resurssit laskutetaan asiakkaalta.</span><span class="sxs-lookup"><span data-stu-id="fe0f1-104">Service agreements let you define the resources that are used in a typical service visit and how those resources are invoiced to the customer.</span></span>

<span data-ttu-id="fe0f1-105">Kukin huoltosopimus liitetään projektiin, jonka kautta tapahtumat kirjataan ja laskutetaan.</span><span class="sxs-lookup"><span data-stu-id="fe0f1-105">Every service agreement is attached to a project through which transactions are posted and invoiced.</span></span> <span data-ttu-id="fe0f1-106">Voit kuitenkin laskuttaa huoltotilaustapahtumia myös suoraan projektin kautta ilman, että huoltotilaus on ensin liitettävä huoltosopimukseen.</span><span class="sxs-lookup"><span data-stu-id="fe0f1-106">However, you can also invoice service order transactions directly through the project without first having to connect the service order to a service agreement.</span></span> <span data-ttu-id="fe0f1-107">Näin voidaan menetellä esimerkiksi silloin, kun huoltotilaus luodaan kertaluontoista huoltokäyntiä varten ja huoltotapahtumien nopea käsittely on tärkeämpää kuin asiakkaan yksityiskohtaisten huoltosopimustietojen ylläpito.</span><span class="sxs-lookup"><span data-stu-id="fe0f1-107">You might decide to do this if the service order is for a one-time-only service visit and the need for processing the service transactions quickly outweighs the need for maintaining detailed service-agreement information about the customer over a period of time.</span></span>

## <a name="service-agreement"></a><span data-ttu-id="fe0f1-108">Huoltosopimus</span><span class="sxs-lookup"><span data-stu-id="fe0f1-108">Service agreement</span></span>

<span data-ttu-id="fe0f1-109">Jokaisessa huoltosopimuksessa on määritettävä huoltosopimuksen tunnus ja ryhmä.</span><span class="sxs-lookup"><span data-stu-id="fe0f1-109">In each service agreement, you must specify a project, a service-agreement ID, and a service-agreement group.</span></span> <span data-ttu-id="fe0f1-110">Huoltosopimusryhmän avulla voidaan lajitella ja järjestää huoltosopimuksia.</span><span class="sxs-lookup"><span data-stu-id="fe0f1-110">The service-agreement group can be used to sort and organize service agreements.</span></span>

<span data-ttu-id="fe0f1-111">Huoltosopimuksen otsikon asetukset koskevat kaikkia sopimusrivejä:</span><span class="sxs-lookup"><span data-stu-id="fe0f1-111">A service agreement header contains settings that apply to all attached agreement lines:</span></span>

-  <span data-ttu-id="fe0f1-112">Keskeytetäänkö huoltosopimus.</span><span class="sxs-lookup"><span data-stu-id="fe0f1-112">Whether the service agreement is suspended.</span></span> <span data-ttu-id="fe0f1-113">Jos huoltosopimus keskeytetään, et voi luoda huoltotilauksia huoltosopimuksesta.</span><span class="sxs-lookup"><span data-stu-id="fe0f1-113">If the service agreement is suspended, you cannot generate service orders from the service agreement.</span></span>
-  <span data-ttu-id="fe0f1-114">Huoltosopimuksen kesto.</span><span class="sxs-lookup"><span data-stu-id="fe0f1-114">The duration of the service agreement.</span></span>
-  <span data-ttu-id="fe0f1-115">Miten huoltotilausrivit yhdistetään huoltotilauksiksi.</span><span class="sxs-lookup"><span data-stu-id="fe0f1-115">How service-order lines are to be combined into service orders.</span></span>
-  <span data-ttu-id="fe0f1-116">Onko huoltosopimus malli.</span><span class="sxs-lookup"><span data-stu-id="fe0f1-116">Whether the service agreement is a template.</span></span>

<span data-ttu-id="fe0f1-117">Huoltosopimuksen otsikossa määritetään myös huoltokohteet ja huoltotehtävät, joita voidaan käyttää huoltosopimuksessa. Se tehdään antamalla tietyt huoltotehtävät tai huoltokohteet, jotka on liitetty sopimuksen eri riveille.</span><span class="sxs-lookup"><span data-stu-id="fe0f1-117">In the service-agreement header, you also set up all the service objects and service tasks that can be used with the service agreement by entering the specific service tasks or service objects that are to be attached to the various lines of the agreement.</span></span>

<span data-ttu-id="fe0f1-118">Huoltosopimuksen otsikosta voidaan kopioida huoltosopimusrivejä tai huoltomallirivejä nykyiseen huoltosopimukseen.</span><span class="sxs-lookup"><span data-stu-id="fe0f1-118">From the service-agreement header, you can also copy service-agreement lines or service-template lines into the current service agreement.</span></span>

<span data-ttu-id="fe0f1-119">Voit keskeyttää huoltosopimuksia ja pysäyttää yksittäisiä huoltosopimusrivejä.</span><span class="sxs-lookup"><span data-stu-id="fe0f1-119">You can suspend service agreements and stop individual service agreement lines.</span></span>

<span data-ttu-id="fe0f1-120">Jos valitset huoltosopimuksessa **Keskeytetty**-valintaruudun, et voi</span><span class="sxs-lookup"><span data-stu-id="fe0f1-120">If you select the **Suspended** check box on a service agreement, you cannot:</span></span>

-    <span data-ttu-id="fe0f1-121">luoda huoltotilauksia automaattisesti tai manuaalisesti huoltosopimuksessa.</span><span class="sxs-lookup"><span data-stu-id="fe0f1-121">Create service orders automatically or manually from the service agreement.</span></span>

<span data-ttu-id="fe0f1-122">Jos valitset huoltosopimusrivillä **Pysäytetty**-valintaruudun, et voi</span><span class="sxs-lookup"><span data-stu-id="fe0f1-122">If you select the **Stopped** check box on a service agreement line, you cannot:</span></span>

-    <span data-ttu-id="fe0f1-123">luoda huoltotilauksia automaattisesti tai manuaalisesti huoltosopimusrivillä</span><span class="sxs-lookup"><span data-stu-id="fe0f1-123">Create service orders automatically or manually from the service agreement line.</span></span>
-    <span data-ttu-id="fe0f1-124">kopioida huoltosopimusriviä toiseen huoltosopimukseen tai toiselle huoltosopimusriville.</span><span class="sxs-lookup"><span data-stu-id="fe0f1-124">Copy the service agreement line into another service agreement or service order.</span></span>


> [!NOTE]
> <span data-ttu-id="fe0f1-125">Jos huoltosopimus keskeytetään, kaikki siihen liittyvät rivit pysäytetään niiden yksittäisistä tiloista riippumatta.</span><span class="sxs-lookup"><span data-stu-id="fe0f1-125">If a service agreement is suspended, all the attached lines are stopped, regardless of their individual status.</span></span>

## <a name="service-agreement-lines"></a><span data-ttu-id="fe0f1-126">Huoltosopimuksen rivit</span><span class="sxs-lookup"><span data-stu-id="fe0f1-126">Service-agreement lines</span></span>

<span data-ttu-id="fe0f1-127">Kullakin huoltosopimusrivillä kuvataan tarkasti ehdotetun huoltotyön sisältö.</span><span class="sxs-lookup"><span data-stu-id="fe0f1-127">Each service-agreement line describes in detail the content of the proposed service work.</span></span> <span data-ttu-id="fe0f1-128">Rivit sisältävät seuraavat asetukset:</span><span class="sxs-lookup"><span data-stu-id="fe0f1-128">The lines contain the following settings:</span></span>

-  <span data-ttu-id="fe0f1-129">Tapahtumatyyppi ja tapahtumatyypin kuvaus.</span><span class="sxs-lookup"><span data-stu-id="fe0f1-129">The transaction type and the description of the transaction type.</span></span>
-  <span data-ttu-id="fe0f1-130">Työntekijä, joka suorittaa huoltotyön.</span><span class="sxs-lookup"><span data-stu-id="fe0f1-130">The employee who performs the service work.</span></span>
-  <span data-ttu-id="fe0f1-131">Huoltosopimuksen kohteet, jotka on huollettava.</span><span class="sxs-lookup"><span data-stu-id="fe0f1-131">The objects on which service must be performed for the service agreement.</span></span>
-  <span data-ttu-id="fe0f1-132">Työn suoritustiheys sekä nimike-, kulu- ja maksutapahtumien kirjaustiheys.</span><span class="sxs-lookup"><span data-stu-id="fe0f1-132">The frequency with which work is performed and associated item, expense, and fee transactions are registered.</span></span>
-  <span data-ttu-id="fe0f1-133">Aikaikkuna, jonka sisällä huoltotilausrivit voidaan ryhmitellä huoltotilaukseksi.</span><span class="sxs-lookup"><span data-stu-id="fe0f1-133">The time window within which service-order lines can be grouped into a service order.</span></span>
-  <span data-ttu-id="fe0f1-134">Huoltotehtävät, joiden avulla sopimusrivien joukko ryhmitellään työtehtäviksi ja joissa on huoltoteknikoille ja asiakkaille yhteenveto suoritettavista huoltotehtävistä.</span><span class="sxs-lookup"><span data-stu-id="fe0f1-134">The service tasks that are used to group sets of agreement lines together into work tasks and to summarize for service technicians and customers what service task is to be provided.</span></span>
-  <span data-ttu-id="fe0f1-135">Pysäytetäänkö rivi.</span><span class="sxs-lookup"><span data-stu-id="fe0f1-135">Whether a line is stopped.</span></span> <span data-ttu-id="fe0f1-136">Jos rivi pysäytetään, et voi luoda huoltotilauksia kyseiselle riville.</span><span class="sxs-lookup"><span data-stu-id="fe0f1-136">If a line is stopped, you cannot create service orders for that individual line.</span></span>
-  <span data-ttu-id="fe0f1-137">Projektiasetukset, kuten luokka ja riviominaisuus.</span><span class="sxs-lookup"><span data-stu-id="fe0f1-137">Project settings, such as the category and the line property.</span></span>

## <a name="related-topics"></a><span data-ttu-id="fe0f1-138">Liittyvät aiheet</span><span class="sxs-lookup"><span data-stu-id="fe0f1-138">Related topics</span></span>

[<span data-ttu-id="fe0f1-139">Huoltosopimusten luominen</span><span class="sxs-lookup"><span data-stu-id="fe0f1-139">Create service agreements</span></span>](create-service-agreements.md)
