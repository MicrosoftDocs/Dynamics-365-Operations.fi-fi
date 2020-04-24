---
title: Maksumuutosten käsittely
description: Etujen maksumuutosten käsittely Microsoft Dynamics 365 Human Resourcesissa, kun uuden tai olemassa olevan etuussuunnitelman kelpoisuussääntöasetukset muuttuvat.
author: andreabichsel
manager: AnnBe
ms.date: 04/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: BenefitWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 850709480326f6a0871f19ea1bb287631cd58b42
ms.sourcegitcommit: a9461650d11d6845e1942865ebf7e35f75f61ad3
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/06/2020
ms.locfileid: "3229934"
---
# <a name="process-rate-changes"></a>Maksumuutosten käsittely

Etujen maksumuutosten käsittely Microsoft Dynamics 365 Human Resourcesissa, kun uuden tai olemassa olevan etuussuunnitelman kelpoisuussääntöasetukset muuttuvat. Jos uusi kelpoisuussääntö luodaan ja liitetään suunnitelmaan, järjestelmää kehotetaan tarkistamaan työntekijän kelpoisuus uudelleen sen tarkistamiseksi, täyttävätkö työntekijät suunnitelman uusien kelpousuusasetusten vaatimukset. 

1. Valitse **Etujen hallinta** -työtilassa **Käsittely**-kohdasta **Maksumuutoksen päivityskäsittely**.

2. Määritä **Suorita edun maksupäivitysprosessi** -valintaruudussa arvot seuraaville kentille:

   | Kenttä | Kuvaus |
   | --- | --- |
   | **Rekisteröitymiskausi** | Rekisteröintijakso, jonka maksumuutokset käsitellään. |

3. Jos haluat suorittaa prosessin taustalla, valitse **Suorita taustalla** ja tee seuraavat tehtävät:

   1. Määritä prosessin tiedot.

   2. Jos haluat määrittää toistuvan työn, valitse **Toistuminen**, kirjoita toistuvuustiedot ja valitse **OK**.

   3. Jos haluat määrittää työpaikkahälytyksen, valitse **Hälytykset**, valitse vastaanotettavat hälytykset ja valitse sitten **OK**.

   4. Valitse **OK**. Prosessi suoritetaan määrittämilläsi parametreilla.

4. Valitse **OK**.
