---
title: Osto- ja kulutusanalyysin Power BI -sisältö
description: Tässä artikkelissa kerrotaan, mitä osto- ja kulutusanalyysin Power BI -sisältöön kuuluu.
author: FrankDahl
ms.date: 04/24/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: kamaybac
ms.search.region: global
ms.author: fdahl
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.custom: 265434
ms.assetid: 3cd9dfce-2687-4303-bc78-349e7cb5ea75
ms.search.form: PurchaseSpendAnalysisPowerBI
ms.openlocfilehash: 757b782131617104422e15f3ceec747b92d96666
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/12/2022
ms.locfileid: "9276657"
---
# <a name="purchase-spend-analysis-power-bi-content"></a>Osto- ja kulutusanalyysin Power BI -sisältö

[!include [banner](../includes/banner.md)]

Tässä artikkelissa kerrotaan, mitä **osto- ja kulutusanalyysin** Microsoft Power BI -sisältöön kuuluu. Siinä selitetään, miten sisältyvät Power BI -raportit avataan, sekä kerrotaan sisällön muodostamisessa käytettävistä tietomallista ja yksiköistä.

## <a name="overview"></a>Yleiskuvaus

**Osto- ja kustannusanalyysin** Power BI -sisältö on suunniteltu ostopäälliköiden ja budjetista vastaavien esimiesten käyttöön, sillä auttaa seuraamaan ostoja ja kulutusta. Esimiehet voivat analysoida ostoja ja kulutusta seuraavin tavoin:

- Ostot vuoden alusta (toimittajaryhmän ja yksittäisten toimittajien, hankintaluokan ja yksittäisten tuotteiden ja toimittajan sijainnin mukaan)
- Ostojen vuosittainen muutos (toimittajaryhmän ja hankintaluokan mukaan)

Sisältö käyttää ostotapahtumiin liittyviä tietoja ja antaa koko yrityksen ostolukujen koostenäkymän sekä toimittaja- ja tuotekohtaisen erittelyn ostoista ja kulutuksesta. Raportit korostavat ostojen ja kulutuksen muutoksia ajanjakson aikana. Tämän vuoksi raportteja voidaan käyttää, kun esimiehille ilmoitetaan yksittäisten toimittajien ja tuotteiden positiivisista ja negatiivisista kulutussuuntauksista. Lisäksi kaaviot osoittavat eri hankintaluokkien ja toimittajaryhmien ostot ja kulutuksen. Näin ollen luokka- ja aluepäälliköitä voivat käyttää kaavioita apuna kulutuskäyttäytymisessä tapahtuvien muutoksien havaitsemisessa.

## <a name="accessing-the-power-bi-content"></a>Power BI -sisällön käyttäminen
**Osto- ja kulutusanalyysin** Power BI -sisältö näkyy **Osto- ja kulutusanalyysi** -sivulla (**Hankinta** \> **Kyselyt ja raportit** \> **Ostojen suorituskykyanalyysi** \> **Osto- ja kulutusanalyysi**).

## <a name="metrics-that-are-included-in-the-power-bi-content"></a>Mittarit, jotka sisältyvät Power BI -sisältöön
**Ostojen ja kulutuksen analyysin** Power BI -sisältöön kuuluu raportti, joka koostuu mittarijoukosta. Nämä mittarit visualisoidaan kaavioina, ruutuina ja taulukoina. 

Seuraavassa osissa on visualisointien yhteenveto.

### <a name="purchase-by-vendor-report-page"></a>Ostot toimittajan mukaan -raporttisivu
**Kaaviot**
- 10 parasta toimittajaa ostojen mukaan (pinottu palkkikaavio)
- Ostot yhteensä toimittajaryhmän/maan/nimen mukaan (ympyräkaavio)
- Ostot toimittajaryhmän/maan/nimen mukaan (sarakekaavio)
- Ostot keskimäärin toimittajaryhmän/maan/nimen mukaan (sarakekaavio)

**Ruudut**
- Osto yhteensä
- Ostojen vuosittainen kasvu
- Toimittajien kokonaismäärä
- Aktiivisten toimittajien kokonaismäärä

**Esimerkki**
<img src="media/spend1.png" alt="Purchase by vendor">

### <a name="purchase-by-product-report-page"></a>Ostot tuotteen mukaan -raporttisivu

**Kaaviot**
- Ostot hankintaluokan / tuotteen nimen mukaan (sarakekaavio)
- Ostot yhteensä hankintaluokan / tuotteen nimen mukaan (ympyräkaavio)
- 10 parasta tuotetta ostojen mukaan (pinottu palkkikaavio)

**Ruudut**
- Tuotteiden kokonaismäärä</li>
- Kaikkien aktiivisten tuotteiden prosenttiosuus tuotteiden kokonaismäärästä
- Tuotteiden määrä, joista koostuu 80 % ostoista

**Esimerkki**


<img src="media/purchaseByProduct.png" alt="Purchase by Product">

### <a name="purchase-by-period-report-page"></a>Ostot ajanjakson mukaan -raporttisivu
Tällä sivulla nähdään ostot tänä ja edellisenä vuonna sekä kasvu hankintaluokan mukaan.

