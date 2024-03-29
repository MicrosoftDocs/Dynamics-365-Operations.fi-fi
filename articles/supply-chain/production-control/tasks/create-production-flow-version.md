---
title: Luo tuotantovirran versio
description: Tässä menettelyssä selvitetään uuden tuotantovirtaversion luomista.
author: johanhoffmann
ms.date: 11/03/2017
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5b72d6162edd0ae6ccbfdcfe3e63ecff30528454
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/29/2021
ms.locfileid: "7569257"
---
# <a name="create-a-production-flow-version"></a>Luo tuotantovirran versio

[!include [banner](../../includes/banner.md)]

Tässä menettelyssä selvitetään uuden tuotantovirtaversion luomista. Tässä menettelyssä Lean-valmistuksen tuotantoparametrit ja luokka-ajan mittayksiköt on määritettävä. Myös arvovirta ja tuotantoryhmä on määritettävä. Lisätietoja Lean-valmistuksen tuotantovirroista ja tehtävistä on Microsoft Dynamics AX:n Lean-valmistusta käsittelevissä teknisissä raporteissa. Tämän menettelyn luomisessa käytetty esittely-yritys on USMF.


## <a name="create-a-production-flow"></a>Luo tuotantovirta
1. Valitse Tuotannonhallinta > Asetukset > Lean-tuotantovirta > Tuotantovirrat.
2. Valitse Uusi.
3. Kirjoita arvo Nimi-kenttään.
4. Kirjoita arvo Kuvaus-kenttään.
5. Avaa haku valitsemalla Nimi-kentässä avattavan valikon painike.
6. Napsauta luettelossa valitulla rivillä olevaa linkkiä.
    * Valitse toimintayksikön tyypiksi arvovirta. Arvovirta on toimintayksikkö, joka kattaa kaikki arvovirran toiminnot ja työnkulut. Tässä vaiheessa toimintayksiköt on rajoitettu yritykseen eikä niillä ole muita toimintoja.  
7. Avaa haku napsauttamalla Tuotantoryhmä-kentässä avattavan valikon painiketta.
8. Napsauta luettelossa valitulla rivillä olevaa linkkiä.
    * Valitse tuotantovirran tuotantoryhmä. Tuotantoryhmien avulla voi määrittää tuotantoprosessin materiaalin, työn ja KET-tilit. Tuotantovirran liittäminen kirjanpitokontekstiin edellyttää tuotantoryhmän valintaa.  
9. Valitse Tallenna.

## <a name="create-a-production-flow-version"></a>Luo tuotantovirran versio
1. ValitseLisää.
2. Anna päivämäärä ja kellonaika Vanhentumispäivä-kenttään.
    * Määritä tarvittaessa version vanhentumispäivä. Voit päivittää sen koska tahansa myös aktiivisissa versioissa. Voit suunnitella sen avulla version käytöstä poistamisen.  
3. Valitse OK.
4. Merkitse valittu rivi luettelossa.
5. Kirjoita arvo Yksikkö-kenttään.
6. Ratkaise muutokset tahtiyksikössä
7. Lisää Keskimääräinen tahtiaika -kenttään luku.
    * Määritä version keskimääräinen tahtiaika. Tuotantovirran tahtiohjausta varten on määritettävä keskimääräinen tavoitetahtiaika. Tahdin määritys on määrä/ajanjakso. Esimerkissä tahtiaika on 10 kappaletta 0,2 tunnissa. Jos työaika on kahdeksan tuntia, päivittäinen työteho on silloin 400 kappaletta.  
8. Lisää Määrä sykliä kohden -kenttään luku.
    * Määritä keskimääräiseen tahtiaikaan liittyvä jaksottainen määrä.  
9. Ota käyttöön Versiotiedot-osan laajennus.
10. Lisää Vähimmäistahtiaika-kenttään luku.
    * Määritä vähimmäistahtiaika. Vähimmäistahtiajan on oltava pienempi tai yhtä suuri kuin keskimääräinen tahtiaika.  
11. Lisää Enimmäistahtiaika-kenttään luku.
    * Enimmäistahtiajan on oltava suurempi tai yhtä suuri kuin keskimääräinen tahtiaika.  
12. Lisää Toteutunut syklin kesto (päivinä) -kenttään luku.
    * Anna toteutuneen syklin keston päivien määrä. Toteutunut syklin kesto on se määrä päiviä, jolloin töitä koostetaan toteutuneesta ajasta taaksepäin, jotta toteutunut syklin kesto voidaan laskea. Arvoa voidaan muuttaa koska tahansa ja sitä käytetään vain toteutuneiden syklien keston laskentaan.  
13. Valitse Tallenna.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]