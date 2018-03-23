---
title: "Kuluraportit ja useita hyväksyjiä"
description: "Tässä ohjeaiheessa on tietoja kuluraportteja, joissa tarvitaan useita hyväksyjiä."
author: saraschi2
manager: AnnBe
ms.date: 02/23/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: TrvExpensesReportList
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 25fa39dc81fc721d7593a25a102ce47041ebc5f0
ms.openlocfilehash: 0f7592c580a21040c8b630885939ceaab3855c2c
ms.contentlocale: fi-fi
ms.lasthandoff: 03/13/2018

---

# <a name="expense-reports-and-multiple-approvers"></a>Kuluraportit ja useita hyväksyjiä

[!include[banner](../includes/banner.md)]

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

