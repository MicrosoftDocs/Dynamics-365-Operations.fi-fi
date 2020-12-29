---
title: Kuljetustenhallinnan tilat
description: Tässä aiheessa käsitellään kuljetuksen tilan luontia ja kyseisen tilan yhdistämistä rahdinkuljettajan tilaan.
author: Henrikan
manager: tfehr
ms.date: 10/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2020-09-08
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: 3f7d471771ec2b4703d878fbf395cd90902b6669
ms.sourcegitcommit: fe7ac653efcb1ac6318083f482394b96ed82b4c7
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/29/2020
ms.locfileid: "4427536"
---
# <a name="transportation-management-statuses"></a><span data-ttu-id="6c7a0-103">Kuljetustenhallinnan tilat</span><span class="sxs-lookup"><span data-stu-id="6c7a0-103">Transportation management statuses</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6c7a0-104">Määritä kuljetuksen tilan pääkoodit selventämään rahdinkuljettajien antamat koodit.</span><span class="sxs-lookup"><span data-stu-id="6c7a0-104">Set up master codes for transportation statuses to interpret codes that are provided by your shipping carriers.</span></span> <span data-ttu-id="6c7a0-105">Tällä tavoin rahdinkuljettajat voidaan integroida antamaan tila.</span><span class="sxs-lookup"><span data-stu-id="6c7a0-105">This lets you integrate with shipping carriers to provide a status.</span></span> <span data-ttu-id="6c7a0-106">Kuljetuksen päätilakoodille annettava kuljetuksen tila voi auttaa seuraamaan kuorman, lähetyksen tai kontin tilaa.</span><span class="sxs-lookup"><span data-stu-id="6c7a0-106">The transportation status that you provide for a transportation master status code can help you track the status of a load, shipment, or container.</span></span> <span data-ttu-id="6c7a0-107">Kuorman, lähetyksen tai kontin tietty kuljetuksen tila voidaan päivittää vain tietoja integroimalla eikä manuaalisesti käyttöliittymässä.</span><span class="sxs-lookup"><span data-stu-id="6c7a0-107">The specific transportation status for a load, shipment, or container can only be updated through data integration and not manually through the user interface.</span></span>

## <a name="create-a-transportation-status"></a><span data-ttu-id="6c7a0-108">Kuljetuksen tilan luominen</span><span class="sxs-lookup"><span data-stu-id="6c7a0-108">Create a transportation status</span></span>

<span data-ttu-id="6c7a0-109">Kuljetuksen tila luodaan seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="6c7a0-109">To create a transportation status, follow these steps:</span></span>

1. <span data-ttu-id="6c7a0-110">Valitse **Kuljetustenhallinta \> Asetukset \> Kuljetuksen tilan päätiedot**.</span><span class="sxs-lookup"><span data-stu-id="6c7a0-110">Go to **Transportation management \> Setup \> Transportation status masters**.</span></span>
1. <span data-ttu-id="6c7a0-111">Luo uudet kuljetuksen tilan päätiedot valitsemalla **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="6c7a0-111">Select **New** to create a transportation status master.</span></span>
1. <span data-ttu-id="6c7a0-112">Kirjoita **Kuljetuksen tilan päätiedot** -kenttään yksilöivä kuljetuksen tilan koodi.</span><span class="sxs-lookup"><span data-stu-id="6c7a0-112">In the **Transportation status master** field, enter a unique code for the transportation status.</span></span>
1. <span data-ttu-id="6c7a0-113">Valitse **Kuljetustyyppi**-kentässä kuljetuksen tyypiksi joko *Rahdinkuljettaja* tai *Keskus*.</span><span class="sxs-lookup"><span data-stu-id="6c7a0-113">In the **Transportation type** field, select either *Shipping carrier* or *Hub* as the type of transportation.</span></span>
1. <span data-ttu-id="6c7a0-114">Anna nimi ja kuljetuksen tila.</span><span class="sxs-lookup"><span data-stu-id="6c7a0-114">Enter a name and transportation status.</span></span>
1. <span data-ttu-id="6c7a0-115">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="6c7a0-115">Close the page.</span></span>

## <a name="map-a-transportation-status-to-a-carrier-status"></a><span data-ttu-id="6c7a0-116">Kuljetuksen tilan yhdistäminen rahdinkuljettajan tilaan</span><span class="sxs-lookup"><span data-stu-id="6c7a0-116">Map a transportation status to a carrier status</span></span>

<span data-ttu-id="6c7a0-117">Kuljetuksen tila yhdistetään rahdinkuljettajan tilaan seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="6c7a0-117">To map a transportation status to a carrier status, follow these steps:</span></span>

1. <span data-ttu-id="6c7a0-118">Valitse **Kuljetustenhallinta \> Asetukset \> Rahdinkuljettajat \> Rahdinkuljettajan kuljettajan tila**.</span><span class="sxs-lookup"><span data-stu-id="6c7a0-118">Go to **Transportation management \> Setup \> Carriers \> Carrier transportation status**.</span></span>
1. <span data-ttu-id="6c7a0-119">Yhdistä rahdinkuljettajan koodi kuljetuksen tilan pääkoodiin valitsemalla **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="6c7a0-119">Select **New** to map a code from a shipping carrier to a transportation status master code.</span></span>
1. <span data-ttu-id="6c7a0-120">Valitse rahdinkuljettajan ja rahdinkuljetuspalvelun yksilöivä tunnus.</span><span class="sxs-lookup"><span data-stu-id="6c7a0-120">Select the unique ID for the shipping carrier and the carrier service.</span></span>
1. <span data-ttu-id="6c7a0-121">Valitse kuljetuksen tilakoodi, jonka haluat määrittää valitun lähetyksen rahdinkuljettajan koodille.</span><span class="sxs-lookup"><span data-stu-id="6c7a0-121">Select the transportation status code that you want to map to the selected shipping carrier's code.</span></span>
1. <span data-ttu-id="6c7a0-122">Anna lähetyksen rahdinkuljettajan käyttämä ulkoinen koodi.</span><span class="sxs-lookup"><span data-stu-id="6c7a0-122">Enter the external code that is used by the shipping carrier.</span></span>
1. <span data-ttu-id="6c7a0-123">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="6c7a0-123">Close the page.</span></span>
