---
title: "Kustannusten hallinnan Power BI -sisältö"
description: "Tässä aiheessa kuvataan, mitä kuuluu kustannushallinnan Power BI -sisältöön."
author: YuyuScheller
manager: AnnBe
ms.date: 02/02/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations
ms.custom: 270314
ms.assetid: 9680d977-43c8-47a7-966d-2280ba21402a
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7b5c4428c8610a7b2d4cf1a28287ba2bb1f9c2ea
ms.openlocfilehash: 6739d769c3f7876f67d80554743458b0abd5aae5
ms.contentlocale: fi-fi
ms.lasthandoff: 02/06/2018

---

# <a name="cost-management-power-bi-content"></a>Kustannusten hallinnan Power BI -sisältö

[!include[banner](../includes/banner.md)]

> [!Note]
> Tämä sisältöpaketti on vanhentunut, kuten on ilmoitettu [PowerBI.comissa julkaistuissa Power BI -sisältöpaketeissa](https://docs.microsoft.com/en-us/dynamics365/unified-operations/dev-itpro/migration-upgrade/deprecated-features#power-bi-content-packs-published-to-powerbicom).


Tässä aiheessa kuvataan, mitä kuuluu kustannushallinnan Power BI -sisältöön. 

**Kustannushallinnan** Microsoft Power BI -sisältö on tarkoitettu varaston kirjanpitäjille tai organisaation henkilöille, jotka ovat vastuussa varastosta. **Kustannustenhallinnan** Power BI -sisältö tarjoaa johdolle näkymän varastoon ja keskeneräisten töiden (KET) varastoon ja miten kustannukset kulkevat niiden läpi luokittain pitkällä aikavälillä. Näitä tietoja voidaan käyttää myös raportin yksityiskohtaisena täydennyksenä.

## <a name="key-measures"></a>Keskeiset mitat

+ Alkusaldo
+ Loppusaldo
+ Nettomuutos
+ Nettomuutos %
+ Erääntyminen

## <a name="key-performance-indicators"></a>Suorituskykyilmaisimet
+ Varaston liikevaihto
+ Varaston tarkkuus

CostStatementCache taulukko on ensisijainen tietolähde kohteelle CostAggregatedCostStatementEntryEntity. tietojoukon välimuistin kehys hallitsee tätä taulua. Oletusarvon mukaan taulukko päivitetään 24 tunnin välein, mutta voit ottaa käyttöön manuaaliset päivitykset tietojen välimuistin määrityksissä. Voit sitten tehdä manuaalisen päivityksen **Kustannushallinta**- tai **Kustannusanalyyis** -työtilassa. Kun CostStatementCache-päivitys on suoritettu, sinun on päivitettävä Power BI.com -sivustolla OData-yhteys nähdäksesi päivitetyt tiedot sivustolla. Varianssin (osto, tuotanto) mitat tässä Power BI -sisällössä pätevät vain nimikkeisiin, jotka arvioidaan varaston vakiokustannuksen menetelmällä. Tuotannon varianssi lasketaan aktiivisten kustannusten ja toteutuneiden kustannusten välisenä erona. Tuotannon varianssi lasketaan, kun tuotantotilauksen tilana on **Päättynyt**. Saat lisätietoja tuotannon varianssin tyypeistä ja siitä, miten kukin tyyppi lasketaan, ohjeaiheesta [Valmiin tuotantotilauksen varianssien analysointi](https://technet.microsoft.com/en-us/library/gg242850.aspx).


## <a name="metrics-that-are-included-in-the-power-bi-content"></a>Mittareita, jotka sisältyvät Power BI -sisältöön
Sisältö sisältää joukon raporttisivuja. Jokainen sivu koostuu joukosta mittareita, jotka ovat visualisoitu kaavioiden, ruutujen ja taulukoiden muodossa. Seuraavassa taulukossa on yleiskatsaus visualisoinneista **kustannushallinnan** Power BI -sisällössä.

| Raporttisivu | Kaaviot | Otsikot |
|---|---|---|
|Varasto, yleinen (oletus nykyisen kauden mukaan) |Tarkkuus |Varaston mitat:<br>Varaston loppusaldo<br>Varaston nettomuutos<br>Varaston nettomuutos %<br>|
| |Varaston liikevaihto | |
| |Varaston loppusaldo resurssiryhmän mukaan | |
| |Varaston nettomuutosta luokan nimitason 1 ja luokan nimitason 2 mukaan| |
| |Oston vaihtelut ja resurssiryhmän ja luokan nimitason 3 mukaan | |
|Varasto toimipaikan mukaan (oletus nykyisen kauden mukaan) |Varaston loppusaldo toimipaikan ja resurssiryhmän mukaan | |
| |Varaston liikevaihto toimipaikan ja resurssiryhmän mukaan | |
| |Varaston loppusaldo paikkakunnan ja resurssiryhmän mukaan | |
|Varasto resurssiryhmän mukaan (oletus nykyisen kauden mukaan) |Varaston mitat | |
| |Varaston tarkkuus määrän ja resurssiryhmän mukaan | |
| |Varaston liikevaihto määrän ja resurssiryhmän mukaan | |
|Varasto, vuosittainen (oletus kuluva vuosi vs edellinen vuosi) |Varaston mitat | |
| |Varaston suorituskykyilmaisimet:<br>Varaston liikevaihto<br>Varaston tarkkuus | |
| |Varaston loppusaldo vuoden ja resurssiryhmän mukaan | |
| |Oston vaihtelut ja vuoden ja luokan nimitason 3 mukaan | |
|Varaston erääntyminen (oletusarvon mukaan kuluva vuosi) |Varaston erääntyminen vuosineljänneksen ja resurssiryhmän mukaan | |
| |Varaston erääntyminen vuosineljänneksen ja toimipaikan nimen mukaan | |
|KET, yleinen (oletus nykyisen kauden mukaan) |KET-nettomuutos luokan nimitason 1 ja luokan nimitason 2 mukaan |Keskeneräisen työn KET-mitat:<br>KET-loppusaldo<br>KET-nettomuutos<br>KET-nettomuutos %<br> |
| |Tuotannon vaihtelut ja resurssiryhmän ja luokan nimitason 3 mukaan | |
| |KET-nettomuutos resurssiryhmän mukaan | |
|KET toimipaikan mukaan (oletus nykyisen kauden mukaan) |Keskeneräisen työn KET-mitat | |
| |KET-nettomuutos toimipaikan nimen ja luokan nimitason 2 mukaan | |
| |Tuotannon vaihtelut ja toimipaikan nimen ja luokan nimitason 3 mukaan | |

## <a name="understanding-the-data-model-and-entities"></a>Tietomallin ja yksiköiden tiedot
Finance and Operationsin tietoja käytetään täyttämään **Kustannusseuranta** – Power BI -sisällön raporttisivut. Nämä tiedot esitetään koottuina mittauksina, jotka vaiheistetaan yksikkösäilössä, joka on analytiikkaa varten optimoitu Microsoft SQL -tietokanta. Lisätietoja on ohjeaiheessa [yleiskatsaus Power BI:n integraatiosta yksikkökaupan kanssa](power-bi-integration-entity-store.md). Seuraavia tärkeitä koostettuja mittoja käytetään sisällön perustana.

| Kokonaisuus            | Tärkeät koostemitat | Finance and Operationsin tietolähde | Kenttä             | kuvaus                       |
|-------------------|---------------------------|---------------------------------------------|-------------------|-----------------------------------|
| Tiliotteen tapahtumat | Nettomuutos                | CostAggregatedCostStatementEntryEntity      | sum(\[Amount\])   | Summa kirjanpitovaluuttana |
| Tiliotteen tapahtumat | Nettomuutoksen määrä       | CostAggregatedCostStatementEntryEntity      | sum(\[Quantity\]) |                                   |

Seuraavassa taulukossa on esitetty, miten tärkeitä koostemittoja käytetään luomaan useita laskettuja mittoja sisällön tietojoukossa.

| Mitta                                 | Miten mitta on laskettu                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|-----------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Alkusaldo                       | \[Ending balance\]-\[Net change\]                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| Aloitussaldon määrä              | \[Ending balance quantity\]-\[Net change quantity\]                                                                                                                                                                                                                                                                                                                                                                                                                        |
| Loppusaldo                          | CALCULATE(SUM(\[Amount\]), FILTER(ALLEXCEPT('Fiscal calendars', 'Fiscal calendars'\[LedgerRecId\], 'entities'\[ID\], 'entities'\[Name\], 'Ledgers'\[Currency\], 'Ledgers'\[Description\], 'Ledgers'\[Name\]), 'Fiscal calendars'\[Date\] &lt;= MAX('Fiscal calendars'\[Date\])))                                                                                                                                                                                           |
| Loppusaldon määrä                 | CALCULATE(SUM(\[Quantity\]), FILTER(ALLEXCEPT('Fiscal calendars', 'Fiscal calendars'\[LedgerRecId\], 'entities'\[ID\], 'entities'\[Name\], 'Ledgers'\[Currency\], 'Ledgers'\[Description\], 'Ledgers'\[Name\]), 'Fiscal calendars'\[Date\] &lt;= MAX('Fiscal calendars'\[Date\])))                                                                                                                                                                                         |
| Varaston alkusaldo             | CALCULATE(\[Beginning balance\], 'Statement entries'\[Statement Type\] = "Inventory")                                                                                                                                                                                                                                                                                                                                                                                      |
| Varaston loppusaldo                | CALCULATE(\[Ending balance\], 'Statement entries'\[Statement Type\] = "Inventory")                                                                                                                                                                                                                                                                                                                                                                                         |
| Varaston nettomuutos                    | CALCULATE(\[Net change\], 'Statement entries'\[Statement type\] = "Inventory")                                                                                                                                                                                                                                                                                                                                                                                             |
| Varaston nettomuutoksen määrä           | CALCULATE(\[Net change quantity\], 'Statement entries'\[Statement type\] = "Inventory")                                                                                                                                                                                                                                                                                                                                                                                    |
| Varaston nettomuutos %                  | IF(\[Inventory ending balance\] = 0, 0, \[Inventory net change\] / \[Inventory ending balance\])                                                                                                                                                                                                                                                                                                                                                                           |
| Varaston kierto määrän mukaan                | if(OR(\[Inventory average balance\] &lt;= 0, \[Inventory sold or consumed issues\] &gt;= 0), 0, ABS(\[Inventory sold or consumed issues\])/\[Inventory average balance\])                                                                                                                                                                                                                                                                                                  |
| Varaston keskimääräinen saldo               | (\[Inventory ending balance\] + \[Inventory beginning balance\]) / 2                                                                                                                                                                                                                                                                                                                                                                                                       |
| Varaston myydyt tai kulutetut ongelmat       | \[Inventory sold\] + \[Inventory consumed material cost\]                                                                                                                                                                                                                                                                                                                                                                                                                  |
| Varaston kulutettujen materiaalien kustannukset        | CALCULATE(\[Inventory net change\], 'Statement entries'\[Category name - level 2\_\] = "ConsumedMaterialsCost")                                                                                                                                                                                                                                                                                                                                                            |
| Myyty varasto                          | CALCULATE(\[Inventory net change\], 'Statement entries'\[Category name - level 2\_\] = "Sold")                                                                                                                                                                                                                                                                                                                                                                             |
| Varaston tarkkuus määrän mukaan            | IF(\[Inventory ending balance\] &lt;= 0, IF(OR(\[Inventory counted amount\] &lt;&gt; 0, \[Inventory ending balance\] &lt; 0), 0, 1), MAX(0, (\[Inventory ending balance\] - ABS(\[Inventory counted amount\]))/\[Inventory ending balance\]))                                                                                                                                                                                                                              |
| Varaston laskettu määrä                | CALCULATE(\[Inventory net change\], 'Statement entries'\[Category name - level 3\_\] = "Counting")                                                                                                                                                                                                                                                                                                                                                                         |
| Varaston erääntyminen                         | if(ISBLANK(max('Fiscal calendars'\[Date\])), blank(), MAX(0, MIN(\[Inventory aging receipts quantity\], \[Inventory aging ending balance quantity\] - \[Inventory aging receipts quantity in the future\]))) \* \[Inventory avg unit cost\]                                                                                                                                                                                                                                |
| Varaston erääntyneiden vastaanottojen määrä       | IF(\[minDate\] = \[minDateAllSelected\], CALCULATE(\[Inventory net change quantity\], 'Statement entries'\[Quantity\] &gt; 0, FILTER(ALLEXCEPT('Fiscal calendars', 'Fiscal calendars'\[LedgerRecId\], 'entities'\[ID\], 'entities'\[Name\], 'Ledgers'\[Currency\], 'Ledgers'\[Description\], 'Ledgers'\[Name\]), 'Fiscal calendars'\[Date\] &lt;= MAX('Fiscal calendars'\[Date\]))), CALCULATE(\[Inventory net change quantity\], 'Statement entries'\[Quantity\] &gt; 0)) |
| Varaston erääntymisen loppusaldon määrä | \[Inventory ending balance quantity\] + CALCULATE(\[Inventory net change quantity\], FILTER(ALLEXCEPT('Fiscal calendars', 'Fiscal calendars'\[LedgerRecId\], 'entities'\[ID\], 'entities'\[Name\], 'Ledgers'\[Currency\], 'Ledgers'\[Description\], 'Ledgers'\[Name\]), 'Fiscal calendars'\[Date\] &gt; max('Fiscal calendars'\[Date\]) ))                                                                                                                                 |
| Varaston erääntyneet vastaanotot tulevaisuudessa  | CALCULATE(\[Inventory net change\], 'Statement entries'\[Amount\] &gt; 0, FILTER(ALLEXCEPT('Fiscal calendars', 'Fiscal calendars'\[LedgerRecId\], 'entities'\[ID\], 'entities'\[Name\], 'Ledgers'\[Currency\], 'Ledgers'\[Description\], 'Ledgers'\[Name\]), 'Fiscal calendars'\[Date\] &gt; MAX('Fiscal calendars'\[Date\])))                                                                                                                                             |
| Varaston keskimääräinen yksikkökustannus                 | CALCULATE(\[Inventory ending balance\] / \[Inventory ending balance quantity\],ALLEXCEPT('Fiscal calendars', 'Fiscal calendars'\[LedgerRecId\], 'entities'\[ID\], 'entities'\[Name\], 'Ledgers'\[Currency\], 'Ledgers'\[Description\], 'Ledgers'\[Name\]))                                                                                                                                                                                                                 |
| Ostojen varianssi                      | CALCULATE(SUM(\[Amount\]), 'Statement entries'\[Category name - level 2\_\] = "Procured", 'Statement entries'\[Statement type\] = "Variance")                                                                                                                                                                                                                                                                                                                              |
| KET-alkusaldo                   | CALCULATE(\[Beginning balance\], 'Statement entries'\[Statement Type\] = "WIP")                                                                                                                                                                                                                                                                                                                                                                                            |
| KET-loppusaldo                      | CALCULATE(\[Ending balance\], 'Statement entries'\[Statement Type\] = "WIP")                                                                                                                                                                                                                                                                                                                                                                                               |
| KET-nettomuutos                          | CALCULATE(\[Net change\], 'Statement entries'\[Statement type\] = "WIP")                                                                                                                                                                                                                                                                                                                                                                                                   |
| KET-nettomuutos %                        | IF(\[WIP ending balance\] = 0, 0, \[WIP net change\] / \[WIP ending balance\])                                                                                                                                                                                                                                                                                                                                                                                             |
| Tuotannon varianssit                    | CALCULATE(SUM(\[Amount\]), 'Statement entries'\[Category name - level 2\_\] = "ManufacturedCost", 'Statement entries'\[Statement type\] = "Variance")                                                                                                                                                                                                                                                                                                                      |
| Luokan nimi - taso 1                 | switch(\[Category name - level 1\_\], "None", "None", "NetSourcing", "Net sourcing", "NetUsage", "Net usage", "NetConversionCost", "Net conversion cost", "NetCostOfGoodsManufactured", "Net cost of goods manufactured", "BeginningBalance", "Beginning balance")                                                                                                                                                                                                         |
| Luokan nimi - taso 2                 | switch(\[Category name - level 2\_\], "None", "None", "Procured", "Procured", "Disposed", "Disposed", "Transferred", "Transferred", "Sold", "Sold", "ConsumedMaterialsCost", "Consumed material cost", "ConsumedManufacturingCost", "Consumed manufacturing cost", "ConsumedOutsourcingCost", "Consumed outsourcing cost", "ConsumedIndirectCost", "Consumed indirect cost", "ManufacturedCost", "Manufactured cost", "Variances", "Variances")                            |
| Luokan nimi - taso 3                 | switch(\[Category name - level 3\_\], "None", "None", "Counting", "None", "ProductionPriceVariance", "Production price", "QuantityVariance", "Quantity", "SubstitutionVariance", "Substitution", "ScrapVariance", "Scrap", "LotSizeVariance", "Lot size", "RevaluationVariance", "Revaluation", "PurchasePriceVariance", "Purchase price", "CostChangeVariance", "Cost change", "RoundingVariance", "Rounding variance")                                                   |

Suodattimina käytetään seuraavia tärkeimpiä dimensioita osittamaan koostemitat, jotta saavutetaan suurempi rakeisuus ja saadaan syvempiä analyyttisiä näkemyksiä.

| Kokonaisuus           | Esimerkkejä määritteistä                       |
|------------------|----------------------------------------------|
| Yksiköt         | Tunnus, nimi                                     |
| Kirjanpidon kalenterit | Kalenteri, kuukausi, kausi, vuosineljännes, vuosi       |
| KPI-tavoitteet        | Varaston tarkkuustavoite, varaston kierron tavoite |
| Kirjanpidot          | Valuutta, nimi, kuvaus                  |
| Toimipaikat            | Tunnus, nimi, maa, paikkakunta                      |






