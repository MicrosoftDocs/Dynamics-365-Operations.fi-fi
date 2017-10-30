---
title: Kiinteiden kompensaatiosuunnitelmien luominen
description: "Kiinteä kompensaatio viittaa työntekijän normaaliin bruttopalkkaan. Tässä artikkelissa esitellään komponentit, jotka on määritettävä ennen kiinteän kompensaatiosuunnitelman luomista ja työntekijöiden määrittämistä."
author: kherr75
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
ms.search.form: HRCCompGrid, HRCCompRefPointSetup, HRMCompEligibility, HRMCompEvent, HRMFixedCompPlanTable
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 15991
ms.assetid: ef8cf992-176c-4c98-9dff-6510e1eb9f1c
ms.search.region: Global
ms.author: kherr75
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Talent July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 399e1fee592c0ab31015e37e87d41c71f9282858
ms.contentlocale: fi-fi
ms.lasthandoff: 09/29/2017

---

# <a name="create-fixed-compensation-plans"></a>Kiinteiden kompensaatiosuunnitelmien luominen

[!include[banner](includes/banner.md)]


Kiinteä kompensaatio viittaa työntekijän normaaliin bruttopalkkaan. Tässä aiheessa esitellään komponentit, jotka on määritettävä ennen kiinteän kompensaatiosuunnitelman luomista ja työntekijöiden määrittämistä.

Kiinteät kompensaatiomäärät voidaan laskea työntekijöille, perustuen esimerkiksi suorituskykyyn, alueeseen ja budjetin korotuksiin. Microsoft Talent tukee vaihetta, luokkaa ja rivin kompensaatiotyyppejä.

## <a name="fixed-compensation-components"></a>Kiinteät kompensaatiokomponentit
### <a name="compensation-levels"></a>Kompensaatiotasot

Voit käyttää **kompensaatiotasoja** määrittääksesi kompensaation eri töille. Ne auttavat takaamaan, että työntekijöille maksetaan oikeudenmukaisesti korvausta.  **Kompensaatiotasot**-sivulla voit määrittää, kompensaatiotasot, joita tarvitaan kussakin vaiheessa, palkkaluokassa ja kompensaatioluokan suunnitelmassa. Käytä **"Ylös"** ja **"Alas"** -painikkeita asettaaksesi tasot oikeaan järjestykseen tyypin mukaan. Työn kompensaatiotasojen määrittäminen auttaa takaamaan, että kaikille kyseisessä työtehtävässä työskenteleville maksetaan saman tasoinen palkka.

### <a name="reference-points"></a>Viitepisteet

**Viitepisteet** ovat ruudukon sarakkeita, jotka määrittävät kompensaatioalueet kullekin tasolle. Kompensaatiotaso on ruudukon rivi. Palkkaluokan tyypin suunnitelman viitepisteet ovat yleensä minimi, keskitaso ja maksimi. Luo viitepisteet **Viitepisteiden määritykset** -sivulla.

### <a name="compensation-grids"></a>Kompensaatioruudukot

Tasojen ja viitepisteiden määrittämisen jälkeen ne voidaan yhdistää luomaan **kompensaatioruudukko**. **Kompensaatioruudukot** -sivulla, määritä ruudukon tiedot. Esimerkiksi, määritä mihin tehtävään ruudukko on tarkoitettu, minkä tyyppiseen suunnitelmaan sitä käytetään ja mitä viitepisteitä tai sarakkeita tarvitaan ruudukossa. Kun olet kirjoittanut tiedot, valitse **Kompensaatiorakenne** lisätäksesi tasoja ja summia ruudukkoon. 

**Vihje:** Käytä **Laajamittaiset muutokset** -toimintoa kompensaatiorakenteessa asettamaan alkuperäiset summat ja kasvata prosentit tai summat eri tasoilla tai viitepisteissä.

### <a name="pay-frequencies"></a>Maksutiheydet

**Maksutiheydet** määrittävät, kuinka työntekijän palkka tai palkkio määritetään (esimerkiksi 10 euroa tunnissa tai 50 000 vuodessa) ja tunti-, viikko-, kuukausi- (12 kuukauden) sekä vuosihinnat muutetaan. Esimerkiksi: Yritys, jolla on 38 tunnin työviikko tuntipalkalla työskenteleville työntekijöille, asettaa maksutiheyden, jonka tuntipalkka on 1, viikkopalkka on 38, kuukausipalkka on 164.6666666667 ja vuosipalkka on 1,976. Näitä muunnoksia käytetään laskettaessa eri palkat, jotka näkyvät työntekijän kiinteässä kompensaatiotietueessa.

