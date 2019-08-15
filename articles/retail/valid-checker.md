---
title: Vähittäismyynnin tapahtumien yhdenmukaisuuden tarkistaja
description: Tässä aiheessa kuvataan vähittäismyynnin tapahtumien yhdenmukaisuuden tarkistajan toiminnot ohjelmassa Microsoft Dynamics 365 for Retail.
author: josaw1
manager: AnnBe
ms.date: 05/30/2019
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
ms.openlocfilehash: f94a674e021d4f23480433440cd239b851491d87
ms.sourcegitcommit: 2c73749779274e0b0abbcb4041bbc1df0fb6d6e4
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 07/26/2019
ms.locfileid: "1790418"
---
# <a name="retail-transaction-consistency-checker"></a>Vähittäismyynnin tapahtumien yhdenmukaisuuden tarkistaja


[!include [banner](includes/banner.md)]
[!include [preview banner](includes/preview-banner.md)]

Tässä aiheessa kuvataan vähittäismyynnin tapahtumien yhdenmukaisuuden tarkistajan, joka on käytössä versiosta 8.1.3. alkaen, toiminnot ohjelmassa Microsoft Dynamics 365 for Finance and Operations. Yhdenmukaisuuden tarkistaja tunnistaa ja osoittaa ei-yhdenmukaiset tapahtumat, ennen kuin laskelmien kirjaamisprosessi ottaa ne käsittelyyn.

Kun laskelma kirjataan Microsoft Dynamics 365 for Retail -sovelluksessa, kirjaus saattaa epäonnistua vähittäismyynnin tauluissa olevien ei-yhdenmukaisten tietojen johdosta. Ongelma tiedoissa saattaa johtua odottamattomista ongelmista myyntipistesovelluksessa, tai siitä, että tapahtumat on tuotu virheellisesti kolmannen osapuolen myyntipistejärjestelmistä. Nämä ristiriidat voivat näyttää esimerkiksi seuraavanlaisilta: 

- Tapahtuman kokonaissumma otsikkotaulussa ei vastaa riveillä olevaa tapahtuman kokonaissummaa.
- Otsikkotaulun rivimäärä ei vastaa transaktiotaulun rivimäärää.
- Otsikkotaulussa olevat verot eivät vastaa riveillä olevaa veron määrää. 

Kun laskelmien kirjausprosessi havaitsee epäyhtenäisiä tapahtumia, luodaan yhteensopimattomia myyntilaskuja ja maksutietoja, ja koko laskelmien kirjausprosessi epäonnistuu tämän seurauksena. Laskelmien palauttaminen sellaisesta tilasta vaatii monimutkaisia tietojen korjauksia moneen transaktiotauluun. Vähittäismyynnin tapahtumien yhdenmukaisuuden tarkistaja estää tällaiset ongelmat.

Seuraavassa kaaviossa havainnollistetaan kirjausprosessi, jossa tapahtumien yhdenmukaisuuden tarkistaja on käytössä.

![Laskelman kirjausprosessi, jossa vähittäismyyntitapahtumien yhdenmukaisuuden tarkistaja on käytössä](./media/validchecker.png "Laskelman kirjausprosessi, jossa vähittäismyyntitapahtumien yhdenmukaisuuden tarkistaja on käytössä")

**Vahvista myymälän tapahtumat** -eräprosessi tarkistaa seuraavien seikkojen yhdenmukaisuuden vähittäismyynnin transaktiotauluista.

