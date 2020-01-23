---
title: Suorituskyvyn optimointi automaattisten tyhjennystehtävien avulla
description: Tässä ohjeaiheessa selitetään, miten voit ratkaista joitakin Microsoftin Dynamics 365 Talentin suorituskykyongelmia tyhjentämällä erätyöhistorian.
author: andreabichsel
manager: AnnBe
ms.date: 09/23/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2019-09-23
ms.dyn365.ops.version: Platform update 24
ms.openlocfilehash: fe536ace5c25765bd9c573f9303bd92f834765f7
ms.sourcegitcommit: 871707a3fd236da693a3d51f401eb0cb9d4bae39
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/06/2019
ms.locfileid: "2897969"
---
# <a name="optimize-performance-with-auto-cleanup-tasks"></a>Suorituskyvyn optimointi automaattisten tyhjennystehtävien avulla

**Lähetä**

Microsoft Dynamics 365 Talentissa voi esiintyä suorituskykyongelmia, jos erätyöhistoria kasvaa liian suureksi.

**Syy**

Usein suoritettavat erätyöt voivat johtaa erätyöhistorian hallitsemattomaan kasvuun. Tämä voi aiheuttaa suorituskykyongelmia. 

**Ratkaisu**

Ajoita automaattinen tehtävä, joka tyhjentää erätyöhistoriasi. Suosittelemme määrittämään tehtävän suoritettavaksi viikoittain, mutta joudut ehkä suorittamaan tyhjennyksen useammin tai harvemmin ympäristösi mukaan. Seuraava toimenpide sisältää suosittelemamme asetukset, mutta voit muuttaa niitä tarpeidesi mukaan.

1. Valitse Talentista **Järjestelmän hallinta**.

2. Kirjoita **Haku**-palkkiin **Erätöiden historian tyhjennys**.

   ![Hae erätyöhistorian tyhjennys](media/talent-batch-history-cleanup-search-bar.png)

3. Syötä **Historiaraja (päivinä)** -kenttään **30**.

   ![Määritä historiarajaksi 30](media/talent-batch-history-cleanup-history-limit.png)

4. Valitse **Suorita taustalla** ja sitten **Toistuminen**.

   ![Määritä toistuminen](media/talent-batch-history-cleanup-recurrence.png)

5. Valitse **Määritä toistuvuus** -osiosta **Aloituspäivä** ja **Aloitusaika** tapahtumaan ruuhka-aikojen ulkopuolella tai viikonloppuna ja valitse sitten **PÄÄTTYMISPÄIVÄ PUUTTUU**. 

   ![Määritä toistuvuuden alkamispäivä ja -aika](media/talent-batch-history-cleanup-define-recurrence.png)

6. Valitse **TOISTUMISEN KUVIO**, valitse **Päivät** ja määritä **TOISTA, KUN MÄÄRITETTY AIKA ON KULUNUT** -asetukseksi **7**.

   ![Määritä tyhjennys toistumaan viikoittain](media/talent-batch-history-cleanup-recurrence-pattern.png)

7. Valitse **OK**.

8. Muuta muita parametrejä **Suorita taustalla**-osiosta tarvittaessa ja valitse sitten **OK**.

