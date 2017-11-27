---
title: "Lähtevien käsittely"
description: "Tässä aiheessa on yleiskatsaus varastonhallinnan lähtevien tuotteiden prosessista."
author: perlynne
manager: AnnBe
ms.date: 10/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: WMSOrder, WMSShipment, MCRPickingWorkbench, WMSPickingRegistration, CustomFilterGroup
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: Core, Operations
ms.custom: 274363
ms.assetid: 375807b2-a426-4f1b-bc1f-2fe00fd48413
ms.search.region: global
ms.search.industry: Distribution
ms.author: perlynne
ms.dyn365.ops.intro: AX 7.0.0
ms.search.validFrom: 2016-02-28
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 1b8b17b719713097d77a117cca53eff6886ff1c7
ms.contentlocale: fi-fi
ms.lasthandoff: 11/03/2017

---

# <a name="outbound-process"></a><span data-ttu-id="370f4-103">Lähtevien käsittely</span><span class="sxs-lookup"><span data-stu-id="370f4-103">Outbound process</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="370f4-104">Tässä aiheessa on yleiskatsaus varastonhallinnan lähtevien tuotteiden prosessista.</span><span class="sxs-lookup"><span data-stu-id="370f4-104">This topic provides an overview of the outbound process in Inventory management.</span></span>

## <a name="output-orders"></a><span data-ttu-id="370f4-105">Toimitustilaukset</span><span class="sxs-lookup"><span data-stu-id="370f4-105">Output orders</span></span>

<span data-ttu-id="370f4-106">Myyntitilausrivit ja siirtotilausrivit linkitetään toimitustilausten avulla lähtevien keräystoimintoihin, jotka käyttävät keräysluetteloita.</span><span class="sxs-lookup"><span data-stu-id="370f4-106">Output orders are used to link sales order lines and transfer order lines with the outbound picking processes that use picking lists.</span></span>

<span data-ttu-id="370f4-107">Kun keräysluetteloita muodostettaan joko myynti- tai siirtotilauksista, toimitustilaukset ja toimitukset luodaan automaattisesti.</span><span class="sxs-lookup"><span data-stu-id="370f4-107">When picking lists are generated from either sales orders or transfer orders, output orders and shipments are automatically created.</span></span> <span data-ttu-id="370f4-108">Keräysluettelolla on yksi-yhteen-suhde toimitukseen.</span><span class="sxs-lookup"><span data-stu-id="370f4-108">A picking list has a one-to-one relationship with a shipment.</span></span> <span data-ttu-id="370f4-109">Siirtotilauksen lähetystä tai myyntitilauksen pakkausluetteloa voi käsitellä lähetyksestä.</span><span class="sxs-lookup"><span data-stu-id="370f4-109">The transfer order shipment or the sales order packing slip can be processed from the shipment.</span></span> 

<span data-ttu-id="370f4-110">Seuraavassa kaaviossa on yhteenveto toimitustilausten prosessista.</span><span class="sxs-lookup"><span data-stu-id="370f4-110">The following diagram shows an overview of the process for outbound orders.</span></span> 

<span data-ttu-id="370f4-111">[![Yhteenveto toimitustilausten prosessista.](./media/outbound-order.png)](./media/outbound-order.png)</span><span class="sxs-lookup"><span data-stu-id="370f4-111">[![Overview of the outbound order process](./media/outbound-order.png)](./media/outbound-order.png)</span></span>

<span data-ttu-id="370f4-112">Lähtevien sääntöjen avulla voit määrittää, miten ohjelma toteuttaa lähtevien käsittelyn.</span><span class="sxs-lookup"><span data-stu-id="370f4-112">You can set up outbound rules to define how the program should handle the outbound process.</span></span> <span data-ttu-id="370f4-113">Voit hallita lähetysprosessia näiden sääntöjen avulla.</span><span class="sxs-lookup"><span data-stu-id="370f4-113">You can use these rules to control the shipment process.</span></span> <span data-ttu-id="370f4-114">Näiden sääntöjen avulla voit hallita, mihin prosessin vaiheeseen lähetyksen voi siirtää.</span><span class="sxs-lookup"><span data-stu-id="370f4-114">In particular, you can use the rules to control which stage in the process a shipment can be sent during.</span></span> <span data-ttu-id="370f4-115">Seuraavat asetukset määrittävät, miten lähtevän tavaran prosessit käsitellään.</span><span class="sxs-lookup"><span data-stu-id="370f4-115">The following settings define how the outbound processes are handled.</span></span>

## <a name="picking-route-status-for-sales-and-transfer-orders"></a><span data-ttu-id="370f4-116">Myynti- ja siirtotilausten keräilyreitin tila</span><span class="sxs-lookup"><span data-stu-id="370f4-116">Picking route status for sales and transfer orders</span></span> 

<span data-ttu-id="370f4-117">Siirry kohtaan **Myyntireskontra** \> **Asetukset** \> **Myyntireskontran parametrit** ja valitse sitten **Päivitykset**-välilehdellä arvo **Keräilyreitin tila** -kenttään.</span><span class="sxs-lookup"><span data-stu-id="370f4-117">Go to **Account receivable** \> **Setup** \> **Account receivable parameters**, and then, on the **Updates** tab, select a value in the **Picking route status** field.</span></span>

