---
title: Elämäntapahtumien muutosten käsittely
description: Tässä aiheessa käsitellään elämäntapahtumien muutosten käsittelemistä Microsoft Dynamics 365 Human Resourcesissa.
author: twheeloc
ms.date: 08/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart, BenefitLifeEventTypes, BenefitEligibilityProcessResultViewer
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: f43ee914bb57b14969b6d729218accbd1009d67a
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/04/2022
ms.locfileid: "8691775"
---
# <a name="process-life-event-changes"></a>Elämäntapahtumien muutosten käsittely


[!INCLUDE [PEAP](../includes/peap-2.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Käsittele elämäntapahtumien muutokset Microsoft Dynamics 365 Human Resourcesissa kahden elämäntapahtumamuutoksen osalta:

- Syntymäpäivämuutokset
- Etukelpoisuuden ohituksen päättymismuutokset 

1. Valitse **Etujen hallinta** -työtilassa **Käsittely**-kohdasta **Elämäntapahtumien muutosten käsittely**.

2. Määritä **Suorita elämäntapahtuman muutosprosessi** -valintaruudussa arvot seuraaville kentille:

   | Kenttä | Kuvaus |
   | --- | --- |
   | Rekisteröitymiskausi | Rekisteröintijakso, jonka elämäntapahtumien muutokset käsitellään. |
   | Oikeushenkilö | Yritys, jonka elämäntapahtumien muutokset käsitellään. |

3. Jos haluat suorittaa prosessin taustalla, valitse **Suorita taustalla** ja tee seuraavat tehtävät:

   1. Määritä prosessin tiedot.

   2. Jos haluat määrittää toistuvan työn, valitse **Toistuminen**, kirjoita toistuvuustiedot ja valitse **OK**.

   3. Jos haluat määrittää työpaikkahälytyksen, valitse **Hälytykset**, valitse vastaanotettavat hälytykset ja valitse sitten **OK**.

   4. Valitse **OK**. Prosessi suoritetaan määrittämilläsi parametreilla.

4. Valitse **OK**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
