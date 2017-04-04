---
title: "Työnkulun elementit"
description: "Tässä artikkelissa kuvataan eri osia, jotka muodostavat työnkulun."
author: sericks007
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User, IT Pro
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 56441
ms.assetid: de740262-6ffd-42b9-a325-540eae5cec94
ms.search.region: Global
ms.author: tjvass
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: ee20b567b402bf638a54f6394159f7f8a9f02da6
ms.lasthandoff: 03/31/2017


---

# <a name="workflow-elements"></a>Työnkulun elementit

Tässä artikkelissa kuvataan eri osia, jotka muodostavat työnkulun.

Työnkulku koostuu elementeistä. Seuraavissa osissa kuvataan kutakin elementtityyppiä.

## <a name="tasks"></a>Tehtävät
*Tehtävä* on työyksikkö, joka on suoritettava. Työnkulkuun voidaan lisätä kahdentyyppisiä tehtäviä: manuaalisia ja automaattisia.

### <a name="manual-task"></a>Manuaalinen tehtävä

*Manuaalinen tehtävä* on työyksikkö, joka käyttäjän on suoritettava. Esimerkiksi kuluraporttityönkulussa voi olla manuaalisia tehtäviä, joille määritettyjen käyttäjien on tehtävä seuraavia toimenpiteitä:

-   Tarkistaa vastaanotot, jotka lähetetään kuluraportin kanssa.
-   Ottaa yhteyttä esimieheen.

### <a name="automated-task"></a>Automaattinen tehtävä

*Automaattinen tehtävä* on työyksikkö, jonka järjestelmä suorittaa. Käyttäjän toimia ei tarvita. Esimerkiksi myyntitilaustyönkulussa voi olla automaattisia tehtäviä, joille järjestelmän on tehtävä seuraavia toimenpiteitä:

-   Suorittaa luottorajan tarkistus.
-   Luoda asiakastietue asiakkaalle, jos tietuetta ei vielä ole.

## <a name="approval-processes"></a>Hyväksyntäprosessit
*Hyväksyntäprosessi* koostuu erilaisista vaiheista. Hyväksyntäprosessin eri vaiheissa käyttäjä voi tehdä seuraavat toimet:

-   Tiedoston hyväksyminen.
-   Tiedoston hylkääminen.
-   Muutospyyntö.
-   Tiedoston siirtäminen toisen käyttäjän hyväksyttäväksi.

## <a name="lineitem-workflow-elements"></a>Työnkulun elementtien Lineitem
Työnkulku voidaan luoda käsittelemään tiedostoja tai sen rivinimikkeitä. Oletetaan esimerkiksi, että olet luonut aikaraporttien hyväksymistyönkulun. (Olemme viittaavat tämän työnkulun *asiakirjan työnkulun*.) Voit lisätä *rivinimikkeen työnkulun* asiakirjan työnkulun elementti. Rivinimikkeen elementtiä suoritettaessa kukin asiakirjan rivinimike lähetetään käsiteltäväksi. Voit määrittää, käsitteleekö sama rivinimikkeiden työnkulku kaikki rivinimikkeet, tai määrittää rivinimikkeille omat rivinimikkeen työnkulut. Oletetaan, että työntekijä on lähettänyt aikaraportin, joka muistuttaa seuraavaa kuvaa. ![Workflow with line items](./media/workflow_lineitemworkflow.gif) Tässä skenaariossa voit luoda seuraavat rivinimikkeiden työkulut:

-   **Rivinimikkeen työnkulku 1** – Työnkulkua käytetään projektitunnuksella 1111 varustettujen rivinimikkeiden käsittelemiseen.
-   **Rivinimikkeen työnkulku 2** – Työnkulkua käytetään projektitunnuksella 2222 varustettujen rivinimikkeiden käsittelemiseen.
-   **Rivinimikkeen työnkulku 3** – Työnkulkua käytetään projektitunnuksella 3333 varustettujen rivinimikkeiden käsittelemiseen.

## <a name="flowcontrol-elements"></a>FlowControl-elementit
Seuraavien elementtien avulla voit suunnitella työnkulkuja, joissa on vaihtoehtoisia tai samanaikaisesti suoritettavia haaroja.

### <a name="manual-decision"></a>Manuaalinen päätös

*Manuaalinen päätös* on piste, jossa työnkulku jakautuu kahteen haaraan. Käyttäjän on tehtävä päätös, joka määrittää, kumpaa haaraa käytetään lähetetyn asiakirjan käsittelyyn.

### <a name="conditional-decision"></a>Ehdollinen päätös

Myös *ehdollinen päätös* on piste, jossa työnkulku jakautuu kahteen haaraan. Järjestelmä kuitenkin määrittää, kumpaa haaraa käytetään lähetetyn asiakirjan käsittelyyn. Järjestelmä tekee päätöksen arvioimalla asiakirjaa ja määrittämällä, täyttääkö se tietyt ehdot.

### <a name="parallel-activity"></a>Rinnakkainen tehtävä

*Rinnakkainen tehtävä* on työnkulun elementti, joka sisältää vähintään kaksi työnkulun haaraa, jotka ovat käynnissä yhtä aikaa.

### <a name="subworkflow"></a>Alityönkulku

*Alityönkulku* suoritetaan toisen työnkulun yhteydessä.


