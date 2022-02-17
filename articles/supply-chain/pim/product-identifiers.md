---
title: Tuotetunnukset
description: Tässä ohjeaiheessa on tietoja erityyppisistä tuotetunnisteista ja selitetään tuotetunnisteiden lisäämiseen tuotetietoihin.
author: t-benebo
ms.date: 03/27/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EcoResProductEntityIdentifierCode, EcoResProductListPage, EcoResProductDetailsExtended, EcoResProductVariantsPerCompany
audience: Application User, IT Pro
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: benebotg
ms.dyn365.ops.version: 7.2999999999999998
ms.search.validFrom: 2017-12-31
ms.openlocfilehash: 638b5c3b0c83f67f3d99331b6456efd1b8f5225a
ms.sourcegitcommit: 4be1473b0a4ddfc0ba82c07591f391e89538f1c3
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/31/2022
ms.locfileid: "8063338"
---
# <a name="product-identifiers"></a>Tuotetunnukset



[!include [banner](../includes/banner.md)]

Tässä ohjeaiheessa on tietoja erityyppisistä tuotetunnisteista ja selitetään tuotetunnisteiden lisäämiseen tuotetietoihin.

Kun käsittelet tuotteita Microsoft Dynamics ERP:n tai Microsoft Dynamics CRM:n työnohjauksessa tai varastossa, tarvitse hyvän strategian kyseisten tuotteiden ja tuotevarianttien tunnistamiseen.

## <a name="unique-product-numberproduct-id"></a>Yksilöivä tuotenumero tai tuotetunnus

Dynamics 365 Supply Chain Managementissa tuotteen ensisijainen tunniste on tuotenumero (joka on sama kuin yksilöivä tuotetunnus). Numerosarja voi muodostaa numeron automaattisesti tai liittää tuotteeseen manuaalisesti. Tuotevarianttien numerot voidaan määrittää tuotenimikkeistömallin kautta.

Tuotenumeroa ei usein ole luotu alun perin Dynamics 365 Supply Chain Management -sovelluksessa. Sen sijaan se liitetään tuotteen elinkaaren hallinta (PLM)- tai tuotteen tiedonhallinta (PDM) -järjestelmään. Tässä tapauksessa tietoyksiköitä käytetään tuotteiden ja tuotevarianttien tuonnissa. Supply Chain Management käyttää sitten numeroita kaikissa toiminnoissa.

Kiinnitä erityistä huomiota tuotenumeroihin Supply Chain Managementin käyttöönoton yhteydessä. Hyvä numerointijärjestelmä parantaa logistiikkaprosesseja ja auttaa estämään virheitä. Tuotetunnuksen pitäisi yleensä olla enintään 20 merkkiä, mutta yleensä on suositeltavaa käyttää alle 10:tä merkkiä ja enintään 5:tä luokittelumerkkiä. Voit käyttää hakunimiä, mikä sallii pikahakujen käytön. Haun nimi on lisänimi, joka edustaa tuotteen luokituksia.

Kun käytät Microsoft Dataversea, Supply Chain Managementissa oleva tuotenumero on tuotenumero myös Microsoft Dataversessa. Tuotevariantit synkronoidaan Dataverseen erillisinä tuotteina.

## <a name="item-number-and-product-dimensions"></a>Nimikenumero ja tuotedimensiot

Nimiketunnus on tuotteen tunniste, jota tietty yritys käyttää. Nimikenumeron tulisi olla sama kuin tuotenumero. Jos nimikkeistö on erilainen yrityksen mukaan, tuotetta on vaikea seurata toimitusketjussa. Tällöin joudutaan myös määrittämään tuotteille uudet etiketit ja ottamaan käyttöön viiteprosessit. Tämä malli on säilytetty, koska se on yhteensopiva vanhempien versioiden kanssa (Microsoft Dynamics AX 2009 ja aiemmat versiot). Suosittelemme kuitenkin yrityskohtaisten tunnisteiden poistamista mahdollisuuksien mukaan. Ensisijaisena tunnisteena kannattaa sen sijaan käyttää yksilöivää tuotenumeroa.

