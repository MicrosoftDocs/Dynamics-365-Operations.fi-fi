---
title: Tilityksen yleiskatsaus
description: Tässä aiheessa on yleisiä tietoja tilitysprosessista. Siinä kuvataan, mitkä tapahtumatyypit voidaan selvittää, sekä ajoitus ja prosessi niiden ratkaisemiseksi. Siinä kuvataan myös selvitysprosessin tulokset.
author: kweekley
manager: AnnBe
ms.date: 04/10/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustOpenTrans, LedgerJournalTransCustPaym, LedgerJournalTransVendPaym, VendOpenTrans
audience: Application User
ms.reviewer: roschlom
ms.custom: 14551
ms.assetid: 0968fa71-5984-415b-8689-759a0136d5d1
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2018-10-31
ms.dyn365.ops.version: 8.0999999999999996
ms.openlocfilehash: a4ad8a124b2de2d364e11b6a32f8845ef438e1d1
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/15/2021
ms.locfileid: "4989161"
---
# <a name="settlement-overview"></a>Tilityksen yleiskatsaus

[!include [banner](../includes/banner.md)]

Tässä aiheessa on yleisiä tietoja tilitysprosessista. Siinä kuvataan, mitkä tapahtumatyypit voidaan selvittää, sekä ajoitus ja prosessi niiden ratkaisemiseksi. Siinä kuvataan myös selvitysprosessin tulokset.

Tilityksessä yhden asiakirjan tapahtumat kohdistetaan toisen asiakirjan tapahtumiin, jotta kummankin asiakirjan saldoa voidaan lisätä tai vähentää. Maksun voi esimerkiksi kohdistaa laskuun. Usean tyyppisten tapahtumien täsmäyttäminen on mahdollista eri aikoina ja erilaisin menetelmin. Tilitysprosessi voi myös luoda uusia tapahtumia.

## <a name="what-transactions-can-be-settled"></a>Mitä tapahtumia voi tilittää

Osto- ja myyntisaamiset -kohdassa selvitys voi tapahtua minkä tahansa transaktiotyypin välillä, jotka vaikuttavat myyjän tai asiakkaan saldoon. Nämä tapahtumatyypit voivat olla laskuja, maksuja, hyvityslaskuja ja maksuja. Kaikki tapahtumatyypit voidaan tilittää mitä tahansa muuta tapahtumatyyppiä vastaan. Voit esimerkiksi tilittää maksusuorituksen laskua vastaan, hyvityslaskun laskua vastaan, laskun toista laskua vastaan ja maksusuorituksen toista maksusuoritusta vastaan.

Voit tilittää maksuja tapahtumaa vastaan samassa tai eri yrityksessä. Keskitettyä maksumallia käyttävissä organisaatioissa [keskitetyt maksut](set-up-centralized-payments.md) voivat auttaa maksuprosessin tehostamisessa.

## <a name="when-to-settle-transactions"></a>Tapahtumien tilitysajankohta

Tapahtumat voidaan selvittää, kun maksuja syötetään. Jos esimerkiksi suoritat maksun toimittajalle, valitset yleensä mitkä laskut maksetaan. Valitsemalla laskut merkitset ne tilitettäviksi maksua vastaan. Kun myyntireskontran maksuista huolehtiva henkilö kirjaa asiakasmaksun, hän voi merkitä asianmukaiset laskut tilitettäviksi kunkin asiakkaan maksuun sisältyvien tietojen perusteella. Käytä **Selvitä tapahtumat** -sivua merkitäksesi tapahtumat tilitettäviksi. Voit avata tämän sivun mistä tahansa kirjaamattomasta laskusta tai maksusta. Kun tapahtuma kirjataan, samalla kirjataan myös tilitys. 

Tapahtumia voi tilittää myös kirjaamisen jälkeen. Voit syöttää ja kirjata asiakasmaksun tilittämättä sitä laskuja vastaan. Haluat kuitenkin varmasti ensin varmistaa, että maksu tilitetään oikeaa laskua vastaan, ennen kuin kirjaat tilityksen. **Selvitä tapahtumat** -sivun voi avata **Kaikki asiakkaat**- tai **Kaikki toimittajat** -sivulta tai kenen tahansa asiakkaan tai toimittajan **Tapahtumat**-sivulta.

Voit myös varata laskulle kirjattuja ennakkomaksuja merkitsemällä maksun tilitettäväksi osto- tai myyntitilausta vastaan. Tässä tapauksessa maksulla on yhä avoin saldo, mutta sitä ei voi tilittää toista laskua vastaan. Maksu tilitetään automaattisesti osto- tai myyntitilauksesta luotua laskua vastaan.

## <a name="how-to-settle-transactions"></a>Tapahtumien tilitystapa

