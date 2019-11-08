---
title: Tilauksen oletusasetukset dimensioille ja tuotevarianteille
description: Tilauksen oletusasetukset määrittävät toimipaikan ja varaston, josta nimikkeet ovat lähtöisin tai säilytetään, minimi-, maksimi-, monikerta- ja vakiomäärät, joita käytetään kaupankäynnissä tai varastonhallinnassa, sekä läpimenoaikojen, lopetusmerkin ja luvattujen tilausten menetelmässä.
author: roxanadiaconu
manager: AnnBe
ms.date: 11/03/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventItemOrderSetup
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 223084
ms.assetid: fbfbcd7b-dc75-44ab-bffc-8bad576804a4
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: d13aabfb36e8af4a32de8bc8949e8b164075532a
ms.sourcegitcommit: d37fb09101c30858bcb975931b3d8f947d72017b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/10/2019
ms.locfileid: "2570699"
---
# <a name="default-order-settings-for-dimensions-and-product-variants"></a>Dimensioiden ja tuotevarianttien oletustilausasetukset

[!include [banner](../includes/banner.md)]

Tilauksen oletusasetukset Dynamics 365 Supply Chain Managementissa määrittävät toimipaikan ja varaston, josta nimikkeet ovat lähtöisin tai säilytetään, minimi-, maksimi-, monikerta- ja vakiomäärät, joita käytetään kaupankäynnissä tai varastonhallinnassa, sekä läpimenoaikojen, lopetusmerkin ja luvattujen tilausten menetelmässä. Tilauksen oletusasetuksia käytetään luotaessa ostotilauksia, myyntitilauksia, siirtotilauksia, varaston kirjauskansioita ja suunniteltujen tilausten luonnin pääsuunnittelussa. Tilauksen oletusasetukset voivat olla nimikekohtaisia, toimipaikkakohtaisia, tuotevarianttikohtaisia tai tuotedimensiokohtaisia.

Voit määrittää nimiketilausten oletusasetukset **Tilauksen oletusasetukset** -sivulla. Voit avata sivun kohdassa **Tuotetietojen hallinta** &gt; **Tuotteet** &gt; **Vapautetut tuotteet** &gt; **Valitse vapautettu tuote** &gt; **Suunnitelma**- tai **Varastonhallinta** -toimintoruutu &gt; **Tilausasetukset** &gt; **Tilauksen oletusasetukset**.

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
Kun luot tapahtumaa, vapautetun tuotteen koko määritelmä on määritettävä rivillä, ennen kuin Supply Chain Management yrittää tunnistaa tilauksen oletusasetukset. Vapautetun tuotteen koko määritelmä tarkoittaa sitä, että nimikenumero ja kaikki aktiiviset tuotedimensiot, kuten konfiguraatio, koko, tyyli ja väri on määritetty tapahtumassa. Esimerkiksi jos luot ostotilausrivin vapautetulle tuotevariantille manuaalisesti, sinun on määritettävä kaikki vaaditut tuotedimensiot ennen toimipaikan, varaston, määrän ja läpimenoajan näkymistä oletusarvoisesti tilausrivillä. 

Kaikkia tilauksen oletusasetusparametreja ei käytetä luotaessa tilausta tai kirjauskansion rivejä. Määrät ja läpimenoaikojen näytetään vain oletusarvon mukaan. Esimerkiksi kun lasketaan kirjauskansion riviä, vain toimipaikka ja varasto näytetään oletuksena, kun rivi luodaan. Luonnollisesti määrien oletusarvojen määrityksiä tai tarkistuksia useista nimikkeitä tai minimeistä ei suoriteta, kun rivi luodaan tai kun päiväkirjaan kirjataan. 

Järjestelmä yrittää aina löytää oletusarvoisen toimipisteen ja varaston kun tilauksen tai kirjauskansion rivi luodaan. Toimipaikkaa ei aina näytetä oletusarvon mukaan tilausasetuksista. Esimerkiksi myyntitilausta tai ostotilausta luotaessa tilausotsikon toimipistettä käytetään automaattisesti tilausriveillä. Luotaessa tuoterakenneriviä käytetään tuoterakenteen otsikon toimipaikkaa. Kun toimipaikka on määritetty, sitä käytetään etsimään toimipaikkakohtaisia tilausasetuksia, joita sitten voidaan käyttää varaston oletusarvoina. 

