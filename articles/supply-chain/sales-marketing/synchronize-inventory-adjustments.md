---
title: Field Servicen varastosiirtojen ja oikaisujen synkronointi Finance and Operationsiin
description: "Tässä ohjeaiheessa käsitellään malleja ja taustalla olevia tehtäviä, joilla Microsoft Dynamics 365 for Finance and Operationsin varaston oikaisut ja siirrot synkronoidaan Microsoft Dynamics 365 for Field Serviceen."
author: ChristianRytt
manager: AnnBe
ms.date: 12/20/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
audience: Application User, IT Pro
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: 
ms.author: crytt
ms.dyn365.ops.version: 8.1.3
ms.search.validFrom: 2018-12-01
ms.translationtype: HT
ms.sourcegitcommit: 8c6cb481f1a3fe48d329c5936118d8df88a4175b
ms.openlocfilehash: 79a1cfac3fa94223cc9af73e758ce95fd47065c9
ms.contentlocale: fi-fi
ms.lasthandoff: 12/20/2018

---

# <a name="synchronize-inventory-adjustments-from-field-service-to-finance-and-operations"></a><span data-ttu-id="2acee-103">Field Servicen varasto-oikaisujen synkronointi Finance and Operationsiin</span><span class="sxs-lookup"><span data-stu-id="2acee-103">Synchronize inventory adjustments from Field Service to Finance and Operations</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="2acee-104">Tässä ohjeaiheessa käsitellään malleja ja taustalla olevia tehtäviä, joilla Microsoft Dynamics 365 for Finance and Operationsin varaston oikaisut ja siirrot synkronoidaan Microsoft Dynamics 365 for Field Serviceen.</span><span class="sxs-lookup"><span data-stu-id="2acee-104">This topic discusses the templates and underlying tasks that are used to synchronize inventory adjustments and transfers from Microsoft Dynamics 365 for Finance and Operations to Microsoft Dynamics 365 for Field Service.</span></span>

<span data-ttu-id="2acee-105">[![Liiketoimintaprosessien synkronointi Finance and Operationsin ja Field Servicen välillä](./media/FSTransAdjOW.png)](./media/FSTransAdjOW.png)</span><span class="sxs-lookup"><span data-stu-id="2acee-105">[![Synchronization of business processes between Finance and Operations and Field Service](./media/FSTransAdjOW.png)](./media/FSTransAdjOW.png)</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="2acee-106">Mallit ja tehtävät</span><span class="sxs-lookup"><span data-stu-id="2acee-106">Templates and tasks</span></span>
<span data-ttu-id="2acee-107">Seuraavalla mallilla ja taustalla olevilla tehtävillä synkronoidaan Microsoft Dynamics 365 for Field Servicen varaston oikaisut ja siirrot synkronoidaan Microsoft Dynamics 365 for Finance and Operationsiin.</span><span class="sxs-lookup"><span data-stu-id="2acee-107">The following template and underlying tasks are used to run synchronization of inventory adjustments and transfers from Microsoft Dynamics 365 for Field Service to Microsoft Dynamics 365 for Finance and Operations.</span></span>

<span data-ttu-id="2acee-108">**Mallien nimet tietojen integroinnissa:**</span><span class="sxs-lookup"><span data-stu-id="2acee-108">**Name of the templates in Data integration:**</span></span>
- <span data-ttu-id="2acee-109">Varasto-oikaisu (Field Servicestä Finance and Operationsiin)</span><span class="sxs-lookup"><span data-stu-id="2acee-109">Inventory Adjustment (Field Service to Finance and Operations)</span></span>
- <span data-ttu-id="2acee-110">Varastosiirrot (Field Servicestä Finance and Operationsiin)</span><span class="sxs-lookup"><span data-stu-id="2acee-110">Inventory Transfers (Field Service to Finance and Operations)</span></span>

<span data-ttu-id="2acee-111">**Tehtävien nimet tietojen integrointiprojekteissa:**</span><span class="sxs-lookup"><span data-stu-id="2acee-111">**Names of the tasks in the Data integration projects:**</span></span>
- <span data-ttu-id="2acee-112">Varasto-oikaisut</span><span class="sxs-lookup"><span data-stu-id="2acee-112">Inventory Adjustments</span></span>
- <span data-ttu-id="2acee-113">Varastosiirrot</span><span class="sxs-lookup"><span data-stu-id="2acee-113">Inventory Transfers</span></span>

