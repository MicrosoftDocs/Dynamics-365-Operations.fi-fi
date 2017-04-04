---
title: Tilauksen oletusasetukset mitat ja tuotevariantit
description: "Tilauksen oletusasetukset määrittävät toimipaikan ja varaston, josta nimikkeet ovat lähtöisin tai säilytetään, minimi-, maksimi-, monikerta- ja vakiomäärät, joita käytetään kaupankäynnissä tai varastonhallinnassa, sekä läpimenoaikojen, lopetusmerkin ja luvattujen tilausten menetelmässä. Tilauksen oletusasetuksia käytetään luotaessa ostotilauksia, myyntitilauksia, siirtotilauksia, varaston kirjauskansioita ja suunniteltujen tilausten luonnin pääsuunnittelussa. Tilauksen oletusasetukset voivat olla nimikekohtaisia, toimipaikkakohtaisia, tuotevarianttikohtaisia tai tuotedimensiokohtaisia."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: InventItemOrderSetup
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 223084
ms.assetid: fbfbcd7b-dc75-44ab-bffc-8bad576804a4
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: 60abaa69debd891b2fe2dd98184c0dab50b0bf9f
ms.lasthandoff: 03/29/2017


---

# <a name="default-order-settings-for-dimensions-and-product-variants"></a>Tilauksen oletusasetukset mitat ja tuotevariantit

Tilauksen oletusasetukset määrittävät toimipaikan ja varaston, josta nimikkeet ovat lähtöisin tai säilytetään, minimi-, maksimi-, monikerta- ja vakiomäärät, joita käytetään kaupankäynnissä tai varastonhallinnassa, sekä läpimenoaikojen, lopetusmerkin ja luvattujen tilausten menetelmässä. Tilauksen oletusasetuksia käytetään luotaessa ostotilauksia, myyntitilauksia, siirtotilauksia, varaston kirjauskansioita ja suunniteltujen tilausten luonnin pääsuunnittelussa. Tilauksen oletusasetukset voivat olla nimikekohtaisia, toimipaikkakohtaisia, tuotevarianttikohtaisia tai tuotedimensiokohtaisia.

Voit määrittää nimiketilausten oletusasetukset **Tilauksen oletusasetukset** -sivulla. Jos haluat avata tämän sivun, siirry **tuotetietojen hallinta**&gt;**tuotteiden**&gt;**vapautetut tuotteet**&gt; valitsemalla vapautetun tuotteen &gt; - **suunnitelma** tai *** hallita varaston *** toimintoruudun &gt;**tilauksen asetukset**&gt;**tilauksen oletusasetukset**.

## <a name="default-order-settings"></a>Tilauksen oletusasetukset
Tilauksen oletusasetuksia on kolme ostoille, myynnille ja varastolle. Tilauksen oletusasetuksia ostoille käytetään luotaessa:

-   Ostotilausrivit
-   Ostosopimuksen rivit
-   Tarjouspyynnön rivit
-   Ostoehdotusrivit
-   Tavaralähetyksen täydennysrivit
-   Suunnitellut ostotilaukset

Tilauksen oletusasetuksia myynnille käytetään luotaessa:

-   Myyntitilausrivit
-   Myyntisopimuksen rivit
-   Myyntitarjousrivit
-   Palautustilausrivit ja nimikkeiden korvaaminen -rivit
-   Kysynnän ennusteen rivit

Myyntitilauksen oletusasetuksia käytetään myös luotaessa:

-   Projektinimikkeen vaatimukset
-   Huoltotilauksen nimiketarpeet

Tilauksen oletusasetuksia varastolle käytetään luotaessa:

-   Varastokirjauskansiot
-   Siirtotilaukset
-   Suunnitellut siirtotilaukset

Varaston oletusasetukset ovat voimassa myös luotaessa:

-   Karanteenitilaukset
-   Laatutilaukset
-   Tuotantotilaukset
-   Tuoterakenteen rivit
-   Suunnitellut tuotantotilaukset

## <a name="full-definition-of-a-released-product"></a>Vapautetun tuotteen koko määritys
Kun luot tapahtuman, haluat määrittää rivin koko vapautetun tuotteen määritelmään ennen Dynamics 365 työvaiheiden yrittää tunnistaa tilauksen oletusasetukset. Vapautetun tuotteen koko määritelmä tarkoittaa sitä, että nimikenumero ja kaikki aktiiviset tuotedimensiot, konfiguraatio, koko, tyyli ja väri, kuten on määritetty tapahtuman. Esimerkiksi jos luot ostotilausrivin vapautetulle tuotevariantille manuaalisesti, sinun on määritettävä kaikki vaaditut tuotedimensiot ennen toimipaikan, varaston, määrän ja läpimenoajan näkymistä oletusarvoisesti tilausrivillä. 

