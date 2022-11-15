---
title: Varmuusmarginaalit
description: Tässä artikkelissa kuvataan, kuinka varmuusmarginaalit toimivat pääsuunnittelun aikana.
author: t-benebo
ms.date: 08/09/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: benebotg
ms.search.validFrom: 2020-9-14
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: 87b38276a2723374969a67c5413dde15537d04ec
ms.sourcegitcommit: 491ab9ae2b6ed991b4eb0317e396fef542d3a21b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/03/2022
ms.locfileid: "9740438"
---
# <a name="safety-margins"></a>Varmuusmarginaalit

[!include [banner](../../includes/banner.md)]

Tässä artikkelissa kuvataan, kuinka varmuusmarginaalit toimivat pääsuunnittelun aikana.

## <a name="safety-margins-overview"></a>Varmuusmarginaalien yleiskatsaus

Varmuusmarginaalien tarkoitus on mahdollistaa sellaisen asetuksen käyttäminen, joka mahdollistaa normaalin läpimenoajan lisäksi puskuriajan. Jos esimerkiksi materiaalin pakkaus on purettava tai materiaali on tarkistettava toimittajalta saapumisen jälkeen et voi vain lisätä aikaa oston läpimenoaikaan, koska tällöin lisäaika annetaan toimittajalle. Tässä esimerkissä vastaanottomarginaalia voidaan käyttää varmistettaessa toimittajan aikainen toimitus. Tämä menetelmä määrittää puskuriajan niin, että tavarat voidaan käsitellä sisäisesti.

Varmuusmarginaalityyppejä on seuraavat kolme:

- **Uudelleentilausmarginaali** – Puskuriaika toimitustilauksen asettamiselle
- **Vastaanottomarginaali** – Puskuriaika saapuvan toimituksen käsittelylle
- **Toimitusmarginaali** – Puskuriaika lähetysten käsittelylle

Seuraavassa kuvassa näkyy, miten näitä varmuusmarginaaleja käytetään ajan kuluessa.

![Varmuusmarginaalit.](media/safety-margins-1.png)

Kaikki marginaalit määritetään päivinä. Oletusarvo, joka on *0* (nolla), osoittaa, että marginaalia ei ole käytetty. Jos määrität useita marginaaleja, ne kaikki lisätään kokonaisaikaan tarjonnan *tilauspäivämäärästä* kysynnän *tarvepäivämäärään*. Ajatellaan, että määrityksellä ei ole läpimenoaikaa, ja jokaisen kolmen marginaalityypin arvoksi on määritetty yksi päivä. Tässä tapauksessa tarjonnan tilauspäivämäärän ja kysynnän tarvepäivämäärän välillä on kolme päivää. Jos siis tilauspäivämäärä on 1.7., tarvepäivämäärän tulisi olla 4.7.

### <a name="receipt-margin"></a>Vastaanottomarginaali

Vastaanottomarginaali on todennäköisesti eniten käytetty kolmesta varmuusmarginaalista. Sitä käytetään *toimituspäivämäärässä* ja *tarvepäivämäärästä* taaksepäin. Toisin sanoen tuotteille on annettava tietty määrä vastaanottomarginaalipäiviä ennen ajankohtaa, jolloin ne tarvitaan.

Seuraavassa kuvassa näkyy vastaanottomarginaali.

![Vastaanottomarginaali.](media/safety-margins-2.png)

Vastaanottomarginaalia käytetään yleensä puskurina. Se varmistaa ajan varastoinnin rekisteröintiä tai muita aikaa vieviä prosesseja varten. Niitä ei tallenneta yleisen läpimenoajan osana järjestelmässä. Ostojen osalta eräs etu on se, että ostotilauksen *toimituspäivämäärää* siirretään eteenpäin vastaavasti. Jos lisäät läpimenoaikaa varmuusmarginaalin käyttämisen sijaan, toimittaja voi yhä pyytää viime hetken toimituksia.

