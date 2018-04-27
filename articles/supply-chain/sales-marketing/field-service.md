---
title: Microsoft Dynamics 365 for Field Servicen integrointi
description: "Tässä ohjeaiheessa on yleiskatsaus Microsoft Dynamics 365 for Field Servicen integroinnista."
author: ChristianRytt
manager: AnnBe
ms.date: 04/10/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
audience: Application User, IT Pro
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: 
ms.author: crytt
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.translationtype: HT
ms.sourcegitcommit: d32a4e376770fc73c79b94924d5ae062d201d84a
ms.openlocfilehash: a224962152e80293f6cf3425dea74d73a283e31a
ms.contentlocale: fi-fi
ms.lasthandoff: 04/12/2018

---


# <a name="integration-with-microsoft-dynamics-365-for-field-service"></a><span data-ttu-id="40f1f-103">Microsoft Dynamics 365 for Field Servicen integrointi</span><span class="sxs-lookup"><span data-stu-id="40f1f-103">Integration with Microsoft Dynamics 365 for Field Service</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="40f1f-104">Microsoft Dynamics 365 for Finance and Operationsin avulla voi synkronoida liiketoimintaprosesseja Finance and Operationsin ja Microsoft Dynamics 365 for Field Servicen välillä.</span><span class="sxs-lookup"><span data-stu-id="40f1f-104">Microsoft Dynamics 365 for Finance and Operations enables synchronization of business processes between Finance and Operations and Microsoft Dynamics 365 for Field Service.</span></span> <span data-ttu-id="40f1f-105">Integrointiskenaariot määritetään käyttämällä laajennettavia tietojen integrointitoiminnon malleja ja Common Data Service (CDS) -palvelua. Niiden avulla liiketoimintaprosessien synkronointi voidaan ottaa käyttöön.</span><span class="sxs-lookup"><span data-stu-id="40f1f-105">The integration scenarios are configured by using extensible Data integrator templates and the Common Data Service (CDS) to enable the synchronization of business processes.</span></span>

<span data-ttu-id="40f1f-106">[![Liiketoimintaprosessien synkronointi Finance and Operationsin ja Field Servicen välillä](./media/field-service-integration.png)](./media/field-service-integration.png)</span><span class="sxs-lookup"><span data-stu-id="40f1f-106">[![Synchronization of business processes between Finance and Operations and Field Service](./media/field-service-integration.png)](./media/field-service-integration.png)</span></span>

<span data-ttu-id="40f1f-107">Field Servicen ja Finance and Operationsin välisen integroinnin ensimmäinen vaihe keskittyy siihen, että Field Servicen työtilauksia ja sopimuksia voidaan laskuttaa Finance and Operationsissa.</span><span class="sxs-lookup"><span data-stu-id="40f1f-107">The first phase  of the integration between Field Service and Finance and Operations is focused on enabling work orders and agreements in Field Service to be invoiced in Finance and Operations.</span></span> <span data-ttu-id="40f1f-108">Tuettu työnkulku käynnistyy Field Servicessä, jossa työtilausten tiedot synkronoidaan Finance and Operationsiin myyntitilauksina.</span><span class="sxs-lookup"><span data-stu-id="40f1f-108">The supported flow starts in Field Service, where information from work orders is synchronized to Finance and Operations as sales orders.</span></span> <span data-ttu-id="40f1f-109">Finance and Operationsissa luodaan laskuasiakirjoja laskuttamalla myyntitilaukset.</span><span class="sxs-lookup"><span data-stu-id="40f1f-109">In Finance and Operations, the sales orders are invoiced to generate invoice documents.</span></span> <span data-ttu-id="40f1f-110">Myös Field Servicen sopimuslaskujen tiedot synkronoidaan Finance and Operationsiin.</span><span class="sxs-lookup"><span data-stu-id="40f1f-110">In addition, the information from Field Service agreement invoices is synchronized to Finance and Operations.</span></span> <span data-ttu-id="40f1f-111">Microsoft Dynamics 365:n tietojen integrointitoiminto synkronoi tiedot käyttämällä mukautettavia projekteja.</span><span class="sxs-lookup"><span data-stu-id="40f1f-111">The Microsoft Dynamics 365 Data integrator synchronizes data by using customizable projects.</span></span> <span data-ttu-id="40f1f-112">Mukautettujen integrointiprojektien luontiin voidaan käyttää vakiomalleja. Näissä projekteissa lisävakiokenttiä ja mukautettuja kenttiä sekä yksiköitä yhdistämällä voidaan muokata integrointi tarpeita vastaavaksi.</span><span class="sxs-lookup"><span data-stu-id="40f1f-112">Standard templates can be used to create custom integration projects where additional standard and custom fields, and also entities, can be mapped to adjust the integration and meet specific requirements.</span></span>

<span data-ttu-id="40f1f-113">Field Servicen ja Finance and Operationsin ensimmäisen vaiheen integrointi mahdollistaa seuraavien nimikkeiden synkronoinnin:</span><span class="sxs-lookup"><span data-stu-id="40f1f-113">The first phase of the integration between Field Service and Finance and Operations enables synchronization of the following items:</span></span>

