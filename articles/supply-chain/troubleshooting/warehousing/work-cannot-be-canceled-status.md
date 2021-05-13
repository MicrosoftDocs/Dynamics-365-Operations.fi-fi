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
ms.openlocfilehash: 60b4da44ca5e6790302e0797640317cef8493db7
ms.sourcegitcommit: 5f5afb46431e1abd8fb6e92e0189914b598dc7fd
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/21/2021
ms.locfileid: "5924252"
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
