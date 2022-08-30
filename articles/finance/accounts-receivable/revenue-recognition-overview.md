---
title: Tuottokirjausten yleiskatsaus (sisältää videon)
description: Tässä artikkelissa on tietoja tuottokirjausominaisuudesta. Tämä ominaisuus tarjoaa joustavan kehyksen, jonka avulla voit määrittää yrityskohtaiset säännöt moniosaisten tilausten tuottohinnan ja tuottoaikataulun tunnistamista varten.
author: bking
ms.date: 03/15/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: Customer
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: bking
ms.search.validFrom: 2018-08-30
ms.dyn365.ops.version: 8.0.4
ms.openlocfilehash: be3e6438e86911d9703a5ac7413515389308b340
ms.sourcegitcommit: 1909d18a74cef85aad020a6a7473281e451f58c7
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/24/2022
ms.locfileid: "9348351"
---
# <a name="revenue-recognition-overview"></a>Tuottokirjausten yleiskatsaus

[!include [banner](../includes/banner.md)]

Useita elementtejä myyvien yritysten, kuten tuotteiden, palveluiden ja tilausten, on pystyttävä purkamaan moniosaiset tilaukset, jotta tuotto voidaan kirjata yrityskohtaisia ja toimialakohtaisia ohjeita noudattaen.

Tuottokirjausten, mukaan lukien myyntirakennetoiminnot, käyttämistä Commerce-kanavissa (verkkokauppa, myyntipiste, puhelinkeskus) ei tueta. Tuottokirjausten kanssa määritettyjä nimikkeitä ei tulisi lisätä Commerce-kanavissa luotuihin tilauksiin tai tapahtumiin.

Yleensä tuoton kirjausprosessia voidaan käyttää seuraavien tehtävien suorittamiseen:

* Kohdista tuotto sen varmistamiseksi, että asianmukainen tuottohinta tunnistetaan moniosaisten tilausten komponenttien arvon perusteella.
* Siirrä tuottoa käyttäen tuottoaikataulua, joka edustaa sopimuksen voimassaoloaikaa sekä prosenttiosuuksia tuoton kirjaamiselle ajan kuluessa.

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE44iER]

[Tuoton tunnistaminen Dynamics 365 Financessa](https://youtu.be/v3amIsiqvoo) -video (yllä) kuuluu YouTubessa saatavilla olevaan [talous- ja toimintosovellusten toistoluetteloon](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW).

Tuoton kirjausominaisuus tarjoaa joustavan kehyksen, jonka avulla voit määrittää yrityskohtaiset säännöt, joiden avulla voidaan tunnistaa tuottohinta ja tuottoaikataulu.

Vapautettuja tuotteita käytetään myyntitilausasiakirjojen tuottojen kirjaamisen tukemiseen. Vapautetut tuotteet sisältävät asetukset, joita tarvitaan tuottohinnan ja tuottoaikataulun määrittämiseen. Myyntitilaus voi olla peräisin aika- ja materiaaliprojektista.

Yritykset voivat käyttää tuottoajoitustoimintoa käyttämättä tuottohintatoimintoa. Tämän vuoksi myyntitilausrivien hintaa käytetään joko tuottona tai lykättynä tuottona. Jos myyntitilausrivillä on tuottoaikataulu, myyntitilausrivin hintaa lykätään. Jos myyntitilausrivillä ei ole tuottoaikataulua, myyntitilausrivin hinta kirjataan tuottotilille laskutettaessa.

Tuottohinta lasketaan joko silloin, kun myyntitilaus vahvistetaan tai laskun kirjaamisen yhteydessä. Jos haluat esikatsella tuottohintaa ennen laskun kirjaamista, sinun on vahvistettava myyntitilaus.

Kun myyntitilaus on vahvistettu, myös odotettu tuottoaikataulu luodaan, jos jollakin myyntitilausrivillä on tuottoaikataulu. Kun myyntitilaus laskutetaan, odotettu tuottoaikataulu poistetaan ja odotettu tuottoaikataulu korvataan todellisella tuoton kirjausaikataululla.

Myynnin tuottoaikataulun tiedot säilyvät kunkin myyntitilausrivin osalta. Tämän vuoksi tuottokirjauksen hallinta voi tarkastella tietoja ja vapauttaa rivit tuottoihin, kun sopimusvelvoite on täytetty. Kunkin kauden lopussa tuottokirjauksen hallinta voi luoda tuottokirjauskansion, joka vapauttaa määritettynä päivänä tai ennen sitä erääntyvät aikataulun rivit. Tätä tuottokirjauskansiota ei kirjata heti. Tämän vuoksi tuottokirjauksen hallinta voi tarkistaa, että oikeat summat vapautetaan laskennallisista tuloista todellisiin tuloihin.

Jos sopimukseen perustuva muutos aiheuttaa uuden myyntitilausrivin lisäämisen joko olemassa olevaan myyntitilaukseen tai uuteen myyntitilaukseen, uudelleenkohdistamista voidaan käyttää korjaamaan myyntitilausten kaikkien rivien tuottohinta.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]