Oletusarvoiset tilaustyyppi, oston ja varaston läpimenoaika voidaan ohittaa nimikkeen kattavuussääntöjen mukaan **Nimikkeen kattavuus** -sivulla. Vaikka tilauksen oletusasetukset eivät salli tuotannon ja siirron läpimenoajan eroa, nimikkeen kattavuussäännöt sallivat sen. Kuitenkin nimikkeen kattavuusasetuksia käytetään ainoastaan tarvesuunnittelussa luotaessa suunniteltua tuotantoa ja suunniteltuja siirtotilauksia, eikä niitä käytetä tuotanto- ja siirtotilausten luomiseen manuaalisesti. 

## <a name="default-order-settings-rules"></a>Tilauksen oletusasetusten säännöt
Voit määrittää yleiset tilauksen oletusasetukset ja haluamasi määrän tilauksen oletusasetusten sääntöjä, jotka ovat käytettävissä vain tietyillä ehdoilla, kuten toimipaikka tai tietty tuotedimensio tai tuotedimensioyhdistelmä. Varastokohtaisia tilausasetuksia ei voi määrittää.

### <a name="rank-in-default-order-settings"></a>Luokitus tilauksen oletusasetuksissa

Tilauksen oletusasetusten säännöt sisältävät luokituksia. Mitä korkeampi luokitus, sitä tärkeämpi sääntö on, joten sillä on suurempi prioriteetti ja sitä on käytettävä ennen alemman luokan sääntöjä. Yleisten tilausten oletusasetuksien luokitusarvo on nolla, jota ei voi muokata. Vain yhdellä säännöllä voi olla luokitus 0. Säännöillä voi olla sama luokitus, jos dimensioilla, joihin niitä sovelletaan, on eroja. Tästä on hyötyä mallinnettaessa toimipaikkakohtaisia tilausasetuksia. Luotaessa uusi tilauksen oletusasetussääntö, tilausarvojen, lopetusmerkin jne. arvot ovat samat kuin säännössä jolla on nollaluokitus, mutta ne voidaan ohittaa.

### <a name="default-order-settings-for-released-products"></a>Vapautettujen tuotteiden oletustilausasetukset

Voit määrittää yksittäisille vapautetuille tuotteille yleiset tilausasetukset tai toimipaikkakohtaiset tilausasetukset. Yleisten tilausasetusten luokitus on aina nolla. Jos määrität uusia myynnin, ostojen ja varaston tilausasetuksia samalla kertaa yhdessä, suosittelemme, että käytät **Tietonäkymä**-kohtaa **Tilauksen oletusasetukset** -sivulla. Voit siirtyä tietonäkymään **Asetukset**-toimintoruudussa &gt; **Sivun asetukset** &gt; **Vaihda näyttö** &gt; **Tietonäkymä**.

### <a name="site-specific-order-settings"></a>Toimipaikkakohtaiset tilausasetukset

Voit luoda sivuston toimipaikkakohtaiset tilausasetukset valitsemalla **Uusi**. **Tietonäkymä**-kohdassa täytä toimipaikka **Asetukset käytössä** &gt; **Toimipaikka**-kentässä. **Ruudukkonäkymä**-kohdassa täytä toimipaikka **Toimipaikka** -sarakkeeseen. Uusi sääntö saa automaattisesti uuden luokitusarvon, joka on suurempi kuin nolla. Voit luoda niin monta toimipaikkakohtaista sääntöä kuin on tarpeen ja määrittää toimipaikkakohtaisille säännöille saman luokituksen mallintaaksesi, että ne ovat yhtä tärkeitä. 

Jos olet **Tietonäkymä**-kohdassa et saat nimikkeelle luotujen sääntöjen yhteenvetoa. Yleisiä tietoja saat **Näytä/piilota luettelo** -painikkeella. Kun tilausrivi luodaan eikä sille anneta toimipaikkaa, Supply Chain Management etsii sääntöä, jossa toimipaikkaa ei ole määritetty. Tämä voi auttaa määrittämään tilausrivin oletustoimipaikan. Tätä toimipaikkaa käytetään etsittäessä toimipaikkakohtaista sääntöä, johon oletusvarasto on voitu määrittää. Tätä varastoa käytetään tilausrivillä.

