---
title: Seulontatyypit
description: Tässä aiheessa kuvataan Dynamics 365 Human Resourcesin Seulontatyypit-yksikköä.
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
ms.openlocfilehash: 227c15acb44e020ea9858961e45c11ad07e18a74
ms.sourcegitcommit: 33b5c8bc4f9461e290513aa22de1ec1fba3b0742
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/05/2021
ms.locfileid: "5126167"
---
# <a name="screening-types"></a>Seulontatyypit

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