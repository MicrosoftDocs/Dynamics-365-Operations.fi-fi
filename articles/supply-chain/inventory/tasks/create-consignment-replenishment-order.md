---
title: Luo tavaralähetyksen täydennystilaus
description: Tässä menettelyssä kuvataan, miten luot tavaralähetyksen täydennystilauksen, jossa voit seurata odotettua toimittajan lähetystä tavaralähetysvarastoon.
author: mkirknel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ConsignmentReplenishmentOrder, ConsignmentReplenishmentOrderCreate, InventTrans, ConsignmentDraftReplenishmentOrderJournal, InventOnhandMovement, InventOnhandItem, InventItemIdLookupSimple
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9d3e33008d04ea8bb7d145c7b63cec23a4a45dd2
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/15/2019
ms.locfileid: "1549873"
---
# <a name="create-a-consignment-replenishment-order"></a>Luo tavaralähetyksen täydennystilaus

[!include [task guide banner](../../includes/task-guide-banner.md)]

Tässä menettelyssä kuvataan, miten luot tavaralähetyksen täydennystilauksen, jossa voit seurata odotettua toimittajan lähetystä tavaralähetysvarastoon. Se siinä kuvataan myös, miten tuotteiden vastaanotto kirjataan niin, että tavaralähetysvarasto rekisteröidään käytettäväksi varastoksi, jonka omistaa toimittaja. Tämä on yleensä hankinta-asiantuntijan tehtävä. Voit käyttää tätä opastusta USMF-yrityksen demotiedoissa. Tätä toimintaohje koskee toimintoa, joka lisättiin Dynamics 365 for Operations -ohjelmiston versiossa 1611.




## <a name="create-a-consignment-replenishment-order"></a>Luo tavaralähetyksen täydennystilaus
1. Siirry kohtaan Hankinta > Tavaralähetys > Tavaralähetyksen täydennystilaukset.
2. Valitse Uusi.
3. Kirjoita Toimittajan tili -kenttään toimittaja US-104.
    * Sinun on valittava toimittaja, joka on rekisteröity omistajaksi Varaston omistajat -sivulla.  
4. Valitse OK.
5. Valitse Lisää rivi.
6. Kirjoita Nimiketunnus-kenttään M9211CI.
    * Valitse nimike, joka on asetettu tavaralähetysvarastoon.  
7. Kirjoita numero Määrä-kenttään.
8. Kirjoita päivämäärä Pyydetty toimituspäivämäärä -kenttään.
    * MRP-moduuli käyttää pyydettyä ja vahvistettua päivämäärää tavaroiden saapumisen arviointiin.  
9. Kirjoita päivämäärä Vahvistettu toimituspäivämäärä-kenttään.
10. Laajenna Rivin erittely -osa.
11. Valitse Varastodimensiot-välilehti.
12. Saat omistajan näkyviin Varastodimensioiden omistaja -kenttään päivittämällä sivun.
    * Toimittaja US-104 on nyt merkitty omistaja.  

## <a name="check-the-inventory-transaction-status"></a>Tarkista varastotapahtuman tila
1. Valitse Varasto.
2. Valitse Tapahtumat.
3. Merkitse valittu rivi luettelossa.
    * Huomaa, että Vastaanotto-kentän arvo on Tilattu.  
4. Sulje sivu.

## <a name="receive-items"></a>Vastaanota nimikkeet
1. Valitse Tuotteen vastaanotto.
2. Kirjoita arvo Ulkoisen tuotteen vastaanotto -kenttään.
3. Syötä Määrä-kenttään numero, joka on pienempi kuin numero, joka siinä on. 
4. Valitse OK.

## <a name="check-the-on-hand-inventory"></a>Tarkista käytettävissä oleva varasto.
1. Valitse Varasto.
2. Valitse Käytettävissä.
3. Valitse Yleiskatsaus.
    * Toimitusvarastoon vastaanotetut nimikkeet, jotka omistaa toimittaja ovat käytettävissä. Tavaralähetyksen täydennystilauksella jäljellä oleva määrä näytetään Tilattu yhteensä -kentässä.  
4. Sulje sivu.
5. Valitse Sulje.

