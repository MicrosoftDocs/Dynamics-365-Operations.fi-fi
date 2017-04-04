---
title: Taloushallinnon dimensiot
description: "Tässä artikkelissa kerrotaan erityyppisistä taloushallinnon dimensioista ja niiden määrittämisestä."
author: RobinARH
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: DimensionDetails, DimensionValueDetails, SysTranslationDetail
audience: Application User
ms.reviewer: RobinARH
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 25871
ms.assetid: af54621c-c8be-4b72-b6df-dcf886c40ce4
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9f4d7fdd8cfa7a540fce219f6ae4792e57dfbe44
ms.openlocfilehash: f849b98cac88d182875aca88aaf04cd3575ed99f
ms.lasthandoff: 03/31/2017


---

# <a name="financial-dimensions"></a>Taloushallinnon dimensiot

Tässä artikkelissa kerrotaan erityyppisistä taloushallinnon dimensioista ja niiden määrittämisestä.

Luo Taloushallinnon dimensiot -sivun avulla tilikartan tilisegmentteinä käytettäviä taloushallinnon dimensioita. Taloushallinnon dimensioita on kahdenlaisia: mukautettuja ja yksikön tukemia dimensioita. Mukautetut dimensiot jaetaan yritysten välillä ja arvot syöttää ja ylläpitää käyttäjä. Yksikön tukemien dimensioiden arvot määritellään toisaalla järjestelmässä, esimerkiksi Asiakkaat- tai Myymälät-osassa. Jotkin yksikön tukemat dimensiot jaetaan yritysten välillä, ja jotkin yksikön tukemat dimensiot ovat yrityskohtaisia. 

Kun taloushallinnon dimensiot on luotu, voit liittää jokaiselle taloushallinnon dimensiolle lisää ominaisuuksia Taloushallinnon dimension arvot -sivun avulla. 

Vaikka voitkin taloushallinnon dimensiot edustavat juridisia yrityksiä luomatta oikeushenkilöt Microsoft Dynamics-365 operaatioille, taloushallinnon dimensiot eivät ole suunniteltu korjaamaan toiminnassa tai yrityksen tarpeiden oikeussubjektien. Yksikköjen kirjanpidon toimintoja Microsoft Dynamics-365 toimintoja varten on suunniteltu vain kirjanpidon tapahtumat luodaan kunkin tapahtuman osoite. 

Ennen kuin määrität taloushallinnon dimensiot yrityksiksi, arvioi liiketoimintaprosessisi seuraavilla alueilla selvittääksesi, jos tätä asetusta voi käyttää organisaatiossasi:

-   Varasto
-   Myynnit ja ostot taloushallinnon dimensioiden ja yritysten välillä
-   Arvonlisäveron laskenta ja ilmoittaminen
-   Toiminnan raportointi

Seuraavassa on esimerkkejä rajoituksista:

-   Voit käyttää arvonlisäverotoimintoa ainoastaan yritysten kanssa, et taloushallinnon dimensioiden.
-   Taloushallinnon dimensiot eivät sisälly tiettyihin raportteihin, eli niiden raportointi ei aina ole mahdollista, ellei raportteja muokata.

**Custom dimensions** 

Voit luoda käyttäjän määrittämiä taloushallinnon dimensio, Käytä arvoja kohteesta-kentästä, valitse &lt;mukautettu dimension&gt;. Voit määrittää myös tilipeitteen rajoittamaan dimensioarvoille annettavaa summaa ja tietojen tyyppiä. Voit syöttää merkkejä, jotka pysyvät samana jokaisessa dimensioarvossa, kuten kirjaimia tai yhdysviivan. Voit myös kirjoittaa ristikkomerkkejä (\#) ja et-merkkiä (&) paikkamerkkeinä kirjaimia ja numeroita, jotka muuttuvat aina, kun luodaan dimensioarvo. Käyttää ristikkomerkkiä (\#) paikkamerkki numero ja et-merkki (&) kirje paikkamerkki. 

**Esimerkki** 

Voit rajoittaa dimensioarvon kirjeet kopio ja kolme numeroa, kirjoita kopio -\#\#\# kuin peitteen muoto. Tämä kenttä on käytettävissä vain, kun &lt;mukautettu dimension &gt; -Käytä arvoja kohteesta-kentästä. 

**Varmuuskopioinnin kohde dimensiot** 

Luoda varmuuskopioinnin kohde taloushallinnon dimension Käytä arvoja kohteesta-kentästä, valitse järjestelmän määrittämä kohde taloushallinnon dimension pohjalta. Taloushallinnon dimensioarvot luodaan tästä valinnasta. Voit luoda esimerkiksi projektien dimensioarvot valitsemalla Projektit. Jokaiselle projektin nimelle luodaan dimensioarvo. Dimensioarvot-sivulla näytetään yksikön arvot ja, jos ne ovat yrityskohtaisia, arvon yritys. 

**Dimensioiden aktivoiminen** 

Taloushallinnon dimension aktivointi päivittää taulun taloushallinnon dimension nimellä ja poistaa poistetut dimensiot. Voit antaa dimensioarvot ennen aktivoit taloushallinnon dimension aktivointia, mutta taloushallinnon dimensiota ei voi kuluttaa missään, ennen kuin se on aktivoitu. Et esimerkiksi voi lisätä taloushallinnon dimensiota tilirakenteeseen ennen dimension aktivointia. Aktivointipainiketta napsauttamalla päivität tilamuutokset kaikille dimensioille. 

**Translations** 

Voit kirjoittaa tekstiä eri kielillä valitun taloushallinnon dimension näytetään sivun tekstin käännös. Päätilin käännös -sivulla voi syöttää päätilissä näytettävät kielet. 

**Legal entity overrides** 

Kaikki mitat ovat voimassa kaikille oikeushenkilöille ja jotkin voivat olla vain asiaa tietyn ajanjakson. Tässä skenaariossa Yrityksen ohitukset -osan avulla määritetään yritykset, joilta dimension käyttö keskeytetään, omistaja sekä ajanjakso, jolloin dimensio on aktiivinen.




