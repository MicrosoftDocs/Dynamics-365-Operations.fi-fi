---
title: Vuoron- ja kassanhallinta
description: "Tässä artikkelissa käsitellään kahden vähittäismyynnin myyntipistetyypin vuoron määrittämistä ja käyttöä. Vuoro voi olla jaettu tai erillinen. Useat käyttäjät voivat käyttää jaettuja vuoroja useassa paikassa, kun taas vain yksi työntekijä voi käyttää erillistä vuoroa."
author: rubencdelgado
manager: AnnBe
ms.date: 02/15/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: RetailHardwareProfile, RetailTerminalTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 105011
ms.assetid: 49a0fcc9-d4db-45ad-8c4b-213ccaced82b
ms.search.region: global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 8a24f8adc4f7886a1f942d83f7a4eb12e7034fcd
ms.openlocfilehash: c1483d3240d266845cea7789b70c038cb98fdfcc
ms.contentlocale: fi-fi
ms.lasthandoff: 03/22/2018

---

# <a name="shift-and-cash-drawer-management"></a>Vuoron- ja kassanhallinta

[!include [banner](includes/banner.md)]

Tässä artikkelissa käsitellään kahden vähittäismyynnin myyntipistetyypin vuoron määrittämistä ja käyttöä. Vuoro voi olla jaettu tai erillinen. Useat käyttäjät voivat käyttää jaettuja vuoroja useassa paikassa, kun taas vain yksi työntekijä voi käyttää erillistä vuoroa.

Vähittäismyynnin myyntipistevuoroja on kahdenlaisia: erillinen ja jaettu. Yksi työntekijä kerrallaan voi käyttää erillistä vuoroa. Useat käyttäjät voivat käyttää jaettua vuoroa useassa paikassa. Niillä voikin luoda tehokkaasti yhden vuoron useille myymälän työntekijöille.

## <a name="standalone-shifts"></a>Erilliset vuorot
Erillisiä vuoroja käytetään perinteisissä kiinteissä myyntipisteskenaarioissa, joissa kassa täsmätään erikseen jokaisessa myyntipisteen kassakoneessa. Esimerkiksi elintarvikemyymälässä on tavallisesti useita kiinteitä myyntipisteen kassakoneita ja kullekin kassakoneelle on määritetty kassa. Tässä tapauksessa jokaisessa kassakoneessa käytetään todennäköisesti erillistä vuoroa ja kassa vastaa kassasta tai kassakoneen fyysisestä kassasta. Erillinen vuoro käsittää kaikki kassakoneen tapahtumat kassan työvuoron aikana. Tehtäviä voivat olla kassaan talletettu alkusumma, kaikki poistot ja lisäykset kassaan eri toiminnoilla, kuten toimitukset pankkiin ja liukuva merkintä, ja kassan laskeminen maksuvälineittäin vuoron lopussa.

### <a name="set-up-a-stand-alone-shift"></a>Määritä erillinen vuoro

Erillinen vuoro määritetään kassatasolla. Tässä menettelyssä käsitellään erillisen vuoron määrittäminen myyntipisteen kassakoneessa.

1.  Valitse **Vähittäismyynti** &gt; **Kanavan asetukset** &gt; **Myyntipisteiden asetukset** &gt; **Myyntipisteiden profiilit** &gt; **Laiteprofiilit**.
2.  Valitse erillisessä vuorossa käytettävä laiteprofiili.
3.  Vahvista **Kassa**-pikavälilehdessä, että **Jaetun vuoron kassa** -asetukseksi on valittu **Ei**.
4.  Valitse **Tallenna**.
5.  Valitse **Vähittäismyynti** &gt; **Kanavan asetukset** &gt; **Myyntipisteen asetukset** &gt; **Kassakoneet**.
6.  Valitse ensin kassakone, jossa käytetään erillistä vuoroa, ja sitten **Muokkaa**.
7.  Valitse **Laiteprofiili**-kentässä sama laiteprofiili, jonka valitsit vaiheessa 2.
8.  Valitse **Tallenna**.
9.  Valitse **Vähittäismyynti** &gt; **Vähittäismyynnin IT** &gt; **Jakeluaikataulu**.
10. Synkronoi myyntipisteen muutokset valitsemalla ensin **1090**-jakeluaikataulu ja sitten **Suorita nyt**.

