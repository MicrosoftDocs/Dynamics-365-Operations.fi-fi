---
title: "Vähittäismyynnin oheislaitteet yleiskatsaus"
description: "Tässä ohjeaiheessa kuvataan käsitteitä, jotka liittyvät vähittäismyynnin oheislaitteet. Siinä kuvataan eri tavoin, että voidaan yhdistää myyntipisteeseen (POS) oheislaitteita ja komponentteja, jotka ovat yhteyttä Myyntipiste hallinnosta."
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User, IT Pro
ms.search.scope: Operations, Core
ms.custom: 268444
ms.assetid: 2ea93e43-8019-49a0-a7f8-325565ebc52d
ms.search.region: global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: 79a43c35691f16d773b88faad63c4ab79cb93f1f
ms.openlocfilehash: c6fb3922ba2c4b15f1043d0bcbac40ff2da9a469
ms.lasthandoff: 03/31/2017


---

# <a name="retail-peripherals-overview"></a>Vähittäismyynnin oheislaitteet yleiskatsaus

Tässä ohjeaiheessa kuvataan käsitteitä, jotka liittyvät vähittäismyynnin oheislaitteet. Siinä kuvataan eri tavoin, että voidaan yhdistää myyntipisteeseen (POS) oheislaitteita ja komponentteja, jotka ovat yhteyttä Myyntipiste hallinnosta.

<a name="concepts"></a>Käsitteet
--------

### <a name="pos-registers"></a>Kassakoneet

Siirtyminen: Valitse **jälleenmyynti- ja commerce**&gt;**kanava-asetukset**&gt;**POS-asetukset**&gt;**Rekisteröi**. Myynti (POS) rekisteri on yksikkö, jota käytetään tavaralta ilmentymän Myyntipiste. Nämä ominaisuudet ovat laitteistoprofiilin tai retail-oheislaitteet, jota käytetään rekisterin, myymälä, joka on yhdistetty rekisteriin ja visuaalisia ominaisuuksia käyttäjä, joka kirjautuu rekisterin asetuksia.

### <a name="devices"></a>Laitteet

Siirtyminen: Valitse **jälleenmyynti- ja commerce**&gt;**kanava-asetukset**&gt;**POS-asetukset**&gt;**laitteet**. Laite on yksikkö, joka ilmaisee myyntipisteen kassakoneeseen yhdistämismääritetyn laitteen fyysisen esiintymän. Kun laite on luotu, se on yhdistetty POS rekisterissä. Laiteyksikkö seuraa seuraavia tietoja: myyntipisteen kassakoneen aktivoinnin ajankohta, käytettävän asiakasohjelman tyyppi ja tietyssä laitteessa käyttöönotettu sovelluspaketti. Laitteet voidaan yhdistää seuraavia sovellustyyppejä: Retail POS-Sovelluksen Moderni, Retail Cloud POS, Moderni Vähittäismyyntipisteen – Windows Phone, Retail POS-Sovelluksen Moderni – Android ja Moderni Vähittäismyyntipisteen – iOS.

### <a name="retail-modern-pos"></a>Retail Modern POS

Moderni POS on POS-ohjelma Microsoft Windows. Se voidaan ottaa käyttöön Windows 10-käyttöjärjestelmissä (OSs).

### <a name="cloud-pos"></a>Cloud POS

Cloud POS on selainpohjainen versio Moderni POS-ohjelma, joka voi käyttää web-selaimessa.

### <a name="modern-pos-for-ios"></a>Moderni POS for iOS

Moderni POS for iOS on Moderni POS-ohjelma, joka voidaan ottaa käyttöön iOS laitteiden iOS-pohjainen versio.

### <a name="modern-pos-for-android"></a>Moderni POS for Android

Moderni POS for Android on Moderni POS-ohjelma, joka voidaan ottaa käyttöön Android laitteet Android-pohjainen versio.

### <a name="pos-peripherals"></a>POS-oheislaitteiden

POS-oheislaitteiden ovat laitteita, jotka tukevat Myyntipisteen toimintoja erikseen. Tiettyjä luokkia jaetaan tavallisesti näitä oheislaitteita. Saat lisätietoja näiden luokkien tämän ohjeaiheen kohdassa "Laiteluokat".

### <a name="hardware-station"></a>Laiteasema

Siirtyminen: Valitse **jälleenmyynti- ja commerce**&gt;**kanavia**&gt;**liikkeistä**&gt;**kaikki liikkeistä**. Valitse ensin myymälä ja sitten **Laiteasemat**-pikavälilehti. **Aseman laitteisto** asetus on kanavan tason asetus, jota käytetään määrittämään esiintymät, joissa retail peripheral logiikan otetaan käyttöön. Kanavan tasolla tätä asetusta käytetään määrittämään laitteen aseman ominaisuudet. Sitä käytetään myös luettelo laitteiston asemilla, jotka ovat käytettävissä tietyn myymälän Moderni POS-esiintymän. Aseman laitteisto on sisäänrakennettuna Moderni POS-ohjelma Windowsille. Laitteiston asema voidaan myös ottaa käyttöön erikseen erillisenä ohjelmana Microsoft Internet Information Services (IIS). Tässä tapauksessa se voi käyttää verkon kautta.

### <a name="hardware-profile"></a>Laiteprofiili

Siirtyminen: Valitse **jälleenmyynti- ja commerce**&gt;**kanava-asetukset**&gt;**POS-asetukset**&gt;**POS-profiilit**&gt;**laitteistoprofiilien**. Laitteistoprofiili on luettelo laitteista, jotka on määritetty POS-rekisteriin tai laitteiston station. Laitteistoprofiili voidaan yhdistää suoraan POS-rekisteriin tai laitteiston station.

## <a name="devices-classes"></a>Luokat: laitteet
POS-oheislaitteiden yleensä jaetaan luokkiin. Tässä osassa kuvataan ja antaa yhteenvedon, joka tukee Nykyaikainen POS laitteita.

### <a name="printer"></a>Tulostin

Tulostimet ovat perinteinen POS vastaanoton Tulostimet ja koko sivun tulostimet. Tulostin tukee objektien linkittämistä ja upottamista käyttöliittymien Retail POS (OPOS) ja Microsoft Windows kautta. Enintään kaksi tulostinta voi käyttää samaan aikaan. Tämä ominaisuus tukee tilanteissa, joissa cash-and-carry asiakkaan kuitit tulostetaan vastaanoton tulostimet taas asiakastilausten suorittaa lisätietoja, jotka tulostuvat koko sivun paperille. Kuitti tulostimet on kytketty suoraan tietokoneen kautta USB, kytkettynä verkkoon kautta Ethernet tai yhdistetty Bluetoothilla.

### <a name="scanner"></a>Skanneri

Enintään kaksi viivakoodi skannerit voidaan käyttää samaan aikaan. Tämä ominaisuus tukee, joka on enemmän mobiili skanneri on pakollinen skannausasetukset suuri tai raskaita kohteita olisi kiinteä upotettu skanneri käytetään useimmissa standardikokoiset nimikkeiden nopeuttamaan poistuminen kertaa. Skannerit, tukee OPOS, Universal Windows Platform (UWP) tai näppäimistön kiila liittymiä. Liitä skanneri tietokoneeseen voi käyttää USB- tai Bluetooth.

### <a name="msr"></a>Magneettinauhan lukulaite

Yksi USB-Magneettinauhan lukulaite (MSR) voidaan määrittää käyttämällä OPOS-ohjaimet. Jos haluat käyttää erillisiä MSR sähköisen varojen siirron (EFT) maksutapahtumat, MSR hallitsee maksu-liitin. Kanta Asiakastapahtuma, työntekijöiden sisään ja lahja kortin merkintä maksu-liitin riippumatta voidaan käyttää itsenäisenä MSRs.

### <a name="cash-drawer"></a>Kassa

Kaksi cash vetolaatikot voidaan tukea per laitteistoprofiilissa. Tämä ominaisuus mahdollistaa kaksi aktiivista vuorot kassapääte saatavissa samaan aikaan. Jaettu VAIHTO tai kassa, jonka avulla kannettavien laitteiden POS samaan aikaan vain yksi kassa voi laitteistoprofiilissa. Cash vetolaatikot olla kytketty suoraan tietokoneen kautta USB, yhteydessä verkkoon tai yhdistetty vastaanotto tulostimen RJ12-liittymän kautta. Joissakin tapauksissa rahaa vetolaatikot voidaan yhdistää myös Bluetoothilla.

### <a name="line-display"></a>Rivinäyttö

