---
title: Kustannusten hallinnan vianmääritys
description: Tässä ohjeaiheessa käsitellään sellaisten ongelmien korjaamista, joita kustannusten hallinnan käytössä voi esiintyä.
author: riluan
manager: tfehr
ms.date: 10/13/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventAgingStorage, InventAgingStorageChart, InventAgingStorageDetails, InventValueProcess, InventValueReportSetup, InventClosing
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: riluan
ms.search.validFrom: 2020-10-13
ms.dyn365.ops.version: Release 10.0.15
ms.openlocfilehash: e84bb167395c06295b0e8ef8b9fd98aa4bc0cc14
ms.sourcegitcommit: aeee39c01d3f93a6dfcf2013965fa975a740596a
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/28/2020
ms.locfileid: "4427518"
---
# <a name="troubleshoot-cost-management"></a>Kustannusten hallinnan vianmääritys

Tässä ohjeaiheessa käsitellään sellaisten ongelmien korjaamista, joita kustannusten hallinnan käytössä voi esiintyä.

## <a name="functional-gaps-between-the-inventory-valueaging-reports-and-their-storage-versions"></a>Varastoarvon ja erääntymisraporttien sekä niiden tallennusversioiden väliset toiminnalliset aukot

[Varaston erääntymisraportin tallennus](inventory-aging-report-storage.md)- ja [Varaston arvon tallennusraportti](inventory-value-report-storage.md) -toimintojen avulla Supply Chain Management voi näyttää suuria määriä varastotapahtumia. Kussakin tapauksessa raporttitulokset tallennetaan selausta ja vientiä varten toisin kuin näiden raporttien ei-tallennettavat versiot. Näiden raporttien ei-tallennusversioissa on kuitenkin toimintoja, joita ei ole tallennusversioissa. Seuraavissa aliosissa on erojen yhteenveto ja niiden kiertotavat.

### <a name="storage-reports-dont-include-subtotals-even-if-they-are-enabled-in-the-report-layout"></a>Tallennusraportit eivät sisällä välisummia, vaikka ne olisi otettu käyttöön raporttiasettelussa.

Välisummat voivat aiheuttaa ongelmia, kun tulos viedään, etenkin jo käyttäjät muuttavat tietuejärjestystä.

Välisummat voi tarkistaa viemällä tulokseen Microsoft Exceliin. Vaihtoehtoisesti välisummat voidaan tarkistaa Supply Chain Managementissa ottamalla *Uusi ruudukon ohjausobjekti*- ja *(Esiversio) Ryhmittely ruudukoissa* -toiminnot käyttöön [ominaisuuksien hallinnassa](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md). Tällä tavoin voidaan tarkastella joustavasti minkä tahansa ryhmän välisumman sarakekohtaisesti. Lisätietoja on aiheessa [Ruudukon ominaisuudet](../../fin-ops-core/fin-ops/get-started/grid-capabilities.md).

### <a name="inventory-value-storage-report-doesnt-support-ledger-account-information"></a>Varastoarvon tallennusraportti ei tue kirjanpitotilin tietoja

Varastotilien saldo saadaan suorittamalla pääkirja, ja tätä saldoa voidaan verrata **Varastoarvon tallennus** -raporttiin.

## <a name="warnings-or-errors-are-shown-when-changing-a-ledger-period-status-without-closing-inventory"></a>Varoitusten tai virheiden näyttäminen muutettaessa kirjanpitokauden tilaa varastoa sulkematta

Microsoft otti seuraavat vahvistukset käyttöön estämään ongelmat, joita kustannuslaskennan virheellinen kauden lopetusprosessi aiheuttaa. Jos jokin seuraavista virhesanomista avautuu, lisätietoja näiden ongelmien ratkaisemisesta on tietoartikkelissa [KB 4561987](https://fix.lcs.dynamics.com/Issue/Details?kb=4561987&bugId=445351&dbType=3&qc=f514f2adcddcddceec43af58c26ae8a9020effdc7cdfe085d9d0deeb8cc7b6a3).

- Olet suorittamassa uudelleenlaskennan päivämäärällä %1 (10-02-2019). Viimeksi rekisteröity uudelleenlaskenta suorittiin edellisellä kaudella päivämäärällä %2 (20-01-2019). Varaston sulkemista ei suoriteta päivämäärällä %3 (31-01-2019), jolla kohdistuskauden loppu on rekisteröity. Muista suorittaa varaston sulkeminen alkaen päivämäärästä %3 (31-01-2019), jolloin kohdistuskausi päättyy. Varastojen arvostus, myytyjen tuotteiden kustannukset ja varianssit eivät ehkä ole oikein alareskontrassa tai kirjanpidossa, kunnes tämä on suoritettu.

- Olet muuttamassa kirjanpitokauden tila %1 tilaksi %2. Varaston sulkemista ei suoriteta päivämäärällä %3, jolla kohdistuskauden loppu on rekisteröity. Suorita varaston sulkeminen alkaen %3 kohdistuskauden lopusta ennen tilan muuttamista. Varastojen arvostus, myytyjen tuotteiden kustannukset ja varianssit eivät ehkä ole oikein alareskontrassa tai kirjanpidossa, kunnes tämä on suoritettu. Raportoidaan yrityksestä %4. Toistaiseksi tämä on vain tiedoksi, mutta vastaisuudessa sinun on suoritettava tällainen toiminto.

- Tilirakennetta %1on muutettu. Vähintään yhtä päätiliä %2 ei enää ole. %3 tarvitsee näitä päätilejä päivämäärällä %4. Lisää nämä päätilit tilirakenteeseen %1 ennen työn %3 jatkamista. Toistaiseksi tämä on vain tiedoksi, mutta vastaisuudessa sinun on suoritettava tällainen toiminto.

- Olet sulkemassa varaston päivämäärällä %1(31-01-2019). Jälkikustannuslaskentaa ei suoriteta päivämäärällä %2 (31-01-2019), jolla kohdistuskauden loppu on rekisteröity. Muista suorittaa jälkikustannuslaskentaa päivämäärällä %3 (31-01-2019), jolla kohdistuskausi päättyy. Varastojen arvostus, myytyjen tuotteiden kustannukset ja varianssit eivät ehkä ole oikein alareskontrassa tai kirjanpidossa, kunnes tämä on suoritettu.

- Olet suorittamassa jälkikustannuslaskennan päivämäärällä %1 (28-02-2019). Viimeksi rekisteröity jälkikustannuslaskenta suorittiin edellisellä kaudella päivämäärällä %2 (31-01-2019). Varaston sulkemista ei suoriteta päivämäärällä %3 (31-01-2019), jolla kohdistuskauden loppu on rekisteröity.
Muista suorittaa varaston sulkeminen alkaen %3 (31-01-2019), jolloin kohdistuskausi päättyy. Varastojen arvostus, myytyjen tuotteiden kustannukset ja varianssit eivät ehkä ole oikein alareskontrassa tai kirjanpidossa, kunnes varaston sulkeminen on suoritettu.

## <a name="inventory-aging-report-discrepancies"></a>Varaston erääntymisraportin ristiriidat

**Varaston erääntymisraportissa** on eri arvot, kun tarkasteltavana on eri varastodimensioita (kuten toimipaikka tai varasto): Lisätietoja raportointilogiikasta on kohdassa [Varaston erääntymisraporttien esimerkkejä ja logiikka](inventory-aging-report.md).