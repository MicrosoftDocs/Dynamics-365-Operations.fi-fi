--- 
title: "Inventoinnin määrittäminen"
description: "Inventointi on varastoprosessi, jota voit käyttää käytettävissä olevien varastonimikkeiden tarkastamiseen."
author: MarkusFogelberg
manager: AnnBe
ms.date: 06/23/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bibis
ms.search.scope: Operations
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: f0d598bbd13406b27a23dcf349f6c81e758a9e61
ms.contentlocale: fi-fi
ms.lasthandoff: 07/27/2017

---
# <a name="define-cycle-counting"></a>Inventoinnin määrittäminen 

[!include[task guide banner](../../includes/task-guide-banner.md)]

Inventointi on varastoprosessi, jota voit käyttää käytettävissä olevien varastonimikkeiden tarkastamiseen. Tämän tehtävän tallenne osoittaa, miten oletusinventointityön prioriteetti määritetään, miten mobiililaitteen valikkovaihtoehto otetaan käyttöön käsittelemään keräys- ja inventointitoimintoja, miten tyhjäksi tulevasta sijainnista käynnistyvä inventointiraja otetaan käyttöön ja miten tietyn nimikkeen inventointisuunnitelma otetaan käyttöön tietyssä varastossa. Varastopäällikkö tekee yleensä nämä tehtävät. Voit käyttää tässä menettelyssä USMF-yrityksen demotietoja tai käyttää omia tietojasi.


## <a name="set-the-priority-of-counting-work"></a>Määritä inventointityön prioriteetti
1. Valitse Varastonhallinta > Asetukset > Varastonhallinnan parametrit.
2. Valitse Inventointi-välilehti.
3. Lisää Inventointityön oletusprioriteetti -kenttään luku.
    * Tämä vaihe muuttaa inventointityön prioriteettia verrattuna varaston muihin työtyyppeihin. Kun syötät luvun, joka on alhaisempi kuin muiden työtyyppien luku, inventointityön prioriteetti nousee.  
4. Valitse Tallenna.
5. Sulje sivu.

## <a name="enable-the-mobile-device"></a>Ota mobiililaite käyttöön
1. Valitse Varastonhallinta > Asetukset > Mobiililaite > Mobiililaitteen valikkovaihtoehdot.
2. Valitse Uusi.
3. Kirjoita arvo Valikkovaihtoehdon nimi -kenttään.
4. Kirjoita Otsikko-kenttään arvo.
5. Valitse Tila-kentässä Työ.
6. Valitse Käytä nykyistä työtä -vaihtoehdossa Kyllä.
    * Kun määrität tämän vaihtoehdon arvoksi Kyllä, järjestelmä etsii aiemmin luotua työtä, kun mobiililaitteen valikkovaihtoehtoa käytetään.  
7. Valitse Ohjaaja-kentässä Järjestelmäohjattu.
    * Jos valitaan Järjestelmäohjattu, varastotyöntekijä ohjataan määritetyissä luokissa olevaan avoimeen työhön. (Nämä työluokat luodaan seuraavaksi.)  
8. Laajenna tai tiivistä Työluokat-osa.
    * Seuraavaksi luodaan kaksi työluokkaa, joita käytetään mobiililaitteen valikkovaihtoehdon kanssa. Kun valikkovaihtoehtoa käytetään, näissä työluokissa voidaan tehdä kyselyjä ja käyttäjälle näytetään työ, jolla on suurin prioriteetti.  
9. Valitse Uusi.
10. Valitse Työluokan tunnus -kentässä arvo.
11. Valitse Uusi.
12. Valitse Työluokan tunnus -kentässä arvo.
13. Valitse Tallenna.
14. Sulje sivu.
15. Valitse Varastonhallinta > Asetukset > Mobiililaite > Mobiililaitteen valikko.
16. Etsi haluamasi tietue luettelosta ja valitse se.
17. Valitse puusta juuri luotu valikkovaihtoehto.
18. Valitse Muokkaa.
19. Lisää valikkovaihtoehto valikkoon nuolen avulla.
20. Valitse Tallenna.

## <a name="create-a-counting-threshold"></a>Luo inventointiraja
1. Valitse Varastonhallinta > Asetukset > Inventointi > Inventointirajat.
2. Valitse Uusi.
3. Kirjoita Inventointirajan tunnus -kenttään arvo.
4. Valitse Käsittele inventointi heti -asetukseksi Kyllä.
5. Kirjoita arvo Kuvaus-kenttään.
6. Valitse Tallenna.
7. Valitse Valitse sijainnit.
8. Merkitse valittu rivi luettelossa.
9. Valitse Ehdot-kentässä arvo.
10. Valitse OK.
11. Sulje sivu.

## <a name="create-a-cycle-count-plan"></a>Luo inventointisuunnitelma
1. Valitse Varastonhallinta > Asetukset > Inventointi > Inventointisuunnitelmat.
2. Valitse Uusi.
3. Kirjoita Inventointisuunnitelman tunnus -kenttään arvo.
4. Kirjoita Kuvaus-kenttään arvo.
5. Lisää Inventointien enimmäismäärä -kenttään luku.
6. Valitse Tallenna.
7. Valitse Valitse sijainnit.
8. Merkitse valittu rivi luettelossa.
9. Valitse Ehdot-kentässä arvo.
10. Valitse OK.
11. Lisää Inventointien välissä olevat päivät -kenttään luku.
    * Jos esimerkiksi jos Inventointien välissä olevat päivät -kentän arvoksi määritetään 5, inventointityö luodaan viiden päivän välein. Jos inventointityöt käsitellään kolmantena päivänä, seuraava inventointityö luodaan viiden päivän jälkeen viimeisestä inventoinnista eli kahdeksantena päivänä.  
12. Valitse Tallenna.
13. Valitse Uusi.
14. Syötä Järjestysnumero-kenttään numero.
    * Lajittelujärjestys on pienimmästä numerosta suurimpaan. Arvon on oltava suurempi kuin 0 (nolla).  
15. Merkitse valittu rivi luettelossa.
16. Kirjoita arvo Kuvaus-kenttään.
17. Valitse Tallenna.
18. Valitse Määritä tuotekysely.
19. Merkitse valittu rivi luettelossa.
20. Syötä tai valitse arvo Ehdot-kenttään.
21. Valitse OK.
22. Sulje sivu.


