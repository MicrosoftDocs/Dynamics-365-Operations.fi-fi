---
title: Dynamics 365 Talent:n uudet tai muuttuneet ominaisuudet (29. lokakuuta 2019)
description: Tässä ohjeaiheessa käsitellään Microsoft Dynamics 365 Talentin uusia tai muuttuneita ominaisuuksia.
author: Darinkramer
manager: AnnBe
ms.date: 10/29/2019
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
ms.search.validFrom: 2019-10-29
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 09d53c82b4244f20d0d7f301691b01263258a32f
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/17/2020
ms.locfileid: "4529681"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-october-29-2019"></a>Dynamics 365 Talent:n uudet tai muuttuneet ominaisuudet (29. lokakuuta 2019)

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Tässä ohjeaiheessa käsitellään Dynamics 365 Talentin uusia tai muuttuneita ominaisuuksia.

## <a name="changes-in-attract"></a>Attractin muutokset

Tässä julkaisussa on vähäisiä Dynamics 365 Talent: Attractin ohjelmakorjauksia.

## <a name="changes-in-onboard"></a>Onboardin muutokset

Tässä julkaisussa on vähäisiä Dynamics 365 Talent: Onboard:n ohjelmakorjauksia.

## <a name="changes-in-core-hr"></a>Core HR:n muutokset

Tässä osassa kuvatut muutokset koskevat koontiversiota 8.1.2586. Joissakin otsikoissa suluissa olevat luvut viittaavat tukinumeroihin Microsoft Dynamics Lifecycle Services (LCS) -palveluissa.

### <a name="delete-parties-with-no-roles-should-be-on-by-default-371233"></a>Roolittomien osapuolien poistamisen pitäisi olla oletusarvoisesti käytössä (371233)

Kun valmistelet uuden ympäristön Talentissa, **Poista osapuolet, jos roolia ei ole** on otettu oletusarvoisesti käyttöön. Kun poistat työntekijän, työntekijään liitettyä osapuolta ei poisteta ellei tätä asetusta ole otettu käyttöön. Tämä muutos rajoittaa yleisen osoitekirjan tietueiden kaksoiskappaleita, kun työntekijöitä on tuotava, muutettava tai tuotava uudelleen.

### <a name="draft-and-cancelled-leave-requests-should-be-allowed-to-be-deleted-in-common-data-service-376999"></a>Lomapyyntöjen luonnosten ja peruutettujen lomapyyntöjen poistaminen Common Data Servicessa on sallittava (376999)

Tämän muutoksen myötä voi nyt poistaa lomapyyntöjä, joiden tila Common Data Servicessa on **Luonnos** tai **Peruutettu**.

### <a name="additional-list-values-in-custom-fields-arent-reflected-in-common-data-service-after-clicking-apply-on-the-custom-fields-form-379599"></a>Mukautettujen kenttien luettelon lisäarvot eivät heijastu Common Data Serviceen, kun Mukautetut kentät -lomakkeessa valitaan Käytä (379599)

Kun lisäät uusia luetteloarvoja aiemmin luotuun mukautettuun kenttään, joka on jo synkronoitu Common Data Servicessa, ne ovat nyt käytettävissä Common Data Servicessa sen jälkeen, kun käytät muutoksia **Mukautetut kentät** -lomakkeessa.

### <a name="apply-onboarding-checklists-across-legal-entities-when-more-than-one-employment-exists-371270"></a>Perehdytyksen tarkistusluetteloiden käyttäminen yrityksissä, kun työsuhteita on useampi kuin yksi (371270)

Tämän viikon julkaisussa voit käyttää tarkistusluetteloita työntekijöillä, joilla on useampi kuin yks työsuhde kohdassa **Työntekijä-lomake > Tarkistusluettelot**.

### <a name="benefits-open-enrollment-preview-feature-has-been-removed"></a>Etuuksien avoimen haun esiversiotoiminto on poistettu

Blogikirjoituksessa [Core HR:ään tehdyt strategiset sijoitukset edistävät operatiivista suorituskykyä](https://cloudblogs.microsoft.com/dynamics365/bdm/2019/10/02/strategic-investments-in-core-hr-drive-operational-excellence) annetun ilmoituksen myötä Microsoft on poistanut etuuksien avoimen haun ominaisuuden julkisesta esiversiosta. Uusi toiminto julkaistaan myöhemmin. Etuuksien avoimen haun toiminnon tuotantokäyttöä ei tueta.

## <a name="coming-soon"></a>Tulossa pian

### <a name="print-performance-reviews"></a>Kehityskeskustelujen tulostaminen

Katso lisätietoja Dynamics 365: vuoden 2019 julkaisuaallon 2 suunnitelman kohdasta [Kehityskeskustelujen tulostaminen](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-talent/print-performance-reviews).

### <a name="feature-management-workspace"></a>Ominaisuushallinnan työtila

Ominaisuudet lisätään ja päivitetään jokaisessa versiossa. Toiminnon hallintakokemus tarjoaa työtilan, jossa voit tarkastella kussakin julkaisussa toimitettujen toimintojen luetteloa. Uudet asetukset ovat oletusarvoisesti poissa käytöstä. Työtilan avulla voit ottaa ne käyttöön ja tarkastella niiden dokumentaatiota.

Lisätietoja tulevista toimintojen hallinnan muutoksista löytyy [Toimintojen hallinnan yleiskuvauksesta](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview).


[!INCLUDE[footer-include](../includes/footer-banner.md)]