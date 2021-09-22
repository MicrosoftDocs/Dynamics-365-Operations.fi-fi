---
title: Palkanlaskennan työntekijä
description: Tämä ohjeaihe sisältää tietoja ja esimerkkikyselyn Palkanlaskennan työntekijä -yksikölle Dynamics 365 Human Resourcesissa.
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
ms.openlocfilehash: 450872a38c833de9d37e2c6224839f2bca7cb4c6
ms.sourcegitcommit: 4d11061f5de0ddba1f968bd5c3fd694a8b104ccc
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/26/2021
ms.locfileid: "7429226"
---
# <a name="payroll-employee"></a>Palkanlaskennan työntekijä

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Tässä aiheessa kuvataan Dynamics 365 Human Resourcesin Palkanlaskennan työntekijä -yksikkö.

Fyysinen nimi: mshr_payrollemployeeentity.

### <a name="description"></a>kuvaus

Tämä yksikkö tarjoaa tietoja työntekijästä. Sinun täytyy määrittää [palkanlaskennan integraation parametrit](hr-admin-integration-payroll-api-parameters.md) ennen tämän yksilön käyttämistä.

>[!IMPORTANT] 
>**FirstName**, **MiddleName**, **LastName**, **NameValidFrom** ja **NameValidTo** -kentät eivät ole enää saatavana tässä entiteetissä. Näin varmistetaan, että tämän entiteetin taustalla on vain yksi voimassaolopäivät ilmaiseva tietolähde.
>Nämä kentät ovat käytettävissä **DirPersonNameHistoricalEntity** ssä, joka julkaistiin Platform-päivityksessä 43. Kohteesta **PayrollEmployeeEntity** on OData-suhde kohteeseen **DirPersonNameHistoricalEntity**. 

## <a name="properties"></a>Ominaisuudet

| Ominaisuus</br>**Fyysinen nimi**</br>**_Laji_** | Käytä | kuvaus |
| --- | --- | --- |
| **Oikeushenkilön tunnus**</br>mshr_legalentityid</br>*Merkkijono* | Vain luku | Määrittää oikeushenkilön (yrityksen). |
| **Henkilöstönumero**</br>mshr_personnelnumber</br>*Merkkijono* | Vain luku | Työntekijän yksilöivä henkilökuntanumero. |
| **Työsuhteen alkamispäivä**</br>mshr_employmentstartdate</br>*Päivämäärä aika siirros* | Vain luku | Työntekijän työsuhteen alkamispäivämäärä. |
| **Työsuhteen päättymispäivämäärä**</br>mshr_employmentenddate</br>*Päivämäärä aika siirros* | Vain luku |Työntekijän työsuhteen päättymispäivämäärä.  |
| **Syntymäpäivämäärä**</br>mshr_birthdate</br>*Päivämäärä aika siirros* | Vain luku | Työntekijän syntymäpäivä. |
| **Sukupuoli**</br>mshr_gender</br>[mshr_hcmpersongender-asetusjoukko](hr-admin-integration-payroll-api-gender.md) | Vain luku | Työntekijän sukupuoli. |
| **Työsuhteen tyyppi**</br>mshr_employmenttype</br>[mshr_hcmemploymenttype-asetusjoukko](hr-admin-integration-payroll-api-hcmemploymenttype.md) | Vain luku | Työsuhteen tyyppi. |
| **Tunnustyypin tunnus**</br>mshr_identificationtypeid</br>*Merkkijono* |Vain luku | Työntekijälle määritetty tunnustyyppi. |
| **Tunnusnumero kohteeseen**</br>mshr_identificationnumber</br>*Merkkijono* | Vain luku |Työntekijälle määritetty tunnusnumero. |
| **Valmis maksettavaksi**</br>mshr_readytopay</br>[mshr_noyes-asetusjoukko](hr-admin-integration-payroll-api-no-yes.md) | Vain luku | Ilmaisee, onko työntekijä merkitty maksuvalmiiksi. |
| **Palkanlaskennan työntekijän yksikön tunnus**</br>mshr_payrollemployeeentityid</br>*GUID* | Vaadittu</br>Järjestelmän luoma | Järjestelmän luoma GUID-arvo, jonka avulla työntekijä voidaan yksilöivästi tunnistaa. |

