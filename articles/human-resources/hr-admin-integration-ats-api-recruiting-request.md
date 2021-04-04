---
title: Työhönottopyyntö
description: Tässä aiheessa kuvataan työhönottopyynnön yksikköä Dynamics 365 Human Resourcesissa.
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
ms.openlocfilehash: b89d257e3874ad7395c0a2c02f259c2f063aa8d0
ms.sourcegitcommit: 2b4809e60974e72df9476ffd62706b1bfc8da4a7
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/04/2021
ms.locfileid: "5500619"
---
# <a name="recruiting-request"></a>Työhönottopyyntö

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Tässä aiheessa kuvataan työhönottopyynnön yksikköä Dynamics 365 Human Resourcesissa.

Fyysinen nimi: mshr_hcmrecruitingrequestentity

### <a name="description"></a>kuvaus

Kuvaa pyyntöä rekrytoida työhön.

### <a name="json-representation"></a>JSON-esitys

```json
{
    "mshr_recruitingrequestid": "String",
    "mshr_hiringmanagerpersonnelnumber": "String",
    "mshr_recruiterpartynumber": "String",
    "mshr_status": Int,
    "mshr_description": "String",
    "mshr_recruitingrequestlocationid": "String",
    "mshr_comments": "String",
    "mshr_jobid": "String",
    "mshr_titleid": "String",
    "mshr_jobfunctionid": "String",
    "mshr_defaultfulltimeequivalency": Decimal,
    "mshr_regulatoryjobcategory": Int,
    "mshr_jobtypeid": "String",
    "mshr_exemptstatus": Int,
    "mshr_estimatedstartdate": "Date",
    "mshr_externaldescription": "String",
    "mshr_compensationlevelid": "String",
    "mshr_compensationlowthreshold": Decimal,
    "mshr_compensationcontrolpoint": Decimal,
    "mshr_compensationhighthreshold": Decimal,
    "mshr_dataareaid": "String",
    "_mshr_dataareaid_id_value": "Guid",
    "_mshr_fk_hiringmanager_id_value": "Guid",
    "_mshr_fk_recruiter_id_value": "Guid",
    "_mshr_fk_job_id_value": "Guid",
    "_mshr_fk_title_id_value": "Guid",
    "_mshr_fk_jobtype_id_value": "Guid",
    "_mshr_fk_compensationlevel_id_value": "Guid",
    "mshr_hcmrecruitingrequestentityid": "Guid",
    "_mshr_fk_recruitingrequestlocation_id_value": “Guid”
}
```

### <a name="properties"></a>Ominaisuudet

