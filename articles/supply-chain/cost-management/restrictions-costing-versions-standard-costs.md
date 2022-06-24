---
title: Standardikustannusten kustannuslaskelmaversioiden rajoitukset
description: Tässä artikkelissa käsitellään standardikustannusten kustannuslaskelmaversiota koskevia rajoituksia.
author: JennySong-SH
ms.date: 01/17/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CostingVersion
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.industry: Manufacturing
ms.author: yanansong
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8c5c00ae8952e2c80d97d039271a6f5c63e9a72f
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8867982"
---
#  <a name="restrictions-on-costing-versions-for-standard-costs"></a>Standardikustannusten kustannuslaskelmaversioiden rajoitukset

[!include [banner](../includes/banner.md)]

Tässä artikkelissa käsitellään standardikustannusten kustannuslaskelmaversiota koskevia rajoituksia. 

Seuraavilla rajoituksilla voidaan varmistaa standardikustannuksen laskennan periaatteiden noudattaminen:

-  Kulut on sisällytettävä nimikkeen kustannukseen. Valmistetun nimikkeen kulut tulevat tuoterakenteen ja reittitietojen kuoletetuista standardikustannuksista. Tämän vuoksi on sisällytettävä yksikkökustannukseen. Myös ostetun nimikkeen kulut sisällytetään nimikkeen yksikkökustannukseen.

-  Valmistettujen nimikkeiden standardikustannusten laskennan on perustuttava standardikustannusten kustannuslaskelmaversiossa oleviin kustannustietueisiin. Vaihtoehtoisia kustannustietojen lähteitä voi käyttää vain suunniteltujen kustannusten kustannuslaskelmaversion kanssa, kuten ostettujen nimikkeiden ostohintakauppasopimusten kanssa. Tuoterakenteen laskentaryhmä määrittää vaihtoehtoiset kustannustietolähteet.

-  Tuoterakennelaskelmat on tehtävä yksitasoisena hajotustilana.

Vakiokustannusten nimikekustannustiedot voi kopioida toiseen kustannuslaskelmaversioon, joka sisältää vakiokustannuksia tai suunniteltuja kustannuksia. Suunniteltujen kustannusten nimikekustannustietoja ei kuitenkaan voi kopioida standardikustannuksia sisältävään kustannuslaskelmaversioon, koska tässä artikkelissa luetellut rajoitukset eivät koskisi suunniteltuja kustannuksia.

## <a name="related-articles"></a>Liittyvät artikkelit

[Kustannuslaskelmaversiot – yleiskatsaus](costing-versions.md)

[Standardikustannusten päivittäminen muussa kuin valmistusympäristössä](update-standard-costs-non-manufacturing-environment.md)

[Valmistettujen nimikkeiden standardikustannusten ylläpitämisen valmistelutoimet](update-standard-costs-manufacturing-environment.md)



[!INCLUDE[footer-include](../../includes/footer-banner.md)]