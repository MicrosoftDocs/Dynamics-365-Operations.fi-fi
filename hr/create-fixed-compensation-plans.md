---
title: Kiinteiden kompensaatiosuunnitelmien luominen
description: "Kiinteä kompensaatio viittaa työntekijän normaaliin bruttopalkkaan. Tässä artikkelissa esitellään komponentit, jotka on määritettävä ennen kiinteän kompensaatiosuunnitelman luomista ja työntekijöiden määrittämistä."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: HRCCompGrid, HRCCompRefPointSetup, HRMCompEligibility, HRMCompEvent, HRMFixedCompPlanTable
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 15991
ms.assetid: ef8cf992-176c-4c98-9dff-6510e1eb9f1c
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9397e84f03ee5b340fa2aa0a64e582fc0078526e
ms.openlocfilehash: bbf08a9620dbc8ad928fe40a3ae5e9b2a2fcb373
ms.lasthandoff: 03/31/2017


---

# <a name="create-fixed-compensation-plans"></a>Kiinteiden kompensaatiosuunnitelmien luominen

Kiinteä kompensaatio viittaa työntekijän normaaliin bruttopalkkaan. Tässä aiheessa kuvataan osat, jotka on määritettävä ennen kuin voit luoda kiinteän kompensaatiosuunnitelmaan ja työntekijöiden rekisteröiminen.

Kiinteät kompensaatiomäärät voidaan laskea työntekijöille, perustuen esimerkiksi suorituskykyyn, alueeseen ja budjetin korotuksiin. Microsoft Dynamics-365 työvaiheiden tukee vaihe, palkkaluokka ja nauha palkkiot.

## <a name="fixed-compensation-components"></a>Kiinteät kompensaatiokomponentit
### <a name="compensation-levels"></a>Kompensaatiotasot

Voit käyttää **kompensaatiotasot** voit määrittää eri töitä, jotka auttavat takaamaan työntekijöille, jotka pidä näitä töitä maksetaan oikeudenmukaisesti korvausta. - **Kompensaatiotasot** -sivulla voit määrittää, joita tarvitaan kunkin vaiheen, palkkaluokka ja nauha suunnitelman kompensaatiotasot. Käytä **"Ylös"** ja **"Alas"** -painikkeita asettaaksesi tasot oikeaan järjestykseen tyypin mukaan. Työn kompensaatiotasojen määrittäminen auttaa takaamaan, että kaikille kyseisessä työtehtävässä työskenteleville maksetaan saman tasoinen palkka.

### <a name="reference-points"></a>Viitepisteet

**Viitepisteet** ovat ruudukon sarakkeita, jotka määrittävät kompensaatioalueet kullekin tasolle. Kompensaatiotaso on ruudukon rivi. Suunnitelman tyyppi a-luokan tyypillinen viitepisteet ovat vähintään ja enintään keskipiste. Voit luoda viitepisteitä **viitepisteiden** sivulla.

### <a name="compensation-grids"></a>Kompensaatioruudukot

Tasojen ja viitepisteiden määrittämisen jälkeen ne voidaan yhdistää luomaan **kompensaatioruudukko**. **Kompensaatioruudukot** -sivulla, määritä ruudukon tiedot. Esimerkiksi, määritä mihin tehtävään ruudukko on tarkoitettu, minkä tyyppiseen suunnitelmaan sitä käytetään ja mitä viitepisteitä tai sarakkeita tarvitaan ruudukossa. Kun olet kirjoittanut tiedot, valitse **Kompensaatiorakenne** lisätäksesi tasoja ja summia ruudukkoon. 

**Vihje:** Käytä **Laajamittaiset muutokset** -toimintoa kompensaatiorakenteessa asettamaan alkuperäiset summat ja kasvata prosentit tai summat eri tasoilla tai viitepisteissä.

### <a name="pay-frequencies"></a>Maksutiheydet

**Maksutiheydet** määrittävät, kuinka työntekijän palkka tai palkkio määritetään (esimerkiksi 10 euroa tunnissa tai 50 000 vuodessa) ja tunti-, viikko-, kuukausi- (12 kuukauden) sekä vuosihinnat muutetaan. Esimerkiksi: Yritys, jolla on 38 tunnin työviikko tuntipalkalla työskenteleville työntekijöille, asettaa maksutiheyden, jonka tuntipalkka on 1, viikkopalkka on 38, kuukausipalkka on 164.6666666667 ja vuosipalkka on 1,976. Näitä muunnoksia käytetään laskettaessa eri palkat, jotka näkyvät työntekijän kiinteässä kompensaatiotietueessa.

