---
title: Varaston näkyvyyden määritykset
description: Tässä aiheessa käsitellään varaston näkyvyyden määrittämistä.
author: yufeihuang
ms.date: 08/02/2021
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2021-08-02
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: 92e42b22d424ab80303d771f760cfcf0599b9f4c
ms.sourcegitcommit: b9c2798aa994e1526d1c50726f807e6335885e1a
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/13/2021
ms.locfileid: "7345030"
---
# <a name="inventory-visibility-configuration"></a>Varaston näkyvyyden määritykset

[!include [banner](../includes/banner.md)]
[!INCLUDE [cc-data-platform-banner](../../includes/cc-data-platform-banner.md)]

Tässä aiheessa käsitellään varaston näkyvyyden määrittämistä.

## <a name="introduction"></a><a name="introduction"></a>Johdanto

Ennen varaston näkyvyyssovelluksen käytön aloittamista on tehtävä seuraavat määritykset tässä aiheessa kuvatulla tavalla:

- [Tietolähteen määritykset](#data-source-configuration)
- [Osion määritykset](#partition-configuration)
- [Tuotehierarkiaindeksin määritykset](#index-configuration)
- [Varausmääritykset (valinnainen)](#reservation-configuration)
- [Oletusmääritysnäyte](#default-configuration-sample)

> [!NOTE]
> Varaston näkyvyysmäärityksiä voi tarkastella ja muokata [Microsoft Power Appsissa](./inventory-visibility-power-platform.md#configuration). Kun määritykset on tehty, valitse sovelluksessa **Päivitä määritys**.

## <a name="data-source-configuration"></a><a name="data-source-configuration"></a>Tietolähteen määritykset

Tietolähde ilmaisee järjestelmän, josta tiedot tulevat. Niitä ovat esimerkiksi `fno` (eli Dynamics 365 Finance and Operations -sovellukset) ja `pos` (eli myyntipiste).

Tietolähdemääritykset sisältävät seuraavat osat:

- Dimensio (dimension yhdistämismääritys)
- Fyysinen mitta
- Laskennallinen mitta

> [!NOTE]
> `fno`-tietolähde on varattu Dynamics 365 Supply Chain Managementin käyttöön.

### <a name="dimension-dimension-mapping"></a><a name="data-source-configuration-dimension"></a>Dimensio (dimension yhdistämismääritys)

Dimensiomääritysten tarkoitus on standardoida monien järjestelmien integrointi dimensioyhdistelmiin perustuvien tapahtumien kirjaamista ja niihin perustuvia kyselyjä varten.

Varaston näkyvyyssovellus tukee seuraavia yleisiä perusdimensioita:

| Dimensiotyyppi | Perusdimensio |
|---|---|
| Tuote | `ColorId` |
| Tuote | `SizeId` |
| Tuote | `StyleId` |
| Tuote | `ConfigId` |
| Seuranta | `BatchId` |
| Seuranta | `SerialId` |
| Toimipaikka | `LocationId` |
| Toimipaikka | `SiteId` |
| Varaston tila | `StatusId` |
| Varastokohtainen | `WMSLocationId` |
| Varastokohtainen | `WMSPalletId` |
| Varastokohtainen | `LicensePlateId` |
| Muut | `VersionId` |
| Varasto (mukautettu) | `InventDimension1`–`InventDimension12` |
| Alanumero | `ExtendedDimension1`–`ExtendedDimension8` |

> [!NOTE]
> Edellisessä taulukossa mainitut dimensiotyypit on tarkoitettu vain tiedoksi. Niitä ei tarvitse määrittää varaston näkyvyyssovelluksessa.
>
> Varaston (mukautetut) dimensiot on ehkä varattu Supply Chain Management -käyttöä varten. Siinä tapauksessa niiden tilalla voidaan käyttää laajennettuja dimensioita.

Ulkoiset järjestelmät voivat käyttää varaston näkyvyyssovellusta sovelluksen RESTful API -ohjelmointirajapintojen kautta. Integrointia varten varaston näkyvyyssovellus sallii _ulkoisen tietolähteen_ määrittämisen ja yhdistämismääritykset _ulkoisista dimensioista_ _perusdimensioihin_. Esimerkki dimension yhdistämismääritystaulukosta.

| Ulkoinen dimensio | Perusdimensio |
|---|---|
| `MyColorId` | `ColorId` |
| `MySizeId` | `SizeId` |
| `MyStyleId` | `StyleId` |
| `MyDimension1` | `ExtendedDimension1` |
| `MyDimension2` | `ExtendedDimension2` |

Dimension yhdistämismäärityksen avulla ulkoiset dimensiot voidaan lähettää suoraan varaston näkyvyyssovellukseen. Varaston näkyvyyssovellus muuntaa sitten ulkoiset dimensiot automaattisesti perusdimensioiksi.

### <a name="physical-measures"></a>Fyysiset mitat

Fyysiset mitat muokkaavat määrän vastaamaan varaston tilaa. Fyysiset mitat voidaan määrittää omien tarpeiden mukaan.

Varaston näkyvyyssovelluksessa on luettelo fyysisistä oletusmitoista, ja tämä luettelo on linkitetty Supply Chain Managementiin (`fno`-tietolähteeseen). Seuraavassa taulukossa on esimerkki fyysisistä mitoista:

| Fyysisen mitan nimi | kuvaus |
|---|---|
| `NotSpecified` | Ei määritetty |
| `Arrived` | Saapunut |
| `AvailOrdered` | Saatavissa oleva tilattu |
| `AvailPhysical` | Saatavissa oleva fyysinen |
| `Deducted` | Toimitettu |
| `OnOrder` | Tilauksessa |
| `Ordered` | Tilattu |
| `PhysicalInvent` | Varastotilanne |
| `Picked` | Keräilty |
| `PostedQty` | Kirjattu määrä |
| `QuotationIssue` | Tarjouksen varasto-otto |
| `QuotationReceipt` | Tarjouksen kuitti |
| `Received` | Vastaanotettu |
| `Registered` | Rekisteröitynyt |
| `ReservOrdered` | Tilatut varatut |
| `ReservPhysical` | Fyysiset varatut |

### <a name="calculated-measures"></a><a name="data-source-configuration-calculated-measure"></a>Laskennalliset mitat

Laskennalliset mitat ovat mukautettu laskentakaava, joka koostuu fyysisten mittojen yhdistelmästä. Tämä toiminto antaa mahdollisuuden määrittää lisättävät ja/tai vähennettävät fyysiset mitat, joiden avulla voidaan muodostaa mukautettu mitta.

Kyse voi olla esimerkiksi seuraavasta kyselyn tuloksesta.

```json
[
    {
        "productId": "T-shirt",
        "dimensions": {
            "SiteId": "1",
            "LocationId": "11",
            "ColorId": "Red"
        },
        "quantities": {
            "pos": {
                "inbound": 80.0,
                "outbound": 20.0
            },
            "fno": {
                "availphysical": 100.0,
                "orderedintotal": 50.0,
                "orderedreserved": 10.0
            },
            "externalchannel": {
                "received": 90.0,
                "scheduled": 30.0,
                "issued": 60.0,
                "reserved": 40.0
            }
        }
    }
]
```

Seuraavaksi määritetään laskennallinen mitta `MyCustomAvailableforReservation`, kuten seuraavassa taulukossa. Kulutusjärjestelmä käyttää tämän laskennallisen mitan.

| Kulutusjärjestelmä | Laskennallinen mitta | Tietolähde | Fyysinen mitta | Laskentalaji |
|---|---|---|---|---|
| `CustomChannel` | `MyCustomAvailableforReservation` | `fno` | `availphysical` | `Addition` |
| `CustomChannel` | `MyCustomAvailableforReservation` | `fno` | `orderedintotal` | `Addition` |
| `CustomChannel` | `MyCustomAvailableforReservation` | `fno` | `orderedreserved` | `Subtraction` |
| `CustomChannel` | `MyCustomAvailableforReservation` | `pos` | `inbound` | `Addition` |
| `CustomChannel` | `MyCustomAvailableforReservation` | `pos` | `outbound` | `Subtraction` |
| `CustomChannel` | `MyCustomAvailableforReservation` | `externalchannel` | `received` | `Addition` |
| `CustomChannel` | `MyCustomAvailableforReservation` | `externalchannel` | `scheduled` | `Addition` |
| `CustomChannel` | `MyCustomAvailableforReservation` | `externalchannel` | `issued` | `Subtraction` |
| `CustomChannel` | `MyCustomAvailableforReservation` | `externalchannel` | `reserved` | `Subtraction` |

Tätä laskentakaavaa käytettäessä uudessa kyselyn tuloksessa on mukautettu mitta.

```json
[
    {
        "productId": "T-shirt",
        "dimensions": {
            "SiteId": "1",
            "LocationId": "11",
            "ColorId": "Red"
        },
        "quantities": {
            "pos": {
                "inbound": 80.0,
                "outbound": 20.0
            },
            "fno": {
                "availphysical": 100.0,
                "orderedintotal": 50.0,
                "orderedreserved": 10.0
            },
            "externalchannel": {
                "received": 90.0,
                "scheduled": 30.0,
                "issued": 60.0,
                "reserved": 40.0
            },
            "CustomChannel": {
                "MyCustomAvailableforReservation": 220.0
            }
        }
    }
]
```

Mukautettujen mittojen laskenta-asetukseen perustuva `MyCustomAvailableforReservation`-tulos on 100+50+80+90+30–10– 20–60–40=220.

## <a name="partition-configuration"></a><a name="partition-configuration"></a>Osion määritykset

Osion määritykset muodostuvat perusdimensioiden yhdistelmästä. Se määrittää tietojen jakelumallin. Saman osion tietotoiminnot ovat suorituskykyisiä ja suhteellisen edullisia. Tämän vuoksi hyvillä osiointimalleilla voidaan saada merkittäviä etuja.

Varaston näkyvyyssovelluksessa on seuraava osion oletusmääritys.

| Perusdimensio | Hierarkia |
|---|---|
| `SiteId` | 1 |
| `LocationId` | 2 |

> [!NOTE]
> Osion oletusmääritys on vain tiedoksi. Sitä ei tarvitse määrittää varaston näkyvyyssovelluksessa. Osion määrityksen päivitystä ei tällä hetkellä tueta.

## <a name="product-index-hierarchy-configuration"></a><a name="index-configuration"></a>Tuotehierarkiaindeksin määritykset

Suurimman osan aikaa käytettävissä olevan varaston kysely ei ole vain korkeimmalla kokonaistasolla. Sen sijaan halutaan ehkä nähdä tuloksia, jotka kootaan varastodimensioiden perusteella.

Varaston näkyvyyssovellus tuo joustavuutta antamalla mahdollisuuden _indeksien_ määrittämiseen. Nämä indeksit perustuvat dimensioon tai dimensioyhdistelmään. Indeksi koostuu *joukon numerosta*, *dimensiosta* ja *hierarkiasta*, jotka on määritetty seuraavan taulukon mukaisesti.

| Nimi | kuvaus |
|---|---|
| Joukon numero | Samaan joukkoon (indeksiin) kuuluvat dimensiot ryhmitellään yhteen ja niille määritetään sama joukon numero. |
| Dimensio | Perusdimensiot, joiden perusteella kyselyn tulos koostetaan. |
| Hierarkia | Hierarkian avulla määritetään tuetut dimensioyhdistelmät, joissa voidaan tehdä kyselyjä. Määritetään esimerkiksi dimensiojoukko, jonka hierarkiajärjestys on `(ColorId, SizeId, StyleId)`. Tässä tapauksessa järjestelmä tukee neljän dimensioyhdistelmän kyselyitä. Ensimmäinen yhdistelmä on tyhjä, toinen on `(ColorId)`, kolmas `(ColorId, SizeId)` ja neljäs `(ColorId, SizeId, StyleId)`. Muita yhdistelmiä ei tueta. Lisätietoja seuraavassa esimerkissä. |

### <a name="example"></a>Esimerkki

Tämän osan esimerkki näyttää, miten hierarkia toimii.

Varastossa on seuraavat nimikkeet.

| Nimike | ColorId | SizeId | StyleId | Määrä |
|---|---|---|---|---|
| T-paita | Musta | Pieni | Leveä | 1 |
| T-paita | Musta | Pieni | Säännöllinen | 2 |
| T-paita | Musta | Suuri | Leveä | 3 |
| T-paita | Musta | Suuri | Säännöllinen | 4 |
| T-paita | Punainen | Pieni | Leveä | 5 |
| T-paita | Punainen | Pieni | Säännöllinen | 6 |
| T-paita | Punainen | Suuri | Säännöllinen | 7 |

Indeksi on seuraavanlainen:

| Joukon numero | Dimensio | Hierarkia |
|---|---|---|
| 1 | `ColorId` | 1 |
| 1 | `SizeId` | 2 |
| 1 | `StyleId` | 3 |

Indeksin antaa mahdollisuuden tehdä kyselyjä käytettävissä olevassa varastossa seuraavin tavoin:

- `()` – ryhmittely kaikkien perusteella.

    - T-paita, 28

- `(ColorId)` – ryhmittelyperusteena `ColorId`

    - T-paita, musta, 10
    - T-paita, punainen, 18

- `(ColorId, SizeId)` – ryhmittelyperusteena `ColorId`- ja `SizeId`-yhdistelmä

    - T-paita, musta, S, 3
    - T-paita, musta, L, 7
    - T-paita, punainen, S, 11
    - T-paita, punainen, L, 7

- `(ColorId, SizeId, StyleId)` – ryhmittelyperusteena `ColorId`-, `SizeId`- ja `StyleId`-yhdistelmä

    - T-paita, musta, S, leveä, 1
    - T-paita, musta, S, normaali, 2
    - T-paita, musta, L, leveä, 3
    - T-paita, musta, L, normaali, 4
    - T-paita, punainen, S, leveä, 5
    - T-paita, punainen, S, normaali, 6
    - T-paita, punainen, L, normaali, 7

> [!NOTE]
> Osiomäärityksessä määritettyjä perusdimensioita ei saa määrittää indeksimäärityksissä.

## <a name="reservation-configuration-optional"></a><a name="reservation-configuration"></a>Varausmääritykset (valinnainen)

[!INCLUDE [preview-banner-section](../../includes/preview-banner-section.md)]

Varausmääritys on välttämätön, jos alustavaa varaustoimintoa halutaan käyttää. Määrityksessä on kaksi keskeistä osaa:

- Alustavan varauksen yhdistämismääritys
- Alustavan varauksen hierarkia

### <a name="soft-reservation-mapping"></a>Alustavan varauksen yhdistämismääritys

Varausta tehtäessä halutaan ehkä tietää, riittääkö käytettävissä oleva varasto varaukseen. Vahvistus on linkitetty laskennalliseen mittaan, joka ilmaistaan fyysisten mittojen yhdistelmän laskentakaavana.

Varausmitta voi perustua esimerkiksi `iv` (varaston näkyvyys) -tietolähteen fyysiseen `SoftReservOrdered`-mittaan. Siinä tapauksessa `iv`-tietolähteen laskennallinen `AvailableToReserve`-mitta määritetään kuten seuraavassa:

| Laskentalaji | Tietolähde | Fyysinen mitta |
|---|---|---|
| Lisäys | `fno` | `AvailPhysical` |
| Lisäys | `pos` | `Inbound` |
| Vähennyslasku | `pos` | `Outbound` |
| Vähennyslasku | `iv` | `SoftReservOrdered` |

Alustavan varauksen yhdistämismääritys määritetään sitten muodostamaan yhdistämismääritys varastusta `SoftReservOrdered`-mitasta laskennalliseen `AvailableToReserve`-mittaan.

| Fyysisen mitan tietolähde | Fyysinen mitta | Varaukseen käytettävissä olevan tietolähde | Varaukseen käytettävissä oleva laskennallinen mitta |
|---|---|---|---|
| `iv` | `SoftReservOrdered` | `iv` | `AvailableToReserve` |

Kun `SoftReservOrdered`-varaus nyt tehdään, varaston näkyvyyssovellus etsii automaattisesti `AvailableToReserve`-mitan ja siihen liittyvän laskentakaavan varauksen vahvistusta varten.

Varaston näkyvyyssovelluksessa on esimerkiksi seuraava käytettävissä oleva varasto.

```json
{
    "productId": "T-shirt",
    "dimensions": {
        "SiteId": "1",
        "LocationId": "11",
        "ColorId": "Red"
    },
    "quantities": {
        "iv": {
            "SoftReservOrdered": 90
        },
        "fno": {
            "availphysical": 70.0,
        },
        "pos": {
            "inbound": 50.0,
            "outbound": 20.0
        }
    }
}
```

Tässä tapauksessa käytetään seuraavaa laskelmaa:

`AvailableToReserve` = `fno.availphysical` + `pos.inbound` – `pos.outbound` – `iv.SoftReservOrdered`  
=70+50–20–90  
=10

Niinpä jos `iv.SoftReservOrdered`-varausta yritetään tehdä ja jos määrä on pieni tai sama kuin `AvailableToReserve` (10), varaus voidaan tehdä.

### <a name="soft-reservation-hierarchy"></a>Alustavan varauksen hierarkia

Varaushierarkia ilmaisee dimensiojärjestyksen, joka on määritettävä varauksia tehtäessä. Se toimii samalla tavoin kuin tuoteindeksihierarkia käytettävissä olevaa varastoa koskevissa kyselyissä.

Varaushierarkia on erillään tuoteindeksihierarkiasta. Tämä erillisyys antaa mahdollisuuden toteuttaa sellainen luokanhallinta, jossa käyttäjät voivat eritellä dimensiot vaatimukset määrittäviksi tiedoiksi. Tämä puolestaan antaa mahdollisuuden entistä tarkempiin varauksiin.

Esimerkki alustavan varauksen hierarkiasta.

| Perusdimensio | Hierarkia |
|---|---|
| `SiteId` | 1 |
| `LocationId` | 2 |
| `ColorId` | 3 |
| `SizeId` | 4 |
| `StyleId` | 5 |

Tässä esimerkissä varaus voidaan tehdä seuraavissa dimensiojärjestyksissä:

- `()` – dimensiota ei määritetä.
- `(SiteId)`
- `(SiteId, LocationId)`
- `(SiteId, LocationId, ColorId)`
- `(SiteId, LocationId, ColorId, SizeId)`
- `(SiteId, LocationId, ColorId, SizeId, StyleId)`

Kelvollisen dimensiojärjestyksen on noudatettava varaushierarkiaa tarkasti dimensio kerrallaan. Esimerkiksi hierarkiajärjestys `(SiteId, LocationId, SizeId)` ei kelpaa, koska `ColorId` puuttuu.

## <a name="default-configuration-sample"></a><a name="default-configuration-sample"></a>Oletusmääritysnäyte

Varaston näkyvyys määrittää alustuksen aikana oletusmäärityksen. Määritystä voi muokata tarpeen mukaan.

### <a name="data-source-configuration"></a>Tietolähteen määritykset

#### <a name="configuration-of-the-iv-data-source"></a>iv-tietolähteen määritykset

Tässä osassa käsitellään `iv`-tietolähteen määrittämistä.

##### <a name="physical-measures-configured-for-the-iv-data-source"></a>iv-tietolähteelle määritetyt fyysiset mitat

`iv`-tietolähteelle määritetään seuraavat fyysiset mitat:

- `Ordered`
- `SoftReservPhysical`
- `SoftReservOrdered`
- `ReservOrdered`
- `ReservPhysical`

##### <a name="orderedtotal-calculated-measure"></a>Laskennallinen OrderedTotal-mitta

Laskennallinen `OrderedTotal`-mitta määritetään `iv`-tietolähteelle kuten seuraavassa taulukossa.

| Laskentalaji | Tietolähde | Fyysinen mitta |
|---|---|---|
| Lisäys | `fno` | `Ordered` |
| Lisäys | `fno` | `Arrived` |
| Lisäys | `iv` | `Ordered` |

##### <a name="onhand-calculated-measure"></a>Laskennallinen OnHand-mitta

Laskennallinen `OnHand`-mitta määritetään `iv`-tietolähteelle kuten seuraavassa taulukossa.

| Laskentalaji | Tietolähde | Fyysinen mitta |
|---|---|---|
| Lisäys | `fno` | `PhysicalInvent` |
| Lisäys | `iom` | `OnHand` |
| Lisäys | `erp` | `Unrestricted` |
| Lisäys | `erp` | `QualityInspection` |
| Lisäys | `pos` | `PosInbound` |
| Vähennyslasku | `pos` | `PosOutbound` |

##### <a name="reservedtotal-calculated-measure"></a>Laskennallinen ReservedTotal-mitta

Laskennallinen `ReservedTotal`-mitta määritetään `iv`-tietolähteelle kuten seuraavassa taulukossa.

| Laskentalaji | Tietolähde | Fyysinen mitta |
|---|---|---|
| Lisäys | `fno` | `ReservPhysical` |
| Lisäys | `fno` | `ReservOrdered` |
| Lisäys | `iv` | `SoftReservPhysical` |
| Lisäys | `iv` | `SoftReservOrdered` |
| Lisäys | `iv` | `ReservPhysical` |
| Lisäys | `iv` | `ReservOrdered` |

##### <a name="softreserved-calculated-measure"></a>Laskennallinen SoftReserved-mitta

Laskennallinen `SoftReserved`-mitta määritetään `iv`-tietolähteelle kuten seuraavassa taulukossa.

| Laskentalaji | Tietolähde | Fyysinen mitta |
|---|---|---|
| Lisäys | `iv` | `SoftReservPhysical` |
| Lisäys | `iv` | `SoftReservOrdered` |

##### <a name="hardreserved-calculated-measure"></a>Laskennallinen HardReserved-mitta

Laskennallinen `HardReserved`-mitta määritetään `iv`-tietolähteelle kuten seuraavassa taulukossa.

| Laskentalaji | Tietolähde | Fyysinen mitta |
|---|---|---|
| Lisäys | `fno` | `ReservPhysical` |
| Lisäys | `fno` | `ReservOrdered` |
| Lisäys | `iv` | `ReservPhysical` |
| Lisäys | `iv` | `ReservOrdered` |

##### <a name="openorder-calculated-measure"></a>Laskennallinen OpenOrder-mitta

Laskennallinen `OpenOrder`-mitta määritetään `iv`-tietolähteelle kuten seuraavassa taulukossa.

| Laskentalaji | Tietolähde | Fyysinen mitta |
|---|---|---|
| Lisäys | `fno` | `OnOrder` |
| Lisäys | `iom` | `OnOrder` |

##### <a name="onhandavailable-calculated-measure"></a>Laskennallinen OnHandAvailable-mitta

Laskennallinen `OnHandAvailable`-mitta määritetään `iv`-tietolähteelle kuten seuraavassa taulukossa.

| Laskentalaji | Tietolähde | Fyysinen mitta |
|---|---|---|
| Lisäys | `fno` | `PhysicalInvent` |
| Lisäys | `iom` | `OnHand` |
| Lisäys | `erp` | `Unrestricted` |
| Lisäys | `erp` | `QualityInspection` |
| Lisäys | `pos` | `PosInbound` |
| Vähennyslasku | `fno` | `ReservPhysical` |
| Vähennyslasku | `iv` | `SoftReservPhysical` |
| Vähennyslasku | `pos` | `PosOutbound` |

##### <a name="availabletoreserve-calculated-measure"></a>Laskennallinen AvailableToReserve-mitta

Laskennallinen `AvailableToReserve`-mitta määritetään `iv`-tietolähteelle kuten seuraavassa taulukossa.

| Laskentalaji | Tietolähde | Fyysinen mitta |
|---|---|---|
| Lisäys | `fno` | `PhysicalInvent` |
| Lisäys | `iom` | `OnHand` |
| Lisäys | `erp` | `Unrestricted` |
| Lisäys | `erp` | `QualityInspection` |
| Lisäys | `pos` | `PosInbound` |
| Lisäys | `fno` | `Ordered` |
| Lisäys | `fno` | `Arrived` |
| Lisäys | `iv` | `Ordered` |
| Vähennyslasku | `fno` | `ReservPhysical` |
| Vähennyslasku | `fno` | `ReservOrdered` |
| Vähennyslasku | `iv` | `SoftReservPhysical` |
| Vähennyslasku | `iv` | `SoftReservOrdered` |
| Vähennyslasku | `iv` | `ReservPhysical` |
| Vähennyslasku | `iv` | `ReservOrdered` |
| Vähennyslasku | `pos` | `PosOutbound` |

##### <a name="inventorysupply-calculated-measure"></a>Laskennallinen InventorySupply-mitta

Laskennallinen `InventorySupply`-mitta määritetään `iv`-tietolähteelle kuten seuraavassa taulukossa.

| Laskentalaji | Tietolähde | Fyysinen mitta |
|---|---|---|
| Lisäys | `fno` | `Ordered` |
| Lisäys | `fno` | `Arrived` |
| Lisäys | `iv` | `Ordered` |
| Lisäys | `fno` | `PhysicalInvent` |
| Lisäys | `iom` | `OnHand` |
| Lisäys | `erp` | `Unrestricted` |
| Lisäys | `erp` | `QualityInspection` |
| Lisäys | `pos` | `PosInbound` |
| Vähennyslasku | `pos` | `PosOutbound` |

##### <a name="inventorydemand-calculated-measure"></a>Laskennallinen InventoryDemand-mitta

Laskennallinen `InventoryDemand`-mitta määritetään `iv`-tietolähteelle kuten seuraavassa taulukossa.

| Laskentalaji | Tietolähde | Fyysinen mitta |
|---|---|---|
| Lisäys | `fno` | `OnOrder` |
| Lisäys | `iom` | `OnOrder` |
| Lisäys | `iv` | `SoftReservPhysical` |
| Lisäys | `iv` | `SoftReservOrdered` |
| Lisäys | `fno` | `ReservPhysical` |
| Lisäys | `fno` | `ReservOrdered` |
| Lisäys | `iv` | `ReservPhysical` |
| Lisäys | `iv` | `ReservOrdered` |

#### <a name="configuration-of-the-fno-data-source"></a>fno-tietolähteen määritykset

Tässä osassa käsitellään `fno`-tietolähteen määrittämistä.

##### <a name="dimension-mappings-for-the-fno-data-source"></a>fno-tietolähteen dimension yhdistämismääritykset

Seuraavan taulukon dimension yhdistämismääritykset on määritetty `fno`-tietolähteelle.

| Ulkoinen dimensio | Perusdimensio |
|---|---|
| `InventBatchId` | `BatchId` |
| `InventColorId` | `ColorId` |
| `InventLocationId` | `LocationId` |
| `InventSerialId` | `SerialId` |
| `InventSiteId` | `SiteId` |
| `InventSizeId` | `SizeId` |
| `InventStatusId` | `StatusId` |
| `InventStyleId` | `StyleId` |
| `LicensePlateId` | `LicensePlateId` |
| `WMSLocationId` | `WMSLocationId` |
| `WMSPalletId` | `WMSPalletId` |
| `ConfigId` | `ConfigId` |
| `InventVersionId` | `VersionId` |
| `InventDimension1` | `CustomDimension1` |
| `InventDimension2` | `CustomDimension2` |
| `InventDimension3` | `CustomDimension3` |
| `InventDimension4` | `CustomDimension4` |
| `InventDimension5` | `CustomDimension5` |
| `InventDimension6` | `CustomDimension6` |
| `InventDimension7` | `CustomDimension7` |
| `InventDimension8` | `CustomDimension8` |
| `InventDimension9` | `CustomDimension9` |
| `InventDimension10` | `CustomDimension10` |
| `InventDimension11` | `CustomDimension11` |
| `InventDimension12` | `CustomDimension12` |

##### <a name="physical-measures-configured-for-the-fno-data-source"></a>fno-tietolähteelle määritetyt fyysiset mitat

`fno`-tietolähteelle määritetään seuraavat fyysiset mitat:

- `Ordered`
- `Arrived`
- `AvailPhysical`
- `PhysicalInvent`
- `ReservPhysical`
- `ReservOrdered`
- `OnOrder`

#### <a name="configuration-of-the-pos-data-source"></a>pos-tietolähteen määritykset

Tässä osassa käsitellään `pos`-tietolähteen määrittämistä.

##### <a name="physical-measures-for-the-pos-data-source"></a>pos-tietolähteelle määritetyt fyysiset mitat

`pos`-tietolähteelle määritetään seuraavat fyysiset mitat:

- `PosInbound`
- `PosOutbound`

##### <a name="availquantity-calculated-measure"></a>Laskennallinen AvailQuantity-mitta

Laskennallinen `AvailQuantity`-mitta määritetään `pos`-tietolähteelle kuten seuraavassa taulukossa.

| Laskentalaji | Tietolähde | Fyysinen mitta |
|---|---|---|
| Lisäys | `fno` | `AvailPhysical` |
| Lisäys | `pos` | `PosInbound` |
| Vähennyslasku | `pos` | `PosOutbound` |

#### <a name="configuration-of-the-iom-data-source"></a>iom-tietolähteen määritykset

`iom` (intelligent order management) -tietolähteelle määritetään seuraavat fyysiset mitat:

- `OnOrder`
- `OnHand`

#### <a name="configuration-of-the-erp-data-source"></a>erp-tietolähteen määritykset

`erp` (toiminnanohjausjärjestelmä) -tietolähteelle määritetään seuraavat fyysiset mitat:

- `Unrestricted`
- `QualityInspection`

### <a name="partition-configuration"></a>Osion määritykset

Seuraavassa taulukossa on osion oletusmääritys.

| Perusdimensio | Hierarkia |
|---|---|
| `SiteId` | 1 |
| `LocationId` | 2 |

### <a name="index-configuration"></a>Indeksin määritykset

Seuraavassa taulukossa on indeksin oletusmääritys.

| Joukon numero | Dimensio | Hierarkia |
|---|---|---|
| 1 | `ColorId` | 1 |
| 1 | `SizeId` | 2 |
| 1 | `StyleId` | 3 |

### <a name="reservation-configuration"></a>Varausmääritykset

Tässä osassa käsitellään varauksen oletusmääritystä.

#### <a name="reservation-mapping"></a>Varauksen yhdistämismääritys

[!INCLUDE [preview-banner-section](../../includes/preview-banner-section.md)]

Seuraavassa taulukossa on varauksen oletusarvoinen yhdistämismääritys.

| Fyysisen mitan tietolähde | Fyysinen mitta | Varaukseen käytettävissä olevan tietolähde | Varaukseen käytettävissä oleva laskennallinen mitta |
|---|---|---|---|
| `iv` | `SoftReservOrdered` | `iv` | `AvailableToReserve` |

#### <a name="reservation-hierarchy"></a>Varaushierarkia

Seuraavassa taulukossa on varauksen oletushierarkia.

| Perusdimensio | Hierarkia |
|---|---|
| `SiteId` | 1 |
| `LocationId` | 2 |
| `ColorId` | 3 |
| `SizeId` | 4 |
| `StyleId` | 5 |
| `BatchId` | 6 |
| `SerialId` | 7 |
| `StatusId` | 8 |
| `LicensePlateId` | 9 |
| `WMSLocationId` | 10 |
| `WMSPalletId` | 11 |
| `ConfigId` | 12 |
| `VersionId` | 13 |
| `CustomDimension1` | 14 |
| `CustomDimension2` | 15 |
| `CustomDimension3` | 16 |
| `CustomDimension4` | 17 |
| `CustomDimension5` | 18 |
| `CustomDimension6` | 19 |
| `CustomDimension7` | 20 |
| `CustomDimension8` | 21 |
| `CustomDimension9` | 22 |
| `CustomDimension10` | 23 |
| `CustomDimension11` | 24 |
| `CustomDimension12` | 25 |
| `ExtendedDimension1` | 26 |
| `ExtendedDimension2` | 27 |
| `ExtendedDimension3` | 28 |
| `ExtendedDimension4` | 29 |
| `ExtendedDimension5` | 30 |
| `ExtendedDimension6` | 31 |
| `ExtendedDimension7` | 32 |
| `ExtendedDimension8` | 33 |

[!INCLUDE[footer-include](../../includes/footer-banner.md)]