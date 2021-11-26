---
title: Kassavirtaennusteet
description: Tässä ohjeaiheessa on kassavirran ennusteprosessin yleiskatsaus. Siinä kerrotaan myös kassavirtaennusten integroinnista muihin järjestelmän moduuleihin.
author: panolte
ms.date: 11/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerCovParameters
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: 5ad3b2444f194f8324a309df32612a5377851995
ms.sourcegitcommit: 03fa7556840aa59f825697f6f9edeb58ea673fca
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/04/2021
ms.locfileid: "7752901"
---
# <a name="cash-flow-forecasting"></a>Kassavirtaennusteet

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Voit analysoida tulevaa kassavirtaa ja valuuttavaatimuksia kassavirran ennustetyökaluilla. Voit tällä tavoin arvioida yrityksen käteisvarojen tarvetta tulevaisuudessa. Sinun on tehtävä seuraavat tehtävät kassavirtaennustetta varten:

- Kaikkien rahatilien tunnistaminen ja luettelointi. Rahatilit ovat yrityksen käteistilejä tai käteisvaroja vastaavia tilejä.
- Määritä yrityksen rahatileihin vaikuttavien tapahtumaennusteiden toiminta.

Kun nämä tehtävät on tehty, voit laskea ja analysoida kassavirran ja tulevien valuuttatarpeiden ennusteet.

## <a name="cash-flow-forecasting-integration"></a>Kassavirtaennusteen integrointi

Kassavirtaennuste voidaan integroida kirjanpitoon, ostoreskontraan, myyntireskontraan budjetointiin ja inventoinnin- ja varastonhallintaan. Ennusteprosessi käyttää järjestelmään vietyjä tapahtumatietoja. Laskentaprosessi puolestaan ennustaa kunkin tapahtuman odotetun käteisvaikutuksen. Seuraavat tapahtumatyypit otetaan huomioon kassavirtaa laskettaessa:

- **Myyntitilaukset** – toistaiseksi laskuttamattomat, fyysisiin tai taloudellisiin myynteihin johtavat myyntitilaukset.
- **Ostotilaukset** – toistaiseksi laskuttamattomat, fyysisiin tai taloudellisiin ostoihin johtavat ostotilaukset.
- **Myyntireskontra** – avoimet asiakastapahtumat (laskut, joita ei ole vielä maksettu).
- **Ostoreskontra** – avoimet toimittajatapahtumat (laskut, joita ei ole vielä maksettu).
- **Kirjanpitotapahtumat** – tapahtumat, joissa määritetään tulevaisuudessa tapahtuva kirjaus.
- **Budjettirekisterimerkinnät** – kassavirtaennusteille valitut budjettirekisterimerkinnät.
- **Kysynnän ennusteet** – kassavirtaennusteille valitut varastoennustemallin rivit.
- **Tarjontaennusteet** – kassavirtaennusteille valitut varastoennustemallin rivit.
- **Projektiennusteet** – Projektinhallinta- ja kirjanpitoennusteet ennustemallin avulla.

## <a name="configuration"></a>Määritys

Voit määrittää kassaviran ennusteprosessin **Kassavirtaennusteen määritys** -sivulla. Voit määrittää tällä sivulla seurattavat rahatilit ja kunkin alueen oletusennustetoiminnot.

### <a name="general-ledger"></a>Kirjanpito

Määritä ensin kassavirtaennusteen aikana seurattavat rahatilit. Yleensä nämä rahatilit ovat päätilejä, jotka on liitetty käteisvaroja vastaanottaviin ja maksaviin pankkitileihin. Valitse **Kassavirtaennusteen määritys** -sivun **Kirjanpito**-välilehdessä ennusteeseen sisällytettävät päätilit. Jos pankkitili on liitetty päätiliin **Pankkitili**-sivulla, se näkyy **Pankkitili**-kentässä.

Voit määrittää riippuvaisen kassavirtaennusteen päätilille, joka sisältää suoraan toisen pääpitotilin tapahtumiin liittyviä tapahtumia. Jokainen **Riippuvissa tileissä** -osassa lisäämäsi rivi luo kassavirtaennusteen summan riippuvaisessa päätilissä. Tämä summa on prosenttiosuus valitsemasi ensisijaisen päävirtatilin kassavirtasummista.

