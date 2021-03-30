---
title: Varaston erääntymisraporttien esimerkkejä ja logiikka
description: Tässä ohjeaiheessa on esimerkkejä, jotka auttavat tulkitsemaan varaston erääntymisraportin tuloksia.
author: RichardLuan
manager: tfehr
ms.date: 5/29/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventAgingStorage, InventAgingStorageChart, InventAgingStorageDetails
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: riluan
ms.search.validFrom: 2020-5-29
ms.dyn365.ops.version: ''
ms.openlocfilehash: 1d9c70a7931c009cd53fbd28a3f4c768d04964a4
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5214415"
---
# <a name="inventory-aging-report-examples-and-logic"></a>Varaston erääntymisraporttien esimerkkejä ja logiikka

[!include [banner](../includes/banner.md)]

Tässä ohjeaiheessa on esimerkkejä, jotka auttavat tulkitsemaan **Varaston erääntyminen** -raportin tuloksia. Tämä raportti luokittelee valitun nimikkeen tai nimikeryhmän varastosaldon ja varastoarvot useisiin aikaväleihin. Ohjeaiheessa myös näytetään raportin sisäinen logiikka.

Ohjeaiheen esimerkeissä näytetään tulokset, jotka esitetään **Varaston erääntyminen** -vakioraportissa. Yleensä kannattaa kuitenkin käyttää tämän raportin [Varaston erääntymisraportin tallennus](inventory-aging-report-storage.md) -versiota, etenkin jos käsiteltäviä nimikkeitä ja varastoja on paljon. Varaston erääntymisraportin tallennus tallentaa jokaisen luodun raportin, näyttää tulokset vuorovaikutteisena sivuna ja kaaviona sekä sallii minkä tahansa tallennetun raportin viennin.

## <a name="sample-data-that-is-used-in-these-examples"></a>Esimerkeissä käytettävät mallitiedot

Ohjeaiheen esimerkit perustuvat tässä osassa käsiteltäviin varastotapahtuman mallitietoihin.

### <a name="storage-dimension-setup"></a>Varastodimensioryhmän määritys

Esimerkkijärjestelmässä on seuraavat varastodimensiot.

| Nimi      | Aktiiviset | Fyysinen varasto | Kirjanpitovarasto |
|-----------|--------|--------------------|---------------------|
| Sivusto      | Kyllä    | Kyllä                | Kyllä                 |
| Varasto | Kyllä    | Kyllä                | Nro                  |

### <a name="inventory-model"></a>Varastomalli

Esimerkkijärjestelmän vapautettujen tuotteiden varastomallin on *FIFO* ja varastomallin **Kustannushinta**-asetus on *Sisällytä fyysinen arvo*.

### <a name="inventory-transactions"></a>Varastotapahtumat

Esimerkkijärjestelmä sisältää seuraavat vapautetun tuotteen varastotapahtumat, kun tuotteen nimikenumero on *1000*.

| Viite      | Sivusto | Varasto | Kuitti   | Otto | Fyysinen pvm. | Rahoituspvm. | Määrä | Kustannussumma | Fyysinen kustannus |
|----------------|------|-----------|-----------|-------|---------------|----------------|----------|-------------|----------------------|
| Ostotilaus | 1    | 11        | Ostettu |       | Maaliskuun 15.      | Maaliskuun 15.       | 10       | 1 000       | 1 000                |
| Ostotilaus | 2    | 21        | Ostettu |       | Maaliskuun 15.      | Maaliskuun 15.       | 10       | 2,000       | 2,000                |
| Ostotilaus | 1    | 11        | Vastaanotettu  |       | Huhtikuun 15.      |                | 5        |             | 375                  |
| Siirtotilaus | 1    | 11        |           | Myyty  | Toukokuun 2.         | Toukokuun 2.          | -5       | -458,33     | -458,33              |
| Siirtotilaus | 1    | 12        | Ostettu |       | Toukokuun 2.         | Toukokuun 2.          | 5        | 458.33      | 458.33               |
| Myyntitilaus    | 1    | 12        |           | Myyty  | Toukokuun 3.         | Toukokuun 3.          | -1       | -91,67      | -91,67               |

## <a name="how-quantities-and-amounts-in-each-period-bucket-are-calculated"></a>Kunkin aikavälin määrien ja summien laskeminen

Edellisissä osissa kuvattuja mallitietoja käyttämällä voit suorittaa **Varaston erääntyminen** -raportin, jossa on seuraavat asetukset:

- **Alkupäivämäärä:** *9.5.2020*
- **Paikka:** *Näkymä*
- **Varasto**: *Ei*
- **Nimiketunnus:** *Yhteensä*
- **Erääntymiskausi:** Tämän kentän käyttäminen luo kuukausittaiset aikavälit.

Tässä tapauksessa luotu luodun raportin sisältö muistuttaa seuraavaa esimerkkiä.

