---
title: Kustannuslaskentalomakkeet
description: "Kustannuslaskentalomakkeen määrittämiseen liittyy kaksi tavoitetta. Ensimmäinen tavoite on valmistettua tuotetta tai tuotantotilausta koskevien myytyjen tuotteiden kustannustietojen esitysmuodon määrittäminen. Tätä esitysmuotoa kutsutaan kustannuslaskentalomakkeeksi. Toinen tavoite on epäsuorien kustannusten laskemisen perustan määrittäminen. Kustannuslaskennan määritys perustuu kustannusryhmän toimintoon, jota käytetään tietojen esittämisessä ja epäsuorien kustannusten laskentakaavoissa. Tässä artikkelissa kuvataan kustannuslaskentalomakkeen määrityksen kaksi tavoitetta."
author: AndersGirke
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CostSheetDesigner
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 53201
ms.assetid: e7d72b43-3892-49ae-8821-9eede3f4d24a
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 3988bd478cfad791b5d4c73d28a86c9cfb68288f
ms.contentlocale: fi-fi
ms.lasthandoff: 11/03/2017

---

# <a name="costing-sheets"></a>Kustannuslaskentalomakkeet

[!INCLUDE [banner](../includes/banner.md)]

Kustannuslaskentalomakkeen määrittämiseen liittyy kaksi tavoitetta. Ensimmäinen tavoite on valmistettua tuotetta tai tuotantotilausta koskevien myytyjen tuotteiden kustannustietojen esitysmuodon määrittäminen. Tätä esitysmuotoa kutsutaan kustannuslaskentalomakkeeksi. Toinen tavoite on epäsuorien kustannusten laskemisen perustan määrittäminen. Kustannuslaskennan määritys perustuu kustannusryhmän toimintoon, jota käytetään tietojen esittämisessä ja epäsuorien kustannusten laskentakaavoissa. Tässä artikkelissa kuvataan kustannuslaskentalomakkeen määrityksen kaksi tavoitetta. 

Kustannuslaskentalomake on tietyn muotoinen esitys valmistettua nimikettä tai tuotantotilausta koskevien myytyjen tuotteiden kustannustiedoista. Määrittäessäsi kustannuslaskentalomaketta määrität tietojen muodon ja välillisten kustannusten laskentaperusteen. Kustannuslaskennan määritys perustuu kustannusryhmätoimintoihin, joita käytetään tietojen esittämisessä ja välillisten kustannusten laskentakaavoissa. Seuraavassa on tietoja kustannuslaskentalomakkeen kahdesta tavoitteesta:
-   **Kustannuslaskentatietueen muoto määritetään.** Kustannuslaskentalomakkeen käyttäjän määrittämä muoto määrittää niiden kustannusten kustannussegmentoinnin, jotka sisältävät valmistettujen nimikkeiden myytyjen tuotteiden kustannukset. Esimerkiksi nimikkeen myytyjen tuotteiden kustannuksia koskevat tiedot voidaan jakaa kustannusryhmien perusteella materiaaliin, työhön ja yleiskustannuksiin. Nämä kustannusryhmät on määritetty nimikkeisiin, reititystoimintojen kustannusluokkiin sekä epäsuorien kustannusten laskukaavoihin. Kustannuslaskentalomakkeen muoto edellyttää tavallisesti välisummien käyttämistä, kun kustannusryhmiä on määritetty useita. Esimerkiksi useita materiaaleihin liittyviä kustannusryhmiä voidaan yhdistää. Kustannuslaskentalomakkeen muodon määritelmä on valinnainen, mutta kustannuslaskentalomakkeen muoto täytyy määrittää, jos epäsuoria kustannuksia lasketaan.
-   **Epäsuorien kustannusten laskentaperusta määritetään.** Välilliset kustannukset kuvastavat valmistetun nimikkeen tuotantoon liittyviä valmistuksen yleiskustannuksia. Välillisten kustannusten laskentakaavan voi esittää lisämaksuna tai hintana. Lisämaksu tarkoittaa arvon prosenttiosuutta ja hinta puolestaan reitityksen työvaiheen tuntikohtaista summaa. Kustannusryhmä määrittää laskentakaavan perustan, joka voi olla esimerkiksi työkustannusryhmää koskeva 100 prosentin lisämaksu tai koneen kustannusryhmää koskeva 50,00 USD:n tuntihinta. Jos haluat määrittää laskentakaavan ja siihen liittyvän kustannusryhmäperustan, kustannuslaskentalomake edellyttää, että määrität yleiskustannuksia kuvaavan kustannusryhmän ja valitset lisämaksu- tai hintamallin.

Jokainen laskukaava täytyy lisätä kustannustietueena. Kustannustietue koostuu määritetystä kustannuslaskelmaversiosta, lisämaksuprosentista tai hinnasta, kustannusryhmän perustasta, tilasta ja voimaantulopäivästä. Kun kustannustietue lisätään, sen tila on aluksi **Odottaa** ja siinä on voimaantulopäivämäärä. Kun kustannustietue aktivoidaan, tila päivitetään niin, että tietue on nykyinen aktiivinen tietue ja voimaantulopäivämäärä päivittyy aktivointipäiväksi. Kustannustietueessa voidaan määrittää myös toimipaikka toimipaikkakohtaista laskentakaavaa varten. Voit myös jättää **Toimipaikka**-kentän tyhjäksi, jos haluat, että laskentakaavaa käytetään koko yrityksessä. Kustannustietue voi myös koostua määritetystä nimikkeestä tai nimikeryhmästä, kun laskentakaava on merkitty nimikekohtaiseksi. 

Nykyisiä aktiivisia välillisten kustannusten laskentakaavojen kustannustietueita käytetään tuotantotilauksen kustannusten arviointiin. Niitä käytetään myös toteutuneiden kustannusten laskentaan, jotka liittyvät ajan ja materiaalin todelliseen kulutukseen. Odottavien kustannusten tietueita käytetään myöhemmissä tuoterakennelaskelmissa. 

Kaksi kustannuslaskelmaversion estokäytäntöä määrittää, voidaanko odottavat kustannukset säilyttää ja aktivoida. Estomenettelyiden avulla voit ensin sallia tietojen ylläpitämisen ja estää sitten kustannuslaskelmaversion kustannustietojen ylläpitämisen. 

Kun olet määrittänyt kustannuslaskentalomakkeen muodon ja välillisten kustannusten laskelmat, suorita erillinen vaihe tietojen vahvistamiseksi ja tallentamiseksi. Kustannuslaskentalomake on koko yhtiötä koskeva muoto, jossa myytyjen tuotteiden kustannustiedot näkyvät yhtenäisesti. 

Kustannuslaskentalomake näkyy **Laske nimikekustannus** -sivun osana. Kustannuslaskentalomake voidaan näyttää valmistetun nimikkeen laskettujen kustannusten tietueelle **Nimikkeen hinta** -sivulla tai tilauskohtaiselle laskentatietueelle **Tuoterakenteen laskemisen tulokset** -sivulla. Se voidaan näyttää myös tuotantotilauksen **Hinnan laskenta** -sivun osana.






