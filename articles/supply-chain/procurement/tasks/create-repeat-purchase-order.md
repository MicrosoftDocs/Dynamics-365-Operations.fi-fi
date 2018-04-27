--- 
title: Toistuvan ostotilauksen luonti
description: "Seuraavassa menettelyssä kuvataan, miten luot toistuvan ostotilauksen (PO) kopioimalla rivejä vanhasta ostotilauksesta uuteen tai vanhaan ostotilaukseen."
author: FrankDahl
manager: AnnBe
ms.date: 08/23/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.author: fdahl
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 257582d889ff55753f9bdbd234f0540503d20f27
ms.contentlocale: fi-fi
ms.lasthandoff: 09/29/2017

---
# <a name="create-a-repeat-purchase-order"></a>Toistuvan ostotilauksen luonti

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

Seuraavassa menettelyssä kuvataan, miten luot toistuvan ostotilauksen (PO) kopioimalla rivejä vanhasta ostotilauksesta uuteen tai vanhaan ostotilaukseen. Toistuvien tilausten luomiseen on kaksi tapaa. Voit käyttää käytettävissä olevia asiakirjatason toimintoja toimintoruudusta tai rivin tietojen toimintoja. Asiakirjan tason toiminnot on tarkoitettu pääasiassa uuden ostotilauksen luomiseen lisäämällä otsikkotiedot ja rivit toisesta tilauksesta, ja rivin tietojen toiminnot on taas tarkoitettu rivien lisäämiseen vanhaan tilaukseen. Tämän oppaan esimerkissä käytetään esittely-yritys USMF:n tietoja. Yleensä ostoedustaja tekee tämän tehtävän.


## <a name="create-a-new-repeat-purchase-order"></a>Luo uusi toistuva ostotilaus
1. Valitse Hankinta > Ostotilaukset > Kaikki ostotilaukset.
    * Yritetään ensin vaihtoehtoa kopioida tiedot uuteen tilaukseen.  
2. Valitse Uusi.
3. Kirjoita Toimittajan tili -kenttään arvoksi US-101.
4. Valitse OK.
5. Valitse toimintoruudussa Ostotilaus.
6. Valitse Kaikista.
    * Tältä sivulta voit kopioida tietoja olemassa olevista tilauksesta omaan tilaukseesi. Rivien kopiointiin on erilaisia vaihtoehtoja, ja kopioinnin lähdeasiakirjoja on myös erilaisia. Tarkastelemme rivien kopiointitapojen vaihtoehtoja ensin.   
7. Laajenna Parametrit-osa.
    * Määräkerroin-kenttä on hyödyllinen, jos sinun on käytettävä määrää, joka poikkeaa kopioinnin lähteenä olevan tilauksen määrästä. Jos esimerkiksi haluat tilata kaksinkertaisen määrän kopioinnin lähteenä oleviin riveihin verrattuna, kirjoita tähän kenttään "2" ja järjestelmä lisää rivit, joissa alkuperäinen määrä on kaksinkertainen.  
    * Myös Vaihda etumerkki -kenttä tukee tilatun määrän muuttamista vaihtamalla lisättyjen tilausrivien määrän etumerkin. Voi olla hyötyä, jos sinun on peruutettava tapahtuma luomalla tilausrivejä, jotka kumoavat tapahtuman. Tämä vaihtoehto valitaan automaattisesti, kun sivu avataan Luo hyvityslasku -toiminnolla.  
    * Kopioi kulut -vaihtoehdon avulla voit kopioida kulut uuteen tilaukseen tilausrivien lähteenä olevasta asiakirjasta.  
    * Laske hinnat uudelleen -vaihtoehto käyttää nykyisiä hintoja ja alennuksia sen sijaan, että ne kopioitaisiin asiakirjasta, jota käytät lähteenä muille tiedoille.  
    * Kopioi täsmällisesti -vaihtoehto luo tarkan kopion tilausasiakirjan otsikon ja rivien kaikkien kenttien arvoista. Jos tämä vaihtoehto ei ole valittuna, monessa toimittajaan ja tuotteisiin liittyvissä kentässä käytetään oletusarvoja, aivan kuin loisit uutta tilausta manuaalisesti. Jos esimerkiksi tilauksessa, josta kopioit ohitettiin toimittajan oletuslaskutustili, kyseinen laskutustili kopioidaan tilaukseesi. Jos et ole valinnut Kopioi täsmällisesti -vaihtoehtoa, toimittajan oletuslaskutustiliä käytetään tilauksessasi sen sijaan.  
    * Poista ostorivit -vaihtoehto poistaa kaikki ostotilausrivit, jotka ovat jo kopioinnin kohteena olevalla ostotilauksella, ennen uusien rivien lisäämistä. Käytä tätä vaihtoehtoa varoen, koska se poistaa kaikki aiemmin luodut rivit ilman varoitusta.  
    * Jos käytät Kopioi tilausotsikko -vaihtoehtoa, uuteen tilaukseen ei tarvitse luoda otsikkotietoja manuaalisesti. Huomaa, että tämän asetuksen kanssa käytetään oletusarvoja toimittajaan liittyvissä kentissä. Jos lähdeasiakirjassa on ei-oletusarvoja, jotka haluat myös kopioida, käytä lisäksi Kopioi täsmällisesti -vaihtoehtoa.  
