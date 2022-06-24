---
title: Pakkausten hallinta
description: Tässä artikkelissa kuvataan, miten pakkauksia käsitellään. Pakkaus koostuu yleensä yhden toimittajan tuotteista yhdelle yksikölle tai yritykselle lähetystä kohden. Pakkauksen tuotteet voivat olla yhdessä kontissa tai jakautuneet useisiin kontteihin.
author: Weijiesa
ms.date: 12/14/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ITMFolioTable, ITMFolioTableListPage
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: weijiesa
ms.search.validFrom: 2020-12-14
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 4cc556c47f7027f2f5d5b24c235b11ced63b3e4e
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8905889"
---
# <a name="manage-folios"></a>Pakkausten hallinta

[!include [banner](../../includes/banner.md)]

Pakkaus määräytyy usein tullisäännösten mukaan. Se voi koostua yhden toimittajan tuotteista yhdelle yksikölle tai yritykselle lähetystä kohden. Voi olla, että pakkauksessa olevat tavarat hallitaan yhdessä kontissa.

Voit avata **Kaikki pakkaukset** -sivun siirtymällä kohtaan **Aiheutunut kustannus \> Pakkaukset \> Kaikki pakkaukset**. Tällä sivulla on luettelo kaikista nykyisistä pakkauksista. Toimintoruudun painikkeiden avulla voit luoda, poistaa ja käsitellä pakkauksia. Voit tarkastella minkä tahansa pakkauksen tietoja **Pakkaukset**-sivulla valitsemalla sen luettelosta.

## <a name="action-pane"></a>Toimintoruutu

Sivujen **Kaikki pakkaukset** ja **Pakkaukset** toimintoruudussa on painikkeita, joiden avulla voit käsitellä valittua pakkausta. Kullakin painikkeella suoritetaan yksittäinen toiminto. Toimintoruudussa on myös välilehtiä, joista kukin puolestaan sisältää joukon asiaan liittyviä painikkeita. Ellei toisin mainita, kaikki seuraavissa alakohdissa kuvatut painikkeet ja välilehdet ovat käytettävissä sekä luettelonäkymässä (eli **Kaikki pakkauukset**-sivulla) että tietonäkymässä (eli **Pakkaukset**-sivulla).

### <a name="buttons-that-appear-directly-on-the-action-pane"></a>Suoraan toimintoruudussa näkyvät painikkeet

Seuraavassa taulukossa kuvataan painikkeet, jotka ovat käytettävissä suoraan toimintoruudussa.

| Painike | kuvaus |
|---|---|
| Luo uusi | Pakkauksen luominen. |
| Delete-näppäin | Poista avoin tai valittu pakkaus. |
| Matkan kustannukset | Avaa **Merikuljetuksen kustannukset** -sivu, jolla voit tarkastella ja lisätä pakkaustason kustannuksia kaikkiin sen sisältämiin tuotteisiin. Kun merikuljetukseen lisätään manuaalisesti pakkauskustannuksia, ne lisätään automaattisesti Kustannustiedustelu-sivulle ja jaetaan kullekin tuotteelle **Merikuljetuksen kustannukset** sivulla määritetyn menetelmän mukaisesti. |

### <a name="buttons-on-the-manage-tab"></a>Hallitse-välilehden painikkeet

Seuraavassa taulukossa kuvataan painikkeet, jotka ovat käytettävissä toimintoruudun **Hallitse**-välilehdessä.

