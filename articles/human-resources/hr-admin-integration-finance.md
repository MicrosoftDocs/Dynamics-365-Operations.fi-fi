---
title: Financeen integroinnin määritys
description: Tässä artikkelissa esitellään toiminto, joka on käytettävissä Dynamics 365 Human Resourcesista ja Dynamics 365 Financesta integrointia varten.
author: andreabichsel
manager: tfehr
ms.date: 03/26/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: SystemAdministrationWorkspaceForm
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 6587b2ced1fdd7a16c6b3f28a34d4a303af9cee5
ms.sourcegitcommit: ea2d652867b9b83ce6e5e8d6a97d2f9460a84c52
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/03/2021
ms.locfileid: "5112386"
---
# <a name="configure-integration-with-finance"></a>Integraation määrittäminen Financen kanssa

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Integroidaksesi Dynamics 365 Human Resources -järjestelmän Dynamics 365 Financeen, voit käyttää henkilöresursseja rahoitusmalliin [Tietojen integrointiohjelmassa](https://docs.microsoft.com/powerapps/administrator/data-integrator). Henkilöstöresurssit rahoitusmalliin mahdollistavat töiden, asemien ja työntekijöiden tiedonkulun. Malli sallii tietojen kulun henkilöstöresursseista rahoitukseen, mutta se ei salli tietojen juoksuttamista henkilöstöresursseihin.

![Human Resourcesista Financeen -integrointivirta](./media/hr-admin-integration-finance-flow.png)

Henkilöstöresursseista talouteen -ratkaisu tarjoaa seuraavanlaisia tietojen synkronointiratkaisuja:

- Pidä työpaikat henkilöstöresursseissa ja synkronoi ne henkilöstöresursseista talouteen
- Pidä toimet ja toimimääritykset Human Resourcesissa ja synkronoi ne Human Resourcesista Financeen
- Pidä työsuhteet Human Resourcesissa ja synkronoi ne Human Resourcesista Financeen
- Pidä työntekijät ja työntekijöiden osoitteet Human Resourcesissa ja synkronoi ne Human Resourcesista Financeen

## <a name="system-requirements-for-human-resources"></a>Human Resourcesin järjestelmävaatimukset

Integrointiratkaisu edellyttää seuraavia Human Resourcesin ja Financen versioita: 

- Dynamics 365 Human Resources, Dataverse
- Dynamics 365 Financen versio 7.2 tai uudempi

## <a name="template-and-tasks"></a>Malli ja tehtävät

Jos haluat käyttää henkilöstöresursseja talousmalliin.

1. Avaa [Power Apps -hallintakeskus](https://admin.powerapps.com/). 

2. Valitse **Projektit** ja valitse sitten **Uusi projekti** oikeasta yläkulmasta. Luo uusi projekti jokaiselle yritykselle, jonka haluat integroida talouteen.

3. Valitse **Henkilöstöhallinnon resurssit (Henkilöstöhallinto Dataversestä talouteen)**, jos haluat synkronoida henkilöresursseista rahoitettavat tiedot.

Malli käyttää seuraavia taustatehtäviä tietueiden synkronointiin henkilöstöhallinnosta talouteen:

- **Työtehtävät kompensaatiotyötehtäviin**
- **Osastot toimintayksiköihin**
- **Työtyypit kompensaatiotyötyyppiin**
- **Työt töihin**
- **Työt työtietoihin**
- **Toimityypit toimityyppiin**
- **Toimet perustoimeen**
- **Toimet toimitietoihin**
- **Toimet toimien kestoihin**
- **Toimet toimihierarkioihin**
- **Työntekijät työntekijään**
- **Työsuhteet työsuhteeseen**
- **Työsuhteet työsuhdetietoihin**
- **Toimen työntekijämääritys toimen työntekijämäärityksiin**
- **Työntekijän osoite työntekijän postiosoitteeseen V2**

## <a name="template-mappings"></a>Mallien yhdistämismääritykset

Seuraavissa mallinyhdistämistaulukoissa tehtävän nimi sisältää kussakin sovelluksessa käytettävät yksiköt. Lähde (Henkilöstöhallinto) on vasemmalla ja kohde (Talous) on oikealla.

### <a name="job-functions-to-compensation-job-function"></a>Työtehtävät kompensaatiotyötehtäviin

| Dataverse-taulu (lähde) | Talousyksikkö (kohde) |
|-------------------------------------|---------------------------------------------|
| cdm_name (cdm_Job   Function Name)  | JOBFUNCTIONID   (JOBFUNCTIONID)            |
| cdm_description   (cdm_description) | DESCRIPTION   (DESCRIPTION)                 |

### <a name="departments-to-operating-unit"></a>Osastot toimintayksiköihin

| Dataverse-taulu (lähde)           | Talousyksikkö (kohde) |
|-----------------------------------------------|---------------------------------------------|
| cdm_name (cdm_name)                           | NAME (NAME)                                 |
| cdm_departmentnumber   (cdm_departmentnumber) | OPERATINGUNITNUMBER   (OPERATINGUNITNUMBER) |
|                                               | OPERATINGUNITTYPE   (OPERATINGUNITTYPE)     |
| cdm_description   (cdm_description)           | NAMEALIAS   (NAMEALIAS)                     |

### <a name="job-types-to-compensation-job-type"></a>Työtyypit kompensaatiotyötyyppiin

| Dataverse-taulu (lähde)   | Talousyksikkö (kohde) |
|---------------------------------------|---------------------------------------------|
| cdm_name (cdm_name)                   | JOBTYPEID   (JOBTYPEID)                     |
| cdm_description   (cdm_description)   | DESCRIPTION   (DESCRIPTION)                 |
| cdm_exemptstatus   (cdm_exemptstatus) | EXEMPTSTATUS   (EXEMPTSTATUS)               |

### <a name="jobs-to-jobs"></a>Työt töihin

| Dataverse-taulu (lähde)                           | Talousyksikkö (kohde)           |
|---------------------------------------------------------------|-------------------------------------------------------|
| cdm_name (cdm_name)                                           | JOBID (JOBID)                                         |
| cdm_maximumnumberofpositions   (cdm_maximumnumberofpositions) | MAXIMUMNUMBEROFPOSITIONS   (MAXIMUMNUMBEROFPOSITIONS) |
| cdm_allowedunlimitedpositions   (cdm_allowunlimitedpositions) | ALLOWUNLIMITEDPOSITIONS   (ALLOWUNLIMITEDPOSITIONS)   |
| cdm_description   (cdm_description)                           | DESCRIPTION   (DESCRIPTION)                           |
| cdm_jobdescription   (cdm_jobdescription)                     | JOBDESCRIPTION   (JOBDESCRIPTIONS)                    |

### <a name="jobs-to-job-detail"></a>Työt työtietoihin

| Dataverse-taulu (lähde)                             | Talousyksikkö (kohde) |
|-----------------------------------------------------------------|---------------------------------------------|
| cdm_name (cdm_name)                                             | JOBID (JOBID)                               |
| cdm_jobtypeid.cdm_name   (Job Type (Job Type Name))             | JOBTYPEID   (JOBTYPEID)                     |
| cdm_jobfunctionid.cdm_name   (Job Function (Job Function Name)) | FUNCTIONID   (FUCNTIONID)                   |
| cdm_validfrom   (Valid From)                                    | VALIDFROM   (VALIDFROM)                     |
| cdm_validto (Valid To)                                        | VALIDTO (VALIDTO)                           |
| cdm_defaultfulltimeequivalent   (Default Full-time Equivalent)   | FULLTIMEEQUIVALENT   (FULLTIMEEQUIVALENT)   |

### <a name="position-types-to-position-type"></a>Toimityypit toimityyppiin

| Dataverse-taulu (lähde)       | Talousyksikkö (kohde) |
|-------------------------------------------|---------------------------------------------|
| cdm_name (cdm_name)                       | POSITIONTYPEID   (POSITIONTYPEID)           |
| cdm_description   (cdm_description)       | DESCRIPTION   (DESCRIPTION)                 |
| cdm_classification   (cdm_classification) | CLASSIFICATION   (CLASSIFICATION)           |

### <a name="job-positions-to-base-position"></a>Toimet perustoimeen

| Dataverse-taulu (lähde)           | Talousyksikkö (kohde) |
|-----------------------------------------------|---------------------------------------------|
| cdm_jobpositionnumber   (Job Position Number) | POSITIONID (POSITIONID)                      |

### <a name="job-positions-to-position-details"></a>Toimet toimitietoihin

| Dataverse-taulu (lähde)              | Talousyksikkö (kohde)       |
|--------------------------------------------------------------------------|---------------------------------------------------|
| cdm_jobpositionnumber  (Job Position Number)                            | POSITIONID (POSITIONID)                             |
| cdm_jobid.cdm_name   (Job (Name))                                        | JOBID (JOBID)                                    |
| cdm_description   (cdm_description)                                        | DESCRIPTION   (DESCRIPTION)                       |
| cdm_departmentid.cdm_departmentnumber   (Department (Department Number)) | DEPARTMENTNUMBER   (DEPARTMENTNUMBER)             |
| cdm_positiontypeid.cdm_name   (Position Type (Name))                     | POSITIONTYPEID   (POSITIONTYPEID)                 |
| cdm_avaialableforassignment   (Available for Assignment)                 | AVAILABLEFORASSIGNMENT   (AVAILABLEFORASSIGNMENT) |
| cdm_validfrom   (Valid From)                                            | VALIDFROM   (VALIDFROM)                           |
| cdm_validto (Valid To)                                                 | VALIDTO (VALIDTO)                               |
| cdm_fulltimeequivalent   (Full-time Equivalent)                           | FULLTIMEEQUIVALENT   (FULLTIMEEQUIVALENT)         |

### <a name="job-positions-to-position-durations"></a>Toimet toimien kestoihin

| Dataverse-taulu (lähde)             | Talousyksikkö (kohde) |
|-------------------------------------------------|---------------------------------------------|
| cdm_jobpositionnumber   (Job Position Number)   | POSITIONID (POSITIONID)                      |
| Calculated   Activation (Calculated Activation) | VALIDFROM (VALIDFROM)                        |
| Calculated   Retirement (Calculated Retirement) | VALIDTO (VALIDTO)                         |

### <a name="job-positions-to-position-hierarchies"></a>Toimet toimihierarkioihin

| Dataverse-taulu (lähde)        | Talousyksikkö (kohde) |
|-----------------------------------------------------------------------------------------------|---------------------------------------------|
| cdm_jobpositionnumber   (Job Position Number)                                                 | POSITIONID(POSITIONID)                      |
| cdm_parentjobpositionid.cdmjobpositionnumber   (cdm_parentjobpositionid.cdmjobpositionnumber) | PARENTPOSITIONID (PARENTPOSITIONID)         |
| cdm_validfrom   (Valid From)                                                                  | VALIDFROM   (VALIDFROM)                     |
| cdm_validto (Valid   To)                                                                      | VALIDTO (VALIDTO)                           |
| HIERARCHYTYPENAME   (HIERARCHYTYPENAME)                                                       | HIERARCHYTYPENAME   (HIERARCHYTYPENAME)     |


### <a name="workers-to-worker"></a>Työntekijät työntekijään
| Dataverse-taulu (lähde)           | Talousyksikkö (kohde)       |
|-----------------------------------------------|---------------------------------------------------|
| cdm_birthdate   (cdm_birthdate)               | BIRTHDATE   (BIRTHDATE)                           |
| cdm_gender   (cdm_gender)                     | GENDER (GENDER)                                   |
| cdm_primaryaddress   (cdm_primaryaddress)     | PRIMARYCONTACTEMAIL   (PRIMARYCONTACTEMAIL )      |
| cdm_primarytelephone   (cdm_primarytelephone) | PRIMARYCONTACTPHONE   (PRIMARYCONTACTPHONE)       |
| cdm_facebookidentity   (cdm_facebookidentity) | PRIMARYCONTACTFACEBOOK   (PRIMARYCONTACTFACEBOOK) |
| cdm_twitteridentity   (cdm_twitteridentity)   | PRIMARYCONTACTTWITTER   (PRIMARYCONTACTTWITTER)   |
| cdm_linkedinIdentity   (cdm_linkedinIdentity) | PRIMARYCONTACTLINKEDIN   (PRIMARYCONTACTLINKEDIN) |
| cdm_websiteurl   (cdm_websiteurl)             | PRIMARYCONTACTURL   (PRIMARYCONTACTURL)           |
| cdm_firstname   (cdm_firstname)               | FIRSTNAME   (FIRSTNAME)                           |
| cdm_middlename   (cdm_middlename)             | MIDDLENAME   (MIDDLENAME)                         |
| cdm_lastname   (cdm_lastname)                 | LASTNAME (LASTNAME)                               |
| cdm_workernumber   (cdm_workernumber)         | PERSONNELNUMBER   (PERSONNELNUMBER)               |
| cdm_type (cdm_type)                           | WORKERTYPE   (WORKERTYPE)                         |
| cdm_state   (cdm_state)                       | WORKSTATUS   (WORKERSTATUS)                       |

### <a name="employments-to-employment"></a>Työsuhteet työsuhteeseen

| Dataverse-taulu (lähde)                             | Talousyksikkö (kohde) |
|-----------------------------------------------------------------|---------------------------------------------|
| cdm_employmentstartdate   (cdm_employmentstartdate)             | EMPLOYMENTSTARTDATE   (EMPLOYMENTSTARTDATE) |
| cdm_employmentenddate   (cdm_employmentenddate)                 | EMPLOYMENTENDDATE   (EMPLOYMENTENDDATE)     |
| cdm_workertype   (cdm_workertype)                               | WORKERTYPE   (WORKERTYPE)                   |
| cdm_workerid.cdm_workernumber   (cdm_workerid.cdm_workernumber) | PERSONNELNUMBER   (PERSONNELNUMBER)         |
| cdm_companyid.cdm_companycode   (cdm_companyid.cdm_companycode) | LEGALENTITYID   (LEGALENTITYID)             |

### <a name="employments-to-employment-detail"></a>Työsuhteet työsuhdetietoihin

| Dataverse-taulu (lähde)                             | Talousyksikkö (kohde)   |
|-----------------------------------------------------------------|-----------------------------------------------|
| cdm_employmentstartdate   (cdm_employmentstartdate)             | EMPLOYMENTSTARTDATE   (EMPLOYMENTSTARTDATE)   |
| cdm_employmentenddate   (cdm_employmentenddate)                 | EMPLOYMENTENDDATE   (EMPLOYMENTENDDATE)       |
| cdm_validfrom   (Valid From)                                    | VALIDFROM   (VALIDFROM)                       |
| cdm_validto (Valid   To)                                        | VALIDTO (VALIDTO)                             |
| cdm_workerstartdate   (cdm_workerstartdate)                     | WORKERSTARTDATE   (WORKERSTARTDATE)           |
| cdm_lastdateworked   (cdm_lastdateworked)                       | LASTDATEWORKED   (LASTDATEWORKED)             |
| cdm_transitiondate   (cdm_transitiondate)                       | TRANSITIONDATE   (TRANSITIONDATE)             |
| cdm_employerunitofnotice   (cdm_employerunitofnotice)           | EMPLOYERUNITOFNOTICE   (EMPLOYERUNITOFNOTICE) |
| cdm_workerunitofnotice   (cdm_workerunitofnotice)               | WORKERUNITOFNOTICE   (WORKERUNITOFNOTICE)     |
| cdm_workerid.cdm_workernumber   (cdm_workerid.cdm_workernumber) | PERSONNELNUMBER   (PERSONNELNUMBER)           |
| cdm_companyid.cdm_companycode   (cdm_companyid.cdm_companycode) | LEGALENTITYID   (LEGALENTITYID)               |
| cdm_employernoticeamount   (cdm_employernoticeamount)           | EMPLOYERNOTICEAMOUNT   (EMPLOYERNOTICEAMOUNT) |
| cdm_workernoticeamount   (cdm_workernoticeamount )              | WORKERNOTICEAMOUNT   (WORKERNOTICEAMOUNT)     |

### <a name="position-worker-assignment-to-position-worker-assignments"></a>Toimen työntekijämääritys toimen työntekijämäärityksiin

| Dataverse-taulu (lähde)                             | Talousyksikkö (kohde)   |
|-----------------------------------------------------------------|-----------------------------------------------|
| cdm_workerid.cdm_workernumber   (cdm_workerid.cdm_workernumber) | PERSONNELNUMBER   (PERSONNELNUMBER)           |
| cdm_jobpositionnumber   (Job Position Number)                   | POSITIONID(POSITIONID)                        |
| cdm_validfrom   (Valid From)                                    | VALIDFROM   (VALIDFROM)                       |
| cdm_validto (Valid To)                                        | VALIDTO (VALIDTO)                             |

### <a name="worker-addresses-to-worker-postal-address-v2"></a>Työntekijän osoite työntekijän postiosoitteeseen V2

| Dataverse-taulu (lähde)                             | Talousyksikkö (kohde)   |
|-----------------------------------------------------------------|-----------------------------------------------|
| cdm_workerid.cdm_workernumber   (cdm_workerid.cdm_workernumber) | PERSONNELNUMBER   (PERSONNELNUMBER)           |
| cdm_addresstype   (cdm_addresstype)                             | ADDRESSLOCATIONROLES   (ADDRESSLOCATIONROLES) |
| cdm_line1   (cdm_line1)                                         | ADDRESSSTREET   (ADDRESSSTREET)               |
| cdm_city (cdm_city)                                             | ADDRESSCITY   (ADDRESSCITY)                   |
| cdm_stateorprovince   (cdm_stateorprovince)                     | ADDRESSSTATE   (ADDRESSSTATE)                 |
| cdm_postalcode   (cdm_postalcode)                               | ADDRESSZIPCODE(ADDRESSZIPCODE)                |
| cdm_countryregion   (cdm_countryregion)                         | ADDRESSCOUNTRYREGION(ADDRESSCOUNTRYREGION)    |
| cdm_addressnumber   (cdm_addressnumber)                         | ADDRESSLOCATIONID(ADDRESSLOCATIONID)          |
| cdm_ispreferred   (cdm_ispreferred)                             | ISPRIMARY   (ISPRIMARY)                       |
| cdm_county   (cdm_county)                                       | ADDRESSCOUNTYID(ADDRESSCOUNTYID)              |
| cdm_addresstype   (cdm_addresstype)                             | ADDRESSDESCRIPTION(ADDRESSDESCRIPTION)        |

## <a name="integration-considerations"></a>Integrointinäkökohdat

Tietojen integrointi henkilöstöhallinnosta talouteen yrittää yhdistää tietueita tunnuksen perusteella. Jos tietueet vastaavat, taloudessa olevat tiedot korvataan henkilöstöhallinnon arvoilla. Tässä voi kuitenkin ilmetä ongelma, jos nämä tietueet ovat loogisesti erilaisia ja sama tunnus luotiin joko Human Resourcesissa tai Financessa kulloisenkin numerosarjan perusteella.

Tämä voi tapahtua kohteessa **Työntekijä**, jossa vastaavuuden perusteena on **henkilöstönumero** ja **Toimet**. Töissä ei käytetä samoja numerosarjoja. Tuloksena tästä, jos sama työtunnus havaitaan sekä henkilöstöhallinnossa että taloudessa, henkilöstöhallinnon tiedot korvaavat Dynamics 365 Financen tiedot. 

Päällekkäisiin tunnuksiin liittyvien ongelmien ehkäisemiseksi voit joko lisätä etuliitteen [numerosarjaan](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/organization-administration/number-sequence-overview?toc=/dynamics365/unified-operations/talent/toc.json) tai määrittää numerosarjan alkamaan sellaisesta numerosta, joka ylittää toisen järjestelmän numeroalueen. 

Työntekijän osoitteessa käytettävä sijaintitunnus ei ole osa numerosarjaa. Kun työntekijän osoitetta integroidaan Human Resourcesista Financeen, saatetaan luoda osoitetietueen kaksoiskappale, jos työntekijän osoite on jo olemassa Financessa. 

Seuraavassa kuvassa on esimerkki mallin yhdistämisestä tietojen integrointiohjelman yhteydessä. 

![Mallin yhdistämismääritys](./media/IntegrationMapping.png)

[!INCLUDE[footer-include](../includes/footer-banner.md)]