8. Tiivistä Parametrit-osa.
    * Kopioinnissa käytettäviä asiakirjalähteitä on erilaisia, ja jokaisella on oma osansa tällä sivulla. Esimerkiksi Ostotilaukset-osassa voit kopioida olemassa olevista ostotilauksista.  
9. Napsauta ostotilauksen riviä, jonka tunnus on 00015. 
10. Valitse rivi valitsemalla valintaruutu.
11. Poista rivin valintaruudun valinta, jotta sitä ei kopioitaisi tilaukseen.
    * Olet nyt valinnut 4 riviä kopioitavaksi ostotilaukseen. Voit valita lisää ostotilausrivejä muista ostotilauksista ja kopioida myös ne tilaukseesi. On myös mahdollista lisätä rivejä muista ostoasiakirjoista. Seuraavissa vaiheissa tarkastellaan näitä vaihtoehtoja.  
12. Tiivistä Ostotilaukset-osa.
13. Laajenna Vahvistus-osa.
    * Tässä voit valita kopioinnin lähteeksi ostotilauksen vahvistuksen. Ostotilauksen vahvistuksen tunnistat liittyvästä ostokirjauskansion tunnuksesta tai ostotilauksen tunnuksesta.  
14. Tiivistä Vahvistus-osa.
15. Laajenna Tuotteiden vastaanotot -osa.
    * Tässä voit valita kopioinnin lähteeksi tuotteen vastaanottokirjauksen. Tuotteen vastaanottokirjaukset tunnistat tuotteen vastaanottotositteesta tai ostotilauksen tunnuksesta.   
16. Tiivistä Tuotteiden vastaanotot -osa.
17. Laajenna Laskut-osa.
    * Tässä voit valita kopioinnin lähteeksi toimittajan laskun. Laskut tunnistat laskutustositteesta tai ostotilauksen tunnuksesta.   
18. Tiivistä Laskut-osa.
19. Laajenna Kopioitavat valitut rivit tai kopioitava otsikko -osa.
    * Tämä näkymä sisältää yhteenvedon kaikista asiakirjoista ja riveistä, jotka on valittu kopioitavaksi uuteen tilaukseen.   
20. Tiivistä Kopioitavat valitut rivit tai kopioitava otsikko -osa.
21. Valitse OK.
    * Valitsemasi 4 riviä on nyt kopioitu uuteen ostotilaukseen.   

## <a name="copy-lines-to-an-existing-purchase-order"></a>Kopioi rivejä vanhaan ostotilaukseen
    * Sen sijaan, että kopioisit kokonaisen tilauksen, on tavallisempaa luoda uusi ostotilaus, täyttää ostotilauksen otsikon tiedot ja kopioida sitten yksittäiset rivit vanhoista tilauksista.  
1. Valitse Ostotilausrivi.
2. Valitse Kaikista.
    * Aukeava sivu on samanlainen kuin aiemmin näytetty, mutta tilausrivinäkymästä avattaessa siihen valitaan eri vaihtoehdot. Tarkastellaan parametreja tarkemmin.   
3. Laajenna Parametrit-osa.
    * Poista valittu ostoehdotusrivi -vaihtoehto ei ole valittuna. Tämä tarkoittaa sitä, että voit kopioida uusia rivejä tilaukseen poistamatta olemassa olevia rivejä.   
    * Kopioi otsikon tilaus -vaihtoehto ei myöskään ole valittuna, koska lisäämme vain rivejä tilaukseen.   
4. Tiivistä Parametrit-osa.
    * Tässä esimerkissä kopioidaan rivejä vanhasta ostotilauksesta.   
5. Napsauta ostotilauksen riviä, jonka tunnus on 00034. 
6. Valitse rivi valitsemalla valintaruutu.
    * Huomaa, että ostotilauksen yksittäinen tilausrivin on myös valittu.  
7. Valitse OK.
    * Uusi tilausrivi on lisätty ostotilaukseen.  


