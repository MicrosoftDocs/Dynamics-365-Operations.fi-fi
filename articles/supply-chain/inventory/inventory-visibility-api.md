---
title: Varaston näkyvyyden julkiset ohjelmointirajapinnat
description: Tässä artikkelissa käsitellään varaston näkyvyyden julkisia ohjelmointirajapintoja.
author: yufeihuang
ms.date: 11/04/2022
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2021-08-02
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: 8b0b8ca261237fbb2190f2a94cc11b816ae05af5
ms.sourcegitcommit: 49f8973f0e121eac563876d50bfff00c55344360
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/14/2022
ms.locfileid: "9762831"
---
# <a name="inventory-visibility-public-apis"></a>Varaston näkyvyyden julkiset ohjelmointirajapinnat

[!include [banner](../includes/banner.md)]

Tässä artikkelissa käsitellään varaston näkyvyyden julkisia ohjelmointirajapintoja.

Varaston näkyvyyden apuohjelman julkinen REST API sisältää useita nimenomaisia integroinnin päätepisteitä. Se tukee neljää pääasiallista vuorovaikutustyyppiä:

- Käytettävissä olevan varastomäärän muutosten kirjaaminen apuohjelmaan ulkoisesta järjestelmästä
- Käytettävissä olevien varastosaldomäärien määrittäminen tai ohittaminen ulkoisesta järjestelmästä apuohjelmassa
- Varaustapahtumien kirjaaminen apuohjelmaan ulkoisesta järjestelmästä
- Nykyisten käytettävissä olevien määrien kysely ulkoisesta järjestelmästä

Seuraavassa taulukossa on tällä hetkellä käytettävissä olevat ohjelmointirajapinnat:

| Polku | Tapa | kuvaus |
|---|---|---|
| /api/environment/{environmentId}/onhand | Kirjaa | [Yhden käytettävissä olevan varastosaldon muutostapahtuman luominen](#create-one-onhand-change-event)|
| /api/environment/{environmentId}/onhand/bulk | Kirjaa | [Useiden muutostapahtumien luominen](#create-multiple-onhand-change-events) |
| /api/environment/{environmentId}/setonhand/{inventorySystem}/bulk | Kirjaa | [Käytettävissä olevien varastosaldomäärien määrittäminen tai ohittaminen](#set-onhand-quantities) |
| /api/environment/{environmentId}/onhand/reserve | Kirjaa | [Yhden alustavan varauksen tapahtuman luominen](#create-one-reservation-event) |
| /api/environment/{environmentId}/onhand/reserve/bulk | Kirjaa | [Useiden alustavien varausten tapahtumien luominen](#create-multiple-reservation-events) |
| /api/environment/{environmentId}/onhand/unreserve | Kirjaa | [Yhden alustavan varauksen tapahtuman peruuttaminen](#reverse-one-reservation-event) |
| /api/environment/{environmentId}/onhand/unreserve/bulk | Kirjaa | [Useiden alustavien varausten tapahtumien peruuttaminen](#reverse-multiple-reservation-events) |
| /api/environment/{environmentId}/onhand/changeschedule | Kirjaa | [Yhden aikataulutetun käytettävissä olevan saldon muutoksen luominen](inventory-visibility-available-to-promise.md) |
| /api/environment/{environmentId}/onhand/changeschedule/bulk | Kirjaa | [Useiden käytettävissä olevien varastosaldojen muutosten ja päivämäärien luominen](inventory-visibility-available-to-promise.md) |
| /api/environment/{environmentId}/onhand/indexquery | Kirjaa | [Post-menetelmää käyttävä kysely](#query-with-post-method) (suositeltu) |
| /api/environment/{environmentId}/onhand | Hae | [Get-menetelmää käyttävä kysely](#query-with-get-method) |
| /api/environment/{environmentId}/onhand/exactquery | Kirjaa | [Post-menetelmää käyttävä tarkka kysely](#exact-query-with-post-method) |
| /api/environment/{environmentId}/allocation<wbr>/allocate | Kirjaa | [Yhden kohdistustapahtuman luominen](inventory-visibility-allocation.md#using-allocation-api) |
| /api/environment/{environmentId}/allocation<wbr>/unallocate | Kirjaa | [Yhden kohdistuksenpoistotapahtuman luominen](inventory-visibility-allocation.md#using-allocation-api) |
| /api/environment/{environmentId}/allocation<wbr>/reallocate | Kirjaa | [Yhden uudelleenkohdistustapahtuman luominen](inventory-visibility-allocation.md#using-allocation-api) |
| /api/environment/{environmentId}/allocation<wbr>/consume | Kirjaa | [Yhden kulutustapahtuman luominen](inventory-visibility-allocation.md#using-allocation-api) |
| /api/environment/{environmentId}/allocation<wbr>/query | Kirjaa | [Kyselyn kohdistustulos](inventory-visibility-allocation.md#using-allocation-api) |

> [!NOTE]
> Polun {environmentId}-osa on ympäristötunnus Microsoft Dynamics Lifecycle Servicesissä.
> 
> Joukkotoimintosovellusliittymä voi palauttaa kullekin pyynnölle enintään 512 tietuetta.

Microsoft on antanut käyttöön *Postman*-pyyntökokoelman. Tämä kokoelma voidaan tuoda *Postman*-ohjelmistoon käyttämällä seuraavaa jaettua linkkiä: <https://www.getpostman.com/collections/95a57891aff1c5f2a7c2>.

## <a name="find-the-endpoint-according-to-your-lifecycle-services-environment"></a><a name = "endpoint-lcs"></a>Lifecycle Services -ympäristön mukaisen päätepisteen etsiminen

Varaston näkyvyyden mikropalvelu otetaan käyttöön Microsoft Azure Service Fabricissa useilla maantieteellisillä alueilla ja useilla alueilla. Tällä hetkellä ei ole keskistettyä päätepistettä, joka uudelleenohjaisi pyynnön automaattisesti oikealle maantieteelliselle alueelle ja alueelle. Tämän vuoksi tieto-osista on muodostettava URL-osoite seuraavan mallin mukaisesti:

`https://inventoryservice.<RegionShortName>-il<IsLandNumber>.gateway.prod.island.powerapps.com`

Alueen lyhyt nimi löytyy Lifecycle Services -ympäristöstä. Seuraavassa taulukossa on tällä hetkellä käytettävissä olevat alueet.

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
| Keskinen Intia       | cin               |
| Etelä-Intia         | sin               |
| Sveitsi, pohjoinen   | nch               |
| Sveitsi, läntinen    | wch               |
| Ranska, eteläinen        | sfr               |
| Itä-Aasia           | eas               |
| Kaakkois-Aasia     | seas              |
| Yhdistyneet arabiemiirikunnat, pohjoinen           | nae               |
| Norja, itäinen         | eno               |
| Norja, läntinen         | wno               |
| Etelä-Afrikka, läntinen   | wza               |
| Etelä-Afrikka, pohjoinen  | nza               |

Saaren numero ilmaisee, missä Lifecycle Services -ympäristö otetaan käyttöön Service Fabricissa. Tätä tietoa ei voi tällä hetkellä saada millään tavalla käyttäjän puolelta.

Microsoft on muodostanut Power Appsiin käyttöliittymän, jonka avulla saadaan täydellinen mikropalvelun päätepiste. Lisätietoja on kohdassa [Palvelun päätepisteen etsiminen](inventory-visibility-configuration.md#get-service-endpoint).

## <a name="authentication"></a><a name="inventory-visibility-authentication"></a>Todennus

Varaston näkyvyyden julkisen ohjelmointirajapinnan kutsumiseen käytetään ympäristön suojaustunnusta. Siksi sinun on luotava *Azure Active Directory (Azure AD) -tunnus* Azure AD -sovelluksen avulla. Tämän jälkeen Azure AD -tunnuksen avulla saat *käyttöoikeustunnuksen* suojauspalvelusta.

Microsoft toimittaa käyttövalmiin *Postman*-tunnusten hakukokoelman. Tämä kokoelma voidaan tuoda *Postman*-ohjelmistoon käyttämällä seuraavaa jaettua linkkiä: <https://www.getpostman.com/collections/496645018f96b3f0455e>.

Palvelun suojaustunnus haetaan seuraavasti:

1. Kirjaudu Azure-portaaliin ja etsi sen avulla Dynamics 365 Supply Chain Management -sovelluksen `clientId`- ja `clientSecret`-arvot.
1. Nouda Azure AD -tunnus (`aadToken`) lähettämällä HTTP-pyyntö, jossa on seuraavat ominaisuudet:

    - **URL-osoite:** `https://login.microsoftonline.com/${aadTenantId}/oauth2/v2.0/token`
    - **Menetelmä:** `GET`
    - **Tekstisisältö (lomaketiedot):**

        | Avain           | Arvo                                            |
        | ------------- | -------------------------------------------------|
        | client_id     | ${aadAppId}                                      |
        | client_secret | ${aadAppSecret}                                  |
        | grant_type    | client_credentials                               |
        | vaikutusalue         | 0cdb527f-a8d1-4bf8-9436-b352c68682b2/.oletusarvo    |

    Vastauksena pitäisi olla Azure AD -tunnus (`aadToken`). Tarran pitäisi on seuraavan esimerkin kaltainen:

    ```json
    {
        "token_type": "Bearer",
        "expires_in": "3599",
        "ext_expires_in": "3599",
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
        "context": "{$LCS_environment_id}",
        "context_type": "finops-env"
    }
    ```

    Huomaa seuraavat seikat:

    - `client_assertion`-arvon on oltava edellisessä vaiheessa vastaanotettu Azure AD -tunnus (`aadToken`).
    - `context`-arvon on oltava sen Lifecycle Services -ympäristön tunnus, jossa apuohjelma halutaan ottaa käyttöön.
    - Kaikki muut arvot määritetään samoiksi kuin esimerkissä.

1. Nouda käyttöoikeustietue (`access_token`) lähettämällä HTTP-pyyntö, jossa on seuraavat ominaisuudet:

    - **URL:** `https://securityservice.operations365.dynamics.com/token`
    - **Menetelmä:** `POST`
    - **HTTP-otsikko:** Ohjelmointirajapinnan versio on sisällytettävä. (Avain on `Api-Version` ja arvo `1.0`.)
    - **Tekstisisältö:** sisällytetään edellisessä vaiheessa luotu JSON-pyyntö.

    Vastauksena pitäisi olla käyttöoikeustietue (`access_token`). Tätä tunnusta on käytettävä haltijatunnuksena, jolla varaston näkyvyyden ohjelmointirajapintaa kutsutaan. Alla on esimerkki.

    ```json
    {
        "access_token": "{Returned_Token}",
        "token_type": "bearer",
        "expires_in": 3600
    }
    ```

> [!IMPORTANT]
> Kun *Postman*-pyyntökokoelmalla kutsutaan varaston näkyvyyden julkinen ohjelmointirajapinta, jokaiseen pyyntöön on lisättävä haltijatunnus. Haltijatunnuksen voi etsiä valitsemalla **Valtuutus**-välilehden pyynnön URL-osoitteessa, valitsemalla **Haltijatunnus**-tyypin ja kopioimalla edellisessä vaiheessa noudetun käyttöoikeustietueen. Tämä artikkelin myöhemmissä osissa `$access_token` ilmaisee tunnuksen, joka noudettiin viimeisessä vaiheessa.

## <a name="create-on-hand-change-events"></a><a name="create-onhand-change-event"></a>Käytettävissä olevan varastosaldon muutostapahtumien luominen

Käytettävissä olevien varastosaldon muutostapahtumien luontiin on käytettävissä kaksi ohjelmointirajapintaa:

- Yhden tietueen luonti: `/api/environment/{environmentId}/onhand`
- Useiden tietueiden luonti: `/api/environment/{environmentId}/onhand/bulk`

Seuraavassa taulukossa on yhteenveto JSON-tekstiosan kunkin kentän merkityksestä.

| Kentän tunnus | Kuvaus |
|---|---|
| `id` | Tietyn muutostapahtuman yksilöivä tunnus. Jos uudelleenlähettäminen tapahtuu palvelun virheen vuoksi, tämän tunnuksen avulla varmistetaan, että samaa tapahtumaa ei lasketa järjestelmässä kahdesti. |
| `organizationId` | Tapahtumaan linkitetyn organisaation tunniste. Tämä arvo yhdistetään Supply Chain Managementin organisaatioon tai tietoalueen tunnukseen. |
| `productId` | Tuotteen tunniste. |
| `quantities` | Määrä, jolla käytettävissä olevaa varastosaldoa on muutettava. Jos hyllylle lisättiin esimerkiksi 10 uutta kirjaa, tämä arvo on `quantities:{ shelf:{ received: 10 }}`. Jos hyllystä poistettiin tai myytiin kolme kirjaa, tämä arvo on `quantities:{ shelf:{ sold: 3 }}`. |
| `dimensionDataSource` | Muutostapahtuman kirjauksessa ja kyselyssä käytettävien dimensioiden tietolähde. Jos tietolähde määritetään, määritetyn tietolähteen mukautettuja dimensioita voidaan käyttää. Varaston näkyvyyssovellus voi käyttää dimensiomääritystä mukautettujen dimensioiden yhdistämiseen yleisiin oletusdimensioihin. Jos `dimensionDataSource`-arvoa ei ole määritetty, kyselyissä voi käyttää vain yleisiä [perusdimensioita](inventory-visibility-configuration.md#data-source-configuration-dimension). |
| `dimensions` | Dynaaminen avain- ja arvopari. Arvot yhdistetään joihinkin Supply Chain Managementin dimensioihin. Lisäksi voidaan kuitenkin lisätä myös mukautettuja dimensioita (kuten *Lähde*) ilmaisemaan, tuleeko tapahtuma Supply Chain Managementista vai ulkoisesta järjestelmästä. |

> [!NOTE]
> `siteId`- ja `locationId`-parametrit muodostavat [osiomäärityksen](inventory-visibility-configuration.md#partition-configuration). Siksi ne on määritettävä dimensioissa, kun luodaan käytettävissä olevan varaston muutostapahtumia, määritetään tai ohitetaan käytettävissä olevan varaston määriä tai luodaan varaustapahtumia.

Seuraavissa aliosissa on esimerkkejä näiden ohjelmointirajapintojen käytöstä.

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

Seuraavassa esimerkissä on näytteen tekstisisältö. Tässä esimerkissä yrityksellä on myyntipistejärjestelmä, joka käsittelee myymälän tapahtumia ja näin ollen myös varastomuutoksia. Asiakas on palauttanut punaisen T-paidan myymälään. Muutoksen vuoksi kirjataan muutostapahtuma *T-paita*-tuotteelle. Tämä tapahtuma lisää *T-paita*-tuotteen määrää yhdellä.

```json
{
    "id": "Test201",
    "organizationId": "usmf",
    "productId": "T-shirt",
    "dimensionDataSource": "pos",
    "dimensions": {
        "siteId": "1",
        "locationId": "11",
        "posMachineId": "0001",
        "colorId&quot;: &quot;red"
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
    "id": "Test202",
    "organizationId": "usmf",
    "productId": "T-shirt",
    "dimensions": {
        "siteId": "1",
        "locationId": "11",
        "colorId": "red"
    },
    "quantities": {
        "pos": {
            "inbound": 1
        }
    }
}
```

### <a name="create-multiple-change-events"></a><a name="create-multiple-onhand-change-events"></a>Useiden muutostapahtumien luominen

Tämä ohjelmointirajapinta voi luoda muutostapahtumia samalla tavalla kuin [yhden tapahtuman ohjelmointirajapinta](#create-one-onhand-change-event). Ainoa ero on, että tällä ohjelmointirajapinnalla voidaan luoda useita tietueita samanaikaisesti. Näin ollen arvot `Path` ja `Body` ovat erilaiset. Tässä ohjelmointirajapinnassa `Body` tuottaa tietuematriisin. Tietueiden enimmäismäärä on 512. Näin ollen varastosaldon muutoksen joukkotoiminto-ohjelmointirajapinta voi tukea jopa 512:n muutostapahtuman tekemistä kerralla. 

Esimerkiksi vähittäismyymälän myyntipisteen kone käsitteli seuraavat kaksi tapahtumaa:

- Yksi palautustilaus yhdelle punaiselle T-paidalle
- Yksi myyntitapahtuma kolmelle mustalle T-paidalle

Tässä tapauksessa molemmat varastopäivitykset voidaan sisällyttää ohjelmointirajapintakutsuun.

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
        "id": "Test203",
        "organizationId": "usmf",
        "productId": "T-shirt",
        "dimensionDataSource": "pos",
        "dimensions": {
            "SiteId": "Site1",
            "LocationId": "11",
            "posMachineId&quot;: &quot;0001"
            "colorId&quot;: &quot;red"
        },
        "quantities": {
            "pos": { "inbound": 1 }
        }
    },
    {
        "id": "Test204",
        "organizationId": "usmf",
        "productId": "T-shirt",
        "dimensions": {
            "siteId": "1",
            "locationId": "11",
            "colorId&quot;: &quot;black"
        },
        "quantities": {
            "pos": { "outbound": 3 }
        }
    }
]
```

## <a name="setoverride-on-hand-quantities"></a><a name="set-onhand-quantities"></a>Käytettävissä olevien varastosaldomäärien määrittäminen tai ohittaminen

*Set on-hand*-ohjelmointirajapinta ohittaa määritetyn tuotteen nykyiset tiedot. Tätä toimintoa käytetään yleensä varaston inventointipäivitysten yhteydessä. Esimerkiksi päivittäisen varastoinventoinnin yhteydessä myymälässä saatetaan havaita, että punaisten T-paitojen todellinen varastosaldo on 100. Tämän vuoksi myyntipisteen saapuva määrä on päivitettävä arvoksi 100 siitä huolimatta, mikä edellinen määrä oli. Voit ohittaa aiemmin luodun arvon käyttämällä tätä ohjelmointirajapintaa.

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

Seuraavassa esimerkissä on näytteen tekstisisältö. Tämän ohjelmointirajapinnan toiminta eroaa aiemmin tässä artikkelissa kohdassa [Käytettävissä olevan varastosaldon muutostapahtumien luominen](#create-onhand-change-event) kuvattujen ohjelmointirajapintojen toiminnasta. Tässä näytteessä *T-paita*-tuotteen määräksi määritetään 1.

```json
[
    {
        "id": "Test204",
        "organizationId": "usmf",
        "productId": "T-shirt",
        "dimensionDataSource": "pos",
        "dimensions": {
            "SiteId": "1",
            "LocationId": "11",
            "posMachineId": "0001"
            "colorId": "red"
        },
        "quantities": {
            "pos": {
                "inbound": 100
            }
        }
    }
]
```

## <a name="create-reservation-events"></a>Varaustapahtumien luominen

*Reserve*-ohjelmointirajapinnan käyttäminen edellyttää varausominaisuuden ottamista käyttöön ja varausmääritysten tekemistä. Lisätietoja (myös tietovuosta ja esimerkkiskenaariosta) on kohdassa [Varausmääritykset (valinnainen)](inventory-visibility-configuration.md#reservation-configuration).

### <a name="create-one-reservation-event"></a><a name="create-one-reservation-event"></a>Yhden varaustapahtuman luominen

Varauksia voidaan tehdä erilaisten tietolähdeasetusten perusteella. Voit määrittää tämän varaustyypin määrittämällä ensin tietolähteen `dimensionDataSource`-parametrissa. Määritä sitten `dimensions`-parametrissa dimensiot kohdetietolähteen dimensioasetusten mukaisesti.

Kun kutsut varausten ohjelmointirajapintaa, voit ohjata varausten vahvistamista määrittämällä `ifCheckAvailForReserv`-totuusarvoparametrin pyynnön tekstiosassa. `True`-arvo tarkoittaa, että vahvistus vaaditaan, ja `False`-arvo, että vahvistusta ei vaadita. Oletusarvona on `True`.

Jos haluat peruuttaa varauksen tai poistaa tiettyjen varastomäärien varauksen, määritä määräsi negatiivinen arvo ja ohita vahvistus määrittämällä `ifCheckAvailForReserv`-parametrin arvoksi `False`. Lisäksi on olemassa määritetty unreserve-ohjelmointirajapinta, joka tekee samat toiminnot. Erona on ainoastaan se, miten näitä kahta ohjelmointirajapintaa kutsutaan. On helpompi peruuttaa tietty varaustapahtuma käyttämällä tunnusta `reservationId` kuin *unreserve*-ohjelmointirajapintaa. Lisätietoja on [Yhden varaustapahtuman varauksen poistaminen](#reverse-reservation-events) -osassa.

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
    "organizationId": "SCM_IV",
    "productId": "iv_postman_product",
    "quantity": 1,
    "quantityDataSource": "iv",
    "modifier": "softReservOrdered",
    "ifCheckAvailForReserv": true,
    "dimensions": {
        "siteId": "iv_postman_site",
        "locationId": "iv_postman_location",
        "colorId": "red",
        "sizeId&quot;: &quot;small"
    }
}
```

Seuraavassa esimerkissä näytetään onnistunut vastaus.

```json
{
    "reservationId": "RESERVATION_ID",
    "id": "ohre~id-822-232959-524",
    "processingStatus": "success",
    "message": "",
    "statusCode": 200
}
``` 

### <a name="create-multiple-reservation-events"></a><a name="create-multiple-reservation-events"></a>Useiden varaustapahtumien luominen

Tämä ohjelmointirajapinta on [yhden tapahtuman ohjelmointirajapinnan](#create-reservation-events) joukkoversio.

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

## <a name="reverse-reservation-events"></a>Varaustapahtumien peruuttaminen

*Unreserve*-ohjelmointirajapinta toimii [*varaustapahtumien*](#create-reservation-events)  peruutustoimintona. Sen avulla voi peruuttaa varaustapahtuman, jonka `reservationId` on määrittänyt, tai vähentää varausmäärää.

### <a name="reverse-one-reservation-event"></a><a name="reverse-one-reservation-event"></a>Yhden varaustapahtuman peruuttaminen

Kun varaus luodaan, `reservationId` sisällytetään vastauksen tekstiin. Anna sama `reservationId`, jos haluat peruuttaa varauksen, ja sisällytä samat varauksen ohjelmointirajapintakutsussa käytetyt tunnukset `organizationId` ja `dimensions`. Määritä lopuksi arvo `OffsetQty`, joka vastaa edellisestä varauksesta vapautettujen nimikkeiden määrää. Varaus voidaan varata kokonaan tai osittain määritetyn arvon `OffsetQty` mukaisesti. Jos esimerkiksi varattiin *100* yksikköä, voit määrittää arvoksi `OffsetQty: 10`, jolloin alkuperäisestä varausmäärästä poistetaan *10* varausta.

```txt
Path:
    /api/environment/{environmentId}/onhand/unreserve
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
        reservationId: string,
        dimensions: {
            [key:string]: string,
        },
        OffsetQty: number
    }
```

Seuraavassa koodissa on esimerkki tekstisisällöstä.

```json
{
    "id": "unreserve-0",
    "organizationId": "SCM_IV",
    "reservationId": "RESERVATION_ID",
    "dimensions": {
        "siteid":"iv_postman_site",
        "locationid":"iv_postman_location",
        "ColorId": "red",
        "SizeId&quot;: &quot;small"
    },
    "OffsetQty": 1
}
```

Seuraavassa koodissa näytetään onnistuneen vastaustekstin esimerkki.

```json
{
    "reservationId": "RESERVATION_ID",
    "totalInvalidOffsetQtyByReservId": 0,
    "id": "ohoe~id-823-11744-883",
    "processingStatus": "success",
    "message": "",
    "statusCode": 200
}
```

> [!NOTE]
> Jos vastaustekstissä `OffsetQty` on pienempi tai yhtä suuri kuin varausmäärä, `processingStatus` on *success* ja `totalInvalidOffsetQtyByReservId` on *0*.
>
> Jos `OffsetQty` on suurempi kuin varattu summa, `processingStatus` on *partialSuccess* ja `totalInvalidOffsetQtyByReservId` on arvon `OffsetQty` ja varatun summan välinen ero.
>
>Jos varauksen määrä on esimerkiksi *10* ja kohdassa `OffsetQty` on arvo *12*, `totalInvalidOffsetQtyByReservId` on *2*.

### <a name="reverse-multiple-reservation-events"></a><a name="reverse-multiple-reservation-events"></a>Useiden varaustapahtumien peruuttaminen

Tämä ohjelmointirajapinta on [yhden tapahtuman ohjelmointirajapinnan](#reverse-one-reservation-event) joukkoversio.

```txt
Path:
    /api/environment/{environmentId}/onhand/unreserve/bulk
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
            reservationId: string,
            dimensions: {
                [key:string]: string,
            },
            OffsetQty: number
        }
        ...
    ]
```

## <a name="query-on-hand"></a>Käytettävissä olevan varastosaldon kysely

*Query on-hand*-ohjelmointirajapinnalla voit noutaa tuotteiden tämän hetkiset käytettävissä olevat varastosaldotiedot. Voit käyttää tätä ohjelmointirajapintaa aina, kun haluat tietää varaston määrän. Näin saattaa tapahtua esimerkiksi silloin, jos haluat tarkistaa tuotteen varastotasot sähköisen kaupankäynnin sivustossa tai tuotteen saatavuuden eri alueilla tai läheisissä myymälöissä ja varastoissa. Sovellusrajapinta tukee tällä hetkellä kyselyä, jossa on enintään 5000 yksittäistä nimikettä `productID`-arvon mukaan. Jokaisessa kyselyssä voi määrittää myös useita `siteID`- ja `locationID`-arvoja. Seuraava yhtälö määrittää enimmäisrajan:

*NumOf(SiteID) \* NumOf(LocationID) <= 100*.

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

Kun määritystä seurataan indeksointia varten, kannattaa käyttää parametria `groupByValues`. Lisätietoja on kohdassa [Tuoteindeksihierarkian määrittäminen](./inventory-visibility-configuration.md#index-configuration).

Parametri `returnNegative` määrittää, sisältävätkö tulokset negatiivisia merkintöjä.

> [!NOTE]
> Jos olet ottanut käyttöön käytössä olevan muutoksen aikataulun ja ATP-ominaisuudet, kyselysi voi sisältää myös `QueryATP` Boolean-parametrin, joka määrittää, sisältävätkö kyselyn tulokset ATP-tietoja. Lisätietoja ja esimerkkejä on kohdassa [Käytettävissä olevan varaston näkyvyyden muutosaikataulut ja luvattavissa olevat aikataulut](inventory-visibility-available-to-promise.md).

Seuraavassa esimerkissä on näytteen tekstisisältö. Tämä osoittaa, että voit tehdä kyselyn varastosaldosta useissa sijainneissa (varastoissa).

```json
{
    "dimensionDataSource": "pos",
    "filters": {
        "organizationId": ["usmf"],
        "productId": ["T-shirt"],
        "siteId": ["1"],
        "locationId": ["11","12","13"],
        "colorId": ["red"]
    },
    "groupByValues": ["colorId", "sizeId"],
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
        "locationId": ["11"],
    },
    "groupByValues": ["colorId", "sizeId"],
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

Alla on get URL -esimerkki. Tämä get-pyyntö täsmälleen sama kuin aiemmin annettu post-näyte.

```txt
/api/environment/{environmentId}/onhand?organizationId=SCM_IV&productId=iv_postman_product&siteId=iv_postman_site&locationId=iv_postman_location&colorId=red&groupBy=colorId,sizeId&returnNegative=true
```

## <a name="on-hand-exact-query"></a><a name="exact-query-with-post-method"></a>Varastosaldon tarkka kysely

Varastosaldon tarkka kysely muistuttaa tavallisia varastosaldokyselyjä, mutta niissä voi määrittää yhdistämismäärityksen hierarkian toimipaikan ja sijainnin välille. Esimerkissä käsitellään seuraavia kahta toimipaikkaa:

- Toimipaikka 1, joka on yhdistetty sijaintiin A
- Toimipaikka 2, joka on yhdistetty sijaintiin B

Jos tavallisessa varastosaldokyselyssä määritetään `"siteId": ["1","2"]` ja `"locationId": ["A","B"]`, Inventory Visibility tekee automaattisesti kyselyn tuloksista seuraavissa toimipaikoissa ja sijainneissa:

- Toimipaikka 1, sijainti A
- Toimipaikka 1, sijainti B
- Toimipaikka 2, sijainti A
- Toimipaikka 2, sijainti B

Tavallinen varastosaldokysely ei siis tunnista sitä, että sijainti A on vain toimipaikassa 1 ja sijainti B vain toimipaikassa 2. Tämän vuoksi se tekee tarpeettomia kyselyjä. Voit käyttää tätä hierarkkista yhdistämismääritystä varastosaldokyselyn avulla määrittämällä sijainnin yhdistämismääritykset kyselyn tekstiosaan. Tässä tapauksessa voit tehdä kyselyn ja vastaanottaa tulokset vain toimipaikasta 1, sijainnista A ja toimipaikasta 2, sijainnista B.

### <a name="exact-query-by-using-the-post-method"></a><a name="exact-query-with-post-method"></a>Post-menetelmää käyttävä tarkka kysely

```txt
Path:
    /api/environment/{environmentId}/onhand/exactquery
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
            dimensions: string[],
            values: string[][],
        },
        groupByValues: string[],
        returnNegative: boolean,
    }
```

Tämän pyynnön tekstiosassa `dimensionDataSource` on valinnainen parametri. Jos sitä ei ole määritetty, kohdan `filters` arvoa `dimensions` käytetään *perusdimensioina*. `filters`-parametrilla on neljä pakollista kenttää: `organizationId`, `productId`, `dimensions` ja `values`.

- `organizationId`-kentän pitäisi sisältää vain yksi arvo, mutta se on silti matriisi.
- `productId` voi sisältää yhden tai useampia arvoja. Jos se on tyhjä matriisi, kaikki tuotteet palautetaan.
- Pakollisia matriisissa `dimensions` ovat `siteId` ja `locationId`, mutta ne voivat näkyä muiden elementtien kanssa missä tahansa järjestyksessä.
- `values` voi sisältää vähintään yhden erillisen arvojen monikon, joka vastaa kohdetta `dimensions`.

`dimensions` kohteessa `filters` lisätään automaattisesti kohteeseen `groupByValues`.

Parametri `returnNegative` määrittää, sisältävätkö tulokset negatiivisia merkintöjä.

Seuraavassa esimerkissä on näytteen tekstisisältö.

```json
{
    "dimensionDataSource": "pos",
    "filters": {
        "organizationId": ["SCM_IV"],
        "productId": ["iv_postman_product"],
        "dimensions": ["siteId", "locationId", "colorId"],
        "values" : [
            ["iv_postman_site", "iv_postman_location", "red"],
            ["iv_postman_site", "iv_postman_location", "blue"],
        ]
    },
    "groupByValues": ["colorId", "sizeId"],
    "returnNegative": true
}
```

Seuraavassa esimerkissä esitetään, miten kaikista tuotteista tehdään kysely useissa sivustoissa ja sijainneissa.

```json
{
    "filters": {
        "organizationId": ["SCM_IV"],
        "productId": [],
        "dimensions": ["siteId", "locationId"],
        "values" : [
            ["iv_postman_site_1", "iv_postman_location_1"],
            ["iv_postman_site_2", "iv_postman_location_2"],
        ]
    },
    "groupByValues": ["colorId", "sizeId"],
    "returnNegative": true
}
```

## <a name="available-to-promise"></a>Luvattavissa oleva määrä (ATP)

Voit määrittää varaston näkyvyyden sallimaan tulevien käytettävissä olevien muutosten ajoituksen ja ATP-määrien laskemisen. ATP on tuotteen määrä, joka on saatavilla ja joka voidaan luvata asiakkaalle seuraavalla kaudella. ATP-laskelman käyttö voi lisätä tilauksen täyttämiskykyä merkittävästi. Tietoja siitä, miten tämä ominaisuus otetaan käyttöön ja miten varaston näkyvyys otetaan käyttöön sen API-liittymän kautta ominaisuuden käytön jälkeen, on kohdassa [Varaston näkyvyyden käytettävissä olevan varaston muutosaikataulut ja luvattavissa olevat määrät](inventory-visibility-available-to-promise.md#api-urls).

## <a name="allocation"></a>Varaus

Kohdistukseen liittyvät ohjelmointirajapinnat sijaitsevat kohdassa [Varaston näkyvyyden kohdistus](inventory-visibility-allocation.md#using-allocation-api).

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
