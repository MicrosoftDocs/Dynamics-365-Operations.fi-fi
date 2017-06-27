---
title: Kattavuusasetukset
description: "Pääajoituksessa käytetään kattavuusasetuksia nimiketarpeiden laskemisessa."
author: YuyuScheller
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
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
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: b42f0515823bd42ec260aa1d175855a923162b62
ms.contentlocale: fi-fi
ms.lasthandoff: 05/25/2017


---

# <a name="coverage-settings"></a>Kattavuusasetukset

[!include[banner](../includes/banner.md)]


Pääajoituksessa käytetään kattavuusasetuksia nimiketarpeiden laskemisessa. 

Voit määrittää kattavuusasetukset useilla eri tavoilla:

-   Määritä kattavuusryhmän kattavuusasetukset. Voit luoda kattavuusryhmän, joka sisältää kaikkien kattavuusryhmään linkitettyjen tuotteiden asetukset. Luo kattavuusryhmä valitsemalla **Pääsuunnittelu &gt; Asetukset &gt; Kattavuus &gt; Kattavuusryhmät**. Voit linkittää kattavuusryhmän tuotteeseen. Jos linkki koskee tiettyä toimipaikkaa, varastoa tai tuotedimensiota, käytä **Nimikkeen kattavuus** -sivun **Kattavuusryhmä**-kenttää. Jos linkki on yleinen tuotedimensioista riippumatta, käytä **Tuotteen tiedot** -sivulla **Suunnitelma**-pikavälilehdessä olevaa **Kattavuusryhmä**-kenttää. Jos tuotteeseen ei linkitetä kattavuusryhmää, pääsuunnittelu käyttää oletusarvoisesti **Pääsuunnittelun parametrit** -sivulla määritettyä **yleistä kattavuusryhmää**.

-   Määritä tuotteen kattavuusasetukset. Voit luoda tietyn tuotteen kattavuusasetukset. Valitse **Tuotetietojen hallinta &gt; Tuotteet &gt; Vapautetut tuotteet**. Valitse tuote ja napsauta **toimintoruudussa** **Suunnitelma**-välilehden **Kattavuusryhmä**-kohdassa **Nimikkeen kattavuus**. Näkyviin tulee **Nimikkeen kattavuus** -sivu. Jos tuote on jo linkitetty kattavuusryhmään, voit ohittaa kattavuusryhmän asetukset **Ohita**-kentän avulla. **Nimikkeen kattavuus** -sivun kattavuusasetukset ovat ensisijaisia **Kattavuusryhmä**-sivun asetuksiin nähden.

<!-- -->

-   Määritä tuotteen kattavuusasetukset ohjatulla toiminnolla. Ohjattu toiminto auttaa määrittämään vaiheittain ensisijaisen nimikkeen kattavuusparametrit. Avaa **Ohjattu nimikekattavuustoiminto** napsauttamalla **Nimikkeen kattavuus** -sivulla **Ohjattu toiminto**.

<!-- -->

-   Määritä dimensioryhmän kattavuusasetukset. Valitse **Tuotetietojen hallinta &gt; Yleinen &gt; Vapautetut tuotteet**. Napsauta **Vapautetun tuotteen tiedot** -sivulla **Yleiset**-välilehden **Hallinta**-ryhmässä **Varastodimensioryhmä**-linkkiä. Valitse **Varastodimensioryhmä** -sivulta **Kattavuussuunnitelma dimension mukaan** -kenttä, jotta voit luoda varastodimensioryhmän dimensiolle kattavuusasetukset. **Kattavuussuunnitelma dimension mukaan** -kentän on oltava valittuna kaikissa tuotedimensioissa, kuten konfiguraatiossa, värissä, koossa ja tyylissä.



<a name="see-also"></a>Lisätietoja
--------

[Pääsuunnitelmat](master-plans.md)




