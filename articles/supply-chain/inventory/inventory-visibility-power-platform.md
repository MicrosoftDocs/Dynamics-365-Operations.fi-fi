---
title: Varaston näkyvyyssovellus
description: Tässä aiheessa käsitellään varaston näkyvyyssovelluksen käyttämistä.
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
ms.openlocfilehash: cc09dd82547ec42041889e9a96662cd17549a3ea
ms.sourcegitcommit: b9c2798aa994e1526d1c50726f807e6335885e1a
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/13/2021
ms.locfileid: "7344999"
---
# <a name="inventory-visibility-app"></a>Varaston näkyvyyssovellus

[!include [banner](../includes/banner.md)]
[!INCLUDE [cc-data-platform-banner](../../includes/cc-data-platform-banner.md)]

Tässä aiheessa käsitellään varaston näkyvyyssovelluksen käyttämistä.

Varaston näkyvyys on mallipohjainen visualisointisovellus. Sovelluksessa on kolme sivua: **Määritys**, **Toiminnon aikainen näkyvyys** ja **Varaston yhteenveto**. Siinä on seuraavat ominaisuudet:

- Se toimii käyttöliittymänä, jossa voi määrittää käytettävissä olevan varaston ja alustavan varauksen.
- Se tukee reaaliaikaisia käytettävissä olevan varaston kyselyjä erilaisten dimensioyhdistelmien avulla.
- Se toimii käyttöliittymänä, jolla voi kirjata varastopyyntöjä.
- Se antaa mukautetun näkymän tuotteiden käytettävissä olevasta varastosta ja kaikista dimensioista.

## <a name="prerequisites"></a>Edellytykset

Varaston näkyvyyden apuohjelma on asennettava ja määritettävä ennen aloittamista kohdassa [Varaston näkyvyyden määrittäminen](inventory-visibility-setup.md) kuvatulla tavalla.

## <a name="configuration"></a><a name="configuration"></a>Määritys

**Määritys**-sivu auttaa määrittämään käytettävissä olevan varaston ja alustavan varauksen. Kun apuohjelma on asennettu, oletusmääritys sisältää Microsoft Dynamics 365 Supply Chain Managementin arvon (`fno`-tietolähde). Oletusasetus voidaan tarkistaa. Määritystä voidaan lisäksi muokata liiketoimintatarpeiden ja ulkoisen järjestelmän varastokirjaustarpeiden mukaan [Dataversessa](/powerapps/maker/common-data-service/data-platform-intro) siten, että useissa järjestelmissä käytetään standardoitua varastomuutosten kirjausta, järjestämistä ja kyselyä.

### <a name="define-data-sources"></a>Tietolähteiden määrittäminen

Kukin varaston näkyvyyssovelluksella integroitava *tietolähde* on määritettävä. Varaston näkyvyyssovellus tukee erilaisten tietolähteiden, kuten myyntipistejärjestelmän, Supply Chain Managementin ja muiden ulkoisten järjestelmien, integrointia. Supply Chain Management määritetään oletusarvoisesti varaston näkyvyyssovelluksen oletustietolähteeksi (`fno`).

Tietolähde lisätään seuraavasti:

1. Kirjaudu Power Apps -ympäristöön ja avaa **Varaston näkyvyys**.
1. Avaa **Määritykset**-sivu.
1. Lisää tietolähde valitsemalla **Tietolähde**-välilehdessä **Uusi tietolähde**.

> [!NOTE]
> Tietolähdettä lisättäessä tietolähteen nimi, fyysiset mitat ja dimensioiden yhdistämismääritykset on tarkistettava ennen määrityksen päivittämistä varaston näkyvyyspalveluun. Näitä asetuksia ei voi muokata sen jälkeen, kun **Päivitä määritys** on valittu.

### <a name="set-up-dimension-mappings"></a>Dimension yhdistämismääritysten määrittäminen

Varaston näkyvyyssovelluksessa on luettelo perusdimensioita, jotka voidaan yhdistää tietolähteen dimensioista. Yhdistämismäärityksissä on käytettävissä 33 dimensiota.