## <a name="entity-set"></a><span data-ttu-id="2acee-114">Yksikköjoukko</span><span class="sxs-lookup"><span data-stu-id="2acee-114">Entity set</span></span>
| <span data-ttu-id="2acee-115">Field Service</span><span class="sxs-lookup"><span data-stu-id="2acee-115">Field Service</span></span>                     | <span data-ttu-id="2acee-116">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="2acee-116">Finance and Operations</span></span>                             |
|-----------------------------------|----------------------------------------------------|
| <span data-ttu-id="2acee-117">msdyn_inventoryadjustmentproducts</span><span class="sxs-lookup"><span data-stu-id="2acee-117">msdyn_inventoryadjustmentproducts</span></span> |   <span data-ttu-id="2acee-118">CDS-varasto-oikaisujen kirjauskansioiden otsikot ja rivit</span><span class="sxs-lookup"><span data-stu-id="2acee-118">CDS Inventory adjustment journal headers and lines</span></span> |
| <span data-ttu-id="2acee-119">msdyn_inventoryadjustmentproducts</span><span class="sxs-lookup"><span data-stu-id="2acee-119">msdyn_inventoryadjustmentproducts</span></span> | <span data-ttu-id="2acee-120">CDS-varastosiirtojen kirjauskansioiden otsikot ja rivit</span><span class="sxs-lookup"><span data-stu-id="2acee-120">CDS inventory transfer journal headers and lines</span></span>   |

## <a name="entity-flow"></a><span data-ttu-id="2acee-121">Yksikön työnkulku</span><span class="sxs-lookup"><span data-stu-id="2acee-121">Entity flow</span></span>
<span data-ttu-id="2acee-122">Field Servicessä tehdyt varasto-oikaisut ja -siirrot synkronoidaan Finance and Operationsiin, kun **kirjauksen tilana** Kirjattu eikä Luotu.</span><span class="sxs-lookup"><span data-stu-id="2acee-122">Inventory adjustments and transfers made in Field Service will synchronize to Finance and Operations, once the **Post status** is changed from Created to Posted.</span></span> <span data-ttu-id="2acee-123">Kun näin tapahtuu, oikaisu- tai siirtotilaus lukitaan vain luku -muotoisena, sillä Finance and Operationsiin voidaan kirjata oikaisuja ja siirtoja eikä sitä voi sen vuoksi muokata.</span><span class="sxs-lookup"><span data-stu-id="2acee-123">When this happen the adjustment or transfer order will be locked and become read-only, as adjustments and transfers might be posted in Finance and Operations and therefor can't be modified.</span></span>
<span data-ttu-id="2acee-124">Voit määrittää Finance and Operationsissa erätyön, joka kirjaa automaattisesti integraatiolla luodut oikaisujen ja siirron varastokirjauskansiot.</span><span class="sxs-lookup"><span data-stu-id="2acee-124">In Finance and Operations you can setup a batch job to automatically post the adjustments and transfer inventory journals generated with the integration.</span></span> <span data-ttu-id="2acee-125">Alla olevissa edellytyksissä on lisätietoja erätyön käyttöönottamisesta.</span><span class="sxs-lookup"><span data-stu-id="2acee-125">See prerequisite below for details on how to enable the batch job.</span></span>

## <a name="field-service-crm-solution"></a><span data-ttu-id="2acee-126">Field Service CRM -ratkaisu</span><span class="sxs-lookup"><span data-stu-id="2acee-126">Field Service CRM solution</span></span> 
<span data-ttu-id="2acee-127">Varastoyksikkö-kenttä on lisätty tuoteyksikköön.</span><span class="sxs-lookup"><span data-stu-id="2acee-127">The Inventory Unit field has been added to the Product entity.</span></span> <span data-ttu-id="2acee-128">Tämä kenttä on välttämätön, sillä myynti- ja varastoyksikkö ei ole aina sama Operationsissa, Operationsin varaston varastoa varten tarvitaan varastoyksikkö.</span><span class="sxs-lookup"><span data-stu-id="2acee-128">This field is needed since the Sales and Inventory Unit is not always the same in Operations, and for the Warehouse Inventory in operations we need the Inventory Unit.</span></span>
<span data-ttu-id="2acee-129">Kun tuote määritetään varasto-oikaisutuotteessa sekä varasto-oikaisuille että varastosiirroille, yksikkö noudetaan tuotteiden varastotuotteen arvosta.</span><span class="sxs-lookup"><span data-stu-id="2acee-129">When you set the Product on an Inventory Adjustment Product for both Inventory Adjustments and Inventory Transfers the Unit will be fetched from the Products Inventory Product value.</span></span> <span data-ttu-id="2acee-130">Jos arvo löydetään, Yksikkö-kenttä lukitaan varasto-oikaisutuotteessa.</span><span class="sxs-lookup"><span data-stu-id="2acee-130">If a value is found the Unit field will be locked on the Inventory Adjustment Product</span></span>

