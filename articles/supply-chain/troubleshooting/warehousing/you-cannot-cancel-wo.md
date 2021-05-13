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
ms.openlocfilehash: e5f6912cfb1d5be8e46b7989856af99f8a611c11
ms.sourcegitcommit: 5f5afb46431e1abd8fb6e92e0189914b598dc7fd
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/21/2021
ms.locfileid: "5924398"
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
