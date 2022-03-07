---
title: Varastoluettelo-sivun suodatinruutu ei toimi odotetusti
description: Varastoluettelo-sivunsuodatinruudun suodattimet eivät suodata tuloksia odotetusti.
author: sherry-zheng
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.16
ms.openlocfilehash: df11b1c1e7de36fa0458cd931d4be7f84a15d143
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476257"
---
# <a name="the-filter-pane-on-the-on-hand-list-page-doesnt-work-as-expected"></a>Varastoluettelo-sivun suodatinruutu ei toimi odotetusti

## <a name="symptoms"></a>Oireet

**Varastoluettelo**-sivun suodatinruudun suodattimet eivät suodata tuloksia odotetusti

## <a name="resolution"></a>Ratkaisu

 **Varastoluettelo**-sivu kootaan yksityiskohtaisesta käytettävissä olevan varaston taulukosta, joka sisältää kaikki käytettävissä olevat dimensiot. Tämän sivun luettelo on kuitenkin yhteenveto. Näin ollen se saattaa yhdistää rivit lähdetaulukosta koostamalla arvot näytettävän dimension mukaan.

Suodatinruudussa määritettyjä suodattimia käytetään lähdetaulukossa, ei koostetussa luettelossa. Tämä toiminta voi joskus tuottaa odottamattomia tuloksia, kuten [näissä esimerkeissä](/dynamics365/supply-chain/inventory/inventory-on-hand-list.md#examples).

 [Ruudukossa olevia suodattimia](/dynamics365/supply-chain/inventory/inventory-on-hand-list.md#grid-filters) kuitenkin *käytetään* koostettuun luetteloon. Nämä suodattimet sisältävät sekä pikasuodattimen ruudukon yläosassa että kunkin sarakeotsikon suodattimen.
