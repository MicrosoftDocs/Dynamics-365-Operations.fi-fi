---
title: Myyntipistekäyttöliittymän visuaaliset kokoonpanot
description: Tässä aiheessa on tietoja Dynamics 365 Commerce POS -käyttöliittymistä.
author: boycezhu
manager: annbe
ms.date: 09/22/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailTillLayout
audience: Application user
ms.reviewer: josaw
ms.custom: 90573
ms.assetid: a6868f93-02ed-4928-9f6a-3b7383e7e399
ms.search.region: global
ms.search.industry: Retail
ms.author: boycez
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 521fbd2c73adca1db38ba7258abf183f7350b109
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5231293"
---
# <a name="pos-user-interface-visual-configurations"></a>Myyntipistekäyttöliittymän visuaaliset kokoonpanot

[!include [banner](includes/banner.md)]


Microsoft Dynamics 365 Commerce -myyntipistekäyttöliittymät (POS) voidaan määrittää käyttäen visuaalisten profiilien ja näyttöasettelujen yhdistelmää, jotka on määritetty myymälöille, kassakoneille ja/tai käyttäjille. Tämä ohjeaihe sisältää tietoja niistä järjestelmän konfigurointivaihtoehdoista.

Seuraava kuva esittää eri yksiköiden suhteita, jotka muodostavat määriteltäviä aspekteja POS-käyttöliittymien välillä.

![POS-näytön asettelun yksikkö](../commerce/media/POS-layout-configuration-entities-diagram.png)

## <a name="visual-profile"></a>Visuaalinen profiili

Visuaaliset profiilit määritetään kassakoneisiin ja niitä käytetään määrittämään visuaalisia elementtejä, jotka ovat kassakonekohtaisia ja kaikille työntekijöille jaettuja. Jokainen käyttäjä, joka kirjautuu kassakoneeseen, näkee samat teemat, asettelun, värit ja kuvat.

![Myyntipisteen (POS) vaalea Tervetuloa-teema](../commerce/media/POS-Welcome-Screen-with-Light-theme.png)

![Myyntipisteen (POS) tapahtuman näytössä tumma teema](../commerce/media/POS-Transaction-Screen-with-Dark-theme.png)

- **Profiilinumero** – profiilinumero on visuaalisen profiilin yksilöivä tunnus.
- **Kuvaus** – kuvauksen avulla voit määrittää kuvaavan nimen, joka auttaa tunnistamaan oikean profiilin tilanteen mukaan.
- **Teema** – Käyttäjät voivat valita **vaalean** tai **tumman** sovellusteeman. Teema vaikuttaa koko sovelluksen fontin ja taustan väreihin.
- **Korostuksen väri** – korostuksen värejä käytetään koko myyntipisteessä erottamaan tai korostamaan tiettyjä visuaalisia elementtejä, kuten ruutuja, painikkeita tai hyperlinkkejä. Nämä elementit ovat yleensä toimintoja.
- **Otsikon väri** – voit määrittää sivun ylätunnisteen värin jälleenmyyjän brändivaatimusten täyttämiseksi.
- **Fonttimalli** – Voit valita **Vakio**- ja **Suurikokoiset** -fonttimallit. Fonttimalli vaikuttaa koko sovelluksen fonttikokoon. Oletusvalinta on **Vakio**.
- **Näytä aina sovelluspalkin otsikot** – Kun tämä asetus on käytössä, seliteteksti näkyy aina sovelluspalkin painikkeiden alla.
- **Asettelu** – Voit valita **Keskitetyn** ja **Oikean** asettelun väliltä. Asettelu vaikuttaa kirjautumisnäytön sisäänkirjautumisruudun tasaukseen. Oletusvalinta on **Keskitetty**.
- **Näytä päivämäärä/aika** – Kun tämä asetus on käytössä, päivämäärä ja kellonaika näkyvät myyntipisteen otsikossa ja kirjautumisnäytössä.
- **Näppäimistö** – Voit valita **Oletus-OS-näppäimistön** ja **Näytä numeronäppäimistön** väliltä määritelläksesi oletusnäppäimistön, jota käytetään kirjautumisnäytössä. Numeronäppäimistö on virtuaalinen näppäimistö, jota käytetään ensisijaisesti kosketuspohjaisissa laitteissa. Oletusvalinta on **Oletus-OS-näppäimistö**.
- **Logon kuva** – Voit määrittää logon kuvan, joka näkyy kirjautumisnäytössä. On suositeltavaa käyttää kuvaa, jonka tausta on läpinäkyvä. Tiedostokoko on pidettävä mahdollisimman pienenä, koska suurien tiedostojen tallentaminen ja lataaminen voivat vaikuttaa sovelluksen toimintaan ja suorituskykyyn.
- **Kirjautumisen tausta** – käyttäjät voivat määrittää kirjautumisnäytön taustakuvan. Taustakuvien tiedostokoot tulisi pitää mahdollisimman pieninä.
- **Tausta** – Käyttäjät voivat määrittää myös yhtenäisen taustakuvan käytettäväksi koko sovelluksessa yhtenäisen teemavärin sijaan. Kirjautumisnäytön taustakuvien osalta tiedoston koko on pidettävä mahdollisimman pienenä.

