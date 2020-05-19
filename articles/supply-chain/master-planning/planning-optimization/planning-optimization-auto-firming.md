---
title: Automaattinen vahvistus ja suunnittelun optimointi
description: Tässä ohjeaiheessa käsitellään automaattista vahvistusta ja suunnittelun optimointia.
author: ChristianRytt
manager: tfehr
ms.date: 11/05/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2019-11-30
ms.dyn365.ops.version: AX 10.0.7
ms.openlocfilehash: 81c26b8a99f86d663d91ac4f549987262c0541ad
ms.sourcegitcommit: 68092ed283bfbb7b6f611cce1b62c791f9b6a208
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/30/2020
ms.locfileid: "3323528"
---
# <a name="auto-firming-with-planning-optimization"></a><span data-ttu-id="cf6a8-103">Automaattinen vahvistus ja suunnittelun optimointi</span><span class="sxs-lookup"><span data-stu-id="cf6a8-103">Auto-firming with Planning Optimization</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="cf6a8-104">Automaattisen vahvistuksen avulla voit vahvistaa (eli vapauttaa) suunnitellut tilaukset pääsuunnitteluprosessin osana.</span><span class="sxs-lookup"><span data-stu-id="cf6a8-104">Automatic firming lets you firm (that is, release) planned orders as part of the master planning process.</span></span> <span data-ttu-id="cf6a8-105">Kun suunnitellut tilaukset vahvistetaan, ne muunnetaan varsinaisiksi osto-, siirto- tai tuotantotilauksiksi.</span><span class="sxs-lookup"><span data-stu-id="cf6a8-105">When planned orders are firmed, they are transformed into actual purchase orders, transfer orders, or production orders.</span></span> <span data-ttu-id="cf6a8-106">Kun suunnittelun optimointia käytetään, suunnitellut tilaukset vahvistetaan pääsuunnitteluajon aikana silloin, kun tilauspäivä (eli aloituspäivä) on vahvistuksen aikarajan sisällä.</span><span class="sxs-lookup"><span data-stu-id="cf6a8-106">When Planning Optimization is used, planned orders are firmed during a master planning run when the order date (that is, the start date) is within the time fence for firming.</span></span>

> [!NOTE]
> <span data-ttu-id="cf6a8-107">Suunnitellut ostotilauksen automaattinen vahvistus on mahdollista vain, jos nimike on liitetty toimittajaan.</span><span class="sxs-lookup"><span data-stu-id="cf6a8-107">Auto-firming of a planned purchase order can occur only if the item is associated with a vendor.</span></span>

## <a name="turn-on-auto-firming"></a><span data-ttu-id="cf6a8-108">Automaattisen vahvistuksen ottaminen käyttöön</span><span class="sxs-lookup"><span data-stu-id="cf6a8-108">Turn on auto-firming</span></span>

<span data-ttu-id="cf6a8-109">Automaattinen vahvistus otetaan käyttöön seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="cf6a8-109">To turn on auto-firming, follow these steps.</span></span>

1. <span data-ttu-id="cf6a8-110">Valitse **Toimintojen hallinta** -työtilan **Uusi**-lehden luettelossa **Suunnittelun optimoinnin automaattinen vahvistus**.</span><span class="sxs-lookup"><span data-stu-id="cf6a8-110">In the **Feature management** workspace, on the **New** tab, select **Auto-firming for Planning Optimization** in the list.</span></span> <span data-ttu-id="cf6a8-111">Jos toiminto ei ole **Uusi**-välilehdessä, tarkista myös **Ei käytössä**- ja **Kaikki**-välilehdet.</span><span class="sxs-lookup"><span data-stu-id="cf6a8-111">If the feature doesn't appear on the **New** tab, look on the **Not enabled** and **All** tabs.</span></span>
1. <span data-ttu-id="cf6a8-112">Valitse **Ota käyttöön nyt**.</span><span class="sxs-lookup"><span data-stu-id="cf6a8-112">Select **Enable now**.</span></span> <span data-ttu-id="cf6a8-113">Vaihtoehtoisesti voi valita **Aikataulu** ja valita sitten ajan, jolloin haluat ottaa toiminnon käyttöön.</span><span class="sxs-lookup"><span data-stu-id="cf6a8-113">Alternatively, select **Schedule**, and then select the time when you want the feature to be turned on.</span></span>

## <a name="set-up-the-firming-time-fence"></a><span data-ttu-id="cf6a8-114">Vahvistuksen aikarajan määrittäminen</span><span class="sxs-lookup"><span data-stu-id="cf6a8-114">Set up the firming time fence</span></span>

