---
title: Painotettu keskiarvo sekä fyysinen arvo ja merkintä
description: Painotettu keskiarvo on varastomalli, joka perustuu painotetun keskiarvon periaatteeseen. Siinä varasto-otot arvotetaan varastoon varaston sulkemiskauden aikana vastaanotettavien nimikkeiden sekä edeltävän kauden mahdollisen käytettävissä olevan varaston keskiarvon mukaan.
author: AndersGirke
ms.date: 02/21/2022
ms.topic: article
ms.search.form: InventJournalLossProfit, InventMarking, InventModelGroup, SalesTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: 65501
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6c124716b70be837573506a738ef2034397f2bda
ms.sourcegitcommit: addae271ddfc5a8b0721c23337f69916153db4cd
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/21/2022
ms.locfileid: "8330223"
---
# <a name="weighted-average-with-physical-value-and-marking"></a>Painotettu keskiarvo sekä fyysinen arvo ja merkintä

[!include [banner](../includes/banner.md)]

Painotettu keskiarvo on varastomalli sen keskiarvon perusteella, joka perustuu kunkin komponentin (nimiketapahtuman) kertolaskuun kertoimella (kustannushinta), joka vastaa sen tärkeyttä (määrää). Painotettu keskiarvoa voidaan kuvailla myös varastomalliksi, joka määrittää varasto-ottotapahtumien kustannukset kauden aikana vastaanotetun varaston ja edeltävän kauden kaikkien käytettävissä olevien varastojen keskiarvon perusteella.

Kun suoritat varaston sulkemisen painotetun keskiarvon varastomallin avulla, selvityksen voi luoda kahdella tavalla. Yleensä kaikki vastaanotot täsmäytetään suhteessa virtuaalivarastostaottoon, joka sisältää vastaanotetun kokonaismäärän ja -arvon. Tällä virtuaalivarastostaotolla on vastaava virtuaalivastaanotto, josta varastostaotot täsmäytetään. Näin kaikille varastostaotoille tulee sama keskimääräinen kustannus. Virtuaalivarastostaoton ja -vastaanoton voi nähdä virtuaalisiirtona, jota kutsutaan *painotetun keskiarvon varastonsulkemissiirroksi*. Tätä selvitysmenetelmää kutsutaan *painotetun keskiarvon yhteenvetotilitykseksi*. Jos vastaanottoja on vain yksi, kaikki varastostaotot voi täsmäyttää siitä, eikä virtuaalisiirtoa luoda. Tätä selvitysmenetelmää kutsutaan *suoraksi tilitykseksi*. Kaikki varaston sulkemisen jälkeen käytettävissä oleva varasto arvotetaan edellisen kauden painotetun keskiarvon mukaan ja sisällytetään seuraavan kauden painotetun keskiarvon laskentaan.

Voit ohittaa painotetun keskiarvon periaatteen merkitsemällä varastotapahtumat niin, että tietyn nimikkeen vastaanotto selvitetään tiettyä varastostaottoa vasten. Varaston kausittainen sulkeminen on pakollinen painotetun keskiarvon varastomallia käytettäessä luodaksesi täsmäytyksen ja oikaistaksesi varasto-ottojen arvon painotetun keskiarvon periaatteella. Varasto-ottotapahtumat arvotetaan fyysisten ja taloudellisten päivitysten suorituksen keskiarvon mukaan, kunnes varaston sulkemisprosessi suoritetaan. Jos et käytä merkintää, juokseva keskiarvo lasketaan, kun fyysinen tai taloudellinen päivitys suoritetaan.

Varaston painotetun keskiarvon kustannuslaskentamenetelmä lasketaan seuraavalla kaavalla:

- Painotettu keskiarvo = (\[Q1 × P1\] + \[Q2 × P2\] + \[Q *n* × P *n*\]) ÷ (Q1 + Q2 + Q *n*)

Q = tapahtuman määrä  
P = tapahtuman hinta

