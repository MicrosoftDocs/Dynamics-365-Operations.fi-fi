---
title: Luokitustaso
description: Tässä artikkelissa kuvataan Dynamics 365 Human Resourcesin Luokitustaso-yksikköä.
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
ms.openlocfilehash: dcd366632456c186eca9682d79a0c8690772e8bc
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8893871"
---
# <a name="rating-level"></a>Luokitustaso


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Tässä artikkelissa kuvataan Dynamics 365 Human Resourcesin Luokitustaso-yksikköä.

Fyysinen nimi: mshr_hcmratinglevelentity

## <a name="description"></a>kuvaus

Tämä yksikkö tarjoaa käytettävissä olevat osaamisalueluokituksen tasot. Luokitustasoja käytetään kaikissa yrityksissä.

## <a name="json-representation"></a>JSON-esitys

```json
{
    "mshr_description": "String",
    "mshr_factor": Int,
    "mshr_note": "String",
    "mshr_ratinglevelid": "String",
    "mshr_ratingmodelid": "String",
    "mshr_primaryfield": "String",
    "_mshr_fk_ratingmodelentity_id_value": "Guid",
    "mshr_hcmratinglevelentityid": "Guid"
}
```

## <a name="properties"></a>Ominaisuudet

| Ominaisuus<br>**Fyysinen nimi**<br>**_Laji_** | Käytä | kuvaus |
| --- | --- | --- |
| **Luokitustason yksikön tunnus**<br>mshr_hcmratinglevelentityid<br>*GUID* | Vain luku<br>Vaadittu<br>Järjestelmän luoma | Järjestelmän luoma tason yksilöivä tunnus. |
| **Luokitustason tunnus**<br>mshr_ratinglevelid<br>*Merkkijono* | Luku/Kirjoitus<br>Vaadittu | Käyttäjän luettava tason yksilöivä tunnus. |
| **Luokitusmallin tunnus**<br>mshr_ratingmodelid<br>*Merkkijono* | Luku/Kirjoitus<br>Vaadittu | Luokitusmalli, johon luokitustaso kuuluu. |
| **Luokitusmallin yksikön tunnus**<br>_mshr_fk_ratingmodelentity_id_value<br>*GUID* | Vain luku<br>Vaadittu<br>Viiteavain: mshr_hcmratingmodelentity-yksikön mshr_hcmratingmodelentityid | Järjestelmän luoma sen luokitusmallin tunnus, johon luokitustaso kuuluu. |
| **Kuvaus**<br>mshr_description<br>*Merkkijono* | Luku/Kirjoitus<br>Vaadittu | Luokitustason kuvaus. |
| **Kerroin**<br>mshr_factor<br>*Kokonaisluku* | Luku/Kirjoitus<br>Vaadittu | Luokitustason kerroin. Kun vertaat nimikkeitä, joissa on eri määrä tasoja, kerrointa käytetään tulosten normalisointiin. Arvon on oltava kokonaisluku väliltä 0–9. |
| **Huomautus**<br>mshr_note<br>*Merkkijono* | Luku/Kirjoitus<br>Valinnainen | Luokitustasoon liittyvät huomautukset. |
| **Ensisijainen kenttä**<br>mshr_primaryfield<br>*Merkkijono* | Vain luku<br>Vaadittu | Kenttä, jota käytetään yksikkötietueen tunnuksena. Luokitustason tunnuksen ja luokitusmallin tunnuksen yhdistelmä. |

## <a name="see-also"></a>Lisätietoja

[Hakijan seurantajärjestelmän integroinnin sovellusliittymän esittely](hr-admin-integration-ats-api-introduction.md)<br>
[Esimerkkikysely palkattavalle hakijalle](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
