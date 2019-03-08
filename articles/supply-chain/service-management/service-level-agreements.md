---
title: Palvelutasosopimukset
description: Palvelutasosopimuksessa asiakas hyväksyy huoltoyrityksen ongelman vastaanottamiseen ja ongelman ratkaisuun perustuvan vähimmäisvasteajan.
author: ShylaThompson
manager: AnnBe
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAServicelevelagreement
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: cffe3a7766502dd5d888a7a99a32150967911301
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/29/2019
ms.locfileid: "364577"
---
# <a name="service-level-agreements"></a><span data-ttu-id="1a60d-103">Palvelutasosopimukset</span><span class="sxs-lookup"><span data-stu-id="1a60d-103">Service level agreements</span></span>        

[!include [banner](../includes/banner.md)]


<span data-ttu-id="1a60d-104">Palvelutasosopimus on huoltoyhtiön ja huoltoasiakkaan välinen sopimus.</span><span class="sxs-lookup"><span data-stu-id="1a60d-104">A service level agreement (SLA) is an agreement between a service company and a service customer.</span></span> <span data-ttu-id="1a60d-105">Palvelutasosopimuksessa asiakas hyväksyy huoltoyrityksen ongelman vastaanottamiseen ja ongelman ratkaisuun perustuvan vähimmäisvasteajan.</span><span class="sxs-lookup"><span data-stu-id="1a60d-105">In a SLA, the customer agrees to a minimum response time based on when the service company records the issue and when the issue is resolved.</span></span>

<span data-ttu-id="1a60d-106">Palvelutasosopimus määrittää asiakkaille tarjottavan vakiopalveluntason. Sopimus myös ilmaisee huoltoyritykselle selkeästi huoltotyön valmistumisajankohdan.</span><span class="sxs-lookup"><span data-stu-id="1a60d-106">A SLA enforces a standard level of service that is offered to customers, and also makes it transparent to a service company when a service job should be completed.</span></span>

<span data-ttu-id="1a60d-107">Palvelusopimuksia voidaan tehdä haluttu määrä, jotta huoltoasiakkaille voidaan tarjota eri tasoisia palveluita.</span><span class="sxs-lookup"><span data-stu-id="1a60d-107">Any number of SLAs can be created to offer service customers different levels of service.</span></span>

## <a name="create-a-service-level-agreement"></a><span data-ttu-id="1a60d-108">Palvelutasosopimuksen luominen</span><span class="sxs-lookup"><span data-stu-id="1a60d-108">Create a service level agreement</span></span>

1.  <span data-ttu-id="1a60d-109">Valitse **Huoltohallinta** \> **Asetukset** \> **Huoltosopimukset** \> **Palvelutasosopimukset**.</span><span class="sxs-lookup"><span data-stu-id="1a60d-109">Click **Service management** \> **Setup** \> **Service agreements** \> **Service level agreements**.</span></span>

2.  <span data-ttu-id="1a60d-110">Kirjoita palvelutasosopimuksen nimi **Palvelutasosopimus**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="1a60d-110">Type a name for the service level agreement in the **Service level agreement** field.</span></span>

3.  <span data-ttu-id="1a60d-111">Kirjoita aika, jonka haluat sallia huoltopyynnöille, jotka liittyvät palvelutasosopimukseen.</span><span class="sxs-lookup"><span data-stu-id="1a60d-111">Type the time that you want to allow for completion of service calls that are attached to the service level agreement.</span></span> <span data-ttu-id="1a60d-112">Valitse sitten kalenteri, jos haluat palvelutasosopimuksen perustuvan tiettyyn kalenteriin.</span><span class="sxs-lookup"><span data-stu-id="1a60d-112">Then select a calendar if you want to base the service level agreement on a specific calendar.</span></span>

## <a name="apply-a-service-level-agreement"></a><span data-ttu-id="1a60d-113">Palvelutasosopimuksen kohdistaminen</span><span class="sxs-lookup"><span data-stu-id="1a60d-113">Apply a service level agreement</span></span>

<span data-ttu-id="1a60d-114">Palvelutasosopimus kohdistetaan suoraan huoltosopimukseen.</span><span class="sxs-lookup"><span data-stu-id="1a60d-114">The SLA is applied directly to a service agreement.</span></span>

<span data-ttu-id="1a60d-115">Manuaalisesti luotavat ja huoltosopimukseen palvelutasosopimuksen avulla liitettävät huoltotilaukset arvioidaan kyseisen palvelutasosopimuksen avulla.</span><span class="sxs-lookup"><span data-stu-id="1a60d-115">Service orders that you create manually and attach to a service agreement that has an SLA are measured against that SLA.</span></span>

<span data-ttu-id="1a60d-116">Automaattisesti luotavia huoltotilauksia ei liitetä palvelutasosopimukseen.</span><span class="sxs-lookup"><span data-stu-id="1a60d-116">Service orders that you create automatically are not attached to an SLA.</span></span>