Selvitykset ovat varaston sulkemiskirjauksia, jotka säätävät varastostaotot sulkemispäivän oikean painotetun keskiarvon mukaisiksi. Seuraavissa esimerkeissä kuvataan painotetun keskiarvon käytön vaikutusta viidessä eri konfiguraatiossa:

- Painotetun keskiarvon suora täsmäytys ilman **Sisällytä fyysinen arvo** -vaihtoehtoa
- Painotetun keskiarvon yhteenvetotäsmäytys ilman **Sisällytä fyysinen arvo** -valintaa
- Painotetun keskiarvon suora täsmäytys ja **Sisällytä fyysinen arvo** -valinta
- Painotetun keskiarvon yhteenvetotäsmäytys ja **Sisällytä fyysinen arvo** -valinta
- Painotettu keskiarvo ja merkintä

## <a name="weighted-average-direct-settlement-without-include-physical-value"></a>Painotetun keskiarvon suora täsmäytys ilman Sisällytä fyysinen arvo -valintaa

Suoran täsmäytyksen periaate luo täsmäytykset suoraan vastaanottojen ja varasto-ottojen välille luomatta uusia varastotapahtumia. Järjestelmä käyttää tätä suoran selvityksen periaatetta seuraavissa tilanteissa:

- Kauden aikana on kirjattu yksi vastaanotto ja vähintään yksi varastostaotto.
- Kauden aikana on kirjattu vain varastostaottoja, ja varasto sisältää käytettävissä olevia nimikkeitä aiemmasta sulkemisesta.

Tässä esimerkissä vapautetun tuotteen **nimikemalliryhmän** **Sisällytä fyysinen arvo** -valintaruudun valinta on tyhjä. Seuraavassa on kuvattu näitä tapahtumia:

- 1a. Varaston fyysinen vastaanotto määrälle 10 yksikkökustannuksen ollessa 10,00 USD.
- 1b. Varaston taloudellinen vastaanotto määrälle 10 yksikkökustannuksen ollessa 10,00 USD.
- 2a. Varaston fyysinen vastaanotto määrälle 10 yksikkökustannuksen ollessa 20,00 USD.
- 3a. Varaston fyysinen varastostaotto määrälle 1 kustannushintaan 10,00 USD (taloudellisesti kirjattujen tapahtumien käyttökeskiarvo).
- 3b. Varaston taloudellinen varastostaotto määrälle 1 kustannushintaan 10,00 USD (taloudellisesti kirjattujen tapahtumien käyttökeskiarvo).
- 4a. Varaston fyysinen varastostaotto määrälle 1 kustannushintaan 10,00 USD / kappale (taloudellisesti kirjattujen tapahtumien käyttökeskiarvo).
- 4b. Varaston taloudellinen varastostaotto määrälle 1 kustannushintaan 10,00 USD / kappale (taloudellisesti kirjattujen tapahtumien käyttökeskiarvo).
- 5a. Varaston fyysinen varastostaotto määrälle 1 kustannushintaan 10,00 USD / kappale (taloudellisesti kirjattujen tapahtumien käyttökeskiarvo).
- 6\. Varaston sulkeminen on suoritettu. Painotetun keskiarvon menetelmään perustuen järjestelmä käyttää suoran täsmäytyksen menetelmää, koska kauden aikana päivitetään vain yksi vastaanotto taloudellisesti. Tässä esimerkissä luodaan yksi tilitys 1b- ja 3b-kohteiden välille ja toinen 1b- ja 4b-kohteiden välille. Oikaisua ei tehdä, koska käyttökeskiarvo on sama kuin painotettu keskiarvo.

Seuraava kaavio kuvaa painotetun keskiarvon varastomallin ja suoran täsmäytysperiaatteen vaikutusta tähän tapahtumien sarjaan, kun **Sisällytä fyysinen arvo** -vaihtoehtoa ei käytetä.

![Painotettu keskiarvo – suora maksu – fyysistä arvoa ei sisällytetä.](media/weighted-average-direct-settlement-without-include-physical-value.png)

