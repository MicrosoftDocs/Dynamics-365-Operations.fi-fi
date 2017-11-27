---
title: "Määritä optimaalinen yhdistelmä päällekkäisiä alennuksia"
description: "Kun alennukset menevät päällekkäin, sinun on määritettävä alennuksien yhdistelmä, joka tuottaa pienimmän tapahtumasumman tai suurimman kokonaisalennuksen. Kun alennuksen määrä vaihtelee ostettujen tuotteiden hinnan mukaan (kuten yleisessä vähittäismyynnin \"osta 1, saat toisen X prosentin alennuksella\" -alennuksessa), tästä prosessista tulee yhdistelmäoptimoinnin ongelma."
author: kfend
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations, Retail
ms.custom: 89643
ms.assetid: 09843c9a-3e19-4e4a-a8ce-80650f2095f9
ms.search.region: global
ms.search.industry: Retail
ms.author: kfend
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 4b561503efa24bc4017a4c4360e0355ce39e2f56
ms.contentlocale: fi-fi
ms.lasthandoff: 11/03/2017

---

# <a name="determine-the-optimal-combination-of-overlapping-discounts"></a>Määritä optimaalinen yhdistelmä päällekkäisiä alennuksia

[!include[banner](includes/banner.md)]


Kun alennukset menevät päällekkäin, sinun on määritettävä alennuksien yhdistelmä, joka tuottaa pienimmän tapahtumasumman tai suurimman kokonaisalennuksen. Kun alennuksen määrä vaihtelee ostettujen tuotteiden hinnan mukaan (kuten yleisessä vähittäismyynnin "osta 1, saat toisen X prosentin alennuksella" -alennus), tästä prosessista tulee yhdistelmäoptimoinnin ongelma.

Tämä artikkeli koskee Microsoft Dynamics AX 2012 R3 KB 3105973 (julkaistu 2.11.2015) tai uudempaa versiota sekä Microsoft Dynamics 365 for Retailia. Päällekkäisten alennusten käyttöä varten on otettu menetelmä, jolla voidaan määrittää päällekkäisten alennusten yhdistelmän käyttö mahdollisimman nopeasti. Kutsumme tätä uutta menetelmää **rajan-arvojen luokitteluksi**. Raja-arvojen luokittelua käytetään silloin kun aika, joka vaaditaan mahdollisten päällekkäisten alennusten yhdistelmien arvioimiseen, ylittää raja-arvon, joka määritetään **Vähittäismyynnin parametrit** -sivulla. Raja-arvon luokittelumenetelmässä arvo lasketaan kullekin päällekkäiselle alennukselle käyttämällä jaettujen tuotteiden alennuksen arvoa. Sitten päällekkäisiä alennuksia käytetään suurimmasta suhteellisesta arvosta pienimpään suhteelliseen arvoon. Lisätietoja tästä uudesta menetelmästä on jäljempänä tässä artikkelissa olevassa "Raja-arvo"-osassa. Raja-arvon luokittelua ei käytetä, kun tuotteen alennussummat eivät vaikuta tapahtuman toisiin tuotteisiin. Tätä menetelmää ei käytetä esimerkiksi kahden yksinkertaisen alennuksen tapauksessa tai yksinkertaisen määräalennuksen yhteydessä.

## <a name="discount-examples"></a>Esimerkkejä alennuksista
Voit luoda rajoittamattoman määrän vähittäismyynnin alennuksia yhteisille tuotejoukoille. Kuitenkin ilman rajoituksia saattaa ilmaantua suorituskyvyn ongelmia, kun yrität laskea alennukset, joita pitäisi käyttää eri tuotteissa. Seuraavissa esimerkeissä kuvataan tarkemmin tätä ongelmaa. Esimerkissä 1 aloitamme kahdesta tuotteesta ja kahdesta päällekkäisestä alennuksesta. Sitten esimerkissä 2 näytämme, miten ongelma kehittyy, kun tuotteita on useampia.

### <a name="example-1-two-products-and-two-discounts"></a>Esimerkki 1: Kaksi tuotetta ja kaksi alennusta

Tässä esimerkissä tarvitaan kaksi tuotetta kunkin alennuksen saadakseen ja alennuksia ei voi yhdistää. Tässä esimerkissä alennukset ovat **Paras hinta** -alennuksia. Molemmat tuotteet oikeuttavat molempiin alennuksiin. Tässä ovat nämä kaksi alennusta.
![Päällekkäisten alennusten yhdistelmä 01](./media/overlapping-discount-combo-01.jpg)

