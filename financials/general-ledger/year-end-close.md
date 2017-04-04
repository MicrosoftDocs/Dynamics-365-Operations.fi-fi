---
title: Tilikauden lopetus
description: "Tässä aiheessa kuvataan tarvittavat asetukset ja ohjeet kirjanpidon vuoden sulkemisprosessi on käynnissä."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: LedgerClosingSheet
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 14091
ms.assetid: c64eed1d-df17-448e-8bb6-d94d63b14607
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 926ee087a0e0c4743f29315b1d82c7d37e95be28
ms.openlocfilehash: 22233cfa1df79076c8ea42f75ea309bac990d574
ms.lasthandoff: 03/31/2017


---

# <a name="year-end-close"></a>Tilikauden lopetus

Tässä aiheessa kuvataan tarvittavat asetukset ja ohjeet kirjanpidon vuoden sulkemisprosessi on käynnissä. 

Tilikauden lopussa koko vuoden saldot siirretään uuden vuoden sulkemisprosessi on suoritettava. Useimmissa organisaatioissa suorittaa vuoden sulkemisprosessi useita kertoja. Ensimmäisen kerran olisi saada saldot siirretään uuteen tilivuoteen. Vuoden lopun sulkemisen jälkeen voidaan suorittaa uudelleen, kuten monta kertaa on pakko siirtää saldot uuden tilikauden, että ne voi muuttaa. 

Sulje prosessi vuoden lopun aikana, siellä on kaksi mahdollista luodut tapahtumat. Avattaessa-tapahtuman aina luodaan ja käytetään luoda uuden tilikauden saldot. Tapahtuman avaaminen uuden tilikauden taseen kirjanpidon tilien saldot näkyvät ja uuden tilikauden tulos kirjanpidon tilien saldot jakamattoman kirjanpitotilin saldoja. Viimeinen tapahtuma luodaan myös tuomaan luopua sulkea tilikauden tulos-tilien saldojen.

## <a name="prepare-to-run-the-year-end-close"></a>Valmistele vuoden lopun sulkeminen
Ennen kuin suoritat Sulje lopetukseen, tarkista seuraavat asetukset: 

**Päätili**-sivulla:

-   Tarkista **Main tyyppi** on määritetty oikein kunkin päätili. Main-tilityypin käytetään määrittämään, onko päätilin saldoa otetaan käyttöön liitteenä alkusaldo tai kiinni olevaan voittovarojen avattaessa-tapahtumaan.
-   **Avata tilin** kenttää voidaan käyttää ensisijaisen tilin saldo siirretään uuden päätilin vuoden lopun sulkemisen aikana. Uusi päätili on kirjoitettu **avata tilin** kenttä. Yleensä tätä käytetään tärkeimmät tasetilien kun päätili inaktiivinen ja uusi päätili käytetään uuden tilikauden.

- **Kirjanpitoparametrien** sivulla kohdassa **tilikauden päättäminen**:

-   **DEL Sulje vuosi tapahtumien** asetusta käytetään määrittämään, onko järjestelmän luoma avaustapahtuma-edellisen vuoden lopun sulkeminen olisi poistettava, kun vuoden lopun sulkeminen suoritetaan uudelleen. Jos tämä asetus on määritetty **Kyllä**, edellisen avaustapahtuma poistetaan ja avataan uusi tapahtuma luodaan perusteella nykyiset saldot. Jos tämä asetus on määritetty **ei**, edellisen avaustapahtuma pysyy ja muita avaustapahtuma luodaan siirtää saldoja toimittaa edellisen vuoden lopun sulkemisen jälkeen kirjatut tapahtumat voi muuttaa.
-   **Luo päätöstapahtumat siirron yhteydessä** asetusta käytetään Luo päätöstapahtumat nolla tulos-tilien saldojen jotta sulkea tilikauden. Jos tämä asetus on määritetty **Kyllä**, avaustapahtuma ja viimeinen tapahtuma luodaan. Jos tämä asetus on määritetty **ei**, vain aloittava tapahtuma luodaan seuraavan tilikauden saldot siirretään. Tuloslaskelman tilien saldot säilyvät tilikauden lopussa.
-   **Aseta tilikauden tilaksi suljettu pysyvästi** vaihtoehtoa käytetään määrittää tilivuoden pysyvästi suljettu tila. Käytä tätä asetusta harkiten, sillä kaikki jaksot pysyvästi suljettu tila ei voi avata uudelleen, estää postittamisen tilikauden oikaisut. Se on parasta, voit asettaa **ei**.
-   **Tositenumero on täytettävä** asetusta käytetään määrittämään, onko tositteen numero on pakollinen, kun vuoden sulkemisprosessi on käynnissä. Se on parasta, voit helposti tunnistaa avattaessa-tapahtuman tositenumero vaativat.