| Painike | kuvaus |
|---|---|
| Kirjaa vastaanottoluettelo | Kirjaa vastaanottoluettelo kaikille pakkauksen ostotilausriveille. Jos käytetään usean yrityksen lähetyksiä, kunkin yrityksen osalta avautuu uusi vastaanottoluettelon kirjaamisen valintaikkuna. |
| Kirjaa tuotteen vastaanotto | Kirjaa tuotteen vastaanotto kaikille pakkauksen tilausriveille. Jos käytetään usean yrityksen merikuljetuksia, kunkin yrityksen osalta avautuu uusi tuotteen vastaanottoluettelon kirjaamisen valintaikkuna. |
| Kirjaa lasku | Kirjaa lasku kaikille pakkauksen tilausriveille. Jos käytetään usean yrityksen merikuljetuksia, kunkin yrityksen osalta avautuu uusi laskun kirjaamisen valintaikkuna. |
| Lähetyksen siirtotilaus | Kirjaa siirtotilaus kaikille siirtotilausriveille, jotka liittyvät liittyvässä lähetyksessä nykyiseen tilaukseen. |
| Vastaanota siirtotilaus | Kirjaa siirtotilauksen vastaanotto kaikille siirtotilausriveille, jotka liittyvät liittyvässä lähetyksessä nykyiseen tilaukseen. |
| Vastaanota matkalla olevat tavarat | Vastaanota kaikki tilausrivit, jotka ovat kuljetettavana pakkauksessa. |
| Asiakirjat vastaanotettu | Päivitä **Asiakirjat vastaanotettu** -asetuksen arvoksi *Kyllä*. Tämän painikkeen avulla voit lukita nimikkeen ja/tai ostorivin, jotta riviä ei voida enää päivittää. |
| Hae automaattiset kustannukset | Etsi asianomaiset matkakustannukset. Jos nämä kustannukset on jo löydetty tai päivitetty, näyttöön tulee viesti "Laskuttamattomia kustannusrivejä löytyi. Haluatko korvata ne?" Huomaa, että merikuljetuksen kustannuksia, jotka on liitetty pakkauksiin ja laskutettu, ei korvata. |
| Luo saapumisen kirjauskansio | Luo saapumisten kirjauskansion organisaatioille käyttämällä edistyneitä varastotoimintoja. Voit valita **Alusta määrä** (suositeltava), **Luo kuljetettavista tavaroista** ja/tai **Luo ostotilauksista**. Viimeksi mainittu vaihtoehto määräytyy sen mukaan, käytetäänkö kuljetettavien tuotteiden käsittelyä. |
| Jaksota kustannukset | Kustannukset voi jaksottaa, jos kustannuslajin veloitukselle on määritetty kirjanpitotili. Tätä painiketta käytetään yleensä, kun varasto on kuljetettava tai kun tuotteet on vastaanotettu ja laskutettu. |

### <a name="buttons-on-the-general-tab"></a>Yleistä-välilehden painikkeet

Seuraavassa taulukossa kuvataan painikkeet, jotka ovat käytettävissä toimintoruudun **Yleistä**-välilehdessä.

| Painike | kuvaus |
|---|---|
| Saapumisluettelo | Kirjaa vastaanottoluettelo kaikille pakkauksen ostotilausriveille. Jos käytetään usean yrityksen matkoja, kunkin yrityksen osalta avautuu uusi vastaanottoluettelon kirjaamisen valintaikkuna. |
| Tuotteen vastaanotto | Näytä tuotteen vastaanottotietue, jos sellaista käytetään. |
| Nimikkeen saapuminen | Tarkastele nimikkeen saapumisten kirjauskansiota, jos sitä käytetään. |
| Kustannuskysely | Avaa kustannuskyselysivu, jossa voit tarkastella kaikkia merikuljetuksen kustannuksia, mukaan lukien kuljetuskontti, pakkaus ja ostotilaus. Voit muokata sivun tarkkaa näkymää käyttämällä Näytä-toimintoa. Voit tarkastella kustannuskyselysivulla alueita sekä nimike- ja kustannustyyppikoodia. Poistamalla nämä nimikkeet voit muokata sivua ryhmittäen kustannuksia yhteen. Tämä ominaisuus voi olla hyödyllinen, kun käytät kokoja ja värejä. Voit muuttaa sivulla näkyviä dimensioita. **Kustannus**-sivulla näkyvät vain kustannuslajikoodit, joissa **Dr**-merkinnän arvona **Kirjaus**-välilehdessä on *Nimike*. |

## <a name="header-view"></a>Otsikkonäkymä

Voit avata **Otsikko**-näkymän avaamalla pakkauksen ja valitsemalla sitten **Otsikko**-välilehden pakkauksen otsikon oikealta puolelta.

