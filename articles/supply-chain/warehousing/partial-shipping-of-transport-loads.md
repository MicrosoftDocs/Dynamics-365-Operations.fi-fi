---
title: Kuljetuskuorman osatoimitus
description: "Tässä ohjeaiheessa käsitellään kuorman osittaista toimittamista ja kuormituksen kapasiteettisuunnittelun lykkäämistä."
author: Mirzaab
manager: AnnBe
ms.date: 03/15/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: WHSTransportLoad
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 1705903
ms.assetid: 427e01b3-4968-4cff-9b85-1717530f72e4
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 8.0.0
ms.translationtype: HT
ms.sourcegitcommit: d9747ba144d56c9410846769e5465372c89ea111
ms.openlocfilehash: 8c172f1b66e56f60e89f56ea98910f8d0e4f3e36
ms.contentlocale: fi-fi
ms.lasthandoff: 08/07/2018

---

# <a name="partial-shipment-of-a-transport-load"></a><span data-ttu-id="5a7af-103">Kuljetuskuorman osatoimitus</span><span class="sxs-lookup"><span data-stu-id="5a7af-103">Partial shipment of a transport load</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="5a7af-104">Kun kuormille määritetään osatoimitus, voit käsitellä kuormia, joiden kapasiteettia ei voi määrittää, ennen kuin kaikki myyntirivit on lisätty kuormaan.</span><span class="sxs-lookup"><span data-stu-id="5a7af-104">By setting up partial shipment of loads, you can handle loads where the capacity can't be determined until all the sales lines have been added to a load.</span></span> <span data-ttu-id="5a7af-105">Prosessi voidaan sitten viimeistellä, kuormalavojen tarkka määrä on tiedossa.</span><span class="sxs-lookup"><span data-stu-id="5a7af-105">The process can then be finalized when the exact pallet count is known.</span></span> <span data-ttu-id="5a7af-106">Näin ollen sinun ei tarvitse päättää kuormalavojen määrittämistä tiettyyn kuljetukseen, ennen kuin kuljetus fyysisesti lastataan vaiheistetusta varastosta.</span><span class="sxs-lookup"><span data-stu-id="5a7af-106">Therefore, you don't have to decide which pallets will be assigned to which transport until the moment when a transport is being physically loaded out of the staged inventory.</span></span>

<span data-ttu-id="5a7af-107">Tämä ominaisuus on vaihtoehto sellaisen jäykän rakenteen noudattamiselle, jos kuormalavat on määritettävä kuljetukseen ennen keräily- tai lastaustyön luontia.</span><span class="sxs-lookup"><span data-stu-id="5a7af-107">This feature offers an alternative to the enforcement of a more rigid structure, where you must determine which pallets will be assigned to which transport before picking work or loading work can be created.</span></span> <span data-ttu-id="5a7af-108">Käyttäjät voivat sen sijaan yksittäisiä kuormia osatoimituksen vahvistukseen.</span><span class="sxs-lookup"><span data-stu-id="5a7af-108">Instead, users can configure individual loads for a partial shipment confirmation.</span></span> <span data-ttu-id="5a7af-109">Kyseisten kuormien lastausprosessit ovat sitten mahdollisia.</span><span class="sxs-lookup"><span data-stu-id="5a7af-109">The transport loading processes for those loads can then occur.</span></span> <span data-ttu-id="5a7af-110">Kuljetuksen suunnitteluosasto voikin suunnitella kuormia ilman, että yksittäisten kuljetusten kapasiteetti olisi otettava huomioon.</span><span class="sxs-lookup"><span data-stu-id="5a7af-110">Therefore, the transportation planning department can plan loads without having to consider the capacity of individual transports.</span></span>

