---
title: Uuden valmistetun nimikkeen standardikustannusten päivittäminen
description: Tämä artikkeli sisältää ohjeita uuden valmistetun tuotteen standardikustannusten päivittämiseen.
author: AndersGirke
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CostingVersion, InventStdCostConv
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 79693
ms.assetid: ba64b70f-3f4c-4373-9a7d-8fd07c45a8cf
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: bc8725bcab61fa20a4c35a83473b00e54cf0bf28
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/15/2019
ms.locfileid: "1569957"
---
# <a name="update-standard-costs-for-a-new-manufactured-item"></a>Uuden valmistetun nimikkeen standardikustannusten päivittäminen

[!include [banner](../includes/banner.md)]

Tämä artikkeli sisältää ohjeita uuden valmistetun tuotteen standardikustannusten päivittämiseen. 

Näissä ohjeissa lähdetään siitä, että standardikustannusten päivityksissä käytetään kahden version mallia. Kahden version mallissa yksi kustannuslaskelmaversio sisältää alun perin määritetyt lukitun kauden standardikustannukset ja toinen kustannuslaskelmaversio uusia valmistettuja nimikkeitä koskevat lisäpäivitykset. Lisäpäivitykset lisätään kustannustietueina toiseen kustannuslaskelmaversioon ja lopuksi ne myös aktivoidaan. Kahden version lähestymistapa edellyttää, että määritetään toinen kustannuslaskelmaversio. Tämän kustannuslaskelmaversion määritysohjeet:

-   Määritä **standardikustannusten** kustannuslaskelmatyyppi.
-   Määritä kustannuslaskelmaversiolle sisältöä kuvaava tunnus, kuten **2016-PÄIVITYKSET**.
-   Varmista **Salli hintatyyppi** -kenttäryhmässä, että **Kustannushinta**-kohdan arvoksi on asetettu **Kyllä**.
-   Salli kustannustietueiden lisääminen kaikille toimipaikoille (eli jätä **Toimipaikka**-kenttä tyhjäksi). Jos lisäät toimipaikan, kustannustietueita voi lisätä vain kyseiselle toimipaikalle.
-   Käytä varmistusperiaatetta **Aktiivinen**.

Jos haluat lisätä uusia valmistettavia nimikkeitä lukitun kauden eri kohtiin, noudata seuraavia ohjeita.

1.  Ota käyttöön kustannustietojen lisääminen toiseen, lisäpäivitykset sisältävään kustannuslaskelmaan **Kustannuslaskentaversion määritys** -sivulla. Estä odottavien kustannusten aktivointi siten, että aktivointi sallitaan vasta, kun odottavat kustannukset on määritetty kokonaisuudessaan ja totuudenmukaisesti. Määritä tyhjä alkamispäivä menettelyksi kustannuslaskelmaversioon ja lisää sitten aloituspäivämäärä kunkin kustannuslaskelman lisäämisen yhteydessä. Aloituspäivämäärän pitäisi vastata päivämäärää, joka sijoittuu uusien nimikkeiden ostamista tai valmistamista edeltävälle ajalle.
2.  **Nimikkeen hinta** -sivun avulla voit lisätä uusien ostettujen nimikkeiden kustannustietueet. Lisää jokaiselle kustannustietueelle kustannuslaskelmaversio, joka sisältää lisäpäivitykset, ja käytä aloituspäivämäärää, joka on uusien valmistettujen nimikkeiden odotettua valmistuspäivämäärää edeltävä päivämäärä.
3.  Laske uusien valmistettujen nimikkeiden kustannukset **Laskenta**-sivulla. Avaa **Laskenta** -sivu **Kustannuslaskentaversion ylläpito** -sivulta ja valitse kustannuslaskentaversio, joka sisältää lisäpäivitykset. Valintaehtojen avulla voit määrittää uuden valmistetun nimikkeen ja jonkin sen valmistetuista komponenteista. Monitasoisessa tuoterakenteessa saatat joutua määrittämään päänimikkeen, jonka komponenttina on uusia valmistettuja nimikkeitä. Lisää tuoterakennelaskelmalle aloituspäivämäärä, joka vastaa uusien valmistettujen nimikkeiden valmistuksen aloittamista. Aloituspäivämäärän pitää olla nimikkeen tuoterakenneversion ja reititysversion voimassaolopäivien puitteissa. **Huomautus:** Puuttuva kustannustietue voi tarkoittaa uutta valmistettua nimikettä. Tuoterakennelaskelmat voivat rajoittua nimikkeisiin, joilla on puuttuvia kustannuksia.
4.  Tarkista, että uusien valmistettujen nimikkeiden lasketut kustannukset ovat täydelliset ja totuudenmukaiset. **Valmis**-sivun avulla voit tarkistaa kunkin kustannustietueen lasketut kustannukset sekä mahdolliset Infoloki-varoitussanomat. Voit käyttää laskettujen kustannusten tarkistamiseen myös **Laskenta**-sivua.
5.  Muuta estomerkkiä **Kustannuslaskentaversion määritys** -sivulla siten, että toiseen kustannuslaskelmaversioon lisätyt odottavat kustannustietueet voidaan aktivoida.
6.  Ota käyttöön kaikki toiseen kustannuslaskelmaversioon lisätyt odottavat kustannustietueet **Aktivoi hinnat** -sivulla (avataan **Kustannuslaskentaversion ylläpito** -sivulta). Yksittäisten nimikkeiden odottavia kustannustietueita voi myös ottaa käyttöön napsauttamalla **Aktivoi**-painiketta **Nimikkeen hinta** -sivulla.
7.  Voit estää muiden tietojen ylläpidon muuttamalla toiseen kustannuslaskentaversioon lisättyjä estomerkintöjä **Kustannuslaskentaversion määritys** -sivulla. Estomenettelyt estävät uusien odottavien kustannusten syötön ja odottavien kustannusten aktivoinnin.




