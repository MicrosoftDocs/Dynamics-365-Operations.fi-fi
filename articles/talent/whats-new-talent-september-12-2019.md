---
title: Dynamics 365 for Talent:n uudet tai muuttuneet ominaisuudet (10. syyskuuta 2019)
description: Tässä ohjeaiheessa käsitellään Microsoft Dynamics 365 for Talentin uusia tai muuttuneita ominaisuuksia.
author: Darinkramer
manager: AnnBe
ms.date: 9/10/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2019-09-10
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 48f41b53060c7f2bfc407b22295aa40d85ce1c9d
ms.sourcegitcommit: 7a93ea2dc90d31175b708566a00cd707cb47ab7c
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/13/2019
ms.locfileid: "1996185"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-september-10-2019"></a>Dynamics 365 for Talent:n uudet tai muuttuneet ominaisuudet (10. syyskuuta 2019)

[!include [banner](includes/banner.md)]

Tässä ohjeaiheessa käsitellään Dynamics 365 for Talentin uusia tai muuttuneita ominaisuuksia.

## <a name="changes-in-attract"></a>Attractin muutokset

### <a name="candidate-e-mail-login"></a>Ehdokkaan kirjautuminen sähköpostilla

Ehdokkaat voivat nyt käyttää mitä tahansa sähköpostiosoitetta luodakseen tilin ja kirjautuakseen sisään Talent-urasivustolle, josta he voivat hakea työpaikkaa ja tarkastaa hakemuksensa tilan. Tämän lisäksi he voivat kirjautua sisään Talent-urasivustolle käyttämällä yhteisöpalvelutiliään tai organisaation tunnuksia.

### <a name="job-activation-and-posting"></a>Töiden aktivointi ja kirjaaminen

Olemme tehneet joitakin muutoksia töiden aktivointiin ja kirjaamiseen. Sinun täytyy aktivoida työt ennen niiden kirjaamista Talent-urasivustolle tai ulkoisille työsivustoille, kuten LinkedIn tai Broadbean.

## <a name="changes-in-onboard"></a>Onboardin muutokset

Tässä julkaisussa on vähäisiä Dynamics 365 Talent: Onboard:n ohjelmakorjauksia.

## <a name="changes-in-core-hr"></a>Core HR:n muutokset

Tässä osassa kuvatut muutokset koskevat koontiversiota 8.1.2482. Joissakin otsikoissa suluissa olevat luvut viittaavat tukinumeroihin Microsoft Dynamics Lifecycle Services (LCS) -palveluissa.

### <a name="you-can-enable-preview-features-in-sandbox-and-trial-environments"></a>Voit ottaa esikatselutoiminnot käyttöön eristys- ja kokeiluympäristöissä

Voit määrittää Talentin uutta esiintymää valmisteltaessa, onko esiintymän tyyppi Tuotanto vai Eristys. Eristys-tyypin esiintymissä uusia toimintoja voi testata varhaisessa vaiheessa. Jos haluat, että jokin aiemmin luoduista esiintymistä päivitetään Eristys-esiintymätyypiksi, ota yhteyttä tukeen ja tee muutospyyntö.

Lisätietoja muutosten julkaisemisesta on kohdassa [Talentin valmistelu](./provisioning-talent.md).

### <a name="platform-update-29"></a>Ympäristön update 29 -päivitys

Lisätietoja Platform update 29 -päivityksestä on kohdassa [Dynamics 365 for Finance and Operations platform update 29 -esiversion toiminnot (lokakuu 2019)](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/get-started/whats-new-platform-update-29).

### <a name="new-job-base-entity-available-in-data-management-framework-347202"></a>Uusi perustyöyksikkö käytettävissä tietojen hallintakehyksessä (347202)

Tässä versiossa on käytettävissä uusi perustyöyksikkö, jonka avulla tietoja voidaan tuoda/viedä. 

