---
title: Työhönottopyynnön toimen tila
description: Tässä aiheessa kuvataan työhönottopyynnön toimen asetusjoukkoa Dynamics 365 Human Resourcesissa.
author: jaredha
ms.date: 02/05/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2021-02-05
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 7e59e9381fb15b339095d6a71296813e0141e9ab
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2021
ms.locfileid: "5789729"
---
# <a name="recruiting-request-position-status"></a>Työhönottopyynnön toimen tila

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Tässä aiheessa kuvataan työhönottopyynnön toimen asetusjoukkoa Dynamics 365 Human Resourcesissa.

Fyysinen nimi: mshr_hcmrecruitingrequestpositionstatus

Tämä valintalista määrittää työhönottopyynnön kunkin toimen tilan arvojen asetusjoukon RecruitingRequestPosition-yksikössä.

| Arvo | Nimiö | kuvaus |
| --- | --- | --- |
| 200000000 | Julkaise | Työhönottopyynnön toimi on avoin työhönottoa varten. Tämä ei ilmaise, että toimelle ei ole tällä hetkellä aktiivista toimen määritystä. Toimelle voi olla työntekijä työhönoton aikana. Se ilmaisee vain, että toimi on käytettävissä työhönottoa varten työhönottopyynnön kontekstissa. |
| 200000001 | Täytetty | Työntekijä on valittu määritettäväksi toimeen. |
| 200000002 | Peruutettu | Tämän toimen työhönottopyyntö on peruutettu. |

## <a name="see-also"></a>Lisätietoja

[Hakijan seurantajärjestelmän integroinnin sovellusliittymän esittely](hr-admin-integration-ats-api-introduction.md)<br>
[Esimerkkikysely työhönottopyyntöä varten](hr-admin-integration-ats-api-recruiting-request-example-query.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]