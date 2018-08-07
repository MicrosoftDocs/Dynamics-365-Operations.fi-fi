---
title: Tilityksen yleiskuvaus
description: "Tässä artikkelissa on yleisiä tietoja tilitysprosessista. Artikkelissa kuvataan tilitettävien tapahtumien tyyppejä, tapahtumien tilitysajankohtia ja -tapoja sekä tilitysprosessin tuloksia."
author: kweekley
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CustOpenTrans, LedgerJournalTransCustPaym, LedgerJournalTransVendPaym, VendOpenTrans
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 14551
ms.assetid: 0968fa71-5984-415b-8689-759a0136d5d1
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 2f1f11a7f1340d408374e658ae616ffa99f3c911
ms.contentlocale: fi-fi
ms.lasthandoff: 11/03/2017

---

# <a name="settlement-overview"></a>Tilityksen yleiskuvaus

[!include [banner](../includes/banner.md)]

Tässä artikkelissa on yleisiä tietoja tilitysprosessista. Artikkelissa kuvataan tilitettävien tapahtumien tyyppejä, tapahtumien tilitysajankohtia ja -tapoja sekä tilitysprosessin tuloksia.

Tilityksessä yhden asiakirjan tapahtumat kohdistetaan toisen asiakirjan tapahtumiin, jotta kummankin asiakirjan saldoa voidaan lisätä tai vähentää. Maksun voi esimerkiksi kohdistaa laskuun. Useiden tapahtumatyyppien täsmäyttäminen on mahdollista eri aikoina ja eri menetelmin. Tilityksen vuoksi voidaan myös joutua luomaan uusia tapahtumia.

## <a name="what-transactions-can-be-settled"></a>Mitä tapahtumia voi tilittää
Osto- ja myyntireskontrassa tilitys voidaan tehdä minkä tahansa toimittaja- tai asiakassaldoon vaikuttavien tapahtumatyyppien, kun laskujen, maksusuoritusten, hyvityslaskujen ja maksujen välillä. Kaikki tapahtumatyypit voidaan tilittää mitä tahansa muuta tapahtumatyyppiä vastaan. Voit esimerkiksi tilittää maksusuorituksen laskua vastaan, hyvityslaskun laskua vastaan, laskun toista laskua vastaan ja maksusuorituksen toista maksusuoritusta vastaan. Voit tilittää maksuja tapahtumaa vastaan samassa tai eri yrityksessä. Keskitettyä maksumallia käyttävissä organisaatioissa [keskitetyt maksut](set-up-centralized-payments.md) voivat auttaa maksuprosessin tehostamisessa.

## <a name="when-to-settle-transactions"></a>Tapahtumien tilitysajankohta
Tapahtumat voidaan tilittää maksukirjauksen yhteydessä. Jos esimerkiksi suoritat maksun toimittajalle, valitset yleensä maksettavat laskut. Valitsemalla laskut merkitset ne tilitettäviksi maksua vastaan. Kun myyntireskontran maksuista huolehtiva henkilö kirjaa asiakasmaksun, hän voi merkitä asianmukaiset laskut tilitettäviksi asiakkaan maksuun sisältyvien tietojen perusteella. Tapahtumat merkitään tilitettäviksi **Selvitä tapahtumat** -sivulla. Sivun voi avata mistä tahansa kirjaamattomasta laskusta tai maksusta. Kun tapahtuma kirjataan, samalla kirjataan myös tilitys. Tapahtumia voi tilittää myös kirjaamisen jälkeen. Voit syöttää ja kirjata asiakasmaksun tilittämättä sitä laskuja vastaan. Kannattaa kuitenkin ensin varmistaa, että maksu tilitetään oikeaa laskua vastaan. **Selvitä tapahtumat** -sivun voi avata **Kaikki asiakkaat**- tai **Kaikki toimittajat** -sivulta tai kenen tahansa asiakkaan tai toimittajan **Tapahtumat**-sivulta. Voit myös varata laskulle kirjattuja ennakkomaksuja merkitsemällä maksun tilitettäväksi osto- tai myyntitilausta vastaan. Tässä tapauksessa maksulla on yhä avoin saldo, mutta sitä ei voi tilittää toista laskua vastaan. Maksu tilitetään automaattisesti osto- tai myyntitilauksesta luotua laskua vastaan.

