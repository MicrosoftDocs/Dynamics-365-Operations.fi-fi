---
title: Työnkulun elementit
description: Tässä ohjeaiheessa kuvataan eri osia, jotka muodostavat työnkulun.
author: ChrisGarty
manager: AnnBe
ms.date: 11/03/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 56441
ms.assetid: de740262-6ffd-42b9-a325-540eae5cec94
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ce4b0c3ee996dfbf0904f8e7fd3b3bfb53a149c2
ms.sourcegitcommit: e55efd2f62bf60f678108c09ad4701a76b20cc68
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/17/2020
ms.locfileid: "3698044"
---
# <a name="workflow-elements"></a>Työnkulun elementit

[!include [banner](../includes/banner.md)]

Tässä ohjeaiheessa kuvataan eri osia, jotka muodostavat työnkulun.

Työnkulku koostuu elementeistä. Seuraavissa osissa kuvataan kutakin elementtityyppiä.

## <a name="tasks"></a>Tehtävät

*Tehtävä* on työyksikkö, joka on suoritettava. Työnkulkuun voidaan lisätä kahdentyyppisiä tehtäviä: manuaalisia ja automaattisia.

### <a name="manual-task"></a>Manuaalinen tehtävä

*Manuaalinen tehtävä* on työyksikkö, joka käyttäjän on suoritettava. Esimerkiksi kuluraporttityönkulussa voi olla manuaalisia tehtäviä, joille määritettyjen käyttäjien on tehtävä seuraavia toimenpiteitä:

- Tarkistaa vastaanotot, jotka lähetetään kuluraportin kanssa.
- Ottaa yhteyttä esimieheen.

### <a name="automated-task"></a>Automaattinen tehtävä

*Automaattinen tehtävä* on työyksikkö, jonka järjestelmä suorittaa. Käyttäjän toimia ei tarvita. Esimerkiksi myyntitilaustyönkulussa voi olla automaattisia tehtäviä, joille järjestelmän on tehtävä seuraavia toimenpiteitä:

- Suorittaa luottorajan tarkistus.
- Luoda asiakastietue asiakkaalle, jos tietuetta ei vielä ole.

## <a name="approval-processes"></a>Hyväksyntäprosessit

*Hyväksyntäprosessi* koostuu erilaisista vaiheista. Hyväksyntäprosessin eri vaiheissa käyttäjä voi tehdä seuraavat toimet:

- Tiedoston hyväksyminen.
- Tiedoston hylkääminen.
- Muutospyyntö.
- Tiedoston siirtäminen toisen käyttäjän hyväksyttäväksi.

## <a name="line-item-workflow-elements"></a>Rivinimikkeen työnkulun elementit:

Työnkulku voidaan luoda käsittelemään tiedostoja tai sen rivinimikkeitä. Oletetaan esimerkiksi, että olet luonut aikaraporttien hyväksymistyönkulun. (Siihen viitataan *asiakirjan työnkulkuna*.) Voit lisätä *rivinimikkeen työnkulun* elementin kyseiseen asiakirjan työnkulkuun. Rivinimikkeen elementtiä suoritettaessa kukin asiakirjan rivinimike lähetetään käsiteltäväksi. Voit määrittää, käsitteleekö sama rivinimikkeiden työnkulku kaikki rivinimikkeet, tai määrittää rivinimikkeille omat rivinimikkeen työnkulut. Oletetaan, että työntekijä on lähettänyt aikaraportin, joka muistuttaa seuraavaa kuvaa.

![Työnkulut rivinimikkeillä](./media/workflow_lineitemworkflow.gif)

Tässä skenaariossa voit luoda seuraavat rivinimikkeen työnkulut:

- **Rivinimikkeen työnkulku 1** – Työnkulkua käytetään projektitunnuksella 1111 varustettujen rivinimikkeiden käsittelemiseen.
- **Rivinimikkeen työnkulku 2** – Työnkulkua käytetään projektitunnuksella 2222 varustettujen rivinimikkeiden käsittelemiseen.
- **Rivinimikkeen työnkulku 3** – Työnkulkua käytetään projektitunnuksella 3333 varustettujen rivinimikkeiden käsittelemiseen.

## <a name="flow-control-elements"></a>Työnkulun ohjauksen elementit

Seuraavien elementtien avulla voit suunnitella työnkulkuja, joissa on vaihtoehtoisia tai samanaikaisesti suoritettavia haaroja.

### <a name="manual-decision"></a>Manuaalinen päätös

*Manuaalinen päätös* on piste, jossa työnkulku jakautuu kahteen haaraan. Käyttäjän on tehtävä päätös, joka määrittää, kumpaa haaraa käytetään lähetetyn asiakirjan käsittelyyn.

### <a name="conditional-decision"></a>Ehdollinen päätös

Myös *ehdollinen päätös* on piste, jossa työnkulku jakautuu kahteen haaraan. Järjestelmä kuitenkin määrittää, kumpaa haaraa käytetään lähetetyn asiakirjan käsittelyyn. Järjestelmä tekee päätöksen arvioimalla asiakirjaa ja määrittämällä, täyttääkö se tietyt ehdot.

### <a name="parallel-activity"></a>Rinnakkainen tehtävä

*Rinnakkainen tehtävä* on työnkulun elementti, joka sisältää vähintään kaksi työnkulun haaraa, jotka ovat käynnissä yhtä aikaa.

### <a name="subworkflow"></a>Alityönkulku

*Alityönkulku* suoritetaan toisen työnkulun yhteydessä.
