---
title: Tilausten lähettäminen suoratoimituksina
description: Tässä aiheessa käsitellään, miten myyntitilaukselle luodaan suoratoimitus.
author: omulvad
manager: tfehr
ms.date: 07/11/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable, PurchCreateFromSalesOrder, VendAccountItemLookup, SalesTableReferences, PurchTable, PurchTablePart, PurchEditLines, PurchTable, PurchTableReferences, MCRDropShipWorkbench, SalesShippingLine
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 31cb26479ccb74dfb58fd5590cd60d7b7c64c292
ms.sourcegitcommit: 827d77c638555396b32d36af5d22d1b61dafb0e8
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/16/2020
ms.locfileid: "4427488"
---
# <a name="ship-orders-as-direct-deliveries"></a>Tilausten lähettäminen suoratoimituksina

[!include [banner](../../includes/banner.md)]

Tässä aiheessa käsitellään, miten myyntitilaukselle luodaan suoratoimitus. Käytät suoratoimitusta, kun haluat lähettää tavarat asiakkaalle suoraan toimittajalta sen sijaan, että ne lähetettäisiin ensin omaan varastoon. Voit suorittaa tämän menettelyn esittely-yrityksen USMF kanssa tai käyttää omia tietojasi. Toisen Luo suoratoimitukset suoraan työtilasta -alitehtävän suorittaminen edellyttää, että myyntitilauksessa valitsemaasi nimikkeeseen on määritetty oletustoimittaja vapautetun päätuotteen oston pikavälilehdessä.

## <a name="set-an-individual-order-for-direct-delivery"></a>Määritä yksittäisen tilauksen suoratoimitus
1. Siirry siirtymisruudussa kohtaan **Moduulit > Myyntireskontra > Tilaukset > Kaikki myyntitilaukset**.
2. Valitse **Uusi**.
3. Syötä tai valitse arvo **Asiakastili**-kentässä ja valitse sitten **OK**.
4. Kirjoita tai valitse arvot **Nimikenumero**- ja **Toimipaikka**-kenttiin ja valitse sitten **Tallenna**.
5. Valitse sitten toimintoruudussa **Myyntitilaus** ja **Suoratoimitus**. Luo toimitus -sivulla on luettelo kaikista myyntitilauksesta kopioiduista avoimista myyntitilausriveistä. Voit tarkastella tilauksen tietoja ja tarvittaessa muokata tietoja, kuten määrää ja hinnoitteluehtoja, ennen suoratoimituksen luontia.  
6. Valitse **Sisällytä kaikki** -kentässä **Kyllä**.
    - Jos haluat muodostaa suoratoimituksen vain myyntitilausrivien alijoukolle, valitse ne yksitellen.  
    - **Toimittajatili**-kenttään on ehkä jo lisätty toimittajanumero. Jos tuotteelle on määritetty oletustoimittaja (liitetyssä nimikekattavuudessa), kyseinen toimittaja kopioidaan riville. Muussa tapauksessa toimittaja on annettava manuaalisesti. Tässä esimerkissä uusi toimittaja valitaan seuraavassa vaiheessa, vaikka yhden tiedot olisi jo täytetty.   
7. Syötä tai valitse arvo **Toimittajatili**-kentässä ja valitse sitten **OK**. Sanoma ilmoittaa, että ostotilaus on luotu.   
8. Laajenna **Rivin erittely** -osa.
9. Valitse **Toimitus**-välilehti ja varmista, että **Suoratoimitus**-kentän arvoksi on määritetty **Kyllä**.
10. Valitse toimintoruudussa **Yleiset**.
11. Valitse **Liittyvät tilaukset**.
12. Valitse **Ostotilaus**-kentän linkki.
13. Laajenna **Rivin esittely** -osa ja valitse **Osoite**-välilehti.
    - Ostotilausrivin toimitusosoite on asiakkaan toimitusosoite eikä yrityksesi osoite.  
    - Jos muutat joko ostotilausrivin tai alkuperäisen myyntitilausrivin toimitusosoitteen, vastaava tilausrivi päivitetään automaattisesti.  
