---
title: Karanteenitilaukset
description: Tässä ohjeaiheessa kuvataan varaston käytön estämistä karanteenitilauksilla.
author: perlynne
manager: tfehr
ms.date: 11/02/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
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
ms.openlocfilehash: 08bb75228c79a0575e8476f41c935d0a03e00f35
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5209607"
---
# <a name="quarantine-orders"></a><span data-ttu-id="a9057-103">Karanteenitilaukset</span><span class="sxs-lookup"><span data-stu-id="a9057-103">Quarantine orders</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a9057-104">Tässä ohjeaiheessa kuvataan varaston käytön estämistä karanteenitilauksilla.</span><span class="sxs-lookup"><span data-stu-id="a9057-104">This topic describes how quarantine orders are used to block inventory.</span></span>

<span data-ttu-id="a9057-105">Varaston käyttö voidaan estää karanteenitilauksilla.</span><span class="sxs-lookup"><span data-stu-id="a9057-105">Quarantine orders can be used to block inventory.</span></span> <span data-ttu-id="a9057-106">Haluat ehkä esimerkiksi siirtää nimikkeitä karanteeniin laadunvalvontasyistä.</span><span class="sxs-lookup"><span data-stu-id="a9057-106">For example, you might want to quarantine items for quality control reasons.</span></span> <span data-ttu-id="a9057-107">Karanteeniin asetettu varasto siirretään karanteenivarastoon.</span><span class="sxs-lookup"><span data-stu-id="a9057-107">Inventory that has been quarantined is transferred to a quarantine warehouse.</span></span> <span data-ttu-id="a9057-108">**Huomautus:** Jos käytät varaston lisähallintaprosesseja (Varastonhallinnassa), karanteenitilauksen käsittelyä käytetään vain palautusmyyntitilauksille.</span><span class="sxs-lookup"><span data-stu-id="a9057-108">**Note:** If you're using advanced warehouse management processes (in Warehouse management), quarantine order processing is used only for return sales orders.</span></span>

## <a name="quarantine-on-hand-inventory-items"></a><span data-ttu-id="a9057-109">Käytettävissä olevien varastonimikkeiden siirtäminen karanteeniin</span><span class="sxs-lookup"><span data-stu-id="a9057-109">Quarantine on-hand inventory items</span></span>
<span data-ttu-id="a9057-110">Kun siirrät nimikkeitä karanteeniin, voit joko luoda karanteenitilauksen manuaalisesti tai määrittää järjestelmän luomaan karanteenitilaukset automaattisesti saapuvien käsittelyn aikana.</span><span class="sxs-lookup"><span data-stu-id="a9057-110">When you quarantine items, you can either create the quarantine orders manually or set up the system to create the quarantine orders automatically during inbound processing.</span></span> <span data-ttu-id="a9057-111">Jos haluat luoda karanteenitilauksia automaattisesti, valitse **Karanteeninhallinta**-vaihtoehto **Nimikemalliryhmät**-sivun **Varastokäytännöt**-välilehdestä.</span><span class="sxs-lookup"><span data-stu-id="a9057-111">To create quarantine orders automatically, select the **Quarantine management** option on the **Inventory policies** tab on the **Item model groups** page.</span></span> <span data-ttu-id="a9057-112">Sinun täytyy myös määrittää oletuskaranteenivarasto vastaanottavien varastojen **Karanteenivarasto**-kentässä.</span><span class="sxs-lookup"><span data-stu-id="a9057-112">You must also specify a default quarantine warehouse in the **Quarantine warehouse** field for the receiving warehouses.</span></span> <span data-ttu-id="a9057-113">Karanteeniin siirretyt nimikkeet siirretään Supply Chain Managementissa automaattisesti karanteenivarastoon, kun fyysinen käytettävissä oleva varasto kirjataan ostotilauksen tai tuotantotilauksen kautta.</span><span class="sxs-lookup"><span data-stu-id="a9057-113">When the physically on-hand inventory is recorded in a purchase order or production order, quarantined items are automatically moved to a quarantine warehouse in Supply Chain Management.</span></span> <span data-ttu-id="a9057-114">Siirto tapahtuu, koska karanteenitilauksen tilaksi muuttuu **Aloitettu**.</span><span class="sxs-lookup"><span data-stu-id="a9057-114">This movement occurs because the status of the quarantine order is changed to **Started**.</span></span> <span data-ttu-id="a9057-115">Luodessasi karanteenitilauksia manuaalisesti ei ole tarpeen määrittää nykyistä nimikettä karantiinihallintaa varten liitetyssä nimikemalliryhmässä.</span><span class="sxs-lookup"><span data-stu-id="a9057-115">When you create quarantine orders manually, the item doesn't have to be set up for quarantine management in the associated item model group.</span></span> <span data-ttu-id="a9057-116">Tässä prosessissa sinun täytyy määrittää käytettävissä oleva varasto, joka on asetettava karanteeniin, sekä käytettävä karanteenivarasto.</span><span class="sxs-lookup"><span data-stu-id="a9057-116">For this process, you must specify the on-hand inventory that should be quarantined and the quarantine warehouse that should be used.</span></span> <span data-ttu-id="a9057-117">Voit käyttää prosessin suunnittelussa apuna karanteenitilauksen tiloja.</span><span class="sxs-lookup"><span data-stu-id="a9057-117">You can use the quarantine order statuses to help plan the process.</span></span>

