---
title: Varaston arvon raporttien esimerkit ja logiikka
description: Tässä artikkelissa on esimerkkejä tuloksista, jotka koskevat kutakin varaston arvon raporttityyppiä. Varaston arvon raporteissa on tietoja varastotilanteen ja kirjanpitovaraston määristä ja summista.
author: JennySong-SH
ms.date: 10/19/2021
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2021-10-19
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: e6c6387be5204fde6ebc7a4983567801900974af
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8877650"
---
# <a name="inventory-value-report-examples-and-logic"></a>Varaston arvon raporttien esimerkit ja logiikka

[!include [banner](../includes/banner.md)]

Varaston arvon raporteissa on tietoja varastotilanteen ja kirjanpitovaraston määristä ja summista. Tässä artikkelissa on esimerkkejä tuloksista, jotka koskevat kutakin varaston arvon raporttityyppiä.

Lisätietoja kunkin varaston arvon raporttityypin luomisesta ja käyttämisestä on kohdassa [Varaston arvon raportit](inventory-value-report-storage.md).

## <a name="sample-data-that-is-used-in-these-examples"></a>Esimerkeissä käytettävät mallitiedot

Artikkelin esimerkit perustuvat tässä osassa käsiteltäviin varastotapahtuman mallitietoihin.

### <a name="storage-dimension-setup"></a>Varastodimensioryhmän määritys

Esimerkkijärjestelmässä on seuraavat varastodimensiot.

| Nimi | Aktiiviset | Fyysinen varasto | Kirjanpitovarasto |
|---|---|---|---|
| Sivusto | Kyllä | Kyllä | Kyllä |
| Varasto | Kyllä | Kyllä | Ei |

### <a name="inventory-model"></a>Varastomalli

Esimerkkijärjestelmän vapautettujen tuotteiden varastomalli on *FIFO* ja varastomallin **Kustannushinta**-kentän asetuksena on *Sisällytä fyysinen arvo*.

### <a name="inventory-transactions"></a>Varastotapahtumat

Esimerkkijärjestelmä sisältää seuraavat vapautetun tuotteen varastotapahtumat, kun tuotteen nimikenumero on *B0001*.

| Viite | Toimipaikka | Varasto | Vastaanotto | Ongelma | Fyysinen pvm. | Rahoituspvm. | Määrä | Kustannussumma | Fyysinen kustannus |
|---|---|---|---|---|---|---|---|---|---|
| Ostotilaus | 1 | 11 | Ostettu | | Maaliskuun 15. | Maaliskuun 15. | 10 | 1 000 | 1 000 |
| Ostotilaus | 2 | 21 | Ostettu | | Maaliskuun 15. | Maaliskuun 15. | 10 | 2,000 | 2,000 |
| Ostotilaus | 1 | 11 | Vastaanotettu | | Huhtikuun 15. | | 5 | | 375 |
| Siirtotilaus | 1 | 11 | | Myyty | Toukokuun 2. | Toukokuun 2. | -5 | -458,33 | -458,33 |
| Siirtotilaus | 1 | 12 | Ostettu | | Toukokuun 2. | Toukokuun 2. | 5 | 458.33 | 458.33 |
| Myyntitilaus | 1 | 12 | | Laskutettu | Toukokuun 3. | Toukokuun 3. | -1 | -91,67 | -91,67 |

### <a name="inventory-value-report-configuration"></a>Varaston arvon raporttimääritys

Esimerkkijärjestelmän varaston arvon raporttimäärityksessä on seuraavat asetukset:

- **Alue:** *Kirjauspäivä*
- **Varasto:** *Kyllä*
- **Laske keskimääräinen yksikkökustannus:** *Kyllä*
- **Kokonaismäärä ja -arvo:** *Kyllä*
- **Toimipaikka, näkymä:** *Valittu*
- **Resurssitunnus, näkymä:** *Kyllä*
- **Taso:** *Summat*

