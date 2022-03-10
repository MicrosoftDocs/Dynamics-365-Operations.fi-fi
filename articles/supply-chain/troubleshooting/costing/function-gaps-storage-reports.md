---
title: Varastoarvon ja erääntymisraporttien sekä niiden tallennusversioiden väliset toiminnalliset aukot
description: Varastoarvon ja erääntymisraporttien sekä niiden tallennusversioiden väliset toiminnalliset aukot
author: AndersGirke
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: InventAgingStorage, InventAgingStorageChart, InventAgingStorageDetails
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: a72e2d32e755e137cebbc0bf7afb0bed08fb93f2
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476252"
---
# <a name="functional-gaps-between-inventory-valueaging-reports-and-their-storage-versions"></a>Varastoarvon ja erääntymisraporttien sekä niiden tallennusversioiden väliset toiminnalliset aukot

[Varaston erääntymisraportin tallennus](/dynamics365/supply-chain/cost-management/inventory-aging-report-storage.md)- ja [Varaston arvon tallennusraportti](/dynamics365/supply-chain/cost-management/inventory-value-report-storage.md) -toimintojen avulla Supply Chain Management voi näyttää suuria määriä varastotapahtumia. Kussakin tapauksessa raporttitulokset tallennetaan selausta ja vientiä varten toisin kuin näiden raporttien ei-tallennettavat versiot. Näiden raporttien ei-tallennusversioissa on kuitenkin toimintoja, joita ei ole tallennusversioissa. Seuraavissa aliosissa on erojen yhteenveto ja niiden kiertotavat.

## <a name="storage-reports-dont-include-subtotals-even-if-they-are-enabled-in-the-report-layout"></a>Tallennusraportit eivät sisällä välisummia, vaikka ne olisi otettu käyttöön raporttiasettelussa.

Välisummat voivat aiheuttaa ongelmia, kun tulos viedään, etenkin jo käyttäjät muuttavat tietuejärjestystä.

Välisummat voi tarkistaa viemällä tulokseen Microsoft Exceliin. Vaihtoehtoisesti välisummat voidaan tarkistaa Supply Chain Managementissa ottamalla *Uusi ruudukon ohjausobjekti*- ja *Ryhmittely ruudukoissa* -toiminnot käyttöön [ominaisuuksien hallinnassa](/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md). Tällä tavoin voidaan tarkastella joustavasti minkä tahansa ryhmän välisumman sarakekohtaisesti. Lisätietoja on aiheessa [Ruudukon ominaisuudet](/dynamics365/fin-ops-core/fin-ops/get-started/grid-capabilities.md).

## <a name="inventory-value-storage-report-doesnt-support-ledger-account-information"></a>Varastoarvon tallennusraportti ei tue kirjanpitotilin tietoja

Varastotilien saldo saadaan suorittamalla pääkirja, ja tätä saldoa voidaan verrata **Varastoarvon tallennus** -raporttiin.