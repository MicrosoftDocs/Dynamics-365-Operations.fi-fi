---
title: Tapahtumasidonnaisten tapahtumien sähköpostimallien luominen
description: Tässä ohjeaiheessa käsitellään tapahtumasidonnaisten tapahtumien sähköpostimallien luontia, lataamista ja määrittämistä Microsoft Dynamics 365 Commercessa.
author: bicyclingfool
ms.date: 10/26/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: stuharg
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 69ba8821cde6788d6e0accb37288f92acdfc776c
ms.sourcegitcommit: 6bf9e18989e6d77497a9dda1c362f324b3c2fbf2
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/27/2021
ms.locfileid: "7713794"
---
# <a name="create-email-templates-for-transactional-events"></a>Tapahtuman tapahtumien sähköpostimallien luominen

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

Tässä ohjeaiheessa käsitellään tapahtumasidonnaisten tapahtumien sähköpostimallien luontia, lataamista ja määrittämistä Microsoft Dynamics 365 Commercessa.

Dynamics 365 Commerce tarjoaa valmiin ratkaisun asiakkaille tapahtumasidonnaisista tapahtumista ilmoittavien sähköpostien lähettämiseen. Sähköpostiviestejä voidaan esimerkiksi, kun tilaus tehdään, se on valmis noudettavaksi tai se on lähetetty. Tässä ohjeaiheessa on ohjeet tapahtumasidonnaisten sähköpostiviestien lähettämiseen käytettyjen sähköpostimallien luomiseen, päivittämiseen ja määrittämiseen.

## <a name="notification-types"></a>Ilmoitustyypit

Ilmoitukset voidaan määrittää ilmoittamaan asiakkaille sähköpostitse, kun tilaus- ja asiakaselinkaaressa tapahtuu tiettyjä tapahtumia. Ilmoitukset voi määrittää suorittamalla yhdistämismäärityksen sähköpostimallin ja ilmoitustyypin välillä luomalla Commercen sähköposti-ilmoitusprofiilin. Tietoja sähköposti-ilmoitusprofiilien määrittämisestä: [Määritä sähköposti-ilmoitusprofiili](email-notification-profiles.md).

Dynamics 365 Commerce tukee seuraavia ilmoitustyyppejä.

### <a name="order-created"></a>Tilaus luotu

*Tilaus luotu* -ilmoitustyyppi käynnistyy, kun Commerce-pääkonttorisovelluksessa luodaan uusi myyntitilaus.

> [!NOTE]
> Tilaus luotu -ilmoitustyyppi ei käynnisty kassapäätteessä esiintyvien itsepalvelutukkutapahtumien osalta. Tällöin luodaan sähköpostitse lähetettävä ja/tai tulostettava kuitti. Lisätietoja: [Sähköpostikuittien lähettäminen Modern POS:stä (MPOS)](email-receipts.md).

### <a name="order-confirmed"></a>Tilaus vahvistettu

*Tilaus vahvistettu* -ilmoitustyyppi käynnistyy, kun Commerce-pääkonttorisovelluksesta luodaan myyntitilauksen tilausvahvistusasiakirja.

### <a name="picking-completed"></a>Kerätty

*Keräily valmis* -ilmoitustyyppi käynnistyy, kun tilauksen keräilyluettelo on merkitty valmiiksi Commerce-pääkonttorisovelluksessa.

> [!NOTE]
> Keräily valmis -ilmoitustyyppi ei käynnisty, kun nimike merkitään keräillyksi kassapäätteessä.

### <a name="packing-completed"></a>Pakattu

*Pakkaus valmis* -ilmoitustyyppi käynnistyy, kun tilauksen pakkausluetteloasiakirja luodaan kassapäätteen Commerce-pääkonttorisovelluksessa.

Pakkaus valmis -ilmoitustyyppi tukee seuraavia ylimääräisiä sähköpostin paikkamerkkejä helpottamaan tilaus valmis noudettavaksi -tapahtumia ja tilausten hakutoimintoa tapahtumasähköposteissa.

