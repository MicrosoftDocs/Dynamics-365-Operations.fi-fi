--- 
title: Ostotilauksen luominen myyntitilauksesta
description: "Tässä menettelyssä käsitellään, miten myyntitilaukseen perustuva ostotilaus luodaan."
author: omulvad
manager: AnnBe
ms.date: 8/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable, PurchCreateFromSalesOrder, VendAccountItemLookup, SalesTableReferences, PurchTable
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 412a8c7acca06fc1be073019f91144e2a3f1c94b
ms.contentlocale: fi-fi
ms.lasthandoff: 09/29/2017

---
# <a name="create-a-purchase-order-from-a-sales-order"></a>Ostotilauksen luominen myyntitilauksesta

[!include [task guide banner](../../includes/task-guide-banner.md)]

Tässä menettelyssä käsitellään, miten myyntitilaukseen perustuva ostotilaus luodaan. Ostotilauksen tuotteen määrät määritetään sitten täyttämään alkuperäisen ostotilauksen kysyntä. Myynnin kysynnän täyttäminen tällä tavoin on vaihtoehto kattavammalle ja optimoidulle jakelutarpeiden suunnittelumenetelmälle. Voit suorittaa tämän menettelyn esittely-yrityksen USMF kanssa tai käyttää omia tietojasi.


## <a name="create-a-purchase-order-from-a-sales-order"></a>Ostotilauksen luominen myyntitilauksesta
1. Siirry kohtaan Myynti ja markkinointi > Myyntitilaukset > Kaikki myyntitilaukset.
2. Valitse Uusi.
3. Avaa haku valitsemalla Asiakastili-kentässä avattavan valikon painike.
4. Etsi haluamasi tietue luettelosta ja valitse se.
5. Valitse OK.
6. Avaa haku valitsemalla Nimiketunnus-kentässä avattavan valikon painike.
7. Etsi haluamasi tietue luettelosta ja valitse se.
    * Jos käytössä on USMF, voit valita D0001.  
8. Kirjoita numero Määrä-kenttään.
9. Valitse Lisää rivi.
10. Avaa haku valitsemalla Nimiketunnus-kentässä avattavan valikon painike.
11. Etsi haluamasi tietue luettelosta ja valitse se.
    * Jos käytössä on USMF, voit valita T0020.  
12. Napsauta luettelossa valitulla rivillä olevaa linkkiä.
13. Kirjoita numero Määrä-kenttään.
14. Valitse Tallenna.
15. Valitse toimintoruudussa Myyntitilaus.
16. Valitse Ostotilaus.
    * Luo ostotilaus -sivulla on luettelo kaikista myyntitilauksesta kopioiduista avoimista myyntitilausriveistä. Voit tarkastella tilauksen tietoja ja tarvittaessa muokata valittuja tietoja, kuten määrää ja hinnoitteluehtoja, ennen ostojen luontia.  
17. Valitse Sisällytä kaikki -vaihtoehto.
    * Jos haluat muodostaa ostotilauksen vain myyntitilausrivien alijoukolle, valitse ne yksitellen.  
    * Toimittajatili-kenttään on ehkä jo lisätty toimittajanumero. Jos tuotteelle on määritetty oletustoimittaja (liitetyssä nimikekattavuudessa), kyseinen toimittaja kopioidaan riville. Muussa tapauksessa toimittaja on annettava manuaalisesti.  Tämän opastuksen seuraavissa vaiheissa pyydetään valitsemaan uusi jokaiselle riville eri toimittaja. Näin toimitaan riippumatta siitä, onko Toimittajatili-kentässä arvo vai ei.  
18. Avaa haku valitsemalla Toimittajan tili -kentässä avattavan valikon painike.
19. Etsi haluamasi tietue luettelosta ja valitse se.
20. Napsauta luettelossa valitulla rivillä olevaa linkkiä.
21. Valitse toinen tilausrivi.
22. Avaa haku valitsemalla Toimittajan tili -kentässä avattavan valikon painike.
23. Etsi haluamasi tietue luettelosta ja valitse se.
24. Napsauta luettelossa valitulla rivillä olevaa linkkiä.
25. Valitse Vahvista.
26. Valitse OK.
    * Sanoma ilmoittaa, että vähintään yksi ostotilaus on luotu. Järjestelmän muodostaa erillisen ostotilauksen kullekin myyntitilausriveille määritetylle toimittajalle. Tämä tarkoittaa sitä, että jos sama toimittaja toimittaa useita myyntitilausrivejä, ostotilauksia luodaan yksi mutta siinä on useita rivejä.  

## <a name="review-purchase-orders-created-from-sales-orders"></a>Tarkastele myyntitilauksista luotuja ostotilauksista.
1. Valitse toimintoruudussa Yleiset.
2. Valitse Liittyvät tilaukset.
    * Liittyvät tilaukset -sivulla on luettelo kaikista myyntitilauksesta luoduista tilauksista. Tässä esimerkissä on muodostettu kaksi ostotilausta kahdelle eri toimittajalle.  
3. Siirry eteenpäin napsauttamalla Ostotilaus-kentän linkkiä.
    * Jokainen ostotilausrivi on liitetty ostoon johtaneeseen myyntitilausriviin. Suhde myyntitilaukseen on ilmaistu Tuote-välilehden Rivin erittely -pikavälilehden Viitetyyppi-, Viitenumero- ja Viite-erä-kentissä.  
4. Laajenna tai tiivistä Rivitiedot-osa.
5. Valitse Tuote-välilehti.
    * Viite-erä varmistaa, että oston kustannukset veloitetaan siihen liitetyssä myyntitilauksessa.  
    * Voit siirtyä alkuperäiseen myyntitilaukseen avaamalla linkin Viitenumero-kentässä.  


