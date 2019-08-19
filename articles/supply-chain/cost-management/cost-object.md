---
title: Kustannusobjektit
description: Tässä artikkelissa on tietoja kustannusobjekteista ja siitä, miten kustannukset ja määrät kerätään. Kustannusobjekti on yksikkö, johon kustannukset ja määrät kerätään. Kustannusobjektiyksiköt voivat olla tuotteita tai tuotevariantteja, kuten tyylin ja värin variantteja.
author: AndersGirke
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventCostOnhandItem
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 19451
ms.assetid: ec776b98-813a-490d-848f-468452d98fac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6501e8d809d12df421ad081662d23a6b5005f39c
ms.sourcegitcommit: 45f8cea6ac75bd2f4187380546a201c056072c59
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 07/12/2019
ms.locfileid: "1742133"
---
# <a name="cost-objects"></a>Kustannusobjektit

[!include [banner](../includes/banner.md)]

Tässä artikkelissa on tietoja kustannusobjekteista ja siitä, miten kustannukset ja määrät kerätään. Kustannusobjekti on yksikkö, johon kustannukset ja määrät kerätään. Kustannusobjektiyksiköt voivat olla tuotteita tai tuotevariantteja, kuten tyylin ja värin variantteja.  

## <a name="cost-objects"></a>Kustannusobjektit

**Kustannuskohde**-sivulla eritellään kaikki kustannuskohteet, jotka on rekisteröity tuotteeseen. Kustannuskohteet määritetään seuraavista lähteistä saaduilla tiedoilla:

-   Tuote
-   Tuotedimensioryhmä
-   Varastodimensioryhmä
-   Seurantadimensioryhmä

**Huomautus:** Kustannuskohde edustaa vain **Suorat Materiaalit** -tyypin kustannusryhmää. Kustannuskohde ja varastokohde eroavat sillä tavalla, että kustannuskohde määritetään varastodimensioiden mukaan, jotka valitaan taloudellista varastoa varten. Esimerkiksi, nimikkeellä on seuraava rakenne:

-   **Toimipaikka:** varastonmääritys = Kyllä, taloudellinen varasto = Kyllä
-   **Varasto:** varastonmääritys = Kyllä, taloudellinen varasto = Ei
-   **Eränumero:** varastonmääritys = Kyllä, taloudellinen varasto = Ei

Seuraavassa taulukossa näkyy mikä on kustannuskohde ja mikä on varastokohde.

| Objektityyppi      | Nimiketunnus | Sivusto | Varasto | Eränumero. |
|------------------|-------------|------|-----------|-----------|
| Kustannuskohde      | x           | x    |           |           |
| Varastokohde | x           | x    |  x        | x         |

## <a name="accumulation-of-costs-and-quantities"></a>Kustannusten ja määrien kasvu
-   Arvo **Arvo**-kentässä on seuraavien arvojen summa:
    -   Fyysinen kustannus
    -   Rahoituksellinen kustannus
    -   Oikaisut
-   Arvo **Määrä**-kentässä on seuraavien arvojen summa:
    -   Vastaanotettu
    -   Toimitettu
    -   Kirjattu määrä
-   **Keskimääräinen yksikkökustannus**-kenttä on laskettu kenttä. Arvo lasketaan jakamalla **Arvo**-arvo **Määrä**-arvolla.

**Huomautus:** **Sisällytä fyysinen arvo** -parametri ei vaikuta edellisiin laskelmiin.

<a name="additional-resources"></a>Lisäresurssit
--------

[Tuotedimensioryhmä](https://technet.microsoft.com/library/aa499382.aspx)

[Varastodimensioryhmä](https://technet.microsoft.com/library/hh209317.aspx)

[Seurantadimensioryhmä](https://technet.microsoft.com/library/hh209465.aspx)

[Uudet ja muuttuneet ominaisuudet](../../fin-and-ops/get-started/whats-new-changed.md)

[Kustannusmerkinnät](cost-entries.md)