| Paikkamerkin nimi    | Tarkoitus |
| ------------------- | ------- |
| `pickupstorename`     | Sen myymälän nimi, josta tilaus on noudettavissa. |
| `pickupstoreaddress`  | Sen myymälän osoite, josta tilaus on noudettavissa. |
| `pickupstorehourfrom` | Noutomyymälän avaamisaika. |
| `pickupstorehourto`   | Noutomyymälän sulkemisaika. |
| `pickupchannelid`     | Noutomyymälän myymälän kanavatunnus. |
| `packingslipid`      | Noudettavan tilauksen pakkausluettelon tunnus. |
| `confirmationid`      | Noudettavan tilauksen tilausvahvistuksen tunnus. (Tätä tunnusta kutsutaan joskus kanavaviitteen tunnukseksi.) |

Lisätietoja asiakkaan sisäänkuittaus- ja tilaushakutoiminnoista: [Maantieteellisen replikoinnin tunnistuksen ja uudelleenohjauksen määrittäminen](geo-detection-redirection.md) ja [Tilaushaun käyttöönotto vierailijoiden uloskuittauksessa](order-lookup-guest.md).

### <a name="order-ready-for-pickup"></a>Tilaus valmis noudettavaksi

*Tilaus valmiina noudettavaksi* -ilmoitustyyppi käynnistyy, kun tilaus merkitään pakatuksi ja toimitustavaksi on määritetty **Asiakasnouto** vähintään yhdellä tilausrivillä.

> [!NOTE]
> Tilaus valmiina noudettavaksi -ilmoitustyyppi on poistettu käytöstä ja korvattu pakkaus valmis -ilmoitustyypillä. Tätä ilmoitustyyppiä voi mukauttaa toimitustavan mukaan.

### <a name="order-shipped"></a>Tilaus lähetetty

*Tilaus lähetetty* -ilmoitustyyppi käynnistyy, kun laskutetaan tilaus, jolla on muut toimitustapa kuin myymälänouto.

> [!NOTE]
> Tilaus lähetetty -ilmoitustyyppi on poistettu käytöstä ja korvattu tilaus laskutettu -ilmoitustyypillä. Tätä ilmoitustyyppiä voi mukauttaa toimitustavan mukaan.

### <a name="order-invoiced"></a>Tilaus laskutettu

*Tilaus laskutettu* -ilmoitustyyppi käynnistyy, kun tilaus laskutetaan kassapäätteellä tai Commerce-pääkonttorisovelluksessa.

### <a name="issue-gift-card"></a>Myönnä lahjakortti

*Myönnä lahjakortti* -ilmoitustyyppi käynnistetään, kun laskutetaan lahjakorttityyppiä olevan tuotteen sisältävä myyntitilaus.

> [!NOTE]
> Lahjakortin myöntämisestä ilmoittava sähköposti lähetetään lahjakortin vastaanottajalle. Lahjakortin vastaanottaja määritetään Commerce-pääkonttorisovelluksessa **Pakkaus**-välilehden **Rivitiedot**-kohdan yksittäisellä myyntitilausrivillä. Sen voi määrittää manuaalisesti tai ohjelmallisesti.

Myönnä lahjakortti -ilmoitustyyppi tukee seuraavia ylimääräisiä paikkamerkkejä.

| Paikkamerkin nimi      | Tarkoitus |
| --------------------- | ------- |
| `giftcardnumber`        | Lahjakortin numero, kun kyseessä on lahjakorttityypin tuotteet. |
| `giftcardbalance`       | Lahjakortin saldo, kun kyseessä on lahjakorttityypin tuotteet. |
| `giftcardmessage`       | Lahjakortin viesti, kun kyseessä on lahjakorttityypin tuotteet. |
| `giftcardpin`         | Lahjakortin henkilökohtainen tunnusluku (PIN), kun kyseessä on lahjakorttityypin tuotteet. (Tämä paikkamerkki koskee vain ulkoisia lahjakortteja.) |
| `giftcardexpiration`    | Lahjakortin vanhentumispäivä, kun kyseessä on lahjakorttityypin tuotteet. (Tämä paikkamerkki koskee vain ulkoisia lahjakortteja.) |
| `giftcardrecipientname` | Lahjakortin vastaanottajan nimi, kun kyseessä on lahjakorttityypin tuotteet. |
| `giftcardbuyername`     | Lahjakortin ostajan nimi, kun kyseessä on lahjakorttityypin tuotteet. |

