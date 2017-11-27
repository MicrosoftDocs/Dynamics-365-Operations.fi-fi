---
title: "Täydennys ja otto-kanbanit"
description: "Tässä ohjeaiheessa käsitellään, miten otto-kanbaneja käytetään valmistustehtävien materiaalitäydennykseen."
author: johanhoffmann
manager: AnnBe
ms.date: 06/16/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: KanbanBoardTransferJob, KanbanFlow, KanbanRules
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 011da8cd894cc044b6af8b740e49ed8d7c3c0c67
ms.contentlocale: fi-fi
ms.lasthandoff: 11/03/2017

---

# <a name="replenishment-with-withdrawal-kanbans"></a>Täydennys ja otto-kanbanit

[!include[banner](../includes/banner.md)]


Tässä ohjeaiheessa käsitellään, miten otto-kanbaneja käytetään valmistustehtävien materiaalitäydennykseen.

## <a name="workflow-for-material-replenishment-that-uses-the-withdrawal-kanban"></a>Otto-kanbania käyttävän materiaalitäydennyksen työnkulku
-------------------------------------------------------------------

Otto-kanbaneja voi käyttää yhden nimikkeen kanbanin siirtämiseen varastojen ja materiaalia kuluttavien tuotantosijaintien välillä. Otto-kanban tukee materiaalitäydennyksen imuohjausratkaisua, jossa imusignaali tarvitaan tarjonnan käynnistämiseen tietylle tarpeelle. 

Seuraavassa skenaariossa on imuohjattu täydennysjärjestelmä, jossa imusignaali käynnistää tuotantoprosessin täydennysmateriaalin kanbanin luonnin. 

[![Imusignaali käynnistää tuotantoprosessin täydennysmateriaalin kanbanin luonnin](./media/material-replenishment-with-withdrawal-kanban.png)](./media/material-replenishment-with-withdrawal-kanban.png)

1.  Otto-kanban
2.  Varastotyön kanbanin lähtö- ja poispanosijainti
3.  Kanbanin kohdesijainti ja tuotannon varastosijainti
4.  Valmistusprosessi
5.  Kanban-keräilyn varastotyö
6.  Raaka-aineen varastosijainnit
7.  Materiaalivarasto
8.  Valmistuksen varasto

Tässä skenaariossa valmistusprosessi (4) kuluttaa materiaalia tuotannon varastosijainnista (3) valmistuksen varastossa (8). Kun materiaalin käsittely-yksikköä (kanbania) kulutetaan, se rekisteröidään tyhjäksi. Nimikkeen alkuperälle luodaan täydennyssignaali ja uusi kanban (1) luodaan. Tässä tapauksessa nimikkeen alkuperä koostuu materiaalivaraston sijainneista (7). Kanbanin materiaali kerätään ja pannan pois saman varaston sijaintiin (2). Kun materiaali kerätään, se on valmis siirrettäväksi sijainnista 2 tuotannon varastosijaintiin (3) valmistuksen varastossa (8).

## <a name="configure-warehouse-work-for-kanban-picking-for-the-withdrawal-kanban"></a>Otto-kanbanin kanban-keräilyn varastotyön määrittäminen

Voit ottaa otto-kanbanin raaka-aineen keräilyn käyttöön määrittämällä **Kanban-keräilyn** työtilaustyypin aaltomallit, työmallit ja sijaintidirektiivit. Tämä työtilaustyyppi ei tue vain otto-kanbanin keräilyprosessia. Se tukee myös valmistus-kanbanin keräilyprosessia. Voit kuitenkin määrittää kummallekin kanban-tyypille erillisen keräilyprosessin erottamalla aaltomallit, työmallit ja sijaintidirektiivit. Voit erottaa aaltomallit, työmallit ja sijaintidirektiivit määrittämällä ehdot kyseisten yksikköjen kyselyjen tehtävätyypissä (**Prosessi** tai **Siirto**).

## <a name="configure-the-withdrawal-kanban"></a>Otto-kanbanin määrittäminen

Otto-kanbanissa käytettävä siirtotehtävä määritetään aktivoidun tehtäväsuunnitelman osana Lean-tuotantovirrassa. Siirtotehtävän määrityksen osana määritetään myös siirron lähtö- ja kohdesijainnit. Kun siirtotehtävä on määritetty, voit määrittää sille **Otto**-tyypin kanban-säännön. Kanban-sääntö määrittää otto-kanbanin käytännöt ja määritykset. Kanbanin määrä määrittää, kuinka monta materiaalin käsittely-yksikön yksikköä kanban siirtää siirtoprosessin aikana. Kiinteää kanban-määrää käytetään, kun valittuna on kiinteä täydennysstrategia. Määrä määrittää, kuinka monta kanbania tarvitaan, jotta varasto ei lopu kysynnän lähteessä. Kiinteä määrä voidaan laskea todellisen kysynnän, historiallisen kysynnän ja palvelutasojen perusteella. Kahdessa seuraavassa skenaariossa kerrotaan, miten voit hallita otto-kanbania käyttävää materiaalitäydennystä.

