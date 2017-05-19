---
title: Projektiennusteet ja -budjetit
description: 
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: ForecastModel, ProjYearEndProcess
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 23501
ms.assetid: 4e6d1384-19a2-4232-b3f3-d2590c218bd7
ms.search.region: Global
ms.author: kfend
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: 06c806da29c8c925bfcea2e8b5045f9bc7043b48
ms.contentlocale: fi-fi
ms.lasthandoff: 04/25/2017


---

# <a name="project-forecasts-and-budgets"></a>Projektiennusteet ja -budjetit

[!include[banner](../includes/banner.md)]




Microsoft Dynamics 365 for Operations -järjestelmässä projekteja voidaan hallita ja kontrolloida kahdella tavalla: projektiennusteilla ja projektibudjeteilla. 

Käytä projektiennusteita, jos organisaatiossasi on operatiivinen perspektiivi ja jos se keskittyy tuottoihin ja kustannuksiin, jotka ovat peräisin tietyistä tapahtumista. Käytä projektibudjetointia, jos organisaatiosi keskittyy enemmän taloushallinnon summiin. 

Sekä projektiennusteet että projektibudjetit käyttävät ennustemalleja arvioitujen tapahtumasummien säilyttämiseen. 

Kummallakin menetelmällä on omat etunsa. Ota seuraavat seikat huomioon, kun valitse menetelmän organisaatioon.

|                           |                                                                                                                                                                                                                                                         |                                                                                                                                                                         |
|---------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|                           | **Projektin ennusteet**                                                                                                                                                                                                                                 | **Projektin budjetointi**                                                                                                                                                   |
| **Kauden kohdistus**     | Tapahtumia ei voi kohdistaa tarkasti tilikaudelle. Ennuste ja ennusteen hallinta perustuvat projektin elinkaareen. Koska ennusteet perustuvat tiettyyn päivämäärään, kausi on johdettava päivämäärästä. | Voit kohdistaa tapahtumat koko projektin tai tilikauden ajalle. Jos kohdistus tehdään koko kaudelle, käyttämättömät summat voidaan siirtää seuraavalle tilikaudelle. |
| **Tapahtumien tarkastelu**  | Voit tarkastella tapahtumia ennustelomakkeissa, joissa koko yrityksen ja kaikkien projektien ennusteet ovat näkyvissä hierarkiasta riippumatta. Tiedot on suodatettava, jos on haluat keskittyä tiettyyn projektiin.                                       | Voit tarkastella yksittäisen projektihierarkian budjetoituja tapahtumia. Niinpä voit tarkastella pääprojektin tai sen aliprojektien tapahtumatietoja.                 |
| **Tapahtumamuuttujat** | Voit käyttää ennustetapahtumien antamisessa kaikkia todellisen tapahtuman määritteitä. Tämä mahdollistaa tarkkojen tietojen käytön ennusteissa. Voit esimerkiksi antaa määritä, työntekijöitä, nimikkeitä ja riviominaisuuksia koskevia tietoja.         | Voit käyttää budjetin tietojen antamiseen vain summia, luokkia ja tehtäviä.                                                                                    |
| **Suojaus**              | Ennusteet perustuvat tapahtumiin, jotka annat ennustelomakkeissa. Siihen ei sisälly prosessinhallinnan mekanismia. Kaikki työntekijät, joilla on ennustelomakkeen käyttöoikeudet, voivat muokata tietoja hyväksyntää tarvitsematta.                                        | Budjetoinnissa käytetään työnkulkujärjestelmää, joka mahdollistaa muutostenhallinnan ja versiohistorian säilyttämisen.                                                       |
| **Merkintätyypit**           | Ennustetapahtumamerkinnät perustuvat yksiköiden määrään sekä kustannuksiin ja myyntiyksikön hintoihin.                                                                                                                                                       | Budjetin tiedot perustuvat summiin, jotka on jaettu tuloihin ja menoihin.                                                                                        |
| **Ennustemallit**       | Koska jokainen ennuste on liitettävä malliin, voit luoda useita ennustemalleja sekä määrittää alimalleja.                                                                                                                               | Projektin budjetointi rajoittaa budjetointiin käytettäviä ennustemalleja. Vähäinen ennustemallien määrä parantaa ennusteiden yhdenmukaisuutta.                           |
| **Kustannusten ylitykset**         | Voit vain sallia tai estää kustannuksen ylityksen aiheuttavien tapahtumien merkinnän.                                                                                                                                                                | Projektin budjetoinnissa käyttäjillä on muita hallintavaihtoehtoja. Voit sallia varoitukset ja ylitykset.                                                                   |
| **Seuranta**               | Ennustetta seurataan ennustevähennysten avulla. Toteutuneet summat vähennetään ennustetapahtuman saldoista ilman kirjausketjua. Tämä voi vaikeuttaa sen seurantaa, missä toteutuneiden tapahtumat tapahtuivat.                   | Projektibudjetin hallinnassa todelliset summat vähennetään jäljellä olevan budjetin summista. Tämä mahdollistaa selkeämmän kirjausketjun.                                   |

