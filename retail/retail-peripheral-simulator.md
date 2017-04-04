---
title: "Vähittäismyynnin peripheral simulator"
description: "Tässä aiheessa kuvataan peripheral simulator-työkalu, joka toimitetaan Microsoft Dynamics-365 työvaiheiden - Retail."
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 266544
ms.assetid: 16f31e70-15fc-441e-9727-e6a31c3a48f5
ms.search.region: global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
translationtype: Human Translation
ms.sourcegitcommit: 42dc414ff2bb6359b47d89c3bd3c510e4258f816
ms.openlocfilehash: b2229466040351d8c2b9494b30b4c928651820b8
ms.lasthandoff: 03/31/2017


---

# <a name="retail-peripheral-simulator"></a>Vähittäismyynnin peripheral simulator

Tässä aiheessa kuvataan peripheral simulator-työkalu, joka toimitetaan Microsoft Dynamics-365 työvaiheiden - Retail.

<a name="overview"></a>Yleiskuvaus
--------

Microsoft Dynamics-365 - toimintoja varten Retail peripheral simulator on työkalu, jolla voit määrittää, testata ja vianmääritys oheislaitteita, joita käytetään vähittäiskaupan ympäristöissä. Voit käyttää peripheral simulator retail oheislaitteet testauksen virtaviivaistamisesta ja eristää ongelmat, jotka johtuvat virheelliset asetukset tai viallisen laitteen ohjaimet. Sisältää syrjäisillä simulator työpöydän ohjelma, jossa on laitteet virtual versiot operaatioille, Dynamics-365 - Retail tukee. Osa virtual jokaiselle laitteelle on laite- ja vähittäiskaupan myyntipaikkaan saakka (POS) välistä vuorovaikutusta. Sen avulla voit myös säätää syöttö, joka on voimassa monissakin POS. Perifeerisen simulator tukee Myyntipiste ja virtual seuraavien laitteiden välistä vuorovaikutusta:

-   **Tulostimen** – peripheral simulator voivat Näytä vastaanotot, jotka on määritetty POS-tulostin.
-   **Näytä rivin** – virtual Rivinäyttö näyttämään fyysistä riviä näyttää tehtävän voi määrittää.
-   **Magneettinauhan lukulaite (MSR)** – voit lähettää magneettiraita simuloidut tapahtumat peripheral simulator-Myyntipiste.
-   **Laatikko** – voit simuloida fyysinen kassa.
-   **Laatikko 2** – määrittämällä toisen kassan, oheislaite Simulator simuloidaan skenaarioita, jotka sisältävät ainoastaan yhtä rekisteriä, jossa on käytössä kaksi vuoroa POS.
-   **Skannerin** –, joka tukee peripheral simulaattorin virtual viivakoodi skanneri voi myöntää viivakoodi skannauksen tapahtumat.
-   **Mittakaavan** – virtual asteikon avulla voit simuloida punnitun nimikkeiden käsittelemisen Myyntipiste.
-   **Henkilökohtainen tunnus (PIN) numeronäppäimistön** – voit simuloida PIN pad toimintojen. **Huomautus:** fyysisen PIN-näppäimistö maksun Connectorin kautta tuki on pantava täytäntöön.
-   **Allekirjoituksen tarkistus** – sisältää syrjäisillä simulator virtual allekirjoitus sieppauslaite, jonka voit määrittää pyytämään allekirjoitukset, joita tarvitaan tarjousten, kuten asiakasmaksut tilin.

Perifeerisen simulaattorin avulla voit myös simuloida näppäimistön kiila tapahtumia, jotka ovat peräisin viivakoodin skannerin ja MSR. Virtuaalisen perifeerisestä simulator tukee erityisesti objektien linkittämisen ja upottamisen Retail POS (OPOS)-laitteille.

## <a name="key-scenarios"></a>Tärkeimpiin
### <a name="troubleshooting"></a>Vianmääritys

