---
title: Vahvista tuotantovirta ja versio
description: Tässä menettelyssä käsitellään, miten Lean-valmistuksen uusi tuotantovirta ja ensimmäinen versio luodaan.
author: ChristianRytt
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LeanProductionFlow
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4ae4c5f55d317a99e23ba6e76fc50ddece1e55a1
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/29/2019
ms.locfileid: "352847"
---
# <a name="validate-a-production-flow-and-version"></a>Vahvista tuotantovirta ja versio

[!include [task guide banner](../../includes/task-guide-banner.md)]

Tässä menettelyssä käsitellään, miten Lean-valmistuksen uusi tuotantovirta ja ensimmäinen versio luodaan. Edellytykset: Lean-valmistuksen tuotantoparametrit ja luokka-ajan mittayksiköt on määritettävä. Sinun on määritettävä arvovirta ja tuotantoryhmä. Lisätietoja Lean-valmistuksesta on teknisissä raporteissa, joissa voit tutustua tuotantovirta- ja tehtäväkäsitteisiin. Tämä menettely viittaa demotiedoissa USMF-yritykseen. Olettaen, että yritys on määritetty Lean-valmistukseen, muita yrityksiä voidaan käyttää.


## <a name="create-a-production-flow"></a>Luo tuotantovirta
1. Valitse Tuotannonhallinta > Asetukset > Lean-tuotantovirta > Tuotantovirrat.
2. Valitse Uusi.
3. Kirjoita arvo Nimi-kenttään.
4. Kirjoita arvo Kuvaus-kenttään.
5. Avaa haku valitsemalla Nimi-kentässä avattavan valikon painike.
6. Napsauta luettelossa valitulla rivillä olevaa linkkiä.
    * Arvovirta on toimintayksikkö, joka kattaa kaikki arvovirran toiminnot ja työnkulut.   Tässä vaiheessa toimintayksiköt on rajoitettu yritykseen eikä niillä ole muita toimintoja.  
7. Avaa haku napsauttamalla Tuotantoryhmä-kentässä avattavan valikon painiketta.
8. Napsauta luettelossa valitulla rivillä olevaa linkkiä.
    * Tuotantoryhmien avulla voi määrittää tuotantoprosessin materiaalin, työn ja KET-tilit. Tuotantovirran liittäminen kirjanpitokontekstiin edellyttää tuotantoryhmän valintaa.  
9. Valitse Tallenna.

## <a name="create-a-production-flow-version"></a>Luo tuotantovirran versio
1. ValitseLisää.
2. Anna päivämäärä ja kellonaika Vanhentumispäivä-kenttään.
    * Voit päivittää version, myös aktiivisten versioiden, vanhentumispäivän koska tahansa. Käytä version vanhentumista version käytöstäpoiston suunnitteluun.  
3. Valitse OK.
4. Merkitse valittu rivi luettelossa.
5. Kirjoita arvo Yksikkö-kenttään.
6. Valitse tahtiyksikkö.
7. Lisää Keskimääräinen tahtiaika -kenttään luku.
    * Tuotantovirran tahtiohjausta varten on määritettävä keskimääräinen tavoitetahtiaika.   Tahdin määritys on määrä/ajanjakso.  Esimerkissä tahtiaika on 10 kappaletta 0,2 tunnissa. Jos työaika on kahdeksan tuntia, päivittäinen työteho on silloin 400 kappaletta.  
8. Lisää Määrä sykliä kohden -kenttään luku.
9. Laajenna tai tiivistä Versiotiedot-osa.
10. Lisää Vähimmäistahtiaika-kenttään luku.
    * Vähimmäistahtiajan on oltava pienempi tai yhtä suuri kuin keskimääräinen tahtiaika.  
11. Lisää Enimmäistahtiaika-kenttään luku.
    * Enimmäistahtiajan on oltava suurempi tai yhtä suuri kuin keskimääräinen tahtiaika.  
12. Anna toteutuneen syklin keston päivinä.
    * Toteutunut syklin kesto on se määrä päiviä, jolloin töitä koostetaan toteutuneesta ajasta taaksepäin, jotta toteutunut syklin kesto voidaan laskea. Arvoa voidaan muuttaa koska tahansa ja sitä käytetään vain toteutuneiden syklien keston laskentaan.  
13. Valitse Tallenna.

