---
title: Työrakenteet
description: Työrakenne (WBS) on kuvaus projektissa tehtävästä työstä. Se on tehtävähierarkia, joka edustaa projektin tiimin käsitystä työn kokoonpanosta ja kunkin osan tai tehtävän koosta, kustannuksista ja kestosta.
author: KimANelson
manager: AnnBe
ms.date: 06/05/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjWorkBreakdownStructure
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 23861
ms.assetid: 241a0464-0056-4a69-b468-0afbe2d5f3ae
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: df4bc39f8df80580261102941712622ed59262bd
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/29/2019
ms.locfileid: "358896"
---
# <a name="work-breakdown-structures"></a>Työrakenteet

[!include [banner](../includes/banner.md)]

Työrakenne (WBS) on kuvaus projektissa tehtävästä työstä. Se on tehtävähierarkia, joka edustaa projektin tiimin käsitystä työn kokoonpanosta ja kunkin osan tai tehtävän koosta, kustannuksista ja kestosta. Työrakenteella on kolme päätavoitetta.

-   Tehtävien työn erittelyn tai kokoonpanon kuvailu.
-   Projektiin liittyvän työn ajoittaminen.
-   Kunkin tehtävän kustannusten arvioiminen.

Työrakenteen tarkkuus riippuu arvioiden ja arvioissa käytettävien seurantasojen vaaditusta tarkkuustasosta. Projektit, joissa on vähän toleranssia aikataulussa tai hinnassa lipeämiseen, edellyttävät tavallisesti yksityiskohtaisemman työrakenteen ja sen, että työnkulkua ja kustannuksia seurataan turvallisemmin työrakenteen puitteissa. Tämän tyyppinen projekti on yleinen rakennus- ja suunnittelutoimialoilla. 

Sen sijaan esimerkiksi media-, mainos-, ohjelmisto- ja IT-infrastruktuurialan projektit ovat usein ainutlaatuisia. Tuottavuus riippuu tehtävän suorittavan henkilön kokemuksesta ja osaamisesta. Tämän vuoksi näillä toimialoilla käytetään työrakennetta projektin kokoarvion saamisessa, ei projektin edistymisen yksityiskohtaisessa seuraamisessa. 

Työrakenteen muodostaminen on intensiivinen prosessi, joka kestää yleensä pitkään ja vaatii useiden henkilöiden yhteistyötä ja tietoja. Tässä ohjeaiheessa kerrotaan, miten Microsoft Dynamics 365 for Finance and Operationsissa olevia työrakenteen parannuksia voidaan käyttää arvioissa ja seuraamisessa vaatimusten täyttämiseksi.

## <a name="prerequisites-for-creating-a-wbs"></a>Työrakenteen luomisen edellytykset
Voit luoda työrakenteen, jos sinulla on työaikataulun ja työn kustannusarvion luontioikeus.

### <a name="prerequisites-for-creating-a-work-schedule"></a>Työaikataulun luomisen edellytykset

Voit käyttää työrakennetoimintojen kaikkia ajoitusominaisuuksia, kun teet seuraavat asetukset:

1.  Määritä oletuskalenteri ja projektikalenteri seuraavasti:
    1.  Valitse **Projektinhallinta ja kirjanpito** &gt; **Asetukset** &gt; **Projektinhallinnan ja kirjanpidon parametrit** &gt; **Aikataulutus**. Määritä oletuskalenteri **Oletustyökalenteri**-kentässä. Tämä on jokaisen uuden luotavan projektin oletustyökalenteri.
    2.  Voit muuttaa määritetyn projektin oletuskalenterin. Valitse projektin tietosivu ja päivitä sitten **Projektiryhmä ja ajoitus** -pikavälilehden **Suunnittelukalenteri**-kenttä valitsemalla siihen toinen kalenteri.

2.  Määritä vakiotyöpäivät ja -työtunnit. Projektin työkalenteriksi määrittämääsi kalenteria käytetään työrakenteessa seuraavien tietojen määrittämiseen:

-   Työpäivät ja lomat
-   Päivän työtuntien määrä

Voit määrittää kalenterin työpäivät ja -tunnit tai luoda uuden kalenterin valitsemalla **Organisaation hallinto** &gt; **Yleinen** &gt; **Kalenterit**.

### <a name="prerequisites-for-estimating-the-cost-of-work"></a>Työn kustannusarvion edellytykset

Voit käyttää työrakenteen kaikkia kustannusarvioissa käytettäviä toimintoja työntekijöiden, nimikkeiden sekä työ-, kulu- ja maksuluokkien kustannusten ja myyntihintojen määrittämisen jälkeen.