Lisätietoja lahjakorteista: [Sähköisen kaupankäynnin digitaaliset lahjakortit](digital-gift-cards.md) ja [Ulkoisten lahjakorttien tuki](dev-itpro/gift-card.md).

### <a name="order-cancellation"></a>Tilauksen peruuttaminen

*Tilauksen peruutus* -ilmoitustyyppi käynnistyy, kun tilaus peruutetaan Commerce-pääkonttorisovelluksessa.

### <a name="customer-created"></a>Asiakas on luotu

*Asiakas luotu* -ilmoitustyyppi käynnistyy, kun Commerce-pääkonttorisovelluksessa luodaan uusi asiakasyksikkö.

### <a name="b2b-prospect-approved"></a>B2B-prospekti hyväksytty

*B2B-prospekti hyväksytty* -ilmoitustyyppi käynnistyy, kun prospektin aktivointipyyntö hyväksytään Commerce-pääkonttorisovelluksessa. Lisätietoja B2B-prospektien hyväksymisestä ja hylkäämisestä: [Järjestelmänvalvojakäyttäjän määrittäminen uudelle liikekumppanille](b2b/manage-b2b-users.md#set-up-the-administrator-user-for-a-new-business-partner). 

B2B-prospekti hyväksytty -ilmoitustyyppi tukee seuraavia ylimääräisiä paikkamerkkejä.

| Paikkamerkin nimi | Tarkoitus                                                      |
| ---------------- | ------------------------------------------------------------ |
| `firstname`       | B2B-prospektin etunimi sellaisena kuin se on syötetty sovellukseen. |
| `lastname`         | B2B-prospektin sukunimi sellaisena kuin se on syötetty sovellukseen. |
| `company`          | Hakijan yrityksen nimi sellaisena kuin se on syötetty sovellukseen. |
| `email`            | Prospektin sähköpostiosoite sellaisena kuin se on syötetty sovellukseen.   |
| `zipcode`          | Prospektin ensisijaisen osoitteen postinumero. |
| `comments`         | Kommentti, jonka prospekti on syöttänyt sovellukseen. |
| `storename`        | Sen kanavan nimi, jossa prospekti on luotu. |
| `storeurl`         | Oletusarvoisesti tyhjä. Tätä paikkamerkkiä varten on luotava mukautettu laajennus. |

### <a name="b2b-prospect-approved"></a>B2B-prospekti hyväksytty

*B2B-prospekti hylätty* -ilmoitustyyppi käynnistyy, kun prospektin aktivointipyyntö hylätään Commerce-pääkonttorisovelluksessa. Lisätietoja B2B-prospektien hyväksymisestä ja hylkäämisestä: [Järjestelmänvalvojakäyttäjän määrittäminen uudelle liikekumppanille](b2b/manage-b2b-users.md#set-up-the-administrator-user-for-a-new-business-partner). 

B2B-prospekti hylätty -ilmoitustyyppi tukee seuraavia ylimääräisiä paikkamerkkejä.

| Paikkamerkin nimi | Tarkoitus                                                      |
| ---------------- | ------------------------------------------------------------ |
| `firstname`        | B2B-prospektin etunimi sellaisena kuin se on syötetty sovellukseen. |
| `lastname`         | B2B-prospektin sukunimi sellaisena kuin se on syötetty sovellukseen. |
| `company`          | Hakijan yrityksen nimi sellaisena kuin se on syötetty sovellukseen. |

## <a name="create-an-email-template"></a>Luo sähköpostimalli

Ennen tietyn tapahtumasidonnaisen tapahtuman yhdistämistä sähköpostimalliin on luotava malli.

Voit luoda sähköpostimallin seuraavien ohjeiden avulla.

1. Siirry Commerce Headquarters -sovelluksessa kohtaan **Retail ja Commerce \> Headquarters -sovelluksen määritys \> Organisaation sähköpostimallit** tai **Organisaation hallinta \> Määritys \> Organisaation sähköpostimallit**.
1. Valitse **Uusi**.
1. Määritä seuraavat kentät **Yleiset**-kohdassa:

    - **Sähköpostitunnus** – Sähköpostitunnus on mallin yksilöivä tunnus. Se on arvo, joka näkyy, kun valitset mallin tapahtuman yhdistämismääritystä varten.
    - **Sähköpostin kuvaus** – Tähän valinnaiseen kenttään voi kirjoittaa mallin kuvauksen. Annettava arvo näkyy vain Commercen pääkonttoriosassa.
    - **Lähettäjän nimi** – annettu nimi näkyy useimpien sähköpostiohjelmien Lähettäjä-kentässä.
    - **Lähettäjän sähköposti** – anna sähköpostiosoite, jota käytetään sähköpostien lähettämiseen tätä mallia käytettäessä.
    - **Oletuskielikoodi** – tämä kenttä määrittää oletusarvoisesti lähetetyn sähköpostin lokalisoidun version, jos mallin käynnistävässä kanavassa ei ole määritetty mitään kieltä.

1. Valitse **Sähköpostiviestin sisältö** -kohdassa **Uusi**.
1. Anna sähköpostimallin kieli **Kieli**-kentässä. Voit lisätä muita kieliä ja lokalisoituja malleja myöhemmin.
1. Kirjoita **Aihe**-kenttään sähköpostin aihe, joka näkyy sähköpostin aihekentässä.
1. Lataa sähköpostimalli valitsemalla **Muokkaa**.

## <a name="create-an-email-message-body-by-using-html"></a>Sähköpostiviestin tekstin luonti HTML-koodin avulla

Sähköpostiviestin tekstissä on käytetty HTML-koodia. Voit käyttää mitä tahansa asettelua, tyyliä ja brändäystä, joiden käytön HTML ja CSS-tyylisivut sallivat. Voit käyttää myös kuvia, jos niitä isännöidään julkisesti saatavana olevassa verkkopäätepisteessä. Lisää kuva antamalla kuvan URL-osoite HTML **&lt;img&gt;** -tunnisteen **src**-määritteessä.

> [!NOTE]
> Sähköpostiohjelmissa on asettelu- ja tyylirajoituksia, jotka voivat edellyttää viestin tekstissä käytettävän HTML-koodin ja CSS-tyylisivujen muokkaamista. Tämän vuoksi kannattaa tutustua sellaisen HTML-koodin luomisen parhaisiin käytäntöihin, joita suositut sähköpostiohjelmat tukevat.

## <a name="add-placeholders-to-the-email-message-body"></a>Paikkamerkkien lisääminen sähköpostiviestin tekstiin

Sähköpostiviestissä voi olla paikkamerkkejä, jotka korvataan asiakas- ja tapahtumakohtaisilla arvoilla, kun sähköpostiviesti luodaan. Paikkamerkkien ympärillä on aina prosenttimerkit (%) ja ne lisätään suoraan HTML-tiedostoon.

Esimerkki:

```html
<p>
    Hello %customername%,<br />
    Order number %salesid%, can be picked up from the <b>%pickupstorename%</b> store.
</p>
```

### <a name="order-placeholders-sales-order-level"></a>Tilauksen paikkamerkit (myyntitilaustaso)

Seuraavilla paikkamerkeillä noudetaan ja näytetään tiedot, jotka on määritetty myyntitilaustasolla (eikä myyntirivitasolla).

| Paikkamerkin nimi     | Tarkoitus                                                      |
| -------------------- | ------------------------------------------------------------ |
| `customername`         | Tilauksen tehneen asiakkaan nimi.               |
| `customeraddress`      | Asiakkaan osoite.                                 |
| `customeremailaddress` | Sähköpostiosoite, jonka asiakas on antanut uloskuittauksen aikana.     |
| `salesid`              | Tilauksen myyntitunnus.                                   |
| `orderconfirmationid`  | Tilauksen luonnin yhteydessä luotu kanavien välinen tunnus.   |
| `channelid`            | Sen vähittäismyynti- tai verkkokanavan tunnus, jonka kautta tilaus tehtiin. |
| `deliveryname`         | Toimitusosoitteeksi määritetty nimi.         |
| `deliveryaddress`      | Lähetettyjen tilausten toimitusosoite.                     |
| `deliverydate`         | Toimituspäivä.                                           |
| `shipdate`             | Lähetyspäivä.                                               |
| `modeofdelivery`       | Tilauksen toimitustapa.                              |
| `ordernetamount`       | Tilauksen kokonaissumma ilman veroja.         |
| `discount`            | Tilauksen kokonaisalennus.                            |
| `charges`              | Tilauksen kokonaiskulut.                             |
| `tax`                  | Tilauksen verot yhteensä.                                 |
| `total`                | Tilauksen kokonaissumma.                              |
| `storename`            | Sen myymälän nimi, jossa tilaus tehtiin.            |
| `storeaddress`         | Tilauksen tehneen myymälän osoite.              |
| `storeopenfrom`        | Tilauksen tehneen myymälän avaamisaika.         |
| `storeopento`          | Tilauksen tehneen myymälän sulkemisaika.         |
| `pickupstorename`      | Sen myymälän nimi, josta tilaus noudetaan.\*   |
| `pickupstoreaddress`   | Sen myymälän osoite, josta tilaus noudetaan.\* |
| `pickupopenstorefrom`  | Sen myymälän avaamisaika, josta tilaus noudetaan.\* |
| `pickupopenstoreto`    | Sen myymälän sulkemisaika, josta tilaus noudetaan.\* |
| `pickupchannelid`     | Se määritetty myymälän kanavatunnus, kun toimitustapana on nouto.\* |
| `packingslipid`        | Sen pakkausluettelon tunnus, joka luotiin, kun tilauksen rivit pakattiin.\* |

\* Nämä paikkamerkit palauttavat tietoja vain, kun niitä käytetään **Tilaus valmis noudettavaksi** -ilmoitustyypissä. 

### <a name="order-line-placeholders-sales-line-level"></a>Tilausrivin paikkamerkit (myyntirivitaso)

Seuraavilla paikkamerkeillä noudetaan ja näytetään myyntitilauksen yksittäisten tuotteiden (rivien) tiedot.

| Paikkamerkin nimi               | Tarkoitus |
|--------------------------------|-------------------|
| `productid`                      | <p>Tuotteen tunnus. Tämä on varianttien tunnus.</p><p><strong>Huomautus</strong>: tämä paikkamerkki on vanhentunut, ja sen tilalla on `lineproductrecid`.</p> |
| `lineproductrecid`               | Tuotteen tunnus. Tämä on varianttien tunnus. Se tunnistaa nimikkeen yksilöivästi varianttitasolla. |
| `lineitemid`                     | Tuotteen tuotantotason tunnus. (Tämä ei ole varianttien tunnus.) |
| `lineproductvariantid`           | Tuotevariantin tunnus. |
| `lineproductname`                | Tuotteen nimi. |
| `lineproductdescription`         | Tuotteen kuvaus. |
| `linequantity`                   | Riville tilattujen yksikköjen määrä sekä mittayksikkö (kuten **kpl** tai **pari**). |
| `lineunit`                       | Rivin mittayksikkö. |
| `linequantity_withoutunit`       | Riville tilattujen yksikköjen määrä ilman mittayksikköä. |
| `linequantitypicked`             | **PickOrder**-tapahtumaa käytettäessä kerättyjen yksiköiden määrä. Muussa tapauksessa **0** (nolla). |
| `linequantitypicked_withoutunit` | **PickOrder**-tapahtumaa käytettäessä kerättyjen yksiköiden määrä ilman mittayksikköä. Muussa tapauksessa **0** (nolla). |
| `linequantitypacked`             | **PackOrder**- ja **Tilaus valmis noudettavaksi** -tapahtumia käytettäessä pakattujen yksiköiden määrä. Muussa tapauksessa **0** (nolla). |
| `linequantitypacked_withoutuom`  | **PackOrder**- ja **Tilaus valmis noudettavaksi** -tapahtumia käytettäessä pakattujen yksiköiden määrä ilman mittayksikköä. Muussa tapauksessa **0** (nolla). |
| `linequantityshipped`            | Aina **0** lukuun ottamatta seuraavalla rivillä kuvattavia erikoistapahtumia käytettäessä. |
| `linequantityshipped_withoutuom` | **ShipOrder**-tapahtumaa käytettäessä kerättyjen yksiköiden määrä ilman mittayksikköä. Muussa tapauksessa **0** (nolla). |
| `lineprice`                      | Yhden yksikön hinta. |
| `linenetamount`                  | Rivin hinta sen jälkeen, kun yksikkömäärä ja alennus on käytetty. |
| `linediscount`                   | Yksittäisen yksikön alennus. |
| `lineshipdate`                   | Rivin lähetyspäivä. |
| `linedeliverydate`               | Rivin toimituspäivä. |
| `linedeliverymode`               | Rivin toimitustapa. |
| `linedeliveryaddress`            | Rivin toimitusosoite. |
| `linepickupdate`                 | Asiakkaan määrittämä noutopäivämäärä tilauksille, joissa toimitustapana on nouto. |
| `linepickuptimeslot`             | Asiakkaan määrittämä noutoaikaväli tilauksille, joissa toimitustapana on nouto. |
| `giftcardnumber`                 | Lahjakortin numero, kun kyseessä on lahjakorttityypin tuotteet. |
| `giftcardbalance`                | Lahjakortin saldo, kun kyseessä on lahjakorttityypin tuotteet. |
| `giftcardmessage`                | Lahjakortin viesti, kun kyseessä on lahjakorttityypin tuotteet. |
| `giftcardpin`                    | Lahjakortin PIN, kun kyseessä on lahjakorttityypin tuotteet. (Tämä paikkamerkki koskee vain ulkoisia lahjakortteja.) |
| `giftcardexpiration`             | Lahjakortin vanhentumispäivä, kun kyseessä on lahjakorttityypin tuotteet. (Tämä paikkamerkki koskee vain ulkoisia lahjakortteja.) |
| `giftcardrecipientname`          | Lahjakortin vastaanottajan nimi, kun kyseessä on lahjakorttityypin tuotteet. |
| `giftcardbuyername`              | Lahjakortin ostajan nimi, kun kyseessä on lahjakorttityypin tuotteet. |

### <a name="format-of-order-line-placeholders-in-the-email-message-body"></a>Tilausrivin paikkamerkkien muoto sähköpostiviestin tekstissä

Kun yksittäiselle tilausriville luodaan HTML-koodi sähköpostiviestin tekstissä, aseta rivien toistuville HTML- ja paikkamerkkilohkojen ympärille seuraavat paikkamerkit. Huomaa, että paikkamerkit ovat HTML-kommenttitunnisteiden sisällä.

```html
<!--%tablebegin.salesline%-->

(Insert the repeating block of HTML and placeholders for individual lines here.)

<!--%tableend.salesline%-->
```

Esimerkki:

```HTML
<table>
    <tr>
        <td>Product name</td>
        <td>Quantity</td>
        <td>Price</td>
    </tr>
    <!--%tablebegin.salesline%-->
    <tr>
        <td>%lineproductname%</td>
        <td>%linequantity_withoutunit%</td>
        <td>%lineprice%</td>
    </tr>
    <!--%tableend.salesline%-->
</table>
```

## <a name="create-a-template-for-emailed-receipts"></a>Sähköpostitse lähetettävien kuittien mallin luominen

Kuitit voidaan lähettää sähköpostitse asiakkaille, jotka tekevät ostoksia vähittäismyymälässä. Yleisesti ottaen sähköpostitse lähetettävän kuittimallin luontivaiheet ovat samat kuin muiden tapahtumasidonnaisten tapahtumien mallien luonnissa. Seuraavat muutokset on kuitenkin tehtävä:

- **%message%**-paikkamerkkiä käytetään kuitin tekstin sähköpostiin lisäämiseen. Kuitin tekstin oikea hahmonnus varmistetaan asettamalla **%message%**-paikkamerkin ympärille HTML-tunnisteet **&lt;pre&gt;** ja **&lt;/pre&gt;**.
- **%receiptid%**-paikkamerkkiä voidaan käyttää näyttämään kuitin tunnusta vastaavan QR-koodin tai viivakoodin. (QR-koodit ja viivakoodit luodaan dynaamisesti, ja niitä voi tuottaa kolmannen osapuolen palvelu.) Lisätietoja siitä, miten sähköpostilla postitetussa kuitissa näytetään QR-koodi tai viivakoodi, on kohdassa [QR-koodin tai viivakoodin lisääminen tapahtuma- tai kuittisähköposteihin](add-qr-code-barcode-email.md).

## <a name="upload-the-email-html"></a>Sähköpostin HTML-koodin lataaminen

Kun viestin tekstin HTML-koodi on luotu ja testattu, se on ladattava Commercen pääkonttoriosaan. Tällä hetkellä sähköpostin HTML-koodi ei voi viedä. Tämän vuoksi HTML-koodin pääkopiota on ylläpidettävä Commercen pääkonttoriosan ulkopuolella.

Lataa uusi tai muokattu sähköpostimallin HTML-koodi seuraavasti:

1. Valitse Commercen pääkonttoriosassa **Vähittäismyynti ja kauppa \> Pääkonttorin asetukset \> Organisaation sähköpostimallit**.
1. Valitse sen kielen rivi, jonka HTML-koodin haluat lisätä tai korvata. Vaihtoehtoisesti voit luoda rivin uudelleen kielelle valitsemalla **Uusi**.
1. Valitse **Muokkaa**.
1. Valitse avautuvassa valintaikkunassa **Selaa**. Siirry ladattavaan HTML-tiedostoon, valitse se ja valitse sitten **Avaa**.
1. Valitse **Lataa palvelimeen**.
1. Kun sähköpostin HTML näkyy esikatseluikkunassa, valitse **OK**.
1. Varmista, että rivin **Leipäteksti on** -valintaruutu on valittu.

Jos Commercen pääkonttoriosa on jo määritetty lähettämään sähköpostia, uusi tai päivitetty sähköposti lähetetään kaikille asiakkaille, jotka suorittavat malliin yhdistetyn tapahtuman käynnistävän tapahtuman.

Lisätietoja sähköpostien määrittämisestä Dynamics 365 Commercessa on kohdassa [Sähköpostiviestin määrittäminen ja lähettäminen](../fin-ops-core/fin-ops/organization-administration/configure-email.md).

## <a name="additional-resources"></a>Lisäresurssit 

[Sähköposti-ilmoitusprofiilin määrittäminen](email-notification-profiles.md)

[Sähköpostiviestin määrittäminen ja lähettäminen](../fin-ops-core/fin-ops/organization-administration/configure-email.md)

[Aseta sähköpostikuitit](/dynamicsax-2012/appuser-itpro/set-up-email-receipts)

[Sähköpostikuittien lähettäminen Modern POS:stä ](email-receipts.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
