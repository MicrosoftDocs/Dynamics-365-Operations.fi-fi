---
title: Dynamics 365 Talent:n uudet tai muuttuneet ominaisuudet (10. joulukuuta 2019)
description: Tässä artikkelissa käsitellään Microsoft Dynamics 365 Talentin uusia tai muuttuneita toimintoja.
author: Darinkramer
manager: AnnBe
ms.date: 12/10/2019
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
ms.search.validFrom: 2019-12-10
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 18f86f5d87b780d5d4ffc83330d389077987dda6
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/17/2020
ms.locfileid: "4528168"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-december-10-2019"></a>Dynamics 365 Talent:n uudet tai muuttuneet ominaisuudet (10. joulukuuta 2019)

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Tässä ohjeaiheessa käsitellään Dynamics 365 Talentin uusia tai muuttuneita ominaisuuksia.

## <a name="changes-in-attract"></a>Attractin muutokset

Tässä julkaisussa on vähäisiä Dynamics 365 Talent: Attractin ohjelmakorjauksia.

## <a name="changes-in-onboard"></a>Onboardin muutokset

Tässä julkaisussa on vähäisiä Dynamics 365 Talent: Onboard:n ohjelmakorjauksia.

## <a name="changes-in-core-hr"></a>Core HR:n muutokset

Tässä osassa kuvatut muutokset koskevat koontiversiota 8.1.2660. Joissakin otsikoissa suluissa olevat luvut viittaavat tukinumeroihin Microsoft Dynamics Lifecycle Services (LCS) -palveluissa.

### <a name="feature-management-workspace"></a>Ominaisuushallinnan työtila

**Toimintojen hallinta** -työtilassa on luettelo kussakin julkaisussa toimitetuista toiminnoista. Uudet asetukset ovat oletusarvoisesti poissa käytöstä. Työtilan avulla voit ottaa ne käyttöön ja tarkastella niiden dokumentaatiota. Lisätietoja Toimintojen hallinnasta on kohdassa [Toimintojen hallinnan yleiskuvaus](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview).

Kaikki uudet toiminnot pysyvät esiversiossa ainakin 30 päivää ja yleensä 30–60 päivää. Tärkeimmät toiminnot ovat yleensä saatavana kunkin vuoden lokakuussa ja huhtikuussa esiversiojakson jälkeen. Voit ottaa uudet ominaisuudet käyttöön heti, kun näet ne **Toimintojen hallinta** -työtilassa. Jotkin toiminnot on ehkä otettu käyttöön oletusarvoisesti.
 
Joskus keskeinen toiminto on otettu käyttöön oletusarvoisesti eikä sitä voi poistaa käytöstä (esimerkiksi **Toimintojen hallinta** -työtilassa).
 
Kun toiminto on yleisesti saatavana, se voidaan ottaa käyttöön tai poistaa käytöstä tuotantoympäristöissä. **Toimintojen hallinta** -työtila ilmaisee, milloin esiversiotoiminto tulee pakolliseksi. Tämä päivämäärä on yleensä 1. lokakuuta tai 1. huhtikuuta eli ne vastaavat puolivuotisia julkaisusuunnitelmia. Pakollisia toimintoja ei voi poistaa käytöstä. Toiminnon voi ottaa käyttöön ja poistaa käytöstä kaikissa ympäristöissä siihen saakka, että muuttuu pakolliseksi.

### <a name="streamlined-worker-form-has-moved-to-the-feature-management-workspace-390583"></a>Virtaviivaistettu työntekijälomake on siirretty ominaisuuksienhallinta-työtilaan (390583)

Tämän muutoksen myötä virtaviivaistettu työntekijälomake voidaan nyt ottaa käyttöön **Ominaisuuksien hallinta** -työtilassa. Tämä ominaisuus on siirretty **Järjestelmäparametrit**-lomakkeesta **Järjestelmän hallinta**-tilassa.

### <a name="prevent-hcmworkerpayrollinfo-records-from-being-written-without-a-worker-value-394526"></a>Estä HcmWorkerPayrollInfo-tietueiden kirjoitus ilman työntekijän arvoa (394526)

Tämän julkaisun yhteydessä **HcmWorkerPayrollInfo**-tietueita ei enää luoda ilman työntekijäviittausta tässä skenaariossa. 

### <a name="message-log-associated-to-the-action-isnt-populated-when-the-action-fails-to-complete-374007"></a>Toimeen liittyvä sanomaloki ei ole täytetty, kun toiminnon suorittaminen epäonnistuu (374007)

Tämä versio sisältää muutoksen, joka täyttää toimenpideviestilokin, kun toiminto epäonnistuu tietyissä tilanteissa. 

### <a name="common-data-service-integration-batch-job-creation-388030"></a>Common Data Service -integroinnin erätyön luonti (388030)

Tällä muutolla luodaan Common Data Service -integroinnin erätyöt, kun palvelu on käytössä.

### <a name="additional-pick-list-values-to-custom-fields-arent-reflected-in-common-data-service-after-clicking-apply-on-the-custom-fields-form-379599"></a>Mukautettujen kenttien poimintaluettelon lisäarvot eivät heijastu Common Data Serviceen, kun Mukautetut kentät -lomakkeessa valitaan Käytä (379599)

Tämän muutoksen myötä Talent-kohteeseen kirjoitetut uudet poimintaluettelon arvot synkronoidaan Common Data Serviceen nyt, kun otat muutokset käyttöön.

### <a name="update-to-common-data-service-for-then-leave-bank-transaction-entity-turns-into-an-insert-on-talent-side-352938"></a>Päivitä Common Data Serviceen ja jätä pankki -tapahtuman entiteetti muuttuu lisää Talent-puolelle (352938)

Tämä muutos korjaa ongelman, jonka vuoksi lomapankkitapahtuman päivitys luo Talentissa uuden tietueen.

## <a name="in-preview"></a>Esiversiossa

Esiversiotoiminnot ovat käytettävissä vain **eritys** ympäristöissä.

### <a name="print-performance-reviews"></a>Kehityskeskustelujen tulostaminen

Katso lisätietoja Dynamics 365: vuoden 2019 julkaisuaallon 2 suunnitelman kohdasta [Kehityskeskustelujen tulostaminen](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-talent/print-performance-reviews).

