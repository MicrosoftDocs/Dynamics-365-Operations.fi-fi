---
title: "Myynnin ja kannattavuuden suorituskyvyn Power BI -sisältö"
description: "Tässä aiheessa kuvataan, mitä kuuluu myynnin ja tuottavuuden suorituskyvyn Power BI -sisältöön. Siinä kuvataan, miten avaat Power BI -raportit. Lisäksi siinä kerrotaan sisältöpaketin rakentamisessa käytetystä tietomallista ja entiteeteistä."
author: YuyuScheller
manager: AnnBe
ms.date: 06/16/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, IT Pro
ms.search.scope: Core, Operations, UnifiedOperations
ms.custom: 260674
ms.assetid: ab457f02-929e-4d34-b813-335be3092287
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: Human Translation
ms.sourcegitcommit: 869151f2486b7a481e4694cfb6992d0ee2cfc008
ms.openlocfilehash: 16fef86e330a392ddd888fcb46060c3e1efa87c5
ms.contentlocale: fi-fi
ms.lasthandoff: 06/13/2017


---

# Myynnin ja kannattavuuden suorituskyvyn Power BI -sisältö
<a id="sales-and-profitability-performance-power-bi-content" class="xliff"></a>

[!include[banner](../includes/banner.md)]

Tässä aiheessa kuvataan, mitä kuuluu **Myynnin ja tuottavuuden suorituskyvyn** Power BI -sisältöön. Siinä kuvataan, miten avaat Power BI -raportit. Lisäksi siinä kerrotaan sisältöpaketin rakentamisessa käytetystä tietomallista ja entiteeteistä.

## Yleiskuvaus
<a id="overview" class="xliff"></a>

**Myynnin ja tuottavuuden suorituskyky** Power BI -sisältöpaketti on tarkoitettu myyntipäälliköille myynnin avainmittareiden (tuotto, bruttovoitto ja katetuotto) seurantaan. Se käyttää myynnin tapahtumiin liittyviä tietoja ja tarjoaa kootun näkymän koko yrityksen myyntiluvuista sekä asiakas- ja tuotekohtaisen erittelyn myynnin suorituksesta.

Raportit korostaa tuoton ja voiton kasvua pitkällä aikavälillä. Tämän vuoksi raportteja voidaan käyttää, kun esimiehille ilmoitetaan yksittäisten asiakkaiden ja tuotteiden positiivisista ja negatiivisista kulutussuuntauksista. Lisäksi taulukoissa verrataan eri tuoteluokkien ja asiakasryhmien tuottoa ja kannattavuutta toisiinsa. Näin ollen luokka- ja aluepäälliköt voivat tunnistaa hitaan ja nopean kehityksen tekijät. Kattava raportti esittää yksittäisen asiakkaan tuoton verrattuna katetuottoon. Tämän ansiosta asiakaspäälliköillä on tietoon perustuvan pohja, jonka perusteella he voivat kohdistaa myynti- ja markkinointitoimet kunkin asiakkaan profiiliin. 

**Myynnin ja tuottavuuden suorituskyky** -sisällön ansiosta myyntipäälliköt pystyvät analysoimaan myynnin suoritusta seuraavasti:

-   Tuotto, vuoden alusta (asiakasryhmittäin ja yksittäisille asiakkaille, myyntiluokille ja yksittäisille tuotteille sekä alueille)
-   Liikevaihdon muutos, vuosittainen (asiakkaan alueen ja myyntiluokan mukaan)

Kannattavuutta voidaan analysoida seuraavasti:

-   Käyttökate ja katetuotto (asiakasryhmittäin ja tuotemyyntiluokittain)
-   Käyttökatteen muutos, vuosittainen
-   Asiakkaan kannattavuus (tuoton ja käyttökatteen suhteen mukaan)

## Power BI -sisällön käyttö
<a id="accessing-the-power-bi-content" class="xliff"></a>
Jos käytössä on Microsoft Dynamics 365 for Finance and Operations, Enterprise Editionin heinäkuun 2017 -päivitys, **Myynnin ja tuottavuuden suorituskyky** Power BI -sisältö näytetään **Myynnin ja tuottavuuden suorituskyky** -sivulla (**Myynti ja markkinointi** > **Kyselyt ja raportit** > **Myynnin suorituskyvyn analyysi** > **Myynnin ja markkinoinnin suorituskyky**). 

