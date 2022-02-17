---
title: Palkanlaskennan työntekijän etusuunnitelma
description: Tämä ohjeaihe sisältää tietoja ja esimerkkikyselyn palkanlaskennan työntekijän etuussuunnitelman yksiköstä Dynamics 365 Human Resourcesissa.
author: marcelbf
ms.date: 07/28/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: marcelbf
ms.search.validFrom: 2021-07-28
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 1805f7efaf2efc48d5996776f3aa27d75606886f
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/31/2022
ms.locfileid: "8068431"
---
# <a name="payroll-worker-benefit-plan"></a>Palkanlaskennan työntekijän etusuunnitelma


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Tässä aiheessa käsitellään Dynamics 365 Human Resourcesin palkanlaskennan työntekijän etuussuunnitelman yksikkö.

Fyysinen nimi: mshr_payrollworkerbenefitplanentities.

### <a name="description"></a>kuvaus

Tässä yksikössä on tietoja tietyn työntekijän etuussuunnitelmasta.

## <a name="properties"></a>Ominaisuudet

| Ominaisuus</br>**Fyysinen nimi**</br>**_Laji_** | Käytä | kuvaus |
| --- | --- | --- |
| **Henkilöstönumero**</br>mshr_personnelnumber</br>*Merkkijono* | Vain luku</br>Vaadittu | Työntekijän yksilöivä henkilökuntanumero. |
| **Oikeushenkilön tunnus**</br>mshr_legalentityID</br>*Merkkijono* | Vain luku | Määrittää oikeushenkilön (yrityksen). |
| **Kauden tunnus**</br>mshr_periodid</br>*Merkkijono* | Vain luku | Kauden tunniste. |
| **Suunnitelman tunnus**</br>mshr_planid</br>*Merkkijono* | Vain luku | Suunnitelman tunniste. |
| **Kattavuusasetus**</br>mshr_coverageoptionid</br>*Merkkijono* | Vain luku | Kattavuusvaihtoehdon tunniste. |
| **Vähennyksen alkamispäivämäärä**</br>mshr_deductionstartdatetime</br>*Päivämäärä aika siirros* | Vain luku | Vähennyksen alkamispäivä. |
| **Vähennyksen päättymispäivä**</br>mshr_deductionenddatetime</br>*Päivämäärä aika siirros* | Vain luku | Vähennyksen päättymispäivä. |
| **Tila**</br>mshr_status</br>*[Työtekijän etuussuunnitelman tilan asetusjoukko](hr-admin-integration-payroll-api-benefit-employee-plan-status.md)* | Vain luku | Etuussuunnitelman tila. |
| **Voimassaolo alkaa**</br>mshr_validfrom</br>*Päivämäärä aika siirros* | Vain luku | Aika, josta lähtien tämä tietue on voimassa. |
| **Voimassaolo päättyy**</br>mshr_validto</br>*Päivämäärä aika siirros* |  Vain luku | Aika, johon asti tämä tietue on voimassa. |
| **Suunnitelman tyypin tunnus**</br>mshr_plantypeid</br>*Merkkijono* | Vain luku | Suunnitelman tyypin tunniste. |
| **Suunnitelman tyypin koodi**</br>mshr_plantypecode</br>*[etuussuunnitelmatyypin kattavuuden asetusjoukko](hr-admin-integration-payroll-api-benefit-plan-type-cover.md)* | Vain luku | Suunnitelman tyypin määritys. |
| **Maksukausien määrä**</br>mshr_payperiod</br>*Kokonaisluku* | Vain luku | Maksukausien määrä, joka ilmaisee, kuinka usein edun toimittajalle tai työntekijöille maksetaan. Tätä määrää käytetään laskettaessa työntekijän vuosittaisen etuuden palkkasumma. |
| **Työntekijän summa**</br>mshr_amountemployee</br>*Desimaali* | Vain luku | Työntekijän summa tai prosenttiosuus. |
| **Työnantajan summa**</br>mshr_amountemployer</br>*Desimaali* | Vain luku | Työnantajan summa tai prosenttiosuus. |
| **Ensisijainen kenttä**</br>mshr_primaryfield</br>*Merkkijono* | Järjestelmän luoma | Ensisijainen kenttä. |
| **Työntekijätunnuksen arvo** </br>_mshr_fk_worker_id_value</br>*GUID* | Viiteavain: mshr_hcmworkerbaseentity-yksikön mshr_hcmworkerbaseentityid. | Järjestelmän luoma työntekijän yksilöivä tunnus. |
| **Kauden tunnuksen arvo**</br> _mshr_fk_period_id_value</br>*GUID* | Viiteavain: mshr_benefitperiodentity-yksikön mshr_benefitperiodentityid. | Järjestelmän luoma kauden yksilöivä tunnus. |
| **Suunnitelman tunnuksen arvo**</br> _mshr_fk_plan_id_value</br>*GUID* | Viiteavain: mshr_benefitplanentity-yksikön mshr_benefitplanentityid. | Järjestelmän luoma suunnitelman yksilöivä tunnus. |
| **Suunnitelman tyypin tunnuksen arvo**</br> _mshr_fk_plantype_id_value</br>*GUID* | Viiteavain: mshr_benefitplantypeentity-yksikön mshr_benefitplantypeentityid. | Järjestelmän luoma suunnitelman yksilöivä tunnus. |
| **Kattavuusvaihtoehdon tunnuksen arvo**</br> _mshr_fk_coverageoption_id_value</br>*GUID* | Viiteavain: mshr_benefitcoverageoptionentity-yksikön mshr_benefitcoverageoptionentityid. | Järjestelmän luoma suunnitelman yksilöivä tunnus. |
| **Palkanlaskennan työntekijän etuussuunnitelman yksikön tunnuksen arvo**</br> mshr_payrollworkerbenefitplanentityid</br>*GUID* | Vain luku </br> Järjestelmän luoma | Järjestelmän luoma tietueen yksilöivä tunnus. |

