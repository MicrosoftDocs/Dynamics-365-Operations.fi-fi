---
title: Myynnin ja tuottavuuden suorituskyvyn Power BI -sisältö
description: Tässä artikkelissa kuvataan, mitä kuuluu myynnin ja tuottavuuden suorituskyvyn Power BI -sisältöön.
author: Henrikan
ms.date: 12/18/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.custom: 260674
ms.assetid: ab457f02-929e-4d34-b813-335be3092287
ms.search.form: SalesProfitabilityPerformancePowerBI
ms.openlocfilehash: 77271ad9f5a1d7c131e1d7750de280f0c70daaa4
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/12/2022
ms.locfileid: "9274656"
---
# <a name="sales-and-profitability-performance-power-bi-content"></a>Myynnin ja tuottavuuden suorituskyvyn Power BI -sisältö

[!include [banner](../includes/banner.md)]

Tässä artikkelissa kuvataan, mitä kuuluu **myynnin ja tuottavuuden suorituskyvyn** Microsoft Power BI -sisältöön. Siinä selitetään, miten sisältyvät Power BI -raportit avataan, sekä kerrotaan sisällön muodostamisessa käytettävistä tietomallista ja yksiköistä.

## <a name="overview"></a>Yleiskuvaus

**Myynnin ja tuottavuuden suorituskyvyn** Power BI -sisältöpaketti on tarkoitettu myyntipäälliköille myynnin avainmittareiden (tuotto, bruttovoitto ja katetuotto) seurantaan. Se käyttää myynnin tapahtumiin liittyviä tietoja ja tarjoaa kootun näkymän koko yrityksen myyntiluvuista sekä asiakas- ja tuotekohtaisen erittelyn myynnin suorituksesta.

Raportit korostaa tuoton ja voiton kasvua pitkällä aikavälillä. Tämän vuoksi raportteja voidaan käyttää, kun esimiehille ilmoitetaan yksittäisten asiakkaiden ja tuotteiden positiivisista ja negatiivisista kulutussuuntauksista. Lisäksi taulukoissa verrataan eri tuoteluokkien ja asiakasryhmien tuottoa ja kannattavuutta toisiinsa. Näin ollen luokka- ja aluepäälliköt voivat tunnistaa hitaan ja nopean kehityksen tekijät. Kattava raportti esittää yksittäisen asiakkaan tuoton verrattuna katetuottoon. Tämän ansiosta asiakaspäälliköillä on tietoon perustuvan pohja, jonka perusteella he voivat kohdistaa myynti- ja markkinointitoimet kunkin asiakkaan profiiliin.

**Myynnin ja tuottavuuden suorituskyky** -sisällön ansiosta myyntipäälliköt pystyvät analysoimaan myynnin suoritusta seuraavasti:

- Tuotto, vuoden alusta (asiakasryhmittäin ja yksittäisille asiakkaille, myyntiluokille ja yksittäisille tuotteille sekä alueille)
- Liikevaihdon muutos, vuosittainen (asiakkaan alueen ja myyntiluokan mukaan)

Kannattavuutta voidaan analysoida seuraavasti:

- Käyttökate ja katetuotto (asiakasryhmittäin ja tuotemyyntiluokittain)
- Käyttökatteen muutos, vuosittainen
- Asiakkaan kannattavuus (tuoton ja käyttökatteen suhteen mukaan)

## <a name="accessing-the-power-bi-content"></a>Power BI -sisällön käyttäminen
**Myynnin ja tuottavuuden suorituskyvyn** Power BI -sisältö näkyy **Myynnin ja tuottavuuden suorituskyky** -sivulla (**Myynti ja markkinointi** \> **Kyselyt ja raportit** \> **Myynnin suorituskykyanalyysi** \> **Myynnin ja tuottavuuden suorituskyky**).

## <a name="metrics-that-are-included-in-the-power-bi-content"></a>Mittarit, jotka sisältyvät Power BI -sisältöön
**Myynnin ja tuottavuuden suorituskyvyn** Power BI -sisältöön lukeutuu raportti, joka koostuu mittarijoukosta. Nämä mittarit visualisoidaan kaavioina, ruutuina ja taulukoina. Seuraavassa taulukossa on esitetty yhteenveto sisällön käytettävistä visualisoinneista.

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

