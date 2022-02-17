---
title: Henkilön ammattikokemus
description: Tässä aiheessa kuvataan Dynamics 365 Human Resourcesin Henkilön ammattikokemus -yksikköä.
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
ms.openlocfilehash: 38535b5dd56b3408ea582fbaf1594b7adefcd171
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/31/2022
ms.locfileid: "8068681"
---
# <a name="person-professional-experience"></a>Henkilön ammattikokemus


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Tässä aiheessa kuvataan Dynamics 365 Human Resourcesin Henkilön ammattikokemus -yksikköä.

Fyysinen nimi: mshr_hcmpersonprofessionalexperienceentity

## <a name="description"></a>kuvaus

Tämä yksikkö kuvaa hakijan ammattikokemusta tai työhistoriaa.

## <a name="json-representation"></a>JSON-esitys

```json
{
    "mshr_partynumber": "String",
    "mshr_employerposition": "String",
    "mshr_startdate": "Date",
    "mshr_allowcontactemployer": Int,
    "mshr_employerlocation": "String",
    "mshr_employername": "String",
    "mshr_enddate": "Date",
    "mshr_note": "String",
    "mshr_phone": "String",
    "mshr_url": "String",
    "mshr_primaryfield": "String",
    "_mshr_fk_person_id_value": "Guid",
    "mshr_hcmpersonprofessionalexperienceentityid": "Guid"
}
```

## <a name="properties"></a>Ominaisuudet

| Ominaisuus<br>**Fyysinen nimi**<br>**_Laji_** | Käytä | kuvaus |
| --- | --- | --- |
| **Henkilön ammattikokemuksen yksikön tunnus**<br>mshr_hcmpersonprofessionalexperienceentityid<br>*GUID* | Vain luku<br>Vaadittu | Järjestelmän luoma yksikkötietueen yksilöivä tunnus. |
| **Osapuolinumero**<br>mshr_partynumber<br>*Merkkijono* | Luku/Kirjoitus<br>Vaadittu | Hakijan henkilöntietueen yksilöivä tunnus. |
| **Henkilötunnuksen arvo**<br>_mshr_fk_person_id_value<br>*GUID* | Vain luku<br>Vaadittu<br>Viiteavain: mshr_dirpersonentity-yksikön mshr_dirpersonentityid | Järjestelmän luoma henkilön yksikkötietueen yksilöivä tunnus. |
| **Työnantajan toimi**<br>mshr_employerposition<br>*Merkkijono* | Luku/Kirjoitus<br>Vaadittu | Hakijan toimen nimike työsuhteen aikana. |
| **Työnantajan nimi**<br>mshr_employername<br>*Merkkijono* | Luku/Kirjoitus<br>Vaadittu | Työnantajan nimi. |
| **Työnantajan sijainti**<br>mshr_employerlocation<br>*Merkkijono* | Luku/Kirjoitus<br>Valinnainen | Työnantajan sijainti. Enimmäispituus: 60. Ei määritettyä tai vaadittua muotoa. |
| **Puhelin**<br>mshr_phone<br>*Merkkijono* | Luku/Kirjoitus<br>Valinnainen | Työnantajan puhelinnumero. |
| **URL**<br>mshr_url<br>*Merkkijono* | Luku/Kirjoitus<br>Valinnainen | Työnantajan verkkosivuston URL-osoite. |
| **Aloituspäivä**<br>mshr_startdate<br>*Datetime* | Luku/Kirjoitus<br>Vaadittu | Hakijan työsuhteen alkamispäivämäärä. |
| **Päättymispäivä**<br>mshr_enddate<br>*Datetime* | Luku/Kirjoitus<br>Valinnainen | Hakijan työsuhteen päättymispäivä. Tyhjäarvo, jos hakija työskentelee yhä tässä toimessa. |
| **Salli yhteydenotto työnantajaan**<br>mshr_allowcontactemployer<br>*mshr_hrmblankyesno-asetusjoukko* | Luku/Kirjoitus<br>Valinnainen | Ilmaisee, salliiko hakija yhteydenoton edelliseen työnantajaan. |
| **Muistiinpanot**<br>mshr_note<br>*Merkkijono* | Luku/Kirjoitus<br>Valinnainen | Muistiinpanot rekrytoijan tai työhönottopäällikön käyttöön. |
| **Ensisijainen kenttä**<br>mshr_primaryfield<br>*Merkkijono* | Vain luku<br>Vaadittu | Kenttä, jota käytetään yksikkötietueen ensisijaisena tunnuksena. Osapuolen numeron, alkamispäivämäärän, työnantajan toimen ja työnantajan nimen yhdistelmä. |

## <a name="see-also"></a>Lisätietoja

[Hakijan seurantajärjestelmän integroinnin sovellusliittymän esittely](hr-admin-integration-ats-api-introduction.md)<br>
[Esimerkkikysely palkattavalle hakijalle](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
