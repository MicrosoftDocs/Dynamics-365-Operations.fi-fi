---
title: Palkanlaskennan työ
description: Tämä ohjeaihe sisältää tietoja ja esimerkkikyselyn Palkanlaskennan työntekijän työyksiköstä Dynamics 365 Human Resourcesissa.
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
ms.openlocfilehash: c0b70411e6535b22d698545438dcb0b16935e731
ms.sourcegitcommit: 12e26ef25c492e5032260733b50cd642cbd6164d
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/28/2021
ms.locfileid: "7559580"
---
# <a name="payroll-position-job"></a>Palkanlaskennan työ

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Tässä aiheessa kuvataan Dynamics 365 Human Resourcesin Palkanlaskennan työ -yksikkö.

### <a name="description"></a>kuvaus

Tämä yksikkö tarjoaa kiinteän kompensaation suunnitelman toimen ja työn välisen suhteen.

Fyysinen nimi: mshr_payrollpositionjobentity.

## <a name="properties"></a>Ominaisuudet

| Ominaisuus</br>**Fyysinen nimi**</br>**_Tyyppi_** | Käytä | Kuvaus |
| --- | --- | --- |
| **Toimen tunnus**</br>mshr_positionid</br>*Merkkijono* | Vain luku | Toimen tunnus. |
| **Voimassaolo alkaa**</br>mshr_validto</br>*Päivämäärä aika siirros* | Vain luku | Päivämäärä, josta alkaen toimi ja työsuhde on voimassa. |
| **Voimassaolo päättyy**</br>mshr_validto</br>*Päivämäärä aika siirros* | Vain luku | Päivämäärä, johon toimi ja työsuhde on voimassa. |
| **Työn tunnus**</br>mshr_jobid</br>*Merkkijono* | Vain luku | Työn tunnus. |
| **Ensisijainen kenttä**</br>mshr_primaryfield</br>*Merkkijono* | Järjestelmän luoma | Ensisijainen kenttä. |
| **Palkanlaskennan työn yksikkötunnus**</br>mshr_payrollpositionjobentityid</br>*Guid* | Järjestelmän luoma. | Järjestelmän muodostama GUID-arvo, jolla työ tunnistetaan yksilöivästi. |

## <a name="relations"></a>Suhteet

| Ominaisuuden arvo | Liittyvä yksikkö | Siirtymisominaisuus | Kokoelmatyyppi |
| --- | --- | --- | --- |
| _mshr_fk_fixedcompplan_id_value | mshr_payrollfixedcompensationplanentity | mshr_FK_FixedCompPlan_id | mshr_FK_PayrollFixedCompensationPlanEntity_Job |
| _mshr_fk_jobdetail_id_value | mshr_hcmjobdetailentity | mshr_FK_JobDetail_id | Ei käytettävissä |
| _mshr_fk_payroll_id_value | mshr_payrollpositionentity | mshr_FK_Payroll_id | mshr_FK_PayrollPositionEntity_Job |

## <a name="example-query"></a>Esimerkkikysely

**Pyyntö**

```http
GET [Organizaton URI]/api/data/v9.1/mshr_payrollpositionjobentities?$filter=mshr_positionid eq '000276'
```

**Vastaus**

```json
{
    "mshr_positionid": "000276",
    "mshr_validfrom": "2016-07-06T18:11:33Z",
    "mshr_validto": "2154-12-31T23:59:59Z",
    "mshr_jobid": "Accountant",
    "mshr_primaryfield": "000276 | Accountant | 7/6/2016 06:11:33 pm",
    "_mshr_fk_jobdetail_id_value": "00000b8d-0000-0000-b0ff-004105000000",
    "_mshr_fk_fixedcompplan_id_value": "0000058a-0000-0000-d5ff-004105000000",
    "_mshr_fk_payroll_id_value": "00000427-0000-0000-df00-014105000000",
    "mshr_payrollpositionjobentityid": "00000906-0000-0000-df00-014105000000"
}
```

## <a name="see-also"></a>Lisätietoja

[Palkanlaskennan integroinnin ohjelmointirajapinnan esittely](hr-admin-integration-payroll-api-introduction.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
