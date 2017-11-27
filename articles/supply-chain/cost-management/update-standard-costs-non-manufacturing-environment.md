---
title: "Vakiokustannusten päivittäminen muissa kuin tuotantoympäristöissä"
description: "Tämä artikkeli sisältää ohjeita vakiokustannusten päivittämiseen muussa kuin tuotantoympäristössä."
author: AndersGirke
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CostingVersion, InventItemPrice
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 79723
ms.assetid: 7ba0c408-2450-4042-9542-6fdf83c12e6c
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 0386ca1e5e7bf6e578ba2abf1b2c9eefe4dd2a02
ms.contentlocale: fi-fi
ms.lasthandoff: 11/03/2017

---

# <a name="update-standard-costs-in-a-non-manufacturing-environment"></a>Vakiokustannusten päivittäminen muissa kuin tuotantoympäristöissä

[!include[banner](../includes/banner.md)]


Tämä artikkeli sisältää ohjeita vakiokustannusten päivittämiseen muussa kuin tuotantoympäristössä.

Näissä ohjeissa lähdetään siitä, että standardikustannusten päivityksissä käytetään kahden version mallia. Kahden version mallissa yksi kustannuslaskelmaversio sisältää alun perin määritetyt lukitun kauden standardikustannukset ja toinen kustannuslaskelmaversio uusia valmistettuja nimikkeitä koskevat lisäpäivitykset. Lisäpäivitykset lisätään kustannustietueina toiseen kustannuslaskelmaversioon ja lopuksi myös aktivoidaan. On myös mahdollista käyttää yhden version lähestymistapaa, jossa käytössä on vakiokustannusten alun perin määritetty joukko. Kahden version lähestymistapa edellyttää, että määritetään toinen kustannuslaskelmaversio. Tämän kustannuslaskelmaversion määritysohjeet:

-   Määritä **standardikustannusten** kustannuslaskelmatyyppi.
-   Määritä kustannuslaskelmaversiolle sisältöä kuvaava mielekäs tunnus, kuten **2016-PÄIVITYKSET**.
-   Varmista, että kustannustietueet kuuluvat sisältöön.
-   Salli kustannustietueiden lisääminen kaikille toimipaikoille. Jos määrität toimipaikan, kustannustietueita voi lisätä vain kyseiselle toimipaikalle.
-   Määritä varmistusperiaatteeksi **Ei mitään**. Varmistusperiaate koskee vain valmistettujen nimikkeiden kustannuslaskentaa.

Voit korjata, oikaista tai päivittää uusien nimikkeiden vakiokustannuksia seuraavalla tavalla:

1.  Ota käyttöön kustannustietojen lisääminen toiseen kustannuslaskelmaan **Kustannuslaskentaversion** **määritys** -sivulla. Valinnaisesti voit estää odottavien kustannusten aktivoinnin siten, että aktivointi sallitaan vasta, kun odottavat kustannukset on määritetty kokonaisuudessaan ja totuudenmukaisesti. Voit myös lisätä päivämäärän **Päivämäärästä**-kenttään. Yleisesti ottaen käytetään päivämäärää, jona aiot ottaa käyttöön lisäpäivitykset. Voit myös jättää kustannuslaskelmaversion **Päivämäärästä**-kentän tyhjäksi ja lisätä päivämäärän kunkin kustannustietueen **Päivämäärästä**-kenttään.
2.  Lisää **Nimikkeen hinta** -sivulla päivityksiä nimikkeen kustannustietueina, jotka lisätään toiseen kustannuslaskelmaversioon.
3.  Tarkista toiseen kustannuslaskelmaversioon lisättävien nimikkeen kustannustietueiden valmiusaste ja tarkkuus **Nimikehinnat**-raportin avulla.
4.  Muuta estomerkkiä **Kustannuslaskentaversion ylläpito** -sivulla siten, että toiseen kustannuslaskelmaversioon lisätyt odottavat kustannustietueet voidaan aktivoida.
5.  Aktivoi kaikki toiseen kustannuslaskelmaversioon lisätyt odottavat kustannustietueet **Aktivoi hinnat** -sivulla (avataan **Kustannuslaskentaversion ylläpito** -sivulta). Yksittäisten nimikkeiden odottavia kustannustietueita voi myös aktivoida napsauttamalla **Aktivoi odottava hinta** -painiketta **Nimikkeen hinta** -sivulla.
6.  Voit estää muiden tietojen ylläpidon muuttamalla toiseen kustannuslaskentaversioon lisättyjä estomerkintöjä **Kustannuslaskentaversion määritys** -sivulla. Estomenettelyt estävät uusien odottavien kustannusten syötön ka odottavien kustannusten aktivoinnin.





