---
title: Viimeisen suljetun työrivin on oltava määritys
description: Viimeisen suljetun työrivin on oltava määritys
author: perlynne
ms.date: 04/15/2021
ms.topic: troubleshooting
ms.search.form: WHSWorkTable_WHSWorkCancel, WHSWorkTableListPage_WHSWorkCancel
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-05-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: a5b78154b51252b3ac96ba28c254e823caf87019
ms.sourcegitcommit: 5f5afb46431e1abd8fb6e92e0189914b598dc7fd
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/21/2021
ms.locfileid: "5924372"
---
# <a name="the-last-closed-work-line-must-be-a-put"></a>Viimeisen suljetun työrivin on oltava määritys

Virhekoodi: WAX1285

## <a name="symptoms"></a>Oireet

Järjestelmä näyttää seuraavan virhesanoman:

> Viimeisen suljetun työrivin on oltava määritys.

## <a name="cause"></a>Syy

Työtä ei voi peruuttaa nykyisessä tilassaan.

Viimeisellä työrivillä **Työn tila** -kentän arvona on *Suljettu*, mutta **Työtyypi**-kentän arvona ei ole *Määritys*.

## <a name="resolution"></a>Ratkaisu

Voit peruuttaa työn seuraavasti.

1. Valitse **Varastonhallinta \> Kausittaiset tehtävät \> Tyhjennä \> Peruuta työ**.
1. Määritä **Työtunnus**-kenttään peruutettavan työn tunnus.
1. Valitse **OK**.
1. Vahvista, että haluat peruuttaa työn valitsemalla **Kyllä**.

Lisätietoja on kohdassa [Varastotyön peruuttaminen poikkeuksen käsittelyä varten](../../warehousing/cancel-warehouse-work.md).
