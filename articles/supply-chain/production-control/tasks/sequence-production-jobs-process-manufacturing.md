--- 
title: "Jaksota tuotantotyöt prosessivalmistukseen"
description: "Näissä toimintaohjeissa käytetään maalituotteita esimerkkinä suunniteltujen tilausten sarjoittamisesta värin ja pakkauskoon prioriteettien mukaan."
author: ChristianRytt
manager: AnnBe
ms.date: 8/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ReqTransPo, PMFSeqReqRouteChangesListPage
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: a25a4575ca1600b07b2dac5949c8775bcd162650
ms.contentlocale: fi-fi
ms.lasthandoff: 09/29/2017

---
# <a name="sequence-production-jobs-for-process-manufacturing"></a>Jaksota tuotantotyöt prosessivalmistukseen

[!include [task guide banner](../../includes/task-guide-banner.md)]

Näissä toimintaohjeissa käytetään maalituotteita esimerkkinä suunniteltujen tilausten sarjoittamisesta värin ja pakkauskoon prioriteettien mukaan. Tämän menettelyn luomisessa käytetty esittely-yritys on USPI. Tämä menettely on tarkoitettu tuotannon suunnittelijalle.


## <a name="run-master-planning-for-uspi"></a>Suorita pääsuunnittelu USPI:lle
1. Valitse Pääsuunnittelu > Pääsuunnittelu > Suorita > Pääsuunnittelu.
2. Avaa haku valitsemalla Pääsuunnitelma-kentässä avattavan valikon painike.
3. Napsauta luettelossa valitulla rivillä olevaa linkkiä.
    * Valitse MasterPlan.  
4. Valitse OK.
    * Tämä käynnistää pääsuunnittelun, mukaan lukien sarjoitusprosessin. Tämä prosessi voi kestää muutamia minuutteja.  

## <a name="view-planned-orders-for-the-paint-products"></a>Näytä maalituotteiden suunnitellut tilaukset
1. Valitse Pääsuunnittelu > Pääsuunnittelu > Suunnitellut tilaukset.
2. Laajenna nimikkeen tietojen tietoruutu.
3. Laajenna aikataulutietojen tietoruutu.
4. Avaa haku valitsemalla Suunnitelma-kentässä avattavan valikon painike.
5. Etsi haluamasi tietue luettelosta ja valitse se.
    * Valitse MasterPlan.  
6. Napsauta luettelossa valitulla rivillä olevaa linkkiä.
7. Pikasuodattimen avulla voit suodattaa Nimiketunnus-kentän arvon P300 mukaan.
    * Avaa lukitus selataksesi oikealle, josta näet tilaus- ja toimituspäivämäärät. Huomaa, että nimikkeiden tilauspäivämäärä on tänään, ja että suunniteltujen tilausten toimituspäivämääriä ei sarjoiteta tärkeysjärjestykseen värin ja pakkauskoon mukaan, kuten tuotenimessä sanotaan. Vie osoitin nimiketunnuksen päälle nähdäksesi tuotteen nimi ja prioriteetti.  

## <a name="sequence-planned-orders-for-paint"></a>Sarjoita suunnitellut maalitilaukset
1. Sulje sivu.
2. Valitse Pääsuunnittelu > Pääsuunnittelu > Sarjoitetut suunnitellut tilaukset
3. Laajenna nimikkeen tietojen tietoruutu.
4. Laajenna aikataulutietojen tietoruutu.
    * Huomautus: Tässä voit nähdä, että suunniteltujen tilausten aloituspäivämäärä/-aika on sarjoitettu värin ja pakkauskoon mukaan 28 päivän aikajaksossa. Nämä jaksot on määritetty Kampanja-kentän numeron mukaan. Sarjoitettu suunniteltu tilaus -lomake toimii samalla tavalla kuin tavallinen suunnitellun tilauksen lomake, ja tuotannon suunnittelija voi vahvistaa suunnitellut tilaukset täällä.  
5. Valitse kaikki rivit.
6. Valitse Hyväksy.
    * Tämä päivittää suunniteltuihin tilauksiin valitun sarjoitetun tehtävän, joka on joko Lykkää tai Aikaista.  

## <a name="verify-the-sequence-of-the-planned-orders"></a>Vahvista suunniteltujen tilausten sarjoitus
1. Sulje sivu.
2. Valitse Pääsuunnittelu > Pääsuunnittelu > Suunnitellut tilaukset.
3. Laajenna nimikkeen tietojen tietoruutu.
4. Laajenna aikataulutietojen tietoruutu.
5. Avaa haku valitsemalla Suunnitelma-kentässä avattavan valikon painike.
6. Etsi haluamasi tietue luettelosta ja valitse se.
    * Valitse MasterPlan.  
7. Napsauta luettelossa valitulla rivillä olevaa linkkiä.
8. Pikasuodattimen avulla voit suodattaa Nimiketunnus-kentän arvon P300 mukaan.
    * Huomaa, että tilaukset nyt on sarjoitettu väri- ja kokoprioriteetin mukaan, ja suunnitellut tilaukset aloitetaan aikaisimpana tilaus- ja toimituspäivänä. Vahvista Tilauspäivämäärä-sarake tai Aloituspäivämäärä Ajoituksen tiedot -tietoruudussa.  


