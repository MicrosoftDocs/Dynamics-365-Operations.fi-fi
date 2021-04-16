---
title: Kunnossapitotyöntekijän kalenteri ja ajoittaminen
description: Tässä aiheessa selitetään kunnossapitotyöntekijän kalenterista suhteessa resurssienhallinnan aikataulutukseen.
author: johanhoffmann
ms.date: 08/19/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EntAssetWorker
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: e1abf029e6f72c1c6a827a00483bb34c4abcaec5
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/01/2021
ms.locfileid: "5808133"
---
# <a name="maintenance-worker-calendar-and-scheduling"></a><span data-ttu-id="53b36-103">Kunnossapitotyöntekijän kalenteri ja ajoittaminen</span><span class="sxs-lookup"><span data-stu-id="53b36-103">Maintenance worker calendar and scheduling</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="53b36-104">Kun ajoitat työtilauksia, luot aikataulun huoltotyöntekijöille, työkaluille ja resursseille.</span><span class="sxs-lookup"><span data-stu-id="53b36-104">When you schedule work orders, you create a schedule for maintenance workers, tools, and assets.</span></span> <span data-ttu-id="53b36-105">Ylläpitotyöntekijöiden aikataulutusta varten jokaiselle heistä on määritettävä kalenteri.</span><span class="sxs-lookup"><span data-stu-id="53b36-105">In order to schedule maintenance workers, a calendar must be set up for each maintenance worker.</span></span> <span data-ttu-id="53b36-106">Kunnossapitotyöntekijät liittyvät resurssiin, ja resursseille määritetään työaikakalenterit.</span><span class="sxs-lookup"><span data-stu-id="53b36-106">Maintenance workers are related to a resource, and working time calendars are set up for resources.</span></span> <span data-ttu-id="53b36-107">Voit määrittää resurssin ja kalenterin kohdassa **Resurssien hallinta** > **Asetukset** > **Työntekijät** >  **Työntekijät**, joka on kuvattu kohdassa [Huoltotyöntekijät ja työntekijäryhmät](../setup-for-objects/workers-and-worker-groups.md).</span><span class="sxs-lookup"><span data-stu-id="53b36-107">You set up the resource and calendar in **Asset management** > **Setup** > **Workers** > **Workers**, which is described in [Maintenance workers and worker groups](../setup-for-objects/workers-and-worker-groups.md).</span></span>

<span data-ttu-id="53b36-108">Alla oleva kuvakaappaus näyttää esimerkin huoltotyöntekijästä, joka liittyy työaikakalenteria Tuotanto käyttävään resurssiin.</span><span class="sxs-lookup"><span data-stu-id="53b36-108">The screenshot below shows an example of a maintenance worker who is related to a resource that uses the working time calendar "Production".</span></span>

![Kuva 1](media/01-work-order-scheduling.png)

<span data-ttu-id="53b36-110">Työkalujen ja resurssien kalenteriasetuksia ei tarvita suhteessa työtilausten suunnitteluun.</span><span class="sxs-lookup"><span data-stu-id="53b36-110">Calendar setup for tools and assets is not needed in relation to work order scheduling.</span></span> <span data-ttu-id="53b36-111">Oletus on, että työkalut ja resurssit ovat käytettävissä 24 tuntia vuorokaudessa huoltoa varten.</span><span class="sxs-lookup"><span data-stu-id="53b36-111">The assumption is that tools and assets are available 24 hours a day for maintenance.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]