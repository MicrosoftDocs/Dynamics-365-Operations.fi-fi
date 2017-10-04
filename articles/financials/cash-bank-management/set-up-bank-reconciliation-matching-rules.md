---
title: "Aseta pankkitilin täsmäytyksen yhteensopivuussäännöt"
description: "Tässä artikkelissa kerrotaan, miten määritetään täsmäytyssäännöt ja täsmäytyksen sääntöjoukot, jotka helpottavat pankkitilin täsmäytysprosessia. Täsmäytyssäännöt ovat ehtojoukko, joilla suodatetaan tiliotteen ja pankkitositteen rivejä täsmäytysprosessin aikana."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: BankReconciliationMatchRule, BankReconciliationMatchRuleSet
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 12971
ms.assetid: b5073f83-31dc-404f-af42-3fd84a02a7c6
ms.search.region: Global
ms.author: leguo
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 869151f2486b7a481e4694cfb6992d0ee2cfc008
ms.openlocfilehash: 60cd6a7f7b4d5c3acc68aa27c920f42f1d4b910e
ms.contentlocale: fi-fi
ms.lasthandoff: 06/13/2017


---

# <a name="set-up-bank-reconciliation-matching-rules"></a>Aseta pankkitilin täsmäytyksen yhteensopivuussäännöt

[!include[banner](../includes/banner.md)]


Tässä artikkelissa kerrotaan, miten määritetään täsmäytyssäännöt ja täsmäytyksen sääntöjoukot, jotka helpottavat pankkitilin täsmäytysprosessia. Täsmäytyssäännöt ovat ehtojoukko, joilla suodatetaan tiliotteen ja pankkitositteen rivejä täsmäytysprosessin aikana.

Voit määrittää täsmäytyssäännöt ja täsmäytyksen sääntöjoukot, jotka helpottavat pankkitilin täsmäytysprosessia. Täsmäytyssääntö on ehtojoukko, jonka avulla tiliotteen ja Microsoft Dynamics 365 for Finance and Operations, Enterprise Editionin pankkitapahtuman rivejä suodatetaan täsmäytysprosessin aikana. Voit määrittää täsmäytyssäännön **Täsmäytyssäännöt**-sivulla. Täsmäytyssääntöjä voi määrittää useita. Tämän jälkeen luodaan täsmäytyssääntö **Täsmäytyksen sääntöjoukot** -sivulla. 

> [!NOTE] 
> Pankkitilin täsmäytyssääntöjä käytetään, jos sähköisen tiliotteen täsmäytys tehdään pankkitilin täsmäytyksen lisätoimintojen avulla. 

**Täsmäytyssäännöt**-sivulla voit määrittää, mitä toimintoja ja valintaperusteita käytetään täsmäytyssääntöä suoritettaessa. Valitse **Toiminnot**-ryhmässä toiminto, joka suoritetaan , kun täsmäytyssääntö suoritetaan täsmäytysprosessin aikana.  

> [!NOTE] 
> Valintasi määrittää näkyviin tulevat kentät.

|                                    |                                                                                                                                                                                                                                                                                                               |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Toiminto**                         |                                                                                                                                                                                                                                                                                                               | **Toiminnon valitsemin jälkeen käytettävissä olevat valintaperusteet**                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| **Täsmäytä pankkitositteen kanssa**       | Luo ehdot, joilla voit määrittää, miten pankkitosite- ja tilioterivit täsmäytetään, kun täsmäytyssääntö suoritetaan **Pankkitilin täsmäytyksen laskentataulukko** -sivun avulla. Tapahtumarivit valitaan pikavälilehdissä määritettyjen lisäehtojen mukaan.                                | **Vaihe 1: Määritä täsmäytyssääntö** – Valitse ehdot, jotka määrittävät, mitkä tiliotteet ja Finance and Operationsin pankkitapahtumat täsmäytetään. **Vaihe 2 (valinnainen): valitse tiliotteen rivit, joiden kanssa täsmäytyssäännöt suoritetaan:** Ota käyttöön sen tiliotteen rivin suodatin, jonka kanssa sääntö suoritetaan.                                                                                                                                                                                                                                                                                                               |
| **Tyhjennä palautuslaskelman rivit** | Luo ehdot, joilla määritetään, miten palautuslaskelmat rivit olisi poistettava **Pankkitilin täsmäytyksen laskentataulukko** -sivulta, kun täsmäytyssääntö suoritetaan. Tätä vaihtoehtoa käytetään, kun tuodussa tiliotteessa on pankin virheen vuoksi kaksi tilioteriviä ja rivit on täsmäytettävä. | **Vaihe 1**:**etsi palautuslaskelman rivit**– Lisää valintaperusteet, joilla valitaan tiliotteen palautuslaskelman rivit. Esimerkiksi vain sekit voidaan valita valitsemalla Kenttä-kentässä **Pankkitapahtuman koodi**, valitsemalla sitten **Operaattori**-kentässä plus-merkki (+) ja syöttämällä Arvo-kenttään **Sekit**. **Vaihe 2: etsi alkuperäisen tiliotteen rivit** – Voit lisätä valintaperusteet, joilla pankkitositteen rivit täsmäytetään tiliotteen riveihin. **Vaihe 3: etsi Finance and Operations -pankkitapahtumat **– Voit lisätä valintaperusteet, joilla Dynamics 365 for Finance and Operationsin pankkitapahtumat täsmäytetään tiliotteen riveihin. |
| **Merkitse uusia tapahtumia**          | Luo ehdot, joilla määritetään, miten uudet tapahtumat merkitään **Pankkitilin täsmäytyksen laskentataulukko** -sivulla, kun täsmäytyssääntö suoritetaan.                                                                                                                                                                 | **Step 1: etsi tiliotteen rivit**– Lisää valintakentät ja määritä, mitkä tiliotteen rivit **Pankkitilin täsmäytyksen laskentataulukko** -sivulla valitaan. **Vaihe 2: etsi Finance and Operations **– Voit lisätä valintaperusteet, joiden avulla haetaan pankkitositteiden rivejä. Jos pankkitositetta ei löydy, tiliotteen rivi merkitään uudeksi tapahtumaksi.                                                                                                                                                                                                                                             |

 






