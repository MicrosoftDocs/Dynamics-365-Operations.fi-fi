---
title: Hakijatoimintojen integraation tulos
description: Tässä aiheessa kuvataan Hakemuksen yhdistämisen tulos -asetusjoukkoa Dynamics 365 Human Resourcesissa.
author: jaredha
manager: tfehr
ms.date: 02/05/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2021-02-05
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 157864cd0eee879013724615ce31306c99c5aa68
ms.sourcegitcommit: 33b5c8bc4f9461e290513aa22de1ec1fba3b0742
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/05/2021
ms.locfileid: "5125806"
---
# <a name="applicant-integration-result"></a>Hakijatoimintojen integraation tulos

Tässä aiheessa kuvataan Hakemuksen yhdistämisen tulos -asetusjoukkoa Dynamics 365 Human Resourcesissa.

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