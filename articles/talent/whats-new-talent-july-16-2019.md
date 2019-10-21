---
title: Dynamics 365 Talentin uudet ja muuttuneet ominaisuudet (16.6.2019)
description: Tässä ohjeaiheessa käsitellään Microsoft Dynamics 365 Talentin uusia tai muuttuneita ominaisuuksia.
author: Darinkramer
manager: AnnBe
ms.date: 07/16/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2019-07-16
ms.dyn365.ops.version: Talent
ms.openlocfilehash: fd70b29089a4bf05c8fa9e3591fdb22383ea0cdc
ms.sourcegitcommit: 434dd21450bddcd891aba0555b9853d9ba0afb6f
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/23/2019
ms.locfileid: "2009713"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-july-16-2019"></a>Dynamics 365 Talentin uudet ja muuttuneet ominaisuudet (16.6.2019)

[!include [banner](includes/banner.md)]

Tässä ohjeaiheessa käsitellään Microsoft Dynamics 365 Talentin uusia tai muuttuneita ominaisuuksia.

## <a name="changes-in-attract"></a>Attractin muutokset
Tässä julkaisussa on vähäisiä Dynamics 365 Talent: Attractin ohjelmakorjauksia.

### <a name="coming-soon-in-attract"></a>Tulossa pian Attractiin
#### <a name="job-approvals-appear-on-the-home-page"></a>Työn hyväksynnät näkyvät aloitussivulla

Hyväksynnät näkyvät koontinäytön **Hyväksynnät**-osassa. Hyväksyjät voivat tarkistaa **Vastuualueensa** hyväksynnät, jolloin työn tunnus, otsikko, muut hyväksyjät ja määritetty päivämäärä näkyvät. Käyttäjät, jotka lähettävät työn hyväksyttäväksi, voivat tarkastella töitään kohdassa **Mitä olet pyytänyt**, joka näyttää hyväksyjät, joiden on vielä hyväksyttävä lähetetty työ.

## <a name="changes-in-onboard"></a>Onboardin muutokset
Tässä julkaisussa on vähäisiä Dynamics 365 Talent: Onboard:n ohjelmakorjauksia.

## <a name="changes-in-core-hr"></a>Core HR:n muutokset
Tässä osassa kuvatut muutokset koskevat koontiversiota 8.1.2390.

### <a name="common-data-service-entities-that-now-support-custom-fields"></a>Mukautettuja kenttiä nyt tukevat Common Data Service -yksikköjä

- BusinessProcessCalendar                     
- BusinessProcessGroupAssignment         
- BusinessProcessStage                          
- BusinessProcessTemplateHeader          
- BusinessProcessTemplateTask            
- HcmBenefitOption                              
- HcmBenefitType                                  
- HcmCompensationGrid                            
- HcmCompensationLevel                          
- HcmCompensationPayFrequency                 
- HcmCompensationReferencePointSetup        
- HcmCompensationReferencePointSetupLine 
- HcmCompensationRegion                     
- HcmCompFixedPlanTable                     
- HcmEmployment                                
- HcmEthnicOrigin                                
- HcmFixedCompensationEvent                 
- HcmJob                                           
- HcmJobFunction
- HcmJobType
- HcmLanguageCode
- HcmPayrollCalculationFrequency
- HcmPosition
- HcmPositionType
- HcmSkillType
- HcmVeteranStatus
- HcmWorkCalendarHoliday
- HcmWorkCalendarHolidayLine
- HcmWorker
- HcmWorkerPersonalDetail
- LeaveType
- OMDepartment
- OMLegalEntity
- PayCycle
- PayPeriod
- PayrollBenefitCalculationRate
- PayrollBenefitCalculationRateDetail
- PayrollEarningCode

### <a name="unable-to-see-goals-and-reviews-in-manager-self-service"></a>Tavoitteita ja arvioita ei näytä esimiesten itsepalvelussa

Tämän viikon muutokset sallivat nyt ohitustason esimiesten tavoitteiden ja arviointien näyttämisen ja muokkaamisen esimiesten itsepalvelussa.

### <a name="goal-form-cannot-be-closed-after-a-user-edits-any-goal-field"></a>Tavoitelomaketta ei voi sulkea, kun käyttäjä muokkaa jotakin tavoitekenttää

Tämä versio korjaa ongelman, jossa tavoitelomake ei sulkeudu, kun **Sulje** valitaan.

### <a name="creating-new-goals-and-saving-displays-error"></a>Uusien tavoitteiden luominen ja tallentaminen näyttää virheen

Tämä versio korjaa tavoitteiden tallentamista koskevan ongelman työntekijän ja esimiehen itsepalvelussa.

### <a name="unable-to-add-a-field-to-position-details"></a>Kenttää ei voi lisätä toimen tietoihin 

