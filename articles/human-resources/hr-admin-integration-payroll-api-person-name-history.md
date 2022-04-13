---
title: Henkilön nimen historia
description: Tämä aiheessa on Henkilön nimen historia -yksikön tietoja ja sitä koskeva esimerkkikysely Dynamics 365 Human Resourcesissa.
author: twheeloc
ms.date: 09/01/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2021-09-01
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: db22a602c782cef15b6e5769b9c0726dff158160
ms.sourcegitcommit: d67f7edaf1a50077c2a7dd105e774f86fc586495
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/02/2022
ms.locfileid: "8533595"
---
# <a name="person-name-history"></a>Henkilön nimen historia


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Tässä aiheessa käsitellään Dynamics 365 Human Resourcesin Henkilön nimen historia -yksikköä.

Fyysinen nimi: mshr_dirpersonnamehistoricalentity.

### <a name="description"></a>Kuvaus

Tässä yksikössä on tietoja tietyn henkilön nimihistoriasta.

> [!IMPORTANT] 
> **FirstName**, **MiddleName**, **LastName**, **NameValidFrom** ja **NameValidTo** -kentät eivät ole enää saatavana Palkanlaskennan työntekijä -yksikössä. Ne poistettu, koska niin varmistetaan, että tämän yksikön taustalla on vain yksi voimassaolopäivät ilmaiseva tietolähde.

## <a name="properties"></a>Ominaisuudet

| Ominaisuus</br>**Fyysinen nimi**</br>**_Tyyppi_** | Käytä | Kuvaus |
| --- | --- | --- |
| **Etunimi**</br>mshr_firstname</br>*Merkkijono* | Vain luku | Etunimi. |
| **Sukunimen etuliite**</br>mshr_lastnameprefix</br>*Merkkijono*) | Vain luku | Sukunimen etuliite. |
| **Sukunimi**</br>mshr_lastname</br>*Merkkijono*) | Vain luku | Sukunimi. |
| **Toinen nimi**</br>mshr_middlename</br>*Merkkijono*) | Vain luku | Toinen nimi. |
| **Voimassaolo päättyy**</br>mshr_validto</br>*Merkkijono*) | Vain luku | Päivämäärä, johon asti nimi on voimassa. |
| **Osapuolinumero**</br>mshr_partynumber</br>*Merkkijono* | Vain luku | Käyttäjän luettava, järjestelmän luoma henkilön yksilöivä tunnus. |
| **Ensisijainen kenttä**</br>mshr_primaryfield</br>*Merkkijono* | Vain luku | Tietueen yksilöivä tunniste. |
| **Henkilön nimen historia -yksikkötunnus**</br>mshr_dirpersonnamehistoricalentityid</br>*GUID* | Järjestelmän luoma | Järjestelmän muodostama GUID-arvo, jolla tietue tunnistetaan yksilöivästi. |

## <a name="relations"></a>Suhteet

| Ominaisuuden arvo | Liittyvä yksikkö | Siirtymisominaisuus | Kokoelmatyyppi |
| --- | --- | --- | --- |
| Ei käytettävissä | [mshr_payrollemployeeentity](hr-admin-integration-payroll-api-payroll-employee.md) | Ei käytettävissä | mshr_FK_PayrollEmployeeEntity_Name |

## <a name="example-query-for-payroll-employee"></a>Esimerkkikysely palkanlaskennan työntekijälle

**Pyyntö**

```http
GET [Organizaton URI]/api/data/v9.1/mshr_dirpersonnamehistoricalentities?$filter=mshr_partynumber eq 'HR000001606'
```

**Vastaus**

```json
{
    "mshr_firstname": "Agustina",
    "mshr_lastnameprefix": "",
    "mshr_lastname": "Fierro",
    "mshr_middlename": "middle",
    "mshr_validto": "2021-09-10T21:23:53Z",
    "mshr_partynumber": "HR000001606",
    "mshr_primaryfield": "HR000001606 | ",
    "mshr_dirpersonnamehistoricalentityid": "00000832-0000-0000-c12b-014105000000",
    "mshr_validfrom": null
},
{
    "mshr_firstname": "Agustina",
    "mshr_lastnameprefix": "",
    "mshr_lastname": "Fierro",
    "mshr_middlename": "",
    "mshr_validto": "2154-12-31T23:59:59Z",
    "mshr_partynumber": "HR000001606",
    "mshr_primaryfield": "HR000001606 | 9/10/2021 09:23:54 pm",
    "mshr_dirpersonnamehistoricalentityid": "00000832-0000-0000-d20b-000010000000",
    "mshr_validfrom": "2021-09-10T21:23:54Z"
}
```

## <a name="see-also"></a>Lisätietoja

[Palkanlaskennan integroinnin ohjelmointirajapinnan esittely](hr-admin-integration-payroll-api-introduction.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