## <a name="fixed-compensation-plans"></a>Kiinteät kompensaatiosuunnitelmat
Voit suunnitella kiinteän kompensaatiosuunnitelman yhdistääksesi kaikki komponentit, jotka olet määrittänyt. Luodaksesi kiinteän kompensaatiosuunnitelman, avaa **Kiinteät kompansaatiosuunnitelmat** -sivu. Tässä voit antaa nimen ja kuvauksen suunnitelmallesi, valita minkä tyyppinen suunnitelma se on (vaihe, luokka tai kompensaatioluokka), valita maksutiheyden, jota aiot käyttää työntekijän palkkatasolle (tuntikohtainen summa, vuosittainen summa ja niin edelleen) ja asettaa joitakin vaihtoehtoja, jotka ohjaavat miten kompensaatiota käsitellään. 

**Alueen ulkopuolinen toleranssi** -asetuksien avulla voit määrittää, miten tiukka haluat olla varmistaaksesi, että kompensaatiosummat ovat vähimmäis- ja enimmäissummien välillä. **Kova** hintatoleranssi edellyttää, että kompensaatio on määritetty tietyllä välillä kullakin tasolla. A **Pehmeä** hintatoleranssi hälyttää, jos korvauksen summa on alueen ulkopuolella, mutta voit jatkaa. Jos laitat toleranssin **"Ei yhtään"**, voit syöttää minkä vain korvaussumman työntekijälle saamatta virhe- tai varoitusviestejä. 

**Työhönottosäännön** asetusten avulla voit määrittää, onko kaikkien työntekijöiden olisi saatava sama kasvua, päivä, jona ne palkattiin riippumatta (**työhönottosäännön** = **ei mitään**), tai onko työntekijät saavat prosentteina, kuinka kauan he olivat työssä jakson aikana perustuvaan palkkioon (**työhönottosäännön** = **%**). 

**Aluekäyttömatriisi** on hyödyllinen, jos haluat joko pienentää aikaa, joka tarvitaan, jotta työntekijät saavuttavat alueensa keskipisteen tai suurentaa aikaa, joka tarvitaan, jotta työntekijät saavuttavat mahdollisimman suuren viitepisteen omalla alueellaan. Esimerkiksi: Haluat antaa niille työntekijöille, jotka ovat 25 prosentin alaosassa 110 prosenttia tavoitepalkkiostaan, mutta haluat antaa työntekijöille, jotka ovat ylimmäisessä 25 prosentissa vain 80 prosenttia heidän tavoitepalkkiostaan, estääksesi heitä saavuttamasta enimmäisarvoa liian pian. 

Kun olet määrittänyt perustiedot kiinteään kompensaatiosuunnitelmaan, voit määrittää suunnitelman kompensaatiorakenteen. Valitse **kompensaation määrittäminen**. Valintaikkunan liukusäädin avautuu, joka antaa kolme vaihtoehtoa:

-   Luo uusi kompensaatioruudukko valitsemalla viitepistemääritys ja antamalla ruudukolle nimen.
-   Luo uusi kompensaatioruudukko kopioimalla olemassa oleva ruudukko, jota voit käyttää pohjana.
-   Käytä jo olemassa olevaa komensaatioruudukkoa, joka on jo määritetty. Kaikki kompensaatiosuunnitelmat, jotka käyttävät samaa ruudukkoa. saavat päivityksiä, jos ruudukkoa muutetaan.

Kun olet valinnut vaihtoehdon **Kompensaatiorakenne** -sivu avautuu ja voit tehdä muutoksia uuteen kompensaatioruudukkoon tai jo olemassa olevaan kompensaatioruudukkoon.

## <a name="fixed-compensation-enrollment"></a>Kiinteän kompensaation voimaanastuminen
### <a name="determine-who-is-eligible-for-the-plan"></a>Määritä, ketkä saavat käyttää suunnitelmaa