### <a name="settings-on-the-general-fasttab"></a>Yleinen-pikavälilehden asetukset

Seuraavassa taulukossa kuvataan kentät, jotka ovat käytettävissä pakkauksen **Otsikko**-näkymän **Yleistä**-pikavälilehdessä.

| Kenttä | kuvaus |
|---|---|
| Lasku | Pakkauksen nimi. Tämä nimi luodaan automaattisesti, kun pakkaus luodaan.|
| Matka | Pakkaukseen liittyvän merikuljetus. |
| Tulliasiamies | Valitse pakkauksen tulliasioitsija. Tulliasioitsijat määritetään toimittajassa. Niiden avulla luodut kustannukset voidaan määrittää automaattisesti. |
| Alalentorahtikirja/rahtikirja | Määritä pakkauksessa käytettävä sisäinen lentorahtikirja tai rahtikirja. |
| Yhtiö | Pakkaukseen liitetty yritys. |
| Rahdin tarkistusnumero | Tulliosastot käyttävät tätä kenttää joissakin maissa tai joillakin alueilla. |
| Mittaus | Tämän kentän avulla **Aiheutunut kustannus** -moduulissa voidaan määrittää mitta. Mittoja käyttävät usein organisaatiot, jotka eivät tiedä tuotteiden yksilöllisiä tilavuuksia tai painoja mutta tarvitsevat tarkemman jakoperusteen kuin määrän tai summan. Huolitsija ilmoittaa painon tai kuutiomitan, jonka voi syöttää joko nimikkeen tai ostotilauksen tasolle. Se voidaan päivittää automaattisesti, jos parametri on valittu, tai sen voi syöttää manuaalisesti. |
| Mittayksikkö | Määritettyyn mittaan sovellettu yksikkö. |
| Laatikoiden määrä | Pakkauksessa olevien laatikoiden määrä. Parametrivalinnan mukaan tämä kenttä voidaan päivittää automaattisesti. |
| Toimittajanro | Valitse pakkaukseen liittyvä toimittaja. Tämä kenttä on tarkoitettu vain tiedoksi. Se ei vaikuta mihinkään toimintoon. |
| Nimi | Valittuna olevan toimittajatilin nimi. |
| Huomautukset | Kirjoita pakkaukseen liittyvät lisätiedot. |
| Tavaroiden kuvaus | Valitse tuotekuvaus, joka auttaa tunnistamaan pakkauksen. Lisätietoja: [Tuotteiden kuvaus](shipping-information-setup.md#description-of-goods). |
| Arvostuspäivämäärä | Tämä kenttä liittyy verojen merkintäsivuun. **Aiheutunut kustannus** -moduuli käyttää tässä määritetyn päivän tullin vaihtokurssia. Oletusarvo on veromerkintäsivun päivämäärä. |
| Tullin tunnus | Syötä tullin tunnus. Maiden tai alueiden tulliosastot antavat tämän tunnuksen. |
| Tariffikoodi | Kirjoita pakkaukseen liitettävä tariffikoodi. Tämä koodi on yleensä pakollinen (ja määritetty) sen maan tai alueen mukaan, jonne lähetys on tehty. |

### <a name="settings-on-the-delivery-fasttab"></a>Toimitus-pikavälilehden asetukset

Seuraavassa taulukossa kuvataan asetukset, jotka ovat käytettävissä pakkauksen **Otsikko**-näkymän **Toimitus**-pikavälilehdessä.

| Kenttä | kuvaus |
|---|---|
| Laskun päivämäärä | Valitse pakkaukseen liitettävä päivämäärä. Oletusarvo on merikuljetuksen luontipäivä. |
| Arvioitu saapumisaika lähetyssatamaan | Arvioitu saapumisaika kohdesatamaan. |
| Arvioitu toimituspäivämäärä | Yleensä päivämäärä, jona tuotteiden on määrä saapua varastoon. Tätä kenttää ei käytetä, kun arvioitu toimituspäivä lasketaan. (Sen sijaan käytetään seurannan ohjauksen arvioitua toimituspäivää.) Jos haluat määrittää tämän kentän niin, että arvo vastaa seurannan ohjauksen arvioitua toimituspäivämäärää, käytä [seurannan ohjauskeskusta](delivery-information-setup.md#tracking-control-center). |
| Alkuperäiset asiakirjat vastaanotettu | Päivämäärä, jona alkuperäiset asiakirjat on otettu vastaan. |
| Välittäjä neuvoi | Päivämäärä, jona välittäjälle on ilmoitettu. |
| Alkuperäinen rahtikirja lähetetty | Päivämäärä, jona alkuperäinen rahtikirja on lähetetty. |
| Vapautetut tavarat | Päivämäärä, jolloin tavarat vapautettiin. |
| Asiakastapaaminen | Asiakastapaamisen päivämäärä. |
| Toimitettu varastoon | Päivämäärä, jona tuotteet on toimitettu varastoon. |
| Tarkistuspäivämäärä | Tarkistuspäivämäärä. |
| Toimitusohjeet | Päivämäärä, jona toimitusohjeet on otettu vastaan. |
| Lähtösatama | Satama, josta matka alkaa. |
| Satamaan | Satama, johon matka saapuu. Kuljetuskonteilla voi olla eri satama, koska laiva saattaa pysähtyä useissa satamissa. |

### <a name="settings-on-the-export-fasttab"></a>Vienti-pikavälilehden asetukset

Seuraavassa taulukossa kuvataan asetukset, jotka ovat käytettävissä pakkauksen **Otsikko**-näkymän **Vienti**-pikavälilehdessä.

| Kenttä | kuvaus |
|---|---|
| Viejä | Viejä voidaan tallentaa pakkaukseen. Kansainvälisessä kaupassa voit lähettää ostotilauksen yhdelle yritykselle mutta vastaanottaa tavarat toisesta yrityksestä. Seuranta ja dokumentaatio ovat pakollisia tullissa. Täällä voit tallentaa viejän nimen ja osoitteen. |
| Nimi | Valitun viejän nimi. |

## <a name="lines-view"></a>Rivinäkymä

Voit avata **Rivit**-näkymän avaamalla pakkauksen ja valitsemalla sitten **Rivit**-välilehden pakkauksen otsikon oikealta puolelta.

### <a name="information-on-the-folio-fasttab"></a>Tietoa Pakkaus-pikavälilehdestä

**Rivit**-näkymän **Pakkaus**-pikavälilehti sisältää tietoja pakkauksesta. Suurin osa näistä tiedoista näkyy myös **Otsikko**-näkymässä, kuten tässä artikkelissa aiemmin on kuvattu.

### <a name="information-and-buttons-on-the-lines-fasttab"></a>Rivit-pikavälilehden tiedot ja painikkeet

**Rivit**-näkymän **Rivit**-pikavälilehdessä näkyy tietoja kustakin täydestä tai osittaisesta ostotilausrivistä, joka sisältyy kulloiseenkin pakkaukseen.

Seuraavassa taulukossa kuvataan painikkeet, jotka ovat käytettävissä **Rivit**-näkymän **Rivit**-pikavälilehdessä.

| Painike | kuvaus |
|---|---|
| Poista | Poista valittu ostotilausrivi matkasta. |
| Varasto \> Tapahtumat | Näytä valitun ostotilausrivin varastotapahtumat. Huomaa, että kuljetettavia tuotteita käytettäessä näkyvissä ovat myös alkuperäinen tilaus ja kuljetettavien tuotteiden tilaus. |
| Varasto \> Näytä dimensiot | Avaa valintaikkuna, jossa voit valita tarkastelemiasi tapahtumia varten näytettävät varastodimensiot. |
| Päiv. | Päivitä tietoja, jotka liittyvät valitun ostotilausrivin määrään, painoon tai tilavuuteen. |

### <a name="information-on-the-lines-details-fasttab"></a>Tietoa Rivien tiedot -pikapalkista

**Rivit**-näkymän **Rivien tiedot** -pikavälilehdessä näkyy tietoja siitä ostotilausrivistä, joka tällä hetkellä on valittuna **Rivit**-pikavälilehdessä.
