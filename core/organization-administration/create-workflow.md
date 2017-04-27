---
title: "Luo työnkulku"
description: "Tässä ohjeaiheessa kerrotaan, miten voit luoda työnkulun."
author: sericks007
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User, IT Pro
ms.search.scope: Core
ms.custom: 195583
ms.assetid: 836ddd01-cc34-45c3-a4b0-20647357dbc6
ms.search.region: Global
ms.author: donaldc
ms.search.validFrom: 2016-08-30
ms.dyn365.ops.version: Platform update 2
translationtype: Human Translation
ms.sourcegitcommit: f707d45290682e79ee439ba0d504852429defa90
ms.openlocfilehash: 1255cf90498f1968568dd2fa5a1377d989f40182
ms.lasthandoff: 03/31/2017


---

# <a name="create-a-workflow"></a>Luo työnkulku

[!include[banner](../includes/banner.md)]


Tässä ohjeaiheessa kerrotaan, miten voit luoda työnkulun.

<a name="open-the-workflow-editor"></a>Avaa työnkulkueditori
------------------------

Microsoft Dynamics 365 for Operations -moduuli, jolla työskentelet, määrittää työnkulun tyypit, joita voit luoda. Valitse näiden ohjeiden avulla työnkulkutyyppi työnkulkueditorin luomiseksi ja avaamiseksi.

1.  Avaa moduuli, jolle haluat luoda uuden työnkulun. Esimerkiksi luoda työnkulun ostoehdotukselle valitsemalla **hankinta**.
2.  Valitse **Asetukset** &gt; **\[moduulin nimi\] työnkulut**.
3.  Luettelosivun, joka näkyy toimintoruudussa valitse**uusi**.
4.  Valitse **luoda työnkulun** -sivu, ja valitse sitten työnkulun tyyppi ja valitse **luoda työnkulun**. Työnkulkueditori tulee näyttöön Seuraavan menetelmän avulla voit rakentaa työnkulun.

## <a name="drag-workflow-elements-onto-the-canvas"></a>Vedä työnkulun elementit alustalle.
**Työnkulun elementit** -alue sisältää osia, jotka voidaan lisätä työnkulkuun. Lisää työnkulun elementit, vedä ne alustalle.

## <a name="connect-the-elements"></a>Yhdistä elementit
Voit yhdistää yhden työnkulkuelementin toiseen pitämällä osoitinta elementin päällä, kunnes yhteyspisteet avautuvat näkyville. Napsauta yhteyspistettä ja vedä se toiseen elementtiin. Varmista, että liität kaikki osat.

## <a name="configure-the-properties-of-the-workflow"></a>Työnkulun ominaisuuksien konfiguroiminen
Seuraavien ohjeiden avulla voit määrittää työnkulkuprosessin ominaisuudet.

1.  Valitse alusta varmistaaksesi, että työnkulun elementtiä ei ole valittuna.
2.  Napsauta **Ominaisuudet**avataksesi**Ominaisuudet**-lomakkeen työnkululle.
3.  Noudata ohjeiden ohjeaiheessa [Työnkulun ominaisuuksien konfiguroiminen](configure-workflow-properties.md).

## <a name="configure-the-elements-of-the-workflow"></a>Työnkulun elementtien konfiguroiminen
Määritä jokainen elementti, jonka vedit alustaan. Lisätietoja kunkin työnkulkuelementin muokkaamisesta on seuraavissa ohjeaiheissa.

-   [Manuaalisen tehtävän konfiguroiminen](configure-manual-task-workflow.md)
-   [Automaattisen tehtävän määrittäminen](configure-automated-task-workflow.md)
-   [Hyväksyntäprosessin konfiguroiminen](configure-approval-process-workflow.md)
-   [Hyväksyntävaiheen konfiguroiminen](configure-approval-step-workflow.md)
-   [Manuaalisen päätöksen konfiguroiminen](configure-manual-decision-workflow.md)
-   [Ehdollisen päätöksen konfiguroiminen](configure-conditional-decision-workflow.md)
-   [Määritä rinnakkainen tehtävä](configure-parallel-activity-workflow.md)
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






