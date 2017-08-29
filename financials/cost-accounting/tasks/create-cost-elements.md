--- 
title: Luo kustannustasot
description: Kustannuselementtien luomiseen Kustannuslaskennassa on useita keinoja.
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
ms.openlocfilehash: 0b1045610881bc272798f1176fbca58731e5d43b
ms.contentlocale: fi-fi
ms.lasthandoff: 07/27/2017

---
# <a name="create-cost-elements"></a>Luo kustannustasot 

[!include[task guide banner](../../includes/task-guide-banner.md)]

Kustannuselementtien luomiseen Kustannuslaskennassa on useita keinoja. Tässä menettelyssä kuvataan, miten kustannuselementtejä luodaan tuomalla päätilejä tietoyhdistimen kautta. Tämän menettelyn luomisessa käytetty USMF-yrityksen demotietoja. Nämä ohjeet koskevat kustannuslaskentatoimintoa, joka lisättiin Dynamics 365 for Operationsin versiossa 1611.


## <a name="create-new-cost-elements"></a>Luo uudet kustannustasot
1. Valitse Kustannuslaskenta > Dimensiot > Kustannuselementin dimensiot.
2. Valitse Uusi.
3. Kirjoita arvo Nimi-kenttään.
4. Syötä tai valitse arvo Dimension jäsenten tietoyhdistin -kentässä.
5. Kirjoita arvo Kuvaus-kenttään.
6. Valitse Tallenna.

## <a name="configure-the-data-connector"></a>Määritä tietoyhdistin
1. Valitse Määritä dimension jäsenen lähde.
2. Anna tai valitse arvo Tilikartta-kentässä.
    * Valitse Jaettu käyttämään jaettua tilikarttaa.  
3. Valitse Uusi.
4. Merkitse valittu rivi luettelossa.
    * Voit suodattaa tilit vastaamaan ehtojasi.  
5. Anna tai valitse arvo Päätililtä-kentässä.
6. Syötä tai valitse arvo Päätilille-kentässä.
7. Valitse OK.

## <a name="import-main-accounts"></a>Tuo päätilit
1. Valitse Tuo dimension jäsenet.
    * Päätilit tuodaan kustannuslaskentaan käytettäväksi kustannuselementteinä.  
2. Valitse OK.

## <a name="view-the-imported-accounts-as-cost-elements"></a>Näytä tuodut tilit kustannuselementteinä
1. Valitse Näytä dimension jäsenet.
    * Näytä tuodut kirjanpitotilit yrityksesi kustannuselementteinä joihin kustannukset voivat virrata.  