Lisäksi tuotevarianttia ei voi yksilöidä nimikenumeron mukaan. Tämä vaatii aina sen nimikenumeron ja kaikkien niiden tuotedimensioiden yhdistelmän, jotka on määritetty päätuotteessa. Tämä edellytys voi muuttua raskaaksi ja hidastaa tunnistamisprosesseja. Myös tästä syystä suositteleme, että nimikenumeron sijaan käytetään yksilöivää tuotenumeroa mahdollisuuksien mukaan.

Useiden sivujen ensisijaiset tunnisteet ovat yhä nimikenumero ja tuotedimensiot. Tuotenumeroita voi kuitenkin käyttää hauissa. Voit muuttaa hakuvalintaa kohdassa **Myynti ja markkinointi** &gt; **Asetukset** &gt; **Haku** &gt; **Hakuparametrit** niin, että se käyttää ensisijaisessa hakustrategiassa tuotenumeroita nimikenumeroiden sijaan. Jos määrität **Ota tuotteiden haku käyttöön** -asetuksen arvoksi **Kyllä**, haku näyttää vain päätuotteet, ei tuotevariantteja. Lisätietoja on kohdassa [Tuotteiden ja tuotevarianttien haku tilaustenkäsittelyn aikana](search-products-product-variants.md).

Haun ja suodatuksen voi tehdä myös tuotenumeron, tuotteen nimen ja kuvauksen sekä tuotevariantin tuotedimension tunnusten mukaan. Kun valitset variantin, liittyvä nimiketunnus ja kaikki tuotedimension tunnukset valitaan. Tämä helpottaa oikean variantin etsimistä ja valitsemista. Tämä asetuksen käyttö on erittäin suositeltavaa, jos käytät tuotevariantteja ja yksilöivää tuotetunnusta tuotteiden ensisijaisina tunnisteina. Ainoa poikkeus voi olla muotiala, jossa liiketoimintaprosessien usein edellyttävät päätuotteen valitsemista ennen varianttia. Arvioi tämä vaihtoehto huolellisesti, ennen kuin otat numerointijärjestelmän käyttöön.

> [!NOTE]
> Tuotteen nimiketunnusta ei voi muuttaa, kun kyseiselle tuotteelle on olemassa yksi tai useampia tapahtumia.

## <a name="product-name-and-description"></a>Tuotteen nimi ja kuvaus

Tuotteen nimi ja kuvaus ovat tuotteen selkokielisiä tunnisteita, joita voidaan ylläpitää useilla kielillä. Supply Chain Management -asiakasohjelma näyttää oletusarvoisesti kaikki tuotetiedot oletusyrityksen kielellä, ei käyttäjän kielellä. Käännettyjä tuotenimiä ja kuvauksia käytetään kuitenkin kaikessa asiakkaiden ja toimittajien kanssa käytävässä viestinnässä. Käännökset perustuvat asiakas- ja toimittajatilien kielikoodiin.

Tuotevarianttien tuotteiden nimet voidaan luoda tuotenimikkeistömallin kautta. Koska tuotenimien ei tarvitse olla yksilöiviä, useilla tuotteilla voi olla sama nimi.

## <a name="product-and-item-search-names"></a>Tuotteiden ja nimikkeiden hakujen nimet

Supply Chain Management tarjoaa toissijaisen haun nimen tuotteille ja myös nimikkeille (vapautetut tuotteet). Tämän hakunimen ei tarvitse olla yksilöivä ja sitä voi muuttaa tuotteen tai tuotevariantin luonnin jälkeen. Tuoteluokittain tapahtuvaa hakua varten on suositeltavaa käyttää hakunimeä. Hakunimien avulla tehdä pikahakuja etenkin myynti- ja ostoprosesseissa.

Hakunimi voi sisältää myös asiakkaan tai toimittajan tuotetunnuksen tai jonkin muun ulkoisen tuotetunnuksen, jos kyseinen ulkoinen tunnus on tuotteen ensisijainen hakuehto.

