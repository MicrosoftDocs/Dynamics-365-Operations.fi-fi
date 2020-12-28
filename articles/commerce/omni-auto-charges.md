---
title: Monikanavaiset edistyneet automaattiset kulut
description: Tässä ohjeaiheessa käsitellään Commerce-kanavan tilausten lisäkulujen hallintaa edistyneiden automaattisten kuluominaisuuksien avulla.
author: hhaines
manager: annbe
ms.date: 03/30/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: hhaines
ms.search.validFrom: ''
ms.dyn365.ops.version: 10
ms.openlocfilehash: 2d463bf01659aeb6599023ce46da0c604f8eeff0
ms.sourcegitcommit: 4c6d31f3ebd88212d3d1497a4bba9c64c5300444
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/24/2020
ms.locfileid: "4412121"
---
# <a name="omni-channel-advanced-auto-charges"></a>Omnikanavan automaattiset etukäteisveloitukset

[!include [banner](includes/banner.md)]

Tässä ohjeaiheessa on tietoja edistyneiden automaattisten kulujen määrittämisestä ja käyttöönottamisesta. Nämä ominaisuudet ovat käytössä Dynamics 365 for Retailin versiossa 10.0.

Kun edistyneet automaattiset kuluominaisuudet on otettu käyttöön, missä tahansa tuetussa Commerce-kanavassa (myyntipiste, puhelinkeskus tai verkko) luoduissa tilauksissa voi käyttää [automaattisten kulujen](https://docs.microsoft.com/dynamics365/unified-operations/retail/configure-call-center-delivery#define-charges-for-delivery-services) määrityksiä, jotka on määritetty ERP-sovelluksessa otsikko- ja rivitason kuluille.

Retailin versiota 10.0 edeltävissä versioissa [automaattisen kulun](https://docs.microsoft.com/dynamics365/unified-operations/retail/configure-call-center-delivery#define-charges-for-delivery-services) määrityksiä voitiin käyttää vain sähköisessä kaupankäynti- ja puhelinkeskuskanavissa. Versiosta 10.0 alkaen myyntipisteessä luoduissa tilauksissa voidaan käyttää automaattisten kulujen määrityksiä. Tällöin tavoin sekalaiset lisäkulut voi lisätä järjestelmällisesti myyntitapahtumiin.

Kun käytössä on versiota 10.0 edeltävä versio, myyntipistekäyttäjää pyydetään lisäämään toimitusmaksu manuaalisesti myyntipisteen Lähetä kaikki- tai Lähetä valitut -tapahtuma. Vaikka sovelluksen muiden kulujen toimintoja käytetään kulujen kirjoittamiseen tilaukseen, mikään järjestelmällinen laskenta ei ole käytettävissä, sillä laskenta määrittää kulujen arvon käyttäjän antamien tietojen perusteella. Kulut voidaan lisätä vain yhtä lähetykseen liittyvänä kulukoodina eikä niitä voi juurikaan muokata tai muuttaa myyntipisteessä sen jälkeen, kun ne on luotu.

Lähetyskulujen lisäämiskehotuksia voi edelleen käyttää versiossa 10.0 ja sitä uudemmissa versioissa. Jos organisaatio ei ota **Edistyneet automaattiset kulut** -parametria käyttöön, myyntipisteen manuaalisen kulujen antamiskehotteet pysyvät entisellään.

Edistyneen automaattisen kuluominaisuuden ansiosta myyntipistekäyttäjät saavat käyttöönsä järjestelmälliset, automaattisiin kulujen määritystaulukoihin perustuvat laskutoimitukset kaikille määritetyille muille kuluille. Käyttäjät voivat myös lisätä tai muokata rajoittamatonta määrää lisäkuluja ja -maksuja minkä tahansa myyntipisteen myyntitapahtuman otsikko- tai rivitasolla (kun kyse on itsepalvelutukku- tai asiakastilauksesta).

## <a name="enabling-advanced-auto-charges"></a>Edistyneiden automaattisten kulujen ottaminen käyttöön

Valitse **Retail ja Commerce \> Pääkonttorin asetukset \> Parametrit \> Commercen parametrit** -sivulla **Asiakastilaukset**-välilehti. Määritä **Kulut**-pikavälilehdessä **Käytä edistyneitä automaattisia kuluja** -asetukseksi **Kyllä**.

![Edistyneet automaattiset kulut -parametri](media/advancedchargesparameter.png)

Kun edistyneet automaattiset kulut on otettu käyttöön, käyttäjiä ei enää pyydetä lisäämään lähetyskulua manuaalisesti kassapäätteessä Lähetä kaikille- tai Lähetä valituilla -asiakastilausta luotaessa. Myyntipisteen tilauskulut lasketaan ja lisätään järjestelmällisesti myyntipistetapahtumaan (jos luotavan tilauksen ehtoa vastaava automaattisten kulujen taulukko löytyy). Käyttäjät voivat lisätä tai ylläpitää otsikko- tai rivitason kuluja myös manuaalisesti juuri lisättyjen myyntipisteen toimintojen kautta. Tämä ominaisuus voidaan lisätä myyntipisteen näyttöasetteluihin.

Kun edistyneet automaattiset kulut on otettu käyttöön, aiemmin luotuja **kuljetusmaksukoodin** ja **palautettavien toimitusmaksujen** **Commercen parametreja** ei enää käytetä. Näitä parametreja käytetään vain, jos **Käytä edistyneitä automaattisia kuluja** -parametrin asetuksena on **Ei**.

Varmista ennen tämän ominaisuuden käyttöönottoa, että olet testannut toimintoa ja kouluttanut työntekijät, sillä käyttöön otettu ominaisuus muuttaa liiketoimintaprosessia, jolla toimituskulut ja muut kulut lasketaan ja lisätään myyntipisteen myyntitilauksiin. Varmista, että tiedät, miten prosessi vaikuttaa tapahtumien luontiin myyntipisteestä. Edistyneiden automaattisten kulujen käyttöönottaminen ei juurikaan vaikuta puhelinkeskuksen ja sähköisen kaupankäynnin tilauksiin. Puhelinkeskuksen ja sähköisen kaupankäynnin sovellukset toimivat samalla tavalla kuin aiemminkin, kun kyse on tilauksen lisämaksujen laskemisesta automaattisen kulutaulukoiden avulla. Puhelinkeskuskanavan käyttäjät voivat jatkossakin muokata manuaalisesti mitä tahansa järjestelmän laskemaa automaattista kulua otsikko- tai rivitasolla tai lisätä manuaalisesti muita kuluja otsikko- ja rivitasolla.

## <a name="additional-pos-operations"></a>Myyntipisteen lisätyövaiheet

Edistyneet automaattiset kulut toimivat myyntipistesovelluksessa odotustenmukaisesti vain, jos myyntipisteen uudet työvaiheet on lisätty. Nämä työvaiheet on lisättävä [myyntipisteen näyttöasetteluihin](https://docs.microsoft.com/dynamics365/unified-operations/retail/pos-screen-layouts) ja otettava käyttöön myyntipistelaitteissa, kun edistyneet automaattiset kulut otetaan käyttöön. Jos näitä työvaiheita ei lisätä, käyttäjät eivät voi hallita eivätkä ylläpitää muita kuluja myyntipistetapahtumissa. He eivät voi myöskään muokata eivätkä muuttaa niiden kulujen arvoja, jotka lasketaan järjestelmällisesti automaattisten kulujen määritysten perusteella. Tämän vuoksi ainakin **Kulujen hallinta** -työvaihe on syytä ottaa käyttöön myyntipisteen asettelussa.

Uudet työvaiheet:

- **142 – Kulujen hallinta** – Myyntipistekäyttäjät voivat tarkastella ja muokata tämän työvaiheen avulla myyntipisteen tapahtuman muita kuluja, jotka lisättiin joko manuaalisesti tai järjestelmällisesti automaattisten kulujen laskennan kautta.
- **141 – Lisää otsikon kulut** – Käyttäjä voi lisätä tällä työvaiheella otsikkotason muun kulun manuaalisesti mihin tahansa myyntipisteen myyntitapahtumaan (ja valita käytettävän kulukoodin).
- **140 – Lisää rivin kulut** – Käyttäjä voi lisätä tällä työvaiheella rivitason muun kulun manuaalisesti mille tahansa myyntipisteen myyntiriville (ja valita käytettävän kulukoodin).
- **143 – Laske kulut uudelleen** – Tällä työvaiheella voi laskea myyntitapahtuman kulut kokonaisuudessaan uudelleen. Käyttäjän aiemmin mahdollisesti korvaavat automaattiset kulut lasketaan uudelleen nykyisen ostoskorimäärityksen perusteella.

Kuten muissakin myyntipisteen työvaiheissa suojausmääritysten avulla on mahdollista edellyttää esimiehen hyväksyntää ennen työvaiheen suorittamista.

On tärkeää huomata, että edellä mainitut myyntipistetoiminnot voidaan lisätä myyntipisteasetteluun myös silloin, kun **Käytä edistyneitä automaattisia kuluja** -parametri on poistettu käytöstä. Tässä skenaariossa organisaatiot saavat lisäetua siitä, että ne voivat tarkastella manuaalisesti lisättyjä kuluja ja muokata niitä **Kulujen hallinta** -toiminnolla. Käyttäjät voivat käyttää myös myyntipistetapahtumien **Lisää otsikon kulut**- ja **Lisää rivin kulut** -toimintoja, kun **Käytä edistyneitä automaattisia kuluja** -parametri on poistettu käytöstä. **Laske kulut uudelleen** -toiminto ei ole yhtä hyödyllinen, jos sitä käytetään, kun **Käytä edistyneitä automaattisia kuluja** on poistettu käytöstä. Tässä skenaariossa mitään ei laskettaisi uudelleen ja tapahtumaan manuaalisesti lisättyjen kulujen arvoksi palautuisi 0,00 $.

## <a name="use-case-examples"></a>Esimerkkejä käyttötapauksista

Tämän osan esimerkkitapaukset auttavat hahmottamaan automaattisten kulujen ja muiden kulujen määrityksiä ja käyttöä Commerce-kanavatilausten yhteydessä. Nämä esimerkit näyttävät, miten sovellus toimii, kun **Käytä edistyneitä automaattisia kuluja** -parametri on otettu käyttöön.

### <a name="auto-charges-header-charges-example"></a>Automaattisten kulujen otsikon kulujen esimerkki

#### <a name="use-case-scenario"></a>Käyttötapausskenaario

Jälleenmyyjä haluaa lisätä rahtikulut automaattisesti, kun tapahtumat luodaan jossain Commerce-kanavassa, jossa tuotteet on lähetettävä asiakkaalle. Jälleenmyyjä antaa kaksi toimitusvaihtoehto: maakuljetus ja lentorahti. Jos asiakas valitsee maakuljetuksen ja tilauksen arvo on alle 100 dollaria, jälleenmyyjä halua veloittaa asiakkaalta rahtikuluna 10 dollaria. Jos tilauksen arvo on yli 100 dollaria ja asiakas valitsee maakuljetuksen, asiakkaalta ei veloiteta rahtikuluja. Jos asiakas valitsee kaikkien tilausten toimitustavaksi lentorahdin, rahtikuluna veloitetaan kokonaisarvosta riippumatta 20,00 dollaria.

#### <a name="setup-and-configuration"></a>Asetukset ja määrittäminen

Tämä skenaario edellyttää kahden automaattisten kulujen taulukon määrittämistä.

Valitse **Myyntireskontra \> Kulujen määritys \> Automaattiset kulut**.

Määritä kaksi erilaista otsikkotason automaattista kulua. Määritä toinen maakuljetukselle ja toinen lentorahdille. Määritä tässä skenaariossa, että niitä käytetään kaikille asiakkaille.

Määritä maakuljetuksen toimituskuluiksi **Automaattiset kulut** -sivun riviosassa kulu, jota käytetään, kun tilauksen arvo on 0,01–100 dollaria. Tässä tapauksessa toimituskuluksi määritetään 10,00 dollaria. Luo toinen kulurivi ilmaisemaan, että tilauksilla, joiden arvo on yli 100,01 dollaria, ei ole kuluja.

![Esimerkki kahdesta automaattisesta veloitustaulukosta](media/headerchargesexample.png)

Määritä lentorahdin toimituskuluiksi automaattisten kulujen lomakkeessa 20 dollaria. Tätä kulua käytetään kaikissa tilauksissa (joiden arvo 0,01–9 999 999 dollaria).

Lähetä muutokset Commercen asteikkoyksikköön/kanavatietokantaan, jotta myyntipiste voi käyttää niitä suorittamalla **1040 jakeluaikataulu** -työn.

#### <a name="sales-processing-for-this-scenario"></a>Myynnin käsittely tässä skenaariossa

Kun edellä mainitut määritysvaiheet on tehty ja muutokset on otettu käyttöön kanavatietokannassa, mikä tahansa myyntipiste-, puhelinkeskus- tai sähköinen kaupankäynti -kanavassa luotu asiakastilaus tai myyntitapahtuma, jonka toimitustavaksi on määritetty maakuljetus tai lentorahti otsikkotasolla, hyödyntää näitä kuluja ja käyttää niitä automaattisesti myyntiin.

Tällä hetkellä kuluja käytetään kaikissa myyntitapahtumissa, jotka on luotu näitä toimitustapoja käyttävässä yrityksessä, sillä millään toiminnolla ei voi määrittää, että automaattisen kulun määritystä käytetään vain tietyssä myyntikanavassa.

Myyntipisteen ja sähköisen kaupankäynnin skenaarioissa näissä tilauksissa ei ole selkeästi määritettyä otsikkoa, joten otsikkotason kuluja käytetään vain, jos kaikki tapahtuman myyntirivit on määritetty toimitettavaksi täsmälleen samalla toimitustavalla. Jos myyntipisteessä tai sähköisen kaupankäynnissä luoduissa tapahtumissa on yhdistelmätoimituksia, vain rivitason automaattiset kulut otetaan huomioon ja vain niitä käytetään.

Puhelinkeskusskenaarioissa käyttäjä voi hallitta toimitustapa-asetusta otsikkotasolla, joten otsikkotason kuluja käytetään näissä tilauksissa, vaikka jotkin myyntirivit olisi määritetty käyttämään toista toimitustapaa. Puhelinkeskustilausten otsikkotason kulut perustuvat aina siihen toimitustapaan, joka on määritetty myyntitilauksen tilausotsikkotasolla.

### <a name="auto-charges-line-charges-example"></a>Automaattisten kulujen rivin kulujen esimerkki

#### <a name="use-case-scenario"></a>Käyttötapausskenaario 

Jälleenmyyjä halua lisätä asiakkaalle lisäkulun asennuskuluiksi, kun asiakas ostaa tietyn mallisen tietokoneen. Tämä tietokone edellyttää pakollisia lisäasennuksia, jotka jälleenmyyjä tekee asiakkaalle. Jälleenmyyjä on ilmoittanut asiakkaalle, että tämän asennuksen vuoksi käytössä on lisämaksu. Jälleenmyyjä haluaa hallita tähän maksuun liittyviä kuluja erillään tuotteen myyntihinnasta taloushallinnon raportoinnin vuoksi. 19,99 dollarin asennusmaksu veloitetaan asiakkaalta, kun tämä kyseinen tietokone ostetaan missä tahansa kanavassa.

#### <a name="setup-and-configuration"></a>Asetukset ja määrittäminen

Tämä skenaario edellyttää yhden rivitason automaattisten kulujen taulukon määrittämistä.

Valitse **Myyntireskontra \> Kulujen määritys \> Automaattiset kulut**.

Valitse avattavassa **Taso**-valikossa **Rivi** ja uusi automaattisten kulujen tietue, joka koskee kaikkia asiakkaita sekä tiettyä tuotetta tai tuoteryhmää, jossa asennusmaksut veloitetaan.

![Esimerkki yhden rivitason automaattisesta kulut-taulusta](media/linechargesexample.png)

Lähetä veloitukset Commercen asteikkoyksikköön/kanavatietokantaan, jotta myyntipiste voi käyttää niitä suorittamalla **1040 jakeluaikataulu** -työn.

#### <a name="sales-processing-for-this-scenario"></a>Myynnin käsittely tässä skenaariossa

Kun edellä mainitut määritysvaiheet on tehty ja muutokset on otettu käyttöön kanavatietokannassa, mikä tahansa myyntipiste-, puhelinkeskus- tai sähköinen kaupankäynti -kanavassa luotu asiakastilaus tai myyntitapahtuma, jonka tilauksessa tämä nimike on, käynnistää rivitason kulun järjestelmällisen lisäämiseen tilauksen kokonaissummaan.

Tällä hetkellä kuluja käytetään niille myyntiriveille, jotka vastaavat rivitason automattisten kulujen määritystä yrityksessä, sillä millään toiminnolla ei voi määrittää, että rivitason automaattista kulua käytetään vain tietyssä myyntikanavassa.

### <a name="manual-header-charges-example"></a>Esimerkki manuaalisista otsikon kuluista

#### <a name="use-case-scenario-description"></a>Käyttötapausskenaarion kuvaus

Jälleenmyyjä tekee poikkeuksen tyypillisiin prosesseihin tarjoamalla tuotteiden kotiinkuljetuksen asiakkaille, jotka tilaavat tuotteet myymälässä. Jälleenmyyjä ja asiakas ovat sopineet, että asiakas maksaa 25 dollarin lisämaksun tämän palvelun käsittelykuluna. Tilauksen vastaanottajan on lisättävä tämä lisämaksu tapahtumaan. Koska maksu on yleismaksu eikä liity mihinkään tiettyyn tilauksen tuotteeseen, otsikon kulun käyttö on mahdollista.

#### <a name="setup-and-configuration"></a>Asetukset ja määrittäminen

Varmista, että tässä skenaariossa käytettävä kulukoodi on määritetty oikein, valitsemalla **Myyntireskontra \> Kulujen määritys \> Kulut** ja määritä skenaarioon sopiva kulukoodi.

![Esimerkki kuluista](media/chargesexample.png)

Jo kulu on toimitukseen liittyvä kulu, jota käytetään toimitusalennuksissa tai -kampanjoissa, valitse kulukoodin **Toimitusmaksu**-asetukseksi **Kyllä**. Jos tämä kulu voidaan palauttaa järjestelmällisesti, kun palautustapahtumaa käsitellään myyntipistesovelluksessa, valitse **Palautettava**-asetukseksi **Kyllä**. **Palautettava**-merkintää käytetään vain, kun **Käytä edistyneitä automaattisia kuluja** -parametrin asetuksena on **Kyllä**.

Lähetä veloitukset Commercen asteikkoyksikköön/kanavatietokantaan, jotta myyntipiste voi käyttää niitä suorittamalla **1040 jakeluaikataulu** -työn.

**Lisää otsikon kulut** -työvaiheen on oltava määritettynä [myyntipisteen näyttöasettelussa](https://docs.microsoft.com/dynamics365/unified-operations/retail/pos-screen-layouts), jotta käyttäjän myyntipisteestä käytettävä painike voi kutsua tämän toimenpiteen (toimenpide 141). Näyttöasettelun muutokset on jaettava kanavaan; lisäksi ne jaettava jakeluaikataulutoiminnon kautta.

#### <a name="sales-processing-of-manual-header-charges"></a>Manuaalisten otsikon kulujen myyntikäsittely

Skenaarion suorittaminen myyntipistesovelluksessa edellyttää, että myyntipisteen käyttäjä luo myyntitapahtuman tavalliseen tapan lisäämällä tuotteet ja mahdolliset muut määritykset myyntiin. Käyttäjä on suoritettava ennen maksun keräämistä **Lisää otsikon kulu** -työvaihe, joka pyytää käyttäjää valitsemaan kulukoodin ja antamaan kulujen arvon. Kun käyttäjä on suorittanut prosessin loppuun, kulu lisätään myyntitilaukseen otsikkotason kuluna.

Tätä prosessia voidaan käyttää puhelinkeskuksessa käyttämällä **Kulut**-ominaisuutta, joka sijaitsee työkalurivin **Myynti**-välilehdessä. Käyttäjä voi lisätä uusia kulurivejä tilauksen otsikkoon **Kulujen ylläpito** -sivulla.

### <a name="manual-line-charges-example"></a>Esimerkki manuaalisista rivin kuluista

#### <a name="use-case-scenario"></a>Käyttötapausskenaario

Asiakas on pyytänyt, että kaksi viidestä myyntitilauksen nimikkeestä paketoidaan lahjaksi. Jälleenmyyjä tarjoaa tämän palvelun valinnaisena 2,00 dollariin nimikekohtaisella maksulla. Tilauksen vastaanottajan on lisättävä nämä maksut niihin nimikkeisiin, jotka on paketoitava lahjaksi.

#### <a name="setup-and-configuration"></a>Asetukset ja määrittäminen

Varmista, että tässä skenaariossa käytettävä kulukoodi on määritetty oikein, valitsemalla **Myyntireskontra \> Kulujen määritys \> Kulut** ja määritä skenaarioon sopiva kulukoodi.

Jo kulu on toimitukseen liittyvä kulu, jota käytetään toimitusalennuksissa tai -kampanjoissa, valitse kulukoodin **Toimitusmaksu**-asetukseksi **Kyllä**. Jos kulu voidaan palauttaa järjestelmällisesti, kun palautustapahtumaa käsitellään myyntipistesovelluksessa, valitse **Palautettava**-asetukseksi **Kyllä**. **Palautettava**-merkintää käytetään vain, kun **Käytä edistyneitä automaattisia kuluja** -parametrin asetuksena on **Kyllä**.

Lähetä veloitukset Commercen asteikkoyksikköön/kanavatietokantaan, jotta myyntipiste voi käyttää niitä suorittamalla **1040 jakeluaikataulu** -työn.

**Lisää rivin kulut** -työvaiheen on oltava määritettynä [myyntipisteen näyttöasettelussa](https://docs.microsoft.com/dynamics365/unified-operations/retail/pos-screen-layouts), jotta käyttäjän myyntipisteestä käytettävä painike voi kutsua tämän toimenpiteen (toimenpide 140). Näyttöasettelun muutokset on jaettava kanavaan; lisäksi ne jaettava jakeluaikataulutoiminnon kautta.

#### <a name="sales-processing-of-the-manual-line-charge"></a>Manuaalisen rivin kulun myyntikäsittely

Skenaarion suorittaminen myyntipistesovelluksessa edellyttää, että myyntipisteen käyttäjä luo myyntitapahtuman tavalliseen tapan lisäämällä tuotteet ja mahdolliset muut määritykset myyntiin. Käyttäjän on valittava ennen maksun keräämistä myyntipisteen nimikeluettelonäytössä rivi, johon maksu kohdistetaan, ja suoritettava **Lisää rivin kulu** -työvaihe. Käyttäjää pyydetään valitsemaan kulukoodi ja antamaan kulujen arvo. Kun käyttäjä on suorittanut prosessin loppuun, kulu linkitetään riviin ja lisätään tilauksen kokonaissummaan rivitason kuluna. Käyttäjä voi tarvittaessa toistaa rivin lisäkulujen lisäämisen muille tapahtuman nimikeriveille.

Samaa prosessia voidaan käyttää puhelinkeskuksessa käyttämällä kulujen ylläpito-ominaisuutta, joka sijaitsee **Myyntitilaus**-sivun **Myyntitilauksen rivit** -osan avattavassa **Myyntitiedot**-valikossa. Valitsemalla tämän vaihtoehdon voidaan lisätä uuden rivikohtaisen kulun tapahtumaan avautuvassa **Ylläpidä kuluja** -sivulla.

## <a name="additional-features"></a>Lisätoiminnot

### <a name="editing-charges-on-a-pos-sales-transaction"></a>Myyntipisteen myyntitapahtuman kulujen muokkaaminen

**Kulujen hallinta** -työvaihe (142) on lisättävä [myyntipisteen näyttöasetteluun](https://docs.microsoft.com/dynamics365/unified-operations/retail/pos-screen-layouts), jotta käyttäjä voi tarkastella ja muokata tai korvata järjestelmän laskeman tai manuaalisesti luodut otsikko- tai rivitason kulut. Jos työvaihetta ei lisätä, käyttäjät eivät voi säätää kulujen arvoa myyntipistetapahtumassa. He eivät voi myöskään tarkastella kulujen tietoja, kuten kuluun sidotun kulukoodin tyyppiä.

Käyttäjä voi tarkastella myyntipisteen **Kulujen hallinta** -sivulla sekä otsikko- että rivitason kulujen tietoja. Käyttäjä voi tehdä tämän sivun **Muokkaa**-toiminnolla muutoksia summaan, joka veloitetaan tietyllä kulurivillä. Kun kulurivi ohitetaan manuaalisesti, sitä ei lasketa järjestelmällisesti uudelleen, ellei käyttäjä käynnistä **Laske kulut uudelleen** -työvaihetta.

Jos **Kulun ohituksen syykoodi** on määritetty **Commercen parametrit** -asetussivulla, käyttäjää pyydetään antamaan syykoodi, kun kuluja on muokattu myyntipistesovelluksessa.

Jos ohitettujen kulujen syykoodit on taltioitu, käytettävissä on uusi raportti, jossa näitä ohituksia voi tarkastella ja jossa ne voidaan tarkistaa. Raportin voi hakea valitsemalla **Retail ja Commerce \> Kyselyt ja raportit \> Kulun ohituksen historia**.

### <a name="refunding-charges-on-a-pos-return-transaction"></a>Myyntipisteen palautustapahtuman palautuskulut

Jos **Käytä edistyneitä automaattisia kuluja** -parametrin asetuksena on **Kyllä**, aiempaa Commercen **Palauta toimitusmaksut** -parametria ei enää käytetä. Jos haluat ilmaista, mitkä kulut palautetaan järjestelmällisesti asiakkaalle edistyneitä automaattisia kuluja käytettäessä, varmista, että liittyvä kulukoodiksi on määritetty **Palautettava** **Kulujen koodi** -asetussivulla. Varmista, että asetukset on synkronoitu Commerce-kanavan tietokantoihin jakeluaikataulun käsittelyn avulla.

### <a name="refunding-charges-on-a-return-order-transaction"></a>Palautustilaustapahtuman palautuskulut

Kuluja ei palauteta järjestelmällisesti Commercessa luotuihin **palautustilauksiin**. Käyttäjien on valittava **Kopioi kulut** -asetus **palautustilausta** luotaessa. Jos **Kopioi kulut** -asetusta ei valita, alkuperäisen myyntitapahtuman kuluja ei automaattisesti palauteta. Jos **Kopioi kulut** on valittu, kaikki kulut kopioidaan palautustilaukseen, ja käyttäjä voi manuaalisesti muokata tai poistaa kuluja, joita he eivät halua palauttaa. Puhelinkeskuksen palautustilausprosessi ei tällä hetkellä tunnista **Palautettava**-merkintää **Kulujen koodi** -asetuksissa.

### <a name="configuring-pos-receipts-to-show-charges"></a>Myyntipisteen kuittien määrittäminen näyttämään kulut

Seuraavat kuittielementit on lisättävä kuittiriville ja alatunnisteeseen tukemaan edistynyttä automaattisten kulujen toimintoa.

- **Rivin toimituskulut** – Tällä rivitason elementillä voidaan kerrata tietyt myyntirivillä käytetyt kulujen koodit. Tässä näkyy vain ne kulujen koodit, jotka on merkitty **toimituskuluiksi** **Kulujen koodi** -sivulla.
- **Rivin muut kulut** – Tällä rivitason elementillä voidaan kerrata kaikki muut kuin lähetyksen myyntirivillä käytetyt kulujen koodit. Ne ovat kulujen koodeja, joissa **Lähetys**-merkintää ei ole otettu käyttöön **Kulujen koodi** -sivulla.
- **Tilauksen toimituskulujen tiedot** – Tämä alatunnistetason elementti näyttää niiden kulujen koodien kuvaukset, joita on käytetty tilaukseen, joka on merkitty **toimituskuluiksi** **Kulujen koodi** -asetussivulla.
- **Tilauksen toimituskulut** – Tämä alatunnistetason elementti näyttää toimitukseen liittyvien kulujen dollariarvon.
- **Tilauksen muiden kulujen tiedot** – Tämä alatunnistetason elementti näyttää niiden kulujen koodien kuvaukset, joita ei ole käytetty tilaukseen, joka on merkitty toimitukseen kuluiksi.
- **Tilauksen muut kulut** – Tämä alatunnistetason elementti näyttää muuhun kuin toimitukseen liittyvien kulujen dollariarvon.

Lisäksi organisaatiota suositellaan lisäämään vapaatekstikentät kuitin alatunnisteeseen, jotta alueet, joissa kuluja kerrataan, voidaan määritetään.

### <a name="preventing-charges-from-being-calculated-until-the-pos-order-is-completed"></a>Kulujen laskennan estäminen ennen myyntipistetilauksen valmistumista

Jotkin organisaatiot haluavat ehkä odottaa, että käyttäjä on lisännyt kaikki myyntirivit myyntipistetapahtumaan ennen kulujen laskemista. Jos haluat estää kulujen laskemisen, kun nimikkeitä lisätään myyntipistetapahtumaan, ota **Manuaalinen veloituksen laskenta** -parametri käyttöön myymälän käyttämässä **toimintoprofiilissa**. Tämän parametrin ottaminen käyttöön edellyttää, että myyntipistekäyttäjä käyttää **Laske loppusummat** -työvaihetta, kun tuotteiden lisääminen myyntipistetapahtumaan on päättynyt. **Laske loppusummat** -työvaihe käynnistää sitten tilauksen otsikon tai rivien mahdollisten automaattisten kulujen laskennan.

### <a name="charges-override-reports"></a>Kulujen ohitusraportit

Jos käyttäjät ohittavat lasketut kulut manuaalisesti tai lisäävät manuaalisen kulun tapahtumaan, nämä tiedot ovat käytettävissä tarkistusta varten **Kulujen ohituksen historia** -raportissa. Raportin voi saada valitsemalla **Retail ja Commerce \> Kyselyt ja raportit \> Kulun ohituksen historia**. On tärkeää huomata, että tähän raporttiin tarvittavat tiedot tuodaan kanavatietokannata HQ-sovellukseen P-jakeluaikataulutöinä. Tämän vuoksi tiedot juuri myyntipisteessä tehdyistä ohituksista eivät ehkä ole heti käytettävissä tässä raportissa, vaan tämän työn on ladattava myymälän tapahtumatiedot ensin HQ-sovellukseen.

## <a name="additional-resources"></a>Lisäresurssit

[Automaattisten veloitusten käyttöönotto ja määritys kanavan mukaan](auto-charges-by-channel.md)

[Otsikon kulujen suhteellinen jakaminen vastaaville myyntiriveille](pro-rate-charges-matching-lines.md)