Voit käyttää peripheral simulator laitteen asennuksen vianmääritystä. Jos sinulla ei ole peripheral simulator tai saman luokan toinen laite voi olla vaikea määrittää, missä ongelmat ovat peräisin. Kuitenkin kun peripheral simulator, voit määrittää näennäislaitteet, ja suorittaa samalla koodipoluissa ja moduuleja, joita käytetään fyysisten laitteiden. Merkittävin ero näennäislaitteet ja fyysisten laitteiden on huoltokohteita tai laiteohjaimen peripheral simulator näkökulmasta. Fyysisten laitteiden huolto-objektin toimitetaan laitteen valmistaja. Sitä vastoin, oheislaite, simulator huoltokohteiden toimitetaan osana peripheral simulator. Perifeerisen simulator toimii oikein, jos laite ei toimi oikein, kun laitteen laitteistoprofiilin nimeä on muutettu todellista laitteen nimen, kun oletetaan, että valmistajan toimittaman huoltokohteen ongelma on.

### <a name="training"></a>Koulutus

Perifeerisen simulaattorin avulla voit lisätä realistinen kerroksen kassa koulutus, kun fyysinen laitteisto-asennus ei ole käytettävissä. Kun peripheral simulator sisältyy koulutus skenaarioita, kassa tehokkaasti käsitellä Myyntipiste tarjoamalla toimia kuten tuotteen koodi tarkistuksia ja lahja kortti swipes ja tarkkailemalla mitä kuitit tulostetaan tietyn tapahtuman.

### <a name="testing"></a>Testaus

Perifeerisen simulaattorin avulla voit testata tuotteen viivakoodien kuitin muotoja ja niin edelleen, tarvitsematta ottaa fyysinen laitteisto virtuaaliympäristössä. Koska fyysisiä laitteita ei tarvita eikä sinulla ole POS asiakkaan laitteisto-asema tai fyysisen tietokoneen käyttöön, voit testata nopeammin takaisin office tehtyjä muutoksia.

## <a name="set-up-the-peripheral-simulator"></a>Määritä peripheral simulator
### <a name="set-up-a-hardware-profile"></a>Laitteistoprofiilin määrittäminen

1.  Määrittäminen peripheral simulator, siirry **jälleenmyynti- ja commerce**&gt;**kanava-asetukset**&gt;**POS-asetukset**&gt;**POS-profiilit**&gt;**laitteistoprofiilien**.
2.  Voit luoda uuden profiilin valitsemalla **uusi**.
3.  Syötä arvot- **profiilin numero** ja **kuvaus** kentät.
4.  Seuraavan taulukon avulla voit määrittää virtuaalisen laitteita, jotka on testattava. Tässä on selitys taulukon sarakkeet:
    -   **Laitteen** – antaa tämän sarakkeen nimi, joka määritetään laitteen Laajenna pikavälilehti.
    -   **Laitteen tyyppi** – tässä sarakkeessa näkyy arvo, joka on merkitty laitteen nimi-kentässä.
    -   **Laitteen nimi** – tässä sarakkeessa näkyy tarkka arvo, joka määritetään laitteen nimi. **Tärkeää:** laitteen nimiä, jotka on annettu tähän tarvitaan, koska laitteisto-asema käyttää näitä erityisiä nimiä laitteiden korjaamiseen. Jos et käytä näitä erityisiä nimiä, laite ei ole käytettävissä.

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

**Huomautus:** laitteistoprofiilissa ei erityisiä asetuksia vaaditaan Simuloi kiila näppäintapahtumat viivakoodin skannerin ja MSR.

### <a name="assign-the-hardware-profile-to-a-register"></a>Määrittää rekisterin laitteistoprofiili

1.  Kun on luotu laitteistoprofiili, siirry **jälleenmyynti- ja commerce**&gt;**kanava-asetukset**&gt;**POS-asetukset**&gt;**Rekisteröi**.
2.  - **Kassakoneet** -luettelosta napsauttamalla linkkiä **rekisterinumero** kenttä rekisterissä, jota tulisi käyttää peripheral simulator.
3.  Valitse **Muokkaa**.
4.  - **Profiilit**, osa **laitteistoprofiilin** kenttään, valitse laitteistoprofiili, jonka olet luonut virtuaalinen oheislaitteiden.
5.  Click **Save**.

