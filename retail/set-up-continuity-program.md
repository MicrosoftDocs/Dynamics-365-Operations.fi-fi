---
title: Aseta jatkuvuusohjelma puhelinpalvelukeskukselle
description: "Tässä artikkelissa kuvataan, miten voit määrittää jatkuvuusohjelman puhelinkeskukselle."
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: annbe
ms.search.scope: AX 7.0.0, Operations, Core, Retail
ms.custom: 16081
ms.assetid: 426a9be7-a931-4780-b372-e06f6083dd60
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: c0a9eec6bdf67deca885b30082b958869e64aae2
ms.contentlocale: fi-fi
ms.lasthandoff: 05/25/2017


---

# <a name="set-up-a-continuity-program-for-a-call-center"></a>Aseta jatkuvuusohjelma puhelinpalvelukeskukselle

[!include[banner](includes/banner.md)]


Tässä artikkelissa kuvataan, miten voit määrittää jatkuvuusohjelman puhelinkeskukselle.

Jatkuvuusohjelmassa, joka tunnetaan myös toistuvan tilauksen ohjelmana, asiakkaat saavat tavalliset tuotelähetykset ennalta määritetyn maksusuunnitelman mukaisesti. Jokainen lähetys voi sisältää eri tuotteen, kuten kuukauden kirja -klubissa tai sama tuote voidaan lähettää toistuvasti. Kun perustat jatkuvuusohjelman, tee seuraavat tehtävät:

1.  Määritä jatkuvuuden parametrit **Puhelinpalvelukeskuksen parametrit** -sivulla.
2.  Luo jatkuvuusohjelma, joka määrittää tiedot, kuten maksusuunnitelman, lähetysten ajoituksen ja sen tapahtuuko laskutus etukäteen. Sinun on myös lisättävä luettelo tuotteista, jotka on sisällytetty jatkuvuusohjelmaan. Jokainen tuote saa tapahtuman tunnusnumeron, joka määritetään järjestyksessä numerosta 1 alkaen. Tapahtumatunnus määrittää järjestyksen, jossa tuotteet lähetetään.
    -   Jos asiakkaat vastaanottavat eri tuotteen kussakin lähetyksessä, tuotteet lähetetään numerojärjestyksessä niiden tapahtumatunnusten mukaan ja alkaen nykyisestä tapahtumasta.
    -   Jos asiakkaat vastaanottavat saman tuotteen kussakin lähetyksessä, luettelo sisältää vain yhden tuotteen, jolla on yksi tapahtumatunnus. Sama tapahtuma toteutuu toistuvasti. Voit määrittää, kuinka monta kertaa jokainen tapahtuma toistetaan.

3.  Luo ylätason tuote, joka edustaa tehtävässä 2 luomaasi jatkuvuusohjelmaa. Jos lisäät tämän tuotteen myyntitilaukseen, **Jatkuvuus**-sivu avautuu. Tämän jälkeen voit käyttää tätä sivua luodaksesi varsinaisen jatkuvuustilauksen. Ylätason tuote ei määritä yksittäisiä tuotteita, jotka asiakas vastaanottaa jokaisessa toimituksessa.

Sen jälkeen kun olet määrittänyt jatkuvuusohjelman yllä kuvatulla tavalla, voit luoda jatkuvuustilauksen asiakkaalle. Saatat ehkä joutua suorittamaan myös seuraavat ylläpitotehtävät:

-   **Päivitä nykyinen jatkuvuustapahtuman kausi**– Määritä komentojonotyö, joka kertoo järjestelmälle, mikä nykyisen tapahtuman kausi on.
-   **Luo jatkuvuuden alitilauksia** – Luo alitilauksia ylätason jatkuvuustilauksesta.
-   **Käsittele jatkuvuuden maksut** – Käsittele laskutus ja maksuhuomautukset, jotka liittyvät jatkuvuuden myyntitilauksiin.
-   **Laajenna jatkuvuusrivejä tarvittaessa** (jos tarpeellista) – Lisää jatkuvuustapahtuman toistokertojen määrää. Lähetysten toisto voi jatkua asetettujen rajojen yli, jotka määritettiin **Jatkuvuuden toistuva kynnys** -kentässä puhelinkeskuksen parametreissä.
-   **Suorita jatkuvuuspäivitys** (tarvittaessa) – Synkronoi muutokset jatkuvuusohjelman ja jatkuvuuspäämyyntitilausten välillä.
-   **Sulje jatkuvuuden päärivit ja tilaukset** - Sulje jatkuvuustilaukset.





