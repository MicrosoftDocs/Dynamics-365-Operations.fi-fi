---
title: Tallennetut näkymät
description: Tässä aiheessa kuvataan, miten tallennettujen näkymien toimintoja käytetään.
author: jasongre
manager: AnnBe
ms.date: 03/02/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2019-07-31
ms.dyn365.ops.version: Platform update 28
ms.openlocfilehash: c6a5880c6ae9470dbf7986f39798ec888d0c22ea
ms.sourcegitcommit: 1789a78de1cbeac19d96767812df653a191c67e9
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/05/2020
ms.locfileid: "3100305"
---
# <a name="saved-views"></a>Tallennetut näkymät

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

## <a name="introduction"></a>Johdanto
Mukautuksella on tärkeä rooli, kun käyttäjät ja organisaatiot voivat optimoida käyttäjäkokemuksensa tarpeidensa mukaan. Lisätietoja mukauttamisesta on kohdassa [Käyttäjäkokemuksen mukauttaminen](personalize-user-experience.md).

Perinteisissä personoinneissa käyttäjillä voi olla vain yksi personointijoukko lomaketta kohden. Tallennetut näkymät laajentuvat mukauttamiseen useilla tärkeillä tavoilla:

-    Näkymien avulla käyttäjillä on useita nimettyjä personointeja lomaketta kohden, ja ne voivat tarpeen mukaan siirtyä nopeasti niiden välillä. Näin käyttäjä voi luoda useita optimoituja näkymiä sivusta, jossa jokainen näkymä on räätälöity tietyn liiketoimintatehtävän suoritustarpeiden mukaiseksi. 