## <a name="project-forecasts"></a>Projektiennusteet
Kun käytät projektin ennustetta, voit kirjoittaa ennustetapahtumia ennustelomakkeilla kullekin tapahtumatyypille. Jokaista todelliselle tapahtumalle käytettävissä olevaa määritettä voidaan käyttää ennustetapahtumaan, kuten rivin kannattavuutta, rivin määritteitä, työntekijöitä tai kuvauksia. Voit myös ennakoida, kuinka kauan kustannuksen syntymisen jälkeen laskutat sen asiakkaalta. 

Projektiennustetapahtumat perustuvat yksiköihin ja summiin. 

Jokainen projektiennuste on liitettävä ennustemalliin. Kun annat ennustetapahtuman, ennustemallia ehdotetaan automaattisesti. Ennustemalli toimii ennustetapahtumien säilönä. 

Voit määrittää ennustemalleja mallin alimalleina. Niinpä voit tehdä ennusteita alueen, aikajakson tai osaston mukaan. Voit kopioida mallin ennustetapahtumat, jos haluat luoda uuden mallin. Voit myös siirtää tapahtumat kirjanpitoon. Ennusteen ja mallin välillä on yksi yhteen -suhde, joten kukin ennustemalli muodostaa erillisen budjetin projektille. 

Ennustemallit voivat käyttää projektihallinnan mekanismeja. Ennustevähennyksellä todelliset tapahtumat vähentävät ennustetapahtuman saldoja. Kuitenkin, koska ennustevähennystä käytetään hierarkian ylimpään projektin, se sisältää vain rajoitetun muutosennusteen. Esimerkiksi jos työntekijä on liitetty aliprojektiin, työntekijän todelliset tapahtumat kirjataan pääprojektiin. Tämä voi vaikeuttaa muutosten seurantaa, koska voi olla vaikea määrittää, mikä tapahtuma aiheutti ennustemäärän vähenemisen ja missä aliprojektissa se tapahtui. Niinpä ennustevähennystä varten on hyvä luoda kopio ennustemallista. Voit tarkastella raporteista, mitä alun perin ennustettiin. 

Voit tarkistaa, kopioida, poistaa tai siirtää projektiennusteita kirjanpitobudjettiin. Prosessinhallintaa ei kuitenkaan ole. Kaikki työntekijät, joilla on ennustelomakkeen käyttöoikeus, voivat tehdä muokkauksia ilman tarkistusta.

-   **Muuta * – Voit muuttaa ennustetapahtumaan samoilla lomakkeilla, joihin alkuperäiset merkinnät on tehty.
-   **Kopioi tai poista** – Kun kopioit ennustetapahtumia, yhden ennustemallin tapahtumarivit kopioidaan toiseen ennustemalliin. Kun poistat ennusteen, poistat ennustemallin ennustetapahtumat. Jos haluat rajoittaa kopioitavia tai rajoitettavia ennustetapahtumia, valitse tietyt tapahtumatyypit ja päivämäärät. Tällä tavoin voit kopioida tai poistaa vain tiettyjä ennusteen osia.
-   **Siirto** – Kun siirrät projektiennusteen kirjanpitobudjettiin, siirrät ennustemallin ennustetapahtumat kirjanpitobudjettiin. Voit korvata siirrettävällä projektiennusteella minkä tahansa kirjanpitobudjettiin aiemmin siirretyn tapahtuman.

## <a name="project-budgets"></a>Projektibudjetit
Projektin budjetointi on yksinkertaisempaa kuin ennusteet, vaikka siihen integroidaan ennustemallit. Alkuperäiset budjetin tiedot ja muutokset ilmoitetaan yhdellä lomakkeella, jossa voi tehdä vain summaan, luokkaan tai tehtävään perustuvia ennusteita. 

Projektin budjetoinnissa kaikki alkuperäisen budjetit ja muutokset on lähettävä projektityönkulkuun hyväksyttäväksi. Työnkulku parantaa prosessin hallintaa ja luo muutoshistoriatietueen. 

Projektin budjetointi muistuttaa kirjanpitobudjetointi, mutta sen määrittäminen on helpompaa ja nopeampaa. Monia kirjanpitobudjetoinnin vaihtoehtoja, kuten numerosarjoja tai valuuttaa, ei tarvitse määrittää erikseen projekteja varten.

Projektibudjetit liitetään automaattisesti kahteen ennustemalliin, joista toinen on alkuperäiselle budjetille ja toinen jäljellä olevalle budjetille. Tämän vuoksi ennustemalleihin perustuvat raportit voivat käyttää budjetin tietoja. Kun projektibudjetti on sidottu, järjestelmä luo raportointiin ja hallintaan käytettäviä ennustetapahtumia liitettyjen mallien perusteella.

## <a name="forecast-models"></a>Ennustemallit
Ennustemalleissa on yksitasoinen hierarkia. Tämä tarkoittaa, että jokaiseen projektiennusteeseen on liitettävä yksi ennustemalli.

Jos käytät projektin ennusteita, voit määrittää mallit alimalleiksi. Voit sitten luoda ennusteita osaston, ajanjakson tai alueen mukaan. Voit esimerkiksi luoda vuodelle ennustemallin ja sitten alimallit alueelliset ennusteet (etelä, pohjoinen, länsi ja itä), jotka aluepäälliköt lähettävät. Valitsemalla eri asetuksia voit tarkastella käytettävissä olevien raporttien tietoja koko ennusten tai alimallin mukaan.




