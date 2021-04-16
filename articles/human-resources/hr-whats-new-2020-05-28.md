---
title: Dynamics 365 Human Resourcesin uudet tai muuttuneet ominaisuudet (28. toukokuuta 2020)
description: Tässä ohjeaiheessa käsitellään Microsoft Dynamics 365 Human Resourcesin 28. toukokuuta 2020 julkaistuja uusia tai muuttuneita ominaisuuksia.
author: andreabichsel
ms.date: 05/28/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2020-05-28
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 0e15891a2cb75851d195e08b87bbfc9efb78e66e
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2021
ms.locfileid: "5803390"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-may-28-2020"></a>Dynamics 365 Human Resourcesin uudet tai muuttuneet ominaisuudet (28. toukokuuta 2020)

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Tässä ohjeaiheessa käsitellään Dynamics 365 Human Resourcesin uusia tai muuttuneita ominaisuuksia. Muutokset koskevat koontiversion numeroa 8.1.3287. Joissakin otsikoissa suluissa olevat luvut viittaavat tukinumeroihin LCS-palveluissa.

## <a name="leaverequest-entity-doesnt-work-when-you-enable-multiple-types-per-leave-plan-447498"></a>LeaveRequest-yksikkö ei toimi, kun otat käyttöön useita tyyppejä per lomasuunnitelma (447498)

Tämän muutoksen avulla **LeaveEnrollmentV2Entity** on nyt käytettävissä korjaamaan virheen, joka ilmenee, kun otat käyttöön useita lomatyyppejä.

## <a name="batch-contention-reduction-feature-preview-446619"></a>Erän varausvirheen vähennystoiminto (esikatselu) (446619)

Kun otat tämän toiminnon käyttöön, voit odottaa eräkehystaulujen eston vähentämistä, kun valitset tehtäviä ja viimeistelytöitä.

## <a name="updateconflict-while-saving-worker-prevents-editing-a-record-in-people-427915"></a>UpdateConflict työntekijän tallennuksen aikana estää tietueen muokkaamisen henkilöillä (427915)

Tämä muutos korjaa virheen, kun uusi työntekijä lisätään, osoitetiedot päivitetään ja kieliasetus muutetaan. Tässä ainutlaatuisessa skenaariossa tietuetta ilmaisevaa virhettä ei voitu päivittää. 

## <a name="unable-to-add-an-attachment-to-an-approved-leave-request-to-resubmit-425407"></a>Liitettä ei voi lisätä hyväksyttyyn lomapyyntöön uudelleen lähettämistä varten (425407)

Tämä muutos sallii nyt liitteiden lisäämisen hyväksyttyihin lomapyyntöihin.

## <a name="user-can-enter-compensation-for-an-employee-in-a-different-legal-entity-form-409529"></a>Käyttäjä voi lisätä työntekijälle kompensaation toisessa yrityslomakkeessa (409529)

Tämä muutos poistaa käytöstä kompensaatioasetukset, jotka estävät väärän yrityksen kompensaatiotietojen tahattoman syötön.

## <a name="error-when-you-transfer-an-employee-and-the-worker-position-assignment-date-is-before-the-position-duration-429402"></a>Virhe siirrettäessä työntekijää ja työntekijän toimen määrityspäivämäärä on ennen toimen kestoa (429402)

Virhesanomat, kun työntekijä siirretään tässä skenaariossa, on päivitetty kuvaamaan paremmin ongelman korjaamiseen tarvittavia muutoksia.

## <a name="attachments-capabilities-in-employee-self-service-benefits-enrollment"></a>Liiteominaisuudet työntekijöiden itsepalvelussa hyödyttävät ilmoittautumista
 
Voit nyt lisätä liitteitä etuuksien rekisteröintiprosessin aikana jokaiselle suunnitelmalle, johon työntekijä on ilmoittautumassa. Tämän jälkeen voit tarkastella liitteitä **Työntekijän kirjatut edut** -lomakkeessa.

## <a name="in-preview"></a>Esiversiossa

## <a name="human-resources-application-in-teams"></a>Teamsin Human Resources -sovellus

