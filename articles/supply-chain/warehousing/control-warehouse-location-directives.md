---
title: Varastotyön valvonta työmallien ja sijaintidirektiivien avulla
description: Tässä ohjeaiheessa kuvataan, miten työmalleja ja sijaintidirektiivejä käytetään määrittämään, miten ja missä työ suoritetaan varastossa.
author: perlynne
manager: tfehr
ms.date: 02/05/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSLocDirFailure, WHSLocDirHint, WHSLocDirTable, WHSLocDirTableUOM, WHSRFMenuItem, WHSWork, WHSWorkClass, WHSWorkPool, WHSWorkTemplateTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 72921
ms.assetid: 377ab8af-5b0c-4b5e-a387-06ac1e1820c0
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: aae57af04be8bcc6da2e5635b5ffa96d9fac147c
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/02/2020
ms.locfileid: "3205733"
---
# <a name="control-warehouse-work-by-using-work-templates-and-location-directives"></a>Varastotyön valvonta työmallien ja sijaintidirektiivien avulla

[!include [banner](../includes/banner.md)]

Tässä ohjeaiheessa kuvataan, miten työmalleja ja sijaintidirektiivejä käytetään määrittämään, miten ja missä työ suoritetaan varastossa.

Ohjeet, jotka varastotyöntekijät saavat mobiililaitteessa, määräytyvät Dynamics 365 Supply Chain Managementissa määrittämiesi työmallien mukaisesti. Työmallit määrittävät, miten kunkin varastoprosessin työt suoritetaan. Linkittämällä sijaintidirektiivin työmalleihin, voit varmistaa, että työ tapahtuu tietyillä fyysisillä varastojen alueilla.

## <a name="work-templates"></a>Työmallit
**Työmallit**-sivun avulla voit määrittää työtoiminnot, jotka on suoritettava varastossa. Yleensä varastotyötoiminnot kostuvat toimintopareista: varaston työntekijä keräilee käsillä olevan varaston yhdessä sijainnissa ja asettaa sitten keräillyt varastotuotteet toiseen paikkaan. 

Työmallit koostuvat otsikosta ja siihen liittyvistä riveistä. Jokainen työmalli on tarkoitettu määrätylle *työtilaustyypille*. Monet työtilaustyypit on liitetty lähdeasiakirjoihin, kuten osto- tai myyntitilauksiin. Muut työtilaustyypit kuitenkin edustavat erillisiä varastoprosesseja kuten inventointia. *työpoolin tunnuksen* avulla voit järjestää työsi ryhmiin. 

Työotsikon määrityksen asetuksia voidaan käyttää määrittämään, milloin uusi työkappale tulisi luoda. Voit esimerkiksi määrittää keräilyrivien maksimimäärän ja odotetun keräilyajan maksimimäärän. Tämän jälkeen, jos myyntitilauksen keräilyprosessin työ ylittää jommankumman näistä arvoista, työ jaetaan kahdeksi työkappaleeksi. 

Työrivit edustavat fyysisiä tehtäviä, jotka vaaditaan työn käsittelemiseen. Esimerkiksi lähtevässä varastoprosessissa saattaa olla työrivi varastossa olevien nimikkeiden keräilyyn ja toinen rivi näiden nimikkeiden sijoittamiseen vaiheiden alueelle. Tämän jälkeen voi olla lisärivi nimikkeiden keräilyyn vaiheiden alueelta ja toinen rivi näiden nimikkeiden poispanoon kuorma-autoon osana lastausprosessia. Voit määrittää *direktiivikoodin* työmallirivillä. Direktiivikoodi linkitetään sijaintidirektiiviin ja se auttaa siten varmistamaan, että varastotyö käsitellään varaston oikeassa sijainnissa. 

Voit määrittää kyselyn ohjaamaan, milloin määrättyä työmallia käytetään. Voit esimerkiksi määrittää rajoituksen siten, että määrättyä mallia voidaan käyttää työhön vain määrätyssä varastossa. Vaihtoehtoisesti sinulla voi olla useita malleja, joita käytetään työn luomiseen lähtevän myyntitilauksen käsittelyyn riippuen myynnin alkuperästä. Järjestelmä käyttää **järjestysnumero**-kenttää määrittämään käytettävissä olevien työmallien arviointijärjestyksen. Siksi, jos sinulla on erityinen kysely tietylle työmallille, anna sille alhainen järjestysnumero. Tämä kysely arvioidaan sitten ennen muita, yleisempiä kyselyitä. 

