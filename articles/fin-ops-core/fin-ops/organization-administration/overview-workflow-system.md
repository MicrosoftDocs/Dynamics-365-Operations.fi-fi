---
title: Työnkulkujärjestelmän yleiskatsaus
description: Tässä ohjeaiheessa käsitellään työnkulkujärjestelmää.
author: sericks007
manager: AnnBe
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 56381
ms.assetid: 20b78595-e1d9-439a-ae1c-a776a3438919
ms.search.region: Global
ms.author: tjvass
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: eef77a5d81d12ec92eea86b1dd9902d9e3d80b33
ms.sourcegitcommit: 57bc7e17682e2edb5e1766496b7a22f4621819dd
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/18/2019
ms.locfileid: "2812360"
---
# <a name="workflow-system-overview"></a>Työnkulkujärjestelmän yleiskatsaus

[!include [banner](../includes/banner.md)]

Tässä ohjeaiheessa käsitellään työnkulkujärjestelmää.

## <a name="what-is-workflow"></a>Mikä on työnkulku?

Termi *työnkulku* voidaan määrittää kahdella tavalla: järjestelmänä tai liiketoimintaprosessina.

### <a name="workflow-is-a-system"></a>Työnkulku järjestelmänä

Työnkulku on järjestelmä, joka suoritetaan Application Object Server (AOS) -palvelimessa. Työnkulkujärjestelmän toimintojen avulla voit luoda yksittäisiä työnkulkuja eli liiketoimintaprosesseja.

### <a name="workflow-is-a-business-process"></a>Työnkulku liiketoimintaprosessina

Työnkulku vastaa liiketoimintaprosessia. Se määrittää, kuinka asiakirja kulkee tai siirtyy järjestelmässä kuvaamalla kenen on suoritettava tehtävä loppuun, tehtävä päätös tai hyväksyttävä asiakirja. Seuraavassa kuvassa on esimerkkityönkulku kuluraporteille.

![Työnkulku, jonka elementtejä on delegoitu käyttäjille](./media/workflow_user.gif)

Tässä työnkulkuesimerkissä Sam lähettää kuluraportin, jonka summa on 7 000 USD. Ivanin on tarkistettava Samin hänelle lähettämät kuitit. Sen jälkeen Frankin ja Suen on hyväksyttävä kuluraportti. Oletetaan, että Sam lähettää kuluraportin, jonka summa on 11 000 Yhdysvaltain dollaria (USD). Tässä tapauksessa Ivanin on tarkistettava kuitit ja Frankin, Suen ja Annin hyväksyttävä kuluraportti.

## <a name="benefits-of-using-the-workflow-system"></a> Työnkulkujärjestelmän edut

Työnkulkujärjestelmän käyttö hyödyttää organisaatiotasi monin eri tavoin:

- **Yhdenmukaiset prosessit** — Voit määrittää, miten tietyt asiakirjat, kuten ostoehdotukset ja kuluraportit käsitellään. Työnkulkujärjestelmän käyttö auttaa varmistamaan, että asiakirjat käsitellään ja hyväksytään johdonmukaisesti ja tehokkaasti.
- **Prosessin näkyvyys** – Voit seurata työnkulun esiintymien tilaa, historiaa ja suorituskykyarvoja. Tämä auttaa määrittämään, tarvitaanko työnkulkuun muutoksia tehokkuuden parantamiseksi.
- **Keskitetty työluettelo** – Käyttäjät voivat tarkastella keskitettyä työluetteloa, joka sisältää työnkulun tehtävät ja niille annetut hyväksynnät.


## <a name="workflow-content"></a>Työnkulun sisältö

+ [Työnkulkujärjestelmän arkkitehtuuri](workflow-system-architecture.md)
+ [Työnkulun elementit](workflow-elements.md)
+ [Toiminnot hyväksyntäprosessien työnkulussa](workflow-actions.md)
+ [Työnkulkujen luonnin yleiskatsaus](create-workflow.md)
+ [Työnkulkuominaisuuksien määrittäminen](configure-workflow-properties.md)
+ [Manuaalisten tehtävien konfiguroiminen työnkulkuun](configure-manual-task-workflow.md)
+ [Automaattisten tehtävien määrittäminen työnkulkuun](configure-automated-task-workflow.md)
+ [Hyväksyntäprosessien lisääminen työnkulkuun](configure-approval-process-workflow.md)
+ [Hyväksyntävaiheiden lisääminen työnkulkuun](configure-approval-step-workflow.md)
+ [Manuaalisten päätösten konfiguroiminen työnkulkuun](configure-manual-decision-workflow.md)
+ [Ehdollisten päätösten konfiguroiminen työnkulkuun](configure-conditional-decision-workflow.md)
+ [Rinnakkaisten tehtävien määrittäminen työnkulussa](configure-parallel-activity-workflow.md)
+ [Määritä rinnakkaiset haarat työnkulussa](configure-parallel-branch-workflow.md)
+ [Rivinimikkeen työnkulkujen määrittäminen](configure-line-item-workflow.md)
+ [Työnkulun usein kysytyt kysymykset](workflow-FAQ.md)
