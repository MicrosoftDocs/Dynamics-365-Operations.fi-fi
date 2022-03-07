---
title: Hinnanoikaisut ja alennukset
description: Tässä artikkelissa on tietoja Dynamics 365 Commercen hinnanoikaisuista ja alennuksista.
author: scott-tucker
ms.date: 06/11/2021
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 96a695df250cda514b7bd8b9716c0f03fb2bfd28d3af4daedaf1335c3099fbb6
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/05/2021
ms.locfileid: "6748495"
---
# <a name="price-adjustments-and-discounts"></a>Hinnanoikaisut ja alennukset

[!include [banner](includes/banner.md)]

Tässä artikkelissa on tietoja Dynamics 365 Commercen hinnanoikaisuista ja alennuksista.

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

> [!NOTE]
> Yhdistelmäalennus ja raja-alennus sisältävät ominaisuudet nimeltään "Laske ei-alennuskelpoiset tuotteet" ja "Laske ei-alennuskelpoiset tuotteet raja-arvon suhteen". Jos nämä ominaisuudet ovat käytössä, nimike, joka ei ole oikeutettu mihinkään alennukseen, voi silti auttaa hyväksymään alennustapahtuman, mutta nimike, jolle ei ole oikeutta, ei saa alennusta. 
> 
> Jos esimerkiksi luot yhdistelmäalennuksen, jossa on kaksi riviä A ja B, jossa asiakkaan tulee saada 10 %:n alennus molemmista nimikkeistä, mutta nimikkeen A konfiguraatiossa on "Estä kaikki alennukset" -valintaruutu, tämä yleensä lopettaisi nimikkeen A sisällyttämisen alennukseen. Jos kuitenkin Laske ei-alennuskelpoiset tuotteet -ominaisuus on käytössä, nimikettä A voidaan käyttää yhdistelmäalennuksen hyväksymiseen, mutta 10 %:n alennus koskee vain nimikettä B. Vastaava logiikka koskee raja-alennusta. 
>
> "Laske ei-alennuskelpoiset tuotteet raja-arvon suhteen" -ominaisuudessa on kuitenkin lisätoiminto verrattuna yhdistelmäalennusten "Laske ei-alennuskelpoiset tuotteet" -ominaisuuteen. Jos raja-alennus on käytössä ja jos jollain nimikkeellä on voimassa oleva alennus, joka estää nimikettä muista alennuksista, nimikkeelle maksettava hinta täyttää raja-arvon, mutta tämä nimike ei saa lisäalennusta.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
