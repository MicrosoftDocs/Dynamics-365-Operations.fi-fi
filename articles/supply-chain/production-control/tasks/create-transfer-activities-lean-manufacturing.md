---
title: Lean-valmistuksen siirtotehtävien luominen
description: Luo Lean-valmistuksen siirtotehtävä.
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
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 629acdebd321154873feddcdfd8555d33e931f4f
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/15/2021
ms.locfileid: "4996823"
---
# <a name="create-transfer-activities-for-lean-manufacturing"></a>Lean-valmistuksen siirtotehtävien luominen

[!include [banner](../../includes/banner.md)]

Luo Lean-valmistuksen siirtotehtävä. 

Edellytykset: 

1. On välttämätöntä luoda tuotantovirta ja versio, jotka eivät ole aktiivisia.

2. Lähtö- ja kohdevarasto ja sijainnit on luotava. Työsolun täydentäminen tai täydennetyn työsolun luominen on valinnaista.


## <a name="find-the-production-flow-version"></a>Etsi tuotantovirran versio
1. Valitse Tuotannonhallinta > Asetukset > Lean-tuotantovirta > Tuotantovirrat.
2. Etsi haluamasi tietue luettelosta ja valitse se.
    * Huomaa, että tuotantovirran version on oltava luonnostilassa.  
3. Napsauta luettelossa valitulla rivillä olevaa linkkiä.

## <a name="create-a-new-activity"></a>Luo uusi tehtävä
1. Valitse Tehtävät.
    * Varmista, että valitulla tuotantovirralla on luonnostilassa oleva versio ja valitse se.  
2. Valitse Luo uusi suunnitelman tehtävä.
3. Valitse Seuraava.
4. Kirjoita arvo Nimi-kenttään.
5. Valitse Tehtävätyyppi-kentässä Siirto.
6. Lisää Prosessin määrä -kenttään numero.
7. Valitse Seuraava.

## <a name="select-the-work-cells"></a>Valitse Työsolut
1. Avaa haku napsauttamalla Täydennetään-kentässä avattavan valikon painiketta.
    * Valitse työsolu, jos haluat käyttää työsolun tuotossijaintia siirtotehtävän lähtösijaintina. Sama voidaan tehdä täydennetyllä työsolulla, joka määrittää siirtotehtävän kohdesijainnin.  
2. Napsauta luettelossa valitulla rivillä olevaa linkkiä.

## <a name="define-the-inventory-updates"></a>Määritä varastopäivitykset
1. Valitse vaihtoehto Tuotetyyppi-kentässä.
    * Huomaa, että siirto ei vaihda tuotteen tyyppiä. Voit siirtää valmiita tai puolivalmiita tuotteita (kahden tuotantovirran tehtävän ja mahdollisen kanban-työnkulun välisen siirto).     Voit valita valmiita tuotteita siirrettäessä, jos tulosten kerääminen tai vastaanottaminen on varastotapahtuma.  

## <a name="define-the-transfer-locations"></a>Määritä siirtosijainnit
1. Valitse Seuraava.
2. Avaa haku valitsemalla Varasto-kentässä avattavan valikon painike.
3. Etsi haluamasi tietue luettelosta ja valitse se.
4. Napsauta luettelossa valitulla rivillä olevaa linkkiä.
5. Avaa haku valitsemalla Sijainnit-kentässä avattavan valikon painike.
6. Napsauta luettelossa valitulla rivillä olevaa linkkiä.
7. Valitse Rahdinkuljettaja-kentässä Huolitsija.
    * Vaihtoehdot: Huolitsija – lähetysvarastoa käyttävä organisaatio, Vastaanottaja – vastaanottovarastoa käyttävä organisaatio ja Rahdinkuljettaja – ulkopuolinen toimittaja. Jos käyttävä organisaatio on toimittaja, siirtotehtävä edellyttää alihankintasopimuksen.  
8. Valitse Seuraava.

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



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]