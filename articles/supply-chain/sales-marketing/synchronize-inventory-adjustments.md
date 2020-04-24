---
title: Varastosiirtojen ja -oikaisujen synkronointi Field Servicesta Supply Chain Managementiin
description: Tässä ohjeaiheessa käsitellään malleja ja taustalla olevia tehtäviä, joilla Dynamics 365 Supply Chain Managementin varaston oikaisut ja siirrot synkronoidaan Dynamics 365 Field Serviceen.
author: ChristianRytt
manager: tfehr
ms.date: 04/30/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: 8.1.3
ms.search.validFrom: 2018-12-01
ms.openlocfilehash: ff64f28af570b792f73b51aa9caf06dd2445b2ca
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/02/2020
ms.locfileid: "3204421"
---
# <a name="synchronize-inventory-transfers-and-adjustments-from-field-service-to-supply-chain-management"></a><span data-ttu-id="c5078-103">Varastosiirtojen ja -oikaisujen synkronointi Field Servicesta Supply Chain Managementiin</span><span class="sxs-lookup"><span data-stu-id="c5078-103">Synchronize inventory transfers and adjustments from Field Service to Supply Chain Management</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="c5078-104">Tässä ohjeaiheessa käsitellään malleja ja taustalla olevia tehtäviä, joilla Dynamics 365 Supply Chain Managementin varaston oikaisut ja siirrot synkronoidaan Dynamics 365 Field Serviceen.</span><span class="sxs-lookup"><span data-stu-id="c5078-104">This topic discusses the templates and underlying tasks that are used to synchronize inventory adjustments and transfers from Dynamics 365 Supply Chain Management to Dynamics 365 Field Service.</span></span>

<span data-ttu-id="c5078-105">[![Liiketoimintaprosessien synkronointi Supply Chain Managementin ja Field Servicen välillä](./media/FSTransAdjOW.png)](./media/FSTransAdjOW.png)</span><span class="sxs-lookup"><span data-stu-id="c5078-105">[![Synchronization of business processes between Supply Chain Management and Field Service](./media/FSTransAdjOW.png)](./media/FSTransAdjOW.png)</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="c5078-106">Mallit ja tehtävät</span><span class="sxs-lookup"><span data-stu-id="c5078-106">Templates and tasks</span></span>
<span data-ttu-id="c5078-107">Seuraavaa mallia ja sen taustalla olevia tehtäviä käytetään synkronoitaessa varasto-oikaisuja ja -siirtoja Field Servicesta Supply Chain Managementiin.</span><span class="sxs-lookup"><span data-stu-id="c5078-107">The following template and underlying tasks are used to synchronize inventory adjustments and transfers from Field Service to Supply Chain Management.</span></span>

<span data-ttu-id="c5078-108">**Tietojen integroinnin mallit**</span><span class="sxs-lookup"><span data-stu-id="c5078-108">**Templates in Data integration**</span></span>
- <span data-ttu-id="c5078-109">Varasto-oikaisu (Field Servicesta Supply Chain Managementiin)</span><span class="sxs-lookup"><span data-stu-id="c5078-109">Inventory Adjustment (Field Service to Supply Chain Management)</span></span>
- <span data-ttu-id="c5078-110">Varastosiirrot (Field Servicesta Supply Chain Managementiin)</span><span class="sxs-lookup"><span data-stu-id="c5078-110">Inventory Transfers (Field Service to Supply Chain Management)</span></span>

<span data-ttu-id="c5078-111">**Tietojen integrointiprojektien tehtävät**</span><span class="sxs-lookup"><span data-stu-id="c5078-111">**Tasks in the Data integration projects**</span></span>
- <span data-ttu-id="c5078-112">Varasto-oikaisut</span><span class="sxs-lookup"><span data-stu-id="c5078-112">Inventory Adjustments</span></span>
- <span data-ttu-id="c5078-113">Varastosiirrot</span><span class="sxs-lookup"><span data-stu-id="c5078-113">Inventory Transfers</span></span>

## <a name="entity-set"></a><span data-ttu-id="c5078-114">Yksikköjoukko</span><span class="sxs-lookup"><span data-stu-id="c5078-114">Entity set</span></span>
| <span data-ttu-id="c5078-115">Field Service</span><span class="sxs-lookup"><span data-stu-id="c5078-115">Field Service</span></span>                     | <span data-ttu-id="c5078-116">Toimitusketjun hallinta</span><span class="sxs-lookup"><span data-stu-id="c5078-116">Supply Chain Management</span></span>                          |
|-----------------------------------|----------------------------------------------------|
| <span data-ttu-id="c5078-117">msdyn_inventoryadjustmentproducts</span><span class="sxs-lookup"><span data-stu-id="c5078-117">msdyn_inventoryadjustmentproducts</span></span> |   <span data-ttu-id="c5078-118">CDS-varasto-oikaisujen kirjauskansioiden otsikot ja rivit</span><span class="sxs-lookup"><span data-stu-id="c5078-118">CDS Inventory adjustment journal headers and lines</span></span> |
| <span data-ttu-id="c5078-119">msdyn_inventoryadjustmentproducts</span><span class="sxs-lookup"><span data-stu-id="c5078-119">msdyn_inventoryadjustmentproducts</span></span> | <span data-ttu-id="c5078-120">CDS-varastosiirtojen kirjauskansioiden otsikot ja rivit</span><span class="sxs-lookup"><span data-stu-id="c5078-120">CDS inventory transfer journal headers and lines</span></span>   |

