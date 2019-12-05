---
title: Hybridit asiakastilaukset
description: Hybridi asiakastilaus on yksittäinen tilaus, joka sisältää tuotteita, jotka asiakas voi kuljettaa ulos myymälästä, sekä tuotteita, jotka kerätään tai toimitetaan myöhemmin.
author: josaw1
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 261164
ms.assetid: 9d99a5b9-4662-499a-bece-3ea1d6092934
ms.search.region: global
ms.search.industry: Retail
ms.author: anpurush
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: ef99a75d29b8fce46943213804239b237d384b07
ms.sourcegitcommit: 57bc7e17682e2edb5e1766496b7a22f4621819dd
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/18/2019
ms.locfileid: "2811899"
---
# <a name="hybrid-customer-orders"></a>Hybridit asiakastilaukset

[!include [banner](includes/banner.md)]

Hybridi asiakastilaus on yksittäinen tilaus, joka sisältää tuotteita, jotka asiakas voi kuljettaa ulos myymälästä, sekä tuotteita, jotka kerätään tai toimitetaan myöhemmin.

Retailissa voit toteuttaa issa kaikki asiakastilauksen tuotteet tai vain valitut tuotteet. Tuotteen rivit, jotka on merkitty asiakkaan kuljetettaviksi, automaattisesti laskutetaan tilauksen luonnin jälkeen. Samoin tämä toimii tilauksessa, joka on kerätään sen jälkeen, kun tilaus on luotu. Erääntynyt summa hybriditilauksissa määritetään lisäämällä talletusprosentti poiminnan ja toimituksen tuotteiden riveillä, asiakkaan kuljettamien tuotteiden rivien kokonaissumman kanssa. Hybriditilauksille järjestelmän tila muuttuu asiakkaan tilauksen tilan ja itsepalvelutukkutilan välillä seuraavasti:

- Jos ostoskorin kaikki tuotteet ovat **asiakkaan kuljettamia**, tilausta käsitellään kuin itsepalvelutukkutapahtumaa.
- Jos ostoskorin mille tahansa riville on määritetty joko **Kerää** tai **Lähetä toimitus**, tilaus käsitellään asiakastilaustapahtumana.

Jos valitun myyntikorin rivi on valittu ja on myös **Kerää valitut**, **Toimita valitut** tai **Asiakas kuljettaa valitut** valittuna, vain tämä tietty ostoskorin rivi on määritetty kyseiselle toimitustavalle. Tässä tapauksessa prosessi jatkuu tavalliseen tapaan. Kuitenkin jos **Kerää valitut**, **Toimita valitut** tai **Asiakas kuljettaa valitut** on valittu, mutta myyntikorin riviä ei, uusi sivu avautuu, jossa luetellaan kaikki ostoskorin rivit. Tällä näytöllä voit valita useita rivejä kerralla toimitustavan asettamiseen. Kun kyseistä menetelmää käytetään rivin valitsemiseen, ohitetaan edelliset toimitustavat, jotka on määritetty riville.

## <a name="additional-resources"></a>Lisäresurssit

[Retail Modern POS:n (MPOS) asiakastilaukset](customer-orders-overview.md)
