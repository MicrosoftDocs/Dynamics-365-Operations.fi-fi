--- 
title: Varastosaatavuuden tarkistus
description: "Tässä menettelyssä kerrotaan, miten tietyn nimiketunnuksen varastosaldo ja käytettävissä oleva varasto tarkistetaan."
author: 
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventOnHandItemListPage, SysQueryForm, InventDimParmFixed, InventSupply, DefaultDashboard, WHSInventPhysicalOnhand, WHSOnHand
audience: Application User
ms.reviewer: 
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: 
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 62338fe11c30781f264e626fad835a2ba9dca837
ms.contentlocale: fi-fi
ms.lasthandoff: 09/29/2017

---
# <a name="check-the-availability-of-stock"></a>Varastosaatavuuden tarkistus

[!include [task guide banner](../../includes/task-guide-banner.md)]

Tässä menettelyssä kerrotaan, miten tietyn nimiketunnuksen varastosaldo ja käytettävissä oleva varasto tarkistetaan. Siinä näytetään myös, miten nimikkeeseen liittyvät toimitustiedot haetaan. Fyysinen käytettävissä oleva varasto on käytettävissä oleva varastosaldo. Se tarkoittaa ostettua, vastaanotettua ja rekisteröityä varastoa. Käytettävissä oleva varasto sisältää käytettävissä olevan varaston, mutta varaston, joka on tilattu ja jota odotetaan saapuvaksi, mutta jota ei ole vielä vastaanotettu tai rekisteröity. Voit käydä tämän menettelyn läpi emotietojen yrityksen USMF avulla tai käyttää omia tietojasi. Jos käytössä on USMF, voit käyttää esimerkiksi esillä olevia arvoja. Varastotyöntekijä tekee yleensä nämä tehtävät.


## <a name="check-on-hand-inventory-for-an-item"></a>Nimikkeen käytettävissä olevan varaston tarkistaminen
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

## <a name="check-physical-on-hand-inventory"></a>Fyysisen käytettävissä olevan varaston tarkistaminen
1. Valitse Varastonhallinta > Kyselyt ja raportit > Fyysinen käytettävissä oleva varasto.
2. Kirjoita arvo Nimiketunnus-kenttään.
    * Voit suodattaa nimikeluettelon Toimipaikka- ja Varasto-kentän avulla.  
3. Päivitä sivu.
4. Valitse Näytä dimensiot.
    * Dimensionäyttö-välilehden avulla voit valita, miten tarkat tiedot haluat nähdä käytettävissä olevasta varastosta.  
5. Valitse OK.
6. Sulje sivu.

## <a name="check-on-hand-inventory-by-location"></a>Käytettävissä olevan varaston tarkistaminen sijainnin mukaan
1. Valitse Varastonhallinta > Kyselyt ja raportit > Varastosaldon sijainnin mukaan.
2. Kirjoita arvo Varasto-kenttään.
    * Jos käytössä on esittelytietojen USMF-yritys, voit käyttää arvoa 51.  
3. Päivitä sivu.
4. Valitse Näytä dimensiot.
5. Valitse OK.
6. Sulje sivu.