## <a name="external-product-identifiers-customer-and-vendor-identifiers"></a>Ulkoiset tuotetunnukset (asiakkaan ja toimittajan tunnukset)

Voit ylläpitää vapautettujen tuotteiden niitä nimikenumeroita, nimikkeiden nimiä ja nimikkeiden kuvauksia, joita asiakas tai toimittaja käyttää. Viitteet näkyvät ulkoisissa asiakirjoissa, kuten myynti- ja ostotilauksissa sekä pakkausluetteloissa ja laskuissa. Nykyisessä Supply Chain Management -versiossa ulkoiset viitteet eivät näy ydintoimintojen sivuilla. Ainoa poikkeus on toimittajan nimiketunnus. Tämä numero näkyy **Tuotetiedot**-valintaikkunassa, jos vapautetulle tuotteelle on määritetty oletustoimittaja.

Voit ylläpitää ulkoisia tuotetunnisteita vapautetun tuotteen, vapautetun tuotevariantin, asiakkaan, asiakasryhmän, toimittajan tai toimittajaryhmän perusteella.

Seuraa **Vapautetut tuotteet** -sivulla jotakin näistä vaiheista.

- Valitse asiakkaille **Liittyvät tiedot** -ryhmän **Myynti**-välilehdessä **Ulkoinen nimikekuvaus**.
- Valitse toimittajille **Liittyvät tiedot** -ryhmän **Osto**-välilehdessä **Ulkoinen nimikekuvaus**.

Voit liittää **Ulkoiset nimikekuvaukset** -sivulla asiakkaan tai toimittajan nimikenumeron vapautettuun tuotteeseen. Tämä liitos on tehtävä jokaiselle yritykselle. Seuraavat tiedot voidaan kerätä. Nykyisen Supply Chain Management -version etiketit ovat valitettavasti hieman harhaanjohtavia. Näitä otsikoita saatetaan kuitenkin muuttaa tulevassa versiossa.

| Kenttä | Vastaavat asiakastiedot | Vastaavat toimittajatiedot |
|-------|------------------------------------|----------------------------------|
| Ulkoinen nimiketunnus | Asiakkaan nimiketunnus | Toimittajan nimiketunnus |
| kuvaus | Nimi, jonka asiakas liittää nimikkeeseen | Nimi, jonka toimittaja liittää nimikkeeseen |
| Ulkoinen nimiketeksti | Asiakkaan nimikkeen kuvaus | Toimittajan nimikkeen kuvaus |

Jos useat asiakkaat tai toimittajat käyttävät samoja nimikenumeroita (kuten ostoyhdistyksessä tai kaupparyhmässä voidaan tehdä), voit luoda asiakas- tai toimittajaryhmiä, jotka yksinkertaistavat ulkoisten tuotetietojen ylläpitämistä.

- Siirry kohtaan **Myynti** &gt; **Asetukset** &gt; **Nimikkeet** &gt; **Ulkoinen nimikekuvaus**, kun haluat luoda ja ylläpitää asiakasryhmiä ja liittyviä nimikenumeroita. Voit liittää asiakkaita ryhmään valitsemalla **Myyntireskontra** &gt; **Asiakkaat** &gt; **Kaikki asiakkaat** ja määrittämällä sitten **Oletusmyyntitilaukset**-pikavälilehdessä arvon **Nimike - asiakasryhmä** -kentässä.
- Siirry kohtaan **Hankinta** &gt; **Asetukset** &gt; **Ulkoisten nimikekuvausten ryhmä** ja luo toimittajaryhmien liittyvät nimikenumerot ja ylläpidä niitä. Voit liittää toimittajia ryhmään valitsemalla **Ostoreskontra** &gt; **Toimittajat** &gt; **Kaikki toimittajat** ja määrittämällä sitten **Oletusostotilaukset**-pikavälilehdessä arvon **Nimike - toimittajaryhmä** -kentässä.
 
## <a name="bar-codes"></a>Viivakoodit

