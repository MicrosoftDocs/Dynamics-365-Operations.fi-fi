---
title: Luo tarjouspyyntöjen pyyntötyypit ja pisteytysperusteet
description: Tässä oppaassa esitellään pyyntötyypin luominen ja sen liittäminen pisteytysmenetelmään.
author: mkirknel
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchRFQSolicitationType, PurchRFQCaseTableListPage, PurchCreateRFQCase, PurchRFQCaseTable, PurchRFQScoringRFQCaseCriteria, PurchRFQScoringCriteriaCopy
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1b3876238a191cbbacc4e8c435bb798232e6fd6f
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/13/2020
ms.locfileid: "4427178"
---
# <a name="create-solicitation-types-and-scoring-criteria-for-rfqs"></a>Luo tarjouspyyntöjen pyyntötyypit ja pisteytysperusteet

[!include [banner](../../includes/banner.md)]

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

