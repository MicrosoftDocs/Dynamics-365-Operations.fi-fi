---
title: Asiakkaan maksuennusteiden käyttöönotto (esiversio)
description: Tässä ohjeaiheessa kerrotaan, miten Asiakkaan maksuennusteet -toiminto otetaan käyttöön ja määritetään Finance Insightsissa.
author: ShivamPandey-msft
ms.date: 07/16/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-05-29
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: 03320aa925ae94ef39d54e64701846089ec66084
ms.sourcegitcommit: e42c7dd495829b0853cebdf827b86a7cf655cf86
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 07/17/2021
ms.locfileid: "6638581"
---
# <a name="enable-customer-payment-predictions-preview"></a>Asiakkaan maksuennusteiden käyttöönotto (esiversio)

[!include [banner](../includes/banner.md)]

Tässä ohjeaiheessa kerrotaan, miten Asiakkaan maksuennusteet -toiminto otetaan käyttöön ja määritetään Finance Insightsissa. Toiminto otetaan käyttöön **Toimintojen hallinta** -työtilassa ja määritysasetukset syötetään **Financial Insights -parametrit** -sivulla. Tämä ohjeaihe sisältää tietoja, joiden avulla voit käyttää toimintoa tehokkaasti.

> [!NOTE]
> Ennen kuin suoritat seuraavat vaiheet, varmista, että olet suorittanut ennalta suoritettavat vaiheet [Määritykset Finance Insightsia varten](configure-for-fin-insites.md) -ohjeaiheesta.

1. Muodosta yhteys ympäristön Azure SQL:n ensisijaiseen esiintymään Microsoft Dynamics Lifecycle Services (LCS) -ratkaisun ympäristösivun tietojen avulla. Suorita seuraava Transact-SQL (T-SQL) -komento, jos haluat ottaa käyttöön eristysympäristön väliversiotestaukset. (Sinun on ehkä otettava käyttöön IP-osoitteen käyttö LCS:ssä ennen etäyhteyden muodostamista Application Object Serveriin \[AOS\].)

    `INSERT INTO SYSFLIGHTING (FLIGHTNAME, ENABLED) VALUES ('PayPredEnableFeature', 1)`

    > [!NOTE]
    > Ohita tämä vaihe, jos käytössä on versio 10.0.20 tai myöhempi versio tai jos käytössä on Service Fabric -toteutus. Finance Insightsin ryhmä on todennäköisesti jo ottanyt sen käyttöön. Jos et näe ominaisuutta **Toimintojen hallinta** -työtilassa tai jos sen käyttöönotossa on ongelmia, ota yhteyttä käyttämällä osoitetta <fiap@microsoft.com>. 

2. Ota käyttöön Asiakasmaksun tiedot -toiminto:

    1. Valitse **Järjestelmänvalvoja \> Työtilat \> Ominaisuuksien hallinta**.
    2. Etsi toiminto, jonka nimi on **Asiakasmaksujen tiedot (esiversio)**.
    3. Valitse **Ota käyttöön nyt**.

    Asiakasmaksujen tiedot -toiminto on nyt käytössä ja valmis määritettäväksi.

3. Määritä Asiakasmaksun tiedot -toiminto:

    1. Siirry kohtaan **Luotonvalvonta \> Asetukset \> Finance Insights \> Finance Insights -parametrit**.

        [![Financial Insights -parametrit -sivu ennen toiminnon määrittämistä.](./media/finance-insights-parameters.png)](./media/finance-insights-parameters.png)

    2. Valitse **Financial Insights -parametrit** -sivun **Asiakasmaksun tiedot** -välilehdessä **Ennustemallissa käytettyjen tietokenttien tarkasteleminen** -linkki ja avaa **Ennustemallin tietokentät** -sivu. Siellä voit tarkastella oletusluetteloa kentistä, joita käytetään asiakkaan maksuennusteiden tekoälyennustemallissa.

        Jos haluat käyttää kenttien oletusluetteloa ja luoda ennustemallin, sulje **Ennustemallin tietokentät** -sivu ja määritä sitten **Financial Insights -parametrit** -sivu ja **Ota toiminto käyttöön** -vaihtoehdon arvoksi **Kyllä**.

    3. Määrtä erittäin paljon myöhässä -tapahtumakausi, jotta voit määrittää, mitä **Erittäin paljon myöhässä** -ennustesäilö tarkoittaa yrityksessä.

        Järjestelmä ennustaa avoimen laskun maksun todennäköisyyden kolmen säilön avulla: **Ajoissa**, **Myöhässä** ja **Erittäin paljon myöhässä**.

        - **Ajoissa** – Tämä säilö sisältää maksut, jotka on ennustettu maksettavaksi ajoissa tai ennen tapahtuman eräpäivää.
        - **Myöhässä** – Tämä säilö sisältää maksut, jotka on ennustettu maksettavaksi tapahtuman eräpäivän jälkeen, mutta ennen Erittäin paljon myöhässä -tapahtumakautta.
        - **Erittäin paljon myöhässä** – Tämä säilö sisältää maksut, jotka on ennustettu maksettavaksi Erittäin paljon myöhässä -tapahtumakauden alun jälkeen.

        > [!NOTE]
        > Jos muutat Erittäin paljon myöhässä -tapahtumakautta ja valitset **Muuta myöhäistä rajaa** -arvoa asiakasmaksujen tekoälyennustemallin luomisen jälkeen, olemassa oleva ennustemalli poistetaan ja uusi luodaan. Uusi ennustemalli siirtää tapahtumat Erittäin paljon myöhässä -kauteen määritettyjen asetusten perusteella.

    4. Kun Erittäin paljon myöhässä -tapahtumakausi on määritetty, valitse **Luo ennustemalli** ja luo ennustemalli. **Ennustemalli**-osassa **Financial Insights -parametrit** -sivulla näkyy ennustemallin tila.

        > [!NOTE]
        > Kun ennustemallia luodaan, voit käynnistää prosessin uudelleen valitsemalla **Nollaa mallin luominen**.

    Toiminto on nyt määritetty ja valmis käytettäväksi.

Kun toiminto on otettu käyttöön ja määritetty ja ennustemalli luotu ja toiminnassa, **Ennustemalli**-osa **Financial Insights -parametrit** -sivulla näyttää mallin tarkkuuden seuraavan kuvan mukaisesti.

[![Financial Insights -parametrit -sivun ennustemallin tarkkuus.](./media/finance-insights-parameters-accuracy.png)](./media/finance-insights-parameters-accuracy.png)

## <a name="release-details"></a>Julkaisun tiedot

Finance Insightsin julkinen esiversio on saatavilla koekäyttöönotoissa Yhdysvalloissa, Euroopassa ja Yhdistyneessä kuningaskunnassa. Microsoft lisää tukea jatkuvasti myös muilla alueilla.

Julkisen esiversion ominaisuudet voidaan ottaa käyttöön vain Taso 2 -eristysympäristöissä. Eristysympäristössä luotuja määrityksiä ja tekoälymalleja ei voi siirtää tuotantoympäristöön. Lisätietoja on kohdassa [Microsoft Dynamics 365 -esiversioiden lisäkäyttöehdot](../../fin-ops-core/fin-ops/get-started/public-preview-terms.md).

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