**Kaavion selite**

- Pystysuorat nuolet kuvaavat varastotapahtumia.
- Fyysisiä tapahtumia kuvastavat lyhyemmät vaalean harmaat nuolet.
- Kirjanpitotapahtumia kuvastavat pidemmät mustat nuolet.
- Akselin yläpuolella olevat pystysuorat nuolet kuvaavat vastaanottoja varastoon.
- Akselin alapuolella olevat pystysuorat nuolet kuvaavat varastostaottoja.
- Kukin uusi vastaanotto- tai varastostaottotapahtuma on merkitty uudella otsikolla.
- Kukin pystysuora nuoli on merkitty järjestystunnuksella, kuten *1a*. Tunnukset ilmaisevat varastotapahtumakirjausten järjestyksen aikajanalla.
- Jokainen kaavion päivämäärä erotetaan ohuella mustalla pystysuoralla viivalla. Päivämäärä näkyy kaavion alareunassa.
- Varaston sulkemiset on kuvattu punaisella pystysuoralla katkoviivalla.
- Varaston sulkemisen suorittamat selvitykset on kuvattu punaisilla katkoviivanuolilla, jotka kulkevat vinosti vastaanotosta varastostaottoon.

## <a name="weighted-average-summarized-settlement-without-the-include-physical-value-option"></a>Painotetun keskiarvon yhteenvetotäsmäytys ilman Sisällytä fyysinen arvo -valintaa

Kun kaudella on useita vastaanottoja, painotettu käyttää yhteenvetotäsmäytysperiaatetta, jossa kaikki tietyllä sulkemisjaksolla tapahtuvat vastaanotot lasketaan yhteen *Painotetun keskiarvon varaston sulkeminen* -nimiseksi tapahtumaksi. Kaikki jakson vastaanotot täsmäytetään luodun uuden varastotapahtuman varastostaottoa vastaan. Kaikki jakson varastostaotot täsmäytetään uuden varastotapahtuman vastaanottoa vastaan. Jos on olemassa käytettävissä olevaa varastoa varaston sulkemisen jälkeen, käytettävissä olevan varaston arvo sisällytetään painotetun keskiarvon varaston sulkemistapahtumien vastaanottotapahtumaan.

Seuraavat tapahtumat on havainnollistettu seuraavassa kuvassa:

- 1a. Varaston fyysinen vastaanotto määrälle 1 yksikkökustannuksen ollessa 10,00 USD.
- 1b. Varaston taloudellinen vastaanotto määrälle 1 yksikkökustannuksen ollessa 10,00 USD.
- 2a. Varaston fyysinen vastaanotto määrälle 1 yksikkökustannuksen ollessa 20,00 USD.
- 2b. Varaston taloudellinen vastaanotto määrälle 1 yksikkökustannuksen ollessa 22,00 USD.
- 3a. Varaston fyysinen varastostaotto määrälle 1 kustannushintaan 16,00 USD (taloudellisesti kirjattujen tapahtumien käyttökeskiarvo).
- 3b. Varaston taloudellinen varastostaotto määrälle 1 kustannushintaan 16,00 USD (taloudellisesti kirjattujen tapahtumien käyttökeskiarvo).
- 4a. Varaston fyysinen vastaanotto määrälle 1 yksikkökustannuksen ollessa 25,00 USD.
- 5a. Varaston fyysinen vastaanotto määrälle 1 yksikkökustannuksen ollessa 30,00 USD.
- 5b. Varaston taloudellinen vastaanotto määrälle 1 yksikkökustannuksen ollessa 30,00 USD.
- 6a. Varaston fyysinen varastostaotto määrälle 1 kustannushintaan 23,00 USD (taloudellisesti kirjattujen tapahtumien käyttökeskiarvo).
- 7\. Varaston sulkeminen on suoritettu.
- 7a. Painotetun keskiarvon varaston sulkemistapahtuman rahoituksellinen varasto-otto muodostetaan, jotta saadaan varaston kaikkien rahoituksellisten vastaanottojen täsmäytysten yhteenveto.
  - Tapahtuma 1b tilitetään määrälle 1 ja tilitetty summa on 10,00 USD.
  - Tapahtuma 2b tilitetään määrälle 1 ja tilitetty summa on 22,00 USD.
  - Tapahtuma 5b tilitetään määrälle 1 ja tilitetty summa on 30,00 USD.
  - Tapahtuma 7a. luodaan määrälle 3 ja tilitettävä summa on 62,00 USD. Tämä tapahtuma vastakirjaa kolmen kaudella taloudellisesti päivitetyn vastaanottotapahtuman summan.
