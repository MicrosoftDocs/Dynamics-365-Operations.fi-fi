--- 
title: "Määritä tuotantovirtamallit"
description: "Tuotantovirran malleissa käsitellään, miten Lean-valmistuksen työsolujen kapasiteetti lasketaan ja miten sitä ylläpidetään."
author: cvocph
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 7850a121ca06f25f6c532e49e18c0b6811bd7455
ms.contentlocale: fi-fi
ms.lasthandoff: 09/29/2017

---
# <a name="define-production-flow-models"></a>Määritä tuotantovirtamallit

[!include[task guide banner](../../includes/task-guide-banner.md)]

Tuotantovirran malleissa käsitellään, miten Lean-valmistuksen työsolujen kapasiteetti lasketaan ja miten sitä ylläpidetään. Tuotantovirran malli onkin määritettävä ennen työsolujen määrittämistä. Tämän menettelyn luomisessa käytetty esittely-yritys on USMF.


## <a name="define-a-production-flow-model"></a>Määritä tuotantovirran malli. 
1. Valitse Tuotannonhallinta > Asetukset > Lean-tuotantovirta > Tuotantovirtamallit.
2. Valitse Uusi.
3. Kirjoita Tuotantovirtamalli-kenttään tuotantovirtamallin tunnus.
4. Valitse vaihtoehto Mallityyppi-kentässä.
    * Mallityyppejä on kaksi: Tuotantokapasiteetti ja Tunnit. Tuotantokapasiteetti-tyypissä tätä tuotantovirtamallia käyttävien työsolujen kapasiteetti ilmaistaan ja lasketaan tuotemäärinä. Tunnit-tyypissä tätä tuotantovirtamallia käyttävien työsolujen kapasiteetti ilmaistaan ja lasketaan tunteina. Huomaa, että tätä ominaisuutta ei voi muuttaa aiemmin luodussa tuotantovirtamallissa. Tuotantovirtamallin tyyppiä ei voi muuttaa, kun työsolussa on kapasiteetin varauksia.  
5. Anna EPE-syklin päivien määrä.
    * Aikaväli tarkoittaa ajanjaksoa, jolloin tuotantovirran tai työsolun jokainen osa tuotetaan vähintään kerran. Mitä lyhyempi EPE-sykli on, sitä joustavampi tuotantoprosessi on. Jos EPE-sykli = 0, koko kysyntä voidaan tuottaa samana päivänä. Lean-prosessin töitä ajoitetaan EPE-syklin avulla. Kun työsoluun ajoitetaan työ, jonka EPE-sykli = 5, ajoitusprosessi etsii työsolusta kapasiteettia kaavalla Määräpäivä–EPE-sykli (5 päivää ennen määräpäivää). Näin varmistetaan, että tuote voidaan tuottaa kyseisessä syklissä. Tuotteen varaston läpimenoaika on yleensä yhtä suuri tai suurempi kuin liittyvän tuotantoprosessin EPE-sykli.  
6. Valitse vaihtoehto Suunnittelukauden tyyppi -kentässä.
    * Suunnittelukauden tyyppiä ei voi muuttaa, kun työsolussa on kapasiteetin varauksia. Voit valita annetulle työsolulle vain tuotantovirran malleja, joilla on sama kausityyppi.  
7. Lisää Suunnittelun aikarajat -kenttään numero.
    * Suunnittelun aikaraja määrittää, kuinka monen päivän kapasiteetin varauksia liittyvissä työsoluissa voidaan tehdä. Anna Suunnittelun aikarajat -kohdassa päivien määrä.   Tämän kauden ulkopuolisia kanban-prosessitöitä ei suunnitella automaattisella suunnitelulla. Suunnittelun aikaraja on yleensä kaksinkertainen tuotantovirrassa tai työsolussa tuotettujen töiden keskimääräiseen varaston läpimenoaikaan verrattuna. EPE-sykli saa olla enintään puolet suunnittelun aikarajasta.     
8. Valitse Kapasiteetin puutteen aiheuttama reaktio -kentässä vaihtoehto.
    * Vaihtoehdot: Lykkää – koko ajoitustapahtuman kysyntä lykätään seuraavaan käytettävissä olevaan päivään, jossa on tuotantokapasiteettia. Peruuta – ajoitustapahtuman automaattinen suunnittelu lopetetaan eikä liittyviä töitä suunnitella.   Lisää pyydettyyn päivämäärään – Pyydetyn kauden pyydetyt työt suunnitellaan. Kyseisen päivän solu ylikuormittuu ja edellyttää, että suunnittelija tarkistaa ja tee manuaalisia toimintoja.   Jaa käytettävissä oleville kausille – Ajoitustapahtuman eri työt jaetaan kaikille käytettävissä oleville tuotantopäiville alkaen ensimmäisestä käytettävissä olevasta päivästä. Kanban-työn määrä on pienin jaettava määrä. Jakelu määrittää vähimmäissuunnittelumäärän (kanban-määrän) jokaiselle päivälle, jossa on riittävästi vapaata tuotantokapasiteettia.  