Voit lopettaa tai keskeyttää työprosessin työrivin **Pysäytä työ** -asetuksen avulla. Siinä tapauksessa työn suorittavaa työntekijää ei pyydetä suorittamaan seuraavaa työrivin vaihetta. Siirtyäkseen seuraavaan vaiheeseen, työntekijän on valittava työ uudelleen. Voit myös erotella tehtävät työkappaleen sisällä käyttämällä eri *työluokan tunnusta* työmallin riveillä.

## <a name="location-directives"></a>Sijaintidirektiivit
Sijaintidirektiivit ovat sääntöjä, jotka auttavat tunnistamaan keräily- ja poispanosijainnit varaston siirrossa. Esimerkiksi myyntitilaustapahtumassa sijaintidirektiivi määrittää, mistä nimikkeet kerätään ja minne kerätyt nimikkeet sijoitetaan. Sijaintidirektiivit koostuvat otsikosta ja siihen liittyvistä riveistä. Luot ne **Sijaintidirektiivi**-sivulla. 

Otsikossa jokaisen direktiivin on oltava liitettynä *työtilaustyypille*. Se määrittää varastotapahtuman tyypin, johon direktiiviä tullaan käyttämään, kuten myyntitilaukset, täydennys, tai raaka-aineiden keräily. *työtyyppi* määrittää, käytetäänkö sijaintidirektiiviä keräily- tai poispanotyöhön, tai johonkin muuhun varastoprosessiin kuten laskentaan tai varaston tilan muutoksiin. Sinun on myös määritettävä *toimipaikka* ja *varasto*. Otsikossa määrittämääsi *direktiivikoodia* voidaan käyttää linkittämään sijaintidirektiivin yhteen tai useampaan työmalliin. 

Mitä tulee työmalleihin, voit määrittää kyselyn tunnistamaan, milloin määrättyä sijaintimallia käytetään. Voit esimerkiksi määrittää, että silloin, kun sähköinen kaupankäynti on myyntitilauksen alkuperä, varasto on keräiltävä määrätyltä varaston alueelta. Järjestelmä käyttää **järjestysnumero**-kenttää määrittämään käytettävissä olevien sijaintidirektiivien arviointijärjestyksen. 

Sijaintidirektiivin rivit asettavat lisärajoituksia sijainnin löytämissääntöjen käytölle. Voit määritellä vähimmäis- ja enimmäismäärät, joihin direktiiviä tulisi soveltaa ja voit määrittää, että direktiivi koskee määrättyä varastoyksikköä. Esimerkiksi jos mittayksikkö on kuormalava, kuormalavojen nimikkeet voidaan asettaa tiettyyn paikkaan. Voit myös määrittää, voidaanko määrä jakaa eri sijainteihin. Samoin kuin sijaintidirektiivin otsikolla, kullakin sijaintidirektiivin rivillä on järjestysnumero, joka määrittää näiden rivien arviointijärjestyksen. 

Sijaintidirektiiveillä on yksi yksityiskohtien taso lisää: *sijaintidirektiivin toiminnot*. Voit määrittää useita sijaintidirektiivin toimintoja kullekin riville. Jälleen kerran järjestysnumeroa käytetään määrittämään järjestys, jossa arvioidaan toimia. Tällä tasolla voit määrittää kyselyn määrittääksesi, miten löydetään paras sijainti varastossa. Voit myös käyttää esimääritettyjä **Strategia**-asetuksia parhaan sijainnin löytämiseen.

## <a name="location-directives-configuration-details"></a>Sijantidirektiivien konfiguraatiotiedot 

 ### <a name="sequence-number"></a>Järjestysnumero
 
Tämä numero osoittaa järjestyksen, jonka mukaan valitun tilaustyypin sijaintidirektiivi käsitellään. Sitä voi muuttaa valikon **Siirrä ylös**- ja **Siirrä alas** -painikkeiden avulla.
 
 ### <a name="work-type"></a>Työtyyppi
 