> [!NOTE]
> **Oikea** asettelu ja päivämäärän/ajan näyttö eivät koske kirjautumisnäyttöä suppeassa näkymässä.

Sinun on suoritettava jakelun aikataulutustehtävä **1090** ( **Rekisterit**), jotta voit synkronoida uusimmat visuaalisen profiilin määritykset kanava tietokantaan.

## <a name="screen-layouts"></a>Näytön asettelut

Näytön asettelun kokoonpano määrittää käyttöliittymän ohjausobjektien toiminnot, sisällön ja sijoittelut myyntipisteen **Tervetuloa**-näytössä ja **Tapahtuma**-näytössä.

![Myyntipisteen näytön asettelun näkymä](../commerce/media/POS-Screen-Layout-View.png)

- **Tervetuloa-näyttö** – Tervetuloa-näyttö on yleensä sivu, jonka käyttäjät näkevät, kun he ensin kirjautuvat myyntipisteeseen. Tervetuloa-näyttö voi koostua tavaramerkin kuvasta painikeruudukoista, jotka tarjoavat pääsyn myyntipisteen toimintoihin. Toiminnot, jotka eivät liity nykyiseen tapahtumaan sijoitetaan yleensä tähän näyttöön.

    ![Myyntipisteen aloitusnäyttö](../commerce/media/POS-Welcome-Screen.png)

- **Tapahtumanäyttö** – **Tapahtumanäyttö** – on POS-sovelluksen päänäyttö myyntitapahtumien ja tilausten käsittelyyn. Sisältö ja asettelu on määritetty näytön asettelun suunnittelutoiminnon avulla.

    ![Myyntipisteen tapahtumanäyttö](../commerce/media/POS-Transaction-Screen.png)

- **Oletusaloitusnäyttö** – jotkin vähittäismyyjät haluavat, että kassa siirtyy suoraan **Tapahtumanäyttöön** kirjautumisen jälkeen. **Oletusarvoisen aloitusnäytön** asetuksien avulla voit määrittää oletusarvoisen näytön, joka näkyy kirjautumisen jälkeen kussakin näyttöasettelussa.

### <a name="assignment"></a>Liitos

Näytön asettelut voidaan määrittää myymälän, kassakoneen tai käyttäjän tasolla. Käyttäjän määritys korvaa kassakoneen ja myymälän määritykset, ja kassakoneen määritys korvaa myymälän määrityksen. Yksinkertaisessa tilanteessa, jossa kaikki käyttäjät käyttävät samaa asettelua riippumatta kassakoneesta tai roolista, näytön asettelu voidaan määrittää vain myymälätasolla. Skenaarioissa, jossa tietyt kassakoneet tai käyttäjät vaativat erityisiä asetteluita, nuo asettelut voidaan määritellä asianmukaisesti.

Riippuen siitä, millä tasolla näytön asettelut on määritetty, sinun on suoritettava jakelun aikataulutustehtävä **1070** (**Kanavan määritys**), **1090** (**Rekisterit**) ja/tai **1060** ( **Henkilöstö**) synkronoidaksesi viimeisimmät ruudun asettelumääritykset kanavan tietokantaan.