<span data-ttu-id="370f4-118">[![Myyntitilausten keräilyreitin tila -kenttä](./media/picking-route-status-sales-order.png)](./media/picking-route-status-sales-order.png)</span><span class="sxs-lookup"><span data-stu-id="370f4-118">[![Picking route status field for sales orders](./media/picking-route-status-sales-order.png)](./media/picking-route-status-sales-order.png)</span></span>

<span data-ttu-id="370f4-119">Jos **Keräilyreitin tila** -kentän arvoksi on asetettu **Valmis**, keräilyprosessi toteutetaan automaattisesti keräysluettelon muodostamisprosessin osana.</span><span class="sxs-lookup"><span data-stu-id="370f4-119">If the **Picking route status** field is set to **Completed**, the picking process occurs automatically as part of the process of generating picking lists.</span></span> <span data-ttu-id="370f4-120">Jos kentän arvo on **Aktivoitu**, keräysluettelon rivit on päivitettävä manuaalisesti.</span><span class="sxs-lookup"><span data-stu-id="370f4-120">If the field is set to **Activated**, the picking list lines must be manually updated.</span></span>

<span data-ttu-id="370f4-121">Samat asetukset koskevat siirtotilauksia.</span><span class="sxs-lookup"><span data-stu-id="370f4-121">The same setup applies to transfer orders.</span></span> <span data-ttu-id="370f4-122">Siirry kohtaa **Varastonhallinta** \> **Asetukset** \> **Varasto ja varastonhallinnan parametrit**, ja valitse sitten **Kuljetus**-välilehden **Keräilyreitin tila** -kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="370f4-122">Go to **Inventory management** \> **Setup** \> **Inventory and warehouse management parameters**, and then, on the **Transport** tab, select a value in the **Picking route status** field.</span></span>

<span data-ttu-id="370f4-123">[![Siirtotilausten keräilyreitin tila -kenttä](./media/picking-route-status-transfer-order.png)](./media/picking-route-status-transfer-order.png)</span><span class="sxs-lookup"><span data-stu-id="370f4-123">[![Picking route status field for transfer orders](./media/picking-route-status-transfer-order.png)](./media/picking-route-status-transfer-order.png)</span></span>

## <a name="end-output-inventory-orders"></a><span data-ttu-id="370f4-124">Toimitustilausten lopettaminen</span><span class="sxs-lookup"><span data-stu-id="370f4-124">End output inventory orders</span></span>

<span data-ttu-id="370f4-125">Siirry kohtaan **Varastonhallinta** \> **Asetukset** \> **Varasto ja varastonhallinnan parametrit**, ja valitse sitten **Yleiset**-välilehden **Lopeta toimitustilaus**-vaihtoehto.</span><span class="sxs-lookup"><span data-stu-id="370f4-125">Go to **Inventory management** \> **Setup** \> **Inventory and warehouse management parameters**, and then, on the **General** tab, set the **End output inventory order** option.</span></span>

