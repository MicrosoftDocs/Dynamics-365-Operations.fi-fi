--- 
title: "Lisää kanban-määrän laskentakäytäntö kanban-sääntöön"
description: "Tässä menettelyssä keskitytään kanban-määrän laskentakäytännön luomiseen ja sen lisäämiseen kanban-sääntöön kanbanin koon ja määrien optimoimista varten."
author: ChristianRytt
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: f9e0ccf25a346d54e48f51b0866f0c11e98bf0a0
ms.contentlocale: fi-fi
ms.lasthandoff: 07/27/2017

---
# <a name="add-a-kanban-quantity-calculation-policy-to-a-kanban-rule"></a>Lisää kanban-määrän laskentakäytäntö kanban-sääntöön

[!include[task guide banner](../../includes/task-guide-banner.md)]

Tässä menettelyssä keskitytään kanban-määrän laskentakäytännön luomiseen ja sen lisäämiseen kanban-sääntöön kanbanin koon ja määrien optimoimista varten. Tämän menettelyn luomisessa käytetty esittely-yritys on USMF. Tämä menettely on tarkoitettu arvovirtaa hallitsevalle työntekijälle. Tämä menettely on Laske kanban-määräehdotukset -menettelyn luomisen edellytys. 


## <a name="create-a-kanban-quantity-calculation-policy"></a>Uuden kanban-määrän laskentakäytännön luominen
1. Siirry kohtaan Tuotannonhallinta > Kausittaiset tehtävät > Kanban-määrän laskeminen > Kanban-määrän laskentakäytännöt.
2. Valitse Uusi.
3. Kirjoita arvo Nimi-kenttään.
    * Syötä esimerkiksi arvo Kaiutin2016.  
4. Avaa haku valitsemalla Pääsuunnitelma-kentässä avattavan valikon painike.
5. Etsi haluamasi tietue luettelosta ja valitse se.
    * Valitse StaticPlan, kun haluat laskea kysynnän.  
6. Napsauta luettelossa valitulla rivillä olevaa linkkiä.
7. Valitse Tallenna.
8. Syötä Kanban-määrä vähintään -kenttään 1.
    * Tämä on kanbanien lisänumero, joka sisällytetään kanban-määrän laskentaan.  
9. Määritä turvallisuuskertoimeksi 1.
    * Tämä on kerroin, jota käytetään varmuusvaraston lisämäärän laskennassa.  
10. Syötä Jäljellä olevat päivät -kenttään 30.
    * Tämä on niiden päivien lukumäärä ennen kanban-määrän laskentapäivämäärää, joka sisällytetään kysynnän laskentaan.  
11. Syötä Myöhästymispäivät-kenttään 30.
    * Tämä on niiden päivien lukumäärä kanban-määrän laskentapäivämäärästä alkaen, joka sisällytetään kysynnän laskentaan.  Laskennassa käytettävässä kaavassa näkyvät toteutuneet arvot. Esimerkki: Kanban-määrä = ((päivän keskimääräinen kysyntä x läpimenoaika x 2,00) / tuotemäärä per käsittely-yksikkö) + 1  
12. Sulje sivu.

## <a name="add-the-kanban-quantity-calculation-policy-to-a-kanban-rule"></a>Kanban-määrän laskentakäytännön lisääminen kanban-sääntöön
1. Siirry kohtaan Tuotetietojen hallinta > Lean-valmistus > Kanban-säännöt.
2. Etsi haluamasi tietue luettelosta ja valitse se.
    * Valitse tässä menettelyssä kanban-sääntö 000020.  
3. Napsauta luettelossa valitulla rivillä olevaa linkkiä.
4. Ota käyttöön Kanban-määrän laskentakäytännöt -osan laajennus.
5. ValitseLisää.
    * Lisää edellisessä alitehtävässä luotu kanban-määrän laskentakäytäntö.  
6. Merkitse valittu rivi luettelossa.
7. Avaa haku valitsemalla Nimi-kentässä avattavan valikon painike.
8. Napsauta luettelossa valitulla rivillä olevaa linkkiä.
    * Valitse edellisessä alitehtävässä luotu käytäntö Kaiutin2016.  


