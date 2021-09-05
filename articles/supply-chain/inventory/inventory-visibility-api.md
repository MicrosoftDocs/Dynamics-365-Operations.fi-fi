---
title: Varaston näkyvyyden julkiset ohjelmointirajapinnat
description: Tässä aiheessa käsitellään varaston näkyvyyden julkisia ohjelmointirajapintoja.
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
ms.openlocfilehash: 0aca5838ff6d7c9c4d881698be1e2da2e0e1c02e
ms.sourcegitcommit: b9c2798aa994e1526d1c50726f807e6335885e1a
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/13/2021
ms.locfileid: "7343629"
---
# <a name="inventory-visibility-public-apis"></a>Varaston näkyvyyden julkiset ohjelmointirajapinnat

[!include [banner](../includes/banner.md)]
[!INCLUDE [cc-data-platform-banner](../../includes/cc-data-platform-banner.md)]

Tässä aiheessa käsitellään varaston näkyvyyden julkisia ohjelmointirajapintoja.

Varaston näkyvyyden apuohjelman julkinen REST API sisältää useita nimenomaisia integroinnin päätepisteitä. Se tukee neljää pääasiallista vuorovaikutustyyppiä:

- Varastosaldon määrän muutosten kirjaaminen apuohjelmaan ulkoisesta järjestelmästä
- Varastosaldomäärien määrittäminen tai ohittaminen ulkoisesta järjestelmästä apuohjelmassa
- Varaustapahtumien kirjaaminen apuohjelmaan ulkoisesta järjestelmästä
- Nykyisten käytettävissä olevien määrien kysely ulkoisesta järjestelmästä

Seuraavassa taulukossa on tällä hetkellä käytettävissä olevat ohjelmointirajapinnat:

| Polku | Tapa | kuvaus |
|---|---|---|
| /api/environment/{environmentId}/onhand | Kirjaa | [Yhden varastosaldon muutostapahtuman luominen](#create-one-onhand-change-event) |
| /api/environment/{environmentId}/onhand/bulk | Kirjaa | [Useiden muutostapahtumien luominen](#create-multiple-onhand-change-events) |
| /api/environment/{environmentId}/setonhand/{inventorySystem}/bulk | Kirjaa | [Varastosaldomäärien määrittäminen tai ohittaminen](#set-onhand-quantities) |
| /api/environment/{environmentId}/onhand/reserve | Kirjaa | [Yhden varaustapahtuman luominen](#create-one-reservation-event) |
| /api/environment/{environmentId}/onhand/reserve/bulk | Kirjaa | [Useiden varaustapahtumien luominen](#create-multiple-reservation-events) |
| /api/environment/{environmentId}/onhand/indexquery | Hae | [Post-menetelmää käyttävä kysely](#query-with-post-method) |
| /api/environment/{environmentId}/onhand/indexquery | Kirjaa | [Get-menetelmää käyttävä kysely](#query-with-get-method) |

Microsoft on antanut käyttöön *Postman*-pyyntökokoelman. Tämä kokoelma voidaan tuoda *Postman*-ohjelmistoon käyttämällä seuraavaa jaettua linkkiä: <https://www.getpostman.com/collections/90bd57f36a789e1f8d4c>.

## <a name="find-the-endpoint-according-to-your-lifecycle-services-environment"></a>Lifecycle Services -ympäristön mukaisen päätepisteen etsiminen

Varaston näkyvyyden mikropalvelu otetaan käyttöön Microsoft Azure Service Fabricissa useilla maantieteellisillä alueilla ja useilla alueilla. Tällä hetkellä ei ole keskistettyä päätepistettä, joka uudelleenohjaisi pyynnön automaattisesti oikealle maantieteelliselle alueelle ja alueelle. Tämän vuoksi tieto-osista on muodostettava URL-osoite seuraavan mallin mukaisesti:

`https://inventoryservice.<RegionShortName>-il<IsLandNumber>.gateway.prod.island.powerapps.com`

Alueen lyhyen nimi on Microsoft Dynamics Lifecycle Services (LCS) -ympäristössä. Seuraavassa taulukossa on tällä hetkellä käytettävissä olevat alueet.

| Azure-alue | Alueen lyhyt nimi |
|---|---|
| Itä-Australia | eau |
| Kaakkois-Australia | seau |
| Kanada, keskinen | cca |
| Kanada, itäinen | eca |
| Pohjois-Eurooppa | neu |
| Länsi-Eurooppa | weu |
| Itä-Yhdysvallat | eus |
| Länsi-Yhdysvallat | wus |
| Eteläinen Yhdistynyt kuningaskunta | suk |
| Läntinen Yhdistynyt kuningaskunta | wuk |

Saaren numero ilmaisee, missä LCS-ympäristö otetaan käyttöön Service Fabricissa. Tätä tietoa ei voi tällä hetkellä saada millään tavalla käyttäjän puolelta.

Microsoft on muodostanut Power Appsiin käyttöliittymän, jonka avulla saadaan täydellinen mikropalvelun päätepiste. Lisätietoja on kohdassa [Palvelun päätepisteen etsiminen](inventory-visibility-power-platform.md#get-service-endpoint).

## <a name="authentication"></a><a name="inventory-visibility-authentication"></a>Todennus

Varaston näkyvyyden julkisen ohjelmointirajapinnan kutsumiseen käytetään ympäristön suojaustunnusta. Siksi sinun on luotava _Azure Active Directory (Azure AD) -tunnus_ Azure AD -sovelluksen avulla. Tämän jälkeen Azure AD -tunnuksen avulla saat _käyttöoikeustunnuksen_ suojauspalvelusta.

Palvelun suojaustunnus haetaan seuraavasti:

1. Kirjaudu Azure-portaaliin ja etsi sen avulla Dynamics 365 Supply Chain Management -sovelluksen `clientId`- ja `clientSecret`-arvot.
1. Nouda Azure AD -tunnus (`aadToken`) lähettämällä HTTP-pyyntö, jossa on seuraavat ominaisuudet:

    - **URL:** `https://login.microsoftonline.com/${aadTenantId}/oauth2/token`
    - **Menetelmä:** `GET`
    - **Tekstisisältö (lomaketiedot):**

        | Avain | Arvo |
        |---|---|
        | client_id | ${aadAppId} |
        | client_secret | ${aadAppSecret} |
        | grant_type | client_credentials |
        | resurssi | 0cdb527f-a8d1-4bf8-9436-b352c68682b2 |

    Vastauksena pitäisi olla Azure AD -tunnus (`aadToken`). Tarran pitäisi on seuraavan esimerkin kaltainen:

    ```json
    {
        "token_type": "Bearer",
        "expires_in": "3599",
        "ext_expires_in": "3599",
        "expires_on": "1610466645",
        "not_before": "1610462745",
        "resource": "0cdb527f-a8d1-4bf8-9436-b352c68682b2",
        "access_token": "eyJ0eX...8WQ"
    }
    ```

1. Muodosta seuraavaa esimerkkiä muistuttava JavaScript Object Notation (JSON) -pyyntö.

    ```json
    {
        "grant_type": "client_credentials",
        "client_assertion_type": "aad_app",
        "client_assertion": "{Your_AADToken}",
        "scope": "https://inventoryservice.operations365.dynamics.com/.default",
        "context": "5dbf6cc8-255e-4de2-8a25-2101cd5649b4",
        "context_type": "finops-env"
    }
    ```

    Huomaa seuraavat seikat:

    - `client_assertion`-arvon on oltava edellisessä vaiheessa vastaanotettu Azure AD -tunnus (`aadToken`).
    - `context`-arvon on oltava ympäristötunnus, jossa apuohjelma halutaan ottaa käyttöön.
    - Kaikki muut arvot määritetään samoiksi kuin esimerkissä.

1. Lähetä HTTP-pyyntö, jossa on seuraavat ominaisuudet:

    - **URL:** `https://securityservice.operations365.dynamics.com/token`
    - **Menetelmä:** `POST`
    - **HTTP-otsikko:** Ohjelmointirajapinnan versio on sisällytettävä. (Avain on `Api-Version` ja arvo `1.0`.)
    - **Tekstisisältö:** sisällytetään edellisessä vaiheessa luotu JSON-pyyntö.

    Vastauksena pitäisi olla käyttöoikeustietue (`access_token`). Tätä tunnusta on käytettävä haltijatunnuksena, jolla varaston näkyvyyden ohjelmointirajapintaa kutsutaan. Esimerkki:

    ```json
    {
        "access_token": "{Returned_Token}",
        "token_type": "bearer",
        "expires_in": 3600
    }
    ```

Myöhemmissä osissa `$access_token` ilmaisee tunnuksen, joka noudettiin viimeisessä vaiheessa.

## <a name="create-on-hand-change-events"></a><a name="create-onhand-change-event"></a>Varastosaldon muutostapahtumien luominen

Varastosaldon muutostapahtumia luontiin on käytettävissä kaksi ohjelmointirajapintaa:

- Yhden tietueen luonti: `/api/environment/{environmentId}/onhand`
- Useiden tietueiden luonti: `/api/environment/{environmentId}/onhand/bulk`

Seuraavassa taulukossa on yhteenveto JSON-tekstiosan kunkin kentän merkityksestä.

| Kentän tunnus | kuvaus |
|---|---|
| `id` | Tietyn muutostapahtuman yksilöivä tunnus. Tämän tunnuksen avulla varmistetaan, että jos viestintä palveluun epäonnistuu kirjauksen aikana, samaa tapahtumaa ei lasketa järjestelmässä kahdesti, jos se lähetetään uudelleen. |
| `organizationId` | Tapahtumaan linkitetyn organisaation tunniste. Tämä arvo yhdistetään Supply Chain Managementin organisaatioon tai tietoalueen tunnukseen. |
| `productId` | Tuotteen tunniste. |
| `quantities` | Määrä, jolla varastosaldoa on muutettava. Jos hyllylle lisättiin esimerkiksi 10 uutta kirjaa, tämä arvo on `quantities:{ shelf:{ received: 10 }}`. Jos hyllystä poistettiin tai myytiin kolme kirjaa, tämä arvo on `quantities:{ shelf:{ sold: 3 }}`. |
| `dimensionDataSource` | Muutostapahtuman kirjauksessa ja kyselyssä käytettävien dimensioiden tietolähde. Jos tietolähde määritetään, määritetyn tietolähteen mukautettuja dimensioita voidaan käyttää. Varaston näkyvyyssovellus voi käyttää dimensiomääritystä mukautettujen dimensioiden yhdistämiseen yleisiin oletusdimensioihin. Jos `dimensionDataSource`-arvoa ei ole määritetty, kyselyissä voi käyttää vain yleisiä [perusdimensioita](inventory-visibility-configuration.md#data-source-configuration-dimension). |
| `dimensions` | Dynaaminen avain- ja arvopari. Arvot yhdistetään joihinkin Supply Chain Managementin dimensioihin. Lisäksi voidaan kuitenkin lisätä myös mukautettuja dimensioita (kuten _Lähde_) ilmaisemaan, tuleeko tapahtuma Supply Chain Managementista vai ulkoisesta järjestelmästä. |

### <a name="create-one-on-hand-change-event"></a><a name="create-one-onhand-change-event"></a>Yhden varastosaldon muutostapahtuman luominen

Tämä ohjelmointirajapinta luo yhden varastosaldon muutostapahtuman.

```txt
Path:
    /api/environment/{environmentId}/onhand
Method:
    Post
Headers:
    Api-Version="1.0"
    Authorization="Bearer $access_token"
ContentType:
    application/json
Body:
    {
        id: string,
        organizationId: string,
        productId: string,
        dimensionDataSource: string, # Optional
        dimensions: {
            [key:string]: string,
        },
        quantities: {
            [dataSourceName:string]: {
                [key:string]: number,
            },
        },
    }
```

Seuraavassa esimerkissä on näytteen tekstisisältö. Tässä näytteessä kirjataan *T-paita*-tuotteen muutostapahtuma. Tämä tapahtuma on myyntipistejärjestelmästä ja asiakas on palauttanut punaisen T-paidan myymälään. Tämä tapahtuma lisää *T-paita*-tuotteen määrää yhdellä.

```json
{
    "id": "123456",
    "organizationId": "usmf",
    "productId": "T-shirt",
    "dimensionDataSource": "pos",
    "dimensions": {
        "ColorId&quot;: &quot;Red"
    },
    "quantities": {
        "pos": {
            "inbound": 1
        }
    }
}
```

Seuraavassa esimerkissä on näytteen tekstisisältö ilman `dimensionDataSource`-arvoa.

```json
{
    "id": "123456",
    "organizationId": "usmf",
    "productId": "T-shirt",
    "dimensions": {
        "ColorId": "Red",
        "SiteId": "1",
        "LocationId&quot;: &quot;11"
    },
    "quantities": {
        "pos": {
            "inbound": 1
        }
    }
}
```

### <a name="create-multiple-change-events"></a><a name="create-multiple-onhand-change-events"></a>Useiden muutostapahtumien luominen

Tällä ohjelmointirajapinnalla voidaan luoda useita tietueita samanaikaisesti. Tämän ohjelmointirajapinnan ja [yhden tapahtuman ohjelmointirajapinnan](#create-one-onhand-change-event) ainoat erot ovat `Path`- ja `Body` -arvoissa. Tässä ohjelmointirajapinnassa `Body` tuottaa tietuematriisin.

```txt
Path:
    /api/environment/{environmentId}/onhand/bulk
Method:
    Post
Headers:
    Api-Version="1.0"
    Authorization="Bearer $access_token"
ContentType:
    application/json
Body:
    [
        {
            id: string,
            organizationId: string,
            productId: string,
            dimensionDataSource: string, # Optional
            dimensions: {
                [key:string]: string,
            },
            quantities: {
                [dataSourceName:string]: {
                    [key:string]: number,
                },
            },
        },
        ...
    ]
```

Seuraavassa esimerkissä on näytteen tekstisisältö.

```json
[
    {
        "id": "123456",
        "organizationId": "usmf",
        "productId": "T-shirt",
        "dimensionDataSource": "pos",
        "dimensions": {
            "PosMachineId&quot;: &quot;0001"
        },
        "quantities": {
            "pos": { "inbound": 1 }
        }
    },
    {
        "id": "654321",
        "organizationId": "usmf",
        "productId": "@PRODUCT1",
        "dimensionDataSource": "pos",
        "dimensions": {
            "PosMachineId&quot;: &quot;0001"
        },
        "quantities": {
            "pos": { "outbound": 3 }
        }
    }
]
```

## <a name="setoverride-on-hand-quantities"></a><a name="set-onhand-quantities"></a>Varastosaldomäärien määrittäminen tai ohittaminen

_Set on-hand_-ohjelmointirajapinta ohittaa määritetyn tuotteen nykyiset tiedot.

```txt
Path:
    /api/environment/{environmentId}/setonhand/{inventorySystem}/bulk
Method:
    Post
Headers:
    Api-Version="1.0"
    Authorization="Bearer $access_token"
ContentType:
    application/json
Body:
    [
        {
            id: string,
            organizationId: string,
            productId: string,
            dimensionDataSource: string, # Optional
            dimensions: {
                [key:string]: string,
            },
            quantities: {
                [dataSourceName:string]: {
                    [key:string]: number,
                },
            },
            modifiedDateTimeUTC: datetime,
        },
        ...
    ]
```

Seuraavassa esimerkissä on näytteen tekstisisältö. Tämän ohjelmointirajapinnan toiminta eroaa aiemmin tässä aiheessa kohdassa [Varastosaldon muutostapahtumien luominen](#create-onhand-change-event) kuvattujen ohjelmointirajapintojen toiminnasta. Tässä näytteessä *T-paita*-tuotteen määräksi määritetään 1.

```json
[
    {
        "id": "123456",
        "organizationId": "usmf",
        "productId": "T-shirt",
        "dimensionDataSource": "pos",
        "dimensions": {
            "PosMachineId": "0001"
        },
        "quantities": {
            "pos": {
                "inbound": 1
            }
        }
    }
]
```

## <a name="create-reservation-events"></a>Varaustapahtumien luominen

[!INCLUDE [preview-banner-section](../../includes/preview-banner-section.md)]

*Reserve*-ohjelmointirajapinnan käyttäminen edellyttää varausominaisuuden avaamista ja varausmääritysten tekemistä. Lisätietoja on kohdassa [Varausmääritykset (valinnainen)](inventory-visibility-configuration.md#reservation-configuration).

### <a name="create-one-reservation-event"></a><a name="create-one-reservation-event"></a>Yhden varaustapahtuman luominen

```txt
Path:
    /api/environment/{environmentId}/onhand/reserve
Method:
    Post
Headers:
    Api-Version="1.0"
    Authorization="Bearer $access_token"
ContentType:
    application/json
Body:
    {
        id: string,
        organizationId: string,
        productId: string,
        dimensionDataSource: string,
        dimensions: {
            [key:string]: string,
        },
        quantityDataSource: string, # optional
        quantities: {
            [dataSourceName:string]: {
                [key:string]: number,
            },
        },
        modifier: string,
        quantity: number,
        ifCheckAvailForReserv: boolean,
    }
```

Seuraavassa esimerkissä on näytteen tekstisisältö.

```json
{
    "id": "reserve-0",
    "organizationId": "usmf",
    "productId": "T-shirt",
    "quantity": 1,
    "quantityDataSource": "iv",
    "modifier": "softreservordered",
    "ifCheckAvailForReserv": true,
    "dimensions": {
        "SiteId": "1",
        "LocationId": "11",
        "ColorId": "Red",
        "SizeId&quot;: &quot;Small"
    }
}
```

### <a name="create-multiple-reservation-events"></a><a name="create-multiple-reservation-events"></a>Useiden varaustapahtumien luominen

Tämä ohjelmointirajapinta on [yhden tapahtuman ohjelmointirajapinnan](#create-one-reservation-event) joukkoversio.

```txt
Path:
    /api/environment/{environmentId}/onhand/reserve/bulk
Method:
    Post
Headers:
    Api-Version="1.0"
    Authorization="Bearer $access_token"
ContentType:
    application/json
Body:
    [
        {
            id: string,
            organizationId: string,
            productId: string,
            dimensionDataSource: string,
            dimensions: {
                [key:string]: string,
            },
            quantityDataSource: string, # optional
            quantities: {
                [dataSourceName:string]: {
                    [key:string]: number,
                },
            },
            modifier: string,
            quantity: number,
            ifCheckAvailForReserv: boolean,
        },
        ...
    ]
```

## <a name="query-on-hand"></a>Varastosaldokysely

_Query on-hand_-ohjelmointirajapinnalla noudetaan tuotteiden tämän hetkiset varastosaldotiedot.

### <a name="query-by-using-the-post-method"></a><a name="query-with-post-method"></a>Post-menetelmää käyttävä kysely

```txt
Path:
    /api/environment/{environmentId}/onhand/indexquery
Method:
    Post
Headers:
    Api-Version="1.0"
    Authorization="Bearer $access_token"
ContentType:
    application/json
Body:
    {
        organizationId: string,
        filters: {
            [dimensionKey:string]: string[],
        },
        groupByValues: string[],
        returnNegative: boolean,
    }
```

Seuraavassa esimerkissä on näytteen tekstisisältö.

```json
{
    "dimensionDataSource": "pos",
    "filters": {
        "organizationId": ["usmf"],
        "productId": ["T-shirt"],
        "ColorId": ["Red"]
    },
    "groupByValues": ["ColorId", "SizeId"],
    "returnNegative": true
}
```

### <a name="query-by-using-the-get-method"></a><a name="query-with-get-method"></a>Get-menetelmää käyttävä kysely

```txt
Path:
    /api/environment/{environmentId}/onhand/indexquery
Method:
    Get
Headers:
    Api-Version="1.0"
    Authorization="Bearer $access_token"
ContentType:
    application/json
Query(Url Parameters):
    groupBy
    returnNegative
    [Filters]
```

get URL -esimerkki: Tämä get-pyyntö täsmälleen sama kuin aiemmin annettu post-näyte.

```txt
/api/environment/{environmentId}/onhand/indexquery?organizationId=usmf&productId=T-shirt&ColorId=Red&groupBy=ColorId,SizeId&returnNegative=true
```

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
