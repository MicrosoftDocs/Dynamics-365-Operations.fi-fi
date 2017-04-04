---
title: Ennakkomaksulaskut ja ennakkomaksut
description: "Tässä artikkelissa kuvaillaan ja vertaillaan kahta menetelmää, joita organisaatiot voivat käyttää ennakkomaksuihin. Ensimmäisessä menetelmässä on luotava ennakkomaksulasku, joka on liitetty ostotilaukseen. Toisessa menetelmässä ennakkomaksukirjauskansion tositteita voi luoda luomalla kirjauskansiovientejä ja merkitsemällä ne ennakkomaksukirjauskansion tositteiksi."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: LedgerJournalTransVendPaym, PurchTable
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 15871
ms.assetid: a0bb5220-73d4-48ae-84d0-46a171c224fa
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 44d51807cd6bb64ae2c4bef58d8a445417ffa3a9
ms.openlocfilehash: 770a6fba8a27e9403235929b7e8cd547cc522486
ms.lasthandoff: 03/31/2017


---

# <a name="prepayment-invoices-vs-prepayments"></a>Ennakkomaksulaskut ja ennakkomaksut

Tässä artikkelissa kuvaillaan ja vertaillaan kahta menetelmää, joita organisaatiot voivat käyttää ennakkomaksuihin. Ensimmäisessä menetelmässä on luotava ennakkomaksulasku, joka on liitetty ostotilaukseen. Toisessa menetelmässä ennakkomaksukirjauskansion tositteita voi luoda luomalla kirjauskansiovientejä ja merkitsemällä ne ennakkomaksukirjauskansion tositteiksi.

Yritykset saattavat suorittaa ennakkomaksuja toimittajille tavaroista tai palveluista jo ennen niiden toimittamista. Ennakkomaksuja voidaan suorittaa toimittajille kahdella tavalla. Riskien minimoimiseksi ennakkomaksuja voi seurata määrittämällä ennakkomaksun ostotilaukselle. Tällöin on luotava ennakkomaksulasku, joka on liitetty ostotilaukseen. Tätä menetelmää kutsutaan ennakkomaksun laskuttamiseksi. Yritykset, jotka eivät halua seurata ennakkomaksuja kovin tarkasti tai eivät saa toimittajalta ennakkomaksulaskuja, voivat käyttää ennakkomaksujen laskutusmenetelmän sijaan ennakkomaksukirjauskansion tositteita. Ennakkomaksukirjauskansion tositteita voi luoda luomalla kirjauskansiovientejä ja merkitsemällä ne ennakkomaksukirjauskansion tositteiksi. Tässä menetelmässä ei voi seurata, mitkä ennakkomaksut toimittajalle vastaavat mitäkin ostotilausta. Voit kuitenkin merkitä kirjatun ennakkomaksun tilitettäväksi ostotilausta vastaan.

## <a name="when-to-use-prepayment-invoicing-vs-prepayments"></a>Milloin ennakkomaksujen laskutusta ja ennakkomaksuja käytetään
| Ennakkomaksujen laskutus                                                                | Ennakkomaksut                                                              |
|-------------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| Määritä ostotilaukselle ennakkomaksun arvo.                                    | Ostotilaukselle ei määritetä ennakkomaksun arvoa.                    |
| Avain: ennakkomaksulasku ja lopullinen lasku on kirjattava.                       | Ennakkomaksulaskua ei kirjata.                                    |
| Ennakkomaksun velka pidetään ennakkomaksutilillä, ei ostoreskontratilillä. | Ennakkomaksun velka pidetään ostoreskontratilillä.                  |
| Toimittajasaldo ei vastaa ennakkomaksun arvoa prosessin aikana.     | Toimittajasaldo vastaa ennakkomaksun arvoa prosessin aikana. |
| Ennakkomaksun laskutusta voi käyttää vain ostoreskontrassa.                         | Ennakkomaksuja voidaan käyttää osto- ja myyntireskontrassa.    |

