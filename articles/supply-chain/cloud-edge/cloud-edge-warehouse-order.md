---
title: Varastotilausten pilvi- ja reunapalvelujen scale unitit
description: Tässä aiheessa käsitellään varastotilausominaisuutta, jota käytetään varaston scale unitin työkuorman osana.
author: perlynne
manager: tfeyr
ms.date: 01/14/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSWarehouseOrderLine, WHSWarehouseReceiptEntry, PurchTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: SCM
ms.author: perlynne
ms.search.validFrom: 2021-01-14
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: c04127b9fe621d962be2d7fe06358b3bd1b78916
ms.sourcegitcommit: 289e9183d908825f4c8dcf85d9affd4119238d0c
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/02/2021
ms.locfileid: "5105704"
---
# <a name="warehouse-orders-for-cloud-and-edge-scale-units"></a><span data-ttu-id="be5e1-103">Varastotilausten pilvi- ja reunapalvelujen scale unitit</span><span class="sxs-lookup"><span data-stu-id="be5e1-103">Warehouse orders for cloud and edge scale units</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

> [!WARNING]
> <span data-ttu-id="be5e1-104">Kaikkia liiketoimintatoimintoja ei tueta kokonaisuudessaan julkisessa esiversiossa, kun scale unitin kuormituksia käytetään.</span><span class="sxs-lookup"><span data-stu-id="be5e1-104">Not all business functionality is fully supported in the public preview when scale unit workloads are used.</span></span> <span data-ttu-id="be5e1-105">Jos scale unitit ovat käytössä, on varmistettava, että vain niitä prosesseja käytetään, joiden tuesta nimenomaisesti ilmoitetaan tässä aiheessa.</span><span class="sxs-lookup"><span data-stu-id="be5e1-105">If you're using scale units, be sure to use only those processes that this topic explicitly describes as supported.</span></span>

## <a name="what-are-warehouse-orders"></a><span data-ttu-id="be5e1-106">Mitä varastotilaukset ovat?</span><span class="sxs-lookup"><span data-stu-id="be5e1-106">What are warehouse orders?</span></span>

<span data-ttu-id="be5e1-107">*Varastotilaukset* ovat tilaustyyppi, joka luotiin tukemaan keskusta ja scale unitia hyödyntäviä varaston käyttöönottoja.</span><span class="sxs-lookup"><span data-stu-id="be5e1-107">*Warehouse orders* are a type of order that was created to support hub and scale unit warehouse deployments.</span></span> <span data-ttu-id="be5e1-108">Niiden avulla voidaan vastaanottaa varastoa, kun varastotyökuorma suoritetaan scale unitissa.</span><span class="sxs-lookup"><span data-stu-id="be5e1-108">They let you receive inventory when you're running a warehouse workload on a scale unit.</span></span> <span data-ttu-id="be5e1-109">Niitä käytetään tällä hetkellä vain ostotilausten yhteydessä.</span><span class="sxs-lookup"><span data-stu-id="be5e1-109">They are currently used only with purchase orders.</span></span>

<span data-ttu-id="be5e1-110">Varastotilauksia käytetään varastonhallintaprosessien osana esimerkiksi silloin, kun varastosovelluksella kirjataan fyysinen käytettävissä oleva varasto saapuvan ostotilauksen käsittelyn aikana.</span><span class="sxs-lookup"><span data-stu-id="be5e1-110">Warehouse orders are used as part of warehouse management processing, such as when the warehouse app is used to register physical on-hand inventory during processing of an inbound purchase order.</span></span> <span data-ttu-id="be5e1-111">Varastotilaukset luodaan *Vapauta varastoon* -prosessin osana. Tätä prosessia voi käyttää ostotilauksissa, jotka määrittävät scale unit -varaston, ja nimikkeissä, joissa varastonhallintaprosessien käyttö on otettu käyttöön.</span><span class="sxs-lookup"><span data-stu-id="be5e1-111">Warehouse orders are created as part of the *Release to warehouse* process that is available for purchase orders that specify a scale unit warehouse and items that are enabled to use warehouse management processes.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="be5e1-112">Varastotilaukset ovat käytettävissä vain käyttöönotoissa, joissa käytetään [varastonhallinnan kuormitusten pilvi- ja reunapalvelujen scale uniteja](cloud-edge-workload-warehousing.md).</span><span class="sxs-lookup"><span data-stu-id="be5e1-112">Warehouse orders are available only in deployments that use [warehouse management workloads for cloud and edge scale units](cloud-edge-workload-warehousing.md).</span></span>

