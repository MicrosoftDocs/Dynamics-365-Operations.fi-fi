---
title: Käytettävissä olevan varaston kustannusarvojen oikaiseminen
description: Käytettävissä olevan varaston oikaisu -sivulla voit oikaista käytettävissä olevan varaston määrien kustannusarvoa varaston sulkemisprosessin suorituksen jälkeen.
author: JennySong-SH
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventAdjInventOnHand
audience: Application User
ms.reviewer: kamaybac
ms.custom: 53231
ms.assetid: bc1fde9f-5ad9-4339-8ae8-e2839b792eb2
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yanansong
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 62122454b2fe0f6a9f04f073057156603e66bb22
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/03/2022
ms.locfileid: "8673295"
---
# <a name="adjust-on-hand-inventory-cost-values"></a>Käytettävissä olevan varaston kustannusarvojen oikaiseminen

[!include [banner](../includes/banner.md)]

Käytettävissä olevan varaston oikaisu -sivulla voit oikaista käytettävissä olevan varaston määrien kustannusarvoa varaston sulkemisprosessin suorituksen jälkeen.

**Käytettävissä olevan varaston oikaisu** -sivulla voit oikaista käytettävissä olevan varaston määrien kustannusarvoa varaston sulkemisprosessin suorituksen jälkeen. **Huomautus:** **Käytettävissä olevan varaston oikaisu** -sivu avataan **Päätös ja oikaisu** -sivulla valitsemalla valmiin varaston sulkemisprosessin tietue ja valitsemalla sitten **Oikaisu** &gt; **Varastosaldo**. **Esimerkki:** Helmikuussa suoritetaan seuraavat tapahtumat:

-   1. helmikuuta: varaston rahoituksellinen vastaanotto, määrä 2, kustannus 10,00 €
-   5. helmikuuta: varaston rahoituksellinen vastaanotto, määrä 1, kustannus 13,00 €
-   19. helmikuuta: rahoituksellinen varasto-otto, määrä 1, juokseva keskimääräinen kustannus 11,00 €.

Tämä nimike on määritetty FIFO-varastomallilla ja varaston sulkeminen suoritettiin 28.2. Rahoituksellinen tapahtumaotto 11,00 $ täsmäytetään vasten rahoituksellista vastaanottoa, jonka päivämäärä on 1.2. Tehdään oikaisu, jonka arvo on 1,00 $. Tämän jälkeen seuraavat varaston vastaanotot sisältävät avoimia varastomääriä:

-   1. helmikuuta: Määrä 1 ja kustannus 10,00 €
-   5. helmikuuta: Määrä 1 ja kustannus 13,00 €

Voit määrittää näiden kahden nimikkeen kustannukseksi 15,00 Yhdysvaltain dollaria oikaisemalla avoimen käytettävissä olevan varaston edellisestä varaston sulkemisesta lähtien. **Huomautus:** Käytettävissä olevan varaston oikaisutapahtuman kirjauspäivämäärä on edellinen varaston sulkemispäivämäärä. Tätä päivämäärää ei voi muokata.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]