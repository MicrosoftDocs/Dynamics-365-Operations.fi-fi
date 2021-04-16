---
title: Tilauksen oletusasetukset dimensioille ja tuotevarianteille
description: Tilauksen oletusasetukset määrittävät toimipaikan ja varaston, josta nimikkeet ovat lähtöisin tai säilytetään, minimi-, maksimi-, monikerta- ja vakiomäärät, joita käytetään kaupankäynnissä tai varastonhallinnassa, sekä läpimenoaikojen, lopetusmerkin ja luvattujen tilausten menetelmässä.
author: t-benebo
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventItemOrderSetup, InventItemIdLookupByDefaultOrderSetting, EcoResProductReleasedStoppedAllChartPart, UnitTestPartitions
audience: Application User
ms.reviewer: kamaybac
ms.custom: 223084
ms.assetid: fbfbcd7b-dc75-44ab-bffc-8bad576804a4
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: benebotg
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 73e6a45dedba0831c15d70ad35676c62a14acabb
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/01/2021
ms.locfileid: "5809155"
---
# <a name="default-order-settings-for-dimensions-and-product-variants"></a>Dimensioiden ja tuotevarianttien oletustilausasetukset

[!include [banner](../includes/banner.md)]

Tilauksen oletusasetukset Dynamics 365 Supply Chain Managementissa määrittävät toimipaikan ja varaston, josta nimikkeet ovat lähtöisin tai säilytetään, minimi-, maksimi-, monikerta- ja vakiomäärät, joita käytetään kaupankäynnissä tai varastonhallinnassa, sekä läpimenoaikojen, lopetusmerkin ja luvattujen tilausten menetelmässä. Tilauksen oletusasetuksia käytetään luotaessa ostotilauksia, myyntitilauksia, siirtotilauksia, varaston kirjauskansioita ja suunniteltujen tilausten luonnin pääsuunnittelussa. Tilauksen oletusasetukset voivat olla nimikekohtaisia, toimipaikkakohtaisia, tuotevarianttikohtaisia tai tuotedimensiokohtaisia.

Voit määrittää tuotteen oletustilausasetukset noudattamalla seuraavia ohjeita.

1. Siirry kohtaan **Tuotetietojen hallinta** &gt; **Tuotteet** &gt; **Vapautetut tuotteet**.
1. Valitse asiaankuuluva tuote ruudukossa.
1. Avaa valitun tuotteen **Oletustilausasetukset** -sivu toimimalla toimintoruudussa seuraavasti:

    - Valitse **Suunnittele**-välilehden **Tilauksen asetukset** -ryhmästä **oletustilaus asetukset**.
    - Valitse **Hallitse varastoa** -välilehden **Tilauksen asetukset** -ryhmästä **oletustilaus asetukset**.

1. Määritä asetukset tämän ohjeaiheen muissa kohdissa kuvatulla tavalla.

## <a name="default-order-settings"></a>Tilauksen oletusasetukset

Tilauksen oletusasetuksia on kolme ostoille, myynnille ja varastolle. Tilauksen oletusasetuksia ostoille käytetään luotaessa:

- Ostotilausrivit
- Ostosopimuksen rivit
- Tarjouspyynnön rivit
- Ostoehdotusrivit
- Lähetyksen täydennysrivit (osittain tuettu, katso huomautus)
- Suunnitellut ostotilaukset

> [!NOTE]
> Lähetyksen täydennystilausriveihin pätevät **Oletusarvoiset tilausasetukset** -sivun **Ostotilaus**-pikavälilehdessä vain **Oletussijainti** -kenttä, **Oletusvarasto**-kenttä ja **Keskeytetty**-valintaikkuna.

Tilauksen oletusasetuksia myynnille käytetään luotaessa:

- Myyntitilausrivit
- Myyntisopimuksen rivit
- Myyntitarjousrivit
- Palautustilausrivit ja nimikkeiden korvaaminen -rivit
- Kysynnän ennusteen rivit

Myyntitilauksen oletusasetuksia käytetään myös luotaessa:

- Projektinimikkeen vaatimukset
- Huoltotilauksen nimiketarpeet

Tilauksen oletusasetuksia varastolle käytetään luotaessa:

- Varastokirjauskansiot
- Siirtotilaukset
- Suunnitellut siirtotilaukset

Varaston oletusasetukset ovat voimassa myös luotaessa:

