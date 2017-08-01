---
title: Budjettisuunnittelun integrointi toisten moduulien kanssa
description: Budjettisuunnitelmia voidaan muodostaa useista eri resursseista. Kausittaisten prosessien peruselementit ovat samat kaikille resursseille.
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 64443
ms.assetid: f9a94db5-906c-404a-9ca5-91528d67c490
ms.search.region: Global
ms.author: sigitac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 975497e8ed0c9738c225bad4db9165bf2ebc0192
ms.openlocfilehash: 7f3dc8089153a6c67c1666aa8f859d63dcc9d3c9
ms.contentlocale: fi-fi
ms.lasthandoff: 06/05/2017


---

# <a name="budget-planning-integration-with-other-modules"></a>Budjettisuunnittelun integrointi toisten moduulien kanssa

[!include[banner](../includes/banner.md)]




<a name="periodic-processes-for-generating-budget-plans"></a>Kausittaiset prosessit budjettisuunnitelmien muodostamiseen
----------------------------------------------

Budjettisuunnitelmia voidaan muodostaa seuraavista resursseista:

-   Kirjanpitotapahtumat
-   Käyttöomaisuudet
-   Ennusteen toimet
-   Projektiennusteet
-   Tarjontaennusteet
-   Kysynnän ennusteet
-   Budjettirekisterimerkinnät
-   Muut budjettisuunnitelmat

Kausittaisten prosessien peruselementit ovat samat kaikille prosesseille. Välilehtien avulla voit määrittää tietojen lähteen, kohteen (budjettisuunnitelma) määritteet ja vaihtoehdot prosessin suorittamiselle taustalla eräprosesseina. Nimikkeet, jotka eivät mahdollisesti ilmene kussakin prosessissa, on kuvattu tarkemmin tämän artikkelin seuraavissa osissa.

### <a name="actions"></a>Toimet

Kullekin luontiprosessille on saatavilla kolme toimintoa:

-   **Luo uusi budjettisuunnitelma** luo uuden suunnitelman, jolla on **Kohde**-osassa valitut määritteet. Näiden määritteiden ei tarvitse olla yksilöiviä. Näin ollen kahdella suunnitelmalla voi olla sama nimi ja muut arvot.
-   **Korvaa nykyinen budjettisuunnitelman skenaario** poistaa kaikki kohdebudjettisuunnitelman tiedot valitussa budjettisuunnitelmaskenaariossa ja luo uusia rivejä, jotka käyttävät valittuja lähdetietoja.
-   **Päivitä nykyinen budjettisuunnitelman skenaario ja liitä uudet tiedot** päivittää kohdesuunnitelman olemassa olevat, lähderivejä vastaavat rivit, ja lisäävät uudet rivit uusille tiedoille. Vastaavuus perustuu kirjanpitotiliin, päivämäärään, budjettiluokkaan ja useisiin muihin kenttiin. Kun esimerkiksi muodostat budjettisuunnitelmia ennusteen toimista, toimen numero on tärkeä kenttä. Kaikki rivit, joilla on toimen lähdenumeroa vastaava toimen numero, korvataan uusilla riveillä lähteestä.

### <a name="source"></a>Lähde

Kaikkien prosessien osalta **Lähde**-välilehden avulla voit suodattaa tietoja käyttämällä **Suodatin**-painiketta. Oletuksena tietyt kentät lisätään suodattimeen kussakin prosessissa. Esimerkiksi **Muodosta budjettisuunnitelma kirjanpidosta** -prosessissa **Kirjanpitotili-** ja **Päätili**-kategoriat ovat saatavilla ja näkyvät luontisivulla. Kaikki suodattimeen lisäämäsi kentät lisätään myös sivulle yhdessä mahdollisesti lisäämiesi kriteerien kanssa.

### <a name="target"></a>Tavoite

**Kohde**-välilehden **Historiallinen**-vaihtoehdon avulla voit käyttää lähdetietojen päivämääriä voimaantulopäivänä budjettisuunnitelmassa. Voimaantulopäivän on yleensä oltava suunnitelman budjettijakson sisällä. Kun määrität **Historiallinen**-valinnaksi **Kyllä**, käytetään lähteen päivämäärää (jopa vuotta) niin, että voit käyttää aiempia tietoja vertailun perusteena. Voit muokata historiallisia tietoja budjettisuunnitelmassa ja suunnitelmalle määritetään hyväksytyn työnkulun tila. Voit kuitenkin tarvittaessa määrittää tilan uudelleen, jos suunnitelman muut skenaariot vaativat muutoksia.