- [<span data-ttu-id="40f1f-114">Finance and Operationsin tuotteet Field Servicen tuotetyyppitietoja sisältäviin tuotteisiin</span><span class="sxs-lookup"><span data-stu-id="40f1f-114">Products in Finance and Operations to products in Field Service that include Product Type information</span></span>](field-service-product.md)
- [<span data-ttu-id="40f1f-115">Field Servicen työtilaukset Finance and Operationsin myyntitilauksiin</span><span class="sxs-lookup"><span data-stu-id="40f1f-115">Work orders in Field Service to sales orders in Finance and Operations</span></span>](field-service-work-order.md)
- [<span data-ttu-id="40f1f-116">Field Servicen laskut Finance and Operationsin vapaatekstilaskuihin</span><span class="sxs-lookup"><span data-stu-id="40f1f-116">Invoices in Field Service to free text invoices in Finance and Operations</span></span>](field-service-invoice.md)

## <a name="system-requirements-for-finance-and-operations"></a><span data-ttu-id="40f1f-117">Finance and Operations -sovelluksen järjestelmävaatimukset</span><span class="sxs-lookup"><span data-stu-id="40f1f-117">System requirements for Finance and Operations</span></span>
<span data-ttu-id="40f1f-118">Field Servicen integrointi tukee seuraavia versioita:</span><span class="sxs-lookup"><span data-stu-id="40f1f-118">Field Service integration supports the following versions:</span></span>

### <a name="dynamics-365-for-finance-and-operations-version-80-april-2018-or-later"></a><span data-ttu-id="40f1f-119">Dynamics 365 for Finance and Operations -versio 8.0 (huhtikuu 2018) tai uudempi</span><span class="sxs-lookup"><span data-stu-id="40f1f-119">Dynamics 365 for Finance and Operations version 8.0 (April 2018) or later</span></span>

- <span data-ttu-id="40f1f-120">Dynamics 365 for Finance and Operations versio 8.0 (huhtikuu 2018) julkaistiin huhtikuussa 2018; sen koontiversionumero on 8.0.30.8020 ja ympäristöpäivitys 15 (7.0.4841.35234).</span><span class="sxs-lookup"><span data-stu-id="40f1f-120">Dynamics 365 for Finance and Operations version 8.0 (April 2018) was released in April 2018 and has an application build number 8.0.30.8020 with Platform Update 15 (7.0.4841.35234).</span></span> 

## <a name="system-requirements-for-field-service"></a><span data-ttu-id="40f1f-121">Field Servicen järjestelmävaatimukset</span><span class="sxs-lookup"><span data-stu-id="40f1f-121">System requirements for Field Service</span></span>
<span data-ttu-id="40f1f-122">Seuraavat komponentit on asennettava, jotta Field Service -integrointiratkaisua voi käyttää:</span><span class="sxs-lookup"><span data-stu-id="40f1f-122">To use the Field Service integration solution, you must install the following components:</span></span>

### <a name="microsoft-dynamics-365-for-field-service-90-or-later"></a><span data-ttu-id="40f1f-123">Microsoft Dynamics 365 for Field Service 9.0 tai uudempi</span><span class="sxs-lookup"><span data-stu-id="40f1f-123">Microsoft Dynamics 365 for Field Service 9.0 or later</span></span>

- <span data-ttu-id="40f1f-124">Dynamics 365 for Field Servicen versio 1612 (9.0.1.733) (DB 9.0.1.733) online tai uudempi versio</span><span class="sxs-lookup"><span data-stu-id="40f1f-124">Dynamics 365 for Field Service version 1612 (9.0.1.733) (DB 9.0.1.733) online or a later version.</span></span>
- <span data-ttu-id="40f1f-125">Dynamics 365:N prospektista käteiseksi (P2C) -ratkaisu, versio 1.15.0.1 tai uudempi versio.</span><span class="sxs-lookup"><span data-stu-id="40f1f-125">Prospect to Cash (P2C) solution for Dynamics 365, version 1.15.0.1 or a later version.</span></span> <span data-ttu-id="40f1f-126">Ratkaisun voi ladata [AppSourcesta](https://appsource.microsoft.com/en-us/product/dynamics-365/mscrm.c7a48b40-eed3-4d67-93ba-f2364281feb3).</span><span class="sxs-lookup"><span data-stu-id="40f1f-126">The solution is available for download from [AppSource](https://appsource.microsoft.com/en-us/product/dynamics-365/mscrm.c7a48b40-eed3-4d67-93ba-f2364281feb3).</span></span>
- <span data-ttu-id="40f1f-127">Dynamics 365:n Field Service -integrointiratkaisu, versio 1.0.0.0 tai uudempi versio.</span><span class="sxs-lookup"><span data-stu-id="40f1f-127">Field Service integration solution for Dynamics 365, version 1.0.0.0 or a later version.</span></span> <span data-ttu-id="40f1f-128">Ratkaisun voi ladata AppSourcesta.</span><span class="sxs-lookup"><span data-stu-id="40f1f-128">The solution is available for download from AppSource.</span></span> <span data-ttu-id="40f1f-129">**(ODOTTAA JULKAISUA)**</span><span class="sxs-lookup"><span data-stu-id="40f1f-129">**(PENDING RELEASE)**</span></span>

