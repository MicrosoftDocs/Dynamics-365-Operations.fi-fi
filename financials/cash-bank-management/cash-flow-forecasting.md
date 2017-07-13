---
title: Kassavirtaennusteet
description: "Tässä ohjeaiheessa on kassavirran ennusteprosessin yleiskatsaus. Siinä kerrotaan myös kassavirtaennusten integroinnista muihin järjestelmän moduuleihin."
author: saraschi
manager: AnnBe
ms.date: 05/15/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.search.scope: Core, Operations, UnifiedOperations
ms.search.region: Global
ms.author: sarasch
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.translationtype: Human Translation
ms.sourcegitcommit: 3abf4b151b177095b71d44e9a6c9fd8541eaa64e
ms.openlocfilehash: a8ccd99431178c3cb4e73e7cd199de8e0845d716
ms.contentlocale: fi-fi
ms.lasthandoff: 06/14/2017


---

# Kassavirtaennusteet
<a id="cash-flow-forecasting" class="xliff"></a>

[!include[banner](../includes/banner.md)]

Voit analysoida tulevaa kassavirtaa ja valuuttavaatimuksia kassavirran ennustetyökaluilla. Voit tällä tavoin arvioida yrityksen käteisvarojen tarvetta tulevaisuudessa. Sinun on tehtävä seuraavat tehtävät kassavirtaennustetta varten:

- Kaikkien rahatilien tunnistaminen ja luettelointi. Rahatilit ovat yrityksen käteistilejä tai käteisvaroja vastaavia tilejä.
- Määritä yrityksen rahatileihin vaikuttavien tapahtumaennusteiden toiminta.

Kun nämä tehtävät on tehty, voit laskea ja analysoida kassavirran ja tulevien valuuttatarpeiden ennusteet.

## Kassavirtaennusteen integrointi
<a id="cash-flow-forecasting-integration" class="xliff"></a>

Kassavirtaennuste voidaan integroida kirjanpitoon, ostoreskontraan, myyntireskontraan budjetointiin ja inventoinnin- ja varastonhallintaan. Ennusteprosessi käyttää järjestelmään vietyjä tapahtumatietoja. Laskentaprosessi puolestaan ennustaa kunkin tapahtuman odotetun käteisvaikutuksen. Seuraavat tapahtumatyypit otetaan huomioon kassavirtaa laskettaessa:

- **Myyntitilaukset** – toistaiseksi laskuttamattomat, fyysisiin tai taloudellisiin myynteihin johtavat myyntitilaukset.
- **Ostotilaukset** – toistaiseksi laskuttamattomat, fyysisiin tai taloudellisiin ostoihin johtavat ostotilaukset.
- **Myyntireskontra** – avoimet asiakastapahtumat (laskut, joita ei ole vielä maksettu).
- **Ostoreskontra** – avoimet toimittajatapahtumat (laskut, joita ei ole vielä maksettu).
- **Kirjanpitotapahtumat** – tapahtumat, joissa määritetään tulevaisuudessa tapahtuva kirjaus.
- **Budjettirekisterimerkinnät** – kassavirtaennusteille valitut budjettirekisterimerkinnät.
- **Kysynnän ennusteet** – kassavirtaennusteille valitut varastoennustemallin rivit.
- **Tarjontaennusteet** – kassavirtaennusteille valitut varastoennustemallin rivit.

Vaikka projektinhallintaa ja kirjanpito eivät ole suoraan integroituja, projektitapahtumat voidaan sisällyttää monella tavalla kassavirtaennusteeseen. Kirjatut projektilaskut sisällytetään ennusteeseen avoimien asiakastapahtumien osana. Projektista peräisin olevat myynti- ja ostotilaukset sisällytetään ennusteeseen avoimina tilauksina sen jälkeen, kun ne on viety järjestelmään. Voit myös siirtää projektiennusteet kirjanpidon budjettimalliin. Tämä kirjanpidon budjettimalli sisällytetään sitten kassavirtaennusteeseen budjettirekisterimerkintöjen osana.

## Konfiguraatio
<a id="configuration" class="xliff"></a>

Voit määrittää kassaviran ennusteprosessin **Kassavirtaennusteen määritys** -sivulla. Voit määrittää tällä sivulla seurattavat rahatilit ja kunkin alueen oletusennustetoiminnot.

### Kirjanpito
<a id="general-ledger" class="xliff"></a>

