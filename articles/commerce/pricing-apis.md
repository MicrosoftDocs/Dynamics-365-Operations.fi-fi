---
title: Commercen hinnoittelun ohjelmointirajapinnat
description: Tässä artikkelissa käsitellään Microsoft Dynamics 365 Commerce -hinnoittelumoduulin tarjoamia hinnoittelun ohjelmointirajapintoja.
author: boycez
ms.date: 08/10/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: global
ms.author: boycez
ms.search.validFrom: 2022-07-15
ms.openlocfilehash: d694c44f6987fbf2a360869d2fb2a2fbaf0d2e4d
ms.sourcegitcommit: 924dbcdc6b03f6a7ae3a07378ec405fd15c7e359
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/13/2022
ms.locfileid: "9294111"
---
# <a name="commerce-pricing-apis"></a>Commercen hinnoittelun ohjelmointirajapinnat

[!include [banner](../includes/banner.md)]

Tässä artikkelissa käsitellään Microsoft Dynamics 365 Commerce -hinnoittelumoduulin tarjoamia hinnoittelun ohjelmointirajapintoja.

Dynamics 365 Commerce -hinnoittelumoduuli tarjoaa seuraavat Retail Server -ohjelmointirajapinnat, joita ulkoiset sovellukset voivat käyttää tukeakseen erilaisia hinnoitteluskenaarioita:

- **GetActivePrices** – Tämä ohjelmointirajapinta noutaa tuotteen lasketun hinnan, mukaan lukien yksinkertaiset alennukset.
- **CalculateSalesDocument** – Tämä ohjelmointirajapinta laskee tuotteiden hinnat ja alennukset tietyille määrille, jos tuotteet ostetaan yhdessä.
- **GetAvailablePromotions** – Tämä ohjelmointirajapinta noutaa ostoskorissa oleville tuotteille käytettävissä olevat alennukset. 
- **AddCoupons** – Tämä ohjelmointirajapinta lisää ostoskoriin kuponkeja.
- **RemoveCoupons** – Tämä ohjelmointirajapinta poistaa kuponkeja ostoskorista.

Lisätietoja Retail Server -ohjelmointirajapintojen käyttämisestä ulkoisissa sovelluksissa on kohdassa [Retail Serverin ohjelmointirajapintojen käyttäminen ulkoisissa sovelluksissa](dev-itpro/consume-retail-server-api.md).

## <a name="getactiveprices"></a>GetActivePrices

*GetActivePrices*-ohjelmointirajapinta otettiin käyttöön Commerce-versiossa 10.0.4. Tämä ohjelmointirajapinta noutaa tuotteen lasketun hinnan, mukaan lukien yksinkertaiset alennukset. Se ei laske monirivisiä alennuksia. Lisäksi se olettaa, että jokaisen ohjelmointirajapintapyyntöön sisältyvän tuotteen määrä on 1. Tämä ohjelmointirajapinta voi vastaanottaa luettelon tuotteita ja noutaa yksittäisten tuotteiden hinnan kerralla.

*GetActivePrices*-ohjelmointirajapinta tukee Commerce-rooleja **Työntekijä**, **Asiakas**, **Anonyymi** ja **Sovellus**.

*GetActivePrices*-ohjelmointirajapintaa käytetään ensisijaisesti tuotetietosivulla (PDP), jossa jälleenmyyjät haluavat esitellä tuotteen parhaan hinnan, mukaan lukien voimassa olevat alennukset.

*GetActivePrices*-ohjelmointirajapinnan syöttöparametrit on kuvattu seuraavassa taulukossa.

| Nimi                                    | Toissijainen nimi | Tyyppi | Pakollinen/valinnainen | Kuvaus |
|-----------------------------------------|----------|------|-------------------|-------------|
| projectDomain                           | | ProjectionDomain | Pakollinen | |
|                                         | ChannelId | long | Pakollinen | |
|                                         | CatalogId | long | Pakollinen | |
| productIds                              | | IEnumerable\<long\> | Pakollinen | Luettelo tuotteista, joiden hinnat lasketaan. |
| activeDate                              | | DateTimeOffset | Pakollinen | Päivämäärä, jolloin hinnat lasketaan. |
| customerId                              | | merkkijono | Valinnainen | Asiakkaan tilinumero. |
| affiliationLoyaltyTiers                 | | IEnumerable\<AffiliationLoyaltyTier\> | Valinnainen | Liitos ja kanta-asiakkuustasot. |
|                                         | AffiliationId | long | Pakollinen | Liitoksen tunnus. |
|                                         | LoyaltyTierId | long | Valinnainen | Kanta-asiakkuustason tunnus. |
| includeSimpleDiscountsInContextualPrice | | bool | Valinnainen | Määritä tämä parametrin arvoksi **true**, jos haluat sisällyttää yksinkertaiset alennukset hinnoittelun laskentaan. Oletusarvo on **epätosi**. |
| includeVariantPriceRange                | | bool | Valinnainen | Aseta tämän parametrin arvoksi **true**, jos haluat noutaa vähimmäis- ja enimmäishinnat päätuotteen kaikkien muuttujien kanssa. Oletusarvo on **epätosi**. |
| includeAttainablePricesAndDiscounts     | | bool | Valinnainen | Määritä tämän parametrin arvoksi **true**, jos haluat noutaa saavutettavissa olevat hinnat ja alennukset. Oletusarvo on **epätosi**. |