**Yhteenlaskettu summa perusteena** -kenttä sivun yläosassa määrittää myös käytettävän päivän. Tämä kenttä laskee summat yhteen ja määrittää voimaantulopäiväksi tilivuoden tai -kauden ensimmäisen päivän. 

Monista **Kohde**-välilehden kentistä tulee muokattavia tai vain luku -muotoisia valitsemastasi toiminnosta riippuen. Kun siirryt uuden budjettisuunnitelman luonnista olemassa olevan suunnitelman päivittämiseen, **Budjettisuunnitelman nimi** -kenttä ei ole enää käytettävissä ja olemassa olevan suunnitelman valitsemiseen liittyvät kentät tulevat saataville. Sekä **Kohde**-välilehdessä että **Lähde**-välilehdessä **Kirjanpito**-kenttä ei ole koskaan käytettävissä, koska tämä arvo määritetään valitussa budjettisuunnitteluprosessissa. 

**Budjettiluokka**-kentässä voit määrittää budjettisuunnitelman rivit joko kulutapahtumiksi tai tuottotapahtumiksi. Yleensä tuottotapahtumat ovat luottoja kirjanpitotilille ja ne tallennetaan siksi negatiivisina lukuina. Nämä tapahtumat myös yleensä näkyvät negatiivisina summina budjettisuunnitelmassa. Lisäämällä budjettiluokan kenttänä suunnitelman asettelussa voit kuitenkin mahdollistaa tuottojen näkymisen positiivisina summina.

### <a name="generation-rules"></a>Muodostussäännöt

Kolme kenttää tarjoaa lisätoimintoja: **Kerroin**, **Minimi**, ja **Pyöristys****-sääntö**. 

**Kerroin**-kentän arvo kerrotaan lähdesummalla budjettisuunnitelman summan määrittämiseksi. Voit sitten tehdä korjauksia budjettisuunnitelman rivejä luodessasi. Voit esimerkiksi kirjoittaa **1,03** kolmen prosentin lisäystä varten. Kertoimen täytyy olla positiivinen luku. 

**Minimi**-kentässä voit määritellä rajasumman budjettisuunnitelman rivin luonnille. Jos lähdesumma on pienempi kuin tämä luku, budjettisuunnitelman riviä ei luoda. Arvo **0,00** sallii kaikki summat, mutta ei rajoita rivejä positiivisiin summiin. (Jos arvoa ei ole, rivit on rajoitettu positiivisiin summiin. Negatiiviset summat sisällytetään aina, ja ne edustavat yleensä kredit-tapahtumia.)

**Pyöristyssääntö**-kentässä voit määritellä luotujen budjettisuunnitelman rivien tarkkuuden. Voit pyöristää summat valuutan lähimpään 1,00, 10,00, 100,00 jne. -arvoon.

## <a name="notes-for-specific-processes"></a>Määrättyjä prosesseja koskevia huomioita
### <a name="generate-budget-plan-from-general-ledger"></a>Muodosta budjettisuunnitelma kirjanpidosta

Kun luot budjettisuunnitelman kirjanpidon tiedoista, sinun on määritettävä **Yhteenlaskettu summa perusteena** -kentän arvoksi **Tilikausi**, jos **Historiallinen**-valinnan arvoksi on asetettu **Ei**. Lähteen kaudet ja päivämäärät eivät mahdollisesti vastaa kohteen kausia ja päivämääriä. Koska prosessilla ei ole luotettavaa tapaa yhdistää näitä arvoja, sinun on rajoitettava prosessi vuoden ensimmäiseen päivään. 

Kohteessa on määritetty **Budjettiluokka**-kenttä joko arvoksi **Kulu** tai **Tuotto**. Tätä asetusta käytetään **Budjettityyppi**-määritteen valitsemisessa luoduille riveille, kun rivin päätili ei ole **Tuotto-** tai **Kulu**-tyyppiä.

### <a name="generate-budget-plan-from-fixed-assets"></a>Muodosta budjettisuunnitelma käyttöomaisuudesta