## <a name="inventory-value-report-example-1"></a>Varaston arvon raporttiesimerkki 1

Seuraavassa taulukossa ja kuvissa on tuloksia, jotka saadaan käytettäessä aiemmin tässä artikkelissa käsiteltyjä näytetietoja ja raporttimääritystä.

| Resurssityyppi | Resurssi | Sivusto | Viite | Varasto: rahoitusmäärä | Varasto: rahoitussumma | Varasto: kirjattu fyysinen määrä | Varasto: kirjattu fyysinen summa | Varasto: Määrä | Varasto: summa | Keskimääräinen yksikkökustannus |
|---|---|---|---|---|---|---|---|---|---|---|
| Materiaali | B0001 | 1 | Loppusaldo | 9.00 | 908.33 | 5.00 | 375.00 | 14,00 | 1,283.33 | 91.67 |
| Materiaali | B0001 | 2 | Loppusaldo | 10.00 | 2,000.00 | 0,00 | 0,00 | 10.00 | 2,000.00 | 200.00 |

### <a name="standard-inventory-value-report-for-example-1"></a>Esimerkin 1 varaston arvon vakioraportti

Seuraavassa kuvassa on esimerkin 1 **Varaston arvo** -vakioraportti. (Voit avata suuremman version kuvasta valitsemalla sen.)

[![Esimerkin 1 varaston arvon raportti](media/inventory-value-report-ex1-small.png "Esimerkin 1 varaston arvon raportti")](media/inventory-value-report-ex1.png)

### <a name="inventory-value-report-storage-report-for-example-1"></a>Esimerkin 1 varaston arvon raportin tallennustilaraportti

Seuraavassa kuvassa on esimerkin 1 **Varaston arvon raportin tallennustila** -raportti. (Voit avata suuremman version kuvasta valitsemalla sen.)

[![Esimerkin 1 varaston arvon raportin tallennustilaraportti](media/inventory-value-report-storage-ex1-small.png "Esimerkin 1 varaston arvon raportin tallennustilaraportti")](media/inventory-value-report-storage-ex1.png)

## <a name="inventory-value-report-example-2"></a>Varaston arvon raporttiesimerkki 2

Seuraavassa taulukossa ja kuvissa on tuloksia, jotka saadaan käytettäessä aiemmin tässä artikkelissa käsiteltyä raporttimääritystä. **Taso**-kentän arvoksi voidaan myös vaihtaa *Tapahtumat* raporttimäärityksissä ja **Päivämäärästä**-kentän asetukseksi määritetään *15. maaliskuuta*, kun raportti suoritetaan.

| Resurssityyppi | Resurssi | Toimipaikka | Päivämäärä | Numero | Viite | Varasto: rahoitusmäärä | Varasto: rahoitussumma | Varasto: kirjattu fyysinen määrä | Varasto: kirjattu fyysinen summa | Varasto: Määrä | Varasto: summa |
|---|---|---|---|---|---|---|---|---|---|---|---|
| Materiaali | B0001 | 1 | 15.3.2021 | 00000126 | Ostotilaus | 0,00 | 0,00 | 10.00 | 1,000.00 | **10.00** | **1,000.00** |
| Materiaali | B0001 | 1 | 15.3.2021 | 00000126 | Ostotilaus | 10.00 | 1,000.00 | -10,00 | -1 000,00 | **0.00** | **0.00** |
| Materiaali | B0001 | 1 | 15.4.2021 | 00000128 | Ostotilaus | 0,00 | 0,00 | 5.00 | 375.00 | **5.00** | **375.00** |
| Materiaali | B0001 | 1 | 2.5.2021 | 000003 | Siirtotilauksen lähetys | -5,00 | -458,33 | 0,00 | 0,00 | **-5,00** | **-458,33** |
| Materiaali | B0001 | 1 | 2.5.2021 | 000003 | Siirtotilauksen vastaanotto | 5.00 | 458.33 | 0,00 | 0,00 | **5.00** | **458.33** |
| Materiaali | B0001 | 1 | 3.5.2021 | 000835 | Myyntitilaus | 0,00 | 0,00 | -1,00 | -91,67 | **-1,00** | **-91,67** |
| Materiaali | B0001 | 1 | 3.5.2021 | 000835 | Myyntitilaus | -1,00 | -91,67 | 1.00 | 91.67 | **0.00** | **0.00** |
| Materiaali | B0001 | 2 | 15.3.2021 | 00000127 | Ostotilaus | 0,00 | 0,00 | 10.00 | 2,000.00 | **10.00** | **2,000.00** |
| Materiaali | B0001 | 2 | 15.3.2021 | 00000127 | Ostotilaus | 10.00 | 2,000.00 | -10,00 | -2 000,00 | **0.00** | **0.00** |
| Materiaali | B0001 | 2 | 2.5.2021 | 000003 | Siirtotilauksen lähetys | 5.00 | 458.33 | 0,00 | 0,00 | **5.00** | **458.33** |
| Materiaali | B0001 | 2 | 2.5.2021 | 000003 | Siirtotilauksen vastaanotto | -5,00 | -458,33 | 0,00 | 0,00 | **-5,00** | **-458,33** |

