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
ms.openlocfilehash: 6e5e795ca6f7831ecd3fa28be9782f0b287eea6e
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/27/2019
ms.locfileid: "2190002"
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

+ [Työnkulun arkkitehtuuri](workflow-system-architecture.md)
+ [Työnkulun elementit](workflow-elements.md)
+ [Työnkulkutehtävät](workflow-actions.md)
+ [Työnkulun luominen](create-workflow.md)
+ [Työnkulkuominaisuuksien asetusten määrittäminen](configure-workflow-properties.md)
+ [Manuaalisen tehtävän konfiguroiminen työnkulkuun](configure-manual-task-workflow.md)
+ [Automaattisen tehtävän määrittäminen työnkulkuun](configure-automated-task-workflow.md)
+ [Hyväksyntäprosessin lisääminen työnkulkuun](configure-approval-process-workflow.md)
+ [Hyväksyntävaiheen lisääminen työnkulkuun](configure-approval-step-workflow.md)
+ [Manuaalisen päätöksen konfiguroiminen työnkulkuun](configure-manual-decision-workflow.md)
+ [Ehdollisen päätöksen konfiguroiminen työnkulkuun](configure-conditional-decision-workflow.md)
+ [Rinnakkaisen tehtävän määrittäminen työnkulussa](configure-parallel-activity-workflow.md)
+ [Määritä rinnakkainen haara työnkulussa](configure-parallel-branch-workflow.md)
+ [Rivinimikkeen työnkulun asetusten määrittäminen](configure-line-item-workflow.md)
+ [Työnkulun usein kysytyt kysymykset](workflow-FAQ.md)