---
title: Suunnitteluversiot ja suunnittelun tuoteluokat
description: Tässä aiheessa käsitellään suunnitteluversiota koskevia tietoja. Suunnitteluversioilla voidaan varmistaa, että tuotteen eri tilat ja sen tiedot pysyvät ajan tasalla ja selkeinä ja että ne voidaan visualisoida järjestelmässä.
author: t-benebo
ms.date: 09/28/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EngChgLookupDynastring, EngChgProductVersionNumberRule, EngChgEcmProductRoute, EngChgEcmRequestProducts, EngChgEcmProductRoute, EngChgEcmProductPreview,EngChgEcmProductBOMItemIdLookup, EngChgEcmProductBOMConsistOf, EngChgEcmProductCreate, EngChgEcmProductLookup, EngChgProductVersionPrCompany, ngChgProductTypeLookup, EngChgProductType, EngChgProductItemPart, EngChgProductItem, EngChgEcmCategory, EngChgEcmBomDesignerEditBom, EngChgEcmBomDesigner, EngChgEcmBOMCopyDialog
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2020-09-28
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 42faa9e5f073d718c18422e37212c2ae8a28b28d
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/29/2021
ms.locfileid: "7572886"
---
# <a name="engineering-versions-and-engineering-product-categories"></a>Suunnitteluversiot ja suunnittelun tuoteluokat

[!include [banner](../includes/banner.md)]

Suunnittelutuotteet kehittyvät tuotteen elinkaaren aikana monista syistä. Muutoksilla voidaan esimerkiksi parantaa tuotteen toimivuutta, vaihtaa osa, koska se ei ole enää toimittajan valikoimassa, reagoida uusien merkityksellisten tietojen perusteella tai korjata alkuperäisen suunnitelman virheitä. On montakin syytä, miksi nämä muutokset on tallennettava keskeneräisen tuotteen osana siten, että aiempia tietoja ei korvata. Tällaisia syitä ovat esimerkiksi seuraavat:

- Halutaan säilyttää tiedot siitä, minkälainen tuote valmistettiin ja toimitettiin asiakkaille elinkaaren aiemmissa vaiheissa.
- Muutosten hyväksymiseen ja käyttämiseen tarvitaan tietty läpimenoaika.
- Jokaiseen muutokseen halutaan aikaleima ja mahdollisuus toimittaa aiemmin valmistettuja tuotteita muista versioista erillään.

*Suunnitteluversioilla* voidaan varmistaa, että tuotteen eri tilat ja sen tiedot pysyvät ajan tasalla ja selkeinä ja että ne voidaan visualisoida järjestelmässä. Tämä käsite auttaa ylläpitämään yhtenäisyyttä, lukitsemaan tuotannon tuoterakenteen, poistamaan vaihtelun ja tunnistamaan muutokset.

Yleisesti ottaen *muoto–sopivuus–toiminto*-säännön avulla voidaan määrittää, mitkä muutokset edellyttävät uutta tuotetta, uutta versiota tai aiemman version päivitystä. Kukin säännön nimessä mainittu tekijä viittaa tiettyyn osatekijään, mikä auttaa suunnittelijoita löytämään tarvetta vastaavan osan. Muoto–sopivuus–toiminto-sääntö tuo lisää joustavuutta suunnittelussa tehtäviin muutoksiin, koska osan muuttamiseen tarvitaan vain dokumentaatiota ja suunnittelukustannukset jäävät pieniksi, kunhan tuotteen sopivuus, muoto ja toiminto säilyvät ennallaan.

