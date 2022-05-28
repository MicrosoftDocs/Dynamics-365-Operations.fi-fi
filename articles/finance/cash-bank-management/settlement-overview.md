---
title: Tilityksen yleiskatsaus
description: Tässä aiheessa on yleisiä tietoja tilitysprosessista. Siinä kuvataan, mitkä tapahtumatyypit voidaan selvittää, sekä ajoitus ja prosessi niiden ratkaisemiseksi. Siinä kuvataan myös selvitysprosessin tulokset.
author: panolte
ms.date: 07/30/2021
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: CustOpenTrans, LedgerJournalTransCustPaym, LedgerJournalTransVendPaym, VendOpenTrans
audience: Application User
ms.reviewer: kfend
ms.custom:
- "14551"
- intro-internal
ms.assetid: 0968fa71-5984-415b-8689-759a0136d5d1
ms.search.region: Global
ms.author: panolte
ms.search.validFrom: 2018-10-31
ms.dyn365.ops.version: 8.0999999999999996
ms.openlocfilehash: e1992019570129461f3ecdd5479a87bafd8aeacb
ms.sourcegitcommit: 631d2cea52590af15f208e9af584446e85540fcf
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/07/2022
ms.locfileid: "8724894"
---
# <a name="settlement-overview"></a>Tilityksen yleiskatsaus

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]


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

## <a name="resolve-issues-with-transactions-that-cant-be-settled"></a>Ongelmien ratkaisu, kun tapahtumia ei voi selvittää

Joskus tapahtumia ei voi selvittää, koska toinen toiminto käsittelee asiakirjaa sillä hetkellä. Jos tapahtumat yritetään selvittää, tapahtuu virhe, koska kyseisiä tapahtumia käytetään. Tämän ongelman voi korjata etsimällä **Merkityn tapahtuman tiedot** -sivun avulla tapahtumia, jotka on merkitty selvitettäviksi, ja määrittää muut mahdolliset niitä käyttävät prosessit.

Tapahtumat merkitään selvitettäviksi joko silloin, kun toimittajan laskuja maksetaan, tai silloin, kun asiakkaat maksavat avoimet laskunsa. Joskus kyseiset laskut on ehkä jo merkitty selvitettäviksi. Sen vuoksi käyttäjät eivät voi valita niitä maksettaviksi. Toinen asiakkaan maksukirjauskansio, myyntitilaus, toimittajan maksukirjauskansio tai ostotilaus on voinut merkitä laskut nykyisessä yrityksessä tai toisessa yrityksessä.

Jos tapahtuman selvitys on estetty, kun asiakkaan maksua kirjataan, avaa **Asiakkaan merkityn tapahtuman tiedot** -sivu (**Ostoreskontra \> Kausittaiset tehtävät \> Asiakkaan merkityn tapahtuman tiedot**). Kohta, jossa tapahtuma on estetty, voidaan tunnistaa nopeasti määrittämällä jokin seuraavista valintaparametreista: **Asiakastili**, **Tosite**, **Päivämäärä** tai **Lasku**. Jos mitään valintaparametria ei määritetä, järjestelmä näyttää kaikki nykyisen yrityksen tai muun valitun yrityksen estetyt asiakirjat. Kun tapahtuma, jonka selvitys on estetty, on tunnistettu, sen voi valita, minkä jälkeen voidaan valita **Poista valittujen tapahtumien merkintä**. Valittu tapahtuma poistetaan sitten niistä kirjauskansioista, joihin se sisältyy. Asiakirjaa ei kuitenkaan poisteta muusta sijainnista. Vain merkintätiedot poistetaan kyseisestä kirjauskansiosta.

Jos tapahtuman selvitys on estetty, kun toimittajan maksua kirjataan, avaa **Toimittajan merkityn tapahtuman tiedot** -sivu (**Myyntireskontra \> Kausittaiset tehtävät \> Toimittajan merkityn tapahtuman tiedot**). Kohta, jossa tapahtuma on estetty, voidaan tunnistaa nopeasti määrittämällä jokin seuraavista valintaparametreista: **Toimittajan tili**, **Tosite**, **Päivämäärä** tai **Lasku**. Jos mitään valintaparametria ei määritetä, järjestelmä näyttää kaikki nykyisen yrityksen tai muun valitun yrityksen estetyt asiakirjat. Kun tapahtuma on tunnistettu, estämisongelman voidaan korjata valitsemalla ensin tapahtuma ja sitten **Poista valittujen tapahtumien merkintä**. Valittu tapahtuma poistetaan sitten niistä kirjauskansioista, joissa se on valittu. Asiakirjaa ei kuitenkaan poisteta muusta sijainnista. Vain merkintätiedot poistetaan kyseisestä kirjauskansiosta.

Kaikki estetyt asiakirjat tunnistetaan avaamalla **Kaikki merkityt tapahtuman tiedot** -sivu (**Myyntireskontra \> Kausittaiset tehtävät \> Kaikki merkityt tapahtumat tiedot** tai **Ostoreskontra \> Kausittaiset tehtävät \> Kaikki merkityt tapahtuman tiedot**). Kohta, jossa tapahtuma on estetty, voidaan tunnistaa nopeasti määrittämällä jokin seuraavista valintaparametreista: **Asiakastili**, **Toimittajan tili**, **Tosite**, **Päivämäärä** tai **Lasku**. Jos mitään valintaparametria ei määritetä, järjestelmä näyttää kaikki nykyisen yrityksen tai muun valitun yrityksen estetyt asiakirjat. Kun tapahtuma on tunnistettu, estämisongelman voidaan korjata valitsemalla ensin tapahtuma ja sitten **Poista valittujen tapahtumien merkintä**. Valittu tapahtuma poistetaan sitten niistä kirjauskansioista, joissa se on valittu. Asiakirjaa ei kuitenkaan poisteta muusta sijainnista. Vain merkintätiedot poistetaan kyseisestä kirjauskansiosta.

Ennen kuin käytät tätä toimintoa, sen on oltava päällä järjestelmässäsi. Järjestelmänvalvojat voivat käyttää **Toimintojen hallinnan** työtilaa tarkistaakseen toiminnon tilan sekä laittaa sen päälle, jos sitä vaaditaan. Tässä tapauksessa toiminto näkyy seuraavalla tavalla:

- **Moduuli:** Maksuliikenteen hallinta
- **Ominaisuuden nimi**: Merkityn tapahtuman tiedot -lomake

## <a name="additional-resources"></a>Lisäresurssit

- [Selvitä jäljellä olevan summa](settle-remainder.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
