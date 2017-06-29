---
title: Yleiskatsaus hankintaan
description: "Tässä artikkelissa on yleiskuvaus Hankinta-moduulissa käytettävissä olevista toiminnoista."
author: YuyuScheller
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 58021
ms.assetid: eea24e23-a803-4de0-a218-6485757cde1b
ms.search.region: Global
ms.author: fdahl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: d3669de6314e65c78ce5d401dae2e7481ec38b68
ms.contentlocale: fi-fi
ms.lasthandoff: 05/25/2017


---

# <a name="procurement-and-sourcing-overview"></a>Yleiskatsaus hankintaan

[!include[banner](../includes/banner.md)]


Tässä artikkelissa on yleiskuvaus Hankinta-moduulissa käytettävissä olevista toiminnoista.

Hankinta kattaa kaikki vaiheet tuotteen tai palvelun tarpeen tunnistamisesta sen hankintaan, vastaanottamiseen, laskuttamiseen ja maksujen käsittelyyn toimittajalla. Hankintaprosessit voidaan määrittää tiettyjä liiketoimintatarpeita varten määrittämällä ostokäytäntöjä ja työnkulkuja.

## <a name="identifying-a-need-for-product-and-services"></a>Tuotteiden ja palvelujen tarpeen tunnistaminen
Tuotteiden ja palveluiden tarve voi syntyä *hankintaehdotuksista* esimerkiksi, kun työntekijä tarvitsee tuotteen. *Tuoteluettelot *voidaan määrittää ohjaamaan saatavilla olevien tuotteiden valintaa, tai voidaan tehdä pyyntöjä tuotteista, joita ei vielä ole saatavilla luettelossa. Tällöin osto-osasto voi harkita, miten tuote voidaan toimittaa.  

*Käyttörajoja *voidaan käyttää rajoittamaan hankintoihin käytettäviä summia, ja *oston työnkulku *tuo mahdollisuuden edellyttää hyväksyntää ennen tilauksen tekemistä. On myös tarvittaessa mahdollista määrittää budjettivarojen kohdistus.  
  
Hankintaosasto määrittää tarvittavien tuotteiden ja palveluiden toimittajat. Tähän voi liittyä *tarjouspyyntöjen *lähettäminen useille mahdollisille toimittajille. On mahdollista jakaa pyydetyn tuotteen määritykset niin, että mahdolliset toimittajat voivat tarkastella näitä ja tarkistaa, pystyvätkö he toimittamaan määrityksiä vastaavan tuotteen. Toimittajat palauttavat tarjouksensa, jotka hankintaosasto tarkistaa ennen sen toimittajan valintaa, jolta hankinta halutaan tehdä.  

Ostotilaukset sisältävät mahdollisuuden lähettää *ostotiedustelu *toimittajalle vaihtoehtona kattavammalle tarjouspyyntöprosessille. Ostotiedustelua voidaan käyttää tilausta koskevien tietojen, kuten hintojen, alennusten ja toimituspäivän selvittämiseen. Jos toimittajat on määritetty käyttämään **Toimittajaportaalia**, ostotiedustelutoiminto ei ole käytössä. Tilaus jaetaan sen sijaan**Toimittaja**portaalissa, ja kun *vahvistuspyyntö* lähetetään, toimittaja voi vahvistaa sen suoraan.  

*Toimittajan tuoteluetteloita *voidaan käyttää toimittajan tarjoamaa tuotevalikoimaa koskevien tietojen keräämiseen. Toimittajat voivat julkaista oman tuoteluettelonsa, joten sitä on helpompi pitää ajan tasalla. Tuotteeseen voidaan liittää *hyväksyttyjen toimittajien luettelo*, joka ohjaa toimittajan valintaa uusia ostotilauksia avattaessa ja estää ei-tarkoitettujen toimittajien käytön.

## <a name="procurement"></a>Hankinta
*Ostotilauksia *voidaan luoda monella eri tavalla mukaan lukien:

-   Pääsuunnittelun tuloksena, jonka yhteydessä on tunnistettu oston vaativa kysyntä. Tämä prosessi luo suunniteltuja ostotilauksia ja kun nämä vapautetaan, järjestelmä luo ostotilaukset.
-   Ostoehdotusten käsittelyn kautta, joka päätyy hankintaan.
-   Ostosopimusten käsittelyn kautta, jossa ostotilaukset luodaan vapautettuina tilauksina sopimusten perusteella. Tätä käytetään usein, kun ostosopimuksia käytetään yleistilauksia varten.
-   Manuaalisesti, kun luotu ostotilaus ei perustu toiseen asiakirjaan.

Ostotilaukset, jotka määritetään*ostojen hyväksyntätyönkulussa*, tarvitsevat hyväksynnän ennen kuin ne kirjataan hyväksytyiksi, ja tämä vaaditaan ennen tilauksen jatkokäsittelyä.  

Ostotilaukset *vahvistetaan* osoituksena siitä, että toimittajan kanssa on solmittu sopimus. Ostotilaus etenee sitten vähitellen eri tilojen kautta, kunnes se lopulta laskutetaan tai perutaan.  

Ostotilausta luodessasi useisiin kenttiin on täytetty valmiiksi oletusmuotoisia toimittajaa koskevia tietoja, jotka on tallennettu **Toimittajat**-sivulle. Tämä tarkoittaa, että sinun tarvitsee täyttää vain rajoitettu määrä ostotilauksen kentistä. Voit kuitenkin halutessasi ohittaa nämä oletusarvot.

### <a name="prices-and-discounts"></a>Hinnat ja alennukset