- Jos yhtenä tietolähteenä on Supply Chain Management, 13 dimensiota yhdistetään oletusarvoisesti Supply Chain Managementin vakiodimensioihin. 12 muuta dimensiosta (`inventDimension1`– `inventDimension12`) yhdistetään Supply Chain Managementin mukautettuihin dimensioihin. Loput kahdeksan dimensiota ovat laajennettuja dimensioita, jotka voidaan yhdistää ulkoisiin tietolähteisiin.
- Jos Supply Chain Managementia ei käytetä yhtenä tietolähteenä, dimensiot voidaan yhdistää vapaasti. Seuraavassa taulukossa on käytettävissä olevien dimensioiden täydellinen luettelo.

> [!NOTE]
> Jos dimensio ei ole oletusdimensioluettelossa ja käytössä on ulkoinen tietolähde, yhdistämismäärityksessä kannattaa käyttää dimensioita `ExtendedDimension1`–`ExtendedDimension8`.

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
| Muu | `VersionId` |
| Varasto (mukautettu) | `InventDimension1`–`InventDimension12` |
| Muu | `ExtendedDimension1`–`ExtendedDimension8` |

Dimension yhdistämismääritykset lisätään seuraavasti:

1. Kirjaudu Power Apps -ympäristöön ja avaa **Varaston näkyvyys**.
1. Avaa **Määritykset**-sivu.
1. Lisää dimension yhdistämismääritykset valitsemalla **Tietolähde**-välilehden **Dimension yhdistämismääritykset** -osassa **Lisää**.
1. Määritä lähdedimensio **Dimension nimi** -kentässä.
1. Valitse **Perusdimensioon**-kentässä yhdistettävä varaston näkyvyyssovelluksen dimensio.
1. Valitse **Tallenna**.

![Dimension yhdistämismääritysten lisääminen](media/inventory-visibility-dimension-mapping.png "Dimension yhdistämismääritysten lisääminen")

Jos tietolähde sisältää esimerkiksi tuotteen väridimension, se voidaan yhdistää `ColorId`-perusdimensioon, jolloin mukautettu `ProductColor`-dimensio lisätään `exterchannel`-tietolähteeseen. Se yhdistetään sitten `ColorId`-perusdimensioon.

## <a name="create-a-physical-measure"></a>Fyysisen mitan luominen

Kun tietolähde kirjaa varastonmuutoksen varaston näkyvyyssovellukseen, muutoksen kirjaamiseen käytetään *fyysisiä mittoja*. Fyysiset mitat ovat määreitä, jotka ilmaisevat varastotapahtuman tilojen yhteenvedon. Kyselyt voivat perustua fyysisiin mittoihin.

Varaston näkyvyyssovellus sisältää fyysisten oletusmittojen luettelon. Nämä fyysiset oletusmitat saadaan Supply Chain Managementin **Varastoluettelo**-sivulla (**Varastonhallinta \> Kyselyt ja raportit \> Varastoluettelo**) olevista varastotapahtuman tiloista.

| Määre | Nimi |
|---|---|
| `PhysicalInvent` | Fyysinen varasto |
| `ReservPhysical` | Fyysinen varattu |
| `AvailPhysical` | Saatavissa oleva fyysinen |
| `ReservOrdered` | Tilaukseen varattu |
| `PostedQty` | Kirjattu määrä |
| `Deducted` | Toimitettu |
| `Picked` | Keräilty |
| `Received` | Vastaanotettu |
| `Registered` | Rekisteröitynyt |
| `Arrived` | Saapunut |
| `Ordered` | Tilattu |
| `OnOrder` | Tilauksessa |
| `QuotationReceipt` | Tarjouksen vastaanotto |
| `QuotationIssue` | Tarjouksen varasto-otto |

Jos tietolähde on Supply Chain Management, fyysisiä oletusmittoja ei tarvitse luoda uudelleen. Jos kyse on kuitenkin ulkoisista tietolähteistä, uudet fyysiset mitat voidaan luoda seuraavasti:

1. Kirjaudu Power Apps -ympäristöön ja avaa **Varaston näkyvyys**.
1. Avaa **Määritykset**-sivu.
1. Valitse **Tietolähde**-välilehden **Fyysiset mitat** -osassa **Lisää**, määritä lähdemitan nimi ja tallenna muutokset.

## <a name="define-the-product-hierarchy-index"></a>Tuotehierarkiaindeksin määrittäminen

Koostettujen dimensioryhmien määrittäminen antaa mahdollisuuden käyttää varaston näkyvyyssovellusta käytettävissä olevan varaston tilakyselyihin. Varaston näkyvyyssovelluksessa kutakin dimensioryhmää kutsutaan *indeksiksi*. Kukin indeksi vastaa määritettyä numeroa. Indeksoinnissa käytettävät dimensiot voidaan valita sen perusteella, minkälaisia kyselyjä varaston näkyvyyssovelluksessa halutaan tehdä.

Tuotehierarkiaindeksi määritetään seuraavasti:

1. Kirjaudu Power Apps -ympäristöön ja avaa **Varaston näkyvyys**.
1. Avaa **Määritykset**-sivu.
1. Lisää dimension yhdistämismääritykset valitsemalla **Tuotehierarkiaindeksi**-välilehden **Dimension yhdistämismääritykset** -osassa **Lisää**.
1. Indeksiluettelo annetaan oletusarvoisesti. Muokkaa aiemmin luotua indeksiä valitsemalla **Muokkaa** tai **Lisää** kyseisen indeksin kohdalla. Luo uusi indeksijoukko valitsemalla **Uusi indeksijoukko**. Tee indeksijoukon kunkin rivin **Dimensio**-kentässä valinta perusdimensioluettelossa. Seuraavien kenttien arvot luodaan automaattisesti:

    - **Joukon numero** – samaan ryhmään (indeksiin) kuuluvat dimensiot ryhmitellään yhteen ja niille määritetään sama joukon numero.
    - **Hierarkia** – Hierarkian avulla määritetään tuetut dimensioyhdistelmät, joissa voidaan tehdä kyselyjä dimensioryhmässä (indeksissä). Jos määritetään esimerkiksi dimensioryhmä, jonka hierarkia järjestys on *tyyli*, *väri* ja *koko*, järjestelmän tukee kolmen kyselyryhmän tuloksia. Ensimmäinen ryhmä on vain tyyli. Toinen ryhmä on tyylin ja värin yhdistelmä. Kolmas ryhmä on puolestaan tyylin, värin ja koon yhdistelmä. Muita yhdistelmiä ei tueta.

