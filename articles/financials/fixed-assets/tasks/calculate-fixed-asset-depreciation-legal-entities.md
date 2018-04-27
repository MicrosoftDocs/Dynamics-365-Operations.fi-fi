--- 
title: "Käyttöomaisuuden poistojen laskenta eri yrityksissä"
description: "Näissä ohjeissa kerrotaan, miten poistoprosessi määritetään ja suoritetaan useille yrityksille."
author: saraschi2
manager: AnnBe
ms.date: 11/02/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: d804480167414cd038f8229db312dc9c52d131f8
ms.openlocfilehash: 4c45da124136b7fecb916d2ff9098c8ffeff6cb1
ms.contentlocale: fi-fi
ms.lasthandoff: 11/02/2017

---
# <a name="calculate-fixed-asset-depreciation-across-legal-entities"></a>Käyttöomaisuuden poistojen laskenta eri yrityksissä

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

Käyttöomaisuuden poisto voidaan suorittaa useille yritykselle yhdellä kertaa. Näissä ohjeissa kerrotaan, miten prosessi määritetään ja suoritetaan useille yrityksille. Prosessissa käytetään kirjanpitäjän roolia.  

Tässä tallenteessa käytetään esittely-yritystä USMF.


Vaiheiden (16) alitehtävä: Määritä yritysten väliset poistoajon kirjauskansiot. 

1. Ensin määritetään kirjauskansiot, joita käytetään yritysten välisessä poistoajossa jokaisessa yrityksessä. Siirry kohtaan Käyttöomaisuus > Asetukset > Käyttöomaisuuden parametrit. 
2. Laajenna Käyttöomaisuuden ehdotukset -osa. 
3. Luo tietue, jolla on kirjauskansion nimi. Sitä käytetään yrityksen jokaisella kirjanpitotasolla. Jos kirjoja ei kirjata kirjanpitoon, liitettylle kirjauskansiolle valitaan Ei mitään -kirjanpitotaso. ValitseLisää. 
4. Syötä tai valitse arvo Kirjanpitotaso-kenttään. 
5. Syötä tai valitse arvo Kirjauskansion nimi -kentässä. 
6. Toista kirjauskansion asetukset kunkin yrityksen Käyttöomaisuuden parametrit -sivulla. 

Alitehtävä: Poiston laskeminen

1. Aloita poistoajo yrityksissä Poistoehdotuksen luominen -sivulla. Siirry kohtaan Käyttöomaisuus > Kirjauskansioviennit > Luo poistoehdotus. 
2. Syötä tai valitse arvo Kirjanpitotaso-kenttään. 
3. Kirjauskansion nimen oletusarvo saadaan käyttömaisuuden parametreista. Nykyisen yrityksen kirjauskansion nimi voidaan vaihtaa tässä. 
4. Kirjoita päivämäärä Päivämäärään-kenttään. 
5. Valitse poistoajoon sisällytettävät yritykset. Luettelo sisältää vain yritykset, joiden kirjauskansiot on määritetty Käyttöomaisuuden parametrit -sivun Käyttöomaisuuden ehdotukset -osassa. 
6. Kun tämä vaihtoehto on käytössä, Kirjaa kirjauskansiot -vaihtoehto kirjaa poistokirjauskansiot automaattisesti niiden luomisen yhteydessä. Kun vaihtoehtoa ei ole valittu, kirjauskansiot luodaan, mutta niitä ei kirjata. Voit siis tarkistaa tiedot ennen kirjaamista. Valitse Kirjaa kirjauskansiot -kentässä Kyllä. 
7. Kenttien suodattaminen sisältää kaiken yrityksen käyttöomaisuuden ja kaikki yrityksen ryhmät ja kirjat, jotka on valittu tähän poistoajoon. 
8. Eräkäsittely-vaihtoehto on käytössä oletusarvoisesti. Kun tämä vaihtoehto on käytössä, poistokirjauskansion luominen ja kirjaaminen suoritetaan taustalla. 
9. Valitse Luo kirjauskansio. 
10. Yrityksissä luodut poistokirjauskansiot on tarkistettava. Valitse Käyttöomaisuus > Kirjauskansioviennit > Käyttöomaisuuden kirjauskansio.

