---
title: Luo tarjouspyyntöjen pyyntötyypit ja pisteytysperusteet
description: Tässä oppaassa esitellään pyyntötyypin luominen ja sen liittäminen pisteytysmenetelmään.
author: GalynaFedorova
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: PurchRFQSolicitationType, PurchRFQCaseTableListPage, PurchCreateRFQCase, PurchRFQCaseTable, PurchRFQScoringRFQCaseCriteria, PurchRFQScoringCriteriaCopy
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: gfedorova
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 69d62941629d0b1321a714df5ce6d81c6f94b9f5
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/03/2022
ms.locfileid: "8678656"
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