Määritä ensin kassavirtaennusteen aikana seurattavat rahatilit. Yleensä nämä rahatilit ovat päätilejä, jotka on liitetty käteisvaroja vastaanottaviin ja maksaviin pankkitileihin. Valitse **Kassavirtaennusteen määritys** -sivun **Kirjanpito**-välilehdessä ennusteeseen sisällytettävät päätilit. Jos pankkitili on liitetty päätiliin **Pankkitili**-sivulla, se näkyy **Pankkitili**-kentässä.

Voit määrittää riippuvaisen kassavirtaennusteen päätilille, joka sisältää suoraan toisen pääpitotilin tapahtumiin liittyviä tapahtumia. Jokainen **Riippuvissa tileissä** -osassa lisäämäsi rivi luo kassavirtaennusteen summan riippuvaisessa päätilissä. Tämä summa on prosenttiosuus valitsemasi ensisijaisen päävirtatilin kassavirtasummista.

Määritä ensin **Päätili**-kentässä ensisijainen päätili, jossa tapahtumien odotetaan aluksi näkyvän. Määritä **Riippuvainen päätili** -kenttään tili, johon ensisijaisen päätilin ensimmäinen tapahtuma vaikuttaa. Määritä rivin muihin kenttiin sopivat arvot. Voit muuttaa **Prosenttia**-kentän arvon sen mukaan, miten ensisijainen päätili vaikuttaa riippuvaiseen päätiliin. Valitse myynti- tai ostoennusteeseen useimmille asiakkaille tai toimittajille tyypillinen **Maksuehto**-arvo. Määritä **Kirjaustyyppi** -kenttään kassavirtaennusteeseen liittyvä odotettu kirjaustyyppi.

### Ostoreskontra
<a id="accounts-payable" class="xliff"></a>

Voit laskea ostojen ennusteen **Kassavirtaennusteen määritys** -sivun **Ostoreskontra**-välilehden asetuksilla. Ennen ostoreskontran kassavirtaennusteen määrittämistä on määritettävä maksuehto, toimittajaryhmät ja toimittajan kirjausprofiilit.

Voit valita **Ostoennusteen oletusarvot** -osassa oletusarvoiset ostotoiminnot kassavirtaennustetta varten. Kolme kenttää määrittää käteisvarojen vaikutusajankohdan: **Toimituspäivän ja laskutuspäivän välinen aika**, **Maksuehto** ja **Laskun eräpäivän ja maksupäivän välinen aika**. Ennuste käyttää **Maksuehto**-kentän oletusasetusta vain, jos arvoa ei ole määritetty tapahtumassa. Maksuehdon avulla voi kuvata kuinka monta päivää prosessin kukin osa yleensä kestää.

**Maksujen rahatilien** kenttään määritetään maksuissa useimmiten käytettävä rahatili. **Summan prosenttiosuus, joka kohdistetaan kassavirtaennusteeseen** -kenttään määritetään, käytetäänkö summien prosenttiosuutta ennusteen aikana. Jätä tämä kenttä tyhjäksi, jos ennusteessa käytetään tapahtumien koko summia.

Voit ohittaa **Laskun eräpäivän ja maksupäivän välinen aika** -kentän oletusasetuksen tietyille toimittajaryhmille. Ennuste käyttää **Ostoennusteen oletusarvot** -osan oletusarvoa, ellei tapahtuman toimittajaan liittyvälle toimittajaryhmälle ole määritetty toista arvoa. Voit ohittaa oletusarvon valitsemalla toimittajaryhmän ja määrittämällä sitten uuden arvon **Ostoaika**-kentässä.

Voit ohittaa tietyn toimittajan kirjausprofiilien **Rahatili**-kentän oletusarvon. Ennuste käyttää **Ostoennusteen oletusarvot** -osan oletusarvoa, ellei tapahtuman toimittajaan liittyvälle kirjausprofiilille ole määritetty toista rahatiliä. Voit ohittaa oletusarvon valitsemalla kirjausprofiilin ja määrittämällä sitten rahatilin, johon vaikutuksen odotetaan kohdistuvan.

### Myyntireskontra
<a id="accounts-receivable" class="xliff"></a>

Voit laskea myyntiennusteen **Kassavirtaennusteen määritys** -sivun **Myyntireskontra**-välilehden asetuksilla. Ennen myyntireskontran kassavirtaennusteen määrittämistä on määritettävä maksuehto, asiakasryhmät ja asiakkaiden kirjausprofiilit.