Tämä on suoritettavan työn tyyppi. Käytettävissä olevan työn tyyppi perustuu varastotapahtuman tyyppiin, jonka olet valinnut **Työtilaustyyppi**-kentässä.
-   **Aseta** – **Aseta**-vaihetta vastaava työtyyppi tarkoittaa, että sijaintidirektiivi yrittää löytää parhaimman sijainnin järjestelmään saapuvan varaston sijoittamiseksi tai paikantaa sen joko vastaanotosta, tuotannosta tai varastomukautuksista. Sitä voidaan käyttää myös määrittämään Aseta-arvo välikaiseen sijaintiin tai lopulliseen lähettäminen lastausovelta -sijaintiin.
-   **Kerää** – **Kerää**-vaihetta vastaava työtyyppi tarkoittaa, että varasto yrittää löytää parhaimman sijainnin varaston varaamiseksi fyysisesti (luo työ). Kerää-vaihe voidaan suorittaa loppuun (Kerää-työlinja voidaan sulkea), vaikka työ ei ole valmis. Käyttäjä voi suorittaa loppuun fyysisen keräämisen eli Kerää-vaiheen. Käyttäjä voi sitten peruuttaa työn mobiililaitteella ja suorittaa työn loppuun myöhemmin. Työn otsikko kuitenkin suljetaan, kun lopullinen Aseta-vaihe on valmis. 
-   **Inventointi, oikaisut, mukautus, varaston tilan muutos, rekisterikilven luonti, tulostus, tilan muutos, pakkaa sisäkkäisiin rekisterikilpiin** – Näitä ei voi käyttää missään sijaintidirektiivin määrityksessä. Tämä on valintalista, joten työtilaustyyppiin ei ole liitetty mitään suodatusta. 

### <a name="directive-code"></a>Direktiivikoodi

Valitse liitettävän työmallin tai täydennysmallin direktiivin koodi. Voit luoda **Direktiivikoodi**-lomakkeessa uudet koodit, joita voidaan käyttää työmallin, täydennysmallin ja sijaintidirektiivin välisiin yhteyksiin. Tätä voidaan käyttää myös linkin luomiseen työmallin rivin ja sijaintidirektiivin välille (kuten lastausovi tai väliaikainen sijainti).

Huomaa, että jos koodi on määritetty ja työ luodaan, järjestelmä ei hae sijaintidirektiiviä järjestyksen vaan direktiivikoodin mukaan. Tämä tarkoittaa, että voit määrittää tarkemmin, mitä sijaintimallia käytetään työmallin tietyssä vaiheessa, kuten materiaalin väliaikaisessa sijoituksessa. 

### <a name="site"></a>Sivusto

Toimipaikka on pakollinen kenttä, koska sijaintidirektiivi tarvitsee voimassa olevaa toimipistettä ja varastoa. 

### <a name="warehouse"></a>Varasto

Varasto on pakollinen kenttä, koska sijaintidirektiivi tarvitsee voimassa olevaa toimipistettä ja varastoa.

### <a name="multiple-sku"></a>Useita varastointiyksiköitä

Tälla tavoin useita varastointiyksiköitä (SKU) voidaan pitää yhdessä sijainnissa, kuten lastausovella. Jos valitset **Useita varastointiyksiköitä** työssä määritetään Aseta-sijainti (joka on odotettu), mutta se voi käsitellä vain usean nimikkeen Aseta-vaiheita (jos työ sisältää erilaisia kerättäviä ja asetettavia varastointiyksiköitä, ei yhtä varastointiyksikön Aseta-vaihetta). Jos et valitse **Useita varastointiyksiköitä**, Aseta-sijainti määritetään vain, jos Aseta-vaiheessa on vain yhdenlainen varastointiyksikkö. Jotta voit käyttää kumpaakin toimintoa, sinun on määritettävä kaksi riviä, joissa yhdessä on useita varastointiyksiköitä käytössä ja toisessa useita varastointiyksiköitä pois käytöstä. Niillä on oltava sama rakenne ja määritys. Aseta-toimintoja varten sinulla on oltava samanlaiset sijaintidirektiivit, vaikka työn tunnuksessa ei tehdä eroa yhden ja useamman varastointiyksikön välillä. Tarvitset myös määrityksen keräystä varten, jos tilauksessa on useampi kuin yksi nimike.

### <a name="sequence-number"></a>Järjestysnumero

Kirjoita järjestys, jonka mukaan valitun työtyypin sijaintidirektiivin rivi käsitellään. Voit myös muokata järjestystä tarvittaessa **Siirrä ylöspäin**- ja **Siirrä alaspäin** -painikkeen avulla.

### <a name="fromto-quantity"></a>Alku-/loppumäärä

Tämän avulla voit määrittää määräalueen, kun valitset keskiruudukon järjestyksen. Voit määrittää alku-/loppualueen määrälle vastaavassa yksikössä.

### <a name="unit"></a>Yksikkö

Voit määritellä vähimmäis- ja enimmäismäärät, joihin direktiiviä tulisi soveltaa ja voit määrittää, että direktiivi koskee määrättyä varastoyksikköä. Rivin yksikkökenttää käytetään vain määrän arviointiin.

