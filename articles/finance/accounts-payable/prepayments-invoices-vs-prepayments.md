---
title: Ennakkomaksulaskujen ja ennakkomaksujen vertailu
description: Tässä ohjeaiheessa kuvaillaan ja vertaillaan kahta menetelmää, joita organisaatiot voivat käyttää ennakkomaksuihin.
author: abruer
ms.date: 10/26/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerJournalTransVendPaym, PurchTable
audience: Application User
ms.reviewer: twheeloc
ms.custom: 15871
ms.assetid: a0bb5220-73d4-48ae-84d0-46a171c224fa
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f05f1d8d2a1fb454f3f227d2cc8138f2b779ff87
ms.sourcegitcommit: 1d2eeacad11c28889681504cdc509c90e3e8ea86
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/05/2022
ms.locfileid: "8716322"
---
# <a name="prepayment-invoices-vs-prepayments"></a>Ennakkomaksulaskujen ja ennakkomaksujen vertailu

[!include [banner](../includes/banner.md)]

Tässä ohjeaiheessa kuvaillaan ja vertaillaan kahta menetelmää, joita organisaatiot voivat käyttää ennakkomaksuihin. Yksi menetelmä luo ennakkomaksulaskun, joka on liitetty ostotilaukseen. Toinen menetelmä luo ennakkomaksukirjauskansion tositteita luomalla kirjauskansiovientejä ja merkitsemällä ne ennakkomaksukirjauskansion tositteiksi.

Yritykset saattavat suorittaa ennakkomaksuja toimittajille tavaroista tai palveluista jo ennen niiden toimittamista. Ennakkomaksuja voidaan suorittaa toimittajille kahdella tavalla. Riskien minimoimiseksi ennakkomaksuja voi seurata määrittämällä ennakkomaksun ostotilaukselle. Tällöin on luotava ennakkomaksulasku, joka on liitetty ostotilaukseen. Tätä menetelmää kutsutaan ennakkomaksun laskuttamiseksi. Yritykset, jotka eivät halua seurata ennakkomaksuja kovin tarkasti tai eivät saa toimittajalta ennakkomaksulaskuja, voivat käyttää ennakkomaksujen laskutusmenetelmän sijaan ennakkomaksukirjauskansion tositteita. Ennakkomaksukirjauskansion tositteita voi luoda luomalla kirjauskansiovientejä ja merkitsemällä ne ennakkomaksukirjauskansion tositteiksi. Tässä menetelmässä ei voi seurata, mitkä ennakkomaksut toimittajalle vastaavat mitäkin ostotilausta. Voit kuitenkin merkitä kirjatun ennakkomaksun tilitettäväksi ostotilausta vastaan.

## <a name="when-to-use-prepayment-invoicing-vs-prepayments"></a>Milloin ennakkomaksujen laskutusta ja ennakkomaksuja käytetään

| Ennakkomaksujen laskutus                                                                | Ennakkomaksut                                                              |
|-------------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| Määritä ostotilaukselle ennakkomaksun arvo.                                    | Ostotilaukselle ei määritetä ennakkomaksun arvoa.                    |
| Ennakkomaksulasku ja lopullinen lasku on kirjattava.                       | Ennakkomaksulaskua ei kirjata.                                    |
| Ennakkomaksun velka pidetään ennakkomaksutilillä, ei ostoreskontratilillä. | Ennakkomaksun velka pidetään ostoreskontratilillä.                  |
| Toimittajasaldo ei vastaa ennakkomaksun arvoa prosessin aikana.     | Toimittajasaldo vastaa ennakkomaksun arvoa prosessin aikana. |
| Ennakkomaksun laskutusta voi käyttää vain ostoreskontrassa.                         | Ennakkomaksuja voidaan käyttää osto- ja myyntireskontrassa.    |

