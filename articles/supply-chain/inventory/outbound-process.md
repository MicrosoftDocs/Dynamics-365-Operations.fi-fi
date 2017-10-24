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
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 274363
ms.assetid: 375807b2-a426-4f1b-bc1f-2fe00fd48413
ms.search.region: global
ms.search.industry: Distribution
ms.author: perlynne
ms.dyn365.ops.intro: AX 7.0.0
ms.search.validFrom: 2016-02-28
ms.translationtype: HT
ms.sourcegitcommit: 9c09a7bd314bb9005eb0b6c69d7cccad1c30cfdb
ms.openlocfilehash: 7b395cab2184f8f9f3f50a7a595c6ed782645323
ms.contentlocale: fi-fi
ms.lasthandoff: 10/04/2017

---

# <a name="outbound-process"></a><span data-ttu-id="ef7eb-103">Lähtevien käsittely</span><span class="sxs-lookup"><span data-stu-id="ef7eb-103">Outbound process</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="ef7eb-104">Tässä aiheessa on yleiskatsaus varastonhallinnan lähtevien tuotteiden prosessista.</span><span class="sxs-lookup"><span data-stu-id="ef7eb-104">This topic provides an overview of the outbound process in Inventory management.</span></span>

## <a name="output-orders"></a><span data-ttu-id="ef7eb-105">Toimitustilaukset</span><span class="sxs-lookup"><span data-stu-id="ef7eb-105">Output orders</span></span>

<span data-ttu-id="ef7eb-106">Myyntitilausrivit ja siirtotilausrivit linkitetään toimitustilausten avulla lähtevien keräystoimintoihin, jotka käyttävät keräysluetteloita.</span><span class="sxs-lookup"><span data-stu-id="ef7eb-106">Output orders are used to link sales order lines and transfer order lines with the outbound picking processes that use picking lists.</span></span>

<span data-ttu-id="ef7eb-107">Kun keräysluetteloita muodostettaan joko myynti- tai siirtotilauksista, toimitustilaukset ja toimitukset luodaan automaattisesti.</span><span class="sxs-lookup"><span data-stu-id="ef7eb-107">When picking lists are generated from either sales orders or transfer orders, output orders and shipments are automatically created.</span></span> <span data-ttu-id="ef7eb-108">Keräysluettelolla on yksi-yhteen-suhde toimitukseen.</span><span class="sxs-lookup"><span data-stu-id="ef7eb-108">A picking list has a one-to-one relationship with a shipment.</span></span> <span data-ttu-id="ef7eb-109">Siirtotilauksen lähetystä tai myyntitilauksen pakkausluetteloa voi käsitellä lähetyksestä.</span><span class="sxs-lookup"><span data-stu-id="ef7eb-109">The transfer order shipment or the sales order packing slip can be processed from the shipment.</span></span> 

<span data-ttu-id="ef7eb-110">Seuraavassa kaaviossa on yhteenveto toimitustilausten prosessista.</span><span class="sxs-lookup"><span data-stu-id="ef7eb-110">The following diagram shows an overview of the process for outbound orders.</span></span> 

<span data-ttu-id="ef7eb-111">[![Yhteenveto toimitustilausten prosessista.](./media/outbound-order.png)](./media/outbound-order.png)</span><span class="sxs-lookup"><span data-stu-id="ef7eb-111">[![Overview of the outbound order process](./media/outbound-order.png)](./media/outbound-order.png)</span></span>

<span data-ttu-id="ef7eb-112">Lähtevien sääntöjen avulla voit määrittää, miten ohjelma toteuttaa lähtevien käsittelyn.</span><span class="sxs-lookup"><span data-stu-id="ef7eb-112">You can set up outbound rules to define how the program should handle the outbound process.</span></span> <span data-ttu-id="ef7eb-113">Voit hallita lähetysprosessia näiden sääntöjen avulla.</span><span class="sxs-lookup"><span data-stu-id="ef7eb-113">You can use these rules to control the shipment process.</span></span> <span data-ttu-id="ef7eb-114">Näiden sääntöjen avulla voit hallita, mihin prosessin vaiheeseen lähetyksen voi siirtää.</span><span class="sxs-lookup"><span data-stu-id="ef7eb-114">In particular, you can use the rules to control which stage in the process a shipment can be sent during.</span></span> <span data-ttu-id="ef7eb-115">Seuraavat asetukset määrittävät, miten lähtevän tavaran prosessit käsitellään.</span><span class="sxs-lookup"><span data-stu-id="ef7eb-115">The following settings define how the outbound processes are handled.</span></span>

