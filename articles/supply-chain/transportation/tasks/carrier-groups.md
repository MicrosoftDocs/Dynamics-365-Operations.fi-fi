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
ms.search.region: Global
ms.search.industry: Distribution
ms.author: henrikan
ms.search.validFrom: 2020-10-30
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 95517153dda06cecf8e57b1f9b080aa07966c111
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5247259"
---
# <a name="carrier-groups"></a><span data-ttu-id="70ef2-103">Rahdinkuljettajaryhmät</span><span class="sxs-lookup"><span data-stu-id="70ef2-103">Carrier groups</span></span>

<span data-ttu-id="70ef2-104">Rahdinkuljettajaryhmä on lähetyksen rahdinkuljettajien ja rahdinkuljettajapalvelujen kokoelma.</span><span class="sxs-lookup"><span data-stu-id="70ef2-104">A carrier group is a collection of shipping carriers and carrier services.</span></span> <span data-ttu-id="70ef2-105">Kukin rahdinkuljettajaryhmä määrittää lähetyksen rahdinkuljettajien ja siihen kuuluvien rahdinkuljettajapalvelujen ensisijaisen järjestyksen.</span><span class="sxs-lookup"><span data-stu-id="70ef2-105">Each carrier group specifies the preferred sequence for the shipping carriers and carrier services that belong to it.</span></span>

<span data-ttu-id="70ef2-106">Jos samalla reittisegmentillä on useita lähetyksen rahdinkuljettajia ja rahdinkuljettajapalveluja, voit määrittää reittisuunnitelmassa tai reittioppaassa rahdinkuljettajaryhmän yksittäisen lähetyksen rahdinkuljettajan ja rahdinkuljettajapalvelun.</span><span class="sxs-lookup"><span data-stu-id="70ef2-106">When multiple shipping carriers and carrier services exist for the same route segment, you can specify a carrier group instead of a specific shipping carrier and carrier service in the route plan or route guide.</span></span>

## <a name="create-a-carrier-group"></a><span data-ttu-id="70ef2-107">Rahdinkuljettajaryhmän luominen</span><span class="sxs-lookup"><span data-stu-id="70ef2-107">Create a carrier group</span></span>

1. <span data-ttu-id="70ef2-108">Valitse **Kuljetustenhallinta &gt; Asetukset &gt; Rahdinkuljettajat &gt; Rahdinkuljettajaryhmä**.</span><span class="sxs-lookup"><span data-stu-id="70ef2-108">Go to **Transportation management &gt; Setup &gt; Carriers &gt; Carrier group**.</span></span>
1. <span data-ttu-id="70ef2-109">Valitse **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="70ef2-109">Select **New**.</span></span>
1. <span data-ttu-id="70ef2-110">Anna ryhmän yksilöivä tunnus **Rahdinkuljettajaryhmä**-kentässä.</span><span class="sxs-lookup"><span data-stu-id="70ef2-110">In the **Carrier group** field, enter a unique identifier (ID) for the group.</span></span>
1. <span data-ttu-id="70ef2-111">Anna **Nimi**-kentässä ryhmää kuvaava nimi.</span><span class="sxs-lookup"><span data-stu-id="70ef2-111">In the **Name** field, enter a descriptive name for the group.</span></span>
1. <span data-ttu-id="70ef2-112">Lisää **Tiedot**-pikavälilehdessä rivi ja valitse siihen lähetyksen rahdinkuljettaja ja rahdinkuljettajapalvelu.</span><span class="sxs-lookup"><span data-stu-id="70ef2-112">On the **Details** FastTab, add a row, and select a shipping carrier and a carrier service for it.</span></span> <span data-ttu-id="70ef2-113">Toista tämä vaihe, kunnes olet lisännyt ryhmään tarvittavan määrän rahdinkuljettajia.</span><span class="sxs-lookup"><span data-stu-id="70ef2-113">Repeat this step until you've added as many carriers as you require for the group.</span></span>
1. <span data-ttu-id="70ef2-114">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="70ef2-114">Close the page.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]