---
title: Dynamics 365 Human Resources:n uudet tai muuttuneet ominaisuudet (03. syyskuuta 2020)
description: Tässä ohjeaiheessa käsitellään Microsoft Dynamics 365 Human Resourcesin 3. syyskuuta 2020 julkaistuja uusia tai muuttuneita ominaisuuksia.
author: andreabichsel
ms.date: 09/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2020-09-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: eae89e9c3bf32ab5a4c4e6c497c9d3baa5b75fde
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 07/06/2021
ms.locfileid: "6359218"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-september-3-2020"></a>Dynamics 365 Human Resources:n uudet tai muuttuneet ominaisuudet (3. syyskuuta 2020)

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Tässä ohjeaiheessa käsitellään Dynamics 365 Human Resourcesin uusia tai muuttuneita ominaisuuksia. Muutokset koskevat koontiversion numeroa 8.1.3504. Joissakin otsikoissa suluissa olevat luvut viittaavat Lifecycle Services (LCS) -palveluiden tukinumeroihin.

Lisätietoja Human Resources -sovelluksen tulevista ominaisuuksista on kohdassa [Dynamics 365 Human Resources -sovelluksen vuoden 2019 julkaisuaallon 2 yleiskatsaus](/dynamics365-release-plan/2019wave2/dynamics365-human-resources/). Lisätietoja Human Resources -sovelluksen päivitysprosessista on kohdassa [Päivitysprosessi](hr-admin-setup-update-process.md).

## <a name="in-this-release"></a>Tässä julkaisussa

### <a name="new-default-financial-dimensions-grid-and-dialog-pattern-throughout-human-resources-469495"></a>Uusi taloushallinnon dimension oletusruudukko ja valintaikkunan malli koko Human Resources -sovelluksessa (469495)

Uusi taloushallinnon dimension malli on nyt käytettävissä seuraavilla alueilla:

- Toimen toiminnot (lomake **HcmPositionActionDetail**)
- Palkanlaskennan ansiokoodit (lomake **PayrollEarningCode**)

### <a name="entries-dont-appear-in-company-leave-calendar-if-leave-and-absence-calendar-enhancements-arent-enabled-484406"></a>Merkinnät eivät näy yrityksen lomakalenterissa, jos loma- ja poissaolokalenterin parannukset eivät ole käytössä (484406)

Tämä versio korjaa ongelman, jossa lomamerkinnät eivät näy yrityksen lomakalenterissa. Tämä ongelma ilmenee vain, kun Ominaisuuksien hallinta -vaihtoehdon **Loma- ja poissaolokalenterin parannukset** -kohta ei ole käytössä.

### <a name="benefitplanemployeeentity-issue-467597"></a>BenefitPlanEmployeeEntity-ongelma (467597)

Tämä julkaisu korjaa ongelman, joka liittyy **BenefitsPlanEmployee**-entiteettiin. Kun työntekijöiden rekisteröitymisiä tuodaan, **Kattavuuskoodi** ja **Suunnitelman tyypin koodi** määritetään nyt oikein. Näiden ongelmien vuoksi työtekijöiden etuussuunnitelmat näkyivät virheellisesti **Työtekijän etuussuunnitelma**- ja **Avoin ilmoittautuminen** -lomakkeissa työntekijän itsepalvelussa.

### <a name="electronic-file-1094-c-output-missing-letter-in-xml-435190"></a>Sähköisen tiedoston 1094-C tulosteesta puuttuu kirjain XML-muodossa (435190)

Tämä muutos korjaa ongelman, jossa 1094-C-tulostetiedostossa ei ole tarvittavia merkkejä, kun se lähetetään IRS:lle.

### <a name="employee-variable-compensation-table-mapped-to-fixed-compensation-form-476117"></a>Työtekijöiden muuttuvan kompensaation taulu, joka on liitetty kiinteän kompensaation lomakkeeseen (476117)

Tämä muutos tasaa kiinteän kompensaation kentät kiinteän kompensaation lomakkeen kanssa. Muuttuvan kompensaation kentät ovat nyt käytettävissä vain muuttuvan kompensaation lomakkeessa.

### <a name="leave-requests-allowed-before-enrollment-if-that-leave-type-has-a-negative-minimum-balance-469917"></a>Lomapyynnöt sallitaan ennen rekisteröintiä, jos tämän lomatyypin vähimmäissaldo on negatiivinen (469917)

Tämä muutos ei salli lomapyyntöjen syöttämistä ennen kuin ne rekisteröidään suunnitelmaan, vaikka rekisteröinnin vähimmäissaldo olisi negatiivinen. Voit syöttää pyynnöt tai lähettää ne vain, kun suunnitelma on aktiivinen.

### <a name="document-templates-dont-download-457279"></a>Asiakirjamalleja ei voi ladata (457279)

Tämän muutoksen avulla voit nyt ladata kaikki asiakirjamallit. 

### <a name="data-displays-as-column-headers-instead-of-rows-for-the-pay-rate-field-in-the-compensation-plan-report-476077"></a>Tiedot näkyvät sarakeotsikkoina kompensaatiosuunnitelmaraportin palkkiokentässä rivien sijaan (476077)

Analyysiraportissa näkyvät nyt oikeat **palkkion** tiedot.

## <a name="in-preview"></a>Esiversiossa

### <a name="human-resources-application-in-teams"></a>Teamsin Human Resources -sovellus

Työntekijät voivat tarkastella ja pyytää lomaa työstä Microsoft Teamsissä. Ne voivat olla vuorovaikutuksessa botin kanssa luodakseen lomapyyntöjä. Lisätietoja:

- [Työntekijän loma- ja poissaolokokemus Microsoft Teamsissa](/dynamics365-release-plan/2020wave1/dynamics365-human-resources/employee-leave-absence-experience-teams) Dynamics 365 2020 Release Wave 1 -suunnitelmassa
- [Teamsin Human Resources -sovellus](./hr-admin-teams-leave-app.md) Human Resources -sovelluksen dokumentaatiossa

### <a name="human-resources-app-in-teams-preview-features"></a>Human Resources -sovellus Teamsin esiversiotoiminnoissa
 
-  **Ilmoitukset**: Poissaolopyyntöjen lähettäjät ja hyväksyjät saavat ilmoitukset Teamsin Human Resources -sovelluksessa. Hyväksyjät voivat hyväksyä tai hylätä poissaolopyyntöjä. Lähettäjille ilmoitetaan, jos pyyntö on hyväksytty tai hylätty. Lisätietoja:
   - [Työntekijän loma- ja poissaolokokemus Microsoft Teamsissa](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/employee-leave-absence-experience-teams) Dynamics 365 2020 Release Wave 2 -suunnitelmassa
   - [Teamsin Human Resources -sovelluksen ilmoitusten käyttöönotto](./hr-admin-teams-leave-app.md#enable-notifications-for-the-human-resources-app-in-teams) Human Resources -sovelluksen dokumentaatiossa
   - [Teams-ilmoitusten käyttöönotto tai käytöstäpoisto yksittäisille käyttäjille](./hr-admin-teams-leave-app.md#turn-teams-notifications-on-or-off-for-individual-users) Human Resources -sovelluksen dokumentaatiossa
   - [Teams-ilmoitukset](./hr-teams-leave-app.md#respond-to-teams-notifications) Human Resources -sovelluksen dokumentaatiossa
   - [Ryhmän lomakalenterin tarkasteleminen](./hr-teams-leave-app.md#view-your-teams-leave-calendar) Human Resources -sovelluksen dokumentaatiossa
 
- **Esimiehen poissaolokalenteri**: Esimiehet voivat nähdä suorien alaisten hyväksytyt ja odottavat poissaolot kalenterinäkymässä. Tämän näkymän avulla on helppo hahmottaa, milloin ryhmä jäsenet ovat poissa töistä. Lisätietoja:
   - [Työntekijän loma- ja poissaolokokemus Microsoft Teamsissa](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/employee-leave-absence-experience-teams) Dynamics 365 2020 Release Wave 2 -suunnitelmassa
   - [Ryhmän lomakalenterin tarkasteleminen](./hr-teams-leave-app.md#view-your-teams-leave-calendar) Human Resources -sovelluksen dokumentaatiossa

### <a name="configuration-option-to-position-work-items-assigned-to-me-list-477004"></a>Toimen Itselle määritetyt työnimikkeet -luettelon määritysasetus (477004)

Uusi asetus on nyt käytettävissä toimelle **Itselle määritetyt työnimikkeet** -luettelossa koontinäytön oikeanpuoleisessa sarakkeessa. Tämän muutoksen myötä kaikki työnimikkeet ja tehtäväluettelot näkyvät samalla alueella. Jos haluat tämän toiminnon käyttöön, ota käyttöön **Esikatselu - työnkulun käyttökokemuksen parannukset** -kohta ominaisuuksien hallinnassa. Lisätietoja esikatseluominaisuuksien ottamisesta käyttöön on kohdassa [Ominaisuuksien hallinta](hr-admin-manage-features.md).

Tämä toiminto edistää myös henkilöstön toimintojen lomakkeissa olevia työnkulkuasetuksia. Työnkulunasetukset näkyvät myös toiminnon nopean käytön pikavälilehdessä. Lisätietoja: 

- [Organisaation ja henkilöstön hallinnan työnkulun käyttökokemuksen parannukset](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/organization-personnel-management-workflow-experience-enhancements) Dynamics 365:n vuoden 2020 julkaisuaallon 2 suunnitelmassa

![Minulle määritetyt työnimikkeet.](./media/hr-workflow-work-items-assigned-to-me.png)

![Työnkulkunimikkeiden nopea käyttö.](./media/hr-workflow-quick-access.png)

## <a name="coming-soon"></a>Tulossa pian

### <a name="checklist-entities-included-in-dataverse"></a>Dataverseen sisältyvät tarkistusluettelokohdat

Käyttöönotto-, käytöstäpoisto-, siirto- ja liiketoimintaprosessien tarkistusluettelokohdat ovat pian saatavilla Dataversessä.

### <a name="benefits-management-reason-codes"></a>Etujen hallinnan syykoodit

Etujen hallinnan syykoodit yhdistetään pian olemassa oleviin syykoodeihin Human Resources -sovelluksessa. Jos olet määrittänyt etujen hallinnassa syykoodeja, joiden pituus on yli 15 merkkiä, syykoodin nimeä on muutettava etujen hallinnan **Syykoodit**-lomakkeessa niin, että pituus on enintään 15 merkkiä. Kun olet päivittänyt nimen, syykoodi näkyy olemassa olevan syykoodilomakkeen henkilöstön hallinnassa. Tämä muutos on käytettävissä tulevaisuudessa. Se ei vaikuta olemassa oleviin toimintoihin.

## <a name="see-also"></a>Lisätietoja

[Human Resourcesin uudet ja muuttuneet ominaisuudet](hr-admin-whats-new.md)</br>
[Yhteenveto Dynamics 365 Human Resourcesin vuoden 2019 julkaisuaallosta 2](/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[Päivitysprosessi](hr-admin-setup-update-process.md)</br>
[Hallitse ominaisuuksia](hr-admin-manage-features.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