## <a name="quarantine-order-statuses"></a><span data-ttu-id="a9057-118">Karanteenitilausten tilat</span><span class="sxs-lookup"><span data-stu-id="a9057-118">Quarantine order statuses</span></span>
<span data-ttu-id="a9057-119">Karanteenitilauksilla voi olla seuraavanlaisia tiloja:</span><span class="sxs-lookup"><span data-stu-id="a9057-119">Quarantine orders can have the following statuses:</span></span>

-   <span data-ttu-id="a9057-120">Luotu</span><span class="sxs-lookup"><span data-stu-id="a9057-120">Created</span></span>
-   <span data-ttu-id="a9057-121">Aloitettu</span><span class="sxs-lookup"><span data-stu-id="a9057-121">Started</span></span>
-   <span data-ttu-id="a9057-122">Ilmoitettu valmiiksi</span><span class="sxs-lookup"><span data-stu-id="a9057-122">Reported as finished</span></span>
-   <span data-ttu-id="a9057-123">Päättynyt</span><span class="sxs-lookup"><span data-stu-id="a9057-123">Ended</span></span>

### <a name="created"></a><span data-ttu-id="a9057-124">Luotu</span><span class="sxs-lookup"><span data-stu-id="a9057-124">Created</span></span>

<span data-ttu-id="a9057-125">Kun karanteenitilaus on luotu manuaalisesti, mutta nimikettä ei ole vielä sijoitettu karanteenivarastoon, karanteenitilauksen tilana on **Luotu**.</span><span class="sxs-lookup"><span data-stu-id="a9057-125">When a quarantine order has been created manually, but the item isn't yet in the quarantine warehouse, the quarantine order has a status of **Created**.</span></span> <span data-ttu-id="a9057-126">Järjestelmä luo kaksi varastotapahtumaa.</span><span class="sxs-lookup"><span data-stu-id="a9057-126">Two inventory transactions are generated.</span></span> <span data-ttu-id="a9057-127">Yksi tapahtumista on ottotapahtuma, jonka tila voi olla **Tilauksessa**, **Varattu fyysinen** tai **Keräilty**.</span><span class="sxs-lookup"><span data-stu-id="a9057-127">One transaction is an issue transaction that can have a status of **On order**, **Reserved physical**, or **Picked**.</span></span> <span data-ttu-id="a9057-128">Toinen on vastaanottotapahtuma, jonka tilana karanteenivarastossa voi olla **Tilattu** tai **Rekisteröity**.</span><span class="sxs-lookup"><span data-stu-id="a9057-128">The other transaction is a receipt transaction that can have a status of **Ordered** or **Registered** at the quarantine warehouse.</span></span> <span data-ttu-id="a9057-129">Voit varata, keräillä ja rekisteröidä varaston päivityksiä käyttämällä tavanomaisia prosesseja.</span><span class="sxs-lookup"><span data-stu-id="a9057-129">You can reserve, pick, and register updates to the inventory by using the usual processes.</span></span>

### <a name="started"></a><span data-ttu-id="a9057-130">Aloitettu</span><span class="sxs-lookup"><span data-stu-id="a9057-130">Started</span></span>

