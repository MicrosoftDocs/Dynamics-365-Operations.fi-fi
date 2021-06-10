---
title: Kaavojen ja niiden osien muutosten hallinta
description: Tässä aiheessa kuvataan, miten kaavojen hallintaa ja prosessin valmistuksen perustietojen muutoksia hallitaan.
author: t-benebo
ms.date: 05/19/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2021-05-19
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 825cc5b9355695a648c857e5197b5b93a21fdb43
ms.sourcegitcommit: 588f8343aaa654309d2ff735fd437dba6acd9d46
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/28/2021
ms.locfileid: "6115182"
---
# <a name="manage-changes-in-formulas-and-their-ingredients"></a>Kaavojen ja niiden osien muutosten hallinta

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]

Jos käytät Microsoft Dynamics 365 Supply Chain Managementin prosessivalmistustoimintoja, voit hallita myös seuraavia muutoksia liittyvien kaavojen hallintaominaisuuksien avulla:

- **Kaava- ja suunnittelunimikkeet:** Hallitse kaavojen sekä niiden oheis- ja sivutuotteiden osiin tehtyjä muutoksia.
- **Oheistuotteet ja sivutuotteet:** Muokkaa kaavan oheistuotteiden ja sivutuotteiden määriä ja muita tietoja.
- **Todellisen painon nimikkeet:** Hallitse todellisen painon nimikkeiden muutoksia.

## <a name="turn-on-this-feature-in-your-system"></a>Tämän toiminnon ottaminen käyttöön järjestelmässä

Sinun täytyy suorittaa seuraavat toimet käyttääksesi tätä ominaisuutta:

1. Ota käyttöön *Suunnittelun muutostenhallinta* -ominaisuus ja sen konfigurointiavain, niin kuin aiheessa [Suunnittelun muutostenhallinnan yleiskatsaus on kuvattu](product-engineering-overview.md). Kuten tässä ohjeaiheessa mainitaan, varmista, että otat myös käyttöön **muutoksenhallinnan prosessivalmistuksen** käyttöoikeusavaimen, joka on **teknisen suunnittelun muutoksenhallinnan** pääkäyttöoikeusavaimen alapuolella.
1. Ota *Kaavojen ja niiden osien muutosten hallinta* käyttöön [ominaisuudenhallinnassa](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

## <a name="feature-naming-conventions"></a>Ominaisuuksien nimeämiskäytäntöjä

Supply Chain Managementin käyttöliittymässä ja dokumentaatiossa muutoksenhallintatoimintoja kutsutaan yleensä *suunnittelumuutosten hallinnaksi*, ja hallittavia tuotteita kutsutaan yleensä *suunnittelutuotteiksi*. Vaikka termejä ei yleensä ole liitetty prosessivalmistuksen kaavojen hallintaan, suunnittelussa on otettava käyttöön suunnittelun muutoksenhallinta yksinkertaisesti muutoksenhallintana. Muista, että suunnittelutuotteet tulisi ottaa käyttöön versiotuotteissa.

## <a name="work-with-formula-change-management-features"></a>Kaavan muutoksen hallintaominaisuuksien luominen

Seuraavassa luettelossa on yhteenveto siitä, miten kaavojen hallintaan sovelletaan suunnittelumuutosten hallintaominaisuuksia. Lisäksi siinä on linkkejä muihin tietoihin. Koska kaavojen muutoksenhallinta on etuna suunnittelumuutosten hallintaominaisuuksissa, sinun on hyvä opetella, miten suunnittelun muutoksenhallinta toimii yleisesti ja miten sitä voidaan käyttää kaavojen ja niiden osien hallintaan.

- **Keskitetty tuotetietojen hallinta** – Määritä organisaatio, joka varmistaa hallitun vapautusprosessin avulla, että käyttäjät voivat käyttää oikeita ja merkityksellisiä tuotetietoja koko yrityksessä. Lisätietoja on kohdassa [Suunnitteluyritykset ja tietojen omistussäännöt](engineering-org-data-ownership-rules.md).
- **Tuoteversioiminen** – Seurataan tuotteiden muutoksia tuoteversioiden kautta ja ohjataan tuotetta toimitusketjun kaikissa vaiheissa. Näin voit seurata muutoksia kaavojen hallinnassa. Lisätietoja on kohdassa [Suunnitteluversiot ja suunnittelun tuoteluokat](engineering-versions-product-category.md).
- **Tuotteiden elinkaaren hallinta** – Tuotetietojen näkyvyyden hallinta koko organisaatiossa ja tuoteversioiden käytettävyyden hallinta toimitusketjun jokaisessa vaiheessa. Voit hallita tarkasti, milloin tuoteversiota voidaan käyttää tietyissä liiketoimintaprosesseissa, ja voit luoda oman elinkaaren tilasi liiketoiminnan tarpeiden mukaan. Lisätietoja on kohdassa [Tuotteen elinkaaren tilat ja tapahtumat](product-lifecycle-state-transactions.md).
- **Kaavan muutoksen hallinta** – Organisaation käyttäjät voivat pyytää muutoksia kaavoihin. Muutostilausten avulla voit arvioida ja dokumentoida ehdotettujen muutosten vaikutuksia. Lisää työnkulut, jotka hallitsevat muutosprosessia sekä tuotteen ja sen kaavojen uusien versioiden vapautusta. Lisätietoja on kohdassa [Suunnittelutuotteiden muutosten hallinta](engineering-change-management.md).
- **Valmiuden hallinta** – Järjestelmän tarkistusten ja käyttäjän ohjeiden (kyselylomakkeiden ja tarkistusluetteloiden) avulla voit varmistaa, että kaikki tarvittavat tuotetiedot lisätään kokonaan ennen tuotteen vapauttamista. Lisätietoja on kohdassa [Tuotteen valmius](product-readiness.md).
- **Paranneltu tuotejulkaisutoiminto** – Vapauttaa tuotteen ja sen kaavan kokonaan määritetyt versiot organisaatiosta (yrityksestä) toisille yrityksille. Voit myös päättää, tuleeko tuotetiedot tarkistaa tai muokata, ennen kuin ne voidaan vapauttaa. Lisätietoja on kohdassa [Tuoterakenteiden vapauttaminen](release-product-structure.md).

Huomaa, että useimmat edellisessä luettelossa linkitetyt ohjeaiheet ovat esimerkkejä tuoterakenteista. Kaavat toimivat kuitenkin samalla tavalla. Seuraavassa on lisäkäsitteitä, jotka ovat hyödyllisiä kaavojen ja tuoterakenteiden hallinnassa, kun käytät muutoksenhallintaa (tai vain kaavan muutoksen hallintaa):

- Voit määrittää kullekin [tuotesuunnitteluluokalle](engineering-versions-product-category.md) tuotantotyypin (tuoterakenne, resepti tai suunnittelunimike). Voit myös määrittää, tarvitaanko tätä luokkaa luokiteltavassa tuotteiden todellisen painon tukea.
- Oheistuotteet ja sivutuotteet eivät ole suunnittelutuotteita. Siksi niitä ei versioida. Jos niitä on muutettava, luo vain uusi tuote. Tämä tapa helpottaa ylläpitoa.
- Voit hallita loppunimikkeitä, jotka ovat tuoterakenteita ja joista on alikaavanimikkeitä. Toimintoja käytetään tuoterakenteiden yhdistelmissä, jotka sisältävät tuoterakenteita ja/tai tuoterakenteita sisältäviä kaavoja.