<table>
<thead>
<tr>
    <th rowspan="2">Nimiketunnus</th>
    <th rowspan="2">Sivusto</th>
    <th rowspan="2">Varastosaldo</th>
    <th rowspan="2">Käytettävissä olevan varaston arvo</th>
    <th rowspan="2">Varaston arvon määrä</th>
    <th rowspan="2">Varaston arvo</th>
    <th rowspan="2">Keskimääräinen yksikkökustannus</th>
    <th colspan="2">8.5.2020–1.5.2020</th>
    <th colspan="2">30.4.2020–1.4.2020</th>
    <th colspan="2">31.3.2020–1.3.2020</th>
</tr>
<tr>
    <th>P1:Määrä</th>
    <th>P1:Summa</th>
    <th>P2:Määrä</th>
    <th>P2:Summa</th>
    <th>P3:Määrä</th>
    <th>P3:Summa</th>
</tr>
</thead>
<tbody>
<tr>
    <td>1000</td>
    <td>1</td>
    <td>14</td>
    <td>1,283.33</td>
    <td>14</td>
    <td>1,283.33</td>
    <td>91.67</td>
    <td></td>
    <td></td>
    <td>5.00</td>
    <td>458.33</td>
    <td>9.00</td>
    <td>825.00</td>
</tr>
<tr>
    <td>1000</td>
    <td>2</td>
    <td>10</td>
    <td>2,000.00</td>
    <td>10</td>
    <td>2,000.00</td>
    <td>200.00</td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td>10.00</td>
    <td>2,000.00</td>
</tr>
</tbody>
<tfoot>
<tr>
    <td><strong>1 000 Summat</strong></td>
    <td></td>
    <td><strong>24.00</strong></td>
    <td><strong>3,283.33</strong></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td><strong>5.00</strong></td>
    <td><strong>458.33</strong></td>
    <td><strong>19</strong></td>
    <td><strong>2,825.00</strong></td>
</tr>
</tfoot>
</table>

Huomaa seuraavat tiedot tässä esimerkkiraportissa:

- Raportissa näkyvät **Varaston arvon määrä**-, **Varastoarvo**- ja **Keskimääräinen yksikkökustannus** -arvot ovat taloushallinnan varastodimension arvoja (tässä tapauksessa **Toimipaikka**).

    Raportti näyttää esimerkiksi toimipaikan 1 osalta seuraavat tiedot:

    - **Varaston arvon määrä** -arvo on *14* (= 10 + 5 – 5 + 5 – 1).
    - **Varastoarvo** -arvo on *1 283,33* (= 1,000 + 375 – 458,33 + 458,33 – 91,67).
    - **Keskimääräinen yksikkökustannus** -arvo on *91,67*.
    - Kunkin aikavälin **Varastosaldo**- ja **Summa**-arvo lasketaan käyttämällä **Keskimääräinen yksikkökustannus** -arvoa.

- Raportti määrittää kunkin aikavälin varastosaldon summaamalla kunkin aikavälin vastaanotetun varastomäärän. Se käyttää sitten FIFO-periaatetta vähentämään varasto-ottojen kokonaismäärän riippumatta siitä, mitä varastomallia nimikkeet käyttävät.

Jos suoritat saman raportin uudelleen, mutta **Toimipaikka**- ja **Varasto**-kenttien asetukseksi määritetään *Näkymä*, uusi raportti muistuttaa seuraavaa esimerkkiä.

<table>
<thead>
<tr>
    <th rowspan="2">Nimiketunnus</th>
    <th rowspan="2">Sivusto</th>
    <th rowspan="2">Varasto</th>
    <th rowspan="2">Varastosaldo</th>
    <th rowspan="2">Käytettävissä olevan varaston arvo</th>
    <th rowspan="2">Varaston arvon määrä</th>
    <th rowspan="2">Varaston arvo</th>
    <th rowspan="2">Keskimääräinen yksikkökustannus</th>
    <th colspan="2">8.5.2020–1.5.2020</th>
    <th colspan="2">30.4.2020–1.4.2020</th>
    <th colspan="2">31.3.2020–1.3.2020</th>
</tr>
<tr>
    <th>P1:Määrä</th>
    <th>P1:Summa</th>
    <th>P2:Määrä</th>
    <th>P2:Summa</th>
    <th>P3:Määrä</th>
    <th>P3:Summa</th>
</tr>
</thead>
<tbody>
<tr>
    <td>1000</td>
    <td>1</td>
    <td>11</td>
    <td>10</td>
    <td>916.67</td>
    <td>14</td>
    <td>1,283.33</td>
    <td>91.67</td>
    <td></td>
    <td></td>
    <td>5.00</td>
    <td>458.33</td>
    <td>5.00</td>
    <td>458.33</td>
</tr>
<tr>
    <td>1000</td>
    <td>1</td>
    <td>12</td>
    <td>4</td>
    <td>366.67</td>
    <td>14</td>
    <td>1,283.33</td>
    <td>91.67</td>
    <td>4.00</td>
    <td>366.67</td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
