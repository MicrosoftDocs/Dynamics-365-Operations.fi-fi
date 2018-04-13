--- 
title: Kustannusobjektien luominen
description: "Tässä menettelyssä kuvataan, miten luot kustannusobjekteja tuomalla Dynamics 365 for Finance and Operationsin kustannuspaikkojen taloushallinnon dimension kustannushallintaan tietoyhdistimellä."
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
ms.sourcegitcommit: a0739304723d19b910388893d08e8c36a1f49d13
ms.openlocfilehash: 21fa90557b665e0777935cc6bae8cd9f1c29cb60
ms.contentlocale: fi-fi
ms.lasthandoff: 03/26/2018

---
# <a name="create-cost-objects"></a>Kustannusobjektien luominen 

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

Tässä menettelyssä kuvataan, miten luot kustannusobjekteja tuomalla Dynamics 365 for Finance and Operationsin kustannuspaikkojen taloushallinnon dimension kustannushallintaan tietoyhdistimellä. Tämän menettelyn luomisessa käytetty USMF-yrityksen demotietoja. Nämä ohjeet koskevat kustannuslaskentatoimintoa, joka lisättiin Dynamics 365 for Operationsin versiossa 1611.


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


