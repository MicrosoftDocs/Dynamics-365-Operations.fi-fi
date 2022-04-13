---
title: Varaston näkyvyyden käytössä olevat muutosaikataulut ja luvattavissa olevat määrät
description: Tässä aiheessa kuvataan, kuinka voidaan ajoittaa tulevia käytettävissä olevan määrän muutoksia ja laskea luvattavissa olevat (ATP) määrät.
author: yufeihuang
ms.date: 03/04/2022
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2022-03-04
ms.dyn365.ops.version: 10.0.26
ms.openlocfilehash: 7ce868871f093fd734a466bb8a06c5782bf83302
ms.sourcegitcommit: a3b121a8c8daa601021fee275d41a95325d12e7a
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2022
ms.locfileid: "8525881"
---
# <a name="inventory-visibility-on-hand-change-schedules-and-available-to-promise"></a>Varaston näkyvyyden käytössä olevat muutosaikataulut ja luvattavissa olevat määrät

[!include [banner](../includes/banner.md)]

Tässä ohjeaiheessa kuvataan, kuinka *Käytössä oleva muutosaikataulu* -ominaisuus määritetään tulevien ajankohtaisten muutosten ajoittamiseksi ja ATP-määrien laskemiseksi. ATP on tuotteen määrä, joka on saatavilla ja joka voidaan luvata asiakkaalle seuraavalla kaudella. Tämän laskelman käyttö voi lisätä tilauksen täyttämiskykyä merkittävästi.

Monille valmistajille, jälleenmyyjille tai myyjille ei riitä, että vain tietää, mitä on käytettävissä. Niillä on oltava täysi näkyvyys tulevaan käytettävyyteen. Tämän tulevan saatavuuden tulisi ottaa huomioon tuleva toimitus, tuleva kysyntä ja ATP.

## <a name="enable-and-set-up-the-features"></a><a name="setup"></a>Ominaisuuksien ottaminen käyttöön ja määrittäminen

Ennen ATP:n käyttöä on määritettävä vähintään yksi laskettu mitta ATP-määrien laskemiseksi. Ominaisuus on otettava myös käyttöön ja määritettävä ATP-asetukset Microsoft Power Appsissa

### <a name="set-up-calculated-measures-for-atp-quantities"></a>ATP-määreiden lasketut määreet

Laskettu *ATP-mitta* on ennalta määritetty laskettu määre, jota käytetään yleensä saatavissa olevan käytettävissä olevan määrän etsimiseksi. Sen lisäysmuutosmääreiden summa on tarjontamäärä ja sen vähennysmuutosmääreiden summa on kysyntämäärä.

Voit laskea ATP-määriä lisäämällä useita laskettuja määreitä. Kaikkien ATP-laskettujen määreiden kokonaismäärän pitäisi kuitenkin olla alle yhdeksän.

Voit esimerkiksi määrittää seuraavan lasketun määreen:

**Käytettävissä oleva varasto** = (*PhysicalInvent* + *OnHand* + *Unrestricted* + *QualityInspection* + *Inbound*) – (*ReservPhysical* + *SoftReservePhysical* + *Outbound*)

(*PhysicalInvent* + *OnHand* + *Unrestricted* + *QualityInspection* + *Inbound*) -määrä kuvaa tarjontaa ja (*ReservPhysical* + *SoftReservePhysical* + *Outbound*) -määrä kuvaa kysyntää. Lasketun määreen voi näin ollen ymmärtää seuraavasti:

**Käytettävissä oleva varasto** = *Tarjonta* – *Kysyntä*