**Muodosta budjettisuunnitelma käyttöomaisuudesta** prosessilla ei ole vaihtoehtoa tehdä kausittainen tai päiväkohtainen kooste. Myöskään suunnitelman määrittäminen historialliseksi ei ole vaihtoehto. Tämän kausittaisen prosessin avulla voit sisällyttää suunnitellut tapahtumat käyttöomaisuudelle budjetin suunnittelussa.

### <a name="generate-budget-plan-from-forecast-positions"></a>Muodosta budjettisuunnitelma ennusteen toimista

**Muodosta budjettisuunnitelma ennusteen toimista** -prosessi määrittää budjettisuunnitelman riville lähteen ennusteen toimen. Voit tarkastella toimea lisäämällä ennusteen toimen rivinä budjettisuunnitelman asetteluun käyttämällä **Budjettisuunnitelman rivit** -kyselyä. Jos et halua, että ennusteen toimi määritetään budjettisuunnitelman riveille, määritä **Sisällytä toimi budjettisuunnitelman riville** -vaihtoehdon asetukseksi **Ei**.

Budjettisuunnitelman rivit koostetaan kirjanpitotilin ja sijainnin mukaan. Voit kuitenkin jättää paikan numeron pois siten, että rivit koostetaan vain kirjanpitotilin mukaan. Määritä **Kohde**-välilehdessä **Sisällytä toimi budjettisuunnitelman riville** -vaihtoedon asetukseksi **Ei**.

Kentässä **Budjettisuunnitelman FTE-skenaario** voit määrittää skenaarion sisältämään budjettisuunnitelman kokopäivätoimisuuksien (FTE) lukumäärän. Tämä kenttä on rajoitettu määrä-tyyppisille skenaarioille, jotka sisällytetään kohdebudjettisuunnitelmaan. Jos valitset FTE-skenaarion, sinun on myös valittava FTE-päätili. Tätä tiliä käytetään määrä-tyyppisten budjettisuunnitelmarivien luontiin 

Lähteessä valittu budjettisuunnitteluprosessi ja budjettisuunnitelman skenaario määrittävät kohteen budjettisuunnitteluprosessin ja -skenaarion. Koska nämä määritteet on liitetty ennusteen toimille, niiden on vastattava budjettisuunnitelmaa. Näin ollen näitä määritteitä ei voida muokata kohteessa.

### <a name="generate-budget-plan-from-project-forecasts"></a>Muodosta budjettisuunnitelma projektiennusteista

**Muodosta budjettisuunnitelma projektiennusteista** -prosessi, samoin kuin **Muodosta budjettisuunnitelma ennusteen toimista** -prosessi sisältää mahdollisuuden sisällyttää projektin määrät (tunnit, kulut ja nimikkeet) määräskenaarioon. Näillä kahdella prosessilla on samankaltaiset suodattimet budjettisuunnitelman asettelun sarakkeille. 

**Lähde**-välilehden kolme **Sisällytä tiliote** -osiossa olevaa vaihtoehtoa määrittävät, mitkä budjettisuunnitelman rivit luodaan. Nämä vaihtoehdot ovat samat kuin ne, jotka ovat käytettävissäsi, kun luot budjettitapahtumia suoraan projektiennusteista. Määritä **Tulos**-vaihtoehdon arvoksi **Kyllä** luodaksesi rivejä kuluille ja tuotoille. Määritä **KET** -asetukseksi **Kyllä** luodaksesi työ prosessitapahtumissa. Määritä **Palkanlaskennan kohdistus** -asetukseksi **Kyllä** luodaksesi rivejä palkanlaskennan vastatileille tuntitapahtumia varten. 

**Budjettiluokka**-kenttää ei ole, koska budjettiluokka (**Kulu** tai **Tuotto**) määrittyy lähteen perusteella. 

Voit käyttää projektibudjetteja lähteenä valitsemalla ennustemallin, joka sisältää projektibudjetin summat. Muista, että projektibudjetit luovat projektiennustetapahtumia, kun ne hyväksytään.

Jos haluat valita vain kulut tai tuotot budjettisuunnitelman riveille, käytä suodatinta valitaksesi **Budjetin päivitykset: Summan tyyppi = Kulu**. Jos haluat valita vain yhden ennustetyypin, käytä suodatinta valitaksesi **Budjetin päivitykset: Tapahtumatyyppi = *xxx***. 

