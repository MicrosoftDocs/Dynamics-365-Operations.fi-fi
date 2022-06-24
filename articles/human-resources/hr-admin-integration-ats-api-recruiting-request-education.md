---
title: Työhönottopyynnön koulutus
description: Tässä artikkelissa kuvataan työhönottopyynnön koulutuksen yksikköä Dynamics 365 Human Resourcesissa.
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
ms.openlocfilehash: bcdb5e2cc61ce551af21401ea34d8e85bc21fc6c
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8893842"
---
# <a name="recruiting-request-education"></a>Työhönottopyynnön koulutus


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Tässä artikkelissa kuvataan työhönottopyynnön koulutuksen yksikköä Dynamics 365 Human Resourcesissa.

Fyysinen nimi: mshr_hcmrecruitingrequesteducationentity

### <a name="description"></a>kuvaus

Kuvaa RecruitingRequest-pyynnön koulutusvaatimukset.

### <a name="json-representation"></a>JSON-esitys

```json
{
    "mshr_recruitingrequestid": "String",
    "mshr_educationdisciplineid": "String",
    "mshr_educationdisciplinedescription": "String",
    "mshr_educationlevelid": "String",
    "mshr_educationleveldescription": "String",
    "mshr_dataareaid": "String",
    "_mshr_dataareaid_id_value": "Guid",
    "mshr_primaryfield": "String",
    "_mshr_fk_recruitingrequest_id_value": "Guid",
    "_mshr_fk_educationdiscipline_id_value": "Guid",
    "_mshr_fk_educationlevel_id_value": "Guid",
    "mshr_hcmrecruitingrequesteducationentityid": "Guid"
}
```

### <a name="properties"></a>Ominaisuudet

| Ominaisuus<br>**Fyysinen nimi**<br>**_Laji_** | Käytä | kuvaus |
| --- | --- | --- |
| **Työhönottopyynnön koulutuksen yksikön tunnus**<br>mshr_hcmrecruitingrequesteducationentityid<br>*GUID* | Vain luku<br>Vaadittu | Järjestelmän luoma työhönottopyynnön koulutuksen tietueen yksilöivä tunnus. |
| **Työhönottopyynnön tunnus**<br>mshr_recruitingrequestid<br>*Merkkijono* | Kirjoita kerran<br>Vaadittu | Käyttäjän luettava liittyvän työhönottopyynnön yksilöivä tunnus. |
| **Työhönottopyynnön tunnuksen arvo**<br>_mshr_fk_recruitingrequest_id_value<br>*GUID* | Vain luku<br>Vaadittu<br>Viiteavain: mshr_hcmrecruitingrequestentity-yksikön mshr_hcmrecruitingrequestentityid | Järjestelmän luoma liittyvän työhönottopyynnön yksilöivä tunnus. |
| **Koulutustason tunnus**<br>mshr_educationlevelid<br>*Merkkijono* | Kirjoita kerran<br>Vaadittu | Vaadittu koulutustaso. |
| **Koulutustason tunnuksen arvo**<br>_mshr_fk_educationlevel_id_value<br>*GUID* | Vain luku<br>Vaadittu<br>Viiteavain: mshr_hcmeducationlevelentity-yksikön mshr_hcmeducationlevelentityid | Järjestelmän luoma vaaditun koulutustason yksilöivä tunnus. |
| **Koulutustason kuvaus**<br>mshr_educationleveldescription<br>*Merkkijono* | Vain luku<br>Vaadittu | Vaadittu osaamisalueen tason kuvaus. |
| **Koulutusalan tunnus**<br>mshr_educationdisciplinedescription<br>*Merkkijono* | Kirjoita kerran<br>Vaadittu | Koulutusala. |
| **Koulutusalan tunnuksen arvo**<br>_mshr_fk_educationdiscipline_id_value<br>*GUID* | Vain luku<br>Vaadittu<br>Viiteavain: mshr_hcmeducationdisciplineentity-yksikön mshr_hcmeducationdisciplineentityid | Järjestelmän luoma koulutusalan yksilöivä tunnus. |
| **Koulutusalan kuvaus**<br>mshr_educationdisciplinedescription<br>Merkkijono | Vain luku<br>Vaadittu | Koulutusalan kuvaus. |
| **Tietoalueen tunnus**<br>mshr_dataareaid<br>*Merkkijono* | Luku/Kirjoitus<br>Valinnainen | Määrittää oikeushenkilön (yrityksen).|
| **Tietoalueen tunnuksen arvo**<br>_mshr_dataareaid_id_value<br>*GUID* | Vain luku<br>Valinnainen<br>Viiteavain: cdm_companyid of cdm_company-yksikkö | Järjestelmän luoma GUID-tunnus, joka yksilöi oikeushenkilön (yrityksen). |
| **Ensisijainen kenttä**<br>mshr_primaryfield<br>*Merkkijono* | Vain luku<br>Vaadittu | Työhönottopyynnön arvon, koulutustason tunnuksen ja koulutusalan tunnuksen ketjutus toisena menetelmänä tietueen yksilöiväksi tunnistamiseksi. |

## <a name="see-also"></a>Lisätietoja

[Hakijan seurantajärjestelmän integroinnin sovellusliittymän esittely](hr-admin-integration-ats-api-introduction.md)<br>
[Esimerkkikysely työhönottopyyntöä varten](hr-admin-integration-ats-api-recruiting-request-example-query.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
