---
title: Ostopalautustilauksen luonti
description: Seuraavassa menettelyssä kuvataan, miten luot ostopalautustilauksen kopioimalla toimittajan laskuasiakirjan rivit uuteen ostotilaukseen käyttämällä Hyvityslasku-toimintoa.
author: mkirknel
manager: tfehr
ms.date: 06/25/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchTable, PurchTablePart, PurchCreateOrder, PurchCopying, InventMarking, PurchEditLines
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 635e9ffb629a844bc5cccfa5d2a538ef0cf098d9
ms.sourcegitcommit: e3f4dd2257a3255c2982f4fc7b72a1121275b88a
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/16/2020
ms.locfileid: "4018187"
---
# <a name="create-a-purchase-return-order"></a>Ostopalautustilauksen luonti

[!include [banner](../../includes/banner.md)]

Seuraavassa menettelyssä kuvataan, miten luot ostopalautustilauksen kopioimalla toimittajan laskuasiakirjan rivit uuteen ostotilaukseen käyttämällä Hyvityslasku-toimintoa. Se kerrotaan myös, miten vahvistat tilauksen ja käsittelet tuotteiden lähettämisen takaisin toimittajalle. Tämän oppaan esimerkissä käytetään esittely-yritys USMF:n tietoja. Yleensä ostoedustaja tekee tämän tehtävän.

## <a name="create-a-new-purchase-return-order"></a>Luo uusi ostopalautustilaus
1. Siirry siirtymisruudussa kohtaan **Moduulit > Hankinta > Ostotilaukset > Kaikki ostotilaukset**. Ensimmäinen vaihe on luoda uusi ostotilaus, jota käytetään ostopalautustilauksena.  
2. Valitse **Uusi**.
3. Kirjoita **Toimittajan tili** -kenttään arvoksi US-102.
4. Valitse **OK**.
5. Valitse **toimintoruudussa** **Osto**.
6. Valitse **Hyvityslasku**. Tältä sivulta voit kopioida tietoja olemassa olevasta toimittajan laskusta palautustilaukseesi. Tämä on sama sivu, jota käytetään muihin kopiointitoimintoihin. Mutta koska se on avattu hyvityslaskun toiminnosta, sivu on määritetty tukemaan palautustilauksen luontia, joka vastakirjaa toimittajalaskuja.  
7. Laajenna **Parametrit** -osa.
    - **Vaihda etumerkki** -vaihtoehto valitaan automaattisesti eikä sitä voi muuttaa. Näin varmistetaan, että määrien etumerkki muutetaan ja lisättävät tilausrivit vastakirjaavat toimittajan laskun.  
    - **Kopioi kulut** -vaihtoehto valitaan automaattisesti eikä sitä voi muuttaa. Tällöin toimittajan laskun kulut lisätään ostopalautustilaukseen alkuperäisten kulujen vastakirjaamiseksi. Muutoksia voi muokata myöhemmin tilauksen otsikossa ja riveillä.  
    - **Kopioi täsmällisesti** -vaihtoehto valitaan automaattisesti eikä sitä voi muuttaa. Tämä varmistaa, että kaikki toimittajan laskun otsikon ja rivien kenttien arvot kopioidaan tarkasti. Tämä tarkoittaa, että ostopalautustilaus luodaan arvoille, jotka vastaavat kaikkia toimittajan laskuasiakirjan ehtoja. 
    - **Poista ostorivit** -vaihtoehto poistaa kaikki ostotilausrivit, jotka ovat jo olevalla ostotilauksella, ennen uusien rivien lisäämistä. Tässä esimerkissä ostopalautustilaukseen ei ole vielä lisätty rivejä, eli tässä tapauksessa vaikutusta ei ole. Käytä tätä vaihtoehtoa varoen, koska se poistaa kaikki aiemmin luodut rivit ilman varoitusta.  
    * **Kopioi tilausotsikko** -vaihtoehto valitaan automaattisesti eikä sitä voi muuttaa. Näin varmistetaan, että toimittaja laskun tiedot kopioidaan ja otetaan käyttöön ostopalautustilauksen otsikossa. Tästä on hyötyä, koska se varmistama, että ostopalautustilaus vastakirjaa laskun samanlaisin ehdoin.  
