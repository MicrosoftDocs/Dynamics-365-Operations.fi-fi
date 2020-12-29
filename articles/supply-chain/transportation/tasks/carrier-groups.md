---
title: Rahdinkuljettajaryhmät
description: Tässä aiheessa käsitellään rahdinkuljettajaryhmien tietojen määrittämisestä.
author: Henrikan
manager: ''
ms.date: 10/30/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TMSCarrierGroup
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: henrikan
ms.search.validFrom: 2020-10-30
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 2570479edac9bc8cc7aa998a8b69f54ffc10cd61
ms.sourcegitcommit: deb711c92251ed48cdf20ea514d03461c26a2262
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/25/2020
ms.locfileid: "4646386"
---
# <a name="carrier-groups"></a><span data-ttu-id="4fda6-103">Rahdinkuljettajaryhmät</span><span class="sxs-lookup"><span data-stu-id="4fda6-103">Carrier groups</span></span>

<span data-ttu-id="4fda6-104">Rahdinkuljettajaryhmä on lähetyksen rahdinkuljettajien ja rahdinkuljettajapalvelujen kokoelma.</span><span class="sxs-lookup"><span data-stu-id="4fda6-104">A carrier group is a collection of shipping carriers and carrier services.</span></span> <span data-ttu-id="4fda6-105">Kukin rahdinkuljettajaryhmä määrittää lähetyksen rahdinkuljettajien ja siihen kuuluvien rahdinkuljettajapalvelujen ensisijaisen järjestyksen.</span><span class="sxs-lookup"><span data-stu-id="4fda6-105">Each carrier group specifies the preferred sequence for the shipping carriers and carrier services that belong to it.</span></span>

<span data-ttu-id="4fda6-106">Jos samalla reittisegmentillä on useita lähetyksen rahdinkuljettajia ja rahdinkuljettajapalveluja, voit määrittää reittisuunnitelmassa tai reittioppaassa rahdinkuljettajaryhmän yksittäisen lähetyksen rahdinkuljettajan ja rahdinkuljettajapalvelun.</span><span class="sxs-lookup"><span data-stu-id="4fda6-106">When multiple shipping carriers and carrier services exist for the same route segment, you can specify a carrier group instead of a specific shipping carrier and carrier service in the route plan or route guide.</span></span>

## <a name="create-a-carrier-group"></a><span data-ttu-id="4fda6-107">Rahdinkuljettajaryhmän luominen</span><span class="sxs-lookup"><span data-stu-id="4fda6-107">Create a carrier group</span></span>

1. <span data-ttu-id="4fda6-108">Valitse **Kuljetustenhallinta &gt; Asetukset &gt; Rahdinkuljettajat &gt; Rahdinkuljettajaryhmä**.</span><span class="sxs-lookup"><span data-stu-id="4fda6-108">Go to **Transportation management &gt; Setup &gt; Carriers &gt; Carrier group**.</span></span>
1. <span data-ttu-id="4fda6-109">Valitse **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="4fda6-109">Select **New**.</span></span>
1. <span data-ttu-id="4fda6-110">Anna ryhmän yksilöivä tunnus **Rahdinkuljettajaryhmä**-kentässä.</span><span class="sxs-lookup"><span data-stu-id="4fda6-110">In the **Carrier group** field, enter a unique identifier (ID) for the group.</span></span>
1. <span data-ttu-id="4fda6-111">Anna **Nimi**-kentässä ryhmää kuvaava nimi.</span><span class="sxs-lookup"><span data-stu-id="4fda6-111">In the **Name** field, enter a descriptive name for the group.</span></span>
1. <span data-ttu-id="4fda6-112">Lisää **Tiedot**-pikavälilehdessä rivi ja valitse siihen lähetyksen rahdinkuljettaja ja rahdinkuljettajapalvelu.</span><span class="sxs-lookup"><span data-stu-id="4fda6-112">On the **Details** FastTab, add a row, and select a shipping carrier and a carrier service for it.</span></span> <span data-ttu-id="4fda6-113">Toista tämä vaihe, kunnes olet lisännyt ryhmään tarvittavan määrän rahdinkuljettajia.</span><span class="sxs-lookup"><span data-stu-id="4fda6-113">Repeat this step until you've added as many carriers as you require for the group.</span></span>
1. <span data-ttu-id="4fda6-114">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="4fda6-114">Close the page.</span></span>
