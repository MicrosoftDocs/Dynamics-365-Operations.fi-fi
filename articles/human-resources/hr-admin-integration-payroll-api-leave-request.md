---
title: Lomapyyntö
description: Tämä artikkelissa sisältää tietoja ja esimerkkikyselyn Lomapyyntö-yksikölle Dynamics 365 Human Resourcesissa.
author: marcelbf
ms.date: 06/25/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: marcelbf
ms.search.validFrom: 2021-06-25
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 47a652d9b7dec15124fc8b62d3c7d0402f88e093
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8899669"
---
# <a name="leave-request"></a>Lomapyyntö


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Tässä artikkelissa kuvataan Dynamics 365 Human Resourcesin Lomapyyntö-yksikkö.

### <a name="description"></a>Kuvaus

Tämä yksikkö tarjoaa tietoja lomapyynnöstä.

Fyysinen nimi: mshr_essleaverequestentity.

## <a name="properties"></a>Ominaisuudet

| Ominaisuus</br>**Fyysinen nimi**</br>**_Laji_** | Käytä | kuvaus |
| --- | --- | --- |
| **Pyynnön tunnus**</br>mshr_requestid</br>*Merkkijono* | Vain luku | Pyynnön tunnus. |
| **Lomatyypin tunnus**</br>mshr_leavetypeid</br>*Merkkijono* | Vain luku | Lomatyypin tunnus. |
| **Päivämäärä**</br>mshr_leavedate</br>*Päivämäärä aika siirros* | Vain luku | Lomapyynnön päivämäärä. |
| **summa**</br>mshr_amount</br>*Desimaali* | Vain luku | Lomapyynnön summa. |
| **Puoli päivää -tyyppi**</br>mshr_halfdaydefinition</br>*mshr_LeaveHalfDayDefinition-asetusjoukko* | Vain luku | Puolipäivävapaan tyyppi. |
| **Kommentti**</br>mshr_comment</br>*Merkkijono* | Vain luku | Pyynnön kommentti. |
| **Tila**</br>mshr_status</br>*mshr_status-asetusjoukko* | Vain luku | Pyynnön tila. |
| **Päivämäärä**</br>mshr_requestdate</br>*Päivämäärä aika siirros* | Vain luku | Pyynnön päivämäärä. |
| **Henkilöstönumero**</br>mshr_personnelnumber</br>*Merkkijono* | Vain luku | Työntekijän yksilöivä henkilökuntanumero. |
| **Syykoodin tunnus**</br>mshr_reasoncodeid</br>*Merkkijono* | Vain luku | Syykoodin tunnus. |
| **Tietoalueen tunnus**</br>mshr_dataareaid</br>*Merkkijono* | Vain luku | Määrittää oikeushenkilön (yrityksen). |
| **Ensisijainen kenttä**</br>mshr_primaryfield</br>*GUID* | Vain luku</br>Järjestelmän luoma | |
| **Lomatyyppi-yksikkö**</br>mshr_essleaverequestentityid</br>*GUID* | Järjestelmän luoma | Järjestelmän luoma GUID-arvo, jonka avulla lomapyyntö voidaan tunnistaa yksilöivästi. |

## <a name="example-query"></a>Esimerkkikysely

**Pyyntö**

```http
GET [Organizaton URI]/api/data/v9.1/mshr_essleaverequestentities?$filter=mshr_personnelnumber eq '000020'
```

**Vastaus**

```json
{
    "mshr_requestid": "USMF-000001",
    "mshr_leavetype": "PTO",
    "mshr_leavedate": "2017-01-02T00:00:00Z",
    "mshr_amount": 8,
    "mshr_halfdaydefinition": 200000000,
    "mshr_comment": "Taking a week off to relax",
    "mshr_status": 200000009,
    "mshr_requestdate": "2017-07-31T00:00:00Z",
    "mshr_personnelnumber": "000020",
    "mshr_reasoncodeid": "",
    "mshr_dataareaid": "usmf",
    "mshr_primaryfield": "USMF-000001 | PTO | 1/2/2017",
    "mshr_essleaverequestentityid": "000004dd-0000-0000-0f00-005001000000",
    "_mshr_dataareaid_id_value": null
}
```

## <a name="see-also"></a>Lisätietoja

[Palkanlaskennan integroinnin ohjelmointirajapinnan esittely](hr-admin-integration-payroll-api-introduction.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
