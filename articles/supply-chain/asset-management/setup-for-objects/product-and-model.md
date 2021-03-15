---
title: Resurssien valmistajat ja mallit
description: Tässä ohje aiheessa kerrotaan, kuinka voit määrittää resurssin valmistajat ja niihin liittyvät mallit resurssien hallinnassa.
author: josaw1
manager: tfehr
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage, EntAssetProductLookup, EntAssetModelLookup, EntAssetProduct
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a1eca3112b95bc7d1a049f101fc1d461272a63aa
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/16/2021
ms.locfileid: "5022253"
---
# <a name="asset-manufacturers-and-models"></a>Resurssien valmistajat ja mallit

[!include [banner](../../includes/banner.md)]

 

Tässä ohje aiheessa kerrotaan, kuinka voit määrittää resurssin valmistajat ja niihin liittyvät mallit resurssien hallinnassa. Mallit voivat liittyä resurssityyppeihin.

## <a name="set-up-product-model-relations"></a>Määritä tuote-malli-suhteet

1. Valitse **Resurssien hallinta**\>**Asetukset** \> **Resurssit** \> **valmistaja ja malli**. 
2. Luo uusi tuote valitsemalla **Uusi**.
3. Syötä **Valmistaja**-kenttään resurssin valmistajan nimi.
4. Syötä **Kuvaus**-kenttään kuvaus.
5. Valitse **Mallit**-pikavälilehdellä **Lisää** luodaksesi resurssimallin, joka liittyy resurssin valmistajaan.
6. Syötä **Malli**-kenttään resurssin mallin nimi.
7. Syötä **Kuvaus**-kenttään kuvaus.
8. Valitse **Resurssityyppi**-kentässä resurssityyppi, johon valmistajan mallin tulisi liittyä.

    > [!NOTE]
    > Voit myös määrittää resurssityyppien, valmistajien ja mallien suhteet **Resurssityypit**-haussa. Lisätietoja on kohdassa [Resurssityypit](../setup-for-objects/object-types.md).

    **Tiedot**-pikavälilehdessä **Mallit**-kentässä näkyy valitulle resurssin valmistajalle asetettujen resurssin mallien määrä. **Resurssit**-kenttä näyttää niiden resurssien määrän, jotka käyttävät valittua valmistajaa.
    
    **Resurssit**-kenttä näyttää niiden objektien määrän, jotka käyttävät valittua mallia.

> [!NOTE]
> Resurssityypillä ei voi olla resurssin valmistajan mallin suhteita, se voi liittyä yhteen resurssin valmistajan malliin tai se voi liittyä useisiin resurssin valmistajan malleihin. Jos resurssin tyyppi liittyy vähintään yhteen valmistajan malliin, vain ne yhdistelmät, jotka on määritetty **Valmistajan malli** -haussa, voidaan valita kyseisillä resurssien hallintasivuilla, joilla resurssityypin, valmistajan ja mallin yhdistelmä voidaan määrittää. Näitä sivuja ovat **Kaikki resurssit**, **Resurssien palvelutasot** **Oletustyötyypit** ja **Ylläpitobudjetin rivit**. Jos jotkin resurssityypit eivät liity mihinkään valmistajan malliin, sivuilla näkyvät vain ne resurssityypit ja valmistajan mallit, joilla ei myöskään ole suhdetta resurssityyppeihin.

## <a name="select-a-manufacturer-and-model-on-an-object"></a>Valitse objektin valmistaja ja malli

1. Valitse **Resurssien hallinta** \> **Yhteiset** \> **Resurssit** \> **Kaikki resurssit**.
2. Valitse **Resurssi**-sarakkeessa resurssin linkki. Näyttöön tulee **Tiedot** -sivu.
3. Valitse **Muokkaa**.
4. Valitse **Yleiset**-pikavälilehdessä **valmistaja**- ja **Malli**-kenttien arvot.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]