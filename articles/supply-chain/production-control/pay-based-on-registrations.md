---
title: Rekisteröinteihin perustuva palkka
description: Tässä ohjeaiheessa käsitellään palkan laskemista työntekijän rekisteröintien perusteella.
author: johanhoffmann
manager: tfehr
ms.date: 03/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: JmgCalcApproveWeekView, JmgProdStatusListPagePayrollCostDetails, JmgPayCountTable, JmgPayStatConfig, JmgOvertimeSlize, JmgPayAgreementOverride, JmgPayCountSum, JmgPayAdjustSetup, JmgPayAdjustCostType, JmgPayEmployee, JmgMESBreak, JmgPayAddTable, JmgPayAddTransSelectTransId, JmgPayrollCostDetailsPart, jmgProdStatusListPagePayrollCosts, JmgPayrollCostPart, JmgPayEvents, JmgTermRegPayStatSetup, JmgPayStatGroup, JmgPayAddTrans, JmgPayStatTrans
audience: Application User
ms.reviewer: kamaybac
ms.custom: 1705903
ms.assetid: 427e01b3-4968-4cff-9b85-1717530f72e4
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2018-03-20
ms.dyn365.ops.version: AX 8.0.0
ms.openlocfilehash: 98ca6f7713b2f605a49a97d391fb8485bea78c4b
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/15/2021
ms.locfileid: "4966377"
---
# <a name="pay-based-on-registrations"></a>Rekisteröinteihin perustuva palkka

[!include [banner](../includes/banner.md)]

Tässä ohjeaiheessa käsitellään yksityiskohtaisesti palkan laskemista työntekijän rekisteröintien perusteella. Se sisältää esimerkkejä siitä, miten laskennan käytettävissä olevien asetusvalintojen eri yhdistelmät vaikuttavat tulokseen. Tässä on joitakin alueita, jotka katetaan:

- Liukuva työaika
- Ylityö
- Tauot
- Kytkentäkoodit
- Palkkatapahtumat
- Maksusopimukset
- Työajan seurannan laskentaparametrit
- Poissaolo

## <a name="the-use-of-flex-time"></a>Liukuvan työajan käyttäminen

Liukuma-ajan jaksot määritetään aikaprofiileissa, joita käytetään työajan seurannassa. Liukuvan työajan profiilityyppejä on kaksi: **Ylijäämä** ja **Vaje**. Kun työntekijä rekisteröi ajan ylijäämäajalla, työntekijän liukuvan työajan saldoon lisätään työskennellyt tunnit. Työntekijä ei saa kompensaatiot tunneista, jotka hän työskenteli ylijäämäajalla. Työntekijä voi kuitenkin olla poissa liukuman vähennyskausien aikana ja saada palkan liukuvan saldon tunneilta. Tämän vuoksi järjestelmä pitää liukuvalle työajalle sijoittuvaa poissaoloaikaa poissaolona.

## <a name="scenarios-based-on-flex-periods"></a>Liukuma-aikoihin perustuvat skenaariot

Seuraavat kaksi skenaariota perustuvat työpäivää ilmaisevaan liukuvan työajan profiiliin. Molemmissa skenaarioissa maksu lasketaan sen liukumajakson perusteella, jossa työntekijä saapuu töihin ja poistuu töistä.

### <a name="flex-profile-for-one-workday"></a>Yhden työpäivän liukumaprofiili

| Profiilin tyyppi  | Alku    | Loppu      | Päivä     |
|---------------|----------|----------|---------|
| Ylityö     | 0.00 | 6.00 | Maanantai  |
| Ylijäämä         | 6.00 | 7.00 | Maanantai  |
| Saapuminen      | 7.00 | 7.00 | Maanantai  |
| Vakioaika | 7.00 | 14.30 | Maanantai  |
| Vaje-         | 14.30 | 15.30 | Maanantai  |
| Poistuminen     | 15.30 | 15.30 | Maanantai  |
| Ylityö     | 15.30 | 6.00 | Tiistai |

### <a name="scenario-1-a-worker-registers-clock-in-during-a-flex-period-and-clock-out-during-a-flex--period"></a>Skenaario 1: Työntekijä rekisteröi saapumisajan ylijäämäajalla ja poistumisajan vajeajalla

Työntekijän rekisteröinnit päivän aikana näyttävät tällaiselta.

| Kirjauskansion rekisteröintityyppi | Alku    | Loppu      |
|---------------------------|----------|----------|
| Saapuminen                  | 6.30 | 6.30 |
| Tuotannon työ            | 6.30 | 14.45 |
| Poistuminen                 | 14.45 | 14.45 |

Työntekijän päivän aikana tekemät rekisteröinnit lasketaan ja siirretään maksettavaksi **Hyväksy**-sivulla (**Työajan seuranta** &gt; **Tarkista ja hyväksy** &gt; **Hyväksy**). Kun rekisteröinnit on laskettu, laskennan tulos näkyy **Ajat**-välilehdessä. 

Seuraavat kentät selittävät tätä skenaariota.

| Liukuman lisäys | Liukuman vähennys | Aika | Maksetaan ajasta |
|--------|--------|------|----------|
| 0,50   | 0.75   | 8,25 | 8,50     |

#### <a name="calculation-of-flex"></a>Liukuman lisäyksen laskenta

Liukumaprofiilin mukaan aikaväli 6.00–7.00 on liukuman lisäysjakso. Jos työntekijä siis saapuu työpaikalle kello 6.30, hän ansaitsee 0,5 tuntia. Työntekijän liukuvan työajan tilille lisättävä aikamäärä.

#### <a name="calculation-of-flex-"></a>Liukuman vähennyksen laskenta

Liukumaprofiilin mukaan liukuman vähennysjakso alkaa 14.30 ja loppuu 15.30. Jos työntekijä poistuu työpaikalta 14.45, vajeajalla jäljellä olevat 45 minuuttia (0,75 tuntia) rekisteröidään palkkatyöajaksi ja sama summa vähennetään työntekijän liukuvan työajan tililtä. 45 minuuttia sisällytetään palkkatyöaikaan, sillä työntekijälle maksetaan palkkaa vajeajassa jäljellä olevalta 45 minuutilta. Jos työntekijä on poissa liukuman vähennyskauden aikana,. työntekijän liukuvan työajan tililtä vähennetään 45 minuuttia.

#### <a name="calculation-of-time"></a>Ajan laskenta

Aika lasketaan saapumisen ja poistumisen väliajaksi, jolloin 6.30–14.45 tarkoittaa 8,25 tuntia.

#### <a name="calculation-of-pay-time"></a>Palkkatyöajan laskenta

