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
ms.openlocfilehash: 0a4e436cc1af6b71049f75fb66bdfb89ca38df9f
ms.sourcegitcommit: 0c927fcb3afd34d870391f05b5393a4673d916e5
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/08/2022
ms.locfileid: "9831771"
---
# <a name="use-the-inventory-visibility-app"></a>Inventory Visibility -sovelluksen käyttäminen

[!include [banner](../includes/banner.md)]

Tässä artikkelissa käsitellään varaston näkyvyyssovelluksen käyttämistä.

Varaston näkyvyys on mallipohjainen visualisointisovellus. Sovelluksessa on kolme sivua: **Määritys**, **Toiminnon aikainen näkyvyys** ja **Varaston yhteenveto**. Siinä on seuraavat ominaisuudet:

- Se toimii käyttöliittymänä, jossa voi määrittää käytettävissä olevan varaston ja alustavan varauksen.
- Se tukee reaaliaikaisia käytettävissä olevan varaston kyselyjä erilaisten dimensioyhdistelmien avulla.
- Se toimii käyttöliittymänä, jolla voi kirjata varastopyyntöjä.
- Se antaa näkymän tuotteiden käytettävissä olevasta varastosta ja kaikista dimensioista.
- Se antaa näkymän tuotteiden varastosaldoluettelosta ja ennalta määritetyistä dimensioista. Varastosaldon luettelonäkymässä voi olla koko yhteenveto tai varastosaldokyselyn esiladatut tulokset.

## <a name="prerequisites"></a>Edellytykset

Varaston näkyvyyden apuohjelma on asennettava ja määritettävä ennen aloittamista kohdassa [Varaston näkyvyyden asennus ja määritys](inventory-visibility-setup.md) kuvatulla tavalla.

## <a name="open-and-authenticate-the-inventory-visibility-app"></a><a name="open-authenticate"></a>Inventory Visibility -sovelluksen avaaminen ja todentaminen

Avaa ja todenna Inventory Visibility -sovellus alla olevien ohjeiden avulla.

1. Kirjaudu Power Apps -ympäristöön.
1. Avaa **Inventory Visibility** -sovellus.
1. Avaa **Operational Visibility** -sivu vasemmanpuoleisessa ruudussa.
1. Valitse **Asetukset**-painike (rataskuvake) sivun yläosassa.
1. Syötä **Asetukset**-valintaikkunaan **Asiakastunnus**-,**Vuokraajan tunnus**- ja **Asiakkaan salasana** -arvot, jotka kirjoitit muistiin [Inventory Visibilityn asentamisen ja määrittämisen](inventory-visibility-setup.md) yhteydessä.
1. Valitse **Päivitä**-painike **Haltijatunnus**-kentän vieressä. Järjestelmä luo uuden haltijatunnuksen syötettyjen tietojen perusteella.

    ![Varastosaldokyselyn asetukset.](media/inventory-visibility-query-settings.png "Varastosaldokyselyn asetukset")

1. Kun saat sallitun haltijatunnuksen, sulje valintaikkuna. Haltijatunnus vanhenee jonkin ajan kuluttua. Tämän vuoksi päivitys on tehtävä tarvittaessa määrityksen, kirjaustietojen tai kyselytietojen päivittämisen yhteydessä.

## <a name="configure-the-inventory-visibility-app"></a><a name="configuration"></a>Inventory Visibility -sovelluksen määrittäminen

Inventory Visibility -sovelluksen **Määritys**-sivu auttaa määrittämään yleistietojen hallinnan määrityksen ja ominaisuuksien määrityksen. Kun apuohjelma on asennettu, oletusmääritys sisältää Microsoft Dynamics 365 Supply Chain Managementin oletusmäärityksen (`fno`-tietolähde). Oletusasetus voidaan tarkistaa. Tämän jälkeen määritystä voidaan muokata liiketoimintatarpeiden ja ulkoisen järjestelmän varastokirjaustarpeiden mukaan siten, että useissa järjestelmissä käytetään standardoitua varastomuutosten kirjausta, järjestämistä ja kyselyä.