Määritä ensin **Päätili**-kentässä ensisijainen päätili, jossa tapahtumien odotetaan aluksi näkyvän. Määritä **Riippuvainen päätili** -kenttään tili, johon ensisijaisen päätilin ensimmäinen tapahtuma vaikuttaa. Määritä rivin muihin kenttiin sopivat arvot. Voit muuttaa **Prosenttia**-kentän arvon sen mukaan, miten ensisijainen päätili vaikuttaa riippuvaiseen päätiliin. Valitse myynti- tai ostoennusteeseen useimmille asiakkaille tai toimittajille tyypillinen **Maksuehto**-arvo. Määritä **Kirjaustyyppi** -kenttään kassavirtaennusteeseen liittyvä odotettu kirjaustyyppi.

### <a name="accounts-payable"></a>Ostoreskontra

Voit laskea ostojen ennusteen **Kassavirtaennusteen määritys** -sivun **Ostoreskontra**-välilehden asetuksilla. Ennen ostoreskontran kassavirtaennusteen määrittämistä on määritettävä maksuehto, toimittajaryhmät ja toimittajan kirjausprofiilit.

Voit valita **Ostoennusteen oletusarvot** -osassa oletusarvoiset ostotoiminnot kassavirtaennustetta varten. Kolme kenttää määrittää käteisvarojen vaikutusajankohdan: **Toimituspäivän ja laskutuspäivän välinen aika**, **Maksuehto** ja **Laskun eräpäivän ja maksupäivän välinen aika**. Ennuste käyttää **Maksuehto**-kentän oletusasetusta vain, jos arvoa ei ole määritetty tapahtumassa. Maksuehdon avulla voi kuvata kuinka monta päivää prosessin kukin osa yleensä kestää.

**Maksujen rahatilien** kenttään määritetään maksuissa useimmiten käytettävä rahatili. **Summan prosenttiosuus, joka kohdistetaan kassavirtaennusteeseen** -kenttään määritetään, käytetäänkö summien prosenttiosuutta ennusteen aikana. Jätä tämä kenttä tyhjäksi, jos ennusteessa käytetään tapahtumien koko summia.

Voit ohittaa **Laskun eräpäivän ja maksupäivän välinen aika** -kentän oletusasetuksen tietyille toimittajaryhmille. Ennuste käyttää **Ostoennusteen oletusarvot** -osan oletusarvoa, ellei tapahtuman toimittajaan liittyvälle toimittajaryhmälle ole määritetty toista arvoa. Voit ohittaa oletusarvon valitsemalla toimittajaryhmän ja määrittämällä sitten uuden arvon **Ostoaika**-kentässä.

Voit ohittaa tietyn toimittajan kirjausprofiilien **Rahatili**-kentän oletusarvon. Ennuste käyttää **Ostoennusteen oletusarvot** -osan oletusarvoa, ellei tapahtuman toimittajaan liittyvälle kirjausprofiilille ole määritetty toista rahatiliä. Voit ohittaa oletusarvon valitsemalla kirjausprofiilin ja määrittämällä sitten rahatilin, johon vaikutuksen odotetaan kohdistuvan.

### <a name="accounts-receivable"></a>Myyntireskontra

Voit laskea myyntiennusteen **Kassavirtaennusteen määritys** -sivun **Myyntireskontra**-välilehden asetuksilla. Ennen myyntireskontran kassavirtaennusteen määrittämistä on määritettävä maksuehto, asiakasryhmät ja asiakkaiden kirjausprofiilit.

Voit valita **Myyntiennusteen oletusarvot** -osassa oletusarvoiset myyntitoiminnot kassavirtaennustetta varten. Kolme kenttää määrittää käteisvarojen vaikutusajankohdan: **Lähetyspäivän ja laskutuspäivän välinen aika**, **Maksuehto** ja **Laskun eräpäivän ja maksupäivän välinen aika**. Ennuste käyttää **Maksuehto**-kentän oletusasetusta vain, jos arvoa ei ole määritetty tapahtumassa. Maksuehdon avulla voi kuvata kuinka monta päivää prosessin kukin osa yleensä kestää. 