- **Kirjanpidon vuosikalenterin** sivulla:

-   Seuraavan tilivuoden on oltava olemassa ennen suorittamista vuoden lopun sulkeminen. Seuraavan tilivuoden vaaditaan, jotta voidaan luoda alkaen saldoja kaudesta.

- **Kirjanpitokalenteri** sivulla:

-   Valinnainen: Kutakin tilijaksoa sulkea tilikauden voidaan määrittää **pitoon** kirjoittamisen uusien tapahtumien estämiseksi. Oikaisevia tunnistetaan, kun edelleen pito jaksot voidaan avata kirjaa oikaisevia, vaikka koko vuoden sulkemisprosessi on jo suoritettu.

## <a name="define-year-end-close-templates"></a>Määritä koko vuoden tiiviissä mallit
Järjestelmä on määritetty, kun vuoden sulkemisprosessi voi suorittaa. - **Tilinpäätös** -sivulla voidaan määrittää mallin osalta suoritetaan, jonka tilinpäätös prosessin oikeussubjektien ryhmän. Malli kunkin vuoden lopun sulkemisen yhteydessä käytetään uudestaan, mutta sitä voi muokata organisaation muuttuessa. 

Ensimmäisen kerran, Määritä **nimi** mallin, ja valitse kirjanpidon vuosikalenteri. Ryhmänimi pitäisi sisällyttää oikeussubjektien ryhmän.  Esimerkiksi mallit voi määrittää perusteella muodostamiin, Pohjois-Amerikan oikeussubjektien oikeussubjektien EMEA ja APAC oikeussubjektien luotu eri ryhmistä. 

Seuraavaksi oikeushenkilöt voidaan lisätä malliin. Oikeushenkilöt voidaan lisätä organisaation hierarkian valitsemalla tai valitsemalla oikeushenkilöt. Jos organisaation hierarkian vain oikeushenkilöt hierarkiassa, joka käyttää valitun kirjanpidon vuosikalenterin lisätään malliin. Jos käytät oikeussubjektien mallin lisääminen, voidaan lisätä vain oikeussubjektien kanssa sama kirjanpidon vuosikalenteri. Sama kirjanpidon vuosikalenteri ei tarvita, sillä vuoden lopun sulkeminen suoritetaan tilikauden, joka voi vaihdella kalenteri kalenteri valitsemalla. 

Kun on lisätty oikeushenkilöt, Määritä jakamattoman päätilit kullekin oikeushenkilölle. **Syntynyt viime vuoden lopussa Sulje** kenttä päivitetään aina vuoden lopussa lähellä suoritetaan oikeushenkilölle. 

**Taloushallinnon dimension** -välilehteä käytetään määrittämään käytetään avattaessa-tapahtuman taloushallinnon dimensiot. Huomaa, että määrität asetukset vaikuttavat vain valittuun oikeushenkilöön **oikeushenkilöt** ruudukko. Toistetaan kullekin oikeushenkilölle Ruudukon asetukset. 

**Mitat taseen siirtää** käytetään määrittämään, onko taloushallinnon dimensiot kirjataan tasetileille tapahtumissa olisi säilytettävä aloittava tapahtuma. Se on paras käytäntö, Määritä tämän asetuksen arvoksi **Kyllä**. **Mitat tulos siirretään** käytetään määrittämään, mitkä tapahtumat kirjataan voitto- ja tappiotili taloushallinnon dimensiot siirretään voittovarojen päätili. Etsi ensin valittuun oikeushenkilöön asianmukaisen taloushallinnon dimensioita. Tähän sisältyisi kaikki taloushallinnon dimensiot kirjataan vuoden aikana vastaan vaikka taloushallinnon dimensio kuuluu aktiivinen tilirakenne. Määritä kunkin dimension joko seuraavaksi **sulkeminen yhden** tai **sulkea kaikki**.  Oletusarvo on **sulkea kaikki**, joka ylläpitää alkuperäinen taloushallinnon dimension arvot kirjattuja tapahtumia ja käyttää niitä varten luodaan avaamalla saldot jakamattoman voiton tilille. Alkusaldot erillisessä voittovarojen luodaan yksilöllinen taloushallinnon dimensioarvojen yhdistelmän. Jos **Sulje single** on valittu, kaikki kyseiseen taloushallinnon dimensioon kirjatut tapahtumat tiivistetään yhdeksi alkusaldo dimension arvon kenttään jälkeen jakamattoman **sulkeminen yhden**. Oletetaan esimerkiksi, että tilikauden kaikki tapahtumat on kirjattu päätilille - osaston tilille rakenteessa. Osaston Taloushallinnan dimension, mallin **Sulje single** on valittu ja 100 on annettu arvo. Jos kaikki osastot, 200, 300 ja 400 kirjattujen tapahtumien kokonaistulo on $100,000, yksi alkusaldon luodaan Retained tulot - 100. Jos valitset **sulkeminen yhden** ja taloushallinnon dimensioarvo jätetään tyhjäksi, kaikki tapahtumat kirjataan kertyneisiin voittovaroihin joilla dimensioarvo on tyhjä. 