<span data-ttu-id="370f4-126">[![Lopeta toimitustilaus -vaihtoehto](./media//end-output-inventory-order.png)](./media//end-output-inventory-order.png)</span><span class="sxs-lookup"><span data-stu-id="370f4-126">[![End output inventory order option](./media//end-output-inventory-order.png)](./media//end-output-inventory-order.png)</span></span>

<span data-ttu-id="370f4-127">Kun varastotyöntekijä vähentää keräysluettelon määriä, vastaavat varastotilauksen määrät poistetaan lähetyksestä.</span><span class="sxs-lookup"><span data-stu-id="370f4-127">When the warehouse worker reduces the picking list quantities, then the corresponding inventory order quantities will be removed from the shipment.</span></span> <span data-ttu-id="370f4-128">Kun keräysluettelo päivitetään tiettynä ajankohtana, jäljellä olevat määrät raportoidaan takaisin tilaukseen, jos **Lopeta toimitustilaus** -asetukseksi on määritetty **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="370f4-128">When the picking list is updated at a point in time, the remaining quantities get reported back to the order if the **End output inventory order** option is set to **Yes**.</span></span> <span data-ttu-id="370f4-129">Jos **Lopeta toimitustilaus** -asetukseksi on määritetty **Ei**, jäljellä olevat määrät säilytetään avoimen toimitustilauksen määränä. Ne on lisättävä uuteen keräysluetteloon **Avoimet toimitustilaukset** -toiminnon osana.</span><span class="sxs-lookup"><span data-stu-id="370f4-129">If the **End output inventory order** option is set to **No**, the remaining quantities are kept as an open output order quantity and must be added to a new picking list as part of the **Open output orders** functionality.</span></span> 

<span data-ttu-id="370f4-130">[![Avoimet toimitustilaukset -komento Toiminnot-valikossa](./media/open-output-order.png)](./media/open-output-order.png)</span><span class="sxs-lookup"><span data-stu-id="370f4-130">[![Open output orders command on the Functions menu](./media/open-output-order.png)](./media/open-output-order.png)</span></span>

<span data-ttu-id="370f4-131">[![Toiminnot-valikko Avoimet toimitustilaukset -sivulla](./media/open-output-order-function.png)](./media/open-output-order-function.png)</span><span class="sxs-lookup"><span data-stu-id="370f4-131">[![Functions menu on the Open output orders page](./media/open-output-order-function.png)](./media/open-output-order-function.png)</span></span>

## <a name="reduce-quantity"></a><span data-ttu-id="370f4-132">Vähennä määrää</span><span class="sxs-lookup"><span data-stu-id="370f4-132">Reduce quantity</span></span>

<span data-ttu-id="370f4-133">Keräysluetteloiden muodostamisprosessissa voi käyttää myös kolmatta parametria, **Vähennä määrää**.</span><span class="sxs-lookup"><span data-stu-id="370f4-133">The third parameter that you can use as part of the process of generating picking lists is the **Reduce quantity** parameter.</span></span> <span data-ttu-id="370f4-134">Tämän parametrin asetus toimii yhdessä **Varaus**-asetuksen kanssa, joka käynnistää varausprosessin osana varastoon vapauttamista.</span><span class="sxs-lookup"><span data-stu-id="370f4-134">The setting of this parameter works together with the **Reservation** setting that triggers a reservation process as part of the release to the warehouse.</span></span>

<span data-ttu-id="370f4-135">[![Vähennä määrää -parametri](./media/reduce-quantity.png)](./media/reduce-quantity.png)</span><span class="sxs-lookup"><span data-stu-id="370f4-135">[![Reduce quantity parameter](./media/reduce-quantity.png)](./media/reduce-quantity.png)</span></span>

## <a name="example-of-an-outbound-process-for-a-sales-order"></a><span data-ttu-id="370f4-136">Esimerkki myyntitilauksen lähtevästä prosessista</span><span class="sxs-lookup"><span data-stu-id="370f4-136">Example of an outbound process for a sales order</span></span>

<span data-ttu-id="370f4-137">Tässä esimerkissä on kaksi nimikettä sisältävä myyntitilaus.</span><span class="sxs-lookup"><span data-stu-id="370f4-137">For this example, there is a sales order for two items.</span></span> <span data-ttu-id="370f4-138">Valitse keräysluettelon luonnin aikana **Vähennä määrää** -parametri.</span><span class="sxs-lookup"><span data-stu-id="370f4-138">During picking list generation, you select the **Reduce quantity** parameter.</span></span> <span data-ttu-id="370f4-139">Siksi keräysrivejä vapautetaan ja luodaan ainoastaan käytettävissä olevalle varastolle.</span><span class="sxs-lookup"><span data-stu-id="370f4-139">Therefore, you release and create picking lines only for available on-hand inventory.</span></span> <span data-ttu-id="370f4-140">Keräily on raportoitava keräysluetteloiden rekisteröintiprosessin kautta (**Keräilyreitin tila** = **Aktivoitu**).</span><span class="sxs-lookup"><span data-stu-id="370f4-140">The picking must be reported via a registration process for picking lists (**Picking route status** = **Activated**).</span></span>

<span data-ttu-id="370f4-141">Varasto, jota ei ole vielä varattu, varataan keräysluettelon luonnin aikana.</span><span class="sxs-lookup"><span data-stu-id="370f4-141">The inventory that hasn't already been reserved is reserved during picking list generation.</span></span> <span data-ttu-id="370f4-142">Ei käytettävissä olevan varaston voi joko poistaa myyntitilaukselta tai vapauttaa varastoon myöhempää käsittelyä varten, kun varasto on käytettävissä keräilyyn.</span><span class="sxs-lookup"><span data-stu-id="370f4-142">The unavailable inventory can be either removed from the sales order or released to the warehouse for outbound processing later, when inventory is available for picking.</span></span>

<span data-ttu-id="370f4-143">[![Päivitä keräysluettelo](./media/update-picking-list.png)](./media/update-picking-list.png)</span><span class="sxs-lookup"><span data-stu-id="370f4-143">[![Update the picking list](./media/update-picking-list.png)](./media/update-picking-list.png)</span></span>

<span data-ttu-id="370f4-144">Kun kaikki **Keräysluettelon kirjaaminen** -sivun keräilyrivit on kerätty, liittyvä lähetys on valmis.</span><span class="sxs-lookup"><span data-stu-id="370f4-144">As soon as all the picking lines have been picked on the **Picking list registration** page, the associated shipment is completed.</span></span> <span data-ttu-id="370f4-145">Myyntitilausten pakkausluetteloprosessi voidaan sitten alustaa keräillyn varaston perusteella.</span><span class="sxs-lookup"><span data-stu-id="370f4-145">The process for sales order packing slips can then be initialized based on the picked inventory.</span></span>

<span data-ttu-id="370f4-146">[![Lähtevien lähetysten päivittäminen](./media/outbound-shipments.png)](./media/outbound-shipments.png)</span><span class="sxs-lookup"><span data-stu-id="370f4-146">[![Update outbound shipments](./media/outbound-shipments.png)](./media/outbound-shipments.png)</span></span>

