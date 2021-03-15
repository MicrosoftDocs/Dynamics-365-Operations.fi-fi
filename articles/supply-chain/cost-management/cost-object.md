---
title: Kustannusobjektit
description: Tässä artikkelissa on tietoja kustannusobjekteista ja siitä, miten kustannukset ja määrät kerätään. Kustannusobjekti on yksikkö, johon kustannukset ja määrät kerätään. Kustannusobjektiyksiköt voivat olla tuotteita tai tuotevariantteja, kuten tyylin ja värin variantteja.
author: AndersGirke
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventCostOnhandItem
audience: Application User
ms.reviewer: kamaybac
ms.custom: 19451
ms.assetid: ec776b98-813a-490d-848f-468452d98fac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 65a0f72f8d97bda36bacd691d545807c413f8825
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/15/2021
ms.locfileid: "4967655"
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





[!INCLUDE[footer-include](../../includes/footer-banner.md)]