Hinnat ja alennukset -kohta sisältää tietoja toimittajan tarjoamista hinnoista, alennuksista ja ostohyvitysehdoista. Hinnat ja alennukset voivat olla kohdassa *kauppasopimukset***. Kauppasopimukset sisältävät toimittajien hinnastot sisältäen hinnat tai alennukset, ja niillä on tietyt päivämäärävälit, jolloin sopimus on voimassa. Hinnat ja alennukset voidaan neuvotella ja ne voidaan esitellä *ostosopimusten kautta, *mukaan lukien ehdot kuten sitoumus ostaa tietty määrä tai tietystä rahallisesta arvosta neuvoteltujen ehtojen edellytyksenä. *Ostohyvityssopimuksia *voidaan solmia toimittajien kanssa, kun määrättyjen tuotteiden tai tuoreryhmien ostaminen saattaa aiheuttaa toimittajan myöntämän hyvityksen ostojen summasta tai volyymistä riippuen.

### <a name="delivery-options"></a>Toimitusvaihtoehdot

Ostotilaukseen liittyy erilaisia toimitusprosessivaihtoehtoja. Tilatut tuotteet voidaan jakaa *toimitusaikatauluihin,* joissa voidaan suunnitella tilatun määrän osien toimitus eri päiville. Toimitus voi myös sisältää *suoran toimituksen*. Se alkaa myyntitilauksesta, joka aiheuttaa automaattisesti pakkausluettelon luonnin ostotilaukselle samaan aikaan, kun tuotteen kuitti tallennetaan ostotilaukselle. Ostotilaukset voivat myös olla osa *konsernin sisäistä tilausketjua*. Näihin viitataan myös konsernin sisäisinä ostotilauksina, joissa tuotteet tilataan vastaavalta konsernin sisäiseltä myyntitilaukselta. Tässä tilanteessa osa vaiheista automatisoidaan kahden toisiinsa liittyvän konsernin sisäisen tilauksen välillä.

### <a name="supplementary-items"></a>Lisänimikkeet

Tuotteet voidaan määrittää sisältämään *lisänimikkeitä*. Tämä tarkoittaa tilauksessa olevaan tuotteeseen liittyvien tuotteiden ehdottamista. Lisätuotteita saatetaan edellyttää tai ne voivat olla valinnaisia. Joissain tapauksissa lisänimikkeitä saatetaan lisätä ilmaisina tuotteina, jotka liitetään muiden tuotteiden ostoon.

### <a name="purchase-order-charges"></a>Ostotilauksen kulut

Ostotilaukselle voidaan määrittää veloituksia. Tämä voi tapahtua automaattisesti automaattisten veloitusten määrittämisellä tai lisäämällä veloitukset manuaalisesti. Veloitukset voidaan määrittää tilaukselle otsikon tasolla tai tilausrivin tasolla. Veloitusten kirjanpito voidaan määrittää monella tavalla. Voit esimerkiksi määrittää, että veloitus lasketaan tuotekustannukseksi. Jos teet näin, veloitukset on kohdistettava tilausrivin tasolla ennen kuin tilaus voidaan vahvistaa. Veloitusten kohdistamiselle tilauksen otsikosta sen riveille on olemassa vaihtoehto, joka tekee tästä helpompaa.

## <a name="product-receipt-and-invoicing"></a>Tuotteen vastaanotto ja laskutus
Fyysisiä tuotteita sisältävät ostotilaukset vaativat usein *saapumisrekisteröinnin* varastossa, jonka jälkeen *tuotteen vastaanotto *rekisteröidään tilaukselle. Ostoehdotuksia täyttävät ostotilaukset voidaan määrittää siten, että tuotetta pyytäneen työntekijän pitää myös antaa *vastaanottovahvistus*.  

Jotkut ostotilaukset sisältävät tuotteita, jotka ovat palveluita tai muita ei-fyysisiä tuotteita, joille vastaanottoa varastossa ei tarvita. Tuotteita voidaan luoda palveluina, tai *hankintaluokkia *voidaan käyttää suoraan tällaisia tilauksia koskevalla ostotilauksella. Näissä tilauksissa tuotteen vastaanoton kirjanpito ohitetaan joskus, ja tilaus laskutetaan suoraan, tai vaihtoehtoisesti tuotteen vastaanottorekisteröinti tehdään ostotilaukselle ilman aiempaa saapumisrekisteröintiä.  

Tuotteen vastaanotto saattaa aiheuttaa automaattisen kulutuksen määrättyä tarkoitusta varten. Tähän sisältyy kulutus suoralla toimituksella, kulutus projektia varten, tai tuotteen kirjaaminen käyttöomaisuuteen.  

Kun* toimittajien laskuja* saapuu toimittajalta, ne saatetaan ensin kirjata *laskurekisteriin *ostotilauksesta riippumattomina ja sitten myöhemmin hyväksyä tietueena ostotilausta vastaan. Toimittajan laskun kirjaaminen ostotilauksen kanssa sisältää tuotteen vastaanoton täsmäyttämisen laskua vastaan.  

*Kirjanpidolliset jaot* voidaan määritellä ostotilauksella kuvaamaan, miten kirjanpito tulee suorittaa. Ne voivat myös määrittää, miten budjettivarojen kohdistus saadaan, kun tämä sisältyy määrityksiisi.  

Laskutetut ostotilaukset tallentavat velan toimittajan tilille ostoreskontraan, mistä *t*o*imittajan maksu *voidaan käsitellä.

## <a name="vendor-performance"></a>Toimittajan suoritustaso
Ostotoimintojen suorituskykyä ja arviointia tuetaan *hankinnan ja ostoreskontran raporttien kautta,* mikä sisältää varojen käytön analyysin ja toimittajan suoritusten analyysin.




