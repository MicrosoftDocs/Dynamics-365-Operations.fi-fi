---
title: Seulontatyypit
description: Tässä aiheessa kuvataan Dynamics 365 Human Resourcesin Seulontatyypit-yksikköä.
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
ms.openlocfilehash: bcbf22aac78f1ff96edb7dd927721453f8d10fa5
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/31/2022
ms.locfileid: "8067751"
---
# <a name="screening-types"></a>Seulontatyypit


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Tässä aiheessa kuvataan Dynamics 365 Human Resourcesin Seulontatyypit-yksikköä.

Fyysinen nimi: mshr_hcmscreeningtypeentity

## <a name="description"></a>kuvaus

Tässä yksikössä kuvataan seulontatyypit, jotka yritys on määrittänyt työsuhdetta edeltäville ja meneillään olevien työsuhteiden seulontaprosesseihin.

## <a name="json-representation"></a>JSON-esitys

```json
{
    "mshr_description": "String",
    "mshr_frequencyunit": Int,
    "mshr_generatefrom": Int,
    "mshr_frequencyinterval": Int,
    "mshr_screeningtypeid": "String",
    "mshr_hcmscreeningtypeentityid": "Guid"
}
```

## <a name="properties"></a>Ominaisuudet

| Ominaisuus<br>**Fyysinen nimi**<br>**_Laji_** | Käytä | kuvaus |
| --- | --- | --- |
| **Seulontatyypin yksikön tunnus**<br>mshr_hcmscreeningtypeentityid<br>*GUID* | Vain luku<br>Vaadittu<br>Järjestelmän luoma | Seulontatyypin tietueen yksilöivä ensisijainen tunnus. |
| **Seulontatyypin tunnus**<br>mshr_screeningtypeid<br>*Merkkijono* | Luku/Kirjoitus<br>Vaadittu | Käyttäjän määrittämä seulontatyypin yksilöivä tunnus. |
| **Kuvaus**<br>mshr_description<br>*Merkkijono* | Luku/Kirjoitus<br>Vaadittu | Seulontatyypin kuvaus. |
| **Tiheyden yksikkö**<br>mshr_frequencyunit<br>*mshr_hcmfrequencyunit-asetusjoukko* | Luku/Kirjoitus<br>Vaadittu | Kuvaa, millä tiheydellä seulonta on suoritettava määritetylle henkilölle. |
| **Luo kohteesta**<br>mshr_generatefrom<br>*mshr_hcmfrequencygeneratefrom-asetusjoukko* | Luku-Kirjoitus<br>Vaadittu | Jos Tiheys-arvo on jokin muu kuin "Vain kerran", GenerateFrom-arvo määrittää päivämäärän, josta seuraava seulontatapahtuma lasketaan. |
| **Tiheysväli**<br>mshr_frequencyinterval<br>*Kokonaisluku* | Luku-Kirjoitus<br>Vaadittu | Jos Tiheys-arvo on jokin muu kuin "Vain kerran", sinun on määritettävä seulontatapahtumien välisten aikayksiköiden aikaväli. |

## <a name="see-also"></a>Lisätietoja

[Hakijan seurantajärjestelmän integroinnin sovellusliittymän esittely](hr-admin-integration-ats-api-introduction.md)<br>
[Esimerkkikysely palkattavalle hakijalle](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
