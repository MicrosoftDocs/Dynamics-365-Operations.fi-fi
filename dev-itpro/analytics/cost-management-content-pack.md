---
title: "Kustannusten hallinnan sisältöä virtaa BI"
description: "Tässä ohjeaiheessa kuvataan kustannusten hallinnassa BI virran sisältöä. Artikkelissa kerrotaan, miten voit käyttää virtaa BI-raportteja ja tietoja tietomallin ja yksiköt, joita käytetään rakentaa sisältöä."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User, IT Pro
ms.search.scope: AX 7.0.0, Operations
ms.custom: 270314
ms.assetid: 9680d977-43c8-47a7-966d-2280ba21402a
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 388b6398488e6f316c1ec07a00182e81c1dc8d08
ms.openlocfilehash: e4de011e6eeac58643b828b65e24b874d981d5e7
ms.lasthandoff: 03/31/2017


---

# <a name="cost-management-power-bi-content"></a>Kustannusten hallinnan sisältöä virtaa BI

Tässä ohjeaiheessa kuvataan kustannusten hallinnassa BI virran sisältöä. Artikkelissa kerrotaan, miten voit käyttää virtaa BI-raportteja ja tietoja tietomallin ja yksiköt, joita käytetään rakentaa sisältöä.

# <a name="overview"></a>Yleiskuvaus

**Cost management** Microsoft Power BI sisältö on tarkoitettu varaston kirjanpitäjät tai organisaation henkilöille, jotka ovat vastuussa varaston. **Cost management** virtaa BI sisältö tarjoaa johto kehitysprojektien varaston ja töihin keskeneräisiin (KET-TYÖT) varaston ja miten kustannukset kulkee niitä luokittain pitkällä aikavälillä. Tiedot voidaan myös yksityiskohtaisen tilinpäätöksen täydennyksenä.

## <a name="key-measures"></a>Tärkeimmät toimenpiteet

+ Alkusaldo
+ Loppusaldo
+ Nettomuutos
+ Nettomuutos %
+ Erääntyminen

## <a name="key-performance-indicators"></a>Suorituskykyilmaisimet
+ Varaston liikevaihto
+ Varaston tarkkuus

