---
title: "Käytettävissä olevan varaston kustannusarvojen oikaiseminen"
description: "Käytettävissä olevan varaston oikaisu -sivulla voit oikaista käytettävissä olevan varaston määrien kustannusarvoa varaston sulkemisprosessin suorituksen jälkeen."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: InventAdjInventOnHand
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 53231
ms.assetid: bc1fde9f-5ad9-4339-8ae8-e2839b792eb2
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: d1ef775c9783b975fd0f852dc7112506d3897605
ms.lasthandoff: 03/31/2017


---

# <a name="adjust-on-hand-inventory-cost-values"></a>Käytettävissä olevan varaston kustannusarvojen oikaiseminen

Käytettävissä olevan varaston oikaisu -sivulla voit oikaista käytettävissä olevan varaston määrien kustannusarvoa varaston sulkemisprosessin suorituksen jälkeen.

**Käytettävissä olevan varaston oikaisu** -sivulla voit oikaista käytettävissä olevan varaston määrien kustannusarvoa varaston sulkemisprosessin suorituksen jälkeen. **Huomautus:** avaamiseen **käytettävissä olevan varaston oikaisu** sivulla oleva **päätös ja oikaisu** sivun, valitse valmis varaston sulkemisprosessi tietue ja valitse sitten **muutos**&gt;**varasto-**. **Esimerkki:** Helmikuussa suoritetaan seuraavat tapahtumat:

-   1. helmikuuta: varaston rahoituksellinen vastaanotto, määrä 2, kustannus 10,00 €
-   5. helmikuuta: varaston rahoituksellinen vastaanotto, määrä 1, kustannus 13,00 €
-   19. helmikuuta: rahoituksellinen varasto-otto, määrä 1, juokseva keskimääräinen kustannus 11,00 €.

Tämä kohde on määritetty ensimmäisen-out (FIFO) ensimmäinen varastomallin ja varaston sulkeminen suoritettiin helmikuun 28. Rahoituksellinen varasto-otto, USD 11.00 tapahtuma täsmäytetään taloudellinen vastaanotto, joka on päivätty helmikuun 1 ja USD 1.00 oikaisu tehdään. Tämän jälkeen seuraavat varaston vastaanotot sisältävät avoimia varastomääriä:

-   1. helmikuuta: Määrä 1 ja kustannus 10,00 €
-   5. helmikuuta: Määrä 1 ja kustannus 13,00 €

Voit määrittää näiden kahden nimikkeen kustannukseksi 15,00 Yhdysvaltain dollaria oikaisemalla avoimen käytettävissä olevan varaston edellisestä varaston sulkemisesta lähtien. **Huomautus:** Käytettävissä olevan varaston oikaisutapahtuman kirjauspäivämäärä on edellinen varaston sulkemispäivämäärä. Tätä päivämäärää ei voi muokata.


