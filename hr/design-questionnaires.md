---
title: Lomakkeen suunnitteleminen
description: "Tässä aiheessa kuvataan kyselylomakkeen luontiprosessia. Ensimmäinen vaihe kyselylomakkeen suunnittelu. Kyselylomakkeen suunnittelu sisältää kysymysten ja vastausten kirjoittamisen lisäksi myös vastausten tallentamisen ja vastausten välillä sarkaimella siirtymisen mahdollistavan rakenteen luomisen."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: KCMCollectionType, KMAnswerCollection, KMCollection
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 17341
ms.assetid: b27e2f12-c7a0-4a54-b8d8-17819f8a1c72
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 0cac68f90f724777cfe8c3b7ac742d94b34ecd6b
ms.contentlocale: fi-fi
ms.lasthandoff: 05/25/2017


---

# Lomakkeen suunnitteleminen
<a id="design-a-questionnaire" class="xliff"></a>

[!include[banner](includes/banner.md)]


Tässä aiheessa kuvataan kyselylomakkeen luontiprosessia. Ensimmäinen vaihe kyselylomakkeen suunnittelu. Kyselylomakkeen suunnittelu sisältää kysymysten ja vastausten kirjoittamisen lisäksi myös vastausten tallentamisen ja vastausten välillä sarkaimella siirtymisen mahdollistavan rakenteen luomisen. 

Huolellisesti suunnittelu kyselylomake voi parantaa keräämiesi tietojen laatua. Huolellisen suunnittelun avulla voit valita kyselylomakkeeseen kulloinkin sopivat vaihtoehdot. Seuraavat seikat auttavat tehokkaan kyselylomakkeen suunnittelemisessa:

-   Määritä kyselylomakkeen tarkoitus selvästi, jolloin voit varmistaa, että kysymykset tukevat sitä.
-   Määritä yksittäinen henkilö tai henkilöryhmä, jonka haluat täyttävän kyselylomakkeen.
-   Tee kyselylomakkeessa näkyvät kysymykset ja sisällytä mahdolliset vastausvaihtoehdot.
-   Varmista, että kyselylomake on looginen. Näin vastaajien mielenkiinto sitä kohtaan säilyy.
-   Järjestä kysymykset ja vastaukset vastaajille näytettävään järjestykseen.
-   Päätä, miten tulokset arvioidaan, jos arviointi suoritetaan.
-   Päätä, tarvitaanko kyselylomakkeessa lisätoimintoja. Voit esimerkiksi määrittää, luokitellaanko tulokset ja tulosten luokittelutavan, mahdollisen aikarajan tai sen, ovatko kaikki kysymykset pakollisia.

Tämän tilauksen suunnitteluvaihe sisältää neljä tehtäväluokkaa.

1.  Määritä tarvittavat edellytykset.
2.  Määritä mahdolliset vastausryhmät ja vastaukset.
3.  Määritä kysymykset ja niiden liitokset vastausryhmiin.
4.  Määritä kyselylomake ja liitä siihen kysymykset.

## Edellytykset
<a id="prerequisites" class="xliff"></a>
Joidenkin edellytysten on täytyttävä, ennen kuin kyselylomakkeet, vastaukset ja kysymykset voidaan luoda. Kaikkia toimintoja voi kuitenkin käyttää, vaikka kaikki edellytykset eivät täyttyisikään.

### Vaadittu
<a id="required" class="xliff"></a>

| Edellytys        | Kuvaus                |
|---------------------|----------------------------|
| Kyselylomaketyypit | Luokittele kyselylomakkeet. |
| Kysymystyypit      | Luokittele kysymykset.      |

### Valinnainen
<a id="optional" class="xliff"></a>

| Edellytys             | Kuvaus                                                    |
|--------------------------|----------------------------------------------------------------|
| Kyselylomakeparametrit | Muokkaa perusohjausobjekteja ja kyselylomakkeen oletusasetuksia. |

### Kyselylomaketyypit
<a id="questionnaire-types" class="xliff"></a>

