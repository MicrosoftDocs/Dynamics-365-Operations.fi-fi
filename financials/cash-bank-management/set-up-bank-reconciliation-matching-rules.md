---
title: "Aseta pankkitilin täsmäytyksen yhteensopivuussäännöt"
description: "Tässä artikkelissa kerrotaan, miten määritetään täsmäytyssäännöt ja täsmäytyksen sääntöjoukot, jotka helpottavat pankkitilin täsmäytysprosessia. Täsmäytyssäännöt ovat ehtojoukko, joilla suodatetaan tiliotteen ja pankkitositteen rivejä täsmäytysprosessin aikana."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: BankReconciliationMatchRule, BankReconciliationMatchRuleSet
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 12971
ms.assetid: b5073f83-31dc-404f-af42-3fd84a02a7c6
ms.search.region: Global
ms.author: leguo
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 3b16ef53f9fb57a6663db0be1f7e0a57471db2fb
ms.openlocfilehash: e4c07a6afb90535c57f372d5b850919b5b34aaa4
ms.lasthandoff: 03/31/2017


---

# <a name="set-up-bank-reconciliation-matching-rules"></a>Aseta pankkitilin täsmäytyksen yhteensopivuussäännöt

Tässä artikkelissa kerrotaan, miten määritetään täsmäytyssäännöt ja täsmäytyksen sääntöjoukot, jotka helpottavat pankkitilin täsmäytysprosessia. Täsmäytyssäännöt ovat ehtojoukko, joilla suodatetaan tiliotteen ja pankkitositteen rivejä täsmäytysprosessin aikana.

Voit määrittää täsmäytyssäännöt ja täsmäytyksen sääntöjoukot, jotka helpottavat pankkitilin täsmäytysprosessia. Vastaavia poistosäännön on joukko ehtoja, joiden avulla haluat suodattaa tiliotteen rivit ja Microsoft Dynamics-365 pankin toimintojen tapahtumarivit täsmäytysprosessin aikana. Voit määrittää täsmäytyssäännön **Täsmäytyssäännöt**-sivulla. Täsmäytyssääntöjä voi määrittää useita. Tämän jälkeen luodaan täsmäytyssääntö **Täsmäytyksen sääntöjoukot** -sivulla. 

> [!NOTE] 
> Täsmäytys pankin sääntöjä käytetään, jos sähköinen tiliote täsmäytetään käyttämällä advance pankkitäsmäytyksen. 

**Täsmäytyssäännöt**-sivulla voit määrittää, mitä toimintoja ja valintaperusteita käytetään täsmäytyssääntöä suoritettaessa. - **Toimintojen** kenttäryhmässä, valitse toiminto, jonka ohjelma suorittaa, kun vastaavia sääntö suoritetaan täsmäytysprosessin aikana.  

> [!NOTE] 
> Valinta, jonka määrittää kentät, jotka näkyvät.

|                                    |                                                                                                                                                                                                                                                                                                               |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Toiminto**                         |                                                                                                                                                                                                                                                                                                               | **Toiminnon valitsemin jälkeen käytettävissä olevat valintaperusteet**                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| **Täsmäytä pankkitositteen kanssa **       | Luo ehdot, joilla voit määrittää, miten pankkitosite- ja tilioterivit täsmäytetään, kun täsmäytyssääntö suoritetaan **Pankkitilin täsmäytyksen laskentataulukko** -sivun avulla. Tapahtumarivit valitaan pikavälilehdissä määritettyjen lisäehtojen mukaan.                                | **Vaihe 1: Määritä vastaavaa sääntöä** – Valitse määrittääksesi, mitkä tiliotteiden Dynamics 365 tulisi vastata toimien pankkitapahtumien criterias. **Vaihe 2 (valinnainen): valitse tiliotteen rivit, joiden kanssa täsmäytyssäännöt suoritetaan:** Ota käyttöön sen tiliotteen rivin suodatin, jonka kanssa sääntö suoritetaan.                                                                                                                                                                                                                                                                                                               |
| **Tyhjennä palautuslaskelman rivit ** | Luo ehdot, joilla määritetään, miten palautuslaskelmat rivit olisi poistettava **Pankkitilin täsmäytyksen laskentataulukko** -sivulta, kun täsmäytyssääntö suoritetaan. Tätä vaihtoehtoa käytetään, kun tuodussa tiliotteessa on pankin virheen vuoksi kaksi tilioteriviä ja rivit on täsmäytettävä. | **Vaihe 1**:** etsi palautuslaskelman rivit **– Lisää valintaperusteet, joilla valitaan tiliotteen palautuslaskelman rivit. Esimerkiksi vain sekit voidaan valita valitsemalla Kenttä-kentässä **Pankkitapahtuman koodi**, valitsemalla sitten **Operaattori**-kentässä plus-merkki (+) ja syöttämällä Arvo-kenttään **Sekit**. **Vaihe 2: etsi alkuperäisen tiliotteen rivit** – Voit lisätä valintaperusteet, joilla pankkitositteen rivit täsmäytetään tiliotteen riveihin. ** Vaihe 3: Etsi Dynamics 365 pankin toimintojen ** – voit lisätä vastaamaan Operations pankkitapahtumien tiliotteen rivit Dynamics 365 valintaperusteet. |
| **Mark new transactions**          | Luo ehdot, joilla määritetään, miten uudet tapahtumat merkitään **Pankkitilin täsmäytyksen laskentataulukko** -sivulla, kun täsmäytyssääntö suoritetaan.                                                                                                                                                                 | **Step 1: etsi tiliotteen rivit **– Lisää valintakentät ja määritä, mitkä tiliotteen rivit **Pankkitilin täsmäytyksen laskentataulukko** -sivulla valitaan. ** Vaihe 2: Etsi Dynamics 365 toimintojen pankkitapahtumien ** – voit lisätä etsimään pankin asiakirjariveillä valintaperusteet. Jos pankkitositetta ei löydy, tiliotteen rivi merkitään uudeksi tapahtumaksi.                                                                                                                                                                                                                                             |

 





