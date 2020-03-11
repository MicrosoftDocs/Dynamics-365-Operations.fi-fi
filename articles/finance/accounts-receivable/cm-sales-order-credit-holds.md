---
title: Myyntitilausten luottorajapidot
description: ''
author: mikefalkner
manager: AnnBe
ms.date: 01/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mfalkner
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 316a626e6a18f0afda632111138482f62f6809db
ms.sourcegitcommit: 12b9d6f2dd24e52e46487748c848864909af6967
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/14/2020
ms.locfileid: "3057667"
---
# <a name="credit-holds-for-sales-orders"></a>Myyntitilausten luottorajapidot
[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]


Tässä ohjeaiheessa käsitellään niiden sääntöjen määrittämistä, joilla myyntitilaus asetetaan luottorajapitoon. Luotonhallinnan estosäännöt voidaan ottaa käyttöön yhden asiakkaan tai asiakasryhmän osalta.  Estosäännöt määrittävät, mihin seuraaviin tilanteisiin vastataan.

1. Erääntyneiden päivien lukumäärä
2. Tilien tila
3. Maksuehdot
4. Luottoraja vanhentunut
5. Erääntynyt summa
6. Myyntitilauksen summa
7. Käytettävissä olevan luoton käytetty osa

Lisäksi on käytössä on kaksi parametria, joilla hallitaan myyntitilauksen estäviä lisäskenaarioita.

1. Maksuehtojen muutos
2. Tilitysalennuksen muutos

## <a name="set-up-blocking-rules-and-exclusion-rules"></a>Esto- ja poikkeussääntöjen määrittäminen

Kun asiakas aloittaa myyntitapahtuman, myyntitilauksen tietoja verrataan estosääntöjoukkoon, jonka avulla päätetään, myönnetäänkö asiakkaalle luottoa vai ei, ja joka sallii myynnin siirtymisen eteenpäin. Voit määrittää myös poikkeuksia, jotka ohittavat estosäännöt ja sallivat myyntitilauksen käsittelyn. Esto- ja poikkeussäännöt määritetään valitsemalla **Luotonhallinta > Asetukset > Luotonhallinnan asetukset > Estosäännöt**-sivu.

### <a name="days-overdue"></a>Erääntymispäivät

Avaa **Erääntymispäivät**-välilehti, jos estosääntö otetaan käyttöön asiakkaalla, jolla vähintään yksi lasku on erääntynyt tiettyjen päivien ajan.
1. Valitse asiakkaat, joiden osalta tämän sääntö on **Kirjaustapa**.
   - Valitse **Taulu**, jos sääntö koskee tiettyä asiakasta.
   - Valitse **Ryhmä**, jos sääntö otetaan käyttöön asiakasryhmätasolla. 
   - Valitse **Kaikki**, jos sääntö koskee kaikkia asiakkaita.
2. Alueen määrittämiseen jälkeen on määritettävä alueella käytettävä **Tili/ryhmä**.
   - Jos alueena on **Taulu**, valittavana on asiakasluettelo. 
   - Valitse **Ryhmä**, jos sääntö otetaan käyttöön asiakasluottoryhmässä.
   - Valitse **Kaikki**, jos sääntö koskee kaikkia asiakkaita. 
3. Valitsemalla **Riskiryhmä** voit ottaa käyttöön ehdot luotonhallinnan pidosta niiden asiakkaiden osalta, jotka on ryhmitelty yhteisten seikkojen perusteella, kuten Dun and Bradstreet -luokituksen, toimintavuosien määrän ja asiakkuuden pituuden mukaan.  
4. Valitse määritettävän säännön tyyppi. **Esto**-asetuksella luodaan tilauksen estävä sääntö. **Poikkeus**-asetuksella luodaan sääntö, joka ohittaa toisen säännön tilauksen estossa. 
5. Valitse **Arvotyyppi**. Oletusarvo on kiinteä päivien lukumäärä. Jos olet luomassa poikkeusta, voit määrittää sen sijaan kiinteä päivien lukumäärän tai summan. 
6. Anna **Erääntyneet**-arvoksi päivien lukumäärä, joka sallitaan valitussa estosäännössä, ennen kuin tilaus asetetaan luotonhallinnan pitoon arviointia varten. Erääntyneiden päivien lukumäärä ilmaisee päivinä ylimääräisen eräpäivän jälkeisen maksuajan, joka lisätään maksun eräpäivään ja joka aika laskulla on, ennen kuin sen katsotaan erääntyneen. Jos **Arvotyyppi** on määritetty poikkeuksessa summana, anna summa ja summan valuutta.

