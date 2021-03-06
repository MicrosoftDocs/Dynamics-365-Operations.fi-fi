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
ms.openlocfilehash: 87efbf7063de373e1e0b844ff1b942cdaab4a021
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/18/2021
ms.locfileid: "6055049"
---
# <a name="payroll-employee"></a>Palkanlaskennan työntekijä

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Tämä ohjeaihe sisältää tietoja ja esimerkkikyselyn Palkanlaskennan työntekijä -yksikölle Dynamics 365 Human Resourcesissa.

## <a name="properties"></a>Ominaisuudet

| Ominaisuus<br>**Fyysinen nimi**<br>**_Laji_** | Käytä | kuvaus |
| --- | --- | --- |
| **Henkilöstönumero**<br>mshr_personnelnumber<br>*Merkkijono* | Vain luku<br>Vaadittu | Työntekijän yksilöivä henkilökuntanumero. |
| **Ensisijainen kenttä**<br>mshr_primaryfield<br>*Merkkijono* | Vaadittu<br>Järjestelmän luoma |  |
| **Sukunimi**<br>mshr_lastname<br>*Merkkijono* | Vain luku<br>Vaadittu | Työntekijän sukunimi. |
| **Oikeushenkilön tunnus**<br>mshr_legalentityID<br>*Merkkijono* | Vain luku<br>Vaadittu | Määrittää oikeushenkilön (yrityksen). |
| **Voimassaolo alkaa**<br>mshr_namevalidfrom<br>*Päivämäärä aika siirros* | Vain luku <br>Vaadittu | Päivämäärä, josta alkaen työntekijän tiedot ovat voimassa.  |
| **Sukupuoli**<br>mshr_gender<br>*Int32* | Vain luku<br>Vaadittu | Työntekijän sukupuoli. |
| **Palkanlaskennan työntekijän yksikön tunnus**<br>mshr_payrollemployeeentityid<br>*GUID* | Vaadittu<br>Järjestelmän luoma | Järjestelmän luoma GUID-arvo, jonka avulla työntekijä voidaan yksilöivästi tunnistaa. |
| **Työsuhteen alkamispäivä**<br>mshr_employmentstartdate<br>*Päivämäärä aika siirros* | Vain luku<br>Vaadittu | Työntekijän työsuhteen alkamispäivämäärä. |
| **Tunnustyypin tunnus**<br>mshr_identificationtypeid<br>*Merkkijono* |Vain luku<br>Vaadittu | Työntekijälle määritetty tunnustyyppi. |
| **Työsuhteen päättymispäivämäärä**<br>mshr_employmentenddate<br>*Päivämäärä aika siirros* | Vain luku<br>Vaadittu |Työntekijän työsuhteen päättymispäivämäärä.  |
| **Tietoalueen tunnus**<br>mshr_dataareaid_id<br>*GUID* | Vaadittu <br>Järjestelmän luoma | Järjestelmän luoma GUID-tunnus, joka yksilöi oikeushenkilön (yrityksen). |
| **Voimassaolo päättyy**<br>mshr_namevalidto<br>*Päivämäärä aika siirros* |  Vain luku<br>Vaadittu | Päivämäärä, johon asti työntekijän tiedot ovat voimassa. |
| **Syntymäpäivämäärä**<br>mshr_birthdate<br>*Päivämäärä aika siirros* | Vain luku <br>Vaadittu | Työntekijän syntymäpäivä |
| **Tunnusnumero kohteeseen**<br>mshr_identificationnumber<br>*Merkkijono* | Vain luku <br>Vaadittu |Työntekijälle määritetty tunnusnumero.  |
| **Etunimi**<br>mshr_firstname<br>*Merkkijono* | Vain luku<br>Vaadittu | Työntekijän etunimi. |
| **Toinen nimi**<br>mshr_middlename<br>*Merkkijono* | Vain luku<br>Vaadittu |Työntekijän toinen nimi.  |

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
            "mshr_firstname": "Cassie",
            "mshr_middlename": "Lassie",
            "mshr_lastname": "Hicks",
            "mshr_namevalidfrom": "2021-03-12T20:34:25Z",
            "mshr_namevalidto": "2154-12-31T23:59:59Z",
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
