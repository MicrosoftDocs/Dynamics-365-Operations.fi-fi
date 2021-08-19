---
title: MyLeaveRequests – yleiskatsaus
description: Microsoft Dynamics 365 Human Resourcesin MyLeaveRequests-yksikkö sisältää luettelon lomapyynnöistä, jotka on rajattu (rajoitettu)-järjestelmään, jonka avulla käyttäjä voi tehdä kyselyitä entiteetistä.
author: andreabichsel
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: intro-internal
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: fefa436142fb99ed3bfb3d4454046a5d76619daecbf6f05100e8e405fca67d48
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/05/2021
ms.locfileid: "6732102"
---
# <a name="myleaverequests-overview"></a>MyLeaveRequests – yleiskatsaus

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