## <a name="entity-flow"></a><span data-ttu-id="c5078-121">Yksikön työnkulku</span><span class="sxs-lookup"><span data-stu-id="c5078-121">Entity flow</span></span>
<span data-ttu-id="c5078-122">Field Servicessa tehdyt varasto-oikaisut ja -siirrot synkronoidaan Supply Chain Managementiin, kun **Kirjauksen tila** muuttuu **Kirjattu**-tilasta **Luotu**-tilaan.</span><span class="sxs-lookup"><span data-stu-id="c5078-122">Inventory adjustments and transfers made in Field Service will synchronize to Supply Chain Management after the **Post status** changes from **Created** to **Posted**.</span></span> <span data-ttu-id="c5078-123">Kun näin tapahtuu, oikaisu- tai siirtotilaus lukitaan vain luku -muotoisena.</span><span class="sxs-lookup"><span data-stu-id="c5078-123">When this occurs, the adjustment or the transfer order will be locked and become read only.</span></span> <span data-ttu-id="c5078-124">Tämän vuoksi Supply Chain Managementiin voidaan kirjata oikaisuja ja siirtoja, mutta niitä ei voi muokata.</span><span class="sxs-lookup"><span data-stu-id="c5078-124">This means that adjustments and transfers can be posted in Supply Chain Management, but cannot be modified.</span></span> <span data-ttu-id="c5078-125">Voit määrittää Supply Chain Managementissa erätyön, joka kirjaa automaattisesti integraation aikana luodut oikaisujen ja siirtojen varastokirjauskansiot.</span><span class="sxs-lookup"><span data-stu-id="c5078-125">In Supply Chain Management, you can set up a batch job to automatically post the adjustments and transfer inventory journals that have been generated during the integration.</span></span> <span data-ttu-id="c5078-126">Seuraavissa edellytyksissä on lisätietoja erätyön käyttöönottamisesta.</span><span class="sxs-lookup"><span data-stu-id="c5078-126">See the following prerequisites for details on how to enable the batch job.</span></span>

## <a name="field-service-crm-solution"></a><span data-ttu-id="c5078-127">Field Service CRM -ratkaisu</span><span class="sxs-lookup"><span data-stu-id="c5078-127">Field Service CRM solution</span></span> 
<span data-ttu-id="c5078-128">**Varastoyksikkö**-kenttä on lisätty **Tuote**-yksikköön.</span><span class="sxs-lookup"><span data-stu-id="c5078-128">The **Inventory unit** field has been added to the **Product** entity.</span></span> <span data-ttu-id="c5078-129">Tämä kenttä on välttämätön, sillä myynti- ja varastoyksikkö ei ole aina sama Supply Chain Managementissa, ja Supply Chain Managementin varaston varastoa varten tarvitaan varastoyksikkö.</span><span class="sxs-lookup"><span data-stu-id="c5078-129">This field is needed because the Sales and Inventory unit is not always the same in Supply Chain Management, and the Inventory Unit is needed for the Warehouse Inventory in Supply Chain Management.</span></span>
<span data-ttu-id="c5078-130">Kun tuote määritetään varasto-oikaisutuotteessa sekä varasto-oikaisuille että varastosiirroille, yksikkö noudetaan varastotuotteen arvosta.</span><span class="sxs-lookup"><span data-stu-id="c5078-130">When you set the product on an Inventory adjustment product for both Inventory adjustments and Inventory transfers, the unit will be fetched from the inventory product value.</span></span> <span data-ttu-id="c5078-131">Jos arvo löydetään, **Yksikkö**-kenttä lukitaan varasto-oikaisutuotteessa.</span><span class="sxs-lookup"><span data-stu-id="c5078-131">If a value is found, the **Unit** field will be locked on the Inventory adjustment product.</span></span>

<span data-ttu-id="c5078-132">**Kirjaa tila** -kenttä on lisätty sekä **Varasto-oikaisu**- että **Varastosiirto**-yksikköihin.</span><span class="sxs-lookup"><span data-stu-id="c5078-132">The **Post status** field has been added to both the **Inventory adjustment** entity and the **Inventory transfer** entity.</span></span> <span data-ttu-id="c5078-133">Tätä kenttää voi käyttää suodattimena, kun oikaisu tai siirto lähetetään Supply Chain Managementiin.</span><span class="sxs-lookup"><span data-stu-id="c5078-133">This field is used as a filter when an adjustment or transfer is sent to Supply Chain Management.</span></span> <span data-ttu-id="c5078-134">Tämän kentän oletusarvo on Luotu (1), mutta sitä ei kuitenkaan lähetetä Supply Chain Managementiin.</span><span class="sxs-lookup"><span data-stu-id="c5078-134">The default for this field is Created (1), however it is not sent to Supply Chain Management.</span></span> <span data-ttu-id="c5078-135">Kun arvoksi päivitetään Kirjattu (2), se lähetetään Supply Chain Managementiin, mutta tämän jälkeen oikaisua tai siirtoa ei voi kuitenkaan voi enää muuttaa eikä uusia rivejä lisätä.</span><span class="sxs-lookup"><span data-stu-id="c5078-135">When you update the value to Posted (2), it is sent to Supply Chain Management, but after that you will no longer be able to change the adjustment or transfer or add new lines.</span></span>

