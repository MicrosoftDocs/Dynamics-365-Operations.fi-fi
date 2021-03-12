---
title: Ostotilauksen luominen myyntitilauksesta
description: Tässä menettelyssä käsitellään, miten myyntitilaukseen perustuva ostotilaus luodaan.
author: omulvad
manager: tfehr
ms.date: 06/26/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable, PurchCreateFromSalesOrder, VendAccountItemLookup, SalesTableReferences, PurchTable, PurchTablePart
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5cabb1647b2008bbb67a7b9d6789fddab66b54e3
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/15/2021
ms.locfileid: "4974832"
---
# <a name="create-a-purchase-order-from-a-sales-order"></a>Ostotilauksen luominen myyntitilauksesta

[!include [banner](../../includes/banner.md)]

Tässä menettelyssä käsitellään, miten myyntitilaukseen perustuva ostotilaus luodaan. Ostotilauksen tuotteen määrät määritetään sitten täyttämään alkuperäisen ostotilauksen kysyntä. Myynnin kysynnän täyttäminen tällä tavoin on vaihtoehto kattavammalle ja optimoidulle jakelutarpeiden suunnittelumenetelmälle. Voit suorittaa tämän menettelyn esittely-yrityksen USMF kanssa tai käyttää omia tietojasi.


## <a name="create-a-purchase-order-from-a-sales-order"></a>Ostotilauksen luominen myyntitilauksesta
1. Valitse **Siirtymisruutu > Moduulit > Myynti ja markkinointi > Myyntitilaukset > Kaikki myyntitilaukset**.
2. Valitse **Uusi**.
3. Avaa haku valitsemalla **Asiakastili**-kentässä avattavan valikon painike.
4. Etsi haluamasi tietue luettelosta ja valitse se.
5. Valitse **OK**.
6. Avaa haku valitsemalla **Nimiketunnus**-kentässä avattavan valikon painike.
7. Etsi haluamasi tietue luettelosta ja valitse se. Jos käytössä on USMF, voit valita D0001.  
8. Anna **Määrä**-kentässä numero.
9. Valitse **Lisää rivi**.
10. Avaa haku valitsemalla **Nimiketunnus**-kentässä avattavan valikon painike.
11. Etsi haluamasi tietue luettelosta ja valitse se. Jos käytössä on USMF, voit valita T0020.  
12. Napsauta luettelossa valitulla rivillä olevaa linkkiä.
13. Anna **Määrä**-kentässä numero.
14. Valitse **Tallenna**.
15. Valitse **toimintoruudussa** **Myyntitilaus**.
16. Valitse **Ostotilaus**. **Luo ostotilaus** -sivulla on luettelo kaikista myyntitilauksesta kopioiduista avoimista myyntitilausriveistä. Voit tarkastella tilauksen tietoja ja tarvittaessa muokata valittuja tietoja, kuten määrää ja hinnoitteluehtoja, ennen ostojen luontia. 
17. Valitse **Sisällytä kaikki** -vaihtoehto.
    - Jos haluat muodostaa ostotilauksen vain myyntitilausrivien alijoukolle, valitse ne yksitellen.  
    - **Toimittajatili**-kenttään on ehkä jo lisätty toimittajanumero. Jos tuotteelle on määritetty oletustoimittaja (liitetyssä nimikekattavuudessa), kyseinen toimittaja kopioidaan riville. Muussa tapauksessa toimittaja on annettava manuaalisesti.  Tämän opastuksen seuraavissa vaiheissa pyydetään valitsemaan uusi toimittaja, joka on jokaiselle riville eri. Näin toimitaan riippumatta siitä, onko **Toimittajatili**-kentässä arvo vai ei.  
18. Avaa haku valitsemalla **Toimittajan tili** -kentässä avattavan valikon painike.
19. Etsi haluamasi tietue luettelosta ja valitse se.
20. Napsauta luettelossa valitulla rivillä olevaa linkkiä.
21. Valitse toinen tilausrivi.
22. Avaa haku valitsemalla **Toimittajan tili** -kentässä avattavan valikon painike.
23. Etsi haluamasi tietue luettelosta ja valitse se.
24. Napsauta luettelossa valitulla rivillä olevaa linkkiä.
25. Valitse **Vahvista**.
26. Valitse **OK**. Sanoma ilmoittaa, että vähintään yksi ostotilaus on luotu. Järjestelmän muodostaa erillisen ostotilauksen kullekin myyntitilausriveille määritetylle toimittajalle. Tämä tarkoittaa sitä, että jos sama toimittaja toimittaa useita myyntitilausrivejä, ostotilauksia luodaan yksi mutta siinä on useita rivejä.  

## <a name="review-purchase-orders-created-from-sales-orders"></a>Tarkastele myyntitilauksista luotuja ostotilauksista.
1. Valitse **toimintoruudussa** **Yleiset**.
2. Valitse **Liittyvät tilaukset**. **Liittyvät tilaukset** -sivulla on luettelo kaikista myyntitilauksesta luoduista tilauksista. Tässä esimerkissä on muodostettu kaksi ostotilausta kahdelle eri toimittajalle. 
3. Avaa **Ostotilaus**-kentän linkki napsauttamalla. Jokainen ostotilausrivi on liitetty ostoon johtaneeseen myyntitilausriviin. Suhde myyntitilaukseen on ilmaistu **Tuote**-välilehden **Rivin erittely** -pikavälilehden **Viitetyyppi**-, **Viitenumero**- ja **Viite-erä**-kentissä.  
4. Laajenna tai tiivistä **Rivitiedot**-osa.
5. Valitse **Tuote**-välilehti.
    - **Viite-erä** varmistaa, että oston kustannukset veloitetaan siihen liitetyssä myyntitilauksessa.  
    - Voit siirtyä alkuperäiseen myyntitilaukseen avaamalla linkin **Viitenumero**-kentässä.  

