--- 
title: "Ostoreskontran laskujen täsmäytyksen vahvistuksen määrittäminen"
description: "Tässä tallenteessa käytetään esittely-yritystä USMF."
author: abruer
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: 8959cf3a45f42e0ef5f0d79726c63184c274efff
ms.contentlocale: fi-fi
ms.lasthandoff: 07/27/2017

---
# <a name="set-up-accounts-payable-invoice-matching-validation"></a>Ostoreskontran laskujen täsmäytyksen vahvistuksen määrittäminen

[!include[task guide banner](../../includes/task-guide-banner.md)]

Tässä tallenteessa käytetään esittely-yritystä USMF. Nämä vaiheet suorittaa ostoreskontran esimies tai laskentapäällikön rooli. Varmista ennen aloittamista, että laskun täsmäytyksen konfigurointiavain on valittuna. Jos oma yrityksesi seuraa kuluja, kuten rahtia, veloituksien avulla, varmista että kulujen konfigurointiavain on valittuna.  Ostoreskontran laskujen täsmäytys on prosessi, jossa täsmäytetään toimittajan laskun, ostotilauksen ja tuotteen vastaanoton tiedot. Näissä asiakirjoissa olevia eroja kutsutaan ristiriidoiksi. Täsmäytysristiriitoja verrataan määritettyihin toleransseihin. Jos täsmäytysristiriita ylittää toleranssin prosentin tai summan, täsmäytyksen varianssin kuvakkeet näkyvät toimittajan laskun lomakkeella ja laskun täsmäytyksen tietojen lomakkeella.

1. Siirry kohtaan Ostoreskontra > Asetukset > Ostoreskontran parametrit.
2. Valitse Laskun oikeellisuustarkistus -välilehti.
3. Valitse Ota käyttöön laskujen täsmäytyksen vahvistus -valintaruutu tai poista sen valinta.
    * Määritä, onko hyväksyntä pakollinen, ennen kuin laskun vastaavuuden ristiriitoja sisältävä lasku voidaan kirjata. Jos arvoksi on määritetty Salli varoituksella, kuvallinen osoitin näyttää, kun laskun täsmäytyksen ristiriita ylittää toleranssin. Voit kuitenkin kirjata laskun. Voit käyttää työnkulkuja yhdessä laskun täsmäytyksen tarkistuksen kanssa, kun varmistat, että Kirjaa lasku, jossa on ristiriitoja -kentän arvoksi on määritetty Salli varoituksella. Tällöin hyväksyntää ei tehdä useita kertoja.  
    * Valitse Päivitä laskun otsikon täsmäytyksen tila automaattisesti -kentässä, suoritetaanko täsmäytys automaattisesti järjestelmän tehdessä laskun tietojen syötön. Suositeltu asetus on Kyllä, jos tietojen syötössä ei ole ongelmia. Automaattisten päivityksen poistaminen käytöstä voi parantaa järjestelmän suorituskykyä, koska laskujen täsmäytyksen tarkistus ohitetaan tietojen syötön aikana. Jos tämän kohdan arvoksi on määritetty Ei, tietojen syöttäjän on päivitettävä laskun täsmäytyksen tila manuaalisesti, jotta laskun täsmäytyksen tarkistustulokset näkyvät.  
4. Ota käyttöön Laskusummien täsmäytys -osan laajennus.
5. Valitse Täsmäytä laskusummat -valintaruutu tai poista sen valinta, kun haluat täsmäyttää toteutuneet laskusummat odotettujen summien kanssa.
    * Määritä, näkyykö kuvake, jos ristiriita laskua kohdistettaessa ylittää nettoyksikköhinnan toleranssin. Voit valita, että kuvake voidaan näyttää, kun positiivinen ristiriita ylittää toleranssin, tai kun joko positiivinen tai negatiivinen ristiriita ylittää toleranssin.  
    * Toleranssi on esimerkiksi 5 prosenttia ja ostotilauksen laskun kokonaissumma on 100,00. Tämän vuoksi hintavastaavuuden kuvake näytetään, jos laskun kokonaissumma ylittää 105,00. Jos valitset Onko suurempi tai pienempi kuin toleranssi -vaihtoehdon, kuvake näkyy myös, jos laskun summa on pienempi kuin 95,00.  
6. Syötä Laskusummien toleranssiprosentti -kenttään numero.
7. Ota käyttöön Hinnan ja määrän täsmäytys -osan laajennus.
    * Valitse Rivien vastaavuuskäytäntö -kentässä arvo, jota käytät oletusarvon mukaisena käytäntönä yritykselle, jonka kanssa työskentelet. Ei pakollinen -arvo tarkoittaa, että yksittäisistä laskurivien hinnoista ostotilauksen hinnoiksi- tai laskujen määristä pakkausluettelon määriksi -tarkistus ei ole pakollinen. Kaksisuuntainen-arvo tarkoittaa, että laskurivien tarkistus on pakollinen, mutta vain ostotilaus ja toimittajan laskuasiakirjat ovat mukana tarkistuksessa. Tuotteen vastaanottoa ei oteta huomioon täsmäytysten tarkistuksissa. Kolmisuuntainen-arvo tarkoittaa, että laskun nettoyksikköhintaa verrataan ostotilauksen nettoyksikköhintaan ja vastaavaa tuotteen vastaanoton määrää verrataan laskun määrään.  
    * Jos käytössä on rivin kaksi- tai kolmisuuntainen vastaavuuskäytäntö, voit määrittää Nimikkeen hintatoleranssi -sivulla yritykselle, nimikkeille ja toimittajille hintatoleranssin prosenttiosuudet. Kun toimittajan laskuja verrataan ostotilaustietoihin, järjestelmä etsii sovellettavaa hintatoleranssin prosenttia.  
8. Valitse vaihtoehto Rivien vastaavuuskäytäntö -kentässä.
    * Voit sallia eritasoisen täsmäytyksen käytettäväksi nimikkeelle, toimittajalle, toimittajan ja nimikkeen yhdistelmällä tai ostotilausriville, valitse arvo Salli vastaavuuskäytännön ohitus -kentässä. Yritysrivin yhteensopivuuskäytännön ohittamisesta tietyn toimittajan, nimikkeen tai toimittajan ja nimikkeen yhdistelmän kohdalla on Vastaavuusmenetelmä-sivulla.  
    * Voit täsmäyttää laskujen rivinimikkeiden kokonaissummat valitsemalla arvo Täsmäytä kokonaishinnat -kentässä. Tällainen täsmäytys on hyödyllistä silloin, kun toimittaja lähettää useita samaa ostotilausriviä koskevia laskuja. Voit verrata laskun kunkin rivin nettosummien ja kaikkien odottavien ja aiemmin kirjattujen laskurivien hintatietoja vastaavan ostotilausrivin nettosummaan.  
9. Valitse vaihtoehto Täsmäytä kokonaishinnat -kentässä.
10. Syötä Ostohinnan kokonaistoleranssi -kenttään numero.
11. Ota käyttöön Kulujen täsmäytys -osan laajennus.
12. Vertaa todellisia veloituksia odotettuihin kuluihin ostotilauksen tietoihin perustuen valitsemalla Täsmäytä kulut -valintaruutu.
13. Sulje sivu.


