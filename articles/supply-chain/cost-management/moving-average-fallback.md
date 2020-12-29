---
title: Liukuva keskiarvo, varalla oleva kustannusjärjestys
description: Tässä ohjeaiheessa on tietoja varakustannusjaksoista keskimääräisten muuttuvien laskelmien tekemiseksi Microsoft Dynamics 365 Supply Chain Managementissa.
author: AndersGirke
manager: tfehr
ms.date: 03/25/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2020-03-25
ms.dyn365.ops.version: Release 10.0.11
ms.openlocfilehash: 0538701588b9c71dff4c538711606913a359de6a
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/13/2020
ms.locfileid: "4427260"
---
# <a name="moving-average-fallback-cost-sequence"></a><span data-ttu-id="f0d6a-103">Liukuva keskiarvo, varalla oleva kustannusjärjestys</span><span class="sxs-lookup"><span data-stu-id="f0d6a-103">Moving average fallback cost sequence</span></span>

<span data-ttu-id="f0d6a-104">Yksi tapa, jolla voit laskea varastosi kustannuksen, on _liukuva keskiarvo_.</span><span class="sxs-lookup"><span data-stu-id="f0d6a-104">One way that you can calculate the cost of your inventory is by using a _moving average_.</span></span> <span data-ttu-id="f0d6a-105">Kuhunkin varastonimikkeeseen voidaan liittää enintään kolme kustannusarvoa:</span><span class="sxs-lookup"><span data-stu-id="f0d6a-105">Up to three cost values can be associated with each inventory item:</span></span>

- <span data-ttu-id="f0d6a-106">**Viimeinen varasto-otto** – Viimeinen varasto-ottokustannus, joka määritettiin ennen kuin varasto muuttui negatiiviseksi</span><span class="sxs-lookup"><span data-stu-id="f0d6a-106">**Last issue** – The last issue cost that was assigned before inventory went negative</span></span>
- <span data-ttu-id="f0d6a-107">**Aktiivinen kustannus** – Uusin kustannuslaskelmaversiossa aktivoitu hinta</span><span class="sxs-lookup"><span data-stu-id="f0d6a-107">**Active cost** – The latest cost that was activated in a costing version</span></span>
- <span data-ttu-id="f0d6a-108">**Nimikehinta** – Vapautetusta tuotteesta määritetty kustannus</span><span class="sxs-lookup"><span data-stu-id="f0d6a-108">**Item price** – The cost that is specified for the released product</span></span>

<span data-ttu-id="f0d6a-109">Määrittääkseen, mitä näistä kustannusarvoista käytetään liukuvissa keskiarvolaskelmissa, järjestelmä käyttää _varakustannussarjaa_ arvojen järjestyksen määrittämiseen.</span><span class="sxs-lookup"><span data-stu-id="f0d6a-109">To determine which of these cost values should be used in moving average calculations, the system uses a _fallback cost sequence_ to establish the order of preference for the values.</span></span> <span data-ttu-id="f0d6a-110">Jos ensisijainen kustannusarvo ei ole käytettävissä, järjestelmä käyttää seuraavaa ensisijaista arvoa ja niin edelleen.</span><span class="sxs-lookup"><span data-stu-id="f0d6a-110">If the preferred cost value isn't available, the system uses the next-preferred value, and so on.</span></span>

<span data-ttu-id="f0d6a-111">Aiemmissa Microsoft Dynamics 365 Supply Chain Management -versioissa järjestelmä käytti vahvistettua varaukustannussarjaa (_viimeinen varasto-otto – aktiivinen kustannus – nimikehinta_).</span><span class="sxs-lookup"><span data-stu-id="f0d6a-111">In previous versions of Microsoft Dynamics 365 Supply Chain Management, the system used a fixed fallback cost sequence (_Last issue – Active cost – Item price_).</span></span> <span data-ttu-id="f0d6a-112">Versiossa 10.0.11 tämä järjestys on edelleen oletusjärjestys.</span><span class="sxs-lookup"><span data-stu-id="f0d6a-112">In version 10.0.11, this sequence is still the default sequence.</span></span> <span data-ttu-id="f0d6a-113">Voit kuitenkin myös ottaa käyttöön toiminnon, jonka avulla voit valita kolmesta käytettävissä olevasta varakustannussekvenssistä.</span><span class="sxs-lookup"><span data-stu-id="f0d6a-113">However, you can also turn on a feature that lets you select among three available fallback cost sequences.</span></span> <span data-ttu-id="f0d6a-114">Tämä ominaisuus voi olla erityisen hyödyllinen organisaatioille, jotka käyttävät säännöllisesti negatiivisia varastoarvoja.</span><span class="sxs-lookup"><span data-stu-id="f0d6a-114">This feature can be especially useful for organizations that regularly use negative inventory values.</span></span>

