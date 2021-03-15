---
title: Henkilön todistus
description: Tässä aiheessa kuvataan Dynamics 365 Human Resourcesin Henkilön todistus -yksikköä.
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
ms.openlocfilehash: fa4582dc00341a647f1ea43ed16d9dce8bfcf688
ms.sourcegitcommit: 33b5c8bc4f9461e290513aa22de1ec1fba3b0742
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/05/2021
ms.locfileid: "5125350"
---
# <a name="person-certificate"></a>Henkilön todistus

Tässä aiheessa kuvataan Dynamics 365 Human Resourcesin Henkilön todistus -yksikköä.

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

| Ominaisuus<br>**Fyysinen nimi**<br>**_Laji_** | Käytä | kuvaus |
| --- | --- | --- |
| **Henkilön todistuksen yksikkötunnus**<br>mshr_hcmpersoncertificateentityid<br>*GUID* | Vain luku<br>Vaadittu | Järjestelmän luoma henkilön todistuksen yksikkötietueen yksilöivä tunnus. |
| **Osapuolinumero**<br>mshr_partynumber<br>*Merkkijono* | Luku/Kirjoitus<br>Vaadittu | Hakijan osapuolen (henkilön) tunnus. |
| **Henkilötunnuksen arvo**<br>_mshr_fk_person_id_value<br>*GUID* | Vain luku<br>Vaadittu<br>Viiteavain: mshr_dirpersonentity-yksikön mshr_dirpersonentityid | Järjestelmän luoma osapuolen (henkilön) yksikkötietueen tunnus. |
| **Todistuksen tyypin tunnus**<br>mshr_certificatetypeid<br>*Merkkijono* | Luku/Kirjoitus<br>Vaadittu |  Human Resourcesin todistustyypin tunnus. |
| **Todistuksen tyypin tunnuksen arvo**<br>_mshr_fk_certificatetype_id_value<br>*GUID* | Vain luku<br>Vaadittu<br>Viiteavain: mshr_hcmcertificatetypeentity-yksikön mshr_hcmcertificatetypeentityid | Järjestelmän luoma todistustyypin tietueen yksilöivä tunnus liitetyssä yksikössä. |
| **Aloituspäivä**<br>mshr_startdate<br>*Datetime* | Luku/Kirjoitus<br>Vaadittu | Päivä, jolloin todistus myönnettiin. |
| **Päättymispäivä**<br>mshr_enddate<br>*Datetime* | Luku/Kirjoitus<br>Valinnainen | Päivä, jolloin todistus vanhenee. |
| **Muistiinpanot**<br>mshr_notes<br>*Merkkijono* | Luku/Kirjoitus<br>Valinnainen | Muistiinpanot rekrytoijan ja työhönottopäällikön käyttöön. |
| **Ensisijainen kenttä**<br>mshr_primaryfield<br>*Merkkijono* | Vain luku<br>Vaadittu |  Kenttä, jota käytetään yksikkötietueen tunnuksena. Osapuolen numeron, todistus tyypin tunnuksen ja alkamispäivämäärän yhdistelmä. |

## <a name="see-also"></a>Lisätietoja

[Hakijan seurantajärjestelmän integroinnin sovellusliittymän esittely](hr-admin-integration-ats-api-introduction.md)<br>
[Esimerkkikysely palkattavalle hakijalle](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]