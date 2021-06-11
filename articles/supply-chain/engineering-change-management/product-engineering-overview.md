---
title: Suunnittelun muutostenhallinnan yleiskuvaus
description: Tässä aiheessa on yleiskatsaus suunnittelun muutostenhallintaan, jonka avulla voi suunnitella ja hallita tuotteen versiointia sekä hallita tuotteen elinkaaria ja suunnittelun muutoksia.
author: t-benebo
ms.date: 11/11/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2020-09-28
ms.dyn365.ops.version: Release 10.0.15
ms.openlocfilehash: d9430fe02abe58f37d2bfd1431b4da61527d0834
ms.sourcegitcommit: 588f8343aaa654309d2ff735fd437dba6acd9d46
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/28/2021
ms.locfileid: "6115046"
---
# <a name="engineering-change-management-overview"></a>Suunnittelun muutostenhallinnan yleiskuvaus

[!include [banner](../includes/banner.md)]

## <a name="feature-summary"></a>Toiminnon yhteenveto

Valmistajat tarvitset nykyisin tehokasta tuotetietojen hallintaa, versionhallintaa ja suunnittelun muutoksenhallintaa, jotta ne menestyisivät jatkuvasti lyhenevistä tuotteiden elinkaaresta, kasvavista laatu- ja luotettavuusvaatimuksista sekä entistä tarkemmasta tuotteiden turvallisuustarkkailusta huolimatta.

Suunnittelun muutostenhallinta tuo rakennetta ja täsmällisyyttä tuotetietojen hallintaprosessiin sekä mahdollistaa tuotteiden hallitun määrittämisen, vapauttamisen ja korjaamiseen työnkulkujen avulla. Tuoteversioiden ja suunnittelun muutostenhallinnan ansiosta suunnittelun muutokset voidaan dokumentoida, niiden vaikutus voidaan arvioida ja ne voidaan ottaa käyttöön koko tuotteen elinkaaren ajan.

Suunnittelun muutostenhallinta auttaa suunnittelemaan ja hallitsemaan tuotteen versiointia sekä hallitsemaan tuotteen elinkaaria ja suunnittelun muutoksia. Tärkeimmät toiminnot:

- Tuotteen versiointi
- Parannettujen tuotteen vapautustoimintojen avulla voidaan ylläpitää tuotteen päätietoja yhdessä yrityksessä (suunnitteluyritys) ja julkaista täysin määritetyt vapautetut tuotteet muihin yrityksiin
- Säännöt, joilla tarkistetaan, että pakolliset tiedot on annettu ennen tuoteversion aktivointia (valmiustarkistukset)
- Parannettu tuotteen elinkaaren hallinta valvomalla tarkasti, milloin vapautettua tuotetta voidaan käyttää tietyissä liiketoimintaprosesseissa
- Työnkulkujen tukemat suunnittelun muutospyynnöt
- Työnkulkujen tukemat suunnittelun muutostilaukset

> [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RE4HE6B]

Edellä oleva video ([Dynamics 365 Supply Chain Managementin muutostenhallinnan ominaisuudet](https://youtu.be/N313FqvRuBc)) sisältyy [Finance and Operations -toistoluetteloon](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW), joka on saatavana YouTubessa.

## <a name="turn-on-the-engineering-change-management-and-version-dimension-features-for-your-system"></a>Ota suunnittelun muutostenhallinnan ja versiodimension toiminnot käyttöön järjestelmässä

Ennen kuin voit käyttää suunnittelun muutostenhallintaa, sinun on otettava käyttöön sekä *Suunnittelun muutostenhallinta* -toiminto että sen määritysavain. Jos haluat seurata myös tapahtumien versiodimensiota (valinnainen), sinun on otettava käyttöön myös *Tuoteversion dimensio* -toiminto ja sen määritysavain.

Ota toiminnot ensin käyttöön seuraavasti.

1. Valitse [Ominaisuuksien hallinta](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) -työtila.
1. Tarkista päivitysten saatavuus.
1. Ota käyttöön *Suunnittelun muutostenhallinta* -niminen toiminto.
1. Jos haluat käyttää sitä, sinun on otettava käyttöön myös *Tuotteen dimensioversio* -niminen toiminto.

Ota seuraavaksi määritysavaimet käyttöön seuraavia vaiheita noudattamalla.

1. Siirrä järjestelmä ylläpitotilaan kohdassa [Ylläpitotila](../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md) kuvatulla tavalla.
1. Valitse **Järjestelmän hallinta \> Asetukset \> Käyttöoikeuden konfiguraatio**.
1. **Kauppa**-solmun laajentaminen.
1. Ota pääominaisuuden määritysavain käyttöön valitsemalla **Suunnittelun muutostenhallinta** -valintaruutu.
1. Laajenna **Tekninen suunnittelun muutoksenhallinta** -solmu ja valitse tarpeen mukaan seuraavat valintaruudut tai poista niiden valinta (käytettävien ominaisuuksien mukaan):

    - **Määritteen haku** – Valitsemalla tämän valintaruudun voit ottaa [määritteen hakutoiminnon](engineering-attributes-and-search.md) käyttöön. On suositeltavaa ottaa tämä toiminto käyttöön, mutta voit poistaa valintaruudun valinnan, jos et käytä sitä.
    - **Prosessivalmistuksen muutoksenhallinta** – Valitse tämä valintaruutu, jos haluat hallita prosessivalmistuksen kaavojen muutoksia suunnittelumuutoksen hallintaominaisuuksien avulla. Jos kaavojen hallintaa ei tarvitse tehdä, tämän valintaruudun voi poistaa. Lisätietoja on kohdassa [Kaavojen ja niiden osien muutosten hallinta](manage-formula-changes.md).

1. Jos haluat myös käyttää versiodimensiota, valitse myös **Tuotedimensio – Versio** -valintaruutu. (Tämä valintaruutu on luettelossa alempana, ei **Suunnittelun muutoshallinta** -solmussa.)
1. Poista järjestelmän ylläpitotila käytöstä kohdassa [Ylläpitotila](../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md) kuvatulla tavalla.

> [!IMPORTANT]
> Huhtikuussa 2022 alkaen sekä **Suunnittelun muutostenhallinta**- että **Tuotedimensio - Versio** -lisenssiavaimet ovat oletusarvon mukaan käytössä kaikissa uusissa asennuksissa, mutta ne voidaan tarvittaessa poistaa käytöstä.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