- 7b. Painotetun keskiarvon varaston sulkemistapahtuman taloudellinen vastaanotto luodaan vastatapahtumaksi taloudellisesti kirjatuille varasto-otoille.
  - Tapahtuma 3b tilitetään määrälle 1 ja tilitetty summa on 20,67 USD. Tätä tapahtumaa oikaistaan 4,67 USD, jolloin alkuperäinen arvo 16,00 USD tulee arvoon 20,67 USD, joka on kauden kirjanpitoon kirjattujen tapahtumien painotettu keskiarvo.
  - Tapahtuma 7b. luodaan määrälle 1 ja tilitettävä summa on 20,67 USD tapahtuman 3b vastakirjaukseksi. Tämä tapahtuma vastakirjaa yhden kaudella taloudellisesti päivitetyn varasto-ottotapahtuman summan.

Seuraava kaavio kuvaa painotetun keskiarvon varastomallin ja yhteenvetotäsmäytyksen vaikutusta tähän tapahtumien sarjaan, kun **Sisällytä fyysinen arvo** -vaihtoehtoa ei käytetä.

![Painotettu keskiarvo – maksun yhteenveto – fyysistä arvoa ei sisällytetä.](media/weighted-average-summarized-settlement-without-include-physical-value.png)

**Kaavion selite**

- Pystysuorat nuolet kuvaavat varastotapahtumia.
- Fyysisiä tapahtumia kuvastavat lyhyemmät vaalean harmaat nuolet.
- Kirjanpitotapahtumia kuvastavat pidemmät mustat nuolet.
- Akselin yläpuolella olevat pystysuorat nuolet kuvaavat vastaanottoja varastoon.
- Akselin alapuolella olevat pystysuorat nuolet kuvaavat varastostaottoja.
- Kukin uusi vastaanotto- tai varastostaottotapahtuma on merkitty uudella otsikolla.
- Kukin pystysuora nuoli on merkitty järjestystunnuksella, kuten *1a*. Tunnukset ilmaisevat varastotapahtumakirjausten järjestyksen aikajanalla.
- Jokainen kaavion päivämäärä erotetaan ohuella mustalla pystysuoralla viivalla. Päivämäärä näkyy kaavion alareunassa.
- Varaston sulkemiset on kuvattu punaisella pystysuoralla katkoviivalla.
- Varaston sulkemisen suorittamat selvitykset on kuvattu punaisilla katkoviivanuolilla, jotka kulkevat vinosti vastaanotosta varastostaottoon.

## <a name="weighted-average-direct-settlement-with-the-include-physical-value-option"></a>Painotetun keskiarvon suora täsmäytys ja Sisällytä fyysinen arvo -valinta

**Sisällytä fyysinen arvo** -parametri toimii painotetun keskiarvon varastomallin yhteydessä eri tavoin kuin tuotteen aiemmissa versioissa. Jos **Sisällytä fyysinen arvo** -asetuksen nimikkeelle **Nimikemalliryhmä**-lomakkeella, järjestelmä käyttää varasto-oton arvioidun kustannushinnan ja juoksevan keskiarvon laskennassa fyysisesti päivitettyjä vastaanottotapahtumia. Varastostaotot kirjataan tämän arvioidun kustannushinnan perusteella kauden aikana. Varaston sulkemisen aikana vain rahoituksellisesti päivitetyt vastaanotot otetaan huomioon painotetun keskiarvon laskennassa.