Sijaintidirektiivin soveltamisen aiheellisuus tarkistetaan sijaintidirektiivin rivillä määritetyn vastaavan yksikön määrän mukaan. Aina kun direktiivisijainnin rivi saavutetaan, järjestelmä yrittää muuntaa kysynnän yksikön rivillä määritetyksi yksiköksi. Jos UOM-muuntoa ei ole olemassa, se jatkaa seuraavalle riville. 

### <a name="locate-quantity"></a>Etsi määrä

Tätä vaihtoehtoa käytetään vain määrän asettamiseen/paikantamiseen varastossa. Se on tarkoitettu vain Aseta-työtyypille. Kelvollisia arvoja ovat:

-   **Rekisterikilpien määrä** – Kun arvioit sitä, onko määrä alku- ja loppumääräalueella, käytä saadussa rekisterikilvessä olevaa määrää.
-   **Määrä, jolle on määrätty yksikkö** – Kun arvioit sitä, onko määrä alku- ja loppumääräalueella, käytä erityisen tapahtuman aikana määrää, jolle on määrätty yksikkö.
-   **Jäljellä oleva määrä** – Kun arvioit sitä, onko määrä alku- ja loppumääräalueella, käytä vastaanotettavaa jäljellä olevaa määrää parhaillaan sisään kuitattavan ostotilauksen rivillä.
-   **Odotettu määrä** – Kun arvioit sitä, onko määrä alku- ja loppumääräalueella, käytä ostotilauksen rivin kokonaismäärää riippumatta siitä, mitä on jo vastaanotettu.

### <a name="restrict-by-unit"></a>Rajoita yksikön mukaan

Tälla tavoin sijaintidirektiivin rivi voidaan määrittää tiettyä mittayksikköä tai useita mittayksiköitä varten. Kun varaat määrän ja haluat varata kuormalavoja tietystä sijaintijoukosta, keskiruudukon järjestys rajoittaa tämän tietyn järjestyksen ”PL”-arvoon, jotta kuormalavaa vähäisempi määrä ei valitse järjestystä. Valitse **Rajoita yksikön mukaan** yksiköiden määrittämiseksi. Voit myös rajoittaa rivin useampaan kuin yhteen yksikköön. Tämä toimii vain Kerää-tyyppisten sijaintidirektiivien kanssa. 

### <a name="round-up-to-unit"></a>Kokoa yksikköön

Tämä kenttä toimii yhdessä **Rajoita yksikön mukaan** -kentän kanssa. Jos sijaintidirektiivin rivi **Rajoita yksikön mukaan** määritetään arvoon "laatikko" ja valitset **Pyöristä ylöspäin yksikköön**, direktiivistä luotu työ raaka-aineen keräämistä varten olisi pyöristettävä ylöspäin käsittely-yksikön kerrannaiseen (määritetty **Rajoita yksikön mukaan** -rivillä). Huomaa, että tämä toimii vain raaka-aineen keräämistä varten ja vain Kerää-tyyppisten sijaintidirektiivien kanssa.

### <a name="locate-packing-qty"></a>Etsi pakkausmäärä

Jos pakkausmäärä on määritetty myyntitilauksessa, siirtotilauksessa tai tuotantotilauksessa, tämä rajoittaa järjestelmän valitsemaan vain sijainnit, joissa on pakkausmäärä sijainnissa. Tämä toimii vain Kerää-tyyppisten sijaintidirektiivien kanssa.

### <a name="allow-split"></a>Salli jakaminen

Tämä määrittää, voiko sijaintidirektiivi jakaa vastaanotettavan määrän tai varattavan määrän useisiin varastosijainteihin tai onko koko määrän sijaittava yhdessä sijainnissa tai onko se varattava yhdestä sijainnista työn luomiseksi. 

### <a name="sequence-number"></a>Järjestysnumero

Numero on järjestys, jonka mukaan valitun työtyypin sijaintidirektiivi käsitellään. Voit tarvittaessa muuttaa järjestystä. Käytä järjestysnumeroita kuitenkin varovasti, koska käsittely suoritetaan aina peräkkäin. 

### <a name="name"></a>Nimi

Kirjoita nimi sijaintidirektiivin toiminnolle. Muista määrittää nimi tarkasti.

### <a name="fixed-location-usage"></a>Kiinteän sijainnin käyttö 