**Maksujen rahatilien** kenttään määritetään maksuissa useimmiten käytettävä rahatili. **Summan prosenttiosuus, joka kohdistetaan kassavirtaennusteeseen** -kenttään määritetään, käytetäänkö summien prosenttiosuutta ennusteen aikana. Jätä tämä kenttä tyhjäksi, jos ennusteessa käytetään tapahtumien koko summia.

Voit ohittaa **Laskun eräpäivän ja maksupäivän välinen aika** -kentän oletusasetuksen tietyille asiakasryhmille. Ennuste käyttää **Myyntiennusteen oletusarvot** -osan oletusarvoa, ellei tapahtuman asiakkaaseen liittyvälle asiakasryhmälle ole määritetty toista arvoa. Voit ohittaa oletusarvon valitsemalla asiakasryhmän ja määrittämällä sitten uuden arvon **Myyntiaika**-kentässä.

Voit ohittaa tietyn asiakkaan kirjausprofiilien **Rahatili**-kentän oletusarvon. Ennuste käyttää **Myyntiennusteen oletusarvot** -osan oletusarvoa, ellei tapahtuman asiakkaaseen liittyvälle kirjausprofiilille ole määritetty toista rahatiliä. Voit ohittaa oletusarvon valitsemalla kirjausprofiilin ja määrittämällä sitten rahatilin, johon vaikutuksen odotetaan kohdistuvan.

### <a name="budgeting"></a>Budjetointi

Budjettimalleista luodut budjetit voidaan sisällyttää kassavirtaennusteisiin. Valitse **Kassavirtaennusteen määritys** -sivun **Budjetointi**-välilehdessä ennusteeseen sisällytettävät budjettimallit. Uudet budjettirekisterimerkinnät sisältyvät oletusarvoisesti ennusteisiin sen jälkeen, kun budjettimalli on otettu käyttöön kassavirtaennusteessa.

Budjettirekisteritapahtumat voidaan sisällyttää kassavirtaennusteeseen yksitellen mukauttamisen avulla. Kun Sisällytä kassavirtaennusteisiin -sarake lisätään **Budjettirekisteritapahtumat**-sivulle, järjestelmä korvaa **Kassavirtaennusten asetukset** -sivulla olevat asetukset siten, että yksittäinen budjettirekisteritapahtuma sisällytetään ennusteeseen.


### <a name="inventory-management"></a>Inventoinnin- ja varastonhallinta

Varaston kysynnän ja tarjonnan ennusteet voidaan sisällyttää kassavirtaennusteisiin. Valitse **Kassavirtaennusteen määritys** -sivun **Inventoinnin- ja varastonhallinta**-välilehdessä kassavirtaennusteeseen sisällytettävät ennustemallit. Kassavirtaennusteen sisällyttäminen voidaan ohittaa yksittäisillä kysynnän ja tarjonnan ennusteriveillä.

### <a name="setting-up-dimensions-for-cash-flow-forecasting"></a>Kassavirran ennustamisen dimensioiden määrittäminen
**Kassavirran ennustamisen määritykset** -sivun uuden välilehden avulla voit määrittää, mitkä taloushallinnon dimensiot otetaan käyttöön suodatettaessa **Kassavirran ennustaminen** -työtilaa. Tämä välilehti näkyy vain, kun Finance Insightsin Kassavirtaennusteet-toiminto on käytössä. 

Valitse **Dimensiot**-välilehdessä suodatuksessa käytettävät dimensiot luettelosta ja siirrä ne oikeanpuoleiseen sarakkeeseen nuolinäppäinten avulla. Kassavirtaennustetietojen suodattamiseen voidaan valita vain kaksi dimensiota. 

### <a name="setting-up-external-source"></a>Ulkoisen lähteen määrittäminen
Ulkoisia tietoja voidaan lisätä tai tuoda kassavirtaennusteisiin. Ulkoiset lähteet on määritettävä ennen ulkoisten tietojen antamista tai tuomista. Määritä ulkoiset kassavirtaluokat **Ulkoinen lähde** -välilehdessä. Luokka voi olla joko **Lähtevä** tai **Saapuva**. Kirjaustyypiksi on valittava **Maksuvalmius**. Valitse **Yrityksen asetukset** -ruudukossa yritykset ja vastaavat päätilit, joita ulkoiset kassavirtaluokat koskevat.

