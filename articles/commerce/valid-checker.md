---
title: Vähittäismyynnin tapahtumien yhdenmukaisuuden tarkistus
description: Tässä aiheessa kuvataan tapahtumien yhdenmukaisuuden tarkistuksen toiminnot ohjelmassa Dynamics 365 Commerce.
author: josaw1
ms.date: 10/07/2020
ms.topic: index-page
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2019-01-15
ms.dyn365.ops.version: 10
ms.openlocfilehash: c8ba0f99743984860119deb96c889f5d62e1728c8772b9e6786d371690b61489
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/05/2021
ms.locfileid: "6741729"
---
# <a name="retail-transaction-consistency-checker"></a>Vähittäismyynnin tapahtumien yhdenmukaisuuden tarkistus

[!include [banner](includes/banner.md)]

Tässä aiheessa kuvataan tapahtumien yhdenmukaisuuden tarkistuksen toiminnot ohjelmassa Microsoft Dynamics 365 Commerce. Yhdenmukaisuuden tarkistus tunnistaa ja osoittaa ei-yhdenmukaiset tapahtumat, ennen kuin laskelmien kirjaamisprosessi ottaa ne käsittelyyn.

Kun laskelma kirjataan, kirjaus saattaa epäonnistua kaupan transaktiotauluissa olevien ei-yhdenmukaisten tietojen johdosta. Ongelma tiedoissa saattaa johtua odottamattomista ongelmista myyntipistesovelluksessa, tai siitä, että tapahtumat on tuotu virheellisesti kolmannen osapuolen myyntipistejärjestelmistä. Nämä ristiriidat voivat näyttää esimerkiksi seuraavanlaisilta: 

- Tapahtuman kokonaissumma otsikkotaulussa ei vastaa riveillä olevaa tapahtuman kokonaissummaa.
- Otsikkotaulun rivimäärä ei vastaa transaktiotaulun rivimäärää.
- Otsikkotaulussa olevat verot eivät vastaa riveillä olevaa veron määrää. 

Kun laskelmien kirjausprosessi havaitsee epäyhtenäisiä tapahtumia, luodaan yhteensopimattomia myyntilaskuja ja maksutietoja, ja koko laskelmien kirjausprosessi epäonnistuu tämän seurauksena. Laskelmien palauttaminen sellaisesta tilasta vaatii monimutkaisia tietojen korjauksia moneen transaktiotauluun. Tapahtumien yhdenmukaisuuden tarkistus estää tällaiset ongelmat.

Seuraavassa kaaviossa havainnollistetaan kirjausprosessi, jossa tapahtumien yhdenmukaisuuden tarkistus on käytössä.

![Laskelman kirjausprosessi ja tapahtuman yhdenmukaisuuden tarkistus.](./media/validchecker.png "Laskelman kirjausprosessi ja vähittäismyyntitapahtuman yhdenmukaisuuden tarkistus")

**Vahvista myymälän tapahtumat** -eräprosessi tarkistaa seuraavien seikkojen yhdenmukaisuuden kaupan transaktiotauluista.

