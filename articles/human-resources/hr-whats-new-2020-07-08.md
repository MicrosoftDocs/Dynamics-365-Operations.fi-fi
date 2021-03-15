---
title: Dynamics 365 Human Resourcesin uudet ja muuttuneet ominaisuudet (8. heinäkuuta 2020)
description: Tässä ohjeaiheessa käsitellään Microsoft Dynamics 365 Human Resourcesin 8. heinäkuuta 2020 julkaistuja uusia tai muuttuneita ominaisuuksia.
author: andreabichsel
manager: tfehr
ms.date: 07/08/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 14dfd925009cb2a9d40044e27f28521ff4d331b7
ms.sourcegitcommit: f8bac7ca2803913fd236adbc3806259a17a110f4
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/06/2021
ms.locfileid: "5130394"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-july-8-2020"></a>Dynamics 365 Human Resourcesin uudet ja muuttuneet ominaisuudet (8. heinäkuuta 2020)

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Tässä ohjeaiheessa käsitellään Dynamics 365 Human Resourcesin uusia tai muuttuneita ominaisuuksia. Muutokset koskevat koontiversion numeroa 8.1.3382. Joissakin otsikoissa suluissa olevat luvut viittaavat tukinumeroihin LCS-palveluissa.

## <a name="database-logging"></a>Tietokannan lokiinkirjaus

Tietokantakirjauksen avulla voit määrittää, mitä taulukoita ja kenttiä seurataan. Sen avulla voit myös määrittää tapahtumat, jotka käynnistävät muutosten seurannan. Tietokantakirjauksen ominaisuuksien avulla nähdään nämä muutokset ajan kuluessa. Lisätietoja on kohdassa [Tietokantakirjauksen määrittäminen ja hallinta](hr-admin-database-logging.md).

## <a name="configure-the-name-of-employee-self-service"></a>Työntekijän itsepalvelun nimen määrittäminen

**Työntekijän itsepalvelu** -työntilan nimen voi nyt vaihtaa **Henkilöstöhallinnon parametrit** -kohdassa muotoon **Itsepalvelu**. Lisätietoja on kohdassa [Työntekijän itsepalvelutyötilan nimen muuttaminen](hr-employee-self-service-workspace-name.md).

## <a name="benefits-management-open-enrollment-access-outside-of-period"></a>Etuuksien hallinnan avoimen ilmoittautumisen käyttäminen kauden ulkopuolella

Tämä versio korjaa virheen, jonka vuoksi työntekijät pystyivät käyttämään etuuksien avointa ilmoittautumista ilmoittautumiskauden ulkopuolella tai ilman elämäntapahtumaa. Tämän vuoksi avoimen ilmoittautumisen esittelyä varten työntekijän itsepalvelussa on muokattava avoimen ilmoittautumisen päivämäärät kuluvalle päivälle (tai sitä aikaisemmaksi), jotta toimintoa voi käyttää. Tätä asetusta voi muuttaa valitsemalla **Etujen hallinta > Sääntö- ja asetuskaudet**.

## <a name="email-employee-enrollment-confirmation"></a>Työntekijän ilmoittautumisen vahvistussähköposti

Voit nyt lähettää työntekijöille sähköpostiviestejä, kun he ovat tehneet etuusvalinnat. Voit lähettää joko oletusviestin tai käyttää organisaation sähköpostimallia. Nämä asetukset ovat kohdassa **Henkilöstöhallinnan parametrit > Etujen hallinta**.

## <a name="canceled-leave-still-appears-in-upcoming-time-off-on-people-workspace-441358"></a>Peruutettu loma näkyy edelleen tulevana poissaolona Henkilöt-työtilassa (441358)

Peruutettu loma ei enää näy tulevana poissaolona **Henkilöt**-työtilan poissaolokorteissa.

## <a name="unable-to-use-the-department-entity-property-in-the-positionv2-entity-456486"></a>Osastoentiteetin ominaisuutta ei voi käyttää PositionV2-entiteetissä (456486)

Voit nyt lisätä osaston ilman, että näin luotaisiin suhteen kaksoiskappale.

## <a name="payrollworkerenrolledbenefitdetailentity-should-only-use-calculated-field-for-retirement-plans-459779"></a>PayrollWorkerEnrolledBenefitDetailEntity-entiteetin on käytettävä vain laskettua kenttää eläkepaketeissa (459779)

