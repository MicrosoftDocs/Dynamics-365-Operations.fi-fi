---
title: "Työnkulun luominen"
description: "Tässä ohjeaiheessa kerrotaan, miten voit luoda työnkulun."
author: sericks007
manager: AnnBe
ms.date: 11/03/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: WorkflowSelectTemplateRnr, WorkflowTableListPageRnr
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 195583
ms.assetid: 836ddd01-cc34-45c3-a4b0-20647357dbc6
ms.search.region: Global
ms.author: donaldc
ms.search.validFrom: 2016-08-30
ms.dyn365.ops.version: Platform update 2
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: ee3f60575d0eaaf56ce08adb1936728a76488dac
ms.contentlocale: fi-fi
ms.lasthandoff: 11/03/2017

---

# <a name="create-a-workflow"></a>Työnkulun luominen

[!include[banner](../includes/banner.md)]


Tässä ohjeaiheessa kerrotaan, miten voit luoda työnkulun.

<a name="open-the-workflow-editor"></a>Avaa työnkulkueditori
------------------------

Käyttämäsi Microsoft Dynamics 365 for Finance and Operationsin moduuli määrittää, mitä työnkulun tyyppejä voi luoda. Valitse näiden ohjeiden avulla työnkulkutyyppi työnkulkueditorin luomiseksi ja avaamiseksi.

1.  Avaa moduuli, jolle haluat luoda uuden työnkulun. Esimerkiksi luoda työnkulun ostoehdotukselle valitsemalla **hankinta**.
2.  Valitse **Asetukset** &gt; **\[moduulin nimi\] työnkulut**.
3.  Luettelosivun, joka näkyy toimintoruudussa valitse **uusi**.
4.  Valitse **luoda työnkulun** -sivu, ja valitse sitten työnkulun tyyppi ja valitse **luoda työnkulun**. Työnkulkueditori tulee näyttöön Seuraavan menetelmän avulla voit rakentaa työnkulun.

## <a name="drag-workflow-elements-onto-the-canvas"></a>Vedä työnkulun elementit alustalle.
**Työnkulun elementit** -alue sisältää osia, jotka voidaan lisätä työnkulkuun. Lisää työnkulun elementit, vedä ne alustalle.

## <a name="connect-the-elements"></a>Yhdistä elementit
Voit yhdistää yhden työnkulkuelementin toiseen pitämällä osoitinta elementin päällä, kunnes yhteyspisteet avautuvat näkyville. Napsauta yhteyspistettä ja vedä se toiseen elementtiin. Varmista, että liität kaikki osat.

## <a name="configure-the-properties-of-the-workflow"></a>Työnkulun ominaisuuksien konfiguroiminen
Seuraavien ohjeiden avulla voit määrittää työnkulkuprosessin ominaisuudet.

1.  Valitse alusta varmistaaksesi, että työnkulun elementtiä ei ole valittuna.
2.  Napsauta **Ominaisuudet** avataksesi **Ominaisuudet**-lomakkeen työnkululle.
3.  Noudata ohjeiden ohjeaiheessa [Työnkulun ominaisuuksien konfiguroiminen](configure-workflow-properties.md).

## <a name="configure-the-elements-of-the-workflow"></a>Työnkulun elementtien konfiguroiminen
Määritä jokainen elementti, jonka vedit alustaan. Lisätietoja kunkin työnkulkuelementin muokkaamisesta on seuraavissa ohjeaiheissa.

-   [Manuaalisen tehtävän konfiguroiminen](configure-manual-task-workflow.md)
-   [Automaattisen tehtävän määrittäminen](configure-automated-task-workflow.md)
-   [Hyväksyntäprosessin konfiguroiminen](configure-approval-process-workflow.md)
-   [Hyväksyntävaiheen asetusten määrittäminen](configure-approval-step-workflow.md)
-   [Manuaalisen päätöksen asetusten määrittäminen](configure-manual-decision-workflow.md)
-   [Ehdollisen päätöksen asetusten määrittäminen](configure-conditional-decision-workflow.md)
-   [Rinnakkaisen tehtävän asetusten määrittäminen](configure-parallel-activity-workflow.md)
-   [Määritä rinnakkaishaara](configure-parallel-branch-workflow.md)
-   [Määritä rivinimikkeen työnkulku](configure-line-item-workflow.md)

## <a name="resolve-any-errors-or-warnings"></a>Korjaa mahdolliset virheet ja varoitukset
Työnkulkueditorin alaosassa oleva **Virheet ja varoitukset** -ruutu näyttää työnkululle luodut sanomat. Jos haluat paikallistaa elementin, jossa on tapahtunut virhe tai varoitus, kaksoisnapsauta virhe- tai varoitussanomaa. Kaikki virheet ja varoitukset on ratkaistava, ennen kuin työnkulun voi aktivoida.

## <a name="save-and-activate-the-workflow"></a>Työnkulun tallennus ja aktivoiminen
Kun olet valmis tallentamaan ja aktivoimaan työnkulun, noudata seuraavia ohjeita.

1.  Valitse **Tallenna ja sulje** sulkeaksesi työnkulkueditori ja avaa **Tallenna työnkulku** -sivu.
2.  Kirjoita kommentit työnkulkuun tekemistäsi muutoksista ja napsauta **OK**.
3.  Jos kaikki virheet ja varoitukset on ratkaistu, **työnkulun aktivoiminen** -sivu tulee näkyviin. Valitse jompikumpi seuraavista vaihtoehdoista:
    -   Voit aktivoida tämän työnkulun version valitsemalla **Ota uusi versio käyttöön**. Kun työnkulku on aktiivinen, käyttäjät voivat lähettää siihen asiakirjoja käsittelyä varten.
    -   Jos et halua aktivoida versiota napsauta **Älä ota uutta versiota käyttöön**. Voit ottaa työnkulun käyttöön myöhemmin.