<span data-ttu-id="a9057-131">Kun karanteenitilauksen tilana on **Aloitettu**, varasto siirretään tavallisesta varastosta karanteenivarastoon, ja järjestelmä luo kaksi varastotapahtumaa.</span><span class="sxs-lookup"><span data-stu-id="a9057-131">When a quarantine order has a status of **Started**, the inventory is transferred from the regular warehouse to the quarantine warehouse, and two inventory transactions are generated.</span></span> <span data-ttu-id="a9057-132">Yhdellä tapahtumalla on tila **Toimitettu**, ja toisella tapahtumalla on tila **Vastaanotettu**.</span><span class="sxs-lookup"><span data-stu-id="a9057-132">One transaction has a status of **Deducted**, and the other transaction has a status of **Received**.</span></span> <span data-ttu-id="a9057-133">Samalla luodaan kaksi varastotapahtumaa palautussiirron käsittelyä varten.</span><span class="sxs-lookup"><span data-stu-id="a9057-133">At the same time, two inventory transactions are created to handle the return transfer.</span></span> <span data-ttu-id="a9057-134">Näitä tapahtumia ei päivätä.</span><span class="sxs-lookup"><span data-stu-id="a9057-134">These transactions aren't dated.</span></span> <span data-ttu-id="a9057-135">Yhdellä tapahtumalla on tila **Varattu fyysinen**, ja toisella tapahtumalla on tila **Tilattu**.</span><span class="sxs-lookup"><span data-stu-id="a9057-135">One transaction has a status of **Reserved physical**, and the other transaction has a status of **Ordered**.</span></span>

### <a name="reported-as-finished"></a><span data-ttu-id="a9057-136">Ilmoitettu valmiiksi</span><span class="sxs-lookup"><span data-stu-id="a9057-136">Reported as finished</span></span>

<span data-ttu-id="a9057-137">Valitsemalla **Ilmoita valmiiksi**, voit ilmoittaa aloitetun karanteenitilauksen valmiiksi.</span><span class="sxs-lookup"><span data-stu-id="a9057-137">By clicking **Report as finished**, you can report a started quarantine order as finished.</span></span> <span data-ttu-id="a9057-138">Nimike vapautetaan karanteenista, mutta sitä ei siirretä vielä tavalliseen varastoon.</span><span class="sxs-lookup"><span data-stu-id="a9057-138">The item is released from quarantine but isn't yet moved back to the regular warehouse.</span></span> <span data-ttu-id="a9057-139">Siirto takaisin tavalliseen varastoon voidaan käsitellä nimikkeen saapumisen kirjauskansiossa, joka voidaan alustaa Ilmoita valmiiksi -prosessin aikana.</span><span class="sxs-lookup"><span data-stu-id="a9057-139">The movement back to the regular warehouse can be processed via an Item arrival journal that can be initialized during the Report as finished process.</span></span>

### <a name="ended"></a><span data-ttu-id="a9057-140">Päättynyt</span><span class="sxs-lookup"><span data-stu-id="a9057-140">Ended</span></span>

<span data-ttu-id="a9057-141">Kun karanteenitilaus on päättynyt, nimike siirretään karanteenivarastosta takaisin tavalliseen varastoon.</span><span class="sxs-lookup"><span data-stu-id="a9057-141">When a quarantine order is ended, the item is moved from the quarantine warehouse back to the regular warehouse.</span></span> <span data-ttu-id="a9057-142">Nimiketapahtuman tilaksi asetetaan karanteenivarastossa **Myyty** ja tavallisessa varastossa **Ostettu**.</span><span class="sxs-lookup"><span data-stu-id="a9057-142">The status of the item transaction is set to **Sold** at the quarantine warehouse and **Purchased** at the regular warehouse.</span></span>

## <a name="quarantine-order-scrap"></a><span data-ttu-id="a9057-143">Karanteenitilausten hävikki</span><span class="sxs-lookup"><span data-stu-id="a9057-143">Quarantine order scrap</span></span>
<span data-ttu-id="a9057-144">Karanteenitilausprosessin aikana varastoa voidaan määrittää hävikiksi.</span><span class="sxs-lookup"><span data-stu-id="a9057-144">As part of the quarantine order process, you can scrap inventory.</span></span> <span data-ttu-id="a9057-145">Hävikkiä käsiteltäessä varaston tilaksi asetetaan **Myyty** ottotapahtumalla karanteenivarastosta.</span><span class="sxs-lookup"><span data-stu-id="a9057-145">When you process scrap, the status of the inventory will be set to **Sold** by an issue transaction from the quarantine warehouse.</span></span>

<a name="additional-resources"></a><span data-ttu-id="a9057-146">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="a9057-146">Additional resources</span></span>
--------

[<span data-ttu-id="a9057-147">Varastoesto</span><span class="sxs-lookup"><span data-stu-id="a9057-147">Inventory blocking</span></span>](inventory-blocking.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]