Palkkatyöaika on aika, jolta työntekijä saa palkkaa. Tässä skenaariossa työntekijä on töissä 8,25 tuntia (**Aika**). **Palkkatyöaika** lasketaan 8,50 tuntina, koska työntekijälle on myönnetty palkka liukuman vähennysjakson aikana sen jälkeen, kun hän poistui töistä. Palkkatyöaika on sama kuin suunniteltujen työtuntien määrä, koska liukuman lisäysaika lisätään työntekijän liukuvan työajan tilille eikä palkkatyöaikaan. Vajeajan aikainen poissaoloaika kompensoidaan palkanmaksuajalla ja vähennetään työntekijän liukuvan työajan tililtä.

| Aika              | Rekisteröintityyppi | Palkkatyöaika (tunnit)      |
|-------------------|-------------------|-----------------------|
| 6.30–7.00 | Ylijäämä             | 0                     |
| 7.00–14.45 | Vakioaika     | 7,75                  |
| 14.45–15.50 | Vaje-             | 0,75 (poissaolojakso) |
|                   | Yhteensä             | 8,50                  |

### <a name="scenario-2-a-worker-works-during-the-whole-flex--period-and-also-works-overtime"></a>Skenaario 2: Työntekijä työskentelee koko vajeajan ja tekee myös ylitöitä

Työntekijän rekisteröinnit päivän aikana näyttävät tällaiselta.

| Kirjauskansion rekisteröintityyppi | Alku    | Loppu      |
|---------------------------|----------|----------|
| Saapuminen                  | 6.30 | 6.30 |
| Tuotannon työ            | 6.30 | 17.00 |
| Poistuminen                 | 17.00 | 17.00 |

Kun olet laskenut **Hyväksyntä**-sivun kirjauskansion rekisteröinnit, voit tarkastella laskennan tulosta **Ajat**-välilehdessä. Saat lisätietoja tästä skenaariosta seuraavien kenttien avulla.

| Liukuman lisäys | Liukuman vähennys | Aika  | Maksetaan ajasta | Maksetaan ylityöstä |
|--------|--------|-------|----------|--------------|
| 0,50   | 0,00   | 10,50 | 10.00    | 1.50         |

#### <a name="calculation-of-flex"></a>Liukuman lisäyksen laskenta

Liukumaprofiilin mukaan aikaväli 6.00–7.00 on liukuman lisäysjakso. Kello 6.30 työpaikalle saapuva työntekijä siis saa 0,5 tuntia ylijäämäaikaa liukuvan työajan tililleen.

#### <a name="calculation-of-flex-"></a>Liukuman vähennyksen laskenta

Koska työntekijä on töissä liukuman vähennysjakson aikana, liukuman vähennystä ei lasketa. Liukuman vähennys lasketaan vain, jos työntekijä on poissa liukuman vähennysjakson aikana. Jos työntekijä työskentelee liukuman vähennysjakson aikana, hänelle myönnetään normaalille työajalle määritetty palkkio. Jos työntekijä on poissa liukuman vähennyskauden aikana,. työntekijän liukuvan työajan tililtä vähennetään 45 minuuttia.

#### <a name="calculation-of-time"></a>Ajan laskenta

Aika lasketaan kello 6.30 tapahtuvan saapumisen ja kello 17.00 tapahtuvan poistumisen väliseksi ajaksi, mikä on 10,5 tuntia.

#### <a name="calculation-of-pay-time"></a>Palkkatyöajan laskenta

Tässä skenaariossa työntekijä työskentelee 10,50 tuntia (**Aika**). **Palkkatyöaika** lasketaan 10,00 tuntina, koska työntekijälle ei ole myönnetty palkkaa liukuman lisäyskauden aikana.

#### <a name="calculation-of-pay-overtime"></a>Palkan ylityön laskenta

| Aika               | Rekisteröintityyppi | Palkkatyöaika (tunnit) |
|--------------------|-------------------|------------------|
| 6.30–7.00  | Ylijäämä             | 0                |
| 7.00–14.30  | Vakioaika     | 7,50             |
| 14.30–15.50  | Vaje-             | 1,00             |
| 15.30–17.00 | Ylityö          | 1.50             |
|                    | Yhteensä             | 10.00            |

### <a name="generation-of-pay-items"></a>Palkkatapahtumien luominen

Työntekijän päivän rekisteröinnit voidaan siirtää **Hyväksy**-sivulta. Siirtoprosessin aikana luodaan palkkatapahtumat ja siirretyt rekisteröinnit. Palkkatapahtumat edustavat palkkatyöajan erittelyä esimerkiksi normaaliin työaikaan, ylityöaikaan ja palkallisiin taukoihin.

Voit avata maksutapahtumaluettelon valitsemalla **Työajan seuranta** &gt; **Tarkista ja hyväksy** &gt; **Hyväksy**. Valitse sitten **Kysely** &gt; **Siirretyt rekisteröinnit**.

Maksukohteet ovat työntekijän palkan peruste. Voit luoda tiedoston, joka sisältää tietoja palkkatapahtumista ja siirtää kyseisen tiedoston palkanlaskentajärjestelmään.

Tuotanto- ja projektitehtävien aika ja kustannukset siirretään siirtoprosessin osana tuotanto- ja projektikirjauskansioihin käytetyn ajan ja kustannusten kirjaamista varten. Siirretyt rekisteröinnit ovat tuotantotilausten ja projektien ajan tuntikohtaisen kustannushinnan perusta. Voit avata siirretyt rekisteröinnit **Hyväksy**-sivun **Kysely**-valikon kautta.

Esimerkiksi skenaariossa 2 luodaan seuraavat palkkatapahtumat.

| Palkkalaji     | Maksulaji | Palkkayksiköt | Osuus  | Kokonaiskustannukset |
|---------------|----------|-----------|-------|------------|
| Vakioaika | 1201     | 10,0      | 10    | 100        |
| Ylityö      | 1 301     | 1.50      | 5     | 7,50       |
|               |          |           | Yhteensä | 107,50     |

Vakiotyöajan maksukohteen palkkayksikkö on 10 tuntia, joka kattaa vakiotyöajan, vajeajan ja ylityön. Vakiotyöaika, vajeaika ja ylityöaika konsolidoidaan yhdeksi maksukohteeksi, koska kaikki tyypit lasketaan vakiotyöaikana **Laskentaparametrit**-sivun parametrin oletusasetuksen (**Työajan seuranta** &gt; **Asetukset** &gt; **Laskentaparametrit**) perusteella. Ylityö lasketaan päälle vakiotyöajan päälle käyttämällä lisähintaa 5.