## <a name="overview-of-the-prepayment-process"></a>Ennakkomaksuprosessin yleiskatsaus
Monissa maissa kirjanpitokäytännöt vaativat, että asiakkaan maksamia tai toimittajalle maksettuja ennakkomaksuja ei kirjata asiakkaan tai toimittajan tavallisille reskontratileille. Sen sijaan ennakkomaksut kirjataan erityisille ennakkomaksujen kirjanpitotileille. Kun myynti- tai ostotilaus tehdään, lasku lähetetään asiakkaalle tai vastaanotetaan toimittajalta. Laskua maksettaessa ennakkomaksujen kirjanpitotilillä näkyvä ennakkomaksu ja arvonlisäveron ennakkomaksu palautetaan ja laskusummat kirjataan automaattisesti tavallisille reskontratileille. Luo maksuehdotus seuraavien ohjeiden mukaan.

1.  Määritä ennakkomaksuille kirjausprofiilit.
2.  Valitse Myyntireskontran parametrit- ja Ostoreskontran parametrit -sivulla **Kirjanpito ja arvonlisävero** -kohdasta uusi kirjausprofiili käyttämällä **Kirjausprofiili maksukirjauskansiolle ennakkomaksun kanssa** -parametria.
3.  Luo maksukirjauskansio ja luo sitten uusi maksu.
4.  Voit merkitä maksun ennakkomaksuksi. Jos maksu on merkitty ennakkomaksuksi, maksu kirjataan kirjanpitotileille, jotka on määritetty vaiheissa 1 ja 2 määritellylle kirjausprofiilille. Lisäksi jos maksu on merkitty ennakkomaksuksi, verot lasketaan, Joissakin maissa verot on maksettava ennakkomaksua kirjattaessa, vaikka laskua ei olisi luotu.
5.  Kirjaa ennakkomaksu.
6.  Valinnainen: Ennakkomaksun voi tilittää osto- tai myyntitilausta vastaan jo ennen laskun luomista. Valitse myynti- tai ostotilaussivulla toimintoruudusta **Selvitä tapahtumat**.
7.  Kun toimittaja on toimittanut tavarat tai palvelut, kirjaa lasku. Jos tilitit ennakkomaksun osto- tai myyntitilausta vastaan vaiheessa 6, ennakkomaksu tilitetään automaattisesti luomaasi laskua vastaan. Jos et tilittänyt ennakkomaksua osto- tai myyntitilausta vastaan, voit tilittää sen laskua vastaan manuaalisesti valitsemalla asiakkaan tai toimittajan sivulta **Selvitä tapahtumat**. Tällöin ennakkomaksusumma palautetaan väliaikaiselta osto- tai myyntireskontran kirjanpitotililtä. Lisäksi jos verot on laskettu, ne peruutetaan, koska todelliset verot sisältyvät laskuun.

## <a name="overview-of-the-prepayment-invoicing-process"></a>Ennakkomaksun laskutusprosessin yleiskatsaus
Ennakkomaksulaskuja käytetään liiketoiminnassa yleisesti. Ennakkomaksulaskun avulla toimittaja vaatii ostoksesta ennakkomaksun ennen ostotilauksen toimittamista. Jotkin toimittajat voivat esimerkiksi vaatia ennakkomaksua mukautetuista tavaroista tai palveluista. Jos toimittaja lähettää ennakkomaksusta laskun, voit käyttää ennakkomaksun laskutustoimintoja. Ostotilaukselle määritetään ennakkomaksun arvo, ennakkomaksulasku kirjataan ja maksetaan ja sen jälkeen lopulliseen laskuun kohdistetaan ennakkomaksulasku. Luo maksuehdotus seuraavien ohjeiden mukaan.

1.  Ostoedustaja luo ja vahvistaa ja lähettää ostotilauksen, josta toimittaja on pyytänyt ennakkomaksua. Ennakkomaksun arvo on määritetty ostotilauksessa sopimuksen osana.
2.  Toimittaja lähettää ennakkomaksulaskun.
3.  Ostoreskontran koordinaattori kirjaa ennakkomaksulaskun ostotilausta vastaan ja ennakkomaksulasku maksetaan.
4.  Toimittaja lähettää maksupyynnön, jota kutsutaan vakiotoimittajalaskuksi. Kun toimittaja on toimittanut tavarat tai palvelut ja niihin liittyvät vakiotoimittajalaskut on vastaanotettu, ostoreskontran koordinaattori kohdistaa niihin ennakkomaksusumman, joka on jo maksettu vakiolaskua vastaan.
5.  Ostoreskontran koordinaattori maksaa ja tilittää vakiolaskun jäljelle jäävän summan.

