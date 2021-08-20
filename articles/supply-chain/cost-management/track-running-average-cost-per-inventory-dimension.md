---
title: Varastodimensiokohtaisen juoksevan keskimääräisen kustannuksen seuranta
description: Jokaiseen varastonimikkeeseen liitetään varastodimensioryhmä. Siten nimikkeen keskimääräinen kustannushinta lasketaan niiden varastodimensioiden perusteella, joita seurataan rahoituksellisesti.
author: AndersGirke
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventOnhandItem
audience: Application User
ms.reviewer: kamaybac
ms.custom: 75053
ms.assetid: 68cc00f4-0f7a-4a7d-be90-8f2e0d0563d3
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9ed1ced17eb25bdc10994b1e9e74c90a1d4ec95227bb1ddb072bae88e9255c0d
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/05/2021
ms.locfileid: "6781083"
---
# <a name="track-running-average-cost-per-inventory-dimension"></a>Varastodimensiokohtaisen juoksevan keskimääräisen kustannuksen seuranta

[!include [banner](../includes/banner.md)]

Jokaiseen varastonimikkeeseen liitetään varastodimensioryhmä. Siten nimikkeen keskimääräinen kustannushinta lasketaan niiden varastodimensioiden perusteella, joita seurataan rahoituksellisesti.

Varastodimensioita on kolmentyyppisiä: tuote, varasto ja seuranta. Tuotedimensioita ovat konfiguraatio, koko ja väri. Tuotedimensiota seurataan aina rahoituksellisesti. Varasto- ja seurantadimensioita ovat toimipaikka, varasto, sijainti, varaston tila, rekisterikilpi, eränumero ja sarjanumero. Voit määrittää rahoituksellisesti seurattavat varasto- ja seurantadimensiot. 

**Esimerkki 1** 

Jos varasto seuraa nimikkeeseen liitettyä varastodimensioryhmää rahoituksellisesti, jokaiselle varastolle lasketaan keskimääräinen kustannushinta. Seuraavat ostotilaukset on laskutettu:

-   Ostotilaus, jonka määrä on 2 ja kustannushinta 10,00 USD, on laskutettu varastolle GW.
-   Ostotilaus, jonka määrä on 3 ja kustannushinta 12,00 USD, on laskutettu varastolle GW.
-   Ostotilaus, jonka määrä on 5 ja kustannushinta 15,00 USD, on laskutettu varastolle MW.

Varaston GW keskimääräinen kustannushinta on 11,20 USD ja varaston MW keskimääräinen kustannushinta on 15,00 USD. Myyntitilauslasku kirjataan varastolle GW. Varaston arvo ja myytyjen tuotteiden kustannukset (ennen varaston sulkemista ja ilman merkintää) ovat 11,20 USD. Toinen myyntitilaus kirjataan varastolle MW. Varaston arvo ja myytyjen tuotteiden kustannukset (ennen varaston sulkemista ja ilman merkintää) ovat 15,00 USD. 

**Esimerkki 2** Jos varasto seuraa nimikkeeseen liitettyä varastodimensioryhmää rahoituksellisesti ja eränumero seuraa seurantadimensioryhmää rahoituksellisesti, keskimääräinen kustannushinta lasketaan kullekin erälle. 

**Huomautus:** Kaikkien seurattavien taloushallinnon dimensioiden kustannushintaa on hyvä pitää silmällä. Seuraavat ostotilaukset on laskutettu:

-   Ostotilaus, jonka määrä on 2 ja kustannushinta 10,00 USD, on laskutettu varastolle GW ja erälle AAA.
-   Ostotilaus, jonka määrä on 3 ja kustannushinta 12,00 USD, on laskutettu varastolle GW ja erälle AAA.
-   Ostotilaus, jonka määrä on 2 ja kustannushinta 15,00 USD, on laskutettu varastolle GW ja erälle BBB.

Varaston GW ja erän AAA keskimääräinen kustannushinta on 11,20 USD ja varaston MW ja erän BBB keskimääräinen kustannushinta on 15,00 USD.





[!INCLUDE[footer-include](../../includes/footer-banner.md)]