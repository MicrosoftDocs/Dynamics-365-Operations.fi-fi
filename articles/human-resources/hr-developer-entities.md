---
title: Dataverse-taulut
description: Microsoft Dynamics 365 Human Resources käyttää Dataverseä laajennettavuuden ja integroinnin skenaarioiden mahdollistamiseksi.
author: twheeloc
ms.date: 12/08/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 51be30f10c8e5f5e962f54f720f66c712a785835
ms.sourcegitcommit: bdee5e642d417a13abdb778c14ec5f2dbbf8dee7
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/09/2022
ms.locfileid: "9838579"
---
# <a name="dataverse-tables"></a>Dataverse-taulut


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Microsoft Dynamics 365 Human Resources käyttää Dataverseä laajennettavuuden ja integroinnin skenaarioiden mahdollistamiseksi.

> [!NOTE]
> Human Resources -yksiköt vastaavat Dataverse-tauluja. Lisätietoja Dataversesta (aiemmin Common Data Service) ja terminologiapäivityksistä on kohdassa [Mikä on Microsoft Dataverse?](/powerapps/maker/data-platform/data-platform-intro)

Seuraavat Dataverse-taulut ovat käytössä Human Resources -yksiköiden perusteella.

Lisätietoja tunnetuista ongelmista on kohdassa [Lifecycle Servicesin (LCS) ongelmahaku](/dev-itpro/lifecycle-services/issue-search-lcs).

## <a name="benefit-tables"></a>Etutaulut

| Nimi | Taulukko | Tunnetut ongelmat  | Tila |
| --- | --- |    --------|----------  |
| Edun laskentatiheys | cdm_benefitcalculationfrequency |     |     |
| Edun laskennan toistuvuuden maksukausi | cdm_benefitcalculationfrequencypayperiod |     |     |
| Edun laskentahinta | cdm_benefitcalculationrate |    |     |
| Edun laskentahinnan tiedot | cdm_benefitcalculationratedetail |753225 | Ratkaistu  |
| Etuusvaihtoehto | cdm_benefitoption |    |     |
| Etusuunnitelma | cdm_benefitplan (Ei käytössä mukautetulla kentän tuella) |    |     |
| Edun tyyppi | cdm_benefittype |    |     |

## <a name="business-process-tasks-tables"></a>Liiketoimintaprosessin tehtävien taulut

| Nimi | Taulukko |Tunnetut ongelmat  | Tila |
| --- | --- |   --------|----------   |
| Liiketoimintaprosessin kalenteri | cdm_businessprocesscalendar | 751867 | Ratkaistu |
| Liiketoimintaprosessin ryhmämääritys | cdm_businessprocessgroupassignment | 751869  751863 | Käytössä|
| Liiketoimintaprosessikirjaston tehtäväryhmä | cdm_businessprocesslibrarytaskgroup |751866 | Valmis |
| Liiketoimintaprosessin vaihe | cdm_businessprocessstage |      |     |
| Tarkistusluettelomallin otsikko | cdm_businessprocesstemplateheader |     |     |
| Tarkistusluettelomallin tehtävä | cdm_businessprocesstemplatetask |      |     |

## <a name="compensation-tables"></a>Kompensaatiotaulut

| Nimi | Taulukko |Tunnetut ongelmat  | Tila |
| --- | --- | ----------      | -------    |
| Kiinteä kompensaatiosuunnitelma | cdm_compensationfixedplan |754453 | Valmis |
| Kompensaatioruudukko | cdm_compensationgrid |             |     |
| Kompensaatiotaso | cdm_compensationlevel |           |     |
| Kompensaation maksutiheys | cdm_compensationpayfrequency |                  |     |
| Kompensaation viitepisteiden asetukset | cdm_compensationreferencepointsetup |               |     |
| Kompensaation viitepisteen asetusrivi | cdm_compensationreferencepointsetupline |             |     |
| Kompensaatioalue | cdm_compensationregion |                   |     |
| Kompensaatiorakenne | cdm_compensationstructure |    754456        | Valmis    |
| Muuttuva kompensaatiosuunnitelma | cdm_compensationvariableplan |               |     |
| Muuttuvan kompensaatiosuunnitelman taso | cdm_compensationvariableplanlevel |                |     |
| Muuttuvan kompensaatiosuunnitelman tyyppi | cdm_compensationvariableplantype |               |     |
| Kiinteä kompensaatiotapahtuma | cdm_fixedcompensationevent |               |     |
| Hyvityssääntö | cdm_vestingrule |              |     |
| Työntekijän kiinteä kompensaatio | cdm_workerfixedcompensation |              |     |

## <a name="organization-tables"></a>Organisaatiotaulut

| Nimi | Taulukko |Tunnetut ongelmat  | Tila |
| --- | --- | ----------      | -------    |
| Osasto | cdm_department |  752194    | Valmis    |
| Työsuhde | cdm_employment | 762414  |  Valmis  |
| Yhtiö | cdm_company |  |     |
| Tehtävä | cdm_job |  |     |
| Työtehtävä | cdm_jobfunction |        |     |
| Toimi | cdm_jobposition | 752214      | Valmis    |
| Toimityyppi | cdm_positiontype |            |     |
| Toimen työntekijän toimeksianto | cdm_positionworkerassignmentmap | 752224    |  Valmis   |
| Toimen dimensio | cdm_jobpositiondimension|       |     |
| Työlaji | cdm_jobtype |      |     |
| Kieli | cdm_language |        |     |
| Tehtävänimike | cdm_title |       |     |

