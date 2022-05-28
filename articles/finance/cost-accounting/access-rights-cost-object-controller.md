---
title: Käyttöoikeudet kustannusobjektin vastuuhenkilölle
description: Tässä ohjeaiheessa on tietoja kustannusobjektin vastuuhenkilöiden käyttöoikeuksista.
author: AndersGirke
ms.date: 06/24/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CAMCostControlWorkspace, CAMParameters
audience: Application User
ms.reviewer: twheeloc
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: twheeloc
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 13d562a4f42644b822c9548d1ea87d44a396b2c2
ms.sourcegitcommit: 5d1772bdeb21a9bec6dc49e64550aaf34127a4e2
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/10/2022
ms.locfileid: "8733875"
---
# <a name="access-rights-for-cost-object-controllers"></a>Käyttöoikeudet kustannusobjektin vastuuhenkilölle

[!include [banner](../includes/banner.md)]

Esimiehet voivat tarkastella **kustannusseurannan** työtilassa keskitetysti kustannusobjektiensa suoriutumista. Esimiehet voivat käyttää tässä tilassa kustannuslaskentatietoja, vaikka he eivät ole kustannuslaskijoita. Tietoturvasyistä esimiesten pitäisi saada tarkastella vain niitä kustannuslaskentatietoja, jotka liittyvät heidän vastuullaan olevien kustannusobjekteihin.

Kustannuslaskennassa on neljä yksilöivää roolia.

| Roolin nimi               | Käyttöoikeus      |
|-------------------------|--------------|
| Kustannuslaskennan hallinta | Tehtävä     |
| Kustannuslaskija         | Operations   |
| Kustannuslaskijan apulainen   | Operations   |
| Kustannusobjektin vastuuhenkilö  | Tiimin jäsenet |

Tässä ohjeaiheessa kerrotaan, miten **kustannusobjektin vastuuhenkilön** määritetään esimiehelle.

Kun **kustannusobjektin vastuuhenkilön** rooli on määritetty esimiehelle, tämä voi suorittaa seuraavat tehtävät:

- **kustannusseurannan** työtilan käyttö (asiakasohjelmassa)

    - porautumista tukevien sivujen poraus- ja tarkasteluoikeudet

- **kustannusseurannan** työtilan käyttö (mobiilisovelluksessa)

> [!NOTE]
> **kustannusobjektin vastuuhenkilön** roolilla ei voi hallita sitä, mitä kustannusobjekteja käyttäjä voi käyttää ja minkä tietoja hän voi tarkastella. Rivitason suojaus perustuu dimensio- ja käyttöoikeusluettelohierarkioihin.

## <a name="grant-access-rights"></a>Käyttöoikeuksien myöntäminen
Seuraavassa on esimerkki dimensiohierarkiasta.

**Dimension hierarkiatiedot**

| Dimensiohierarkian nimi | Dimensio    | Dimensiohierarkiatyypin nimi      | Käyttöoikeusluettelohierarkia |
|--------------------------|--------------|------------------------------------|-----------------------|
| Organisaatio             | Kustannuspaikat | Dimension luokitteluhierarkia | **Kyllä**               |

Voit lisätä kuhunkin solmuun käyttäjätunnuksia hierarkian suunnittelutoiminnon **Käyttäjät**-pikavälilehdessä.

|             Solmukohdat                 | Käyttäjät            | Lähtödimension jäsen     |   Kohdedimension jäsen   |
|-----------------------------------|------------------|---------------------------|-------------------------|
| Organisaatio                      | Benjamin, Claire |                           |                         |
| &nbsp;&nbsp;Hallinto                 | Huhtikuu            |                           |                         |
| &nbsp;&nbsp;&nbsp;&nbsp;Myyntitiedot   | Alicia           | CC002                     | CC003                   |
|                                   |                  | CC007                     | CC007                   |
| &nbsp;&nbsp;&nbsp;&nbsp;Henkilöstöhallinto        | Arnie            | CC001                     | CC001                   |
| &nbsp;&nbsp;Tuotanto            | David            |                           |                         |
| &nbsp;&nbsp;&nbsp;&nbsp;Pakkaus | Ellen            | CC005                     | CC005                   |
| &nbsp;&nbsp;&nbsp;&nbsp;Kokoonpano  | Chris            | CC006                     | CC006                   |

> [!NOTE]
> Kustannuslaskijat on määritettävä hierarkian ylimmälle tasolle, jotta he näkevät kaikki kustannuslaskennan merkinnät.

Ennen käyttöoikeushierarkian ja sen suojausasetusten käyttöönottoa **Ota käyttöön katseluoikeus kustannusobjektin dimension jäsenille** -asetukseksi on valittava **Kyllä** **Kustannuslaskentaparametrit**-sivun **Yleiset**-välilehdessä (**Kustannuslaskenta** > **Asetukset** > **Parametrit**).

Käyttöoikeusluettelohierarkian asetuksilla hallitaan seuraavilla alueilla näkyviä tietoja:

- **Kustannusseurannan** työtila (asiakasohjelmassa):

    - Porautumiseen käytettävien sivujen tiedot

- **Kustannusseurannan** työtila (mobiilisovelluksessa):

    - Korttien saldot

- Microsoft Power BI:

    - Power BI -visualisoinneissa näytettävät tiedot
    - Tietojen Power BI -visualisoinnit, jotka on upotettu Dynamics 365 Financen asiakasohjelmassa

> [!IMPORTANT]
> - Käyttöoikeusluettelon hierarkia ei ole vaikuta Power BI -tietoihin, ennen kuin käyttöoikeusluettelon hierarkia ja Power BI:n rivitason suojaus ovat muodostaneet parin. Lisätietoja on ohjeaiheessa [Kustannuslaskennan sisältöpaketin suojauksen määrittäminen](../../fin-ops-core/dev-itpro/analytics/setup-security-cost-accounting-content-pack.md).
> - Tässä ohjeaiheessa käsitellään edellytykset, joita ilman **kustannusseurannan** työtilaa ei voi käyttää.

Lisäresurssit

- [Kustannusseurannan työtila](cost-control-workspace.md)
- [Dimensiohierarkia](dimension-hierarchy.md)
- [Kustannuslaskennan sisältöpaketin määrittäminen](../../fin-ops-core/dev-itpro/analytics/setup-security-cost-accounting-content-pack.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