Voit valita **Myyntiennusteen oletusarvot** -osassa oletusarvoiset myyntitoiminnot kassavirtaennustetta varten. Kolme kenttää määrittää käteisvarojen vaikutusajankohdan: **Lähetyspäivän ja laskutuspäivän välinen aika**, **Maksuehto** ja **Laskun eräpäivän ja maksupäivän välinen aika**. Ennuste käyttää **Maksuehto**-kentän oletusasetusta vain, jos arvoa ei ole määritetty tapahtumassa. Maksuehdon avulla voi kuvata kuinka monta päivää prosessin kukin osa yleensä kestää. 

**Maksujen rahatilien** kenttään määritetään maksuissa useimmiten käytettävä rahatili. **Summan prosenttiosuus, joka kohdistetaan kassavirtaennusteeseen** -kenttään määritetään, käytetäänkö summien prosenttiosuutta ennusteen aikana. Jätä tämä kenttä tyhjäksi, jos ennusteessa käytetään tapahtumien koko summia.

Voit ohittaa **Laskun eräpäivän ja maksupäivän välinen aika** -kentän oletusasetuksen tietyille asiakasryhmille. Ennuste käyttää **Myyntiennusteen oletusarvot** -osan oletusarvoa, ellei tapahtuman asiakkaaseen liittyvälle asiakasryhmälle ole määritetty toista arvoa. Voit ohittaa oletusarvon valitsemalla asiakasryhmän ja määrittämällä sitten uuden arvon **Myyntiaika**-kentässä.

Voit ohittaa tietyn asiakkaan kirjausprofiilien **Rahatili**-kentän oletusarvon. Ennuste käyttää **Myyntiennusteen oletusarvot** -osan oletusarvoa, ellei tapahtuman asiakkaaseen liittyvälle kirjausprofiilille ole määritetty toista rahatiliä. Voit ohittaa oletusarvon valitsemalla kirjausprofiilin ja määrittämällä sitten rahatilin, johon vaikutuksen odotetaan kohdistuvan.

### Budjetointi
<a id="budgeting" class="xliff"></a>

Budjettimalleista luodut budjetit voidaan sisällyttää kassavirtaennusteisiin. Valitse **Kassavirtaennusteen määritys** -sivun **Budjetointi**-välilehdessä ennusteeseen sisällytettävät budjettimallit. Uudet budjettirekisterimerkinnät sisältyvät oletusarvoisesti ennusteisiin sen jälkeen, kun budjettimalli on otettu käyttöön kassavirtaennusteessa. Kassavirtaennusteen sisällyttäminen voidaan ohittaa yksittäisissä budjettirekisterimerkinnöissä.

### Inventoinnin- ja varastonhallinta
<a id="inventory-management" class="xliff"></a>

Varaston kysynnän ja tarjonnan ennusteet voidaan sisällyttää kassavirtaennusteisiin. Valitse **Kassavirtaennusteen määritys** -sivun **Inventoinnin- ja varastonhallinta**-välilehdessä kassavirtaennusteeseen sisällytettävät ennustemallit. Kassavirtaennusteen sisällyttäminen voidaan ohittaa yksittäisillä kysynnän ja tarjonnan ennusteriveillä.

### Laskelma
<a id="calculation" class="xliff"></a>

Kassavirran laskentaprosessin on suoritettava ennen kassavirtaennusteen analyysien tarkastelemista. Laskentaprosessi projisoi vietyjen tapahtumien tulevat vaikutukset käteisvaroihin.

Laske kassavirtaennuste **Laske kassavirtaennusteet** -sivulla. Voit laskea koko kassavirtaennusteen tai kasvavan kassavirtaennusteen. 

- Voit poistaa kaikki kassavirtaennusten tapahtumat ja laskea uudelleen valitsemalla **Kassavirtaennusteen laskentamenetelmä** -kentässä **Yhteensä**. Tämän menetelmän käyttö on suositeltavaa, jos et ole päivittänyt kassavirtaennusteita pitkään aikaan. 
- Voit päivittä aiemmin luodun kassavirran tiedot vain uusilla tapahtumilla valitsemalla **Kassavirtaennusteen laskentamenetelmä** -kentässä **Uusi**. Sivulla näkyy ajankohta, jolloin kassavirtalaskenta viimeksi suoritettiin.

