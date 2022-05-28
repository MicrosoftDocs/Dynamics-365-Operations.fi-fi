---
title: Painotettu keskimääräinen päivämäärä sisältää fyysisen arvon ja merkinnän
description: Painotetun keskiarvon päivämäärä on painotetun keskiarvon periaatteeseen perustuva varastomalli, jossa varasto-otot arvotetaan varastoon vastaanotettujen nimikkeiden keskiarvon mukaan kunakin erillisenä päivänä varaston sulkemiskauden aikana.
author: JennySong-SH
ms.date: 03/04/2022
ms.topic: article
ms.search.form: InventJournalLossProfit, InventMarking, InventModelGroup, SalesTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: 28991
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1497cb08f4cc5a455c832b9bf125c309cd90aa3d
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/03/2022
ms.locfileid: "8672119"
---
# <a name="weighted-average-date-with-include-physical-value-and-marking"></a>Painotettu keskimääräinen päivämäärä sisältää fyysisen arvon ja merkinnän

[!include [banner](../includes/banner.md)]

*Painotettu keskimääräinen päivämäärä* on varastomalli, joka perustuu keskiarvoon, joka lasketaan kertomalla jokainen komponentti (tuotetapahtuma) tekijällä (kustannushinta), joka kuvastaa sen tärkeyttä (määrää) kauden jokaisena päivänä. Toisin sanoen tämä varastomalli määrittää liikkeeseenlaskutapahtumien kustannukset joka päivä vastaanotetun kaiken varaston keskiarvon perusteella sekä mahdollisen edellisen päivän varaston.

Kun suoritat varaston sulkemisen käyttämällä painotetun keskiarvon päivämäärän varastomallia, selvityksen luomiseen voidaan käyttää kahta menetelmää. Yleensä kaikki vastaanotot täsmäytetään suhteessa virtuaalivarastostaottoon, joka sisältää vastaanotetun kokonaismäärän ja -arvon. Tällä virtuaalivarastostaotolla on vastaava virtuaalivastaanotto, josta varastostaotot täsmäytetään. Näin kaikille varastostaotoille tulee kunakin päivänä sama keskimääräinen kustannus. Virtuaalista varastostaottoa ja virtuaalivastaanottoa voidaan pitää virtuaalisiirtona. Tätä virtuaalisiirtoa kutsutaan *painotetun keskiarvon varaston sulkemissiirroksi*. Siitä syystä tätä selvitysmenetelmä tunnetaan *painotetun keskiarvon yhteenvetotilityksenä*. Jos vastaanottoja on vain yksi, kaikki varastostaotot voi täsmäyttää siitä, eikä virtuaalisiirtoa luoda. Tätä selvitysmenetelmää kutsutaan *suoraksi tilitykseksi*. Kaikki varaston sulkemisen jälkeen käsillä oleva varasto arvostetaan edellisen kauden viimeisen päivän painotettuun keskiarvoon ja sisällytetään seuraavan kauden painotetun keskiarvon päivämäärälaskelmaan.

Voit ohittaa painotetun keskiarvopäivän periaatteen merkitsemällä varastotapahtumat niin, että tietyn nimikkeen vastaanotto selvitetään tiettyä varastostaottoa vasten. Säännöllinen varaston sulkeminen vaaditaan, kun käytät painotetun keskiarvon päivämäärän varastomallia selvitysten luomiseen ja liikkeeseenlaskujen arvon säätämiseen painotetun keskiarvon päivämäärän periaatteen mukaisesti. Varasto-ottotapahtumat arvotetaan fyysisten ja taloudellisten päivitysten suorituksen keskiarvon mukaan, kunnes varaston sulkeminen suoritetaan. Jos et käytä merkintää, juokseva keskiarvo lasketaan, kun fyysinen tai taloudellinen päivitys suoritetaan.

Varaston painotetun keskiarvopäivän kustannuslaskentamenetelmä lasketaan seuraavan kaavan avulla kunakin päivänä:

*Cost* = \[(*Q*<sub>*b*</sub> × *P*<sub>*b*</sub>) + &#x2211;<sub>*n*</sub>(*Q*<sub>*n*</sub> × *P*<sub>*n*</sub>)\] ÷ (*Q*<sub>*b*</sub> + &#x2211;<sub>*n*</sub>*Q*<sub>*n*</sub>)

- *Q* = Tapahtuman määrä
- *P* = Tapahtuman hinta

Toisin sanoen painotettu keskiarvokustannus on sama kuin alkumäärä kertaa ensimmäinen hinta ja jokaisen vastaanottomäärän summa kertaa vastaanottohinta, kaikki jaettuna alkumäärällä ja vastaanottomäärien summalla.

Varaston sulkemisen aikana laskenta suoritetaan päivittäin.

> [!NOTE]
> Lisätietoja selvityksistä on kohdassa [Varaston sulkeminen](inventory-close.md).

Seuraavissa esimerkeissä kuvataan painotetun keskiarvopäivän käytön vaikutusta viidessä eri konfiguraatiossa:

- Painotetun keskiarvon päivämäärän suora selvitys ilman **Sisällytä fyysinen arvo** -asetusta
- Painotetun keskiarvon päivämäärän yhteenvetoselvitys ilman **Sisällytä fyysinen arvo** -asetusta
- Painotetun keskiarvon päivämäärän suora selvitys **Sisällytä fyysinen arvo** -asetuksella
- Painotetun keskiarvon päivämäärän yhteenvetoselvitys **Sisällytä fyysinen arvo** -asetuksella
- Painotetun keskiarvon päivämäärä käyttäen merkintää

## <a name="weighted-average-date-direct-settlement-when-the-include-physical-value-option-isnt-used"></a>Painotetun keskiarvon päivämäärän suora selvitys ilman Sisällytä fyysinen arvo -asetusta

Suoran täsmäytyksen periaate luo täsmäytykset suoraan vastaanottojen ja varasto-ottojen välille luomatta uusia varastotapahtumia. Järjestelmä käyttää tätä suoran selvityksen periaatetta seuraavissa tilanteissa:

- Kauden aikana on kirjattu yksi vastaanotto ja vähintään yksi varastostaotto.
- Kauden aikana on kirjattu vain varastostaottoja, ja varasto sisältää käytettävissä olevia nimikkeitä aiemmasta sulkemisesta.

Tässä esimerkissä vapautetun tuotteen **nimikemalliryhmän** **Sisällytä fyysinen arvo** -sivun valinta on tyhjä. Seuraavassa kaaviossa on kuvattu näitä tapahtumia:

**1. päivä:**

- 1a. Varaston fyysinen vastaanotto määrälle 10 yksikkökustannuksen ollessa 10,00 USD.
- 1b. Varaston taloudellinen vastaanotto määrälle 10 yksikkökustannuksen ollessa 10,00 USD.
- 2a. Varaston fyysinen vastaanotto määrälle 10 yksikkökustannuksen ollessa 20,00 USD.
- 3a. Varaston fyysinen varastostaotto määrälle 1 kustannushintaan 10,00 USD (taloudellisesti kirjattujen tapahtumien käyttökeskiarvo).
- 3b. Varaston taloudellinen varastostaotto määrälle 1 kustannushintaan 10,00 USD (taloudellisesti kirjattujen tapahtumien käyttökeskiarvo).

**2. päivä:**

- 4a. Varaston fyysinen vastaanotto määrälle 1 yksikkökustannuksen ollessa 25,00 USD.
- 5a. Varaston fyysinen vastaanotto määrälle 1 yksikkökustannuksen ollessa 30,00 USD.
- 5b. Varaston taloudellinen vastaanotto määrälle 1 yksikkökustannuksen ollessa 30,00 USD.
- 6a. Varaston taloudellinen varastostaotto määrälle 1 kustannushintaan 20,00 USD / kappale (taloudellisesti kirjattujen tapahtumien käyttökeskiarvo).

**3. päivä:**

- 7\. Varaston sulkeminen on suoritettu. Päivämäärän painotetun keskiarvon menetelmään perustuen järjestelmä käyttää suoraselvitystapaa 30. joulukuuta (30.12.), koska vain yksi kuitti päivitetään taloudellisesti 30.12. Tässä esimerkissä luodaan yksi tilitys tapahtumien 1b ja 3b välille. 10,00 USD:n oikaisu tehdään tapahtuman 3b arvon nostamiseksi 20,00:een. Oikaisua tai selvitystä ei tehdä 31. joulukuuta (31.12.), koska 31.12. ei ole taloudellisesti päivitettyjä asioita.

Seuraava kaavio kuvaa tämän tapahtumasarjan ja painotetun keskimääräisen varastomallin ja suoran selvitysperiaatteen käytön vaikutukset ilman **Sisällytä fyysinen arvo** -vaihtoehtoa.

![Painotetun keskiarvon päivämäärän suora selvitys ilman Sisällytä fyysinen arvo -asetusta.](media/weighted-average-date-direct-settlement-without-include-physical-value.png)

**Kaavion selite:**

- Pystysuorat nuolet kuvaavat varastotapahtumia.
- Fyysisiä tapahtumia kuvastavat lyhyemmät vaalean harmaat nuolet.
- Kirjanpitotapahtumia kuvastavat pidemmät mustat nuolet.
- Akselin yläpuolella olevat pystysuorat nuolet kuvaavat vastaanottoja varastoon.
- Akselin alapuolella olevat pystysuorat nuolet kuvaavat varastostaottoja.
- Kukin uusi vastaanotto- tai varastostaottotapahtuma on merkitty uudella otsikolla.
- Kukin pystysuora nuoli on merkitty järjestystunnuksella, kuten *1a*. Tunnukset ilmaisevat varastotapahtumakirjausten järjestyksen aikajanalla.
- Päivämäärät erotetaan ohuilla mustilla pystyviivoilla. Päivämäärät näkyvät kaavion alareunassa.
- Varaston sulkemiset on kuvattu punaisilla pystysuorilla katkoviivoilla.
- Varaston sulkemisen suorittamat selvitykset on kuvattu punaisilla katkoviivanuolilla, jotka kulkevat vinosti vastaanotosta varastostaottoon.

## <a name="weighted-average-date-summarized-settlement-when-the-include-physical-value-option-isnt-used"></a>Painotetun keskiarvon päivämäärän yhteenvetoselvitys ilman Sisällytä fyysinen arvo -asetusta

Kun jaksolla on useita kuitteja, painotettu keskimääräinen päivämäärä käyttää yhteenvetolaskennan periaatetta, jossa kaikki yhden päivän tulot kootaan tapahtumaksi, jonka nimi on *Painotetun keskiarvon varaston sulkeminen*. Kaikki päivän vastaanotot täsmäytetään luodun uuden varastotapahtuman varastostaottoa vastaan. Kaikki päivän varastostaotot täsmäytetään uuden varastotapahtuman vastaanottoa vastaan. Jos on olemassa käytettävissä olevaa varastoa varaston sulkemisen jälkeen, käytettävissä olevan varaston arvo sisällytetään painotetun keskiarvon varaston sulkemistapahtumien vastaanottotapahtumaan.

Seuraavassa kaaviossa on kuvattu näitä tapahtumia:

**1. päivä:**

- 1a. Varaston fyysinen vastaanotto määrälle 1 yksikkökustannuksen ollessa 10,00 USD.
- 1b. Varaston taloudellinen vastaanotto määrälle 1 yksikkökustannuksen ollessa 10,00 USD.
- 2a. Varaston fyysinen vastaanotto määrälle 1 yksikkökustannuksen ollessa 20,00 USD.
- 2b. Varaston taloudellinen vastaanotto määrälle 1 yksikkökustannuksen ollessa 22,00 USD.
- 3a. Varaston fyysinen varastostaotto määrälle 1 kustannushintaan 16,00 USD (taloudellisesti kirjattujen tapahtumien käyttökeskiarvo).
- 3b. Varaston taloudellinen varastostaotto määrälle 1 kustannushintaan 16,00 USD (taloudellisesti kirjattujen tapahtumien käyttökeskiarvo).

**2. päivä:**

- 4a. Varaston fyysinen vastaanotto määrälle 1 yksikkökustannuksen ollessa 25,00 USD.
- 5a. Varaston fyysinen vastaanotto määrälle 1 yksikkökustannuksen ollessa 30,00 USD.
- 5b. Varaston taloudellinen vastaanotto määrälle 1 yksikkökustannuksen ollessa 30,00 USD.
- 6a. Varaston fyysinen varastostaotto määrälle 1 kustannushintaan 23,00 USD (taloudellisesti kirjattujen tapahtumien käyttökeskiarvo).

**3. päivä:**

- 7\. Varaston sulkeminen on suoritettu.
- 7a. Painotetun keskiarvon varaston sulkemistapahtuman rahoituksellinen varasto-otto muodostetaan, jotta saadaan varaston kaikkien rahoituksellisten vastaanottojen täsmäytysten yhteenveto.

    - Tapahtuma 1b tilitetään määrälle 1 ja tilitetty summa on 10,00 USD.
    - Tapahtuma 2b tilitetään määrälle 1 ja tilitetty summa on 22,00 USD.
    - Tapahtuma 7a luodaan määrälle 2 ja tilitetty summa on 32,00 USD. Tämä tapahtuma vastakirjaa kahden kaudella taloudellisesti päivitetyn vastaanottotapahtuman summan.

- 7b. Painotetun keskiarvon varaston sulkemistapahtuman taloudellinen vastaanotto luodaan vastatapahtumaksi taloudellisesti kirjatuille varasto-otoille.

    - Tapahtuma 3b tilitetään määrälle 1 ja tilitetty summa on 16,00 USD. Tapahtumaa ei oikaista, koska se on taloudellisesti kirjattujen tapahtumien painotettu keskiarvo joulukuun 1. päivänä (1.12.).
    - Tapahtuma 7b luodaan määrälle 2, jonka rahamäärä on 32,00 USD ja maksettu summa USD 16,00, tapahtuman 3b kuittaamiseksi. Tämä tapahtuma vastakirjaa yhden kaudella taloudellisesti päivitetyn varasto-ottotapahtuman summan. Tapahtuma jää avoimeksi, koska sitä on vielä yksi.

Seuraava kaavio kuvaa painotetun keskiarvon varastomallin ja yhteenvetotäsmäytyksen vaikutusta tähän tapahtumien sarjaan, kun **Sisällytä fyysinen arvo** -vaihtoehtoa ei käytetä.

![Painotetun keskiarvon päivämäärän yhteenvetoselvitys ilman Sisällytä fyysinen arvo -asetusta.](media/weighted-average-date-summarized-settlement-without-include-physical-value.png)

**Kaavion selite:**

- Pystysuorat nuolet kuvaavat varastotapahtumia.
- Fyysisiä tapahtumia kuvastavat lyhyemmät vaalean harmaat nuolet.
- Kirjanpitotapahtumia kuvastavat pidemmät mustat nuolet.
- Akselin yläpuolella olevat pystysuorat nuolet kuvaavat vastaanottoja varastoon.
- Akselin alapuolella olevat pystysuorat nuolet kuvaavat varastostaottoja.
- Kukin uusi vastaanotto- tai varastostaottotapahtuma on merkitty uudella otsikolla.
- Kukin pystysuora nuoli on merkitty järjestystunnuksella, kuten *1a*. Tunnukset ilmaisevat varastotapahtumakirjausten järjestyksen aikajanalla.
- Päivämäärät erotetaan ohuilla mustilla pystyviivoilla. Päivämäärät näkyvät kaavion alareunassa.
- Varaston sulkemiset on kuvattu punaisilla pystysuorilla katkoviivoilla.
- Varaston sulkemisen suorittamat selvitykset on kuvattu punaisilla katkoviivanuolilla, jotka kulkevat vinosti vastaanotosta varastostaottoon.

## <a name="weighted-average-date-direct-settlement-when-the-include-physical-value-option-is-used"></a>Painotetun keskiarvon päivämäärän suora selvitys Sisällytä fyysinen arvo -asetuksella

Tuotteen nykyisessä versiossa **Sisällytä fyysinen arvo** -vaihtoehto toimii eri tavalla painotetun keskimääräisen päivämäärän varastomallin kanssa kuin aiemmissa versioissa. Kun **Sisällytä fyysinen arvo** -valintaruutu on valittuna nimikkeen **nimikemalliryhmän** sivulla, järjestelmä käyttää juoksevan arvioidun tai keskimääräisen ongelman kustannushinnan laskennassa fyysisesti päivitettyjä vastaanottotapahtumia. Varastostaotot kirjataan tämän arvioidun kustannushinnan perusteella kauden aikana. Varaston sulkemisen aikana vain taloudellisesti päivitetyt vastaanotot otetaan huomioon painotetun keskiarvon laskennassa.

Seuraavassa kaaviossa on kuvattu näitä tapahtumia:

**1. päivä:**

- 1a. Varaston fyysinen vastaanotto määrälle 10 yksikkökustannuksen ollessa 10,00 USD.
- 1b. Varaston taloudellinen vastaanotto määrälle 10 yksikkökustannuksen ollessa 10,00 USD.
- 2a. Varaston fyysinen vastaanotto määrälle 10 yksikkökustannuksen ollessa 20,00 USD.
- 3a. Varaston fyysinen varastostaotto määrälle 1 kustannushintaan 15,00 USD (fyysisesti ja taloudellisesti kirjattujen tapahtumien käyttökeskiarvo).
- 3b. Varaston taloudellinen varastostaotto määrälle 1 kustannushintaan 15,00 USD (fyysisesti ja taloudellisesti kirjattujen tapahtumien käyttökeskiarvo).

**2. päivä:**

- 4a. Varaston fyysinen vastaanotto määrälle 1 yksikkökustannuksen ollessa 25,00 USD.
- 5a. Varaston fyysinen vastaanotto määrälle 1 yksikkökustannuksen ollessa 30,00 USD.
- 5b. Varaston taloudellinen vastaanotto määrälle 1 yksikkökustannuksen ollessa 30,00 USD.
- 6a. Varaston fyysinen varastostaotto määrälle 1 kustannushintaan 21,25 USD / kappale (fyysisesti ja taloudellisesti kirjattujen tapahtumien käyttökeskiarvo).

**3. päivä:**

- 7\. Varaston sulkeminen on suoritettu. Päivämäärän painotetun keskiarvon menetelmään perustuen järjestelmä käyttää suoraselvitystapaa 30. joulukuuta (30.12.), koska vain yksi kuitti päivitetään taloudellisesti 30.12. Tässä esimerkissä luodaan yksi tilitys tapahtumien 1b ja 3b välille. Varasto-ottoon ei tehdä oikaisua 30.12. Lisäksi oikaisua tai selvitystä ei tehdä 31. joulukuuta (31.12.), koska 31.12. ei ole taloudellisesti päivitettyjä asioita.

Seuraava kaavio kuvaa tämän tapahtumasarjan ja painotetun keskimääräisen varastomallin ja suoran selvitysperiaatteen käytön vaikutukset **Sisällytä fyysinen arvo** -vaihtoehdon kanssa.

![Painotetun keskiarvon suora täsmäytys Sisällytä fyysinen arvo -valinnan kanssa.](media/weighted-average-date-direct-settlement-with-include-physical-value.png)

**Kaavion selite:**

- Pystysuorat nuolet kuvaavat varastotapahtumia.
- Fyysisiä tapahtumia kuvastavat lyhyemmät vaalean harmaat nuolet.
- Kirjanpitotapahtumia kuvastavat pidemmät mustat nuolet.
- Akselin yläpuolella olevat pystysuorat nuolet kuvaavat vastaanottoja varastoon.
- Akselin alapuolella olevat pystysuorat nuolet kuvaavat varastostaottoja.
- Kukin uusi vastaanotto- tai varastostaottotapahtuma on merkitty uudella otsikolla.
- Kukin pystysuora nuoli on merkitty järjestystunnuksella, kuten *1a*. Tunnukset ilmaisevat varastotapahtumakirjausten järjestyksen aikajanalla.
- Päivämäärät erotetaan ohuilla mustilla pystyviivoilla. Päivämäärät näkyvät kaavion alareunassa.
- Varaston sulkemiset on kuvattu punaisilla pystysuorilla katkoviivoilla.
- Varaston sulkemisen suorittamat selvitykset on kuvattu punaisilla katkoviivanuolilla, jotka kulkevat vinosti vastaanotosta varastostaottoon.

## <a name="weighted-average-date-summarized-settlement-when-the-include-physical-value-option-is-used"></a>Painotetun keskiarvon päivämäärän yhteenvetoselvitys Sisällytä fyysinen arvo -asetuksella

Tuotteen nykyisessä versiossa **Sisällytä fyysinen arvo** -vaihtoehto toimii eri tavalla painotetun keskiarvon kanssa kuin aiemmissa versioissa. Kun **Sisällytä fyysinen arvo** -valintaruutu on valittuna nimikkeen **nimikemalliryhmän** sivulla, järjestelmä käyttää juoksevan arvioidun tai keskimääräisen kustannushinnan laskennassa fyysisesti päivitettyjä vastaanottotapahtumia. Varastostaotot kirjataan tämän arvioidun kustannushinnan perusteella kauden aikana. Varaston sulkemisen aikana vain taloudellisesti päivitetyt vastaanotot otetaan huomioon painotetun keskiarvon laskennassa. On suositeltavaa, että varasto suljetaan painotetun keskiarvon varastomallia käytettäessä joka kuukausi. Tässä esimerkissä painotetun keskimääräisen päivämäärän yhteenvetoselvityksen varastomalli on merkitty sisältämään fyysisen arvon.

Seuraavassa kaaviossa on kuvattu näitä tapahtumia:

**1. päivä:**

- 1a. Varaston fyysinen vastaanotto määrälle 1 yksikkökustannuksen ollessa 10,00 USD.
- 1b. Varaston taloudellinen vastaanotto määrälle 1 yksikkökustannuksen ollessa 10,00 USD.
- 2a. Varaston fyysinen vastaanotto määrälle 1 yksikkökustannuksen ollessa 20,00 USD.
- 2b. Varaston taloudellinen vastaanotto määrälle 1 yksikkökustannuksen ollessa 22,00 USD.
- 3a. Varaston fyysinen varastostaotto määrälle 1 kustannushintaan 16,00 USD (fyysisesti ja taloudellisesti kirjattujen tapahtumien käyttökeskiarvo).
- 3b. Varaston taloudellinen varastostaotto määrälle 1 kustannushintaan 16,00 USD (fyysisesti ja taloudellisesti kirjattujen tapahtumien käyttökeskiarvo).

**2. päivä:**

- 4a. Varaston fyysinen vastaanotto määrälle 1 yksikkökustannuksen ollessa 25,00 USD.
- 5a. Varaston fyysinen vastaanotto määrälle 1 yksikkökustannuksen ollessa 30,00 USD.
- 5b. Varaston taloudellinen vastaanotto määrälle 1 yksikkökustannuksen ollessa 30,00 USD.
- 6a. Varaston fyysinen varastostaotto määrälle 1 kustannushintaan 23,67 USD (fyysisesti ja taloudellisesti kirjattujen tapahtumien käyttökeskiarvo).

**3. päivä:**

- 7\. Varaston sulkeminen on suoritettu.
- 7a. Painotetun keskiarvon varaston sulkemistapahtuman rahoituksellinen varasto-otto muodostetaan, jotta saadaan varaston kaikkien rahoituksellisten vastaanottojen täsmäytysten yhteenveto.

    - Tapahtuma 1b tilitetään määrälle 1 ja tilitetty summa on 10,00 USD.
    - Tapahtuma 2b tilitetään määrälle 1 ja tilitetty summa on 22,00 USD.
    - Tapahtuma 7a luodaan määrälle 2 ja tilitetty summa on 32,00 USD. Tämä tapahtuma vastakirjaa kahden kaudella taloudellisesti päivitetyn vastaanottotapahtuman summan.

- 7b. Painotetun keskiarvon varaston sulkemistapahtuman taloudellinen vastaanotto luodaan vastatapahtumaksi taloudellisesti kirjatuille varasto-otoille.

    - Tapahtuma 3b tilitetään määrälle 1 ja tilitetty summa on 16,00 USD. Tapahtumaa ei oikaista, koska se on taloudellisesti kirjattujen tapahtumien painotettu keskiarvo joulukuun 1. päivänä (1.12.).
    - Tapahtuma 7b luodaan määrälle 2, jonka rahamäärä on 32,00 USD ja maksettu summa USD 16,00, tapahtuman 3b kuittaamiseksi. Tämä tapahtuma vastakirjaa yhden kaudella taloudellisesti päivitetyn varasto-ottotapahtuman summan. Tapahtuma jää avoimeksi, koska sitä on vielä yksi.

Seuraava kaavio kuvaa tämän tapahtumasarjan ja painotetun keskimääräisen varastomallin ja yhteenlasketun selvitysperiaatteen käytön vaikutukset ilman **Sisällytä fyysinen arvo** -vaihtoehtoa.

![Painotetun keskiarvon yhteenvetotäsmäytys ja Sisällytä fyysinen arvo.](media/weighted-average-date-summarized-settlement-with-include-physical-value.png)

**Kaavion selite:**

- Pystysuorat nuolet kuvaavat varastotapahtumia.
- Fyysisiä tapahtumia kuvastavat lyhyemmät vaalean harmaat nuolet.
- Kirjanpitotapahtumia kuvastavat pidemmät mustat nuolet.
- Akselin yläpuolella olevat pystysuorat nuolet kuvaavat vastaanottoja varastoon.
- Akselin alapuolella olevat pystysuorat nuolet kuvaavat varastostaottoja.
- Kukin uusi vastaanotto- tai varastostaottotapahtuma on merkitty uudella otsikolla.
- Kukin pystysuora nuoli on merkitty järjestystunnuksella, kuten *1a*. Tunnukset ilmaisevat varastotapahtumakirjausten järjestyksen aikajanalla.
- Päivämäärät erotetaan ohuilla mustilla pystyviivoilla. Päivämäärät näkyvät kaavion alareunassa.
- Varaston sulkemiset on kuvattu punaisilla pystysuorilla katkoviivoilla.
- Varaston sulkemisen suorittamat selvitykset on kuvattu punaisilla katkoviivanuolilla, jotka kulkevat vinosti vastaanotosta varastostaottoon.

## <a name="weighted-average-date-when-marking-is-used"></a>Painotetun keskiarvon päivämäärä käyttäen merkintää

Merkintä on prosessi, jonka avulla voit linkittää (eli merkitä) varaston ottotapahtuman vastaanottotapahtumaan. Merkintä voi tapahtua joko ennen tapahtuman kirjaamista tai sen jälkeen. Merkinnän avulla voit varmistaa tarkan varastokustannuksen, kun tapahtuma kirjataan, kun varaston sulkeminen suoritetaan.

Oletetaan esimerkiksi, että yrityksesi asiakaspalveluosasto on hyväksynyt kiireellisen tilauksen tärkeältä asiakkaalta. Koska tilaus on kiireellinen, tästä nimikkeestä on maksettava tavallista enemmän, jotta asiakkaan pyynnön voisi toteuttaa. Sinun on varmistettava, että tämän varastonimikkeen kustannus otetaan huomioon myyntitilauslaskun katteessa (tai myydyn tavaran kustannuksissa).

Kun ostotilaus kirjataan, varasto vastaanotetaan hintaan 120,00 USD. Jos myyntitilausasiakirja on merkitty ostotilaukseen ennen pakkausluettelon tai laskun postittamista, COGS on 120,00 USD tuotteen nykyisen juoksevan keskihinnan sijaan. Jos merkintä tapahtuu myyntitilauspakkausluettelon tai -laskun kirjauksen jälkeen, COGS kirjataan juoksevan keskihinnan mukaan.

Ennen varaston sulkemista nämä kaksi tapahtumaa voidaan vielä merkitä toisiinsa.

Jos vastaanottotapahtuma merkitään varasto-ottotapahtumaan, nimikkeen nimikemalliryhmässä määritetty arvostustapa ohitetaan, ja järjestelmä täsmäyttää nämä tapahtumat toisiaan vasten.

Voit merkitä varastostaottotapahtuman vastaanottoon kirjauksen jälkeen. Voit tehdä tämän merkinnän myyntitilausrivin **Myyntitilauksen tiedot** -sivulla. Voit tarkastella avoimia vastaanottotapahtumia **Merkintä**-sivulla.

Voit merkitä varastostaottotapahtuman vastaanottoon myös tapahtuman kirjauksen jälkeen. Voit täsmäyttää tai merkitä varastostaottotapahtuman varastoidun nimikkeen avoimeen vastaanottotapahtumaan kirjatusta varaston oikaisukirjauskansiosta.

Seuraavassa kaaviossa on kuvattu näitä tapahtumia:

**1. päivä:**

- 1a. Varaston fyysinen vastaanotto määrälle 1 yksikkökustannuksen ollessa 10,00 USD.
- 1b. Varaston taloudellinen vastaanotto määrälle 1 yksikkökustannuksen ollessa 10,00 USD.
- 2a. Varaston fyysinen vastaanotto määrälle 1 yksikkökustannuksen ollessa 20,00 USD.
- 2b. Varaston taloudellinen vastaanotto määrälle 1 yksikkökustannuksen ollessa 22,00 USD.
- 3a. Varaston fyysinen varastostaotto määrälle 1 kustannushintaan 16,00 USD (taloudellisesti kirjattujen tapahtumien käyttökeskiarvo).
- 3b. Varaston taloudellinen varastostaotto määrälle 1 kustannushintaan 16,00 USD (taloudellisesti kirjattujen tapahtumien käyttökeskiarvo).
- 3c. Tapahtuman 3b varaston taloudellinen varasto-otto on merkitty taloudelliseen varasto-ottoon tapahtumaan 2b.

**2. päivä:**

- 4a. Varaston fyysinen vastaanotto määrälle 1 yksikkökustannuksen ollessa 25,00 USD.
- 5a. Varaston fyysinen vastaanotto määrälle 1 yksikkökustannuksen ollessa 30,00 USD.
- 5b. Varaston taloudellinen vastaanotto määrälle 1 yksikkökustannuksen ollessa 30,00 USD.
- 6a. Varaston fyysinen varastostaotto määrälle 1 kustannushintaan 23,00 USD (taloudellisesti kirjattujen tapahtumien käyttökeskiarvo).

**3. päivä:**

- 7\. Varaston sulkeminen on suoritettu. Painotetun keskiarvon menetelmää käyttävän merkintäperiaatteen mukaan merkityt tapahtumat täsmäytetään toisiaan vasten. Tässä esimerkissä tapahtuma 3b täsmäytetään tapahtuma 2b:tä vasten ja 6,00 USD kirjataan tapahtuma 3b:lle, jolloin arvo on 22,00 USD. Tässä esimerkissä ei tehdä muita tilitysitä, koska sulkeminen luo täsmäytyksen vain taloudellisesti päivitettyjä tapahtumia varten.

Seuraavassa kaaviossa näkyy tämä tapahtumasarja ja painotetun keskimääräisen varastomallin käytön vaikutukset merkinnällä.

![Painotettu keskiarvo ja merkintä.](media/weighted-average-date-with-marking.png)

**Kaavion selite:**

- Pystysuorat nuolet kuvaavat varastotapahtumia.
- Fyysisiä tapahtumia kuvastavat lyhyemmät vaalean harmaat nuolet.
- Kirjanpitotapahtumia kuvastavat pidemmät mustat nuolet.
- Akselin yläpuolella olevat pystysuorat nuolet kuvaavat vastaanottoja varastoon.
- Akselin alapuolella olevat pystysuorat nuolet kuvaavat varastostaottoja.
- Kukin uusi vastaanotto- tai varastostaottotapahtuma on merkitty uudella otsikolla.
- Kukin pystysuora nuoli on merkitty järjestystunnuksella, kuten *1a*. Tunnukset ilmaisevat varastotapahtumakirjausten järjestyksen aikajanalla.
- Päivämäärät erotetaan ohuilla mustilla pystyviivoilla. Päivämäärät näkyvät kaavion alareunassa.
- Varaston sulkemiset on kuvattu punaisilla pystysuorilla katkoviivoilla.
- Varaston sulkemisen suorittamat selvitykset on kuvattu punaisilla katkoviivanuolilla, jotka kulkevat vinosti vastaanotosta varastostaottoon.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
