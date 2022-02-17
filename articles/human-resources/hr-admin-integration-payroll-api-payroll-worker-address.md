---
title: Palkanlaskennan työntekijän osoite
description: Tämä ohjeaihe sisältää tietoja ja esimerkkikyselyn palkanlaskennan työntekijän osoite -yksikölle Dynamics 365 Human Resourcesissa.
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
ms.openlocfilehash: 70e42cbf657a28327699d927731edd36de7c4a64
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/31/2022
ms.locfileid: "8069754"
---
# <a name="payroll-worker-address"></a>Palkanlaskennan työntekijän osoite


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Tässä aiheessa kuvataan Dynamics 365 Human Resourcesin Palkanlaskennan työntekijän osoite -yksikkö.

Fyysinen nimi: mshr_payrollworkeraddressentity.

### <a name="description"></a>kuvaus

Tämä yksikkö tarjoaa tietyn työntekijän palkanlaskennan asuinsijainnista ja palkanlaskennan työsijainnista.

## <a name="properties"></a>Ominaisuudet

| Ominaisuus</br>**Fyysinen nimi**</br>**_Tyyppi_** | Käytä | Kuvaus |
| --- | --- | --- |
| **Henkilöstönumero**</br>mshr_personnelnumber</br>*Merkkijono* | Vain luku | Työntekijän yksilöivä henkilökuntanumero. |
| **Sijainnin tunnus**</br>mshr_locationidbr>*Merkkijono* | Vain luku | Osoitteen tunnus. |
| **Asui osoitteessa**</br>mshr_islivedinaddressbr </br> *[mshr_NoYes-asetusjoukko](hr-admin-integration-payroll-api-no-yes.md)* | Vain luku | Arvo ilmaisee, asuuko työntekijä kyseisessä osoitteessa. |
| **Työskenteli osoitteessa** </br> mshr_isworkedinaddressbr </br>*[mshr_NoYes-asetusjoukko](hr-admin-integration-payroll-api-no-yes.md)* | Vain luku | Arvo ilmaisee, työskenteleekö työntekijä kyseisessä osoitteessa. |
| **Maa alue**</br>mshr_countryregionid</br>*Merkkijono* | Vain luku</br>Vaadittu | Osoitteelle määritetty maa tai alue. |
| **Postinumero**</br>mshr_zipcode<br>*Merkkijono* | Vain luku | Työntekijälle määritetty tunnusnumero. |
| **Katuosoite**</br>mshr_street</br>*Merkkijono* | Vain luku | Osoitteelle määritetty katu. |
| **Kaupunki**</br>mshr_city</br>*Merkkijono* | Vain luku | Osoitteelle määritetty paikkakunta. |
| **Alue**</br>mshr_state</br>*Merkkijono* | Vain luku | Osoitteelle määritetty osavaltio tai provinssi. |
| **Piirikunta**</br>mshr_county</br>*Merkkijono* | Vain luku | Osoitteelle määritetty maakunta. |
| **Voimassaolo alkaa**</br>mshr_postaladdressvalidfrom</br>*Päivämäärä aika siirros* | Vain luku | Päivämäärä, josta alkaen osoite on voimassa. |
| **Voimassaolo päättyy**</br>mshr_postaladdressvalidto</br>*Päivämäärä aika siirros* | Vain luku | Päivämäärä, johon asti osoite on voimassa. |
| **Ensisijainen kenttä**</br>mshr_primaryfield</br>*Merkkijono* | Vain luku | Ensisijainen kenttä. |
| **Palkanlaskennan työntekijän osoitteen tunnus**</br>mshr_payrollworkeraddressentityid</br>*GUID* | Järjestelmän luoma | Järjestelmän muodostama GUID-arvo, jolla osoite tunnistetaan yksilöivästi. |

## <a name="relations"></a>Suhteet

| Ominaisuuden arvo | Liittyvä yksikkö | Siirtymisominaisuus | Kokoelmatyyppi |
| --- | --- | --- | --- |
| _mshr_fk_worker_id_value | [mshr_payrollemployeeentity](hr-admin-integration-payroll-api-payroll-employee.md) | mshr_FK_Worker_id | mshr_FK_PayrollEmployeeEntity_Address |

## <a name="example-query"></a>Esimerkkikysely

**Pyyntö**

```http
GET [Organizaton URI]/api/data/v9.1/mshr_payrollworkeraddressentities?$filter=mshr_personnelnumber eq @personnelnumber and mshr_postaladdressvalidfrom le @asofdate and mshr_postaladdressvalidto ge @asofdate&@personnelnumber='000041'&@asofdate=2021-04-01
```

**Vastaus**

```json
{
    "mshr_personnelnumber": "000041",
    "mshr_locationid": "000000538",
    "mshr_islivedinaddress": 200000001,
    "mshr_isworkedinaddress": 200000000,
    "mshr_countryregionid": "USA",
    "mshr_zipcode": "99025",
    "mshr_street": "6543 Cypress Ave",
    "mshr_city": "Tacoma",
    "mshr_state": "WA",
    "mshr_county": "KING",
    "mshr_postaladdressvalidfrom": "2012-09-20T20:14:27Z",
    "mshr_postaladdressvalidto": "2154-12-31T23:59:59Z",
    "mshr_primaryfield": "000041 | 000000538 | 9/20/2012 08:14:27 pm",
    "_mshr_fk_worker_id_value": "00000d3c-0000-0000-d5ff-004105000000",
    "mshr_payrollworkeraddressentityid": "000006f0-0000-0000-f90f-014105000000"

}
```

## <a name="see-also"></a>Lisätietoja

[Palkanlaskennan integroinnin ohjelmointirajapinnan esittely](hr-admin-integration-payroll-api-introduction.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
