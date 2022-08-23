---
title: Commerce Scale Unitin alustaminen (pilvi)
description: Tässä artikkelissa kerrotaan, miten Commerce Scale Unit (pilvi) alustetaan Microsoft Dynamics 365 Commercessa.
author: jashanno
ms.date: 06/03/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: jashanno
ms.search.validFrom: 2018-04-30
ms.openlocfilehash: 6b42252a37f01a2b387c2393760998a6b2e4761d
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/12/2022
ms.locfileid: "9271512"
---
# <a name="initialize-commerce-scale-unit-cloud"></a>Commerce Scale Unitin alustaminen (pilvi)

[!include[banner](../includes/banner.md)]

Tässä artikkelissa kerrotaan, miten Commerce Scale Unit (pilvi) alustetaan Microsoft Dynamics 365 Commercessa.

Jos käytät Tier-2-version eristys- tai tuotantoympäristöä, jossa on sovellusversio 8.1.2.x tai sitä myöhempi versio, Commerce Scale Unit (pilvi) on alustettava, ennen kuin voit käyttää vähittäismyyntikanavan toimintoja joko myyntipisteen (POS) toiminnoissa tai sähköisen kaupan toiminnoissa, jotka käyttävät Retail Serveriä pilvessä. Alustus ottaa käyttöön Commerce Scale Unitin (pilvi).

> [!IMPORTANT]
> Jotta nykyinen asiakas voi käyttää pilvipalvelussa vähittäismyyntikanavan toimintoja ja varmistaa liiketoiminnan jatkuvan ja keskeytymättömän tuen, vähittäismyyntikanavat on päivitettävä käyttämään Commerce Scale Unitia. Ilman Commerce Scale Unitia käyttöön otettavat uudet ympäristöt eivät enää voi vastaanottaa pilvipalvelussa ylläpidettyjen vähittäismyyntikanavan komponenttien laatu- ja palvelupäivityksiä. Commerce Scale Unitia (paikallinen ympäristö) käyttävät asiakkaat eivät tarvitse toimenpiteitä. Jos tarvitset jatkoaikaa, ota yhteys Microsoft FastTrack Solution Architect -asiantuntijaan.

## <a name="prerequisites"></a>Edellytykset

1. Ota käyttöön Tier-2-version eristys- tai tuotantoympäristö, jonka versio on 8.1.2.x tai myöhempi.
2. Voit ottaa käyttöön enintään kaksi Commerce Scale Unitia ympäristöä kohti. Jos tarvitset enemmän kuin kaksi Commerce Scale Unitia ympäristöä kohden, luo Microsoft Dynamics Lifecycle Servicesissä tukipyyntö **Pyyntö ylimääräisestä Commerce Scale Unitista** ja määritä ympäristötunnus, Commerce Scale Unitien määrä ja halutut konesalialueet. Pyyntö täytetään viiden työpäivän kuluessa. Jos et tarvitse yli kahta Commerce Scale Unitia ympäristöä kohden, tukipyyntöä ei tarvitse luoda. 
3. Sinulla on oltava projektin omistajan käyttöoikeudet Lifecycle Services -palveluissa, ennen kuin voit alustaa Commerce Scale Unitin.
4. Varmista, että Retail-lisenssien määritysavaimet ovat käytössä ympäristössäsi. Lisätietoja: [Käyttöoikeuskoodien ja määritysavainten raportti](../sysadmin/license-codes-configuration-keys-report.md). Seuraavat avaimet on otettava käyttöön Commerce Scale Unitin käyttöä varten.

    - RetailBasic
    - RetaileCommerce – Jos aiot käyttää E-Commerce for Dynamics 365 Commercea.
    - RetailGiftCard - Jos aiot käyttää lahjakortteja.
    - RetailInvent - Jos aiot käyttää varastoa.
    - RetailModernPos - Jos aiot käyttää myyntipistettä (POS).
    - RetailReplenishment - Jos aiot käyttää täydennyksiä.
    - RetailScheduler
    - RetailStores - Jos aiot käyttää myyntipistettä.


