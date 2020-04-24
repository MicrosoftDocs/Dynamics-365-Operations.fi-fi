---
title: Standardikustannusten kustannuslaskelmaversioiden rajoitukset
description: Tässä ohjeaiheessa käsitellään standardikustannusten kustannuslaskelmaversiota koskevia rajoituksia.
author: AndersGirke
manager: tfehr
ms.date: 01/17/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CostingVersion
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.industry: Manufacturing
ms.author: aevengir
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2348d7721cd281bb2a1b5af007c98ce69377a412
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/02/2020
ms.locfileid: "3214432"
---
#  <a name="restrictions-on-costing-versions-for-standard-costs"></a>Standardikustannusten kustannuslaskelmaversioiden rajoitukset

[!include [banner](../includes/banner.md)]

Tässä ohjeaiheessa käsitellään standardikustannusten kustannuslaskelmaversiota koskevia rajoituksia. 

Seuraavilla rajoituksilla voidaan varmistaa standardikustannuksen laskennan periaatteiden noudattaminen:

-  Kulut on sisällytettävä nimikkeen kustannukseen. Valmistetun nimikkeen kulut tulevat tuoterakenteen ja reittitietojen kuoletetuista standardikustannuksista. Tämän vuoksi on sisällytettävä yksikkökustannukseen. Myös ostetun nimikkeen kulut sisällytetään nimikkeen yksikkökustannukseen.

-  Valmistettujen nimikkeiden standardikustannusten laskennan on perustuttava standardikustannusten kustannuslaskelmaversiossa oleviin kustannustietueisiin. Vaihtoehtoisia kustannustietojen lähteitä voi käyttää vain suunniteltujen kustannusten kustannuslaskelmaversion kanssa, kuten ostettujen nimikkeiden ostohintakauppasopimusten kanssa. Tuoterakenteen laskentaryhmä määrittää vaihtoehtoiset kustannustietolähteet.

-  Tuoterakennelaskelmat on tehtävä yksitasoisena hajotustilana.

Vakiokustannusten nimikekustannustiedot voi kopioida toiseen kustannuslaskelmaversioon, joka sisältää vakiokustannuksia tai suunniteltuja kustannuksia. Suunniteltujen kustannusten nimikekustannustietoja ei kuitenkaan voi kopioida standardikustannuksia sisältävään kustannuslaskelmaversioon, koska tässä ohjeaiheessa luetellut rajoitukset eivät koskisi suunniteltuja kustannuksia.

<a name="related-topics"></a>Liittyvät aiheet
--------

[Kustannuslaskelmaversiot – yleiskatsaus](costing-versions.md)

[Standardikustannusten päivittäminen muussa kuin valmistusympäristössä](update-standard-costs-non-manufacturing-environment.md)

[Valmistettujen nimikkeiden standardikustannusten ylläpitämisen valmistelutoimet](update-standard-costs-manufacturing-environment.md)

