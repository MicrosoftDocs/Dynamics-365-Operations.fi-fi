---
title: Työ on edelleen estetty
description: Työ on edelleen estetty
author: perlynne
ms.date: 04/15/2021
ms.topic: troubleshooting
ms.search.form: WHSWorkTableListPage_WHSWorkUnblocking
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-05-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: f85364d1ecfadc36b26c3395ab4402d3cb3b1603
ms.sourcegitcommit: 5f5afb46431e1abd8fb6e92e0189914b598dc7fd
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/21/2021
ms.locfileid: "5924127"
---
# <a name="work-remains-blocked"></a>Työ on edelleen estetty

Virhekoodi: WHSWorkBlockingExecutingWaveReason_ErrorMessage

## <a name="symptoms"></a>Oireet

Järjestelmä näyttää seuraavan virhesanoman:

> Työ %1 on edelleen estetty, koska liittyvän aallon %2 tila on %3.

## <a name="cause"></a>Syy

Työtä käsitellään parhaillaan aallossa eikä sen estoa voi poistaa, kuten jokin seuraavista ehdoista on osoittanut:

- **Eston syyt** -välilehdessä **Työn eston syy** -kentässä yhen tai usean rivin arvona on *Aallon käsittely*.
- Kun valitset **Aalto** **Aiheeseen liittyviä tietoja** -ryhmässä toimintoruudun **Aiheeseen liittyviä tietoja** -välilehdessä, **Aallon tila** -kentän arvoksi tulee *Käsitellään*.

## <a name="resolution"></a>Ratkaisu

Valitse toimintoruudun **Aiheeseen liittyviä tietoja**-välilehden **Aiheeseen liittyvät tiedot**-ryhmässä **Aalto**. Sitten **Aallot**-sivulla toimintoruudussa **Aalto**-välilehdessä **Aalto**-ryhmässä valitse **Tyhjennä aallon tiedot**.

## <a name="workaround"></a>Ongelman kiertäminen

Jos edelliset vaiheet eivät korjaa ongelmaa, voit peruuttaa työn noudattamalla seuraavia vaiheita.

1. Valitse **Varastonhallinta \> Kausittaiset tehtävät \> Tyhjennä \> Peruuta työ**.
1. Määritä **Työtunnus**-kentässä peruutettavan työn tunnus ja jonka **Työn tila** -arvona on *Avoinna*, *Käsittelyssä*, *Peruutettu*, *Yhdistetty* tai *Suljettu*.
1. Valitse **OK**.
1. Vahvista, että haluat peruuttaa työn valitsemalla **Kyllä**.

Lisätietoja on kohdassa [Varastotyön peruuttaminen poikkeuksen käsittelyä varten](../../warehousing/cancel-warehouse-work.md).
