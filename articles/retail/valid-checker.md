---
title: Vähittäismyynnin tapahtumien yhdenmukaisuuden tarkistaja
description: Tässä aiheessa kuvataan vähittäismyynnin tapahtumien yhdenmukaisuuden tarkistajan toiminnot ohjelmassa Microsoft Dynamics 365 for Retail.
author: josaw1
manager: AnnBe
ms.date: 01/08/2019
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2019-01-15
ms.dyn365.ops.version: 10
ms.openlocfilehash: db01a12b92574b41f1f4fe7281c23992e0d36027
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/29/2019
ms.locfileid: "302231"
---
# <a name="retail-transaction-consistency-checker"></a>Vähittäismyynnin tapahtumien yhdenmukaisuuden tarkistaja


[!include [banner](includes/banner.md)]
[!include [preview banner](includes/preview-banner.md)]

Tässä aiheessa kuvataan vähittäismyynnin tapahtumien yhdenmukaisuuden tarkistajan, joka on käytössä versiosta 8.1.3. alkaen, toiminnot ohjelmassa Microsoft Dynamics 365 for Finance and Operations. Yhdenmukaisuuden tarkistaja tunnistaa ja osoittaa yhtäpitämättömät tapahtumat, ennen kuin laskelmien kirjaamisprosessi ottaa ne käsittelyyn.

Kun laskelma kirjataan Retailissa, kirjaus saattaa epäonnistua vähittäismyynnin tauluissa olevien yhtäpitämättömien tietojen johdosta. Ongelma tiedoissa saattaa johtua odottamattomista ongelmista myyntipistesovelluksessa, tai siitä, että tapahtumat on tuotu virheellisesti kolmannen osapuolen myyntipistejärjestelmistä. Nämä ristiriidat voivat näyttää esimerkiksi seuraavanlaisilta: 

  - Tapahtuman kokonaissumma otsikkotaulussa ei vastaa riveillä olevaa tapahtuman kokonaissummaa.
  - Otsikkotaulun rivimäärä ei vastaa transaktiotaulun rivimäärää.
  - Otsikkotaulussa olevat verot eivät vastaa riveillä olevaa veron määrää. 
  
Kun laskelmien kirjausprosessi havaitsee epäyhtenäisiä tapahtumia, luodaan yhteensopimattomia myyntilaskuja ja maksutietoja, ja koko laskelmien kirjausprosessi epäonnistuu tämän seurauksena. Laskelmien palauttaminen sellaisesta tilasta vaatii monimutkaisia tietojen korjauksia moneen transaktiotauluun. Vähittäismyynnin tapahtumien yhdenmukaisuuden tarkistaja estää tällaiset ongelmat.

Seuraavassa kaaviossa havainnollistetaan kirjausprosessi, jossa tapahtumien yhdenmukaisuuden tarkistaja on käytössä.

![Laskelman kirjausprosessi, jossa tapahtumien yhdenmukaisuuden tarkistaja on käytössä](./media/validchecker.png "Laskelman kirjausprosessi, jossa tapahtumien yhdenmukaisuuden tarkistaja on käytössä")

**Vahvista myymälän tapahtumat** -eräajoprosessi tarkistaa seuraavien seikkojen yhdenmukaisuuden vähittäismyynnin transaktiotauluista.

- Asiakkaan tili - Tarkistaa, että vähittäismyynnin transaktiotauluissa oleva asiakastili on olemassa asiakkaan alkuperäisissä tiedoissa pääkonttorissa.
- Rivien määrä - Tarkistaa, että rivien määrä transaktioiden otsikkotaulussa vastaa myynnin transaktiotauluissa olevien rivien määrää.

## <a name="set-up-the-consistency-checker"></a>Määritä yhdenmukaisuuden tarkistaja
Määritä "Vahvista myymälän tapahtumat" -eräajoprosessi tapahtumaan säännöllisesti paikassa **Vähittäismyynti \> Vähittäismyynti IT \> Myyntipisteen laskenta**. Eräajoprosessi voidaan aikatauluttaa myymälän organisaatiohierarkian perusteella samaan tapaan kuin "Laskelman laskeminen erässä" - ja "Laskelman kirjaaminen erässä" -prosessit on määritetty. Suosittelemme määrittelemään tämän eräajoprosessin käynnistymään useita kertoja päivässä ja aikatauluttamaan sen siten, että se käynnistyy jokaisen P-tehtävän suorituskerran lopuksi.

## <a name="results-of-validation-process"></a>Tarkistusprosessin tulokset
Eräajoprosessin suorittaman tarkistuksen tulokset yhdistetään asianmukaiseen vähittäismyynnin tapahtumaan. **Vahvistuksen tila** -kenttä vähittäismyynnin tapahtumatietueessa on joko **Onnistui** tai **Virhe**, ja edellisen tarkistusajon päivämäärä näkyy **Edellisen tarkistuksen aika** -kentässä.

Katso kuvaavampi tarkistuksen epäonnistumiseen liittyvä virheteksti valitsemalla asiaankuuluva vähittäismyymälän transaktiotietue ja napauttamalla **Oikeellisuustarkistusvirheet**-painiketta.

Tapahtumia, jotka eivät läpäise tarkistusta, ja tapahtumia, joita ei ole vielä tarkistettu, ei tuoda laskelmiin. ”Laske laskelma” -prosessin aikana käyttäjille lähetetään ilmoitus, jos on tapahtumia, jotka olisi voitu sisällyttää laskelmaan mutta joita ei ole siihen sisällytetty.

Jos löydetään tarkistusvirhe, ainoa tapa sen korjaamiseksi on ottaa yhteyttä Microsoftin tukeen. Tulevissa versioissa ohjelmaan lisätään toiminto, jonka avulla käyttäjät voivat korjata käyttöliittymän kautta ne tietueet, jotka aiheuttivat virheen. Tapahtumaloki- ja auditointiominaisuudet tulevat myös saataville muutoshistorian seurantaa varten.

> [!NOTE]
> Tarkistussääntöjä useamman mahdollisen tilanteen kattamiseksi lisätään tulevissa versioissa.
