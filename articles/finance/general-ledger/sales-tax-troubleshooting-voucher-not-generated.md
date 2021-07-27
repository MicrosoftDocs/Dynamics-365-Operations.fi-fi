---
title: Tositetta ei luoda
description: Tämä ohjeaihe sisältää vianmääritystietoja, jotka voivat auttaa, kun tosite pitäisi luoda mutta niin ei tehdä.
author: qire
ms.date: 04/13/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: 82357b7fe00b93715f44eb024ac78d7cc1adca84
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 07/06/2021
ms.locfileid: "6356098"
---
# <a name="voucher-isnt-generated"></a>Tositetta ei luoda

[!include [banner](../includes/banner.md)]

Jos tosite pitäisi luoda, mutta **Tositetapahtumat**-sivulla ei ole tositteita, suorita tämän ongelman vianmäärityksessä tarvittavat seuraavien osien vaiheet.

[![Tositetapahtumat-sivu, jolla ei ole tositteita.](./media/voucher-not-generated-Picture1.png)](./media/voucher-not-generated-Picture1.png)

## <a name="check-the-tax-applicability"></a>Veron käytettävyyden tarkistus

1. Valitse **Vero** \> **Kausittaiset tehtävät** \> **Alareskontran kirjauskansioviennit, joita ei ole vielä siirretty**.
2. Jos kirjauskansiotietue on olemassa, valitse se ja valitse sitten **Siirrä nyt**.

    [![Siirrä nyt -painike Alareskontran kirjauskansioviennit, joita ei ole vielä siirretty -sivulla.](./media/voucher-not-generated-Picture2.png)](./media/voucher-not-generated-Picture2.png)

3. Avaa **Tositetapahtumat**-sivu uudelleen ja tarkista, onko tosite luotu.

## <a name="determine-whether-customization-exists"></a>Määritä, onko mukautus olemassa

Jos olet suorittanut edellisen osan vaiheet, mutta et ole löytänyt ongelmaa, selvitä, onko mukautus olemassa. Jos mukautusta ei ole, luo Microsoftin huoltopyyntö lisätuen saamiseksi.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