CostStatementCache taulukko on ensisijainen tietolähde CostAggregatedCostStatementEntryEntity. Tässä taulukossa hallitaan tiedot välimuistiin puitteissa. Oletusarvon mukaan taulukko päivitetään 24 tunnin välein, mutta voit ottaa käyttöön tietojen välimuistin määritys manuaaliset päivitykset. Voit sitten tehdä manuaalisen päivityksen **Cost management** tai **Cost analysis** työtila. Kun CostStatementCache päivitys on suoritettu, sinun on päivitettävä virtaa BI.com-sivustolla näet päivitetyt tiedot OData-yhteys. Varianssi (osto, tuotanto) toimenpiteiden sisällön virtaa BI päteä vain kohteita, jotka ovat tavara varaston vakiokustannuksen menetelmällä. Tuotannon varianssi lasketaan aktiivisten kustannusten ja toteutuneiden kustannusten välisen eron. Tuotannon varianssi lasketaan, kun tuotantotilauksen tilana on **päättynyt**. Saat lisätietoja tuotannon varianssin tyyppejä ja miten lasketaan kullekin [valmiin tuotantotilauksen varianssien analysointi tietoja](https://technet.microsoft.com/en-us/library/gg242850.aspx).

## <a name="accessing-the-power-bi-content"></a>Power BI-sisällön käyttämistä
**Cost management** virtaa BI-sisältöä on saatavana PowerBI.com. Saat lisätietoja siitä, miten yhdistää ja lataa Microsoft Dynamics-365, toimintojen tietojen [PowerBI.com sisällön käyttö Power BI](power-bi-home-page.md).

## <a name="metrics-that-are-included-in-the-power-bi-content"></a>Mittareita, jotka sisältyvät Power BI-sisältö
Sisältö sisältää raportin sivuja. Jokainen sivu koostuu joukko mittareita, jotka ovat visualized laatat, kaavioiden ja taulukoiden muodossa. Seuraavassa taulukossa on yleiskatsaus visualisointi **Cost management** virtaa BI-sisältöä.

| Raportti-sivu | Kaaviot | Otsikot |
|---|---|---|
|Varaston Yleinen (oletus nykyisen kauden mukaan) |Tarkkuus |Varaston mitat:<br>Varasto, loppusaldo<br>Varaston nettomuutosta.<br>Varaston nettomuutosta %<br>|
| |Varaston liikevaihto | |
| |Varaston resurssiryhmä, loppusaldo | |
| |Varaston nettomuutosta luokan nimi taso 1 ja luokan nimi-taso 2| |
| |Oston vaihtelut ja resurssiryhmän nimi luokka-taso 3 | |
|Varasto-sivusto (oletusarvon mukaan nykyisen kauden) |Loppusaldo sivustonimi ja resurssiryhmän varastoa | |
| |Varaston ottaa sivustonimi ja resurssiryhmä | |
| |Varaston toimipaikka- ja ryhmän loppusaldo | |
|Varasto mukaan resurssiryhmä (oletusarvon mukaan nykyisen kauden) |Varaston toimenpiteet | |
| |Varaston tarkkuutta resurssiryhmän määrä | |
| |Varaston ottaa resurssiryhmän määrä | |
|Varaston vs (oletus kuluvan vuoden vs edellisenä vuonna) |Varaston toimenpiteet | |
| |Varaston KPI: tä:<br>Varaston liikevaihto<br>Varaston tarkkuus | |
| |Loppusaldo vuoden ja resurssin varasto | |
| |Oston vaihtelut mukaan vuoden ja luokan nimi-taso 3 | |
|Varaston tilanne (oletusarvon mukaan kuluvan vuoden) |Varaston tilanne ryhmittäin vuosineljännes- ja | |
| |Varaston tilanne neljännes ja sivuston nimi | |
|KET, yleinen (oletus nykyisen kauden mukaan) |Nettomääräinen KET muuta luokan nimi taso 1 ja luokan nimi-taso 2 |Keskeneräiset työt-KET-mitat:<br>KET-loppusaldo<br>KET Nettomuutos<br>KET Nettomuutos %<br> |
| |Tuotannon varianssit ja resurssiryhmän nimi luokka-taso 3 | |
| |KET, resurssiryhmän Nettomuutos | |
|KET-sivusto (oletusarvon mukaan nykyisen kauden) |Keskeneräiset työt-KET toimenpiteet | |
| |Nettomääräinen KET muuta sivustonimi ja luokan nimi-taso 2 | |
| |Tuotannon varianssit sivustonimi ja luokan nimi-taso 3 | |

## <a name="understanding-the-data-model-and-entities"></a>Tietomallin ja yksiköiden tiedot
Raportin sivujen täyttämiseen käytetään työvaiheiden tietoja Dynamics 365 **Cost management** virtaa BI-sisältöä. Nämä tiedot esitetään koostaa mitat, jotka lisätään yrityksen säilössä, joka on Microsoft SQL-tietokannan, joka on optimoitu analytics. Lisätietoja on ohjeaiheessa [yksikön Myymälän integrointi yleistä Power BI](power-bi-integration-entity-store.md). Avaimen koosta mittauksissa käytetään sisällön perusteella.

| Kokonaisuus            | Avaimen koosta mittaus | Tietolähteen Dynamics 365 operaatioille | Kenttä             | kuvaus                       |
|-------------------|---------------------------|---------------------------------------------|-------------------|-----------------------------------|
| Tiliotteen tapahtumien | Nettomuutos                | CostAggregatedCostStatementEntryEntity      | Summa (\[summan\])   | Summa-kirjanpitovaluutta |
| Tiliotteen tapahtumien | Nettomuutos-määrä       | CostAggregatedCostStatementEntryEntity      | Summa (\[määrä\]) |                                   |

Seuraavassa taulukossa on esitetty, miten avaimen koostaa mitat voidaan luoda useita laskettuja mittoja sisällön dataset-ryhmän.

| Mitta                                 | Miten on laskettu mitta                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|-----------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Alkusaldo                       | \[Loppusaldo\]-\[Nettomuutos\]                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| Saldo aloitusmäärän.              | \[Saldo lopetus\]-\[määrän Nettomuutos\]                                                                                                                                                                                                                                                                                                                                                                                                                        |
| Loppusaldo                          | Laske (summa (\[summan\]), suodatin (ALLEXCEPT ('Kirjanpitokalenterit', 'Kirjanpitokalenterit'\[LedgerRecId\], 'yksiköt'\[tunnus\], 'yksiköt'\[nimi\], 'Kirjaukset'\[valuutan\], 'Kirjaukset'\[kuvaus\], 'Kirjaukset'\[nimi\]), 'Kirjanpidon vuosikalenterit'\[päivämäärä\]&lt;= MAX ('Kirjanpidon vuosikalenterit'\[päivämäärä\])))                                                                                                                                                                                           |
| Loppu Saldomäärä                 | Laske (summa (\[määrä\]), suodatin (ALLEXCEPT ('Kirjanpitokalenterit', 'Kirjanpitokalenterit'\[LedgerRecId\], 'yksiköt'\[ID\], 'yksiköt'\[nimi\], 'Kirjaukset'\[valuutan\], 'Kirjaukset'\[kuvaus\], 'Kirjaukset'\[nimi\]), 'Kirjanpidon vuosikalenterit'\[päivämäärä\]&lt;= MAX ('Kirjanpidon vuosikalenterit'\[päivämäärä\])))                                                                                                                                                                                         |
| Varasto, alkusaldo             | Laske (\[alkusaldo\], 'Tiliotteen tapahtumien'\[tyyppiä\] = "Varaston")                                                                                                                                                                                                                                                                                                                                                                                      |
| Varasto, loppusaldo                | Laske (\[loppusaldo\], 'Tiliotteen tapahtumien'\[tyyppiä\] = "Varaston")                                                                                                                                                                                                                                                                                                                                                                                         |
| Varaston nettomuutosta.                    | Laske (\[nettomuutos\], 'Tiliotteen tapahtumien'\[tyyppiä\] = "Varaston")                                                                                                                                                                                                                                                                                                                                                                                             |
| Varaston määrän Nettomuutos           | Laske (\[määrää muuttaa Net\], 'Tiliotteen tapahtumien'\[tyyppiä\] = "Varaston")                                                                                                                                                                                                                                                                                                                                                                                    |
| Varaston nettomuutosta %                  | IF (\[varaston loppusaldo\] = 0, 0, \[varaston nettomuutosta\] / \[varaston loppusaldo\])                                                                                                                                                                                                                                                                                                                                                                           |
| Varaston määrä ottaa                | Jos (tai (\[varaston keskimääräisen saldon\]&lt;= 0, \[varaston myytyjä tai kulutettuja ongelmat\]&gt;= 0), 0, ABS (\[varaston myytyjä tai kulutettuja ongelmien\]) ja\[varaston keskimääräisen saldon\])                                                                                                                                                                                                                                                                                                  |
| Varaston keskimääräisen saldon               | (\[Varaston loppusaldo\] + \[varaston alkusaldo\]) / 2                                                                                                                                                                                                                                                                                                                                                                                                       |
| Varaston myytyjä tai kulutettuja ongelmat       | \[Myydyn\] + \[varastoa kulutetaan materiaalikustannukset\]                                                                                                                                                                                                                                                                                                                                                                                                                  |
| Varaston kulutettu kustannus        | Laske (\[varaston nettomuutosta\], 'Tiliotteen tapahtumien'\[luokkanimi - tason 2\_\] = "ConsumedMaterialsCost")                                                                                                                                                                                                                                                                                                                                                            |
| Myydyn                          | Laske (\[varaston nettomuutosta\], 'Tiliotteen tapahtumien'\[luokkanimi - tason 2\_\] = "Myyty")                                                                                                                                                                                                                                                                                                                                                                             |
| Varaston määrä tarkkuus            | IF (\[varaston loppusaldo\]&lt;= 0, jos (tai (\[varasto laskettu summa\]&lt;&gt; 0, \[varaston loppusaldo\]&lt; 0), 0, 1), MAX (0, (\[varaston loppusaldo\] -ABS (\[varasto laskettu summa\])) /\[varaston loppusaldo\]))                                                                                                                                                                                                                              |
| Laskettu summa varasto                | Laske (\[varaston nettomuutosta\], 'Tiliotteen tapahtumien'\[luokkanimi - tason 3\_\] = "Laskenta")                                                                                                                                                                                                                                                                                                                                                                         |
| Varaston erääntyminen                         | Jos (ONTYHJÄ (max ('Kirjanpidon vuosikalenterit'\[päivämäärä\])), blank(), MAX (0, MIN (\[kuitit varaston erääntymisen määrän\], \[varasto tilanne saldo Lopetusmäärän\] - \[erääntymisen varaston vastaanottoja määrä tulevaisuudessa\]))) \*\[varaston keskimääräinen yksikkökustannus\]                                                                                                                                                                                                                                |
| Varaston vastaanottojen määrä tilanne       | Jos (\[minDate\] = \[minDateAllSelected\], Laske (\[varaston nettomuutosta määrä\], 'Tiliotteen tapahtumien'\[määrä\]&gt; 0, suodatin (ALLEXCEPT ('Kirjanpitokalenterit', 'Kirjanpitokalenterit'\[LedgerRecId\], 'yksiköt'\[tunnus\], 'yksiköt'\[nimi\], 'Kirjaukset'\[valuutan\], 'Kirjaukset'\[kuvaus\], 'Kirjaukset'\[nimi\]), 'Kirjanpidon vuosikalenterit'\[päivämäärä\]&lt;= MAX ('Kirjanpidon vuosikalenterit'\[päivämäärä\]))), Laske (\[varaston nettomuutosta määrä\], 'Tiliotteen tapahtumien'\[määrä\]&gt; 0)) |
| Varaston tilanne saldo lopetus | \[Varaston loppuarvo saldo\] + Laske (\[varaston määrän nettomuutos\], suodatin (ALLEXCEPT ('Kirjanpitokalenterit', 'Kirjanpitokalenterit'\[LedgerRecId\], 'yksiköt'\[ID\], 'yksiköt'\[nimi\], 'Kirjaukset'\[valuutan\], 'Kirjaukset'\[kuvaus\], 'Kirjaukset'\[nimi\]), 'Kirjanpidon vuosikalenterit'\[päivämäärä\]&gt; max ('Kirjanpidon vuosikalenterit'\[päivämäärä\])))                                                                                                                                 |
| Erääntymisen varastovastaanottoja tulevaisuudessa  | Laske (\[varaston nettomuutosta\], 'Tiliotteen tapahtumien'\[summa\]&gt; 0, suodatin (ALLEXCEPT ('Kirjanpitokalenterit', 'Kirjanpitokalenterit'\[LedgerRecId\], 'yksiköt'\[tunnus\], 'yksiköt'\[nimi\], 'Kirjaukset'\[valuutan\], 'Kirjaukset'\[kuvaus\], 'Kirjaukset'\[nimi\]), 'Kirjanpidon vuosikalenterit'\[päivämäärä\]&gt; MAX ('Kirjanpidon vuosikalenterit'\[päivämäärä\])))                                                                                                                                             |
| Varaston keskimääräinen yksikkökustannus                 | Laske (\[varaston loppusaldo\] / \[varaston saldo Lopetusmäärän\], ALLEXCEPT ('Kirjanpitokalenterit', 'Kirjanpitokalenterit'\[LedgerRecId\], 'yksiköt'\[ID\], 'yksiköt'\[nimi\], 'Kirjaukset'\[valuutan\], 'Kirjaukset'\[kuvaus\], 'Kirjaukset'\[nimi\]))                                                                                                                                                                                                                 |
| Oston vaihtelut.                      | Laske (summa (\[summan\]), 'Tiliotteen tapahtumien'\[luokkanimi - tason 2\_\] = "Procured", 'Tiliotteen tapahtumien'\[tyyppiä\] = "Vaihtelu")                                                                                                                                                                                                                                                                                                                              |
| KET-alkusaldo                   | Laske (\[alkusaldo\], 'Tiliotteen tapahtumien'\[tyyppiä\] = "KET)                                                                                                                                                                                                                                                                                                                                                                                            |
| KET-loppusaldo                      | Laske (\[loppusaldo\], 'Tiliotteen tapahtumien'\[tyyppiä\] = "KET)                                                                                                                                                                                                                                                                                                                                                                                               |
| KET Nettomuutos                          | Laske (\[nettomuutos\], 'Tiliotteen tapahtumien'\[tyyppiä\] = "KET)                                                                                                                                                                                                                                                                                                                                                                                                   |
| KET Nettomuutos %                        | IF (\[loppusaldo KET\] = 0, 0, \[KET nettomuutos\] / \[loppusaldo KET\])                                                                                                                                                                                                                                                                                                                                                                                             |
| Tuotannon varianssit                    | Laske (summa (\[summan\]), 'Tiliotteen tapahtumien'\[luokkanimi - tason 2\_\] = "ManufacturedCost", 'Tiliotteen tapahtumien'\[tyyppiä\] = "Vaihtelu")                                                                                                                                                                                                                                                                                                                      |
| Luokkanimi - taso 1                 | Vaihda (\[luokkanimi - tason 1\_\], "Ei mitään", "Ei mitään", "NetSourcing", "Net hankinta", "NetUsage", "Net käyttö", "NetConversionCost", "Net kustannusten muuntaminen", "NetCostOfGoodsManufactured", "Net valmistettujen tuotteiden kustannukset", "BeginningBalance", "Alkusaldo")                                                                                                                                                                                                         |
| Luokkanimi - taso 2                 | Vaihda (\[luokkanimi - tason 2\_\], "Ei mitään", "Ei mitään", "Procured", "Procured", "Disposed", "Disposed", "Siirretty", "Siirretty", "Myyty", "Myyty", "ConsumedMaterialsCost", "Kulutettu kustannukset", "ConsumedManufacturingCost", "Tuotannon kulutus", "ConsumedOutsourcingCost", "Kulutettu teettämisen kustannukset", "ConsumedIndirectCost", "Kulutettu välilliset kustannukset", "ManufacturedCost", "Valmistettu kustannukset", "Varianssit", "Varianssit")                            |
| Luokkanimi - taso 3                 | Vaihtaa (\[luokkanimi - tason 3\_\], "Ei mitään", "Ei mitään", "Lasketaan" "Ei mitään", "ProductionPriceVariance", "Tuotannon hinta", "QuantityVariance", "Määrä", "SubstitutionVariance", "Korvaus", "ScrapVariance", "Romu", "LotSizeVariance", "Erän koko", "RevaluationVariance", "Uudelleenarvostuksen", "PurchasePriceVariance", "Ostohinnalla", "CostChangeVariance", "Muuttaa", "RoundingVariance", "Pyöristysvarianssi")                                                   |

Suodattimina käytetään seuraavat tärkeimmät mitat osittaa yhteenlaskettu mittausten saavuttaa suurempi rakeisuus ja syvemmälle analyyttinen asuun.

| Kokonaisuus           | Esimerkkejä määritteet                       |
|------------------|----------------------------------------------|
| Yksiköt         | Tunnuksen nimi                                     |
| Kirjanpidon kalenterit | Kalenterin kuukausi, kausi, vuosineljännes, vuosi       |
| KPI-tavoitteet        | Varaston tarkkuus tavoitteen varaston ottaa tavoite |
| Kirjanpidot          | Valuutan nimi, kuvaus                  |
| Toimipaikat            | Tunnus, nimi, maa ja Kaupunki                      |

## <a name="additional-resources"></a>Lisäresurssit
Seuraavista linkeistä löydät hyödyllistä, entiteetteihin ja Power BI -sisällön rakentamiseen liittyvää tietoa:

-   [Tietoyksiköt](..\data-entities\data-entities.md)
-   [Organisaation sisältöpakettien luominen](https://powerbi.microsoft.com/en-us/documentation/powerbi-service-organizational-content-packs-introduction/)
-   [Tietojen mallinnus Power BI:n avulla](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-2-1-intro-modeling-data)
-   [Power BI -ruutujen lisääminen työtiloihin](configure-power-bi-integration.md)