Tapahtumia voi tilittää manuaalisesti, automaattisesti tai näiden yhdistelmällä. Selvitysmenetelmän valinta määräytyy liiketoimintaprosessien mukaan. **Ostoreskontran parametrit**- ja **myyntireskontran parametrit** -sivuilla voit määrittää tilitysprosessin niin, että se on kohdistettu kyseisiin liiketoimintaprosesseihin.

Voit luoda toimittajamaksuja ja asiakkaan suoraveloitusmaksuja käyttämällä maksuehdotusta.. Maksuehdotuksen avulla valitaan maksettavat laskut. Maksuehdotus aloitetaan manuaalisesti, ja sitten järjestelmä merkitsee valitut laskut automaattisesti tilitettäviksi, kun maksut luodaan.

Jos maksut luodaan manuaalisesti, voit valita tilitettävät laskut **Selvitä tapahtumat** -sivulla. Voit valita laskut manuaalisesti tai käyttää **Merkitse tärkeyden mukaan** -vaihtoehtoja, jolloin laskut merkitään tilitettäviksi automaattisesti. **Merkitse tärkeyden mukaan** -vaihtoehtoa voi käyttää vain myyntireskontrassa. Voit ottaa tämän vaihtoehdon käyttöön **myyntireskontran parametrit** -sivun **tilitysprioriteetti**-välilehdessä.

Jos maksuja hoitava henkilö kirjaa maksun mutta ei tilitä sitä ennen kirjaamista, maksu voidaan tilittää automaattisesti. Voit ottaa käyttöön automaattisen tilityksen **Myyntireskontran parametrit** ja **Ostoreskontran parametrit** sivuilla. Automaattinen tilitys selvittää tapahtumat vain samassa oikeushenkilössä. Se ei ratkaise useiden oikeushenkilöiden tapahtumia.

Kun käytät automaattista tilitystä, voit käyttää etukäteen määritettyä tilitysprioriteettia tai määrittää oman tilitysjärjestyksen **Myyntireskontran parametrit** -sivulla. Tätä toimintoa voi käyttää vain myyntireskontrassa.

## <a name="results-of-settlement"></a>Tilityksen tulokset

Kun tapahtumia tilitetään, kunkin tapahtuman jäljellä oleva saldo kasvaa tai pienenee. Yleensä, kun tilitetään lasku ja maksu, kummankin tapahtuman tila ja saldo päivittyvät seuraavien sääntöjen mukaisesti:

- Jos maksun summa on suurempi kuin laskun summa, laskun saldo vähennetään arvoon 0,00 ja lasku suljetaan. Maksu jää avoimeksi, ja saldo on erotus maksun ja laskun summan välillä.
- Jos maksun summa on pienempi kuin laskun summa, maksun saldo vähennetään arvoon 0,00 ja maksu suljetaan. Lasku jää avoimeksi, ja saldo on erotus laskun ja maksun summan välillä.
- Jos maksun summa on sama kuin laskun summa, sekä maksu että lasku suljetaan ja molempien saldo vähentyy 0,00:ksi.

Jos [maksun summa on pienempi kuin laskun summa](../accounts-payable/vendor-payments-partial-amount.md) käteisalennuksen, poiston tai liian pienen maksusumman vuoksi, lasku ja maksu voidaan silti sulkea riippuen siitä, miten tilitykset on määritetty **Myyntireskontran parametrit** ja **Ostoreskontran parametrit** -kohtien tilitysasetusten mukaan.

Tilitykset voivat myös luoda tapahtumia. Esimerkiksi laskun ja maksun tilitys voi tuottaa käteisalennuksen, realisoituneen voiton tai tappion, arvonlisäveron oikaisuja, poistoja tai erotuksia, joiden suuruus on senttien luokkaa.

## <a name="identifying-marked-transactions-during-settlement"></a>Merkittyjen tapahtumien tunnistaminen selvityksen aikana

Kun yrität selvittää tapahtuman, saatat huomata symbolin, joka ilmaisee, että tapahtuma on merkitty toiseen sijaintiin. Tässä tapauksessa voit valita tapahtuman **Selvitä tapahtumat** -sivulla ja valita sitten selvityksen **Kysely \>Tilitys tilitysikkunasta**. Tämän kyselyn näkymä sisältää kirjauskansiot, myyntitilaukset, laskut, maksuehdotukset ja asiakkaan sijainnit, jotka voivat estää tapahtuman tilitystä. Voit ratkaista ongelman valitsemalla linkin, joka siirtyy suoraan kyselyn estettyyn sijaintiin. Tämän jälkeen voit päivittää asiakirjan sen tilittämiseen tarvittavilla oikaisuilla. **Merkityn** mittarin avulla voit myös tunnistaa muut samaan estosijaintiin sisältyvät tiedostot.

## <a name="additional-resources"></a>Lisäresurssit

- [Selvitä jäljellä olevan summa](settle-remainder.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]