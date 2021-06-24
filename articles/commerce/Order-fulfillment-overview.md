---
title: Myymälän tilauksen täyttäminen
description: Tässä aiheessa on myymälän tilauksen täyttämisen yhteenveto.
author: rubencdelgado
ms.date: 10/30/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RetailStoreTable, RetailTillLayout
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.search.industry: retail
ms.author: rubendel
ms.search.validFrom: 2017-10-30
ms.dyn365.ops.version: ''
ms.openlocfilehash: 88665c70b05d9ecf8ec2641862d870d87604092f
ms.sourcegitcommit: 74e47075eab2b0b28f82b0d57f439719847ecb01
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/07/2021
ms.locfileid: "6193152"
---
# <a name="store-order-fulfillment"></a>Myymälän tilauksen täyttäminen

[!include [banner](includes/banner.md)]

Monet jälleenmyyjät haluaisivat optimoida tilausten täyttämisen antamalla myymälöille mahdolliseen täyttää tilauksia. Tilauksen täyttäminen myymälätasolla voi helpottaa yksittäisten myymälöiden liian suuria varastoja. Se voi olla tarpeellista myös logistiikan vuoksi tilanteissa, joissa myymälässä on ylimääräistä tilaa tai joissa se sijaitsee toimituksen kannalta lähempänä asiakasta. Näitä tarpeita varten myyntipisteissä voi käytätä yhdistettyä tilausten täyttämistoimintoa.

Tietyssä myymälässä täytettävien tilausten varastoa ilmoitetaan tilauksen otsikossa tai tilausriveillä.

Myyntipisteen tilauksen täyttämistoiminto on yhtenäinen myyntipisteen työalue, jossa tilaukset voidaan käsitellä myyntipisteessä. Käsiteltäviä toimintoja ovat niin tilauksen hyväksyminen, tilauksen merkitseminen lähetetyksi kuin myymälästä noudon käynnistäminen.

## <a name="access-unified-order-fulfillment-in-the-point-of-sale"></a>Myyntipisteen yhdistetyn tilauksen täyttämisen käyttö

Tilauksen täyttämisen, [toimintotunnus 928](pos-operations.md), avulla voidaan käyttää myymälän tilauksen täyttämisen työaluetta myyntipisteessä.

Tilauksen täyttämistoiminnon käyttöoikeudet eivät ole heti käytössä, mutta käyttäjät voivat tulevaisuudessa kutsua toiminnon myyntipisteestä **Salli tilauksen noutaminen** -käyttöoikeudella.

Myymälätasolla on määritysasetus, jolla voidaan määrittää, onko tilausrivi hyväksyttävä manuaalisesti myyntipisteestä. Jos tätä määritysasetusta ei ole määritetty, tilausrivit hyväksytään oletusarvoisesti. Jos tämä määritysasetus on otettu käyttöön, tilauksien hyväksyminen myyntipisteestä edellyttää, että myyntipisteen käyttäjät valitsevat **Salli tilauksen hyväksyminen** -käyttöoikeuden.

Tilausrivit voidaan myös hylätä myyntipisteestä. Tilausrivi hylkääminen tarkoittaa, että sitä ei täytetä kyseisessä myymälässä. Lisäksi tilausrivi lähetetään määritettäväksi uudelleen toiseen myymälään tai varastoon. Tilausrivin hylkäysoikeus myönnetään **Salli tilauksen hylkääminen** -käyttöoikeuden kautta.

## <a name="order-fulfillment-operation-parameters"></a>Tilauksen täyttämistoiminnon parametrit

Tilauksen täyttämiseen sisältyy valmiita parametreja, joita voidaan käyttää myyntipisteessä kutsuttavissa toiminnoissa. Jos **Kaikki tilaukset** -parametri on määritetty, kaikki tilaukset näytetään, kun toimintoa käytetään. **Lähetettävät tilaukset** -parametri näyttää vain tilaukset, jotka on lähetettävä myymälästä, kun taas **Noudettavat tilaukset** näyttää myymälästä noudettavat tilaukset.

## <a name="orders-for-fulfillment"></a>Täytettävät tilaukset