## <a name="region-availability"></a>Alueellinen saatavuus
Commerce Scale Unitia voi käyttää seuraavilla alueilla.

| Globaali sijainti | Alue              | Saatavuus        | Kommentit                  |
|-----------------|---------------------|---------------------|---------------------------|
| AMERIKAN MANNER        | Itä-Yhdysvallat             | Yleisesti saatavilla |  Ei kommentteja.                         |
| AMERIKAN MANNER        | Itä-Yhdysvallat 2           | Yleisesti saatavilla |  Ei kommentteja.                          |
| AMERIKAN MANNER        | Keskinen Pohjois-Yhdysvallat    | Rajallinen kapasiteetti    |  Ei kommentteja.                            |
| AMERIKAN MANNER        | Keskinen Etelä-Yhdysvallat    | Rajallinen kapasiteetti    |  Ei kommentteja.                            |
| AMERIKAN MANNER        | Keskinen Yhdysvallat          | Yleisesti saatavilla |  Ei kommentteja.                            |
| AMERIKAN MANNER        | Länsi-Yhdysvallat             | Yleisesti saatavilla |  Ei kommentteja.                            |
| AMERIKAN MANNER        | Länsi-Yhdysvallat 2           | Yleisesti saatavilla |  Ei kommentteja.                            |
| AMERIKAN MANNER        | Kanada, keskinen      | Rajallinen kapasiteetti    |  Ei kommentteja.                            |
| AMERIKAN MANNER        | Kanada, itäinen         | Rajallinen kapasiteetti    |   Ei kommentteja.                           |
| AMERIKAN MANNER        | Keskinen Länsi-Yhdysvallat     | Rajallinen kapasiteetti    |   Ei kommentteja.                           |
| APAC            | Itä-Australia      | Yleisesti saatavilla |   Ei kommentteja.                           |
| APAC            | Kaakkois-Aasia      | Rajoitettu kapasiteetti | Käyttöönottoja ei sallita.    |
| APAC            | Itä-Japani          | Yleisesti saatavilla |  Ei kommentteja.                            |
| APAC            | Länsi-Japani          | Yleisesti saatavilla |   Ei kommentteja.                           |
| APAC            | Kaakkois-Australia | Yleisesti saatavilla |   Ei kommentteja.                           |
| APAC            | Itä-Aasia           | Rajallinen kapasiteetti    |   Ei kommentteja.                           |
| APAC            | Intia, etelä         | Rajoitettu kapasiteetti | Käyttöönottoja ei sallita.    |
| APAC            | Keskinen Intia       | Rajallinen kapasiteetti    | Vaatii hyväksyntäprosessin. |
| EMEA            | Länsi-Eurooppa         | Rajallinen kapasiteetti    | Ei saatavana LCS:ssä tällä hetkellä. |
| EMEA            | Pohjois-Eurooppa        | Rajallinen kapasiteetti    | Ei saatavana LCS:ssä tällä hetkellä. |
| EMEA            | Yhdistynyt kuningaskunta, etelä            | Yleisesti saatavilla |    Ei kommentteja.                          |
| EMEA            | Yhdistynyt kuningaskunta, länsi             | Yleisesti saatavilla |    Ei kommentteja.                          |
| Sveitsi     | Sveitsi, pohjoinen   | Rajallinen kapasiteetti    | Vaatii hyväksyntäprosessin. |
| Yhdistyneet arabiemiirikunnat             | Yhdistyneet arabiemiirikunnat, pohjoinen           | Rajallinen kapasiteetti    | Vaatii hyväksyntäprosessin. |

