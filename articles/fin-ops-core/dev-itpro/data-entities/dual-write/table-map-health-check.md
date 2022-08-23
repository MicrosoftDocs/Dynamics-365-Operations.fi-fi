---
title: Taulumäärityksen kuntotarkistusta koskevat virhekoodit
description: Tässä artikkelissa kuvataan taulumäärityksen kuntotarkistusta koskevat virhekoodit.
author: RamaKrishnamoorthy
ms.date: 05/31/2022
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2021-10-04
ms.openlocfilehash: d3f413f34296fd01da6741bb49658285394cbd17
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/12/2022
ms.locfileid: "9288757"
---
# <a name="errors-codes-for-the-table-map-health-check"></a>Taulumäärityksen kuntotarkistusta koskevat virhekoodit

[!include [banner](../../includes/banner.md)]



Tässä artikkelissa kuvataan taulumäärityksen kuntotarkistusta koskevat virhekoodit.

## <a name="error-100"></a>Virhe 100

Virheilmoitus on Talous- ja toimintosovellusten ympäristöversion on oltava vähintään PU 43, jotta talous- ja toimintosovellussuositukset voidaan suorittaa.

Ominaisuus vaatii talous- ja toimintosovellusten version 10.0.19 tai sitä uudempien Platform update -päivitykset.

## <a name="error-400"></a>Virhe 400

Virhesanoma on Yksiköstä \{Talous- ja toimintosovellusten UniqueEntityName\} ei löydetty liiketapahtumien rekisteröintitietoja, mikä tarkoittaa, että määritys ei ole käynnissä tai että kaikki kenttämääritykset ovat yksisuuntaisia.

## <a name="error-500"></a>Virhe 500

Virhesanoma on Projektille \{projektin nimi\} ei löydy projektimäärityksiä. Tämä voi johtua joko siitä, että projekti ei ole käytössä tai kaikki kenttämääritykset ovat yksisuuntaisia asiakasvuorovaikutussovelluksesta talous- ja toimintosovelluksiin.

Tarkista taulumäärityksen määritykset. Jos ne ovat yksisuuntaisia asiakasvuorovaikutussovelluksista talous- ja toimintosovelluksiin, reaaliaikaiselle synkronoinnille talous- ja toimintosovelluksista Dataverseen ei luoda liikennettä.

## <a name="error-900"></a>Virhe 900

Virhesanomana on Virheellinen lähdesuodattimen \{sourceFilter\} muoto yksikölle \{Talous- ja toimintosovellusten UniqueEntityName\}.