- **Sopivuus** viittaa osan tai ominaisuuden mahdollisuuteen muodostaa yhteys, pariliitos tai liitos kokoonpanon toisen ominaisuuden tai osan kanssa. Sopivuuden ansiosta osa on kokoonpanon toleranssirajojen mukainen, joten sitä voidaan käyttää.
- **Muoto** viittaa osan tai kokoonpanon ominaisuuksiin, kuten ulkomittoihin, painoon, kokoon tai ulkoasuun. Suunnittelijan esteettiset valinnat vaikuttavat eniten juuri muotoon. Muoto sisältää kotelon, rungon ja hallintapaneelin, jotka muodostavat tuotteen ulkoasun.
- **Toiminto** on ehto, joka toteutuu, kun osa tehokkaasti ja luotettavasti suorittaa sille määritetyn tehtävän. Esimerkiksi elektroniikkatuotteessa toiminto voi olla riippuvainen käytettävistä puolijohdekomponenteista sekä ohjelmistosta ja laiteohjelmistosta. Usein se voi olla riippuvainen myös valitun kotelon ominaisuuksista. Kaksi yleisintä syytä, miksi kotelon toimintoehto ei toteudu, on porttien virheellinen sijoittaminen tai virheellinen koko sekä harhaanjohtava tai puuttuva merkintä. 

## <a name="engineering-versions"></a>Suunnitteluversiot

Suunnittelutuotteita käytettäessä kullakin tuotteella on ainakin yksi suunnitteluversio. Ensimmäinen suunnitteluversio luodaan automaattisesti, kun suunnittelutuote luodaan. Kuhunkin suunnitteluversioon tallennetaan versiokohtaisia suunnitteluun liittyviä tietoja. Esimerkkejä tällaisista tiedoista:

- Versionumero ja edellinen versionumero (jos käytössä)
- Voimassaolon alkamis- ja päättymispäivämäärät
- Tuoteversion aktiivisuustila, mikä ilmaisee, voidaanko versio vapauttaa ja voidaanko sitä käyttää tapahtumissa (lisätietoja on kohdassa [Tuotteen valmius](product-readiness.md))
- Tuotteen luonut ja sen omistava suunnitteluyritys (lisätietoja on kohdassa [Suunnitteluyritykset ja tietojen omistussäännöt](engineering-org-data-ownership-rules.md))
- Liittyvät suunnitteluasiakirjat, kuten kokoonpano-opas, käyttöohjeet, kuvat ja linkit
- Suunnittelumääritteet (lisätietoja on kohdassa [Suunnittelumääritteet ja suunnittelumääritteiden haku](engineering-attributes-and-search.md).)
- Tekninen suunnittelutuotteiden tuoterakenne
- Prosessivalmistuksen tuotteiden mallit
- Suunnittelureitit

*Suunnittelun muutostilauksella* voidaan päivittää nämä tiedot aiemmin luodussa versiossa tai luoda uusi versio. (Lisätietoja kohdassa [Suunnittelutuotteiden muutostenhallinta](engineering-change-management.md).) Jos luot tuotteen uuden version, järjestelmä kopioi kaikki suunnitteluun liittyvät tiedot uuteen versioon. Tietoja voi sitten muokata kyseisessä uudessa versiossa. Tällä tavoin voidaan seurata tiettyjä kunkin peräkkäisen version tietoja voidaan seurata. Voit vertailla peräkkäisten suunnitteluversioiden eroja suunnittelun muutostilauksen avulla, sillä se sisältää kaikki muutokset ilmaisevat muutostyypit.

Kuten aiemmin mainittiin ensimmäinen suunnitteluversio luodaan automaattisesti, kun suunnittelutuote luodaan. Kyseisen version versionumero noudattaa tuotteen suunnitteluluokassa määritettyä versionumerosääntöä. Seuraavaan versioon siirtyminen edellyttää tuotteen lisäämistä rivinä suunnittelun muutostilaukseen, minkä lisäksi **Vaikutus**-kentän asetukseksi on määritettävä *Uusi versio*. Suunnittelun muutostilauksessa on tiedot nykyisen ja seuraavan version välisistä muutoksista.

Huomaa, että suunnittelutuote on voi olla samanaikaisesti vain yhdessä suunnittelun muutostilauksessa. Tämä rajoitus varmistaa tietojen tarkkuuden ja auttaa estämään päällekkäiset tai ristiriitaiset muutokset tuotteessa. Huomaa myös, että suunnittelun muutostilauksen **Otsikko**-näkymän **Suunnittele**-kentässä on sen suunnittelijan nimi, joka teki muutostilauksen. Jos suunnittelija on järjestelmässä määritetyn ryhmän jäsen, **Vastuunhenkilö**-kentässä on kyseisen ryhmän johtajan nimi.