8. Tiivistä **Parametrit** -osa.
9. Laajenna **Laskut** -osa. Sivu on avattu hyvityslaskutoiminnosta, joten ainoa vaihetoehto on kopioida tietoja toimittajan laskuista. Tämä välilehti sisältää kaikki käytettävissä olevat toimittajatilin laskut, jotka on määritetty aiemmin luodussa ostopalautustilauksessa.   Laskut tunnistat laskutustositteesta tai ostotilauksen tunnuksesta.
10. Etsi toimittajan lasku, jonka tunnisteena on laskunumero AP-0006 ja valitse rivi napsauttamalla mitä tahansa rivin kenttää.
11. Valitse rivi valitsemalla sen valintaruutu. Huomaa, että toimittajan laskun käytettävissä olevat rivit on valittu automaattisesti tilauksen kanssa. Tällä nimenomaisella toimittajan laskulla on 2 tilausriviä. Tässä esimerkissä palautetaan osa toisen rivin määrästä.
12. Valitse toinen rivi (rivillä on nimike M0006) napsauttamalla mitä tahansa kyseiselle rivin kenttää.
13. Muuta **Määrä** -kentän arvoksi 10. Tämä on toimittajalle palautettava määrä. 
14. Valitse ensimmäinen rivi (rivillä on nimike M0005) napsauttamalla mitä tahansa kyseiselle rivin kenttää.
15. Poista rivin valintaruudun merkintä. Vain rivit, jotka olet valinnut kopioidaan tilaukseen.
16. Tiivistä **Laskut** -osa.
17. Laajenna **Kopioitavat valitut rivit tai kopioitava otsikko** -osa. Tämä näkymä sisältää yhteenvedon kaikista asiakirjoista ja riveistä, jotka on valittu kopioitavaksi uuteen tilaukseen.  
18. Tiivistä **Kopioitavat valitut rivit tai kopioitava otsikko** -osa.
19. Valitse **OK**. Valitsemasi rivi on nyt kopioitu uuteen ostopalautustilaukseen. **Määrä** -kentän arvo on -10.   
20. Valitse **Ostotilausrivi** -osa **Varasto**.
21. Valitse **Merkintä**. Luotu toimittajan laskun tilausrivi merkitään vastaamaan varastotapahtumaa. Näin varmistetaan, että toimittajalle palautettavat nimikkeet ovat samat, jotka toimittajalta on vastaanotettu. Joissain tilanteissa merkintää ei tapahdu, kuten jos varasto on jo merkitty kulutetuksi tai tuote on sellainen, jolla merkintää ei käytetä.  

22. Valitse **OK**.

## <a name="confirm-and-record-the-shipment-of-goods"></a>Vahvista ja kirjaa tavaroiden toimitus
1. Valitse **Toiminnot > Vahvista**.
2. Valitse **toimintoruudussa** **Vastaanota**.
3. Valitse **Tuotteen vastaanotto**.
    - Tällä sivulla kirjataan tuotteen vastaanotto ostotilauksille sekä käsitellään tuotteiden palauttaminen toimittajalle. Tilausrivit, joilla on negatiivinen määrä tarkoittavat, että tavarat palautetaan toimittajalle, ja että tältä sivulta luotavaa asiakirjaa voi käyttää pakkausluettelona tätä varten.   
    - Valitse tässä esimerkissä **Määrä** -kentän arvoksi Tilattu määrä. Näin varmistetaan, että lähetys käsitellään koko tilatulle määrälle, jolle tilausrivit luotiin.   
4. Kirjoita arvo **Tuotteen vastaanotto** -kenttään. Tätä kenttää käytetään syöttämään viite, jota käytetään tositteena tuotteen vastaanoton kirjauskansiossa.  
5. Valitse **OK**. Tavarat on nyt tallennettu lähetetyiksi ostopalautustilauksella, ja sitä vastaava tuotteen vastaanoton kirjauskansio on luotu. Voit käyttää Tuotteen vastaanotto -toimintoa ostotilauksesta luotujen kirjauskansioiden tarkasteluun selvittääksesi mitä on vastaanotettu tai palautettu ja milloin.  