Kaikkia tilauksen oletusasetusparametreja ei käytetä luotaessa tilausta tai kirjauskansion rivejä. Määrät ja läpimenoaikojen vain näyttää oletusarvon mukaan. Esimerkiksi kun inventoinnin kirjauskansion rivi, toimipaikan ja varaston näyttää oletuksena kun rivi luodaan. Luonnollisesti ei ole määrä oletusarvo tai useita tarkastuksia ja enimmäis suoritetaan, kun rivi luodaan tai päiväkirjan kirjaamisen. 

Järjestelmä yrittää aina löytää oletusarvoisen toimipisteen ja varaston kun tilauksen tai kirjauskansion rivi luodaan. Toimipaikkaa ei aina näytetä oletusarvon mukaan tilausasetuksista. Esimerkiksi myyntitilausta tai ostotilausta luotaessa tilausotsikon toimipistettä käytetään automaattisesti tilausriveillä. Luotaessa tuoterakenneriviä käytetään Tuoterakenteen otsikko sivuston. Kun sivusto on määritetty, sitä käytetään voit etsiä minkä tahansa sivuston, joka sitten voidaan käyttää oletusarvoksi varastolle toimipaikkakohtaiset Tilausasetukset. 

Oletusarvoista tilaustyyppiä osto ja varaston Toimitusaikoja voidaan ohittaa nimikkeen kattavuussäännöt mukaan **nimikkeen kattavuus** sivulla. Vaikka tuotanto ja toimitusaika siirron erojen ei salli tilauksen oletusasetukset, nimikkeen kattavuussäännöt salli sitä. Kuitenkin nimikkeen kattavuusasetuksia käytetään ainoastaan tarvesuunnittelussa luotaessa suunniteltua tuotantoa ja suunniteltuja siirtotilauksia, eikä niitä käytetä tuotanto- ja siirtotilausten luomiseen manuaalisesti. 

## <a name="default-order-settings-rules"></a>Tilauksen oletusasetusten säännöt
Voit määrittää yleiset tilauksen oletusasetukset ja haluamasi määrän tilauksen oletusasetusten sääntöjä, jotka ovat käytettävissä vain tietyillä ehdoilla, kuten toimipaikka tai tietty tuotedimensio tai tuotedimensioyhdistelmä. Varastokohtaisia tilausasetuksia ei voi määrittää.

### <a name="rank-in-default-order-settings"></a>Luokitus tilauksen oletusasetuksissa

Tilauksen oletusasetusten säännöt sisältävät luokituksia. Mitä korkeampi luokitus, sitä tärkeämpi sääntö on, joten sillä on suurempi prioriteetti ja sitä on käytettävä ennen alemman luokan sääntöjä. Yleisten tilausten oletusasetuksien luokitusarvo on nolla, jota ei voi muokata. Vain yhdellä säännöllä voi olla luokitus 0. Säännöillä voi olla sama luokitus, jos dimensioilla, joihin niitä sovelletaan, on eroja. Tästä on hyötyä mallinnettaessa toimipaikkakohtaisia tilausasetuksia. Luotaessa uusi tilauksen oletusasetussääntö, tilausarvojen, lopetusmerkin jne. arvot ovat samat kuin säännössä jolla on nollaluokitus, mutta ne voidaan ohittaa.

### <a name="default-order-settings-for-released-products"></a>Vapautettujen tuotteiden oletustilausasetukset

Voit määrittää yksittäisille vapautetuille tuotteille yleiset tilausasetukset tai toimipaikkakohtaiset tilausasetukset. Yleisten tilausasetusten luokitus on aina nolla. Jos määrität uusia myynnin, ostojen ja varaston tilausasetuksia samalla kertaa yhdessä, suosittelemme, että käytät **Tietonäkymä**-kohtaa **Tilauksen oletusasetukset ** -sivulla. Siirry Siirry tietonäkymään **asetukset** toimintoruudun &gt;**sivun asetukset**&gt;**muuttaa näkymää**&gt;**tiedot-näkymässä**.

### <a name="site-specific-order-settings"></a>Toimipaikkakohtaiset tilausasetukset

Voit luoda sivuston toimipaikkakohtaiset tilausasetukset valitsemalla **Uusi**. - **Tiedot-näkymässä**, täyttää sivuston **sovellettavat asetukset**&gt;**sivusto** kenttä. **Ruudukkonäkymä**-kohdassa täytä toimipaikka **Toimipaikka** -sarakkeeseen. Uusi sääntö saa automaattisesti uuden luokitusarvon, joka on suurempi kuin nolla. Voit luoda niin monta toimipaikkakohtaista sääntöä kuin on tarpeen ja määrittää toimipaikkakohtaisille säännöille saman luokituksen mallintaaksesi, että ne ovat yhtä tärkeitä. 