**Mallipyynnön tekstiosa**

```json
{
    "projectDomain": 
    {
        "ChannelId": 5637144592,
        "CatalogId": 0
    },
    "productIds": 
    [
        68719489871
    ],
    "activeDate": "2022-06-20T14:40:05.873+08:00",
    "includeSimpleDiscountsInContextualPrice": true,
    "includeVariantPriceRange": false
}
```

**Mallivastauksen tekstiosa**

```json
{
    "value": 
    [
        {
            "ProductId": 68719489871,
            "ListingId": 68719489871,
            "BasePrice": 0,
            "TradeAgreementPrice": 0,
            "AdjustedPrice": 0,
            "MaxVariantPrice": 0,
            "MinVariantPrice": 0,
            "CustomerContextualPrice": 0,
            "DiscountAmount": 0,
            "CurrencyCode": "USD",
            "ItemId": "82000",
            "InventoryDimensionId": null,
            "UnitOfMeasure": "ea",
            "ValidFrom": "2022-06-20T01:40:05.873-05:00",
            "ProductLookupId": 0,
            "ChannelId": 5637144592,
            "CatalogId": 0,
            "SalesAgreementPrice": 0,
            "PriceSourceTypeValue": 1,
            "DiscountLines": [],
            "AttainablePriceLines": [],
        }
    ]
}
```

## <a name="calculatesalesdocument"></a>CalculateSalesDocument

*CalculateSalesDocument*-ohjelmointirajapinta otettiin käyttöön Commerce-versiossa 10.0.25. Tämä ohjelmointirajapinta laskee tuotteiden hinnat ja alennukset tietyille määrille, jos tuotteet ostetaan yhdessä tilauksessa. *CalculateSalesDocument*-ohjelmointirajapinnan perustana oleva hintojen laskenta huomioi sekä yksiriviset että moniriviset alennukset.

*CalculateSalesDocument*-ohjelmointirajapintaa käytetään ensisijaisesti skenaarioissa, jossa ostoskorin koko konteksti ei säily (esimerkiksi myyntitarjouksissa). Myös myyntipisteessä ja Commercessa tapahtuvat skenaariot voivat hyötyä tästä käyttötavasta. Kun ostoskorin nimikkeet lasketaan joukkona (esimerkiksi erilliset niput, linkitetyt tai suositellut tuotteet tai jo ostoskoriin lisätyt tuotteet), alhaisempi kokonaishinta voi houkutella asiakasta lisäämään ostoskoriin lisää tuotteita.

*CalculateSalesDocument*-ohjelmointirajapintojen pyynnön ja vastauksen tietomalli on molemmille **Cart**. Tämän ohjelmointirajapinnan kontekstissa tietomallin nimi on kuitenkin **SalesDocument**. Koska useimmat ominaisuudet ovat valinnaisia ja vain muutamat niistä vaikuttavat hinnoittelun laskentaan, seuraavassa taulukossa näytetään vain hinnoitteluun liittyvät kentät. Emme suosittele muiden kenttien käyttämistä ohjelmointirajapintapyynnössä.

*CalculateSalesDocument*-ohjelmointirajapinta on tarkoitettu vain hintojen ja alennusten laskemiseen. Se ei huomioi veroja tai maksuja.

Seuraavassa taulukossa esitetään **salesDocument**-objektin syöttöparametrit.

