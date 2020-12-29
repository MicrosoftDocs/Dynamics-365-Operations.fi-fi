---
title: Ajoitusmoduulin suorituskyvyn parantaminen
description: Tässä ohjeaiheessa on tietoja ajoitusmoduulista ja sen suorituskyvyn parantamisesta.
author: ChristianRytt
manager: tfehr
ms.date: 09/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 19311
ms.assetid: 5ffb1486-2e08-4cdc-bd34-b47ae795ef0f
ms.search.region: Global
ms.search.industry: ''
ms.author: kamaybac
ms.search.validFrom: 2020-09-03
ms.dyn365.ops.version: ''
ms.openlocfilehash: 1c1b940754021956998fe27ba16020d4b16aedf1
ms.sourcegitcommit: 092ef6a45f515b38be2a4481abdbe7518a636f85
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/16/2020
ms.locfileid: "4427386"
---
# <a name="improve-scheduling-engine-performance"></a>Ajoitusmoduulin suorituskyvyn parantaminen

[!include [banner](../includes/banner.md)]

Resurssien ajoitusmoduulia käytetään suunniteltujen ja vapautettujen tuotantotilausten reittien aikatauluttamiseen. Moduuli julkaistiin alun perin Dynamics AX 2012:n osana, ja sitä on parannettu useita kertoja julkaisun jälkeen.

