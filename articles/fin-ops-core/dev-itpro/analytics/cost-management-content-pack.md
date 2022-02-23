---
title: Kustannushallinnan Power BI -sisältöpaketti
description: Tässä aiheessa kuvataan, mitä kuuluu kustannushallinnan Power BI -sisältöön.
author: ShylaThompson
manager: AnnBe
ms.date: 03/16/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: CostAdminWorkspace, CostAnalysisWorkspace, CostObjectWithLowestAccuracy, CostVarianceChart, CostObjectWithLowestTurn
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 270314
ms.assetid: 9680d977-43c8-47a7-966d-2280ba21402a
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kfend
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: bd5558c89130b48595a9b889072a18a4416b5bd7
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/05/2020
ms.locfileid: "4683892"
---
# <a name="cost-management-power-bi-content"></a>Kustannushallinnan Power BI -sisältöpaketti

[!include [banner](../includes/banner.md)]

## <a name="overview"></a>Yleiskuvaus

**Kustannushintojen hallinnan** Microsoft Power BI -sisältö on tarkoitettu varaston kirjanpitäjille tai organisaation henkilöille, jotka ovat vastuussa tai kiinnostuneita varaston tilasta tai keskeneräisistä töistä tai jotka ovat vastuussa tai kiinnostuneita standardikustannusvarianssien analysoinnista.

