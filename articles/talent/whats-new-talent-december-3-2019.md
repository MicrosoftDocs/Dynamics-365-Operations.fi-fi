---
title: Dynamics 365 Talent:n uudet tai muuttuneet ominaisuudet (3. joulukuuta 2019)
description: Tässä artikkelissa käsitellään Microsoft Dynamics 365 Talentin uusia tai muuttuneita toimintoja.
author: Darinkramer
manager: AnnBe
ms.date: 12/03/2019
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
ms.search.validFrom: 2019-12-03
ms.dyn365.ops.version: Talent
ms.openlocfilehash: bf1ad4ca2e0ab18aaa35a7410d80a54e7a2160ce
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/17/2020
ms.locfileid: "4528690"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-december-3-2019"></a>Dynamics 365 Talent:n uudet tai muuttuneet ominaisuudet (3. joulukuuta 2019)

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Tässä artikkelissa käsitellään Dynamics 365 Talentin uusia tai muuttuneita toimintoja.

## <a name="changes-in-attract"></a>Attractin muutokset

Tässä julkaisussa on vähäisiä Dynamics 365 Talent: Attractin ohjelmakorjauksia.

## <a name="changes-in-onboard"></a>Onboardin muutokset

Tässä julkaisussa on vähäisiä Dynamics 365 Talent: Onboard:n ohjelmakorjauksia.

## <a name="changes-in-core-hr"></a>Core HR:n muutokset

Tässä osassa kuvatut muutokset koskevat koontiversiota 8.1.2646. Joissakin otsikoissa suluissa olevat luvut viittaavat tukinumeroihin Microsoft Dynamics Lifecycle Services (LCS) -palveluissa.

### <a name="feature-management-workspace"></a>Ominaisuushallinnan työtila

**Toimintojen hallinta** -työtilassa on luettelo kussakin julkaisussa toimitetuista toiminnoista. Uudet asetukset ovat oletusarvoisesti poissa käytöstä. Työtilan avulla voit ottaa ne käyttöön ja tarkastella niiden dokumentaatiota. Lisätietoja Toimintojen hallinnasta on kohdassa [Toimintojen hallinnan yleiskuvaus](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview).

Kaikki uudet toiminnot pysyvät esiversiossa ainakin 30 päivää ja yleensä 30–60 päivää. Tärkeimmät toiminnot ovat yleensä saatavana kunkin vuoden lokakuussa ja huhtikuussa esiversiojakson jälkeen. Voit ottaa uudet ominaisuudet käyttöön heti, kun näet ne **Toimintojen hallinta** -työtilassa. Jotkin toiminnot on ehkä otettu käyttöön oletusarvoisesti.
 
Joskus keskeinen toiminto on otettu käyttöön oletusarvoisesti eikä sitä voi poistaa käytöstä (esimerkiksi **Toimintojen hallinta** -työtilassa).
 
Kun toiminto on yleisesti saatavana, se voidaan ottaa käyttöön tai poistaa käytöstä tuotantoympäristöissä. **Toimintojen hallinta** -työtila ilmaisee, milloin esiversiotoiminto tulee pakolliseksi. Tämä päivämäärä on yleensä 1. lokakuuta tai 1. huhtikuuta eli ne vastaavat puolivuotisia julkaisusuunnitelmia. Pakollisia toimintoja ei voi poistaa käytöstä. Toiminnon voi ottaa käyttöön ja poistaa käytöstä kaikissa ympäristöissä siihen saakka, että muuttuu pakolliseksi.

### <a name="add-automatic-scheduling-of-batch-job-history-cleanup-332528"></a>Lisää erätyöhistorian uudelleenjärjestämisen automaattinen ajoitus (332528)

Tämän muutoksen avulla **erätyöhistoria** suoritetaan joka yö ja se poistaa yli 30 päivää vanhat erätyön historiakohteet.

### <a name="talent-doesnt-respond-in-worker-actions-when-identification-number-length-doesnt-match-the-identification-type-390971"></a>Talent ei vastaa työntekijätoiminnoissa, kun tunnusnumeron pituus ei vastaa tunnustyyppiä (390971)

Tämä julkaisu korjaa ongelman, joka ilmenee, kun tunnusnumeron pituus ei vastaa tunnistustyypin määritystä. 