## <a name="overview-of-the-prepayment-process"></a>Ennakkomaksuprosessin yleiskatsaus
Monissa maissa kirjanpitokäytännöt vaativat, että asiakkaan maksamia tai toimittajalle maksettuja ennakkomaksuja ei kirjata asiakkaan tai toimittajan tavallisille reskontratileille. Sen sijaan ennakkomaksut kirjataan erityisille ennakkomaksujen kirjanpitotileille. Kun myynti- tai ostotilaus tehdään, lasku lähetetään asiakkaalle tai vastaanotetaan toimittajalta. Laskua maksettaessa ennakkomaksujen kirjanpitotilillä näkyvä ennakkomaksu ja arvonlisäveron ennakkomaksu palautetaan ja laskusummat kirjataan automaattisesti tavallisille reskontratileille. Luo maksuehdotus seuraavien ohjeiden mukaan.

1.  Määritä ennakkomaksuille kirjausprofiilit.
2.  Valitse Myyntireskontran parametrit- ja Ostoreskontran parametrit -sivulla **Kirjanpito ja arvonlisävero** -kohdasta uusi kirjausprofiili käyttämällä **Kirjausprofiili maksukirjauskansiolle ennakkomaksun kanssa** -parametria.
3.  Luo maksukirjauskansio ja luo sitten uusi maksu.
4.  Voit merkitä maksun ennakkomaksuksi. Jos maksu on merkitty ennakkomaksuksi, maksu kirjataan kirjanpitotilille, joka määritetään kirjausprofiili, joka määritetään vaiheet 1 ja 2. Lisäksi, jos maksu on merkitty ennakkomaksuksi, verot lasketaan. Joissakin maissa verot on maksettava ennakkomaksua kirjattaessa, vaikka laskua ei olisi luotu.
5.  Kirjaa ennakkomaksu.
6.  Valinnainen: Voit selvittää vastaan osto- tai myyntitilauksen ennakkomaksu ennen kuin luot laskun. Myyntitilaus tai ostotilaus-sivu, toimintoruudussa, voit käyttää **tapahtumat selvitetään**.
7.  Kun toimittaja on toimittanut tavarat tai palvelut, kirjaa lasku. Jos tilitit ennakkomaksun osto- tai myyntitilausta vastaan vaiheessa 6, ennakkomaksu tilitetään automaattisesti luomaasi laskua vastaan. Jos et tilittänyt ennakkomaksua osto- tai myyntitilausta vastaan, voit tilittää sen laskua vastaan manuaalisesti valitsemalla asiakkaan tai toimittajan sivulta **Selvitä tapahtumat**. Tällöin ennakkomaksusumma palautetaan väliaikaiselta osto- tai myyntireskontran kirjanpitotililtä. Lisäksi jos verot on laskettu, ne peruutetaan, koska todelliset verot sisältyvät laskuun.

## <a name="overview-of-the-prepayment-invoicing-process"></a>Ennakkomaksun laskutusprosessin yleiskatsaus
Ennakkomaksulaskuja käytetään liiketoiminnassa yleisesti. Ennakkomaksulaskun avulla toimittaja vaatii ostoksesta ennakkomaksun ennen ostotilauksen toimittamista. Jotkin toimittajat voivat esimerkiksi vaatia ennakkomaksua mukautetuista tavaroista tai palveluista. Jos toimittaja lähettää ennakkomaksusta laskun, voit käyttää ennakkomaksun laskutustoimintoja. Ostotilaukselle määritetään ennakkomaksun arvo, ennakkomaksulasku kirjataan ja maksetaan ja sen jälkeen lopulliseen laskuun kohdistetaan ennakkomaksulasku. Luo maksuehdotus seuraavien ohjeiden mukaan.

1.  Ostoedustaja luo ja vahvistaa ja lähettää ostotilauksen, josta toimittaja on pyytänyt ennakkomaksua. Ennakkomaksun arvo on määritetty ostotilauksessa sopimuksen osana.
2.  Toimittaja lähettää ennakkomaksulaskun.
3.  Ostoreskontran koordinaattori kirjaa ennakkomaksulaskun ostotilausta vastaan ja ennakkomaksulasku maksetaan.
4.  Kun toimittaja on toimittanut tavarat tai palvelut ja niihin liittyvät toimittajalaskut on vastaanotettu, ostoreskontran koordinaattori kohdistaa niihin ennakkomaksusumman, joka on jo maksettu laskua vastaan.
5.  Ostoreskontran koordinaattori maksaa ja tilittää jäljelle jäävän summan.



