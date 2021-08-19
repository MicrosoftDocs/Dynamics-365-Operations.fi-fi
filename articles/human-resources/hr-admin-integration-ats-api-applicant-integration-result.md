---
title: Hakijatoimintojen integraation tulos
description: Tässä aiheessa kuvataan Hakemuksen yhdistämisen tulos -asetusjoukkoa Dynamics 365 Human Resourcesissa.
author: jaredha
ms.date: 02/05/2021
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
ms.openlocfilehash: 3f173e15d5524dfd4d63113760760b2534cc8769456df621415a11e4053cc6fb
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/05/2021
ms.locfileid: "6725911"
---
# <a name="applicant-integration-result"></a>Hakijatoimintojen integraation tulos

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

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