-   Voit määrittää työ-, kulu- ja maksuluokan kustannukset ja myyntihinnat valitsemalla **Projektinhallinta ja kirjanpito** &gt; **Asetukset** &gt; **Hinnat**.
-   Voit määrittää nimikkeiden kustannukset ja myyntihinnat Tuotetietojen hallinta -kohdan **Vapautetut tuotteet** -luettelosivun kunkin nimikkeen **Kauppasopimukset**-sivulla.

## <a name="creating-a-wbs"></a>Työrakenteen luominen
Työrakenteen luominen sisältää seuraavat kolme tehtävää:

1.  **Työn hajottaminen** – Luo työn erittely hallittaviin joukkoihin tai tehtäviin.
2.  **Työaikataulu** – Arvioi tehtävän suorittamiseen kuluva aika, määritä tehtävän keskinäiset riippuvuudet ja valitse tehtävien alkamis- ja päättymispäivämäärät.
3.  **Kustannusarvio** – Arvioi kunkin tehtävän kustannukset.

Seuraavissa osissa käsitellään sitä, miten työrakennetoiminnot voivat auttaa näiden tehtävien suorittamisessa.

### <a name="work-decomposition"></a>Työn hajottaminen

Työn erittelyn tai hajottamisen luominen on yleensä työrakenteen luomisprosessin ensimmäinen vaihe. Työrakennetoiminto tukee seuraavia työrakenteen tai hajottamisen perusrakenteita. 

**Projektin juuritehtävä** Projektin juuritehtävä on projektin ylimmän tason yhteenvetotehtävä. Kaikki muut projektit luodaan sen alle. Juuritehtävän nimeksi annetaan aina projektin nimi. Juurisolmun työ, päivämäärät ja kesto määrittävät juuritehtävän alla olevien tehtävien arvojen yhteenvedon. Juuritehtävän ominaisuuksia ei voi muokata eikä juuritehtävää voi poistaa.

**Yhteenveto- tai säilötehtävä** Yhteenvetotehtävä on tehtävä, joka sisältää alitehtäviä tai osatehtäviä. Yhteenvetotehtävällä ei ole omia töitä tai kustannuksia. Sen sijaan yhteenvetotehtävän työt ja kustannukset ovat sen osatehtävien töiden ja kustannusten summia. Osatehtävien aikaisinta alkamispäivämäärää käytetään yhteenvetotehtävän alkamispäivämääränä ja osatehtävien viimeisintä päättymispäivämäärää yhteenvetotehtävän päättymispäivämääränä. Voit muokata yhteenvetotehtävän nimeä, mutta et voi muokata työn, päivämäärien ja keston ajoitusominaisuuksia. Jos poistat yhteenvetotehtävän, voit poistaa myös kaikki sen osatehtävät. 

**Lehtisolmutehtävät** Lehtisolmutehtävä edustaa projektin yksityiskohtaisinta työpakettia. Lehtisolmu sisältää arvioidun työn, suunniteltujen resurssien määrän, suunnitellun alkamis- ja päättymispäivän sekä keston. 

Voit suorittaa seuraavat hierarkiatoiminnot, kun haluat ottaa käyttöön projektin työhierarkian tai hajottamisen luonnin. 

**Uusi tehtävä** Kaikki luodut uudet tehtävät lisätään automaattisesti juurisolmuun. Tehtävälle liitetään automaattisesti työrakennenumero. Työrakennenumero edustaa tehtävän tasoa hierarkiassa. Projektin juuritehtävän ensimmäisen tason tehtäville käytetään numerointimallia 1, 2, 3 jne. Ensimmäisen tason alla oleville tehtäville käytetään numerointimallia 1.1, 1.2, 1.3 jne. Jokaiselle edellisen tason alle lisätyille tasoille lisätään uusi numerosarja pisteen kanssa. 

Tällä hetkellä työrakenteen numerointia ei voi mukauttaa. 

**Sisennä tehtävä** Kun tehtävä sisennetään, siitä tulee edeltävän tehtävän alitehtävä. Uuden alitehtävän työrakennenumero lasketaan automaattisesti sen uuden päätason työrakennenumeron perusteella. Päätehtävä on nyt yhteenveto- tai säilötehtävä. Tämän vuoksi siitä tulee se osatehtävien koontitehtävä. 

> [!NOTE] 
> Kun tehtäviä sisennetään sellaisen tehtävän alla, joka oli lehtisolmu ennen sisennystoimintoa, uusi luotava yhteenvetotehtävä menettää omat päivämääränsä, työn ja resurssien määrän. Se käyttää nyt uusien osatehtävien arvojen yhteenvetoa. 

