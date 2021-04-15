---
title: Dynamics 365 Human Resourcesin uudet ja muuttuneet ominaisuudet (20. huhtikuuta 2020)
description: Tässä ohjeaiheessa käsitellään Microsoft Dynamics 365 Human Resourcesin 20. elokuuta 2020 julkaistuja uusia tai muuttuneita ominaisuuksia.
author: andreabichsel
ms.date: 08/20/2020
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
ms.search.validFrom: 2020-08-20
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 69304cbffafa4c20dbbbb31d5c19920f669761b9
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2021
ms.locfileid: "5800162"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-august-20-2020"></a>Dynamics 365 Human Resourcesin uudet ja muuttuneet ominaisuudet (20. huhtikuuta 2020)

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Tässä ohjeaiheessa käsitellään Dynamics 365 Human Resourcesin uusia tai muuttuneita ominaisuuksia. Muutokset koskevat koontiversion numeroa 8.1.3478. Joissakin otsikoissa suluissa olevat luvut viittaavat Lifecycle Services (LCS) -palveluiden tukinumeroihin.

## <a name="show-upcoming-and-pending-leave-of-absence-information-to-cards-in-people-workspace"></a>Tulevien ja odottavien poissaolotietojen näyttäminen Ihmiset-työtilan korteissa

Odottavat ja tulevat poissaolopyyntöjen vaihtoehdot ovat käytettävissä **Ihmiset**-työtilan loma- ja poissaolokorteissa.

## <a name="private-field-isnt-yes-by-default-for-employee-role-in-employee-self-service-477106"></a>Yksityinen-kentän asetus ei ole oletusarvoisesti Kyllä työntekijän itsepalvelun työntekijäroolissa (477106)

**Yksityinen**-kentän asetukseksi tulee nyt oletusarvoisesti **Kyllä**, kun työntekijät lisäävät uusia osoitetietoja työntekijän itsepalvelun **Henkilökohtaiset tiedot** -sivulla. 

## <a name="candidates-to-hire-fasttab-in-personnel-management-shows-an-incorrect-count-of-candidates-470110"></a>Henkilöstöhallinnon Palkattavat ehdokkaat -pikavälilehdessä on virheellinen ehdokasmäärä (470110)

Palkattavien ehdokkaiden määrä näkyy nyt oikein **Henkilöstöhallinto**-sivulla. 

## <a name="cant-enter-sickness-for-terminated-employee-when-accrual-is-set-to-zero-446195"></a>Työntekijän, jonka työsuhde on päättynyt, sairauslomaa ei voi antaa, kun jaksotukseksi on määritetty nolla (446195)

Poissaolotapahtumat ovat nyt mahdollisia työntekijöille, joiden työsuhde on päättynyt tulevaisuudessa, ja jaksotukseksi on määritetty nolla. Poissaolotapahtumia voidaan antaa työntekijän työsuhteen päättymiseen saakka. 

## <a name="adding-custom-fields-to-the-new-worker-form-disables-the-fields-in-the-action-pane-for-manage-leave-473314"></a>Mukautettujen kenttien lisääminen uuteen työntekijälomakkeeseen poistaa kentät käytöstä poissaolon hallinnan toimintopaneelissa (473314)

**Poissaolojen hallinnan** uuden **Työntekijä**-lomakkeen toimintopaneelin vaihtoehtoja ei enää poisteta käytöstä, jos uuteen **Työntekijä**-kenttään on lisätty mukautettuja kenttiä.

## <a name="making-the-leave-comment-field-mandatory-allows-a-leave-request-to-be-submitted-when-no-comment-is-entered-473543"></a>Poissaolon kommenttikentän pakollisuus sallii poissaolopyynnön lähettämisen, kun kommenttia ei lisätty (473543)

Kommenttikentät voivat olla nyt pakollisia, ja poissaolopyynnöt noudattavat tätä asetusta. Pakolliset kentät ovat esiversiotoimintoja.

### <a name="dmf-entity-available-for-accrual-suspensions"></a>DMF-yksikkö käytettävissä suoriteperusteisia keskeytyksiä varten

DMF-yksikkö on nyt käytettävissä suoriteperusteisia keskeytyksiä varten.

## <a name="in-preview"></a>Esiversiossa

### <a name="mandatory-fields"></a>Pakolliset kentät

Voit tehdä kentistä pakollisia käyttämällä henkilöstöhallinnon mukauttamisominaisuuksia. Tämä toiminto edellyttää **tallennettuja näkymiä**. Lisätietoja tallennetuista näkymistä on kohdassa:

- [Tallennetut näkymät – yleinen käytettävyys](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/finance-operations/finance-operations-crossapp-capabilities/saved-views--general-availability) Dynamics 365 2020 Release Wave 2 -suunnitelmassa
- [Tallennettuja näkymiä täysimääräisesti hyödyntävien lomakkeiden luominen](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/user-interface/understanding-saved-views)

