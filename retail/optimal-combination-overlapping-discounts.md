---
title: "Määrittää optimaalinen yhdistelmä päällekkäisiä alennuksia"
description: "Kun päällekkäisiä alennuksia, sinun on selvitettävä yhdistelmä, joka tuottaa pienin tapahtuman summa päällekkäisiä alennuksia tai suurin kokonaisalennus. Alennuksen määrä vaihtelee mukaan tuotteet, jotka on ostettu hinta, kun niitä tarkastellaan yhteisen &quot;ostaa 1, käytön 1 X prosenttia&quot; (BOGO) vähittäismyynnin alennus, tämä prosessi tulee ongelman combinatorial optimointi."
author: kfend
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 89643
ms.assetid: 09843c9a-3e19-4e4a-a8ce-80650f2095f9
ms.search.region: global
ms.search.industry: Retail
ms.author: kfend
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: 31e5104045ed5b8fbfa3677a7f5702d551de4231
ms.lasthandoff: 03/31/2017


---

# <a name="determine-the-optimal-combination-of-overlapping-discounts"></a>Määrittää optimaalinen yhdistelmä päällekkäisiä alennuksia

Kun päällekkäisiä alennuksia, sinun on selvitettävä yhdistelmä, joka tuottaa pienin tapahtuman summa päällekkäisiä alennuksia tai suurin kokonaisalennus. Alennuksen määrä vaihtelee mukaan tuotteet, jotka on ostettu hinta, kun niitä tarkastellaan yhteisen "ostaa 1, käytön 1 X prosenttia" (BOGO) vähittäismyynnin alennus, tämä prosessi tulee ongelman combinatorial optimointi.

Tämä artikkeli koskee Microsoft Dynamics AX 2012: n R3 kt 3105973 (julkaistu 2 marraskuussa-2015) tai myöhemmin ja helmikuu 2016 vapauttaa Microsoft Dynamics AX: n. Voit selvittää yhdessä päällekkäisiä alennuksia hyvissä ajoin ja jatkaa rich discounting tavalla, joka on saatavilla Microsoft Dynamics AX for Retail-olemme ovat ottaneet käyttöön menetelmän soveltamisesta päällekkäisiä alennuksia. Kutsumme tätä uutta tapaa **rajan arvon luokittelu**. Rajan arvon luokittelu käytetään aika, joka vaaditaan, jotta voidaan arvioida mahdolliset yhdistelmät päällekkäisiä alennuksia ylittää raja-arvon, joka määritetään, kun **vähittäismyynnin parametreja** Dynamics AX-sivulla. Rajan arvon menetelmän luokittelu arvo lasketaan kunkin päällekkäisen alennus alennuksen arvo käyttämällä jaettuja tuotteita. Päällekkäisen alennukset kohdistetaan suurin suhteellinen arvo suhteellinen arvo on pienin. Lisätietoja uusi menetelmä on jäljempänä tässä artikkelissa olevassa "Rajan arvo"-osassa. Rajan arvon luokittelu ei ole käyttää, kun tuotteen alennussummat vaikutakaan tapahtuman toisen tuotteen. Tätä menetelmää ei käytetä esimerkiksi yksinkertainen alennuksen tai yksinkertainen alennus ja alennuksen määrä yhden tuotteen.

## <a name="discount-examples"></a>Esimerkkejä alennus
Dynamics AX: ssä voit luoda rajoittamattoman määrän vähittäismyynnin alennuksia yhteisiä tuotteita. Kuitenkin ei ole rajoitettu, koska suorituskyvyn ongelmat voivat ilmetä, kun yrität laskea alennukset, joita käytetään eri tuotteissa. Seuraavissa esimerkeissä kuvataan tarkemmin tämän ongelman. Esimerkissä 1 emme Aloita tuotteita ja kaksi päällekkäisiä alennuksia. Sitten Esimerkki 2, näytämme, miten ongelma siihen on lisätty muita tuotteita.

### <a name="example-1-two-products-and-two-discounts"></a>Esimerkki 1: Kaksi tuotetta ja kaksi alennukset