### <a name="accounts-status"></a>Tilien tila

Avaa **Tilien tila** -välilehti, jos estosääntöä koskee asiakasta, jolla on valittu tilin tila.
1. Valitse määritettävän säännön tyyppi.  **Esto** luo tilauksen estävän säännön. **Poikkeus** luo säännön, joka ohittaa säännön tilauksen estossa. 
2. Valitse **Tilin tila**, jonka vuoksi sääntö asettaa myyntitilauksen pitoon ja ohittaa sen.

### <a name="terms-of-payment"></a>Maksuehdot

Valitse **Maksuehdot**, jos estosääntö koskee valittua maksuehtoa.
1. Valitse määritettävän säännön tyyppi.  **Esto** luo tilauksen estävän säännön. **Poikkeus** luo säännön, joka ohittaa säännön tilauksen estossa. 
2. Valitse **Maksuehdot**, jonka vuoksi sääntö asettaa myyntitilauksen pitoon ja ohittaa sen.

### <a name="credit-limit-expired"></a>Luottoraja vanhentunut

Avaa **Luottoraja vanhentunut** -välilehti, jos estosääntö koskee asiakkaita, joiden luottorajat ovat vanhentuneet.
1. Valitse asiakkaat, joiden osalta tämän sääntö on **Kirjaustapa**.
   - Valitse **Taulu**, jos sääntö koskee tiettyä asiakasta.
   - Valitse **Ryhmä**, jos sääntö otetaan käyttöön asiakasryhmätasolla. 
   - Valitse **Kaikki**, jos sääntö koskee kaikkia asiakkaita.
2. Alueen määrittämiseen jälkeen on määritettävä alueella käytettävä **Tili/ryhmä**.
   - Jos alueena on **Taulu**, valinta tehdään asiakasluettelosta. 
   - Valitse **Ryhmä**, jos sääntö otetaan käyttöön asiakkaan luotonhallintaryhmässä.
   - Valitse **Kaikki**, jos sääntö koskee kaikkia asiakkaita. 
3. Valitse **Riskiryhmä**, jos haluat rajoittaa entisestään luetteloa asiakkaista, jotka asetetaan luotonhallinnan pitoon. 
4. Valitse määritettävän säännön tyyppi. 
  - Luo tilauksen estävän sääntö valitsemalla **Esto**. 
  - Valitsemalla **Poikkeus** luodaan sääntö, joka ohittaa toisen säännön tilauksen estossa. 
6. Anna valitun estosäännön **Luottoraja vanhentunut päiviä** -arvo, jonka jälkeen tilaus asetetaan luotonhallinnan pitoon. Erääntyneiden päivien lukumäärä ilmaisee päivinä ylimääräisen eräpäivän jälkeisen maksuajan, joka lisätään päivinä luottorajan vanhentumiseen.

### <a name="overdue-amount"></a>Erääntynyt summa

Avaa **Erääntynyt summa** -välilehti, jos estosääntö koskee asiakkaita, joilla on erääntyneitä summia.
1. Valitse asiakkaat, joiden osalta tämän sääntö on **Kirjaustapa**.
   - Valitse **Taulu**, jos sääntö koskee tiettyä asiakasta.
   - Valitse **Ryhmä**, jos sääntö otetaan käyttöön asiakasryhmätasolla. 
   - Valitse **Kaikki**, jos sääntö koskee kaikkia asiakkaita.
2. Alueen määrittämiseen jälkeen on määritettävä alueella käytettävä **Tili/ryhmä**.
   - Jos alueena on **Taulu**, valittavana on asiakashaku. 
   - Valitse **Ryhmä**, jos sääntö otetaan käyttöön asiakkaan luotonhallintaryhmässä.
   - Valitse **Kaikki**, jos sääntö koskee kaikkia asiakkaita. 
3. Valitse **Riskiryhmä**, jos haluat rajoittaa entisestään luetteloa asiakkaista, jotka asetetaan luotonhallinnan pitoon. 
4. Valitse määritettävän säännön tyyppi. 
  - Luo tilauksen estävän sääntö valitsemalla **Esto**. 
  - Valitsemalla **Poikkeus** luodaan sääntö, joka ohittaa toisen säännön tilauksen estossa. 
