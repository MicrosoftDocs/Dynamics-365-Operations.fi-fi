---
title: Luo myyntihinnan valintaperusteet
description: Tässä toimintaohjeessa kuvataan, miten voit luoda myyntihinnan valintaehdon määriteperustaiselle myyntihintamallille.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCPriceModelSelectionCriteria, SysQueryForm, SysQueryTableLookUp, SysQueryFieldLookUp
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1ce4388cc4bea8314e131690409ad181c9174bcc
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/29/2019
ms.locfileid: "336057"
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

