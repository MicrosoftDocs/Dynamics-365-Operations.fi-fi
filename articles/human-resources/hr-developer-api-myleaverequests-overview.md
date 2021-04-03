---
title: MyLeaveRequests – yleiskatsaus
description: Microsoft Dynamics 365 Human Resourcesin MyLeaveRequests-yksikkö sisältää luettelon lomapyynnöistä, jotka on rajattu (rajoitettu)-järjestelmään, jonka avulla käyttäjä voi tehdä kyselyitä entiteetistä.
author: andreabichsel
manager: tfehr
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: c2c14a0cc935ad166a2c6600f1e96c3e09ab16ca
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/17/2021
ms.locfileid: "5465507"
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