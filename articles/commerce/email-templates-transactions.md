---
title: Tapahtumasidonnaisten tapahtumien sähköpostimallien luominen
description: Tässä ohjeaiheessa käsitellään tapahtumasidonnaisten tapahtumien sähköpostimallien luontia, lataamista ja määrittämistä Microsoft Dynamics 365 Commercessa.
author: bicyclingfool
manager: annbe
ms.date: 03/01/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: stuharg
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 756e2a64ef4c33c347106968eb6bc79a413c3ff7
ms.sourcegitcommit: 88babb2fffe97e93bbde543633fc492120f2a4fc
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/06/2021
ms.locfileid: "5555242"
---
# <a name="create-email-templates-for-transactional-events"></a>Tapahtuman tapahtumien sähköpostimallien luominen

[!include [banner](includes/banner.md)]

Tässä ohjeaiheessa käsitellään tapahtumasidonnaisten tapahtumien sähköpostimallien luontia, lataamista ja määrittämistä Microsoft Dynamics 365 Commercessa.

## <a name="overview"></a>Yleiskuvaus

Dynamics 365 Commerce on valmis ratkaisu sellaisten sähköpostien lähettämiseen, jotka ilmoittavat asiakkaille tapahtumasidonnaisista tapahtumista (kuten tilauksen tekemisestä, noutamista odottavasta tilauksesta tai lähetetystä tilauksesta). Tässä ohjeaiheessa on ohjeet tapahtumasidonnaisten sähköpostiviestien lähettämiseen käytettyjen sähköpostimallien luomiseen, päivittämiseen ja määrittämiseen.

## <a name="create-an-email-template"></a>Luo sähköpostimalli

Ennen tietyn tapahtumasidonnaisen tapahtuman yhdistämistä sähköpostimalliin on luotava malli.

Voit luoda sähköpostimallin seuraavien ohjeiden avulla.

1. Siirry Commerce Headquarters -sovelluksessa kohtaan **Retail ja Commerce \> Headquarters -sovelluksen määritys \> Organisaation sähköpostimallit** tai **Organisaation hallinta \> Määritys \> Organisaation sähköpostimallit**.
1. Valitse **Uusi**.
1. Määritä seuraavat kentät **Yleiset**-kohdassa:

    - **Sähköpostitunnus** – sähköpostitunnus on mallin yksilöivä tunniste ja arvo, joka näytetään, kun tapahtumaan yhdistettävä malli valitaan.
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

| Paikkamerkin nimi     | Paikkamerkin arvo                                            |
| -------------------- | ------------------------------------------------------------ |
| customername         | Tilauksen tehneen asiakkaan nimi.               |
| salesid              | Tilauksen myyntitunnus.                                   |
| deliveryaddress      | Lähetettyjen tilausten toimitusosoite.                     |
| customeraddress      | Asiakkaan osoite.                                 |
| customeremailaddress | Sähköpostiosoite, jonka asiakas on antanut uloskuittauksen aikana.     |
| deliverydate         | Toimituspäivä.                                           |
| shipdate             | Lähetyspäivä.                                               |
| modeofdelivery       | Tilauksen toimitustapa.                              |
| kulut              | Tilauksen kokonaiskulut.                             |
| vero                  | Tilauksen verot yhteensä.                                 |
| yhteensä                | Tilauksen kokonaissumma.                              |
| ordernetamount       | Tilauksen kokonaissumma ilman veroja.         |
| alennus             | Tilauksen kokonaisalennus.                            |
| storename            | Sen myymälän nimi, jossa tilaus tehtiin.            |
| storeaddress         | Tilauksen tehneen myymälän osoite.              |
| storeopenfrom        | Tilauksen tehneen myymälän avaamisaika.         |
| storeopento          | Tilauksen tehneen myymälän sulkemisaika.         |
| pickupstorename      | Sen myymälän nimi, josta tilaus noudetaan.     |
| pickupstoreaddress   | Sen myymälän osoite, josta tilaus noudetaan.  |
| pickupopenstorefrom  | Sen myymälän avaamisaika, josta tilaus noudetaan. |
| pickupopenstoreto    | Sen myymälän sulkemisaika, josta tilaus noudetaan. |

### <a name="order-line-placeholders-sales-line-level"></a>Tilausrivin paikkamerkit (myyntirivitaso)

