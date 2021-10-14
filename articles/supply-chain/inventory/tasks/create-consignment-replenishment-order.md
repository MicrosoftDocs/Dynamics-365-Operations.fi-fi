---
title: Luo tavaralähetyksen täydennystilaus
description: Tässä aiheessa kuvataan, miten luot tavaralähetyksen täydennystilauksen, jossa voit seurata odotettua toimittajan lähetystä tavaralähetysvarastoon.
author: yufeihuang
ms.date: 08/19/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ConsignmentReplenishmentOrder, ConsignmentReplenishmentOrderCreate, InventTrans, ConsignmentDraftReplenishmentOrderJournal, InventOnhandMovement, InventOnhandItem, InventItemIdLookupSimple, ConsignmentProductReceiptJournal, ConsignmentReplenishmentOrderLineQuantity
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: yufeihuang
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9076207b73c6c76cfc44e1e02b21aad4e3f321f8
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/29/2021
ms.locfileid: "7574590"
---
# <a name="create-a-consignment-replenishment-order"></a>Luo tavaralähetyksen täydennystilaus

[!include [banner](../../includes/banner.md)]

Tässä aiheessa kuvataan, miten luot tavaralähetyksen täydennystilauksen, jossa voit seurata odotettua toimittajan lähetystä tavaralähetysvarastoon. Se siinä kuvataan myös, miten tuotteiden vastaanotto kirjataan niin, että tavaralähetysvarasto rekisteröidään käytettäväksi varastoksi, jonka omistaa toimittaja. Tämä on yleensä hankinta-asiantuntijan tehtävä. Voit käyttää tätä opastusta USMF-yrityksen demotiedoissa. Tätä toimintaohje koskee toimintoa, joka lisättiin Dynamics 365 for Operations -ohjelmiston versiossa 1611.

## <a name="create-a-consignment-replenishment-order"></a>Luo tavaralähetyksen täydennystilaus
1. Siirry siirtymisruudussa kohtaan **Moduulit > Hankinta > Tavaralähetys > Tavaralähetyksen täydennystilaukset**.
2. Valitse **Uusi**.
3. Valitse **Toimittajatili**-kentässä toimittaja **US-104** (sinun on valittava toimittaja, joka on rekisteröity omistajaksi **varaston omistajat** -sivulla). 
4. Valitse **OK**.
5. Valitse **Lisää rivi**.
6. Kirjoita **Nimiketunnus**-kenttään `M9211CI` (sinun on valittava nimike, joka on määritetty lähetysvarastoa varten).
7. Anna **Määrä**-kentässä numero.
8. Kirjoita päivämäärä **Pyydetty toimituspäivämäärä** -kenttään. MRP-moduuli käyttää pyydettyä ja vahvistettua päivämäärää tavaroiden saapumisen arviointiin.  
9. Kirjoita päivämäärä **Vahvistettu toimituspäivämäärä** -kenttään.
10. Laajenna **Rivin erittely** -osa.
11. Valitse **Varastodimensiot**-välilehti.
12. Saat omistajan näkyviin **Varastodimensioiden omistaja** -kenttään päivittämällä sivun. Toimittaja US-104 on nyt merkitty omistaja.  

## <a name="check-the-inventory-transaction-status"></a>Tarkista varastotapahtuman tila
1. Valitse **Varasto**.
2. Valitse **Tapahtumat**.
3. Huomaa halutulla rivillä, että **Vastaanotto**-kentän arvo on **Tilattu**.  
4. Sulje sivu.

## <a name="receive-items"></a>Vastaanota nimikkeet
1. Valitse **Tuotteen vastaanotto**.
2. Kirjoita arvo **Ulkoisen tuotteen vastaanotto** -kenttään.
3. Syötä **Määrä**-kenttään numero, joka on pienempi kuin numero, joka siinä on. 
4. Valitse **OK**.

## <a name="check-the-on-hand-inventory"></a>Tarkista käytettävissä oleva varasto.
1. Valitse **Varasto**.
2. Valitse **Varastosaldo**.
3. Valitse **Yleiskatsaus**. Toimitusvarastoon vastaanotetut nimikkeet, jotka omistaa toimittaja ovat käytettävissä. Tavaralähetyksen täydennystilauksella jäljellä oleva määrä näytetään **Tilattu yhteensä** -kentässä.  
4. Sulje sivu.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]