**Ulonna tehtävä** Kun tehtävä ulonnetaan, se ei enää ole päätehtävänsä osatehtävä. Tämän tehtävän työrakennenumero lasketaan automaattisesti uudelleen hierarkian tehtävän uuden tason mukaiseksi. Tehtävän edellisen päätehtävän työ, kustannukset ja päivämäärät lasketaan uudelleen, kun tämä tehtävä suljetaan pois. 

**Siirrä ylös ja Siirrä alas** Kun valitset **Siirrä ylös**- tai **Siirrä alas** -kohdan, muutat tehtävän sijaintia päähierarkiassa. Tehtävän sijainti ei vaikuta tehtävän työhön, kustannuksiin, päivämääriin tai kestoon. Tehtävän työrakennenumero lasketaan kuitenkin automaattisesti uudelleen tehtävän uuden sijainnin mukaiseksi.

### <a name="schedule-estimation"></a>Aikatauluarvio

Aikatauluarvio on yleensä työrakenteen luomisen toinen vaihe. Parhaan käytännön mukaisesti kannattaa tehdä aikatauluarvio ennen tehtävien luomista. Finance and Operationsin **Työrakenne**-sivu sisältää kaksi osaa. Yläruutu on tarkoitettu aikatauluarviolle. Alempi ruutu sisältää **Arvioidut kustannukset ja tuotto** -välilehden, jota käytetään kustannusarviossa. 
**Tehtävän riippuvuudet** Voit luoda työrakenteen tehtävien välille edeltäjäsuhteita. Kun liität edeltäjätehtävän tehtävään, kyseinen tehtävä voi alkaa vasta, kun kaikki sen edeltäjätehtävät on suoritettu. Tehtävän suunniteltu alkamispäivämäärä määritetään automaattisesti kaikkien sen edeltäjätehtävien viimeiseksi päivämääräksi. 

**Tehtävien ajoitus Microsoft Dynamics 365 for Finance and Operationsissa** Seuraavat tekijät määrittävät lehtisolmutehtävien ajoituksen:

-   Edeltäjät
-   Työmäärä
-   Resurssien määrä
-   Aloitus- ja päättymispäivät.

Projektin ajoituksen alkamispäivämäärä asetetaan automaattisesti sellaisen lehtisolmutehtävän alkamispäivämääräksi, jolla ei ole edeltäjiä. Lehtisolmutehtävän kesto lasketaan aina sen alkamis- ja päättymispäivämäärien välisten työpäivien määränä. 

*<strong><em>Ajoitussäännöt</em></strong>* Kun automaattinen ajoituksen aputoiminto on käytössä, lehtisolmutehtävien ajoituksessa käytetään seuraavia sääntöjä:

-   Tehtävän alkamis- ja päättymispäivämäärän on oltava työpäiviä projektin ajoituskalenterin mukaan.
-   Edeltäjiä omaavan tehtävän alkamispäivämääräksi määritetään automaattisesti sen edeltäjätehtävien viimeinen päivämäärä.
-   Tehtävän työ lasketaan automaattisesti seuraavalla tavalla:

Henkilöiden määrä × kesto × projektikalenterin vakiotyöpäivien tuntimäärä. 

Joskus näistä säännöistä halutaan ehkä poiketa. Voit poistaa automaattisen ajoituksen käytöstä, kun haluat, ettei Finance and Operations määritä tai korjaa lehtisolmutehtävien ominaisuuksia automaattisesti. Kun syötät tehtävälle tiedot, jotka rikkovat jotakin ajoitussääntöä, tehtävän kohdalla näytetään aikatauluvirhekuvake. Jos et halua aikatauluvirheiden olevan näkyvissä, valitse **Aikatauluvirheet näytetään** -kohta, jolloin toiminto poistetaan käytöstä. 

> [!NOTE] 
> Yhteenveto- tai säilötehtävän arvoja lasketaan jatkossakin osatehtävien arvojen summana siitä huolimatta, onko automaattisen ajoituksen aputoiminto käytössä vai ei. 

**Aikatauluvirheiden korjaaminen** Kun automaattisen ajoituksen aputoiminto on päällä, aikatauluvirheitä ei todennäköisesti tapahdu. Jos kuitenkin automaattisen ajoituksen aputoiminto poistetaan käytöstä ja otetaan uudelleen käyttöön myöhemmin, aikatauluvirhekuvakkeet saattavat näkyä työrakenteessa. 

