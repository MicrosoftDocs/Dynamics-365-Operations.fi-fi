---
title: Varaston näkyvyyden julkiset ohjelmointirajapinnat
description: Tässä aiheessa käsitellään varaston näkyvyyden julkisia ohjelmointirajapintoja.
author: yufeihuang
ms.date: 12/09/2021
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2021-08-02
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: cb02e8d10a5c673734727682436ba1b3fc996935
ms.sourcegitcommit: 1877696fa05d66b6f51996412cf19e3a6b2e18c6
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/20/2022
ms.locfileid: "8786862"
---
# <a name="inventory-visibility-public-apis"></a>Varaston näkyvyyden julkiset ohjelmointirajapinnat

[!include [banner](../includes/banner.md)]


Tässä aiheessa käsitellään varaston näkyvyyden julkisia ohjelmointirajapintoja.

Varaston näkyvyyden apuohjelman julkinen REST API sisältää useita nimenomaisia integroinnin päätepisteitä. Se tukee neljää pääasiallista vuorovaikutustyyppiä:

- Käytettävissä olevan varastomäärän muutosten kirjaaminen apuohjelmaan ulkoisesta järjestelmästä
- Käytettävissä olevien varastosaldomäärien määrittäminen tai ohittaminen ulkoisesta järjestelmästä apuohjelmassa
- Varaustapahtumien kirjaaminen apuohjelmaan ulkoisesta järjestelmästä
- Nykyisten käytettävissä olevien määrien kysely ulkoisesta järjestelmästä

Seuraavassa taulukossa on tällä hetkellä käytettävissä olevat ohjelmointirajapinnat:

| Polku | Tapa | kuvaus |
|---|---|---|
| /api/environment/{environmentId}/onhand | Kirjaa | [Yhden käytettävissä olevan varastosaldon muutostapahtuman luominen](#create-one-onhand-change-event) |
| /api/environment/{environmentId}/onhand/bulk | Kirjaa | [Useiden muutostapahtumien luominen](#create-multiple-onhand-change-events) |
| /api/environment/{environmentId}/setonhand/{inventorySystem}/bulk | Kirjaa | [Käytettävissä olevien varastosaldomäärien määrittäminen tai ohittaminen](#set-onhand-quantities) |
| /api/environment/{environmentId}/onhand/reserve | Kirjaa | [Yhden varaustapahtuman luominen](#create-one-reservation-event) |
| /api/environment/{environmentId}/onhand/reserve/bulk | Kirjaa | [Useiden varaustapahtumien luominen](#create-multiple-reservation-events) |
| /api/environment/{environmentId}/onhand/changeschedule | Kirjaa | [Yhden aikataulutetun käytettävissä olevan saldon muutoksen luominen](inventory-visibility-available-to-promise.md) |
| /api/environment/{environmentId}/onhand/changeschedule/bulk | Kirjaa | [Useiden aikataulutettujen käytettävissä olevien varastosaldojen muutosten luominen](inventory-visibility-available-to-promise.md) |
| /api/environment/{environmentId}/onhand/indexquery | Kirjaa | [Post-menetelmää käyttävä kysely](#query-with-post-method) |
| /api/environment/{environmentId}/onhand | Hae | [Get-menetelmää käyttävä kysely](#query-with-get-method) |
| /api/environment/{environmentId}/allocation/allocate | Kirjaa | [Yhden kohdistustapahtuman luominen](inventory-visibility-allocation.md#using-allocation-api) |
| /api/environment/{environmentId}/allocation/unallocate | Kirjaa | [Yhden kohdistuksenpoistotapahtuman luominen](inventory-visibility-allocation.md#using-allocation-api) |
| /api/environment/{environmentId}/allocation/reallocate | Kirjaa | [Yhden uudelleenkohdistustapahtuman luominen](inventory-visibility-allocation.md#using-allocation-api) |
| /api/environment/{environmentId}/allocation/consume | Kirjaa | [Yhden kulutustapahtuman luominen](inventory-visibility-allocation.md#using-allocation-api) |
| /api/environment/{environmentId}/allocation/query | Kirjaa | [Kyselyn kohdistustulos](inventory-visibility-allocation.md#using-allocation-api) |

> [!NOTE]
> Polun {environmentId}-osa on ympäristötunnus Microsoft Dynamics Lifecycle Servicesissä (LCS).
> 
> Joukkotoimintosovellusliittymä voi palauttaa kullekin pyynnölle enintään 512 tietuetta.

Microsoft on antanut käyttöön *Postman*-pyyntökokoelman. Tämä kokoelma voidaan tuoda *Postman*-ohjelmistoon käyttämällä seuraavaa jaettua linkkiä: <https://www.getpostman.com/collections/ad8a1322f953f88d9a55>.

## <a name="find-the-endpoint-according-to-your-lifecycle-services-environment"></a>Lifecycle Services -ympäristön mukaisen päätepisteen etsiminen

Varaston näkyvyyden mikropalvelu otetaan käyttöön Microsoft Azure Service Fabricissa useilla maantieteellisillä alueilla ja useilla alueilla. Tällä hetkellä ei ole keskistettyä päätepistettä, joka uudelleenohjaisi pyynnön automaattisesti oikealle maantieteelliselle alueelle ja alueelle. Tämän vuoksi tieto-osista on muodostettava URL-osoite seuraavan mallin mukaisesti:

`https://inventoryservice.<RegionShortName>-il<IsLandNumber>.gateway.prod.island.powerapps.com`

Alueen lyhyen nimi on Microsoft Dynamics Lifecycle Services (LCS) -ympäristössä. Seuraavassa taulukossa on tällä hetkellä käytettävissä olevat alueet.

| Azure-alue        | Alueen lyhyt nimi |
| ------------------- | ----------------- |
| Itä-Australia      | eau               |
| Kaakkois-Australia | seau              |
| Kanada, keskinen      | cca               |
| Kanada, itäinen         | eca               |
| Pohjois-Eurooppa        | neu               |
| Länsi-Eurooppa         | weu               |
| Itä-Yhdysvallat             | eus               |
| Länsi-Yhdysvallat             | wus               |
| Eteläinen Yhdistynyt kuningaskunta            | suk               |
| Läntinen Yhdistynyt kuningaskunta             | wuk               |
| Itä-Japani          | ejp               |
| Länsi-Japani          | wjp               |
| Etelä-Brasilia        | sbr               |
| Keskinen Etelä-Yhdysvallat    | scus              |

Saaren numero ilmaisee, missä LCS-ympäristö otetaan käyttöön Service Fabricissa. Tätä tietoa ei voi tällä hetkellä saada millään tavalla käyttäjän puolelta.

Microsoft on muodostanut Power Appsiin käyttöliittymän, jonka avulla saadaan täydellinen mikropalvelun päätepiste. Lisätietoja on kohdassa [Palvelun päätepisteen etsiminen](inventory-visibility-configuration.md#get-service-endpoint).

## <a name="authentication"></a><a name="inventory-visibility-authentication"></a>Todennus

Varaston näkyvyyden julkisen ohjelmointirajapinnan kutsumiseen käytetään ympäristön suojaustunnusta. Siksi sinun on luotava _Azure Active Directory (Azure AD) -tunnus_ käyttämällä Azure AD -sovellustasi. Tämän jälkeen Azure AD -tunnuksen avulla saat _käyttöoikeustunnuksen_ suojauspalvelusta.

Microsoft toimittaa käyttövalmiin *Postman*-tunnusten hakukokoelman. Tämä kokoelma voidaan tuoda *Postman*-ohjelmistoon käyttämällä seuraavaa jaettua linkkiä: <https://www.getpostman.com/collections/496645018f96b3f0455e>.

Palvelun suojaustunnus haetaan seuraavasti:

1. Kirjaudu Azure-portaaliin ja etsi sen avulla Dynamics 365 Supply Chain Management -sovelluksen `clientId`- ja `clientSecret`-arvot.
1. Nouda Azure AD -tunnus (`aadToken`) lähettämällä HTTP-pyyntö, jossa on seuraavat ominaisuudet:

   - **URL:** `https://login.microsoftonline.com/${aadTenantId}/oauth2/token`
   - **Menetelmä:** `GET`
   - **Tekstisisältö (lomaketiedot):**

     | Avain           | Arvo                                |
     | ------------- | ------------------------------------ |
     | client_id     | ${aadAppId}                          |
     | client_secret | ${aadAppSecret}                      |
     | grant_type    | client_credentials                   |
     | resurssi      | 0cdb527f-a8d1-4bf8-9436-b352c68682b2 |

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
   - `context`-arvon on oltava LCS-ympäristötunnus, jossa apuohjelma halutaan ottaa käyttöön.
   - Kaikki muut arvot määritetään samoiksi kuin esimerkissä.

1. Nouda käyttöoikeustietue (`access_token`) lähettämällä HTTP-pyyntö, jossa on seuraavat ominaisuudet:

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

> [!IMPORTANT]
> Kun *Postman*-pyyntökokoelmalla kutsutaan varaston näkyvyyden julkinen ohjelmointirajapinta, jokaiseen pyyntöön on lisättävä haltijatunnus. Haltijatunnuksen voi etsiä valitsemalla **Valtuutus**-välilehden pyynnön URL-osoitteessa, valitsemalla **Haltijatunnus**-tyypin ja kopioimalla edellisessä vaiheessa noudetun käyttöoikeustietueen. Tämä aiheen myöhemmissä osissa `$access_token` ilmaisee tunnuksen, joka noudettiin viimeisessä vaiheessa.

## <a name="create-on-hand-change-events"></a><a name="create-onhand-change-event"></a>Käytettävissä olevan varastosaldon muutostapahtumien luominen

Käytettävissä olevien varastosaldon muutostapahtumien luontiin on käytettävissä kaksi ohjelmointirajapintaa:

- Yhden tietueen luonti: `/api/environment/{environmentId}/onhand`
- Useiden tietueiden luonti: `/api/environment/{environmentId}/onhand/bulk`

Seuraavassa taulukossa on yhteenveto JSON-tekstiosan kunkin kentän merkityksestä.

| Kentän tunnus | kuvaus |
|---|---|
| `id` | Tietyn muutostapahtuman yksilöivä tunnus. Tämän tunnuksen avulla varmistetaan, että jos viestintä palveluun epäonnistuu kirjauksen aikana, samaa tapahtumaa ei lasketa järjestelmässä kahdesti, jos se lähetetään uudelleen. |
| `organizationId` | Tapahtumaan linkitetyn organisaation tunniste. Tämä arvo yhdistetään Supply Chain Managementin organisaatioon tai tietoalueen tunnukseen. |
| `productId` | Tuotteen tunniste. |
| `quantities` | Määrä, jolla käytettävissä olevaa varastosaldoa on muutettava. Jos hyllylle lisättiin esimerkiksi 10 uutta kirjaa, tämä arvo on `quantities:{ shelf:{ received: 10 }}`. Jos hyllystä poistettiin tai myytiin kolme kirjaa, tämä arvo on `quantities:{ shelf:{ sold: 3 }}`. |
| `dimensionDataSource` | Muutostapahtuman kirjauksessa ja kyselyssä käytettävien dimensioiden tietolähde. Jos tietolähde määritetään, määritetyn tietolähteen mukautettuja dimensioita voidaan käyttää. Varaston näkyvyyssovellus voi käyttää dimensiomääritystä mukautettujen dimensioiden yhdistämiseen yleisiin oletusdimensioihin. Jos `dimensionDataSource`-arvoa ei ole määritetty, kyselyissä voi käyttää vain yleisiä [perusdimensioita](inventory-visibility-configuration.md#data-source-configuration-dimension). |
| `dimensions` | Dynaaminen avain- ja arvopari. Arvot yhdistetään joihinkin Supply Chain Managementin dimensioihin. Lisäksi voidaan kuitenkin lisätä myös mukautettuja dimensioita (kuten _Lähde_) ilmaisemaan, tuleeko tapahtuma Supply Chain Managementista vai ulkoisesta järjestelmästä. |

> [!NOTE]
> `SiteId`- ja `LocationId`-parametrit muodostavat [osiomäärityksen](inventory-visibility-configuration.md#partition-configuration). Siksi ne on määritettävä dimensioissa, kun luodaan käytettävissä olevan varaston muutostapahtumia, määritetään tai ohitetaan käytettävissä olevan varaston määriä tai luodaan varaustapahtumia.

### <a name="create-one-on-hand-change-event"></a><a name="create-one-onhand-change-event"></a>Yhden käytettävissä olevan varastosaldon muutostapahtuman luominen

Tämä ohjelmointirajapinta luo yhden käytettävissä olevan varastosaldon muutostapahtuman.

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
        "SiteId": "1",
        "LocationId": "11",
        "PosMachineId": "0001",
        "ColorId&quot;: &quot;Red"
    },
    "quantities": {
        "pos": {
            "inbound": 1
        }
    }
}
```

Seuraavassa esimerkissä on näytteen tekstisisältö ilman `dimensionDataSource`-arvoa. Tässä tapauksessa `dimensions`-parametri toimii [perusdimensioina](inventory-visibility-configuration.md#data-source-configuration-dimension). Jos `dimensionDataSource` on määritetty, `dimensions` voi toimia joko tietolähdedimensioina tai perusdimensioina.

```json
{
    "id": "123456",
    "organizationId": "usmf",
    "productId": "T-shirt",
    "dimensions": {
        "SiteId": "1",
        "LocationId": "11",
        "ColorId": "Red"
    },
    "quantities": {
        "pos": {
            "inbound": 1
        }
    }
}
```

### <a name="create-multiple-change-events"></a><a name="create-multiple-onhand-change-events"></a>Useiden muutostapahtumien luominen

Tällä ohjelmointirajapinnalla voidaan luoda useita tietueita samanaikaisesti. Tämän ohjelmointirajapinnan ja [yhden tapahtuman ohjelmointirajapinnan](#create-one-onhand-change-event) ainoat erot ovat `Path`- ja `Body` -arvoissa. Tässä ohjelmointirajapinnassa `Body` tuottaa tietuematriisin. Tietueiden enimmäismäärä on 512, mikä tarkoittaa, että käytettävissä oleva joukkotoiminto-ohjelmointirajapinta voi tukea enintään 512 muutostapahtumaa kerrallaan.

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
            "PosSiteId": "1",
            "PosLocationId": "11",
            "PosMachineId&quot;: &quot;0001"
        },
        "quantities": {
            "pos": { "inbound": 1 }
        }
    },
    {
        "id": "654321",
        "organizationId": "usmf",
        "productId": "Pants",
        "dimensions": {
            "SiteId": "1",
            "LocationId": "11",
            "ColorId&quot;: &quot;black"
        },
        "quantities": {
            "pos": { "outbound": 3 }
        }
    }
]
```

## <a name="setoverride-on-hand-quantities"></a><a name="set-onhand-quantities"></a>Käytettävissä olevien varastosaldomäärien määrittäminen tai ohittaminen

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

Seuraavassa esimerkissä on näytteen tekstisisältö. Tämän ohjelmointirajapinnan toiminta eroaa aiemmin tässä aiheessa kohdassa [Käytettävissä olevan varastosaldon muutostapahtumien luominen](#create-onhand-change-event) kuvattujen ohjelmointirajapintojen toiminnasta. Tässä näytteessä *T-paita*-tuotteen määräksi määritetään 1.

```json
[
    {
        "id": "123456",
        "organizationId": "usmf",
        "productId": "T-shirt",
        "dimensionDataSource": "pos",
        "dimensions": {
             "PosSiteId": "1",
            "PosLocationId": "11",
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

*Reserve*-ohjelmointirajapinnan käyttäminen edellyttää varausominaisuuden avaamista ja varausmääritysten tekemistä. Lisätietoja on kohdassa [Varausmääritykset (valinnainen)](inventory-visibility-configuration.md#reservation-configuration).

### <a name="create-one-reservation-event"></a><a name="create-one-reservation-event"></a>Yhden varaustapahtuman luominen

Varauksia voidaan tehdä erilaisten tietolähdeasetusten perusteella. Voit määrittää tämän varaustyypin määrittämällä ensin tietolähteen `dimensionDataSource`-parametrissa. Määritä sitten `dimensions`-parametrissa dimensiot kohdetietolähteen dimensioasetusten mukaisesti.

Kun kutsut varausten ohjelmointirajapintaa, voit ohjata varausten vahvistamista määrittämällä `ifCheckAvailForReserv`-totuusarvoparametrin pyynnön tekstiosassa. `True`-arvo tarkoittaa, että vahvistus vaaditaan, ja `False`-arvo, että vahvistusta ei vaadita. Oletusarvona on `True`.

Jos haluat perua varauksen tai poistaa tiettyjen varastomäärien varauksen, määritä määräsi negatiivinen arvo ja ohita vahvistus määrittämällä `ifCheckAvailForReserv`-parametrin arvoksi `False`.

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

## <a name="query-on-hand"></a>Käytettävissä olevan varastosaldon kysely

_Query on-hand_-ohjelmointirajapinnalla voit noutaa tuotteiden tämän hetkiset käytettävissä olevat varastosaldotiedot. Sovellusrajapinta tukee tällä hetkellä kyselyä, jossa on enintään 100 yksittäistä nimikettä `ProductID`-arvon mukaan. Jokaisessa kyselyssä voi määrittää myös useita `SiteID`- ja `LocationID`-arvoja. Enimmäisrajaksi määritetään `NumOf(SiteID) * NumOf(LocationID) <= 100`.

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
        dimensionDataSource: string, # Optional
        filters: {
            organizationId: string[],
            productId: string[],
            siteId: string[],
            locationId: string[],
            [dimensionKey:string]: string[],
        },
        groupByValues: string[],
        returnNegative: boolean,
    }
```

Tämän pyynnön tekstiosassa `dimensionDataSource` on edelleen valinnainen parametri. Jos sitä ei ole määritetty, sitä `filters`-parametria käytetään *perusdimensioina*. `filters`-parametrilla on neljä pakollista kenttää: `organizationId`, `productId`, `siteId` ja `locationId`.

- `organizationId`-kentän pitäisi sisältää vain yksi arvo, mutta se on silti matriisi.
- `productId` voi sisältää yhden tai useampia arvoja. Jos se on tyhjä matriisi, kaikki tuotteet palautetaan.
- Kenttiä `siteId` ja `locationId` käytetään varaston näkyvyydessä osiointiin. *Varastosaldokysely*-pyynnössä voi määrittää useita `siteId`- ja `locationId`-arvoja. Nykyisessä versiossa on määritettävä sekä `siteId`- että `locationId`-arvo.

`groupByValues`-parametrin pitäisi noudattaa indeksointimääritystä. Lisätietoja on kohdassa [Tuoteindeksihierarkian määrittäminen](./inventory-visibility-configuration.md#index-configuration).

Parametri `returnNegative` määrittää, sisältävätkö tulokset negatiivisia merkintöjä.

> [!NOTE]
> Jos olet ottanut käyttöön käytössä olevan muutoksen aikataulun ja ATP-ominaisuudet, kyselysi voi sisältää myös `QueryATP` Boolean-parametrin, joka määrittää, sisältävätkö kyselyn tulokset ATP-tietoja. Lisätietoja ja esimerkkejä on kohdassa [Käytettävissä olevan varaston näkyvyyden muutosaikataulut ja luvattavissa olevat aikataulut](inventory-visibility-available-to-promise.md).

Seuraavassa esimerkissä on näytteen tekstisisältö.

```json
{
    "dimensionDataSource": "pos",
    "filters": {
        "organizationId": ["usmf"],
        "productId": ["T-shirt"],
        "siteId": ["1"],
        "LocationId": ["11"],
        "ColorId": ["Red"]
    },
    "groupByValues": ["ColorId", "SizeId"],
    "returnNegative": true
}
```

Seuraavassa esimerkissä esitetään, miten kaikkia tuotteita kysellään tietyllä sivustolla ja tietyssä sijainnissa.

```json
{
    "filters": {
        "organizationId": ["usmf"],
        "productId": [],
        "siteId": ["1"],
        "LocationId": ["11"],
    },
    "groupByValues": ["ColorId", "SizeId"],
    "returnNegative": true
}
```

### <a name="query-by-using-the-get-method"></a><a name="query-with-get-method"></a>Get-menetelmää käyttävä kysely

```txt
Path:
    /api/environment/{environmentId}/onhand
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
/api/environment/{environmentId}/onhand?organizationId=usmf&productId=T-shirt&SiteId=1&LocationId=11&ColorId=Red&groupBy=ColorId,SizeId&returnNegative=true
```

## <a name="available-to-promise"></a>Luvattavissa oleva määrä (ATP)

Voit määrittää varaston näkyvyyden sallimaan tulevien käytettävissä olevien muutosten ajoituksen ja ATP-määrien laskemisen. ATP on tuotteen määrä, joka on saatavilla ja joka voidaan luvata asiakkaalle seuraavalla kaudella. ATP-laskelman käyttö voi lisätä tilauksen täyttämiskykyä merkittävästi. Tietoja siitä, miten tämä ominaisuus otetaan käyttöön ja miten varaston näkyvyys otetaan käyttöön sen API-liittymän kautta ominaisuuden käytön jälkeen, on kohdassa [Varaston näkyvyyden käytettävissä olevan varaston muutosaikataulut ja luvattavissa olevat määrät](inventory-visibility-available-to-promise.md#api-urls).

## <a name="allocation"></a>Varaus

Kohdistukseen liittyvät ohjelmointirajapinnat sijaitsevat kohdassa [Varaston näkyvyyden kohdistus](inventory-visibility-allocation.md#using-allocation-api).

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