### <a name="human-resources-application-in-teams"></a>Teamsin Human Resources -sovellus

Työntekijät voivat tarkastella ja pyytää lomaa työstä Microsoft Teamsissä. Ne voivat olla vuorovaikutuksessa botin kanssa luodakseen lomapyyntöjä. Lisätietoja:

- [Työntekijän loma- ja poissaolokokemus Microsoft Teamsissa](https://docs.microsoft.com/dynamics365-release-plan/2020wave1/dynamics365-human-resources/employee-leave-absence-experience-teams) Dynamics 365 2020 Release Wave 1 -suunnitelmassa
- [Teamsin Human Resources -sovellus](https://go.microsoft.com/fwlink/?linkid=2127841)

## <a name="coming-soon"></a>Tulossa pian

### <a name="human-resources-app-in-teams-preview-features"></a>Human Resources -sovellus Teamsin esiversiotoiminnoissa
 
-  **Ilmoitukset**: Poissaolopyyntöjen lähettäjät ja hyväksyjät saavat ilmoitukset Teamsin Human Resources -sovelluksessa. Hyväksyjät voivat hyväksyä tai hylätä poissaolopyyntöjä, ja lähettäjille ilmoitetaan, jos pyyntö hyväksyttiin tai hylättiin.
 
- **Esimiehen poissaolokalenteri**: Esimiehet voivat nähdä suorien alaisten hyväksytyt ja odottavat poissaolot kalenterinäkymässä. Tämän näkymän avulla on helppo hahmottaa, milloin ryhmä jäsenet ovat poissa töistä.

### <a name="checklist-entities-included-in-dataverse"></a>Dataverseen sisältyvät tarkistusluettelokohdat

Käyttöönotto-, käytöstäpoisto-, siirto- ja liiketoimintaprosessien tarkistusluettelokohdat ovat pian saatavilla Dataversessä.

## <a name="known-issues"></a>Tunnetut ongelmat

**Ominaisuuksien hallinta** -työtilassa voi olla ominaisuuksia, jotka on poistettu käytöstä esikatselun ominaisuutena, kun ne ovat yleisesti saatavilla. Alla on luettelo yleisesti käytettävissä olevista ominaisuuksista, joiden tila on virheellinen. 

- Etujen hallinta
- Palvelupyynnön hallinta
- Tietokannan lokikirjaus (valvonta)
- Loman jaksotus yhdelle yritykselle tai yhdelle suunnitelmalle
- Lomien ja poissaolojen jaksotuksen keskeytys
- Saldon oikaisun syykoodi ja kommentti
- Vaihda lomaa rahaksi tai lomapalkka vapaaksi
- Loma- ja poissaolokalenteri
- Loman siirtokirjaussäännöt
- Loman jaksotuksen tarkistus
- Loman jaksotuksen poisto
- Lomien jaksotusten pyöristys
- Määritä useita lomatyyppejä yhdessä lomasuunnitelmassa
- Poissaolon päivityksen parannukset
- Käytä työntekijän toimen laskennallista kokopäivätoimisuutta jaksotuksessa
- Yritystenvälinen kompensaationäkymä
- Kehityskeskustelujen tulostaminen
- Loman jaksotuksen juhlapäiväkorjaukset

### <a name="benefit-plan-employee-entity"></a>Etuussuunnitelman työntekijäentiteetti 

**EtuussuunnitelmaTyöntekijä**-entiteetissä on äskettäin havaittu kaksi ongelmaa. Kun työntekijöiden rekisteröitymisiä tuodaan, **Kattavuuskoodi** ja **Suunnitelman tyypin koodi** määritetään virheellisesti. Näiden ongelmien vuoksi työtekijöiden etuussuunnitelmat näkyvät virheellisesti **Työtekijän etuussuunnitelma**- ja **Avoin ilmoittautuminen** -lomakkeissa työntekijän itsepalvelussa. Tämä ongelma voi vaikuttaa myös työntekijän mahdollisuuteen valita suunnitelma työntekijän itsepalvelussa. Tällä hetkellä ongelmaa ei voi välttää. Tätä ongelmaa käsitellään korkean prioriteetin korjauksena, ja korjaus otetaan käyttöön seuraavassa versiossa.

## <a name="see-also"></a>Lisätietoja

[Human Resourcesin uudet ja muuttuneet ominaisuudet](hr-admin-whats-new.md)</br>
[Yhteenveto Dynamics 365 Human Resourcesin vuoden 2019 julkaisuaallosta 2](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[Päivitysprosessi](hr-admin-setup-update-process.md)</br>
[Hallitse ominaisuuksia](hr-admin-manage-features.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]