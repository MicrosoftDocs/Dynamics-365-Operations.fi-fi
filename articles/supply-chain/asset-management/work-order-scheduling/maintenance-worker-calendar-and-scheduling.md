---
title: Kunnossapitotyöntekijän kalenteri ja ajoittaminen
description: Tässä aiheessa selitetään kunnossapitotyöntekijän kalenterista suhteessa resurssienhallinnan aikataulutukseen.
author: josaw1
manager: AnnBe
ms.date: 08/19/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 3f86f6475e5226443f5e4d43fb91acafe2afdbb9
ms.sourcegitcommit: f93ead945afe5ae18706c66bce6e64a6b57aac50
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/19/2019
ms.locfileid: "1887385"
---
# <a name="maintenance-worker-calendar-and-scheduling"></a><span data-ttu-id="d793a-103">Kunnossapitotyöntekijän kalenteri ja ajoittaminen</span><span class="sxs-lookup"><span data-stu-id="d793a-103">Maintenance worker calendar and scheduling</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="d793a-104">Kun ajoitat työtilauksia, luot aikataulun huoltotyöntekijöille, työkaluille ja resursseille.</span><span class="sxs-lookup"><span data-stu-id="d793a-104">When you schedule work orders, you create a schedule for maintenance workers, tools, and assets.</span></span> <span data-ttu-id="d793a-105">Huoltotyöntekijöille on määritettävä kalenteri kullekin kunnossapitotyöntekijälle, jotta ne voidaan ajoittaa.</span><span class="sxs-lookup"><span data-stu-id="d793a-105">In order to carry out scheduling on maintenance workers, a calendar must be set up for each maintenance worker.</span></span> <span data-ttu-id="d793a-106">Kunnossapitotyöntekijät liittyvät resurssiin, ja työaikakalenterit määritetään resursseihin.</span><span class="sxs-lookup"><span data-stu-id="d793a-106">Maintenance workers are related to a resource, and working time calendars are set up on resoures.</span></span> <span data-ttu-id="d793a-107">Voit määrittää työntekijään liittyvän resurssin ja kalenterin kohdassa**Resurssien hallinta** > **Asetukset** > **Työntekijät** >  **Työntekijät**, joka on kuvattu kohdassa [Huoltotyöntekijät ja työntekijäryhmät](../setup-for-objects/workers-and-worker-groups.md).</span><span class="sxs-lookup"><span data-stu-id="d793a-107">You set up the resource and calendar related to a worker in **Asset management** > **Setup** > **Workers** > **Workers**, which is described in [Maintenance workers and worker groups](../setup-for-objects/workers-and-worker-groups.md).</span></span>

<span data-ttu-id="d793a-108">Alla oleva kuvakaappaus näyttää esimerkin huoltotyöntekijästä, joka liittyy työaikakalenteria Tuotanto käyttävään resurssiin.</span><span class="sxs-lookup"><span data-stu-id="d793a-108">The screenshot below shows an example of a maintenance worker who is related to a resource that uses the working time calendar "Production".</span></span>

![Kuva 1](media/01-work-order-scheduling.png)

<span data-ttu-id="d793a-110">Työkalujen ja resurssien kalenteriasetuksia ei tarvita suhteessa työtilausten suunnitteluun.</span><span class="sxs-lookup"><span data-stu-id="d793a-110">Calendar setup for tools and assets is not needed in relation to work order scheduling.</span></span> <span data-ttu-id="d793a-111">Oletus on, että työkalut ja resurssit ovat käytettävissä 24 tuntia vuorokaudessa huoltoa varten.</span><span class="sxs-lookup"><span data-stu-id="d793a-111">The assumption is that tools and assets are available 24 hours a day for maintenance.</span></span>