Seuraavat tapahtumat on havainnollistettu seuraavassa kuvassa:

- 1a. Varaston fyysinen vastaanotto määrälle 10 yksikkökustannuksen ollessa 10,00 USD.
- 1b. Varaston taloudellinen vastaanotto määrälle 10 yksikkökustannuksen ollessa 10,00 USD.
- 2a. Varaston fyysinen vastaanotto määrälle 10 yksikkökustannuksen ollessa 20,00 USD.
- 3a. Varaston fyysinen varastostaotto määrälle 1 kustannushintaan 15,00 USD (fyysisesti ja taloudellisesti kirjattujen tapahtumien käyttökeskiarvo).
- 3b. Varaston taloudellinen varastostaotto määrälle 1 kustannushintaan 15,00 USD (fyysisesti ja taloudellisesti kirjattujen tapahtumien käyttökeskiarvo).
- 4a. Varaston fyysinen varastostaotto määrälle 1 kustannushintaan 15,00 USD / kappale (fyysisesti ja taloudellisesti kirjattujen tapahtumien käyttökeskiarvo).
- 4b. Varaston taloudellinen varastostaotto määrälle 1 kustannushintaan 15,00 USD / kappale (fyysisesti ja taloudellisesti kirjattujen tapahtumien käyttökeskiarvo).
- 5a. Varaston fyysinen varastostaotto määrälle 1 kustannushintaan 15,00 USD / kappale (fyysisesti ja taloudellisesti kirjattujen tapahtumien käyttökeskiarvo).
- 6\. Varaston sulkeminen on suoritettu. Painotetun keskiarvon menetelmään perustuen järjestelmä käyttää suoran täsmäytyksen menetelmää, koska kauden aikana päivitetään vain yksi vastaanotto taloudellisesti. Tässä esimerkissä luodaan yksi tilitys 1b- ja 3b-kohteiden välille ja toinen 1b- ja 4b-kohteiden välille. Tapahtumat 3b ja 4b oikaistaan summalla -5,00 USD, jotta arvoksi saadaan 10,00 USD.

Seuraava kaavio kuvaa painotetun keskiarvon varastomallin ja suoran täsmäytysperiaatteen vaikutusta tähän tapahtumien sarjaan, kun **Sisällytä fyysinen arvo** -vaihtoehto on käytössä.

![Painotettu keskiarvo – suora maksu – fyysinen arvo sisällytetään.](media/weighted-average-direct-settlement-with-include-physical-value.png)

**Kaavion selite**

- Pystysuorat nuolet kuvaavat varastotapahtumia.
- Fyysisiä tapahtumia kuvastavat lyhyemmät vaalean harmaat nuolet.
- Kirjanpitotapahtumia kuvastavat pidemmät mustat nuolet.
- Akselin yläpuolella olevat pystysuorat nuolet kuvaavat vastaanottoja varastoon.
- Akselin alapuolella olevat pystysuorat nuolet kuvaavat varastostaottoja.
- Kukin uusi vastaanotto- tai varastostaottotapahtuma on merkitty uudella otsikolla.
- Kukin pystysuora nuoli on merkitty järjestystunnuksella, kuten *1a*. Tunnukset ilmaisevat varastotapahtumakirjausten järjestyksen aikajanalla.
- Jokainen kaavion päivämäärä erotetaan ohuella mustalla pystysuoralla viivalla. Päivämäärä näkyy kaavion alareunassa.
- Varaston sulkemiset on kuvattu punaisella pystysuoralla katkoviivalla.
- Varaston sulkemisen suorittamat selvitykset on kuvattu punaisilla katkoviivanuolilla, jotka kulkevat vinosti vastaanotosta varastostaottoon.

## <a name="weighted-average-summarized-settlement-with-the-include-physical-value-option"></a>Painotetun keskiarvon yhteenvetotäsmäytys ja Sisällytä fyysinen arvo -valinta

