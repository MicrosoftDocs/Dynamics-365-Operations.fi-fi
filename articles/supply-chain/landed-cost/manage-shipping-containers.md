---
title: Kuljetuskonttien hallinta
description: Tässä aiheessa käsitellään kuljetuskonttien käsittelemistä. Kuljetuskonteilla ryhmitellään yhteen tuotteita, jotka ryhmitellään fyysisesti yhteen. Niitä käytetään myös silloin, kun kustannukset on jaettava vain näiden tuotteiden välillä – yleensä koska ne ovat fyysisesti yhdessä.
author: sherry-zheng
ms.date: 12/14/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ITMContainersListPage, ITMContainers
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2020-12-14
ms.dyn365.ops.version: Release 10.0.17
ms.openlocfilehash: 62a19262f4101105654ff948cef634d825b22c4189c73eb236bd1a4730a412f5
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/05/2021
ms.locfileid: "6734184"
---
# <a name="manage-shipping-containers"></a>Kuljetuskonttien hallinta

[!include [banner](../../includes/banner.md)]

Kuljetuskonteilla ryhmitellään yhteen tuotteita, jotka ryhmitellään fyysisesti yhteen. Niitä käytetään myös silloin, kun kustannukset on jaettava vain näiden tuotteiden välillä – yleensä koska ne ovat fyysisesti yhdessä.

Voit tarkastella ja käsitellä tavaroita kuljetuskonttisivulla valitsemalla **Aiheutunut kustannus \> Kuljetuskontit \> Kaikki kuljetuskontit**. **Kaikki kuljetuskontit** -sivulla näkyy luettelo kaikista käytettävistä olevista kuljetuskonteista. Toimintoruudun painikkeiden avulla voit luoda, poistaa ja käsitellä kuljetuskontteja. Voit tarkastella minkä tahansa kuljetuskontin tietoja **Kuljetuskontit**-sivulla valitsemalla sen luettelosta.

Kuljetuskontin tietosivun yläosassa näkyvät kuljetuskontin ja kustannuslaskennan tiedot. **Rivit**-osassa näkyvät paketit, nimikkeet ja osto- tai siirtotilaukset, jotka on liitetty konttiin.

## <a name="action-pane"></a>Toimintoruutu

Sivujen **Kaikki kuljetussäiliöt** ja **Kuljetussäiliöt** toimintoruudussa on painikkeita, joiden avulla voit käsitellä valittua kuljetuskonttia. Kullakin painikkeella suoritetaan yksittäinen toiminto. Toimintoruudussa on myös välilehtiä, joista kukin puolestaan sisältää joukon asiaan liittyviä painikkeita. Ellei toisin mainita, kaikki seuraavissa alakohdissa kuvatut painikkeet ja välilehdet ovat käytettävissä sekä luettelonäkymässä (eli **Kaikki kuljetuskontit**-sivulla) että tietonäkymässä (eli **Kuljetuskontit**-sivulla).

### <a name="buttons-on-the-manage-tab"></a>Hallitse-välilehden painikkeet

Seuraavassa taulukossa kuvataan painikkeet, jotka ovat käytettävissä toimintoruudun **Hallitse**-välilehdessä.

