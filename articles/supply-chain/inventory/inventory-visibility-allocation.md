---
title: Inventory Visibilityn varaston kohdistus
description: Tässä artikkelissa kerrotaan, miten varastonkohdistustoiminto määritetään ja kuinka sitä käytetään. Tämän toiminnon avulla voit varata erillisen varaston, jotta voit käsitellä kannattavimmat kanavat tai asiakkaat.
author: yufeihuang
ms.date: 05/27/2022
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2022-05-13
ms.dyn365.ops.version: 10.0.27
ms.openlocfilehash: f79497a24a5b4dd501bb0d13d9eaca7e98672533
ms.sourcegitcommit: f2175fe5e900d39f34167d671aab5074b09cc1b8
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/17/2022
ms.locfileid: "9306111"
---
# <a name="inventory-visibility-inventory-allocation"></a>Varaston näkyvyyden varaston kohdistus

[!include [banner](../includes/banner.md)]

## <a name="business-background-and-purpose"></a>Liiketoiminnallinen tausta ja tarkoitus

Useissa tapauksissa valmistajien, vähittäismyyjien ja muiden toimitusketjun yritysten on esikohdistettava varastoa tärkeitä myyntikanavia, sijainteja tai asiakkaita varten tai erityisiä myyntitapahtumia varten. Varaston kohdistus on myynnin suunnitteluprosessissa tyypillinen käytäntö, ja se tehdään ennen myyntitapahtumien toteutumista ja myyntitilauksen luomista.

Esimerkiksi polkupyöräyhtiöllä voi olla hyvin suosittua polkupyörää varastossa rajoitetusti. Tämä yritys tekee sekä online- että myymälämyyntiä. Jokaisessa myyntikanavassa yrityksellä on muutamia tärkeitä yrityskumppaneita (markkinapaikkoja ja suuria vähittäismyyjiä), jotka vaativat, että tietty osa kyseisen polkupyörän varastosta on varattu niille. Siksi polkupyöräyrityksen on pystyttävä tasapainottamaan varaston jakelua eri kanaville ja vastattava VIP-yhteistyökumppaneiden odotuksiin. Paras tapa saavuttaa molemmat tavoitteet on käyttää varaston kohdistusta, jotta kukin kanava ja vähittäismyyjä voi saada tiettyjä kohdistettuja määriä, jotka voidaan myydä asiakkaille myöhemmin.

Varaston kohdistuksella on kaksi liiketoiminnallista perustarkoitusta:

- **Varaston suojaaminen (ringfencing)** – Organisaatiot haluavat esikohdistaa rajoitetuttuja varastoja priorisoiduille kanaville, alueille, VIP-asiakkaille ja tytäryhtiöille. Varaston näkyvyyden kohdistustoiminnon on tarkoitus suojata kohdistettua varastoa, jotta muut kohdistukset, varaukset tai muut myyntivaatimukset eivät vaikuta aiemmin kohdistettuun varastoon.
- **Ylimyynnin hallinta** – Varaston näkyvyyden kohdistustoiminnon on tarkoitus rajoittaa aiemmin kohdistettuja määriä, jotta vastaanottava taho (esimerkiksi kanava tai asiakasryhmä) ei ylikäytä niitä, kun todellinen, alustavaan varaukseen perustuva myyntitapahtuma tulee voimaan.

## <a name="allocation-definition-in-inventory-visibility-service"></a>Kohdistuksen määritelmä varaston näkyvyyspalvelussa

Vaikka kohdistusominaisuus varaston näkyvyyspalvelussa ei siirrä fyysisiä varastomääriä syrjään, se viittaa fyysiseen varastomäärään määrittääkseen alkuperäisen *käytettävissä kohdistamisessa* -virtuaalimäärän. Varaston kohdistus varaston näkyvyydessä on alustava kohdistus. Se tehdään ennen todellisia myyntitapahtumia eikä se riipu myyntitilauksista. Voit esimerkiksi kohdistaa varaston tärkeimmille myyntikanaville tai suurille yritysmyyjille, ennen kuin mikään loppuasiakkaista käy myyntikanavalla tai vähittäismyyntiliikkeestä ostamassa sen.