Ota huomioon, että vastaanottomarginaali ei muuta tarjonnan *tarvepäivämäärää*. Tämän vuoksi vastaanottomarginaali ei ole suoraan nähtävissä, kun kysynnän ja tarjonnan tarvepäivämääriä vertaillaan (esimerkiksi **Nettotarpeet**-sivulla). Jos esimerkiksi vastaanottomarginaaliksi on asetettu neljä päivää ja ostotilausriville on suunniteltu vastaanotto kuukauden 15. päivälle, pääsuunnittelu laskee oikaistuksi vastaanottopäiväksi kuukauden 19. päivän.

Huomaa, että vastaanottomarginaalia ei käytetä, kun käytettävissä olevaa varastoa käytetään tarjontana. Kaikkien käytettävissä olevien varastojen oletetaan olevan saatavilla välittömästi riippumatta siitä, milloin ne on vastaanotettu.

### <a name="reorder-margin"></a>Uudelleentilausmarginaali

Seuraavassa kuvassa näkyy uudelleentilausmarginaali.

![Uudelleentilausmarginaali.](media/safety-margins-3.png)

Uudelleentilausmarginaali lisätään ennen nimikkeen läpimenoaikaa kaikille suunnitelluille tilauksille pääsuunnittelun aikana. Näin se varmistaa, että toimitustilauksen asettamiselle on käytettävissä lisäaikaa. Tätä marginaalia käytetään yleensä puskurina, jotta voidaan varmistaa riittävä aika toimitustilausten luonnin aikana tarvittaville hyväksymisprosesseille ja muille sisäisille prosesseille. Uusintatilausmarginaali asetetaan toimituksen *tilauspäivämäärän* ja *alkupäivämäärän* välille.

### <a name="issue-margin"></a>Toimitusmarginaali

Seuraavassa kuvassa näkyy toimitusmarginaali.

![Toimitusmarginaali.](media/safety-margins-4.png)

Toimitusmarginaali vähennetään kysynnän tarvepäivämäärästä pääsuunnittelun aikana. Sen avulla voit varmistaa, että käyttäjällä on aikaa reagoida saapuviin kysyntätilauksiin ja lähettää ne. Tätä marginaalia käytetään yleensä puskurina, joka varmistaa ajan lähetyksille ja liittyville lähteville varastoprosesseille.

Huomaa, että kun toimitusmarginaalia käytetään, siihen liittyvät tarjonnan ja kysynnän tarvepäivämäärät eivät vastaa toisiaan. Sen sijaan ne eroavat toimitusmarginaalin perusteella, koska toimitusmarginaali on lisätty tarjonnan *tarvepäivämäärän* ja kysynnän *tarvepäivämäärän* välille.

## <a name="set-up-safety-margins"></a>Varmuusmarginaalien määrittäminen

### <a name="turn-safety-margins-on-or-off"></a>Varmuusmarginaalien käyttöönotto tai käytöstäpoisto

Jos haluat käyttää tätä ominaisuutta, se on otettava käyttöön järjestelmässä. Supply Chain Managementin versiosta 10.0.29 alkaen tämä toiminto on pakollinen, eikä sitä voi poistaa käytöstä. Jos käytät vanhempaa versiota kuin 10.0.29, järjestelmänvalvojat voivat ottaa tämän toiminnon käyttöön tai pois käytöstä hakemalla *Suunnittelun optimoinnin marginaalit* -toimintoa [Toimintojen hallinta](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) -työtilassa.

### <a name="define-safety-margins"></a>Varmuusmarginaalien määrittäminen

Varmuusmarginaaleilla on joustava määritys. Ne voidaan määrittää sekä *kattavuusryhmälle* että *pääsuunnitelmalle*. On tärkeää ymmärtää, että marginaalit lisätään toistensa päälle. Esimerkiksi kattavuusryhmän kahden päivän ja pääsuunnitelman kolmen päivän vastaanottomarginaalit lasketaan yhteen, joten vastaanottomarginaalien kokonaismäärä on viisi päivää.

