---
title: "Poistomenetelmät ja -käytännöt"
description: "Tässä artikkelissa on yleiskuvaus Microsoft Dynamics 365 for Finance and Operationsin tukemista poistomenetelmistä."
author: twheeloc
manager: AnnBe
ms.date: 04/25/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: AssetDepreciationProfile, AssetGroupBookSetup, AssetGroupDepBookSetup
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 3441
ms.assetid: 1d8267b1-86a8-44bf-8814-f56b5d45a0ae
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a0739304723d19b910388893d08e8c36a1f49d13
ms.openlocfilehash: eb38de1e7e39cb66d15bfe344f6f5fcd5d4fccd7
ms.contentlocale: fi-fi
ms.lasthandoff: 03/26/2018

---

# <a name="depreciation-methods-and-conventions"></a>Poistomenetelmät ja -käytännöt

[!include[banner](../includes/banner.md)]


Tässä artikkelissa on yleiskuvaus Microsoft Dynamics 365 for Finance and Operationsin tukemista poistomenetelmistä.

Voit valita useita poistomenetelmiä. Menetelmien tarkoituksena on kohdistaa käyttöomaisuuserän poistokelpoinen arvo tilikausille. Käyttöomaisuuserän poistokelpoinen arvo on hankintahinta vähennettynä mahdollisella jäännösarvolla. 

Jos käytät poistomenetelmiä ja muutat käyttöomaisuuserän viimeisen poiston suorituspäivää, jolloin jotkin poistot jäävät väliin, viimeisen vuoden poisto voi olla odotettua suurempi tai pienempi. Poistoa muutetaan niiden poistokausien määrällä, joihin viimeisen poistokerran päivämäärän muuttaminen vaikuttaa

Jos esimerkiksi käytät puolivuosittaista poistomenetelmää kolmen vuoden ajan, poistot tehdään yleensä 3,5 vuoden aikana. Jos muutat viimeisen poiston suorituspäivää tämän 3 1/2 vuoden kuluessa, viimeinen poistovuosi siirtää niiden kausien määrää, joihin muutos vaikuttaa. Jos siirrät päivämäärää kolmella kuukaudella, viimeisessä vuodessa on yhdeksän kuukautta poistettavaa, kun tavallisesti siinä olisi kuusi kuukautta poistettavaa.

Voit valita jonkin seuraavista poistomenetelmistä.


-   Puolivuosi
-   Täysi kuukausi
-   Vuosineljänneksen puoliväli
-   Kuukauden puoliväli (kuukauden 1. päivä)
-   Kuukauden puoliväli (kuukauden 15. päivä)
-   Puolivuosi (vuoden alku)
-   Puolivuosi (seuraava vuosi)

Voit valita seuraavista poistomenetelmistä.
-   Tasapoisto - käyttöaika
-   Jäännösarvopoisto
-   Manuaalinen
-   Kerroin
-   Kulutus
-   Tasapoisto - jäljellä oleva käyttöaika
-   Jäännös 200 %
-   Jäännös 175 %
-   Jäännös 150 %
-   Jäännös 125 %

 



<a name="see-also"></a>Lisätietoja
--------

[Käyttöomaisuuden poisto](fixed-asset-depreciation.md)

[Käyttöikään perustuva tasapoisto](Straight-line-service-life-depreciation.md)

[Jäännöspoisto](reduce-balance-depreciation.md)

[Manuaalinen poisto](manual-depreciation.md)

[Kerroinpoisto](factor-depreciation.md)

[Kulutuspoisto](consumption-depreciation.md)

[Jäljellä olevan käyttöajan tasapoisto](straight-line-life-remaining-depreciation.md)

[Jäännöspoisto 125 prosenttia](125-percent-reducing-balance-depreciation.md)

[Jäännöspoisto 150 prosenttia](150-percent-reducing-balance-depreciation.md)

[Jäännöspoisto 175 prosenttia](175-percent-reducing-balance-depreciation.md)

[Jäännöspoisto 200 prosenttia](200-percent-reducing-balance-depreciation.md)




