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
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: eb45b79fa710699cfa267e7c6359ba3ce761d62d
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/04/2022
ms.locfileid: "8693224"
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