Voit käyttää kassavirtaennusteen laatimiseen myös eräkäsittelyä. Voit varmistaa, että ennusteanalytiikka päivitetään säännöllisesti määrittämällä kassavirtaennusteen laskennalle toistuvan eräkäsittelyn.

### Raportointi
<a id="reporting" class="xliff"></a>

Analyyttinen raportointi edellyttää, että liitetyt yksikkötiedot on päivitettävä kassavirtaennusteen laskemisen jälkeen. Valitse **Yksikkösäilö**-säilö sivulla **LedgerCovLiquidityMeasurement-kooste**-mitta ja valitse sitten **Päivitä**.

Kassavirtaennusteen tietoja on kahdessa työtilassa. Toisessa työtilassa on kaikkien yritysten tiedot ja toisessa on vain nykyisen yrityksen tiedot.

Kaikkien yritysten työntilan käyttöä hallitaan **Näytä kassavirta – kaikkien yritysten työtila** -velvollisuuden kautta. **Kassayhteenveto – kaikki yritykset** -työtila on oletusarvoisesti kaikkien seuraavien roolien käytettävissä:

- Pääjohtaja
- Talousjohtaja
- Laskentatoimen controller

Nykyisen yrityksen työntilan käyttöä hallitaan **Näytä kassavirta – nykyinen yrityksen työtila** -velvollisuuden kautta. **Kassayhteenveto – nykyinen yrityksen** työtila on oletusarvoisesti kaikkien seuraavien roolien käytettävissä:

- Kirjanpitäjä
- Laskentapäällikkö
- Taloushallintopäällikkö
- Ostoreskontrapäällikkö
- Myyntireskontrapäällikkö

**Kassayhteenveto – kaikki yritykset** -työtila näyttää kassavirtaennusten analytiikan järjestelmän valuuttana. Analytiikassa käytettävä järjestelmän valuutta ja järjestelmän vaihtokurssityyppi määritetään **Järjestelmän parametrit** -sivulla. Työtilassa on kaikkien yritysten kassavirtaennusteiden ja pankkitilin saldojen yhteenveto. Tilikartan saapuvat ja lähtevät kassavirrat on yhteenveto käteisvarojen tulevista siirroista ja saldoista järjestelmän valuuttana. Siinä on myös tarkkoja tietoja ennakoiduista tapahtumista. Näkyvissä on myös valuuttasaldojen ennuste.

**Kassayhteenveto – nykyinen yrityksen** työtilassa kassavirtaennusteen analytiikka näkyy yrityksen määrittämänä kirjanpitovaluuttana. Analytiikassa käytettävä kirjanpitovaluutta määritetään **Kirjanpito**-sivulla. Työtilassa on nykyisen yrityksen kassavirtaennusteiden ja pankkitilin saldojen yhteenveto. Tilikartan saapuvat ja lähtevät kassavirrat on yhteenveto käteisvarojen tulevista siirroista ja saldoista kirjanpitovaluuttana. Siinä on myös tarkkoja tietoja ennakoiduista tapahtumista. Näkyvissä on myös valuuttasaldojen ennuste.

Lisätietoja kassavirtaennusteiden analytiikasta on ohjeaiheessa Kassayhteenveto – Power BI -sisältö.

Voit tarkastella myös tiettyjen tilien, tilausten ja nimikkeiden kassavirtaennustetietoja seuraavilla sivuilla:

- **Pääkirja**: voit tarkastella valitun päätilin tulevia kassavirtoja valitsemalla **Kassavirtaennusteet**.
- **Kaikki myyntitilaukset**: voit tarkastella valitun myyntitilauksen ennakoitua käteisvaikutusta valitsemalla **Lasku**-välilehdessä **Kassavirtaennusteet**.
- **Kaikki ostotilaukset**: voit tarkastella valitun ostotilauksen ennakoitua käteisvaikutusta valitsemalla **Lasku**-välilehdessä **Kassavirtaennusteet**.
- **Tarjontaennuste**: voit tarkastella valitun nimikkeen tarjontaennusteeseen liitettyjä kassavirtoja valitsemalla **Kassavirtaennusteet**.
- **Kysynnän ennuste**: voit tarkastella valitun nimikkeen kysynnän ennusteeseen liitettyjä kassavirtoja valitsemalla **Kassavirtaennusteet**.


