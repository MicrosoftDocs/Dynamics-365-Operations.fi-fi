---
title: Hybridit asiakastilaukset
description: "Hybridi asiakastilaus on yksittäinen tilaus, joka sisältää tuotteita, jotka asiakas voi kuljettaa ulos myymälästä, sekä tuotteita, jotka kerätään tai toimitetaan myöhemmin."
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 261164
ms.assetid: 9d99a5b9-4662-499a-bece-3ea1d6092934
ms.search.region: global
ms.search.industry: Retail
ms.author: anpurush
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: eb6ba7cfdf098671192d4d6e73119f96b287c437
ms.contentlocale: fi-fi
ms.lasthandoff: 05/25/2017


---

# <a name="hybrid-customer-orders"></a>Hybridit asiakastilaukset

[!include[banner](includes/banner.md)]


Hybridi asiakastilaus on yksittäinen tilaus, joka sisältää tuotteita, jotka asiakas voi kuljettaa ulos myymälästä, sekä tuotteita, jotka kerätään tai toimitetaan myöhemmin.

Microsoft Dynamics 365 for Operations - Retail -sovelluksessa voit valita kaikki tai vain valitut tuotteet asiakkaan kuljetettaviksi. Tuotteen rivit, jotka on merkitty asiakkaan kuljetettaviksi, automaattisesti laskutetaan tilauksen luonnin jälkeen. Samoin tämä toimii tilauksessa, joka on kerätään sen jälkeen, kun tilaus on luotu. Erääntynyt summa hybriditilauksissa määritetään lisäämällä talletusprosentti poiminnan ja toimituksen tuotteiden riveillä, asiakkaan kuljettamien tuotteiden rivien kokonaissumman kanssa. Hybriditilauksille järjestelmän tila muuttuu asiakkaan tilauksen tilan ja itsepalvelutukkutilan välillä seuraavasti:

-   Jos ostoskorin kaikki tuotteet ovat **asiakkaan kuljettamia**, tilausta käsitellään kuin itsepalvelutukkutapahtumaa.
-   Jos ostoskorin mille tahansa riville on määritetty joko **Kerää** tai **Lähetä toimitus**, tilaus käsitellään asiakastilaustapahtumana.

Jos valitun myyntikorin rivi on valittu ja on myös **Kerää valitut**, **Toimita valitut** tai **Asiakas kuljettaa valitut** valittuna, vain tämä tietty ostoskorin rivi on määritetty kyseiselle toimitustavalle. Tässä tapauksessa prosessi jatkuu tavalliseen tapaan. Kuitenkin jos **Kerää valitut**, **Toimita valitut** tai **Asiakas kuljettaa valitut** on valittu, mutta myyntikorin riviä ei, uusi sivu avautuu, jossa luetellaan kaikki ostoskorin rivit. Tällä näytöllä voit valita useita rivejä kerralla toimitustavan asettamiseen. Kun kyseistä menetelmää käytetään rivin valitsemiseen, ohitetaan edelliset toimitustavat, jotka on määritetty riville.

<a name="see-also"></a>Lisätietoja
--------

[Asiakastilausten yleiskatsaus](customer-orders-overview.md)




