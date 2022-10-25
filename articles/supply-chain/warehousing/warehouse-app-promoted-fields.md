---
title: Korotettujen kenttien määrittäminen Warehouse Managementin mobiilisovelluksen vaiheita varten
description: Tässä artikkelissa kuvataan, miten korotetaan ja korostetaan tiettyjä tietoja minkä tahansa Warehouse Managementin mobiilisovelluksen vaiheen osalta.
author: Mirzaab
ms.date: 08/09/2022
ms.topic: article
ms.search.form: WHSMobileAppFlowStepSelectPromotedFields, WHSMobileAppFlowStepListPage, WHSMobileAppFlowStepAddDetour, WHSMobileAppFlowStepDetourSelectFields
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2021-10-15
ms.dyn365.ops.version: 10.0.23
ms.openlocfilehash: e2d65f20febaf9bd1d143414054b121f8decb7c0
ms.sourcegitcommit: 3e04f7e4bc0c29c936dc177d5fa11761a58e9a02
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/18/2022
ms.locfileid: "9689827"
---
# <a name="configure-promoted-fields-for-steps-in-the-warehouse-management-mobile-app"></a>Korotettujen kenttien määrittäminen Warehouse Managementin mobiilisovelluksen vaiheita varten

[!include [banner](../includes/banner.md)]

> [!IMPORTANT]
> Tässä artikkelissa käsitellyt toiminnot koskevat vain uutta Warehouse Management -mobiilisovellusta. Niillä ei ole vaikutusta vanhaan varastosovellukseen, joka on nyt vanhentunut.

Tässä artikkelissa kuvataan, miten korotetaan ja korostetaan tiettyjä tietoja minkä tahansa Warehouse Managementin mobiilisovelluksen vaiheen osalta. Tämä ominaisuus auttaa kohdistamaan työntekijöiden huomiota tärkeimpiin kenttiin työnkulun suorittamisen aikana. Järjestelmänvalvojat voivat jokaisen prosessin vaiheen osalta valita, mitkä kentät korotetaan ja mitkä korostetaan.

## <a name="enable-promoted-fields-in-your-system"></a>Korotettujen kenttien käyttöönotto järjestelmässä

Jos käytössä on Supply Chain Managementin version 10.0.28 tai aiempi versio, sinun suoritettava ennen korotettuja kenttien määrittämistä seuraava menettely, jolla otetaan käyttöön tarvittavat toiminnot ja luodaan tarvittavat kenttänimet Warehouse Managementin mobiilisovelluksessa. Jos käytössä on Supply Chain Managementin versio 10.0.29 tai uudempi versio, toiminnot ovat pakollisia, eikä niitä voi poistaa käytöstä. Voit siis ohittaa tämän menettelyn.

1. Valitse **Järjestelmänvalvoja \> Työtilat \> Ominaisuuksien hallinta**. (Katso lisätietoja tästä sivusta kohdasta [Toimintojen hallinnan yleiskuvaus](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).)
1. Varmista, että *Varastosovelluksen vaiheohjeet* -ominaisuus on käytössä järjestelmässäsi. Tämä ominaisuus on edellytys *Varastosovelluksen korotetut kentät* -ominaisuudelle. Supply Chain Managementin versiosta 10.0.29 alkaen se on pakollinen, eikä sitä voi poistaa käytöstä. Lisätietoja *Varastosovelluksen vaiheohjeet*-toiminnosta: [Vaiheotsikkojen ja ohjeiden mukauttaminen Warehouse Management -mobiilisovelluksessa](mobile-app-titles-instructions.md).
1. Varmista, että *Varastosovelluksen ylemmälle tasolle siirretyt kentät* -toiminto on käytössä järjestelmässäsi. Tätä toimintoa käsitellään tässä artikkelissa. Supply Chain Managementin versiosta 10.0.29 alkaen se on pakollinen, eikä sitä voi poistaa käytöstä.
1. Päivitä Warehouse Management -mobiilisovelluksen kenttänimet siirtymällä kohtaan **Varastonhallinta \> Määritys \> Mobiililaite \> Varastosovelluksen kenttänimet** ja valitsemalla **Luo oletusmääritys**. Toista tämä vaihe jokaiselle yritykselle, jossa käytät Warehouse Management -mobiilisovellusta. Lisätietoja: [Varastonhallinnan mobiilisovelluksen kenttien konfigurointi](configure-app-field-names-priorities-warehouse.md).

## <a name="configure-promoted-fields-from-a-menu-specific-override"></a>Valikkokohtaisen ohituksen korotettujen kenttien määrittäminen

Seuraavien ohjeiden avulla voit määrittää korottuja kenttiä.

