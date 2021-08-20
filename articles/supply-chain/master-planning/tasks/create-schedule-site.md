---
title: Luo toimipisteelle aikataulu
description: Seuraavassa menettelyssä kuvataan, toimipaikan aloittamattomat tuotantotilaukset ajoitetaan.
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ProdTableListPage, ProdSchedule, ProdRouteJob
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a2af6b4553592099919be19aab62875e43ffdb0838a7e32e90a72283044fa348
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/05/2021
ms.locfileid: "6770261"
---
# <a name="create-a-schedule-for-a-site"></a>Luo toimipisteelle aikataulu

[!include [banner](../../includes/banner.md)]

Seuraavassa menettelyssä kuvataan, toimipaikan aloittamattomat tuotantotilaukset ajoitetaan.  Tämän menettelyn täytössä on käytetty USMF-yrityksen demotietoja.


## <a name="identify-production-orders-that-are-not-started"></a>Tunnista aloittamattomat tuotantotilaukset
1. Siirry kohtaan Tuotannonhallinta > Tuotantotilaukset > Kaikki tuotantotilaukset.
2. Käytä pikasuodatinta tietueiden etsimiseen. Voit esimerkiksi suodattaa Toimipaikka-kenttää arvolla 1.
    * 1 edustaa USMF:n toimipistettä. Jos et käytä USMF:ää, valitse oman yrityksesi toimipaikka.  
3. Avaa Tila-sarakkeen suodatin.
4. Suodattimen operaattorin "on täsmälleen" avulla voit käyttää suodatinta kentässä "Tila", jonka arvo on "Ajoitettu".

## <a name="create-a-schedule"></a>Luo aikataulu
1. Merkitse kaikki rivit tai poista kaikkien rivien merkinnät luettelossa.
2. Valitse toimintoruudussa Aikataulu.
3. Valitse Ajoita työt.
4. Valitse Ajoituksen suunta -kentässä Toimituspäivästä taaksepäin.
5. Valitse Rajallinen kapasiteetti -kentässä Ei.
6. Valitse Rajallinen materiaali -kentässä Ei.
7. Valitse OK.
    * Tämä saattaa kestää jonkin aikaa.  

## <a name="view-the-result-of-scheduled-production-orders"></a>Katso ajoitettujen tuotantotilauksien tulos
1. Merkitse valittu rivi luettelossa.
    * Voit merkitä minkä tahansa rivin.  
2. Valitse toimintoruudussa Tuotantotilaus.
3. Valitse Kaikki työt.
    * Tällä sivulla voit tarkastella työluetteloa. Aikataulutus-välilehdessä näet projektin alkamis- ja päättymispäivämäärät.  
4. Napsauta kohtaa Materiaalit.
    * Tällä sivulla voit tarkastella tuotantotilauksen toimintojen arvioitua materiaalinkulutusta ja käytettävissä olevaa varastoa.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]