- Karanteenitilaukset
- Laatutilaukset
- Tuotantotilaukset
- Tuoterakenteen rivit
- Suunnitellut tuotantotilaukset

## <a name="full-definition-of-a-released-product"></a>Vapautetun tuotteen koko määritys

Kun luot tapahtumaa, vapautetun tuotteen koko määritelmä on määritettävä rivillä niin, että Supply Chain Management yrittää tunnistaa tilauksen oletusasetukset. Vapautetun tuotteen koko määritelmässä nimikenumero ja kaikki aktiiviset tuotedimensiot, kuten konfiguraatio, koko, tyyli ja väri on määritetty tapahtumassa. Esimerkiksi jos luot ostotilausrivin vapautetulle tuotevariantille manuaalisesti, sinun on määritettävä kaikki vaaditut tuotedimensiot ennen toimipaikan, varaston, määrän ja läpimenoajan näkymistä oletusarvoisesti tilausrivillä. 

Kaikkia tilauksen oletusasetusparametreja ei käytetä luotaessa tilausta tai kirjauskansion rivejä. Määrät ja läpimenoaikojen näytetään vain oletusarvon mukaan. Esimerkiksi kun lasketaan kirjauskansion riviä, vain toimipaikka ja varasto näytetään oletuksena, kun rivi luodaan. Tästä syystä oletusmäärää tai tarkistuksia useista nimikkeitä tai minimeistä ei suoriteta, kun rivi luodaan tai kun päiväkirjaan kirjataan. 

Järjestelmä yrittää aina löytää oletusarvoisen toimipisteen ja varaston kun tilauksen tai kirjauskansion rivi luodaan. Toimipaikkaa ei aina näytetä oletusarvon mukaan tilausasetuksista. Esimerkiksi myyntitilausta tai ostotilausta luotaessa tilausotsikon toimipistettä käytetään automaattisesti tilausriveillä. Luotaessa tuoterakenneriviä käytetään tuoterakenteen otsikon toimipaikkaa. Kun toimipaikka on määritetty, sitä käytetään etsimään toimipaikkakohtaisia tilausasetuksia, joita sitten voidaan käyttää varaston oletusarvoina. 

Oletusarvoiset tilaustyyppi, oston ja varaston läpimenoaika voidaan ohittaa nimikkeen kattavuussääntöjen mukaan **Nimikkeen kattavuus** -sivulla. Vaikka tilauksen oletusasetukset eivät salli tuotannon ja siirron läpimenoajan eroa, nimikkeen kattavuussäännöt sallivat sen. Kuitenkin nimikkeen kattavuusasetuksia käytetään ainoastaan tarvesuunnittelussa luotaessa suunniteltua tuotantoa ja suunniteltuja siirtotilauksia, eikä niitä käytetä tuotanto- ja siirtotilausten luomiseen manuaalisesti. 

## <a name="default-order-settings-rules"></a>Tilauksen oletusasetusten säännöt

Voit määrittää yleiset tilauksen oletusasetukset ja haluamasi määrän tilauksen oletusasetusten sääntöjä, jotka ovat käytettävissä vain tietyillä ehdoilla, kuten toimipaikka tai tietty tuotedimensio tai tuotedimensioyhdistelmä. Varastokohtaisia tilausasetuksia ei voi määrittää.

### <a name="rank-in-default-order-settings"></a>Luokitus tilauksen oletusasetuksissa

Tilauksen oletusasetusten säännöt sisältävät luokituksia. Mitä korkeampi luokitus, sitä tärkeämpi sääntö on, joten sillä on suurempi prioriteetti ja sitä on käytettävä ennen alemman luokan sääntöjä. Yleisten tilausten oletusasetuksien luokitusarvo on nolla, jota ei voi muokata. Vain yhdellä säännöllä voi olla luokitus 0. Säännöillä voi olla sama luokitus, jos dimensioilla, joihin niitä sovelletaan, on eroja. Tästä on hyötyä mallinnettaessa toimipaikkakohtaisia tilausasetuksia. Luotaessa uusi tilauksen oletusasetussääntö, tilausarvojen, lopetusmerkin jne. arvot ovat samat kuin säännössä jolla on nollaluokitus, mutta ne voidaan ohittaa.

### <a name="default-order-settings-for-released-products"></a>Vapautettujen tuotteiden oletustilausasetukset

