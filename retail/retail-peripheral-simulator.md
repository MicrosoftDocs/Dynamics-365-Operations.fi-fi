---
title: "Vähittäismyynnin oheislaitesimulaattori"
description: "Tässä aiheessa käsitellään Microsoft Dynamics 365 for Operations - Retailin mukana toimitettavaa oheislaitesimulaattorityökalua."
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core, Retail
ms.custom: 266544
ms.assetid: 16f31e70-15fc-441e-9727-e6a31c3a48f5
ms.search.region: global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 894aaaaa844447030dae73826d326f99366aa068
ms.contentlocale: fi-fi
ms.lasthandoff: 05/25/2017


---

# <a name="retail-peripheral-simulator"></a>Vähittäismyynnin oheislaitesimulaattori

[!include[banner](includes/banner.md)]


Tässä aiheessa käsitellään Microsoft Dynamics 365 for Operations - Retailin mukana toimitettavaa oheislaitesimulaattorityökalua.

<a name="overview"></a>Yleiskuvaus
--------

Microsoft Dynamics 365 for Operations - Retailin oheislaitesimulaattori on työkalu, joka auttaa vähittäismyyntiympäristössä käytettävissä olevien oheislaitteiden määrittämisessä, testaamisessa ja vianmäärityksessä. Oheislaitesimulaattoria voi käyttää vähittäismyynnin oheislaitteiden testaamisen yksinkertaistamisessa ja virheellisten määritysten tai väärin toimivien laiteohjainten aiheuttamien ongelmien löytämisessä. Oheislaitesimulaattori sisältää työpöytäohjelman, joka sisältää Dynamics 365 for Operations - Retailin tukemien laitteiden virtuaaliversiot. Kunkin virtuaalilaitteen osassa näkyy laitteen ja myyntipisteen välinen vuorovaikutus. Sen avulla voi myös antaa eri myyntipisteskenaarioissa sallittun syötteen. Oheislaitesimulaattori tukee myyntipisteen ja seuraavien virtuaalilaitteiden välistä vuorovaikutusta:

-   **Tulostin** – Oheislaitesimulaattori voi näyttää myyntipisteen tulostimelle määritetyt kuitit.
-   **Rivinäyttö** – Voit määrittää virtuaalisen rivinäytön niin, että se näyttää fyysisen rivinäytön aktiviteetin.
-   **Magneettinauhan lukulaite (MSR)** – Voit lähettää oheislaitesimulaattorista simuloituja magneettinauhatapahtumia myyntipisteelle.
-   **Kassa** – Voit simuloida fyysisen kassan.
-   **Kassa 2** – Jos oheislaitesimulaattoriin määritetään toinen kassa, voit simuloida skenaarion, jossa on yksi myyntipisteen kassakone ja kaksi aktiivista vuoroa.
-   **Skanneri** – Viivakoodin virtuaalinen lukulaite, jota oheislaitesimulaattori tukee, voi käynnistää viivakoodin lukutapahtumia.
-   **Vaaka** – Virtuaalivaa'an avulla voit simuloida punnittujen nimikkeiden ja myyntipisteen välistä vuorovaikutusta.
-   **Henkilökohtainen tunnistenumero (PIN) -näppäimistö** – Voit simuloida PIN-näppäimistötoimintoja. **Huomautus:** Fyysisen PIN-näppäimistön tuki on otettava käyttöön maksuyhdistimen kautta.
-   **Allekirjoituksen tarkistus** – Oheislaitesimulaattori sisältää virtuaalisen allekirjoituksen tarkistuslaitteen, jonka voi määrittää pyytämään allekirjoituksia. Jotkin maksuvälineet, kuten asiakasmaksutilit, vaativat allekirjoituksia.

Oheislaitesimulaattorin avulla voit simuloida viivakoodin lukulaitteen ja magneettinauhan lukulaitteen käynnistämiä näppäimistön kortinlukijatapahtumia. Virtuaalinen oheislaitesimulaattori tukee erityisesti Retail POS (OPOS) -laitteiden objektien linkittämistä ja upottamista.

## <a name="key-scenarios"></a>Tärkeimmät skenaariot
### <a name="troubleshooting"></a>Vianmääritys