Rajallisen kapasiteetin alueilla on erittäin rajoitettu käyttökapasiteetti. Käyttöönottopyynnöt arvioidaan tapauskohtaisesti. Jos rajallisen kapasiteetin alueilla on tehtävä liiketoimintaa, voit lisätä tukipyynnön odotusluetteloon. Rajoitetun kapasiteetin alueet eivät tällä hetkellä mahdollista Commerce Scale Unit -käyttöönottoa. 

![Kartta, jossa alueellinen käytettävyys.](media/Commerce-Scale-Unit-Region-Availability.png "Kartta, jossa alueellinen käytettävyys")

## <a name="initialize-commerce-scale-unit-as-part-of-a-new-environment-deployment"></a>Commerce Scale Unitin alustaminen osana uutta ympäristön käyttöönottoa

Varmista, että pääkonttori on käytettävissä. Tämä on tarpeen, jotta skaalausyksikkö rekisteröidään pääkonttoriin alustusprosessin aikana. Skaalausyksikön alustaminen ei ole suositeltavaa, kun pääkonttori on huollettavana, sillä se ei ehkä ole käytettävissä huoltoprosessin aikana.

1. Varmista, että headquarters-ympäristö on käytettävissä mutta ei [ylläpitotilassa](../sysadmin/maintenance-mode.md).
2. Valitse LCS:n ympäristön tietosivulta **Ympäristön ominaisuudet \> Commerce**.
3. Valitse Commerce-määrityksen käyttöönottosivulla **Alusta**.
4. Valitse alustettava Commerce Scale Unitin versio.
5. Valitse alue, jossa Commerce Scale Unit alustetaan.

## <a name="configure-channels-to-use-commerce-scale-unit"></a>Commerce Scale Unitin käytön konfiguroiminen kanaviin

Kun Commerce Scale Unit on otettu käyttöön, sinun on varmistettava, että kanavat on määritetty käyttämään sen tietokantaa. 

Voit määrittää kanavat käyttämään Commerce Scale Unit -tietokantaa noudattamalla seuraavia vaiheita.

1. Valitse Commerce-pääkonttorisovelluksessa **Retail ja Commerce \> Pääkonttorin asetukset \> Commerce-ajastus \> Kanavatietokanta**.
1. Valitse kanavatietokanta vasemmanpuoleisesta ruudusta.
1. Valitse **Vähittäismyyntikanava**-pikavälilehdessä **Lisää** ja valitse sitten vähittäismyyntikanava avattavasta luettelosta.
1. Valitse **Lisää** ja valitse sitten avattavasta luetteloruudusta online-kanava. 

Kun olet valmis, siirry kohtaan **Retail ja Commerce \> Retail ja Commerce IT \> Jakeluaikataulu** ja suorita 9999-työ.

> [!NOTE] 
> Työ 9999 synkronoi kaikki uudet tuotteet ja asiakkaat Commerce Scale Unitiin. Tämä prosessi voi kestää kauan. Jos kanavan on oltava käytettävissä vain sähköisen kaupankäynnin muodostimen konfiguroinnissa, voit suorittaa työn 1070 työn 9999 asemesta.

### <a name="database-refresh-and-commerce-scale-units"></a>Tietokannan päivitys ja Commerce Scale Unitit

Varmista ennen aloittamista, että tiedät [Tietokannan päivityksen jälkeiset vaiheet ympäristössä, jotka käyttävät Commerce-toimintoja](../database/database-refresh.md).

Skaalausyksikön kanavatietokantatietueita (kanavan tietokantalomakkeessa) ei voi siirtää eri ympäristöjen välillä osana tietokannan päivitystä. Tämä johtuu siitä, että tietueet edustavat ympäristökohtaista konfiguraatiota.

Tietokantapäivityksen jälkeen voit luoda skaalausyksikön kanavatietokannan tietueen uudelleen käyttöönottamalla skaalausyksikön uudelleen LCS:ssä. Skaalausyksikön käyttöönotto- tai huoltotoiminto yrittää rekisteröidä skaalausyksikön pääkonttorin kanssa, jos rekisteröinti on havaittu puuttuvaksi.