Tilauksen täyttämistoiminto näyttää vain ne tilaukset, jotka joko noudetaan tai lähetetään valitusta myymälästä. Muiden myymälöiden täytettäviä tilauksia ei mainita tilauksen täyttötoimintoa käytettäessä.

## <a name="line-selection"></a>Rivin valinta

Rivit voidaan valita toimintoruudun **Valitse**-toiminnolla. Kun **Valitse** on otettu käyttöön, käsiteltäväksi voidaan valita useita rivejä. Voit poistaa valitut rivit napsauttamalla samaa riviä uudelleen.

## <a name="line-details"></a>Rivin erittely

Rivin tiedot voidaan näyttää käyttämällä rivitietojen lisätietoikkunaa. Avattuna tässä ikkunassa on kolme välilehteä, jossa on lisätietoja valitusta rivistä. Ensimmäisessä **Rivin erittely** -välilehdessä on tietoja itse rivistä sekä tilatusta ja jäljellä olevasta määrästä. Näkyvissä on myös muita tietoja, kuten noudettu, pakattu ja laskutettu määrä sekä toimitustapa ja toimitusosoite. **Tilauksen tiedot** -välilehdessä on tilauksen otsikon tiedot, kuten asiakas, asiakastunnus, tilausnumero, tilauksen kokonaissumma ja saldo. **Varasto**-välilehdessä on tietoja valitun rivin fyysisesti saatavilla olevasta varastosta, varatusta varastosta ja tilatusta varastosta.

Jos valittuna on useita rivejä, tilauksen rivitietojen lisätietoikkuna ilmaisee vain, että useita rivejä on valittu. Jos haluat näyttää yhden rivin tiedot, poista rivejä, kunnes jäljellä on vain yksi rivi.

## <a name="pending-order-lines"></a>Odottavat tilausrivit

Yhdistetty tilauksen täyttäminen sisältää mahdollisuuden hyväksyä tilauksia manuaalisesti. Oletusarvosti myymälässä täytettävät tilaukset on jo hyväksytty. Jos liiketoimintaprosessit kuitenkin edellyttävät, että myymälätason työntekijä hyväksyy tilaukset, manuaalinen hyväksyntä voidaan ottaa käyttöön vähittäismyymälätasolla. Ota tilauksen hyväksyntä käyttöön valitsemalla **Vähittäismyynti ja kauppa** \> **Kanavat** \> **Myymälät** \> **Kaikki myymälät**. Avaa myymälä ja etsi sitten **Yleiset**-välilehdessä **Tilauksen täyttäminen** -alaotsikko. Tässä kohdassa on **Manuaalinen hyväksyminen** -asetus, jossa on oletusarvoisesti valittu **Ei**. Kun valitset asetukseksi **Kyllä** ja synkronoit muutokset kanavan tietokantaan, tilausrivit voidaan nyt käsitellä hyväksymisprosessin mukaisesti.

Työntekijät, joilla on **Salli tilauksen hyväksyminen** -käyttöoikeus, voivat avata tilauksen täyttämisen ja valita hyväksyttävät rivit. Kun rivit on hyväksytty, niiden tila ei ole enää **Odottaa** vaan **Hyväksytty** ja tilauksen hyväksymisprosessia voidaan jatkaa. Kun **Manuaalinen hyväksyminen** on otettu käyttöön, tilauksia ei käsitellä, ennen kuin ne on hyväksytty.

Myymälästä noudettavien tilausten tila ei ole koskaan **Odottaa**. Tällä tavoin voidaan estää tilanne, jossa asiakas saapuu myymälään mutta tilausriviä ei voi käsitellä, koska paikalla ei ole riittävät oikeudet omaavaa työntekijää.

## <a name="accepted-order-lines"></a>Hyväksytyt tilausrivit

Tilausten, joiden rivin tila on **Hyväksytty**, loput tilauksen täyttämiseen liittyvät vaiheet voidaan käsitellä myyntipisteessä. Kun tilaus on hyväksytty, tilausriville voidaan tehdä kaikki jäljellä olevat toiminnot.

Hyväksytty tilausrivi voidaan esimerkiksi valita ja sitten noutaa suoraan ilman keräys- ja pakkausvaiheita.

