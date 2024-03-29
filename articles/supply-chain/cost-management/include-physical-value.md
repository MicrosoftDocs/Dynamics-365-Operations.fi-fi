---
title: Sisällytä fyysinen arvo
description: Nimikemalliryhmät -sivun Varastomalli-pikavälilehden Sisällytä fyysinen arvo -valintaruudun avulla määritetään, otetaanko fyysisesti päivitetyt tapahtumat huomioon nimikkeen keskimääräisen käyttökustannushinnan laskennassa.
author: JennySong-SH
ms.date: 10/31/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventModelGroup
audience: Application User
ms.reviewer: kamaybac
ms.custom: 79033
ms.assetid: 1928c145-bf82-436d-87ca-e7a173e31923
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yanansong
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6fb7a2a401bd7900555646c3ff0e1be9bf4a50d3
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/03/2022
ms.locfileid: "8672399"
---
# <a name="include-physical-value"></a>Sisällytä fyysinen arvo

[!include [banner](../includes/banner.md)]

Nimikemalliryhmät -sivun Varastomalli-pikavälilehden Sisällytä fyysinen arvo -valintaruudun avulla määritetään, otetaanko fyysisesti päivitetyt tapahtumat huomioon nimikkeen keskimääräisen käyttökustannushinnan laskennassa.

**Sisällytä fyysinen arvo** -valintaruudulla on seuraavat arvot.

| Arvo    | Tulos                                                                                                                          |
|----------|---------------------------------------------------------------------------------------------------------------------------------|
| Valittu | Keskimääräisen kustannushinnan laskennassa käytetään sekä fyysisesti että rahoituksellisesti päivitettyjä tapahtumia. |
| Selvitetyt  | Keskimääräisen kustannushinnan laskennassa käytetään vain rahoituksellisesti päivitettyjä tapahtumia.                                     |

Valintaruudulla on hieman erilaisia vaikutuksia käytettävän varastomallin mukaan.

-   Jos valitset **Sisällytä fyysinen arvo** -valintaruudun, kun käytät FIFO-, LIFO- tai LIFO-päivämäärävarastomallia, varaston sulkeminen oikaisee myös fyysisesti päivitetyt tapahtumat.
-   Jos et valitse **Sisällytä fyysinen arvo** -valintaruutua käyttäessäsi näitä varastomalleja, varaston sulkeminen selvittää vain kirjanpidollisesti päivitetyt tapahtumat.
-   Kun käytät painotettua keskiarvoa tai painotetun keskiarvon päivämäärän varastomallia, varaston sulkeminen selvittää vain rahoituksellisesti päivitetyt tapahtumat riippumatta siitä, onko **Sisällytä fyysinen arvo** -valintaruutu valittu.

**Esimerkki 1** Olet valinnut **Sisällytä fyysinen arvo** -valintaruudun ja saat seuraavat ostotilaukset:

-   Ostotilaus, jonka määrä on 2 ja kustannushinta 10,00 USD, on pakkausluettelopäivitetty.
-   Ostotilaus, jonka määrä on 3 ja kustannushinta 12,00 USD, on laskupäivitetty.

Tässä tilanteessa keskimääräinen käyttökustannushinta on 11,20 = (2x10+3x12)/(2+3) Yhdysvaltain dollaria (USD), koska kustannushinnan laskennassa käytetään sekä fyysisesti että rahoituksellisesti päivitettyjä tapahtumia. 

**Esimerkki 2** Et ole valinnut **Sisällytä fyysinen arvo** -valintaruutua ja nimikeasetusten kustannushinta on 10,00 Yhdysvaltain dollaria (USD). 

-   Saat ostotilauksen, jonka määrä on 20 ja kustannushinta 12,00 USD, ja se on pakkausluettelopäivitetty.

Kun myyntitilaus kirjataan, kirjattu kustannussumman on 10,00 Yhdysvaltain dollaria (USD), koska fyysisesti kirjatut tapahtumat eivät ole mukana keskimääräisessä käyttökustannushinnassa. 

> [!NOTE]
> Jos puolestaan olet valinnut nimikkeen **Sisällytä fyysinen arvo** -valintaruudun ja myyntitilaus kirjataan, kirjattu kustannussumma on 12,00 Yhdysvaltain dollaria.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]