Jos haluat, että normaali työaika ja ylityö erottuvat selvästi niin, että palkkatyyppien maksuyksiköt kattavat vain normaalin työajan ja ylityön todellisen käytetyn ajan, normaalin työajan palkkayksiköiden on oltava 8,50 ja ylityön palkkayksiköiden 1,50.

Jos haluat määrittää järjestelmän erottamaan vakiotyöajan ja ylityön selkeästi toisistaan, ylityö on jätettävä pois vakiotyöajasta. Sinun on myös muutettava ylityön maksulajin asetuksia, jotta ylityön palkkio kattaa kaikki ylityötä tehtyjen tuntien maksut.

### <a name="exclude-overtime-from-the-standard-time"></a>Jätä ylityö pois normaalista työajasta

Valitse **Laskentaparametrit**-sivulla profiilin määritystyypiksi **Ylityö** ja määritä **Palkkatyöaika**-asetuksen arvoksi **Ei** tässä kuvatulla tavalla.

| Rekisterin määrittely | Profiilin määrittelylaji | Laskelma   |     | Maksettu         |     |
|--------------------|----------------------------|---------------|-----|--------------|-----|
| Työaika       | Ylityö                   | Vakioaika | Kyllä | Maksetaan ajasta     | En  |
|                    |                            | Maksetaan ajasta      | Kyllä | Maksetaan ylityöstä | Kyllä |

Kun laskentaparametrit on oikaistu, seuraavat palkkatapahtumat luodaan.

| Palkkalaji     | Maksulaji | Palkkayksiköt | Osuus  | Kokonaiskustannukset |
|---------------|----------|-----------|-------|------------|
| Vakioaika | 1201     | 8,50      | 10    | 85,0       |
| Ylityö      | 1 301     | 1.50      | 15    | 22,50      |
|               |          |           | Yhteensä | 107,50     |

> [!NOTE]
> Laskentaparametreilla on suositeltu vakioasetus. Näiden parametrien muuttamisen yhteydessä kannattaa olla varovainen. Voit palauttaa suositellut vakioasetukset valitsemalla **Laskentaparametrit**-sivulla **Palauta arvot**.

### <a name="allow-a-deviation-from-the-standard-pay-profiles"></a>Salli vakiopalkkaprofiilien poikkeama

**Profiilit**-sivulla (**Työajan seuranta** &gt; **Asetukset** &gt; **Aikaprofiilit** &gt; **Profiilit**) voit määrittää kytkentäkoodit ja tauot sisältävien profiilien tyypit.

### <a name="switch-codes"></a>Kytkentäkoodit

Voi antaa kytkentäkoodien avulla työntekijöille mahdollisuuden poiketa omasta profiilityypistä toiseen profiilityyppiin vaihtamalla. Voit esimerkiksi antaa työntekijälle mahdollisuuden muuttaa liukuman lisäysajan ylityöksi. Työntekijä voi lisätä kytkentäkoodin rekisteröinnin yhteydessä tai rekisteröintien hyväksyjälle voidaan määrittää kytkentäkoodin lisäystehtävä.

Ennen kuin kytkentäkoodia voi käyttää, sen tyypiksi on määritettävä epäsuora tehtävä. Sinun on sitten lisättävä vaihtokoodi sen kauden aikaprofiiliin, jolloin sallit profiilityypin vaihtamisen. Noudata näitä vaiheita esimerkiksi silloin, kun liukuman lisäysjakson muuttamisen mahdollistavan kytkentäkoodin, jossa jakson muutos on 6.30–7.00 ja ylityöaika.

1. Luo kytkentäkoodi, jonka nimi on **OTBCI (Muunna liukuva työaika ylityöksi ennen saapumista)**. Valitse **Työajan seuranta** &gt; **Ylläpidä epäsuoria toimintoja** &gt; **Epäsuorat toiminnot**.
2. Lisää **Kytkentäkoodi**-sarakkeeseen OTBCI aikaprofiilin liukuman lisäysriville.
3. Lisää **Toissijainen**-sarakkeeseen **Ylityö**-profiilityyppi.

Ota huomioon seuraavaa työpäivää edustava liukumaprofiili.

| Profiilin tyyppi  | Alku    | Loppu      | Päivä     |
|---------------|----------|----------|---------|
| Ylityö     | 0.00 | 6.00 | Maanantai  |
| Ylijäämä         | 6.00 | 7.00 | Maanantai  |
| Saapuminen      | 7.00 | 7.00 | Maanantai  |
| Vakioaika | 7.00 | 14.30 | Maanantai  |
| Vaje-         | 14.30 | 15.30 | Maanantai  |
| Poistuminen     | 15.30 | 15.30 | Maanantai  |
| Ylityö     | 15.30 | 6.00 | Tiistai |

Tässä ovat työntekijän rekisteröinnit päivän aikana.

| Kirjauskansion rekisteröintityyppi | Alku    | Loppu      |
|---------------------------|----------|----------|
| Saapuminen                  | 6.30 | 6.30 |
| Tuotannon työ            | 6.30 | 14.45 |
| Poistuminen                 | 17.00 | 17.00 |

Seuraavat maksutapahtumia luodaan siirron jälkeen.

| Palkkalaji     | Maksulaji | Palkkayksiköt | Osuus  | Kokonaiskustannukset |
|---------------|----------|-----------|-------|------------|
| Vakioaika | 1201     | 8,50      | 10    | 85,0       |
| Ylityö      | 1 305     | 1.50      | 15    | 22,50      |
|               |          |           | Yhteensä | 107,50     |

Peruuta siirto **Hyväksyntä**-sivulla ja kohdista sitten **OTBCI**-kytkentäkoodi **Kytkentäkoodi**-valikon avulla. Kun siirrät rekisteröinnit toisen kerran, seuraavat palkkatapahtumat luodaan.

| Palkkalaji     | Maksulaji | Palkkayksiköt | Osuus  | Kokonaiskustannukset |
|---------------|----------|-----------|-------|------------|
| Vakioaika | 1201     | 8,50      | 10    | 80,0       |
| Ylityö      | 1 305     | 2,00      | 15    | 30,0       |
|               |          |           | Yhteensä | 107,50     |

> [!NOTE]
> Kun käytät kytkentäkoodia, ylityöaikaa lisään 0,5 tunnilla 1,50 tunnista 2,00 tuntiin. Rekisteröidyn ylijäämäajan muunto on 0,5 tuntia. Rekisteröintiaika on 6.30–7.00 ja sitten ylityöaika.

### <a name="breaks"></a>Tauot

Työn tauot vaikuttavat työntekijän palkan laskentaan. Taukojen tyypiksi määritetään epäsuora tehtävä. Määrityksenä voi olla joko **Palkallinen**, jolloin tauko lisätään työntekijän palkkaan, tai **Palkaton**, joka estää tauon lisäämisen työntekijän palkkaan. Tauko voidaan määrittää myös joko **suunnitelluksi** tai **rekisteröidyksi**.

