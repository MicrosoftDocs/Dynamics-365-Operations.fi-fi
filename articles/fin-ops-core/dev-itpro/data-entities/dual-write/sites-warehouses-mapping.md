---
title: Integroidut toimipaikat ja varastot
description: Tässä aiheessa kuvataan sivuston ja varaston tietojen integraatiota Finance and Operationsin ja Dataversen välillä.
author: t-benebo
ms.date: 10/09/2019
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 533635ece005636dcee4e24d1d132111e1e2b370
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2021
ms.locfileid: "5750663"
---
# <a name="integrated-sites-and-warehouses"></a>Integroidut toimipaikat ja varastot

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]



Tässä aiheessa kuvataan sivuston ja varaston tietojen integraatiota Finance and Operationsin ja Dataversen välillä. Toiminnalliset toimipaikat ja varastot ovat Supply Chain Management -sovelluksen yleisiä käsitteitä. Niitä käytetään yrityksen toimitusketjun mallintamiseen.

## <a name="templates"></a>Mallit

Dataverse -integraation kanssa nämä käsitteet ja kaikki niihin liittyvät tiedot ovat käytettävissä Dataversessa seuraavassa taulukossa esitettyjen toimipaikkojen ja varastojen tietotaulujen avulla.

Finance and Operations -sovellukset | Muut Dynamics 365 -sovellukset | kuvaus
--------------------------|---------------------------|---
Sivustot | msdyn_operationalsites | 
Varastot | msdyn_warehouses | 

[!include [symbols](../../includes/dual-write-symbols.md)]

[!include [operational sites](includes/InventOperationalSiteEntity-msdyn-operationalsite.md)]

[!include [warehouses](includes/InventWarehouseEntity-msdyn-warehouse.md)]



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]