## <a name="scenario-1-replenish-a-production-input-location-by-using-a-fixed-withdrawal-kanban"></a>Skenaario 1: Tuotannon varastointisijainnin täydentäminen kiinteän otto-kanbanin avulla

Valmistusprosessi kuluttaa ostettua raaka-ainetta tuotannon varastosijainnista, joka sijaitsee tuotantovarastossa. Kun raaka-aine vastaanotetaan toimittajalta, se varastoidaan materiaalivaraston sijainteihin. Koska materiaalin kysyntä katsotaan olevan vakaa kauden aikana, se määritetään tuotannon toimittajaksi kiinteämääräisellä kanban-työnkululla. Kun kanban on kulutettu tuotannon varastointisijainnissa, tyhjän signaali rekisteröidään ja uusi samantyyppinen kanban lisätään työnkulkuun. 

Tyhjän signaali voidaan määrittää tapahtumaan automaattisesti, kun kanban on valmis. Tyhjän signaali voidaan vaihtoehtoisesti määrittää manuaaliseksi vuorovaikutukseksi, joka annetaan joko kanban-siirron taulusta tai kämmenlaitteen valikosta. Kanban-siirron taulu on työtila, jossa hallitaan kaikkia kanban-elinkaaren tehtäviä. 

Kanbania luotaessa raaka-aineen aaltorivi lisätään materiaalivaraston kanban-aaltoon. Kanban-siirron taulun keräysluettelo-osassa voi seurata materiaalin ja liittyvien varastoprosessien tilaa aallon luonnista työn luontiin siihen saakka, että materiaali on varastossa siirron lähtösijainnissa ja valmis siirrettäväksi tuotannon varastointisijainteihin. Kanban voidaan suorittaa joko kanban-siirron taulusta tai kämmenlaitteen valikosta. 

Tässä skenaariossa materiaalivaraston keräystyö käsitellään yhtenä tehtävänä. Materiaalivaraston ja tuotannon varastoinnin sijainnin välinen siirtotehtävä käsitellään erillisenä tehtävänä. Tällä voi olla kätevä toimintatapa, jos esimerkiksi kahden varaston välinen etäisyys on suuri. Siinä tapauksessa kanban-siirtotehtävä voi vastata kuorma-auton kuormaa. 

Jos varastosijainnit ja tuotannon varastoinnin sijainnit eivät ole kaukana toisistaan, siirtotehtävä kannattaa ehkä sisällyttää keräilyprosessiin. Se voidaan sitten materiaalin keräilyn jälkeen asettaa suoraan tuotannon varastoinnin sijaintiin. Voit tukea tätä prosessia määrittämällä siirtotehtävän siten, että se valmistuu automaattisesti, kun otto-kanbanin keräystyö on käsitelty.

## <a name="scenario-2-automatically-complete-the-transfer-activity-when-kanban-picking-work-is-processed"></a>Skenaario 2: Siirtotehtävän valmistuminen automaattisesti, kun kanban-keräystyö on käsitelty

Seuraavassa skenaariossa otto-kanbanin siirtotehtävä on määritetty siirtymään kahden sijainnin välillä samassa varastossa. Otto-kanbanin siirtotehtävä on määritetty siten, että se valmistuu automaattisesti. 

[![Siirtotehtävä valmistuu automaattisesti, kun kanban-keräystyö käsitellään](./media/transfer-activities-when-processing-kanban-picking.png)](./media/transfer-activities-when-processing-kanban-picking.png)

1.  Raaka-aineiden ja tuotannon jaettu varasto
2.  Raaka-aineiden varastosijainnit
3.  Varastotyön kanbanin lähtö- ja poispanosijainti
4.  Otto-kanban
5.  Tuotannon varastointisijainti
6.  Valmistusprosessi

Kun kanban on kulutettu tuotannon varastointisijainnissa, kanban ilmoitetaan tyhjäksi ja uusi kanban lisätään työnkulkuun. Kanbania luotaessa kanban-aaltoon lisätään aaltorivi. Kun kanban-aalto käsitellään, kanban-keräilylle luodaan varastotyö. Varastotyöntekijä käsittelee kanban-keräilyn työn, ja työ ohjaa hänet keräämään kanbanin materiaalin varastosijainnissa. Kun tämä varastotyöntekijä vahvistaa keräilyn, kanban valmistuu automaattisesti ja varastotyöntekijä ohjataan sijoittamaan materiaali tuotannon varastoinnin sijaintiin.


