---
title: Kappaleen keräilyvahvistus
description: Tässä ohjeaiheessa kerrotaan kappaleen keräilyvahvistuksen määrittämisestä ja käyttämisestä mobiililaitteessa.
author: Mirzaab
manager: tfehr
ms.date: 05/26/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSRFAutoConfirm, WHSRFMenuItem
audience: Application User
ms.reviewer: kamaybac
ms.custom: 269384
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 66903d142ecb7228e4fdec56dbd45472acbdeb69
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/15/2021
ms.locfileid: "4989640"
---
# <a name="piece-picking-confirmation"></a><span data-ttu-id="43268-103">Kappaleen keräilyvahvistus</span><span class="sxs-lookup"><span data-stu-id="43268-103">Piece picking confirmation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="43268-104">Kappalekeräilyssä voit vahvistaa mobiililaitteessa varaston jokaisen kappaleen keräily- tai inventointityön avulla.</span><span class="sxs-lookup"><span data-stu-id="43268-104">Piece picking allows you to confirm each piece of inventory through picking or counting work on a mobile device.</span></span> <span data-ttu-id="43268-105">Voit vahvistaa keräilyssä käsiteltävän työn määrän kerättävään työhön määritettyyn määrään saakka.</span><span class="sxs-lookup"><span data-stu-id="43268-105">For picks, you can confirm the quantity of work to be processed up to the quantity that is specified on work to be picked.</span></span> <span data-ttu-id="43268-106">Voit skannata inventointityössä inventoitavan varaston ja seurata kokonaismäärää.</span><span class="sxs-lookup"><span data-stu-id="43268-106">For counting work, you can scan the inventory that you are counting and track the total amount.</span></span>

<span data-ttu-id="43268-107">Kun otat kappalekeräilyn käyttöön, tuotevahvistus valitaan automaattisesti.</span><span class="sxs-lookup"><span data-stu-id="43268-107">When you enable piece picking, product confirmation is automatically selected.</span></span> <span data-ttu-id="43268-108">Kun työn tyyppinä on keräys, kappaleiden enimmäismäärä otetaan käyttöön.</span><span class="sxs-lookup"><span data-stu-id="43268-108">For work-type picks, a maximum number of pieces is enabled.</span></span> <span data-ttu-id="43268-109">Tällä tavoin voit määrittää työprosessin aikana vahvistettavien kappaleiden enimmäismäärän.</span><span class="sxs-lookup"><span data-stu-id="43268-109">This allows you to set a maximum to the number of pieces that must be confirmed during the work process.</span></span> <span data-ttu-id="43268-110">Enimmäismäärä perustuu käsiteltävänä olevaan nykyiseen työyksikköön.</span><span class="sxs-lookup"><span data-stu-id="43268-110">The maximum quantity is based on the current work unit that is being processed.</span></span> <span data-ttu-id="43268-111">Enimmäismäärää ei voi määrittää, jos työtyyppinä on inventointi.</span><span class="sxs-lookup"><span data-stu-id="43268-111">The counting work type does not allow a maximum.</span></span>

<span data-ttu-id="43268-112">Voit käyttää myös skannattuun viivakoodin liitettyä määrää ja mittayksikköä.</span><span class="sxs-lookup"><span data-stu-id="43268-112">You can also use the quantity and unit of measure (UOM) that is associated with a scanned bar code.</span></span> <span data-ttu-id="43268-113">Tämä saapuvien ja lähtevien virtojen työ sisältää yhdistetyn rekisterikilven vastaanoton, ostotilausnimikkeen, siirtotilausnimikkeen ja kuormanimikkeen.</span><span class="sxs-lookup"><span data-stu-id="43268-113">This will work for receiving on inbound flows including mixed license plate receiving, purchase order item, transfer order item, and load item.</span></span> <span data-ttu-id="43268-114">Se toimii myös kappalekeräilyssä, jossa viivakoodin skannaus lisää määrän vahvistettujen kappaleiden kokonaismäärään muuntamalla mittayksikön viivakoodin ja työyksikön välillä.</span><span class="sxs-lookup"><span data-stu-id="43268-114">It also works for piece picking where scanning the bar code will add the quantity to the total number of confirmed pieces converting between the UOM on the bar code and the work unit.</span></span> <span data-ttu-id="43268-115">Jos viivakoodin mittayksikköä inventoitaessa vahvistetaan, että määrä on sallittu sarjaryhmän inventoinnissa, määrä lisätään kokonaismäärään.</span><span class="sxs-lookup"><span data-stu-id="43268-115">If, when counting the UOM on the bar code, it is confirmed that the quantity is allowed for counting on the sequence group, the quantity will be added to the total count.</span></span>

