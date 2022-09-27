---
title: Varaston näkyvyyssovellus
description: Tässä artikkelissa käsitellään varaston näkyvyyssovelluksen käyttämistä.
author: yufeihuang
ms.date: 09/15/2022
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2021-08-02
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: 674adb70cc4372a8c5ca8c75ed3ef840d8ec7b79
ms.sourcegitcommit: d2046cad5de570e6302a4390b41881a7ecb12e26
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/15/2022
ms.locfileid: "9520861"
---
# <a name="use-the-inventory-visibility-app"></a>Inventory Visibility -sovelluksen käyttäminen

[!include [banner](../includes/banner.md)]

Tässä artikkelissa käsitellään varaston näkyvyyssovelluksen käyttämistä.

Varaston näkyvyys on mallipohjainen visualisointisovellus. Sovelluksessa on kolme sivua: **Määritys**, **Toiminnon aikainen näkyvyys** ja **Varaston yhteenveto**. Siinä on seuraavat ominaisuudet:

- Se toimii käyttöliittymänä, jossa voi määrittää käytettävissä olevan varaston ja alustavan varauksen.
- Se tukee reaaliaikaisia käytettävissä olevan varaston kyselyjä erilaisten dimensioyhdistelmien avulla.
- Se toimii käyttöliittymänä, jolla voi kirjata varastopyyntöjä.
- Se antaa näkymän tuotteiden käytettävissä olevasta varastosta ja kaikista dimensioista.
- Se antaa näkymän tuotteiden varastosaldoluettelosta ja ennalta määritetyistä dimensioista.


## <a name="prerequisites"></a>Edellytykset

Varaston näkyvyyden apuohjelma on asennettava ja määritettävä ennen aloittamista kohdassa [Varaston näkyvyyden asennus ja määritys](inventory-visibility-setup.md) kuvatulla tavalla.

## <a name="open-the-inventory-visibility-app"></a>Varaston näkyvyyssovelluksen avaaminen

Voit avata varaston näkyvyyssovelluksen kirjautumalla Power Apps -ympäristöösi ja avaamalla **Varaston näkyvyyden**.

## <a name="configuration"></a><a name="configuration"></a>Määritys

Varaston näkyvyyssovelluksen **Määritys**-sivu auttaa määrittämään käytettävissä olevan varaston ja alustavan varauksen. Kun apuohjelma on asennettu, oletusmääritys sisältää Microsoft Dynamics 365 Supply Chain Managementin oletusmäärityksen (`fno`-tietolähde). Oletusasetus voidaan tarkistaa. Tämän jälkeen määritystä voidaan muokata liiketoimintatarpeiden ja ulkoisen järjestelmän varastokirjaustarpeiden mukaan siten, että useissa järjestelmissä käytetään standardoitua varastomuutosten kirjausta, järjestämistä ja kyselyä.

Täydelliset tiedot ratkaisun määrittämisestä: [Varaston näkyvyyden määritys](inventory-visibility-configuration.md).

## <a name="operational-visibility"></a>Toiminnon aikainen näkyvyys

**Toiminnon aikainen näkyvyys** -sivu antaa käytettävissä olevan varaston reaaliaikaiset tulokset erilaisten dimensioyhdistelmien perusteella. Kun *OnHandReservation*-ominaisuus on otettu käyttöön, varauspyyntöjä voi kirjata myös **Toiminnan aikainen näkyvyys** -sivulla.

### <a name="on-hand-query"></a>Varastosaldokysely

**Varastosaldokysely**-välilehdessä on reaaliaikaisen varastosaldokyselyn tulokset.

Kun **Toiminnon aikainen näkyvyys** -sivun **Varastosaldokysely**-välilehti avataan, järjestelmä kysyy tunnistetietotoja, joiden avulla se voi hakea haltijatunnuksen. Sitä tarvitaan kyselyn tekemiseen varaston näkyvyyspalvelussa. Haltijatunnus voidaan liittää **BearerToken**-kenttään ja valintaikkuna sulkea. Tämän jälkeen varastosaldokyselypyyntö voidaan kirjata.