### <a name="layout-sizes"></a>Asettelukoot

Suurin osa POS-käyttöliittymän aspekteista on herkästi reagoivia ja asettelu säätyy automaattisesti näytön koon ja suunnan perusteella. Kuitenkin myyntipisteessä **Tapahtuma**-ruutu on määritettävä jokaisen tarvittavan näytöntarkkuuden mukaan.

Käynnistettäessä POS-sovellus valitsee automaattisesti lähimmän laitteeseen määritellyn asettelun koon. Näytön asettelu voi sisältää myös sekä vaaka- että pystytilat sekä täysikokoisen ja tiivistetyn konfiguraatiot. Tämän vuoksi käyttäjät voidaan määrittää yhteen näyttöasetteluun, joka toimii myymälän erikokoissa ja erityyppisissä laitteissa.

![Myyntipisteen asettelukoot](../commerce/media/POS-Screen-Layout-Sizes.png)

- **Nimi** – Määritä kuvaava nimi, joka yksilöi näytön koon.
- **Asettelutyyppi** – POS-sovelluksessa voidaan näyttää sen käyttöliittymän erilaisia tiloja, että voidaan taata paras mahdollinen käyttäjäkokemus tietyllä laitteella.

    - **Modern POS – täydellinen** – täydelliset asettelut ovat yleensä parhaimmillaan suurissa näytöissä kuten PC-näytöissä tai tableteissa. Voit valita haluamasi asettelun käyttöliittymäelementit, määrittää elementtien koon ja sijoittelun sekä elementtien yksityiskohtaiset ominaisuudet. Täydelliset asettelut tukevat sekä vaaka- että pystykokoonpanoja.
    - **Modern POS – kompakti** – kompaktit asettelut sopivat parhaiten puhelimiin ja pieniin tabletteihin. Kompaktien laitteiden suunnittelumahdollisuudet ovat rajalliset. Voit määrittää kuitti- ja summaruutujen sarakkeet ja kentät.

- **Leveys ja korkeus** – arvot edustavat kuvapisteinä tehokasta näytön kokoa, joka vaaditaan asetteluun. Muista, että jotkin käyttöjärjestelmät käyttävät skaalausta korkean resoluution näytöissä.

> [!TIP]
> Löydät vaaditun asettelun koon, jota POS-näytön tarkkuus vaatii tarkastelemalla resoluutiota sovelluksessa. Käynnistä Myyntipiste ja siirry **Asetukset \> Istuntotietoja**. POS näyttää tällä hetkellä ladatun näyttöasettelun, asettelun koon ja sovellusikkunan resoluution.

![POS-istunnon tietosivu, joka näyttää tällä hetkellä ladatun näytön asettelun, asettelun koon ja sovellusikkunan resoluution](../commerce/media/POS-Session-Information.png)

### <a name="button-grids"></a>Painikeruudukot

Voit konfiguroida ja määrittää painikeruudukoiden POS-Tervetuloa-näytön ja **Tapahtuma**-näytön asettelun kullekin koolle näyttöasettelussa. Tervetuloa-näytön painikeruudukot on aseteltu automaattisesti vasemmalta oikealle, pienimmästä numerosta (Tervetuloa-näyttö 1) suurimpaan numeroon.

Koko myyntipisteen asetteluissa painikeruudukoiden sijoittelu on määritetty näytön asettelun suunnittelutyökalussa.

Kompakteissa myyntipisteiden asetteluissa painikeruudukot on aseteltu automaattisesti ylhäältä alas, pienimmästä numerosta (Tervetuloa-näyttö 1) suurimpaan numeroon. Niitä voidaan käyttää **Toimenpiteet**-valikossa.

![Kompaktit asettelun painikeruudukot](../commerce/media/Compact-View-Button-Grids.png)

> [!NOTE]
> Suunnitteluohjelman painikkeiden koot sovitetaan ikkunan kokoon, joten ne eivät välttämättä vastaa myyntipistesovelluksessa muodostuvia painikkeita. Voit simuloida painikeruudukon asettelun säätämällä suunnitteluikkunoihin saman koon kuin myyntipisteessä.

### <a name="images"></a>Kuvat