Voit käyttää oheislaitesimulaattoria laitteen asetusten vianmäärityksessä. Jos sinulla ei ole oheislaitesimulaattoria tai toista saman luokan laitetta, ongelman alkuperän selvittäminen voi olla vaikeaa. Kun käytössäsi on oheislaitesimulaattori, voit määrittää virtuaalilaitteita ja suorittaa fyysisissä laitteissa käytössä olevat koodipolut ja liiketoimintalogiikan. Tärkein ero virtuaalilaitteiden ja fyysisten laitteiden välillä oheislaitesimulaattorin näkökulmasta on palveluobjekti tai laiteohjain. Laitteen valmistaja tarjoaa fyysisten laitteiden palveluobjektin. Sitä vastoin oheislaitesimulaattorin palveluobjektit ovat osa oheislaitesimulaattoria. Kun oheislaitesimulaattori toimii oikein, mutta laite ei toimi oikein sen jälkeen, kun laiteprofiilissa olevaksi laitteen nimeksi on muutettu todellinen laite, voit olettaa, että ongelma on valmistajan toimittamassa palveluobjektissa.

### <a name="training"></a>Koulutus

Voit lisätä oheislaitesimulaattorin avulla realistisen tason kassanhoitajakoulutukseen, kun fyysisiä laiteasetuksia ei ole saatavana. Kun oheislaitesimulaattori sisältyy koulutusskenaarioihin, kassanhoitaja voi olla tehokkaammin käyttää myyntipäätettä syöttämällä tietoja, kuten tuotteen viivakoodin lukuja ja lahjakorttien lukuja ja seuraamalla, mitkä tietyn tapahtuman kuitit tulostetaan.

### <a name="testing"></a>Testaus

Voit käyttää oheislaitesimulaattoria tuotteen viivakoodien, kuittimuotojen jne. testaamiseen ilman fyysisen laitteen käyttöönottamista virtuaaliympäristössä. Koska fyysinen laite ei ole pakollinen eikä myyntipisteen asiakasohjelmaa tarvitse ottaa käyttöön laiteasemassa tai fyysisessä tietokoneessa, taustatietokannassa tehdyt muutokset voidaan testata nopeammin.

## <a name="set-up-the-peripheral-simulator"></a>Oheislaitesimulaattorin määrittäminen
### <a name="set-up-a-hardware-profile"></a>Laiteprofiilin määrittäminen

1.  Voit määrittää oheislaitesimulaattorin siirtymällä kohtaan **Vähittäismyynti ja kauppa** &gt; **Kanavan asetukset** &gt; **Myyntipisteen asetukset** &gt; **Myyntipisteen profiilit** &gt; **Laiteprofiilit**.
2.  Voit luoda uuden profiilin valitsemalla **Uusi**.
3.  Anna arvot **Profiilinumero**- ja **Kuvaus**-kenttään.
4.  Määritä testattavat virtuaalilaitteet seuraavan taulukon avulla. Alla on kuvaus taulukon sarakkeista:
    -   **Laite** – Tämä sarake määrittää sen pikavälilehden nimen, joka laajennetaan laitteen nimen määrittämisen yhteydessä.
    -   **Laitetyyppi** – Tämä sarake määrittää sen kentän arvon, jonka nimeksi annetaan laitteen nimi.
    -   **Laitteen nimi** – Tämä sarake määrittää laitteen nimelle annettavan täsmällisen arvon. **Tärkeää:** Tässä annettavat laitteiden nimet vaaditaan, koska laiteasema viittaa laitteisiin näiden nimien avulla. Jos et käytä näitä määritettyjä nimiä, laite ei ole käytettävissä.

    | Laite            | Laitetyyppi | Laitteen nimi              |
    |-------------------|-------------|--------------------------|
    | Tulostin           | OPOS        | MockOPOSPrinter          |
    | Rivinäyttö      | OPOS        | MockOPOSLineDisplay      |
    | Magneettinauhan lukulaite               | OPOS        | MockOPOSMSR              |
    | Asettaja            | OPOS        | MockOPOSDrawer1          |
    | Drawer2           | OPOS        | MockOPOSDrawers          |
    | Skanneri           | OPOS        | MockOPOSScanner          |
    | Mittakaava             | OPOS        | MockOPOSScale            |
    | PIN-näppäimistö           | OPOS        | MockOPOSPinPad           |
    | Allekirjoituksen tarkistus | OPOS        | MockOPOSSignatureCapture |

**Huomautus:** Laiteprofiilissa ei tarvita tiettyjä asetuksia, kun näppäimistön kortinlukijatapahtumat simuloidaan viivakoodin lukulaitteesta ja magneettinauhasta.

### <a name="assign-the-hardware-profile-to-a-register"></a>Laiteprofiilin määrittäminen kassakoneeseen

