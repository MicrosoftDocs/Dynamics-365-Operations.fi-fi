---
title: Common Data Service -yksiköt
description: Microsoft Dynamics 365 Human Resources käyttää Common Data Serviceä laajennettavuuden ja integroinnin skenaarioiden mahdollistamiseksi.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 988fa0b6d39a49b973626a8a0abe83c546f42297
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/17/2020
ms.locfileid: "4530003"
---
# <a name="common-data-service-entities"></a>Common Data Service -yksiköt

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Microsoft Dynamics 365 Human Resources käyttää Common Data Serviceä laajennettavuuden ja integroinnin skenaarioiden mahdollistamiseksi.

Lisätietoja Common Data Servicestä on kohdassa [Mikä on Common Data Service](https://docs.microsoft.com/powerapps/maker/common-data-service/data-platform-intro) .

Seuraavat henkilöstöhallinnon resurssiyksiköt ovat käytettävissä Common Data Servicessä.

## <a name="benefit-entities"></a>Etuyksiköt

| Nimi | Kokonaisuus |
| --- | --- |
| Edun laskentatiheys | cdm_benefitcalculationfrequency |
| Edun laskennan toistuvuuden maksukausi | cdm_benefitcalculationfrequencypayperiod |
| Edun laskentahinta | cdm_benefitcalculationrate |
| Edun laskentahinnan tiedot | cdm_benefitcalculationratedetail |
| Etuusvaihtoehto | cdm_benefitoption |
| Etusuunnitelma | cdm_benefitplan (Ei käytössä mukautetulla kentän tuella) |
| Edun tyyppi | cdm_benefittype |

## <a name="business-process-tasks-entities"></a>Liiketoimintaprosessin tehtävien yksiköt

| Nimi | Kokonaisuus |
| --- | --- |
| Liiketoimintaprosessin kalenteri | cdm_businessprocesscalendar |
| Liiketoimintaprosessin ryhmämääritys | cdm_businessprocessgroupassignment |
| Liiketoimintaprosessikirjaston tehtäväryhmä | cdm_businessprocesslibrarytaskgroup |
| Liiketoimintaprosessin vaihe | cdm_businessprocessstage |
| Tarkistusluettelomallin otsikko | cdm_businessprocesstemplateheader |
| Tarkistusluettelomallin tehtävä | cdm_businessprocesstemplatetask |

## <a name="compensation-entities"></a>Kompensaatioyksiköt

| Nimi | Kokonaisuus |
| --- | --- |
| Kompensaation kiinteä suunnitelma | cdm_compensationfixedplan |
| Kompensaatioruudukko | cdm_compensationgrid |
| Kompensaatiotaso | cdm_compensationlevel |
| Kompensaation maksutiheys | cdm_compensationpayfrequency |
| Kompensaation viitepisteiden asetukset | cdm_compensationreferencepointsetup |
| Kompensaation viitepisteen asetusrivi | cdm_compensationreferencepointsetupline |
| Kompensaatioalue | cdm_compensationregion |
| Kompensaatiorakenne | cdm_compensationstructure |
| Muuttuva kompensaatiosuunnitelma | cdm_compensationvariableplan |
| Muuttuvan kompensaatiosuunnitelman taso | cdm_compensationvariableplanlevel |
| Muuttuvan kompensaatiosuunnitelman tyyppi | cdm_compensationvariableplantype |
| Kiinteä kompensaatiotapahtuma | cdm_fixedcompensationevent |
| Hyvityssääntö | cdm_vestingrule |
| Työntekijän kiinteä kompensaatio | cdm_workerfixedcompensation |

## <a name="organization-entities"></a>Organisaatioyksiköt

| Nimi | Kokonaisuus |
| --- | --- |
| Osasto | cdm_department |
| Työsuhde | cdm_employment |
| Yritys  | cdm_company |
| Tehtävä | cdm_job |
| Työtehtävä | cdm_jobfunction |
| Toimi | cdm_jobposition |
| Toimityyppi | cdm_positiontype |
| Toimen työntekijän toimeksianto | cdm_positionworkerassignmentmap |
| Toimen dimensio | cdm_jobpositiondimension|
| Työlaji | cdm_jobtype |
| Kieli | cdm_language |
| Tehtävänimike | cdm_title |

> [!NOTE]
> Talous hallinnon dimensiot **Toimityypille**, **Toimen työntekijämääritykselle** ja **Työllisyydelle** tarjoavat yhdensuuntaisen integroinnin Common Data Service -järjestelmään. Taloushallinnon dimensioiden päivityksiä ei tällä hetkellä synkronoida Common Data Service -sovelluksesta Human Resources -sovellukseen. 

## <a name="leave-and-absence-entities"></a>Loman ja poissaolon kohteet

| Nimi | Yksikkö |
| --- | --- |
| Lomapankkitapahtuma | cdm_leavebanktransaction |
| Lomailmoittautuminen | cdm_leaveenrollment |
| Lomasuunnitelma | cdm_leaveplan |
| Lomapyyntö | cdm_leaverequest |
| Lomapyynnön tiedot | cdm_leaverequestdetail |
| Lomatyyppi | cdm_leavetype |
| Lomatyypin syykoodi | cdm_leavetypereasoncode |

## <a name="payroll-entities"></a>Palkanlaskentayksiköt

| Nimi | Kokonaisuus |
| --- | --- |
| Maksujakso | cdm_paycycle |
| Maksukausi | cdm_payperiod |
| Palkanlaskennan ansiokoodi | cdm_payrollearningcode |
| Pankkitilisuoritukset | cdm_bankaccountdisbursement |
| Verotusalue | cdm_taxregion |

## <a name="worker-entities"></a>Työntekijäyksiköt

| Nimi | Kokonaisuus |
| --- | --- |
| Työntekijä | cdm_worker |
| Työntekijän osoite | cdm_workeraddress |
| Työntekijän henkilötiedot | cdm_workerpersonaldetail |
| Työntekijän tunnusnumero | cdm_workerpersonidentificationnumber |
| Työntekijän tunnustyyppi | cdm_workerpersonidentificationtype |
| Työkalenteri | cdm_workcalendar |
| Työkalenteripäivämäärä | cdm_workcalendarday |
| Työkalenterin lomapäivä |cdm_workcalendarholiday |
| Työkalenterin lomapäivärivi | cdm_workcalendarholidayline |
| Työkalenterin aikaväli | cdm_workcalendartimeinterval (Ei käytössä mukautetulla kentän tuella) |
| Työntekijän pankkitili | cdm_workerbankaccount |

## <a name="worker-setup-entities"></a>Työntekijän asetusyksiköt

| Nimi | Kokonaisuus |
| --- | --- |
| Sotaveteraanitila | cdm_veteranstatus |
| Etninen tausta | HcmEthnicOrigin |
| Syykoodi | cdm_reasoncode |
| Henkilötunnuksen myöntänyt virasto | cdm_personidentificationissuingagency |

## <a name="competency-entities"></a>Osaamisyksiköt

| Nimi | Kokonaisuus |
| --- | --- |
| Osaamisaluetyyppi | cdm_skilltype |

## <a name="entity-relationship-models"></a>Yksikkösuhteen mallit

### <a name="worker"></a>Työntekijä

![Työntekijä](./media/HCMCommon-worker-entity-diagram.png)

### <a name="job-and-job-position"></a>Työ ja työn sijainti

![Työ ja työn sijainti](./media/HCMCommon-job-and-job-position-entity-diagram.png)

### <a name="benefits"></a>Edut

![Edut](./media/HCMCommon-benefits-entity-diagram.png)

### <a name="compensation"></a>Kompensaatio

![Kompensaatio](./media/HCMCommon-compensation-entity-diagram.png)

### <a name="leave"></a>Poistu

![Poistu](./media/HCMCommon-leave-entity-diagram.png)

### <a name="work-calendar"></a>Työkalenteri

![Työkalenteri](./media/HCMCommon-work-calendar-entity-diagram.png)

## <a name="see-also"></a>Lisätietoja

[Valitse tietojen integraatioteknologia](hr-admin-integration-choose-technology.md)</br>
[Common Data Service -integroinnin määritys](hr-admin-integration-common-data-service.md)
