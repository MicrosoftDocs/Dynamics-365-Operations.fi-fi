---
title: Kaksoiskirjoitusmääritysten tarkistus taloushallinnon ja toimintojen sovelluksissa ja Dataversessä
description: Tässä ohjeaiheessa kerrotaan, miten voit määrittää, onko taloushallinnon ja toimintojen sovelluksissa ja Dataversessa määritetty kaksoiskirjoitus.
author: RamaKrishnamoorthy
ms.date: 03/16/2020
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: tfehr
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: 3fa16a450032464e445ae166f0699fe0dc388071
ms.sourcegitcommit: 4be1473b0a4ddfc0ba82c07591f391e89538f1c3
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/31/2022
ms.locfileid: "8062797"
---
# <a name="verify-dual-write-configuration-in-finance-and-operations-apps-and-dataverse"></a>Kaksoiskirjoitusmääritysten tarkistus taloushallinnon ja toimintojen sovelluksissa ja Dataversessä

[!include [banner](../../includes/banner.md)]





Tässä ohjeaiheessa on vianetsintätietoja kaksoiskirjoituksen integroinnista taloushallinnon ja toimintojen sovellusten ja Dataversen välillä. Erityisesti se selittää miten voit määrittää, onko taloushallinnon ja toimintojen sovelluksissa ja Dataversessa määritetty kaksoiskirjoitus.

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