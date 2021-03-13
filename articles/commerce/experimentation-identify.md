---
title: Hypoteesin ja kokeen mittareiden määrittäminen
description: Tässä ohjeaiheessa käsitellään hypoteesin ja sähköisessä kaupankäyntisivustossa Dynamics 365 Commercessa suorittavan kokeen onnistumismittareiden määrittämistä.
author: sushma-rao
manager: AnnBe
ms.date: 10/21/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
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
ms.openlocfilehash: 5594b81d09eade263487244a14c0305d589ff94e
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/15/2021
ms.locfileid: "5009996"
---
# <a name="identify-a-hypothesis-and-determine-success-metrics-for-an-experiment"></a>Hypoteesin ja kokeen onnistumismittareiden määrittäminen
Kokeen elinkaaren ensimmäinen vaihe sisältää kokeen hypoteesin ja onnistumisen arvioinnissa käytettävien mittareiden määrittämisen. Seuraavassa kaaviossa on kaikki vaiheet, jotka sisältyvät [kokeen määrittämiseen ja suorittamiseen ](experimentation-overview.md) sähköisessä kaupankäyntisivustossa Dynamics 365 Commercessa. Muut vaiheet käsitellään erillisissä ohjeaiheissa. 

[ ![Kokeilun käyttäjän siirtymä – määrittäminen](./media/experimentation_identify.svg) ](./media/experimentation_identify.svg#lightbox)

Hypoteesi on väite, joka ennakoi kokeen tuloksen. Hypoteesin määrittämisessä on monia vaiheita, kuten käyttäjien toiminnasta ja sivustosta kerättyihin tietoihin tutustuminen. Hypoteesin avulla määritetään oletus tai teoria, joka halutaan vahvistaa kokeen avulla. Kokeen hypoteesi voi olla esimerkiksi seuraava: *aloitussivulla oleva kuva valkoisesta teepaidasta tuottaa kesäkuukausina enemmän mainoslinkin napsautuksia kuin tummansininen neule, koska ihmiset haluat käyttää ohuita ja vaaleita vaatteita kesällä*. Tässä tapauksessa luodaan variaatiot, joissa käytetään valkoista teepaitaa ja tummansinistä neuletta, ja molemmat julkaistaan samanaikaisesti.

Hypoteesin vahvistamista varten kokeen onnistuminen tai epäonnistuminen on sidottava suoraan käyttäjän toimintoihin, kuten siihen, napsauttaako sivuston käyttäjä linkkiä tai painiketta. Näiden toimintojen on sitten vastattava tapahtumia, jotka ilmoitetaan koetta seuraavalle kolmannen osapuolen palvelulle. Toiminnon ajan mittaan suorittavien käyttäjien prosenttiosuus lasketaan yhteen mittarina, jolla voi luoda raportteja ja tehdä analyyseja. Lisätietoja kaikkien käytettävissä olevien tapahtumien ja määritteiden tarkistamisesta on kohdassa [Commerce-komponenttien diagnostiikka- ja vianmääritystapahtumat](dev-itpro/retail-component-events-diagnostics-troubleshooting.md).

## <a name="previous-step"></a>Edellinen vaihe
[Kokeilu Dynamics 365 Commercessa](experimentation-overview.md)


## <a name="next-step"></a>Seuraava vaihe
[Kokeilun määrittäminen](experimentation-setup.md)
