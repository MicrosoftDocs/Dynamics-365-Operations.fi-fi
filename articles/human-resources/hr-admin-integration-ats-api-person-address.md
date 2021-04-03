---
title: Henkilön osoite
description: Tässä aiheessa kuvataan Dynamics 365 Human Resourcesin Henkilön osoite -yksikköä.
author: jaredha
manager: tfehr
ms.date: 02/05/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2021-02-05
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 0bca48c9e980f95e4dd72a075b34824331ae05dc
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/17/2021
ms.locfileid: "5466541"
---
# <a name="person-address"></a>Henkilön osoite

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Tässä aiheessa kuvataan Dynamics 365 Human Resourcesin Henkilön osoite -yksikköä.

Fyysinen nimi: mshr_hcmpersonaddressentities

## <a name="description"></a>kuvaus

Tämä yksikkö sisältää hakijatietueiden postinumeroiden luettelon.

## <a name="json-representation"></a>JSON-esitys

```json
{
    "mshr_partynumber": "String",
    "mshr_locationid": "String",
    "mshr_description": "String",
    "mshr_roles": "String",
    "mshr_countryregionid": "String",
    "mshr_zipcode": "String",
    "mshr_street": "String",
    "mshr_city": "String",
    "mshr_state": "String",
    "mshr_county": "String",
    "mshr_isprimary": Int,
    "mshr_isprivate": Int,
    "mshr_primaryfield": "String",
    "_mshr_fk_person_id_value": "Guid",
    "_mshr_fk_countryregion_id_value": "Guid",
    "mshr_hcmpersonaddressentityid": "Guid"
}
```

## <a name="properties"></a>Ominaisuudet

| Ominaisuus<br>**Fyysinen nimi**<br>**_Laji_** | Käytä | kuvaus |
| --- | --- | --- |
| **Henkilön osoitteen yksikkötunnus**<br>mshr_hcmpersonaddressentityid<br>*Merkkijono* | Vain luku<br>Vaadittu | Järjestelmän luoma yksikkötietueen yksilöivä tunnus. |
| **Osapuolinumero**<br>mshr_partynumber<br>*Merkkijono* | Luku/Kirjoitus<br>Vaadittu | Liittyvän osapuolen (henkilön) tietueen tunnus. |
| **Henkilötunnuksen arvo**<br>_mshr_fk_person_id_value<br>*GUID* | Vain luku<br>Vaadittu<br>Viiteavain: mshr_dirpersonentity-yksikön mshr_dirpersonentityid | Järjestelmän luoma osapuolen (henkilön) yksikkötietueen tunnus. |
| **Sijainnin tunnus**<br>mshr_locationid<br>*Merkkijono* | Luku/Kirjoitus<br>Vaadittu | Osoitetietueen sijaintitunnus. Määirtä mshr_logisticspostaladdresslocationcdsentity-yksikössä. |
| **Kuvaus**<br>mshr_description<br>*Merkkijono* | Luku/Kirjoitus<br>Vaadittu | Hakijan osoitteen kuvaus. |
| **Roolit**<br>mshr_roles<br>*Merkkijono* | Luku/Kirjoitus<br>Vaadittu | Osoitteeseen liitetyt roolit. Rooleja voi määrittää useita. Kukin rooli tulee erottaa toisistaan puolipisteellä. mshr_logisticslocationroleentity-yksikkö sisältää voimassa olevat arvot. |
| **Katu**<br>mshr_street<br>*Merkkijono* | Luku/Kirjoitus<br>Valinnainen | Kadunnumero. |
| **Paikkakunta**<br>mshr_city<br>*Merkkijono* | Luku/Kirjoitus<br>Valinnainen | Osoitteen paikkakunta. Määritetään mshr_logisticsaddresscityentity-yksikössä. |
| **Alue**<br>mshr_state<br>*Merkkijono* | Luku/Kirjoitus<br>Valinnainen | Osoitteen osavaltio. Määritetään mshr_logisticsaddressstateentity-yksikössä. |
| **Lääni**<br>mshr_county<br>*Merkkijono* | Luku/Kirjoitus<br>Valinnainen | Osoitteen alue. Määritetään mshr_logisticsaddresscountyentity-yksikössä. |
| **Postinumero**<br>mshr_zipcode<br>*Merkkijono* | Luku/Kirjoitus<br>Valinnainen | Osoitteen postinumero. Määritetään mshr_logisticsaddresspostalcodeentity-yksikössä. |
| **Maan/alueen tunnus**<br>mshr_countryregionid<br>*Merkkijono* | Luku/Kirjoitus<br>Valinnainen | Osoitteen maa tai alue. |
| **Maan/alueen tunnuksen arvo**<br>_mshr_fk_countriregion_id_value<br>*GUID* | Vain luku<br>Valinnainen<br>Viiteavain: mshr_logisticsaddresscountryregionentity-yksikön mshr_logisticaddresscountryregionentityid | Järjestelmän luoma osoitteen maan/alueen yksilöivä tunnus. |
| **On ensisijainen**<br>mshr_isprimary<br>*mshr_noyes-asetusjoukko* | Luku/Kirjoitus<br>Vaadittu | Määrittää, onko tämä osoite määritetyn roolin henkilön ensisijainen osoite. |
| **On yksityinen**<br>mshr_isprivate<br>*mshr_noyes-asetusjoukko* | Luku/Kirjoitus<br>Vaadittu | Määrittää, onko tämä osoite henkilön yksityinen osoite. |
| **Ensisijainen kenttä**<br>mshr_primaryfield<br>*Merkkijono* | Vain luku<br>Vaadittu | Kenttä, jota käytetään yksikkötietueen ensisijaisena tunnuksena. Osapuolen numeron ja sijainnin tunnuksen yhdistelmä. |

## <a name="see-also"></a>Lisätietoja

[Hakijan seurantajärjestelmän integroinnin sovellusliittymän esittely](hr-admin-integration-ats-api-introduction.md)<br>
[Esimerkkikysely palkattavalle hakijalle](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]