---
title: GS1-viivakoodit
description: Tässä aiheessa käsitellään GS1-viivakoodien ja QR-koodien määrittämistä siten, että etiketit voidaan skannata varastossa.
author: Mirzaab
ms.date: 03/21/2022
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2021-08-02
ms.dyn365.ops.version: 10.0.25
ms.openlocfilehash: ea928bc8a020035adb36ae2e7873c656e8c3985d
ms.sourcegitcommit: 1050e58e621d9a0454895ed07c286936f8c03320
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/21/2022
ms.locfileid: "8625275"
---
# <a name="gs1-bar-codes"></a>GS1-viivakoodit

[!include [banner](../includes/banner.md)]

Varastotyöntekijöiden on usein suoritettava useita tehtäviä, kun rekisteröivät nimikkeen, kuormalavan tai kontin liikkeitä mobiililaitteen skannerin avulla. Nämä tehtävät voivat sisältää sekä viivakoodien skannauksen että tietojen antamisen manuaalisesti mobiililaitteessa. Viivakoodeissa käytetään yrityskohtaista muotoa, joka määritetään ja jota hallitaan Microsoft Dynamics 365 Supply Chain Managementissa.

Osoitetarrojen GS1-viivakoodit kehitettiin tarjoamaan yleinen standardi yritysten väliseen tietojen vaihtoon. Niitä on saatavana sekä suoraviivaisina (1D) symboleina (viivakoodimuodoissa), kuten GS1-128, että 2D-symboleissa, kuten GS1 DataMatrix ja GS1 QR -koodit. Tietojen koodaamisen lisäksi GS1-viivakoodien avulla tietojen merkitys voidaan määrittää käyttämällä esimääritettyä *sovellustunnisteiden* luetteloa. GS1-standardi määritetään tietomuodon ja erilaiset tiedot, joita voidaan koodata sen avulla. Aiemmista viivakoodistandardeista poiketen GS1-viivakoodeissa voi olla useita tietoelementtejä. Niinpä yksi viivakoodiskannaus voi siepata erityyppisiä tuotetietoja, kuten erän ja vanhentumispäivän.

Supply Chain Management GS1-tuki yksinkertaistaa huomattavasti skannausprosessia varastoissa, joissa kuormalavojen ja konttien etiketeissä käytetään GS1-muotoisia viivakoodeja. Varastotyöntekijät saavat kaiken tarvittavan tiedon yhdellä GS1-viivakoodin skannauksella. Koska useita skannauksia ja/tai tietojen manuaalista antamista ei tarvita, GS1-viivakoodit auttavat lyhentämään tehtäviin kuluvaa aikaa. Samalla myös tarkkuus paranee.

Logistiikkapäälliköiden on määritettävä pakollisten sovellustunnisteiden luettelo ja liittää kukin tunniste soveltuviin mobiililaitteen valikkovaihtoehtoon. Sovellustunnisteita voidaan käyttää koko varastossa yleisenä siirto- ja pakkausasetuksena. Näin ollen kaikkien osoitetarrojen muoto on yhtenäinen.

Ellei toisin mainita, *viivakoodi* viittaa tässä aiheessa sekä lineaarisiin (1D) viivakoodeihin että 2D-viivakoodeihin.

## <a name="the-gs1-bar-code-format"></a>GS1-viivakoodin muoto

