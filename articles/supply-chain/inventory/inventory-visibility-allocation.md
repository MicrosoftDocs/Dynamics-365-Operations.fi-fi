---
title: Inventory Visibilityn varaston kohdistus
description: Tässä artikkelissa kerrotaan, miten varastonkohdistustoiminto määritetään ja kuinka sitä käytetään. Tämän toiminnon avulla voit varata erillisen varaston, jotta voit käsitellä kannattavimmat kanavat tai asiakkaat.
author: yufeihuang
ms.date: 11/04/2022
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2022-05-13
ms.dyn365.ops.version: 10.0.27
ms.openlocfilehash: 449ca0616405ba589b92fba1ef078a4350d1e3b1
ms.sourcegitcommit: 49f8973f0e121eac563876d50bfff00c55344360
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/14/2022
ms.locfileid: "9762669"
---
# <a name="inventory-visibility-inventory-allocation"></a>Inventory Visibilityn varaston kohdistus

[!include [banner](../includes/banner.md)]

## <a name="business-background-and-purpose"></a>Liiketoiminnallinen tausta ja tarkoitus

Organisaatioiden on usein kohdistettava varastosaldo ennalta tärkeimmille myyntikanaville, asiakasryhmille, alueille ja markkinointitapahtumille. Näin varmistetaan, että ennalta kohdistettu varasto on suojattu muulta käytöltä ja se voidaan käyttää vain kohdistukseen liittyvissä myyntitapahtumissa. Varaston kohdistus Inventory Visibilityssa on myyntitoimintojen suunnitteluprosessin osa. Se tehdään ennen yhdenkään myyntitapahtuman toteutumista ja myyntitilauksen luomista.

Esimerkiksi Contoso-niminen yritys valmistaa suosittuja pyöriä. Valitettavasti viimeaikaisen toimitusketjussa tapahtuneen keskeytyksen vuoksi pyörän siirtovarasto ei ole kunnossa. Contosolla on vain rajoitettu käytettävissä oleva varasto, joka on nyt saatava riittämään. Contosolla on myyntiä sekä verkossa että myymälöissä. Jokaisessa myyntikanavassa yrityksellä on muutamia tärkeitä yrityskumppaneita (markkinapaikkoja ja suuria vähittäismyyjiä), jotka vaativat, että tietty osa kyseisen polkupyörän varastosta on varattu niille. Siksi polkupyöräyrityksen on pystyttävä tasapainottamaan varaston jakelua eri kanaville ja vastattava VIP-yhteistyökumppaneiden odotuksiin. Paras tapa saavuttaa molemmat tavoitteet on käyttää varaston kohdistusta, jotta kukin kanava ja vähittäismyyjä voi saada tiettyjä kohdistettuja määriä, jotka voidaan myydä asiakkaille myöhemmin.

Varaston kohdistuksella on kaksi liiketoiminnallista perustarkoitusta:

- **Varaston suojaaminen (ring fencing)** – Organisaatiot haluavat esikohdistaa rajoitetuttuja varastoja priorisoiduille kanaville, alueille, VIP-asiakkaille ja tytäryhtiöille. Varaston näkyvyyden kohdistustoiminnon on tarkoitus suojata kohdistettua varastoa, jotta muut kohdistukset, varaukset tai muut myyntivaatimukset eivät vaikuta aiemmin kohdistettuun varastoon.
- **Ylimyynnin hallinta** – Varaston näkyvyyden kohdistustoiminnon on tarkoitus rajoittaa aiemmin kohdistettuja määriä, jotta vastaanottava taho (esimerkiksi kanava tai asiakasryhmä) ei ylikäytä niitä, kun todellinen, alustavaan varaukseen perustuva myyntitapahtuma tulee voimaan.

## <a name="allocation-definition-in-inventory-visibility-service"></a>Kohdistuksen määritelmä varaston näkyvyyspalvelussa

### <a name="allocation-virtual-pool"></a>Kohdistuksen virtuaalipooli

