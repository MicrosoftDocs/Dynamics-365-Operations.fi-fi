---
title: Dynamics 365 Talentin uudet tai muuttuneet ominaisuudet (14. helmikuuta 2019)
description: Tässä ohjeaiheessa käsitellään Microsoft Dynamics 365 Talentin uusia tai muuttuneita ominaisuuksia.
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
ms.openlocfilehash: 32f3bab38233833498ed566fa1558a023b3bc0dd
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/13/2020
ms.locfileid: "4461053"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-february-14-2019"></a>Dynamics 365 Talentin uudet tai muuttuneet ominaisuudet (14. helmikuuta 2019)

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
