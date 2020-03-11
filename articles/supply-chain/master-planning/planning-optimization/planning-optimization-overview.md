---
title: Suunnittelun optimoinnin yleiskuvaus
description: Tässä ohjeaiheessa on suunnittelun optimoinnin toimintojen yleiskatsaus.
author: ChristianRytt
manager: AnnBe
ms.date: 10/31/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: 9ccf00b6fcd1e3a6002086360b1a4c5c464ba054
ms.sourcegitcommit: a688c864fc609e35072ad8fd2c01d71f6a5ee7b9
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/20/2020
ms.locfileid: "3076152"
---
# <a name="planning-optimization-overview"></a>Suunnittelun optimoinnin yleiskuvaus

[!include [banner](../../includes/banner.md)]
[!include [banner](../../includes/preview-banner.md)]

Microsoft Dynamics 365 Supply Chain Managementin suunnittelun optimoinnin lisäosan avulla pääsuunnittelulaskelma voidaan tehdä Dynamics 365 Supply Chain Managementin ja liittyvän SQL-tietokannan ulkopuolella. Suunnittelun optimointitoimintoon liittyviä etuja ovat esimerkiksi suorituskyvyn parantuminen ja pääsuunnitteluajon vähäinen vaikutus SQL-tietokantaan. Nopeita suunnitteluajoja voidaan tehdä myös työaikana, joten suunnittelijat voivat reagoida heti kysynnän tai parametrin muutoksiin.

Suunnittelun optimoinnin käyttöä varten on asennettava suunnittelun optimoinnin lisäosa Microsoft Dynamics Lifecycle Servicesin (LCS) projektista ja otettava suunnittelun optimointitoiminto käyttöön Supply Chain Managementissa. Lisätietoja on kohdassa [Suunnittelun optimoinnin käytön aloittaminen](get-started.md).

Seuraava kuva osoittaa suunnittelun optimoinnin työaikana tapahtuvan käytön edut.

![Suunnittelun optimoinnin työaikana tapahtuvan käytön edut](media/PlanningOptimization1.png)

## <a name="improved-performance"></a>Parantunut suorituskyky

Suunnittelun optimointia voidaan käyttää pitkäkestoisia pääsuunnitelmia sisältävissä skenaarioissa. Se on suunniteltu erityisesti erittäin nopeisiin laskelmiin, joissa käytetään erittäin suuria tietomääriä. Koska on muodostettu äärimmäisen skaalautuvana monen vuokraajan palveluna, suunnitelman laskemiseen voidaan käyttää samanaikaisesti useita yhdessä työskenteleviä esiintymiä. Suunnittelupalvelu poistaa lisäksi pääsuunnittelun kuormituksen järjestelmästä ja käyttää palvelinkuormituksen minimoivaa tietovirtaa.

Suunnittelun optimointi auttaa saavuttamaan seuraavat tavoitteet:

- Lyhentynyt ajoaika parantaa suunnittelun suorituskykyä.
- Pienentynyt vaikutus muihin prosesseihin pääsuunnitteluajon aikana.
- Suunnitteluajojen välit lyhenevät. (Ajot eivät rajoitus yhteen kertaan päivässä.)
- Tieto siitä, että yrityksen kasvu tulevaisuudessa ei ylikuormita suunnittelujärjestelmää.

## <a name="architecture-and-data-flow"></a>Arkkitehtuuri ja tiedonkulku

Kun suunnittelun optimoinnin lisäosa asennetaan LCS:stä, suunnittelun optimointipalveluun muodostetaan suojattu yhteys. Palvelu sijaitsee samassa maassa tai samalla alueella olevassa palvelinkeskuksessa kuin liittyvä Supply Chain Management -esiintymä. Suunnittelun optimoinnin määrittämisen jälkeen päätiedot ja tapahtumatiedot lähetetään pääsuunnittelun suorittamisen aikana Supply Chain Managementista suunnittelun optimointipalveluun.

Jos suunnittelun optimoinnin lisäosan asennus poistetaan, kaikki suunnittelun optimointipalveluun liittyvät tiedot poistetaan.

### <a name="high-level-data-flow-for-regeneration-runs"></a>Uudelleenluontiajojen korkean tason tiedonkulku

1. Supply Chain Management -asiakasohjelma lähettää signaalin, jolla pyydetään suunnitteluajoa suunnittelun optimoinnista.
2. Suunnittelun optimointi pyytää tarvittavia tietoja integroidun yhdistimen kautta.
3. SQL-tietokanta lähettää pyydetyt asetuksia sekä pää- ja tapahtumatietoja koskevat tiedot suunnittelun optimointiin yhdistimen kautta. Yhdistin kääntää tiedot Supply Chain Managementin ja suunnittelun optimointipalvelun välillä.
4. Suunnittelun optimointipalvelu säilyttää suunnitteluun liittyvät tiedot muistissa ja tekee pyydetyt laskutoimitukset.
5. Suunnittelun tulos lähetetään Supply Chain Management -tietokantaa yhdistimen kautta. Tuloksissa on tietoja esimerkiksi suunnitteluista tilauksista ja tarvekohdistuksesta. Suunnittelun optimoinnin Supply Chain Managementiin lähettämä signaali ilmaisee, että suunnitteluajo on valmis. Se lähettää myös mahdolliset liittyvät sanomat ja varoitukset.

Seuraavassa kuvassa näkyy tiedonkulku.

![Uudelleenluontiajojen tiedonkulku](media/PlanningOptimization2.png)

## <a name="related-resources"></a>Liittyvät resurssit

[Suunnittelun optimoinnin aloittaminen](get-started.md)

[Suunnittelun optimoinnin sopivuusanalyysi](planning-optimization-fit-analysis.md)

[Suunnitelman historia- ja suunnittelulokien tarkasteleminen](plan-history-logs.md)

[Suodattimien käyttäminen suunnitelmaan](plan-filters.md)

[Suunnittelutyön peruuttaminen](cancel-planning-job.md)