-    Tietyille sivutyypeille luodut näkymät voivat olla myös käyttäjän lisäämiä suodattimia tai lajitteluita, joiden avulla käyttäjät voivat nopeasti palata usein suodatettuihin tietojoukkoihin. Lisätietoja [Mitkä sivut tukevat näkymiä](saved-views.md#what-pages-support-views) -osiossa. 

-    Näkymiä voidaan julkaista käyttäjille tietyissä käyttöoikeusrooleissa ja tietyissä yrityksissä. Siten kuka tahansa käyttäjä, jolla on tietty rooli ja pääsyoikeus tietyssä yrityksessä voi käyttää kulloistakin näkymää, vaikka käyttäjä ei pystyisi mukauttamaan sitä. Tämän julkaisutoiminnon avulla organisaatiot voivat määrittää yrityksen vakionäkymiä, jotka on optimoitu heidän liiketoimintaansa varten. Lisätietoja esitetään osassa [Personalisoinnin hallinta organisaation tasolla ja näkymien kera](saved-views.md#managing-personalizations-at-an-organizational-level-with-views).

-    Toisin kuin perinteiset mukautustoiminnot, näkymiä ei tallenneta automaattisesti, kun käyttäjä suorittaa täsmällisiä mukautuksia tai suodattaa luettelon. Täsmälliset tallennukset ovat välttämättömiä, jotta näkymä voidaan luoda joustavasti ennen tai jälkeen näkymään liittyviä muutoksia ja jotta näkymämäärityksiä ei vahingossa muuteta suodattimilla tai räätälöineillä, joita ei ole tarkoitettu pitkäaikaiseen käyttöön.  

-    Näkymiä voidaan lisätä työtiloihin ruutuina, luetteloina tai linkkeinä. Siksi suodatettu tietojoukko voidaan ottaa näkyviin työtilassa, jolloin käyttäjät voivat liittää ruutuun tai linkkiin mukautusjoukon, joka on olennainen tietojoukon kannalta.

## <a name="switching-between-views"></a>Vaihtaminen näkymien välillä
Kun näkymät on otettu käyttöön ympäristössä, kaikki näkymiä tukevat sivut ovat lomakkeen yläosassa tiivistetyn näkymän sen lomakkeen yläosassa, joka näyttää nykyisen näkymän nimen.  

Näkymän valitsimessa on kaksi kokovaihtoehtoa: 

-   **Suuret näkymävalitsimet**: Sivuilla, jotka ovat näkyvästi esillä luettelossa on suurempi näkymävalitsin muutamista syistä. Mikä tärkeintä, suuremman näkymän valitsin ilmaisee sivut, joilla näkymässä voi olla käyttäjän määrittämiä suodattimia. Koska suodattimet sisältyvät näkymään, suuremman valitsimen koko on myös oikeutettu, koska näkymien nimet ovat usein paras kuvaus näytössä näytettyjen tietojen kuvauksessa, ja oletuksena on, että käyttäjät vaihtavat näkymää useammin näillä sivutyypeillä.  
 
-   **Pienet näkymävalitsimet**: Kaikilla muilla kokosivun lomakkeilla (paitsi työtiloissa ja koontinäytöissä) on pienempi näyttövalitsin, joka näkyy sivun otsikon vieressä. Näillä sivuilla olevat näkymät sisältävät vain räätälöinnit (eivätkä käyttäjän määrittämiä suodattimia). Näillä sivuilla lomakkeen otsikko tai tietueen otsikko on usein tärkein tieto lomakkeen yläosassa. Pienempi koko kuvaa myös näiden sivujen odotettua pienempää näyttökertojen määrää. 
 
Jos napsautat näkymän nimeä, näyttöön tulee valintaikkunanäkymä, jossa näkyy käytettävissä olevien näkymien luettelo.

-    **Vakionäkymä**: **Vakio**-näkymä (aiemmin **Perinteinen** näkymä) on sivun käyttövalmis näkymä, johon ei sovelleta eksplisiittisiä mukautuksia.
-    **Henkilökohtaiset näkymät**: Näkymät ilman riippulukkoja edustavat henkilökohtaisia näkymiä. Nämä ovat näkymiä, jotka joko olet luonut tai jotka järjestelmänvalvoja on antanut sinulle.  
-    **Lukitut näkymät**: Joidenkin näkymien (kuten **Vakio**-näkymän ja kaikkien roolillesi julkaistujen näkymien) vieressä näkymänvalitsimessa on lukko. Tämä symboli ilmaisee, että kyseisiä näkymiä ei voi muokata. Implisiittiset mukautukset, jotka perustuvat sivun käyttöön, kuitenkin tallennetaan automaattisesti. Näitä implisiittisiä mukautuksia ovat esimerkiksi ruudukon sarakkeen leveyden muutos tai pikavälilehden laajennus tai kutistus. Jos sinulla kuitenkin on mukautusoikeudet, voit käyttää **Tallenna nimellä** -toimintoa luodaksesi henkilökohtaisen näkymän, joka perustuu lukittuun näkymään.
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
     1.    Valitse **Tallenna nimellä**. 
     2.    Kirjoita näkymän nimi ja (mahdollinen) kuvaus.
     3.    Valitse **Tallenna**.

## <a name="changing-the-default-view"></a>Oletusnäkymän muuttaminen
Oletusnäkymä on näkymä, jota järjestelmä yrittää avata, kun siirryt sivulle. Määritä tämä näkymään, jota odotat käyttäväsi useimmiten.  

Voit vaihtaa sivun oletusnäkymää toimimalla seuraavasti: 
1.  Siirry oletusnäkymään, jota käytät. 
2.  Avaa näkymänvalitsin valitsemalla näkymän nimi. 
3.  Valitse **Lisää** ja **Kiinnitä oletukseksi**.  

Kun luot uuden näkymän (**Tallenna nimellä** -toiminnon avulla), voit vaihtoehtoisesti määrittää uuden näkymän oletusnäkymiksi määrittämällä **PIN-tunnuksen oletusasetukseksi** ennen näkymän tallentamista.

Huomaa, että joissakin tapauksissa oletusnäkymään liittyvä kysely ei ole käytössä, kun siirryt sivulle ensimmäisen kerran. Jos esimerkiksi siirryt ruudun kautta sivulle, ruudun kysely suoritetaan riippumatta oletusnäkymään liittyvästä kyselystä. Jos siirryt sivulle, jonka vakionäkymässä on jo määritetty kysely, alkuperäinen kysely suoritetaan oletusnäkymän kyselyn sijaan. Kun näin tapahtuu, saat ilmoituksen, kun näkymä latautuu. Näkymien vaihtaminen sivun lataamisen jälkeen mahdollistaa sen, että näkymäkysely suoritetaan odotetulla tavalla. Alkaen versiosta 10.0.10 Platform update 34 tietosanoma sisältää upotetun toiminnon, jonka avulla voit ladata oletusnäkymän kyselyn suoraan.

## <a name="managing-personal-views"></a>Henkilökohtaisten näkymien hallinta 
**Omien näkymien hallinta** -valintaikkunan avulla voit hallita omia näkemyksiäsi ja näkymien järjestystä näkymän valitsimessa. Avaa tämä sivu napsauttamalla näkymän nimeä, jolloin näkyviin tulee avattava valikko. Valitse**Lisää** ja valitse sitten**Omien näkymien hallinta**.  

Luettelon käytettävissä olevista näkymistä on käytettävissä seuraavat toiminnot.  
-    **Oletusnäkymän muuttaminen**: Voit tehdä korostetusta näkymästä tämän sivun oletusnäkymän käyttämällä **PIN-koodi oletuksena** -toimintoa.  
-    **Järjestä näkymät uudelleen**: Voit järjestää näkymät tiettyyn järjestykseen **Siirrä ylös**- ja **Siirrä alas** -toimintojen avulla.  
-    **Näkymän nimeäminen uudelleen**: Muuta nykyisen korostetun henkilökohtaisen näkymän nimeä **Nimeä uudelleen** -toiminnon avulla. Tämä toiminto on poistettu käytöstä lukituissa näkymissä. 
-    **Näkymän poistaminen**: **Poista**-toiminnolla voit poistaa nykyisen korostetun näkymän pysyvästi sivulta. Näkymää ei voi palauttaa poistamisen jälkeen.  

Kaikki tähän valintaikkunaan tehdyt muutokset tulevat voimaan, kun valitset **Tallenna**-painikkeen.

## <a name="managing-personalizations-at-an-organizational-level-with-views"></a>Räätälöintien hallinta organisaatiotasolla näkymien avulla
Tässä osassa selitetään tarkemmin, miten tallennetun näkymät parantavat mukautusten hallintaa organisaation tasolla, kuvaamalla joitakin eroja mukautusten hallinnassa tallennettujen näkymien ominaisuuden kanssa ja ilman niitä.

Ilman näkymiä järjestelmänvalvojat käyttävät sivun personointijoukkoa käyttäjälle, käyttäjäryhmälle tai käyttäjille mukautussivun kautta. Jos näillä käyttäjillä on mukautusoikeudet, räätälöinnit otetaan käyttöön kyseiselle sivulle. Ei kuitenkaan ollut mitään mahdollisuutta estää käyttäjiä edelleen räätälöimästä sivua, mikä tarkoitti sitä, että organisaatio ei pystynyt varmistamaan, että käyttäjillä olisi yhdenmukainen käyttöliittymä. Jos jollakin näistä käyttäjistä ei ollut mukautusoikeuksia, järjestelmänvalvojan antamia mukautuksia ei ladattu. Jos uusia käyttäjiä palkattiin organisaatioon, järjestelmänvalvojien piti ladata manuaalisesti käyttäjän personointeja. Ei ollut automaattista mekanismia, jolla voisi määrittää tietyt räätälöinnit, jotka olisivat saatavilla tietyssä roolissa oleville käyttäjille.

Tallennetut näkymät -ominaisuuden avulla mukautusten hallinta on huomattavasti helpompaa, mikä johtuu pääasiassa mahdollisuudesta julkaista näkymiä käyttäjäryhmille. Kun näkymä on julkaistu, kuka tahansa käyttäjä, jolla on jokin määritetyistä käyttöoikeusrooleista ja pääsy määritettyihin yrityksiin, voi nähdä ja käyttää näkymää, vaikka käyttäjä ei välttämättä pystykään mukauttamaan sitä. Vaikka jokaisella käyttäjällä on kopio julkaistusta näkymästä, jossa sivun käyttö (implisiittiset mukautukset) otetaan automaattisesti käyttöön, yksikään käyttäjä ei voi tallentaa eksplisiittisiä mukautuksia tai kyselypäivityksiä julkaistuun näkymään. Toisin sanoen julkaistut näkymät on lukittu. Jos uusille käyttäjille lisäksi annetaan rooleja yrityksissä, joille näkymiä on julkaistu, nämä käyttäjät näkevät automaattisesti ne näkymät, jotka on liitetty heidän rooleihinsa ja yrityksiinsä. Järjestelmänvalvojalta ei tässäkään vaadita lisätoimia. Samoin jos käyttäjien rooli vaihtuu organisaatiossa tai he saavat käyttöönsä muita yrityksiä, he eivät välttämättä enää pysty käyttämään niitä näkymiä, jotka on aiemmin julkaistu heille. Järjestelmänvalvojalta ei tässäkään vaadita lisätoimia.

Julkaistun näkymän päivitykset voidaan jakaa helposti käyttäjille julkaisemalla näkymä uudelleen asianmukaisille käyttöoikeusrooleille ja yrityksille.

Julkaisutoiminnon avulla organisaatiot voivat määrittää heidän liiketoimintaansa varten optimoituja yrityksen vakionäkymiä, jotka on kohdistettu käyttäjille tietyissä turvallisuusrooleissa.  

## <a name="publishing-views"></a>Julkaisunäkymät
Julkaisuprosessin aikana näkymiä voidaan kohdentaa yhdelle tai useammalle yhden tai useamman yrityksen käyttöoikeusroolille. Siksi kaikki käyttäjät, joilla on käytössään yritys ja jolle on kohdennettu yksi näistä rooleista voi käyttää näkymiä, vaikka he eivät voi muokata niitä. Järjestelmänvalvojilla on okeus käyttää **Julkaisu**-toimintoa näkymänvalitsimen avattavasta valikosta. Kuitenkin myös muille luotetuille organisaation jäsenille voidaan antaa oikeus näkymien julkaisuun käyttämällä uutta **Tallennettujen näkymien valvoja** -roolia.

Julkaise näkymä seuraavien ohjeiden avulla: 
1.  Luo ja tallenna sen näkymän henkilökohtainen kopio, jonka haluat julkaista. 
2.  Kun näkymä on ladattuna, avaa avattavan näkymän valitsimen avattavasta valikosta näkymän nimi. 
3.  Valitse **Lisää**-painike ja sitten **Julkaise**. Julkaise-valintaikkuna aukeaa.  
4.  Anna näkymälle nimi ja (mahdollinen) kuvaus. Antamasi nimi on se nimi, jonka tämän näkymän vastaanottavat käyttäjät näkevät näkymänvalitsimissaan. Sivun julkaistujen näkymien nimien on oltava yksilöllisiä. Saman nimen käyttämistä kahdesti ei sallita, vaikka roolit tai yritykset, joille näkymät on kohdennettu, olisivat erilaisia.
5.  Lisää käyttöoikeusroolit, jota vastaavat tämän näkymän kohteena olevia käyttäjiä.
6. Lisää yritykset, joiden käytettävissä näkymän on tarkoitus olla. 
7. [10.0.9/Platform-päivitys 33 tai uudempi] määrittää, julkaistaanko näkymä valittujen käyttäjien oletusnäkyminä. Näkymän oletusarvo tarkoittaa, että tämä on näkymä, jonka käyttäjät näkevät, kun he avaavat kohdesivun seuraavan kerran. Tämä muokkaa oletusnäkymää näille käyttäjille. Käyttäjät voivat kuitenkin edelleen muuttaa oletusnäkymiään julkaisemisen jälkeen.    
8.  Valitse **Julkaise**.

Huomaa, että joissakin ympäristöissä saattaa kestää jonkin aikaa (enintään tunti), ennen kuin käyttäjät näkevät julkaistun näkymän.

## <a name="modifying-a-published-view"></a>Julkaistun näkymän muokkaaminen
Kun olet julkaissut näkymän, saatat huomata, että haluat tehdä muutoksia julkaistuun näkymään. Vaikka et voi tehdä suoria muutoksia julkaistuun näkymään, koska nämä näkymät on lukittu muokkausta varten kaikille käyttäjille (myös julkaisijoille), voit julkaista näkymän uudelleen ja tehdä siihen päivityksiä.  

Jos muutokset, jotka haluat tehdä julkaistavaan näkymään, sisältävät vain julkaisuparametrit (näkymän nimen ja kuvauksen tai käyttöoikeusroolit, joihin näkymä on julkaistu), toimi seuraavasti: 
1.  Siirry päivitettävän parametrin julkaistuun näkymään. 
2.  Valitse **Julkaise** avattavasta valikosta. 
3.  Valitse **Kyllä**, jos haluat päivittää aiemmin luodun näkymän (tai **Ei**, jos haluat julkaista sen eri nimellä).
4.  Päivitä näkymän nimi, kuvaus ja/tai käyttöoikeusroolit. 
5.  Valitse **Julkaise**. 
6.  [10.0.8/Platform update 32 tai aiempi] Jos olet päivittänyt julkaistun näkymän nimen, sinun on myös poistettava julkaistu näkymä vanhalla nimellä (lisätietoja on **Julkaistujen näkymien hallinta** -osassa). 
7. [10.0.9/Platform-päivitys 33 tai uudempi] Jos olet alun perin valinnut tämän julkaistun näkymän oletusnäkymäksi, se on näiden käyttäjien oletusnäkymä uudelleen julkaisemisen jälkeen.  

Jos julkaistuun näkymään tehdyt muutokset edellyttävät näkymään liittyvien räätälöintien tai suodattimien muokkaamista, toimi seuraavasti: 
1.  Siirry julkaistuun näkymään, jota haluat muokata. 
2.  Voit luoda julkaistun näkymän paikallisen luonnoksen tallentamalla julkaistun näkymän kopion. 
3.  Muokkaa paikallista luonnosta tarvittavin muutoksin.
4.  Julkaise näkymä alkuperäisellä nimellä. 

## <a name="managing-published-views"></a>Julkaistujen näkymien hallinta
Omien näkymien hallinnan tapaan **Omien näkymien hallinta** -valintaikkunan avulla käyttäjät, joilla on julkaisuoikeudet, voivat käyttää tämän sivun julkaistuja näkymiä (omien henkilökohtaisten näkymien lisäksi). Avaa tämä sivu valitsemalla näkymän nimeä, jolloin näkyviin tulee avattava valikko. Valitse **Lisää** ja valitse sitten **Omien näkymien hallinta**.

Kun kaikki käyttäjät näkevät **Omat näkymät** -välilehden, jossa näkyvät omat näkymät, julkaisuoikeuksilla varustetut käyttäjät näkevät myös **Julkaistu**-välilehden, jossa näkyvät kaikki sivun julkaistut näkymät. Koska useat käyttäjät voivat julkaista näkymiä, on tärkeää pystyä hallitsemaan täydellistä luetteloa julkaistuista näkymistä riippumatta siitä, onko käyttäjä itse julkaissut näkymän.

Luetteloon sivun kaikista julkaistuista näkymistä on käytettävissä seuraavat toiminnot. 

-    **Julkaise**: **Julkaise**-toiminnon avulla voit julkaista näkymän uudelleen, kun julkaisuparametrit (nimi, kuvaus, käyttöoikeusroolit tai yritykset) ovat muuttuneet.
-    **Poista**: Käytä **Poista**-toimintoa julkaistun näkymän poistamiseen pysyvästi. Tämä toiminto poistaa näkymän kaikilta järjestelmän käyttäjiltä. Julkaistujen näkymien poistaminen tulee voimaan, kun **Tallenna**-painike on valittuna.

## <a name="frequently-asked-questions"></a>Usein kysytyt kysymykset
### <a name="how-do-i-enable-saved-views-in-my-environment"></a>Miten voin ottaa tallennetut näkymät käyttöön omassa ympäristössäni? 
Huomautus: **Tallennetut näkymät** -toiminto edellyttää, että mukautusjärjestelmä Finance and Operationsissa otetaan käyttöön. Jos mukauttaminen on poistettu käytöstä koko ympäristössä, näkymät poistetaan käytöstä, vaikka noudattaisit alla mainittuja vaiheita. 

**10.0.9/Platform-päivitys 33 ja** uudemmat **Tallennetut näkymät** -toiminto on käytettävissä suoraan ominaisuuksienhallinnassa missä tahansa ympäristössä. Kuten muutkin julkiset esikatseluominaisuudet, tämän toiminnon ottaminen käyttöön tuotannossa edellyttää [Lisäkäyttöehdot-sopimusta](https://go.microsoft.com/fwlink/?linkid=2105274).  

**10.0.8/Platform-päivitys 32 ja** aiemmat **Tallennetut näkymät** -ominaisuus voidaan ottaa käyttöön Tier 1 (Dev/Test)- ja Tier 2 (eristysympäristö) -ympäristöissä, jotta voit tarjota lisätestejä ja rakennemuutoksia noudattamalla seuraavia ohjeita.

1.  **Ota pikapäivitys käyttöön**: Suorita seuraava SQL-lause: 

    `INSERT INTO SYSFLIGHTING (FLIGHTNAME, enabled, FLIGHTSERVICEID, PARTITION) VALUES('CLISavedViewsEnableFeature', 1, 0, 5637144576);`

2. **Palauta IIS** tyhjentääksesi staattisen välimuistin. 

3.  **Etsi ominaisuus**: Siirry **Ominaisuuksien hallinta** -työtilaan. Jos **Tallennetut näkymät** eivät näy luettelossa, valitse **Tarkista päivitykset** -painike.   

4.  **Ota ominaisuus käyttöön**: Etsi **Tallennetut näkymät** -ominaisuus ominaisuuksien luettelosta ja napsauta **Ota käyttöön nyt** tietoruudussa.

Kaikki myöhemmät käyttäjäistunnot alkavat, kun tallennetut näkymät ovat käytössä.


### <a name="what-happens-to-existing-personalizations-when-views-are-enabled"></a>Mitä tapahtuu olemassa oleville räätälöinteille, kun näkymät ovat käytössä? 
Kun näkymät ovat käytössä, käyttäjän ja lomakkeen aiemmat mukautukset tallennetaan uuteen **Oma näkymä** -näkymään, joka määritetään automaattisesti oletusnäkymäksi. Tämän on tarkoitus varmistaa, että käyttökokemus on yhtenäinen sekä ennen näkymien käyttöönottoa että sen jälkeen, lukuun ottamatta lomakkeissa näkyvän näkymän valitsin-ohjausobjektia.  

### <a name="what-pages-support-views"></a>Mitkä sivut tukevat näkymiä? 
Näkymiä voi käyttää useimmilla, mutta ei kaikilla sivuilla. Näkymät ovat tällä hetkellä käytettävissä kaikilla koko näytön sivuilla lukuun ottamatta koontinäyttöjä ja työtiloja. Muut kuin kokonäytön sivut, joihin sisältyvät valintaikkunat, avattavat dialogit, haut ja parannetut esikatselut, eivät tue näkymiä. Lisäsivutyyppien, kuten työtilojen ja valintaikkunoiden, tuen tarkasteleminen voidaan ottaa huomioon tulevassa päivityksessä.   

### <a name="who-is-allowed-to-publish-views"></a>Kuka saa julkaista näkymiä?
Vain järjestelmänvalvojilla ja käyttäjillä, joille on osoitettu rooli **Tallennettujen näkymien valvoja**, on oikeus julkaista näkymiä. 

### <a name="why-am-i-not-able-to-save-filters-with-this-view"></a>Miksi suodattimia ei voi tallentaa tämän näkymän avulla? 
On olemassa muutamia syitä siihen, miksi suodatin ei ehkä näy tallennettavassa näkymässä: 

- Sivu ei ehkä tue suodattimien tallentamista näkymämäärityksen yhteydessä. Huomaa, että vain sivut, joilla on suuri näkymävalitsin, sallivat personointien ja kyselyjen muutosten tallentamisen näkymiksi. Lisätietoa on **Näkymän vaihtaminen** -osiossa. 

- Kyseinen sivu ei ehkä tue näkymiä oikein, sillä se saattaa ohittaa näkymäkyselyn kokonaan tai käyttää väliaikaista taulukkoa, jonka tiedot eivät ole pysyviä. 

### <a name="what-data-will-i-see-when-i-visit-a-page"></a>Mitä tietoja näen, kun vierailen sivulla? 
Jos sivuilla on pienet näkymävalitsimet (vain räätälöinnit voidaan tallentaa näkymään), samat tiedot tulevat näkyviin aina, kun käyt sivulla. 

Jos sivuilla on suuret näkymävalitsimet (personoinnit ja kyselyt voidaan tallentaa näkymään), näet ensisijaisesti tiedot, jotka on linkitetty oletusnäkymään liittyvään kyselyyn. Tähän on kaksi pääpoikkeusta: - Jos siirryt ruudusta sivulle, ruudun kysely suoritetaan riippumatta oletusnäkymään liittyvästä kyselystä. Jos olet luonut tämän ruudun näkymien käyttöönoton jälkeen, ruudun valinta avaa sivun, joka sisältää kyseiseen ruutuun liitetyn näkymän.   
     - Jos siirryt sivulle ja aloituskohdassa on kysely, alkuperäinen kysely suoritetaan alkuperäisen oletusnäkymän kyselyn sijaan. Sinun tulisi varoa, kun saat tämän ilmoituksen, kun näkymä latautuu. Voit myös vahvistaa sen siirtymällä tähän näkymään sivun latautuessa, sillä sen pitäisi mahdollistaa näkymäkyselyn suorittaminen riippumatta.  