**Aikatauluvirheiden korjaaminen tehtävän mukaan** Kun kaksoisnapsautat tietyn tehtävän aikatauluvirhekuvaketta, valintaikkunassa näkyvät kaikki kyseisen tehtävän aikatauluvirheet. Voit päättää, mitkä tehtävän aikatauluvirheet korjataan. 

**Kaikkien aikatauluvirheiden korjaaminen** Jos haluat Finance and Operationsin korjaavan kaikki työrakenteen aikatauluvirheet, valitse toimintoruudussa **Korjaa kaikki aikatauluristiriidat**. 

> [!NOTE] 
> Tämä toiminto voi aiheuttaa merkittäviä muutoksia työrakenteeseen. Virheet korjataan seuraavassa järjestyksessä:

1.  Kaikkien tehtävien arvioitua työtä muokataan niin, että se on sama kuin projektikalenterissa määritetty kapasiteetti.
2.  Kunkin tehtävän alkamispäivämäärää muokataan niin, että tehtävä alkaa sen edeltäjätehtävien suorituksen jälkeen.
3.  Kunkin tehtävän alkamispäivämäärää muokataan niin, että edeltäjätehtävien alkamispäivämäärien välit poistuvat.

### <a name="cost-estimation"></a>Kustannusarvio

Kuten aiemmin tässä asiakirjassa mainittiin, kunkin lehtisolmutehtävän kustannusarvio syötetään **Työrakenne**-sivun alemman ruudun **Arvioidut kustannukset ja tuotto** -välilehdessä. 

> [!NOTE] 
> Yhteenveto- tai säilötehtävän kustannusarviota ei voi muokata. Yhteenvetotehtävän kustannusarvio on sama kuin sen lehtisolmutehtävän kustannusarvion summa. Kunkin tehtävän arvioidut kokonaiskustannukset lasketaan seuraavien tapahtumatyyppien arvioitujen kustannusten summana:

-   Työ
-   Nimike tai materiaali
-   Kulut

**Maksu**-tyyppistä tapahtumaa käytetään maksuun perustuvan tuoton arvioinnissa. Tällä tapahtumatyypillä ei ole kustannuskomponenttia. Sen vuoksi sitä ei oteta huomioon kustannusarviossa. 

**Ennakkomaksu**-tyyppistä tapahtumaa käytetään sopimuksen myyntiarvon tallentamisessa projektityypeissä, joiden arvo on kiinteä. Tätä tapahtumatyyppiä ei oteta myöskään huomioon kustannusarviossa. 

Kun kunkin tehtävän työn, materiaalin ja kulujen kustannuksia arvioidaan, projektiluokka on liitettävä arvioituihin kustannuksiin. 

**Työkustannusten arvioiminen** Jokaiselle lehtisolmutehtävälle liitetään työ tunteina sekä oletusluokka. Tämän vuoksi kyseisen tehtävän työkustannusarvio lisätään automaattisesti työn oletusluokkaan tehtävän aikataulun määrittämisen yhteydessä. Kustannusarvio näkyy kyseisen tehtävän **Rivin erittely** -ruudukon **Arvioidut kustannukset ja tuotto** -välilehdessä. Jos haluat lisää työkustannusarvioita, voit lisätä niitä välilehdessä. Jos suurennat tai pienennät työkustannusarvion tunteja, tehtävän aikataulu lasketaan automaattisesti uudelleen. 

**Kulujen ja materiaalikustannusten arvioiminen** **Arvioidut kustannukset ja tuotto** -välilehden avulla voi myös arvioida tehtävän kulut ja materiaalikustannukset arvioita varten. 

Kunkin työ- tai kuluarviorivin kustannus ja myyntihinta perustuu kohdan **Projektinhallinta ja kirjanpito** &gt; **Asetukset** &gt; **Hinnoittelu** hinnoittelutauluissa kullekin luokalle määritettyihin asetuksiin. Nimikkeiden kustannukset ja myyntihinnat lisätään oletusarvoisesti nimikkeestä tai kauppasopimuksista Tuotetietojen hallinta -kohdan **Vapautetut tuotteet** -luettelosivulla.

## <a name="tracking-progress-on-the-wbs"></a>Työrakenteen edistymisen seuraaminen
Joillakin toimialoilla projektin edistymistä seurataan hyvin yksityiskohtaisella työrakenteen tasolla, kun taas joillakin toimialoilla edistymistä seurataan työrakenteen korkeammalla tasolla. Tässä osassa kerrotaan, miten työrakenteen seurantaa voidaan käyttää projektin vaatimusten mukaisesti. 

Finance and Operations sisältää kolme projektin työrakenteen näkymää: suunnittelunäkymä, työnseurantanäkymä ja kustannusseurantanäkymä.

