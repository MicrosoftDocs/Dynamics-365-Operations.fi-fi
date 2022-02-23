---
title: Kokeen määrittäminen
description: Tässä aiheessa käsitellään kokeen määrittämistä kolmannen osapuolen palvelussa.
author: sushma-rao
manager: AnnBe
ms.date: 10/21/2020
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
ms.openlocfilehash: 29c21ceb4c259f463f4a039942e51141201a9809
ms.sourcegitcommit: cd83f2bc0e52e13071ad306e07e4c255fc65cb03
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/22/2020
ms.locfileid: "4412113"
---
# <a name="set-up-an-experiment"></a>Kokeen määrittäminen

Sen jälkeen kun olet [määrittänyt hypoteesin ja käytettävät onnistumismittarit](experimentation-identify.md), koe on määritettävä kolmannen osapuolen palvelussa. Seuraavassa kaaviossa on kaikki vaiheet, jotka sisältyvät kokeen määrittämiseen ja suorittamiseen sähköisessä kaupankäyntisivustossa Dynamics 365 Commercessa. Muut vaiheet käsitellään erillisissä ohjeaiheissa.

[ ![Kokeilun käyttäjän siirtymä – määrittäminen](./media/experimentation_setup.svg) ](./media/experimentation_setup.svg#lightbox)


## <a name="set-up-your-experiment-in-the-third-party-service"></a>Kokeen määrittäminen kolmannen osapuolen palvelussa
Tässä vaiheessa kolmannen osapuolen palvelun pitäisi olla valittuna kokeen suorittamista ja seurantaa varten sekä kokeen yhdistämisen määrittämistä varten. Nämä edellytykset on mainittu [Kokeilut Dynamics 365 Commercessa](experimentation-overview.md).

Luo koe kolmannen osapuolen palvelussa noudattamalla annettuja ohjeita. Jos yhdistin on määritetty oikein, täydellinen kolmannen osapuolen palvelussa määritettyjen kokeiden luettelo tulee näkyviin Commercen sivustonmuodostimeen noin 5 minuutin kuluessa.

## <a name="set-up-your-success-metrics"></a>Onnistumismittareiden määrittäminen
Kaikki kokeet tarvitsevat mittarin, jolla mitataan variaatioiden vaikutusta ja vahvistaa hypoteesi. Noudata seuraavia ohjeita ja ota mittareiden laskenta käyttöön kolmannen osapuolen palvelussa käyttämällä Dynamics 365 Commercen live-telemetriatapahtumia.

Onnistumismittarit määritetään seuraavasti:

1. Valitse Commercen sivustonmuodostimen vasemmassa siirtymisruudussa **Sivut**-välilehti ja valitse sitten sivu, josta haluat kerätä mittaustietoja. 
1. Siirry **Seurattava tapahtumatunnukset** -osaan seurattavan sivun tai moduulin oikeassa ominaisuusruudussa.
1. Valitse **Näytä**. Näkyvissä on kaikki tapahtumatunnukset sisältävä luettelo. Kopioi seurattava tapahtuma ja liitä tapahtuma-avain sille varattuun sijaintiin kolmannen osapuolen palvelussa. Jos tarvitset useita tapahtumia, kopioi avaimet yksi kerrallaan. 
    - Lisätietoja kaikkien käytettävissä olevien tapahtumien ja määritteiden, myös sivunäkymien ja tuoton seuraamisen, näyttämisestä on kohdassa [Commerce-komponenttien diagnostiikka- ja vianmääritystapahtumat](dev-itpro/retail-component-events-diagnostics-troubleshooting.md).
1. Suorita muut kolmannen osapuolen palvelun edellyttämät mittareiden seurantaan tarvittavat vaiheet.

## <a name="previous-step"></a>Edellinen vaihe
[Kokeilun hypoteesin ja mittarien määrittäminen](experimentation-identify.md) 


## <a name="next-step"></a>Seuraava vaihe
[Kokeilun yhdistäminen ja muokkaaminen](experimentation-connect-edit.md)
