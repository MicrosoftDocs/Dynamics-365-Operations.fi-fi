---
title: Ylläpidon määritetyypit
description: Tässä artikkelissa kerrotaan, kuinka määritetyypit luodaan resurssien hallinnassa.
author: johanhoffmann
ms.date: 06/24/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage, EntAssetFunctionalLocationTypeCopy, EntAssetAttributeType, EntAssetAttributeTypeValue, EntAssetFunctionalLocationType
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5a0aca3ccf24505c064ad59f0adafb771056ba95
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8887657"
---
# <a name="maintenance-attribute-types"></a>Ylläpidon määritetyypit

[!include [banner](../../includes/banner.md)]

 

Tässä artikkelissa kerrotaan, kuinka määritetyypit luodaan resurssien hallinnassa. Määritteiden avulla kuvataan eri elementtien ominaisuuksia. Voit määrittää määritteitä seuraaville elementeille:

- [Toiminnalliset sijaintityypit](../setup-for-functional-locations/functional-location-types.md)
- [Luo toiminnalliset sijainnit](../functional-locations/create-functional-locations.md)
- [Resurssityypit](../setup-for-objects/object-types.md)
- Resurssit

Määritteet, jotka voit määrittää, vaihtelevat elementin mukaan. Jos kyseessä on esimerkiksi toiminnallinen sijainti, voit määrittää sijainnin määrityksen ja sijainnin fyysisen koon määritteet. Voit määrittää resurssityypille tai resurssille määritteitä moottorin tilavuuteen, virrankulutukseen ja enimmäiskuormauskapasiteettiin eri olosuhteissa.

## <a name="create-attribute-types"></a>Luo ominaisuustyypit

Voit luoda omia määritetyyppejä. Lisäksi voit siirtää tuotedimensiot **Määritetyypit**-sivulle.

1. Valitse **Resurssien hallinta** \> **Asetukset** \> **Määritetyypit**.
2. Kun määrität määritetyyppejä ensimmäistä kertaa, valitse **Luo tuotedimensiot** siirtääksesi vakiotuotedimensiot automaattisesti.
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


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]