1.  Siirry laiteprofiilin luomisen jälkeen kohtaan **Vähittäismyynti ja kauppa** &gt; **Kanavan asetukset** &gt; **Myyntipisteen asetukset** &gt; **Kassakoneet**.
2.  Valitse **Kassakoneet**-luettelosta sen kassan **Kassakoneen numero** -kentän linkki, joka käyttää oheislaitesimulaattoria.
3.  Valitse **Muokkaa**.
4.  Valitse **Profiilit**-osan **Laiteprofiili**-kentässä se laiteprofiili, jolle virtuaaliset oheislaitteet luotiin.
5.  Valitse **Tallenna**.

### <a name="synchronize-changes-to-the-channel-database"></a>Muutosten synkronoiminen kanavatietokantaan

1.  Siirry kohtaan **Vähittäismyynti ja kauppa** &gt; **Vähittäismyynnin IT** &gt; **Jakeluaikataulu**.
2.  Valitse **1090**-jakeluaikataulu.
3.  Valitse **Suorita nyt**, kun haluat synkronoida muutokset myyntipisteen kanssa.

Kun tiedot on synkronoitu, uusi laiteprofiili ja kassakoneen muutokset ovat käytettävissä kanavatietokannassa.

## <a name="install-the-peripheral-simulator"></a>Oheislaitesimulaattorin asentaminen
1.  Siirry kohtaan **Vähittäismyynti ja kauppa** &gt; **Kanavan asetukset** &gt; **Myyntipisteen asetukset** &gt; **Myyntipisteen profiilit** &gt; **Laiteprofiilit**.
2.  Valitse **Lataa** ja valitse sitten **PeripheralSimulator**. **Huomautus:** Ponnahdusikkunoiden esto-ohjelmat on poistettava käytöstä, ennen kuin oheislaitesimulaattori ladataan.
3.  Kun lataus on valmis, avaa **Ladatut tiedostot** -kansio ja käynnistä asennusohjelma kaksoisnapsauttamalla **VirtualPeripherals.msi**-tiedostoa.
4.  Asenna oheislaitesimulaattori käyttämällä oletusasetuksia.

Asenna oheislaitesimulaattorin lisäksi yhteiset ohjausobjektit, jotka Monroe Consulting Services tarjoaa. Muussa tapauksessa oheislaitesimulaattori ei toimi oikein. Voit ladata yhteiset ohjausobjektit siirtymällä osoitteeseen <http://monroecs.com/oposccos_current.htm>.

## <a name="using-the-peripheral-simulator"></a>Oheislaitesimulaattorin käyttäminen
Aloita oheislaitesimulaattorin käyttäminen valitsemalla tietokoneessa **Käynnistä** ja kirjoittamalla **Vähittäismyynnin oheislaitesimulaattori (Retail peripheral simulator)**. Valitse sitten hakutuloksissa näkyvä sovellus. Kun olet käynnistänyt oheislaitesimulaattorin, voit tarkastella tuettuja laitteita valitsemalla laitteen nimen. Nämä laitteet näkyvät ikkunan vasemmalla puolella olevissa välilehdissä. Voit tarkastella tiettyä laitetta, kun valitse laitteen välilehden.

### <a name="line-display-capabilities"></a>Rivinäytön ominaisuudet

Rivinäyttö on ensimmäinen oheislaitesimulaattorin luettelossa oleva laite. Kun virtuaalinen rivinäyttö on määritetty, se näyttää rivinimikkeet sellaisina, kuin ne on luettu myyntipisteen tapahtumassa. Rivinimikkeiden lisäksi näyttö esittää maksuvälineen valinnan aikaisen kokonaissumman myyntipisteessä. Se näyttää myös maksettavan saldon, jos maksuväline on annettu, mutta tapahtuman saldo on yhä maksamatta. Kun myyntipistettä ei käytetä, voidaan näyttää kassan sulkemisen osoittava sanoma. Sanoma on määritettävä laiteprofiilin **Rivinäyttö**-pikavälilehdessä.

### <a name="cash-drawer-capabilities"></a>Kassan ominaisuudet