### <a name="use-a-stand-alone-shift"></a>Käytä erillistä vuoroa

1.  Kirjaudu myyntipisteeseen.
2.  Jos yhtään avointa vuoroa ei ole, valitse **Avaa uusi vuoro**.
3.  Valitse **Tilitä aloitussumma** -toiminto ja määritä kassaan työpäivän alussa lisättävän kassan määrä.
4.  Tee muutamia tapahtumia.
5.  Laske jäljellä oleva kassa valitsemalla päivän lopussa **Laske kassa maksuvälineittäin**.
6.  Anna kassan summa ja tallenna maksuvälineittäin laskettu kassa valitsemalla **Tallenna**.
7.  Sulje vuoro valitsemalla **Sulje vuoro**.

**Huomautus:** Vuoron aikana on käytettävissä muita toimintoja sen mukaan, mitä liiketoimintaprosesseja on käytössä. **Toimitus kassakaappiin**-, **Toimitus pankkiin**- ja **Maksuvälineen poisto** -toiminnoilla voidaan poistaa rahaa kassasta päivän aikana tai ennen vuoron sulkemista. Jos kassa käy vähiin, kassaa voidaan lisätä **Liukuva merkintä** -toiminnolla.

## <a name="shared-shifts"></a>Jaetut vuorot
Jaettua vuoroa käytetään ympäristössä, jossa kassalla tai kassaryhmällä on useita käyttäjiä työpäivän aikana. Jaettua vuoroa käytetään yleensä mobiilimyyntipisteympäristöissä. Mobiiliympäristössä kassoja ei määritetä henkilökohtaisesti eikä yksittäinen henkilö vastaa tietystä kassasta. Sen sijaan kaikkien kassojen on voitava hoitaa myynti ja täydentää kassaa heitä lähimmässä kassassa. Tässä skenaariossa jaetut kassat sisältyvät jaettuun vuoroon. Kaikki jaetun vuoron kassat sisältyvät samaan vuoroon, jotta vuoron kassanhallintaan liittyvät toimet voidaan hoitaa. Vuoron alkusumman pitäisikin siksi sisältää kaikkien jaettuun vuoroon sisältyvin kassojen yhteiskassavarat. Samoin kassan laskeminen maksuvälineittäin on kaikkien jaettuun vuoroon sisältyvin kassojen yhteiskassavarat. **Huomautus:** Kussakin myymälässä voi olla avoinna samanaikaisesti vain yksi jaettu vuoro. Samassa myymälässä voi käyttää jaettuja vuoroja ja erillisiä vuoroja.

### <a name="set-up-a-shared-shift"></a>Määritä jaettu vuoro

1.  Valitse **Vähittäismyynti** &gt; **Kanavan asetukset** &gt; **Myyntipisteiden asetukset** &gt; **Myyntipisteiden profiilit** &gt; **Laiteprofiilit**.
2.  Valitse jaetussa vuorossa käytettävä laiteprofiili.
3.  Valitse **Kassa**-pikavälilehdessä **Jaetun vuoron kassa** -asetukseksi **Kyllä**.
4.  Valitse **Tallenna**.
5.  Valitse **Vähittäismyynti** &gt; **Kanavan asetukset** &gt; **Myyntipisteen asetukset** &gt; **Kassakoneet**.
6.  Valitse ensin kassakone, jossa käytetään jaettua vuoroa, ja sitten **Muokkaa**.
7.  Valitse **Laiteprofiili**-kentässä sama laiteprofiili, jonka valitsit vaiheessa 2.
8.  Valitse **Tallenna**.
9.  Valitse **Vähittäismyynti** &gt; **Vähittäismyynnin IT** &gt; **Jakeluaikataulu**.
10. Synkronoi myyntipisteen muutokset valitsemalla ensin **1090**-jakeluaikataulu ja sitten **Suorita nyt**.