**Sisällytä fyysinen arvo** -parametri toimii painotetun keskiarvon yhteydessä eri tavoin kuin aiemmissa versioissa. Valitse **Sisällytä fyysinen arvo** -valintaruutu nimikkeelle **Nimikemalliryhmä**-sivulta. Järjestelmä käyttää tämän jälkeen fyysisesti päivitettyjä vastaanottoja arvioidun kustannushinnan tai käyttökeskiarvon laskemiseen. Varastostaotot kirjataan tämän arvioidun kustannushinnan perusteella kauden aikana. Varaston sulkemisen aikana vain rahoituksellisesti päivitetyt vastaanotot otetaan huomioon painotetun keskiarvon laskennassa. On suositeltavaa, että varasto suljetaan painotetun keskiarvon varastomallia käytettäessä joka kuukausi. Tässä painotetun keskiarvon yhteenvetotäsmäytyksen esimerkissä varastomalli on merkitty sisältämään fyysinen arvo.

Seuraavat tapahtumat on havainnollistettu seuraavassa kuvassa:

- 1a. Varaston fyysinen vastaanotto määrälle 1 yksikkökustannuksen ollessa 10,00 USD.
- 1b. Varaston taloudellinen vastaanotto määrälle 1 yksikkökustannuksen ollessa 10,00 USD.
- 2a. Varaston fyysinen vastaanotto määrälle 1 yksikkökustannuksen ollessa 20,00 USD.
- 2b. Varaston taloudellinen vastaanotto määrälle 1 yksikkökustannuksen ollessa 22,00 USD.
- 3a. Varaston fyysinen varastostaotto määrälle 1 kustannushintaan 16,00 USD (fyysisesti ja taloudellisesti kirjattujen tapahtumien käyttökeskiarvo).
- 3b. Varaston taloudellinen varastostaotto määrälle 1 kustannushintaan 16,00 USD (fyysisesti ja taloudellisesti kirjattujen tapahtumien käyttökeskiarvo).
- 4a. Varaston fyysinen vastaanotto määrälle 1 yksikkökustannuksen ollessa 25,00 USD.
- 5a. Varaston fyysinen vastaanotto määrälle 1 yksikkökustannuksen ollessa 30,00 USD.
- 5b. Varaston taloudellinen vastaanotto määrälle 1 yksikkökustannuksen ollessa 30,00 USD.
- 6a. Varaston fyysinen varastostaotto määrälle 1 kustannushintaan 23,67 USD (fyysisesti ja taloudellisesti kirjattujen tapahtumien käyttökeskiarvo).
- 7\. Varaston sulkeminen on suoritettu.
- 7a. Painotetun keskiarvon varaston sulkemistapahtuman rahoituksellinen varasto-otto muodostetaan, jotta saadaan varaston kaikkien rahoituksellisten vastaanottojen täsmäytysten yhteenveto.
  - Tapahtuma 1b tilitetään määrälle 1 ja tilitetty summa on 10,00 USD.
  - Tapahtuma 2b tilitetään määrälle 1 ja tilitetty summa on 22,00 USD.
  - Tapahtuma 5b tilitetään määrälle 1 ja tilitetty summa on 30,00 USD.
  - Tapahtuma 7a. luodaan määrälle 3 ja tilitettävä summa on 62,00 USD.  
- 7b. Painotetun keskiarvon varaston sulkemistapahtuman taloudellinen vastaanotto luodaan vastatapahtumaksi taloudellisesti suljetuille varasto-ottotapahtumille.
  - Tapahtuma 3b tilitetään määrälle 1 ja tilitetty summa on 20,67 USD. Tätä tapahtumaa oikaistaan 4,67 USD, jolloin alkuperäinen arvo 16,00 USD tulee arvoon 20,67 USD, joka on kauden kirjanpitoon kirjattujen tapahtumien painotettu keskiarvo.
  - Tapahtuma 7b. luodaan määrälle 1 ja tilitettävä summa on 20,67 USD tapahtuman 3b vastakirjaukseksi.