#### <a name="planned-breaks"></a>Suunnitellut tauot

Jos yrityksellä on kiinteä taukoaika, kuten kiinteä lounastauko, tauko voidaan määrittää aikaprofiilissa. Tällöin työntekijän ei tarvitse rekisteröidä taukoa työkortin sivuilla. Sen sijaan tauko kirjataan automaattisesti, kun työntekijän rekisteröinnit lasketaan **Hyväksyntä**-sivulla.

#### <a name="registered-breaks"></a>Rekisteröidyt tauot

Jos yrityksessä ei käytetä suunniteltuja taukoja, työntekijät voivat rekisteröidä tauot työpäivän aikana. Rekisteröityjä taukoja voi käyttää esimerkiksi silloin, kun työntekijä työskentelee sellaisen liukuvan aikaprofiilin kanssa, jolle ei ole määritetty saapumis- ja lähtemisaikaa. Rekiströityjen taukojen tyyppi on epäsuora tehtävä. Työntekijä rekisteröi tauon **Työkortti**-päätesivulla tai **Työkortti**-laitesivulla. Käyttäjä voi valita molemmilla sivuilla tauon tyypin ennalta määritettyjen taukotehtävien luettelosta.

#### <a name="paid-and-unpaid-breaks"></a>Palkalliset ja palkattomat tauot

Taukotehtävät voidaan määrittää **palkallisiksi** tai **palkattomaksi**. Palkallinen tauko sisältyy palkkatyöajan laskentaan. Järjestelmä käyttää **Tauko**-rekisteröintityypin palkkasopimuksessa määritettyä palkkatyyppiä.

### <a name="example-of-a-planned-break"></a>Esimerkki suunnitellusta tauosta

Ota huomioon, että seuraava aikaprofiili sisältää palkattoman lounastauon.

| Profiilin tyyppi  | Alku    | Loppu      | Päivä     |
|---------------|----------|----------|---------|
| Ylityö     | 0.00 | 6.00 | Maanantai  |
| Ylijäämä         | 6.00 | 7.00 | Maanantai  |
| Saapuminen      | 7.00 | 7.00 | Maanantai  |
| Vakioaika | 7.00 | 12.00 | Maanantai  |
| Tauko         | 12.00 | 12.30 | Maanantai  |
| Vakioaika | 12.30 | 14.30 | Maanantai  |
| Vaje-         | 14.30 | 15.30 | Maanantai  |
| Poistuminen     | 15.30 | 15.30 | Maanantai  |
| Ylityö     | 15.30 | 6.00 | Tiistai |

Tässä ovat työntekijän rekisteröinnit päivän aikana.

| Kirjauskansion rekisteröintityyppi | Alku    | Loppu      |
|---------------------------|----------|----------|
| Saapuminen                  | 6.30 | 6.30 |
| Tuotannon työ            | 6.30 | 14.45 |
| Poistuminen                 | 17.00 | 17.00 |

Kun olet laskenut **Hyväksyntä**-sivun kirjauskansion rekisteröinnit, voit tarkastella laskennan tulosta **Ajat**-välilehdessä. Saat lisätietoja tästä skenaariosta seuraavien kenttien avulla.

| Liukuman lisäys | Liukuman vähennys | Aika  | Maksetaan ajasta | Palkaton tauko | Maksetaan ylityöstä |
|--------|--------|-------|----------|---------------------|--------------|
| 0,50   | 0,00   | 10,50 | 9,50     | 0,5                 | 1.50         |

> [!NOTE] 
> Järjestelmä lasketaan 0,5 tuntia palkatonta taukoaikaa eikä kyseinen aika ole osa palkkatyöaikaa.

### <a name="example-of-a-registered-break"></a>Esimerkki rekisteröidystä tauosta

Ota huomioon, että seuraavalla aikaprofiililla ei ole suunniteltuja taukoja.

| Profiilin tyyppi  | Alku    | Loppu      | Päivä     |
|---------------|----------|----------|---------|
| Ylityö     | 0.00 | 6.00 | Maanantai  |
| Ylijäämä         | 6.00 | 7.00 | Maanantai  |
| Saapuminen      | 7.00 | 7.00 | Maanantai  |
| Vakioaika | 7.00 | 14.30 | Maanantai  |
| Vaje-         | 14.30 | 15.30 | Maanantai  |
| Poistuminen     | 15.30 | 15.30 | Maanantai  |
| Ylityö     | 15.30 | 6.00 | Tiistai |

Tässä ovat työntekijän rekisteröinnit päivän aikana.

| Kirjauskansion rekisteröintityyppi | Alku    | Loppu      |
|---------------------------|----------|----------|
| Saapuminen                  | 6.30 | 6.30 |
| Tuotannon työ            | 6.30 | 17.00 |
| Tauko                     | 12.30 | 12.32 |
| Poistuminen                 | 17.00 | 17.00 |

Kun rekisteröinnit on laskettu, tehtävien aika lasketaan.

| Kirjauskansion rekisteröintityyppi | Alku    | Loppu      | Aika  |
|---------------------------|----------|----------|-------|
| Saapuminen                  | 6.30 | 6.30 |       |
| Tuotannon työ            | 6.30 | 17.00 | 10.00 |
| Tauko                     | 12.30 | 12.32 | 0,50  |
| Poistuminen                 | 17.00 | 17.00 |       |

> [!NOTE]
> Tauon aika kulkee rinnakkain tehtävän ajan kanssa. (Tässä esimerkissä tehtävä on tuotantotyö.) Tätä toimintatapaa käytetään aina taukotehtävissä. Kun rekisteröinnit on laskettu, taukoaika vähennetään tehtäväajasta. Tässä tapauksessa tuotantotyön kesto on 10,50 tuntia, mutta ajan laskemisessa käytetään 10 tuntia, koska tehtävän ajasta vähennetään taukoon kulunut aika eli 0,5 tuntia.

Kun olet laskenut **Hyväksyntä**-sivun kirjauskansion rekisteröinnit, voit tarkastella laskennan tulosta **Ajat**-välilehdessä. Saat lisätietoja tästä skenaariosta seuraavien kenttien avulla.

| Liukuman lisäys | Liukuman vähennys | Aika  | Maksetaan ajasta | Palkaton tauko | Maksetaan ylityöstä |
|--------|--------|-------|----------|---------------------|--------------|
| 0,50   | 0,00   | 10,50 | 9,50     | 0,5                 | 1.50         |

Jos suunniteltu tauko on palkallinen eikä palkaton, laskennan tulos näyttää tältä.

