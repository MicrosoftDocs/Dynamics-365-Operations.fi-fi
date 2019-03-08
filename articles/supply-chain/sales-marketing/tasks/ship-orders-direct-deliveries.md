---
title: Lähetä tilaukset suoratoimituksina
description: Tässä menettelyssä käsitellään, miten myyntitilaukselle luodaan suoratoimitus.
author: omulvad
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable, PurchCreateFromSalesOrder, VendAccountItemLookup, SalesTableReferences, PurchTable, PurchEditLines, PurchTableReferences, MCRDropShipWorkbench
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5cd68aa1c15672c702db887c08ecf9b3d63f2618
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/29/2019
ms.locfileid: "339277"
---
# <a name="ship-orders-as-direct-deliveries"></a>Lähetä tilaukset suoratoimituksina

[!include [task guide banner](../../includes/task-guide-banner.md)]

Tässä menettelyssä käsitellään, miten myyntitilaukselle luodaan suoratoimitus. Käytät suoratoimitusta, kun haluat lähettää tavarat asiakkaalle suoraan toimittajalta sen sijaan, että ne lähetettäisiin ensin omaan varastoon. Voit suorittaa tämän menettelyn esittely-yrityksen USMF kanssa tai käyttää omia tietojasi. Toisen Luo suoratoimitukset suoraan työtilasta -alitehtävän suorittaminen edellyttää, että myyntitilauksessa valitsemaasi nimikkeeseen on määritetty oletustoimittaja vapautetun päätuotteen oston pikavälilehdessä.


## <a name="set-an-individual-order-for-direct-delivery"></a>Määritä yksittäisen tilauksen suoratoimitus
1. Siirry Kaikki myyntitilaukset -kohtaan.
2. Valitse Uusi.
3. Syötä tai valitse arvo Asiakastili-kentässä.
    * Jos käytössä on USMF, voit valita tilin US-001.  
4. Valitse OK.
5. Syötä tai valitse arvo Nimiketunnus-kentässä.
    * Jos käytössä on USMF, voit valita nimikkeen T0020.  
6. Valitse Tallenna.
7. Valitse toimintoruudussa Myyntitilaus.
8. Valitse Suoratoimitus.
    * Luo toimitus -sivulla on luettelo kaikista myyntitilauksesta kopioiduista avoimista myyntitilausriveistä. Voit tarkastella tilauksen tietoja ja tarvittaessa muokata tietoja, kuten määrää ja hinnoitteluehtoja, ennen suoratoimituksen luontia.  
9. Valitse Sisällytä kaikki -kentässä Kyllä.
    * Jos haluat muodostaa suoratoimituksen vain myyntitilausrivien alijoukolle, valitse ne yksitellen.  
    * Toimittajatili-kenttään on ehkä jo lisätty toimittajanumero. Jos tuotteelle on määritetty oletustoimittaja (liitetyssä nimikekattavuudessa), kyseinen toimittaja kopioidaan riville. Muussa tapauksessa toimittaja on annettava manuaalisesti. Tässä esimerkissä uusi toimittaja valitaan seuraavassa vaiheessa, vaikka yhden tiedot olisi jo täytetty.   
10. Anna tai valitse arvo Toimittajatili-kentässä.
    * Jos käytössä on USMF, voit valita tilin 1001.  
11. Valitse OK.
    * Sanoma ilmoittaa, että ostotilaus on luotu.   
12. Laajenna Rivin erittely -osa.
13. Valitse Toimitus-välilehti.
    * Suoratoimitus-kentän asetuksena on nyt Kyllä.  
    * Luotu ostotilaus näkyy suoratoimituksen tilassa.   
14. Valitse toimintoruudussa Yleiset.
15. Valitse Liittyvät tilaukset.
16. Siirry eteenpäin napsauttamalla Ostotilaus-kentän linkkiä.
17. Laajenna Rivin erittely -osa.
18. Valitse Osoite-välilehti.
    * Huomaa, että ostotilausrivin toimitusosoite on asiakkaan toimitusosoite eikä yrityksesi osoite.  
    * Jos muutat joko ostotilausrivin tai alkuperäisen myyntitilausrivin toimitusosoitteen, vastaava tilausrivi päivitetään automaattisesti.  