5. Anna valitun estosäännön **Erääntynyt summa** -arvo, jonka jälkeen tilaus asetetaan luotonhallinnan pitoon arviointia varten. 
6. Valitse **Arvotyyppi**, jonka määrittämää arvon tyyppiä käytetään myös testaamaan sitä, kuinka paljon luottorajasta on käytetty. Prosenttiosuus on oltava estosäännöissä, mutta poisjätössä voi olla kiinteä summa tai prosenttiosuus
. Raja liittyy luottorajaan.
7. Anna valitun säännön **Luottorajan raja-arvo**, jonka jälkeen asiakas asetetaan luotonhallinnan pitoon. Arvo voi olla summa tai prosenttiosuus sen mukaan, mikä arvotyyppi on valittu.
8. Sääntö tarkistaa, että **Erääntynyt summa** ja **Luottorajan raja-arvo** on ylitetty. 

### <a name="sales-order"></a>Myyntitilaus 

Valitse **Myyntitilaus**, jos estosääntö koskee myyntitilauksen arvoa.
1. Valitse asiakkaat, joiden osalta tämän sääntö on **Kirjaustapa**.
   - Valitse **Taulu**, jos sääntö koskee tiettyä asiakasta.
   - Valitse **Ryhmä**, jos sääntö otetaan käyttöön asiakasryhmätasolla. 
   - Valitse **Kaikki**, jos sääntö koskee kaikkia asiakkaita.
2. Alueen määrittämiseen jälkeen on määritettävä alueella käytettävä **Tili/ryhmä**.
   - Jos alueena on **Taulu**, valittavana on asiakashaku. 
   - Valitse **Ryhmä**, jos sääntö otetaan käyttöön asiakkaan luotonhallintaryhmässä.
   - Valitse **Kaikki**, jos sääntö koskee kaikkia asiakkaita. 
3. Valitse **Riskiryhmä**, jos haluat rajoittaa entisestään luetteloa asiakkaista, jotka asetetaan luotonhallinnan pitoon. 
4. Valitse määritettävän säännön tyyppi.  
  - Luo tilauksen estävän sääntö valitsemalla **Esto**. 
  - Valitsemalla **Poikkeus** luodaan sääntö, joka ohittaa toisen säännön tilauksen estossa. 
6. Anna valitun estosäännön **Myyntitilauksen summa** -arvo, jonka jälkeen tilaus asetetaan luotonhallinnan pitoon. 

Myyntitilaussääntö sisältää kaikki muut säännöt ohittavan lisäasetuksen. Voit luoda poikkeuksen, joka vapauttaa myyntitilauksen ottamatta huomioon mitään muita sääntöjä, valitsemalla **Vapauta myyntitilaus** -valintaruudun poikkeusrivillä.

### <a name="credit-limit-used"></a>Käytetty luottoraja

Valitse **Käytetty luottoraja**, jos estosääntö koskee asiakkaan käytettyä luottorajan summaa.
1. Valitse asiakkaat, joiden osalta tämän sääntö on **Kirjaustapa**.
   - Valitse **Taulu**, jos sääntö koskee tiettyä asiakasta.
   - Valitse **Ryhmä**, jos sääntö otetaan käyttöön asiakasryhmätasolla. 
   - Valitse **Kaikki**, jos sääntö koskee kaikkia asiakkaita.
2. Alueen määrittämiseen jälkeen on määritettävä alueella käytettävä **Tili/ryhmä**.
   - Jos alueena on **Taulu**, valittavana on asiakashaku. 
   - Valitse **Ryhmä**, jos sääntö otetaan käyttöön asiakkaan luotonhallintaryhmässä.
   - Valitse **Kaikki**, jos sääntö koskee kaikkia asiakkaita. 
3. Valitse **Riskiryhmä**, jos haluat rajoittaa entisestään luetteloa asiakkaista, jotka asetetaan luotonhallinnan pitoon. 
4. Valitse määritettävän säännön tyyppi.
   - Luo tilauksen estävän sääntö valitsemalla **Esto**. 
   - Valitsemalla **Poikkeus** luodaan sääntö, joka ohittaa toisen säännön tilauksen estossa. 
5. Valitse **Jäljellä oleva raja**, joka määrittää myyntitilauksen estävän luottorajan prosenttiosuuden. Jos tilauksen arvo nostaa käytetyn luottorajan summan prosenttiosuuden yläpuolelle, tilaus asetetaan pitoon. 