## <a name="set-up-parameters-to-enable-the-prepayment-invoicing-process"></a>Määritä parametrit ennakkomaksulaskutusprosessin käyttöön ottamista varten
Ennakkomaksutili on määritettävä **Varaston kirjaus** -sivun **Ostotilaus**-välilehdessä (**Varastonhallinta \> Asetukset \> Kirjaus \> Kirjaus**). Ennakkomaksutili päivitetään, yleensä veloitetaan, kun ennakkomaksulasku kirjataan. Ennakkomaksutilin saldo peruutetaan, kun ennakkomaksulaskuun kohdistettu vakiolasku kirjataan. Jos ennakkomaksulaskua ei tilitetä maksuun ennen ennakkomaksulaskun kohdistamista vakiolaskuun, kirjatun ennakkomaksulaskun kirjanpitotapahtumat peruutetaan, kun vakiolasku kirjataan.

Ostoreskontran yhteenvetovastatili määritetään **Toimittajan kirjaus** -profiilissa. Voit määrittää oletuskirjausprofiilin valitsemalla **Ostoreskontra \>Asetukset \> Ostoreskontran parametrit \> Kirjanpito ja arvonlisävero -välilehti \> Kirjausprofiilin ennakkomaksun toimittajalaskulle**.

**Ennakkomaksun kohdistuskäytäntö** ilmaisee, kohdistaako järjestelmä automaattisesti selvitetyt ennakkomaksulaskut manuaalisesti luotuun lopulliseen laskuun. Tietoentiteetin avulla luodut laskut eivät viittaa **ennakkomaksun kohdistuskäytäntöön**. Selvitetyt ennakkomaksulaskut on kohdistettava manuaalisesti laskuihin, jotka on luotu tietoentiteetin avulla. Voit määrittää käytännön siirtymällä kohtaan **Ostoreskontra \>Asetukset \> Ostoreskontran parametrit \> Kirjanpito ja arvonlisävero -välilehti \> Ennakkomaksun kohdistuskäytäntö**. Jos **Ennakkomaksun kohdistuskäytäntö** -kentän arvoksi on määritetty **Automaattinen**, ennakkomaksulasku merkitään automaattisesti tilitettäväksi lopullisella laskulla. Jos kentän arvoksi määritetään **Ilmoitus**, näkyviin tulee visuaalinen merkki siitä, että ennakkomaksulasku on kohdistettavissa, kun lopullinen lasku luodaan.

## <a name="create-a-purchase-order-that-contains-prepayment-invoice-information"></a>Ennakkomaksulaskun tietoja sisältävän ostotilauksen luominen
Kun toimittaja kertoo, että ostotilauksen sisältämät tavarat ja palvelut edellyttävät ennakkomaksua, liittyvän ostotilauksen ennakkomaksun arvo on määritettävä. Siirry kohtaan **Ostoreskontra \> Yhteiset \> Ostotilaukset \> Kaikki ostotilaukset** ja etsi toimittajan ostotilaus. Valitse toimintoruudussa ensin **Osto**-välilehti ja sitten **Ennakkomaksu**. Kirjoita ennakkomaksun tiedot, mukaan lukien kuvaus, ennakkomaksun arvo, ja tieto siitä, onko ennakkomaksu kiinteä määrä vai prosenttiosuus ja ennakkomaksun luokan tunniste. 

Huomaa, että ostotilauksen useat ennakkomaksumääritykset eivät ole sallittuja. Jos haluat sallia useita ostotilauksen ennakkomaksuja, kirjaa maksut käyttämällä maksukirjauskansiota ennakkomaksulaskun asemesta.

Ennakkomaksu voidaan poistaa ostotilauksesta, ellet ole jo tilittänyt maksua kirjatulle ennakkomaksulaskulle tai kirjannut vakiolaskua. Voit poistaa ennakkomaksun tiedot ostotilauksesta valitsemalla **Ostoreskontra \> Yhteiset \> Ostotilaukset \> Kaikki ostotilaukset** ja etsi toimittajan ostotilaus. Valitse toimintoruudussa ensin **Osto**-välilehti ja sitten **Poista ennakkomaksu**.

