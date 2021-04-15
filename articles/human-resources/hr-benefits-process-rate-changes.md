---
title: Maksumuutosten käsittely
description: Etujen maksumuutosten käsittely Microsoft Dynamics 365 Human Resourcesissa, kun uuden tai olemassa olevan etuussuunnitelman kelpoisuussääntöasetukset muuttuvat.
author: andreabichsel
ms.date: 04/06/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart, BenefitRate, BenefitEligibilityProcessResultViewer
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: c841f5d5d409c7e73cdc38988f8233747a11f837
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2021
ms.locfileid: "5803822"
---
# <a name="process-rate-changes"></a>Maksumuutosten käsittely

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

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


[!INCLUDE[footer-include](../includes/footer-banner.md)]