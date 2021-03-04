---
title: Valtuuta oikaistu ennuste
description: Kaikkia ennusteen tietoja ei tarvitse valtuuttaa heti. Tässä artikkelissa kerrotaan, miten voit määrittää kauden, jolle ennuste on valtuutettu. Siinä myös kerrotaan, miten voit valtuuttaa ennusteen määrätyille yrityksille ja ennustemalleille.
author: roxanadiaconu
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqDemPlanImportForecastDialog
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 72734
ms.assetid: cb8fd809-605a-4a8b-a390-636edfec21f9
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5b599385f4bc79707ac7b6b814dd106813cbf3c9
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/13/2020
ms.locfileid: "4427321"
---
# <a name="authorize-an-adjusted-forecast"></a>Valtuuta oikaistu ennuste

[!include [banner](../includes/banner.md)]

Kaikkia ennusteen tietoja ei tarvitse valtuuttaa heti. Tässä artikkelissa kerrotaan, miten voit määrittää kauden, jolle ennuste on valtuutettu. Siinä myös kerrotaan, miten voit valtuuttaa ennusteen määrätyille yrityksille ja ennustemalleille.

Kaikkia ennusteen tietoja ei tarvitse valtuuttaa heti. Voit määrittää sen kauden alkamis- ja päättymispäivät, jolle ennuste on valtuutettu. Tämän toiminnon avulla voit lukita määrätyt aikajaksot. 

Määrittämäsi alkamis- ja päättymispäivämäärät pitää vastata sen säilön alkamis- ja päättymispäivämääriä, jossa ennuste luodaan. Järjestelmä pakottaa tämän rajoituksen ja säätää automaattisesti päivämäärät, jos muutos on tarpeen. 

Sivun **Valtuutus** välilehdellä **Tiedot** voit tarkastella viimeksi luotuja ennusteen tietoja. 

Voit valita yritykset ja ennustemallit, jotka valtuuttavat ennusteen käyttöön otettavaksi. Oletuksena tämä ruudukko sisältää kaikki yritykset, joille ennustettu kysyntä on luotu. Kullakin yrityksellä ennustemalli, joka vastaa nykyistä, pääsuunnitteluparametreissa määritettyä ennustesuunnitelmaa, on valmiiksi täytetty. Voit kuitenkin muuttaa tätä ennustemallia miksi tahansa kyseiselle yritykselle kuuluvaksi ennustemalliksi. Jos kysynnän ennusteen tietoja ei ole luotu valitulle yritykselle, saat tuontihetkellä varoitussanoman. 

On erittäin tärkeää, että ymmärrät, miten **Tallenna kysynnän perusennusteeseen tehdyt manuaaliset oikaisut** -valintaruutu toimii. Jos olet tehnyt manuaalisia oikaisuja tilastolliseen perusennusteeseen, oikaistut arvot on valtuutettu käytettäväksi, vaikka tämä valintaruutu olisi tyhjä. Muutokset kuitenkin hylätään valtuutuksen jälkeen. Näin ollen, seuraavan kerran kun ennuste luodaan, tämä ennuste on vain tilastollinen ennuste, eikä sillä ole manuaalisia ohituksia, vaikka **Siirrä manuaaliset oikaisut kysynnän ennusteeseen** -valintaruutu on valittuna. Voit näin ollen harkita **Tallenna kysynnän perusennusteeseen tehdyt manuaaliset oikaisut** -valintaruutumekanismia, jonka avulla voit säilyttää tai hylätä kaikki manuaaliset muutokset.

<a name="additional-resources"></a>Lisäresurssit
--------

[Manuaalisten oikaisujen tekeminen perusennusteeseen](manual-adjustments-baseline-forecast.md)

[Ennusteen tarkkuuden seuranta](monitor-forecast-accuracy.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]