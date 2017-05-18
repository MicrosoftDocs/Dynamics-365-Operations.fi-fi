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
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: 5ee2d132f0b23ceec2a79ee6b0ee33862d6a0518
ms.contentlocale: fi-fi
ms.lasthandoff: 04/25/2017


---

# <a name="financial-dimensions"></a>Taloushallinnon dimensiot

[!include[banner](../includes/banner.md)]


Tässä artikkelissa kerrotaan erityyppisistä taloushallinnon dimensioista ja niiden määrittämisestä.

Luo Taloushallinnon dimensiot -sivun avulla tilikartan tilisegmentteinä käytettäviä taloushallinnon dimensioita. Taloushallinnon dimensioita on kahdenlaisia: mukautettuja ja yksikön tukemia dimensioita. Mukautetut dimensiot jaetaan yritysten välillä ja arvot syöttää ja ylläpitää käyttäjä. Yksikön tukemien dimensioiden arvot määritellään toisaalla järjestelmässä, esimerkiksi Asiakkaat- tai Myymälät-osassa. Jotkin yksikön tukemat dimensiot jaetaan yritysten välillä, ja jotkin yksikön tukemat dimensiot ovat yrityskohtaisia. 

Kun taloushallinnon dimensiot on luotu, voit liittää jokaiselle taloushallinnon dimensiolle lisää ominaisuuksia Taloushallinnon dimension arvot -sivun avulla. 

Voit käyttää taloushallinnon dimensioita edustamaan yrityksiä ilman, että luot yrityksiä Microsoft Dynamics 365 for Operationsissa. Taloushallinnon dimensioita ei ole kuitenkaan suunniteltu vastaamaan yritysten toiminnallisiin tai liiketaloudellisiin tarpeisiin. Microsoft Dynamics 365 for Operationsin yksiköiden välisen kirjanpidon toiminnallisuus on suunniteltu käsittelemään vain jokaisen tapahtuman luomat kirjanpitomerkinnät. 

Ennen kuin määrität taloushallinnon dimensiot yrityksiksi, arvioi liiketoimintaprosessisi seuraavilla alueilla selvittääksesi, jos tätä asetusta voi käyttää organisaatiossasi:

-   Varasto
-   Myynnit ja ostot taloushallinnon dimensioiden ja yritysten välillä
-   Arvonlisäveron laskenta ja ilmoittaminen
-   Toiminnan raportointi

Seuraavassa on esimerkkejä rajoituksista:

-   Voit käyttää arvonlisäverotoimintoa ainoastaan yritysten kanssa, et taloushallinnon dimensioiden.
-   Taloushallinnon dimensiot eivät sisälly tiettyihin raportteihin, eli niiden raportointi ei aina ole mahdollista, ellei raportteja muokata.

**Mukautetut dimensiot** 

Käyttäjän määrittämän taloushallinnon dimension voit luoda napsauttamalla Käytä arvoja kohteesta -kentässä &lt; Mukautettu dimensio &gt;. Voit määrittää myös tilipeitteen rajoittamaan dimensioarvoille annettavaa summaa ja tietojen tyyppiä. Voit syöttää merkkejä, jotka pysyvät samana jokaisessa dimensioarvossa, kuten kirjaimia tai yhdysviivan. Voit myös antaa numeromerkkejä (\#) ja et-merkkejä (&) kirjaimien ja numerojen paikkamerkkeinä, jotka muuttuvat aina, kun dimensioarvo luodaan. Käytä numeromerkkiä (\#) numeron paikkamerkkinä ja et-merkkiä (&) kirjaimen paikkamerkkinä. 

**Esimerkki** 

Jos haluat rajoittaa dimensioarvon kirjaimiin CC ja kolmeen numeroon, syötä muotoilupeitteeksi CC-\#\#\#. Tämä kenttä on käytettävissä vain, kun valitset &lt; Mukautettu dimensio &gt; Käytä arvoja -kentässä. 

**Yksikön tukemat dimensiot** 

Yksikön tukeman taloushallinnon dimension voit luoda valitsemalla Käytä arvoja kohteesta -kenttään järjestelmän määrittämä yksikkö, johon taloushallinnon dimensio tukeutuu. Taloushallinnon dimensioarvot luodaan tästä valinnasta. Voit luoda esimerkiksi projektien dimensioarvot valitsemalla Projektit. Jokaiselle projektin nimelle luodaan dimensioarvo. Dimensioarvot-sivulla näytetään yksikön arvot ja, jos ne ovat yrityskohtaisia, arvon yritys. 

**Dimensioiden aktivointi** 

Taloushallinnon dimension aktivointi päivittää taulun taloushallinnon dimension nimellä ja poistaa poistetut dimensiot. Voit antaa dimensioarvot ennen aktivoit taloushallinnon dimension aktivointia, mutta taloushallinnon dimensiota ei voi kuluttaa missään, ennen kuin se on aktivoitu. Et esimerkiksi voi lisätä taloushallinnon dimensiota tilirakenteeseen ennen dimension aktivointia. Aktivointipainiketta napsauttamalla päivität tilamuutokset kaikille dimensioille. 

**Käännökset** 

Tekstin käännös -sivulle voi syöttää valitussa taloushallinnon dimensiossa näytettävät kielet. Päätilin käännös -sivulla voi syöttää päätilissä näytettävät kielet. 

**Yrityksen ohitukset** 

Kaikki dimensiot eivät kelpaa kaikille yrityksille, ja jotkin dimensiot saattavat olla olennaisia vain tietyn ajanjakson ajan. Tässä skenaariossa Yrityksen ohitukset -osan avulla määritetään yritykset, joilta dimension käyttö keskeytetään, omistaja sekä ajanjakso, jolloin dimensio on aktiivinen.






