--- 
title: Kustannusobjektien luominen
description: "Tässä menettelyssä kuvataan, miten luot kustannusobjekteja tuomalla Dynamics 365 for Finance and Operations, Enterprise Editionin kustannuspaikkojen taloushallinnon dimension kustannushallintaan tietoyhdistimellä."
author: YuyuScheller
manager: AnnBe
ms.date: 10/25/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: yuyus
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: 79cb18717c6b42ef0307f304d28902dd66f0f932
ms.contentlocale: fi-fi
ms.lasthandoff: 07/27/2017

---
# <a name="create-cost-objects"></a>Kustannusobjektien luominen 

[!include[task guide banner](../../includes/task-guide-banner.md)]

Tässä menettelyssä kuvataan, miten luot kustannusobjekteja tuomalla Dynamics 365 for Finance and Operations, Enterprise Editionin kustannuspaikkojen taloushallinnon dimension kustannushallintaan tietoyhdistimellä. Tämän menettelyn luomisessa käytetty USMF-yrityksen demotietoja. Nämä ohjeet koskevat kustannuslaskentatoimintoa, joka lisättiin Dynamics 365 for Operationsin versiossa 1611.


## <a name="create-new-cost-objects"></a>Luo uudet kustannusobjektit
1. Valitse Kustannuslaskenta > Dimensiot > Kustannusobjektin dimensiot.
2. Valitse Uusi.
3. Kirjoita arvo Nimi-kenttään.
4. Syötä tai valitse arvo Dimension jäsenten tietoyhdistin -kentässä.
5. Kirjoita arvo Kuvaus-kenttään.
6. Valitse Tallenna.

## <a name="configure-the-data-connector"></a>Määritä tietoyhdistin
1. Valitse Määritä dimension jäsenen lähde.
    * Valitse CostCenter tuodaksesi CostCenter-dimension kustannuslaskentaan.  
2. Valitse Dimension nimi -kentässä Kustannuspaikka.
3. Valitse OK.

## <a name="import-cost-centers"></a>Tuo kustannuspaikat
1. Valitse Tuo dimension jäsenet.
2. Valitse OK.

## <a name="view-the-imported-cost-centers"></a>Näytä tuodut kustannuspaikat
1. Valitse Näytä dimension jäsenet.