### <a name="planning-view"></a>Suunnittelunäkymä

Suunnittelunäkymä sisältää aikataulun ja kustannusten tietojen suunnitellun arvion tai perusarvion. Vaikka projektin työrakenteen version ja perusversion seurantaa varten ei ole toimintoja, tämän näkymän arvoja käytetään perusversion esittämisessä. Tämän ohjeaiheen Aikatauluarvio- ja Kustannusarvio-osassa kerrotaan tietoja tästä näkymästä ja sen käyttämisestä työrakenteen luomisessa.

### <a name="effort-tracking-view"></a>Työnseurantanäkymä

Työnseurantanäkymä sisältää työrakenteen tehtävien edistymisen seuraamisen. Se vertaa tehtävän kumulatiivisia toteutuneita työtunteja suunniteltuihin työtunteihin. Seuraavat kaavat määrittävät työnseurantanäkymän arvot.

-   Edistyminen prosentteina = toteutunut työ tähän mennessä ÷ tehtävän suunniteltu työ
-   Jäljellä oleva työ (tunnetaan myös nimellä valmistumisarvio \[ETC\]) = suunniteltu työ – toteutunut työ tähän mennessä
-   Arvio lopussa (kustannusarvio) = jäljellä oleva työ + toteutunut työ tähän mennessä
-   Ennakoitu työvarianssi = suunniteltu työ – kustannusarvio

Työnseurantanäkymä sisältää tehtävän työvarianssin projektion. Se perustuu siihen, onko kustannusarvio suurempi vai pienempi kuin suunniteltu työ.

-   Jos kustannusarvio on suurempi kuin suunniteltu työ, tehtävän arvioidaan kestävän kauemmin kuin alussa suunniteltiin. Tehtävä on siis jäljessä aikataulusta.
-   Jos kustannusarvio on pienempi kuin suunniteltu työ, tehtävän arvioidaan kestävän vähemmän aikaa kuin alussa suunniteltiin. Tehtävä on siis edellä aikataulusta.

**Projektipäällikön tekemä uusi työn projektio** Joskus projektipäällikön tai muun projektin edistymistä seuraavan henkilön on korjattava tehtävän alkuperäisiä arvioita. Tehtävä saattaa sujua alkuperäistä arviota nopeammin tai hitaammin useiden eri syiden vuoksi. Esimerkiksi laajuutta on saatettu pienentää tai työntekijöillä on alun perin suunniteltua vähemmän kokemusta. Projektiot ovat projektipäällikön käsitys arvioista projektin nykyisen tilan perusteella. Yleensä perustason numeroita ei muuteta, koska projektin perustaso on projektin aikataulun ja kustannusarvion tarkkaan harkittu asiakirja, jonka kaikki projektin sidosryhmät ovat hyväksyneet. 

Projektipäälliköt voivat muokata tehtävien töitä kahdella eri tavalla:

-   Sen jäljellä olevan työn muokkaaminen, joka on määritetty päivittämään automaattisesti tehtävän todellinen jäljellä oleva työ.
-   Sen edistymisprosentin muokkaaminen, joka on määritetty päivittämään automaattisesti tehtävän todellinen edistyminen.

Molempien tapojen käyttäminen aiheuttaa tehtävän arvion valmistumiseen, kustannusarvio ja edistymisprosentin sekä tehtävän arvioidun työvarianssin laskemisen uudelleen. Yhteenvetotehtävien valmistumisarvio, kustannusarvio ja edistymisprosentti lasketaan myös uudelleen ja yhteenvetotehtävien arvioitu työvarianssi päivitetään. 

**Yhteenvetotehtävien muokattu työ** Voit muokata yhteenveto- tai säilötehtävien työtä. Laskennat suoritetaan automaattisesti seuraavassa järjestyksessä siitä huolimatta, muokataanko näitä arvoja käyttämällä yhteenvetotehtävien jäljellä olevaa työtä vai etenemisprosenttia:

1.  Tehtävän kustannusarvio, valmistumisarvio ja edistymisprosentti lasketaan.
2.  Uusi kustannusarvio jaetaan alitehtäville alkuperäisen kustannusarviosumman suhteessa.
3.  Kullekin lehtisolmutehtävälle lasketaan uusi kustannusarvio.
4.  Jäljellä oleva työ ja edistymisprosentti lasketaan uudelleen kaikille muuttuneille alitehtäville uuden kustannusarvion arvon perusteella. Tehtävien työvarianssi lasketaan myös uudelleen.
5.  Yhteenvetotehtävien kustannusarvio lasketaan myös uudelleen lehtisolmuista.

