---
title: Vähittäismyyntilaskelmiin vaikuttavien parametrien määrittäminen
description: Tässä aiheessa esitellään Commercen parametrit konfiguraatiot, jotka vaikuttavat laskelmien luomiseen ja kirjaamiseen.
author: josaw1
manager: AnnBe
ms.date: 08/01/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailParameters
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d8cae6d2fa7c469f50fa92141a6cb5a0af1df4b0
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/01/2020
ms.locfileid: "3022377"
---
# <a name="configure-parameters-that-affect-retail-statements"></a>Vähittäismyyntilaskelmiin vaikuttavien parametrien määrittäminen

[!include[task guide banner](../includes/task-guide-banner.md)]

Tässä aiheessa esitellään Commercen parametrit konfiguraatiot, jotka vaikuttavat laskelmien luomiseen ja kirjaamiseen. Näissä toimintaohjeissa käytetään esittely-yritystä USRT.

1. Siirry siirtymisruudussa kohtaan **Moduulit >Retail ja Commerce > Pääkonttorin asetukset > Parametrit > Commercen parametrit**.
2. Valitse **Kirjaus**-välilehti.
    - Valitse **Kyllä**, jos haluat kirjata erityisesti kausialennussummat.  
    - Valitse **Vakio**, kun haluat käyttää oletustilejä. Valitse **Kausittainen**, jos haluat määrittää kunkin kausialennuksen käyttämän tili.  
      - Valitse **Yhteenveto**, jos varastorivit yhdistetään aina, kun se on mahdollista.  
      - Valitse **Kyllä**, jos laskut ja maksut selvitetään automaattisesti laskelman kirjausprosessin osana.  
      - Valitse **Kyllä**, jos kassakaappiin toimitukset yhdistetään.  
      - Valitse **Kyllä**, jos pankkiin toimitukset yhdistetään.  
      - Valitse **Kyllä**, jos laskelman kirjauksen yhdistäminen otetaan käyttöön.  
      - Valitse **Kyllä**, kun tilaukset luodaan ja käsitellään rinnakkain, kun laskelmat kirjataan.  
      - Syötä kussakin erätyötehtävässä käsiteltävien tilausten enimmäismäärä.  
3. Valitse **Tallenna**.

