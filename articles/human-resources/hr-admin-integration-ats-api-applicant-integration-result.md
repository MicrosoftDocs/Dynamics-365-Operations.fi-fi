---
title: Hakijatoimintojen integraation tulos
description: Tässä artikkelissa kuvataan Hakemuksen yhdistämisen tulos -asetusjoukkoa Dynamics 365 Human Resourcesissa.
author: jaredha
ms.date: 09/12/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2021-02-05
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 86f3f75e538268644cea4f927f04c07aae115f00
ms.sourcegitcommit: 27ce4fc706100b626b81c3a1023238acd872e76c
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/20/2022
ms.locfileid: "9702225"
---
# <a name="applicant-integration-result"></a>Hakijatoimintojen integraation tulos


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Tässä artikkelissa kuvataan Hakemuksen yhdistämisen tulos -asetusjoukkoa Dynamics 365 Human Resourcesissa.

Fyysinen nimi: mshr_hcmapplicantintegrationresult

Tämä valintalista antaa hakijan tietueen tilan.

| Arvo | Nimiö | kuvaus |
| --- | --- | --- |
| 200000000 | Ei käsitelty | Hakijaa harkitaan edelleen. |
| 200000001 | Otettu työhön | Hakija on palkattu. |
| 200000002 | Ei ole palkattu | On tehty päätös siitä, ettei hakijaa palkata. |
| 200000003 | Hylätty | Hakija hylättiin harkinnasta. |

## <a name="see-also"></a>Lisätietoja

[Hakijan seurantajärjestelmän integroinnin sovellusliittymän esittely](hr-admin-integration-ats-api-introduction.md)<br>
[Esimerkkikysely palkattavalle hakijalle](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