- **Asiakkaan tili** - Tarkistaa, että vähittäismyynnin transaktiotauluissa oleva asiakastili on olemassa asiakkaan alkuperäisissä tiedoissa pääkonttorissa.
- **Rivien määrä** - Tarkistaa, että rivien määrä transaktioiden otsikkotaulussa vastaa myynnin transaktiotauluissa olevien rivien määrää.
- **Hinta sisältää veron** – Tarkistaa, että **Hinta sisältää veron** -parametri on yhdenmukainen kaikilla tapahtumariveillä.
- **Maksun summa** -tarkistaa, että maksut vastaavat otsikon maksuja.
- **Bruttosumma** – Tarkistaa, että otsikon bruttosumma on sama kuin rivien nettosummien ja veron määrä laskettuna yhteen.
- **Nettosumma** – Tarkistaa, että otsikon nettosumma on sama kuin rivien nettosummien ja veron määrä laskettuna yhteen.
- **Liika-/alimaksu** – Tarkistaa, että otsikon bruttosumman ja maksusumman välinen ero ei ylitä määritettyä ali- ja ylimaksun enimmäismäärää.
- **Alennuksen summa** – Tarkistaa, että vähittäismyyntitapahtumien rivien taulukon alennuksen summan alennustaulukoiden alennuksen summa on yhdenmukainen ja että otsikon alennuksen summa on sama kuin rivien alennusten summien kokonaismäärä.
- **Rivialennus** – Tarkistaa, että tapahtumarivin rivialennus on kaikkien tapahtumariviin liittyvien alennustaulukon rivien summa.
- **Lahjakorttinimike** – Retail ei tue lahjakorttinimikkeiden palautusta. Lahjakortin saldo voidaan kuitenkin lunastaa. Kaikki lahjakorttinimikkeet, jotka on käsitelty palautusrivinä lunastusrivin sijaan, epäonnistuvat laskelman kirjausprosessissa. Lahjakorttien tarkistusprosessin avulla voidaan varmistaa, että vähittäismyyntitapahtuman taulukoiden kaikki palautuksen lahjakorttirivinimikkeet ovat lahjakortin lunastuksen rivejä.
- **Negatiivinen hinta** – Tarkistaa, että negatiivisen hinnan tapahtumarivejä ei ole.
- **Nimike ja variantti** – Tarkistaa, että tapahtumarivien nimikkeet ja variantit ovat nimikkeen ja variantin päätiedostossa.
- **Veron summa** -verotietueen oikeellisuustarkistus vastaa rivien verosummia. 

## <a name="set-up-the-consistency-checker"></a>Yhdenmukaisuuden tarkistajan määrittäminen

Määritä "Vahvista myymälän tapahtumat" -eräprosessi tapahtumaan säännöllisesti paikassa **Vähittäismyynti \> Vähittäismyynnin IT \> Myyntipisteen laskenta**. Eräprosessi voidaan aikatauluttaa myymälän organisaatiohierarkian perusteella samaan tapaan kuin "Laskelman laskeminen erässä" - ja "Laskelman kirjaaminen erässä" -prosessit on määritetty. Suosittelemme määrittelemään tämän eräprosessin käynnistymään useita kertoja päivässä ja aikatauluttamaan sen siten, että se käynnistyy jokaisen P-tehtävän suorituskerran lopuksi.

## <a name="results-of-validation-process"></a>Tarkistusprosessin tulokset

Eräprosessin suorittaman tarkistuksen tulokset yhdistetään asianmukaiseen vähittäismyynnin tapahtumaan. **Vahvistuksen tila** -kenttä vähittäismyynnin tapahtumatietueessa on joko **Onnistui** tai **Virhe**, ja edellisen tarkistusajon päivämäärä näkyy **Edellisen tarkistuksen aika** -kentässä.

Katso kuvaavampi tarkistuksen epäonnistumiseen liittyvä virheteksti valitsemalla asiaankuuluva vähittäismyymälän transaktiotietue ja napauttamalla **Oikeellisuustarkistusvirheet**-painiketta.

Tapahtumia, jotka eivät läpäise tarkistusta, ja tapahtumia, joita ei ole vielä tarkistettu, ei tuoda laskelmiin. ”Laske laskelma” -prosessin aikana käyttäjille lähetetään ilmoitus, jos on tapahtumia, jotka olisi voitu sisällyttää laskelmaan mutta joita ei ole siihen sisällytetty.

Jos löydetään tarkistusvirhe, ainoa tapa sen korjaamiseksi on ottaa yhteyttä Microsoftin tukeen. Tulevissa versioissa ohjelmaan lisätään toiminto, jonka avulla käyttäjät voivat korjata käyttöliittymän kautta ne tietueet, jotka aiheuttivat virheen. Tapahtumaloki- ja auditointiominaisuudet tulevat myös saataville muutoshistorian seurantaa varten.

> [!NOTE]
> Tarkistussääntöjä useamman mahdollisen tilanteen kattamiseksi lisätään tulevissa versioissa.
