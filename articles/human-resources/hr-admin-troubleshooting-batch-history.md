---
title: Suorituskyvyn optimointi automaattisilla tyhjennystehtävillä
description: Tässä ohjeaiheessa käsitellään suorituskyvyn parantamista Microsoftin Dynamics 365 Human Resourcesissa erätyöhistorian tyhjentämisen avulla.
author: twheeloc
ms.date: 08/21/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Platform update 24
ms.openlocfilehash: 12876cf4cbbac893bcbb0178280245d5637bdf73
ms.sourcegitcommit: 7e32e5e39e762a4b1606161cb603a450d13b5251
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/23/2021
ms.locfileid: "7413484"
---
# <a name="optimize-performance-with-auto-cleanup-tasks"></a>Suorituskyvyn optimointi automaattisilla tyhjennystehtävillä

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

**Lähetä**

Microsoft Dynamics 365 Human Resourcesissa voi esiintyä suorituskykyongelmia, jos erätyöhistoria kasvaa liian suureksi.

**Syy**

Usein suoritettavat erätyöt voivat johtaa erätyöhistorian hallitsemattomaan kasvuun. Tämä voi aiheuttaa suorituskykyongelmia. 

**Ratkaisu**

Ajoita automaattinen tehtävä, joka tyhjentää erätyöhistoriasi. Suosittelemme määrittämään tehtävän suoritettavaksi viikoittain, mutta joudut ehkä suorittamaan tyhjennyksen useammin tai harvemmin ympäristösi mukaan. Seuraava toimenpide sisältää suosittelemamme asetukset, mutta voit muuttaa niitä tarpeidesi mukaan.

1. Valitse Human Resourcesissa **Järjestelmän hallinta**.

2. Kirjoita **Haku**-palkkiin **Erätöiden historian tyhjennys**.

   ![Hae erätyöhistorian tyhjennys.](media/talent-batch-history-cleanup-search-bar.png)

3. Syötä **Historiaraja (päivinä)** -kenttään **30**.

   ![Määritä historiarajaksi 30.](media/talent-batch-history-cleanup-history-limit.png)

4. Valitse **Suorita taustalla** ja sitten **Toistuminen**.

   ![Määritä toistuminen.](media/talent-batch-history-cleanup-recurrence.png)

5. Valitse **Määritä toistuvuus** -osiosta **Aloituspäivä** ja **Aloitusaika** tapahtumaan ruuhka-aikojen ulkopuolella tai viikonloppuna ja valitse sitten **PÄÄTTYMISPÄIVÄ PUUTTUU**. 

   ![Määritä toistuvuuden alkamispäivä ja -aika.](media/talent-batch-history-cleanup-define-recurrence.png)

6. Valitse **TOISTUMISEN KUVIO**, valitse **Päivät** ja määritä **TOISTA, KUN MÄÄRITETTY AIKA ON KULUNUT** -asetukseksi **7**.

   ![Määritä tyhjennys toistumaan viikoittain.](media/talent-batch-history-cleanup-recurrence-pattern.png)

7. Valitse **OK**.

8. Muuta muita parametrejä **Suorita taustalla**-osiosta tarvittaessa ja valitse sitten **OK**.



[!INCLUDE[footer-include](../includes/footer-banner.md)]
