---
title: "Myynnin ja kannattavuuden suorituskyky BI virran sisältö"
description: "Tässä aiheessa kuvataan, mitä sisältyy työvaiheiden - myynti ja kannattavuus suorituskyvyn sisältö pack for Microsoft Power BI Dynamics-365. Siinä kerrotaan, kuinka voit käyttää sisällön Packin raportteja ja tietoja tietomallin ja yksiköt, joita käytetään rakentaa sisältö pack."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 260674
ms.assetid: ab457f02-929e-4d34-b813-335be3092287
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: 388b6398488e6f316c1ec07a00182e81c1dc8d08
ms.openlocfilehash: 3e6b48768bb8e69d46f1555d9300f3b878b01ff1
ms.lasthandoff: 03/31/2017


---

# <a name="sales-and-profitability-performance-power-bi-content"></a>Myynnin ja kannattavuuden suorituskyky BI virran sisältö

Tässä aiheessa kuvataan, mitä sisältyy työvaiheiden - myynti ja kannattavuus suorituskyvyn sisältö pack for Microsoft Power BI Dynamics-365. Siinä kerrotaan, kuinka voit käyttää sisällön Packin raportteja ja tietoja tietomallin ja yksiköt, joita käytetään rakentaa sisältö pack.

<a name="overview"></a>Yleiskuvaus
--------

Tämä sisältö pack on luotu myyntipäälliköt valvoa myynnin mittareita myyntituotto ja Bruttovoitto voittomarginaalit. Myynnin tapahtumiin liittyviä tietoja Dynamics 365 käyttää toimintoja ja tarjoaa asiakkaille ja tuotteille sekä koko yrityksen myyntiluvut yhteenlaskettu tutkimuksen ja myynnin erittelyn. Korostamalla muutoksia tulojen ja voiton kasvu pitkällä aikavälillä raportit voidaan ilmoitus esimiehet, positiivisten ja negatiivisten suuntausten tietoja yksittäisten asiakkaiden ja tuotteiden. Luokka ja alueellisten johtajien hyödyllistä on kaavioita, joissa vertaillaan tuoton ja kannattavuuden eri tuoteluokkien ja asiakasryhmät toisiinsa niputettuina reskontraan Hidastelijat ja johtajat. Kattava raportti, joka esittää yksittäisen asiakkaan tulot ja voittomarginaali tarjouksia account managerit tiedot varmuuskopioidaan foundation attune myynnin ja markkinoinnin pyrkimyksiä kunkin profiilin jokaiselle asiakkaalle. Myynnin ja kannattavuuden suorituskykyä sisällön Packin avulla voit analysoida myynnin suorituskyvyn käyttämällä myyntipäälliköt

-   Tuotto vuoden alusta (mukaan asiakkaan ja yksittäisten asiakkaiden, myynnin luokkaa ja yksittäisten tuotteiden ja paikkojen)
-   Liikevaihdon muutos vuoden vuosittaisen (mukaan asiakkaan alueiden ja luokat)

Kannattavuutta voidaan analysoida mukaan:

-   Bruttovoitto ja voittomarginaali (mukaan asiakkaan ja tuotteen myynnin luokat)
-   Bruttovoiton muutos vuoden-over-vuosi
-   Asiakkaan kannattavuus (mukaan käyttökate / tuotto)

## <a name="accessing-the-content-pack"></a>Sisältö pack käyttäminen
Myynnin ja kannattavuuden suorituskyky Power BI sisältö pack toteutus varoiksi Lifecycle Services (LCS) on julkaistu ja voi käyttää Dynamics 365 operaatioille. Saat lisätietoja siitä, miten käyttää ja käynnistää Power BI-raportteihin [virtaa BI sisältöä Microsoftin ja kumppanien LCS-](power-bi-content-microsoft-partners.md).

## <a name="metrics-included-in-the-content-pack"></a>Mittareita Packin sisältö
Sisältö pack sisältää raportin, joka koostuu joukko mittareita visualized laatat, kaavioiden ja taulukoiden muodossa. Seuraavassa taulukossa on yhteenveto visualisations sisältö Pack.

|                        |                                            |                                                         |
|------------------------|--------------------------------------------|---------------------------------------------------------|
| **Raportti-sivu**        | **Charts**                                 | **Laatat**                                               |
| Asiakkaan myyntituotto    | Top 10 asiakkaat tuoton mukaan                | Kokonaistuotto                                           |
|                        | Kokonaistuotto asiakasryhmän mukaan            | VS tulojen kasvu                                      |
|                        | Keskimääräinen asiakkaan tulojen mukaan asiakkaan | Käyttökate                                            |
|                        | Tuotto & Bruttovoitto asiakasryhmän mukaan   |                                                         |
| Tuotto tuotteen mukaan     | Tuotto & Bruttovoitto myyntiluokittain   | Yhteensä \#tuotteiden                                    |
|                        | Top 10 tuotetta tuoton mukaan                 | Aktiiviset tuotteet ja prosenttiosuus kokonaismäärästä kokonaismäärä |
|                        | Kokonaistuotto myyntiluokittain            | 80 prosenttia tuloista kirjanpidollinen tuotteiden määrä           |
| Tuotto jakson mukaan\*    | Myyntituotto kuukauden mukaan                           | VS tulojen kasvu                                      |
|                        | Lopussa tulot vaihtelu vs             | VS tulojen kasvu %                                    |
|                        | Yhteensä asiakkaiden alueittain Myynnin varianssi    |                                                         |
| Tuotto sijainnin mukaan    | Kaupungin myyntituotto                      |                                                         |
|                        | VS tulojen kasvu %                       |                                                         |
|                        | Myyntituoton alueen mukaan                    |                                                         |
| Asiakkaan kannattavuus | Käyttökate vs. tuotto asiakkaan mukaan   | Bruttovoitto, käyttökate, vs tulojen kasvu          |
| Kannattavuusanalyysi | Myyntituotto ja Bruttovoitto kuukauden mukaan          |                                                         |
|                        | TOP 15 asiakkaat mukaan käyttökate           |                                                         |
|                        | Bruttovoitto vs kuukausittain                 |                                                         |

