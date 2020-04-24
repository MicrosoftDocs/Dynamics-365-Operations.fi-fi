---
title: Tuoterakenteen laskeminen käyttämällä yhtä tasorakennetta (helmikuu 2016)
description: Tämä menettely osoittaa, miten valmiin tuotteen kustannukset lasketaan käyttämällä kustannuslaskentalomakkeeseen perustuvaa yksitasoista hajotusta.
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductDetailsExtended, InventItemPrice, BOMCalcDialog
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e7c2c34474cada787b7a7ba720ba177aa8dc125f
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/02/2020
ms.locfileid: "3214343"
---
# <a name="calculate-a-bom-by-using-a-single-level-structure-february-2016"></a>Tuoterakenteen laskeminen käyttämällä yhtä tasorakennetta (helmikuu 2016)

[!include [banner](../../includes/banner.md)]

Tämä menettely osoittaa, miten valmiin tuotteen kustannukset lasketaan käyttämällä kustannuslaskentalomakkeeseen perustuvaa yksitasoista hajotusta. Tämä on tuoterakenteen laskentasarjan kuudes tehtävä. Tämän tehtävän luomisessa käytetty esittely-yritys on USMF.

1. Siirry Vapautetut tuotteet -kohtaan.
2. Etsi haluamasi tietue luettelosta ja valitse se.
    * Valitse tuotteen BOM_1.  
3. Valitse toimintoruudussa Hallitse kustannuksia.
4. Valitse Nimikkeen hinta.
5. Valitse Laske nimikekustannus.
    * Asetus ei ehkä ole päävalikossa näkyvissä, ennen kuin ellipsipainiketta (...) napsautetaan.  
6. Avaa haku napsauttamalla Kustannusversio-kentässä avattavan valikon painiketta.
    * Valitse tässä esimerkissä 10. Tätä kustannuslaskentaversiosta käytetään myös kustannushinnan lisäämiseen osiin.  
7. Valitse OK.
8. Valitse Näytä laskennan tiedot.
    * Asetus ei ehkä ole päävalikossa näkyvissä, ennen kuin ellipsipainiketta (...) napsautetaan.    Kustannuksen kokoonpano:  *    10 johdetaan kohteesta ITEM_A, 10 kohteesta ITEM_B, 10 kohteesta BOM_2. Tässä tapauksessa kohteen BOM_2 tietoja ei ole, koska se annettiin standardikustannuksena 10 eikä sitä saatu laskemalla.  *  7 johdetaan asetusajasta, joka on vakiokustannus, ja ylimääräinen 7 johdetaan ajoaikatyövaiheesta (prosessi).  *   Lisäksi on epäsuoria kustannuksia vastaavia summia.  
9. @SysTaskRecorder:_RequestClose