Mille tahansa kahdelle tuotteelle parempi näitä alennuksista määräytyy kummankin tuotteen hinnan perusteella. Kun molempien tuotteiden hinta on sama tai lähes sama, alennus 1 on parempi. Kun yhden tuotteen hinta on huomattavasti pienempi kuin toisen tuotteen hinta, alennus 2 on parempi. Näitä kahta alennusta voi vertailla keskenään tällä matemaattisella säännöllä: ![Päällekkäisten alennusten yhdistelmä 02](./media/overlapping-discount-combo-02.jpg)

**Huomautus:** Kun tuotteen 1 hinta on yhtä suuri kuin kaksi kolmasosaa tuotteen 2 hinnasta, kaksi alennusta ovat yhtä suuria. Tässä esimerkissä voimassa oleva alennusprosentti alennukselle 1 vaihtelee muutamasta prosentista (kun näiden kahden tuotteen hinnat ovat kaukana toisistaan) enintään 25 prosenttiin (kun kahdella tuotteella on sama hinta). Alennuksen 2 voimassa oleva alennusprosentti on kiinteä. Se on aina 20 prosenttia. Koska alennuksen 1 voimassa oleva alennusprosentti voi olla suurempi tai pienempi kuin alennus 2, paras alennus riippuu näiden kahden alennettavan tuotteen hinnoista. Tässä esimerkissä laskutoimitukset on suoritettu nopeasti, koska käytetään vain kahta alennusta kahteen tuotteeseen. On vain kaksi mahdollista yhdistelmää: alennuksen 1 yksi käyttö tai alennuksen 2 yksi käyttö. Tässä ei tarvitse laskea permutaatioita, koska niitä ei ole. Kunkin alennuksen arvo lasketaan käyttämällä kumpaakin tuotetta ja parasta alennusta käytetään.

### <a name="example-2-four-products-and-two-discounts"></a>Esimerkki 2: Neljä tuotetta ja kaksi alennusta

Seuraavaksi käytämme neljää tuotetta ja samaa kahta alennusta. Kaikki neljä tuotetta oikeuttavat molempiin alennuksiin. Tässä tapauksessa on 12 mahdollista yhdistelmää. Lopuksi kahta alennusta sovelletaan tapahtumaan jossain seuraavista kolmesta yhdistelmästä: kaksi alennuksen 1 käyttöä, kaksi alennuksen 2 käyttöä tai sekä yksi alennuksen 1 käyttö että yksi alennuksen 2 käyttö. Mahdollisten yhdistelmien esittelemiseksi tarkastelemme kahta eri neljän tuotteen joukkoa, joilla on eri hinnat:

-   Kaikilla neljällä tuotteella on sama hinta 15,00 $. Tässä tapauksessa paras alennusyhdistelmä on kaksi alennuksen 1 käyttöä. Kaksi tuotetta on täysihintaisia ja kahdesta tuotteesta saa 50 prosenttia alennusta. Tapahtuman alennettu loppusumma on 45 $ (15 + 15 + 7,50 + 7,50), joka on 15 $ (25 prosenttia) alentamattomasta hinnasta 60 $. Alennus 2 on vain 12 $ (20 prosenttia).
-   Kahden tuotteen hinta on 20 $, yhden tuotteen 15 $ ja yhden 5 $. Tässä tapauksessa paras alennusyhdistelmä alennuksen 2 yksi käyttö ja alennuksen 1 käyttö. Seuraavissa taulukoissa on kuvattu alennukset.

Voit lukea taulukoita käyttämällä yhtä tuotetta riviltä ja yhtä tuotetta sarakkeesta. Esimerkiksi alennuksen 1 taulukossa yhdistämällä kaksi 20 dollarin tuotetta saat alennusta 10 $. Alennuksen 2 taulukossa yhdistämällä yhden 15 dollarin tuotteen ja 5 dollarin tuotteen saat alennusta 4 $.
![Päällekkäisten alennusten yhdistelmä 03](./media/overlapping-discount-combo-03.jpg)

Ensin etsimme suurimman alennuksen, joka on saatavilla mille tahansa kahdelle tuotteelle käyttäen kumpaa tahansa alennusta. Nämä kaksi taulukkoa näyttävät kaikkien kahden tuotteen yhdistelmien alennussummat. Taulukoiden varjostetut osiot edustavat joko tuotteen yhdistämistä itsensä kanssa (jota ei voi tehdä) tai kahden tuotteen käänteistä yhdistämistä, joka tuottaa saman alennussumman (ja voidaan jättää huomiotta). Katsomalla taulukoita näet, että alennus 1 on kahdelle 20 dollarin tuotteelle suurin alennus, joka on saatavilla kummalla tahansa alennuksella kaikille neljälle tuotteelle. (Tämä alennus näkyy korostettuna ensimmäisessä taulukossa vihreällä.) Jäljelle jää vielä 15 ja 5 dollarin tuotteet. Katsomalla taulukoita uudelleen näet, että näille kahdelle tuotteelle alennus 1 antaa 2,50 dollarin alennuksen, kun taas alennus 2 antaa 4 dollarin alennuksen. Näin ollen voimme valita alennuksen 2. Kokonaisalennus on 14 $. Havainnollistamisen avuksi tässä on kaksi lisätaulukkoa, joissa näkyy voimassa oleva alennusprosentti kaikille mahdollisille kahden tuotteen yhdistelmille sekä alennukselle 1 että alennukselle 2. Vain puolet yhdistelmien luettelosta näytetään, koska näille kahdelle alennukselle ei ole merkitystä, missä järjestyksessä kaksi tuotetta alennetaan. Korkein tehokas alennus (25 prosenttia) on korostettu vihreällä ja pienin tehokas alennus (10 prosenttia) on korostettu punaisella. 