| Painike | Kuvaukset |
|---|---|
| Kirjaa vastaanottoluettelo | Kirjaa vastaanottoluettelo tai tarkastele kaikkien kuljetuskontin ostotilausrivien tuotteen vastaanottoluetteloja. Jos käytetään usean yrityksen lähetyksiä, kunkin yrityksen osalta avautuu uusi vastaanottoluettelon kirjaamisen valintaikkuna. |
| Kirjaa tuotteen vastaanotto | Kirjaa tuotteen vastaanotto kaikille kuljetuskontin tilausriveille. |
| Kirjaa lasku | Kirjaa lasku kaikille kuljetuskontin tilausriveille. Jos käytetään usean yrityksen lähetyksiä, kunkin yrityksen osalta avautuu uusi laskun kirjaamisen valintaikkuna. |
| Lähetyksen siirtotilaus | Kirjaa siirtotilauslähetys kaikille kuljetuskontin siirtotilausriveille. Valintaikkunassa näkyvät vain ne kuljetuskontin rivit, joiden tyyppi on siirtotilaus. |
| Vastaanota siirtotilaus | Kirjaa vastaanotto kaikille kuljetuskontin siirtotilausriveille. Vastaanoton valintaikkuna on yksinkertaisin tapa vastaanottaa kuljetuskontin tai matkan tuotteita, ja se on yksi kolmesta vaihtoehdosta. Voit vastaanottaa myös saapumisten kirjauskansioiden tai mobiililaitekäsittelyn avulla. |
| Luo saapumisen kirjauskansio | Voit luoda saapumisten kirjauskansion organisaatioille käyttämällä edistyneitä varastotoimintoja. Vaihtoehdot ovat _Alusta määrä_ (suositeltava) ja joko _Luo kuljetettavista tavaroista_ tai _Luo ostotilauksista_. Kaksi viimeksi mainittua vaihtoehtoa määräytyvät sen mukaan, käytetäänkö kuljetettavien tuotteiden käsittelyä. |
| Nimeä uudelleen | Avaa valintaikkuna, jossa voit muuttaa valitun kuljetuskontin nimeä. |
| Muuta matkamallia | Matkamallin muuttaminen. Kun olet muuttanut matkamallia, sinun voi olla tarpeen valita **Hae automaattisia kustannuksia** tai lisätä kustannukset jälleen manuaalisesti, koska lähetyskustannukset poistetaan. |
| Muunna vuokraksi | Muuta valittu kuljetuskontti vuokrakuljetuskontiksi. |

### <a name="buttons-on-the-general-tab"></a>Yleistä-välilehden painikkeet

Seuraavassa taulukossa kuvataan painikkeet, jotka ovat käytettävissä toimintoruudun **Yleistä**-välilehdessä.

| Painike | Kuvaukset |
|---|---|
| Saapumisluettelo | Kirjaa vastaanottoluettelo kaikille kuljetuskontin tilausriveille. Jos käytetään usean yrityksen matkoja, kunkin yrityksen osalta avautuu uusi vastaanottoluettelon kirjaamisen valintaikkuna. |
| Tuotteen vastaanotto | Näytä tuotteen vastaanottotietue, jos sellaista käytetään. Tuotteen vastaanottoprosessia käytetään vain, jos tuotteissa ei käytetä kuljetettavien tuotteiden toimintoa. |
| Nimikkeen saapuminen | Näytä kuljetuskontin nimikkeiden saapumisen kirjauskansio, jos kyseistä kirjauskansiota käytetään. |
| Etapit | Etappeja käytetään matkan eri osien yksilöintiin. Kullekin etapille voi määrittää läpimenoajan helpottamaan lähetyksen jäljitystä. Lisätietoja: [Usean etapin matkan määrittäminen](multi-leg-journey-setup.md). |
| Seuranta | Näytä tai päivitä lähetyksen jäljitys. |
| Matkalla olevien tavaroiden tilaukset | Voit avata **Kuljetettavat tuotteet** -sivun suoraan kontista. tämä sivu näyttää vain valitun kuljetuskontin kuljetettavien tuotteiden tietueet. |

## <a name="header-view"></a>Otsikkonäkymä

Voit avata **Otsikko**-näkymän avaamalla kuljetuskontin ja valitsemalla sitten **Otsikko**-välilehden kuljetuskontin otsikon oikealta puolelta.

### <a name="settings-on-the-general-fasttab"></a>Yleinen-pikavälilehden asetukset

Seuraavassa taulukossa kuvataan asetukset, jotka ovat käytettävissä kuljetuskontin **Otsikko**-näkymän **Yleistä**-pikavälilehdessä.