Budjettisuunnitelman skenaarion muodostamiseen voi käyttää vain yhtä ennustemallia. Jos suoritat prosessin yhdelle ennustemallille, teet sitten päivityksen ja yrität määrittää toisen mallin, ensimmäinen malli korvataan, jos kyseessä ovat samat projekti- ja kirjanpitotilit. Jos haluat luoda budjettisuunnitelman skenaarion useammasta kuin yhdestä ennustemallista, muodosta ne eri budjettisuunnitelman skenaarioiksi ja käytä kohdistusvaihtoehtoja lisätäksesi yhdistääksesi ne toisessa skenaariossa. 

**Muodosta budjettisuunnitelma projektin toimista** -prosessi määrittää budjettisuunnitelman riville myös lähdeprojektin.

### <a name="generate-budget-plan-from-supply-forecast"></a>Muodosta budjettisuunnitelma tarjontaennusteesta

**Muodosta budjettisuunnitelma tarjontaennusteesta** -prosessin lähdesuodatusasetukset mallinnettiin **Siirrä ostobudjetti kirjanpitoon** -toiminnon jälkeen prosessin ja toiminnon samankaltaisuudesta johtuen.

### <a name="generate-budget-plan-from-demand-forecast"></a>Muodosta budjettisuunnitelma kysynnän ennusteesta

**Muodosta budjettisuunnitelma kysynnän ennusteesta** -prosessissa voit määrittää **Myyntitilaus** -asetukseksi **Kyllä** muodostaaksesi budjettisuunnitelman tuottorivit, **Kulutus**-asetukseksi **Kyllä** luodaksesi kulurivit, tai määrittää molemmaksi asetukseksi **Kyllä**.

### <a name="generate-budget-plan-from-budget-register-entries"></a>Luo budjettisuunnitelma budjettirekisterimerkinnöistä

**Luo budjettisuunnitelma budjettirekisterimerkinnöistä** -prosessissa lähteen on määritettävä vain yksi osamalli, yksi budjettikoodi ja yksi tapahtuman numero. Voit toisin sanoen luoda budjettisuunnitelman rivejä vain yhdelle budjettitapahtumalle kerrallaan. Voit käyttää useampia tapahtumia samassa budjettisuunnitelmassa suorittamalla prosessin kerran kullekin lähdetapahtumalle.

### <a name="generate-budget-plan-from-budget-plan"></a>Muodosta budjettisuunnitelma budjettisuunnitelmasta

**Muodosta budjettisuunnitelma budjettisuunnitelmasta** -prosessissa voit **Kohde**-välilehdessä olevien asetusvaihtoehtojen avulla määrittää uusia taloushallinnon dimensioita. Jos taloushallinnon dimensio on valittu, kyseistä arvoa käytetään kaikille budjettisuunnitelman riveille. Näin ollen voit käyttää yhtä budjettisuunnitelmaa muiden budjettisuunnitelmien pohjana, mutta voit myös määrittää esimerkiksi eri osaston tai kustannuspaikan uusille budjettisuunnitelmille.

## <a name="looking-back-from-the-budget-plan"></a>Näkymä budjettisuunnitelmasta takaisinpäin
### <a name="budget-plans-by-dimension-set-inquiry"></a>Budjettisuunnitelmat dimensioyhdistelmäkyselyn mukaan

**Budjettisuunnitelmat dimensioyhdistelmän mukaan** -kysely sisältää useita vaihtoehtoja, joiden avulla voit suorittaa kyselyn budjettisuunnitelman tietojen lähteen tunnistamiseksi. 

Valitse rivi ja napsauta **Budjettisuunnitelmarivit**-painiketta suorittaaksesi **Budjettisuunnitelmarivit**-kyselyn. Tulokset suodatetaan kyseisen rivin dimensioarvojen perusteella. Tämän jälkeen voit määrittää lisäparametreja. 

Käytä **Tarjontaennuste-** ja **Kysyntäennuste**-painikkeita näiden kyselyiden suorittamiseen. Molemmissa tapauksissa kysely etsii ennusterivejä, jotka olisivat voineet luoda budjettisuunnitelman rivit. 

Muihin saatavilla oleviin raportteihin kuuluu esimerkiksi **Ennusteen toimet budjettisuunnitelman mukaan** -raportti. Tämä raportti on erityisen hyödyllinen, kun haluat määrittää, onko toimi kohdistettu budjettisuunnitelmille oikein.




