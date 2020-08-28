---
title: Työnkulkujen luonnin yleiskuvaus
description: Tässä ohjeaiheessa kerrotaan, miten voit luoda työnkulun.
author: ChrisGarty
manager: AnnBe
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WorkflowSelectTemplateRnr, WorkflowTableListPageRnr
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 195583
ms.assetid: 836ddd01-cc34-45c3-a4b0-20647357dbc6
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-08-30
ms.dyn365.ops.version: Platform update 2
ms.openlocfilehash: bcd548bf8e03e0e6df4d413afe8c9ae01c570899
ms.sourcegitcommit: e55efd2f62bf60f678108c09ad4701a76b20cc68
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/17/2020
ms.locfileid: "3698015"
---
# <a name="create-workflows-overview"></a>Työnkulkujen luonnin yleiskuvaus

[!include [banner](../includes/banner.md)]

Tässä ohjeaiheessa kerrotaan, miten voit luoda työnkulun.

## <a name="open-the-workflow-editor"></a>Avaa työnkulkueditori

Käyttämäsi moduuli määrittää työnkulun tyypit, joita voit luoda. Valitse näiden ohjeiden avulla työnkulkutyyppi työnkulkueditorin luomiseksi ja avaamiseksi.

1. Avaa moduuli, jolle haluat luoda uuden työnkulun. Esimerkiksi luoda työnkulun ostoehdotukselle valitsemalla **hankinta**.
2. Valitse **Asetukset** &gt; **\[moduulin nimi\] työnkulut**.
3. Luettelosivun, joka näkyy toimintoruudussa valitse **uusi**.
4. Valitse **luoda työnkulun** -sivu, ja valitse sitten työnkulun tyyppi ja valitse **luoda työnkulun**. Työnkulkueditori tulee näyttöön Seuraavan menetelmän avulla voit rakentaa työnkulun.

## <a name="drag-workflow-elements-onto-the-canvas"></a>Vedä työnkulun elementit alustalle.

**Työnkulun elementit** -alue sisältää osia, jotka voidaan lisätä työnkulkuun. Lisää työnkulun elementit, vedä ne alustalle.

## <a name="connect-the-elements"></a>Yhdistä elementit

Voit yhdistää yhden työnkulkuelementin toiseen pitämällä osoitinta elementin päällä, kunnes yhteyspisteet avautuvat näkyville. Napsauta yhteyspistettä ja vedä se toiseen elementtiin. Varmista, että liität kaikki osat.

## <a name="configure-the-properties-of-the-workflow"></a>Työnkulun ominaisuuksien konfiguroiminen

Seuraavien ohjeiden avulla voit määrittää työnkulkuprosessin ominaisuudet.

1. Valitse alusta varmistaaksesi, että työnkulun elementtiä ei ole valittuna.
2. Napsauta **Ominaisuudet** avataksesi **Ominaisuudet**-lomakkeen työnkululle.
3. Noudata ohjeaiheen [Työnkulun ominaisuuksien konfiguroiminen](configure-workflow-properties.md) menettelyjä.

## <a name="configure-the-elements-of-the-workflow"></a>Työnkulun elementtien konfiguroiminen

Määritä jokainen elementti, jonka vedit alustaan. Lisätietoja kunkin työnkulkuelementin muokkaamisesta on seuraavissa ohjeaiheissa.

- [Manuaalisten tehtävien konfiguroiminen työnkulkuun](configure-manual-task-workflow.md)
- [Automaattisten tehtävien määrittäminen työnkulkuun](configure-automated-task-workflow.md)
- [Hyväksyntäprosessien lisääminen työnkulkuun](configure-approval-process-workflow.md)
- [Hyväksyntävaiheiden lisääminen työnkulkuun](configure-approval-step-workflow.md)
- [Manuaalisten päätösten konfiguroiminen työnkulkuun](configure-manual-decision-workflow.md)
- [Ehdollisten päätösten konfiguroiminen työnkulkuun](configure-conditional-decision-workflow.md)
- [Määritä rinnakkaiset haarat työnkulussa](configure-parallel-activity-workflow.md)
- [Rinnakkaishaaran asetusten määrittäminen](configure-parallel-branch-workflow.md)
- [Rivinimikkeen työnkulkujen määrittäminen](configure-line-item-workflow.md)

## <a name="resolve-any-errors-or-warnings"></a>Korjaa mahdolliset virheet ja varoitukset

Työnkulkueditorin alaosassa oleva **Virheet ja varoitukset** -ruutu näyttää työnkululle luodut sanomat. Jos haluat paikallistaa elementin, jossa on tapahtunut virhe tai varoitus, kaksoisnapsauta virhe- tai varoitussanomaa. Kaikki virheet ja varoitukset on ratkaistava, ennen kuin työnkulun voi aktivoida.

## <a name="save-and-activate-the-workflow"></a>Työnkulun tallennus ja aktivoiminen

Kun olet valmis tallentamaan ja aktivoimaan työnkulun, noudata seuraavia ohjeita.

1. Valitse **Tallenna ja sulje** sulkeaksesi työnkulkueditori ja avaa **Tallenna työnkulku** -sivu.
2. Kirjoita kommentit työnkulkuun tekemistäsi muutoksista ja napsauta **OK**.
3. Jos kaikki virheet ja varoitukset on ratkaistu, **työnkulun aktivoiminen** -sivu tulee näkyviin. Valitse jompikumpi seuraavista vaihtoehdoista:

    - Voit aktivoida tämän työnkulun version valitsemalla **Ota uusi versio käyttöön**. Kun työnkulku on aktiivinen, käyttäjät voivat lähettää siihen asiakirjoja käsittelyä varten.
    - Jos et halua aktivoida versiota napsauta **Älä ota uutta versiota käyttöön**. Voit ottaa työnkulun käyttöön myöhemmin.
