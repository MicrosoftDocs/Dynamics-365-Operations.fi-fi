---
title: Käyttäjän työn peruuttaminen ei onnistu
description: Käyttäjän työn peruuttaminen ei onnistu
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
ms.openlocfilehash: 1d7b0140d0c2724234a549ca4dfb23109012654abe0e60fcea1f98e8f17c153a
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/05/2021
ms.locfileid: "6748688"
---
# <a name="you-cant-cancel-work-that-is-on-a-user"></a>Käyttäjän työn peruuttaminen ei onnistu

Virhekoodi: WAX708

## <a name="symptoms"></a>Oireet

Järjestelmä näyttää seuraavan virhesanoman:

> Et voi peruuttaa työtä, joka on käyttäjällä.

## <a name="cause"></a>Syy

Työ on käyttäjän lukitsema eikä sitä voi peruuttaa. Voit vahvistaa tämän avaamalla työtunnuksen ja avaamalla sitten **Yleiset**-välilehden. Jos työ on lukittu, **Työn tila** -kentän arvoksi määritetään *Käsittelyssä* ja **Lukitsija**-kenttään määritetään käyttäjätunnus.

## <a name="resolution"></a>Ratkaisu

Voit peruuttaa työn seuraavasti.

1. Valitse **Varastonhallinta \> Kausittaiset tehtävät \> Tyhjennä \> Peruuta työ**.
1. Määritä **Työtunnus**-kenttään peruutettavan työn tunnus.
1. Valitse **OK**.
1. Vahvista, että haluat peruuttaa työn valitsemalla **Kyllä**.

Lisätietoja on kohdassa [Varastotyön peruuttaminen poikkeuksen käsittelyä varten](../../warehousing/cancel-warehouse-work.md).
