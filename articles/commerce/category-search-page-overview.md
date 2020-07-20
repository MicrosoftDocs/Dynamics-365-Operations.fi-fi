---
title: Luokan oletussaapumissivun ja oletushakutulossivun yleiskatsaus
description: Tässä ohjeaiheessa on luokan oletussaapumis- ja oletushakutulossivun yleiskatsaus Dynamics 365 Commerce -sovelluksessa.
author: ashishmsft
manager: annbe
ms.date: 06/30/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Operations, Retail, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: asharchw
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: e85449c10fa4a768a144ce423a77bd1fc2c94352
ms.sourcegitcommit: ce397c2759f642c595e30fef58a770b50360b2bd
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 07/01/2020
ms.locfileid: "3527465"
---
# <a name="default-category-landing-page-and-search-results-page-overview"></a>Luokan oletussaapumissivun ja oletushakutulossivun yleiskatsaus

[!include [banner](includes/banner.md)]

Tässä ohjeaiheessa on luokan oletussaapumis- ja oletushakutulossivun yleiskatsaus Microsoft Dynamics 365 Commercen sähköisessä kaupankäynnissä.

## <a name="default-category-landing-page"></a>Luokan oletussaapumissivu

Luokan oletussaapumissivu on sivu, jolle sivustojen käyttäjät yleensä siirretään, kun he valitsevat siirtymishierarkiassa luokan. Luokka-sivulla voit selata ja myös lajitella ja tarkentaa luokiteltuja tuotteita.

![Luokan oletussaapumissivu](./media/SimpleCategoryLandingDressCategory.png)

Sivun yläosassa on ylätunniste, jossa näkyvät kaikki tuoteluokat ja muut sivut, jotka myynninedistämispäällikkö on luokitellut. Määritys tehdään kanavan siirtymishierarkian määrityksen osana. Sivun alaosassa on alatunniste, joka sisältää pikalinkkejä erilaisiin ostajaa mahdollisesti kiinnostaviin aiheisiin.

Seuraavat komponentit ovat olennaisia luokassa:

- **Tuotesijoitteluruudut** näyttävät tuotteet, jotka myynninedistämispäällikkö on määrittänyt luokkaan siirtymishierarkian määrityksen osana.
- **Tarkennusten ja valinnan yhteenveto** ovat suodattimia määriä varten. Niiden avulla voi myös tarkentaa nimikkeitä. Myynninedistämispäällikkö määrittää ne osana kanavaluokkiin ja tuotemääritteisiin liittyvien metatietojen määritystä.
- **Lajitteluasetusten** avulla sivuston vierailijat voivat lajitella tuotteet. Oletusarvoisesti käytettävissä ovat seuraavat lajitteluvaihtoehdot:

    - Hinta – matalasta korkeaan
    - Hinta – korkeasta matalaan
    - Tuotteen nimi – \[A-Ö\]
    - Tuotteen nimi – \[Ö-A\]
    - Luokitukset – matalasta korkeaan
    - Luokitukset – korkeasta matalaan

- **Sivutuksen** avulla sivuston vierailijat voivat siirtyä yhdeltä luokitellun tuotteen sivulta toiselle.
- **Kokonaismäärä** määrittää luokkaan määritettyjen tuotteiden kokonaismäärän.

## <a name="enrich-a-category-landing-page"></a>Luokan saapumissivun täydentäminen

Jos haluat, että luokan saapumissivun tietyllä luokalla on paljon räätälöityä kokemusta, voit täydentää kyseisen luokan saapumissivua. Voit esimerkiksi lisätä markkinointivideon ja joitakin luokan tarinoita, joiden avulla saat ostajan huomion. Lisätietoja on kohdassa [Luokan saapumissivun täydentäminen](enrich-category-page.md).

![Täydennetty luokan saapumissivu](./media/CategoryLandingPages.png)

## <a name="auto-suggest-and-search-results-pages"></a>Automaattisten ehdotusten ja hakutulosten sivut

Sivuston käyttäjät voivat selata sivustoa siirtymishierarkian luokan avulla tai syöttämällä hakutermin hakukenttään.

Heti, kun käyttäjät alkavat kirjoittaa tekstiä hakukenttään, he näkevät automaattisen ehdotustoiminnon, joka ehdottaa hakutermejä.

Seuraavassa on joitakin ehdotuksia, jotka saattavat tulla näkyviin:

- **Avainsanoja** käytetään etsittäessä nimikkeitä kaikista kanavan tuotteista.
- **Tuotteet** sisältävät suorat linkit tuotetietosivulle.
- **Luokkahakualueen ehdotukset** tuovat näyttöön eri luokkia. Niiden avulla käyttäjät voivat hakea tietyn luokan avainsanoja.

![Mukaansatempaava automaattinen ehdotustoiminto](./media/ImmersiveAutoSuggestUX.png)

Kun käyttäjät valitsevat jonkin avainsanan tai luokkahakualueen ehdotukset tai kun hakutermillä ei saada ehdotuksia, käyttäjät siirretään hakutulossivulle. Käyttäjät voivat tämän jälkeen selata, lajitella ja tarkentaa hakutulosluetteloa löytääksesi haluamasi nimikkeen.

![Aloitussivu](./media/SearchLanding.png)

Seuraavat osat ovat olennaisia hakutulossivulla:

- **Tuotesijoitteluruudut** näyttävät käyttäjän haun tuotteet. Oletusarvoisesti nämä ruudut lajitellaan pilvipohjaisen hakurelevanssin pisteiden mukaan käyttäjähaussa.
- **Tarkennusten ja valinnan yhteenveto** ovat suodattimia määriä varten. Niiden avulla voi myös tarkentaa nimikkeitä. Myynninedistämispäällikkö määrittää ne osana kanavaluokkien ja tuotemääritteiden metatietojen määritystä.
- **Lajitteluasetusten** avulla sivuston vierailijat voivat lajitella tuotteet. Oletusarvoisesti käytettävissä ovat seuraavat lajitteluvaihtoehdot:

    - Hinta – matalasta korkeaan
    - Hinta – korkeasta matalaan
    - Tuotteen nimi – \[A-Ö\]
    - Tuotteen nimi – \[Ö-A\]
    - Luokitukset – matalasta korkeaan
    - Luokitukset – korkeasta matalaan
    - Oletus

- **Sivutuksen** avulla sivuston vierailijat voivat siirtyä yhdeltä luokitellun tuotteen sivulta toiselle.
- **Kokonaismäärä** määrittää luokkaan määritettyjen ja hakuehtoja vastaavien tuotteiden kokonaismäärän.

>[!NOTE]
>Nämä pilvipohjaiset hakutoiminnot ovat saatavilla versiosta 10.0.8 alkaen. Varmista, että valikossa **Kaupan parametrit > Määrityksen parametrit** on merkintä ProductSearch.UseAzureSearch set to 'true'. 
![Määrityksen parametrit pilvipohjaiselle haulle](./media/CloudPoweredSearchConfigurationParameters.png)

## <a name="additional-resources"></a>Lisäresurssit

[Pilvipohjaisen haun yleiskatsaus](cloud-powered-search-overview.md)

[Aloitussivun yleiskatsaus](quick-tour-home-page.md)

[Tuotetietosivujen yleiskatsaus](quick-tour-pdp.md)

[Ostoskorin ja maksusivun yleiskatsaus](quick-tour-cart-checkout.md)

[Tilinhallintasivujen yleiskatsaus](quick-tour-account-management.md)

