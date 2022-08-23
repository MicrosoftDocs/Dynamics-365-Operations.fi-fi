---
title: Kaksoiskirjoitusmääritysten tarkistus talous- ja toimintosovelluksissa sekä Dataversessä
description: Tässä artikkelissa käsitellään sen selvittämistä, onko kaksoiskirjoitus määritetty talous- ja toimintosovelluksissa sekä Dataversessa.
author: RamaKrishnamoorthy
ms.date: 03/16/2020
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: 4ff7821fce661f174f57fb45667d4ceb3cfcede9
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/12/2022
ms.locfileid: "9289387"
---
# <a name="verify-dual-write-configuration-in-finance-and-operations-apps-and-dataverse"></a>Kaksoiskirjoitusmääritysten tarkistus talous- ja toimintosovelluksissa sekä Dataversessä

[!include [banner](../../includes/banner.md)]





Tässä artikkelissa on vianmääritystietoja kaksoiskirjoituksen integroinnista talous- ja toimintosovellusten sekä Dataversen välillä. Erityisesti siinä käsitellään sen määrittämistä, onko kaksoiskirjoitus määritetty talous- ja toimintosovelluksissa sekä Dataversessa.

## <a name="verify-that-dual-write-is-configured-in-a-finance-and-operations-app"></a>Kaksoiskirjoituksen määrittämisen tarkistaminen talous- ja toimintosovelluksessa

Jos haluat määrittää, näytetäänkö kaksoiskirjoitusvirheet, kun yrität tallentaa rivejä päivitystä varten, varmista ensin, että kaksoiskirjoitus on määritetty.

+ Jos sinulla on talous- ja toimintosovelluksen järjestelmänvalvojan oikeudet, valitse ensin **Työtilat \> Tietojen hallinta** ja sitten **Kaksoiskirjoitus**-ruutu. Jos linkitettyjen ympäristöjen tiedot ja käytössä olevien taulukarttojen luettelo näytetään, kaksoiskirjoitus on määritetty.

    ![Talous- ja toimintosovelluksen yhteyden tarkistaminen, kun sinulla on järjestelmänvalvojan oikeudet.](media/verify_fin_ops_1.png)

+ Jos sinulla ei ole järjestelmänvalvojan oikeuksia, näyttöön avautuu virhesanoma *Tietoja ei voi kirjoittaa yksikköön \<entity name\>*. Seuraavassa esimerkissä asiakasriviä ei voi luoda talous- ja toimintosovelluksessa, koska kaksoiskirjoitus on määritetty mutta asiakasryhmä- ja maksujen viitetietoja ei ole Dataversessä.

    ![Talous- ja toimintosovelluksen yhteyden tarkistaminen, kun sinulla ei ole järjestelmänvalvojan oikeuksia.](media/verify_fin_ops_2.png)

Lisätietoja ongelmien korjaamisesta, kun tietoja luodaan talous- ja toimintosovelluksissa, on kohdassa [Suorasynkronointiongelmien vianmääritys](dual-write-troubleshooting-live-sync.md).

## <a name="verify-that-dual-write-is-configured-in-dataverse"></a>Varmista, että kaksoiskirjoitus on määritetty Dataverse -sovelluksissa

Kaksoiskirjoitus on määritetty, jos tietoja luotaessa Dataversen sivuilla näkyy **Yritys**-sarake.

![Dataverse-yhteyden tarkistaminen.](media/verify_cds.png)

Lisätietoja ongelmien korjaamisesta, kun tietoja luodaan Dataversessa, on kohdassa [Suorasynkronointiongelmien vianmääritys](dual-write-troubleshooting-live-sync.md).

Lisätietoja virhetietojen katsomisesta, jos virheitä syntyy luodessasi tietoja Dataversessä on kohdassa [Ota käyttöön ja tarkastele laajennuksen jäljityslokia Dataversessä nähdäksesi virhetiedot](dual-write-troubleshooting.md#enable-view-trace).


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
