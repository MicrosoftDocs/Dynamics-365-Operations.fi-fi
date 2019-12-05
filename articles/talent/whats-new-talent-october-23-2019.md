---
title: Dynamics 365 Talent:n uudet tai muuttuneet ominaisuudet (23. lokakuuta 2019)
description: Tässä ohjeaiheessa käsitellään Microsoft Dynamics 365 Talentin uusia tai muuttuneita ominaisuuksia.
author: Darinkramer
manager: AnnBe
ms.date: 10/23/2019
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
ms.search.validFrom: 2019-10-23
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 66419d9093cff68aa6109b22ab57bcb46ac6c718
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/06/2019
ms.locfileid: "2772893"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-october-23-2019"></a>Dynamics 365 Talent:n uudet tai muuttuneet ominaisuudet (23. lokakuuta 2019)

[!include [banner](includes/banner.md)]

Tässä ohjeaiheessa käsitellään Dynamics 365 Talentin uusia tai muuttuneita ominaisuuksia.

## <a name="changes-in-attract"></a>Attractin muutokset
Tässä julkaisussa on vähäisiä Dynamics 365 Talent: Attractin ohjelmakorjauksia.

## <a name="changes-in-onboard"></a>Onboardin muutokset
Tässä julkaisussa on vähäisiä Dynamics 365 Talent: Onboard:n ohjelmakorjauksia.

## <a name="changes-in-core-hr"></a>Core HR:n muutokset

Tässä osassa kuvatut muutokset koskevat koontiversiota 8.1.2569. Joissakin otsikoissa suluissa olevat luvut viittaavat tukinumeroihin Microsoft Dynamics Lifecycle Services (LCS) -palveluissa.

### <a name="platform-update-30-for-finance-and-operations-apps"></a>Finance and Operations -sovellusten Platform update 30

Lisätietoja on kohdassa [Finance and Operations -sovellusten Platform update 30:n uudet ja muuttuneet ominaisuudet (marraskuu 2019).](https://docs.microsoft.com/en-us/dynamics365/fin-ops-core/fin-ops/get-started/whats-new-platform-update-30)

### <a name="remove-benefits-open-enrollment-preview-feature"></a>Etuuksien avoimen haun esiversiotoiminnon poistaminen

Blogiviestissä [Strategic investments in core HR drive operational excellence](https://cloudblogs.microsoft.com/dynamics365/bdm/2019/10/02/strategic-investments-in-core-hr-drive-operational-excellence) annetun ilmoituksen myötä Microsoft poistaa etuuksien avoimen haun ominaisuuden julkisesta esiversiosta 18.10.2019. Sen korvaava toiminto julkaistaan myöhemmin. Julkisessa esiversiossa olevaa etuuksien avoimen haun toimintoa ei tueta tuotantokäytössä.

### <a name="error-while-selecting-the-countryregion-on-the-worker-form-a-second-time-350294"></a>Virhe valittaessa maata/aluetta Työntekijä-lomakkeessa toista kertaa (350294)

Tämän viikon julkaisussa ongelma on korjattu, kun **Työntekijä**-lomakkeessa valitaan maata/aluetta.

### <a name="financial-dimension-values-default-to-the-combination-display-field-when-do-not-allow-manual-entry-is-set-to-true-340097"></a>Taloushallinnon dimension arvot siirtyvät oletusarvoisesti Yhdistelmänäyttö-kenttään, kun Älä salli manuaalista määritystä -asetuksen arvo on tosi (340097)

Tämän muutoksen myötä järjestelmä siirtää dimension arvon oletusarvoisesti oikein **Yhdistelmänäyttö**-kenttään, kun taloushallinnon dimensioita määritetään ja käytetään asetusta Älä salli manuaalista määritystä.

### <a name="new-relationship-types-should-be-added-to-relationship-lookup-in-the-personal-contacts-form-347691"></a>Uusia suhdetyyppejä pitäisi lisätä henkilökohtaisten tietojen lomakkeen Suhteet-hakuun (347691).

Tämä julkaisu sisältää uusia mahdollisuuksia lisätä uusia suhdetyyppejä **Suhdetyypit**-taulukkoon ja käyttää näitä muutoksia henkilökohtaisten yhteystietojen suhdehaussa.

### <a name="additional-list-values-in-custom-fields-arent-reflected-in-common-data-service-379599"></a>Ylimääräiset luetteloarvot mukautetuissa kentissä eivät näy Common Data Servicessä (379599)

Tämän viikon julkiasun myötä uuden luetteloarvon lisääminen olemassa olevaan mukautettuun kenttään, joka on jo synkronoitu Common Data Servicen kanssa, saa nyt uudet keräysluettelon arvot näkyviin, kun muutokset on otettu käyttöön yksikössä.

### <a name="on-the-terms-of-employment-page-all-employees-terms-of-employment-appear-after-selecting-open-in-excel-348073"></a>Kaikkien työntekijöiden työehdot tulevat näkyviin Työehdot-sivulla, kun valitaan Avaa Excelissä (348073).

Tämän julkaisun myötä Excelissä avautuvat vain valittujen työntekijöiden työehdot. Myös kaikki yrityksen tietoturva on otettu huomioon.

### <a name="the-association-between-the-work-calendar-holiday-entity-and-the-work-calendar-entity-is-missing-in-common-data-service-324178"></a>Työkalenterin lomayksikön ja työkalenteriyksikön välinen liitos puuttuu Common Data Servicessä (324178)

Suhde on lisätty tässä julkaisussa. Tämä muutos mahdollistaa työntekijän työpäivien esittämisen PowerAppsissa. 

### <a name="error-when-using-employee-self-service-workflows-with-configurable-hierarchies-370132"></a>Virhe käytettäessä työntekijän itsepalvelutyönkulkuja yhdessä määritettävien hierarkioiden kanssa (370132)

Tässä julkaisussa on käytettävissä parempia ohjeita työnkulkujen määrittämiseen määritettävien hierarkioiden avulla. 

### <a name="system-allows-creation-of-new-positions-where-the-available-for-assignment-date-is-earlier-than-the-activation-date-340103"></a>Järjestelmä sallii uusien toimien luomisen, kun Käytettävissä toimeksiantoa varten -päivämäärä on Aktivointi-päivämäärää aikaisemmin (340103)

Tämä muutos saa näkyviin varoituksen, kun **Käytettävissä toimeksiantoa varten** -päivämäärä on ennen toimen **Aktivointi**-päivämäärää.

## <a name="coming-soon"></a>Tulossa pian

### <a name="print-performance-reviews"></a>Kehityskeskustelujen tulostaminen

Katso lisätietoja Dynamics 365: vuoden 2019 julkaisuaallon 2 suunnitelman kohdasta [Kehityskeskustelujen tulostaminen](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-talent/print-performance-reviews).

### <a name="feature-management-workspace"></a>Ominaisuushallinnan työtila

Ominaisuudet lisätään ja päivitetään jokaisessa versiossa. Toiminnon hallintakokemus tarjoaa työtilan, jossa voit tarkastella kussakin julkaisussa toimitettujen toimintojen luetteloa. Uudet asetukset ovat oletusarvoisesti poissa käytöstä. Työtilan avulla voit ottaa ne käyttöön ja tarkastella niiden dokumentaatiota.

Lisätietoja tulevista toimintojen hallinnan muutoksista löytyy [Toimintojen hallinnan yleiskuvauksesta](https://docs.microsoft.com/en-us/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview).