**Kaaviot** 
- Ostot kuukauden/päivän mukaan (sarakekaavio)
- Kumulatiivisten ostojen vuosittainen varianssi (vesiputouskaavio)
- Ostot yhteensä, vuosittainen kasvu (sarakekaavio)
- Hankintaraportti (matriisi)

**Ruudut**
- Ostojen vuosittainen kasvu
- Ostojen vuosittainen kasvuprosentti

**Esimerkki**
<img src="media/purchaseByPeriod.png" alt="Purchase by Period">

### <a name="purchase-by-vendor-location-report-page"></a>Ostot toimittajan toimipaikan mukaan -raporttisivu

**Kaaviot**
- Ostot kaupungin mukaan
- Ostojen vuosittainen kasvuprosentti
- Ostot maan mukaan

**Esimerkki**
<img src="media/purchByVendorLocation.png" alt="Purchase by Vendor Location">

### <a name="purchase-spend-analysis-by-time-report-page"></a>Ostojen ja kulutuksen analyysi ajan mukaan -raporttisivu

**Kaaviot** 
- Ostojen kuluva vuosi kuukauden/päivän mukaan (viivakaavio)
- Ostojen kuluva ja edellinen vuosi (viiva- ja sarakekaavio)

**Esimerkki**
<img src="media/PurchByTIme.png" alt="Purchase by Time">

### <a name="purchase-spend-analysis-by-vendor-report-page"></a>Ostojen ja kulutuksen analyysi toimittajan mukaan -raporttisivu

**Kaaviot** 
- 10 parasta toimittajaa ostojen prosenttiosuuden mukaan (suppilokaavio)
- 10 toimittajaa, joiden vuosittainen kulutus on noussut eniten
- 10 toimittajaa, joiden vuosittainen kulutus on laskenut eniten

**Esimerkki** 
<img src="media/PurchSpendAnalysisByVendor.png" alt="Purchase spend by vendor">


## <a name="data-model-and-entities"></a>Tietomalli ja yksiköt
Seuraavia tietoja käytetään **osto- ja kulutusanalyysin** Power BI -sisällön raporttisivujen täyttämiseen. Nämä tiedot esitetään koottuina mittauksina, joka vaiheistetaan yksikkösäilössä. Yksikkösäilö on analytiikkaa varten optimoitu Microsoft SQL Server -tietokanta. Lisätietoja on kohdassa [Power BI:n ja yksikkösäilön integraatio](power-bi-integration-entity-store.md).

Sisällön koostetut mittaukset ovat alijoukko Microsoft Dynamics AX 2012:n ja Microsoft Dynamics AX 2012 R3:n ostokuutiossa saatavilla olleista koostetuista mittauksista. Jotta kuution koostetut mittaukset voi tallentaa yksikkösäilöön, niistä on tehtävä käyttöönottokelpoisia. Lisätietoja koostettujen mittojen tallentamisesta yksikkösäilöön on kohdassa [Power BI:n ja yksikkösäilön integrointi](power-bi-integration-entity-store.md). Seuraavat tärkeät koostemitat ovat käytettävissä suoraan laskun rivien yksiköstä. Niitä käytetään sisällön perustana.

| Kokonaisuus        | Tärkeät koostemitat | Tietolähde                                 | Kenttä              | kuvaus                            |
|---------------|----------------------------|---------------------------------------------|--------------------|----------------------------------------|
| Laskurivit | Osto                   | VendInvoiceTrans                            | SUM(LineAmountMST) | Summa kirjanpitovaluuttana. |

Seuraavassa taulukossa esitellään tärkeät mitat, jotka lasketaan sisällössä ja jotka saadaan laskun rivien yksiköstä.

| Mitta               | Laskelma                                                                                         |
|-----------------------|-----------------------------------------------------------------------------------------------------|
| Kuluvan vuoden ostot | Kuluvan vuoden ostot = SUM('Invoice lines'\[Purchase\])                                            |
| Edellisen vuoden ostot    | Edellisen vuoden ostot = CALCULATE(SUM('Invoice lines'\[Purchase\]), SAMEPERIODLASTYEAR(Dates\[Date\])) |
| Ostojen vuosittainen kasvu   | Ostojen vuosittainen kasvu = \[Kuluvan vuoden ostot\] – \[Edellisen vuoden ostot\]                            |

Seuraavia sisällön tärkeitä dimensioita käytetään koostemittojen ositussuodattimina. Tämä parantaa rakeisuutta ja sen avulla saadaan entistä tarkempaa analyysitietoa.

| Kokonaisuus                 | Esimerkkejä määritteistä                                |
|------------------------|-------------------------------------------------------|
| Toimittajat                | Toimittajaryhmät, toimittajan maa tai alueet, toimittajan nimi |
| Tuotteet               | Tuotenumero, tuotteen nimi, nimikeryhmien nimi        |
| Hankintaluokat | Hankintaluokka, hankintaluokkien nimet      |
| Oikeushenkilöt         | Yrityksen nimi                                     |
| Päivämäärät                  | Päivämäärät, vuosisiirtymä                                    |

Kuluvan kalenterivuoden tiedot näkyvät oletusarvoisesti sisällössä. Voit kuitenkin muuttaa päivämääräsuodatinta raportin suodatinosassa. Voit muuttaa myös yrityssuodatinta.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
