---
title: Henkilön seulonta
description: Tässä artikkelissa kuvataan Dynamics 365 Human Resourcesin Henkilön seulonta -yksikköä.
author: jaredha
ms.date: 12/05/2022
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
ms.openlocfilehash: 3c316e0381f4d407ed7c4c39b5949717b71477bd
ms.sourcegitcommit: 0c927fcb3afd34d870391f05b5393a4673d916e5
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/08/2022
ms.locfileid: "9831887"
---
# <a name="person-screening"></a>Henkilön seulonta


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Tässä artikkelissa kuvataan Dynamics 365 Human Resourcesin Henkilön seulonta -yksikköä.

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
    "_mshr_fk_screeningtype_id_value": "Guid",
    "mshr_primaryfield": "String",
    "_mshr_fk_person_id_value": "Guid",
    "mshr_hcmpersonscreeningentityid": "Guid",
    "mshr_completeddate": "Date"
}
```

## <a name="properties"></a>Ominaisuudet

| Ominaisuus<br>**Fyysinen nimi**<br>**_Tyyppi_** | Käytä | kuvaus |
| --- | --- | --- |
| **Muistiinpanot**<br>mshr_note<br>*Merkkijono* | Luku/Kirjoitus<br>Valinnainen | Muistiinpanot rekrytoijan ja työhönottopäällikön käyttöön. |
| **Määräpäivä**<br>mshr_requiredby<br>*Datetime* | Luku/Kirjoitus<br>Valinnainen | Päivämäärä, johon mennessä seulonnat on suoritettava loppuun. |
| **Tila**<br>mshr_status<br>*mshr_hcmcompletionstatus-asetusjoukko*|Luku/Kirjoitus<br>Pakollinen | Hakijan tila seulonnalle. |
| **Osapuolinumero**<br>mshr_partynumber<br>*Merkkijono* | Luku/Kirjoitus<br>Pakollinen | Hakijan osapuolen (henkilön) numero. |
| **Seulontatyypin tunnus**<br>mshr_screeningtypeid<br>*Merkkijono* | Luku/Kirjoitus<br>Vaadittu<br>Viiteavain: ScreeningType | Human Resourcesin seulontatyypin tunnus. |
| **Seulontatyypin tunnuksen arvo**<br>_mshr_fk_screeningtype_id_value<br>*GUID* | Vain luku<br>Vaadittu<br>Viiteavain: mshr_hcmscreeningtypeentity-yksikön mshr_hcmscreeningtypeentityid | Järjestelmän luoma seulontatyypin tietueen tunnus liitetyssä yksikössä. |
| **Ensisijainen kenttä**<br>mshr_primaryfield<br>*Merkkijono* |  Vain luku<br>Pakollinen | Kenttä, jota käytetään yksikkötietueen tunnuksena. |
| **Henkilötunnuksen arvo**<br>_mshr_fk_person_id_value<br>*GUID* | Vain luku<br>Vaadittu<br>Viiteavain: mshr_dirpersonentity-yksikön mshr_dirpersonentityid | Järjestelmän luoma osapuolen (henkilön) yksikkötietueen tunnus. |
| **Henkilön seulonnan yksikkötunnus**<br>mshr_hcmpersonscreeningentityid<br>*GUID* | Vain luku<br>Vaadittu<br>Järjestelmän luoma| Henkilön seulontatietueen yksilöivä ensisijainen tunnus. |
| **Valmistumispäivämäärä**<br>mshr_completeddate<br>*Datetime* | Luku/Kirjoitus<br>Valinnainen | Päivämäärä, jolloin seulonta suoritettiin loppuun. |


## <a name="see-also"></a>Lisätietoja

[Hakijan seurantajärjestelmän integroinnin sovellusliittymän esittely](hr-admin-integration-ats-api-introduction.md)<br>
[Esimerkkikysely palkattavalle hakijalle](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
