---
title: Field Servicen varastosiirtojen ja oikaisujen synkronointi Finance and Operationsiin
description: Tässä ohjeaiheessa käsitellään malleja ja taustalla olevia tehtäviä, joilla Microsoft Dynamics 365 for Finance and Operationsin varaston oikaisut ja siirrot synkronoidaan Microsoft Dynamics 365 for Field Serviceen.
author: ChristianRytt
manager: AnnBe
ms.date: 04/30/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: 8.1.3
ms.search.validFrom: 2018-12-01
ms.openlocfilehash: 145c9c06635aa6518fd1f76324a8bd6e4cc07d16
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/01/2019
ms.locfileid: "1835715"
---
# <a name="synchronize-inventory-adjustments-from-field-service-to-finance-and-operations"></a><span data-ttu-id="f346e-103">Field Servicen varasto-oikaisujen synkronointi Finance and Operationsiin</span><span class="sxs-lookup"><span data-stu-id="f346e-103">Synchronize inventory adjustments from Field Service to Finance and Operations</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="f346e-104">Tässä ohjeaiheessa käsitellään malleja ja taustalla olevia tehtäviä, joilla Microsoft Dynamics 365 for Finance and Operationsin varaston oikaisut ja siirrot synkronoidaan Microsoft Dynamics 365 for Field Serviceen.</span><span class="sxs-lookup"><span data-stu-id="f346e-104">This topic discusses the templates and underlying tasks that are used to synchronize inventory adjustments and transfers from Microsoft Dynamics 365 for Finance and Operations to Microsoft Dynamics 365 for Field Service.</span></span>

<span data-ttu-id="f346e-105">[![Liiketoimintaprosessien synkronointi Finance and Operationsin ja Field Servicen välillä](./media/FSTransAdjOW.png)](./media/FSTransAdjOW.png)</span><span class="sxs-lookup"><span data-stu-id="f346e-105">[![Synchronization of business processes between Finance and Operations and Field Service](./media/FSTransAdjOW.png)](./media/FSTransAdjOW.png)</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="f346e-106">Mallit ja tehtävät</span><span class="sxs-lookup"><span data-stu-id="f346e-106">Templates and tasks</span></span>
<span data-ttu-id="f346e-107">Seuraavalla mallilla ja taustalla olevilla tehtävillä synkronoidaan Microsoft Dynamics 365 for Field Servicen varaston oikaisut ja siirrot Microsoft Dynamics 365 for Finance and Operationsiin.</span><span class="sxs-lookup"><span data-stu-id="f346e-107">The following template and underlying tasks are used to synchronize inventory adjustments and transfers from Microsoft Dynamics 365 for Field Service to Microsoft Dynamics 365 for Finance and Operations.</span></span>

<span data-ttu-id="f346e-108">**Tietojen integroinnin mallit**</span><span class="sxs-lookup"><span data-stu-id="f346e-108">**Templates in Data integration**</span></span>
- <span data-ttu-id="f346e-109">Varaston oikaisu (Field Servicestä Fin and Opsiin)</span><span class="sxs-lookup"><span data-stu-id="f346e-109">Inventory Adjustment (Field Service to Fin and Ops)</span></span>
- <span data-ttu-id="f346e-110">Varastonsiirrot (Field Servicestä Fin and Opsiin)</span><span class="sxs-lookup"><span data-stu-id="f346e-110">Inventory Transfers (Field Service to Fin and Ops)</span></span>

<span data-ttu-id="f346e-111">**Tietojen integrointiprojektien tehtävät**</span><span class="sxs-lookup"><span data-stu-id="f346e-111">**Tasks in the Data integration projects**</span></span>
- <span data-ttu-id="f346e-112">Varasto-oikaisut</span><span class="sxs-lookup"><span data-stu-id="f346e-112">Inventory Adjustments</span></span>
- <span data-ttu-id="f346e-113">Varastosiirrot</span><span class="sxs-lookup"><span data-stu-id="f346e-113">Inventory Transfers</span></span>

## <a name="entity-set"></a><span data-ttu-id="f346e-114">Yksikköjoukko</span><span class="sxs-lookup"><span data-stu-id="f346e-114">Entity set</span></span>
| <span data-ttu-id="f346e-115">Field Service</span><span class="sxs-lookup"><span data-stu-id="f346e-115">Field Service</span></span>                     | <span data-ttu-id="f346e-116">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="f346e-116">Finance and Operations</span></span>                             |
|-----------------------------------|----------------------------------------------------|
| <span data-ttu-id="f346e-117">msdyn_inventoryadjustmentproducts</span><span class="sxs-lookup"><span data-stu-id="f346e-117">msdyn_inventoryadjustmentproducts</span></span> |   <span data-ttu-id="f346e-118">CDS-varasto-oikaisujen kirjauskansioiden otsikot ja rivit</span><span class="sxs-lookup"><span data-stu-id="f346e-118">CDS Inventory adjustment journal headers and lines</span></span> |
| <span data-ttu-id="f346e-119">msdyn_inventoryadjustmentproducts</span><span class="sxs-lookup"><span data-stu-id="f346e-119">msdyn_inventoryadjustmentproducts</span></span> | <span data-ttu-id="f346e-120">CDS-varastosiirtojen kirjauskansioiden otsikot ja rivit</span><span class="sxs-lookup"><span data-stu-id="f346e-120">CDS inventory transfer journal headers and lines</span></span>   |