Jos haltijatunnus ei kelpaa tai se on vanhentunut, liitä uusi tunnus **BearerToken**-kenttään. Anna oikeat **Asiakastunnus**-, **Vuokraajan tunnus** ja **Asiakasohjelman salaisuus** -arvot ja valitse **Päivitä**. Järjestelmä hakee automaattisesti uuden, kelvollisen haltijatunnuksen.

Kirjaa varastosaldokysely antamalla kysely pyynnön tekstiosassa. Käytä kaavaa, jota käsitellään kohdassa [Kysely kirjausmenetelmää käyttämällä](inventory-visibility-api.md#query-with-post-method).

![Varastosaldokyselyn asetukset](media/inventory-visibility-query-settings.png "Varastosaldokyselyn asetukset")

### <a name="reservation-posting"></a>Varauksen kirjaus

**Toiminnon aikainen näkyvyys** -sivun **Varauksen kirjaus** -välilehden avulla voit kirjata varauspyynnön. *OnHandReservation*-ominaisuus on otettava käyttöön ennen varauspyynnön kirjaamista. Lisätietoja tästä ominaisuudesta ja sen käyttöönotosta on kohdassa [Varaston näkyvyyssovelluksen varaukset](inventory-visibility-reservations.md).

Varauspyynnön kirjaaminen edellyttää, että arvo annetaan pyynnön tekstiosassa. Käytä kaavaa, jota käsitellään kohdassa [Yhden varauspyynnön luominen](inventory-visibility-api.md#create-one-reservation-event). Valitse sitten **Kirjaa**. Pyynnön vastaustietoja voidaan tarkastella valitsemalla **Näytä tiedot**. Myös `reservationId`-arvo voidaan saada vastauksen tiedoista.

## <a name="inventory-summary"></a><a name="inventory-summary"></a>Varaston yhteenveto

**Varaston yhteenveto** -sivu sisältää tuotteiden ja kaikkien dimensioiden varaston yhteenvedon. Se on mukautettu *Varastosaldon summa* -yksikön näkymä. Varaston yhteenvetotiedot synkronoidaan säännöllisesti varaston näkyvyydestä.

Seuraavien ohjeiden avulla voit ottaa **Varaston yhteenveto** -sivun käyttöön ja määrittää synkronointivälin:

1. Avaa **Määritykset**-sivu.
1. Avaa **Ominaisuuksien hallinta ja asetukset** -välilehti.
1. Määritä **OnHandMostSpecificBackgroundService**-toiminnon vaihtopainikkeen arvoksi *Kyllä*.
1. Kun toiminto on otettu käyttöön **Palvelun määritys** -osa on käytettävissä ja sisältää rivin **OnHandMostSpecificBackgroundService**-toiminnon määrittämistä varten. Tämän asetuksen avulla voit valita varaston yhteenvetotietojen synkronointivälin. Muuta synkronoinnin välistä aikaa **Arvo**-sarakkeen **Ylös**- ja **Alas**-painikkeiden avulla (pienin mahdollinen väli on 5 minuuttia). Valitse sitten **Tallenna**.

    ![OnHandMostSpecificBackgroundService-asetus](media/inventory-visibility-ohms-freq.png "OnHandMostSpecificBackgroundService-asetus")

1. Tallenna kaikki muutokset valitsemalla **Päivitä määritys**.


> [!NOTE]
> *OnHandMostSpecificBackgroundService*-ominaisuus seuraa vain käytettävissä olevan varaston muutoksia, jotka ovat tapahtuneet sen jälkeen, kun ominaisuus on otettu käyttöön. Niiden tuotteiden tietoja, jotka eivät ole muuttuneet sen jälkeen, kun olet ottanut toiminnon käyttöön, ei synkronoida varastopalvelun välimuistista ympäristöön Dataverse. Jos **Varaston yhteenveto** -sivulla ei ole kaikkia odotettuja käytettävissä olevia tietoja, avaa Supply Chain Management ja siirry kohtaan **Varastonhallinta > Kausittaiset tehtävät > Varaston näkyvyyden integrointi**, poista erätyö käytöstä ja ota se uudelleen käyttöön. Tämä toimii alkusysäyksenä, ja kaikki tiedot synkronoidaan *Käytettävissä olevan varaston summa* -yksikköön seuraavan 15 minuutin kuluttua. Jos haluat käyttää tätä *OnHandMostSpecificBackgroundService*-ominaisuutta, on suositeltavaa ottaa se käyttöön ennen käytettävissä olevan varaston muutosten luontia ja ottaa käyttöön **Varaston näkyvyyden integrointi** -erätyö.

## <a name="preload-a-streamlined-on-hand-query"></a><a name="preload-the-inventory-visibility-onhand-query"></a>Käytettävissä olevan varaston virtaviivaistetun kyselyn esilataaminen

[!INCLUDE [preview-banner-section](../../includes/preview-banner-section.md)]
<!-- KFM: Preview until further notice -->

Supply Chain Management tallentaa suuren osan nykyisen käytettävissä olevan varaston tiedoista ja määrittää ne käytettävissä oleviksi useita tarkoituksia varten. Monet päivittäiset toiminnot ja kolmannen osapuolen integroinnit edellyttävät kuitenkin vain pienen osajoukon näistä tiedoista. Kun järjestelmässä tehdään kysely kaikista tiedoista, saatetaan tulokseksi saadaan suuria tietojoukkoja, joiden kokoaminen ja siirtäminen kestää kauan. Tämän vuoksi varaston näkyvyyspalvelu voi säännöllisesti hakea ja tallentaa tehostetun käytettävissä olevan varaston tietojen joukon, jolloin optimoidut tiedot ovat jatkuvasti käytettävissä. Tallennetut käytettävissä olevan varaston tiedot suodatetaan määritettyjen liiketoiminnan ehtojen perusteella. Näin varmistetaan, että vain olennaiset tiedot ovat mukana. Koska suodatut käytettävissä olevan varaston luettelot tallennetaan paikallisesti varaston näkyvyyspalveluun ja päivitetään säännöllisesti, ne tukevat nopeaa käyttöä, tarvittavien tietojen vientejä ja ulkoisten järjestelmien tehostettua integrointia.

> [!NOTE]
> Tämän ominaisuuden nykyinen esiversio voi määrittää vain esiladatut tulokset, jotka sisältävät sivuston ja sijainnin. Ominaisuuden lopullisen version tulee mahdollistaa muiden dimensioiden valinta, jotta esilataus tulosten kanssa on mahdollista.

**Varaston näkyvyyden yhteenvedon esilataus** -sivulla on *Käytettävissä olevan varaston indeksin kyselyn esilatauksen tulokset* -entiteetin näkymä. Toisin kuin *Varaston yhteenveto* -entiteetti, *Käytettävissä olevan varaston indeksin kyselyn esilatauksen tulokset* -entiteetti määrittää tuotteiden käytettävissä olevan varaston luettelon yhdessä valittujen dimensioiden kanssa. Varaston näkyvyys synkronoi esiladatut yhteenvetotiedot 15 minuutin välein.

Jos haluat tarkastella **Varaston näkyvyyden yhteenvedon esilataus** -välilehteä, ota käyttöön *OnHandIndexQueryPreloadBackgroundService*-ominaisuus **Määritys**-sivun **Ominaisuuksien hallinta** -välilehdessä. Valitse **Päivitä määritys** (katso myös [Varaston näkyvyyden määrittäminen](inventory-visibility-configuration.md) -kohta).

> [!NOTE]
> Kuten *OnhandMostSpecificBackgroudService*-ominaisuuden kohdalla, *OnHandIndexQueryPreloadBackgroundService*-ominaisuus käsittelee vain käytettävissä olevan varaston muutoksia, jotka ovat tapahtuneet ominaisuuden käyttöönoton jälkeen. Niiden tuotteiden tietoja, jotka eivät ole muuttuneet sen jälkeen, kun olet ottanut toiminnon käyttöön, ei synkronoida varastopalvelun välimuistista ympäristöön Dataverse. Jos **Varaston yhteenveto** -sivulla ei ole kaikkia odotettuja käytettävissä olevia tietoja, siirry kohtaan **Varastonhallinta > Kausittaiset tehtävät > Varaston näkyvyyden integrointi**, poista erätyö käytöstä ja ota se uudelleen käyttöön. Tämä toimii alkusysäyksenä, ja kaikki tiedot synkronoidaan *Käytettävissä olevan varaston indeksin kyselyn esilatauksen tulokset* -yksikköön seuraavan 15 minuutin kuluttua. Jos haluat käyttää tätä toimintoa, on suositeltavaa ottaa se käyttöön ennen käytettävissä olevan varaston muutosten luontia ja ottaa käyttöön **Varaston näkyvyyden integrointi** -erätyö.

## <a name="filter-and-browse-the-inventory-summaries"></a><a name="additional-tip-for-viewing-data"></a>Varaston yhteenvetojen suodattaminen ja selaaminen

Dataversen **lisäsuodattimen** avulla voi luoda oman näkymän, jossa on näkyvissä itselle tärkeät rivit. Lisäsuodatinvaihtoehtojen avulla voi luoda monenlaisia niin yksinkertaisia kuin monimutkaisiakin näkymiä. Lisäksi niiden avulla voidaan lisätä ryhmiteltyjä ja sisäkkäisiä ehtoja suodattimiin. Lisätietoja lisäsuodattimen käyttämisestä on kohdassa [Omien näkymien muokkaaminen tai luominen lisäruudukkosuodattimien avulla](/powerapps/user/grid-filters-advanced).

**Varaston yhteenveto** -sivulla ruudukon yläpuolella on kolme kenttää (**Oletusdimensio**, **Mukautettu dimensio** ja **Mittari**), joiden avulla voit määrittää, mitkä sarakkeet ovat näkyvissä. Nykyisen tuloksen voi myös suodattaa tai lajitella minkä tahansa sarakeotsikon kyseisen sarakkeen avulla. Seuraavassa näyttökuvassa ovat **Varaston yhteenveto** -sivulla käytettävissä ovat dimension, suodatuksen, tulosten määrän ja Lataa lisää -kenttien tärkeimmät kohdat.

![Varaston yhteenveto -sivu.](media/inventory-visibility-onhand-list.png "Varaston yhteenveto -sivu")

**Varaston näkyvyyden yhteenvedon esilataus** -sivulla näkyvät dimensioon liittyvät sarakkeet, koska yhteenvetotietojen lataukseen on käytetty ennalta määritettyjä dimensioita. *Dimensioita ei mukauteta, vaan järjestelmä vain tukee käytettävissä olevan varaston luetteloiden sivuston ja sijainnin dimensioita.* **Varaston näkyvyyden yhteenvedon esilataus** -sivulla ovat suodattimet, jotka ovat samanlaisia kuin **Varaston yhteenveto** -sivulla olevat valittuja dimensioita lukuun ottamatta. Seuraavassa näyttökuvassa ovat **Varaston näkyvyyden yhteenvedon esilataus** -sivulla olevat suodatuskentät.

![Varaston näkyvyyden yhteenvedon esilataus -sivu.](media/inventory-visibility-preload-onhand-list.png "Varaston näkyvyyden yhteenvedon esilataus -sivu")

**Varaston näkyvyyden yhteenvedon esilataus**- ja  **Varaston yhteenveto** -sivuilla on tietoja, kuten "50 tietuetta (29 valittua)" tai "50 tietuetta". Nämä tiedot viittaavat **Lisäsuodatin**-tuloksista ladattuina oleviin tietueisiin. Teksti 29 valittu viittaa tietueiden määrään, jotka on valittu käyttämällä ladattujen tietueiden sarakeotsikkosuodatinta. Näkyvissä on myös **Lataa lisää** -painike, jolla voi ladata lisää tietueita Dataversesta. Ladattavien tietueiden oletusmäärä on 50. Kun **Lataa lisää** valitaan, seuraavat 1 000 käytettävissä olevaa tietuetta ladataan näkymään. **Lataa lisää** -painikkeessa oleva luku ilmaisee ladattuina olevien tietueiden määrän ja **Lisäsuodatin**-tuloksen tietueiden kokonaismäärän.
