---
title: Ylläpidon tarkistuslistat
description: Tässä ohjeaiheessa kuvataan ylläpidon tarkistuslistoja resurssien hallinnassa.
author: josaw1
manager: AnnBe
ms.date: 08/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-15
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 325ff1fa0811d6aac5189cc69f21483fce6b3e8f
ms.sourcegitcommit: f5bfa3212bc3ef7d944a358ef08fe8863fd93b91
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/16/2019
ms.locfileid: "1875636"
---
# <a name="maintenance-checklists"></a>Ylläpidon tarkistuslistat


[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

Kunnossapitotarkistusluettelot määritetään huoltotöidentyypeille, ja niitä käytetään työtilausta käsiteltäessä. Kunnossapidon tarkistuslistojen täyttäminen on osa työtilauksen täyttämistä. Lisätietoja kunnossapidon tarkistusluetteloiden määrittämisestä ylläpitotyötyypeille **Ylläpitotyön tyyppien oletukset** -lomakkeessa on kohdassa [Ylläpitotöiden tyyppiluokat ja ylläpitotöiden tyypit, ylläpitotöiden tyyppien variantit, ylläpitotöiden toimialat ja ylläpidon tarkistuslistat](../setup-for-work-orders/job-groups-and-job-types-variants-trades-and-checklists.md).

Kun käsittelet kunnossapidon tarkistuslistoja työtilauksessa, voit täyttää valmiiksi määritetyt kunnossapitotöiden tarkistusluettelot, jotka liittyvät kunnossapitotyötyyppeihin. On myös mahdollista lisätä kunnossapidon lisätarkistuslistoja.

## <a name="fill-out-a-maintenance-checklist"></a>Huollon tarkistusluettelon täyttäminen

1. Valitse **Resurssien hallinta** >  **yhteiset** >  **työtilaukset** >  **Kaikki työtilaukset** tai **Aktiiviset työtilaukset**.

2. Valitse työtilaus ja valitse **Ylläpidon tarkistuslista**.

3. **Työtilauksen ylläpitotöiden tarkistuslista** -kohdassa näkyvät kaikkien työtilaustöiden kunnossapitotarkistusluettelot. Jos työtilaustöillä on erilaiset kunnossapitotyölajit, kunnossapitotarkistusluettelot voivat olla erilaiset jokaisessa työtilaustyössä. Valitse työtilaustyö, jota käytetään liittyvän huollon tarkistusluettelon kanssa. Valitun huollon tarkistusluettelorivin tiedot näkyvät **Rivin tiedot** -pikavälilehdessä.

4. Täytä kaikki huollon tarkistusluettelon rivit yksi kerrallaan järjestyksessä, jossa ne näkyvät. Huollon tarkistusluettelon riviä, jonka tyyppi on "otsikko", käytetään alla olevien kunnossapitoluettelorivien ryhmittelemiseen. Otsikkoa ei tarvitse täyttää, mutta kuten kaikissa huollon tarkistusluettelon rivityypeissä, otsikkoon voidaan lisätä **Huomautus.**

5. Jos ohjeet liittyvät huollon tarkistusluetteloriviin, **Ohjeet**-valintaruutu valitaan. Lue valitun huollon tarkistusluettelorivin ohjeet **Rivin tiedot** -pikavälilehden **Ohjeet**-osassa.

6. Huollon tarkistusluettelon rivin suorittamiseen tarvittavat tiedot voivat vaihdella liittyvän huollon tarkistusluettelotyypin mukaan. Täytät huollon tarkistusluettelorivin täyttämällä **Rivin tiedot** -pikavälilehden kentät. Esimerkiksi rivillä, jonka tyyppi on "Teksti", lisätään **Huomautus**, joka ilmaisee, mikä oli kyseisen tarkistusluettelorivin tulos. Kun rivin tyyppi on "Mittaus", lisäät laitteesta luetun **Laskurin arvo** -arvon ja voit myös lisätä **Huomautus**-kentän, jos se on tarpeen.

- Kun olet täyttänyt huollon tarkistusluettelorivin, merkitse se valmiiksi valitsemalla rivillä oleva **Tarkistettu**-valintaruutu. Jos haluat hylätä huollon tarkistusluettelorivin, koska se ei ole oleellinen työtilauksen työn kannalta, valitse rivin **Ei saatavilla** -valintaruutu. Jos huollon tarkistusluettelon rivi on merkitty arvolla **Pakollinen**, siihen on merkittävä joko "Tarkistettu" tai "Ei saatavilla".  
- Kunnossapitoluettelon rekisteröintejä voi päivittää vain, jos työtilaus on [aktiivisessa](../setup-for-work-orders/work-order-lifecycle-states.md) elinkaaritilassa.  


## <a name="add-a-maintenance-checklist-line"></a>Huollon tarkistusluettelorivin lisääminen

Ylläpitotarkistusluettelot luodaan ylläpitotyön tyypin määrityksestä oletusarvon mukaan ja siirretään työtilaustyöhön. Tarvittaessa voit lisätä kunnossapidon tarkistusluettelorivejä työtilaustyöhön. Manuaalisesti lisätyt huollon tarkistusluettelorivit saavat viitteen "Manuaalinen".

1. Valitse **Työtilauksen ylläpitotöiden tarkistuslista** -kohdassa työtilaustyö, jolle haluat lisätä kunnossapitotarkistusluettelon.

2. Valitse **Ylläpiston tarkistusluettelon rivit** -pikavälilehdessä kunnossapidon tarkistusluettelorivi ja paina näppäimistön nuoli alas -painiketta, jos haluat lisätä uuden rivin valitun huollon tarkistusluettelorivin jälkeen. **Rivinumero**-kentään lisätään automaattisesti järjestyksessä seuraava numero. Voit myös valita huollon tarkistusluettelorivin ja napsauttaa **Lisää rivi** -painiketta, jos haluat lisätä uuden rivin valitun huollon tarkistusluettelorivin yläpuolelle.

3. Kirjoita **Nimi**-kenttään ylläpiton tarkistuslistan rivin nimi.

4. Kirjoita **tyyppi**-kenttään ylläpiton tarkistuslistan rivin tyyppi. Kunkin huollon tarkistusluettelotyyppiin liittyvät kentät näkyvät **Rivin tiedot** -pikavälilehdessä.  
  a. "Teksti"-muodon avulla lisätään huollon tarkistusluettelon rivi, jonka tekstikuvaus kertoo ohjeet. Tätä huollon tarkistusluettelon tyyppiä voidaan käyttää, jos työntekijä haluaa tarkistaa jotain, mutta ei odota tiettyä (mitattavaa) tulosta. Lisää kuvaus siitä, mitä on tehtävä **Rivin tiedot** -pikavälilehden **Ohjeet**-osioon. b. "Otsikko"-muotoa käytetään otsikkona, kun ryhmitellään otsikon alla näkyviä kunnossapidon tarkistusluettelon rivejä. Tästä on hyötyä, jos sinulla on useita huollon tarkistusluettelon rivejä, jotka voidaan jakaa tiettyihin alueisiin. Lisää kuvaava nimi **Nimi** -kenttään.  
  c. "Malli"-muoto ei ole käytettävissä, kun huollon tarkistusluettelorivi lisätään manuaalisesti työtilaustyöhön.  
  d. "Muuttuja"-muodon avulla määritetään mahdollinen tulos huollon tarkistusluettelorivin arvoalueella. Ylläpidon tarkistuslistojen muuttujien määrittäminen on kuvattu kohdassa [Ylläpitotöiden tyyppiluokat ja ylläpitotöiden tyypit, ylläpitotöiden tyyppien variantit, ylläpitotöiden toimialat ja ylläpidon tarkistuslistat](../setup-for-work-orders/job-groups-and-job-types-variants-trades-and-checklists.md). Kirjoita **Nimi**-kenttään muuttujaa kuvaava nimi. Valitse muuttuja **Muuttuja**-kentästä. Lisää kuvaus siitä, mitä on tehtävä **Rivin tiedot** -pikavälilehden **Ohjeet**-osioon.  
  e. "Mittaus"-muotoa käytetään tietyn mittauksen tallentamiseen. Kirjoita **Nimi**-kenttään mittauksen nimi. Valitse **Rivin tiedot** -pikavälilehdessä **Laskuri** ja **Yksikkö**. Lisää kuvaus tehtävistä toimista **Ohjeet**-osaan.  

5. Kun olet lisännyt huollon tarkistusluettelorivit manuaalisesti, täytä rivit edellä kuvatulla tavalla.

>[!NOTE]
>**Työtilauksen ylläpitotöiden tarkistuslista** -kohdassa ei voi poistaa huollon tarkistusluettelon rivejä, joilla on viite "Työlaji". Huollon tarkistusluettelon rivejä voi poistaa vain, kun viite on "Manuaalinen", jonka sinä tai muut kunnossapitotyöntekijät olette luoneet manuaalisesti.


![Kuva 1](media/14-work-orders.png)