Seuraava kaavio kuvaa painotetun keskiarvon varastomallin ja yhteenvetotäsmäytyksen vaikutusta tähän tapahtumien sarjaan, kun **Sisällytä fyysinen arvo** -vaihtoehtoa ei käytetä.

![Painotettu keskiarvo – maksun yhteenveto – fyysinen arvo sisällytetään.](media/weighted-average-summarized-settlement-with-include-physical-value.png)

**Kaavion selite**

- Pystysuorat nuolet kuvaavat varastotapahtumia.
- Fyysisiä tapahtumia kuvastavat lyhyemmät vaalean harmaat nuolet.
- Kirjanpitotapahtumia kuvastavat pidemmät mustat nuolet.
- Akselin yläpuolella olevat pystysuorat nuolet kuvaavat vastaanottoja varastoon.
- Akselin alapuolella olevat pystysuorat nuolet kuvaavat varastostaottoja.
- Kukin uusi vastaanotto- tai varastostaottotapahtuma on merkitty uudella otsikolla.
- Kukin pystysuora nuoli on merkitty järjestystunnuksella, kuten *1a*. Tunnukset ilmaisevat varastotapahtumakirjausten järjestyksen aikajanalla.
- Jokainen kaavion päivämäärä erotetaan ohuella mustalla pystysuoralla viivalla. Päivämäärä näkyy kaavion alareunassa.
- Varaston sulkemiset on kuvattu punaisella pystysuoralla katkoviivalla.
- Varaston sulkemisen suorittamat selvitykset on kuvattu punaisilla katkoviivanuolilla, jotka kulkevat vinosti vastaanotosta varastostaottoon.

## <a name="weighted-average-with-marking"></a>Painotettu keskiarvo ja merkintä

Merkintä on prosessi, jonka avulla voit linkittää (eli merkitä) varaston ottotapahtuman vastaanottotapahtumaan. Merkintä voi tapahtua joko ennen tapahtuman kirjaamista tai sen jälkeen. Merkinnän avulla voit varmistaa tarkan varastokustannuksen, kun tapahtuma kirjataan tai kun varaston sulkeminen suoritetaan.

Oletetaan esimerkiksi, että yrityksesi asiakaspalveluosasto on hyväksynyt kiireellisen tilauksen tärkeältä asiakkaalta. Koska tilaus on kiireellinen, tästä nimikkeestä on maksettava tavallista enemmän, jotta asiakkaan pyynnön voisi toteuttaa. Sinun on varmistettava, että tämän varastonimikkeen kustannus otetaan huomioon myyntitilauslaskun katteessa (tai myydyn tuotteen kustannuksissa).

Kun ostotilaus kirjataan, varasto vastaanotetaan hintaan 120,00 USD. Esimerkiksi tämä myyntitilausasiakirja on merkitty ostotilaukseen ennen pakkausluettelon tai laskun kirjausta. Tämän jälkeen myytyjen tuotteiden kustannukset ovat 120,00 USD nimikkeen nykyisen keskimääräinen käyttökustannuksen sijaan. Jos myyntitilauksen pakkausluettelo tai lasku kirjataan ennen merkintää, myydyn tavaran kustannus kirjataan käyttäen käyttökeskiarvon mukaista kustannushintaa.

Ennen varaston sulkemista nämä kaksi tapahtumaa voidaan vielä merkitä toisiinsa.

Varastostaottotapahtuma merkitään varastostaottotapahtumaan. Tämän jälkeen nimikkeen nimikemalliryhmälle valittu arvostusmenetelmä ohitetaan, ja järjestelmä täsmäyttää nämä tapahtumat keskenään.

Voit merkitä varastostaottotapahtuman vastaanottoon kirjauksen jälkeen. Voit tehdä tämän myyntitilausrivin **Myyntitilauksen tiedot** -sivulla. Voit tarkastella avoimia vastaanottotapahtumia **Merkintä**-sivulla.

