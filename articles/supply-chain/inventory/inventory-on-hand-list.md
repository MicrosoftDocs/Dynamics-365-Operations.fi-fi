---
title: Käytettävissä olevan varaston luettelo
description: Tässä aiheessa kuvataan Käytettävissä oleva varasto sivun käytettävissä olevan varaston tietojen tarkastaminen. Aiheessa on tietoja tavoista, joilla erilaiset suodatus- ja lajitteluasetukset toimivat yhdessä, sekä yhdistelmien mahdollisista odottamattomista tuloksista.
author: sherry-zheng
manager: tfehr
ms.date: 07/07/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventOnhandItem, InventOnHandItemListPage, WHSOnHand
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2020-07-07
ms.dyn365.ops.version: Release 10.0.12
ms.openlocfilehash: 94e54220a68889fd31ac3b269f7a7f6f8dd98c8e
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/15/2021
ms.locfileid: "5005199"
---
# <a name="inventory-on-hand-list"></a>Käytettävissä olevan varaston luettelo

[!include [banner](../includes/banner.md)]

Tässä aiheessa kuvataan **Käytettävissä oleva varasto** -sivun käytettävissä olevan varaston tietojen tarkastaminen. Aiheessa on tietoja tavoista, joilla erilaiset suodatus- ja lajitteluasetukset toimivat yhdessä, sekä yhdistelmien mahdollisista odottamattomista tuloksista.

## <a name="query-your-on-hand-inventory"></a>Kyselyn tekeminen käytettävissä olevasta varastosta

Jos haluat tarkistaa varaston käytettävyyden, siirry kohtaan **Varastonhallinta \> Kyselyt ja raportit \> Käytettävissä olevien luettelo**.

**Käytettävissä olevien luettelo** -sivu päivittyy automaattisesti, kun tapahtumia tehdään varastossa. Nämä tapahtumat voivat olla ennustettuja, fyysisiä tai kirjanpitotapahtumia.

Seuraavien työkalujen avulla voit etsiä haluamaasi tuotejoukkoa:

- Valitse toimintoruudussa [**Dimensiot**](#dimensions), jos haluat avata valintaikkunan, jossa voit lisätä tai poistaa **Käytettävissä oleva** -ruudukon sarakkeita.
- Anna [**Suodattimet**-ruudussa](#filters-pane) tiettyjen kenttien arvot, jotta näkyviin tulevat vain näitä arvoja vastaavat tietueet. Huomaa, että tässä määrittämäsi suodattimet koskevat lähdetaulukoita, jotka voidaan koota myöhemmin uudelleen näytettäväksi valittujen dimensioiden mukaan. Lisätietoja siitä, miten tämä toiminta voi vaikuttaa tuloksiin, on myöhemmin tämän ohjeaiheen [esimerkeissä](#examples).
- Valitse **Suodattimet**-ruudussa **Käytä**, jos haluat luoda luettelon käytettävissä olevasta varastosta **Käytettävissä oleva** -ruudukossa.
- Valitse **Käytettävissä oleva** -ruudukossa mikä tahansa sarakeotsikko, jota käytetään lajittelussa tai suodatuksessa arvojen mukaan. Ruudukon yläosassa oleva pikasuodatin sisältää lisäsuodatusmahdollisuuksia. Nämä suodattimet koskevat tuloksia, eivät lähdetaulukoita. Lisätietoja siitä, miten tämä toiminta voi vaikuttaa tuloksiin, on myöhemmin tämän ohjeaiheen [esimerkeissä](#examples).

**Käytettävissä oleva** -ruudukko sisältää jokaisen vastaavan nimikkeen varaston tietojen seuraavat sarakkeet.

| Pylväskaavio | kuvaus |
|---|---|
| Fyysinen varasto | Varastosta käytettävissä oleva fyysinen määrä. |
| Fyysiset varatut | Fyysisesti varattu kokonaismäärä. |
| Saatavissa oleva fyysinen | Käytettävissä oleva (ei varattu) määrä, joka on käytettävissä fyysisessä varastossa.<p>**Käytettävissä oleva fyysinen** on laskettu kenttä. Arvo on sama kuin **fyysisen varaston** arvo vähennettynä **fyysisellä varatulla** arvolla.</p> |
| Käytettävissä oleva fyysinen lisädimensioilla | Kaikkien ruudukossa näkyvien dimensioiden käytettävissä oleva fyysinen määrä. |
| Tilattu yhteensä | Kokonaismäärä, joka sisältyy saapuviin tilauksiin tai jolla on positiivinen määrä eri varastokirjauskansioissa. |
| Tilauksessa | Kokonaismäärä, joka sisältyy lähteviin tilauksiin tai jolla on negatiivinen määrä eri varastokirjauskansioissa. |
| Tilatut varatut | Tilattuihin vastaanottoihin varattu kokonaismäärä. Tämän kentän arvo vastaa niiden lähtevien tapahtumien nimikkeiden kokonaismäärää, joiden tila on _Tilattu varattu_. Tilattuina varatut nimikkeet eivät ole fyysisesti käytettävissä varastossa. Siksi niitä ei voi suoraan kerätä ja toimittaa. |
| Varattavissa | Käytettävissä olevan varaston kokonaismäärä, joka voidaan varata.<p>**Huomautus:** Jos **Varaa tilatut nimikkeet** -valintaruutu on valittu **Varastonhallinnan parametrit** -sivulla, tämän kentän arvo sisältää odotetut vastaanotot. Jos valintaruutua ei ole valittu, arvo ei sisällä odotettuja vastaanottoja.</p> |
| Yhteensä käytettävissä | Käytettävissä oleva kokonaismäärä.<p>**Käytettävissä oleva kokonaismäärä** on laskettu kenttä. Arvo on sama kuin **Käytettävissä oleva fyysinen** -arvo sekä **Tilattu kokonaisarvo** vähennettynä **Tilauksessa**-arvolla.</p> |

## <a name="apply-filters-to-find-the-records-that-youre-looking-for"></a><a name="filters-pane"></a>Suodattimien kohdistaminen ja haluttujen tietueiden etsiminen

**Suodattimet**-ruudun avulla voit suodattaa käytettävissä olevan varaston luettelon siten, että se sisältää vain ne tietueet, joiden kenttien arvot vastaavat suodatusehtoja. Voit määrittää suodattimen alla olevien vaiheiden avulla.

1. Etsi **Suodattimet**-ruudussa kenttä, jonka mukaan haluat tehdä suodatuksen.
2. Valitse kohdekentän nimen alla olevassa kentässä looginen operaattori (esimerkiksi *alkaa*, *yhtä suuri kuin* tai *suurempi kuin*).
3. Anna tai valitse etsittävä arvo.

> [!IMPORTANT]
> **Käytettävissä olevien luettelo** -sivu kootaan yksityiskohtaisesta käytettävissä olevan varaston taulukosta, joka sisältää kaikki käytettävissä olevat dimensiot. Tämän sivun luettelo on kuitenkin yhteenveto. Näin ollen se saattaa yhdistää rivit lähdetaulukosta koostamalla arvot näytettävän dimension mukaan.
>
> **Suodattimet**-ruudussa määritettyjä suodattimia käytetään lähdetaulukossa, ei kootussa luettelossa. Tämä toiminta voi joskus aiheuttaa odottamattomia tuloksia. Lisätietoja siitä, miten tämä toiminta voi vaikuttaa tuloksiin, on myöhemmin tämän ohjeaiheen [esimerkeissä](#examples).
> 
> Kuitenkin [ruudukossa olevat suodattimet](#grid-filters) *kohdistetaan* koottuun luetteloon. Nämä suodattimet sisältävät sekä pikasuodattimen ruudukon yläosassa että kunkin sarakeotsikon suodattimen.

Voit muokata **Suodattimet**-ruudun suodatinjoukkoa alla olevien vaiheiden avulla.

- Jos haluat poistaa suodattimen ruudukosta, valitse sen **Sulje**-painike (**X**).
- Jos haluat lisätä suodattimen, valitse **Lisää** **Suodattimet**-ruudun yläosassa. Näkyviin tulevassa **Lisää suodatinkenttiä** -valintaikkunassa on käytettävissä olevien kenttien luettelo. Siinä näkyvät myös kunkin kentän tietotyypin ja taulukon tiedot. Sarakeotsikoiden avulla voit suodattaa ja lajitella luettelon haluamallasi tavalla. Sitten voit valita kunkin sellaisen kentän valintaikkunan, jonka haluat lisätä **Suodatin**-ruutuun. Kun olet valmis, valitse **Lisää** ja ota muutokset käyttöön.

## <a name="select-which-dimensions-to-show"></a><a name="dimensions"></a>Näytettävien dimensioiden valitseminen

Dimensioiden avulla saat lisätietoja kustakin käytettävissä olevan varaston luettelon nimikkeestä ja voit lajitella ja suodattaa luettelon. Näytettäväksi valitut dimensiot vaikuttavat myös siihen, miten rivit koostetaan **Käytettävissä olevien luettelo** -sivulla. Tämä kooste vuorostaan voi vaikuttaa siihen, miten lähdetaulukkojen rivit yhdistetään näytettävissä tuloksissa. Lisätietoja siitä, miten tämä toiminta voi vaikuttaa tuloksiin, on myöhemmin tämän ohjeaiheen [esimerkeissä](#examples).

Jos haluat mukauttaa näkyvissä olevien varastodimensioiden valintaa, noudata näitä ohjeita.

1. Valitse toimintoruudussa **Dimensiot**.

    Näkyviin tulevassa **Dimension näyttö** -valintaikkunassa ovat kaikki dimensiot.

2. Valitse jokaisen ruudukkoon sisällytettävän dimension valintaruutu.
3. Jos haluat, että valintaa käytetään oletusarvoisesti seuraavalla kerralla, kun **Käytettävissä olevien luettelo** -sivu avataan, määritä **Tallenna asetukset** -asetuksen arvoksi **Kyllä**. Jos määrität asetukseksi **Ei**, valintaa käytetään vain nykyisen istunnon aikana. Tämän vuoksi seuraavalla sivun avauskerralla käytetään nykyistä oletusvalintaa.
4. Ota muutokset käyttöön ja sulje valintaikkuna valitsemalla **OK**.

## <a name="filter-on-the-output-of-the-inventory-on-hand-list"></a><a name="grid-filters"></a>Varaston käytettävissä olevien luettelon tuloksen suodattaminen

Valitse **Käytettävissä oleva** -ruudukossa mikä tahansa sarakeotsikko, jota käytetään lajittelussa tai suodatuksessa arvojen mukaan. Ruudukon yläosassa oleva pikasuodatin sisältää lisäsuodatusmahdollisuuksia. Nämä suodattimet koskevat tuloksia, eivät lähdetaulukoita. Lisätietoja siitä, miten tämä toiminta voi vaikuttaa tuloksiin, on myöhemmin tämän ohjeaiheen [esimerkeissä](#examples).

> [!NOTE]
> Kaikkia sarakkeita ei voi suodattaa ja lajitella. Suurin osa määräsarakkeista ei sisällä lajittelu- ja suodatusohjausobjekteja, koska ne ovat laskettuja kenttiä. **Tilauksessa**-sarake on poikkeus.

## <a name="examples"></a><a name="examples"></a>Esimerkkejä

Järjestelmä sisältää yksityiskohtaisen (ei kootun) varastotaulukon, joka sisältää seuraavan käytettävissä olevan varaston.

| Nimiketunnus | Sivusto | Varasto | Fyysinen varasto | Saatavissa oleva fyysinen |
|---|---|---|---|---|
| IA0001 | 1 | 1 | 1 | 1 |
| IA0001 | 1 | 2 | 2 | 2 |
| IA0001 | 1 | 3 | 1 | 1 |

### <a name="scenario-1"></a>Skenaario 1

**Käytettävissä olevien luettelo** -sivu on määritetty näyttämään seuraavat lopulliset dimensiot:

- Nimiketunnus
- Sivusto
- Varasto

**Suodattimet**-ruudussa määritetään seuraavat suodatusehdot:

- **Nimiketunnus** \| **on täsmälleen** \| _IA0001_
- **Käytettävissä oleva fyysinen** \| **pienempi tai yhtä suuri kuin** \| _1_

Tässä on tuloksena saatu tuotos.

| Nimiketunnus | Sivusto | Varasto | Fyysinen varasto | Saatavissa oleva fyysinen |
|---|---|---|---|---|
| IA0001 | 1 | 1 | 1 | 1 |
| IA0001 | 1 | 3 | 1 | 1 |

### <a name="scenario-2"></a>Skenaario 2

**Käytettävissä olevien luettelo** -sivu on määritetty näyttämään seuraavat lopulliset dimensiot:

- Nimiketunnus
- Sivusto

**Suodattimet**-ruudussa määritetään seuraavat suodatusehdot:

- **Nimiketunnus** \| **on täsmälleen** \| _IA0001_
- **Käytettävissä oleva fyysinen** \| **pienempi tai yhtä suuri kuin** \| _1_

Tässä on tuloksena saatu tuotos.

| Nimiketunnus | Sivusto | Fyysinen varasto | Saatavissa oleva fyysinen |
|---|---|---|---|
| IA0001 | 1 | 2 | 2 |

Huomaa, että **Suodattimet**-ruudun asetukset koskevat eriteltyä (ei koostettua) varastotaulukkoa, joka näkyy tämän osan alussa. Tämän vuoksi ehto **Käytettävissä oleva fyysinen** \| **pienempi tai yhtä suuri kuin** \| _1_ etsii kaksi riviä taulukosta (ensimmäinen ja kolmas rivi, jossa kussakin näkyy **Käytettävissä oleva fyysinen** -arvo _1_). Tässä skenaariossa **Käytettävissä olevien luettelo** -sivua ei kuitenkaan ole määritetty näyttämään **Varasto**-dimensiota. Näin ollen se koostaa kaksi alkuperäistä riviä yhdeksi tulosriviksi, koska molemmilla riveillä on samanlaiset arvot kaikissa näkyvissä olevissa dimensioissa. Tämä rivi rikkoo suodatusehtoa, koska **Käytettävissä oleva fyysinen** -arvona on _2_. Tulos on kuitenkin oikein, koska **Suodattimet**-ruudun asetukset kohdistetaan lähdetaulukkoon, ei **Käytettävissä olevien luettelo** -sivun koostetaulukkoon.