| Liukuman lisäys | Liukuman vähennys | Aika  | Maksetaan ajasta | Palkalliset tauot | Maksetaan ylityöstä |
|--------|--------|-------|----------|-----------------|--------------|
| 0,50   | 0,00   | 10,50 | 10.00    | 0,5             | 1.50         |

### <a name="pay-items-and-paid-breaks"></a>Palkkatapahtumat ja palkalliset tauot

Kun siirrät rekisteröinnit **Hyväksy**-sivulle, palkkatapahtumat luodaan. Maksetuille tauoille luodaan erillinen maksukohde.

Palkallinen tauon palkkio määräytyy tauon maksusopimuksissa määritetyn maksulajin mukaan. Palkkatyypin sijaan määritetyssä päivämäärävälissä voidaan käyttää tuntikohtaista kustannushintaa tauolle.

Ota huomioon seuraava aikaprofiili.

| Profiilin tyyppi  | Alku    | Loppu      | Päivä     |
|---------------|----------|----------|---------|
| Ylityö     | 0.00 | 6.00 | Maanantai  |
| Ylijäämä         | 6.00 | 7.00 | Maanantai  |
| Saapuminen      | 7.00 | 7.00 | Maanantai  |
| Vakioaika | 7.00 | 14.30 | Maanantai  |
| Vaje-         | 14.30 | 15.30 | Maanantai  |
| Poistuminen     | 15.30 | 15.30 | Maanantai  |
| Ylityö     | 15.30 | 6.00 | Tiistai |

Tässä ovat työntekijän rekisteröinnit päivän aikana.

| Kirjauskansion rekisteröintityyppi | Alku    | Loppu      | Aika |
|---------------------------|----------|----------|------|
| Saapuminen                  | 7.00 | 7.00 |      |
| Tuotannon työ            | 7.00 | 15.00 | 7,5  |
| Tauko (palkallinen)              | 12.00 | 12.30 | 0,5  |
| Poistuminen                 | 15.00 | 15.00 |      |

Esimerkiksi normaalin työajan maksulajiksi on määritetty **1201** ja maksusopimuksen palkkioksi on määritetty **10**. Palkallisen tauon maksulaji on **1301** ja palkkio **8**. Kun rekisteröinnit on siirretty, palkkatapahtumat luodaan.

| Palkkalaji     | Maksulaji | Palkkayksiköt | Osuus |
|---------------|----------|-----------|------|
| Vakioaika | 1201     | 7,50      | 10   |
| Vaje-         | 1201     | 0,50      | 10   |
| Tauko (palkallinen)  | 1 301     | 0,50      | 8    |

## <a name="how-the-cost-of-paid-breaks-is-allocated-to-projects-and-production-orders"></a>Miten palkallisten taukojen kustannukset kohdistetaan projekteihin ja tuotantotilauksiin

Projektitehtävien ja tuotantotöiden tuntikustannukset voidaan määrittää siten, että ne määritetään joko työajan seurannassa laskettavien palkkioiden tai tehtäville määritettyjen kustannusluokkien mukaan.

Voit määrittää kustannusluokan valitsemalla **Tuotannonhallinta** &gt; **Asetukset** &gt; **Tuotannonohjaus** &gt; **Tuotantotilauksen oletusarvot** ja määrittämällä **Kustannusluokka**-kentän arvoksi **Kyllä** tai **Ei**.

- **Ei** – Kustannus lasketaan työajan seurannan rekisteröintityypeille määritettyjen palkkatyyppien perusteella.
- **Kyllä** – Kustannukset lasketaan tuotannon ja projektin tehtävien kustannusluokkien perusteella.

### <a name="cost-calculation-based-on-pay-rates-that-are-calculated-in-time-and-attendance"></a>Työajan seurannassa laskettuihin palkkioihin perustuva kustannuslaskenta

Seuraavassa esimerkissä näytetään, miten tuntikustannukset lasketaan, kun kustannukset on määritetty palkkioiden perusteella laskettaviksi.

Tuotantotilauksissa ja projekteissa käytetty tuntikustannushinta lasketaan siirtoprosessin aikana. Voit tarkastella tehtäväkohtaista tuntihintaa avaavalla työseurannan **Hyväksy**-sivun ja valitsemalla sitten **Kysely** &gt; **Siirretyt rekisteröinnit**. Voit määrittää rekisteröintikohtaisen tuntikustannushinnan **Kustannushinnat**-välilehdessä.

Ota huomioon, että seuraavat rekisteröinnit käyttävät edellisessä esimerkissä käytössä olevaa aikaprofiilia.

| Kirjauskansion rekisteröintityyppi | Alku    | Loppu      | Aika |
|---------------------------|----------|----------|------|
| Saapuminen                  | 7.00 | 7.00 |      |
| Käsittely (tilaus: 4711)     | 7.00 | 11.00 | 4    |
| Käsittely (tilaus: 4712)     | 11.00 | 15.00 | 3,50 |
| Tauko (palkallinen)              | 12.00 | 12.30 | 0,50 |
| Poistuminen                 | 15.00 | 15.00 |      |

Kun rekisteröinnit on siirretty, seuraavat siirretyt rekisteröinnit luodaan.

| Rekisteröintityyppi     | Aika | Kustannushinta tuntia kohden |
|-----------------------|------|---------------------|
| Saapuminen              | 0,00 | 0,00                |
| Käsittely (tilaus: 4711) | 4,00 | 10.00               |
| Käsittely (tilaus: 4712) | 3,50 | 11,14               |
| Tauko (palkallinen)          | 0,50 | 0,00                |
| Poistuminen             | 0,00 | 0,00                |

Palkallinen tauon tuntikohtaisen kustannushinnan laskenta määräytyy suorien palkkakustannusasetuksen mukaan. Valitse **Työajan seuranta** &gt; **Asetukset** &gt; **Työajan seurannan parametrit**. Voit valita **Suorat palkkakustannukset** -kohdan **Kustannushinta**-välilehden **Normaali työaika** -kentässä **Kyllä**, **Ei** tai **Kohdistus**.

- **Kyllä** – Tätä arvoa käytetään edellisessä esimerkissä. Kustannus kohdistetaan siihen tuotantoon tai projektitehtävään, joka suoritetaan rinnakkain palkallisen taukotehtävän kanssa. Tässä esimerkissä tehtävä on tilauksen 4712 tuotantotyö. Kuten näet, palkallisen tauon tuntikohtainen kustannushinta on 0 (nolla) ja se on kohdistetty työhön, joka suoritetaan rinnakkain tauon kanssa.

    Palkallisen tauon kesto on 0,5 tuntia ja sen palkkio on 8. Palkallisen tauon kokonaiskustannus on siksi 4. Kokonaiskustannus kohdistetaan sitten 3,5 tunnin prosessityöhön. Palkallinen tauko tuntikohtainen kustannus on siis 1,14 (4 ÷ 3,5 = 1,14).

