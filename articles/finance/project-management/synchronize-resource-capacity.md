---
title: Resurssin kapasiteetin synkronointi
description: Tässä aiheessa on tietoja resurssikapasiteetin synkronoinnista kalenterien ja projektien välillä.
author: Yowelle
manager: AnnBe
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 27b6fde91a72e37bb2712daba765032322cbd4e9
ms.sourcegitcommit: 241ada0945c72d769eaa70ae35aedbb6a3233fdf
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/02/2020
ms.locfileid: "3760532"
---
# <a name="synchronize-resource-capacity"></a>Resurssin kapasiteetin synkronointi

[!include [banner](../includes/banner.md)]

Resurssin synkronointiprosessi auttaa varmistamaan, että kalenterin ja peruskalenterin tiedot siirtyvät projektiresurssien ajoitukseen. Jos kalenteria muutetaan, prosessit tekevät projektiresurssien ajoitukseen tarvittavat päivitykset. Prosessit parantavat myös suorituskykyä, koska resurssin kalenteritiedot synkronoidaan etukäteen. Näin päivitykset resurssien ajoitustietoihin tapahtuvat entistä nopeammin. Prosessit kannattaa ajoittaa eräajona, ei yksitellen. Muussa tapauksessa riskinä on, että edelliseen synkronointiin sisällytettävät päivämäärät unohtuvat. Jos sisällytettäviä päivämääriä ei käytetä, päivämäärien synkronointiin voi jäädä aukkoja.

![Kalenterin synkronointi](./media/projectresourcing04-1024x471.jpg)

## <a name="synchronize-resource-capacity-roll-ups"></a>Synkronoi resurssin kapasiteetin koonnit

Synkronointiprosessin tarkoituksena on synkronoida kaikki resurssin kalenteritiedot. Näihin tietoihin sisältyvät peruskalenterin tiedot kaikista muutoksista, jotka tehdään projektin resurssikalenterin kapasiteettitaulukkoon. Jos projektiin lisätään uusia resursseja, synkronoinnin avulla voidaan varmistaa, että päivitetyt kalenteritiedot ovat käytettävissä. Synkronoinnin voi tehdä milloin tahansa.

Ne kannattaa tehdä eräajona. Vaihtoehdot ovat käytettävissä kapasiteettivarauksia synkronoitaessa.

1. Valitse **Projektinhallinta ja kirjanpito** &gt; **Kausittainen** &gt; **Kapasiteetin synkronointi** &gt; **Synkronoi resurssin kapasiteetin koonnit**.
2. Määritä asetukset seuraavassa taulukossa.

    | Vaihtoehto      | kuvaus |
    |-------------|-------------|
    | Kausikoodi | Voit myös valita pääkirjanpidon päivämäärävälin koodin, jolla asetetaan resurssin kapasiteetin koontien synkronointiprosessin aloitus- ja lopetuspäivämäärät. |
    | Aloituspäivämäärä  | Anna resurssin kapasiteetin koontien synkronointiprosessin aloituspäivä. |
    | Päättymispäivämäärä    | Anna resurssin kapasiteetin koontien synkronointiprosessin päättymispäivä. |

[![Synkronointiprosessi](./media/projectresourcing09.jpg)](./media/projectresourcing09.jpg)
