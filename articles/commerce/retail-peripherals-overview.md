---
title: Oheislaitteet
description: Tässä artikkelissa esitellään Commercen oheislaitteisiin liittyvät käsitteet.
author: BrianShook
ms.date: 09/08/2022
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: josaw
ms.custom:
- "268444"
- intro-internal
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: b3113626b18ad7f074c808d7631d13b09071bef2
ms.sourcegitcommit: f88273627ba105ede27f28fe67ccec2d7f78261c
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/09/2022
ms.locfileid: "9459989"
---
# <a name="peripherals"></a>Oheislaitteet

[!include[banner](includes/banner.md)]

Tässä artikkelissa esitellään myymälän oheislaitteisiin liittyvät käsitteet. Artikkelissa kerrotaan, miten oheislaitteet voidaan yhdistää myyntipisteeseen, ja esitellään komponentit, jotka ovat vastuussa myyntipisteen yhteyden hallinnasta.

## <a name="concepts"></a>Käsitteet

### <a name="pos-registers"></a>Kassakoneet

Siirtyminen: **Vähittäismyynti ja kauppa \> Kanavan asetukset \> POS-asetukset \> Kassakoneet**. Myyntipisteen kassakone on yksikkö, jolla määritetään tietyn myyntipisteen esiintymän ominaisuudet. Näitä ominaisuuksia ovat laiteprofiili tai kassakoneessa käytettävien oheislaitteiden asetukset, myymälä, johon kassakone on yhdistetty, ja kyseiseen kassakoneeseen kirjautuvan käyttäjän visuaalinen kokemus.

### <a name="devices"></a>Laitteet

Siirtyminen: **Retail ja Commerce \> Kanavan asetukset \> POS-asetukset \> Laitteet**. Laite on yksikkö, joka ilmaisee myyntipisteen kassakoneeseen yhdistämismääritetyn laitteen fyysisen esiintymän. Kun laite on luotu, siitä muodostetaan yhdistämismääritys myyntipisteen kassakoneeseen. Laiteyksikkö seuraa seuraavia tietoja: myyntipisteen kassakoneen aktivoinnin ajankohta, käytettävän asiakasohjelman tyyppi ja tietyssä laitteessa käyttöönotettu sovelluspaketti. 

Laitteet voidaan yhdistää seuraaviin sovellustyyppeihin: Retail Modern POS, Retail Cloud POS, Retail Modern POS – Android ja Retail Modern POS – iOS.

### <a name="modern-pos"></a>Moderni myyntipiste

Modern POS on Microsoft Windowsin POS-ohjelma. Se voidaan ottaa käyttöön Windows 10- ja Windows 11 -käyttöjärjestelmissä.

### <a name="cloud-pos"></a>Cloud POS

Cloud POS on Modern POS -ohjelman selainpohjainen versio, jota voidaan käyttää selaimen avulla.

### <a name="modern-pos-for-ios"></a>Modern POS iOS:lle

Modern POS iOS:lle on Modern POS -ohjelman iOS-pohjainen versio, joka voidaan ottaa käyttöön iOS-laitteissa.

### <a name="modern-pos-for-android"></a>Modern POS Androidille

Modern POS Androidille onModern POS-ohjelman Android-pohjainen versio, joka voidaanottaa käyttöön Android-laitteissa.

### <a name="pos-peripherals"></a>Myyntipisteen oheislaitteet

Myyntipisteen oheislaitteet ovat laitteita, joita tuetaan eksplisiittisesti myyntipisteen toiminnoissa. Nämä oheislaitteet jaetaan tavallisesti tiettyihin luokkiin. Lisätietoja näistä luokista on tämän artikkelin Laiteluokat-kohdassa.

### <a name="hardware-station"></a>Laiteasema

Siirtyminen: **Retail ja Commerce \> Kanavat \> Myymälät \> Kaikki myymälät**. Valitse ensin myymälä ja sitten **Laiteasemat**-pikavälilehti. **Laiteasema**-asetus on kanavan tason asetus, jota käytetään määritettäessä instanssit, joissa käytetään oheislaitteiden logiikkaa. Tätä kanavatason asetusta käytetään määritettäessä laiteaseman ominaisuudet. Sitä käytetään myös lueteltaessa Modern POS -instanssin tietyssä myymälässä käytettävissä olevat laiteasemat. Laiteasema muodostetaan Windowsin Modern POS -ohjelmiin Windowsille ja Androidille. Laiteasema voidaan ottaa käyttöön myös itsenäisesti Microsoft Internet Information Services (IIS) -palveluiden erillisenä ohjelmana. Tällöin sitä käytetään verkon kautta.

### <a name="hardware-profile"></a>Laiteprofiili

Siirtyminen: **Retail ja Commerce \> Kanavan asetukset \> POS-asetukset \> POS-profiilit \> Laiteprofiilit**. Laitteistoprofiili on niiden laitteiden luettelo, jotka on määritetty myyntipisteen kassakonetta tai laiteasemaa varten. Laiteprofiili voidaan yhdistää suoraan myyntipisteen kassakoneeseen tai laiteasemaan.

## <a name="devices-classes"></a>Laitteiden luokat
Myyntipisteen oheislaitteet jaetaan tavallisesti luokkiin. Tässä osassa esitellään Modern POS -sovelluksen tukemat laitteet ja laitteiden yleiskatsaus.

### <a name="printer"></a>Tulostin

Tulostimet sisältävät perinteiset myyntipisteiden kuittitulostimet ja koko sivun tulostimet. Tulostimia tuetaan Retail POS objektien linkittämisen ja upottamisen (OPOS) ja Microsoft Windows -ohjaimen liittymien kautta. Samaan aikaan voi käyttää enintään kahta tulostinta. Tämä ominaisuus tukee skenaarioita, joissa itsepalvelutukkuasiakkaiden kuitit tulostetaan kuittitulostimella. Enemmän tietoja sisältävät asiakastilaukset sen sijaan tulostetaan koko sivun tulostimella. Kuittitulostimet voidaan yhdistää suoraan tietokoneeseen USB-liitännän avulla ja verkkoon Ethernet-kaapelin avulla. Ne voidaan yhdistää myös Bluetoothin avulla.

### <a name="scanner"></a>Skanneri

Samaan aikaan voi käyttää enintään kahta viivakoodin lukulaitetta. Tämä ominaisuus tukee skenaarioita, joissa vaaditaan liikkuvaa skanneria suurten tai painavien tuotteiden lukemista varten. Kiinteää ja upotettua skanneria puolestaan käytetään useimmissa normaalikokoisissa tuotteissa kassatoimintojen nopeuttamiseksi. OPOS, universaali Windows-ympäristö (Universal Windows Platform, UWP) tai näppäimistön kortinlukijaliittymät voivat tukea skannereita. Skanneri voidaan yhdistää tietokoneeseen USB:n tai Bluetoothin avulla.

### <a name="msr"></a>Magneettinauhan lukulaite

OPOS-ohjainten avulla voidaan määrittää yksi USB-magneettinauhan lukulaite. Jos haluat käyttää erillistä magneettinauhan lukulaitetta sähköisten rahansiirtojen maksutapahtumissa, maksuyhdistimen on hallittava magneettinauhan lukulaitetta. Erillisiä magneettinauhan lukulaitteita ei voi käyttää asiakkaan kanta-asiakasmerkinnässä, työntekijän kirjautumisessa eikä lahjakorttimerkinnässä maksuyhdistimestä riippumatta.

### <a name="cash-drawer"></a>Kassa

Laiteprofiili voi tukea kahta kassaa. Tämä ominaisuus mahdollistaa kaksi samanaikaista aktiivista vuoroa kassakonetta kohti. Jos kyseessä on jaettu vuoro tai kassa, joka on useiden myyntipisteiden mobiililaitteiden käytettävissä samanaikaisesti, laiteprofiilia kohti sallitaan vain yksi kassa. Kassat voidaan yhdistää suoraan tietokoneeseen USB-liitännän avulla tai verkkoon. Ne voidaan yhdistää myös kuittitulostimeen RJ12-liittymän kautta. Joissakin tapauksissa kassat voidaan yhdistää myös Bluetoothin kautta.

### <a name="line-display"></a>Rivinäyttö

Rivinäyttöjä käytetään tuotteiden, tapahtumien saldojen ja muiden hyödyllisten tietojen näyttämisessä asiakkaalle tapahtuman aikana. Yksi rivinäyttö voidaan yhdistää tietokoneeseen USB-liitännän tai OPOS-ohjainten avulla.

### <a name="signature-capture"></a>Allekirjoituksen tarkistus

Allekirjoituksen tarkistuslaitteet voidaan yhdistää tietokoneeseen suoraan USB-liitännän tai OPOS-ohjainten avulla. Kun allekirjoituksen tarkistus on määritetty, asiakasta pyydetään kirjautumaan laitteelle. Kun allekirjoitus on saatu, se näytetään kassanhoitajalle hyväksymistä varten.