<span data-ttu-id="f0d6a-115">Jos haluat, että varakustannussarjavalitsin on käytettävissä, sinun (tai ylläpitäjän) on käytettävä [Ominaisuuksien hallintaa](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md), jotta voit ottaa käyttöön toiminnon, jonka nimi on _liukuva keskiarvo_.</span><span class="sxs-lookup"><span data-stu-id="f0d6a-115">To make the selector for the fallback cost sequence available, you (or an admin) must use [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) to turn on the feature that is named _Moving average fallback cost sequence_.</span></span>

<span data-ttu-id="f0d6a-116">Voit valita liukuvan keskiarvolaskennan varauksen kustannusjärjestyksen noudattamalla seuraavia vaiheita.</span><span class="sxs-lookup"><span data-stu-id="f0d6a-116">To select the fallback cost sequence for moving average calculations, follow these steps.</span></span>

1. <span data-ttu-id="f0d6a-117">Avaa **Parametrit**-sivu.</span><span class="sxs-lookup"><span data-stu-id="f0d6a-117">Open the **Parameters** page.</span></span>
2. <span data-ttu-id="f0d6a-118">Määritä **Varastokirjanpito**-välilehden **Liukuva keskiarvo** -osassa **Varakustannussarja**-kentän arvoksi jokin seuraavista arvoista:</span><span class="sxs-lookup"><span data-stu-id="f0d6a-118">On the **Inventory accounting** tab, in the **Moving average** section, set the **Fallback cost sequence** field to one of the following values:</span></span>

    - <span data-ttu-id="f0d6a-119">**Viimeinen varasto-otto – aktiivinen kustannus – nimikkeen hinta** – Tämä järjestys on oletusjärjestys.</span><span class="sxs-lookup"><span data-stu-id="f0d6a-119">**Last issue – Active cost – Item price** – This sequence is the default sequence.</span></span> <span data-ttu-id="f0d6a-120">Se on sama järjestys, jota käytetään, jos _liukuva keskiarvovarakustannussekvenssi_ -toiminto ei ole käytössä.</span><span class="sxs-lookup"><span data-stu-id="f0d6a-120">It's the same sequence that is used if the _Moving average fallback cost sequence_ feature isn't turned on.</span></span>
    - <span data-ttu-id="f0d6a-121">**Aktiivinen kustannus – viimeisin varasto-otto**</span><span class="sxs-lookup"><span data-stu-id="f0d6a-121">**Active cost – Last issue**</span></span>
    - <span data-ttu-id="f0d6a-122">**Aktiivinen kustannus – nimike hinta** – Organisaatioissa saattaa ilmetä suorituskykyongelmia, jos ne käyttävät liiketoimintaprosesseja, joissa varasto säännöllisesti muuttuu negatiiviseksi ja samaan aikaan transaktion määrä on suuri.</span><span class="sxs-lookup"><span data-stu-id="f0d6a-122">**Active cost – Item price** – Organizations might experience performance issues if they use business processes where inventory regularly goes negative and, at the same time, the transaction volume is high.</span></span> <span data-ttu-id="f0d6a-123">Tämän asetuksen avulla voit lieventää suorituskykyongelmia.</span><span class="sxs-lookup"><span data-stu-id="f0d6a-123">This setting can help mitigate those performance issues.</span></span>

<span data-ttu-id="f0d6a-124">![Varastokirjanpitoparametrit](media/inventory-accounting-parameters.png "Varastokirjanpitoparametrit")</span><span class="sxs-lookup"><span data-stu-id="f0d6a-124">![Inventory accounting parameters](media/inventory-accounting-parameters.png "Inventory accounting parameters")</span></span>