## <a name="how-to-settle-transactions"></a>Tapahtumien tilitystapa
Tapahtumia voi tilittää manuaalisesti, automaattisesti tai näiden yhdistelmällä. Valittava tilitysmenetelmä riippuu liiketoimintaprosesseista, ja se voidaan ottaa käyttöön Myyntireskontran parametrit- ja Ostoreskontran parametrit -sivujen tilitysasetuksissa. Voit luoda toimittajamaksuja ja asiakkaan suoraveloitusmaksuja käyttämällä maksuehdotusta, jolla valitaan maksettavat laskut. Maksuehdotus käynnistetään manuaalisesti, mutta Microsoft Dynamics 365 for Finance and Operations merkitsee tällöin valitut laskut automaattisesti tilitettäviksi, kun maksut luodaan. Jos maksut luodaan manuaalisesti, voit valita tilitettävät laskut **Selvitä tapahtumat** -sivulla. Voit valita laskut manuaalisesti tai käyttää **Merkitse tärkeyden mukaan** -vaihtoehtoja, jolloin laskut merkitään tilitettäviksi automaattisesti. **Merkitse tärkeyden mukaan** -vaihtoehtoa voi käyttää vain myyntireskontrassa. Voit ottaa tämän vaihtoehdon käyttöön Myyntireskontran parametrit -kohdassa **Tilitysprioriteetti**-sivulla. Jos maksuja hoitava henkilö kirjaa maksun mutta ei tilitä sitä ennen kirjaamista, maksu voidaan tilittää automaattisesti. Voit ottaa käyttöön automaattinen tilitys Myyntireskontran ja Ostoreskontran parametreissa. Kun käytät automaattista tilitystä, voit käyttää etukäteen määritettyä tilitysjärjestystä tai määrittää oman tilitysjärjestyksen Myyntireskontran parametrit -kohdassa. Tätä toimintoa voi käyttää vain myyntireskontrassa.

## <a name="results-of-settlement"></a>Tilityksen tulokset
Kun tapahtumia tilitetään, kunkin tapahtuman jäljellä oleva saldo kasvaa tai pienenee. Tyypillisessä tilanteessa, jossa tilitetään lasku ja maksu, kummankin tapahtuman tila ja saldo päivittyvät seuraavien sääntöjen mukaisesti:

-   Jos maksun summa on suurempi kuin laskun summa, laskun saldo vähennetään arvoon 0,00 ja lasku suljetaan. Maksu jää avoimeksi, ja saldo on summa, jolla maksu ylittää laskun summan.
-   Jos maksun summa on pienempi kuin laskun summa, maksun saldo vähennetään arvoon 0,00 ja maksu suljetaan. Lasku jää avoimeksi, ja saldo on maksun ja laskun summien erotus.
-   Jos maksun summa on sama kuin laskun summa, sekä maksu että lasku suljetaan ja molempien saldoksi tulee 0,00.

Jos [maksu on pienempi kuin laskun summa](../accounts-payable/vendor-payments-partial-amount.md) käteisalennuksen, poiston tai liian pienen maksusumman vuoksi, lasku ja maksu voidaan silti sulkea Myyntireskontran parametrit- ja Ostoreskontran parametrit -kohtien tilitysasetusten mukaan. Tilitys voi myös luoda tapahtumia. Esimerkiksi laskun ja maksun tilitys voi tuottaa käteisalennuksen, realisoituneen voiton tai tappion, arvonlisäveron oikaisuja, poistoja tai erotuksia, joiden suuruus on senttien luokkaa.