### <a name="synchronize-changes-to-the-channel-database"></a>Synkronoi kanavan tietokantaan tehdyt muutokset

1.  Siirry **jälleenmyynti- ja commerce**&gt;**vähittäismyynnin IT**&gt;**aikataulun jakelu**.
2.  Valitse **1090** jakeluaikataulu.
3.  Valitse **suorittaa nyt** Myyntipiste muutokset synkronoidaan.

Kun tiedot on synkronoitu, uuden laitteistoprofiilin ja rekisterin muutokset ovat käytettävissä tietokanta kanava.

## <a name="install-the-peripheral-simulator"></a>Asenna peripheral simulator
1.  Siirry **jälleenmyynti- ja commerce**&gt;**kanava-asetukset**&gt;**POS-asetukset**&gt;**POS-profiilit**&gt;**laitteistoprofiilien**.
2.  Valitse **Lataa**, ja sitten **PeripheralSimulator**. **Huomautus:** on poistettava käytöstä ponnahdusikkunoiden esto-ohjelmat, ennen kuin lataat peripheral simulator.
3.  Kun lataus on valmis, Avaa **Lataa** -kansio ja kaksoisnapsauta **VirtualPeripherals.msi** Käynnistä asennusohjelma.
4.  Perifeerisen simulator asentaa käyttäen oletusasetuksia.

Lisäksi peripheral simulator sinun on asennettava yhteisten valvonta-objektien Monroe konsultointipalvelut. Muussa tapauksessa peripheral simulator ei toimi oikein. Voit ladata yhteisten valvonta-objektien, <http://monroecs.com/oposccos_current.htm>.

## <a name="using-the-peripheral-simulator"></a>Peripheral simulaattorin avulla.
Perifeerisen simulator Aloita valitsemalla **käynnistää** tietokoneeseen, kirjoita **Retail peripheral simulator**, ja valitse sitten sovellus, kun se tulee näkyviin etsinnän tuloksiin. Kun olet käynnistänyt peripheral simulator, valitsemalla laitteen nimen, jos haluat nähdä tuettujen laitteiden. Nämä laitteet näkyy vasemmalla puolella ikkunan välilehdet. Jos haluat tarkastella tietyn laitteen, valitse laitteen välilehti.

### <a name="line-display-capabilities"></a>Rivin näytön ominaisuuksia

Rivin näyttö on ensimmäinen laite on kerrottu peripheral simulator. Kun virtuaalinen rivin näyttö on määritetty, näyttää Rivinimikkeet sellaisena kuin ne on skannattu Myyntipisteen tapahtumassa. Lisäksi rivinimikkeet näytössä näkyy summa, joka on maksettava, kun tarjous on valittu myyntipisteessä. Se näyttää myös, joka on erääntynyt saldo Jos tarjouksia on annettu, mutta tasapaino on edelleen tapahtuman eräpäivä. POS ei ole käytössä, kun sanoma näytetään osoittamaan, kassan suljetaan. Sinun on määritettävä viestin **viiva näyttää** laitteistoprofiili-pikavälilehdessä.

### <a name="cash-drawer-capabilities"></a>Rahaa laatikon ominaisuudet