## <a name="picking-route-status-for-sales-and-transfer-orders"></a><span data-ttu-id="ef7eb-116">Myynti- ja siirtotilausten keräilyreitin tila</span><span class="sxs-lookup"><span data-stu-id="ef7eb-116">Picking route status for sales and transfer orders</span></span> 

<span data-ttu-id="ef7eb-117">Siirry kohtaan **Myyntireskontra** \> **Asetukset** \> **Myyntireskontran parametrit** ja valitse sitten **Päivitykset**-välilehdellä arvo **Keräilyreitin tila** -kenttään.</span><span class="sxs-lookup"><span data-stu-id="ef7eb-117">Go to **Account receivable** \> **Setup** \> **Account receivable parameters**, and then, on the **Updates** tab, select a value in the **Picking route status** field.</span></span>

<span data-ttu-id="ef7eb-118">[![Myyntitilausten keräilyreitin tila -kenttä](./media/picking-route-status-sales-order.png)](./media/picking-route-status-sales-order.png)</span><span class="sxs-lookup"><span data-stu-id="ef7eb-118">[![Picking route status field for sales orders](./media/picking-route-status-sales-order.png)](./media/picking-route-status-sales-order.png)</span></span>

<span data-ttu-id="ef7eb-119">Jos **Keräilyreitin tila** -kentän arvoksi on asetettu **Valmis**, keräilyprosessi toteutetaan automaattisesti keräysluettelon muodostamisprosessin osana.</span><span class="sxs-lookup"><span data-stu-id="ef7eb-119">If the **Picking route status** field is set to **Completed**, the picking process occurs automatically as part of the process of generating picking lists.</span></span> <span data-ttu-id="ef7eb-120">Jos kentän arvo on **Aktivoitu**, keräysluettelon rivit on päivitettävä manuaalisesti.</span><span class="sxs-lookup"><span data-stu-id="ef7eb-120">If the field is set to **Activated**, the picking list lines must be manually updated.</span></span>

<span data-ttu-id="ef7eb-121">Samat asetukset koskevat siirtotilauksia.</span><span class="sxs-lookup"><span data-stu-id="ef7eb-121">The same setup applies to transfer orders.</span></span> <span data-ttu-id="ef7eb-122">Siirry kohtaa **Varastonhallinta** \> **Asetukset** \> **Varasto ja varastonhallinnan parametrit**, ja valitse sitten **Kuljetus**-välilehden **Keräilyreitin tila** -kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="ef7eb-122">Go to **Inventory management** \> **Setup** \> **Inventory and warehouse management parameters**, and then, on the **Transport** tab, select a value in the **Picking route status** field.</span></span>

<span data-ttu-id="ef7eb-123">[![Siirtotilausten keräilyreitin tila -kenttä](./media/picking-route-status-transfer-order.png)](./media/picking-route-status-transfer-order.png)</span><span class="sxs-lookup"><span data-stu-id="ef7eb-123">[![Picking route status field for transfer orders](./media/picking-route-status-transfer-order.png)](./media/picking-route-status-transfer-order.png)</span></span>

## <a name="end-output-inventory-orders"></a><span data-ttu-id="ef7eb-124">Toimitustilausten lopettaminen</span><span class="sxs-lookup"><span data-stu-id="ef7eb-124">End output inventory orders</span></span>

<span data-ttu-id="ef7eb-125">Siirry kohtaan **Varastonhallinta** \> **Asetukset** \> **Varasto ja varastonhallinnan parametrit**, ja valitse sitten **Yleiset**-välilehden **Lopeta toimitustilaus**-vaihtoehto.</span><span class="sxs-lookup"><span data-stu-id="ef7eb-125">Go to **Inventory management** \> **Setup** \> **Inventory and warehouse management parameters**, and then, on the **General** tab, set the **End output inventory order** option.</span></span>

