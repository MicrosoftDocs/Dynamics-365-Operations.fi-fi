---
title: Lomasaldo
description: Tämä artikkelissa sisältää tietoja ja esimerkkikyselyn Lomasaldo-yksikölle Dynamics 365 Human Resourcesissa.
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
ms.openlocfilehash: 4792c316b8b7af3e86b097029eb281af4a10d113
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8899698"
---
# <a name="leave-balance"></a>Lomasaldo


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Tässä artikkelissa kuvataan Dynamics 365 Human Resourcesin Lomasaldo-yksikkö.

### <a name="description"></a>Kuvaus

Tämä yksikkö tarjoaa tietyn työntekijän lomasaldon per lomatyyppi.

Fyysinen nimi: mshr_essleavebalanceentities.

## <a name="properties"></a>Ominaisuudet

| Ominaisuus</br>**Fyysinen nimi**</br>**_Laji_** | Käytä | kuvaus |
| --- | --- | --- |
| **Henkilöstönumero**</br>mshr_personnelnumber</br>*Merkkijono* | Vain luku | Työntekijän yksilöivä henkilökuntanumero. |
| **Nykyinen saldo**</br>mshr_balanceavailable</br>*Desimaali* | Vain luku | Työntekijän nykyinen saldo. |
| **Laji**</br>mshr_balanceavailable</br>*Merkkijono* | Vain luku | Lomatyypin tunnus. |
| **Jaksotushinta**</br>mshr_accrualratedescription</br> | Vain luku | Jaksotussuhde. |
| **Viimeinen siirrettävä summa**</br>mshr_lastcarryforwardamount</br>*Desimaali* | Vain luku | Viimeisin siirtokirjaus -summa. |
| **Otettu tänä vuonna**</br>mshr_takenthisyear</br>*Desimaali* | Vain luku | Tänä vuonna käytetyn loman määrä. |
| **Kuluva vuosi yhteensä**</br>mshr_totalthisyear</br>*Desimaali* | Vain luku | Tämän vuoden kokonaissumma. |
| **Tietoalueen tunnus**</br>mshr_dataareaid_id</br>*Merkkijono* | Vain luku | Määrittää oikeushenkilön (yrityksen). |
| **Ensisijainen kenttä**</br>mshr_primaryfield</br>*GUID* | Vain luku</br>Järjestelmän luoma | |
| **Lomatyypin tunnus**</br>_mshr_fk_leavetype_id_value</br>*GUID* | Vain luku</br>Viiteavain: mshr_essleavetypeentity-yksikön mshr_essleavetypeentityid  | Lomatyypin tunnus |
| **Lomasaldo-yksikkö**</br>mshr_essleavebalanceentityid</br>*GUID* | Järjestelmän luoma | Järjestelmän luoma GUID-arvo, jonka avulla saldo voidaan tunnistaa yksilöivästi. |

## <a name="example-query"></a>Esimerkkikysely

**Pyyntö**

```http
GET [Organizaton URI]/api/data/v9.1/mshr_essleavebalanceentities?$filter=mshr_personnelnumber eq '000013'
```

**Vastaus**

```json
{
    "mshr_personnelnumber": "000013",
    "mshr_balanceavailable": 67.76,
    "mshr_leavetypeid": "PTO",
    "mshr_accrualratedescription": "6.16 hrs / Semimonthly",
    "mshr_lastcarryforwardamount": 0,
    "mshr_takenthisyear": 0,
    "mshr_totalthisyear": 67.76,
    "mshr_dataareaid": "usmf",
    "mshr_primaryfield": "000013 | PTO",
    "_mshr_fk_leavetype_id_value": "00000a6c-0000-0000-0000-005001000000",
    "mshr_essleavebalanceentityid": "0000091f-0000-0000-2703-005001000000",
    "_mshr_dataareaid_id_value": null
},
{
    "mshr_personnelnumber": "000013",
    "mshr_balanceavailable": 80,
    "mshr_leavetypeid": "Sick",
    "mshr_accrualratedescription": "80.00 hrs / Annually",
    "mshr_lastcarryforwardamount": 0,
    "mshr_takenthisyear": 0,
    "mshr_totalthisyear": 80,
    "mshr_dataareaid": "usmf",
    "mshr_primaryfield": "000013 | Sick",
    "_mshr_fk_leavetype_id_value": "00000a6c-0000-0000-ee02-005001000000",
    "mshr_essleavebalanceentityid": "0000091f-0000-0000-3003-005001000000",
    "_mshr_dataareaid_id_value": null
},
{
    "mshr_personnelnumber": "000013",
    "mshr_balanceavailable": 0,
    "mshr_leavetypeid": "Bereavement",
    "mshr_accrualratedescription": "0.00 hrs / Annually",
    "mshr_lastcarryforwardamount": 0,
    "mshr_takenthisyear": 0,
    "mshr_totalthisyear": 0,
    "mshr_dataareaid": "usmf",
    "mshr_primaryfield": "000013 | Bereavement",
    "_mshr_fk_leavetype_id_value": "00000a6c-0000-0000-f402-005001000000",
    "mshr_essleavebalanceentityid": "0000091f-0000-0000-4403-005001000000",
    "_mshr_dataareaid_id_value": null
},
{
    "mshr_personnelnumber": "000013",
    "mshr_balanceavailable": 66.65,
    "mshr_leavetypeid": "Vacation",
    "mshr_accrualratedescription": "13.33 hrs / Monthly",
    "mshr_lastcarryforwardamount": 0,
    "mshr_takenthisyear": 0,
    "mshr_totalthisyear": 66.65,
    "mshr_dataareaid": "usmf",
    "mshr_primaryfield": "000013 | Vacation",
    "_mshr_fk_leavetype_id_value": "00000a6c-0000-0000-f502-005001000000",
    "mshr_essleavebalanceentityid": "0000091f-0000-0000-1009-005001000000",
    "_mshr_dataareaid_id_value": null
}
```

## <a name="see-also"></a>Lisätietoja

[Palkanlaskennan integroinnin ohjelmointirajapinnan esittely](hr-admin-integration-payroll-api-introduction.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
