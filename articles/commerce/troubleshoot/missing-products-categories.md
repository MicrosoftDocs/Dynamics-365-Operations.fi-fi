---
title: Tuotteita ja luokkia puuttuu ympäristön kopioinnin jälkeen
description: Tämä ohjeaihe antaa vianmääritysohjeet, jotka voivat auttaa, kun tuotteet ja luokat puuttuvat, kun sivusto on kopioitu eri ympäristöstä tai samassa ympäristössä.
author: Reza-Assadi
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rassadi
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 4964b9623a91286d4f8260bcae7941feb48f8962
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/11/2021
ms.locfileid: "6022395"
---
# <a name="products-and-categories-missing-after-environment-copy"></a>Tuotteita ja luokkia puuttuu ympäristön kopioinnin jälkeen

[!include [banner](../../includes/banner.md)]

Tämä ohjeaihe antaa vianmääritysohjeet, jotka voivat auttaa, kun tuotteet ja luokat puuttuvat, kun sivusto on kopioitu eri ympäristöstä tai samassa ympäristössä.

## <a name="description"></a>kuvaus

Kun sivusto on kopioitu ympäristöstä toiseen tai samassa ympäristössä, tuotteet ja luokat puuttuvat sivustosta. Tuotteet ja luokat puuttuvat verkkokaupasta ja Commercen sivuston luontiohjelman **Tuotteet**-välilehdestä.

## <a name="resolution"></a>Ratkaisu

### <a name="map-the-channel-operating-unit-number-to-a-newly-copied-site-in-commerce-site-builder"></a>Kanavan toimintayksikkönumeron määritys juuri kopioituun sivustoon Commercen sivuston luontiohjelmassa

Voit määrittää kanavan toimintayksikkönumeron (OUN) juuri kopioituun sivustoon Commercen sivuston luontiohjelmassa toimimalla seuraavasti.

1. Valitse juuri kopioitu sivusto.
1. Valitse **Sivuston asetukset** -kohdassa **Kanavat**.
1. Valitse kanavan nimen vieressä kolme pistettä (**...**) ja valitse sitten **Vaihda verkkokaupan kanava**.
1. Valitse **Vaihda verkkokaupan kanava** -valintaikkunassa kanava, johon haluat yhdistää juuri kopioidun sivuston, ja valitse sitten **OK**.
1. Valitse **Tallenna ja julkaise**.

## <a name="additional-resources"></a>Lisäresurssit

[Dynamics 365 Commerce -sivuston liittäminen online-kanavaan](../associate-site-online-store.md)