| Nimi             | Toissijainen nimi | Tyyppi | Pakollinen/valinnainen | Kuvaus |
|------------------|----------|------|-------------------|-------------|
| Tunnus               | | merkkijono | Pakollinen | Myyntiasiakirjan tunniste. |
| CartLines        | | IList\<CartLine\> | Valinnainen | Luettelo riveistä, joiden hinnat ja alennukset lasketaan. |
|                  | Tuotetunnus | long | Pakollinen CartLine-objektin kontekstissa | Tuotetietueen tunnus. |
|                  | ItemId | merkkijono | Valinnainen | Nimikkeen tunniste. Jos arvo on määritetty, sen täytyy vastata **ProductId**-parametrin arvoa. |
|                  | InventoryDimensionId | merkkijono | Valinnainen | Varastodimension tunniste. Jos arvo on määritetty, **ItemId**- ja **InventoryDimensionId**-arvojen yhdistelmän täytyy vastata **ProductId**-parametrin arvoa. |
|                  | Määrä | desimaali | Pakollinen CartLine-objektin kontekstissa | Tuotteen määrä. |
|                  | UnitOfMeasureSymbol | merkkijono | Valinnainen | Tuotteen yksikkö. Jos arvoa ei ole määritetty, ohjelmointirajapinta käyttää oletusarvoisesti tuotteen myyntiyksikköä. |
| Asiakastunnus       | | merkkijono | Valinnainen | Asiakkaan tilinumero. |
| LoyaltyCardId    | | merkkijono | Valinnainen | Kanta-asiakaskortin tunniste. Kaikkien kanta-asiakaskorttiin liitettyjen asiakastilien täytyy vastata **CustomerId**-parametrin arvoa (jos se on määritetty). Kanta-asiakaskorttia ei huomioida, jos sitä ei löydy tai jos sen tila on **Estetty**. |
| AffiliationLines | | IList\<AffiliationLoyaltyTier\> | Valinnainen | Liitoksen kanta-asiakkuustasorivit. Jos **CustomerId**- ja/tai **LoyaltyCardId**-arvo on määritetty, vastaavat liitoksen kanta-asiakkuustasorivit yhdistetään **AffiliationLines**-arvossa annettujen rivien kanssa. |
|                  | AffiliationId | long | Pakollinen AffiliationLoyaltyTier-objektin kontekstissa | Liitostietueen tunnus. |
|                  | LoyaltyTierId | long | Pakollinen AffiliationLoyaltyTier-objektin kontekstissa | Kanta-asiakkuustasotietueen tunnus. |
|                  | AffiliationTypeValue | int | Pakollinen AffiliationLoyaltyTier-objektin kontekstissa | Arvo, joka ilmaisee, onko liitosrivin tyyppi **Yleinen** (**0**) vai **Kanta-asiakkuus** (**1**). Jos parametrin arvoksi on määritetty **0**, ohjelmointirajapinta ottaa **AffiliationId**-arvon tunnisteeksi ja jättää **LoyaltyTunnus**-arvon huomiotta. Jos arvoksi on määritetty **1**, ohjelmointirajapinta ottaa **LoyaltyTierId**-arvon tunnisteeksi ja jättää **AffiliationId**-arvon huomiotta. |
|                  | ReasonCodeLines | Valikoima\<ReasonCodeLine\> | Pakollinen AffiliationLoyaltyTier-objektin kontekstissa | Syykoodien rivit. Tämä parametri ei vaikuta hinnoittelun laskentaan, mutta se on pakollinen osana **AffiliationLoyaltyTier**-objektia. |
|                  | Asiakastunnus | merkkijono | Pakollinen AffiliationLoyaltyTier-objektin kontekstissa | Asiakkaan tilinumero. |
| Kupongit          | | IList\<Coupon\> | Valinnainen | Hinnoittelun laskennassa ei oteta huomioon kuponkeja, joita ei voida käyttää (jotka eivät ole aktiivisia, jotka ovat vanhentuneet tai joita ei löydy). |
|                  | Koodi | merkkijono | Pakollinen Coupon-objektin kontekstissa | Kuponkikoodi. |
|                  | CodeId | merkkijono | Valinnainen | Kuponkikoodin tunniste. Jos arvo on määritetty, sen täytyy vastata **Code**-parametrin arvoa. |
|                  | DiscountOfferId | merkkijono | Valinnainen | Alennuksen tunniste. Jos arvo on määritetty, sen täytyy vastata **Code**-parametrin arvoa. |

**Mallipyynnön tekstiosa**

```json
{
    "salesDocument": 
    {
        "Id": "CalculateSalesDocument",
        "CartLines": 
        [
            {
                "ProductId": 68719491408,
                "ItemId": "91003",
                "InventoryDimensionId": "",
                "Quantity": 1,
                "UnitOfMeasureSymbol": "ea"
            },
            {
                "ProductId": 68719493014,
                "Quantity": 2,
                "UnitOfMeasureSymbol": "ea"
            }
        ],
        "CustomerId": "3003",
        "AffiliationLines": 
        [
            {
                "AffiliationId": 68719476742,
                "LoyaltyTierId": 0,
                "AffiliationTypeValue": 0,
                "ReasonCodeLines": [],
                "CustomerId": null
            }
        ],
        "LoyaltyCardId": "55103",
        "Coupons": 
        [
            {
                "CodeId": "CODE-0005",
                "Code": "CPN0004",
                "DiscountOfferId": "ST100077"
            }
        ]
    }
}
```

Vastauksen tekstiosana palautetaan ostoskoriobjekti. Jos haluat tarkistaa hinnat ja alennukset, sinun tulisi keskittyä seuraavan taulukon kenttiin.