[JSS (job shop scheduling) -ongelma](https://en.wikipedia.org/wiki/Job_shop_scheduling) on erittäin monimutkainen kombinatorinen ongelma, jossa ratkaisuaika kasvaa eksponentiaalisesti päätöksen muuttujien määrän mukaan. Asiakkaat määrittävät usein tuotantoreitit ja liittyvät tiedot siten, että tuloksena on aikataulutusongelma, jota ei ratkaista kohtuullisessa ajassa kaikkein uusimmillakaan laitteilla. Tässä ohjeaiheessa käsitellään ajoitusmoduulia ja tapaa, jolla tietyt määritykset voivat vaikuttaa suorituskykyyn.

Aikatauluttamisen suorituskykyä parannettaessa yleisesti suositellaan yksinkertaistamaan ongelmaa, joka moduulin on ratkaistava. Keskeisiä suorituskykyyn vaikuttavia tekijöitä ovat esimerkiksi seuraavat:

- Reitit, joissa on useita työvaiheita
- Reitit, joissa on samanaikaisia työvaiheita
- Työvaiheet, joissa resurssien määrä on suurempi kuin yksi
- Työvaiheet, joissa on useita käytettäviä resursseja
- Kiinteiden linkkien käyttö
- Rajallisen kapasiteetin käyttö
- Käytettyjen kalenterien määrä
- Kalenterissa olevien ajankohtien päiväkohtainen määrä
- Reitin kokonaiskesto
- Useiden ajoitusmoduulien suorittaminen samanaikaisesti

## <a name="overview-of-basic-scheduling-flow"></a>Ajoituksen perustyönkulun yleiskatsaus

Tietyn määrityksen vaikutusta suorituskykyyn selvitettäessä on tärkeää tietää ainakin jossain määrin, miten prosessi etenee sekä moduulissa että sitä ympäröivässä X++-koodissa.

Aikataulutuksen perusprosessissa on kolme päävaihetta:

- **Tietojen lataaminen** – X++-tietomallit muunnetaan tässä vaiheessa moduulin sisäiseksi tietomalliksi töinä ja rajoituksina.
- **Aikatauluttaminen** – Tämä vaihe aikataulutuksen päälähde, joka käsittelee annetun mallin ja rajoitteet sekä muodostaa tuloksen. Moduuli pyytää tämän prosessin aikana tarvittaessa työaikaa koskevia tietoja ja aiemmin luotuja kapasiteetin varauksia X++-koodista.
- **Tietojen tallennus** – X++-koodi käsittelee moduulin tuloksena olevat työn kapasiteetin varauksen ajankohdat, jolloin kapasiteetin varaukset tallennetaan sekä töiden/työvaiheen/tilauksen alkamis- ja päättymisajat päivitetään.

## <a name="load-data-into-the-engine"></a>Tietojen lataaminen moduuliin

Ajoitusmoduulissa on Supply Chain Managementin tietokantaa abstraktimpi tietomalli, koska se on muodostettu yleisenä moduulina, joka voi käsitellä erilaisia tietolähteitä. Reitin, toissijaisten työvaiheiden ja suoritusajan käsitteet on muunnettava yleiseksi työ- ja rajoitusmalliksi, jonka moduuli tuo näkyviin. Mallin muodostamislogiikka sisältää merkittävän osan liiketoimintalogiikkaa ja se vaihtelee lähdetietojen mukaan. Vastaava X++-luokka on `WrkCtrScheduler` ja siinä on johdetut luokat suunniteltuja tuotantotilauksia, vapautettuja tuotantotilauksia ja projektiennusteita varten.

Käytetään esimerkkinä seuraavassa taulukossa ja kuvassa näkyvää reittiä, joka vaikuttaa olevan suhteellisen yksinkertainen.

| Työv. Nro | Prioriteetti | Asetusaika | Ajoaika | Jonotusaika jälkeen | Resurssien määrä | Seuraava |
| --- | --- | --- | --- | --- | --- | --- |
| 10 | Ensisijainen | 1.00 | 2.00 | | 1 | 20 |
| 10 | Toissijainen&nbsp;1 | | | | 1 | 20 |
| 20 | Ensisijainen | | 3.00 | 1.00 | 3 | 0 |

![Reittikaavioesimerkki](media/scheduling-engine-route.png "Reittikaavioesimerkki")

Kun tämä lähetetään moduuliin, se jakautuu kahdeksaksi työksi, kuten seuraavassa kuvassa. (Voit suurentaa kuvan valitsemalla sen.)

[![Ajoitusmoduulin työt](media/scheduling-engine-jobs.png "Ajoitusmoduulin työt")](media/scheduling-engine-jobs-large.png)

Kahden työn välinen vakiolinkki on `FinishStart`. Tämä tarkoittaa sitä, että yhden työn päättymisajan on oltava ennen toisen työn alkamisaikaa. Koska määrityksen tekijän on oltava sama resurssi, joka tekee myöhemmin prosessin, niiden välillä on `OnSameResource`-rajoituksia. Kohdan 10 ensisijaisen ja toissijaisen työvaiheen välillä on `StartStart`- ja `FinishFinish`-linkit. Tämä tarkoittaa sitä, että kummankin työn on alettava ja päätyttävä samanaikaisesti. `NotOnSameResource`-rajoitukset puolestaan estävät sen, että sama resurssi ei voi olla ensisijainen ja toissijainen.

Työvaiheen 20 resurssien määräksi on määritetty 3, ja prosessityö on jaettuna siinä kolmeksi erilliseksi työksi, jossa kaikki työt on suoritettava täsmälleen samanaikaisesti.
Tässä tapauksessa reittiryhmä on määritetty olevaan varaamatta kapasiteettia jonolle aikojen jälkeen, minkä vuoksi jälkeen tulevassa jonossa on vain yksi työ.

Ajoitusmoduuli ymmärtää vain töiden käsitteen eikä tiedä, mitä työvaiheet ovat. Tämän vuoksi työvaiheita aikataulutettaessa myös työvaiheet jaetaan töiksi, joita ei kuitenkaan säilytetä tietokannassa.

Jokaiselle työlle määritetään myös työn kapasiteettitarve (tarvittavien sekuntien määrä). Resurssitarpeiden määritysten mukaan kullekin työlle voidaan lähettää myös luettelo kaikista mahdollisesti sopivista resursseista, joilla työ voitaisiin suorittaa, ja mikä on resurssitarve on kyseiselle resurssille. Vaikka luettelo sopivista resursseista lähetetään mallia muodostettaessa, moduulin on silti varmistettava, että resurssimääritys on voimassa koko työn keston ajan.

## <a name="scheduling-engine-internals"></a>Moduulin sisäisten toimintojen aikatauluttaminen

### <a name="scheduling-engine-interface"></a>Moduuliliittymän aikatauluttaminen

Moduulin sisäisestä toiminnasta saa parhaan käsityksen tarkastelemalla ulkoisesti näkyvissä olevia toimintoja. X++-koodissa tärkein liittymä `WrkCtrSchedulerEngineInterface`. Sen menetelmät käsitellään seuraavissa alikohdissa.

#### <a name="general-engine"></a>Yleinen moduuli

| **Tapa** | **Tarkoitus** |
| --- | --- |
| `run` | Aikatauluttaa kaikki ladatut työt ja palauttaa virhekoodin. |
| `getJobSchedulingSequenceResult` | Hakee aikataulutuksen tuloksen ja ensimmäisen virhetyön tietyn työ määrittämälle jaksolle. |
| `validateJobCapacityReservations` | Vahvistaa kaikkien moduulin tallentamien töiden kapasiteetin varaukset. |
| `setReservationsTimeStamp` | Lähettää aikaleiman moduuliin, joka on määritetty kaikissa moduulin välimuistissa ajoitettujen töiden uusissa kapasiteetin varauksissa. |
| `addPropertyToGroupAggregation` | Lisää ominaisuuden etuliitteen ominaisuusjoukkoon, jota käytetään, kun kapasiteettia koostetaan. |
| `addResource` | Lisää resurssin ajoitusmoduulin resurssipooliin. |
| `addResourceGroup` | Lisää resurssiryhmän ajoitusmoduulin resurssiryhmäpooliin. |
| `addResourceGroupMembership` | Lisää resurssin jäsenenä resurssiryhmään. |
| `addOptimizationGoal` | Lisää aikataulutuksen optimointitavoitteen (keston tai prioriteetin). |

#### <a name="individual-jobs"></a>Yksittäiset työt

| **Tapa** | **Tarkoitus** |
| --- | --- |
| `addJobInfo` | Lisää työtietotietueen, joka ilmoittaa moduulille ajoitettavasta työstä. |
| `addConstraintJobEndsAt` | Lisää rajoituksen, jonka mukaan työn on päätyttävä määritettynä päivänä ja aikana. |
| `addConstraintJobStartsAt` | Lisää rajoituksen, jonka mukaan työn on alettava määritettynä päivänä ja aikana. |
| `addConstraintMaxJobDays` | Määrittää rajoituksen, jonka mukaan työ voi kestää enintään määritetyn määrän päiviä. |
| `addConstraintResourceRequirement` | Lisää rajoituksen, jonka mukaan työ aikataulutettava tietyssä resurssissa. |
| `addJobBindPriority` | Lisää työn sidonnan prioriteetin (työ, rajoitustaso) parille. Mitä korkeampi prioriteetin arvo on, sitä aiemmin työn muuttujat sidotaan. Työ käsitellään ennen töitä, joiden prioriteetin arvo samassa jaksossa on alhaisempi. |
| `addJobCapacity` | Lisää kapasiteetin kuormituksen työlle (kuten pakollisen työn suorituspalvelun) riippumatta siitä, missä resurssissa työ suoritetaan. |
| `addJobResourceCapacity` | Lisää resurssin resurssijoukkoon, jolla voidaan suorittaa työ, ja ilmaisee kyseisen resurssin suorittamiseen tarvittavan kapasiteetin. |
| `addJobGoal` | Lisää työn tavoitetyypit tietylle rajoitustasolle (varhaisin päättymisaika tai myöhäisin alkamisaika). |
| `addJobResourcePriority` | Lisää prioriteetin, jota käytetään, kun työ aikataulutetaan resurssille. |
| `addJobResourceRuntime` | Määrittää työn ajan, joka on riippuvainen resurssista, johon työ aikataulutetaan. |
| `addJobRuntime` | Määrittää työn ajan, joka ei ole riippuvainen resurssista, johon työ aikataulutetaan. |
| `scheduleJobOnResourceGroup` | Merkitsee työn aikataulutettavaksi resurssiryhmätasolla. |
| `setJobResourcePreemptionAllowed` | Määrittää, onko työn etuosto sallittu resurssin työlle (jos moduuli saa aikatauluttaa työn epäyhtenäiset kapasiteettipaikat). |
| `setRequiredNumberOfResources` | Määrittää työn ajoittamiseen tarvittavien resurssien määrän (vain työvaiheiden ajoituksessa). |

#### <a name="constraints-between-jobs"></a>Töiden väliset rajoitukset

| **Tapa** | **Tarkoitus** |
| --- | --- |
| `addJobLink` | Lisää linkin (kuten finish\>start) kahden työn välille. |
| `addConstraintEndsDelayed` | Määrittää rajoituksen, jonka mukaan työ ei voi päättyä, ennen kuin toiset työt päättyvät. Sisältää myös viiveajan. |
| `addConstraintJobListWorkingTimeIntersect` | Lisää rajoituksen, jonka mukaan töille varattujen kapasiteettipaikkojen on oltava töiden käyttämien kahden resurssin työaikojen leikkauskohdassa. |
| `addConstraintJobOverlap` | Lisää rajoituksen, joka määrittää, miten työt jaksotetaan, kun annettua nimikkeen määrää voidaan siirtää kahden resurssin välillä silloin, kun ensimmäisten resurssin käsittelyä ei ole käsitelty. Tällä tavoin toinen resurssi voi aloittaa käsittelyn. |
| `addConstraintNotOnSameResource` | Lisää rajoituksen, jonka mukaan kahta työtä ei saa aikatauluttaa samalle resurssille. |
| `addConstraintOnSameResource` | Lisää rajoituksen, jonka mukaan kahden työn on käytettävä samaa resurssia. |
| `addJobSameReservations` | Lisää rajoituksen, jonka mukaan työn kapasiteetin varauksen on oltava samassa ajankohdassa kuin ensisijainen työ. |
| `setPrimaryParallelJob` | Lisää tietoja siitä, mikä työ on ensisijainen työ samanaikaisten töiden joukossa. |

### <a name="solver"></a>Selvitys

Moduuli itsessään on käytännössä erikoistunut rajoitusten selvitystoiminto, johon on lisätty mukautettua heuristiikkaa. Selvitystoiminto perustuu kahteen pääelementtiin: muuttujiin ja rajoituksiin.

#### <a name="variable"></a>Muuttuva

Muuttuja vastaa mahdollisten arvojen toimialuetta. Ajoitusmoduulissa on kahdentyyppisiä muuttujia:

- **Päivämäärä- ja aikamuuttuja** – Sisältää kaikkien päivämäärien ja kellonaikojen toimialueen. Toimialuetta voidaan rajoittaa siirtämällä muuttujan kellonajan ala- ja ylärajaa lähemmäksi toisiaan.
- **Resurssimuuttuja** – Sisältää käytettävien resurssien toimialueen. Toimialuetta voidaan rajoittaa poistamalla resursseja luettelosta.

#### <a name="constraint"></a>Rajoitus

Rajoitus rajoittaa muuttujien toimialueita. Samalla se on kuitenkin riippuvainen muuttujista, joten se aktivoituu, kun muuttujat muuttuvat. Rajoituksen levittämisprosessi tapahtuu, kun rajoitus suorittaa päätoimintoaan ja raportoi takaisin päälogiikkaan, jos se onnistuu.

Muuttujaa pidetään sidottuna, kun sitä ei voi enää rajoittaa. Päivämäärä- ja aikamuuttujan osalta tämä tarkoittaa, että sidonta on sama ylhäällä ja alhaalla, ja resurssimuuttujan osalta se tarkoittaa, että sillä on vain yksi käytettävä resurssi. Kun kaikki muuttujat sidotaan, ratkaisu on löytynyt.

### <a name="constraint-levels"></a>Rajoitustasot

Kun aikatauluttaminen suoritetaan materiaalitarpeiden suunnittelun (MRP) vaiheessa, tilaukset aikataulutetaan tarvepäivästä taaksepäin. Jos kuluvana päivänä tai myöhemmin alkavaa ja ennen tarvepäivää päättyvää aikataulua ei löydy, aikataulutuksen suunta muuttuu eteenpäin kuluvasta päivästä.

Tämä pääliiketoimintasääntö käsitellään järjestelmällä rajoitukset tasoihin. Jos ratkaisua ei löydy, kun rajoituksia käytetään korkeimmalla tasolla, kaikki kyseisen tason rajoitukset jätetään pois ja alempaa tasoa kokeillaan. Käytännössä tämä tarkoittaa, että taaksepäin suuntautuvassa aikataulutuksessa mallin tasolla 1 on myöhäisimmän aloitusajan työn tavoitteet annetulla suurimmalla päättymisaikarajoituksella (tarvepäivä) ja tasolla 0 on aikaisimman päättymisajan työn tavoitteet annetulla kuluvan päivän pienimmällä aloitusaikarajoituksella.

### <a name="algorithm"></a>Algoritmi

Moduulin algoritmin päävaiheet:

1. Erikseen ratkaistavien jaksojen (työketjujen) etsiminen.
1. Yritetään etsiä jaksolle ensin ratkaisu korkeimmalla rajoitustasolla.
    1. Töiden lajittelu jaksossa työn tavoitteen ja prioriteettien perusteella siten, että aloitustyö löydetään.
    1. Työt toistetaan seuraavassa järjestyksessä:
        1. Kaikkien levitettävien rajoitusten etsiminen ja levittämisen suorittaminen.
        1. Jos kaikki työn muuttujat on sidottu, kyseisen työn ratkaisu on löydetty.
        1. Jos yhtä muuttujista ei voitu sitoa rajoituksia rikkomatta, muuttujan sidonta perutaan, toimialueella kokeillaan toista (resurssimuuttujan) arvoa ja rajoituksen levittäminen suoritetaan uudelleen.
1. Jos ratkaisua ei löydy, kaikki nykyisen rajoitustason rajoitukset poistetaan, rajoitustasoa alennetaan (jos alempia tasoja on käytettävissä) ja ratkaisuhaku suoritetaan uudelleen uudella rajoitusjoukolla.
1. Jos sopivaa ratkaisua ei löytynyt, optimointivaihe käynnistetään. Se yrittää löytää paremman ratkaisun siihen saakka, että optimointi aikakatkaistaan, tai kaikki resurssiyhdistelmät on kokeiltu.

Ratkaisun selvitystoiminto ei ole tietoinen aikataulutusalgoritmin yksityiskohdista. Ratkaisevaa onkin erilaisten rajoitusten määritelmät ja niiden yhdistelmä.

### <a name="determining-working-times"></a>Työaikojen määrittäminen

Suuri osa moduulin (sisäisistä) rajoituksista hallitsee resurssin työaikaa ja kapasiteettia. Tehtävänä on siis käydä läpi resurssin työajan ajankohdat tietystä vaiheesta tiettyyn suuntaan ja etsiä riittävän pitkää aikaväliä, joihin kapasiteettia (aikaa) tarvitsevat työt sopivat.

Sitä varten moduulin on tiedettävä resurssin työajat. Päämallin tiedoista poiketen työajoissa käytetään *tarveohjattua latausta* eli ne ladataan moduuliin, kun niitä tarvitaan. Näin toimitaan siksi, että Supply Chain Managementissa kalenterissa on usein työaikoja hyvin pitkille jaksoille ja yleensä kalentereita on useita, joten valmiiksi ladattavia tietoja olisi paljon.

Moduuli pyytää kalenteritietoja paloina kutsumalla X++-luokkamenetelmän `WrkCtrSchedulingInteropDataProvider.getWorkingTimes`. Pyyntö koskee tietyn kalenteritunnuksen tiettyä aikaväliä. Sen mukaan, mikä on palvelimen välimuistin tila Supply Chain Managementissa, kukin näistä pyynnöistä voi päätyä useisiin tietokantakutsuihin, mikä vie paljon aikaa (suhteessa pelkkään laskenta-aikaan). Jos kalenterissa on lisäksi erittäin tarkkoja työaikamääritelmiä ja useita päiväkohtaisia työaikavälejä, myös tämä pidentää latautumisaikaa.

Kun työaikatietoja ladataan ajoitusmoduuliin, se säilyttää tietyn kalenterin sisäisessä välimuistissa. Tämä tarkoittaa sitä, että jos jotkin muut työt tai resurssit käyttävät samaa kalenteria, seuraavat haut voidaan tehdä nopeasti muistista. Yksi yleinen syy huonolle suorituskyvylle on se, että kullekin resurssille käytetään erillistä kalenteritunnusta, jolloin kullekin kalenterille on pyydettävä tiedot, vaikka kalenterien sisältö olisi sama.

### <a name="finite-capacity"></a>Rajallinen kapasiteetti

Rajallista kapasiteettia käytettäessä kalenterin työajan ajankohdat jaetaan ja niitä vähennetään aiemmin luotujen kapasiteetin varausten perusteella. Vaikka nämä varaukset noudetaan myös samalla `WrkCtrSchedulingInteropDataProvider`-luokalla kuin kalenterit, niissä käytetään menetelmää `getCapacityReservations`. Jos aikataulutus tehdään pääsuunnittelun aikana, tietyn pääsuunnitelman varaukset otetaan huomioon ja, jos **Pääsuunnittelun parametrit** -sivulla on niin määritetty, myös vahvistettujen tuotantotilausten varaukset sisällytetään. Vastaavasti myös tuotantotilausta aikataulutettaessa on mahdollista sisällyttää varauksia aiemmin luoduista suunnitelluista tilauksista, vaikka se ei olekaan yhtä yleistä kuin toisin päin.

Rajallisen kapasiteetin käyttäminen hidastaa aikatauluttamista monesta syystä:

- Kapasiteettitietojen noutaminen tietokannasta on hidasta ja kapasiteettitietojen palvelinpuolen välimuistitallennus ei ole yleensä yhtä tehokasta, sillä niitä ei jaeta resurssien kesken toisin kuin kalenterit, jotka yleensä jaetaan.
- Läpikäytävien työajan ajankohtien määrä kasvaa jakojen vuoksi, ja pitkiä ajanjaksoja on yleensä tutkittava, ennen kuin ratkaisu löytyy.
- Kun aikataulutus on valmis, ristiriitaiset varaukset on tarkistettava. (Lisätietoja on kohdassa Useiden ajoitusmoduulien suorittaminen samanaikaisesti.)

### <a name="examining-the-resource-combinations"></a>Resurssiyhdistelmien tutkiminen

Jos työjakso sisältää vain `FinishStart`-vakiolinkkejä eli se muodostaa yksinkertaisen ketjun ilman haaroja, optimaalinen tulos (yksittäisestä tilauksesta katsottuna, ei tilausten välillä) saavutetaan etsimällä paras ratkaisu ensimmäiselle työlle ja siirtymällä sitten etsimään parasta ratkaisua seuraavalle työlle. Työn paras ratkaisu tarkoittaa sellaisen resurssin etsimistä, jolla saadaan työn tavoitetta lähinnä oleva työn aloitus- ja päättymispäivä (mikä tarkoittaa eteenpäin aikatauluttamisessa mahdollisimman varhaisen työn päättymispäivän hakemista) noudattaen silti samalla rajoituksia.

Samanaikaisissa töissä ratkaisun etsiminen voi edellyttää eri resurssiyhdistelmien tutkimista. Mahdollisten resurssiyhdistelmien määrä saadaan yhdistettyjen rinnakkaisten töiden käytettävien resurssien määrästä. Etenkin aikataulutettaessa tilausta taaksepäin tarvepäivästä voi kestää jonkin aikaa, ennen kuin logiikka tiedostaa, ettei millään ongelman ratkaisulla saada samanaikaisia töitä sopimaan ennen kuluvaa päivää. Niinpä sen on tarkistettava kaikki yhdistelmät, koska saattaa löytyä joitakin tehokkaita resursseja tai eri kalenteri, jolla voidaan saada tulos. Niinpä jos aikakatkaisurajaa ei ole määritetty, logiikkaa suoritetaan pitkään, ennen kuin suunta vaihdetaan eteenpäin.

Tämä kombinatorinen logiikka myös tarkoittaa, että käytettävien lisäresurssien lisääminen voi hidastaa moduulin toimintaa. Jos suorituskykyongelmia esiintyy, kun samanaikaisia työvaiheita ja aikataulutusta suoritetaan rajoittamattomalla kapasiteetilla, ongelmat voidaan korjata osittain tekemällä reitin suunnitteluohjelmalla päätös käytettävästä resurssista ja delegoimalla resurssi sitten suoraan työvaiheeseen (sillä moduuli päätyy useimmissa tapauksissa poimimaan saman resurssin, joten lopputulos on sama).

### <a name="hard-links"></a>Kiinteät linkit

Kun kahden työn välinen linkkityyppi määritetään kiinteäksi, yhden työn lopettamisen ja seuraavan työn aloittamisen välillä ei ole lainkaan aikaväliä. Tämä voi olla erittäin kätevää skenaarioissa, kuten silloin kun metallia kuumennetaan yhdessä työssä ja sitten prosessoidaan seuraavassa työssä, sillä metallin ei haluta viilenevän vaiheiden välissä.

Jos reitti muodostaa vakiomuotoista symbolista linkkiä ja eteenpäin aikatauluttamista käytettäessä yksinkertaisen ketjun ilman haaroja, tulos saadaan etsimällä ensimmäisen työn ratkaisu, joka vastaa omia rajoituksia ja siirtymällä sitten ketjussa edellisen työn päättymisajasta seuraavaan työhön. Jos nykyinen työ ei löydä kapasiteettia, sen aloitusaika siirretään eteenpäin välittämättä siitä, että edelliset työt voivat luoda aukkoja töiden väliin. Jos samassa skenaariossa käytetään kuitenkin kiinteitä linkkejä (etenkin yhdessä rajallisen kapasiteetin kanssa), ketjussa myöhemmin tuleva työ ei löydä kapasiteettia, jolloin kaikkia aiemmin aikataulutettuja töitä on kuljetettava mukana ja siten aikataulutettava uudelleen useita tapoja. Etenkin skenaarioissa, joissa useissa resursseissa on suuri kuormitus, kiinteät linkit voivat aiheuttaa ketjureaktion, jossa kaikki työt vaikuttavat toisiinsa ja suoritettavien iteraatioiden määrään, ennen kuin tulos vakiintuu toimivaksi aikatauluksi.

## <a name="running-scheduling-engines-in-parallel"></a>Ajoitusmoduulien suorittaminen samanaikaisesti

Jos aikataulutus suoritetaan osana pääsuunnittelua, jossa käytetään apuosia, jokainen pääsuunnittelun apuosaketju voi poimia myös tuotantotilauksen aikataulutustehtäviä. Tämän vuoksi samanaikaisesti voidaan suorittaa useita ajoitusmoduuleja. Vaikka monisäikeisyydestä on yleensä merkittäviä suorituskykyetuja, aikataulutuksen yhteydessä siinä tiettyjä toiminnallisia haittoja.

Tarvesuunnittelussa kaikki tietyn tuoterakennetason tuotantotilaukset aikataulutetaan tarvepäiväjaksossa, joten tilaukset, joilla on aikaisin tarvepäivä, on aikataulutettava ensimmäisenä. Niinpä ne myös todennäköisimmin saavat käytettävissä olevan resurssin kapasiteetin. Jos useat moduulit kuitenkin tekevät poimintoja aikatauluttamattomien tilausten luettelosta, järjestys ei ole enää varma, sillä tilaukset voivat valmistua eri aikaan.

Jos aikataulutukseen käytetään lisäksi rajallista kapasiteettia ja useat moduuliesiintymät yrittävät aikatauluttaa tilauksia, jotka mahdollisesti käyttävät samoja resursseja samalla aikavälillä, seurauksena voi olla kilpailutilanne. Kyseisten kilpailutilanteiden määrä kirjataan **Aikatauluristiriidat**-kenttään pääsuunnitelmien historiasivulla. Ristiriitojen ratkaisulla on seuraava logiikka:

- Ajoita tilaus (lukitsematta) ja hae kapasiteetin varaukset.
- Tee lukitus.
- Tarkista, onko aikataulutetuilla resursseilla uusia kapasiteetin varauksia.
  - Jos ei, kirjoita kapasiteetti ja avaa lukitus.
  - Jos kyllä, vapauta lukitus ja aikatauluta tilaus uudelleen alusta alkaen.

Niinpä kun useita moduuliesiintymiä aikataulutetaan, tulos ei ole täysin deterministinen, koska tulos määräytyy sen mukaan, mikä on kunkin säikeen ajoitus.

## <a name="operation-scheduling-performance"></a>Työvaiheen aikataulutuksen suorituskyky

Vaikka työvaiheen aikataulutusta kutsutaan myös kapasiteetin raakasuunnitteluksi, moduulin kannalta sen ratkaiseminen voi olla hankalaa rajallista kapasiteettia käytettäessä, sillä toimivuuden määrittämiseen tarvitaan enemmän tietoja.

Resurssiryhmän kapasiteetti määrittää, mitkä resurssit ja kuinka monta resurssia on resurssiryhmän jäseninä. Itse resurssiryhmällä ei ole lainkaan kapasiteettia; sillä on kapasiteettia vain silloin, kun resurssit ovat ryhmän jäseniä. Koska resurssiryhmän jäsenyys voi vaihdella ajan mittaan, kapasiteetti on laskettava päivittäin.

Työvaiheiden aikatauluttamisessa resurssiryhmän kalenteria käytetään määrittämään kunkin työvaiheen aloitus- ja päättymisaika. Tämän vuoksi resurssiryhmän kalenteri rajoittaa sitä, kuinka paljon aikaa yhdelle työvaiheelle voidaan aikatauluttaa yhtenä päivänä yhdessä resurssiryhmässä. Toisin kuin tiettyjen resurssien kalenterissa kalenterin tehokkuustiedot ohitetaan resurssiryhmän osalta, sillä siinä ilmoitetaan vain aukioloajat eikä varsinaista kapasiteettia.

Jos esimerkiksi resurssiryhmän työaika tiettynä päivänä on 8.00–16.00, yksi työvaihe ei voi kuormittaa resurssiryhmää enemmän kuin mahtuu 8 tuntiin riippumatta siitä, kuinka paljon kapasiteettia resurssiryhmällä yhteensä on kyseisenä päivänä. Käytettävissä oleva kapasiteetti voi kuitenkin rajoittaa kuormitusta entisestään.

Kaikkien resurssiryhmään kuuluvien resurssien työn aikataulutuksen kuormitus tiettynä päivänä otetaan huomioon, kun resurssiryhmän käytettävissä olevaa kapasiteettia lasketaan kyseiselle päivälle. Laskenta tehdään seuraavasti kunkin päivän osalta:

*Käytettävissä oleva resurssiryhmän kapasiteetti = ryhmän resurssien kapasiteetti resurssien kalentereiden perusteella &ndash; ryhmän resursseille aikataulutettu työmäärä &ndash; toimintojen ryhmän resursseille aikataulutettu määrä &ndash; toimintojen resurssiryhmälle aikataulutettu määrä*

Resurssitarpeet voidaan määrittää reittityövaiheen **Resurssitarpeet**-välilehdessä käyttämällä joko tiettyä resurssia (jolloin työvaihe aikataulutetaan kyseisellä resurssilla) resurssiryhmässä tai resurssityypissä tai vähintään yhteä ominaisuutta, taitoa, kurssia tai sertifikaattia. Vaikka kaikkien näiden vaihtoehtojen käyttäminen tuo valtavasti joustavuutta reittisuunnitteluun, se myös monimutkaistaa moduulin aikatauluttamista, sillä kapasiteetti on otettava huomioon ominaisuuskohtaisesti. (Ominaisuus on abstrakti nimi, jolla moduuli viittaa esimerkiksi toimintoon tai taitoihin.)

Ominaisuus resurssiryhmän kapasiteetti on kaikkien niiden resurssiryhmän resurssien kapasiteetin summa, joilla on kyseinen ominaisuus. Jos ryhmän resurssilla on ominaisuus, se otetaan huomioon riippumatta siitä, mikä kapasiteettitaso tarvitaan.

Työvaiheiden aikataulutuksessa resurssiryhmän tietyn ominaisuuden käytettävissä olevaa kapasiteettia vähennetään, kun siihen on ladattu työvaihe, joka edellyttää kyseistä ominaisuutta. Jos työvaiheeseen tarvitaan useita ominaisuuksia, kapasiteettia vähennetään kaikissa tarvittavissa ominaisuuksissa.

Kunkin päivän osalta tarvitaan seuraava laskenta:

*Ominaisuuden käytettävissä oleva kapasiteetti = ominaisuuden kapasiteetti &ndash; työn aikataulutettu määrä resurssiryhmään sisältyvälle resurssille, jolla on tietty ominaisuus &ndash; toimintojen aikataulutettu määrä resurssiryhmään sisältyvälle resurssille, jolla on tietty ominaisuus &ndash; toimintojen aikataulutettu kuorma resurssiryhmälle, joka edellyttää tiettyä ominaisuutta*

Niinpä jos tiettyä resurssia on kuormitettu, kuormitus on otetaan huomioon resurssiryhmän ominaisuuskohtaisessa käytettävissä olevan kapasiteetin laskennassa, koska tietyn resurssin kuormitus vähentää resurssiryhmän kapasiteetin osuutta ominaisuudessa riippumatta siitä, koskeeko tietyn resurssin kuormitus kyseistä ominaisuutta. Jos kuormitus on resurssiryhmätasolla, se otetaan huomioon resurssiryhmän käytettävissä olevan ominaisuuskohtaisen kapasiteetin laskennassa vain, jos kuormitus koskee työvaihetta, joka edellyttää tiettyä ominaisuutta.

Edellä oleva logiikka on monimutkaista, koska sama koskee jokaista ominaisuustyyppiä, joten työvaiheiden aikatauluttaminen rajallista kapasiteettia käyttäen edellyttää, että tietoja ladataan merkittävä määrä.

## <a name="viewing-scheduling-engine-input-and-output"></a>Ajoitusmoduulin syötteen ja tuloksen näyttäminen

Saat lisätietoja aikataulutusprosessin syötteistä ja tuloksesta ottamalla lokiin kirjaamisen käyttöön valitsemalla **Organisaation hallinto \> Asetukset \> Aikataulutus \> Aikataulutuksen jäljityscockpit**.

Valitse tällä sivulla ensin **Ota lokiin kirjaus käyttöön** toimintoruudussa. Suorita sitten tuotantotilauksen aikatauluttaminen. Kun se on valmis palaa **Aikataulutuksen jäljityscockpit** -sivulle ja valitse **Poista lokiin kirjaus käytöstä** toimintoruudussa. Päivitä sivu, jonka jälkeen uusi rivi näkyy ruudukossa. Valitse ensin uusi rivi ja valitse sitten toimintoruudussa **Lataa**. Saat tällä tavoin pakatun .zip-kansion, jossa on seuraavat tiedostot:

- **Log.txt** – Tämä lokitiedosto sisältää vaiheet, jotka moduuli suorittaa. Se on erittäin tarkka ja voi tuntua sekavalta. Kun sitä käytetään reittiasetusten kokeilujen osana suorituskykyongelmia ratkaisemista, ensimmäisenä kannattaa katsoa ensimmäisen ja viimeisen rivin välistä aikaeroa, sillä näin saadaan selville tarkasti aika, jonka ajoitustoiminto on käyttänyt.
- **XmlModel.xml** – Tämä tiedosto sisältää X++-koodilla muodostetun mallin ja johon moduulin toiminta perustuu. Tiedostossa käytetty `JobId` vastaa työt (`ReqRouteJob` tai `ProdRouteJob`) sisältävää lähdetaulukon `RecId`-ominaisuuden. Tässä tiedostossa katsotaan yleensä, että `ConstraintJobStartsAt`- ja `ConstraintJobEndsAt`-ominaisuuksissa annetut päivämäärät ovat odotusten mukaiset, että `JobGoal`-ominaisuus on määritetty oikein ja että työt liittyvät toisiinsa `JobLink`-rajoitusten kautta.
- **XmlSlots.xml** – Tämä tiedosto sisältää kaikki moduulin pyytämät työajat ja kapasiteetin varaukset. Moduuli pyytää kalenterin työajat ja varaukset vain niinä aikajaksoina, jolloin se yrittää sijoittaa töitä (ja lisäpuskurin), joten jos tiedostossa on kaukana tulevaisuudessa olevia aikoja, se voi olla osoitus määrityksissä olevasta ongelmasta. `ResourceProperty`-solmut näytetään jokaiselle resurssille, joihin resurssiryhmä ja sen ominaisuudet on liitetty sekä niiden kaudet.
- **Result.xml** – Tämä tiedosto sisältää aikataulutusajon tuloksen.

Huomaa, että jäljitystoiminto voi vaikuttaa merkittävästi suorituskykyyn, joten käytä sitä vain tiettyjen tilausten aikatauluttamisen tutkimiseen harkitusti. Jos se on otettu käyttöön pääsuunnitteluajon aikana, se saavuttaa nopeasti kokorajan ja pysähtyy.

## <a name="troubleshooting-performance"></a>Suorituskyvyn vianmääritys

Kuten edellisissä osissa on selitetty, ajoitusmoduulin määrittämisessä käytössä on joitakin heikkouksia, mikä voi johtaa suorituskykyongelmiin. Näiden ongelmien vianmäärityksen apuna voi käyttää seuraavaa tarkistusluetteloa. On tärkeää ottaa huomioon kaikki mainitut kohdat, sillä usein juuri useiden seikkojen yhdistelmää aiheuttaa ongelmia.

### <a name="performing-scheduling-as-part-of-mrp-when-it-is-not-needed"></a>Aikataulutuksen suorittaminen tarvesuunnittelun osana, kun se ei ole välttämätöntä

Vaikka reittejä käytetään tuotannon hallinnassa esimerkiksi kustannuslaskennassa ja raportoinnissa, niitä ei kuitenkaan ehkä tarvitse ottaa huomioon tarvesuunnittelun aikana. Joissakin tapauksissa suunnitteluun riittää, että käytössä on nimikkeelle määritetty tuotannon vakioläpimenoaika. Poista reitin aikatauluttaminen käytöstä määrittämällä kapasiteetin aikarajaksi nolla. Jos aikataulutus on tehtävä, kapasiteetin aikaraja on määritettävä huolellisesti, koska reittejä ei ehkä tarvitse ottaa huomioon tarvesuunnittelun koko laajuuden aikarajoissa.

Huomaa, että jos tilausta ei aikatauluteta tarvesuunnittelun aikana, se on siinä tapauksessa aikataulutettava, kun suunniteltu tilaus vahvistetaan. Tämän vuoksi vahvistusprosessi kestää kauemmin, joten tarvesuunnittelun aikana saatu suorituskykyhyöty voidaan menettää vahvistuksen aikana sen mukaan, kuinka monta ehdotettua suunniteltua tilausta vahvistetaan.

### <a name="route-with-unnecessary-operations"></a>Reitti, jossa on tarpeettomia työvaiheita

Reittiä suunniteltaessa on kiusaus yrittää mallintaa todellisuutta täsmällisesti ja ottaa huomioon kaikki tuotannon vaiheet. Vaikka tämä voi olla hyödyllistä joissain tapauksissa, se heikentää suorituskykyä, sillä moduulin käsittelemä malli suurenee (sekä töiden että rajoitusten osalta) ja SQL-lausekkeita suoritetaan enemmän töiden ja kapasiteetin varausten lisäämisen ja päivittämisen vuoksi. Vaikutuksia on myöhemmin, sillä töiden edistymisestä on jossain vaiheessa raportoitava. Tätä tosin voidaan helpottaa automaattisilla julkaisuilla. Jos tietoja ei käytetä mihinkään, syntyy turhaa kuormitusta.

Tämän vuoksi kannattaakin luoda vain työvaiheet, joita ehdottomasti tarvitaan aikataulutukseen (mikä on tyypillisesti pullonkaularesurssit) ja/tai kustannuslaskentaan. Vaihtoehtoisesti pienet, erilliset työvaiheet voi ryhmitellä yksi suureksi työvaiheeksi, joka vastaa suurempaa prosessin osaa.

### <a name="many-applicable-resources-for-an-operation"></a>Työvaiheessa useita käytettäviä resursseja

Työvaiheen käytettävien resurssien määrä määritetään työvaihesuhteessa määritettyjen resurssitarpeiden perusteella. Tarve voi koskea joko tiettyä (yksittäistä) resurssia tai se voi perustua resurssin resurssiryhmän jäsenyyteen tai ominaisuuteen.

Jos aikataulutuksessa ei käytetä rajallista kapasiteettia ja kaikilla käytettävillä resursseilla on sama kalenteri ja tehokkuus, ajoitusmoduuli päätyy poimimaan työvaiheeseen aina saman resurssin mutta vasta sen jälkeen, kun se on kokeillut kaikki käytettäviä resursseja, koska se on halunnut tarkistaa, onko jokin resursseista parempi kuin jokin toinen. Tässä tapauksessa aikataulutuksen kuormitusta voidaan vähentää merkittävästi määrittämällä aina vain tietyn resurssin työvaiheeseen reitin suunnittelun aikana.

### <a name="route-with-parallel-operations"></a>Reitti, joissa on samanaikaisia työvaiheita

Vaikka samanaikaiset työvaiheet (ensisijainen/toissijainen) ovat tehokas työkalu mallintaa skenaarioita, joissa esimerkiksi konetta ja koneen käyttäjää tarvitaan suorittamaan tietty tehtävä, ne myös aiheuttavat paljon suorituskykyongelmia. Jos tietyn yksittäisen resurssin tarve on määritetty sekä ensisijaiselle että toissijaiselle työvaiheelle, se ei yleensä ole ongelma. Mutta jos kummallekin työvaiheelle on monia mahdollisia resursseja, aikataulutuksen laskennallisen monimutkaisuus lisääntyy merkittävästi.

Samanaikaisten työvaiheiden tilalla voi käyttää joko parien mallintamista virtuaalisina resursseina (jotka sitten ilmaisevat ryhmän, joka on aina yhdessä työvaiheessa) tai toisen työvaiheen jättämistä mallintamatta, jos se ei ilmaise pullonkaulaa.

### <a name="route-with-quantity-of-resources-higher-than-1"></a>Reitti, joissa resurssien määrä on suurempi kuin 1

Jos työvaiheeseen tarvittavien resurssien määrä on määritetty suurempi kuin yksi, tulos on käytännössä sama kuin käytettäessä ensisijaisia/toissijaisia työvaiheita, koska moduuliin lähetetään useita samanaikaisia töitä. Tässä tapauksessa ei kuitenkaan ole mahdollisuutta käyttää tietyn resurssin määrityksiä, koska määrän ollessa suurempi kuin yksi työvaiheessa on oltava käytettävissä useampi kuin yksi resurssi.

### <a name="excessive-use-of-finite-capacity"></a>Liiallinen rajallisen kapasiteetin käyttö

Rajallisen kapasiteetin käyttö edellyttää, että moottori lataa kapasiteettitiedot tietokannasta ja on ylimääräistä laskentakapasiteettia, koska ratkaisun on löytäminen on vaikeampaa etenkin ympäristöissä, joissa resurssit varataan lähelle enimmäiskapasiteettia. Tämän vuoksi onkin tärkeää arvioida huolellisesti, onko resurssin todellakin käytettävä rajallista kapasiteetti vai voidaanko ne ylivarata. Koska rajallisen kapasiteetin resurssien kesken voi olla eroja siitä, kuinka tärkeää on, ettei niitä ylivarata, resurssissa kannattaa käyttää pullonkaula-asetusta yhdessä suunnitelman erillisen Kapasiteetin aikaraja pullonkaularesursseille -arvon kanssa. Pullonkaulan käyttäminen voi mahdollistaa sen, että yleistä rajallisen kapasiteetin aikarajaa voidaan alentaa.

### <a name="setting-hard-links"></a>Kiinteiden linkkien määrittäminen

Reitin vakiolinkkityyppi on *symbolinen*, jolloin yhden työvaiheen valmistumisajan ja seuraavan alkamisajan välillä voi olla aikaväli. Valitettavasti tämän salliminen aiheuttaa sen, että jos yhdelle työvaiheelle ei ole käytettävissä materiaaleja tai kapasiteettia erittäin pitkään aikaan, tuotanto voi joutua odottamaan pitkäänkin, mikä puolestaan voi lisätä keskeneräisiä töitä. Kiinteitä linkkejä käytettäessä näin ei tapahdu, sillä päättymisen ja alkamisen on vastattava toisiaan täydellisesti. Kiinteiden linkkien määrittäminen kuitenkin hankaloittaa aikataulutusongelmaa entisestään, koska työajan ja kapasiteetin leikkaukset on laskettava työvaiheiden kahdelle resurssille. Jos mukana on myös samanaikaisia työvaiheita, laskennallinen aika lisääntyy merkittävästi. Jos kahden työvaiheen resursseilla on eri kalenterit, joilla ei ole lainkaan päällekkäisyyksiä, ongelmaa ei voida ratkaista.

Kiinteitä linkkejä kannattaakin käyttää vain silloin, kun ne ovat ehdottoman välttämättömiä, minkä lisäksi on pohdittava huolellisesti tarvitaanko niitä reitin jokaisessa työvaiheessa.

Keskeneräisten töiden määrää voi vähentää kiinteitä linkkejä käyttämättä aikatauluttamalla tilauksen kahdesti siten, että jälkimmäisellä kerralla käytetään päinvastaista suuntaa. Jos ensimmäinen aikataulutus tehtiin taaksepäin toimituspäivästä, toinen on sitten tehtävä eteenpäin aikataulutetusta alkamispäivästä. Tällä tavoin työt tiivistetään mahdollisimman hyvin, jolloin keskeneräisen työ minimoidaan.

### <a name="separate-calendar-for-each-resource"></a>Jokaisella resurssilla erillinen kalenteri

Yksi tärkeimmistä ajoitusmoduulin tietolähteistä on kalenterin tiedot, joiden lataaminen tietokannasta voi olla kallista. Koska kalenterit luodaan mallien pohjalta, kullekin resurssille on kiusaus luoda oma kalenteri, jonka tietoja sitten säädetään, jos resurssilla on käyttökatkos tai muita ongelmia. Jos näin toimitaan moduulien mahdollisuus tallentaa kalenterin tiedot välimuistiin rajoittuu huomattavasti, sillä moduulin olisi pyydettävä uudet tiedot kullekin resurssille, mikä voi olla merkittävä suorituskykyongelmien aiheuttaja. Kalentereita kannattaa sen sijaan käyttää mahdollisimman paljon uudelleen resurssien kesken ja hallita sitten käyttökatkosmuutoksia määrittämällä jaksolle eri kalenteritunnus.

### <a name="high-number-of-working-time-slots-per-calendar-day"></a>Kalenteri suuri työn ajankohtien päiväkohtainen määrä

Koska moduuli etsii kapasiteettia tarkastelemalla ajankohtia yksi kerrallaan, kalenterin päiväkohtaisten ajankohtien määrä kannattaa minimoida. Se voidaan tehdä esimerkiksi miettimällä, onko tärkeää, että aikataulussa näkyy työntekijöiden viiden minuutin tauko kerran tunnissa.

### <a name="large-or-none-scheduling-timeouts"></a>Aikataulutuksen pitkät (tai puuttuvat) aikakatkaisut

Ajoitusmoduulin suorituskyky voidaan optimoida käyttämällä **Ajoitusparametrit**-sivulla olevia parametreja. **Aikataulutuksen aikakatkaisu käytössä**- ja **Aikataulutuksen optimoinnin aikakatkaisu käytössä** -asetuksena on aina oltava **Kyllä**. Jos asetuksena on **Ei**, aikataulutus voi periaatteessa jatkua vaikka kuinka kauan, jos luotu reitti ei ole käyttökelpoinen ja siinä on paljon vaihtoehtoja.

**Sarjakohtainen enimmäisajoitusaika** -asetuksen arvo määrittää, kuinka monta sekuntia voidaan enintään yrittää löytää ratkaisu yhdelle jaksolle (useimmissa tapauksissa jakso vastaa yhtä tilausta). Tässä käytettävä arvo määräytyy ennen kaikkea reitin monimutkaisuuden ja asetusten, rajallinen kapasiteetti, mukaan. Yleensä enintään 30 sekuntia on hyvä lähtökohta.

**Optimointiyritysten aikakatkaisu** -asetuksen arvo määrittää, kuinka monta sekuntia enintään etsitään ratkaisua, joka on parempi kuin alun perin löydetty ratkaisu. Tämä vaikuttaa vain reitteihin, joissa käytetään samanaikaisia työvaiheita, sillä on välttämätöntä, että erilaisia yhdistelmiä testataan.

> [!NOTE]
> Aikakatkaisuille määritettyjä arvoja voidaan käyttää sekä vapautettujen tuotantotilausten aikatauluttamiseen että suunniteltujen tilausten aikatauluttamiseen tarvesuunnittelun osana. Jos asetuksella on erittäin suuri arvo, tarvesuunnittelun suoritusaika voi tämän vuoksi pidentyä merkittävästi, kun suoritetaan suunnitelma, jossa on monia suunniteltuja tuotantotilauksia:
