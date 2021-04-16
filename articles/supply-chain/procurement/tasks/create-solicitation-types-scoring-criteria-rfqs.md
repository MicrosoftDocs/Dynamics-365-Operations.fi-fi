---
title: Luo tarjouspyyntöjen pyyntötyypit ja pisteytysperusteet
description: Tässä oppaassa esitellään pyyntötyypin luominen ja sen liittäminen pisteytysmenetelmään.
author: kamaybac
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: PurchRFQSolicitationType, PurchRFQCaseTableListPage, PurchCreateRFQCase, PurchRFQCaseTable, PurchRFQScoringRFQCaseCriteria, PurchRFQScoringCriteriaCopy
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: dabourq
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2d28cb4bf20ba50aae6b85e835339e2df711c99d
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/01/2021
ms.locfileid: "5812059"
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



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]