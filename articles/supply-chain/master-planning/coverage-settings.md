---
title: Kattavuusasetukset
description: Tässä ohjeaiheessa on tietoja kattavuusasetuksista, joita pääajoitus käyttää nimiketarpeiden laskennassa.
author: roxanadiaconu
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqGroup, ReqItemTable, ReqItemTableWizard
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 2494
ms.assetid: 5a95ae4f-ca75-47d9-a1c3-68c97b42f166
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 99e094a7131b6d3a299fc72abd0141529908ddd2
ms.sourcegitcommit: 9e50bee6a67f0fe2fa6f86e02c7e8de16d0e2482
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/08/2019
ms.locfileid: "1538891"
---
# <a name="coverage-settings"></a>Kattavuusasetukset

[!include [banner](../includes/banner.md)]

Pääajoituksessa käytetään kattavuusasetuksia nimiketarpeiden laskemisessa.

Voit määrittää kattavuusasetukset useilla eri tavoilla:

- Määritä kattavuusryhmän kattavuusasetukset.

    Voit luoda kattavuusryhmän, joka sisältää kaikkien kattavuusryhmään linkitettyjen tuotteiden asetukset. Luodaksesi kattavuusryhmän, valitse **Pääsuunnittelu &gt; Asetukset &gt; Kattavuus &gt; Kattavuusryhmät**. Voit linkittää kattavuusryhmän tuotteeseen. Jos linkki koskee tiettyä toimipaikkaa, varastoa tai tuotedimensiota, käytä **Nimikkeen kattavuus** -sivun **Kattavuusryhmä**-kenttää. Jos linkki on yleinen tuotedimensioista riippumatta, käytä **Tuotteen tiedot** -sivulla **Suunnitelma**-pikavälilehden **Kattavuusryhmä**-kenttää. Oletusarvoisesti, jos tuotteeseen ei linkitetä kattavuusryhmää, pääsuunnittelu käyttää oletusarvoisesti **Pääsuunnittelun parametrit** -sivulla määritettyä yleistä kattavuusryhmää.

- Määritä tuotteen kattavuusasetukset.

    Voit luoda tietyn tuotteen kattavuusasetukset. Mene **Tuotetietojen hallinta &gt; Tuotteet &gt; Vapautetut tuotteet**. Valitse tuote ja napsauta toimintoruudussa **Suunnitelma**-välilehden **Kattavuusryhmä**-kohdassa **Nimikkeen kattavuus**. Näkyviin tulee **Nimikkeen kattavuus** -sivu. Jos tuote on jo linkitetty kattavuusryhmään, voit ohittaa kattavuusryhmän asetukset **Ohita**-kentän avulla. **Nimikkeen kattavuus** -sivun kattavuusasetukset ovat ensisijaisia **Kattavuusryhmä**-sivun asetuksiin nähden.

- Määritä tuotteen kattavuusasetukset ohjatulla toiminnolla.

    Ohjattu toiminto opastaa vaiheittain ensisijaisen nimikkeen kattavuusparametrien määrittämisessä. Avaa **Ohjattu nimikekattavuustoiminto** napsauttamalla **Nimikkeen kattavuus** -sivulla toimintoruudusta **Ohjattu toiminto**.

- Määritä dimensioryhmän kattavuusasetukset.

    Mene **Tuotetietojen hallinta &gt; Tuotteet &gt; Vapautetut tuotteet**. Napsauta **Vapautetun tuotteen tiedot** -sivulla **Yleiset**-pikavälilehden **Hallinta**-osassa **Varastodimensioryhmä**-linkkiä. Valitse **Varastodimensioryhmät** -sivulta **Kattavuussuunnitelma dimension mukaan** -valintaruutu, jotta voit luoda varastodimensioryhmän dimensiolle kattavuusasetukset. **Kattavuussuunnitelma dimension mukaan** -kentän on oltava valittuna kaikissa tuotedimensioissa, kuten konfiguraatiossa, värissä, koossa ja tyylissä.

## <a name="additional-resources"></a>Lisäresurssit

[Pääsuunnitelmat](master-plans.md)