## <a name="line-actions"></a>Rivitoiminnot

### <a name="pick"></a>Keräilyt

**Keräile**-luokan toiminnot on tarkoitettu auttamaan tilausrivien keräilyä hyllyiltä. Keräystoiminto voidaan suorittaa vain tilausriveillä, jotka on hyväksytty aiemmin.

**Toiminto: keräys**

- **Tuloksena oleva myyntipisteen tila**: keräys
- **Tuloksena oleva taustajärjestelmän tila**: ei muutosta

Kun tilaus on hyväksytty, rivit voidaan valita ja niiden tilaksi voidaan merkitä **Keräys**. Kun rivin merkintä on **Keräys**, se ilmaisee, että rivin keräys on jo suoritettu. Tällä tavoin estetään se, että kaksi työntekijää yrittäisi kerätä saman tilausrivin samanaikaisesti.

**Toiminto: keräysluettelon tulostaminen**

- **Tuloksena oleva tila**: keräys
- **Tuloksena oleva taustajärjestelmän tila**: ei muutosta

Keräysluettelot voidaan tulostaa myyntipisteessä, mikä auttaa työntekijöitä keräysprosessissa. Keräystä suorittava työntekijä voi kuljettaa tulostettua keräysluetteloa mukanaan, ja hän voi merkitä keräysluettelon tuotteet manuaalisesti kerätyiksi tuotteiden keräyksen yhteydessä.

Keräysluettelon muoto määritetään Commercessa, jossa se lisätään kuittiprofiiliin. Lisätietoja kuittiprofiilien määrittämisestä on kohdassa [Kuittimallit ja tulostaminen](receipt-templates-printing.md).

Jos rivejä on valittu ja kyseisten rivien keräysluettelo on tulostettu, niiden tilaksi päivitetään automaattisesti **Keräys**.

**Toiminto: merkitty kerätyksi**

- **Tuloksena oleva tila**: keräilty tai osittain keräilty
- **Tuloksena oleva taustajärjestelmän tila**: keräilty tai osittain keräilty

Kun fyysiseen keräily on tehty, rivin tilaksi voidaan merkitä **Keräilty**. Kun rivi valitaan ja sen tilaksi merkitään **Keräilty**, tapahtuu reaaliaikainen kutsu päivittää tilausrivi. Kun rivin tilaksi on merkitty myyntipisteessä **Keräilty**, myös taustajärjestelmän tilaksi päivitetään **Keräilty** ja varastotapahtumat osoittavat, että tietty määrä on vähennetty.

Kun tilauksia käsitellään ajan mittaan, tietyllä rivillä voidaan käsitellä osittainen määrä. Jos rivi on valittu ja tehdään toiminto **Merkitty kerätyksi** ja jos määrä on suurempi kuin yksi, käyttäjää pyydetään ilmoittamaan määrä. Jäljellä oleva kerättävä määrä täytetään automaattisesti. Jos määritetty määrä on pienempi kuin jäljellä oleva määrä, rivin tilaksi tulee **Osittain kerätty**. Kun tilausrivi päivitetään taustajärjestelmässä, myös se ilmaisee osittain kerättyä tilaa ja varastopäivityksessä käytettyä käyttäjän antamaa määrää.

Jos tilausrivi kerätään vahingossa, tilausrivin keräys on kumottava taustajärjestelmässä. Myyntipisteessä ei tueta tällä hetkellä mitään keräyksen kumoustoimintoa.

Eri tilauksista voi valita tilausrivejä ja niiden tilaksi voidaan merkitä **Keräys**, ne voidaan tulostaa samaan keräysluettelon tai niiden tilaksi voi merkitä **Keräilty**.

### <a name="pack"></a>Pakkaus

Tilausrivit voidaan pakata koska tahansa sen jälkeen, kun tilausrivi on hyväksytty.

**Toiminto: tulosta pakkausluettelo**

- **Tuloksena oleva tila**: pakattu tai osittain pakattu
- **Tuloksena oleva taustajärjestelmän tila**: toimitettu tai osittain toimitettu

