---
title: Toistuvan ostotilauksen luonti
description: Tässä artikkelissa kuvataan, miten luot toistuvan ostotilauksen (PO) kopioimalla rivejä vanhasta ostotilauksesta uuteen tai vanhaan ostotilaukseen.
author: GalynaFedorova
ms.date: 09/30/2020
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: PurchTable, PurchTablePart, PurchCreateOrder, PurchCopying
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: gfedorova
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 335461d60fa0bc92e9711806c6e42643a3f75d02
ms.sourcegitcommit: 073604c07116e0a87f78ab2c76cb89ae83ebba3c
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/30/2022
ms.locfileid: "9608103"
---
# <a name="create-a-repeat-purchase-order"></a>Toistuvan ostotilauksen luonti

[!include [banner](../../includes/banner.md)]

Tässä artikkelissa kuvataan, miten luot toistuvan ostotilauksen (PO) kopioimalla rivejä vanhasta ostotilauksesta uuteen tai vanhaan ostotilaukseen. Toistuvien tilausten luomiseen on kaksi tapaa. Voit käyttää käytettävissä olevia asiakirjatason toimintoja toimintoruudusta tai rivin tietojen toimintoja. Asiakirjan tason toiminnot on tarkoitettu uuden ostotilauksen luomiseen lisäämällä otsikkotiedot ja rivit toisesta tilauksesta, ja rivin tietojen toiminnot on taas tarkoitettu rivien lisäämiseen vanhaan tilaukseen. Tämän oppaan esimerkissä käytetään esittely-yritys USMF:n tietoja. Yleensä ostoedustaja tekee tämän tehtävän.

## <a name="create-a-new-repeat-purchase-order"></a>Luo uusi toistuva ostotilaus

1. Siirry siirtymisruudussa kohtaan **Moduulit \> Hankinta \> Ostotilaukset \> Kaikki ostotilaukset**. Yritetään ensin vaihtoehtoa kopioida tiedot uuteen tilaukseen.  
1. Valitse **Uusi**.
1. Kirjoita **Toimittajan tili** -kenttään arvoksi `US-101`.
1. Valitse **OK**.
1. Avaa toimintoruudussa **Ostotilaus**-välilehti ja valitse **Kopioi**-ryhmässä **Kaikista**. **Kopioi muista asiakirjoista** -valintaikkuna avautuu. Tässä voit kopioida olemassa olevista tilauksista omaan tilaukseesi. Rivien kopiointiin on erilaisia vaihtoehtoja, ja kopioinnin lähdeasiakirjoja on myös erilaisia. Tarkastelemme rivien kopiointitapojen vaihtoehtoja ensin.
1. Laajenna **Parametrit**-pikavälilehti.

    - **Määräkerroin**-kenttä on hyödyllinen, jos sinun on käytettävä määrää, joka poikkeaa kopioinnin lähteenä olevan tilauksen määrästä. Jos esimerkiksi haluat tilata kaksinkertaisen määrän kopioinnin lähteenä oleviin riveihin verrattuna, kirjoita tähän kenttään "2" ja järjestelmä lisää rivit, joissa alkuperäinen määrä on kaksinkertainen.  
    - Myös **Vaihda etumerkki** -kenttä tukee tilatun määrän muuttamista vaihtamalla lisättyjen tilausrivien määrän etumerkin. Voi olla hyötyä, jos sinun on peruutettava tapahtuma luomalla tilausrivejä, jotka kumoavat tapahtuman. Tämä vaihtoehto valitaan automaattisesti, kun sivu avataan **Luo hyvityslasku** -toiminnolla.  
    - **Kopioi kulut** -vaihtoehdon avulla voit kopioida kulut uuteen tilaukseen tilausrivien lähteenä olevasta asiakirjasta.  
    - **Laske hinnat uudelleen** -vaihtoehto käyttää nykyisiä hintoja ja alennuksia sen sijaan, että ne kopioitaisiin asiakirjasta, jota käytät lähteenä muille tiedoille.  
    - **Kopioi täsmällisesti** -vaihtoehto kopioi tilausasiakirjan otsikon ja rivien useiden kenttien arvot. Jos tämä vaihtoehto ei ole valittuna, monessa toimittajaan ja tuotteisiin liittyvissä kentässä käytetään oletusarvoja, aivan kuin uuden tilauksen manuaalisen luomisen yhteydessä. Jos esimerkiksi määrität **Kopioi täsmällisesti** -kohdan arvoksi *Kyllä* ja kopioit tilauksen, joka korvaa toimittajan oletuslaskutustilin, tämä sama laskutustili kopioidaan uuteen tilaukseen. Jos olet määrittänyt **Kopioi täsmällisesti** -vaihtoehdon arvoksi *Ei*, toimittajan oletuslaskutustiliä käytetään tilauksessasi sen sijaan. Seuraavien kenttien arvot kopioidaan, kun **Kopioi täsmällisesti** -kohdan arvoksi on määritetty *Kyllä*:
        - Kieli
        - Maksuehdot
        - Maksutapa
        - Maksumäärittely
        - Numerosarjaryhmä
        - Käteisalennus
        - Alennusprosentti
        - Valuutta
        - Toimitusehdot
        - Toimitustapa
        - Dimensio
        - Arvonlisäveroryhmä
        - Ohita arvonlisävero
        - Hinnat sisältävät arvonlisäveron
        - Välitys
        - Portti
        - Tilastomenettely
        - Mallitunnus
        - Toimitusasiakkaan nimi
        - Postiosoite
        - Viite
        - Viitetaulun tunnus
    - **Poista ostorivit** -vaihtoehto poistaa kaikki ostotilausrivit, jotka ovat jo kopioinnin kohteena olevalla ostotilauksella, ennen uusien rivien lisäämistä. Käytä tätä vaihtoehtoa varoen, koska se poistaa kaikki aiemmin luodut rivit ilman varoitusta.  
    - Jos käytät **Kopioi tilausotsikko** -vaihtoehtoa, uuteen tilaukseen ei tarvitse luoda otsikkotietoja manuaalisesti. Tämän asetuksen kanssa käytetään oletusarvoja toimittajaan liittyvissä kentissä. Jos lähdeasiakirjassa on ei-oletusarvoja, jotka haluat myös kopioida, käytä lisäksi **Kopioi täsmällisesti** -vaihtoehtoa.
    - Kopioinnissa käytettäviä asiakirjalähteitä on erilaisia, ja jokaisella on oma osansa tällä sivulla. Esimerkiksi **Ostotilaukset**-osassa voit kopioida olemassa olevista ostotilauksista.  

