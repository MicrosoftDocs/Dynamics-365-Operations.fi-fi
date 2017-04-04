---
title: Toimintoperusteisen alihankinta
description: "Tässä aiheessa kuvataan yksityiskohtaisesti alihankinnasta käyttäminen tuotantovirran lean-valmistuksen."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: KanbanJobSchedulingListPage, LeanRuleReassignmentWizard, PlanActivity, ReqSupplyDemandSchedule
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 267034
ms.assetid: 15c76a51-fa6d-42d2-994a-c67df6bae6a9
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: 8e57c53ca894aa44b71e15c1f66bd7c722ea8a81
ms.lasthandoff: 03/31/2017


---

# <a name="activity-based-subcontracting"></a>Toimintoperusteisen alihankinta

Tässä aiheessa kuvataan yksityiskohtaisesti alihankinnasta käyttäminen tuotantovirran lean-valmistuksen.

Microsoft Dynamics-365 operaatioille, ovat samanarvoisena, alihankinta: tuotantotilaukset ja lean-valmistuksen. Lean-valmistuksen lähestymistapaa alihankinta työtä on mallinnettu palveluna, joka liittyy Tuotantovirran tehtävän. Kustannusryhmän tyyppi, jonka nimi on erityinen **suora ulkoistaminen** on otettu käyttöön, ja alihankinnan palvelut kuuluvat enää tuoterakenne (BOM). Lean-valmistuksen kustannuslaskennan ratkaisun täysin integroitu alihankintatöiden kustannuslaskentaan.

## <a name="production-flows-that-involve-subcontractors"></a>Tuotantovirtojen, joihin liittyy alihankkijoiden
Tuotantovirran perusperiaatteena ei muutu, kun tehtävät ovat alihankintana. Materiaali kulkee sijaintien välillä prosessin toimintojen muuntaminen materiaali tuotteita ja siirtotehtäviä siirtää materiaali tai tuotteiden paikasta toiseen. Voit mallintaa sijainnit ja toimi solut toimittajan hallitaan määrittämällä toimittajatili, varastoon tai resurssi resurssiryhmään.  

Näiden ominaisuuksien perusteella, lean-valmistuksen ei vaadi erityisiä piirteitä materiaalia ja tuotteiden tukemiseksi. Mahdollista käyttävät valmistajien kuin tuotanto- tai -palvelujen tarjoajille voidaan mallintaa skenaariot perustuvat tuotantovirran ja arkkitehtuuri.  

Esimerkiksi supermarket, joka sijaitsee alihankkijan ulkopuolella toimii alihankkija. Kun käsittely-yksiköt tyhjennetään samalla alihankkijan, kanban-kortit palautetaan Seuraava toimitus ja kokoonpano-soluun. Supermarket on alihankkijan sitten täyttää. Siirrot ja alihankkijan avulla voidaan mallintaa eksplisiittinen siirtotehtäviä, keräilyyn ja lähetyksen prosessin tukemiseksi. Tarvittaessa nimenomainen rekisteröinti ei ole fyysinen liikenteen tukemiseksi siirto toiminta voidaan jättää pois.  

Tuotantovirran yleisen kapasiteetin kuormitusta voidaan käyttää alihankkija. Tuotantovirran on mallinnettu esimerkiksi ajoitettu kanban-sääntöjen avulla. Suunnittelija käyttää kanban-ajoituksen aikataulu ja lataa taso hallituksessa sekä työsolun pyydettäessä. Suunnittelija tarkkailee myös supermarket konsolidoitu toimitusaikataulun **toimitusaikataulun** sivulla. Yhtä tai useaa tuotantovirtojen voi mallintaa useiden alihankkijoiden ja voi olla useita kanban-säännöt, joiden avulla voidaan antaa saman tuotteen eri toimintojen kautta samaan paikkaan. Suunnittelija voi Muunna kanbanit vaihtoehtoinen kanban-sääntö, joka on alun perin luotu vaihtoehtoisen prosessin sisäisen tuotannon kanban aikatauluttaa uudelleen. Itse asiassa työsolua alihankintana luonne ei ole vaikutusta tuotantovirran. Sama toimintaperiaate koskee kahden rinnakkaisen sisäinen työsolun tai solujen alihankintana.   

