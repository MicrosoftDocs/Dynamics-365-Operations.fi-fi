---
title: Esimerkkikysely palkattavalle hakijalle
description: Tämä ohjeaihe sisältää esimerkkikyselyn Palkattava hakija -yksikölle Dynamics 365 Human Resourcesissa.
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
ms.openlocfilehash: 963e12e9114664a995b92ffe22063c14f904da35
ms.sourcegitcommit: 33b5c8bc4f9461e290513aa22de1ec1fba3b0742
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/05/2021
ms.locfileid: "5125758"
---
# <a name="example-query-for-candidate-to-hire"></a>Esimerkkikysely palkattavalle hakijalle

Tämä ohjeaihe sisältää esimerkkikyselyn Palkattava hakija -yksikölle Dynamics 365 Human Resourcesissa.

Tämä ohjeaihe sisältää esimerkin siitä, miten voit luoda uuden hakijan tietueen yksityiskohtaiset tiedot yhdellä API-liittymän toiminnolla *syvän lisäämisen* avulla. Lisätietoja syvästä lisäyksestä on kohdassa [Liittyvien yksikkötietueiden luominen yhdellä toiminnolla](https://docs.microsoft.com/powerapps/developer/data-platform/webapi/create-entity-web-api#create-related-entity-records-in-one-operation).

**mshr_hcmcandidatetohireentity**-yksikkö on yksilöivä, koska sillä on suhde **mshr_dirpersonentity**-yksikköön. Monet **mshr_hcmcandidatetohireentity**-yksikön ominaisuuksista (esim. **mshr_firstname**, **mshr_lastname** ja **mshr_birthdate**) johdetaan **mshr_dirpersonentity**-tietueesta. Jos kirjaat uuden hakijan tietueen **mshr_hcmcandidatetohireentity**-yksikköön käyttämättä syviä lisäyksiä, voit määrittää näiden ominaisuuksien arvot suoraan **mshr_hcmcandidatetohireentity**-tietueessa. Liittyvä **mshr_dirpersonentity**-tietua luodaan epäsuorasti ominaisuuksille määritettyjen arvojen kanssa. Tämän jälkeen voit luoda mitä tahansa muita liittyviä yksikkötietueita (kuten osaamisalueita tai koulutuksia) erillisinä API-kutsuina.

Jos haluat käyttää syviä lisäyksiä kaikkien toisiinsa liittyvien yksiköiden luomiseen yhdellä toiminnolla, **mshr_dirpersonentity**-yksikön ominaisuudet on määritettävä toiminnon sisäkkäisillä tasoilla.

Tässä esimerkissä kerrotaan, miten voit luoda hakijatietueen, liittyvän henkilötietueen sekä henkilön osaamisalueet ja koulutuksen kolmella sisäkkäisellä tasolla käyttämällä syviä lisäyksiä yhdessä API-liittymän toiminnossa.

> [!NOTE]
> Esimerkissä ei ole kaikkien API-yksiköiden kaikkia ominaisuuksia. Tiedot on yksinkertaistettu esittelyä varten.

**Pyyntö**

```http

POST [Organization URI]/api/data/v9.1/mshr_hcmcandidatetohireentities
Content-Type: application/json; charset=utf-8
OData-MaxVersion: 4.0
OData-Version: 4.0
Accept: application/json

{
    "mshr_dataareaid": "usmf",
    "mshr_recruitingrequestid": "USMF-000141",
    "mshr_positionid": "000601",
    "mshr_iswillingtorelocate": 200000000,
    "mshr_availabilitydate": "2021-03-18",
    "mshr_comments": "Evelyn's experience is exactly what we need for this position.",
    "mshr_FK_Person_id":
        {
            "mshr_firstname": "Evelyn",
            "mshr_lastname": "Chambers",
            "mshr_namesequencedisplayas": "FirstMiddleLast",
            "mshr_FK_HcmPersonSkillEntity_Person":
            [
                {
                    "mshr_skillid": "CustFocus",
                    "mshr_ratingid": "Skills",
                    "mshr_levelid": "4",
                    "mshr_ratinglevelexaminer": "",
                    "mshr_leveltype": 200000000,
                    "mshr_yearsofexperience": 0,
                    "mshr_verified": 200000000,
                    "mshr_leveldate": "2013-01-01T00:00:00Z"
                },
                {
                    "mshr_skillid": "CashFlow",
                    "mshr_ratingid": "Skills",
                    "mshr_levelid": "4",
                    "mshr_ratinglevelexaminer": "",
                    "mshr_leveltype": 200000000,
                    "mshr_yearsofexperience": 0,
                    "mshr_verified": 200000000,
                    "mshr_leveldate": "2013-01-01T00:00:00Z"
                }
            ],
            "mshr_FK_HcmPersonEducationEntity_Person": [
                {
                    "mshr_creditbasis": 200000000,
                    "mshr_enddate": "2021-02-22T00:00:00Z",
                    "mshr_educationlevelid": "Bachelor",
                    "mshr_creditsearned": 0,
                    "mshr_startdate": "2017-02-21T00:00:00Z",
                    "mshr_creditscompleted": 0,
                    "mshr_educationinstitutionid": "Cottonwood Univ",
                    "mshr_educationdisciplineid": "Business Mgmt",
                    "mshr_durationunit": 200000000
                }              
            ]
        }
}
```

**Vastaus**

```http

HTTP/1/1 204 No Content
OData-Version: 4.0
OData-EntityId: [Organization URI]/api/data/v9.1/mshr_hcmcandidatetohireentities(00000d2d-0000-0000-7317-005001000000)

```

## <a name="see-also"></a>Lisätietoja

[Hakijan seurantajärjestelmän integroinnin sovellusliittymän esittely](hr-admin-integration-ats-api-introduction.md)<br>


[!INCLUDE[footer-include](../includes/footer-banner.md)]