---
title: Inventory Visibilityn määrittäminen
description: Tässä artikkelissa käsitellään varaston näkyvyyden määrittämistä.
author: yufeihuang
ms.date: 11/04/2022
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2021-08-02
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: 2a368535c9644e174d1a2460ac0891c9dc1b1b3f
ms.sourcegitcommit: 44f0b4ef8d74c86b5c5040be37981e32eb43e1a8
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/14/2022
ms.locfileid: "9850020"
---
# <a name="configure-inventory-visibility"></a>Inventory Visibilityn määrittäminen

[!include [banner](../includes/banner.md)]

Tässä artikkelissa käsitellään varaston näkyvyyden määrittämistä varaston näkyvyyssovelluksen avulla Power Appsissa.

## <a name="introduction"></a><a name="introduction"></a>Johdanto

Ennen varaston näkyvyyssovelluksen käytön aloittamista on tehtävä seuraavat määritykset tässä artikkelissa kuvatulla tavalla:

- [Tietolähteen määritykset](#data-source-configuration)
- [Osion määritykset](#partition-configuration)
- [Tuotehierarkiaindeksin määritykset](#index-configuration)
- [Varausmääritykset (valinnainen)](#reservation-configuration)
- [Kyselyn esilatauksen määritys (valinnainen)](#query-preload-configuration)
- [Oletusmääritysnäyte](#default-configuration-sample)

## <a name="prerequisites"></a>Edellytykset

Varaston näkyvyyden apuohjelma on asennettava ja määritettävä ennen aloittamista kohdassa [Varaston näkyvyyden asennus ja määritys](inventory-visibility-setup.md) kuvatulla tavalla.

## <a name="the-configuration-page-of-the-inventory-visibility-app"></a><a name="configuration"></a>Varaston näkyvyyssovelluksen määrityssivu

Power Appsissa [varaston näkyvyyssovelluksen](inventory-visibility-power-platform.md) **Määritys**-sivu auttaa määrittämään käytettävissä olevan varaston ja alustavan varauksen. Kun apuohjelma on asennettu, oletusmääritys sisältää Microsoft Dynamics 365 Supply Chain Managementin arvon (`fno`-tietolähde). Oletusasetukset voidaan tarkistaa. Määritystä voidaan lisäksi muokata liiketoimintatarpeiden ja ulkoisen järjestelmän varastokirjaustarpeiden mukaan siten, että useissa järjestelmissä käytetään standardoitua varastomuutosten kirjausta, järjestämistä ja kyselyä. Tämän artikkelin jäljellä olevissa osissa käsitellään **Määritys**-sivun kunkin osan käyttämistä.

Kun määritykset on tehty, muista valita sovelluksessa **Päivitä määritys**.

## <a name="enable-inventory-visibility-features-in-power-apps-feature-management"></a><a name="feature-switch"></a>Varaston näkyvyysominaisuuksien käyttöönotto Power Appsin ominaisuuksienhallinnassa

Varaston näkyvyyden lisäosa lisää Power Apps-asennukseen useita uusia ominaisuuksia. Nämä ominaisuudet on oletusarvoisesti poistettu käytöstä. Niitä voidaan käyttää avaamalla **Määritys**-sivu ja ottamalla seuraavat ominaisuudet sitten vaatimustesi mukaan käyttöön **Ominaisuuden hallinta** -välilehdessä.

| Ominaisuuksien hallinnan nimi | Kuvaus |
|---|---|
| *OnHandReservation* | Tämä ominaisuus auttaa sinua luomaan varauksia, käyttämään varauksia ja/tai poistamaan määritettyjen varastomäärien varauksia varaston näkyvyyssovelluksella. Lisätietoja on kohdassa [Varaston näkyvyyden varaukset](inventory-visibility-reservations.md). |
| *OnHandMostSpecificBackgroundService* | Tämä ominaisuus sisältää tuotteiden ja kaikkien dimensioiden varaston yhteenvedon. Varaston yhteenvetotiedot synkronoidaan säännöllisesti varaston näkyvyydestä. Synkronoinnin oletustiheys on 15 minuuttia. Se voidaan määrittää tehtäväksi enintään 5 minuutin välein. Lisätietoja on kohdassa [Varastoyhteenveto](inventory-visibility-power-platform.md#inventory-summary). |
| *OnHandIndexQueryPreloadBackgroundService* | Tämä ominaisuus noutaa ja tallentaa säännöllisesti käytettävissä olevan varaston yhteenvetotiedot valmiiksi määritettyjen dimensioiden perusteella. Se tuottaa varastoyhteenvedon, joka sisältää vain päivittäiseen liiketoimintaan liittyvä dimensiot ja joka yhteensopiva varastonhallintaprosesseja käyttävien nimikkeiden kanssa. Lisätietoja on kohdissa [Valmiiksi ladattujen käytettävissä olevan varaston kyselyjen ottaminen käyttöön ja määrittäminen](#query-preload-configuration) ja [Käytettävissä olevan varaston virtaviivaistetun kyselyn esilataaminen](inventory-visibility-power-platform.md#preload-streamlined-onhand-query). |
| *OnhandChangeSchedule* | Tämä valinnainen ominaisuus ottaa käyttöön käytettävissä olevan vaihtoaikataulun ja luvattavissa olevan määrän (ATP) ominaisuudet. Lisätietoja on kohdassa [Käytettävissä olevan varaston näkyvyyden muutosaikataulu ja luvattavissa ole aikataulu](inventory-visibility-available-to-promise.md). |
| *Varaus* | Tämän valinnaisen ominaisuuden avulla Inventory Visibility voi mahdollistaa varaston suojauksen (ring fencing) ja ylimyynnin hallinnan. Lisätietoja on kohdassa [Varaston näkyvyyden varaston kohdistus](inventory-visibility-allocation.md). |
| *Ota varastonimikkeet käyttöön Varaston näkyvyys -kohdassa* | Tämän valinnaisen ominaisuuden avulla varaston näkyvyys tukee nimikkeitä, jotka on otettu käyttöön varastonhallintaprosesseissa (WMS). Lisätietoja on kohdassa [Varaston näkyvyyden tuki WMS-nimikkeille](inventory-visibility-whs-support.md). |

> [!IMPORTANT]
> On suositeltavaa käyttää joko *OnHandIndexQueryPreloadBackgroundService*- tai *OnHandMostSpecificBackgroundService*-ominaisuutta mutta ei molempia. Molempien ominaisuuksien ottaminen käyttää vaikuttaa suorituskykyyn.

## <a name="find-the-service-endpoint"></a><a name="get-service-endpoint"></a>Palvelun päätepisteen etsiminen

Jos oikea varaston näkyvyyspalvelun päätepiste ei ole tiedossa, avaa **Määritys**-sivu Power Appsissa ja valitse sitten **Näytä palvelun tiedot** oikeassa yläkulmassa. Sivulla näkyy oikea palvelun päätepiste. Päätepiste löytyy myös Microsoft Dynamics Lifecycle Servicesista kohdan [Lifecycle Services -ympäristön mukaisen päätepisteen etsiminen](inventory-visibility-api.md#endpoint-lcs) -ohjeiden mukaisesti.

> [!NOTE]
> Virheellisen päätepisteen käyttäminen voi aiheuttaa Inventory Visibility -asennuksen epäonnistumisen ja virheitä Supply Chain Managementin ja Inventory Visibilityn integroinnissa. Jos et ole varma, mitä päätepistettä tulisi käyttää, ota yhteyttä järjestelmänvalvojaan. Päätepisteiden URL-osoitteet ovat seuraavassa muodossa:
>
> `https://inventoryservice.<RegionShortName>-il<IsLandNumber>.gateway.prod.island.powerapps.com`

## <a name="data-source-configuration"></a><a name="data-source-configuration"></a>Tietolähteen määritykset

Kukin tietolähde ilmaisee järjestelmän, josta tiedot tulevat. Esimerkkejä tietolähteiden nimistä ovat `fno` (joka vastaa Supply Chain Managementia) ja `pos` (joka tarkoittaa myyntipistettä). Supply Chain Management määritetään oletusarvoisesti varaston näkyvyyssovelluksen oletustietolähteeksi (`fno`).

> [!NOTE]
> `fno`-tietolähde on varattu Supply Chain Managementia varten. Jos Inventory Visibility -apuohjelma on integroitu Supply Chain Management -ympäristöön, on suositeltavaa, ettei tietolähteen kohteeseen `fno` liittyviä määrityksiä poisteta.

Tietolähde lisätään seuraavasti:

1. Kirjaudu Power Apps -ympäristöön ja avaa **Varaston näkyvyys**.
1. Avaa **Määritykset**-sivu.
1. Valitse **Tietolähde**-välilehdessä **Uusi tietolähde**, jos haluat lisätä tietolähteen (joka voi olla esimerkiksi `ecommerce` tai toinen merkityksellinen tietolähteen tunnus).

> [!NOTE]
> Tietolähdettä lisättäessä tietolähteen nimi, fyysiset mitat ja dimensioiden yhdistämismääritykset on tarkistettava ennen määrityksen päivittämistä varaston näkyvyyspalveluun. Näitä asetuksia ei voi muokata sen jälkeen, kun **Päivitä määritys** on valittu.

Tietolähdemääritykset sisältävät seuraavat osat:

- Dimensiot (dimension yhdistämismääritys)
- Fyysiset mitat
- Laskennalliset mitat

### <a name="dimensions-dimension-mapping"></a><a name="data-source-configuration-dimension"></a>Dimensiot (dimension yhdistämismääritys)

Dimensiomääritysten tarkoitus on standardoida monien järjestelmien integrointi dimensioyhdistelmiin perustuvien tapahtumien kirjaamista ja niihin perustuvia kyselyjä varten. Varaston näkyvyyssovelluksessa on luettelo perusdimensioita, jotka voidaan yhdistää tietolähteen dimensioista. Yhdistämismäärityksissä on käytettävissä 33 dimensiota.

- Jos yhtenä tietolähteenä on Supply Chain Management, 13 dimensiota on jo yhdistetty oletusarvoisesti Supply Chain Managementin vakiodimensioihin. 12 muuta dimensiosta (`inventDimension1`–`inventDimension12`) yhdistetään myös Supply Chain Managementin mukautettuihin dimensioihin. Loput kahdeksan dimensiota (`ExtendedDimension1`–`ExtendedDimension8`) ovat laajennettuja dimensioita, jotka voidaan yhdistää ulkoisiin tietolähteisiin.
- Jos Supply Chain Managementia ei käytetä yhtenä tietolähteenä, dimensiot voidaan yhdistää vapaasti. Seuraavassa taulukossa on käytettävissä olevien dimensioiden täydellinen luettelo.

> [!NOTE]
> Jos käytössä on Supply Chain Management ja muutat Supply Chain Managementin ja Inventory Visibilityn välisiä dimension oletusyhdistämismäärityksiä, muutetut dimensiot eivät synkronoi tietoja. Jos siis dimensio ei ole oletusdimensioluettelossa ja käytössä on ulkoinen tietolähde, yhdistämismäärityksessä kannattaa käyttää dimensioita `ExtendedDimension1`–`ExtendedDimension8`.

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
| Laajennus | `ExtendedDimension1`–`ExtendedDimension8` |
| System | `Empty` |

> [!NOTE]
> Edellisessä taulukossa mainitut dimensiotyypit on tarkoitettu vain tiedoksi. Niitä ei tarvitse määrittää varaston näkyvyyssovelluksessa.
>
> Varaston (mukautetut) dimensiot on ehkä varattu Supply Chain Management -käyttöä varten. Siinä tapauksessa niiden tilalla voidaan käyttää laajennettuja dimensioita.

Ulkoiset järjestelmät voivat käyttää varaston näkyvyyssovellusta sovelluksen RESTful API -ohjelmointirajapintojen kautta. Integrointia varten varaston näkyvyyssovellus sallii *ulkoisen tietolähteen* määrittämisen ja yhdistämismääritykset *ulkoisista dimensioista* *perusdimensioihin*. Esimerkki dimension yhdistämismääritystaulukosta.

| Ulkoinen dimensio | Perusdimensio |
|---|---|
| `MyColorId` | `ColorId` |
| `MySizeId` | `SizeId` |
| `MyStyleId` | `StyleId` |
| `MyDimension1` | `ExtendedDimension1` |
| `MyDimension2` | `ExtendedDimension2` |

Dimension yhdistämismäärityksen avulla ulkoiset dimensiot voidaan lähettää suoraan varaston näkyvyyssovellukseen. Varaston näkyvyyssovellus muuntaa sitten ulkoiset dimensiot automaattisesti perusdimensioiksi.

Dimension yhdistämismääritykset lisätään seuraavasti:

1. Kirjaudu Power Apps -ympäristöön ja avaa **Varaston näkyvyys**.
1. Avaa **Määritykset**-sivu.
1. Valitse **Tietolähde**-välilehdessä tietolähde, jossa haluat tehdä dimension yhdistämismäärityksen. Valitse sitten **Dimension yhdistämismääritykset** -osassa **Lisää**, jos haluat lisätä dimension yhdistämismäärityksen.

    ![Dimension yhdistämismääritysten lisääminen](media/inventory-visibility-dimension-mapping.png "Dimension yhdistämismääritysten lisääminen")

1. Määritä lähdedimensio **Dimension nimi** -kentässä.
1. Valitse **Perusdimensioon**-kentässä yhdistettävä varaston näkyvyyssovelluksen dimensio.
1. Valitse **Tallenna**.

Jos olet esimerkiksi luonut jo tietolähteen nimeltä `ecommerce` ja se sisältää tuotteen väridimension. Tässä tapauksessa voit tehdä yhdistämismäärityksen lisäämällä ensin arvon `ProductColor` **Dimension nimi** -kenttään tietolähteessä `ecommerce` ja valitsemalla arvon `ColorId` **Perusdimensioon**-kentässä.

### <a name="physical-measures"></a><a name="data-source-configuration-physical-measures"></a>Fyysiset mitat

Kun tietolähde kirjaa varastonmuutoksen varaston näkyvyyssovellukseen, muutoksen kirjaamiseen käytetään *fyysisiä mittoja*. Fyysiset mitat muokkaavat määrän vastaamaan varaston tilaa. Fyysiset mitat voidaan määrittää omien tarpeiden mukaan. Kyselyt voivat perustua fyysisiin mittoihin.

Inventory Visibilityssa on luettelo fyysisistä oletusmitoista. Tämä luettelo on yhdistetty Supply Chain Managementiin (tietolähde `fno`). Nämä fyysiset oletusmitat saadaan Supply Chain Managementin **Varastoluettelo**-sivulla (**Varastonhallinta \> Kyselyt ja raportit \> Varastoluettelo**) olevista varastotapahtuman tiloista. Seuraavassa taulukossa on esimerkki fyysisistä mitoista:

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

Jos tietolähde on Supply Chain Management, fyysisiä oletusmittoja ei tarvitse luoda uudelleen. Jos kyse on kuitenkin ulkoisista tietolähteistä, uudet fyysiset mitat voidaan luoda seuraavasti:

1. Kirjaudu Power Apps -ympäristöön ja avaa **Varaston näkyvyys**.
1. Avaa **Määritykset**-sivu.
1. Valitse **Tietolähde**-välilehdessä tietolähde, johon lisätään fyysiset mitat (esimerkiksi tietolähde `ecommerce`). Valitse sitten **Fyysiset mitat** -osassa **Lisää** ja määritä mitan nimi (esimerkiksi `Returned`, jos haluat tallentaa palautetut määrät tässä tietolähteessä Inventory Visibilityyn). Tallenna muutokset.

### <a name="extended-dimensions"></a>Laajennetut dimensiot

Asiakkaat, jotka haluavat käyttää ulkoisia tietolähteitä tietolähteessä, voivat hyödyntää Dynamics 365:n laajennettavuutta luomalla `InventOnHandChangeEventDimensionSet`- ja `InventInventoryDataServiceBatchJobTask`-luokille [luokkalaajennuksia](../../fin-ops-core/dev-itpro/extensibility/class-extensions.md).

Tietokanta on muistettava synkronoida laajennusten luonnin jälkeen, sillä mukautetut kentät lisätään näin `InventSum`-taulukkoon. Sen jälkeen mukautetut dimensiot voidaan yhdistää tämän artikkelin Dimensiot-osan ohjeiden mukaisesti mihin tahansa varaston kahdeksaan laajennettuun `BaseDimensions`-dimensioon.

> [!NOTE] 
> Lisätietoja laajennusten luomisesta on kohdassa [Laajennettavuuden aloitussivu](../../fin-ops-core/dev-itpro/extensibility/extensibility-home-page.md).

### <a name="calculated-measures"></a>Laskennalliset mitat

Varaston näkyvyyssovelluksen avulla voidaan tehdä sekä varaston fyysisiä mittoja että *mukautettuja laskennallisia mittoja* koskevia kyselyjä. Laskennalliset mitat ovat mukautettu laskentakaava, joka koostuu fyysisten mittojen yhdistelmästä. Tämä toiminto antaa mahdollisuuden määrittää lisättävät ja/tai vähennettävät fyysiset mitat, joiden avulla voidaan muodostaa mukautettu mitta.

> [!IMPORTANT]
> Laskettu mitta on fyysisten mittojen yhdistelmä. Sen kaava voi sisältää vain fyysisiä mittoja ilman kaksoiskappaleita, ei laskettuja mittoja.

Määritys antaa mahdollisuuden määrittää laskettujen mittakaavojen joukon, joka sisältää lisäys- tai vähennysmääreitä. Niiden avulla saadaan tietää koostetuloksen kokonaismäärä.

Voit määrittää mukautetun laskennallisen mitan noudattamalla seuraavia ohjeita.

1. Kirjaudu Power Apps -ympäristöön ja avaa **Varaston näkyvyys**.
1. Avaa **Määritykset**-sivu.
1. Lisää laskennallinen mitta valitsemalla **Laskennallinen mitta** -välilehdessä **Uusi laskennallinen mitta**.
1. Määritä uudelle lasketulle määrälle seuraavat kentät:

    - **Uusi laskettu mitan nimi** – Kirjoita lasketun mitan nimi.
    - **Tietolähde** – Valitse uuteen laskettuun mittaan sisältyvä tietolähde. Kyselyjärjestelmä on tietolähde.

1. Lisää uuteen laskettuun mittariin määre valitsemalla **Lisää**.
1. Määritä uudelle määreelle seuraavat kentät:

    - **Määre** – Valitse määreen tyyppi (*Lisäys* tai *Vähennys*).
    - **Tietolähde** – Valitse tietolähde, josta määrearvon antava mittayksikkö löytyy.
    - **Määre** – Valitse (valitusta tietolähteestä) määreen nimi, joka sisältää muuttujan arvon.

1. Toista vaiheet 5 ja 6, kunnes olet lisännyt kaikki vaaditut määreet ja tehnyt lasketun mitan kaavan valmiiksi.
1. Valitse **Tallenna**.

Esimerkiksi muotialan yritys käyttää seuraavia kolmea tietolähdettä:

- `pos` – vastaa myymälän kanavaa.
- `fno` – vastaa Supply Chain Managementia.
- `ecommerce` – vastaa verkkokanavaa.

Kun tehdään kysely tuotteesta D0002 (kaappi) ilman laskettuja mittoja toimipaikassa 1, varastossa 11 ja kohteen `ColorID`  dimension arvolla `Red`, saatetaan saada seuraava kyselytulos. Se osoittaa kunkin esimääritetyn fyysisen mitan varastomäärät. Tietolähteissä ei kuitenkaan ole näkyvyyttä varausmäärien kokonaissaatavuuteen.

```json
[
    {
        "productId": "D0002",
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
            "ecommerce": {
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
| `CrossChannel` | `MyCustomAvailableforReservation` | `fno` | `availphysical` | `Addition` |
| `CrossChannel` | `MyCustomAvailableforReservation` | `fno` | `orderedintotal` | `Addition` |
| `CrossChannel` | `MyCustomAvailableforReservation` | `fno` | `orderedreserved` | `Subtraction` |
| `CrossChannel` | `MyCustomAvailableforReservation` | `pos` | `inbound` | `Addition` |
| `CrossChannel` | `MyCustomAvailableforReservation` | `pos` | `outbound` | `Subtraction` |
| `CrossChannel` | `MyCustomAvailableforReservation` | `ecommerce` | `received` | `Addition` |
| `CrossChannel` | `MyCustomAvailableforReservation` | `ecommerce` | `scheduled` | `Addition` |
| `CrossChannel` | `MyCustomAvailableforReservation` | `ecommerce` | `issued` | `Subtraction` |
| `CrossChannel` | `MyCustomAvailableforReservation` | `ecommerce` | `reserved` | `Subtraction` |

Tätä laskentakaavaa käytettäessä uudessa kyselyn tuloksessa on mukautettu mitta.

```json
[
    {
        "productId": "D0002",
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
            "ecommerce": {
                "received": 90.0,
                "scheduled": 30.0,
                "issued": 60.0,
                "reserved": 40.0
            },
            "CrossChannel": {
                "MyCustomAvailableforReservation": 220.0
            }
        }
    }
]
```

Mukautettujen mittojen laskenta-asetukseen perustuva `MyCustomAvailableforReservation`-tulos on 100 + 50 – 10 + 80 – 20 + 90 + 30 – 60 – 40 = 220.

## <a name="partition-configuration"></a><a name="partition-configuration"></a>Osion määritykset

Tällä hetkellä osiointimääritys koostuu kahdesta perusdimensiosta (`SiteId` ja `LocationId`), jotka ilmaisevat tietojen jakelun. Samaan osiointiin liittyvät toiminnot voivat tuottaa suuremman suorituskyvyn alhaisemmin kustannuksin. Seuraavassa taulukossa näkyy osion oletusmääritys, jonka varaston näkyvyyssovellus tarjoaa.

| Perusdimensio | Hierarkia |
|---|---|
| `SiteId` | 1 |
| `LocationId` | 2 |

Ratkaisu sisältää oletusarvon mukaan tämän osiointimäärityksen. Näin ollen *sinun ei tarvitse määrittää sitä itse*.

> [!IMPORTANT]
> Älä mukauta oletusosiointimääritystä. Jos poistat tai muutat sitä, se aiheuttaa todennäköisesti odottamattoman virheen.

## <a name="product-index-hierarchy-configuration"></a><a name="index-configuration"></a>Tuotehierarkiaindeksin määritykset

Suurimman osan aikaa käytettävissä olevan varaston kysely ei ole vain korkeimmalla kokonaistasolla. Sen sijaan halutaan ehkä nähdä tuloksia, jotka kootaan varastodimensioiden perusteella.

Varaston näkyvyys mahdollistaa joustavuuden, koska voit määrittää *indeksejä* kyselyjen suorituskyvyn parantamiseksi. Nämä indeksit perustuvat dimensioon tai dimensioyhdistelmään. Indeksi koostuu *joukon numerosta*, *dimensiosta* ja *hierarkiasta*, jotka on määritetty seuraavan taulukon mukaisesti.

| Nimi | kuvaus |
|---|---|
| Joukon numero | Samaan joukkoon (indeksiin) kuuluvat dimensiot ryhmitellään yhteen ja niille määritetään sama joukon numero. |
| Dimensio | Perusdimensiot, joiden perusteella kyselyn tulos koostetaan. |
| Hierarkia | Hierarkian avulla voit parantaa tiettyjen dimensioyhdistelmien suorituskykyä suodatus- ja ryhmittelykyselyparametreissa. Jos dimensiojoukko määritetään esimerkiksi käyttämällä hierarkiasarjaa `(ColorId, SizeId, StyleId)`, järjestelmä voi käsitellä neljään dimensioyhdistelmään liittyvät kyselyt aiempaa nopeammin. Ensimmäinen yhdistelmä on tyhjä, toinen on `(ColorId)`, kolmas `(ColorId, SizeId)` ja neljäs `(ColorId, SizeId, StyleId)`. Muiden yhdistelmien käsittelemistä ei voi nopeuttaa. Suodattimia ei rajoiteta järjestyksen mukaan. Niiden on kuitenkin oltava näiden dimensioiden sisällä, jos suorituskykyä halutaan parantaa. Lisätietoja seuraavassa esimerkissä. |

Tuotehierarkiaindeksi määritetään seuraavasti:

1. Kirjaudu Power Apps -ympäristöön ja avaa **Varaston näkyvyys**.
1. Avaa **Määritykset**-sivu.
1. Lisää dimension yhdistämismääritykset valitsemalla **Tuotehierarkiaindeksi**-välilehden **Dimension yhdistämismääritykset** -osassa **Lisää**.
1. Indeksiluettelo annetaan oletusarvoisesti. Muokkaa aiemmin luotua indeksiä valitsemalla **Muokkaa** tai **Lisää** kyseisen indeksin kohdalla. Luo uusi indeksijoukko valitsemalla **Uusi indeksijoukko**. Tee indeksijoukon kunkin rivin **Dimensio**-kentässä valinta perusdimensioluettelossa. Seuraavien kenttien arvot luodaan automaattisesti:

    - **Joukon numero** – samaan ryhmään (indeksiin) kuuluvat dimensiot ryhmitellään yhteen ja niille määritetään sama joukon numero.
    - **Hierarkia** – Hierarkia parantaa tiettyjen dimensioyhdistelmien suorituskykyä suodatus- ja ryhmittelykyselyparametreissa.

> [!TIP]
> Seuraavassa on muutamia vinkkejä, jotka on hyvä pitää mielessä, kun määrität indeksihierarkiaa:
>
> - Osiomäärityksessä määritettyjä perusdimensioita ei saa määrittää indeksimäärityksissä. Jos indeksikonfiguraatiossa on määritetty uudelleen perusdimensio, tällä indeksillä ei voi tehdä kyselyä.
> - Jos sinun tarvitsee kysellä vain varastoa, joka koostetaan kaikkien dimensioyhdistelmien perusteella, voit määrittää yksittäisen hakemiston, joka sisältää perusdimension `Empty`.

### <a name="example"></a>Esimerkki

Tämän osan esimerkki näyttää, miten hierarkia toimii.

Seuraavassa taulukossa on luettelo tässä esimerkissä käytettävissä olevasta varastosta.

| Nimike | ColorId | SizeId | StyleId | Määrä |
|---|---|---|---|---|
| D0002 | Musta | Pieni | Leveä | 1 |
| D0002 | Musta | Pieni | Säännöllinen | 2 |
| D0002 | Musta | Suuri | Leveä | 3 |
| D0002 | Musta | Suuri | Säännöllinen | 4 |
| D0002 | Punainen | Pieni | Leveä | 5 |
| D0002 | Punainen | Pieni | Säännöllinen | 6 |
| D0002 | Punainen | Suuri | Säännöllinen | 7 |

Seuraavassa taulukko näyttää, miten indeksihierarkia määritetään.

| Joukon numero | Dimensio | Hierarkia |
|---|---|---|
| 1 | `ColorId` | 1 |
| 1 | `SizeId` | 2 |
| 1 | `StyleId` | 3 |

Indeksin antaa mahdollisuuden tehdä kyselyjä käytettävissä olevassa varastossa seuraavin tavoin:

- `()` – ryhmittely kaikkien perusteella.

    - D0002, 28

- `(ColorId)` – ryhmittelyperusteena `ColorId`

    - D0002, musta, 10
    - D0002, punainen, 18

- `(ColorId, SizeId)` – ryhmittelyperusteena `ColorId`- ja `SizeId`-yhdistelmä

    - D0002, musta, S, 3
    - D0002, musta, L, 7
    - D0002, punainen, S, 11
    - D0002, punainen, L, 7

- `(ColorId, SizeId, StyleId)` – ryhmittelyperusteena `ColorId`-, `SizeId`- ja `StyleId`-yhdistelmä

    - D0002, musta, S, leveä, 1
    - D0002, musta, S, normaali, 2
    - D0002, musta, L, leveä, 3
    - D0002, musta, L, normaali, 4
    - D0002, punainen, S, leveä, 5
    - D0002, punainen, S, normaali, 6
    - D0002, punainen, L, normaali, 7

## <a name="reservation-configuration-optional"></a><a name="reservation-configuration"></a>Varausmääritykset (valinnainen)

Varausmääritys on välttämätön, jos alustavaa varaustoimintoa halutaan käyttää. Määrityksessä on kaksi keskeistä osaa:

- Alustavan varauksen yhdistämismääritys
- Alustavan varauksen hierarkia

### <a name="soft-reservation-mapping"></a>Alustavan varauksen yhdistämismääritys

Varausta tehtäessä halutaan ehkä tietää, riittääkö käytettävissä oleva varasto varaukseen. Vahvistus on linkitetty laskennalliseen mittaan, joka ilmaistaan fyysisten mittojen yhdistelmän laskentakaavana.

Kun yhdistämismääritys määritetään fyysisestä mitasta laskennalliseen mittaan, varaston näkyvyyspalvelu voi tarkistaa automaattisesti varauksen saatavuuden fyysisen mitan perusteella.

Ennen kuin tämä yhdistämismääritys voidaan määrittää, fyysiset mitat, laskennalliset mitat ja niiden tietolähteet on määritettävä Power Appsin **Määritys**-sivun **Tietolähde**- ja **Laskennallinen mitta** -välilehdissä (aiemmin tässä artikkelissa kuvatulla tavalla).

Alustavan varauksen yhdistämismääritys määritetään seuraavasti:

1. Määritä alustavana varausmittana toimiva fyysinen mitta (esimerkki: `SoftReservPhysical`).
1. Määritä **Määritys**-sivun **Laskennallinen mitta** -välilehdessä laskennallinen *käytettävissä varaukseen* -mitta, jonka sisältämä laskentakaava halutaan yhdistää fyysiseen mittaan. Esimerkiksi `AvailableToReserve` (käytettävissä varaukseen) voidaan määrittää siten, että se yhdistetään aiemmin määritettyyn fyysiseen `SoftReservPhysical` -mittaan. Tällä tavoin voidaan etsiä, mitkä sellaiset määrät ovat käytettävissä varaukseen, joiden varaston tila on `SoftReservPhysical`. Seuraavassa taulukossa on laskentakaava varaukseen käytettävissä olevasta varastosta.

    | Laskentalaji | Tietolähde | Fyysinen mitta |
    |---|---|---|
    | Lisäys | `fno` | `AvailPhysical` |
    | Lisäys | `pos` | `Inbound` |
    | Vähennyslasku | `pos` | `Outbound` |
    | Vähennyslasku | `iv` | `SoftReservPhysical` |

    On suositeltavaa määrittää laskennallinen mitta niin, että se sisältää fyysisen mitan, jolle varausmitta perustuu. Tällöin varausmitan määrä vaikuttaa laskennallisen mitan määrään. Siksi tässä esimerkissä `iv`-tietolähteen laskinnallisen mitan `AvailableToReserve` pitäisi sisältää komponenttina `iv`-tietolähteen fyysinen mitta `SoftReservPhysical`.

1. Avaa **Määritykset**-sivu.
1. Määritä **Alustavan varauksen yhdistämismääritys** -välilehdessä yhdistämismääritys fyysisestä mitasta laskennalliseen mittaan. Edellisessä esimerkissä `AvailableToReserve` voidaan yhdistää aiemmin määritettyyn fyysiseen `SoftReservPhysical`-mittaan seuraavien asetusten avulla:

    | Fyysisen mitan tietolähde | Fyysinen mitta | Varaukseen käytettävissä olevan tietolähde | Varaukseen käytettävissä oleva laskennallinen mitta |
    |---|---|---|---|
    | `iv` | `SoftReservPhysical` | `iv` | `AvailableToReserve` |

    > [!NOTE]
    > Jos et voi muokata **Alustavan varauksen yhdistämismääritys** -välilehteä, voi olla tarpeen ottaa *OnHandReservation*-ominaisuus käyttöön **Ominaisuuksien hallinta** -välilehdessä.

Kun `SoftReservPhysical`-varaus nyt tehdään, varaston näkyvyyssovellus etsii automaattisesti `AvailableToReserve`-mitan ja siihen liittyvän laskentakaavan varauksen vahvistusta varten.

Varaston näkyvyyssovelluksessa on esimerkiksi seuraava käytettävissä oleva varasto.

```json
{
    "productId": "D0002",
    "dimensions": {
        "SiteId": "1",
        "LocationId": "11",
        "ColorId": "Red"
    },
    "quantities": {
        "iv": {
            "SoftReservPhysical": 90
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

`AvailableToReserve` = `fno.availphysical` + `pos.inbound` – `pos.outbound` – `iv.SoftReservPhysical`  
=70+50–20–90  
=10

Jos siis kohteen `iv.SoftReservPhysical` varauksia yritetään tehdä ja jos määrä on pienempi tai yhtä suuri kuin `AvailableToReserve` (10), alustavan varauksen pyyntö onnistuu.

> [!NOTE]
> Kun kutsut varausten ohjelmointirajapintaa, voit ohjata varausten vahvistamista määrittämällä `ifCheckAvailForReserv`-totuusarvoparametrin pyynnön tekstiosassa. Arvo `True` tarkoittaa, että tarkistus on pakollinen. Arvo `False` tarkoittaa, että tarkistus ei ole pakollinen (vaikka saatat saada negatiivisen kohteen `AvailableToReserve` määrän, järjestelmä sallii silti alustavan varauksen). Oletusarvona on `True`.

### <a name="soft-reservation-hierarchy"></a>Alustavan varauksen hierarkia

Varaushierarkia ilmaisee dimensiojärjestyksen, joka on määritettävä varauksia tehtäessä. Se toimii samalla tavoin kuin tuoteindeksihierarkia käytettävissä olevaa varastoa koskevissa kyselyissä.

Varaushierarkia on erillään tuoteindeksihierarkiasta. Tämä erillisyys antaa mahdollisuuden toteuttaa sellainen luokanhallinta, jossa käyttäjät voivat eritellä dimensiot vaatimukset määrittäviksi tiedoiksi. Tämä puolestaan antaa mahdollisuuden entistä tarkempiin varauksiin. Alustavan varauksen historian pitäisi sisältää tunnukset `SiteId` ja `LocationId` komponentteina, koska ne muodostavat osionmäärityksen. Kun teet varauksen, sinun on määritettävä tuotteelle osio.

Esimerkki alustavan varauksen hierarkiasta.

| Perusdimensio | Hierarkia |
|---|---|
| `SiteId` | 1 |
| `LocationId` | 2 |
| `ColorId` | 3 |
| `SizeId` | 4 |
| `StyleId` | 5 |

Tässä esimerkissä varaus voidaan tehdä seuraavissa dimensiojärjestyksissä. Sinun on määritettävä tuotteelle osio, kun teet varauksen. Siksi perushierarkia, jota voit käyttää, on `(SiteId, LocationId)`.

- `(SiteId, LocationId)`
- `(SiteId, LocationId, ColorId)`
- `(SiteId, LocationId, ColorId, SizeId)`
- `(SiteId, LocationId, ColorId, SizeId, StyleId)`

Kelvollisen dimensiojärjestyksen on noudatettava varaushierarkiaa tarkasti dimensio kerrallaan. Esimerkiksi hierarkiajärjestys `(SiteId, LocationId, SizeId)` ei kelpaa, koska `ColorId` puuttuu.

## <a name="available-to-promise-configuration-optional"></a>Luvattavissa oleva konfiguraatio (valinnainen)

Voit määrittää varaston näkyvyyden sallimaan tulevien käytettävissä olevien muutosten ajoituksen ja luvattavissa olevien (ATP)määrien laskemisen. ATP on tuotteen määrä, joka on saatavilla ja joka voidaan luvata asiakkaalle seuraavalla kaudella. Tämän laskelman käyttö voi lisätä tilauksen täyttämiskykyä merkittävästi. Jotta tätä toimintoa voi käyttää, se on otettava käyttöön **ominaisuuksien hallinta** -välilehdessä ja määritettävä sen asetukset **ATP-asetus**-välilehdissä. Lisätietoja on kohdassa [Varaston näkyvyys - käytettävissä olevan varaston muutosaikataulut ja luvattavissa oleva määrä](inventory-visibility-available-to-promise.md).

## <a name="turn-on-and-configure-preloaded-on-hand-queries-optional"></a><a name="query-preload-configuration"></a>Valmiiksi ladattujen käytettävissä olevan varaston kyselyjen ottaminen käyttöön ja määrittäminen (valinnainen)

Varaston näkyvyys voi noutaa ja tallentaa säännöllisesti käytettävissä olevan varaston yhteenvetotiedot valmiiksi määritettyjen dimensioiden perusteella. Näin saadaan seuraavat edut:

- Selkeä näkymä, johon tallennettava varastoyhteenveto sisältää vain päivittäiseen liiketoimintaan liittyvät dimensiot.
- Varastoyhteenveto on yhteensopiva sellaisten nimikkeiden kanssa, joissa on otettu käyttöön varastonhallintaprosessit.

Lisätietoja tämän ominaisuuden käyttämisestä sen jälkeen, kun se on määritetty, on kohdassa [Käytettävissä olevan varaston virtaviivaistetun kyselyn esilataaminen](inventory-visibility-power-platform.md#preload-streamlined-onhand-query).

> [!IMPORTANT]
> On suositeltavaa käyttää joko *OnHandIndexQueryPreloadBackgroundService*- tai *OnHandMostSpecificBackgroundService*-ominaisuutta mutta ei molempia. Molempien ominaisuuksien ottaminen käyttää vaikuttaa suorituskykyyn.

Määritä ominaisuus seuraavasti:

1. Kirjaudu varaston näkyvyyden Power App -sovellukseen.
1. Valitse **Määritys \> Ominaisuuksien hallinta ja asetukset**.
1. Jos *OnHandIndexQueryPreloadBackgroundService*-ominaisuus on otettu jo käyttöön, se kannattaa poistaa käytöstä nyt, koska puhdistamisprosessin valmistuminen voi kestää erittäin kauan. Se voidaan ottaa uudelleen käyttöön myöhemmin tässä menettelyssä.
1. Avaa **Esilatausasetus**-välilehti.
1. Valitse **Vaihe 1: Esilatauksen tallennustilan tyhjentäminen** -osassa **Tyhjennä**. Tämä asetus tyhjentää tietokannan ja valmistelee sen hyväksymään uudet ryhmittelyasetukset.
1. Syötä **Vaihe 2: arvoihin perustuvan ryhmittelyn määrittäminen** -osan **Tulosten ryhmittelyperuste** -kenttään pilkuin eroteltu luettelo kentän nimistä, joiden perusteella kyselyn tulokset ryhmitellään. Tätä asetusta ei voi muuttaa sen jälkeen, kun esiladatussa tallennustietokannassa on tietoja, muutoin kuin tyhjentämällä tietokannan edellisessä vaiheessa kuvatulla tavalla.
1. Valitse **Määritys \> Ominaisuuksien hallinta ja asetukset**.
1. *OnHandIndexQueryPreloadBackgroundService*-ominaisuus käyttöön.
1. Hyväksy muutokset valitsemalla **Päivitä määritys** **Määritys**-sivun oikeassa yläkulmassa.

## <a name="complete-and-update-the-configuration"></a>Määrityksen viimeisteleminen ja päivittäminen

Kun määritys on valmis, kaikki muutokset on vahvistettava varaston näkyvyyssovellukseen. Ota muutokset käyttöön alla olevien ohjeiden avulla.

1. Valitse Power Appsin **Määritys**-sivun oikeassa yläkulmassa **Päivitä määritys**. 
1. Järjestelmä pyytää antamaan kirjautumisen tunnistetiedot. Syötä seuraavat arvot:

    - **Asiakastunnus** – varaston näkyvyyssovellukselle luotu Azure-sovelluksen tunnus.
    - **Vuokraajan tunnus** – Azure-vuokraajan tunnus.
    - **Asiakasohjelman salasana** – varaston näkyvyyssovellukselle luotu Azure-sovelluksen tunnus.

    Lisätietoja näistä tunnistetiedoista ja niiden löytämisestä on kohdassa [Inventory Visibilityn asentaminen ja määrittäminen](inventory-visibility-setup.md).

    > [!IMPORTANT]
    > Tietolähteen nimi, fyysiset mitat ja dimensioiden yhdistämismääritykset on tarkistettava ennen määrityksen päivittämistä. Näitä asetuksia ei voi muokata päivittämisen jälkeen.

1. Valitse sisäänkirjautumisen jälkeen uudelleen **Päivitä määritys**. Järjestelmä ottaa asetukset käyttöön ja näyttää muuttuneet tiedot.

## <a name="default-configuration-sample"></a><a name="default-configuration-sample"></a>Oletusmääritysnäyte

Varaston näkyvyys määrittää alustuksen aikana oletusmäärityksen, joka esitellään tässä. Määritystä voi muokata tarpeen mukaan.

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

- `Arrived`
- `PhysicalInvent`
- `ReservPhysical`
- `onorder`
- `notspecified`
- `availordered`
- `availphysical`
- `picked`
- `postedqty`
- `quotationreceipt`
- `received`
- `ordered`
- `ReservOrdered`

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
| Vähennys | `pos` | `PosOutbound` |

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

Seuraavassa taulukossa on varauksen oletusarvoinen yhdistämismääritys.

| Fyysisen mitan tietolähde | Fyysinen mitta | Varaukseen käytettävissä olevan tietolähde | Varaukseen käytettävissä oleva laskennallinen mitta |
|---|---|---|---|
| `iv` | `SoftReservPhysical` | `iv` | `AvailableToReserve` |

#### <a name="reservation-hierarchy"></a>Varaushierarkia

Seuraavassa taulukossa on varauksen oletushierarkia.

| Perusdimensio | Hierarkia |
|---|---|
| `SiteId` | 1 |
| `LocationId` | 2 |
| `ColorId` | 3 |
| `SizeId` | 4 |

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
