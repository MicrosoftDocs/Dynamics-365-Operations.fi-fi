---
title: "Ostojen ja kulutuksen analyysi - Power BI -sisältö"
description: "Tässä ohjeaiheessa kerrotaan, mitä osto- ja kulutusanalyysin Power BI -sisältö sisältää. Siinä selitetään, miten sisältöön sisältyvät raportit avataan, sekä kerrotaan sisällön muodostamisessa käytetyistä tietomallista ja yksiköistä."
author: FrankDahl
manager: AnnBe
ms.date: 06/16/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations, UnifiedOperations
ms.custom: 265434
ms.assetid: 3cd9dfce-2687-4303-bc78-349e7cb5ea75
ms.search.region: global
ms.author: fdahl
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 3e42746329b1194c0ce0e2fb5c476742259a5b43
ms.contentlocale: fi-fi
ms.lasthandoff: 09/29/2017

---

# <a name="purchase-spend-analysis-power-bi-content"></a>Ostojen ja kulutuksen analyysi - Power BI -sisältö

[!include[banner](../includes/banner.md)]

Tässä ohjeaiheessa kerrotaan, mitä **osto- ja kulutusanalyysin** Microsoft Power BI -sisältö sisältää. Siinä kuvataan, miten avaat Power BI -raportit. Lisäksi siinä kerrotaan sisältöpaketin rakentamisessa käytetystä tietomallista ja entiteeteistä.

## <a name="overview"></a>Yleiskuvaus

**Osto- ja kustannusanalyysin** Power BI -sisältö on suunniteltu ostopäälliköiden ja budjetista vastaavien esimiesten käyttöön, sillä auttaa seuraamaan ostoja ja kulutusta. Esimiehet voivat analysoida ostoja ja kulutusta seuraavin tavoin:

-   Ostot vuoden alusta (toimittajaryhmän ja yksittäisten toimittajien, hankintaluokan ja yksittäisten tuotteiden ja toimittajan sijainnin mukaan)
-   Ostojen vuosittainen muutos (toimittajaryhmän ja hankintaluokan mukaan)

Sisältö käyttää ostotapahtumiin liittyviä tietoja ja antaa koko yrityksen ostolukujen koostenäkymän sekä toimittaja- ja tuotekohtaisen erittelyn ostoista ja kulutuksesta. Raportit korostavat ostojen ja kulutuksen muutoksia ajanjakson aikana. Tämän vuoksi raportteja voidaan käyttää, kun esimiehille ilmoitetaan yksittäisten toimittajien ja tuotteiden positiivisista ja negatiivisista kulutussuuntauksista. Lisäksi kaaviot osoittavat eri hankintaluokkien ja toimittajaryhmien ostot ja kulutuksen. Näin ollen luokka- ja aluepäälliköitä voivat käyttää kaavioita apuna kulutuskäyttäytymisessä tapahtuvien muutoksien havaitsemisessa.

## <a name="accessing-the-power-bi-content"></a>Power BI -sisällön käyttö
Jos käytössä on Microsoft Dynamics 365 for Finance and Operations, Enterprise Editionin heinäkuun 2017 päivitys, **osto- ja kulutusanalyysin** Power BI -sisältö näkyy **Osto- ja kulutusanalyysi** -sivulla (**Hankinta** > **Kyselyt ja raportit** > **Ostojen suorituskykyanalyysi** > **Osto- ja kulutusanalyysi**). 