Tässä esimerkissä kaksi tuotetta tarvitaan kunkin alennuksen saadakseen ja alennuksia ei voi yhdistää. Tässä esimerkissä alennukset ovat **paras hinta** alennuksia. Molemmat tuotteet sekä alennuksia voidaan myöntää. Tähän on kaksi alennuksia. [![Combo-01 alennus päällekkäisiä](./media/overlapping-discount-combo-01.jpg)](./media/overlapping-discount-combo-01.jpg) minkä tahansa kahden tuotteen parempi näistä kahdesta alennukset riippuu tuotteiden hinnat. Molempien tuotteiden hinta on sama tai lähes sama, kun alennus 1 on parempi. Kun yhden tuotteen hinta on huomattavasti pienempi kuin muut tuotteen hinta, alennus 2 on parempi. Tässä arvioinnissa toisiaan vastaan nämä kaksi alennukset matemaattisia säännön on: [![Overlapping alennus combo 02](./media/overlapping-discount-combo-02.jpg)](./media/overlapping-discount-combo-02.jpg) Huomaa, että kaksi kolmasosaa 2 tuotteen hinta on 1 tuotteen hintaan, kun kaksi alennukset ovat yhtä. Tässä esimerkissä tehokas alennusprosentti alennus 1 vaihtelee muutaman prosentin (kun kaksi tuotteiden hinnat ovat kaukana toisistaan) on enintään 25 prosenttia (kun kaksi tuotetta on sama hinta). Tehokas alennusprosentti alennus 2 on korjattu. Se on aina 20 prosenttia. Koska tehokas alennusprosentti alennus 1 on alue, joka voi olla suurempi tai pienempi kuin alennus 2, paras alennus riippuu kaksi tuotetta, jotka on alennettu hinta. Tässä esimerkissä laskutoimitukset on suoritettu nopeasti, koska vain kaksi alennuksia tuotteista vain kaksi. On vain kaksi mahdollista yhdistelmät: 2 alennus alennus 1 tai yksi soveltamisen yhteen sovellukseen. Ei ole permutaatioiden laskemiseen. Kunkin alennuksen arvo lasketaan käyttämällä sekä tuotteet ja parhaat alennusta käytetään.

### <a name="example-2-four-products-and-two-discounts"></a>Esimerkki 2: Neljä tuotteet ja kaksi alennukset

Seuraavaksi Käytämme neljä tuotteiden ja saman alennuksen. Kaikki neljä tuotteet sekä alennuksia voidaan myöntää. On 12 mahdolliset yhdistelmät. Lopuksi kaksi alennuksia sovelletaan tapahtumaa kolmen yhdistelmät: kaksi alennus 1, kaksi sovellukset sovellukset alennus alennus 2 1 ja toinen alennuksen soveltamisen 2 tai yksi sovellus. Kuvaamaan mahdolliset yhdistelmät tarkastelemme neljä tuotteet, joilla on eri hinnat eri kahdet:

-   Kaikki neljä tuotteilla on sama hinta $15.00. Tässä tapauksessa alennus paras yhdistelmä on kaksi sovellusta alennus 1. Tuotteita on koko hinnan ja kaksi on 50 prosenttia pois. Tapahtuman kokonaisalennus on käytöstä $60 diskonttaamattomina yhteensä $45 (15 + 15 + 7.50 + 7.50), joka on $15 (25 prosenttia). Alennus 2 on vain $12 (20 prosenttia).
-   Tuotteet ovat aina $20, yksi tuote on $15 ja yksi tuote on $5. Tässä tapauksessa alennus paras yhdistelmä on yksi sovellus 2 ja toinen alennuksen soveltamisen alennus 1. Seuraavissa taulukoissa on kuvattu alennukset.

Lukeminen taulukoita, käytä yhden rivin ja sarakkeen yhden tuotteet. Esimerkiksi taulukon alennus 1, kun yhdistät kaksi $20, tuotteita saat $10. Taulukossa 2 on voimassa kun yhdistät tuotteen $15 ja $5, tuotteen saat $4. [![Päällekkäiset alennus combo 03](./media/overlapping-discount-combo-03.jpg)](./media/overlapping-discount-combo-03.jpg) emme Etsi suurin alennus, joka on käytettävissä kaksi tuotteita käyttämällä joko alennus. Taulukot Näytä kaikki yhdistelmät tuotteet alennussumma. Varjostetut osuudet taulukot edustavat molemmissa tapauksissa, johon tuote on yhdistetty itse, joita emme voi tehdä tai käänteinen laiteparin, kaksi tuotetta, joka tuottaa saman alennuksen suuruus ja voidaan jättää huomiotta. Katsomalla taulukoista näet niitä kahta $20, alennus 1 on suurin alennus, joka on saatavilla joko neljä kaikista tuotteista alennusta. (Tämä alennus näkyy korostettuna ensimmäisen taulukon vihreä.) Joka lähtee vain $15 tuote ja $5 tuote. Katsomalla taulukot uudelleen, näet, että näiden kahden tuotteen alennus 1 antaa $2.50 alennus, alennuksen 2 antaa alennuksen $4 vuoksi. Näin ollen voimme valita alennuksen 2. Kokonaisalennus on $14. Helpottaa tätä keskustelua havainnollistaa, tässä on kaksi taulukoita, ja näyttäminen sekä alennus 1 kaikki mahdolliset kahden tuote yhdistelmät tehokas alennusprosentti alennus 2. Vain puolet yhdistelmien luetteloa ei, koska nämä kaksi alennuksia, jossa kaksi tuotteita markkinoille alennuksen tilauksen yhdentekevä. Korkein tehokas alennus (25 prosenttia) korostetaan vihreää ja pienin tehokas alennus (10 prosenttia) on korostettu punaisella. [![Combo-04 alennus päällekkäisiä](./media/overlapping-discount-combo-04.jpg)](./media/overlapping-discount-combo-04.jpg)**Huomautus:** hinnat vaihtelevat, ja kilpailla kahden tai useamman alennuksen, kun alennukset sekä arvioida ja verrata niitä on ainoa tapa taata paras yhdistelmä alennuksia.