</tr>
<tr>
    <td>1000</td>
    <td>2</td>
    <td></td>
    <td>10</td>
    <td>2,000.00</td>
    <td>10</td>
    <td>2,000.00</td>
    <td>200.00</td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td>10.00</td>
    <td>2,000.00</td>
</tr>
</tbody>
<tfoot>
<tr>
    <td><strong>1 000 Summat</strong></td>
    <td></td>
    <td></td>
    <td><strong>24.00</strong></td>
    <td><strong>3,283.33</strong></td>
    <td></td>
    <td></td>
    <td></td>
    <td><strong>4.00</strong></td>
    <td><strong>366.67</strong></td>
    <td><strong>5.00</strong></td>
    <td><strong>458.33</strong></td>
    <td><strong>15</strong></td>
    <td><strong>2,458.33</strong></td>
</tr>
</tfoot>
</table>

Tällä kertaa toimipaikka 1 jaetaan kahteen riviin, joista toinen on varasto 11 ja toinen varasto 12. **Varaston arvon määrä**-, **Varastoarvo**- ja **Keskimääräinen yksikkökustannus** -arvot ovat kuitenkin samat, koska **Varasto** ei ole taloushallinnan varastodimensio.

Huomaa myös, että toimipaikan 1 määräjakauma on erilainen. Ensimmäisessä suoritetussa raportissa järjestelmä ohitti samassa toimipaikassa tapahtuneen siirtotilauksen ja vähensi myyntilaskun määrän toimipaikan 1 aikavälistä **31.3.2020–1.3.2020**. Uudessa raportissa järjestelmä kuitenkin vähentää myyntilaskun määrän aikaväliltä **8.5.2020–1.5.2020** varastossa 12.

## <a name="effects-of-inventory-closing"></a>Varaston sulkemisen vaikutukset

Jos suoritetaan varaston toukokuun sulkeminen ja sen jälkeen edellinen raportti suoritetaan uudelleen siten, että **Alkupäivämäärä**-kentän arvona on *31.5.2020*, tulokset ovat seuraavat:

- **Varastoarvo**- ja **Keskimääräinen yksikkökustannus**-arvot on päivitetty.
- **Varastosaldo**-arvo ja kunkin aikavälin kaikki **Summa**-arvot päivitetään vastaavasti.

Uusi raportti muistuttaa seuraavaa esimerkkiä:

<table>
<thead>
<tr>
    <th rowspan="2">Nimiketunnus</th>
    <th rowspan="2">Sivusto</th>
    <th rowspan="2">Varasto</th>
    <th rowspan="2">Varastosaldo</th>
    <th rowspan="2">Käytettävissä olevan varaston arvo</th>
    <th rowspan="2">Varaston arvon määrä</th>
    <th rowspan="2">Varaston arvo</th>
    <th rowspan="2">Keskimääräinen yksikkökustannus</th>
    <th colspan="2">31.5.2020–1.5.2020</th>
    <th colspan="2">30.4.2020–1.4.2020</th>
    <th colspan="2">31.3.2020–1.3.2020</th>
</tr>
<tr>
    <th>P1:Määrä</th>
    <th>P1:Summa</th>
    <th>P2:Määrä</th>
    <th>P2:Summa</th>
    <th>P3:Määrä</th>
    <th>P3:Summa</th>
</tr>
</thead>
<tbody>
<tr>
    <td>1000</td>
    <td>1</td>
    <td>11</td>
    <td>10</td>
    <td>910.70</td>
    <td>14</td>
    <td>1,275.00</td>
    <td>91.07</td>
    <td>0,00</td>
    <td></td>
    <td>5.00</td>
    <td>455.36</td>
    <td>5.00</td>
    <td>455.36</td>
</tr>
<tr>
    <td>1000</td>
    <td>1</td>
    <td>12</td>
    <td>4</td>
    <td>364.29</td>
    <td>14</td>
    <td>1,275.00</td>
    <td>91.07</td>
    <td>4.00</td>
    <td>364.29</td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
</tr>
<tr>
    <td>1000</td>
    <td>2</td>
    <td></td>
    <td>10</td>
    <td>2,000.00</td>
    <td>10</td>
    <td>2,000.00</td>
    <td>200.00</td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td>10.00</td>
    <td>2,000.00</td>
</tr>
</tbody>
<tfoot>
<tr>
    <td><strong>1 000 Summat</strong></td>
    <td></td>
    <td></td>
    <td><strong>24.00</strong></td>
    <td><strong>3,275.00</strong></td>
    <td></td>
    <td></td>
    <td></td>
    <td><strong>4.00</strong></td>
    <td><strong>364.29</strong></td>
    <td><strong>5.00</strong></td>
    <td><strong>455.36</strong></td>
    <td><strong>15</strong></td>
    <td><strong>2,455.36</strong></td>
</tr>
</tfoot>
</table>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]