Voit määrittää yksittäisille vapautetuille tuotteille yleiset tilausasetukset tai toimipaikkakohtaiset tilausasetukset. Yleisten tilausasetusten luokitus on aina nolla. Jos määrität uusia myynnin, ostojen ja varaston tilausasetuksia samalla kertaa yhdessä, suosittelemme, että käytät **Tietonäkymä**-kohtaa **Tilauksen oletusasetukset** -sivulla. Voit siirtyä tietonäkymään valitsemalla **Asetukset** &gt; **Sivun asetukset** &gt; **Vaihda näyttö** &gt; **Tietonäkymä**.

### <a name="site-specific-order-settings"></a>Toimipaikkakohtaiset tilausasetukset

Voit luoda sivuston toimipaikkakohtaiset tilausasetukset valitsemalla **Uusi**. **Tietonäkymä**-kohdassa täytä toimipaikka **Asetukset käytössä**-osan **Toimipaikka**-kentässä. **Ruudukkonäkymä**-kohdassa syötä toimipaikka **Toimipaikka** -sarakkeeseen. Uudelle säännölle määritetään automaattisesti uusi sijoitusarvo, joka on suurempi kuin 0 (nolla). Voit luoda tarvitsemasi määrän sivustokohtaisia sääntöjä. Jos haluat osoittaa, että ne ovat yhtä tärkeitä, voit määrittää saman sijoitusarvon kaikille toimipaikkakohtaisille säännöille.

Jos olet **Tietonäkymä**-kohdassa et saat nimikkeelle luotujen sääntöjen yhteenvetoa. Yleisiä tietoja saat **Näytä/piilota luettelo** -painikkeella. Kun tilausrivi luodaan eikä sille anneta toimipaikkaa, Supply Chain Management etsii sääntöä, jossa toimipaikkaa ei ole määritetty. Tämä voi auttaa määrittämään tilausrivin oletustoimipaikan. Tätä toimipaikkaa käytetään etsittäessä toimipaikkakohtaista sääntöä, johon oletusvarasto on voitu määrittää. Tätä varastoa käytetään tilausrivillä.

### <a name="specific-order-settings-for-product-dimension"></a>Tuotedimension erityistilausasetukset

Voit määrittää tilausasetusten säännöt, joita käytetään aktiiviseen tuotedimensioon tai aktiiviseen tuotedimensioyhdistelmään. Jos tuotedimension kenttä on tyhjä, sääntö koskee kaikkia tuotedimension arvoja. 

Tarkastellaan seuraavaa esimerkkituotetta:

|                                                     |                                         |
|-----------------------------------------------------|-----------------------------------------|
| **Tuotteen nimi**                                    | Valosähköanturi                    |
| **Nimiketunnus**                                     | XW56                                    |
| **Konfiguraatio** (käytetään mallinnettaessa valotyyppiä) | C1: näkyvä punainen valo, C2: infrapunavalo |
| **Versio** | V1, V2, V3                              |

Tässä esimerkissä oletetaan että tuote on hankittu eikä sitä ole valmistettu. Oletamme lisäksi että konfiguraatiota C1 käytetään useammin, joten sillä on lyhyemmät läpimenoajat. 

Luo seuraavat tilauksen oletusasetukset tämän skenaarion mallintamiseksi.

| Sijoitus | Toimipaikka | Määritys | Versio | Osto: ohita oletusasetukset | Oston läpimenoaika | Osto: estetty | Myynti: ohita oletusasetukset | Myynti: pysäytetty |
|------|------|---------------|-------|--------------------------------------|--------------------|--------------------|-----------------------------------|-----------------|
| 10   |      | C1            |       | Kyllä                                  | 2                  |                    |                                   |                 |
| 0    |      |               |       |                                      | 5                  |                    |                                   |                 |

Kun suunniteltu ostotilaus tai ostotilausrivi luodaan nimikkeelle XW56, konfiguraatio C1, versiosta tai toimipaikasta riippumatta, johon rivi on tehty, läpimenoaikana pidetään 2. Oletetaan, että kaikki versiot paitsi V3 on pysäytetty.

Voit luoda seuraavat Tilauksen oletusasetusten säännöt.

