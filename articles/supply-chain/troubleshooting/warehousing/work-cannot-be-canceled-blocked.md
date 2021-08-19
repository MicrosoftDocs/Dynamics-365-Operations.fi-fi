---
title: Työtä ei voi peruuttaa, koska se on estetty.
description: Työtä ei voi peruuttaa, koska se on estetty.
author: perlynne
ms.date: 04/15/2021
ms.topic: troubleshooting
ms.search.form: WHSWorkTable_WHSWorkCancel
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-05-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: a24f199484c7596189b19e4cddf344e9186c6044edd2906affca9b530de44168
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/05/2021
ms.locfileid: "6722196"
---
# <a name="work-cant-be-canceled-because-its-blocked"></a>Työtä ei voi peruuttaa, koska se on estetty.

Virhekoodi: WHSCancellationOfWorkBlockedByExecutingWave_ErrorMessage

## <a name="symptoms"></a>Oireet

Järjestelmä näyttää seuraavan virhesanoman:

> Työtä %1 ei voi peruuttaa, koska se on syytyyppi %2 on estänyt sen. Työ on peruutettava, ennen kuin se voidaan peruuttaa.

## <a name="cause"></a>Syy

Työ on estetty eikä sitä voi peruuttaa.

**Työ**-sivun **Yleiset**-välilehdessä **Estetty**-kohdan asetuksena on *Kyllä*. Tämä asetus ilmaisee, että työ on estetty. **Eston syyt** -välilehdessä näkyy, miksi työ on estetty.

## <a name="resolution"></a>Ratkaisu

Voit poistaa työn eston valitsemalla **Eston syyt** -välilehden ja noudattamalla seuraavia vaiheita:

- Jos **Työn esto syy** -kentän arvoksi on määritetty *Määrittämätön syy*: Valitse toimintoruudun **Työ**-välilehden **Työ**-ryhmässä **Poista työn esto**.
- Jos **Työn esto syy** -kentän arvona on *Aallon käsittely*: Toimintoruudun **Aiheeseen liittyviä tietoja** -välilehden **Aiheeseen liittyviä tietoja** -ryhmässä valitse **Aalto**. Sitten **Aallot**-sivulla toimintoruudussa **Aalto**-välilehdessä **Aalto**-ryhmässä valitse **Tyhjennä aallon tiedot**.

## <a name="workaround"></a>Ongelman kiertäminen

Jos edelliset vaiheet eivät korjaa ongelmaa, voit peruuttaa työn noudattamalla seuraavia vaiheita.

1. Valitse **Varastonhallinta \> Kausittaiset tehtävät \> Tyhjennä \> Peruuta työ**.
1. Määritä **Työtunnus**-kentässä peruutettavan työn tunnus ja jonka **Työn tila** -arvona on *Avoinna*, *Käsittelyssä*, *Peruutettu*, *Yhdistetty* tai *Suljettu*.
1. Valitse **OK**.
1. Vahvista, että haluat peruuttaa työn valitsemalla **Kyllä**.

Lisätietoja on kohdassa [Varastotyön peruuttaminen poikkeuksen käsittelyä varten](../../warehousing/cancel-warehouse-work.md).