## <a name="put-a-sales-order-on-hold-based-on-other-criteria"></a>Myyntitilauksen asettaminen pitoon muiden ehtojen perusteella
  
### <a name="rank-payment-terms"></a>Maksuehtojen sijoitukset  

Voit pakottaa luottovalvontasäännöt suoritettavaksi, kun maksuehtoja muutetaan. Maksuehdot on asetettava keskinäiseen järjestykseen ja niille on määritettävä sijoitusarvo. Jos muutat tilauksen maksuehtoja siten, että uusien maksuehtojen sijoitus on korkeampi kuin vanhojen maksuehtojen sijoitus, tilaus lähetetään luotonhallintaan hyväksyttäväksi.

Voit määrittää maksuehtojen sijoituksen valitsemalla **Luotonhallinta > Asetukset > Luotonhallinnan asetukset > Maksuehtojen sijoitus** -sivun.

1. Valitse sijoitettavaksi maksuehdon **Maksuehdot**-kenttä. Kun valitset ehdon, kuvaus näkyy **Kuvaus**-kentässä.
2. Valitse ehdon sijoitus **Sijoitus**-kentässä. Arvot ovat suhteessa toisiinsa, joten voit käyttää arvoja 1,2,3 tai 10,20,30. Voit myös käyttää samaa arvoa useimmissa maksuehdoissa, jotta enintään pari maksuehtoa käynnistää luottotarkistuksen.

### <a name="rank-settlement-discounts"></a>Tilitysalennusten sijoitukset   

Voit pakottaa luottovalvontasäännöt suoritettavaksi, kun tilitysalennuksia muutetaan. Tilitysalennukset on asetettava keskinäiseen järjestykseen ja niille on määritettävä sijoitusarvo. Jos muutat tilauksen tilitysalennuksia siten, että uusien tilitysalennusten sijoitus on korkeampi kuin vanhojen tilitysalennusten sijoitus, tilaus lähetetään luotonhallintaan hyväksyttäväksi.

Voit määrittää maksuehtojen sijoituksen valitsemalla **Luotonhallinta > Asetukset > Luotonhallinnan asetukset > Tilitysalennusten sijoitus** -sivun.

1. Valitse sijoitettava **Käteisalennus**. Tilityksen **Kuvaus**-kenttä avautuu.
2. Valitse **Sijoitus**-arvo. Arvot ovat suhteessa toisiinsa, joten voit käyttää arvoja 1,2,3 tai 10,20,30. Voit myös käyttää samaa arvoa useimmissa tilitysalennuksissa, jotta enintään pari tilitysalennusta käynnistää luottotarkistuksen.

## <a name="sequence-the-application-of-rules"></a>Sääntöjen käyttöjärjestys

Säännöt suoritetaan tietyssä järjestyksessä, jota voi muuttaa organisaation tarpeiden mukaan. 

- Yhdessä tapauksessa myyntitilauksen poikkeussäännöillä voi ohittaa kaikki myyntitilauksen mahdollisesti estävät säännöt. Luo myyntitilauksen poikkeussääntö ja merkitse **Vapauta myyntitilaus** -vaihtoehto. Tilausta ei aseteta pitoon, jos kyseisen poikkeussäännön arvo on tosi, eikä mitään muuta sääntöä tarkisteta.
- Estosäännöt voivat asettaa tilauksen pitoon.
- Poikkeussäännöt suoritetaan estosääntöjen jälkeen. Poikkeussäännöt koskevat vain sääntöä, jonka perusteella ne on määritetty. 
- Esto- ja poikkeussäännöt suoritetaan järjestyksessä Taulu, Ryhmä ja Kaikki. Tämän käsittelyjärjestyksen vuoksi on mahdollista, että Kaikki-tasolla on estosääntö, jota ei suoriteta, koska Taulu- tai Ryhmä-tason poikkeussääntö suoritetaan.
- Poikkeukset eivät ohita estosääntöä, jos ne ovat samalla tasolla. Esimerkiksi ryhmätason poikkeussääntö ei ohita ryhmätason estosääntöä. Poikkeuksia ei tarvitse määrittää Kaikki-tasolla lukuun ottamatta edellä mainittua yhtä myyntitilauksen poikkeussäännön tapausta. 

