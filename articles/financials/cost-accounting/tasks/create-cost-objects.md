--- 
title: Kustannusobjektien luominen
description: "Tässä menettelyssä kuvataan, miten luot kustannusobjekteja tuomalla Dynamics 365 for Finance and Operations, Enterprise Editionin kustannuspaikkojen taloushallinnon dimension kustannushallintaan tietoyhdistimellä."
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CAMDimension, CAMAXFinancialDimensionMemberProviderConfiguration, CAMDimensionMember
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 5d43274aed2edbb91fd4e399cb8d45e91646b055
ms.contentlocale: fi-fi
ms.lasthandoff: 09/29/2017

---
# <a name="create-cost-objects"></a>Kustannusobjektien luominen 

[!include [task guide banner](../../includes/task-guide-banner.md)]

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