Voit ottaa skaalausyksikön uudelleen käyttöön muuttamatta komponentteja valitsemalla saman version, jonka skaalausyksikkösi on jo ottanut käyttöön. Tämän voi tehdä LCS:ssä seuraavien vaiheiden mukaisesti:

1. Valitse LCS:n ympäristön tietosivulta **Ympäristön ominaisuudet \> Retail**.
2. Valitse asetusten käyttöönottosivulla skaalausyksikkö, jonka haluat ottaa uudelleen käyttöön.
3. Valitse skaalausyksikön työvaihevalikosta **Päivitä**.
4. Valitse liukusäätimessä avattavasta **Valitse versio** -valikosta  **Määritä versio**.
5. Kirjoita skaalausyksikölle **Nykyinen versio** -kohdan vieressä näkyvä versio **Määritä versio** -kohdan tekstiruutuun.
6. Valitse **Päivitä**-painike.

**Päivitä laajennukset** -kohtaa ei tarvitse valita, vaikka olet aiemmin käyttänyt laajennuksia, sillä skaalausyksikköön viimeksi kohdistettu laajennuspaketti kerätään automaattisesti skaalausyksikön päivityksen yhteydessä.

Jos sinulla on useita skaalausyksiköitä, sinun on suoritettava yllä oleva toiminto kullekin skaalausyksikölle. Voit tarvittaessa suorittaa nämä toiminnot rinnakkain.

## <a name="deploy-additional-commerce-scale-units-optional"></a>Ota käyttöön lisää Commerce Scale Uniteja (valinnainen)