Kyselylomakkeen tyypit ovat pakollisia. Ne on liitettävä kyselylomakkeen luomisen yhteydessä. Kyselylomakkeen tyypit auttavat kyselylomakkeiden hallinnassa ja luokittelussa. Kyselylomaketyyppien avulla voit luokitella kyselylomakkeita ja erottaa ne toisistaan. Jos esimerkiksi valittavissa on useita kyselylomakkeita, tietyn kyselylomakkeen löytäminen helpottuu, kun suodatat niitä tyypin mukaan. Seuraavassa on joitakin esimerkkejä kyselylomaketyypeistä:

-   henkilöstön kehitys
-   asiakastutkimukset
-   Tarkistus

### Kysymystyypit
<a id="question-types" class="xliff"></a>

Kysymystyypit ovat pakollisia. Ne on liitettävä kysymykseen luomisen yhteydessä. 

Kysymystyyppien avulla voit luokitella kysymyksiä raportointia varten. Kysymystyyppien avulla on myös helppo etsiä kysymyksiä, koska voit käyttää tyyppejä suodattimina **Kysymykset**-sivulla. Seuraavassa on joitakin esimerkkejä kysymystyypeistä:

-   henkilöstöhallinto
-   liiketoiminnan hallinta
-   kurssin arviointi.

### Kyselylomakeparametrit
<a id="questionnaire-parameters" class="xliff"></a>

Kyselylomakeparametrit ovat valinnaisia. Organisaation vaatimuksista riippuen ne eivät välttämättä ole käytössä. 

Kyselylomakeparametrit määrittävät anonyymin tilan, numerosarjan koodit ja kyselylomakkeen viitetyypit. Kun organisaatio jakelee kyselylomakkeen, anonyymisti vastaamisen vaihtoehtoon tulee kiinnittää huomiota. 

Numerosarjan koodeja käytetään kysymysten ja vastausten järjestämisessä. Arvot liitetään automaattisesti nimikkeisiin näiden numerosarjan koodien perusteella. 

Kaikki parametrit tulee määritettävä, ennen kuin tietoja aletaan luoda. Voit muokata kyselylomakeparametrien asetuksia milloin tahansa.

## Kyselylomakkeen osat
<a id="questionnaire-components" class="xliff"></a>
Kyselylomake muodostuu kolmesta pääelementistä: vastausryhmistä, jotka sisältävät monivalintakysymysten vastaukset, kysymyksistä ja itse kyselylomakkeesta. Voit halutessasi ryhmitellä kyselylomakkeen kysymykset tulosryhmiin. Tulosryhmien avulla voit luokitella kysymykset ja tehdä kyselylomakkeesta lisäanalyysin. 

[![QuestionnaireComponents](./media/questionnairecomponents-1024x615.png)](./media/questionnairecomponents.png)

### Vastausryhmät ja vastaukset
<a id="answer-groups-and-answers" class="xliff"></a>

Vastaajat voivat vastata kysymykseen kahdella eri tavalla kysymyksen aiheen mukaan.

-   Avointen kysymysten vastausten ei tarvitse olla tietyn muotoisia. Vastaajat voivat kirjoittaa vastauksen tekstinä, numerona, päivämääränä tai aikana. Kysymykset edellyttävät vastaajilta yleensä subjektiivisia tietoja kuten mielipiteitä, kuvauksia, arviointeja tai arvioita.
-   Monivalintakysymykset edellyttävät, että vastaaja valitsee vastauksen mahdollisten oikeiden vastausten luettelosta.

Voit määrittää monivalintakysymysten mahdollisten vastausten luettelon luomalla vastaukset **Vastausryhmät**-sivulla. 

Vastausryhmät ja vastaukset ovat komponentteja, jotka muodostavat kysymysten luomisessa käytettävien tietojen päätekstiosan. Kun olet luonut vastausryhmän, voit liittää sen kysymykseen **Kysymykset**-sivun **Vastausryhmä**-kentässä. 