### <a name="project-management-and-accounting"></a>Projektinhallinta ja kirjanpito

Versiossa 10.0.17 uusi ominaisuus mahdollistaa integroinnin projektinhallintaan ja kirjanpitoon sekä kassavirtaennusteisiin. Ota **Ominaisuuksien hallinta** -työtilassa käyttöön **Kassavirtaprojektin ennuste** -ominaisuus, jos haluat sisällyttää ennustetut kustannukset ja tuotot kassavirtaennusteeseen. Valitse **Kassavirtaennusteen asetukset** -sivun **Projektinhallinta ja kirjanpito** -välilehdessä projektityypit ja tapahtumatyypit, jotka sisällytetään kassavirtaennusteeseen. Valitse sitten projektin ennustemalli. Vähennystyypin alimalli toimii parhaiten. Myyntireskontra-asetuksiin syötettyjä maksuvalmiustilejä käytetään maksuvalmiustilien oletusarvona. Tämän vuoksi maksuvalmiustilejä ei tarvitse syöttää kassavirtaennustetta määrittäessä. Budjettimallia voidaan käyttää myös, mutta projektinhallinnan ja kirjanpidon **Kassavirtaennusteen asetukset** -sivulla voidaan valita vain yksi tyyppi. Ennustemalli tarjoaa eniten joustavuutta, kun käytetään projektinhallintaa ja kirjanpitoa tai Project Operationsia.