Täydelliset tiedot ratkaisun määrittämisestä: [Varaston näkyvyyden määritys](inventory-visibility-configuration.md).

## <a name="operational-visibility"></a>Toiminnon aikainen näkyvyys

**Toiminnon aikainen näkyvyys** -sivu antaa varastosaldon varastokyselyn, varauksen kirjauksen ja kohdistuksen reaaliaikaiset tulokset erilaisten dimensioyhdistelmien perusteella. Kun *OnHandReservation*-ominaisuus on [otettu käyttöön](inventory-visibility-configuration.md), voit myös kirjata varauspyynnöt **Toiminnon aikainen näkyvyys** -sivulta.

### <a name="on-hand-query"></a>Varastosaldokysely

**Varastosaldokysely**-välilehdessä **Toiminnon aikainen näkyvyys** -sivulla voit tehdä reaaliaikaisen kyselyn varastosaldosta. Näiden ohjeiden avulla voit määrittää ja suorittaa kyselyn.

1. Avaa **Inventory Visibility** -sovellus.
1. Avaa **Operational Visibility** -sivu vasemmanpuoleisessa ruudussa.
1. Syötä **Varastosaldokysely**-välilehdessä **Organisaation tunnus**-, **Toimipaikan tunnus**- ja **Sijainnin tunnus** -arvot, joista kysely tehdään.
1. Syötä **Tuotetunnus**-kenttään vähintään yksi tuotetunnus, jotta saat kyselylle tarkan vastaavuuden. Jos jätät **Tuotetunnus**-kentän tyhjäksi, tuloksissa on kaikki tuotteet tietyssä toimipaikassa ja sijainnissa.
1. Jos haluat saada tarkempia tuloksia (esimerkiksi näkymän dimension arvojen, kuten värin ja koon, mukaan), valitse ryhmittele dimensioiden mukaan **Tulosten ryhmittelyperuste** -kentässä.
1. Voit etsiä nimikkeitä, joilla on tietty dimension arvo (esimerkiksi väri = punainen) valitsemalla dimension **Suodata dimensiot** -kentässä ja syöttämällä dimension arvon.
1. Valitse **Tee kysely**. Näkyviin tulee onnistumissanoma (vihreä) tai epäonnistumisesta kertova sanoma (punainen). Jos kysely epäonnistuu, tarkista kyselyehdot ja varmista, [haltijatunnus](#open-authenticate) ei ole vanhentunut.

Toinen tapa varastosaldokyselyn tekemiseksi on tehdä suoria ohjelmointirajapintapyyntöjä. Voit käyttää kyselyä `/api/environment/{environmentId}/onhand/indexquery` tai `/api/environment/{environmentId}/onhand`. Lisätietoja on kohdassa [Varaston näkyvyyden julkiset API:t](inventory-visibility-api.md).

### <a name="reservation-posting"></a>Varauksen kirjaus

**Toiminnon aikainen näkyvyys** -sivun **Varauksen kirjaus** -välilehden avulla voit kirjata varauspyynnön. *OnHandReservation*-ominaisuus on otettava käyttöön ennen varauspyynnön kirjaamista. Lisätietoja tästä ominaisuudesta ja sen käyttöönotosta on kohdassa [Varaston näkyvyyssovelluksen varaukset](inventory-visibility-reservations.md).

> [!NOTE]
> Ominaisuutta voi testata käyttöliittymän alustavan varauksen tekemisen mahdollisuuden vuoksi. Jokainen alustavan varauksen pyyntö on liitettävä tapahtuman tilausrivin muutokseen (esimerkiksi luonti, muokkaus tai poisto). Siksi on suositeltavaa tehdä vain taustatilaukseen linkitettyjä alustavia varauksia. Lisätietoja on kohdassa [Varaston näkyvyyden varaukset](inventory-visibility-reservations.md).

Näiden ohjeiden avulla voit kirjata alustavan varauksen pyynnön käyttöliittymän avulla.

1. Avaa **Inventory Visibility** -sovellus.
1. Avaa **Operational Visibility** -sivu vasemmanpuoleisessa ruudussa.
1. Määritä **Varauksen kirjaus** -välilehden **Määrä**-kentässä alustavan varauksen määrä.
1. Tyhjennä **Ota käyttöön negatiivinen varasto ylimyynnin tukemiseksi** -valintaruudun valinta estääksesi varaston ylimyynti tai ylivaraus.
1. Valitse **Operaattori**-kentässä tietolähde ja fyysinen mitta, jotka koskevat alustavasti varattua määrää.
1. Syötä kyselyä varten **Organisaation tunnus**-, **Toimipaikan tunnus**-, **Sijainnin tunnus**- ja **Tuotetunnus**-arvot.
1. Jos haluat yksityiskohtaiset tulokset, valitse tietolähde, dimensiot ja dimensioiden arvot.

Toinen tapa kirjata alustava varaus on tehdä suoria ohjelmointirajapintapyyntöjä. Käytä kaavaa, jota käsitellään kohdassa [Yhden varauspyynnön luominen](inventory-visibility-api.md#create-one-reservation-event). Valitse sitten **Kirjaa**. Pyynnön vastaustietoja voidaan tarkastella valitsemalla **Näytä tiedot**. Myös `reservationId`-arvo voidaan saada vastauksen tiedoista.

### <a name="allocation"></a>Kohdistus

Lisätietoja käyttöliittymän ja ohjelmointirajapintojen kohdistusten hallinnasta on kohdassa [Inventory Visibilityn varaston kohdistus](inventory-visibility-allocation.md).

## <a name="inventory-summary"></a><a name="inventory-summary"></a>Varaston yhteenveto

**Varaston yhteenveto** -sivu sisältää tuotteiden ja kaikkien dimensioiden varaston yhteenvedon. Se on mukautettu *Varastosaldon summa* -yksikön näkymä. Varaston yhteenvetotiedot synkronoidaan säännöllisesti varaston näkyvyydestä.

Seuraavien ohjeiden avulla voit ottaa **Varaston yhteenveto** -sivun käyttöön ja määrittää synkronointivälin:

1. Avaa **Määritykset**-sivu.
1. Avaa **Ominaisuuksien hallinta ja asetukset** -välilehti.
1. Määritä *OnHandMostSpecificBackgroundService*-toiminnon vaihtopainikkeen arvoksi *Kyllä*.
1. Kun toiminto on otettu käyttöön **Palvelun määritys** -osa on käytettävissä ja sisältää rivin **OnHandMostSpecificBackgroundService**-toiminnon määrittämistä varten. Tämän asetuksen avulla voit valita varaston yhteenvetotietojen synkronointivälin. Muuta synkronoinnin välistä aikaa **Arvo**-sarakkeen **Ylös**- ja **Alas**-painikkeiden avulla (pienin mahdollinen väli on 5 minuuttia). Valitse sitten **Tallenna**.

    ![OnHandMostSpecificBackgroundService-asetus](media/inventory-visibility-ohms-freq.png "OnHandMostSpecificBackgroundService-asetus")

1. Tallenna kaikki muutokset valitsemalla **Päivitä määritys**.

> [!NOTE]
> *OnHandMostSpecificBackgroundService*-ominaisuus seuraa vain käytettävissä olevan varaston muutoksia, jotka ovat tapahtuneet sen jälkeen, kun ominaisuus on otettu käyttöön. Niiden tuotteiden tietoja, jotka eivät ole muuttuneet sen jälkeen, kun olet ottanut toiminnon käyttöön, ei synkronoida varastopalvelun välimuistista ympäristöön Dataverse. Jos **Varaston yhteenveto** -sivulla ei ole kaikkia odotettuja käytettävissä olevia tietoja, avaa Supply Chain Management ja siirry kohtaan **Varastonhallinta > Kausittaiset tehtävät > Varaston näkyvyyden integrointi**, poista erätyö käytöstä ja ota se uudelleen käyttöön. Tämä toimii alkusysäyksenä, ja kaikki tiedot synkronoidaan *Käytettävissä olevan varaston summa* -yksikköön seuraavan 15 minuutin kuluttua. Jos haluat käyttää tätä *OnHandMostSpecificBackgroundService*-ominaisuutta, on suositeltavaa ottaa se käyttöön ennen käytettävissä olevan varaston muutosten luontia ja ottaa käyttöön **Varaston näkyvyyden integrointi** -erätyö.

## <a name="preload-a-streamlined-on-hand-query"></a><a name="preload-streamlined-onhand-query"></a>Käytettävissä olevan varaston virtaviivaistetun kyselyn esilataaminen

[!INCLUDE [preview-banner-section](../../includes/preview-banner-section.md)]
<!-- KFM: Preview until further notice -->

Supply Chain Management tallentaa suuren osan nykyisen käytettävissä olevan varaston tiedoista ja määrittää ne käytettävissä oleviksi useita tarkoituksia varten. Monet päivittäiset toiminnot ja kolmannen osapuolen integroinnit edellyttävät kuitenkin vain pienen osajoukon näistä tiedoista. Kun järjestelmässä tehdään kysely kaikista tiedoista, saatetaan tulokseksi saadaan suuria tietojoukkoja, joiden kokoaminen ja siirtäminen kestää kauan. Tämän vuoksi varaston näkyvyyspalvelu voi säännöllisesti hakea ja tallentaa tehostetun käytettävissä olevan varaston tietojen joukon, jolloin optimoidut tiedot ovat jatkuvasti käytettävissä. Tallennetut käytettävissä olevan varaston tiedot suodatetaan määritettyjen liiketoiminnan ehtojen perusteella. Näin varmistetaan, että vain olennaiset tiedot ovat mukana. Koska suodatut käytettävissä olevan varaston luettelot tallennetaan paikallisesti varaston näkyvyyspalveluun ja päivitetään säännöllisesti, ne tukevat nopeaa käyttöä, tarvittavien tietojen vientejä ja ulkoisten järjestelmien tehostettua integrointia.

**Varaston näkyvyyden yhteenvedon esilataus** -sivulla on *Käytettävissä olevan varaston indeksin kyselyn esilatauksen tulokset* -entiteetin näkymä. Toisin kuin *Varaston yhteenveto* -entiteetti, *Käytettävissä olevan varaston indeksin kyselyn esilatauksen tulokset* -entiteetti määrittää tuotteiden käytettävissä olevan varaston luettelon yhdessä valittujen dimensioiden kanssa. Varaston näkyvyys synkronoi esiladatut yhteenvetotiedot 15 minuutin välein.

Tietojen tarkasteleminen **Esilataa Varaston näkyvyys -yhteenveto** -välilehdessä edellyttää, että *OnHandIndexQueryPreloadBackgroundService*-ominaisuus otetaan käyttöön ja määritetään. Ohjeet ovat kohdassa [Valmiiksi ladattujen varastosaldokyselyjen ottaminen käyttöön ja määrittäminen](inventory-visibility-configuration.md#query-preload-configuration).

> [!NOTE]
> *OnHandMostSpecificBackgroundService*-ominaisuuden tavoin *OnHandIndexQueryPreloadBackgroundService*-ominaisuus käsittelee vain käytettävissä olevan varaston muutoksia, jotka ovat tapahtuneet ominaisuuden käyttöönoton jälkeen. Niiden tuotteiden tietoja, jotka eivät ole muuttuneet sen jälkeen, kun olet ottanut toiminnon käyttöön, ei synkronoida varastopalvelun välimuistista ympäristöön Dataverse. Jos **Varaston yhteenveto** -sivulla ei ole kaikkia odotettuja käytettävissä olevia tietoja, siirry kohtaan **Varastonhallinta > Kausittaiset tehtävät > Varaston näkyvyyden integrointi**, poista erätyö käytöstä ja ota se uudelleen käyttöön. Tämä toimii alkusysäyksenä, ja kaikki tiedot synkronoidaan *Käytettävissä olevan varaston indeksin kyselyn esilatauksen tulokset* -yksikköön seuraavan 15 minuutin kuluttua. Jos haluat käyttää tätä toimintoa, on suositeltavaa ottaa se käyttöön ennen käytettävissä olevan varaston muutosten luontia ja ottaa käyttöön **Varaston näkyvyyden integrointi** -erätyö.

## <a name="filter-and-browse-the-inventory-summaries"></a><a name="additional-tip-for-viewing-data"></a>Varaston yhteenvetojen suodattaminen ja selaaminen

Dataversen **lisäsuodattimen** avulla voi luoda oman näkymän, jossa on näkyvissä itselle tärkeät rivit. Lisäsuodatinvaihtoehtojen avulla voi luoda monenlaisia niin yksinkertaisia kuin monimutkaisiakin näkymiä. Lisäksi niiden avulla voidaan lisätä ryhmiteltyjä ja sisäkkäisiä ehtoja suodattimiin. Lisätietoja lisäsuodattimen käyttämisestä on kohdassa [Omien näkymien muokkaaminen tai luominen lisäruudukkosuodattimien avulla](/powerapps/user/grid-filters-advanced).

**Varaston yhteenveto** -sivulla ruudukon yläpuolella on kolme kenttää (**Oletusdimensio**, **Mukautettu dimensio** ja **Mittari**), joiden avulla voit määrittää, mitkä sarakkeet ovat näkyvissä. Nykyisen tuloksen voi myös suodattaa tai lajitella minkä tahansa sarakeotsikon kyseisen sarakkeen avulla. Seuraavassa näyttökuvassa ovat **Varaston yhteenveto** -sivulla käytettävissä ovat dimension, suodatuksen, tulosten määrän ja Lataa lisää -kenttien tärkeimmät kohdat.

![Varaston yhteenveto -sivu.](media/inventory-visibility-onhand-list.png "Varaston yhteenveto -sivu")

**Inventory Visibility -yhteenvedon esilataus** -sivulla näkyvät dimensioon liittyvät sarakkeet, koska yhteenvetotietojen lataukseen on käytetty ennalta määritettyjä dimensioita. *Dimensioita ei mukauteta, vaan järjestelmä vain tukee käytettävissä olevan varaston luetteloiden sivuston ja sijainnin dimensioita.* **Varaston näkyvyyden yhteenvedon esilataus** -sivulla ovat suodattimet, jotka ovat samanlaisia kuin **Varaston yhteenveto** -sivulla olevat valittuja dimensioita lukuun ottamatta. Seuraavassa näyttökuvassa ovat **Varaston näkyvyyden yhteenvedon esilataus** -sivulla olevat suodatuskentät.

![Varaston näkyvyyden yhteenvedon esilataus -sivu.](media/inventory-visibility-preload-onhand-list.png "Varaston näkyvyyden yhteenvedon esilataus -sivu")

**Varaston näkyvyyden yhteenvedon esilataus**- ja  **Varaston yhteenveto** -sivuilla on tietoja, kuten "50 tietuetta (29 valittua)" tai "50 tietuetta". Nämä tiedot viittaavat **Lisäsuodatin**-tuloksista ladattuina oleviin tietueisiin. Teksti 29 valittu viittaa tietueiden määrään, jotka on valittu käyttämällä ladattujen tietueiden sarakeotsikkosuodatinta. Näkyvissä on myös **Lataa lisää** -painike, jolla voi ladata lisää tietueita Dataversesta. Ladattavien tietueiden oletusmäärä on 50. Kun **Lataa lisää** valitaan, seuraavat 1 000 käytettävissä olevaa tietuetta ladataan näkymään. **Lataa lisää** -painikkeessa oleva luku ilmaisee ladattuina olevien tietueiden määrän ja **Lisäsuodatin**-tuloksen tietueiden kokonaismäärän.