> [!NOTE]
> Talous hallinnon dimensiot **Toimityypille**, **Toimen työntekijämääritykselle** ja **Työllisyydelle** tarjoavat yhdensuuntaisen integroinnin Dataverse -järjestelmään. Taloushallinnon dimensioiden päivityksiä ei tällä hetkellä synkronoida Dataverse -sovelluksesta Human Resources -sovellukseen. 

## <a name="leave-and-absence-tables"></a>Loma- ja poissaolotaulut

| Nimi | Taulukko | Tunnetut ongelmat  | Tila |
| --- | --- |   ----------      | -------    |
| Lomapankkitapahtuma | cdm_leavebanktransaction |  752252    |    Ratkaistu |
| Lomarekisteröinti | cdm_leaveenrollment |  752934    |Valmis     |
| Lomasuunnitelma | cdm_leaveplan |   752232   |   Valmis  |
| Lomapyyntö | cdm_leaverequest | 753207     | Valmis    |
| Lomapyynnön tiedot | cdm_leaverequestdetail | 753207     |   Valmis  |
| Lomatyyppi | cdm_leavetype |      |     |
| Lomatyypin syykoodi | cdm_leavetypereasoncode |         |     |

>[!NOTE]
>Kaksoiskirjoituksen integrointi Lomien ja poissaolojen Dataverse-taulukoiden avulla on käytettävissä vain, kun **Määritä useita lomatyyppejä yhdessä lomasuunnitelmassa** -ominaisuus on otettu käyttöön Microsoft Dynamics 365 Financessa käyttämällä **ominaisuuksien hallintaa**. 

## <a name="payroll-tables"></a>Palkanlaskentataulut

| Nimi | Taulukko |Tunnetut ongelmat  | Tila |
| --- | --- |  ----------      | -------    |
| Maksujakso | cdm_paycycle |    |     |
| Maksukausi | cdm_payperiod |          |     |
| Palkkalaji | cdm_payrollearningcode |   754458        |   Valmis  |
| Pankkitilisuoritukset | cdm_bankaccountdisbursement |    751904     |   Valmis  |
| Verotusalue | cdm_taxregion |          |     |

## <a name="worker-tables"></a>Työntekijätaulut

| Nimi | Taulukko |Tunnetut ongelmat  | Tila |
| --- | --- |----------      | -------    |
| Työntekijä | cdm_worker |    751906    |    Valmis |
| Työntekijän osoite | cdm_workeraddress |   754465     |Valmis     |
| Työntekijän henkilötiedot | cdm_workerpersonaldetail |   751906     |   Valmis  |
| Työntekijän tunnusnumero | cdm_workerpersonidentificationnumber |  766704      |   Valmis  |
| Työntekijän tunnustyyppi | cdm_workerpersonidentificationtype |        |     |
| Työkalenteri | cdm_workcalendar |        |     |
| Työkalenteripäivämäärä | cdm_workcalendarday |        |     |
| Työkalenterin lomapäivä |cdm_workcalendarholiday |        |     |
| Työkalenterin lomapäivärivi | cdm_workcalendarholidayline |        |     |
| Työkalenterin aikaväli | cdm_workcalendartimeinterval (Ei käytössä mukautetulla kentän tuella) |        |     |
| Työntekijän pankkitili | cdm_workerbankaccount |        |     |

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

![Työntekijä.](./media/HCMCommon-worker-entity-diagram.png)

### <a name="job-and-job-position"></a>Työ ja työn sijainti

![Työ ja työn sijainti.](./media/HCMCommon-job-and-job-position-entity-diagram.png)

### <a name="benefits"></a>Edut

![Edut.](./media/HCMCommon-benefits-entity-diagram.png)

### <a name="compensation"></a>Kompensaatio

![Kompensaatio.](./media/HCMCommon-compensation-entity-diagram.png)

### <a name="leave"></a>Loma

![Loma.](./media/HCMCommon-leave-entity-diagram.png)

### <a name="work-calendar"></a>Työkalenteri

![Työkalenteri.](./media/HCMCommon-work-calendar-entity-diagram.png)

## <a name="see-also"></a>Lisätietoja

[Valitse tietojen integrointiteknologia](hr-admin-integration-choose-technology.md)<br>
[Dataverse -integroinnin määritys](hr-admin-integration-common-data-service.md)<br>
[Määritä Dataverse -virtuaalitaulukot](hr-admin-integration-common-data-service-virtual-entities.md)<br>
[Human Resourcesin virtuaalitaulut – usein kysytyt kysymykset](hr-admin-virtual-entity-faq.md)<br>
[Mikä on Microsoft Dataverse?](/powerapps/maker/data-platform/data-platform-intro)<br>
[Terminologiapäivitykset](/powerapps/maker/data-platform/data-platform-intro#terminology-updates)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
