---
title: Dataverse-taulut
description: Microsoft Dynamics 365 Human Resources käyttää Dataverseä laajennettavuuden ja integroinnin skenaarioiden mahdollistamiseksi.
author: andreabichsel
ms.date: 01/25/2021
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 8ddb74a2f0b6265c5be3c13a009211455ea862da
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/13/2021
ms.locfileid: "5893397"
---
# <a name="dataverse-tables"></a>Dataverse-taulut

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Microsoft Dynamics 365 Human Resources käyttää Dataverseä laajennettavuuden ja integroinnin skenaarioiden mahdollistamiseksi.

> [!NOTE]
> Human Resources -yksiköt vastaavat Dataverse-tauluja. Lisätietoja Dataversesta (aiemmin Common Data Service) ja terminologiapäivityksistä on kohdassa [Mikä on Microsoft Dataverse?](/powerapps/maker/data-platform/data-platform-intro)

Seuraavat Dataverse-taulut ovat käytössä Human Resources -yksiköiden perusteella.

## <a name="benefit-tables"></a>Etutaulut

| Nimi | Taulu |
| --- | --- |
| Edun laskentatiheys | cdm_benefitcalculationfrequency |
| Edun laskennan toistuvuuden maksukausi | cdm_benefitcalculationfrequencypayperiod |
| Edun laskentahinta | cdm_benefitcalculationrate |
| Edun laskentahinnan tiedot | cdm_benefitcalculationratedetail |
| Etuusvaihtoehto | cdm_benefitoption |
| Etusuunnitelma | cdm_benefitplan (Ei käytössä mukautetulla kentän tuella) |
| Edun tyyppi | cdm_benefittype |

## <a name="business-process-tasks-tables"></a>Liiketoimintaprosessin tehtävien taulut

| Nimi | Taulu |
| --- | --- |
| Liiketoimintaprosessin kalenteri | cdm_businessprocesscalendar |
| Liiketoimintaprosessin ryhmämääritys | cdm_businessprocessgroupassignment |
| Liiketoimintaprosessikirjaston tehtäväryhmä | cdm_businessprocesslibrarytaskgroup |
| Liiketoimintaprosessin vaihe | cdm_businessprocessstage |
| Tarkistusluettelomallin otsikko | cdm_businessprocesstemplateheader |
| Tarkistusluettelomallin tehtävä | cdm_businessprocesstemplatetask |

## <a name="compensation-tables"></a>Kompensaatiotaulut

| Nimi | Taulu |
| --- | --- |
| Kiinteä kompensaatiosuunnitelma | cdm_compensationfixedplan |
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

## <a name="organization-tables"></a>Organisaatiotaulut

| Nimi | Taulu |
| --- | --- |
| Osasto | cdm_department |
| Työsuhde | cdm_employment |
| Yhtiö | cdm_company |
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
> Talous hallinnon dimensiot **Toimityypille**, **Toimen työntekijämääritykselle** ja **Työllisyydelle** tarjoavat yhdensuuntaisen integroinnin Dataverse -järjestelmään. Taloushallinnon dimensioiden päivityksiä ei tällä hetkellä synkronoida Dataverse -sovelluksesta Human Resources -sovellukseen. 

## <a name="leave-and-absence-tables"></a>Loma- ja poissaolotaulut

| Nimi | Taulu |
| --- | --- |
| Lomapankkitapahtuma | cdm_leavebanktransaction |
| Lomarekisteröinti | cdm_leaveenrollment |
| Lomasuunnitelma | cdm_leaveplan |
| Lomapyyntö | cdm_leaverequest |
| Lomapyynnön tiedot | cdm_leaverequestdetail |
| Lomatyyppi | cdm_leavetype |
| Lomatyypin syykoodi | cdm_leavetypereasoncode |

## <a name="payroll-tables"></a>Palkanlaskentataulut

| Nimi | Taulu |
| --- | --- |
| Maksujakso | cdm_paycycle |
| Maksukausi | cdm_payperiod |
| Palkkalaji | cdm_payrollearningcode |
| Pankkitilisuoritukset | cdm_bankaccountdisbursement |
| Verotusalue | cdm_taxregion |

## <a name="worker-tables"></a>Työntekijätaulut

| Nimi | Taulu |
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

## <a name="worker-setup-tables"></a>Työntekijän asetustaulut

| Nimi | Taulu |
| --- | --- |
| Sotaveteraanitila | cdm_veteranstatus |
| Etninen alkuperä | cdm_ethnicorigin |
| Syykoodi | cdm_reasoncode |
| Henkilötunnuksen myöntäjätaho | cdm_personidentificationissuingagency |

## <a name="competency-tables"></a>Pätevyystaulut

| Nimi | Taulu |
| --- | --- |
| Osaamisaluetyyppi | cdm_skilltype |

## <a name="table-relationship-models"></a>Taulukkosuhteen mallit

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

[Valitse tietojen integraatioteknologia](hr-admin-integration-choose-technology.md)<br>
[Dataverse -integroinnin määritys](hr-admin-integration-common-data-service.md)<br>
[Määritä Dataverse -virtuaalitaulukot](hr-admin-integration-common-data-service-virtual-entities.md)<br>
[Human Resourcesin virtuaalitaulut – usein kysytyt kysymykset](hr-admin-virtual-entity-faq.md)<br>
[Mikä on Microsoft Dataverse?](/powerapps/maker/data-platform/data-platform-intro)<br>
[Terminologiapäivitykset](/powerapps/maker/data-platform/data-platform-intro#terminology-updates)


[!INCLUDE[footer-include](../includes/footer-banner.md)]