---
title: Työtä ei voi peruuttaa sen tilan vuoksi
description: Työtä ei voi peruuttaa sen tilan vuoksi
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
ms.openlocfilehash: f983501b490c5516525b4d5904603ed62e8799f9e6124e5672b36a12804ecb0a
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/05/2021
ms.locfileid: "6755975"
---
# <a name="work-cant-be-canceled-because-of-its-status"></a>Työtä ei voi peruuttaa sen tilan vuoksi

Virhekoodi: WAX2190

## <a name="symptoms"></a>Oireet

Järjestelmä näyttää seuraavan virhesanoman:

> Et voi peruuttaa työtä %1, koska sen tila on %2.

## <a name="cause"></a>Syy

Työtä ei voi peruuttaa nykyisessä tilassaan.

Työotsikolla tai työriveillä ei ole odotettua **Työn tila** -arvoa. Työotsikon **Työn tila** -kentän arvoksi ei ole määritetty *Avoin* tai *Käsittelyssä*.

## <a name="resolution"></a>Ratkaisu

Voit peruuttaa työn seuraavasti.

1. Valitse **Varastonhallinta \> Kausittaiset tehtävät \> Tyhjennä \> Peruuta työ**.
1. Määritä **Työtunnus**-kenttään peruutettavan työn tunnus.
1. Valitse **OK**.
1. Vahvista, että haluat peruuttaa työn valitsemalla **Kyllä**.

Lisätietoja on kohdassa [Varastotyön peruuttaminen poikkeuksen käsittelyä varten](../../warehousing/cancel-warehouse-work.md).