<span data-ttu-id="2acee-131">Kirjaa tila -kenttä on lisätty sekä Varasto-oikaisu- että Varastosiirto-yksikköihin.</span><span class="sxs-lookup"><span data-stu-id="2acee-131">The Post Status field has been added to both the Inventory Adjustment entity and the Inventory Transfer entity.</span></span> <span data-ttu-id="2acee-132">Tätä kenttää voi käyttää suodattimena, kun oikaisu tai siirto lähetetään Operationsiin.</span><span class="sxs-lookup"><span data-stu-id="2acee-132">This field is used as a filter for when a adjustment or transfer is sent to Operations.</span></span> <span data-ttu-id="2acee-133">Kentän oletusarvona on Luotu (1), jolloin sitä ei lähetetä Operationsiin.</span><span class="sxs-lookup"><span data-stu-id="2acee-133">The field is defaulted to Created (1) and its then not sent over to Operations.</span></span> <span data-ttu-id="2acee-134">Kentät, joiden arvoksi on vaihdettu Kirjattu (2), lähetetään Operationsiin. Tämän jälkeen mitään ei kuitenkaan voi enää muuttaa Oikaisu- tai Siirto-kohdassa eikä siihen voi lisätä uusia rivejä.</span><span class="sxs-lookup"><span data-stu-id="2acee-134">Ones you change is to Posted (2) It is sent over to operations, but you will then no longer be able to change anything in the Adjustment or Transfer or add any new lines to it.</span></span>
<span data-ttu-id="2acee-135">Numerosarja-kenttä on lisätty varasto-oikaisutuotteen yksikköön.</span><span class="sxs-lookup"><span data-stu-id="2acee-135">The Number Sequence field has been added to the Inventory Adjustment Product entity.</span></span> <span data-ttu-id="2acee-136">Tämän kentän avulla integraatio saa yksilöivän numeron, joten integraatio tietää, milloin tehdään luonteja ja milloin päivityksiä.</span><span class="sxs-lookup"><span data-stu-id="2acee-136">This field helps the integration to have a Unique number, so the integration knows when to do creates and when to do updates.</span></span> <span data-ttu-id="2acee-137">Kun luot ensimmäisen varasto-oikaisutuotteen, se luo uuden tietueen automaattisen P2C-numeroinnin yksikön ylläpitämään numerosarjaa ja käytettyä etuliitettä.</span><span class="sxs-lookup"><span data-stu-id="2acee-137">When you create your first Inventory Adjustment Product it will create a new record in the P2C AutoNumber entity to maintain the number series and the prefix that is used.</span></span>

## <a name="prerequisites-and-mapping-setup"></a><span data-ttu-id="2acee-138">Edellytykset ja yhdistämismääritykset</span><span class="sxs-lookup"><span data-stu-id="2acee-138">Prerequisites and mapping setup</span></span>

### <a name="in-finance-and-operations"></a><span data-ttu-id="2acee-139">Finance and Operationsissa</span><span class="sxs-lookup"><span data-stu-id="2acee-139">In Finance and Operations</span></span>
<span data-ttu-id="2acee-140">Integraation luomat integroinnin varastokirjauskansiot voidaan kirjata automaattisesti erätyön avulla.</span><span class="sxs-lookup"><span data-stu-id="2acee-140">The integration inventory journals generated by the integration can automatically be posted with a batch job.</span></span> <span data-ttu-id="2acee-141">Se tehdään valitsemalla: Inventoinnin- ja varastonhallinta > Kausittaiset tehtävät > CDS-integrointi > Kirjaa integroinnin varastokirjauskansiot</span><span class="sxs-lookup"><span data-stu-id="2acee-141">This is enabled from: Inventory management > Periodic tasks > CDS integration > Post integration inventory journals</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="2acee-142">Mallin yhdistäminen tietojen integroinnin yhteydessä</span><span class="sxs-lookup"><span data-stu-id="2acee-142">Template mapping in Data integration</span></span>

<span data-ttu-id="2acee-143">Seuraavissa kuvissa on esimerkki mallin yhdistämisestä tietojen integroinnin yhteydessä.</span><span class="sxs-lookup"><span data-stu-id="2acee-143">The following illustrations show the template mapping in Data integration.</span></span>

### <a name="inventory-adjustment-field-service-to-finance-and-operations-inventory-adjustment"></a><span data-ttu-id="2acee-144">Varasto-oikaisu (Field Servicestä Finance and Operationsiin): varasto-oikaisu</span><span class="sxs-lookup"><span data-stu-id="2acee-144">Inventory Adjustment (Field Service to Finance and Operations): Inventory Adjustment</span></span>

<span data-ttu-id="2acee-145">[![Mallin yhdistäminen tietojen integroinnin yhteydessä](./media/FSAdj1.png)](./media/FSAdj1.png)</span><span class="sxs-lookup"><span data-stu-id="2acee-145">[![Template mapping in Data integration](./media/FSAdj1.png)](./media/FSAdj1.png)</span></span>


### <a name="inventory-transfer-field-service-to-finance-and-operations-inventory-transfer"></a><span data-ttu-id="2acee-146">Varastosiirto (Field Servicestä Finance and Operationsiin): varastosiirto</span><span class="sxs-lookup"><span data-stu-id="2acee-146">Inventory Transfer (Field Service to Finance and Operations): Inventory Transfer</span></span>

<span data-ttu-id="2acee-147">[![Mallin yhdistäminen tietojen integroinnin yhteydessä](./media/FSTrans1.png)](./media/FSTrans1.png)</span><span class="sxs-lookup"><span data-stu-id="2acee-147">[![Template mapping in Data integration](./media/FSTrans1.png)](./media/FSTrans1.png)</span></span>

