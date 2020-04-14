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
ms.openlocfilehash: 7892a216d836ebcc297a5b7eb87bc996dd9b91bf
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/18/2020
ms.locfileid: "3140829"
---
# <a name="configure-parameters-that-affect-retail-statements"></a>Vähittäismyyntilaskelmiin vaikuttavien parametrien määrittäminen

[!include [banner](../includes/banner.md)]

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

