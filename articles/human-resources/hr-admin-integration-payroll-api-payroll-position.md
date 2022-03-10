---
title: Palkanlaskennan tiedot toimista
description: Tämä ohjeaihe sisältää tietoja ja esimerkkikyselyn palkanlaskennan tiedot toimiyksiköstä Dynamics 365 Human Resourcesissa.
author: jcart
ms.date: 04/07/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2021-04-07
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 2bbb234d2f51391ea65e3d6153d6cee250f3c6dc
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/31/2022
ms.locfileid: "8069804"
---
# <a name="payroll-position"></a>Palkanlaskennan toimi


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Tässä aiheessa kuvataan Dynamics 365 Human Resourcesin Palkanlaskennan toimet -yksikkö.

Fyysinen nimi: mshr_payrollpositionentity.

### <a name="description"></a>kuvaus

Tämä yksikkö tarjoaa työntekijän toimeen liittyviä tietoja.

Fyysinen nimi: mshr_payrollpositionentity.

## <a name="properties"></a>Ominaisuudet

| Ominaisuus</br>**Fyysinen nimi**</br>**_Tyyppi_** | Käytä | Kuvaus |
| --- | --- | --- |
| **Toimen tunnus**</br>mshr_positionid</br>*Merkkijono* | Vain luku | Toimen tunnus. |
| **Maksujakson tunnus**</br>mshr_paycycleid</br>*Merkkijono* | Vain luku | Toimessa määritetty maksusykli. |
| **Vuosittaiset vakiotunnit**</br>annualregularhours</br>*Desimaali* | Vain luku | Toimessa määritetyt vuosittaiset säännölliset tunnit. |
| **Yrityksen maksama**</br>paidbylegalentity</br>*Merkkijono* | Vain luku | Maksun määräyksestä vastaavassa toimessa määritetty yritys. |
| **Voimassaolo päättyy**</br>validto</br>*Päivämäärä aika siirros* | Vain luku | Päivämäärä, johon toimitiedot ovat voimassa. |
| **Voimassaolo alkaa**</br>validfrom</br>*Päivämäärä aika siirros* | Vain luku | Päivämäärä, josta alkaen toimitiedot ovat voimassa. |
| **Ensisijainen kenttä**</br>mshr_primaryfield</br>*Merkkijono* | Järjestelmän luoma | Ensisijainen kenttä. |
| **Palkanlaskennan toimen tiedot -yksikön tunnus**</br>payrollpositiondetailsentityid</br>*Guid* | Vaadittu</br>Järjestelmän luoma. | Järjestelmän muodostama GUID-arvo, jolla toimi tunnistetaan yksilöivästi. |

## <a name="relations"></a>Suhteet

| Ominaisuuden arvo | Liittyvä yksikkö | Siirtymisominaisuus | Kokoelmatyyppi |
| --- | --- | --- | --- |
| _mshr_fk_fixedcompplan_id_value | [mshr_payrollfixedcompensationplanentity](hr-admin-integration-payroll-api-payroll-fixed-compensation-plan.md) | mshr_FK_FixedCompPlan_id | mshr_FK_PayrollFixedCompensationPlanEntity_PayrollPosition |
| _mshr_fk_hcmpositionhierarchy_id_value | mshr_hcmpositionhierarchyentity | mshr_FK_HcmPositionHierarchy_id | Ei käytettävissä |
| _mshr_fk_job_id_value | mshr_payrollpositionjobentity | mshr_FK_Job_id | mshr_FK_PayrollPositionJobEntity_Payroll |
| _mshr_fk_positionassignmentv2_id_value | mshr_hcmpositionworkerassignmentv2entity | mshr_FK_PositionAssignmentV2_id | Ei käytettävissä |

## <a name="example-query"></a>Esimerkkikysely

**Pyyntö**

```http
GET [Organizaton URI]/api/data/v9.1/mshr_payrollpositionentities?$filter=mshr_positionid eq @positionid and mshr_validfrom le @asofdate and mshr_validto ge @asofdate&@positionid='000276'&@asofdate=2021-04-01
```

**Vastaus**

```json
{
    "mshr_positionid": "000276",
    "mshr_paycycleid": "w",
    "mshr_annualregularhours": 3000,
    "mshr_paidbylegalentity": "USMF",
    "mshr_validfrom": "2021-03-14T00:00:00Z",
    "mshr_validto": "2154-12-31T00:00:00Z",
    "mshr_primaryfield": "000276 | 3/14/2021",
    "_mshr_fk_job_id_value": "00010094-0000-0000-df00-014105000000",
    "_mshr_fk_fixedcompplan_id_value": "0000029f-0000-0000-d5ff-004105000000",
    "mshr_payrollpositionentityid": "00010097-0000-0000-df00-014105000000"
}
```

## <a name="see-also"></a>Lisätietoja

[Palkanlaskennan integroinnin ohjelmointirajapinnan esittely](hr-admin-integration-payroll-api-introduction.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