Tämä toiminto merkitsee rivit pakatuiksi tai osittain pakatuiksi ja tulostaa pakkausluettelon. Pakkausluettelo voidaan tulostaa ja sen avulla voidaan tarkistaa yhdessä pakatut tuotteet. Pakkausluettelon muoto määritetään Commercessa, jossa se lisätään kuittiprofiiliin. Lisätietoja kuittiprofiilien määrittämisestä on kohdassa [Kuittimallit ja tulostaminen](receipt-templates-printing.md).

**Toiminto: merkitse pakatuksi**

- **Tuloksena oleva tila**: pakattu tai osittain pakattu
- **Tuloksena oleva taustajärjestelmän tila**: toimitettu tai osittain toimitettu

**Merkitse pakatuksi** -toiminnolla voidaan ilmaista, että rivit on pakattu ilman pakkausluettelon tulostamista. Sekä **Tulosta pakkausluettelo** että **Merkitse pakatuksi** aiheuttavat varastotapahtumia taustajärjestelmässä. Myyntipisteen pakkausrivit aiheuttavat pakkausluettelon kirjauskansioiden luonnin taustajärjestelmässä.

Jos tilausrivi on pakattu vahingossa, pakkausluettelon kirjauskansio on korjattava taustajärjestelmässä.

Samanaikaisesti voidaan pakata vain saman tilauksen rivejä, joilla on sama toimitustapa.

Tällä hetkellä asetus, jolla myymälän noutorivien tilaksi merkitään **Pakattu**, on poistettu käytöstä. Tämä ominaisuus lisätään tulevissa versioissa. Pakkausluettelon luontiprosessi laajennetaan tukemaan kolmannen osapuolen lähetystietojen lisäämistä pakkausluetteloprosessiin.

### <a name="pick-up"></a>Keräile

Myymälästä noudettavat tilaukset voidaan noutaa suoraan, kun ne on noudettu myyntipisteessä. Myymälän noutotilauksia ei tarvitse hyväksyä.

**Toiminto: nouto**

- **Tuloksena oleva tila**: laskutettu tai osittain laskutettu
- **Tuloksena oleva taustajärjestelmän tila**: laskutettu tai osittain laskutettu

Jos yhdistetystä tilauksen täyttämisestä on valittu rivi noudettava, koko tilaus ladataan myyntipisteeseen ja valitun rivin koko määrä merkitään. Myös muut tilauksen rivit ladataan myyntipisteen tapahtumanäkymään, mutta niiden määräksi on merkitty nolla.

Kun noudon rivit on ladattu tapahtumanäkymään, tapahtuma voidaan veloittaa tavalliseen tapaan.

Jos noudon rivit on laskutettu kokonaan, ne eivät enää näy yhdistetyssä tilauskäsittelyssä. Osittain noudetut rivit näkyvät edelleen yhdistetyssä tilauksen täyttämisessä siihen saakka, ne on noudettu kokonaan.

Jos rivi on noudettu vahingossa, virhe on korjattava tekemällä palautus.

Samanaikaisesti voidaan noutaa vain saman tilauksen rivejä, joilla on sama toimitustapa.

### <a name="shipping"></a>Lähetys

Myymälästä lähetettävät tilausrivit voidaan käsitellä yhdistetyssä tilauksen täyttämisessä **Lähetys**-toiminnolla. Jos manuaalinen tilausrivin hyväksyntä on määritetty kanavatasolla, tilaukset on hyväksyttävä ennen lähetystä. Tilaus voidaan lähettää, kun tilaus on hyväksytty ja sen tilana on **Odottaa** tai jokin muu tila.

**Toiminto: lähetys**

- **Tuloksena oleva tila**: laskutettu tai osittain laskutettu
- **Tuloksena oleva taustajärjestelmän tila**: laskutettu tai osittain laskutettu

Yhdistetystä tilauksen täyttämisestä lähetetyt rivit laskutetaan taustajärjestelmästä samalla tavoin kuin jos tilaus laskutettaisiin suoraan taustajärjestelmästä. Yhdistetystä tilauksen täyttämisestä lähetettäviä rivejä ei ladata tapahtumanäkymään eikä veloitusta suoriteta rivien lähetysajankohtana.