## <a name="fixed-compensation-plans"></a>Kiinteät kompensaatiosuunnitelmat
Voit suunnitella kiinteän kompensaatiosuunnitelman yhdistääksesi kaikki komponentit, jotka olet määrittänyt. Luodaksesi kiinteän kompensaatiosuunnitelman, avaa **Kiinteät kompansaatiosuunnitelmat** -sivu. Tässä voit antaa nimen ja kuvauksen suunnitelmallesi, valita minkä tyyppinen suunnitelma se on (vaihe, luokka tai kompensaatioluokka), valita maksutiheyden, jota aiot käyttää työntekijän palkkatasolle (tuntikohtainen summa, vuosittainen summa ja niin edelleen) ja asettaa joitakin vaihtoehtoja, jotka ohjaavat miten kompensaatiota käsitellään. 

**Alueen ulkopuolinen toleranssi** -asetuksien avulla voit määrittää, miten tiukka haluat olla varmistaaksesi, että kompensaatiosummat ovat vähimmäis- ja enimmäissummien välillä. **Kova** hintatoleranssi edellyttää, että kompensaatio on määritetty tietyllä välillä kullakin tasolla. A **Pehmeä** hintatoleranssi hälyttää, jos korvauksen summa on alueen ulkopuolella, mutta voit jatkaa. Jos laitat toleranssin **"Ei yhtään"**, voit syöttää minkä vain korvaussumman työntekijälle saamatta virhe- tai varoitusviestejä. 

**Työhönottosääntö**-asetuksien avulla voit määrittää kaikkien työntekijöiden vastaanottavan saman lisäyksen riippumatta päivämäärästä, jolloin heidät palkattiin (**Työhönottosääntö**  =  **Ei yhtään**), tai saavatko työntekijät prosenttiosuuden palkasta, perustuen siihen kauanko he työskentelivät kauden aikana (**Työhönottosääntö**  =  **Prosentti**). 

**Aluekäyttömatriisi** on hyödyllinen, jos haluat joko pienentää aikaa, joka tarvitaan, jotta työntekijät saavuttavat alueensa keskipisteen tai suurentaa aikaa, joka tarvitaan, jotta työntekijät saavuttavat mahdollisimman suuren viitepisteen omalla alueellaan. Esimerkiksi: Haluat antaa niille työntekijöille, jotka ovat 25 prosentin alaosassa 110 prosenttia tavoitepalkkiostaan, mutta haluat antaa työntekijöille, jotka ovat ylimmäisessä 25 prosentissa vain 80 prosenttia heidän tavoitepalkkiostaan, estääksesi heitä saavuttamasta enimmäisarvoa liian pian. 

Kun olet määrittänyt perustiedot kiinteään kompensaatiosuunnitelmaan, voit määrittää suunnitelman kompensaatiorakenteen. Valitse **Määritä kompensaatio**. Valintaikkunan liukusäädin avautuu, joka antaa kolme vaihtoehtoa:

-   Luo uusi kompensaatioruudukko valitsemalla viitepistemääritys ja antamalla ruudukolle nimen.
-   Luo uusi kompensaatioruudukko kopioimalla olemassa oleva ruudukko, jota voit käyttää pohjana.
-   Käytä jo olemassa olevaa komensaatioruudukkoa, joka on jo määritetty. Kaikki kompensaatiosuunnitelmat, jotka käyttävät samaa ruudukkoa. saavat päivityksiä, jos ruudukkoa muutetaan.

Kun olet valinnut vaihtoehdon **Kompensaatiorakenne** -sivu avautuu ja voit tehdä muutoksia uuteen kompensaatioruudukkoon tai jo olemassa olevaan kompensaatioruudukkoon.

## <a name="fixed-compensation-enrollment"></a>Kiinteän kompensaation voimaanastuminen
### <a name="determine-who-is-eligible-for-the-plan"></a>Määritä, ketkä saavat käyttää suunnitelmaa

