---
title: "Ostojen ja kulutuksen analyysi - Power BI -sisältö"
description: "Tässä aiheessa kuvataan, mitä kuuluu Microsoft Power BI:n ostojen ja kulutuksen analyysin sisältöpakettiin. Siinä kuvataan, miten avaat sisältöpakettiin kuuluvat raportit. Lisäksi siinä kerrotaan sisältöpaketin rakentamisessa käytetystä tietomallista ja entiteeteistä."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 265434
ms.assetid: 3cd9dfce-2687-4303-bc78-349e7cb5ea75
ms.search.region: global
ms.author: fdahl
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: Human Translation
ms.sourcegitcommit: d392b88942f4b7d7365b000df1cd69809060b910
ms.openlocfilehash: e39b1677038037cd91cfad8d104d0130bc20fb9b
ms.contentlocale: fi-fi
ms.lasthandoff: 04/26/2017


---

# <a name="purchase-spend-analysis-power-bi-content"></a>Ostojen ja kulutuksen analyysi - Power BI -sisältö

[!include[banner](../includes/banner.md)]


Tässä aiheessa kuvataan, mitä kuuluu Microsoft Power BI:n ostojen ja kulutuksen analyysin sisältöpakettiin. Siinä kuvataan, miten avaat sisältöpakettiin kuuluvat raportit. Lisäksi siinä kerrotaan sisältöpaketin rakentamisessa käytetystä tietomallista ja entiteeteistä.

<a name="overview"></a>Yleiskuvaus
--------

Microsoft Power BI:n ostojen ja kulutuksen analyysin sisältöpaketti luotiin ostopäälliköille ja budjeteista vastaaville esimiehille. Sen avulla voidaan pitää silmällä ostoja ja kulutusta. Se käyttää ostotapahtumiin liittyviä tietoja Microsoft Dynamics 365 for Operations -ohjelmasta ja tarjoaa kootun näkymän koko yrityksen ostoluvuista sekä toimittaja- ja tuotekohtaisen erittelyn ostoista ja kulutuksesta. Raportit korostavat ostojen ja kulutuksen muutoksia ajanjakson aikana. Tämän vuoksi niitä voidaan käyttää, kun esimiehille ilmoitetaan yksittäisten toimittajien ja tuotteiden positiivisista ja negatiivisista kulutussuuntauksista. Kaaviot esittävät eri hankintaluokkien ja toimittajaryhmien ostot ja kulutuksen. Nämä kaaviot saattavat auttaa luokka- ja aluepäälliköitä tunnistamaan kulutuskäyttäytymisessä tapahtuvia muutoksia. Sisältöpaketin avulla ostopäälliköt ja budjeteista vastuussa olevat esimiehet voivat analysoida ostoja ja kulutusta seuraavilla tavoilla:

-   Ostot vuoden alusta (toimittajaryhmän ja yksittäisten toimittajien, hankintaluokan ja yksittäisten tuotteiden ja toimittajan sijainnin mukaan)
-   Ostojen vuosittainen muutos (toimittajaryhmän ja hankintaluokan mukaan)

## <a name="accessing-the-content-pack"></a>Sisältöpaketin avaaminen
Ostojen ja kulutuksen analyysin sisältöpaketti julkaistaan käyttöönotettavana resurssina Microsoft Dynamics Lifecycle Services -palvelussa (LCS) ja se on käytettävissä Microsoft Dynamics 365 for Operations -ohjelmassa. Lisätietoja Power BI -raporttien käyttämisestä ja avaamisesta löydät artikkelista [Power BI -sisältö LCS:ssä Microsoftilta ja kumppaneiltasi](power-bi-content-microsoft-partners.md).
Huomautus: KB 4011327 on edellytys tämän Power BI -sisällön käytölle. Kun olet kirjautunut Lifecycle Servicesiin, pääset artikkeliin tästä: https://fix.lcs.dynamics.com/issue/results/?q=kb4011327.

## <a name="metrics-that-are-included-in-the-content-pack"></a>Mittarit, jotka sisältyvät sisältöpakettiin
Ostojen ja kulutuksen analyysin sisältöpakettiin kuuluu raportti, joka koostuu mittarijoukosta. Nämä mittarit visualisoidaan kaavioina, ruutuina ja taulukoina. Seuraavassa taulukossa on esitetty yhteenveto sisältöpaketissa käytettävistä visualisoinneista.

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

