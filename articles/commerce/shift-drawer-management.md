---
title: Vuoron ja kassan hallinta
description: Tässä ohjeaiheessa käsitellään miten määritetään ja käytetään vuoroja Commercen myyntipisteessä (POS).
author: jblucher
ms.date: 05/10/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RetailHardwareProfile, RetailTerminalTable
audience: Application User
ms.reviewer: josaw
ms.custom: 105011
ms.assetid: 49a0fcc9-d4db-45ad-8c4b-213ccaced82b
ms.search.region: global
ms.search.industry: Retail
ms.author: brshoo
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 2ac42c92d38299c20bfcb293ac062aa9e4b1c628
ms.sourcegitcommit: f4823a97c856e9a9b4ae14116a43c87f9482dd90
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/09/2021
ms.locfileid: "7779741"
---
# <a name="shift-and-cash-drawer-management"></a>Vuoron ja kassan hallinta

[!include [banner](includes/banner.md)]

Tässä ohjeaiheessa käsitellään miten määritetään ja käytetään vuoroja Commercen myyntipisteessä (POS).

Dynamics 365 Commercessa *vuoro* tarkoittaa myyntipisteen tapahtumatietojen keräämistä kahden päivämäärän välillä. Kunkin vuoron tavoitteeksi asetettua rahasummaa verrataan summaan, joka on laskettu ja ilmoitettu.

Yleensä vuorot avataan työpäivän alussa. Tässä vaiheessa käyttäjä ilmoittaa alkusumman, joka sisältää pohjakassan määrän. Myyntitapahtumia suoritetaan läpi päivän. Päivän lopussa kassa lasketaan ja sulkemisajan summat ilmoitetaan. Vuoro suljetaan ja Z-raportti luodaan. Z-raportti osoittaa yli- tai alijäämät.

## <a name="typical-shift-scenarios"></a>Tyypillisiä työvuoron tilanteita

Commerce sisältää erilaisia konfiguraatiomahdollisuuksia ja POS-toimintoja, jotka tukeva monia erilaisia myyntipisteen prosesseja päivän päättyessä. Tässä osassa kuvataan muutamia tyypillisiä työvuorotilanteita.

### <a name="fixed-till"></a>Kiinteä kassa

Perinteisesti tämä tilanne on eniten käytetty. Sitä käytetään edelleen kattavasti. ”Kiinteän kassan” vuorossa vuoro ja kassa liitetään tiettyyn kassakoneeseen. Niitä ei siirretä yhdestä kassakoneesta toiseen. ”Kiinteä kassan” vuoroa voi käyttää joko yksi käyttäjä tai se voidaan jakaa useiden käyttäjien kesken. ”Kiinteä kassan” vuorot eivät vaadi mitään erityistä määrittelyä.

### <a name="floating-till"></a>Juokseva kassa

”Juoksevassa kassassa” vuoro- ja kassalaatikko voidaan siirtää yhdestä kassakoneesta toiseen. Vaikka kassakoneessa voi olla vain yksi aktiivinen vuoro kassalaatikkoa kohden, vuorot voi keskeyttää ja jatkaa sitten myöhemmin tai eri kassakoneessa.

Esimerkiksi kaupassa on kaksi kassakonetta. Jokainen kassapääte avataan päivän alussa, kun myyjä avaa uuden vuoron ja toimittaa aloitussumman. Yhden kassan ollessa valmiina tauolle, kyseinen työntekijä keskeyttää vuoron ja poistaa kassapäätteen kassan. Kassakone on silloin muiden myyjien käytettävissä. Toinen kassanhoitaja voi kirjautua ja avata oman vuoronsa kassalla. Kun ensimmäisen kassan tauko on päättynyt, kassanhoitaja voi jatkaa vuoroaan, kun jokin muu kassakone on käytettävissä. ”Juoksevan kassan” vuorot eivät vaadi mitään erityistä määrittelyä tai lupaa.

### <a name="single-user"></a>Yksi käyttäjä