Työntekijät voivat tarkastella ja pyytää lomaa työstä Microsoft Teamsissä. Ne voivat olla vuorovaikutuksessa botin kanssa luodakseen lomapyyntöjä. Lisätietoja on kohdassa [Human Resources -sovellus Teamsissa](https://go.microsoft.com/fwlink/?linkid=2127841). 

## <a name="leave-suspension"></a>Loman keskeytys

Voit keskeyttää työntekijän loman ja poissaolon henkilöstöhallinnossa. Loman keskeyttäminen pysäyttää valittujen lomatyyppien lomajaksotukset. Jos keskeytys tapahtuu jaksotuksen käsittelyn jälkeen, loman keskeyttäminen luo suhteutetun oikaisun työntekijän lomasaldoon. Lisätietoja on kohdassa [Loman keskeytys](hr-leave-and-absence-suspend-leave.md).

## <a name="update-user-experience-to-indicate-that-accrual-is-suspended-429550"></a>Päivitä käyttäjäkokemus osoittamaan, että jaksotus on keskeytetty (429550)

Käyttökokemus ilmaisee nyt, että jaksotus on keskeytetty suunnitelmaa varten.

## <a name="coming-soon"></a>Tulossa pian

## <a name="database-logging-in-preview-in-june"></a>Tietokannan kirjaaminen (kesäkuussa esikatselussa)

Tietokannan kirjaamistoiminnon avulla voit määrittää, mitä taulua ja kenttiä seurataan. Sen avulla voit myös määrittää tapahtumat, jotka käynnistävät muutosten seurannan. Kyselytoiminnot ovat käytettävissä, jotta nämä muutokset tulevat näkyviin ajan mittaan.

## <a name="buy-and-sell-leave-in-preview-june-1"></a>Loman vaihtaminen rahaksi ja lomapalkan vaihtaminen vapaaksi (esikatselussa 1. kesäkuuta)

Jotkut organisaatiot tarjoavat edun, jonka avulla työntekijät voivat vaihtaa lomaa rahaksi tai rahaa vapaaksi. Tätä prosessia hallitaan usein manuaalisesti. Tämän toiminnon avulla voit hallita HR-osaston käytäntöjä ja pyyntöjä entistä automatisoidummin. Se auttaa poistamaan virheitä ja virtaviivaistamaan lomanhallintaprosessia. Lisätietoja:

- [Käytäntöjen hallinta loman vaihtamisessa rahaksi ja lomapalkan vaihtamisessa vapaaksi](hr-leave-and-absence-manage-buy-and-sell-leave-policies.md)
- [Vaihda lomaa rahaksi tai lomapalkka vapaaksi](hr-employee-self-service-buy-sell-leave.md)

## <a name="data-management-framework-dmf-entities-for-benefits-management"></a>Tietojen hallintakehys (DMF) -yksiköt etuuksien hallintaa varten
 
Etujen hallintayksiköt julkaisevat. DMF-yksiköt sallivat tietojen tuomisen ja viemisen, jotta etuuksien hallinta voidaan määrittää helposti. Tietojen siirtämiseen on käytettävissä myös etujen hallintamalli. Malli vie tiedot ja tuo ne peräkkäisessä järjestyksessä tietoriippuvuuksien noudattamista varten.

## <a name="add-reason-code-to-accrual-suspensions-june-1"></a>Lisää syykoodi jaksotuskeskeytyksiin (Kesäkuun 1.)

Syykoodit on lisätty kertymän keskeyttämiseen.

## <a name="carry-forward-rules-june-1"></a>Siirtokirjauksen suorituksen säännöt (Kesäkuun 1.)

Voit määrittää siirrettäville saldoille siirtosäännön, johon on siirto-oikaisut siirretään. Jos työntekijä esimerkiksi siirtää vapaata kymmenen päivää eteenpäin, voit valita eri lomatyypin näiksi 10 päiväksi. Lisätietoja on kohdassa [Loma- ja poissaolotyyppien määrittäminen](hr-leave-and-absence-types.md).

## <a name="suspend-leave-accrual-for-specified-leave-types-june-1"></a>Valitun lomatyypin kertymän keskeyttäminen (Kesäkuun 1.)

Tässä julkaisussa HR voi luoda säännön, joka keskeyttää työntekijöiden loma- ja palkatonta lomaa varten syötettyjen lomapyyntöjen maksamisen. Palkaton vapaa voi olla tyyppi, mutta sen ei tarvitse olla. Voit keskeyttää minkä tahansa toiseen lomatyyppiin perustuvan loman.

## <a name="dmf-entity-available-for-accrual-suspensions-june-1"></a>DMF-yksikkö käytettävissä suoriteperusteisia keskeytyksiä varten (Kesäkuun 1.)

DMF-yksikkö on nyt käytettävissä suoriteperusteisia keskeytyksiä varten.

## <a name="see-also"></a>Lisätietoja

[Human Resourcesin uudet ja muuttuneet ominaisuudet](hr-admin-whats-new.md)</br>
[Yhteenveto Dynamics 365 Human Resourcesin vuoden 2019 julkaisuaallosta 2](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[Päivitysprosessi](hr-admin-setup-update-process.md)</br>
[Hallitse ominaisuuksia](hr-admin-manage-features.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]