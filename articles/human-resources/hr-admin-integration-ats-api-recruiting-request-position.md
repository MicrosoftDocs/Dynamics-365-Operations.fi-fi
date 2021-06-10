---
title: Työhönottopyynnön toimi
description: Tässä aiheessa kuvataan työhönottopyynnön toimen yksikköä Dynamics 365 Human Resourcesissa.
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
ms.openlocfilehash: a709b8fb2f22c0e7a81399349cacbcfbfc91c8b2
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/18/2021
ms.locfileid: "6059253"
---
# <a name="recruiting-request-position"></a>Työhönottopyynnön toimi

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Tässä aiheessa kuvataan työhönottopyynnön toimen yksikköä Dynamics 365 Human Resourcesissa.

Fyysinen nimi: mshr_hcmrecruitingrequestpositionentity

### <a name="description"></a>kuvaus

Kuvaa työhönottopyynnön toimen tai toimet. Toimen lisääminen työhönottopyyntöön on valinnaista. Toimen ominaisuudet ovat vain luku -ominaisuuksia, koska työhönottopyynnön toimen ominaisuudet eivät voi olla erilaiset kuin ne ovat toimen päätietueessa. Jos ominaisuuksia on tarve muuttaaa, se tulee tehdä toimen päätietueessa, ennen kuin toimi lisätään työhönottopyyntöön.

### <a name="json-representation"></a>JSON-esitys
```json
{
    "mshr_recruitingrequestid": "String",
    "mshr_positionid": "String",
    "mshr_description": "String",
    "mshr_positiontypeid": "String",
    "mshr_status": Int,
    "mshr_departmentnumber": "String",
    "mshr_reportstopositionid": "String",
    "mshr_reportstopersonnelnumber": "String",
    "mshr_financialdimension": "String",
    "mshr_dataareaid": "String",
    "_mshr_dataareaid_id_value": "Guid",
    "mshr_primaryfield": "String",
    "_mshr_fk_recruitingrequest_id_value": "Guid",
    "_mshr_fk_position_id_value": "Guid",
    "_mshr_fk_positiontype_id_value": "Guid",
    "_mshr_fk_department_id_value": "Guid",
    "_mshr_fk_reportstoposition_id_value": "Guid",
    "_mshr_fk_reportstoworker_id_value": "Guid",
    "mshr_hcmrecruitingrequestpositionentityid": "Guid"
}
```

### <a name="properties"></a>Ominaisuudet