Mahdollisuus määrittää pääsuunnitelman marginaali voi olla hyödyllinen, jos haluat simuloida pidemmät läpimenoajat tai tietyn suunnitelman epävarmuustekijät ilman, että päivän suunnitelmat muuttuvat.

#### <a name="coverage-group-safety-margins"></a>Kattavuusryhmän varmuusmarginaalit

Jos haluat käyttää varmuusmarginaalia kattavuusryhmässä, tee seuraavat toiminnot.

1. Siirry kohtaan **Pääsuunnittelu \> Määritys \> Kattavuusryhmät**.
1. Valitse haluamasi kattavuusryhmä luetteloruudusta.
1. Käytä **Muut**-pikavälilehden **Varmuusmarginaalit päivinä** -osassa seuraavia kenttiä pakollisten varmuusmarginaalien (päivät) määrittämisessä:

    - Tarvepäivään lisätty vastaanottomarginaali
    - Tarvepäivästä vähennetty toimitusmarginaali
    - Nimikkeen läpimenoaikaan lisätty uudelleenjärjestyksen marginaali

#### <a name="master-plan-safety-margins"></a>Pääsuunnitelman varmuusmarginaalit

Jos haluat käyttää varmuusmarginaalia pääsuunnitelmassa, tee seuraavat toiminnot.

1. Siirry kohtaan **Pääsuunnittelu \> Määritykset \> Suunnitelmat \> Pääsuunnitelmat**.
1. Valitse haluamasi pääsuunnitelma luetteloruudusta.
1. Käytä **Varmuusmarginaalit päivinä** -pikavälilehdessä seuraavia kenttiä, jos haluat määrittää pakolliset varmuusmarginaalit (päivinä):

    - Tarvepäivään lisätty vastaanottomarginaali
    - Tarvepäivästä vähennetty toimitusmarginaali
    - Nimikkeen läpimenoaikaan lisätty uudelleenjärjestyksen marginaali

### <a name="define-whether-calculations-are-based-on-calendar-days-or-work-days"></a>Määritä, perustuvatko laskelmat kalenteripäiviin vai työpäiviin

Voit määrittää kaikki varmuusmarginaalit niin, että ne lasketaan joko kalenteripäivien tai työpäivien perusteella.

1. Valitse **Pääsuunnittelu \> Määritys \> Pääsuunnittelun parametrit**.
1. Määritä **Yleistä**-välilehden **Varmuusmarginaalit päivinä** -osassa **Työpäivät**-asetukseksi *Kyllä*, jos marginaalit lasketaan työpäivien perusteella. Määritä asetukseksi *Ei*, jos marginaalit lasketaan kalenteripäivien perusteella.

Ajatellaan, että kalenteri on auki maanantaista perjantaihin ja suljettu lauantaina ja sunnuntaina. Jos vastaanottomarginaali on yksi päivä, tarpepäivämäärä maanantaina tarkoittaa edellisen perjantain toimituspäivää, koska lauantai ja sunnuntai eivät ole työpäiviä.

Työpäivien määrittämisessä käytettävä kalenteri riippuu määritys- ja tarjontatyypistä. Kattavuusryhmän, varaston ja toimittajan kalenterit voivat ohjata sitä.

> [!NOTE]
> Jos *varasto* ei ole osa kattavuusdimensiota (eli suunnittelu perustuu vain *toimipaikkaan*), varaston kalenteria ei käytetä.

Järjestelmä voi käsitellä asetusta, jossa on määritetty vähintään yksi kalenteri. Seuraavat aliosat kuvaavat mahdollisia yhdistelmiä, joita voidaan käyttää tuloksen hallinnassa.

#### <a name="calendar-that-is-used-for-the-duration"></a>Kestossa käytettävä kalenteri