## <a name="data-model-and-entities"></a>Tietomalli ja yksiköt
Dynamics 365 for Operations -ohjelman tietoja käytetään ostojen ja kulutuksen analyysin sisältöpaketin raportoinnissa. Nämä tiedot esitetään koottuina mittauksina, jotka vaiheistetaan yksikkösäilössä, joka on analytiikkaa varten optimoitu Microsoft SQL -tietokanta. Lisätietoja yksikkösäilöstä on kohdassa [Power BI -integraatio yksikkösäilöön Dynamicsissa](https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/06/09/power-bi-integration-with-entity-store-in-dynamics-ax-7-may-update/) blog post. Sisältöpaketin koostetut mittaukset ovat alijoukko Microsoft Dynamics AX 2012:n ja AX 2012 R3:n ostokuutiossa saatavilla olleista koostetuista mittauksista. Jotta kuution koostetut mittaukset voi tallentaa yksikkösäilöön, niistä on tehtävä käyttöönottokelpoisia. Lue lisätietoja koostettujen mittausten tallentamisesta yksikkösäilöön blogikirjoituksesta [Power BI -integraatio yksikkösäilöön Dynamicsissa](https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/06/09/power-bi-integration-with-entity-store-in-dynamics-ax-7-may-update/). Seuraavat tärkeät koostetut mittaukset ovat käytettävissä suoraan laskun rivien yksiköstä. Niitä käytetään sisältöpaketin perustana.

| Kokonaisuus        | Tärkeät koostemitat | Dynamics 365 for Operationsin tietolähde | Kenttä              | kuvaus                           |
|---------------|----------------------------|---------------------------------------------|--------------------|---------------------------------------|
| Laskurivit | Osto                   | VendInvoiceTrans                            | SUM(LineAmountMST) | Summa kirjanpitovaluuttana |

Seuraavassa taulukossa esitellään tärkeät mitat, jotka lasketaan sisältöpaketissa ja jotka saadaan laskun rivien yksiköstä.

| Mitta               | Laskelma                                                                                         |
|-----------------------|-----------------------------------------------------------------------------------------------------|
| Kuluvan vuoden ostot | Kuluvan vuoden ostot = SUM('Invoice lines'\[Purchase\])                                            |
| Edellisen vuoden ostot    | Edellisen vuoden ostot = CALCULATE(SUM('Invoice lines'\[Purchase\]), SAMEPERIODLASTYEAR(Dates\[Date\])) |
| Ostojen vuosittainen kasvu   | Ostojen vuosittainen kasvu = \[Kuluvan vuoden ostot\] – \[Edellisen vuoden ostot\]                            |

Sisältöpaketin suodattimina käytetään seuraavia tärkeimpiä dimensioita osittamaan koostemitat, jotta saavutetaan suurempi rakeisuus ja saadaan syvempiä analyyttisiä näkemyksiä.

| Kokonaisuus                 | Esimerkkejä määritteistä                                |
|------------------------|-------------------------------------------------------|
| Toimittajat                | Toimittajaryhmät, toimittajan maa tai alueet, toimittajan nimi |
| Tuotteet               | Tuotenumero, tuotteen nimi, nimikeryhmien nimi        |
| Hankintaluokat | Hankintaluokka, hankintaluokkien nimet      |
| Oikeushenkilöt         | Yrityksen nimi                                     |
| Päivämäärät                  | Päivämäärät, vuosisiirtymä                                    |

Sisältöpaketissa näkyvät oletusarvoisesti kuluvan kalenterivuoden tiedot. Voit kuitenkin muuttaa päivämääräsuodatinta raportin suodatinosassa. Voit muuttaa myös yrityssuodatinta.

## <a name="additional-resources"></a>Lisäresurssit
Seuraavista linkeistä löydät hyödyllistä, entiteetteihin ja Power BI -sisällön rakentamiseen liittyvää tietoa:

-   [Tietoyksiköt](..\data-entities\data-entities.md)
-   [Organisaation sisältöpakettien luominen](https://powerbi.microsoft.com/en-us/documentation/powerbi-service-organizational-content-packs-introduction/)
-   [Tietojen mallinnus Power BI:n avulla](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-2-1-intro-modeling-data)
-   [Power BI -ruutujen lisääminen työtiloihin](configure-power-bi-integration.md)