## <a name="entity-flow"></a><span data-ttu-id="f346e-121">Yksikön työnkulku</span><span class="sxs-lookup"><span data-stu-id="f346e-121">Entity flow</span></span>
<span data-ttu-id="f346e-122">Field Servicessä tehdyt varasto-oikaisut ja -siirrot synkronoidaan Finance and Operationsiin, kun **kirjauksen tilana** on **Kirjattu** eikä **Luotu**.</span><span class="sxs-lookup"><span data-stu-id="f346e-122">Inventory adjustments and transfers made in Field Service will synchronize to Finance and Operations after the **Post status** changes from **Created** to **Posted**.</span></span> <span data-ttu-id="f346e-123">Kun näin tapahtuu, oikaisu- tai siirtotilaus lukitaan vain luku -muotoisena.</span><span class="sxs-lookup"><span data-stu-id="f346e-123">When this occurs, the adjustment or the transfer order will be locked and become read only.</span></span> <span data-ttu-id="f346e-124">Tämän vuoksi Finance and Operationsiin voidaan kirjata oikaisuja ja siirtoja mutta niitä ei voi muokata.</span><span class="sxs-lookup"><span data-stu-id="f346e-124">This means that adjustments and transfers can be posted in Finance and Operations, but cannot be modified.</span></span> <span data-ttu-id="f346e-125">Voit määrittää Finance and Operationsissa erätyön, joka kirjaa automaattisesti integraation aikana luodut oikaisujen ja siirron varastokirjauskansiot.</span><span class="sxs-lookup"><span data-stu-id="f346e-125">In Finance and Operations, you can set up a batch job to automatically post the adjustments and transfer inventory journals that have been generated during the integration.</span></span> <span data-ttu-id="f346e-126">Seuraavissa edellytyksissä on lisätietoja erätyön käyttöönottamisesta.</span><span class="sxs-lookup"><span data-stu-id="f346e-126">See the following prerequisites for details on how to enable the batch job.</span></span>

## <a name="field-service-crm-solution"></a><span data-ttu-id="f346e-127">Field Service CRM -ratkaisu</span><span class="sxs-lookup"><span data-stu-id="f346e-127">Field Service CRM solution</span></span> 
<span data-ttu-id="f346e-128">**Varastoyksikkö**-kenttä on lisätty **Tuote**-yksikköön.</span><span class="sxs-lookup"><span data-stu-id="f346e-128">The **Inventory unit** field has been added to the **Product** entity.</span></span> <span data-ttu-id="f346e-129">Tämä kenttä on välttämätön, sillä myynti- ja varastoyksikkö ei ole aina sama Finance and Operationsissa ja Finance and Operationsin varaston varastoa varten tarvitaan varastoyksikkö.</span><span class="sxs-lookup"><span data-stu-id="f346e-129">This field is needed because the Sales and Inventory unit is not always the same in Finance and Operations, and the Inventory Unit is needed for the Warehouse Inventory in Finance and Operations.</span></span>
<span data-ttu-id="f346e-130">Kun tuote määritetään varasto-oikaisutuotteessa sekä varasto-oikaisuille että varastosiirroille, yksikkö noudetaan varastotuotteen arvosta.</span><span class="sxs-lookup"><span data-stu-id="f346e-130">When you set the product on an Inventory adjustment product for both Inventory adjustments and Inventory transfers, the unit will be fetched from the inventory product value.</span></span> <span data-ttu-id="f346e-131">Jos arvo löydetään, **Yksikkö**-kenttä lukitaan varasto-oikaisutuotteessa.</span><span class="sxs-lookup"><span data-stu-id="f346e-131">If a value is found, the **Unit** field will be locked on the Inventory adjustment product.</span></span>