### <a name="scale"></a>Asteikko

Vaa'at voidaan yhdistää tietokoneeseen USB-liitännän tai OPOS-ohjainten avulla. Kun tapahtumaan lisätään tuote, joka on merkitty punnittavaksi tuotteeksi, myyntipiste lukee painon vaa'alta, lisää tuotteen tapahtumaan ja käyttää vaa'an antamaa määrää.

### <a name="pin-pad"></a>PIN-näppäimistö

OPOS tukee henkilökohtaisen tunnistenumeron näppäimistöjä, mutta niiden hallinta on tehtävä maksuyhdistimen kautta.

### <a name="secondary-display"></a>Toissijainen näyttö

Kun toissijainen näyttö määritetään, perustiedot näytetään Windowsin numero 2 -näytössä. Oletusarvon mukaan toissijainen näyttö ei ole konfiguroitava, ja siinä näkyy rajoitettua sisältöä. Toissijaisen näytön tarkoituksena on tukea itsenäisen ohjelmistotoimittajan (ISV) laajennusta. 

### <a name="payment-device"></a>Maksulaite

Maksulaitteen tuki otetaan käyttöön maksuyhdistimen kautta. Maksulaitteet voivat suorittaa yhden tai useita toimintoja, jotka muut laiteluokat mahdollistavat. Esimerkiksi maksulaite voi toimia magneettinauhan/kortin lukulaitteena, rivinäyttönä, allekirjoituksen tarkistuslaitteena tai PIN-näppäimistönä. Maksulaitteiden tuki otetaan käyttöön erillisenä osana muille laiteprofiiliin kuuluville laitteille annettavan erillisten laitteiden tuesta.

## <a name="supported-interfaces"></a>Tuetut liittymät
### <a name="opos"></a>OPOS

Jotta suurinta osaa laitteista voidaan käyttää Commercen kanssa, myyntipistetoimialan OLE-standardi on ensisijainen oheislaiteympäristö, jota tuetaan. Myyntipisteen OLE-standardin tuottaja on National Retail Federation (NRF), joka tekee toimialakohtaisia tietoliikenneprotokollia oheislaitteille. OPOS on myyntipisteen OLE-standardin laajalti hyväksytty toteutus. OPOS kehitettiin 1990-luvun puolivälissä, jonka jälkeen sitä on päivitetty useita kertoja. OPOS tarjoaa laiteohjainarkkitehtuurin, jonka avulla myyntipisteen laite on helppo integroida Windows-pohjaisiin myyntipistejärjestelmiin. OPOS-ohjausobjektit hoitavat viestinnän yhteensopivan laitteen ja myyntipisteohjelmiston välillä. OPOS-ohjaus sisältää seuraavat kaksi osaa:

-   **Ohjausobjekti** – Laiteluokan (kuten rivinäytön) ohjausobjekti sisältää ohjelman liittymän. Monroe Consulting Services ([www.monroecs.com](http://www.monroecs.com/)) tarjoaa vakiojoukon OPOS-ohjausobjekteja, jota kutsutaan myös yhteisiksi ohjausobjekteiksi (CCO). Commercen myyntipisteen komponentti testataan yhteisten ohjausobjektien avulla. Testaamisen avulla voidaan varmistaa, että jos Commerce tukee laiteluokkaa OPOS:n kautta, useita laitetyyppejä voidaan tukea, jos valmistaja tarjoaa OPOS:lle muodostetun palveluobjektin. Jokaista laitetyyppiä ei tarvitse testata eksplisiittisesti.
-   **Palveulobjekti** – Palveluobjekti mahdollistaa ohjausobjektin ja laitteen välisen yhteydenpidon. Laitteen valmistaja tarjoaa yleensä laitteen palveluobjektin. Joissakin tapauksissa palveluobjekti on kuitenkin ladattava valmistajan sivustosta. Saatavana voi olla esimerkiksi uudempi palveluobjekti. Valmistajan sivuston osoite löytyy laitteen dokumentaatiosta.

[![Ohjausobjekti ja palveluobjekti.](./media/retail_peripherals_overview01.png)](./media/retail_peripherals_overview01.png) Myyntipisteen OLE:n OPOS-toteutuksen tuki auttaa varmistamaan, että laitteiden valmistajat ja myyntipisteen julkaisijat ottavat standardin käyttöön oikein. Myyntipisteiden järjestelmät ja tuetut laitteet voivat toimia yhdessä, vaikka niitä ei olisi aiemmin testattu yhdessä. 

> [!NOTE]
> OPOS-tuki ei takaa sitä, että kaikkia OPOS-ohjaimen sisältäviä laitteita tuetaan. Commercen on ensin tuettava tätä laitetyyppiä tai -luokkaa OPOS:n kautta. Lisäksi palveluobjekteja ei ehkä aina ole päivitetty uusimman ohjausobjektiversion mukaisesti. Ota huomioon, että yleensä palveluobjektien laatu vaihtelee.

### <a name="windows"></a>Windows

Kuitin tulostaminen myyntipisteessä on optimoitu OPOS:ia varten. OPOS-tulostaminen on yleensä paljon nopeampaa kuin tulostaminen Windowsin kautta. Tämän vuoksi kannattaa käyttää OPOS:ia erityisesti ympäristöissä, joissa tulostetaan 40 sarakkeen kuitteja ja joiden tapahtuma-aikojen tulee olla lyhyitä. Useimmissa laitteissa käytetään OPOS-ohjausobjekteja. Jotkin OPOS-kuittitulostimet kuitenkin tukevat myös Windows-ohjaimia. Kun käytössä on Windows-ohjain, voit käyttää uusimpia fontteja ja yhtä verkkotulostinta useissa kassakoneissa. Windows-ohjainten käyttämisessä on kuitenkin huonoja puolia. Seuraavassa on joitakin esimerkkejä näistä huonoista puolista:

-   Kun käytetään Windows-ohjaimia, kuvat muodostetaan ennen tulostamista. Tämän vuoksi tulostaminen on yleensä hitaampaa kuin OPOS-ohjausobjekteja käyttävissä tulostimissa.
-   Laitteet, jotka on yhdistetty tulostimen kautta (ketjutettu), eivät ehkä toimi oikein Windows-ohjainten kanssa. Esimerkiksi kassa ei ehkä avaudu tai kuittitulostin ei toimi odotetulla tavalla.
-   OPOS tukee myös laajempaa kuittitulostimille määritettyä muuttujajoukkoa, kuten paperin leikkaamista ja luettelon tulostamista.
-   Windows-tulostimia ei tueta IIS-laiteasemalla. 

Jos OPOS-ohjausobjektit ovat käytettävissä käyttämässäsi Windows-tulostimessa, tulostin todennäköisesti toimii oikein Commercen kanssa.

### <a name="plug-and-play-devices"></a>Automaattisesti liitettävät laitteet

Kun automaattisesti liitettävä laite yhdistetään Windows OS:n versioon, joka tukee kyseistä laitetyyppiä, laitteen ohjainta ei vaadita. Jos esimerkiksi Windows tunnistaa Bluetooth-kaiuttimen, OS tietää, että laitteen luokkatyyppi on "Kaiutin" ja pitää laitetta kaiuttimena. Lisäasetuksia ei vaadita. 

Myyntipisteiden oheislaitteissa voidaan ottaa käyttöön useita USB-laitteita niin, että Windows-käyttöjärjestelmä tunnistaa ne HID (Human Interface Device) -laitteiksi. Windows ei ehkä kuitenkaan pysty määrittämään laitteen ominaisuuksia, koska laite ei määritä laitteen luokkaa tai tyyppiä. Windows 10 -käyttöjärjestelmässä viivakoodin ja magneettinauhan lukulaitteiden laiteluokat on lisätty. Jos siis laite ilmaisee Windows 10:lle kuuluvansa johonkin näistä luokista, Windows kuuntelee laitteen tapahtumia soveltuvina ajankohtina.

Modern POS tukee universaalia Windows-ympäristöä ja skannereita. Kun Modern POS on valmis ottamaan vastaan jonkin mainitun laitteen syötteen ja yhdistetty laite kuuluu johonkin mainituista laiteluokista, laitetta voidaan käyttää. Jos esimerkiksi automaattisesti tunnistettava viivakoodin lukulaite kytketään Windows 10 -tietokoneeseen ja viivakoodin kirjautuminen on määritetty Modern POS -myyntipistettä varten, viivakoodin lukulaite aktivoidaan kirjautumissivulla. Lisäasetuksia ei vaadita.

Windowsiin lisätään muita POS-oheislaitteita, kuten kassakoneita ja kuittitulostimia. Näiden uusien laiteluokkien Modern POS -tuki on tulossa.

> [!NOTE] 
> Tietyt USB-laitteet voivat olla epäluotettavia tai ne eivät vastaa, kun niitä hallitaan Windows 10 power management -ominaisuuden avulla. Se on nimeltään [USB:n valikoiva keskeytys](/windows-hardware/drivers/usbcon/usb-selective-suspend). Jos USB-oheislaite ei vastaa, on ehkä poistettava valikoiva keskeytystoiminto käytöstä laitteessa. Lisätietoja on kohdassa [Valikoivan keskeytyksen käyttöönotto](/windows-hardware/drivers/usbcon/usb-selective-suspend#enabling-selective-suspend). 

### <a name="keyboard-wedge"></a>Näppäimistön kortinlukija

Näppäimistön kortinlukulaitteet lähettävät tiedot tietokoneelle niin kuin ne olisi kirjoitettu näppäimistön avulla. Tämän vuoksi myyntipisteen aktiivinen kenttä vastaanottaa skannerilla luetut tai lukupään avulla luetut tiedot. Joissakin tapauksissa tämä toiminto voi aiheuttaa väärien tietojen lukemisen kenttään. Esimerkiksi viivakoodi voidaan lukea kenttään, joka on tarkoitettu luottokorttitiedoille. Useissa tapauksissa myyntipiste sisältää logiikan, joka määrittää luetut tiedot viivakoodin tai kortin lukemiseksi. Tämän vuoksi tietojen käsittely tapahtuu oikein. Jos laitteet on kuitenkin määritetty OPOS-laitteiksi näppäimistön kortinlukijalaitteiden sijaan, laitteiden tietojen käyttämiseen liittyy enemmän ohjausta. Tämä johtuu siitä, että laitteesta, josta tiedot ovat peräisin, tiedetään enemmän. Esimerkiksi viivakoodin lukulaitteen tiedot tunnistetaan automaattisesti viivakoodiksi ja tietokannan liittyvä tietue löytyy helpommin ja nopeammin kuin silloin, kun käytössä esimerkiksi näppäimistön kortinlukijalaitteissa käytettävä yleinen merkkijonohaku.

> [!NOTE]
> Kun kassapäätteessä käytetään näppäimistön wedge-skanneria, ne on ohjelmoitu lähettämään kuljetuspalautus tai **anna** tapahtuma viimeisen skannatun merkin jälkeen. Jos tätä määritystä ei tehdä, näppäimistön wedge-skannerit eivät toimi oikein. Laitteen valmistajan toimittamassa dokumentaatiossa on tietoja kuljetuspalautustapahtuman lisäämisistä.  

### <a name="device-printers"></a>Laitetulostimet

Laite-tyyppiä olevat tulostimet voidaan määrittää niin, että ne pyytävät käyttäjää valitsemaan tietokoneelle määritetyn tulostimen. Kun tulostimen tyyppi on "Laite" ja Modern POS:lle lähetetään tulostuskomento, käyttäjää pyydetään valitsemaan tulostin luettelosta. Tämä toiminta eroaa Windows-ohjainten toiminnasta, koska Windows-tyyppisten tulostimien laiteprofiili ei näytä käyttäjälle tulostinluetteloa. Tämän sijaan tulostimen nimi on annettava **Laitteen nimi** -kenttään.

### <a name="network"></a>Verkko

Verkossa käytettäviä kassoja, kuittitulostimia ja maksupäätteitä voi käyttää verkossa joko suoraan Modern POS Windowsille -sovellukselle muodostetun IPC (Interprocess Communications) -laiteaseman tai muiden Modern POS -asiakasohjelmien IIS-laiteasemien kautta.

## <a name="hardware-station-deployment-options"></a>Laiteaseman käyttöönoton asetukset

### <a name="dedicated"></a>Varattu

Nykyaikaisissa POS-asiakkaissa Windowsille ja Androidille on **Erilliset** tai sisäänrakennetut laiteasemat. Nämä asiakkaat voivat kommunikoida suoraan oheislaitteiden kanssa käyttämällä sovelluksiin sisäänrakennettua liiketoimintalogiikkaa. Android- sovellus tukee vain verkkolaitteita. Lisätietoja Android-järjestelmänoheistuesta on artikkelissa [POS Hybrid -sovelluksen määrittäminen Androidille ja iOS:lle](./dev-itpro/hybridapp.md).

Suorita seuraavat vaiheet, kun haluat käyttää varattua laiteasemaa.

1. Liitä laiteprofiili Modern POS Windows- tai Android-sovellusta käyttävään kassakoneeseen.
1. Luo "Varattu"-tyyppinen laiteasema myymälälle, jossa kassakonetta käytetään. 
1. Avaa Modern POS ei-kassatilassa ja ota laiteasemaominaisuudet käyttämällä **Laiteasemien hallinta** -toimintoa. Laite, jonka varattu laiteasema on oletusarvon mukaan aktiivinen. 
1. Kirjaudu ulos Modern POS -sovelluksesta. Kirjaudu takaisin sisään ja avaa vuoro. Laiteprofiiliin määritetyt oheislaitteet ovat nyt käyttökelpoisia. 

### <a name="shared"></a>Jaettu

Joskus kutsutaan myös IIS-laiteasemaksi. IIS tarkoittaa sitä, että POS-sovellus muodostaa yhteyden laitteistoasemaan Microsoftin Internet Information Servicesin kautta. Myyntipisteen sovellus muodostaa yhteyden IIS-laiteasemaan sen tietokoneen verkkopalveluiden avulla, johon laite on yhdistetty. Kun jaettu laiteasema on käytössä, laiteasemaan yhdistettyjä oheislaitteita voi käyttää missä tahansa sellaisessa myyntipisteen kassakoneessa, joka kuuluu samaan verkkoon kuin IIS-laiteasema. Koska vain Modern POS for Windowsille ja Androidille sisältää oheislaitteiden sisäänrakennetun tuen, kaikissa muissa Modern POS -sovelluksissa on käytettävä IIS-laiteasemaa. Näin laiteprofiilissa määritettyihin myyntipisteen oheislaitteisiin voidaan muodostaa yhteys. Tämän vuoksi kukin IIS-laiteaseman instanssi vaatii tietokoneen, jossa on käytössä verkkopalvelu ja sovellus, joka on yhteydessä laitteiden kanssa. 

Jaetun laiteaseman avulla voidaan sallia useiden myyntipisteiden jakaa oheislaitteet tai hallita sidottuja oheislaitteita yhdessä myyntipisteessä. 

Kun laiteasemaa käytetään tukemaan oheislaitteiden jakamista useiden POS-asiakkaiden välillä, käytetään vain käteislaatikoita, kuittitulostimia ja maksupäätteitä. Yhteyttä ei voi muodostaa suoraan erillisiin viivakoodin lukulaitteisiin, magneettinauhan lukulaitteisiin, vaakoihin tai muihin laitteisiin. Muussa tapauksessa aiheutuu ristiriitoja, kun useiden myyntipisteiden laitteet yrittävät käyttää oheislaitteita samaan aikaan. Ristiriitoja hallitaan tuetuissa laitteissa seuraavalla tavalla:

-   **Kassa** – Kassa avautuu laitteelle lähetetyn tapahtuman kautta. Ongelma kassan kutsumisessa voi tapahtua, kun kassa on jo auki. Jos käytössä on jaetun laiteaseman määritys, kassan tyypiksi laiteprofiilissa on määritettävä **Jaettu**. Tämän asetuksen seurauksena myyntipiste ei tarkista, onko kassa jo auki, kun se lähettää avauskomennon.
-   **Kuittitulostin** – Jos laiteasemalle lähetetään kaksi kuittitulostuskomentoa samaan aikaan, jompikumpi komento menetetään laitteesta riippuen. Joissakin laitteissa on käytössä sisäinen muisti tai ryhmitystoiminto, jolloin tämä ongelma ei esiinny. Jos tulostuskomento ei onnistu, kassanhoitaja vastaanottaa virhesanoman. Tämän jälkeen hän voi lähettää tulostuskomennon uudelleen myyntipisteestä.
-   **Maksupääte** – Jos kassanhoitaja yrittää käyttää tapahtumassa maksuvälinettä maksupäätteellä, joka on jo käytössä, kassanhoitaja vastaanottaa sanoman, jossa kerrotaan päätteen olevan käytössä ja kehotetaan yrittämään myöhemmin uudelleen. Kassanhoitajat yleensä näkevät, että pääte on käytössä, ja odottavat tapahtuman valmistumista ennen kuin yrittävät käyttää maksuvälinettä uudelleen.

Tuleviin versioihin on suunnitellaan tarkistusta, joka havaitsee jaettuun laiteasemaan yhdistettyyn laiteprofiiliin määritetyt laitteet, joita ei tueta. Jos ei-tuettuja laitteita havaitaan, käyttäjä vastaanottaa sanoman, jossa kerrotaan, että laitteita ei tueta jaetuissa laiteasemissa. Valitse jaetuissa laiteasemissa **Valitse maksuvälinetapahtuman aikana** -valinnan arvoksi **Kyllä** kassakoneen tasolla. Myyntipisteen käyttäjää pyydetään valitsemaan laiteasema, kun tapahtumalle valitaan maksuväline myyntipisteessä. Kun laiteasema valitaan vain maksuvälinetapahtuman aikana, laiteaseman valinta lisätään suoraan mobiiliskenaarioiden myyntipisteen työnkulkuun. Maksupäätteen rivinäyttö ei ole käytössä jaetuissa skenaarioissa. Jos maksupäätettä käytetään rivinäyttönä, muiden käyttäjien pääsy päätteelle saatetaan estää tapahtuman valmistumiseen asti. Mobiiliskenaarioissa rivejä saatetaan lisätä tapahtumaan pitkän ajan kuluessa. Tämän vuoksi **Valitse maksuvälinetapahtuman aikana** -valinta on pakollinen. Se varmistaa, että laite on käytettävissä.

### <a name="network-peripherals"></a>Verkon oheislaitteet

Laiteprofiilin laitteiden verkkosuunnittelun avulla kassat, kuittitulostimet ja maksupäätteet voidaan yhdistää verkkoyhteyden avulla.

#### <a name="modern-pos-for-windows"></a>Modern POS Windowsille

Voit määrittää verkon oheislaitteiden IP-osoitteet kahdessa kohdassa. Jos Modern POS:n Windows-asiakasohjelma käyttää yhtä verkon oheislaitejoukkoa, IP-osoitteet on määritettävä laitteille, joissa on otettu käyttöön kassakoneen toimintoruudun **IP-määritys**-valinta. Jos verkkolaitteet jaetaan myyntipisteiden kassakoneille, laiteprofiili, johon on liitetty verkkolaitteita, voidaan yhdistää suoraan jaettuihin laiteasemiin. Voit määrittää IP-osoitteet, kun valitset laiteaseman **Myymälät**-sivulla ja määrität laiteasemaan liitetyt verkkolaitteet **Laiteasemat**-osan **IP-määritys**-valinnan avulla. Jos laiteasemissa on vain verkkolaitteita, laiteasemaa ei tarvitse ottaa käyttöön. Tällöin laiteasema vaaditaan vain, jos verkossa käytettävät laitteet ryhmitellään käsitteellisesti myymälän sijainnin mukaan.

#### <a name="cloud-pos-and-modern-pos-for-ios"></a>Cloud POS ja Modern POS iOS:lle

Laiteasema sisältää logiikan, joka ohjaa fyysisesti liitettyjä ja verkossa käytettäviä oheislaitteita. Tämän vuoksi IIS-laiteasema on otettava käyttöön ja aktivoitava kaikille myyntipisteen asiakasohjelmille Modern POS Windowsia ja Androidia lukuun ottamatta. Näin myyntipiste voi muodostaa yhteyden oheislaitteiden kanssa huolimatta siitä, onko oheislaitteet yhdistetty fyysisesti laiteasemaan vai ovatko ne verkossa käytettävissä.

## <a name="setup-and-configuration"></a>Asetukset ja määrittäminen
### <a name="hardware-station-installation"></a>Laiteaseman asentaminen

Lisätietoja IIS-laiteaseman asentamisesta on kohdassa [Hardware Stationin määrittäminen ja asentaminen](retail-hardware-station-configuration-installation.md).

### <a name="modern-pos-for-windows-setup-and-configuration"></a>Moderni POS Windowsille -sovelluksen asetus ja määritys

Lisätietoja on kohdassa [Modern POS:n (MPOS) määrittäminen, asentaminen ja aktivoiminen](retail-modern-pos-device-activation.md).

### <a name="modern-pos-for-android-and-ios-setup-and-configuration"></a>Moderni POS Androidille ja iOS:ille -sovelluksen asetus ja määritys

Katso lisätietoja kohdasta [POS Hybrid -sovelluksen määrittäminen Android- ja iOS-laitteissa](./dev-itpro/hybridapp.md).

### <a name="opos-device-setup-and-configuration"></a>OPOS-laitteen asetukset ja määrittäminen

Lisätietoja OPOS-komponenteista on tämän asiakirjan Tuetut liittymät -osassa. Laitteen valmistaja toimittaa yleensä OPOS-ohjaimet. Kun OPOS-laitteen ohjain asennetaan, se lisää Windows-rekisteriin avaimen johonkin seuraavista kohdista:

-   **32-bittinen järjestelmä:** HKEY\_LOCAL\_MACHINE\SOFTWARE\OLEforRetail\ServiceOPOS
-   **64-bittinen järjestelmä:** HKEY\_LOCAL\_MACHINE\SOFTWARE\WOW6432Node\OLEforRetail\ServiceOPOS

ServiceOPOS-rekisterin sijainnissa määritetyt laitteet järjestetään OPOS-laitteiden luokkien mukaan. Tallennetaan useita laiteohjaimia.

## <a name="supported-scenarios-by-hardware-station-type"></a>Tuetut skenaariot laiteaseman tyypin mukaan
### <a name="client-support--ipc-hardware-station-vs-iis-hardware-station"></a>Asiakasohjelman tuki – IPC-laiteasema vs. IIS-laiteasema

Seuraavassa taulukossa esitellään tuetut topologiat ja käyttöönottotilanteet.

| Asiakas      | IPCL-laiteasema | IIS-laiteasema |
|-------------|----------------------|----------------------|
| Windows-sovellus | Kyllä                  | Kyllä                  |
| Cloud POS   | Ei                   | Kyllä                  |
| Android     | Kyllä                  | Kyllä                  |
| iOS         | Ei                   | Kyllä                  |

### <a name="network-peripherals"></a>Verkon oheislaitteet

Verkon oheislaitteita voidaan tukea suoraan Modern POS Windowsille ja Androidille -sovelluksiin muodostetun laiteaseman kautta. Muille asiakasohjelmille on otettava käyttöön IIS-laiteasema.

| Asiakas      | IPCL-laiteasema | IIS-laiteasema |
|-------------|----------------------|----------------------|
| Windows-sovellus | Kyllä                  | Kyllä                  |
| Cloud POS   | Ei                   | Kyllä                  |
| Android     | Kyllä                  | Kyllä                  |
| iOS         | Ei                   | Kyllä                  |

## <a name="supported-device-types-by-hardware-station-type"></a>Tuetut laitetyypit laiteaseman tyypin mukaan
### <a name="modern-pos-for-windows-with-an-ipc-built-in-hardware-station"></a>Modern POS Windowsille ja IPC-laiteasema (sisäänrakennettu)

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Tuettu laiteluokka</th>
<th>Tuetut liittymät</th>
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
<li>UWP (asetusta ei tarvita)</li>
<li>Näppäimistön kortinlukija (asennusta ei tarvita)</li>
</ul></td>
</tr>
<tr class="even">
<td>Asettaja</td>
<td><ul>
<li>OPOS</li>
<li>Verkko </br><strong>Huomautus:</strong> vain yksi kassa voidaan määrittää, jos kassalle on määritetty <strong>Käytä jaettua vuoroa</strong> -asetus.</li>
</ul></td>
</tr>
<tr class="odd">
<td>Kassa 2</td>
<td><ul>
<li>OPOS</li>
<li>Verkko </br><strong>Huomautus:</strong> vain yksi kassa voidaan määrittää, jos kassalle on määritetty <strong>Käytä jaettua vuoroa</strong> -asetus.</li>
</ul></td>
</tr>
<tr class="even">
<td>Skanneri</td>
<td><ul>
<li>OPOS</li>
<li>UWP (asetusta ei tarvita)</li>
<li>Näppäimistön kortinlukija (asennusta ei tarvita)</li>
</ul></td>
</tr>
<tr class="odd">
<td>Skanneri 2</td>
<td><ul>
<li>OPOS</li>
<li>UWP (asetusta ei tarvita)</li>
<li>Näppäimistön kortinlukija (asennusta ei tarvita)</li>
</ul></td>
</tr>
<tr class="even">
<td>Mittakaava</td>
<td>OPOS</td>
</tr>
<tr class="odd">
<td>PIN-näppäimistö</td>
<td>OPOS (tuki annetaan maksuyhdistimen mukauttamisen kautta)</td>
</tr>
<tr class="even">
<td>Allekirjoituksen tarkistus</td>
<td>OPOS</td>
</tr>
<tr class="odd">
<td>Maksupääte</td>
<td><ul>
<li>Mukautetun laitteen tuki</li>
<li>Verkko (lisätietoja on maksuyhdistimen dokumentaatiossa)</li>
</ul></td>
</tr>
</tbody>
</table>

### <a name="all-modern-pos-clients-that-have-a-committed-shared-iis-hardware-station"></a>Kaikki Modern POS -asiakasohjelmat, joilla on sidottu jaettu IIS-laiteasema

> [!NOTE]
> Kun IIS-laiteasema on sidottu, myyntipisteen asiakasohjelman ja laiteaseman välillä on yksi yhteen -suhde.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Tuettu laiteluokka</th>
<th>Tuetut liittymät</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Tulostin</td>
<td><ul>
<li>OPOS</li>
<li>Verkko</li>
</ul></td>
</tr>
<tr class="even">
<td>Tulostin 2</td>
<td><ul>
<li>OPOS</li>
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
<li>Verkko </br><strong>Huomautus:</strong> laiteprofiilille voidaan määrittää vain yksi kassa, jos kassalle on määritetty <strong>Käytä jaettua vuoroa</strong> -asetus.</li>
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
<td>OPOS (tuki annetaan maksuyhdistimen mukauttamisen kautta)</td>
</tr>
<tr class="odd">
<td>Allekirj. kaappaa</td>
<td>OPOS</td>
</tr>
<tr class="even">
<td>Maksupääte</td>
<td><ul>
<li>Mukautetun laitteen tuki</li>
<li>Verkko (lisätietoja on maksuyhdistimen dokumentaatiossa)</li>
</ul></td>
</tr>
</tbody>
</table>

### <a name="all-modern-pos-clients-that-share-an-iis-hardware-station"></a>Kaikki Modern POS -asiakasohjelmat, jotka jakavat IIS-laiteaseman

> [!NOTE]
> Kun IIS-laiteasema on jaettu, useat laitteet voivat käyttää laiteasemaa samanaikaisesti. Tässä tilanteessa tulee käyttää vain seuraavan taulukon laitteita. Jos yrität jakaa laitteita, joita taulukosta ei löydy, kuten viivakoodin tai magneettinauhan lukulaitteita, tuloksena on virhe, kun useat laitteet yrittävät käyttää samaa oheislaitetta. Tulevissa versioissa tällaisen määrityksen tekeminen estetään eksplisiittisesti.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Tuettu laiteluokka</th>
<th>Tuetut liittymät</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Tulostin</td>
<td><ul>
<li>OPOS</li>
<li>Verkko</li>
</ul></td>
</tr>
<tr class="even">
<td>Tulostin 2</td>
<td><ul>
<li>OPOS</li>
<li>Verkko</li>
</ul></td>
</tr>
<tr class="odd">
<td>Asettaja</td>
<td><ul>
<li>OPOS</li>
<li>Verkko </br><strong>Huomautus:</strong> laiteprofiilille voidaan määrittää vain yksi kassa, jos kassalle on määritetty <strong>Käytä jaettua vuoroa</strong> -asetus.</li>
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
<li>Verkko (lisätietoja on maksuyhdistimen dokumentaatiossa)</li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="configuration-for-supported-scenarios"></a>Tuettujen skenaarioiden määritys
Lisätietoja laiteprofiilien luomisesta on kohdassa [Oheislaitteiden yhdistämiseen myyntipisteeseen](define-maintain-channel-clients-registers-hw-stations.md). 

### <a name="modern-pos-for-windows-with-an-ipc-built-in-hardware-station"></a>Modern POS Windowsille ja IPC-laiteasema (sisäänrakennettu)

Tämä määritys on yleisin perinteisissä kiinteissä myyntipisteen kassakoneissa. Tämän skenaarion laiteprofiilin tiedot yhdistetään suoraan kassakoneeseen. EFT-päätteen numero on määritettävä myös kassakoneeseen. Voit tehdä nämä määritykset seuraavien vaiheiden avulla.

1.  Luo laiteprofiili, jossa kaikki vaaditut oheislaitteet on määritetty.
2.  Yhdistä laiteprofiili myyntipisteen kassakoneeseen.
3.  Luo **Varattu**-tyyppinen laiteasema myymälälle, jossa myyntipisteen kassakonetta käytetään. Kuvaus on valinnainen. 

    > [!NOTE]
    > Laiteaseman muita ominaisuuksia ei tarvitse määrittää. Kaikki vaaditut tiedot, kuten laiteprofiili, saadaan kassakoneelta.

4.  Mene kohtaan **Retail ja Commerce \> Retail ja Commerce IT \> Jakeluaikataulu**.
5.  Valitse **1090**-jakeluaikataulu, kun haluat synkronoida uuden laiteprofiilin myymälän kanssa. Valitse **Suorita nyt**, kun haluat synkronoida muutokset myyntipisteen kanssa.
6.  Valitse **1040**-jakeluaikataulu, kun haluat synkronoida uuden laiteaseman myymälän kanssa. Valitse **Suorita nyt**, kun haluat synkronoida muutokset myyntipisteen kanssa.
7.  Asenna ja aktivoi Modern POS Windowsille.
8.  Käynnistä Modern POS Windowsille ja aloita yhdistettyjen oheislaitteiden käyttäminen.

### <a name="modern-pos-for-android-with-an-ipc-built-in-hardware-station"></a>Modern POS Androidille ja IPC-laiteasema (sisäänrakennettu)

**Uutta versiossa 10.0.8** - Epson-verkkotulostimet ja näihin tulostimiin liitetyt kassakoneet ovat nyt tuettuja Modern POS Android -sovelluksessa. Lisätietoja on artikkelissa [POS Hybrid -sovelluksen määrittäminen Android- ja iOS-laitteissa](./dev-itpro/hybridapp.md).

### <a name="all-modern-pos-clients-that-have-a-committed-shared-iis-hardware-station"></a>Kaikki Modern POS -asiakasohjelmat, joilla on sidottu jaettu IIS-laiteasema

Tätä määritystä voidaan käyttää kaikissa Modern POS -asiakasohjelmissa, joilla on vain yhdessä myyntipisteen kassakoneessa käytössä oleva laiteasema. Voit tehdä nämä määritykset seuraavien vaiheiden avulla.

1.  Luo laiteprofiili, jossa kaikki vaaditut oheislaitteet on määritetty.
2.  Luo **Varattu**-tyyppinen laiteasema myymälälle, jossa myyntipisteen kassakonetta käytetään.
3.  Määritä varatulle laiteasemalle seuraavat ominaisuudet:
    -   **Isännän nimi** – Sen isäntäkoneen nimi, jolla laiteasema on käynnissä. 
    
        > [!NOTE]
        > Cloud POS määrittää paikallisen tietokoneen, jossa Cloud POS on käynnissä, käyttämällä **localhost**-komentoa. Cloud POS:n ja laiteaseman laiteparin muodostamisessa vaaditun varmenteen tietokoneen nimenä on oltava myös Localhost. Voit välttää ongelmat, kun listaat myymälän jokaisen varatun laiteaseman instanssin vaaditulla tavalla. Jokaisen laiteaseman isännän nimen on oltava sen tietokoneen nimi, jossa laiteasema on käytössä.
    
    -   **Portti** – Portti, jota laiteasema käyttää ollessaan yhteydessä Modern POS -asiakasohjelmaan.
    -   **Laiteprofiili** – Jos laiteprofiilia ei ole annettu laiteasemassa, käytetään kassakoneessa määritettyä laiteprofiilia.
    -   **EFT-myyntipisteen numero** – EFT-päätteen tunnus, jota käytetään EFT-varmennusten lähettämisen yhteydessä. Luottokortin käsittelijä toimittaa tämän tunnuksen.
    -   **Paketin nimi** – Laiteaseman paketti, jota käytetään laiteaseman käyttöönoton yhteydessä.

4.  Mene kohtaan **Retail ja Commerce \> Retail ja Commerce IT \> Jakeluaikataulu**.
5.  Valitse **1090**-jakeluaikataulu, kun haluat synkronoida uuden laiteprofiilin myymälän kanssa. Valitse **Suorita nyt**, kun haluat synkronoida muutokset myyntipisteen kanssa.
6.  Valitse **1040**-jakeluaikataulu, kun haluat synkronoida uuden laiteaseman myymälän kanssa. Valitse **Suorita nyt**, kun haluat synkronoida muutokset myyntipisteen kanssa.
7.  Asenna laiteasema. Lisätietoja laiteaseman asentamisesta on kohdassa [Retail Hardware Stationin määrittäminen ja asentaminen](retail-hardware-station-configuration-installation.md).
8.  Asenna ja aktivoi Modern POS. Lisätietoja Modern POS -sovelluksen asentamisesta on kohdassa [Retail Modern POS:n (MPOS) määrittäminen, asentaminen ja aktivoiminen](retail-modern-pos-device-activation.md).
9.  Kirjaudu Modern POS -sovellukseen ja valitse **Suorita muita kuin kassatoimintoja**.
10. Käynnistä **laiteasemien hallintatoiminto**.
11. Valitse **Hallinta**.
12. Määritä laiteaseman hallintasivulla laiteaseman käyttöönoton valinta päälle.
13. Valitse käytettävä laiteasema ja valitse sitten **Muodosta laitepari**.
14. Kun laiteasema on yhdistetty, valitse **Sulje**.
15. Valitse laiteaseman valintasivulla juuri valittu laiteasema ja aktivoi se.

### <a name="all-modern-pos-clients-that-have-a-shared-iis-hardware-station"></a>Kaikki Modern POS -asiakasohjelmat, joilla on jaettu IIS-laiteasema

Tätä määritystä voidaan käyttää kaikissa Modern POS -asiakasohjelmissa, jotka jakavat laiteasemia muiden laitteiden kanssa. Voit tehdä nämä määritykset seuraavien vaiheiden avulla.

1.  Luo laiteprofiili, jossa vaaditut oheislaitteet on määritetty.
2.  Luo **Jaettu**-tyyppinen laiteasema myymälälle, jossa myyntipisteen kassakonetta käytetään.
3.  Määritä jaetulle laiteasemalle seuraavat ominaisuudet:
    -   **Isännän nimi** – Sen isäntäkoneen nimi, jolla laiteasema on käynnissä.
    -   **Kuvaus** – Teksti, jonka avulla laiteasema tunnistetaan, kuten **Palautukset** tai **Myymälän edusta**.
    -   **Portti** – Portti, jota laiteasema käyttää ollessaan yhteydessä Modern POS -asiakasohjelmaan.
    -   **Laiteprofiili** – Jaetuissa laiteasemissa jokaisella laiteasemalla on oltava laiteprofiili. Laiteprofiilit voidaan jakaa laiteasemien kesken, mutta ne on yhdistettävä jokaiseen laiteasemaan. Lisäksi suositellaan jaettujen vuorojen käyttämistä, kun useat laitteet käyttävät samaa jaettua laiteasemaa. Voit määrittää jaetun vuoron valitsemalla **Vähittäismyynti ja kauppa \> Kanavan asetukset \> Myyntipisteen asetukset \> Myyntipisteen profiilit \> Laiteprofiilit**. Valitse jokaiselle jaetulle laiteprofiilille kassa ja määritä **Jaetun vuoron kassa** -valinnan arvoksi **Kyllä**.
    -   **EFT-myyntipisteen numero** – EFT-päätteen tunnus, jota käytetään EFT-varmennusten lähettämisen yhteydessä. Luottokortin käsittelijä toimittaa tämän tunnuksen.
    -   **Paketin nimi** – Laiteaseman paketti, jota käytetään laiteaseman käyttöönoton yhteydessä.

4.  Toista vaiheet 2 ja 3 jokaisen myymälässä tarvittavan laiteaseman kohdalla.
5.  Mene kohtaan **Retail ja Commerce \> Retail ja Commerce IT \> Jakeluaikataulu**.
6.  Valitse **1090**-jakeluaikataulu, kun haluat synkronoida uuden laiteprofiilin myymälän kanssa. Valitse **Suorita nyt**, kun haluat synkronoida muutokset myyntipisteen kanssa.
7.  Valitse **1040**-jakeluaikataulu, kun haluat synkronoida uuden laiteaseman myymälän kanssa. Valitse **Suorita nyt**, kun haluat synkronoida muutokset myyntipisteen kanssa.
8.  Asenna laiteasema jokaiselle vaiheissa 2 ja 3 määritetylle isäntäkoneelle. Lisätietoja laiteaseman asentamisesta on kohdassa [Retail Hardware Stationin määrittäminen ja asentaminen](retail-hardware-station-configuration-installation.md).
9.  Asenna ja aktivoi Modern POS. Lisätietoja Modern POS -sovelluksen asentamisesta on kohdassa [Retail Modern POS:n (MPOS) määrittäminen, asentaminen ja aktivoiminen](retail-modern-pos-device-activation.md).
10. Kirjaudu Modern POS -sovellukseen ja valitse **Suorita muita kuin kassatoimintoja**.
11. Käynnistä **laiteasemien hallintatoiminto**.

12. Valitse **Hallinta**.
13. Määritä laiteaseman hallintasivulla laiteaseman käyttöönoton valinta päälle.
14. Valitse käytettävä laiteasema ja valitse sitten **Muodosta laitepari**.
15. Toista vaihe 14 jokaiselle laiteasemalle, jota Modern POS käyttää.
16. Kun kaikkien tarvittujen laiteasemien kanssa on muodostettu laitepari, valitse **Sulje**.
17. Valitse laiteaseman valintasivulla juuri valittu laiteasema ja aktivoi se. 

> [!NOTE]
> Jos laitteet käyttävät usein eri laiteasemia, suosittelemme, että Modern POS määritetään pyytämään kassanhoitajia määrittämään laiteaseman maksuvälineprosessin alussa. Siirry kohtaan **Vähittäismyynti ja kauppa \> Kanavan asetukset \> POS-asetukset \> Kassakoneet**. Valitse kassakone ja määritä **Valitse maksuvälinetapahtuman aikana** -valinnan arvoksi **Kyllä**. Käytä **1090**-jakeluaikataulua, kun synkronoit muutokset kanavatietokannan kanssa.

## <a name="extensibility"></a>Laajennettavuus
Tietoja laiteaseman laajennettavuusskenaarioista on kohdassa [Integroi myyntipiste uuden laitteen kanssa ja muodosta laajennuksen asennusohjelma](dev-itpro/hardware-device-extension.md).

## <a name="security"></a>Suojaus
Nykyisten suojausstandardien mukaan tuotantoympäristössä tulisi käyttää seuraavia asetuksia: 

### <a name="hardware-station-installer"></a>Laiteaseman asennusohjelma
Laiteaseman asennusohjelma tekee nämä rekisterimuutokset automaattisesti itsepalvelun kautta tehtävän asennuksen osana.

-   Secure Sockets Layer (SSL) on poistettava käytöstä.
-   Vain Transport Layer Security (TLS) -versio 1.2 (tai uudempi versio) voi olla käytössä. 

### <a name="ssl-and-tls"></a>SSL ja TLS
Oletusarvoisesti SSL ja kaikki TLS-versiot TLS 1.2 -versiota lukuun ottamatta on poistettu käytöstä. Voit muokata näitä arvoja seuraavien vaiheiden avulla:
    1.  Paina Windows-näppäintä +R-kirjainta, kun haluat avata **Suorita**-ikkunan.
    2.  Kirjoita **Avaa**-kenttään **Regedit** ja valitse **OK**.
    3.  Jos **käyttäjätilien valvontasanoman** ruutu avautuu, valitse **Kyllä**.
    4.  Siirry **Rekisterieditori**-ikkunassa kohtaan **HKEY\_LOCAL\_MACHINESystemCurrentControlSetSecurityProvidersSCHANNELProtocols**. Seuraavat avaimet on lisätty automaattisesti, jolloin vain TLS 1.2 voi olla käytössä:
        -   TLS 1.2Server:Enabled=1
        -   TLS 1.2Server:DisabledByDefault=0
        -   TLS 1.2Client:Enabled=1
        -   TLS 1.2Client:DisabledByDefault=0
        -   TLS 1.1Server:Enabled=0
        -   TLS 1.1Client:Enabled=0
        -   TLS 1.0Server:Enabled=0
        -   TLS 1.0Client:Enabled=0
        -   SSL 3.0Server:Enabled=0
        -   SSL 3.0Client:Enabled=0
        -   SSL 2.0Server:Enabled=0
        -   SSL 2.0Client:Enabled=0
-   Muut verkkoportit eivät voi olla auki, ellei niitä tarvita jonkin tunnetun ja määritetyn syyn vuoksi.
-   Eri alkuperiä sisältävien resurssien jakaminen on poistettava käytöstä ja hyväksyttävät sallitut alkuperät on määritettävä.
-   Tietokoneissa, joissa on käytössä laiteasema, tulee käyttää vain luotetun varmenteen myöntäjien varmenteita.

> [!NOTE]
> IIS:n ja maksukorttiyhdistysten vaatimusten suojausohjeiden tarkistaminen on erittäin tärkeää.

## <a name="peripheral-simulator"></a>Oheislaitesimulaattori
Lisätietoja on kohdassa [Commercen oheislaitesimulaattori](dev-itpro/retail-peripheral-simulator.md).

## <a name="microsoft-tested-peripheral-devices"></a>Microsoftin testaamat oheislaitteet
### <a name="ipc-built-in-hardware-station"></a>IPC-laiteasema (sisäänrakennettu)

Seuraavat oheislaitteet on testattu käyttämällä Modern POS Windowsille -sovellukselle muodostettua IPC-laiteasemaa.

#### <a name="printer"></a>Tulostin

| Valmistaja | Malli    | Käyttöliittymä | Kommentit                |
| ------------ | -------- | --------- | ----------------------- |
| Epson        | TM-T88V  | OPOS      |                         |
| Epson        | TM-T88IV | OPOS      |                         |
| HP           | H300     | OPOS      | Powered USB             |
| Star         | TSP650II | Mukautettu    | Yhdistetty verkon välityksellä   |
| Star         | mPOP     | OPOS      | Yhdistetty Bluetoothilla |
| Toshiba      | HSP100   | OPOS      |                         |
| Toshiba      | HSP150   | OPOS      |                         |

> [!NOTE]
> Star TSP 100 -tulostinta ei tueta sisäänrakennetussa laiteasemassa. Sisäänrakennettu laiteasema käyttää 64-bittistä prosessia, joka ei ole yhteensopiva aiemmin luotujen TP 100 -ohjainten kanssa. 

#### <a name="bar-code-scanner"></a>Viivakoodin lukulaite

| Valmistaja  | Malli         | Käyttöliittymä | Kommentit |
| ------------- | ------------- | --------- | -------- |
| Datalogic     | Magellan 8400 | OPOS      |          |
| Honeywell     | 1900          | UWP       |          |
| HP-integroitu | E1L07AA       | OPOS      |          |
| Symboli        | LS2208        | OPOS      |          |

#### <a name="payment-terminals-and-pin-pads"></a>Maksupäätteet ja PIN-näppäimistöt

Dynamics 365 Commerce tarjoaa käyttövalmiin ratkaisun maksupalveluiden Adyen-integrointiin. [Dynamics 365 Payment Connector for Adyen](dev-itpro/adyen-connector.md) -yhdistin käyttää laiteriippumatonta [Adyen-maksupäätteen ohjelmointirajapintaa](https://www.adyen.com/blog/introducing-the-terminal-api) ja se voi olla vuorovaikutuksessa kaikkien tämän ohjelmointirajapinnan tukemien maksupäätteiden kanssa. Kattava luettelo tuetuista maksupäätteistä on kohdassa [Adyen POS -päätteet](https://www.adyen.com/pos-payments/terminals).

Voit myös käyttää muita maksutoimittajia Dynamics 365 Commercen kanssa luomalla mukautetun liittimen. Mitä tahansa maksupäätettä, jota maksupalvelu tukee, voidaan käyttää Dynamics 365 Commercen kanssa. Vastaavasti Dynamics 365 Commerce mahdollistaa minkä tahansa maksulaitteen integrointimallin, jota maksupalvelu tukee, esimerkiksi paikallisen IP-osoitteen, pilvipalveluliittymän tai suoran yhteyden (esimerkiksi USB:n kautta) myyntipisteeseen. Lisätietoja: [Kattavan maksun integroinnin luominen maksupäätteelle](dev-itpro/end-to-end-payment-extension.md).

#### <a name="cash-drawer"></a>Kassa

| Valmistaja | Malli     | Käyttöliittymä | Kommentit                |
|--------------|-----------|-----------|-------------------------|
| Star         | mPOP      | OPOS      | Yhdistetty Bluetoothilla |
| APG          | Atwood    | Mukautettu    | Yhdistetty verkon välityksellä   |
| Star         | SMD2-1317 | OPOS      |                         |
| HP           | QT457AA   | OPOS      |                         |
| Epson        |           | Mukautettu    | Kytketty verkko-Epson-tulostimeen DK-portin kautta |

#### <a name="line-display"></a>Rivinäyttö

| Valmistaja | Malli    | Käyttöliittymä | Kommentit |
| ------------ | -------- | --------- | -------- |
| Epson        | DM-D110  | OPOS      |          |
| HP           | T-sarja | OPOS      |          |

#### <a name="signature-capture"></a>Allekirjoituksen tarkistus

| Valmistaja | Malli  | Käyttöliittymä | Kommentit |
|--------------|--------|-----------|----------|
| Scriptel     | ST1550 | OPOS      |          |

#### <a name="scale"></a>Mittakaava

| Valmistaja | Malli         | Käyttöliittymä | Huomautukset |
|--------------|---------------|-----------|----------|
| Datalogic    | Magellan 8400 | OPOS      |          |

#### <a name="msr"></a>Magneettinauhan lukulaite

| Valmistaja | Malli       | Käyttöliittymä | Huomautukset |
|--------------|-------------|-----------|----------|
| Magtek       | 21073075    | UWP       |          |
| Magtek       | 21073062    | OPOS      |          |
| HP           | IDRA-334133 | OPOS      |          |

### <a name="dedicated-iis-hardware-station"></a>Varattu IIS-laiteasema

Seuraavat oheislaitteet on testattu käyttämällä varattua (ei jaettua) IIS-laiteasemaa sekä Modern POS Windowsille- ja Cloud POS -sovellusta.

#### <a name="printer"></a>Tulostin

| Valmistaja | Malli    | Käyttöliittymä | Kommentit                |
| ------------ | -------- | --------- | ----------------------- |
| Epson        | TM-T88V  | OPOS      |                         |
| Epson        | TM-T88IV | OPOS      |                         |
| HP           | H300     | OPOS      | Powered USB             |
| Star         | TSP650II | Mukautettu    | Yhdistetty verkon välityksellä   |
| Star         | mPOP     | OPOS      | Yhdistetty Bluetoothilla |
| Toshiba      | HSP100   | OPOS      |                         |
| Toshiba      | HSP150   | OPOS      |                         |

#### <a name="bar-code-scanner"></a>Viivakoodin lukulaite

| Valmistaja  | Malli         | Käyttöliittymä | Kommentit |
| ------------- | ------------- | --------- | -------- |
| Datalogic     | Magellan 8400 | OPOS      |          |
| HP-integroitu | E1L07AA       | OPOS      |          |
| Symboli        | LS2208        | OPOS      |          |

#### <a name="payment-terminals-and-pin-pads"></a>Maksupäätteet ja PIN-näppäimistöt

Dynamics 365 Commerce tarjoaa käyttövalmiin ratkaisun maksupalveluiden Adyen-integrointiin. [Dynamics 365 Payment Connector for Adyen](dev-itpro/adyen-connector.md) -yhdistin käyttää laiteriippumatonta [Adyen-maksupäätteen ohjelmointirajapintaa](https://www.adyen.com/blog/introducing-the-terminal-api) ja se voi olla vuorovaikutuksessa kaikkien tämän ohjelmointirajapinnan tukemien maksupäätteiden kanssa. Kattava luettelo tuetuista maksupäätteistä on kohdassa [Adyen POS -päätteet](https://www.adyen.com/pos-payments/terminals).

Voit myös käyttää muita maksutoimittajia Dynamics 365 Commercen kanssa luomalla mukautetun liittimen. Mitä tahansa maksupäätettä, jota maksupalvelu tukee, voidaan käyttää Dynamics 365 Commercen kanssa. Vastaavasti Dynamics 365 Commerce mahdollistaa minkä tahansa maksulaitteen integrointimallin, jota maksupalvelu tukee, esimerkiksi paikallisen IP-osoitteen, pilvipalveluliittymän tai suoran yhteyden (esimerkiksi USB:n kautta) myyntipisteeseen. Lisätietoja: [Kattavan maksun integroinnin luominen maksupäätteelle](dev-itpro/end-to-end-payment-extension.md).

#### <a name="cash-drawer"></a>Kassa

| Valmistaja | Malli     | Käyttöliittymä | Kommentit              |
|--------------|-----------|-----------|-----------------------|
| APG          | Atwood    | Mukautettu    | Yhdistetty verkon välityksellä |
| Star         | SMD2-1317 | OPOS      |                       |
| HP           | QT457AA   | OPOS      |                       |
| Epson        |           | Mukautettu    | Kytketty verkko-Epson-tulostimeen DK-portin kautta |

#### <a name="line-display"></a>Rivinäyttö

| Valmistaja  | Malli   | Käyttöliittymä | Huomautukset |
|---------------|---------|-----------|----------|
| HP-integroitu | G6U79AA | OPOS      |          |
| Epson         | M58DC   | OPOS      |          |

#### <a name="signature-capture"></a>Allekirjoituksen tarkistus

| Valmistaja | Malli  | Käyttöliittymä | Huomautukset |
|--------------|--------|-----------|----------|
| Scriptel     | ST1550 | OPOS      |          |

#### <a name="scale"></a>Mittakaava

| Valmistaja | Malli         | Käyttöliittymä | Huomautukset |
|--------------|---------------|-----------|----------|
| Datalogic    | Magellan 8400 | OPOS      |          |

#### <a name="msr"></a>Magneettinauhan lukulaite

| Valmistaja | Malli       | Käyttöliittymä | Huomautukset |
|--------------|-------------|-----------|----------|
| Magtek       | 21073075    | UWP       |          |
| Magtek       | 21073062    | OPOS      |          |
| HP           | IDRA-334133 | OPOS      |          |

### <a name="shared-iis-hardware-station"></a>Jaettu IIS-laiteasema

Seuraavat oheislaitteet on testattu käyttämällä jaettua IIS-laiteasemaa sekä Modern POS Windowsille- ja Cloud POS -sovellusta. 

> [!NOTE]
> Vain tulostinta, maksupäätettä ja kassaa tuetaan.

#### <a name="printer"></a>Tulostin

| Valmistaja | Malli    | Käyttöliittymä | Kommentit                |
| ------------ | -------- | --------- | ----------------------- |
| Epson        | TM-T88V  | OPOS      |                         |
| Epson        | TM-T88IV | OPOS      |                         |
| HP           | H300     | OPOS      | Powered USB             |
| Star         | mPOP     | OPOS      | Yhdistetty Bluetoothilla |
| Toshiba      | HSP100   | OPOS      |                         |
| Toshiba      | HSP150   | OPOS      |                         |

#### <a name="payment-terminal"></a>Maksupääte

Dynamics 365 Commerce tarjoaa käyttövalmiin ratkaisun maksupalveluiden Adyen-integrointiin. [Dynamics 365 Payment Connector for Adyen](dev-itpro/adyen-connector.md) -yhdistin käyttää laiteriippumatonta [Adyen-maksupäätteen ohjelmointirajapintaa](https://www.adyen.com/blog/introducing-the-terminal-api) ja se voi olla vuorovaikutuksessa kaikkien tämän ohjelmointirajapinnan tukemien maksupäätteiden kanssa. Kattava luettelo tuetuista maksupäätteistä on kohdassa [Adyen POS -päätteet](https://www.adyen.com/pos-payments/terminals).

Voit myös käyttää muita maksutoimittajia Dynamics 365 Commercen kanssa luomalla mukautetun liittimen. Mitä tahansa maksupäätettä, jota maksupalvelu tukee, voidaan käyttää Dynamics 365 Commercen kanssa. Vastaavasti Dynamics 365 Commerce mahdollistaa minkä tahansa maksulaitteen integrointimallin, jota maksupalvelu tukee, esimerkiksi paikallisen IP-osoitteen, pilvipalveluliittymän tai suoran yhteyden (esimerkiksi USB:n kautta) myyntipisteeseen. Lisätietoja: [Kattavan maksun integroinnin luominen maksupäätteelle](dev-itpro/end-to-end-payment-extension.md).

#### <a name="cash-drawer"></a>Kassa

| Valmistaja | Malli     | Käyttöliittymä | Kommentit              |
|--------------|-----------|-----------|-----------------------|
| APG          | Atwood    | Mukautettu    | Yhdistetty verkon välityksellä |
| Star         | SMD2-1317 | OPOS      |                       |
| HP           | QT457AA   | OPOS      |                       |
| Epson        |           | Mukautettu    | Kytketty verkko-Epson-tulostimeen DK-portin kautta |


## <a name="troubleshooting"></a>Vianmääritys
### <a name="modern-pos-can-detect-the-hardware-station-in-its-list-for-selection-but-it-cant-complete-the-pairing"></a>Moderni POS voi tunnistaa valintaluettelon laiteaseman, mutta laiteparin muodostaminen ei onnistu

**Ratkaisu:** Tarkista seuraava mahdollisten virhekohtien luettelo:

-   Tietokone, jolla Modern POS on käytössä, luottaa varmenteeseen, joka on käytössä laiteaseman tietokoneessa.
    -   Voit varmistaa nämä asetukset siirtymällä verkkoselaimessa URL-osoitteeseen https://&lt;Computer Name&gt;&lt;Port Number&gt;/HardwareStation/ping.
    -   URL-osoite varmistaa testauksen avulla, että tietokone on käytettävissä. Selain osoittaa, onko varmenne luotettava. (Esimerkiksi Internet Explorerissa lukitussymboli näkyy osoiterivillä. Kun valitse tämän symbolin, Internet Explorer tarkistaa, voiko varmenteeseen luottaa. Voit asentaa varmenteen paikalliselle tietokoneelle tarkistamalla näytettävän varmenteen tiedot.)
-   Laiteaseman tietokoneen laiteaseman käyttämä portti avataan palomuurissa.
-   Laiteasema on asentanut oikein kauppiastilin tiedot kauppatietojen asennustyökalun avulla. Se suoritetaan laiteaseman asennusohjelman lopussa.

### <a name="modern-pos-cant-detect-the-hardware-station-in-its-list-for-selection"></a>Moderni POS ei pysty tunnistamaan laiteasemaa valintaluettelosta

**Ratkaisu:** Virheen voi aiheuttaa jokin seuraavista seikoista:

-   Laiteasemaa ei ole asennettu oikein Headquartersissa. Lisätietoja on kohdassa [Retail Hardware Stationin määrittäminen ja asentaminen](retail-hardware-station-configuration-installation.md#troubleshooting). 
-   Töitä ei ole suoritettu kanavan määrityksen päivittämistä varten. Tässä tapauksessa tulee suorittaa 1070-työ kanavan määritystä varten.

### <a name="modern-pos-doesnt-reflect-new-cash-drawer-settings"></a>Moderni POS ei näytä uuden kassan asetuksia

**Ratkaisu:** Sulje nykyinen erä. Kassan muutokset päivitetään Modern POS -sovellukseen vasta nykyisen erän sulkemisen jälkeen.

### <a name="modern-pos-is-reporting-an-issue-with-a-peripheral"></a>Moderni POS ilmoittaa ongelmasta oheislaitteen kanssa

**Ratkaisu:** Seuraavassa esitellään joitakin yleisiä syitä:

-   Varmista, että muun laitteen ohjaimen määritysapuohjelmat on suljettu. Jos näitä apuohjelmia on auki, ne voivat estää laitteen käyttämisen Modern POS -sovellukselta tai laiteasemalta.
-   Jos oheislaite on jaettu useiden myyntipisteiden laitteiden kanssa, varmista, että se kuuluu johonkin seuraavista luokista:
    -   Kassa
    -   Kuittitulostin
    -   Maksupääte

    Jos oheislaite ei kuulu mihinkään näistä luokista, laiteasemaa ei ole suunniteltu oheislaitteiden jakamiseen useiden myyntipisteiden laitteiden kanssa.
-   Joskus laiteohjaimet voivat aiheuttaa virheitä yhteisten ohjausobjektien toimintaan. Jos laite on asennettu äskettäin, mutta se ei toimi oikein tai huomaat muita ongelmia, ongelma voidaan usein ratkaisua asentamalla ohjausobjekti uudelleen. Voit ladata yhteiset ohjausobjektit osoitteesta <http://monroecs.com/oposccos_current.htm>.
-   Jos oheislaitteita muutetaan usein testaamisen tai virheenetsinnän aikana, sinun on ehkä palautettava IIS:n asetukset tai odotettava välimuistin päivittymistä. Voit palauttaa IIS:n asetukset seuraavien vaiheiden avulla:
    1.  Valitse **Käynnistä**-valikko ja kirjoita **CMD**.
    2.  Napsauta **komentokehotetta** hiiren kakkospainikkeella ja valitse sitten **Suorita järjestelmänvalvojana**.
    3.  Kirjoita **komentokehoteikkunaan** **iisreset/Restart** ja paina sitten Enter-näppäintä.
    4.  Kun IIS on käynnistetty uudelleen, käynnistä uudelleen Moderni POS.
-   Kun oheislaitteisiin tehdään usein muutoksia ja myös käynnistät ja lopetat myyntipisteen asiakasohjelman usein, edellisen myyntipisteen istunnon dllhost-prosessi voi häiritä kuluvaa istuntoa. Tässä tapauksessa laitetta ei ehkä voi käyttää, ennen kuin suljet edellistä istuntoa hallinneen dynaamisen linkkikirjaston (DLL) isännän. Sulje DLL-isäntä seuraavien vaiheiden avulla:
    1.  Valitse **Käynnistä**-valikko ja kirjoita **Tehtävienhallinta**.
    2.  Valitse hakutuloksista **Tehtävienhallinta**.
    3.  Valitse tehtävienhallinnan **Tiedot**-välilehdessä sarake, jonka otsikko on **Nimi**, jolloin taulu järjestetään aakkosjärjestykseen nimen mukaan.
    4.  Vieritä alas, kunnes dllhost.exe löytyy.
    5.  Valitse jokainen DLL-isäntä ja valitse sitten **Lopeta tehtävä**.
    6.  Kun DLL-isännät on suljettu, käynnistä Modern POS uudelleen.


## <a name="additional-resources"></a>Lisäresurssit

[Commercen oheislaitesimulaattori](dev-itpro/retail-peripheral-simulator.md)




[!INCLUDE[footer-include](../includes/footer-banner.md)]