Määritetyt kalenterit ohjaavat todellista kokonaisläpimenoaikaa kalenteripäivinä tarjonnan tilauspäivämäärästä kysynnän tarvepäivämäärään. Käytetään seuraavaa kalenterin priorisointia:

- **Oston läpimenoaika** – Vain kattavuusryhmän kalenteri otetaan huomioon.
- **Vastaanottomarginaali** – Kattavuusryhmän kalenteria käytetään, jos se on määritetty. Muussa tapauksessa käytetään varaston kalenteria.
- **Toimitusmarginaali** – Kattavuusryhmän kalenteria käytetään, jos se on määritetty. Muussa tapauksessa käytetään varaston kalenteria.
- **Tilausmarginaali** – Vain kattavuusryhmän kalenteri otetaan huomioon.

#### <a name="calendar-that-is-used-for-the-final-date"></a>Lopullisessa päivämäärässä käytettävä kalenteri

Seuraavien sääntöjen avulla voit määrittää, voiko suunnittelumoduuli käyttää annettua päivämäärätyyppiä tiettynä päivänä:

- **Oston vastaanottopäivämäärä** – Toimittajan kalenteria käytetään, jos se on määritetty. Muussa tapauksessa käytetään kattavuusryhmän kalenteria, jos se on määritetty. Jos kumpaakaan näistä kalentereista ei ole määritetty, käytetään varaston kalenteria.
- **Siirron vastaanottopäivämäärä** – Kattavuusryhmän kalenteria käytetään, jos se on määritetty. Muussa tapauksessa käytetään varaston kalenteria.
- **Tuotannon vastaanottopäivämäärä** – Kattavuusryhmän kalenteria käytetään, jos se on määritetty. Muussa tapauksessa käytetään varaston kalenteria.
- **Kysynnän toimituksen avoin päivä** – Varaston kalenteria käytetään, jos se on määritetty. Muussa tapauksessa käytetään kattavuusryhmän kalenteria.
- **Tilauksen avoin päivä** – Käytetään kattavuusryhmän kalenterin ja toimittajan kalenterin yhdistelmää. Molempien kalenterien on oltava avoimia, jotta päivämäärää voidaan käyttää. Jos vain toinen kalentereista on määritetty, käytetään vain määritettyä kalenteria.

#### <a name="calendar-setup-overview-matrix"></a>Kalenterin asetusten yhteenvedon matriisi

Seuraavassa kuvassa on matriisi, jossa on yhteenveto siitä, mitä kalentereita käytetään varmuusmarginaalien laskemisessa. (Valitse kuva, josta haluat avata suuritarkkuuksisen version.) Seuraavien lyhenteiden ja värien avulla ilmaistaan, missä kukin kalenterityyppi määritetään:

- **Kattavuusryhmä:** Vihreä
- **Varasto:** Keltainen
- **Toimittaja:** Sininen

[![Kalenterin asetusten yhteenvedon matriisi.](media/safety-margins-calendar-matrix.png)](media/safety-margins-calendar-matrix-high.png)

## <a name="calculating-delays"></a>Viiveiden laskeminen

Kaikki varmuusmarginaalien kolme tyyppiä otetaan huomioon, kun järjestelmä määrittää tilauksen mahdollisen viivästymisen.

Esimerkiksi nimikkeen läpimenoaika on yksi päivä ja vastaanottomarginaali on kolme päivää. Tämän nimikkeen myyntitilaus vaaditaan tänään. Tässä tapauksessa viive lasketaan seuraavasti: *läpimenoaika* + *vastaanottomarginaali* = neljä päivää. Jos siis tänään on 14.8., neljän päivän viive tuottaa tulokseksi 18.8. Seuraavassa kuvassa on esimerkki tästä tapauksesta.

![Esimerkki viiveen laskennasta.](media/safety-margins-delays.png)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]