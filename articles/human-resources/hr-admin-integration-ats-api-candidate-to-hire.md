---
title: Palkattava ehdokas
description: Tässä aiheessa kuvataan palkattavan ehdokkaan yksikköä Dynamics 365 Human Resourcesissa.
author: jaredha
ms.date: 02/05/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2021-02-05
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: f0ddf7bd403c926b231f9e010280083d1638b3ad
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2021
ms.locfileid: "5795042"
---
# <a name="candidate-to-hire"></a>Palkattava ehdokas

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Tässä aiheessa kuvataan palkattavan ehdokkaan yksikköä Dynamics 365 Human Resourcesissa.

Fyysinen nimi: mshr_hcmcandidatetohireentity

## <a name="description"></a>kuvaus

Tämä yksikkö antaa hakijan tiedot, joita käytetään työntekijän luomiseen Dynamics 365 Human Resourcesissa. Sitä käytetään kaikkien hakijan tietueiden lukemiseen sekä sisäisten ja ulkoisten hakijatietueiden luomiseen. Näin voit luoda henkilökohtaisia tietoja uutta hakijaa varten.

Kun luot järjestelmään ulkoisen hakijan tietueen, joka tulee olemaan järjestelmässä uusi henkilö, et saa luoda osapuolen (henkilön) numeroa, vaan kirjaat uuden hakijan tietueen. Uusi henkilön yksikkötietue luodaan uuden hakijan tietueen kanssa.

Kun luot sisäisen hakijan tietueen (hakijalle, jolla on jo työntekijätietue yrityksessä), määritä sen tietueen osapuolen (henkilön) numero, joka on jo olemassa hakijatietueen mshr_partynumber-ominaisuudessa sen sijaan, että määrittäsit henkilökohtaiset tiedot (kuten nimen, sukupuolen tai syntymäajan ), joita käytetään uuden henkilötietueen luomiseen.

## <a name="json-representation"></a>JSON-esitys

```json
        {
            "mshr_candidateid": "String",
            "mshr_partynumber": "String",
            "mshr_partytype": "String",
            "mshr_recruitingrequestid": "String",
            "mshr_positionid": "String",
            "mshr_firstname": "String",
            "mshr_middlename": "String",
            "mshr_lastnameprefix": "String",
            "mshr_lastname": "String",
            "mshr_gender": Int,
            "mshr_birthdate": "Date",
            "mshr_citizenshipcountrycode": "String",
            "mshr_veteranstatusid": "String",
            "mshr_isdisabledveteran": Int,
            "mshr_availabilitydate": "Date",
            "mshr_iswillingtorelocate": Int,
            "mshr_comments": "String",
            "mshr_applicantintegrationresult": Int,
            "mshr_donothirereasoncodeid": "String",
            "mshr_dataareaid": "String",
            "_mshr_dataareaid_id_value": "Guid",
            "_mshr_fk_person_id_value": "Guid",
            "_mshr_fk_recruitingrequest_id_value": "Guid",
            "_mshr_fk_position_id_value": "Guid",
            "mshr_hcmcandidatetohireentityid": "Guid",
            "_mshr_fk_veteranstatus_id_value": "Guid",
            "_mshr_fk_reasoncode_id_value": "Guid",
            "mshr_militaryserviceenddate": "Guid",
            "mshr_militaryservicestartdate": "Guid"
        }
```

## <a name="properties"></a>Ominaisuudet