Voit määrittää kutakin näyttöasettelun kokoa varten kuvat, jotka sisällytetään POS-käyttöliittymään. POS-sovelluksen koko asetteluissa Tervetuloa-näyttöön voidaan määrittää yksi kuva. Kuva näkyy käyttöliittymän ensimmäisenä elementtinä vasemmalla puolella. **Tapahtuma**-näytössä kuvia voidaan käyttää välilehden kuvina tai logoina. Kompaktit myyntipisteen asettelut eivät käytä näitä kuvia.

### <a name="screen-layout-designer"></a>Näytön asettelun suunnittelutoiminto

Näytön asettelun suunnittelutoiminnon avulla voit määrittää myyntipisteen **Tapahtuma**-näytön eri puolia asettelun kullekin koolle sekä pysty- että vaaka-asennossa, ja sekä kokonaisissa että tiivistetyissä asetteluissa. Näytön asettelun suunnittelutoiminto käyttää ClickOnce-käyttöönottoteknologiaa lataamaan, asentamaan ja käynnistämään sovelluksen uusimman version aina, kun se avataan. Muista tarkistaa ClickOnce-käyttöönottoteknologiaa koskevat selainvaatimukset. Jotkut selaimet, kuten Google Chrome, edellyttävät laajennuksia.

> [!IMPORTANT]
> Määritä näyttöasettelu kullekin asettelukoolle, joka on määritetty ja jota käytetään myyntipisteessä.

### <a name="full-layout-designer"></a>Täysi asettelun suunnittelutoiminto

Koko asettelun suunnittelutoiminnon avulla käyttäjät voivat vetää POS-käyttöliittymän ohjausobjekteja **tapahtuma**-näyttöön ja määrittää näiden ohjainten asetuksia.

![Myyntipisteen asettelun täysi suunnittelutoiminto (vaaka-tila)](../commerce/media/POS-Full-Layout-Designer-Landscape.png)

- **Tuo asettelu ja Vie asettelu** – voit viedä ja tuoda myyntipisteen näytön asettelun suunnitelmat XML-tiedostoina, jotta voit käyttää niitä uudelleen ja jakaa ympäristöissä. On tärkeää, että tuot asettelusuunnitelmista oikean kokoiset asettelumallit. Muussa tapauksessa käyttöliittymän osat eivät ehkä näy oikein näytössä.
- **Vaaka/pysty** – Mikäli käyttäjät voivat käyttää myyntipisteen laitteen avulla sekä vaaka- että pystymallia, näyttöasettelu on määritettävä kullekin tilalle. Myyntipiste tunnistaa automaattisesti näytön suunnan ja näyttää oikean asettelun.
- **Asetteluruudukko** – Myyntipisteen asettelun suunnittelutoiminto käyttää 4-kuvapisteen ruudukkoa. Käyttöliittymän ohjaus ”Kohdista” auttaa sinua sijoittamaan sisällön oikein ruudukkoon.
- **Suunnittelijazoomaus** – voit suurentaa tai pienentää kohdetta suunnittelutyökalulla tarkastellaksesi paremmin sisältöä POS-näytössä. Tämä ominaisuus on hyödyllinen, kun näytön resoluutio myyntipisteessä eroaa suuresti suunnittelussa käytetyn näytön tarkkuudesta.
- **Näytä tai piilota siirtymispalkki** – koko myyntipisteen asetteluja varten voit valita, näkyykö vasen siirtymispalkki **Tapahtuma**-näytössä. Tämä toiminto on hyödyllinen näytöissä, joissa on pienempi tarkkuus. Määritä näkyvyys hiiren kakkospainikkeella suunnittelutyökalun siirtymispalkissa ja valitse tai poista **Aina näkyvissä** -valintaruutu. Jos siirtymispalkki on piilotettu, myyntipisteen käyttäjät voivat löytää sen vasemman yläkulman valikon avulla.

    ![Näytä / piilota siirtymispalkki](../commerce/media/Navigation-Bar.PNG)