1. Valitse **Ostotilaukset**-osassa rivit, jotka haluat kopioida leikepöydälle. Voit valita lisää ostotilausrivejä muista ostotilauksista ja kopioida myös ne tilaukseesi. On myös mahdollista lisätä rivejä muista ostoasiakirjoista. Seuraavissa vaiheissa tarkastellaan näitä vaihtoehtoja.  
1. Laajenna **Vahvistus**-osa. Tässä voit valita kopioinnin lähteeksi ostotilauksen vahvistuksen. Ostotilauksen vahvistuksen tunnistat liittyvästä ostokirjauskansion tunnuksesta tai ostotilauksen tunnuksesta.  
1. Laajenna **Tuotteiden vastaanotot** -osa. Tässä voit valita kopioinnin lähteeksi tuotteen vastaanottokirjauksen. Tuotteen vastaanottokirjaukset tunnistat tuotteen vastaanottotositteesta tai ostotilauksen tunnuksesta.
1. Laajenna **Laskut**-osa. Tässä voit valita kopioinnin lähteeksi toimittajan laskun. Laskut tunnistat laskutustositteesta tai ostotilauksen tunnuksesta.
1. Laajenna **Kopioitavat valitut rivit tai kopioitava otsikko** -osa. Tämä näkymä sisältää yhteenvedon kaikista asiakirjoista ja riveistä, jotka on valittu kopioitavaksi uuteen tilaukseen.
1. Valitse **OK**. Valitsemasi rivit on nyt kopioitu uuteen ostotilaukseen.

## <a name="copy-lines-to-an-existing-purchase-order"></a>Kopioi rivejä vanhaan ostotilaukseen  

Sen sijaan, että kopioisit kokonaisen tilauksen, on tavallisempaa luoda uusi ostotilaus, täyttää ostotilauksen otsikon tiedot ja kopioida sitten yksittäiset rivit vanhoista tilauksista.  

1. Valitse **Ostotilausrivi**.
1. Valitse **Kaikista**. Aukeava sivu on samanlainen kuin aiemmin näytetty, mutta tilausrivinäkymästä avattaessa siihen valitaan eri vaihtoehdot. Tarkastellaan parametreja tarkemmin.
1. Laajenna **Parametrit**-osa.

    - **Poista ostorivit** -vaihtoehto ei ole valittuna. Tämä tarkoittaa sitä, että voit kopioida uusia rivejä tilaukseen poistamatta olemassa olevia rivejä.
    - **Kopioi otsikon tilaus** -vaihtoehto ei myöskään ole valittuna, koska lisäämme vain rivejä tilaukseen.
    - Tässä esimerkissä kopioidaan rivejä vanhasta ostotilauksesta.

1. Valitse halutun ostotilauksen rivi. Huomaa, että ostotilauksen yksittäinen tilausrivin on myös valittu.  
1. Valitse **OK**. Uusi tilausrivi on lisätty ostotilaukseen.  

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]