-   **Kiinteät ja ei-kiinteät sijainnit** – Sijaintidirektiivi harkitsee kaikkia sijainteja.
-   **Vain kiinteät sijainnit tuotteelle** – Sijaintidirektiivi harkitsee vain kiinteitä sijainteja tuotteille.
-   **Vain kiinteät sijainnit tuotevariantille** – Sijaintidirektiivi harkitsee vain kiinteitä sijainteja tuotevarianteille.

### <a name="allow-negative-inventory"></a>Salli negatiivinen varasto

Valitse tämä vaihtoehto, jos haluat sallia negatiivisen varaston määritetyssä varastosijainnissa sijaintidirektiiveissä. 

### <a name="batch-enabled"></a>Erä käytössä 

Valitse tämä vaihtoehto, jos haluat käyttää erästrategioita nimikkeille, joille erä on käytettävissä. Jos rivi saavutetaan, kun **Erä käytössä** on määritetty erään kuulumattomalle nimikkeelle, prosessi jatkuu seuraavalla toimintorivillä. 

### <a name="strategy"></a>Strategia

-   **Konsolidoi** – Tätä strategiaa käytetään tietyssä sijainnissa olevien nimikkeiden konsolidoimiseen, kun vastaavat nimikkeet ovat jo käytettävissä.. Tämä toimii vain Aseta-tyyppiselle sijaintidirektiiville. Aseta-tyypin yleinen määritys on, että konsolidointi suoritetaan ensimmäisellä toimintorivillä ja seuraavalla toimintorivillä konsolidointia ei suoriteta. Tuotteiden konsolidointi tehostaa keräystä vastaisuudessa.
-   **Täsmäytä pakkausmäärä** – Tämä strategiaa etsii sijainnin, jossa on tarkan vaaditun määrän sisältävä rekisterikilpi. Sitä ei voi käyttää sellaisten sijaintien osalta, jotka eivät ole rekisterikilpihallittuja. Tämä strategia toimii vain Kerää-tyyppiselle sijaintidirektiiville.
-   **FEFO-erävaraus** – Tätä strategiaa käytetään, kun varasto paikannetaan käyttämällä erän vanhentumispäivää ja se kohdistetaan erävaraukseen. Voit käyttää tämän strategian vain eränimikkeissä. Tämä toimii vain Kerää-tyyppiselle sijaintidirektiiville. 
-   **Pyöristä kokonaiseen rekisterikilpeen** – Tätä strategiaa käytetään varastomäärän pyöristämiseen ylöspäin vastaamaan kerättäviin nimikkeisiin määritettyä rekisterikilven määrää. Tätä strategiaa voi käyttää vain Kerää-tyyppisen sijaintidirektiivin täydennystyypille. 
-   **Tyhjä sijainti ilman saapuvia töitä** – Tätä strategiaa käytetään tyhjien sijaintien paikantamiseen. Sijainnin katsotaan olevan tyhjä, jos sillä ei ole fyysistä varastoa, eikä odotettuja saapuvia töitä. Tätä strategiaa käytetään vain Aseta-tyyppiselle sijaintidirektiiville. 

### <a name="example-of-the-use-of-location-directives"></a>Esimerkki sijaintidirektiivien käytöstä.

Tarkastele tätä esimerkkiä varten ostotilausprosessia, jossa sijaintidirektiivin on löydettävä varastosta vapaata kapasiteettia varastonimikkeille, jotka on juuri rekisteröity vastaanottolaiturilla. Sinun on ensin löydettävä varastosta vapaata kapasiteettia konsolidoimalla nykyiseen käsillä olevaan varastoon. Jos konsolidointi ei ole mahdollista, sinun on löydettävä tyhjä sijainti. 

Tätä skenaariota varten sinun on määritettävä kaksi sijaintidirektiivitoimintoa. Sarjan ensimmäisen toiminnon on käytettävä **Konsolidointi**-strategiaa, ja toisen tulisi käyttää **Tyhjä sijainti ilman saapuvia töitä** -strategiaa. Jollet määritä kolmatta toimintoa käsittelemään ylivuotoskenaariota, on mahdollista saada kaksi lopputulosta, kun varastossa ei ole enää kapasiteettia: työ voidaan luoda, vaikka sijainteja ei ole määritetty, tai työn luontiprosessi saattaa epäonnistua. Tulos määrittyy sivun **Sijaintidirektiivivirheet** määrityksistä, joissa voit päättää, valitaanko **Pysäytä työ sijaintidirektiivivirheeseen** -asetus kullekin työtilaustyypille.
