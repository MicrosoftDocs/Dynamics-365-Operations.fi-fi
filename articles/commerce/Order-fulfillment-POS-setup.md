---
title: Myymälöiden tilauksen täyttämisen määrittäminen
description: Tässä aiheessa käsitellään myymälän tilauksen täyttämisen määrittämistä.
author: rubencdelgado
manager: AnnBe
ms.date: 10/30/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailStoreTable, RetailTillLayout
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.search.industry: retail
ms.author: rubendel
ms.search.validFrom: 2017-10-30
ms.dyn365.ops.version: ''
ms.openlocfilehash: 8d6cfa0d1eba4ccb0b24839b7cc632835b17107e
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/15/2021
ms.locfileid: "4965309"
---
# <a name="set-up-order-fulfillment-for-stores"></a>Myymälöiden tilauksen täyttämisen määrittäminen

[!include [banner](includes/banner.md)]

## <a name="overview"></a>Yleiskuvaus

Monet jälleenmyyjät haluaisivat optimoida tilausten täyttämisen antamalla myymälöille mahdolliseen täyttää tilauksia. Tilauksen täyttäminen myymälätasolla voi helpottaa yksittäisten myymälöiden liian suuria varastoja. Se voi olla tarpeellista myös logistiikan vuoksi tilanteissa, joissa myymälässä on ylimääräistä tilaa tai joissa se sijaitsee toimituksen kannalta lähempänä asiakasta. Näitä tarpeita varten myyntipisteissä voi käytätä yhdistettyä tilausten täyttämistoimintoa.

Tietyssä myymälässä täytettävien tilausten varastoa ilmoitetaan tilauksen otsikossa tai tilausriveillä.

Myyntipisteen tilauksen täyttämistoiminto on yhtenäinen myyntipisteen työalue, jossa tilaukset voidaan käsitellä myyntipisteessä. Käsiteltäviä toimintoja ovat niin tilauksen hyväksyminen, tilauksen merkitseminen lähetetyksi kuin myymälästä noudon käynnistäminen.

## <a name="set-up-the-order-fulfillment-operation"></a>Tilauksen täyttämistoiminnon määrittäminen