Voit merkitä varastostaottotapahtuman vastaanottoon tapahtuman kirjauksen jälkeen. Voit täsmäyttää tai merkitä varastostaottotapahtuman varastoidun nimikkeen avoimeen vastaanottotapahtumaan kirjatusta varaston oikaisukirjauskansiosta.

Seuraavat tapahtumat on havainnollistettu seuraavassa kuvassa:

- 1a. Varaston fyysinen vastaanotto määrälle 1 yksikkökustannuksen ollessa 10,00 USD.
- 1b. Varaston taloudellinen vastaanotto määrälle 1 yksikkökustannuksen ollessa 10,00 USD.
- 2a. Varaston fyysinen vastaanotto määrälle 1 yksikkökustannuksen ollessa 20,00 USD.
- 2b. Varaston taloudellinen vastaanotto määrälle 1 yksikkökustannuksen ollessa 22,00 USD.
- 3a. Varaston fyysinen varastostaotto määrälle 1 kustannushintaan 16,00 USD (taloudellisesti kirjattujen tapahtumien käyttökeskiarvo).
- 3b. Varaston taloudellinen varastostaotto määrälle 1 kustannushintaan 16,00 USD (taloudellisesti kirjattujen tapahtumien käyttökeskiarvo).
- 3c. Kohteen 3b varaston taloudellinen varasto-otto on merkitty taloudelliseen varasto-ottoon 2b.
- 4a. Varaston fyysinen vastaanotto määrälle 1 yksikkökustannuksen ollessa 25,00 USD.
- 5a. Varaston fyysinen vastaanotto määrälle 1 yksikkökustannuksen ollessa 30,00 USD.
- 5b. Varaston taloudellinen vastaanotto määrälle 1 yksikkökustannuksen ollessa 30,00 USD.
- 6a. Varaston fyysinen varastostaotto määrälle 1 kustannushintaan 23,00 USD (taloudellisesti kirjattujen tapahtumien käyttökeskiarvo).
- 7\. Varaston sulkeminen on suoritettu. Painotetun keskiarvon menetelmää käyttävän merkintäperiaatteen mukaan merkityt tapahtumat täsmäytetään toisiaan vasten. Tässä esimerkissä 3b täsmäytetään 2b:tä vasten ja 6,00 USD kirjataan 3b:lle, jolloin arvo on 22,00 USD. Tässä esimerkissä ei tehdä muita tilitysitä, koska sulkeminen luo täsmäytyksen vain taloudellisesti päivitettyjä tapahtumia varten.

Seuraavassa kaaviossa havainnollistetaan painotetun keskiarvon varastomallin ja merkinnän käyttämisen vaikutus tähän tapahtumien sarjaan.

![Painotettu keskiarvo merkinnän kanssa.](media/weighted-average-with-marking.png)

**Kaavion selite**

- Pystysuorat nuolet kuvaavat varastotapahtumia.
- Fyysisiä tapahtumia kuvastavat lyhyemmät vaalean harmaat nuolet.
- Kirjanpitotapahtumia kuvastavat pidemmät mustat nuolet.
- Akselin yläpuolella olevat pystysuorat nuolet kuvaavat vastaanottoja varastoon.
- Akselin alapuolella olevat pystysuorat nuolet kuvaavat varastostaottoja.
- Kukin uusi vastaanotto- tai varastostaottotapahtuma on merkitty uudella otsikolla.
- Kukin pystysuora nuoli on merkitty järjestystunnuksella, kuten *1a*. Tunnukset ilmaisevat varastotapahtumakirjausten järjestyksen aikajanalla.
- Jokainen kaavion päivämäärä erotetaan ohuella mustalla pystysuoralla viivalla. Päivämäärä näkyy kaavion alareunassa.
- Varaston sulkemiset on kuvattu punaisella pystysuoralla katkoviivalla.
- Varaston sulkemisen suorittamat selvitykset on kuvattu punaisilla katkoviivanuolilla, jotka kulkevat vinosti vastaanotosta varastostaottoon.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
