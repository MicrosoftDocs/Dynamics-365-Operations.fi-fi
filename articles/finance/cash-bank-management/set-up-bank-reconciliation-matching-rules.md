---
title: Pankkitilin täsmäytyksen täsmäytyssääntöjen asetukset
description: Tässä artikkelissa kerrotaan, miten määritetään täsmäytyssäännöt ja täsmäytyksen sääntöjoukot, jotka helpottavat pankkitilin täsmäytysprosessia. Täsmäytyssäännöt ovat ehtojoukko, joilla suodatetaan tiliotteen ja pankkitositteen rivejä täsmäytysprosessin aikana.
author: angelad116
ms.date: 11/22/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BankReconciliationMatchRule, BankReconciliationMatchRuleSet
audience: Application User
ms.reviewer: kfend
ms.custom: 12971
ms.assetid: b5073f83-31dc-404f-af42-3fd84a02a7c6
ms.search.region: Global
ms.author: angelading
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ac5ab5e2bcb9a63bb52d5a74bd5e4b5db51ba603
ms.sourcegitcommit: 81bb8e51951395be3f18f45212e47e6c41656f6a
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/23/2022
ms.locfileid: "9803934"
---
# <a name="set-up-bank-reconciliation-matching-rules"></a>Pankkitilin täsmäytyksen täsmäytyssääntöjen asetukset

[!include [banner](../includes/banner.md)]

Tässä artikkelissa kerrotaan, miten määritetään täsmäytyssäännöt ja täsmäytyksen sääntöjoukot, jotka helpottavat pankkitilin täsmäytysprosessia. Täsmäytyssäännöt ovat ehtojoukko, joilla suodatetaan tiliotteen ja pankkitositteen rivejä täsmäytysprosessin aikana.

Voit määrittää täsmäytyssäännöt ja täsmäytyksen sääntöjoukot, jotka helpottavat pankkitilin täsmäytysprosessia. Täsmäytyssääntö on ehtojoukko, joilla suodatetaan tiliotteen rivejä ja Dynamics 365 Financen pankkitapahtuman rivejä täsmäytysprosessin aikana. Voit määrittää täsmäytyssäännön **Täsmäytyssäännöt**-sivulla. Täsmäytyssääntöjä voi määrittää useita. Tämän jälkeen luodaan täsmäytyssääntö **Täsmäytyksen sääntöjoukot** -sivulla. 

> [!NOTE] 
> Pankkitilin täsmäytyssääntöjä käytetään, jos sähköisen tiliotteen täsmäytys tehdään pankkitilin täsmäytyksen lisätoimintojen avulla. 

**Täsmäytyssäännöt**-sivulla voit määrittää, mitä toimintoja ja valintaperusteita käytetään täsmäytyssääntöä suoritettaessa. Valitse **Toiminnot**-ryhmässä toiminto, joka suoritetaan , kun täsmäytyssääntö suoritetaan täsmäytysprosessin aikana.  

Täsmäytyssäännöt täsmäyttävät oletusarvoisesti ensimmäisen pankkiasiakirjan, joka vastaa täsmäytyssäännön ehtoja. Jos moni pankkiasiakirja vastaa säännön ehtoja, manuaalista täsmäytystä edellyttävä parametri voidaan ottaa käyttöön valitsemalla **Maksuliikenteen hallinta > Asetukset > Maksuliikennetiedot > Pankkitilin täsmäytys > Edellytä manuaalista täsmäyttämistä, kun pankkitilin täsmäytyksen lisätoimintojen täsmäytyssäännöt löytävät useita summaa vastaavia asiakirjoja**.

> [!NOTE] 
> Valintasi määrittää näkyviin tulevat kentät.

| Toimenpide | kuvaus   | Toiminnon valitsemin jälkeen käytettävissä olevat valintaperusteet     |
|--------|---------------|----------------------------------------------------------|
| **Täsmäytä pankkitositteen kanssa**       | Luo ehdot, joilla voit määrittää, miten pankkitosite- ja tilioterivit täsmäytetään, kun täsmäytyssääntö suoritetaan **Pankkitilin täsmäytyksen laskentataulukko** -sivun avulla. Tapahtumarivit valitaan pikavälilehdissä määritettyjen lisäehtojen mukaan. | <ul><li>**Vaihe 1: määritä täsmäytyssääntö** – Valitse ehdot, jotka määrittävät, mitkä tiliotteet ja Financen pankkitapahtumat täsmäytetään.</li><li> **Vaihe 2 (valinnainen): valitse tiliotteen rivit, joiden kanssa täsmäytyssäännöt suoritetaan:** Ota käyttöön sen tiliotteen rivin suodatin, jonka kanssa sääntö suoritetaan.</li></ul>                                       |
| **Tyhjennä palautuslaskelman rivit** | Luo ehdot, joilla määritetään, miten palautuslaskelmat rivit olisi poistettava **Pankkitilin täsmäytyksen laskentataulukko** -sivulta, kun täsmäytyssääntö suoritetaan. Tätä vaihtoehtoa käytetään, kun tuodussa tiliotteessa on pankin virheen vuoksi kaksi tilioteriviä ja rivit on täsmäytettävä. |<ul><li> **Vaihe 1**:**etsi palautuslaskelman rivit**– Lisää valintaperusteet, joilla valitaan tiliotteen palautuslaskelman rivit. Esimerkiksi vain sekit voidaan valita valitsemalla **Kenttä**-kentässä **Pankkitapahtuman koodi**, valitsemalla sitten **Operaattori**-kentässä plus-merkki (+) ja syöttämällä **Arvo**-kenttään **Sekit**. </li><li>**Vaihe 2: etsi alkuperäisen tiliotteen rivit** – Voit lisätä valintaperusteet, joilla pankkitositteen rivit täsmäytetään tiliotteen riveihin. </li><li>**Vaihe 3: etsi Finance-pankkitapahtumat** – Voit lisätä valintaperusteet, joilla Financen pankkitapahtumat täsmäytetään tiliotteen riveihin.</li></ul>  |
| **Merkitse uusia tapahtumia**          | Luo ehdot, joilla määritetään, miten uudet tapahtumat merkitään **Pankkitilin täsmäytyksen laskentataulukko** -sivulla, kun täsmäytyssääntö suoritetaan.                                                                                                                                                                 | <ul><li>**Step 1: etsi tiliotteen rivit**– Lisää valintakentät ja määritä, mitkä tiliotteen rivit **Pankkitilin täsmäytyksen laskentataulukko** -sivulla valitaan.</li><li> **Vaihe 2: etsi talous- ja toimintosovellukset** – Voit lisätä valintaperusteet, joiden avulla haetaan pankkitositteiden rivejä. Jos pankkitositetta ei löydy, tiliotteen rivi merkitään uudeksi tapahtumaksi. </li></ul>         |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]