- **Kohdistus** – Palkallinen tauko jaetaan tasan päivän rekisteröityjen töiden kesken. Jos edellisessä esimerkissä käytetään tätä arvoa, luodaan seuraavat siirretyt rekisteröinnit.

    | Rekisteröintityyppi     | Aika | Kustannushinta tuntia kohden |
    |-----------------------|------|---------------------|
    | Saapuminen              | 0,00 | 0,00                |
    | Käsittely (tilaus: 4711) | 4,00 | 10,53               |
    | Käsittely (tilaus: 4712) | 3,50 | 10,53               |
    | Tauko (palkallinen)          | 0,50 | 0,00                |
    | Poistuminen             | 0,00 | 0,00                |

    Kahden tuotantotyön käsittelyaika yhteensä on 7,5 tuntia ja palkallisen tauon kokonaiskustannus on 4. Tauon kustannukseksi lasketaan siksi 0,53 (= 4 ÷ 7,5).

- **Ei** – Palkallisten tauon kustannus ei nosta prosessitehtävien tuntikustannusta.

    | Rekisteröintityyppi     | Aika | Kustannushinta tuntia kohden |
    |-----------------------|------|---------------------|
    | Saapuminen              | 0,00 | 0,00                |
    | Käsittely (tilaus: 4711) | 4,00 | 10.00               |
    | Käsittely (tilaus: 4712) | 3,50 | 10.00               |
    | Tauko (palkallinen)          | 0,50 | 0,00                |
    | Poistuminen             | 0,00 | 0,00                |

## <a name="absence"></a>Poissaolo

Poissaolokoodia käytetään työntekijän poissaolojakson rekisteröimisessä. Poissaolokoodi on epäsuoran tehtävän tyyppi, kuten tauot ja kytkentäkoodit. Poissaoloaika voi olla suunniteltu tai rekisteröity. Poissaolo voi olla luvallinen tai luvaton. Luvallisen poissaolon esimerkkejä ovat lääkärikäynti, seminaari ja valamiespalvelu. Luvaton poissaolo on poissaolo, jolle ei ole hyvää syytä. Luvaton poissaolo voi olla esimerkiksi myöhästyminen töistä. Luvallista poissaoloa ei yleensä vähennetä työntekijän palkasta, kun taas luvaton poissaolo voidaan vähentää.

### <a name="planned-absence"></a>Suunniteltu poissaolo

Voit luoda työntekijöiden suunnitellun poissaolon **Luo suunniteltu poissaolo** -sivulla (**Työajan seuranta** &gt; **Luo suunniteltu poissaolo**). Suunniteltu poissaolo rekisteröidään siellä poissaolona työstä tietylle päivämäärä- ja aikavälille.

Työ perustuu kyselyyn. Voit siis luoda suunnitellun poissaolon useille työntekijöille, kuten samaan laskentaryhmään kuuluville työntekijöille. Jos suunniteltu poissaolo koskee yksittäistä työntekijää, rekisteröinti voidaan tehdä joko **Poissaolo**- tai **Aikarekisteröinnin työntekijät** -sivulla.

- Voit antaa poissaolokirjaukset **Läsnäolo**-sivulla valitsemalla ensin **Työajan seuranta** &gt; **Kyselyt ja raportit** &gt; **Läsnäolo** &gt; **Läsnäolo** ja sitten **Poissaolokirjaukset**.
- Voit antaa poissaolokirjaukset *<strong><em>Aikarekisteröintityöntekijät</em></strong>*-sivulla valitsemalla ensin <strong>Työajan seuranta</strong> &gt; <strong>Asetukset</strong> &gt; <strong>Aikarekisteröintityöntekijät</strong> ja sitten <strong>Aika</strong>-välilehden <strong>Aikamääritys</strong> <strong>Poissaolokirjaukset</strong>.

Voit tarkastella työntekijöiden suunniteltuja poissaoloja **Suunnitellut poissaolot** -raportin avulla. Voit avata tämän raportin valitsemalla **Työajan seuranta** &gt; **Kyselyt ja raportit** &gt; **Poissaoloraportit** &gt; **Suunnitellut poissaolot**.

### <a name="registered-absence"></a>Rekisteröity poissaolo

Yleisesti ottaen työntekijää pidetään poissaolevana, jos tämä ei ole töissä suunnitellun saapumisajan ja lähtöajan välisenä aikana. Jos työntekijät saapuvat töihin suunniteltua myöhemmin tai lähtevät töistä suunniteltua aiemmin, heitä pyydetään valitsemaan poissaolon syyn osoittava poissaolokoodi. Poissaolokoodi voidaan määrittää niin, että sitä voidaan käyttää rekisteröinnissä. Luettelossa on vain käytettävissä olevia koodeja.

## <a name="scenarios-based-on-various-combinations-of-work-hour-registrations"></a>Erilaisiin työtuntien rekisteröintiyhdistelmiin perustuvat skenaariot

Seuraavissa skenaarioissa näytetään hyväksyttävät maksutapahtumat ja kirjaukset, jotka luodaan työntekijöille rekisteröintien perusteella. Kaikki skenaariot perustuvat seuraavaan aikaprofiiliin.

| Profiilin tyyppi  | Alku    | Loppu      | Päivä     |
|---------------|----------|----------|---------|
| Ylityö     | 0.00 | 6.00 | Maanantai  |
| Ylijäämä         | 6.00 | 7.00 | Maanantai  |
| Saapuminen      | 7.00 | 7.00 | Maanantai  |
| Vakioaika | 7.00 | 14.30 | Maanantai  |
| Vaje-         | 14.30 | 15.30 | Maanantai  |
| Poistuminen     | 15.30 | 15.30 | Maanantai  |
| Ylityö     | 15.30 | 6.00 | Tiistai |

### <a name="scenario-1-the-worker-clocks-in-later-than-planned"></a>Skenaario 1: Työntekijä saapuu töihin suunniteltua myöhemmin

Työntekijä saapuu työpaikalle 8.30. Koska suunniteltu saapumisaika on 7.00, hän myöhästyy töistä 1,50 tuntia. Työntekijää pyydetään syöttämään poissaolokoodi, koska 1,50 tuntia käsitellään poissaoloaikana. Työntekijä poistuu työpaikalta kello 15.30, mikä on suunniteltu poistumisaika. Kun työntekijän rekisteröinnit lasketaan ja hyväksytään, poissaolokirjaus sekä työntekijän saapuessa valitsema poissaolokoodi näkyvät ajalle 7.00–8.30.

