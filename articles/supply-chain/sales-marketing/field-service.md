---
title: Microsoft Dynamics 365 for Field Servicen integrointi
description: "Tässä ohjeaiheessa on yleiskatsaus Microsoft Dynamics 365 for Field Servicen integroinnista."
author: ChristianRytt
manager: AnnBe
ms.date: 04/25/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
audience: Application User, IT Pro
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: 
ms.author: crytt
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.translationtype: HT
ms.sourcegitcommit: d9747ba144d56c9410846769e5465372c89ea111
ms.openlocfilehash: 2ef7f71dc6d58108b498ed89e9175ff2ce900cda
ms.contentlocale: fi-fi
ms.lasthandoff: 08/07/2018

---


# <a name="integration-with-microsoft-dynamics-365-for-field-service"></a><span data-ttu-id="8c2a0-103">Microsoft Dynamics 365 for Field Servicen integrointi</span><span class="sxs-lookup"><span data-stu-id="8c2a0-103">Integration with Microsoft Dynamics 365 for Field Service</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="8c2a0-104">Microsoft Dynamics 365 for Finance and Operationsin avulla voi synkronoida liiketoimintaprosesseja Finance and Operationsin ja Microsoft Dynamics 365 for Field Servicen välillä.</span><span class="sxs-lookup"><span data-stu-id="8c2a0-104">Microsoft Dynamics 365 for Finance and Operations enables synchronization of business processes between Finance and Operations and Microsoft Dynamics 365 for Field Service.</span></span> <span data-ttu-id="8c2a0-105">Integrointiskenaariot määritetään käyttämällä laajennettavia tietojen integrointitoiminnon malleja ja Common Data Service (CDS) -palvelua. Niiden avulla liiketoimintaprosessien synkronointi voidaan ottaa käyttöön.</span><span class="sxs-lookup"><span data-stu-id="8c2a0-105">The integration scenarios are configured by using extensible Data integrator templates and the Common Data Service (CDS) to enable the synchronization of business processes.</span></span>

<span data-ttu-id="8c2a0-106">[![Liiketoimintaprosessien synkronointi Finance and Operationsin ja Field Servicen välillä](./media/field-service-integration.png)](./media/field-service-integration.png)</span><span class="sxs-lookup"><span data-stu-id="8c2a0-106">[![Synchronization of business processes between Finance and Operations and Field Service](./media/field-service-integration.png)](./media/field-service-integration.png)</span></span>

<span data-ttu-id="8c2a0-107">Field Servicen ja Finance and Operationsin välisen integroinnin ensimmäinen vaihe keskittyy siihen, että Field Servicen työtilauksia ja sopimuksia voidaan laskuttaa Finance and Operationsissa.</span><span class="sxs-lookup"><span data-stu-id="8c2a0-107">The first phase  of the integration between Field Service and Finance and Operations is focused on enabling work orders and agreements in Field Service to be invoiced in Finance and Operations.</span></span> <span data-ttu-id="8c2a0-108">Tuettu työnkulku käynnistyy Field Servicessä, jossa työtilausten tiedot synkronoidaan Finance and Operationsiin myyntitilauksina.</span><span class="sxs-lookup"><span data-stu-id="8c2a0-108">The supported flow starts in Field Service, where information from work orders is synchronized to Finance and Operations as sales orders.</span></span> <span data-ttu-id="8c2a0-109">Finance and Operationsissa luodaan laskuasiakirjoja laskuttamalla myyntitilaukset.</span><span class="sxs-lookup"><span data-stu-id="8c2a0-109">In Finance and Operations, the sales orders are invoiced to generate invoice documents.</span></span> <span data-ttu-id="8c2a0-110">Myös Field Servicen sopimuslaskujen tiedot synkronoidaan Finance and Operationsiin.</span><span class="sxs-lookup"><span data-stu-id="8c2a0-110">In addition, the information from Field Service agreement invoices is synchronized to Finance and Operations.</span></span> <span data-ttu-id="8c2a0-111">Microsoft Dynamics 365:n tietojen integrointitoiminto synkronoi tiedot käyttämällä mukautettavia projekteja.</span><span class="sxs-lookup"><span data-stu-id="8c2a0-111">The Microsoft Dynamics 365 Data integrator synchronizes data by using customizable projects.</span></span> <span data-ttu-id="8c2a0-112">Mukautettujen integrointiprojektien luontiin voidaan käyttää vakiomalleja. Näissä projekteissa lisävakiokenttiä ja mukautettuja kenttiä sekä yksiköitä yhdistämällä voidaan muokata integrointi tarpeita vastaavaksi.</span><span class="sxs-lookup"><span data-stu-id="8c2a0-112">Standard templates can be used to create custom integration projects where additional standard and custom fields, and also entities, can be mapped to adjust the integration and meet specific requirements.</span></span>

<span data-ttu-id="8c2a0-113">Field Servicen ja Finance and Operationsin ensimmäisen vaiheen integrointi mahdollistaa seuraavien nimikkeiden synkronoinnin:</span><span class="sxs-lookup"><span data-stu-id="8c2a0-113">The first phase of the integration between Field Service and Finance and Operations enables synchronization of the following items:</span></span>

- [<span data-ttu-id="8c2a0-114">Finance and Operationsin tuotteet Field Servicen tuotetyyppitietoja sisältäviin tuotteisiin</span><span class="sxs-lookup"><span data-stu-id="8c2a0-114">Products in Finance and Operations to products in Field Service that include Product Type information</span></span>](field-service-product.md)
- [<span data-ttu-id="8c2a0-115">Field Servicen työtilaukset Finance and Operationsin myyntitilauksiin</span><span class="sxs-lookup"><span data-stu-id="8c2a0-115">Work orders in Field Service to sales orders in Finance and Operations</span></span>](field-service-work-order.md)
- [<span data-ttu-id="8c2a0-116">Field Servicen laskut Finance and Operationsin vapaatekstilaskuihin</span><span class="sxs-lookup"><span data-stu-id="8c2a0-116">Invoices in Field Service to free text invoices in Finance and Operations</span></span>](field-service-invoice.md)