Vastausryhmää voit käyttää useassa saman kyselylomakkeen kysymyksessä tai useassa eri kyselylomakkeessa. 

>**Huomautus** Tietojen arviointi vaikeutuu, jos täytetyissä kysymyslomakkeissa käytettyjen vastausryhmien vastausten tekstiä muokataan, eivätkä kyselylomakkeen tulokset välttämättä ole enää voimassa. Jos vastausryhmää on muutettava, kannattaa ehkä luoda uusi vastausryhmä aiemmin luodun ryhmän muuttamisen sijaan. Kysymykseen tai vastaukseen liitettyjä vastausryhmiä tai vastausryhmiä, joihin on vastattu, ei voi poistaa.

### Kysymykset
<a id="questions" class="xliff"></a>

Kyselylomakkeessa on oltava kysymyksiä. Kysymykset voivat olla joko avoimia tai rajattuja.

-   Avointen kysymysten vastauksia ei ohjata, vaan vastaajat voivat kirjoittaa vastauksensa.
-   Monivalintakysymykset vaativat luettelon ennalta määritetyistä vastausvaihtoehdoista. Kysymysten rakenne voidaan määrittää niin, että vastaaja voi valita useita vastauksia. Kysymykset tulisi suunnitella siten, että ne houkuttelevat vastaajan antamaan yksityiskohtaisia tietoja. Kysymykset tulee linkittää vastausryhmään, joka sisältää kunkin monivalintakysymyksen vastausvaihtoehdot. 
    >**Huomautus** Vastausryhmät ja vastaukset on luotava ennen monivalintakysymysten määrittämistä.

Kysymykset voidaan järjestää ehdolliseen kysymyshierarkiaan niin, että toissijaiset kysymykset riippuvat edellisen kysymyksen kohdalla valitusta vastauksesta. Voit kirjoittaa kysymykset ensin ja järjestää ne hierarkiaan myöhemmin.

## Kyselylomakkeiden määrittäminen
<a id="setting-up-questionnaires" class="xliff"></a>
>**Huomautus**
>  Ennen kyselylomakkeen määrittämistä on määritettävä vastaukset, kysymykset ja edellytykset. 

Voit määrittää kullekin kyselylomakkeelle seuraavat tiedot:

-   pakollisiin kysymyksiin vastaamisen kokonaisaika tai aikaraja
-   kaikkien kysymysten pakollisuus
-   lasketaanko kyselylomakkeen pisteiden enimmäismäärä
-   tulosten luokittelutapa
-   kyselylomakkeen käyttäminen rajoitetussa vastaajajoukossa
-   lomakemallin näyttäminen kyselylomakkeen sivujen taustalla
-   lisähuomautusten pakollisuus, kun halutaan selventää kyselylomakkeen tarkoitusta vastaajille
-   kysymysten näyttäminen kiinteässä järjestyksessä tai kysymysten valitseminen poolista satunnaisessa järjestyksessä
-   kysymysten esittäminen vain silloin, kun edelliset vastaukset sisältävät tiettyjä elementtejä.

### Kyselylomakkeen määrittäminen
<a id="set-up-a-questionnaire" class="xliff"></a>

Ensisijainen sivu, jota käytetään kyselylomakkeen määrittämisessä **Kyselylomakkeet**-sivulla. Voit määrittää kyselylomakkeen suorittamalla seuraavat tehtävät järjestyksessä:

1.  Luo kyselylomake.
2.  Liitä kyselylomakkeeseen kysymykset näiden vaiheiden avulla:
    -   Jos käytössä ovat tulosryhmät, voit liittää kysymykset kyselylomakkeeseen niiden avulla. Määritä ensin kyselylomakkeen tulosryhmät ja lisää sitten tulosryhmiin kysymykset.
    -   Jos tulosryhmät eivät ole käytössä, voit liittää kysymykset suoraan kyselylomakkeeseen.

3.  Määritä ehdollinen kysymyshierarkia, jos se vaaditaan.
4.  Testaa kyselylomake.

