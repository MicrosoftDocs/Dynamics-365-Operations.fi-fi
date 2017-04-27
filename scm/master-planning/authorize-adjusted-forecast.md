---
title: Valtuuta oikaistu ennuste
description: "Kaikkia ennusteen tietoja ei tarvitse valtuuttaa heti. Tässä artikkelissa kerrotaan, miten voit määrittää kauden, jolle ennuste on valtuutettu. Siinä myös kerrotaan, miten voit valtuuttaa ennusteen määrätyille yrityksille ja ennustemalleille."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: ReqDemPlanImportForecastDialog
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 72734
ms.assetid: cb8fd809-605a-4a8b-a390-636edfec21f9
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: f151f4b4290df0b2bf1b5d1159654bd248a439b1
ms.lasthandoff: 03/31/2017


---

# <a name="authorize-an-adjusted-forecast"></a>Valtuuta oikaistu ennuste

[!include[banner](../includes/banner.md)]


Kaikkia ennusteen tietoja ei tarvitse valtuuttaa heti. Tässä artikkelissa kerrotaan, miten voit määrittää kauden, jolle ennuste on valtuutettu. Siinä myös kerrotaan, miten voit valtuuttaa ennusteen määrätyille yrityksille ja ennustemalleille.

Kaikkia ennusteen tietoja ei tarvitse valtuuttaa heti. Voit määrittää sen kauden alkamis- ja päättymispäivät, jolle ennuste on valtuutettu. Tämän toiminnon avulla voit lukita määrätyt aikajaksot. 

Määrittämäsi alkamis- ja päättymispäivämäärät pitää vastata sen säilön alkamis- ja päättymispäivämääriä, jossa ennuste luodaan. Järjestelmä pakottaa tämän rajoituksen ja säätää automaattisesti päivämäärät, jos muutos on tarpeen. 

Sivun **Valtuutus** välilehdellä **Tiedot** voit tarkastella viimeksi luotuja ennusteen tietoja. 

Voit valita yritykset ja ennustemallit, jotka valtuuttavat ennusteen käyttöön otettavaksi. Oletuksena tämä ruudukko sisältää kaikki yritykset, joille ennustettu kysyntä on luotu. Kullakin yrityksellä ennustemalli, joka vastaa nykyistä, pääsuunnitteluparametreissa määritettyä ennustesuunnitelmaa, on valmiiksi täytetty. Voit kuitenkin muuttaa tätä ennustemallia miksi tahansa kyseiselle yritykselle kuuluvaksi ennustemalliksi. Jos kysynnän ennusteen tietoja ei ole luotu valitulle yritykselle, saat tuontihetkellä varoitussanoman. 

On erittäin tärkeää, että ymmärrät, miten **Tallenna kysynnän perusennusteeseen tehdyt manuaaliset oikaisut** -valintaruutu toimii. Jos olet tehnyt manuaalisia oikaisuja tilastolliseen perusennusteeseen, oikaistut arvot on valtuutettu käytettäväksi, vaikka tämä valintaruutu olisi tyhjä. Muutokset kuitenkin hylätään valtuutuksen jälkeen. Näin ollen, seuraavan kerran kun ennuste luodaan, tämä ennuste on vain tilastollinen ennuste, eikä sillä ole manuaalisia ohituksia, vaikka **Siirrä manuaaliset oikaisut kysynnän ennusteeseen** -valintaruutu on valittuna. Voit näin ollen harkita **Tallenna kysynnän perusennusteeseen tehdyt manuaaliset oikaisut** -valintaruutumekanismia, jonka avulla voit säilyttää tai hylätä kaikki manuaaliset muutokset.

<a name="see-also"></a>Lisätietoja
--------

[Manuaalisten oikaisujen tekeminen perusennusteeseen](manual-adjustments-baseline-forecast.md)

[Ennusteen tarkkuuden valvonta](monitor-forecast-accuracy.md)




