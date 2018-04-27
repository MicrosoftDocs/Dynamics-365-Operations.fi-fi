---
title: Kattavuusasetukset
description: "Pääajoituksessa käytetään kattavuusasetuksia nimiketarpeiden laskemisessa."
author: roxanadiaconu
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ReqGroup, ReqItemTable, ReqItemTableWizard
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 2494
ms.assetid: 5a95ae4f-ca75-47d9-a1c3-68c97b42f166
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 591b1cd739bb3be61299f33f180ca7c264d21a35
ms.contentlocale: fi-fi
ms.lasthandoff: 04/13/2018

---

# <a name="coverage-settings"></a>Kattavuusasetukset

[!INCLUDE [banner](../includes/banner.md)]

Pääajoituksessa käytetään kattavuusasetuksia nimiketarpeiden laskemisessa. 

Voit määrittää kattavuusasetukset useilla eri tavoilla:

-   Määritä kattavuusryhmän kattavuusasetukset. Voit luoda kattavuusryhmän, joka sisältää kaikkien kattavuusryhmään linkitettyjen tuotteiden asetukset. Luo kattavuusryhmä valitsemalla **Pääsuunnittelu &gt; Asetukset &gt; Kattavuus &gt; Kattavuusryhmät**. Voit linkittää kattavuusryhmän tuotteeseen. Jos linkki koskee tiettyä toimipaikkaa, varastoa tai tuotedimensiota, käytä **Nimikkeen kattavuus** -sivun **Kattavuusryhmä**-kenttää. Jos linkki on yleinen tuotedimensioista riippumatta, käytä **Tuotteen tiedot** -sivulla **Suunnitelma**-pikavälilehdessä olevaa **Kattavuusryhmä**-kenttää. Jos tuotteeseen ei linkitetä kattavuusryhmää, pääsuunnittelu käyttää oletusarvoisesti **Pääsuunnittelun parametrit** -sivulla määritettyä **yleistä kattavuusryhmää**.

-   Määritä tuotteen kattavuusasetukset. Voit luoda tietyn tuotteen kattavuusasetukset. Valitse **Tuotetietojen hallinta &gt; Tuotteet &gt; Vapautetut tuotteet**. Valitse tuote ja napsauta **toimintoruudussa** **Suunnitelma**-välilehden **Kattavuusryhmä**-kohdassa **Nimikkeen kattavuus**. Näkyviin tulee **Nimikkeen kattavuus** -sivu. Jos tuote on jo linkitetty kattavuusryhmään, voit ohittaa kattavuusryhmän asetukset **Ohita**-kentän avulla. **Nimikkeen kattavuus** -sivun kattavuusasetukset ovat ensisijaisia **Kattavuusryhmä**-sivun asetuksiin nähden.

<!-- -->

-   Määritä tuotteen kattavuusasetukset ohjatulla toiminnolla. Ohjattu toiminto auttaa määrittämään vaiheittain ensisijaisen nimikkeen kattavuusparametrit. Avaa **Ohjattu nimikekattavuustoiminto** napsauttamalla **Nimikkeen kattavuus** -sivulla **Ohjattu toiminto**.

<!-- -->

- Määritä dimensioryhmän kattavuusasetukset. Valitse <strong>Tuotetietojen hallinta &gt; Yleinen &gt; Vapautetut tuotteet</strong>. Napsauta <strong>Vapautetun tuotteen tiedot **-sivulla **Yleiset</strong>-välilehden <strong>Hallinta</strong>-ryhmässä <strong>Varastodimensioryhmä</strong>-linkkiä. Valitse <strong>Varastodimensioryhmä</strong> -sivulta <strong>Kattavuussuunnitelma dimension mukaan</strong> -kenttä, jotta voit luoda varastodimensioryhmän dimensiolle kattavuusasetukset. <strong>Kattavuussuunnitelma dimension mukaan</strong> -kentän on oltava valittuna kaikissa tuotedimensioissa, kuten konfiguraatiossa, värissä, koossa ja tyylissä.



<a name="see-also"></a>Lisätietoja
--------

[Pääsuunnitelmat](master-plans.md)




