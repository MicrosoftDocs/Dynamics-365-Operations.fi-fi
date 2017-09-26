---
title: "Varaston kokonaismäärän laskeminen"
description: "Tässä menettelyssä käsitellään varaston inventointikirjauskansion luonti- ja kirjausprosessi, jolla voidaan inventoida tietty nimike varastosijainnissa."
author: MarkusFogelberg
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mafoge
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 9b947a02be981155053e33a4ef20e19bf2a194a5
ms.openlocfilehash: 1d2ecf1cd80e05b59f206fb5f684d6a86fa5733e
ms.contentlocale: fi-fi
ms.lasthandoff: 07/27/2017

---
# <a name="count-inventory-in-a-warehouse"></a>Varaston kokonaismäärän laskeminen

[!include[task guide banner](../../includes/task-guide-banner.md)]

Tässä menettelyssä käsitellään varaston inventointikirjauskansion luonti- ja kirjausprosessi, jolla voidaan inventoida tietty nimike varastosijainnissa. Menettely koskee Inventoinnin- ja varastonhallinta -moduulin varastoinnin perustoimintoja. Se ei koske Varastonhallinta-moduulin varastointitoimintoja. Voit käydä tämän menettelyn läpi emotietojen yrityksen USMF avulla tai käyttää omia tietojasi. Jos käytät omia tietoja, varmista, että olet määrittänyt tuotteita ja sijainteja ja että olet luonut inventointikirjauskansioille varastokirjauskansion. Varastoinventoinnin suorittaa tavallisesti varastotyöntekijä.


## <a name="create-an-inventory-counting-journal"></a>Luo varaston inventointikirjauskansio
1. Valitse Inventoinnin- ja varastonhallinta > Kirjauskansioviennit > Inventointi > Inventointi.
2. Valitse Uusi.
3. Avaa haku valitsemalla Nimi-kentässä avattavan valikon painike.
4. Valitse luettelosta käytettävä varaston inventointikirjauskansio
    * Joidenkin kenttien tiedot voidaan lisätä valitsemasi varaston inventointikirjauskansion asetusten perusteella.  
5. Avaa haku napsauttamalla Työntekijä-kentässä avattavan valikon painiketta.
6. Valitse luettelosta työntekijä, jota haluat käyttää.
7. Klikkaa Valitse.
8. Valitse OK.

## <a name="create-journal-lines"></a>Tämän kirjauskansion rivit
1. Valitse Uusi.
2. Avaa haku valitsemalla Nimiketunnus-kentässä avattavan valikon painike.
3. Etsi haluamasi tietue luettelosta ja valitse se.
    * Jos käytät USMF-yrityksen demotietoja, valitse A0001.  
4. Avaa haku napsauttamalla Toimipaikka-kentässä avattavan valikon painiketta.
5. Etsi haluamasi tietue luettelosta ja valitse se.
    * Jos käytät USMF-yrityksen demotietoja, valitse toimipaikka 2.  
6. Avaa haku valitsemalla Varasto-kentässä avattavan valikon painike.
7. Etsi haluamasi tietue luettelosta ja valitse se.
    * Jos käytät USMF-yrityksen demotietoja, valitse varasto 24.  
8. Avaa haku valitsemalla Sijainnit-kentässä avattavan valikon painike.
9. Etsi haluamasi tietue luettelosta ja valitse se.
    * Jos käytät USMF-yrityksen demotietoja, valitse sijainti BULK-001.  
10. Lisää Inventoitu-kenttään numero.
    * Jos annat inventoitu määrä, joka poikkeaa Varastosaldo-kentässä olevasta numerosta, Määrä-kenttä päivitetään näyttämään ristiriita.  
11. Valitse Tallenna.

## <a name="post-the-inventory-counting-journal"></a>Kirjaa varaston inventointikirjauskansio
1. Valitse Kirjaa.
    * Jos varaston inventointikirjauskansiota kirjatessa kirjataan varastovastaanoton Varastosaldo-kentässä tai varasto-otossa olevasta määrästä eroava inventoitu määrä, varastotaso ja arvo muuttuvat ja kirjanpitotapahtumat muodostetaan.  
2. Valitse OK.

## <a name="view-inventory-transactions"></a>Näytä varastotapahtumat
1. Valitse Varasto.
2. Valitse Tapahtumat.
    * Tässä näkyvät kaikki liittyvät tapahtumat, jotka luodaan, kun varaston inventointikirjauskansioon kirjataan.   