Kassan on toinen laite, joka on kerrottu peripheral simulator. Laitteistoprofiili on määritetty käyttämään virtual rahaa vetolaatikot, Myyntipiste avataan, kun aktiivinen VAIHTO kassan vastaus laatikon toimintoja kuten kassan laskemisia maksuvälineittäin, ja siten, että kassa voi tehdä muuta tai tallettaa rahaa vakio cash-and-carry tapahtumien aikana. Virtual rahaa vetolaatikot on otsikot **Main laatikko** ja **toinen laatikko**. Nämä otsikot edustavat laatikon ja laatikko 2 laitteistoprofiilissa, vastaavasti. Kun laatikossa on suljettu, suljettu kassan kuva näkyy ja lukee suljettu kassa-painiketta **Vetolaatikko**. Jos napsautat tätä painiketta, kuva korvataan kuva Avaa kassan osoittamaan, laatikko on nyt Avoin. Avaa kassa-painikkeen otsikko on **Sulje laatikko**. Useilla operaatioilla myyntipisteessä saattaa avata kassan. Useimmat toiminnot voi jatkaa kassan ollessa avoinna. Poikkeuksia ovat osa päivä toiminnoista. Jos POS käyttäjä saa virhesanoman, joka ilmaisee, että toimintoa ei voi suorittaa kassan ollessa avoinna, käyttäjän on suljettava virtuaalisen tai fyysisen kassan jatkaa. Jos kassa, on merkitty **jaettujen** laitteistoprofiilin, järjestelmä ei tarkista kassa suljetaan ennen operaation. Toiminto etenee normaalisti, vaikka kassan on avoinna. Tämä toiminta tukee skenaarioita, jossa myynti associates kesken jaetaan rahaa vetolaatikot ja yksi liittää käyttää kassa kun toinen associate itsenäisistä tehtävistä suorittaa oman POS-laite. Kassan tehtyjä muutoksia ei ole ilmeistä, ennen kuin nykyinen VAIHTO suljetaan ja avataan uusi vuoro.

### <a name="msr-capabilities"></a>MSR-ominaisuudet

Perifeerisen simulator tuki vakaan virtual MSR toimintoja käsittelemällä OPOS-tilassa tai näppäimistötilassa sen kiila. OPOS-tilassa edellyttää, että MSR määritettävä laitteistoprofiili OPOS-laitteen toimimaan. Kiila näppäimistötilassa lähettää kiila näppäintapahtumat vain Microsoft Windows. Erot asetuksissa, paitsi OPOS ja näppäimistön kiila tilat eroavat toisistaan seuraavilla tavoilla:

-   POS-asiakas antaa tiettyjä skenaarioita, kuten skenaarioita, joiden avulla kanta tai lahja kortin merkintä magneettinauhan tiedot laitteiden OPOS-MSR.
-   Näppäimistötilassa kiila oheislaite simulator lähettää näppäimistö kiila kenttä, joka on aktiivinen, kun tiedot lähetetään. Näin muistuttaa ongelma, joka ilmenee, jos tiedot on syötetty näppäimistöllä. Käyttäjä siirtyy käyttämään MSR näppäimistön kiila, Retail Moderni POS (MPOS) varmistaaksesi, että tiedot on saatu oikeaan kenttään. Tämän vuoksi viive, voit määrittää niin, että hänellä on aikaa varmistaa, että tiedot lähetetään oikealle kentälle.

#### <a name="testing-gift-and-payment-card-swipes"></a>Lahja- ja maksu korttia swipes testaus

Virtual MSR, oheislaite simulator tarjoaa myös avulla voit määrittää tiettyjä tilanteita, joissa lahjan ja maksu korttia swipes testata MSR tietoja. Luo kortti, napsauta plus-merkkiä (**+**)-painiketta ja valitse kortti. Määritä kortin numero tai seurata tietoja, jotka on lähetettävä Myyntipiste voimassaolokuukausi ja kortin, jonka määrität vuoden jälkeen. Arvo, jotka olet valinnut **kortin tyyppi** kenttä on aivan otsikon, jossa voidaan yhdistää kortti. Tämän tarran helpottaa tunnistaa kortteja kun ne on luettu peripheral simulaattorin avulla. Voit valita kortit, jotka on määritetty käyttämällä nuoli vasemmalle peripheral simulator (**&lt;**) ja oikea nuoli (**&gt;**) kortin kuva yllä painikkeita. Voit muokata ja poistaa kortteja käyttämällä **Muokkaa** ja **poistaa** vieressä olevaa plus-merkkiä (**+**) painiketta.

### <a name="pin-pad"></a>PIN-näppäimistö