Kun kassavirtaprojektin ennusteominaisuus on käytössä, kassavirtaennustetta voidaan tarkastella kunkin projektin osalta **Kaikki projektit** -sivulla. Valitse toimintoruudun **Suunnitelma**-välilehden **Ennuste**-ryhmässä **Kassavirtaennuste**. **Kassayhteenveto**-työtiloissa (katso myöhemmin tässä ohjeaiheessa [Raportointi](#reporting)-osa) projektin ennustetapahtumatyyppi näyttää sisäänvirtaukset (projektiennusteen tuotot) ja ulosvirtaukset (projektiennusteen kustannukset). Summat voidaan sisällyttää vain, jos **Kassayhteenveto**-työtilojen **Projektin vaihe** -kentän arvoksi on määritetty **Käsittelyssä**.

Projektitapahtumat sisältyvät kassavirtaennusteeseen edelleen monin tavoin riippumatta siitä, onko **Kassavirtaprojektin ennuste** -ominaisuus käytössä. Kirjatut projektilaskut sisällytetään ennusteeseen avoimien asiakastapahtumien osana. Projektista peräisin olevat myynti- ja ostotilaukset sisällytetään ennusteeseen avoimina tilauksina sen jälkeen, kun ne on viety järjestelmään. Voit myös siirtää projektiennusteet kirjanpidon budjettimalliin. Tämä kirjanpidon budjettimalli sisällytetään sitten kassavirtaennusteeseen budjettirekisterimerkintöjen osana. Jos **Kassavirtaprojektin ennuste** -ominaisuus on käytössä, älä siirrä projektiennusteita kirjanpidon budjettimalliin, koska tämä toiminto aiheuttaa projektiennusteiden laskemisen kahteen kertaan.

### <a name="calculation"></a>Laskelma

Kassavirran laskentaprosessin on suoritettava ennen kassavirtaennusteen analyysien tarkastelemista. Laskentaprosessi projisoi vietyjen tapahtumien tulevat vaikutukset käteisvaroihin.

Laske kassavirtaennuste **Laske kassavirtaennusteet** -sivulla. Voit laskea koko kassavirtaennusteen tai kasvavan kassavirtaennusteen. 

- Voit poistaa kaikki kassavirtaennusten tapahtumat ja laskea uudelleen valitsemalla **Kassavirtaennusteen laskentamenetelmä** -kentässä **Yhteensä**. Tämän menetelmän käyttö on suositeltavaa, jos et ole päivittänyt kassavirtaennusteita pitkään aikaan. 
- Voit päivittä aiemmin luodun kassavirran tiedot vain uusilla tapahtumilla valitsemalla **Kassavirtaennusteen laskentamenetelmä** -kentässä **Uusi**. Sivulla näkyy ajankohta, jolloin kassavirtalaskenta viimeksi suoritettiin.

Voit käyttää kassavirtaennusteen laatimiseen myös eräkäsittelyä. Voit varmistaa, että ennusteanalytiikka päivitetään säännöllisesti määrittämällä kassavirtaennusteen laskennalle toistuvan eräkäsittelyn.

Versiossa 10.0.13 vapautettiin laskentaprosessin parannus. Se käyttää prosessin automatisoinnin kehystä ja ajoittaa kassavirran laskentatyön. Tämä otetaan käyttöön **Kassavirran ennusteen automatisointi** -ominaisuuden avulla **Ominaisuuksien hallinta** -työtilassa. Kun tämä on käytössä, valitse **Kassavirran ennusteen automatisointi** -linkki, jos haluat näyttää uuden automatisointisivun. Sivulla voi ajoittaa kassavirran laskentaprosessin. Voit luoda uuden kassavirran ennusteajoituksen valitsemalla **Luo uusi prosessin automatisointi** ja valitse sitten **Kassavirran ennusteen automatisointi** avattavasta **Ajoituksen tyyppi** -valikosta. Määritä aikataulu jokaiselle yritykselle, jonka kassavirran ennustetiedot päivitetään.  Tällä sivulla määritetään myös, mitkä kassavirran ennusteen automatisoinnin työt odottavat ja milloin edellinen työ on tehty valmiiksi.  

> [!NOTE] 
> Jos aiemmin luodut erätyöt on jo ajoitettu kassavirran ennusteisiin, näyttöön tulee virhesanoma, etkä voi ottaa tätä ominaisuutta käyttöön. Aiemmin luodut erätyöt on tyhjennettävä, ennen kuin voit ottaa tämän ominaisuuden käyttöön. 

Lisätietoja on kohdassa [Prosessin automatisointi](../../fin-ops-core/dev-itpro/sysadmin/process-automation.md).

### <a name="reporting"></a>Raportointi

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

**Kassayhteenveto – nykyinen yritys** -työtilassa kassavirtaennusteen analytiikka näkyy yrityksen määrittämänä kirjanpitovaluuttana. Analytiikassa käytettävä kirjanpitovaluutta määritetään **Kirjanpito**-sivulla. Työtilassa on nykyisen yrityksen kassavirtaennusteiden ja pankkitilin saldojen yhteenveto. Tilikartan saapuvat ja lähtevät kassavirrat on yhteenveto käteisvarojen tulevista siirroista ja saldoista kirjanpitovaluuttana. Siinä on myös tarkkoja tietoja ennakoiduista tapahtumista. Näkyvissä on myös valuuttasaldojen ennuste.

Lisätietoja kassavirtaennusteiden analytiikasta on kohdassa [Käteisvarojen yleiskatsauksen Power BI -sisältö](Cash-Overview-Power-BI-content.md).

Voit tarkastella myös tiettyjen tilien, tilausten ja nimikkeiden kassavirtaennustetietoja seuraavilla sivuilla:

- **Pääkirja**: voit tarkastella valitun päätilin tulevia kassavirtoja valitsemalla **Kassavirtaennusteet**.
- **Kaikki myyntitilaukset**: voit tarkastella valitun myyntitilauksen ennakoitua käteisvaikutusta valitsemalla **Lasku**-välilehdessä **Kassavirtaennusteet**.
- **Kaikki ostotilaukset**: voit tarkastella valitun ostotilauksen ennakoitua käteisvaikutusta valitsemalla **Lasku**-välilehdessä **Kassavirtaennusteet**.
- **Tarjontaennuste**: voit tarkastella valitun nimikkeen tarjontaennusteeseen liitettyjä kassavirtoja valitsemalla **Kassavirtaennusteet**.
- **Kysynnän ennuste**: voit tarkastella valitun nimikkeen kysynnän ennusteeseen liitettyjä kassavirtoja valitsemalla **Kassavirtaennusteet**.



[!INCLUDE[footer-include](../../includes/footer-banner.md)]
