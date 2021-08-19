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
ms.openlocfilehash: 96a644bf129de6dd3f78098bcb6415d17058d6decbd7d904a99bb6f050d3a9e0
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/05/2021
ms.locfileid: "6730439"
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
| **Henkilöstönumero**</br>mshr_personnelnumber</br>*Merkkijono* | Vain luku</br>Vaadittu |Työntekijän yksilöivä henkilökuntanumero.  |
| **Palkkion päivämäärä**</br>mshr_awarddate</br>*Päivämäärä aika siirros* | Vain luku</br>Vaadittu | Palkkion päivämäärä. |
| **Palkkion tyyppi**</br>mshr_awardtype</br>*[mshr_HrmCompVarAwardEmplType-asetusjoukko](hr-admin-integration-payroll-api-award-type.md)* | Vain luku</br>Vaadittu | Muuttuvalle kompensaatiosuunnitelmalle määritetyn palkkion tyyppi. |
| **Valuutta**</br>mshr_unitcurrencycode</br>*Merkkijono* | Vain luku </br>Vaadittu |Muuttuvalle kompensaatiosuunnitelmalle määritetty valuutta.   |
| **Kiinteän kompensaatiosuunnitelman tunnus**</br>mshr_fixedplanid</br>*Merkkijono* | Vain luku | Palkkion laskemisen perustana käytettävä kiinteä kompensaatiosuunnitelma. |
| **Yksikköarvo**</br>mshr_awardamount</br>*Desimaali* | Vain luku | Yksikön arvo |
| **Käsittelyn tyyppi**</br>mshr_processtype</br>*[mshr_hrmCompProcessType-asetusjoukko](hr-admin-integration-payroll-api-process-type.md)* | Vain luku | Käsittelyn tyyppi. |
| **Muuttuvan kompensaatiosuunnitelman tyyppi**</br>Merkkijono</br>*mshr_typeid* | Vain luku | Muuttuvan kompensaatiosuunnitelman tyyppi. |
| **Muuttuvan kompensaatiosuunnitelman tunnus**</br>Merkkijono</br>*mshr_planid* | Vain luku | Muuttuvan kompensaatiosuunnitelman tunnus. |
| **Ensisijainen kenttä**</br>mshr_primaryfield</br>*GUID* | Vain luku</br>Järjestelmän luoma. | |
| **Työntekijän tunnus**</br>mshr_fk_employee_id_value</br>*GUID* | Vain luku</br>Vaadittu</br>Foreign key:mshr_Employee_id of mshr_payrollemployeeentity entity  | Työntekijän tunnus. |
| **Palkanlaskennan muuttava kompensaatiosuunnitelma -yksikkö**</br>mshr_payrollvariablecompensationawardentityid</br>*GUID* | Vaadittu</br>Järjestelmän luoma | Järjestelmän luoma GUID-arvo, jonka avulla kompensaatiosuunnitelma voidaan yksilöivästi tunnistaa. |


## <a name="example-query"></a>Esimerkkikysely

**Pyyntö**

```http
GET [Organizaton URI]/api/data/v9.1/mshr_payrollvariablecompensationawardentities?$filter=mshr_personnelnumber eq '000001'
```

**Vastaus**

```json
{
    "mshr_personnelnumber": "000001",
    "mshr_awarddate": "2015-01-15T00:00:00Z",
    "mshr_awardtype": 200000000,
    "mshr_unitcurrencycode": "USD",
    "mshr_fixedplanid": "",
    "mshr_awardamount": 1,
    "mshr_processtype": 200000003,
    "mshr_typeid": "Bonus",
    "mshr_planid": "MgBonus",
    "mshr_primaryfield": "000001 | MgBonus | Bonus | 1/15/2015",
    "_mshr_fk_employee_id_value": "00000655-0000-0000-adff-004105000000",
    "mshr_payrollvariablecompensationawardentityid": "000001a1-0000-0000-adff-004105000000",
    "_mshr_fk_fixedcomp_id_value": null
}
```

## <a name="see-also"></a>Lisätietoja

[Palkanlaskennan integroinnin ohjelmointirajapinnan esittely](hr-admin-integration-payroll-api-introduction.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