Määritä työrakenteen seurannan ja ylläpidon taso valitsemalla työnseurantanäkymän **Laajenna tasolle** -kohta. Työrakenne laajennetaan avaamisen yhteydessä automaattisesti kyseiselle tasolle työnseurantanäkymässä.

### <a name="cost-tracking-view"></a>Kustannusseurantanäkymä

Kustannusseurantanäkymä sisältää tehtävän kustannusten kulutuksen seurannan. Tässä näkymässä tehtävän tähän mennessä toteutuneita kustannuksia verrataan tehtävän suunniteltuihin kustannuksiin. Seuraavat kaavat määrittävät kustannusseurantanäkymän arvot.

-   Kulutettujen kustannusten prosenttiosuus = toteutuneet kustannukset tähän mennessä ÷ tehtävän suunnitellut kustannukset
-   Jäljellä olevat kustannukset = suunnitellut kustannukset – toteutuneet kustannukset tähän mennessä
-   Arvio lopussa (kustannusarvio) = jäljellä olevat kustannukset + toteutuneet kustannukset tähän mennessä
-   Ennakoitu kustannuspoikkeama = suunnitellut kustannukset – kustannusarvio

Kustannusseurantanäkymä sisältää tehtävän kustannuspoikkeaman projektion. Se perustuu siihen, onko kustannusarvio suurempi vai pienempi kuin suunnitellut kustannukset.

-   Jos kustannusarvio on suurempi kuin suunnitellut kustannukset, tehtävän arvioidaan kuluttavan enemmän rahaa kuin alussa suunniteltiin. Se siis ylittää budjetin.
-   Jos kustannusarvio on pienempi kuin suunnitellut kustannukset, tehtävän arvioidaan kuluttavan vähemmän rahaa kuin alussa suunniteltiin. Se siis alittaa budjetin.

**Projektipäällikön tekemä uusi kustannusten projektio** Projektipäällikön on korjattava tehtävän alkuperäistä kustannusarviota jäljellä olevien kustannusten avulla. Projektipäällikkö voi muokata jäljellä olevien kustannusten arvoksi tehtävän valmistumiseen vaaditut kustannukset. Jos jäljellä olevien kustannusten arvoa muokataan, tehtävän jäljellä olevat kustannukset, kustannusarvio ja kulutettujen kustannusten prosenttiosuus sekä tehtävän arvioitu kustannuspoikkeama lasketaan uudelleen. Yhteenvetotehtävien valmistumisarvio, kustannusarvio ja kulutettujen kustannusten prosenttiosuus lasketaan myös uudelleen ja yhteenvetotehtävien arvioitu kustannuspoikkeama päivitetään. 

> [!NOTE] 
> Kun työrakenteen tehtävän työtä muutetaan työnseurantanäkymässä, tehtävän jäljellä olevat kustannukset, kustannusarvio ja kulutettujen kustannusten prosenttiosuus sekä arvioitu kustannuspoikkeama lasketaan uudelleen kustannusseurantanäkymässä. Kustannusversiot eivät kuitenkaan vaikuta työnseurantanäkymän arvoihin, koska kustannuksia tapahtumatyypin mukaan (työ, materiaali tai kulu) tai projektiluokkaa ei ole muutettu. 

**Projektin versio kustannuksille yhteenvetotehtävissä** Jos muokkaat yhteenvetotehtävien kustannuksia, laskelmat näkyvät automaattisesti seuraavassa järjestyksessä:

1.  Tehtävän kustannusarvio, jäljellä olevat kustannukset ja kulutettujen kustannusten prosenttiosuus lasketaan uudelleen.
2.  Uusi kustannusarvio jaetaan alitehtäville tehtävien alkuperäisen kustannusarvion suhteessa.
3.  Kunkin tehtävän uusi kustannusarvio lasketaan.
4.  Palvelukustannukset ja kulutettujen kustannusten prosenttiosuus lasketaan uudelleen muuttuneille alitehtäville kustannusarvion arvon perusteella. Tehtävien kustannuspoikkeama lasketaan myös uudelleen.
5.  Kaikkien yhteenvetotehtävien kustannusarvio lasketaan uudelleen tämän muutoksen perusteella.

Määritä työrakenteen seurannan ja ylläpidon taso valitsemalla kustannusseurantanäkymän **Laajenna tasolle** -kohta. Työrakenne laajennetaan avaamisen yhteydessä kyseiselle tasolle kustannusseurantanäkymässä.

### <a name="earned-value-management"></a>Ansaitun arvon hallinta