Kokonaisuudessaan lähetetyt tilausrivit eivät enää näy yhdistetyssä tilauksen täyttämisessä. Osittain lähetetyt rivit näkyvät edelleen yhdistetyssä tilauksen täyttämisessä siihen saakka, ne on lähetetty kokonaan.

Samanaikaisesti voidaan toimittaa vain saman tilauksen rivejä. Jos saman tilauksen riveillä on erilaiset toimitustavat, ne voidaan silti valita lähetettäväksi samanaikaisesti.

### <a name="reject"></a>Hylkää

Rivit tai osittaiset rivit voidaan hylätä. Niinpä ne voidaan määrittää taustajärjestelmästä uudelleen toiseen myymälään tai varastoon. Rivit voidaan hylätä vain, jos niitä ei ole vielä kerätty tai pakattu. Jos kerätty tai pakattu rivi halutaan hylätä, kyseisen rivin keräys tai pakkaus on kumottava taustajärjestelmässä.

**Toiminto: hylkää**

- **Tuloksena oleva tila**: hylätty
- **Tuloksena oleva taustajärjestelmän tila**: ei muutosta

Hylättyjä tilausrivejä voi tarkastella **Myyntitilausten käsittely ja kysely** -työtilassa. Voit tarkastella kaikki myymälöiden hylättyjä tilausrivejä tyhjentämällä työtilan henkilösuodattimen. Tilausrivin tiedot näkyvät **Tilaukset ja suosikit** -osan **Hylätyt tilausrivit** -välilehdessä. Käyttäjät voivat siirtyä myyntitilausnäkymässä myös napsauttamalla **Hylätyt tilausrivit** -painiketta **Yhteenveto**-osassa. Näkyviin tulee kaikki myyntitilaukset, joissa on vähintään yksi hylätty tilausrivi. Jos jaettu tilaustenhallinta (DOM) on otettu käyttöön, nämä hylätyt tilaukset määritetään täyttämistä varten automaattisesti uudelleen sopiviin myymälöihin. Nämä tilausrivit voidaan kuitenkin määrittää uudelleen myös manuaalisesti. Voit tehdä sen valitsemalla rivin, joka **Toteutumisen tila** on **Hylätty**, muuttamalla sitten toimipistettä tai varastoa. Napsauta avattavaa **Päivitä rivi** -valikkoa ja valitse **Palauta täytäntöönpanon tila**. Täyttämisen tila **Hylätty** vaihtuu nyt tilauksen täyttämismääritysten mukaan tilaksi **Hyväksytty** tai **Odottaa**. Kun täyttämisen tila on palautettu, myymälän työntekijät voivat tarkastella tilausrivejä myyntipisteessä.

## <a name="line-quantity-tracking"></a>Rivin määrän seuranta

Yksi tilausrivi, jonka määrä on suurempi kuin yksi, voidaan käsitellä ajan mittaan, jolloin seurauksena on useita tilausrivien alitiloja. Jos esimerkiksi rakennuttajalla on projekti, jossa tarvitaan 500 lautaa, mutta rakennuttaja noutaa tai hänelle toimitetaan vain muutamia lautoja kerrallaan projektin kuluessa, määrätietoja voi olla samanaikaisesti keräykselle, pakatuille ja lähetetyille.

Aina kun rivi valitaan, rivin jäljellä oleva määrä täytetään automaattisesti oletuksella, että jäljellä oleva määrä käsitellään. Edellä olevaa esimerkkiä käytettäessä, jos 200 lautaa on jo kerätty ja lautojen rivi valitaan keräystä varten, määräksi täytetään automaattisesti jäljellä oleva määrä, 300. Näin toimitaan myös siinä tapauksessa, että 200 lautaa on jo laskutettu. Siinä tapauksessa vain jäljellä oleva määrä täytetään automaattisesti.

Käytetään edelleen samaa esimerkkiä. Jos valitaan pakatuiksi ja lähetetyiksi merkityt 200 lautaa, koko määrä, 500, täytetään automaattisesti. Jos vain 200 lautaa lähetetään, järjestelmä olettaa, että aiemmin pakatut laudat lähetetään ja pakattujen määrää vähennetään. Jos lähettyjä lautoja on 201, pakatut laudat vähennetään ensin ja järjellä oleva yksi lauta vähennetään jäljellä olevasta määrästä.