| Ominaisuus<br>**Fyysinen nimi**<br>**_Laji_** | Käytä | kuvaus |
| --- | --- | --- |
| **Työhönottopyynnön toimen yksikön tunnus**<br>mshr_hcmrecruitingrequestpositionentityid<br>*GUID* | Vain luku<br>Vaadittu |    Järjestelmän luoma työhönottopyynnön toimitietueen tunnus. |
| **Työhönottopyynnön tunnus**<br>mshr_recruitingrequestid<br>*Merkkijono* | Kirjoita kerran<br>Vaadittu | Käyttäjän luettava työhönottopyynnön yksilöivä tunnus. |
| **Työhönottopyynnön tunnuksen arvo**<br>_mshr_fk_recruitingrequest_id_value<br>*GUID* | Vain luku<br>Vaadittu<br>Viiteavain: mshr_hcmrecruitingrequestentity-yksikön mshr_hcmrecruitingrequestentityid | Järjestelmän luoma sen työhönottopyynnön tunnus, johon toimi on määritetty. |
| **Toimen tunnus**<br>mshr_positionid<br>*Merkkijono* | Kirjoita kerran<br>Vaadittu | Käyttäjän luettava toimen yksilöivä tunnus. |
| **Toimen tunnuksen arvo**<br>_mshr_fk_position_id_value<br>*GUID* | Vain luku<br>Vaadittu<br>Viiteavain: mshr_hcmpositionv2entity-yksikön mshr_hcmpositionv2entityid | Järjestelmän luoma toimen tunnus. |
| **Kuvaus**<br>mshr_description<br>*Merkkijono* | Vain luku<br>Vaadittu | Toimen kuvaus. |
| **Toimityypin tunnus**<br>mshr_positiontypeid<br>*Merkkijono* | Vain luku<br>Valinnainen | Käyttäjän luettava toimityypin yksilöivä tunnus tälle toimelle. |
| **Toimityypin tunnuksen arvo**<br>_mshr_fk_positiontype_id_value<br>*GUID* | Vain luku<br>Valinnainen<br>Viiteavain: mshr_hcmpositiontypeentity-yksikön mshr_hcmpositiontypeentityid | Järjestelmän luoma toimityypin yksilöivä tunnus tälle toimelle. |
| **Tila**<br>mshr_status<br>*RecruitingRequestPositionStatus*-asetusjoukko | Luku/Kirjoitus<br>Vaadittu | Työhönottopyynnön toimen tila. |
| **Osaston numero**<br>mshr_departmentnumber<br>*Merkkijono* | Vain luku<br>Valinnainen<br> | Toimen osastonumero. |
| **Osastotunnuksen arvo**<br>_mshr_fk_department_id_value<br>*GUID* | Vain luku<br>Valinnainen<br>Viiteavain: mshr_omdepartmententity-yksikön mshr_omdepartmententityid | Järjestelmän luoma toimen osaston yksilöivä tunnus. |
| **Esimiehen toimen tunnus**<br>mshr_reportstopositionid<br>*Merkkijono* | Vain luku<br>Vaadittu | Sen toimen käyttäjän luettava tunnus, jolle rekrytoitu toimi raportoi organisaatiohierarkiassa. |
| **Esimiehen toimen tunnuksen arvo**<br>_mshr_fk_reportstoposition_id_value<br>*GUID* | Vain luku<br>Vaadittu<br>Viiteavain: mshr_hcmpositionv2entity-yksikön mshr_hcmpositionv2entityid | Järjestelmän luoma sen toimen tunnus, jolle rekrytoitu toimi raportoi. |
| **Esimiehen henkilöstönumero**<br>mshr_reportstopersonnelnumber<br>*Merkkijono* | Vain luku<br>Vaadittu | Sen työntekijän työntekijätunnus, jolle palkattu hakija raportoi. |
| **Esimiehen työntekijätunnuksen arvo**<br>_mshr_fk_reportstoworker_id_value<br>*GUID* | Vain luku<br>Vaadittu<br>Viiteavain: mshr_hcmworkerbaseentity-yksikön mshr_hcmworkerbaseentityid | Järjestelmän luoma työntekijän tunnus, jolle palkattu hakija raportoi. |
| **Taloushallinnon dimensio**<br>mshr_financialdimension<br>*Merkkijono* | Vain luku<br>Valinnainen | Toimelle määritetty taloushallinnon dimensio (esimerkiksi kustannuspaikka). Taloushallinnon dimensio määritetään kullekin toimelle yrityskohtaisesti. Dimensioissa määritetyt kustannuskeskukset ovat käytettävissä mshr_dimattributeomcostcenterentity-yksikön kautta. |
| **Tietoalueen tunnus**<br>mshr_dataareaid<br>*Merkkijono* | Luku/Kirjoitus<br>Valinnainen | Määrittää työhönottopyynnön toimen yrityksen. |
| **Tietoalueen tunnuksen arvo**<br>_mshr_dataareaid_id_value<br>*GUID* | Vain luku<br>Valinnainen<br>Viiteavain: cdm_companyid of cdm_company-yksikkö | Järjestelmän luoma GUID-tunnus, joka yksilöi työhönottopyynnön toimen oikeushenkilön (yrityksen). |
| **Ensisijainen kenttä**<br>mshr_primaryfield<br>*Merkkijono* | Vain luku<br>Vaadittu | Työhönottopyynnön arvon ja toimitunnuksen ketjutus toisena menetelmänä tietueen yksilöiväksi tunnistamiseksi. |

## <a name="see-also"></a>Lisätietoja

[Hakijan seurantajärjestelmän integroinnin sovellusliittymän esittely](hr-admin-integration-ats-api-introduction.md)<br>
[Esimerkkikysely työhönottopyyntöä varten](hr-admin-integration-ats-api-recruiting-request-example-query.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]