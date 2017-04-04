---
title: Maksutapojen tiedostomuodot
description: "Tässä ohjeaiheessa kerrotaan kaksi tapaa hankkia tiedostomuotoja, voit käyttää maksutavat."
author: ShylaThompson
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: CustPaymMode, VendPaymMode
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 262514
ms.assetid: 72ea2018-5a49-419c-93d0-755e5ff2722f
ms.search.region: Belgium, France, Germany, Norway, Spain, Sweden, Switzerland
ms.author: v-lenest
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: f707d45290682e79ee439ba0d504852429defa90
ms.openlocfilehash: 54af22f1f2ec779bf947ae584a3ae09c20e6a364
ms.lasthandoff: 03/31/2017


---

# <a name="file-formats-for-methods-of-payment"></a>Maksutapojen tiedostomuodot

Tässä ohjeaiheessa kerrotaan kaksi tapaa hankkia tiedostomuotoja, voit käyttää maksutavat.

On kaksi tapaa, joiden avulla voit saada tiedostomuodot menetelmien maksun, sähköisen raportoinnin (ER)-tiedostomuodot ja X ++-tiedostomuotojen kanssa käytettäväksi. Kun määrität asiakkaan tai toimittajan maksutapa, ilmaiset tiedostomuodoista ja standardit olisi käytettävä maksujen ja miten maksut tullaan käsittelemään. Voit valita seuraavia muotoja:

-   Vienti
-   Tuonti
-   Palautus
-   Maksusuoritus

### <a name="method-1-electronic-reporting-file-formats"></a>Tapa 1: Sähköisen raportoinnin tiedostomuodot

Tiedostomuotojen, jotka perustuvat konfiguraatiot ER sinun on tuotava konfiguraatiot-Lifecycle Services (LCS). Lisätietoja on ohjeaiheessa [ladata sähköisen raportoinnin Lifecycle Services-kokoonpanojen](/dynamics365/operations/dev-itpro/analytics/download-electronic-reporting-configuration-lcs). Kun tuot raportointipalvelimen konfiguraatiot, jotka tiedostomuodot, tuodut muodot voidaan valita **maksutavat** sivulla. Tuontiin ja valitsemalla tiedostomuodot Euroopassa tapahtuu Japanissa ohjeiden tapaan. <!---For more details, see [Enable the JBA payment file format](https://ax.help.dynamics.com/en/wiki/enable-the-jba-payment-file-format/).-->

### <a name="method-2-x-file-formats"></a>Tapa 2: X ++-tiedostomuodot

Valitse tiedostomuodot, jotka perustuvat X ++-koodia, tee seuraavat toimet.

1.  Siirry **maksutavat** sivulla.
2.  - **Tiedostomuodot** -pikavälilehden Valitse **asetusten**.
3.  Valitse välilehti, joka vastaa tiedoston tiedostotyyppi.
4.  Valitse tiedostomuoto- **käytettävissä** luettelosta ja siirrä se **valittu** luettelon nuolta kontrolliin.
5.  Sulje **Maksutapojen tiedostomuodot** sivulla.
6.  - **Tiedostomuodot** -pikavälilehden maksutavan sopivassa muodossa-kentästä käytettävä tiedostomuoto. Yleisen sähköisen raportoinnin asetukset on asetettava **ei** X ++-tiedostomuotoihin.



