---
title: Dataverse-taulukoiden integroinnin määrittäminen
description: Tässä artikkelissa käsitellään Microsoft Dynamics 365 Human Resourcesn ja Dataversein integrointia.
author: anschmidt
ms.date: 12/06/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SystemAdministrationWorkspaceForm
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2022-12-07
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 63c25020b7026a76ecc6e2c3563f8299627ec8a8
ms.sourcegitcommit: bdee5e642d417a13abdb778c14ec5f2dbbf8dee7
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/09/2022
ms.locfileid: "9838623"
---
# <a name="configure-integration-with-dataverse-tables"></a>Dataverse-taulukoiden integroinnin määrittäminen

>[!Important]
>Tässä artikkelissa mainittu toiminto on tällä hetkellä saatavana talous- ja toimintosovellusinfrastruktuurin Dynamics 365 Human Resources -asiakkaiden käytettävissä. 


Microsoft Dynamics 365 Human Resourcesin ja Dataversen integrointiin voidaan käyttää [tietojen integrointiohjelmaa](/powerapps/administrator/data-integrator). Human Resourcesista Dataverseen siirtymismalli mahdollistaa töitä, toimia, työntekijöitä ja muita koskevien tietojen siirtymisen Human Resourcesista Dataverseen ja Dataversesta Human Resourcesiin siten, että molempiin järjestelmiin kirjoitetaan.

## <a name="system-requirements-for-human-resources"></a>Human Resourcesin järjestelmävaatimukset

Integrointiratkaisu edellyttää seuraavia Human Resourcesin ja Dynamics 365 Financen versioita: 

- Dynamics 365 Finance -versio 7.2 ja sitä myöhemmät versiot
- Dynamics CRM -ympäristö, johoon on luotu tietokanta ja jossa sallitaan Dynamics 365 -sovellusten käyttäminen

## <a name="template-and-tasks"></a>Malli ja tehtävät

Human Resourcesista Financeen siirtymismalli otetaan käyttöön seuraavien vaiheiden mukaan.