Kassa on toinen oheislaitesimulaattorin luettelossa oleva laite. Kun laiteprofiili määritetään käyttämään virtuaalisia kassoja, myyntipiste avaa aktiivisen vuoron kassan kassatoiminnon, kuten maksuvälineittäin tehtyjen laskemistapahtumien, suorittamisen yhteydessä. Näin kassanhoitaja voi tehdä muutoksen tai tallettaa käteistä normaalien itsepalvelutukkutapahtumien yhteydessä. Virtuaalisten kassojen nimet ovat **Pääkassa** ja **Toissijainen kassa**. Nimet laiteprofiilissa ovat vastaavasti Kassa ja Kassa 2. Kun kassa on suljettu, näkyvissä on suljetun kassan kuva ja suljetun kassan painikkeen nimi on **Avaa kassa**. Jos valitse tämän painikkeen, kuvaksi tulee avoimen kassan kuva. Avoimen kassan painikkeen nimi on **Sulje kassa**. Useat myyntipisteen toiminnot voivat avata kassan. Useimpia toimintoja ei voi jatkaa, kun kassa on auki. Poikkeuksia ovat jotkin päivän päättyessä tehtävät toiminnot. Jos myyntipisteen käyttäjä saa virhesanoman, jossa kerrotaan, että toimintoa ei voi suorittaa kassan ollessa auki, käyttäjän on suljettava virtuaalinen tai fyysinen kassa. Toimintoa voi jatkaa vasta tämän jälkeen. Jos kassa on merkitty laiteprofiilissa **jaetuksi**, järjestelmä ei vahvista ennen toimintoa, että kassa on suljettu. Toiminto jatkuu normaaliin tapaan, vaikka kassa olisi auki. Tämä toiminto tukee skenaarioita, joissa kassat on jaettu useiden myyjien kesken ja yksi myyjä käyttää kassaa toisen suorittaessa omalla myyntipisteen laitteellaan muita tehtäviä. Kassaan tehtävät muutokset ovat näkyvissä vasta sitten, kun kuluva vuoro suljetaan ja uusi vuoro avataan.

### <a name="msr-capabilities"></a>Magneettinauhan lukulaitteen ominaisuudet

Oheislaitesimulaattori tarjoaa luotettavan tuen virtuaalisille magneettinauhan lukulaitetoiminnoille toimimalla joko OPOS-tilassa tai näppäimistön kortinlukijatilassa. OPOS-tila edellyttää, että magneettinauhan lukulaite on määritettävä laiteprofiilissa. Näin se voi toimia OPOS-laitteena. Näppäimistön kortinlukijatila lähettää näppäimistön kortinlukijan tietotapahtumat Microsoft Windowsille. Asetusten erojen lisäksi OPOS-tila ja näppäimistön kortinlukijatila eroavat toisistaan seuraavasti:

-   Myyntipisteen asiakasohjelma käyttää OPOS:n magneettinauhan lukulaitteita tietyissä skenaarioissa, kuten magneettinauhan tiedoissa kanta-asiakas- tai lahjakortin merkinnässä.
-   Näppäimistön kortinlukijatilassa oheislaitesimulaattori lähettää näppäimistön kortinlukijan tiedot kenttään, joka on aktiivinen tietojen lähettämisen aikana. Tämä toiminto muistuttaa toimintoa, joka tapahtuu syötettäessä tiedot näppäimistön avulla. Magneettinauhan lukulaitetta voidaan käyttää näppäimistön kortinlukijana, jos käyttäjä alkaa käyttää Retail Modern POS (MPOS) -sovellusta ja varmistaa, että tiedot vastaanotetaan oikeaan kenttään. Tämän vuoksi kannattaa määrittää viive, jolloin käyttäjä ehtii varmistaa, että tiedot lähetetään oikeaan kenttään.

#### <a name="testing-gift-and-payment-card-swipes"></a>Lahja- ja maksukorttien lukemisen testaaminen

Oheislaitesimulaattorin tarjoama virtuaalinen magneettinauhan lukulaite mahdollistaa myös tiettyjen magneettinauhan lukulaitteen tietojen määrittämisen. Näiden tietojen avulla voidaan testata lahja- ja maksukorttien lukemisen skenaariot. Luo kortti valitsemalla plusmerkin (**+**) painike ja valitsemalla sitten kortin tyyppi. Määritä sitten kortin numero tai seuraa myyntipisteeseen lähetettäviä tietoja sekä määritettävän kortin vanhenemiskuukautta ja -vuotta. **Kortin tyyppi** -kentässä valittu arvo on vain nimi, joka voidaan yhdistää korttiin. Tämän nimen avulla on helpompi tunnistaa kortit, kun ne luetaan oheislaitesimulaattorin kautta. Voit valita oheislaitesimulaattorissa määritetyt kortit kortin kuvan yläpuolella olevan vasemman nuolen (**&lt;**) ja oikean nuolen (**&gt;**) painikkeen avulla. Voit muokata ja poistaa kortteja plusmerkin (**+**) painikkeen vieressä olevan **Muokkaa**- ja **Poista**-painikkeen avulla.

