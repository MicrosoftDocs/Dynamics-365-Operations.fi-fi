---
title: "Power BI:n myynnin ja kannattavuuden suorituskykysisältö"
description: "Tässä aiheessa kuvataan, mitä sisältyy Microsoft Power BI:n Dynamics 365 for Operations - Myynnin ja kannattavuuden suorituskyvyn sisältöpakettiin. Siinä kuvataan, miten avaat sisältöpakettiin kuuluvat raportit. Lisäksi siinä kerrotaan sisältöpaketin rakentamisessa käytetystä tietomallista ja entiteeteistä."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 260674
ms.assetid: ab457f02-929e-4d34-b813-335be3092287
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 357f7071d801b13518c83170f8d0e7946dd9dede
ms.contentlocale: fi-fi
ms.lasthandoff: 05/25/2017


---

# <a name="sales-and-profitability-performance-power-bi-content"></a>Power BI:n myynnin ja kannattavuuden suorituskykysisältö

[!include[banner](../includes/banner.md)]


Tässä aiheessa kuvataan, mitä sisältyy Microsoft Power BI:n Dynamics 365 for Operations - Myynnin ja kannattavuuden suorituskyvyn sisältöpakettiin. Siinä kuvataan, miten avaat sisältöpakettiin kuuluvat raportit. Lisäksi siinä kerrotaan sisältöpaketin rakentamisessa käytetystä tietomallista ja entiteeteistä.

<a name="overview"></a>Yleiskuvaus
--------

Tämä sisältöpaketti on tarkoitettu myyntipäälliköille myynnin avainmittareiden (tuotto, bruttovoitto ja katetuotto) seurantaan. Se käyttää myynnin tapahtumiin liittyviä tietoja Dynamics 365 for Operations -sovelluksesta ja tarjoaa kootun näkymän koko yrityksen myyntiluvuista sekä asiakas- ja tuotekohtaisen erittelyn myynnin suorituksesta. Korostamalla muutoksia tuotoissa ja voiton kasvussa pitkällä aikavälillä, raportteja voi käyttää ilmoittamaan esimiehille tiettyjen asiakkaiden tai tuotteiden positiivisista ja negatiivisista suuntauksista. Luokka- ja aluepäälliköille voi olla hyödyllistä käyttää taulukoita, joissa verrataan eri tuoteluokkien ja asiakasryhmien tuottoa ja kannattavuutta toisiinsa, jonka perusteella voidaan erotella toisistaan johtajat ja hidastelijat. Kattava raportti, joka esittää yksittäisen asiakkaan tuoton verrattuna katetuottoon tarjoaa asiakaspäälliköille tietoon perustuvan pohjan, jonka perusteella he voivat kohdistaa myynti- ja markkinointitoimet kunkin asiakkaan profiiliin. Myynnin ja kannattavuuden suorituskykysisällön paketti antaa myyntipäälliköille mahdollisuuden analysoida myynnin suorituskykyä seuraavien mukaisesti:

-   Tuotto, vuoden alusta (asiakasryhmittäin ja yksittäisille asiakkaille, myyntiluokille ja yksittäisille tuotteille sekä alueille)
-   Liikevaihdon muutos, vuosittainen (asiakkaan alueen ja myyntiluokan mukaan)

Kannattavuuden analysointia varten on saatavilla:

-   Käyttökate ja katetuotto (asiakasryhmittäin ja tuotemyyntiluokittain)
-   Käyttökatteen muutos, vuosittainen
-   Asiakkaan kannattavuus (tuoton ja käyttökatteen suhteen mukaan)

## <a name="accessing-the-content-pack"></a>Sisältöpaketin avaaminen
Microsoft Power BI:n myynnin ja kannattavuuden suorituskyvyn sisältöpaketti julkaistaan käyttöönotettavana resurssina elinkaaripalveluissa (LCS) ja se on käytettävissä Dynamics 365 for Operations -sovelluksessa. Lisätietoja Power BI -raporttien käyttämisestä ja avaamisesta löydät artikkelista [Power BI -sisältö LCS:ssä Microsoftilta ja kumppaneiltasi](power-bi-content-microsoft-partners.md).
**Huomautus:** KB 4011327 on edellytys tämän Power BI -sisällön käytölle. Kun olet kirjautunut Lifecycle Servicesiin, pääset artikkeliin tästä: <a href="https://fix.lcs.dynamics.com/issue/results/?q=kb4011327">https://fix.lcs.dynamics.com/issue/results/?q=kb4011327</a>.

## <a name="metrics-included-in-the-content-pack"></a>Sisältöpakettiin sisältyvät mittarit
Sisältöpakettiin kuuluu raportti, joka koostuu kaavioina, ruutuina ja taulukoina esitettävästä mittarijoukosta. Seuraavassa taulukossa on esitetty yhteenveto sisältöpaketissa käytettävistä visualisoinneista.

