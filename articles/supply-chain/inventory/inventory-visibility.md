---
title: Varaston näkyvyyden apuohjelma
description: Tässä aiheessa käsitellään Dynamics 365 Supply Chain Managementin varaston näkyvyyden apuohjelman asentamista ja määrittämistä.
author: chuzheng
manager: tfehr
ms.date: 10/26/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2020-10-26
ms.dyn365.ops.version: Release 10.0.15
ms.openlocfilehash: 2976153a6a7e4b4130e8f7673ed128945aeabf65
ms.sourcegitcommit: 03c2e1717b31e4c17ee7bb9004d2ba8cf379a036
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/24/2020
ms.locfileid: "4625062"
---
# <a name="inventory-visibility-add-in"></a>Varaston näkyvyyden apuohjelma

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Varaston näkyvyyden apuohjelma on itsenäinen ja erittäin skaalautuva mikropalvelu, joka mahdollistaa reaaliaikaisen käytettävissä olevan varaston seurannan ja antaa tällä tavoin yleisen näkymän varaston näkyvyyteen.

Kaikki käytettävissä olevaan varastoon liittyvät tiedot viedään palveluun lähes reaaliaikaisesti käyttämällä matala-asteista SQL-integraatiota. Ulkoiset palvelut käyttävät palvelut tekevät RESTful API -ohjelmointirajapinnoilla käytettävissä olevien tietojen kyselyjä annetuissa dimensioissa ja saavat tällä tavoin luettelon käytettävissä olevista paikoista.

Varastoin näkyvyys on Common Data Serviceen perustuva mikropalvelu, joten sitä voi laajentaa muodostamalla Power Apps -sovelluksia ja käyttämällä Power BI:ta tuottamaan liiketoiminnan tarpeita vastaavia mukautettuja toimintoja. Indeksi voidaan lisäksi päivittää tekemään varastokyselyjä.

Varaston näkyvyydessä on määritysvaihtoehtoja, joiden avulla sen voi integroida useiden kolmannen osapuolen järjestelmien kanssa. Se tukee standardoitua varastodimensiota, mukautettua laajennettavuutta ja standardoituja, määritettäviä laskettuja määriä.

Tässä aiheessa käsitellään Dynamics 365 Supply Chain Managementin varaston näkyvyyden apuohjelman asentamista ja määrittämistä sekä sen ohjelmointirajapinnan käyttöä.

## <a name="install-the-inventory-visibility-add-in"></a>Varaston näkyvyyden lisäapuohjelman asentaminen

Varaston näkyvyyden lisäapuohjelman asentamiseen on käytettävä Microsoft Dynamics Lifecycle Servicesiä (LCS). LCS on yhteistyöportaali, jonka muodostamassa ympäristössä ja jonka säännöllisesti päivitetyillä palveluilla voi hallita Dynamics 365 Finance and Operations -sovellusten elinkaarta.

Lisätietoja on kohdassa [Lifecycle Services -resurssit](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/lifecycle-services/lcs).

### <a name="prerequisites"></a>Edellytykset

Ennen varaston näkyvyyden apuohjelman asentamista:

- Hanki LCS-toteutusprojekti, jossa on otettu käyttöön vähintään yksi ympäristö.
- Luo tarjoomalle beeta-avaimet LCS:ssa.
- Ota tarjooman beeta-avaimet käyttöön käyttäjälle LCS:ssa.
- Ota yhteys Microsoftin varaston näkyvyyden tuotetiimiin and ympäristötunnus, jossa haluat ottaa varaston näkyvyyden apuohjelman käyttöön.

Jos sinulla on näitä edellytyksiä koskevia kysymyksiä, ota yhteys varaston näkyvyyden tuotetiimiin.

### <a name="install-the-add-in"></a><a name="install-add-in"></a>Lisäosan asentaminen

Varaston näkyvyyden apuohjelman asentaminen:

1. Kirjaudu [Lifecycle Services (LCS)](https://lcs.dynamics.com/Logon/Index) -portaaliin.
1. Valitse aloitussivulla projekti, jossa ympäristö on otettu käyttöön.
1. Valitse projektisivulla ympäristö, johon haluat asentaa apuohjelman.
1. Vieritä ympäristösivulla **Ympäristöapuohjelmat** -osaan. Jos osa ei ole näkyvissä, varmista, että edellytyksissä mainitut beeta-avaimet on käsitelty kokonaisuudessaan.
1. Valitse **Ympäristöapuohjelmat**-osassa **Asenna uusi apuohjelma**.
    ![Ympäristösivu LCS:ssa](media/inventory-visibility-environment.png "Ympäristösivu LCS:ssa")
1. Valitse **Asenna uusi apuohjelma** -linkki. Käytettävissä olevien apuohjelmien luettelo avautuu.
1. Valitse luettelossa **Varastopalvelu**. (Huomaa, että sen nimi voi olla nyt **Dynamics 365 Supply Chain Managementin varaston näkyvyyden apuohjelma**.)
1. Anna arvot seuraavissa ympäristön kentissä:

    - **AAD-sovelluksen tunnus**
    - **AAD-vuokraajan tunnus**

    ![Apuohjelman määrityssivu](media/inventory-visibility-setup.png "Apuohjelman määrityssivu")

1. Hyväksy käyttöehdot valitsemalla **Käyttöehdot**-valintaruutu.
1. Valitse **Asenna**. Apuohjelman tilana näkyy nyt **Asennetaan**. Se on valmis, päivitä sivu, jonka jälkeen tilana on **Asennettu**.

### <a name="get-a-security-service-token"></a>Palvelun suojaustunnuksen hankkiminen

Palvelun suojaustunnus haetaan seuraavasti:

1. Hanki `aadToken` ja tee päätepistekutsu: https://securityservice.operations365.dynamics.com/token.
1. Korvaa `client_assertion` tekstiosassa omalla `aadToken`-tunnuksella.
1. Vaihda tekstiosan kontekstin tilalle ympäristö, jossa haluat ottaa apuohjelman käyttöön.
1. Vaihda vaikutusalue tekstiosassa seuraavasti:

    - MCK-vaikutusalue – https://inventoryservice.operations365.dynamics.cn/.default  
    (Azure Active Directory -sovelluksen tunnus ja MCK-vuokraajan tunnus ovat kohdassa `appsettings.mck.json`.)
    - PROD-vaikutusalue – https://inventoryservice.operations365.dynamics.com/.default  
    (Azure Active Directory -sovelluksen tunnus ja PROD-vuokraajan tunnus ovat kohdassa `appsettings.prod.json`.)

    Tuloksen pitäisi muistuttaa seuraavaa esimerkkiä:

    ```json
    {
        "grant_type": "client_credentials",
        "client_assertion_type":"aad_app",
        "client_assertion": "{**Your_AADToken**}",
        "scope":"**https://inventoryservice.operations365.dynamics.com/.default**",
        "context": "**5dbf6cc8-255e-4de2-8a25-2101cd5649b4**",
        "context_type": "finops-env"
    }
    ```

1. `access_token` saadaan vastauksessa. Sitä tarvitaan haltijatunnuksena, jolla varastoin näkyvyyden ohjelmointirajapintaa kutsutaan. Esimerkki:

    ```json
    {
        "access_token": "{Returned_Token}",
        "token_type": "bearer",
        "expires_in": 1200
    }
    ```

### <a name="uninstall-the-add-in"></a>Lisäosan asennuksen poistaminen

Poista apuohjelman asennus valitsemalla **Poista asennus**. Päivitä LCS, ja varaston näkyvyyden apuohjelma poistetaan. Asennuksen poistoprosessi poistaa apuohjelman rekisteröinnin sekä käynnistää kaikkien palveluun tallennettujen liiketoimintatietojen puhdistustyön.

## <a name="inventory-visibility-add-in-public-api"></a>Varaston näkyvyyden apuohjelman julkinen ohjelmointirajapinta

Varaston näkyvyyden apuohjelman julkinen REST API sisältää useita nimenomaisia integroinnin päätepisteitä. Se tukee kolmea pääasiallista vuorovaikutustyyppiä:

- Varastosaldon määrän muutosten kirjaaminen apuohjelmaan ulkoisesta järjestelmästä.
- Nykyisten käytettävissä olevien määrien kysely ulkoisesta järjestelmästä.
- Automaattinen synkronointi Supply Chain Managementin käytettävissä olevan varaston kanssa.

Automaattinen synkronointi ei sisälly julkiseen ohjelmointirajapintaan, vaan se käsitellään taustalla ympäristöissä, joissa varaston näkyvyyden apuohjelma on otettu käyttöön.

### <a name="authentication"></a>Todennus

Ympäristön suojaustunnusta käytetään varaston näkyvyyden apuohjelman kutsumiseen, joten Azure Active Directory -tunnus on luotava Azure Active Directory -sovelluksessa.

Lisätietoja suojaustunnuksen hakemista on kohdassa [Varaston näkyvyyden apuohjelman asentaminen](#install-add-in).

### <a name="configure-the-inventory-visibility-api"></a>Varaston näkyvyyden ohjelmointirajapinnan määrittäminen

Ennen palvelun käyttöä on tehtävä valmiiksi seuraavissa aliosissa käsiteltävät määritykset. Määritykset voivat vaihdella ympäristön tietojen mukaan. Siinä pääasiallisesti neljä osaa:

- [Osiointi](#partitioning)
- [Dimensiomääritykset](#dimension-configurations)
- [Indeksointi](#indexing)
- [Mukautettu mitta](#custom-measurement)

#### <a name="partitioning"></a>Osiointi

Osiointi voi vaikuttaa merkittävästi varaston näkyvyyden ohjelmointirajapinnan toimintaan. Niinpä kannattaakin määrittää rakenne, jossa voidaan ryhmitellä tietoja pienissä osissa siten, että merkitykselliset tietokyselyt ovat mahdollisia.

`organizationId` (Supply Chain Managementissa `dataAreaId`) sisältyy aina osiointiin, ja varaston näkyvyys osioidaan oletusarvoisesti dimensioiden perusteella, kuten *Toimipaikka + sijainti*. Tämän vuoksi palveluissa tehtävissä kyselyissä on aina käytettävä suodattimissa määritettyjä dimensioita.

> [!NOTE]
> *Toimipaikka* ja *sijainti* ovat kaksi varaston näkyvyyden yleistä oletusdimensiota. Supply Chain Managementin näiden dimensioiden nimet ovat *toimipaikka* (`InventSiteId`) ja *varasto* (`InventLocationId`)

### <a name="dimension-configurations"></a>Dimensiomääritykset

Varaston näkyvyyden yleisten oletusdimensioiden luettelon ansiosta usein lähdejärjestelmien integrointi on mahdollista.

Seuraavassa taulukossa on varastodimensiot, jotka tulevat varaston näkyvyyden oletusdimensionimiksi.

| Dimensiotyyppi | Dimension nimi |
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

> [!NOTE]
> Edellisessä taulukossa mainittu dimensiotyyppi on tarkoitettu vain tiedoksi. Dimensiotyyppiä ei tarvitse määrittää varaston näkyvyydessä.

Jos mukautettu dimensio on luotu ja sen on siirryttävä oletusarvoon, kun varaston näkyvyys käyttää sitä, **mukautetun dimension** nimi voidaan määrittää varaston näkyvyydessä.

Ulkoiset järjestelmät käyttävät varaston näkyvyyttä RESTful API -ohjelmointirajapinnoilla, jotka ottavat käytettävissä olevat tiedot käyttöön annetuissa dimensiojoukoissa, joissa kyselyt tehdään. Integroinnin osalta varaston näkyvyydessä voidaan määrittää *ulkoinen kanavan tietolähde* ja *kohdedimensioiden* lähdedimensio varaston näkyvyydessä.

Kohdedimensioiden on oltava jokin seuraavista:

- Varaston näkyvyyden oletusdimensiot
- Mukautetut dimensiot

Dimensiomääritysten tarkoitus on standardoida monen järjestelmän integrointi dimensiokyselyitä ja tapahtuman dimensioihin kirjaamista varten.

#### <a name="indexing"></a>Indeksointi

Käytettävissä olevan varaston kysely ei ole useimmiten korkeimmalla kokonaistasolla, vaan tulokset halutaan ehkä nähdä varastodimensioiden mukaan koostettuina.

Varaston näkyvyys on joustava, sillä siinä voidaan määrittää dimensioon tai dimensioyhdistelmiin perustuvia indeksejä.

> [!NOTE]
> Tällä hetkellä indeksejä voi määrittään enintään viisi. Käytettävää dimensiota tai dimensioyhdistelmää on harkittava huolellisesti ennen toteutusta, sillä näin voidaan varmistaa, että se todella vastaa liiketoiminnan tarpeita. Tuotekysely voidaan haluta tehdä esimerkiksi seuraavasti:

- Kyselynä käytettävissä oleva koostetuote *väri*- ja *koko*-dimension mukaan.
- Joissakin tapauksissa kyselyn kohteena voi olla tuote kokonaisuudessaan.

Kaksi indeksiä määritetään seuraavasti:

- `["ColorId", "SizeId"]`
- `[]`

Tyhjä hakasulje tekee koosteen osiossa olevan tuotetunnuksen perusteella.

Indeksointi määrittää, miten tulokset ryhmitellään `groupBy`-kyselyasetuksen perusteella. Jos tässä tapauksessa ei määritetä `groupBy`-arvoja, tuloksena on `productid`-kohtainen kokonaismäärä. Jos `groupBy`-määrityksenä on sen sijaan `groupBy=ColorId&groupBy=SizeId`, tuloksena on useita rivejä, jotka perustuvat järjestelmässä oleviin väri- ja kokoyhdistelmiin.

Kyselyehdot voidaan asettaa pyynnön tekstiosaan.

Seuraavassa esimerkissä on väri- ja kokoyhdistelmää käyttävä tuotekysely.

```json
{
    "filters": {
        "OrganizationId": ["usmf"],
        "ProductId": ["MyProduct"],
        "LocationId": ["21"],
        "SiteId": ["2"],
        "ColorId": ["Red"]
    },
    "groupByValues": [
        "SizeId",
        "ColorId"
    ],
    "returnNegative": true
}
```

#### <a name="custom-measurement"></a>Mukautettu mitta

Vaikka oletusarvoiset mittamäärät linkitetään Supply Chain Managementiin, myös oletusmittamäärien yhdistelmistä koostuva määrä on mahdollinen. Sitä varten on määritettävä mukautettuja määritä, jotka lisätään käytettävissä olevan määrän tulosteisiin.

Toiminnon antaa yksinkertaisesti mahdollisuuden määrittää lisättävän ja/tai vähennettävän mittajoukon, joiden avulla voidaan muodostaa mukautettu mitta.

Esimerkiksi seuraavalla kyselyehdolla määritetään mukautetun mitan määräksi `MyCustomAvailableforReservation`, jonka kulutusjärjestelmä käyttää.

```json
[
    {
        "productId": "MyProduct",
        "dimensions": {
            "colorid": "Red"
        },
        "quantities": {
            "mypos": {
                "outbound": 20.0,
                "inbound": 80.0
            },
            "fno": {
                "availphysical": 100.0,
                "orderedintotal": 50.0,
                "orderedreserved": 10.0
            },
            "exterchannel": {
                "received": 90.0,
                "scheduled": 30.0,
                "issued": 60.0,
                "reserved": 40.0
            }
        }
    }
]

```



| Kulutusjärjestelmä | Lasketut mitat | Tietolähde | Määre | Määreen laskentatyyppi |
|---|---|---|---|---|
| `CustomChannel` | `MyCustomAvailableforReservation` | `fno` | `availphysical` | Lisäys |
| `CustomChannel` | `MyCustomAvailableforReservation` | `fno` | `orderedintotal` | Lisäys |
| `CustomChannel` | `MyCustomAvailableforReservation` | `fno` | `orderedreserved` | Vähennyslasku |
| `CustomChannel` | `MyCustomAvailableforReservation` | `mypos` | `inbound` | Lisäys |
| `CustomChannel` | `MyCustomAvailableforReservation` | `mypos` | `outbound` | Vähennyslasku |
| `CustomChannel` | `MyCustomAvailableforReservation` | `exterchannel` | `received` | Lisäys |
| `CustomChannel` | `MyCustomAvailableforReservation` | `exterchannel` | `scheduled` | Lisäys |
| `CustomChannel` | `MyCustomAvailableforReservation` | `exterchannel` | `issued` | Vähennyslasku |
| `CustomChannel` | `MyCustomAvailableforReservation` | `exterchannel` | `reserved` | Vähennyslasku |

Mukautetun mittamäärän kysely palauttaa sitten seuraavan tuloksen.

```json
[
    {
        "productId": "MyProduct",
        "dimensions": {
            "colorid": "Red"
        },
        "quantities": {
            "mypos": {
                "outbound": 20.0,
                "inbound": 80.0
            },
            "fno": {
                "availphysical": 100.0,
                "orderedintotal": 50.0,
                "orderedreserved": 10.0
            },
            "exterchannel": {
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

`MyCustomAvailableforReservation`-tulos perustuu seuraavaan mukautettujen mittojen laskenta-asetukseen:  
 *100 + 50 + 80 + 90 + 30 &ndash; 10 &ndash; 20 &ndash; 60 &ndash; 40 = 220*

### <a name="posting-on-hand-changes"></a>Varastosaldon muutosten kirjaaminen

Tarkka URL-osoite, johon tapahtuma kirjataan, määräytyy maantieteellisen alueen mukaan. Sen muoto on seuraava:

`https://{serviceURL}/api/environment/{environmentId}/onhand`

Tätä URL-osoitetta käytetään todennuksessa HTTP `POST` -menetelmän ohella lähettämään varastosaldon muutostapahtumat palveluun.

Dynamics 365 -palvelun kanssa HTTP-pyyntöjen avulla tapahtuvassa viestinnässä käytetään erityisotsikko, joka ilmaisee sen Supply Chain Management -esiintymän ympäristötunnuksen, johon tiedot on linkitetty. Esimerkki:

`x-ms-environment-id: 2db79622-f97a-4d64-9844-d12efed41796`

#### <a name="posting-on-hand-changes-query-example-1"></a>Varastosaldon muutosten kirjaamisen kyselyesimerkki 1

Tässä esimerkissä on skenaario, jossa dimensiomääritys määritetään Power Appsissa.

Määritä dimension yhdistämismääritys Power Appsissa käyttämällä seuraavaa kyselyä:

```json
{
    "PosSizeId": "SizeId",
    "PosColorId": "ColorId",
    "PosSiteId": "SiteId",
    "PosLocationId": "LocationId"
}
```

Voit nyt tehdä `dimensionDataSource`-määrityksen ja käyttää mukautettuja dimensioita kyselyissä. Järjestelmä muuntaa mukautetut dimensiot automaattisesti perusdimensioiksi.

```json
{
    "id": "demo-test-00007",
    "organizationId": "usmf",
    "productId": "MyProduct",
    "quantities": {
        "pos": {
            "Outbound": 1
        }
    },
    "dimensionDataSource": "pos",
    "dimensions": {
        "PosSizeId": "Large",
        "PosColorId": "Red",
        "PosSiteId": "2",
        "PosLocationId": "21"
    }
}
```

#### <a name="posting-on-hand-changes-query-example-2"></a>Varastosaldon muutosten kirjaamisen kyselyesimerkki 2

Tässä esimerkissä on skenaario, jossa yhtään dimensiomäärityksen yhdistämismääritystä ei määritetä Power Appsissa, joten myös kirjaamisessa on käytettävä perusdimensioita. Kaikkien dimensioiden on oltava perusdimensioita, kun `dimensionDataSource`-kentässä on tyhjäarvo, se on tyhjä tai siinä on välilyönti.

```json
{
    "id": "demo-test-00007",
    "organizationId": "usmf",
    "productId": "MyProduct",
    "quantities": {
        "pos": {
            "Outbound": 1
        }
    },
    "dimensions": {
        "SizeId": "Large",
        "ColorId": "Red",
        "SiteId": "2",
        "LocationId": "21"
    }
}
```

#### <a name="json-document-field-properties"></a>JSON-tiedostokentän ominaisuudet

Aiemmin käsitellyissä JSON-kyselyesimerkkien kentissä oli seuraavassa taulukossa olevia ominaisuuksia.

| Kentän tunnus | kuvaus |
|---|---|
| `id` | Tietyn muutostapahtuman yksilöivä tunnus. Tämän tunnuksen avulla varmistetaan, että jos viestintä palveluun epäonnistuu kirjauksen aikana, tapahtuman lähettäminen uudelleen ei aiheuta saman tapahtuman laskemista kahdesti järjestelmässä. |
| `organizationId` | Tapahtumaan linkitetyn organisaation tunnus. Tämä yhdistetään Supply Chain Management -organisaatioihin tai tietoalueen tunnuksiin. |
| `productId` | Kyseisen tuotteen tunniste. |
| `quantity` | Määrä, jolla varastosaldoa on muutettava. Jos hyllylle esimerkiksi lisättiin 10 uutta sämpylää, tämä arvo 10. Jos 3 sämpylää sitten poistettiin hyllystä tai myyntiin, tämä arvo on -3. |
| `dimensionDataSource` | Muutostapahtuman kirjauksessa ja kyselyssä käytettävien dimensioiden tietolähde. Jos tietolähde määritetään, määritetyn tietolähteen mukautettuja dimensioita voidaan käyttää. Dimensiomääritysten ansiosta varaston näkyvyys voi yhdistää mukautetut dimensiot yleisiin oletusdimensioihin. Jos `dimensionDataSource` ei ole määritetty, kyselyissä voi käyttää vain yleisiä oletusdimensioita.   |
| `dimensions` | Dynaaminen avain- ja arvoparisäilö. Ne yhdistetään joihinkin Supply Chain Managementin dimensioihin, minkä lisäksi voidaan lisätä mukautettuja dimensioita (kuten *Lähde*), jotka voivat ilmaista, saapuuko tapahtuma Supply Chain Managementista vai ulkoisesta järjestelmästä. |

### <a name="querying-current-on-hand"></a>Kyselyt nykyisessä varastosaldossa

Nykyisen varastosaldon kyselyjen päätepisteessä on samankaltainen URL-osoite:

`https://{serviceURL}/api/environment/{environmentId}/onhand/indexquery`

Kysely siinä tehdään HTTP `POST` -menetelmällä.

#### <a name="current-on-hand-query-example-1"></a>Nykyisen varastosaldon kyselyesimerkki 1

Tässä esimerkissä on skenaario, jossa Power Appsissa on jo valmis dimensiomääritys.

Määritä dimension yhdistämismääritys Power Appsissa käyttämällä seuraavaa kyselyä:

```json
{
    "PosSizeId": "SizeId",
    "PosColorId": "ColorId",
    "PosSiteId": "SiteId",
    "PosLocationId": "LocationId"
}
```

Voit nyt tehdä `dimensionDataSource`-määrityksen ja käyttää mukautettuja dimensioita kyselyissä. Järjestelmä muuntaa mukautetut dimensiot automaattisesti perusdimensioiksi. `DimensionDataSource` voidaan määrittää `filters`-kohdassa ja mukautetut dimensiot vodaan määrittää sekä `filters`- että `groupByValues`-kohdissa. Järjestelmä muuntaa mukautetut dimensiot automaattisesti perusdimensioiksi.

```json
{
    "filters": {
        "OrganizationId": ["usmf"],
        "ProductId": ["MyProduct"],
        "DimensionDataSource": ["Pos"],
        "PosLocationId": ["21"],
        "PosSiteId": ["2"],
        "PosColorId": ["Red"]
    },
    "groupByValues": [
        "PosSizeId",
        "PosColorId"
    ],
    "returnNegative": true
}
```

#### <a name="current-on-hand-query-example-2"></a>Nykyisen varastosaldon kyselyesimerkki 2

Tässä esimerkissä on skenaario, jossa yhtään dimensiomäärityksen yhdistämismääritystä ei määritetä Power Appsissa, joten myös kirjaamisessa on käytettävä perusdimensioita. Kaikkien dimensioiden on oltava perusdimensioita, kun `filters`-kohdan `dimensionDataSource`-kentässä on tyhjäarvo, se on tyhjä tai siinä on välilyönti.

```json
{
    "filters": {
        "OrganizationId": ["usmf"],
        "ProductId": ["MyProduct"],
        "LocationId": ["21"],
        "SiteId": ["2"],
        "ColorId": ["Red"]
    },
    "groupByValues": [
        "SizeId",
        "ColorId"
    ],
    "returnNegative": true
}
```

#### <a name="example-return-result"></a>Palautetun tuloksen esimerkki

Edellisten esimerkkien kyselyissä voitiin palauttaa seuraavankaltainen tulos.

```json
[
    {
        "productId": "MyProduct",
        "dimensions": {
            "colorid": "Red"
        },
        "quantities": {
            "mypos": {
                "outbound": 20.0,
                "inbound": 80.0
            },
            "fno": {
                "availphysical": 100.0,
                "orderedintotal": 50.0,
                "orderedreserved": 10.0
            },
            "exterchannel": {
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

Huomaa, että määräkentät on jäsennelty mittahakemistoksi ja niihin liittyviksi arvoiksi.