| Sijoitus | Toimipaikka | Määritys | Versio | Osto: ohita oletusasetukset | Oston läpimenoaika | Osto: estetty | Myynti: ohita oletusasetukset | Myynti: pysäytetty |
|------|------|---------------|-------|--------------------------------------|--------------------|--------------------|-----------------------------------|-----------------|
| 20   |      |               | V2    | Kyllä                                  |                    | Kyllä                | Kyllä                               | Kyllä             |
| 20   |      |               | V1    | Kyllä                                  |                    | Kyllä                | Kyllä                               | Kyllä             |
| 10   |      | C1            |       | Kyllä                                  | 2                  |                    |                                   |                 |
| 0    |      |               |       |                                      | 5                  |                    |                                   |                 |

Vanhojen versioiden pysäyttämisen kaksi sääntöä ovat samat. Siksi ne ovat yhtä tärkeitä. Koska kummallakin on korkeampi luokitus kuin konfiguraation C1 säännöllä, ne ohittavat konfiguraation C1 säännön. 

Tässä esimerkissä selitetään luokituksen tarve. Jos luokitusta ei käytetä, kun ostotilaus luodaan konfiguraatiolle C1 ja versiolle V2, , kaksi V2 ja C1 -konfiguraatiolle määritettyä sääntöä ovat moniselitteisiä. Supply Chain Management ratkaisee moniselitteisyyden etsimällä sääntöjä laskevassa luokitusjärjestyksessä ja käyttää ensimmäistä käytettävissä olevaa sääntöä. Tässä esimerkissä, luotaessa ostotilausriviä konfiguraatiolle C1 ja versiolle V2, käyttäjä saa varoitusviestin, joka ilmoittaa, että nimike on pidossa ja tämä aiheutuu version arvosta. Jos konfiguraatiota koskeva luokitus on korkeampi kuin version sääntö, konfiguraation C1 ja version V2 ostotilausrivin luominen on onnistunut eikä "nimike on pidossa" viestiä anneta käyttäjälle. 

Ota huomioon seuraavat tilauksen oletusasetusten säännöt.

| Sijoitus | Toimipaikka | Määritys | Versio | Oletustoimipaikka | Oletusvarasto | Osto: Ohita oletusvarastodimensio | Ostovarasto |
|------|------|---------------|-------|--------------|-------------------|------------------------------------------------|--------------------|
| 20   | 2    |               |       |              |                   | Kyllä                                            | 22                 |
| 10   |      | C1            |  V2   |  2           |  21               |                                                |                    |
| 0    |      |               |       | 1            | 11                |                                                |                    |

Järjestelmän käy läpi sääntöjoukon kahdesti määrittääkseen toimipisteen ja varaston. Kun konfiguraation C1 versio V2 ostotilausrivi luodaan, toimipaikka määritetään luokituksen 10 säännön perusteella. Järjestelmä etsii sitten sääntöä toimipaikalle 2 määrittääkseen varaston. Sääntö 20 löytyy ja koska sen luokitus on suurempi, ostotilausrivillä on varasto 22 eikä 21.

Yleisen periaatteen mukaisesti erityissäännöt ja tärkeämpien dimensioiden säännöt saavat korkeamman luokituksen ja yleiset säännöt saavat alemman luokituksen. 

Sääntö, jonka luokitus on nolla, toimii turvaverkkona. Jos muut säännöt eivät päde, käytetään nollasäännön mukaisia tilauksen oletusasetukset. 

Koska luokitusnumero on tärkeä, **Tilauksen oletusasetukset** -toimintoruudussa on toimintoja säännön siirtämiseksi ylös tai alas tai säännön uudelleennumeroimiseksi, niin että ne etenevät aina 10 kerrallaan. 

Vapautetulla tuotteella voi olla useita luotuja sääntöjä. Saat selkeämmän käsityksen siitä, mikä sääntö on hallitseva ja miksi sitä tarvitaan, kohdasta **Ruudukkonäkymä** **Tilauksen oletusasetukset** -sivulla. Voit ottaa ruudukkonäkymän käyttöön valitsemalla **Asetukset** &gt; **Sivun asetukset** &gt; **Vaihda näkymää** &gt; **Ruudukkonäkymä**. Ruudukossa näytettävien sarakkeiden määrä voi olla hyvin suuri, erityisesti myynti- ja varasto-välilehdillä. Näytettävien sarakkeiden enimmäismäärää ruudukossa voidaan rajoittaa piilottamalla tai näyttämällä sarakeryhmiä painikkeilla kohdassa **Tilauksen oletusasetukset** &gt; **Sarakkeen näyttö** -valikko.

### <a name="specific-order-settings-for-released-product-variant"></a>Vapautetun tuotevariantin erityistilausasetukset

