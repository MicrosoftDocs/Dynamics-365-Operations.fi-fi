---
title: Dynamics 365 Talentin uudet tai muuttuneet ominaisuudet (31. tammikuuta 2019)
description: Tässä ohjeaiheessa kerrotaan Microsoft Dynamics 365 Talentin uusista tai muuttuneista ominaisuuksista.
author: andreabichsel
manager: AnnBe
ms.date: 01/31/2019
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
ms.author: anbichse
ms.search.validFrom: 2019-01-29
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 8e8c11e460a4678efea81f8d3d1eec96b673d329
ms.sourcegitcommit: 53174ed4e7cc4e1ba07cdfc39207e7296ef87c1f
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/07/2020
ms.locfileid: "4690049"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-january-31-2019"></a>Dynamics 365 Talentin uudet tai muuttuneet ominaisuudet (31. tammikuuta 2019)

Tässä ohjeaiheessa käsitellään Dynamics 365 Talentin uusia tai muuttuneita ominaisuuksia.

**Koontiversio 8.1.2128**

## <a name="core-hr-changes"></a>Core HR:n muutokset

### <a name="time-off-taken-on-leave-people-card-doesnt-consider-leave-plan-dates"></a>Käytetty poissaolo lomalla olevan kortissa ei ota huomioon lomasuunnitelman päivämääriä
**Otettu**-kortti näyttää nyt suunnitelman määrittämänä lomavuonna käytetyt poissaolot, joiden lomasuunnitelmat eivät ole kalenterivuoden mukaisia. Jos organisaation lomavuosi on esimerkiksi 1.6.–30.5. ja työntekijä on ollut poissa kolme päivää joulukuussa, 15.1. **Otettu**-kortissa näkyy 3 päivää. 

### <a name="accrual-amounts-not-matching-tier-date-basis"></a>Jaksotussummat eivät vastaa tasopäivämääräperustetta
Lomiin ja poissaoloihin on lisätty uusia asetuksia (**Henkilöstöhallinto**-parametrit), joiden avulla asiakkaat voivat määrittää, milloin työntekijöiden työkuukausipäivämäärät ovat voimassa. Joissakin organisaatioissa päivämäärä on kuukauden lopussa, kun taas toisessa se voi olla kuukauden alussa. Yksi organisaatio voi esimerkiksi myöntää poissaolon 31.12., kun taas toisen tekee sen 1.1. Tällä asetuksella voi valita, milloin myöntämisen tapahtuu. 

### <a name="worker-hire-actions-are-stuck-in-workflow-complete-state"></a>Työntekijän työhönottotoiminnot ovat juuttuneet Työnkulku valmis -tilaan
Tehdyillä muutoksilla on korjattu ongelma, jossa pieni määrä työnkulkuja päättyi Työnkulku valmis -tilaan. Uusien työnkulkujen pitäisi nyt siirtyä Valmis- tilaan, kun työnkulku päättyy. Jos työnkulku on Työnkulku valmis -tilassa, se siirretään virhetilaan, jotta se voidaan tarvittaessa päivittää tai poistaa. 