## <a name="relations"></a>Suhteet

|Ominaisuuden arvo | Liittyvä yksikkö | Siirtymisominaisuus | Kokoelmatyyppi |
| --- | --- | --- | --- |
| _mshr_fk_employment_id_value | mshr_hcmemploymentdetailentity | mshr_FK_Employment_id | - |
| _mshr_fk_fixedcompplan_id_value | [mshr_payrollfixedcompensationplanentity](hr-admin-integration-payroll-api-payroll-fixed-compensation-plan.md) | mshr_FK_FixedCompPlan_id | mshr_FK_PayrollFixedCompensationPlanEntity_Employee |
| _mshr_fk_name_id_value | mshr_dirpersonnamehistoricalentity | mshr_FK_Name_id | - |
| _mshr_fk_worker_id_value | mshr_hcmworkerbaseentity | mshr_FK_Worker_id | - |
| _mshr_fk_workerbankaccount_id_value | mshr_hcmworkerbankaccountentity | mshr_FK_WorkerBankAccount_id | - |
| _mshr_fk_variablecompaward_id_value | [mshr_payrollvariablecompensationawardentity](hr-admin-integration-payroll-api-payroll-variable-compensation-plan.md) | mshr_FK_VariableCompAward_id | mshr_FK_PayrollVariableCompensationAwardEntity_Employee |
| _mshr_fk_address_id_value | [mshr_payrollworkeraddressentity](hr-admin-integration-payroll-api-payroll-worker-address.md) | mshr_FK_Address_id | mshr_FK_PayrollWorkerAddressEntity_Worker |

## <a name="example-query-for-payroll-employee"></a>Esimerkkikysely palkanlaskennan työntekijälle

**Pyyntö**

```http
GET [Organizaton URI]/api/data/v9.1/mshr_payrollemployeeentities?$filter=mshr_personnelnumber eq '000041'
```

**Vastaus**

```json
{
    "mshr_legalentityid": "USMF",
    "mshr_personnelnumber": "000041",
    "mshr_employmentstartdate": "2011-04-05T07:00:00Z",
    "mshr_employmentenddate": "2154-12-31T23:59:59Z",
    "mshr_birthdate": "1987-09-12T00:00:00Z",
    "mshr_gender": 200000002,
    "mshr_employmenttype": 200000000,
    "mshr_identificationtypeid": "SSN",
    "mshr_identificationnumber": "888-99-9342",
    "mshr_readytopay": 200000000,
    "mshr_dataareaid": "USMF",
    "mshr_primaryfield": "000041 | USMF | 4/5/2011 07:00:00 am",
    "_mshr_fk_employment_id_value": "00000d4e-0000-0000-0600-014105000000",
    "_mshr_fk_fixedcompplan_id_value": "00000598-0000-0000-4cd0-fda002000000",
    "_mshr_fk_name_id_value": "00000832-0000-0000-d700-014105000000",
    "_mshr_fk_worker_id_value": "000000af-0000-0000-d5ff-004105000000",
    "_mshr_fk_workerbankaccount_id_value": "000006f2-0000-0000-b7ff-004105000000",
    "mshr_payrollemployeeentityid": "00000666-0000-0000-d5ff-004105000000",
    "_mshr_fk_address_id_value": null,
    "_mshr_fk_variablecompaward_id_value": null,
    "_mshr_dataareaid_id_value": null
}
```

## <a name="see-also"></a>Lisätietoja

[Palkanlaskennan integroinnin ohjelmointirajapinnan esittely](hr-admin-integration-payroll-api-introduction.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