Jos tilauksen oletusasetusten sääntöjärjestelmä on liian hankala, on mahdollista määrittää tilauksen oletusasetukset jokaiselle tuotevariantille. Seuraavassa esimerkissä esitetään, miten tämä etsii tuotetta ja edellä kuvattuja tapauksia.

| Sijoitus | Toimipaikka | Määritys | Versio | Osto: ohita oletusasetukset | Oston läpimenoaika | Osto: estetty | Myynti: ohita oletusasetukset | Myynti: pysäytetty |
|------|------|---------------|-------|--------------------------------------|--------------------|--------------------|-----------------------------------|-----------------|
| 10   |      | C2            | V3    | Kyllä                                  | 5                  |                    |                                   |                 |
| 10   |      | C2            | V2    | Kyllä                                  | 5                  | Kyllä                | Kyllä                               | Kyllä             |
| 10   |      | C2            | V1    | Kyllä                                  | 5                  | Kyllä                | Kyllä                               | Kyllä             |
| 10   |      | C1            | V3    | Kyllä                                  | 2                  |                    |                                   |                 |
| 10   |      | C1            | V2    | Kyllä                                  | 2                  | Kyllä                | Kyllä                               | Kyllä             |
| 10   |      | C1            | V1    | Kyllä                                  | 2                  | Kyllä                | Kyllä                               | Kyllä             |
| 0    |      |               |       |                                      | 5                  |                    |                                   |                 |

Luokituksella ei tällöin ole todellista merkitystä, joten voit piilottaa sen. Ratkaisu aiheuttaa mahdollisesti ylläpito-ongelmia. Haluat ehkä kuitenkin käyttää näitä asetuksia, jos olet harkinnut integrointia tuotteen elinkaaren hallintajärjestelmään (PLM).

## <a name="use-strict-or-standard-validation-of-default-order-quantities"></a>Käytä tiukkaa tai vakiotarkistusta oletustilausmäärille

Voit valita, kuinka tiukka järjestelmä on vahvistettaessa tuotteen **Oletustilausasetukset**-kohtaan syötettyjä määriä. Kun käytät uutta tiukkaa vaihtoehtoa, **vakiotilausmäärän** on aina oltava määritetyn **Monikerta**-arvon monikerta ostotilauksille, varastolle ja myyntitilauksille. Jos käytät tiukkaa vahvistusta, et voi tallentaa oletustilausasetuksia, jotka eivät täytä tätä vaatimusta (virhe näytetään sanomarivillä). 

Tiukka vahvistus koskee **Vakiotilausmäärä**-arvoja, jotka on määritetty **Ostotilaus**-, **Varasto**- ja **Myyntitilaus**-pikavälilehdissä **Oletustilausasetukset**-sivulla. Jokaisella pikavälilehdellä on oma **Monikerta**-asetus, jota käytetään tarkistettaessa kyseisen pikavälilehden **Vakiotilausmäärä**-arvoa.

### <a name="enable-the-strict-validation-option"></a>Tiukan vahvistusasetuksen käyttöönotto

Ennen kuin käytät tiukkaa vahvistusasetusta, se on otettava käyttöön järjestelmässä. Järjestelmänvalvojat voivat käyttää [ominaisuuksien hallinnan](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) sivua ja tarkistaa toiminnon tilan sekä ottaa sen käyttöön tarvittaessa. Toiminto näkyy seuraavasti:

- **Moduuli** - *Tuotetietojen hallinta*
- **Ominaisuuden nimi** - *Oletustilausmäärien tiukka vahvistus*

### <a name="set-the-validation-option"></a>Vahvistusasetuksen määrittäminen

Voit määrittää vahvistusasetuksen seuraavasti:

1. Siirry kohtaan **Tuotetietojen hallinta \> Asetukset \> Tuotetietojen hallinnan parametrit**.
1. Määritä **Yleistä**-välilehdessä **Oletustilausmäärien vahvistus** jollekin seuraavista arvoista:
    - **Tiukka** - Valitse tämä asetus, jos haluat varmistaa, että kaikki **vakiotilausmäärän** arvot ovat **Monikerta**-arvon monikertoja kussakin pikavälilehdessä (**Ostotilaus**, **Varasto** ja **Myyntitilaus**).
    - **Vakio** - Valitse tämä asetus, jos haluat käyttää vakiovahvistusta (joka toimii samalla tavalla, jos tämä ominaisuus ei ole käytössä).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]