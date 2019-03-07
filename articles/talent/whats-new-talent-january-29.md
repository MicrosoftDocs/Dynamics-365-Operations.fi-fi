---
title: Dynamics 365 for Talentin uudet tai muuttuneet ominaisuudet (31. tammikuuta 2019)
description: Tässä ohjeaiheessa käsitellään Microsoft Dynamics 365 for Talentin uusia tai muuttuneita ominaisuuksia.
author: Darinkramer
manager: AnnBe
ms.date: 1/31/2019
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
ms.search.validFrom: 2019-01-29
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 5c9449e2bdec8c17cc2cf659ed68ac1d713a26ad
ms.sourcegitcommit: 1e32d78868098fd76124bb41363f15c4ec3ea15a
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/05/2019
ms.locfileid: "374731"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-january-31-2019"></a>Dynamics 365 for Talentin uudet tai muuttuneet ominaisuudet (31. tammikuuta 2019)

[!include [banner](includes/banner.md)]

Tässä ohjeaiheessa käsitellään Dynamics 365 for Talentin uusia tai muuttuneita ominaisuuksia

**Koontiversio 8.1.2128**

## <a name="core-hr-changes"></a>Core HR:n muutokset

### <a name="time-off-taken-on-leave-people-card-doesnt-consider-leave-plan-dates"></a>Käytetty poissaolo lomalla olevan kortissa ei ota huomioon lomasuunnitelman päivämääriä
Niiden henkilöiden **Otettu**-kortti näyttää nyt suunnitelman määrittämänä lomavuonna käytetyt poissaolot, joiden lomasuunnitelmat eivät ole kalenterivuoden mukaisia. Jos organisaation lomavuosi on esimerkiksi 1.6.–30.5. ja työntekijä on ollut poissa kolme päivää joulukuussa, 15.1. **Otettu**-kortissa näkyy 3 päivää. 

### <a name="accrual-amounts-not-matching-tier-date-basis"></a>Jaksotussummat eivät vastaa tasopäivämääräperustetta
Lomiin ja poissaoloihin on lisätty uusia asetuksia (**Henkilöstöhallinto**-parametrit), joiden avulla asiakkaat voivat määrittää, milloin työntekijöiden työkuukausipäivämäärät ovat voimassa. Joissakin organisaatioissa päivämäärä on kuukauden lopussa, kun taas toisessa se voi olla kuukauden alussa. Yksi organisaatio voi esimerkiksi myöntää poissaolon 31.12., kun taas toisen tekee sen 1.1. Tällä asetuksella voi valita, milloin myöntämisen tapahtuu. 

### <a name="worker-hire-actions-are-stuck-in-workflow-complete-state"></a>Työntekijän työhönottotoiminnot ovat juuttuneet Työnkulku valmis -tilaan
Tehdyillä muutoksilla on korjattu ongelma, jossa pieni määrä työnkulkuja päättyi Työnkulku valmis -tilaan. Uusien työnkulkujen pitäisi nyt siirtyä Valmis- tilaan, kun työnkulku päättyy. Jos työnkulku on Työnkulku valmis -tilassa, se siirretään virhetilaan, jotta se voidaan tarvittaessa päivittää tai poistaa. 
