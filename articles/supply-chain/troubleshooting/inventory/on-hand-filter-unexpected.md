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
ms.openlocfilehash: 2b2b233e22378c8710a63dce83d168bfd89eba7f
ms.sourcegitcommit: 008779c530798f563fe216810d34b2d56f2c8d3c
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/14/2021
ms.locfileid: "7920495"
---
# <a name="the-filter-pane-on-the-on-hand-list-page-doesnt-work-as-expected"></a>Varastoluettelo-sivun suodatinruutu ei toimi odotetusti

## <a name="symptoms"></a>Oireet

**Varastoluettelo**-sivunsuodatinruudun suodattimet eivät suodata tuloksia odotetusti.

## <a name="resolution"></a>Ratkaisu

**Käytettävissä olevien luettelo** -sivu kootaan yksityiskohtaisesta käytettävissä olevan varaston taulukosta, joka sisältää kaikki käytettävissä olevat dimensiot. Tämän sivun luettelo on kuitenkin yhteenveto. Näin ollen se saattaa yhdistää rivit lähdetaulukosta koostamalla arvot näytettävän dimension mukaan.

Suodatinruudussa määritettyjä suodattimia käytetään lähdetaulukossa, ei koostetussa luettelossa. Tämä toiminta voi joskus tuottaa odottamattomia tuloksia, kuten [näissä esimerkeissä](/dynamics365/supply-chain/inventory/inventory-on-hand-list.md#examples).

Kuitenkin [ruudukossa olevat suodattimet](/dynamics365/supply-chain/inventory/inventory-on-hand-list.md#grid-filters) *kohdistetaan* koottuun luetteloon. Nämä suodattimet sisältävät sekä pikasuodattimen ruudukon yläosassa että kunkin sarakeotsikon suodattimen.