Kuten muut toimintaa tuotantovirran, alihankinnasta voi kuluttaa ja tarjonta varastoiduilla, varastoiduilla (keskeneräinen työ \[KET\]), ja puolivalmiiden materiaalia ja tuotteita. Prosessien ajoitus ja Alihankintana hankittavien tehtävien suorittamista varten ovat kaikissa tapauksissa samat. Lisäksi nämä käsitellä samalla tavalla kuin sisäisen työn prosesseja.

## <a name="purchase-process-for-subcontracted-activities-services"></a>Alihankintana hankittavien tehtävien (palvelut) ostoprosessi
Fyysinen materiaalivirtojen, joka on rekisteröity kanban-työn edistymistä, esimerkiksi perustuu alihankinnasta ostoprosessi, käynnistää tai suorittaa. Taloushallinnon virtaus, esimerkiksi kustannusten, alihankintatöiden on sekundaarinen vuo, joka seuraa fyysistä kulkua. Samaan aikaan ostoprosessi on riippumaton prosessi, joka mahdollistaa manuaalisen muuttamisen ostoasiakirjoissa jokaisessa vaiheessa. Alihankintana hankittavien tehtävien ostoprosessi on:

1.  Luo ostosopimus. Ostosopimuksen palvelua varten luotuihin ja Tuotantovirran tehtävän yhteydessä.
2.  Luo ostotilaus. Oston vapautustilauksen luomista-palvelun ajoitettu kanban-töiden perusteella. Saman palvelun työt voidaan ryhmitellä ostotilauksen riveille päivän, viikon tai kuukauden mukaan. Milloin tahansa sen jälkeen, kun luodaan kanban-työt voidaan luoda ostotilausrivejä. Jopa jälkeen se voidaan luoda ostotilausrivejä. Yleensä tämä vaihtoehto valitaan, jos alihankkijalle tarjoaa muita ilmoittamatta, joka vastaanottaa alihankkijan tai kanbanit kanban-korttien perusteella. Tässä tapauksessa pienentää ostotilauksen ja laskun väliset poikkeamat.
3.  Luo kanban-kortit, materiaali ja valmistella jalostukseen alihankkijan lähettää keräysluettelon. Tuotantovirran, yksityiskohtainen mallinnus mukaan valmisteen tapahtuu prosessin toimintojen kanban-taulun keräysluettelo ja valmiste-funktion avulla. Vaihtoehtoisesti valmisteen tapahtuu siirtotöiden kanban-taulu keräysluettelo ja alku- tai käyttämällä. Varastoiduilla materiaalin molemmissa tapauksissa voidaan tukea WMS-keräyksen ja toimitus prosessi. Tarvittaessa voidaan luoda rahtikirjan.
4.  Luo kanban-käsittely-yksiköt ja kanban-kortit. Käsittelyn jälkeen kortit palautetaan alihankkijan. Kortit ovat yleensä toimituksen Huomautus, joka määrittää fyysinen materiaali, joka on toimitettu. Viittaus annetut palvelut ei tarvita. Kanban-taulun mukaan kanban-kortit on rekisteröity materiaalista tai asiakkaan tuotteen saapumisesta. (Tai prosessin toimintojen kanban-taulu-siirtotöiden kanban-taulun käytetään mallinnettu toiminnasta riippuen.).
5.  Luo vastaanoton neuvoa. Neuvoa-antava vastaanottoa voidaan käyttää korvaamaan pakkausluettelon vastaanotettujen palveluiden slip-asiakirja. Tiedotteiden vastaanoton voi luoda valmiin kanban-töiden alihankinnan tehtävän perusteella valitulta ajanjaksolta. Kunkin työn vastaanoton tiedotteiden luodaan liittyvät ostotilausriville. Neuvoa-antava vastaanotto voivat tulostaa ja lähettää vahvistuksen vastaanottamisesta alihankkijan.
6.  Luo lasku.

