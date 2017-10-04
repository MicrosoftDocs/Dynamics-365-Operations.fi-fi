---
title: Kustannusobjektit
description: "Tässä artikkelissa on tietoja kustannusobjekteista ja siitä, miten kustannukset ja määrät kerätään. Kustannusobjekti on yksikkö, johon kustannukset ja määrät kerätään. Kustannusobjektiyksiköt voivat olla tuotteita tai tuotevariantteja, kuten tyylin ja värin variantteja."
author: YuyuScheller
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventCostOnhandItem
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 19451
ms.assetid: ec776b98-813a-490d-848f-468452d98fac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-02-28T00:00:00.000Z
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 9262dcaa3b326d8c31b7d7416b102920795da94b
ms.openlocfilehash: 823d3edd106925339607d01fbf5f1921b85ff244
ms.contentlocale: fi-fi
ms.lasthandoff: 06/13/2017

---

# <a name="cost-objects"></a>Kustannusobjektit

[!include[banner](../includes/banner.md)]


Tässä artikkelissa on tietoja kustannusobjekteista ja siitä, miten kustannukset ja määrät kerätään. Kustannusobjekti on yksikkö, johon kustannukset ja määrät kerätään. Kustannusobjektiyksiköt voivat olla tuotteita tai tuotevariantteja, kuten tyylin ja värin variantteja.  

<a name="cost-objects"></a>Kustannusobjektit
------------

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

<a name="see-also"></a>Lisätietoja
--------

[Tuotedimensioryhmä](https://technet.microsoft.com/en-us/library/aa499382.aspx)

[Varastodimensioryhmä](https://technet.microsoft.com/en-us/library/hh209317.aspx)

[Seurantadimensioryhmä](https://technet.microsoft.com/en-us/library/hh209465.aspx)

[Uudet ja muuttuneet ominaisuudet](/dynamics365/unified-operations/dev-itpro/get-started/whats-new-changed)

[Kustannusmerkinnät](cost-entries.md)



