---
title: Palkanlaskennan työntekijä
description: Tämä ohjeaihe sisältää tietoja ja esimerkkikyselyn Palkanlaskennan työntekijä -yksikölle Dynamics 365 Human Resourcesissa.
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
ms.openlocfilehash: 20e74e97f98d0bc0fd454d54cbf969d4f1b46c7c98b2949b0ed8cfe671312dd2
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/05/2021
ms.locfileid: "6768188"
---
# <a name="payroll-employee"></a>Palkanlaskennan työntekijä

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Tässä aiheessa kuvataan Dynamics 365 Human Resourcesin Palkanlaskennan työntekijä -yksikkö.

Fyysinen nimi: mshr_payrollemployeeentity.

### <a name="description"></a>kuvaus

Tämä yksikkö tarjoaa tietoja työntekijästä. Sinun täytyy määrittää [palkanlaskennan integraation parametrit](hr-admin-integration-payroll-api-parameters.md) ennen tämän yksilön käyttämistä.

>[!IMPORTANT] 
>**FirstName**, **MiddleName**, **LastName**, **NameValidFrom** ja **NameValidTo** -kentät eivät ole enää saatavana tässä entiteetissä. Näin varmistetaan, että tämän entiteetin taustalla on vain yksi voimassaolopäivät ilmaiseva tietolähde.
>Nämä kentät ovat käytettävissä **DirPersonNameHistoricalEntity** ssä, joka julkaistiin Platform-päivityksessä 43. Kohteesta **PayrollEmployeeEntity** on OData-suhde kohteeseen **DirPersonNameHistoricalEntity** kentässä **Person**. 

## <a name="properties"></a>Ominaisuudet

| Ominaisuus<br>**Fyysinen nimi**<br>**_Laji_** | Käytä | kuvaus |
| --- | --- | --- |
| **Henkilöstönumero**<br>mshr_personnelnumber<br>*Merkkijono* | Vain luku | Työntekijän yksilöivä henkilökuntanumero. |
| **Ensisijainen kenttä**<br>mshr_primaryfield<br>*Merkkijono* | Vain luku<br>Järjestelmän luoma |  |
| **Oikeushenkilön tunnus**<br>mshr_legalentityID<br>*Merkkijono* | Vain luku | Määrittää oikeushenkilön (yrityksen). |
| **Sukupuoli**<br>mshr_gender<br>[mshr_hcmpersongender-asetusjoukko](hr-admin-integration-payroll-api-gender.md) | Vain luku | Työntekijän sukupuoli. |
| **Palkanlaskennan työntekijän yksikön tunnus**<br>mshr_payrollemployeeentityid<br>*GUID* | Vaadittu<br>Järjestelmän luoma | Järjestelmän luoma GUID-arvo, jonka avulla työntekijä voidaan yksilöivästi tunnistaa. |
| **Työsuhteen alkamispäivä**<br>mshr_employmentstartdate<br>*Päivämäärä aika siirros* | Vain luku | Työntekijän työsuhteen alkamispäivämäärä. |
| **Tunnustyypin tunnus**<br>mshr_identificationtypeid<br>*Merkkijono* |Vain luku | Työntekijälle määritetty tunnustyyppi. |
| **Työsuhteen päättymispäivämäärä**<br>mshr_employmentenddate<br>*Päivämäärä aika siirros* | Vain luku |Työntekijän työsuhteen päättymispäivämäärä.  |
| **Tietoalueen tunnus**<br>mshr_dataareaid_id<br>*GUID* | Vain luku <br>Järjestelmän luoma | Järjestelmän luoma GUID-tunnus, joka yksilöi oikeushenkilön (yrityksen). |
| **Voimassaolo päättyy**<br>mshr_namevalidto<br>*Päivämäärä aika siirros* |  Vain luku | Päivämäärä, johon asti työntekijän tiedot ovat voimassa. |
| **Syntymäpäivämäärä**<br>mshr_birthdate<br>*Päivämäärä aika siirros* | Vain luku | Työntekijän syntymäpäivä |
| **Tunnusnumero kohteeseen**<br>mshr_identificationnumber<br>*Merkkijono* | Vain luku |Työntekijälle määritetty tunnusnumero.  |

## <a name="example-query-for-payroll-employee"></a>Esimerkkikysely palkanlaskennan työntekijälle

**Pyyntö**

```http
GET [Organizaton URI]/api/data/v9.1/mshr_payrollemployeeentities?$filter=mshr_personnelnumber eq @personnelnumber and mshr_identificationtypeid eq @idtype and mshr_namevalidfrom le @asofdate and mshr_namevalidto ge @asofdate&@personnelnumber='000041'&@idtype='SSN'&@asofdate=2021-04-01
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
    "mshr_identificationtypeid": "SSN",
    "mshr_identificationnumber": "888-99-9342",
    "mshr_dataareaid": "USMF",
    "mshr_primaryfield": "000041 | USMF | 4/5/2011 07:00:00 am",
    "_mshr_fk_worker_id_value": "000000ad-0000-0000-d5ff-004105000000",
    "_mshr_fk_employment_id_value": "00000d0d-0000-0000-0600-014105000000",
    "_mshr_fk_fixedcompplan_id_value": "0000029f-0000-0000-d5ff-004105000000",
    "mshr_payrollemployeeentityid": "00000d3c-0000-0000-d5ff-004105000000",
    "_mshr_dataareaid_id_value": null
}
```
## <a name="see-also"></a>Lisätietoja

[Palkanlaskennan integroinnin ohjelmointirajapinnan esittely](hr-admin-integration-payroll-api-introduction.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