Tilauksen täyttämisen, [toimintotunnus 928](https://docs.microsoft.com/dynamics365/unified-operations/retail/pos-operations), avulla voidaan käyttää myymälän tilauksen täyttämisen työaluetta myyntipisteessä.

Määritä parametri, jolla tilauksen täyttäminen aktivoidaan myyntipisteessä, kohdan [Toiminnon lisääminen painikeruudukkoon](https://docs.microsoft.com/dynamics365/unified-operations/retail/pos-screen-layouts) ohjeiden mukaisesti. Kun tilauksen täyttämistoiminnot on määritetty **Kaikki tilaukset** on oletusarvoisesti valittuna. Kun määritys on tehty tällä parametrilla, toiminto lisää luetteloon kaikki valitun myymälän täytettävät tilausrivit. Valittavana on myös **Lähetettävät tilaukset**, joka voidaan määrittää painikkeeseen ja jota käytetään, kun käyttäjä haluaa nähdä vain myymälästä lähetettävät tilaukset. Lisäksi valittavana on **Noudettavat tilaukset**. Kun aktivointi tehdään myyntipisteessä, tässä luettelossa näkyy myymälästä noudettavat tilaukset. Koska eri painikkeille voidaan määrittää eri parametri, käyttäjä voi tarkastella tilauksen täyttämistä eri tavoin.

### <a name="enable-users-to-access-order-fulfillment-at-the-point-of-sale"></a>Tilauksen täyttämisen ottaminen käyttöön myyntipisteessä käyttäjien osalta

Tilauksen täyttämistoiminnon käyttöoikeudet eivät ole heti käytössä, mutta käyttäjät voivat edellyttää tulevaisuudessa toiminnon aktivointia myyntipisteestä **Salli tilauksen noutaminen** -käyttöoikeudella.

Myymälätasolla on määritysasetus, jolla voidaan määrittää, onko tilausrivi hyväksyttävä manuaalisesti myyntipisteestä. Jos tätä määritysasetusta ei ole määritetty, tilausrivit hyväksytään oletusarvoisesti. Jos tämä määritysasetus on otettu käyttöön, tilauksien hyväksyminen myyntipisteestä edellyttää, että myyntipisteen käyttäjillä on **Salli tilauksen hyväksyminen** -käyttöoikeus.

### <a name="enable-manual-order-acceptance"></a>Manuaalisen tilauksen hyväksymisen ottaminen käyttöön

Myymälään määritetyt tilausrivit on oletusarvoisesti merkitty **hyväksytyiksi**. Tällöin oletetaan, että ne täytetään määritetystä myymälästä eikä niitä määritetä enää uudelleen. Joissakin tapauksissa jälleenmyyjät voivat kuitenkin haluta hyväksyä tilaukset manuaalisesti ennen täyttämistä. Jos myymälässä ei ole esimerkiksi riittävästi työntekijöitä eikä tilausta voida täyttää, myymäläpäällikkö hyväksyy käsiteltäväksi vain niin monta tilausta kuin voidaan olettaa voitavan käsitellä tiettynä päivänä. Taustajärjestelmä on voi määrittää tilauksen toiseen myymälään tilauksen hyväksymiseen saakka. Niinpä tilauksen hyväksyntä on myös tapa ilmaista, että myymälä on kuitannut tilauksen ja että se täytetään.

Myymälästä noudettavat tilausrivit merkitään **odottaviksi** eikä niitä hyväksytä.

Voit ottaa tilausrivien manuaalisen hyväksymisen käyttöön valitsemalla **Retail ja Commerce** \> **Kanavat** \> **Myymälät** \> **Kaikki myymälät**. Valitse myymälä. Voit tarkastella myymälän tietoja napsauttamalla myymälätunnusta. Valitse **Muokkaa**. Etsi **Yleiset**-pikavälilehdessä **Tilauksen täyttäminen** -alaotsikko ja vaihda **Manuaalinen hyväksyminen** -asetukseksi **Kyllä** **Ei**-vaihtoehdon sijaan.

### <a name="enable-reject-order-line-capability"></a>Tilausrivin hylkäysominaisuuden ottaminen käyttöön

Tilausrivit voidaan myös hylätä myyntipisteestä. Tilausrivi hylkääminen tarkoittaa, että sitä ei täytetä kyseisessä myymälässä. Lisäksi tilausrivi lähetetään määritettäväksi uudelleen toiseen myymälään tai varastoon. Tilausrivin hylkäysoikeus myönnetään työntekijään liitetyn myyntipisteen käyttöoikeusryhmän **Salli tilauksen hylkäys** -käyttöoikeudella. Jälleenmyyjä voi edellyttää, että työntekijät ilmoittavat, minkä vuoksi rivi on hylätty. Se voidaan tehdä käyttämällä **Tietokoodin tehtävä** -tietokoodin **Tilauksen täyttäminen** -tyyppiä ja määrittämällä kanavaan liitetyssä toimintoprofiilissa infokoodiksi **Hylkää tilausrivi**.

> [!NOTE]
> Vain **Tietokoodin tehtävä** -tietokoodin **Tilauksen täyttäminen** -tyyppi voidaan määrittää **Hylkää tilausrivi** -toiminnossa.

### <a name="synchronize-changes-to-the-channel-database"></a>Muutosten synkronoiminen kanavatietokantaan

Kun toiminto on määritetty painikeruudukkoon, soveltuvat käyttöoikeudet on myönnetty ja kanava on määritetty, kanava on synkronoitava kanavatietokantaan. Tehdäksesi näin, mene kohtaan **Retail ja Commerce** \> **Retail ja Commerce IT** \> **Jakeluaikataulu**. Synkronoi painikeruudukko muutokset valitsemalla 1090, kassakoneet ja valitse sitten **Suorita nyt**. Synkronoi seuraavaksi käyttöoikeuksien muutokset valitsemalla ensin 1060, henkilökunta ja sitten **Suorita nyt**. Synkronoi sitten kanava muutokset valitsemalla ensin 1070, Kanavan konfigurointi ja sitten **Suorita nyt**. Synkronoi lopuksi juuri luotu hylkäyssyyn tietokoodi valitsemalla 1110, yleinen konfiguraatio ja sitten **Suorita nyt**.

## <a name="use-order-fulfillment-at-the-point-of-sale"></a>Tilauksen täyttämisen käyttäminen myyntipisteessä

Avaa myyntipiste ja valitse tilauksen täyttämistoiminto. Luettelo sisältää määritysten mukaan joko kaikki rivit, noudettavat tilausrivit tai lähetettävät tilausrivit.

### <a name="order-fulfillment-view"></a>Tilauksen täyttämisnäkymä

Tilauksen täyttämisnäkymässä on luettelo myymälässä täytettävistä tilausriveistä. Näkymässä on seuraavat sarakkeet:

- Tilausnumero
- Tuotenumero
- kuvaus
- Tilattu määrä
- Pyydetty toimituspäivämäärä
- Asiakkaan nimi
- Toteutumisen tila

Lisätietoja tietystä tilausrivistä voi tarkastella valitsemalla tilausrivi ja avaamalla sitten lisätietoikkuna, joka sijaitsee myyntipisteen otsikossa näytettävän kirjautuneen käyttäjän tai vuorotietojen alapuolella. Lisätietoikkunassa on kaksi välilehteä: toisessa on rivin ja toisessa tilauksen tiedot. Rivitietojen välilehdessä on seuraavat tiedot:

- Tilattu määrä
- Jäljellä oleva lähettämistä tai noutoa odottava määrä
- Kerätty määrä
- Pakattu määrä
- Laskutettu määrä (noudettu tai lähetetty määrä)
- Toimitustapa
- Toimitusosoite

Lisätietoikkunassa on myös välilehti, jossa on esimerkiksi seuraavat tarkat tilaustason tiedot:

- Asiakkaan nimi
- Asiakastunnus
- Tilausnumero
- Tilauksen kokonaissumma
- Tilauksen saldo

Tilauksen täyttämisnäkymän alareunassa on toimintoruutu. Se sisältää kaikki toiminnot, joita tilausrivillä voidaan tehdä. Jos toimintoa ei voi käyttää rivin tilan vuoksi, toiminto ei ole käytettävissä.

Kaikkien tilausten tila on oletusarvoisesti **Hyväksytty**. Tilauksen tilaa voi tarkastella tilausriviluettelon sarakkeena. Jos **Manuaalinen hyväksyminen** on määritetty kanavatasolla, kaikkien lähettävien rivien tilana on **Odottaa** ja ne on hyväksyttävä, ennen kuin ne voidaan täyttää. Myymälästä noudettavien tilausten tila on oletusarvoisesti **Odottaa** eikä niitä tarvitse hyväksyä

### <a name="order-fulfillment-line-actions"></a>Tilauksen täyttämisen rivitoiminnot

- **Muokkaa** – Jos tilauksen tila on odottaa, sitä voidaan muokata myyntipisteessä. Osittain kerättyjä, pakattuja tai laskutettuja tilauksia ei voi muokata tilauksen täyttämisnäkymästä.
- **Hyväksy** – jos **Manuaalinen hyväksyminen** määritetään kanavatasolla, rivit on hyväksyttävä, ennen kuin ne voivat siirtyä tilauksen täyttämisprosessissa.
- **Keräilyt** – Keräilyasetus tukee useita toimintoja. Ensiksikin **Keräys** päivittää tilausrivin tilan, jotta kukaan muu ei yritä kerätä myymälässä samaa riviä. Seuraavaksi **Tulosta keräysluettelo** tulostaa valittujen rivien keräysluettelon ja päivittää myös niiden tilaksi **Keräys**. Keräysluettelomuotoja hallitaan kuittimuotojen osana. Lisätietoja kuittimuotojen määrittämisestä on kohdassa [Kuittimallit ja tulostaminen](https://docs.microsoft.com/dynamics365/unified-operations/retail/receipt-templates-printing). Lopuksi **Merkitty kerätyksi** ilmaisee, että rivi on kerätty. **Merkitty kerätyksi** käynnistää vastaavat varastotapahtumat taustajärjestelmässä. Keräystoimintoja voi suorittaa samanaikaisesti useissa tilauksissa ja useilla riveillä toimitustavasta riippumatta.
- **Hylkää** – Rivit tai osittaiset rivit voidaan hylätä. Niinpä ne voidaan määrittää taustajärjestelmästä uudelleen toiseen myymälään tai varastoon. Rivit voidaan hylätä vain, jos niitä ei ole vielä kerätty tai pakattu. Jos kerätty tai pakattu rivi halutaan hylätä, kyseisen rivin keräys tai pakkaus on kumottava taustajärjestelmässä.
- **Pakkaa** – Pakkausasetus tukee kahta toimintoa: **Tulosta pakkausluettelo** tulostaa valittujen rivien pakkausluettelon ja **Merkitse pakatuksi** merkitsee rivit pakatuiksi ja toimitetuiksi taustajärjestelmässä. Samanaikaisesti voidaan pakata vain saman tilauksen rivejä, joilla on sama toimitustapa. Pakkausluettelomuotoja hallitaan kuittimuotojen osana. Lisätietoja kuittimuotojen määrittämisestä on kohdassa [Kuittimallit ja tulostaminen](https://docs.microsoft.com/dynamics365/unified-operations/retail/receipt-templates-printing).
- **Lähetä** – Lähetystoiminto merkitsee valitut rivit **toimitetuiksi** taustajärjestelmässä. Kun rivi on kokonaan lähetetty, se ei enää näy tilauksen täyttämisnäkymässä.
- **Nouto** – Noutotoiminto lisää rivit tapahtumanäkymään noudettaviksi. Jos tilauksessa on muita rivejä, joita ei olla nyt noutamassa, ne lisätään tapahtumanäkymään siten, että niiden määrä on nolla. Kun rivi on kokonaan noudettu, se ei enää näy tilauksen täyttämisnäkymässä.

### <a name="order-fulfillment-filtering"></a>Tilauksen täyttämisen suodatus

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