Kun **PayrollWorkerEnrolledBenefitDetailEntity**-entiteetti viedään, vienti määrittää, käyttääkö se laskettua kenttää palkkataulukon perusteella vai käyttääkö se **ContributionAmountCur**-kenttää varmuuskopiotaulussa. Tietoentiteetin käyttämä logiikka käyttää palkkataulua tilanteissa, joissa sovellus ei sitä yleensä tee. Tämän logiikan vuoksi entiteettiviennit palauttavat sarakkeelle nolla-arvon, koska laskennan palkkataulukkoa ei ole eikä tuote anna asiakkaalle mahdollisuutta sen määrittämiseen.
 
## <a name="confusing-translations-in-czech-language-in-personnel-management-and-employee-self-service-400276"></a>Epäselvät tšekinkieliset käännökset henkilöstöhallinnassa ja työntekijän itsepalvelussa (400276)

Tämä versio korjaa käännökset sanoille **yrityksen hakemisto**, **seuraava rekisteröity kurssi**, **työ** ja **paikka**.
 
## <a name="the-workcalendaremployment-table-doesnt-have-the-created-and-modified-system-fields-enabled-460171"></a>WorkCalendarEmployment-taulu ei ole luonut ja muokannut käyttöönotettuja järjestelmäkenttiä (460171)

Luodut ja muokatut järjestelmäkentät on nyt otettu käyttöön Human Resourcen **WorkCalendarEmployment**-taulussa.
 
## <a name="null-reference-exception-for-hire-and-add-details-for-future-employee-455475"></a>Työhönoton tyhjäarvoviittaus tulevan työntekijän Työhönotto ja tietojen lisääminen -toiminnossa (455475)

Tämä versio korjaa virheen (tyhjäarvoviittaus) sujuvoitetussa työntekijämerkinnässä, kun työntekijän työhönottoon käytetään **Työhönotto ja tietojen lisääminen** -toimintoa.

## <a name="changes-made-in-the-dataverse-worker-entity-dont-reflect-in-human-resources-455652"></a>Dataversen työntekijäentiteettiin tehdyt muutokset eivät siirry Human Resourcesiin (455652)

Seuraaviin Dataversen **Työntekijä**-entiteettiin tehdyt muutokset näkyvät nyt Human Resourcesissa:

- **Työskentelee kotoa käsin**
- **Ikälisäpäivä**
- **Vuosipäivän päivämäärä**
- **Alkuperäinen työsuhteen alkamispäivämäärä**

## <a name="correct-compensation-level-doesnt-default-based-on-the-job-assigned-to-the-position-394136"></a>Oikea kompensaatiotaso ei palaa oletusarvoon toimeen määritetyn työn perusteella (394136)

Tämän muutoksen myötä kompensaatiotaso palaa oikein oletusarvoon **Toimen tiedot** -kohdan **Voimassaolotietueet**-tietueiden ja **Kompensaatiopaketin määritys** -kohdan **alkamispäivän** perusteella.

## <a name="in-preview"></a>Esiversiossa

## <a name="mandatory-fields"></a>Pakolliset kentät 

Nyt voit tehdä kentistä pakollisia käyttämällä henkilöstöhallinnon mukauttamisominaisuuksia. Tämä toiminto edellyttää **tallennettuja näkymiä**.

## <a name="human-resources-application-in-teams"></a>Teamsin Human Resources -sovellus