## Mittareita, jotka sisältyvät Power BI -sisältöön
<a id="metrics-that-are-included-in-the-power-bi-content" class="xliff"></a>
**Myynnin ja tuottavuuden suorituskyky** Power BI -sisältöön lukeutuu raportti, joka koostuu mittarijoukosta. Nämä mittarit visualisoidaan kaavioina, ruutuina ja taulukoina. Seuraavassa taulukossa on esitetty yhteenveto sisällön käytettävistä visualisoinneista.

| Raporttisivu            | Kaaviot                                     | Ruudut                                                   |
|------------------------|--------------------------------------------|---------------------------------------------------------|
| Asiakaskohtainen tuotto    | 10 parasta asiakasta tuoton mukaan                | Kokonaistuotto                                           |
|                        | Kokonaistuotto asiakasryhmän mukaan            | Vuosittainen tuoton kasvu                                      |
|                        | Keskimääräinen asiakkaan tuotto asiakasryhmän mukaan | Käyttökate                                            |
|                        | Tuotto & bruttovoitto asiakasryhmän mukaan   |                                                         |
| Tuotto tuotteen mukaan     | Tuotto & bruttovoitto myyntiluokittain   | Tuotteet yhteensä, \#                                    |
|                        | 10 parasta tuotetta tuoton mukaan                 | Aktiivisten tuotteiden kokonaismäärä ja prosenttiosuus kokonaismäärästä |
|                        | Kokonaistuotto myyntiluokittain            | Tuotteiden määrä, joista koostuu 80 % tuotosta           |
| Tuotto kauden mukaan\*    | Tuotto kuukauden mukaan                           | Vuosittainen tuoton kasvu                                      |
|                        | Laskeva tuottovarianssi, vuosittainen             | Vuosittainen tuoton kasvu %                                    |
|                        | Myynnin kokonaisvarianssi asiakkaan alueen mukaan    |                                                         |
| Tuotto sijainnin mukaan    | Myyntituotto kaupungeittain                      |                                                         |
|                        | Vuosittainen tuoton kasvu %                       |                                                         |
|                        | Myyntituotto alueen mukaan                    |                                                         |
| Asiakkaan kannattavuus | Käyttökatteen ja tuoton suhde, asiakkaittain   | Bruttovoitto, käyttökate, vuosittainen tuoton kasvu          |
| Kannattavuusanalyysi | Kuukausittainen tuotto ja bruttovoitto          |                                                         |
|                        | 15 parasta asiakasta käyttökatteen mukaan           |                                                         |
|                        | Bruttovoitto kuukausittain, vuosittainen                 |                                                         |

\* Tuotto tänä ja viime vuonna, ja kasvu myyntiluokittain.

## Power BI -sisällön laajentaminen
<a id="extending-the-power-bi-content" class="xliff"></a>
Jos käytät Microsoft Dynamics Lifecycle Servicesin (LCS) sisältöpaketteja, voit tehdä erinomaisia analyyseja henkilöille, jotka eivät käytä Microsoft Dynamics 365:tä. Voit muokata näitä sisältöpaketit sisältämään muita raportteja ja visuaalisia tietoja ja julkaista sitten sisältöpaketit analysoitavaksi Power BI.com -vuokraajassa.