Voit käyttää ansaitun arvon menetelmää projektin edistymisen seurannassa. Voit tarkastella ansaitun arvon mittareita projektipäällikön roolikeskuksessa. Ansaitun arvon kaavion osa näyttää suunnitellun arvon ja toteutuneiden kustannusten aikajaksotetut arvot. Kuluvan päivän ansaittu arvo näytetään pisteenä. Ansaitun arvon aikajaksotetut tiedot eivät ole tällä hetkellä käytettävissä. 

Ansaitun arvon aikajaksotus näytetään viikoittain tai kuukausittain. Tässä osassa esitellään ansaitun arvon menetelmän kolme pääkohtaa: suunniteltu arvo, ansaittu arvo ja toteutuneet kustannukset. 

**Suunniteltu arvo** Ansaitun arvon menetelmän teoriassa kerrotaan, että suunnitellun arvon kuvio esittää projektin tiimin projektille suunnitteleman ansaitun arvon hintaa. 

Finance and Operations käyttää 0:100-ansaintasääntöä suunnitellun arvon esittämisessä. Tämän säännön mukaan tehtävän arvo kirjataan tehtävään sen päättymispäivämääränä. Arvoja ei kirjata, ennen kuin tehtävä on täysin valmis. 

Projektinhallinta ja kirjanpito -kohdassa syötetään lehtisolmujen päättymispäivämäärä ja niiden suunnitellut kustannukset. Kun suunnitellun arvon kaavio näytetään viikon mukaan, kaikkien lehtisolmutehtävien suunnitellut arvot lasketaan yhteen viikon ajalta projektin keston aikana. 

**Ansaittu arvo** Ansaitun arvon menetelmän teoriassa kerrotaan, että ansaitun arvon kuvio esittää projektin tiimin projektille todellisuudessa ansaitseman arvon hintaa. 

Finance and Operations käyttää 0:100-ansaintasääntöä ansaitun arvon esittämisessä. Tämän säännön mukaan tehtävän arvo kirjataan tehtävään sen päättymispäivämääränä. Arvoja ei kirjata, ennen kuin tehtävä on täysin valmis. 

Kun ansaittu arvo lasketaan, kunkin tehtävän edistymisprosentti otetaan huomioon. Kun käytössä on 0:100-ansaintasääntö, vain määritetyn kauden valmiit tehtävät otetaan huomioon ansaitun arvon laskennassa kyseisen kauden lopussa. Projektin ansaittu arvo lasketaan kaikkien kaavion luomisen yhteydessä valmiina olleiden tehtävien perusteella. 

> [!NOTE] 
> Tällä hetkellä työrakenteen seurantajärjestelmässä ei ole tietorakenteita, joiden avulla kunkin tehtävän aiemmat edistymisprosentit voitaisiin tallentaa. Tämän vuoksi ansaitut arvot voidaan raportoida vain sen ajan osalta, jona kuutio käsitellään. Käsittele kuutio säännöllisesti ja päivitä roolikeskuksessa näytettävät ansaitun arvon tiedot. 

**Toteutuneet kustannukset** Ansaitun arvon menetelmän teoriassa kerrotaan, että toteutuneiden kustannusten kuviossa esitetään hinta, jonka perusteella projektissa käytetään rahaa. 

Projektiin kirjattuja tapahtumia käytetään toteutuneiden kustannusten rivin kuvaamisessa. Kustannusten yhteenveto esitetään päivän mukaan. Tietoja käytetään tämän jälkeen ansaitun arvon kaavion toteutuneiden kustannusten esittämisessä viikon tai kuukauden mukaan.

### <a name="how-to-use-the-concepts-of-planned-value-earned-value-and-actual-cost"></a>Suunniteltu arvo-, ansaittu arvo- ja toteutuneet kustannukset -käsitteen käyttäminen

**Aikatauluvarianssi** Suunnittelun aikana luodaan aikajanan työn ennuste. Tämän vuoksi suunniteltu arvo on hinta, jonka projektin suunnittelijat arvelivat projektin valmistumiseen kuluvan. Sen jälkeen kun projekti on käynnissä, työ on tehty valmiiksi ja projekti saa ansaittua arvoa. Voit tarkastella projektin työn edistymistä vertaamalla suunniteltua arvoa ansaittuun arvoon. Vertailun tulosta kutsutaan aikatauluvarianssiksi. 

Jos kauden suunniteltu arvo on suurempi kuin ansaittu arvo, projektin suoritetun työn määrä on pienempi kuin suunnitellun työn määrä. Projekti on siis jäljessä aikataulusta. Koska suunniteltu arvo ja ansaittu arvo esitetään rahamääräisin termein, projektin viiveaika ilmoitetaan myös rahamääräisenä arvona. 