Vaikka kohdistusominaisuus Inventory Visibilityssa ei siirrä fyysisiä varastomääriä syrjään, se viittaa fyysiseen varastomäärään määrittääkseen alkuperäisen *käytettävissä olevan kohdistamisen* virtuaalipoolin määrän. Varaston kohdistus varaston näkyvyydessä on alustava kohdistus. Se tehdään ennen todellisia myyntitapahtumia eikä se riipu myyntitilauksista. Voit esimerkiksi kohdistaa varaston tärkeimmille myyntikanaville tai suurille yritysmyyjille, ennen kuin mikään loppuasiakkaista käy myyntikanavalla tai vähittäismyyntiliikkeestä ostamassa sen.

### <a name="difference-between-inventory-allocation-and-soft-reservation"></a>Varaston kohdistuksen ja alustavan varauksen välinen ero

[Alustavat varaukset](inventory-visibility-reservations.md) linkitetään yleensä todellisiin myyntitapahtumiin (myyntitilausriveihin). Sekä kohdistusta että alustavaa varausta voidaan käyttää itsenäisesti, mutta jos niitä halutaan käyttää yhdessä, alustava varaus on tehtävä kohdistuksen jälkeen. O suositeltavaa tehdä ensin varaston kohdistus ja sitten kohdistettujen määrien alustava varaus. Näin saavutetaan lähes reaaliaikainen kohdistuksen kulutus. Lisätietoja: [Kuluta alustavana varauksena](#consume-to-soft-reserved).

Varaston kohdistustoiminnon avulla myynnin suunnittelijat tai avainasiakaspäälliköt voivat hallita ja esikohdistaa tärkeää varastoa kohdistusryhmille (kuten kanavat, alueet ja asiakasryhmät). Se tukee myös reaaliaikaista seurantaa, oikaisuja ja kohdistettujen määrien kulutuksen analytiikkaa. Näin varmistetaan, että täydennys ja uudelleenkohdistus voidaan tehdä ajoissa. Reaaliaikainen kohdistuksen, kulutuksen ja kohdistustasapainon näkyvyysominaisuus on erityisen tärkeä pikamyynnissä ja kampanjatapahtumissa.

## <a name="terminology"></a>Termit

Seuraavat termit ja käsitteet ovat hyödyllisiä varaston kohdistusta käsittelevissä keskusteluissa:

- **Kohdistusryhmä** – Ryhmä, joka omistaa kohdistuksen. Kohdistus voi olla esimerkiksi myyntikanava, asiakasryhmä tai tilaustyyppi.
- **Kohdistusryhmän arvo** – Kunkin kohdistusryhmän arvo. Esimerkiksi *verkko* tai *myymälä* voi olla myyntikanavan kohdistusryhmän arvo, kun taas *VIP* tai *tavallinen* voi olla asiakaskohdistusryhmän arvo.
- **Kohdistushierarkia** – Tapa yhdistää kohdistusryhmät hierarkkisesti. Voit esimerkiksi määrittää *kanavan* hierarkiatasoksi 1, *alueen* tasoksi 2 ja *asiakasryhmän* tasoksi 3. Varaston kohdistuksen aikana kohdistushierarkian järjestystä on noudatettava, kun kohdistusryhmän arvon määritetään. Voit esimerkiksi kohdistaa 200 punaista polkupyörää *Verkko*-kanavalle, *Lontoon* alueelle ja *VIP*-asiakasryhmälle.
- **Käytettävissä kohdistuksessa** – *Virtuaalinen yleinen pooli*, joka ilmaisee määrän, joka on käytettävissä lisäkohdistusta varten. Se on laskettu mitta, jonka voit vapaasti määrittää omalla kaavallasi. Jos käytössä on myös alustavan varauksen ominaisuus, on suositeltavaa käyttää samaa kaavaa käytettävissä kohdistuksessa -määrän ja varattavissa olevan määrän laskemiseen.
- **Kohdistettu** : Fyysinen mitta, joka osoittaa kohdistetun kiintiön, jonka kohdistusryhmät voivat kuluttaa. Se vähennetään samalla, kun kulutettu määrä lisätään.
- **Kulutettu** – Fyysinen mitta, joka osoittaa määrät, jotka on kulutettu alkuperäistä kohdistettua määrää vasten. Kun tähän fyysiseen mittariin lisätään numeroita, kohdistettu fyysinen mitta pienenee automaattisesti.

Seuraava kuva esittää varaston kohdistuksen liiketoiminnallisen työnkulun.

![Varaston näkyvyyden kohdistuksen liiketoiminnallinen työnkulku.](media/inventory-visibility-allocation-flow.png "Varaston näkyvyyden kohdistuksen liiketoiminnallinen työnkulku.")

Seuraavassa kuvassa esitetään kohdistushierarkia ja kohdistusryhmät. *Yleinen virtuaalipooli*, joka näytetään tässä, on kohdistukseen käytettävissä oleva määrä.

[<img src="media/inventory-visibility-allocation-hierarchy.png" alt="Inventory Visibility allocation hierarchy." title="Inventory Visibilityn kohdistushierarkia" width="720" />](media/inventory-visibility-allocation-hierarchy.png)

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

Kohdistusominaisuuden konfiguroinnissa on kolme vaihetta:

- Ota käyttöön Inventory Visibility -sovelluksen ominaisuus siirtymällä kohtaan **Määritys \> Ominaisuuksien hallinta ja asetukset \> Kohdistus**.
- Määritä tietolähde [ja sen](inventory-visibility-configuration.md#data-source-configuration) ja sen [määreet](inventory-visibility-configuration.md#data-source-configuration-physical-measures).
- Määritä kohdistusryhmän nimi ja hierarkia.

### <a name="predefined-data-source"></a>Esimääritetty tietolähde

Kun otat kohdistusominaisuuden käyttöön ja kutsut konfiguraation päivityksen ohjelmointirajapintaa, varaston näkyvyys luo yhden ennalta määritetyn tietolähteen ja useita alustavia määreitä.

Tietolähde on nimeltään `@iv`. Mukana on joukko fyysisiä oletusmittoja. Voit tarkastella niitä Inventory Visibility -sovelluksessa siirtymällä kohtaan **Määritys \> Tietolähde**. Näkyvissä tulisi olla **Tietolähde - @IV**. Laajenna tietolähde `@iv`, jotta näkyviin tulee alkuperäisten fyysisten mittojen luettelo seuraavalla tavalla:

- `@iv`

    - `@allocated`
    - `@cumulative_allocated`
    - `@consumed`
    - `@cumulative_consumed`

Valitse **Lasketut mitat** -välilehti, jos haluat tarkastella alkuperäistä laskettua mittaa nimeltä `@iv.@available_to_allocate`:

- `@iv`

    - `@iv.@available_to_allocate` = `??` – `??` – `@iv.@allocated`

### <a name="add-other-physical-measures-to-the-available-to-allocate-calculated-measure"></a>Lisää muita fyysisiä määreitä laskettuun käytettävissä kohdistuksessa -määreeseen

Kohdistusta varten on määritettävä kaava oikein lasketulle kohdistukselle käytettävissä olevaa mittaa varten (`@iv.@available_to_allocate`). Sinulla on esimerkiksi tietolähde `fno` ja mitta `onordered` sekä tietolähde `pos` ja mitta `inbound`. Haluat tehdä kohdistuksen käytettävissä olevaan varastoon summalla `fno.onordered` ja `pos.inbound`. Tässä tapauksessa `@iv.@available_to_allocate`:n tulisi sisältää `pos.inbound` ja `fno.onordered` kaavassa. Tässä on esimerkki:

`@iv.@available_to_allocate` = `fno.onordered` + `pos.inbound` – `@iv.@allocated`

> [!NOTE]
> Tietolähde `@iv` on ennalta määritetty tietolähde. Kohdassa `@iv` etuliitteen `@` kanssa määritetyt fyysiset mittausarvot ovat ennalta määritettyjä mittausarvoja. Nämä mittausarvot ovat kohdistustoiminnon ennalta määritetty määritys, joten niitä ei voi muuttaa eikä poistaa. Jos näin tehdään, kohdistustoiminnon käyttämisen yhteydessä tapahtuu todennäköisesti odottamattomia virheitä.
>
> Voit lisätä uusia fyysisiä mittausarvoja ennalta määritettyyn laskettuun mittausarvoon `@iv.@available_to_allocate`, mutta sen nimeä ei saa muuttaa.

### <a name="manage-allocation-groups"></a>Kohdistusryhmien hallinta

Enintään kahdeksan kohdistusryhmän nimeä voidaan määrittää. Ryhmissä on hierarkia. Voit tarkastella ja päivittää kohdistusryhmiä alla olevien ohjeiden mukaan.

1. Kirjaudu Power Apps -ympäristöön ja avaa **Varaston näkyvyys**.
1. Avaa **Määritys**-sivu ja valitse **Kohdistus**-välilehdessä **Muokkaa määritystä**. Oletusarvoisessa kohdistushierarkiassa on neljä tasoa: `Channel` (ylin taso), `customerGroup` (toinen taso),`Region` (kolmas taso) ja `OrderType` (neljäs taso).
1. Voit poistaa olemassa olevan kohdistusryhmän valitsemalla sen vieressä olevan **X**-kohdan. Voit myös lisätä hierarkiaan uusia kohdistusryhmiä syöttämällä kunkin uuden ryhmän nimen suoraan kenttään.

    > [!IMPORTANT]
    > Ole varovainen, kun poistat kohdistushierarkian yhdistämismäärityksen tai muutat sitä. Ohjeita on kohdassa [Vihjeitä kohdistuksen käyttämistä varten](#allocation-tips).

1. Kun kohdistusryhmän ja hierarkian määritysten määrittäminen on tehty, tallenna muutokset ja valitse oikeassa yläosassa oleva **Päivitä määritys**. Määritettyjen kohdistusryhmien arvot päivitetään, kun luot kohdistuksen käyttämällä käyttöliittymää tai ohjelmointirajapinnan POST-toimintoa (/api<wbr>/environment<wbr>/\{environmentId\}<wbr>/allocation<wbr>/allocate). Myöhemmin tässä artikkelissa kerrotaan lisää näistä toiminnoista.

Jos käytät neljää ryhmän nimeä ja määrität ne muotoihin \[`channel`, `customerGroup`, `region`, `orderType`\], kyseiset nimet ovat kelvollisia kohdistukseen liittyvissä pyynnöissä, kun kutsut määrityksen päivityksen ohjelmointirajapintaa.

### <a name="tips-for-using-allocation"></a><a name="allocation-tips"></a>Vihjeitä kohdistuksen käyttämistä varten

- Jokaisessa tuotteessa kohdistustoiminnon tulisi käyttää samaa *dimensiotasoa*, joka vastaa tuotteen indeksihierarkiaa, jonka määritit [tuotteen indeksihierarkian määrityksissä](inventory-visibility-configuration.md#index-configuration). Oletetaan esimerkiksi, että indeksihierarkiasi on \[`Site`, `Location`, `Color`, `Size`\]. Jos kohdistat dimensiotasolla \[`Site`, `Location`, `Color`\] yhdelle tuotteelle määrän, kun haluat kohdistaa tämän tuotteen seuraavan kerran, se on tehtävä samalla tasolla, \[`Site`, `Location`, `Color`\]. Jos käytät tasoa \[`Site`, `Location`, `Color`, `Size`\] tai \[`Site`, `Location`\], tiedot ovat ristiriitaisia.
- **Kohdistusryhmien ja -hierarkian muokkaaminen:** Jos järjestelmässä on jo kohdistustiedot, olemassa olevien kohdistusryhmien poistaminen tai siirtyminen kohdistusryhmähierarkiaan vahingoittaa kohdistusryhmien välillä olevaa yhdistämismääritystä. Tämän vuoksi kaikki vanhat tiedot on tyhjennettävä manuaalisesti ennen uuden määrityksen päivittämistä. Koska uusien kohdistusryhmien lisäys alimpaan hierarkiaan ei kuitenkaan vaikuta olemassa oleviin yhdistämismäärityksiin, tietoja ei tarvitse tyhjentää.
- Kohdistus onnistuu vain, jos tuotteella on positiivinen kohdan `available_to_allocate` määrä.
- Jos haluat kohdistaa korkean *kohdistustason* ryhmän tuotteet aliryhmään, käytä `Reallocate`-ohjelmointirajapintaa. Olet esimerkiksi kohdistanut kohdistusryhmän hierarkian \[`channel`, `customerGroup`, `region`, `orderType`\]haluat kohdistaa joitakin tuotteita kohdistusryhmästä \[Online, VIP \] alakohdistusryhmään \[Online, VIP, EU\], käytä `Reallocate`-ohjelmointirajapintaa määrän siirtämiseen. Jos käytät `Allocate`-ohjelmointirajapintaa, se kohdistaa määrän virtuaalisesta yleisestä poolista.
- Jos haluat tarkastella tuotteen saatavuutta (yleinen pooli), käytä [kysely varastosaldosta](inventory-visibility-api.md#query-on-hand) -ohjelmointirajapintaa tehdessäsi kyselyn varaston summasta, joka on *käytettävissä kohdistusta varten*. Tämän jälkeen voit tehdä kohdistuksen näiden tietojen perusteella.

## <a name="use-the-allocation-api"></a><a name="using-allocation-api"></a>Kohdistuksen ohjelmointirajapinnan käyttäminen

Viisi kohdistuksen ohjelmointirajapintaa on avattu:

- **POST /api<wbr>/environment<wbr>/\{environmentId\}<wbr>/allocation<wbr>/allocate** – Tätä ohjelmointirajapintaa käytetään alkuperäisen kohdistuksen luomisessa.
- **POST /api<wbr>/environment<wbr>/\{environmentId\}<wbr>/allocation<wbr>/unallocate** –Tätä ohjelmointirajapintaa käytetään kohdistettujen määrien palauttamisessa tai poistamisessa.
- **POST /api<wbr>/environment<wbr>/\{environmentId\}<wbr>/allocation<wbr>/reallocate** – Tätä ohjelmointirajapintaa käytetään kohdistetun määrän siirtämisessä olemassa olevasta kohdistuksesta muihin kohdistusryhmiin.
- **POST /api<wbr>/environment<wbr>/\{environmentId\}<wbr>/allocation<wbr>/consume** – Tätä ohjelmointirajapintaa käytetään kohdistetun määrän vähentämisessä (käyttämisessä).
- **POST /api<wbr>/environment<wbr>/\{environmentId\}<wbr>/allocation<wbr>/query** – Tätä ohjelmointirajapintaa käytetään olemassa olevien kohdistustietueiden tarkistamisessa kohdistusryhmien ja -hierarkian avulla.

### <a name="allocate"></a>Kohdista

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
    "id": "test101",
    "productId": "Bike",
    "groups": {
        "channel": "Web",
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

### <a name="unallocate"></a>Poista kohdistus

Käytä `Unallocate`-ohjelmointirajapintaa kumotaksesi `Allocate`-toiminnon. Negatiivinen määrä ei ole sallittu `Allocate`-toiminnossa. `Unallocate`-sisältö on sama kuin `Allocate`-toiminnossa.

### <a name="reallocate"></a>Uudelleenkohdista

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
    "id": "test102",
    "productId": "Bike",
    "sourceGroups": {
        "channel": "Web",
        "customerGroup": "VIP",
        "region": "US"
    },
    "groups": {
        "channel": "Web",
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

### <a name="consume"></a>Kulutus

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
    "id": "test103",
    "organizationId": "usmf",
    "productId": "Bike",
    "dimensions": {
        "siteId": "1",
        "locationId": "11",
        "colorId": "red"
    },
    "groups": {
        "channel": "Web",
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

Huomaa tämän pyynnön yhteydessä, että fyysisen määreen, jota käytät kulutuspyynnössä, tulisi käyttää vastakkaista muuttujatyyppiä (lisäys tai vähennys) verrattuna lasketussa määreessä käytettyyn muuttujatyyppiin. Näin ollen tässä kulutuksessa kohteella `iv.inbound` on arvo `Subtraction`, ei `Addition`.

`fno`-tietolähdettä ei voi käyttää kulutuksessa, koska varaston näkyvyys ei voi muuttaa mitään tietoja `fno`-tietolähteessä. Tietovirta on yksisuuntainen, mikä tarkoittaa, että `fno`-tietolähteen kaikkien määrän muutosten on oltava peräisin Supply Chain Management -ympäristöstä.

### <a name="consume-as-a-soft-reservation"></a><a name="consume-to-soft-reserved"></a>Kuluta alustavana varauksena

`Consume`-ohjelmointirajapinta voi kuluttaa kohdistetun määrän myös alustavana varauksena. Tässä tapauksessa `Consume`-toiminto vähentää kohdistettua määrää ja tekee sitten alustavan varauksen kyseistä määrää vastaavasti. Käyttääksesi tätä menetelmää sinun on käytettävä myös [alustava varaus](inventory-visibility-reservations.md) -ominaisuutta varaston näkyvyydessä.

Olet esimerkiksi määrittänyt alustavan varauksen fyysiseksi mitaksi `iv.softreserved`. Seuraavaa kaavaa käytetään laskettua varattavissa-määrettä varten:

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
        "channel": "Web",
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

### <a name="query"></a>Kysely

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
        "channel": "Web",
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
        "channel": "Web",
        "customerGroup": "VIP",
        "region": "US"
    },
}
```

## <a name="use-the-allocation-user-interface"></a>Kohdistuksen käyttöliittymän käyttäminen

Voit hallita manuaalisesti kohdistuksia käyttöliittymässä avaamalla Inventory Visibility -sovelluksen ja siirtymällä kohtaan **Toiminnan aikainen näkyvyys \> Kohdistus**. Voit nyt suorittaa mitä tahansa seuraavissa aliosissa kuvattuja toimintoja.

### <a name="create-an-allocation"></a>Kohdistuksen luominen

Alla olevien ohjeiden avulla voit luoda kohdistuksen Inventory Visibilityn **Kohdistus**-sivulla.

1. Valitse **Kohdista**.
1. Määritä peruskentät, -dimensiot ja kohdistusryhmien kohdearvot. (Kun valitset tietolähteen keräämisen **Dimensiot**-osassa, käytä ensin avattavaa luetteloa määrittääksesi dimensiot (esimerkiksi `siteId`). Syötä sitten dimensioiden arvot näkyviin tuleviin kenttiin.)
1. Valitse **Lähetä**.

### <a name="consume-an-allocation"></a>Kohdistuksen kuluttaminen

Kuluta kohdistusta valitsemalla **Kuluta**. Varmista, että kulutat oikeaa kohdistusryhmää ja -hierarkiaa, syöttämällä samat organisaatiojoukot ja dimension tiedot, jotka syötit kohdistuksen luomisen yhteydessä.

### <a name="reallocate-an-allocation"></a>Kohdistuksen kohdistaminen uudelleen

Valitse **Kohdista uudelleen**, jos haluat siirtää olemassa olevan kohdistetun määrän kohdistusryhmästä toiseen.

### <a name="query-existing-allocations"></a>Kyselyn tekeminen olemassa olevista kohdistuksista

Valitse **Tee kysely** ja syötä tuotteen, organisaation, dimension ja kohdistusryhmän arvot saadaksesi olemassa olevien kohdistusten kyselytulokset.
