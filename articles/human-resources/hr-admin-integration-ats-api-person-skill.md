---
title: Henkilön osaamisalue
description: Tässä aiheessa kuvataan Dynamics 365 Human Resourcesin Henkilön osaamisalue -yksikköä.
author: jaredha
ms.date: 02/05/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2021-02-05
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 03181d6377fdacee0faa600551e8b7ad7c68a76d
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/18/2021
ms.locfileid: "6059229"
---
# <a name="person-skill"></a>Henkilön osaamisalue

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Tässä aiheessa kuvataan Dynamics 365 Human Resourcesin Henkilön osaamisalue -yksikköä.

Fyysinen nimi: mshr_hcmpersonskillentity

## <a name="description"></a>kuvaus

Tämä yksikkö kuvaa hakijan osaamisalueita.

## <a name="json-representation"></a>JSON-esitys

```json
{
    "mshr_certifier": "String",
    "mshr_partynumber": "String",
    "mshr_levelid": "String",
    "mshr_ratinglevelexaminer": "String",
    "mshr_skillid": "String",
    "mshr_ratingid": "String",
    "mshr_leveltype": Int,
    "mshr_yearsofexperience": Decimal,
    "mshr_verified": Int,
    "mshr_leveldate": "Date",
    "mshr_primaryfield": "String",
    "_mshr_fk_certifier_id_value": "Guid",
    "_mshr_fk_person_id_value": "Guid",
    "_mshr_fk_ratinglevel_id_value": "Guid",
    "_mshr_fk_ratinglevelexaminer_id_value": "Guid",
    "_mshr_fk_skill_id_value": "Guid",
    "mshr_hcmpersonskillentityid": "Guid"
}
```

## <a name="properties"></a>Ominaisuudet

| Ominaisuus<br>**Fyysinen nimi**<br>**_Laji_** | Käytä | kuvaus |
| --- | --- | --- |
| **Henkilön osaamisalueen yksikkötunnus**<br>mshr_hcmpersonskillentityid<br>*GUID* | Vain luku<br>Vaadittu | Järjestelmän luoma yksikkötietueen yksilöivä tunnus. |
| **Osapuolinumero**<br>mshr_partynumber<br>*Merkkijono* | Luku/Kirjoitus<br>Vaadittu |   Liittyvän osapuolen (henkilön) tietueen tunnus. |
| **Henkilötunnuksen arvo**<br>_mshr_fk_person_id_value<br>*GUID* | Vain luku<br>Vaadittu<br>Viiteavain: mshr_dirpersonentity-yksikön mshr_dirpersonentityid | Järjestelmän luoma osapuolen (henkilön) yksikkötietueen tunnus. |
| **Sertifioija**<br>mshr_certifier<br>*Merkkijono* | Luku/Kirjoitus<br>Valinnainen | Osaamisalueen todentaneen työntekijän henkilökuntanumero. |
| **Sertifioijan tunnuksen arvo**<br>_mshr_fk_certifier_id_value<br>*GUID* | Vain luku<br>Valinnainen<br>Viiteavain: mshr_hcmworkerentity-yksikön mshr_hcmworkerentityid | Osaamisalueen todentaneen työntekijän tietueen järjestelmän luoma yksilöivä tunnus. |
| **Osaamisaluetunnus**<br>mshr_skillid<br>*Merkkijono* | Luku/Kirjoitus<br>Vaadittu | Human Resourcesin osaamisalueen tunnus. |
| **Osaamisaluetunnuksen arvo**<br>_mshr_fk_skill_id_value<br>*GUID* | Vain luku<br>Vaadittu<br>Viiteavain: mshr_hcmskillentity-yksikön mshr_hcmskillentityid | Järjestelmän luoma valitun osaamisalueen tunnus. |
| **Kokemus vuosina**<br>mshr_yearsofexperience<br>*Desimaali* | Luku/Kirjoitus<br>Valinnainen | Hakijan tämän osaamisalueen kokemus vuosina. |
| **Luokitustunnus**<br>mshr_ratingid<br>*Merkkijono* | Luku/Kirjoitus<br>Vaadittu | Arviointiasteikon tyyppi. Tälle yksikölle arvo on **Osaamisalueet**. |
| **Tasotyyppi**<br>mshr_leveltype<br>*mshr_hrmskillleveltype-asetusjoukko* | Luku/Kirjoitus<br>Vaadittu | Osaamisaluetasolle määritetty tyyppiluokitus. |
| **Tason tunnus**<br>mshr_levelid<br>*Merkkijono* | Luku/Kirjoitus<br>Vaadittu | Sen luokitustason tunnus, jolla hakijalla on tämä osaamisalue. |
| **Luokitustason tunnuksen arvo**<br>_mshr_fk_ratinglevel_id_value<br>*GUID* | Vain luku<br>Vaadittu<br>Viiteavain: mshr_hcmratinglevelentity-yksikön mshr_hcmratinglevelentityid | Järjestelmän luoma luokitustason tunnus. |
| **Tason päivämäärä**<br>mshr_leveldate<br>*Datetime* | Luku/Kirjoitus<br>Vaadittu | Päivämäärä, jolloin hakijan osaamisalue on luokiteltu. |
| **Luokitustason tarkastaja**<br>mshr_ratinglevelexaminer<br>*Merkkijono* | Luku/Kirjoitus<br>Valinnainen | Ehdokkaan luokitelleen työntekijän henkilökuntanumero. |
| **Luokitustason tarkastajan tunnuksen arvo**<br>_mshr_fk_ratinglevelexaminer_id_value<br>*GUID* | Vain luku<br>Valinnainen<br>Viiteavain: mshr_hcmworkerentity-yksikön mshr_hcmworkerentityid | Järjestelmän luoma sen työntekijän tunnus, joka tarkasti hakijan osaamistason. |
| **Tarkistettu**<br>mshr_verified<br>*mshr_noyes-asetusjoukko* | Luku/Kirjoitus<br>Vaadittu | Ilmaisee, onko arvioitu osaamisaluetaso varmennettu. |
| **Ensisijainen kenttä**<br>mshr_primaryfield<br>*Merkkijono* | Vain luku<br>Vaadittu | Kenttä, jota käytetään yksikkötietueen tunnuksena. Osapuolen numeron, tason tyypin, osaamisaluetunnuksen ja tason päivämäärän yhdistelmä. |

## <a name="see-also"></a>Lisätietoja

[Hakijan seurantajärjestelmän integroinnin sovellusliittymän esittely](hr-admin-integration-ats-api-introduction.md)<br>
[Esimerkkikysely palkattavalle hakijalle](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]