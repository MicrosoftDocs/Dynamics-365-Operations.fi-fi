---
title: Hinnanoikaisut ja alennukset
description: Tässä artikkelissa on tietoja Dynamics 365 Commercein hinnanoikaisuista ja alennuksista.
author: scott-tucker
manager: AnnBe
ms.date: 11/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailParameters, RetailPeriodicDiscount
audience: Application User
ms.reviewer: josaw
ms.custom: 15891
ms.assetid: bab5adf3-ddf0-4c22-a2eb-b4d25b88de99
ms.search.region: global
ms.search.industry: Retail
ms.author: scotttuc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: f29e90e1c61792c70d4d6eaeee7758676bf193b2
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/15/2021
ms.locfileid: "4972478"
---
# <a name="price-adjustments-and-discounts"></a>Hinnanoikaisut ja alennukset

[!include [banner](includes/banner.md)]

Tässä artikkelissa on tietoja Dynamics 365 Commercein hinnanoikaisuista ja alennuksista.

Voit tehdä Commercessa tuotteiden hinnanoikaisuja ja myös määrittää alennuksia, joita käytetään nimikkeeseen tai tapahtumaan myyntipisteessä, puhelinkeskuksen myyntitilauksessa tai verkkotilauksessa. Sekä hinnanoikaisut että alennukset voidaan linkittää hintaryhmiin. Hinnanoikaisuille ja alennuksille voidaan määrittää yksi aloitus- ja päättymispäivämäärä tai toistuva jakso, alennuskoodi ja joitakin muita määritteitä. 

Hinnanoikaisuja ja alennuksia voidaan käyttää tuotteissa, varianteissa tai kategorioissa. Jos tuotteelle on useita alennuksia, asiakas voi saada minkä tahansa alennuksen tai alennusten yhdistelmän alennuksen määritysten mukaisesti. Commerce käyttää automaattisesti alennusta tai alennusten yhdistelmää, joka takaa asiakkaalle parhaan hinnan. Kun määrität hinnanoikaisua tai alennusta, muista vahvistaa, että hintaryhmät on liitetty oikeisiin kanaviin, luetteloihin, liitoksiin tai kanta-asiakasohjelmiin, joissa haluat käyttää alennusta. Lisäksi jos haluat luoda alennustunnuksen automaattisesti, määritä numerosarjat **Commercen parametrit** -sivulla, ennen kuin määrität uuden hinnanoikaisun tai alennuksen.

> [!NOTE]
> Voit poistaa hinnanoikaisun tai alennuksen. Tällöin tilastotiedot kuitenkin häviävät.

## <a name="types-of-discounts"></a>Alennusten tyypit

Alennuksia on useita tyyppejä:

- **Yksinkertainen alennus** – Yksi prosenttiosuus tai määrä.
- **Määräalennus** – alennus, jota käytetään, kun tuotteita ostetaan vähintään kaksi.
- **Yhdistelmäalennus** – alennus, jota käytetään, kun ostetaan tietty tuoteyhdistelmä.
- **Raja-arvon alennus** – alennus, jota käytetään, kun tapahtuman kokonaissumma ylittää tietyn summan.
- **Maksuvälinepohjainen alennus** – Alennus, jota käytetään, kun tapahtuman kokonaissumma on määritettyä summaa suurempi ja tiettyä maksutyyppiä (esimerkiksi käteinen, luottokortti tai pankkikortti) on käytetty maksussa.
- **Lähetysalennus** – Alennus, jota käytetään, kun tapahtuman kokonaissumma on enemmän kuin määritetty summa ja jos tilauksessa on käytössä tietty toimitustapa (esimerkiksi kahden päivän toimitus tai toimitus yön aikana).

Sekä hinnanoikaisut että alennukset voidaan yhdistää hintaryhmiin. Hintaryhmät voidaan tämän jälkeen liittää kanaviin, luetteloihin, liitoksiin ja kanta-asiakasohjelmiin.


[!INCLUDE[footer-include](../includes/footer-banner.md)]