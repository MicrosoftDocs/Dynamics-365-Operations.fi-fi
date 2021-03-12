---
title: Varastosaatavuuden tarkistus
description: Tässä menettelyssä kerrotaan, miten tietyn nimiketunnuksen varastosaldo ja käytettävissä oleva varasto tarkistetaan.
author: ShylaThompson
manager: tfehr
ms.date: 06/25/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventOnHandItemListPage, SysQueryForm, InventDimParmFixed, InventSupply, DefaultDashboard, WHSInventPhysicalOnhand, WHSOnHand, InventOnhandItem
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d04abae36e144b429b8ebc73b4c110389fecd1f0
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/15/2021
ms.locfileid: "5000156"
---
# <a name="check-the-availability-of-stock"></a>Varastosaatavuuden tarkistus

[!include [banner](../../includes/banner.md)]

Tässä menettelyssä kerrotaan, miten tietyn nimiketunnuksen varastosaldo ja käytettävissä oleva varasto tarkistetaan. Siinä näytetään myös, miten nimikkeeseen liittyvät toimitustiedot haetaan. Fyysinen käytettävissä oleva varasto on käytettävissä oleva varastosaldo. Se tarkoittaa ostettua, vastaanotettua ja rekisteröityä varastoa. Käytettävissä oleva varasto sisältää käytettävissä olevan varaston, mutta varaston, joka on tilattu ja jota odotetaan saapuvaksi, mutta jota ei ole vielä vastaanotettu tai rekisteröity. Voit käydä tämän menettelyn läpi emotietojen yrityksen USMF avulla tai käyttää omia tietojasi. Jos käytössä on USMF, voit käyttää esimerkiksi esillä olevia arvoja. Varastotyöntekijä tekee yleensä nämä tehtävät.


## <a name="check-on-hand-inventory-for-an-item"></a>Nimikkeen käytettävissä olevan varaston tarkistaminen
1. Valitse **Siirtymisruutu > Moduulit > Varastonhallinta > Kyselyt ja raportit > Käytettävissä oleva varasto**.
2. Valitse **Nimiketunnus**-rivi. Voit tehdä kyselyn käytettävissä olevasta varastosta nimiketunnuksen perusteella valitsemalla rivin, jossa taulun arvoksi on määritetty **Käytettävissä oleva varasto** ja kentän arvoksi on määritetty **Nimiketunnus**.
3. Valitse **Ehdot**-kentässä nimike, josta haluat tehdä kyselyn. Jos käytössä on esittely-yritys USMF:n tiedot, voit valita arvon M9201.  
4. Valitse **OK**.
5. Valitse **toimintoruudussa** **Dimensiot**. **Dimensiot**-välilehden avulla voit valita, miten tarkat tiedot haluat nähdä käytettävissä olevasta varastosta. Jos tarvitset varaukseen liittyviä tietoja, kaikki varastonhallinnan prosessien lisätoimintoja käyttävien nimikkeiden varastodimensiot on näytettävä.
6. Valitse **OK**.
7. Valitse **toimintoruudussa** **Liittyvät tiedot**. Jos vaihtoehto ei ole näkyvissä, valitse kolme pistettä -painike (…), jolloin näkyviin tulevat toimintoruudun lisävaihtoehdot.
8. Valitse **Toimituksen yhteenveto**. **Toimituksen yhteenveto** -välilehdessä on tietyn nimikkeen tietoja, kuten käytettävissä oleva varasto, läpimenoaika ja toimittajan tiedot.  
9. Laajenna **Varasto**-osa.
10. Laajenna **Toimittajat**-osa.
11. Sulje sivu.
12. Sulje sivu.

## <a name="check-physical-on-hand-inventory"></a>Fyysisen käytettävissä olevan varaston tarkistaminen
1. Valitse **Siirtymisruutu > Moduulit > Varastonhallinta > Kyselyt ja raportit > Fyysinen käytettävissä oleva varasto**.
2. Kirjoita arvo **Nimiketunnus**-kenttään. Voit suodattaa nimikeluettelon Toimipaikka- ja Varasto-kentän avulla. 
3. Päivitä sivu.
4. Valitse **toimintoruudussa** **Näytä dimensiot**. Dimensionäyttö-välilehden avulla voit valita, miten tarkat tiedot haluat nähdä käytettävissä olevasta varastosta.
5. Valitse **OK**.
6. Sulje sivu.

## <a name="check-on-hand-inventory-by-location"></a>Käytettävissä olevan varaston tarkistaminen sijainnin mukaan
1. Valitse **Siirtymisruutu > Moduulit > Varastonhallinta > Kyselyt ja raportit > Varastosaldo sijainnin mukaan**.
2. Kirjoita arvo **Varasto**-kenttään. Jos käytössä on esittelytietojen USMF-yritys, voit käyttää arvoa 51.  
3. Päivitä sivu.
4. Valitse **Näytä dimensiot**.
5. Valitse **OK**.
6. Sulje sivu.