Voit määrittää PIN pad simulator Simuloi OPOS-PIN-näppäimistö. Kun sähköisen varojen siirron (EFT) on tapahtuma suoritetaan, kun myyntipisteessä ja se edellyttää PIN-tunnuslukua, laitteiston station kutsuu PIN-tunnuksen laitteen kysymään PIN-määrite. Toimimaan, oheislaite Simulator PIN-näppäimistö edellyttää EFT maksun connector tukea.

### <a name="printer"></a>Tulostin

Virtuaalisen perifeerisestä tulostin näkyy vain vastaanotot POS tulostusmuodossa. Jos tulostuksen toiminta tuottaa useita vastaanottoja, voit selata vastaanotot.

#### <a name="configure-receipt-printing"></a>Määritä kuitin tulostus

1.  Siirry **jälleenmyynti- ja commerce**&gt;**kanava-asetukset**&gt;**POS-asetukset**&gt;**POS-profiilit**&gt;**laitteistoprofiilien**.
2.  Valitse laitteistoprofiili, jonka loit virtual oheislaitteet.
3.  - **Tulostimen** -pikavälilehden valitsemalla **Muokkaa**.
4.  - **Vastaanoton Profiilitunnus** vastaanotto-profiili-kenttään.
5.  Click **Save**.

### <a name="scale"></a>Mittakaava

Asteikon tuote lisätään POS-tapahtumaan ja asteikko on määritetty, kun Myyntipiste hakee paino asteikko. Molemmat virtuaalinen ja fyysinen asteikkoa tuotteen tai paino olisi määritettävä ennen tuotteen lisäämistä tapahtumaan. Ennen kuin lisäät tuotteen tapahtumaan, siirry peripheral Simulator mittakaava ja käytä plus-merkkiä (**+**) ja miinusmerkkiä (**–**) painikkeita muuttamaan paino, mittakaava tulee raportoida. Voit myös kirjoittaa suoraan haluttu paino **nykyisen arvon** kenttä. Voit säätää paino asteikon yksiköistä, käyttämällä plusmerkkiä (**+**), **Muokkaa**, ja **poistaa** painikkeita. Tällä tavoin yksiköt voidaan määrittää tuotteet, jotka punnitaan tai kieli, jossa käytetään asteikon perusteella.

#### <a name="configure-a-scale-product"></a>Määritä skaalaus-tuote

1.  Siirry **vähittäiskaupan ja****commerce**&gt;**tuotteet ja luokat**&gt;**vapautetut tuotteet luokittain**.
2.  Avaa tuotetietue.
3.  Valitse tuote, jolla voidaan punnita.
4.  - **Retail** -pikavälilehdessä määrittää **tuotteen** vaihtoehto **ei**, **Kyllä**.

#### <a name="synchronize-changes-to-the-channel-database"></a>Synkronoi kanavan tietokantaan tehdyt muutokset

1.  Siirry **jälleenmyynti- ja commerce**&gt;**vähittäismyynnin IT**&gt;**aikataulun jakelu**.
2.  Valitse **1040** jakeluaikataulu.
3.  Valitse **suorittaa nyt** Myyntipiste muutokset synkronoidaan.

Kun tiedot on synkronoitu, kun asteikko tuote lisätään Myyntipisteen tapahtuman POS tarkistaa paino asteikko.

### <a name="signature-capture"></a>Allekirjoituksen tarkistus

Virtual allekirjoitus sieppauslaite käyttäjää antaa allekirjoituksen virtual allekirjoituksen capture alustalla, jota käytetään tarjous edellyttää allekirjoitusta. Käyttäjä voi hyväksyä allekirjoitusta näytettävät myyntipisteessä. Kassanhoitaja voi sitten hyväksyä allekirjoitus. Allekirjoitus on sitten tallennettu ja tarjouksen ja tausta tapahtuman muut tiedot synkronoidaan.

#### <a name="set-up-a-tender-to-require-a-signature"></a>Määritä tarjouksen allekirjoitus vaaditaan