19. Valitse Toimitus-välilehti.
    * Myyntitilausrivin tavoin myös liitetyn ostotilausrivin tyypiksi on määritetty Suoratoimitus.  
    * Ostotilausrivin toimituspäivämääräksi ja vahvistetuksi toimituspäivämääräksi on määritetty alkuperäisellä myyntitilausrivillä Pyydetty vastaanottopäivämäärä ja Vahvistettu vastaanottopäivämäärää.   
    * Jos päivität jommankumman näistä päivämääristä joko ostorivillä tai myyntirivillä, vastaavan tilauksen päivämäärät päivitetään automaattisesti.     
    * Ostotilaus joka on määritetty toimittamaan tavarat suoraan asiakkaalle on linkitetty alkuperäiseen myyntitilauksen erikoisliitoksella. Tämä liitos määrää säännön, jonka mukaan myyntitilauksen pakkausluetteloa ei voi päivittää myyntitilauksesta vaan se on tehtävä ostotilauksen avulla. Asiakaslaskutus on kuitenkin tehtävä myyntitilauksesta.  
20. Valitse toimintoruudussa Osta.
21. Valitse Vahvistus.
22. Valitse OK.
23. Valitse toimintoruudussa Vastaanota.
24. Valitse Tuotteen vastaanotto.
25. Kirjoita arvo Tuotteen vastaanotto -kenttään.
26. Valitse OK.
27. Valitse toimintoruudussa Yleiset.
28. Valitse Liittyvät tilaukset.
29. Merkitse valittu rivi luettelossa.
    * Kun ostotilaus on päivitetty vastaanotetuiksi – eli toimittaja on lähettänyt tavarat asiakkaan osoitteeseen, jonka jälkeen alkuperäisen myyntitilauksen tilaksi on päivitetty automaattisesti Toimitettu.  
    * Myyntitilaus voidaan nyt laskuttaa.    
30. Valitse OK.
31. Sulje sivu.
32. Valitse OK.

## <a name="create-direct-deliveries-from-the-workbench"></a>Luo suoratoimitukset suoraan työtilasta
1. Sulje sivu.
2. Sulje sivu.
3. Siirry Kaikki myyntitilaukset -kohtaan.
4. Valitse Uusi.
5. Syötä tai valitse arvo Asiakastili-kentässä.
6. Valitse OK.
7. Syötä tai valitse arvo Nimiketunnus-kentässä.
8. Laajenna Rivin erittely -osa.
9. Valitse Toimitus-välilehti.
    * Sen sijaan että suoratilaus luotaisiin myyntitilauksen osana kuten edellisessä menettelyssä, voit siirtää tämän tehtävän ostajalle. Jos haluat sisällyttää myyntitilausrivin suoratoimituksen käsittelyprosessiin, rivi on merkittävä suoratoimitettavaksi.  
10. Valitse Suoratoimitus-kentässä Kyllä.
    *   Jos nimike on jo määritetty oletusarvoisesti suoratoimitukseen, kentän asetuksena on tilausrivin käsittelyssä automaattisesti Kyllä. Voit määrittää nimikkeen suoratoimitettavaksi vapautetun tuotteen päätuotteessa valitsemalla Suoratoimitus-asetukseksi Kyllä ja valitsemalla suoratoimituksen oletusvaraston.  
    * Koska ostotilausta ei ole vielä luotu, suoratoimituksen tilana Suoratoimitettava.   
11. Sulje sivu.
12. Sulje sivu.
13. Valitse Suoratoimitus.
    * Suoratoimitus-sivu toimii työtilana, jossa ostoedustaja saa yhteenvedon kaikista suoratoimitettavista myyntitilausriveistä, joten he voivat luoda vastaavat ostotilaukset. Lisäksi he tarkastella Vahvistus- ja Toimitus-välilehdissä avoimia suoratoimitustilauksia ja vahvistettuja tilauksia.   
14. Valitse Luo suoratoimitus.
15. Valitse Vahvistus-välilehti.
    * Luotu suoratoimitustilaus siirretään automaattisesti Vahvistus-välilehteen. Voit halutessasi vahvistaa tilauksen suoraan tällä sivulla. Kun osto on vahvistettu, se siirretään automaattisesti Toimitus-välilehteen, josta voit rekisteröidä sen vastaanoton.  

