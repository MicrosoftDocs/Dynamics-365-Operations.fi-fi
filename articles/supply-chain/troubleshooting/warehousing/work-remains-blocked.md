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
ms.openlocfilehash: 898390c78bb26fb8a44f77a10ad27a00720f7d1a3396cec5fff10e9d6b93364d
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/05/2021
ms.locfileid: "6768567"
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