### <a name="use-a-shared-shift"></a>Käytä jaettua vuoroa

1.  Kirjaudu myyntipisteeseen.
2.  Jos myyntipistettä ei ole vielä liitetty laiteasemaan, aktivoi jaetun vuoron laiteasema valitsemalla ensin **Muu kuin kassatoiminto** ja sitten **Valitse laiteasema** -toiminto. Tämä vaihe on tarvittava tehdä vain, kun kassakone lisätään ensimmäisen kerran jaettuun vuoroympäristöön.
3.  Kirjaudu ulos myyntipisteestä ja kirjaudu takaisin sisään.
4.  Valitse **Luo uusi vuoro**.
5.  Valitse **Tilitä aloitussumma**.
6.  Anna myymälän kaikkien jaettuun vuoroon sisältyvien kassojen aloitussumma ja valitse sitten **Tallenna**.
    -   Lisää aloitussumman osa jokaiseen seuraavaan kassaan, aktivoi laiteasema **Valitse laiteasema**-toiminnolla.
    -   Voit lisätä tietyn kassan kassaan **Avaa kassa** -toiminnolla.
    -   Jatka, kunnes kaikilla jaetun vuoron kassoilla on osa aloitussummaa.

7.  Avaa päivän lopussa kukin kassa ja poista kassavarat.
8.  Kun olet poistanut kassavarat viimeisestä kassasta, laske kaikki kassat.
9.  Laske kaikkien jaetun vuoron kassojen kokonaiskassa **Laske kassa maksuvälineittäin** -toiminnolla.
10. Sulje jaettu vuoro **Sulje vuoro** -toiminnolla.

## <a name="shift-operations"></a>Vuorotoiminnot
Vuoron tilaa voidaan muuttaa tai kassassa olevaa rahasummaa voidaan suurentaa tai pienentää eri toiminnoilla. Seuraavassa osassa käsitellään näitä Dynamics 365 for Retail Modern POS:n ja Cloud POS:n vuorotoimintoja.

**Avoin vuoro**

Myyntipisteen kirjanpitotapahtumaan eli myyntiin, palautukseen tai asiakastilaukseen päättyvien toimintojen suorittaminen edellyttää, että käyttäjällä on aktiivinen ja avoin vuoro.  

Myyntipisteeseen kirjauduttaessa järjestelmä tarkistaa ensimmäiseksi, onko käyttäjällä aktiivista vuoroa nykyisessä kassakoneessa. Jos näin ei ole, käyttäjä voi avata uuden vuoron, jatkaa aiemmin luotua vuoroa tai kirjautua sisään muuhun kuin kassatilaan järjestelmän määrityksistä ja käyttäjien käyttöoikeuksista riippuen.

**Tilitä aloitussumma**

Tämä toiminto on usein ensimmäisenä juuri avatussa vuorossa. Käyttäjät määrittävät käteissumman, joka kassassa on vuoron alkaessa. Tämä on tärkeää, koska vuoroa suljettaessa tapahtuvan laskennan yli- tai alijäämä selittää tämän summan.

**liukuva merkintä**

Liukuvat merkinnät ovat muita kuin myyntitapahtumia, jotka suoritetaan aktiivisen vuoron aikana. Ne lisäävät kassassa olevan käteisen määrää. Yleinen esimerkki liukuvasta merkinnästä on muutoksen lisääminen kassaan, kun käteistä on vähän.

**Maksuvälineen poisto**