## <a name="example-query-for-payroll-worker-benefit-plan"></a>Palkanlaskennan työntekijän etuussuunnitelman esimerkkikysely

**Pyyntö**

```http
GET [Organization URI]/api/data/v9.1/mshr_payrollworkerbenefitplanentities?$filter=mshr_personnelnumber eq '000020'
```

**Vastaus**

```json
{
    "mshr_personnelnumber": "000020",
    "mshr_legalentityid": "USMF",
    "mshr_periodid": "2021",
    "mshr_planid": "Dental plan",
    "mshr_coverageoptionid": "Emp Only",
    "mshr_deductionstartdatetime": "2021-01-01T06:00:00Z",
    "mshr_deductionenddatetime": "2021-12-31T06:00:00Z",
    "mshr_status": 200000001,
    "mshr_validfrom": "2021-01-01T06:00:00Z",
    "mshr_validto": "2021-12-31T06:00:00Z",
    "mshr_plantypeid": "Dental",
    "mshr_plantypecode": 200000001,
    "mshr_payperiod": 12,
    "mshr_amountemployee": 47,
    "mshr_amountemployer": 57,
    "mshr_primaryfield": "000020 | USMF | 2021 | Dental plan",
    "_mshr_fk_worker_id_value": "000000ae-0000-0000-bfff-004105000000",
    "_mshr_fk_period_id_value": "00000807-0000-0000-ee02-005001000000",
    "_mshr_fk_plan_id_value": "00000c61-0000-0000-0200-005001000000",
    "_mshr_fk_plantype_id_value": "0000057c-0000-0000-0200-005001000000",
    "_mshr_fk_coverageoption_id_value": "00000391-0000-0000-0b00-005001000000",
    "mshr_payrollworkerbenefitplanentityid": "000006c4-0000-0000-bfff-004105000000"
}
```
## <a name="see-also"></a>Lisätietoja

[Palkanlaskennan integroinnin ohjelmointirajapinnan esittely](hr-admin-integration-payroll-api-introduction.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
