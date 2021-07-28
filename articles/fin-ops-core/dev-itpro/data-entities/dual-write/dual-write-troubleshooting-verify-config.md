---
title: Finance and Operations -sovellusten ja Dataversen kaksoiskirjoitusmäärityksen varmistaminen
description: Tässä ohjeaiheessa kerrotaan, miten voit määrittää, onko Finance and Operations -sovelluksissa ja Dataverse -moduulissa määritetty kaksoiskirjoitus.
author: RamaKrishnamoorthy
ms.date: 03/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: d903d58fbd5e9d6bd9ecf7943d09525446721ba2
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 07/06/2021
ms.locfileid: "6350761"
---
# <a name="verify-dual-write-configuration-in-finance-and-operations-apps-and-dataverse"></a>Finance and Operations -sovellusten ja Dataversen kaksoiskirjoitusmäärityksen varmistaminen

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]



Tässä artikkelissa on vianetsintätietoja kaksoiskirjoituksen integroinnista Finance and Operations -sovellusten ja Dataversen välillä. Erityisesti se selittää miten voit määrittää, onko Finance and Operations -sovelluksissa ja Dataverse -moduulissa määritetty kaksoiskirjoitus.

## <a name="verify-that-dual-write-is-configured-in-a-finance-and-operations-app"></a>Varmista, että kaksoiskirjoitus on määritetty Finance and Operations -sovelluksessa

Jos haluat määrittää, näytetäänkö kaksoiskirjoitusvirheet, kun yrität tallentaa rivejä päivitystä varten, varmista ensin, että kaksoiskirjoitus on määritetty.

+ Jos sinulla on Finance and Operations -sovelluksen järjestelmänvalvojan oikeudet, siirry kohtaan **Työtilat \> Tietojen hallinta** ja valitse **Kaksoiskirjoitus**-ruutu. Jos linkitettyjen ympäristöjen tiedot ja käytössä olevien taulukarttojen luettelo näytetään, kaksoiskirjoitus on määritetty.

    ![Finance and Operations -sovellusyhteyden tarkistaminen, kun sinulla on järjestelmänvalvojan oikeudet.](media/verify_fin_ops_1.png)

+ Jos sinulla ei ole järjestelmänvalvojan oikeuksia, näyttöön avautuu virhesanoma *Tietoja ei voi kirjoittaa yksikköön \<entity name\>*. Seuraavassa esimerkissä asiakasriviä ei voi luoda Finance and Operations -sovelluksessa, koska kaksoiskirjoitus on määritetty, mutta asiakasryhmä- ja maksujen viitetietoja ei ole Dataversessä.

    ![Finance and Operations -sovellusyhteyden tarkistaminen, kun sinulla ei ole järjestelmänvalvojan oikeuksia.](media/verify_fin_ops_2.png)

Lisätietoja ongelmien korjaamisesta, kun tietoja luodaan Finance and Operations -sovelluksissa, on kohdassa [Suorasynkronointiongelmien vianmääritys](dual-write-troubleshooting-live-sync.md).

## <a name="verify-that-dual-write-is-configured-in-dataverse"></a>Varmista, että kaksoiskirjoitus on määritetty Dataverse -sovelluksissa

Kaksoiskirjoitus on määritetty, jos tietoja luotaessa Dataversen sivuilla näkyy **Yritys**-sarake.

![Dataverse-yhteyden tarkistaminen.](media/verify_cds.png)

Lisätietoja ongelmien korjaamisesta, kun tietoja luodaan Dataversessa, on kohdassa [Suorasynkronointiongelmien vianmääritys](dual-write-troubleshooting-live-sync.md).

Lisätietoja virhetietojen katsomisesta, jos virheitä syntyy luodessasi tietoja Dataversessä on kohdassa [Ota käyttöön ja tarkastele laajennuksen jäljityslokia Dataversessä nähdäksesi virhetiedot](dual-write-troubleshooting.md#enable-view-trace).


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]