Työntekijöiden rekisteröiminen kiinteään kompensaatiosuunnitelmaan on ensimmäinen vaihe määritettäessä, kuka soveltuu suunnitelmassa määritettyyn kompensaatioon. Ennen kuin voidaan määrittää oikeutussääntöjä, suunnitelmaa ei voida määrittää kenellekään työntekijälle. Voit määrittää oikeutuksen avaamalla **Oikeutussäännöt**-sivun. Tässä voit luoda uuden oikeutussäännön kompensaatiosuunnitelmalle ja määrittää ehdot, jotka työntekijän on täytettävä, jotta hänellä olisi oikeutus suunnitelmaan. Voit rajoittaa sopivuutta koskien osastoa, ammattijärjestöä, kompensaatioaluetta (sijainti), työtä, työnkuvaa, työn tyyppiä tai kompensaatiotasoa. Vain ne työntekijät, jotka täyttävät oikeutussäännön kaikki ehdot, voidaan rekisteröidä kompensaatiosuunnitelmaan. 

**Huomaa:** Oikeutussääntöjä käytetään määrittelemään kelopisuus sekä kiinteisiin että muuttuviin kompensaatiosuunnitelmiin. 

Oikeutussääntö arvioi tiettyjen toimikenttien arvot kuten työ, virka ja työntekijätietueet, määrittääkseen onko työntekijä kompensaatiosuunnitelmaan oikeutettu.

-   **Työ**-sivulla oikeutussäännössä otetaan huomioon seuraavat kentät:
    -   **Työ**-kenttä
    -   **Töiden luokittelu** -välilehdessä **Toiminto-** ja **Työtyyppi-** kentät
    -   **Kompensaatio**-välilehdessä **Taso**-kenttä
-   **Toimet**-sivulla oikeutussäännössä otetaan huomioon **Osasto-** ja **Kompensaatioalue**-kentät.

Oikeutussäännössä otetaan huomioon myös ammattijärjestöt, jotka liittyvät työntekijään (**Työntekijät**-sivulla **Työntekijä**-välilehdessä, klikkaa **Henkilökohtaisia tietoja** &gt; **Ammattijärjestöt**).

### <a name="define-fixed-compensation-actions"></a>Määritä kiinteän kompensaation toiminnot

**Kiinteän kompensaation toimintoja** käytetään asetettaessa ja soveltaessa työntekijän kiinteän kompensaation asetuksia. Kiinteän kompensaation toiminnot avulla voit antaa kuvaavat nimet eri toiminnoille, joita korvaus- ja etujenhallinta voi suorittaa. Erilaisilla toimenpidetyypeillä on erityinen logiikka, niin, että niitä voidaan käyttää tiettyinä aikoina. 

Esimerkiksi, kun työntekijälle on määritetty kiinteä kompensaatio, vain toimintoja, joilla on **Palkkaa/Palkkaa uudelleen**-tyyppi, käytetään. Tässä tapauksessa voit halutessasi luoda kolme eri toimintaa **Palkkaa/Palkkaa uudelleen**-tyypille ja nimetä ne **Palkkaa**, **Palkkaa uudelleen** ja **Siirrä**. Sen jälkeen sinulla on kuvaavampi selitys sille, miksi työntekijä sai kiinteän kompensaation tai sitä muutettiin.

### <a name="enroll-the-employee"></a>Merkitse työntekijä

Voit nyt määrittää työntekijän kiinteään kompensaatiosuunnitelmaan. Avaa **Työntekijät**-sivu ja valitse työntekijä, joka määritetään kompensaatiosuunnitelmaan. Valitse toimintoruudussa **Kompensaatio** &gt; **Kiinteä suunnitelma**. Voit nyt luoda uuden kiinteän kompensaatiotoiminnon kyseiselle työntekijälle. 

**Huomautus:** Kompensaatiosuunnitelma-kentässä näkyvät vain ne suunnitelmat, joihin työntekijä on oikeutettu, niiden oikeutussääntöjen mukaisesti, jotka on määritetty jokaiselle suunnitelmalle. Jos oikeutussääntöä ei ole määritetty suunnitelmalle, kukaan työntekijä ei ole oikeutettu suunnitelmaan. 

Järjestelmä tarkistaa, että se kompensaatiosumma, joka on eritelty luokan tai tyypin kompensaatiosuunnitelmassa, on vähimmäis- ja enimmäisviitepisteiden väilllä, työntekijän työn annetulla kompensaatiotasolla. Jos korvaussumma on sallitun alueen ulkopuolella, varoitus tai virhesanoma tulee näkyviin, joka on määritetty kiinteän kompensaatiosuunnitelman toleranssitason mukaisesti.

<a name="see-also"></a>Lisätietoja
--------

[Kompensaatiosuunnitelmat](compensation-plans.md)




