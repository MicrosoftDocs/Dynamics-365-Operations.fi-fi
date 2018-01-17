---
title: Osittain varattujen siirtotilauserien vapautus
description: "Tässä ohjeaiheessa kerrotaan mobiililaitteen osittain varattujen siirtotilauksen vapautuksen erätoiminnon määrittämisestä ja käyttämisestä."
author: pjacobse
manager: AnnBe
ms.date: 05/26/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, Operations
ms.custom: 269384
ms.search.region: Global
ms.author: pjacobse
ms.search.validFrom: 2017-09-20
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0ca19ab9ed7a52328c5dd5252c418bb9343bdc2b
ms.openlocfilehash: 3aa9b24c40efb053507b10a7a219857480e0b75e
ms.contentlocale: fi-fi
ms.lasthandoff: 12/14/2017

---

# <a name="batch-release-of-partially-reserved-transfer-orders"></a><span data-ttu-id="8b9ff-103">Osittain varattujen siirtotilauserien vapautus</span><span class="sxs-lookup"><span data-stu-id="8b9ff-103">Batch release of partially reserved transfer orders</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="8b9ff-104">Osittain varattujen siirtotilausten vapauttamisen erätoiminto mahdollistaa siirtotilausten osittaisen vapauttamisen varastoon erätyön avulla.</span><span class="sxs-lookup"><span data-stu-id="8b9ff-104">The functionality for batch release of partially reserved transfer orders lets you partially release transfer orders to a warehouse by using a batch job.</span></span>
<span data-ttu-id="8b9ff-105">Koska voit vapauttaa osan määrästä, sinun ei tarvitse odottaa, että koko määrä on saatavilla varastossa ennen kuin vapautat tilauksen.</span><span class="sxs-lookup"><span data-stu-id="8b9ff-105">Because you have the option to release a partial quantity, you don’t have to wait for the whole order quantity to be available in the warehouse before you release an order.</span></span>

<span data-ttu-id="8b9ff-106">Tilausten vapauttaminen varastoon on varastonhallinnan lisäprosessi.</span><span class="sxs-lookup"><span data-stu-id="8b9ff-106">The release of orders to a warehouse is an advanced warehouse management process.</span></span> <span data-ttu-id="8b9ff-107">Tämä prosessi käsittää tehtäviä, kuten keräily, pakkaus ja toimitus, jotka varastotyöntekijä voi tehdä mobiililaitteen avulla.</span><span class="sxs-lookup"><span data-stu-id="8b9ff-107">This process involves activities, such as picking, packing, and shipping, that a warehouse worker can perform by using a mobile device.</span></span>

## <a name="where-it-applies"></a><span data-ttu-id="8b9ff-108">Käyttö</span><span class="sxs-lookup"><span data-stu-id="8b9ff-108">Where it applies</span></span>

<span data-ttu-id="8b9ff-109">Tässä toiminnossa siirtotilaukset vapautetaan varastoon erätyön avulla.</span><span class="sxs-lookup"><span data-stu-id="8b9ff-109">For this functionality, transfer orders are released to a warehouse by using a batch job.</span></span> <span data-ttu-id="8b9ff-110">Tämä toiminto on hyödyllinen, jos sinulla ei ole varastossa riittävästi varastoa, mutta haluat siirtää nimikkeitä varastosta toiseen.</span><span class="sxs-lookup"><span data-stu-id="8b9ff-110">This functionality is useful when you don’t have enough inventory in the warehouse, but you still want to transfer items from one warehouse to another.</span></span>

## <a name="how-it-is-set-up"></a><span data-ttu-id="8b9ff-111">Määritysohjeet</span><span class="sxs-lookup"><span data-stu-id="8b9ff-111">How it is set up</span></span>

