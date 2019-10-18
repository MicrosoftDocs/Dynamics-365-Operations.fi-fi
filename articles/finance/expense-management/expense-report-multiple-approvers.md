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
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2d83a473e2e894856c12b36b4d005c6cb06b765a
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/27/2019
ms.locfileid: "2177534"
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