---
title: MyLeaveRequests – yleiskatsaus
description: MyLeaveRequests-entiteetti Microsoft Dynamics 365 Human Resources -ohjelmassa sisältää luettelon lomapyynnöistä.
author: twheeloc
ms.date: 02/03/2020
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 20cc53ec3bcf38444ccf75f81e28d5efd9fc4537
ms.sourcegitcommit: 1d2eeacad11c28889681504cdc509c90e3e8ea86
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/05/2022
ms.locfileid: "8717052"
---
# <a name="myleaverequests-overview"></a>MyLeaveRequests – yleiskatsaus


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Microsoft Dynamics 365 Human Resourcesin MyLeaveRequests-yksikkö sisältää luettelon lomapyynnöistä, jotka on rajattu (rajoitettu)-järjestelmään, jonka avulla käyttäjä voi tehdä kyselyitä entiteetistä.

## <a name="key"></a>Avain

  | Ominaisuuden nimi | Tietotyyppi |
  |---------------|-----------|
  | dataAreaId    | Merkkijono    |
  | RequestId     | Merkkijono    |
  | LeaveType     | Merkkijono    |
  | LeaveDate     | Päivämäärä      |
  
## <a name="properties"></a>Ominaisuudet

  | Ominaisuuden nimi     | Tietotyyppi | Tarvitaan |
  |-------------------|-----------|----------|
  | dataAreaId        | Merkkijono    | X        |
  | RequestId         | Merkkijono    | X        |
  | LeaveType         | Merkkijono    | X        |
  | LeaveDate         | Päivämäärä      | X        |
  | ReasonCodeId      | Merkkijono    |          |
  | PersonnelNumber   | Merkkijono    | X        |
  | RequestDate       | Päivämäärä      | X        |
  | Kommentti           | Merkkijono    |          |
  | Tila            | Valintalista      | X        |
  | Määrä            | Reaaliluku      |          |
  | HalfDayDefinition | Valintalista      |          |

## <a name="actions"></a>Toimenpiteet

 | Toiminnon nimi                               | Kuvaus                                     |
 |-------------------------------------------|-------------------------------------------------|
 | [lähetä](hr-developer-api-myleaverequests-submit.md)   | Lähetä pyyntö, jota työnkulku käsittelee. |

## <a name="see-also"></a>Lisätietoja

- [Lähetä lomapyyntö työnkulkuun](hr-developer-api-myleaverequests-submit.md)
- [Todennus](hr-developer-api-authentication.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