Tässä versiossa mukautettuja kenttiä tuetaan nyt toimen tiedoissa.
 
### <a name="unable-to-set-up-expiring-date-on-the-earning-code-through-data-management"></a>Ansiokoodin päättymispäivää ei voitu määrittää tietojen hallinnan kautta

Muutokset sallivat nyt ansiokoodien vanhentumispäivien määrittämisen tietojen hallinnassa

### <a name="new-custom-fields-dont-sync-quickly-enough"></a>Uudet mukautetut kentät eivät synkronoidu riittävän nopeasti

Mukautetun kentän synkronointia Common Data Serviceen on nyt parannettu tämän viikon julkaisussa.

### <a name="entity-export-to-database-jobs-fail-with-error-message-format-of-the-initialization-string-does-not-conform-to-specification-starting-at-index-0"></a>Yksikön vienti tietokantatöihin epäonnistuu ja näkyvissä on seuraava virhesanoma: Alustusmerkkijonon muoto ei ole indeksistä (0) alkavan määrityksen mukainen.

Tämä julkaisu korjaa ongelman, jossa tietokannan erätyöt epäonnistuvat. Manuaalinen päivitys:

1. Valitse **Tietojen hallinta**.
2. Valitse **Konfiguroi yksiköiden vienti tietokantaan**.
3. Anna kohdetietokannan yhteysmerkkijono uudelleen ja valitse **Tallenna**.

### <a name="smtp-email-configuration-suddenly-fails-with-error-message-the-smtp-server-requires-a-secure-connection-or-the-client-was-not-authenticated"></a>SMTP-sähköpostimäärityksessä epäonnistuu äkillisesti ja näkyvissä on seuraava virhesanoma: SMTP-palvelin edellyttää suojatun yhteyden, tai asiakasta ei todennettu.

Tämä julkaisu korjaa SMTP-sähköpostimäärityksen, joka epäonnistuu äkillisesti. Manuaalinen päivitys:

1. Valitse **Järjestelmän hallinta**.
2. Valitse **Sähköpostiparametrit**.
3. Valitse **SMTP-asetukset**. 
4. Anna SMTP-palvelimessa käytettävä käyttäjänimi ja salasana uudelleen ja valitse **Tallenna**.

## <a name="in-preview"></a>Esiversiossa

### <a name="preview-features-are-enabled-only-in-sandbox-instances"></a>Esiversiotoiminnot on otettu käyttöön vain eristysympäristöissä

Voit määrittää Talentin uutta esiintymää valmisteltaessa, onko esiintymän tyyppi **Tuotanto** vai **Eristys**. **Eristys**-tyypin esiintymissä uusia toimintoja voi testata varhaisessa vaiheessa. Kaikki aiemmin luodut Talent-esiintymät päivitetään **Tuotanto**-esiintymän tyyppiin. Jos haluat, että jokin aiemmin luoduista esiintymistä päivitetään **Eristys**-esiintymätyypiksi, ota yhteyttä [tukeen](https://docs.microsoft.com/dynamics365/unified-operations/talent/talent-support) ja tee muutospyyntö.

Lisätietoja muutosten julkaisemisesta on kohdassa [Talentin valmistelu](https://docs.microsoft.com/dynamics365/unified-operations/talent/provisioning-talent).

### <a name="restrict-leave-types-in-time-off-requests"></a>Poissaolopyyntöjen lomatyyppien rajoittaminen

Organisaatiot voivat tarjota työntekijöille useita erilaisia vapaatyyppejä. Työntekijät eivät kuitenkaan ehkä voi lähettää joidenkin lomatyyppien poissaolopyyntöjä. Kyseisiä lomatyyppejä hallitaan sen sijaan henkilöstöhallinnossa. Tässä versiossa voit määrittää, mitä lomatyyppejä varten työntekijät voivat lähettää pyyntöjä. 

### <a name="view-performance-information-for-direct-and-extended-reports-in-manager-self-service"></a>Suorien ja epäsuorien alaisten suoritustietojen näyttäminen esimiehen itsepalvelutoiminnossa

Uuden vaihtoehdon avulla esimiehet voit tarkastella sekä suorien että epäsuorien alaisten suoriutumista. Tällä hetkellä linjapäälliköt voivat määrittää ja päivittää suorituskykytavoitteita ja antaa uusia arvioita. Lisäksi suorat esimiehet ja heidän alaisensa voivat ylläpitää ja päivittää suoritustason kirjauskansioita. Tämä auttaa varmistamaan, että kehityskeskusteluprosessi toimii sujuvasti. Kun tämä muutos otetaan käyttöön, esimiehet voivat tarkastella ja ylläpitää epäsuorien alaisten suoritustasotietoja suorien alaisten tietojen lisäksi.
