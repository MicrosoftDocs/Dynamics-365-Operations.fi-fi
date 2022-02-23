---
title: Tuottokirjausten yleiskatsaus
description: Tässä ohjeaiheessa on tietoja tuottokirjausominaisuudesta. Tämä ominaisuus tarjoaa joustavan kehyksen, jonka avulla voit määrittää yrityskohtaiset säännöt, joiden avulla voidaan tunnistaa moniosaisten tilausten tuottohinta ja tuottoaikataulu.
author: kweekley
manager: aolson
ms.date: 11/11/2019
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: Customer
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2018-08-30
ms.dyn365.ops.version: 8.0.4
ms.openlocfilehash: 92af567499c1a8a23cd4d51e5bab48eaab2d8422
ms.sourcegitcommit: e544c51a68ad5daf748c0e877bdbde094ad40bd2
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/03/2020
ms.locfileid: "4458957"
---
# <a name="revenue-recognition-overview"></a>Tuottokirjausten yleiskatsaus

[!include [banner](../includes/banner.md)]

> [!NOTE]
> Tuoton kirjaustoimintoa ei voi ottaa käyttöön ominaisuuksien hallinnan avulla. Tällä hetkellä se on otettava käyttöön konfigurointiavainten avulla.

Useita elementtejä myyvien yritysten, kuten tuotteiden, palveluiden ja tilausten, on pystyttävä purkamaan moniosaiset tilaukset, jotta tuotto voidaan kirjata yrityskohtaisia ja toimialakohtaisia ohjeita noudattaen.

Yleensä tuoton kirjausprosessia voidaan käyttää seuraavien tehtävien suorittamiseen:

* Kohdista tuotto sen takaamiseksi, että asianmukainen tuottohinta tunnistetaan moniosaisten tilausten komponenttien arvon perusteella.
* Siirrä tuottoa käyttäen tuottoaikataulua, joka edustaa sopimuksen voimassaoloaikaa sekä prosenttiosuuksia tuoton kirjaamiselle ajan kuluessa.

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE44iER]

[Tuoton tunnistaminenDynamics 365 Financessa](https://youtu.be/v3amIsiqvoo) -video (yllä) kuuluu [Finance and Operations -soittolistaan](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW) YouTubessa.

Tuoton kirjausominaisuus tarjoaa joustavan kehyksen, jonka avulla voit määrittää yrityskohtaiset säännöt, joiden avulla voidaan tunnistaa tuottohinta ja tuottoaikataulu.

Vapautettuja tuotteita käytetään myyntitilausasiakirjojen tuottojen kirjaamisen tukemiseen. Vapautetut tuotteet sisältävät asetukset, joita tarvitaan tuottohinnan ja tuottoaikataulun määrittämiseen. Myyntitilaus voi olla peräisin aika- ja materiaaliprojektista.

Yritykset voivat käyttää tuottoajoitustoimintoa käyttämättä tuottohintatoimintoa. Tämän vuoksi myyntitilausrivien hintaa käytetään joko tuottona tai lykättynä tuottona. Jos myyntitilausrivillä on tuottoaikataulu, myyntitilausrivin hintaa lykätään. Jos myyntitilausrivillä ei ole tuottoaikataulua, myyntitilausrivin hinta kirjataan tuottotilille laskutettaessa.

Tuottohinta lasketaan joko silloin, kun myyntitilaus vahvistetaan tai laskun kirjaamisen yhteydessä. Jos haluat esikatsella tuottohintaa ennen laskun kirjaamista, sinun on vahvistettava myyntitilaus.

Kun myyntitilaus on vahvistettu, myös odotettu tuottoaikataulu luodaan, jos jollakin myyntitilausrivillä on tuottoaikataulu. Kun myyntitilaus laskutetaan, odotettu tuottoaikataulu poistetaan ja odotettu tuottoaikataulu korvataan todellisella tuoton kirjausaikataululla.

Myynnin tuottoaikataulun tiedot säilyvät kunkin myyntitilausrivin osalta. Tämän vuoksi tuottokirjauksen hallinta voi tarkastella tietoja ja vapauttaa rivit tuottoihin, kun sopimusvelvoite on täytetty. Kunkin kauden lopussa tuottokirjauksen hallinta voi luoda tuottokirjauskansion, joka vapauttaa määritettynä päivänä tai ennen sitä erääntyvät aikataulun rivit. Tätä tuottokirjauskansiota ei kirjata heti. Tämän vuoksi tuottokirjauksen hallinta voi tarkistaa, että oikeat summat vapautetaan laskennallisista tuloista todellisiin tuloihin.

Jos sopimukseen perustuva muutos aiheuttaa uuden myyntitilausrivin lisäämisen joko olemassa olevaan myyntitilaukseen tai uuteen myyntitilaukseen, uudelleenkohdistamista voidaan käyttää korjaamaan myyntitilausten kaikkien rivien tuottohinta.