GS1:n yleiset tiedot määrittävät, mitä symbolit ovat käytössä GS1-viivakoodeissa ja miten viivakoodin tiedot koodataan. Tässä osassa on lyhyt esittely aiheeseen. Tarkempia tietoja on GS1:n julkaisuissa [GS1:n yleisissä määrityksessä](https://www.gs1.org/docs/barcodes/GS1_General_Specifications.pdf). GS1-määritysasiakirjaa päivitetään säännöllisesti, ja sen tiedot ovat ajan tasalla GS1:n yleisessä määrityksen versiossa 22.0.

GS1-viivakoodit käyttävät seuraavia symboleja:

- **Suoraviivaiset tai 1D-viivakoodit** – GS1-128 ja GS1-tietopalkki
- **2D-viivakoodit** – GS1 DataMatrix, GS1 QR-koodi ja GS1 Dotcode

Huomaa, että GS1-128:ssa on erityismaininnat GS1:stä, joka on erikoistapaus tavallisesta Code-128 lineaarisesta viivakoodista, GS1 DataMatrixista ja GS1 QR-koodista. GS1-version ja ei-GS1-version välinen ero on erityismerkki (FNC1) viivakooditietojen ensimmäisenä merkkinä. FNC1-merkki ilmaisee, että viivakoodin tietoja on tulkittava GS1-määritysten mukaisesti.

Itse viivakoodin tiedot koostuvat useista tietoelementeistä, joista jokaisella on sovelluksen tunnus kentän alussa. Yleensä tiedot esitetään myös viivakoodina luettavassa muodossa, jossa sovelluksen tunnus näytetään sulkeissa. Esimerkki: `(01) 09521101530001 (17) 210119 (10) AB-123`. Tämä viivakoodi sisältää kolme elementtiä:

- **Hakemuksen tunnus 01** – Nimikkeen GS1 yleinen kauppanimikenumero (GTIN).
- **Hakemuksen tunnus 17** – Viimeinen voimassaolopäivä.
- **Hakemuksen tunnus 10** – Eränumero.

Kunkin elementin tietojen pituus voi olla joko ennalta määritetty pituus tai muuttuva pituus. Sovellustunnusten kiinteä luettelo sisältää ennalta määritetyt pituudet. Kaikilla muilla sovellustunnuksilla on muuttuva pituus, ja GS1-sovelluksen tunnusluettelo määrittää tietojen enimmäispituuden ja muodon. Esimerkiksi sovelluksen tunnisteessa 01 on ennalta määritetty pituus 16 merkkiä (kaksi itse sovelluksen tunnisteelle ja sitten 14 GTIN:lle), ja sovelluksen tunnisteessa 17 on ennalta määrätty pituus kahdeksan merkkiä (kaksi itse sovelluksen tunnisteelle ja sitten kuusi merkkiä varten päivämäärä). Sovelluksen tunnuksella 10 on kuitenkin kaksi numeroa sovelluksen tunnukselle ja sen jälkeen enintään 20 aakkosnumeerista merkkiä.

Jos elementti seuraa muuttuvan pituuden elementtiä, on käytettävä erotinmerkkiä. Tämä erotin voi olla joko erityinen FNC1-merkki tai ryhmän erotinmerkki (ei-tulostettava merkki, jossa on ASCII-koodi 29 ja heksadesimaalikoodi 1D). Erotinta ei saa käyttää viimeisen elementin jälkeen. Vaikka erotinta ei myöskään tulisi käyttää ennalta määrätyn pituisten elementtien jälkeen, sen olemassaolo ei ole kriittinen virhe.

Viivakooditiedoissa edellisestä viivakoodin esimerkistä, joka sisältää sovellustunnisteet 01, 17 ja 10, Koodi-128-, QR-koodi- tai DataMatrix-symbolin tiedot koodataan muodossa `<FNC1>`**`01`**`09521101530001`**`17`**`210119`**`10`**`AB-123` (sovelluksen tunnukset näkyvät lihavoituna). Paras käytäntö on, että kaikki elementit, joilla on muuttuva pituus, on poistettava, jotta lisäryhmän erotinmerkkiä ei tarvita. Viivakoodilla voi kuitenkin olla myös eri elementtien järjestys, jossa erotin on pakollinen. Esimerkki: `<FNC1>`**`01`**`09521101530001`**`10`**`AB-123<GS>`**`17`**`210119`.

### <a name="dates-and-decimal-numbers"></a>Päivämäärät ja desimaaliluvut

Päivämäärät esitetään aina *VVMMDD*-muodossa, jossa vuoden päivämäärät määräytyvät GS1-tietojen mukaan. Vain päivämäärät 49 vuotta menneisyydestä 50 vuoteen tulevaisuudessa (suhteessa kuluvaan vuoteen) voidaan esittää.

Jotkin tietoelementit sisältävät desimaalilukuja. Esimerkiksi sovellustunnukset 3100, 3101, ... 3105 edustavat nettopainoa kilogrammoina. Koska näiden sovellustunnusten ennalta määritetty pituus on 10, määrää varten on käytettävissä kuusi numeroa. Desimaalipisteen sijainti määritetään sovellustunnuksen viimeisen numeron perusteella. Siksi myös tätä sovellustunnusten sukua voi edustaa *310n*. Koska GS1-vakio määrittää, että desimaalipisteen vasemmalla puolella on oltava vähintään yksi luku, enintään viisi desimaalia sallitaan.

Seuraavassa on muutamia esimerkkejä, jotka osoittavat, miten numeroita *123456* tulkitaan eri sovellustunnuksilla (lihavoituna):

- **`3100`**`123456` &rarr; 123456 (kokonaisluku)
- **`3101`**`123456` &rarr; 12345,6 (yksi desimaali)
- **`3102`**`123456` &rarr; 1234,56 (kaksi desimaalia)
- **`3103`**`123456` &rarr; 123,456 (kolme desimaalia)
- **`3104`**`123456` &rarr; 12,3456 (neljä desimaalia)
- **`3105`**`123456` &rarr; 1,23456 (viisi desimaalia)

## <a name="scanning-gs1-bar-codes-in-supply-chain-management"></a>GS1-viivakoodien skannaaminen Supply Chain Managementissa

Varastotyöntekijät käyttävät GS1-viivakoodien skannaamiseen skanneria, joka on integroitu tai liitetty matkapuhelimeen. Tämän jälkeen skanneri lähettää skannatun viivakoodin Warehouse Management -mobiilisovellukseen näppäimistön tapahtumien sarjana. Tätä käyttötilaa kutsutaan myös *näppäimistön sektoriksi* tai *sektoriksi*. Mobiilisovellus lähettää vastaanotetut tekstit Supply Chain Managementiin. Kun järjestelmä vastaanottaa syöttötiedot, se määrittää ensin, aloitetaanko tietojen alussa jokin konfiguroitu etuliite, joka ilmaisee, että tiedot ovat todellisuudessa GS1-viivakoodi (katso [Määritä yleiset GS1-asetukset](#set-gs1-options) -osa). Jos skannatut tiedot alkavat yhdellä näistä etuliitteistä, järjestelmä jäsentää tiedot GS1-jäsentimen avulla ja poimii yksittäisiä tietoelementtejä sovellustunnusten mukaan. Kun tiedot on jäsentetty, skannatut tiedot täytetään joko nykyiseen syöttökenttään tai useisiin kenttiin.

### <a name="configuration-of-bar-code-scanner-hardware-and-software"></a>Viivakoodin skannerin laitteiston ja ohjelmiston konfiguroiminen

Jotta Supply Chain Management tunnistaisi ja poistaisi GS1-viivakoodit oikein, laitteiston lukulaite tai tukiohjelmisto on määritettävä suorittamaan seuraavat toimenpiteet:

- Lisää skannattuihin viivakoodeihin etuliite, jotta järjestelmä tunnistaa GS1-viivakoodin.
- Muunna tulostettava ASCII-ryhmän erotinmerkki (ASCII-koodi 29 tai heksadesimaalikoodi 1D) tulostettavaksi merkiksi, kuten aaltoviivaksi (~).

Vaikka voit lisätä minkä tahansa etuliitteen skannattavaan viivakoodiin, yksi vaihtoehto on lisätä ISO/IEC 15424 -symbolitunnus, joka tunnetaan myös *AIM-tunnisteena*. Tämä kolmimerkkinen tunnus alkaa merkillä `]`, ja sen jälkeen sillä on yksi merkki, joka yksilöi käytetyn symbolin, ja sen jälkeen sillä on numero, jota käytetään edelleen määreenä. Esimerkiksi AIM-tunniste `]C1` määrittää koodin 128 viivakoodin (merkin `C` takia), ja muuntaja `1` määrittää, että tietojen ensimmäisessä kohdassa on FNC1-merkki. Toisaalta koodi `]C0` on koodi 128 -viivakoodi, jossa on mikä tahansa muu merkki tietojen ensimmäisenä merkkinä.

Seuraavat viisi symbolitunnusta vastaavat GS1-viivakoodeja, joissa on sovelluksen tunnuselementtejä:

- `]C1` – Koodi 128 (`C`), jossa FNC1-merkki on ensimmäisessä kohdassa (`1`), tunnetaan myös nimellä GS1-128.
- `]e0` – GS1-tietopalkki.
- `]d2` – DataMatrix (`d`), jossa on ECC 200 ja FNC1 ensimmäisessä kohdassa (`2`), tunnetaan myös nimellä GS1 DataMatrix.
- `]Q3` – QR-koodi (`Q`) Malli 2, jossa on FNC1 ensimmäisessä kohdassa (`3`), tunnetaan myös nimellä GS1 QR-koodi.
- `]J1` – GS1 DotCode.

Jos käytät näitä tunnisteita, yhteensopivuus muiden kuin GS1-viivakoodien kanssa edellyttää, että skannerit tai skannaavat ohjelmat on konfiguroitu poistamaan kaikki tunnukset, jotka eivät vastaa GS1-tunnuksia. Jos esimerkiksi skannaat "normaalin" viivakoodin 39, etuliite `]A0` lisätään. Koska järjestelmä ei ymmärrä tätä etuliitettä GS1-etuliitteenä, se tulkitsee sen tiedoksi ja tuottaa odottamattomia tuloksia.

> [!NOTE]
> Warehouse Management -mobiilisovelluksen versiosta 2.0.17.0 ja sitä myöhemmästä voidaan poistaa kaikki ne AIM-etuliitteet, jotka eivät sisälly aiempiin luetteloihin. Tämä toiminto tukee tapauksia, joissa voit määrittää skannerin lisäämään AIM-etuliitteen, mutta et poistaa ei-toivottuja etuliitteitä.

### <a name="single-and-multiple-field-scanning"></a>Yhden ja useiden kenttien skannaaminen

Kun tiedot on jäsennetty viivakoodista, ne syötetään kannettavan laitteen työnkulun ohjausobjekteihin. On olemassa kaksi menetelmää, jotka käsitellään vuorotellen:

- **Yksittäinen kentän skannaaminen** – Tämä menetelmä täyttää vain kentän, jonne viivakoodi on skannattu. Jos esimerkiksi skannaat viivakoodin `<FNC1>`**`01`**`09521101530001`**`17`**`210119`**`10`**`AB-123`, kun kohdistin on **Nimike**-kentässä, kenttään kirjoitetaan viivakoodin GTIN `09521101530001`. Jos esimerkiksi skannaat saman viivakoodin, kun kohdistin on **Erätunnus**-kentässä, kenttään kirjoitetaan erätunnus `AB-123` viivakoodista. Tämä tila toimii kaikissa työnkuluissa, ja se edellyttää vain, että yleiset GS1-asetukset on konfiguroitu. Jos viivakoodi sisältää useita elementtejä, se on skannattava useita kertoja, sillä vain yksi osa viivakoodista syötetään kerrallaan kannettavan laitteen työnkulkuun. Yleiset GS1-asetukset ohjaavat tätä toimintatapaa [yleisten GS1-määritysten määrittäminen](#generic-gs1-setup) -osassa kuvatulla tavalla.
- **Useiden kenttien skannaaminen** – Tämä menetelmä täyttää useita kenttiä yhden viivakoodin skannauksen yhteydessä työntämällä lisätietoja matkalaitteen työnkulkutilaan. Käytäntö on esimerkiksi määritetty työntämään sovelluksen tunniste 01 `ItemId`-ohjausobjektiin ja sovellustunnus 10 `InventBatchId`-kenttään. Jos skannaat viivakoodin `<FNC1>`**`01`**`09521101530001`**`17`**`210119`**`10`**`AB-123`, molempien muuttujien tietoja työnnetään samalla kertaa. Järjestelmä ei siis kysy nimikettä ja/tai eränumeroa työnkulussa. Tätä toimintaa ohjaavat GS1-käytännöt, jotka on linkitetty valikkokohtiin, kuten on kuvattu osiossa [Määritä GS1-käytännöt mobiililaitteen valikkokohtiin.](#policies-for-menus).

> [!WARNING]
> GS1-oletuskäytännöt on testattu toimimaan ilman odottamattomia toimintoja. Valikkokohteisiin linkitettyjen GS1-käytäntöjen mukauttaminen voi kuitenkin aiheuttaa odottamattomia toimintoja, koska jotkin tiedot eivät ehkä ole käytettävissä tiettyna aikana.

## <a name="turn-on-the-gs1-feature"></a>GS1-toiminnon käyttöönotto

Ennen kuin voit käyttää tätä ominaisuutta, se on otettava käyttöön järjestelmässäsi. Järjestelmänvalvojat voivat käyttää [toimintojen hallinnan](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) asetuksia ja tarkistaa toiminnon tilan sekä laittaa sen päälle tarvittaessa. **Ominaisuuksien hallinta** -työtilassa ominaisuus on luetteloitu seuraavalla tavalla:

- **Moduuli:** *Varastonhallinta*
- **Toiminnon nimi:** *GS1-viivakoodien skannaus*

### <a name="turn-on-the-enhanced-parser-for-gs1-barcodes-feature"></a>Ota GS1-viivakoodien parannettu jäsennys käyttöön

Jos käytät GS1-viivakoodeja, on suositeltavaa ottaa käyttöön myös *GS1-viivakoodien parannettu jäsentäminen* -ominaisuudet. Tämä ominaisuus parantaa GS1-viivakoodin jäsennintä. Siihen lisätään seuraavat parannukset:

- Se noudattaa GS1-yleismääritysalgoritmia symbolitietojen jäsentämiseen ja tarkistamiseen, että symbolin tiedot ovat kelvollisia määritysten mukaisesti.
- Se ei edellytä, että määrität **tunnisteen enimmäispituus** -arvon, ja se käytät pisintä etuliitevastaavuutta määritetyistä sovellustunnisteista.
- Sen avulla voit konfiguroida desimaalisovelluksen tunnukset helpommin käyttämällä kirjainta *n*, joka vastaa mitä tahansa numeroa. Voit esimerkiksi konfiguroida vain yhden sovelluksen tunnuksen (*310n*) erillisien sovellustunnusten asemesta (*3101*, *3102*, *3103* ja niin edelleen).
- Se korjaa ongelman, jossa virheellisesti koodattuja tietoja tulkitaan kenttätiedoksi.
- Se on erillinen luokka, jota voidaan käyttää uudelleen muissa konteksteissa, ja mahdollistaa sen, että laajennettavuuspisteen avulla voidaan muokata skannattuja tietoja, ennen kuin työnkulkukentät on täytetty.

## <a name="set-up-global-gs1-options"></a><a name="set-gs1-options"></a>Yleisten GS1-asetusten määrittäminen

**Varastonhallinnan parametrit** -sivulla on muutamia yleiset GS1-asetukset muodostavia asetuksia.

Yleiset GS1-asetukset määritetään seuraavasti:

1. Siirry kohtaan **Varastonhallinta \> Asetukset \> Varastonhallinnan parametrit**.
1. Määritä seuraavat kentät **Viivakoodit**-pikavälilehdessä:

    - **FNC1-merkki**, **Datamatrix-merkki** ja **QR-koodimerkki** – Määritä merkit, joita on tulkittava kunkin GS1-viivakoodityypin etuliitteenä.
    - **Ryhmän erotin** – Määritä merkki, joka korvaa ASCII-ryhmän erottimen merkin.
    - **Tunnisteen enimmäispituus** – määritä sovellustunnisteen suurin sallittu merkkimäärä. Tätä kenttää ei tarvita, jos järjestelmään on otettu käyttöön *parannettu GS1-jäsennintoiminto*.

> [!NOTE]
> Etuliitteet ilmaisevat järjestelmälle, että viivakoodi on koodattu GS1-standardin mukaisesti. Samanaikaisesti voi käyttää eri tarkoituksiin enintään kolmea etuliitettä (**FNC1-merkki**, **tietomatriisin merkki** ja **QR-koodin merkki**).

## <a name="gs1-application-identifiers"></a>GS1-sovellustunnisteet

Tietojen koodaamisen lisäksi GS1-muotojen avulla tietojen merkitys voidaan määrittää käyttämällä esimääritettyä sovellustunnisteiden luetteloa. Logistiikkapäälliköiden on määritettävä pakollisten sovellustunnisteiden luettelo ja liittää kukin tunniste soveltuviin mobiililaitteen valikkovaihtoehtoon. Tunnisteita voidaan sitten käyttää koko varastossa yleisenä siirto- ja pakkausasetuksena. Näin ollen kaikkien osoitetarrojen muoto on yhtenäinen.

Järjestelmä käyttää tietoja, etenkin esimääritettyjä sovellustunnisteita, sellaisten sääntöjen muodostamiseen, joita on käytettävä soveltuvaan skannattuun tietoon.

Kukin sovellustunniste ilmaisee järjestelmälle, että seuraavat skannatun viivakoodin merkit on katsottava salatuksi tietolohkoksi. Sovellustunnisteiden määritys määrittää, miten järjestelmä tulkitsee viivakoodin ja tallentaa sen arvona järjestelmään.

Logistiikkapäälliköt voivat käyttää kansainvälisiä vakiosovellustunnisteita ja/tai luoda omia tunnisteita.

### <a name="load-the-standard-application-identifiers"></a>Vakiosovellustunnisteiden lataaminen

Alkuun pääsee nopeasti lataamalla yleisten kansainvälisten sovellustunnisteiden luettelon. Luetteloa voi sitten tarvittaessa laajentaa tai muokata myöhemmin.

Vakiosovellustunnisteet ladataan seuraavasti:

1. Valitse **Varastonhallinta \> Määritys \> GS1 \> GS1-sovellustunnisteet**.
1. Valitse toimintoruudussa **Luo oletusasetukset**.

> [!WARNING]
> **Luo oletusasetus** -komento poistaa kaikki tällä hetkellä määritetyt sovellustunnisteet ja korvaa ne vakioluettelolla. Kun oletusasetus on ladattu, luetteloa voi kuitenkin mukauttaa tarpeen mukaan.

### <a name="set-up-custom-application-identifiers"></a>Mukautettujen sovellustunnisteiden määrittäminen

Jos jotkin tai kaikki yrityksen käyttämät sovellustunnisteet poikkeavat vakiotunnisteista, omat koodit voidaan luoda alusta alkaen tai vakiotunnisteita voidaan mukauttaa tarpeen mukaan.

Omat GS1-sovellustunnisteet määritetään tai niitä mukautetaan seuraavasti:

1. Valitse **Varastonhallinta \> Määritys \> GS1 \> GS1-sovellustunnisteet**.
1. Noudata seuraavia ohjeita:

    - Uuden tunnisteen luominen: valitse toimintoruudussa **Uusi**.
    - Aiemmin luodun tunnisteen muokkaaminen: valitse ensin tunniste ja valita sitten toimintoruudussa **Muokkaa**.

1. Määritä seuraavat uuden tai valitun tunnisteen kentät:

    - **Sovellustunniste** – Anna sovellustunnisteen tunnuskoodi. Tämä on koodi on yleensä kaksinumeroinen kokonaisluku, mutta se voi olla myös pidempi luku. Desimaaliarvoissa viimeinen numero ilmaiseen desimaalien määrän. Lisätietoja on myöhemmin tässä luettelossa **Desimaali**-valintaruudun kuvauksessa. Jos *GS1-viivakoodien parannetut jäsentimen* ominaisuudet ovat käytössä, voit luoda yksittäisen sovellustunnuksen kaikille desimaalivaihtoehtoversioille käyttämällä sovelluksen tunnuksen viimeisenä merkkinä kirjainta *n*. Voit esimerkiksi konfiguroida vain yhden sovelluksen tunnuksen (*310n*) jokaisen desimaalipaikan erillisien sovellustunnusten asemesta (*3101*, *3102*, *3103* ja niin edelleen).
    - **Kuvaus** – anna tunnisteen lyhyt kuvaus.
    - **Kiinteä pituus** – Valitse tämä valintaruutu, jos tämän sovellustunnisteen avulla skannattavilla arvoilla on kiinteä merkkimäärä. Poista tämän valintaruudun valinta, jos arvojen pituus vaihtelee. Siinä tapauksessa arvon päättyminen on ilmaistava käyttämällä **Varastonhallinnan parametrit** -sivulla määritettyä ryhmän erotinmerkkiä.
    - **Pituus** – Anna suurin merkkimäärä, jota voidaan käyttää tämän sovellustunnisteen avulla skannattavissa arvoissa. Jos **Kiinteä pituus** -valintaruutu on valittu, odotusarvona on juuri kyseinen merkkimäärä.
    - **Tyyppi** – Valitse tämän sovellustunnisteen avulla skannattavan arvon tyyppi (*numeerinen*, *aakkosnumeerinen* tai *päivämäärä*). Lisätietoja siitä, miten päivämäärät ja numerot esitetään viivakooditietoina, on [Päivämäärät ja desimaalinumerot](#dates-and-decimal-numbers) -osassa.
    - **Desimaali** – Valitse tämän valintaruutu, jos arvon katsotaan sisältävän desimaalitarkkuuden. Jos tämä ruutu valitaan, järjestelmä määrittää desimaalien määrän sovellustunnisteen viimeisen numeron perusteella. Lisätietoja siitä, miten päivämäärät ja numerot esitetään viivakooditietoina, on [Päivämäärät ja desimaalinumerot](#dates-and-decimal-numbers) -osassa.

> [!WARNING]
> Vaikka järjestelmän avulla voit määrittää minkä tahansa sovelluksen tunnuksen **kiinteän pituuden** valintaruudun, sitä tulee käyttää vain niiden sovellustunnusten osajoukolle, joiden yleisille GS1-määritykselle on määritetty pituus ennalta. Paranneltu GS1-jäsennin sisältää jo luettelon kaikista sovellustunnuksista, joilla on määritettyjä pituuksia.

> [!NOTE]
> **Warehouse managementin parametrit** -sivulla määritetty **ryhmäerottimen** arvo on valinnainen, jos sovelluksen tunnuksen jälkeen määritetyllä arvolla on kiinteä pituus.

## <a name="establish-the-generic-gs1-setup"></a><a name="generic-gs1-setup"></a>Yleisten GS1-asetusten määrittäminen

Yleisillä GS1-asetuksilla muodostetaan yleisten yhdistämismääritysten kokoelma. Nämä yhdistämismääritykset kohdistavat mobiilisovelluksen soveltuvat syöttökentät siihen sovellustunnisteeseen, joka määrittää, miten skannattujen viivakoodien kyseiseen kenttään tallennettuja arvoja tulkitaan. Oletusarvoisesti nämä asetukset koskevat kaikkien mobiililaitteen valikkovaihtoehtojen kaikkia skannauksia. Tietylle valikkovaihtoehdolle määritetty GS1-käytäntö voi kuitenkin korvata ne tietyissä kentissä.

Yleiset GS1-asetukset sallivat vain yhden arvon skannauksen kerralla. Niinpä jos yhdellä skannauksella halutaan ladata useita kentän arvoja, kyseisille valikkovaihtoehdoille on määritettävä GS1-käytäntö.

Lisätietoja GS1-käytännöistä on seuraavassa osassa.

### <a name="load-the-standard-generic-gs1-setup"></a>Yleisten GS1-vakioasetusten lataaminen

**Yleiset GS1-asetukset** -sivulla voi ladata vakiojoukon mobiililaitteen kenttien ja oletusmäärityksen luomien vakiosovellustunnisteiden välisiä yhdistämismäärityksiä.

Määritä yleiset GS1-asetukset valitsemalla **Varastonhallinta \> Määritys \> GS1 \> Yleiset GS1-asetukset**. Valitse sitten **Luo oletusasetus**, jolloin sopiva sovellustunniste määritetään automaattisesti kullekin kentälle, jota mobiililaitteen valikkovaihtoehdot tyypillisesti käyttävät.

> [!WARNING]
> Jos jokin yleinen GS1-asetus on määritetty jo aiemmin, **Luo oletusasetus** -komento poistaa sen kokonaan ja lataa vakioasetukset.

### <a name="customize-the-standard-generic-gs1-setup"></a>Yleisten GS1-vakioasetusten mukauttaminen

Yleisiä GS1-asetuksia mukautetaan seuraavasti:

1. Valitse **Varastonhallinta \> Määritys \> GS1 \> Yleiset GS1-asetukset**.
1. Noudata seuraavia ohjeita:

    - Uuden yhdistämismäärityksen luominen: valitse toimintoruudussa **Uusi**.
    - Aiemmin luodun yhdistämismäärityksen muokkaaminen: valitse ensin yhdistämismääritys ja valitse sitten toimintoruudussa **Muokkaa**.

1. Määritä seuraavat uuden tai valitun yhdistämismäärityksen kentät:

    - **Kenttä** – Valitse tai anna mobiilisovelluksen syöttökenttä, johon saapuva arvo on määritettävä. Arvo ei ole työntekijöiden näkemä näyttönimi. Sen sijaan se on sen avaimen nimi, joka on määritetty kenttään taustalla olevassa koodissa. Oletusmääritys sisältää kokoelman todennäköisesti hyödyllisiä kenttiä, ja kullakin kokoelman kentällä on intuitiivinen nimi ja vastaavat ohjelmoidut toiminnot. Omaan toteutukseen sopivista valinnoista kannattaa kuitenkin keskustella kehittäjäkumppanien kanssa.
    - **Sovellustunniste** – Valitse **GS1-sovellustunnisteet**-sivulla määritetty sopiva sovellustunniste. Tunniste määrittää, miten viivakoodia tulkitaan ja miten se tallennetaan nimetyn kentän arvona. Kun sovellustunniste on valittu, **Kuvaus**-kentässä on sen kuvaus.

## <a name="set-up-gs1-policies-to-be-to-mobile-device-menu-items"></a><a name="policies-for-menus"></a>GS1-käytäntöjen määrittäminen mobiililaitteen valikkovaihtoehtoihin

GS1-vakio tarkoitus on antaa työntekijöille mahdollisuus ladata useita arvoja, kun he skannaavat kerran yhden viivakoodin. Jotta tämä olisi mahdollista, logistiikkapäälliköiden on määritettävä GS1-käytännöt ilmoittamaan järjestelmälle, miten useita arvoja sisältäviä viivakoodeja tulkitaan. Myöhemmin mobiililaitteen valikkovaihtoehtoihin voidaan määrittää käytäntöjä ohjaamaan viivakoodin tulkintaa, kun työntekijät skannaavat sen tietyn valikkovaihtoehdon käytön yhteydessä.

Jos valikkovaihtoehdolle ei ole määritetty GS1-käytäntöä, järjestelmä voi siepata vain yhden arvon. Arvoa käytetään siihen mobiilisovelluksen syötteeseen, joka on valittuna, kun työtekijä suorittaa skannauksen yleisten GS1-asetusten määrittämällä tavalla. Jos valikkovaihtoehtoon on määritetty GS1-käytäntö, järjestelmää käyttää edelleen yleisiä GS1-asetuksia ensimmäisen viivakoodin arvon yhdistämiseen valittuun kenttään. Tämän jälkeen se voi kuitenkin siepata lisää kentän arvoja käytettävän käytännön mukaisesti.

### <a name="load-the-standard-specific-gs1-policies"></a>Tiettyjen GS1-vakiokäytäntöjen lataaminen

Alkuun pääsee nopeasti lataamalla GS1-käytäntöjoukon. Käytäntöjä voi sitten tarvittaessa laajentaa tai muokata myöhemmin.

Vakiosovellustunnisteet ladataan seuraavasti:

1. Valitse **Varastonhallinta \> Määritys \> GS1 \> GS1-käytäntö**.
1. Valitse toimintoruudussa **Luo oletusasetukset**.

> [!WARNING]
> **Luo oletusasetus** -komento poistaa kaikki tällä hetkellä määritetyt käytännöt ja korvaa ne vakiokäytäntöjoukolla. Kun oletusasetus on ladattu, käytäntöjä voi kuitenkin mukauttaa tarpeen mukaan.

### <a name="set-up-custom-specific-gs1-policies"></a>Tiettyjen GS1-käytäntöjen mukauttaminen

> [!WARNING]
> Jotkin GS1-käytännöt eivät ehkä toimi kaikkien käytössäsi olevien mobiilityönkulkujen kanssa. Kun konfiguroit mukautettuja GS1-käytäntöjä, sinun on testattava kannettavan laitteen työnkulkua käyttämällä erilaisia tietoja, jotka skannataan eri kohdissa työnkulussa. Näin voit määrittää, toimiiko työnkulku odottamallasi tavalla.

GS1-käytäntöjä määritetään ja mukautetaan seuraavasti:

1. Valitse **Varastonhallinta \> Määritys \> GS1 \> GS1-käytäntö**.
1. Noudata seuraavia ohjeita:

    - Uuden käytännön luominen: valitse toimintoruudussa **Uusi**.
    - Aiemmin luodun käytännön muokkaaminen: valitse käytäntö luetteloruudussa.

1. Määritä uuden tai valitun käytännön otsikossa seuraavat kentät:

    - **Käytännön nimi** – annan käytännön nimi.
    - **Kuvaus** – anna käytännön lyhyt kuvaus.

1. Otsikon alla on pikavälilehti, jossa kentän nimet voidaan yhdistää sovellustunnisteisiin nykyisen käytännön edellyttämällä tavalla. Lisää ja poista rivejä tarpeen mukaan työkalurivin painikkeilla. Määritä kullekin riville seuraavat kentät:

    - **Kenttä** – Valitse tai anna mobiilisovelluksen syöttökenttä, johon saapuva arvo on määritettävä. Arvo ei ole työntekijöiden näkemä näyttönimi. Sen sijaan se on sen avaimen nimi, joka on määritetty kenttään taustalla olevassa koodissa. Oletusmääritys sisältää kokoelman todennäköisesti hyödyllisiä kenttiä, ja kullakin kokoelman kentällä on intuitiivinen nimi ja vastaavat ohjelmoidut toiminnot. Omaan toteutukseen sopivista valinnoista kannattaa kuitenkin keskustella kehittäjäkumppanien kanssa.
    - **Sovellustunniste** – Valitse **GS1-sovellustunnisteet**-sivulla määritetty sopiva sovellustunniste. Tunniste määrittää, miten viivakoodia tulkitaan ja miten se tallennetaan nimetyn kentän arvona. Kun sovellustunniste on valittu, **Kuvaus**-kentässä on sen kuvaus.
    - **Lajittelu** – Kussakin moniarvoisessa viivakoodissa on sovellustunnistesarja, joista kunkin perässä on arvo. Soveltuva GS1-käytäntö määrittää, mikä sovellustunniste määritetään kuhunkin tietokantakenttään. Jos viivakoodi kuitenkin käyttää samaa sovellustunnistetta useita kertoja, järjestelmä yhdistää sovellustunnisteet kenttiin siinä järjestyksessä, jossa ne ovat koodissa. Jos rivit jakavat sovellustunnisteen vähintään yhden muun rivin kanssa, muodosta tämän kentän avulla järjestys, jossa vastaavat rivit käsitellään. Rivi, jonka lajitteluarvo on pienin, käsitellään ensimmäisenä.

> [!NOTE]
> Jos viivakoodissa halutaan käyttää useampaa kuin yhtä samaa sovellustunnistetta, kenttien järjestys *on* muodostettava **Lajittelu**-kentän avulla.

## <a name="assign-gs1-policies-to-mobile-device-menu-items"></a>GS1-käytäntöjen määrittäminen mobiililaitteen valikkovaihtoehtoihin.

Kaikissa mobiililaitteen valikkovaihtoehtoissa on oletusarvoisesti syötekentät, joissa työntekijät voivat skannata yhden arvon yleisten GS1-asetusten mukaisesti. Jos halutaan, että työntekijät voivat skannata useita kentän arvoja yhdellä mobiililaitteen valikkovaihtoehdon skannauksella, GS1-käytäntö on määritettävä seuraavasti:

1. Siirry kohtaan **Varastonhallinta \> Asetukset \> Mobiililaite \> Mobiililaitteen valikkovaihtoehdot**.
1. Luo tai avaa valikkovaihtoehto.
1. Määritä **Yleinen**-pikavälilehden **GS1-käytäntö**-kentässä käytäntö, jota käytetään valikkovaihtoehdossa.

## <a name="gs1-setup-example"></a>GS1-määritysesimerkki

Tämä esimerkki koskee järjestelmää, jossa GS1-asetukset on määritetty seuraavasti:

- **Varastonhallinnan parametrit** -sivulla on määritetty seuraavat yleiset asetukset:

    - **FNC1-merkki:** *\]C1*
    - **Ryhmäerotin:** *\~*

- Seuraavat sovellustunnisteet koskevat tätä esimerkkiä **GS1-sovellustunnisteet**-sivulla:

    | Sovellustunniste | kuvaus | Kiinteä pituus | Pituus | Laji | Desimaali |
    |---|---|---|---|---|---|
    | 01 | GTIN | Valittu | 14 | Numeerinen | Selvitetyt |
    | 10 | Eränumero | Selvitetyt | 20 | Aakkosnumeerinen | Selvitetyt |
    | 17 | Erääntymispäivä | Valittu | 6 | Päivämäärä | Selvitetyt |
    | 30 | Vastaanottava määrä | Selvitetyt | 8 | Numeerinen | Selvitetyt |

- Seuraavat **Yleiset GS1-asetukset** -sivun yleisen GS1-käytännön asetukset koskevat tätä esimerkkiä.

    | Kenttä | Sovellustunniste | kuvaus |
    |---|---|---|
    | ItemId | 01 | GTIN |

- **GS1-käytäntö**-sivulla on käytäntö, jossa **Käytännön nimi** -kentän määrityksenä on *Ostojen vastaanotto*. Tämä käytäntö sisältää seuraavat rivit:

    | Kenttä | Sovellustunniste | kuvaus | Lajittelu |
    |---|---|---|---|
    | ExpDate | 17 | Erääntymispäivä | 0 |
    | InventBatchId | 10 | Eränumero | 0 |
    | Määrä | 30 | Vastaanottava määrä | 0 |

- **Mobiililaitteen valikkovaihtoehdot** -sivulla on valikkovaihtoehto, jonka nimi on *Ostojen vastaanotto*. **GS1-käytäntö**-kentän määrityksenä on *Ostojen vastaanotto*.

Kun ostotilauksen tavarat saapuvat varastoon, työntekijä toimii seuraavasti:

1. Valitse mobiililaitteessa **Ostojen vastaanotto** -valikkovaihtoehto.
1. Anna ostotilauksen numero.
1. Valitse **Nimike**-kenttä ja skannaa seuraava viivakoodi: `]C10100000012345678~3030~10b1~17220215`.

Tätä esimerkkiä varten muodostettujen asetusten perusteella järjestelmä jäsentää skannatun viivakoodin seuraavasti:

| Kentän avain | Sovelluksen tunnus | Arvo | Seteli |
|---|---|---|---|
| ItemId | 01 | 00000012345678 | Koska työntekijä skannasi **Kohde**-kenttään, viivakoodin ensin arvo yhdistetään kyseiseen kenttään. Tämä yhdistämismääritys haetaan yleisistä GS1-asetuksista. |
| Määrä | 30 | 30 | Koska yhdellä skannauksella siepataan useita kentän arvoja, tämä yhdistämismääritys ja kaikki jäljellä olevat yhdistämismääritykset haetaan GS1-käytännöstä, joka on määritetty **Ostojen vastaanotto** -valikkovaihtoehtoon. Tämä arvo on vastaanotettu määrä. |
| InventBatchId | 10 | b1 | Tämä arvo on erän tunnus. |
| ExpDate | 17 | 220215 | Päivämäärän muoto on VVKKPP. Vanhenemispäivämäärä onkin sen vuoksi 15. helmikuuta 2022. |

Vastaanotto rekisteröidään sitten, ja soveltuvat tietokanta-arvot annetaan yhden skannauksen jälkeen.