### <a name="worker-advanced-security-policy-incorrectly-displays-positions-in-position-hierarchy-354868"></a>Työntekijöiden kehittynyt suojauskäytäntö näyttää toimet virheellisesti toimihierarkiassa (354868)

Tämän version myötä toimia ei näytetä enää avoimina "tyhjällä" työntekijällä, kun käyttäjillä on rajoitetut käyttöoikeudet.

### <a name="job-form-close-box-wont-close-form-in-certain-situations-342467"></a>Työlomakkeen sulkemisruutu ei sulje lomaketta tietyissä tilanteissa (342467)

Tämä julkaisu sisältää muutoksen, jonka avulla työlomake sulkeutuu kaikissa skenaarioissa.

### <a name="new-case-on-employee-record-is-locked-for-human-resources-manager-role-337111"></a>Työntekijäntietueen uusi palvelupyyntö on lukittu henkilöstöhallintopäällikön roolille (337111)

Tämän muutoksen myötä palvelupyyntöjen hallintalomake ei ole enää lukittuna, kun sitä käytetään työntekijälomakkeesta.

### <a name="employment-end-date-always-defaults-to-235959-351492"></a>Työsuhteen päättymispäivä on oletusarvoisesti aina klo 23.59.59 (351492).

Tämän muutoksen myötä voit muuttaa työsuhteen päivämäärän joksikin muuksi ajaksi kuin klo 23.59.59, kun työsuhde lopetetaan manuaalisesti.

### <a name="unable-to-set-up-expiration-date-on-an-earning-code-through-data-management-336604"></a>Ansiokoodin vanhentumispäivää ei voi määrittää tietojen hallinnan kautta (336604)

Tässä versiossa voit määrittää vanhenevat ansiokoodit **PayrollWorkerPositionEarningCodeEntity**-entiteetin kautta.

### <a name="employee-development-analytic-report-doesnt-display-data-348737"></a>Työntekijän kehitysanalyysin raportti ei näytä tietoja (348737)

Tämän viikon julkaisussa työntekijöiden osaamisalueiden analyysi on päivitetty tarjoamaan tarkkoja raportteja.

### <a name="terms-of-employment-datetime-dont-default-to-beginning-of-day-349101"></a>Työehtojen päivämäärä/aika eivät ole oletusarvoisesti päivän alussa (349101)

Tämän muutoksen myötä alkamispäivä/-aika on oletusarvoisesti päivän alussa ja päättymispäivä/-aika on oletusarvoisesti päivän lopussa.

### <a name="changing-the-employment-end-date-on-worker-action-form-displays-an-error-354092"></a>Työsuhteen päättymispäivän muuttaminen työntekijätietolomakkeesta aiheuttaa virheen (354092) 

Tämä muutos korjaa ongelman, kun työsuhteen päättymispäivää muokataan osana työntekijätoimintoa.

### <a name="applying-onboarding-checklists-across-companies-338433"></a>Perehdytyksen tarkistusluetteloiden käyttäminen eri yritysten välillä (338433)

Tämä julkaisu tarjoaa nyt mahdollisuuden käyttää tarkistusluetteloita työntekijöille, jotka työskentelevät muissa kuin sisäänkirjautuneessa yrityksessä.

## <a name="in-preview"></a>Esiversiossa

### <a name="streamlined-employee-entry-and-navigation"></a>Yksinkertaistettu työntekijöiden lisääminen ja navigointi

Tämä toiminto on nyt käytettävissä eristysympäristöissä. Ota tämä toiminto käyttöön valitsemalla **Järjestelmän hallinta > Linkit > Asetukset > Järjestelmän parametrit > Esiversio-ominaisuudet**. Valitse **Laajennettu työntekijälomake ja siirtyminen**. Nämä muutokset otetaan nyt käyttöön kaikille käyttäjille. Voit poistaa tämän asetuksen käytöstä milloin tahansa.

Lisätietoja on kohdassa [Yksinkertaistettu työntekijöiden lisääminen ja navigointi](./streamlined-employee-entry.md).
