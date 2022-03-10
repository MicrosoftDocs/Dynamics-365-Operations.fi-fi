---
title: Korotettujen kenttien määrittäminen Warehouse Managementin mobiilisovelluksen vaiheita varten
description: Tässä aiheessa kuvataan, miten korotetaan ja korostetaan tiettyjä tietoja minkä tahansa Warehouse Managementin mobiilisovelluksen vaiheen osalta.
author: Mirzaab
ms.date: 10/15/2021
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2021-10-15
ms.dyn365.ops.version: 10.0.23
ms.openlocfilehash: 0ce3fb829d349a35c6c2f29838a2c725f7b61c55
ms.sourcegitcommit: 008779c530798f563fe216810d34b2d56f2c8d3c
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/14/2021
ms.locfileid: "7920320"
---
# <a name="configure-promoted-fields-for-steps-in-the-warehouse-management-mobile-app"></a>Korotettujen kenttien määrittäminen Warehouse Managementin mobiilisovelluksen vaiheita varten

[!include [banner](../includes/banner.md)]

> [!IMPORTANT]
> Tässä aiheessa käsitellyt toiminnot koskevat vain uutta Warehouse Management -mobiilisovellusta. Niillä ei ole vaikutusta vanhaan varastosovellukseen, joka on nyt vanhentunut.

Tässä aiheessa kuvataan, miten korotetaan ja korostetaan tiettyjä tietoja minkä tahansa Warehouse Managementin mobiilisovelluksen vaiheen osalta. Tämä ominaisuus auttaa kohdistamaan työntekijöiden huomiota tärkeimpiin kenttiin työnkulun suorittamisen aikana. Järjestelmänvalvojat voivat jokaisen prosessin vaiheen osalta valita, mitkä kentät korotetaan ja mitkä korostetaan.

## <a name="enable-promoted-fields-in-your-system"></a>Korotettujen kenttien käyttöönotto järjestelmässä

Ennen kuin voit määrittää korotettuja kenttiä, sinun suoritettava seuraava menettely, jolla otetaan käyttöön tarvittavat ominaisuudet ja luodaan tarvittavat kenttänimet Warehouse Managementin mobiilisovelluksessa.

1. Valitse **Järjestelmänvalvoja \> Työtilat \> Ominaisuuksien hallinta**.
1. Ota [**Ominaisuuksien hallinta** -työtilassa](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) luetteloitu ominaisuus käyttöön seuraavalla tavalla:

    - **Moduuli:** *Varastonhallinta*
    - **Toiminnon nimi:** *Varastosovelluksen vaiheohjeet*

    Lisätietoja *Varastosovelluksen vaiheohjeet*-toiminnosta: [Vaiheotsikkojen ja ohjeiden mukauttaminen Warehouse Management -mobiilisovelluksessa](mobile-app-titles-instructions.md). Tämä ominaisuus on edellytys *Varastosovelluksen korotetut kentät* -ominaisuudelle.

1. Ota luetteloitu toiminto käyttöön seuraavasti:

    - **Moduuli:** *Varastonhallinta*
    - **Ominaisuuden nimi:** *Varastosovelluksen korotetut kentät*

    Tämä ominaisuus kuvataan tässä aiheessa.

1. Päivitä Warehouse Management -mobiilisovelluksen kenttänimet siirtymällä kohtaan **Varastonhallinta \> Määritys \> Mobiililaite \> Varastosovelluksen kenttänimet** ja valitsemalla **Luo oletusmääritys**. Lisätietoja: [Varastonhallinnan mobiilisovelluksen kenttien konfigurointi](configure-app-field-names-priorities-warehouse.md).
1. Toista edellinen vaihe kullekin yritykselle, jossa käytät Warehouse Management -mobiilisovellusta.

## <a name="configure-promoted-fields-from-a-menu-specific-override"></a>Valikkokohtaisen ohituksen korotettujen kenttien määrittäminen

Seuraavien ohjeiden avulla voit määrittää korottuja kenttiä.

1. Luo valikkokohtainen ohitus kulloisellekin valikolle ja vaiheelle kohdan [Warehouse Management ‑mobiilisovelluksen vaiheiden otsikoiden ja ohjeiden mukauttaminen](mobile-app-titles-instructions.md) ohjeiden mukaisesti.
1. Etsi muokattavat **Vaiheen tunnus**- ja **Valikkovaihtoehdon nimi** -arvot ja valitse sitten arvo **Vaiheen tunnus** -sarakkeessa.
1. Valitse näkyviin tulevan sivun **Valitse korotetut kentät** -pikavälilehden työkalupalkin **Valitse kentät**.
1. Valitse **Korotetut kentät** -valintaikkunassa kentät, jotka haluat korottaa. Voit myös korostaa enintään kaksi valituista kentistä. Korostetut kentät näytetään lihavoituna Warehouse Managementin mobiilisovelluksessa. Kun valitset kenttiä, ota huomioon, että joissakin näytöissä voi niiden koon vuoksi näkyä vain yksi tai kaksi ylimmistä korotetuista kentistä. Esimerkin näiden asetusten käyttämisestä löydät myöhemmin tässä aiheessa esitettävästä skenaariosta.

    > [!NOTE]
    > **Käytettävissä olevat kentät** -luettelo on rajattu kenttiin, jotka voivat tulla näkyviin valikkokohteen osalta. Muut tekijät (kuten nimikkeen kokoonpano) kuitenkin määrittävät, näkyykö kenttä todella Warehouse Managementin mobiilisovelluksessa. Jos olet määrittänyt korotettuja kenttiä, vain valitut kentät näkyvät Warehouse Managementin mobiilisovelluksen pääsivulla. Työntekijät voivat kuitenkin tarkastella muitakin kenttiä napauttamalla tietosivua.

1. Ota asetukset käyttöön valitsemalla **OK**. Valitut kentät on nyt lueteltu **Valitse korotetut kentät**-pikavälilehdessä.

## <a name="example-scenario"></a>Esimerkkiskenaario

### <a name="enable-sample-data"></a>Mallitietojen ottaminen käyttöön

Jotta voit käyttää tämän skenaarion läpi käymisessä tarvittavia mallitietueita ja -arvoja, sinun on käytettävä järjestelmää, johon on asennettu vakio-demotiedot. Sinun on myös valittava **USMF**-yritys ennen aloittamista.

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