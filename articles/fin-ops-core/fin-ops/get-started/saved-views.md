---
title: Tallennetut näkymät
description: Tässä aiheessa kuvataan, miten tallennettujen näkymien toimintoja käytetään.
author: jasongre
ms.date: 09/13/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2019-07-31
ms.dyn365.ops.version: Platform update 28
ms.openlocfilehash: d6a7b1b21816db43a92364584e15ec04b891c611
ms.sourcegitcommit: 7a2001e4d01b252f5231d94b50945fd31562b2bc
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/15/2021
ms.locfileid: "7487838"
---
# <a name="saved-views"></a>Tallennetut näkymät

[!include [banner](../includes/banner.md)]

## <a name="introduction"></a>Johdanto

Mukautuksella on tärkeä rooli, kun käyttäjät ja organisaatiot voivat optimoida käyttäjäkokemuksensa tarpeidensa mukaan. Lisätietoja mukauttamisesta on kohdassa [Käyttäjäkokemuksen mukauttaminen](personalize-user-experience.md).

Perinteisissä personoinneissa käyttäjillä voi olla vain yksi personointijoukko sivua kohden. **Tallennetut näkymät** -ominaisuus laajentaa mukauttamista useitta tärkeillä tavoilla seuraavasti:

- Näkymien avulla käyttäjillä on useita nimettyjä personointeja lomaketta kohden, ja ne voivat tarpeen mukaan siirtyä nopeasti niiden välillä. Näin käyttäjä voi luoda useita optimoituja näkymiä sivusta, jossa jokainen näkymä on räätälöity tietyn liiketoimintatehtävän suoritustarpeiden mukaiseksi. 
- Tietyille sivutyypeille luodut näkymät voivat olla myös käyttäjän lisäämiä suodattimia tai lajitteluita, joiden avulla käyttäjät voivat nopeasti palata usein suodatettuihin tietojoukkoihin. Lisätietoja [Mitkä sivut tukevat näkymiä](saved-views.md#what-pages-support-views) -osiossa. 
- Näkymiä voidaan julkaista käyttäjille tietyissä käyttöoikeusrooleissa ja tietyissä yrityksissä. Siten kuka tahansa käyttäjä, jolla on tietty rooli ja pääsyoikeus tietyssä yrityksessä voi käyttää kulloistakin näkymää, vaikka käyttäjällä ei olisi mukauttamisoikeuksia. Tämän julkaisutoiminnon avulla organisaatiot voivat määrittää yrityksen vakionäkymiä, jotka on optimoitu heidän liiketoimintaansa varten. Lisätietoja esitetään osassa [Personalisoinnin hallinta organisaation tasolla ja näkymien kera](saved-views.md#managing-personalizations-at-an-organizational-level-with-views).
- Toisin kuin perinteiset mukautustoiminnot, näkymiä ei tallenneta automaattisesti, kun käyttäjä suorittaa mukautuksia tai suodattaa luettelon. Eksplisiittisiä tallennuksia tarvitaan, jotta käyttäjät voivat joustavasti luoda näkymän ennen muutosten liittämistä näkymään tai sen jälkeen. Vaatimukset varmistavat myös sen, että suodatukset tai mukautukset eivät vahingossa muuta näkymän määrityksiä pitkäaikaisessa käytössä. Nimikkeet, jotka järjestelmä tallentaa automaattisesti osana tyypillistä sivun käyttöä (esimerkiksi sarakkeiden leveydet tai osien laajennettu tai tiivistetty tila), tallennetaan näkymäkohtaisesti.
- Näkymiä voidaan lisätä työtiloihin ruutuina, luetteloina tai linkkeinä. Siksi suodatettu tietojoukko voidaan ottaa näkyviin työtilassa, jolloin käyttäjät voivat liittää ruutuun tai linkkiin mukautusjoukon, joka on olennainen tietojoukon kannalta.

## <a name="switching-between-views"></a>Vaihtaminen näkymien välillä

Kun näkymät on määritetty käytettäviksi ympäristössä, kaikkien näkymiä tukevien sivujen yläosissa on tiivistetyn näkymän valintaohjausobjekti. Se näyttää nykyisen näkymän nimen.

Näkymän valitsimessa on kaksi kokovaihtoehtoa: 

- **Suuret näkymävalitsimet** – Sivuilla, jotka ovat näkyvästi esillä luettelossa on suurempi näkymävalitsin muutamista syistä. Mikä tärkeintä, suuremman näkymän valitsin ilmaisee sivut, joilla näkymässä voi olla käyttäjän määrittämiä suodattimia. Koska suodattimet sisältyvät näkymään, suuremman valitsimen koko on myös oikeutettu, koska näkymien nimet ovat usein paras kuvaus näytössä näytettyjen tietojen kuvauksessa, ja oletuksena on, että käyttäjät vaihtavat näkymää useammin näillä sivutyypeillä.
- **Pienet näkymävalitsimet** – Kaikilla muilla koko näytön sivuilla (paitsi työtiloissa ja koontinäytöissä) on pienempi näyttövalitsin, joka näkyy sivun otsikon vieressä. Näillä sivuilla olevat näkymät sisältävät vain mukautukset, eivät käyttäjän määrittämiä suodattimia. Näillä sivuilla otsikko tai tietueen otsikko on usein tärkein tieto sivun yläosassa. Näkymävalitsimen pienempi koko kuvaa myös näiden sivujen odotettua pienempää näyttökertojen määrää. 
 
Jos valitset näkymän nimen, näyttöön tulee valintaikkunanäkymä, jossa näkyy käytettävissä olevien näkymien luettelo.

**Version 10.0.21 tai uudempi:** Jos **Tallennettujen näkyvien parannettu yritystuki** -ominaisuus on otettu käyttöön, käytettävissä olevat näkymät näkyvät näkymänvalitsimessa kahdessa osassa. Ensimmäisessä osassa on näkyvissä kaikki nykyisen yrityksen näkymät ja toisessa osassa on näkyvissä kaikissa yrityksissä käytettävissä olevat näkymät. Ensimmäinen osa näkyy vain, jos sivulla on yrityskohtaisia näkymiä.

- **Vakionäkymä** – **Vakionäkymä** on sivun valmis näkymä, johon ei ole kohdistettu mukautuksia.
- **Henkilökohtaiset näkymät** – Näkymät ilman riippulukkoja edustavat henkilökohtaisia näkymiä. Nämä ovat näkymiä, jotka joko olet luonut tai jotka järjestelmänvalvoja on antanut sinulle.
- **Lukitut näkymät** – Joidenkin näkymien (kuten **Vakio**-näkymän ja kaikkien roolillesi julkaistujen näkymien) vieressä näkymänvalitsimessa on lukko. Tämä symboli ilmaisee, että kyseisiä näkymiä ei voi muokata. Mukautukset, jotka perustuvat sivun käyttöön, kuitenkin tallennetaan automaattisesti. Nämä muutokset sisältävät ruudukon sarakkeen leveyden muutokset sekä pikavälilehden laajennetun tai tiivistetyn tilan muutokset. Jos sinulla kuitenkin on mukautusoikeudet, voit käyttää **Tallenna nimellä** -toimintoa luodaksesi henkilökohtaisen näkymän, joka perustuu lukittuun näkymään.
- **Uudet näkymät** – Julkaistut näkymät, joita ei ole vielä avattu, sisältävät kipinäsymbolin näkymän nimen vasemmalla puolella.

Jos haluat siirtyä toiseen näkymään, avaa ensin näkymävalitsin ja valitse sitten ladattava näkymä. 

## <a name="creating-and-modifying-views"></a>Näkymien luominen ja muokkaaminen

Toisin kuin perinteisen mukautuksen näkymät, näitä ei tallenneta automaattisesti käyttäjän mukauttaessa sivua tai käyttäjän kohdistaessa luetteloon suodattimen tai lajitellessa suodatinta. Muutosten tallentaminen näkymään edellyttää täsmällistä toimenpidettä. Tämän vaatimuksen avulla käyttäjät voivat joustavasti luoda näkymän ennen muutosten liittämistä näkymään tai sen jälkeen. Tämä varmistaa myös sen, että kertasuodattimet tai mukautukset eivät vahingossa muuta näkymän määrityksiä. Huomaa, että tyypillisen sivun käytön nimikkeet (esimerkiksi sarakkeiden leveydet tai osien laajennettu tai tiivistetty tila) tallennetaan automaattisesti nykyiseen näkymään, myös lukituissa näkymissä.

Tarkista, että nykyisen näkymän nimen vieressä on tähti (\*). Näin voit varmistaa, että näkymän nykyinen tila on tiedossa, kun aloitat näkymän muuttamisen mukauttamalla tai suodattamalla. Tämä symboli osoittaa, että näkymä on tallentamaton ja muokattu versio.

Jos haluat tallentaa muutokset, toimi seuraavasti.

1. Avaa näkymänvalitsin valitsemalla näkymän nimi.
2. Voit muokata aiemmin luotua näkymää valitsemalla **Tallenna**. Huomaa, että tämä toiminto ei ole käytettävissä lukituissa näkymissä. 
3. Luo uusi pyyntö:

    1. Valitse **Tallenna nimellä**. 
    2. Anna **Tallenna näkymä nimellä** ruudussa näkymän nimi ja valinnaisesti myös sen kuvaus.
    3. Jos tätä näkymää halutaan käyttää oletusnäkymänä, valitse **Kiinnitä oletukseksi**. Lisätietoja oletusnäkymistä on seuraavassa osassa [Oletusnäkymän muuttaminen](#changing-the-default-view). 
    4. **Versio 10.0.21 tai uudempi:** jos **Tallennettujen näkymien parannettu yritystuki** -ominaisuus on otettu käytötön, tämän näkymän osalta voidaan valita, onko se kaikkien yritysten vai vain yritysten alijoukon käytettävissä.
    5. Valitse **Tallenna**.

## <a name="changing-the-default-view"></a>Oletusnäkymän muuttaminen

Oletusnäkymä on näkymä, jota järjestelmä yrittää avata, kun avaat sivun ensimmäisen kerran. Määritä tämä oletusnäkymäksi näkymä, jota aiot käyttää eniten. 

> [!NOTE]
> - **Tallennetut näkymät** -perusominaisuudessa on yksi, yleinen kaikkia yrityksiä koskeva oletusnäkymä. Jos muutat oletusnäkymää, kyseinen näkymä avataan oletusarvoisesti käytössä olevasta yrityksestä huolimatta.
> - **Versio 10.0.21 tai uudempi:** kun **Tallennettujen näkymien parannettu yritystuki** -ominaisuus on otettu käyttöön, kullakin yrityksellä voi olla oma sivukohtainen oletusnäkymä.

Voit vaihtaa sivun oletusnäkymää toimimalla seuraavasti:

1. Siirry oletusnäkymään, jota käytät. 
2. Avaa näkymänvalitsin valitsemalla näkymän nimi. 
3. Valitse **Lisää** ja **Kiinnitä oletukseksi**.

Kun luot uuden näkymän (**Tallenna nimellä** -toiminnon avulla), voit vaihtoehtoisesti määrittää uuden näkymän oletusnäkymiksi määrittämällä **PIN-tunnuksen oletusasetukseksi** ennen näkymän tallentamista.

> [!WARNING]
> Joissakin tapauksissa oletusnäkymään liittyvää kyselyä ei suoriteta, kun sivu avataan ensimmäisen kerran. Jos esimerkiksi avaat sivun ruudun kautta, ruudun kysely suoritetaan riippumatta oletusnäkymään liittyvästä kyselystä. Jos lisäksi avataan sivu, jonka **vakionäkymässä** on jo määritetty kysely, alkuperäinen kysely suoritetaan oletusnäkymän kyselyn sijaan. Tässä tapauksessa näyttöön tulee tietosanoma, kun näkymä ladataan. Jos näkymää vaihdetaan sivun lataamisen jälkeen, näkymän kysely on mahdollista suorittaa odotetusti. Alkaen versiosta 10.0.10 vastaanotettava tietosanoma sisältää upotetun toiminnon, jonka avulla voit ladata oletusnäkymän kyselyn suoraan.

## <a name="managing-personal-views"></a>Henkilökohtaisten näkymien hallinta

**Omien näkymien hallinta** -valintaikkunan avulla voit hallita omia näkemyksiäsi ja näkymien järjestystä näkymän valitsimessa. Avaa tämä sivu valitsemalla näkymän nimeä, jolloin näkyviin tulee avattava valikko. Valitse **Lisää** ja valitse sitten **Omien näkymien hallinta**.

**Versio 10.0.21 tai uudempi:** Jos **Tallennettujen näkymien parannettu yritystuki** -ominaisuus on otettu käyttöön **Omien näkymien hallinta** -valintaikkunan **Omat näkymät** -osassa on osia, jossa on näkyvissä sivun käytettävissä olevat näkymät. Kaikki nykyistä yritystä koskevat näkymät näkyvät omassa osassa. **Yleiset näkymät** -osa on aina näkyvissä, joten sivun kaikkien yritysten käytettävissä olevia näkymiä voidaan hallita. 

Luettelon käytettävissä olevista näkymistä on käytettävissä seuraavat toiminnot.

- **Oletusnäkymän muuttaminen** – Voit tehdä valitusta näkymästä tämän sivun oletusnäkymän käyttämällä **PIN-koodi oletuksena** -toimintoa. Jos **Tallennettujen näkymien parannettu yritystuki** -ominaisuus on otettu käyttöön, **Yleiset näkymät** -osassa näkymästä voidaan tehdä joko nykyisen yrityksen tai kaikkien yritysten oletusnäkymä.
- **Järjestä näkymät uudelleen** – Voit järjestää näkymät tiettyyn järjestykseen **Siirrä ylös**- ja **Siirrä alas** -toimintojen avulla.
- **Näkymän nimeäminen uudelleen** – Muuta nykyisen valitun henkilökohtaisen näkymän nimeä **Nimeä uudelleen** -toiminnon avulla. Tämä toiminto on poistettu käytöstä lukituissa näkymissä. 
- **Näkymän poistaminen** – **Poista**-toiminnolla voit poistaa nykyisen valitun näkymän pysyvästi sivulta. Näkymää ei voi palauttaa poistamisen jälkeen.

Kaikki tähän valintaikkunaan tehdyt muutokset otetaan käyttöön, kun **Tallenna**-painike valitaan.

## <a name="managing-personalizations-at-an-organizational-level-with-views"></a>Räätälöintien hallinta organisaatiotasolla näkymien avulla

Tässä osassa selitetään tarkemmin, miten tallennetun näkymät parantavat mukautusten hallintaa organisaation tasolla, kuvaamalla joitakin eroja mukautusten hallinnassa **tallennettujen näkymien** ominaisuuden kanssa ja ilman niitä.

Ilman näkymiä järjestelmänvalvojat käyttävät sivun personointijoukkoa käyttäjälle, käyttäjäryhmälle tai käyttäjille mukautussivun kautta. Jos näillä käyttäjillä on mukautusoikeudet, räätälöinnit otetaan käyttöön kyseiselle sivulle. Ei kuitenkaan ollut mitään mahdollisuutta estää käyttäjiä edelleen räätälöimästä sivua, mikä tarkoitti sitä, että organisaatio ei pystynyt varmistamaan, että käyttäjillä olisi yhdenmukainen käyttöliittymä. Jos jollakin näistä käyttäjistä ei ollut mukautusoikeuksia, järjestelmänvalvojan antamia mukautuksia ei ladattu. Jos uusia käyttäjiä palkattiin organisaatioon, järjestelmänvalvojien piti ladata manuaalisesti käyttäjän personointeja. Ei ollut automaattista mekanismia, jolla voisi määrittää tietyt räätälöinnit, jotka olisivat saatavilla tietyssä roolissa oleville käyttäjille.

**Tallennetut näkymät** -ominaisuuden avulla mukautusten hallinta on huomattavasti helpompaa, mikä johtuu pääasiassa mahdollisuudesta julkaista näkymiä käyttäjäryhmille. Kun näkymä on julkaistu, kuka tahansa käyttäjä, jolla on jokin määritetyistä käyttöoikeusrooleista ja pääsy määritettyihin yrityksiin, voi nähdä ja käyttää näkymää, vaikka käyttäjällä ei olisi mukautusoikeutta. Vaikka jokaisella käyttäjällä on kopio julkaistusta näkymästä, jossa sivun käytön nimikkeet otetaan automaattisesti käyttöön, yksikään käyttäjä ei voi tallentaa eksplisiittisiä mukautuksia tai kyselypäivityksiä julkaistuun näkymään. Toisin sanoen julkaistut näkymät on lukittu. Jos uusille käyttäjille lisäksi annetaan rooleja yrityksissä, joille näkymiä on julkaistu, nämä käyttäjät näkevät automaattisesti ne näkymät, jotka on liitetty heidän rooleihinsa ja yrityksiinsä. Järjestelmänvalvojalta ei vaadita muita toimia. Samoin jos käyttäjien rooli vaihtuu organisaatiossa tai he saavat käyttöönsa muita yrityksiä, he eivät välttämättä enää pysty käyttämään niitä näkymiä, jotka on aiemmin julkaistu heille. Järjestelmänvalvojalta ei tässäkään vaadita lisätoimia.

Julkaistun näkymän päivitykset voidaan jakaa helposti käyttäjille julkaisemalla näkymä uudelleen asianmukaisille käyttöoikeusrooleille ja yrityksille.

Julkaisutoiminnon avulla organisaatiot voivat määrittää heidän liiketoimintaansa varten optimoituja yrityksen vakionäkymiä, jotka on kohdistettu käyttäjille tietyissä turvallisuusrooleissa.

## <a name="publishing-views"></a>Julkaisunäkymät

Julkaisuprosessin aikana näkymiä voidaan kohdentaa yhdelle tai useammalle yhden tai useamman yrityksen käyttöoikeusroolille. Siksi kaikki käyttäjät, joilla on käytössään yritys ja jolle on kohdennettu yksi näistä rooleista voi käyttää näkymiä. Käyttäjä ei kuitenkaan voi muokata näkymiä. Oletusarvoisesti järjestelmänvalvojilla on oikeus käyttää **Julkaisu**-toimintoa näkymänvalitsimen avattavasta valikosta. Kuitenkin myös muille luotetuille organisaation jäsenille voidaan antaa oikeus näkymien julkaisuun käyttämällä uutta **Tallennettujen näkymien valvoja** -roolia.

Julkaise näkymä seuraavien ohjeiden avulla:

1. Luo ja tallenna sen näkymän henkilökohtainen kopio, jonka haluat julkaista. 
2. Kun näkymä on ladattuna, avaa avattavan näkymän valitsimen avattavasta valikosta näkymän nimi. 
3. Valitse **Lisää**-painike ja sitten **Julkaise**. Julkaise-valintaikkuna aukeaa.
4. Anna näkymän nimi. Antamasi nimi on se nimi, jonka tämän näkymän vastaanottavat käyttäjät näkevät näkymänvalitsimissaan. Sivun julkaistujen näkymien nimien on oltava yksilöllisiä. Saman nimen käyttämistä kahdesti ei sallita, vaikka roolit tai yritykset, joille näkymät on kohdennettu, olisivat erilaisia.
5. **Päivitys 10.0.17 tai uudempi:** Jos **(Esiversio) Organisaationäkymien käännöstuki** -toiminto on otettu käyttöön, näkymän nimen käännökset voidaan lisätä organisaation tarvitsemilla kielillä valitsemalla **Käännökset**-painike **Nimi**-kentän vieressä. Näkymän nimi näytetään sitten käyttäjille heidän valittuna olevalla kielellä. Voit myös määrittää oletuskielen määrittämään käännös, joka näytetään käyttäjille, kun heidän käyttämälleen kielelle ei ole määritetty käännöstä.
5. Valinnainen: Anna näkymän kuvaus, joka selittää näkymän saaville käyttäjille sen tarkoituksen. 
6. Määritä, julkaistaanko näkymä valittujen käyttäjien oletusnäkyminä. Kun näkymä määritetään oletusarvoksi, käyttäjät näkevät sen, kun he avaavat kohdesivun seuraavan kerran. Jokaisen kohdekäyttäjän yksittäinen, yleinen oletusnäkymä muuttuu. Käyttäjät voivat kuitenkin edelleen muuttaa oletusnäkymiään julkaisemisen jälkeen.

    > [!NOTE]
    > Seuraava toiminta on otettava huomioon, kun näkymä julkaistaan oletusnäkymänä:
    >
    > - Jos näkymä julkaistaan joidenkin tai kaikkien yritysten oletusnäkymänä, toiminta on seuraavanlaista:
    >
    >    - Jos vain **Tallennetut näkymät** -perusominaisuus otetaan käyttöön, jokaiselle kohdennetulle käyttäjälle vaihdetaan yksi, yleinen oletusnäkymä. 
    >    - **Versio 10.0.21 tai uudempi:** jos **Tallennettujen näkymien parannettu yritystuki** -ominaisuus otetaan käyttöön ja näkymä julkaistaan yritysten alijoukolle, kyseisten yritysten oletusnäkymä muuttuu jokaisen kohdennetun käyttäjän osalta.
    >
    > - Jos käyttäjällä on rooleja, joissa useita näkymiä julkaistaan oletusnäkyminä, viimeksi julkaistua näkymää käytetään käyttäjän oletusnäkymänä. 

8. Lisää käyttöoikeusroolit, jota vastaavat tämän näkymän kohteena olevia käyttäjiä. 
9. Määritä, julkaistaanko näkymä kunkin valitun käyttöoikeusroolin aliroolille. Jos näin tehdään, valitse **Sisällytä aliroolit** -valintaruutu soveltuvien käyttöoikeusroolien rivillä. Huomaa, että tämä valintaruutu ei ole käytettävissä rooleille, joilla ei ole alirooleja.
10. Lisää yritykset, joiden käytettävissä näkymän on tarkoitus olla. 

    > [!NOTE]
    > Seuraava toiminta on otettava huomioon, jos näkymä julkaistaan tietyssä yrityksessä eikä kyseistä näkymää julkaista oletusnäkymänä:
    >
    > - Jos vain **Tallennetut näkymät** -perusominaisuus otetaan käyttöön, käyttäjän sivun näkymänvalitsin näyttää näkymän vain määritetyissä yrityksissä. Sen jälkeen kun näkymä on kuitenkin ladattu ensimmäisen kerran, se näkyy aina sivun näkymävalitsimessa riippumatta siitä, mikä yritys on kyseessä.
    > - **Version 10.0.21 tai uudempi:** Jos **Tallennettujen näkyvien parannettu yritystuki** -ominaisuus on otettu käyttöön, näkymänvalitsin näyttää näkymän aina vain määritetyille yrityksille.

11. Valitse **Julkaise**.

Huomaa, että joissakin ympäristöissä saattaa kestää jonkin aikaa (enintään tunti), ennen kuin käyttäjät näkevät julkaistun näkymän.

## <a name="modifying-a-published-view"></a>Julkaistun näkymän muokkaaminen

Kun olet julkaissut näkymän, haluat ehkä muuttaa sitä. Vaikka et voi tehdä suoria muutoksia julkaistuun näkymään, koska nämä näkymät on lukittu muokkausta varten kaikille käyttäjille (myös julkaisijoille), voit julkaista näkymän uudelleen ja tehdä siihen päivityksiä.

Jos muutokset, jotka haluat tehdä julkaistavaan näkymään, sisältävät vain julkaisuparametrit (näkymän nimen ja kuvauksen tai käyttöoikeusroolit, joihin näkymä on julkaistu), toimi seuraavasti:

1. Siirry päivitettävän parametrin julkaistuun näkymään. 
2. Valitse näkymävalitsimen avattavassa valikossa **Julkaise uudelleen**. Jos käytössä on versio 10.0.12 tai uudempi versio, valitse **Julkaise** ja valitse sitten **Kyllä**, jos haluat päivittää olemassa olevan version.
3. Päivitä näkymän nimi, kuvaus, käyttöoikeusroolit ja yritykset. 
4. Valitse **Julkaise**. Jos valitsit alun perin tämän julkaistun näkymän oletusnäkymäksi, se on oletusnäkymä käyttäjille myös uudelleenjulkaisun jälkeen. 

Jos julkaistuun näkymään tehdyt muutokset edellyttävät näkymään liittyvien räätälöintien tai suodattimien muokkaamista, toimi seuraavasti:

1. Lataa julkaistu näkymä, jota haluat muuttaa. 
2. Tee tarvittavat muutokset paikalliseen luonnokseen.
3. Valitse näkymävalitsimen avattavassa valikossa **Julkaise uudelleen**.
4. Valitsemalla **Kyllä** voit määrittää, että haluat julkaista näkymän yhdessä sen tallentamattomien muutosten kanssa. 
5. Oikaise julkaisun parametreja tarvittaessa ja valitse sitten **Julkaise**. 

## <a name="managing-published-views"></a>Julkaistujen näkymien hallinta

Omien näkymien hallinnan tapaan **Omien näkymien hallinta** -valintaikkunan avulla käyttäjät, joilla on julkaisuoikeudet, voivat käyttää tämän sivun julkaistuja näkymiä (omien henkilökohtaisten näkymien lisäksi). Avaa tämä sivu valitsemalla näkymän nimeä, jolloin näkyviin tulee avattava valikko. Valitse **Lisää** ja valitse sitten **Omien näkymien hallinta**.

Vaikka kaikilla käyttäjillä on **Omat näkymät** -välilehti, jossa näkyvät omat näkymät, julkaisuoikeudet omaavilla käyttäjillä on myös **Organisaationäkymät**-välilehti. Se sisältää kyseisen sivun kaikki julkaistut ja julkaisemattomat näkymät. Koska useat käyttäjät voivat julkaista näkymiä, on tärkeää pystyä hallitsemaan täydellistä luetteloa julkaistuista näkymistä riippumatta siitä, kuka on julkaissut näkymän.

Luetteloon sivun kaikista julkaistuista näkymistä on käytettävissä seuraavat toiminnot. 

- **Julkaise uudelleen** – **Julkaise**-toiminnon avulla voit julkaista näkymän uudelleen, kun julkaisuparametrit (nimi, kuvaus, käyttöoikeusroolit tai yritykset) ovat muuttuneet.
- **Julkaise** – **Julkaise**-toiminnon avulla voit julkaista näkymän, joka on tällä hetkellä julkaisematon. 
- **Peruuta julkaisu** – **Peruuta julkaisu** -toiminnon avulla voit tehdä näkymästä passiivisen. Näkymä on edelleen käytettävissä järjestelmässä, mutta käyttäjät eivät näe sitä näkymävalitsimessa ennen näkymän uudelleenjulkaisua.
- **Tallenna henkilökohtaisena** – Voit luoda henkilökohtaisen luonnoskopion julkaistusta näkymästä **Tallenna henkilökohtaisena** -toiminnolla. Tämän ominaisuuden avulla voit ymmärtää sellaisen näkymän sisällön, jota ei ole julkaistu sinulle tai jota ei ole vielä julkaistu. Sen avulla voit myös muokata näkymää ja julkaista sen uudelleen.
- **Poista** – Käytä **Poista**-toimintoa, jos haluat poistaa pysyvästi julkaistun näkymän tai näkymän, jonka julkaisu on peruutettu. Tämä toiminto poistaa näkymän myös kaikilta järjestelmän käyttäjiltä. Julkaistujen näkymien poistaminen tulee voimaan, kun **Tallenna**-painike valitaan. Kun näkymä on poistettu, sitä ei voi palauttaa. 

## <a name="managing-views-globally"></a>Näkymien hallinta globaalisti

Vaikka jotkin hallintaominaisuudet näkyvät kaikilla sivuilla, kuten tässä ohjeaiheessa on mainittu, **Järjestelmän järjestelmänvalvojat** ja **Tallennetut näkymän järjestelmänvalvojat** voivat hallita näkymiä automaattisesti **Mukautus**-sivun kautta. Erityisesti tällä sivulla on seuraavat osiot ja ominaisuudet: 

- **Julkaistut näkymät** – Tässä osassa luetellaan kaikki organisaatiollesi julkaistut näkymät. Tässä voit julkaista näkymän uudelleen sen jälkeen, kun olet oikaissut näkymän kohteena olevat käyttöoikeusroolit tai yritykset. Voit myös viedä ja poistaa näkymiä sekä peruuttaa niiden julkaisun. Voit luoda näkymästä henkilökohtaisen kopion **Tallenna henkilökohtaiseksi** -toiminnon avulla, jolloin voit päivittää näkymän tai saada paremman käsityksen sen sisällöstä. 
- **Julkaisemattomat näkymät** – Tässä osassa luetellaan kaikki järjestelmän organisaationäkymät, joita ei ole tällä hetkellä julkaistu. Nämä näkymät tulevat useimmiten järjestelmään tuontitoiminnon avulla. Voit julkaista, viedä ja poistaa näitä näkymiä. Versioon 10.0.12 lisätty **Pikajulkaisu**-toiminto mahdollistaa useiden tämän osan näkymien julkaisemisen yhdessä toiminnossa käyttämällä aiemmin luotua käyttöoikeusroolia ja yritysten konfiguraatioita. Voit luoda näkymästä henkilökohtaisia kopioita **Tallenna henkilökohtaisena** -toiminnon avulla, jolloin saada paremman käsityksen niiden sisällöstä.
- **Henkilökohtaiset näkymät** – Tämä osio luetteloi näkymät, jotka ovat järjestelmän käyttäjien luomia. Nyt voit julkaista henkilökohtaisen näkymän organisaatiolle tai kopioida yhden tai useamman näistä näkymistä muille käyttäjille. Voit myös viedä ja poistaa näitä näkymiä tarpeen mukaan.
- **Käyttäjän asetukset** – Valitse käyttäjä, jota haluat tarkastella, tai muokkaa käyttäjän mahdollisuuksia käyttää mukautusta koko järjestelmässä tai tietyillä sivuilla, joilla käyttäjä on vieraillut. Voit tarkastella ja käsitellä käyttäjän mukautuksia järjestelmässä. Voit myös poistaa kaikki käyttäjän omat mukautukset tai palauttaa käyttäjän kuvatekstitoiminnot. Jos kuvatekstitoiminnot palautetaan, uusia ominaisuuksia esittelevät ponnahdusikkunat ja käyttäjän aiemmin hylkäämät ponnahdusikkunat tulevat näkyviin uudelleen, kun kyseinen käyttäjä kohtaa nämä ominaisuudet.
- **Järjestelmäasetukset** – Voit poistaa kaikkien järjestelmän käyttäjien mukautukset käytöstä väliaikaisesti. Tällöin yhdellekään käyttäjälle ei kohdisteta mukautuksia. Kaikki sivut palautetaan oletustiloihinsa. Jos otat mukautukset myöhemmin jälleen käyttöön, kaikkia mukautuksia sovelletaan uudelleen. Voit poistaa tässä välilehdessä kaikkien järjestelmän käyttäjien mukautukset myös pysyvästi. Poistettuja mukautuksia ei voi palauttaa. Varmista tämän vuoksi ennen tämän tehtävän suorittamista, että olet vienyt kaikki ne mukautukset, jotka ehkä tarvitset myöhemmin.

Käyttäjät, joilla on käytössään **Mukauttaminen**-sivu, voivat myös tuoda henkilökohtaisia tai organisaationäkymiä toimintoruudun **Tuo näkymiä** -painikkeen avulla. Organisaationäkymissä voidaan valita **Julkaise heti**, jolloin näkymät ovat käyttäjien käytettävissä ilman muuta julkaisemista.

## <a name="known-issues"></a>Tunnetut ongelmat

Lisätietoja tunnetuista ongelmista ja tallennetuista näkymistä on kohdassa [Tallennettuja näkymiä täysimääräisesti hyödyntävien lomakkeiden luominen](../../dev-itpro/user-interface/understanding-saved-views.md).

## <a name="frequently-asked-questions"></a>Usein kysytyt kysymykset

### <a name="how-do-i-enable-saved-views-in-my-environment"></a>Miten voin ottaa tallennetut näkymät käyttöön omassa ympäristössäni?

> [!NOTE]
> **Tallennetut näkymät** -toiminto edellyttää, että mukautusjärjestelmä Finance and Operationsissa otetaan käyttöön. Jos mukauttaminen on poistettu käytöstä koko ympäristössä, näkymät poistetaan käytöstä, vaikka noudattaisit alla mainittuja vaiheita. 

**Tallennetut näkymät** -toiminto voidaan ottaa käyttöön ja poistaa käytöstä ominaisuuksien hallinnassa kaikissa ympäristöissä. Kun toiminto on otettu käyttöön, tallennetut näkyvät ovat käytössä kaikissa seuraavissa käyttäjäistunnoissa.

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

Jos sivuilla on pienet näkymävalitsimet (vain mukautukset voidaan tallentaa näkymään), samat tiedot tulevat näkyviin aina, kun käyt sivulla. 

Jos sivuilla on suuret näkymävalitsimet (mukautukset ja kyselyt voidaan tallentaa näkymään), näet ensisijaisesti tiedot, jotka on linkitetty oletusnäkymään liittyvään kyselyyn. Seuraavat kaksi ovat pääpoikkeuksia:

- Jos siirryt ruudusta sivulle, ruudun kysely suoritetaan riippumatta oletusnäkymään liittyvästä kyselystä. Jos olet luonut tämän ruudun näkymien käyttöönoton jälkeen, ruudun valinta avaa sivun, joka sisältää kyseiseen ruutuun liitetyn näkymän.
- Jos siirryt sivulle ja aloituskohdassa on kysely, alkuperäinen kysely suoritetaan alkuperäisen oletusnäkymän kyselyn sijaan. Sinun tulisi varoa, kun saat tämän ilmoituksen, kun näkymä latautuu. Voit myös vahvistaa sen siirtymällä tähän näkymään sivun latautuessa, sillä sen pitäisi mahdollistaa näkymäkyselyn suorittaminen riippumatta.

### <a name="why-is-a-view-that-was-published-for-a-specific-legal-entity-visible-in-all-legal-entities"></a>Miksi tietylle yritykselle julkaistu näkymää näkyy kaikissa yrityksissä?

Jos näkymä julkaistaan tietyssä yrityksessä mutta kyseistä näkymää ei julkaista oletusnäkymänä, tulos on seuraavanlainen:

- Jos vain **Tallennetut näkymät** -perusominaisuus otetaan käyttöön, käyttäjän sivun näkymänvalitsin näyttää näkymän vain määritetyissä yrityksissä. Sen jälkeen kun näkymä on kuitenkin ladattu ensimmäisen kerran, se näkyy aina sivun näkymävalitsimessa riippumatta siitä, mikä yritys on kyseessä. Tämä toiminta johtuu siitä, että käyttäjät saaman oman kopion julkaistusta näkymästä, kun se ladataan, ja omat näkymät ovat yleisiä.
- **Version 10.0.21 tai uudempi:** Jos **Tallennettujen näkyvien parannettu yritystuki** -ominaisuus on otettu käyttöön, näkymänvalitsin näyttää näkymän aina vain määritetyille yrityksille. Tämä toiminta johtuu siitä, että näkymät (mukaan lukien omat näkymät) voidaan linkittää tiettyihin yrityksiin.

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