Lisätietoja on kohdassa [Tuoteindeksihierarkian määrittäminen](inventory-visibility-configuration.md#index-configuration).

### <a name="example"></a>Esimerkki

Tämän osan esimerkki näyttää, miten hierarkia toimii. Seuraavassa taulukossa on luettelo tässä esimerkissä käytettävissä olevasta varastosta.

| Nimike | Tyyli | Väri | Koko | Määrä |
|---|---|---|---|---|
| I0001 | Leveä | Musta | Pieni | 1 |
| I0001 | Leveä | Musta | Suuri | 2 |
| I0001 | Leveä | Punainen | Pieni | 3 |
| I0001 | Säännöllinen | Musta | Pieni | 4 |
| I0001 | Säännöllinen | Musta | Suuri | 5 |
| I0001 | Säännöllinen | Punainen | Pieni | 6 |
| I0001 | Säännöllinen | Punainen | Suuri | 7 |

Seuraavassa taulukko näyttää, miten indeksihierarkia määritetään.

| Avain | Joukon numero | Hierarkia |
|---|---|---|
| `StyleId` | 1 | 1 |
| `ColorId` | 1 | 2 |
| `SizeId` | 1 | 3 |

Edellä olevien asetusten perusteella varaston näkyvyyskyselyn dimensioyhdistelmä on *tyyli*, *väri* ja *koko*. Hierarkiamääritysten perusteella ulkoiset järjestelmät voivat tehdä kyselyjä käytettävissä olevassa varastossa seuraavin tavoin:

- `()` – Ryhmittely kaikkien perusteella. Tulos:

    - I0001, 28

- `(StyleId)` – Ryhmittely tyylin perusteella. Tulos:

    - I0001, leveä, 6
    - I0001, normaali, 22

- `(StyleId, ColorId)` – Ryhmittely tyyli- ja väriyhdistelmän perusteella. Tulos:

    - I0001, leveä, musta, 3
    - I0001, leveä, punainen, 3
    - I0001, normaali, musta, 9
    - I0001, normaali, punainen, 13

- `(StyleId, ColorId, SizeId)` – Ryhmittely tyyli-, väri- ja kokoyhdistelmän perusteella. Tulos:

    - I0001, leveä, musta, S, 1
    - I0001, leveä, musta, L, 2
    - I0001, leveä, punainen, S, 3
    - I0001, normaali, musta, S, 4
    - I0001, normaali, musta, L, 5
    - I0001, normaali, punainen, S, 6
    - I0001, normaali, punainen, L, 7

## <a name="set-up-a-custom-calculated-measure"></a>Mukautetun laskennallisen mitan määrittäminen

Varaston näkyvyyssovelluksen avulla voidaan tehdä sekä varaston fyysisiä mittoja että *mukautettuja laskennallisia mittoja* koskevia kyselyjä.

Määritys antaa mahdollisuuden määrittää määrejoukon, jota lisäämällä tai vähentämällä saadaan koostetuloksen kokonaismäärä.

1. Kirjaudu Power Apps -ympäristöön ja avaa **Varaston näkyvyys**.
1. Avaa **Määritykset**-sivu.
1. Lisää laskennallinen mitta valitsemalla **Laskennallinen mitta** -välilehdessä **Uusi laskennallinen mitta**. Määritä sitten kentät seuraavassa taulukossa ilmaistulla tavalla.

    | Kenttä | Arvo |
    |---|---|
    | Uuden laskennallisen mitan nimi | Anna laskennallisen mitan nimi. |
    | Tietolähde | Kyselyjärjestelmä on tietolähde. |
    | Määreen tietolähde | Anna määreen tietolähde. |
    | Määre | Anna määreen nimi. |
    | Määreen tyyppi | Valitsee määreen tyyppi (*Lisäys* tai *Vähennys*). |

Seuraavassa taulukossa oleva `MyCustomAvailableforReservation` on esimerkki mukautetusta laskennallisesta mitasta. Lisätietoja tästä esimerkistä on kohdassa [Tietolähteen määritys](inventory-visibility-configuration.md#data-source-configuration).

| Laskennallisen mitan tietolähde | Laskennallinen mitta | Määreen tietolähde | Määre | Määreen tyyppi |
|---|---|---|---|---|
| `CustomChannel` | `MyCustomAvailableforReservation` | `fno` | `availphysical` | `Addition` |
| `CustomChannel` | `MyCustomAvailableforReservation` | `fno` | `orderedintotal` | `Addition` |
| `CustomChannel` | `MyCustomAvailableforReservation` | `fno` | `orderedreserved` | `Subtraction` |
| `CustomChannel` | `MyCustomAvailableforReservation` | `mypos` | `Inbound` | `Addition` |
| `CustomChannel` | `MyCustomAvailableforReservation` | `mypos` | `Outbound` | `Subtraction` |
| `CustomChannel` | `MyCustomAvailableforReservation` | `exterchannel` | `received` | `Addition` |
| `CustomChannel` | `MyCustomAvailableforReservation` | `exterchannel` | `issued` | `Subtraction` |
| `CustomChannel` | `MyCustomAvailableforReservation` | `Exteexterchannelrchannel` | `reserved` | `Subtraction` |

### <a name="set-up-a-soft-reservation-mapping"></a><a name="setup-reservation-mapping"></a>Alustavan varauksen yhdistämismäärityksen määrittäminen

[!INCLUDE [preview-banner-section](../../includes/preview-banner-section.md)]

Ennen **Alustavan varauksen yhdistämismääritys** -välilehden muokkaamista *OnHandReservation*-ominaisuus on otettava käyttöön **Ominaisuuksien hallinta** -välilehdessä.

Kun yhdistämismääritys määritetään fyysisestä mitasta laskennalliseen mittaan, varaston näkyvyyspalvelu voi tarkistaa automaattisesti varauksen saatavuuden fyysisen mitan perusteella.

Ennen kuin tämä yhdistämismääritys voidaan määrittää, fyysiset mitat, laskennalliset mitat ja niiden tietolähteet on määritettävä Power Appsin **Määritys**-sivun **Tietolähde**- ja **Laskennallinen mitta** -välilehdissä (aiemmin tässä aiheessa kuvatulla tavalla).

Alustavan varauksen yhdistämismääritys määritetään seuraavasti:

1. Määritä alustavana varausmittana toimiva fyysinen mitta (esimerkki: `softreservordered`).
1. Määritä **Määritys**-sivun **Laskennallinen mitta** -välilehdessä laskennallinen *käytettävissä varaukseen* -mitta, jonka sisältämä laskentakaava halutaan yhdistää fyysiseen mittaan. Esimerkiksi `availforreserv` (käytettävissä varaukseen) voidaan määrittää siten, että se yhdistetään aiemmin määritettyyn fyysiseen `softreservordered` -mittaan. Tällä tavoin voidaan etsiä, mitkä sellaiset määrät ovat käytettävissä varaukseen, joiden varaston tila on `softreservordered`. Seuraavassa taulukossa on laskentakaava varaukseen käytettävissä olevasta varastosta.

    | Määre | Tietolähde | Mitta |
    |---|---|---|
    | `Addition` | `fno` | `availphysical` |
    | `Addition` | `pos` | `inbound` |
    | `Subtraction` | `pos` | `outbound` |
    | `Subtraction` | `iv` | `softreservordered` |

1. Avaa **Määritykset**-sivu.
1. Määritä **Alustavan varauksen yhdistämismääritys** -välilehdessä yhdistämismääritys fyysisestä mitasta laskennalliseen mittaan. Edellisessä esimerkissä `availforreserv` voidaan yhdistää aiemmin määritettyyn fyysiseen `softreservordered`-mittaan seuraavien asetusten avulla:

    | Fyysisen mitan tietolähde | Fyysinen mitta | Varaukseen käytettävissä olevan tietolähde | Varaukseen käytettävissä oleva laskennallinen mitta |
    |---|---|---|---|
    | `iv` | `softreservordered` | `iv` | `availforreserv` |

### <a name="set-up-a-soft-reservation-hierarchy"></a><a name="setup-reservation-hierarchy"></a>Alustavan varaushierarkian määrittäminen

[!INCLUDE [preview-banner-section](../../includes/preview-banner-section.md)]

Ennen **Alustavan varauksen hierarkia** -välilehden muokkaamista *OnHandReservation*-ominaisuus on otettava käyttöön **Ominaisuuksien hallinta** -välilehdessä.

Varaushierarkia ilmaisee dimensiojärjestyksen, joka on määritettävä varauksia tehtäessä. Se toimii samalla tavoin kuin tuoteindeksihierarkia käytettävissä olevaa varastoa koskevissa kyselyissä.

Varaushierarkia voi poiketa käytettävissä olevan varaston indeksihierarkiasta. Tämä erillisyys antaa mahdollisuuden toteuttaa sellainen luokanhallinta, jossa käyttäjät voivat eritellä dimensiot vaatimukset määrittäviksi tiedoiksi. Tämä puolestaan antaa mahdollisuuden entistä tarkempiin varauksiin.

#### <a name="example"></a>Esimerkki

Järjestelmässä määrittään seuraava varaushierarkia.

| Dimensio | Hierarkia |
|---|---|
| `ColorId` | 1 |
| `SizeId ` | 2 |
| `StyleId` | 3 |

Tässä varastohierarkiassa varaus voidaan tehdä seuraavissa dimensiotilauksissa:

- `()` – dimensiota ei anneta.
- `(ColorId)`
- `(ColorId, SizeId)`
- `(ColorId, SizeId, StyleId)`

Dimensiotilauksen on noudatettava varaushierarkiajärjestystä tarkasti dimensio kerrallaan. Esimerkiksi varauksia, joissa on `(ColorId, StyleId)`, ei sallita tässä esimerkissä, koska tätä järjestystä ei ole määritetty varaushierarkiassa.

### <a name="control-feature-management"></a><a name="feature-switch"></a>Ominaisuuksien hallinnan hallinta

Varaston näkyvyyden apuohjelma sisältää esimerkiksi ominaisuudet *OnHandReservation* ja *OnHandMostSpecificBackgroundService*. Nämä ominaisuudet on oletusarvoisesti poistettu käytöstä. Niitä voidaan käyttää avaamalla **Määritys**-sivu Power Appsissa ja ottamalla ne sitten käyttöön **Ominaisuuden hallinta** -välilehdessä.

### <a name="complete-and-update-the-configuration"></a>Määrityksen viimeisteleminen ja päivittäminen

Kun määritys on valmis, kaikki muutokset on vahvistettava varaston näkyvyyssovellukseen. Vahvista muutokset valitsemalla **Päivitä määritys** Power Appsin **Määritys**-sivun oikeassa yläkulmassa.

Kun **Päivitä määritys** valitaan ensimmäisen kerran, järjestelmä kysyy tunnistetietoja.

- **Asiakastunnus** – varaston näkyvyyssovellukselle luotu Azure-sovelluksen tunnus.
- **Vuokraajan tunnus** – Azure-vuokraajan tunnus.
- **Asiakasohjelman salasana** – varaston näkyvyyssovellukselle luotu Azure-sovelluksen tunnus.

Määritys päivitetään varaston näkyvyyspalveluun kirjautumisen jälkeen.

> [!NOTE]
> Tietolähteen nimi, fyysiset mitat ja dimensioiden yhdistämismääritykset on tarkistettava ennen määrityksen päivittämistä varaston näkyvyyspalveluun. Näitä asetuksia ei voi muokata sen jälkeen, kun **Päivitä määritys** on valittu.

### <a name="find-the-service-endpoint"></a><a name="get-service-endpoint"></a>Palvelun päätepisteen etsiminen

Jos oikea varaston näkyvyyspalvelun päätepiste ei ole tiedossa, avaa **Määritys**-sivu Power Appsissa ja valitse sitten **Näytä palvelun päätepiste** oikeassa yläkulmassa. Sivulla näkyy oikea palvelun päätepiste.

## <a name="operational-visibility"></a>Toiminnon aikainen näkyvyys

**Toiminnon aikainen näkyvyys** -sivu antaa käytettävissä olevan varaston reaaliaikaiset tulokset erilaisten dimensioyhdistelmien perusteella. Kun *OnHandReservation*-ominaisuus on otettu käyttöön, varauspyyntöjä voi kirjata myös **Toiminnan aikainen näkyvyys** -sivulla.

### <a name="on-hand-query"></a>Varastosaldokysely

**Varastosaldokysely**-välilehdessä on reaaliaikaisen varastosaldokyselyn tulokset.

Kun **Varastosaldokysely**-välilehti valitaan, järjestelmä kysyy tunnistetietotoja, joiden avulla se voi hakea haltijatunnuksen, jota tarvitaan kyselyn tekemiseen varaston näkyvyyspalvelussa. Haltijatunnus voidaan liittää **BearerToken**-kenttään ja valintaikkuna sulkea. Tämän jälkeen varastosaldokyselypyyntö voidaan kirjata.

Jos haltijatunnus ei kelpaa tai se on vanhentunut, liitä uusi tunnus **BearerToken**-kenttään. Anna oikeat **Asiakastunnus**-, **Vuokraajan tunnus** ja **Asiakasohjelman salaisuus** -arvot ja valitse **Päivitä**. Järjestelmä hakee automaattisesti uuden, kelvollisen haltijatunnuksen.

Kirjaa varastosaldokysely antamalla kysely pyynnön tekstiosassa. Käytä kaavaa, jota käsitellään kohdassa [Kysely kirjausmenetelmää käyttämällä](inventory-visibility-api.md#query-with-post-method).

![Varastosaldokyselyn asetukset](media/inventory-visibility-query-settings.png "Varastosaldokyselyn asetukset")

### <a name="reservation-posting"></a>Varauksen kirjaus

[!INCLUDE [preview-banner-section](../../includes/preview-banner-section.md)]

Kirjaa varastopyyntö **Varastokirjaus**-välilehdessä. *OnHandReservation*-ominaisuus on otettava käyttöön ennen varauspyynnön kirjaamista. Lisätietoja tästä ominaisuudesta on kohdassa [Varaston näkyvyyssovelluksen varaukset](inventory-visibility-reservations.md).

Varauspyynnön kirjaaminen edellyttää, että arvo annetaan pyynnön tekstiosassa. Käytä kaavaa, jota käsitellään kohdassa [Yhden varauspyynnön luominen](inventory-visibility-api.md#create-one-reservation-event). Valitse sitten **Kirjaa**. Pyynnön vastaustietoja voidaan tarkastella valitsemalla **Näytä tiedot**. Myös **reservationId**-arvo voidaan saada vastauksen tiedoista.

## <a name="inventory-summary"></a>Varaston yhteenveto

**Varaston yhteenveto** on mukautettu *Varastosaldon summaentiteetti* -näkymä. Se sisältää tuotteiden ja kaikkien dimensioiden varaston yhteenvedon. Dataversen **lisäsuodattimen** avulla voi luoda oman näkymän, jossa on näkyvissä itselle tärkeät rivit. Lisäsuodatinvaihtoehtojen avulla voi luoda monenlaisia niin yksinkertaisia kuin monimutkaisiakin näkymiä. Lisäksi niiden avulla voidaan lisätä ryhmiteltyjä ja sisäkkäisiä ehtoja suodattimiin.

Lisätietoja **lisäsuodattimen** käyttämisestä on kohdassa [Omien näkymien muokkaaminen tai luominen lisäruudukkosuodattimien avulla](/powerapps/user/grid-filters-advanced)

Mukautetun näkymän yläosassa on kolme kenttää: **Oletusdimensio**, **Mukautettu dimensio** ja **Mitta**. Näiden kenttien avulla voidaan hallita näkyvissä olevia kenttiä.

Nykyisen tuloksen voi suodattaa tai lajitella valitun sarakeotsikon avulla.

Mukautetun näkymän alareunassa on tietoja, kuten 50 tietuetta (29 valittu) tai 50 tietuetta. Nämä tiedot viittaavat **Lisäsuodatin**-tuloksista ladattuina oleviin tietueisiin. Teksti 29 valittu viittaa tietueiden määrään, jotka on valittu käyttämällä ladattujen tietueiden sarakeotsikkosuodatinta.

Näkymän alareunassa on **Lataa lisää** -painike, jolla voi ladata lisää tietueita Dataversesta. Ladattavien tietueiden oletusmäärä on 50. Kun **Lataa lisää** valitaan, seuraavat 1 000 käytettävissä olevaa tietuetta ladataan näkymään. **Lataa lisää** -painikkeessa oleva luku ilmaisee ladattuina olevien tietueiden määrän ja **Lisäsuodatin**-tuloksen tietueiden kokonaismäärän.

![Varaston yhteenveto](media/inventory-visibility-onhand-list.png "Varaston yhteenveto")
