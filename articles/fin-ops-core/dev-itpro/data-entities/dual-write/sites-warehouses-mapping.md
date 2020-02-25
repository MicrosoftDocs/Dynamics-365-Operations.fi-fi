---
title: Integroidut toimipaikat ja varastot
description: Tässä aiheessa kuvataan sivuston ja varaston tietojen integraatiota Finance and Operationsin ja Common Data Servicen välillä.
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
ms.openlocfilehash: 0f5ed58ad50df49250aa4c001401ff52d460dfa6
ms.sourcegitcommit: 54baab2a04e5c534fc2d1fd67b67e23a152d4e57
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/04/2020
ms.locfileid: "3019755"
---
# <a name="integrated-sites-and-warehouses"></a><span data-ttu-id="6784e-103">Integroidut toimipaikat ja varastot</span><span class="sxs-lookup"><span data-stu-id="6784e-103">Integrated sites and warehouses</span></span>

[!include [banner](../../includes/banner.md)]

[!include [preview-banner](../../includes/preview-banner.md)]

<span data-ttu-id="6784e-104">Tässä aiheessa kuvataan sivuston ja varaston tietojen integraatiota Finance and Operationsin ja Common Data Servicen välillä.</span><span class="sxs-lookup"><span data-stu-id="6784e-104">This topic describes the integration of site and warehouse data between Finance and Operations and Common Data Service.</span></span> <span data-ttu-id="6784e-105">Toiminnalliset toimipaikat ja varastot ovat Supply Chain Management -sovelluksen yleisiä käsitteitä.</span><span class="sxs-lookup"><span data-stu-id="6784e-105">Operational sites and warehouses are common concepts in a Supply Chain Management application.</span></span> <span data-ttu-id="6784e-106">Niitä käytetään yrityksen toimitusketjun mallintamiseen.</span><span class="sxs-lookup"><span data-stu-id="6784e-106">They are used to model the supply chain of your company.</span></span>

## <a name="templates"></a><span data-ttu-id="6784e-107">Mallit</span><span class="sxs-lookup"><span data-stu-id="6784e-107">Templates</span></span>

<span data-ttu-id="6784e-108">Common Data Service -integraation kanssa nämä käsitteet ja kaikki niihin liittyvät tiedot ovat käytettävissä Common Data Servicessa seuraavassa taulukossa esitettyjen toimipaikkojen ja varastojen tietoyksiköiden avulla.</span><span class="sxs-lookup"><span data-stu-id="6784e-108">With the integration with Common Data Service, these concepts and all their related information are available in Common Data Service using the sites and warehouses data entities in the following table.</span></span>

<span data-ttu-id="6784e-109">Finance and Operations -sovellukset</span><span class="sxs-lookup"><span data-stu-id="6784e-109">Finance and Operations apps</span></span> | <span data-ttu-id="6784e-110">Muut Dynamics 365 -sovellukset</span><span class="sxs-lookup"><span data-stu-id="6784e-110">Other Dynamics 365 apps</span></span> | <span data-ttu-id="6784e-111">Kuvaus</span><span class="sxs-lookup"><span data-stu-id="6784e-111">Description</span></span>
--------------------------|---------------------------|---
<span data-ttu-id="6784e-112">Sivustot</span><span class="sxs-lookup"><span data-stu-id="6784e-112">Sites</span></span> | <span data-ttu-id="6784e-113">msdyn_operationalsites</span><span class="sxs-lookup"><span data-stu-id="6784e-113">msdyn_operationalsites</span></span> | 
<span data-ttu-id="6784e-114">Varastot</span><span class="sxs-lookup"><span data-stu-id="6784e-114">Warehouses</span></span> | <span data-ttu-id="6784e-115">msdyn_warehouses</span><span class="sxs-lookup"><span data-stu-id="6784e-115">msdyn_warehouses</span></span> | 

[!include [symbols](../../includes/dual-write-symbols.md)]

[!include [operational sites](includes/InventOperationalSiteEntity-msdyn-operationalsite.md)]

[!include [warehouses](includes/InventWarehouseEntity-msdyn-warehouse.md)]

