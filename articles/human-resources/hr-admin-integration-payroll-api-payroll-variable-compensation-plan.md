---
title: Palkanlaskennan muuttava kompensaatiosuunnitelma
description: Tämä ohjeaihe sisältää tietoja ja esimerkkikyselyn Palkanlaskennan muuttava kompensaatiosuunnitelma -yksiköstä Dynamics 365 Human Resourcesissa.
author: marcelbf
ms.date: 06/15/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: marcelbf
ms.search.validFrom: 2021-06-15
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: c30df23debed9e2ab90745e6ea9d0e6b8a05b6d5
ms.sourcegitcommit: 4d11061f5de0ddba1f968bd5c3fd694a8b104ccc
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/26/2021
ms.locfileid: "7429264"
---
# <a name="payroll-variable-compensation-plan"></a>Palkanlaskennan muuttava kompensaatiosuunnitelma

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Tässä aiheessa kuvataan Dynamics 365 Human Resourcesin Palkanlaskennan muuttava kompensaatiosuunnitelma -yksikkö.

### <a name="description"></a>kuvaus

Tämä yksikkö tarjoaa työntekijän tietylle toimelle kohdistetun palkanlaskennan muuttuvan kompensaatiosuunnitelman.

Fyysinen nimi: mshr_payrollvariablecompensationawardentity.

## <a name="properties"></a>Ominaisuudet

| Ominaisuus</br>**Fyysinen nimi**</br>**_Laji_** | Käytä | kuvaus |
| --- | --- | --- |
| **Henkilöstönumero**</br>mshr_personnelnumber</br>*Merkkijono* | Vain luku | Työntekijän yksilöivä henkilökuntanumero.  |
| **Palkkion päivämäärä**</br>mshr_awarddate</br>*Päivämäärä aika siirros* | Vain luku | Palkkion päivämäärä. |
| **Palkkion tyyppi**</br>mshr_awardtype</br>*[mshr_HrmCompVarAwardEmplType-asetusjoukko](hr-admin-integration-payroll-api-award-type.md)* | Vain luku | Muuttuvalle kompensaatiosuunnitelmalle määritetyn palkkion tyyppi. |
| **Valuutta**</br>mshr_unitcurrencycode</br>*Merkkijono* | Vain luku |Muuttuvalle kompensaatiosuunnitelmalle määritetty valuutta.   |
| **Kiinteän kompensaatiosuunnitelman tunnus**</br>mshr_fixedplanid</br>*Merkkijono* | Vain luku | Palkkion laskemisen perustana käytettävä kiinteä kompensaatiosuunnitelma. |
| **Yksikköarvo**</br>mshr_awardamount</br>*Desimaali* | Vain luku | Yksikön arvo |
| **Käsittelyn tyyppi**</br>mshr_processtype</br>*[mshr_hrmCompProcessType-asetusjoukko](hr-admin-integration-payroll-api-process-type.md)* | Vain luku | Käsittelyn tyyppi. |
| **Muuttuvan kompensaatiosuunnitelman tyyppi**</br>Merkkijono</br>*mshr_typeid* | Vain luku | Muuttuvan kompensaatiosuunnitelman tyyppi. |
| **Muuttuvan kompensaatiosuunnitelman tunnus**</br>Merkkijono</br>*mshr_planid* | Vain luku | Muuttuvan kompensaatiosuunnitelman tunnus. |
| **Yksiköiden määrä**</br>Desimaali</br>*mshr_numberofunits* | Vain luku | Palkkion yksikkömäärä. |
| **Ensisijainen kenttä**</br>mshr_primaryfield</br>*GUID* | Vain luku</br>Järjestelmän luoma. | |
| **Palkanlaskennan muuttava kompensaatiosuunnitelma -yksikkö**</br>mshr_payrollvariablecompensationawardentityid</br>*GUID* | Järjestelmän luoma | Järjestelmän luoma GUID-arvo, jonka avulla kompensaatiosuunnitelma voidaan yksilöivästi tunnistaa. |

## <a name="relations"></a>Suhteet 

|Ominaisuuden arvo | Liittyvä yksikkö | Siirtymisominaisuus | Kokoelmatyyppi |
| --- | --- | --- | --- |
| _mshr_fk_employee_id_value | [mshr_payrollemployeeentity](hr-admin-integration-payroll-api-payroll-employee.md) | mshr_FK_Employee_id | mshr_FK_PayrollEmployeeEntity_VariableCompAward |
| _mshr_fk_fixedcomp_id_value | [mshr_payrollfixedcompensationplanentity](hr-admin-integration-payroll-api-payroll-fixed-compensation-plan.md) | mshr_FK_FixedComp_id | mshr_FK_PayrollFixedCompensationPlanEntity_VariableCompAward |

## <a name="example-query"></a>Esimerkkikysely

**Pyyntö**

```http
GET [Organizaton URI]/api/data/v9.1/mshr_payrollvariablecompensationawardentities?$filter=mshr_personnelnumber eq '000046'
```

**Vastaus**

```json
{
    "mshr_personnelnumber": "000046",
    "mshr_awarddate": "2015-01-15T00:00:00Z",
    "mshr_awardtype": 200000000,
    "mshr_unitcurrencycode": "USD",
    "mshr_fixedplanid": "",
    "mshr_unitvalue": 1,
    "mshr_processtype": 200000003,
    "mshr_typeid": "Bonus",
    "mshr_planid": "MgBonus",
    "mshr_numberofunits": 1500,
    "mshr_primaryfield": "000046 | MgBonus | Bonus | 1/15/2015",
    "_mshr_fk_employee_id_value": "00000666-0000-0000-daff-004105000000",
    "mshr_payrollvariablecompensationawardentityid": "000001a4-0000-0000-0d00-005001000000",
    "_mshr_fk_fixedcomp_id_value": null
}
```

## <a name="see-also"></a>Lisätietoja

[Palkanlaskennan integroinnin ohjelmointirajapinnan esittely](hr-admin-integration-payroll-api-introduction.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
