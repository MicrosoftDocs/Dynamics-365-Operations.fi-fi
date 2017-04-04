---
title: Kattavuusasetukset
description: "Pääajoituksessa käytetään kattavuusasetuksia nimiketarpeiden laskemisessa."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: ReqGroup, ReqItemTable, ReqItemTableWizard
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 2494
ms.assetid: 5a95ae4f-ca75-47d9-a1c3-68c97b42f166
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: c1c5654afa6b592e178af052e3e4a7e246a94c9f
ms.lasthandoff: 03/31/2017


---

# <a name="coverage-settings"></a>Kattavuusasetukset

Pääajoituksessa käytetään kattavuusasetuksia nimiketarpeiden laskemisessa. 

Voit määrittää kattavuusasetukset useilla eri tavoilla:

-   Määritä kattavuusryhmän kattavuusasetukset. Voit luoda kattavuusryhmän, joka sisältää kaikkien kattavuusryhmään linkitettyjen tuotteiden asetukset. Valitse **Master planning &gt;asennus &gt;kattavuus &gt;kattavuusryhmiä** voit luoda kattavuusryhmän. Voit linkittää kattavuusryhmän tuotteeseen. Jos linkki koskee tiettyä toimipaikkaa, varastoa tai tuotedimensiota, käytä **Nimikkeen kattavuus** -sivun **Kattavuusryhmä**-kenttää. Jos linkki on yleinen tuotedimensioista riippumatta, käytä **Tuotteen tiedot** -sivulla **Suunnitelma**-pikavälilehdessä olevaa **Kattavuusryhmä**-kenttää. Jos tuotteeseen ei linkitetä kattavuusryhmää, pääsuunnittelu käyttää oletusarvoisesti **Pääsuunnittelun parametrit** -sivulla määritettyä **yleistä kattavuusryhmää**.

-   Määritä tuotteen kattavuusasetukset. Voit luoda tietyn tuotteen kattavuusasetukset. Valitse **tuotetietojen hallinta &gt;tuotteita &gt;vapautetut tuotteet**. Tuotteen, valitse **toimintoruudun**edelleen **suunnitelma** -lehden **kattavuusryhmän**, valitse **nimikkeen kattavuus** Avaa **nimikkeen kattavuus** sivun. Jos tuote on jo linkitetty kattavuusryhmään, voit ohittaa kattavuusryhmän asetukset **Ohita**-kentän avulla. **Nimikkeen kattavuus** -sivun kattavuusasetukset ovat ensisijaisia **Kattavuusryhmä**-sivun asetuksiin nähden.

<!-- -->

-   Määritä tuotteen kattavuusasetukset ohjatulla toiminnolla. Ohjattu toiminto auttaa määrittämään vaiheittain ensisijaisen nimikkeen kattavuusparametrit. Avaa **Ohjattu nimikekattavuustoiminto** napsauttamalla **Nimikkeen kattavuus** -sivulla **Ohjattu toiminto**.

<!-- -->

-   Määritä dimensioryhmän kattavuusasetukset. Valitse **tuotetietojen hallinta &gt;yhteisen &gt;vapautetut tuotteet**. -** Julkaissut tuotteen tiedot ** sivu edelleen **yleisen** -lehden **hallinta** ryhmän, valitse **varastodimensioryhmä** linkki. Valitse **Varastodimensioryhmä** -sivulta **Kattavuussuunnitelma dimension mukaan** -kenttä, jotta voit luoda varastodimensioryhmän dimensiolle kattavuusasetukset. Kaikki tuotedimensiot, kuten kokoonpano, väri, koko, tyyli, on oltava **Kattavuussuunnitelma dimension mukaan** kenttä on valittu.



<a name="see-also"></a>Lisätietoja
--------

[Master plans](master-plans.md)


