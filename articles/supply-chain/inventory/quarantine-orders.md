---
title: Karanteenitilaukset
description: Tässä ohjeaiheessa kuvataan varaston käytön estämistä karanteenitilauksilla.
author: perlynne
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventLocation, InventModelGroup, InventQuarantineOrder, InventQuarantineParmEnd, InventQuarantineParmReportFinished, InventQuarantineParmStartUp, InventTrans
audience: Application User
ms.reviewer: kamaybac
ms.custom: 30021
ms.assetid: d5047727-653c-49da-b489-6fd3fe50445e
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5e1eed14b7d38cf569af7192dec9580e771f06df
ms.sourcegitcommit: 8362f3bd32ce8b9a5af93c8e57daef732a93b19e
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/28/2021
ms.locfileid: "5956179"
---
# <a name="quarantine-orders"></a><span data-ttu-id="59f70-103">Karanteenitilaukset</span><span class="sxs-lookup"><span data-stu-id="59f70-103">Quarantine orders</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="59f70-104">Tässä ohjeaiheessa kuvataan varaston käytön estämistä karanteenitilauksilla.</span><span class="sxs-lookup"><span data-stu-id="59f70-104">This topic describes how to use quarantine orders to block inventory.</span></span>

<span data-ttu-id="59f70-105">Karanteenitilausten avulla voit estää varaston.</span><span class="sxs-lookup"><span data-stu-id="59f70-105">Quarantine orders let you block inventory.</span></span> <span data-ttu-id="59f70-106">Haluat ehkä esimerkiksi siirtää nimikkeitä karanteeniin laadunvalvontasyistä.</span><span class="sxs-lookup"><span data-stu-id="59f70-106">For example, you might want to quarantine items for quality control reasons.</span></span> <span data-ttu-id="59f70-107">Karanteeniin asetettu varasto siirretään karanteenivarastoon.</span><span class="sxs-lookup"><span data-stu-id="59f70-107">Inventory that has been quarantined is transferred to a quarantine warehouse.</span></span>

> [!NOTE]
> <span data-ttu-id="59f70-108">Jos käytät varaston lisähallintaprosesseja (Varastonhallinnassa), karanteenitilauksen käsittelyä käytetään vain palautusmyyntitilauksille.</span><span class="sxs-lookup"><span data-stu-id="59f70-108">If you're using advanced warehouse management processes (in Warehouse management), quarantine order processing is used only for return sales orders.</span></span>

## <a name="quarantine-on-hand-inventory-items"></a><span data-ttu-id="59f70-109">Käytettävissä olevien varastonimikkeiden siirtäminen karanteeniin</span><span class="sxs-lookup"><span data-stu-id="59f70-109">Quarantine on-hand inventory items</span></span>

<span data-ttu-id="59f70-110">Kun siirrät nimikkeitä karanteeniin, voit joko luoda karanteenitilauksen manuaalisesti tai määrittää järjestelmän luomaan karanteenitilaukset automaattisesti saapuvien käsittelyn aikana.</span><span class="sxs-lookup"><span data-stu-id="59f70-110">When you quarantine items, you can either manually create the quarantine orders or set up the system to automatically create them during inbound processing.</span></span>

<span data-ttu-id="59f70-111">Määritä, että järjestelmä luo karanteenitilaukset automaattisesti, noudattamalla seuraavia vaiheita.</span><span class="sxs-lookup"><span data-stu-id="59f70-111">To set up the system to automatically generate quarantine orders, follow these steps.</span></span>

1. <span data-ttu-id="59f70-112">Siirry kohtaan **Varastonhallinta \> Asetukset \> Varasto \> Nimikemalliryhmät**.</span><span class="sxs-lookup"><span data-stu-id="59f70-112">Go to **Inventory management \> Setup \> Inventory \> Item model groups**.</span></span>
1. <span data-ttu-id="59f70-113">Valitse haluamasi malliryhmä luetteloruudusta tai luo uusi malliryhmä.</span><span class="sxs-lookup"><span data-stu-id="59f70-113">Select a relevant model group in the list pane, or create a new model group.</span></span>
1. <span data-ttu-id="59f70-114">Valitse **Varastokäytännöt**-pikavälilehdessä **Karanteeninhallinta**-valintaruutu.</span><span class="sxs-lookup"><span data-stu-id="59f70-114">On the **Inventory policies** FastTab, select the **Quarantine management** check box.</span></span>
1. <span data-ttu-id="59f70-115">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="59f70-115">Close the page.</span></span>
1. <span data-ttu-id="59f70-116">Sinun täytyy määrittää oletuskaranteenivarasto vastaanottavien varastojen **Karanteenivarasto**-kentässä.</span><span class="sxs-lookup"><span data-stu-id="59f70-116">In the **Quarantine warehouse** field for the receiving warehouses, specify a default quarantine warehouse.</span></span>