Sulje tilinpäätösprosessi ei noudata tilirakenteissa. Tämä johtuu siitä, että tilirakenteissa voi muuttaa koko tilikauden ja aina ei ole mahdollista tunnistaa asiaa kesken näiden muutosten vuoksi.  Avaustapahtumat luodaan, kun saldot aikaistaa taloushallinnon dimensiot on määritelty vuoden lopussa Sulje malli. Alusta saldot tapahtumat voi sisällyttää taloushallinnon dimensiot enää nykyisen tilin rakenne ja segmentin yhdistelmiä, jotka eivät enää kelpaa valitun tilin rakenne. Jos organisaatio haluaa jättää taloushallinnon dimension on pidätetty ansaitsee alkusaldo, Määritä taloushallinnon dimension on **sulkeminen yhden** ja dimensioarvo jätetään tyhjäksi.

## <a name="run-the-year-end-close-process"></a>Suorittamalla Sulje tilinpäätösprosessi
Koko vuoden tiiviissä mallit luodaan, kun vuoden sulkemisprosessi on aloitettu valitsemalla **suorittaa tilikauden** toimintoruudussa. Valitse kaikki tai osajoukko oikeussubjektien malli, jonka haluat suorittaa vuoden lopun sulkemisen. Kun käynnissä tilinpäätöksen sulkea tilikauden ensimmäistä kertaa, todennäköisesti valitaan kaikki oikeushenkilöt Luo alkusaldot juridiset henkilöt. Jos käytät vuoden lopun sulkeminen uudelleen, voit ajaa-prosessin vain juridiset henkilöt, joille on kirjattu oikaisevia. 

Valitse tilikausi, jonka haluat suorittaa Sulje tilinpäätösprosessi vastaan. Jos tilivuoden viimeisen kauden on olemassa enemmän kuin yksi jakso **nimi** kenttä ole käytettävissä, voit valita mitä lopetuskausi suljetaan, tapahtuma kirjataan, jos asetukset on määritetty, voit luoda tapahtumaa suljetaan. 

Syötä tositteen tai numero, johon ei välttämättä vaadita riippuen yleensä asetusten kirjanpidon parametrit. Samaa tositenumeroa käytetään kaikkien vuoden lopussa Sulje prosessi valittu oikeushenkilöt. Tositteen numeroa ei luoda numerosarjan perusteella. On parasta, kirjoita tositteen numero, vaikka sitä ei vaadita. Tositenumero kirjoittamalla helpompaa uuden tilikauden avaaminen tapahtuma löytyy. Tositteen numeroa ei ole annettu, jos tosite on tyhjä, tapahtuman avaaminen. 

Jos haluat vaihtaa valitun tilikauden lähelle edellisen vuoden lopussa **kumota edellisen sulkemisen**, **Kyllä**. Vuoden lopun sulkeminen peruutetaan, mutta prosessi voi suorittaa milloin tahansa. Jos Sulje, tilinpäätöksen **syntynyt viime vuoden lopussa Sulje** on saatavilla. 

Vuoden sulkemisprosessi oletusarvo on ajo erätilassa. Se on parasta prosessi suoritetaan erätilassa käyttäjä palaa muihin toimiin. Vuoden lopussa sulkemisprosessi on valmis, **syntynyt viime vuoden lopussa Sulje** istunnon päivämäärä päivitetään.

Lisätietoja on ohjeaiheessa [sulkea kauden lopussa kirjanpidon](close-general-ledger-at-period-end.md).


