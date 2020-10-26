---
title: Variaation määrittäminen ja kokeen päättäminen
description: Tässä ohjeaiheessa käsitellään onnistuneen variaation korottamista ja kokeen päättämistä Dynamics 365 Commercessa.
author: sushma-rao
manager: AnnBe
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: sushmar
ms.search.validFrom: 2020-09-30
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: 2e011f10e908d6a2efe2e928fc5e0abc7659cb8b
ms.sourcegitcommit: b6ab46f6e5ce60e2c3d70a348827eaf60c84cae2
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/01/2020
ms.locfileid: "3930184"
---
# <a name="promote-a-variation-and-complete-an-experiment"></a>Variaation määrittäminen ja kokeen päättäminen

Tässä ohjeaiheessa käsitellään kokeessa parhaan tuloksen tuottaneen variaation korottamista ja kokeen päättämistä. Seuraavassa kaaviossa on kaikki vaiheet, jotka sisältyvät kokeen määrittämiseen ja suorittamiseen sähköisessä kaupankäyntisivustossa Dynamics 365 Commercessa. Muut vaiheet käsitellään erillisissä ohjeaiheissa.

[ ![Kokeilun käyttäjän siirtymä – arviointi ja päättäminen](./media/experimentation_review_complete.svg) ](./media/experimentation_review_complete.svg#lightbox)

Kun [koe on suoritettu](experimentation-run-monitor.md) ja on kerätty riittävästi tietoa sen määrittämiseen, mitä variaatiota halutaan käyttää live-sivustossa, variaatio korotetaan ja koe lopetetaan.

## <a name="promote-a-variation"></a>Variaation korottaminen
Kolmannen osapuolen palvelussa suoritettuun kokeeseen liittyvien tietojen ja analyysien avulla voi päättää, millä variaatiolla saatiin parhaat tulokset. Live-sivuston nykyisen sisällön voi korvata voittajavariaatiolla siten, että se on kaikkien käyttäjien käytettävissä, toimimalla seuraavasti: 

1. Siirry sivustonmuodostimessa **Kokeet**-välilehteen ja valitse koe.
1. Valitse yläpalkissa **Päätä koe**.
1. Valitse **Päätä koe** -valintaikkunassa **Arvioi kokeen tiedot**. Voit arvioida avautuvassa kolmannen osapuolen palvelussa mittareita ja määrittää, mikä variaatio suoriutui parhaiten.
1. Valitse sivustonmuodostimen **Päätä koe** -valintaikkunassa voittajavariaatio ja valitse sitten **Seuraava**.
1. Avaa kolmannen osapuolen palvelu ja pysäytä kokeilu.
1. Valitse sivustonmuodostimessa **Päätä**. jolloin alkuperäinen live-sivusto korvataan ja voittajavariaatio julkaistaan. Sen jälkeen kyseinen variaatio on kaikkien sivuston käyttäjien käytettävissä. 

> [!NOTE]
> Jos valitset nykyisen live-sivun säilyttämisen etkä julkaise variaatiota, valitse **Julkaise alkuperäinen sivu uudelleen**.

## <a name="delete-your-experiment"></a>Kokeen poistaminen
Vaikka Commercessa päättynyttä koetta ei ole pakko poistaa, sen voi poistaa, mikä säästää tilaa ja siistii työntilaa. Poista koe seuraavasti:

1. Siirry sivustonmuodostimessa **Kokeet**-välilehteen ja valitse koe. 
    > [!NOTE]
    > Jos koe on edelleen aktiivinen, lopeta koe kolmannen osapuolen palvelussa ennen jatkamista.
1. Poista variaatiosisältö live-sivustosta valitsemalla komentopalkissa **Peruuta julkaisu**.
1. Poista koe valitsemalla komentopalkissa **Poista**.

## <a name="previous-step"></a>Edellinen vaihe
[Kokeen suorittaminen ja seuranta](experimentation-run-monitor.md)