## <a name="create-and-post-a-prepayment-invoice"></a>Luo ja kirjaa ennakkolasku
Jos haluat kirjata toimittajan ennakkomaksulaskun, siirry **Toimittajan lasku** -sivulle valitsemalla **Ennakkomaksulasku** -vaihtoehdon **Ostotilaukset** -sivulla (**Ostoreskontra \> Yhteiset \> Ostotilaukset \> Kaikki ostotilaukset \> Lasku-välilehti \> Ennakkomaksulasku**). Kirjoita tiedot ennakkomaksulaskulle, mukaan lukien laskun numero. Et voi muuttaa ennakkomaksun laskun määriä. Jos toimittaja on laskuttanut ostotilauksessa määritetyn ennakkomaksun arvon osasumman, voit päivittää yksikköhintaa vastaamaan osittaista arvoa.

Toimittajan saldo ja ennakkomaksutili päivitetään, kun ennakkomaksulasku kirjataan. Myös ostotilauksen sisältämän ennakkomaksumäärityksen **Ennakkomaksun kohdistus** -arvo päivitetään. Kirjatun ennakkomaksutositteen taloushallinnon oletusdimensiomerkinnät tulevat ostotilauksen otsikkotiedoista.

## <a name="post-and-settle-payments-for-the-prepayment-invoice"></a>Ennakkomaksulaskun kirjaaminen ja selvittäminen
Seuraavaksi ennakkomaksulasku maksetaan **Maksukirjauskansio**-sivulla. Voit käyttää maksukirjauskansioita valitsemalla **Ostoreskontra \> Kirjauskansiot \> Maksut \> Maksukirjauskansio**. Kun maksun tilitys on tehty ennakkomaksulaskuun, ostotilauksen **Ennakkomaksun kohdistus jäljellä** -arvo päivitetään.

Ennen ennakkomaksulaskun vakiolaskun kirjaamista voit peruuttaa maksun selvityksen ennakkomaksulaskusta. Kun vakiolasku on kohdistettu ennakkomaksulaskuun, maksun selvitystä ei voi peruuttaa ennakkomaksulaskusta.

## <a name="post-the-standard-vendor-invoice-for-the-purchase-order-and-apply-the-prepayment-invoice-to-the-standard-invoice"></a>Ostotilauksen vakiotoimittajalaskun kirjaaminen ja ennakkomaksulaskun kohdistaminen vakiolaskuun
Kirjaa toimittajalta saatu vakiolasku. Osana tätä prosessia voit kohdistaa selvitetyn ennakkomaksulaskun toimittajan laskuun siten, että laskun arvoa vähennetään jo maksetulla summalla. Kohdistamalla ennakkomaksulaskun toimittajan laskuun varmistat, että ennakkomaksulaskun kirjanpitomerkinnät peruutetaan.

## <a name="application-of-the-prepayment-invoice-after-posting-the-standard-invoice"></a>Ennakkomaksulaskun kohdistaminen vakiolaskun kirjauksen jälkeen
Jos unohdat kohdistaa ennakkomaksun toimittajan vakiolaskuun toimittajalaskun kirjauksen yhteydessä, selvitetty ennakkomaksu on käytettävissä kohdistettavaksi muihin tämän toimittajan laskuihin **Toimittajat**-sivulla (**Ostoreskontra \> Yhteiset \> Toimittajat \> Kaikki toimittajat \> Lasku-välilehti \> Kohdista**).

## <a name="reversal-of-the-prepayment-application-process"></a>Ennakkomaksun kohdistusprosessin peruuttaminen
Jos haluat peruuttaa täsmäytyksen tai ennakkomaksulaskun kohdistamisen vakiolaskusta, valitse **Toimittajat**-sivulta **Peruuta**-toiminto (**Ostoreskontra \> Yhteiset \> Toimittajat \> Kaikki toimittajat \> Lasku-välilehti \> Peruuta**). Kun ennakkomaksun kohdistus on peruutettu, voit kohdistaa ennakkomaksun toiseen vakiolaskuun. 



[!INCLUDE[footer-include](../../includes/footer-banner.md)]
