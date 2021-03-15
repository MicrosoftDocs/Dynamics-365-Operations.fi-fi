---
title: Luo toimipaikan suunnitelma
description: Tuotannon suunnittelija laskee materiaali- ja kapasiteettivaatimukset, jotka koskevat tietyn nimikkeen tuotantoa.
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, ReqCreatePlanWorkspace, ReqTransPlanCard, ReqTransPOUrgentFormPart, SysQueryForm
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1b6d433257056c604500953060bf11ce3a3f5866
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/15/2021
ms.locfileid: "5007938"
---
# <a name="create-a-plan-for-a-site"></a>Luo toimipaikan suunnitelma

[!include [banner](../../includes/banner.md)]

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



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]