### <a name="specify-fulfillment-criteria-for-transfer-orders-and-sales-orders"></a><span data-ttu-id="8b9ff-112">Määritä myyntitilausten ja siirtotilausten täyttämisehdot</span><span class="sxs-lookup"><span data-stu-id="8b9ff-112">Specify fulfillment criteria for transfer orders and sales orders</span></span>

<span data-ttu-id="8b9ff-113">Täyttämisehtojen tulee täyttyä ennen kuin tilauksen voi vapauttaa osittain varastoon erässä.</span><span class="sxs-lookup"><span data-stu-id="8b9ff-113">Before an order can be partially released to a warehouse in a batch, the fulfillment criteria must be met.</span></span> <span data-ttu-id="8b9ff-114">Täyttämisehdot määritetään täyttämiskäytännöissä.</span><span class="sxs-lookup"><span data-stu-id="8b9ff-114">These fulfillment criteria are determined by the fulfillment policy.</span></span>

<span data-ttu-id="8b9ff-115">Siirto- ja myyntitilausten täyttämiskäytännöt määritetään yrityksen tasolla.</span><span class="sxs-lookup"><span data-stu-id="8b9ff-115">Fulfillment policies for transfer orders and sales orders are specified at the company level.</span></span> <span data-ttu-id="8b9ff-116">Täyttämiskäytännön määrityksistä riippuu, hyväksytäänkö vai hylätäänkö tilausten vapauttaminen eräajossa.</span><span class="sxs-lookup"><span data-stu-id="8b9ff-116">Depending on the setup of the fulfillment policy, the release of orders in a batch will be accepted or rejected.</span></span> <span data-ttu-id="8b9ff-117">Tilaukset käsitellään sitten tavalliseen tapaan.</span><span class="sxs-lookup"><span data-stu-id="8b9ff-117">The orders will then be processed accordingly.</span></span>

-   <span data-ttu-id="8b9ff-118">Siirto- ja myyntitilauksille luodaan täyttämiskäytäntöjä valitsemalla **Varastonhallinta** \> **Asetukset** \> **Varastoon vapauttaminen** \> **Täyttämiskäytäntö** ja kirjoittamalla sitten käytännölle nimi ja kuvaus.</span><span class="sxs-lookup"><span data-stu-id="8b9ff-118">To create fulfillment policies for transfer orders and sales orders, click **Warehouse management** \> **Setup** \> **Release to warehouse** \> **Fulfillment policy**, and then create a fulfillment policy by entering a name and a description.</span></span>

-   <span data-ttu-id="8b9ff-119">Voit määrittää täytäntöönpanoasteen, arvotyypin ja viestin, joka näytetään, jos käytäntöä rikotaan valitsemalla **Varastonhallinta** \> **Asetukset** \> **Vapauta varastoon** \> **Täyttämiskäytäntö**, ja määritä sitten **Täytäntöönpanoaste**, **Arvotyyppi**, ja **Viesti täytäntöönpanon rikkomuksista** -kentät.</span><span class="sxs-lookup"><span data-stu-id="8b9ff-119">To specify a fulfillment rate, a value type, and the message that is shown if the fulfillment policy is violated, click **Warehouse management** \> **Setup** \> **Release to warehouse** \> **Fulfillment policy**, and then set the **Fulfillment rate**, **Value type**, and **Fulfillment violation message** fields.</span></span>

### <a name="set-the-fulfillment-policies-for-transfer-orders-and-sales-orders"></a><span data-ttu-id="8b9ff-120">Määritä myyntitilausten ja siirtotilausten täyttämiskäytännöt</span><span class="sxs-lookup"><span data-stu-id="8b9ff-120">Set the fulfillment policies for transfer orders and sales orders</span></span>

