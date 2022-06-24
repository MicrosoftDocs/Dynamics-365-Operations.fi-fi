---
title: Kaksoiskirjoitusmääritysten tarkistus Finance and Operations -sovelluksissa sekä Dataversessä
description: Tässä artikkelissa kerrotaan, miten voit määrittää, onko talous- ja toimintosovelluksissa ja Dataversessa määritetty kaksoiskirjoitus.
author: RamaKrishnamoorthy
ms.date: 03/16/2020
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: tfehr
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: 7131e6c2c4ca4d9c6bb84ad74bf425faf28bd92c
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8884456"
---
# <a name="verify-dual-write-configuration-in-finance-and-operations-apps-and-dataverse"></a>Kaksoiskirjoitusmääritysten tarkistus Finance and Operations -sovelluksissa sekä Dataversessä

[!include [banner](../../includes/banner.md)]





Tässä artikkelissa on vianetsintätietoja kaksoiskirjoituksen integroinnista talous- ja toimintosovellusten ja Dataversen välillä. Erityisesti se selittää miten voit määrittää, onko taloushallinnon ja toimintojen sovelluksissa ja Dataversessa määritetty kaksoiskirjoitus.

## <a name="verify-that-dual-write-is-configured-in-a-finance-and-operations-app"></a>Kaksoiskirjoitusmääritysten tarkistus taloushallinnon ja toimintojen sovelluksessa

Jos haluat määrittää, näytetäänkö kaksoiskirjoitusvirheet, kun yrität tallentaa rivejä päivitystä varten, varmista ensin, että kaksoiskirjoitus on määritetty.

+ Jos sinulla on taloushallinnon ja toimintojen sovelluksen järjestelmänvalvojan oikeudet, siirry kohtaan **Työtilat \> Tietojen hallinta** ja valitse **Kaksoiskirjoitus**-ruutu. Jos linkitettyjen ympäristöjen tiedot ja käytössä olevien taulukarttojen luettelo näytetään, kaksoiskirjoitus on määritetty.

    ![Taloushallinnon ja toimintojen sovellusyhteyden tarkistaminen, kun sinulla on järjestelmänvalvojan oikeudet.](media/verify_fin_ops_1.png)

+ Jos sinulla ei ole järjestelmänvalvojan oikeuksia, näyttöön avautuu virhesanoma *Tietoja ei voi kirjoittaa yksikköön \<entity name\>*. Seuraavassa esimerkissä asiakasriviä ei voi luoda taloushallinnon ja toimintojen sovelluksessa, koska kaksoiskirjoitus on määritetty, mutta asiakasryhmä- ja maksujen viitetietoja ei ole Dataversessä.

    ![Taloushallinnon ja toimintojen sovellusyhteyden tarkistaminen, kun sinulla ei ole järjestelmänvalvojan oikeuksia.](media/verify_fin_ops_2.png)

Lisätietoja ongelmien korjaamisesta, kun tietoja luodaan taloushallinnon ja toimintojen sovelluksissa, on kohdassa [Suorasynkronointiongelmien vianmääritys](dual-write-troubleshooting-live-sync.md).

## <a name="verify-that-dual-write-is-configured-in-dataverse"></a>Varmista, että kaksoiskirjoitus on määritetty Dataverse -sovelluksissa

Kaksoiskirjoitus on määritetty, jos tietoja luotaessa Dataversen sivuilla näkyy **Yritys**-sarake.

![Dataverse-yhteyden tarkistaminen.](media/verify_cds.png)

Lisätietoja ongelmien korjaamisesta, kun tietoja luodaan Dataversessa, on kohdassa [Suorasynkronointiongelmien vianmääritys](dual-write-troubleshooting-live-sync.md).

Lisätietoja virhetietojen katsomisesta, jos virheitä syntyy luodessasi tietoja Dataversessä on kohdassa [Ota käyttöön ja tarkastele laajennuksen jäljityslokia Dataversessä nähdäksesi virhetiedot](dual-write-troubleshooting.md#enable-view-trace).


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]