<span data-ttu-id="f346e-132">**Kirjaa tila** -kenttä on lisätty sekä **Varasto-oikaisu**- että **Varastosiirto**-yksikköihin.</span><span class="sxs-lookup"><span data-stu-id="f346e-132">The **Post status** field has been added to both the **Inventory adjustment** entity and the **Inventory transfer** entity.</span></span> <span data-ttu-id="f346e-133">Tätä kenttää voi käyttää suodattimena, kun oikaisu tai siirto lähetetään Finance and Operationsiin.</span><span class="sxs-lookup"><span data-stu-id="f346e-133">This field is used as a filter when an adjustment or transfer is sent to Finance and Operations.</span></span> <span data-ttu-id="f346e-134">Tämän kentän oletusarvo on Luotu (1), mutta sitä ei kuitenkaan lähetetty Finance and Operationsiin.</span><span class="sxs-lookup"><span data-stu-id="f346e-134">The default for this field is Created (1), however it is not sent to Finance and Operations.</span></span> <span data-ttu-id="f346e-135">Kun arvoksi päivitetään Kirjattu (2), se lähetetään Finance and Operationsiin, mutta tämän jälkeen oikaisua tai siirtoa ei voi kuitenkaan voi enää muuttaa eikä uusia rivejä lisätä.</span><span class="sxs-lookup"><span data-stu-id="f346e-135">When you update the value to Posted (2), it is sent to Finance and Operations, but after that you will no longer be able to change the adjustment or transfer or add new lines.</span></span>

<span data-ttu-id="f346e-136">**Numerosarja**-kenttä on lisätty **Varasto-oikaisutuote**-yksikköön.</span><span class="sxs-lookup"><span data-stu-id="f346e-136">The **Number sequence** field has been added to the **Inventory adjustment product** entity.</span></span> <span data-ttu-id="f346e-137">Tämä kenttä varmistaa, että integraatiolla on yksilöivä numero, jotta integraatio voi luoda ja päivittää oikaisun.</span><span class="sxs-lookup"><span data-stu-id="f346e-137">This field ensures that the integration has a unique number, so the integration can create and update the adjustment.</span></span> <span data-ttu-id="f346e-138">Kun luot ensimmäisen varasto-oikaisutuotteen, se luo uuden tietueen **automaattisen P2C-numeroinnin** yksikön ylläpitämään numerosarjaa ja käytettyä etuliitettä.</span><span class="sxs-lookup"><span data-stu-id="f346e-138">When you create your first inventory adjustment product, it will create a new record in the **P2C AutoNumber** entity to maintain the number series and the prefix that is used.</span></span>

## <a name="prerequisites-and-mapping-setup"></a><span data-ttu-id="f346e-139">Edellytykset ja yhdistämismääritykset</span><span class="sxs-lookup"><span data-stu-id="f346e-139">Prerequisites and mapping setup</span></span>

### <a name="finance-and-operations"></a><span data-ttu-id="f346e-140">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="f346e-140">Finance and Operations</span></span>
<span data-ttu-id="f346e-141">Integraation luomat integroinnin varastokirjauskansiot voidaan kirjata automaattisesti erätyön avulla.</span><span class="sxs-lookup"><span data-stu-id="f346e-141">The integration inventory journals generated by the integration can automatically be posted using a batch job.</span></span> <span data-ttu-id="f346e-142">Se tehdään valitsemalla **Inventoinnin- ja varastonhallinta > Kausittaiset tehtävät > CDS-integrointi > Kirjaa integroinnin varastokirjauskansiot**.</span><span class="sxs-lookup"><span data-stu-id="f346e-142">This is enabled from **Inventory management > Periodic tasks > CDS integration > Post integration inventory journals**.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="f346e-143">Mallin yhdistäminen tietojen integroinnin yhteydessä</span><span class="sxs-lookup"><span data-stu-id="f346e-143">Template mapping in Data integration</span></span>

<span data-ttu-id="f346e-144">Seuraavissa kuvissa on esimerkki mallin yhdistämisestä tietojen integroinnin yhteydessä.</span><span class="sxs-lookup"><span data-stu-id="f346e-144">The following illustrations show the template mapping in Data integration.</span></span>

### <a name="inventory-adjustment-field-service-to-fin-and-ops-inventory-adjustment"></a><span data-ttu-id="f346e-145">Varasto-oikaisu (Field Servicestä Fin and Opsiin): varasto-oikaisu</span><span class="sxs-lookup"><span data-stu-id="f346e-145">Inventory adjustment (Field Service to Fin and Ops): Inventory adjustment</span></span>

<span data-ttu-id="f346e-146">[![Mallin yhdistäminen tietojen integroinnin yhteydessä](./media/FSAdj1.png)](./media/FSAdj1.png)</span><span class="sxs-lookup"><span data-stu-id="f346e-146">[![Template mapping in Data integration](./media/FSAdj1.png)](./media/FSAdj1.png)</span></span>


### <a name="inventory-transfer-field-service-to-fin-and-ops-inventory-transfer"></a><span data-ttu-id="f346e-147">Varastosiirto (Field Servicestä Fin and Opsiin): varastosiirto</span><span class="sxs-lookup"><span data-stu-id="f346e-147">Inventory transfer (Field Service to Fin and Ops): Inventory transfer</span></span>

<span data-ttu-id="f346e-148">[![Mallin yhdistäminen tietojen integroinnin yhteydessä](./media/FSTrans1.png)](./media/FSTrans1.png)</span><span class="sxs-lookup"><span data-stu-id="f346e-148">[![Template mapping in Data integration](./media/FSTrans1.png)](./media/FSTrans1.png)</span></span>
