---
title: Dynamics 365 Human Resourcesin uudet ja muuttuneet ominaisuudet (06. huhtikuuta 2020)
description: Tässä ohjeaiheessa käsitellään Microsoft Dynamics 365 Human Resourcesin 6. elokuuta 2020 julkaistuja uusia tai muuttuneita ominaisuuksia.
author: andreabichsel
ms.date: 08/06/2020
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
ms.search.validFrom: 2020-08-06
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 263650cae4b8408f1f7a4a27c43294d2f51c1444
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2021
ms.locfileid: "5800138"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-august-06-2020"></a>Dynamics 365 Human Resourcesin uudet ja muuttuneet ominaisuudet (06. huhtikuuta 2020)

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Tässä ohjeaiheessa käsitellään Dynamics 365 Human Resourcesin uusia tai muuttuneita ominaisuuksia. Muutokset koskevat koontiversion numeroa 8.1.3444. Joissakin otsikoissa suluissa olevat luvut viittaavat tukinumeroihin LCS-palveluissa.

## <a name="platform-update-1001236-is-now-available"></a>Platform Update 10.0.12(36) on nyt saatavana

Lisätietoja on kohdassa [Finance and Operations -sovellusten version 10.0.12 ympäristöpäivitykset (elokuu 2020)](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/get-started/whats-new-platform-update-10-0-12).

## <a name="data-management-framework-dmf-entities-for-benefits-management"></a>Tietojen hallintakehys (DMF) -yksiköt etuuksien hallintaa varten
 
Etujen hallintayksiköt julkaisevat. DMF-yksikköjen avulla voi tuoda ja viedä tietoja, mikä helpottaa etuuksien hallinnan määrittämistä. Tietojen siirtämiseen on käytettävissä etuuksien hallintamalli. Malli vie tiedot ja tuo ne peräkkäin tietojen riippuvaisuuksia noudattaen. Lisätietoja:

- [DMF-yksikkötuki](https://docs.microsoft.com/dynamics365-release-plan/2020wave1/dynamics365-human-resources/dmf-entity-support) Dynamics 365 2020 Release Wave 1 -suunnitelmassa
- [Tietojen hallinnan yleiskatsaus](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/data-entities/data-entities-data-packages)


## <a name="claire-creates-a-workflow-for-buying-and-selling-leave-requests-446557"></a>Claire luo työnkulun poissaolojen osto- ja myyntipyynnöille (446557)

Lisätietoja:

- [Salli työntekijöiden ostaa ja myydä lomaa](https://docs.microsoft.com/dynamics365-release-plan/2020wave1/dynamics365-human-resources/allow-employees-buy-sell-leave) Dynamics 365 2020 Release Wave 2 -suunnitelmassa
- [Käytäntöjen hallinta loman vaihtamisessa rahaksi ja lomapalkan vaihtamisessa vapaaksi](https://docs.microsoft.com/dynamics365/human-resources/hr-leave-and-absence-manage-buy-and-sell-leave-policies)
- [Vaihda lomaa rahaksi tai lomapalkka vapaaksi](https://docs.microsoft.com/dynamics365/human-resources/hr-employee-self-service-buy-sell-leave)


## <a name="worker-postal-addresses-v2-entity-has-access-across-legal-entities-with-restricted-access-459126"></a>Työntekijän postiosoitteet V2-yksikkö käyttää yrityksiä, joilla on rajoitetut käyttöoikeudet (459126)

Tämän muutoksen yhteydessä **työntekijän postiosoite V2** -yksikkö rajoittaa käyttäjän antaman oikeushenkilön käyttöoikeuden perusteella.

## <a name="workflow-email-hyperlink-fails-to-open-relevant-reviews-437398"></a>Työnkulun sähköpostin hyperlinkki ei avaa asiaankuuluvia arvosteluja (437398)

Kun käytät paikkamerkkiä tarkistustyönkulun suorituskyvyn tarkistuksen avaamiseen, sähköpostissa muodostettu hyperlinkki avaa valitun tietueen.

## <a name="new-entities-for-buying-and-selling-leave-473180"></a>Uudet yksiköt, jotka ostavat ja myyvät lomaa (473180)

Tietojen hallinnan puiteyksiköt ovat nyt ostamassa ja myymässä lomaa. Lisätietoja on kohdassa [Tiedonhallinnan yleiskatsaus](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/data-entities/data-entities-data-packages).

## <a name="when-viewing-record-information-and-using-advanced-filters-a-user-could-gain-access-to-other-employees-records-472490"></a>Kun tarkastelet tietuetietoja ja käytät kehittyneitä suodattimia, käyttäjä voi käyttää muiden työntekijöiden tietueita (472490)

Tämän muutoksen avulla työntekijöiden itsepalvelukäyttäjät voivat käyttää vain omia tietueitaan, kun he käyttävät työntekijöiden itsepalvelua. Tietuetietojen tarkasteleminen suodatusasetuksia muutettaessa ei enää näytä lisätietoja.

## <a name="personnel-management-analytics-include-exited-worker-records-382893"></a>Henkilöstöhallinnon analyysit sisältävät poistuneet työntekijätiedot (382893)

Tässä julkaisussa henkilöstöhallinnan analyysi sisältää nyt vain aktiiviset työntekijät. 
 
## <a name="unable-to-process-a-merit-increase-for-an-employee-473125"></a>Työntekijän ansiolisäystä ei voi käsitellä (473125)

Tämän muutoksen avulla voit lisätä ansiolisäyksiä, kun muutat uuden ansiolisäyksen voimaantulopäivämäärää.

## <a name="review-workflow-can-be-started-more-than-once-467541"></a>Tarkistustyönkulku voidaan aloittaa useammin kuin kerran (467541)

Tämän muutoksen avulla voit käynnistää suorituskyvyn tarkistuksen työnkulun vain kerran. Esimiehen tila ei enää näytä tarkistuksen aloitusvaihtoehtoa.

## <a name="leave-request-work-flow-ends-in-error-when-canceling-an-approved-leave-request-472063"></a>Lomapyynnön työnkulku päättyy virheeseen, kun hyväksyttyä lomapyyntöä peruutetaan (472063)

Kun peruutat hyväksytyn lomapyynnön, pyynnön tila ei enää ole hyväksytty tässä versiossa, ja työnkulku jatkuu.

## <a name="system-suggests-exited-workers-when-creating-a-new-review-form-the-template-460624"></a>Järjestelmä ehdottaa poistuneita työntekijöistä, kun uusi tarkastelu luodaan mallista (460624)

Tämän muutoksen myötä poistuneet työntekijät ovat enää käytettävissä, kun uusia arvosteluja luodaan mallista. Et voi luoda sellaisten työntekijöiden arvosteluja, jotka eivät ole työpäivien ulkopuolella.

## <a name="position-hierarchy-circular-reference-detection-415879"></a>Toimen hierarkian kehäviittauksen havaitseminen (415879)

Tämän muutoksen yhteydessä toimihierarkiakehäviittauksen tunnistaminen on rajoitettu yhteen ajankohtaan. Voit määrittää eri päivämäärien kehäviittauksen tunnistamisen, kun haluat tarkistaa, ettei raportointirakenteessa ole kehäviittauksia.

## <a name="buy-and-sell-leave"></a>Vaihda lomaa rahaksi tai lomapalkka vapaaksi 

Jotkut organisaatiot tarjoavat edun, jonka avulla työntekijät voivat vaihtaa lomaa rahaksi tai rahaa vapaaksi. Tätä prosessia hallitaan usein manuaalisesti. Tämä toiminto automatisoi henkilöstöosaston käytäntöjen ja pyyntöjen hallinnan. Se sujuvoittaa lomien hallintaprosessia ja auttaa poistamaan virheitä. Lisätietoja:

- [Salli työntekijöiden ostaa ja myydä lomaa](https://docs.microsoft.com/dynamics365-release-plan/2020wave1/dynamics365-human-resources/allow-employees-buy-sell-leave) Dynamics 365 2020 Release Wave 2 -suunnitelmassa
- [Käytäntöjen hallinta loman vaihtamisessa rahaksi ja lomapalkan vaihtamisessa vapaaksi](https://docs.microsoft.com/dynamics365/human-resources/hr-leave-and-absence-manage-buy-and-sell-leave-policies)
- [Vaihda lomaa rahaksi tai lomapalkka vapaaksi](https://docs.microsoft.com/dynamics365/human-resources/hr-employee-self-service-buy-sell-leave)

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

## <a name="in-preview"></a>Esiversiossa

### <a name="mandatory-fields"></a>Pakolliset kentät

Voit tehdä kentistä pakollisia käyttämällä henkilöstöhallinnon mukauttamisominaisuuksia. Tämä toiminto edellyttää **tallennettuja näkymiä**. Lisätietoja tallennetuista näkymistä on kohdassa:

- [Tallennetut näkymät – yleinen käytettävyys](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/finance-operations/finance-operations-crossapp-capabilities/saved-views--general-availability) Dynamics 365 2020 Release Wave 2 -suunnitelmassa
- [Tallennettuja näkymiä täysimääräisesti hyödyntävien lomakkeiden luominen](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/user-interface/understanding-saved-views)

### <a name="human-resources-application-in-teams"></a>Teamsin Human Resources -sovellus

Työntekijät voivat tarkastella ja pyytää lomaa työstä Microsoft Teamsissä. Ne voivat olla vuorovaikutuksessa botin kanssa luodakseen lomapyyntöjä. Lisätietoja:

- [Työntekijän loma- ja poissaolokokemus Microsoft Teamsissa](https://docs.microsoft.com/dynamics365-release-plan/2020wave1/dynamics365-human-resources/employee-leave-absence-experience-teams) Dynamics 365 2020 Release Wave 1 -suunnitelmassa
- [Teamsin Human Resources -sovellus](https://go.microsoft.com/fwlink/?linkid=2127841)

### <a name="dmf-entity-available-for-accrual-suspensions"></a>DMF-yksikkö käytettävissä suoriteperusteisia keskeytyksiä varten

DMF-yksikkö on nyt käytettävissä suoriteperusteisia keskeytyksiä varten.

## <a name="coming-soon"></a>Tulossa pian

## <a name="checklist-entities-included-in-dataverse"></a>Dataverseen sisältyvät tarkistusluettelokohdat

Käyttöönotto-, käytöstäpoisto-, siirto- ja liiketoimintaprosessien tarkistusluettelokohdat ovat pian saatavilla Dataversessä.

## <a name="known-issues"></a>Tunnetut ongelmat

**Ominaisuuksien hallinta** -työtilassa voi olla ominaisuuksia, jotka on poistettu käytöstä esikatselun ominaisuutena, kun ne ovat yleisesti saatavilla. Alla on luettelo yleisesti käytettävissä olevista ominaisuuksista, joiden tila on virheellinen. 

1.  Etujen hallinta
2.  Palvelupyynnön hallinta
3.  Tietokannan lokikirjaus (valvonta)
4.  Loman jaksotus yhdelle yritykselle tai yhdelle suunnitelmalle
5.  Lomien ja poissaolojen jaksotuksen keskeytys
6.  Saldon oikaisun syykoodi ja kommentti
7.  Vaihda lomaa rahaksi tai lomapalkka vapaaksi
8.  Loma- ja poissaolokalenteri
9.  Loman siirtokirjaussäännöt
10. Loman jaksotuksen tarkistus
11. Loman jaksotuksen poisto
12. Lomien jaksotusten pyöristys
13. Määritä useita lomatyyppejä yhdessä lomasuunnitelmassa
14. Poissaolon päivityksen parannukset
15. Käytä työntekijän toimen laskennallista kokopäivätoimisuutta jaksotuksessa
16. Yritystenvälinen kompensaationäkymä
17. Kehityskeskustelujen tulostaminen
18. Loman jaksotuksen juhlapäiväkorjaukset

## <a name="see-also"></a>Lisätietoja

[Human Resourcesin uudet ja muuttuneet ominaisuudet](hr-admin-whats-new.md)</br>
[Yhteenveto Dynamics 365 Human Resourcesin vuoden 2019 julkaisuaallosta 2](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[Päivitysprosessi](hr-admin-setup-update-process.md)</br>
[Hallitse ominaisuuksia](hr-admin-manage-features.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]