- **Asiakkaan tili** – Tarkistaa, että transaktiotauluissa oleva asiakastili on olemassa asiakkaan alkuperäisissä tiedoissa pääkonttorissa.
- **Rivien määrä** – Tarkistaa, että rivien määrä transaktioiden otsikkotaulussa vastaa myynnin transaktiotauluissa olevien rivien määrää.
- **Hinta sisältää veron** – Tarkistaa, että **Hinta sisältää veron** -parametri on yhdenmukainen eri tapahtumariveillä ja että myyntirivin hinta noudattaa Hinta sisältää veron- ja verovapauskonfiguraatiota.
- **Maksun summa** – Tarkistaa, että maksut vastaavat otsikon maksuja, samalla eritellen pyöristyskonfiguraatiota kirjanpidossa.
- **Bruttosumma** – Tarkistaa, että otsikon bruttosumma on sama kuin rivien nettosummien ja veron määrä laskettuna yhteen, samalla eritellen pyöristyskonfiguraatiota kirjanpidossa.
- **Nettosumma** – Tarkistaa, että otsikon nettosumma on sama kuin rivien nettosummat laskettuna yhteen, samalla eritellen pyöristyskonfiguraatiota kirjanpidossa.
- **Liika-/alimaksu** – Tarkistaa, että otsikon bruttosumman ja maksusumman välinen ero ei ylitä määritettyä ali- ja ylimaksun enimmäismäärää, samalla eritellen pyöristyskonfiguraatiota kirjanpidossa.
- **Alennuksen summa** – Tarkistaa, että vähittäismyyntitapahtumien rivien taulukon alennuksen summan alennustaulukoiden alennuksen summa on yhdenmukainen ja että otsikon alennuksen summa on sama kuin rivien alennusten summien kokonaismäärä, samalla eritellen pyöristyskonfiguraatiota kirjanpidossa.
- **Rivialennus** – Tarkistaa, että tapahtumarivin rivialennus on kaikkien tapahtumariviin liittyvien alennustaulukon rivien summa.
- **Lahjakorttinimike** – Commerce ei tue lahjakorttinimikkeiden palautusta. Lahjakortin saldo voidaan kuitenkin lunastaa. Kaikki lahjakorttinimikkeet, jotka on käsitelty palautusrivinä lunastusrivin sijaan, epäonnistuvat laskelman kirjausprosessissa. Lahjakorttien tarkistusprosessin avulla voidaan varmistaa, että transaktiotaulujen kaikki palautuksen lahjakorttirivinimikkeet ovat lahjakortin lunastuksen rivejä.
- **Negatiivinen hinta** – Tarkistaa, että negatiivisen hinnan tapahtumarivejä ei ole.
- **Nimike ja variantti** – Tarkistaa, että tapahtumarivien nimikkeet ja variantit ovat nimikkeen ja variantin päätiedostossa.
- **Veron summa** – Tarkistaa, että verotietueen oikeellisuustarkistus vastaa rivien verosummia.
- **Sarjanumero** – Tarkistaa, että sarjanumero on sarjanumeroseurannassa olevien nimikkeiden tapahtumariveillä.
- **Allekirjoita** – Tarkistaa, että määrän ja nettosumman etumerkki on sama kaikilla tapahtumariveillä.
- **Liiketoiminnan päivämäärä** – Tarkistaa, että tapahtumien liiketoiminnan päivämäärien tilikaudet ovat avoimia.
- **Veloitukset** – Tarkistaa, että otsikon ja rivin veloitussumma on hinnan mukainen, ottaen huomioon lukien vero- ja verovapauskonfiguraation.

## <a name="set-up-the-consistency-checker"></a>Yhdenmukaisuuden tarkistuksen määrittäminen

Määritä Tarkista myymälän tapahtumat -eräprosessi tapahtumaan säännöllisesti kohdassa **Retail ja Commerce \> Retailin ja Commercen IT \> Myyntipistekirjaus**. Eräprosessi voidaan aikatauluttaa myymälän organisaatiohierarkian perusteella samaan tapaan kuin "Laskelman laskeminen erässä"- ja "Laskelman kirjaaminen erässä" -prosessit on määritetty. Suosittelemme määrittelemään tämän eräprosessin käynnistymään useita kertoja päivässä ja aikatauluttamaan sen siten, että se käynnistyy jokaisen P-tehtävän suorituskerran lopuksi.

## <a name="results-of-validation-process"></a>Tarkistusprosessin tulokset

Eräprosessin suorittaman tarkistuksen tulokset yhdistetään asianmukaiseen tapahtumaan. **Vahvistuksen tila** -kenttä tapahtumatietueessa on joko **Onnistui** tai **Virhe**, ja edellisen tarkistusajon päivämäärä näkyy **Edellisen tarkistuksen aika** -kentässä.

Katso kuvaavampi tarkistuksen epäonnistumiseen liittyvä virheteksti valitsemalla asiaankuuluva transaktiotietue ja napauttamalla **Oikeellisuustarkistusvirheet**-painiketta.

Tapahtumia, jotka eivät läpäise tarkistusta, ja tapahtumia, joita ei ole vielä tarkistettu, ei tuoda laskelmiin. ”Laske laskelma” -prosessin aikana käyttäjille lähetetään ilmoitus, jos on tapahtumia, jotka olisi voitu sisällyttää laskelmaan mutta joita ei ole siihen sisällytetty.

Jos löydetään tarkistusvirhe, ainoa tapa sen korjaamiseksi on ottaa yhteyttä Microsoftin tukeen. Tulevissa versioissa ohjelmaan lisätään toiminto, jonka avulla käyttäjät voivat korjata käyttöliittymän kautta ne tietueet, jotka aiheuttivat virheen. Tapahtumaloki- ja auditointiominaisuudet tulevat myös saataville muutoshistorian seurantaa varten.

> [!NOTE]
> Tarkistussääntöjä useamman mahdollisen tilanteen kattamiseksi lisätään tulevissa versioissa.


[!INCLUDE[footer-include](../includes/footer-banner.md)]