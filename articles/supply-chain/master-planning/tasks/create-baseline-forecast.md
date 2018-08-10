--- 
title: Luo perusennuste
description: "Tuotannon suunnittelija voi luoda perusennusteen aikasarjan ennustemallien avulla tai kopioimalla aiemman kysynnän."
author: ShylaThompson
manager: AnnBe
ms.date: 111/02/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 76334f7ee4efe33df4a86aaa11a59748387cec89
ms.openlocfilehash: 6a712077fed4a94ae6ae6ce7ea2cfba8848e5fa5
ms.contentlocale: fi-fi
ms.lasthandoff: 11/02/2017

---
# <a name="create-a-baseline-forecast"></a>Luo perusennuste

[!include [task guide banner](../../includes/task-guide-banner.md)]

Tuotannon suunnittelija voi luoda perusennusteen aikasarjan ennustemallien avulla tai kopioimalla aiemman kysynnän. Tässä menettelyssä kerrotaan, miten perusennuste luodaan kaikille tuotteille yhden nimikkeen kohdistustunnuksen avulla niin, että aiempi kysyntä kopioidaan. 


## <a name="set-up-an-item-allocation-key"></a>Nimikkeenkohdistustunnuksen määrittäminen
1. Siirry kohtaan Pääsuunnittelu > Asetukset > Konsernin sisäiset suunnitteluryhmät.
2. Käytä pikasuodatinta tietueiden etsimiseen. Voit esimerkiksi suodattaa Nimi-kenttää arvolla 10.
    * Kysynnän ennuste suoritetaan kaikille yrityksille. Tämän vuoksi on määritettävä kaikki yritykset, joille haluat luoda ennusteet yhdessä konsernin sisäisen suunnitteluryhmässä.  
3. Etsi haluamasi tietue luettelosta ja valitse se.
4. Valitse Nimikkeen kohdistustunnukset.
    * Valitse kaikki nimikkeen kohdistustunnukset, joille haluat luoda ennusteet.  
5. Merkitse valittu rivi luettelossa.
    * Valitse nimikkeen kohdistustunnus D_Aloc.  
6. Napsauta >.
7. Sulje sivu.
8. Sulje sivu.

## <a name="set-up-the-demand-forecasting-parameters"></a>Kysynnän ennusteen parametrien määrittäminen
1. Siirry kohtaan Pääsuunnittelu > Asetukset > Kysynnän ennuste > Kysynnän ennusteen parametrit.
2. Laajenna Ennustealgoritmin parametrit -osa.
3. Valitse Kysynnän luontistrategia -kentässä Kopioi historiallisen kysynnän päälle.
4. Valitse Tallenna.

## <a name="create-a-baseline-forecast"></a>Luo perusennuste
1. Siirry kohtaan Pääsuunnittelu > Ennuste > Kysynnän ennuste > Luo tilastollinen perusennuste.
2. Syötä päivämäärä Päivämäärästä-kenttään.
    * Jos olemassa on myyntitilauksia, jotka alkavat 1.1.2015, syötä tämä päivämäärä. Jos päivämäärä ei ole oikea, syötä ensimmäisen myyntitilauksen päivämäärä.  
3. Kirjoita päivämäärä Päivämäärään-kenttään.
    * Syötä myyntitilausten viimeinen päivämäärä, esimerkiksi "2015-03-31".  
4. Syötä päivämäärä Päivämäärästä-kenttään.
    * Syötä '2015-04-01'. Tämä päivämäärä lasketaan automaattisesti seuraavan ennustejakson alkupäivänä.  
5. Laajenna Tietueet-kohta ja sisällytä osaan.
6. Valitse Suodatin.
7. Merkitse valittu rivi luettelossa.
    * Merkitse rivi, jossa kentän arvo on Konsernin sisäinen suunnitteluryhmä.  
8. Kirjoita arvo Ehdot-kenttään.
    * Syötä konsernin sisäinen suunnitteluryhmä. Voit valita arvoksi esimerkiksi 10, jota käytettiin ensimmäisessä tehtävässä.  
9. Etsi haluamasi tietue luettelosta ja valitse se.
    * Valitse rivi, jossa kentän arvo on Nimikkeen kohdistustunnus.  
10. Kirjoita arvo Ehdot-kenttään.
11. Valitse OK.
12. Laajenna Lisäparametrit-osa.
13. Valitse Ennustejakso-kentässä Kuukausi.
14. Syötä Ennustehorisontti-kenttään 3.
15. Syötä Lukitusaikaraja-kenttään 1.
16. Valitse OK.

## <a name="visualize-the-demand-forecast"></a>Kysynnän ennusteen havainnollistaminen
1. Siirry kohtaan Pääsuunnittelu > Ennuste > Kysynnän ennuste > Oikaistu kysynnän ennuste.
2. Valitse koostenäkymätaulussa rivin 1 ja sarakkeen 2 solu. Tämä on toinen kuukausi, jolle ennuste on luotu.
3. Määritä QtyCell-kohdan arvoksi 400.
    * Syötä soluun numero, joka on eri kuin ennustettu numero. Voit syöttää arvoksi esimerkiksi 400.  
4. Olet tehnyt ennusteeseen manuaalisen oikaisun. Huomaa seuraavassa vaiheessa oleva graafinen tunnus.
5. Valitse Ennusteen rivitiedot.
    * Tällä sivulla näkyvät tarkkuusarvot, aiempi kysyntä ja ennuste. Voit muuttaa myös ennustetta.  