### <a name="pin-pad"></a>PIN-näppäimistö

Voit määrittää PIN-näppäimistösimulaattorin, kun haluat simuloida OPOS:n PIN-näppäimistön. Kun myyntipisteessä suoritetaan sähköinen rahansiirtotapahtuma, joka vaatii PIN-tunnuksen, laiteasema kutsuu PIN-laitetta, joka pyytää PIN-tunnusta. Oheislaitesimulaattorin PIN-näppäimistö vaatii toimiakseen sähköisen rahansiirron maksuyhdistimen tuen.

### <a name="printer"></a>Tulostin

Virtuaalinen oheislaitetulostin näyttää kuitit sellaisina, kuin ne on tulostettu myyntipisteessä. Jos tulostustoiminnon tuloksena saadaan useita kuitteja, kuitteja on mahdollisuus selata.

#### <a name="configure-receipt-printing"></a>Kuittien tulostamisen määrittäminen

1.  Siirry kohtaan **Vähittäismyynti ja kauppa** &gt; **Kanavan asetukset** &gt; **Myyntipisteen asetukset** &gt; **Myyntipisteen profiilit** &gt; **Laiteprofiilit**.
2.  Valitse virtuaalioheislaitteille luotu laiteprofiili.
3.  Valitse **Tulostin**-pikavälilehdessä **Muokkaa**.
4.  Valitse **Kuittiprofiilin tunnus** -kentässä kuittiprofiili.
5.  Valitse **Tallenna**.

### <a name="scale"></a>Mittakaava

Kun punnittava tuote lisätään myyntipisteen tapahtumaan ja vaaka on määritetty, myyntipiste vastaanottaa painon vaa'alta. Tuote tai paino on määritettävä sekä virtuaaliselle että fyysiselle vaa'alle, ennen kuin tuote lisätään tapahtumaan. Ennen kuin punnittava tuote lisätään tapahtumaan, siirry oheislaitesimulaattorin vaakaan ja muuta vaa'an ilmoittamaa painoa plusmerkin (**+**) ja miinusmerkin (**–**) painikkeiden avulla. Voit myös antaa halutun painon suoraan **Nykyinen arvo** -kenttään. Voit muuttaa vaa'an mittayksikköä plusmerkin (**+**) painikkeen sekä **Muokkaa**- ja **Poista**-painikkeen avulla. Näin yksiköt voidaan määrittää punnittujen tuotteiden tai vaa'an maakohtaisten asetusten mukaan.

#### <a name="configure-a-scale-product"></a>Punnittavan tuotteen määrittäminen

1.  Siirry kohtaan **Vähittäismyynti ja** **kauppa** &gt; **Tuotteet ja luokat** &gt; **Vapautetut tuotteet luokittain**.
2.  Avaa tuotetietue.
3.  Valitse punnittava tuote.
4.  Määritä **Vähittäismyynti**-pikavälilehden **Punnittava tuote** -vaihtoehdon arvo **Ei** arvoksi **Kyllä**.

#### <a name="synchronize-changes-to-the-channel-database"></a>Muutosten synkronoiminen kanavatietokantaan

1.  Siirry kohtaan **Vähittäismyynti ja kauppa** &gt; **Vähittäismyynnin IT** &gt; **Jakeluaikataulu**.
2.  Valitse **1040**-jakeluaikataulu.
3.  Valitse **Suorita nyt**, kun haluat synkronoida muutokset myyntipisteen kanssa.

Kun tiedot on synkronoitu ja punnittava tuote on lisätty myyntipisteen tapahtumaan, myyntipiste tarkistaa vaa'an punnitusta varten.

### <a name="signature-capture"></a>Allekirjoituksen tarkistus

Virtuaalinen allekirjoituksen tarkistuslaite pyytää käyttäjältä allekirjoitusta virtuaaliseen allekirjoituksen tarkistuksen syöttökenttään, kun käytetty maksuväline vaatii allekirjoituksen. Käyttäjä voi hyväksyä allekirjoituksen, jolloin se näkyy myyntipisteessä. Kassanhoitaja voi sitten hyväksyä allekirjoituksen. Allekirjoitus tallennetaan yhdessä maksuvälineen kanssa ja synkronoidaan tietokantaan yhdessä muiden tapahtumatietojen kanssa.

