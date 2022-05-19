---
title: Kirjanpitokalenterin muuttaminen tai määrittäminen uudelleen
description: Tässä ohjeaiheessa kerrotaan, miten kirjanpidon määritettyä kalenteria muutetaan ja miten uusi kalenteri määritetään kirjanpitoon.
author: kweekley
ms.date: 05/07/2021
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2021-5-07
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 25777a5b807921acc13338116627e9356fe62a20
ms.sourcegitcommit: 04e6c1c9400e1b582180cf3e0e4767434e736c26
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/05/2022
ms.locfileid: "8711628"
---
# <a name="change-or-reassign-a-ledger-calendar"></a>Kirjanpitokalenterin muuttaminen tai määrittäminen uudelleen

[!include [banner](../includes/banner.md)]

Tässä ohjeaiheessa kerrotaan, miten kirjanpidon määritettyä kalenteria muutetaan ja miten uusi kalenteri määritetään kirjanpitoon.

## <a name="issue"></a>Ongelma

Joskus yritysten on joko muutettava olemassa olevaa kirjanpidon määritettyä kalenteria tai määritettävä uusi kalenteri.

## <a name="resolution"></a>Ratkaisu

Kirjanpitokalenterin muuttamiseksi tai sen määrittämiseksi uudelleen on kaksi eri skenaariota. Ensimmäisessä skenaariossa muutetaan olemassa olevaa kalenteria, joka on jo määritetty kirjanpitoon. Toisessa skenaariossa luodaan uusi kalenteri ja määritetään se kirjanpitoon. Molemmat muutokset voidaan tehdä milloin tahansa. Ne voidaan tehdä jopa sen jälkeen, kun kirjanpitoon on kirjattu tapahtumia.

### <a name="change-an-existing-fiscal-calendar"></a>Aiemmin luodun kirjanpidon kalenterin muuttaminen

Jos haluat muuttaa kirjanpidon määritettyä olemassa olevaa kalenteria, siirry kohtaan **Kirjanpito \> Kirjanpidon asetukset \> Kirjanpito** ja avaa **Kirjanpidon kalenterit** -sivu valitsemalla kirjanpidon kalenterin linkki.

Kalenteriin ei voi tehdä mitä tahansa muutoksia. Esimerkiksi vuoden *jaksojen* aloitus- ja päättymispäivää voi muuttaa, mutta kalenterin *vuoden* aloitus- ja päättymispäivää ei voi muuttaa.

Jos haluat muuttaa vuoden jaksoja, valitse haluamasi kalenteri ja vuosi. Poista ensin joitakin toimintajaksoja tai kaikki toimintajaksot **Poista jakso** -painikkeen avulla. Kaikki toimintajaksot voidaan poistaa ensimmäistä lukuun ottamatta. Jaa sitten jäljellä oleva jakso tai jäljellä olevat jaksot **Jaa jakso** -painikkeen avulla uusiksi jaksoiksi syöttämällä seuraavalle jaksolle soveltuva aloituspäivämäärä.

Kun kalenterin jaksot on muutettu, suorita **Laske kirjanpidon jaksot uudelleen** -prosessi jokaisessa yrityksessä, jolle kalenteri on määritetty. Vaikka tämän vaiheen suorittamisesta ei muistuteta varoitussanomalla, uudelleenlaskentaprosessi vaaditaan, jotta kirjanpidon kuhunkin kirjattuun tapahtumaan määritetty jakso päivitetään. Voit suorittaa uudelleenlaskentaprosessin valitsemalla **Laske kirjanpidon jaksot uudelleen** kunkin yrityksen **Kirjanpidon asetukset** -sivulla.

Jos uudelleenlaskentaprosessia ei suoriteta, pääkirjan tai raporttien tapahtumien saldojen sisällytys jaksoihin voi olla virheellinen. Tässä tapauksessa voit korjata saldot milloin tahansa suorittamalla uudelleenlaskentaprosessin.

### <a name="assign-a-new-fiscal-calendar"></a>Uuden kirjanpidon kalenterin määrittäminen

Jos haluat määrittää uuden kirjanpidon kalenterin, siirry kohtaan **Kirjanpito \> Kirjanpidon asetukset \> Kirjanpito** ja valitse **Muokkaa**. Tämän jälkeen **Kirjanpito**-sivu on muokkaustilassa. Valitse sitten **Kirjanpidon kalenteri** -kenttä ja valitse uusi kirjanpidon kalenteri.

Kun kirjanpidon kalenteria on muutettu, suorita **Laske kirjanpidon jaksot uudelleen**. Kun määrität kirjanpitoon uuden kirjanpidon kalenterin, näyttöön tulee tämän vaiheen suorittamisesta muistuttava sanoma. Uudelleenlaskentaprosessi ei ole valinnainen, vaikka sanomasta saattaa saada sellaisen kuvan. Kirjanpidon kullekin kirjatulle tapahtumalle määritetty jakso on päivitettävä. Jos haluat suorittaa uudelleenlaskentaprosessin, valitse **Laske kirjanpidon jaksot uudelleen** **Kirjanpidon asetukset** -sivulla.

Jos uudelleenlaskentaprosessia ei suoriteta, pääkirjan tai raporttien tapahtumien saldojen sisällytys jaksoihin voi olla virheellinen. Tässä tapauksessa voit korjata saldot milloin tahansa suorittamalla uudelleenlaskentaprosessin.
