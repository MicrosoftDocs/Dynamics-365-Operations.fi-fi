---
title: Luo uusi projekti
description: Tämä ohjeaihe sisältää uuden projektin luomista käsitteleviä tietoja.
author: Yowelle
manager: AnnBe
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c8c52b8c1c86ea2f6e03cf439ba5930f1006ab4f
ms.sourcegitcommit: 241ada0945c72d769eaa70ae35aedbb6a3233fdf
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/02/2020
ms.locfileid: "3760533"
---
# <a name="create-a-new-project"></a>Luo uusi projekti

[!include [banner](../includes/banner.md)]

Luo uusi projekti seuraavalla tavalla.

1. Valitse **Projektin hallinta** -sivulla **Uusi projekti** ja anna seuraavat arvot:

    - **Projektityyppi:** Aika ja materiaali
    - **Projektin nimi:** XYZ-päivitysvaihe 2
    - **Projektiryhmä**: TM\_WIP
    - **Projektisopimuksen tunnus:** 00000002

2. Valitse **Luo projekti**.

## <a name="assign-a-resource-to-a-project"></a>Resurssin määrittäminen projektiin

1. Valitse **Työntekijät**-sivun **Työntekijät**-luettelosta sen työntekijän tietue, jonka osaamisalueet määritit aiemmassa vaiheessa, ja avaa tietue.
2. Valitse toimintoruudussa **Projekti**-välilehden **Asetukset**-ryhmästä **Määritä projektit**.
3. Suodata **Resurssin oikeellisuustarkistuksen projektimääritykset** -sivun **Projektit**-välilehden **Lisää projekti valittuihin projekteihin** -kentässä **XYZ-päivitysvaihe 2** -projektiin.
4. Valitse **Jäljellä olevat projektit** -ruudusta haluamasi projekti ja lisää se **Valitut projektit** -ruutuun napsauttamalla nuolta.

Tarvittaessa voit myös määrittää resurssille luokkia. Luokkatyyppi on joko **Kustannus** tai **Tuotto**. Luokkatyyppi määräytyy organisaation mukaan. Jos resurssille ei ole määritetty luokkia, Finance etsii oletusluokan kustannusten ja tuoton tuntihinnoista.

## <a name="set-up-project-resource-and-role-characteristics"></a>Projektin resurssin ja rooliominaisuuksien määrittäminen

Projektipäällikkö voi projektin resursointitoiminnolla luoda projektissa tarvittavia rooleja. Rooleja voidaan käyttää, kun vahvistetut resurssit eivät ole vielä tiedossa resurssien varaamisen aikana. Rooleja voidaan väliaikaisesti varata suunnitelluiksi resursseiksi, jotta voit jatkaa projektin suunnitteluvaiheita.

[![Esimerkki roolista](./media/projectresourcing05.jpg)](./media/projectresourcing05.jpg) 

**Skenaario:** Contoso palkattiin suorittamaan aika- ja materiaaliprojekti, jolla on hyväksytty projektin perustamisasiakirja. Nuorempi projektipäällikkö on yhä laatimassa projektin laajuutta. Resurssipäällikkö on parhaillaan määrittämässä resursseja, jotka varataan uuteen projektiin. Koska projekti on erityisen tärkeä, projektin sponsori on toivonut yhden rooleista olevan vastaava projektipäällikkö. Resurssipäällikön on hankittava uusi resurssi, ja hän määrittää roolin järjestelmään siltä varalta, että nuorempi projektipäällikkö tarvitsee resurssitiedot projektin suunnittelua varten.

Seuraavissa vaiheissa on esitetty, miten resurssipäällikkö voi määrittää vastaavan projektipäällikön roolin ja liittää siihen resurssin ominaisuudet. Myöhemmin roolin avulla voidaan hakea käytettävissä olevia resursseja, jotka vastaavat tarvittavia resurssin osaamisalueita.

1. Valitse **Määritä roolit** -sivulla **Uusi** ja anna seuraavat arvot:

    - **Roolin tunnus:** Vastaava projektipäällikkö
    - **Kuvaus:** Vastaava projektipäällikkö

2. Valitse **Luo**.
3. Valitse **Vastaava projektipäällikkö** -rooli ja sitten **Määritä ominaisuudet**.
4. Valitse **Ominaisuuden tyyppi** -kentästä **Osaamisalue**.
5. Syötä **Käytettävissä olevat ominaisuudet** -kenttään haettava osaamisalue.
6. Valitse **Ominaisuustyyppi**-kentästä **Todistus**.
7. Syötä **Käytettävissä olevat ominaisuudet** -kenttään haettava todistustyyppi.

## <a name="assign-a-project-resource-to-a-project"></a>Projektiresurssin määrittäminen projektiin

1. Valitse **Kaikki projektit** -sivulla **XYZ-päivitysvaihe 2** -projekti.
2. Valitse **Projektiryhmä ja ajoitus** -välilehdestä **Lisää**.
3. Valitse **Rooli**-kentästä **Ryhmän jäsen**.
4. Valitse **Varaa kalenterista**.
5. Valitse **Resurssin saatavuus** -sivulta **Näyttöasetukset**.
6. Syötä **Muuta näyttöasetuksia** -sivulle seuraavat arvot:

    - **Päivämääräalueen muoto:** Päivä
    - **Näytä saatavuuskuvaukset:** Kyllä
    - **Näytä jäljellä oleva kapasiteetti:** Kyllä

7. Valitse resurssiluettelosta haluamasi resurssi.
8. Valitse **Kiinteä varaus** ja **Koko kapasiteetti**.

## <a name="assign-a-resource-to-a-default-role"></a>Resurssin määrittäminen oletusrooliin

Voit auttaa projekti- tai resurssipäälliköitä porautumalla alemmas resursseihin, jotka voidaan varata projektiin. Voit liittää oletusroolin aiemmin luotuun tai vasta hankittuun resurssiin. Esimerkiksi kun Daniel palkattiin, hänellä oli yritysanalyytikon rooliin tarvittava kokemus ja osaamisalueet. Resurssipäällikkö määritti tämän roolin Danielin oletusrooliksi. Resurssipäällikkö lisäsi Danielin toisin sanoen niiden yritysanalyytikkojen pooliin, jotka ovat käytettävissä projekteissa.

Resurssin varaamisen yhteydessä projektipäälliköt voivat suodattaa roolin resurssit, jotka ovat käytettävissä projektitöihin. Päälliköt voivat käyttää näitä tietoja yhtenä ehtona analysoidessaan päätöksiä useiden ehtojen perusteella resurssien täyttämisen yhteydessä. He voivat lisätä suodattimeen muitakin resurssin ominaisuuksia ja hakea niiden avulla resursseja, joilla on projektissa tarvittavat osaamisalueet, koulutus ja kokemus.

**Skenaario:** Hyväksytty projekti on alkanut, ja vastaavan projektipäällikön rooli on varattu suunniteltuna resurssina projektin suunnitteluvaiheessa. Resurssipäällikön on nyt hankittava rooliin sopiva resurssi.

1. Valitse **Resurssiluettelo**-sivulta **Daniel Goldschmidt**.
2. Valitse **Resurssin rooli** -sivulla **Uusi** ja anna seuraavat arvot:

    - **Voimassa:** Anna nykyinen päivämäärä.
    - **Päättyminen:** anna arvoksi **Ei koskaan**.
    - **Rooli:** anna arvoksi **Vastaava projektipäällikkö**.

3. Valitse **Tallenna** ja sulje sitten sivu.
4. Lisää **Osaamistiedot**-välilehdessä **ProjectMgmt**-osaamisalue ja **PMP**-todistus.