Voit määrittää aikaprofiiliin **Saapuminen**-rekisteröintityypin, joka määrittää työntekijöille työstä myöhästymisen toleranssin. Jos esimerkiksi määrität toleranssiksi 5, työntekijältä pyydetään poissaolokoodia vain, kun hän saapuu töihin myöhemmin kuin kello 7.05.

Koska työntekijällä ei tässä tapauksessa ole hyvää syytä myöhästymiselle, hän valitsee luvattomalle poissaololle määritetyn poissaolokoodin. Poissaolokoodia voidaan käyttää luvattomissa poissaoloissa, jos ylityövähennyksen asetus on käytössä siinä poissaoloryhmässä, johon poissaolokoodi kuuluu. Määritä asetus valitsemalla ensin **Työajan seuranta** &gt; **Asetukset** &gt; **Ryhmät** &gt; **Poissaoloryhmät** ja sitten **Vähennä ylityötä** -valintaruutu.

Tässä kerrotaan, miten työntekijän päivän rekisteröinnit näkyvät **Hyväksyntä**-sivulla laskennan jälkeen.

| Kirjauskansion rekisteröintityyppi         | Alku    | Loppu      | Aika |
|-----------------------------------|----------|----------|------|
| Poissaolo (luvaton - töistä myöhästyminen) | 7.00 | 8.30 | 1.5  |
| Saapuminen                          | 8.30 | 8.30 |      |
| Tuotannon työ                    | 7.30 | 15.30 | 7.0  |
| Poistuminen                         | 15.30 | 15.30 |      |

Tässä on tuloksena saatava palkkatapahtuma rekisteröintien siirron jälkeen.

| Palkkalaji     | Maksulaji | Palkkayksiköt | Osuus |
|---------------|----------|-----------|------|
| Vakioaika | 1201     | 7:00      | 10   |

### <a name="scenario-2-the-worker-clocks-out-before-the-planned-clock-out-time-during-a-standard-time-period"></a>Skenaario 2: Työntekijä poistuu töistä ennen suunniteltua poistumisaikaa vakiotyöajan aikana

Työntekijä saapuu työpaikalle kello 8.00 ja poistuu aikaisin kello 13.00. Koska 13.00 on aiempi ajankohta kuin suunniteltu poistumisaika 15.30 ja 13.00 kuuluu vakiotyöaikaan, työntekijän on valittava poissaolokoodi. Työntekijä valitsee poissaolokoodiksi lääkärissä käynnin, joka on määritetty luvalliseksi poissaoloksi. Luvallisen poissaolon palkkio määritetään **Poissaolo**-rekisteröintityypin maksusopimuksissa (**Työnajan seuranta** &gt; **Asetukset** &gt; **Palkanlaskenta** &gt; **Maksusopimukset**).

Tässä kerrotaan, miten työntekijän päivän rekisteröinnit näkyvät **Hyväksyntä**-sivulla laskennan jälkeen.

| Kirjauskansion rekisteröintityyppi              | Alku    | Loppu      | Aika |
|----------------------------------------|----------|----------|------|
| Saapuminen                               | 7.00 | 7.00 |      |
| Tuotannon työ                         | 7.00 | 13.00 | 4.0  |
| Poistuminen                              | 13.00 | 13.00 |      |
| Poissaolo (luvallinen - lääkärikäynti) | 13.00 | 15.30 | 3.5  |

Tässä on tuloksena saatava palkkatapahtuma rekisteröintien siirron jälkeen.

| Palkkalaji     | Maksulaji | Palkkayksiköt | Osuus |
|---------------|----------|-----------|------|
| Vakioaika | 1201     | 7,50      | 10   |

### <a name="scenario-3-the-worker-clocks-out-before-the-planned-clock-out-time-during-a-flex--period"></a>Skenaario 3: Työntekijä poistuu töistä ennen suunniteltua poistumisaikaa vajeajan aikana

Työntekijä saapuu työpaikalle kello 7.00 ja poistuu kello 14.15, mikä ajoittuu suunnitellulle vajeajalle. Varsinainen poistumisen ja suunnitellun poistumisen välistä aikaa ei pidetä poissaolona eikä työntekijää pyydetä valitsemaan poissaolokoodia. Summa vähennetään työntekijän liukuvan työntekijän tililtä ja työntekijälle maksetaan palkkaa vajeajan jäljellä olevalta ajalta 14.15–15.30.

Tässä kerrotaan, miten työntekijän päivän rekisteröinnit näkyvät **Hyväksyntä**-sivulla laskennan jälkeen.

| Kirjauskansion rekisteröintityyppi | Alku    | Loppu      | Aika |
|---------------------------|----------|----------|------|
| Saapuminen                  | 7.00 | 7.00 |      |
| Tuotannon työ            | 7.00 | 14.15 | 7,25 |
| Poistuminen                 | 14.15 | 14.15 |      |

Tässä on tuloksena saatava palkkatapahtuma rekisteröintien siirron jälkeen.

| Palkkalaji     | Maksulaji | Palkkayksiköt | Osuus |
|---------------|----------|-----------|------|
| Vakioaika | 1201     | 8,50      | 10   |

### <a name="scenario-4-the-worker-clocks-in-late-and-clocks-out-after-the-planned-clock-out-time-during-an-overtime-period"></a>Skenaario 4: Työntekijä saapuu töihin myöhässä ja poistuu töistä suunnitellun poistumisajan jälkeen ylityöajalla

Työntekijä saapuu töihin myöhässä kello 9.30 ja korvaa sitten tämän ajan jäämällä ylitöihin ja poistuu 17.00. Koska työntekijä tuli töihin myöhässä ja korvasi ajan työskentelemällä pidempään, yritys ei myönnä työntekijälle ylityölisää ajasta, jonka työntekijä työskenteli suunnitellun poistumisajan eli kello 15.30 ja työntekijän todellisen poistumisajan eli kello 17.00 väliseltä ajalta, vaikka jakso on määritetty ylityöksi aikaprofiilissa.

Tätä skenaariota varten poissaolokoodit voidaan määrittää vähentämään ylityötunteja työntekijän mahdollisella samana päivänä tapahtuneella luvattomalla poissaololla. Valitse ensin **Työajan seuranta** &gt; **Asetukset** &gt; **Ryhmät** &gt; **Poissaoloryhmät** ja sitten **Vähennä ylityötä** -valintaruutu, jos haluat poistaa ylityöaja luvattoman poissaolon työtunneilta.

Tässä kerrotaan, miten työntekijän päivän rekisteröinnit näkyvät **Hyväksyntä**-sivulla laskennan jälkeen.

