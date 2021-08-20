---
title: Määrää ei voi vähentää, kun myyntitilaus peruutetaan
description: Määrää ei voi vähentää, kun myyntitilaus peruutetaan.
author: hja-ms
ms.date: 5/17/2021
ms.topic: troubleshooting
ms.search.form: SalesTable_SalesCancelOrder, SalesTableListPage_SalesCancelOrder
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: hja
ms.search.validFrom: 2021-05-17
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: f3453c83b5e8ead4269a6054167d73a0cd12381ba374b98bc407c01edaa68a1c
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/05/2021
ms.locfileid: "6752631"
---
# <a name="the-quantity-cant-be-reduced-when-a-sales-order-is-canceled"></a>Määrää ei voi vähentää, kun myyntitilaus peruutetaan

Virhekoodi: SYS138831

## <a name="symptoms"></a>Oireet

Järjestelmä näyttää seuraavan virhesanoman:

> Määrää ei voi vähentää. Tilauksen varastotapahtumien määrä on liian pieni, koska määrään tai sen osaan viitataan toimitustilauksessa tai tuotantotilauksessa tai se on merkitty muihin tapahtumiin.

## <a name="cause"></a>Syy

Jos myyntitilaukseen liittyy työtä, et voi peruuttaa myyntitilausta, ennen kuin työ peruutetaan ja palautetaan. Tämä vaatimus on pätee, vaikka myyntitilaukseen liittyvä työ olisi suljettu.

## <a name="resolution"></a>Ratkaisu

Voit korjata ongelman tekemällä seuraavat toimet:

1. Peruuta avoimet työt.
1. Poista kuorma.
1. Vähennä kerättyä määrää.

### <a name="cancel-open-work"></a>Peruuta avoimet työt

Voit peruuttaa avoimet työt seuraavasti.

1. Valitse **Varastonhallinta \> Kausittaiset tehtävät \> Tyhjennä \> Peruuta työ**.
1. Määritä **Työtunnus**-kentässä peruutettavan työn tunnus ja jonka **Työn tila** -arvona on *Avoinna*, *Käsittelyssä*, *Peruutettu*, *Yhdistetty* tai *Suljettu*.
1. Valitse **OK**.
1. Vahvista, että haluat peruuttaa työn valitsemalla **Kyllä**.

### <a name="delete-the-load"></a>Poista kuorma

Voit poistaa kuorman seuraavasti.

1. Valitse **Myynti ja markkinointi \> Myyntitilaukset \> Kaikki myyntitilaukset**.
1. Avaa asianmukainen myyntitilaus.
1. Valitse **Myyntitilausrivit**-pikavälilehdessä **Varasto \> Työn tiedot**.
1. Valitse **Työ**-sivun toimintoruudun **Työ**-välilehden **Työ**-ryhmässä **Peruuta työ**.
1. Vahvista, että **Työn tila** -kentän arvoksi on määritetty *Peruutettu*.
1. Sulje **Työ**-sivu.
1. Valitse myyntitilauksen tietosivun **Myyntitilausrivit**-pikavälilehdestä **Varasto \> Kuorman tiedot**.
1. Valitse toimintoruudussa **Poista**.
1. Vahvista, että haluat poistaa kuorman valitsemalla **Kyllä**.
1. Sulje **Kuorma**-sivu.

### <a name="reduce-the-picked-quantity"></a>Vähennä kerättyä määrää

Kun kaikki työt on peruutettu, pienennä keräysmäärää noudattamalla näitä ohjeita.

1. Valitse **Myynti ja markkinointi \> Myyntitilaukset \> Kaikki myyntitilaukset**.
1. Avaa asianmukainen myyntitilaus.
1. Valitse **Myyntitilausrivit**-pikavälilehdessä **Päivitä rivi \> Kerää** työkaluriviltä.
1. Valitse **Kerää**-sivun **Tapahtumat**-osasta rivi, jonka **Varasto-ottotila**-kentän arvoksi on määritetty *Kerätty*.
1. Valitse **Tapahtumat**-osassa **Lisää keräilyrivi** työkaluriviltä.
1. Valitse **Keräilyrivit**-osassa **Vahvista kaikkien keräily** työkaluriviltä.
1. Sulje **Kerää**-sivu.
1. Valitse myyntitilauksen tietosivun toimintoruudun **Myyntitilaus**-välilehden **Ylläpidä**-ryhmässä **Peruuta**.
1. Vahvista, että haluat peruuttaa myyntitilauksen valitsemalla **Kyllä**.