## <a name="apply-the-service-level-agreement-to-the-service-agreement"></a><span data-ttu-id="1a60d-117">Palvelutasosopimuksen kohdistaminen huoltosopimukseen</span><span class="sxs-lookup"><span data-stu-id="1a60d-117">Apply the service level agreement to the service agreement</span></span>

1.  <span data-ttu-id="1a60d-118">Valitse **Palvelunhallinta** \> **Yleinen** \> **Palvelusopimukset** \> **Palvelusopimukset**.</span><span class="sxs-lookup"><span data-stu-id="1a60d-118">Click **Service management** \> **Common** \> **Service agreements** \> **Service agreements**.</span></span> <span data-ttu-id="1a60d-119">Valitse huoltosopimus, jota haluat käyttää palvelutasosopimuksessa, ja valitse sitten **Muokkaa** **toimintoruudussa**.</span><span class="sxs-lookup"><span data-stu-id="1a60d-119">Select the service agreement that you want to apply the SLA to, and then click **Edit** on the **Action Pane**.</span></span>

2.  <span data-ttu-id="1a60d-120">Valitse **Palvelutasosopimus**-kentässä palvelutasosopimus, joka liitetään.</span><span class="sxs-lookup"><span data-stu-id="1a60d-120">In the **Service level agreement** field, select the SLA that you want to assign.</span></span>

## <a name="apply-the-service-level-agreement-to-the-service-agreement-group"></a><span data-ttu-id="1a60d-121">Palvelutasosopimuksen kohdistaminen huoltosopimusryhmään</span><span class="sxs-lookup"><span data-stu-id="1a60d-121">Apply the service level agreement to the service agreement group</span></span>

1.  <span data-ttu-id="1a60d-122">Valitse **Palvelunhallinta** \> **Asetukset** \> **Huoltosopimukset** \> **Huoltosopimusryhmät**.</span><span class="sxs-lookup"><span data-stu-id="1a60d-122">Click **Service management** \> **Setup** \> **Service agreements** \> **Service agreement groups**.</span></span>

2.  <span data-ttu-id="1a60d-123">Valitse **Palvelutasosopimus**-kentässä palvelutasosopimus, joka liitetään.</span><span class="sxs-lookup"><span data-stu-id="1a60d-123">In the **Service level agreement** field, select the SLA that you want to assign.</span></span>

## <a name="track-time-on-a-service-order-against-an-sla"></a><span data-ttu-id="1a60d-124">Huoltotilaukseen kuluvan ajan seuraaminen palvelutasosopimuksen mukaan</span><span class="sxs-lookup"><span data-stu-id="1a60d-124">Track time on a service order against an SLA</span></span>

<span data-ttu-id="1a60d-125">Luodessasi uuden huoltotilauksen huoltosopimukseen, johon palvelutasosopimus on liitetty, huollon toimituksen aikaväli alkaa ja järjestelmä alkaa seurata toimitusaikaa.</span><span class="sxs-lookup"><span data-stu-id="1a60d-125">When you create a new service order for a service agreement that an SLA is assigned to, the time interval for the delivery of the service is initiated, and the system starts to track the delivery time.</span></span> <span data-ttu-id="1a60d-126">Lisäksi voit määrittää seuraavat asetukset:</span><span class="sxs-lookup"><span data-stu-id="1a60d-126">Additionally, you can set the following options:</span></span>

  - <span data-ttu-id="1a60d-127">Voit käynnistää ja pysäyttää huoltotilauksen ajanoton, kun haluat rekisteröidä huoltotilauksiin kuluneen kokonaisajan.</span><span class="sxs-lookup"><span data-stu-id="1a60d-127">You can start and stop time recording on the service order to register the total amount of time that is spent on service orders.</span></span>

  - <span data-ttu-id="1a60d-128">Voit seurata yhteensopivuutta palvelutasosopimuksessa määritetyllä aikavälillä.</span><span class="sxs-lookup"><span data-stu-id="1a60d-128">You can monitor compliance with the time interval that is set in the service level agreement.</span></span>

  - <span data-ttu-id="1a60d-129">Voit määrittää syykoodit, jotka on määritettävä, jos palvelutasosopimuksen aikaväli ylitetään.</span><span class="sxs-lookup"><span data-stu-id="1a60d-129">You can define reason codes that must be set if the time interval of the service level agreement is exceeded.</span></span>

## <a name="see-also"></a><span data-ttu-id="1a60d-130">Lisätietoja</span><span class="sxs-lookup"><span data-stu-id="1a60d-130">See also</span></span>

[<span data-ttu-id="1a60d-131">Palvelutasosopimusten yhteensopivuuden tarkasteleminen</span><span class="sxs-lookup"><span data-stu-id="1a60d-131">View compliance with service level agreements</span></span>](view-compliance-with-service-level-agreements.md)

  