![Päällekkäisten alennusten yhdistelmä 04](./media/overlapping-discount-combo-04.jpg)

**Huomautus:** Kun hinnat vaihtelevat ja vähintään kaksi alennusta kilpailee, ainoa tapa varmistaa paras alennusten yhdistelmä on arvioida molemmat alennukset ja verrata niitä.

## <a name="total-possible-combinations"></a>Mahdollisia yhdistelmiä yhteensä
Tässä osassa jatketaan edellisen osan esimerkkiä. Lisäämme enemmän tuotteita ja vielä yhden alennuksen, jolloin näemme, kuinka monta yhdistelmää pitää laskea ja verrata. Seuraavassa taulukossa on esitetty mahdollisten alennusyhdistelmien määrä tuotteen määrän kasvaessa. Taulukosta näkyy, mitä tapahtuu, kun on kaksi päällekkäistä alennusta, kuten edellisessä esimerkissä, ja kun on kolme päällekkäistä alennusta. Mahdollisten arvioitavien alennusyhdistelmien määrä ylittää määrän, jota edes nopea tietokone ei voi laskea ja verrata riittävän nopeasti vähittäismyynnin tarpeisiin.

![Päällekkäisten alennusten yhdistelmä 05](./media/overlapping-discount-combo-05.jpg)

Kun käytetään vielä suurempia määriä tai useampia päällekkäisiä alennuksia, mahdollisten alennusyhdistelmien kokonaismäärä nousee nopeasti miljooniin, ja parhaan yhdistelmän valinta kestää jo huomattavan pitkään. Vähittäismyynnin hintamoduuliin on tehty joitain optimointeja, jotta voitaisiin vähentää arvioitavien yhdistelmien määrää. Koska tapahtuman päällekkäisten alennusten määriä ja tuotemääriä ei ole rajoitettu, paljon yhdistelmiä on arvioitava aina, kun on päällekkäisiä alennuksia. Raja-arvojen luokittelumenetelmä on yksi ratkaisu tähän ongelmaan.

## <a name="marginal-value-method"></a>Raja-arvomenetelmä
Eksponentiaalisesti kasvavan arvioitavien yhdistelmien määrän ongelman ratkaisemiseksi on olemassa optimointi, joka laskee arvon per jaettu tuote kullekin alennukselle, joka on kohdistettu tuotejoukkoon, johon voidaan käyttää kahta tai useampaa alennusta. Viittaamme tähän arvoon jaettujen tuotteiden alennuksen **raja-arvona**. Raja-arvo on tuotemäärän nostamisen keskimääräinen kokonaisalennussumman nousu, kun jaetut tuotteet kuuluvat kunkin alennuksen piiriin. Raja-arvo lasketaan ottamalla kokonaisalennussumma (DTotal), vähentämällä alennussumma ilman jaettuja tuotteita (DMinus\\ Shared) ja jakamalla kyseinen erotus jaettujen tuotteiden määrällä (ProductsShared). 
![Päällekkäisten alennusten yhdistelmä 06](./media/overlapping-discount-combo-06.jpg)

Kun jaetun tuotejoukon kunkin alennuksen raja-arvo on laskettu, alennukset käytetään jaettuihin tuotteisiin järjestyksessä, läpi kaikkien tapausten, korkeimmasta raja-arvosta pienimpään raja-arvoon. Tässä menetelmässä kaikkia jäljellä olevia alennusmahdollisuuksia ei verrata aina, kun yhtä alennuksen ilmentymää käytetään. Sen sijaan päällekkäisiä alennuksia verrataan yhden kerran ja käytetään sitten järjestyksessä. Muita vertailuja ei tehdä. Voit määrittää ylärajan, joka ylitettäessä siirrytään käyttämään raja-arvomenetelmää, **Alennus**-välilehdessä **Vähittäismyynnin parametrit** -sivulla. Hyväksyttävä aika kokonaisalennuksen laskentaan vaihtelee vähittäiskaupan toimialasta riippuen. Tämä aika on yleensä kuitenkin kymmenistä millisekunneista yhteen sekuntiin.