Työntekijöiden rekisteröiminen kiinteään kompensaatiosuunnitelmaan on ensimmäinen vaihe määritettäessä, kuka soveltuu suunnitelmassa määritettyyn kompensaatioon. Ennen kuin voidaan määrittää oikeutussääntöjä, suunnitelmaa ei voida määrittää kenellekään työntekijälle. Voit määrittää kelpoisuus, Avaa **oikeutussääntöjä** sivun. Tässä voit luoda uuden kelpoisuus sääntö että kompensaatiosuunnitelmalle ja määrittää ehdot, jotka työntekijän on täytettävä, jotta annettaisiin suunnitelma. Voit rajoittaa sopivuutta koskien osastoa, ammattijärjestöä, kompensaatioaluetta (sijainti), työtä, työnkuvaa, työn tyyppiä tai kompensaatiotasoa. Vain ne työntekijät, jotka täyttävät oikeutussäännön kaikki ehdot, voidaan rekisteröidä kompensaatiosuunnitelmaan. 

**Huomaa:** Oikeutussääntöjä käytetään määrittelemään kelopisuus sekä kiinteisiin että muuttuviin kompensaatiosuunnitelmiin. 

Oikeutussääntö arvioi tiettyjen toimikenttien arvot kuten työ, virka ja työntekijätietueet, määrittääkseen onko työntekijä kompensaatiosuunnitelmaan oikeutettu.

-   **Työ**-sivulla oikeutussäännössä otetaan huomioon seuraavat kentät:
    -   **Työ**-kenttä
    -   **Töiden luokittelu** -välilehdessä **Toiminto-** ja **Työtyyppi-**kentät
    -   **Kompensaatio**-välilehdessä **Taso**-kenttä
-   **Toimet**-sivulla oikeutussäännössä otetaan huomioon **Osasto-** ja **Kompensaatioalue**-kentät.

Oikeutussäännön katsoo myös ammattijärjestöt, jotka liittyvät työntekijän (- **työntekijöiden** -sivulla **työntekijän** -välilehdessä **henkilökohtaisia tietoja**&gt;**ammattijärjestöt**).

### <a name="define-fixed-compensation-actions"></a>Määritä kiinteän kompensaation toiminnot

**Kiinteän kompensaation toimintoja** käytetään asetettaessa ja soveltaessa työntekijän kiinteän kompensaation asetuksia. Kiinteän kompensaation toiminnot avulla voit antaa kuvaavat nimet eri toiminnoille, joita korvaus- ja etujenhallinta voi suorittaa. Erilaisilla toimenpidetyypeillä on erityinen logiikka, niin, että niitä voidaan käyttää tiettyinä aikoina. 

Esimerkiksi, kun työntekijälle on määritetty kiinteä kompensaatio, vain toimintoja, joilla on **Palkkaa/Palkkaa uudelleen**-tyyppi, käytetään. Tässä tapauksessa voit halutessasi luoda kolme eri toimintaa **Palkkaa/Palkkaa uudelleen**-tyypille ja nimetä ne **Palkkaa**, **Palkkaa uudelleen** ja **Siirrä**. Sen jälkeen sinulla on kuvaavampi selitys sille, miksi työntekijä sai kiinteän kompensaation tai sitä muutettiin.

### <a name="enroll-the-employee"></a>Merkitse työntekijä

Voit nyt määrittää työntekijän kiinteään kompensaatiosuunnitelmaan. Avaa **Työntekijät**-sivu ja valitse työntekijä, joka määritetään kompensaatiosuunnitelmaan. Valitse toimintoruudussa **korvaus**&gt;**kiinteä suunnitelma**. Voit nyt luoda uusia kiinteän Kompensaatiotoiminnon työntekijän. 

**Huomautus:** Kompensaatiosuunnitelma-kentässä näkyvät vain ne suunnitelmat, joihin työntekijä on oikeutettu, niiden oikeutussääntöjen mukaisesti, jotka on määritetty jokaiselle suunnitelmalle. Jos oikeutussääntöä ei ole määritetty suunnitelmalle, kukaan työntekijä ei ole oikeutettu suunnitelmaan. 

Järjestelmä tarkistaa, että se kompensaatiosumma, joka on eritelty luokan tai tyypin kompensaatiosuunnitelmassa, on vähimmäis- ja enimmäisviitepisteiden väilllä, työntekijän työn annetulla kompensaatiotasolla. Jos korvaussumma on sallitun alueen ulkopuolella, varoitus tai virhesanoma tulee näkyviin, joka on määritetty kiinteän kompensaatiosuunnitelman toleranssitason mukaisesti.

<a name="see-also"></a>Lisätietoja
--------

[Kompensaatiosuunnitelmat](compensation-plans.md)


