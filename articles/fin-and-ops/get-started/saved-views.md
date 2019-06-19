---
title: Tallennetut näkymät
description: Tässä aiheessa kuvataan, miten tallennettujen näkymien toimintoja käytetään.
author: jasongre
manager: AnnBe
ms.date: 06/05/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard
ROBOTS: NOINDEX, NOFOLLOW
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2019-07-31
ms.dyn365.ops.version: Platform update 28
ms.openlocfilehash: ea2f2dbd615480bb76e1d04a106ae69bf6f45f4b
ms.sourcegitcommit: fcae2e7938d7dbd94b76b0948b084d90d5fc919c
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/05/2019
ms.locfileid: "1620775"
---
# <a name="saved-views"></a>Tallennetut näkymät

[!include [banner](../includes/banner.md)]
[!include [private preview banner](../includes/private-preview-banner.md)]

## <a name="introduction"></a>Johdanto
Mukautuksella on tärkeä rooli, kun käyttäjät ja organisaatiot voivat optimoida käyttäjäkokemuksensa Microsoft Dynamics 365 for Finance and Operationsissa tarpeidensa tyydyttämiseksi. Lisätietoja mukauttamisesta on kohdassa [Käyttäjäkokemuksen mukauttaminen](personalize-user-experience.md).

Perinteisissä personoinneissa käyttäjillä voi olla vain yksi personointijoukko lomaketta kohden. Tallennetut näkymät laajentuvat mukauttamiseen useilla tärkeillä tavoilla:

-    Näkymien avulla käyttäjillä on useita nimettyjä personointeja lomaketta kohden, ja ne voivat tarpeen mukaan siirtyä nopeasti niiden välillä. Näin käyttäjä voi luoda useita optimoituja näkymiä sivusta, jossa jokainen näkymä on räätälöity tietyn liiketoimintatehtävän suoritustarpeiden mukaiseksi. 