Prosessi päättyy, kun alihankkijan laskutetaan ajan. Laskun vastine on tehty tiedotteiden vastaanoton, jotka on luotu vastaan. Koska tiedotteiden vastaanoton edustavat tarkka fyysinen vastaanottamisesta, kolmisuuntainen vastaavuus on yksinkertaistettu.

## <a name="configuring-activities-for-subcontracting"></a>Määritetään tehtävät alihankinta
Seuraavissa osissa kuvataan tehtävät alihankinta määrittämisestä.

### <a name="subcontracted-services"></a>Alihankintapalvelujen

Maksu, jota käytetään toimintoperusteisen alihankinta on oltava tuote, joka on seuraavat ominaisuudet:

-   **Tuotetyyppi:** huolto
-   **Varastomalliryhmä:** ei-varastoitaviksi

Tämä vaatimus pakottaa ensimmäistä käyttöä-varastomallin ensimmäinen out (FIFO). **Huomautus:** tuotteiden kustannuslaskennan vaatii palvelun vakiokustannuksen määritellään. Toimittajan kanssa ostosopimus on pakollinen. Muutoin palvelu ei voi käyttää toimintoperusteisen alihankinta.

### <a name="subcontracted-process-activities"></a>Alihankinnan prosessin toimintojen

Alihankintana hankittavien tehtävien määrittää prosessin toimintaa, seuraavien ohjeiden mukaisesti.

1.  Määritä työsolun alihankintana. Määrittää työsolun alihankintana, sinun on luotava jokin resurssi **toimittajan** kirjoittaa ja liittää työsolun (resurssiryhmä). Runtime kustannusluokan, **suora ulkoistaminen** liitetään työsolua kustannusryhmän tyyppi. Kustannusluokkien asetukset ja määrää ei tarvita.
2.  Kun prosessin toiminta on luotu ja liittyvät alihankintatöiden soluun, palvelun tehtävälle on määritettävä ennen tuotantovirran versioon voidaan aktivoida. Olet tehnyt tämän vaiheen **tehtävän****tiedot** sivulla. Toimille, jotka liittyvät alihankintatöiden solun **-palvelun ehdot** pikavälilehdessä näkyy. Tässä pikavälilehdessä Lisää oletuspalvelua, joka koskee kaikkia tuotoksen nimikkeitä. Jos kortinlukijan osat edellyttävät erilaisia palveluja tai palvelun eri Laskentaparametrit (esimerkiksi eri Palvelusuhde), voit lisätä muita palveluita tehtävään.

## <a name="subcontracted-transfer-activities"></a>Alihankinnan siirtotehtäviä
Alihankintana hankittavien tehtävien, sen mukaan, mikä on määritetty siirto toiminta **rahdinkuljettaja** siirto toiminnan määrittäminen. Valittavissa ovat seuraavat vaihtoehdot:

-   **Lähettäjä** – tehtävä on alihankintana, jos siirto varastosta hallitsee toimittajan (kuten varaston ominaisuuden mukaan). Kaikki palvelut valittu ostosopimuksia fyysisen varastoinnin on oltava saman Toimittajatunnus.
-   **Vastaanottajan** – tehtävä on alihankintana, jos fyysisen varaston siirto hallitsee toimittajan (kuten varaston ominaisuuden mukaan). Kaikki palvelut valittu ostosopimuksia fyysisen varastoinnin on oltava saman Toimittajatunnus.
-   **Kantoaallon** – tehtävä on alihankintana myyjälle, joka tarjoaa palvelua. Kelvollisen liikenteenharjoittajan on luotava varastonhallintaa ja on oltava määritetty toimittajatili.

Prosessin toimintojen kuin sinun on määritettävä oletuspalvelua tehtävien siirtäminen alihankintana **palvelun ehdot** pikavälilehdessä **toimintaa****tiedot** sivulla.

## <a name="service-quantity-calculation"></a>Palvelumäärän laskenta
Palvelun kohteen on viittaus perustuu koko ostoprosessin. Tämän nimikkeen viittauksen mitataan palvelun mittayksikkö. Palvelut mitataan yleensä services (yksiköt) määrä tai aika. Voit laskea huoltomäärä rekisteröity kanban-töiden päättymisen perusteella seuraavilla tavoilla:

-   **Laskentaan, joka perustuu työpaikkojen määrän** – yksi kanban-työ on sama kuin *n* riippumatta tuotteen määrä, joka toimitetaan palvelun yksiköt. Lean-valmistuksen yksi työ vastaa yksi käsittely-yksikkö. Tätä laskentamenetelmää sovelletaan kaikkiin palveluihin, joissa on kiinteä hinta per käsittely-yksikkö. Tätä menetelmää sovelletaan tämän vuoksi yleensä siirtää toimintaa. Kuitenkin sitä käyttää myös prosessin toimintaan, jotka käsittelevät koko käsittely-yksiköt.
-   **Laskentaan, joka perustuu tuotteen määrä** – palvelun määrä on suhteessa tuotteen määrä, joka on suunniteltu tai toimitetaan. Kun toimitettavaa hyödykettä määrä lasketaan, virheelliset määrät voidaan joko vai jätetäänkö ne. Tätä laskentamenetelmää sovelletaan kaikissa tapauksissa, jossa palvelun Yksikköhinta, jalostettu tuote on sovittu.
-   **Laskentaan, joka perustuu tehtäväaika** – teoreettinen tehtäväajat lasketaan käsittelyaika toiminnan perusteella yhteensä käsitelty määrä ja tuotantokapasiteetin jalostetun tuotteen välinen suhde. Tätä laskentamenetelmää koskee palveluja, jotka on maksettu tunti ja on aika jalostettua tuotetta kohti vaihtelut.

## <a name="cost-accounting-of-subcontracted-services"></a>Kustannuslaskennan Alihankintapalvelujen
Neuvoa vastaanoton tai toimittajan tuotantovirran (toisin sanoen ostotilaus, joka on luotu alihankinnasta kanban-töiden perusteella) varten luotu ostotilaus-pakkausluettelo kirjataan, kun vastaanoton arvo on yhdistelty tuotantovirran ja KET-tileille. Laskujen poikkeamia käsitellään myös tuotannon virtaukseen. Alihankkijalle annettu työ kustannusluokka on otettu käyttöön. Tämän kustannusluokan käyttöön avoimia seuranta Alihankkijalle annettu työ, joka on kohdistettu KET ja kulutetun ajan arvo.  

Lean-valmistuksen kustannuslaskennan kauden lopussa jälkikustannuslaskennan laskee tuotteet, jotka on valmistettu tuotantovirran kustannuslaskennan ajan todellinen varianssit.

## <a name="modeling-transfers-as-subcontracted-activities"></a>Alihankintana hankittavien tehtävien muodossa siirtää mallinnus
Ihmiset katsovat usein kuljetus tuottamattoman ja se Lisää arvoa think. Kuitenkin verrattaessa alihankinta kustannus on sisäinen tuotantokustannuksia, kuljetuksen toiminnan kustannukset on otettava huomioon. Tuotantovirran, joka ulottuu useisiin sijainteihin ja vaatii kuljetuspalveluja olisi malli kuljetus kustannukset kustannus asiakkaalle tuotteiden osana. 

Toimintoperusteisen alihankinta lean-valmistuksen avulla voit integroida harjoittajien ja liikenne, siirtyä tuotantovirran sijainnit materiaalien ja tuotteiden toimittajat. Modeling siirto-toiminto, voit määrittää rahdinkuljettajan tai toimittaja. Toimintaa ja siirtotyön perustuu palvelu ja osto sopimuksen ja voit luoda ostotilauksia ja tiedotteiden vastaanoton, töiden varsinaisen siirron perusteella. Tämä toiminto on sama kuin alihankintana prosessin toimintojen toiminnallisuutta.  

Siksi nyt tukee tuoterakennelaskelmassa, jossa on kuljetuspalveluja, perustamista liittyvät ostotilaukset, integroitu vastaanoton rekisteröiminen ja kuljetusten integrointia toimintoja varten 365 Dynamics palvelun kustannukset kyselyjä tuotantovirran Jälkilaskelma.