## <a name="line-statuses"></a>Rivin tilat

Myyntipisteen tilausriveillä on useita tiloja ilmaisemaan tilausrivin tilaa. Myyntipisteen ja taustajärjestelmän tilat eivät aina vastaa toisiaan. Tilausrivin tilaa voi tarkastella myyntipisteessä tilauksen täyttämistoimintojen avulla. Taustajärjestelmässä tilausrivejä tarkastellaan tilauksen tietojen kautta. Tilauksen tietoihin pääsee valitsemalla **Vähittäismyynti ja kauppa** \> **Asiakkaat** \> **Kaikki asiakastilaukset**. Voit tarkastella tilauksen tietoja valitsemalla **Tilauksen tunnus**. Valitse tilauksen tiedoissa ensin **Myyntitilaus**-välilehti ja sitten **Näytä**-alakohdassa **Tilan tiedot**.

- **Odottaa** – Myymälään määritettyjen tilausrivien, joita ei ole vielä hyväksytty, tila on **Odottaa**, kun niitä tarkastellaan myyntipisteessä. Myyntipisteessä hyväksyntää odottavina näkyvien rivien tila on taustajärjestelmässä **Tilausta käsitellään**.
- **Hyväksytty** – Manuaalisesti tai automaattisesti hyväksyttyjen tilausrivien tila on **Hyväksytty**, kun niitä tarkastellaan myyntipisteessä. Rivien, joiden tila on **Hyväksytty**, tila on taustajärjestelmässä **Tilausta käsitellään**.
- **Keräily** – Myymälätasolla kerättävien rivien tila on **Keräily**. Samojen rivien tila on taustajärjestelmässä tarkasteltaessa **Tilausten käsitteleminen**.
- **Keräilty** ja **Osittain keräilty** – Keräiltyjen tai osittain keräiltyjen rivien tila on myyntipisteessä **Keräilty** tai **Osittain keräilty**. Samojen rivien tila on myös taustajärjestelmässä **Keräilty** tai **Osittain keräilty**.
- **Pakattu** ja **Osittain pakattu** – Pakattujen tai osittain pakattujen rivien tila on myyntipisteessä **Pakattu** tai **Osittain pakattu**. Samojen rivien tila on taustajärjestelmässä **Toimitettu** tai **Osittain toimitettu**.
- **Osittain laskutettu** – osittain noudettujen tai osittain lähetettyjen rivien tila on **Osittain laskutettu** sekä myyntipisteessä että taustajärjestelmässä.
- **Laskutettu** – Myyntipisteessä kokonaan laskutetut rivit eivät enää näy täytettävinä. Taustajärjestelmässä näiden rivien tila on **Laskutettu**.

## <a name="order-fulfillment-filtering"></a>Tilauksen täyttämisen suodatus

Tilauksen täyttäminen myyntipisteessä sisältää suodatuksen, jonka avulla käyttäjien on helppo näyttää tarvitsemansa. Suodattimia voi muuttaa **Myyntipiste**-näytön alareunan toimintoruudussa. Oletusarvoisesti käytössä on **Toimitustyyppi**-suodatin sen mukaan, miten toiminto on määritetty. Jos toiminto on määritetty **Kaikki tilaukset** -parametrilla, tätä suodatinta käytetään tilauksen täyttämistä käytettäessä. Samaa koskee **Nouto myymälästä**- ja **Myymälästä lähetys** -parametria. Muita tilauksen täyttämisen kanssa käytettäviä suodattimia:

- Asiakasnumero
- Asiakkaan nimi
- Asiakkaan sähköpostiosoite
- Tilausnumero
- Toimitustapa
- Kuittinumero
- Kanavan viitetunnus
- Alkuperäinen myymälän numero
- Rivin tila
- Luontipäivämäärä
- Toimituspäivä
- Vastaanottopäivä


[!INCLUDE[footer-include](../includes/footer-banner.md)]