1.  Siirry **jälleenmyynti- ja commerce**&gt;**kanavia**&gt;**liikkeistä**&gt;**kaikki liikkeistä**.
2.  Valitse retail store.
3.  Valitse **Muokkaa**.
4.  Valitse **määrittää**, ja sitten **määrittäminen** -osassa **maksutavat**.
5.  Valitse **Muokkaa**.
6.  Valitse maksutapa, joka edellyttää allekirjoitusta.
7.  - **Yleisen** osan alle **allekirjoituksen Capture**, aseta **käytä allekirjoitusta sieppauslaite** asetuksella **Kyllä**.
8.  - **Allekirjoituksen tarkistuksen vähimmäissumma** -kenttään vähimmäismäärä, joka käynnistää Allekirjoituksen tarkistus.

#### <a name="synchronize-changes-to-the-channel-database"></a>Synkronoi kanavan tietokantaan tehdyt muutokset

1.  Siirry **jälleenmyynti- ja commerce**&gt;**vähittäismyynnin IT**&gt;**aikataulun jakelu**.
2.  Valitse **1070** jakeluaikataulu.
3.  Valitse **suorittaa nyt** Myyntipiste muutokset synkronoidaan.

Sen jälkeen, kun tiedot synkronoidaan, kun tarjouksen käytetään allekirjoitusta edellyttävää ja summan allekirjoituksen raja-arvon mukainen, Myyntipiste kysyy näennäisen allekirjoitus sieppauslaite allekirjoituksen.

## <a name="additional-configuration"></a>Muita määrityksiä
Voit muokata peripheral simulator määritystiedoston korjaamiseen skenaarioita, joka olet testaus kudoksiin. Löydät osoitteesta C: määritystiedoston\\Program Files (x86)\\Microsoft Dynamics-365\\70\\VirtualPeripherals\\Microsoft.Dynamics.Commerce.VirtualPeripherals.Client.exe.config. Kokoonpanomääritystiedostossa määrittää yksiköt, joita voidaan testata asteikon ja viivakoodin tyypit Korttityypit testausta varten käytettävissä olevat. Esimerkiksi muokkaamalla määritystiedostossa tekstiarvoja, voit lisätä uuden korttityypin tai mittayksikkö, joka on valittu suorituksen aikana. Uudet arvot näkyvät, kun sovellus on käynnistetty uudelleen.

## <a name="troubleshooting"></a>Vianmääritys
Perifeerisen simulator tehtävät kirjataan peripheral simulator sisällä. Loki löytyy osoitteesta C:\\Program Files (x86)\\Microsoft Dynamics-365\\70\\VirtualPeripherals\\Microsoft.Dynamics.Commerce.VirtualPeripherals.Client.exe.config. Peripheral simulator ilmoittaa ongelmista myös Windowsin tapahtumalokiin, jota voi käyttää osoitteessa **sovellus- ja palvelulokit**&gt;**Microsoft**&gt;**DynamicsAX**. Jos laitteistoprofiili tai muilla alueilla tehdyt muutokset eivät ole ilmeistä MPOS tai oheislaite simulator, tarkista jakelun ajoitustyön, jota käytit kanavan tietokannan tiedot. Jos muutokset on synkronoitu, mutta eivät silti ilmeistä myyntipisteessä, uudelleen myyntipisteen. Määritetty rahavirtaa vetolaatikot muutoksia ei oteta tehokkaita, kunnes luodaan uusi vuoro. Varmista siis, jos teet muutoksia käteisen vetolaatikot, voit testata uutta rahaa laatikko asetukset olemassa VAIHTO aina sulkea. Joskus Jos valmistajan ohjain on asennettu jälkeen yhteinen valvonta objekteja Monroe konsultointipalvelut, kuljettaja voi aiheuttaa yleisiä hallinta-objekteja voi lakata toimimasta oikein. Tässä tapauksessa sinun on asennettava yhteisen control-objektit.

<a name="see-also"></a>Lisätietoja
--------

[Retail peripherals overview](retail-peripherals-overview.md)