## <a name="create-a-warehouse-order"></a><span data-ttu-id="be5e1-113">Varastotilauksen luominen</span><span class="sxs-lookup"><span data-stu-id="be5e1-113">Create a warehouse order</span></span>

<span data-ttu-id="be5e1-114">Varastotilaus luodaan seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="be5e1-114">To create a warehouse order, follow these steps.</span></span>

1. <span data-ttu-id="be5e1-115">Kirjaudu Microsoftin Dynamics 365 Supply Chain Managementn esiintymään, joka suoritetaan keskuksessa.</span><span class="sxs-lookup"><span data-stu-id="be5e1-115">Sign in to the instance of Microsoft Dynamics 365 Supply Chain Management that is running on the hub.</span></span> <span data-ttu-id="be5e1-116">(*Vapauta varastoon* -prosessi on käynnistettävä keskukseen kirjautuneena.)</span><span class="sxs-lookup"><span data-stu-id="be5e1-116">(You must initiate the *Release to warehouse* process while you're signed in on the hub.)</span></span>
1. <span data-ttu-id="be5e1-117">Siirry kohtaan **Hankinta ja alihankinta \> Ostotilaukset \> Kaikki ostotilaukset**.</span><span class="sxs-lookup"><span data-stu-id="be5e1-117">Go to **Procurement and sourcing \> Purchase orders \> All purchase orders**.</span></span>
1. <span data-ttu-id="be5e1-118">Valitse toimintoruudussa **Varasto**-välilehden **Toiminnot**-ryhmässä **Vapauta varastoon**.</span><span class="sxs-lookup"><span data-stu-id="be5e1-118">On the Action Pane, on the **Warehouse** tab, in the **Actions** group, select **Release to warehouse**.</span></span>
1. <span data-ttu-id="be5e1-119">Liittyviä varastotilauksia rivejä voi tarkastella avaamalla liittyvän ostotilauksen, valitsemalla rivin **Ostotilausrivit**-osassa ja valitsemalla sitten työkalurivillä **Varasto \> Varastotilausrivit**.</span><span class="sxs-lookup"><span data-stu-id="be5e1-119">To view the related warehouse order lines, open the relevant purchase order, select a line in the **Purchase order lines** section, and then, on the toolbar, select **Warehouse \> Warehouse order lines**.</span></span> <span data-ttu-id="be5e1-120">Kaikki rivit voidaan näyttää valitsemalla **Varastonhallinta \> Kyselyt ja raportit \> Varastotilausrivit**.</span><span class="sxs-lookup"><span data-stu-id="be5e1-120">To view all the lines, go to **Warehouse management \> Inquiries and reports \> Warehouse order lines**.</span></span>

## <a name="cancel-a-warehouse-order"></a><span data-ttu-id="be5e1-121">Varastotilauksen peruuttaminen</span><span class="sxs-lookup"><span data-stu-id="be5e1-121">Cancel a warehouse order</span></span>

<span data-ttu-id="be5e1-122">*Vapauta varastoon* -prosessin osana keskus linkittää ostotilauksen varastotapahtumat varastotilauksiin ja lukitsee niiden päivittämisen.</span><span class="sxs-lookup"><span data-stu-id="be5e1-122">As part of the *Release to warehouse* process, purchase order inventory transactions are linked to warehouse orders and locked from being updated by the hub.</span></span> <span data-ttu-id="be5e1-123">Jos vapautus varastoon on tehty vahingossa tai jos varastotilausrivien luonti halutaan peruuttaa jostain muusta syystä, varastotilausrivien peruuttamista voidaan pyytää.</span><span class="sxs-lookup"><span data-stu-id="be5e1-123">If you released to the warehouse by mistake, or if you have some other reason to reverse the creation of warehouse order lines, you can request to cancel warehouse order lines.</span></span>

<span data-ttu-id="be5e1-124">Varastotilausrivit peruutetaan seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="be5e1-124">To cancel warehouse order lines, follow these steps.</span></span>

1. <span data-ttu-id="be5e1-125">Kirjaudu Supply Chain Managementin esiintymään, joka suoritetaan keskuksessa.</span><span class="sxs-lookup"><span data-stu-id="be5e1-125">Sign in to the Supply Chain Management instance that is running on the hub.</span></span>
1. <span data-ttu-id="be5e1-126">Valitse **Varastonhallinta \> Kyselyt ja raportit \> Varastotilausrivit**.</span><span class="sxs-lookup"><span data-stu-id="be5e1-126">Go to **Warehouse management \> Inquiries and reports \> Warehouse order lines**.</span></span>
1. <span data-ttu-id="be5e1-127">Valitse rivi.</span><span class="sxs-lookup"><span data-stu-id="be5e1-127">Select the relevant line.</span></span>
1. <span data-ttu-id="be5e1-128">Valitse toimintoruudussa **Peruuta varastotilausrivit**.</span><span class="sxs-lookup"><span data-stu-id="be5e1-128">On the Action Pane, select **Cancel warehouse order lines**.</span></span>

> [!NOTE]
> <span data-ttu-id="be5e1-129">Sellaisten rivien peruuttamispyyntö hylätään, jotka jo odottavat peruuttamista tai joita käsitellään aktiivisesti työkuorman scale unitissa suorittavassa varastossa.</span><span class="sxs-lookup"><span data-stu-id="be5e1-129">The request to cancel lines will be denied for any lines that are already pending cancellation or that are actively being processed at a warehouse that is running its workload on a scale unit.</span></span>

## <a name="monitor-a-warehouse-order"></a><span data-ttu-id="be5e1-130">Varastotilauksen seuraaminen</span><span class="sxs-lookup"><span data-stu-id="be5e1-130">Monitor a warehouse order</span></span>

<span data-ttu-id="be5e1-131">**Varastotilausrivit**-näkymässä voi seurata saapuvan vastaanoton etenemistä tarkastelemalla **Jäljellä oleva vastaanotettava määrä** -sarakkeen arvoja.</span><span class="sxs-lookup"><span data-stu-id="be5e1-131">In the **Warehouse order lines** view, you can monitor the progress of inbound receiving by reviewing the values in the **Quantity left to receive** column.</span></span> <span data-ttu-id="be5e1-132">Varastosovelluksella tehtävään työhön liittyviä tietoja voi tarkastella jollakin seuraavista tavoista:</span><span class="sxs-lookup"><span data-stu-id="be5e1-132">To view details that are related to work that is done by using the warehouse app, follow one of these steps.</span></span>

- <span data-ttu-id="be5e1-133">Valitse **Varastonhallinta \> Kyselyt ja raportit \> Varastotilausrivit** ja etsi rivit suodattimen avulla.</span><span class="sxs-lookup"><span data-stu-id="be5e1-133">Go to **Warehouse management \> Inquiries and reports \> Warehouse order lines**, and use the filter to find the lines that you're looking for.</span></span>
- <span data-ttu-id="be5e1-134">Valitse **Hankinta \> Ostotilaukset \> Kaikki ostotilaukset** ja avaa kyseinen ostotilaus.</span><span class="sxs-lookup"><span data-stu-id="be5e1-134">Go to **Procurement and sourcing \> Purchase orders \> All purchase orders**, and open the relevant purchase order.</span></span> <span data-ttu-id="be5e1-135">Valitse **Ostotilausrivit**-osassa vähintään yksi rivi ja valitse sitten työkalurivillä **Varasto \> Varaston vastaanottoviennit**.</span><span class="sxs-lookup"><span data-stu-id="be5e1-135">In the **Purchase order lines** section, select one or more lines, and then, on the toolbar, select **Warehouse \> Warehouse receipt entries**.</span></span>