<span data-ttu-id="c5078-136">**Numerosarja**-kenttä on lisätty **Varasto-oikaisutuote**-yksikköön.</span><span class="sxs-lookup"><span data-stu-id="c5078-136">The **Number sequence** field has been added to the **Inventory adjustment product** entity.</span></span> <span data-ttu-id="c5078-137">Tämä kenttä varmistaa, että integraatiolla on yksilöivä numero, jotta integraatio voi luoda ja päivittää oikaisun.</span><span class="sxs-lookup"><span data-stu-id="c5078-137">This field ensures that the integration has a unique number, so the integration can create and update the adjustment.</span></span> <span data-ttu-id="c5078-138">Kun luot ensimmäisen varasto-oikaisutuotteen, se luo uuden tietueen **automaattisen P2C-numeroinnin** yksikön ylläpitämään numerosarjaa ja käytettyä etuliitettä.</span><span class="sxs-lookup"><span data-stu-id="c5078-138">When you create your first inventory adjustment product, it will create a new record in the **P2C AutoNumber** entity to maintain the number series and the prefix that is used.</span></span>

## <a name="prerequisites-and-mapping-setup"></a><span data-ttu-id="c5078-139">Edellytykset ja yhdistämismääritykset</span><span class="sxs-lookup"><span data-stu-id="c5078-139">Prerequisites and mapping setup</span></span>

### <a name="supply-chain-management"></a><span data-ttu-id="c5078-140">Toimitusketjun hallinta</span><span class="sxs-lookup"><span data-stu-id="c5078-140">Supply Chain Management</span></span>
<span data-ttu-id="c5078-141">Integraation luomat integroinnin varastokirjauskansiot voidaan kirjata automaattisesti erätyön avulla.</span><span class="sxs-lookup"><span data-stu-id="c5078-141">The integration inventory journals generated by the integration can automatically be posted using a batch job.</span></span> <span data-ttu-id="c5078-142">Se tehdään valitsemalla **Inventoinnin- ja varastonhallinta > Kausittaiset tehtävät > CDS-integrointi > Kirjaa integroinnin varastokirjauskansiot**.</span><span class="sxs-lookup"><span data-stu-id="c5078-142">This is enabled from **Inventory management > Periodic tasks > CDS integration > Post integration inventory journals**.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="c5078-143">Mallin yhdistäminen tietojen integroinnin yhteydessä</span><span class="sxs-lookup"><span data-stu-id="c5078-143">Template mapping in Data integration</span></span>

<span data-ttu-id="c5078-144">Seuraavissa kuvissa on esimerkki mallin yhdistämisestä tietojen integroinnin yhteydessä.</span><span class="sxs-lookup"><span data-stu-id="c5078-144">The following illustrations show the template mapping in Data integration.</span></span>

### <a name="inventory-adjustment-field-service-to-supply-chain-management-inventory-adjustment"></a><span data-ttu-id="c5078-145">Varasto-oikaisu (Field Servicesta Supply Chain Managementiin): Varasto-oikaisu</span><span class="sxs-lookup"><span data-stu-id="c5078-145">Inventory adjustment (Field Service to Supply Chain Management): Inventory adjustment</span></span>

<span data-ttu-id="c5078-146">[![Mallin yhdistäminen tietojen integroinnin yhteydessä](./media/FSAdj1.png)](./media/FSAdj1.png)</span><span class="sxs-lookup"><span data-stu-id="c5078-146">[![Template mapping in Data integration](./media/FSAdj1.png)](./media/FSAdj1.png)</span></span>


### <a name="inventory-transfer-field-service-to-supply-chain-management-inventory-transfer"></a><span data-ttu-id="c5078-147">Varastosiirto (Field Servicesta Supply Chain Managementiin): Varastosiirto</span><span class="sxs-lookup"><span data-stu-id="c5078-147">Inventory transfer (Field Service to Supply Chain Management): Inventory transfer</span></span>

<span data-ttu-id="c5078-148">[![Mallin yhdistäminen tietojen integroinnin yhteydessä](./media/FSTrans1.png)](./media/FSTrans1.png)</span><span class="sxs-lookup"><span data-stu-id="c5078-148">[![Template mapping in Data integration](./media/FSTrans1.png)](./media/FSTrans1.png)</span></span>