Seuraavilla paikkamerkeillä noudetaan ja näytetään myyntitilauksen yksittäisten tuotteiden (rivien) tiedot.

| Paikkamerkin nimi               | Paikkamerkin arvo |
|--------------------------------|-------------------|
| productid                      | Rivin tuotetunnus. |
| lineproductname                | Tuotteen nimi. |
| lineproductdescription         | Tuotteen kuvaus. |
| linequantity                   | Riville tilattujen yksikköjen määrä sekä mittayksikkö (kuten **kpl** tai **pari**). |
| lineunit                       | Rivin mittayksikkö. |
| linequantity_withoutunit       | Riville tilattujen yksikköjen määrä ilman mittayksikköä. |
| linequantitypicked             | **PickOrder**-tapahtumaa käytettäessä kerättyjen yksiköiden määrä. Muussa tapauksessa **0** (nolla). |
| linequantitypicked_withoutunit | **PickOrder**-tapahtumaa käytettäessä kerättyjen yksiköiden määrä ilman mittayksikköä. Muussa tapauksessa **0** (nolla). |
| linequantitypacked             | **PackOrder**- ja **Tilaus valmis noudettavaksi** -tapahtumia käytettäessä pakattujen yksiköiden määrä. Muussa tapauksessa **0** (nolla). |
| linequantitypacked_withoutuom  | **PackOrder**- ja **Tilaus valmis noudettavaksi** -tapahtumia käytettäessä pakattujen yksiköiden määrä ilman mittayksikköä. Muussa tapauksessa **0** (nolla). |
| linequantityshipped            | Aina **0** lukuun ottamatta seuraavalla rivillä kuvattavia erikoistapahtumia käytettäessä. |
| linequantityshipped_withoutuom | **ShipOrder**-tapahtumaa käytettäessä kerättyjen yksiköiden määrä ilman mittayksikköä. Muussa tapauksessa **0** (nolla). |
| lineprice                      | Yhden yksikön hinta. |
| linenetamount                  | Rivin hinta sen jälkeen, kun yksikkömäärä ja alennus on käytetty. |
| linediscount                   | Yksittäisen yksikön alennus. |
| lineshipdate                   | Rivin lähetyspäivä. |
| linedeliverydate               | Rivin toimituspäivä. |
| linedeliverymode               | Rivin toimitustapa. |
| linedeliveryaddress            | Rivin toimitusosoite. |
| giftcardnumber                 | Lahjakortin numero, kun kyseessä on lahjakorttityypin tuotteet. |
| giftcardbalance                | Lahjakortin saldo, kun kyseessä on lahjakorttityypin tuotteet. |
| giftcardmessage                | Lahjakortin viesti, kun kyseessä on lahjakorttityypin tuotteet. |
| giftcardpin                    | Lahjakortin henkilökohtainen tunnusluku (PIN), kun kyseessä on lahjakorttityypin tuotteet. (Tämä paikkamerkki koskee vain ulkoisia lahjakortteja.) |
| giftcardexpiration             | Lahjakortin vanhentumispäivä, kun kyseessä on lahjakorttityypin tuotteet. (Tämä paikkamerkki koskee vain ulkoisia lahjakortteja.) |
| giftcardrecipientname          | Lahjakortin vastaanottajan nimi, kun kyseessä on lahjakorttityypin tuotteet. |
| giftcardbuyername              | Lahjakortin ostajan nimi, kun kyseessä on lahjakorttityypin tuotteet. |

### <a name="format-of-order-line-placeholders-in-the-email-message-body"></a>Tilausrivin paikkamerkkien muoto sähköpostiviestin tekstissä

Kun yksittäiselle tilausriville luodaan HTML-koodi sähköpostiviestin tekstissä, aseta rivien toistuville HTML- ja paikkamerkkilohkojen ympärille seuraavat HTML-kommenttitunnisteiden paikkamerkit.

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

- Kuitin teksti lisätään sähköpostiin **%message%**-paikkamerkin avulla. Kuitin tekstin oikea hahmonnus varmistetaan asettamalla **%message%**-paikkamerkin ympärille HTML-tunnisteet **&lt;pre&gt;** ja **&lt;/pre&gt;**.
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

[Aseta sähköpostikuitit](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-up-email-receipts)

[Sähköpostikuittien lähettäminen Modern POS:stä ](email-receipts.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