Maksuvälineen poistot ovat muita kuin myyntitapahtumia, jotka suoritetaan aktiivisen vuoron aikana, kun kassassa olevan käteisen määrää halutaan vähentää. Tätä käytetään useimmiten yhdessä eri vuoron liukuvan merkinnän kanssa. Esimerkiksi kassa 1 sisältää vain vähän käteistä, joten kassan 2 käyttäjä suorittaa maksuvälineen poiston ja pienentää kassan summaa. Kassakoneen 1 voisi sitten suurentaa summaa tekemällä liukuvan merkinnän.

**Keskeytä vuoro**

Käyttäjät voivat keskeyttää aktiivisen vuoronsa ja vapauttaa tilaa valitussa kassakoneessa toiselle käyttäjälle tai siirtää vuoronsa toiseen kassakoneeseen (jota kutsutaan usein kelluvaksi kassaksi). 

Vuoron keskeyttäminen estää vuoron uudet tapahtumat tai muutokset ennen vuoron jatkamista.

**Jatka vuoroa**

Tämä toiminto antaa käyttäjälle mahdollisuuden jatkaa keskeytettyä vuoroa kassakoneessa, jos ei ole vielä aktiivista vuoroa.

**Kassan laskeminen maksuvälineittäin**

Kassan laskeminen maksuvälineittäin on toiminto, jonka tekemällä käyttäjä määrittää kassassa kyseisellä hetkellä olevan käteisen yhteissumman. Useimmiten tämä tehdään ennen vuoron sulkemista. Tätä arvoa verrataan odotettuun vuoroon yli- tai alijäämäsumman laskettaessa.

**Toimitus kassakaappiin**

Aktiivisessa vuorossa kassakaappiin toimitukset voidaan suorittaa milloin tahansa. Tämä toiminto poistaa rahaa kassasta, jotta se voidaan siirtää turvallisempaan paikkaa, kuten toimiston kassakaappiin. Kassakaappiin toimitukseen kirjattu kokonaissumma sisältyy edelleen vuoron summiin, mutta sitä ei tarvitse laskea osaksi kassan laskemista maksuvälineittäin.

**Toimitus pankkiin**

Pankkiin toimitukset suoritetaan aktiivisille vuoroille, kuten kassakaappiin toimitukset. Tämä toiminto poistaa rahat vuorosta pankkitalletuksen valmistua varten.

**Piilotettu suljettu vuoro**

Sokkona suljettu vuoro on vuoro, joka ei ole enää aktiivinen, mutta jota ei ole täysin suljettu. Sokkona suljettuja vuoroja ei voi jatkaa kuten keskeytettyjä vuoroja, mutta menettelyt, kuten aloitussummien tilittäminen ja kassan laskeminen maksuvälineittäin, voidaan suorittaa myöhemmin tai eri rekisteristä.

Sokkona suljettuja vuoroja käytetään usein, kun halutaan vapauttaa rekisteri uutta käyttäjää tai vuoroa varten ilman, että vuoro pitää ensin inventoida, täsmäyttää ja sulkea ensin kokonaan. 

**Sulje vuoro**

Tätä toiminto laskee vuoron kokonaissumman, yli- ja alijäämäsummat sekä viimeistelee aktiivisen tai piilotettuna suljetun vuoron. Suljettuja vuoroja ei voi jatkaa tai muokata.  

**Ylläpidä työvuoroja**

Tämä toiminto antaa käyttäjälle mahdollisuuden tarkastella kaikkia myymälän aktiivisia, keskeytettyjä ja piilotettuina suljettuja vuoroja. Käyttäjät voivat suorittaa lopulliset sulkemismenettelyt, kuten kassan laskemisen maksuvälineittäin ja sokkona suljettujen vuorojen sulkemisen, käyttäjien käyttöoikeuksista riippuen. Tämän toiminto käyttäjille mahdollisuuden myös tarkastella ja poistaa virheellisiä vuoroja siinä harvinaisessa tapauksessa, että vuoro jää virhetilaan offline- ja online-tiloja vaihdettaessa. Tällaisissa virheellisissä vuoroissa ei ole mitään täsmäytyksessä tarvittavia taloushallinnon tietoja tai tapahtumatietoja. 