<span data-ttu-id="5a7af-111">Työntekijät voivat määrittää lastauksen aikana uuden kuljetuskuorman, johon kuormalava lastataan.</span><span class="sxs-lookup"><span data-stu-id="5a7af-111">At the time of loading, workers can define a new transport load that a pallet can be loaded to.</span></span> <span data-ttu-id="5a7af-112">Vaihtoehtoisesti he voivat tunnistaa aiemmin luodun kuljetuskuorman.</span><span class="sxs-lookup"><span data-stu-id="5a7af-112">Alternatively, they can identify an existing transport load.</span></span> <span data-ttu-id="5a7af-113">Nämä tiedot voidaan tallentaa mobiililaitteella.</span><span class="sxs-lookup"><span data-stu-id="5a7af-113">This data can be recorded via a mobile device.</span></span> <span data-ttu-id="5a7af-114">Niinpä useat varastotyöntekijät voivat lastata samojen tai eri kuormien varastoa samaan kuorma-autoon.</span><span class="sxs-lookup"><span data-stu-id="5a7af-114">Therefore, several warehouse workers can load inventory from the same loads or different loads onto the same truck.</span></span> <span data-ttu-id="5a7af-115">Kuormat voidaan sitten toimittaa kokonaan tai osittain.</span><span class="sxs-lookup"><span data-stu-id="5a7af-115">The loads can then be fully or partially shipped.</span></span>

> [!NOTE] 
> <span data-ttu-id="5a7af-116">Jos kuorman varastoa voitaisiin lastata tiettyyn kuormaan tai kuorman osatoimitus voitaisiin tehdä, työ on luotava käyttämällä työmallin lastausluokkaa.</span><span class="sxs-lookup"><span data-stu-id="5a7af-116">In order to load inventory from a load to a specific transport load and partially ship the load, work must be generated by using a loading class in a work template.</span></span> <span data-ttu-id="5a7af-117">Tavallista **Keräily**-tyypin keräilytyötä ei voi lastata kuljetuksen kuormaan, kuten kuorma-autoon.</span><span class="sxs-lookup"><span data-stu-id="5a7af-117">Ordinary picking work of the **Picking** type can't be loaded to a transport load such as a truck.</span></span>

## <a name="set-up-transport-loads-for-partial-shipment"></a><span data-ttu-id="5a7af-118">Osatoimituksen kuljetuskuorman määrittäminen</span><span class="sxs-lookup"><span data-stu-id="5a7af-118">Set up transport loads for partial shipment</span></span>

<span data-ttu-id="5a7af-119">Kuormien osatoimitusten määrittäminen koostuu kahdesta menettelystä.</span><span class="sxs-lookup"><span data-stu-id="5a7af-119">The setup for partial shipment of loads consists of the following two procedures.</span></span>

### <a name="set-the-loading-strategy"></a><span data-ttu-id="5a7af-120">Kuormitusstrategian määrittäminen</span><span class="sxs-lookup"><span data-stu-id="5a7af-120">Set the loading strategy</span></span>

<span data-ttu-id="5a7af-121">Osakuormitus on otettava käyttöön määrittämällä kuormitusstrategia.</span><span class="sxs-lookup"><span data-stu-id="5a7af-121">You must enable partial loading by setting the loading strategy.</span></span> <span data-ttu-id="5a7af-122">Voit määrittää kuormitusstrategian sen jälkeen, kun olet luonut kuorman.</span><span class="sxs-lookup"><span data-stu-id="5a7af-122">You can set the loading strategy after you've created a load.</span></span>

1. <span data-ttu-id="5a7af-123">Valitse **Varastonhallinta** \> **Kuormat** \> **Kaikki kuormat**.</span><span class="sxs-lookup"><span data-stu-id="5a7af-123">Select **Warehouse management** \> **Loads** \> **All loads**.</span></span>
2. <span data-ttu-id="5a7af-124">Valitse ensin kuorma ja sitten **Ylätunniste**.</span><span class="sxs-lookup"><span data-stu-id="5a7af-124">Select a load, and then click **Header**.</span></span>
3. <span data-ttu-id="5a7af-125">Valitse **Kuormitusstrategia**-kentässä **Osittaisen kuorman lähetys on sallittu**.</span><span class="sxs-lookup"><span data-stu-id="5a7af-125">In the **Loading strategy** field, select **Partial load shipping allowed**.</span></span>

