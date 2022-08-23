---
title: Luo kustannustasot
description: Kustannuselementtien luomiseen Kustannuslaskennassa on useita keinoja.
author: kfend
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: kfend
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.search.form: CAMDimension, CAMAXMainAccountDimensionMemberProviderConfiguration, CAMDimensionMember
ms.openlocfilehash: 9ca826e54171a3dc3582dc5ceb716ac009d45674
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/12/2022
ms.locfileid: "9280717"
---
# <a name="create-cost-elements"></a>Luo kustannustasot 

[!include [banner](../../includes/banner.md)]

Kustannuselementtien luomiseen Kustannuslaskennassa on useita keinoja. Tässä menettelyssä kuvataan, miten kustannuselementtejä luodaan tuomalla päätilejä tietoyhdistimen kautta. Tämän menettelyn luomisessa käytetty USMF-yrityksen demotietoja. Tätä toimintaohje koskee Kustannuslaskennan toimintoa, joka lisättiin Dynamics 365 for Operations -ohjelmiston versiossa 1611.


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



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