\*Tulot tämän ja viime vuonna ja kasvu myynnin luokittain.

## <a name="understanding-the-data-model-and-entities"></a>Tietomallin ja yksiköiden tiedot
Työvaiheiden tietoja Dynamics 365 käytetään raportin myynnin ja kannattavuuden suorituskyvyn sisältöpaketti täyttämiseen. Se esitetään koostaa mitat, jotka lisätään yrityksen säilössä, joka on optimoitu analytics Microsoft SQL-tietokannan. Lue lisää sen blogin [Dynamics yksikön Myymälän integrointi BI virran](https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/06/09/power-bi-integration-with-entity-store-in-dynamics-ax-7-may-update/). Tämä sisältö pack koostaa mitat ovat koostaa mitat, jotka olivat käytettävissä Sales-kuution Dynamics AX 2012: n ja R3 AX 2012: n osajoukko. Vaiheittainen kuution yksikön myymälän koosta mittaukset on tehtävä ne esikunnista. Lisätietoja, katso menettelyn vaihe yksikön blogin säilöön yhteenlaskettu mittaukset [Dynamics yksikön Myymälän integrointi BI virran](https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/06/09/power-bi-integration-with-entity-store-in-dynamics-ax-7-may-update/). Sisältö pack perustana käytetään laskun rivit-yksikön seuraavat avaimen koosta mittaukset.

|               |                                              |                                                 |                                              |                                          |
|---------------|----------------------------------------------|-------------------------------------------------|----------------------------------------------|------------------------------------------|
| **Entity**    | **Avaimen koosta mittaukset**               | **Tietolähteen Dynamics 365 operaatioille** | **Field**                                    | **Description**                          |
| Laskurivit | Myyntituotto                                      | CustInvoiceTrans                                | SUM(LineAmountMST)                           | Summa kirjanpitovaluuttana            |
|               | Myytyjen tuotteiden kustannukset                           | InventTrans                                     | SUMMA (CostAmountPosted + CostAmountAdjustment) | Kustannusten summa + oikaisu                 |
|               | Komission summa – kirjanpitovaluutta | CustInvoiceTrans                                | SUM(CommissAmountMST)                        | Komission summa kirjanpitovaluuttana |

Seuraavassa taulukossa on esitetty tärkeimmät yhteenlaskettu mittaukset yksikön laskun rivit, joiden avulla voit luoda useita laskettuja mittoja sisältö pack dataset-ryhmän.

|                   |                                                                                                  |
|-------------------|--------------------------------------------------------------------------------------------------|
| **Measure**       | **Laskettuna**                                                                                |
| Bruttovoitto      | SUMMA (tuotto – MTK – komission – arvonlisävero (sisältyy asiakkaan laskurivin summaan))          |
| Käyttökate      | SUMMA (Bruttotuotto / (tuotot - arvonlisävero (sisältyy asiakkaan laskurivin summaan)))             |
| Tuotto edellisenä vuonna | Tuotto = Laske viime vuonna (summa ('laskurivit\[tulojen\]), SAMEPERIODLASTYEAR (päivämäärät\[päivämäärä\]) |

Seuraava avain mitat **Sales-kuution** käytetään suodattimena osittaa yhteenlaskettu mittausten saavuttaa suurempi rakeisuus ja syvemmälle analyyttisiä ohjeita.

|                  |                                                      |
|------------------|------------------------------------------------------|
| **Entity**       | **Esimerkkejä määritteet**                           |
| Asiakkaat        | Asiakasryhmät, alueiden asiakkaan osoite, teollisuuden |
| Tuotteet         | Tuotenumero, tuotteen nimi, nimi ryhmät       |
| Myyntiluokat | Myynnin luokkien nimet                                 |
| Oikeushenkilöt   | Oikeushenkilön nimi                                   |
| Päivämäärät            | Päivämäärät                                                |

Oletusarvon mukaan sisällön pack näyttää kuluvan kalenterivuoden tietoja, mutta voit avata raportin suodattimet-osa ja muuta Pvm-suodatus. Voit myös muuttaa oman yrityksen suodatus.

## <a name="additional-resources"></a>Lisäresurssit
Seuraavista linkeistä löydät hyödyllistä, entiteetteihin ja Power BI -sisällön rakentamiseen liittyvää tietoa:

-   [Tietoyksiköt](..\data-entities\data-entities.md)
-   [Organisaation sisältöpakettien luominen](https://powerbi.microsoft.com/en-us/documentation/powerbi-service-organizational-content-packs-introduction/)
-   [Tietojen mallinnus Power BI:n avulla](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-2-1-intro-modeling-data)
-   [Power BI -ruutujen lisääminen työtiloihin](configure-power-bi-integration.md)