### <a name="standard-inventory-value-report-for-example-2"></a>Esimerkin 2 varaston arvon vakioraportti

Seuraavassa kuvassa on esimerkin 2 **Varaston arvo** -vakioraportti. (Voit avata suuremman version kuvasta valitsemalla sen.)

[![Esimerkin 2 varaston arvon raportti](media/inventory-value-report-ex2-small.png "Esimerkin 2 varaston arvon raportti")](media/inventory-value-report-ex2.png)

### <a name="inventory-value-report-storage-report-for-example-2"></a>Esimerkin 2 varaston arvon raportin tallennustilaraportti

Seuraavassa kuvassa on esimerkin 2 **Varaston arvon raportin tallennustila** -raportti. (Voit avata suuremman version kuvasta valitsemalla sen.)

[![Esimerkin 2 varaston arvon raportin tallennustilaraportti](media/inventory-value-report-storage-ex2-small.png "Esimerkin 2 varaston arvon raportin tallennustilaraportti")](media/inventory-value-report-storage-ex2.png)

## <a name="inventory-value-report-example-3"></a>Varaston arvon raporttiesimerkki 3

Varaston arvon raportit kannattaa suorittaa uudelleenlaskennan tai varaston sulkemisen jälkeen, sillä näin saadaan tapahtumat ja summat, joihin uudelleenlaskenta tai varaston sulkeminen vaikuttaa.

Seuraavissa aliosissa näkyy ne varaston arvon raportit 30. toukokuuhun saakka, jotka luotiin varaston sulkemisen jälkeen.

### <a name="example-3-when-the-totals-level-is-used"></a>Esimerkki 3 käytettäessä Summat-tasoa

Seuraavassa taulukossa on tuloksia, jotka saadaan käytettäessä aiemmin tässä artikkelissa käsiteltyjä näytetietoja ja raporttimääritystä. (Kyseisessä raporttimäärityksissä **Taso**-kentän asetuksena on *Summat*.)

| Resurssityyppi | Resurssi | Toimipaikka | Viite | Varasto: rahoitusmäärä | Varasto: rahoitussumma | Varasto: kirjattu fyysinen määrä | Varasto: kirjattu fyysinen summa | Varasto: Määrä | Varasto: summa | Keskimääräinen yksikkökustannus |
|---|---|---|---|---|---|---|---|---|---|---|
| Materiaali | B0001 | 1 | Loppusaldo | 9.00 | 900.00 | 5.00 | 375.00 | 14,00 | 1,275.00 | 91.07 |
| Materiaali | B0001 | 2 | Loppusaldo | 10.00 | 2,000.00 | 0,00 | 0,00 | 10.00 | 2,000.00 | 200.00 |