**Käytetty luottoraja** -säännön toiminta muuttaa **Tarkista myyntitilauksen luottoraja** -parametrin asetusten perusteella. Tämä parametri on luotonvalvonnan parametrilomakkeessa.
- Jos parametrin arvoksi on määritetty Ei, Käytetty luottoraja -sääntöä ei suoriteta.
- Jos parametrin arvoksi on määritetty Kyllä ja **Sanoma luottorajan ylittyessä** -asetukseksi on määritetty varotus, luottorajan ylittymisestä annetaan varoitus. **Käytetty luottoraja** -säännön suorittamisella voidaan tarkistaa, onko olemassa sääntöjä, jotka pitäisi suorittaa. Tässä skenaariossa ei kuitenkaan yleensä lisätä sääntöjä.
- Jos parametrin arvoksi on määritetty Kyllä ja **Sanoma luottorajan ylittyessä** -asetuksen arvoksi on määritetty virhe, luottoraja tarkistetaan ja tilaus asetetaan pitoon, jos luottoraja ylittyy. Lisäksi **Käytetty luottoraja** -säännön suorittamisella tarkistetaan, onko olemassa suoritettavia lisäsääntöjä. Vaikka virhesanomaa ei näytetä, näkyviin tulee **Luottoraja ylitetty** eston syynä. 

## <a name="settings-that-will-change-the-way-an-order-is-placed-on-hold"></a>Tilauksen pitoon asettamistavan muuttavat asetukset

Tilaukset voidaan ohittaa luotonhallinnassa, vaikka sääntöjä olisi otettu käyttöön. 

- Jos muutat **Kaikki asiakkaat > valitse asiakas > Luotonhallinta-pikavälilehden** **Ohita asiakas luotonhallinnassa** -asetukseksi **Kyllä**, mitään kyseisen asiakkaan tilauksia ei käsitellä.
- Jos muutat **Ohita luotonhallinnassa** -arvoksi **Kyllä** **Luotonhallinta-pikavälilehden** **myyntitilausten otsikossa**, luotonhallinnan sääntöjä ei käsitellä. Vain luottovirkailija ja luottopäällikkö voi muuttaa tämän asetuksen.

## <a name="processing-orders-on-hold-using-the-credit-management-hold-list"></a>Pidossa olevien tilausten käsittely luotonhallinnan pitoluettelon avulla

Luotonhallinnan pitoluettelon avulla luottopäälliköt voivat tarkastella kaikki pitoon asetettuja myyntitilauksia sekä poistaa pidot, kun luotto-ongelmat on käsitelty. **Luotonhallinnan pitoluettelo** -sivulla on näkyvissä kaikki pitoon asetetut myyntitilaukset. Voit tarkastella pitoluetteloa **Kaikki luottorajapidot** -sivulla (**Luotonhallinta > Luotonhallinnan pitoluettelo > Kaikki luottorajapidot**).
Kaikkien yritysten myyntitilaukset lähetetään samaan luotonhallinnan pitoluetteloon, joten käytettävissä on keskitetty näkymä kaikista toimenpiteitä odottavista tapahtumista. Käyttäjät näkevät vain niiden yritysten tiedot, joiden käyttöoikeus heillä on.

Myyntitilaus voidaan asettaa pitoluetteloon seuraavista syistä:
1. Asiakkaalla on lasku, joka on erääntynyt määritetyn määrän päiviä. 
2. Tilauksessa on tietty tilin tila.
3. Tilauksessa on tietyt maksuehdot.
4. Asiakkaalla on vanhentunut luottoraja.
5. Asiakkaalla on erääntynyt summa ja on käyttänyt määritetyn prosenttiosuuden luottorajasta.
6. Myyntitilaus ylittää tietyn summan.
7. Asiakas on ylittänyt tietyn prosenttiosuuden luottorajasta.
8. Maksuehdot poikkeavat asiakkaan oletusmaksuehdoista.
9. Tilitysalennukset poikkeavat asiakkaan oletustilitysalennuksesta.

Kunkin myyntitilauksen eston syy näkyy pitoluettelossa. Jos pidolla on useita syitä, syynä näkyy **Useita**. Voit tarkastella toimintoruudun **Eston syyt** -valikon avulla kaikkia syitä, joiden vuoksi myyntitilaus on asetettu pitoon. **Eston syyt** ovat näkyvissä myös tietoruutuna.

### <a name="releasing-orders-from-the-hold-list-for-processing"></a>Tilausten vapauttaminen pitoluettelosta käsiteltäväksi