| Ominaisuus<br>**Fyysinen nimi**<br>**_Laji_** | Käytä | kuvaus |
| --- | --- | --- |
| **Työhönottopyynnön tunnus**<br>mshr_recruitingrequestid<br>*Merkkijono* | Vain luku<br>Vaadittu<br>Järjestelmän luoma | Käyttäjän luettava yksilöllinen tunnus pyynnölle, joka näkyy HR-sovelluksessa. Numerosarja. |
| **Työhönottopyynnön yksikön tunnus**<br>mshr_hcmrecruitingrequestentityid<br>*GUID* | Vain luku<br>Vaadittu<br>Järjestelmän luoma | Järjestelmän luoma GUID-arvo, jonka avulla työhönottopyyntö voidaan yksilöivästi tunnistaa. |
| **Tietoalueen tunnus**<br>mshr_dataareaid<br>*Merkkijono* | Luku/Kirjoitus<br>Valinnainen<br> | Määrittää työhönottopyynnön yrityksen. |
| **Tietoalueen tunnuksen arvo**<br>_mshr_dataareaid_id_value<br>*GUID*<br> | Vain luku<br>Valinnainen<br>Viiteavain: cdm_companyid of cdm_company-yksikkö | Järjestelmän luoma GUID-tunnus, joka yksilöi työhönottopyynnön oikeushenkilön (yrityksen). |
| **Työhön ottavan esimiehen henkilönumero**<br>mshr_hiringmanagerpersonnelnumber<br>*Merkkijono* | Luku/Kirjoitus<br>Valinnainen | Tähän työhönottopyyntöön liittyvän työhönottopäällikön henkilökuntanumero. |
| **Työhön ottavan esimiehen tunnuksen arvo**<br>_mshr_fk_hiringmanager_id_value<br>*GUID* | Vain luku<br>Valinnainen<br>Viiteavain: mshr_hcmworkerbaseentity-yksikön mshr_hcmworkerbaseentityid | Järjestelmän luoma rekrytointipyyntöön liittyvän esimiehen yksilöivä GUID-tunnus. |
| **Työhön ottavan osapuolen numero**<br>mshr_recruiterpartynumber<br>*Merkkijono* | Luku/Kirjoitus<br>Valinnainen | Pyyntöön valitun työhönoton henkilön (osapuolen) numero. |
| **Työhönottajan tunnuksen arvo**<br>_mshr_fk_recruiter_id_value<br>*GUID* | Vain luku<br>Valinnainen<br>Viiteavain: mshr_dirpersonentity-yksikön mshr_dirpersonentityid | Järjestelmän luoma rekrytointipyyntöön liittyvän työhönottajan yksilöivä GUID-tunnus. |
| **Tila**<br>mshr_status<br>*RecruitingRequestStatus*-asetusjoukko | Luku/Kirjoitus<br>Vaadittu<br> | Ilmaisee työhönottopyynnön tilan. |
| **Kuvaus**<br>mshr_description<br>*Merkkijono* | Luku/Kirjoitus<br>Vaadittu | Pyynnön kuvaus. |
| **Työhönottopyynnön sijainnin tunnus**<br>mshr_recruitingrequestlocationid<br>*Merkkijono* | Luku/Kirjoitus<br>Valinnainen | Käyttäjän luettava tähän pyyntöön liitetyn työsijainnin yksilöivä tunnus. |
| **Työhönottosijainnin tunnuksen arvo**<br>_mshr_fk_recruitinglocation_id_value<br>*GUID* | Vain luku<br>Valinnainen<br>Viiteavain: mshr_hcmrecruitingrequestlocationentity-yksikön mshr_hcmrecruitingrequestlocationentityid | Järjestelmän luoma pyyntöön valitun työhönottosijainnin yksilöivä GUID-tunnus. |
| **Huomautukset**<br>mshr_comments<br>*Merkkijono* | Luku/Kirjoitus<br>Valinnainen | Työhönottopäälliköiden ja rekrytointihenkilöiden pyyntöön liittyvät huomautukset. |
| **Työn tunnus**<br>mshr_jobid<br>*Merkkijono* | Kirjoita kerran<br>Vaadittu |   Käyttäjän luettava tähän pyyntöön liitetyn kaikkien toimien yhteisen työn yksilöivä tunnus. |
| **Työtunnuksen arvo**<br>_mshr_fk_job_id_value<br>*GUID* | Vain luku<br>Vaadittu<br>Viiteavain: mshr_hcmjobentity-yksikön mshr_hcmjobentityid | Järjestelmän luoma tähän työhönottopyyntöön liitetyn kaikkien toimien yhteisen työn yksilöivä tunnus. |
| **Nimikkeen tunnus**<br>mshr_titleid<br>*Merkkijono* | Vain luku<br>Vaadittu | Käyttäjän luettava tähän pyyntöön liitetyn työnimikkeen yksilöivä tunnus. |
| **Nimikkeen tunnuksen arvo**<br>_mshr_fk_title_id_value<br>*GUID* | Vain luku<br>Vaadittu<br>Viiteavain: mshr_hcmtitleentity-yksikön mshr_hcmtitleid | Järjestelmän luoma työhönottopyyntöön valitun työn yksilöivä tunnus. |
| **Työtehtävän tunnus**<br>mshr_jobfunctionid<br>*Merkkijono* | Vain luku<br>Vaadittu<br>Viiteavain: mshr_hcmjobfunctionentity-yksikön mshr_jobfunctionid | Käyttäjän luettava tähän pyyntöön liitetyn työtehtävän yksilöivä tunnus. |
| **Oletusarvoisesti kokopäiväinen**<br>mshr_defaultfulltimeequivalency<br>*Kaksinkertainen* | Vain luku<br>Vaadittu | Työn kokoaikaisuutta vastaava arvo, jossa 1,0 edustaa kokoaikaista työntekijää. |
| **Säännösten mukainen tehtäväluokka**<br>mshr_regulatoryjobcategory<br>*RegulatoryJobCategory*-asetusjoukko | Vain luku<br>Valinnainen | Työlle valitun työtehtävän EEO-tehtäväluokka. Kelvolliset arvot sisältyvät HcmRegulatoryJobCatetory (mshr_hcmregulatoryjobcategory) -asetusjoukkoon. |
| **Työtyypin tunnus**<br>mshr_jobtypeid<br>*Merkkijono* | Vain luku<br>Valinnainen | Toimeen liittyvän työn tyyppi. Työtyypit ovat käyttäjän määrittämiä arvoja, jotka ovat käytettävissä mshr_hcmjobtypeentity-yksikössä. |
| **Työtyypin tunnuksen arvo**<br>_mshr_fk_jobtype_id_value<br>*GUID* | Vain luku<br>Valinnainen<br>Viiteavain: mshr_hcmjobtypenentity-yksikön mshr_hcmjobtypeentityid | Järjestelmän luoma työhönottopyynnön työhön liitetyn työtyypin yksilöivä tunnus. |
| **Vapautustila**<br>mshr_exemptstatus<br>*JobExemptStatus*-asetusjoukko | Vain luku<br>Valinnainen | FLSA-vapautustila, joka perustuu työlajiin. |
| **Arvioitu alkamispäivämäärä**<br>mshr_estimatedstartdate<br>*Päivämäärä* | Luku/Kirjoitus<br>Vaadittu | Arvioitu päivämäärä, jolloin hakija aloittaisi työn. |
| **Ulkoinen kuvaus**<br>mshr_externaldescription<br>*Merkkijono* | Luku/Kirjoitus<br>Valinnainen | Työn/toimen hakijalle näkyvä kuvaus. | 
| **Kompensaation alaraja**<br>mshr_compensationlowthreshold<br>*Kaksinkertainen* | Luku/Kirjoitus<br>Valinnainen | Kompensaatiotason alaraja. |
| **Kompensaation kontrollipiste**<br>mshr_compensationcontrolpoint<br>*Kaksinkertainen* | Luku/Kirjoitus<br>Valinnainen | Kompensaatiotason kontrollipiste. |
| **Kompensaation yläraja**<br>mshr_compensationhighthreshold<br>*Kaksinkertainen* | Luku/Kirjoitus<br>Valinnainen | Kompensaatiotason yläraja. |
| **Kompensaatiotaso**<br>mshr_compensationlevelid<br>*Merkkijono* | Luku/Kirjoitus<br>Valinnainen | Työn kompensaatiotaso. Työlle voi määrittää useita kompensaatiotasoja. Tämä määrite ilmaisee valitun työn kompensaatiotason tälle pyynnölle. |
| **Työn kompensaation tunnus**<br>_mshr_fk_jobcompensation_id_value<br>*GUID* | Vain luku<br>Valinnainen<br>Viiteavain: mshr_hcmjobcompensationentity-yksikön mshr_hcmjobcompensationentityid | Järjestelmän luoma työhönottopyynnön työhön liitetyn kompensaatiotason yksilöivä tunnus. |

## <a name="see-also"></a>Lisätietoja

[Hakijan seurantajärjestelmän integroinnin sovellusliittymän esittely](hr-admin-integration-ats-api-introduction.md)<br>
[Esimerkkikysely työhönottopyyntöä varten](hr-admin-integration-ats-api-recruiting-request-example-query.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