### <a name="example-3-when-the-transactions-level-is-used"></a>Esimerkki 3 käytettäessä Tapahtumat-tasoa

Seuraavassa taulukossa on tulokset, kun käytetään aiemmin tässä artikkelissa käsiteltyjä esimerkkitietoja mutta **Taso**-kentän arvoksi vaihdetaan raporttimäärityksissä *Tapahtumat*.

| Resurssityyppi | Resurssi | Toimipaikka | Päivämäärä | Numero | Viite | Varasto: rahoitusmäärä | Varasto: rahoitussumma | Varasto: kirjattu fyysinen määrä | Varasto: kirjattu fyysinen summa | Varasto: Määrä | Varasto: summa |
|---|---|---|---|---|---|---|---|---|---|---|---|
| Materiaali | B0001 | 1 | 15.3.2021 | 00000126 | Ostotilaus | 0,00 | 0,00 | 10.00 | 1,000.00 | 10.00 | 1,000.00 |
| Materiaali | B0001 | 1 | 15.3.2021 | 00000126 | Ostotilaus | 10.00 | 1,000.00 | -10,00 | -1 000,00 | 0,00 | 0,00 |
| Materiaali | B0001 | 1 | 15.4.2021 | 00000128 | Ostotilaus | 0,00 | 0,00 | 5.00 | 375.00 | 5.00 | 375.00 |
| Materiaali | B0001 | 1 | 2.5.2021 | 000003 | Siirtotilauksen lähetys | -5,00 | -458,33 | 0,00 | 0,00 | -5,00 | -458,33 |
| Materiaali | B0001 | 1 | 2.5.2021 | 000003 | Siirtotilauksen vastaanotto | 5.00 | 458.33 | 0,00 | 0,00 | 5.00 | 458.33 |
| Materiaali | B0001 | 1 | 3.5.2021 | 000835 | Myyntitilaus | 0,00 | 0,00 | -1,00 | -91,67 | -1,00 | -91,67 |
| Materiaali | B0001 | 1 | 3.5.2021 | 000835 | Myyntitilaus | -1,00 | -91,67 | 1.00 | 91.67 | 0,00 | 0,00 |
| Materiaali | B0001 | 1 | 31.5.2021 | 000835 | Myyntitilaus | 0,00 | -8,33 | 0,00 | 0,00 | 0,00 | -8,33 |
| Materiaali | B0001 | 1 | 31.5.2021 | 000003 | Siirtotilauksen lähetys | 0,00 | -41,67 | 0,00 | 0,00 | 0,00 | -41,67 |
| Materiaali | B0001 | 1 | 31.5.2021 | 000003 | Siirtotilauksen vastaanotto | 0,00 | 41.67 | 0,00 | 0,00 | 0,00 | 41.67 |
| Materiaali | B0001 | 2 | 15.3.2021 | 00000127 | Ostotilaus | 0,00 | 0,00 | 10.00 | 2,000.00 | 10.00 | 2,000.00 |
| Materiaali | B0001 | 2 | 15.3.2021 | 00000127 | Ostotilaus | 10.00 | 2,000.00 | -10,00 | -2 000,00 | 0,00 | 0,00 |
| Materiaali | B0001 | 2 | 2.5.2021 | 000003 | Siirtotilauksen lähetys | 5.00 | 458.33 | 0,00 | 0,00 | 5.00 | 458.33 |
| Materiaali | B0001 | 2 | 2.5.2021 | 000003 | Siirtotilauksen vastaanotto | -5,00 | -458,33 | 0,00 | 0,00 | -5,00 | -458,33 |
| Materiaali | B0001 | 2 | 31.5.2021 | 000003 | Siirtotilauksen lähetys | 0,00 | 41.67 | 0,00 | 0,00 | 0,00 | 41.67 |
| Materiaali | B0001 | 2 | 31.5.2021 | 000003 | Siirtotilauksen vastaanotto | 0,00 | -41,67 | 0,00 | 0,00 | 0,00 | -41,67 |