<span data-ttu-id="8c2a0-117">Esimerkki työtilauksen synkronoimisesta Field Servicen ja Finance and Operationsin välillä on lyhyessä YouTube-videossa [Työtilauksen  Dynamics 365 for Field Servicen ja Finance and Operationsin välillä](https://www.youtube.com/watch?v=hAB4TDVMjxU).</span><span class="sxs-lookup"><span data-stu-id="8c2a0-117">To see an example of how you can synchronize a work order between Field Service and Finance and Operations, watch the short YouTube video [Synchronize a work order between Dynamics 365 for Field Service and Finance and Operations](https://www.youtube.com/watch?v=hAB4TDVMjxU).</span></span>

[![](https://img.youtube.com/vi/hAB4TDVMjxU/0.jpg)](https://www.youtube.com/watch?v=hAB4TDVMjxU)

## <a name="system-requirements-for-finance-and-operations"></a><span data-ttu-id="8c2a0-118">Finance and Operations -sovelluksen järjestelmävaatimukset</span><span class="sxs-lookup"><span data-stu-id="8c2a0-118">System requirements for Finance and Operations</span></span>
<span data-ttu-id="8c2a0-119">Field Servicen integrointi tukee seuraavia versioita:</span><span class="sxs-lookup"><span data-stu-id="8c2a0-119">Field Service integration supports the following versions:</span></span>

### <a name="dynamics-365-for-finance-and-operations-version-80-april-2018-or-later"></a><span data-ttu-id="8c2a0-120">Dynamics 365 for Finance and Operations -versio 8.0 (huhtikuu 2018) tai uudempi</span><span class="sxs-lookup"><span data-stu-id="8c2a0-120">Dynamics 365 for Finance and Operations version 8.0 (April 2018) or later</span></span>

- <span data-ttu-id="8c2a0-121">Dynamics 365 for Finance and Operations versio 8.0 (huhtikuu 2018) julkaistiin huhtikuussa 2018; sen koontiversionumero on 8.0.30.8020 ja ympäristöpäivitys 15 (7.0.4841.35234).</span><span class="sxs-lookup"><span data-stu-id="8c2a0-121">Dynamics 365 for Finance and Operations version 8.0 (April 2018) was released in April 2018 and has an application build number 8.0.30.8020 with Platform Update 15 (7.0.4841.35234).</span></span> 

## <a name="system-requirements-for-field-service"></a><span data-ttu-id="8c2a0-122">Field Servicen järjestelmävaatimukset</span><span class="sxs-lookup"><span data-stu-id="8c2a0-122">System requirements for Field Service</span></span>
<span data-ttu-id="8c2a0-123">Seuraavat komponentit on asennettava, jotta Field Service -integrointiratkaisua voi käyttää:</span><span class="sxs-lookup"><span data-stu-id="8c2a0-123">To use the Field Service integration solution, you must install the following components:</span></span>

### <a name="microsoft-dynamics-365-for-field-service-90-or-later"></a><span data-ttu-id="8c2a0-124">Microsoft Dynamics 365 for Field Service 9.0 tai uudempi</span><span class="sxs-lookup"><span data-stu-id="8c2a0-124">Microsoft Dynamics 365 for Field Service 9.0 or later</span></span>

- <span data-ttu-id="8c2a0-125">Dynamics 365 for Field Servicen versio 1612 (9.0.1.733) (DB 9.0.1.733) online tai uudempi versio</span><span class="sxs-lookup"><span data-stu-id="8c2a0-125">Dynamics 365 for Field Service version 1612 (9.0.1.733) (DB 9.0.1.733) online or a later version.</span></span>
- <span data-ttu-id="8c2a0-126">Dynamics 365:N prospektista käteiseksi (P2C) -ratkaisu, versio 1.15.0.1 tai uudempi versio.</span><span class="sxs-lookup"><span data-stu-id="8c2a0-126">Prospect to Cash (P2C) solution for Dynamics 365, version 1.15.0.1 or a later version.</span></span> <span data-ttu-id="8c2a0-127">Ratkaisun voi ladata [AppSourcesta](https://appsource.microsoft.com/en-us/product/dynamics-365/mscrm.c7a48b40-eed3-4d67-93ba-f2364281feb3).</span><span class="sxs-lookup"><span data-stu-id="8c2a0-127">The solution is available for download from [AppSource](https://appsource.microsoft.com/en-us/product/dynamics-365/mscrm.c7a48b40-eed3-4d67-93ba-f2364281feb3).</span></span>
- <span data-ttu-id="8c2a0-128">Dynamics 365:n Field Service -integrointiratkaisu, versio 1.0.0.0 tai uudempi versio.</span><span class="sxs-lookup"><span data-stu-id="8c2a0-128">Field Service integration solution for Dynamics 365, version 1.0.0.0 or a later version.</span></span> <span data-ttu-id="8c2a0-129">Ratkaisun voi ladata [AppSourcesta](https://appsource.microsoft.com/en-us/product/dynamics-365/mscrm.p2cfieldserviceintegration).</span><span class="sxs-lookup"><span data-stu-id="8c2a0-129">The solution is available for download from [AppSource](https://appsource.microsoft.com/en-us/product/dynamics-365/mscrm.p2cfieldserviceintegration).</span></span>