Valitse **Kyselylomakkeet**-sivulla **Vahvista** testataksesi, onko kyselylomake koottu oikein. Kyselylomake kannattaa täyttää ja testata itse ennen sen lähettämistä.

### Kyselylomakkeen muokkaaminen
<a id="modify-a-questionnaire" class="xliff"></a>

Voit toteuttaa seuraavat tehtävät **Kyselylomakkeet**-sivulla:

-   muokata kyselylomakkeen tietoja, kuten tulosryhmiä ja kysymyksiä
-   poistaa ja lisätä kysymyksiä
-   muuttaa tulosryhmiä ja järjestysnumeroa. 

>**Varoitus** Ole tarkkana, kun teet muutoksia kyselylomakkeisiin, joihin on jo vastattu. Muutosten tekeminen voi vähentää tilastojen ja arviointien tarkkuutta. Vastatun kysymyksen muuttamisen sijaan kannattaa luoda uusi kysymys.

Seuraavia kysymystyyppejä ei voi poistaa kyselylomakkeesta:

-   kyselylomakkeeseen liitetyt kysymykset
-   kysymykset, joihin on jo vastattu ja jotka näkyvät sen vuoksi **Vastaukset**-valintaikkunassa.

### Tulosryhmät
<a id="result-groups" class="xliff"></a>

Tulosryhmiä ei ole pakko käyttää, kun kyselylomakkeeseen liitetään kysymyksiä. 

Tulosryhmää käytetään pisteiden laskemisessa ja kyselylomakkeen tulosten luokittelussa. Jos tulosryhmät ovat käytössä, voit suorittaa seuraavat tehtävät:

-   kyselylomakkeen tulosten arvioiminen pistetilastotietojen perusteella
-   vastaajan pisteiden arvioiminen jokaisessa määritetyssä tulosryhmässä.
-   Voit luoda kustakin tulosryhmästä tilastotietoja, jos haluat analysoida tuloksia.
-   Tulosta raportti, jossa näkyvät kunkin tulosryhmän tulokset sekä valinnaiset pisteet/tekstit, jotka perustuvat samassa tulosryhmässä saatuihin pisteisiin.

> **Huomautus**
>  Seuraavat tehtävät on suoritettava ennen tulosryhmien määrittämistä:

-   Määritä monivalintakysymykset. Monivalintakysymysten **Kysymykset**-sivun syöttötyypiksi on määritettävä **valintaruutu**, **vaihtoehtopainike** tai **yhdistelmäruutu**.
-   Määritä pisteet vastauksille, jotka kuuluvat kuhunkin kysymykseen liitettyyn vastausryhmään.
-   Määritä kyselylomake.

Voit liittää kyselylomakkeeseen kysymykset tulosryhmien avulla määrittämällä ensin kyselylomakkeen tulosryhmät ja lisäämällä sitten tulosryhmiin kysymykset. Jos et käytä tulosryhmiä, voit liittää kysymykset suoraan kyselylomakkeeseen. 

Voit määrittää useita tulosryhmiä, kun haluat arvioida vastaajien kussakin luokassa saamat pisteet. Kun kyselylomake on valmis, näkyviin tulevat kussakin tulosryhmässä saadut pisteet. 

> **Vihje**
>  Voit arvioida kyselylomakkeen käyttämällä pisteitä ilman erillisiä luokkia, kun lisäät kaikki kysymykset yhteen tulosryhmään. 

Voit myös määrittää jokaiselle tulosryhmälle vähintään yhden pisteisiin perustuvan sanoman, joka lähetetään vastaajille, kun he ovat täyttäneet kyselylomakkeen. Näyttöön tuleva teksti voi vaihdella sen mukaan, mitkä pisteet vastaaja on saanut tulosryhmässä. Voit käyttää pisteisiin perustuvia sanomia, kun määrität pistevälit ja kunkin pistevälin kuvauksen. Kun vastaaja saa tiettyyn pisteväliin kuuluvan tuloksen, kyseiseen pisteväliin liittyvä teksti näkyy tulosraportissa. 

Koska tulosryhmä liittyy pisteisiin, jotka on liitetty kyselylomakkeen tiettyihin joukkoihin, voit käyttää vain tiettyä kyselylomakkeen tulosjoukkoa.

#### Esimerkki: Pisteiden tai tekstien luominen tulosryhmää 3 varten
<a id="example-pointstexts-for-result-group-3" class="xliff"></a>

Käytössä on johtamistaitotestin kyselylomake, jossa on 15 kysymystä kolmessa eri luokassa. Luo kolme tulosryhmää ja lisää kuhunkin tulosryhmään viisi kysymystä. Kolmen ryhmän pisteet lasketaan yhteen. Kolme tulosryhmää ovat seuraavat:

-   luovat taidot
-   johtamistaidot
-   tekniset taidot.

Kun käytössä ovat pisteisiin perustuvat viestit, voit määrittää jokaiselle tulosryhmälle tekstivälit. Jokaiseen kysymykseen liitetään kaksi pistettä. Tämän vuoksi kunkin tulosryhmän enimmäispistemäärä on 10 

Seuraavassa taulussa näkyvät johtamistaidot-tulosryhmälle määritetyt pisteisiin perustuvat sanomat.

| Pisteväli | Teksti                                       |
|----------------|--------------------------------------------|
| 1−3         | Sinulla on keskinkertaiset johtamistaidot.     |
| 4−7         | Sinulla on hyvät johtamistaidot.        |
| 8−10        | Sinulla on loistavat johtamistaidot. |

Voit määrittää pistevälejä ja tekstejä jokaiselle kyselylomakkeen tulosryhmälle. Kunkin vastaajan tuloksia vastaava teksti näkyy tulosryhmän kohdalla. 

> **Huomautus**
>  Voit muuttaa välejä ja tekstejä. Jos kyselylomake on täytetty, muutokset voivat aiheuttaa eroja edellisten ja uusien tulosraporttien välillä.

### Ehdolliset kysymyshierarkiat
<a id="conditional-question-hierarchies" class="xliff"></a>

Ehdolliset kysymyshierarkiat ovat valinnaisia kyselylomakkeen määrittämisen yhteydessä. 

> **Huomautus**
>  Ennen kuin voit määrittää ehdollisen kysymyshierarkian, kyselylomakkeeseen täytyy liittää kysymykset, joille on liitetty kysymysryhmät. 

Jos käytät ehdollisia kysymyksiä kyselylomakkeen kysymyshierarkian luomiseen, voit muodostaa järjestyksen, jossa kysymykset esitetään vastaajan kysymykseen valitseman vastauksen perusteella. Kun kysymysten järjestys perustuu vastaajan vastaukseen, voit muokata kyselylomaketta samalla, kun vastaaja täyttää sitä.

#### Esimerkkejä
<a id="examples" class="xliff"></a>

Yritys tarjoaa asiakkailleen sekä nimikkeitä että palveluita. Tällaisissa tapauksissa käy usein niin, että asiakkaat saattavat ostaa pelkästään tuotteita tai palveluita tai molempia. Ku yritys siis lähettää asiakastyytyväisyyskyselyn, kyselylomakkeeseen lisätään ehdollinen rakenne, jolloin vain palveluita ostaneiden asiakkaiden ei tarvitse vastata nimikkeitä koskeviin kysymyksiin. 

Vaihtoehtoisesti kyselylomakkeen voi määrittää niin, että jos vastaaja valitsee kysymykseen 1 vastaksen A, seuraavaksi esitetään kysymys 2. Mutta jos vastaaja valitsee kysymykseen 1 vastauksen B, seuraavaksi esitetään kysymys 5.

Lisätietoja
<a id="see-also" class="xliff"></a>
--------

[Kyselylomakkeiden käyttäminen](questionnaires.md)

[Kyselylomakkeiden jakelu ja täyttäminen](distribute-questionnaires.md)

[Kyselylomakkeen tulosten tarkasteleminen ja arvioiminen](evaluate-questionnaire-results.md)




