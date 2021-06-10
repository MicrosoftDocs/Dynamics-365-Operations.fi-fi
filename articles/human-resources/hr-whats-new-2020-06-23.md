---
title: Dynamics 365 Human Resourcesin uudet ja muuttuneet ominaisuudet (25. kesäkuuta 2020)
description: Tässä ohjeaiheessa käsitellään Microsoft Dynamics 365 Human Resourcesin 23. kesäkuuta 2020 julkaistuja uusia tai muuttuneita ominaisuuksia.
author: andreabichsel
ms.date: 06/25/2020
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
ms.search.validFrom: 2020-06-25
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 228883dd4af3f4f51c53524813c1852d392c1d29
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/18/2021
ms.locfileid: "6053944"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-june-23-2020"></a>Dynamics 365 Human Resourcesin uudet ja muuttuneet ominaisuudet (23. kesäkuuta 2020)

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Tässä ohjeaiheessa käsitellään Dynamics 365 Human Resourcesin uusia tai muuttuneita ominaisuuksia. Muutokset koskevat koontiversion numeroa 8.1.3347. Joissakin otsikoissa suluissa olevat luvut viittaavat tukinumeroihin LCS-palveluissa.

## <a name="when-an-enrollment-is-expired-for-a-terminated-employee-the-leave-type-balance-and-amount-are-all-cleared-in-the-leave-enrollment-form-444867"></a>Kun poistetun työntekijän rekisteröityminen vanhenee, loman tyyppi, saldo ja määrä nollataan loman rekisteröintilomakkeessa (444867)

**Lomatyyppi**, **Saldo** ja **Määrä** säilyvät nyt nollaamiseen sijaan, kun teet tämän valinnan.

## <a name="incorrect-forecasted-balance-when-new-feature-leave-accrual-for-a-single-company-or-a-single-plan-is-enabled-456553"></a>Virheellinen ennustettu saldo, kun uusi ominaisuus (loman jaksotus yksittäisessä yrityksessä tai yksittäisessä suunnitelmassa) (456553)

Oikea ennustettu saldo näkyy nyt, kun yksittäisen yrityksen tai yksittäisen suunnitelman loman jaksotus on otettu käyttöön.

## <a name="entities-with-relations-that-result-in-duplicate-navigation-properties-456486"></a>Yksiköt, joilla on suhteita, jotka aiheuttavat kaksinkertaisia navigointiominaisuuksia (456486)

Tämä versio korjaa ongelman, joka liittyy useiden yksiköiden navigointiominaisuuksiin (suhteeseen). Kaksinkertaisia suhteita havaitaan. Kaikki nämä tapaukset on korjattu.
 
## <a name="cross-company-comments-on-performance-review-455536"></a>Yritysten väliset kommentit suorituskykyarviossa (455536)

Yritysten väliset kommentit näkyvät nyt suorituskykyarvioissa tämän korjauksen myötä. Tämä muutos korjaa niiden arvioijan kommenttien näkymän, jotka syötettiin eri yrityksissä samaan suorituskykyarvioon.
 
## <a name="inconsistency-in-showing-compensation-management-data-432562"></a>Epäjohdonmukaisuus kompensaationhallintatietojen näyttämisessä (432562)

Kompensaatiotietojen johdonmukainen näkymä säilyy nyt esimiehen itsepalvelussa. Sen mukaan, miten siirryt työntekijän **kompensaatiotietoihin**, kompensaatiotiedot näkyvät nyt johdonmukaisesti esimiehille.
 
## <a name="fixed-compensation-plans-effective-date-defaults-to-todays-date-411994"></a>Korjatun kompensaatiosuunnitelman voimaantulopäivä on oletusarvoisesti kuluva päivä (411994)

Kompensaation alkamispäivä perustuu nyt työntekijälle määritetyn aseman alkamispäivään.

## <a name="leave-and-absence-form-enable-half-day-definition-is-disabled-when-form-opens-452607"></a>Loma- ja poissaololomakkeen Ota käyttöön puolipäiväiset määritykset on pois käytöstä, kun lomake avautuu (452607)

Tämän muutoksen myötä **Ota käyttöön puolipäiväiset määritykset** on käytössä, kunnes uusi lomatapahtuma on olemassa. 

## <a name="unable-to-publish-to-hcmdiscussionentity-via-excel-totalratingscore-field-error-453899"></a>HcmDiscussionEntity-arvoa ei voida julkaista Excelissä; TotalRatingScore-kenttävirhe (453899)

Nyt voit päivittää **TotalRatingScore**-kentän käyttämällä **HCMDiscussionEntity**-arvoa Excel-työkirjan suunnittelussa.

## <a name="in-preview"></a>Esiversiossa

## <a name="database-logging"></a>Tietokannan lokiinkirjaus

Tietokantakirjauksen avulla voit määrittää, mitä taulukoita ja kenttiä seurataan. Sen avulla voit myös määrittää tapahtumat, jotka käynnistävät muutosten seurannan. Tietokantakirjauksen ominaisuuksien avulla nähdään nämä muutokset ajan kuluessa. Lisätietoja on kohdassa [Tietokantakirjauksen määrittäminen ja hallinta](hr-admin-database-logging.md).

## <a name="mandatory-fields"></a>Pakolliset kentät 

Nyt voit tehdä kentistä pakollisia käyttämällä henkilöstöhallinnon mukauttamisominaisuuksia. Tämä toiminto edellyttää **tallennettuja näkymiä**.

## <a name="human-resources-application-in-teams"></a>Teamsin Human Resources -sovellus

Työntekijät voivat tarkastella ja pyytää lomaa työstä Microsoft Teamsissä. Ne voivat olla vuorovaikutuksessa botin kanssa luodakseen lomapyyntöjä. Lisätietoja on kohdassa [Human Resources -sovellus Teamsissa](./hr-admin-teams-leave-app.md). 

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

## <a name="configure-the-name-of-employee-self-service"></a>Työntekijän itsepalvelun nimen määrittäminen

**Henkilöstöhallintoparametreissa** on uusi vaihtoehto, jolla voi päivittää Työntekijän itsepalvelu -työtilan nimen itsepalveluksi.

## <a name="checklist-entities-included-in-dataverse"></a>Dataverseen sisältyvät tarkistusluettelokohdat

Käyttöönotto-, käytöstäpoisto-, siirto- ja liiketoimintaprosessien tarkistusluettelokohdat ovat pian saatavilla Dataversessä.

## <a name="see-also"></a>Lisätietoja

[Human Resourcesin uudet ja muuttuneet ominaisuudet](hr-admin-whats-new.md)</br>
[Yhteenveto Dynamics 365 Human Resourcesin vuoden 2019 julkaisuaallosta 2](/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[Päivitysprosessi](hr-admin-setup-update-process.md)</br>
[Hallitse ominaisuuksia](hr-admin-manage-features.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]