Jos olet **Tietonäkymä**-kohdassa et saat nimikkeelle luotujen sääntöjen yhteenvetoa. Yleisiä tietoja saat **Näytä/piilota luettelo** -painikkeella. Kun on annettu ei sivuston luomisen yhteydessä tilausrivi kaikenlaisia, Dynamics 365 työvaiheiden etsii sääntöä ei ole määritetty toimipaikka. Tämä voi auttaa selvittämään tilausrivin oletussivusto. Tätä toimipaikkaa käytetään etsittäessä toimipaikkakohtaista sääntöä, johon oletusvarasto on voitu määrittää. Tätä varastoa käytetään tilausrivillä.

### <a name="specific-order-settings-for-product-dimension"></a>Tuotedimension erityistilausasetukset

Voit määrittää tilausasetusten säännöt, joita käytetään aktiiviseen tuotedimensioon tai aktiiviseen tuotedimensioyhdistelmään. Jos tuotedimension kenttä on jätetty tyhjäksi, sääntö koskee kaikkia tuotedimension arvoja. 

Tarkastellaan seuraavaa esimerkkituotetta:

|                                                     |                                         |
|-----------------------------------------------------|-----------------------------------------|
| **Product name**                                    | Valosähköanturi                    |
| **Item number**                                     | XW56                                    |
| **Konfiguraatio** (käytetään mallinnettaessa valotyyppiä) | C1: näkyvä punainen valo, C2: infrapunavalo |
| **Tyyli** (käytetään mallinnettaessa teknistä versiota)  | R1, R2, R3                              |

Tässä esimerkissä oletetaan että tuote on hankittu eikä sitä ole valmistettu. Oletamme lisäksi että konfiguraatiota C1 käytetään useammin, joten sillä on lyhyemmät läpimenoajat. 

Luo seuraavat tilauksen oletusasetukset tämän skenaarion mallintamiseksi.

| Sijoitus | Sivusto | Konfiguraatio | Tyyli | Osto: ohita oletusasetukset | Oston läpimenoaika | Osto: estetty | Myynti: ohita oletusasetukset | Myynti: pysäytetty |
|------|------|---------------|-------|--------------------------------------|--------------------|--------------------|-----------------------------------|-----------------|
| 10   |      | C1            |       | Kyllä                                  | 2                  |                    |                                   |                 |
| 0    |      |               |       |                                      | 5                  |                    |                                   |                 |

Kun suunniteltu ostotilaus tai ostotilausrivi luodaan XW56:lle, konfiguraatio C1, versiosta tai toimipaikasta riippumatta, johon rivi on tehty, läpimenoaikana pidetään 2. Oletetaan, että kaikki versiot paitsi R3 on pysäytetty.

Voit luoda seuraavat Tilauksen oletusasetusten säännöt.

| Sijoitus | Sivusto | Konfiguraatio | Tyyli | Osto: ohita oletusasetukset | Oston läpimenoaika | Osto: estetty | Myynti: ohita oletusasetukset | Myynti: pysäytetty |
|------|------|---------------|-------|--------------------------------------|--------------------|--------------------|-----------------------------------|-----------------|
| 20   |      |               | R2    | Kyllä                                  |                    | Kyllä                | Kyllä                               | Kyllä             |
| 20   |      |               | R1    | Kyllä                                  |                    | Kyllä                | Kyllä                               | Kyllä             |
| 10   |      | C1            |       | Kyllä                                  | 2                  |                    |                                   |                 |
| 0    |      |               |       |                                      | 5                  |                    |                                   |                 |

Kahdella vanhojen versioiden lopettamissäännöllä on sama luokittelu, eli ne ovat yhtä tärkeitä. Kummallakin on korkeampi luokitus kuin konfiguraation C1 säännöllä, mikä tarkoittaa, että ne ohittavat konfiguraation C1 säännön. 

Tässä esimerkissä selitetään luokituksen tarve. Jos ostotilaus luodaan konfiguraatiolle C1 ja versiolle R2 ja luokitus puuttuu, kaksi R2 ja C1 -konfiguraatiolle määritettyä sääntöä ovat moniselitteisiä. Moniselitteisyyden ratkaisemiseksi Dynamics 365 for Operations etsii sääntöjä laskevassa luokitusjärjestyksessä ja käyttää ensimmäisen käytettävissä olevaa sääntöä. Tässä esimerkissä, luotaessa ostotilausriviä konfiguraatiolle C1 ja versiolle R2, käyttäjä saa varoitusviestin, että nimike on pidossa ja tämä aiheutuu version arvosta. Jos konfiguraatiota koskeva luokitus on korkeampi kuin version sääntö, konfiguraation C1 ja version R2 ostotilausrivin luominen on onnistunut eikä "nimike on pidossa" viestiä anneta käyttäjälle. 

