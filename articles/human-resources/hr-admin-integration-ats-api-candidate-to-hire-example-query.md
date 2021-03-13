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
# <a name="example-query-for-candidate-to-hire"></a><span data-ttu-id="32853-103">Esimerkkikysely palkattavalle hakijalle</span><span class="sxs-lookup"><span data-stu-id="32853-103">Example query for Candidate to hire</span></span>

<span data-ttu-id="32853-104">Tämä ohjeaihe sisältää esimerkkikyselyn Palkattava hakija -yksikölle Dynamics 365 Human Resourcesissa.</span><span class="sxs-lookup"><span data-stu-id="32853-104">This topic provides an example query for the Candidate to hire entity in Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="32853-105">Tämä ohjeaihe sisältää esimerkin siitä, miten voit luoda uuden hakijan tietueen yksityiskohtaiset tiedot yhdellä API-liittymän toiminnolla *syvän lisäämisen* avulla.</span><span class="sxs-lookup"><span data-stu-id="32853-105">This topic provides an example demonstrating how you can use *deep inserts* to create all the detail of a new candidate record in a single API operation.</span></span> <span data-ttu-id="32853-106">Lisätietoja syvästä lisäyksestä on kohdassa [Liittyvien yksikkötietueiden luominen yhdellä toiminnolla](https://docs.microsoft.com/powerapps/developer/data-platform/webapi/create-entity-web-api#create-related-entity-records-in-one-operation).</span><span class="sxs-lookup"><span data-stu-id="32853-106">For more information about deep inserts, see [Create related entity records in one operation](https://docs.microsoft.com/powerapps/developer/data-platform/webapi/create-entity-web-api#create-related-entity-records-in-one-operation).</span></span>

<span data-ttu-id="32853-107">**mshr_hcmcandidatetohireentity**-yksikkö on yksilöivä, koska sillä on suhde **mshr_dirpersonentity**-yksikköön.</span><span class="sxs-lookup"><span data-stu-id="32853-107">The **mshr_hcmcandidatetohireentity** entity is unique because of its relationship to the **mshr_dirpersonentity** entity.</span></span> <span data-ttu-id="32853-108">Monet **mshr_hcmcandidatetohireentity**-yksikön ominaisuuksista (esim. **mshr_firstname**, **mshr_lastname** ja **mshr_birthdate**) johdetaan **mshr_dirpersonentity**-tietueesta.</span><span class="sxs-lookup"><span data-stu-id="32853-108">Many of the properties on the **mshr_hcmcandidatetohireentity** (for example, **mshr_firstname**, **mshr_lastname**, and **mshr_birthdate**) are derived from the **mshr_dirpersonentity** record.</span></span> <span data-ttu-id="32853-109">Jos kirjaat uuden hakijan tietueen **mshr_hcmcandidatetohireentity**-yksikköön käyttämättä syviä lisäyksiä, voit määrittää näiden ominaisuuksien arvot suoraan **mshr_hcmcandidatetohireentity**-tietueessa.</span><span class="sxs-lookup"><span data-stu-id="32853-109">If you post a new candidate record to **mshr_hcmcandidatetohireentity** without using deep inserts, you can define values for these properties directly on the **mshr_hcmcandidatetohireentity** record.</span></span> <span data-ttu-id="32853-110">Liittyvä **mshr_dirpersonentity**-tietua luodaan epäsuorasti ominaisuuksille määritettyjen arvojen kanssa.</span><span class="sxs-lookup"><span data-stu-id="32853-110">The associated **mshr_dirpersonentity** record is created implicitly with the defined values for the properties.</span></span> <span data-ttu-id="32853-111">Tämän jälkeen voit luoda mitä tahansa muita liittyviä yksikkötietueita (kuten osaamisalueita tai koulutuksia) erillisinä API-kutsuina.</span><span class="sxs-lookup"><span data-stu-id="32853-111">You can then create any other related entity records (such as skills or education) as separate API calls.</span></span>

<span data-ttu-id="32853-112">Jos haluat käyttää syviä lisäyksiä kaikkien toisiinsa liittyvien yksiköiden luomiseen yhdellä toiminnolla, **mshr_dirpersonentity**-yksikön ominaisuudet on määritettävä toiminnon sisäkkäisillä tasoilla.</span><span class="sxs-lookup"><span data-stu-id="32853-112">If, however, you want to use deep inserts to create all related entities in one operation, the properties specific to the **mshr_dirpersonentity** entity must be defined on that nested level of the operation.</span></span>

<span data-ttu-id="32853-113">Tässä esimerkissä kerrotaan, miten voit luoda hakijatietueen, liittyvän henkilötietueen sekä henkilön osaamisalueet ja koulutuksen kolmella sisäkkäisellä tasolla käyttämällä syviä lisäyksiä yhdessä API-liittymän toiminnossa.</span><span class="sxs-lookup"><span data-stu-id="32853-113">This example shows how you can create a candidate record, the associated person record, and the person's skills and education in three nested levels using deep inserts in a single API operation.</span></span>

> [!NOTE]
> <span data-ttu-id="32853-114">Esimerkissä ei ole kaikkien API-yksiköiden kaikkia ominaisuuksia.</span><span class="sxs-lookup"><span data-stu-id="32853-114">The example does not include all properties of each of the API entities.</span></span> <span data-ttu-id="32853-115">Tiedot on yksinkertaistettu esittelyä varten.</span><span class="sxs-lookup"><span data-stu-id="32853-115">It is simplified for demonstration purposes.</span></span>

<span data-ttu-id="32853-116">**Pyyntö**</span><span class="sxs-lookup"><span data-stu-id="32853-116">**Request**</span></span>

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

<span data-ttu-id="32853-117">**Vastaus**</span><span class="sxs-lookup"><span data-stu-id="32853-117">**Response**</span></span>

```http

HTTP/1/1 204 No Content
OData-Version: 4.0
OData-EntityId: [Organization URI]/api/data/v9.1/mshr_hcmcandidatetohireentities(00000d2d-0000-0000-7317-005001000000)

```

## <a name="see-also"></a><span data-ttu-id="32853-118">Lisätietoja</span><span class="sxs-lookup"><span data-stu-id="32853-118">See also</span></span>

[<span data-ttu-id="32853-119">Hakijan seurantajärjestelmän integroinnin sovellusliittymän esittely</span><span class="sxs-lookup"><span data-stu-id="32853-119">Applicant Tracking System integration API introduction</span></span>](hr-admin-integration-ats-api-introduction.md)<br>
