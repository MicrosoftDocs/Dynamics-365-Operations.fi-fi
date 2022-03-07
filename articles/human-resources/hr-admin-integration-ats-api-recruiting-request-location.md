---
title: Työhönottopyynnön sijainti
description: Tässä aiheessa kuvataan työhönottopyynnön sijainnin yksikköä Dynamics 365 Human Resourcesissa.
author: jaredha
ms.date: 02/05/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2021-02-05
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: f22926292690cb23d9d19cf3887a005b71d44c8d
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2021
ms.locfileid: "5789657"
---
# <a name="recruiting-request-location"></a>Työhönottopyynnön sijainti

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Tässä aiheessa kuvataan työhönottopyynnön sijainnin yksikköä Dynamics 365 Human Resourcesissa.

Fyysinen nimi: mshr_hcmrecruitingrequestlocationentity

### <a name="description"></a>kuvaus

Niiden sijaintien luettelo, jotka on määritetty sijainneiksi, joissa rekrytoidyt työntekijät tulevat työskentelemään palkkauksen jälkeen. Nämä ovat eri yrityksille luotuja sijainteja.

### <a name="json-representation"></a>JSON-esitys

```
{
    "mshr_recruitingrequestlocationid": "String",
    "mshr_locationid": "String",
    "mshr_description": "String",
    "mshr_countryregionid": "String",
    "mshr_zipcode": "String",
    "mshr_street": "String",
    "mshr_city": "String",
    "mshr_state": "String",
    "mshr_county": "String",
    "mshr_telephone": "String",
    "mshr_email": "String",
    "mshr_internetaddress": "String",
    "_mshr_dataareaid_id_value": "Guid",
    "mshr_dataareaid": "String",
    "_mshr_fk_countryregion_id_value": "Guid",
    "mshr_hcmrecruitingrequestlocationentityid": "Guid"
}
```

### <a name="properties"></a>Ominaisuudet

| Ominaisuus<br>**Fyysinen nimi**<br>**_Laji_** | Käytä | kuvaus |
| --- | --- | --- |
| **Sijainnin tunnus**<br>mshr_locationid<br>*Merkkijono* | Kirjoita kerran<br>Vaadittu | Järjestelmän luoma, käyttäjän luettava rekrytointisijainnin tunnus. |
| **Työhönottopyynnön sijainti**<br>mshr_recruitingrequestlocationid<br>*Merkkijono* | Kirjoita kerran<br>Vaadittu | Käyttäjän määrittämä työhönottosijainnin yksilöivä tunnus. |
| **Työhönottopyynnön sijainnin yksikön tunnus**<br>mshr_hcmrecruitingrequestlocationentityid<br>*GUID* | Vain luku<br>Vaadittu | Järjestelmän luoma työhönottopyynnön sijainnin tietueen yksilöivä tunnus. |
| **Kuvaus**<br>mshr_description<br>*Merkkijono* | Luku/Kirjoitus<br>Vaadittu | Sijainnin kuvaus. |
| **Maan/alueen tunnus**<br>mshr_countryregionid<br>*Merkkijono* | Vain luku<br>Valinnainen | Määrittää maan/alueen, jossa hakijalla on kansalaisuus. |
| **Maan/alueen tunnuksen arvo**<br>_mshr_fk_countriregion_id_value<br>*GUID* | Vain luku<br>Valinnainen<br>Viiteavain: mshr_logisticsaddresscountryregionentity-yksikön mshr_logisticaddresscountryregionentityid | Järjestelmän luoma osoitteen maan/alueen yksilöivä tunnus. |
| **Postinumero**<br>mshr_zipcode<br>*Merkkijono* | Vain luku<br>Valinnainen | Postinumero. |
| **Katu**<br>mshr_street<br>*Merkkijono* | Vain luku<br>Valinnainen | Katuosoite. |
| **Paikkakunta**<br>mshr_city<br>*Merkkijono* | Vain luku<br>Valinnainen | Paikkakunta. |
| **Alue**<br>mshr_state<br>*Merkkijono* | Vain luku<br>Valinnainen | Osavaltio tai provinssi. |
| **Lääni**<br>mshr_county<br>*Merkkijono* | Vain luku<br>Valinnainen | Lääni. |
| **Puhelin**<br>mshr_telephone<br>*Merkkijono* | Luku/Kirjoitus<br>Valinnainen | Sijainnin puhelinnumero. |
| **Sähköposti**<br>mshr_email<br>*Merkkijono* | Luku/Kirjoitus<br>Valinnainen | Sähköpostiosoite. |
| **Internet-osoite**<br>mshr_internetaddress<br>*Merkkijono* | Luku/Kirjoitus<br>Valinnainen | Sijainnin verkkosivuston URL-osoite. |
| **Tietoalueen tunnus**<br>mshr_dataareaid<br>*Merkkijono* | Luku/Kirjoitus<br>Valinnainen | Määrittää oikeushenkilön (yrityksen). |
| **Tietoalueen tunnuksen arvo**<br>_mshr_dataareaid_id_value<br>*GUID* | Vain luku<br>Valinnainen<br>Viiteavain: cdm_companyid of cdm_company-yksikkö | Järjestelmän luoma GUID-tunnus, joka yksilöi oikeushenkilön (yrityksen). |

## <a name="see-also"></a>Lisätietoja

[Hakijan seurantajärjestelmän integroinnin sovellusliittymän esittely](hr-admin-integration-ats-api-introduction.md)<br>
[Esimerkkikysely työhönottopyyntöä varten](hr-admin-integration-ats-api-recruiting-request-example-query.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]