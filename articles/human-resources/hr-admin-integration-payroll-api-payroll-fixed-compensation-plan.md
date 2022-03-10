---
title: Palkanlaskennan kiinteän kompensaation suunnitelma
description: Tämä ohjeaihe sisältää tietoja ja esimerkkikyselyn palkanlaskennan kiinteän kompensaatiosuunnitelman yksiköstä Dynamics 365 Human Resourcesissa.
author: jcart
ms.date: 08/25/2021
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
ms.openlocfilehash: 14829f18fb5e3adde83e265cd6e70b60e1ff03ac
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/31/2022
ms.locfileid: "8069093"
---
# <a name="payroll-fixed-compensation-plan"></a>Palkanlaskennan kiinteän kompensaation suunnitelma


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Tässä aiheessa kuvataan Dynamics 365 Human Resourcesin Palkanlaskennan kiinteä kompensaatiosuunnitelma -yksikkö.

### <a name="description"></a>kuvaus

Tämä yksikkö tarjoaa työntekijän tietylle toimelle kohdistetun palkanlaskennan kiinteän kompensaatiosuunnitelman.

Fyysinen nimi: mshr_payrollfixedcompensationplanentity.

## <a name="properties"></a>Ominaisuudet

| Ominaisuus</br>**Fyysinen nimi**</br>**_Laji_** | Käytä | kuvaus |
| --- | --- | --- |
| **Suunnitelman tunnus**</br>mshr_planid</br>*Merkkijono* | Vain luku | Määrittää kompensaatiosuunnitelman.  |
| **Henkilöstönumero**</br>mshr_personnelnumber</br>*Merkkijono* | Vain luku | Työntekijän yksilöivä henkilökuntanumero. |
| **Palkkio**</br>mshr_payrate</br>*Desimaali* | Vain luku | Kiinteässä kompensaatiosuunnitelmassa määritetty palkkio. |
| **Toimen tunnus**</br>mshr_positionid</br>*Merkkijono* | Vain luku | Työntekijään ja kiinteän kompensaation suunnitelman rekisteröintiin liittyvän toimen tunnus. |
| **Voimassaolo alkaa**</br>mshr_validfrom</br>*Päivämäärä aika siirros* |  Vain luku | Päivämäärä, josta alkaen työntekijän kiinteä kompensaatio on voimassa.  |
| **Voimassaolo päättyy**</br>mshr_validto</br>*Päivämäärä aika siirros* | Vain luku | Päivämäärä, johon asti työntekijän kiinteä kompensaatio on voimassa. |
| **Maksutiheys**</br>mshr_payfrequency</br>*Merkkijono* | Vain luku | Tietyn maksumäärän [kompensaation maksutiheyden](hr-admin-integration-payroll-api-compensation-pay-frequency.md) tunnus. |
| **Valuutta**</br>mshr_currency</br>*Merkkijono* | Vain luku | Kiinteälle kompensaatiosuunnitelmalle määritetty valuutta. |
| **Palkanlaskennan kiinteän kompensaatiosuunnitelman yksikkö**</br>mshr_payrollfixedcompensationplanentityid</br>*GUID* | Järjestelmän luoma | Järjestelmän luoma GUID-arvo, jonka avulla kompensaatiosuunnitelma voidaan yksilöivästi tunnistaa. |

## <a name="relations"></a>Suhteet

|Ominaisuuden arvo | Liittyvä yksikkö | Siirtymisominaisuus | Kokoelmatyyppi |
| --- | --- | --- | --- |
| _mshr_fk_employee_id_value | [mshr_payrollemployeeentity](hr-admin-integration-payroll-api-payroll-employee.md) | mshr_FK_Employee_id | mshr_FK_PayrollEmployeeEntity_FixedCompPlan |
| _mshr_fk_job_id_value | [mshr_payrollpositionjobentity](hr-admin-integration-payroll-api-payroll-position-job.md) | mshr_FK_Job_id | mshr_FK_PayrollPositionJobEntity_FixedCompPlan |
| _mshr_fk_payrollposition_id_value | [mshr_payrollpositionentity](hr-admin-integration-payroll-api-payroll-position.md) | mshr_FK_PayrollPosition_id | mshr_FK_PayrollPositionEntity_FixedCompPlan |
| _mshr_fk_plan_id_value | mshr_hcmcompfixedplantableentity | mshr_FK_Plan_id | - |
| _mshr_fk_variablecompaward_id_value | [mshr_payrollvariablecompensationawardentity](hr-admin-integration-payroll-api-payroll-variable-compensation-plan.md) | mshr_FK_VariableCompAward_id | mshr_FK_PayrollVariableCompensationAwardEntity_FixedComp |

## <a name="example-query"></a>Esimerkkikysely

**Pyyntö**

```http
GET [Organizaton URI]/api/data/v9.1/mshr_payrollfixedcompensationplanentities?$filter=mshr_personnelnumber eq @personnelnumber and mshr_validfrom le @asofdate and mshr_validto ge @asofdate&@personnelnumber='000041'&@asofdate=2021-04-01
```

**Vastaus**

```json
{
    "mshr_planid": "GradeC",
    "mshr_personnelnumber": "000041",
    "mshr_payrate": 75200,
    "mshr_positionid": "000276",
    "mshr_validfrom": "2011-04-05T00:00:00Z",
    "mshr_validto": "2154-12-31T00:00:00Z",
    "mshr_payfrequency": "Annual",
    "mshr_currency": "USD",
    "_mshr_fk_employee_id_value": "00000d3c-0000-0000-d5ff-004105000000",
    "_mshr_fk_plan_id_value": "0000070c-0000-0000-b328-fef003000000",
    "_mshr_fk_job_id_value": "00010094-0000-0000-df00-014105000000",
    "mshr_payrollfixedcompensationplanentityid": "0000029f-0000-0000-d5ff-004105000000",
    "_mshr_fk_payroll_id_value": null
}
```

## <a name="see-also"></a>Lisätietoja

[Palkanlaskennan integroinnin ohjelmointirajapinnan esittely](hr-admin-integration-payroll-api-introduction.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
