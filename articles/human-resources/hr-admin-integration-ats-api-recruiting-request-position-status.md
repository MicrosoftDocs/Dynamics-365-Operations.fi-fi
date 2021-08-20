---
title: Työhönottopyynnön toimen tila
description: Tässä aiheessa kuvataan työhönottopyynnön toimen asetusjoukkoa Dynamics 365 Human Resourcesissa.
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
ms.openlocfilehash: dee34366289f2e7ade1a1ae24bea15c0d19683d79720a44a6327879e8060a810
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/05/2021
ms.locfileid: "6725887"
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