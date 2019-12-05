---
title: Integroidut toimipaikat ja varastot
description: Tässä aiheessa kuvataan toimipaikkojen ja varastojen tietojen integraatiota Finance and Operationsin ja Common Data Servicen välillä.
author: t-benebo
manager: AnnBe
ms.date: 10/09/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: benebotg
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-08-15
ms.openlocfilehash: 4cf402e2811aaf92ddfa78eaf6d8887d88d93cbc
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/06/2019
ms.locfileid: "2770983"
---
# <a name="integrated-sites-and-warehouses"></a><span data-ttu-id="b1ede-103">Integroidut toimipaikat ja varastot</span><span class="sxs-lookup"><span data-stu-id="b1ede-103">Integrated sites and warehouses</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b1ede-104">Tässä aiheessa kuvataan toimipaikkojen ja varastojen tietojen integraatiota Finance and Operationsin ja Common Data Servicen välillä.</span><span class="sxs-lookup"><span data-stu-id="b1ede-104">This topic describes the integration of site and warehouse data between Finance and Operations and Common Data Service.</span></span> <span data-ttu-id="b1ede-105">Toiminnalliset toimipaikat ja varastot ovat Supply Chain Management -sovelluksen yleisiä käsitteitä.</span><span class="sxs-lookup"><span data-stu-id="b1ede-105">Operational sites and warehouses are common concepts in a Supply Chain Management application.</span></span> <span data-ttu-id="b1ede-106">Niitä käytetään yrityksen toimitusketjun mallintamiseen.</span><span class="sxs-lookup"><span data-stu-id="b1ede-106">They are used to model the supply chain of your company.</span></span>

## <a name="templates"></a><span data-ttu-id="b1ede-107">Mallit</span><span class="sxs-lookup"><span data-stu-id="b1ede-107">Templates</span></span>

<span data-ttu-id="b1ede-108">Common Data Service -integraation kanssa nämä käsitteet ja kaikki niihin liittyvät tiedot ovat käytettävissä Common Data Servicessa seuraavassa taulukossa esitettyjen toimipaikkojen ja varastojen tietoyksiköiden avulla.</span><span class="sxs-lookup"><span data-stu-id="b1ede-108">With the integration with Common Data Service, these concepts and all their related information are available in Common Data Service using the sites and warehouses data entities in the following table.</span></span>

<span data-ttu-id="b1ede-109">Finance and Operations -sovellukset</span><span class="sxs-lookup"><span data-stu-id="b1ede-109">Finance and Operations apps</span></span> | <span data-ttu-id="b1ede-110">Muut Dynamics 365 -sovellukset</span><span class="sxs-lookup"><span data-stu-id="b1ede-110">Other Dynamics 365 apps</span></span> | <span data-ttu-id="b1ede-111">Kuvaus</span><span class="sxs-lookup"><span data-stu-id="b1ede-111">Description</span></span>
--------------------------|---------------------------|---
<span data-ttu-id="b1ede-112">Sivustot</span><span class="sxs-lookup"><span data-stu-id="b1ede-112">Sites</span></span> | <span data-ttu-id="b1ede-113">msdyn_operationalsites</span><span class="sxs-lookup"><span data-stu-id="b1ede-113">msdyn_operationalsites</span></span> | 
<span data-ttu-id="b1ede-114">Varastot</span><span class="sxs-lookup"><span data-stu-id="b1ede-114">Warehouses</span></span> | <span data-ttu-id="b1ede-115">msdyn_warehouses</span><span class="sxs-lookup"><span data-stu-id="b1ede-115">msdyn_warehouses</span></span> | 

[!include [symbols](../includes/dual-write-symbols.md)]

[!include [operational sites](dual-write/InventOperationalSiteEntity-msdyn-operationalsite.md)]

[!include [warehouses](dual-write/InventWarehouseEntity-msdyn-warehouse.md)]