Käteisen ja kassalaatikkoa koskevan vastuun varmistamiseksi monet vähittäiskaupat sallivat vain yhden käyttäjän vuoroa kohti. Jos vain yksi käyttäjä voi käyttää työvuoroon liitettyä kassaa, kyseistä käyttäjää voidaan pitää yksin vastuussa mahdollisista eroavaisuuksista. Jos vuorossa on useampi kuin yksi käyttäjä, on vaikea määrittää kuka teki virheen tai kuka voi yrittää varastaa kassasta.

### <a name="multiple-users"></a>Useita käyttäjiä

Jotkin vähittäismyyjät ovat valmiit uhraamaan vastuullisuuden tason, jonka yksi käyttäjä vuorossa tarjoaa ja sallii useita käyttäjiä vuorossa. Tämä on normaali käytäntö tilanteessa, jossa käyttäjiä on enemmän kuin kassapäätteitä ja joustavuuden ja nopeuden tarve on merkittävämpi kuin mahdolliset tappiot. On myös tyypillistä, että myymäläpäälliköillä ei ole omaa vuoroa, mutta he voivat tarpeen mukaan käyttää minkä tahansa kassan vuoroa. Kirjautuakseen sisään ja käyttääkseen vuoroa, jonka toinen käyttäjä on avannut, hänellä on oltava **Salli useita vuorokirjautumisia** -POS-käyttöoikeus.

### <a name="shared-shift"></a>Jaettu vuoro

”Jaettuun vuoro" -konfiguraatio sallii vähittäismyyjillä olevan yhden vuoron useissa kassoissa, käteislaatikoissa ja käyttäjillä. Jaetulla vuorolla on yksi aloitussumma ja yksi sulkemissumma, joihin on laskettu kaikkien käteislaatikoiden summat. Jaettu vuoro on tyypillinen, kun käytetään kannettavia laitteita. Tällöin kassalaatikkoa ei ole varattu tietylle kassapäätteelle. Sen sijaan kaikki kassapäätteet voivat jakaa yhden kassalaatikon.

Voidakseen käyttää jaettuja vuoroja myymälässä, kassa on määritettävä ”jaetuksi vuorokassaksi” kohdassa **Retail ja Commerce\> Kanavan asetukset \> Myyntipisteen asetukset \> POS-profiilit \> laitteistojen laiteprofiilit \> kassalaatikko**. Käyttäjillä on oltava vähintään jaetut vuorokäyttöoikeudet (Salli hallinnoi jaettua vuoroa ja Salli jaettu vuoro).

> [!NOTE]
> Kussakin myymälässä voi olla avoinna samanaikaisesti vain yksi jaettu vuoro. Samassa myymälässä voi käyttää jaettuja vuoroja ja erillisiä vuoroja.

## <a name="shift-and-drawer-operations"></a>Vuoro- ja kassatoiminnot

Vuoron tilaa voidaan muuttaa tai kassassa olevaa rahasummaa voidaan suurentaa tai pienentää eri toiminnoilla. Tässä osassa käsitellään näitä Modern POS:n ja Cloud POS:n vuorotoimintoja.

### <a name="open-shift"></a>Avoin vuoro

Myyntipisteen kirjanpitotapahtumaan eli myyntiin, palautukseen tai asiakastilaukseen päättyvien toimintojen suorittaminen edellyttää, että käyttäjällä on aktiivinen ja avoin vuoro.

Käyttäjä kirjautuessa sisään myyntipisteessä, järjestelmä tarkistaa ensin, onko aktiivinen vuoro kassalla nykyisen käyttäjän käytettävissä. Mikäli aktiivista vuoroa ei ole käytettävissä, käyttäjä voi avata uuden vuoron, jatkaa aiemmin luotua vuoroa tai kirjautua sisään muuhun kuin kassatilaan järjestelmän määrityksistä ja käyttäjien käyttöoikeuksista riippuen.

### <a name="declare-start-amount"></a>Tilitä aloitussumma

Tämä toiminto on usein ensimmäisenä juuri avatussa vuorossa. Tätä toimintoa varten käyttäjät määrittävät käteissumman, joka kassassa on vuoron alkaessa. Tämä toiminto on tärkeä, koska yli-/alijäämä työvuoroa suljettaessa tehtävässä laskelmassa otetaan huomioon alkusummana.

### <a name="float-entry"></a>Liukuva merkintä

