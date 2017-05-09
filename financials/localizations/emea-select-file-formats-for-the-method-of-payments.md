---
title: Maksutapojen tiedostomuodot
description: "Tässä ohjeaiheessa kerrotaan kaksi tapaa hankkia tiedostomuotoja, joita voit käyttää maksutavoissa."
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

[!include[banner](../includes/banner.md)]


Tässä ohjeaiheessa kerrotaan kaksi tapaa hankkia tiedostomuotoja, joita voit käyttää maksutavoissa.

On kaksi tapaa, joiden avulla voit saada tiedostomuodot maksutapoihin: sähköisen raportoinnin (ER) tiedostomuodot ja X ++ -tiedostomuodot. Kun määrität asiakkaan tai toimittajan maksutavan, ilmaiset, mitä tiedostomuotoja ja standardeja olisi käytettävä maksuille ja miten maksut tullaan käsittelemään. Valittavissa ovat seuraavat tyypit tai muodot:

-   Vienti
-   Tuonti
-   Palautus
-   Maksusuoritus

### <a name="method-1-electronic-reporting-file-formats"></a>Tapa 1: Sähköisen raportoinnin (ER) tiedostomuodot

Tiedostomuodoille, jotka perustuvat ER-konfiguraatioihin, sinun on tuotava konfiguraatiot Lifecycle Services (LCS) -palvelusta. Lisätietoja on ohjeaiheessa [Lataa sähköisen raportoinnin konfiguraatiot Lifecycle Servicesistä](/dynamics365/operations/dev-itpro/analytics/download-electronic-reporting-configuration-lcs). Kun olet tuonut raportointikonfiguraatiot näille tiedostomuodoille, tuodut muodot ovat saatavilla **Maksutavat** -sivulla. Tiedostomuotojen tuonnin ja valitsemisen prosessi on Euroopassa samanlainen kuin Japanissa. <!---For more details, see [Enable the JBA payment file format](https://ax.help.dynamics.com/en/wiki/enable-the-jba-payment-file-format/).-->

### <a name="method-2-x-file-formats"></a>Tapa 2: X++ -tiedostomuodot

Valitaksesi tiedostomuodot, jotka perustuvat X++ -koodia, tee seuraavat toimet.

1.  Siirry **Maksutavat** -sivulle.
2.  Valitse **Tiedostomuodot** -pikavälilehdessä **Asetukset**.
3.  Valitse välilehti, joka vastaa tiedostotyyppiä.
4.  Valitse tiedostomuoto- **Käytettävissä**-luettelosta ja siirrä se **Valitut**-luetteloon nuolen avulla.
5.  Sulje **Maksutapojen tiedostomuodot** -sivu.
6.  Valitse **Tiedostomuodot**-pikavälilehdessä maksutavan tiedostomuoto asianmukaisesta tiedostomuodon kentästä. Yleinen sähköinen raportointi -kentän arvoksi on määritettävä **Ei** X++ -tiedostomuodoille.