Kun olet tutustunut pidon syihin ja selvittänyt ne, voit vapauttaa myyntitilaukset lisäkäsittelyyn.

1) Valitse rivi pitoluettelossa. Voit vapauttaa useita tilauksia valitsemalla useita rivejä.
2) Valitse vapautettavaksi valitulle tilaukselle **Vapautuksen syy**.  
3) Anna kullekin vapautettavaksi valitulle tilaukselle **Tarkistuspäivä**.  
4) Vapauta tilaus valitsemalla toimintoruudussa **Vapauta**-valikko. Tämä valikko on käytettävissä vasta, kun tapahtumat on valittu. Käyttäjällä on kaksi vaihtoehtoa:
 - Valitse **Kirjataan**, jos haluat poistaa pidon ja kirjat asiakirjan samalla kirjausprosessilla, jota käytettiin, kun asiakirja asetettiin pitoon. Jos esimerkiksi myyntitilauksen vahvistus asetettiin pitoon, myyntitilauksen vahvistus valmistuisi vapautuksen jälkeen. Myyntitilauksen kirjauslomake avautuu, ja käyttäjä voi kirjata vahvistuksen.
 - Valitse **Kirjaamatta**, jos haluat poistaa pidon tekemättä ilman muita toimenpiteitä. Myyntitilaus voidaan kirjata manuaalisesti.

### <a name="rejecting-orders-in-the-hold-list"></a>Pitoluettelossa olevien tilausten hylkääminen
Voit hylätä myyntitilauksen käyttämällä toimintoruudun **Hylkää**-valikkoa.
1. Valitse rivi pitoluettelossa. Voit vapauttaa useita tilauksia valitsemalla useita rivejä.
2. Tilaus poistetaan pitoluettelosta ja myyntitilauksen otsikko päivitetään näyttämään tilauksen hylkääminen.

### <a name="automatically-releasing-credit-management-holds"></a>Luotonhallinnan pitojen automaattinen vapauttaminen
Myyntitilaukset sijoitetaan pitoluetteloon estosääntöjen perusteella. Jotkin pitojen syyt voivat muuttua ajan kuluessa, jos myyntitilaus on pitoluettelossa tietyn aikaa. Asiakas voi esimerkiksi maksaa laskunsa, jolloin luottoraja alittuu. 

Voit arvioida pitoluettelon myyntitilauksia **Arviointi vapautusta varten** -valikossa ja vapauttaa ne automaattisesti, jos pidon syy ei ole enää aiheellinen.
1.  Valitse **Arviointi vapautusta varten** -valikko.
2.  Voit tarkastella kaikkia myyntitilauksia valitsemalla **Käsittele estosäännöt**. Voit tarkastella vain valittuja rivejä valitsemalla **Käsittele valittujen rivien estosäännöt**.
3. Voit valita vain yhden asiakkaan esiin tulevalle liukusäätimellä. Jos haluat kaikki asiakkaat, jätä avattava asiakasvalikko tyhjäksi. 
4. Kun valitset OK, prosessi suoritetaan taustalla ja voit jatkaa muiden tehtävien parissa. Jos valitset eräkäsittelyn ennen Ok-painikkeen napsauttamista, prosessi suoritetaan eränä, kun valitse Ok. Luettelon pidossa olevien tilausten käsittely voi kestään jonkin aikaa, joten päivitä tilausten tila valitsemalla Päivitä. 
5.  Jos eston syy ei koske enää tilausta, eston syy ei ole enää asianmukainen eikä syyn vieressä ole enää valintamerkkiä, kun eston syitä tarkastellaan.
6.  Jos kaikki eston syyt on poistettu, eston syyluetteloon lisätään uusi syy, **Valmis vapautettavaksi**. Myyntitilaus voidaan vapauttaa automaattisesti.
7.  Jos **Automaattinen vapautus** -parametrin arvo **Luotonvalvonta > Asetukset > Luotonvalvonnan parametrit > Luotto > Automaattinen vapautus** -välilehdessä on **Kirjataan**, sinua pyydetään tekemään kirjaus käyttämällä estetyn asiakirjan kirjauslomaketta.
8.  Jos **Automaattinen vapautus** -parametrin arvo **Luotonvalvonta > Asetukset > Luotonvalvonnan parametrit > Luotto > Automaattinen vapautus** -välilehdessä on **Kirjaamatta**, tilauksen kirjaus on tehtävä manuaalisesti.

