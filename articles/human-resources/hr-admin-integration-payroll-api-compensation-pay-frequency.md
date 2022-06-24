---
title: Kompensaation maksutiheys
description: Tässä artikkelissa on Dynamics 365 Human Resourcesin Kompensaation maksutiheys -yksikköä koskevia tietoja ja esimerkkikysely.
author: marcelbf
ms.date: 09/01/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: marcelbf
ms.search.validFrom: 2021-09-01
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 9afe27776797b2355a32226bbd7fa514b5c5d962
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8894611"
---
# <a name="compensation-pay-frequency"></a>Kompensaation maksutiheys


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Tässä artikkelissa käsitellään Dynamics 365 Human Resourcesin Kompensaation maksutiheys -yksikköä.

Fyysinen nimi: mshr_hcmpayrateconversionentity.

### <a name="description"></a>Kuvaus

Yksikössä on tietoja tietyn kompensaation maksutiheyden palkkion muunnoksesta.

## <a name="properties"></a>Ominaisuudet

| Ominaisuus</br>**Fyysinen nimi**</br>**_Tyyppi_** | Käytä | Kuvaus |
| --- | --- | --- |
| **Vuosipalkan muunto**</br>mshr_annualconversionfactor</br>*Desimaali* | Vain luku | Toimitustiheyden vuosittainen muuntokerroin. |
| **Kuvaus**</br>mshr_description</br>*Merkkijono* | Vain luku | Muuntokurssin kuvaus. |
| **Tuntipalkan muunto**</br>mshr_hourlyconversionfactor</br>*Desimaali* | Vain luku | Maksutiheyden tuntikohtainen muuntokerroin. |
| **Kuukausipalkan muunto**</br>mshr_monthlyconversionfactor</br>*Desimaali* | Vain luku | Toimitustiheyden kuukausittainen muuntokerroin. |
| **Palkkion muunnos**</br>mshr_payrateconversion</br>*Merkkijono* | Vain luku | Muuntokurssin yksilöivä merkkijono. |
| **Jakso**</br>mshr_period</br>*kausiasetusjoukko* | Vain luku | Tietyn palkkion muunnon pääkausi. |
| **Viikkopalkan muunto**</br>mshr_weeklyconversionfactor</br>*Desimaali* | Vain luku | Maksutiheyden viikoittainen muuntokerroin. |
| **Tietoalueen tunnus**</br>mshr_dataareaid</br>*Merkkijono* | Vain luku | Yritys (yhtiö). |
| **Kompensaation maksutiheys -yksikön tunnus**</br>mshr_dirpersonnamehistoricalentityid</br>*GUID* | Järjestelmän luoma | Järjestelmän muodostama GUID-arvo, jolla tietue tunnistetaan yksilöivästi. |

## <a name="example-query-for-payroll-employee"></a>Esimerkkikysely palkanlaskennan työntekijälle

**Pyyntö**

```http
GET [Organizaton URI]/api/data/v9.1/mshr_hcmpayrateconversionentities?$filter=mshr_payrateconversion eq 'Annual' and mshr_dataareaid eq 'usmf'
```

**Vastaus**

```json
{
    "mshr_annualconversionfactor": 1,
    "mshr_description": "Annual",
    "mshr_hourlyconversionfactor": 0.0004807692,
    "mshr_monthlyconversionfactor": 0.0833333333,
    "mshr_payrateconversion": "Annual",
    "mshr_period": 200000000,
    "mshr_weeklyconversionfactor": 0.0192307692,
    "mshr_dataareaid": "usmf",
    "mshr_hcmpayrateconversionentityid": "0000056e-0000-0000-b027-fef003000000",
    "_mshr_dataareaid_id_value": null
}
```

## <a name="see-also"></a>Lisätietoja

[Palkanlaskennan integroinnin ohjelmointirajapinnan esittely](hr-admin-integration-payroll-api-introduction.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
