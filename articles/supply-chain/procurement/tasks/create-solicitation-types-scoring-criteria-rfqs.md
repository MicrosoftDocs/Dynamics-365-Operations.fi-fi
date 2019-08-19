---
title: Luo tarjouspyyntöjen pyyntötyypit ja pisteytysperusteet
description: Tässä oppaassa esitellään pyyntötyypin luominen ja sen liittäminen pisteytysmenetelmään.
author: mkirknel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchRFQSolicitationType, PurchRFQCaseTableListPage, PurchCreateRFQCase, PurchRFQCaseTable, PurchRFQScoringRFQCaseCriteria, PurchRFQScoringCriteriaCopy
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1a3e0d00d674af913953d7fd01183b0289c20d3d
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/01/2019
ms.locfileid: "1844096"
---
# <a name="create-solicitation-types-and-scoring-criteria-for-rfqs"></a>Luo tarjouspyyntöjen pyyntötyypit ja pisteytysperusteet

[!include [task guide banner](../../includes/task-guide-banner.md)]

Tässä oppaassa esitellään pyyntötyypin luominen ja sen liittäminen pisteytysmenetelmään. Siinä esitellään myös pyyntötyypin käyttäminen tarjouspyynnössä, jolla asetetaan oletuspisteytysmenetelmä. Yleensä ostopäällikkö tekee nämä tehtävät. Voit käyttää tätä menettelyä USMF-demoyrityksen tiedoilla tai omilla tiedoillasi. Tarvitset käytettävän pisteytysmenetelmän ennen aloittamista.


## <a name="create-a-solicitation-type"></a>Luo pyyntötyyppi.
1. Siirry kohtaan Hankinta > Asetukset > Tarjouspyyntö > Pyyntötyyppi.
2. Valitse Uusi.
3. Kirjoita arvo Nimi-kenttään.
4. Kirjoita arvo Kuvaus-kenttään.
5. Valitse Pisteytysmenetelmä-kentästä menetelmä, jota haluat käyttää kyseisellä pyyntötyypillä.
6. Valitse Tallenna.
7. Sulje sivu.

## <a name="use-the-solicitation-type"></a>Käytä pyyntötyyppiä
1. Valitse Hankinta > Tarjouspyynnöt > Kaikki tarjouspyynnöt.
2. Valitse Uusi.
3. Valitse Pyyntö-kentässä juuri luomasi pyyntötyyppi. 
    *   
4. Valitse OK.
5. Valitse Pisteytysehdot.
    * Esitetyt pisteytysperusteet ovat peräisin on pyyntöön liittämästäsi pisteytysmenetelmästä. Voit halutessasi lisätä tai poistaa perusteita tällä sivulla. On myös mahdollista lisätä uusia perusteita kopioimalla ne muista pisteytysmenetelmistä.  
6. Napsauta Kopioi ehdot -painiketta.
7. Anna tai valitse arvo Pisteytysmenetelmä-kentässä.
8. Valitse OK.
9. Sulje sivu.

