---
title: Henkilön tunnusnumero
description: Tässä aiheessa kuvataan Dynamics 365 Human Resourcesin Henkilön tunnusnumero -yksikköä.
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
ms.openlocfilehash: ef33e3922ca676b1312a3d60ae07aa2fe2828056
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/18/2021
ms.locfileid: "6055169"
---
# <a name="person-identification-number"></a>Henkilön tunnusnumero

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Tässä aiheessa kuvataan Dynamics 365 Human Resourcesin Henkilön tunnusnumero -yksikköä.

Fyysinen nimi: mshr_hcmpersonidentificationnumberentity

## <a name="description"></a>kuvaus

Tämä yksikkö kuvaa hakijan tunnusnumeroa. Sen avulla API-kuluttaja voi kirjoittaa tunnusnumerot, kuten henkilötunnukset tai passin numerot, hakijan tietueeseen. Työntekijätietueessa näkyvät tunnusnumerot, mutta eivät hakijan tietueessa. Integroiva sovellus voi kirjoittaa arvot Human Resourcesin tietokantaan, mutta numerot eivät näy Human Resourcesissa, ennen kuin hakijan työntekijätietue on luotu.

## <a name="json-representation"></a>JSON-esitys

```json
{
    "mshr_entrytype": "String",
    "mshr_description": "String",
    "mshr_expirationdate": "Datetime",
    "mshr_isprimary": Int,
    "mshr_identificationnumber": "String",
    "mshr_partynumber": "String",
    "mshr_identificationtypeid": "String",
    "mshr_issuingagencyid": "String",
    "mshr_primaryfield": "String",
    "_mshr_fk_person_id_value": "Guid",
    "_mshr_fk_issuingagency_id_value": "Guid",
    "_mshr_fk_identificationtype_id_value": "Guid",
    "mshr_hcmpersonidentificationnumberentityid": "Guid",
    "mshr_issueddate": "Datetime"
}
```

## <a name="properties"></a>Ominaisuudet

| Ominaisuus<br>**Fyysinen nimi**<br>**_Laji_** | Käytä | kuvaus |
| --- | --- | --- |
| **Työntekijän tunnusnumeron yksikön tunnus**<br>mshr_hcmpersonidentificationnumberentityid<br>*GUID* | Vain luku<br>Vaadittu<br>Järjestelmän luoma | Henkilön tunnusnumerotietueen yksilöivä ensisijainen tunnus. |
| **Merkinnän tyyppi**<br>mshr_entrytype<br>*Merkkijono* | Luku-Kirjoitus<br>Valinnainen | Vapaa arvo, joka viittaa tunnusnumeron merkintätyyppiin. |
| **Kuvaus**<br>mshr_description<br>*Merkkijono* | Luku-Kirjoitus<br>Valinnainen | Tunnusnumeron kuvaus. |
| **Vanhentumispäivä**<br>mshr_expirationdate<br>*Datetime* | Luku-Kirjoitus<br>Valinnainen | Päivämäärä, jolloin tunnusnumero tai siihen liittyvä asiakirja vanhenee. |
| **On ensisijainen**<br>mshr_isprimary<br>*mshr_noyes-asetusjoukko* | Luku-Kirjoitus<br>Valinnainen | Määrittää, onko tunnusnumero tämän tunnustyypin henkilön ensisijainen tietue. |
| **Tunnusnumero**<br>mshr_identificationnumber<br>*Merkkijono* | Luku-Kirjoitus<br>Vaadittu | Tunnusnumero. |
| **Osapuolinumero**<br>mshr_partynumber<br>*Merkkijono* | Luku-Kirjoitus<br>Vaadittu | Tunnusnumeron omistavan osapuolen (henkilön) tunnus. |
| **Henkilötunnuksen arvo**<br>_mshr_fk_person_id_value<br>*GUID* | Vain luku<br>Vaadittu<br>Viiteavain: mshr_dirpersonentity-yksikön mshr_dirpersonentityid | Osapuolen (henkilön) yksilöivä tunniste. |
| **Tunnustyypin tunnus**<br>mshr_identificationtypeid<br>*Merkkijono* | Luku-Kirjoitus<br>Vaadittu | Tunnusnumeron tyyppi. |
| **Tunnustyypin tunnuksen arvo**<br>_mshr_fk_identificationtype_id_value<br>*GUID* | Vain luku<br>Vaadittu<br>Viiteavain: mshr_hcmidentificationtypeentity-yksikön mshr_hcmidentificationtypeentityid | Järjestelmän luoma tunnustyypin yksilöivä tunnus. |
| **Myöntäjätahon tunnus**<br>mshr_issuingagencyid<br>*Merkkijono* | Luku-Kirjoitus<br>Valinnainen | Tunnusnumeron antanut taho tai organisaatio. |
| **Myöntäjätahon tunnuksen arvo**<br>_mshr_fk_issuingagency_id_value<br>*GUID* | Vain luku<br>Valinnainen<br>Viiteavain: mshr_hcmissuingagencyentity-yksikön mshr_hcmissuingagencyentityid | Järjestelmän luoma tunnusnumeron myöntävän tahon yksilöivä tunnus. |
| **Ensisijainen kenttä**<br>mshr_primaryfield<br>*Merkkijono* | Vain luku<br>Vaadittu | Kenttä, jota käytetään yksikkötietueen tunnuksena. Osapuolen numeron, tunnustyypin tunnuksen ja tunnusnumeron yhdistelmä. |
| **Myöntämispäivämäärä**<br>mshr_issuedate<br>*Päivämäärä* | Luku-Kirjoitus<br>Valinnainen | Päivä, jolloin tunnusnumero myönnettiin. |

## <a name="see-also"></a>Lisätietoja

[Hakijan seurantajärjestelmän integroinnin sovellusliittymän esittely](hr-admin-integration-ats-api-introduction.md)<br>
[Esimerkkikysely palkattavalle hakijalle](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]