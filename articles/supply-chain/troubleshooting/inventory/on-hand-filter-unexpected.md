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
ms.openlocfilehash: 3857ce3720430c6f512d5abc4c9c4d390a0c3377
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/04/2022
ms.locfileid: "8686680"
---
# <a name="the-filter-pane-on-the-on-hand-list-page-doesnt-work-as-expected"></a>Varastoluettelo-sivun suodatinruutu ei toimi odotetusti

## <a name="symptoms"></a>Oireet

**Varastoluettelo**-sivunsuodatinruudun suodattimet eivät suodata tuloksia odotetusti.

## <a name="resolution"></a>Ratkaisu

**Käytettävissä olevien luettelo** -sivu kootaan yksityiskohtaisesta käytettävissä olevan varaston taulukosta, joka sisältää kaikki käytettävissä olevat dimensiot. Tämän sivun luettelo on kuitenkin yhteenveto. Näin ollen se saattaa yhdistää rivit lähdetaulukosta koostamalla arvot näytettävän dimension mukaan.

Suodatinruudussa määritettyjä suodattimia käytetään lähdetaulukossa, ei koostetussa luettelossa. Tämä toiminta voi joskus tuottaa odottamattomia tuloksia, kuten [näissä esimerkeissä](/dynamics365/supply-chain/inventory/inventory-on-hand-list#examples).

Kuitenkin [ruudukossa olevat suodattimet](/dynamics365/supply-chain/inventory/inventory-on-hand-list#grid-filters) *kohdistetaan* koottuun luetteloon. Nämä suodattimet sisältävät sekä pikasuodattimen ruudukon yläosassa että kunkin sarakeotsikon suodattimen.