*Liukuvat merkinnät* ovat muita kuin myyntitapahtumia, jotka suoritetaan aktiivisen vuoron aikana. Ne lisäävät kassassa olevan käteisen määrää. Tyypillinen esimerkki liukuvasta merkinnästä on vaihtorahan lisääminen kassaan, kun käteistä on vähän.

### <a name="tender-removal"></a>Maksuvälineen poisto

*Maksuvälineen poistot* ovat muita kuin myyntitapahtumia, jotka suoritetaan aktiivisen vuoron aikana, kun kassassa olevan käteisen määrää halutaan vähentää. Tätä toimintoa käytetään useimmiten yhdessä eri vuoron liukuvan merkinnän kanssa. Esimerkiksi kassa 1 sisältää vain vähän käteistä, joten kassan 2 käyttäjä suorittaa maksuvälineen poiston ja pienentää kassan summaa. Käyttäjä kassalla 1 tekee liukuvan merkinnän lisätäkseen oman kassansa rahan määrää.

### <a name="suspend-shift"></a>Keskeytä vuoro

Käyttäjät voivat keskeyttää aktiivisen vuoronsa ja vapauttaa tilaa valitussa kassakoneessa toiselle käyttäjälle tai siirtää vuoronsa toiseen kassakoneeseen (tässä tapauksessa vuoroa kutsutaan usein kelluvan kassan vuoroksi).

Vuoron keskeyttäminen estää vuoron uudet tapahtumat tai muutokset ennen vuoron jatkamista.

### <a name="resume-shift"></a>Jatka vuoroa

Tämä toiminto antaa käyttäjälle mahdollisuuden jatkaa keskeytettyä vuoroa kassakoneessa, jossa ei ole vielä aktiivista vuoroa.

### <a name="tender-declaration"></a>Kassan laskeminen maksuvälineittäin

Tämä toiminto suoritetaan tämän hetkisen kassan kokonaissumman määrittämiseksi. Käyttäjät suorittavat useimmiten tämän toiminnon ennen kuin sulkevat vuoron. Tätä määritettyä arvoa verrataan odotettuun vuoron summaan yli- tai alijäämäsummaa laskettaessa.

### <a name="safe-drop"></a>Toimitus kassakaappiin

Aktiivisessa vuorossa kassakaappiin toimitukset voidaan suorittaa milloin tahansa. Tämä toiminto poistaa rahaa kassasta, jotta se voidaan siirtää turvallisempaan paikkaan, kuten toimiston kassakaappiin. Kassakaappiin toimitukseen kirjattu kokonaissumma sisältyy edelleen vuoron summiin, mutta sitä ei tarvitse laskea osaksi kassan laskemista maksuvälineittäin.

### <a name="bank-drop"></a>Toimitus pankkiin

Pankkiin toimitukset suoritetaan aktiivisille vuoroille, kuten kassakaappiin toimitukset. Tämä toiminto poistaa rahat vuorosta pankkitalletuksen valmistua varten.

### <a name="blind-close-shift"></a>Piilotettu suljettu vuoro

*Piilotettuina suljetut vuorot* eivät ole enää aktiivisia, mutta niitä ei ole suljettu kokonaan. Toisin kuin keskeytettyjä vuoroja, piilotettuina suljettuja vuoroja ei voi jatkaa. Toimintoja, kuten Ilmoita aloitussumma ja kassan laskeminen maksuvälineittäin voidaan suorittaa myöhemmin tai eri rekisteristä.

Piilotettuina suljettuja vuoroja käytetään usein, kun halutaan vapauttaa rekisteri uutta käyttäjää tai vuoroa varten ilman, että vuoro pitää ensin inventoida, täsmäyttää ja sulkea ensin kokonaan.

### <a name="close-shift"></a>Sulje vuoro

Tämä toiminto laskee vuoron kokonaissumman, yli- ja alijäämäsummat sekä viimeistelee aktiivisen tai piilotettuna suljetun vuoron. Käyttäjän käyttöoikeuksien mukaan myös Z-raportti tulostetaan vuoroa varten. Suljettuja vuoroja ei voi jatkaa tai muokata.

### <a name="print-x"></a>Tulosta X

Tämä toiminto luo ja tulostaa X-raportin nykyiselle aktiiviselle vuorolle.

### <a name="reprint-z"></a>Tulosta Z uudelleen

