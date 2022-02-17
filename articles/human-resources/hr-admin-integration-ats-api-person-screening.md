---
title: Henkilön seulonta
description: Tässä aiheessa kuvataan Dynamics 365 Human Resourcesin Henkilön seulonta -yksikköä.
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
ms.openlocfilehash: 5129348f928fd709a5fabe73917522799a2d47e0
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/31/2022
ms.locfileid: "8066290"
---
# <a name="person-screening"></a>Henkilön seulonta


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Tässä aiheessa kuvataan Dynamics 365 Human Resourcesin Henkilön seulonta -yksikköä.

Fyysinen nimi: mshr_hcmpersonscreeningentity

## <a name="description"></a>kuvaus

Tässä yksikössä kuvataan seulonnat, jotka hakija on läpäissyt tai jotka hänen pitää läpäistä työpaikkaa varten.

## <a name="json-representation"></a>JSON-esitys

```json
{
    "mshr_note": "String",
    "mshr_requiredby": "Date",
    "mshr_status": Int,
    "mshr_partynumber": "String",
    "mshr_screeningtypeid": "String",
    "mshr_primaryfield": "String",
    "_mshr_fk_person_id_value": "Guid",
    "mshr_hcmpersonscreeningentityid": "Guid",
    "mshr_completeddate": "Date"
}
```

## <a name="properties"></a>Ominaisuudet

| Ominaisuus<br>**Fyysinen nimi**<br>**_Laji_** | Käytä | kuvaus |
| --- | --- | --- |
| **Henkilön seulonnan yksikkötunnus**<br>mshr_hcmpersonscreeningentityid<br>*GUID* | Vain luku<br>Vaadittu<br>Järjestelmän luoma | Henkilön seulontatietueen yksilöivä ensisijainen tunnus. |
| **Osapuolinumero**<br>mshr_partynumber<br>*Merkkijono* | Luku/Kirjoitus<br>Vaadittu | Hakijan osapuolen (henkilön) numero. |
| **Henkilötunnuksen arvo**<br>_mshr_fk_person_id_value<br>*GUID* | Vain luku<br>Vaadittu<br>Viiteavain: mshr_dirpersonentity-yksikön mshr_dirpersonentityid | Järjestelmän luoma osapuolen (henkilön) yksikkötietueen tunnus. |
| **Seulontatyypin tunnus**<br>mshr_screeningtypeid<br>*Merkkijono* | Luku/Kirjoitus<br>Vaadittu<br>Viiteavain: ScreeningType | Human Resourcesin seulontatyypin tunnus. |
| **Seulontatyypin tunnuksen arvo**<br>_mshr_fk_screeningtype_id_value<br>*GUID* | Vain luku<br>Vaadittu<br>Viiteavain: mshr_hcmscreeningtypeentity-yksikön mshr_hcmscreeningtypeentityid | Järjestelmän luoma seulontatyypin tietueen tunnus liitetyssä yksikössä. |
| **Määräpäivä**<br>mshr_requiredby<br>*Datetime* | Luku/Kirjoitus<br>Valinnainen | Päivämäärä, johon mennessä seulonnat on suoritettava loppuun. |
| **Tila**<br>mshr_status<br>*mshr_hcmcompletionstatus-asetusjoukko*<br>Luku/Kirjoitus<br>Vaadittu | Hakijan tila seulonnalle. |
| **Valmistumispäivämäärä**<br>mshr_completeddate<br>*Datetime* | Luku/Kirjoitus<br>Valinnainen | Päivämäärä, jolloin seulonta suoritettiin loppuun. |
| **Muistiinpanot**<br>mshr_note<br>*Merkkijono* | Luku/Kirjoitus<br>Valinnainen | Muistiinpanot rekrytoijan ja työhönottopäällikön käyttöön. |

## <a name="see-also"></a>Lisätietoja

[Hakijan seurantajärjestelmän integroinnin sovellusliittymän esittely](hr-admin-integration-ats-api-introduction.md)<br>
[Esimerkkikysely palkattavalle hakijalle](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