<span data-ttu-id="ef7eb-126">[![Lopeta toimitustilaus -vaihtoehto](./media//end-output-inventory-order.png)](./media//end-output-inventory-order.png)</span><span class="sxs-lookup"><span data-stu-id="ef7eb-126">[![End output inventory order option](./media//end-output-inventory-order.png)](./media//end-output-inventory-order.png)</span></span>

<span data-ttu-id="ef7eb-127">Joskus joitakin varastonimikkeitä ei voi keräillä keräysluetteloprosessissa.</span><span class="sxs-lookup"><span data-stu-id="ef7eb-127">Sometimes, some items in inventory can't be picked as part of the picking list process.</span></span> <span data-ttu-id="ef7eb-128">Näin voi tapahtua jos esimerkiksi varastotyöntekijä vähentää keräilyrivien määriä ja käsittelee sitten keräysluettelon.</span><span class="sxs-lookup"><span data-stu-id="ef7eb-128">For example, this situation might occur if a warehouse worker reduces the quantities on picking lines and processes the picking list.</span></span> <span data-ttu-id="ef7eb-129">Jos **Lopeta toimitustilaus** -asetukseksi on määritetty **Kyllä**, jäljelle jäävät, keräilemättömät määrät raportoidaan takaisin tilaustasolle.</span><span class="sxs-lookup"><span data-stu-id="ef7eb-129">If the **End output inventory order** option is set to **Yes**, the remaining unpicked quantities are reported back to the order level.</span></span> <span data-ttu-id="ef7eb-130">Jos tämä asetus on **Ei**, keräilemättömät määrät pidetään avoimena toimitustilauksen määränä.</span><span class="sxs-lookup"><span data-stu-id="ef7eb-130">If the option is set to **No**, the remaining unpicked quantities are kept as an open output order quantity.</span></span> <span data-ttu-id="ef7eb-131">Tässä tapauksessa määrät pysyvät vapautettuna varastossa, ja ne täytyy uuteen keräysluetteloon **Avoimet toimitustilaukset** -toiminnolla.</span><span class="sxs-lookup"><span data-stu-id="ef7eb-131">In this case, the quantities remain released to the warehouse and must be added to a new picking list as part of the **Open output orders** functionality.</span></span>

<span data-ttu-id="ef7eb-132">[![Avoimet toimitustilaukset -komento Toiminnot-valikossa](./media/open-output-order.png)](./media/open-output-order.png)</span><span class="sxs-lookup"><span data-stu-id="ef7eb-132">[![Open output orders command on the Functions menu](./media/open-output-order.png)](./media/open-output-order.png)</span></span>

<span data-ttu-id="ef7eb-133">[![Toiminnot-valikko Avoimet toimitustilaukset -sivulla](./media/open-output-order-function.png)](./media/open-output-order-function.png)</span><span class="sxs-lookup"><span data-stu-id="ef7eb-133">[![Functions menu on the Open output orders page](./media/open-output-order-function.png)](./media/open-output-order-function.png)</span></span>

## <a name="reduce-quantity"></a><span data-ttu-id="ef7eb-134">Vähennä määrää</span><span class="sxs-lookup"><span data-stu-id="ef7eb-134">Reduce quantity</span></span>

<span data-ttu-id="ef7eb-135">Keräysluetteloiden muodostamisprosessissa voi käyttää myös kolmatta parametria, **Vähennä määrää**.</span><span class="sxs-lookup"><span data-stu-id="ef7eb-135">The third parameter that you can use as part of the process of generating picking lists is the **Reduce quantity** parameter.</span></span> <span data-ttu-id="ef7eb-136">Tämän parametrin asetus toimii yhdessä **Varaus**-asetuksen kanssa, joka käynnistää varausprosessin osana varastoon vapauttamista.</span><span class="sxs-lookup"><span data-stu-id="ef7eb-136">The setting of this parameter works together with the **Reservation** setting that triggers a reservation process as part of the release to the warehouse.</span></span>

<span data-ttu-id="ef7eb-137">[![Vähennä määrää -parametri](./media/reduce-quantity.png)](./media/reduce-quantity.png)</span><span class="sxs-lookup"><span data-stu-id="ef7eb-137">[![Reduce quantity parameter](./media/reduce-quantity.png)](./media/reduce-quantity.png)</span></span>

## <a name="example-of-an-outbound-process-for-a-sales-order"></a><span data-ttu-id="ef7eb-138">Esimerkki myyntitilauksen lähtevästä prosessista</span><span class="sxs-lookup"><span data-stu-id="ef7eb-138">Example of an outbound process for a sales order</span></span>

<span data-ttu-id="ef7eb-139">Tässä esimerkissä on kaksi nimikettä sisältävä myyntitilaus.</span><span class="sxs-lookup"><span data-stu-id="ef7eb-139">For this example, there is a sales order for two items.</span></span> <span data-ttu-id="ef7eb-140">Valitse keräysluettelon luonnin aikana **Vähennä määrää** -parametri.</span><span class="sxs-lookup"><span data-stu-id="ef7eb-140">During picking list generation, you select the **Reduce quantity** parameter.</span></span> <span data-ttu-id="ef7eb-141">Siksi keräysrivejä vapautetaan ja luodaan ainoastaan käytettävissä olevalle varastolle.</span><span class="sxs-lookup"><span data-stu-id="ef7eb-141">Therefore, you release and create picking lines only for available on-hand inventory.</span></span> <span data-ttu-id="ef7eb-142">Keräily on raportoitava keräysluetteloiden rekisteröintiprosessin kautta (**Keräilyreitin tila** = **Aktivoitu**).</span><span class="sxs-lookup"><span data-stu-id="ef7eb-142">The picking must be reported via a registration process for picking lists (**Picking route status** = **Activated**).</span></span>

<span data-ttu-id="ef7eb-143">Varasto, jota ei ole vielä varattu, varataan keräysluettelon luonnin aikana.</span><span class="sxs-lookup"><span data-stu-id="ef7eb-143">The inventory that hasn't already been reserved is reserved during picking list generation.</span></span> <span data-ttu-id="ef7eb-144">Ei käytettävissä olevan varaston voi joko poistaa myyntitilaukselta tai vapauttaa varastoon myöhempää käsittelyä varten, kun varasto on käytettävissä keräilyyn.</span><span class="sxs-lookup"><span data-stu-id="ef7eb-144">The unavailable inventory can be either removed from the sales order or released to the warehouse for outbound processing later, when inventory is available for picking.</span></span>

<span data-ttu-id="ef7eb-145">[![Päivitä keräysluettelo](./media/update-picking-list.png)](./media/update-picking-list.png)</span><span class="sxs-lookup"><span data-stu-id="ef7eb-145">[![Update the picking list](./media/update-picking-list.png)](./media/update-picking-list.png)</span></span>

<span data-ttu-id="ef7eb-146">Kun kaikki **Keräysluettelon kirjaaminen** -sivun keräilyrivit on kerätty, liittyvä lähetys on valmis.</span><span class="sxs-lookup"><span data-stu-id="ef7eb-146">As soon as all the picking lines have been picked on the **Picking list registration** page, the associated shipment is completed.</span></span> <span data-ttu-id="ef7eb-147">Myyntitilausten pakkausluetteloprosessi voidaan sitten alustaa keräillyn varaston perusteella.</span><span class="sxs-lookup"><span data-stu-id="ef7eb-147">The process for sales order packing slips can then be initialized based on the picked inventory.</span></span>

<span data-ttu-id="ef7eb-148">[![Lähtevien lähetysten päivittäminen](./media/outbound-shipments.png)](./media/outbound-shipments.png)</span><span class="sxs-lookup"><span data-stu-id="ef7eb-148">[![Update outbound shipments](./media/outbound-shipments.png)](./media/outbound-shipments.png)</span></span>