-   <span data-ttu-id="8b9ff-121">Voit asettaa siirtotilausten täyttämiskäytännöt valitsemalla **Varastonhallinta** \> **Asetukset** \> **Varasto ja varastonhallinnan parametrit** \> **Siirtotilaukset** \> **Varastonhallinta** ja valitsemalla sitten siirtotilauksen täyttämiskäytännön.</span><span class="sxs-lookup"><span data-stu-id="8b9ff-121">To set the fulfillment policies for transfer orders, click **Inventory management** \> **Setup** \> **Inventory and warehouse management parameters** \> **Transfer orders** \> **Warehouse management**, and then select a transfer order fulfillment policy.</span></span>

-   <span data-ttu-id="8b9ff-122">Myyntitilausten täyttämiskäytännöt voit asettaa kohdassa **Myyntireskontra** \> **Asetukset** \> **Myyntireskontran parametrit** \> **Varastonhallinta** ja valitsemalla myyntitilauksen täyttämiskäytännön.</span><span class="sxs-lookup"><span data-stu-id="8b9ff-122">To set the fulfillment policies for sales orders, click **Accounts receivable** \> **Setup** \> **Accounts receivable parameters** \> **Warehouse management**, and then select a sales order fulfillment policy.</span></span>

## <a name="allow-release-in-a-batch-and-specify-the-quantity-that-should-be-release-in-a-batch"></a><span data-ttu-id="8b9ff-123">Salli vapauttaminen eräajossa ja aseta erässä vapautettava määrä</span><span class="sxs-lookup"><span data-stu-id="8b9ff-123">Allow release in a batch and specify the quantity that should be release in a batch</span></span>

<span data-ttu-id="8b9ff-124">Tilaukset vapautetaan varastoon erässä erätyön avulla.</span><span class="sxs-lookup"><span data-stu-id="8b9ff-124">A batch job is used to release orders to a warehouse in a batch.</span></span> <span data-ttu-id="8b9ff-125">Erätyössä ajettavien tilausten tunnistamiseen käytettävät parametrit asetetaan erätyössä itsessään.</span><span class="sxs-lookup"><span data-stu-id="8b9ff-125">The parameters that distinguish the orders that should be run in a batch job are set on the batch job itself.</span></span>

<span data-ttu-id="8b9ff-126">**Määrä**-parametri määrää, vapautetaanko erässä koko määrä vai fyysisesti varattu määrä.</span><span class="sxs-lookup"><span data-stu-id="8b9ff-126">The **Quantity** parameter specifies whether the whole quantity or the physically reserved quantity should be released in the batch.</span></span> <span data-ttu-id="8b9ff-127">**Salli osittain vapautettujen tilausten vapautus** -parametri määrää, hyväksytäänkö vai hylätäänkö erässä olevat tilaukset, jos ne on vapautettu osittain aiemmin.</span><span class="sxs-lookup"><span data-stu-id="8b9ff-127">The **Allow release of partially released orders** parameter determines whether orders in the batch should be accepted or rejected if they were partially released earlier.</span></span>

-   <span data-ttu-id="8b9ff-128">Voit määrittää **Määrä**- ja **Salli osittain vapautettujen tilausten vapautus** -parametrit siirtotilauksille kohdassa **Varastonhallinta** \> **Vapauta varastoon** \> **Siirtotilauksien automaattinen vapauttaminen**.</span><span class="sxs-lookup"><span data-stu-id="8b9ff-128">To set the **Quantity** and **Allow release of partially released orders** parameters for transfer orders, click **Warehouse management** \> **Release to warehouse** \> **Automatic release of transfer orders**.</span></span>

-   <span data-ttu-id="8b9ff-129">Voit määrittää **Määrä**- ja **Salli osittain vapautettujen tilausten vapautus** -parametrit myyntitilauksille kohdassa **Varastonhallinta** \> **Vapauta varastoon** \> **Myyntitilauksien automaattinen vapauttaminen**.</span><span class="sxs-lookup"><span data-stu-id="8b9ff-129">To set the **Quantity** and **Allow release of partially released orders** parameters for sales orders, click **Warehouse management** \> **Release to warehouse** \> **Automatic release of sales orders**.</span></span>

