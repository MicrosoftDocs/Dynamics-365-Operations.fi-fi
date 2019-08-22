---
title: Ylläpidon määritetyypit
description: Tässä ohjeaiheessa kerrotaan, kuinka määritetyypit luodaan resurssien hallinnassa.
author: josaw1
manager: AnnBe
ms.date: 06/24/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3b3247f693f5934b3fbf83b7b831c7ed221514cb
ms.sourcegitcommit: 747bcd25ce7c6c20ce9eaa0027e730f74d4fd6aa
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 07/23/2019
ms.locfileid: "1783230"
---
# <a name="maintenance-attribute-types"></a>Ylläpidon määritetyypit

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

Tässä ohjeaiheessa kerrotaan, kuinka määritetyypit luodaan resurssien hallinnassa. Määritteiden avulla kuvataan eri elementtien ominaisuuksia. Voit määrittää määritteitä seuraaville elementeille:

- [Toiminnallisen sijainnin tyypit](../setup-for-functional-locations/functional-location-types.md)
- [Toiminnalliset sijainnit](../functional-locations/create-functional-locations.md)
- [Resurssityypit](../setup-for-objects/object-types.md)
- Resurssit

Määritteet, jotka voit määrittää, vaihtelevat elementin mukaan. Jos kyseessä on esimerkiksi toiminnallinen sijainti, voit määrittää sijainnin määrityksen ja sijainnin fyysisen koon määritteet. Voit määrittää resurssityypille tai resurssille määritteitä moottorin tilavuuteen, virrankulutukseen ja enimmäiskuormauskapasiteettiin eri olosuhteissa.

## <a name="create-attribute-types"></a>Luo ominaisuustyypit

Voit luoda omia määritetyyppejä. Lisäksi voit siirtää tuotedimensiot Microsoft Dynamics 365 for Finance and Operationsista **Määritetyypit**-sivulle.

1. Valitse **Resurssien hallinta** \> **Asetukset** \> **Määritetyypit**.
2. Kun määrität määrit tyyppejä ensimmäistä kertaa, valitse **Luo tuote dimensiot**, jos haluat siirtää vakio Finance and Operationsin tuotedimensiot automaattisesti.
3. Luo uusi määritetyyppi valitsemalla **Uusi**.
4. Kirjoita **Määritetyyppi**-kenttään määritetyypin nimi.
5. Syötä **Kuvaus**-kenttään kuvaus.
6. Valitse **Yksikkö**-kentässä asianmukainen määriteyksikkö tarpeen mukaan.
7. Valitse **Tietotyyppi**-kentässä yksikön tietotyyppi.
8. Jos olet valinnut tietotyypiksi **Merkkijono**, luo määritetyypille arvot noudattamalla seuraavia vaiheita:

    1. Valitse määritetyyppi ja valitse sitten **Arvot**.
    2. Valitse **Määritteen arvot**-kentässä **Uusi**.
    3. Valitse määritteen tyyppi (dimensio) **Määritteen tyyppi** -kentässä.
    4. Syötä liittyvä arvo **Arvo**-kentässä.
    5. Syötä **Kuvaus**-kenttään kuvaus.
    6. Tallenna tietue.
    7. Palaa **Määritetyypit** -sivulle.

9. Tallenna tietue.

    **Toiminnallisten sijaintien tyypit** -kentässä näkyy niiden toiminnallisten sijaintien määrä, jotka käyttävät määritetyyppiä. **Resurssityypit**-kentässä näkyy sitä käyttävien resurssityyppien määrä.
