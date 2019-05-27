---
title: Käytettävissä olevan varaston kustannusarvojen oikaiseminen
description: Käytettävissä olevan varaston oikaisu -sivulla voit oikaista käytettävissä olevan varaston määrien kustannusarvoa varaston sulkemisprosessin suorituksen jälkeen.
author: AndersGirke
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventAdjInventOnHand
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 53231
ms.assetid: bc1fde9f-5ad9-4339-8ae8-e2839b792eb2
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: aevengir
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2417a278e58f4309873ab4d33b0d1f1686081951
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/15/2019
ms.locfileid: "1556112"
---
# <a name="adjust-on-hand-inventory-cost-values"></a>Käytettävissä olevan varaston kustannusarvojen oikaiseminen

[!include [banner](../includes/banner.md)]

Käytettävissä olevan varaston oikaisu -sivulla voit oikaista käytettävissä olevan varaston määrien kustannusarvoa varaston sulkemisprosessin suorituksen jälkeen.

**Käytettävissä olevan varaston oikaisu** -sivulla voit oikaista käytettävissä olevan varaston määrien kustannusarvoa varaston sulkemisprosessin suorituksen jälkeen. **Huomautus**: Voit avata **Päätös ja oikaisu** -sivun **Käytettävissä olevan varaston oikaisu** -sivulla tietueen valmiiden varaston sulkemisprosessien tietueen ja siirtyä sitten kohtaan **Oikaisu** &gt; **Varastosaldo**. **Esimerkki:** Helmikuussa suoritetaan seuraavat tapahtumat:

-   1. helmikuuta: varaston rahoituksellinen vastaanotto, määrä 2, kustannus 10,00 €
-   5. helmikuuta: varaston rahoituksellinen vastaanotto, määrä 1, kustannus 13,00 €
-   19. helmikuuta: rahoituksellinen varasto-otto, määrä 1, juokseva keskimääräinen kustannus 11,00 €.

Tämä nimike on määritetty FIFO-varastomallilla ja varaston sulkeminen suoritettiin 28.2. Rahoituksellinen tapahtumaotto 11,00 $ täsmäytetään vasten rahoituksellista vastaanottoa, jonka päivämäärä on 1.2. Tehdään oikaisu, jonka arvo on 1,00 $. Tämän jälkeen seuraavat varaston vastaanotot sisältävät avoimia varastomääriä:

-   1. helmikuuta: Määrä 1 ja kustannus 10,00 €
-   5. helmikuuta: Määrä 1 ja kustannus 13,00 €

Voit määrittää näiden kahden nimikkeen kustannukseksi 15,00 Yhdysvaltain dollaria oikaisemalla avoimen käytettävissä olevan varaston edellisestä varaston sulkemisesta lähtien. **Huomautus:** Käytettävissä olevan varaston oikaisutapahtuman kirjauspäivämäärä on edellinen varaston sulkemispäivämäärä. Tätä päivämäärää ei voi muokata.
