--- 
title: Luo toimipaikan suunnitelma
description: Tuotannon suunnittelija laskee materiaali- ja kapasiteettivaatimukset, jotka koskevat tietyn nimikkeen tuotantoa.
author: YuyuScheller
manager: AnnBe
ms.date: 06/10/2016
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
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: d89d34d4d429faf87c70943961f7141a6258d482
ms.contentlocale: fi-fi
ms.lasthandoff: 07/27/2017

---
# <a name="create-a-plan-for-a-site"></a>Luo toimipaikan suunnitelma

[!include[task guide banner](../../includes/task-guide-banner.md)]

Tuotannon suunnittelija laskee materiaali- ja kapasiteettivaatimukset, jotka koskevat tietyn nimikkeen tuotantoa. Kun hankintaehdotukset on luotu, suunnittelija löytää tilaukset suunnittelemaltaan toimipaikalta ja vahvistaa tilaukset, aloittaen tärkeämmästä. Kiireisimpiä tilauksia ovat ne, jotka on vahvistettava samana päivänä. Käytä esittelyversion yritystä, USMF:ää, näiden tehtävien suorittamiseen.


## <a name="create-a-materials-and-capacity-plan-for-an-item"></a>Luo nimikkeen materiaali- ja kapasiteettisuunnitelma
1. Valitse Pääsuunnittelu.
    * Sinun on siirryttävä oletuskoontinäytölle.  
2. Valitse Suorita.
3. Laajenna Tietueet-kohta ja sisällytä osaan.
4. Valitse Suodatin.
5. Merkitse valittu rivi luettelossa.
6. Kirjoita arvo Ehdot-kenttään.
    * Esimerkki: D0001  
7. Valitse OK.
8. Valitse OK.
    * Tämä voi kestää muutamia minuutteja.  
9. Päivitä sivu.

## <a name="identify-the-urgent-planned-orders-for-the-item"></a>Tunnista nimikkeen suunnitellut tilaukset, jotka ovat kiireisiä
1. Avaa nimiketunnuksen sarakkeen suodatin.
2. Käytä suodatinta Nimiketunnus-kentässä niin, että arvo on D0001 ja suodatinoperaattori Alkaa.
3. Avaa sarakkeen Tilauspvm.-suodatin.
4. Käytä suodatinta "Tilauspäivä"-kentässä käyttäen arvona nykyistä päivämäärää ja "on täsmälleen" -suodatinoperaattoria.

## <a name="firm-all-the-urgent-orders-for-the-item"></a>Vahvista kaikki nimikkeen suunnitellut tilaukset, jotka ovat kiireisiä
1. Merkitse kaikki rivit tai poista kaikkien rivien merkinnät luettelossa.
2. Valitse Vahvista.
3. Valitse OK.


