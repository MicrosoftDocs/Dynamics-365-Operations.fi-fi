---
title: "Hälytysten eräkäsittely"
description: "Tässä ohjeaiheessa on tietoja Microsoft Dynamics 365 for Finance and Operationsin hälytysten eräkäsittelystä."
author: tjvass
manager: AnnBe
ms.date: 06/08/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application user
ms.reviewer: sericks
ms.search.scope: Operations
ms.search.region: Global
ms.author: tjvass
ms.search.validFrom: 2018-3-30
ms.dyn365.ops.version: Platform update 15
ms.translationtype: HT
ms.sourcegitcommit: 764d4c9049d94ebcd55c61654aa2f4133b35bae6
ms.openlocfilehash: 74db212b2086bd7c94825d8a52d9a8b86ea7b739
ms.contentlocale: fi-fi
ms.lasthandoff: 08/08/2018

---

# <a name="batch-processing-of-alerts"></a>Hälytysten eräkäsittely
[!include [banner](../includes/banner.md)]

Eräkäsittelytoiminto käsittelee hälytykset Microsoft Dynamics 365 for Finance and Operations -sovelluksessa. Sinun on määritettävä eräkäsittely, ennen kuin hälytyksiä voidaan toimittaa.

Finance and Operations tukee seuraavaa kahta tapahtumatyyppiä:

- Tapahtumat, jotka muutoksiin perustuvat tapahtumat käynnistävät. Näitä tapahtumia kutsutaan myös tapahtumien luomiseksi tai poistamiseksi ja tapahtumien päivittämiseksi.
- Tapahtumat, jotka eräpäivät käynnistävät.

Voit määrittää kutakin tapahtumatyyppiä varten eräprosessin.
        
## <a name="batch-processing-for-change-based-events"></a>Muutokseen perustuvien tapahtumien eräkäsittely
Finance and Operations lukee kaikki muutoksiin perustuvat tapahtumat, jotka ovat tapahtuneet eräkäsittelyn edellisen suorituksen jälkeen. Muutokseen perustuvat tapahtumat sisältävät päivitykset kenttiin, tietueiden poistamisen ja tietueiden luonnin. Näitä tapahtumia verrataan hälytyssäännöissä määritettyihin ehtoihin. Kun tapahtuma vastaa säännön ehtoja, eräprosessi luo hälytyksen.

### <a name="frequency-for-change-based-events"></a>Muutoksiin perustuvien tapahtumien aikaväli
Voit määrittää muutoksiin perustuvia tapahtumia varten eräkäsittelytehtävän, joka käynnistää tapahtuman käsittelemisen nopeasti tapahtuman järjestelmään kirjaamisen jälkeen. Jos määrität erätyön useammin tapahtuvaksi, käyttäjät saavat hälytykset nopeammin muutosten tekemisen jälkeen. Usein suoritettava eräkäsittely voi kuitenkin vaikuttaa järjestelmän suorituskykyyn.

Toisaalta erätyö, jota ei suoriteta niin usein, ja joka ajoitetaan aikaan, jolloin järjestelmän kuormitus on alhainen, voi parantaa järjestelmän suorituskykyä. Harvoin suoritettava eräkäsittely ei kuitenkaan ehkä täytä käyttäjien hälytysvaatimuksia.

Kun määrität muutoksiin perustuvien tapahtumien eräkäsittelyn aikavälejä, ota tämän vuoksi huomioon hälytysten aikarajat ja koko järjestelmän suorituskyky. Tämä on erityisen tärkeää silloin, kun hälytyssääntöjä luovien käyttäjien määrä lisääntyy. Tiheys ei vaikuta käsiteltävien tapahtumien määrään. Jos useammat käyttäjät luovat sääntöjä, on suoritettava useampia tarkistuksia. Tietojen tämän tyyppinen vaihtaminen voi vaikuttaa järjestelmän suorituskykyyn.

#### <a name="the-risks-of-low-batch-frequency"></a>Pitkillä aikaväleillä toteutettujen eräkäsittelyjen riskit
Jos määrität muutosperustaisten tapahtumien eräkäsittelyn aikavälit pitkiksi, hälytyssääntöjen ehtojen tiedot voivat muuttua ennen erän käsittelyä. Voit menettää hälytykset tämän vuoksi.

