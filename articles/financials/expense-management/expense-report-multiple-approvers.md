---
title: Kuluraportit ja useita hyväksyjiä
description: Tässä ohjeaiheessa on tietoja kuluraportteja, joissa tarvitaan useita hyväksyjiä.
author: saraschi2
manager: AnnBe
ms.date: 02/23/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TrvExpensesReportList
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1483de5405895d60f0cb302ab622758b2b05d2ca
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/15/2019
ms.locfileid: "1566981"
---
# <a name="expense-reports-and-multiple-approvers"></a>Kuluraportit ja useita hyväksyjiä

[!include [banner](../includes/banner.md)]

Organisaation kulujen hyväksyntäkäytäntöjen mukaan useat henkilöt voivat hyväksyä työntekijän lähettämän kuluraportin. Kun määritä kuluraportin hyväksyntätyönkulun, voit lisätä työnkulkuelementtejä, jotka sisältävät vaiheita vähintään yhdelle kuluraportin hyväksyjälle. Voit esimerkiksi edellyttää, että kaikki kuluraportit on ensin hyväksytettävä raportin lähettäneen työntekijän esimiehellä ja sitten ostoreskontran koordinaattorilla.

Jos päätät edellyttää useita kuluraportin hyväksyjiä, voit lisätä työnkulun elementtejä seuraavilla tavoilla:

- Lisää hyväksyntäelementti, jossa on yksi vaihe. Vaihe voi esimerkiksi edellyttää, että kuluraportti määritetään käyttäjäryhmälle ja että 50 % ryhmän jäsenistä on hyväksyttävä se.
- Lisää hyväksyntäelementti, jossa on useita vaiheita. Hyväksyntäelementissä voi olla esimerkiksi seuraavat vaiheet:

    1. Kuluraportin lähettäneen työntekijän esimies hyväksyy raportin.
    2. Ostoreskontra-assistentti varmistaa kuitit ja kuluraportin nimikkeet.
    3. Budjetin omistaja hyväksyy kuluraportin.

- Lisää useita hyväksyntäelementtejä, joista jokaisella on yksi vaihe. Voit esimerkiksi lisätä erillisen hyväksyntäelementin kullekin seuraavista vaiheista:

    1. Työntekijän esimies hyväksyy kuluraportin.
    2. Budjetin omistaja hyväksyy kuluraportin.
