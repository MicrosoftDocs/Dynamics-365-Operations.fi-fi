---
title: Pankkitilin täsmäytyksen täsmäytyssääntöjen asetukset
description: Tässä ohjeaiheessa kerrotaan, miten määritetään täsmäytyssäännöt ja täsmäytyksen sääntöjoukot, jotka helpottavat pankkitilin täsmäytysprosessia. Täsmäytyssäännöt ovat ehtojoukko, joilla suodatetaan tiliotteen ja pankkitositteen rivejä täsmäytysprosessin aikana.
author: panolte
manager: AnnBe
ms.date: 08/24/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BankReconciliationMatchRule, BankReconciliationMatchRuleSet
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 12971
ms.assetid: b5073f83-31dc-404f-af42-3fd84a02a7c6
ms.search.region: Global
ms.author: panolte
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3302738a05852dfb37f8266074386d9f2998994d
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/13/2020
ms.locfileid: "4442768"
---
# <a name="set-up-bank-reconciliation-matching-rules"></a>Pankkitilin täsmäytyksen täsmäytyssääntöjen asetukset

[!include [banner](../includes/banner.md)]

Tässä ohjeaiheessa kerrotaan, miten määritetään täsmäytyssäännöt ja täsmäytyksen sääntöjoukot, jotka helpottavat pankkitilin täsmäytysprosessia. Täsmäytyssäännöt ovat ehtojoukko, joilla suodatetaan tiliotteen ja pankkitositteen rivejä täsmäytysprosessin aikana.

Voit määrittää täsmäytyssäännöt ja täsmäytyksen sääntöjoukot, jotka helpottavat pankkitilin täsmäytysprosessia. Täsmäytyssääntö on ehtojoukko, joilla suodatetaan tiliotteen rivejä ja Dynamics 365 Financein pankkitapahtuman rivejä täsmäytysprosessin aikana. Voit määrittää täsmäytyssäännön **Täsmäytyssäännöt**-sivulla. Täsmäytyssääntöjä voi määrittää useita. Tämän jälkeen luodaan täsmäytyssääntö **Täsmäytyksen sääntöjoukot** -sivulla. 

> [!NOTE] 
> Pankkitilin täsmäytyssääntöjä käytetään, jos sähköisen tiliotteen täsmäytys tehdään pankkitilin täsmäytyksen lisätoimintojen avulla. 

**Täsmäytyssäännöt**-sivulla voit määrittää, mitä toimintoja ja valintaperusteita käytetään täsmäytyssääntöä suoritettaessa. Valitse **Toiminnot**-ryhmässä toiminto, joka suoritetaan , kun täsmäytyssääntö suoritetaan täsmäytysprosessin aikana.  

Täsmäytyssäännöt täsmäyttävät oletusarvoisesti ensimmäisen pankkiasiakirjan, joka vastaa täsmäytyssäännön ehtoja. Jos moni pankkiasiakirja vastaa säännön ehtoja, manuaalista täsmäytystä edellyttävä parametri voidaan ottaa käyttöön valitsemalla **Maksuliikenteen hallinta > Asetukset > Maksuliikennetiedot > Pankkitilin täsmäytys > Edellytä manuaalista täsmäyttämistä, kun pankkitilin täsmäytyksen lisätoimintojen täsmäytyssäännöt löytävät useita summaa vastaavia asiakirjoja**.

> [!NOTE] 
> Valintasi määrittää näkyviin tulevat kentät.

|                                    |                                                                                                                                                                                                                                                                                                               |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Toiminto**                         |                                                                                                                                                                                                                                                                                                               | **Toiminnon valitsemin jälkeen käytettävissä olevat valintaperusteet**                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| **Täsmäytä pankkitositteen kanssa**       | Luo ehdot, joilla voit määrittää, miten pankkitosite- ja tilioterivit täsmäytetään, kun täsmäytyssääntö suoritetaan **Pankkitilin täsmäytyksen laskentataulukko** -sivun avulla. Tapahtumarivit valitaan pikavälilehdissä määritettyjen lisäehtojen mukaan.                                | **Vaihe 1: määritä täsmäytyssääntö** – Valitse ehdot, jotka määrittävät, mitkä tiliotteet ja Financen pankkitapahtumat täsmäytetään. **Vaihe 2 (valinnainen): valitse tiliotteen rivit, joiden kanssa täsmäytyssäännöt suoritetaan:** Ota käyttöön sen tiliotteen rivin suodatin, jonka kanssa sääntö suoritetaan.                                                                                                                                                                                                                                                                                                               |
| **Tyhjennä palautuslaskelman rivit** | Luo ehdot, joilla määritetään, miten palautuslaskelmat rivit olisi poistettava **Pankkitilin täsmäytyksen laskentataulukko** -sivulta, kun täsmäytyssääntö suoritetaan. Tätä vaihtoehtoa käytetään, kun tuodussa tiliotteessa on pankin virheen vuoksi kaksi tilioteriviä ja rivit on täsmäytettävä. | **Vaihe 1**:**etsi palautuslaskelman rivit**– Lisää valintaperusteet, joilla valitaan tiliotteen palautuslaskelman rivit. Esimerkiksi vain sekit voidaan valita valitsemalla Kenttä-kentässä **Pankkitapahtuman koodi**, valitsemalla sitten **Operaattori**-kentässä plus-merkki (+) ja syöttämällä Arvo-kenttään **Sekit**. **Vaihe 2: etsi alkuperäisen tiliotteen rivit** – Voit lisätä valintaperusteet, joilla pankkitositteen rivit täsmäytetään tiliotteen riveihin. **Vaihe 3: etsi Finance-pankkitapahtumat** – Voit lisätä valintaperusteet, joilla Financen pankkitapahtumat täsmäytetään tiliotteen riveihin. |
| **Merkitse uusia tapahtumia**          | Luo ehdot, joilla määritetään, miten uudet tapahtumat merkitään **Pankkitilin täsmäytyksen laskentataulukko** -sivulla, kun täsmäytyssääntö suoritetaan.                                                                                                                                                                 | **Step 1: etsi tiliotteen rivit**– Lisää valintakentät ja määritä, mitkä tiliotteen rivit **Pankkitilin täsmäytyksen laskentataulukko** -sivulla valitaan. **Vaihe 2: Etsi Finance and Operations** – Voit lisätä valintaperusteet, joiden avulla haetaan pankkitositteiden rivejä. Jos pankkitositetta ei löydy, tiliotteen rivi merkitään uudeksi tapahtumaksi.                                                                                                                                                                                                                                             |