## <a name="total-possible-combinations"></a>Yhteensä mahdolliset yhdistelmät
Tässä osassa edelleen Esimerkki edellisestä osasta. Olemme lisätä enemmän tuotteita ja toinen alennuksen ja laskea kuinka monta yhdistelmää ja verrattuna. Seuraavassa taulukossa on esitetty mahdollisista alennusyhdistelmistä määrä tuotteen määrän vähentymisenä. Taulukosta näkyy, mitä tapahtuu, kun on kaksi päällekkäisiä alennuksia, kuten edellisessä esimerkissä, ja kun on kolme päällekkäisiä alennuksia. Mahdollisen alennuksen yhdistelmätyypit, joita on arvioitava määrä ylittää pian nopea tietokone voi laskea ja verrata pitää hyväksyttävänä Vähittäismyyntitapahtumille tarpeeksi nopeasti. [![Combo-05 alennus päällekkäisiä](./media/overlapping-discount-combo-05.jpg)](./media/overlapping-discount-combo-05.jpg) kun jopa suurempia määriä tai useita päällekkäisiä alennuksia mahdollisista alennusyhdistelmistä määrä siirtyy nopeasti miljoonia ja aika, joka vaaditaan, jotta voidaan arvioida ja valita paras mahdollinen yhdistelmä nopeasti tulee havaittavissa. Jotkut optimoinnit on tehty-retail hinta moottorin vähentää määrä yhdistelmiä, jotka on arvioitava. Kuitenkin määrä päällekkäisiä alennuksia ja tapahtumassa määrät eivät ole rajoitettu, koska paljon yhdistelmiä on aina arvioitava aina, kun on päällekkäisiä alennuksia. Tämä ongelma on ongelma, joka korjaa menetelmän luokittelu rajan arvo.

## <a name="marginal-value-method"></a>Rajan arvon laskentatapa
Optimointia on humanististen määrän yhdistelmiä, jotka on arvioitava ongelman ratkaisemiseksi, joka laskee kunkin joukko tuotteita, jotka kahden tai useamman alennuksia voidaan soveltaa alennusta jaetun tuotekohtaisesti. Viittaamme kuin tämä arvo **rajan arvo** alennuksen jaetun tuotteille. Rajan arvo tuotteen kokonaisalennussumma nousua kohden keskimäärin kun jaetun tuotteet sisältyvät kunkin alennuksen. Rajan arvo lasketaan ottamalla alennussumman ilman jaettua tuotteiden alennusten kokonaissummaa (DTotal), (DMinus\\ jaettu), ja jakamalla kyseinen erotus jaettuja tuotteita (ProductsShared). [![Päällekkäiset alennus combo 06](./media/overlapping-discount-combo-06.jpg)](./media/overlapping-discount-combo-06.jpg) rajan, kunkin alennuksen jaetun joukon tuotteiden arvo lasketaan, kun alennusten järjestyksessä, jaettuja tuotteita yksilöityinä, suurin rajan arvosta pienimpään rajan. Tämä menetelmä kaikkien jäljellä olevien alennusmahdollisuudet eivät ole verrattuna aina yhden esiintymän, alennuksen jälkeen. Sen sijaan päällekkäisiä alennuksia verrattuna yhden kerran ja sitten soveltaa järjestyksessä. Ei ole muita vertailuja on tehty. Voit määrittää rajan arvon menetelmä siirtyminen raja **alennus** -välilehdessä **vähittäismyynnin parametreja** sivun. Hyväksyttävä aika Kokonaisalennus lasketaan, vaihtelee eri toimialoja vähittäiskaupan. Tällä hetkellä kuuluu kuitenkin yleensä kymmenien millisekunteina yhden sekunnin välillä.


