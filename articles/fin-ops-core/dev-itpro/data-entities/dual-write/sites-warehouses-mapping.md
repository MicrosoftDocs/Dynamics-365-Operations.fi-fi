---
title: Integroidut toimipaikat ja varastot
description: Tässä aiheessa kuvataan sivuston ja varaston tietojen integraatiota Finance and Operationsin ja Dataversen välillä.
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
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: benebotg
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-08-15
ms.openlocfilehash: d192343d78f9248e4d1232d6aee1a1f800383805
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/05/2020
ms.locfileid: "4679317"
---
# <a name="integrated-sites-and-warehouses"></a><span data-ttu-id="0e116-103">Integroidut toimipaikat ja varastot</span><span class="sxs-lookup"><span data-stu-id="0e116-103">Integrated sites and warehouses</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]



<span data-ttu-id="0e116-104">Tässä aiheessa kuvataan sivuston ja varaston tietojen integraatiota Finance and Operationsin ja Dataversen välillä.</span><span class="sxs-lookup"><span data-stu-id="0e116-104">This topic describes the integration of site and warehouse data between Finance and Operations and Dataverse.</span></span> <span data-ttu-id="0e116-105">Toiminnalliset toimipaikat ja varastot ovat Supply Chain Management -sovelluksen yleisiä käsitteitä.</span><span class="sxs-lookup"><span data-stu-id="0e116-105">Operational sites and warehouses are common concepts in a Supply Chain Management application.</span></span> <span data-ttu-id="0e116-106">Niitä käytetään yrityksen toimitusketjun mallintamiseen.</span><span class="sxs-lookup"><span data-stu-id="0e116-106">They are used to model the supply chain of your company.</span></span>

## <a name="templates"></a><span data-ttu-id="0e116-107">Mallit</span><span class="sxs-lookup"><span data-stu-id="0e116-107">Templates</span></span>

<span data-ttu-id="0e116-108">Dataverse -integraation kanssa nämä käsitteet ja kaikki niihin liittyvät tiedot ovat käytettävissä Dataversessa seuraavassa taulukossa esitettyjen toimipaikkojen ja varastojen tietotaulujen avulla.</span><span class="sxs-lookup"><span data-stu-id="0e116-108">With the integration with Dataverse, these concepts and all their related information are available in Dataverse using the sites and warehouses data tables in the following table.</span></span>

<span data-ttu-id="0e116-109">Finance and Operations -sovellukset</span><span class="sxs-lookup"><span data-stu-id="0e116-109">Finance and Operations apps</span></span> | <span data-ttu-id="0e116-110">Muut Dynamics 365 -sovellukset</span><span class="sxs-lookup"><span data-stu-id="0e116-110">Other Dynamics 365 apps</span></span> | <span data-ttu-id="0e116-111">kuvaus</span><span class="sxs-lookup"><span data-stu-id="0e116-111">Description</span></span>
--------------------------|---------------------------|---
<span data-ttu-id="0e116-112">Sivustot</span><span class="sxs-lookup"><span data-stu-id="0e116-112">Sites</span></span> | <span data-ttu-id="0e116-113">msdyn_operationalsites</span><span class="sxs-lookup"><span data-stu-id="0e116-113">msdyn_operationalsites</span></span> | 
<span data-ttu-id="0e116-114">Varastot</span><span class="sxs-lookup"><span data-stu-id="0e116-114">Warehouses</span></span> | <span data-ttu-id="0e116-115">msdyn_warehouses</span><span class="sxs-lookup"><span data-stu-id="0e116-115">msdyn_warehouses</span></span> | 

[!include [symbols](../../includes/dual-write-symbols.md)]

[!include [operational sites](includes/InventOperationalSiteEntity-msdyn-operationalsite.md)]

[!include [warehouses](includes/InventWarehouseEntity-msdyn-warehouse.md)]