|                        |                                            |                                                         |
|------------------------|--------------------------------------------|---------------------------------------------------------|
| **Raporttisivu**        | **Kaaviot**                                 | **Ruudut**                                               |
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
Dynamics 365 for Operations -sovelluksen tietoja käytetään Myynnin ja kannattavuuden suorituskyvyn sisältöpaketin raportin täyttämiseen. Tämä esitetään koostettuina mittauksina, jotka vaiheistetaan yksikkösäilössä, joka on analytiikkaa varten optimoitu Microsoft SQL -tietokanta. Lue lisää blogikirjoituksesta [Power BI -integraatio yksikkösäilöön Dynamicsissa](https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/06/09/power-bi-integration-with-entity-store-in-dynamics-ax-7-may-update/). Sisältöpaketin koostetut mittaukset ovat alijoukko Dynamics AX 2012:n ja AX 2012 R3:n myyntikuutiossa saatavilla olleista koostetuista mittauksista. Jotta kuution koostetut mittaukset voi tallentaa yksikkösäilöön, niistä on tehtävä käyttöönottokelpoisia. Lue lisätietoja koostettujen mittausten tallentamisesta yksikkösäilöön blogikirjoituksesta [Power BI integration with Entity Store in Dynamics](https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/06/09/power-bi-integration-with-entity-store-in-dynamics-ax-7-may-update/). Seuraavia tärkeitä koostettuja laskurivi-yksikön rivien mittoja käytetään sisältöpaketin perustana.

|               |                                              |                                                 |                                              |                                          |
|---------------|----------------------------------------------|-------------------------------------------------|----------------------------------------------|------------------------------------------|
| **Yksikkö**    | **Tärkeät koostemitat**               | **Dynamics 365 for Operationsin tietolähde** | **Kenttä**                                    | **Kuvaus**                          |
| Laskurivit | Myyntituotto                                      | AsiakasLaskuTapahtuma                                | SUM(LineAmountMST)                           | Summa kirjanpitovaluuttana            |
|               | Myytyjen tuotteiden kustannukset                           | InventTrans                                     | SUM(CostAmountPosted + CostAmountAdjustment) | Kustannussumma + oikaisu                 |
|               | Provisiorivin summa – kirjanpitovaluutta | AsiakasLaskuTapahtuma                                | SUM(CommissAmountMST)                        | Provisiorivin summa kirjanpitovaluuttana |

Seuraavassa taulukossa on esitetty, miten laskurivi-yksikön tärkeitä koostemittoja käytetään luomaan useita laskettuja mittoja sisältöpaketin tietojoukossa.

|                   |                                                                                                  |
|-------------------|--------------------------------------------------------------------------------------------------|
| **Mitta**       | **Lasketaan**                                                                                |
| Bruttovoitto      | SUM(Tuotto – MTKUST – Provisio – Arvonlisävero (sisältyy asiakkaan laskurivin summaan))          |
| Käyttökate      | SUM(Bruttovoitto / (Tuotto – Arvonlisävero (sisältyy asiakkaan laskurivin summaan)))             |
| Tuotto edellisenä vuonna | Tuotto edellisenä vuonna = CALCULATE(SUM('Invoice lines'\[Revenue\]), SAMEPERIODLASTYEAR(Dates\[Date\]) |

Suodattimina **Myyntikuutiossa** käytetään seuraavia tärkeimpiä dimensioita osittamaan koostemitat, jotta saavutetaan suurempi rakeisuus ja saadaan syvempiä analyyttisiä näkemyksiä.

|                  |                                                      |
|------------------|------------------------------------------------------|
| **Yksikkö**       | **Esimerkkejä määritteistä**                           |
| Asiakkaat        | Asiakasryhmät, Asiakkaan alueet, Osoite, Ala |
| Tuotteet         | Tuotenumero, tuotteen nimi, nimikeryhmien nimi       |
| Myyntiluokat | Myyntiluokkien nimet                                 |
| Oikeushenkilöt   | Yritysten nimet                                   |
| Päivämäärät            | Päivämäärät                                                |

Oletusarvon mukaan sisältöpaketti näyttää kuluvan kalenterivuoden tietoja, mutta raportin suodatinosan voi avata ja päivämääräsuodatinta muuttaa. Voit muuttaa myös yrityssuodatinta.

## <a name="additional-resources"></a>Lisäresurssit
Seuraavista linkeistä löydät hyödyllistä, entiteetteihin ja Power BI -sisällön rakentamiseen liittyvää tietoa:

-   [Tietoyksiköt](..\data-entities\data-entities.md)
-   [Organisaation sisältöpakettien luominen](https://powerbi.microsoft.com/en-us/documentation/powerbi-service-organizational-content-packs-introduction/)
-   [Tietojen mallinnus Power BI:n avulla](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-2-1-intro-modeling-data)
-   [Power BI -ruutujen lisääminen työtiloihin](configure-power-bi-integration.md)





