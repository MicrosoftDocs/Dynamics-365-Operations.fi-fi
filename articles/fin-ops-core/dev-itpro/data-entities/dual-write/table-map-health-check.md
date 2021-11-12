---
title: Taulumäärityksen kuntotarkistusta koskevat virhekoodit
description: Tässä aiheessa kuvataan taulumäärityksen kuntotarkistusta koskevat virhekoodit.
author: nhelgren
ms.date: 10/04/2021
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.region: global
ms.author: nhelgren
ms.search.validFrom: 2021-10-04
ms.openlocfilehash: 4f0b92a6bc6c051a6bb24b49d3280ca5ecea3625
ms.sourcegitcommit: c4500b626667185643b3a2e7fc3a004d42198d07
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/29/2021
ms.locfileid: "7725072"
---
# <a name="errors-codes-for-the-table-map-health-check"></a>Taulumäärityksen kuntotarkistusta koskevat virhekoodit

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Tässä aiheessa kuvataan taulumäärityksen kuntotarkistusta koskevat virhekoodit.

## <a name="error-100"></a>Virhe 100

Virhesanoma on Finance and Operations -suositusten suorittaminen edellyttää vähintään Finance and Operations -ympäristön versiota PU 43.

Ominaisuus vaatii platform update -päivitykset Finance and Operations -sovellusten versioon 10.0.19 tai sitä uudempiin.

## <a name="error-400"></a>Virhe 400

Virhesanoma on Yksiköstä \{Finance and Operations UniqueEntityName\} ei löydetty liiketapahtumien rekisteröintitietoja, mikä tarkoittaa, että määritys ei ole käynnistä tai kaikki kenttämääritykset ovat yksisuuntaisia.

## <a name="error-500"></a>Virhe 500

Virhesanoma on Projektille \{projektin nimi\} ei löydy projektimäärityksiä. Tämä voi johtua joko siitä, että projekti ei ole käytössä tai kaikki kenttämääritykset ovat yksisuuntaisia Customer Engagementista Finance and Operationsiin.

Tarkista taulumäärityksen määritykset. Jos ne ovat yksisuuntaisia Customer Engagement -sovelluksista Finance and Operations -sovelluksiin, reaaliaikaiselle synkronoinnille Finance and Operations -sovelluksista Dataverseen ei luoda liikennettä.

## <a name="error-900"></a>Virhe 900

Virhesanomana on Virheellinen lähdesuodattimen \{sourceFilter\} muoto yksikölle \{Finance and Operations UniqueEntityName\}."

Finance and Operations -sovellusten taulumäärityksessä määritetty lähdesuodatin ei ole syntaksisesti oikein. Ohjeet suodatinperusteiden tarkistamiseen: [Reaaliaikaisen synkronoinnin ongelmien vianmääritys](dual-write-troubleshooting-live-sync.md#live-synchronization-issues-that-are-caused-by-incorrect-query-filter-syntax-on-the-dual-write-maps).

## <a name="error-1000"></a>Virhe 1000

Virhesanoma Yksikön \{Finance and Operations UniqueEntityName\} kaksoiskirjoituksen reaaliaikaiseen synkronointiin käytetty kysely on \{Finance and Operations EntityFilterQueryString\}. Tietueet, jotka täyttävät kyselyperusteet noudetaan reaaliaikaista synkronointia varten.

Palautettu yksikkökysely on yksikön SQL-kyselyn taustakysely. Tarkista sisäliitosten tai kyselysuodattimien varalta, jotka määrittävät reaaliaikaista synkronointia varten noudettavat liiketoimintatiedot. Sisäliitokset ja suodattimet ovat pakollisia ehtoja, jotka on täytettävä jokaisen kaksoiskirjoituksen reaaliaikaiseen synkronointiin noudettavan tietueen osalta.

## <a name="error-1300"></a>Virhe 1300

Virhesanoma on Yksikön \{Finance and Operations EntityMetadata.EntityProperties.LogicalEntityName\} virtuaalikenttiä \{s.EntityFieldName\} ei voi jäljittää kaksoiskirjoituksen osalta.

Finance and Operations -taulujen virtuaalikenttiä ei voi jäljittää. Reaaliaikainen synkronointi voi synkronoida tiedot, mutta se ei voi noutaa sarakkeisiin tehtyjä muutoksia.

## <a name="error-1500"></a>Virhe 1500

Virhesanoma on Vähintään yhden kentän on oltava määritettynä muuhun kuin hakukenttään Customer Engegementissa, jotta tietolähdettä \{datasource.DataSourceName\} voi jäljittää.

Yksikön tietolähteellä ei ole kaksoiskirjoitusta varten määritettyä kenttää. Pohjana olevaan tauluun tehtyjä muutoksia ei jäljitetä kaksoiskirjoituksen osalta.

## <a name="error-1600"></a>Virhe 1600

Virhesanoma on yksikön \{Finance and Operations EntityMetadata.EntityProperties.LogicalEntityName\} tietolähteellä \{datasource.DataSourceName\} on alue. Vain alue-ehtoa vastaavat tietueet noudetaan lähteviä varten.

Finance and Operations -sovellusten yksiköillä voi olla tietolähteitä, joissa on käytössä suodatinalueita. Nämä alueet määrittävät tietueet, jotka noudetaan reaaliaikaiseen synkronointiin. Jos joitakin tietueita ohitetaan Finance and Operations -sovelluksesta Dataverseen, tarkista, täyttävätkö tietueet yksikön alueperusteet. Yksinkertainen tapa tehdä tämä tarkistus on suorittaa SQL-kysely, joka muistuttaa seuraavaa esimerkkiä.

```sql
select * from <EntityName> where <filter criteria for the records> on SQL.
```

## <a name="error-1700"></a>Virhe 1700

Virhesanoma on Yksikön \{datasourceTable.Key.entityName\} taulua \{datasourceTable.Key.subscribedTableName\} jäljitetään yksikön \{origTableToEntityMaps.EntityName\} osalta. Useiden taulujen seuraaminen useiden yksikköjen osalta voi vaikutta järjestelmän suorituskykyyn reaaliaikaisissa synkronointitapahtumissa.

Jos useammat yksiköt seuraavat samaa taulua, muutokset tauluun käynnistävät kaksoiskirjoituksen arvioinnin linkitettyjen yksikköjen osalta. Vaikka suodatinlausekkeet lähettävät vain kelvolliset tietueet, arviointi saattaa aiheuttaa suorituskykyongelman, jos on olemassa pitkäkestoisia kyselyjä tai optimoimattomia kyselysuunnitelmia. Tätä ongelmaa ei ehkä voi välttää liiketoiminnan näkökulmasta. Jos kuitenkin useilla yksiköillä on useita risteäviä tauluja, kannattaa harkita yksikön yksinkertaistamista tai yksikkökyselyjen optimointien tarkistamista.

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