Työntekijät voivat tarkastella ja pyytää lomaa työstä Microsoft Teamsissä. Ne voivat olla vuorovaikutuksessa botin kanssa luodakseen lomapyyntöjä. Lisätietoja on kohdassa [Human Resources -sovellus Teamsissa](https://go.microsoft.com/fwlink/?linkid=2127841). 

## <a name="data-management-framework-dmf-entities-for-benefits-management"></a>Tietojen hallintakehys (DMF) -yksiköt etuuksien hallintaa varten
 
Etujen hallintayksiköt julkaisevat. DMF-yksikköjen avulla voi tuoda ja viedä tietoja, mikä helpottaa etuuksien hallinnan määrittämistä. Tietojen siirtämiseen on käytettävissä etuuksien hallintamalli. Malli vie tiedot ja tuo ne peräkkäin tietojen riippuvaisuuksia noudattaen.

## <a name="buy-and-sell-leave"></a>Vaihda lomaa rahaksi tai lomapalkka vapaaksi 

Jotkut organisaatiot tarjoavat edun, jonka avulla työntekijät voivat vaihtaa lomaa rahaksi tai rahaa vapaaksi. Tätä prosessia hallitaan usein manuaalisesti. Tämä toiminto automatisoi henkilöstöosaston käytäntöjen ja pyyntöjen hallinnan. Se sujuvoittaa lomien hallintaprosessia ja auttaa poistamaan virheitä. Lisätietoja:

- [Käytäntöjen hallinta loman vaihtamisessa rahaksi ja lomapalkan vaihtamisessa vapaaksi](hr-leave-and-absence-manage-buy-and-sell-leave-policies.md)
- [Vaihda lomaa rahaksi tai lomapalkka vapaaksi](hr-employee-self-service-buy-sell-leave.md)

## <a name="leave-accrual-for-a-single-company-or-single-plan"></a>Yhden yrityksen tai yhden suunnitelman mukainen loman jaksotus

Asiakkaat voi käsitellä yhden yrityksen tai yhden suunnitelman loma- ja poissaolosuunnitelman jaksotukset. Tämä selkeyttää jaksotusprosessia, kun asiakkailla on erilaisia lomavuosi- tai loman jaksotuskäytäntöjä. Lisätietoja on kohdassa [Loman jaksottaminen yrityksen tai lomasuunnitelman mukaan](hr-leave-and-absence-accrue.md).

## <a name="add-attachments-to-time-off-requests"></a>Liitteiden lisääminen poissaolopyyntöihin

Mahdollisuus lisätä liitteitä hyväksyttyihin lomapyyntöihin on tärkeää nykyisessä COVID-19-tilanteessa. Työntekijät voivat nyt lisätä nämä liitteet. He saavat lisää merkityksellisiä tietoja lomapyyntöihin tehtävistä päivityksistä. Lisätietoja on kohdassa [Liitteen lisääminen aiemmin luotuun pyyntöön](hr-employee-self-service-request-time-off.md#add-an-attachment-to-an-existing-request).

## <a name="add-reason-code-to-accrual-suspensions"></a>Syykoodin lisääminen jaksotuskeskeytyksiin 

Syykoodit on lisätty kertymän keskeyttämiseen.

## <a name="carry-forward-rules"></a>Siirtokirjauksen suorituksen säännöt 

Voit määrittää siirrettäville saldoille siirtosäännön, johon on siirto-oikaisut siirretään. Jos työntekijä esimerkiksi siirtää vapaata kymmenen päivää eteenpäin, voit valita eri lomatyypin näiksi 10 päiväksi. Lisätietoja on kohdassa [Loma- ja poissaolotyyppien määrittäminen](hr-leave-and-absence-types.md).

## <a name="suspend-leave-accrual-for-specified-leave-types"></a>Valittujen lomatyyppien jaksotuksen keskeyttäminen

Voit luoda säännön, joka keskeyttää työntekijöiden lomaa ja palkatonta lomaa varten annettujen lomapyyntöjen maksamisen. Palkaton vapaa voi olla tyyppi, mutta sen ei tarvitse olla. Voit keskeyttää minkä tahansa toiseen lomatyyppiin perustuvan loman.

## <a name="dmf-entity-available-for-accrual-suspensions"></a>DMF-yksikkö käytettävissä suoriteperusteisia keskeytyksiä varten 

DMF-yksikkö on nyt käytettävissä suoriteperusteisia keskeytyksiä varten.

## <a name="coming-soon"></a>Tulossa pian

## <a name="checklist-entities-included-in-dataverse"></a>Dataverseen sisältyvät tarkistusluettelokohdat

Käyttöönotto-, käytöstäpoisto-, siirto- ja liiketoimintaprosessien tarkistusluettelokohdat ovat pian saatavilla Dataversessä.

## <a name="see-also"></a>Lisätietoja

[Human Resourcesin uudet ja muuttuneet ominaisuudet](hr-admin-whats-new.md)</br>
[Yhteenveto Dynamics 365 Human Resourcesin vuoden 2019 julkaisuaallosta 2](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[Päivitysprosessi](hr-admin-setup-update-process.md)</br>
[Hallitse ominaisuuksia](hr-admin-manage-features.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]