| Ominaisuus<br>**Fyysinen nimi**<br>**_Laji_** | Käytä | kuvaus |
| --- | --- | --- |
| **Palkattavan hakijan yksikön tunnus**<br>mshr_hcmcandidatetohireentityid<br>GUID | Vain luku<br>Vaadittu<br>Järjestelmän luoma | Järjestelmän luoma yksikkötietueen yksilöivä tunnus. |
| **Ehdokkaan tunnus**<br>mshr_candidateid<br>Merkkijono | Vain luku<br>Vaadittu<br>Järjestelmän luoma | Yksikön yksilöivä tunniste. |
| **Osapuolinumero**<br>mshr_partynumber<br>Merkkijono | Vain luku<br>Vaadittu | Hakijan henkilötietueen osapuoli-/henkilönumero. |
| **Henkilötunnuksen arvo**<br>_mshr_fk_person_id_value<br>GUID | Vain luku<br>Vaadittu<br>Viiteavain: mshr_direpersonentity-yksikön mshr_dirpersonentityid | Järjestelmän luoma hakijan osapuolen (henkilön) tietueen yksilöivä tunnus. |
| **Osapuolen tyyppi**<br>mshr_partytype<br>mshr_dirpartytype-asetusjoukko | Vain luku<br>Vaadittu | Tietueen osapuolityyppi, joka on määritetty mshr_dirpartytype-asetusjoukossa. Tämän yksikön tyyppi on aina Henkilö. |
| **Työhönottopyynnön tunnus**<br>mshr_recruitingrequestid<br>Merkkijono | Kirjoita kerran<br>Valinnainen | Viittaa työhönottopyyntöön, jonka tämä hakija täyttää. |
| **Työhönottopyynnön tunnuksen arvo**<br>_mshr_fk_recruitingrequest_id_value<br>GUID | Luku/Kirjoitus<br>Valinnainen<br>Viiteavain: mshr_hcmrecruitingrequestentity-yksikön mshr_hcmrecruitingrequestentityid | Järjestelmän luoma hakijan täyttämän työhönottopyynnön yksilöivä tunnus. |
| **Toimen tunnus**<br>mshr_positionid<br>Merkkijono | Luku/Kirjoitus<br>Valinnainen | Sen toimen tunnus, johon hakijaa harkitaan. |
| **Toimen tunnuksen arvo**<br>_mshr_fk_position_if_value<br>GUID | Vain luku<br>Valinnainen<br>Viiteavain: mshr_hcmpositionv2entity-yksikön mshr_hcmpositionv2entityid | Järjestelmän luoma sen toimen tunnus, johon hakijaa harkitaan. |
| **Etunimi**<br>mshr_firstname<br>Merkkijono | Luku/Kirjoitus<br>Vaadittu | Hakijan etunimi. |
| **Toinen nimi**<br>mshr_middlename<br>Merkkijono | Luku/Kirjoitus<br>Valinnainen | Hakijan toinen nimi. |
| **Sukunimen etuliite**<br>mshr_lastnameprefix<br>Merkkijono | Luku/Kirjoitus<br>Valinnainen | Hakijan sukunimen etuliite. |
| **Sukunimi**<br>mshr_lastname<br>Merkkijono | Luku/Kirjoitus<br>Valinnainen | Hakijan sukunimi. |
| **Sukupuoli**<br>mshr_gender<br>mshr_hcmpersongender-asetusjoukko | Luku/Kirjoitus<br>Valinnainen | Hakijan sukupuoli. |
| **Syntymäpäivämäärä**<br>mshr_birthdate<br>Datetime | Luku/Kirjoitus<br>Valinnainen | Hakijan syntymäpäivä. |
| **Kansalaisuuden maa-/aluekoodi**<br>mshr_citizenshipcountrycode<br>Merkkijono | Luku/Kirjoitus<br>Valinnainen | Määrittää maan/alueen, jossa hakijalla on kansalaisuus. Voimassa olevat maakoodit ovat mshr_logisticaddresscountryregionentity-yksikössä. |
| **Sotaveteraanitilan tunnus**<br>mshr_veteranstatusid<br>Merkkijono | Luku/Kirjoitus<br>Valinnainen | Ilmaisee hakijan sotaveteraanitilan. |
| **Sotaveteraanitilan tunnuksen arvo**<br>_mshr_fk_veteranstatus_id_value<br>GUID | Vain luku<br>Valinnainen<br>Viiteavain: mshr_hcmveteranstatusentity-yksikön mshr_hcmveteranstatusentityid | Järjestelmän luoma sotaveteraanitilan yksikkötietueen yksilöivä tunnus. |
| **Sotilaspalveluksen alkamispäivämäärä**<br>mshr_militaryservicestartdate<br>Datetime | Luku/Kirjoitus<br>Valinnainen | Hakijan asevelvollisuuden alkamispäivämäärä. |
| **Sotilaspalveluksen päättymispäivämäärä**<br>mshr_militaryserviceenddate<br>Datetime | Luku/Kirjoitus<br>Valinnainen | Hakijan asevelvollisuuden päättymispäivämäärä. |
| **On sotainvalidi**<br>mshr_isdisabledveteran<br>mshr_noyes-asetusjoukko | Luku/Kirjoitus<br>Valinnainen | Ilmaisee, onko hakijalla vammautuneen sotaveteraanitila. |
| **Käytettävissä (päivämäärä)**<br>mshr_availabilitydate<br>Datetime | Luku/Kirjoitus<br>Valinnainen | Varhaisin päivämäärä, jolloin hakija voi aloittaa työskentelyn. |
| **On halukas muuttamaan**<br>mshr_iswillingtorelocate<br>mshr_noyes-asetusjoukko | Luku/Kirjoitus<br>Valinnainen | Ilmaisee, onko hakija valmis muuttamaan toimen mukaan. |
| **Huomautukset**<br>mshr_comments<br>Merkkijono | Luku/Kirjoitus<br>Valinnainen | Työhönottajan tai palkkaavan päällikön käyttämät kommentit. |
| **Hakemuksen yhdistämisen tulos**<br>mshr_applcantintegrationresult<br>mshr_applicantintegrationresult-asetusjoukko | Luku/Kirjoitus<br>Vaadittu | Integrointiin liittyvän työhönottoprosessin hakijan tila. |
| **Älä palkkaa – syykoodin tunnus**<br>mshr_donothirereasoncodeid<br>Merkkijono | Luku/Kirjoitus<br>Valinnainen | Syykoodi annetaan tarvittaessa, kun tilaksi (hakemuksen yhdistämisen tulos) määritetään "Ei palkata". |
| **Syykoodin tunnuksen arvo**<br>_mshr_fk_reasoncode_id_value<br>GUID | Vain luku<br>Valinnainen<br>Viiteavain: mshr_hcmreasoncodeentity-yksikön mshr_hcmreasoncodeentityid | Järjestelmän luoman **Ei palkata** -syykoodin yksilöivä tunnus. |
| **Tietoalueen tunnus**<br>mshr_dataareaid<br>Merkkijono | Luku/Kirjoitus<br>Valinnainen |  Määrittää oikeushenkilön (yrityksen). |
| **Tietoalueen tunnuksen arvo**<br>_mshr_dataareaid_id_value<br>GUID | Vain luku<br>Valinnainen<br>Viiteavain: cdm_companyid of cdm_company-yksikkö | Järjestelmän luoma GUID-tunnus, joka yksilöi oikeushenkilön (yrityksen). |

## <a name="see-also"></a>Lisätietoja

[Hakijan seurantajärjestelmän integroinnin sovellusliittymän esittely](hr-admin-integration-ats-api-introduction.md)<br>
[Esimerkkikysely palkattavalle hakijalle](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]