> [!NOTE]
> Tässä ohjeaiheessa käsitelty **kustannushintojen hallinnan** Power BI -sisältö koskee versiota Dynamics 365 Finance and Operations 8.0.
> 
> AppSource-sivustoon julkaistu **kustannushintojen hallinnan** Power BI -sisältöpaketti on vanhentunut. Lisätietoja tästä vanhentumisesta on kohdassa [Finance and Operationsin poistetut tai vanhentuneet toiminnot](../migration-upgrade/deprecated-features.md#power-bi-content-packs-available-on-appsource).

Tämä Power BI -sisältö antaa luokitellun muodon, joka auttaa seuraamaan varastojen toimintaa ja visualisoimaan niiden kautta kulkevat kustannusvirrat. Saat johdon tarvitsemia tietoja esimerkiksi kiertonopeudesta, ajasta päivinä, jonka varasto on käytettävissä, tarkkuudesta ja ABC-luokittelusta valitsemallasi koostetasolla (yritys, nimike, nimikeryhmä tai toimipaikka). Näitä tietoja voidaan käyttää myös raportin eriteltynä täydennyksenä.

Power BI -sisältö perustuu **CostObjectStatementCacheMonthly**-koostemittaan, jonka ensisijainen tietolähde on **CostObjectStatementCache**-taulu. tietojoukon välimuistin kehys hallitsee tätä taulua. Taulu päivitetään oletusarvoisesti 24 tunnin välein, mutta voit muuttaa päivitysväliä tai ottaa käyttöön manuaaliset päivitykset tietojoukon välimuistin määrityksissä. Manuaaliset päivitykset suoritetaan joko **Kustannuslaskenta**- tai **Kustannusanalyysi**-työtilassa.

**CostObjectStatementCacheMonthly**-koostemitta on päivitettävä jokaisen **CostObjectStatementCache**-taulun päivityksen jälkeen ennen Power BI -visualisointien tietojen päivitystä.

## <a name="accessing-the-power-bi-content"></a>Power BI -sisällön käyttäminen

**Kustannushintojen hallinnan** Power BI -sisältö näkyy **Kustannuslaskenta**- ja **Kustannusanalyysi**-työtiloissa.

**Kustannuslaskenta**-työtilassa on seuraavat välilehdet:

- **Yhteenveto** – välilehti sisältää sovelluksen tiedot.
- **Varaston kirjanpidon tila** – tässä välilehdessä on Power BI -sisältöä.
- **Valmistuksen kirjanpidon tila** – tässä välilehdessä on Power BI -sisältöä.

**Kustannusanalyysi**-työtilassa on seuraavat välilehdet:

- **Yhteenveto** – välilehti sisältää sovelluksen tiedot.
- **Varaston kirjanpidon analyysi** – tässä välilehdessä on Power BI -sisältöä.
- **Valmistuksen kirjanpidon analyysi** – tässä välilehdessä on Power BI -sisältöä.
- **Standardikustannusten varianssianalyysi** – tässä välilehdessä on Power BI -sisältöä.

## <a name="report-pages-that-are-included-in-the-power-bi-content"></a>Power BI -sisältöön sisältyvät raporttisivut

**Kustannushintojen hallinnan** Power BI -sisältö sisältää mittarijoukosta koostuvan joukon raporttisivuja. Nämä mittarit visualisoidaan kaavioina, ruutuina ja taulukoina. 

Seuraavassa taulukossa on yleiskatsaus **kustannushintojen hallinnan** Power BI -sisällön visualisoinneista.

### <a name="inventory-accounting-status"></a>Varaston kirjanpidon tila

| Raporttisivu                               | Visualisointi                                   |
|-------------------------------------------|-------------------------------------------------|
| Varaston yleiskuvaus                        | Alkusaldo                               |
|                                           | Nettomuutos                                      |
|                                           | Nettomuutos-%                                    |
|                                           | Loppusaldo                                  |
|                                           | Varaston tarkkuus                              |
|                                           | Varaston kiertonopeus                        |
|                                           | Varastopäiviä käytettävissä                          |
|                                           | Kauden aktiivinen tuote                        |
|                                           | Kauden aktiiviset kustannusobjektit                   |
|                                           | Saldo nimikeryhmän mukaan                           |
|                                           | Saldo toimipaikan mukaan                                 |
|                                           | Luokkakohtainen raportti                           |
|                                           | Nettomuutos neljännesvuosittain                           |
| Varaston yleiskuvaus toimipaikan ja nimikeryhmän mukaan | Varaston tarkkuus toimipaikan mukaan                      |
|                                           | Varaston kiertonopeus toimipaikan mukaan                |
|                                           | Varaston loppusaldo toimipaikan mukaan                |
|                                           | Varaston tarkkuuden nimikeryhmän mukaan                |
|                                           | Varaston kiertonopeus nimikeryhmän mukaan          |
|                                           | Varaston loppusaldo toimipaikan ja nimikeryhmän mukaan |
| Varastoraportti                       | Varastoraportti                             |
| Varastoraportti toimipaikan mukaan               | Varastoraportti toimipaikan mukaan                     |
| Varastoraportti tuotehierarkian mukaan  | Varastoraportti                             |
| Varastoraportti tuotehierarkian mukaan  | Varastoraportti toimipaikan mukaan                     |

### <a name="manufacturing-accounting-status"></a>Valmistuksen kirjanpidon tila

| Raporttisivu                | Visualisointi                       |
|----------------------------|-------------------------------------|
| KET-yhteenveto vuoden alusta           | Alkusaldo                   |
|                            | Nettomuutos                          |
|                            | Nettomuutos-%                        |
|                            | Loppusaldo                      |
|                            | KET-kiertonopeus                  |
|                            | Päivän käytettävissä oleva KET                    |
|                            | Kauden aktiivinen kustannusobjekti        |
|                            | Nettomuutos resurssiryhmän mukaan        |
|                            | Saldo toimipaikan mukaan                     |
|                            | Luokkakohtainen raportti               |
|                            | Nettomuutos neljännesvuosittain               |
| KET-raportti              | Alkusaldo                   |
|                            | Loppusaldo                      |
|                            | Luokkakohtainen KET-raportti           |
| KET-raportti toimipaikan mukaan      | Alkusaldo                   |
|                            | Loppusaldo                      |
|                            | Luokka- ja toimipaikkakohtainen KET-raportti  |
| KET-raportti hierarkian mukaan | Alkusaldo                   |
|                            | Loppusaldo                      |
|                            | KET-raportti luokkahierarkian mukaan |

### <a name="inventory-accounting-analysis"></a>Varaston kirjanpidon analyysi

| Raporttisivu        | Visualisointi                                                                |
|--------------------|------------------------------------------------------------------------------|
| Varaston tiedot  | 10 parasta resurssia loppusaldon mukaan                                           |
|                    | 10 parasta resurssia nettomuutoksen kasvun mukaan                                      |
|                    | 10 parasta resurssia nettomuutoksen laskun mukaan                                      |
|                    | 10 parasta resurssia varaston kiertonopeuden mukaan                                 |
|                    | Resurssit varaston pienen kiertonopeuden ja kynnysarvon ylittävän loppusaldon mukaan |
|                    | 10 parasta resurssia pienen varaston tarkkuuden mukaan                                             |
| ABC-luokittelu | Varaston loppusaldo                                                     |
|                    | Kulutettu materiaali                                                            |
|                    | Myyty (myytyjen tuotteiden kustannukset)                                                                  |
| Varastotrendit   | Varaston loppusaldo                                                     |
|                    | Varaston nettomuutos                                                         |
|                    | Varaston kiertonopeus                                                     |
|                    | Varaston tarkkuus                                                           |

### <a name="manufacturing-accounting-analysis"></a>Valmistuksen kirjanpidon analyysi

| Raporttisivu | Visualisointi      |
|-------------|--------------------|
| KET-trendit  | KET-loppusaldo |
|             | KET-nettomuutos     |
|             | KET-kiertonopeus |

### <a name="std-cost-variance-analysis"></a>Standardikustannusten varianssianalyysi

| Raporttisivu                             | Visualisointi                                        |
|-----------------------------------------|------------------------------------------------------|
| Ostohintavarianssi (vakiokustannus) vuoden alusta | Hankitun saldo                                     |
|                                         | Ostohintavarianssi                              |
|                                         | Ostohintavarianssin suhde                        |
|                                         | Varianssi nimikeryhmän mukaan                               |
|                                         | Varianssi toimipaikan mukaan                                     |
|                                         | Ostohinta vuosineljänneksen mukaan                            |
|                                         | Ostohinta vuosineljänneksen ja nimikeryhmän mukaan             |
|                                         | 10 parasta resurssia epäsuotuisan ostohinnan suhteen mukaan |
|                                         | 10 parasta resurssia suotuisan ostohinnan suhteen mukaan   |
| Tuotannon varianssi (vakiokustannus) vuoden alusta     | Valmistuskustannus                                    |
|                                         | Tuotannon varianssi                                  |
|                                         | Tuotannon varianssin suhde                            |
|                                         | Varianssi nimikeryhmän mukaan                               |
|                                         | Varianssi toimipaikan mukaan                                     |
|                                         | Tuotannon varianssi neljännesvuosittain                       |
|                                         | Tuotannon varianssi neljännesvuosittain ja varianssityypin mukaan     |
|                                         | 10 parasta resurssia epäsuotuisan tuotannon varianssin mukaan  |
|                                         | 10 parasta resurssia suotuisan tuotannon varianssin mukaan    |

## <a name="understanding-the-data-model-and-entities"></a>Tietomallin ja yksiköiden tiedot

**Kustannushintojen hallinnan** Power BI -sisällön raporttisivujen täyttämiseen käytetään sovelluksen tietoja. Nämä tiedot esitetään koottuina mittauksina, jotka vaiheistetaan yksikkösäilössä, joka on analytiikkaa varten optimoitu Microsoft SQL Server -tietokanta. Lisätietoja on kohdassa [Power BI:n ja yksikkösäilön integraatio](power-bi-integration-entity-store.md).

Seuraavien objektien tärkeitä koostemittoja käytetään Power BI -sisällön perustana.

| Objekti                          | Tärkeät koostemitat | Finance and Operationsin tietolähde | Kenttä               |
|---------------------------------|----------------------------|----------------------------------------|---------------------|
| CostObjectStatementCacheMonthly | Määrä                     | CostObjectStatementCache               | Määrä              |
| CostObjectStatementCacheMonthly | Määrä                   | CostObjectStatementCache               | Määrä                 |
| CostInventoryAccountingKPIGoal  | AnnualInventoryTurn        | CostInventoryAccountingKPIGoal         | AnnualInventoryTurn |
| CostInventoryAccountingKPIGoal  | InventoryAccuracy          | CostInventoryAccountingKPIGoal         | InventoryAccuracy   |

Seuraavassa taulukossa on Power BI -sisällön tärkeimmät lasketut mitat.

| Mitta                            | Laskelma |
|------------------------------------|-------------|
| Alkusaldo                  | Alkusaldo = \[Loppusaldo\]-\[Nettomuutos\] |
| Aloitussaldon määrä             | Aloitussaldon määrä = \[Loppusaldon määrä\]-\[Nettomuutoksen määrä\] |
| Loppusaldo                     | Loppusaldo = (CALCULATE(SUM(\[Amount\]), FILTER(ALL(FiscalCalendar) ,FiscalCalendar\[MONTHSTARTDATE\] \<= MAX(FiscalCalendar\[MONTHSTARTDATE\])))) |
| Loppusaldon määrä                | Loppusaldon määrä = CALCULATE(SUM(\[QTY\]), FILTER(ALL(FiscalCalendar),FiscalCalendar\[MONTHSTARTDATE\] \<= MAX(FiscalCalendar\[MONTHSTARTDATE\]))) |
| Nettomuutos                         | Nettomuutos = SUM(\[AMOUNT\]) |
| Nettomuutoksen määrä                    | Nettomuutoksen määrä = SUM(\[QTY\]) |
| Varaston kiertonopeus summan mukaan | Varaston kiertonopeus summan mukaan = if(OR(\[Varaston keskimäärinen saldo\] \<= 0, \[Inventory sold or consumed issues\] \>= 0), 0, ABS(\[Varaston myydyt tai kulutetut ongelmat\])/\[Varaston keskimääräinen saldo\]) |
| Varaston keskimääräinen saldo          | Varaston keskimäärinen saldo = ((\[Loppusaldo\] +  \[Alkusaldo\]) / 2) |
| Varastopäiviä käytettävissä             | Päivän käsillä oleva varasto = 365 / CostObjectStatementEntries\[Varaston kiertonopeus summan mukaan\] |
| Varaston tarkkuus                 | Varaston tarkkuus määrän mukaan = IF (\[Loppusaldo\] \<= 0, IF(OR(\[Inventory counted amount\] \<\> 0, \[loppusaldo\] \< 0), 0,1), MAX(0, (\[loppu saldo\] - ABS (\[Varaston laskettu summa\]))/\[Loppusaldo\])) |

Seuraavia avaindimensioita käytetään suodattimina koostemittojen osittamisessa. Tällä tavoin saavutetaan suurempi rakeisuus ja saadaan tarkempia analyysitietoja.


| Kokonaisuus                                                  | Esimerkkejä määritteistä                          |
|---------------------------------------------------------|-------------------------------------------------|
| Tuotteet                                                | Tuotenumero, tuotteen nimi, yksikkö, nimikeryhmät |
| Luokkahierarkiat (kustannushintojen hallinnan rooliin määritetty) | Luokkahierarkia, luokkataso              |
| Oikeushenkilöt                                          | Yritysten nimet                              |
| Kirjanpidon kalenterit                                        | Kirjanpidon vuosikalenteri, vuosi, vuosineljännes, kausi, kuukausi   |
| Sivusto                                                    | Tunnus, nimi, osoite, osavaltio, maa               |
