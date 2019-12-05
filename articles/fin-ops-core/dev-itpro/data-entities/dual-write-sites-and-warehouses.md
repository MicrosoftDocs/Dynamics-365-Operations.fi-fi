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
# <a name="integrated-sites-and-warehouses"></a>Integroidut toimipaikat ja varastot

[!include [banner](../includes/banner.md)]

Tässä aiheessa kuvataan toimipaikkojen ja varastojen tietojen integraatiota Finance and Operationsin ja Common Data Servicen välillä. Toiminnalliset toimipaikat ja varastot ovat Supply Chain Management -sovelluksen yleisiä käsitteitä. Niitä käytetään yrityksen toimitusketjun mallintamiseen.

## <a name="templates"></a>Mallit

Common Data Service -integraation kanssa nämä käsitteet ja kaikki niihin liittyvät tiedot ovat käytettävissä Common Data Servicessa seuraavassa taulukossa esitettyjen toimipaikkojen ja varastojen tietoyksiköiden avulla.

Finance and Operations -sovellukset | Muut Dynamics 365 -sovellukset | Kuvaus
--------------------------|---------------------------|---
Sivustot | msdyn_operationalsites | 
Varastot | msdyn_warehouses | 

[!include [symbols](../includes/dual-write-symbols.md)]

[!include [operational sites](dual-write/InventOperationalSiteEntity-msdyn-operationalsite.md)]

[!include [warehouses](dual-write/InventWarehouseEntity-msdyn-warehouse.md)]