Esimerkiksi hälytyssääntö on määritetty käynnistämään hälytys, kun tapahtuma on **asiakkaan yhteystietojen muutokset** ja ehtona on **asiakas = BB**. Toisin sanoen tapahtuma kirjataan, kun asiakkaan BB yhteyshenkilöä muutetaan. Eräkäsittelyjärjestelmä määritetään kuitenkin niin, että eräkäsittely tapahtuu tietojen merkintää harvemmin. Jos asiakkaan nimi muuttuu nimestä **BB** nimeksi **AA** ennen uuden tapahtuman käsittelyä, tietokannan tiedot eivät enää vastaa säännön ehtoa **asiakas = BB**. Tämän vuoksi hälytystä ei muodosteta, kun tapahtuma lopulta käsitellään.

### <a name="set-up-processing-for-change-based-alerts"></a>Muutokseen perustuvien hälytysten käsittelyn määrittäminen
1. Siirry kohtaan **Järjestelmän hallinta** &gt; **Kausittaiset tehtävät** &gt; **Hälytykset** &gt; **Muutokseen perustuvat hälytykset**.
2. Syötä **Muutokseen perustuvat hälytykset** -valintaikkunaan soveltuvat tiedot.

## <a name="batch-processing-for-due-date-events"></a>Eräpäivään perustuvien tapahtumien eräkäsittely
Finance and Operations havaitsee kaikki eräpäivien aiheuttamat tapahtumat, joita verrataan hälytyssääntöjen määrittämiin ehtoihin. Eräkäsittely luo hälytyksen, kun tapahtuma täyttää säännön ehdot.

### <a name="frequency-for-due-date-events"></a>Eräpäivään perustuvien tapahtumien aikaväli
Saatat haluta määrittää eräpäivään perustuvien tapahtumien eräkäsittelyn yöhön tai päivän hiljaisiin hetkiin järjestelmän kuormituksen tasapainottamiseksi. Erätyö on suositeltavaa määrittää suoritettavaksi vähintään kerran päivässä. Jos hälytysten halutaan lähtevän mahdollisimman nopeasti, määritä eräkäsittely niin, että se tapahtuu heti järjestelmän päivämäärän muutoksen jälkeen. Jos haluat luoda hälytyksiä eräpäivään perustuvista tapahtumista, jotka tapahtuvat sen jälkeen, kun erätyö on jo käsitellyt hälytykset, voit suorittaa erätyön uudelleen samana päivänä.

Esimerkiksi erätyö on suoritettu tiettynä päivänä. Tämän jälkeen luodaan ostotilaus, jonka eräpäivä käynnistää hälytyksen kyseisenä päivänä. Jos haluat saada hälytyksen samana päivänä, erätyö on suoritettava uudelleen ostotilauksen luonnin jälkeen. Jos et kuitenkaan suorita erätyötä uudelleen tuona päivänä, erätyö löytää seuraavana päivänä edellisinä päivinä käsittelemättä jääneet eräpäivään perustuvat tapahtumat.

> [!NOTE]
> Samasta eräpäiväperustaisesta tapahtumasta, joka täyttää samat ehdot, ei monisteta hälytystä, vaikka eräkäsittely suoritettaisiin useamman kerran päivässä. Hälytyksiä luodaan vain edellisen erätyön suorituksen jälkeen järjestelmään tehtyihin muutoksiin perustuvista eräpäivistä.

### <a name="batch-processing-window"></a>Eräkäsittelyikkuna
Yrityksen hälytyssääntöjen käsittely voidaan keskeyttää eri syistä. Näitä syitä ovat esimerkiksi lomat, järjestelmävirheet tai muut ongelmat, jotka estävät erätöiden suorittamisen joksikin aikaa.

Voit estää eräpäivähälytysten vanhentumisen sen vuoksi, ettei erätyötä ole suoritettu useisiin päivän, määrittämällä eräkäsittelyn aikavälin. Eräkäsittelyn ikkunan avulla ei voi estää erätyön suorittamista määritettyinä päivinä.

Jos määrität eräkäsittelyn ikkunan, hälytys lähetetään hälytyssäännön käsittelyn yhteydessä, vaikka hälytys ylittäisi eräpäivän ehdoissa määritetyn aikarajan. Hälytys lähetetään siihen asti kunnes tämän aikarajan ja eräkäsittelyn ikkunan määrittämä kausi vanhenee. Kun aikarajan ja eräkäsittelyn ikkunan määrittämä kausi on ohitettu, hälytystä ei enää lähetetä.

### <a name="set-up-processing-for-due-date-alerts"></a>Eräpäivään perustuvien hälytysten käsittelyn määrittäminen
1. Siirry kohtaan **Järjestelmän hallinta** &gt; **Kausittaiset tehtävät** &gt; **Hälytykset** &gt; **Eräpäivän hälytykset**.
2. Syötä **Eräpäivän hälytykset** -valintaikkunaan soveltuvat tiedot.

