---
title: Kanban-määräehdotusten laskeminen
description: Tässä menettelyssä keskitytään tietyn kanbanin koon ja määrien optimointiin tietylle kanban-säännölle kanban-määrän laskelman avulla.
author: ChristianRytt
manager: tfehr
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 409903740413994fead3f65b12afb414ca5c43ed
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5255394"
---
# <a name="calculate-kanban-quantity-suggestions"></a>Kanban-määräehdotusten laskeminen

[!include [banner](../../includes/banner.md)]

Tässä menettelyssä keskitytään tietyn kanbanin koon ja määrien optimointiin tietylle kanban-säännölle kanban-määrän laskelman avulla. Tämän menettelyn luomisessa käytetty esittely-yritys on USMF. Tämä menettely on tarkoitettu arvovirtaa hallitsevalle työntekijälle. Edellytys on Lisää uusi kanban-määrän laskentakäytäntö kanban-sääntöön -menettelyn suorittaminen.


## <a name="create-a-kanban-quantity-calculation"></a>Kanban-määrän laskelman luominen
1. Siirry kohtaan Tuotannonhallinta > Kausittaiset tehtävät > Kanban-määrän laskeminen > Laske Kanban-määrä.
2. Valitse Uusi.
3. Syötä Nimi-kenttään Kaiutin2016.
4. Avaa haku valitsemalla Nimi-kentässä avattavan valikon painike.
    * Valitse Lisää uusi kanban-määrän laskentakäytäntö kanban-sääntöön -menettelyssä luotu käytäntö. Valitse esimerkiksi arvo Kaiutin2016.  
5. Napsauta luettelossa valitulla rivillä olevaa linkkiä.
6. Määritä Säännön voimassaolon alkupäivämäärä -kenttään päivämääräksi ja kellonajaksi 17.12.2012 8.00,00.
    * Tämä Päivämäärä toimii kanban-määrän laskentaan sisällytettävien kiinteiden kanban-sääntöjen määrittämisen perustana.  
7. Määritä Täytetyn kysynnän kauden aloituspäivämäärä -kenttään päivämääräksi ja kellonajaksi 17.11.2012 9.00,00
    * Päivämäärä, josta alkaen aiemman kysynnän tapahtumat sisällytetään kanban-määrän laskentaan.  
8. Määritä Täytetyn kysynnän kauden päättymispäivämäärä -kenttään päivämääräksi ja kellonajaksi 17.12.2012 07.59,59.
    * Päivämäärä, johon asti aiemman kysynnän tapahtumat sisällytetään kanban-määrän laskentaan.  
9. Määritä Kysynnän kauden aloituspäivämäärä -kenttään päivämääräksi ja kellonajaksi 17.12.2012 8.00,00.
    * Päivämäärä, josta alkaen kuluvan kysynnän tapahtumat sisällytetään kanban-määrän laskentaan.  
10. Määritä Kysynnän kauden lopetuspäivämäärä -kenttään päivämääräksi ja kellonajaksi 16.1.2012 07.59,59.
    * Päivämäärä, johon asti kuluvan kysynnän tapahtumat sisällytetään kanban-määrän laskentaan.  

## <a name="generate-kanban-quantity-proposal"></a>Kanban-määräehdotuksen luominen
1. Valitse Tallenna.
2. Valitse Luo.
    * Tämä luo kanban-säännölle 000020 kanban-määräehdotusrivin.  

## <a name="run-kanban-quantity-calculation"></a>Kanban-määrän laskelman suorittaminen
1. Valitse Laske.
    * Tässä lasketaan kanban-määräehdotus.  
2. Valitse OK.
3. Merkitse valittu rivi luettelossa.
    * Huomaa, että ehdotettu kanban-määrä on 2.  

## <a name="change-product-quantity-and-calculate-again"></a>Tuotemäärän muuttaminen ja laskeminen uudelleen
1. Määritä tuotemääräksi 5.
2. Valitse Laske.
3. Valitse OK.
    * Huomaa, että jos kanban-määrä on 5, ehdotus muutetaan kanban-määräksi 4.  
    * Tämä johtuu siitä, että kun tuotemäärä on alempi, kysynnän täyttämiseksi tarvitaan enemmän kanbaneita.  

## <a name="update-kanban-rule"></a>Kanban-säännön päivittäminen
1. Syötä päivämäärä ja kellonaika Säännön voimaantulopäivämäärä -kenttään.
    * Määritä Säännön voimassaolon alkupäivämäärä -kohdan arvoksi tuleva päivämäärä. Syötä arvoksi esimerkiksi kuluvan päivä + yksi vuosi.  
2. Valitse Päivitä.
3. Valitse OK.
4. Sulje sivu.

## <a name="validate-change-on-kanban-rule"></a>Kanban-säännön muutoksen vahvistaminen
1. Siirry kohtaan Tuotetietojen hallinta > Lean-valmistus > Kanban-säännöt.
2. Napsauta luettelossa valitulla rivillä olevaa linkkiä.
    * Valitse edellisessä alitehtävässä luotu kanban-sääntö. Tämän tulee olla numeroiden mukaan lajitellun luettelon ensimmäinen kanban-sääntö.  
3. Ota käyttöön Tiedot-osan laajennus.
    * Ota huomioon voimaantulopäivä. Sääntö ei ole aktiivinen ennen tätä päivää.  
4. Ota käyttöön Määrät-osan laajennus.
    * Huomaa, että tämä on kanban-määrän laskelmassa syöttämäsi oletusmäärä.  
    * Huomaa, että tämä on kanban-määrän laskelman kiinteä kanban-määrä 4.  
5. Valitse ListPanel-välilehti.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]