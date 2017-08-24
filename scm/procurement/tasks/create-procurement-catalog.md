--- 
title: Luo hankintaluettelo
description: "Tässä oppaassa näytetään, miten tuotteiden hankintaluettelo luodaan."
author: mkirknel
manager: AnnBe
ms.date: 08/23/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bibis
ms.search.scope: Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: 19d053a0bdbdcc764b3361fe5a326e8c68cdc682
ms.contentlocale: fi-fi
ms.lasthandoff: 07/27/2017

---
# <a name="create-a-procurement-catalog"></a>Luo hankintaluettelo

[!include[task guide banner](../../includes/task-guide-banner.md)]

Tässä oppaassa näytetään, miten tuotteiden hankintaluettelo luodaan. Yleensä hankinta-asiantuntijat suorittavat tämän tehtävän. Opit myös, miten työntekijät voivat käyttää luetteloa ostoehdotuksien luonnissa. Järjestelmässä on oltava hankintaluokkahierarkia ennen luettelon luomista. Hierarkia periytyy uuteen luetteloon, kuten myös kaikki hierarkian tuotteet. Voit käyttää tätä opasta USMF-demoyrityksessä, jossa hankintaluokkahierarkia sekä menettelyn ohjeissa käytetyt esimerkit ovat saatavilla.


## <a name="ensure-that-a-procurement-category-hierarchy-exists"></a>Varmista, että hankintaluokkahierarkia on olemassa
1. Valitse Hankinta > Hankintaluokat.
    * Hankintaluokkahierarkia sisältyy USMF-demoyrityksen tietoihin ja tuotteet on lisätty Toimiston koneet/Tietokoneet -luokkaan. Jos käytät menettelyä tehtäväoppaana, sinun on ehkä poistettava lukitus, jos haluat selata luokkaa. Jos hierarkia ei ole käytettävissä, voit luoda sen napsauttamalla Uusi-painiketta. Tämän voi tehdä vain kerran.  
2. Sulje sivu.

## <a name="create-a-catalog"></a>Luo luettelo
1. Siirry kohtaan Hankinta > Luettelot > Tuotteiden hankintaluettelot.
2. Avaa valintaikkuna valitsemalla Uusi tuotteiden hankintaluettelo.
3. Kirjoita arvo Nimi-kenttään.
4. Valitse OK.
5. Laajenna puussa CORP PROCUREMENT CATEGORIES.
6. Laajenna puussa OFFICE MACHINES.
7. Valitse puussa "Tietokoneet".
    * Hankintaluokan tuotteet näytetään luettelossa. Jos haluat lisätä tuotteen luokkaan, tämä on tehtävä Hankintaluokkahierarkia-sivulla tai Nimiketiedot-sivulla.  
    * Päivityksen oletustyyppi määrittää, ovatko uudet, hankintaluokkahierarkiaan lisätyt tuotteet välittömästi näkyvissä luettelossa. Jos päivityksen tyyppinä on dynaaminen, muutokset näkyvät heti. Jos päivitystyyppi on staattinen, uudet tuotteet näkyvät luettelon käyttäjille vasta, kun se on julkaistu uudelleen. Julkaise-toiminto on käytettävissä sivun yläosan toimintoruudussa. Jos tuotteita poistetaan hankintaluokkahierarkiasta, muutos näkyy heti Oletuspäivitystyyppi-kentän arvosta huolimatta.  
8. Etsi haluamasi tietue luettelosta ja valitse se.
9. Valitse Piilota.
10. Valitse toimintoruudussa Luettelonavigointi.
11. Valitse Poista käytöstä.
12. Valitse toimintoruudussa Luettelonavigointi.
13. Napsauta Ota käyttöön.
14. Valitse Aktivoi luettelo.
15. Sulje sivu.

## <a name="make-the-catalog-visible"></a>Tee luettelosta näkyvä
1. Siirry kohtaan Hankinnat > Asetukset > Käytännöt > Ostokäytännöt.
2. Valitse hankintakäytäntö USMF.
    * Sinun on valittava ostokäytäntö yritykselle, johon käyttäjäprofiiliisi liitetty työntekijä saa tilata tuotteita. USMF-demoyrityksen tiedoissa järjestelmänvalvoja on liitetty työntekijään nimeltä Julia Funderburk, joka on USMF:n oletustilaaja tuotteille.  
3. Napsauta luettelossa valitulla rivillä olevaa linkkiä.
4. Valitse juuri luomasi luettelo.
5. Valitse OK.
6. Sulje sivu.
7. Sulje sivu.

## <a name="use-the-catalog"></a>Käytä luetteloa
1. Siirry kohtaan Hankinta > Ostoehdotukset > Kaikki ostoehdotukset.
2. Valitse Uusi.
3. Kirjoita arvo Nimi-kenttään.
4. Valitse OK.
5. Valitse Lisää tuotteet.
6. Etsi haluamasi tietue luettelosta ja valitse se.
    * Voit käyttää tuotteiden suodattamiseen luokkahierarkiaa vasemmalla tai luettelon yläosassa olevaa suodatinta.  
7. Valitse Lisää riveihin.
8. Etsi haluamasi tietue luettelosta ja valitse se.
9. Valitse Lisää riveihin.
10. Valitse OK.