<span data-ttu-id="cf6a8-115">Vahvistuksen aikaraja lasketaan eteenpäin pääsuunnittelun ajopäivämäärästä.</span><span class="sxs-lookup"><span data-stu-id="cf6a8-115">The firming time fence is calculated forward from the master planning run date.</span></span> <span data-ttu-id="cf6a8-116">Se määritetään sen mukaan, kuinka monta päivää ilmoitat.</span><span class="sxs-lookup"><span data-stu-id="cf6a8-116">It's defined by the number of days that you enter.</span></span> <span data-ttu-id="cf6a8-117">Vahvistuksen aikarajaa voi hallita seuraavilla tavoilla:</span><span class="sxs-lookup"><span data-stu-id="cf6a8-117">You can control the firming time fence in the following ways:</span></span>

- <span data-ttu-id="cf6a8-118">Voit määrittää kattavuusryhmän vahvistuksen oletusaikarajan valitsemalla ensin **Pääsuunnittelu** \> **Asetukset** \> **Kattavuus** \> **Kattavuusryhmät** ja valitsemalla sitten kattavuusryhmän.</span><span class="sxs-lookup"><span data-stu-id="cf6a8-118">To define the default firming time fence for a coverage group, go to **Master planning** \> **Setup** \> **Coverage** \> **Coverage groups**, and select a coverage group.</span></span> <span data-ttu-id="cf6a8-119">Anna sitten päivien määrä **Muu**-pikavälilehden **Automaattisen vahvistuksen aikaraja (päivää)** -kentässä.</span><span class="sxs-lookup"><span data-stu-id="cf6a8-119">Then, on the **Other** FastTab, in the **Automatic firming time fence (days)** field, enter the number of days.</span></span>
- <span data-ttu-id="cf6a8-120">Voit ohittaa tietyn nimikkeen kattavuusryhmälle määritetyn vahvistuksen aikarajan valitsemalla ensin **Tuotetietojen hallinta** \> **Vapautetut tuotteet**, sitten toimintoruudussa **Suunnitelma** ja lopuksi **Nimikkeen kattavuus**.</span><span class="sxs-lookup"><span data-stu-id="cf6a8-120">To overwrite the firming time fence that is defined for the coverage group for a specific item, go to **Product information management** \> **Released products**, then from the action pane select **Plan** and then select **Item coverage**.</span></span> <span data-ttu-id="cf6a8-121">Valitse tämän jälkeen **Yleiset**-välilehdessä **Ohita aikarajat** ja anna päivien määrä **Automaattisen vahvistuksen aikaraja (päivää)** -kentässä.</span><span class="sxs-lookup"><span data-stu-id="cf6a8-121">Then, on the **General** tab, select **Override time fence** and in the **Automatic firming time fence (days)** field, enter the number of days.</span></span>
- <span data-ttu-id="cf6a8-122">Voit ohittaa tietylle kattavuusryhmälle määritetyn aikarajan ja tietyn pääsuunnitelman nimikkeen kattavuuden valitsemalla ensin **Pääsuunnittelu** \> **Asetukset** \> **Pääsuunnitelmat** ja valitsemalla sitten pääsuunnitelman.</span><span class="sxs-lookup"><span data-stu-id="cf6a8-122">To overwrite the firming time fence that is defined for the coverage group and item coverage for a specific master plan, go to **Master planning** \> **Setup** \> **Master plans**, and select a Master plan.</span></span> <span data-ttu-id="cf6a8-123">Anna sitten päivien määrä valitsemalla **Aikarajat päivinä** -pikavälilehdessä **Lukitus**-asetukseksi **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="cf6a8-123">Then, on the **Time fence in days** FastTab, set **Freeze** to **Yes**, and enter the number of days.</span></span>

<span data-ttu-id="cf6a8-124">Jos automaattinen vahvistus on otettu käyttöön suunnittelun optimointia käyttävässä pääsuunnitteluajossa, automaattinen vahvistusprosessi tehdään automaattisten vahvistusasetusten mukaisesti.</span><span class="sxs-lookup"><span data-stu-id="cf6a8-124">If auto-firming is turned on for a master planning run that uses Planning Optimization, the auto-firming process is done according to the auto-firming setup.</span></span> <span data-ttu-id="cf6a8-125">Jos automaattinen vahvistusta ei ole otettu käyttöön tai jos suunnittelu käynnistetään **Nettotarpeet**-sivulta, automaattinen vahvistusprosessi ohitetaan.</span><span class="sxs-lookup"><span data-stu-id="cf6a8-125">If auto-firming isn't turned on, or if planning is started from the **Net requirements** page, the auto-firming process is skipped.</span></span>