Talous- ja toimintosovellusten taulumäärityksessä määritetty lähdesuodatin ei ole syntaktisesti oikein. Ohjeet suodatinperusteiden tarkistamiseen: [Reaaliaikaisen synkronoinnin ongelmien vianmääritys](dual-write-troubleshooting-live-sync.md#live-synchronization-issues-that-are-caused-by-incorrect-query-filter-syntax-on-the-dual-write-maps).

## <a name="error-1000"></a>Virhe 1000

Virhesanoma on Yksikön \{Talous- ja toimintosovellusten UniqueEntityName\} kaksoiskirjoituksen reaaliaikaiseen synkronointiin käytetty kysely on \{Talous- ja toimintosovellusten EntityFilterQueryString\}". Tietueet, jotka täyttävät kyselyperusteet noudetaan reaaliaikaista synkronointia varten.

Palautettu yksikkökysely on yksikön SQL-kyselyn taustakysely. Tarkista sisäliitosten tai kyselysuodattimien varalta, jotka määrittävät reaaliaikaista synkronointia varten noudettavat liiketoimintatiedot. Sisäliitokset ja suodattimet ovat pakollisia ehtoja, jotka on täytettävä jokaisen kaksoiskirjoituksen reaaliaikaiseen synkronointiin noudettavan tietueen osalta.

## <a name="error-1300"></a>Virhe 1300

Virhesanoma on Yksikön \{Talous- ja toimintosovellusten EntityMetadata.EntityProperties.LogicalEntityName\} virtuaalikenttiä \{s.EntityFieldName\} ei voi jäljittää kaksoiskirjoituksen osalta.

Talous- ja toimintosovellusten taulujen virtuaalikenttiä ei voi jäljittää. Reaaliaikainen synkronointi voi synkronoida tiedot, mutta se ei voi noutaa sarakkeisiin tehtyjä muutoksia.

## <a name="error-1500"></a>Virhe 1500

Virhesanoma on Vähintään yhden kentän on oltava määritettynä muuhun kuin hakukenttään Customer Engegementissa, jotta tietolähdettä \{datasource.DataSourceName\} voi jäljittää.

Yksikön tietolähteellä ei ole kaksoiskirjoitusta varten määritettyä kenttää. Pohjana olevaan tauluun tehtyjä muutoksia ei jäljitetä kaksoiskirjoituksen osalta.

## <a name="error-1600"></a>Virhe 1600

Virhesanoma on Yksikön \{Talous- ja toimintosovellusten EntityMetadata.EntityProperties.LogicalEntityName\} tietolähteellä \{datasource.DataSourceName\} on alue. Vain alue-ehtoa vastaavat tietueet noudetaan lähteviä varten.

Talous- ja toimintosovellusten yksiköillä voi olla tietolähteitä, joissa on käytössä suodatinalueita. Nämä alueet määrittävät tietueet, jotka noudetaan reaaliaikaiseen synkronointiin. Jos joitakin tietueita ohitetaan talous- ja toimintosovelluksesta Dataverseen, tarkista, täyttävätkö tietueet yksikön alueperusteet. Yksinkertainen tapa tehdä tämä tarkistus on suorittaa SQL-kysely, joka muistuttaa seuraavaa esimerkkiä.

```sql
select * from <EntityName> where <filter criteria for the records> on SQL.
```

## <a name="error-1700"></a>Virhe 1700

Virhesanoma on Yksikön \{datasourceTable.Key.entityName\} taulua \{datasourceTable.Key.subscribedTableName\} jäljitetään yksikön \{origTableToEntityMaps.EntityName\} osalta. Useiden taulujen seuraaminen useiden yksikköjen osalta voi vaikutta järjestelmän suorituskykyyn reaaliaikaisissa synkronointitapahtumissa.

Jos useammat yksiköt seuraavat samaa taulua, muutokset tauluun käynnistävät kaksoiskirjoituksen arvioinnin linkitettyjen yksikköjen osalta. Vaikka suodatinlausekkeet lähettävät vain kelvolliset tietueet, arviointi saattaa aiheuttaa suorituskykyongelman, jos on olemassa pitkäkestoisia kyselyjä tai optimoimattomia kyselysuunnitelmia. Tätä ongelmaa ei ehkä voi välttää liiketoiminnan näkökulmasta. Jos kuitenkin useilla yksiköillä on useita risteäviä tauluja, kannattaa harkita yksikön yksinkertaistamista tai yksikkökyselyjen optimointien tarkistamista.

## <a name="error-1800"></a>Virhe 1800
Virhesanoma on seuraava: "Datasource : {} yksikölle CustCustomerV3Entity sisältää aluearvon. Yksikön aluearvot voivat vaikuttaa saapuvan tietueen lisäyksiin Dataversesta talous- ja toimintosovelluksiin. Testaa tietueen päivitykset Dataversesta talous- ja toimintosovelluksiin tietueilla, jotka eivät vastaa suodatusehtoja, jotta voit vahvistaa asetukset."

Jos talous- ja toimintosovellusten yksikölle on määritetty arvoalue, saapuva synkronointi Dataversesta talous- ja toimintosovelluksiin tulee testata sellaisten tietueiden toiminnan päivittämiseksi, jotka eivät vastaa arvoalueen ehtoja. Entiteetti käsittelee lisäystoimintona kaikkia tietueita, jotka eivät vastaa arvoaluetta. Jos pohjana olevassa taulussa on olemassa oleva tietue, lisäys epäonnistuu. Tämä käyttötapaus kannattaa testata kaikissa skenaarioissa ennen ottamista tuotantoon.

## <a name="error-1900"></a>Virhe 1900
Virhesanoma on seuraava: "Yksiköllä on {} tietolähdettä, joita lähtevä kaksoiskirjoitus ei seuraa. Tämä voi vaikuttaa live-synkronoinnin kyselyn suorituskykyyn. Muodosta malli uudelleen talous- ja toimintosovelluksissa, jos haluat poistaa käyttämättömät tietolähteet ja taulut tai ottaa käyttöön taulun getEntityRecordIdsImpactedByTableChange suorituksenaikaisten kyselyjen optimoimiseksi."

Jos löytyy useita tietolähteitä, joita ei käytetä toteutuneen live-synkronoinnin seuraamiseen talous- ja toimintosovelluksista, yksikön suorituskyky voi vaikuttaa live-synkronointiin. Voit optimoida seuratut taulut käyttämällä getEntityRecordIdsImpactedByTableChange-menetelmää.

## <a name="error-5000"></a>Virhe 5000
Virhesanoma on seuraava: "Synkronoinnin laajennukset on rekisteröity yksikön tilien tiedonhallinnan tapahtumia varten. Ne voivat vaikuttaa alkuperäisen synkronoinnin ja live-synkronoinnin tuonnin suorituskykyyn Dataversessa. Muuta laajennukset asynkronista käsittelyä varten parhaan suorituskyvyn saamiseksi. Rekisteröityjen laajennusten luettelo {}."

Dataverse-yksikön synkroniset laajennukset voivat vaikuttaa live-synkronointiin ja alkuperäiseen synkronoinnin suorituskykyyn, koska se lisää tapahtumakuormitusta. Suositeltu tapa on poistaa laajennukset käytöstä tai tehdä näistä laajennuksista asynkronisia, jos alkuperäisen synkronoinnin tai live-synkronoinnin latausajat ovat pitkiä.

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]

