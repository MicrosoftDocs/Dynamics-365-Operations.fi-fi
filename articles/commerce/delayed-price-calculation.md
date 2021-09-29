---
title: Tarkan hinnan ja alennuksen laskemisen viive suorituskyvyn parantamiseksi
description: Tässä aiheessa kuvaillaan viivytetty hinnan laskemisen toiminto, joka on käytössä Microsoft Dynamics 365 Commerce -myyntipisteessä (POS) ja -puhelinkeskuksessa.
author: boycezhu
ms.date: 09/09/2021
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgri
ms.search.region: Global
ms.author: boycez
ms.search.validFrom: 2017-06-20
ms.openlocfilehash: 8c4264c3a4c71e6aab0e1ef8d7d8cfffad065a46
ms.sourcegitcommit: 7a2001e4d01b252f5231d94b50945fd31562b2bc
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/15/2021
ms.locfileid: "7488360"
---
# <a name="delay-exact-price-and-discount-calculation-for-improved-performance"></a>Tarkan hinnan ja alennuksen laskemisen viive suorituskyvyn parantamiseksi

[!include [banner](includes/banner.md)]

Tässä aiheessa kuvaillaan viivytetty hinnan laskemisen toiminto, joka on käytössä Microsoft Dynamics 365 Commerce -myyntipisteessä (POS) ja -puhelinkeskuksessa.

Dynamics 365 Commerce tukee monirivialennusten luomista, jota käytetään, kun myyntitilauksen tai myyntitarjouksen useita myyntirivejä yhdistetään. Alennuksiin kuuluvat yhdistelmä-, rajan ylittyessä- ja määräalennukset.

Kun tilaukseen lisätään uusi rivi, Commerce-hinnoitteluydin arvioi koko ostoskorin ja määrittää, voiko jotakin näistä monirivialennuksista käyttää. Uudelleenlaskennan vuoksi uusien rivien lisäys voi vaikuttaa suorituskykyyn myyntitilauksen kasvaessa.

Yritystenvälistä yhteistyötä (B2B) tekevillä yrityksillä ja joillakin kuluttajakauppaa (B2C) tekevillä yrityksillä on kuitenkin usein suuria tilauskokoja. Siksi joskus voi kulua paljon aikaa, kun joudutaan odottamaan, kun hinnoitteluydin tekee uudelleenlaskennan jokaisen ostoskoriin lisätyn nimikkeen myötä. Suurten tilausten tarkan hinnan ja alennuksen näyttäminen ei yleensä ole erityisen tärkeää jokaisen ostoskoriin lisätyn nimikkeen myötä. On tärkeämpää, että käyttäjät voivat lisätä nimikkeitä nopeasti. Mahdollisuus viivyttää tarkkaa hinta- ja alennuslaskentaa siihen asti, että käyttäjä pyytää sitä tai tilaus on valmis, voi parantaa suorituskykyä merkittävästi. Se voi myös lyhentää tilauksen valmistumiseen tarvittavaa aikaa.

Mahdollisuus viivyttää tarkkaa hinnan ja alennuksen laskentaa on kauan ollut käytettävissä myyntipisteessä. Commerce-version 10.0.22 julkaisun myötä se on käytössä myös puhelinkeskuksessa.

## <a name="enable-delayed-price-and-discount-calculation-for-pos"></a>Ota käyttöön viivytetty hinnan ja alennuksen laskeminen myyntipisteessä

Ota käyttöön viivytetty hinnan ja alennuksen laskeminen myyntipisteessä seuraavasti.

1. Siirry Commercen pääkonttorissa fyysiseen myymälään liittyvään toimintoprofiiliin.
1. Ota käyttöön **Määrä**-pikavälilehdessä **Laske manuaalisesti moninimikealennukset** -määritys.
1. Avaa näytön asettelun suunnitteluohjelma niille kassoille, joissa viivytetyn laskennan pitäisi olla käytössä.
1. Lisää painike **Laske kokonaissumma** -operaatiolle haluamaasi painikeruudukkoon.
1. Suorita työt **1070** ja **1090**.

Nyt kun nimikkeet on lisätty tapahtumaan, monirivialennuksia ei lasketa, ellei kassa valitse **Laske kokonaissumma** -painiketta. Sen jälkeen, kun **Laske kokonaissumma** on valittu tapahtumalle, sille lasketaan aina monirivialennukset. Kassan ei tarvitse valita painiketta uudelleen, vaikka lisänimikkeitä lisättäisiin ostoskoriin. Järjestelmä ei salli kassan siepata maksua ennen kuin **Laske kokonaissumma** on valittu.

## <a name="enable-delayed-price-and-discount-calculation-for-call-center"></a>Ota käyttöön viivytetty hinnan ja alennuksen laskeminen puhelinkeskuksessa

Ota käyttöön viivytetty hinnan ja alennuksen laskeminen puhelinkeskuksessa seuraavasti.

1. Siirry Commerce pääkonttorissa kohtaan **Työtilat \> Ominaisuuksien hallinta**.
1. Ota käyttöön ominaisuus **Estä tahaton Commerce-tilauksen hintojen laskeminen**. Tämä ominaisuus on edellytys viivytetyn hinnan ja alennuksen laskemisen toiminnolle.

    > [!NOTE]
    > Uusissa käyttöönotoissa **Estä tahaton Commerce-tilauksen hintojen laskeminen** -ominaisuus on oletusarvoisesti otettu käyttöön.

1. Siirry **Commerce-parametrit \> Hinnat ja alennukset**.
1. Ota käyttöön **Muut**-osassa **Laske monirivihinnat ja -alennukset manuaalisesti** -määritys.

Kun myyntitilaus tai myyntitarjous luodaan tai sitä muokataan puhelinkeskuksessa, sen tarkka hinta- ja alennuslaskelma viivytetään. Hinnoitteluydin ottaa huomioon vain lisättävät tai muokatut myyntirivit, eikä se huomioi muita myyntirivejä. Nimikkeen nettosumma sisältää hinnan laskennan ja yksinkertaiset alennukset (yksittäisen nimikkeen alennusprosentti tai alennussumma). Yhdistelmä-, rajan ylittyessä- ja määräalennuksia ei kuitenkaan sovelleta. Puhelinkeskuksen käyttäjät, jotka haluavat tarkastella tarkkaa hintaa, mukaan lukien kaikkia alennuksia, voivat valita yhden kolmesta painikkeesta: **Laske uudelleen**, **Kokonaismäärät** tai **Valmis**.

> [!NOTE]
> Puhelinkeskustilauksissa järjestelmä näyttää varoitussanoman, joka muistuttaa, että käyttäjän on valittava painike **Laske uudelleen**, **Kokonaismäärät** tai **Valmis**, jotta tarkan hinnan ja alennuksen laskenta tehdään. Tilauksissa, joissa **Valmis**-painike on käytössä, puhelinkeskuskäyttäjä ei voi jättää pois tarkan hinnan ja alennuksen laskemista, koska hänen on valittava **Valmis** viimeistelläkseen tilauksen sieppauksen. Tilauksissa, joissa **Valmis**-painike ei ole käytössä, ei ole toimintoa, joka ilmaisee tilauksen sieppauksen valmistumista. Siksi on puhelinkeskuskäyttäjän vastuulla, että joko kohta **Laske uudelleen** tai **Kokonaismäärät** valitaan ennen kuin tilauksen sieppaus viimeistellään.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