**Myynnin ja tuottavuuden suorituskyky** – Power BI -sisältö sijaitsee LCS:n Jaettu omaisuus -kirjastossa. Lisätietoja sisällön lataamisesta ja sen käyttöönottamisesta organisaatiossa on ohjeaiheessa [Microsoftin ja kumppaneiden Power BI -sisältö LCS-sovelluksessa](power-bi-content-microsoft-partners.md). Katso Power BI -sisällön käyttöönotosta kertova esittely Office Mixin kohdassa [Microsoftin ja kumppaneiden Power BI -sisältö Dynamics Lifecycle Services -sovelluksessa](https://mix.office.com/watch/9puyb1b2xs1w).

Muista ladata käyttämääsi Dynamics 365 -versiota vastaava **Myynnin ja tuottavuuden suorituskyky** -sisältö.

> [!NOTE]
> Jos käytössä on Microsoft Dynamics 365 for Operations versio 1611, Power BI -sisällön edellytyksenä on KB 4011327. Kun olet kirjautunut LCS:ään, voit siirtyä tietämyskantaan osoitteessa https://fix.lcs.dynamics.com/issue/results/?q=kb4011327.

## Tietomallin ja yksiköiden tiedot
<a id="understanding-the-data-model-and-entities" class="xliff"></a>
**Myynnin ja tuottavuuden suorituskyky** – Power BI -sisällön raportissa käytetään seuraavia tietoja. Nämä tiedot esitetään koottuina mittauksina, joka vaiheistetaan yksikkösäilössä. Yksikkösäilö on analytiikkaa varten optimoitu Microsoft SQL Server -tietokanta. Lisätietoja on ohjeaiheessa [yleiskatsaus Power BI:n integraatiosta yksikkökaupan kanssa](power-bi-integration-entity-store.md). 

Sisällön koostetut mittaukset ovat alijoukko Microsoft Dynamics AX 2012:n ja AX 2012 R3:n myyntikuutiossa saatavilla olleista koostemitoista. Jotta kuution koostetut mittaukset voi tallentaa yksikkösäilöön, niistä on tehtävä käyttöönottokelpoisia. Lue lisätietoja koostettujen mittausten tallentamisesta yksikkösäilöön blogikirjoituksesta [Power BI -integraatio yksikkösäilöön Dynamicsissa](https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/06/09/power-bi-integration-with-entity-store-in-dynamics-ax-7-may-update/). 

Seuraavia tärkeitä koostettuja laskurivi-yksikön rivien mittoja käytetään sisällön perustana.

| Kokonaisuus        | Tärkeät koostemitat                   | Dynamics 365:n tietolähde                    | Kenttä                                        | kuvaus                                   |
|---------------|----------------------------------------------|-------------------------------------------------|----------------------------------------------|----------------------------------------------|
| Laskurivit | Myyntituotto                                      | AsiakasLaskuTapahtuma                                | SUM(LineAmountMST)                           | Summa kirjanpitovaluuttana.            |
|               | Myytyjen tuotteiden kustannukset                           | InventTrans                                     | SUM(CostAmountPosted + CostAmountAdjustment) | Kustannussumman ja oikaisun summa.    |
|               | Provisiorivin summa – kirjanpitovaluutta | AsiakasLaskuTapahtuma                                | SUM(CommissAmountMST)                        | Provision määrä kirjanpidon valuuttana. |

Seuraavassa taulukossa on esitetty, miten laskurivi-yksikön tärkeitä koostemittoja käytetään luomaan useita laskettuja mittoja sisällön tietojoukossa.

| Mitta           | Laskelma                                                                                      |
|-------------------|--------------------------------------------------------------------------------------------------|
| Bruttovoitto      | SUM(Tuotto – MTKUST – Provisio – Arvonlisävero (sisältyy asiakkaan laskurivin summaan))          |
| Käyttökate      | SUM(Bruttovoitto / (Tuotto – Arvonlisävero (sisältyy asiakkaan laskurivin summaan)))             |
| Tuotto edellisenä vuonna | Tuotto edellisenä vuonna = CALCULATE(SUM('Invoice lines'\[Revenue\]), SAMEPERIODLASTYEAR(Dates\[Date\]) |

Suodattimina myyntikuutiossa käytetään seuraavia tärkeimpiä dimensioita osittamaan koostemitat, jotta saavutetaan suurempi rakeisuus ja saadaan syvempiä analyyttisiä näkemyksiä.

| Kokonaisuus           | Esimerkkejä määritteistä                               |
|------------------|------------------------------------------------------|
| Asiakkaat        | Asiakasryhmät, Asiakkaan alueet, Osoite, Ala |
| Tuotteet         | Tuotenumero, tuotteen nimi, nimikeryhmien nimi       |
| Myyntiluokat | Myyntiluokkien nimet                                 |
| Oikeushenkilöt   | Yritysten nimet                                   |
| Päivämäärät            | Päivämäärät                                                |

Kuluvan kalenterivuoden tiedot näkyvät oletusarvoisesti sisällössä. Voit kuitenkin muuttaa päivämääräsuodatinta raportin suodatinosassa. Voit muuttaa myös yrityssuodatinta.