### <a name="specific-order-settings-for-product-dimension"></a>Tuotedimension erityistilausasetukset

Voit määrittää tilausasetusten säännöt, joita käytetään aktiiviseen tuotedimensioon tai aktiiviseen tuotedimensioyhdistelmään. Jos tuotedimension kenttä on jätetty tyhjäksi, sääntö koskee kaikkia tuotedimension arvoja. 

Tarkastellaan seuraavaa esimerkkituotetta:

|                                                     |                                         |
|-----------------------------------------------------|-----------------------------------------|
| **Tuotteen nimi**                                    | Valosähköanturi                    |
| **Nimiketunnus**                                     | XW56                                    |
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

Tässä esimerkissä selitetään luokituksen tarve. Jos ostotilaus luodaan konfiguraatiolle C1 ja versiolle R2 ja luokitus puuttuu, kaksi R2 ja C1 -konfiguraatiolle määritettyä sääntöä ovat moniselitteisiä. Supply Chain Management ratkaisee moniselitteisyyden etsimällä sääntöjä laskevassa luokitusjärjestyksessä ja käyttää ensimmäistä käytettävissä olevaa sääntöä. Tässä esimerkissä, luotaessa ostotilausriviä konfiguraatiolle C1 ja versiolle R2, käyttäjä saa varoitusviestin, että nimike on pidossa ja tämä aiheutuu version arvosta. Jos konfiguraatiota koskeva luokitus on korkeampi kuin version sääntö, konfiguraation C1 ja version R2 ostotilausrivin luominen on onnistunut eikä "nimike on pidossa" viestiä anneta käyttäjälle. 

Ota huomioon seuraavat tilauksen oletusasetusten säännöt.

| Sijoitus | Sivusto | Konfiguraatio | Tyyli | Oletustoimipaikka | Oletusvarasto | Osto: Ohita oletusvarastodimensio | Ostovarasto |
|------|------|---------------|-------|--------------|-------------------|------------------------------------------------|--------------------|
| 20   | 2    |               |       |              |                   | Kyllä                                            | 22                 |
| 10   |      | C1            |  R2   |  2           |  21               |                                                |                    |
| 0    |      |               |       | 1            | 11                |                                                |                    |

Järjestelmän käy läpi sääntöjoukon kahdesti määrittääkseen toimipisteen ja varaston. Kun konfiguraation C1 versio R2 ostotilausrivi luodaan, toimipaikka määritetään luokituksen 10 säännön perusteella. Järjestelmä etsii sääntöä toimipaikalle 2 määrittääkseen varaston. Sääntö 20 löytyy ja koska sen luokitus on suurempi, ostotilausrivillä on varasto 22 eikä 21. 

Yleisen periaatteen mukaisesti erityissäännöt ja tärkeämpien dimensioiden säännöt saavat korkeamman luokituksen ja yleiset säännöt saavat alemman luokituksen. 

Sääntö, jonka luokitus on nolla, toimii turvaverkkona. Jos muut säännöt eivät päde, käytetään nollasäännön mukaisia tilauksen oletusasetukset. 

Koska luokitusnumero on tärkeä, **Tilauksen oletusasetukset**-toimintoruudussa on toimintoja säännön siirtämiseksi ylös tai alas tai säännön uudelleennumeroimiseksi, niin että ne etenevät aina 10 kerrallaan. 

Vapautetulla tuotteella voi olla useita luotuja sääntöjä. Saat selkeämmän käsityksen siitä, mikä sääntö on hallitseva ja miksi sitä tarvitaan, kohdasta **Ruudukkonäkymä** **Tilauksen oletusasetukset** -sivulla. Voit ottaa ruudukkonäkymän käyttöön kohdassa **Asetukset**-toimintoruutu &gt; **Sivun asetukset** &gt; **Vaihda näkymää** &gt; **Ruudukkonäkymä**. Ruudukossa näytettävien sarakkeiden määrä voi olla hyvin suuri, erityisesti myynti- ja varasto-välilehdillä. Näytettävien sarakkeiden enimmäismäärää ruudukossa voidaan rajoittaa piilottamalla tai näyttämällä sarakeryhmiä painikkeilla kohdassa **Tilauksen oletusasetukset** &gt; **Sarakkeen näyttö** -valikko.

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



