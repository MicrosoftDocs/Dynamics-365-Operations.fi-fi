---
title: Työhönottopyynnön toimen tila
description: Tässä aiheessa kuvataan työhönottopyynnön toimen asetusjoukkoa Dynamics 365 Human Resourcesissa.
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
ms.openlocfilehash: 3f7bae64f58f0bdc1603b3c1b5493f1ebcfa8de9
ms.sourcegitcommit: 33b5c8bc4f9461e290513aa22de1ec1fba3b0742
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/05/2021
ms.locfileid: "5126047"
---
# <a name="recruiting-request-position-status"></a>Työhönottopyynnön toimen tila

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