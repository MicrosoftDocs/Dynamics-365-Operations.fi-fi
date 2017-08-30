--- 
title: Varaston varastotasojen oikaisu (perusvarastointi)
description: "Tässä menettelyssä selvitetään varaston oikaisun kirjauskansion luonti- ja kirjausprosessi, jolla voidaan oikaista varastossa olevien tuotteiden varastotasoja."
author: MarkusFogelberg
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mafoge
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 9b947a02be981155053e33a4ef20e19bf2a194a5
ms.openlocfilehash: f96db79bcb6ec26daaeb66d29edb18486daafab0
ms.contentlocale: fi-fi
ms.lasthandoff: 07/27/2017

---
# Varaston varastotasojen oikaisu (perusvarastointi)

[!include[task guide banner](../../includes/task-guide-banner.md)]

Tässä menettelyssä selvitetään varaston oikaisun kirjauskansion luonti- ja kirjausprosessi, jolla voidaan oikaista varastossa olevien tuotteiden varastotasoja. Ennen aloittamista varasto-oikaisuille on oltava määritettynä varaston oikaisun kirjauskansio. Voit käydä tämän menettelyn läpi emotietojen yrityksen USMF avulla tai käyttää omia tietojasi. Yleensä varastotyöntekijä tekee nämä tehtävät.


## Luo varaston oikaisun kirjauskansio
1. Valitse Inventoinnin- ja varastonhallinta > Kirjauskansioviennit > Nimikkeet > Varaston oikaisu.
2. Valitse Uusi.
3. Avaa haku valitsemalla Nimi-kentässä avattavan valikon painike.
4. Valitse luettelosta varaston oikaisun kirjauskansio, jota haluat käyttää.
    * Joidenkin kenttien tiedot voidaan lisätä valitsemasi varaston oikaisun kirjauskansion asetusten perusteella.  
5. Valitse OK.

## Tämän kirjauskansion rivit
1. Valitse Uusi.
2. Merkitse luettelossa nimiketunnuskenttä.
3. Valitse Nimiketunnus-kentässä nimike. Jos käytät USMF-yrityksen demotietoja, kirjoita D0001.
4. Avaa haku napsauttamalla Toimipaikka-kentässä avattavan valikon painiketta.
5. Valitse luettelosta toimipaikka.
6. Avaa haku valitsemalla Varasto-kentässä avattavan valikon painike.
7. Valitse luettelosta varasto.
    * Jos olet valinnut nimikkeen, jossa sijainti on pakollinen dimensio, sijainti on määritettävä tässä.  
8. Kirjoita numero Määrä-kenttään.
    * Kustannushinnan kenttä määrittää varastovastaanottojen yksikkökohtaisen kustannuksen. Jos nimiketunnukselle ei ole määritetty kustannusta tai haluat muuttaa sitä manuaalisesti, voit tehdä sen tässä.  

## Vahvista ja kirjaa varaston oikaisun kirjauskansio
1. Valitse Vahvista.
2. Valitse OK.
3. Valitse Kirjaa.
    * Kun kirjaat tämäntyyppisen kirjauskansion, järjestelmä kirjaa varastovastaanoton tai varasto-oton, muuttaa varastotason ja -arvon sekä luo kirjanpitotapahtumat.  
4. Valitse OK.
5. Sulje lomake.
6. Sulje sivu.

