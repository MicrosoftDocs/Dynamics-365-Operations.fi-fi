---
title: "Kustannusobjektin vastuuhenkilöiden käyttöoikeuksien määrittäminen"
description: "Tässä ohjeaiheessa on tietoja kustannusobjektin vastuuhenkilöiden käyttöoikeuksista."
author: AndersGirke
manager: AnnBe
ms.date: 06/24/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CAMCostControlWorkspace, CAMParameters
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 2ba38ddc5c717df29462e4316dc5045d0eef8c1a
ms.contentlocale: fi-fi
ms.lasthandoff: 11/03/2017

---

# <a name="access-rights-of-a-cost-object-controller"></a>Kustannusobjektin vastuuhenkilön käyttöoikeudet

[!include[banner](../includes/banner.md)]

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

|                                   | Käyttäjät            | Dimension jäsenalueet   |                         |
|-----------------------------------|------------------|---------------------------|-------------------------|
| **Solmukohdat**                         | **Käyttäjätunnus**      | **Lähtödimension jäsen** | **Kohdedimension jäsen** |
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
    - Microsoft Dynamics 365 for Finance and Operations, Enterprise Editionin asiakasohjelmaan upotetut tietojen Power BI -visualisoinnit

> [!IMPORTANT]
> - Käyttöoikeusluettelohierarkialla ei ole vaikutusta Power BI -tietoihin, ennen kuin käyttöoikeusluettelohierarkia ja Power BI:n rivitason suojaus ovat muodostaneet parin. Lisätietoja on ohjeaiheessa [Kustannuslaskennan sisältöpaketin suojauksen määrittäminen](../../dev-itpro/analytics/setup-security-cost-accounting-content-pack.md).
> - Tässä ohjeaiheessa käsitellään edellytykset, joita ilman **kustannusseurannan** työtilaa ei voi käyttää.

Lisätietoja

- [Kustannusseurannan työtila](cost-control-workspace.md)
- [Dimensiohierarkia](dimension-hierarchy.md)
- [Kustannuslaskennan sisältöpaketin määrittäminen](../../dev-itpro/analytics/setup-security-cost-accounting-content-pack.md)

