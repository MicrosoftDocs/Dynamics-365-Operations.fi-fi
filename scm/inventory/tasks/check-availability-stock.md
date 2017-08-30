--- 
title: Varastosaatavuuden tarkistus
description: "Tässä menettelyssä kerrotaan, miten tietyn nimiketunnuksen varastosaldo ja käytettävissä oleva varasto tarkistetaan."
author: perlynne
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
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 9b947a02be981155053e33a4ef20e19bf2a194a5
ms.openlocfilehash: d103eb52a498e6273b1fdb43fc10dae4133e76b2
ms.contentlocale: fi-fi
ms.lasthandoff: 07/27/2017

---
# Varastosaatavuuden tarkistus

[!include[task guide banner](../../includes/task-guide-banner.md)]

Tässä menettelyssä kerrotaan, miten tietyn nimiketunnuksen varastosaldo ja käytettävissä oleva varasto tarkistetaan. Siinä näytetään myös, miten nimikkeeseen liittyvät toimitustiedot haetaan. Fyysinen käytettävissä oleva varasto on käytettävissä oleva varastosaldo. Se tarkoittaa ostettua, vastaanotettua ja rekisteröityä varastoa. Käytettävissä oleva varasto sisältää käytettävissä olevan varaston, mutta varaston, joka on tilattu ja jota odotetaan saapuvaksi, mutta jota ei ole vielä vastaanotettu tai rekisteröity. Voit käydä tämän menettelyn läpi emotietojen yrityksen USMF avulla tai käyttää omia tietojasi. Jos käytössä on USMF, voit käyttää esimerkiksi esillä olevia arvoja. Varastotyöntekijä tekee yleensä nämä tehtävät.


## Nimikkeen käytettävissä olevan varaston tarkistaminen
1. Valitse Inventoinnin- ja varastonhallinta > Kyselyt ja raportit > Käytettävissä oleva varasto.
2. Valitse nimiketunnuksen rivi.
    * Voit tehdä kyselyn käytettävissä olevasta varastosta nimiketunnuksen perusteella valitsemalla rivin, jossa taulun arvoksi on määritetty Käytettävissä oleva varasto ja kentän arvoksi on määritetty Nimiketunnus.  
3. Valitse Ehdot-kentässä nimike, josta haluat tehdä kyselyn.
    * Jos käytössä on esittely-yritys USMF:n tiedot, voit valita arvon M9201.  
4. Valitse OK.
5. Valitse Dimensiot.
    * Dimensiot-välilehden avulla voit valita, miten tarkat tiedot haluat nähdä käytettävissä olevasta varastosta. Jos tarvitset varaukseen liittyviä tietoja, kaikki varastonhallinnan prosessien lisätoimintoja käyttävien nimikkeiden varastodimensiot on näytettävä.  
6. Valitse OK.
7. Valitse toimintoruudussa Liittyvät tiedot.
    * Jos kohta ei ole näkyvissä, valitse ellipsipainike (…), jolloin näkyviin tulevat toimintoruudun lisävaihtoehdot.  
8. Valitse Toimituksen yhteenveto.
    * Toimituksen yhteenveto -välilehdessä on tietyn nimikkeen tietoja, kuten käytettävissä oleva varasto, läpimenoaika ja toimittajan tiedot.  
9. Laajenna Varasto-osa.
10. Laajenna Toimittajat-osa.
11. Sulje sivu.
12. Sulje sivu.

## Fyysisen käytettävissä olevan varaston tarkistaminen
1. Valitse Varastonhallinta > Kyselyt ja raportit > Fyysinen käytettävissä oleva varasto.
2. Kirjoita arvo Nimiketunnus-kenttään.
    * Voit suodattaa nimikeluettelon Toimipaikka- ja Varasto-kentän avulla.  
3. Päivitä sivu.
4. Valitse Näytä dimensiot.
    * Dimensionäyttö-välilehden avulla voit valita, miten tarkat tiedot haluat nähdä käytettävissä olevasta varastosta.  
5. Valitse OK.
6. Sulje sivu.

## Käytettävissä olevan varaston tarkistaminen sijainnin mukaan
1. Valitse Varastonhallinta > Kyselyt ja raportit > Varastosaldon sijainnin mukaan.
2. Kirjoita arvo Varasto-kenttään.
    * Jos käytössä on esittelytietojen USMF-yritys, voit käyttää arvoa 51.  
3. Päivitä sivu.
4. Valitse Näytä dimensiot.
5. Valitse OK.
6. Sulje sivu.