| Kirjauskansion rekisteröintityyppi         | Alku    | Loppu      | Aika |
|-----------------------------------|----------|----------|------|
| Poissaolo (luvaton - töistä myöhästyminen) | 7.00 | 9.30 | 1.5  |
| Saapuminen                          | 9.30 | 9.30 |      |
| Tuotannon työ                    | 9.30 | 17.00 | 7,5  |
| Poistuminen                         | 17.30 | 17.30 |      |

Jos valitulle poissaolokoodille on valittu **Vähennä ylityötä** -valintaruutu, ylityöajan palkkaa vähennetään työntekijän luvattomien poissaolojen tuntimäärällä. Tässä tapauksessa seuraavat palkkatapahtumat luodaan rekisteröintien siirron jälkeen.

| Palkkalaji     | Maksulaji | Palkkayksiköt | Osuus |
|---------------|----------|-----------|------|
| Vakioaika | 1201     | 9:00      | 10   |
| Ylityö      | 1 301     | 0,5       | 15   |

Tässä 1,5 tuntia luvatonta poissaoloa aikana 7.00–9.30 vähentävät 2,0 tunnin verran ylitöitä aikana 15.30–17.30. Rekisteröinnin tulos on 1,5 tuntia vakiotyöaikaa ja 0,5 tuntia ylityötä.

Jos sitä vastoin valitun poissaolokoodin **Vähennä ylityötä** -valintaruutu tyhjennetään, ylityöajan palkka myönnetään työntekijälle, vaikka tämä olisi myöhässä ja vaikka poissaolokoodi olisi luvaton. Tässä tapauksessa seuraavat palkkatapahtumat luodaan rekisteröintien siirron jälkeen.

| Palkkalaji     | Maksulaji | Palkkayksiköt | Osuus |
|---------------|----------|-----------|------|
| Vakioaika | 1201     | 7,50      | 10   |
| Ylityö      | 1 301     | 2,0       | 15   |

### <a name="scenario-5-the-worker-clocks-out-before-the-planned-clock-out-time-and-can-convert-the-absence-period-to-a-flex--period"></a>Skenaario 5: Työntekijä poistuu ennen suunniteltua poistumisaikaa ja voi muuntaa poissaoloajan vajeajaksi

Seuraavassa esimerkissä näytetään, miten työntekijän liukuvan työajan tililtä voidaan tehdä vähennys muuntamalla poissaoloaika vajeajaksi.

Työntekijä saapuu työpaikalle kello 8.00 ja poistuu kello 15.30. Työntekijä on sopinut esimiehensä kanssa, että hän voi lähteä viikonlopun viettoon vähentämällä kyseiset tunnit liukuvan työajan tunneista. Kun työntekijä poistuu työpaikalta 12.00, häntä pyydetään valitsemaan poissaolokoodi, koska jäljellä olevan työpäivän poissaolo-osuus on suunnitellun vajeajan ulkopuolella. Jos työpäivän jäljellä oleva osa halutaan muuntaa vajeajaksi, työntekijä voi valita liukuvan työajan tilillä määritetyn poissaolokoodin.

Voit vähentää poissaolon työnpäivänä kirjaavien työntekijöiden liukuvan työajan tunteja valitsemalla ensin **Työajan seuranta** &gt; **Asetukset** &gt; **Ryhmät** &gt; **Poissaoloryhmät** ja sitten **Kavenna liukumaa** -valintaruudun.

Tässä kerrotaan, miten työntekijän päivän rekisteröinnit näkyvät **Hyväksyntä**-sivulla ennen laskentaa.

| Kirjauskansion rekisteröintityyppi | Alku    | Loppu      | Aika |
|---------------------------|----------|----------|------|
| Saapuminen                  | 7.00 | 7.00 |      |
| Tuotannon työ            | 7.00 | 13.00 | 6,0  |
| Poistuminen                 | 13.00 | 13.00 |      |

Jos työntekijä valitsee luvattoman poissalon poissaolokoodin, palkkatapahtuma näyttää tältä rekisteröinnin siirtämisen jälkeen.

| Palkkalaji     | Maksulaji | Palkkayksiköt | Osuus |
|---------------|----------|-----------|------|
| Vakioaika | 1201     | 6,00      | 10   |

Jos työntekijä valitsee luvattoman poissalon poissaolokoodin ja poissaolokoodi määritetään tekemään vähennys liukuvan työajan tililtä, palkkatapahtuma näyttää tältä rekisteröinnin siirtämisen jälkeen.

| Palkkalaji     | Maksulaji | Palkkayksiköt | Osuus |
|---------------|----------|-----------|------|
| Vakioaika | 1201     | 8,50      | 10   |

Tässä tapauksessa työntekijän liukuman saldo vähennetään toteutuneen lähtöajan ja suunnitellun lähtöajan välisten tuntien määrällä (eli 2,5 tunnilla 13.00–15.30 välisenä aikana).

> [!NOTE]
> Ei ole suositeltavaa, että poissaolokoodille valitaan sekä **Vähennä liukuma**- että **Vähennä ylityötä** -valintaruutu valitaan, koska tämä asetus vähentää luvattomat tunnit työntekijän ylityötunneista ja samanaikaisesti myös työntekijän liukuvan työajan tiliä vähennetään.

### <a name="scenario-6-there-is-no-planned-absence-for-the-day-and-no-worker-attendance-for-the-day"></a>Skenaario 6: Päivällä ei ole suunniteltu poissaoloaikaa eikä työntekijöiden läsnäoloa

Jos työntekijä ei tule töihin työpäivänä eikä työntekijällä ole suunniteltua poissaoloa kyseisenä päivänä, työntekijän rekisteröintien laskennassa käytetään oletuspoissaolokoodia. Voit määrittää oletuspoissaolokoodit valitsemalla **Työajan seuranta** &gt; **Työajan seurannan parametrit**. Voit sitten valita poissaolokoodin seuraavissa kentissä:

- Automaattinen liukuvan työajan lisäys
- Automaattinen poissaolon lisäys

Kun sellaisen työntekijän päivän rekisteröintejä lasketaan, jolla on käytössä liukuva työaika, **Automaattinen liukuvan työajan lisäys** -kentässä määritettyä poissaolokoodia käytetään oletuspoissaolokoodina. Jos liukuman tunnit eivät ole käytössä työntekijällä, käytetään **Automaattinen poissaolon lisäys** -kentässä määritettyä poissaolokoodia. Jos yrityksellä on työntekijöitä, joilla liukuman tunnit ovat käytössä, ja työntekijöitä, joilla ne eivät ole käytössä, molemmat parametrit on määritettävä.
