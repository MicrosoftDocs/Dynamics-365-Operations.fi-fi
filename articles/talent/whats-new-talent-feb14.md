---
title: Dynamics 365 for Talentin uudet tai muuttuneet ominaisuudet (14. helmikuuta 2019)
description: Tässä ohjeaiheessa käsitellään Microsoft Dynamics 365 for Talentin uusia tai muuttuneita ominaisuuksia.
author: Darinkramer
manager: AnnBe
ms.date: 02/14/2019
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
ms.search.validFrom: 2019-02-14
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 1db7d032eade3f996e0554e64d6ea0704a347ed8
ms.sourcegitcommit: 608e68b603afef9eb98d8fb25e90109c2473ef87
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/19/2019
ms.locfileid: "859387"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-february-14-2019"></a>Dynamics 365 for Talentin uudet tai muuttuneet ominaisuudet (14. helmikuuta 2019)

[!include [banner](includes/banner.md)]

Tässä ohjeaiheessa käsitellään Talentin uusia tai muuttuneita ominaisuuksia.

## <a name="changes-in-attract"></a>Attractin muutokset
Tässä julkaisussa on vähäisiä ohjelmakorjauksia.

## <a name="changes-in-onboarding"></a>Onboardingin muutokset
Tässä julkaisussa on vähäisiä ohjelmakorjauksia.
 
## <a name="changes-in-core-hr"></a>Core HR:n muutokset 
**Koontiversio 8.1.2146**

### <a name="employee-fixed-compensation-entity-doesnt-export-all-records"></a>Työntekijän kiinteä kompensaatio -yksikkö ei vie kaikkia tietueita
Tämän muutoksen ansiosta **Työntekijän kiinteä kompensaatio** -yksikkö vie nyt kaikki tietueet. Yksikön avulla voidaan luoda ja päivittää aiemmin luodut työntekijöiden kiinteän kompensaation tietueet. 

### <a name="employment-end-date-doesnt-honor-employee-preferred-time-zone-settings"></a>Työsuhteen päättymispäivä ei noudata työntekijän ensisijaisen aikavyöhykkeen asetuksia
Työsuhteen päättymispäivät noudattavat nyt käyttäjän ensisijaista aikavyöhykettä, kun työsuhde yrityksessä luodaan tai se päättyy.
 
### <a name="uk-addresses-display-in-analytics-as-eastern-switzerland-addresses"></a>Brittiläiset osoitteet näkyvät analytiikassa itäsveitsiläisinä osoitteina.
Tässä julkaisussa on tehty muutos, joka korjaa **henkilöstöhallinnon** sijaintikohtaisen henkilömääräraportin osoitteiden virheellisen kohdistuksen.
 
### <a name="termination-code-is-not-populated-on-the-worker-position-assignment-record-when-ending-the-position"></a>Työsuhteen päättymiskoodia ei täytetä työntekijän toimen määritystietueessa toimea päätettäessä
Irtisanomisen syy -oletuskoodiin on tehty muutos, kun sitä käytetään työtekijän toimimäärityksen päättämiseen.

### <a name="new-entity-created-for-job-compensation-levels"></a>Työn kompensaatiotasojen uuden yksikön luonti
Luotiin uusi Data Management Framework (DMF). Yksikkö mahdollistaa kunkin järjestelmässä määritetyn työn kompensaatiotasojen, markkina-arvojen ja kyselytietojen luonnin ja päivittämisen.