Tämä toiminto tulostaa uudelleen viimeisen Z-raportin, jonka järjestelmä loi, kun työvuoro on suljettiin.

### <a name="manage-shifts"></a>Ylläpidä työvuoroja

Tämä toiminto antaa käyttäjälle mahdollisuuden tarkastella kaikkia myymälän aktiivisia, keskeytettyjä ja piilotettuina suljettuja vuoroja. Käyttäjät voivat suorittaa lopulliset sulkemismenettelyt, kuten kassan laskemisen maksuvälineittäin ja piilotettuna suljettujen vuorojen sulkemisen, käyttäjien käyttöoikeuksista riippuen. Tämä toiminto antaa käyttäjille mahdollisuuden myös tarkastella ja poistaa virheellisiä vuoroja siinä harvinaisessa tapauksessa, että vuoro jää virhetilaan offline- ja online-tiloja vaihdettaessa. Tällaisissa virheellisissä vuoroissa ei ole mitään täsmäytyksessä vaadittavia taloushallinnon tietoja tai tapahtumatietoja.

## <a name="shift-and-drawer-permissions"></a>Vuorojen ja kassan oikeudet

Seuraavat POS-käyttöoikeudet vaikuttavat siihen, mitä käyttäjä voi tai ei voi tehdä eri tilanteissa:

- **Salli piilottava sulkeminen**
- **Salli X-raportin tulostus**
- **Salli Z-raportin tulostaminen**
- **Salli kassan laskeminen maksuvälineittäin**
- **Salli liukuva kassatilitys**
- **Avaa kassa ilman myyntiä**
- **Salli useita vuorokirjautumisia** – Tämä oikeus sallii käyttäjän kirjautua sisään ja käyttää vuoroa, jonka toinen käyttäjä on avannut. Käyttäjät, joilla ei ole tätä oikeutta voivat kirjautua sisään ja käyttää vain vuoroa, jonka ovat avanneet.
- **Salli jaetun vuoron hallinta** – Käyttäjillä täytyy olla oikeus avata ja sulkea jaettu vuoro.
- **Salli jaetun vuoron käyttö** – Käyttäjillä täytyy olla lupa kirjautua sisään ja käyttää jaettua vuoroa.

## <a name="back-office-end-of-day-considerations"></a>Taustalla tapahtuviin päivän päätökseen liittyviä huomioon otettavia seikkoja

Tapa, jolla vuorot ja kassan täsmäytys tehdään myyntipisteessä eroaa siitä, miten tapahtumatiedoista tehdään yhteenveto tilinpäätöstä laskettaessa. On tärkeää, että ymmärrät tämän eron. Kokoonpanosta ja liiketoimintaprosesseistasi riippuen myyntipisteen vuoron tiedot (Z-raportti) ja tilinpäätös voivat antaa erilaisia tuloksia. Tämä ei välttämättä merkitse sitä, että vuoron tiedot tai tilinpäätöslaskelma ovat virheellisiä tai tiedoissa on ongelma. Se tarkoittaa sitä, että toimitetut parametrit saattavat sisältää ylimääräisiä tapahtumia tai vähemmän tapahtumia tai tapahtumat on laskettu eri tavalla.

Vaikka jokaisella myyjällä on eri liiketoimintavaatimukset, on suositeltavaa määrittää järjestelmä seuraavalla tavalla, että vältetään tilanteet, jossa tämäntyyppisiä eroja ilmenee:

Siirry **Retail ja Commerce \> Kanavat \> Myymälät \> kaikki myymälät \> laskelma/sulkeminen**, ja kullekin myymälälle luo sekä **Laskelmatapa**-kenttä että **Sulkemistapa**-kenttä **vuoroon**.

Tämän asetuksen avulla varmistat, että taustalaskelmat sisältävät samat tapahtumat kuin vuorot myyntipisteessä ja tiedoista tehdään yhteenveto kyseisen vuoron mukaan.

Lisätietoja lausunnoista ja sulkemismenetelmistä kohdassa [Vähittäismyynnin konfiguraatiot Retail-lausunnoissa](/dynamics365/unified-operations/retail/tasks/store-configurations-retail-statements).


[!INCLUDE[footer-include](../includes/footer-banner.md)]