## <a name="planning-optimization-vs-the-built-in-supply-chain-management-planning-engine"></a><span data-ttu-id="cf6a8-126">Suunnittelun optimoinnin ja Supply Chain Managementin sisäisen suunnittelumoduulin vertailu</span><span class="sxs-lookup"><span data-stu-id="cf6a8-126">Planning Optimization vs. the built-in Supply Chain Management planning engine</span></span>

<span data-ttu-id="cf6a8-127">Sekä suunnittelun optimointia että Microsoft Dynamics 365 Supply Chain Managementiin sisältyvää suunnittelumoduulia voi käyttää suunniteltujen tilausten automaattiseen vahvistamiseen.</span><span class="sxs-lookup"><span data-stu-id="cf6a8-127">Both Planning Optimization and the planning engine that is built into Microsoft Dynamics 365 Supply Chain Management can be used to auto-firm planned orders.</span></span> <span data-ttu-id="cf6a8-128">Niillä on kuitenkin tärkeitä eroavaisuuksiakin.</span><span class="sxs-lookup"><span data-stu-id="cf6a8-128">However, there are some important differences.</span></span> <span data-ttu-id="cf6a8-129">Esimerkiksi siinä missä suunnittelun optimointi käyttää tilauspäivää (eli aloituspäivää) määrittämään, mitkä suunnitellut tilaukset vahvistetaan, Supply Chain Managementin sisäinen suunnittelumoduuli käyttää tarvepäivää (eli päättymispäivää).</span><span class="sxs-lookup"><span data-stu-id="cf6a8-129">For example, whereas Planning Optimization uses the order date (that is, the start date) to determine which planned orders to firm, the built-in Supply Chain Management planning engine uses the requirement date (that is, the end date).</span></span> <span data-ttu-id="cf6a8-130">Yhteenveto eroista:</span><span class="sxs-lookup"><span data-stu-id="cf6a8-130">Here is a summary of the differences.</span></span>

<span data-ttu-id="cf6a8-131">**Suunnittelun optimointi**</span><span class="sxs-lookup"><span data-stu-id="cf6a8-131">**Planning Optimization**</span></span>

- <span data-ttu-id="cf6a8-132">Automaattinen vahvistus perustuu tilauspäivään (aloituspäivään).</span><span class="sxs-lookup"><span data-stu-id="cf6a8-132">Auto-firming is based on the order date (start date).</span></span>
- <span data-ttu-id="cf6a8-133">Koska tilauspäivä (aloituspäivä) käynnistää vahvistuksen, läpimenoaikaa ei tarvitse sisällyttää vahvistuksen aikarajaan.</span><span class="sxs-lookup"><span data-stu-id="cf6a8-133">Because the order date (start date) triggers the firming, you don't have to consider the lead time as part of the firming time fence.</span></span>
- <span data-ttu-id="cf6a8-134">Jos haluat vahvistaa kaikki tilaukset, joiden on käynnistyttävä kuluvana viikkona, vahvistuksen aikarajan on oltava yksi viikko.</span><span class="sxs-lookup"><span data-stu-id="cf6a8-134">If you want to firm all orders that must start during the current week, the firming time fence must be one week.</span></span>

<span data-ttu-id="cf6a8-135">**Supply Chain Managementin sisäinen suunnittelumoduuli**</span><span class="sxs-lookup"><span data-stu-id="cf6a8-135">**Built-in Supply Chain Management planning engine**</span></span>

- <span data-ttu-id="cf6a8-136">Automaattinen vahvistus perustuu tarvepäivään (päättymispäivään).</span><span class="sxs-lookup"><span data-stu-id="cf6a8-136">Auto-firming is based on the requirement date (end date).</span></span>
- <span data-ttu-id="cf6a8-137">Vahvistuksen aikarajan on oltava pidempi kuin läpimenoajan, jotta voidaan varmistaa, että tilaukset vahvistetaan ajoissa.</span><span class="sxs-lookup"><span data-stu-id="cf6a8-137">To help guarantee that orders are firmed in due time, the firming time fence must be longer than the lead time.</span></span>
- <span data-ttu-id="cf6a8-138">Jos haluat vahvistaa kaikki tilaukset, joiden on käynnistyttävä kuluvana viikkona, vahvistuksen aikarajan on oltava läpimenoaika plus yksi viikko.</span><span class="sxs-lookup"><span data-stu-id="cf6a8-138">If you want to firm all orders that must start during the current week, the firming time fence must be the lead time plus one week.</span></span>
