---
title: Tuotannonohjauksessa tuotannossa oletusasetukset
description: 
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: JmgProdParameters
audience: Application User
ms.reviewer: annbe
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 70073
ms.assetid: 620944ae-3e20-444a-807e-65495f160904
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: b310e799c1ef0756291c5f7ab886531e4caf1945
ms.lasthandoff: 03/31/2017


---

# <a name="production-order-defaults-in-manufacturing-execution"></a>Tuotannonohjauksessa tuotannossa oletusasetukset



Täytyy miettiä tarkkaan kaikki asetukset **oletusarvo on tuotannon** sivulla ennen työntekijöiden merkinnät tuotantotöistä. Jos yrityksesi käyttää multisite-toimintoa, haluat ehkä määrittää eri oletusarvoja tuotantotilausten jokaiselle sivustolle. Tilausten oletusasetukset tuotannonhallinnan integrointiin asetetaan seuraavilla **Tuotantotilausten oletusarvot** -sivun välilehdillä:

-   **Yleinen** – Yleiset tilauksen oletusarvot tuotantotöille tuotannonohjauksessa.
-   **Aloitus** – Tilauksen oletusarvot, kun tuotantotöitä tai työvaiheita aloitetaan.
-   **Työvaiheet** – Tilauksen oletusasetukset, joita käytetään tuotantotöille tai työvaiheille sekä työvaiheiden palautteessa tuotantoprosessin aikana.
-   **Ilmoita valmiiksi** - Tilauksen oletusarvot, joita käytetään, kun nimikkeitä ilmoitetaan valmiiksi tuotantotilauksen viimeisessä työvaiheessa.
-   **Oikeellisuustarkistus** – Tilauksen oletusarvot, joiden avulla tuotantotilausten aloitus- ja palautemäärien oikeellisuus tarkistetaan.

## <a name="types-of-production-jobs"></a>Tuotannon töiden tyypit
**Työvaiheet** -välilehdessä voit valita tuotantotöiden tyypit, jotka on rekisteröitävä **Työn rekisteröinti** -sivulla. Tavallisesti työntekijät voivat luoda rekisteröintejä asetus- ja prosessitöille. Jos kuitenkin töiden ajoitus on käytössä, voit valita muitakin työtyyppejä, kuten kuljetustöitä, joille työntekijöiden on myös suoritettava rekisteröinti tuotantotilausta käsiteltäessä. **Tärkeää:** Varmista, että kaikki asianmukaiset työlajit ovat valittuina. Muutoin työt eivät välttämättä ole rekisteröitävissä **Työn rekisteröinti** -sivulla. Kohdista valintasi niihin, jotka tehdään **Reititysryhmät**-sivun **Töiden hallinta** -sarakkeessa. Jos **Töiden hallinta** on valittuna reititysryhmälle, työlaji ilmoitetaan valmiiksi tuotantotilauksessa. Tämä ilmoitus tapahtuu, kun työ ilmoitetaan valmiiksi tuotannonhallinnassa. Kun kaikki työlajit, joille **Töiden hallinta** on valittuna ilmoitetaan valmiiksi työvaiheessa, tuotannonhallinta ilmoittaa myös työvaiheen valmiiksi. **Huomautus:** Osan työlajeista voi ilmoittaa manuaalisesti tuotantokirjauskansioita käyttäen. Tässä tapauksessa voit valita **töiden hallinnan** työlajille, mutta jättää työlajin rekisteröinnin valitsematta **Tuotantotilausten oletusarvot** -sivun **Työvaiheet**-välilehdellä.

## <a name="bom-consumption-and-picking-list-journals"></a>Tuoterakenteen kulutuksen ja keräysluettelon kirjauskansiot
Materiaalit voi määrittää niin, että ne kulutetaan joko automaattisesti tai manuaalisesti tuotannossa. Automaattista kulutusta ohjaa tuoterakenteen riveille määritetty materiaaliottosääntö sekä tuotantotilauksen oletusarvojen **Automaattinen tuoterakennekulutus** -kenttä. Automaattisen kulutuksen voi määrittää tapahtumaan tuotantotilauksen alkaessa tai sitä ilmoitettaessa valmiiksi. Kulutus voi vaihtoehtoisesti tapahtua myös työn tasolla sen alkaessa tai valmistuessa.

### <a name="controlling-material-consumption-when-a-production-order-is-started"></a>Materiaalikulutuksen hallinta tuotantotilausta käynnistäessä

Tuotantotilausta käynnistäessä materiaalikulutusta ohjaa **Aloitus**-välilehden **Automaattinen tuoterakennekulutus** -kenttä. Käytettävissä ovat seuraavat arvot:

-   **Materiaaliottosääntö** – Kun tuotantotilaus aloitetaan, materiaaleja kulutetaan tuoterakenteen riveille määritetyn materiaaliottosäännön mukaisesti. Ainoastaan materiaalirivejä, joiden materiaaliottosäännöksi on määritetty **Aloitus** kulutetaan tuotannon alkaessa.
-   **Aina** – Materiaaleja, joiden määrät ovat verrannolliset aloitusmäärään käytetään aina.
-   **Ei koskaan** – Materiaalia ei käytetä missään tapauksessa.

### <a name="controlling-material-consumption-when-a-production-job-is-started-or-completed"></a>Materiaalikulutuksen hallinta tuotantotilauksen alkaessa tai valmistuessa

Tuotannon työn alkaessa tai valmistuessa materiaalikulutusta ohjaa **Työvaiheet**-välilehden **Automaattinen tuoterakennekulutus** -kenttä. Käytettävissä ovat seuraavat arvot:

-   **Materiaaliottosääntö** – Kun tuotantotyön määrä aloitetaan tai kun se valmistuu, materiaaleja kulutetaan tuoterakenteen riveille määritetyn materiaaliottosäännön mukaisesti. Ainoastaan materiaalirivejä, joiden materiaaliottosäännöksi on määritetty **Aloitus** tai **Valmis** kulutetaan.
-   **Aina** – Materiaaleja, joiden määrät ovat verrannolliset työn aloitusmäärään käytetään aina.
-   **Ei koskaan** – Materiaalia ei käytetä missään tapauksessa.

### <a name="controlling-material-consumption-when-a-production-order-is-reported-as-finished"></a>Materiaalikulutuksen hallinta tuotantotilausta ilmoitettaessa valmiiksi

Tuotantotilauksen Ilmoita valmiiksi -prosessissa materiaalikulutusta ohjaa **Ilmoita valmiiksi** -välilehden **Automaattinen tuoterakennekulutus** -kenttä. Käytettävissä ovat seuraavat arvot:

-   **Materiaaliottosääntö** – Kun tuotantotilaus ilmoitetaan valmiiksi, materiaaleja kulutetaan tuoterakenteen riveille määritetyn materiaaliottosäännön mukaisesti. Ainoastaan materiaalirivejä, joiden materiaaliottosäännöksi on määritetty **Valmis** kulutetaan.
-   **Aina** – Materiaaleja, joiden määrät ovat verrannolliset työn valmiiksi ilmoitettuun määrään käytetään aina.
-   **Ei koskaan** – Materiaalia ei käytetä missään tapauksessa.