1. Avaa [Power Apps -hallintakeskus](https://admin.powerapps.com/). 
2. Valitse ympäristön kohdalla ensin **Dynamics 365 -sovellukset** ja sitten työkalurivillä **AppSource**.
3. Asenna malli käyttämällä hakusanaa Human Resourcesin kaksoiskirjoitus tai siirry suoraan seuraavaan osoitteeseen <https://appsource.microsoft.com/product/dynamics-365/mscrm.hcm_dualwrite>.
3. Kun asennus on valmis, avaa Dynamics 365 Finance.
4. Avaa **Tietojen hallinta** -työtila. 
5. Valitse **Kaksoiskirjoitus**. 
6. Suorita ainakin yhden organisaatiossa olevan yrityksen ympäristön linkitysprosessi. 
7. Kun linkki Dataverse-ympäristöön on määritetty, valitse **Käytä ratkaisua**. Ratkaisua käytetään ja yhdistämismäärityksen asennetaan integrointisovellukseen.

## <a name="template-mappings"></a>Mallien yhdistämismääritykset

Seuraavissa mallinyhdistämistaulukoissa tehtävän nimi ilmaisee kussakin sovelluksessa käytettävät yksiköt. Finance on vasemmalla, Dataverse oikealla.

### <a name="bank-account-disbursements-dual-write-to-bank-account-disbursement"></a>Pankkitilisuoritukset (kaksoiskirjoitus) pankkitilisuoritukseen

| Talousyksikkö                 | Dataverse-taulu                                    | 
|--------------------------------|----------------------------------------------------|
| ACCOUNTIDENTIFICATIONID        | cdm\_bankaccountid.cdm\_accountidentification        |
| SUMMA                         | cdm\_amount                                         |
| PRIORITEETTI                       | cdm\_disbursementpriority                           |
| HENKILÖSTÖNUMERO                | cdm\_bankaccountid.cdm\_workerid.cdm\_workernumber    |
| JÄLJELLÄ OLEVA MÄÄRÄ                      | cdm\_isremainder                                    |

### <a name="benefit-calculation-rate-detail-dual-write-to-benefit-calculation-rate-detail"></a>Edun laskentahinnan tiedot (kaksoiskirjoitus) edun laskentahinnan tietoihin

| Talousyksikkö                 | Dataverse-taulu                                    | 
|--------------------------------|----------------------------------------------------|
| CONTRIBUTIONMETHOD             | cdm\_contributionmethod                             |
| VOIMASSA                      | cdm\_effective                                      |
| EMPLOYERCONTRIBUTION           | cdm\_employercontribution                           |
| PÄÄTTYMINEN                     | cdm\_expiration                                     |
| WORKERDEDUCTION                | cdm\_workerdeduction                                |
| NIMI                           | cdm\_calculationrateid.cdm\_name                     |

### <a name="benefit-calculation-rate-header-to-benefit-calculation-rate"></a>Edun laskentahinnan otsikko edun laskentahintaan

| Talousyksikkö                 | Dataverse-taulu                                    | 
|--------------------------------|----------------------------------------------------|
| KUVAUS                    | cdm\_description                                    |
| NIMI                           | cdm\_name                                           |
| TIERTYPE                       | cdm\_tiertype                                       |

### <a name="benefit-option-to-benefit-option"></a>Etuusvaihtoehto etuusvaihtoehtoon

| Talousyksikkö                 | Dataverse-taulu                                    | 
|--------------------------------|----------------------------------------------------|
| ALLOWBENEFICIARYDESIGNATIONS   | cdm\_allowbeneficiarydesignations                   |
| ALLOWDEPENDENTCOVERAGE         | cdm\_allowdependentcoverage                         |
| BENEFITOPTIONID                | cdm\_name                                           |
| KUVAUS                    | cdm\_description                                    |
| ISWAIVE                        | cdm\_iswaived                                       |

### <a name="benefit-type-to-benefit-type"></a>Edun tyyppi edun tyyppiin

| Talousyksikkö                 | Dataverse-taulu                                    | 
|--------------------------------|----------------------------------------------------|
| BENEFITTYPEID                  | cdm\_name                                           |
| CONCURRENTENROLLMENT           | cdm\_concurrentenrollment                           |
| KUVAUS                    | cdm\_description                                    |
| PAYROLLCATEGORY                | cdm\_payrollcategory                                |

### <a name="business-calendar-to-business-process-calendar"></a>Liiketoimintakalenteri liiketoimintaprosessin kalenteriin

| Talousyksikkö                 | Dataverse-taulu                                    | 
|--------------------------------|----------------------------------------------------|
| CALENDARID                     | cdm\_name                                           |
| NIMI                           | cdm\_calendarname                                   |
| STARTDATE                      | cdm\_startdate                                      |
| ENDDATE                        | cdm\_enddate                                        |
| ISOPENMONDAY                   | cdm\_ismondayopen                                   |
| ISOPENTUESDAY                  | cdm\_istuesdayopen                                  |
| ISOPENWEDNESDAY                | cdm\_iswednesdayopen                                |
| ISOPENTHURSDAY                 | cdm\_isthursdayopen                                 |
| ISOPENFRIDAY                   | cdm\_isfridayopen                                   |
| ISOPENSATURDAY                 | cdm\_issaturdayopen                                 |
| ISOPENSUNDAY                   | cdm\_issundayopen                                   |

### <a name="business-process-to-business-process-header"></a>Liiketoimintaprosessista liiketoimintaprosessin otsikkoon

| Talousyksikkö                 | Dataverse-taulu                                    | 
|--------------------------------|----------------------------------------------------|
| PROCESSID                      | cdm\_processid                                      |
| PROCESSTYPE                    | cdm\_processtype                                    |
| GENERICSUBTYPE                 | cdm\_genericsubtype                                 |
| NIMI                           | cdm\_name                                           |
| KUVAUS                    | cdm\_description                                    |
| TILA                         | cdm\_status                                         |
| TARGETDATE                     | cdm\_targetdate                                     |
| STARTDATETIME                  | cdm\_startdatetime                                  |
| ENDDATETIME                    | cdm\_enddatetime                                    |
| RESOLVEDBYPERSONNELNUMBER      | cdm\_resolvedbyid.cdm\_workernumber                  |
| PROCESSOWNERPERSONNELNUMBER    | cdm\_processownerid.cdm\_workernumber                |
| SOURCETEMPLATENAME             | cdm\_sourcetemplateid.cdm\_name                      |
| SOURCETEMPLATEPROCESSTYPE      | cdm\_sourcetemplateid.cdm\_businessprocesstype       |
| SOURCETEMPLATEGENERICSUBTYPE   | cdm\_sourcetemplateid.cdm\_genericsubtype            |

### <a name="business-process-library-task-group-to-business-process-library-task-group"></a>Liiketoimintaprosessikirjaston tehtäväryhmä liiketoimintaprosessikirjaston tehtäväryhmään

| Talousyksikkö                 | Dataverse-taulu                                    | 
|--------------------------------|----------------------------------------------------|
| PROCESSTYPE                    | cdm\_processtype                                    |
| NIMI                           | cdm\_name                                           |
| KUVAUS                    | cdm\_description                                    |

### <a name="business-process-stage-to-business-process-stage"></a>Liiketoimintaprosessin vaihe liiketoimintaprosessin vaiheeseen

| Talousyksikkö                 | Dataverse-taulu                                    | 
|--------------------------------|----------------------------------------------------|
| PROCESSTYPE                    | cdm\_businessprocesstype                            |
| NIMI                           | cdm\_name                                           |
| KUVAUS                    | cdm\_description                                    |
| SEQUENCENUMBER                 | cdm\_sequencenumber                                 |

### <a name="business-process-task-to-business-process-task"></a>Liiketoimintaprosessin tehtävä liiketoimintaprosessin tehtävään

| Talousyksikkö                 | Dataverse-taulu                                    | 
|--------------------------------|----------------------------------------------------|
| KUVAUS                    | cdm\_description                                    |
| DUEDATE                        | cdm\_duedate                                        |
| TASKID                         | cdm\_taskid                                         |
| OHJEET                   | cdm\_instructions                                   |
| COMPLETIONDATETIME             | cdm\_completiondatetime                             |
| ASSIGNMENTTYPE                 | cdm\_assignmenttype                                 |
| ISOPTIONAL                     | cdm\_isoptional                                     |
| NIMI                           | cdm\_name                                           |
| TILA                         | cdm\_status                                         |
| RESOLVEDBY\_PERSONNELNUMBER     | cdm\_resolvedbyid.cdm\_workernumber                  |
| TEMPLATETASKID                 | cdm\_templatetaskid.cdm\_taskid                      |
| ASSIGNEDWORKER\_PERSONNELNUMBER | cdm\_assignedworkerid.cdm\_workernumber              |
| PROCESSID                      | cdm\_processheaderid.cdm\_processid                  |
| ASSIGNEDGROUP\_NAME             | cdm\_assignedgroupid.cdm\_name                       |
| ASSIGNEDPOSITION\_POSITIONID    | cdm\_assignedposition.cdm\_jobpositionnumber         |

### <a name="business-process-template-to-checklist-template-header"></a>Liiketoimintaprosessimalli tarkistusluettelomallin otsikkoon

| Talousyksikkö                 | Dataverse-taulu                                    | 
|--------------------------------|----------------------------------------------------|
| PROCESSTYPE                    | cdm\_businessprocesstype                            |
| GENERICSUBTYPE                 | cdm\_genericsubtype                                 |
| NIMI                           | cdm\_name                                           |
| KUVAUS                    | cdm\_description                                    |
| CALENDARID                     | cdm\_businessprocesscalendarid.cdm\_name             |
| HENKILÖSTÖNUMERO                | cdm\_processownerid.cdm\_workernumber                |
| ISACTIVE                       | cdm\_isactive                                       |

### <a name="business-process-template-task-to-checklist-template-task"></a>Liiketoimintaprosessimallin tehtävään tarkistusluettelomallin tehtävään

| Talousyksikkö                 | Dataverse-taulu                                    | 
|--------------------------------|----------------------------------------------------|
| TASKID                         | cdm\_taskid                                         |
| NIMI                           | cdm\_name                                           |
| TEMPLATEHEADER\_PROCESSTYPE     | cdm\_businessprocesstemplateheaderid.cdm\_businessprocesstype |
| TEMPLATEHEADER\_GENERICSUBTYPE  | cdm\_businessprocesstemplateheaderid.cdm\_genericsubtype |
| TEMPLATEHEADER\_NAME            | cdm\_businessprocesstemplateheaderid.cdm\_name       |
| KUVAUS                    | cdm\_description                                    |
| DUEDATEOFFSETDAYS              | cdm\_duedateoffsetdays                              |
| MENUITEMTYPE                   | cdm\_tasklinktype                                   |
| MENUITEM                       | cdm\_tasklink                                       |
| CONTACTPERSON\_PERSONNELNUMBER  | cdm\_contactpersonid.cdm\_workernumber               |
| ASSIGNMENTTYPE                 | cdm\_assignmenttype                                 |
| ASSIGNEDWORKER\_PERSONNELNUMBER | cdm\_assignedworkerid.cdm\_workernumber              |
| ASSIGNEDPOSITION\_POSITIONID    | cdm\_assignedpositionid.cdm\_jobpositionnumber       |
| ASSIGNEDGROUP\_NAME             | cdm\_assignedgroupid.cdm\_name                       |
| ISOPTIONAL                     | cdm\_isoptional                                     |
| OHJEET                   | cdm\_instructions                                   |

### <a name="calculation-frequency-to-benefit-calculation-frequency"></a>Laskentatiheys edun laskentatiheyteen

| Talousyksikkö                 | Dataverse-taulu                                    | 
|--------------------------------|----------------------------------------------------|
| KUVAUS                    | cdm\_description                                    |
| FREQUENCY                      | cdm\_name                                           |
| FREQUENCYCONTROL               | cdm\_frequencycontrol                               |
| ISIMMUTABLE                    | cdm\_isimmutable                                    |

### <a name="calculation-frequency-pay-period-to-benefit-calculation-frequency-pay-period"></a>Laskennan toistuvuuden maksukausi edun laskentatiheyden maksukauteen

| Talousyksikkö                 | Dataverse-taulu                                    | 
|--------------------------------|----------------------------------------------------|
| CALCULATIONFREQUENCYID         | cdm\_benefitcalculationfrequencyid.cdm\_name         |
| PERIODSTARTDATE                | cdm\_payperiodid.cdm\_periodstartdate                |
| PAYCYCLEID                     | cdm\_payperiodid.cdm\_paycycleid.cdm\_name            |

### <a name="calendar-to-work-calendar"></a>Kalenteri työkalenteriin

| Talousyksikkö                 | Dataverse-taulu                                    | 
|--------------------------------|----------------------------------------------------|
| CALENDARID                     | cdm\_name                                           |
| CALENDARNAME                   | cdm\_description                                    |
| WORKCALENDARHOLIDAYID          | cdm\_workcalendarholidayid.cdm\_name                 |

### <a name="compensation-fixed-action-table-to-fixed-compensation-event"></a>Kompensaation kiinteän toiminnon taulu kiinteään kompensaatiotapahtumaan

| Talousyksikkö                 | Dataverse-taulu                                    | 
|--------------------------------|----------------------------------------------------|
| TOIMINTO                         | cdm\_name                                           |
| AKTIIVINEN                         | cdm\_isactive                                       |
| KUVAUS                    | cdm\_description                                    |
| TYYPPI                           | cdm\_eventtype                                      |

### <a name="compensation-fixed-plan-to-compensation-fixed-plan"></a>Kiinteä kompensaatiosuunnitelma kiinteään kompensaatiosuunnitelmaan

| Talousyksikkö                 | Dataverse-taulu                                    | 
|--------------------------------|----------------------------------------------------|
| SUUNNITELMA                           | cdm\_name                                           |
| KUVAUS                    | cdm\_description                                    |
| TYYPPI                           | cdm\_type                                           |
| EFFECTIVEDATE                  | cdm\_effectivedate                                  |
| EXPIRATIONDATE                 | cdm\_expirationdate                                 |
| VALUUTTA                       | cdm\_transactioncurrencyid.isocurrencycode          |
| PAYFREQUENCY                   | cdm\_payfrequency.cdm\_name                          |
| HIRERULE                       | cdm\_hirerule                                       |
| OUTOFRANGETOLERANCE            | cdm\_outofrangetolerance                            |
| RECOMMENDATIONALLOWED          | cdm\_recommendationallowed                          |
| COMPENSATIONSTRUCTURE          | cdm\_compensationgrid.cdm\_name                      |
| REFPOINTSETUPID                | cdm\_referencepointsetupline.cdm\_referencepointsetupid.cdm\_name |
| CONTROLPOINT                   | cdm\_referencepointsetupline.cdm\_name               |

### <a name="compensation-grids-to-compensation-grid"></a>Kompensaatioruudukot kompensaatioruudukkoon

| Talousyksikkö                 | Dataverse-taulu                                    | 
|--------------------------------|----------------------------------------------------|
| GRIDID                         | cdm\_name                                           |
| KUVAUS                    | cdm\_description                                    |
| EFFECTIVEDATE                  | cdm\_effectivedate                                  |
| EXPIRATIONDATE                 | cdm\_expirationdate                                 |
| REFERENCESETUP                 | cdm\_referencepointsetupid.cdm\_name                 |
| TYYPPI                           | cdm\_type                                           |
| VALUUTTA                       | cdm\_transactioncurrencyid.isocurrencycode          |

### <a name="compensation-job-function-to-job-function"></a>Kompensaation työtehtävä työtehtäviin

| Talousyksikkö                 | Dataverse-taulu                                    | 
|--------------------------------|----------------------------------------------------|
| JOBFUNCTIONID                  | cdm\_name                                           |
| KUVAUS                    | cdm\_description                                    |

### <a name="compensation-job-type-to-job-type"></a>Kompensaation työn tyyppi työtyyppiin

| Talousyksikkö                 | Dataverse-taulu                                    | 
|--------------------------------|----------------------------------------------------|
| JOBTYPEID                      | cdm\_name                                           |
| KUVAUS                    | cdm\_description                                    |
| EXEMPTSTATUS                   | cdm\_exemptstatus                                   |

### <a name="compensation-pay-frequency-to-compensation-pay-frequency"></a>Kompensaation maksutiheys kompensaation maksutiheyteen

| Talousyksikkö                 | Dataverse-taulu                                    | 
|--------------------------------|----------------------------------------------------|
| PAYRATECONVERSION              | cdm\_name                                           |
| KAUSI                         | cdm\_period                                         |
| KUVAUS                    | cdm\_description                                    |
| ANNUALCONVERSIONFACTOR         | cdm\_annualconversionfactor                         |
| HOURLYCONVERSIONFACTOR         | cdm\_hourlyconversionfactor                         |
| MONTHLYCONVERSIONFACTOR        | cdm\_monthlyconversionfactor                        |
| WEEKLYCONVERSIONFACTOR         | cdm\_weeklyconversionfactor                         |

### <a name="compensation-regions-to-compensation-region"></a>Kompensaatioalueet kompensaatioalueeseen

| Talousyksikkö                 | Dataverse-taulu                                    | 
|--------------------------------|----------------------------------------------------|
| KUVAUS                    | cdm\_description                                    |
| SIJAINTI                       | cdm\_name                                           |

### <a name="compensation-variable-plan-v2-to-compensation-variable-plan"></a>Muuttuva kompensaatiosuunnitelma V2 muuttuvaan kompensaatiosuunnitelmaan

| Talousyksikkö                 | Dataverse-taulu                                    | 
|--------------------------------|----------------------------------------------------|
| VARIABLEAWARDBASIS             | cdm\_awardbasis                                     |
| AWARDBASISCALCULATION          | cdm\_awardbasiscalculation                          |
| CALCULATIONTYPE                | cdm\_calculationtype                                |
| KUVAUS                    | cdm\_description                                    |
| ENABLEENROLLMENT               | cdm\_enableenrollment                               |
| ENABLELEVELS                   | cdm\_enablelevels                                   |
| ENABLERECOMMENDATION           | cdm\_enablerecommendation                           |
| HIRERULE                       | cdm\_hirerule                                       |
| LEVERAGE100PERCENT             | cdm\_leverage100percent                             |
| LEVERAGEMAXIMUM                | cdm\_leveragemaximum                                |
| LEVERAGEMINIMUM                | cdm\_leverageminimum                                |
| LEVERAGEOVEROBJECTIVE          | cdm\_leverageoverobjective                          |
| LEVERAGEUNDEROBJECTIVE         | cdm\_leverageunderobjective                         |
| PERCENTOFBASIS                 | cdm\_percentofbasis                                 |
| PLANID                         | cdm\_name                                           |
| VARIABLECOMPENSATIONTYPE       | cdm\_variablecompensationtypeid.cdm\_name            |
| UNITCURRENCYCODE               | transactioncurrencyid.isocurrencycode              |
| UNITRELATIONSHIP               | cdm\_unitrelationship                               |
| UNITVALUE                      | cdm\_unitvalue                                      |
| NUMBEROFUNITSREAL              | cdm\_numberofunits                                  |
| EFFECTIVEDATE                  | cdm\_effectivedate                                  |
| EXPIRATIONDATE                 | cdm\_expirationdate                                 |
| VESTINGRULE                    | cdm\_vestingruleid.cdm\_name                         |
| LEVERAGETOLERANCEMAX           | cdm\_leveragetolerancemax                           |
| LEVERAGETOLERANCEMIN           | cdm\_leveragetolerancemin                           |

### <a name="compensation-variable-type-to-compensation-variable-plan-type"></a>Kompensaation muuttuva tyyppi muuttuvaan kompensaatiosuunnitelman tyyppiin

| Talousyksikkö                 | Dataverse-taulu                                    | 
|--------------------------------|----------------------------------------------------|
| KUVAUS                    | cdm\_description                                    |
| TYYPPI                           | cdm\_awardtype                                      |
| VARIABLECOMPENSATIONTYPE       | cdm\_name                                           |

### <a name="compensation-vesting-rules-to-vesting-rule"></a>Kompensaation hyvityssäännöt hyvityssääntöön

| Talousyksikkö                 | Dataverse-taulu                                    | 
|--------------------------------|----------------------------------------------------|
| KUVAUS                    | cdm\_description                                    |
| HUOMAUTUS                           | cdm\_notes                                          |
| VESTINGRULE                    | cdm\_name                                           |

### <a name="department-v2-to-department"></a>Osasto V2 osastoon

| Talousyksikkö                 | Dataverse-taulu                                    | 
|--------------------------------|----------------------------------------------------|
| OPERATINGUNITNUMBER            | cdm\_departmentnumber                               |
| NIMI                           | cdm\_name                                           |
| SEARCHNAME                     | cdm\_description                                    |
| PARTYTYPE                      | cdm\_partytype                                      |

### <a name="dual-write-tax-region-to-tax-region"></a>Kaksoiskirjoituksen verotusalue veroalueeseen

| Talousyksikkö                 | Dataverse-taulu                                    | 
|--------------------------------|----------------------------------------------------|
| PAIKKAKUNTA                           | cdm\_city                                           |
| COUNTRYORREGION                | cdm\_countryorregion                                |
| LÄÄNI                         | cdm\_county                                         |
| OSAVALTIO                          | cdm\_stateorprovince                                |
| TAXREGIONNAME                  | cdm\_name                                           |

### <a name="dual-write-worker-identification-to-worker-person-identification-number"></a>Kaksoiskirjoituksen työntekijän tunnus työntekijän henkilötunnuksen numeroon

| Talousyksikkö                 | Dataverse-taulu                                    | 
|--------------------------------|----------------------------------------------------|
| KUVAUS                    | cdm\_description                                    |
| ENTRYTYPE                      | cdm\_entrytype                                      |
| EXPIRATIONDATE                 | cdm\_expirationdate                                 |
| IDENTIFICATIONNUMBER           | cdm\_identificationnumber                           |
| IDENTIFICATIONTYPEID           | cdm\_identificationtypeid.cdm\_name                  |
| ISPRIMARY                      | cdm\_isprimary                                      |
| ISSUEDATE                      | cdm\_issuedate                                      |
| ISSUINGAGENCYID                | cdm\_issuingagencyid.cdm\_name                       |
| WORKERNUMBER                   | cdm\_workerid.cdm\_workernumber                      |

### <a name="compensation-structure-to-compensation-structure"></a>Kompensaatiorakenne kompensaatiorakenteeseen

| Talousyksikkö                 | Dataverse-taulu                                    | 
|--------------------------------|----------------------------------------------------|
| SUMMA                         | cdm\_amount                                         |
| RUUDUKKO                           | cdm\_compensationgridid.cdm\_name                    |
| LEVELID                        | cdm\_compensationlevelid.cdm\_name                   |
| REFERENCEPOINTLINENUMBER       | cdm\_referencepointid.cdm\_linenumber                |
| REFERENCESETUP                 | cdm\_referencepointid.cdm\_referencepointsetupid.cdm\_name |
| REFERENCEPOINT                 | cdm\_referencepointid.cdm\_name                      |

### <a name="earning-code-to-payroll-earning-code"></a>Ansiokoodi palkkalajiin

| Talousyksikkö                 | Dataverse-taulu                                    | 
|--------------------------------|----------------------------------------------------|
| EARNINGCODE                    | cdm\_name                                           |
| KUVAUS                    | cdm\_description                                    |
| INCLUDEINPAYMENTTYPE           | cdm\_includeinpaymenttype                           |
| QUANTITYUNIT                   | cdm\_quantityunit                                   |
| TRACKFMLAHOURS                 | cdm\_trackfmlahours                                 |
| ISPRODUCTIVE                   | cdm\_isproductive                                   |

### <a name="employee-fixed-compensation-to-worker-fixed-compensation"></a>Työntekijän kiinteä kompensaatio työntekijän kiinteään kompensaatioon

| Talousyksikkö                 | Dataverse-taulu                                    | 
|--------------------------------|----------------------------------------------------|
| COMPENSATIONLEVELID            | cdm\_compensationlevelid.cdm\_name                   |
| TYYPPI                           | cdm\_compensationtype                               |
| EFFECTIVEDATE                  | cdm\_effectivedate                                  |
| EXPIRATIONDATE                 | cdm\_expirationdate                                 |
| LINENUMBER                     | cdm\_linenumber                                     |
| PAYFREQUENCY                   | cdm\_payfrequencyid.cdm\_name                        |
| PALKKIO                        | cdm\_payrate                                        |
| SUUNNITELMA                           | cdm\_planid.cdm\_name                                |
| POSITIONID                     | cdm\_positionid.cdm\_jobpositionnumber               |
| PROCESSTYPE                    | cdm\_processtype                                    |
| HENKILÖSTÖNUMERO                | cdm\_workerid.cdm\_workernumber                      |
| TOIMINTO                         | cdm\_eventid.cdm\_name                               |
| VAIHE                           | cdm\_referencepointsetuplineid.cdm\_name             |
| REFPOINTSETUPID                | cdm\_referencepointsetuplineid.cdm\_referencepointsetupid.cdm\_name |

### <a name="employment-per-company-to-employment"></a>Työsuhteita yritystä kohti työsuhteeseen

| Talousyksikkö                 | Dataverse-taulu                                    | 
|--------------------------------|----------------------------------------------------|
| EMPLOYMENTENDDATE              | cdm\_employmentenddate                              |
| HENKILÖSTÖNUMERO                | cdm\_workerid.cdm\_workernumber                      |
| EMPLOYMENTSTARTDATE            | cdm\_employmentstartdate                            |
| WORKERTYPE                     | cdm\_workertype                                     |
| DIMENSIONDISPLAYVALUE          | cdm\_dimensiondisplayvalue                          |
| ADJUSTEDWORKERSTARTDATE        | cdm\_adjustedworkerstartdate                        |
| EMPLOYERNOTICEAMOUNT           | cdm\_employernoticeamount                           |
| EMPLOYERUNITOFNOTICE           | cdm\_employerunitofnotice                           |
| WORKERUNITOFNOTICE             | cdm\_workerunitofnotice                             |
| WORKERNOTICEAMOUNT             | cdm\_workernoticeamount                             |
| LASTDATEWORKED                 | cdm\_lastdateworked                                 |
| PROBATIONENDDATE               | cdm\_probationenddate                               |
| TRANSITIONDATE                 | cdm\_transitiondate                                 |
| TRANSITIONREASONCODENAME       | cdm\_transitionreasoncode.cdm\_name                  |
| WORKERSTARTDATE                | cdm\_workerstartdate                                |
| VALIDTO                        | cdm\_validto                                        |
| VALIDFROM                      | cdm\_validfrom                                      |

### <a name="ethnic-origins-to-ethnic-origin"></a>Etniset alkuperät etniseen alkuperään

| Talousyksikkö                 | Dataverse-taulu                                    | 
|--------------------------------|----------------------------------------------------|
| ETHNICORIGINID                 | cdm\_name                                           |
| KUVAUS                    | cdm\_description                                    |

### <a name="group-assignment-to-business-process-group-assignment"></a>Ryhmämääritys liiketoimintaprosessin ryhmämääritykseen

| Talousyksikkö                 | Dataverse-taulu                                    | 
|--------------------------------|----------------------------------------------------|
| NIMI                           | cdm\_name                                           |
| KUVAUS                    | cdm\_description                                    |
| ISACTIVE                       | cdm\_isactive                                       |

### <a name="identification-type-to-worker-person-identification-type"></a>Tunnuksen tyyppi työntekijän henkilötunnuksen tyyppiin

| Talousyksikkö                 | Dataverse-taulu                                    | 
|--------------------------------|----------------------------------------------------|
| KUVAUS                    | cdm\_description                                    |
| IDENTIFICATIONTYPEID           | cdm\_name                                           |
| ALLOWEDVALUES                  | cdm\_allowedvalues                                  |
| FIXEDLENGTH                    | cdm\_fixedlength                                    |
| IDENTIFICATIONNUMBERFORMAT     | cdm\_identificationnumberformat                     |

### <a name="issuing-agency-to-person-identification-issuing-agency"></a>Myöntäjätaho henkilötunnuksen myöntäjätahoon

| Talousyksikkö                 | Dataverse-taulu                                    | 
|--------------------------------|----------------------------------------------------|
| SÄHKÖPOSTI                          | cdm\_email                                          |
| ALANUMERO                      | cdm\_extension                                      |
| FAKSI                            | cdm\_fax                                            |
| ISSUINGAGENCY                  | cdm\_name                                           |
| MOBILEPHONE                    | cdm\_mobilephone                                    |
| INTERNETADDRESS                | cdm\_websiteurl                                     |
| NIMI                           | cdm\_description                                    |
| HAKULAITE                          | cdm\_pager                                          |
| Tekstiviesti                            | cdm\_sms                                            |
| PUHELIN                      | cdm\_telephone                                      |
| TELEXNUMBER                    | cdm\_telex                                          |
| ADDRESSCITY                    | cdm\_city                                           |
| ADDRESSCOUNTY                  | cdm\_county                                         |
| ADDRESSDESCRIPTION             | cdm\_addressdescription                             |
| ADDRESSSTATE                   | cdm\_stateorprovince                                |
| ADDRESSSTREET                  | cdm\_street                                         |
| ADDRESSZIPCODE                 | cdm\_postalcode                                     |
| ADDRESSCOUNTRYREGIONISOCODE    | cdm\_countryregion                                  |

### <a name="job-positions-dual-write-to-job-position"></a>Toimien kaksoiskirjoitus toimeen

| Talousyksikkö                 | Dataverse-taulu                                    | 
|--------------------------------|----------------------------------------------------|
| POSITIONID                     | cdm\_jobpositionnumber                              |
| AKTIVOINTI                     | cdm\_activation                                     |
| AVAILABLEFORASSIGNMENT         | cdm\_availableforassignment                         |
| COMPENSATIONREGIONID           | cdm\_compensationregionid.cdm\_name                  |
| DEPARTMENTID                   | cdm\_departmentid.cdm\_departmentnumber              |
| KUVAUS                    | cdm\_description                                    |
| FULLTIMEEQUIVALENT             | cdm\_fulltimeequivalent                             |
| JOBID                          | cdm\_jobid.cdm\_name                                 |
| PARENTPOSITIONID               | cdm\_parentjobpositionid.cdm\_jobpositionnumber      |
| POSITIONTYPEID                 | cdm\_positiontypeid.cdm\_name                        |
| ELÄKKEELLE SIIRTYMINEN                     | cdm\_retirement                                     |
| TITLEID                        | cdm\_titleid.cdm\_name                               |
| VALIDFROM                      | cdm\_validfrom                                      |
| VALIDTO                        | cdm\_validto                                        |

### <a name="jobs-dual-write-to-job"></a>Töiden kaksoinkirjoitus työhön

| Talousyksikkö                 | Dataverse-taulu                                    | 
|--------------------------------|----------------------------------------------------|
| JOBID                          | cdm\_name                                           |
| KUVAUS                    | cdm\_description                                    |
| JOBDESCRIPTION                 | cdm\_jobdescription                                 |
| ALLOWUNLIMITEDPOSITIONS        | cdm\_allowunlimitedpositions                        |
| MAXIMUMNUMBEROFPOSITIONS       | cdm\_maximumnumberofpositions                       |
| JOBFUNCTIONID                  | cdm\_jobfunctionid.cdm\_name                         |
| JOBTYPEID                      | cdm\_jobtypeid.cdm\_name                             |
| TITLEID                        | cdm\_titleid.cdm\_name                               |
| VALIDFROM                      | cdm\_validfrom                                      |
| VALIDTO                        | cdm\_validto                                        |
| DEFAULTFULLTIMEEQUIVALENCY     | cdm\_defaultfulltimeequivalent                      |

### <a name="language-codes-to-language"></a>Kielikoodit kieleen

| Talousyksikkö                 | Dataverse-taulu                                    | 
|--------------------------------|----------------------------------------------------|
| LANGUAGECODEID                 | cdm\_name                                           |
| KUVAUS                    | cdm\_description                                    |

### <a name="leave-and-absence-bank-transaction-v2-to-leave-bank-transaction"></a>Loma- ja poissaolopankin tapahtuma V2 lomapankkitapahtumaan

| Talousyksikkö                 | Dataverse-taulu                                    | 
|--------------------------------|----------------------------------------------------|
| SUMMA                         | cdm\_amount                                         |
| LEAVETYPEID                    | cdm\_leavetypeid.cdm\_type                           |
| LEAVEPLANID                    | cdm\_leaveplanid.cdm\_name                           |
| TRANSACTIONDATE                | cdm\_transactiondate                                |
| TRANSACTIONNUMBER              | cdm\_transactionnumber                              |
| HENKILÖSTÖNUMERO                | cdm\_workerid.cdm\_workernumber                      |
| TRANSACTIONTYPE                | cdm\_transactiontype                                |

### <a name="leave-and-absence-enrollment-v2-to-leave-enrollment"></a>Loman ja poissaolon rekisteröinti V2 lomarekisteröintiin

| Talousyksikkö                 | Dataverse-taulu                                    | 
|--------------------------------|----------------------------------------------------|
| STARTDATE                      | cdm\_startdate                                      |
| ENDDATE                        | cdm\_enddate                                        |
| CUSTOMDATE                     | cdm\_customdate                                     |
| ACCRUALSTARTDATE               | cdm\_accrualstartdate                               |
| ACCRUALDATEBASIS               | cdm\_accrualdatebasis                               |
| ISACCRUALSUSPENDED             | cdm\_isaccrualsuspended                             |
| LEAVEPLANID                    | cdm\_leaveplanid.cdm\_name                           |
| TIERBASIS                      | cdm\_tierbasis                                      |
| HENKILÖSTÖNUMERO                | cdm\_workerid.cdm\_workernumber                      |

### <a name="leave-and-absence-plan-v2-to-leave-plan"></a>Loma- ja poissaolosuunnitelma V2 lomasuunnitelmaan

| Talousyksikkö                 | Dataverse-taulu                                    | 
|--------------------------------|----------------------------------------------------|
| ACCRUALFREQUENCY               | cdm\_accrualfrequency                               |
| NIMI                           | cdm\_name                                           |
| KUVAUS                    | cdm\_description                                    |
| STARTDATE                      | cdm\_startdate                                      |
| LEAVETYPEID                    | cdm\_leavetypeid.cdm\_type                           |

### <a name="leave-and-absence-type-to-leave-type"></a>Loman ja poissaolon tyyppi lomatyyppiin

| Talousyksikkö                 | Dataverse-taulu                                    | 
|--------------------------------|----------------------------------------------------|
| KUVAUS                    | cdm\_description                                    |
| TYYPPI                           | cdm\_type                                           |
| EARNINGCODEID                  | cdm\_earningcodeid.cdm\_name                         |

### <a name="leave-and-absence-type-reason-code-to-leave-type-reason-code"></a>Loman ja poissaolon tyypin syykoodi lomatyypin syykoodiin

| Talousyksikkö                 | Dataverse-taulu                                    | 
|--------------------------------|----------------------------------------------------|
| LEAVETYPE                      | cdm\_typeid.cdm\_type                                |
| REASONCODEID                   | cdm\_reasoncodeid.cdm\_name                          |

### <a name="leave-time-off-request-detail-to-leave-request-detail"></a>Loma- ja poissaolopyynnön tiedot lomapyynnön tietoihin

| Talousyksikkö                 | Dataverse-taulu                                    | 
|--------------------------------|----------------------------------------------------|
| SUMMA                         | cdm\_amount                                         |
| LEAVEDATE                      | cdm\_leavedate                                      |
| REQUESTID                      | cdm\_leaverequestid.cdm\_leaverequestnumber          |
| TYYPPI                           | cdm\_leavetypeid.cdm\_type                           |

### <a name="leave-time-off-request-header-to-leave-request"></a>Lomien ja poissaolojen pyynnön otsikko lomapyyntöön

| Talousyksikkö                 | Dataverse-taulu                                    | 
|--------------------------------|----------------------------------------------------|
| REQUESTID                      | cdm\_leaverequestnumber                             |
| REQUESTDATE                    | cdm\_requestdate                                    |
| TILA                         | cdm\_status                                         |
| KOMMENTTI                        | cdm\_comment                                        |
| HENKILÖSTÖNUMERO                | cdm\_workerid.cdm\_workernumber                      |

### <a name="levels-to-compensation-level"></a>Tasot kompensaatiotasoon

| Talousyksikkö                 | Dataverse-taulu                                    | 
|--------------------------------|----------------------------------------------------|
| TYYPPI                           | cdm\_type                                           |
| KUVAUS                    | cdm\_description                                    |
| TASO                          | cdm\_name                                           |

### <a name="onboarding-process-header-to-onboard-process-header"></a>Perehdytysprosessin otsikko perehdytysprosessin otsikkoon

| Talousyksikkö                 | Dataverse-taulu                                    | 
|--------------------------------|----------------------------------------------------|
| PROCESSID                      | cdm\_processheaderid.cdm\_processid                  |
| ONBOARDEDEMPLOYEEPERSONNELNUMBER | cdm\_onboardedemployeeid.cdm\_workernumber           |
| EMPLOYMENTPERSONNELNUMBER      | cdm\_employmentid.cdm\_workerid.cdm\_workernumber     |
| LEGALENTITYID                  | cdm\_employmentid.cdm\_companyid.cdm\_companycode     |
| EMPLOYMENTSTARTDATE            | cdm\_employmentid.cdm\_employmentstartdate           |

### <a name="pay-cycle-to-pay-cycle"></a>Maksujakso maksujaksoon

| Talousyksikkö                 | Dataverse-taulu                                    | 
|--------------------------------|----------------------------------------------------|
| PAYCYCLEID                     | cdm\_name                                           |
| KUVAUS                    | cdm\_description                                    |
| PAYCYCLEFREQUENCY              | cdm\_frequency                                      |

### <a name="pay-period-to-pay-period"></a>Maksukausi maksukauteen

| Talousyksikkö                 | Dataverse-taulu                                    | 
|--------------------------------|----------------------------------------------------|
| COMMENTS                       | cdm\_description                                    |
| DEFAULTPAYMENTDATE             | cdm\_defaultpaymentdate                             |
| PAYCYCLEID                     | cdm\_paycycleid.cdm\_name                            |
| PERIODENDDATE                  | cdm\_periodenddate                                  |
| PERIODSTARTDATE                | cdm\_periodstartdate                                |
| TILA                         | cdm\_status                                         |

### <a name="payroll-details-for-positions-to-payroll-position-detail"></a>Palkanlaskennan tiedot toimista palkanlaskennan toimen tietoihin

| Talousyksikkö                 | Dataverse-taulu                                    | 
|--------------------------------|----------------------------------------------------|
| PAYCYCLEID                     | cdm\_paycycle.cdm\_name                              |
| POSITIONID                     | cdm\_position.cdm\_jobpositionnumber                 |
| VALIDFROM                      | cdm\_validfrom                                      |
| VALIDTO                        | cdm\_validto                                        |
| ANNUALREGULARHOURS             | cdm\_annualregularhours                             |
| PAIDBYLEGALENTITY              | cdm\_paidby.cdm\_companycode                         |

### <a name="position-default-dimensions-dual-write-to-job-position-dimension"></a>Toimen oletusdimensioiden kaksoiskirjoitus toimen oletusdimensioihin

| Talousyksikkö                 | Dataverse-taulu                                    | 
|--------------------------------|----------------------------------------------------|
| DIMENSIONDISPLAYVALUE          | cdm\_dimensiondisplayvalue                          |
| POSITIONID                     | cdm\_jobpositionid.cdm\_jobpositionnumber            |

### <a name="position-type-to-position-type"></a>Toimityyppi toimityyppiin

| Talousyksikkö                 | Dataverse-taulu                                    | 
|--------------------------------|----------------------------------------------------|
| POSITIONTYPEID                 | cdm\_name                                           |
| KUVAUS                    | cdm\_description                                    |
| LUOKITTELU                 | cdm\_classification                                 |

### <a name="position-worker-assignments-v2-to-position-worker-assignment"></a>Toimen työntekijän toimeksiannot V2 toimen työntekijän toimeksiantoon

| Talousyksikkö                 | Dataverse-taulu                                    | 
|--------------------------------|----------------------------------------------------|
| HENKILÖSTÖNUMERO                | cdm\_workerid.cdm\_workernumber                      |
| POSITIONID                     | cdm\_jobpositionid.cdm\_jobpositionnumber            |
| VALIDFROM                      | cdm\_validfrom                                      |
| VALIDTO                        | cdm\_validto                                        |
| IsPrimaryPosition              | cdm\_isprimaryposition                              |

### <a name="reason-codes-to-reason-code"></a>Syykoodit syykoodiin

| Talousyksikkö                 | Dataverse-taulu                                    | 
|--------------------------------|----------------------------------------------------|
| REASONCODEID                   | cdm\_name                                           |
| KUVAUS                    | cdm\_description                                    |
| ISABSENCEAPPLICABLE            | cdm\_isabsenceapplicable                            |
| ISAPPLICATIONAPPLICABLE        | cdm\_isapplicationapplicable                        |
| ISCOMPENSATIONAPPLICABLE       | cdm\_iscompensationapplicable                       |
| ISCREATENEWPOSITIONAPPLICABLE  | cdm\_iscreatenewpositionapplicable                  |
| ISEDITPOSITIONAPPLICABLE       | cdm\_iseditpositionapplicable                       |
| ISHIREAPPLICABLE               | cdm\_ishireapplicable                               |
| ISSKILLMAPPINGAPPLICABLE       | cdm\_isskillmappingapplicable                       |
| ISTERMINATIONAPPLICABLE        | cdm\_isterminationapplicable                        |
| ISTRANSFERAPPLICABLE           | cdm\_istransferapplicable                           |

### <a name="reference-point-setup-line-dual-write-to-compensation-reference-point-setup-line"></a>Viitepisteen asetusrivit (kaksoiskirjoitus) kompensaation viitepisteen määritysriviin

| Talousyksikkö                 | Dataverse-taulu                                    | 
|--------------------------------|----------------------------------------------------|
| KUVAUS                    | cdm\_description                                    |
| LINENUM                        | cdm\_linenumber                                     |
| REFPOINTID                     | cdm\_name                                           |
| REFPOINTSETUPID                | cdm\_referencepointsetupid.cdm\_name                 |

### <a name="reference-point-setups-to-compensation-reference-point-setup"></a>Viitepisteiden määritykset kompensaation viitepistemääritykseen

| Talousyksikkö                 | Dataverse-taulu                                    | 
|--------------------------------|----------------------------------------------------|
| REFERENCESETUP                 | cdm\_name                                           |
| KUVAUS                    | cdm\_description                                    |
| TYYPPI                           | cdm\_compensationtype                               |

### <a name="skill-types-to-skill-type"></a>Osaamisaluetyypit osaamisaluetyyppeihin

| Talousyksikkö                 | Dataverse-taulu                                    | 
|--------------------------------|----------------------------------------------------|
| SKILLTYPE                      | cdm\_name                                           |
| KUVAUS                    | cdm\_description                                    |

### <a name="titles-to-title"></a>Otsikot otsikkoon

| Talousyksikkö                 | Dataverse-taulu                                    | 
|--------------------------------|----------------------------------------------------|
| TITLEID                        | cdm\_name                                           |

### <a name="variable-compensation-level-v2-to-compensation-variable-plan-level"></a>Muuttuva kompensaation taso V2 muuttuvaan kompensaatiosuunnitelman tasoon

| Talousyksikkö                 | Dataverse-taulu                                    | 
|--------------------------------|----------------------------------------------------|
| AWARDAMOUNT                    | cdm\_awardamount                                    |
| AWARDPERCENT                   | cdm\_awardpercent                                   |
| AWARDUNITSREAL                 | cdm\_awardunits                                     |
| COMPENSATIONLEVELID            | cdm\_compensationlevelid.cdm\_name                   |
| PLANID                         | cdm\_compensationvariableplanid.cdm\_name            |

### <a name="veteran-status-to-veteran-status"></a>Sotaveteraanitila sotaveteraanitilaan

| Talousyksikkö                 | Dataverse-taulu                                    | 
|--------------------------------|----------------------------------------------------|
| VETERANSTATUSID                | cdm\_name                                           |
| KUVAUS                    | cdm\_description                                    |
| ISPROTECTEDVETERAN             | cdm\_isprotectedveteran                             |

### <a name="work-calendar-enrollments-to-work-calendar-enrollment"></a>Työkalenterin rekisteröinnit työkalenterin rekisteröinteihin

| Talousyksikkö                 | Dataverse-taulu                                    | 
|--------------------------------|----------------------------------------------------|
| STARTDATE                      | cdm\_employmentid.cdm\_employmentstartdate           |
| HENKILÖSTÖNUMERO                | cdm\_employmentid.cdm\_workerid.cdm\_workernumber     |
| CALENDARID                     | cdm\_workcalendarid.cdm\_name                        |
| COMPANYID                      | cdm\_employmentid.cdm\_companyid.cdm\_companycode     |

### <a name="work-calendar-holiday-to-work-calendar-holiday"></a>Työkalenterin lomapäivä työkalenterin lomapäivään

| Talousyksikkö                 | Dataverse-taulu                                    | 
|--------------------------------|----------------------------------------------------|
| Tunnus                             | cdm\_name                                           |
| KUVAUS                    | cdm\_description                                    |

### <a name="work-calendar-holiday-line-to-work-calendar-holiday-line"></a>Työkalenterin lomapäivärivi työkalenterin lomapäiväriviin

| Talousyksikkö                 | Dataverse-taulu                                    | 
|--------------------------------|----------------------------------------------------|
| HOLIDAYID                      | cdm\_workcalendarholidayid.cdm\_name                 |
| NIMI                           | cdm\_name                                           |
| HOLIDAYDATE                    | cdm\_holidaydate                                    |

### <a name="worker-to-worker"></a>Työntekijä työntekijään

| Talousyksikkö                 | Dataverse-taulu                                    | 
|--------------------------------|----------------------------------------------------|
| HENKILÖSTÖNUMERO                | cdm\_workernumber                                   |
| FIRSTNAME                      | cdm\_firstname                                      |
| MIDDLENAME                     | cdm\_middlename                                     |
| LASTNAME                       | cdm\_lastname                                       |
| WORKERTYPE                     | cdm\_type                                           |
| WORKERSTATUS                   | cdm\_status                                         |
| PRIMARYCONTACTEMAIL            | cdm\_primaryemailaddress                            |
| PRIMARYCONTACTPHONE            | cdm\_primarytelephone                               |
| PRIMARYCONTACTFACEBOOK         | cdm\_facebookidentity                               |
| PRIMARYCONTACTTWITTER          | cdm\_twitteridentity                                |
| PRIMARYCONTACTLINKEDIN         | cdm\_linkedinidentity                               |
| PRIMARYCONTACTURL              | cdm\_websiteurl                                     |
| GENDER                         | cdm\_gender                                         |
| BIRTHDATE                      | cdm\_birthdate                                      |
| NIMI                           | cdm\_fullname                                       |

### <a name="worker-bank-accounts-to-worker-bank-account"></a>Työntekijän pankkitilit työntekijän pankkitiliin

| Talousyksikkö                 | Dataverse-taulu                                    | 
|--------------------------------|----------------------------------------------------|
| ACCOUNTIDENTIFICATION          | cdm\_accountidentification                          |
| ADDRESSCITY                    | cdm\_city                                           |
| ADDRESSCOUNTRYREGIONID         | cdm\_countryorregion                                |
| ADDRESSCOUNTY                  | cdm\_county                                         |
| ADDRESSDESCRIPTION             | cdm\_addressdescription                             |
| ADDRESSDISTRICTNAME            | cdm\_districtname                                   |
| ADDRESSPOSTBOX                 | cdm\_postofficebox                                  |
| ADDRESSSTATE                   | cdm\_stateorprovince                                |
| ADDRESSZIPCODE                 | cdm\_postalcode                                     |
| HENKILÖSTÖNUMERO                | cdm\_workerid.cdm\_workernumber                      |
| BANKACCOUNTNUMBER              | cdm\_bankaccountnumber                              |
| BANKACCOUNTTYPE                | cdm\_bankaccounttype                                |
| SÄHKÖPOSTI                          | cdm\_email                                          |
| ALANUMERO                      | cdm\_extension                                      |
| FAKSI                            | cdm\_fax                                            |
| INTERNETADDRESS                | cdm\_websiteurl                                     |
| MOBILEPHONE                    | cdm\_mobilephone                                    |
| ROUTINGNUMBER                  | cdm\_routingnumber                                  |
| PUHELIN                      | cdm\_telephone                                      |
| TELEXNUMBER                    | cdm\_telexnumber                                    |
| BANKIBAN                       | cdm\_iban                                           |
| SWIFTNO                        | cdm\_swiftcode                                      |
| BANKLOCATIONCODE               | cdm\_banklocationcode                               |
| BRANCHNAME                     | cdm\_branchname                                     |
| BRANCHNUMBER                   | cdm\_branchnumber                                   |
| ROUTINGNUMBERTYPE              | cdm\_routingnumbertype                              |
| ACCOUNTHOLDER                  | cdm\_accountholder                                  |
| NAMEOFPERSON                   | cdm\_nameofperson                                   |
| NIMI                           | cdm\_description                                    |
| ADDRESSSTREET                  | cdm\_line1                                          |
| ADDRESSSTREETNUMBER            | cdm\_line2                                          |

### <a name="worker-personal-details-to-worker-personal-detail"></a>Työntekijän henkilötiedot työntekijän henkilötietoihin

| Talousyksikkö                 | Dataverse-taulu                                    | 
|--------------------------------|----------------------------------------------------|
| HENKILÖSTÖNUMERO                | cdm\_workerid.cdm\_workernumber                      |
| BIRTHDATE                      | cdm\_birthdate                                      |
| PERSONBIRTHCITY                | cdm\_birthcity                                      |
| GENDER                         | cdm\_gender                                         |
| EXPATRIATEENDDATE              | cdm\_expatriateenddate                              |
| EXPATRIATESTARTDATE            | cdm\_expatriatestartdate                            |
| DISABLEDVETERAN                | cdm\_isdisabledveteran                              |
| DECEASEDDATE                   | cdm\_deceaseddate                                   |
| DISABLEDVERIFICATIONDATE       | cdm\_disabledveteranverificationdate                |
| KOULUTUS                      | cdm\_education                                      |
| ETHNICORIGINID                 | cdm\_ethnicoriginid.cdm\_name                        |
| ISDISABLED                     | cdm\_isdisabled                                     |
| ISFULLTIMESTUDENT              | cdm\_isfulltimestudent                              |
| ISEXPATRIATERULINGAPPLICABLE   | cdm\_isexpatriaterulingapplicable                   |
| MARITALSTATUS                  | cdm\_maritalstatus                                  |
| MILITARYSERVICESTARTDATE       | cdm\_militaryservicestartdate                       |
| MILITARYSERVICEENDDATE         | cdm\_militaryserviceenddate                         |
| NUMBEROFDEPENDENTS             | cdm\_numberofdependents                             |
| NATIVELANGUAGEID               | cdm\_nativelanguageidid.cdm\_name                    |
| NATIONALITYCOUNTRYREGION       | cdm\_nationalitycountryregion                       |
| PERSONBIRTHCOUNTRYREGION       | cdm\_birthcountryregion                             |
| FATHERBIRTHCOUNTRYREGION       | cdm\_fatherbirthcountryregion                       |
| MOTHERBIRTHCOUNTRYREGION       | cdm\_motherbirthcountryregion                       |
| CITIZENSHIPCOUNTRYREGION       | cdm\_citizenshipcountryregion                       |
| VETERANSTATUSID                | cdm\_veteranstatusid.cdm\_name                       |

### <a name="worker-postal-addresses-dual-write-to-worker-address"></a>Työntekijän postiosoitteiden kaksoiskirjoitus työntekijän osoitteeseen

| Talousyksikkö                 | Dataverse-taulu                                    | 
|--------------------------------|----------------------------------------------------|
| HENKILÖSTÖNUMERO                | cdm\_workerid.cdm\_workernumber                      |
| ADDRESSLOCATIONID              | cdm\_addressnumber                                  |
| ADDRESSLOCATIONROLES           | cdm\_addresstype                                    |
| VOIMASSA                      | cdm\_effectivedate                                  |
| PÄÄTTYMINEN                     | cdm\_expirationdate                                 |
| ADDRESSSTREET                  | cdm\_street                                         |
| ADDRESSSTREETNUMBER            | cdm\_streetnumber                                   |
| ADDRESSCITY                    | cdm\_city                                           |
| ADDRESSCOUNTRYREGIONISOCODE    | cdm\_countryregion                                  |
| ADDRESSSTATE                   | cdm\_stateorprovince                                |
| ADDRESSCOUNTYID                | cdm\_county                                         |
| ADDRESSDESCRIPTION             | cdm\_description                                    |
| ADDRESSLATITUDE                | cdm\_latitude                                       |
| ADDRESSLONGITUDE               | cdm\_longitude                                      |
| ADDRESSZIPCODE                 | cdm\_postalcode                                     |
| ADDRESSPOSTBOX                 | cdm\_postofficebox                                  |
| ISPRIMARY                      | cdm\_ispreferred                                    |

### <a name="working-time-to-work-calendar-time-interval"></a>Työaika työkalenterin aikajaksoon

| Talousyksikkö                 | Dataverse-taulu                                    | 
|--------------------------------|----------------------------------------------------|
| ENDTIME                        | cdm\_endtime                                        |
| STARTTIME                      | cdm\_starttime                                      |
| WORKCALENDARDATE               | cdm\_workcalendardayid.cdm\_calendardate             |
| WORKCALENDARID                 | cdm\_workcalendarid.cdm\_name                        |
| WORKCALENDARID                 | cdm\_workcalendardayid.cdm\_workcalendarid.cdm\_name  |

### <a name="working-times-to-work-calendar-day"></a>Työajat työkalenterin päivään

| Talousyksikkö                 | Dataverse-taulu                                    | 
|--------------------------------|----------------------------------------------------|
| CALENDARDATE                   | cdm\_calendardate                                   |
| WORKCALENDARID                 | cdm\_workcalendarid.cdm\_name                        |
| WORKINGDAYDEFINITION           | cdm\_status                                         |

## <a name="integration-considerations"></a>Integrointinäkökohdat

- Toinen järjestelmä vahvistaa kaikki jommassakummassa järjestelmässä tietoihin tehdyt muutokset. Virhetilanteessa tietoja ei kirjoitata kumpaankaan järjestelmään. 
- Tietojen palautuminen oletusarvoihin koskee kaikki kirjoituksia (jos mukautettu logiikka tapahtuu Financessa).
- Kaksoiskirjoituksen integrointisovellus käyttää integrointiavaimia kahden järjestelmän välillä tehtävän yhdistämiseen. Joskus oikean integrointiavaimen valinta on hankalaa etenkin, jos monet integrointiavaimet vastaavat vaatimuksia. Seuraavassa taulukossa on ehdotuksia helpottamaan yhdistämismääritysten integrointiavoimien valintaa.

| Dataverse-taulu                          | Integrointiavaimet |
|------------------------------------------|------------------|
| Pankkitilisuoritukset                | cdm\_bankaccountid.cdm\_accountidentification, cdm\_bankaccountid.cdm\_workerid.cdm\_workernumber, cdm\_companyid.cdm\_companycode |
| Edun laskentatiheys            | cdm\_name |
| Edun laskennan toistuvuuden maksukausi | cdm\_payperiodid.cdm\_periodstartdate, cdm\_payperiodid.cdm\_paycycleid.cdm\_name, cdm\_benefitcalculationfrequencyid.cdm\_name |
| Edun laskentahinta                 | cdm\_name |
| Edun laskentahinnan tiedot          | cdm\_workerdeduction, cdm\_effective, cdm\_calculationrateid.cdm\_name |
| Etuusvaihtoehto                           | cdm\_name |
| Edun tyyppi                             | cdm\_name |
| Liiketoimintaprosessin kalenteri                | cdm\_name |
| Liiketoimintaprosessin ryhmämääritys        | cdm\_name |
| Liiketoimintaprosessin otsikko                  | cdm\_processid |
| Liiketoimintaprosessikirjaston tehtäväryhmä      | cdm\_processtype, cdm\_name |
| Liiketoimintaprosessin vaihe                   | cdm\_name, cdm\_businessprocesstype, cdm\_companyid.cdm\_companycode |
| Liiketoimintaprosessin tehtävä                    | cdm\_taskid |
| Liiketoimintayksikkö                            | |
| Tarkistusluettelomallin otsikko                | cdm\_businessprocesstype, cdm\_name, cdm\_genericsubtype |
| Tarkistusluettelomallin tehtävä                  | cdm\_taskid |
| Yhtiö                                  | cdm\_companycode |
| Kiinteä kompensaatiosuunnitelma                  | cdm\_name, cdm\_company.cdm\_companycode |
| Kompensaatioruudukko                        | cdm\_name, cdm\_companyid.cdm\_companycode |
| Kompensaatiotaso                       | cdm\_name |
| Kompensaation maksutiheys               | cdm\_name, cdm\_companyid.cdm\_companycode |
| Kompensaation viitepisteiden asetukset       | cdm\_name, cdm\_companyid.cdm\_companycode |
| Kompensaation viitepisteen asetusrivi  | cdm\_name, cdm\_referencepointsetupid.cdm\_name, cdm\_referencepointsetupid.cdm\_companyid.cdm\_companycode |
| Kompensaatioalue                      | cdm\_name |
| Kompensaatiorakenne                   | cdm\_compensationlevelid.cdm\_name, cdm\_referencepointid.cdm\_name, cdm\_referencepointid.cdm\_referencepointsetupid.cdm\_name, cdm\_referencepointid.cdm\_referencepointsetupid.cdm\_companyid.cdm\_companycode, cdm\_companyid.cdm\_companycode, cdm\_compensationgridid.cdm\_name, cdm\_compensationgridid.cdm\_companyid.cdm\_companycode |
| Muuttuva kompensaatiosuunnitelma               | cdm\_name, cdm\_companyid.cdm\_companycode |
| Muuttuvan kompensaatiosuunnitelman taso         | cdm\_companyid.cdm\_companycode, cdm\_compensationvariableplanid.cdm\_name, cdm\_compensationvariableplanid.cdm\_companyid.cdm\_companycode, cdm\_compensationlevelid.cdm\_name |
| Muuttuvan kompensaatiosuunnitelman tyyppi          | cdm\_name, cdm\_companyid.cdm\_companycode |
| Valuutta                                 | isocurrencycode |
| Osasto                               | cdm\_departmentnumber |
| Työsuhde                               | cdm\_employmentstartdate, cdm\_workerid.cdm\_workernumber, cdm\_companyid.cdm\_companycode |
| Etninen alkuperä                            | cdm\_name |
| Kiinteä kompensaatiotapahtuma                 | cdm\_name, cdm\_companyid.cdm\_companycode |
| Tehtävä                                      | cdm\_name |
| Työtehtävä                             | cdm\_name |
| Toimi                             | cdm\_jobpositionnumber |
| Toimen dimensio                   | cdm\_jobpositionid.cdm\_jobpositionnumber, cdm\_companyid.cdm\_companycode |
| Työlaji                                 | cdm\_name |
| Kieli                                 | cdm\_name |
| Lomapankkitapahtuma                   | cdm\_transactiondate, cdm\_transactiontype, cdm\_transactionnumber, cdm\_leavetypeid.cdm\_type, cdm\_leavetypeid.cdm\_companyid.cdm\_companycode, cdm\_companyid.cdm\_companycode, cdm\_workerid.cdm\_workernumber |
| Lomarekisteröinti                         | cdm\_startdate, cdm\_leaveplanid.cdm\_name, cdm\_leaveplanid.cdm\_companyid.cdm\_companycode, cdm\_companyid.cdm\_companycode, cdm\_workerid.cdm\_workernumber |
| Lomasuunnitelma                               | cdm\_name, cdm\_companyid.cdm\_companycode |
| Lomapyyntö                            | cdm\_leaverequestnumber, cdm\_companyid.cdm\_companycode |
| Lomapyynnön tiedot                     | cdm\_leavedate, cdm\_leavetypeid.cdm\_type, cdm\_leavetypeid.cdm\_companyid.cdm\_companycode, cdm\_leaverequestid.cdm\_leaverequestnumber, cdm\_leaverequestid.cdm\_companyid.cdm\_companycode |
| Lomatyyppi                               | cdm\_type, cdm\_companyid.cdm\_companycode |
| Lomatyypin syykoodi                   | cdm\_reasoncodeid.cdm\_name, cdm\_typeid.cdm\_type, cdm\_typeid.cdm\_companyid.cdm\_companycode |
| Perehdytysprosessin otsikko                   | cdm\_processheaderid.cdm\_processid |
| Organisaatio                             | |
| Maksujakso                                | cdm\_name |
| Maksukausi                               | cdm\_periodstartdate, cdm\_paycycleid.cdm\_name, cdm\_periodenddate |
| Palkkalaji                     | cdm\_name |
| Palkanlaskennan toimen tiedot                  | cdm\_validfrom, cdm\_validto, cdm\_position.cdm\_jobpositionnumber |
| Henkilötunnuksen myöntäjätaho     | cdm\_name |
| Toimityyppi                            | cdm\_name |
| Toimen työntekijän toimeksianto               | cdm\_validfrom, cdm\_jobpositionid.cdm\_jobpositionnumber |
| Syykoodi                              | cdm\_name |
| Osaamisaluetyyppi                               | cdm\_name |
| Verotusalue                               | cdm\_stateorprovince, cdm\_name, cdm\_countryorregion, cdm\_county, cdm\_city |
| Ryhmä                                     | azureactivedirectoryobjectid, membershiptype |
| Nimi                                    | cdm\_name |
| Käyttäjä                                     | azureactivedirectoryobjectid |
| Hyvityssääntö                             | cdm\_name, cdm\_companyid.cdm\_companycode |
| Sotaveteraanitila                           | cdm\_name |
| Työkalenteri                            | cdm\_name, cdm\_companyid.cdm\_companycode |
| Työkalenteripäivämäärä                        | cdm\_calendardate, cdm\_companyid.cdm\_companycode, cdm\_workcalendarid.cdm\_name, cdm\_workcalendarid.cdm\_companyid.cdm\_companycode |
| Työkalenterin rekisteröinti                 | cdm\_employmentid.cdm\_employmentstartdate, cdm\_employmentid.cdm\_workerid.cdm\_workernumber, cdm\_employmentid.cdm\_companyid.cdm\_companycode |
| Työkalenterin lomapäivä                    | cdm\_name |
| Työkalenterin lomapäivärivi               | cdm\_holidaydate, cdm\_workcalendarholidayid.cdm\_name |
| Työkalenterin aikaväli              | cdm\_starttime, cdm\_workcalendardayid.cdm\_calendardate, cdm\_workcalendardayid.cdm\_companyid.cdm\_companycode, cdm\_workcalendardayid.cdm\_workcalendarid.cdm\_name, cdm\_workcalendardayid.cdm\_workcalendarid.cdm\_companyid.cdm\_companycode, cdm\_companyid.cdm\_companycode, cdm\_workcalendarid.cdm\_name, cdm\_workcalendarid.cdm\_companyid.cdm\_companycode |
| Työntekijä                                   | cdm\_workernumber |
| Työntekijän osoite                           | cdm\_addressnumber, cdm\_addresstype, cdm\_workerid.cdm\_workernumber |
| Työntekijän pankkitili                      | cdm\_accountidentification, cdm\_workerid.cdm\_workernumber |
| Työntekijän kiinteä kompensaatio                | cdm\_linenumber, cdm\_effectivedate, cdm\_companyid.cdm\_companycode, cdm\_positionid.cdm\_jobpositionnumber, cdm\_workerid.cdm\_workernumber, cdm\_eventid.cdm\_name, cdm\_eventid.cdm\_companyid.cdm\_companycode, cdm\_planid.cdm\_name, cdm\_planid.cdm\_company.cdm\_companycode |
| Työntekijän tunnusnumero      | cdm\_identificationnumber, cdm\_workerid.cdm\_workernumber, cdm\_identificationtypeid.cdm\_name |
| Työntekijän tunnustyyppi        | cdm\_name |
| Työntekijän henkilötiedot                   | cdm\_workerid.cdm\_workernumber |