## <a name="where-it-applies"></a><span data-ttu-id="43268-116">Käyttö</span><span class="sxs-lookup"><span data-stu-id="43268-116">Where it applies</span></span>

<span data-ttu-id="43268-117">Kappalekeräilyä voi käyttää kaikissa inventointitöissä ja kaikenlaisten työtyyppien ensimmäisellä keräyksessä.</span><span class="sxs-lookup"><span data-stu-id="43268-117">Piece picking works for all counting work and for the initial pick for any type of work.</span></span> <span data-ttu-id="43268-118">Kappalekeräystä ei voi käyttää, jos nimikettä ohjataan sarjanumeroilla tai jos se on tuotanto- tai kanban-keräily rekisterikilpisijainnista ja jos nimike on määritetty väliaikaiseen varastoon.</span><span class="sxs-lookup"><span data-stu-id="43268-118">Piece picking does not apply if the item is controlled by serial numbers or if it is a production or kanban pick from a license plate (LP) location and the item is set to staging.</span></span>

## <a name="set-up-piece-picking"></a><span data-ttu-id="43268-119">Kappalekeräilyn määrittäminen</span><span class="sxs-lookup"><span data-stu-id="43268-119">Set up piece picking</span></span>

1.  <span data-ttu-id="43268-120">Avaa mobiililaitteen valikossa työn vahvistuksen määrityslomake: Varastonhallinta > **Varastonhallinta** > **Asetukset** > **Mobiililaite** > **Mobiililaitteen valikkovaihtoehdot**.</span><span class="sxs-lookup"><span data-stu-id="43268-120">On a mobile device menu item, open the setup form for work confirmation: Warehouse management > **Warehouse management** > **Setup** > **Mobile device** > **Mobile device menu items**.</span></span> 
2. <span data-ttu-id="43268-121">Avaa mobiililaitteen valikossa Työn vahvistusasetukset.</span><span class="sxs-lookup"><span data-stu-id="43268-121">From the mobile device menu item, open Work confirmation setup.</span></span>

<span data-ttu-id="43268-122">Seuraavat asetukset ovat valittavissa, kun työtyyppinä on keräily tai inventointi.</span><span class="sxs-lookup"><span data-stu-id="43268-122">The following options become available for selection when the work type is pick or counting.</span></span>


|           <span data-ttu-id="43268-123">Vaihtoehto</span><span class="sxs-lookup"><span data-stu-id="43268-123">Option</span></span>           |                                                                            <span data-ttu-id="43268-124">kuvaus</span><span class="sxs-lookup"><span data-stu-id="43268-124">Description</span></span>                                                                            |
|----------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="43268-125">Kappaleen keräilyvahvistus</span><span class="sxs-lookup"><span data-stu-id="43268-125">Piece picking confirmation</span></span> | <span data-ttu-id="43268-126">Käytettävissä, kun työtyyppinä on keräily tai inventointi.</span><span class="sxs-lookup"><span data-stu-id="43268-126">Available for pick and counting work types.</span></span> <span data-ttu-id="43268-127">Tuotteen vahvistus valitaan automaattisesti.</span><span class="sxs-lookup"><span data-stu-id="43268-127">Product confirmation is automatically selected.</span></span> <span data-ttu-id="43268-128">Jokainen varastokappale voidaan vahvistaa mobiililaitteessa.</span><span class="sxs-lookup"><span data-stu-id="43268-128">Allows you to confirm each piece of inventory from the mobile device.</span></span> |
|  <span data-ttu-id="43268-129">Kappaleiden enimmäismäärä</span><span class="sxs-lookup"><span data-stu-id="43268-129">Maximum number of pieces</span></span>  |                   <span data-ttu-id="43268-130">Käytettävissä keräilytyössä, jos kappalekeräilyn vahvistus on otettu käyttöön.</span><span class="sxs-lookup"><span data-stu-id="43268-130">Available for pick work if piece picking confirmation is enabled.</span></span> <span data-ttu-id="43268-131">Määrittää rajan vahvistettavien kappaleiden määrälle.</span><span class="sxs-lookup"><span data-stu-id="43268-131">Sets a limit to the number of pieces that you must confirm.</span></span>                   |