14. Valitse **Toimitus**-välilehti.
    - Myyntitilausrivin tavoin myös liitetyn ostotilausrivin tyypiksi on määritetty Suoratoimitus.  
    - Ostotilausrivin toimituspäivämääräksi ja vahvistetuksi toimituspäivämääräksi on määritetty alkuperäisellä myyntitilausrivillä Pyydetty vastaanottopäivämäärä ja Vahvistettu vastaanottopäivämäärä.   
    - Jos päivität jommankumman näistä päivämääristä joko ostorivillä tai myyntirivillä, vastaavan tilauksen päivämäärät päivitetään automaattisesti.     
    - Ostotilaus joka on määritetty toimittamaan tavarat suoraan asiakkaalle on linkitetty alkuperäiseen myyntitilauksen erikoisliitoksella. Tämä liitos määrää säännön, jonka mukaan myyntitilauksen pakkausluetteloa ei voi päivittää myyntitilauksesta vaan se on tehtävä ostotilauksen avulla. Asiakaslaskutus on kuitenkin tehtävä myyntitilauksesta.  
15. Valitse toimintoruudussa **Osto**.
16. Valitse **Vahvistus**.
17. Valitse **OK**.
18. Valitse toimintoruudussa **Vastaanota**.
19. Valitse **Tuotteen vastaanotto**.
20. Kirjoita arvo **Tuotteen vastaanotto** -kenttään.
21. Valitse **OK**.
22. Valitse toimintoruudussa **Yleiset**.
23. Valitse **Liittyvät tilaukset** ja korosta haluamasi tietue.
    - Kun ostotilaus on päivitetty vastaanotetuiksi – eli toimittaja on lähettänyt tavarat asiakkaan osoitteeseen, jonka jälkeen alkuperäisen myyntitilauksen tilaksi on päivitetty automaattisesti Toimitettu.  
    - Myyntitilaus voidaan nyt laskuttaa.    
24. Valitse **OK**.
25. Sulje sivu.
26. Valitse **OK**. Palaa kotisivulle sulkemalla sivut.

## <a name="create-direct-deliveries-from-the-workbench"></a>Luo suoratoimitukset suoraan työtilasta
1. Siirry siirtymisruudussa kohtaan **Moduulit > Myyntireskontra > Tilaukset > Kaikki myyntitilaukset**.
2. Valitse **Uusi**.
3. Syötä tai valitse arvo **Asiakastili**-kentässä ja valitse sitten **OK**.
4. Syötä tai valitse arvot **Nimiketunnus**- ja **Toimipaikka**-kentissä.
5. Laajenna **Rivin erittely** -osa ja valitse sitten **Toimitus**-välilehti. Sen sijaan että suoratilaus luotaisiin myyntitilauksen osana kuten edellisessä menettelyssä, voit siirtää tämän tehtävän ostajalle. Jos haluat sisällyttää myyntitilausrivin suoratoimituksen käsittelyprosessiin, rivi on merkittävä suoratoimitettavaksi.  
6. Valitse **Suoratoimitus**-kentässä **Kyllä**.
    - Jos nimike on jo määritetty oletusarvoisesti suoratoimitukseen, kentän asetuksena on tilausrivin käsittelyssä automaattisesti Kyllä. Voit määrittää nimikkeen suoratoimitettavaksi vapautetun tuotteen päätuotteessa valitsemalla Suoratoimitus-asetukseksi Kyllä ja valitsemalla suoratoimituksen oletusvaraston.  
    - Koska ostotilausta ei ole vielä luotu, suoratoimituksen tilana Suoratoimitettava.   
7. Valitse **Tallenna**.
8. Palaa kotisivulle sulkemalla sivut.
9. Kirjoita hakupalkkiin `Direct delivery`.
    - Suoratoimitus-sivu toimii työtilana, jossa ostoedustaja saa yhteenvedon kaikista suoratoimitettavista myyntitilausriveistä, joten he voivat luoda vastaavat ostotilaukset. Lisäksi he tarkastella Vahvistus- ja Toimitus-välilehdissä avoimia suoratoimitustilauksia ja vahvistettuja tilauksia.  
    - Luotu suoratoimitustilaus siirretään automaattisesti Vahvistus-välilehteen. Voit halutessasi vahvistaa tilauksen suoraan tällä sivulla. Kun osto on vahvistettu, se siirretään automaattisesti Toimitus-välilehteen, josta voit rekisteröidä sen vastaanoton.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]