### <a name="create-a-menu-item-for-loading-of-transport-loads"></a><span data-ttu-id="5a7af-126">Valikkovaihtoehdon luominen kuljetuskuormien lastaamiselle</span><span class="sxs-lookup"><span data-stu-id="5a7af-126">Create a menu item for loading of transport loads</span></span>

<span data-ttu-id="5a7af-127">Sinun on luotava uusi valikkovaihtoehto, joka mahdollistaa kuljetuskuormien lastaamisen.</span><span class="sxs-lookup"><span data-stu-id="5a7af-127">You must create a new menu item that enables transport loads to be loaded.</span></span> <span data-ttu-id="5a7af-128">Kuljetuskuorman avulla voi ryhmittää yhden tai usean kuorman työrivit.</span><span class="sxs-lookup"><span data-stu-id="5a7af-128">A transport load lets you group work lines from one load or multiple loads.</span></span> <span data-ttu-id="5a7af-129">Kaikki kuljetuskuormaan lisättävä voidaan sitten lähettää käyttämällä mobiililaitetta.</span><span class="sxs-lookup"><span data-stu-id="5a7af-129">Everything that is added to the transport load can then be shipped by using a mobile scanner.</span></span>

1. <span data-ttu-id="5a7af-130">Valitse **Varastonhallinta** \> **Asetukset** \> **Mobiililaite** \> **Mobiililaitteen valikkovaihtoehdot**.</span><span class="sxs-lookup"><span data-stu-id="5a7af-130">Select **Warehouse management** \> **Setup** \> **Mobile device** \> **Mobile device menu items**.</span></span>
2. <span data-ttu-id="5a7af-131">Valitse ensin **Uusi** ja sitten **Menetelmä** -kentässä **Työ**.</span><span class="sxs-lookup"><span data-stu-id="5a7af-131">Select **New**, and then, in the **Mode** field, select **Work**.</span></span>
3. <span data-ttu-id="5a7af-132">Valitse **Käytä nykyistä työtä** -asetukseksi **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="5a7af-132">Set the **Use existing work** option to **Yes**.</span></span>
4. <span data-ttu-id="5a7af-133">Valitse **Yleinen**-välilehden **Ohjaaja**-kentässä **Kuljetuksen kuormaus**.</span><span class="sxs-lookup"><span data-stu-id="5a7af-133">On the **General** tab, in the **Directed by** field, select **Transport loading**.</span></span>
5. <span data-ttu-id="5a7af-134">Voit ottaa käyttöön lähetyksen vahvistamisen mobiililaitteella valitsemalla **Sallittu lähetyksen vahvistuksen tyyppi** -kentässä **Kuljetuksen kuorma**.</span><span class="sxs-lookup"><span data-stu-id="5a7af-134">To enable shipment confirmation on a mobile scanner, in the **Allowed ship confirmation type** field, select **Transport load**.</span></span>

## <a name="confirm-shipment-of-a-transport-load-from-the-client"></a><span data-ttu-id="5a7af-135">Kuljetuksen kuorman lähetyksen vahvistus asiakasohjelmasta</span><span class="sxs-lookup"><span data-stu-id="5a7af-135">Confirm shipment of a transport load from the client</span></span>

<span data-ttu-id="5a7af-136">Tällä asetuksella voi vahvistaa, että täyden kuorman tai osakuorman sisältävä kuljetuksen kuorma voidaan lähettää.</span><span class="sxs-lookup"><span data-stu-id="5a7af-136">This setup lets you confirm a transport load that includes a full load or a partially loaded load to be shipped.</span></span>

1. <span data-ttu-id="5a7af-137">Valitse **Varastonhallinta** \> **Kuormat** \> **Kuljetuksen kuormat**.</span><span class="sxs-lookup"><span data-stu-id="5a7af-137">Select **Warehouse management** \> **Loads** \> **Transport loads**.</span></span>
2. <span data-ttu-id="5a7af-138">Valitse toimintoruudun **Lähetä ja vastaanota** -välilehden **Vahvista**-ryhmässä **Kuljetus**.</span><span class="sxs-lookup"><span data-stu-id="5a7af-138">On the Action Pane, on the **Ship and receive** tab, in the **Confirm** group, select **Transport**.</span></span>

