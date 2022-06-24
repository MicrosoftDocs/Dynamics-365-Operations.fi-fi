---
title: Lomatyyppi
description: Tämä artikkelissa sisältää tietoja ja esimerkkikyselyn Lomatyyppi-yksikölle Dynamics 365 Human Resourcesissa.
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
ms.openlocfilehash: 6e7905989df92e943b86f86194c87dcb2a7b1446
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8893783"
---
# <a name="leave-type"></a>Lomatyyppi


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Tässä artikkelissa kuvataan Dynamics 365 Human Resourcesin Lomatyyppi-yksikkö.

### <a name="description"></a>Kuvaus

Tämä yksikkö tarjoaa tietoja lomatyypistä.

Fyysinen nimi: mshr_essleavetypeentity.

## <a name="properties"></a>Ominaisuudet

| Ominaisuus</br>**Fyysinen nimi**</br>**_Laji_** | Käytä | kuvaus |
| --- | --- | --- |
| **Lomatyypin tunnus**</br>mshr_leavetypeid</br>*Merkkijono* | Vain luku | Lomatyypin tunnus. |
| **Kuvaus**</br>mshr_description</br>*Merkkijono* | Vain luku | Lomatyypin kuvaus. |
| **Luokka**</br>mshr_category</br>*mshr_LeaveTypeCategory-asetusjoukko* | Vain luku | Lomatyypin luokka. |
| **Syykoodi on pakollinen**</br>mshr_isreasoncoderequired</br>*mshr_NoYes-asetusjoukko* | Vain luku | Määrittää, vaatiiko lomatyyppi syykoodin. |
| **Loman yhtenäisyys**</br>mshr_leaveamountunit</br>*mshr_LeaveAmountUnit-asetusjoukko* | Vain luku | Tämän lomatyypin yhtenäisyys. |
| **Ota puolikkaat päivät käyttöön**</br>mshr_enablehalfdaydefinition</br>*mshr_NoYes-asetusjoukko* | Määrittää, ovatko puolikkaat päivät käytössä lomatyypille. |
| **Tietoalueen tunnus**</br>mshr_dataareaid_id</br>*Merkkijono* | Vain luku | Määrittää oikeushenkilön (yrityksen). |
| **Lomatyyppi-yksikkö**</br>mshr_essleavetypeentityid</br>*GUID* | Järjestelmän luoma | Järjestelmän luoma GUID-arvo, jonka avulla lomatyyppi voidaan tunnistaa yksilöivästi. |

## <a name="example-query"></a>Esimerkkikysely

**Pyyntö**

```http
GET [Organizaton URI]/api/data/v9.1/mshr_essleavetypeentities?$filter=mshr_leavetypeid eq 'PTO'
```

**Vastaus**

```json
{
    "mshr_leavetypeid": "PTO",
    "mshr_description": "Paid time off",
    "mshr_category": 200000000,
    "mshr_isreasoncoderequired": 200000000,
    "mshr_leaveamountunit": 200000000,
    "mshr_enablehalfdaydefinition": 200000000,
    "mshr_dataareaid": "usmf",
    "mshr_essleavetypeentityid": "00000a6c-0000-0000-0000-005001000000",
    "_mshr_dataareaid_id_value": null
}
```

## <a name="see-also"></a>Lisätietoja

[Palkanlaskennan integroinnin ohjelmointirajapinnan esittely](hr-admin-integration-payroll-api-introduction.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