## <a name="understanding-the-data-model-and-entities"></a>Tietomallin ja yksiköiden tiedot
**Myynnin ja tuottavuuden suorituskyvyn** Power BI -sisällön raportissa käytetään seuraavia tietoja. Nämä tiedot esitetään koottuina mittauksina, joka vaiheistetaan yksikkösäilössä. Yksikkösäilö on analytiikkaa varten optimoitu Microsoft SQL Server -tietokanta. Lisätietoja on kohdassa [Power BI:n ja yksikkösäilön integraatio](power-bi-integration-entity-store.md).

Tämän sisällön koostetut mittaukset ovat Microsoft Dynamics AX 2012:n ja Microsoft Dynamics AX 2012 R3:n myyntikuutiossa saatavilla olleiden koostettujen mittausten osajoukko. Jotta kuution koostetut mittaukset voi tallentaa yksikkösäilöön, niistä on tehtävä käyttöönottokelpoisia. Lue lisätietoja koostettujen mittausten tallentamisesta yksikkösäilöön blogikirjoituksesta [Power BI -integraatio yksikkösäilöön Dynamicsissa](/archive/blogs/dynamicsaxbi/power-bi-integration-with-entity-store-in-dynamics-ax-7-may-update).

Seuraavia tärkeitä koostettuja laskurivi-yksikön rivien mittoja käytetään sisällön perustana.

| Kokonaisuus        | Tärkeät koostemitat                   | Dynamics 365:n tietolähde | Kenttä                                        | kuvaus                                       |
|---------------|----------------------------------------------|------------------------------|----------------------------------------------|---------------------------------------------------|
| Laskurivit | Myyntituotto                                      | AsiakasLaskuTapahtuma             | SUM(LineAmountMST)                           | Summa kirjanpitovaluuttana.            |
|               | Myytyjen tuotteiden kustannukset                           | InventTrans                  | SUM(CostAmountPosted + CostAmountAdjustment) | Kustannussumman ja oikaisun summa.    |
|               | Provisiorivin summa – kirjanpitovaluutta | AsiakasLaskuTapahtuma             | SUM(CommissAmountMST)                        | Provision määrä kirjanpidon valuuttana. |

Seuraavassa taulukossa on esitetty, miten laskurivi-yksikön tärkeitä koostemittoja käytetään luomaan useita laskettuja mittoja sisällön tietojoukossa.

| Mitta           | Laskelma                                                                                      |
|-------------------|--------------------------------------------------------------------------------------------------|
| Bruttovoitto      | SUM(Tuotto – MTKUST – Provisio – Arvonlisävero (sisältyy asiakkaan laskurivin summaan))          |
| Käyttökate      | SUM(Bruttovoitto / (Tuotto – Arvonlisävero (sisältyy asiakkaan laskurivin summaan)))             |
| Tuotto edellisenä vuonna | Tuotto edellisenä vuonna = CALCULATE(SUM('Invoice lines'\[Revenue\]), SAMEPERIODLASTYEAR(Dates\[Date\]) |

Myyntikuutiossa käytetään suodattimina seuraavia tärkeimpiä dimensioita osittamaan koostemitat, jotta saavutetaan suurempi rakeisuus ja saadaan syvempiä analyyttisiä näkemyksiä.

| Kokonaisuus           | Esimerkkejä määritteistä                               |
|------------------|------------------------------------------------------|
| Asiakkaat        | Asiakasryhmät, Asiakkaan alueet, Osoite, Ala |
| Tuotteet         | Tuotenumero, tuotteen nimi, nimikeryhmien nimi       |
| Myyntiluokat | Myyntiluokkien nimet                                 |
| Oikeushenkilöt   | Yritysten nimet                                   |
| Päivämäärät            | Päivämäärät                                                |

Kuluvan kalenterivuoden tiedot näkyvät oletusarvoisesti sisällössä. Voit kuitenkin muuttaa päivämääräsuodatinta raportin suodatinosassa. Voit muuttaa myös yrityssuodatinta.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
