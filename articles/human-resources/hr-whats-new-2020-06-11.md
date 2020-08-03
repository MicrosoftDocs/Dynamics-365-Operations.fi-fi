---
title: Dynamics 365 Human Resourcesin uudet ja muuttuneet ominaisuudet (11. kesäkuuta 2020)
description: Tässä ohjeaiheessa käsitellään Microsoft Dynamics 365 Human Resourcesin uusia tai muuttuneita ominaisuuksia.
author: Darinkramer
manager: AnnBe
ms.date: 6/16/2020
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
ms.author: dkrame
ms.search.validFrom: 2020-06-11
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: cba6e48899ec39fc4de6656f8151a42b8aa43261
ms.sourcegitcommit: bd9ff0d28718d535356ffbe1cffaaf60310dd430
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 07/13/2020
ms.locfileid: "3555192"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-june-11-2020"></a>Dynamics 365 Human Resourcesin uudet ja muuttuneet ominaisuudet (11. kesäkuuta 2020)

Tässä artikkelissa käsitellään Dynamics 365 Human Resourcesin uusia tai muuttuneita toimintoja. Muutokset koskevat koontiversion numeroa 8.1.3316. Joissakin otsikoissa suluissa olevat luvut viittaavat tukinumeroihin LCS-palveluissa.

## <a name="streamlined-employee-form-sometimes-causes-child-form-close-x-buttons-to-stop-working-442369"></a>Sujuvoitettu työntekijälomake aiheuttaa joskus alilomakkeen sulkemispainikkeiden (X) toiminnan päättymisen (442369)

Kun uusi **Työntekijä**-lomake otettiin käyttöön, sulkemispainike (**X**) ei aina toimi alilomakkeissa. Tämä ongelma oli ajoittainen. Lomakkeen voisi sulkea sen jälkeen, kun olet poistunut ja palannut siihen takaisin. Voisit esimerkiksi valita valikkovaihtoehdon vasemmalla, siirtyä sitten **Työntekijä**-lomakkeeseen ja sulkea sen. Tämän viikon julkaisu korjaa tämän ongelman. 

## <a name="the-worker-personal-contact-person-entity-doesnt-export-personal-contacts-with-a-parent-relationship-type"></a>Työntekijän henkilökohtaisen yhteyshenkilöentiteetti ei vie henkilökohtaisia yhteyshenkilöitä, joiden tyyppinä on ylätason suhde

Tässä versiossa **Työntekijän henkilökohtainen yhteyshenkilö** -entiteetti vie kaikki suhdetyypit.

## <a name="the-hcmpositionworkerassignmentv2entity-should-be-part-of-the-ceridian-payroll-integration-package-by-default-448506"></a>HcmPositionWorkerAssignmentV2Entity-entiteetin pitäisi oletusarvoisesti olla Ceridian-palkanlaskennan integraatiopaketin osa (448506)

Tämän muutoksen myötä **HcmPositionWorkerAssignmentV2Entity** sisältyy Ceridian-palkanlaskennan integraatiopakettiin.

## <a name="in-preview"></a>Esiversiossa

## <a name="database-logging"></a>Tietokannan lokiinkirjaus

Tietokantakirjaustoiminnon avulla voit määrittää, mitä taulukoita ja kenttiä seurataan. Sen avulla voit myös määrittää tapahtumat, jotka käynnistävät muutosten seurannan. Tietokantakirjauksen ominaisuuksien avulla nähdään nämä muutokset ajan kuluessa. Lisätietoja on kohdassa [Tietokantakirjauksen määrittäminen ja hallinta](hr-admin-database-logging.md).

## <a name="human-resources-application-in-teams"></a>Teamsin Human Resources -sovellus

Työntekijät voivat tarkastella ja pyytää lomaa työstä Microsoft Teamsissä. Ne voivat olla vuorovaikutuksessa botin kanssa luodakseen lomapyyntöjä. Lisätietoja on kohdassa [Human Resources -sovellus Teamsissa](https://go.microsoft.com/fwlink/?linkid=2127841). 

## <a name="data-management-framework-dmf-entities-for-benefits-management"></a>Tietojen hallintakehys (DMF) -yksiköt etuuksien hallintaa varten
 
Etujen hallintayksiköt julkaisevat. DMF-yksikköjen avulla voi tuoda ja viedä tietoja, mikä helpottaa etuuksien hallinnan määrittämistä. Tietojen siirtämiseen on käytettävissä etuuksien hallintamalli. Malli vie tiedot ja tuo ne peräkkäin tietojen riippuvaisuuksia noudattaen.

## <a name="buy-and-sell-leave"></a>Vaihda lomaa rahaksi tai lomapalkka vapaaksi 

Jotkut organisaatiot tarjoavat edun, jonka avulla työntekijät voivat vaihtaa lomaa rahaksi tai rahaa vapaaksi. Tätä prosessia hallitaan usein manuaalisesti. Tämä toiminto automatisoi henkilöstöosaston käytäntöjen ja pyyntöjen hallinnan. Se sujuvoittaa lomien hallintaprosessia ja auttaa poistamaan virheitä. Lisätietoja:

- [Käytäntöjen hallinta loman vaihtamisessa rahaksi ja lomapalkan vaihtamisessa vapaaksi](hr-leave-and-absence-manage-buy-and-sell-leave-policies.md)
- [Vaihda lomaa rahaksi tai lomapalkka vapaaksi](hr-employee-self-service-buy-sell-leave.md)

## <a name="leave-accrual-for-a-single-company-or-single-plan"></a>Yhden yrityksen tai yhden suunnitelman mukainen loman jaksotus

Asiakkaat voi käsitellä yhden yrityksen tai yhden suunnitelman loma- ja poissaolosuunnitelman jaksotukset. Tämä selkeyttää jaksotusprosessia, kun asiakkailla on erilaisia lomavuosi- tai loman jaksotuskäytäntöjä. Lisätietoja on kohdassa [Loman jaksottaminen yrityksen tai lomasuunnitelman mukaan](hr-leave-and-absence-accrue.md#accrue-leave-per-company-or-per-leave-plan).

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

## <a name="new-platform-capabilities"></a>Ympäristön uudet ominaisuudet 

Kentistä voi tehdä pakollisia mukautuksia käyttämällä. Tämä toiminto edellyttää **tallennettujen näkymien** ottamista käyttöön.

## <a name="configure-the-name-of-employee-self-service"></a>Työntekijän itsepalvelun nimen määrittäminen

Human Resourcesin parametreissa on uusi vaihtoehto, jolla voi päivittää Työntekijän itsepalvelu -työtilan nimen itsepalveluksi. 

## <a name="see-also"></a>Lisätietoja

[Human Resourcesin uudet ja muuttuneet ominaisuudet](hr-admin-whats-new.md)</br>
[Yhteenveto Dynamics 365 Human Resourcesin vuoden 2019 julkaisuaallosta 2](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[Päivitysprosessi](hr-admin-setup-update-process.md)</br>
[Hallitse ominaisuuksia](hr-admin-manage-features.md)