#### <a name="set-up-a-tender-to-require-a-signature"></a>Allekirjoitusta vaativan maksuvälineen määrittäminen

1.  Siirry kohtaan **Vähittäismyynti ja kauppa** &gt; **Kanavat** &gt; **Vähittäismyymälät** &gt; **Kaikki vähittäismyymälät**.
2.  Valitse vähittäismyymälä.
3.  Valitse **Muokkaa**.
4.  Valitse **Asetukset** ja valitse sitten **Asetukset**-osassa **Maksutavat**.
5.  Valitse **Muokkaa**.
6.  Valitse maksutapa, joka vaatii allekirjoituksen.
7.  Määritä **Yleinen**-osan **Allekirjoituksen tarkistus** -kohdan **Käytä allekirjoituksen tarkistuslaitetta** -vaihtoehdon arvoksi **Kyllä**.
8.  Anna **Allekirjoituksen tarkistuksen vähimmäissumma** -kenttään vähimmäissumma, joka käynnistää allekirjoituksen tarkistuksen.

#### <a name="synchronize-changes-to-the-channel-database"></a>Muutosten synkronoiminen kanavatietokantaan

1.  Siirry kohtaan **Vähittäismyynti ja kauppa** &gt; **Vähittäismyynnin IT** &gt; **Jakeluaikataulu**.
2.  Valitse **1070**-jakeluaikataulu.
3.  Valitse **Suorita nyt**, kun haluat synkronoida muutokset myyntipisteen kanssa.

Kun tietojen synkronoinnin jälkeen käytetään allekirjoituksen vaativaa maksuvälinettä ja summa vastaa allekirjoituksen rajaa, myyntipiste pyytää allekirjoituksen virtuaalisessa allekirjoituksen tarkistuslaitteessa.

## <a name="additional-configuration"></a>Lisämääritys
Voit muokata oheislaitesimulaattorin määritystiedostoa niin, että se käsittelee testattavat skenaariot asianmukaisesti. Määritystiedosto sijaitsee kohdassa C:\\Program Files (x86)\\Microsoft Dynamics 365\\70\\VirtualPeripherals\\Microsoft.Dynamics.Commerce.VirtualPeripherals.Client.exe.config. Määritystiedosto määrittää vaa'an testaamisessa käytettävissä olevat yksiköt, testaamisessa käytettävissä olevat korttityypit ja viivakoodityypit. Esimerkiksi määritystiedoston tekstiarvoja muokkaamalla voidaan lisätä suorituksen aikana valittavissa oleva uusi korttityyppi tai mittayksikkö. Uudet arvot tulevat näkyviin, kun sovellus on käynnistetty uudelleen.

## <a name="troubleshooting"></a>Vianmääritys
Oheislaitesimulaattorin aktiviteetit kirjataan lokiin oheislaitesimulaattorissa. Loki sijaitsee kohdassa C:\\Program Files (x86)\\Microsoft Dynamics 365\\70\\VirtualPeripherals\\Microsoft.Dynamics.Commerce.VirtualPeripherals.Client.exe.config. Oheislaitesimulaattori raportoi ongelmat myös Windowsin tapahtumalokiin. Se löytyy kohdasta **Sovellus- ja palvelulokit** &gt; **Microsoft** &gt; **DynamicsAX**. Jos laiteprofiiliin tai muulle alueelle tekemäsi muutokset eivät näy, kun käytät MPOS-sovellusta tai oheislaitesimulaattoria, tarkista jakelun ajastustyöt, joiden avulla tiedot synkronoidaan kanavatietokannan kanssa. Jos muutokset on synkronoitu, mutta ne eivät senkään jälkeen näy myyntipisteessä, käynnistä myyntipisteen asiakasohjelma uudelleen. Määritettyihin kassoihin tehdyt muutokset näkyvät vasta, kun uusi vuoro on luotu. Jos siis teet muutoksia kassoihin, varmista, että suljet aina aiemmin avatun vuoron, ennen kuin testaat uuden kassan asetukset. Jos valmistajan ohjain on asennettu Monroe Consulting Services -toimittajan yhteisten ohjausobjektien jälkeen, ohjain saattaa aiheuttaa virheitä yhteisten ohjausobjektien toiminnassa. Jos näin tapahtuu, yhteiset ohjausobjektit tulee asentaa uudelleen.

<a name="see-also"></a>Lisätietoja
--------

[Vähittäismyynnin oheislaitteiden yleiskatsaus](retail-peripherals-overview.md)