Näyttää rivin käytetään osoittamaan tuotteiden, tapahtumien saldot ja muita hyödyllisiä tietoja asiakkaalle tapahtuman aikana. Yhden rivin näyttö voidaan kytkeä tietokone kautta USB OPOS-ohjainten avulla.

### <a name="signature-capture"></a>Allekirjoituksen tarkistus

Allekirjoituksen capture laitteet voidaan kytkeä suoraan tietokoneen kautta USB OPOS-ohjainten avulla. Allekirjoituksen tarkistus on määritetty, kun asiakas pyytää kirjautua laitteeseen. Allekirjoitus on käytettävissä, kun se näkyy hyväksyminen kassalle.

### <a name="scale"></a>Mittakaava

Skaalaa voi kytkeä tietokoneen kautta USP OPOS-ohjainten avulla. Kun tapahtuma on lisätty tuote, joka on merkitty "Weighed" tuotteena, Myyntipiste lukee paino asteikko, Lisää tuotteen tapahtumaan ja käyttää määrää, joka oli asteikko.

### <a name="pin-pad"></a>PIN-näppäimistö

Henkilökohtainen tunnus (PIN) numeropainikkeisiin tukee OPOS kautta, mutta ne on hoidettava maksu Connectorin kautta.

### <a name="secondary-display"></a>Toissijainen näyttö

Toissijainen näyttö on määritetty, kun Windows näytön numero 2 käytetään Näytä perustietoja. Toissijainen näyttö tarkoituksena on tukea riippumattoman ohjelmiston toimittaja (ISV) tunniste koska laatikosta, toissijainen näyttö ei ole määritettävissä ja näyttää rajoitetun sisällön.

### <a name="payment-device"></a>Maksulaite

Maksu laitteen tuki toteutetaan maksun Connectorin kautta. Laitteiden maksun voi suorittaa yhden tai useita toimintoja, jotka tarjoavat muita laiteluokat. Esimerkiksi maksu-laite voi toimia magneettinauhan Lukulaitteen/kortin lukulaite, rivin näyttö, allekirjoitus sieppauslaite tai PIN-näppäimistö. Tuki laitteet maksu toteutetaan erikseen erillisenä laitteena tuki, jota annetaan muita laitteita, jotka sisältyvät laitteistoprofiilin.

## <a name="supported-interfaces"></a>Tuettuja liittymiä
### <a name="opos"></a>OPOS

Auttavat takaamaan, että laitteiden suurin alue voidaan käyttää Microsoft Dynamics-365 kanssa Operations - Retail, OLE POS alan standardi, on ensisijainen retail oheislaitteen ympäristö, jota tueta Microsoft Dynamics-365 työvaiheiden - Retail. POS-standardin OLE tuotettiin mukaan kansallisen Retail Federation (NRF), jossa määrätään yleisesti protokollia retail oheislaitteiden. OPOS on laajalti hyväksytyn täytäntöönpano OLE standardin POS. Se kehitettiin mid-1990-luvun alussa ja on päivitetty sen jälkeen useita kertoja. OPOS sisältää laitteen ohjaimen arkkitehtuuri, joka mahdollistaa helpon integraation POS laitteita Windows-pohjainen POS-järjestelmien kanssa. OPOS ohjaa yhteensopivien laitteiden ja POS ohjelmisto välisen tietoliikenteen kahva. OPOS-ohjausobjektin koostuu kahdesta osasta:

-   **Objektin ohjausobjektin** – ohjausobjekti (esimerkiksi rivi näyttää) laiteluokan tarjoaa ohjelman käyttöliittymä. Monroe konsultointipalvelut ([www.monroecs.com](http://www.monroecs.com/)) on standardoitu joukko OPOS komponentin objektit, joita kutsutaan yhteisten valvonta-objektien (CCOs). Voit testata Microsoft Dynamics-365 työvaiheiden - Retail POS-osa käytetään CCOs. Tämän vuoksi testaus auttaa taata, että jos Microsoft Dynamics-365 työvaiheiden - Retail tukee OPOS-laitteen erilaisia kautta laiteluokan voidaan pitää hyväksyttävänä, edellyttäen, että valmistaja antaa huolto-objektin, joka on luotu OPOS. Sinun ei tarvitse erikseen testata jokaisen laitteen tyyppiä.
-   **Huoltokohteen** – palvelu-objekti sisältää ohjausobjekti (CCO) ja laitteen välinen tietoliikenne. Laitteen huolto-objektin toimitetaan yleensä laitteen valmistaja. Kuitenkin joissakin tapauksissa joudut ehkä huolto-objektin lataaminen valmistajan WWW-sivustosta. Esimerkiksi uudempia huoltokohteen voi olla käytettävissä. Valmistajan WWW-sivuston osoite, Katso laitteiston ohjeista.

[![Määrittää objektin ja huoltokohteen](./media/retail_peripherals_overview01.png)](./media/retail_peripherals_overview01.png) tukea OLE täytäntöönpanon OPOS POS auttaa taata, jos laitteen valmistajat ja POS julkaisijat toteuttaa standardin oikein, POS systems ja tuettujen laitteiden voitte työskennellä yhdessä, vaikka niitä ei ole aiemmin testattu yhdessä. **Huomautus:** OPOS-tuki ei takaa kaikkien laitteiden, joilla OPOS-ohjaimet tukevat. Microsoft Dynamicsin 365 - toimintoja varten Retail ensin tuettava kyseisen laitteen tyyppi tai luokka OPOS kautta. Lisäksi huoltokohteet ehkä ole aina ajan tasalla CCOs uusimman version kanssa. Sinun tulisi olla tietoinen, että yleisesti ottaen huoltokohteet laatu vaihtelee.

### <a name="windows"></a>Windows

Kuitin tulostus myyntipisteessä on optimoitu OPOS. OPOS yleensä paljon nopeammin kuin tulostaminen Windowsin avulla. Siksi on järkevää käyttää OPOS-erityisesti vähittäiskaupan ympäristöissä, jossa 40 saraketta kuitit tulostetaan ja Siirtotapahtuma-ajat on oltava nopeaa. Useimmat laitteet käyttävät OPOS-ohjausobjekteja. Kuitenkin jotkin OPOS-vastaanoton tulostimet tukevat myös Windows-ohjaimia. Windows-ohjaimen avulla voit käyttää uusimman fontit ja yksi verkkotulostin on useita rekistereitä. Ovat kuitenkin haitoista käyttäen Windows-ohjaimia. Seuraavassa on esimerkkejä näistä haitoista:

-   Kun käytetään Windows-ohjaimia, kuvia tuotetaan ennen tulostamista. Tämän vuoksi tulostus yleensä hitaammin kuin sen tulostimella, joka käyttää OPOS-komponentteja.
-   ("Ketjutettu") tulostimen kautta kytketyt laitteet eivät ehkä toimi oikein kun käytetään Windows-ohjaimet. Kassan ei ehkä aukea, tai slip-tulostin ei ehkä sanan haluamallasi tavalla.
-   OPOS tukee myös laajempi joukko muuttujia, jotka liittyvät vähittäismyynnin vastaanoton tulostimet, kuten paperin leikkaaminen tai pakkausluettelon tulostamiseen.

OPOS-ohjausobjektit ovat käytettävissä Windows-tulostinta, jota käytät, jos tulostimen pitäisi toimia oikein Microsoft Dynamics-365 työvaiheiden - tuotepaketti.

### <a name="universal-windows-platform"></a>Universal Windows-ympäristössä

UWP, oheislaitteiden vähittäiskaupan osalta liittyy Windowsin Plug and Play-laitteiden tuki. Plug and Play-laite on yhdistetty Windows-käyttöjärjestelmän versio, joka tukee kyseistä laitetta, kun ei kuljettaja tarvitaan laite, jota käytetään tarkoitetulla tavalla. Esimerkiksi jos Windows tunnistaa laitteen Bluetooth kaiutin, Käyttöjärjestelmä tietää että laite on **kaiuttimen** luokan tyyppi. Tämän vuoksi ja se käsittelee kyseistä laitetta kaiutin. Ei ole muita asetuksia ei tarvita. Monet USB-laitteet on kytketty verkkovirtaan, POS laitteita ja Windows tunnistaa ne HID-laitteet (HIDs). Kuitenkin se ei ehkä pysty määrittämään ominaisuuksista, joita laite antaa, koska laite ei määritä luokan tai laitteen tyypin. Windows 10-laiteluokat viivakoodi Skannerit ja MSRs on lisätty. Siis Jos laite vakuuttaa itse Windows 10 jonkin näistä luokkien laitteena, Windows kuuntelee tapahtumia laitteesta sopivina ajankohtina. Moderni POS tukee UWP MSRs ja skannerit. Siksi, kun se on valmis näiden laitteiden toimia ja on liitetty laite, joka kuuluu johonkin näistä luokista, laitetta voidaan käyttää. Esimerkiksi jos UWP Viivakoodin lukijalaitetta Windows 10-tietokone on kytketty ja viivakoodin sisään on määritetty käyttämään nykyaikaisia POS, viivakoodi skanneri aktivoituvat sisään näytössä. Ei ole muita asetuksia ei tarvita. Muita luokkia kohdan service UWP laitteet lisätään Windows. Nämä luokat sisältävät käteisen vetolaatikot ja vastaanoton tulostimet luokat. Uusi Nykyaikainen POS näiden laiteluokkien tuki odottaa.

### <a name="keyboard-wedge"></a>Näppäimistön kiila

Näppäimistön kiila laitteiden lähettää tietoja tietokoneeseen kuin jos tiedot on kirjoitettu näppäimistön. Tämän vuoksi oletusarvon mukaan kenttä, joka on käytettävissä myyntipisteessä saavat tietoja, jotka on skannattu tai luettu. Joissakin tapauksissa tämä saattaa aiheuttaa väärän tyyppisen skannattavan väärään kenttään tietoja. Esimerkiksi viivakoodi voidaan tarkistaa kenttään, joka on tarkoitettu luottokorttitietojen syöttöä. Monissa tapauksissa on logiikkaa, joka määrittää, onko tiedot, jotka on luettu tai skannattu viivakoodin tai kortin lukemista myyntipisteessä. Tämän vuoksi ne käsitellään oikein. Kun laitteet on määritetty OPOS näppäimistön kiila laitteiden sijasta, on kuitenkin tarkemmin miten kyseisten laitteiden tiedot voidaan kuluttaa, koska yksi on "tiedetään", joka on peräisin tietoja laitteen. Viivakoodin skannerin tiedot tunnistetaan automaattisesti viivakoodi, ja liitetyn tietueen tietokannasta löytyy helpommin ja nopeammin kuin jos haun merkkijono yleinen käytettiin, kuten näppäimistön kiila laitteiden tapauksessa.

### <a name="native-printer"></a>Oma tulostin

Alkuperäinen (tai laitteistoprofiilin nimi on "Laite" tyyppi) tulostimet voidaan määrittää tuomaan näyttöön kehotteen valita tulostimen, joka on määritetty tietokoneen käyttäjää. Kun kirjoitin, **laitteen** tyyppi on määritetty, jos Moderni POS kohtaa print-komennon, käyttäjää pyydetään valitsemaan luettelosta tulostin. Tämä eroaa toimintaa Windows-ohjaimet, koska **Windows** tulostimen tyyppi laitteistoprofiili ei Näytä tulostimien luettelo. Sen sijaan se edellyttää, että nimetyt tulostimen toimitetaan **laitteen nimi** kenttä.

### <a name="windows"></a>Windows

**Windows** vain tulostimia käytetään laitteen tyyppiä. Kun Windows-tulostin on määritetty laitteistoprofiili, tulostimen nimi on annettava. Moderni POS kohtaa Tulosta tapahtumat, jos Windows-tulostin on määritetty, kun tapahtuma välitetään määritetty Windows-tulostin. Käyttäjää ei kehoteta valitsemaan tulostimen.

### <a name="network"></a>Verkko

Verkon käytettävissä rahaa vetolaatikot, vastaanoton Tulostimet ja päätteiden maksu voidaan käyttää verkossa, suoraan Interprocess viestintä (IPC) laitteisto-asema, joka on rakennettu Moderni POS for Windows-sovelluksen tai IIS: N laitteiston asema Moderni POS muiden asiakkaiden kautta.

## <a name="hardware-station-deployment-options"></a>Aseman käyttöönoton lisälaitteet
### <a name="ipc-built-in"></a>IPC (sisäinen)

Interprocess viestintä (IPC) laitteisto asema on rakennettu Moderni POS for Windows-sovellus. IPC-laitteiston station käyttämään laiteprofiilin rekisteriin, jota käyttää nykyaikaisia POS for Windows-sovellus. Luo sitten laitteiston aseman **erityisvarastopaikka** jossa rekisteriä käytetään myymälän tyyppi. Kun käynnistät Moderni POS, IPC laitteiston asema on aktiivinen ja POS-oheislaitteet, jotka on määritetty on valmis käytettäväksi. Tilapäisesti Paikalliset laitteet eivät vaadi jostain syystä, jos **hallita laitteiston asemilla** aseman laitteisto-ominaisuudet käytöstä-toiminto. Moderni POS käyttää myös IPC laitteisto-aseman yhteydessä verkkoon liitettyihin oheislaitteisiin.

### <a name="iis"></a>IIS: N

Voit käyttää IIS: N tai itsenäinen versio aseman laitteisto kahdella tavalla. Kuvaajan "IIS" tarkoittaa sitä, että POS-sovellus muodostaa yhteyden laitteen aseman kautta Microsoft Internet Information Services. POS-sovellus muodostaa yhteyden IIS laitteiston aseman kautta web-palvelut, jotka suoritetaan tietokoneessa, jossa laitteet on liitetty. Kun IIS on käytössä, voidaan käyttää retail-oheislaitteet, jotka on yhdistetty laitteisto-asema, joka on samassa verkossa kuin IIS-laitteiston station POS rekisterien mukaan. Vain Moderni POS for Windows sisältää sisäisen tuen retail oheislaitteet, koska kaikki nykyaikaiset POS-sovellusten on käytettävä IIS-laitteiston station, jotka on määritetty laitteistoprofiili POS-oheislaitteiden kanssa. Siksi jokaisen esiintymän IIS-laitteiston station edellyttää web-palvelua käyttävän tietokoneen ja sovelluksen, joka kommunikoi laitteen kanssa. Kaikki ei - Windows Moderni POS sovellukset IIS: N laitteisto-asema tarvitaan.

#### <a name="dedicated"></a>Varattu

Moderni POS-sovellus käyttää laitteen asemilla olevien **erityisvarastopaikka** tunnistaa, että tietokone, jossa sovellus käytetään suoraan liittyvät oheislaitteet tyyppi. Kuitenkin **erityisvarastopaikka** tyyppiä voidaan käyttää myös IIS-laitteiston asemilla. Perinteisten, kiinteiden POS skenaariossa, joka POS-sovellus käyttää Cloud POS **erityisvarastopaikka** asema laitetyyppi käytetään IIS: N laitteiston asemilla, jotka on otettu samassa tietokoneessa, jonka käyttöjärjestelmä on pilvi POS. Vähittäismyynnin oheislaitteet näkökulmasta kiinteä IIS-laitteiston station on paremmin retail POS perinteisten, kiinteiden tilanteissa peripheral tuki. Kiinteä laitteisto-asemat tukevat kaikki lisälaitteet, joita tuetaan laitteistoprofiilissa.

#### <a name="shared"></a>Yhteiset ominaisuudet

Jaettujen asemien tarkoituksena on useita päivän kurssin kautta POS laitteita käytetään laitteiston. Jaettujen asemien tuki vain käteinen vetolaatikot, vastaanoton Tulostimet ja päätteiden maksu on optimoitu laite. Et voi muodostaa suoraan erillinen viivakoodi skannerit, MSRs, rivi näyttää, asteikkoja tai muita laitteita. Muussa tapauksessa ristiriitoja syntyy, kun yrittää väittää niiden oheislaitteiden samaan aikaan useita POS laitteita. Tässä on, miten hallitaan ristiriitoja tuettujen laitteiden:

-   **Kassan** – tapahtuma, joka lähetetään laitteen kautta avataan kassan. Ainoa ongelma, joka voi ilmetä, kun kassa kutsutaan ilmenee, jos kassan on jo avoinna. Jaettu laitteiston asemilla, jos kassan on asetettava **jaettujen** laitteistoprofiilissa. Tämä asetus estää Myyntipiste tarkistetaan, onko kassan on jo avoinna, kun se lähettää Avaa-komentoja.
-   **Kuittitulostimen** – Jos kaksi Kuitin tulostaminen komennot lähetetään samaan aikaan, jokin komento aseman laitteisto voidaan menettää, jos laite. Joissakin laitteissa on sisäinen muisti tai jakavan, voit estää tämän ongelman. Jos Tulosta-komento ei ole onnistunut, kassa saa seuraavankaltaisen virhesanoman ja yrittää uudelleen POS print-komennon.
-   **Maksun pääte** – Jos kassa yrittää tarjouskilpailun tapahtuman maksun pääte, joka on jo käytössä, viesti ilmoittaa kassa pääte on käytössä ja kysyy kassanhoitajalta, yritä myöhemmin uudelleen. Kassat näkevät yleensä päätteen on jo käytössä ja odottaa, kunnes muut tapahtuma on valmis, ennen kuin he yrittävät uudelleen tarjouksen.

Vahvistus on suunniteltu tulevan julkaisun, voit tunnistaa, onko ei-tuetut laitteet on määritetty laitteistoprofiilin, joka on yhdistetty jaettuun laitteiston station. Jos laitteita ei tueta havaitaan, käyttäjä saa viestin, jossa ilmoitetaan, että laitteet eivät tue jaettuja laitteita asemien. Jaettuja laitteita asemien osalta **Valitse tarjouskilpailun yhteydessä** asetus **Kyllä** rekisteri-tasolla. POS-käyttäjää pyydetään sitten valitsemaan aseman laitteisto, kun tarjous on valittu tapahtuman myyntipisteessä. Kun vain silloin, kun tarjous on valittu laitteiston station, laitteiston aseman valinta lisätään suoraan POS työnkulun mobiili-skenaarioissa. Rivin näyttö terminal maksu ei ole lisähyötyä, muodossa käyttää jaettu skenaarioita. Jos terminal maksu käytetään rivin näyttö, muiden käyttäjien saattaa estää käyttämästä päätteessä, kunnes tapahtuma on valmis. Mobiili tilanteissa rivit lisännyt tapahtumaan pidemmän päälle. Tämän vuoksi **Valitse tarjouskilpailun yhteydessä** laitteen optimaalisen saatavuuden takaamiseksi tarvitaan vaihtoehto.

### <a name="network-peripherals"></a>Verkko-oheislaitteet

Verkon laitteiden laitteistoprofiilin nimeäminen antaa rahaa vetolaatikot vastaanoton Tulostimet ja päätteiden maksu yhdistetään verkkoyhteyden kautta.

#### <a name="modern-pos-for-windows"></a>Moderni POS for Windows

Voit määrittää IP-osoitteet verkon oheislaitteet kahdessa paikassa. Jos Moderni POS Windows client käyttää yhtenäisiä verkon oheislaitteet, tulisi asettaa kyseisten laitteiden IP-osoitteita käyttämällä **IP-määrityksen** rekisteröi itsensä toimintoruudun vaihtoehto. Verkon laitteissa, jotka jaetaan kesken kassakoneet, laitteistoprofiili, joka on sille verkkolaitteet voidaan yhdistää suoraan laitteiston jaetun aseman. Voit määrittää IP-osoitteet, valitse aseman laitteisto **liikkeistä** sivulle ja käytä sitten **IP-määritykset** -vaihtoehdon **laitteiston asemilla** määrittää verkkolaitteet, jotka on määritetty aseman laitteisto-osan. Laitteisto-asemien, joissa on vain verkkolaitteet sinun ei tarvitse asentaa laitteisto-asema itse. Tässä tapauksessa laitteisto asema edellyttää vain ryhmitellään käsitteellisesti osoitteelliset verkon laitteiden vähittäiskaupan myymälän niiden sijainnin mukaan.

#### <a name="cloud-pos-modern-pos-for-ios-and-modern-pos-for-android"></a>Cloud POS, Moderni POS for iOS ja Moderni POS for Android

Logiikka, joka fyysisesti yhteydessä ja verkon osoitteelliset oheislaitteet asemat sisältyy laitteisto-asema. Siis kaikki POS asiakkaiden lukuun ottamatta Moderni POS for Windows, IIS laitteiston station on oltava käyttöön ja aktiivinen POS oheislaitteet, niiden oheislaitteet ovat fyysisesti kytketty laite station tai osoitettu verkon kautta yhteydessä käyttöön.

## <a name="setup-and-configuration"></a>Asennus ja määritys
### <a name="hardware-station-installation"></a>Laiteasennus station

Lisätietoja [Retail-laitteiston määritykset ja asennus](retail-hardware-station-configuration-installation.md).

### <a name="modern-pos-for-windows-setup-and-configuration"></a>Moderni POS for Windows-asennus ja määritys

Lisätietoja [Retail POS-Sovelluksen Moderni kokoonpano ja asennus](retail-modern-pos-device-activation.md).

### <a name="opos-device-setup-and-configuration"></a>OPOS-laitteen asennus ja määritys

Saat lisätietoja OPOS-osat "Tuettuja liittymiä" tämän asiakirjan kohdassa. OPOS-ohjaimet toimitetaan yleensä laitteen valmistaja. OPOS-laiteohjain asennetaan, se Lisää avain Windows-rekisterin jossakin seuraavista paikoista:

-   **32-bittinen järjestelmä:** HKEY\_PAIKALLISTEN\_MACHINESOFTWAREOLEforRetailServiceOPOS
-   **64-bittinen järjestelmä:** HKEY\_PAIKALLISTEN\_MACHINESOFTWAREWOW6432NodeOLEforRetailServiceOPOS

ServiceOPOS rekisterin sijaintia määritettyjä laitteita on järjestetty OPOS-laitteen luokan mukaan. Tallennetaan useita laiteohjaimia.

## <a name="supported-scenarios-by-hardware-station-type"></a>Tuetut tilanteita station laitetyypin mukaan
### <a name="client-support--ipc-hardware-station-vs-iis-hardware-station"></a>Asiakkaan tuki – IPC laitteiston station vs. IIS laitteiston station

Seuraavassa taulukossa on esitetty topologioissa ja käyttöönottoskenaarioissa, joita tuetaan.

| Asiakas      | IPC-laitteiston station | IIS: N laitteiston station |
|-------------|----------------------|----------------------|
| Windows-app | Kyllä                  | Kyllä                  |
| Cloud POS   | Nro                   | Kyllä                  |
| Android     | Nro                   | Kyllä                  |
| iOS         | Nro                   | Kyllä                  |

### <a name="network-peripherals"></a>Verkko-oheislaitteet

Verkon oheislaitteet voidaan tukea suoraan laitteisto-asema, joka on rakennettu Moderni POS for Windows-sovelluksen kautta. Muita asiakkaita varten on otettava käyttöön IIS laitteiston station.

| Asiakas      | IPC-laitteiston station | IIS: N laitteiston station |
|-------------|----------------------|----------------------|
| Windows-app | Kyllä                  | Kyllä                  |
| Cloud POS   | Nro                   | Kyllä                  |
| Android     | Nro                   | Kyllä                  |
| iOS         | Nro                   | Kyllä                  |

## <a name="supported-device-types-by-hardware-station-type"></a>Tuetut tyypit laitteen laitteisto-aseman tyypin mukaan
### <a name="modern-pos-for-windows-with-an-ipc-built-in-hardware-station"></a>Moderni POS for Windows (sisäinen) IPC laitteisto aseman kanssa

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Tuetun laitteen luokka</th>
<th>Tuettuja liittymiä</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Tulostin</td>
<td><ul>
<li>OPOS</li>
<li>Windows-ohjain</li>
<li>Laite</li>
<li>Verkko</li>
</ul></td>
</tr>
<tr class="even">
<td>Tulostin 2</td>
<td><ul>
<li>OPOS</li>
<li>Windows-ohjain</li>
<li>Laite</li>
<li>Verkko</li>
</ul></td>
</tr>
<tr class="odd">
<td>Rivinäyttö</td>
<td>OPOS</td>
</tr>
<tr class="even">
<td>Kaksi näyttöä</td>
<td>Windows-ohjain</td>
</tr>
<tr class="odd">
<td>Magneettinauhan lukulaite</td>
<td><ul>
<li>OPOS</li>
<li>UWP (ei asennus tarvitaan.)</li>
<li>Näppäimistön kiila (ei asennus tarvitaan.)</li>
</ul></td>
</tr>
<tr class="even">
<td>Asettaja</td>
<td><ul>
<li>OPOS</li>
<li>Verkon <strong>Huomautus:</strong> Jos voidaan määrittää vain yksi laatikko <strong>käyttää jaettua VAIHTO</strong> kassan määritetään.</li>
</ul></td>
</tr>
<tr class="odd">
<td>Kassa 2</td>
<td><ul>
<li>OPOS</li>
<li>Verkon <strong>Huomautus:</strong> Jos voidaan määrittää vain yksi laatikko <strong>käyttää jaettua VAIHTO</strong> kassan määritetään.</li>
</ul></td>
</tr>
<tr class="even">
<td>Skanneri</td>
<td><ul>
<li>OPOS</li>
<li>UWP (ei asennus tarvitaan.)</li>
<li>Näppäimistön kiila (ei asennus tarvitaan.)</li>
</ul></td>
</tr>
<tr class="odd">
<td>Skanneri 2</td>
<td><ul>
<li>OPOS</li>
<li>UWP (ei asennus tarvitaan.)</li>
<li>Näppäimistön kiila (ei asennus tarvitaan.)</li>
</ul></td>
</tr>
<tr class="even">
<td>Mittakaava</td>
<td>OPOS</td>
</tr>
<tr class="odd">
<td>PIN-näppäimistö</td>
<td>OPOS (tuki annetaan mukauttaminen maksun liittimen kautta.)</td>
</tr>
<tr class="even">
<td>Allekirjoituksen tarkistus</td>
<td>OPOS</td>
</tr>
<tr class="odd">
<td>Maksupääte</td>
<td><ul>
<li>Mukautetun laitteen tuki</li>
<li>Verkko (Katso lisätietoja maksun connector-ohjeista.)</li>
</ul></td>
</tr>
</tbody>
</table>

### <a name="all-modern-pos-clients-that-have-a-dedicated-iis-hardware-station"></a>Kaikki nykyaikaiset POS-asiakkailla on kiinteä IIS-laitteiston station

**Huomautus:** IIS-laitteiston station "palvelee," Kun on suhde POS-asiakas- ja laitteisto-asema.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Tuetun laitteen luokka</th>
<th>Tuettuja liittymiä</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Tulostin</td>
<td><ul>
<li>OPOS</li>
<li>Windows-ohjain <strong>Huomautus:</strong> Windows-verkon tulostimet, laitteiston aseman käyttäjällä on oltava käyttöoikeus tulostimen.</li>
<li>Verkko</li>
</ul></td>
</tr>
<tr class="even">
<td>Tulostin 2</td>
<td><ul>
<li>OPOS</li>
<li>Windows-ohjain</li>
<li>Verkko</li>
</ul></td>
</tr>
<tr class="odd">
<td>Rivinäyttö</td>
<td>OPOS</td>
</tr>
<tr class="even">
<td>Magneettinauhan lukulaite</td>
<td>OPOS</td>
</tr>
<tr class="odd">
<td>Asettaja</td>
<td><ul>
<li>OPOS</li>
<li>Verkon <strong>Huomautus:</strong> Jos voidaan määrittää vain yksi laatikko laitteistoprofiilin kohti <strong>käyttää jaettua VAIHTO</strong> kassan määritetään.</li>
</ul></td>
</tr>
<tr class="even">
<td>Kassa 2</td>
<td><ul>
<li>OPOS</li>
<li>Verkko</li>
</ul></td>
</tr>
<tr class="odd">
<td>Skanneri</td>
<td>OPOS</td>
</tr>
<tr class="even">
<td>Skanneri 2</td>
<td>OPOS</td>
</tr>
<tr class="odd">
<td>Mittakaava</td>
<td>OPOS</td>
</tr>
<tr class="even">
<td>PIN-näppäimistö</td>
<td>OPOS (tuki annetaan mukauttaminen maksun liittimen kautta.)</td>
</tr>
<tr class="odd">
<td>SIG. kaappaa</td>
<td>OPOS</td>
</tr>
<tr class="even">
<td>Maksupääte</td>
<td><ul>
<li>Mukautetun laitteen tuki</li>
<li>Verkko (Katso lisätietoja maksun connector-ohjeista.)</li>
</ul></td>
</tr>
</tbody>
</table>

### <a name="all-modern-pos-clients-that-have-a-shared-iis-hardware-station"></a>Kaikki nykyaikaiset POS-asiakkailla on jaettu IIS-laitteiston station

**Huomautus:** kun IIS-laitteiston station "jaetaan," useita laitteita käyttää laitteisto-aseman samaan aikaan. Tässä tilanteessa sinun tulee käyttää vain laitteita, jotka on lueteltu seuraavassa taulukossa. Jos yrität jakaa laitteita, joita ei ole lueteltu tässä, viivakoodi Skannerit ja MSRs, kuten virheitä ilmenee, kun yrität väittää samaa oheislaite useita laitteita. Jatkossa kokoonpanossa nimenomaisesti estetään.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Tuetun laitteen luokka</th>
<th>Tuettuja liittymiä</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Tulostin</td>
<td><ul>
<li>OPOS</li>
<li>Windows-ohjain <strong>Huomautus:</strong> Windows-verkon tulostimet, laitteiston aseman käyttäjällä on oltava käyttöoikeus tulostimen.</li>
<li>Verkko</li>
</ul></td>
</tr>
<tr class="even">
<td>Tulostin 2</td>
<td><ul>
<li>OPOS</li>
<li>Windows-ohjain</li>
<li>Verkko</li>
</ul></td>
</tr>
<tr class="odd">
<td>Asettaja</td>
<td><ul>
<li>OPOS</li>
<li>Verkon <strong>Huomautus:</strong> Jos voidaan määrittää vain yksi laatikko laitteistoprofiilin kohti <strong>käyttää jaettua VAIHTO</strong> kassan määritetään.</li>
</ul></td>
</tr>
<tr class="even">
<td>Kassa 2</td>
<td><ul>
<li>OPOS</li>
<li>Verkko</li>
</ul></td>
</tr>
<tr class="odd">
<td>Maksupääte</td>
<td><ul>
<li>Mukautetun laitteen tuki</li>
<li>Verkko (Katso lisätietoja maksun connector-ohjeista.)</li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="configuration-for-supported-scenarios"></a>Tuetut tilanteet kokoonpano
Saat lisätietoja siitä, miten luoda laitteistoprofiileja [Määritä ja Ylläpidä kanavan asiakkaiden, rekisterit ja laitteiston asemilla kuten](define-maintain-channel-clients-registers-hw-stations.md). **Huomautus:** For Microsoft Dynamics 365 version toiminnot 1611, laitteistoprofiili asema ei ole enää käytössä. Määritteet, jotka olet aiemmin määrittänyt aseman laitteistoprofiilissa ovat nyt itse laitteisto-asema.

### <a name="modern-pos-for-windows-with-an-ipc-built-in-hardware-station"></a>Moderni POS for Windows (sisäinen) IPC laitteisto aseman kanssa

Tämä kokoonpano on POS-Sovelluksen kassojen perinteisten, kiinteiden yleisin kokoonpano. Tämän skenaarion laitteisto profiilitiedot on yhdistetty suoraan itse rekisteriä. EFT-päätteen numero on määritettävä myös itse kassalla. Voit määrittää tässä kokoonpanossa, toimi seuraavasti.

1.  Voit luoda laitteistoprofiilin, jossa määritetään tarvittavat lisälaitteet.
2.  Yhdistä laitteistoprofiili POS-rekisteriin.
3.  Luo laitteisto-aseman **erityisvarastopaikka** Vähittäismyymälä, jossa käytetään POS-rekisteri tyyppi. Kuvaus on valinnainen. **Huomautus:** sinun ei tarvitse määrittää muita ominaisuuksia laitteisto-asema. Kaikki muut tarvittavat tiedot, kuten laitteistoprofiilin, haetaan rekisteristä itse.
4.  Valitse **jälleenmyynti- ja commerce**&gt;**vähittäismyynnin IT**&gt;**aikataulun jakelu**.
5.  Valitse **1090** jakelu aikataulun synkronointi säilöön uuden laitteistoprofiilin. Valitse **suorittaa nyt** Myyntipiste tehtyjen muutosten synkronointi.
6.  Valitse **1040** jakelu aikataulun synkronointi aseman säilöön uusi laitteisto. Valitse **suorittaa nyt** Myyntipiste tehtyjen muutosten synkronointi.
7.  Asenna ja aktivoi nykyaikaiset POS for Windows.
8.  Moderni POS for Windowsin käynnistyksen ja käytön yhteydessä oheislaitteita.

### <a name="all-modern-pos-clients-that-have-a-dedicated-iis-hardware-station"></a>Kaikki nykyaikaiset POS-asiakkailla on kiinteä IIS-laitteiston station

Tässä kokoonpanossa kaikki nykyaikaiset POS-asiakkailla on laitteisto-asema, jota käytetään yksinomaan yhden POS voidaan rekisteröidä. Voit määrittää tässä kokoonpanossa, toimi seuraavasti.

1.  Voit luoda laitteistoprofiilin, jossa määritetään tarvittavat lisälaitteet.
2.  Luo laitteisto-aseman **erityisvarastopaikka** Vähittäismyymälä, jossa käytetään POS-rekisteri tyyppi.
3.  Määritä kiinteä laitteisto-asema on seuraavat ominaisuudet:
    -   **Isännän nimi** – jossa suoritetaan laitteiston station isäntäkoneen nimi. **Huomautus:** Cloud Myyntipisteen voit ratkaista **localhost** määrittää paikallisen tietokoneen, jossa on käynnissä Cloud POS. Todistuksen, joka edellyttää liitettävään Cloud POS laitteisto-aseman on myös oltava "Localhost" tietokoneen nimenä. Ongelmien välttämiseksi on suositeltavaa luetella myymälän tarvittaessa Kiinteä laitteisto jokaisen aseman esiintymää. Laitteiston kunkin aseman isännän nimi pitäisi olla tietyn tietokonenimen jossa laitteisto asema otetaan käyttöön.
    -   **Portin** – laitteisto asema Moderni myyntipisteen yhteydessä käytettävän portin.
    -   **Laitteistoprofiilin** – Jos laitteistoprofiili ei ole Jos itse laitteisto-asema-laitteistoprofiili, joka on määritetty rekisterissä voidaan käyttää.
    -   **EFT: N POS-numero** – EFT-päätteen tunnus käyttää EFT luvat lähetettäessä. Tämä tunnus on antama luottokorttien käsittelijä.
    -   **Pakettinimi** – kun laitteisto-asema on otettu käyttöön laitteiston station-paketti.

4.  Valitse **jälleenmyynti- ja commerce**&gt;**vähittäismyynnin IT**&gt;**aikataulun jakelu**.
5.  Valitse **1090** jakelu aikataulun synkronointi säilöön uuden laitteistoprofiilin. Valitse **suorittaa nyt** Myyntipiste tehtyjen muutosten synkronointi.
6.  Valitse **1040** jakelu aikataulun synkronointi aseman säilöön uusi laitteisto. Valitse **suorittaa nyt** Myyntipiste tehtyjen muutosten synkronointi.
7.  Asenna laitteisto-asema. Saat lisätietoja siitä, miten voit asentaa laitteisto-asema [Retail-laitteiston määritykset ja asennus](retail-hardware-station-configuration-installation.md).
8.  Asenna ja aktivoi nykyaikaiset POS. Saat lisätietoja siitä, miten asentaa nykyaikaisia POS [Retail POS-Sovelluksen Moderni kokoonpano ja asennus](retail-modern-pos-device-activation.md).
9.  Moderni POS kirjautua ja valita **kassa toimintojen suorittaminen**.
10. Käynnistä **hallita laitteiston asemilla** toimintaa.
11. Valitse **hallinta**.
12. Laitteiston aseman hallinta-sivulla voit ottaa aseman laitteisto asetus.
13. Valitse laitteisto-asema ja valitse sitten **pari**.
14. Kun laitteisto-asema on pareja, valitse **Sulje**.
15. Valitse laitteiston aseman valinta-sivu, muuta se aktiiviseksi laitteiston äskettäin valitun aseman.

### <a name="all-modern-pos-clients-that-have-a-shared-iis-hardware-station"></a>Kaikki nykyaikaiset POS-asiakkailla on jaettu IIS-laitteiston station

Tätä määritystä voi käyttää kaikki nykyaikaiset POS-asiakkaille, jotka laitteiston asemien jakaminen muiden laitteiden kanssa. Voit määrittää tässä kokoonpanossa, toimi seuraavasti.

1.  Voit luoda laitteistoprofiilin, jossa määritetään tarvittavat lisälaitteet.
2.  Luo laitteisto-aseman **jaettujen** Vähittäismyymälä, jossa käytetään POS-rekisteri tyyppi.
3.  Määritä jaettu laitteisto-asema seuraavat ominaisuudet:
    -   **Isännän nimi** – jossa suoritetaan laitteiston station isäntäkoneen nimi.
    -   **Kuvaus** – teksti, joka auttaa tunnistamaan laitteisto-asema **palauttaa** tai **myymälän edessä**.
    -   **Portin** – laitteisto asema Moderni myyntipisteen yhteydessä käytettävän portin.
    -   **Laitteistoprofiilin** – jaettu laitteiston asemien laitteiston kunkin aseman pitäisi olla laitteistoprofiilin. Laitteistoprofiilit voidaan jakaa laitteen asemien kesken, mutta ne on yhdistettävä laite kunkin aseman. Lisäksi on suositeltavaa käyttää jaettu vuorot, kun useita laitteita käyttämällä samaa jaettua laitteiston station. Voit määrittää jaetun VAIHTO, **jälleenmyynti- ja commerce**&gt;**kanava-asetukset**&gt;**POS-asetukset**&gt;**POS-profiilit**&gt;**laitteistoprofiilien**. Kunkin jaetun laitteistoprofiilin kassan ja määrittää **jaettu VAIHTO laatikko** asetukseksi **Kyllä**.
    -   **EFT: N POS-numero** – EFT-päätteen tunnus käyttää EFT luvat lähetettäessä. Tämä tunnus on antama luottokorttien käsittelijä.
    -   **Pakettinimi** – kun laitteisto-asema on otettu käyttöön laitteiston station-paketti.

4.  Toista vaiheet 2 ja 3 kunkin lisälaitteita station, joita tarvitaan kauppa.
5.  Valitse **jälleenmyynti- ja commerce**&gt;**vähittäismyynnin IT**&gt;**aikataulun jakelu**.
6.  Valitse **1090** jakelu aikataulun synkronointi säilöön uuden laitteistoprofiilin. Valitse **suorittaa nyt** Myyntipiste tehtyjen muutosten synkronointi.
7.  Valitse **1040** jakelu aikataulun synkronointi aseman säilöön uusi laitteisto. Valitse **suorittaa nyt** Myyntipiste tehtyjen muutosten synkronointi.
8.  Asenna laitteisto station jokaisen tietokoneen, joka määritetään vaiheet 2 ja 3. Saat lisätietoja siitä, miten voit asentaa laitteisto-asema [Retail-laitteiston määritykset ja asennus](retail-hardware-station-configuration-installation.md).
9.  Asenna ja aktivoi nykyaikaiset POS. Saat lisätietoja siitä, miten asentaa nykyaikaisia POS [Retail POS-Sovelluksen Moderni kokoonpano ja asennus](retail-modern-pos-device-activation.md).
10. Moderni POS kirjautua ja valita **kassa toimintojen suorittaminen**.
11. Käynnistä **hallita laitteiston asemilla** toimintaa.

12. Valitse **hallinta**.
13. Laitteiston aseman hallinta-sivulla voit ottaa aseman laitteisto asetus.
14. Valitse laitteisto-asema ja valitse sitten **pari**.
15. Toista vaihe 14, jotka käyttävät nykyaikaisia POS laitteisto jokaisen aseman.
16. Kun tarvittavat laitteet asemilla on pareja, valitse **Sulje**.
17. Valitse laitteiston aseman valinta-sivu, muuta se aktiiviseksi laitteiston äskettäin valitun aseman. **Huomautus:** jos laitteissa on usein erilaisia laitteita asemilla, on suositeltavaa määrittää nykyaikaisen POS antamaan Valitse kun ne aloittaa tarjouksen aseman laitteisto. Valitse **jälleenmyynti- ja commerce**&gt;**kanava-asetukset**&gt;**POS-asetukset**&gt;**Rekisteröi**. Valitse rekisteri- ja Aseta **Valitse tarjouksen yhteydessä** asetuksella **Kyllä**. Käytössä **1090** jakelu aikataulun synkronointi kanava tietokantaan tehdyt muutokset.

## <a name="extensibility"></a>Laajennettavuus
Lisätietoja laitteiston station laajennettavuus tilanteita, joissa on [Hardware Station kattavampi](dev-itpro/hardware-station-extensibility.md).

## <a name="security"></a>Suojaus
Nykyisen turvallisuusvaatimusten mukaisesti tuotantoympäristössä käytetään seuraavia asetuksia: **Huomautus:** laitteiston aseman Asennusohjelma tekee automaattisesti seuraavat rekisterin muokkauksia itsepalvelun kautta asennuksen yhteydessä.

-   Secure Sockets Layer (SSL) poistetaan käytöstä.
-   Vain Transport Layer Security (TLS) versio 1.2 (tai nykyistä versiota) on otettava käyttöön ja käyttää. **Huomautus:** oletusarvon mukaan SSL- ja TLS TLS 1.2 lukuun ottamatta kaikki versio on poistettu käytöstä. Voit muokata tai ottaa käyttöön nämä arvot, toimi seuraavasti:
    1.  Paina Windows-näppäin key + R voit avata **suorittaa** ikkuna.
    2.  - **Avoin** -kenttään **Regedit**, ja valitse **OK**.
    3.  Jos **Käyttäjätilien valvonnan** sanomaruutu tulee näkyviin, valitse **Kyllä**.
    4.  - **Registry Editor** ikkunassa, siirry **HKEY\_PAIKALLISTEN\_MACHINESystemCurrentControlSetSecurityProvidersSCHANNELProtocols**. Sallia vain TLS 1.2 syötetty automaattisesti seuraavat avaimet:
        -   TLS-1.2Server: käytössä = 1
        -   TLS-1.2Server:DisabledByDefault = 0
        -   TLS-1.2Client: käytössä = 1
        -   TLS-1.2Client:DisabledByDefault = 0
        -   TLS-1.1Server: käytössä = 0
        -   TLS-1.1Client: käytössä = 0
        -   TLS-1.0Server: käytössä = 0
        -   TLS-1.0Client: käytössä = 0
        -   SSL 3.0Server: käytössä = 0
        -   SSL 3.0Client: käytössä = 0
        -   SSL 2.0Server: käytössä = 0
        -   SSL 2.0Client: käytössä = 0
-   Ei ole muita verkkoportit olisi voitava osallistua, elleivät ne ole pakollinen tiedossa määritetyn syistä.
-   Cross-alkuperä resurssien jakaminen on poistettava käytöstä ja Määritä sallittu alkuperää, joka on hyväksytty.
-   Vain luotettujen sertifikaatin myöntäjien olisi käytettävä hankkia sertifikaatteja, joita käytetään tietokoneissa, joiden käyttöjärjestelmä, laitteisto-asema.

**Huomautus:** on erittäin tärkeää, että luet suojausohjeet IIS ja maksun kortin tuotannonalan (PCI) vaatimukset.

## <a name="peripheral-simulator"></a>Oheislaitesimulaattori
Lisätietoja [Retail peripheral simulator](retail-peripheral-simulator.md).

## <a name="microsofttested-peripheral-devices"></a>Microsofttested oheislaitteiden
### <a name="ipc-built-in-hardware-station"></a>Laitteiston station IPC (sisäinen)

Seuraavat oheislaitteet testattiin käyttäen IPC laitteisto-asema, joka on rakennettu Moderni POS for Windows.

#### <a name="printer"></a>Tulostin

| Valmistaja | Malli    | Käyttöliittymä | Huomautukset                |
|--------------|----------|-----------|-------------------------|
| EPSON        | TM-T88IV | OPOS      |                         |
| EPSON        | TM-T88V  | OPOS      |                         |
| Star         | TSP650II | OPOS      |                         |
| Star         | TSP650II | Mukautettu    | Verkon välityksellä   |
| Star         | mPOP     | OPOS      | Yhdistetty Bluetoothilla |
| HP           | F7M67AA  | OPOS      | Virtaa USB             |

#### <a name="bar-code-scanner"></a>Viivakoodi skanneri

| Valmistaja  | Malli         | Käyttöliittymä | Huomautukset |
|---------------|---------------|-----------|----------|
| Motorola      | DS9208        | OPOS      |          |
| Honeywell     | 1900          | UWP       |          |
| Symboli        | LS2208        | OPOS      |          |
| HP integroitu | E1L07AA       | OPOS      |          |
| Datalogic     | Magellan-8400 | OPOS      |          |

#### <a name="pin-pad"></a>PIN-näppäimistö

| Valmistaja | Malli  | Käyttöliittymä | Huomautukset                                        |
|--------------|--------|-----------|-------------------------------------------------|
| VeriFone     | 1000SE | OPOS      | Vaatii maksun yhdistimen mukauttaminen |

#### <a name="payment-terminal"></a>Maksupääte

| Valmistaja | Malli | Käyttöliittymä | Huomautukset                                                                       |
|--------------|-------|-----------|--------------------------------------------------------------------------------|
| Equinox      | L5300 | Mukautettu    | Vaatii maksun yhdistimen mukauttaminen                                |
| VeriFone     | MX925 | Mukautettu    | Edellyttää mukauttamista maksun yhdysviivalle; Verkko- ja USB välityksellä. |
| VeriFone     | MX915 | Mukautettu    | Edellyttää mukauttamista maksun yhdysviivalle; Verkko- ja USB välityksellä. |

#### <a name="cash-drawer"></a>Kassa

| Valmistaja | Malli     | Käyttöliittymä | Huomautukset                |
|--------------|-----------|-----------|-------------------------|
| Star         | mPOP      | OPOS      | Yhdistetty Bluetoothilla |
| APG          | Atwood    | Mukautettu    | Verkon välityksellä   |
| Star         | SMD2-1317 | OPOS      |                         |
| HP           | QT457AA   | OPOS      |                         |

#### <a name="line-display"></a>Rivinäyttö

| Valmistaja  | Malli   | Käyttöliittymä | Huomautukset |
|---------------|---------|-----------|----------|
| HP integroitu | G6U79AA | OPOS      |          |
| EPSON         | M58DC   | OPOS      |          |

#### <a name="signature-capture"></a>Allekirjoituksen tarkistus

| Valmistaja | Malli  | Käyttöliittymä | Huomautukset |
|--------------|--------|-----------|----------|
| Scriptel     | ST1550 | OPOS      |          |

#### <a name="scale"></a>Mittakaava

| Valmistaja | Malli         | Käyttöliittymä | Huomautukset |
|--------------|---------------|-----------|----------|
| Datalogic    | Magellan-8400 | OPOS      |          |

#### <a name="msr"></a>Magneettinauhan lukulaite

| Valmistaja | Malli       | Käyttöliittymä | Huomautukset |
|--------------|-------------|-----------|----------|
| Magtek       | 21073075    | UWP       |          |
| Magtek       | 21073062    | OPOS      |          |
| HP           | IDRA-334133 | OPOS      |          |

### <a name="dedicated-iis-hardware-station"></a>Kiinteä laitteisto IIS-asema

Seuraavat oheislaitteet testattiin käyttämällä varatussa (ei jaetussa) IIS laitteiston aseman sekä Moderni POS for Windows Cloud POS.

#### <a name="printer"></a>Tulostin

| Valmistaja | Malli    | Käyttöliittymä | Huomautukset                  |
|--------------|----------|-----------|---------------------------|
| EPSON        | TM-T88IV | OPOS      |                           |
| EPSON        | TM-T88V  | OPOS      |                           |
| Star         | TSP650II | OPOS      |                           |
| Star         | TSP650II | Mukautettu    | Verkon välityksellä     |
| Star         | TSP100   | OPOS      | Vaatii TSP650II ohjaimet |
| HP           | F7M67AA  | OPOS      | Virtaa USB               |

#### <a name="bar-code-scanner"></a>Viivakoodi skanneri

| Valmistaja  | Malli   | Käyttöliittymä | Huomautukset |
|---------------|---------|-----------|----------|
| Motorola      | DS9208  | OPOS      |          |
| Symboli        | LS2208  | OPOS      |          |
| HP integroitu | E1L07AA | OPOS      |          |

#### <a name="pin-pad"></a>PIN-näppäimistö

| Valmistaja | Malli  | Käyttöliittymä | Huomautukset                                        |
|--------------|--------|-----------|-------------------------------------------------|
| VeriFone     | 1000SE | OPOS      | Vaatii maksun yhdistimen mukauttaminen |

#### <a name="payment-terminal"></a>Maksupääte

| Valmistaja | Malli | Käyttöliittymä | Huomautukset                                                                       |
|--------------|-------|-----------|--------------------------------------------------------------------------------|
| Equinox      | L5300 | Mukautettu    | Vaatii maksun yhdistimen mukauttaminen                                |
| VeriFone     | MX925 | Mukautettu    | Edellyttää mukauttamista maksun yhdysviivalle; Verkko- ja USB välityksellä. |
| VeriFone     | MX915 | Mukautettu    | Edellyttää mukauttamista maksun yhdysviivalle; Verkko- ja USB välityksellä. |

#### <a name="cash-drawer"></a>Kassa

| Valmistaja | Malli     | Käyttöliittymä | Huomautukset              |
|--------------|-----------|-----------|-----------------------|
| APG          | Atwood    | Mukautettu    | Verkon välityksellä |
| Star         | SMD2-1317 | OPOS      |                       |
| HP           | QT457AA   | OPOS      |                       |

#### <a name="line-display"></a>Rivinäyttö

| Valmistaja  | Malli   | Käyttöliittymä | Huomautukset |
|---------------|---------|-----------|----------|
| HP integroitu | G6U79AA | OPOS      |          |
| EPSON         | M58DC   | OPOS      |          |

#### <a name="signature-capture"></a>Allekirjoituksen tarkistus

| Valmistaja | Malli  | Käyttöliittymä | Huomautukset |
|--------------|--------|-----------|----------|
| Scriptel     | ST1550 | OPOS      |          |

#### <a name="scale"></a>Mittakaava

| Valmistaja | Malli         | Käyttöliittymä | Huomautukset |
|--------------|---------------|-----------|----------|
| Datalogic    | Magellan-8400 | OPOS      |          |

#### <a name="msr"></a>Magneettinauhan lukulaite

| Valmistaja | Malli       | Käyttöliittymä | Huomautukset |
|--------------|-------------|-----------|----------|
| Magtek       | 21073075    | UWP       |          |
| Magtek       | 21073062    | OPOS      |          |
| HP           | IDRA-334133 | OPOS      |          |

### <a name="shared-iis-hardware-station"></a>Jaettu IIS-laitteiston station

Seuraavat oheislaitteet testattiin käyttämällä jaettua IIS laitteiston asema sekä Moderni POS for Windows Cloud POS. **Huomautus:** tuetaan vain tulostin, maksu terminal ja kassa.

#### <a name="printer"></a>Tulostin

| Valmistaja | Malli    | Käyttöliittymä | Huomautukset                  |
|--------------|----------|-----------|---------------------------|
| EPSON        | TM-T88IV | OPOS      |                           |
| EPSON        | TM-T88V  | OPOS      |                           |
| Star         | TSP650II | OPOS      |                           |
| Star         | TSP650II | Mukautettu    | Verkon välityksellä     |
| Star         | TSP100   | OPOS      | Vaatii TSP650II ohjaimet |
| HP           | F7M67AA  | OPOS      | Virtaa USB               |

#### <a name="payment-terminal"></a>Maksupääte

| Valmistaja | Malli | Käyttöliittymä | Huomautukset                                                                       |
|--------------|-------|-----------|--------------------------------------------------------------------------------|
| VeriFone     | MX925 | Mukautettu    | Edellyttää mukauttamista maksun yhdysviivalle; Verkko- ja USB välityksellä. |
| VeriFone     | MX915 | Mukautettu    | Edellyttää mukauttamista maksun yhdysviivalle; Verkko- ja USB välityksellä. |

#### <a name="cash-drawer"></a>Kassa

| Valmistaja | Malli     | Käyttöliittymä | Huomautukset              |
|--------------|-----------|-----------|-----------------------|
| APG          | Atwood    | Mukautettu    | Verkon välityksellä |
| Star         | SMD2-1317 | OPOS      |                       |
| HP           | QT457AA   | OPOS      |                       |

## <a name="troubleshooting"></a>Vianmääritys
### <a name="modern-pos-can-detect-the-hardware-station-in-its-list-for-selection-but-it-cant-complete-the-pairing"></a>Moderni POS laitteisto-asema tunnistaa sen valinta luettelossa, mutta ei voi suorittaa laiteparin muodostaminen

**Ratkaisu:** tarkistaa mahdollisen epäonnistumisen pistettä Seuraava luettelo:

-   Tietokone, jossa on Moderni POS luottaa sertifikaatin, jota käytetään tietokoneessa, joka suorittaa laitteiston station.
    -   Voit tarkistaa asetukset, web-selaimessa, siirry seuraavan URL-Osoitteen: https://&lt;tietokonenimi&gt;:&lt;porttinumero&gt;/HardwareStation/ping.
    -   Varmista, että tietokone voi käyttää ja selain ilmaisee, onko sertifikaatti luotettujen Tämä URL-osoite käyttää ping-kutsuun. (Esimerkiksi Internet Explorerissa kaksoisnapsauttamalla kuvaketta näkyy osoiterivillä. Kun napsautat tätä kuvaketta, Internet Explorer tarkistaa, onko sertifikaatti luotettujen tällä hetkellä. Voit asentaa sertifikaatin paikalliseen tietokoneeseen, todistus, joka esitetään tietoja.)
-   Portti, jota käytetään laitteiston asema avataan tietokoneessa, joka suorittaa aseman laitteisto palomuuri.
-   Laitteisto-asema on asennettu oikein asennus myyjän tiedot työkalun, joka suorittaa laitteiston station asennusohjelman lopussa myyjän tilitiedot.

### <a name="modern-pos-cant-detect-the-hardware-station-in-its-list-for-selection"></a>Moderni POS ei pysty tunnistamaan sen valinnan-luettelosta laitteiston station

**Ratkaisu:** joko seuraavat tekijät saattavat aiheuttaa tämän ongelman:

-   Laitteisto-asema ei ole vielä määritetty oikein headquarters. Tarkista kirjoitettu oikein station laitteistoprofiilin ja laitteiston station tämän ohjeaiheen ohjeiden avulla.
-   Töitä ei ole suoritettu kanavan kokoonpanosta. Tässä tapauksessa Suorita 1070 kanavien konfigurointiin.

### <a name="modern-pos-doesnt-reflect-new-cash-drawer-settings"></a>Moderni POS ei vastaa uutta rahaa laatikko asetukset

**Ratkaisu:** sulkea nykyisen erän. Kassan tehdyt muutokset eivät päivity Moderni POS, kunnes nykyinen erä suljetaan.

### <a name="modern-pos-is-reporting-an-issue-with-a-retail-peripheral"></a>Moderni POS on haavoittuvuudesta retail peripheral kanssa

**Ratkaisu:** tässä on joitakin tavallisia syitä tämän ongelman:

-   Varmista, että laitteen ohjaimen kokoonpanon muita apuohjelmia on suljettu. Jos ne ovat auki, ne voi estää Moderni POS tai laitteisto-asema laitteen väitti.
-   Jos retail oheislaite on jaettu useita POS laitteita, varmista, että se kuuluu johonkin seuraavista luokista:
    -   Kassa
    -   Vastaanotto-tulostin
    -   Maksupääte

    Jos oheislaite ei kuulu johonkin näistä luokista, aseman laitteisto ei ole suunniteltu oheislaite jaetaan kesken useita POS laitteita.
-   Joskus ohjaimet voivat aiheuttaa yhteisten valvonta-objektien (CCOs) voi lakata toimimasta oikein. Jos laite on asennettu viime aikoina, mutta se ei toimi oikein tai muita ongelmia huomaat, voi usein ratkaista ongelman asentamalla CCOs. Voit ladata CCOs, <http://monroecs.com/oposccos_current.htm>.
-   Jos muutat usein syrjäisillä aikana testaamisessa ja vianmäärityksessä, saatat joutua Käynnistä IIS uudelleen odottamatta välimuisti päivittää itse. Jos haluat palauttaa IIS: N, toimi seuraavasti:
    1.  Siitä **käynnistää** valikosta, kirjoita **CMD**.
    2.  Napsauta haun tuloksissa **komentorivi**, ja sitten **Suorita järjestelmänvalvojana**.
    3.  - **Komentorivi** ikkunan, kirjoita **iisreset/restart** ja paina sitten Enter-näppäintä.
    4.  Kun IIS on käynnistetty uudelleen, uudelleen Moderni POS.
-   Kun teet toistuvasti muutoksia oheislaitteita, usein myös aloittaa ja lopettaa myyntipisteen, POS aiemmasta istunnosta dllhost-prosessi voi häiritä nykyisessä istunnossa. Tässä tapauksessa laite ei ehkä voi käyttää ennen kuin olet sulkenut dynaamisesti linkitettävää kirjastoa (DLL) isäntä, joka hallitsee edellisessä istunnossa. Sulje DLL-isäntä, toimi seuraavasti:
    1.  Siitä **käynnistää** valikosta, kirjoita **Tehtävienhallinnan**.
    2.  Valitse etsinnän tulokset- **Tehtävienhallinnan**.
    3.  -Tehtävienhallinta- **tiedot** -välilehdestä sarakeotsikko, jonka nimi on **nimi** voit lajitella taulukon aakkosjärjestykseen nimen mukaan.
    4.  Vieritä alas kunnes löydät dllhost.exe.
    5.  Vastaanottavilla dll-tiedoston, ja valitse sitten **lopetustehtävä**.
    6.  Kun DLL-kirjasto on suljettu hosts, Moderni POS käynnistää uudelleen.


<a name="see-also"></a>Lisätietoja
--------

[Vähittäismyynnin peripheral simulator](retail-peripheral-simulator.md)