Kun olet alustanut Commerce Scale Unitin, voit ottaa käyttöön toisen Scale Unitin, jos käyttöoikeutesi sen oikeuttaa. Jos haluat ottaa käyttöön enemmän kuin kaksi Scale Unitia, luo tukipyyntö. Anna tukipyynnössä haluamasi Commerce Scale Unitien määrä, ympäristön nimi ja halutut alueet. Lisätietoja lisensseistä on [Dynamics 365:n käyttöoikeusoppaassa](https://go.microsoft.com/fwlink/?LinkId=866544&clcid=0x409). 

On suositeltavaa luoda kullekin käyttöön otettavalle Commerce Scale Unitille erillinen kanavatietokantaryhmä seuraavien vaiheiden mukaisesti.

1. Valitse Commerce-pääkonttorisovelluksessa **Retail ja Commerce > Retail Headquarters > Retail-ajastuksen asetukset > Kanavatietokantaryhmä**.
2. Luo uusi kanavatietokantaryhmä.
3. Siirry kohtaan **Retail ja Commerce > Retail Headquarters > Retail-ajastuksen asetukset > Kanavatietokanta** ja valitse kanavatietokanta, joka vastaa juuri luotua Commerce Scale Unitia.
4. Valitse **Muokkaa** ja valitse uusi kanavatietokantaryhmä.
5. Valitse **Tallenna**.
6. Valitse valitulle kanavatietokannalle **Suorita täydellinen tietojen synkronointi**.

## <a name="additional-considerations-if-you-initialize-cloud-hosted-commerce-channel-components-in-an-existing-environment"></a>Muita huomioon otettavia seikkoja, jos alustat pilvipalvelussa ylläpidetyt Commerce-kanavakomponentit aiemmin luodussa ympäristössä

Jos käytät jo ympäristössä pilvipalvelussa isännöityjä Commerce-kanavakomponentteja, Commerce Scale Unitin alustaminen auttaa vähentämään käyttökatkoja, kun kyseisiä komponentteja päivitetään. Lisää suunnittelua tarvitaan ennen Commerce Scale Unitin alustamista.

Kun alustat ensimmäisen Commerce Scale Unitin ympäristössä, joka käyttää pilvipalvelussa isännöityä Commerce-kanavaosia, alustusprosessi siirtää pilvipalvelussa ylläpidettyihin kanavakomponentteihin liittyvät kanavat ensimmäiseen skaalausyksikköön. Myymälän skaalausyksiköihin liittyvät kanavat eivät muutu.

Siirtoprosessi kanaviin on läpinäkyvä. Kun skaalausyksikön alustus käynnistyy, seuraavat toiminnot suoritetaan automaattisesti:

1. Ympäristölle luodaan uusi Commerce Scale Unit, joka liitetään siihen.
2. Commerce Scale Unit rekisteröidään käytettävissä olevaksi kanavatietokannaksi pääkonttorissa.
3. Kaikki pääkonttorin **Oletus**-kanavatietokantaan liittyvät kanavat päivitetään yhdistämään uuteen Commerce Scale Unitiin.
4. Täydellinen Commerce Data Exchange (CDX) -synkronointi suoritetaan, jotta kanavan tiedot voidaan tuoda uuteen skaalausyksikköön.

**Commerce Scale Unitin alustuksen suunnittelu ja testaaminen** Yleissääntönä on, että Commerce Scale Unitia alustettaessa on suunniteltava myymälätoimintojen sekä kaikkia Retail Serveriä tai pilvimyyntipistettä käyttävät sähköisen kaupan kanavan toimintojen käyttökatkoa viideksi tunniksi.

1. Suorita tietokannan päivitys tuotantoympäristöstä eristettyyn UAT-ympäristöön. 
2. Alusta Commerce Scale Unit UAT-ympäristössä. 
3. Pane merkille Commerce Scale Unitin alustusaika. Tämä on verrattavissa siihen aikaan, jonka prosessi kestää tuotantoympäristössä, jonka aikana myymälän toiminnot ja sähköinen kaupankäynti ei ole käytettävissä.

Suorita seuraavat lisävaiheet ennen Commerce Scale Unitin alustamista.

- **Sulje kaikki myyntipisteiden työvuorot** - Myyntipisteen käyttäjät eivät voi siirron jälkeen sulkea siirtoprosessin aikana aktiivisia vuoroja.
- **Vahvista, että kaikki P-työt on suoritettu onnistuneesti loppuun** - On suositeltavaa, että P-työt synkronoidaan, ennen kuin CSU alustetaan.
- **Kirjaudu ulos kaikista myyntipistelaitteista** - myyntipistetoimintoja ei tueta siirron aikana.
- **Peruuta ja mitätöi kaikki myyntipisteen keskeytetyt tapahtumat** - Keskeytettyjä tapahtumia ei säilytetä alustuksen osana.

> [!IMPORTANT]
> Osana Commerce Scale Unitin alustusta aiemmat keskeytetyt tapahtumat menetetään, eikä niitä voi peruuttaa. 

Alustuksen aikana tapahtuu näin:

- Pilvessä ylläpidetyt Commerce-kanavat eivät toimi, ellet ota myyntipisteen offline-ominaisuutta käyttöön.
- Myyntipistelaitteissa, joissa on offline-ominaisuus käytössä, on rajoitettu toiminnallisuus.
- Kaikki Retail Serveristä riippuvat e-Commerce -työasemat häiriintyvät.
- Commerce Scale Unit (paikallinen ympäristö) -kanavat eivät muutu.
- Pääkonttorin toiminnallisuus ei muutu.

Näin tapahtuu alustuksen jälkeen:

- Kaikkien aktivoitujen myyntipistelaitteiden aktivointitila säilytetään, mikä tarkoittaa, että laitteita ei tarvitse aktivoida uudelleen.
- Itsenäiset Hardware Station -instanssit jatkavat toimimista.
- Myyntipistekanavan sivuraportit nollataan, eikä tietoja näytetä ajalta ennen alustamista.
- Näytä kirjauskansio -työvaihe myös nollataan, eikä tietoja näy ajalta ennen alustamista.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
