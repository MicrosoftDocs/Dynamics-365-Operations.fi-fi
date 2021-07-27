---
title: Variaation määrittäminen ja kokeen päättäminen
description: Tässä ohjeaiheessa käsitellään onnistuneen variaation korottamista ja kokeen päättämistä Dynamics 365 Commercessa.
author: sushma-rao
ms.date: 10/21/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: sushmar
ms.search.validFrom: 2020-09-30
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: 2d098f323d58bf3233a83655b213afe131ae3f36
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 07/06/2021
ms.locfileid: "6349277"
---
# <a name="promote-a-variation-and-complete-an-experiment"></a>Variaation määrittäminen ja kokeen päättäminen

Tässä ohjeaiheessa käsitellään kokeessa parhaan tuloksen tuottaneen variaation korottamista ja kokeen päättämistä. Seuraavassa kaaviossa on kaikki vaiheet, jotka sisältyvät kokeen määrittämiseen ja suorittamiseen sähköisessä kaupankäyntisivustossa Dynamics 365 Commercessa. Muut vaiheet käsitellään erillisissä ohjeaiheissa.

[ ![Kokeilun käyttäjän siirtymä – arviointi ja päättäminen.](./media/experimentation_review_complete.svg) ](./media/experimentation_review_complete.svg#lightbox)

Kun [koe on suoritettu](experimentation-run-monitor.md) ja on kerätty riittävästi tietoa sen määrittämiseen, mitä variaatiota halutaan käyttää live-sivustossa, variaatio korotetaan ja koe lopetetaan.

## <a name="promote-a-variation"></a>Variaation korottaminen
Kolmannen osapuolen palvelussa suoritettuun kokeeseen liittyvien tietojen ja analyysien avulla voi päättää, millä variaatiolla saatiin parhaat tulokset. Sen voi sitten korottaa korvaamalla live-sivuston nykyisen sisällön voittajavariaatiolla siten, että se on kaikkien käyttäjien käytettävissä.

Voittajavariaatio korotetaan seuraavasti: 

1. Valitse Commercen sivustonmuodostimen vasemmassa siirtymisruudussa ensin **Kokeet** ja sitten koe.
1. Valitse komentopalkissa **Päätä koe**.
1. Valitse **Päätä koe** -valintaikkunassa **Arvioi kokeen tiedot**. Voit arvioida avautuvassa kolmannen osapuolen palvelussa mittareita ja määrittää, mikä variaatio suoriutui parhaiten.
1. Valitse **Päätä koe** -valintaikkunassa voittajavariaatio ja valitse sitten **Seuraava**.
1. Avaa kolmannen osapuolen palvelu ja pysäytä kokeilu.
1. Valitse sivustonmuodostimessa **Päätä**. jolloin alkuperäinen live-sivusto korvataan ja voittajavariaatio julkaistaan. Sen jälkeen kyseinen variaatio on kaikkien sivuston käyttäjien käytettävissä. 

> [!NOTE]
> Jos valitset nykyisen live-sivun säilyttämisen etkä julkaise variaatiota, valitse **Julkaise alkuperäinen sivu uudelleen**.

## <a name="delete-your-experiment"></a>Kokeen poistaminen
Vaikka Commercessa päättynyttä koetta ei ole pakko poistaa, sen voi poistaa, mikä säästää tilaa ja siistii työntilaa. 

Kokeen voi poistaa Commercen sivustonmuodostimessa seuraavasti:

1. Valitse Commercen vasemmassa siirtymisruudussa ensin **Kokeet** ja sitten koe. 
    > [!NOTE]
    > Jos koe on edelleen aktiivinen, lopeta koe kolmannen osapuolen palvelussa ennen jatkamista.
1. Poista variaatiosisältö live-sivustosta valitsemalla komentopalkissa **Peruuta julkaisu**.
1. Poista koe valitsemalla **Poista**.

## <a name="previous-step"></a>Edellinen vaihe
[Kokeilun suoritus ja seuranta](experimentation-run-monitor.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]