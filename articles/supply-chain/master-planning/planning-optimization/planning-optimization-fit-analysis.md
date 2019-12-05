---
title: Suunnittelun optimoinnin sopivuusanalyysi
description: Tässä ohjeaiheessa käsitellään, miten nykyisten asetusten ja tietojen yhteensopivuus suunnittelun optimointitoiminnon ominaisuuksien kanssa varmistetaan.
author: ChristianRytt
manager: AnnBe
ms.date: 1030/2019
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
ms.openlocfilehash: 26b067f8526df16474c0ab52d0abf816170ff5cb
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/06/2019
ms.locfileid: "2773950"
---
[!include [banner](../../includes/preview-banner.md)]
[!include [banner](../../includes/banner.md)]

# <a name="planning-optimization-fit-analysis"></a>Suunnittelun optimoinnin sopivuusanalyysi

Voit tarkistaa, kuinka yhteensopivia nykyiset asetukset ja tiedot ovat suunnittelu optimointitoiminnon kanssa valitsemalla ensin **Pääsuunnittelu** \> **Asetukset** \> **Suunnittelun optimoinnin sopivuusanalyysi** ja valitse sitten **Suorita analyysi**. Jos analyysissa havaitaan ristiriitoja, ne mainitaan samalla sivulla. (Analyysin suorittaminen voi kestää muutaman minuutin.)

> [!NOTE]
> Jos ristiriitoja löytyy, suunnittelun optimointia voi silti käyttää. Sopivuusanalyysin tulokset vain osoittavat, missä suunnittelupalvelu ei noudata nykyisiä asetuksia. Ne siis näyttävät kohdat, joissa joitakin prosesseja voidaan ohittaa tai joissa niitä ei ehkä tueta.

## <a name="analysis-results-example-1"></a>Analyysin tulokset: Esimerkki 1

- **Toiminto:** Tuotanto
- **Ongelma:** Nimikkeet, joiden tuoterakenteen taso on suurempi kuin nolla: 56
- **Selitys:** Sopivuusanalyysi löysi 56 nimikettä, joissa on tuotannon tuoterakenteen asetuksia. Koska suunnittelun optimoinnin nykyinen versio ei tue tuotantoa, suunnittelun optimointi luo suunniteltuja ostotilauksia eikä suunniteltuja tuotantotilauksia. Näkyviin tulee myös varoitus, jossa mainitaan nimikkeet, joita ongelma koskee.

### <a name="analysis-results-example-2"></a>Analyysin tulokset: Esimerkki 2

- **Toiminto:** Toimenpiteet
- **Ongelma:** Kattavuusryhmät, joissa toimenpidelaskelma on otettu käyttöön: 6
- **Selitys:** Sopivuusanalyysi havaitsi kuusi kattavuusryhmää, joissa toimenpidelaskelma on otettu käyttöön. Koska suunnittelun optimoinnin nykyinen versio ei tue toimenpiteitä, toimenpiteitä ei luoda pääsuunnittelun aikana.

## <a name="related-resources"></a>Liittyvät resurssit

[Suunnittelun optimoinnin yleiskuvaus](planning-optimization-overview.md)

[Suunnittelun optimoinnin aloittaminen](get-started.md)

[Suunnitelman historia- ja suunnittelulokien tarkasteleminen](plan-history-logs.md)

[Suodattimien käyttäminen suunnitelmaan](plan-filters.md)

[Suunnittelutyön peruuttaminen](cancel-planning-job.md)