## <a name="track-versions-in-transactions"></a>Versioiden seuranta tapahtumissa

Suunnittelun muutostenhallintaa käytettäessä tuotteen päätietoihin sisältyy aina vähintään yksi suunnitteluversio. Suunnittelutuotteiden asetuksissa voidaan valita, onko suunnitteluversio myös *logististen tapahtumien* osa. (Lisätietoja on jäljempänä tässä aiheessa kohdassa [Suunnittelun tuoteluokkien määrittäminen](#product-category).) Jos logistisella vaikutuksella on merkitystä, se eroaa tuote- ja yrityskohtaisesti. Joskus käytetään vain tuotteen uusinta versiota. Siinä tapauksessa uuden version ottaminen käyttöön tarkoittaa, ettei edellistä versiota voi enää käyttää. Muissa tapauksissa edellistä versiota tarvitaan logistisissa tapahtumissa seuraavien haasteiden selvittämistä varten:

- Logistiikkaosaston on lähetettävä kaksi kappaletta tuotetta asiakkaalle. Tässä tapauksessa on päätettävä, haluatko lähettää kaksi eri versiota tai sallitaanko kahden eri version lähettäminen.
- Myöhemmin havaitaan tiettyyn muutokseen liittyvä ongelma. Tässä tapauksessa saattaa on hyödyllistä selvittää tarkasti, mikä versio kussakin tilauksessa lähetettiin.
- Yritykset haluavat yleensä lähettää vanhat versiot ensin, jotta ne saadaan poistumaan varastosta. Etenkin jos tuotemäärät ovat pienet, tätä menettelyä voidaan usein hallita määrittämällä uuden version voimaantulopäivät suhteessa ennusteeseen siitä, milloin vanha versio loppuu varastosta. Tämä ei kuitenkaan ole välttämättä aina mahdollista tai varastotasoennusteita pidetään liian epävarmoina.

Päätös pitää versiot näkyvinä varastossa määräytyy eri tekijöiden mukaan, joita ovat aiemmin mainittujen seikkojen lisäksi yrityskäytäntö ja muut yrityskohtaiset huomioon otettavat seikat. *Suunnittelun tuoteluokan* toiminta voidaan määrittää. Sitä käytetään sitten kaikissa kyseissä luokassa luoduissa tuotteissa kaikissa niissä yrityksissä, joihin tuote vapautetaan.

Jos tuotteille on määritetty logistinen vaikutus, suunnitteluversio on määritettävä kullekin tapahtumalle. Vaikka järjestelmä ehdottaa *uusinta aktiivista versiota*, mikä tahansa yrityksessä käytettävissä oleva aktiivinen versio voidaan valita. Jos tuotteille ei ole määritetty logistista vaikutusta, suunnitteluversiota ei määritetä tapahtumissa. Järjestelmä käyttää kuitenkin uusinta aktiivista versiota. Kun esimerkiksi lisäät tuotteen tuotannon tuoterakenteeseen, käytetään uusinta versiota, ja kun suorita pääsuunnittelun, oletusarvona on uusin versio.

## <a name="set-up-engineering-product-categories"></a><a name="product-category"></a>Suunnittelun tuoteluokkien määrittäminen

Suunnittelun tuoteluokka muodostaa perustan luotavalle tietylle suunnittelutuotteelle. Kukin luokkaa määrittää joukon oletusarvoja ja käytäntöjä. Tämän vuoksi suunnittelutuotetta luotaessa ensimmäisenä valitaan luokka, josta se luodaan.

Huomaa, että uuden luokan hierarkiatyyppi (*suunnittelun tuotehierarkia*) määritetään automaattisesti. Voit luoda luokkia manuaalisesti valitsemalla **Suunnittelun muutostenhallinta \> Määritys \> Suunnittelun tuoteluokan tiedot**.

Kukin suunnittelun tuoteluokka määrittää kyseisen luokan perusteella luotujen suunnittelutuotteiden oletustoiminnan. Kun suunnittelutuote on luotu, sen suunnittelun tuoteluokkaa ei voi muuttaa. Jos valitset väärän luokan, voit kuitenkin poistaa tuotteen ja luoda sen sitten uudelleen.

Kun suunnittelun tuoteluokka on luotu, et voi muuttaa seuraavia asetuksia:

- Suunnitteluyritys
- Tuotetyyppi
- Tuotteen alatyyppi
- Tuotedimensioryhmä
- Määritysmenetelmä
- Versionumerosääntö

Muut asetukset saattavat periä suunnittelun tuoteluokalle määritetyt oletusarvot. Järjestelmän sääntöjen mukaan kyseisiä arvoja voi kuitenkin muuttaa.

Voit käyttää suunnittelun tuoteluokkia valitsemalla **Suunnittelun muutostenhallinta \> Määritys \> Suunnittelun tuoteluokan tiedot**. Tee sitten jokin seuraavista:

- Luo uusi luokka valitsemalla toimintoruudussa **Uusi** ja määritä sitten kentät seuraavissa alaosissa kuvatulla tavalla.
- Muokkaa aiemmin luotua luokkaa valitsemalla se luetteloruudussa ja sitten valitsemalla toimintoruudussa **Muokkaa**. Määritä sitten kentät seuraavissa alaosissa kuvatulla tavalla.
- Voit poistaa aiemmin luodun luokan valitsemalla sen luetteloruudussa ja valitsemalla sitten toimintoruudussa **Poista**.

### <a name="header"></a>Otsikko

Määritä seuraavat kentät suunnittelun tuoteluokan otsikossa.

| Kenttä | kuvaus |
|---|---|
| Nimi | Anna suunnittelun tuoteluokalle nimi. |
| Suunnitteluyritys | Valitse suunnitteluyritys, jossa tämän suunnittelun tuoteluokan tuotteet voidaan luoda ja missä niitä ylläpidetään. |

### <a name="details-fasttab"></a>Tiedot-pikavälilehti

Määritä seuraavat kentät suunnittelun tuoteluokan **Tiedot**-pikavalikossa.

| Kenttä | kuvaus |
|---|---|
| Tuotetyyppi | Valitse, koskeeko luokka tuotteita vai palveluita. |
| Tuotantolaji | Tämä kenttä on näkyvissä vain, kun olet ottanut [kaavan muutoksen hallinnan](manage-formula-changes.md) käyttöön järjestelmässä. Valitse tuotannon tyyppi, jota tämä tekninen tuoteluokka koskee:<ul><li>**Suunnittelunimike** – Tämän suunnitteluluokan avulla voit tehdä kaavan muutoksen hallinnan suunnittelunimikkeille. Suunnittelunimikkeissä käytetään kaavoja. Ne muistuttavat kaavanimikkeitä, mutta niitä käytetään vain oheistuotteiden ja sivutuotteiden, ei valmiiden tuotteiden tuottamiseen. Kaavaa käytetään prosessivalmistuksen aikana.</li><li>**Tuoterakenne** – Tämän suunnitteluluokan avulla voit hallita suunnittelutuotteita, jotka eivät käytä kaavoja ja jotka tavallisesti (mutta eivät välttämättä) sisältävät tuoterakenteita.</li><li>**Kaava** – Tämän suunnitteluluokan avulla voit tehdä kaavan muutoksen hallinnan valmiille tuotteille. Näillä nimikkeillä on kaava, mutta ei tuoterakennetta. Kaavaa käytetään prosessivalmistuksen aikana.</li></ul> |
| Todellinen paino | Tämä vaihtoehto on näkyvissä vain, kun olet ottanut [kaavan muutoksen hallinnan](manage-formula-changes.md) käyttöön järjestelmässä. Se on käytettävissä vain, kun **tuotantotyyppi**-kentän arvoksi on määritetty *Suunnittelunimike* tai *Kaava*. Valitse tämä vaihtoehto *Kyllä*, jos käytät tätä suunnitteluluokkaa nimikkeiden hallintaan, jotka edellyttävät todellisen painon tukea. |
| Versioiden seuranta tapahtumissa | Valitse, leimataanko tuotteen versio kaikkiin tapahtumiin (logistinen vaikutus). Jos versiota esimerkiksi seurataan tapahtumissa, kussakin myyntitilauksessa näkyy, mikä tuotteen versio myyntiin kyseisessä myyntitilauksessa. Jos tapahtumia ei seurata tapahtumissa, myyntitilauksissa ei näy, mikä versio myytiin. Niissä näkyy sen sijaan aina uusin versio.<ul><li>Jos kyseisenä asetuksena on *Kyllä*, tuotteelle luodaan päätuote ja tuotteen kukin versio on variantti, joka käyttää *version* tuotedimensiota. **Tuotteen alatyyppi** -kentän asetuksena on automaattisesti *Päätuote* ja **Tuotedimensioryhmä**-kentässä on valittava tuotedimensioryhmä, jossa *version dimensio* on aktiivinen. Vain ne tuotedimensioryhmät, jossa *versio* on aktiivinen dimensio, näytetään. Voit luoda uusia tuotedimensioryhmiä valitsemalla **Muokkaa**-painikkeen (kynäsymboli).</li><li>Jos tähän asetukseen on määritetty *Ei*, *version* tuotedimensiota ei käytetä. Voit sitten valita, luodaanko muita dimensioita käyttävä tuote tai päätuote.</li></ul><p>Tätä asetusta käytetään usein tuotteissa, joissa versioiden kustannusten välillä on ero, tai tuotteissa, joissa käytetään erilaisia ehtoja suhteessa asiakkaaseen. Tämän vuoksi on tärkeää ilmaista, mitä versiota käytetään kussakin tapahtumassa.</p> |
| Tuotteen alatyyppi | Valitse, sisältääkö luokka tuotteita vai päätuotteita. Päätuotteissa käytetään tuotedimensioita.
| Tuotedimensioryhmä | **Version seuranta tapahtumissa** -asetuksella voidaan valita tuotteen dimensioryhmä. Jos version seuranta tapahtumissa on määritetty, tuotedimensioryhmät, joissa käytetään *version* dimensioita, näytetään. Muussa tapauksessa vain ne tuotedimensioryhmät, joissa *versio* ei ole aktiivinen dimensio, näytetään. |
| Tuotteen elinkaaren tila luotaessa | Määritä oletusarvoinen tuotteen elinkaaren tila, joka suunnitelmatuotteella on, kun se luodaan ensimmäisen kerran. Lisätietoja on kohdassa [Tuotteen elinkaaren tilat ja tapahtumat](product-lifecycle-state-transactions.md). |
| Versionumerosääntö | Valitse luokkaa koskeva versionumerosääntö:<ul><li>**Manuaalinen** – valitse kunkin uuden version versionumero.</li><li>**Automaattinen** – Järjestelmä määrittää versionumeron määritetyn muodon perusteella. Käytä muodon määrittämisestä numeromerkkiä (\#) ilmaisemaan numeron ja muut merkit, jotka ilmaisevat vakioarvon. Jos muodosti määritetään esimerkiksi *V-\#\#*, ensimmäinen versio on V-01, toinen versio on V-02 ja niin edelleen.</li><li>**Luettelo** – järjestelmä hakee seuraavan numeron määritettyjen mukautettujen arvojen esimääritetystä luettelosta.</li></ul> |
| Pakota voimassaolo | Valitse, onko suunnitteluversioiden voimassaolopäivämäärien oltava peräkkäisiä tai voiko niiden välillä olla aukkoja ja päällekkäisyyksiä. Tämä asetus vaikuttaa tapaan, jolla kunkin sellaisen suunnitteluversion **Voimassaolo alkaa**- ja **Voimassaolo päättyy** -kenttää käytetään, jota luokka koskee.<ul><li>Jos tämän asetuksen arvo on *Kyllä*, **Voimassaolo alkaa** -arvo on määritettävä kullekin versiolle eikä versioiden välillä saa olla päällekkäisyyksiä tai aukkoja. Kun suunnitteluversion päivämääräalue yhdistetään suoraan edelliseen ja seuraavaan suunnitteluversioon, jos sellaiset ovat olemassa. Tässä skenaariossa käytetään aina uusinta versiota eikä vanhoja versioita enää käytetä.</li><li>Jos tämän vaihtoehdon asetuksena on **Ei**, suunnitteluversioiden voimassaolon alkamispäivämääräkentillä ei ole rajoituksia ja sekä päällekkäisyydet ja aukot sallitaan. Tässä skenaariossa useita versioita voi olla aktiivisena samanaikaisesti ja mitä tahansa aktiivista versiota voi käyttää.</li></ul><p>Tämä vaihtoehto vaikuttaa myös tuoterakenteisiin ja reitteihin, jotka on yhdistetty tuoteversioon. Lisätietoja on jäljempänä tämän aiheen kohdassa [Tuoterakenteiden ja reittien yhdistäminen suunnitteluversioihin](#boms-routes).</p> |
| Käytä numeron säännön nimikkeistöä | Määrittämällä tämän vaihtoehdon asetukseksi *Kyllä* voit ottaa käyttöön säännöt, joilla tuotenumero määritetään käyttämällä numerosarjoja, suunnittelumääritteen nimiä ja arvoja sekä tekstivakioita segmentteinä. Voit luoda tai muokata sääntöjä valitsemalla **Muokkaa**-painike. |
| Käytä nimen säännön nimikkeistöä | Määrittämällä tämän vaihtoehdon asetukseksi *Kyllä* voit ottaa käyttöön säännöt, joilla nimi määritetään käyttämällä suunnittelumääritteen nimiä ja arvoja sekä tekstivakioita segmentteinä. Voit luoda tai muokata sääntöjä valitsemalla **Muokkaa**-painike. |
| Käytä kuvauksen säännön nimikkeistöä | Määrittämällä tämän vaihtoehdon asetukseksi *Kyllä* voit ottaa käyttöön säännöt, joilla kuvaus määritetään käyttämällä suunnittelumääritteen nimiä ja arvoja sekä tekstivakioita segmentteinä. Voit luoda tai muokata sääntöjä valitsemalla **Muokkaa**-painike. |

### <a name="attributes-fasttab"></a>Määritteet-pikavälilehti

Määritä **Määritteet**-pikavälilehden ruudukossa suunnittelumääritteet, joita käytetään tähän luokkaan kuuluviin tuotteisiin. Lisätietoja suunnittelumääritteiden luomisesta on kohdassa [Suunnittelumääritteet ja suunnittelumääritteiden haku](engineering-attributes-and-search.md).

**Määritteet**-pikavälilehden painikkeilla voi lisätä, poistaa ja järjestelmää ruudukon määritteitä.

Jos suunnitteluluokan määritevalintaa muutetaan ja kyseiseen luokkaan perustuvia tuotteita on jo olemassa, sinun on päätettävä, käytetäänkö muutoksia kyseisissä tuotteissa. Jos haluat käyttää muutoksia aiemmin luoduissa tuotteissa, valitse **Päivitä aiemmin luodut tuotteet** **Määritteet**-pikavälilehdessä.

Määritä seuraavat kentät jokaiselle ruudukkoon lisättävälle riville.

| Kenttä | kuvaus |
|---|---|
| Nimi | Valitse lisättävä määrite. |
| Arvo | Valitse määritteen oletusarvo. |
| Pakollinen | Jos *Totuusarvo*-tyypin määritteiden asetuksena on *Kyllä*, käyttäjien on määritettävä määritteen asetukseksi *Kyllä*. Jos tämän vaihtoehdon asetuksen on *Ei*, käyttäjät voivat määrittää määritteen asetukseksi *Kyllä* tai *Ei*. Muissa tietotyypissä tämän vaihtoehdon asetus on vain tiedoksi. |
| Erämäärite | Valitse, levitetäänkö määrite erätoiminnolla. |

### <a name="readiness-policy-fasttab"></a>Valmiuskäytäntö-pikavälilehti

Valitse **Tuotteen valmiuskäytäntö** -kentän avulla valmiuskäytäntö, jota tulisi soveltaa tämän suunnitteluluokan perusteella luotuihin tuotteisiin. Lisätietoja on kohdassa [Tuotteen valmius](product-readiness.md).

> [!NOTE]
> **Tuotteen valmiuskäytäntö** -kenttä toimii hieman eri tavalla, jos olet ottanut järjestelmän *Tuotteen valmiustarkistus* -ominaisuuden käyttöön. (Tämän toiminnon avulla voit ottaa käyttöön valmiuskäytännöt vakiomuotoisiin \[ei-suunnittelu\]-tuotteisiin). Lisätietoja on kohdassa [Vakio- ja suunnittelutuotteiden valmiuskäytäntöjen määrittäminen](product-readiness.md#assign-policy).

### <a name="release-policy-fasttab"></a>Vapautuskäytäntö-pikavälilehti

**Tuotteen vapautuskäytäntö** -kentässä valitaan tähän luokkaan kuuluvien tuotteiden vapautuskäytäntö. Lisätietoja on kohdassa [Tuoterakenteiden vapauttaminen](release-product-structure.md).

## <a name="connect-boms-and-routes-to-engineering-versions"></a><a name="boms-routes"></a>Tuoterakenteiden ja reittien yhdistäminen suunnitteluversioihin

**Pakotettu voimassaolo** -asetuksen määrittäminen on tärkeää yhdistettäessä tuoterakenteet ja reitit kuhunkin suunnitteluversioon. Voit aktivoida useita tuoterakenteita ja reittejä tuotekohtaisesti vain, jos jossakin seuraavista asetuksissa on ero:

- Tuotedimensio
- Määrä
- Toimipaikka
- Voimassaolopäivät

Suunnittelun tuoterakenteet ja reitit luodaan suunnitteluversiosta, jossa niitä käytetään. Ne tunnistetaan siitä, että **Suunnitteluohjattu**-valintaruudussa on valintamerkki. Suunnittelun tuoterakennetta ja reittejä käytettäessä niitä ei yleensä suunnitella käyttämällä eri määriä. Erilaisia tuoterakenteita ei myöskään tyypillisesti suunnitella toimipaikkakohtaisesti. Lisäksi suunnittelun tuoterakenteiden ja reittien voimassaolopäivämäärä haetaan aina suunnitteluversiosta. Tämän vuoksi suunnitteluversiolla, sen tuoterakenteella ja sen reiteillä on samat voimassaolopäivät.

Tuotteissa, joissa käytetään *version* tuotedimensiota (yhdessä tapahtumien logistisen vaikutuksen kanssa), versio lisätään myös tuoterakenteisiin ja reitteihin. Tämä toiminta auttaa erottamaan peräkkäisten versioiden tuoterakenteet ja reitit **Pakotettu voimassaolo** -asetuksesta riippumatta.

Tuotteissa, joissa ei käytetä *version* tuotedimensiota (ilman tapahtumien logistista vaikutusta), versiota ei lisätä tuoterakenteisiin tai reitteihin. Niinpä peräkkäisten tuoterakenteiden ja reittien välillä ei ole eroa. Tässä tapauksessa **Pakotettu voimassaolo** -asetukseksi kannattaa määrittää *Kyllä*. Tällä tavoin voit estää päällekkäiset suunnitteluversiot ja voit myös aktivoida uuden version tuoterakenteen ja reitin ilman, että edellisen version tuoterakenteen ja reitin aktivointi olisi ensin poistettava. Jos **Pakotettu voimassaolo** -asetuksena on *Kyllä*, siinä tapauksessa vanhojen versioiden tuoterakenteiden ja reittien aktivointi on poistettava manuaalisesti ennen uusimman version aktivointia.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