Ota huomioon seuraavat tilauksen oletusasetusten säännöt.

| Sijoitus | Sivusto | Konfiguraatio | Tyyli | Oletustoimipaikka | Oletusvarasto | Osto: Ohita oletusvarastodimensio | Ostovarasto |
|------|------|---------------|-------|--------------|-------------------|------------------------------------------------|--------------------|
| 20   | 2    |               |       |              |                   | Kyllä                                            | 22                 |
| 10   |      | C1            |  R2   |  2           |  21               |                                                |                    |
| 0    |      |               |       | 1            | 11                |                                                |                    |

Järjestelmän käy läpi sääntöjoukon kahdesti määrittääkseen toimipisteen ja varaston. Kun ostotilausrivi on luotu kokoonpano C1, R2, tyyli sivusto määritetään sija 10 säännön perusteella. Sitten järjestelmä etsii sivuston 2 sääntö määrittää varaston. Sääntö 20 löytyy ja koska sen luokitus on suurempi, ostotilausrivillä on varasto 22 eikä 21. 

Yleisen periaatteen mukaisesti erityissäännöt ja tärkeämpien dimensioiden säännöt saavat korkeamman luokituksen ja yleiset säännöt saavat alemman luokituksen. 

Sääntö, jonka luokitus on nolla, toimii turvaverkkona. Jos muut säännöt eivät päde, käytetään nollasäännön mukaisia tilauksen oletusasetukset. 

Koska luokitusnumero on tärkeä, **Tilauksen oletusasetukset **-toimintoruudussa on toimintoja säännön siirtämiseksi ylös tai alas tai säännön uudelleennumeroimiseksi, niin että ne etenevät aina 10 kerrallaan. 

Vapautetulla tuotteella voi olla useita luotuja sääntöjä. Saat selkeämmän käsityksen siitä, mikä sääntö on hallitseva ja miksi sitä tarvitaan, kohdasta **Ruudukkonäkymä** ** Tilauksen oletusasetukset** -sivulla. Otat ruudukkonäkymän avulla **asetukset** toimintoruudun &gt;**sivun asetukset**&gt;**muuttaa näkymää**&gt;**ruudukkonäkymässä**. Ruudukossa näytettävien sarakkeiden määrä voi olla hyvin suuri, erityisesti myynti- ja varasto-välilehdillä. Voit rajoittaa ruudukossa näkyvien sarakkeiden määrä, ryhmien sarakkeiden on piilotettu vai näkyvissä painikkeiden avulla **tilauksen oletusasetukset**&gt;**sarakkeen näyttö** valikosta.

### <a name="specific-order-settings-for-released-product-variant"></a>Vapautetun tuotevariantin erityistilausasetukset

Jos tilauksen oletusasetusten sääntöjärjestelmä on liian hankala, on mahdollista määrittää tilauksen oletusasetukset jokaiselle tuotevariantille. Seuraavissa esimerkeissä esitetään, miten tämä etsii tuotetta ja edellä kuvattuja tapauksia.

| Sijoitus | Sivusto | Konfiguraatio | Tyyli | Osto: ohita oletusasetukset | Oston läpimenoaika | Osto: estetty | Myynti: ohita oletusasetukset | Myynti: pysäytetty |
|------|------|---------------|-------|--------------------------------------|--------------------|--------------------|-----------------------------------|-----------------|
| 10   |      | C2            | R3    | Kyllä                                  | 5                  |                    |                                   |                 |
| 10   |      | C2            | R2    | Kyllä                                  | 5                  | Kyllä                | Kyllä                               | Kyllä             |
| 10   |      | C2            | R1    | Kyllä                                  | 5                  | Kyllä                | Kyllä                               | Kyllä             |
| 10   |      | C1            | R3    | Kyllä                                  | 2                  |                    |                                   |                 |
| 10   |      | C1            | R2    | Kyllä                                  | 2                  | Kyllä                | Kyllä                               | Kyllä             |
| 10   |      | C1            | R1    | Kyllä                                  | 2                  | Kyllä                | Kyllä                               | Kyllä             |
| 0    |      |               |       |                                      | 5                  |                    |                                   |                 |

Luokituksella ei tällöin ole todellista merkitystä, joten voit piilottaa sen. Ratkaisu aiheuttaa mahdollisesti ylläpito-ongelmia. Haluat ehkä kuitenkin käyttää näitä asetuksia, jos olet harkinnut integrointia tuotteen elinkaaren hallintajärjestelmään (PLM).