-    Tietyille sivutyypeille luodut näkymät voivat olla myös käyttäjän lisäämiä suodattimia tai lajitteluita, joiden avulla käyttäjät voivat nopeasti palata usein suodatettuihin tietojoukkoihin. Lisätietoja [Mitkä sivut tukevat näkymiä](saved-views.md#what-pages-support-views) -osiossa. 

-    Näkymät voidaan julkaista käyttöoikeusrooleihin, mikä tarkoittaa sitä, että kuka tahansa käyttäjä, jolla on kyseinen rooli, voi käyttää tätä näkymää riippumatta siitä, mikä on käyttäjän mahdollisuus mukauttaa. Tämän julkaisutoiminnon avulla organisaatiot voivat määrittää yrityksen vakionäkymiä, jotka on optimoitu heidän liiketoimintaansa varten. Lisätietoja on [Personalisoinnin hallinta organisaation tasolla ja näkymien kera](saved-views.md#managing-personalizations-at-an-organizational-level-with-views) -osassa.

-    Toisin kuin perinteiset mukautustoiminnot, näkymiä ei tallenneta automaattisesti, kun käyttäjä suorittaa täsmällisiä mukautuksia tai suodattaa luettelon. Täsmälliset tallennukset ovat välttämättömiä, jotta näkymä voidaan luoda joustavasti ennen tai jälkeen näkymään liittyviä muutoksia ja jotta näkymämäärityksiä ei vahingossa muuteta suodattimilla tai räätälöineillä, joita ei ole tarkoitettu pitkäaikaiseen käyttöön.  

## <a name="switching-between-views"></a>Vaihtaminen näkymien välillä
Kun näkymät on otettu käyttöön ympäristössä, kaikki näkymiä tukevat sivut ovat lomakkeen yläosassa tiivistetyn näkymän sen lomakkeen yläosassa, joka näyttää nykyisen näkymän nimen.  

Näkymän valitsimessa on kaksi kokovaihtoehtoa: 

-   **Suuret näkymävalitsimet**: Sivuilla, jotka ovat näkyvästi esillä luettelossa on suurempi näkymävalitsin muutamista syistä. Mikä tärkeintä, suuremman näkymän valitsin ilmaisee sivut, joilla näkymässä voi olla käyttäjän määrittämiä suodattimia. Koska suodattimet sisältyvät näkymään, suuremman valitsimen koko on myös oikeutettu, koska näkymien nimet ovat usein paras kuvaus näytössä näytettyjen tietojen kuvauksessa, ja oletuksena on, että käyttäjät vaihtavat näkymää useammin näillä sivutyypeillä.  
 
-   **Pienet näkymävalitsimet**: Kaikilla muilla kokosivun lomakkeilla on pienempi näyttövalitsin, joka näkyy sivun otsikon vieressä. Näillä sivuilla olevat näkymät sisältävät vain räätälöinnit (eivätkä käyttäjän määrittämiä suodattimia). Näillä sivuilla lomakkeen otsikko tai tietueen otsikko on usein tärkein tieto lomakkeen yläosassa. Pienempi koko kuvaa myös näiden sivujen odotettua pienempää näyttökertojen määrää. 
 
Jos napsautat näkymän nimeä, näyttöön tulee valintaikkunanäkymä, jossa näkyy käytettävissä olevien näkymien luettelo.

-    **Perinteinen näkymä**: Perinteinen näkymä on sivun ulkopuolella oleva näkymä, johon ei ole kohdistettu täsmällisiä mukautuksia.  
-    **Henkilökohtaiset näkymät**: Näkymät ilman riippulukkoja edustavat henkilökohtaisia näkymiä. Nämä ovat näkymiä, jotka joko olet luonut tai jotka järjestelmänvalvoja on antanut sinulle.  
-    **Lukitut näkymät**: Joidenkin näkymien (kuten perinteisen näkymän ja roolille julkaistujen näkymien) vieressä on lukko, joka ilmaisee, että näitä näkymiä ei voi muokata. Sivun käytön ympärillä olevat epäsuorat mukautukset tallennetaan kuitenkin automaattisesti, esimerkiksi ruudukkosarakkeen leveyden muuttaminen tai pikavälilehden laajentaminen tai kutistaminen. Voit kuitenkin tehdä henkilökohtaisen näkymän lukitun näkymän perusteella käyttämällä **Tallenna kopio** -toimintoa, jos sinulla on mukautusoikeudet.
-    **Uudet näkymät**: Julkaistut näkymät, joita ei ole vielä avattu, rajataan näkymän nimen vasemmalla puolella olevalla sparkilla.  

Jos haluat siirtyä toiseen näkymään, avaa ensin näkymävalitsin ja valitse sitten ladattava näkymä. 

## <a name="creating-and-modifying-views"></a>Näkymien luominen ja muokkaaminen
Toisin kuin perinteiset mukautustoiminnot, näkymiä ei tallenneta automaattisesti, kun käyttäjä suorittaa täsmällisiä mukautuksia (tai suodattaa luettelon). Muutosten tallentaminen näkymään edellyttää täsmällistä toimenpidettä. Tämä antaa käyttäjälle joustavuuden luoda näkymän ennen tai jälkeen kyseiseen näkymään liittyviä muutoksia ja varmistaa myös, että kertaluonteiset suodattimet tai henkilökohtaiset muutokset eivät vahingossa muuta näkymien määritelmiä. Huomaa, että epäsuorat mukautukset (kuten FastTabin laajentaminen tai kokoonpanon katkaiseminen tai ruudukon sarakkeen leveyden muuttaminen) tallennetaan automaattisesti nykyiseen näkymään jopa lukittujen näkymien osalta. 

Jos haluat varmistaa, että näkymän tila on tiedossa, kun aloitat muutosten tekemisen näkymään tekemällä täsmällisen mukautus- tai suodatustoiminnon, nykyisen näkymän nimen viereen tulee tähti, joka osoittaa, että katselet tallentamatonta, muokattua versiota tästä näkymästä.

Jos haluat tallentaa muutokset, toimi seuraavasti.
1.  Avaa näkymänvalitsin valitsemalla näkymän nimi.
2.  Voit muokata aiemmin luotua näkymää seuraavasti:
     1. Valitse **Tallenna**. Huomaa, että tämä toiminto ei ole käytössä lukituissa näkymissä. 
3.  Luo uusi pyyntö:
     1.    Valitse **Tallenna kopio**. 
     2.    Kirjoita näkymän nimi ja (mahdollinen) kuvaus.
     3.    Valitse **Tallenna**.

## <a name="changing-the-default-view"></a>Oletusnäkymän muuttaminen
Oletusnäkymä on näkymä, jota järjestelmä yrittää avata, kun siirryt sivulle. Määritä tämä näkymään, jota odotat käyttävän usein.  

Voit vaihtaa sivun oletusnäkymää toimimalla seuraavasti: 
1.  Siirry oletusnäkymään, jota käytät. 
2.  Avaa näkymänvalitsin valitsemalla näkymän nimi. 
3.  Valitse **Lisää** ja **Kiinnitä oletukseksi**.  

Kun luot uuden näkymän (**Tallenna kopio** -toiminnon avulla), voit vaihtoehtoisesti määrittää uuden näkymän oletusnäkymiksi määrittämällä **PIN-tunnuksen oletusasetukseksi** ennen näkymän tallentamista.  

Huomaa, että joissakin tapauksissa oletusnäkymään liittyvä kysely ei ole käytössä, kun siirryt sivulle ensimmäisen kerran. Jos esimerkiksi siirryt ruudun kautta sivulle, ruudun kysely suoritetaan riippumatta oletusnäkymään liittyvästä kyselystä. Jos siirryt sivulle, jonka perinteisessä näkymässä on jo määritetty kysely, alkuperäinen kysely suoritetaan alkuperäisen oletusnäkymän kyselyn sijaan. Kun näin tapahtuu, saat ilmoituksen, kun näkymä latautuu. Näkymien vaihtaminen sivun lataamisen jälkeen mahdollistaa sen, että näkymäkysely suoritetaan odotetulla tavalla.

## <a name="managing-personal-views"></a>Henkilökohtaisten näkymien hallinta 
**Omien näkymien hallinta** -valintaikkunan avulla voit hallita omia näkemyksiäsi ja näkymien järjestystä näkymän valitsimessa. Avaa tämä sivu napsauttamalla näkymän nimeä, jolloin näkyviin tulee avattava valikko. Valitse**Lisää** ja valitse sitten**Omien näkymien hallinta**.  

Luettelon käytettävissä olevista näkymistä on käytettävissä seuraavat toiminnot.  
-    **Oletusnäkymän muuttaminen**: Voit tehdä korostetusta näkymästä tämän sivun oletusnäkymän käyttämällä **PIN-koodi oletuksena** -toimintoa.  
-    **Järjestä näkymät uudelleen**: Voit järjestää näkymät tiettyyn järjestykseen **Siirrä ylös**- ja **Siirrä alas** -toimintojen avulla.  
-    **Näkymän nimeäminen uudelleen**: Muuta nykyisen korostetun henkilökohtaisen näkymän nimeä **Nimeä uudelleen** -toiminnon avulla. Tämä toiminto on poistettu käytöstä lukituissa näkymissä. 
-    **Näkymän poistaminen**: **Poista**-toiminnolla voit poistaa nykyisen korostetun näkymän pysyvästi sivulta. Näkymää ei voi palauttaa poistamisen jälkeen.  

Kaikki tähän valintaikkunaan tehdyt muutokset tulevat voimaan, kun valitset **Tallenna**-painikkeen.

## <a name="managing-personalizations-at-an-organizational-level-with-views"></a>Räätälöintien hallinta organisaatiotasolla näkymien avulla
Jos haluat tietää, miten personointia hallitaan organisaation tasolla, tarkista ensin, miten personoinnin hallinta on toiminut ennen näkymiä.  

Ilman näkymiä järjestelmänvalvojat käyttävät sivun personointijoukkoa käyttäjälle, käyttäjäryhmälle tai käyttäjille, jotka käyttävät mukautuslomaketta. Jos näillä käyttäjillä on mukautusoikeudet, räätälöinnit otetaan käyttöön kyseiselle sivulle. Ei kuitenkaan ollut mitään mahdollisuutta estää käyttäjiä edelleen räätälöimästä sivua, mikä tarkoitti sitä, että organisaatio ei pystynyt varmistamaan, että käyttäjillä olisi yhdenmukainen käyttöliittymä. Jos jollakin näistä käyttäjistä ei ollut mukautusoikeuksia, järjestelmänvalvojan antamia mukautuksia ei ladattu. Jos uusia käyttäjiä palkattiin organisaatioon, järjestelmänvalvojien piti ladata manuaalisesti käyttäjän personointeja. Ei ollut automaattista mekanismia, jolla voisi määrittää tietyt räätälöinnit, jotka olisivat saatavilla tietylle käyttäjälle.

Tallennetut näkymät -ominaisuuden avulla räätälöinnin hallinta on huomattavasti helpompaa, mikä johtuu pääasiassa mahdollisuudesta julkaista näkymiä käyttöoikeusrooleihin. Kun näkymä on julkaistu, kuka tahansa käyttäjä, jolla on kyseinen rooli, voi käyttää tätä näkymää riippumatta siitä, mikä on käyttäjän mahdollisuus mukauttaa. Vaikka jokaisella käyttäjällä on kopio julkaistusta näkymästä, jossa sivun käyttö (implisiittiset personoinnit) otetaan automaattisesti käyttöön, yksikään käyttäjä ei voi tallentaa eksplisiittisiä personointeja tai päivityksiä kyselyyn julkaistuun näkymään (mikä tarkoittaa, että julkaistut näkymät on lukittu). Lisäksi, jos uusille käyttäjille annetaan rooli, johon näkymä on julkaistu, he näkevät automaattisesti rooleihin liitetyt näkymät ilman järjestelmänvalvojan toimia. Vastaavasti jos käyttäjä muuttaa rooleja organisaatiossa, heidän vanhaan rooliinsa liittyvät näkymät eivät enää ole niiden käytettävissä. Julkaistun näkymän päivitykset voidaan jakaa helposti käyttäjille julkaisemalla näkymä uudelleen asianmukaisille käyttöoikeusrooleille.

Julkaisutoiminnon avulla organisaatiot voivat määrittää heidän liiketoimintaansa varten optimoituja yrityksen vakionäkymiä, jotka on kohdistettu käyttäjille tietyissä turvallisuusrooleissa.  

## <a name="publishing-views"></a>Julkaisunäkymät
Julkaisuprosessin aikana näkymät voidaan liittää yhteen tai useaan käyttöoikeusrooliin, mikä tarkoittaa, että kuka tahansa käyttäjä, jolla on kyseinen rooli, voi käyttää tätä näkymää, vaikka hän ei voi muokata näkymää. Tällä hetkellä vain järjestelmänvalvojilla on oikeus käyttää **Julkaisu**-toimintoa näkymän valitsimen avattavasta valikosta.  

Julkaise näkymä seuraavien ohjeiden avulla: 
1.  Luo ja tallenna sen näkymän henkilökohtainen kopio, jonka haluat julkaista. 
2.  Kun näkymä on ladattuna, avaa avattavan näkymän valitsimen avattavasta valikosta näkymän nimi. 
3.  Valitse **Lisää**-painike ja sitten **Julkaise**. Julkaise-valintaikkuna aukeaa.  
4.  Anna näkymälle nimi ja (mahdollinen) kuvaus. Tämä on nimi, jonka tämän näkymän vastaanottavat käyttäjät näkevät näkymän valitsimien avulla. Huomaa, että julkaistujen näkymien samannimisiä nimiä ei sallita sivulle, vaikka niiden roolien luettelo olisi erilainen.  
5.  Lisää käyttöoikeusroolit, jotka vastaavat tämän näkymän käyttäjiä.  
6.  Valitse **Julkaise**.

Huomaa, että joissakin ympäristöissä saattaa kestää jonkin aikaa (enintään tunti), ennen kuin käyttäjät näkevät julkaistun näkymän.

## <a name="modifying-a-published-view"></a>Julkaistun näkymän muokkaaminen
Kun olet julkaissut näkymän, saatat huomata, että haluat tehdä muutoksia julkaistuun näkymään. Vaikka et voi tehdä suoria muutoksia julkaistuun näkymään, koska nämä näkymät on lukittu muokkausta varten kaikille käyttäjille (myös julkaisijoille), voit julkaista näkymän uudelleen ja tehdä siihen päivityksiä.  

Jos muutokset, jotka haluat tehdä julkaistavaan näkymään, sisältävät vain julkaisuparametrit (näkymän nimen ja kuvauksen tai käyttöoikeusroolit, joihin näkymä on julkaistu), toimi seuraavasti: 
1.  Siirry päivitettävän parametrin julkaistuun näkymään. 
2.  Valitse **Julkaise** avattavasta valikosta. 
3.  Valitse **Kyllä**, jos haluat päivittää aiemmin luodun näkymän (tai **Ei**, jos haluat julkaista sen eri nimellä).
4.  Päivitä näkymän nimi, kuvaus ja/tai käyttöoikeusroolit. 
5.  Valitse **Julkaise**. 
6.  Jos olet päivittänyt julkaistun näkymän nimen, sinun on myös poistettava julkaistu näkymä vanhalla nimellä (lisätietoja on **Julkaistujen näkymien hallinta** -osassa). 

Jos julkaistuun näkymään tehdyt muutokset edellyttävät näkymään liittyvien räätälöintien tai suodattimien muokkaamista, toimi seuraavasti: 
1.  Siirry julkaistuun näkymään, jota haluat muokata. 
2.  Voit luoda julkaistun näkymän paikallisen luonnoksen tallentamalla julkaistun näkymän kopion. 
3.  Muokkaa paikallista luonnosta tarvittavin muutoksin.
4.  Julkaise näkymä alkuperäisellä nimellä. 

## <a name="managing-published-views"></a>Julkaistujen näkymien hallinta
Omien näkymien hallinnan tapaan **Omien näkymien hallinta** -valintaikkunan avulla käyttäjät, joilla on julkaisuoikeudet, voivat käyttää tämän sivun julkaistuja näkymiä (omien henkilökohtaisten näkymien lisäksi). Avaa tämä sivu valitsemalla näkymän nimeä, jolloin näkyviin tulee avattava valikko. Valitse **Lisää** ja valitse sitten **Omien näkymien hallinta**.

Kun kaikki käyttäjät näkevät **Omat näkymät** -välilehden, jossa näkyvät omat näkymät, julkaisuoikeuksilla varustetut käyttäjät näkevät myös **Julkaistu**-välilehden, jossa näkyvät kaikki sivun julkaistut näkymät. Koska useat käyttäjät voivat julkaista näkymiä, on tärkeää pystyä hallitsemaan täydellistä luetteloa julkaistuista näkymistä riippumatta siitä, onko käyttäjä itse julkaissut näkymän.

Luetteloon sivun kaikista julkaistuista näkymistä on käytettävissä seuraavat toiminnot. 

-    **Julkaise**: **Julkaise**-toiminnon avulla voit julkaista näkymän uudelleen muokattujen julkaisuparametrien avulla (nimi, kuvaus, käyttöoikeusroolit).  
-    **Poista**: Käytä **Poista**-toimintoa julkaistun näkymän poistamiseen pysyvästi. Tämä toiminto poistaa näkymän kaikilta järjestelmän käyttäjiltä.  
 
Kaikki tähän valintaikkunaan tehdyt muutokset tulevat voimaan, kun **Tallenna**-painike valitaan.

## <a name="frequently-asked-questions"></a>Usein kysytyt kysymykset
### <a name="how-do-i-enable-saved-views-in-my-environment"></a>Miten voin ottaa tallennetut näkymät käyttöön omassa ympäristössäni? 
Jos haluat ottaa tallennetut näkymät käyttöön, järjestelmänvalvojan on tehtävä seuraavat toimet: 
1.  Siirry **Mukautus**-sivulle käyttämällä siirtymishakua. 
2.  Valitse **Asetukset**-välilehti.
3.  Määritä **Ota tallennetut näkymät käyttöön** -asetukseksi **Kyllä**.

Kun tämä toiminto on otettu käyttöön, kaikki myöhemmät käyttäjäistunnot alkavat näkymien ollessa käytössä.  

Huomaa, että jos mukauttaminen on poistettu käytöstä ympäristössä, näkymät otetaan käyttöön, vaikka noudattaisit edellä mainittuja vaiheita. Tämä johtuu siitä, että näkymät-toiminto on rakennettu personointi-alijärjestelmän yläosaan.

### <a name="what-happens-to-existing-personalizations-when-views-are-enabled"></a>Mitä tapahtuu olemassa oleville räätälöinteille, kun näkymät ovat käytössä? 
Kun näkymät ovat käytössä, käyttäjän ja lomakkeen aiemmat mukautukset tallennetaan uuteen **Oma näkymä** -näkymään, joka määritetään automaattisesti oletusnäkymäksi. Tämän on tarkoitus varmistaa, että käyttökokemus on yhtenäinen sekä ennen näkymien käyttöönottoa että sen jälkeen, lukuun ottamatta lomakkeissa näkyvän näkymän valitsin-ohjausobjektia.  

### <a name="what-pages-support-views"></a>Mitkä sivut tukevat näkymiä? 
Näkymiä voi käyttää useimmilla, mutta ei kaikilla Finance and Operations -sivuilla. Näkymät ovat tällä hetkellä käytettävissä kaikilla koko näytön sivuilla lukuun ottamatta koontinäyttöjä ja työtiloja. Muut kuin kokonäytön sivut, joihin sisältyvät valintaikkunat, avattavat dialogit, haut ja parannetut esikatselut, eivät myöskään tue näkymiä. Lisäsivutyyppien, kuten työtilojen ja valintaikkunoiden, tuen tarkasteleminen voidaan ottaa huomioon tulevassa päivityksessä.   

### <a name="who-is-allowed-to-publish-views"></a>Kuka saa julkaista näkymiä?
Tällä hetkellä järjestelmänvalvojat ovat ainoat käyttäjät, joilla on oikeus julkaista näkymiä.  Suunnitteilla on uusi käyttöoikeusrooli, joka antaa asiakkaille enemmän joustavuutta julkaisuihin.  

### <a name="why-am-i-not-able-to-save-filters-with-this-view"></a>Miksi suodattimia ei voi tallentaa tämän näkymän avulla? 
On olemassa muutamia syitä siihen, miksi suodatin ei ehkä näy tallennettavassa näkymässä: 

- Sivu ei ehkä tue suodattimien tallentamista näkymämäärityksen yhteydessä. Huomaa, että vain sivut, joilla on suuri näkymävalitsin, sallivat personointien ja kyselyjen muutosten tallentamisen näkymiksi. Lisätietoa on Näkymän vaihtaminen -osiossa 

- Jos näkymä on oletusnäkymä ja sivun siirtymispolku sisältää kyselyn, näkymän kyselyä ei ehkä käytetä aluksi. Kaksi ensisijaista skenaariota ovat seuraavat: 
     - Jos siirryt ruudusta sivulle, ruudun kysely suoritetaan riippumatta oletusnäkymään liittyvästä kyselystä. 
     - Jos siirryt sivulle ja aloituskohdassa on kysely, alkuperäinen kysely suoritetaan alkuperäisen oletusnäkymän kyselyn sijaan. 
     
  Näissä tapauksissa saat ilmoituksen, kun näkymä latautuu. Voit myös vahvistaa sen siirtymällä tähän näkymään sivun latautuessa, sillä sen pitäisi mahdollistaa näkymäkyselyn suorittaminen riippumatta.  

- Kyseessä oleva sivu ei ehkä tue näkymiä oikein, sillä se voi ohittaa tarkastelukyselyn kokonaan. Ilmoita tällaisista tapauksista **Palaute**-mekanismin kautta. Pääset palautesivulle valitsemalla **Ohje ja tuki** ja sitten **Palaute**.  