<span data-ttu-id="59f70-117">Kun varastoon vastaanotetuksi rekisteröity nimike kuuluu malliryhmään, jossa **Karanteeninhallinta**-valintaruutu on valittuna, järjestelmä luo sille karanteenitilauksen.</span><span class="sxs-lookup"><span data-stu-id="59f70-117">When an item that is registered as received at the warehouse belongs to a model group where the **Quarantine management** check box is selected, the system generates a quarantine order for it.</span></span> <span data-ttu-id="59f70-118">Karanteenitilaus kehottaa työntekijöitä siirtämään nimikkeen karanteenivarastoon.</span><span class="sxs-lookup"><span data-stu-id="59f70-118">The quarantine order instructs workers to move the item to the quarantine warehouse.</span></span>

<span data-ttu-id="59f70-119">Luodessasi karanteenitilauksia manuaalisesti **Karanteenitilaukset**-sivulla ei ole tarpeen määrittää nykyistä nimikettä karantiinihallintaa varten liitetyssä nimikemalliryhmässä.</span><span class="sxs-lookup"><span data-stu-id="59f70-119">When you manually create quarantine orders on the **Quarantine orders** page, the item doesn't have to be set up for quarantine management in the associated item model group.</span></span> <span data-ttu-id="59f70-120">Tässä prosessissa sinun täytyy määrittää käytettävissä oleva varasto, joka on asetettava karanteeniin, sekä käytettävä karanteenivarasto.</span><span class="sxs-lookup"><span data-stu-id="59f70-120">For this process, you must specify the on-hand inventory that should be quarantined and the quarantine warehouse that should be used.</span></span> <span data-ttu-id="59f70-121">Voit käyttää prosessin suunnittelussa apuna karanteenitilauksen tiloja.</span><span class="sxs-lookup"><span data-stu-id="59f70-121">You can use the quarantine order statuses to help plan the process.</span></span>

## <a name="quarantine-order-statuses"></a><span data-ttu-id="59f70-122">Karanteenitilausten tilat</span><span class="sxs-lookup"><span data-stu-id="59f70-122">Quarantine order statuses</span></span>

<span data-ttu-id="59f70-123">Karanteenitilauksilla voi olla seuraavanlaisia tiloja:</span><span class="sxs-lookup"><span data-stu-id="59f70-123">Quarantine orders can have the following statuses:</span></span>

- <span data-ttu-id="59f70-124">Luotu</span><span class="sxs-lookup"><span data-stu-id="59f70-124">Created</span></span>
- <span data-ttu-id="59f70-125">Aloitettu</span><span class="sxs-lookup"><span data-stu-id="59f70-125">Started</span></span>
- <span data-ttu-id="59f70-126">Ilmoitettu valmiiksi</span><span class="sxs-lookup"><span data-stu-id="59f70-126">Reported as finished</span></span>
- <span data-ttu-id="59f70-127">Päättynyt</span><span class="sxs-lookup"><span data-stu-id="59f70-127">Ended</span></span>

### <a name="created"></a><span data-ttu-id="59f70-128">Luotu</span><span class="sxs-lookup"><span data-stu-id="59f70-128">Created</span></span>

<span data-ttu-id="59f70-129">Kun karanteenitilaus on luotu manuaalisesti, mutta nimikettä ei ole vielä sijoitettu karanteenivarastoon, karanteenitilauksen tilana on **Luotu**.</span><span class="sxs-lookup"><span data-stu-id="59f70-129">When a quarantine order has been created manually, but the item isn't yet in the quarantine warehouse, the quarantine order has a status of **Created**.</span></span> <span data-ttu-id="59f70-130">Järjestelmä luo kaksi varastotapahtumaa.</span><span class="sxs-lookup"><span data-stu-id="59f70-130">Two inventory transactions are generated.</span></span> <span data-ttu-id="59f70-131">Yksi tapahtumista on ottotapahtuma, jonka tila voi olla **Tilauksessa**, **Varattu fyysinen** tai **Keräilty**.</span><span class="sxs-lookup"><span data-stu-id="59f70-131">One transaction is an issue transaction that can have a status of **On order**, **Reserved physical**, or **Picked**.</span></span> <span data-ttu-id="59f70-132">Toinen on vastaanottotapahtuma, jonka tilana karanteenivarastossa voi olla **Tilattu** tai **Rekisteröity**.</span><span class="sxs-lookup"><span data-stu-id="59f70-132">The other transaction is a receipt transaction that can have a status of **Ordered** or **Registered** at the quarantine warehouse.</span></span> <span data-ttu-id="59f70-133">Voit varata, keräillä ja rekisteröidä varaston päivityksiä käyttämällä tavanomaisia prosesseja.</span><span class="sxs-lookup"><span data-stu-id="59f70-133">You can reserve, pick, and register updates to the inventory by using the usual processes.</span></span>

### <a name="started"></a><span data-ttu-id="59f70-134">Aloitettu</span><span class="sxs-lookup"><span data-stu-id="59f70-134">Started</span></span>