| Kenttä | kuvaus |
|---|---|
| Lähetyskontti | Kuljetuskontin nimi. |
| Matka | Kuljetuskonttiin liittyvän matkan nimi. |
| Lähetyskontin tyyppi | Syötä kuljetuskontin tyyppi. Tämä kenttä on määritettävä. Voit käyttää sitä rahtikustannusten määrittämiseen esimerkiksi valitsemalla automaattisen kustannuksen, joka on määritetty kuljetuskontin tyypille. |
| Alus | Syötä tai valitse alus. Jos alus ei ole arvoluettelossa, voit syöttää aluksen tunnuksen vapaana tekstinä. Tällöin päätaulukkoa ei päivitetä, jolloin aluksen tunnus voidaan valita tässä kentässä myöhemmin. Lisätietoja: [Alukset](shipping-information-setup.md#vessels). |
| Yksikkötyyppi | Yksikkötyyppejä käytetään lisävälineenä kuljetuskonttien ryhmittelyssä ja yksilöinnissä. Ne näytetään kuljetuskonttisivulla ja valitaan sieltä. Lisätietoja: [Yksikkötyyppien määrittäminen](shipping-container-setup.md#unit-types). |
| Kylmäsäilytystyyppi | Jäähdytystyyppejä käytetään lisävälineenä kuljetuskonttien ja yleensä jäähdytettyjen konttien ryhmittelyssä ja yksilöinnissä. Ne näytetään kuljetuskonttisivulla ja valitaan sieltä. Lisätietoja: [Jäähdytystyyppien määrittäminen](shipping-container-setup.md#refrigeration-types). |
| Mittaus | Tämän kentän avulla **Aiheutunut kustannus** -moduulissa voidaan määrittää mitta. Mittoja käyttävät usein organisaatiot, jotka eivät tiedä tuotteiden yksilöllisiä tilavuuksia tai painoja mutta tarvitsevat tarkemman jakoperusteen kuin määrän tai summan. Huolitsija ilmoittaa painon kilogrammoina tai kuutiomitan, jonka voi syöttää joko nimikkeen tai ostotilauksen tasolle. Se voidaan päivittää automaattisesti, jos parametri on valittu, tai sen voi syöttää manuaalisesti. |
| Mittayksikkö | Mittayksikkö, jota käytetään **Mitta**-kentässä. |
| Todellinen paino | Voit kirjata pakkauksen tai kontin kulloisenkin painon. Tätä arvoa voi käyttää vertaamiseen kuljetuskontin suurimpaan sallittuun painoon. |
| Laatikoiden määrä | Pakkausten määrä päivitetään automaattisesti, jos parametri on valittuna. |
| Tavaroiden kuvaus | Tuotteiden kuvaus voidaan valita kuljetuskontissa tai pakkausotsikossa. Sen avulla voi yksilöidä matkan, kuljetuskontin tai pakkauksellisen tuotteita. Lisätietoja: [Tuotteiden kuvaus](shipping-information-setup.md#description-of-goods). |
| Alalentorahtikirja/rahtikirja | Voit määrittää kuljetuskontin sisäisen lentorahtikirjan tai rahtikirjan. |
| Huomautukset | Kuljetuskonttiin liittyviä lisätietoja. |
| Palautettavissa | Arvo, joka ilmaisee, voiko kuljetuskontin palauttaa matkan jälkeen. |
| Matkan tila | Kuljetuskonttiin liittyvän matkan tila. |
| Ostotilauksen tila | Kuljetuskonttiin liittyvän ostotilauksen tila. |

### <a name="settings-on-the-delivery-fasttab"></a>Toimitus-pikavälilehden asetukset

Seuraavassa taulukossa kuvataan asetukset, jotka ovat käytettävissä kuljetuskontin **Otsikko**-näkymän **Toimitus**-pikavälilehdessä.

| Kenttä | kuvaus |
|---|---|
| Luonnin päivämäärä ja aika | Päivämäärä ja kellonaika, jona kontti luotiin. |
| Lähettäjältä noutamisen päivämäärä | Tämä päivämäärä annetaan yleensä tehtaalle/toimittajalle ilmaisemaan, milloin tuotteiden odotetaan lähtevän sen tiloista. Jos tehdään yhteistyötä Aasiassa toimivan tehtaan kanssa, tämä päivämäärä vaaditaan usein sen päivämäärän sijaan, jona tuotteiden odotetaan saapuvan. (Paikallisissa toimituksissa taas vaaditaan päivämäärä, jona tuotteiden odotetaan saapuvan.) Tämä kenttä voidaan täyttää kuljetuskonttiluettelon ostotilausrivien perusteella. Se voidaan syöttää tähän myös manuaalisesti. |
| Lähetyspäivä | Tämä päivämäärä voidaan tulostaa ostotilausasiakirjassa. Sillä ilmoitetaan yleensä tehtaalle/toimittajalle se päivämäärä, jona tuotteet pitäisi toimittaa satamaan. Tämä kenttä on tarkoitettu vain tiedoksi. Sitä ei käytetä kuljetuskontin tuotteiden odotetun toimituspäivän arvioimiseen. Tämä kenttä voidaan määrittää siten, että se päivitetään automaattisesti, kun jäljityksenhallintasivu päivitetään. |
| Myymälään tulon päivämäärä | Aikaisin päivämäärä, jona matkaan liittyvien ostotilausten tuotteet ovat myytävissä.|
| Arvioitu toimituspäivämäärä | Yleensä päivämäärä, jona tuotteiden on määrä saapua varastoon. Tämä kenttä on tarkoitettu vain tiedoksi. Sitä ei käytetä pääsuunnitteluun kuljetuskontin ostotilausriveissä. Ostotilausrivien odotettu toimituspäivämäärä päivitetään jäljityksenhallinnan avulla. Tämä kenttä voidaan määrittää siten, että se päivitetään, kun jäljityksenhallintasivu päivitetään. |
| Lähtöpäivämäärä | Yleensä päivämäärä, jona lentokone tai alus todella lähtee ulkomailla olevasta lähtöpaikastaan. |
| Arvioitu saapumisaika lähetyssatamaan | Arvioitu saapumispäivämäärä kohdesatamaan. |
| Alkuperäiset asiakirjat vastaanotettu | Valinnaista : Päivitä päivämäärä, jona alkuperäiset asiakirjat on otettu vastaan. |
| Välittäjä neuvoi | Valinnaista: Päivitä päivämäärä, jona välittäjälle on ilmoitettu. |
| Alkuperäinen rahtikirja lähetetty | Valinnaista: Päivitä päivämäärä, jona alkuperäinen rahtikirja on lähetetty. |
| Vapautetut tavarat | Valinnaista : Päivitä päivämäärä, jona tuotteet on vapautettu. |
| Asiakastapaaminen | Valinnaista: Päivitä asiakastapaamisen päivämäärä. |
| Toimitettu varastoon | Valinnaista: Päivitä päivämäärä, jona tuotteet on toimitettu varastoon. |
| Tarkistuspäivämäärä | Valinnaista: Päivitä tarkistuspäivämäärä. |
| Toimitusohjeet | Valinnaista: Päivitä toimitusohjeiden päivämäärä. |
| Lähtösatama | Satama, jossa nimikkeet lähetetään. |
| Satamaan | Satama, johon nimikkeet lähetetään. |
| Paikallinen huolitsija | Tämä kenttä on tarkoitettu vain tiedoksi. Paikallisen huolitsijan pitäisi olla valittavissa toimittajaluettelosta. |
| Paikallisen kuljetuksen päivämäärä | Syötä päivämäärä, jolle paikallinen kuljetus on varattu. Tämä kenttä voi auttaa varastoa suunnittelussa. |
| Paikallisen kuljetuksen aika | Syötä aikaväli. Tämä kenttä voi auttaa varastoa suunnittelussa. |
| Matkamalli | Matkalle määritetty matkamalli. Matkamalli sisältää lähtö- ja kohdesatamien tiedot sekä läpimenoajat, jotka liittyvät kuljetuskontin jäljityksenhallintaan. |

### <a name="settings-on-the-other-fasttab"></a>Muuta-pikavälilehden asetukset

Seuraavassa taulukossa kuvataan asetukset, jotka ovat käytettävissä kuljetuskontin **Otsikko**-näkymän **Muuta**-pikavälilehdessä.

| Kenttä | kuvaus |
|---|---|
| Vuokra | Arvo, joka ilmaisee, onko kuljetuskontti vuokrakuljetuskontti. Vuokrakontteihin voi yhdistää vuokrauskustannuksia. |
| Muunnettu vuokraksi | Arvo, joka ilmaisee, onko kuljetuskontti muutettu vuokrakuljetuskontiksi. Vuokrakontteihin voi yhdistää vuokrauskustannuksia. |
| Alkuperäinen matka | Jos kuljetuskontti on siirretty uudelle matkalle, tämä on alkuperäinen matka. |
| Käytetty | Tätä käytetään sen kirjaamiseen, onko käytetty vuokrakonttia. Se on tarkoitettu vain tiedoksi. |
| Odotettu kuormauksen päivämäärä | Päivämäärä, jona kuljetuskonttiin odotetaan lastattavan tuotteita. |
| Oma sarjanumero | Syötä sarjanumero, jota yrityksesi käyttää kuljetuskontista sisäisesti. |
| Rahdinkuljettajan sarjanumero | Syötä sarjanumero, jonka rahdinkuljettaja tai edustaja on antanut kuljetuskontille. |
| Tarkastustodistuksen kohdistuksen päivämäärä | Päivämäärä, jona kuljetuskontin tarkastusta on pyydetty. |
| Tarkastustodistuksen vastaanottopäivämäärä | Päivämäärä, jona tutkimustodistus on vastaanotettu. |
| Tarkastustodistuksen vanhenemispäivä | Päivämäärä, jona tutkimustodistus vanhenee. |
| Tarkastustodistuksen numero | Tarkastuksen jälkeen laaditun todistuksen todistusnumero. |

## <a name="lines-view"></a>Rivinäkymä

Voit avata **Rivit**-näkymän avaamalla kuljetuskontin ja valitsemalla sitten **Rivit**-välilehden kuljetuskontin otsikon oikealta puolelta.

### <a name="information-on-the-shipping-container-fasttab"></a>Tietoa Kuljetuskontti-pikavälilehdestä

**Rivit**-näkymän **Kuljetuskontti**-pikavälilehti sisältää tietoja pakkauksesta. Suurin osa näistä tiedoista näkyy myös **Otsikko**-näkymässä, kuten tässä aiheessa aiemmin on kuvattu.

### <a name="information-and-buttons-on-the-lines-fasttab"></a>Rivit-pikavälilehden tiedot ja painikkeet

**Rivit**-näkymän **Rivit**-pikavälilehdessä näkyy tietoja kustakin täydestä tai osittaisesta ostotilausrivistä, joka sisältyy kulloiseenkin kuljetuskonttiin.

Seuraavassa taulukossa kuvataan painikkeet, jotka ovat käytettävissä **Rivit**-näkymän **Rivit**-pikavälilehdessä.

| Painike | kuvaus |
|---|---|
| Poista | Poista valittu ostotilausrivi matkasta. |
| Varasto \> Tapahtumat | Näytä valitun ostotilausrivin varastotapahtumat. Huomaa, että kuljetettavia tuotteita käytettäessä näkyvissä ovat myös alkuperäinen tilaus ja kuljetettavien tuotteiden tilaus. |
| Varasto \> Näytä dimensiot | Avaa valintaikkuna, jossa voit valita tarkastelemiasi tapahtumia varten näytettävät varastodimensiot. |
| Päiv. | Päivitä tietoja, jotka liittyvät valitun ostotilausrivin määrään, painoon tai tilavuuteen. |

### <a name="information-on-the-lines-details-fasttab"></a>Tietoa Rivien tiedot -pikapalkista

**Rivit**-näkymän **Rivien tiedot** -pikavälilehdessä näkyy tietoja siitä ostotilausrivistä, joka tällä hetkellä on valittuna **Rivit**-pikavälilehdessä.
