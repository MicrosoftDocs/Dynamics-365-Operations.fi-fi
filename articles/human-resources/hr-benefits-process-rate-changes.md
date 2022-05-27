---
title: Hintamuutosten käsittely
description: Tässä aiheessa käsitellään edun hintamuutosten käsittelyä Microsoft Dynamics 365 Human Resourcesissa.
author: twheeloc
ms.date: 08/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart, BenefitRate, BenefitEligibilityProcessResultViewer
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: c1eea61df6dd5fbe0b52a21944deba69928b5125
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/04/2022
ms.locfileid: "8696123"
---
# <a name="process-rate-changes"></a>Hintamuutosten käsittely


[!INCLUDE [PEAP](../includes/peap-2.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Tässä aiheessa käsitellään etujen hintamuutosten käsittelyä Microsoft Dynamics 365 Human Resourcesissa, kun uuden tai olemassa olevan etuussuunnitelman kelpoisuussääntöasetukset muuttuvat. Jos uusi kelpoisuussääntö luodaan ja liitetään suunnitelmaan, järjestelmää kehotetaan tarkistamaan työntekijän kelpoisuus uudelleen sen tarkistamiseksi, täyttävätkö työntekijät suunnitelman uusien kelpousuusasetusten vaatimukset. 

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
