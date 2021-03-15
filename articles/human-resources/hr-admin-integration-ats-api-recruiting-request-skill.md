---
title: Työhönottopyynnön taito
description: Tässä aiheessa kuvataan työhönottopyynnön osaamisalueen yksikköä Dynamics 365 Human Resourcesissa.
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
ms.openlocfilehash: 83a9956b9aa820e8aca9bf6b2ab920a45c1061f6
ms.sourcegitcommit: 33b5c8bc4f9461e290513aa22de1ec1fba3b0742
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/05/2021
ms.locfileid: "5125999"
---
# <a name="recruiting-request-skill"></a>Työhönottopyynnön taito

Tässä aiheessa kuvataan työhönottopyynnön osaamisalueen yksikköä Dynamics 365 Human Resourcesissa.

Fyysinen nimi: mshr_hcmrecruitingrequestskillentity

### <a name="description"></a>kuvaus

Kuvaa RecruitingRequest-pyynnön osaamisaluevaatimukset.

### <a name="json-representation"></a>JSON-esitys

```json
{
    "mshr_recruitingrequestid": "String",
    "mshr_skillid": "String",
    "mshr_skilldescription": "String",
    "mshr_ratinglevelid": "String",
    "mshr_ratingmodelid": "String",
    "mshr_ratingleveldescription": "String",
    "mshr_dataareaid": "String",
    "_mshr_dataareaid_id_value": "Guid",
    "mshr_primaryfield": "String",
    "_mshr_fk_recruitingrequest_id_value": "Guid",
    "_mshr_fk_skill_id_value": "Guid",
    "_mshr_fk_ratinglevel_id_value": "Guid",
    "_mshr_fk_ratingmodel_id_value": "Guid",
    "mshr_hcmrecruitingrequestskillentityid": "Guid"
}
```

### <a name="properties"></a>Ominaisuudet

| Ominaisuus<br>**Fyysinen nimi**<br>**_Laji_** | Käytä | kuvaus |
| --- | --- | --- |
| **Työhönottopyynnön osaamisalueen yksikön tunnus**<br>mshr_hcmrecruitingrequestskillentityid<br>*GUID* | Vain luku<br>Vaadittu | Järjestelmän luoma **työhönottopyynnön osaamisalueen** tietueen yksilöivä tunnus. |
| **Työhönottopyynnön tunnus**<br>mshr_recruitingrequestid<br>*Merkkijono* | Kirjoita kerran<br>Vaadittu | Käyttäjän luettava liittyvän työhönottopyynnön yksilöivä tunnus. |
| **Työhönottopyynnön tunnuksen arvo**<br>_mshr_fk_recruitingrequest_id_value<br>*GUID* | Vain luku<br>Vaadittu<br> Viiteavain: mshr_hcmrecruitingrequestentity-yksikön mshr_hcmrecruitingrequestentityid | Järjestelmän luoma liittyvän työhönottopyynnön yksilöivä tunnus. |
| **Osaamisaluetunnus**<br>mshr_skillid<br>*Merkkijono*<br> | Kirjoita kerran<br>Vaadittu | Käyttäjän luettava vaaditun osaamisalueen yksilöivä tunnus. |
| **Osaamisaluetunnuksen arvo**<br>_mshr_fk_skill_id_value<br>*GUID* | Vain luku<br>Vaadittu<br>Viiteavain: mshr_hcmskillentity-yksikön mshr_hcmskillentityid | Järjestelmän luoma vaaditun osaamisalueen yksilöivä tunnus. |
| **Luokitustason tunnus**<br>mshr_ratinglevelid<br>*Merkkijono* | Kirjoita kerran<br>Valinnainen | Työlle valittu vaadittu osaamisaluetason arvo osaamisalueelle määritetyn arviointimallin perusteella. |
| **Luokitustason tunnuksen arvo**<br>_mshr_fk_ratinglevel_id_value<br>*GUID* | Vain luku<br>Valinnainen<br>Viiteavain: mshr_hcmratinglevelentity-yksikön mshr_hcmratinglevelentityid | Järjestelmän luoma tason yksilöivä tunnus. |
| **Osaamisalueen kuvaus**<br>mshr_skilldescription<br>*Merkkijono* | Vain luku<br>Vaadittu | Osaamisalueen kuvaus. |
| **Luokitustason kuvaus**<br>mshr_ratingleveldescription<br>*Merkkijono* | Vain luku<br>Valinnainen | Valitun osaamisaluetason kuvaus. |
| **Tietoalueen tunnus**<br>mshr_dataareaid<br>*Merkkijono* | Luku/Kirjoitus<br>Valinnainen | Määrittää oikeushenkilön (yrityksen). |
| **Tietoalueen tunnuksen arvo**<br>_mshr_dataareaid_id_value<br>*GUID* | Vain luku<br>Valinnainen<br>Viiteavain: cdm_companyid of cdm_company-yksikkö | Järjestelmän luoma GUID-tunnus, joka yksilöi oikeushenkilön (yrityksen). |
| **Ensisijainen kenttä**<br>mshr_primaryfield<br>*Merkkijono* | Vain luku<br>Vaadittu | Työhönottopyynnön arvon ja osaamisaluetunnuksen ketjutus toisena menetelmänä tietueen yksilöiväksi tunnistamiseksi. |
| **Arviointimallin tunnus**<br>mshr_ratingmodelid<br>*Merkkijono* | Luku-Kirjoitus<br>Vaadittu | Osaamisalueen arvioinnissa käytettävä luokitusmalli. |
| **Arviointimallin tunnuksen arvo**<br>_mshr_fk_hcmratingmodel_id_value<br>*GUID* | Vain luku<br>Vaadittu<br>Viiteavain: mshr_hcmratingmodelentity-yksikön mshr_hcmratingmodelentityid | Järjestelmän luoma osaamisalueen arvioimiseksi käytetyn arviointimallin yksilöivä tunnus. |

## <a name="see-also"></a>Lisätietoja

[Hakijan seurantajärjestelmän integroinnin sovellusliittymän esittely](hr-admin-integration-ats-api-introduction.md)<br>
[Esimerkkikysely työhönottopyyntöä varten](hr-admin-integration-ats-api-recruiting-request-example-query.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]