---
title: Varmista, että kaksoiskirjoitus on määritetty Finance and Operations -sovelluksissa ja Common Data Servicessä
description: Tässä ohjeaiheessa kerrotaan, miten voit määrittää, onko Finance and Operations -sovelluksissa ja Common Data Service -moduulissa määritetty kaksoiskirjoitus.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 03/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: 2f2ba2564ad3e8e444e27fcc0c586ddf252afabd
ms.sourcegitcommit: 68f1485de7d64a6c9eba1088af63bd07992d972d
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/27/2020
ms.locfileid: "3172642"
---
# <a name="verify-that-dual-write-is-configured-in-finance-and-operations-apps-and-common-data-service"></a>Varmista, että kaksoiskirjoitus on määritetty Finance and Operations -sovelluksissa ja Common Data Servicessä

[!include [banner](../../includes/banner.md)]



Tässä artikkelissa on vianetsintätietoja kaksoiskirjoituksen integroinnista Finance and Operations -sovellusten ja Common Data Servicen välillä. Erityisesti se selittää miten voit määrittää, onko Finance and Operations -sovelluksissa ja Common Data Service -moduulissa määritetty kaksoiskirjoitus.

## <a name="verify-that-dual-write-is-configured-in-a-finance-and-operations-app"></a>Varmista, että kaksoiskirjoitus on määritetty Finance and Operations -sovelluksessa

Jos haluat määrittää, näytetäänkö kaksoiskirjoitusvirheet, kun yrität tallentaa tietoja päivitystä varten, varmista ensin, että kaksoiskirjoitus on määritetty.

+ Jos sinulla on Finance and Operations -sovelluksen järjestelmänvalvojan oikeudet, siirry kohtaan **Työtilat \> Tietojen hallinta** ja valitse **Kaksoiskirjoitus**-ruutu. Jos linkitettyjen ympäristöjen tiedot ja käytössä olevan yksikkökarttojen luettelo näytetään, kaksoiskirjoitus määritetään.

    ![Finance and Operations -sovellusyhteyden tarkistaminen, kun sinulla on järjestelmänvalvojan oikeudet](media/verify_fin_ops_1.png)

+ Jos sinulla ei ole järjestelmänvalvojan oikeuksia, näyttöön tulee virhesanoma *Tietoja ei voi kirjoittaa yksikköön \<yksikön nimi\>*. Seuraavassa esimerkissä asiakastietuetta ei voi luoda Finance and Operations -sovelluksessa, koska kaksoiskirjoitus on määritetty, mutta asiakasryhmä- ja maksujen viitetietoja ei ole Common Data Service -järjestelmässä.

    ![Finance and Operations -sovellusyhteyden tarkistaminen, kun sinulla ei ole järjestelmänvalvojan oikeuksia](media/verify_fin_ops_2.png)

Lisätietoja ongelmien korjaamisesta, kun tietoja luodaan Finance and Operations -sovelluksissa, on kohdassa [Suorasynkronointiongelmien vianmääritys](dual-write-troubleshooting-live-sync.md).

## <a name="verify-that-dual-write-is-configured-in-common-data-service"></a>Varmista, että kaksoiskirjoitus on määritetty Common Data Service -sovelluksissa

Kun luot tietoja, voit määrittää kaksoiskirjoituksen, jos Common Data Service -lomakkeen sivulla näkyy **Yritys**-kenttä.

![Common Data Service -yhteyden tarkistaminen](media/verify_cds.png)

Lisätietoja ongelmien korjaamisesta, kun tietoja luodaan Common Data Servicessa, on kohdassa [Suorasynkronointiongelmien vianmääritys](dual-write-troubleshooting-live-sync.md).

Lisätietoja virhetietojen katsomisesta, jos virheitä syntyy luodessasi tietoja Common Data Servicessä on kohdassa [Ota käyttöön ja tarkastele laajennuksen jäljityslokia Common Data Servicessä nähdäksesi virhetiedot](dual-write-troubleshooting.md#enable-and-view-the-plug-in-trace-log-in-common-data-service-to-view-error-details).
