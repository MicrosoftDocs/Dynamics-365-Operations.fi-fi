---
title: Henkilön todistus
description: Tässä artikkelissa kuvataan Dynamics 365 Human Resourcesin Henkilön todistus -yksikköä.
author: jaredha
ms.date: 12/15/2022
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
ms.openlocfilehash: 1f9d5a8c83d9714a4d10dec16e66ab87b794b074
ms.sourcegitcommit: 69d7dd6a2d0dc7f2661c7d1f61e8874c7bde1448
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/19/2022
ms.locfileid: "9887314"
---
# <a name="person-certificate"></a>Henkilön todistus


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Tässä artikkelissa kuvataan Dynamics 365 Human Resourcesin Henkilön todistus -yksikköä.

Fyysinen nimi: mshr_hcmpersoncertificateentity

## <a name="description"></a>kuvaus

Tämä yksikkö kuvaa hakijan ammattitodistuksia.

## <a name="json-representation"></a>JSON-esitys

```json
{
    "mshr_certificatetypeid": "String",
    "mshr_startdate": "Date",
    "mshr_enddate": "Date",
    "mshr_notes": "String",
    "mshr_partynumber": "String",
    "mshr_primaryfield": "String",
    "_mshr_fk_certificatetype_id_value": "Guid",
    "_mshr_fk_person_id_value": "Guid",
    "mshr_hcmpersoncertificateentityid": "Guid"
}
```

## <a name="properties"></a>Ominaisuudet

| Ominaisuus<br>**Fyysinen nimi**<br>**_Tyyppi_** | Käytä | kuvaus |
| --- | --- | --- |
| **Todistuksen tyypin tunnus**<br>mshr_certificatetypeid<br>*Merkkijono* | Luku/Kirjoitus<br>Vaadittu |  Human Resourcesin todistustyypin tunnus. |
| **Aloituspäivä**<br>mshr_startdate<br>*Datetime* | Luku/Kirjoitus<br>Pakollinen | Päivä, jolloin todistus myönnettiin. |
| **Päättymispäivä**<br>mshr_enddate<br>*Datetime* | Luku/Kirjoitus<br>Valinnainen | Päivä, jolloin todistus vanhenee. |
| **Muistiinpanot**<br>mshr_notes<br>*Merkkijono* | Luku/Kirjoitus<br>Valinnainen | Muistiinpanot rekrytoijan ja työhönottopäällikön käyttöön. |
| **Osapuolinumero**<br>mshr_partynumber<br>*Merkkijono* | Luku/Kirjoitus<br>Pakollinen | Hakijan osapuolen (henkilön) tunnus. |
| **Ensisijainen kenttä**<br>mshr_primaryfield<br>*Merkkijono* | Vain luku<br>Pakollinen |  Kenttä, jota käytetään yksikkötietueen tunnuksena. Osapuolen numeron, todistus tyypin tunnuksen ja alkamispäivämäärän yhdistelmä. |
| **Todistuksen tyypin tunnuksen arvo**<br>_mshr_fk_certificatetype_id_value<br>*GUID* | Vain luku<br>Vaadittu<br>Viiteavain: mshr_hcmcertificatetypeentity-yksikön mshr_hcmcertificatetypeentityid | Järjestelmän luoma todistustyypin tietueen yksilöivä tunnus liitetyssä yksikössä. |
| **Henkilötunnuksen arvo**<br>_mshr_fk_person_id_value<br>*GUID* | Vain luku<br>Vaadittu<br>Viiteavain: mshr_dirpersonentity-yksikön mshr_dirpersonentityid | Järjestelmän luoma osapuolen (henkilön) yksikkötietueen tunnus. |
| **Henkilön todistuksen yksikkötunnus**<br>mshr_hcmpersoncertificateentityid<br>*GUID* | Vain luku<br>Vaadittu | Järjestelmän luoma henkilön todistuksen yksikkötietueen yksilöivä tunnus. |




## <a name="see-also"></a>Lisätietoja

[Hakijan seurantajärjestelmän integroinnin sovellusliittymän esittely](hr-admin-integration-ats-api-introduction.md)<br>
[Esimerkkikysely palkattavalle hakijalle](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