### <a name="credit-management-approval-workflow"></a>Luotonhallinnan hyväksynnän työnkulku

Voit hallita luottorajapitojen vapauttamista myös luomalla **luotonhallinnan työnkulkuja**. Kun työnkulku on määritetty **Luotonhallinta > Asetukset > Luotonhallinnan työnkulut** -sivulla, vapautettavaksi tai hylättäväksi merkityt tilaukset lähetetään työnkulkuun, jossa ne on hyväksyttävä, ennen kuin ne voidaan vapauttaa tai hylätä. 

Jos tehtävät sisällytetään työnkulkuun, kun vapauttaessa tehdään kirjaus tai kun kirjausta ei tehdä, myös työnkulun hyväksyntä vapauttaa myyntitilauksen. Jos vapautusprosessi kuitenkin epäonnistuu puuttuvien asetustietojen tai muiden syiden vuoksi, myyntitilaus on kutsuttava takaisin työnkulusta, virheen aiheuttanut ongelma on korjattava ja tilaus on lähetettävä uudelleen työnkulkuun.

Jos tehtäviä ei sisällytetä työnkulkuun, kun vapauttaessa tehdään kirjaus tai kun kirjausta ei tehdä, työnkulun hyväksyntäprosessi antaa vain mahdollisuuden vapauttaa myyntitilaus manuaalisesti, hyväksyntä on valmis.

### <a name="forced-credit-hold"></a>Pakotettu luottorajapito  
  
Myyntitilaukset on joskus estettävä, vaikka tilaus ei vastaa estosääntöjen kriteerejä. Luottopäällikölle voidaan esimerkiksi ilmoittaa asiakkaan muusta kuin luottoon liittyvästä ongelmasta, ja tämä voi päättää asettaa tilaukset heti manuaalisesti pitoon siihen saakka, että ongelma ratkaistaan. Voit pakottaa myyntitilauksen manuaalisesti pitoon tällaisessa tilanteessa.

1. Avaa myyntitilaus, jonka haluat asettaa pitoon.  
2. Valitse **Pakotettu luottorajapito** **Luotonhallinta**-toimintoruudun **Luotonhallinta**-välilehdessä.
3. Valitse **Pakotetun pidon syy**.
4. Valitse **OK**. Myyntitilaus palautetaan luotonhallinnan pitoluetteloon.

Voit pakottaa pitoon myös useita tilauksia **Luotonhallinta > Kausittaiset tehtävä > Pakota luottorajapito** -sivulla. Voit esimerkiksi asettaa kaikki tietyn asiakkaan myyntitilaukset pitoon.
1. Valitse **Pakotetun pidon syy**. 
2. Valitse pitoon asetettavat myyntitilaukset valitsemalla **Sisällytettävät tietueet**. 
3. Käsittele valitut myyntitilaukset valitsemalla **OK**.

Pitoon pakotettujen myyntitilausten käsittelyyn ei voi käyttää työnkulkua.

#### <a name="releasing-orders-that-were-added-to-the-credit-management-hold-list-with-a-forced-credit-hold"></a>Luotonhallinnan pitoluettelon pakotetulla luottorajapidolla lisättyjen tilausten vapauttaminen
Myyntitilauksia, joilla on pakotetun pidon syy, ei voi vapauttaa automaattisesti. Jos myyntitilaus pakotettiin pitoon ja olet käyttänyt myyntitilaukset automaattisesti vapauttavaa prosessia, myyntitilauksen tilana on nyt **Valmis vapautettavaksi** ja se on edelleen pitoluettelossa. Tilaus on vapautettava **Vapauta**-valikon avulla.
 
## <a name="free-text-invoices-orders-and-project-invoice-support-in-credit-management"></a>Luotonhallinnan vapaatekstilaskujen, tilausten ja projektilaskujen tuki 
Luotonhallintaa voi käyttää tällä hetkellä vain myyntitilauksissa. Vapaatekstilaskut, myyntipistetilaukset ja puhelinkeskustilaukset käyttävät tilapäisiä luottorajoja sekä vakuuksia/takauksia, joita lisäämällä luottorajaa säädetään. Niissä ei käytetä estosääntöjä eikä niitä aseteta pitoluetteloon, jos luottorajassa ongelma.

Luotonhallinta ei tue projektilaskuja.