| Nimi           | Toissijainen nimi | Tyyppi | Kuvaus |
|----------------|----------|------|--------------|
| NetPrice       | | desimaali | Koko myyntiasiakirjan nettohinta ennen alennusten lisäämistä. |
| DiscountAmount | | desimaali | Koko myyntiasiakirjan kokonaisalennuksen summa. |
| TotalAmount    | | desimaali | Koko myyntiasiakirjan kokonaissumma. |
| CartLines      | | IList\<CartLine\> | Lasketut rivit, jotka sisältävät hintojen ja alennusten tiedot. |
|                | Hinta | desimaali | Tuotteen yksikköhinta. |
|                | NetPrice | desimaali | Rivin nettohinta ennen alennusten lisäämistä (= *Hinta* &times; *Määrä*). |
|                | DiscountAmount | desimaali | Alennuksen summa. |
|                | TotalAmount | desimaali | Rivin hinnoittelun lopullinen kokonaistulos. |
|                | PriceLines | IList\<PriceLine\> | Hintatiedot, mukaan lukien hinnan lähde (perushinta, hinnanoikaisu tai kauppasopimus) ja summa. |
|                | DiscountLines | IList\<DiscountLine\> | Alennuksen tiedot. |

## <a name="getavailablepromotions"></a>GetAvailablePromotions 

Jos ostoskorissa on useita ostoskoririvejä, *GetAvailablePromotions*-ohjelmointirajapinta palauttaa kaikki ostoskoririveille soveltuvat alennukset. 

*GetAvailablePromotions*-ohjelmointirajapintaa käytetään ensisijaisesti ostoskorisivulla, jossa vähittäismyyjät haluavat esitellä ostoskorille saatavilla olevia alennuksia tai kuponkeja.

*GetAvailablePromotions*-ohjelmointirajapinnan syöttöparametrit on kuvattu seuraavassa taulukossa.

| Nimi        | Tyyppi | Pakollinen/valinnainen | Kuvaus |
|-------------|------|-------------------|-------------|
| avain         | merkkijono | Pakollinen | Ostoskorin tunnus. |
| cartLineIds | IEnumerable\<string\> | Valinnainen | Määritä tämä parametri palauttaaksesi alennuksia vain valituille ostoskoririveille. |

**Mallivastauksen tekstiosa**

```json
{
    "value": 
    [
        {
            "LineId": "f495ffa507bc4f63a47a409cd8713dd7",
            "Promotion": {
                "OfferId": "ST100012",
                "OfferName": "Loyalty 5% off over $100",
                "PeriodicDiscountTypeValue": 4,
                "IsDiscountCodeRequired": false,
                "ValidationPeriodId": null,
                "AdditionalRestrictions": null,
                "Description": "All loyalty members get 5% with transaction total above $10 unless some exclusive or best price discounts are already applied on the transaction",
                "ValidFromDate": "2022-06-20T06:52:56.2460219Z",
                "ValidToDate": "2022-06-20T06:52:56.2460224Z",
                "CouponCodes": [],
                "ValidationPeriod": null
            }
        }
    ]
}
```

## <a name="addcoupons"></a>AddCoupons

*AddCoupons*-ohjelmointirajapinta tukee kuponkiluettelon lisäämistä ostoskoriin. Se palauttaa ostoskoriobjektin, kun kupongit on lisätty.

*AddCoupons*-ohjelmointirajapinnan syöttöparametrit on kuvattu seuraavassa taulukossa.

| Nimi                 | Tyyppi | Pakollinen/valinnainen | Kuvaus |
|----------------------|------|-------------------|-------------|
| avain                  | merkkijono | Pakollinen | Ostoskorin tunnus. |
| couponCodes          | IEnumerable\<string\> | Pakollinen | Ostoskoriin lisättävät kuponkikoodit. |
| isLegacyDiscountCode | bool | Valinnainen | Määritä tämän parametrin arvoksi **true** osoittaaksesi, että kuponki on vanha alennuskoodi. Oletusarvo on **epätosi**. |

## <a name="removecoupons"></a>RemoveCoupons

*RemoveCoupons*-ohjelmointirajapinta tukee kuponkiluettelon poistamista ostoskorista. Se palauttaa ostoskoriobjektin, kun kupongit on poistettu.

*RemoveCoupons*-ohjelmointirajapinnan syöttöparametrit on kuvattu seuraavassa taulukossa.

| Nimi        | Tyyppi | Pakollinen/valinnainen | Kuvaus |
|-------------|------|-------------------|-------------|
| avain         | merkkijono | Pakollinen | Ostoskorin tunnus. |
| couponCodes | IEnumerable\<string\> | Pakollinen | Ostoskorista poistettavat kuponkikoodit. |

[!INCLUDE[footer-include](../includes/footer-banner.md)]
