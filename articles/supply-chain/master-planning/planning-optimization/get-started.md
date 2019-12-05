---
title: Suunnittelun optimoinnin aloittaminen
description: Tässä ohjeaiheessa käsitellään suunnittelun optimointitoiminnon käytön aloittamisesta.
author: ChristianRytt
manager: AnnBe
ms.date: 10/29/2019
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
ms.openlocfilehash: 37c2acb2397b2a0ad69272c0645bd200a8d7910d
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/06/2019
ms.locfileid: "2773947"
---
[!include [banner](../../includes/preview-banner.md)]
[!include [banner](../../includes/banner.md)]

# <a name="get-started-with-planning-optimization"></a>Suunnittelun optimoinnin aloittaminen

Suunnittelun optimointitoiminto ei tällä hetkellä tue kaikki niitä toimintoja, joita on Microsoft Dynamics 365 Supply Chain Managementin sisäisessä suunnittelumoduulissa. Tämän vuoksi on tärkeää arvioida, vastaako suunnittelun optimoinnissa tällä hetkellä käytössä oleva toimintojoukko tarpeitasi. Suunnittelun optimointitoimintoa ei ole oletusarvoisesti otettu käyttöön Dynamics Lifecycle Servicesissa (LCS). Niinpä arvioinnin voi tehdä, ennen kuin toiminto otetaan käyttöön.

Suunnittelun optimointi tulee jossain vaiheessa korvaamaan nykyisen Supply Chain Managementin sisäisen suunnittelumoduulin.

Ennen suunnittelun optimoinnin ottamista käyttöön on syytä arvioida suunnittelun optimoinnin sopivuusanalyysin tulokset. Lisätietoja on kohdassa [Suunnittelun optimoinnin sopivuusanalyysi](planning-optimization-fit-analysis.md).

### <a name="licensing"></a>Käyttöoikeudet

Jos voit suorittaa pääsuunnittelua nykyisellä käyttöoikeudella, suunnittelun optimoinnin käytön aloittamista varten ei tarvitse ostaa käyttöoikeutta.

### <a name="install-the-add-in"></a>Lisäosan asentaminen

Suunnittelun optimoinnin käyttöä varten on asennettava Dynamics 365 Supply Chain Managementin suunnittelun optimoinnin lisäosa. Voit käyttää lisäosaa LCS-projektista ja ottaa suunnittelun optimointitoiminnon käyttöön Supply Chain Management -käyttöliittymässä.

1. Kirjaudu sisään LCS:ään ja avaa sopiva ympäristö.
1. Valitse **Kaikki tiedot**.
1. Valitse **Ylläpito** tai selaa alas **Ympäristön lisäosat** -pikavälilehteen.
1. Valitse **Asenna uusi lisäosa**.
1. Valitse **Suunnittelun optimointi**.
1. Noudata asennusoppaan ohjeita ja hyväksy käyttöehdot.
1. Valitse **Asenna**.

### <a name="planning-optimization-integration"></a>Suunnittelun optimoinnin integrointi

Voit määrittää, käytetäänkö suunnittelun optimoinnin lisää pääsuunnittelussa valitsemalla **Pääsuunnittelu** \> **Asetukset** \> **Suunnittelun optimoinnin integrointi** \> **Integrointiparametrit**.

#### <a name="connection-status"></a>Yhteyden tila

Yhteyden tila ilmaisee Supply Chain Managementin ja suunnittelun optimointipalvelun välisen yhteyden nykyisen tilan. Mahdolliset arvot ovat seuraavassa taulukossa.

| Yhteyden tila | Kuvaus | Voiko suunnittelun optimointia käyttää? |
|---|---|---|
| Yhdistetty | Suunnittelun optimointipalvelun ja Supply Chain Managementin välille on muodostettu yhteys. | Kyllä |
| Otetaan yhteyttä käyttöön | Pyyntöä ottaa yhteys suunnittelun optimointipalveluun käsitellään. | Ei |
| Yhteys katkaistu | Suunnittelun optimointipalveluun ei ole yhteyttä. Yhteys voidaan ottaa käyttöön LCS:ssä aiemmin tässä ohjeaiheessa kuvatulla tavalla. | Ei |
| Poistettaan yhteyttä käytöstä | Pyyntöä katkaista yhteys suunnittelun optimointipalveluun käsitellään. | Ei |
| Tilan saaminen | Järjestelmä odottaa tilatietoja suunnittelun optimointipalvelusta. | Ei |

#### <a name="the-use-planning-optimization-option"></a>Käytä suunnittelun optimointia -vaihtoehto

**Käytä suunnittelun optimointia** -vaihtoehdossa valittu asetus määrittää, mitä suunnittelumoduulia pääsuunnittelussa käytetään:

- **Kyllä** – suunnittelun optimointia käytetään pääsuunnittelussa.
- **Ei** – Supply Chain Managementin sisäistä suunnittelumoduulia käytetään pääsuunnittelussa.

> [!NOTE]
> Jos Supply Chain Managementin sisäiselle suunnittelumoduulille aiemmin luodut suunnittelun erätyöt käynnistyvät, kun **Käytä suunnittelun optimointia** -asetuksena on **Kyllä**, kyseiset työt epäonnistuvat.

### <a name="integration-with-the-setup"></a>Integrointi määrityksiin

Jos suunnittelun optimoinnin esiversio on otettu käyttöön, suunnittelun optimoinnin lisäosaa käytetään pääsuunnittelussa. Tällä on vaikutusta pääsuunnittelun tuloksiin ja toimintoihin.

## <a name="related-resources"></a>Liittyvät resurssit

[Esiversion ehdot](https://go.microsoft.com/fwlink/?linkid=2015274)

[Suunnittelun optimoinnin yleiskuvaus](planning-optimization-overview.md)

[Suunnittelun optimoinnin sopivuusanalyysi](planning-optimization-fit-analysis.md)

[Suunnitelman historia- ja suunnittelulokien tarkasteleminen](plan-history-logs.md)

[Suodattimien käyttäminen suunnitelmaan](plan-filters.md)

[Suunnittelutyön peruuttaminen](cancel-planning-job.md)