- **Myyntipisteen ohjaimet** – Myyntipisteen asettelun suunnittelutoiminto tukee seuraavia ohjaimia. Voit määrittää useita ohjausobjekteja ja napsauttamalla hiiren oikealla painikkeella ja käyttämällä pikavalikkoa.

    ![Myyntipisteen käyttöliittymän ohjausobjektit](../commerce/media/POS-UI-Controls.png)

    - **Numeronäppäimistö** – Numeronäppäimistö on tärkein syöttötapa myyntipisteen **Tapahtuma**-näytössä. Voit määrittää hallinnan siten, että koko numeronäppäimistö on näkyvissä. Tämä valinta on ihanteellinen kosketusnäyttölaitteille. Vaihtoehtoisesti voit määrittää sen niin, että vain syöttökenttä näytetään. Tällöin fyysistä näppäimistöä käytetään tietojen syöttämiseen. Numeronäppäimistön asetukset ovat käytettävissä vain täydellisessä asettelussa. Tiiviissä asetteluissa koko numeronäppäimistö näkyy aina **Tapahtuma**-näytössä.
    - **Summapaneeli** - Summapaneeliin voidaan määrittää joko yksi tai kaksi saraketta näyttämään arvot kuten rivin määrä, alennussumma, kulut, välisumma ja ALV. Tiivistetyt asettelut tukevat ainoastaan yksittäisiä sarakkeita.
    - **Kuittiruutu** – Kuittiruutu sisältää myyntirivit, maksurivit ja toimitustiedot myyntipisteessä käsitellyille tuotteille ja palveluille. Voit määrittää sarakkeet, leveydet ja sijainnit. Tiivistetyissä asetteluissa voit myös määrittää tiivistettyjä asetteluja, jotka näkyvät päärivin alla olevalla rivillä.
    - **Asiakaskortti** – Asiakaskortti näyttää tämänhetkiseen tapahtumaan liittyvän asiakkaan tietoja. Asiakaskortti voidaan määrittää näyttämään tai piilottamaan lisätiedot.
    - **Välilehtiohjausobjekti** – Välilehtiohjausobjekti voidaan sijoittaa näyttöasetteluun, ja muut ohjausobjektit, kuten numeronäppäimistö, asiakaskortti ja painikeruudukko voidaan sijoittaa välilehden sisään. Välilehtiohjausobjekti on säilö, joka auttaa sinua mahduttamaan enemmän sisältöä näyttöön. Välilehtiohjausobjekti on käytettävissä vain täydellisissä asetteluissa.
    - **Kuva** – Kuva-ohjausobjektia voidaan käyttää näyttämään myymälän logo tai muu brändikuva **Tapahtuma**-näytössä. Kuva-ohjausobjekti on käytettävissä vain täydellisissä asetteluissa.
    - **Suositellut tuotteet** – Jos tämä on määritetty ympäristöön, Suositellut tuotteet -ohjausobjekti näyttää tuote-ehdotuksia koneoppimiseen perustuen.
    - **Mukautettu ohjausobjekti** – Mukautettu ohjausobjekti toimii näytössä paikkamerkkinä varaamassa tilaa mukautetulle sisällölle. Mukautettu ohjausobjekti on käytettävissä vain täydellisissä asetteluissa.

### <a name="compact-layout-designer"></a>Kompakti näytön asettelun suunnittelutoiminto

Kuten täyden asettelun suunnittelutoiminnonkin, kompaktin suunnittelutoiminnon avulla voit määrittää myyntipisteen näyttöasettelun puhelimille ja pienille tableteille. Tässä tapauksessa itse asettelu on korjattu. Voit määrittää useita asetteluohjausobjekteja ja napsauttamalla hiiren oikealla painikkeella ja käyttämällä pikavalikkoa. Et kuitenkaan voi käyttää vedä ja pudota -toimintoja ylimääräistä sisältöä varten.

![Kompakti näytön asettelun suunnittelutoiminto](../commerce/media/Compact-Layout-Designer.png)

### <a name="button-grid-designer"></a>Painikeruudukon suunnittelutoiminto

Painikkeruudukon suunnitteluohjelman avulla voit määrittää painikeruudukoita, joita käytetään myyntipisteen Tervetuloa-näytössä ja **Tapahtuma**-näytön täydellisille sekä kompakteille asetteluille. Samaa painikeruudukkoa voidaan käyttää eri asetteluissa ja asettelutyypeissä. Näytön asettelun suunnittelutoiminto käyttää ClickOnce-käyttöönottoteknologiaa lataamaan, asentamaan ja käynnistämään sovelluksen uusimman version aina, kun se avataan. Muista tarkistaa ClickOnce-käyttöönottoteknologiaa koskevat selainvaatimukset. Jotkut selaimet, kuten Google Chrome, edellyttävät laajennuksia.

