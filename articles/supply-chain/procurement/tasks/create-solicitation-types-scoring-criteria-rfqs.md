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
ms.openlocfilehash: 6d1c24213b03ef234607517bd4767b4054a9c18ed3fefdd639c0024a6d7a08c5
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/05/2021
ms.locfileid: "6758469"
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