1. Luo valikkokohtainen ohitus kulloisellekin valikolle ja vaiheelle kohdan [Warehouse Management ‑mobiilisovelluksen vaiheiden otsikoiden ja ohjeiden mukauttaminen](mobile-app-titles-instructions.md) ohjeiden mukaisesti.
1. Etsi muokattavat **Vaiheen tunnus**- ja **Valikkovaihtoehdon nimi** -arvot ja valitse sitten arvo **Vaiheen tunnus** -sarakkeessa.
1. Valitse näkyviin tulevan sivun **Valitse korotetut kentät** -pikavälilehden työkalupalkin **Valitse kentät**.
1. Valitse **Korotetut kentät** -valintaikkunassa kentät, jotka haluat korottaa. Voit myös korostaa enintään kaksi valituista kentistä. Korostetut kentät näytetään lihavoituna Warehouse Managementin mobiilisovelluksessa. Kun valitset kenttiä, ota huomioon, että joissakin näytöissä voi niiden koon vuoksi näkyä vain yksi tai kaksi ylimmistä korotetuista kentistä. Esimerkin näiden asetusten käyttämisestä löydät myöhemmin tässä artikkelissa esitettävästä skenaariosta.

    > [!NOTE]
    > **Käytettävissä olevat kentät** -luettelo on rajattu kenttiin, jotka voivat tulla näkyviin valikkokohteen osalta. Muut tekijät (kuten nimikkeen kokoonpano) kuitenkin määrittävät, näkyykö kenttä todella Warehouse Managementin mobiilisovelluksessa. Jos olet määrittänyt korotettuja kenttiä, vain valitut kentät näkyvät Warehouse Managementin mobiilisovelluksen pääsivulla. Työntekijät voivat kuitenkin tarkastella muitakin kenttiä napauttamalla tietosivua.

1. Ota asetukset käyttöön valitsemalla **OK**. Valitut kentät on nyt lueteltu **Valitse korotetut kentät**-pikavälilehdessä.

## <a name="example-scenario"></a>Esimerkkiskenaario

### <a name="enable-sample-data"></a>Mallitietojen ottaminen käyttöön

Jos haluat suorittaa tämän skenaarion käyttämällä määritettyjä esimerkkitietueita ja -arvoja, sinun täytyy käyttää järjestelmää, johon vakiomuotoiset [demotiedot](../../fin-ops-core/fin-ops/get-started/demo-data.md) on asennettu. Sinun on myös valittava **USMF**-yritys ennen aloittamista.

### <a name="configure-sales-picking-with-promoted-steps-on-the-license-plate-step"></a>Myyntikeräilyn määrittäminen korotetuilla vaiheilla rekisterikilpivaiheessa

Tässä menettelyssä määrität korotettuja ja korotettuja kenttiä **Myynnin keräily** -valikkokohteelle rekisterikilpivaiheessa.

1. Valitse **Varastonhallinta \> Asetukset \> Mobiililaite \> Mobiililaitteen vaiheet**.
1. Etsi vaihetunnus nimeltä *LicensePlateId* ja valitse se.
1. Valitse toimintoruudussa **Luo vaiheen määritys**.
1. Käytä avattavassa valintaikkunassa kenttää **Valikkokohde** etsiäksesi ja valitaksesi *Myynnin keräily*.
1. Valitse **OK**.
1. Luomasi ohituksen tietosivu tulee näkyviin. Valitse **Valitse korotetut kentät** -pikavälilehden työkalupalkin **Valitse kentät**.
1. **Korotetut kentät** -valintaikkunassa voit valita korotettavat ja korostettavat kentät. Hae **Käytettävissä olevat kentät** -luettelosta seuraavat kentät, valitse ne ja siirrä ne **Valitut kentät** -luetteloon painikkeiden avulla:

    - Sijainti
    - Nimike
    - Tuotteen nimi
    - Varaston tila

1. Ylä- ja alanuolipainikkeiden avulla voit mukauttaa **Valitut kentät** -luettelon kenttien järjestystä. Warehouse Managementin mobiilisovelluksessa kentät tulevat näkyviin tässä valitsemassasi järjestyksessä.
1. Valitse **Sijainti**-kenttä ja valitse sitten **Korosta**.
1. Tallenna määritys valitsemalla **OK**.

### <a name="view-the-promoted-fields-in-the-warehouse-management-mobile-app"></a>Korotettujen kenttien tarkastelu Warehouse Management -mobiilisovelluksessa

Tässä menettelyssä avataan Warehouse Managementin mobiilisovellus ja suoritetaan vaiheet, joiden avulla voidaan tarkastella edellisessä menettelyssä korotettuja ja korostettuja kenttiä.

1. Luo Microsoft Dynamics 365 Supply Chain Managementissa myyntitilaus, joka edellyttää keräilyvaihetta sijainnissa, jota seurataan rekisterikilvillä. Vapauta myyntitilaus sitten varastoon. Kirjoita luotu työn tunnus muistiin.
1. Avaa Warehouse Management -mobiilisovellus ja kirjaudu sisään varastoon 24. (Kirjaudu standardidemotiedoissa sisään käyttämällä numeroa *24* käyttäjätunnuksena ja numeroa *1* salasanana.)
1. Valitse **Lähtevät**-valikko ja valitse sitten **Myynnin keräily** -valikkokohde.
1. Noudata näytön tiedonsyöttöohjeita ja syötä vaiheessa 1 luotu työn tunnus.
1. Vaiheessa, joka sisältää tekstin **Skannaa rekisterikilpi**, pitäisi nähdä muutokset, jotka on tehty tietosivulla. Kentät näkyvät siinä järjestyksessä, joka on määritetty korotetuille kentille, ja **Sijainti**-kenttä näkyy lihavoituna.
