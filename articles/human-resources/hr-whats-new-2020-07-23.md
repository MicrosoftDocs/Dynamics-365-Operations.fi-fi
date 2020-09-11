---
title: Dynamics 365 Human Resourcesin uudet ja muuttuneet ominaisuudet (23. heinäkuuta 2020)
description: Tässä ohjeaiheessa käsitellään Microsoft Dynamics 365 Human Resourcesin 23. heinäkuuta 2020 julkaistuja uusia tai muuttuneita ominaisuuksia.
author: Darinkramer
manager: AnnBe
ms.date: 07/23/2020
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
ms.search.validFrom: 2020-07-23
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 30662ccf7e37f7f1e131e3b18b5a770c53fea0d1
ms.sourcegitcommit: 2bcacef1e010c312f019dbf9740ce87d627848a7
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/20/2020
ms.locfileid: "3711865"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-july-23-2020"></a>Dynamics 365 Human Resourcesin uudet ja muuttuneet ominaisuudet (23. heinäkuuta 2020)

Tässä ohjeaiheessa käsitellään Dynamics 365 Human Resourcesin uusia tai muuttuneita ominaisuuksia. Muutokset koskevat koontiversion numeroa 8.1.3416. Joissakin otsikoissa suluissa olevat luvut viittaavat tukinumeroihin LCS-palveluissa.

## <a name="deleting-financial-dimensions-on-a-position-doesnt-work-as-expected-445476"></a>Talousdimensioiden poistaminen sijainnista ei toimi odotetulla tavalla (445476)

Dimensioiden poistaminen sijainnista poistaa nyt samat sijainnit myös Common Data Service -sovelluksesta.

## <a name="positions-not-in-hierarchy-show-inactive-positions-397257"></a>Sijainnit, jotka eivät ole hierarkiassa, näyttävät passiiviset sijainnit (397257)

Sijainnit, jotka ovat passiivisia (joiden kesto on päättynyt), eivät enää näy sijaintien hierarkiassa **Sijainnit eivät ole hierarkiassa** -merkinnän kanssa. 

## <a name="validation-occurring-between-leaveenrollmententity-and-hcmworkerentity-on-data-management-framework-dmf-import-causes-slow-data-loads-442324"></a>Vahvistus, joka tapahtuu LeaveEnrollmentEntity- ja HcmWorkerEntity-entiteettien välillä Data Management Frameworkin (DMF) tuonnissa aiheuttaa tietojen latauksen hidastumista (442324)

Tämän version muutokset lisäävät **LeaveEnrollmentEntity**-entiteetin suorituskykyä.

## <a name="unable-to-personalize-in-organization-administration-447490"></a>Organisaation hallinnan mukauttaminen ei onnistu (447490)

Tämän muutoksen avulla voit nyt mukauttaa linkkejä **Organisaation hallinnassa**.

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

## <a name="checklist-entities-included-in-common-data-service"></a>Common Data Serviceen sisältyvät tarkistusluettelokohdat

Käyttöönotto-, käytöstäpoisto-, siirto- ja liiketoimintaprosessien tarkistusluettelokohdat ovat pian saatavilla Common Data Servicessä.

## <a name="platform-changes"></a>Alustan muutokset

Platform Update 10.0.12 (36)

## <a name="see-also"></a>Lisätietoja

[Human Resourcesin uudet ja muuttuneet ominaisuudet](hr-admin-whats-new.md)</br>
[Yhteenveto Dynamics 365 Human Resourcesin vuoden 2019 julkaisuaallosta 2](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[Päivitysprosessi](hr-admin-setup-update-process.md)</br>
[Hallitse ominaisuuksia](hr-admin-manage-features.md)
