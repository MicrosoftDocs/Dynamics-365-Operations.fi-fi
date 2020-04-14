---
title: Lean-valmistuksen alihankintatyösolun luominen
description: Kun haluat mallintaa alihankkijalle annetun lean-valmistuksen työn, luo työsolu, joka on liitetty työn tarjoavaan toimittajaan.
author: cvocph
manager: AnnBe
ms.date: 06/23/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: conradv
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 03fcc62236b14a8721a4cb611978e8672ae77ea3
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/18/2020
ms.locfileid: "3146925"
---
# <a name="create-a-subcontracted-work-cell-for-lean-manufacturing"></a>Lean-valmistuksen alihankintatyösolun luominen

[!include [banner](../../includes/banner.md)]

Kun haluat mallintaa alihankkijalle annetun lean-valmistuksen työn, luo työsolu, joka on liitetty työn tarjoavaan toimittajaan. Alihankinnan työsolu linkitetään toimittajaan Toimittaja-tyyppisen resurssin liitoksen kautta. Jos tämä tallenne toistetaan USMF-demoyrityksessä, voit valita toimittajan tilin, jonka tunnus on 1002, ja toimipaikan 1.


## <a name="create-a-vendor-resource"></a>Luo toimittajan resurssi
1. Siirry Resurssit-kohtaan.
2. Valitse Uusi.
3. Kirjoita arvo Resurssi-kenttään.
4. Kirjoita arvo Kuvaus-kenttään.
5. Valitse Tyyppi-kenttään Toimittaja.
6. Avaa haku valitsemalla Toimittaja-kentässä avattavan valikon painike.

## <a name="create-the-resource-group"></a>Luo resurssiryhmä
1. Siirry Resurssiryhmät-kohtaan.
2. Valitse Uusi.
3. Kirjoita arvo Resurssiryhmä-kenttään.
4. Kirjoita arvo Kuvaus-kenttään.
5. Avaa haku napsauttamalla Toimipaikka-kentässä avattavan valikon painiketta.
    * Valitse toimipaikka, johon työsolu kohdistetaan. Teoriassa toimipaikka voi edustaa yksittäistä toimittajan toimipaikkaa. Kuitenkin suurimmassa osassa tapauksia alihankinnan resurssit kohdistetaan toimipaikkaan, joka on tilannut alihankkijalle annetun työn. Ota huomioon, että alihankinnan työsolujen syöttö- ja tuotosvaraston on oltava samassa toimipaikassa.  
6. Kirjoita arvo Toimipaikka-kenttään.
7. @SysTaskRecorder:_RequestClose
8. Valitse Työsolu-valintaruutu tai poista valintaruudun valinta.
9. Avaa haku napsauttamalla Syöttövarasto-kentässä avattavan valikon painiketta.
    * Valitse varasto ja sijainti, joita käytetään materiaalin paikkana toimittajan hallitsemassa työsolussa. Useissa tapauksissa varasto ja sijainti voidaan mallintaa käyttämällä erillistä varastoa toimittajaa kohti ja yhtä sijaintia työsolua kohti.  
10. Avaa haku napsauttamalla Syöttösijainti-kentässä avattavan valikon painiketta.
11. Avaa haku napsauttamalla Tuotosvarasto-kentässä avattavan valikon painiketta.
    * Määritä varasto ja sijainti, jonne materiaali kirjataan, kun työsolun alihankintatehtävät kirjataan. Varasto ja sijainti voivat olla toimittajan toimipaikassa, jos toimittaja raportoi kanban-työt. Vaihtoehtoisesti varasto ja sijainti voivat olla vastaanottosijainnissa, joka on liitetty tuotantovirran seuraavaan vaiheeseen.  
12. Avaa haku napsauttamalla Tuotossijainti-kentässä avattavan valikon painiketta.
13. Laajenna tai tiivistä Kalenterit-osa.
14. ValitseLisää.
15. Avaa haku valitsemalla Kalenteri-kentässä avattavan valikon painike.
    * Liitä työsolun työaikakalenteri resurssiryhmään. Kriittisiä resursseja varten kannattaa määrittää erityiset kalenterit, jotka edustavat tarkkoja työaikoja ja työsolun tai toimittajan toimipaikan liittyviä kapasiteetteja.  
16. Laajenna tai tiivistä Resurssit-osa.
17. ValitseLisää.
    * Alihankinnan resurssiryhmällä on oltava liitetty resurssi, jonka tyyppi on Toimittaja. Se linkittää resurssiryhmän toimittajan tiliin.  
18. Avaa haku valitsemalla Resurssi-kentässä avattavan valikon painike.
    * Valitse tai syötä edellisessä alitehtävässä luotu toimittajan resurssi.  
19. Laajenna tai tiivistä Työsolun kapasiteetti -osa.
20. ValitseLisää.
    * Työsolulle on määritettävä kapasiteetti. Tässä esimerkissä luodaan 100 kappaleen tuotantoteho tavallista työpäivää kohti.  
21. Avaa haku napsauttamalla Tuotantovirtamalli-kentässä avattavan valikon painiketta.
22. Valitse vaihtoehto Kapasiteettikausi-kentässä.
23. Lisää Tuotantokapasiteetin keskimääräinen määrä -kenttään numero.
24. Avaa haku napsauttamalla Yksikkö -kentässä avattavan valikon painiketta.
25. Ratkaise muutokset yksikössä.