Ero varaston kohdistuksen ja [varaston alustavan varauksen](inventory-visibility-reservations.md) välillä on se, että alustava varaus on tavallisesti linkitetty todellisiin myyntitapahtumiin (myyntitilausriveihin). Jos haluat käyttää kohdistuksen ja alustavan varauksen ominaisuuksia yhdessä, on suositeltavaa tehdä ensin varaston kohdistus ja tehdä sitten alustava varaus kohdistettuja määriä vasten. Lisätietoja: [Kuluta alustavana varauksena](#consume-to-soft-reserved).

Varaston kohdistustoiminnon avulla myynnin suunnittelijat tai avainasiakaspäälliköt voivat hallita ja esikohdistaa tärkeää varastoa kohdistusryhmille (kuten kanavat, alueet ja asiakasryhmät). Se tukee myös reaaliaikaista seurantaa, oikaisuja ja kohdistettujen määrien kulutuksen analytiikkaa, jotta täydennys ja uudelleenkohdistus voidaan tehdä ajoissa. Reaaliaikainen kohdistuksen, kulutuksen ja kohdistustasapainon näkyvyysominaisuus on erityisen tärkeä pikamyynnissä ja kampanjatapahtumissa.

## <a name="terminology"></a>Termit

Seuraavat termit ja käsitteet ovat hyödyllisiä varaston kohdistusta käsittelevissä keskusteluissa:

- **Kohdistusryhmä** – Ryhmä, joka omistaa kohdistuksen. Kohdistus voi olla esimerkiksi myyntikanava, asiakasryhmä tai tilaustyyppi.
- **Kohdistusryhmän arvo** – Kunkin kohdistusryhmän arvo. Esimerkiksi *verkko* tai *myymälä* voi olla myyntikanavan kohdistusryhmän arvo, kun taas *VIP* tai *tavallinen* voi olla asiakaskohdistusryhmän arvo.
- **Kohdistushierarkia** – Tapa yhdistää kohdistusryhmät hierarkkisesti. Voit esimerkiksi määrittää *kanavan* hierarkiatasoksi 1, *alueen* tasoksi 2 ja *asiakasryhmän* tasoksi 3. Varaston kohdistuksen aikana kohdistushierarkian järjestystä on noudatettava, kun kohdistusryhmän arvon määritetään. Voit esimerkiksi kohdistaa 200 punaista polkupyörää *Verkko*-kanavalle, *Lontoon* alueelle ja *VIP*-asiakasryhmälle.
- **Käytettävissä kohdistuksessa** – *Virtuaalinen yleinen pooli*, joka ilmaisee määrän, joka on käytettävissä lisäkohdistusta varten. Se on laskettu mitta, jonka voit vapaasti määrittää omalla kaavallasi. Jos käytössä on myös alustavan varauksen ominaisuus, on suositeltavaa käyttää samaa kaavaa käytettävissä kohdistuksessa -määrän ja varattavissa olevan määrän laskemiseen.
- **Kohdistettu** : Fyysinen mitta, joka osoittaa kohdistetun kiintiön, jonka kohdistusryhmät voivat kuluttaa.
- **Kulutettu** – Fyysinen mitta, joka osoittaa määrät, jotka on kulutettu alkuperäistä kohdistettua määrää vasten. Kun tähän fyysiseen mittariin lisätään numeroita, kohdistettu fyysinen mitta pienenee automaattisesti.

Seuraava kuva esittää varaston kohdistuksen liiketoiminnallisen työnkulun.

![Varaston näkyvyyden kohdistuksen liiketoiminnallinen työnkulku.](media/inventory-visibility-allocation-flow.png "Varaston näkyvyyden kohdistuksen liiketoiminnallinen työnkulku.")

## <a name="set-up-inventory-allocation"></a>Varaston kohdistuksen määrittäminen

Varaston kohdistustoiminto koostuu seuraavista osista:

- Ennalta määritetyt kohdistukseen liittyvä tietolähde, fyysiset mitat ja laskennalliset mitat.
- Mukautettavat kohdistusryhmät, joilla on enintään kahdeksan tasoa.
- Joukko kohdistuksen ohjelmointirajapintoja:
  - kohdista
  - uudelleenkohdista
  - poista kohdistus
  - kuluta
  - kysely

Kohdistusominaisuuden konfiguroinnissa on kaksi vaihetta:

- Määritä tietolähde [ja sen](inventory-visibility-configuration.md#data-source-configuration) ja sen [määreet](inventory-visibility-configuration.md#data-source-configuration-physical-measures).
- Määritä kohdistusryhmän nimi ja hierarkia.

### <a name="predefined-data-source"></a>Esimääritetty tietolähde

Kun otat kohdistusominaisuuden käyttöön ja kutsut konfiguraation päivityksen ohjelmointirajapintaa, varaston näkyvyys luo yhden ennalta määritetyn tietolähteen ja useita alustavia määreitä.

Tietolähde on nimeltään `@iv`.

Alkuperäiset fyysiset määreet ovat seuraavat:

- `@iv`
  - `@allocated`
  - `@cumulative_allocated`
  - `@consumed`
  - `@cumulative_consumed`

Alkuperäiset lasketut määreet ovat seuraavat:

- `@iv`
  - `@iv.@available_to_allocate` = `??` – `??` – `@iv.@allocated`

### <a name="add-other-physical-measures-to-the-available-to-allocate-calculated-measure"></a>Lisää muita fyysisiä määreitä laskettuun käytettävissä kohdistuksessa -määreeseen

Kohdistusta varten on määritettävä laskettu käytettävissä kohdistuksessa -määre (`@iv.@available_to_allocate`). Sinulla on esimerkiksi `fno`-tietolähde ja `onordered`-määre, `pos`-tietolähde ja `inbound`-määre, ja haluat tehdä kohdistuksen käytettävissä olevaan summalla `fno.onordered` ja `pos.inbound`. Tässä tapauksessa `@iv.@available_to_allocate`:n tulisi sisältää `pos.inbound` ja `fno.onordered` kaavassa. Tässä on esimerkki:

`@iv.@available_to_allocate` = `fno.onordered` + `pos.inbound` – `@iv.@allocated`

> [!NOTE]
> Tietolähde `@iv` on ennalta määritetty tietolähde. Kohdassa `@iv` etuliitteen `@` kanssa määritetyt fyysiset mittausarvot ovat ennalta määritettyjä mittausarvoja. Nämä mittausarvot ovat kohdistustoiminnon ennalta määritetty määritys, joten niitä ei voi muuttaa eikä poistaa. Jos näin tehdään, kohdistustoiminnon käyttämisen yhteydessä tapahtuu todennäköisesti odottamattomia virheitä.
>
> Voit lisätä uusia fyysisiä mittausarvoja ennalta määritettyyn laskettuun mittausarvoon `@iv.@available_to_allocate`, mutta sen nimeä ei saa muuttaa.

### <a name="change-the-allocation-group-name"></a>Kohdistusryhmän nimen muuttaminen

Enintään kahdeksan kohdistusryhmän nimeä voidaan määrittää. Ryhmissä on hierarkia.

Ryhmien nimet määritetään **Varaston näkyvyyden Power App -määritys** -sivulla Avataksesi tämän sivun avaa Microsoft Dataverse -ympäristössä varaston näkyvyyssovellus ja valitse **Määritys \> Kohdistus**.

Jos käytät esimerkiksi neljää ryhmän nimeä ja määrität ne muotoihin \[`channel`, `customerGroup`, `region`, `orderType`\], kyseiset nimet ovat kelvollisia kohdistukseen liittyvissä pyynnöissä, kun kutsut määrityksen päivityksen ohjelmointirajapintaa.

### <a name="allocation-using-tips"></a>Kohdistus vihjeiden avulla.

- Jokaisessa tuotteessa kohdistustoiminnon tulisi käyttää samaa *dimensiotasoa*, joka vastaa tuotteen indeksihierarkiaa, jonka määritit [tuotteen indeksihierarkian määrityksissä](inventory-visibility-configuration.md#index-configuration). Oletetaan esimerkiksi, että indeksihierarkiasi on \[`Site`, `Location`, `Color`, `Size`\]. Jos kohdistat dimensiotasolla \[`Site`, `Location`, `Color`\] yhdelle tuotteelle määrän, kun haluat kohdistaa tämän tuotteen seuraavan kerran, se on tehtävä samalla tasolla, \[`Site`, `Location`, `Color`\]. Jos käytät tasoa \[`Site`, `Location`, `Color`, `Size`\] tai \[`Site`, `Location`\], tiedot ovat ristiriitaisia.
- Kohdistusryhmän nimen muuttaminen ei vaikuta palveluun tallennettuihin tietoihin.
- Kohdistuksen tulisi tapahtua, kun tuotteen käytettävissä oleva määrä on positiivinen.
- Jos haluat kohdistaa korkean *kohdistustason* ryhmän tuotteet aliryhmään, käytä `Reallocate`-ohjelmointirajapintaa. Olet esimerkiksi kohdistanut kohdistusryhmän hierarkian \[`channel`, `customerGroup`, `region`, `orderType`\]haluat kohdistaa joitakin tuotteita kohdistusryhmästä \[Online, VIP \] alakohdistusryhmään \[Online, VIP, EU\], käytä `Reallocate`-ohjelmointirajapintaa määrän siirtämiseen. Jos käytät `Allocate`-ohjelmointirajapintaa, se kohdistaa määrän virtuaalisesta yleisestä poolista.

### <a name="using-the-allocation-api"></a><a name="using-allocation-api"></a>Kohdistuksen ohjelmointirajapinnan käyttäminen

Viisi kohdistuksen ohjelmointirajapintaa on avattu:

- POST /api/environment/{environmentId}/allocation/allocate
- POST /api/environment/{environmentId}/allocation/unallocate
- POST /api/environment/{environmentId}/allocation/reallocate
- POST /api/environment/{environmentId}/allocation/consume
- POST /api/environment/{environmentId}/allocation/query

#### <a name="allocate"></a>Kohdista

Kutsu `Allocate`-ohjelmointirajapintaa kohdistaaksesi tuotteen, jolla on erityisiä dimensioita. Tässä rakenne pyyntöä varten.

```json
{
    "id": "string",
    "productId": "string",
    "dimensionDataSource": "string",
    "groups": {
        "groupA": "string",
        "groupB": "string",
        "groupC": "string"
    },
    "quantity": 0,
    "organizationId": "string",
    "dimensions": {
        "dimension1": "string",
        "dimension2": "string",
        "dimension3": "string"
    }
}
```

Haluat esimerkiksi kohdistaa 10 kappaleen määrän tuotetta *Polkupyörä*, toimipaikalle *1*, sijainnille *11*, värille *punainen*, kanavalle *Online*, asiakasryhmälle *VIP* ja alueelle *US*. Voit tehdä tämän kohdistuksen tekemällä kutsun, jossa on seuraava sisältö.

```json
{
    "id": "???",
    "productId": "Bike",
    "groups": {
        "channel": "Online",
        "customerGroup": "VIP",
        "region": "US"
    },
    "quantity": 10,
    "organizationId": "usmf",
    "dimensions": {
        "siteId": "1",
        "locationId": "11",
        "colorId": "red"
    }
}
```

Määrän on oltava aina suurempi kuin 0 (nolla).

#### <a name="unallocate"></a>Poista kohdistus

Käytä `Unallocate`-ohjelmointirajapintaa kumotaksesi `Allocate`-toiminnon. Negatiivinen määrä ei ole sallittu `Allocate`-toiminnossa. `Unallocate`-sisältö on sama kuin `Allocate`-toiminnossa.

#### <a name="reallocate"></a>Uudelleenkohdista

Käytä `Reallocate`-ohjelmointirajapintaa siirtääksesi jonkin kohdistetun määrän toiseen ryhmäyhdistelmään. Tässä rakenne pyyntöä varten.

```json
{
    "id": "string",
    "productId": "string",
    "dimensionDataSource": "string",
    "sourceGroups": {
        "groupA": "string",
        "groupB": "string",
        "groupC": "string"
    },
    "groups": {
        "groupD": "string",
        "groupE": "string",
        "groupF": "string"
    },
    "quantity": 0,
    "organizationId": "string",
    "dimensions": {
        "dimension1": "string",
        "dimension2": "string",
        "dimension3": "string"
    }
}
```

Voit esimerkiksi siirtää kaksi polkupyörää, joilla on dimensiot \[toimipaikka=1, sijainti=11, väri=punainen\], kohdistusryhmästä \[Online, VIP, US\] kohdistusryhmään \[Online, VIP, EU\] kutsumalla `Reallocate`-ohjelmointirajapintaa ja antamalla seuraavan tekstin.

```json
{
    "id": "???",
    "productId": "Bike",
    "sourceGroups": {
        "channel": "Online",
        "customerGroup": "VIP",
        "region": "US"
    },
    "groups": {
        "channel": "Online",
        "customerGroup": "VIP",
        "region": "EU"
    },
    "quantity": 2,
    "organizationId": "usmf",
    "dimensions": {
        "siteId": "1",
        "locationId": "11",
        "colorId": "red"
    }
}
```

#### <a name="consume"></a>Kulutus

Käytä `Consume`-ohjelmointirajapintaa kirjataksesi kulutetun määrän kohdistusta vasten. Voit esimerkiksi käyttää tätä ohjelmointirajapintaa siirtääksesi kohdistetun määrän joihinkin todellisiin määreisiin. Tässä rakenne pyyntöä varten.

```json
{
    "id": "string",
    "productId": "string",
    "dimensionDataSource": "string",
    "groups": {
        "groupA": "string",
        "groupB": "string",
        "groupC": "string"
    },
    "quantity": 0,
    "organizationId": "string",
    "dimensions": {
        "dimension1": "string",
        "dimension2": "string",
        "dimension3": "string"
    },
    "physicalMeasures": {
        "datasource1": {
            "measure": "string" // Addition or Subtraction
        }
    }
}
```

On esimerkiksi kahdeksan kohdistettua polkupyörää, joilla on dimensiot \[toimipaikka=1, sijainti=11, väri=punainen\] kohdistusryhmässä \[Online, VIP, US\]. Käytetään seuraavaa käytettävissä kohdistuksessa -kaavaa:

`@iv.@available_to_allocate` = `fno.onordered` + `pos.inbound` – `@iv.@allocated`

Kahdeksan polkupyörää kohdistetaan `pos.inbound`-määreestä.

Nyt on myyty kolme polkupyörää, ja ne on otettu kohdistusjoukosta. Voit rekisteröidä siirron tekemällä kutsun, jossa on seuraava pyyntösisältö.

```json
{
    "id": "???",
    "organizationId": "usmf",
    "productId": "Bike",
    "dimensions": {
        "siteId": "1",
        "locationId": "11",
        "colorId": "red"
    },
    "groups": {
        "channel": "Online",
        "customerGroup": "VIP",
        "region": "US"
    },
    "quantity": 3,
    "physicalMeasures": {
        "pos": {
            "inbound": "Subtraction"
        }
    }
}
```

Tämän kutsun jälkeen tuotteen kohdistettua määrää vähennetään kolmella. Lisäksi varaston näkyvyys muodostaa käytettävissä olevaan muutostapahtuman, jossa `pos.inbound` = *-3*. Vaihtoehtoisesti voit pitää `pos.inbound`-arvon muuttumattomana ja vain kuluttaa kohdistetun määrän. Tässä tapauksessa on kuitenkin joko luotava toinen fyysinen määre kulutettujen määrien pitämiseksi tai käytettävä esimääritettyä määrettä `@iv.@consumed`.

Huomaa tämän pyynnön yhteydessä, että fyysisen määreen, jota käytät kulutuspyynnössä, tulisi käyttää vastakkaista muuttujatyyppiä (lisäys tai vähennys) verrattuna lasketussa määreessä käytettyyn muuttujatyyppiin. Näin ollen tässä kulutuksessa `iv.inbound`-arvo on `Subtraction`, ei `Addition`.

`fno`-tietolähdettä ei voi käyttää kulutuksessa, koska varaston näkyvyys ei voi muuttaa mitään tietoja `fno`-tietolähteessä. Tietovirta on yksisuuntainen, mikä tarkoittaa, että `fno`-tietolähteen kaikkien määrän muutosten on oltava peräisin Supply Chain Management -ympäristöstä.

#### <a name="consume-as-a-soft-reservation"></a><a name="consume-to-soft-reserved"></a>Kuluta alustavana varauksena

`Consume`-ohjelmointirajapinta voi kuluttaa kohdistetun määrän myös alustavana varauksena. Tässä tapauksessa `Consume`-toiminto vähentää kohdistettua määrää ja tekee sitten alustavan varauksen kyseistä määrää vastaavasti. Käyttääksesi tätä menetelmää sinun on käytettävä myös [alustava varaus](inventory-visibility-reservations.md) -ominaisuutta varaston näkyvyydessä.

Olet esimerkiksi määrittänyt alustavan varauksen muuttujaksi (määreeksi) `iv.softreserved`. Seuraavaa kaavaa käytetään laskettua varattavissa-määrettä varten:

`iv.available_to_reserve` = `fno.onordered` + `pos.inbound` – `iv.softreserved`

Käyttääksesi tätä asetusta kohdistusominaisuuden kanssa lisää `@iv.@allocated` kohtaan `iv.available_to_reserve` tuottaaksesi seuraavan kaavan:

`iv.available_to_reserve` = `fno.onordered` + `pos.inbound` – `iv.softreserved` – `@iv.@allocated`

Päivitä sitten `@iv.@available_to_allocate` samalle arvolle.

Kun haluat kuluttaa määrän 3 ja varata suoraan tämän määrän, voit tehdä kutsun, jossa on seuraava pyyntö.

```json
{
    "id": "???",
    "organizationId": "usmf",
    "productId": "Bike",
    "dimensions": {
        "siteId": "1",
        "locationId": "11",
        "colorId": "red"
    },
    "groups": {
        "channel": "Online",
        "customerGroup": "VIP",
        "region": "US"
    },
    "quantity": 3,
    "physicalMeasures": {
        "iv": {
            "softreserved": "Addition"
        }
    }
}
```

Huomaa tämän pyynnön yhteydessä, että `iv.softreserved`-arvo on `Addition`, ei `Subtraction`.

#### <a name="query"></a>Kysely

Käytä `Query`-ohjelmointirajapintaa hakeaksesi kohdistukseen liittyviä tuotetietoja. Voit kaventaa tuloksia dimensiosuodattimien ja kohdistusryhmän suodattimien avulla. Dimensioiden on vastattava tarkalleen haettavaa kohdetta, esimerkiksi \[toimipaikka=1, sijainti=11\] palauttaa ei-liittyviä tuloksia verrattuna vaihtoehtoon \[toimipaikka=1, sijainti=11, väri=punainen\].

```json
{
    "productId": "string",
    "organizationId": "string",
    "dimensions": {
        "dimension1": "string",
        "dimension2": "string",
        "dimension3": "string"
    },
    "groups": {
        "additionalProp1": "string",
        "additionalProp2": "string",
        "additionalProp3": "string"
    },
}
```

Käytä esimerkiksi \[toimipaikka=1, sijainti=11, väri=punainen\] ja tyhjennä ryhmäkenttä saadaksesi kohdistustietueet:

```json
{
    "organizationId": "usmf",
    "productId": "Bike",
    "dimensions": {
        "siteId": "1",
        "locationId": "11",
        "colorId": "red"
    },
    "groups": {
        "channel": "Online",
        "customerGroup": "VIP",
        "region": "US"
    },
}
```

Käytä \[toimipaikka=1, sijainti=11, väri=punainen\] ja ryhmät \[kanava=Online, asiakasryhmä=VIP, alue=US\] saadaksesi kohdistustietueet tätä ryhmää varten:

```json
{
    "organizationId": "usmf",
    "productId": "Bike",
    "dimensions": {
        "siteId": "1",
        "locationId": "11",
        "colorId": "red"
    },
    "groups": {
        "channel": "Online",
        "customerGroup": "VIP",
        "region": "US"
    },
}
```
