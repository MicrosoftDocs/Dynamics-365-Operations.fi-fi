---
title: Etsi sovellettavat hinnat ja alennukset
description: Menettelyssä selvitetään, miten voidaan etsiä tietyllä asiakkaalla voimassaoleva tuotehinta ja/tai -alennus myyntitilausta luomatta.
author: omulvad
manager: tfehr
ms.date: 11/10/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9bd85d9cd2d7273ad6e05d794a96e4d6a8d7c526
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/15/2021
ms.locfileid: "5010769"
---
# <a name="look-up-applicable-prices-and-discounts"></a>Etsi sovellettavat hinnat ja alennukset

[!include [banner](../../includes/banner.md)]

Menettelyssä selvitetään, miten voidaan etsiä tietyllä asiakkaalla voimassaoleva tuotehinta ja/tai -alennus myyntitilausta luomatta. Menettelyssä käsitellään yksi esimerkki yksityiskohtaisesti ja, jotta voisit seurata esimerkkiä ja valita tarvittavat arvon, sinun on käytettävä USMF-demoyritystä.


## <a name="find-the-applicable-price"></a>Etsi sovellettava hinta
1. Valitse Myynti ja markkinointi > Hinnat ja alennukset > Etsi hinnat.
2. Avaa haku valitsemalla Asiakastili-kentässä avattavan valikon painike.
3. Etsi luettelosta asiakas US-001 ja valitse se.
4. Napsauta luettelossa valitulla rivillä olevaa linkkiä.
5. Kirjoita Nimiketunnus-kenttään T0004.
    * Määrä-kentän oletusarvo on 1. Jos kuitenkin tiedät, kuinka paljon kukin asiakas aikoo kyseistä tuotetta tilata, anna sen sijaan kyseinen arvo. Näillä tiedoilla on merkitystä, jos asiakkaan kanssa solmitussa sopimuksessa on määrärajoja eli tuotteen hinta määräytyy ostetun vähimmäismäärän mukaan.  
6. Anna Päivämäärä-kenttää päivämäärä, jolloin asiakas odottaa tekevänsä tilauksen. 
    * Päivämäärä voi kuluva päivä tai mikä tahansa tuleva päivä.  
    * Järjestelmä palauttaa nyt hinnan, joka koskee valittua tuotetta, jota valittu asiakas on ostanut tietyn määrän valittuna päivämääränä. Jos asiakas US-001 on tässä esimerkissä ostanut tänään 1 yksikön tuotetta T0004, asiakkaalta veloitettaisiin yksikköä kohden 350 Kanadan dollaria. Tämä hinta perustuu asiakkaan kanssa aiemmin solmittuun, aktiiviseen kauppasopimukseen.      Sivun muissa kentissä on lisätietoja tuotehinnasta ja tuotteen kustannuksista (jos ne on määritetty päätuotteessa) sekä laskettu kannattavuus.  
    * Jos Näytä liittyvät tuotevariantit -vaihtoehto on valittu, tuotevarianteille on muita kauppasopimuksia.  
7. Valitse Näytä liittyvät tuotevariantit -valintaruutu.
    * Näkyvissä on tuotevarianttiluettelo, jossa on tietoja niiden dimensioista.  
8. Merkitse luettelossa väriä Valkoinen vastaava rivi.
    * Huomaa, että tuotehinta poikkeaa nyt hinnasta, joka näytettiin, kun sitä ei oltu määritetty dimensiokohtaisesti.  
9. Valitse Näytä myyntihinnat.
    * Hinta (myynti) -sivulla on nähtävissä kaikki tuotteeseen ja sen variantteihin sovellettavat kauppasopimukset.  
10. Sulje sivu.

## <a name="find-the-applicable-discount"></a>Etsi sovellettava alennus
Varmista, Asiakastili-kentässä on asiakasnumero US-001    
1. Kirjoita Nimiketunnus-kenttään T0012.
    * Varmista, että Määrä-kentän arvo on 1.  
    * Seuraavat tuotteelle T0012 näytetyt hinnoittelutiedot perustuvat vähintään yhteen kauppasopimukseen: yksikköhinta on 1 000 Kanadan dollaria ja alennusprosentti 5.  
2. Valitse määräksi 20.
    * Tilausmäärän kasvun vuoksi asiakkaalle annettava rivialennus muuttuu 5 prosentista 7 prosenttiin.  
    * Nettosumma lasketaan yksikköhinnan, alennuksen ja kokonaismäärän perusteella.  
3. Valitse Näytä rivialennus.
    * Tuotteella T0012 on kaksi rivialennussopimusta, joista toinen antaa 5 prosentin alennuksen, kun tilausmäärä on 1–10 ja toinen 7 prosentin alennuksen, kun määrä on yli 10. Huomaa, että alennuksia käytetään tuoteryhmissä, tässä esimerkissä ryhmäkoodi 01, johon tuote T0012 kuuluu.  
4. Sulje sivu.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]