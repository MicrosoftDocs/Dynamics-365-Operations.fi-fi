--- 
title: Luo myyntihinnan valintaperusteet
description: "Tässä toimintaohjeessa kuvataan, miten voit luoda myyntihinnan valintaehdon määriteperustaiselle myyntihintamallille."
author: ShylaThompson
manager: AnnBe
ms.date: 10/13/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 59f6a4131f6a27c0089a1259e3f849f91a47bc87
ms.contentlocale: fi-fi
ms.lasthandoff: 09/29/2017

---
# <a name="create-sales-price-selection-criteria"></a>Luo myyntihinnan valintaperusteet

[!include [task guide banner](../../includes/task-guide-banner.md)]

Tässä toimintaohjeessa kuvataan, miten voit luoda myyntihinnan valintaehdon määriteperustaiselle myyntihintamallille. Tämän menettelyn suorittaminen edellyttää, että ainakin yksi myyntihintamalli on käytettävissä. Tässä esimerkissä käytetään hintamallia esittelytietojen USMF-yrityksen Kaiutinratkaisu-hintamallissa. Tämän tehtävän suorittaa yleensä tuotepäällikkö.


## <a name="add-a-new-criterion-for-an-existing-sales-price-model"></a>Uuden ehdon lisääminen vanhalle myyntihintamallille
1. Valitse Tuotevarianttimallin määritys.
2. Valitse Tuotekonfiguraation mallit.
3. Valitse luettelosta kaiutinratkaisun tuotemalli, mutta älä napsauta mallinimen linkkiä.
4. Valitse toimintoruudussa Malli.
5. Valitse Hintamalliehdot.
6. Valitse Uusi.
7. Syötä Nimi-kenttään "Asiakasryhmä 10".
    * Valinnan ehdot tunnistetaan hinnoittelumallin ehdon nimen avulla.  
8. Syötä tai valitse arvo kentässä Hintamalli.
9. Valitse Tilaustyyppi-kenttään Myyntitilaus.
    * Tilauksen tyyppi määrittää tietokannan kentät, jotka ovat saatavilla valintakyselyssä.  
10. Kirjoita päivämäärä Voimassaolo alkaa -kenttään.
11. Syötä päivämäärä Vanhentuu-kenttään.
12. Valitse Tallenna.

## <a name="create-the-query-for-the-selection-criteria"></a>Luo kysely valintaperusteilla
1. Valitse Muokkaa.
2. Valitse Asiakkaat Taulukko-kentässä. 
3. Valitse Kenttä-kentässä Asiakasryhmä.
    * Tässä esimerkissä tiettyä asiakasryhmää valintakriteerinä.  
4. Valitse Ehto-kentässä Asiakasryhmä 10. 
5. Valitse OK.


