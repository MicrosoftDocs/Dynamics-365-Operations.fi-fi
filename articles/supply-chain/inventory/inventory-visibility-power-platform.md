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
ms.openlocfilehash: 0457190f2fc8cd0ed39e109e6720509b77b83566
ms.sourcegitcommit: 1e5a46271bf7fae2f958d2b1b666a8d2583e04a8
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/25/2021
ms.locfileid: "7678516"
---
# <a name="use-the-inventory-visibility-app"></a>Varaston näkyvyyssovelluksen käyttö

[!include [banner](../includes/banner.md)]
[!INCLUDE [cc-data-platform-banner](../../includes/cc-data-platform-banner.md)]

Tässä aiheessa käsitellään varaston näkyvyyssovelluksen käyttämistä.

Varaston näkyvyys on mallipohjainen visualisointisovellus. Sovelluksessa on kolme sivua: **Määritys**, **Toiminnon aikainen näkyvyys** ja **Varaston yhteenveto**. Siinä on seuraavat ominaisuudet:

- Se toimii käyttöliittymänä, jossa voi määrittää käytettävissä olevan varaston ja alustavan varauksen.
- Se tukee reaaliaikaisia käytettävissä olevan varaston kyselyjä erilaisten dimensioyhdistelmien avulla.
- Se toimii käyttöliittymänä, jolla voi kirjata varastopyyntöjä.
- Se antaa mukautetun näkymän tuotteiden käytettävissä olevasta varastosta ja kaikista dimensioista.

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

Kun **Varastosaldokysely**-välilehti valitaan, järjestelmä kysyy tunnistetietotoja, joiden avulla se voi hakea haltijatunnuksen, jota tarvitaan kyselyn tekemiseen varaston näkyvyyspalvelussa. Haltijatunnus voidaan liittää **BearerToken**-kenttään ja valintaikkuna sulkea. Tämän jälkeen varastosaldokyselypyyntö voidaan kirjata.

Jos haltijatunnus ei kelpaa tai se on vanhentunut, liitä uusi tunnus **BearerToken**-kenttään. Anna oikeat **Asiakastunnus**-, **Vuokraajan tunnus** ja **Asiakasohjelman salaisuus** -arvot ja valitse **Päivitä**. Järjestelmä hakee automaattisesti uuden, kelvollisen haltijatunnuksen.

Kirjaa varastosaldokysely antamalla kysely pyynnön tekstiosassa. Käytä kaavaa, jota käsitellään kohdassa [Kysely kirjausmenetelmää käyttämällä](inventory-visibility-api.md#query-with-post-method).

![Varastosaldokyselyn asetukset](media/inventory-visibility-query-settings.png "Varastosaldokyselyn asetukset")

### <a name="reservation-posting"></a>Varauksen kirjaus

Kirjaa varastopyyntö **Varastokirjaus**-välilehdessä. *OnHandReservation*-ominaisuus on otettava käyttöön ennen varauspyynnön kirjaamista. Lisätietoja tästä ominaisuudesta on kohdassa [Varaston näkyvyyssovelluksen varaukset](inventory-visibility-reservations.md).

Varauspyynnön kirjaaminen edellyttää, että arvo annetaan pyynnön tekstiosassa. Käytä kaavaa, jota käsitellään kohdassa [Yhden varauspyynnön luominen](inventory-visibility-api.md#create-one-reservation-event). Valitse sitten **Kirjaa**. Pyynnön vastaustietoja voidaan tarkastella valitsemalla **Näytä tiedot**. Myös `reservationId`-arvo voidaan saada vastauksen tiedoista.

## <a name="inventory-summary"></a><a name="inventory-summary"></a>Varaston yhteenveto

**Varaston yhteenveto** on mukautettu *Varastosaldon summa* -yksikön näkymä. Se sisältää tuotteiden ja kaikkien dimensioiden varaston yhteenvedon. Varaston yhteenvetotiedot synkronoidaan säännöllisesti varaston näkyvyydestä. Ennen kuin voit nähdä tiedot **Varaston yhteenveto**-välilehdessä, sinun on otettava käyttöön *OnHandMostSpecificBackgroundService*-ominaisuus **Ominaisuuksienhallinta**-välilehdessä.

Dataversen **lisäsuodattimen** avulla voi luoda oman näkymän, jossa on näkyvissä itselle tärkeät rivit. Lisäsuodatinvaihtoehtojen avulla voi luoda monenlaisia niin yksinkertaisia kuin monimutkaisiakin näkymiä. Lisäksi niiden avulla voidaan lisätä ryhmiteltyjä ja sisäkkäisiä ehtoja suodattimiin. Lisätietoja **lisäsuodattimen** käyttämisestä on kohdassa [Omien näkymien muokkaaminen tai luominen lisäruudukkosuodattimien avulla](/powerapps/user/grid-filters-advanced).

Mukautetun näkymän yläosassa on kolme kenttää: **Oletusdimensio**, **Mukautettu dimensio** ja **Mitta**. Näiden kenttien avulla voidaan hallita näkyvissä olevia kenttiä.

Nykyisen tuloksen voi suodattaa tai lajitella valitun sarakeotsikon avulla.

Mukautetun näkymän alareunassa on tietoja, kuten 50 tietuetta (29 valittu) tai 50 tietuetta. Nämä tiedot viittaavat **Lisäsuodatin**-tuloksista ladattuina oleviin tietueisiin. Teksti 29 valittu viittaa tietueiden määrään, jotka on valittu käyttämällä ladattujen tietueiden sarakeotsikkosuodatinta.

Näkymän alareunassa on **Lataa lisää** -painike, jolla voi ladata lisää tietueita Dataversesta. Ladattavien tietueiden oletusmäärä on 50. Kun **Lataa lisää** valitaan, seuraavat 1 000 käytettävissä olevaa tietuetta ladataan näkymään. **Lataa lisää** -painikkeessa oleva luku ilmaisee ladattuina olevien tietueiden määrän ja **Lisäsuodatin**-tuloksen tietueiden kokonaismäärän.

![Varaston yhteenveto](media/inventory-visibility-onhand-list.png "Varaston yhteenveto")