### <a name="fixed-compensation-doesnt-update-level-with-changes-to-position-details--348085"></a>Kiinteä kompensaatio ei päivitä tasoa sijaintitietojen muutoksin (348085)

Tämän viikon versiossa **Kompensaation alkamispäivämäärä** määrittää työn, joka liittyy toimeen kyseisenä ajankohtana luotaessa uutta kiinteää kompensaatiotietuetta työntekijälle.

### <a name="workers-employees-and-contractors-lists-show-worker-type-as-both-when-they-should-only-be-worker-or-contractor-384473"></a>Työntekijä ja alihankkija -luettelot osoittavat työntekijätyypin molemmiksi, kun heidän tulisi olla vain työntekijöitä tai alihankkijoita (384473)

Tämä muutos kuvastaa tarkasti syötetyn työntekijän tyyppiä (alihankkija tai työntekijä).

### <a name="email-notifications-for-new-hire-actions-dont-contain-name-information-due-to-security-policies-383402"></a>Uusien työhönottotoimintojen sähköposti-ilmoitukset eivät sisällä suojauskäytäntöjen vuoksi nimitietoja (383402)

Tämä muutos korjaa työnkulun paikkamerkkien etu- tai sukunimikentissä näytettävät tiedot, kun kehittynyt suojaus on käytössä.

### <a name="system-allows-two-full-day-leave-requests-for-the-same-day-379284"></a>Järjestelmä sallii kaksi koko päivän vapaan pyyntöä samana päivänä (379284)

Tällä muutoksella et voi antaa samana päivän kahta lomapyyntöä. 

### <a name="address-changes-list-should-be-sorted-by-effective-date-352798"></a>Osoitteiden muutosluettelo tulee lajitella voimaantulopäivämäärän mukaan (352798)

Tämän muutoksen myötä osoitteenmuutosluettelo lajitellaan nyt **voimaantulopäivämäärän** mukaan.

### <a name="leave-requests-should-allow-deletes-from-common-data-service-to-talent-376999"></a>Lomapyyntöjen pitäisi sallia poistot Common Data Servicestä Talentiin (376999)

Tämän muutoksen avulla luonnokset ja peruutetut lomapyynnöt voidaan poistaa Common Data Servicestä ja poistaa sitten Talentista.

### <a name="delete-earning-codes-is-allowed-when-the-same-earning-code-is-assigned-to-an-employee-371792"></a>Poista ansaintakoodit sallitaan, kun sama ansaintakoodi on määritetty työntekijälle (371792)

Tässä versiossa sinun on ensin poistettava ansaintakoodi työntekijästä ennen kuin poistat ansaintakoodin järjestelmästä.

### <a name="leave-and-absence-workflow-with-two-approval-stages-fails-to-complete--391116"></a>Vapaan ja poissaolon työnkulku, jossa on kaksi hyväksymisvaihetta, epäonnistuu (391116)

Tämän muutoksen myötä loma- ja poissaolon työnkulku jatkuu kaikissa vaiheissa, kun pyynnölle on määritetty useampi kuin yksi hyväksymisvaihe.

### <a name="issue-date-doesnt-sync-to-common-data-service-when-updated-or-entered-in-talent-397361"></a>Myöntämispäivämäärää ei synkronoida Common Data Serviceen, kun päivitetään tai syötetään Talent-kohteeseen (397361)

Tämä muutos korjaa ongelman, jossa **henkilön tunnistus**-tietueiden seuranta-ajankohtaa ei synkronoitu Common Data Serviceen Talentista.

### <a name="hierarchy-circular-reference-error-issued-when-assigning-a-manager-to-a-position-386659"></a>Hierarkian kehäviittausvirhe esimiestä toimeen määritettäessä (386659)

Tämä muutos korjaa yksilöllisen skenaarion, jossa kehäviittausvirhe tulee näkyviin, kun määrität uuden esimiehen toimeen.

### <a name="common-data-service-entities-that-now-support-custom-fields"></a>Mukautettuja kenttiä nyt tukevat Common Data Service -yksikköjä

Seuraavat mukautetut Common Data Service -yksiköt tukevat mukautettuja kenttiä:

| Nimi | Kokonaisuus |
| --- | --- |
| Pankkitilisuoritukset | cdm_bankaccountdisbursement |
| Edun laskentatiheys | cdm_benefitcalculationfrequency |
| Edun laskennan toistuvuuden maksukausi | cdm_benefitcalculationfrequencypayperiod |
| Edun laskentahinta | cdm_benefitcalculationrate |
| Edun laskentahinnan tiedot | cdm_benefitcalculationratedetail |
| Etuusvaihtoehto | cdm_benefitoption |
| Etusuunnitelma | cdm_benefitplan (Ei käytössä mukautetulla kentän tuella) |
| Edun tyyppi | cdm_benefittype |
| Liiketoimintaprosessin kalenteri | cdm_businessprocesscalendar |
| Liiketoimintaprosessin ryhmämääritys | cdm_businessprocessgroupassignment |
| Liiketoimintaprosessikirjaston tehtäväryhmä | cdm_businessprocesslibrarytaskgroup |
| Liiketoimintaprosessin vaihe | cdm_businessprocessstage |
| Tarkistusluettelomallin otsikko | cdm_businessprocesstemplateheader |
| Tarkistusluettelomallin tehtävä | cdm_businessprocesstemplatetask |
| Yritys  | cdm_company |
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
| Osasto | cdm_department |
| Työsuhde | cdm_employment |
| Etninen tausta | HcmEthnicOrigin |
| Kiinteä kompensaatiotapahtuma | cdm_fixedcompensationevent |
| Tehtävä | cdm_job |
| Työtehtävä | cdm_jobfunction |
| Tehtävänimike | cdm_jobposition |
| Työtyyppi | cdm_jobtype |
| Kieli | cdm_language |
| Loman pankkitapahtuma | cdm_leavebanktransaction |
| Lomailmoittautuminen | cdm_leaveenrollment |
| Lomasuunnitelma | cdm_leaveplan |
| Lomapyyntö | cdm_leaverequest |
| Lomapyynnön tiedot | cdm_leaverequestdetail |
| Lomatyyppi | cdm_leavetype |
| Lomatyypin syykoodi | cdm_leavetypereasoncode |
| Maksujakso | cdm_paycycle |
| Maksukausi | cdm_payperiod |
| Palkanlaskennan ansiokoodi | cdm_payrollearningcode |
| Henkilötunnuksen myöntänyt virasto | cdm_personidentificationissuingagency |
| Toimityyppi | cdm_positiontype |
| Toimen työntekijän toimeksianto | cdm_positionworkerassignmentmap |
| Syykoodi | cdm_reasoncode |
| Osaamisaluetyyppi | cdm_skilltype |
| Verotusalue | cdm_taxregion |
| Hyvityssääntö | cdm_vestingrule |
| Sotaveteraanitila | cdm_veteranstatus |
| Työkalenteri | cdm_workcalendar |
| Työkalenteripäivämäärä | cdm_workcalendarday |
| Työkalenterin lomapäivä |cdm_workcalendarholiday |
| Työkalenterin lomapäivärivi | cdm_workcalendarholidayline |
| Työkalenterin aikaväli | cdm_workcalendartimeinterval (Ei käytössä mukautetulla kentän tuella) |
| Työntekijä | cdm_worker |
| Työntekijän osoite | cdm_workeraddress |
| Työntekijän pankkitili | cdm_workerbankaccount |
| Työntekijän kiinteä kompensaatio | cdm_workerfixedcompensation |
| Työntekijän henkilötiedot | cdm_workerpersonaldetail |
| Työntekijän tunnusnumero | cdm_workerpersonidentificationnumber |
| Työntekijän tunnustyyppi | cdm_workerpersonidentificationtype |

## <a name="in-preview"></a>Esiversiossa

Esiversiotoiminnot ovat käytettävissä vain **eritys** ympäristöissä.

### <a name="print-performance-reviews"></a>Kehityskeskustelujen tulostaminen

Katso lisätietoja Dynamics 365: vuoden 2019 julkaisuaallon 2 suunnitelman kohdasta [Kehityskeskustelujen tulostaminen](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-talent/print-performance-reviews).


[!INCLUDE[footer-include](../includes/footer-banner.md)]