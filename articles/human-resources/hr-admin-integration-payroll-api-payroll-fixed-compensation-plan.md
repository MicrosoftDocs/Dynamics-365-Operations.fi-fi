---
title: Palkanlaskennan kiinteän kompensaation suunnitelma
description: Tämä ohjeaihe sisältää tietoja ja esimerkkikyselyn palkanlaskennan kiinteän kompensaatiosuunnitelman yksiköstä Dynamics 365 Human Resourcesissa.
author: jcart
ms.date: 04/07/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2021-04-07
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 85cfce6f626090adab422ea6c60fc0778fd1ac67
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/11/2021
ms.locfileid: "6021293"
---
# <a name="payroll-fixed-compensation-plan"></a>Palkanlaskennan kiinteän kompensaation suunnitelma

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Tämä ohjeaihe sisältää tietoja ja esimerkkikyselyn palkanlaskennan kiinteän kompensaatiosuunnitelman yksiköstä Dynamics 365 Human Resourcesissa.

## <a name="properties"></a>Ominaisuudet

| Ominaisuus<br>**Fyysinen nimi**<br>**_Laji_** | Käytä | kuvaus |
| --- | --- | --- |
| **Työntekijän tunnus**<br>mshr_fk_employee_id_value<br>*GUID* | Vain luku<br>Vaadittu<br>Foreign key:mshr_Employee_id of mshr_payrollemployeeentity entity  | Työntekijän tunnus |
| **Palkkio**<br>mshr_payrate<br>*Desimaali* | Vain luku<br>Vaadittu | Kiinteässä kompensaatiosuunnitelmassa määritetty palkkio. |
| **Suunnitelman tunnus**<br>mshr_planid<br>*Merkkijono* | Vain luku<br>Vaadittu |Määrittää kompensaatiosuunnitelman.  |
| **Voimassaolo alkaa**<br>mshr_validfrom<br>*Päivämäärä aika siirros* |  Vain luku<br>Vaadittu |Päivämäärä, josta alkaen työntekijän kiinteä kompensaatio on voimassa.  |
| **Palkanlaskennan kiinteän kompensaatiosuunnitelman yksikkö**<br>mshr_payrollfixedcompensationplanentityid<br>*GUID* | Vaadittu<br>Järjestelmän luoma | Järjestelmän luoma GUID-arvo, jonka avulla kompensaatiosuunnitelma voidaan yksilöivästi tunnistaa. |
| **Maksutiheys**<br>mshr_payfrequency<br>*Merkkijono* | Vain luku<br>Vaadittu |Kuinka usein työntekijälle maksetaan palkkoja.  |
| **Voimassaolo päättyy**<br>mshr_validto<br>*Päivämäärä aika siirros* | Vain luku <br>Vaadittu | Päivämäärä, johon asti työntekijän kiinteä kompensaatio on voimassa. |
| **Toimen tunnus**<br>mshr_positionid<br>*Merkkijono* | Vain luku <br>Vaadittu | Työntekijän ja kiinteän kompensaatiosuunnitelman rekisteröintiin liittyvä postitustunnus. |
| **Valuutta**<br>mshr_currency<br>*Merkkijono* | Vain luku <br>Vaadittu |Kiinteälle kompensaatiosuunnitelmalle määritetty valuutta   |
| **Henkilöstönumero**<br>mshr_personnelnumber<br>*Merkkijono* | Vain luku<br>Vaadittu |Työntekijän yksilöivä henkilökuntanumero.  |

**Kysely**

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
