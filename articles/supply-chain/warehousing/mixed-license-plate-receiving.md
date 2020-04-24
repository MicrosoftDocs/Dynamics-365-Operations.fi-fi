---
title: Yhdistetyn rekisterikilven vastaanotto
description: Tässä ohjeaiheessa kerrotaan, miten yhdistetyn rekisterikilven vastaanotolla rekisteröidään ja luodaan työ useille nimikkeille mobiililaitteessa.
author: Mirzaab
manager: tfehr
ms.date: 05/26/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSRFAutoConfirm
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 269384
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 15c058887da33b522c5d9a1a8d2c45a5d1566a5d
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/02/2020
ms.locfileid: "3215766"
---
# <a name="mixed-license-plate-receiving"></a><span data-ttu-id="4053b-103">Yhdistetyn rekisterikilven vastaanotto</span><span class="sxs-lookup"><span data-stu-id="4053b-103">Mixed license plate receiving</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4053b-104">Yhdistetyn rekisterikilven vastaanoton avulla voit muodostaa useista nimikkeistä koostuvia rekisterikilpiä ennen rekisteröintiä painopanotyön luontia.</span><span class="sxs-lookup"><span data-stu-id="4053b-104">Mixed license plate receiving allows you to build a license plate consisting of multiple items before you register and create put-away work.</span></span> 

<span data-ttu-id="4053b-105">Useista nimikkeistä koostuvaa rekisterikilpeä ei tarvitse jakaa vastaanottolaiturilla kunkin nimikkeen rekisteröintiä varten.</span><span class="sxs-lookup"><span data-stu-id="4053b-105">A license plate that consists of multiple items does not have to be split at the receiving dock for you to register each item.</span></span> 

<span data-ttu-id="4053b-106">Kun lähdeasiakirjanrivien tunnistamiseen käytetään nimikeperusteista työnkulkua, voit skannata viivakoodit nimikehallinnassa.</span><span class="sxs-lookup"><span data-stu-id="4053b-106">When using an item-related flow to identify the source document lines, you can scan bar codes on the item control.</span></span> <span data-ttu-id="4053b-107">Jos viivakoodiin on määritetty määrä ja mittayksikkö, nimike ja määrä lisätään automaattisesti yhdistettyyn rekisterikilpeen ja näyttö palautuu uuden nimikkeen skannaustilaan.</span><span class="sxs-lookup"><span data-stu-id="4053b-107">If the bar code has a quantity and a unit of measure (UOM) configured on it, the item and quantity will automatically be added to the mixed license plate, and you will be returned to the screen to scan another item.</span></span> <span data-ttu-id="4053b-108">Voit tällä tavoin tarkastaa kaikki nimikkeet nopeasti ilman, että jokainen vaihe on vahvistettava.</span><span class="sxs-lookup"><span data-stu-id="4053b-108">This allows you to quickly scan all the items without having to make a confirmation at each step.</span></span> 

<span data-ttu-id="4053b-109">Voit näyttää yhdistetyn rekisterikilven vastaanottovirrassa luettelon nimikkeistä, jotka on jo skannattu rekisterikilpeen. Voit myös muokata tai korvat nimikkeen määrän siellä.</span><span class="sxs-lookup"><span data-stu-id="4053b-109">In the flow for mixed license plate receiving, you can display the list of items that are already scanned to the license plate and from here you can modify or correct the quantity of an item.</span></span>

## <a name="where-it-applies"></a><span data-ttu-id="4053b-110">Käyttö</span><span class="sxs-lookup"><span data-stu-id="4053b-110">Where it applies</span></span>

<span data-ttu-id="4053b-111">Yhdistetyn rekisterikilven vastaanotto on mobiililaitteen vastaanottovirta useiden rivien tai nimikkeiden samanaikaista rekisteröintiä ja työn luomista varten.</span><span class="sxs-lookup"><span data-stu-id="4053b-111">Mixed license plate receiving is a mobile device receiving flow to register and create work for multiple lines/items at the same time.</span></span> <span data-ttu-id="4053b-112">Tämä on kätevää, jos vastaanotat saapuvia rekisterikilpiä, joissa on useita nimikkeitä.</span><span class="sxs-lookup"><span data-stu-id="4053b-112">This is useful if you receive inbound license plates with multiple items.</span></span> 

## <a name="how-to-set-up-mixed-license-plate-receiving"></a><span data-ttu-id="4053b-113">Yhdistetyn rekisterikilven vastaanoton määrittäminen</span><span class="sxs-lookup"><span data-stu-id="4053b-113">How to set up mixed license plate receiving</span></span>
<span data-ttu-id="4053b-114">Yhdistetyn rekisterikilven vastaanotto määritetään mobiililaitteen valikkovaihtoehtona.</span><span class="sxs-lookup"><span data-stu-id="4053b-114">Mixed license plate receiving is set up as a mobile device menu item.</span></span>

<span data-ttu-id="4053b-115">Sinun on luotava uusi valikkovaihtoehto, jossa tilaksi on määritetty työ, joka ei käytä aiemmin luotua työtä ja joka käyttää jotakin seuraavista menetelmiä:</span><span class="sxs-lookup"><span data-stu-id="4053b-115">You need to create a new menu item with mode work that does not use existing work and use one of the following methods:</span></span>

- <span data-ttu-id="4053b-116">Yhdistetyn rekisterikilven vastaanotto</span><span class="sxs-lookup"><span data-stu-id="4053b-116">Mixed license plate receiving</span></span>
- <span data-ttu-id="4053b-117">Yhdistetyn rekisterikilven vastaanotto ja poispano</span><span class="sxs-lookup"><span data-stu-id="4053b-117">Mixed license plate receiving and put away</span></span>

<span data-ttu-id="4053b-118">Lähdeasiakirjarivien tunnistamisvaihtoehdot ovat ostotilausnimike, ostotilausrivi, palautustilaus, siirtotilausnimike ja siirtotilausrivi.</span><span class="sxs-lookup"><span data-stu-id="4053b-118">The options to identify the source document lines are purchase order item, purchase order line, return order, transfer order item, and transfer order line.</span></span> <span data-ttu-id="4053b-119">Nämä vaihtoehdot voivat muuttaa yhden rekisterikilven vastaanottotilauksen.</span><span class="sxs-lookup"><span data-stu-id="4053b-119">These options can change the receiving order on a single license plate.</span></span> <span data-ttu-id="4053b-120">Viimeinen vaihtoehto on kuormanimikkeen mukaan.</span><span class="sxs-lookup"><span data-stu-id="4053b-120">The last option is by load item.</span></span> <span data-ttu-id="4053b-121">Voit lisätä rekisterikilpeen useita nimikkeitä mutta vaihtelu useiden kuormien välillä ei ole mahdollista.</span><span class="sxs-lookup"><span data-stu-id="4053b-121">You can add multiple items to a license plate, but you cannot switch between multiple loads.</span></span>