Lisätietoja lasketuista mittareista on kohdassa [Lasketut mittarit](inventory-visibility-configuration.md#calculated-measures).

### <a name="turn-on-the-on-hand-change-schedule-feature-and-configure-atp-settings"></a>Ota käyttöön käytössä olevan muutoksen ajoitustoiminto ja määritä ATP-asetukset

Seuraavia vaiheita noudattamalla voit ottaa käyttöön *käytössä olevan muutoksen ajoitus* -ominaisuuden Power Appsissa ja määrittää ATP-asetukset.

1. Kirjaudu Power Appsiin ja avaa Varaston näkyvyys.
1. Avaa **Määritykset**-sivu.
1. Ota *OnhandChangeSchedule*-ominaisuus käyttöön **Ominaisuuksien hallinta** -välilehdessä.
1. Valitse **ATP-asetukset**-välilehti.
1. Kun teet kyselyn varaston näkyvyydestä, tuloksena on tulos, joka sisältää jokaisen tähän lisättävän ATP-lasketun mitan. Valitse **Lisää** lisätäksesi uuden lasketun mittarin APT:hen.
1. Määritä seuraavat kentät:

    - **Tietolähde** – Valitse laskettuun mittaan liittyvä tietolähde.
    - **Laskettu mitta** – Valitse valittuun tietolähteeseen liittyvä lasketun mitan määrä, jota haluat käyttää käytettävissä olevan varastomäärän etsimiseen.
    - **Aikataulutuskausi** – Määritä, kuinka monta päivää käyttäjät voivat tarkastella ja lähettää ajoitettuja käytettävissä olevan määrän muutoksia, kun valittua laskettua mittaria käytetään. Varastotietoja kyselevät käyttäjät saavat käytettävissä olevan varaston määrän, ajoitetut käytettävissä olevan varaston muutokset ja ATP-tiedon jokaista tämän kauden päivää kohden kuluvasta päivämäärästä alkaen. Valitse kokonaisluku väliltä 1 – 7.

    > [!IMPORTANT]
    > Aikataulukausi sisältää nykyisen päivämäärän. Siksi käyttäjät voivat ajoittaa käytettävissä olevan varastoajan muutoksia milloin tahansa kuluvasta päivästä alkaen (muutospäivämäärä) tulevana päivänä (aikataulutuskausi – 1).

1. Valitse **Tallenna**.
1. Toista vaiheet 5 - 7, kunnes olet lisännyt kaikki ATP:hen vaadittavat laskettavat mitat.
1. Kun olet määrittänyt kaikki tarvittavat asetukset, valitse **Päivityskonfiguraatio**.

Lisätietoja on kohdassa [Viimeistele ja päivitä määritys](inventory-visibility-configuration.md).

## <a name="how-the-on-hand-change-schedule-and-atp-calculations-work"></a>Miten käytössä oleva muutosaikataulu ja ATP-laskelmat toimivat

*Käytettävissä oleva muutossuunnitelma* näyttää suunniteltujen varastomuutosten odotetut päivämäärät ja määrät. Voit lähettää käytettävissä olevan varaston näkyvyyden muutosaikataulun, jos päivämäärät ovat **ajoituskauden** asetuksen määrittämän kauden sisällä (katso [Ota käyttöön ja määritä ominaisuudet](#setup) -osa). Varastotietoja kyselevät käyttäjät saavat käytettävissä olevan varaston määrän, ajoitetut käytettävissä olevan varaston muutokset ja ATP-tiedon tämän kauden kunakin päivänä.

Ajoitetut muutokset ovat aluksi sitomattomia, eivätkä ne siksi vaikuta todellisiin, järjestelmän käytettävissä oleviin määriin. Muutokset voi tehdä lähettämällä *käytettävissä olevan vaihtotapahtuman*, joka päivittää todellisen käytettävissä olevan varastomäärän. Tämän jälkeen ajoitettu muutos on muutettava lähettämällä vastaavalle negatiiviselle määrälle käytettävissä olevan muutoksen aikataulu.

Teet esimerkiksi tilauksen kymmenestä pyörästä ja odotat sen saapuvan huomenna. Näin ollen lähetät käytettävissä olevan vaihtoaikataulun, jonka saapuva määrä on 10 ja jonka päivämäärä on huominen. Kun tilaus saapuu seuraavana päivänä, lisäät sen fyysiseen käytettävissä olevaan varastoon. Muutos on sitten tehtävä järjestelmään, jotta todellinen käytettävissä oleva määrä päivittyy. Voit tehdä muutoksen lähettämällä käytettävissä olevan vaihtotapahtuman, jonka saapuva määrä on 10. Tämän jälkeen ajoitettu muutos muutetaan lähettämällä ajantasainen muutosaikataulu, jonka saapuvien määrä on -10.

Kun teet kyselyn käytettävissä olevan varaston ja ATP-määrän varastonäkyvyydestä, se palauttaa seuraavat tiedot jokaista aikataulukauden päivää varten:

- **Päivämäärä** – Kirjoita viimeinen päivämäärä, johon tulos liittyy.
- **Käytettävissä oleva määrä** – Todellinen käytettävissä oleva määrä määritettynä päivämääränä. Tämä laskelma tehdään varaston näkyvyyttä varten määritetyn ATP:n lasketun mitan mukaan.
- **Ajoitettu toimitus** – Niiden suunniteltujen saapuvien määrien summa, jotka eivät ole fyysisesti käytettävissä välitöntä kulutusta tai lähetystä varten määritettynä päivämääränä.
- **Ajoitettu kysyntä** – Kaikkien ajoitettujen lähtevien määrien summa, joita ei ole kulutettu tai lähetetty määritettynä päivämääränä.
- **ATP-määrä** – Pienin arvioitu käytettävissä oleva määrä, joka on käytettävissä määritetystä päivämäärästä ajoituskauden loppuun saakka. Tämä määrä sisältää kaikki ajoitetun määrän oikaisut. Se on enimmäismäärä, joka voidaan luvata kuluvana päivänä toimitusta tai kulutusta varten tuona päivänä.

Jos nykyinen päivämäärä on esimerkiksi 1.2.2022 ja aikataulukausi on 7, käyttäjät voivat lähettää ajoitettuja käytettävissä olevia varastomuutoksia, joiden odotetaan tapahtuvan 1.2.–7.2.2022. Tällöin esimerkiksi 3. helmikuuta päivälle laskettu ATP-määrä lasketaan tämän päivän käytettävissä olevan määrän ja ajoitettujen määrien perusteella 3.2. - 7.2.

## <a name="example"></a>Esimerkki

Seuraavassa esimerkissä kerrotaan, miten ajoitettujen määrän muutosten sarja vaikuttaa varaston näkyvyysraporttien käytettävissä olevan varaston määriin ja ATP-määriin. Siinä kerrotaan myös, miten ajoitettu muutosvahvistus tehdään, miten sidottu aikataulun muutos vaikuttaa tuloksiin ja mitä tuloksia voi tapahtua, jos ajoitettua muutosta ei vahvisteta.

Tämän esimerkin tuloksissa näkyy *arvioitu käytettävissä oleva* arvo. Tämä arvo sisältää kaikki ajoitetut päivitykset havainnollistusta varten, mutta sitä ei todellisuudessa raportoida varaston näkyvyyskyselyn yhteydessä.

1. Seuraavat asetukset on määritetty järjestelmääsi varten **ATP-asetukset**-sivulla Power Appsissa:

    - **ATP:n laskettu mitta** – Käytössä on laskettu mittari, jonka nimi on *käytettävissä*. Sen laskentaan seuraavasti *käytettävissä oleva = tarjonta – kysyntä*. Voit valita tämän mitan tässä.
    - **Aikataulukausi** – valitset *7*.

1. Seuraavat ehdot myös pätevät:

    - Nykyinen päivämäärä on 1. helmikuuta 2022.
    - Nykyinen käytettävissä oleva määrä on 20.

1. Kuluvana päivänä (1.2.2022) lähetät varaston näkyvyyteen suunnitellun tarvemäärän 3. Tällöin arvioitu käytettävissä oleva määrä on 17 nimikettä. Tulokset ovat seuraavassa taulukossa.

    | Päivämäärä | Käytettävissä oleva | Ajoitettu toimitus | Ajoitettu kysyntä | Arvioitu käytettävissä oleva varasto | ATP |
    | --- | --- | --- | --- | --- | --- |
    | 1.2.2022 | 20 | | 3 | 17 | 17 |
    | 2.2.2022 | 20 | | | 17 | 17 |
    | 3.2.2022 | 20 | | | 17 | 17 |
    | 4.2.2022 | 20 | | | 17 | 17 |
    | 5.2.2022 | 20 | | | 17 | 17 |
    | 6.2.2022 | 20 | | | 17 | 17 |
    | 7.2.2022 | 20 | | | 17 | 17 |

1. Kuluvana päivänä (1. helmikuuta 2022) lähetät 3.2.2022 ajoitetun toimituksen, jonka määrä on 10. Tulokset ovat seuraavassa taulukossa.

    | Päivämäärä | Käytettävissä oleva | Ajoitettu toimitus | Ajoitettu kysyntä | Arvioitu käytettävissä oleva varasto | ATP |
    | --- | --- | --- | --- | --- | --- |
    | 1.2.2022 | 20 | | 3 | 17 | 17 |
    | 2.2.2022 | 20 | | | 17 | 17 |
    | 3.2.2022 | 20 | 10 | | 27 | 27 |
    | 4.2.2022 | 20 | | | 27 | 27 |
    | 5.2.2022 | 20 | | | 27 | 27 |
    | 6.2.2022 | 20 | | | 27 | 27 |
    | 7.2.2022 | 20 | | | 27 | 27 |

1. Kuluvana päivänä (1.2.2022) lähetät seuraavat ajoitetun määrän muutokset:

    - 4. helmikuuta 2022 tarvemäärä 15
    - 5. helmikuuta 2022 toimitusmäärä 1
    - 6. helmikuuta 2022 tarvemäärä 3

    Tulokset ovat seuraavassa taulukossa.

    | Päivämäärä | Käytettävissä oleva | Ajoitettu toimitus | Ajoitettu kysyntä | Arvioitu käytettävissä oleva varasto | ATP |
    | --- | --- | --- | --- | --- | --- |
    | 1.2.2022 | 20 | | 3 | 17 | 12 |
    | 2.2.2022 | 20 | | | 17 | 12 |
    | 3.2.2022 | 20 | 10 | | 27 | 12 |
    | 4.2.2022 | 20 | | päivänä | 12 | 12 |
    | 5.2.2022 | 20 | 1 | | 13 | 13 |
    | 6.2.2022 | 20 | 3 | | 16 | 16 |
    | 7.2.2022 | 20 | | | 16 | 16 |

1. Kuluvana päivänä (1.2.2022) lähetät ajoitetun määrän, joka on 3. Tämä muutos on näin ollen tehtävä, jotta se heijastuu todelliseen käytettävissä olevaan määrään. Voit tehdä muutoksen lähettämällä käytettävissä olevan vaihtotapahtuman, jonka lähtevä määrä on 3. Tämän jälkeen ajoitettu muutos muutetaan lähettämällä ajantasainen muutosaikataulu, jonka lähtevien määrä on -3. Tulokset ovat seuraavassa taulukossa.

    | Päivämäärä | Käytettävissä oleva | Ajoitettu toimitus | Ajoitettu kysyntä | Arvioitu käytettävissä oleva varasto | ATP |
    | --- | --- | --- | --- | --- | --- |
    | 1.2.2022 | 17 | | 0 | 17 | 12 |
    | 2.2.2022 | 17 | | | 17 | 12 |
    | 3.2.2022 | 17 | 10 | | 27 | 12 |
    | 4.2.2022 | 17 | | päivänä | 12 | 12 |
    | 5.2.2022 | 17 | 1 | | 13 | 13 |
    | 6.2.2022 | 17 | 3 | | 16 | 16 |
    | 7.2.2022 | 17 | | | 16 | 16 |

1. Seuraavana päivänä (2.2.2022) aikataulukausi siirtyy eteenpäin yhdellä päivällä. Tulokset ovat seuraavassa taulukossa.

    | Päivämäärä | Käytettävissä oleva | Ajoitettu toimitus | Ajoitettu kysyntä | Arvioitu käytettävissä oleva varasto | ATP |
    | --- | --- | --- | --- | --- | --- |
    | 2.2.2022 | 17 | | | 17 | 12 |
    | 3.2.2022 | 17 | 10 | | 27 | 12 |
    | 4.2.2022 | 17 | | päivänä | 12 | 12 |
    | 5.2.2022 | 17 | 1 | | 13 | 13 |
    | 6.2.2022 | 17 | 3 | | 16 | 16 |
    | 7.2.2022 | 17 | | | 16 | 16 |
    | 8.2.2022 | 17 | | | 16 | 16 |

1. Kaksi päivää myöhemmin (4. helmikuuta 2022) 3. helmikuuta ajoitettu toimitusmäärä 10 ei ole kuitenkaan saapunut. Tulokset ovat seuraavassa taulukossa.

    | Päivämäärä | Käytettävissä oleva | Ajoitettu toimitus | Ajoitettu kysyntä | Arvioitu käytettävissä oleva varasto | ATP |
    | --- | --- | --- | --- | --- | --- |
    | 4.2.2022 | 17 | | päivänä | 2 | 2 |
    | 5.2.2022 | 17 | 1 | | 3 | 3 |
    | 6.2.2022 | 17 | 3 | | 6 | 6 |
    | 7.2.2022 | 17 | | | 6 | 6 |
    | 8.2.2022 | 17 | | | 6 | 6 |
    | 9.2.2022 | 17 | | | 6 | 6 |
    | 10.2.2022 | 17 | | | 6 | 6 |

    Ajoitetut (mutta ei sidotut) käytettävissä olevan määrän muutokset eivät vaikuta todelliseen käytettävissä olevaan varastomäärään.

## <a name="submit-change-schedules-change-events-and-atp-queries-through-the-api"></a><a name="api-urls"></a>Muutosaikataulujen, muutostapahtumien ja ATP-kyselyiden lähettäminen ohjelmointirajapinnan kautta

Seuraavien ohjelmointirajapinta (API) -URL-osoitteiden avulla voit lähettää käytettävissä olevan vaihto-ohjelman muutosaikatauluja, muutostapahtumia ja kyselyitä.

| Polku | Tapa | Kuvaus |
| --- | --- | --- |
| `/api/environment/{environmentId}/on-hand/changeschedule` | `POST` | Yhden aikataulutetun käytettävissä olevan varastosaldon muutoksen luominen. |
| `/api/environment/{environmentId}/on-hand/changeschedule/bulk` | `POST` | Useiden aikataulutettujen käytössä olevien varastosaldojen muutosten luominen. |
| `/api/environment/{environmentId}/onhand` | `POST` | Yhden käytössä olevan varastosaldon muutostapahtuman luominen. |
| `/api/environment/{environmentId}/onhand/bulk` | `POST` | Useiden muutostapahtumien luominen. |
| `/api/environment/{environmentId}/onhand/indexquery` | `POST` | `POST`-menetelmää käyttävä kysely. |
| `/api/environment/{environmentId}/onhand` | `GET` | `GET`-menetelmää käyttävä kysely. |

Lisätietoja on kohdassa [Varaston näkyvyyden julkiset API:t](inventory-visibility-api.md).

### <a name="submit-on-hand-change-schedules"></a>Käytössä olevien varastomuutosten aikataulujen lähettäminen

Käytettävissä olevan varaston muutosaikataulut tehdään lähettämällä `POST`-pyyntö asiaankuuluvaan varaston näkyvyyspalvelun URL-osoitteeseen (katso [Muutosaikataulujen lähettäminen, muutostapahtumat ja ATP-kyselyt ohjelmointirajapinnan kautta](#api-urls) osa). Voit myös lähettää joukkopyyntöjä.

Ajantasaisen muutosaikataulun lähettämiseksi pyynnön rungon on sisällettävä organisaatiotunnus, tuotetunnus, ajoitettu päivämäärä ja määrät päivämäärän mukaan. Ajoitetun päivämäärän on oltava kuluvan päivämäärän ja nykyisen ajoituskauden lopun välissä.

#### <a name="example-request-body-that-contains-a-single-update"></a>Yksittäisen päivityksen sisältävä esimerkkipyynnön teksti

Seuraava esimerkki näyttää yksittäisen päivityksen sisältävän esimerkkipyynnön tekstin.

```json
# Url
# replace {RegionShortName} and {EnvironmentId} with your value
https://inventoryservice.{RegionShortName}-il301.gateway.prod.island.powerapps.com/api/environment/{EnvironmentId}/on-hand/changeschedule

# Method
Post

# Header
# Replace {access_token} with the one from your security service
Api-version: "1.0"
Content-Type: "application/json"
Authorization: "Bearer {access_token}"

# Body
{
    "id": "id-bike-0001",
    "organizationId": "usmf",
    "productId": "Bike",
    "dimensions": {
        "SiteId": "1",
        "LocationId": "11",
        "ColorId": "Red",
        "SizeId": "Small"
    },
    "quantitiesByDate":
    {
        "2022/02/01": // today
        {
            "pos":{
                "inbound": 10,
            },
        },
    },
}
```

#### <a name="example-request-body-that-contains-multiple-bulk-updates"></a>Useita päivityksiä (joukkopäivitys) sisältävä esimerkkipyynnön teksti

Seuraava esimerkki näyttää useita päivityksiä (joukkopäivitys) sisältävän esimerkkipyynnön tekstin.

```json
# Url
# replace {RegionShortName} and {EnvironmentId} with your value
https://inventoryservice.{RegionShortName}-il301.gateway.prod.island.powerapps.com/api/environment/{EnvironmentId}/on-hand/changeschedule/bulk

# Method
Post

# Header
# replace {access_token} with the one from your security service
Api-version: "1.0"
Content-Type: "application/json"
Authorization: "Bearer {access_token}"

[
    {
        "id": "id-bike-0001",
        "organizationId": "usmf",
        "productId": "Bike",
        "dimensions": {
            "SiteId": "1",
            "LocationId": "11",
            "ColorId": "Red",
            "SizeId": "Small"
        },
        "quantitiesByDate":
        {
            "2022/02/01": // today
            {
                "pos":{
                    "inbound": 10,
                },
            },
        },
    },
    {
        "id": "id-bike-0002",
        "organizationId": "usmf",
        "productId": "Car",
        "dimensions": {
            "SiteId": "1",
            "LocationId": "11",
            "ColorId": "Red",
            "SizeId": "Small"
        },
        "quantitiesByDate":
        {
            "2022/02/05":
            {
                "pos":{
                    "outbound": 10,
                },
            },
        },
    }
]
```

### <a name="submit-on-hand-change-events"></a>Käytettävissä olevan varastosaldon muutostapahtumien lähettäminen

Käytettävissä olevan varaston muutostapahtumat tehdään lähettämällä `POST`-pyyntö asiaankuuluvaan varaston näkyvyyspalvelun URL-osoitteeseen (katso [Muutosaikataulujen lähettäminen, muutostapahtumat ja ATP-kyselyt ohjelmointirajapinnan kautta](#api-urls) osa). Voit myös lähettää joukkopyyntöjä.

> [!NOTE]
> Käytettävissä olevan varaston muutoksen tapahtumat eivät ole yksilöllisiä ATP-toiminnoille, vaan ne kuuluvat varaston vakionäkyvyyden sovellusliittymään. Tämä esimerkki on sisällytetty, koska tapahtumat ovat merkityksellisiä, kun työskentelet ATP:n kanssa. Käytettävissä olevan varastomuutosten tapahtumat muistuttavat käytettävissä olevan varastomuutosten varauksia, mutta tapahtumasanomat on lähetettävä eri sovellusliittymän URL-osoitteeseen ja tapahtumat, joissa käytetään `quantities`-määritettä `quantityByDate`n sijaan sanoman rungossa. Lisätietoja käytettävissä olevan varaston muutostapahtumista ja muista Varaston näkyvyys -ohjelmointirajapinnan ominaisuuksista on ohjeaiheessa [Varaston näkyvyys -ohjelmointirajapinnat](inventory-visibility-api.md).

Käytettävissä olevan muutostapahtuman lähettämiseksi pyynnön rungon on sisällettävä organisaatiotunnus, tuotetunnus, ajoitettu päivämäärä ja määrät päivämäärän mukaan. Ajoitetun päivämäärän on oltava kuluvan päivämäärän ja nykyisen ajoituskauden lopun välissä.

Seuraava esimerkki näyttää yksittäisen käytettävissä olevan muutostapahtuman sisältävän esimerkkipyynnön tekstin.

```json
# Url
# replace {RegionShortName} and {EnvironmentId} with your value
https://inventoryservice.{RegionShortName}-il301.gateway.prod.island.powerapps.com/api/environment/{EnvironmentId}/onhand

# Method
Post

# Header
# Replace {access_token} with the one from your security service
Api-version: "1.0"
Content-Type: "application/json"
Authorization: "Bearer {access_token}"

# Body
{
    "id": "id-bike-0001",
    "organizationId": "usmf",
    "productId": "Bike",
    "dimensions": {
        "SiteId": "1",
        "LocationId": "11",
        "SizeId": "Big",
        "ColorId": "Red",
    },
    "quantities": {
        "pos": {
            "inbound": 10.0
        }
    }
}
```

## <a name="query-the-scheduled-on-hand-changes-and-atp-results"></a>Ajoitettujen käytössä olevien varastomuutosten ja ATP-tulosten kysely

Voit tehdä ajoitettujen varastomuutosten ja ATP-tulosten kyselyn lähettämällä joko `POST`-pyynnön tai `GET`-pyynnön asianmukaiseen API-URL-osoitteeseen (katso [Muutosaikataulujen lähettäminen, muutostapahtumat ja ATP-kyselyt ohjelmointirajapintojen avulla](#api-urls) -osa).

Valitse `QueryATP`-pyyntösi arvoksi *Tosi*, jos haluat kysellä ajoitettuja käytössä olevan varaston muutoksia ja ATP-tuloksia.

- Jos lähetät pyynnön `GET`-menetelmällä, määritä tämä parametri URL-osoitteeseen.
- Jos lähetät pyynnön `POST`-menetelmällä, määritä tämä parametri pyynnön runkoon.

> [!NOTE]
> Riippumatta siitä, onko `returnNegative`-parametrin pyyntöosaosassa *tosi* vai *epätosi*, tulos sisältää negatiiviset arvot, kun ajoitettuja käytössä olevan varaston muutoksia ja ATP-tuloksia pyydetään. Nämä negatiiviset arvot sisällytetään, koska jos vain tarvetilaukset ajoitetaan tai jos toimitusmäärät ovat pienempiä kuin tarvemäärät, ajoitetut käytettävissä olevan määrän muutosmäärät ovat negatiivisia. Jos negatiivisia arvoja ei sisällytetä, tulokset voivat aiheuttaa sekaannuksia. Lisätietoja tästä vaihtoehdosta ja sen toiminnasta muun tyyppisissä kyselyissä on ohjeaiheessa [Varaston näkyvyys julkisissa ohjelmointirajapinnoissa](inventory-visibility-api.md).

### <a name="post-method-example"></a>POST-menetelmäesimerkki

Seuraavassa esimerkissä kerrotaan, miten luodaan pyyntöosa, joka voidaan lähettää varaston läpinäkyvyyteen `POST`-menetelmällä.

```json
# Url
# replace {RegionShortName} and {EnvironmentId} with your value
https://inventoryservice.{RegionShortName}-il301.gateway.prod.island.powerapps.com/api/environment/{EnvironmentId}/on-hand/indexquery

# Method
Post

# Header
# replace {access_token} with the one from your security service
Api-version: "1.0"
Content-Type: "application/json"
Authorization: "Bearer {access_token}"

# Body
{
    "filters": {
        "organizationId": ["usmf"],
        "productId": ["Bike"],
        "siteId": ["1"],
        "LocationId": ["11"],
    },
    "groupByValues": ["ColorId", "SizeId"],
    "returnNegative": true,
    "QueryATP":true,
}
```

### <a name="get-method-example"></a>GET-menetelmäesimerkki

Seuraavassa esimerkissä kerrotaan, miten pyynnön URL-osoite luodaan `GET`-pyynnöksi.

```txt
https://inventoryservice.{RegionShortName}-il301.gateway.prod.island.powerapps.com/api/environment/{EnvironmentId}/onhand?organizationId=usmf&productId=Bike&SiteId=1&groupBy=ColorId,SizeId&returnNegative=true&QueryATP=true
```

Tämän `GET`-pyynnön tulos on täsmälleen sama kuin edellisen esimerkin `POST`-pyynnön tulos.

### <a name="query-result-example"></a>Kyselyn tuloksen esimerkki

Molemmat aiemmista kyselyesimerkeistä voivat tuottaa seuraavan vastauksen. Tässä esimerkissä järjestelmä on määritetty seuraavilla asetuksilla:

- **ATP laskettu mittari:** *iv.onhand = pos.inbound – pos.outbound*
- **Ajoita kausi:** *7*

Esimerkki vastauksen rungosta.

```json
[
    {
        "quantitiesByDate": {
            "2022-02-02T00:00:00": {
                "pos": {
                    "outbound": 5,
                    "inbound": 0,
                },
                "iv": {
                    "onhand": -5,
                },
            },
            "2022-02-06T00:00:00": {
                "pos": {
                    "inbound": 7,
                    "outbound": 0,
                },
                "iv": {
                    "onhand": 7,
                },
            }
        },
        "atpQuantities": {
            "2022-02-01T00:00:00Z": {
                "iv": {
                    "onhand": 5.0
                }
            },
            "2022-02-02T00:00:00Z": {
                "iv": {
                    "onhand": 5.0
                }
            },
            "2022-02-03T00:00:00Z": {
                "iv": {
                    "onhand": 5.0
                }
            },
            "2022-02-04T00:00:00Z": {
                "iv": {
                    "onhand": 5.0
                }
            },
            "2022-02-05T00:00:00Z": {
                "iv": {
                    "onhand": 5.0
                }
            },
            "2022-02-06T00:00:00Z": {
                "iv": {
                    "onhand": 12.0
                }
            },
            "2022-02-07T00:00:00Z": {
                "iv": {
                    "onhand": 12.0
                }
            }
        },
        "productId": "Bike ",
        "dimensions": {
            "ColorId": "Red",
            "SizeId": "Big",
            "siteid": "1",
            "locationid": "11"
        },
        "quantities": {
            "pos": {
                "inbound": 10.0,
                "outbound": 0,
            },
            "iv": {
                "onhand": 10.0,
            }
        }
    }
]
```