## <a name="metrics-that-are-included-in-the-power-bi-content"></a>Mittareita, jotka sisältyvät Power BI -sisältöön
**Ostojen ja kulutuksen analyysin** Power BI -sisältöön lukeutuu raportti, joka koostuu mittarijoukosta. Nämä mittarit visualisoidaan kaavioina, ruutuina ja taulukoina. Seuraavassa taulukossa on visualisointien yhteenveto.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th>Raporttisivu</th>
<th>Kaaviot</th>
<th>Ruudut</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Ostot toimittajan mukaan</td>
<td><ul>
<li>10 parasta toimittajaa ostojen mukaan (pinottu palkkikaavio)</li>
<li>Ostot yhteensä toimittajaryhmän/maan/nimen mukaan (ympyräkaavio)</li>
<li>Ostot toimittajaryhmän/maan/nimen mukaan (sarakekaavio)</li>
<li>Ostot keskimäärin toimittajaryhmän/maan/nimen mukaan (sarakekaavio)</li>
</ul></td>
<td><ul>
<li>Osto yhteensä</li>
<li>Ostojen vuosittainen kasvu</li>
<li>Toimittajien kokonaismäärä</li>
<li>Aktiivisten toimittajien kokonaismäärä</li>
</ul></td>
</tr>
<tr class="even">
<td>Ostot tuotteen mukaan</td>
<td><ul>
<li>Ostot hankintaluokan / tuotteen nimen mukaan (sarakekaavio)</li>
<li>Ostot yhteensä hankintaluokan / tuotteen nimen mukaan (ympyräkaavio)</li>
<li>10 parasta tuotetta ostojen mukaan (pinottu palkkikaavio)</li>
</ul></td>
<td><ul>
<li>Tuotteiden kokonaismäärä</li>
<li>Kaikkien aktiivisten tuotteiden prosenttiosuus tuotteiden kokonaismäärästä</li>
<li>Tuotteiden määrä, joista koostuu 80 % ostoista</li>
</ul></td>
</tr>
<tr class="odd">
<td>Ostot kauden mukaan*</td>
<td><ul>
<li>Ostot kuukauden/päivän mukaan (sarakekaavio)</li>
<li>Kumulatiivisten ostojen vuosittainen varianssi (vesiputouskaavio)</li>
<li>Ostot yhteensä, vuosittainen kasvu (sarakekaavio)</li>
<li>Hankintaraportti (matriisi)</li>
</ul></td>
<td><ul>
<li>Ostojen vuosittainen kasvu</li>
<li>Ostojen vuosittainen kasvuprosentti</li>
</ul></td>
</tr>
<tr class="even">
<td>Ostot toimittajan sijainnin mukaan</td>
<td><ul>
<li>Ostot kaupungin mukaan</li>
<li>Ostojen vuosittainen kasvuprosentti</li>
<li>Ostot maan mukaan</li>
</ul></td>
<td></td>
</tr>
<tr class="odd">
<td>Ostojen ja kulutuksen analyysi ajan mukaan</td>
<td><ul>
<li>Ostojen kuluva vuosi kuukauden/päivän mukaan (viivakaavio)</li>
<li>Ostojen kuluva ja edellinen vuosi (viiva- ja sarakekaavio)</li>
</ul></td>
<td></td>
</tr>
<tr class="even">
<td>Ostojen ja kulutuksen analyysi toimittajan mukaan</td>
<td><ul>
<li>10 parasta toimittajaa ostojen prosenttiosuuden mukaan (suppilokaavio)</li>
<li>10 toimittajaa, joiden vuosittainen kulutus on noussut eniten</li>
<li>10 toimittajaa, joiden vuosittainen kulutus on laskenut eniten</li>
</ul></td>
<td></td>
</tr>
</tbody>
</table>

\* Ostot tänä ja edellisenä vuonna sekä kasvu hankintaluokan mukaan

## <a name="extending-the-power-bi-content"></a>Power BI -sisällön laajentaminen
Jos käytät Microsoft Dynamics Lifecycle Servicesin (LCS) sisältöpaketteja, voit tehdä erinomaisia analyyseja henkilöille, jotka eivät käytä Microsoft Dynamics 365:tä. Voit muokata näitä sisältöpaketit sisältämään muita raportteja ja visuaalisia tietoja ja julkaista sitten sisältöpaketit analysoitavaksi Power BI.com -vuokraajassa. 

**Osto- ja kulutusanalyysin** Power BI -sisältö sijaitsee LCS:n Jaettu omaisuus -kirjastossa. Lisätietoja sisällön lataamisesta ja sen käyttöönottamisesta organisaatiossa on ohjeaiheessa [Microsoftin ja kumppaneiden Power BI -sisältö LCS-sovelluksessa](power-bi-content-microsoft-partners.md). Katso Power BI -sisällön käyttöönotosta kertova esittely Office Mixin kohdassa [Microsoftin ja kumppaneiden Power BI -sisältö Dynamics Lifecycle Services -sovelluksessa](https://mix.office.com/watch/9puyb1b2xs1w).

Muista ladata käyttämääsi Dynamics 365 -versiota vastaava **osto- ja kulutusanalyysin** sisältö.

> [!NOTE]
> Jos käytössä on Microsoft Dynamics 365 for Operations versio 1611, Power BI -sisällön edellytyksenä on KB 4011327. Kun olet kirjautunut LCS:ään, voit siirtyä tietämyskantaan osoitteessa https://fix.lcs.dynamics.com/issue/results/?q=kb4011327.

## <a name="data-model-and-entities"></a>Tietomalli ja yksiköt
Seuraavia tietoja käytetään **osto- ja kulutusanalyysin** Power BI -sisällön raporttisivujen täyttämiseen. Nämä tiedot esitetään koottuina mittauksina, joka vaiheistetaan yksikkösäilössä. Yksikkösäilö on analytiikkaa varten optimoitu Microsoft SQL Server -tietokanta. Lisätietoja on ohjeaiheessa [yleiskatsaus Power BI:n integraatiosta yksikkökaupan kanssa](power-bi-integration-entity-store.md).

Sisällön koostetut mittaukset ovat alijoukko Microsoft Dynamics AX 2012:n ja AX 2012 R3:n ostokuutiossa saatavilla olleista koostemitoista. Jotta kuution koostetut mittaukset voi tallentaa yksikkösäilöön, niistä on tehtävä käyttöönottokelpoisia. Lisätietoja koostettujen mittojen tallentamisesta yksikkösäilöön on ohjeaiheessa [Power BI:n ja yksikkösäilön integroinnin yleiskatsaus](power-bi-integration-entity-store.md). Seuraavat tärkeät koostemitat ovat käytettävissä suoraan laskun rivien yksiköstä. Niitä käytetään sisällön perustana.

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