Jos haluat käyttää viivakoodin lukijalaitetta tuotteiden tunnistamisessa, tuotetunnuksen on vastattava käytössä olevaa viivakoodistandardia. Viivakoodit ei yleensä ole tuotetunnusta sellaisenaan ja nimenomaisesti valitulle viivakooditekniikalle muodostettu tunnus. Voit ylläpitää useita viivakoodin tyyppikohtaisia viivakoodeja. Voit myös liittää saman viivakoodin useisiin tuotteisiin ja valita sitten varsinaisen aktiivisen liitoksen, kun luet viivakoodin.

Määritä vähintään yksi viivakoodiasetus, ennen kuin määrität viivakoodeja. Viivakoodiasetuksilla voi tarkistaa, että viivakoodit ovat ohjeiden mukaiset ja että ne voidaan siten tulostaa ja lukea tehokkaasti. Voit lisäksi ylläpitää myös erityisviivakoodeja tietyille tuotemäärille.

Viivakoodin määrittäminen ylläpitämään GTIN (Global Trade Item Number) tai EAN (International Article Number) -koodeja on suositeltavaa.

Voit ylläpitää viivakoodeja valitsemalla **Vapautetut tuotteet** -sivun **Varastonhallinta**-välilehden **Varasto**-ryhmässä **Viivakoodit**.

## <a name="gtin-codes"></a>GTIN-koodit