Jos kauden suunniteltu arvo on pienempi kuin ansaittu arvo, projektin suoritetun työn määrä on suurempi kuin suunnitellun työn määrä. Projekti on siis edellä aikataulusta. Myös läpimenoaika esitetään rahamääräisenä arvona.

**Kustannuspoikkeama** Koska ansaitun arvon kerroin on kustannushinta, ansaittu arvo osoittaa projektin suoritetun työn kustannukset. Projektin edistyessä tapahtumalokiin tallennetaan projektissa kulutetut rahasummat. Kun ansaittua arvoa verrataan toteutuneisiin kustannuksiin, esille saadaan käytetty summa verrattuna ansaittuun summaan. Vertailun tulosta kutsutaan kustannuspoikkeamaksi. 

Jos kauden toteutuneiden käytettyjen kustannusten määrä on suurempi kuin ansaittu arvo, projektissa on käytetty enemmän rahaa kuin ansaittu. Projekti siis ylittää budjetin. 

Jos kauden toteutuneiden käytettyjen kustannusten määrä on pienempi kuin ansaittu arvo, projektissa ansaittu enemmän rahaa kuin käytetty. Projekti siis alittaa budjetin.

## <a name="wbs-templates"></a>WBS-mallit
Voit luoda projekteille vakiomalleja työrakennemallien avulla. Jos yrityksen tarjoamat projektit sisältävät paljon toistettavaa työtä, työrakennemalli kannattaa luoda. 

Voit luoda aiemmin luodun projektin työrakenteesta työrakennemallin. Näin voit käyttää uudelleen aiemman projektin suunnittelun yhteydessä kerätyt tiedot ja parhaat käytännöt vastaavissa tulevaisuuden projekteissa. Joskus koko työrakennetta ei kuitenkaan kannata tallentaa mallina. Voit luoda malleja myös projektin työrakenteen osista.

### <a name="saving-a-projects-wbs-as-a-template"></a>Projektin työrakenteen tallentaminen mallina

Kun olet luonut mallin, voit tuoda sen uuden projektin työrakenteeseen juurisolmun tai minkä tahansa projektin työrakenteen tehtävän alle.

### <a name="importing-a-wbs-template-into-a-projects-wbs"></a>Työrakennemallin tuominen projektin työrakenteeseen

Kun tuot tehtäviä, mallin tehtävät järjestetään sen tehtävän alkamispäivämäärän mukaan, jonka alle tehtävät tuodaan. Tuonnin aikana tuotavien tehtävien alkamispäivämäärät lasketaan mallitehtävien edeltäjäsuhteiden avulla. Tuotavien tehtävien päättymispäivämäärät lasketaan kohdeprojektin vakiotyökalenterin avulla niin, että nykyisen projektin työkalenterin määritetyt työpäivät ja vakiotyötunnit säilytetään. 

Arviorivien kustannussummat ja myyntihinnat kohdistetaan, jotta voidaan varmistaa, että projekti- tai projektisopimuskohtaisten hintojen päivämäärät ovat kelvolliset.

### <a name="differences-between-a-projects-wbs-and-a-wbs-template"></a>Projektin työrakenteen ja työrakennemallin väliset erot

-   Työrakennemallien tehtävillä ei ole alkamis- ja päättymispäivämääriä.

Työrakennemalleille ei ole määritetty työpäiviä ja muita kuin työpäiviä.

-   Työrakennemallit käyttävät aina kaikkien projektien oletuskalenteriksi määritettyä ajoituskalenteria.

Oletusajoituskalenteria käytetään vain etsittäessä vakiotyöpäivän tunnit.

-   Edeltäjäsuhteita ei kopioida työrakennemalliin.

Koska työrakennemalleilla ei ole päivämääriä, edeltäjien päättymispäivämäärään perustuvaa alkamispäivämäärälogiikkaa ei vaadita.

-   Työkustannusarviorivi luodaan automaattisesti, kun tehtävä luodaan työrakennemalliin. Myyntihinta ja kustannussumma kopioidaan valitulta työntekijältä.

Kulut ja nimikekustannukset voidaan luoda manuaalisesti samalla tavalla kuin projektin työrakenteessa.

-   Aikatauluvirheet näytetään, kun seuraava kaava osoittaa poikkeamia:

Työ = resurssien määrä × kesto × vakiotyöpäivän tuntien määrä 

Voit korjata kaikki aikatauluvirheet samaan aikaan valitsemalla **Korjaa kaikki aikatauluvirheet**. 

Vaihtoehtoisesti voit korjata aikatauluvirheet yksitellen valitsemalla kunkin tehtävän varoituskuvakkeen.