<span data-ttu-id="59f70-135">Kun karanteenitilauksen tilana on **Aloitettu**, varasto siirretään tavallisesta varastosta karanteenivarastoon, ja järjestelmä luo kaksi varastotapahtumaa.</span><span class="sxs-lookup"><span data-stu-id="59f70-135">When a quarantine order has a status of **Started**, the inventory is transferred from the regular warehouse to the quarantine warehouse, and two inventory transactions are generated.</span></span> <span data-ttu-id="59f70-136">Yhdellä tapahtumalla on tila **Toimitettu**, ja toisella tapahtumalla on tila **Vastaanotettu**.</span><span class="sxs-lookup"><span data-stu-id="59f70-136">One transaction has a status of **Deducted**, and the other transaction has a status of **Received**.</span></span> <span data-ttu-id="59f70-137">Samalla luodaan kaksi varastotapahtumaa palautussiirron käsittelyä varten.</span><span class="sxs-lookup"><span data-stu-id="59f70-137">At the same time, two inventory transactions are created to handle the return transfer.</span></span> <span data-ttu-id="59f70-138">Näitä tapahtumia ei päivätä.</span><span class="sxs-lookup"><span data-stu-id="59f70-138">These transactions aren't dated.</span></span> <span data-ttu-id="59f70-139">Yhdellä tapahtumalla on tila **Varattu fyysinen**, ja toisella tapahtumalla on tila **Tilattu**.</span><span class="sxs-lookup"><span data-stu-id="59f70-139">One transaction has a status of **Reserved physical**, and the other transaction has a status of **Ordered**.</span></span>

### <a name="reported-as-finished"></a><span data-ttu-id="59f70-140">Ilmoitettu valmiiksi</span><span class="sxs-lookup"><span data-stu-id="59f70-140">Reported as finished</span></span>

<span data-ttu-id="59f70-141">Voit ilmoittaa aloitetun karanteenitilauksen valmiiksi avaamalla tilauksen ja valitsemalla toimintoruudusta **Ilmoita valmiiksi**.</span><span class="sxs-lookup"><span data-stu-id="59f70-141">To report a started quarantine order as finished, open the order, and select **Report as finished** on the Action Pane.</span></span> <span data-ttu-id="59f70-142">Nimike vapautetaan karanteenista, mutta sitä ei siirretä vielä tavalliseen varastoon.</span><span class="sxs-lookup"><span data-stu-id="59f70-142">The item is released from quarantine, but it isn't yet moved back to the regular warehouse.</span></span> <span data-ttu-id="59f70-143">Siirto takaisin tavalliseen varastoon voidaan käsitellä nimikkeen saapumisen kirjauskansiossa, joka voidaan alustaa Ilmoita valmiiksi -prosessin aikana.</span><span class="sxs-lookup"><span data-stu-id="59f70-143">The movement back to the regular warehouse can be processed via an item arrival journal that can be initialized during the report as finished process.</span></span>

### <a name="ended"></a><span data-ttu-id="59f70-144">Päättynyt</span><span class="sxs-lookup"><span data-stu-id="59f70-144">Ended</span></span>

<span data-ttu-id="59f70-145">Kun karanteenitilaus on päättynyt, nimike siirretään karanteenivarastosta takaisin tavalliseen varastoon.</span><span class="sxs-lookup"><span data-stu-id="59f70-145">When a quarantine order is ended, the item is moved from the quarantine warehouse back to the regular warehouse.</span></span> <span data-ttu-id="59f70-146">Nimiketapahtuman tilaksi asetetaan karanteenivarastossa *Myyty* ja tavallisessa varastossa *Ostettu*.</span><span class="sxs-lookup"><span data-stu-id="59f70-146">The status of the item transaction is set to *Sold* at the quarantine warehouse and *Purchased* at the regular warehouse.</span></span>

## <a name="quarantine-order-scrap"></a><span data-ttu-id="59f70-147">Karanteenitilausten hävikki</span><span class="sxs-lookup"><span data-stu-id="59f70-147">Quarantine order scrap</span></span>

<span data-ttu-id="59f70-148">Karanteenitilausprosessin aikana varastoa voidaan määrittää hävikiksi.</span><span class="sxs-lookup"><span data-stu-id="59f70-148">As part of the quarantine order process, you can scrap inventory.</span></span> <span data-ttu-id="59f70-149">Hävikkiä käsiteltäessä varaston tilaksi asetetaan *Myyty* ottotapahtumalla karanteenivarastosta.</span><span class="sxs-lookup"><span data-stu-id="59f70-149">When you process scrap, the status of the inventory is set to *Sold* by an issue transaction from the quarantine warehouse.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="59f70-150">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="59f70-150">Additional resources</span></span>

- [<span data-ttu-id="59f70-151">Varastoesto</span><span class="sxs-lookup"><span data-stu-id="59f70-151">Inventory blocking</span></span>](inventory-blocking.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