![Painikeruudukon suunnittelutoiminto](../commerce/media/Button-Grid-Designer.png)

- **Uusi painike** – Napsauttamalla tätä voit lisätä uuden painikkeen painikeruudukkoon. Oletusarvoisesti uudet painikkeet ovat ruudukon vasemmassa yläkulmassa. Voit järjestää painikkeiden asettelua vetämällä.

    > [!IMPORTANT]
    > Painikeruudukon sisältö saattaa mennä päällekkäin. Järjestellessäsi painikkeita varmista, että ne eivät piilota muita painikkeita.

- **Uusi suunnitelma** – Napsauttamalla tätä voit määrittää automaattisesti painikeruudukon määrittämällä painikkeiden määrän riviä ja sarakkeita kohti.
- **Painikkeen ominaisuudet** – Voit määrittää painikeominaisuudet painamalla hiiren kakkospainiketta ja käyttämällä pikavalikkoa.

    > [!IMPORTANT]
    > Jotkin painikeruudukon asetukset vaikuttavat vain yritysportaalin POS-sovellukseen, eivätkä Modern POS-sovellukseen tai Cloud POS-sovellukseen.

    ![Painikeruudukon painikeominaisuudet](../commerce/media/Button-grid-button-properties.png)

    - **Toiminnot** – käytettäessä myyntipisteen toimintoja valitse listasta toiminto, joka suoritetaan, kun painiketta napsautetaan myyntipisteessä.

        Myyntipisteen tuettujen toimintojen luettelo on kohdassa [Myyntipisteen online- ja offline-toiminnot](pos-operations.md).

    - **Toiminnon parametrit** – Jotkin myyntipisteen toiminnoista käyttävät lisäparametreja, kun ne käynnistetään. Esimerkiksi työvaiheelle Lisää tuote käyttäjät voivat määrittää lisättävän tuotteen.
    - **Painikkeen teksti** – Määritä teksti, joka näkyy myyntipisteen painikkeessa.
    - **Piilota painikkeen teksti** – Tämän valintaruudun avulla voit näyttää tai piilottaa painikkeen tekstin. Painikkeiden teksti piilotetaan usein pienissä painikkeissa, joista näkyy vain kuvake.
    - **Työkaluvihje** – Määritä näytettävä lisäohjeteksti, joka näkyy, kun käyttäjä vie hiiren painikkeen päälle.
    - **Sarakkeiden koko / rivien koko** – Voit määrittää, kuinka pitkä ja leveä painike on.

        ![Myyntipisteen painikkeiden koot riveillä ja sarakkeissa](../commerce/media/POS-Button-Sizes-In-Rows-And-Columns.png)

    - **Mukautettu fontti** – Kun valitset **Ota käyttöön mukautettu fontti myyntipisteelle** -valintaruudun, voit määrittää jonkun muun kuin järjestelmän oletusfontin myyntipisteessä.
    - **Mukautettu teema** – Oletusarvoisesti myyntipisteen painikkeissa käytetään visuaalisen profiilin korostusväriä. Kun valitset **Käytä mukautettua teemaa** -valintaruudun, voit määrittää muita värejä.

        > [!NOTE]
        > Modern POS-sovellus ja Cloud POS käyttävät vain **Taustan väri** ja **fontin väri** -arvoja.

    - **Painikkeen kuva** – painikkeet voivat sisältää kuvia tai kuvakkeita. Valitse käytettävissä olevista kuvista, jotka on määritetty kohdassa **Retail ja Commerce \> Kanavan asetukset \> Myyntipisteen asetukset \> Myyntipisteen \> kuvia**.

![Esimerkki painikeruudukosta myyntipisteessä](../commerce/media/Example-Button-Grid-In-POS.png)

## <a name="additional-resources"></a>Lisäresurssit

[Retail point of salen (POS) asettelun suunnittelutoiminnon asentaminen](install-pos-layout-designer.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]