Sähköisessä kaupankäynnissä on tärkeää, että kaikki osapuolet puhuvat samaa kieltä ja viittaavat tuotteisiin samoilla tunnuksilla. Tämän vuoksi joillakin toimialoilla on käytössä [GTIN](https://www.gs1.org/id-keys/gtin), mikä on yleinen GS1:n edistämä nimiketunnusjärjestelmä.

Suosittelemme säilyttämään GTIN:n viivakoodina. Voit kuitenkin ylläpitää sitä myös **Nimike - GTIN** -sivulla. Voit avata tämän sivun valitsemalla **Vapautetut tuotteet** -sivun **Varastonhallinta**-välilehden **Varasto**-ryhmässä **GTIN-koodit**. GTIN-koodia ei ylläpidetä yleisenä numerona. Sen sijaan sitä ylläpitää yritys.

Supply Chain Managementissa määrität varastotoimintojen pakkausvariantit määrittämällä tietyn mittayksikön. Esimerkiksi nimike voidaan tallentaa kappaleina, kuuden kappaleen nippuina, 18 kappaleen lokeroissa tai kokonaisina kuormalavoina. Jokaiselle pakkausvariantille määritetään mittayksikkö. Koska GTIN liittyy yleensä tuotteen pakkausyksikköön, **Nimike - GTIN** -sivulla voi ylläpitää tuotteen ja mittayksikön useita GTIN-koodeja. Voit kuitenkin käyttää samaa GTIN-koodia vain kerran yrityksen eri nimikkeissä tai tuotevarianteissa.

Voit ylläpitää **GTIN-koodeja** valitsemalla **Vapautetut tuotteet** -sivun **Varastonhallinta**-välilehden **Varasto**-ryhmässä **GTIN**.

## <a name="external-codes"></a>Ulkoiset koodit

Ulkoisia koodia voidaan määrittää useille yksiköille. Voit esimerkiksi määrittää ulkoiset koodit, jotka yksilöivät tuotteet ja vapautetut tuotteet. Näillä ulkoisilla koodeilla voidaan liittää tilastotietojen koodeja tai arvonlisäverokoodeja vapautettuihin tuotteisiin ja vapautettuihin tuotevariantteihin. Ulkoiset koodit on määritetty yrityksen ja koodityypin mukaan. Ne on voitava yksilöidä yrityksen, koodityypin ja tauluviitteen mukaan.

Ulkoisten koodien avulla tehtävään tuotehakuun ei ole valitettavasti mitään vakiotoimintoa.

## <a name="data-entities-that-are-used-to-import-and-export-product-identifiers"></a>Tietoyksiköt, joiden avulla tuotetunnukset tuodaan ja viedään

| Yksikön nimi | Tuo tunnisteet | Vie tunnisteet | Huomautukset |
|-------------|--------------------|--------------------|----------|
| Tuotteet V2 | Tuotenumero, tuotteen haun nimi, tuotteen nimi, tuotteen kuvaus | Tuotenumero, tuotteen haun nimi, tuotteen nimi, tuotteen kuvaus | Tuotenumero voidaan luoda automaattisesti tuonnin yhteydessä tuotenumeron yksiköstä ja numerosarjasta riippuen. |
| Tuotevariantit | Tuotenumero, tuotteen haun nimi, tuotteen nimi, tuotteen kuvaus | Tuotenumero, tuotteen haun nimi, tuotteen nimi, tuotteen kuvaus | Tuotenumero voidaan luoda automaattisesti tuonnin yhteydessä tuotenimikkeistömallista riippuen. Voit kuitenkin tuoda minkä tahansa tuotenumeron. Tuotenumeron ei tarvitse noudattaa tuotenimikkeistömallin rakennetta. |
| Tuotekäännökset | Tuotteen nimi, tuotteen kuvaus | Tuotteen nimi, tuotteen kuvaus | Tämä yksikkö korvaa minkä tahansa kielen. Kun yrityksen ensisijaisen kielen kuvaus on korvattu, tuotteen nimi ja kuvaus muuttuvat. |
| Vapautetun tuotteen luominen V2 | Nimikenumero, tuotenumero, nimikkeen haun nimi| Nimikenumero, tuotenumero, nimikkeen haun nimi, tuotteen haun nimi, tuotteen nimi | Tämä yksikkö voi olla haastava, kun numerosarjoja käytetään luotaessa uusia vapautettuja tuotteita. Sekä **nimikenumeron** että **tuotenumeron** numerosarjalla on vaikutusta. **Nimikenumeron** numerosarja on yrityskohtainen, kun taas **tuotenumeron** numerosarja on yleinen. Tämän vuoksi **Nimiketunnus**-numerosarjan käyttöä ei suositella otettaessa käyttöön uusia tuotteita. Kun yksikköä käytetään aiemmin luodun tuotteen julkaisussa, yksikölle on tietysti annettava tuotenumero. Lisätietoja on tämän ohjeaiheen Tuotteiden ja nimikkeiden numerosarjat -osassa. |
| Vapautetut tuotevariantit | Nimikenumero, tuotedimensiot, tuotenumero | Tuotenumero, tuotteen haun nimi, tuotteen nimi, tuotteen kuvaus, tuotteen dimensiot | Tätä yksikköä voi käyttää **Tuotevariantit**-yksikön tapaan, kun uusia tuotteita luodaan joko tuotenimikkeistömallin seuraamista tai variantin omien tuotenumeroiden käyttämistä varten. |
| Asiakkaiden ulkoinen nimikekuvauus | Asiakkaan nimikenumero, asiakkaan nimikkeen nimi, asiakkaan kuvaus, asiakastili | Asiakkaan nimikenumero, asiakkaan nimikkeen nimi, asiakkaan kuvaus, asiakastili | Asiakkaista koostuva ryhmä (esimerkiksi ostajayhdistys) voidaan koota yhdeksi ryhmäksi **Ulkoisen nimikekuvauksen asiakasryhmät** -yksikön avulla. |
| Toimittajien ulkoinen nimikekuvaus | Toimittajan nimikkeen tunnus, toimittajan nimikkeen nimi, toimittajan kuvaus, toimittajatili | Toimittajan nimikkeen tunnus, toimittajan nimikkeen nimi, toimittajan kuvaus, toimittajatili | Toimittajista koostuva ryhmä (esimerkiksi myyntiyhdistys toimialan organisaatio) tai voidaan koota yhdeksi ryhmäksi **Ulkoisen nimikekuvauksen toimittajaryhmät** -yksikön avulla. |
| Nimikkeen viivakoodi | Viivakoodi | Viivakoodi | Tuonnin aikana on käytettävä kohdejärjestelmässä määritettyä viivakoodiasetusta. Tuodut viivakoodiviitteet tarkistetaan viivakoodiasetusten perusteella ja hylätään, jos viivakoodit eivät vastaa asetuksissa määritettyjä vaatimuksia. |
| Vapautettujen tuotteiden ulkoiset koodit | Ulkoinen koodi | Ulkoinen koodi, ulkoisten koodien luokat, nimikenumero | Ulkoiset koodit yrityksen mukaan. Tuonnissa on viitattava määritettyyn koodin luokkaan. Tuo koodiluokat **Vapautettujen tuotteiden ulkoiset koodiluokat** -yksikön avulla. |
| Vapautettujen tuotevarianttien ulkoiset koodit | Ulkoinen koodi | Ulkoinen koodi, ulkoisten koodien luokat, nimikenumero, tuotedimensiot | Ulkoiset koodit yrityksen mukaan. Tuonnissa on viitattava määritettyyn koodin luokkaan. Tuo koodiluokat **Vapautettujen tuotteiden ulkoiset koodiluokat** -yksikön avulla. Tämä yksikkö viittaa tuotevariantteihin tuotetunnuksen ja tuotedimension mukaan. |
| Vapautettujen tuotevarianttien ulkoiset koodit tuotenumeron tunnisteen mukaan | Ulkoinen koodi | Ulkoinen koodi, ulkoisten koodien luokat, tuotenumero | Ulkoiset koodit yrityksen mukaan. Tuonnissa on viitattava määritettyyn koodin luokkaan. Tuo koodiluokat **Vapautettujen tuotteiden ulkoiset koodiluokat** -yksikön avulla. Tämä yksikkö viittaa tuotevariantteihin variantin tuotetunnuksen mukaan. (Seuraavasta pääjulkaisusta) |
| GTIN | Ei käytettävissä | Ei käytettävissä | Tällä hetkellä GTIN-koodien tuontia ja vientiä varten ei ole määritettyä yksikköä. Suosituksena on sen sijaan **Nimikkeen viivakoodi** -yksiön käyttäminen. |
| Tuoteyksikön Common Data Service -tunnisteen yksikkö | Ei käytettävissä | Nimikenumero, nimikkeen haun nimi, tuotteen haun nimi, toimittajan nimikenumero, asiakkaan nimikenumero, ulkoiset koodit, GTIN-koodit, viivakoodit | Tämä yksikkö konsolidoi kaikki tunnisteen yhteen tietomalliin, jotta kaikki tunnisteet ja niihin liittyvät tyypit voidaan viedä kätevästi yhdestä liittymästä. Vie tunnistekoodit ja kuvaukset **Tuoteyksikön tunnistekoodi** -yksikön avulla. Vie vaikutusalueen lisätiedot tunnisteeseen, kuten osapuoli, yritys, määrä tai yksikkö, **Tuoteyksikön tunnisteen vaikutusalue** -yksikön avulla. |

### <a name="product-and-item-number-sequences"></a>Tuotteen ja nimikkeen numerosarjat

Voit määrittää kaksi eri numerosarjaa:

- Yleisen tuotetunnuksen **Tuotetunnus**-numerojärjestys.
- Yrityskohtaisen nimiketunnuksen **Nimiketunnus**-numerosarja

> [!NOTE]
> Käytä nimiketunnusta erillisenä tunnisteena vain, kun siirrät eri yrityksiä sellaisista erillistä lähteistä, joissa on ollut erilaiset numerointijärjestelmät. Yritä aina käyttää tuotetunnistetta, joka on yksilöivä kaikissa yrityksissä. Valitse tämän vuoksi **Nimiketunnus**-numerosarjan **Manuaalinen**-asetukseksi **Kyllä**. Näin nimikenumero seuraa tuotenumeroa luonnin yhteydessä. Jos Supply Chain Management ei ole uusien tuotenumeroiden johtava järjestelmä, määritä **Manuaalinen**-vaihtoehdon arvoksi **Kyllä** sekä **nimikenumeron** että **tuotenumeron** numerosarjoille.

Kun luot tuotteita **Vapautetut tuotteenluonnit V2** -yksiköllä, useat asetukset voivat vaikuttaa siihen, miten tuote- ja nimiketunnus luodaan numerosarjojen avulla:

- **Tuotetunnus**-numerosarjan asetukset
- **Nimiketunnus**-numerosarjan asetukset
- Nimiketunnuksen yhdistämismääritys 
- Tuotetunnuksen yhdistämismääritys

Seuraavassa taulukossa on yhteenveto tuonnin ja manuaalisen luonnin tulokset, kun käytössä on tietty numerojärjestysten ja kentän yhdistämismääritysasetusten yhdistelmä.

| Tuotenumeron numerosarja | Nimikenumeron numerosarja | Nimikenumeron yhdistämismääritys | Tuotenumeron yhdistämismääritys | Yksikön tuonnin tulos | Manuaalisen luonnin tulos | Johtopäätökset |
|--------------------------------|-----------------------------|----------------------------|-------------------------------|-------------------------|----------------------------|-----------|
| Manuaalinen = ei | Manuaalinen = ei | Ei vastaavuusmäärityksiä | Ei vastaavuusmäärityksiä | Tuotenumerot käyttävät **tuotenumeron** numerosarjaa. Nimikenumerot käyttävät **nimikenumeron** numerosarjaa. | Tuotenumerot käyttävät **tuotenumeron** numerosarjaa. Nimikenumerot käyttävät **nimikenumeron** numerosarjaa. | Tämän konfiguroinnin yhteydessä tuotenumerot noudattavat tuotenumerosarjaa, ja nimiketunnukset noudattavat nimiketunnusjärjestystä. Tämä määritys ei kuitenkaan toimi, jos tuotavia kohteita on useita (rivejä). |
| Manuaalinen = ei | Manuaalinen = kyllä | Luo automaattisesti | Ei vastaavuusmäärityksiä | Sekä tuote- että nimikenumeroissa käytetään **nimikenumeron** numerosarjaa. | Sekä tuote- että nimikenumeroissa käytetään **tuotenumeron** numerosarjaa. | Sekä tuote- että nimikenumerot seuraavat tuotenumeron numerosarjaa. Tämä on suositeltu tapa tuoda bulkkituotteet vapautetun Product Creation v2 -tietoyksikön avulla.<br><br>Voit käyttää tätä menetelmää vain, kun nimikkeitä tuodaan joukoittain (useita rivejä) ja kun et ole luomassa nimikkeitä käyttöliittymän kautta. Jos tuotteita on sekä tuotava joukkoina että luotava käyttöliittymän avulla, käytä sen sijaan tämän taulukon seuraavan rivin menettelyä. Jos haluat vaihtaa joukkotuonnista tuotteiden manuaaliseen tuomiseen ja luomiseen käyttöliittymän avulla, sinun on manuaalisesti muokattava nimikenumeron numerosarjan **Seuraava numero** vastaamaan tuotenumeron numerosarjan **Seuraavaa numeroa**. Sitten voit vaihtaa menetelmää tämän taulukon seuraavalla rivillä. |
| Manuaalinen = ei | Manuaalinen = kyllä | Ei vastaavuusmäärityksiä | Ei vastaavuusmäärityksiä | Sekä tuote- että nimikenumeroissa käytetään **tuotenumeron** numerosarjaa. | Sekä tuote- että nimikenumeroissa käytetään **tuotenumeron** numerosarjaa. | Sekä tuote- että nimikenumerot käyttävät tuotenumeron numerosarjaa. Tämä määritys ei kuitenkaan toimi, jos tuotavia kohteita on useita (rivejä).<br><br>tätä menetelmää on käytettävä, jos sinun on sekä tuotava tuotteita entiteettejä käyttäen (vain yksi rivi voidaan tuoda kerrallaan) että luotava tuotteita käyttöliittymän avulla. |
| Manuaalinen = kyllä | Ei käytettävissä | Ei käytettävissä | Luo automaattisesti | Näyttöön tulee virhesanoma, jonka mukaan numerosarjaa ei löydetä. | **Nimikenumeron** numerosarjan mukaan | Tätä asetusta ei tueta tuonnin yhteydessä. |

## <a name="product-entity-identifier-export-all-product-identifiers"></a>Tuoteyksikön tunniste (vie kaikki tuotetunnisteet)

Tuoteyksikön tunnistemalli luotiin, jotta Dataversen versio 1.0 voidaan valmistella kaikilla tuotteeseen viittaavilla tunnisteilla. Tehtävää on yksinkertaistettu keräämällä kaikki tunnisteet yhteen yleiseen tunnistetauluun, jolloin ne voidaan vietä yhtenä mallina. Huomaa, että tämä Dataversen versio ei käytä tuotetunnusten mallia. **Tuoteyksikön Common Data Service -tunnisteyksikkö** -yksiköllä ja tällä prosessilla onkin vain vähän käytännön merkitystä ja se tulee todennäköisesti muuttumaan myöhemmin.

Tuotetunnistetaulukko on yleinen taulukko, jonka tiedot täytetään kaikista pääyrityksen viitetaulukoista toistuvana erätyönä. Valitse yleisten päätietojen vaikutusalueen määritelmäksi yritys ja tuoteluokkahierarkia. Yleisen tuotetunnuksen taulun luonti on rajoitettu tuotteisiin, jotka on vapautettu valitulle yritykselle ja tuotteisiin, jotka ovat **Common data service** -roolin tuotehierarkian jäseniä tuoteluokkahierarkiassa.

Tämä prosessi olettaa, että tuotteen päätietoja ylläpidetään ensisijaisesti yhdessä keskitetyssä yrityksessä. (Tämä yritys voi kuitenkin olla virtuaalinen yritys, jota käytetään vain yleisten päätietojen ylläpitämisessä.)

Määritä ympäristö näiden ohjeiden avulla.

1. Valitse Dataversen luokkahierarkia. Jos **Luokkahierarkian rooliliitokset** -sivulla ei ole liitetty hierarkiaa **Common data service** -rooliin, sinun on luotava uusi liitos. Valitse **Common data service** -rooli ja liitä sitten Dataverseen synkronoitavaa tuotevalikoimaa edustava luokkahierarkia.
2. Valitse yleisen tuotteen päätietojen yritys. Valitse **Tuotetietojen hallintaparametrit** -sivun **Tuotemääritteet**-välilehdessä pääyritys, jossa tuotetta ja nimiketunnuksia pääasiassa ylläpidetään.
3. Määritä vietävät tunnisteen koodityypit ja koodit. Siirry kohtaan **Tuotetietojen hallinta** &gt; **Asetukset** &gt; **Tuotteen tunnistekoodit**. Voit muodostaa tunnistekoodityyppejä valitsemalla **Luo koodit**. Valitun yrityksen tunnisteen jokaiselle tyypille luodaan merkintä, jonka tyyppi on Koodi.

    Jokaiselle viivakoodiasetukselle luodaan koodin tyyppi. Jokaiselle ulkoisen koodin luokalle luodaan koodityyppi.

    Voit nyt ylläpitää koodityyppiluetteloa. Voit muuttaa koodia, nimeä tai kuvausta. Voit myös poistaa koodityyppejä. Poistettuja koodityyppejä ei käytetä yleisen tuoteyksikön tunnisteiden taulukoiden täyttämisessä.

4. Kun olet määrittänyt tuotetunnisteen koodityypit, voit luoda tunnisteita yleisessä taulussa aloittamalla **Luo tuoteyksikön tunnisteet** -työn **Tuoteyksikön tunnistekoodit** -sivulla. Tämä työ on suoritettava eränä. Tämä työ on määritettävä kausittaiseksi erätyöksi, jotta tauluun lisätään tietoja uusien tapahtumien mukaan.

Voit nyt käyttää **Tuoteyksikön Common Data Service -tunnisteen yksikkö**-, **Tuoteyksikön tunnistekoodi** ja **Tuoteyksikön tunnisteen vaikutusalue** -tietoyksiköitä ja viedä niiden avulla tunnisteita mihin tahansa kohdejärjestelmään.

## <a name="related-topic"></a>Liittyvä aihe

[Tuotteiden ja tuotevarianttien haku tilaustenkäsittelyn aikana](search-products-product-variants.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
