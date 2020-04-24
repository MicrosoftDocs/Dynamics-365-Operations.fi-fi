---
title: Lean-valmistuksen prosessitehtävien luominen
description: Luo Lean-valmistuksen prosessitehtävä.
author: cvocph
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LeanProductionFlow, PlanActivity, PlanActivityWizard, LeanWorkCellLookup, InventLocationIdLookup
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: dc93f3f696f470d7e2f174bd3342f0877e0b4e74
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/02/2020
ms.locfileid: "3212155"
---
# <a name="create-process-activities-for-lean-manufacturing"></a>Lean-valmistuksen prosessitehtävien luominen

[!include [banner](../../includes/banner.md)]

Luo Lean-valmistuksen prosessitehtävä. 

Edellytykset: 

1. On välttämätöntä luoda tuotantovirta ja versio, jotka eivät ole aktiivisia.

2. Työsolu on luotava.


## <a name="find-the-production-flow-version"></a>Etsi tuotantovirran versio
1. Valitse Tuotannonhallinta > Asetukset > Lean-tuotantovirta > Tuotantovirrat.
2. Etsi haluamasi tietue luettelosta ja valitse se.
3. Napsauta luettelossa valitulla rivillä olevaa linkkiä.

## <a name="create-a-new-activity"></a>Luo uusi tehtävä
1. Valitse Tehtävät.
    * Varmista, että valitulla tuotantovirralla on luonnostilassa oleva versio ja valitse se.  
2. Valitse Luo uusi suunnitelman tehtävä.
3. Valitse Seuraava.
4. Kirjoita arvo Nimi-kenttään.
5. Kirjoita arvo Nimi-kenttään.
    * Huomaa, että tietyn tuotantovirran kaikilla versioilla on oltava yksilöllinen nimi.  
6. Lisää Prosessin määrä -kenttään numero.
    * Huomaa, että käsiteltävästä työmäärästä riippumatta tämä on työkohtainen vähimmäismäärä työkustannusten laskentaan. Jos työmäärät poikkeavat tästä määrästä, työkustannuspoikkeama luodaan.  
7. Valitse Seuraava.

## <a name="select-the-work-cell"></a>Valitse työsolu
1. Avaa haku valitsemalla Työsolu-kentässä avattavan valikon painike.
2. Napsauta luettelossa valitulla rivillä olevaa linkkiä.

## <a name="define-the-inventory-updates"></a>Määritä varastopäivitykset
1. Valitse Päivitä käytettävissä olevan varaston vastaanotto -valintaruutu tai poista sen valinta.
    * Jos Päivitä käytettävissä oleva varasto -arvona on Ei, voit määrittää tehtävän vastaanottamaan puolivalmiin tuotteen. (Tehtävä ei tavoita seuraavaa tuoterakennetasoa.)    Voit myös valita puolivalmiiden tuotteiden kulutuksen.  

## <a name="define-the-picking-activities"></a>Määritä keräystehtävät
1. Valitse Seuraava.
2. Merkitse valittu rivi luettelossa.
    * Oletuskeräystehtävä luodaan valitun työsolun syöttösijaintiin.  
3. ValitseLisää.
    * Voit luoda tietyille tuotteille lisäkeräystehtäviä, joita ei vaiheisteta työsolun syöttötehtävässä.  
4. Etsi haluamasi tietue luettelosta ja valitse se.
5. Kirjoita arvo Nimiketunnus-kenttään.
6. Avaa haku valitsemalla Varasto-kentässä avattavan valikon painike.
    * Tällä määrityksellä kaikki tehtävässä kulutetut materiaalit kerätään oletussyöttövarastosta ja -sijainnista lukuun ottamatta toisessa keräystehtävässä määritettyä nimikettä. Tämä nimike kerätään eri varastoista ja sijainnista.  
7. Etsi haluamasi tietue luettelosta ja valitse se.
8. Napsauta luettelossa valitulla rivillä olevaa linkkiä.
9. Valitse Rekisteröi hävikki -valintaruutu tai poista sen valinta.
10. Valitse Seuraava.

## <a name="define-the-activity-times"></a>Määritä tehtäväajat
1. Etsi haluamasi tietue luettelosta ja valitse se.
    * Suorituksenaikainen kohde on määritettävä. Suorituksenaikaisella kohteella lasketaan kanban-töiden kustannukset ja läpimenoajat. Suorituksenaikaisia kohteita ei käytetä kapasiteetin kuormituksen ja kulutuksen laskentaan, sillä ne lasketaan tuotantovirran versiotehtävästä johdetusta syklin kestosta.  
2. Lisää Aika-kenttään numero.
3. Kirjoita arvo Yksikkö-kenttään.
4. Valitse Aikayksikkö.
5. Lisää Määrää kohden -kenttään numero.
6. Etsi haluamasi tietue luettelosta ja valitse se.
    * Jonotusajat ovat valinnaisia  
7. Lisää Aika-kenttään numero.
8. Kirjoita arvo Yksikkö-kenttään.
9. Valitse Aikayksikkö.
10. Lisää Määrää kohden -kenttään numero.
11. Valitse Seuraava.
12. Valitse Valmis.
13. Sulje sivu.

